---
title: Intern fakturering
description: Denne artikel indeholder oplysninger om og eksempler på intern fakturering af projekter.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f66af9b7e2cb0e18a5464b23216ff03b63a0a3
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685371"
---
# <a name="intercompany-invoicing"></a>Intern fakturering

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om og eksempler på intern fakturering af projekter.

Din organisation kan have flere afdelinger, datterselskaber og andre juridiske enheder, som overfører produkter og tjenester til hinanden i forbindelse med projekter. Den juridiske enhed, der leverer tjenesten eller produktet, kaldes den *juridiske udlånsenhed*, og den juridiske enhed, der modtager servicen eller produktet, kaldes den *juridiske låneenhed*. 

I følgende illustration vises et typisk scenarie, hvor to juridiske objekter, SI FR (den juridiske låneenhed) og SI USA (den juridiske udlånsenhed) deler ressourcer for at levere et projekt til kunde A. I dette scenario er SI FR forpligtet i henhold til kontrakt til at levere arbejdet til kunde A. 

[![Eksempel på intern fakturering.](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Målet er at gøre omkostningskontrol, indtægtsføring, moms og overførselspris for interne projekttransaktioner mere fleksibelt og effektivt. Derudover leveres følgende egenskaber:

-   Du kan oprette debitorfakturaer på grundlag af et projekt i en juridisk låneenhed ved hjælp af interne timesedler, udgifter og leverandørfakturaer i en juridisk udlånsenhed.
-   Understøtter momsberegninger og indirekte omkostninger.
-   Udsæt indtægtsføring i en juridisk udlånsenhed, og når en juridisk låneenhed skal genkende omkostningerne.
-   Akkumuler omsætning for igangværende arbejde i den juridiske udlånsenhed.
-   Angiv overførselspriser, der kan være baseret på forskellige prisfastsættelsesmodeller. Her er nogle eksempler:
    -   **Antal** – Den mængde, som du angiver i feltet **Prisfastsættelse**, er den faktiske omkostning pr. antal eller enhed.
    -   **Gebyrbeløb** – Prisen/omkostningerne pr. transaktion plus det gebyrbeløb, du angiver i feltet **Prisfastsættelse**.
    -   **Gebyrprocent** – Overførselsprisen er prisen/omkostningerne pr. transaktion ganget med den gebyrprocent, som du angiver i feltet **Prisfastsættelse**.
    -   **Procent af salgspris** – Den procentdel af salgsprisen, der overføres til den juridiske udlånsenhed.
    -   **Beløb under salgspris** – Det beløb, som den juridiske låneenhed holder tilbage fra salgspriserne, før de overføres til den juridiske udlånsenhed.
    -   **Dækningsgrad** – Det tal, du angiver i feltet **Prisfastsættelse**, er dækningsgraden, som angives som en procentdel af salgsprisen.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Eksempel 1: Opsætning af parametre til intern fakturering
I dette eksempel er USSI en juridisk udlånsenhed, og dens ressourcer er rapporteringsperiode set i forhold til den juridiske låneenhed, FRSI, der ejer kontrakten med slutbrugeren. Timer og udgifter, som USSI's medarbejdere rapporterer, kan medtages i den projektfaktura, som FRSI genererer. Derudover findes der en tredje kilde til transaktioner, som kan stamme fra den juridiske udlånsenhed (her: USSI), når den leverer delte leverandørtjenester til datterselskaber (som f.eks. FRSI) og derefter overfører disse omkostninger til projekter i de pågældende datterselskaber. Alle tilsvarende fakturadokumenter og momsberegninger fuldføres i Finance. 

I dette eksempel skal FRSI være en kunde i den juridiske enhed USSI, og USSI skal være en leverandør i den juridiske enhed FRSI. Derefter kan du konfigurere en intern relation mellem de to juridiske enheder. Den følgende procedure viser, hvordan du konfigurerer parametrene, så begge juridiske enheder kan deltage i intern fakturering.

1. Konfigurer FRSI som kunde i den juridiske enhed USSI, og konfigurer USSI som leverandør i den juridiske enhed FRSI. Der er tre indgangspunkter for de trin, der skal udføres for denne opgave.

   | Trin |                                                       Indgangspunkt                                                        |                                                                                                                                                                                               Beskrivelse                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | I USSI skal du klikke på <strong>Debitor</strong> &gt; <strong>Kunder</strong> &gt; <strong>Alle kunder</strong>. |                                                                                                                                                                  Opret en ny kundepost for FRSI, og vælg kundegruppen.                                                                                                                                                                  |
   |  F   |    I FRSI skal du klikke på <strong>Kreditor</strong> &gt; <strong>Leverandører</strong> &gt; <strong>Alle leverandører</strong>.     |                                                                                                                                                                    Opret en ny leverandørpost for USSI, og vælg leverandørgruppen.                                                                                                                                                                    |
   |  C   |                                  Åbn den leverandørpost, som du lige har oprettet, i FRSI.                                  | I handlingsruden skal du på fanen <strong>Generelt</strong> i gruppen <strong>Konfiguration</strong> klikke på <strong>Intern</strong>. På siden <strong>Intern</strong> skal du på fanen <strong>Samhandelsforhold</strong> angive skyderen <strong>Aktiv</strong> til <strong>Ja</strong>. I feltet <strong>Kundevirksomhed</strong> skal du vælge den kundepost, som du oprettede i trin A. |


2. Klik på **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Regnskabsparametre til projektstyring**, og klik dernæst på fanen **Intern**. Den måde, du konfigurerer parametrene på, afhænger af, om du er den juridiske låneenhed eller den juridiske udlånsenhed.
   -   Hvis du er den juridiske låneenhed, skal du vælge den indkøbskategori, der skal bruges til at afstemme leverandørfakturaerne, som genereres automatisk.
   -   Hvis du er juridisk udlånsenhed for hver låneenhed, skal du vælge en standardprojektkategori for de enkelte transaktionstyper. Projektkategorier bruges til momskonfiguration, når den fakturerede kategori i interne transaktioner kun findes i den juridiske låneenhed. Du kan vælge at akkumulere omsætningen for interne transaktioner. Denne akkumulering sker, når transaktionerne bogføres og derefter tilbageføres, når den interne faktura bogføres.

3. Klik på **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Priser** &gt; **Overfør pris**.
4. Vælg en valuta, transaktionstype og model for prisoverførsel. Den valuta, der bruges på fakturaen, er den valuta, der er konfigureret i kundeposten for den juridiske låneenhed i den juridiske udlånsenhed. Valutaen bruges til at sammenhold poster i tabellen med overførelsesprisen.
5. Klik på **Generel hovedbog** &gt; **Opsætning af bogføring** &gt; **Internt regnskab**, og konfigurer en relation for USSI og FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Eksempel 2: oprettelse og bogføring af en intern timeseddel
USSI, som er den juridiske udlånsenhed, skal oprette og bogføre timesedlen for et projekt fra FRSI, som er den juridiske låneenhed. Der er to indgangspunkter for de trin, der skal udføres for denne opgave.

| Trin | Indgangspunkt                                                                       | Beskrivelse                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektstyring og regnskab** &gt; **Timesedler** &gt; **Alle timesedler** | Opret en ny timeseddel. På timeseddellinjen i feltet **Juridisk enhed** skal du vælge **FRSI**. I feltet **Projekt-id** skal du vælge projektet i FRSI. Angiv timerne for hver dag i ugen. |
| F    | Siden **Timeseddel**                                                                | Når arbejdsprocessen kører, skal du bogføre timesedlen og notere bilagsnummeret.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Eksempel 3: oprettelse og bogføring af en intern leverandørfaktura
USSI, som er den juridiske udlånsenhed, skal oprette og bogføre den interne leverandørfaktura for et projekt fra FRSI, som er den juridiske låneenhed. Denne leverandørfaktura repræsenterer det udliciterede arbejde og de outsourcede udgifter, der blev udført af leverandører, som er blevet betalt af USSI. Der er to indgangspunkter for de trin, der skal udføres for denne opgave.

| Trin | Indgangspunkt                                                                                      | Beskrivelse                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditor** &gt; **Fakturaer** &gt; **Åbne leverandørfakturaer** &gt; **Ny leverandørfaktura** | Opret en ny leverandørfaktura, og angiv de tjenester, der blev anskaffet på vegne af FRSIs projekt.                                                                                                                                                                                  |
| F    | Siden **Leverandørfaktura**                                                                      | Angiv de linjer, der repræsenterer de outsourcede tjenester på vegne af FRSI. På hurtigfanen **Linjedetaljer** skal du på fanen **Projekt** for den pågældende fakturalinje i feltet **Projektvirksomhed** angive **FRSI**. Angiv projektet og de tilsvarende oplysninger. Bogfør derefter leverandørfakturaen. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Eksempel 4: oprettelse og bogføring af den interne faktura
USSI, som er den juridiske udlånsenhed, skal oprette og bogføre den interne faktura. Der er to indgangspunkter for de trin, der skal udføres for denne opgave.

| Trin | Indgangspunkt                                                                                             | Beskrivelse                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Intern kundefaktura**  | Klik på **Ny** for at åbne siden **Opret intern faktura**.                                                                                  |
| F    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Interne kundefakturaer** | På siden **Opret intern faktura** skal du angive den juridiske enhed, specificere hvilken transaktion, der skal inkluderes, og derefter klikke på **Søg**. |
| C    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Interne kundefakturaer** | Vælg de transaktioner, der skal faktureres, eller klik på **Markér alle** for at fakturere alle transaktioner på listen, og klik derefter på **OK**.                  |
| D    | Siden **Intern faktura**                                                                       | Forslaget til den interne kundefaktura vises.                                                                                             |
| E    | Siden **Intern faktura**                                                                       | Klik på **Indlæg**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Eksempel 5: bogfør leverandørfakturaen og fakturerer kunden
Når den juridiske udlånsenhed, USSI, bogfører den interne kundefaktura, oprettes der en tilsvarende afventende leverandørfaktura i den juridiske låneenhed FRSI. Når denne leverandørfaktura er bogført, fakturerer FRSI også projektkunden for de timer, som USSI har angivet. Der er tre indgangspunkter for de trin, der skal udføres for denne opgave.

| Trin | Indgangspunkt                                                                                        | Beskrivelse                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditor** &gt; **Fakturaer** &gt; **Afventende leverandørfakturaer**                            | Gennemse fakturaen for at bekræfte, at værdierne for timesedlen er inkluderet heri, og bogfør derefter leverandørfakturaen.                  |
| F    | **Projektstyring og regnskab** &gt; **Projektfakturaer** &gt; **Forslag til projektfaktura** | Opret en ny projektfaktura for projektet, og kontrollér, at de timetransaktioner, der er bogført, vises.            |
| C    | Siden **Projektfaktura**                                                                       | Vælg projektfakturaen, og klik derefter på **Vis detaljer** for at gennemgå omkostningerne og salgsbeløbet. Bogfør derefter fakturaen. |


Du kan finde flere oplysninger i [Konfiguration af intern projektfakturering](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]