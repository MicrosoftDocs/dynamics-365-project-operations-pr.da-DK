---
title: Konfigurer satser for omkostninger og salg af katalogprodukter - lille
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere satser for omkostninger og salg for varer i et produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274451"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurer satser for omkostninger og salg af katalogprodukter - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Opsætningen af priser for produktkatalogvarer i Dynamics 365 Project Operations er den samme som i Dynamics 365 Sales.

I Project Operations kan produkter ikke estimeres eller bruges på projekter, så produktkatalogpriser behøver ikke at blive angivet på projektprislister for tilbud og kontrakter.

Brug feltet **Produktpris** i et tilbud, en kontrakt eller på en konto til at konfigurere produktkatalogpriser. Konfigurer ikke produktkatalogpriser på projektprislisterne. Projektprislister er eksklusive for Project Operations. Den applikationsspecifikke forretningslogik kopierer prislisterne fra et tilbud til en kontrakt. Resultatet er en kontraktspecifik projektprisliste. Kopieringshandlingen kan forsinke processen for vundne tilbud, hvis projektets prisliste i tilbuddet bliver for stor. Produktprislisterne kopieres ikke for at oprette brugerdefinerede prislister på kontrakter. Da der ikke er nogen kopiering involveret, påvirkes tilbudsprocessens ydeevne ikke.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]