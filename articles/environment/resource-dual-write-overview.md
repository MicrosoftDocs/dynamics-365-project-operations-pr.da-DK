---
title: Integration af dobbeltskrivning i Project Operations
description: Denne artikel indeholder en oversigt over integration med dobbeltskrivning i Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927965"
---
# <a name="project-operations-dual-write-integration-overview"></a>Oversigt over integration af dobbeltskrivning i Project Operations

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Project Operations bruger [funktioner til dobbelt skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) til at synkronisere data på tværs af Microsoft Dataverse og Dynamics 365 Finance.

I følgende illustration vises, hvordan data synkroniseres som en del af denne integration mellem Dataverse og Finance.

![Oversigt over dataflow i Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations på Dataverse indeholder en moderne brugergrænseflade (UI) og nem udvidelse uden kode/med lav kode ved hjælp af Power Platform-funktioner. Projektledere, Resource Manager, medlemmer af projektteam og andre front office-personer udfører deres aktiviteter i Project Operations på Dataverse.

Project Operations i Finance understøtter projektregnskaber og indtægtsføring. Project Operations-plugins til den økonomiske ramme i Finance til momsberegning, valutakurser, rapportering om økonomiske dimensioner og meget mere. Projektrevisorens erfaringer findes primært i Finance.

Integration af Project Operations består af følgende komponentintegration:


- [Opsætning af Project Operations og konfiguration af dataintegration](resource-dual-write-setup-integration.md) 
- [Projektestimater og faktiske tal](resource-dual-write-estimates-actuals.md)
- [Projektfakturaer](resource-dual-write-project-invoice.md)
- [Udgiftsstyring](resource-dual-write-expense.md)
- [Leverandørfaktura](resource-dual-write-vendor-invoice.md)
