---
title: Projektplanlægningens API-ydeevne
description: Denne artikel indeholder oplysninger om benchmarks for projektplanlægnings-API'ernes ydeevne og identificerer bedste praksis for optimal anvendelse.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911175"
---
# <a name="project-schedule-api-performance"></a>Projektplanlægningens API-ydeevne

_**Gælder for:** Project Operations til ressource/ikke-lagerbaserede scenarier, Lille udrulning – aftale om proformafakturaren, Project for the web_

Denne artikel indeholder oplysninger om benchmarks for ydeevnen for grænseflader til programmering af apps (API'er) i forbindelse med projektplanlægning og identificerer den bedste praksis for optimal anvendelse.

## <a name="project-scheduling-service"></a>Projektplanlægningstjeneste
Projektplanlægningstjenesten er en tjeneste på flere lejere, som kører i Microsoft Azure. Den er udviklet til at forbedre interaktionen ved at give brugerne en hurtig oplevelse, når de arbejder på projekter. Disse forbedringer opnås ved at acceptere ændringsanmodninger, behandle dem og derefter straks returnere resultatet. Tjenesten forbliver asynkron i Dataverse og forhindrer ikke brugere i at udføre andre handlinger.

API'erne for projektplanlægning er afhængige af, at projektplanlægningstjenesten kører forespørgsler, hvilket er beskrevet mere detaljeret senere i denne artikel.

API'erne for projektplanlægning er udviklet til at kunne arbejde sammen med følgende objekter i arbejdsopgavehierarkiet (WBS):

  - Project
  - Projektopgave
  - Projektopgaveafhængighed
  - Medlem af projektteam
  - Ressourcetildeling
  
Både standardfelterne og de brugerdefinerede felter understøttes. Medmindre andet er angivet, understøttes alle almindelige handlinger såsom oprettelse, opdatering og sletning. Du kan finde flere oplysninger i [Brug API'er for projektplanlægning til at udføre handlinger og planlægge objekter](schedule-api-preview.md).

Som en del af API'erne for projektplanlægning er der tilføjet et arbejdsenhedsmønster. Dette mønster kaldes et OperationSet, og det kan bruges, når flere forespørgsler skal behandles i en enkelt transaktion.

I følgende illustration vises det flow, som en partner vil opleve, når denne funktion bruges.

![Dataverse og projektplanlægningstjenesteflow.](./media/dataverse-project-scheduling-service-flow.png)

**Trin 1**: En klient foretager et API-opkald til et Open Data Protocol-slutpunkt (OData) i Dataverse for at oprette et OperationSet.

**Trin 2**: Når det nye OperationSet er oprettet, returneres værdien **OperationSetId**. 

**Trin 3**: Klienten bruger værdien **OperationSetId** til at foretage en anden API-forespørgsel i projektplanlægning. Resultatet er en oprettelse, opdatering eller sletning af anmodninger for et planlægningsobjekt. Når denne anmodning er foretaget, udføres der validering af metadata. Hvis valideringen ikke lykkes, afsluttes anmodningen, og der returneres en fejl.

**Trin 4a-4c**: Disse trin repræsenterer fasen ACCEPTÉR. Klienten kalder API'en **ExecuteOperationSetV1**, som sender alle ændringerne af projektplanlægningstjenesten i én batch. Projektplanlægningstjenesten kører sine egne valideringer på forespørgsler i batchen. Eventuelle valideringsfejl fortryder batchen og returnerer en undtagelse til den kaldende. Hvis batchen accepteres af projektplanlægningstjenesten, opdateres status for OperationSet, så den afspejler, at OperationSet behandles af projektplanlægningstjenesten.

**Trin 5**: Dette trin repræsenterer fasen BESTÅ. Projektplanlægningstjenesten skriver asynkront batchen til Dataverse i en transaktion. Hvis skrivehandlingen lykkes, er OperationSet markeret som **Fuldført**. Eventuelle fejl annullerer transaktionen og batchen, og OperationSet markeres som **Mislykket**.

## <a name="performance-methodology"></a>Metode for ydeevne
Udførelsestid defineres som tiden fra opkaldet til API'en **ExecuteOperationSetV1**, indtil projektplanlægningstjenesten er færdig med at skrive til Dataverse. Alle handlinger kører i alt 2.200 gange, og P99-tidsmålene rapporteres. Der måles enkeltpost- og massehandlinger.

Ved en handling med en enkelt post indeholder OperationSet én anmodning. I forbindelse med massehandlinger indeholder det 20, 50 eller 100 forespørgsler. Hver massestørrelse rapporteres særskilt.

Disse handlinger køres på en lille udrulning af UR 15 Project Operations i Nordamerika.

## <a name="results"></a>Resultater
### <a name="create-operations"></a>Opret handlinger
#### <a name="single-record-create-operations"></a>Handlinger til oprettelse af en enkelt post
I følgende tabel vises udførelsestiden for oprettelsen af en enkelt post. Tiderne er angivet i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Post&nbsp;&nbsp;&nbsp;type</th>
    <th class="tg-0lax" colspan="2">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle understøttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Opgave</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tildeling</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlemmer</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Afhængighed</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Handlinger for masseoprettelse
I følgende tabel vises udførelsestiden for oprettelsen af mange poster. Microsoft har specifikt målt udførelsestiderne for oprettelsen af 20, 50 og 100 poster i et enkelt OperationSet. Tiderne er angivet i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Post&nbsp;&nbsp;&nbsp;type</th>
    <th class="tg-0lax" colspan="6">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 poster</th>
    <th class="tg-0lax" colspan="2">50 poster</th>
    <th class="tg-0lax" colspan="2">100 poster</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle understøttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle understøttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle understøttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opgave</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tildeling</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Afhængighed</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Handlinger til masseoprettelse i objekterne **Projekt** og **Teammedlemmer** medtages ikke i denne tabel, da kørslen af disse handlinger ligner kørslen, når API'en til oprettelse af en enkelt post kaldes flere gange. Disse API'er køres straks i Dataverse.

I følgende illustration vises en afbildning af udførelsestiderne for objekterne **Opgave**, **Tildeling** og **Afhængighed**, når der oprettes 20, 50 og 100 poster, og alle understøttede felter bruges.

![Opret diagram over udførelsestid for poster.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Opdater handlinger
#### <a name="single-record-update-operations"></a>Handlinger til opdatering af en enkelt post
I følgende tabel vises udførelsestiden for opdatering af en enkelt post. Tiderne er angivet i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Post&nbsp;&nbsp;&nbsp;type</th>
    <th class="tg-0lax" colspan="2">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter </th>
    <th class="tg-0lax">Alle understøttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Opgave</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlemmer</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Opdateringshandlinger på objekterne **Ressourcetildelinger** og **Projektopgaveafhængighed** understøttes ikke.

#### <a name="bulk-update-operations"></a>Handlinger for masseopdatering
I følgende tabel vises udførelsestiden for opdateringer af mange poster. Microsoft har specifikt målt udførelsestiderne for opdateringer af 20, 50 og 100 poster i et enkelt OperationSet. Tiderne er angivet i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Post&nbsp;&nbsp;&nbsp;type</th>
    <th class="tg-0lax" colspan="6">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 poster</th>
    <th class="tg-0lax" colspan="2">50 poster</th>
    <th class="tg-0lax" colspan="2">100 poster</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle understøttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle understøttede felter</th>
    <th class="tg-0lax">Obligatoriske felter</th>
    <th class="tg-0lax">Alle understøttede felter</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opgave</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlemmer</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Opdateringshandlinger på objekterne **Ressourcetildelinger** og **Projektopgaveafhængighed** understøttes ikke.

I følgende illustration vises en afbildning af udførelsestiderne for objekterne Opgave og Teammedlem, når der opdateres 20, 50 og 100 poster, og alle understøttede felter bruges.

![Opdater diagram over udførelsestid for poster.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Slettehandlinger
#### <a name="single-record-delete-operations"></a>Handlinger til sletning af en enkelt post
I følgende tabel vises udførelsestiden for sletning af en enkelt post. Tiderne er angivet i sekunder.

| Posttype | Tid  |
|-------------|-------|
| Opgave        | 20.12 |
| Tildeling  | 10.86 |
| Teammedlemmer | 12.52 |
| Afhængighed  | 20.89 |

> [!NOTE]
> Sletningshandlinger for objektet **Projekt** understøttes ikke.

#### <a name="bulk-delete-operations"></a>Massesletningshandlinger
I følgende tabel vises udførelsestiden for sletningen af mange poster. Microsoft har specifikt målt udførelsestiderne for sletningen af 20, 50 og 100 poster i et enkelt OperationSet. Tiderne er angivet i sekunder.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Post&nbsp;&nbsp;&nbsp;type</th>
    <th class="tg-0lax" colspan="3">Tid</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 poster</th>
    <th class="tg-0lax">50 poster</th>
    <th class="tg-0lax">100 poster</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opgave</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tildeling</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammedlemmer</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Afhængighed</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Sletningshandlinger for objektet **Projekt** understøttes ikke.

I følgende illustration vises en afbildning af udførelsestiderne for objekterne **Opgave**, **Tildeling** og **Teammedlem** og **Afhængighed**, når der slettes 20, 50 og 100 poster.

![Slet diagram over udførelsestid for poster.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observationer
For hver posthandling bruger API'en **ExecuteOperationSet** ca. 800 millisekunder til at sende en anmodning til projektplanlægningstjenesten. Projektplanlægningstjenesten tager derefter ca. fem sekunder om at behandle nyttedataene og foretage opkald til Dataverse. Resten af udførelsestiden bruges på at køre forretningslogik og skrive data til databasen i Dataverse.

Når der oprettes, opdateres eller slettes 100 poster, tager API'en **ExecuteOperationSet** ca. tre sekunder om at sende anmodningen til projektplanlægningstjenesten. Projektplanlægningstjenesten tager derefter ca. fem sekunder om at behandle anmodningerne og foretage opkald til Dataverse. Massehandlinger skal betale en **Projektplanlægningsserviceafgift** én gang for alle posterne i OperationSet. Massehandlinger har derfor en betydeligt lavere gennemsnitlig udførelsestid end handlinger med en enkelt post.

## <a name="scenarios"></a>Scenarier
I følgende tabel vises udførelsestiderne, når API'er for projektplanlægning bruges til at udføre bestemte scenarier. Tiderne er angivet i sekunder.

| Scenarie                                                                   | Tid  |
|----------------------------------------------------------------------------|-------|
| Opret et projekt med 40 opgaver.                                      | 36.01 |
| Opret et projekt, der har 40 opgaver og 20 afhængigheder.                  | 38.11 |
| Opret et projekt, der har 40 opgaver og 30 tildelinger.                   | 60.17 |
| Opret et projekt, der har 40 opgaver, 20 afhængigheder og 30 tildelinger. | 60.27 |

## <a name="best-practices"></a>Bedste praksis
På baggrund af resultaterne fra det foregående scenario har API'erne en bedre ydeevne under følgende betingelser:

  - Gruppér så mange handlinger som muligt. Den gennemsnitlige kørsel for massehandlinger er bedre end den gennemsnitlige kørsel for handlinger med en enkelt post. Jo mindre antallet af OperationSets, der er i brug, er, jo hurtigere vil den gennemsnitlige udførelsestid være.
  - Angiv kun de minimumattributter, der kræves for at opnå scenariet. Vær omhyggelig med at vælge de ikkekrævede felter, som er inkluderet i en OperationSet-anmodning. Felter, der indeholder fremmede nøgler eller akkumuleringsfelter, påvirker ydeevnen negativt.
