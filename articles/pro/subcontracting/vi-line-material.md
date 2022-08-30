---
title: Leverandørfakturalinjer for produkter
description: I denne artikel forklares det, hvordan du registrerer leverandørfakturalinjer for produkter og bruger de forskellige felter til at registrere produktkøb fra leverandører.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261551"
---
# <a name="vendor-invoice-lines-for-products"></a>Leverandørfakturalinjer for produkter

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan have leverandørfakturalinjer for produkter (kaldes også materiale). Projektledere kan bruge leverandørfakturalinjer for produkter til at registrere omkostningerne for produkter, der er købt på projekter.

Leverandørfakturalinjer for produkter refererer muligvis ikke til en underentrepriselinje for materiale. Hvis en leverandørfakturalinje for et produkt refererer til en underentreprise, kan projektledere afstemme og kontrollere, hvilke produkter der faktureres leverandørfakturalinjen, med brugen af købte produkter, der registreres og godkendes af projektledere.

I følgende tabel er der oplysninger om felter på leverandørfakturalinjer for produkter.

| Felt | Description | Funktionspåvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen for at hjælpe med identifikationen. | Dette navn vises som den første kolonne i alle opslag, der er baseret på leverandørfakturalinjer. |
| Description | En kort beskrivelse af de produkter, der faktureres af leverandører på leverandørfakturalinjen. | None |
| Underentreprise | Den underentreprise, som produkterne oprindeligt blev bestilt på. | Når der vælges en underentreprise til leverandørfakturaen, arver alle leverandørfakturalinjerne dette valg. En leverandørfaktura kan ikke have leverandørfakturalinjer, der refererer til forskellige underentrepriser. |
| Underentrepriselinje | Den underentrepriselinje, som produkterne blev bestilt på. Listen over de underentrepriselinjer, der kan vælges, er begrænset til linjerne på den valgte underentreprise. | Når der vælges en underentrepriselinje på en leverandørfakturalinje for produkter, angives standardværdierne for felterne **Projekt**, **Opgave** og **Produkt** fra de tilsvarende felter på underentrepriselinjen. Hvis den valgte underentrepriselinje har værdier i felterne **Projekt**, **Opgave** og **Produkt**, kan værdierne i de tilsvarende felter på leverandørfakturalinjen ikke adskille sig fra disse værdier. |
| Transaktionsdato | Den dato, hvor de faktiske omkostninger på leverandørfakturalinjen registreres i projektet. | None|
| Transaktionsklasse | Når produkterne faktureres, skal dette felt angives til **Materiale**. | Værdien **Materiale** indikerer, at leverandørfakturalinjen bruges til at registrere fakturabeløbet for materiale, der er købt. |
| Project | Navnet på det projekt, som de produkter, der faktureres, blev brugt på. | Dette felt er påkrævet, og må ikke være tomt. |
| Opgave | Navnet på den projektopgave, som de produkter, der faktureres, blev brugt på. Dette felt er kun tilgængeligt, hvis der er valgt et projekt. Det er valgfrit, om du vil vælge en projektopgave. | Hvis dette felt ikke udfyldes, kan projektlederen afstemme leverandørfakturalinjen med det købte produkt, der bruges på en hvilken som helst opgave i projektet. Hvis leverandørfakturalinjen ikke refererer til en underentrepriselinje, og dette felt ikke udfyldes, knyttes de faktiske omkostninger, der er oprettet af leverandørfakturalinjen, ikke til ikke-fakturerede faktiske salgsværdier. Hvis der i dette tilfælde konfigureres opgavebaseret fakturering, kan omkostningerne ikke faktureres slutbrugeren. |
| Vælg produkt | Vælg, om produktet, der faktureres, er et eksisterende produkt fra kataloget, eller et produkt, der skal indkøbes. | Standardværdien angives fra underentrepriselinjen, når der vælges en underentrepriselinje. |
| Produkt | Vælg produktet fra kataloget. Hvis produktet er et indkøbt produkt, skal du angive navnet på produktet. | Dette felt bruges til at angive standardindkøbspriser for eksisterende produkter. |
| Antal | Angiv den mængde af materialer, der faktureres af leverandøren på denne fakturalinje. | None |
| Enhedsgruppe | Vælg enhedsgruppen for den enhed, som det antal, der faktureres, angives i. | None |
| Enhed | Standardværdien er basisenheden for den valgte tidsenhedsgruppe. Du kan ændre denne værdi for at betale i en hvilken som helst enhed i den valgte enhedsgruppe. | Kombinationen af værdierne **Produkt** og **Enhed** bruges som standarden eller beregnede værdier for feltet **Enhedspris** for leverandørfakturalinjen. |
| Enhedspris | Standardenhedsprisen bruger kombinationen af værdierne for **Produkt** og **Enhed** fra den projektprisliste, der er anvendelig for transaktionsdatoen for leverandørfakturalinjen. | None |
| Subtotal | Dette skrivebeskyttede felt beregnes som *Mængde* &times; *Enhedspris*, hvis der angives værdier i begge felter for **Mængde** og **Enhedspris**. Hvis det ene eller begge disse felter er tomme, kan du angive en værdi i dette felt. | None |
| Moms | Angiv omsætningsskattebeløbet. | None |
| Samlet beløb | Det samlede beløb på leverandørfakturalinjen, herunder moms. Denne værdi beregnes som *Delsum* + *Salgsmoms*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
