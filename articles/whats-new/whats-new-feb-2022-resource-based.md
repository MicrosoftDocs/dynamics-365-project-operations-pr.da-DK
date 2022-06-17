---
title: Nyheder februar 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i februar 2022-udgivelsen af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932979"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder februar 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

*Finder anvendelse for: Project Operations for ressource-/ikke-lagerbaserede scenarier*

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.28.0.120
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.24

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

- I denne version kan du tilføje op til 300 teammedlemmer på et enkelt projekt. Tidligere var grænsen for antallet af teammedlemmer 150. Du kan finde flere oplysninger under [Projektbegrænsninger](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Opdatering af tilknytning af dobbeltskrivning i Project Operations

På følgende liste vises de tilknytninger med dobbelt skrivning, der er ændret eller tilføjet i Project Operations-versionen fra februar 2022.

| Objekttilknytning | Opdateret version | Kommentarer |
| --- | --- | --- |
| Integrationsobjekt for eksport af projektudgifter i Project Operations (msdyn\_expenses) | 1.0.0.3 | Udvidet til synkronisering af projektaktiviteter til Dataverse. |

Du kan se den aktuelle liste og de aktuelle versioner af tilknytninger med dobbelt skrivning under [Project Operations-versioner med tilknytning med dobbelt skrivning](../environment/resource-dual-write-maps.md).

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2415109 | Standardværdien i feltet **Betalingsbetingelser for drift** skal være projektkontraktkundeposten og proformafakturaposten. |
| Fakturering og prisfastsættelse | 2497369 | Væsentlig rettelse skal følge datoværdien i parametrene **Rettelse**. |
| Fakturering og prisfastsættelse | 2498697 | Forbedret sikkerhedskonfigurationen for **Tilbagekaldelse af tidsregistrering**. |
| Fakturering og prisfastsættelse | 2513824 | I ressourcebaserede scenarier må transaktionskategori-id'et ikke være mere end 28 tegn i Project Operations. |
| Fakturering og prisfastsættelse | 2517455 | Handlingen **Opdater fakturalinjetransaktioner** må ikke udløses flere samtidige gange for den samme faktura. |
| Fakturering og prisfastsættelse | 2517465 | Handlingen **Deaktiver fakturalinjedetaljer** blokeres, fordi den ikke understøttes. |
| Fakturering og prisfastsættelse | 2556660 | Løste problemet med kontrollen af datoeffektivitet, der foretages på den prisliste, som er knyttet til en projektparameterpost. |
| Styring af salgsmuligheder | 2369202 | Korrigerede den forretningslogik, der kontrollerer, at prislister med overlappende ikrafttrædelsesdatoer kan knyttes til den samme projektkontrakt. |
| Styring af salgsmuligheder | 2385965 | Korrigerede funktionsmåden under fanen **Kunder** på siden **Projektkontrakt**, når du vælger **Gem og luk**. |
| Tid og udgift | 2538503 | En projektopgave skal være tilgængelig i objektet **Faktiske projektværdier**, når en udgiftsrapport bogføres. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Project Management and Accounting på Dynamics 365 Finance

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Projektstyring og regnskab | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Der opstår en fejl ved import af leverandørkreditnotaer. Fejlmeddelelsen siger: "Tilbageholdelsesbeløb må ikke være større end det resterende nettobeløb". |
| Projektstyring og regnskab | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Hvis et fakturaforslag omfatter alle gebyrtransaktioner med nulbeløb, der er ikke-fakturerede faktiske salgsværdier, kan faktureringen ikke finde sted. |
| Projektstyring og regnskab | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Den bogførte omkostning er ikke korrekt, når købsprisen er opdateret, og parameteren **Aktivér ændringsstyring** er aktiveret.|
| Projektstyring og regnskab | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | I bogføringsestimatet for et fastprisprojekt bruges den forkerte valuta og det forkerte beløb i estimatbilaget, selv når også når funktionen **Aktiver projektkontraktvalutaen til estimeret beregning** er aktiveret. |
| Projektstyring og regnskab | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** bør ikke foretage et opkald for at aktivere ændringssporing uden at fange undtagelser for enheder, der har konfigurationsnøgler, som ikke er aktiveret. |
| Projektstyring og regnskab | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Batchjobbet fastlåses, når der bogføres flere avancerede kladder, og der opstår en fejl. |
| Rejser og udgifter | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | På grund af et afregningsproblem, der er relateret til kassebeholdningen i udgiftsrapporter, dækkes momsbeløbet ikke som en del af det kontante forskud. |
| Rejser og udgifter | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Momsoplysninger medtages ikke i rapporten **Udgifter – bogførte transaktioner**. |
| Rejser og udgifter | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Politikken for overtrædelse af **Kvitteringer er påkrævet** for udgifter viser uberettiget en advarsel i udgiftsrapporter. |
| Rejser og udgifter | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | En projekttransaktion medtager ikke moms, der ikke kan inddrives, i det samlede salgsbeløb, når transaktionen er resultatet af en kørselsudgift. |
| Rejser og udgifter | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Når en elementiseret linje indeholder moms, kan du ikke ændre linjedatoen for elementisering, og der opstår en fejl i kildedokumenttilstanden. |

## <a name="removed-and-deprecated-features"></a>Fjernede og udfasede funktioner

Artiklen [Fjernede eller udfasede funktioner i Project Operations](removed-depreciated-features-project.md) beskriver funktioner, der er blevet fjernet eller udfaset for Dynamics 365 Project Operations.

- En fjernet funktion er ikke længere tilgængelig i produktet.
- En udfaset funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

En udfasningsmeddelelse vil blive vist i artiklen [Fjernede eller udfasede funktioner i Project Operations](removed-depreciated-features-project.md) 12 måneder inden, at en funktion fjernes fra produktet.

For ændringer, der kun påvirker kompileringstiden, men som er binært kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Disse ændringer er oftest funktionelle opdateringer, der skal foretages i compileren.
