---
title: Nyheder eller ændringer i Project Operations, oktober 2021 for lagerbaserede/produktionsbaserede scenarier
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i oktober 2021-udgivelsen af Project Operations for lager-/produktionsbaserede scenarier.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933669"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Nyheder eller ændringer i Project Operations, oktober 2021 for lagerbaserede/produktionsbaserede scenarier

_**Gælder for:** Project Operations for lagerbaserede/produktionsbaserede scenarier_

Denne artikel gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Projektstyring og regnskab i et Dynamics 365 Finance-miljø version 10.0.22
 
## <a name="quality-updates"></a>Kvalitetsopdateringer

| Funktionsområde | Referencenummer | Kvalitetsopdatering |
|--------------|------------------|----------------|
| Projektstyring og regnskab | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Beløbene for igangværende projektarbejdet (IGVA) og den akkumulerede omsætning tilbageføres ikke korrekt, når der bogføres en intern kundefaktura. |
| Projektstyring og regnskab | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funktionen **Forhindr lukning af projekt, hvis der findes åbne transaktioner** virker ikke. |
| Projektstyring og regnskab | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Faktureringsklassifikationen på en fritekstfaktura udfyldes ikke automatisk i dimensionerne fra projekter, når funktionaliteten er aktiveret. |
| Projektstyring og regnskab | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | I ikke-interne scenarier tilbageføres beløbene for igangværende projektarbejdet (IGVA) og den akkumulerede omsætning ikke korrekt, når projektfakturaen bogføres. |
| Projektstyring og regnskab | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debet- og kreditværdier byttes rundt, når tilføjelsesprogrammet for Microsoft Excel bruges sammen med projektudgiftskladden, og feltet **Modposteringskontotype** angives til **Projekt**. |
| Projektstyring og regnskab | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Det beløb, der bogføres i projekttransaktioner, overdrives på en projektkøbsordre, der indeholder lagervarer, og som har momsbeløb, der ikke kan trækkes fra, når **UseTax** er markeret. |
| Projektstyring og regnskab | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | I systemet opdeles beløbet mellem projektresultat- og projekttabsrapporterne og rapporterne for igangværende arbejde på projektet. |
| Projektstyring og regnskab | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Det tilgængelige lager er forkert, når en delvist returneret vare justeres. |
| Projektstyring og regnskab | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Ressourcenavne duplikeres i Project Operations, når de redigeres i Microsoft Project. |
| Projektstyring og regnskab | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Interne udgiftsrapporter, der indeholder interne, afventende leverandørkreditomkostninger bogføres først til bogføringstypen **Omkostninger for igangværende arbejde på projekt**. Under behandlingen bogføres de estimatrelaterede omkostninger dog til bogføringstypen **Projektomkostninger** i stedet for den forventede bogføringstype **Interne omkostninger**. |
| Projektstyring og regnskab | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Leverandørtilbageholdelse resulterer i, at projektomkostningstransaktioner ikke vises. |
| Projektstyring og regnskab | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Timeseddelen skal afrunde transaktionsbeløbet i transaktionsvalutaen til et angivet antal decimaler i alle regnskabsfordelinger og posteringer i den generelle kladdeallokering. |
| Projektstyring og regnskab | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Antallet af projektelementkrav opdateres automatisk, når de planlagte ordrer bekræftes. |
| Projektstyring og regnskab | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Bilagsnummeret, transaktionstypen, leverandørsaldo og kontonummer kan ikke fortrydes på forudbetalingsfakturaen for en købsordre. |
| Projektstyring og regnskab | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Den interne leverandørfaktura brydes, når integration af leverandørfakturaer slås til. |
| Projektstyring og regnskab | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Når du opretter en projektomkostningskladde, vises omkostningsbeløbet i feltet **Kredit**. |
| Projektstyring og regnskab | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Betalingsbetingelserne på projektfakturaer fungerer ikke som forventet. |
| Projektstyring og regnskab | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Bilag til timesedler kan genbruges, når nummerserien konfigureres som kontinuerlig. |
| Projektstyring og regnskab | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANKRIG: Logikken for **Manuel tilbageholdelsesbeløb** stemmer ikke overens med logikken for **Automatisk tilbageholdelsesbeløb** i fakturaforslaget på projektkontrakten. |
| Projektstyring og regnskab | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Når leverandørtilbageholdelsen frigives, indeholder bilagsbogføringen flere linjer. |
| Projektstyring og regnskab | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Når feltet **Fakturadato** på siden **Opret fakturaforslag** ændres, kan følgende fejl opstå: "Objektreferencen er ikke angivet til en forekomst af et objekt." |
| Projektstyring og regnskab | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Der opstår en fejl, når du forsøger at godkende en timeseddel fra **TSLine**-arbejdsprocessen, og der er en timeseddelpolitik for lørdag og søndag. |
| Projektstyring og regnskab | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Projektelementtypen startsaldo medtages ikke i **Transaktionsoversigter for fakturaforslag**, når fakturatotalen for fakturaforslaget beregnes. |
| Projektstyring og regnskab | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Hvis forbrugsomkostningen på en projektproduktionsordre er 0 (nul), opstår følgende fejl, når du forsøger at estimere: "Forsøg på at dele med nul." |
| Projektstyring og regnskab | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Appen Project Timesheet Mobile til Android stopper med at svare. Problemet er relateret til **TimeEntryDataManager ArgumentNullException**. |
| Projektstyring og regnskab | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Integrationskladden for Project Operations mislykkes, når du bogfører den, fordi en konto mangler dimensioner. Den konto, der mangler dimensionerne, er dog ikke den konto, som du bogfører til. |
| Projektstyring og regnskab | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filteret **ToDate** i søgninger ryddes ikke, når det fjernes fra dialogboksen **Vælg** på siden **Bogfør omkostninger**. |
| Projektstyring og regnskab | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Nulstil al distribution** mislykkes, og der vises en fejl i de timesedler, der er oprettet for et projekt af typen **Kun tid**. |
| Projektstyring og regnskab | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Fanen **Projekt** kan ikke redigeres på en afventende leverandørfaktura, når indkøbskategorien tildeles til varen. |
| Projektstyring og regnskab | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigationsruden mangler, hvis du ikke er logget på Project Operations Dataverse. |
| Projektstyring og regnskab | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Der problemer i destinationsvirksomheden i forbindelse med interne projekttilpasningstransaktioner. |
| Projektstyring og regnskab | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Ved bekræftede omkostninger for et projekt beregnes det forkerte antal og den forkerte kostpris, hvis købsordren blev behandlet af **Årsafslutningsprocessen** i finanskladden. |
| Projektstyring og regnskab | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Når en projektproduktionsordre med gode ordrer rapporteres som færdig, opstår følgende fejl: "Ingen virtuel transaktion er markeret med lagertransaktion." |
| Projektstyring og regnskab | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Når en projektrelateret kreditorfaktura bogføres, opstår følgende fejl: "Optalt tekstprojekt - omkostning - vare findes ikke." |
| Projektstyring og regnskab | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Indirekte omkostninger fordobles, når du periodiserer omsætning manuelt. |
| Projektstyring og regnskab | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Periodisering af omsætning og bogføring af igangværende arbejde genererer ikke transaktioner. |
| Projektstyring og regnskab | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivering af den afventende pris mislykkes for et standardkostpriselement, når der findes en modtaget projektkøbsordre. |
| Projektstyring og regnskab | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Værdien for igangværende arbejde, der er tilbageført fra en bogført faktura, er forskellig fra den oprindelige bogførte værdi for igangværende arbejde fra en tidsregistrering. |
| Projektstyring og regnskab | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Der er et problem med bogføring af projektfaktureret omsætning i anvendte tilbageholdelsestilfælde, hvor transaktionerne på bilaget ikke stemmer. |
| Projektstyring og regnskab | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Oprettelse af et estimat, når et fakturaforslag er bogført, blokeres importen af korrektionslinjer i Project Operations. |
| Projektstyring og regnskab | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Det bør ikke være muligt at ændre en fuldt faktureret milepælspost. |
| Projektstyring og regnskab | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Når der bruges automatiske gebyrer, kan den interne kundefaktura for en timeseddel ikke bogføres, og der vises en fejlmeddelelse. |
| Projektstyring og regnskab | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adressen på et underprojekt opdateres ikke korrekt. |
| Projektstyring og regnskab | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Kostprisen på varekrav opdateres med købsprisen for samlede købsordrer. |
| Projektstyring og regnskab | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Den bogførte omkostning er ikke korrekt, når købsprisen er opdateret, og parameteren **Aktivér ændringsstyring** er aktiveret. |
| Rejser og udgifter | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alle brugerudgifter er synlige, når du søger efter en kategori i mobilappen Udgift. |
| Rejser og udgifter | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Forkerte beløb i leverandørtransaktioner og momstransaktioner, der er bogført fra en udgift, som blev oprettet på grundlag af en kreditkorttransaktion. |
| Rejser og udgifter | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Der vises en irrelevant meddelelse, når du opdaterer siderne med udgiftsrapporter. |
| Rejser og udgifter | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Den forkerte midlertidige godkender bruges, når du sletter en midlertidig godkender og derefter indsender udgiftsrapporten igen via arbejdsprocessen. |
| Rejser og udgifter | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Der opstår en bogføringsfejl, der er relateret til konfigurationen af kilometertal. |
| Rejser og udgifter | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribution opdaterer ikke den juridiske enhed, når en ikke-tilgængelig transaktion igen tilføjes til udgiftsrapporten på en intern omkostning. |

### <a name="regulatory-updates"></a>Lovgivningsmæssige opdateringer

Du kan finde oplysninger om lovgivningsmæssige opdateringer til programmer til finans og drift under [Lovgivningsmæssige opdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på Microsoft Dynamics Lifecycle Services (LCS) og bruge problemsøgningsværktøjet til at få vist planlagte lovpligtige opdateringer. Problemsøgning giver dig mulighed for at søge efter land eller område, funktionstype og udgivelse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
