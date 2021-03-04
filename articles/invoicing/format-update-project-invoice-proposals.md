---
title: Administrer forslag til projektfakturaer
description: Dette emne indeholder oplysninger om behandling af kundeorienterede fakturaer med Project Operations for ressource-/ikke-lagerbaserede scenarier.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089224"
---
# <a name="manage-project-invoice-proposals"></a>Administrer forslag til projektfakturaer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Projektfakturaforslag kan behandles af din faktureringsafdeling, når følgende to betingelser er opfyldt:

  - Projektlederen bekræfter proformafakturaen i Microsoft Dataverse.
  - Alle ikke-fakturerede salgstransaktioner, der er inkluderet i proformafakturaen, bogføres ved at integrere Dynamics 365 **Project Operations Integration**-kladden.

Benyt følgende fremgangsmåde for at oprette et forslag til en projektfaktura i Dynamics 365 Finance.

1. Gennemse faktureringsoplysninger for tids- og materialetransaktioner, og bogfør kladden til **Integration af Project Operations**.
2. Gennemse faktureringsoplysninger milepæle med fast prisfakturering.
3. Gennemse og formater et projektfakturaforslag.
4. Bogfør og udskriv projektfakturaer.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Administrer faktureringsoplysninger i kladden til Integration af Project Operations

De faktiske projektoplysninger, der er oprettet i Dataverse, gennemses og bogføres i Finance af projektets bogholder. Du kan finde flere oplysninger om at arbejde med integrationskladden under [Integrationskladde i Project Operations](../project-accounting/project-operations-integration-journal.md).

Faktiske omkostninger og ikke-fakturerede faktiske salgstal tilføjes til integrationskladden som separate linjer:

  - Enhedsomkostningsprisen og omkostningsbeløbet i den faktiske omkostning er standardværdien fra projektets faktiske omkostningstransaktioner i Dataverse.
  - Enhedens salgspris og salgsbeløbet på den ikke-fakturerede salgstransaktion er standardværdien fra projektets faktiske ikke-fakturerede salgstransaktion i Dataverse.

### <a name="billing-sales-tax"></a>Fakturering af moms

Beregning af moms til fakturering bestemmes af kombinationen af felterne **Fakturering af momsgruppe** og **Fakturering af varemomsgruppe** på en ikke-faktureret salgspost i kladdelinjen i **Integration af Project Operations**. Systemet bruger som standard disse feltværdier på baggrund af indstillingerne under fanen **Økonomi** på siden **Projektstyring og regnskabsparametre**.

- **Metoden momsgruppe** afgør standardlogikken for fakturering af momsgruppen:
  
  - **Projekt**: Vil som standard altid være projektets fakturerede momsgruppe. Du kan gennemse eller ændre et projekts standard for fakturering af momsgruppen ved at vælge **Vis standardregnskab** på siden **Alle projekter**.
  - **Projektkontrakt**: Vil som standard altid være projektkontraktens fakturerede momsgruppe. Du kan gennemse eller ændre en projektkontrakts standard for fakturering af momsgruppen ved at vælge **Vis standardregnskab** på siden **Projektkontrakter**.
  - **Kunde**: Vil som standard altid være kundens fakturerede momsgruppe.
  - **Søg**: Søger på tværs af alle ovennævnte objekter og vælger den første tilgængelige værdi. Søgningen starter med objektet **Projekt**, derefter objektet **Projektkontrakt** og til sidst objektet **Kunde**.

- **Metoden varemomsgruppe** afgør standardlogikken for fakturering af varemomsgruppen:
  
  - I forbindelse med transaktionstyper for tid, udgifter og gebyrer vil faktureringen af varemomsgruppen som standard altid stamme fra objektet **Produktkategori**.
  - I forbindelse med materialetransaktionstyper er standarden for fakturering af varemomsgruppen baseret på indstillingen for **Metoden varemomsgruppe** i **Parametre for projektstyring og regnskab**. Varenummeret bruges som standard for varemomsgruppen og er baseret på objektet **Frigivet produkt**. Kategorien bruges som standard for varemomsgruppen og er baseret på objektet **Projektkategori**.

### <a name="financial-dimensions"></a>Økonomiske dimensioner

De økonomiske dimensioner for ikke-fakturerede salgsposter i kladden for **Integration af Project Operations** er som standard baseret på objektet **Projekt**. Økonomiske dimensioner kan gennemses og justeres ved at vælge **Fordel beløb**. Hvis du har brug for at ændre de økonomiske dimensioner i den ikke-fakturerede salgspost, efter at integrationskladden er bogført, men før proformafakturaen bekræftes, skal du gå til **Alle projekter** > **Administrer** > **Bogførte transaktioner** og vælge transaktionen og derefter vælge **Behandl** > **Tilpas regnskab**.

### <a name="exchange-rates"></a>Valutakurser

Ikke-faktureret transaktionsvaluta i Dataverse anvendes som transaktionsvaluta i Finance og konverteres til virksomhedens regnskabsvaluta ved hjælp af de i Finance definerede valutakurser.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Administrer de økonomiske attributter for faktureringsmilepæle 

Projektkontraktlinjer, som bruger faktureringsmetoden med fast pris, faktureres via [Fastprismilepæle](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Projektets bogholder kan gennemgå faktureringsmilepæle i Finance ved at gå til **Projektstyring og regnskab** > **Alle projekter** > **Administrer** > **Aconto transaktioner**.

### <a name="billing-sales-tax"></a>Fakturering af moms

Værdierne for **Momsgruppe** og **Varemomsgruppe** vises som standard under indstillingerne, når der oprettes en ny faktureringsmilepæl i Dataverse. Systemet bruger som standard værdierne fra disse felter på baggrund af indstillingerne under fanen **Økonomi** på siden **Parametre for projektstyring og regnskab**.

- **Metoden momsgruppe** afgør standardlogikken for **Fakturering af momsgruppen**:

    - **Projekt** vil som standard altid være projektets fakturerede momsgruppe. Du kan gennemse eller ændre et projekts standardmomsgruppen ved at vælge **Vis standardregnskab** på siden **Alle projekter**.
    - **Projektkontrakt** vil som standard altid være projektkontraktens fakturerede momsgruppe. Du kan gennemse eller ændre en projektkontrakts standard momsgruppe ved at vælge **Vis standardregnskab** på siden **Projektkontrakter**.
    - **Kunde** vil som standard altid være kundens fakturerede momsgruppe.
    - **Søg** søger på tværs af alle ovennævnte objekter i denne liste og vælger den første tilgængelige værdi. Søgningen starter med objektet **Projekt**, derefter objektet **Projektkontrakt** og dernæst objektet **Kunde**.

- **Fastprismilepæl for varemomsgruppe** bruges som standard til værdien i feltet **Varemomsgruppe**.

### <a name="financial-dimensions"></a>Økonomiske dimensioner

De økonomiske standarddimensioner for milepælen for fakturering af fast pris angives på projektkontraktlinjer. Gå til **Projektkontrakter** > **Vis standardregnskab**, og på fanen **Kontraktlinjer** skal du vælge **Priskontraktlinje** og derefter angive de økonomiske dimensionsværdier, som du vil bruge som standard.

Projektets bogholder kan redigere oplysningerne om moms og de økonomiske dimensioner i fakturamilepæle, indtil projektfakturaforslaget oprettes.


## <a name="create-project-invoice-proposals"></a>Opret projektfakturaforslag

Projektfakturaforslag kan gennemses i modulet **Projektstyring og regnskab** ved at gå til **Projektfakturaer** > **Projektfakturaforslag**.

Overskriften til projektfakturaforslag oprettes i Finance, når proformafakturaen bekræftes i Dataverse. Systemet angiver det samme nummer for projektfakturaforslaget i Finance til som ID'et for proformafakturaen i Dataverse. Da proformafakturaer ikke nødvendigvis bekræftes i samme rækkefølge, som de oprettes, skal nummerserien for projektfakturaforslag i Finance tillade ændringer til lavere og højere tal. Konfigurer nummerserier ved hjælp af følgende trin:

1. I Finance skal du gå til **Administration af organisation** > **Nummerserier** > **Nummerserier**.
2. I filteret **Område** skal du vælge **Projekter**.
3. I filteret **Reference** skal du vælge **Fakturaforslag**.
4. Brug feltet **Virksomhed** til at filtrere de enkelte juridiske enheder, hvor integration af Project Operations Dataverse er aktiveret.
5. Åbn **Oplysninger om nummerserie**, og angiv følgende under fanen **Generelt**:

    - **Tillad brugerændringer: Til et lavere tal** = **Ja**
    - **Tillad brugerændringer: Til et højere tal** = **Ja**

Projektfakturaforslagslinjer tilføjes af systemet ved hjælp af den periodiske proces for **Import fra midlertidig tabel** (**Projektstyring og regnskab** > **Periodisk** > **Integration af Project Operations** > **Import fra midlertidig tabel**). Denne proces kan køres enten manuelt eller ved hjælp af en periodisk plan. Systemet tilføjer ikke linjer til fakturaforslagsdokumentet, før alle linjer er klar til at blive faktureret. Tids- og materialetransaktioner er kun klar til at blive faktureret, når de bogføres ved at integrere kladden til **Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formater og udskriv fakturaforslag

Projektets bogholder kan tilpasse udskriften af en projektfaktura ved hjælp af siden **Formater fakturaforslag** og funktioner til udskrivning.

### <a name="format-invoice-proposals"></a>Formater fakturaforslag

Siden **Formater fakturaforslag** gør det muligt at vise brugerdefinerede grupperingstransaktioner i kundeprojektfakturaen.

1. På siden **Projektfakturaforslag** skal du vælge **Udskriv** > **Formater fakturaforslag**.
2. Vælg **Ny** for at oprette en ny gruppering for udskriften af projektfakturaen.
3. I feltet **Detaljer/oversigt** skal du vælge indstillinger for denne gruppering:

    - Vælg **Detalje** for at udskrive transaktionsoplysningerne for kundefakturaen.
    - Vælg **Oversigt** for at udskrive transaktionsoversigten for kundefakturaen.

> [!NOTE]
> Dit valg i feltet **Detalje/oversigt** på siden **Formater fakturaforslag**, tilsidesættes den indstilling, der er valgt i feltet **Fakturaformat** på siden **Fakturaforslag**, for at udskrive en detaljeret faktura eller en oversigtsfaktura.

- Vælg de transaktionslinjer, der skal inkluderes i dette afsnit, under fanen **Tilgængelige transaktioner**, og vælg **Medtag transaktioner** for at flytte dem til fanen **Valgte transaktioner**.
- Vælg **Flyt op** og **Flyt ned** for at ændre sektionernes rækkefølge.
- Vælg **Vis udskrift** for at få vist en forhåndsversion af den formaterede faktura.

### <a name="print-management"></a>Udskriftsstyring

I udskriftsstyring bruges forskellige rapportfiler til at udskrive, angive destinationer og tilpasse teksten i fakturaens sidefod. Udskriftsstyring kan konfigureres på modulniveau, men disse indstillinger kan tilsidesættes for et bestemt kunde-, kontrakt- eller fakturaforslag. Du kan få adgang til denne funktion på siden **Projektfakturaforslag** ved at vælge **Udskriv** > **Udskriftsstyring**.

Konfiguration af udskrivningsstyring vises som en trævisning, hvor de tilgængelige dokumenter, der skal justeres, vises på de enkelte nodeniveauer. Du kan tildele brugerdefinerede udskrifter på dokumentniveauet for modulet, kunden, kontrakten eller fakturaforslaget. Hvis du vil ændre udskriften af det oprindelige dokument, skal du udvide den ønskede node og vælge **Oprindeligt element**. I feltet **Rapportformat** skal du vælge det rapportformat, der skal bruges til udskrivning. Du kan bruge brugerdefinerede rapportformater ved hjælp af [rammen for dokumentstyring for virksomheder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Bogfør fakturaforslag

Når fakturaen er blevet gennemset og redigeret, og fakturaforslagslinjerne er klar, skal du kontrollere fakturaens totaler og moms. I gruppen **Detaljer** skal du vælge **Totaler** og derefter vælge **Bogfør** for at bogføre fakturaen.

Hvis du vil have vist fakturaen, før du bogfører den, skal du fjerne markeringen i afkrydsningsfeltet **Bogfør**. **Proforma** udskrives på fakturaen for at indikere, at det er en eksempelfaktura. Hvis du vil udskrive fakturaen, skal du markere afkrydsningsfeltet **Udskriv fakturaen**.

Ud over siden **Fakturaforslag** kan fakturaforslag også bogføres ved at køre det periodiske job **Bogfør fakturaforslag**. Du kan finde dette job ved at gå til **Projektstyring og regnskab** > **Periodisk** > **Projektfakturaer** > **Bogfør fakturaforslag**.

På denne side vises alle de fakturaforslag, der er klar til at blive bogført. Du kan planlægge at bogføre fakturaforslag ved at vælge **Batch**. Angiv **Batchbehandlingsparameteren** til **Ja**, og angiv gentagelsen af batchbehandling ved at vælge **Gentagelse**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]