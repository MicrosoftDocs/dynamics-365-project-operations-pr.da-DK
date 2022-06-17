---
title: Leverandørfakturalinjer for tid
description: I denne artikel forklares det, hvordan du registrerer leverandørfakturalinjer for de tidsomkostninger, som underleverandører har leveret.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927535"
---
# <a name="vendor-invoice-lines-for-time"></a>Leverandørfakturalinjer for tid

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan have leverandørfakturalinjer for tid. Projektledere kan bruge leverandørfakturalinjer for tid til at registrere omkostningerne for underleverandørtid på projekter.

Leverandørfakturalinjer for tid refererer muligvis ikke til en underentrepriselinje for tid. Hvis en leverandørfakturalinje for tid refererer til en underentreprise, kan projektledere afstemme og kontrollere, hvilken tid der faktureres leverandørfakturalinjen, med brugen af tid, der registreres af underleverandører og godkendes af projektledere på projektet.

I følgende tabel er der oplysninger om felter på leverandørfakturalinjer for tid.

| Felt | Description | Funktionspåvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen for at hjælpe med identifikationen. | Dette navn vises som den første kolonne i alle opslag, der er baseret på leverandørfakturalinjer. |
| Description | En kort beskrivelse af de tjenester, der faktureres af leverandører på leverandørfakturalinjen. | None |
| Underentreprise | Den underentreprise, som tjenesterne oprindeligt blev bestilt på. | Når der vælges en underentreprise til leverandørfakturaen, arver alle leverandørfakturalinjerne dette valg. En leverandørfaktura kan ikke have leverandørfakturalinjer, der refererer til forskellige underentrepriser. |
| Underentrepriselinje | Den underentrepriselinje, som tjenesterne blev bestilt på. Listen over de underentrepriselinjer, der kan vælges, er begrænset til linjerne på den valgte underentreprise. | Når der vælges en underentrepriselinje på en leverandørfakturalinje for tid, angives standardværdierne for felterne **Projekt**, **Rolle** og **Reserverbar ressource** fra de tilsvarende felter på underentrepriselinjen. Hvis den valgte underentrepriselinje har værdier i felterne **Projekt**, **Rolle** og **Reserverbar**, kan værdierne i de tilsvarende felter på leverandørfakturalinjen ikke adskille sig fra disse værdier. |
| Transaktionsdato | Den dato, hvor de faktiske omkostninger på leverandørfakturalinjen registreres i projektet. | None |
| Transaktionsklasse | Standardværdien er **Tid**. | Værdien **Tid** indikerer, at leverandørfakturalinjen bruges til at registrere fakturabeløbet for underleverandørens tid. |
| Project | Navnet på det projekt, som de tjenester, der faktureres, blev brugt på. | Dette felt er påkrævet, og må ikke være tomt. |
| Opgave | Navnet på det den projektopgave, som de tjenester, der faktureres, blev brugt på. Dette felt er kun tilgængeligt, hvis der er valgt et projekt. Det er valgfrit, om du vil vælge en projektopgave. | Hvis dette felt ikke udfyldes, kan projektlederen afstemme leverandørfakturalinjen med den tid, der registreres for underleverandørers ressourcer på en hvilken som helst opgave i projektet. Hvis leverandørfakturalinjen ikke refererer til en underentrepriselinje, og dette felt ikke udfyldes, knyttes de faktiske omkostninger, der er oprettet af leverandørfakturalinjen, ikke til ikke-fakturerede faktiske salgsværdier. Hvis der i dette tilfælde konfigureres opgavebaseret fakturering, kan omkostningerne muligvis ikke faktureres slutbrugeren. |
| Rolle | Rollen for de underentrepriseressourcer, hvor tid faktureres. | I dette felt angives den rolle, der udføres af de underleverandørressourcer, hvis tid faktureres på leverandørfakturaen. |
| Reserverbar ressource | Navnet på den underleverandør, hvor tid faktureres. Det er valgfrit, om du vil vælge en reserverbar ressource. | Hvis dette felt ikke udfyldes, kan projektlederen afstemme leverandørfakturalinjen med den tid, der registreres for enhver ressource, som tilhører leverandører, på leverandørfakturalinjen. |
| Antal | Angiv antal timer, der faktureres af leverandøren på fakturalinjen. |None |
| Enhedsgruppe | Standardværdien er **Tidsenhedsgruppe** og kan ikke ændres. | None |
| Enhed | Standardværdien er basisenheden for timer fra tidsenhedsgruppen. Du kan ændre denne værdi for at indkøbe en hvilken som helst tidsenhedsgruppe såsom dag eller uge. | Kombinationen af værdierne **Rolle** og **Enhed** bruges som standarden eller beregnede værdier for feltet **Enhedspris** for leverandørfakturalinjen. |
| Enhedspris | Standardenhedsprisen bruger kombinationen af værdierne for **Rolle** og **Enhed** fra den projektprisliste, der er anvendelig for transaktionsdatoen for leverandørfakturalinjen. | Hvis prisen på den relevante projektprisliste er angivet i en enhed, der adskiller sig fra enheden på leverandørfakturalinjen, bruges enhedskonverteringen til at beregne enhedsprisen. |
| Subtotal | Dette skrivebeskyttede felt beregnes som *Mængde* &times; *Enhedspris*, hvis der angives værdier i begge felter for **Mængde** og **Enhedspris**. Hvis det ene eller begge disse felter er tomme, kan du angive en værdi i dette felt. | None |
| Moms | Angiv omsætningsskattebeløbet. | None |
| Samlet beløb | Det samlede beløb på leverandørfakturalinjen, herunder moms. Denne værdi beregnes som *Delsum* + *Salgsmoms*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
