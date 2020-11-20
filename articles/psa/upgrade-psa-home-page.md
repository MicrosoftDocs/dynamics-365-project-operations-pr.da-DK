---
title: Startside for opgradering
description: Dette emne viser, hvor du kan finde vigtige oplysninger om de nye og ændrede funktioner i Dynamics 365 Project Service Automation og processen for opgradering til den nyeste version.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
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
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121751"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="3373d-103">Startside for opgradering</span><span class="sxs-lookup"><span data-stu-id="3373d-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="3373d-104">Opgradere fra PSA version 2.x eller 1.x til version 3.x</span><span class="sxs-lookup"><span data-stu-id="3373d-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="3373d-105">Nye forekomster</span><span class="sxs-lookup"><span data-stu-id="3373d-105">New instances</span></span>

<span data-ttu-id="3373d-106">Fra og med 17. maj 2019 installeres version 3.x som standard, når Project Service Automation er valgt under klargøring af en ny forekomst.</span><span class="sxs-lookup"><span data-stu-id="3373d-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="3373d-107">Eksisterende forekomster</span><span class="sxs-lookup"><span data-stu-id="3373d-107">Existing instances</span></span>

<span data-ttu-id="3373d-108">Tidligere skulle kunder, der havde en forekomst af PSA version 2.x, og som havde behov for at opgradere til version 3.x, som er den UCI-baserede (Unified Client Interface) version af PSA, kontakte Microsoft Support for at få oplysninger om deres forekomster, så supportafdelingen kunne aktivere forekomsten i forbindelse med opgraderingen til version 3.x.</span><span class="sxs-lookup"><span data-stu-id="3373d-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="3373d-109">Fra og med 1. marts 2020, kan de kunder, som har en forekomst af PSA version 2.x, og som skal opgradere til version 3.x, opgradere deres forekomster direkte fra admin-portalen, uden at skulle kontakte Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="3373d-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="3373d-110">PSA-version 3.x indeholder betydelige ændringer.</span><span class="sxs-lookup"><span data-stu-id="3373d-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="3373d-111">Den er baseret på Unified Interface-rammen med det formål at give en bedre brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="3373d-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="3373d-112">Den nydesignede app har en ensartet, effektiv brugergrænseflade (UI) med dynamisk design og optimal visning på en hvilken som helst skærmstørrelse eller enhed.</span><span class="sxs-lookup"><span data-stu-id="3373d-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="3373d-113">Der er sket andre ændringer i hele programmet.</span><span class="sxs-lookup"><span data-stu-id="3373d-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="3373d-114">Nogle af de områder, der er blevet ændret, omfatter prisfastsættelse, reservation og tildeling af ressourcer, tid, udgifter og godkendelser.</span><span class="sxs-lookup"><span data-stu-id="3373d-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="3373d-115">Det anbefales, at du udfører følgende opgaver, før du påbegynder opgraderingsprocessen:</span><span class="sxs-lookup"><span data-stu-id="3373d-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="3373d-116">Kontrollér, om både Dynamics 365 Field Service og Project Service Automation er installeret på den identificerede forekomst.</span><span class="sxs-lookup"><span data-stu-id="3373d-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="3373d-117">Hvis begge løsninger er installeret, bør du planlægge at opgradere dem begge, før du genoptager den almindelige brug af forekomsten.</span><span class="sxs-lookup"><span data-stu-id="3373d-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="3373d-118">Gennemse følgende emner grundigt.</span><span class="sxs-lookup"><span data-stu-id="3373d-118">Carefully review the following topics.</span></span> <span data-ttu-id="3373d-119">Kendskab til og forståelse af forskellene mellem versionerne kan hjælpe dig med opgraderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="3373d-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="3373d-120">Disse emner indeholder oplysninger om de største ændringer i PSA samt overvejelser og anbefalinger i forbindelse med planlægning af opgraderingen til version 3.x.</span><span class="sxs-lookup"><span data-stu-id="3373d-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="3373d-121">Nyheder eller ændringer i Project Service Automation version 3</span><span class="sxs-lookup"><span data-stu-id="3373d-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="3373d-122">Overvejelser i forbindelse med opgradering – Project Service Automation version 2.x eller 1.x til version 3</span><span class="sxs-lookup"><span data-stu-id="3373d-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="3373d-123">Opgrader sandkasseforekomsten for at evaluere ændringerne i implementeringen, før du opgraderer din produktionsforekomst.</span><span class="sxs-lookup"><span data-stu-id="3373d-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="3373d-124">Når du har gennemgået de emner, der er nævnt tidligere, og du er klar til at opgradere til PSA version 3.x eller den UCI-baserede version, skal du indsende en forespørgsel til Microsoft Support for at gøre opgraderingen tilgængelig fra Administration.</span><span class="sxs-lookup"><span data-stu-id="3373d-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="3373d-125">Angiv oplysningerne om din forekomst i din anmodning.</span><span class="sxs-lookup"><span data-stu-id="3373d-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="3373d-126">Ældre versioner af PSA (PSA version 2.x) i en nyoprettet forekomst</span><span class="sxs-lookup"><span data-stu-id="3373d-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="3373d-127">Fra og med 17. maj 2019 har alle nye forekomster også UCI som standardklient.</span><span class="sxs-lookup"><span data-stu-id="3373d-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="3373d-128">For at kunne tilpasse sig denne ændring vil PSA version 3.x og Field Service version 8.x blive leveret som standard, da disse versioner er udviklet til at fungere sammen med UCI-klienten.</span><span class="sxs-lookup"><span data-stu-id="3373d-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="3373d-129">Fra og med 1. marts 2020 kan kunder med Dynamics PSA ikke længere oprette et nyt miljø med ældre versioner af PSA, såsom PSA version 2.x eller ældre.</span><span class="sxs-lookup"><span data-stu-id="3373d-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="3373d-130">Alle nye miljøer kan kun hentes til version 3.x af PSA.</span><span class="sxs-lookup"><span data-stu-id="3373d-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="3373d-131">For at få den bedste oplevelse, når du bruger ældre versioner af Field Service- og PSA-programmer, skal du gå til siden **Systemindstillinger** og for feltet **Brug kun den nye Unified Interface (anbefales)** skal du klikke på **Nej**, da disse versioner ikke er designet til at blive indlæst korrekt i UCI.</span><span class="sxs-lookup"><span data-stu-id="3373d-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="3373d-132">Når du har slået UCI fra, kan du åbne og køre disse versioner af Field Service og PSA ved hjælp af den gamle webklient.</span><span class="sxs-lookup"><span data-stu-id="3373d-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
