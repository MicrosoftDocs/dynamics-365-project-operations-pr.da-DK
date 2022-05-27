---
title: Leverandørfakturalinjer for udgiftskategorier
description: I dette emne forklares det, hvordan du registrerer leverandørfakturalinjer for udgiftskategorier.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579529"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Leverandørfakturalinjer for udgiftskategorier

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan have leverandørfakturalinjer for udgiftskategorier. Projektledere kan bruge leverandørfakturalinjer for udgiftskategorier til at registrere omkostningerne for tjenester, der er indkøbt som udgiftskategorier.

Leverandørfakturalinjer for udgiftskategorier refererer muligvis ikke til en underentrepriselinje for udgiftskategorier. Hvis en leverandørfakturalinje for udgiftskategorier refererer til en underentreprise, kan projektledere afstemme og kontrollere, hvilke udgifter der faktureres af leverandørfakturalinjen, med brugen af udgifter, der registreres på disse udgiftskategorier og godkendes af projektledere på projektet.

I følgende tabel er der oplysninger om felter på leverandørfakturalinjer for udgiftskategorier.

| Felt | Description | Funktionspåvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen for at hjælpe med identifikationen. | Dette navn vises som den første kolonne i alle opslag, der er baseret på leverandørfakturalinjer. |
| Description | En kort beskrivelse af de tjenester, der faktureres af leverandører på leverandørfakturalinjen. | None |
| Underentreprise | Den underentreprise, som tjenesterne oprindeligt blev bestilt på. | Når der vælges en underentreprise til leverandørfakturaen, arver alle leverandørfakturalinjerne dette valg. En leverandørfaktura kan ikke have leverandørfakturalinjer, der refererer til forskellige underentrepriser. |
| Underentrepriselinje | Den underentrepriselinje, som tjenesterne blev bestilt på. Listen over de underentrepriselinjer, der kan vælges, er begrænset til linjerne på den valgte underentreprise. | Når der vælges en underentrepriselinje på en leverandørfakturalinje for udgiftskategorier, angives standardværdierne for felterne **Projekt**, **Opgave** og **Transaktionskategori** fra de tilsvarende felter på underentrepriselinjen. Hvis den valgte underentrepriselinje har værdier i felterne **Projekt**, **Projektopgave** og **Transaktionskategori**, kan værdierne i de tilsvarende felter på leverandørfakturalinjen ikke adskille sig fra disse værdier. |
| Transaktionsdato | Den dato, hvor de faktiske omkostninger på leverandørfakturalinjen registreres i projektet. |None |
| Transaktionsklasse | Vælg **Udgifter** for at registrere en leverandørfaktura for en udgiftskategori. | Værdien **Udgift** indikerer, at leverandørfakturalinjen bruges til at registrere fakturabeløbet for tjenester, der er købt, som udgiftskategorier. |
| Project | Navnet på det projekt, som de tjenester, der faktureres, blev brugt på. | Dette felt er påkrævet, og må ikke være tomt. |
| Opgave | Navnet på det den projektopgave, som de tjenester, der faktureres, blev brugt på. Dette felt er kun tilgængeligt, hvis der er valgt et projekt. Det er valgfrit, om du vil vælge en projektopgave. | Hvis dette felt ikke udfyldes, kan projektlederen afstemme leverandørfakturalinjen med udgifter, der er registreret på en hvilken som helst opgave i projektet. Hvis leverandørfakturalinjen ikke refererer til en underentrepriselinje, og dette felt ikke udfyldes, knyttes de faktiske omkostninger, der er oprettet af leverandørfakturalinjen, ikke til ikke-fakturerede faktiske salgsværdier. Hvis der i dette tilfælde konfigureres opgavebaseret fakturering, kan omkostningerne muligvis ikke faktureres slutbrugeren. |
| Transaktionskategori | Den transaktionskategori, der faktureres. Der skal oprettes en tilsvarende udgiftskategori for den valgte transaktionskategori. | Kombinationen af værdierne **Transaktionskategori** og **Enhed** bruges som standarden eller beregnede værdier for feltet **Enhedspris** for leverandørfakturalinjen. |
| Antal | Angiv den mængde, der faktureres af leverandøren på fakturalinjen. |None|
| Enhedsgruppe | Der angives en standardværdi på baggrund af enhedsgruppen for den valgte transaktionskategori. | None |
| Enhed | Standardværdien er basisenheden for den valgte tidsenhedsgruppe. Du kan ændre denne værdi for at købe i en hvilken som helst enhed i enhedsgruppen. | Kombinationen af værdierne **Transaktionskategori** og **Enhed** bruges som standarden eller beregnede værdier for feltet **Enhedspris** for leverandørfakturalinjen. |
| Enhedspris | Standardenhedsprisen bruger kombinationen af værdierne for **Transaktionskategori** og **Enhed** fra den projektprisliste, der er anvendelig for transaktionsdatoen for leverandørfakturalinjen. | Hvis prisen på den relevante projektprisliste er angivet i en enhed, der adskiller sig fra enheden på leverandørfakturalinjen, bruges enhedskonverteringen til at beregne enhedsprisen. |
| Subtotal | Dette skrivebeskyttede felt beregnes som *Mængde* &times; *Enhedspris*, hvis der angives værdier i begge felter for **Mængde** og **Enhedspris**. Hvis det ene eller begge disse felter er tomme, kan du angive en værdi i dette felt.| None |
| Moms | Angiv omsætningsskattebeløbet. | None |
| Samlet beløb | Det samlede beløb på leverandørfakturalinjen, herunder moms. Denne værdi beregnes som *Delsum* + *Salgsmoms*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
