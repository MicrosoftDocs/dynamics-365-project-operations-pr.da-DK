---
title: Underentrepriselinjer for udgiftskategorier
description: I dette emne forklares det, hvordan du registrerer underentrepriselinjer for udgifter og bruger felterne til at registrere køb af tid fra leverandører.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323814"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Underentrepriselinjer for udgiftskategorier

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En underentreprise i Dynamics 365 Project Operations kan have en linje for udgiftskategorier. Underentrepriselinjer for udgiftskategorier giver projektlederen mulighed for at købe kategorier af tjenester eller produkter fra leverandører, som de kan opkræve på et projekt.

For at oprette en underentrepriselinje for udgiftskategorier i Project Operations skal du fuldføre følgende trin.

1. I navigationsruden skal du vælge **Underentrepriser** og åbne den underentreprise, som du vil arbejde med.
2. På fanen **Underentrepriselinjer** skal du vælge **Ny** for at oprette en ny linje.
3. På siden **Hurtig oprettelse** skal du i feltet **Transaktionsklasse** vælge **Udgifter** og angive eller vælge eventuelle andre krævede feltoplysninger.

Følgende tabel indeholder oplysninger om felterne på detaljesiden **Underentrepriselinje** og siden **Hurtig oprettelse**.

| **Felt** |  **Beskrivelse** |
| ----------| ---------------- |
| Navn | Navnet på underentrepriselinjen. |
| Beskrivelse | En kort beskrivelse af de tjeneste- og produktkategorier, der købes på baggrund af underentrepriselinjen. |
| Linjetype | Dette felts standardværdi er **Mængdebaseret**.  |
| Faktureringsmetode | Faktureringsmetoden for underentrepriselinjen. Afhængigt af faktureringsmetoden for linjen er en milepælsbaseret fakturaplan tilgængelig for fastprisfaktureringsmetoden.  |
| Transaktionsklasse | Dette felts standardværdi er **Tid**. Hvis du vil oprette underentrepriselinjer for produktkøb, skal du i feltet **Transaktionsklasse** angive **Udgifter**. Denne feltværdi angiver, at underentrepriselinjen bruges til at registrere et køb i en produkt- eller tjenestekategori, der skal bruges på projekter. |
| Transaktionskategori | Vælg transaktionskategorien. |
| Ønsket start | Den dato, hvor købskategorierne skal være tilgængelige fra leverandøren. Den anmodede start bruges også til at vælge en projektprisliste blandt de projektprislister, der er knyttet til underentreprisen. Omkostningerne for kategorien på underentrepriselinjen hentes som standard fra den pågældende prisliste. |
| Anmodet afslutning | Den dato, hvor købskategorierne ikke længere er nødvendige. Denne dato kalder en advarsel, når en projektleder knytter denne underentrepriselinje til bestemte udgiftsestimater for de projekter, der er dateret efter denne dato. |
| Bestilt antal | Mængden af den kategori, der købes fra leverandøren. Når en projektleder overtrækker fra det indkøbte antal, vises der en advarsel.  |
| Enhedsgruppe | Denne feltværdi er standardværdier, der er baseret på den standardenhedsgruppe, som er konfigureret for den valgte kategori. |
| Enhed | Denne feltværdi er standardværdier, der er baseret på den standardenhed, som er konfigureret for den valgte kategori. Kombinationen af kategori og enhed bruges til at angive standarden for enhedsprisen på underentrepriselinjen. |
| Enhedspris | Feltværdien for enhedsprisen angives som standard ved at kombinere kategorien og enheden fra de kategoripriser, der er relateret til den projektprisliste, som gælder for den ønskede startdato for underentrepriselinjen.  |
| Subtotal | Dette skrivebeskyttede felt beregnes automatisk som enhedsprisen for antallet, hvis der angives både mængde- og enhedsprisværdier. Hvis enten det ene eller begge felter er tomme, kan du angive en værdi manuelt i dette felt.  |
| Moms | Angiv omsætningsskattebeløbet.  |
| Samlet beløb | Det samlede beløb på underentrepriselinjen inklusive moms. Denne værdi beregnes som delsum + salgsmoms.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
