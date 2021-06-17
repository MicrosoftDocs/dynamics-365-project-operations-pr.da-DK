---
title: Konfigurer satser for omkostninger og salg af katalogprodukter - lille
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere satser for omkostninger og salg for varer i et produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004309"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurer satser for omkostninger og salg af katalogprodukter - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Opsætningen af priser for produktkatalogvarer i Dynamics 365 Project Operations er den samme som i Dynamics 365 Sales.

I Project Operations kan produkter ikke estimeres eller bruges på projekter, så produktkatalogpriser behøver ikke at blive angivet på projektprislister for tilbud og kontrakter.

Brug feltet **Produktpris** i et tilbud, en kontrakt eller på en konto til at konfigurere produktkatalogpriser. Konfigurer ikke produktkatalogpriser på projektprislisterne. Projektprislister er eksklusive for Project Operations. Den applikationsspecifikke forretningslogik kopierer prislisterne fra et tilbud til en kontrakt. Resultatet er en kontraktspecifik projektprisliste. Kopieringshandlingen kan forsinke processen for vundne tilbud, hvis projektets prisliste i tilbuddet bliver for stor. Produktprislisterne kopieres ikke for at oprette brugerdefinerede prislister på kontrakter. Da der ikke er nogen kopiering involveret, påvirkes tilbudsprocessens ydeevne ikke.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]