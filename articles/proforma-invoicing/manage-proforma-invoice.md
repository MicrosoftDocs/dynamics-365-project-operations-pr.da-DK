---
title: Administrer en projektbaseret proformafaktura
description: Dette emne indeholder oplysninger om, hvordan du administrerer og arbejder med projektbaserede proformafakturaer.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1b0f70f25d157e1d7e2d14dc011a048d698d299
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012534"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Administrer en projektbaseret proformafaktura

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

I Dynamics 365 Project Operations er proformafakturaer bygget som en udvidelse til fakturaerne i Dynamics 365 Sales. Der er dog mange forskelle i faktureringsprocessen mellem Sales og Project Operations, når det kommer til fakturering. Det er f.eks. ikke muligt at oprette en ny faktura fra siden **Fakturaliste** i Project Operations, men det er muligt at gøre det i Sales. Disse forskelle og udvidelser kan bruges til at understøtte faktureringsprocesser for projekter, der adskiller sig fra en typisk faktura for en salgsordre.

> [!IMPORTANT]
> På grund af forskellene skal du ikke skifte mellem at fakturere i Sales og Project Operations.

## <a name="invoice-header"></a>Fakturaoverskrift

Følgende oplysninger er tilgængelige i forbindelse med en overskrift til en proformafaktura i Project Operations.

| Felt | Lokation | Beskrivelse |
| --- | --- | --- | 
| **Faktura-id** | Fanen **Oversigt** | App-id'et, der genereres automatisk, når en proformafaktura oprettes. Et skrivebeskyttet felt, der er låst mod redigering. Dette felt bruges som reference for hver proformafaktura. |
| **Navn** | Fanen **Oversigt** | Angiv navnet på standardprojektkontrakten. Dette felt kan redigeres. | 
| **Valuta** | Fanen **Oversigt** | Angiv valutaen for standardprojektkontrakten. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Prisliste** | Fanen **Oversigt** | Angiv prislisten for standardprojektkontrakten. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Salgsmulighed** | Fanen **Oversigt** | Referencen til den sammenkædede salgsmulighed. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Kontrakt** | Fanen **Oversigt** | Referencen til den sammenkædede projektkontrakt. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Kunde** | Fanen **Oversigt** | Referencen til den sammenkædede projektkontrakt. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Beskrivelse** | Fanen **Oversigt** | Det tekstfelt, der beskriver fakturaen. Dette felt kan redigeres. | 
| **Faktureres til** og relaterede felter | **Fanen Oversigt** | Standard angives fra projektkontraktkunden. Dette felt kan redigeres.  | 
| **Status** | Fanen **Oversigt** | Angiver følgende indstillinger: **Aktiv**, **Lukket**, **Betalt** og **Annulleret** og kan redigeres. Ikke-understøttede statusser for Project Operations omfatter **Lukkede** og **Annullerede**. </br> Status angives til **Aktiv**, når fakturaen oprettes. </br>Statussen bør angives til kun at blive **Betalt**, når fakturaen er bekræftet.  | 
| **Projektfakturastatus** | Fanen **Oversigt** | Angiver følgende indstillinger: **Kladde**, **Under revision** og **Bekræftet** og kan redigeres. Fakturaen kan redigeres både i statusserne **Kladde** og **Gennemgås**. Fakturaen kan ikke redigeres, når den er bekræftet. | 
| **Detaljebeløb** | Fanen **Oversigt** | Summen af beløbene på alle fakturalinjerne efter forskud og fradrag. Et skrivebeskyttet felt, der er låst mod redigering.  Dette felt bruges til at beregne det endelige beløb. | 
| **Rabat (%)** | Fanen **Oversigt** | Du kan redigere feltet, hvis du vil angive en rabatprocent. Dette felt understøttes ikke af funktionaliteten Project Operations. Dette felt understøttes ikke.|  
| **Rabatbeløb** | Fanen **Oversigt** | Du kan redigere feltet, hvis du vil angive rabatbeløbet. Dette felt understøttes ikke af funktionaliteten Project Operations. Dette felt understøttes ikke. |  
| **Beløb før fragt** | **Fanen Oversigt** | Det samlede fakturabeløb, efter at rabatter er anvendt. Et skrivebeskyttet felt, der er låst mod redigering. Dette felt bruges til at beregne det endelige beløb.  | 
| **Fragtbeløb** | Fanen **Oversigt** | Du kan redigere feltet, hvis du vil angive fragtbeløbet. Dette felt understøttes ikke af funktionaliteten Project Operations. Dette felt understøttes ikke. |
| **Samlet moms** | Fanen **Oversigt** | Den samlede moms fra alle fakturalinjer på fakturaen. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Samlet beløb** | Fanen **Oversigt** | Summen af beløbet efter rabatter og moms. Summen er det beløb, som kunden skal betale. | 

## <a name="project-based-invoice-lines"></a>Projektbaserede fakturalinjer

I Project Operations er der altid én fakturalinje for hver projektkontraktlinje. Fakturalinjen oprettes, selvom der ikke er faktiske værdier. Følgende oplysninger er tilgængelige på en proformafakturalinje.

| Felt | Lokation | Beskrivelse | 
| --- | --- | --- |
| **Faktura-id** | Fanen **Generelt** | Referencen til faktura-id'et. Et skrivebeskyttet felt, der er låst mod redigering. Du kan bruge linket til faktura-id'et til at navigere tilbage til fakturaens overskrift. | 
| **Navn** | Fanen **Generelt** | Navnet på den fakturalinje, der som standard angives ud fra kontraktlinjenavnet. Dette felt kan redigeres. |
| **Project** | Fanen **Generelt** | Projektet på den relaterede projektkontraktlinje. Et skrivebeskyttet felt, der er låst mod redigering. Projektlinket kan bruges til at navigere til projektet. | 
| **Faktureringsmetode** | Fanen **Generelt** | Faktureringsmetoden på den relaterede projektkontraktlinje. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Kontraktlinjebeløb** | Fanen **Generelt** | Kontraktbeløber på den relaterede projektkontraktlinje. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Faktureret indtil dato** | Fanen **Generelt** | Summen af beløb for alle fakturalinjedetaljer på denne faktura. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Beløb** | Fanen **Generelt** | Summen af beløb for alle fakturernare fakturalinjedetaljer på denne faktura. Et skrivebeskyttet felt, der er låst mod redigering. Dette felt bruges til at beregne det endelige beløb i overskriften til fakturaen. | 
| **Moms** | Fanen **Generelt** | Summen af momsbeløb for alle fakturalinjedetaljer på denne fakturalinje. Et skrivebeskyttet felt, der er låst mod redigering. Dette felt bruges til at beregne det endelige momsbeløb i overskriften til fakturaen. | 
| **Samlet beløb** | Fanen **Generelt** | Summen af de samlede momsbeløb (**moms+beløb**) for alle fakturerbare fakturalinjedetaljer på denne fakturalinje. Et skrivebeskyttet felt, der er låst mod redigering. Dette felt bruges til at beregne det endelige beløb i overskriften til fakturaen. |

## <a name="invoice-line-details"></a>Fakturalinjedetaljer

Hver fakturalinje i en projektfaktura inkluderer oplysninger om fakturalinjer. Disse linjedetaljer er relateret til de ikke-fakturerede faktiske salgsværdier og milepæle, der vedrører den kontraktlinje, der henvises til på fakturalinjen. Alle disse transaktioner er markeret som **Klar til fakturering**.

For en linje i en **Faktura for tid og materialer** grupperes fakturalinjedetaljer i **Fakturerbar**, **Ikke-fakturerbar** og **Gratis** på siden **Fakturalinje**. **Fakturerbare fakturalinje**-detaljer føjes til fakturalinjetotalen. **Gratis** og **Ikke-fakturerbare faktiske værdier** føjes ikke til fakturalinjetotalen.

For en linje i en **Fastprisfaktura**, oprettes fakturalinjedetaljer ud fra milepæle, der er markeret som **Klar til fakturering** på den relaterede kontraktlinje. Når fakturalinjedetaljerne er oprettet fra en milepæl, bliver faktureringsstatussen for milepælen opdateret til **Kundefaktura er oprettet**.

### <a name="edit-invoice-line-details"></a>Rediger fakturalinjedetaljer

Følgende felter er tilgængelige på fakturalinjedetaljen, der er understøttet af en ikke-faktureret faktisk salgsværdi.

| Felt | Beskrivelse |
| --- | --- | 
| **Fakturalinje** | En referencen til **Fakturalinje-id'et**. Dette felt er skrivebeskyttet og låst mod redigering. Linket kan bruges til at navigere tilbage til fakturaens overskrift. | 
| **Beskrivelse** | En beskrivelse af fakturalinjedetaljen. Du kan som standard angive dette i feltet **Interne kommentarer** på **Tidsregistrering** og fra feltet **Beskrivelse** i **Udgiftsregistrering**. Feltet kan redigeres.| 
| **Ekstern beskrivelse** | En beskrivelse af fakturalinjedetaljen. Du kan som standard angive dette i feltet **Eksterne kommentarer** på **Tidsregistrering** og feltet **Beskrivelse** i **Udgiftsregistrering**. Feltet kan redigeres. Denne beskrivelse kan bruges til at angive, hvad der skal stå på den udskrevne faktura, som skal sendes til kunden. I Project Operations indeholder en proformafaktura ikke alle de nødvendige funktioner til konfiguration af udskriftsindstillinger for en faktura. | 
| **Startdato** | Dette er et skrivebeskyttet felt, der som standard angives fra den faktiske kilde. |
| **Project** | Dette er et skrivebeskyttet felt, der som standard angives fra den faktiske kilde til projektet på den relaterede kontraktlinje. |  
| **Opgave** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Transaktionskategori** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Rolle** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |  
| **Reserverbar ressource** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Ressourcevirksomhed** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Ressourceenhed** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Antal** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |  
| **Enhedsplan** | Hvis der er oplysninger om fakturalinjen for tid, angives dette altid til tid, og den kan ikke redigeres. For udgifter angives dette som standard fra kilden til de faktiske udgifter. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Enhed** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |  
| **Pris** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Valuta** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Beløb** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Skat** | Angives som standard fra de faktiske værdikilder. Feltet kan redigeres.| 
| **Samlet beløb** | Et beregnet felt, der er beregnet som **Beløb+moms**. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Faktureringstype** | Angives som standard fra de faktiske værdikilder. Feltet kan redigeres. Hvis du vælger **Fakturerbar**, tilføjes linjen til totalen på fakturalinjen. **Gratis** og **Ikke-fakturerbar** udelades fra fakturalinjetotalen.| 
| **Vælg produkt** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Produkt** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Produktnavn** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |  
| **Beskrivelse rekvirering** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Transaktionstype** | Dette er et skrivebeskyttet felt, der som standard angives fra den faktiske kilde for **Faktureret salg**. |  
| **Transaktionsklasse** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | 

Følgende felter er tilgængelige på en fakturalinjedetalje, der er understøttet af en milepæl.

| Felt | Beskrivelse |
| --- | --- | 
| **Fakturalinje** | Reference til **Fakturalinje-id'et**. Et skrivebeskyttet felt, der er låst mod redigering. Linket kan bruges til at navigere tilbage til fakturaens overskrift.  | 
| **Beskrivelse** | Beskrivelse af fakturalinjedetaljen. Angives som standard ud fra beskrivelsen af kildemilepælen. | 
|**Ekstern beskrivelse** | Beskrivelse af de fakturalinjedetaljer, der som standard angives i beskrivelsen af kildemilepælen. Dette felt kan bruges til at angive, hvad der skal stå på den udskrevne faktura, som skal sendes til kunden. En proformafaktura i Project Operations indeholder ikke alle de nødvendige funktioner til konfiguration af udskriftsindstillinger for en faktura. | 
| **Startdato** | Angives som standard fra datoen for **Milepælen** på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Project** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Opgave** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Transaktionskategori** | Et skrivebeskyttet felt, der er låst mod redigering. |
| **Rolle** | Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Reserverbar ressource** | Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Ressourceenhed** | Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Enhedsplan** | Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Enhed** | Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Pris** | Angives som standard ud fra beløbet på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Valuta** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Beløb** | Angives som standard ud fra beløbet på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Moms** | Angives som standard ud fra momsbeløbet på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Samlet beløb** | Angives som standard ud fra det udvidede beløb på kildemilepælen. Feltet kan redigeres. | 
| **Faktureringstype** | Angives altid som standard til **Fakturerbar**. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Transaktionstype** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | 
| **Transaktionsklasse** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | 

## <a name="refresh-invoice-transactions"></a>Opdater fakturatransaktioner

Hvis du har faktiske værdier, der indgik, efter at du har oprettet fakturaen, kan du inkludere disse faktiske værdier på fakturaen.

1. I **Visning af faktureringsefterslæb** skal du markere dataene som **Klar til fakturering**.   
2. Åbn kladdeproformafakturaen, og på båndet **Handlinger** skal du vælge **Opdatér fakturalinjetransaktioner**.

  Der oprettes fakturalinjedetaljer for alle faktiske tal, der er forældet og markeret som **Klar til fakturering**, men som ikke findes på fakturaen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
