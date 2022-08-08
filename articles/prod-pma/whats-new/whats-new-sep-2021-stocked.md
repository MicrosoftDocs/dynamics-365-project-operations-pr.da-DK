---
title: Nyheder eller ændringer i Project Operations, september 2021 for lagerbaserede/produktionsbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i september 2021-udgivelsen af Project Operations for lagerførte/produktionsbaserede scenarier.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029845"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Nyheder eller ændringer i Project Operations, september 2021 for lagerbaserede/produktionsbaserede scenarier

_**Gælder for:** Project Operations for lagerbaserede/produktionsbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.21
 
## <a name="quality-updates"></a>Kvalitetsopdateringer

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
|---|---|---|
| Projektstyring og regnskab | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Hvis indkøbslederens rolle tildeles adgang til en juridisk enhed, får denne også adgang til alle projekter i alle juridiske enheder. |
| Projektstyring og regnskab | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Der opstår et afrundingsproblem med moms, når en kreditnota afrundes i forhold til en oprindelig projektfaktura. |
| Projektstyring og regnskab | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Brug et alternativt projektbudget til budgetkontrol. |
| Projektstyring og regnskab | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Prisgruppen **Timesalgspris** er ikke beregnet på baggrund af arbejdsopgavehierarki i projekttilbud. |
| Projektstyring og regnskab | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Udelukkelse af estimater mislykkes, når funktionen **Aktivér projektkontraktvaluta for estimatberegning** er aktiveret. |
| Projektstyring og regnskab | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Momsfaktorisering efter antal tilføjes til salgsprisen, når der bruges moms i momsgruppen i projektudgiftskladden. |
| Projektstyring og regnskab | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Betinget moms beregnes ikke korrekt for den sidste betaling, når der blev anvendt leverandørtilbageholdelse og forudbetaling på indkøbsordrefakturaer. |
| Projektstyring og regnskab | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Sporing af tilpasning virker ikke i forbindelse med kladder med åbningssaldi. |
| Projektstyring og regnskab | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Allokeringen af projektbudgetrevision efter periode** opdeles på tværs af alle budgetperioder. Når allokeringen indsendes, ryddes posten ikke. |
| Projektstyring og regnskab | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Igangværende arbejder (IGVA) bogføres med et forkert beløb i finanskladden. |
| Projektstyring og regnskab | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Godkendelsen af projekttimekladden virker ikke. |
| Projektstyring og regnskab | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Projektets justerede salgspris opdateres ikke med indirekte omkostninger, når finansieringsgrænsen ikke er markeret. |
| Projektstyring og regnskab | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Et varekrav kan ikke oprettes, når salgstabeloverskriften faktureres, og den underliggende købsordre for eksisterende linjer er afsluttet. |
| Projektstyring og regnskab | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Tilbageholdelsesbeløbet for en faktureringsregel, der har en milepæl for et andet projekt, bogføres ikke i det tilsvarende projekt-id, der blev valgt for milepælen. I stedet bogføres det på det første projekt. |
| Projektstyring og regnskab | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Når du vælger **Finansielle dimensionssæt** på et fakturaforslag, opstår følgende fejl: "Objektet 'DynamicsAX.Application.FormIntControl' kan ikke tvinges til at konvertere til typen 'Dynamics.AX.Application.FormStringControl'." |
| Projektstyring og regnskab | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Rapporten for **Projektfaktura** springer linjer over. |
| Projektstyring og regnskab | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Der opstår en fejl, når du beregner omkostningskontrolelementet for et investeringsprojekt. |
| Projektstyring og regnskab | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metoden **ProjTable::InitCustTable - canDeletePostalAddress** giver problemer med ydeevnen. |
| Projektstyring og regnskab | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Fejlmeddelelsen bør være tydeligere end "Uventet fejl". |
| Projektstyring og regnskab | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Batchjobbet for bogføring af projektfakturaer behandler og bogfører fakturaforslaget, selv om fakturalinjerne ikke er blevet oprettede. |
| Projektstyring og regnskab | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Der opstår et afrundingsproblem, når konfigurationsnøglen til offentlig licens er slået fra. Der genereres en forkert kost- eller salgspris på timesedlerne for kontrakter, der har flere kilder til finansieringskilder. |
| Projektstyring og regnskab | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Projektsalgsprisen på en faktureret projektkøbsordre beregnes forkert, når salgsprismodellen er **Bidragsprocent**. |
| Projektstyring og regnskab | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Systemet tager ikke højde for de mellemliggende aktive dage, når det beregner den effektive arbejdssats for en medarbejder. |
| Projektstyring og regnskab | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Der opstår en bogføringsfejl på den interne timeseddel på grund af følgende valideringsfejl: "Der er ikke konfigureret nogen partner for den juridiske enhed." |
| Projektstyring og regnskab | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Beskrivelsen fra en købsordre, der har en udgiftskategori, hentes ikke på den bogførte projekttransaktionsliste. |
| Projektstyring og regnskab | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Der er en forkert konvertering i varekladderne, som bogføres på et projekt. |
| Projektstyring og regnskab | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Du kan bekræfte en købsordre, selvom grænsen for finansiering er overskredet. |
| Projektstyring og regnskab | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Sektionen **Ret/annuller faktura** på en fritekstfaktura forsvinder, når der vælges et projekt-id. |
| Projektstyring og regnskab | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Der er problemer med ydeevnen, når et forslag til en projektfaktura bogføres fra en projektsalgsordre, der indeholder en lagervare. |
| Projektstyring og regnskab | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projektkøbsfakturaer kan ikke bogføres, fordi følgende fejl opstår: "Funktionen AccDistProcessorProjectExtension.createForProjectRevenueLine er blevet kaldt forkert." |
| Projektstyring og regnskab | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Opdater til oprettelsen af batchjob for projektestimater med henblik på at understøtte udførelsen af flere underopgaver. |
| Projektstyring og regnskab | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Statussen for en timeseddel kan ikke opdateres til **Kladde**, når arbejdsprocessen sidder fast i tilstanden **Annulleret**. |
| Projektstyring og regnskab | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Tilbageholdelsesbeløb beregnes ikke i kreditnotaens fakturaforslag, hvis der findes flere linjer. |
| Projektstyring og regnskab | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Når du forsøger at ændre beløbet på en genereret faktura på grundlag af en købsordre, opstår følgende fejl: "Transaktionerne på bilaget stemmer ikke med XX/XX/XXXX. (regnskabsvaluta: 0,00 – rapporteringsvaluta: 0,01)." |
| Projektstyring og regnskab | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Der er problemer med ydeevnen, når et forslag til en projektfaktura bogføres i batchtilstand, fordi der oprettes joinforbindelse med **GeneralJournalAccountEntry**. |
| Projektstyring og regnskab | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Der er problemer med ydeevnen, når en timeseddel bogføres. |
| Projektstyring og regnskab | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Omkostningsestimathierarkiet for arbejdsopgavehierarki afstemmes ikke korrekt, når alle opgaver udvides, eller når en enkelt opgave er udvidet manuelt. |
| Projektstyring og regnskab | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Excel-skabelonen for projekttilbud kan ikke tilføjes til menuen **Åbn i Excel**. |
| Projektstyring og regnskab | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Antallet af momsundtagelse for en juridisk enhed inkluderes ikke på den udskrevne projektfaktura. |
| Projektstyring og regnskab | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Der opdateres ingen finansielle data i lagerenhedsfejlen, når et projekt justeres i forhold til kreditlinjer. |
| Projektstyring og regnskab | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Når du anvender videnbase 461935, kan du ikke bogføre estimater, hvis du skifter til kontinuerlige nummersekvenser. |
| Projektstyring og regnskab | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** medfører, at mobilappen Project Timesheet til Android stopper med at svare. |
| Projektstyring og regnskab | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Værdien for igangværende arbejde, der er tilbageført fra en bogført faktura, er forskellig fra den oprindelige bogførte værdi for igangværende arbejde fra tidsregistreringen. |
| Projektstyring og regnskab | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | I anvendte tilbageholdelsestilfælde stemmer transaktionerne på bilaget ikke, når den fakturerede omsætning for et projekt bogføres. |
| Projektstyring og regnskab | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Når funktionen **Forbedring af ydeevnen for projektressourceplanlægning** er aktiveret, afrundes decimalværdier forkert for ressourcetilgængelighed og kapacitet. |
| Projektstyring og regnskab | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Når funktionen **Opret projektestimat ved hjælp af flere batchopgaver** er aktiveret, fungerer oprettelse af estimater i en batch, der har flere underopgaver, kun for den aktuelle periode. |
| Rejser og udgifter | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | En politik for rejserekvisition ignoreres, og arbejdsprocessen godkendes uden fejl. |
| Rejser og udgifter | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobilappen Udgift gemmer ikke følgende oplysninger på udgiftslinjen:</p><ul><li>Projekt-id'et</li><li>Om udgifterne kan faktureres</li><li>Aktivitetsnummeret</li></ul> |
| Rejser og udgifter | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Feltet **Vedhæftede kvitteringer** er angivet til **Ja**, selvom der ikke er vedhæftet kvitteringer til udgiftslinjen. |
| Rejser og udgifter | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Der opstår en fejl, når du ændrer udgiftskategorien til **Personlig**. |
| Rejser og udgifter | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Du kan ikke vedhæfte en kvittering og redigere den overordnede udgift, når en kreditkorttransaktion opdeles på en personlig udgift. |
| Rejser og udgifter | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Udgiftspolitikken for interne transaktioner med et projekt-id fungerer ikke korrekt. |
| Rejser og udgifter | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Den bogførte datooplysning mangler for bogførte udgiftsrapporter. |
| Rejser og udgifter | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Der er problemer med betalingsmetoden i mobilappen Udgift. |
| Rejser og udgifter | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | En rejserekvisition, der er oprettet for én arbejder, kan bruges til en anden arbejders udgiftsrapport før stedfortræderdatoen. |
| Rejser og udgifter | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Når du opretter en udgift, opdateres ændringer af værdierne for økonomiske dimension ikke korrekt på regnskabsfordelingsniveau i arbejdsområdet **Udgiftsstyring**. |
| Rejser og udgifter | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status for godkendelse af hovedudgiftslinjen synkroniseres ikke med den angivne status for godkendelse af arbejdsproceslinjer. |
| Rejser og udgifter | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Der opstår en fejl, hvis du bogfører en udgiftsrapport, og momsinddrivelse er aktiveret. |
| Rejser og udgifter | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | En stedfortræder kan ikke slette udgiftsdokumenter for en afskediget medarbejder. |
| Rejser og udgifter | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Sletning af en udgiftslinje tager længere tid end forventet og påvirker ydeevnen. |
| Rejser og udgifter | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** resulterer i en mistet **TaxUncommitted**-post, da alene **SourceDocumentLine** slettes. |
| Rejser og udgifter | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** efterlever ikke **trvExpTrans.ReferenceDataAreaId** for at oprette den nye nummersekvens. |

## <a name="regulatory-updates"></a>Lovgivningsmæssige opdateringer

Du kan finde oplysninger om lovgivningsmæssige opdateringer til programmer til finans og drift under [Lovgivningsmæssige opdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på Microsoft Dynamics Lifecycle Services (LCS) og bruge problemsøgningsværktøjet til at få vist planlagte lovpligtige opdateringer. Problemsøgning giver dig mulighed for at søge efter land eller område, funktionstype og udgivelse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
