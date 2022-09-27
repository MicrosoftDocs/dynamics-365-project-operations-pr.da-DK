---
title: Underentrepriselinjer for udgiftskategorier
description: I denne artikel forklares det, hvordan du registrerer underleverandørlinjer for udgifter og bruger felterne til at registrere køb af tid fra leverandører.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ba1241ce40b7c5b488e278e8f1b8e9f352f45dc8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522600"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Underentrepriselinjer for udgiftskategorier

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

En underentreprise i Dynamics 365 Project Operations kan have en linje for udgiftskategorier. Underentrepriselinjer for udgiftskategorier giver projektlederen mulighed for at købe kategorier af tjenester eller produkter fra leverandører, som de kan opkræve på et projekt.

For at oprette en underentrepriselinje for udgiftskategorier i Project Operations skal du fuldføre følgende trin.

1. I navigationsruden skal du vælge **Underentrepriser** og åbne den underentreprise, som du vil arbejde med.
2. På fanen **Underentrepriselinjer** skal du vælge **Ny** for at oprette en ny linje.
3. På siden **Hurtig oprettelse** skal du i feltet **Transaktionsklasse** vælge **Udgifter** og angive eller vælge eventuelle andre krævede feltoplysninger.

Følgende tabel indeholder oplysninger om felterne på detaljesiden **Underentrepriselinje** og siden **Hurtig oprettelse**.

| **Felt** | **Beskrivelse** | **Funktionspåvirkning** |
| --- | --- | --- |
| Navn | Navnet på underentrepriselinjen for at hjælpe med identifikationen. | Dette vises som den første kolonne i alle opslag baseret på underentrepriselinjer. |
| Beskrivelse | En kort beskrivelse af de udgiftskategorier, der købes på underentrepriselinjen. | Intet |
|Linjetype | Dette felt har en standardværdi, der er **Mængdebaseret**. |Intet |
| Faktureringsmetode | Dette er en grupperet indstilling, der repræsenterer de to primære kontraktmodeller, som understøttes af Project Operations: **Fast pris** og **Tid og materialer**. | En milepælsbaseret fakturaplan gøres tilgængelig for underentrepriselinjer, hvis faktureringsmetoden Fast pris vælges. |
| Transaktionsklasse | Dette felts standardværdi er **Tid**. Hvis du vil oprette underentrepriselinjer for produktkøb, skal du i feltet **Transaktionsklasse** angive **Udgifter**.  | Dette angiver, at underentrepriselinjen bruges til at registrere køb af en kategori af udgifter, der skal bruges på projekter. |
| Transaktionskategori | Viser en liste over aktive transaktionskategorier i systemet. |Intet |
| Ønsket start | Angiv den dato, hvor kategorierne for køb skal være tilgængelige fra leverandøren. | Anmodet start bruges til at vælge en projektprisliste fra de projektprislister, der er knyttet til underentreprisen. Omkostningerne for kategorien på underentrepriselinjen kommer fra den pågældende prisliste. |
| Anmodet afslutning | Angiv den dato, hvor kategorierne for køb ikke længere er nødvendige. | Den bruges til at vise advarsler, når en projektleder knytter denne underentrepriselinje til bestemte udgiftsestimater for projektet, der skal bruges efter denne dato. |
| Bestilt antal | Mængden i kategorien, der købes fra leverandøren. | Dette bruges til at vise advarsler, når en projektleder bruger mere end den angivne mængde.|
| Enhedsgruppe | Standardværdien er baseret på den standardenhedsgruppe, der er konfigureret for den valgte kategori. |Intet |
| Enhed | Standarden er baseret på den standardenhed, der er konfigureret for den valgte kategori.  | Kombinationen af **Kategori** og **Enhed** bruges som standarden eller beregnes for enhedsprisen for underentrepriselinjen.  |
| Enhedspris | I standardværdien bruges kombinationen af **Kategori** og **Enhed** fra de kategoripriser, der er relateret til projektprislisten, som gælder for den anmodede start af underentrepriselinjen. |Intet |
| Subtotal | Dette er et skrivebeskyttet felt, der beregnes som Mængde X Enhedspris, hvis der angives både mængde- og enhedsprisværdier. Hvis et eller begge felter er tomme, kan du angive en værdi i dette felt. |Intet |
| Moms | Angiv omsætningsskattebeløbet. |Intet |
| Samlet beløb | Det samlede beløb på underentrepriselinjen inklusive moms. Denne værdi beregnes som delsum + salgsmoms. |Intet |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
