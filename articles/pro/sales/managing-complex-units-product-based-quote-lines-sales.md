---
title: Administration af komplekse undermoduler såsom pr. bruger pr. måned i forbindelse med produktbaserede tilbudslinjer
description: Dette emne indeholder oplysninger om, hvordan du administrerer komplekse enheder for projektbaserede tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965756"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="ea1fe-103">Administration af komplekse undermoduler såsom pr. bruger pr. måned i forbindelse med produktbaserede tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="ea1fe-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="ea1fe-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="ea1fe-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea1fe-105">Dynamics 365 Project Operations bruger mængdefaktorer til at understøtte salget af abonnementsbaserede produkter.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="ea1fe-106">I forbindelse med abonnementsbaserede produkter udtrykkes antallet i tilbuds- eller projektkontraktlinjen som antallet af brugermåneder.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="ea1fe-107">Prisen for abonnementsprogrammer gemmes som regel i kataloget som pris pr. bruger pr. måned.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="ea1fe-108">Under salgsprocessen er prisen i tilbudslinjen som regel den pris pr. bruger, pris pr. måned, som blev forhandlet og fratrukket af IT-salgsagenten.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="ea1fe-109">Hver handel har et forskelligt antal brugere og et forskelligt antal abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="ea1fe-110">Det antal, der bruges til at beregne tilbudslinjen, er et produkt af antallet af brugere og antallet af abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="ea1fe-111">For at understøtte denne type salg introduceres konceptet med mængdefaktorer i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="ea1fe-112">Mængdefaktorer er baseret på produktattributterne i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="ea1fe-113">Når du konfigurerer bestemte egenskaber for et produkt, giver Project Operations dig mulighed for at markere et undersæt eller alle egenskaberne som mængdefaktorer.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="ea1fe-114">Project Operations validerer, at kun numeriske egenskaber eller produktegenskaber med numerisk datatype markeres som mængdefaktorer.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="ea1fe-115">Når du tilføjer et produkt med mængdefaktorer til en tilbudslinje, bliver feltet **Antal** skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="ea1fe-116">Når du har angivet værdier for produktegenskaber, der er mængdefaktorer, beregner Project Operations antallet i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="ea1fe-117">Dynamics 365 Sales kan f.eks. have følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="ea1fe-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="ea1fe-118">**Antal brugere**: Antallet af brugere</span><span class="sxs-lookup"><span data-stu-id="ea1fe-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="ea1fe-119">**Antal måneder**: Antallet af abonnementsmåneder</span><span class="sxs-lookup"><span data-stu-id="ea1fe-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="ea1fe-120">**Produkt-SKU**</span><span class="sxs-lookup"><span data-stu-id="ea1fe-120">**Product SKU**</span></span>

<span data-ttu-id="ea1fe-121">Du kan markere egenskaberne **Antal brugere** og **Antal måneder** som mængdefaktorer ved at redigere egenskaberne for produktlinjen.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="ea1fe-122">Hvis du vil oprette mængdefaktorer fra produktegenskaber, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="ea1fe-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="ea1fe-123">I venstre navigationsrude i Project Operations skal du gå til **Salg** > **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="ea1fe-124">Åbn det produkt, som du vil konfigurere mængdefaktorer for.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="ea1fe-125">Kontroller, at produktets egenskaber allerede er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="ea1fe-126">På projektets side med **Projektoplysninger** skal du vælge fanen **Mængdefaktorer**.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="ea1fe-127">I undergitteret skal du vælge **Beregning af + nyt felt**.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="ea1fe-128">Angiv navnet på mængdefaktoren, og vælg den egenskabsværdi, der er knyttet til feltets beregning.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="ea1fe-129">Gem og luk formularen.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-129">Save and close the form.</span></span> <span data-ttu-id="ea1fe-130">Gentag disse trin for alle de egenskaber, der skal bruges til beregning af mængden for den produktbaserede tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="ea1fe-131">Når du opretter en produktbaseret tilbudslinje for et produkt, låses mængden på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="ea1fe-132">Antallet beregnes som et produkt af de egenskabsværdier, du kan angive for den pågældende tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
