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
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="581ff-103">Konfigurer satser for omkostninger og salg af katalogprodukter - lille</span><span class="sxs-lookup"><span data-stu-id="581ff-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="581ff-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="581ff-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="581ff-105">Konfiguration af prisfastsættelse for varer i produktkatalog i Dynamics 365 Project Operations er de samme som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="581ff-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="581ff-106">Da produkter ikke kan estimeres eller bruges på projekter i Project Operations, er det ikke nødvendigt at angive priser for produktkataloget på projektprislister for tilbud og kontrakter.</span><span class="sxs-lookup"><span data-stu-id="581ff-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="581ff-107">Produktkatalogpriser bør oprettes i feltet **Produktpris** for et tilbud, en kontrakt eller et firma.</span><span class="sxs-lookup"><span data-stu-id="581ff-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="581ff-108">Du kan ikke konfigurere priser for produktkataloger i projektprislisterne for disse objekter.</span><span class="sxs-lookup"><span data-stu-id="581ff-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="581ff-109">Projektprislister er eksklusive for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="581ff-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="581ff-110">Der er programspecifik forretningslogik, der kopierer prislisterne fra et tilbud til en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="581ff-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="581ff-111">Resultatet er en kontraktspecifik projektprisliste.</span><span class="sxs-lookup"><span data-stu-id="581ff-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="581ff-112">Kopieringshandlingen kan forsinke processen for vundne tilbud, hvis projektets prisliste i tilbuddet bliver for stor.</span><span class="sxs-lookup"><span data-stu-id="581ff-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="581ff-113">Produktprislisterne kopieres ikke for at oprette brugerdefinerede prislister på kontrakter.</span><span class="sxs-lookup"><span data-stu-id="581ff-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="581ff-114">Dette betyder, at produktprislister ikke påvirker ydeevnen for processen for vundne tilbud.</span><span class="sxs-lookup"><span data-stu-id="581ff-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
