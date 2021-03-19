---
title: Opret en manuel proformafaktura - lille
description: Dette emne indeholder oplysninger om, hvordan du opretter en manuel proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274181"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Opret en manuel proformafaktura - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I Dynamics 365 Project Operations kan proformafakturaer oprettes manuelt efter behov. Du kan manuelt oprette en proformafaktura på listesiden **Projektkontrakter** eller på siden med oplysninger om **Projektkontrakt**.

##  <a name="project-contracts-list-page"></a>Listeside med projektkontrakt

På listesiden **Projektkontrakter** skal du vælge en eller flere projektkontrakter og oprette fakturaer for alle de valgte poster.

Systemet kontrollerer, hvilke af de valgte projektkontrakter der har et efterslæb med **Klar til at blive faktureret**, som er dateret før dags dato. På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer. Hvis der er flere kunder i en projektkontrakt, kan der oprettes én faktura pr. kunde og flere fakturaer pr. projektkontrakt.

Alle de oprettede projektfakturaer er tilgængelige på siden **Faktura** i sektionen **Fakturering** i området **Salg**.

## <a name="project-contract-details-page"></a>Side med oplysninger om projektkontrakt

Der kan også oprettes en proformafaktura på siden med detaljer for **Projektkontrakt**. Systemet verficerer, at projektkontrakten et efterslæb med **Klar til at blive faktureret**, som er dateret før dags dato. På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer, der er baseret på antallet af kunder på hver kontraktlinje.

Når der er oprettet en enkelt proformafaktura, åbnes siden **Faktura**. Hvis der oprettes flere fakturaer for den pågældende projektkontrakt, åbnes listesiden **Fakturaer** for at vise alle de oprettede fakturaer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]