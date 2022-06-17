---
title: Nyheder marts 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i marts 2022-udgivelsen af Project Operations for ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910899"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheder marts 2022 - Project Operations for ressource-/ikke-lagerbaserede scenarier

*Finder anvendelse for: Project Operations for ressource-/ikke-lagerbaserede scenarier*

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.30.0.99
- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.25

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Diæter understøttes nu i det nye og redesignede moderne udgiftsarbejdsområde. Virksomheder, der bruger diæter, kan aktivere denne funktion for at give brugerne en nem måde at indsende og få godtgjort deres diætudgifter på. Du kan finde flere oplysninger i [Diætudgifter](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Opdateringer af Project Operations med dobbeltskrivning-tilknytninger

På følgende liste vises de tilknytninger med dobbelt skrivning, der er ændret eller tilføjet i Project Operations-versionen fra marts 2022.

| **Objekttilknytning** | **Opdateret version** | **Kommentarer** |
| --- | --- | --- |
| Integrationsobjekt for eksport af projektleverandørfakturalinje i Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Tilknytninger er opdateret, så de stemmer overens med leverandørfakturalinjeobjektet i Dataverse. <br>Aktivér ikke tilknytningsversionen 1.0.0.4. Den vil være klar til brug i kombination med Finance-miljøet version 10.0.26 i den næste månedlige opdatering. |

Kør altid den nyeste version af tilknytningen i dit miljø, og aktivér alle relaterede tabeltilknytninger, når du opdaterer din version af Project Operations Dataverse-løsningen og Finance-løsningen. Nogle funktioner fungerer måske ikke korrekt, hvis den nyeste version af tilknytningen ikke er aktiveret. Du kan få vist den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbeltskrivning**. For at aktivere en ny version af tilknytningen skal du vælge **Versioner af tabeltilknytning**, vælge den nyeste version og derefter gemme den valgte version. Hvis du har tilpasset en standardtabeltilknytning, skal du anvende ændringerne igen. Du kan finde flere oplysninger i [Anvendelse af programlivscyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du støder på problemer, når du starter tilknytningen, skal du følge instruktionerne i afsnittet [Problem med manglende tabelkolonner i tilknytninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i fejlfindingsvejledningen til dobbeltskrivning.

## <a name="quality-updates"></a>Kvalitetsopdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Tid og udgift | 2388011 | Vis kommentarer for afvisning af indsendere af tidsregistreringer under massegodkendelse. |
| Projektplanlægning og -sporing | 2495294 | Projektdetaljer må ikke kunne redigeres på siden **Opgavedetaljer**. |
| Fakturering og prisfastsættelse | 2499605 | Kontraktmilepæle, der er oprettet ud fra tilbudsmilepæle, er forkert markeret som skrivebeskyttet. |
| Projektplanlægning og -sporing | 2506050 | Handlingssættet afventer i en time, hvis der ikke er ændringer, der skal gemmes. Sættet markeres derefter forkert som **Mislykket**, men det skal fuldføres med det samme. |
| Fakturering og prisfastsættelse | 2507401 | Der angives forkerte standardkontrakter i projekter på grund af forkert cachelagring. |
| Fakturering og prisfastsættelse | 2541660 | **Validering af salgsordrer** med dobbelt skrivning skal kun være for projektbaserede ordrer. |
| Fakturering og prisfastsættelse | 2552745 | Moms er ikke opdelt mellem kunder, der har oprettet opdelte faktureringsregler. |
| Fakturering og prisfastsættelse | 2558859 | Forbedrede fejlmeddelelser, når der konfigureres dimensioner for prisfastsættelse. |
| Fakturering og prisfastsættelse | 2558933 | **Import fra projektestimater** lykkes ikke, når **msdyn\_project** tilføjes som en prisfastsættelsesdimension. |
| Fakturering og prisfastsættelse | 2559101 | Sletning af projektparameter blokeres ikke og giver problemer. |
| Styring af salgsmuligheder | 2570390 | Du kan bruge plug-in'en med dobbelt skrivning til at gennemtvinge, at kontotypen for tilbud, ordrer og salgsmuligheder skal være **Kunde**, selvom den pågældende kontotype ikke er korrekt. |
| Fakturering og prisfastsættelse | 2586097 | Opdelt fakturering af faktiske omkostninger ændres ikke, når et projekt fjernes fra en projektkontraktlinje. |
| Fakturering og prisfastsættelse | 2589619 | Momsen på indkøbt materiale overføres til ikke-fakturerede faktiske salgsværdier og fakturaen. |
| Styring af salgsmuligheder | 2594015 | Et tilbud kan ikke lukkes som vundet for kunder, der har betalingsbetingelserne **Net60**. |
| Projektplanlægning og -sporing | 2595841 | I Project for the Web modtager brugere en fejlmeddelelse om en manglende **msdyn\_actualstart**, når de opretter en ny ressourceanmodning. |
| Tid og udgift | 2602511 | I feltet **Afvist af** for tidsposter vises **System** i stedet for en navngivet bruger som afviser. |
| Tid og udgift | 2602528 | En projektgodkender kan godkende tid på projekter, hvor de ikke er angivet som godkender. |
| Fakturering og prisfastsættelse | 2608550 | En rettelsesfaktura kan bekræftes, selvom originalen ikke ændres. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Project Management and Accounting på Dynamics 365 Finance

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
| --- | --- | --- |
| Projektstyring og regnskab | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Der er en uoverensstemmelse mellem Finance og Project Operations i den tilladte længde af feltet **Kategori-id**. |
| Projektstyring og regnskab | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Fastprisprojekt kan ikke elimineres, når feltet **Fakturering på konto** angives til **Fortjeneste og tab**, og princippet om **Procentdel for fuldført** anvendes. |
| Projektstyring og regnskab | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Der angives en forkert standard momsgruppe fra projektkonfigurationen på udgiftslinjer i integrationskladden for Project Operations. |
| Projektstyring og regnskab | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Du kan ikke redigere dimensionerne i projektfakturaforslagets overskrift i en integreret udrulning af Project Operations. |
| Projektstyring og regnskab | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Interne leverandørfakturaer må ikke integreres med Dataverse. |
| Projektstyring og regnskab | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Der er en uoverensstemmelse i valutaen for kundens saldi og rapporteringsvalutaen. |
| Projektstyring og regnskab | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Du kan bogføre en projektfaktura, selvom kunden er afventer alle fakturaer. |
| Projektstyring og regnskab | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Knappen **Slet alle linjer** mangler i projektfakturaforslag, der indeholder visningerne **Overskrift** og **Linjer**. |
| Projektstyring og regnskab | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Når du bogfører en leverandørfaktura, opstår følgende fejl: "Regnskabsdatoen for fakturaen skal være i samme regnskabsår som den relaterede købsordre. Kør købsordrens afslutningsproces, eller ret datoen til det aktuelle regnskabsår." |
| Rejser og udgifter | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | De reserverede omkostninger for et projekt frigives ikke, når rejserekvisitionens reserverede omkostninger er frigivet. |
| Rejser og udgifter | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Følgende fejl opstår, når du indsender en Staksporing af en udgiftsrapport: "Staksporing: Firmaet findes ikke." |
| Rejser og udgifter | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Standarden for **Projekt-id** angives ikke i udgiftsrapporter, når parameteren **Kræv aktivitet for kladde** vælges i projektet. |
| Rejser og udgifter | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Knappen **Bogfør udgifter** fungerer ikke korrekt i Project Operations i ressource/ikke-lagerbaserede scenarier. |
| Rejser og udgifter | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Der er problemer med **Sats pr. kilometer** for en rapport for kørselsudgifter, der omfatter passagerer. |
| Rejser og udgifter | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Kilometersatser for kørselsudgifter for medarbejdere regnes ikke korrekt sammen, når der bruges to forskellige køretøjstyper i udgiftskategorien **Niveauer for kørselssats**. |
| Rejser og udgifter | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Opslaget for feltet **Projekt** på en rejserekvisitionslinje returnerer ikke den korrekte liste over projekter. |
| Rejser og udgifter | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Revision af kilometertal** viser en advarsel om udgiftsrapporter. |
| Rejser og udgifter | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Tjenesten til modtagelse af optisk tegngenkendelse (OCR) fungerer ikke på grund af et problem med URL-adressen til omkostningens OCR-tjeneste. |
| Rejser og udgifter | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Når funktionen **Mulighed for hurtigt at elementisere tilbagevendende udgifter** aktiveres, ændres beløbene på elementiseringslinjer i udgiftsrapporter, hver gang siden **Elementiser** åbnes. |
| Rejser og udgifter | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Du kan ikke slette en udgiftsrapport, når den midlertidige liste har mere end én godkender. |

## <a name="removed-and-deprecated-features"></a>Fjernede og udfasede funktioner

Artiklen [Fjernede eller udfasede funktioner i Project Operations](removed-depreciated-features-project.md) beskriver funktioner, der er blevet fjernet eller udfaset for Dynamics 365 Project Operations.

- En fjernet funktion er ikke længere tilgængelig i produktet.
- En udfaset funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

En udfasningsmeddelelse vil blive vist i artiklen [Fjernede eller udfasede funktioner i Project Operations](removed-depreciated-features-project.md) 12 måneder inden, at en funktion fjernes fra produktet.

For ændringer, der kun påvirker kompileringstiden, men som er binært kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Disse ændringer er oftest funktionelle opdateringer, der skal foretages i compileren.
