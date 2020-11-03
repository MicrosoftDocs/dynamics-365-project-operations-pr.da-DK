---
title: Konfigurer satser for omkostninger og salg for katalogprodukter
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere satser for omkostninger og salg for varer i et produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074239"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Konfigurer satser for omkostninger og salg for katalogprodukter

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Konfiguration af prisfastsættelse for varer i produktkatalog i Dynamics 365 Project Operations er de samme som i Dynamics 365 Sales.

Da produkter ikke kan estimeres eller bruges på projekter i Project Operations, er det ikke nødvendigt at angive priser for produktkataloget på projektprislister for tilbud og kontrakter.

Produktkatalogpriser bør oprettes i feltet **Produktpris** for et tilbud, en kontrakt eller et firma. Du kan ikke konfigurere priser for produktkataloger i projektprislisterne for disse objekter. Projektprislister er eksklusive for Project Operations. Der er programspecifik forretningslogik, der kopierer prislisterne fra et tilbud til en kontrakt. Resultatet er en kontraktspecifik projektprisliste. Kopieringshandlingen kan forsinke processen for vundne tilbud, hvis projektets prisliste i tilbuddet bliver for stor. Produktprislisterne kopieres ikke for at oprette brugerdefinerede prislister på kontrakter. Dette betyder, at produktprislister ikke påvirker ydeevnen for processen for vundne tilbud.
