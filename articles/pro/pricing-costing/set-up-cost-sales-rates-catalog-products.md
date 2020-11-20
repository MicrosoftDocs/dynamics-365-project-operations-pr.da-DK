---
title: Konfigurer satser for omkostninger og salg af katalogprodukter - lille
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere satser for omkostninger og salg for varer i et produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176694"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurer satser for omkostninger og salg af katalogprodukter - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Konfiguration af prisfastsættelse for varer i produktkatalog i Dynamics 365 Project Operations er de samme som i Dynamics 365 Sales.

Da produkter ikke kan estimeres eller bruges på projekter i Project Operations, er det ikke nødvendigt at angive priser for produktkataloget på projektprislister for tilbud og kontrakter.

Produktkatalogpriser bør oprettes i feltet **Produktpris** for et tilbud, en kontrakt eller et firma. Du kan ikke konfigurere priser for produktkataloger i projektprislisterne for disse objekter. Projektprislister er eksklusive for Project Operations. Der er programspecifik forretningslogik, der kopierer prislisterne fra et tilbud til en kontrakt. Resultatet er en kontraktspecifik projektprisliste. Kopieringshandlingen kan forsinke processen for vundne tilbud, hvis projektets prisliste i tilbuddet bliver for stor. Produktprislisterne kopieres ikke for at oprette brugerdefinerede prislister på kontrakter. Dette betyder, at produktprislister ikke påvirker ydeevnen for processen for vundne tilbud.
