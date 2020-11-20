---
title: Opret en manuel proformafaktura - lille
description: Dette emne indeholder oplysninger om, hvordan du opretter en manuel proformafaktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176379"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Opret en manuel proformafaktura - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I Dynamics 365 Project Operations kan du oprette proformafakturaer manuelt efter behov. Du kan manuelt oprette en proformafaktura på listesiden **Projektkontrakter** eller på siden med oplysninger om **Projektkontrakt**.

##  <a name="project-contracts-list-page"></a>Listeside med projektkontrakt

På listesiden **Projektkontrakter** skal du vælge en eller flere projektkontrakter og oprette fakturaer for alle de valgte poster.

Systemet kontrollerer, hvilke af de valgte projektkontrakter der har et efterslæb med **Klar til at blive faktureret**, som er dateret før dags dato. På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer. Hvis der er flere kunder i en projektkontrakt, kan der oprettes én faktura pr. kunde og flere fakturaer pr. projektkontrakt.

Alle de oprettede projektfakturaer er tilgængelige på siden **Faktura** i sektionen **Fakturering** i området **Salg**.

## <a name="project-contract-details-page"></a>Side med oplysninger om projektkontrakt

Du kan også oprette en proformafaktura på siden med oplysninger om **Projektkontrakt**, hvilket opretter fakturaen for den pågældende projektkontrakt. Systemet kontrollerer, om den valgte projektkontrakt har et efterslæb med **Klar til at blive faktureret**, som er dateret før dags dato. På grundlag af disse kontrakter opretter systemet kladdeproformafakturaer, der er baseret på antallet af kunder på hver kontraktlinje.

Når der er oprettet en enkelt proformafaktura, åbnes siden **Faktura**. Hvis der er oprettet flere fakturaer for den pågældende projektkontrakt, åbnes listesiden **Fakturaer**, hvor du kan se alle de oprettede fakturaer.
