---
title: Bestil ikke-lagerbaserede materialer til et projekt ved hjælp af projektindkøbsordrer
description: I denne artikel forklares det, hvordan du kan bestille ikke-lagerførte materialer til et projekt ved hjælp af projektindkøbsordrer.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929805"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Ordreindkøbskategorier eller ikke-lagerbaserede materialer til et projekt ved hjælp af projektindkøbsordrer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Indkøbsafdelingen i organisationen kan bruge [indkøbsordrer](/dynamics365/supply-chain/procurement/purchase-order-overview) til at spore ordrer på varer og tjenester. Indkøbsordrer til indkøbskategorier eller ikke-lagerbaserede materialer kan tilskrives et projekt. Fakturering af disse indkøbsordre bogfører omkostningerne i forhold til projektet.

## <a name="prerequisites"></a>Forudsætninger
Fuldfør følgende trin for at aktivere funktionaliteten for projektindkøbsordrer.

1. Gå til arbejdsområdet **Funktionsstyring** i Dynamics 365 Finance.
2. I funktionslisten skal du søge efter og vælge funktionen **Aktivér projektindkøbsordrer for Project Operations for ressourcebaserede/ikke-lagerbaserede scenarier**.
3. Vælg **Aktivér**.
4. Konfigurer ikke-lagerbaserede materialer og afventende leverandørfakturaer som beskrevet under [Konfigurer ikke-lagerbaserede materialer og afventende leverandørfakturaer](configure-materials-nonstocked.md).
5. Konfigurer indkøbskategorier som beskrevet i [Brug indkøbskategorier sammen med projektkøbsordrer og afventende leverandørfakturaer](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Opret en projektindkøbsordre fra projektindkøbslisten

1. I Finance skal du gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter** og vælge et projekt.
2. I handlingsruden under fanen **Administrer** skal du i gruppen **Ny** vælge **Vareopgave** > **Indkøbsordre**.
3. På siden **Opret indkøbsordre** skal du vælge den leverandør, som du vil placere indkøbsordren ved, og angive andre oplysninger efter behov, og derefter vælge **Ok**.
4. På siden **Indkøbsordre** skal du i gitteret **Indkøbsordrelinjer** vælge **Tilføj linje**.
5. Angiv et varenummer eller en indkøbskategori, antal, enhed, enhedspris og andre oplysninger efter behov.

    > [!NOTE]
    > Kun indkøbskategorier, ikke-lagerbaserede varer og tjenester kan bruges sammen med projektindkøbsordrer. Lagervarer understøttes ikke.

6. Fortsæt med at tilføje varer eller indkøbskategorier efter behov, og bekræft indkøbsordren.

    Kvitteringer for varer og tjenester kan registreres ved at oprette og bogføre en produktkvittering.

    > [!NOTE]
    > Produktkvitteringerne registreres ikke i projektets faktiske værdier i Microsoft Dataverse og påvirker ikke projektets kladdepostering.

    Når en leverandør sender fakturaen for varer og tjenester på indkøbsordren, kan indkøbsafdelingen oprette en faktura for indkøbsordren ved at gå til **Faktura** > **Opret** > **Faktura** i handlingsruden. Du kan finde flere oplysninger om afventende leverandørfakturaer under [Køb ikke-lagerbaserede materialer ved hjælp af en afventende leverandørfaktura](pending-vendor-invoices.md).
