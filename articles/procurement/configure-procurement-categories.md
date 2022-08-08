---
title: Brug indkøbskategorier sammen med projektkøbsordrer og afventende leverandørfakturaer
description: I denne artikel beskrives det, hvordan du kan konfigurere indkøbskategorier, der kan anvendes sammen med projektkøb og afventende leverandørfakturaer.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028603"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Brug indkøbskategorier sammen med projektkøbsordrer og afventende leverandørfakturaer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Indkøbsmedarbejdere kan oprette og vedligeholde kataloger over varer og tjenesteydelser, der kan bruges i projektindkøbsordrer og afventende leverandørfakturaer. [Indkøbskataloger](/dynamics365/supply-chain/procurement/procurement-catalogs) gør det nemt at kategorisere køb uden at skulle konfigurere og bruge et udgivet produktkatalog. Hver indkøbskategori kan tilknyttes en projektkategori for tids-, udgifts- eller varetransaktioner. Når der er bogført en afventende leverandørfaktura, som anvender en indkøbskategori, opretter systemet faktiske værdier for tid, udgifter eller materialer på projektet, projekttransaktioner og posteringer i delkladder.

## <a name="minimum-version-requirements"></a>Krav til minimumsversion

Følgende versioner kræves for at bruge indkøbskategorier sammen med projektkøbsordrer til Microsoft Dynamics 365 Project Operations ikke-lagerbaserede/ressourcebaserede scenarier:

- Project Operations Dataverse-løsning version 4.41.0.45 eller nyere
- finans og drift-miljø version 10.0.26 eller nyere

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Kør tilknytninger med dobbelt skrivning for kategorisupport

Kontrollér, at tilknytningen for **Integration af objektet for eksport af projektleverandørlinje i Project Operations msdyn\_projectvendorinvoicelines** bruger version 1.0.0.4 eller nyere.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Aktiver funktionsnøglen for indkøbskategorier

Følg disse trin for at aktivere funktionaliteten til brug for indkøbskategorier sammen med projektkøbsordrer.

1. Åbn arbejdsområdet **Funktionsadministration** i Dynamics 365 Finance.
1. I funktionslisten skal du finde funktionen **Brug indkøbskategorier i Project Operations for ressourcebaserede/ikke-lagerbaserede scenarier** og derefter vælge **Aktivér**.

> [!IMPORTANT]
> Du skal som en forudsætning også aktivere funktionen **Aktivér afventende leverandørfakturaer for Project Operations for ressourcebaserede/ikke-lagerbaserede scenarier**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Tilknyt projektkategorier i indkøbskategorihierarkiet

Følg disse trin for at tilknytte projektkategorier til indkøbskategorier i hierarkiet **Indkøbskategori**:

1. Gå til **Indkøb og forsyning \> Indkøbskategorier**.
1. Vælg **Rediger kategorihierarki**.
1. Vælg den ønskede kategorihierarkinode, og knyt derefter på fanen **Tildel projektkategorier** noden sammen med projektkategorien fra kategorien **Tid**, **Udgifter** eller **Vareprojekt** (dvs. kategorien **Standardtid** eller **Standardudgifter**).
1. Vælg **Gem**.
1. Luk siden.

> [!NOTE]
> Det er valgfrit, om du vil knytte en indkøbskategori til en projektkategori. Hvis der ikke er tilknyttet en indkøbskategori, bruger systemet den værdi, der er angivet i feltet **Vare** i afsnittet **Projektkategoristandarder** under fanen **Project Operations på Dynamics 365 Customer Engagement** på siden **Projektstyring og regnskabsparametre**.
