---
title: Underentrepriselinjer for produkter
description: I dette emne forklares det, hvordan du registrerer underentrepriselinjer for produkter og bruger de forskellige felter til at registrere produktkøb fra leverandører.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71e4a48c3d29d7ea5b015f6c6797da60001fccff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579066"
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

| Felt | Beskrivelse | Funktionspåvirkning|
| ----- | ----------- | ----------- |
| Navn | Navnet på underentrepriselinjen for at hjælpe med identifikationen. |Dette vises som den første kolonne i alle opslag baseret på underentrepriselinjer.
| Beskrivelse | En kort beskrivelse af de produkter, der købes på underentrepriselinjen. | Intet |
| Linjetype | Dette felts standardværdi er **Mængdebaseret**. |Intet |
| Faktureringsmetode | Dette er en grupperet indstilling, der repræsenterer de to primære kontraktmodeller, som understøttes af Project Operations: **Fast pris** og **Tid og materialer**. | På grundlag af den valgte faktureringsmetode gøres en milepælsbaseret fakturaplan tilgængelig for underentrepriselinjer med faktureringsmetoden Fast pris. |
| Transaktionsklasse |Dette felts standardværdi er **Tid**. Hvis du vil oprette underentrepriselinjer for produktkøb, skal du i feltet **Transaktionsklasse** angive **Materialer**.  | Dette angiver, at underentrepriselinjen bruges til at registrere køb af en kategori af produkter, der skal bruges på projekter. |
| Vælg produkt | Vælg, om det produkt, der købes, skal forblive i produktkataloget, eller om det er et produkt, der skal tilføres. |Intet |
| Produkt | Vælg et aktivt produkt fra kataloget. Dette felt er kun tilgængeligt, når **Vælg produkt** er angivet til **Eksisterende**. |Kombinationen af **Produkt** og **Enhed** bruges som standarden eller beregnes for enhedsprisen for underentrepriselinjen.
| Produkter, der skal rekvireres | Angiv navnet på det produkt, der skal tilføres. Dette felt er kun tilgængeligt, når **Vælg produkt** er angivet til **Tilførelse**.  |Købsprisen angives ikke automatisk for produkter, der skal indkøbes.|
| Anmodet leveringsdato | Angiv den påkrævede leveringsdato for produkterne.| Denne dato bruges også til at vælge en projektprisliste blandt de projektprislister, der er knyttet til underentreprisen. Omkostningerne for produktet på underentrepriselinjen hentes derefter som standard fra den pågældende prisliste. |
| Kontraktbestemt leveringsdato | Angiv den dato, hvor produkterne skal aftales i henhold til det i kontrakten aftalte.  |Intet|
| Bestilt antal | Angiv antallet af det produkt, der købes fra leverandøren.| Dette bruges til at vise advarsler, når en projektleder bruger mere end den angivne mængde.|
| Enhedsgruppe | Denne værdi bruges kun som standard for katalogprodukter. |Når både **Produkt** og **Anmodet leveringsdato** vælges, vælger systemet den gældende prisliste på baggrund af leveringsdatoen. Der forespørges om de relaterede prislisteelementer for det tilsvarende produkt. Enheds- og enhedsgruppeværdierne hentes som standard fra konfigurationen på prislisteelementposten. |
| Enhed | Denne værdi bruges som standard for den enhed, der er konfigureret i prislisteelementposten. Du kan ændre dette til en anden enhed efter behov.| Kombinationen af produkt og enhed bruges til at angive standarden for enhedsprisen på underentrepriselinjen for eksisterende katalogprodukter. |
| Enhedspris | Enhedsprisen angives som standard ved hjælp af en kombination af produkt og enhed fra de prislisteelementer, der er relateret til den projektprisliste, som gælder for den ønskede leveringsdato for underentrepriselinjen.  |Intet |
| Subtotal | Dette skrivebeskyttede felt beregnes som Antal x Enhedspris, hvis der er angivet værdier i begge felter. Hvis enten feltet **Antal** eller feltet **Enhedspris** er tomme, eller de begge er tomme, kan du angive en værdi manuelt.  |Intet |
| Moms | Angiv salgsmomsværdien. |Intet |
| Samlet beløb | I dette beregnede felt vises det samlede beløb for underentrepriselinjen inklusive moms. Værdien i dette felt beregnes som delsum + moms. |Intet |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
