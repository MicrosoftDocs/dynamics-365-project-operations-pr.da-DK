---
title: Opdatering af plug-in-attributter med nye prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om, hvordan du opdaterer plug-in-attributter til prisfastsættelsesdimensioner.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643211"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="4a83a-103">Opdater plug-in-attributter med nye prisfastsættelsesdimensioner</span><span class="sxs-lookup"><span data-stu-id="4a83a-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="4a83a-104">Dette emne indeholder oplysninger om, hvordan du opdaterer plug-in-attributter til prisfastsættelsesdimensioner.</span><span class="sxs-lookup"><span data-stu-id="4a83a-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="4a83a-105">Dette emne kan kun anvendes på tilbuds- og kontraktfunktionerne i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4a83a-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4a83a-106">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="4a83a-106">Prerequisites</span></span>
<span data-ttu-id="4a83a-107">Før du fuldfører trinnene i dette emne, skal du have fuldført procedurerne under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="4a83a-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="4a83a-108">Opret brugerdefinerede felter og objekter</span><span class="sxs-lookup"><span data-stu-id="4a83a-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="4a83a-109">Tilføj brugerdefinerede felter til prisopsætning og transaktionsobjekter</span><span class="sxs-lookup"><span data-stu-id="4a83a-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="4a83a-110">[Konfigurer brugerdefinerede felter som prisfastsættelsesdimensioner](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="4a83a-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="4a83a-111">Hvis du ikke har fuldført procedurerne, skal du fuldføre dem og derefter vende tilbage til dette emne.</span><span class="sxs-lookup"><span data-stu-id="4a83a-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="4a83a-112">Registrer en plug-in</span><span class="sxs-lookup"><span data-stu-id="4a83a-112">Register a plug-in</span></span>
<span data-ttu-id="4a83a-113">Når der oprettes en tilbudslinjedetalje på siden **Tilbudslinje** for en linje i en projekttilbud, oprettes der to estimatlinjer i systemet.</span><span class="sxs-lookup"><span data-stu-id="4a83a-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="4a83a-114">En linje til omkostningssiden af estimatet, og en anden linje til salgssiden.</span><span class="sxs-lookup"><span data-stu-id="4a83a-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="4a83a-115">Det samme gælder for projektkontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="4a83a-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="4a83a-116">Når du foretager en ændring af mængden eller et felt på omkostningssiden, foretages denne ændring også på salgssiden.</span><span class="sxs-lookup"><span data-stu-id="4a83a-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="4a83a-117">Dette er muligt, fordi plug-ins til forudhandling i objekterne tilbudslinjedetalje og kontraktlinedetalje knytter bestemte attributter på omkostningssiden til salgssiden i transaktionen.</span><span class="sxs-lookup"><span data-stu-id="4a83a-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="4a83a-118">Hvis du har brug for at foretage ændringer i prisfastsættelsesdimensionsværdierne på salgssiden, som også skal udføres på omkostningssiden, skal følgende plug-ins registreres igen, når du har foretaget ændringer af en prisfastsættelsesdimension.</span><span class="sxs-lookup"><span data-stu-id="4a83a-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="4a83a-119">Disse plug-ins bruges til at opdatere og registrere data igen:</span><span class="sxs-lookup"><span data-stu-id="4a83a-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="4a83a-120">PreOperationContractLineDetailUpdate - **Opdater msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="4a83a-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="4a83a-121">PreOperationQuoteLineDetailUpdate - **Opdaterer msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="4a83a-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="4a83a-122">Udfør følgende trin for at opdatere og registrere plug-ins igen.</span><span class="sxs-lookup"><span data-stu-id="4a83a-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="4a83a-123">Åbn **PluginRegistrationTool**, og opret forbindelse til Project Operations Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4a83a-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="4a83a-124">Vælg **Søg**, og skriv de første bogstaver i det plug-in, der skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="4a83a-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="4a83a-125">Når plug-in'en er fundet, skal du markere den og derefter vælge **Vælg i hovedformular**.</span><span class="sxs-lookup"><span data-stu-id="4a83a-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="4a83a-126">Vælg trinnet **Opdater msdyn_orderlinetransaction**, højreklik på det, og vælg derefter **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="4a83a-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="4a83a-127">På dialogsiden **Opdater** skal du klikke på ellipseknappen (**...**) i filtreringsattributterne.</span><span class="sxs-lookup"><span data-stu-id="4a83a-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="4a83a-128">Vinduet med filtreringsattributter åbnes, og der vises en liste over alle attributter i objekt- og prisfastsættelsesdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="4a83a-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="4a83a-129">Markér afkrydsningsfelterne ud for prisfastsættelsesdimensionsattributterne.</span><span class="sxs-lookup"><span data-stu-id="4a83a-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="4a83a-130">Vælg **OK** for at lukke siden, og vælg derefter **Opdater trin**.</span><span class="sxs-lookup"><span data-stu-id="4a83a-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="4a83a-131">Gentag trin 2-7 for den anden plug-in **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="4a83a-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="4a83a-132">For denne plug-in skal du opdatere trinnet **Opdatering af msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="4a83a-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="4a83a-133">Luk **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="4a83a-133">Close **PluginRegistrationTool**.</span></span>
