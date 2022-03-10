---
title: Administrer en proformafaktura på projektet
description: Dette emne indeholder oplysninger om, hvordan du arbejder med projektproformafakturaer.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f14cf9d5ee25247500180081b8f407ee311db481a5ef5eac330e75d45baba54a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997419"
---
# <a name="manage-a-proforma-project-invoice"></a>Administrer en proformafaktura på projektet 

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I Dynamics 365 Project Operations er proformafakturaer bygget som en udvidelse til fakturaerne i Dynamics 365 Sales. Der er dog mange forskelle i faktureringsprocessen mellem Sales og Project Operations, når det kommer til fakturering. Det er f.eks. ikke muligt at oprette en ny faktura fra siden **Fakturaliste** i Project Operations, men det er muligt at gøre det i Sales. Disse forskelle og udvidelser kan bruges til at understøtte faktureringsprocesser for projekter, der adskiller sig fra en typisk faktura for en salgsordre.

> [!IMPORTANT]
> På grund af forskellene skal du ikke skifte mellem at fakturere i Sales og Project Operations.

## <a name="invoice-header"></a>Fakturaoverskrift

Følgende oplysninger er tilgængelige i forbindelse med en overskrift til en proformafaktura i Project Operations.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| **Faktura-id** | Fanen **Oversigt** | App-id'et, der genereres automatisk, når en proformafaktura oprettes. Et skrivebeskyttet felt, der er låst mod redigering. | Dette felt bruges som reference for hver proformafaktura. |
| **Navn** | Fanen **Oversigt** | Angiv navnet på standardprojektkontrakten. Dette felt kan redigeres af brugeren. | &nbsp;  |
| **Valuta** | Fanen **Oversigt** | Angiv valutaen for standardprojektkontrakten. Et skrivebeskyttet felt, der er låst mod redigering. |&nbsp; |
| **Prisliste** | Fanen **Oversigt** | Angiv prislisten for standardprojektkontrakten. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Salgsmulighed** | Fanen **Oversigt** | Referencen til den sammenkædede salgsmulighed. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp;  |
| **Kontrakt** | Fanen **Oversigt** | Referencen til den sammenkædede projektkontrakt. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Kunde** | Fanen **Oversigt** | Referencen til den sammenkædede projektkontrakt. Et skrivebeskyttet felt, der er låst mod redigering. |&nbsp;  |
| **Beskrivelse** | Fanen **Oversigt** | Det tekstfelt, der beskriver fakturaen. Dette felt kan redigeres af brugeren. | &nbsp; |
| **Faktureres til** og relaterede felter | **Fanen Oversigt** | Standard angives fra projektkontraktkunden. Dette felt kan redigeres af brugeren.  | &nbsp; |
| **Status** | Fanen **Oversigt** | Angiver følgende indstillinger: **Aktiv**, **Lukket**, **Betalt** og **Annulleret** og kan redigeres af brugeren. | Ikke-understøttede statusser for Project Operations omfatter **Lukkede** og **Annullerede**. </br> Status angives til **Aktiv**, når fakturaen oprettes. </br>Statussen bør angives til kun at blive **Betalt**, når fakturaen er bekræftet. |
| **Projektfakturastatus** | Fanen **Oversigt** | Angiver følgende indstillinger: **Kladde**, **Gennemgås** og **Bekræftet** og kan redigeres af brugeren. | Fakturaen kan redigeres både i statusserne **Kladde** og **Gennemgås**. Fakturaen kan ikke redigeres, når den er bekræftet. |
| **Detaljebeløb** | Fanen **Oversigt** | Summen af beløbene på alle fakturalinjerne efter forskud og fradrag. Et skrivebeskyttet felt, der er låst mod redigering. | Dette felt bruges til at beregne det endelige beløb. |
| **Rabat (%)** | Fanen **Oversigt** | Du kan redigere feltet, hvis du vil angive en rabatprocent. Dette felt understøttes ikke af funktionaliteten Project Operations. | Dette felt understøttes ikke. |
| **Rabatbeløb** | Fanen **Oversigt** | Du kan redigere feltet, hvis du vil angive rabatbeløbet. Dette felt understøttes ikke af funktionaliteten Project Operations. | Dette felt understøttes ikke. |
| **Beløb før fragt** | **Fanen Oversigt** | Det samlede fakturabeløb, efter at rabatter er anvendt. Et skrivebeskyttet felt, der er låst mod redigering. | Dette felt bruges til at beregne det endelige beløb. |
| **Fragtbeløb** | Fanen **Oversigt** | Du kan redigere feltet, hvis du vil angive fragtbeløbet. Dette felt understøttes ikke af funktionaliteten Project Operations. | Dette felt understøttes ikke. |
| **Samlet moms** | Fanen **Oversigt** | Den samlede moms fra alle fakturalinjer på fakturaen. Et skrivebeskyttet felt, der er låst mod redigering. | Ingen. |
| **Samlet beløb** | Fanen **Oversigt** | Summen af beløbet efter rabatter og moms. | Summen er det beløb, som kunden skal betale. |
## <a name="project-based-invoice-lines"></a>Projektbaserede fakturalinjer

I Project Operations er der altid én fakturalinje for hver projektkontraktlinje. Fakturalinjen oprettes, selvom der ikke er faktiske værdier. Følgende oplysninger er tilgængelige på en proformafakturalinje.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| **Faktura-id** | Fanen **Generelt** | Referencen til faktura-id'et. Et skrivebeskyttet felt, der er låst mod redigering. | Du kan bruge linket til faktura-id'et til at navigere tilbage til fakturaens overskrift. |
| **Navn** | Fanen **Generelt** | Navnet på den fakturalinje, der som standard angives ud fra kontraktlinjenavnet. Dette felt kan redigeres af brugeren. | &nbsp; |
| **Project** | Fanen **Generelt** | Projektet på den relaterede projektkontraktlinje. Et skrivebeskyttet felt, der er låst mod redigering. | Projektlinket kan bruges til at navigere til projektet. |
| **Faktureringsmetode** | Fanen **Generelt** | Faktureringsmetoden på den relaterede projektkontraktlinje. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Kontraktlinjebeløb** | Fanen **Generelt** | Kontraktbeløber på den relaterede projektkontraktlinje. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Faktureret indtil dato** | Fanen **Generelt** | Summen af beløb for alle fakturalinjedetaljer på denne faktura. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Beløb** | Fanen **Generelt** | Summen af beløb for alle fakturernare fakturalinjedetaljer på denne faktura. Et skrivebeskyttet felt, der er låst mod redigering. | Dette felt bruges til at beregne det endelige beløb i overskriften til fakturaen. |
| **Moms** | Fanen **Generelt** | Summen af momsbeløb for alle fakturalinjedetaljer på denne fakturalinje. Et skrivebeskyttet felt, der er låst mod redigering. | Dette felt bruges til at beregne det endelige momsbeløb i overskriften til fakturaen. |
| **Samlet beløb** | Fanen **Generelt** | Summen af de samlede momsbeløb (**moms+beløb**) for alle fakturerbare fakturalinjedetaljer på denne fakturalinje. Et skrivebeskyttet felt, der er låst mod redigering. | Dette felt bruges til at beregne det endelige beløb i overskriften til fakturaen. |


## <a name="invoice-line-details"></a>Fakturalinjedetaljer

Hver fakturalinje i en projektfaktura inkluderer oplysninger om fakturalinjer. Disse linjedetaljer er relateret til de ikke-fakturerede faktiske salgsværdier og milepæle, der vedrører den kontraktlinje, der henvises til på fakturalinjen. Alle disse transaktioner er markeret som **Klar til fakturering**.

For en linje i en **Faktura for tid og materialer** grupperes fakturalinjedetaljer i **Fakturerbar**, **Ikke-fakturerbar** og **Gratis** på siden **Fakturalinje**. **Fakturerbare fakturalinje**-detaljer føjes til fakturalinjetotalen. **Gratis** og **Ikke-fakturerbare faktiske tal** svarer ikke til fakturalinjetotalen.

For en linje i en **Fastprisfaktura**, oprettes fakturalinjedetaljer ud fra milepæle, der er markeret som **Klar til fakturering** på den relaterede kontraktlinje. Når fakturalinjedetaljerne er oprettet fra en milepæl, bliver faktureringsstatussen for milepælen opdateret til **Kundefaktura er oprettet**.

### <a name="edit-invoice-line-details"></a>Rediger fakturalinjedetaljer

Følgende felter er tilgængelige på en fakturalinjedetalje, der er understøttet af en ikke-faktureret faktisk salgsværdi:

| Felt | Beskrivelse | Downstream-virkning |
| --- | --- | --- |
| **Fakturalinje** | En referencen til **Fakturalinje-id'et**. Et skrivebeskyttet felt, der er låst mod redigering. | Linket kan bruges til at navigere tilbage til fakturaens overskrift. |
| **Beskrivelse** | En beskrivelse af fakturalinjedetaljen. Du kan som standard angive dette i feltet **Interne kommentarer** på **Tidsregistrering** og fra feltet **Beskrivelse** i **Udgiftsregistrering**. Feltet kan redigeres af brugeren.| &nbsp; |
| **Ekstern beskrivelse** | En beskrivelse af fakturalinjedetaljen. Du kan som standard angive dette i feltet **Eksterne kommentarer** på **Tidsregistrering** og feltet **Beskrivelse** i **Udgiftsregistrering**. Feltet kan redigeres af brugeren. | Denne beskrivelse kan bruges til at angive, hvad der skal stå på den udskrevne faktura, som skal sendes til kunden. I Project Operations indeholder en proformafaktura ikke alle de nødvendige funktioner til konfiguration af udskriftsindstillinger for en faktura. |
| **Startdato** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdikilde. |
| **Project** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Angives som standard for projektet på den relaterede kontraktlinje. |
| **Opgave** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdikilde. På en rulleliste vises alle de opgaver, der er knyttet til den relaterede projektkontraktlinje.  |
| **Transaktionskategori** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk kilde. |
| **Rolle** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdikilde. |
| **Reserverbar ressource** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk kilde. |
| **Ressourceenhed** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdikilde. |
| **Antal** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdikilde. |
| **Enhedsplan** | Hvis der er oplysninger om fakturalinjen for tid, angives dette altid til tid, og den kan ikke redigeres. For udgifter angives dette som standard fra kilden til de faktiske udgifter. Et skrivebeskyttet felt, der er låst mod redigering. | Angives som standard til **Tid** på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdi. |
| **Enhed** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdikilde |
| **Pris** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Feltet kan redigeres på en ny fakturalinjedetalje, der ikke er understøttet af en faktisk værdikilde. Hvis der ikke angives en værdi, angives den som standard, når den er blevet **Gemt**. |
| **Valuta** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Angives som standard fra fakturaoverskriften, når der oprettes en ny fakturadetalje, som ikke understøttes af faktiske værdier.  Et skrivebeskyttet felt, der er låst mod redigering. |
| **Beløb** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Beregnes som **Antal \* Pris** ved oprettelse af en ny fakturadetalje uden understøttelse af en faktisk værdi. Den beregnes efter at være blevet **Gemt**. Et skrivebeskyttet felt, der er låst mod redigering. |
| **Moms** | Angives som standard fra de faktiske værdikilder. Feltet kan redigeres af brugeren | Feltet kan redigeres af brugeren, når der oprettes en ny fakturalinjedetalje, som ikke understøttes en faktisk værdi. |
| **Samlet beløb** | Et beregnet felt, der er beregnet som **Beløb+moms**. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Faktureringstype** | Angives som standard fra de faktiske værdikilder. Feltet kan redigeres af brugeren. | Hvis du vælger **Fakturerbar**, tilføjes linjen til totalen på fakturalinjen. **Gratis** og **Ikke-fakturerbar** udelades fra fakturalinjetotalen. |
| **Vælg produkt** | Dette er et skrivebeskyttet felt og er som standard angivet fra den faktiske kilde. | Når du opretter en ny fakturalinjedetalje uden en bagvedliggende faktisk værdi, kan dette felt redigeres. |
| **Produkt** | Dette er et skrivebeskyttet felt og er som standard angivet fra den faktiske kilde. | Når du opretter en ny fakturalinjedetalje uden en bagvedliggende faktisk værdi, kan dette felt redigeres, hvis feltet **Vælg produkt** er angivet til **Eksisterende produkt**. |
| **Produktnavn** | Dette er et skrivebeskyttet felt og er som standard angivet fra den faktiske kilde. | På en ny fakturalinje, hvor produkt-id'et vælges fra katalog, angives dette felt til produktnavnet. I forbindelse med et rekvireret produkt angives feltet til navnet, der skal rekvireres. |
| **Beskrivelse rekvirering** | Dette felt er skrivebeskyttet og er som standard angivet fra den faktiske kilde. | Når du opretter en ny fakturalinjedetalje uden en bagvedliggende faktisk værdi, kan du tilføje et rekvireret produkt i beskrivelsen af produktet. |
| **Transaktionstype** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Angives som standard til **Faktureret salg** og låses, når der oprettes en ny **Fakturalinjedetalje**, som ikke er understøttet af en faktisk værdi.  |
| **Transaktionsklasse** | Angives som standard fra de faktiske værdikilder. Et skrivebeskyttet felt, der er låst mod redigering. | Angives som standard på baggrund af, om brugeren vælger at oprette en fakturalinjedetaljer for **Tid**, **Udgifter**, **Materiale** eller **Gebyr**, samtidig med at der oprettes en ny **Fakturalinjedetalje** uden en bagvedliggende faktisk værdi. Låst mod redigering. |

Følgende felter er tilgængelige på en fakturalinjedetalje, der er understøttet af en milepæl:

| Felt | Beskrivelse | Downstream-virkning |
| --- | --- | --- |
| **Fakturalinje** | Reference til **Fakturalinje-id'et**. Et skrivebeskyttet felt, der er låst mod redigering. | Linket kan bruges til at navigere tilbage til fakturaens overskrift. |
| **Beskrivelse** | Beskrivelse af fakturalinjedetaljen. Angives som standard ud fra beskrivelsen af kildemilepælen. | &nbsp; |
|**Ekstern beskrivelse** | Beskrivelse af de fakturalinjedetaljer, der som standard angives i beskrivelsen af kildemilepælen. | Dette felt kan bruges til at angive, hvad der skal stå på den udskrevne faktura, som skal sendes til kunden. En proformafaktura i Project Operations indeholder ikke alle de nødvendige funktioner til konfiguration af udskriftsindstillinger for en faktura. |
| **Startdato** | Angives som standard fra datoen for **Milepælen** på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Project** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Opgave** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Transaktionskategori** | Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Rolle** | Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Reserverbar ressource** | Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Ressourceenhed** | Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Enhedsplan** | Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Enhed** | Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Pris** | Angives som standard ud fra beløbet på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Valuta** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. |&nbsp; |
| **Beløb** | Angives som standard ud fra beløbet på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Moms** | Angives som standard ud fra momsbeløbet på kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Samlet beløb** | Angives som standard ud fra det udvidede beløb på kildemilepælen. Feltet kan redigeres af brugeren | &nbsp; |
| **Faktureringstype** | Angives altid som standard til **Fakturerbar**. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Transaktionstype** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |
| **Transaktionsklasse** | Angives som standard fra kildemilepælen. Et skrivebeskyttet felt, der er låst mod redigering. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Opret nye fakturalinjedetaljer

I fakturalinjer med tid og materialer kan du oprette nye fakturalinjedetaljer. Disse fakturalinjedetaljer er ikke understøttet af en faktisk værdi. På fakturalinjen for en fakturalinje med tid og materialer kan du vælge **Ny** for at oprette en ny fakturalinjedetalje for de transaktionsklasser, der er medtaget på kontraktlinjen.

## <a name="refresh-invoice-transactions"></a>Opdater fakturatransaktioner

Hvis du har faktiske værdier, der indgik, efter at du har oprettet fakturaen, kan du inkludere disse faktiske værdier på fakturaen.

1. I **Visning af faktureringsefterslæb** skal du markere dataene som **Klar til fakturering**.   
2. Åbn kladden for at oprette en proformafaktura, og klik på **Handlinger** på båndet og derefter på **Opdater fakturalinjetransaktioner**.

  Dermed oprettes fakturalinjedetaljer for eventuelle faktiske værdier, der har en tidligere dato og er markeret som **Klar til fakturering**, men som ikke er inkluderet i fakturaen.

## <a name="product-based-invoice-lines"></a>Produktbaserede fakturalinjer

I Project Operations kan du oprette fakturalinjer for produkter, der ikke er gælder for et andet projekt eller for alle projekter, sammen med projektbaserede fakturalinjer. Disse fakturalinjer oprettes som produktbaserede kontraktlinjer, og når de er markeret som klar til fakturering, tilføjes de som produktbaserede fakturalinjer.

Når du har tilføjet produktbaserede fakturalinjer, kan de ikke ændres. De kan dog slettes fra proformafakturakladden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
