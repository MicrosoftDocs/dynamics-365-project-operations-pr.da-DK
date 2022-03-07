---
title: Estimer projektsalg og -omkostninger, når en reserverbar ressource udfylder flere roller i et projekt
description: I dette emne forklares det, hvordan du kan bruge prisfastsættelsesdimensioner til at understøtte prisfastsættelses- og omkostningsestimater for en ressource, der udfylder flere roller i et projekt.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28a67e79b03dfbc38e9786350c931838ef27891a3d26787fc0334e0572528228
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990129"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimer projektsalg og -omkostninger, når en reserverbar ressource udfylder flere roller i et projekt 

_**Gælder for:** Project Operations for ressource/ikke-lagerbaserede scenarier, lille udrulning - aftale om proformafakturering og Project Operations for lagerbaserede/produktionsbaserede scenarier_ 

Projektbaserede virksomheder har ofte brug for, at en ressource udfylder flere roller på et projekt. Hver rolle kan være prisfastsat og omkostningsfastsat forskelligt. Dette betyder, at den samme ressources tid på et projekt kan få et andet økonomisk estimat, afhængigt af fakturerings- og omkostningssatserne for de enkelte roller. Du kan konfigurere værdierne for teammedlemsposten for den navngivne ressource med forskellige tilsidesættelser på hver af de opgaver, som teammedlemmet er tilknyttet.

I følgende eksempel gennemgås det, hvordan en simpel tilsidesættelse af en værdi gør det muligt for en ressource at have flere roller på et projekt med forskellige omkostnings- og faktureringssatser.

## <a name="create-tasks"></a>Opret opgaver
For at oprette opgaver skal du tilføje opgaver samt oversigtsopgaver, hvorefter du skal tildele opgaven, før du tilføjer opgavevarighed. 

### <a name="add-tasks-and-summary-tasks"></a>Tilføj opgaver og oversigtsopgaver
For at tilføje en opgave skal du fuldføre følgende fremgangsmåde.

1. Gå til **Projekter**, og åbn det projekt, du vil tilføje opgaver til.
2. Vælg **Tilføj ny opgave**. Navngiv opgaven, og tryk derefter på **Enter**.
3. Angiv et andet opgavenavn, og tryk derefter på **Enter**. Gentag dette, indtil du har en komplet liste over opgaver.
3. Hvis du vil indrykke opgaver under **Oversigtsopgaver**, skal du markere de tre lodrette punkter ud for opgavenavnet og derefter vælge **Opret under opgave**. 

  > [!TIP]
  > Hvis du vil markere mere end én opgave, skal du vælge en opgave, trykke på og holde **CTRL** nede og derefter vælge en anden opgave.
  >
  > Du kan også vælge **Opgrader underopgave** for at flytte opgaver væk fra **Oversigtsopgaver**.

### <a name="assign-tasks"></a>Tildel opgaver

For at tildele opgaver skal du fuldføre følgende fremgangsmåde.

1. I en opgaves kolonne med **Tildelt til** skal du vælge personens ikon.
2. Vælg et teammedlem fra listen, eller skriv en tekst for at søge efter et navn.

### <a name="add-task-duration-and-columns"></a>Tilføj opgavevarighed og kolonner

Det er ofte nemmest at begynde opbygningen af dit projekt med varigheden. For at tilføje en opgavevarighed skal du fuldføre følgende fremgangsmåde.

1. I en opgaves kolonne med **Varighed** skal du angive det antal dage, det skal tage at udføre opgaven. Hvis du vil bruge en anden tidsenhed, skal du skrive et tal plus ordet **timer**, **uger** eller **måneder**.
2. Hvis opgaven skal vises som en diamantformet milepæl i visningen **Tidslinje**, skal du i kolonnen for **Varighed** skrive **0 dage**.
3. Tryk på **Enter** for at gå til feltet med den næste opgaves **Varighed**, og fortsæt med at angive varigheder.

  > [!NOTE]
  > Du kan ikke angive en varighed for oversigtsopgaver.

Du kan tilføje kolonner til projektet for at angive flere oplysninger. Det kan du gøre ved at vælge **Tilføj kolonne**. 

Du kan finde flere oplysninger under [Opret et projekt](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Konfigurer rollen og organisationsenheden for et generelt projektteammedlem
Benyt følgende fremgangsmåde for at konfigurere en rolle og en organisationsenhed for et generelt teammedlem.

1. På siden **Opgaver** skal du vælge rækken **Opgave** for **Opgave A**. 
2. I **Tildelt til** skal du vælge **Tilføj standardressource**. Derved åbnes siden **Hurtig oprettelse for teammedlem**.
3. På siden **Hurtig oprettelse af teammedlem** skal du angive attributterne for det generiske teammedlem, der kan udføre denne opgave.
4. Vælg den relevante rolle og afdeling, og vælg derefter **Gem og luk**. Der oprettes et generisk gruppemedlem, og medlemmet tildeles til denne opgave. 
5. Gentag trin 1-4 for **Opgave B**. **Opgave B** skal dog have tildelt en anden rolle og organisatorisk enhed for det generelle gruppemedlem end **Opgave A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Konfigurer rollen og organisationsenheden for en projektopgave
Benyt følgende fremgangsmåde for at konfigurere en rolle og en organisationsenhed for en opgave.

1. Når du har oprettet **Opgave A**, skal du markere opgaven og derefter vælge ikonet **i** for at åbne ruden **Opgavedetaljer**. 
2. I ruden **Opgavedetaljer** skal du rulle ned i bunden og vælge **Vis detaljer** for at åbne siden **Opgavedetaljer**.
3. På siden **Opgavedetaljer** skal du for **Rolle** og **Organisationsenhed** tilføje de værdier, der kræves for at udføre denne opgave for ressourcen. 

  > [!NOTE]
  > Hvis du fuldfører dette scenario ved hjælp af demonstrationsdata fra Project Operations, skal du vælge **Konsulterende kundeemne** for rollen og **Fabrikam US** som organisationsenhed.

4. Vælg **Opgave B**, og vælg derefter opgaven.
5. Vælg ikonet **i** for at åbne ruden **Opgavedetaljer**. 
6. I ruden **Opgavedetaljer** skal du rulle ned i bunden og vælge **Vis detaljer** for at åbne siden **Opgavedetaljer**.
7. På siden **Opgavedetaljer** skal du for **Rolle** og **Organisationsenhed** tilføje de værdier, der kræves af en ressource, som skal udføre denne opgave. Værdierne i **Rolle** og **Organisationsenhed** for **Opgave B** skal være forskellige fra dem, der er angivet for **Opgave A**. 

  > [!NOTE]
  > Hvis du fuldfører dette scenario ved hjælp af demonstrationsdata fra Project Operations, skal du vælge **Netværkstekniker** for rollen og **Fabrikam US** som organisationsenhed.

8. Gem og luk, og vælg siden **Opgavedetaljer**. 

## <a name="team-member-and-estimates-behavior"></a>Funktionsmåde for teammedlemmer og estimater 
Hvis du vil forstå funktionsmåden for gitteret **Teammedlem** og estimaterne, skal du benytte følgende fremgangsmåde.

1. I gitteret **Teammedlem** skal du vælge de to generelle teammedlemmer og derefter vælge **Generer behov**. Dette vil generere ressourcekrav. 
2. Vælg teammedlemmets række for **Konsulterende kundeemne**, og vælg derefter **Reserver**. Planlægningsområdet åbnes med en liste over ressourcer. Vælg en ressource, og vælg derefter **Reserver** for at reservere den ressource, der passer til behovet.
3. Vælg teammedlemmets række for **Netværkstekniker**, og vælg derefter **Reserver**. Planlægningsområdet åbnes med en liste over ressourcer. Vælg den samme ressource som ovenfor, og vælg derefter **Reserver** for at reservere den ressource, der passer til behovet.

### <a name="team-member-grid"></a>Teammedlemsgitter 

I gitteret **Teammedlem** slettes de to generiske teammedlemsposter og erstattes med kun én ressource. Der er ét sæt værdier for denne ressource, som er et standardsæt af værdier for **Rolle** og **Organisationsenhed**.

Når du udvider rækken for den pågældende teammedlemspost, kan du se de forskellige tildelinger i teammedlemsposten for begge opgaver. Hver tildelingsrække har opgavespecifikke værdier for **Rolle** og **Afdeling**. 

### <a name="estimates-grid"></a>Gitter til estimater 

I gitteret **Estimater** prisfastsættes begge tildelinger for samme ressource forskelligt. Tildelingen for ressourcen på **Opgave A** er prisfastsat ved hjælp af attributværdien **Rolle** for **Konsulterende kundeemne**. Tildelingen for den samme ressource på **Opgave B** er prisfastsat ved hjælp af attributværdien **Rolle** for **Netværkstekniker**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]