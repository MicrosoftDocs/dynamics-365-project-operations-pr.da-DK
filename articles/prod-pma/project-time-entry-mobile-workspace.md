---
title: Mobilt arbejdsområde for tidsregistrering på projekter
description: Dette emne indeholder oplysninger om det mobile arbejdsområde for tidsregistreringer på projekter. I dette arbejdsområde kan brugere indtaste og spare tid i løbet af et projekt ved at anvende deres mobilenhed.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eae471cf42f02e64844a4682cc8ed02cbb14c34
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288867"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="cbeda-104">Mobilt arbejdsområde for tidsregistrering på projekter</span><span class="sxs-lookup"><span data-stu-id="cbeda-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbeda-105">Dette emne indeholder oplysninger om det mobile arbejdsområde for **Tidsregistrering på projekter**.</span><span class="sxs-lookup"><span data-stu-id="cbeda-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="cbeda-106">I dette arbejdsområde kan brugere indtaste og spare tid i løbet af et projekt ved at anvende deres mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="cbeda-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="cbeda-107">Dette mobile arbejdsområde er beregnet til at blive brugt sammen med Dynamics 365 Unified Ops-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="cbeda-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="cbeda-108">Oversigt</span><span class="sxs-lookup"><span data-stu-id="cbeda-108">Overview</span></span>
<span data-ttu-id="cbeda-109">Projektressourcer tildeles ofte på stedet eller rejser som led i deres daglige arbejde.</span><span class="sxs-lookup"><span data-stu-id="cbeda-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="cbeda-110">Det mobile arbejdsområde for **Tidsregistrering på projekter** gør det muligt for brugerne at angive deres fakturerbare eller ikke-fakturerbare tid i forhold til et projekt på den ønskede mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="cbeda-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="cbeda-111">Projektressourcer kan derfor registrere tidspunkter når som helst og hvor som helst.</span><span class="sxs-lookup"><span data-stu-id="cbeda-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="cbeda-112">Du kan også få vist tidsregistreringer, der allerede er blevet registreret.</span><span class="sxs-lookup"><span data-stu-id="cbeda-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="cbeda-113">Derudover kan brugere i det mobile arbejdsområde for **Tidsregistrering på projekter** udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="cbeda-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="cbeda-114">På en given dato kan du angive det antal timer, som du har brugt på en bestemt opgave.</span><span class="sxs-lookup"><span data-stu-id="cbeda-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="cbeda-115">Søg efter projektnavn eller kunde for at finde det projekt, der skal angives tid for.</span><span class="sxs-lookup"><span data-stu-id="cbeda-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="cbeda-116">Angiv kategorien og aktiviteten for den tid, du har brugt.</span><span class="sxs-lookup"><span data-stu-id="cbeda-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="cbeda-117">Registrer tiden som fakturerbar eller ikke-fakturerbar på projektet.</span><span class="sxs-lookup"><span data-stu-id="cbeda-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="cbeda-118">Du kan eventuelt angive eksterne eller interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="cbeda-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cbeda-119">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="cbeda-119">Prerequisites</span></span>
<span data-ttu-id="cbeda-120">Forudsætningerne er forskellige, afhængigt af den version af Microsoft Dynamics 365, der er installeret i din organisation.</span><span class="sxs-lookup"><span data-stu-id="cbeda-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="cbeda-121">Forudsætninger, hvis du bruger Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="cbeda-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="cbeda-122">Hvis Finance er blevet udrullet i din organisation, skal systemadministrator publicere det mobile arbejdsområde for **Tidsregistrering på projekter**.</span><span class="sxs-lookup"><span data-stu-id="cbeda-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="cbeda-123">Du kan finde en vejledning i [Publicer et mobilt arbejdsområde](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="cbeda-123">For instructions, see [Publish a mobile workspace](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="cbeda-124">Forudsætninger, hvis du bruger version 1611 sammen med platformsopdatering 3 eller nyere</span><span class="sxs-lookup"><span data-stu-id="cbeda-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="cbeda-125">Hvis version 1611 med platformsopdatering 3 eller nyere er blevet udrullet i din organisation, skal følgende forudsætninger fuldføres af systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="cbeda-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cbeda-126">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="cbeda-126">Prerequisite</span></span></th>
<th><span data-ttu-id="cbeda-127">Rolle</span><span class="sxs-lookup"><span data-stu-id="cbeda-127">Role</span></span></th>
<th><span data-ttu-id="cbeda-128">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cbeda-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="cbeda-129">Implementer KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="cbeda-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="cbeda-130">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="cbeda-130">System administrator</span></span></td>
<td><span data-ttu-id="cbeda-131">KB 4018050 er et hotfix til X++-opdateringen eller metadata, der indeholder det mobile arbejdsområde <strong>Tidsregistrering på projekter</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbeda-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="cbeda-132">Hvis du vil implementere KB 4018050, skal systemadministratoren udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="cbeda-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="cbeda-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Hent hotfixet til metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="cbeda-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="cbeda-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hotfixet til metadata</a>.</span><span class="sxs-lookup"><span data-stu-id="cbeda-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="cbeda-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbare pakke</a>, som indeholder modellerne <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong>, og overfør derefter den installerbare pakke til LCS.</span><span class="sxs-lookup"><span data-stu-id="cbeda-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="cbeda-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a>.</span><span class="sxs-lookup"><span data-stu-id="cbeda-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cbeda-137">Publicer det mobile arbejdsområde for <strong>Tidsregistrering på projekter</strong>.</span><span class="sxs-lookup"><span data-stu-id="cbeda-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="cbeda-138">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="cbeda-138">System administrator</span></span></td>
<td><span data-ttu-id="cbeda-139">Se <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicer et mobilt arbejdsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="cbeda-139">See <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="cbeda-140">Hent og installer mobilappen</span><span class="sxs-lookup"><span data-stu-id="cbeda-140">Download and install the mobile app</span></span>

<span data-ttu-id="cbeda-141">Hent og installer Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="cbeda-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="cbeda-142">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="cbeda-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="cbeda-143">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="cbeda-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="cbeda-144">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="cbeda-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="cbeda-145">Start mobilappen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="cbeda-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="cbeda-146">Angiv din URL-adresse til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cbeda-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="cbeda-147">Første gang, du logger på, bliver du bedt om at angive dit brugernavn og din adgangskode.</span><span class="sxs-lookup"><span data-stu-id="cbeda-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="cbeda-148">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="cbeda-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="cbeda-149">Når du har logget på, vises de tilgængelige arbejdsområder for virksomheden.</span><span class="sxs-lookup"><span data-stu-id="cbeda-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="cbeda-150">Bemærk, at hvis systemadministratoren udgiver et nyt arbejdsområde på et senere tidspunkt, skal du opdatere listen over mobile arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="cbeda-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="cbeda-151">[![Træk ned for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="cbeda-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="cbeda-152">Angiv tid ved at bruge det mobile arbejdsområde for tidsregistrering på projekter</span><span class="sxs-lookup"><span data-stu-id="cbeda-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="cbeda-153">Vælg arbejdsområdet **Tidsregistrering på projekter** på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="cbeda-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="cbeda-154">Vælg **Tidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="cbeda-154">Select **Time entry**.</span></span> <span data-ttu-id="cbeda-155">Kalenderdatoerne for den aktuelle uge vises.</span><span class="sxs-lookup"><span data-stu-id="cbeda-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="cbeda-156">Vælg **Handlinger** &gt; **Ny registrering** for en angivet dato.</span><span class="sxs-lookup"><span data-stu-id="cbeda-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="cbeda-157">Angiv antallet af timer, der skal registreres.</span><span class="sxs-lookup"><span data-stu-id="cbeda-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="cbeda-158">Vælg projektet for tidsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="cbeda-158">Select the project for the time entry.</span></span> <span data-ttu-id="cbeda-159">På en liste vises de projekter, der er indlæst i appen til offlinebrug.</span><span class="sxs-lookup"><span data-stu-id="cbeda-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="cbeda-160">Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer.</span><span class="sxs-lookup"><span data-stu-id="cbeda-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="cbeda-161">Du kan finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="cbeda-161">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="cbeda-162">Hvis projektet ikke findes på listen, skal du vælge **Søg**.</span><span class="sxs-lookup"><span data-stu-id="cbeda-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="cbeda-163">Søg efter navn, eller skift for at søge efter projektnavn eller kunde.</span><span class="sxs-lookup"><span data-stu-id="cbeda-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="cbeda-164">Vælg en kategori.</span><span class="sxs-lookup"><span data-stu-id="cbeda-164">Select a category.</span></span> <span data-ttu-id="cbeda-165">På en liste vises de kategorier, der er indlæst i appen til offlinebrug.</span><span class="sxs-lookup"><span data-stu-id="cbeda-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="cbeda-166">Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer.</span><span class="sxs-lookup"><span data-stu-id="cbeda-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="cbeda-167">Du kan finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="cbeda-167">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="cbeda-168">Hvis kategorien ikke findes på listen, skal du vælge **Søg**.</span><span class="sxs-lookup"><span data-stu-id="cbeda-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="cbeda-169">Søg efter kategori, eller skift til at søge efter kategorinavn.</span><span class="sxs-lookup"><span data-stu-id="cbeda-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="cbeda-170">Vælg en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="cbeda-170">Select an activity.</span></span> <span data-ttu-id="cbeda-171">På en liste vises de aktiviteter, der er indlæst i appen til offlinebrug.</span><span class="sxs-lookup"><span data-stu-id="cbeda-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="cbeda-172">Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer.</span><span class="sxs-lookup"><span data-stu-id="cbeda-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="cbeda-173">Du kan finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="cbeda-173">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="cbeda-174">Hvis aktiviteten ikke findes på listen, skal du vælge **Søg**.</span><span class="sxs-lookup"><span data-stu-id="cbeda-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="cbeda-175">Søg efter aktivitetsnummer, eller skift til at søge efter formål.</span><span class="sxs-lookup"><span data-stu-id="cbeda-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="cbeda-176">Vælg linjeegenskaben.</span><span class="sxs-lookup"><span data-stu-id="cbeda-176">Select the line property.</span></span>
12. <span data-ttu-id="cbeda-177">Valgfrit: Angiv eksterne og interne kommentarer.</span><span class="sxs-lookup"><span data-stu-id="cbeda-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="cbeda-178">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="cbeda-178">Select **Done**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]