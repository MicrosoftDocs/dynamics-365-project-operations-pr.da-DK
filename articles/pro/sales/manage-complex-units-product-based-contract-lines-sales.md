---
title: Administrer komplekse undermoduler til produktbaserede kontraktlinjer - lille
description: Dette emne indeholder oplysninger om support af salget af abonnementsbaserede produkter.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177369"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="df0cc-103">Administrer komplekse undermoduler til produktbaserede kontraktlinjer - lille</span><span class="sxs-lookup"><span data-stu-id="df0cc-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="df0cc-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="df0cc-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="df0cc-105">Dynamics 365 Project Operations bruger mængdefaktorer til at understøtte salget af abonnementsbaserede produkter.</span><span class="sxs-lookup"><span data-stu-id="df0cc-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="df0cc-106">I forbindelse med abonnementsbaserede produkter udtrykkes antallet i kontrakten eller projektkontraktlinjen som antallet af brugermåneder.</span><span class="sxs-lookup"><span data-stu-id="df0cc-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="df0cc-107">Prisen for abonnementsprogrammer gemmes i kataloget som pris pr. bruger pr. måned.</span><span class="sxs-lookup"><span data-stu-id="df0cc-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="df0cc-108">Under salgsprocessen er prisen i kontraktlinjen som regel den pris pr. bruger, pris pr. måned, som blev forhandlet og fratrukket af salgsagenten.</span><span class="sxs-lookup"><span data-stu-id="df0cc-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="df0cc-109">Hver handel har et forskelligt antal brugere og et forskelligt antal abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="df0cc-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="df0cc-110">Det antal, der bruges til at beregne beløbet i kontraktlinjen, er et produkt af antallet af brugere og antallet af abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="df0cc-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="df0cc-111">For at understøtte denne type salg understøtter Project Operations konceptet *mængdefaktorer*.</span><span class="sxs-lookup"><span data-stu-id="df0cc-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="df0cc-112">Mængdefaktorer er baseret på produktattributter.</span><span class="sxs-lookup"><span data-stu-id="df0cc-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="df0cc-113">Når du konfigurerer bestemte egenskaber for et produkt, kan du markere et undersæt af disse egenskaber eller alle egenskaberne som mængdefaktorer.</span><span class="sxs-lookup"><span data-stu-id="df0cc-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="df0cc-114">Project Operations validerer, at kun numeriske egenskaber eller produktegenskaber med numerisk datatype markeres som mængdefaktorer.</span><span class="sxs-lookup"><span data-stu-id="df0cc-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="df0cc-115">Når der tilføjes et produkt med konfigurerede mængdefaktorer til en kontraktlinje, bliver feltet **Antal** skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="df0cc-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="df0cc-116">Når du har angivet værdier for produktegenskaber, der er mængdefaktorer, beregner Project Operations antallet i kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="df0cc-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="df0cc-117">Dynamics 365 Sales kan f.eks. have følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="df0cc-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="df0cc-118">**Antal brugere**: Antallet af brugere.</span><span class="sxs-lookup"><span data-stu-id="df0cc-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="df0cc-119">**Antal måneder**: Antallet af abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="df0cc-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="df0cc-120">**Produktvarenummer**: Produktets lagerbeholdningsenhed (varenummer).</span><span class="sxs-lookup"><span data-stu-id="df0cc-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="df0cc-121">Egenskaberne **Antal brugere** og **Antal måneder** kan mærkes som mængdefaktorer ved at redigere egenskaberne for produktlinjen.</span><span class="sxs-lookup"><span data-stu-id="df0cc-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="df0cc-122">Hvis du vil oprette mængdefaktorer fra produktegenskaber, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="df0cc-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="df0cc-123">I **Project Operations** skal du vælge **Salgsprodukter**.</span><span class="sxs-lookup"><span data-stu-id="df0cc-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="df0cc-124">Åbn det produkt, som du vil konfigurere mængdefaktorer for.</span><span class="sxs-lookup"><span data-stu-id="df0cc-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="df0cc-125">Kontroller, at produktet har egenskaber, der allerede er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="df0cc-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="df0cc-126">På siden **Projektoplysninger** skal du vælge fanen **Mængdefaktorer**.</span><span class="sxs-lookup"><span data-stu-id="df0cc-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="df0cc-127">I undergitteret skal du vælge **Beregning af + nyt felt**.</span><span class="sxs-lookup"><span data-stu-id="df0cc-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="df0cc-128">Angiv navnet på **Mængdefaktoren**, og vælg den egenskabsværdi, der er knyttet til feltets beregning.</span><span class="sxs-lookup"><span data-stu-id="df0cc-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="df0cc-129">Gem og luk formularen.</span><span class="sxs-lookup"><span data-stu-id="df0cc-129">Save and close the form.</span></span>
7. <span data-ttu-id="df0cc-130">Gentag trin 2-6 for alle de egenskaber, der tilsammen udgør antallet i den produktbaserede kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="df0cc-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="df0cc-131">Hvis mængdefaktorer er konfigureret, og brugeren opretter en kontraktlinje for dette produkt, låses antallet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="df0cc-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="df0cc-132">Antallet beregnes derefter som et produkt af egenskabsværdierne for den pågældende kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="df0cc-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
