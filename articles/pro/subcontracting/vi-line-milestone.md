---
title: Leverandørfakturalinjer for milepæle
description: I dette emne forklares det, hvordan du kan oprette leverandørfakturalinjer for milepæle på en underentreprise.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590615"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Leverandørfakturalinjer for milepæle

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan have leverandørfakturalinjer for milepæle, der er defineret på en underentrepriselinje. Projektledere kan bruge leverandørfakturalinjer for milepæle til at registrere omkostningerne til tjenester, der faktureres som milepælsbaserede omkostninger, der afholdes til tjenester eller produkter, som er faktureret for projektet.

Leverandørfakturalinjer for milepæle skal altid referere til en underentrepriselinje, der har en faktureringsmetode til fast pris. Når en leverandørfakturalinje refererer til en underentrepriselinje, kan projektledere afstemme og kontrollere de underliggende omkostninger til tid, udgifter eller materialer, der refererer til den pågældende underentrepriselinje, med den milepæl, som leverandøren fakturerer.

I følgende tabel er der oplysninger om felter på leverandørfakturalinjer for milepæle.

| Felt | Description | Funktionspåvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen for at hjælpe med identifikationen. | Dette navn vises som den første kolonne i alle opslag, der er baseret på leverandørfakturalinjer. |
| Description | En kort beskrivelse af tjenester og produkter, der faktureres af leverandører på leverandørfakturalinjen. | None |
| Underentreprise | Den underentreprise, som tjenesterne oprindeligt blev bestilt på. | Når der vælges en underentreprise til leverandørfakturaen, arver alle leverandørfakturalinjerne dette valg. En leverandørfaktura kan ikke have leverandørfakturalinjer, der refererer til forskellige underentrepriser. |
| Underentrepriselinje | Den underentrepriselinje, som tjenesterne blev bestilt på. Listen over de underentrepriselinjer, der kan vælges, er begrænset til linjerne på den valgte underentreprise. | Når der vælges en underentrepriselinje på en leverandørfakturalinje for milepæle, er felterne **Rolle** og **Transaktionskategori** og produktrelaterede felter ikke tilgængelige. Felterne **Mængde**, **Enhed** og **Enhedsgruppe** er heller ikke relevante for milepælsbaserede leverandørfakturalinjer. |
| Transaktionsdato | Den dato, hvor de faktiske omkostninger på leverandørfakturalinjen registreres i projektet. | None |
| Transaktionsklasse | Vælg **Milepæl** for at registrere en leverandørfaktura for en fuldført milepæl, der er defineret på en underentrepriselinje. | None |
| Milepæl | Vælg den milepæl, der er defineret på den relaterede underentrepriselinje, der er markeret som **Klar til fakturering**. | Milepæle i underentrepriser, der har statussen **Klar til fakturering**, kan vælges på en leverandørfakturalinje. |
| Project | Navnet på det projekt, som de tjenester, der faktureres, blev brugt på. | Dette felt er påkrævet, og må ikke være tomt. |
| Opgave | Navnet på det den projektopgave, som de tjenester, der faktureres, blev brugt på. Dette felt er kun tilgængeligt, hvis der er valgt et projekt. Det er valgfrit, om du vil vælge en projektopgave. | Hvis dette felt ikke udfyldes, kan projektlederen afstemme leverandørfakturalinjen med den transaktionsklasse på den relaterede underentrepriselinje, der registreres på en hvilken som helst opgave i projektet. Hvis leverandørfakturalinjen ikke refererer til en underentrepriselinje, og dette felt ikke udfyldes, knyttes de faktiske omkostninger, der er oprettet af leverandørfakturalinjen, ikke til ikke-fakturerede faktiske salgsværdier. Hvis der i dette tilfælde konfigureres opgavebaseret fakturering, kan omkostningerne muligvis ikke faktureres slutbrugeren. |
| Beløb for milepæl | Angiv den værdi for den milepæl, der er defineret på underentrepriselinjen, der er markeret som klar til fakturering. | None |
| Moms | Angiv omsætningsskattebeløbet. | None |
| Samlet beløb | Det samlede beløb på leverandørfakturalinjen, herunder moms. Dette felt beregnes som *Milepælsbeløb* + *Moms*. | None |

> [!NOTE]
> Når der oprettes en leverandørfakturalinje, der refererer til en milepæl i en underentrepriselinje, opdateres statussen for underentreprisemilepælen til **Leverandørfaktura oprettet**. Når den pågældende leverandørfaktura bekræftes, opdateres statussen for milepælen på underentrepriselinjen til **Leverandørfaktura bekræftet**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
