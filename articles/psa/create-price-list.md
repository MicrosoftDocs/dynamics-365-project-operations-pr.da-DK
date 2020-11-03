---
title: Oprette en prisliste
description: Sådan opretter du en prisliste i Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf75286fd1837e27a9b6053ccb21b60771ee197d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074208"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="fe5e2-103">Oprette en prisliste (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fe5e2-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fe5e2-104">Prislister indeholder en skabelon, som dine kontoadministratorer kan bruge til at oprette tilbud og projekter og til at fastsætte omkostningerne i et projekt.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="fe5e2-105">De har en linjevareliste over roller og udgifter, og den pris, der skal opkræves for hver.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="fe5e2-106">Du kan oprette flere prislister, så du kan benytte separate prisstrukturer til forskellige regioner, du sælger dine produkter i, eller til forskellige salgskanaler.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="fe5e2-107">Det er en god ide at oprette mindst én prisliste for hver valuta, du vil fakturere dine kunder i.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="fe5e2-108">Når du vil oprette økonomiske estimater for det arbejde, der skal leveres, skal du sørge for, at hvert projekt har en sikkerhedskopi af omkostnings- og prisliste.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="fe5e2-109">Opret en standard kost- og salgsprisliste, der gælder for alle projekter, der oprettes i din organisation.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="fe5e2-110">Prislister er baseret på roller og udgiftskategorier, så før du opretter en prisliste, skal du allerede have konfigureret rollerne og udgiftskategorier, du vil bruge under oprettelsen af prislisten.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="fe5e2-111">Gå til **Project Service > Prislister**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="fe5e2-112">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="fe5e2-113">I **Kontekst** skal du vælge, om denne prisliste er til **Omkostninger** , **Køb** eller **Salg**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-113">In **Context** , select whether this price list is for **Cost** , **Purchase** , or **Sales**.</span></span>  
  
4.  <span data-ttu-id="fe5e2-114">I **Navn** skal du angive et navn til prislisten.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-114">In **Name** , enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="fe5e2-115">I **Valuta** skal du vælge den valuta, du vil bruge til fakturerings- eller efterkalkulation.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-115">In **Currency** , select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="fe5e2-116">I **Tidsenhed** skal du angive tidsperioden, som prisen gælder for, som dag eller time.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-116">In **Time Unit** , specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="fe5e2-117">Udfyld **Startdato** , **Slutdato** og **Beskrivelse** efter behov.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-117">Fill in the **Start Date** , **End Date** , and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="fe5e2-118">Klik på **Gem** for at oprette posten, så du kan fortsætte med at redigere den.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="fe5e2-119">For at tilføje en rollepris på prislisten skal du klikke på **+** under **Rollepriser**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="fe5e2-120">I ruden **Rollepris** skal du angive oplysninger og derefter klikke på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fe5e2-121">Fortsæt med at tilføje rollepriser efter behov.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="fe5e2-122">Når du er færdig med redigeringen, skal du klikke på knappen **Gem** i nederste højre hjørne af skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="fe5e2-123">For at tilføje en udgiftskategori på prislisten skal du klikke på **+** under **Kategoripriser**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="fe5e2-124">I ruden **Transaktionskategoripris** skal du angive oplysninger og derefter klikke på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fe5e2-125">Fortsæt med at tilføje kategoripriser efter behov.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="fe5e2-126">Når du er færdig med redigeringen, skal du klikke på knappen **Gem** i nederste højre hjørne af skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="fe5e2-127">For at tilføje prislisteelementer på prislisten skal du klikke på **+** under **Prislisteelementer**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="fe5e2-128">I ruden **Prislisteelement** skal du angive oplysninger og derefter klikke på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fe5e2-129">Fortsæt med at tilføje prislisteelementer efter behov.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="fe5e2-130">Når du er færdig med redigeringen, skal du klikke på knappen **Gem** i nederste højre hjørne af skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="fe5e2-131">For at tilføje distriktsrelationer på prislisten skal du klikke på **+** under **Distriktsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="fe5e2-132">I vinduet **Ny forbindelse** skal du angive oplysninger og derefter klikke på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="fe5e2-133">Fortsæt med at tilføje distriktsrelationer efter behov.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="fe5e2-134">Når du er færdig med redigeringen, skal du klikke på knappen **Gem** i nederste højre hjørne af skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="fe5e2-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fe5e2-135">Se også</span><span class="sxs-lookup"><span data-stu-id="fe5e2-135">See Also</span></span>  
 [<span data-ttu-id="fe5e2-136">Konfigurere Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fe5e2-136">Configure Project Service Automation</span></span>](../psa/configure.md)
