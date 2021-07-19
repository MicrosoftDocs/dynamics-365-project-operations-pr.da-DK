---
title: Udrul Project Operations Dataverse-appen manuelt med understøttelse af dobbelt skrivning
description: I dette emne forklares det, hvordan du udruller Project Operations Dataverse-appen manuelt, så den understøtter dobbelt skrivning.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274001"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="57eae-103">Udrul Project Operations Dataverse-appen manuelt med understøttelse af dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="57eae-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="57eae-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="57eae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="57eae-105">I dette emne forklares det, hvordan du udruller Microsoft Dynamics 365 Project Operations i Microsoft Dataverse manuelt, så den understøtter dobbelt skrivning.</span><span class="sxs-lookup"><span data-stu-id="57eae-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="57eae-106">Project Operations registrerer miljøets konfiguration og tilføjer yderligere understøttelse af dobbelt skrivning, hvis forudsætningerne opfyldes.</span><span class="sxs-lookup"><span data-stu-id="57eae-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="57eae-107">Hvis du har fulgt instruktionerne i dette emne under udrulningen af Microsoft Dynamics Lifecycle Services (LCS), kan du springe udrulningen af Microsoft Power Platform-integrationen over (tidligere kendt som Common Data Service-miljøet) over.</span><span class="sxs-lookup"><span data-stu-id="57eae-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="57eae-108">Udrulningsprocessen for Project Operations i Dataverse, således at den understøtter dobbeltskrivning, har fire hovedtrin:</span><span class="sxs-lookup"><span data-stu-id="57eae-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="57eae-109">[Opret et nyt miljø i Dataverse, der understøtter dobbelt skrivning](#create).</span><span class="sxs-lookup"><span data-stu-id="57eae-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="57eae-110">[Tilføj forudsætninger for dobbelt skrivning i miljøet](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="57eae-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="57eae-111">[Tilføj appen Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="57eae-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="57eae-112">[Link til dine miljøer](#link).</span><span class="sxs-lookup"><span data-stu-id="57eae-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="57eae-113">Opret et nyt miljø i Dataverse, der understøtter dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="57eae-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="57eae-114">Du skal logge på som en administrator for at fuldføre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="57eae-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="57eae-115">Åbn [Power Platform Administration](https://admin.powerplatform.com), og log på som en administrator.</span><span class="sxs-lookup"><span data-stu-id="57eae-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="57eae-116">Opret et nyt miljø, og navngiv det.</span><span class="sxs-lookup"><span data-stu-id="57eae-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="57eae-117">Vælg miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="57eae-117">Select the environment type.</span></span> <span data-ttu-id="57eae-118">Hvis du tilmeldte dig prøvetilbuddet, skal du vælge **Prøveversion (abonnementsbaseret)**.</span><span class="sxs-lookup"><span data-stu-id="57eae-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="57eae-119">Bekræft udrulningsområdet.</span><span class="sxs-lookup"><span data-stu-id="57eae-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="57eae-120">Aktivér muligheden **Opret en database for dette miljø**.</span><span class="sxs-lookup"><span data-stu-id="57eae-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="57eae-121">Bekræft sproget, og kontrollér derefter, at valutaen stemmer overens med valutaen for dine Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="57eae-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="57eae-122">Aktivér muligheden **Dynamics 365-apps**, og bekræft, at feltet **Automatisk udrulning af disse apps** er angivet til **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="57eae-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="57eae-123">Tilføj en sikkerhedsgruppe, hvis der kræves en sikkerhedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="57eae-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="57eae-124">Vælg **Gem** for at oprette miljøet.</span><span class="sxs-lookup"><span data-stu-id="57eae-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="57eae-125">Vent, indtil udrulningen er fuldført, og miljøet når tilstanden **Klar**.</span><span class="sxs-lookup"><span data-stu-id="57eae-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="57eae-126">Tilføj forudsætninger for dobbelt skrivning i miljøet.</span><span class="sxs-lookup"><span data-stu-id="57eae-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="57eae-127">Understøttelse af dobbelt skrivning omfatter yderligere felter, der tilføjes til nøgleobjekter såsom objektet **Virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="57eae-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="57eae-128">Hvis du tilføjer understøttelse af dobbelt skrivning til et eksisterende miljø, skal du måske opdatere dataene for at aktivere supporten.</span><span class="sxs-lookup"><span data-stu-id="57eae-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="57eae-129">Du kan få flere oplysninger om, hvordan du bootstrapper dataene under [Bootstrap virksomhedsdata](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="57eae-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="57eae-130">Du kan finde flere oplysninger om systemkrav til dobbelt skrivning under [Systemkrav til dobbelt skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="57eae-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="57eae-131">Fuldfør denne procedure for at tilføje forudsætningerne for dobbelt skrivning til dit miljø.</span><span class="sxs-lookup"><span data-stu-id="57eae-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="57eae-132">Åbn det miljø, som du netop har oprettet, og gå derefter til **Resource** \> **Dynamics 365-apps**.</span><span class="sxs-lookup"><span data-stu-id="57eae-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="57eae-133">Vælg **Kerneløsning til dobbelt skrivning** på listen over apps, og installer den.</span><span class="sxs-lookup"><span data-stu-id="57eae-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="57eae-134">Vent, indtil installationen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="57eae-134">Wait until the installation is completed.</span></span> <span data-ttu-id="57eae-135">Vælg dernæst **Organisering af dobbelt skrivningsapplikation** på listen over apps, og installer den.</span><span class="sxs-lookup"><span data-stu-id="57eae-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="57eae-136">Tilføj appen Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="57eae-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="57eae-137">Du kan kun fuldføre denne procedure, hvis du har fuldført de tidligere procedurer, før du installerede Project Operations.</span><span class="sxs-lookup"><span data-stu-id="57eae-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="57eae-138">Under installationen analyserer systemet miljøkonfigurationen og tilføjer understøttelse af dobbelt skrivning, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="57eae-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="57eae-139">Åbn det miljø, som du oprettede tidligere, og gå derefter til **Resource** \> **Dynamics 365-apps**.</span><span class="sxs-lookup"><span data-stu-id="57eae-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="57eae-140">Vælg **Microsoft Dynamics 365 Project Operations** på applisten, og installer det.</span><span class="sxs-lookup"><span data-stu-id="57eae-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="57eae-141">Link til dine miljøer</span><span class="sxs-lookup"><span data-stu-id="57eae-141">Link your environments</span></span>

<span data-ttu-id="57eae-142">Når Dataverse-miljøet er udrullet, kan du konfigurere linket i dine Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="57eae-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="57eae-143">Følg trinnene i [Guiden til anvendelse af dobbelt skrivning for at linke til dine miljøer](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="57eae-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
