---
title: Underentrepriselinjer for produkter
description: I dette emne forklares det, hvordan du registrerer underentrepriselinjer for produkter og bruger de forskellige felter til at registrere produktkøb fra leverandører.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323679"
---
# <a name="subcontract-lines-for-products"></a>Underentrepriselinjer for produkter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En underentreprise i Dynamics 365 Project Operations kan have en underentrepriselinje for produkter. Disse linjer gør det muligt for en projektleder at købe produkter fra leverandører, som de derefter kan bruge til projektopgaver.

Udfør følgende trin for at oprette en underentrepriselinje for produkter i Project Operations.

1. På navigationssiden skal du vælge **Underentrepriser** og derefter åbne den underentreprise, som du vil arbejde med. 
2. På fanen **Underentrepriselinjer** skal du vælge **+Ny** for at oprette en ny underentrepriselinje.
3. På siden **Hurtig oprettelse** skal du i feltet **Transaktionsklasse** vælge **Materialer** og angive eller vælge de nødvendige feltoplysninger. 
4. Vælg **Gem**.

Følgende tabel indeholder oplysninger om felterne på siden **Underentrepriselinjedetaljer** og siden **Hurtig oprettelse**, da de er relevante for køb af produkter.

| Felt | Beskrivelse |
| ----- | ----------- |
| Navn | Navnet på underentrepriselinjen. |
| Beskrivelse | En kort beskrivelse af de produkter, der købes på underentrepriselinjen. |
| Linjetype | Denne feltværdi hentes som standard fra **Mængdebaseret**. |
| Faktureringsmetode |  Faktureringsmetoden for underentrepriselinjen. En milepælsbaseret fakturaplan er tilgængelig for fastprisfaktureringsmetoder. |
| Transaktionsklasse | Denne feltværdi hentes som standard fra **Tid**. Hvis du vil oprette underentrepriselinjer til køb af produkter, skal du i feltet **Transaktionsklasse** vælge **Materialer**. Dette valg angiver, at underentrepriselinjen bruges til at registrere et produktkøb, der skal bruges på projekter. |
| Vælg produkt | Vælg, om det produkt, der købes, skal forblive i produktkataloget, eller om det er et produkt, der skal tilføres. |
| Produkt | Vælg et aktivt produkt fra kataloget. Dette felt er kun tilgængeligt, når **Vælg produkt** er angivet til **Eksisterende**. |
| Produkter, der skal rekvireres | Angiv navnet på det produkt, der skal tilføres. Dette felt er kun tilgængeligt, når **Vælg produkt** er angivet til **Tilførelse**.  |
| Anmodet leveringsdato | Vælg den krævede leveringsdato for produkterne. Denne dato bruges også til at vælge en projektprisliste blandt de projektprislister, der er knyttet til underentreprisen. Omkostningerne for produktet på underentrepriselinjen hentes derefter som standard fra den pågældende prisliste. |
| Kontraktbestemt leveringsdato | Vælg den dato, hvor produkterne i henhold til kontrakt skal leveres.  |
| Bestilt antal | Angiv antallet af det produkt, der købes fra leverandøren. Hvis en projektleder overtrækker fra dette antal, vises der en advarsel. |
| Enhedsgruppe | Denne værdi bruges kun som standard for katalogprodukter. Når både **Produkt** og **Anmodet leveringsdato** vælges, vælger systemet den gældende prisliste på baggrund af leveringsdatoen. Der forespørges om de relaterede prislisteelementer for det tilsvarende produkt. Enheds- og enhedsgruppeværdierne hentes som standard fra konfigurationen på prislisteelementposten. |
| Enhed | Denne værdi hentes som standard fra enhedskonfigurationen i prislisteelementposten. Du kan ændre dette til en anden enhed efter behov. Kombinationen af produkt og enhed bruges til at angive standarden for enhedsprisen på underentrepriselinjen for eksisterende katalogprodukter. |
| Enhedspris | Enhedsprisen angives som standard ved hjælp af en kombination af produkt og enhed fra de prislisteelementer, der er relateret til den projektprisliste, som gælder for den ønskede leveringsdato for underentrepriselinjen.  |
| Subtotal | Dette skrivebeskyttede felt beregnes som Antal x Enhedspris, hvis der er angivet værdier i begge felter. Hvis enten feltet **Antal** eller feltet **Enhedspris** er tomme, eller de begge er tomme, kan du angive en værdi manuelt.  |
| Moms | Angiv salgsmomsværdien. |
| Samlet beløb | I dette beregnede felt vises det samlede beløb for underentrepriselinjen inklusive moms. Værdien i dette felt beregnes som delsum + moms. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
