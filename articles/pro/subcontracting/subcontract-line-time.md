---
title: Underentrepriselinjer for tid
description: I denne artikel forklares det, hvordan du registrerer underleverandørlinjer for tid og registrerer køb af tid fra leverandører.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522225"
---
# <a name="subcontract-lines-for-time"></a>Underentrepriselinjer for tid

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

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
