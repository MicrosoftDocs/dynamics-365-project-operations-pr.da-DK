---
title: Konfigurer satser for omkostninger og salg af katalogprodukter - lille
description: Denne artikel indeholder oplysninger om, hvordan du konfigurerer omkostnings- og salgspriser for varer i et produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917385"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurer satser for omkostninger og salg af katalogprodukter - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Opsætningen af priser for produktkatalogvarer i Dynamics 365 Project Operations er den samme som i Dynamics 365 Sales.

I Project Operations kan produkter ikke estimeres eller bruges på projekter, så produktkatalogpriser behøver ikke at blive angivet på projektprislister for tilbud og kontrakter.

Brug feltet **Produktpris** i et tilbud, en kontrakt eller på en konto til at konfigurere produktkatalogpriser. Konfigurer ikke produktkatalogpriser på projektprislisterne. Projektprislister er eksklusive for Project Operations. Den applikationsspecifikke forretningslogik kopierer prislisterne fra et tilbud til en kontrakt. Resultatet er en kontraktspecifik projektprisliste. Kopieringshandlingen kan forsinke processen for vundne tilbud, hvis projektets prisliste i tilbuddet bliver for stor. Produktprislisterne kopieres ikke for at oprette brugerdefinerede prislister på kontrakter. Da der ikke er nogen kopiering involveret, påvirkes tilbudsprocessens ydeevne ikke.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]