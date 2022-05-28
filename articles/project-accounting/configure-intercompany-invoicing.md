---
title: Konfigurer intern fakturering
description: Dette emne indeholder oplysninger om og eksempler på, hvordan du kan konfigurere intern fakturering for projekter.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ad6022670048e5aa3635998852b78c49af461d4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591581"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurer intern fakturering

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Benyt følgende fremgangsmåde for at konfigurere interne fakturaer for projekter i Dynamics 365 Project Operations. Interne transaktioner er tids- og udgiftstransaktioner fra en projektkontrakt, der er knyttet til én virksomhed eller organisationsenhed, mens ressourcerne i projektkontrakten er en del af en anden virksomhed eller organisationsenhed.

## <a name="example-configure-intercompany-invoicing"></a>Eksempel: Konfigurer intern fakturering

I følgende eksempel er Contoso Robotics USA (USPM) den juridiske låneenhed, og Contoso Robotics UK (GBPM) er den juridiske udlånsenhed. 

1. **Konfigurer internt regnskab mellem juridiske enheder**. Alle par af juridiske låne- og udlånsenheder skal konfigureres i finanskladden [Internt regnskab](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. I Dynamics 365 Finance skal du gå til **Hovedbog** > **Konfiguration af bogføring** > **Internt regnskab**. Opret en post med følgende oplysninger:

        - **Oprindelig virksomhed** = **GBPM**
        - **Destinationsvirksomhed** = **USPM**

2. **Konfigurer handelsforholdet mellem de juridiske enheder**. Den kundepost, der repræsenterer den juridiske låneenhed, skal oprettes i den juridiske udlånsenhed. Den leverandørpost, der repræsenterer den udlånende juridiske enhed, skal oprettes i den låntagende juridiske enhed.

     1. Vælg den juridiske enhed **GBPM** i Finance.
     2. Gå til **Debitor** > **Kunde** > **Alle kunder**. Opret en ny post for den juridiske enhed **USPM**.
     3. Udvid **Navn**, filtrer posterne efter **Type**, og vælg **Juridiske enheder**. 
     4. Find og vælg kundeposten for **Contoso Robotics USA (USPM)**.
     5. Vælg **Brug match**. 
     6. Vælg kundegruppen **50 - Interne kunder**, og gem derefter posten.
     7. Vælg den juridiske enhed **USPM**.
     8. Gå til **Kreditor** > **Leverandører** > **Alle leverandører**. Opret en ny post for den juridiske enhed **GBPM**.
     9. Udvid **Navn**, filtrer poster efter **Type**, og vælg **Juridiske enheder**. 
     10. Find og vælg kundeposten for **Contoso Robotics UK (GBPM)**.
     11. Vælg **Brug match**, vælg leverandørgruppen, og gem derefter posten.
     12. I leverandørposten skal du vælge **Generelt** > **Opsætning** > **Intern**.
     13. På fanen **Handelsforhold** skal du angive **Aktiv** til **Ja**.
     14. Angiv feltet **Kundevirksomhed** til **GBPM**, og vælg i **Min firmapost** den kundepost, som du oprettede tidligere i proceduren.

3. **Konfigurer interne indstillinger i parametre for projektstyring og regnskab**. 

    1. Vælg den juridiske enhed **USPM**, og gå til **Projektstyring og regnskab** > **Opsætning** > **Parametre for projektstyring og regnskab**.
    2. På fanen **Intern** skal du vælge den indkøbskategori, som skal knyttes til de leverandørfakturaer, der oprettes automatisk.
    3. I **Standardkategori** skal du vælge **Interne ressourcer**.
    4. Vælg den juridiske enhed **GBPM**, og gå til **Projektstyring og regnskab** > **Opsætning** > **Parametre for projektstyring og regnskab**.
    5. På fanen **Intern** skal du vælge en standardprojektkategori for de enkelte transaktionstyper. Projektkategorier bruges til momskonfiguration, når den fakturerede kategori i interne transaktioner kun findes i den juridiske låneenhed. Du kan vælge at akkumulere omsætningen for interne transaktioner. Periodisering sker, når transaktionerne bogføres via integrationskladden i Project Operations i den juridiske udlånsenhed. Kladden tilbageføres, når den interne faktura bogføres.
    6. I gruppen **Ved udlån af ressourcer** skal du vælge **...** > **Ny**. 
    7. I gitteret skal du vælge følgende oplysninger:

          - **Juridiske låneenhed** = **USPM**
          - **Periodiser omsætning** = **Ja**
          - **Standardtimeseddelskategori** = **Standard – time**
          - **Standard udgiftskategori** = **Standard – udgift**

4. **Angiv interne omkostnings- og indtægtskonti i opsætningen af bogføring i hovedbogen**. Den interne indtægtskonto krediteres, når den interne kundefaktura bogføres i den juridiske udlånsenhed. Den interne omkostningskonto debiteres, når den tilsvarende afventende leverandørfaktura bogføres i den juridiske låneenhed. Disse konti konfigureres i tilsvarende juridiske enheder. 
      
     1. Vælg den juridiske låneenhed **USPM** i Finance. 
     2. Gå til **Projektstyring og regnskab** > **Opsætning** > **Bogføring** > **Opsætning af bogføring i hovedbogen**. 
     3. På fanen **Omkostningskonti** i **Type af finanskonto** skal du vælge **Intern omkostning**. Opret en ny post med følgende oplysninger:
      
        - **Juridiske udlånsenhed** = **GBPM**
        - **Hovedkonto** = Vælg hovedkontoen til interne omkostninger. Denne opsætning er obligatorisk. Konfigurationen bruges til interne flow i Finance, men ikke i projektrelaterede interne flow. Denne indstilling har ingen downstream-effekt. 
        
     4. Vælg den juridiske udlånsenhed **GBPM**. 
     5. Gå til **Projektstyring og regnskab** > **Opsætning** > **Bogføring** > **Opsætning af bogføring i hovedbogen**. 
     6. På fanen **Omsætningskonti** i **Type af finanskonto** skal du vælge **Intern omsætning**. Opret en ny post med følgende oplysninger:

        - **Juridiske låneenhed** = **USPM**
        - **Hovedkonto** = Vælg hovedkontoen til intern omsætning. Denne opsætning er obligatorisk. Konfigurationen bruges til interne flow i Finance, men ikke i projektrelaterede interne flow. Denne indstilling har ingen downstream-effekt. 

5. **Konfigurer overførselspriser for arbejde**. Den interne overførselspris er konfigureret i Project Operations på Dataverse. Konfigurer [omkostningssatser for arbejdskraft](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) og [faktureringssats for arbejdskraft](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) for de interne faktureringer. Overførselspriser understøttes ikke ved interne udgiftstransaktioner. Den interne enhedssalgspris angives altid til den samme værdi som kostprisen for ressourceenheden.

      Udviklerressourceomkostningerne i Contoso Robotcs UK er 88 GBP pr. time. Contoso Robotics UK fakturerer Contoso Robotics USA 120 USD for hver time, denne ressource arbejdede på amerikanske projekter. Contoso Robotics USA vil fakturere kunden Adventure Works 200 USD for det arbejde, der udføres af udviklerressourcen i Contoso Robotics UK.

      1. I Project Operations på Dataverse skal du gå til **Salg** > **Prislister**. Opret en ny kostprisliste kaldet **Omkostningssatser for Contoso Robotics UK.** 
      2. I kostprislisten skal du oprette en post med følgende oplysninger:
         - **Rolle** = **Udvikler**
         - **Omkostning** = **88 GBP**
      3. Gå til **Indstillinger** > **Organisationsenheder**, og knyt denne kostprisliste til organisationsenheden **Contoso Robotics UK**.
      4. Gå til **Salg** > **Prislister**. Opret en kostprisliste kaldet **Omkostningssatser for Contoso Robotics USA**. 
      5. I kostprislisten skal du oprette en post med følgende oplysninger:
          - **Rolle** = **Udvikler**
          - **Ressourcevirksomhed** = **Contoso Robotics UK**
          - **Omkostning** = **120 USD**
      6. Gå til **Indstillinger** > **Organisationsenheder**, og knyt kostprislisten for **Omkostningssatser for Contoso Robotics USA** til organisationsenheden **Contoso Robotics USA**.
      7. Gå til **Salg** > **Prislister**. Opret en salgspris liste med navnet **Faktureringssatser for Adventure Works**. 
      8. I salgsprislisten skal du oprette en post med følgende oplysninger:
          - **Rolle** = **Udvikler**
          - **Ressourcevirksomhed** = **Contoso Robotics UK**
          - **Faktureringssats** = **200 USD**
      9. Gå til **Salg** > **Projektkontrakter**, og knyt prislisten for **Faktureringssatser for Adventure Works** sammen med projektkontraktens projektprisliste for Adventure Works.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
