---
title: Underentrepriselinjer for tid
description: I dette emne forklares det, hvordan du registrerer underentrepriselinjer for tid og registrerer køb af tid fra leverandører.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547237"
---
# <a name="subcontract-lines-for-time"></a>Underentrepriselinjer for tid

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En underentreprise i Dynamics 365 Project Operations kan have en underentrepriselinje for tid. Underleverandørlinjer for tid gør det muligt for en projektleder at købe leverandørressourcetid for at besætte projektopgaver og ressourcekrav med medarbejdere.

For at oprette en underentrepriselinje for tid i Project Operations skal du fuldføre følgende trin.

1. I navigationsruden skal du vælge **Underentrepriser** og åbne en underentreprise.
2. På fanen **Underentrepriselinjer** skal du vælge **Ny** for at oprette en ny underentrepriselinje.
3. På siden **Hurtig oprettelse** skal du i feltet **Transaktionsklasse** vælge **Tid**.
4. Angiv de resterende feltoplysninger, og vælg derefter **Gem**.

  Følgende tabel indeholder oplysninger om felterne på siden **Underentrepriselinje** og siden **Hurtig oprettelse**.

| **Felt** | **Beskrivelse** | **Funktionspåvirkning** |
| --- | --- | --- |
| Navn | Navnet på underentrepriselinjen for at hjælpe med identifikationen. | Dette vises som den første kolonne i alle opslag baseret på underentrepriselinjer. |
| Beskrivelse | En kort beskrivelse af de tjenester, der købes på underentrepriselinjen. |Intet |
| Linjetype |   Dette felts standardværdi er **Mængdebaseret**.| Intet |
| Faktureringsmetode | Dette er en grupperet indstilling, der repræsenterer de to primære kontraktmodeller, som understøttes af Project Operations: **Fast pris** og **Tid og materialer**. | På grundlag af den valgte faktureringsmetode gøres en milepælsbaseret fakturaplan tilgængelig for underentrepriselinjer med faktureringsmetoden Fast pris. |
| Transaktionsklasse | Standardværdien er **Tid**. | Dette angiver, at underentrepriselinjen bruges til at registrere et køb af underentreprisens tid. |
| Rolle | Vælg rollen for de underentrepriseressourcer, hvor tid købes. | Den rolle, der udføres af underentrepriseressourcerne, bestemmer omkostningerne ved købet. |
| Ønsket start | Angiv den dato, hvor underentrepriseressourcerne skal bruges for at begynde at arbejde. | Dette bruges til at vælge en projektprisliste fra de projektprislister, der er knyttet til underentreprisen. Omkostningerne for rollen på underentrepriselinjen kommer fra den pågældende prisliste. |
| Anmodet afslutning | Angiv den dato, hvor underentreprisens ressourcetildeling slutter. | Den bruges til at vise advarsler, når en projektleder trækker på kapaciteten i forbindelse med ressourcekrav, der opstår efter denne dato. |
| Bestilt antal | Angiv antallet af timer for den rolle, der købes fra leverandøren. | Den bruges til at vise advarsler, når en projektleder overforbruger denne kapacitet for ressourcekrav. |
| Enhedsgruppe | Standardværdien er **Tidsenhedsgruppe**, som ikke kan ændres. | Intet|
| Enhed | Standarden for dette felt er basisenheden for timer fra **Tidsenhedsgruppen**. Du kan ændre denne værdi for at købe en hvilken som helst enhed af **Tidsenhedsgruppen** såsom dag eller uge. | Kombinationen af **Rolle** og **Enhed** bruges som standarden eller beregnes for enhedsprisen for underentrepriselinjen. |
| Enhedspris | Standardenhedsprisen bruger kombinationen af **Rolle** og **Enhed** fra de projektprislister, der er anvendelige for datoen for **Anmodet start** på underentrepriselinjen. | Når den gældende projektprisliste har konfigureret prisen i en anden enhed end enheden på underentrepriselinjen, bruger systemet enhedskonverteringen til at beregne enhedsprisen. |
| Subtotal |    Dette er et skrivebeskyttet felt, der beregnes som Mængde X Enhedspris, hvis der angives både mængde- og enhedsprisværdier. Hvis enten mængde eller enhedspris er tomme, eller de begge er tomme, kan du angive en værdi manuelt i feltet. | Intet|
| Moms |   Angiv omsætningsskattebeløbet. |Intet |
| Samlet beløb | Det samlede beløb på underentrepriselinjen inklusive moms. Denne værdi beregnes som delsum + salgsmoms.|Intet |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
