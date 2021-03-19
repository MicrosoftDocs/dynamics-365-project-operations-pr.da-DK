---
title: Opdatere plug-in-attributter, så de indeholder nye prisdimensioner
description: Dette emne indeholder oplysninger om opdatering af plug-in-attributter til prisdimensioner.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281786"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="210b9-103">Opdatere plug-in-attributter, så de indeholder nye prisdimensioner</span><span class="sxs-lookup"><span data-stu-id="210b9-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="210b9-104">Hvis du ikke bruger tilbudsgivningsfunktionen eller kontraktenheden i PSA (Project Service Automation), kan du springe dette emne over.</span><span class="sxs-lookup"><span data-stu-id="210b9-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="210b9-105">Dette emne forudsætter, at du har fuldført procedurerne i emnerne [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities.md), [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](field-references.md) og [Konfigurere brugerdefinerede felter som prisfastsættelsesdimensioner](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="210b9-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="210b9-106">Hvis du ikke har fuldført procedurerne, skal du gå tilbage og fuldføre dem og derefter vende tilbage til dette emne.</span><span class="sxs-lookup"><span data-stu-id="210b9-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="210b9-107">Når der oprettes en tilbudslinjedetalje på siden **Tilbudslinje** for en produkttilbudslinje, opretter systemet to estimatlinjer i baggrunden – en linje for estimatets omkostningsside og én for salgssiden.</span><span class="sxs-lookup"><span data-stu-id="210b9-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="210b9-108">Det samme gælder for projektkontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="210b9-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="210b9-109">Når du foretager en ændring af mængden eller et felt på omkostningssiden, overføres denne ændring til salgssiden.</span><span class="sxs-lookup"><span data-stu-id="210b9-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="210b9-110">Dette er muligt på grund af følgende plug-ins, der skal registreres igen, efter at der er foretaget en ændring i prisdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="210b9-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="210b9-111">PreOperationContractLineDetailUpdate – Opdateringer **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="210b9-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="210b9-112">PreOperationQuoteLineDetailUpdate – Opdateringer **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="210b9-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="210b9-113">I følgende trin forklares, hvordan du kan registrere plug-ins.</span><span class="sxs-lookup"><span data-stu-id="210b9-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="210b9-114">Åbn **PluginRegistrationTool** og opret forbindelse til din online-forekomst.</span><span class="sxs-lookup"><span data-stu-id="210b9-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="210b9-115">Klik på **Søg**, og søg efter den plug-in, der skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="210b9-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Skærmbillede af søgetræet](media/PRT-1.png)

3. <span data-ttu-id="210b9-117">Når plug-in'en er fundet, skal du markere den og derefter klikke på **Vælg i hovedformular**.</span><span class="sxs-lookup"><span data-stu-id="210b9-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="210b9-118">Vælg trinnet for den plug-in, du vil opdatere, højreklik, og vælg derefter **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="210b9-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Skærmbilledet af plug-in'en, der skal opdateres](media/PRT-2.png)
 
5. <span data-ttu-id="210b9-120">I opdateringsvinduet skal du klikke på ellipseknappen (**...**) i filtreringsattributterne.</span><span class="sxs-lookup"><span data-stu-id="210b9-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Skærmbillede af opdatering af oplysningerne om konfiguration af eksisterende trin](media/PRT-3.png)
 
6. <span data-ttu-id="210b9-122">Markér afkrydsningsfelterne for prisattributter.</span><span class="sxs-lookup"><span data-stu-id="210b9-122">Select the pricing attribute check boxes.</span></span>

 ![Skærmbillede, der viser det markerede afkrydsningsfelt for prisattributter](media/PRT-4.png)

7. <span data-ttu-id="210b9-124">Klik på **OK** for at lukke siden, og vælg derefter **Opdater trin**.</span><span class="sxs-lookup"><span data-stu-id="210b9-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Skærmbillede, der viser knappen "Opdater trin"](media/PRT-5.png)
 
8. <span data-ttu-id="210b9-126">Gentag denne proces for den anden plug-in, **PreOperationQuoteLineDetail – Opdatering af msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="210b9-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="210b9-127">Luk Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="210b9-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]