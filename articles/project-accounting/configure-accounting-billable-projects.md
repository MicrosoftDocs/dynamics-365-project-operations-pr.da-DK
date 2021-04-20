---
title: Konfigurer regnskab for fakturerbare projekter
description: Dette emne indeholder oplysninger om regnskabsindstillinger for fakturerbare projekter.
author: sigitac
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 629e3fc2f9069d104d459d0b4a6fa46c37f5c6f2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858646"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurer regnskab for fakturerbare projekter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations understøtter forskellige regnskabsindstillinger for fakturerbare projekter, der omfatter tids- og materialetransaktioner og transaktioner med fast pris.

- **Tids- og materialetransaktioner**: Disse transaktioner faktureres, efterhånden som arbejdet skrider frem, og er baseret på forbruget af timer, udgifter, varer eller gebyrer i projektet. Disse transaktionsomkostninger kan sammenlignes med omsætningen på hver enkelt transaktion, og projektet faktureres, mens arbejdet skrider frem. Projektomsætning kan også periodiseres på det tidspunkt, hvor transaktionen indtræffer. Under fakturering registreres omsætningen, og periodiseret omsætning tilbageføres, hvis det er relevant.
- **Fastpristransaktioner**: Disse transaktioner faktureres i henhold til en faktureringsplan, der er baseret på projektkontrakten. Omsætningen for fastpristransaktioner kan registreres ved fakturering eller beregnes og bogføres periodisk i henhold til metoderne **Afsluttet kontrakt** eller **Afsluttet procentdel**.

Et projekt betragtes som fakturerbart, når det knyttes til en eller flere kontraktlinjer. En projektkontraktlinje definerer for sig selv, hvilken faktureringsmetode og hvilke transaktionstyper der er tilladt.

Som eksempel har Fabrikam Robotics vundet en projektkontrakt med Adatum Corporation til optimering af udstyr. Adatum vil betale et fast beløb på 10.000 DKK til dækning af påløbne projektudgifter. Dette er faktureringsmetode for faste priser. Tidsforbrug og gebyrer for projektet faktureres pr. gang. Dette er en faktureringsmetode for tidsforbrug og materialeforbrug. Alt arbejde spores under et enkelt projekt med navnet Adatum udstyrsoptimering.

Et projektteammedlem indsender otte timers arbejde på projektet Adatum udstyrsoptimering. Når projektlederen godkender denne tid, bruger systemet faktureringsmetoden for tidsforbrug og materialeforbrug til at oprette faktiske transaktioner, en faktura og en konto. Denne transaktion inkluderes ikke i den estimerede beregning af fast pris-omsætning.

Et andet projektteammedlem indsender rejseudgifter for 2.000,00 DKK i forbindelse med projektet Adatum udstyrsoptimering. Når projektlederen godkender denne indsendelse, bruger systemet en faktureringsmetode for fast pris til at oprette faktiske transaktioner og en konto for disse projektudgifter. Kunden faktureres ikke på baggrund af denne transaktion. Kunden faktureres i stedet ved hjælp af en separat konfigureret faktureringsmilepæl. Denne udgiftstransaktion og udgiftsestimater inkluderes i den estimerede beregning af fast pris-omsætning.

Regnskabsprincipper for projekttransaktioner defineres i projektomkostnings- og indtægtsprofiler. For hver projekttransaktion bestemmer systemet den relevante projektomkostnings- og indtægtsprofil ved hjælp af reglerne for projektomkostnings- og indtægtsprofil, der er konfigureret.

## <a name="define-project-cost-and-revenue-profiles"></a>Definer projektets omkostnings- og omsætningsprofiler 

Projektomkostnings- og indtægtsprofiler fastsætter regnskabsreglerne for projekttransaktioner. Disse profiler er konfigureret i Projektstyring og regnskab. 

Benyt følgende fremgangsmåde for at oprette en ny projektomkostnings- og indtægtsprofil. 

1. Gå til **Projektstyring og regnskab** > **Opsætning** > **Bogføring** > **Projektomkostnings- og indtægtsprofiler**. 
2. Vælg **Ny** for at oprette en ny projektomkostnings- og indtægtsprofil.
3. I feltet **Navn** skal du angive navnet på og en kort beskrivelse af profilen.
4. I feltet **Faktureringsmetode** skal du vælge **Tid og materialer** eller **Fast pris**.
5. Udvid oversigtspanelet **Hovedbog**. Felterne under denne fane definerer de regnskabsprincipper, der skal bruges, når projekttransaktioner journaliseres ved hjælp af kladden til integration af Project Operations og derefter faktureres via projektfakturaforslaget.
6. Vælg de relevante oplysninger i følgende felter på oversigtspanelet **Hovedbog**:

    - **Bogfør omkostninger – time**:

       - *Ingen hovedbog*: Omkostningerne for timetransaktioner vil ikke blive bogført i hovedbogen, når kladden til integration af Project Operations bogføres. Bogholderen kan dog bogføre omkostninger ved hjælp af funktionen Bogfør omkostninger på et senere tidspunkt.
       - **Saldo**: Kostprisen for timetransaktioner debiteres hovedbogskontotypen *IGVA - kostværdien* og krediteres på *Lønfordelingskontoen* i opsætningen af opsætning af bogføring i hovedbogen. Bogholderen bruger funktionen Bogfør omkostninger til at flytte disse omkostninger fra en saldokonto til en driftskonto med jævne mellemrum.
       - **Drift**: Når du bogfører kladden for integration af Project Operations, debiteres tidstransaktionsomkostninger på hovedbogskontotypen *Omkostning*, og den krediteres på den *Lønfordelingskonto*, der er defineret under fanen **Omkostninger** på siden **Opsætning af finanskontering** (**Projektstyring og regnskab** \> **Opsætning** \> **Bogføring** \> **Opsætning af bogføring i hovedbog**). Dette er den mest almindelige opsætning for tids- og materialetransaktioner.
        - *Aldrig finanskonto*: Omkostningen for timetransaktioner vil aldrig blive bogført i hovedbogen.

    - **Bogfør omkostninger - udgifter**:

         - **Saldo**: Når du bogfører integrationskladden for Project Operations, debiteres omkostningstransaktionsudgiften på hovedbogskontotypen *IGVA - kostværdi* som defineret under fanen **Omkostninger** på siden **Opsætning af bogføring i hovedbog** og krediteres på modkontoen på kladdelinjen. Standardmodkonti for udgifter defineres i **Projektstyring og regnskab** > **Opsætning** \> **Bogføring** \> **Standardmodkonti for udgifter**. Bogholderen bruger funktionen **Bogfør omkostninger** til at flytte disse omkostninger fra saldokontoen til driftskontoen med jævne mellemrum.
        - **Driftskonto**: Når du bogfører integrationskladden for Project Operations, debiteres omkostningstransaktionsudgiften på hovedbogskontotypen *Omkostninger* som defineret under fanen **Omkostninger** på siden **Opsætning af bogføring i hovedbogen** og krediteres på modkontoen på kladdelinjen. Standardmodkonti for udgifter defineres i **Projektstyring og regnskab** \> **Opsætning** \> **Bogføring** \> **Standardmodkonti for udgifter**.
      
    - **Bogfør omkostninger – vare**:

         - **Saldo**: Når du bogfører integrationskladden i Project Operations, debiteres varens transaktionsomkostninger på typen finanskonto *Igangværende arbejde – omkostningsværdi – element vare* som defineret under fanen **Omkostninger** på siden **Opsætning af hovedbogsbogføring** og krediteres på følgende:
    
              - Ved dokumenter af typen brug: kontoen **Omkostning – vare** i **Opsætning af hovedbogsbogføring**.  
              - Ved dokumenter af typen køb: **Indkøbsintegrationskonto** på **Projektstyring og regnskabsparametre**.
           Bogholderen bruger funktionen **Bogfør omkostninger** til at flytte disse omkostninger fra saldokontoen til driftskontoen med jævne mellemrum.
        - **Resultatopgørelse**: Når du bogfører integrationskladden i Project Operations, debiteres varens transaktionsomkostninger på finanskontotypen *Omkostning* som defineret under fanen **Omkostninger** på siden **Opsætning af hovedbogsbogføring** og krediteres på følgende:
         
             - Ved dokumenter af typen brug: kontoen **Omkostning – vare** i **Opsætning af hovedbogsbogføring**.  
             - Ved dokumenter af typen køb: **Indkøbsintegrationskonto** på **Projektstyring og regnskabsparametre**.
       
    - **Aconto-fakturering**:

        - **Saldo**: Når du bogfører Projektfakturaforslaget, krediteres en aconto-transaktion (faktureringsmilepæl) til hovedbogskontotypen *IGVA - aconto* som defineret under fanen **Omsætning** på siden **Opsætning af bogføring på hovedbog**, og som debiteres på debitors saldokonto.
         - **Drift**: Når du bogfører Projektfakturaforslaget, krediteres en aconto-transaktion (faktureringsmilepæl) til hovedbogskontotypen *Faktureret omsætning - aconto* som defineret under fanen **Omsætning** på siden **Opsætning af bogføring på hovedbog**, og som debiteres på debitors saldokonto. Kundesaldokonti defineres i **Debitor** \> **Opsætning** \> **Profiler for kundebogføring**.

   Når du definerer bogføringsprofilerne for tid- og materialefaktureringsmetoder, har du mulighed for at akkumulere omsætning pr. transaktionstype (time, udgifter, vare og gebyr). Hvis indstillingen **Periodiseret omsætning** er angivet til **Ja**, registreres ikke-fakturerede salgstransaktioner i integrationskladden til Project Operations i finanskladden. Salgsværdien debiteres på **IGVA - salgsværdikonto** og krediteres på kontoen **Periodiseret omsætning - salgsværdi**, der blev konfigureret på siden **Opsætning af bogføring i hovedbogen** på fanen **Omsætning**. 
  
  > [!NOTE]
  > Indstillingen **Periodiseret omsætning** er kun tilgængelig, hvis den respektive transaktionstype **Omkostninger** bogføres på driftskontoen.
    
7. Udvid oversigtspanelet **Estimering**. Felterne under denne fane definerer beregningsindstillingerne for estimater for fast pris-omsætning. Felterne under denne fane gælder kun for projektomkostnings- og indtægtsprofiler med faktureringsmetoden **Fastpris**.
8. Vælg de relevante oplysninger i følgende felter på oversigtspanelet **Estimering**:

    - **Princippet bruges til beregning af færdiggørelse af projekt**:

        - **Afsluttet kontrakt**: Omkostningsperiodisering og indtægtsføring foretages ikke før projektet afsluttes. Omkostningerne afspejles som IGVA i saldoen, indtil projektet er fuldført.
        - **Afsluttet procentdel**: Periodiseret omsætning beregnes og bogføres i finanskladden for hver periode på grundlag af projektets færdiggørelsesprocent. Der findes flere metoder til beregning af færdiggørelsesprocenten. Disse metoder kan være automatiske på grundlag af konfiguration eller manuelle.
        - **Ingen IGVA**: Denne opsætning bruges til fastprisprojekter med en kort levetid, hvor fakturaen og omkostningerne opstår i samme periode. I dette tilfælde angives feltværdien **Aconto-fakturering** i oversigtspanelet **Hovedbog** automatisk til **Drift** for at sikre, at indtægter registreres ved fakturering. Indtægtsestimeringsprocessen bruges ikke for denne projektomkostnings- og indtægtsprofil.

    - **Periodiseringsprincip**: Dette felt bestemmer, hvordan den beregnede salgsværdi (periodiseret omsætning) skal bogføres i hovedbogen.

        - Ved hjælp af princippet **Salgsværdi**, beregner systemet salgsværdien ved at matche omkostningerne og omsætning og derefter bogføre den som et enkelt beløb.
        - Ved hjælp af princippet **Produktion og avance** deler systemet salgsværdien op i realiserede omkostninger og beregnet avance. Disse bogføres separat.

    - **Omkostningsskabeloner**: Tillad, at projekttransaktioner grupperes på baggrund af transaktionstype og projektkategori, og definer beregningsregler for procent for færdiggørelse for disse grupper.
    - **Periodekoder**: Definer den hyppighed, hvormed omsætningsestimater beregnes for en bestemt projektomkostnings- og indtægtsprofil.
    - **Kategorier for estimat**: Bruges til bogføring af salgsværdi (periodiseret omsætning) i projekttransaktioner. Du skal først konfigurere den dedikerede projektkategori for en **Gebyr**-transaktionstype og derefter angive flaget **Estimering** for denne projektkategori. Vælg derefter denne projektkategori i feltet **Salgsværdi** eller **Avance** i projektomkostnings- og indtægtsprofilen, afhængigt af det valgte periodiseringsprincip.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Eksempel på konfigurationer for projektomkostnings- og indtægtsprofiler

Tid og materialer – ingen IGVA

![Omkostnings- og omsætningsprofil: tid og materialer - ingen IGVA](media/time-material-no-wip.png)

Tid og materialer – IGVA (omsætning)

![Omkostnings- og omsætningsprofil: tid og materialer - IGVA](media/time-material-with-wip.png)

Fast pris – ingen IGVA

![Omkostnings- og omsætningsprofil: fast pris - ingen IGVA](media/fixed-price-no-wip.png)

Fast pris – afsluttet kontrakt

![Omkostnings- og omsætningsprofil: fast pris - afsluttet kontrakt](media/fixed-price-completed-contract.png)

Fast pris – færdiggørelsesprocent

![Omkostnings- og omsætningsprofil: fast pris - færdiggørelsesprocent](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Eksempel på regnskabshændelser for eksempler på projektomkostnings- og indtægtsprofiler.

| Regnskabshændelse                  | Tid og materiale - ingen IGVA                       | Tid og materiale - IGVA                                                                                           | Fast pris – ingen IGVA                                            | Fast pris – afsluttet kontrakt                                                                            | Fast pris – færdiggørelsesprocent                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Journalisering af tidstransaktioner    | Debet – omkostninger <br>Kredit – Lønfordeling          | Debet - omkostninger <br>Kredit – Lønfordeling <br>Debet – salgsværdi for IGVA <br>Kredit – salgsværdi for periodiseret omsætning                | Debet – omkostninger <br>Kredit – Lønfordeling                         | Debet – omkostninger <br>Kredit – Lønfordeling                                                                    | Debet – omkostninger <br>Kredit – Lønfordeling                       |
| Journalisering af udgiftstransaktioner | Debet – omkostninger <br>Kredit – modkonto til udgift | Debet – omkostninger <br>Kredit – modkonto til udgift <br>Debet – salgsværdi for IGVA <br>Kredit – salgsværdi for periodiseret omsætning      | Debet – omkostninger <br>Kredit – modkonto til udgift                 | Debet – omkostninger<br> Kredit – modkonto til udgift                                                            | Debet – omkostninger <br>Kredit – modkonto til udgift               |
| Fakturering af kunder                | Debet – kundesaldo <br>Kredit – faktureret omsætning | Debet – kundesaldo <br>Kredit – faktureret omsætning <br>Kredit – salgsværdi for IGVA – debet – salgsværdi for periodiseret omsætning | Debet – kundesaldo <br>Kredit – faktureret omsætning - aconto | Debet – kundesaldo <br>Kredit – IGVA – faktureret aconto                                                  | Debet – kundesaldo <br>Kredit – IGVA - faktureret aconto    |
| Bogfør anslået omsætning             | Ikke tilgængelig                                   | Ikke tilgængelig                                                                                                    | Ikke relevant                                                  | Debet – omkostningsværdi af IGVA <br>Kredit – omkostning                                                                         | Debet - IGVA - salgsværdi <br>Kredit – salgsværdi for periodiseret omsætning |
| Fjern                         | Ikke tilgængelig                                   | Ikke tilgængelig                                                                                                    | Ikke relevant                                                  | Kredit – omkostningsværdi af IGVA <br>Debet – omkostninger <br>Kredit – periodiseret omsætning - salgsværdi <br>Debet – IGVA faktureret aconto | Debet – IGVA – faktureret aconto <br>Kredit – salgsværdi af IGVA     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurer regler for projektets omkostnings- og omsætningsprofiler

Reglerne for projektomkostnings- og omsætningsprofiler bestemmer, hvilke projektomkostnings- og indtægtsprofiler der skal bruges, når fakturerbare projekttransaktioner skal behandles. Definer reglerne ved at gå til **Projektstyring og regnskab** \> **Opsætning** \> **Bogføring** \> **Regler for projektomkostnings- og omsætningsprofil**.

Regler kan defineres ud fra projektkontrakt, projektgruppe eller efter et bestemt projekt. Systemet vælger altid den højeste granuleringsregel først.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
