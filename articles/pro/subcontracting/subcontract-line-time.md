---
title: Underentrepriselinjer for tid
description: I dette emne forklares det, hvordan du registrerer underentrepriselinjer for tid og registrerer køb af tid fra leverandører.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323859"
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

| **Felt** | **Beskrivelse** |
| --- | --- |
| Navn | Navnet på underentrepriselinjen. |
| Beskrivelse | En kort beskrivelse af de tjenester, der købes på underentrepriselinjen. | 
| Linjetype | Dette felt er en standardværdi.  |
| Faktureringsmetode | Vælg faktureringsmetoden. Afhængigt af faktureringsmetoden for den refererede underentrepriselinje stilles en milepælsbaseret fakturaplan til rådighed for fastprisfaktureringsmetoden. |
| Transaktionsklasse | Dette felt er en standardværdi, der angiver, om underentrepriselinjen bruges til at registrere et køb af tid fra underleverandør. |
| Rolle | Rollen for de underleverandørressourcer, hvis tid købes. Den rolle, der er tildelt til underentrepriseressourcerne, bestemmer omkostningerne ved købet. |
| Ønsket start | Den dato, hvor underentrepriseressourcerne skal bruges til at begynde at arbejde. Den anmodede start bruges også til at vælge en projektprisliste blandt de projektprislister, der er knyttet til underentreprisen. Omkostningerne for rollen på underentrepriselinjen hentes derefter som standard fra den pågældende prisliste. |
| Anmodet afslutning | Den dato, hvor tildeling af underentrepriseressourcerne slutter. Denne dato bruges til at vise advarsler, når en projektleder trækker på denne kapacitet til ressourcekrav, der opstår efter denne dato. |
| Bestilt antal | Antallet af rolletimer, der købes fra leverandøren. Denne værdi bruges til at vise advarsler, når en projektleder overtrækker fra denne kapacitet til ressourcekrav. |
| Enhedsgruppe | Denne feltværdi bruges som standard for tidsenhedsgruppen og kan ikke ændres.  |
| Enhed | Dette felt bruges som standard til basisenheden for timer fra tidsenhedsgruppen. Du kan ændre denne værdi for at købe en hvilken som helst enhed af tidsenhedsgruppen såsom dag eller uge. Kombinationen af rolle og kategori bruges til at beregne enhedsprisen for underentrepriselinjen. |
| Enhedspris | Enhedsprisen angives som standard på baggrund af en kombination af rolle og enhed fra den projektprisliste, som gælder for den ønskede startdato for underentrepriselinjen. Når den gældende projektprisliste har konfigureret prisen i en anden enhed end enheden på underentrepriselinjen, bruger systemet enhedskonverteringen til at beregne enhedsprisen. |
| Subtotal | Dette er et skrivebeskyttet felt, som beregnes automatisk som **Mængde x enhedsprisen**, hvis der angives både mængde- og enhedsprisværdier. Hvis enten mængde eller enhedspris er tomme, eller de begge er tomme, kan du angive en værdi manuelt i feltet. |
| Moms |  Angiv omsætningsskattebeløbet. |
| Samlet beløb | Det samlede beløb på underentrepriselinjen, når moms er indregnet. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
