---
title: Nyheder eller ændringer i opdateringsudgivelse 22, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8863d321ad88d761d0fcbd82ca26562a69468f2f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948997"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="e3fef-103">Opdateringsudgivelse 22 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="e3fef-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e3fef-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e3fef-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e3fef-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="e3fef-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e3fef-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e3fef-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e3fef-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="e3fef-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e3fef-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e3fef-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e3fef-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 22. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="e3fef-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="e3fef-110">Denne version har buildnummer V 3.10.33.48 og er generelt tilgængelig via en opdatering, du selv har udført i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="e3fef-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="e3fef-111">22. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="e3fef-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e3fef-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="e3fef-112">Bug fixes</span></span>



<span data-ttu-id="e3fef-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="e3fef-113">**Time and Expense**</span></span>

<span data-ttu-id="e3fef-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="e3fef-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e3fef-115">**Tidsregistreringer** tilføjes ikke automatisk i planen for Tidsregistreringer efter importen.</span><span class="sxs-lookup"><span data-stu-id="e3fef-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="e3fef-116">Datovælgergitteret for **Tidsregistrering** genkender ikke en brugers internationale indstillinger.</span><span class="sxs-lookup"><span data-stu-id="e3fef-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="e3fef-117">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="e3fef-117">**Resource Management**</span></span>

<span data-ttu-id="e3fef-118">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="e3fef-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="e3fef-119">I manuel tilstand kan ændringer af konturerne **Ressourcetildelingen** ikke genkendes under generering af **Ressourcebehov**.</span><span class="sxs-lookup"><span data-stu-id="e3fef-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="e3fef-120">**Ressourceanmodninger** understøtter ikke brugerdefinerede anmodningsstatusser.</span><span class="sxs-lookup"><span data-stu-id="e3fef-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="e3fef-121">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="e3fef-121">**Project Management**</span></span>

<span data-ttu-id="e3fef-122">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="e3fef-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="e3fef-123">Hvis dobbeltklikker på EstimateGridControl, fortolkes opdelte hollandske formatnumre ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="e3fef-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="e3fef-124">Tildelte timer opdateres ikke korrekt, når tildelinger ændres ved hjælp af Microsoft Project-klienttilføjelsesprogrammet for stationære computere.</span><span class="sxs-lookup"><span data-stu-id="e3fef-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="e3fef-125">Gitrene for Projektsporing og Estimater viser ukorrekte salgsvalutakode, når en kontraktvaluta er forskellig fra kundevaluta, og organisation er konfigureret til at vise valutakoder i stedet for valutasymboler.</span><span class="sxs-lookup"><span data-stu-id="e3fef-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="e3fef-126">Et gruppemedlems slutdato vil tilføje én dag, hvis arbejdstidsplanen er 24 timer pr. dag.</span><span class="sxs-lookup"><span data-stu-id="e3fef-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="e3fef-127">Hvis du føjer en Transaktionskategori til en Projektplan, udløser den ikke automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="e3fef-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="e3fef-128">Følgende fejl vises, når du føjer et gruppemedlem til Projektskabelonen: "Ressourcekrav kan ikke knyttes til projektskabeloner".</span><span class="sxs-lookup"><span data-stu-id="e3fef-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="e3fef-129">Scriptet med regel for bånd "msdyn.Approval.CanApproveOrReject" viser en timeoutfejl.</span><span class="sxs-lookup"><span data-stu-id="e3fef-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="e3fef-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e3fef-130">**Sales**</span></span>

<span data-ttu-id="e3fef-131">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="e3fef-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="e3fef-132">Meddelelsen om valideringsfejl vises ikke, når der vælges en Kostprisliste i Prislisteopslaget på "Formular/objekt for prisliste for nyt tilbudsprojekt".</span><span class="sxs-lookup"><span data-stu-id="e3fef-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="e3fef-133">Når du lukker tilbuddet som vundet, navigeres der ikke til den oprettede kontrakt, hvis et BPF, der er knyttet til tilbuddet, er i det sidste stadie.</span><span class="sxs-lookup"><span data-stu-id="e3fef-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="e3fef-134">Hvis du tilbagefører **Ikke-faktureret salg**, knyttes de til den oprindelige omkostning, når en tidsregistrering tilbagekaldes.</span><span class="sxs-lookup"><span data-stu-id="e3fef-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="e3fef-135">Når du har valgt knappen **Bekræft**, ændres fakturaens status ikke til **Bekræftet**, medmindre fakturaen opdateres.</span><span class="sxs-lookup"><span data-stu-id="e3fef-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]