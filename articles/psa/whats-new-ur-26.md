---
title: Nyheder eller ændringer i opdateringsudgivelse 26, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948817"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="ba082-103">Opdateringsudgivelse 26 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="ba082-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ba082-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ba082-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ba082-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="ba082-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ba082-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ba082-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ba082-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="ba082-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ba082-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ba082-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ba082-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 26. opdateringsudgivelse, V3.</span><span class="sxs-lookup"><span data-stu-id="ba082-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="ba082-110">Denne version har et build-nummer V3.10.44.59 og er generelt tilgængelig via egen opdatering i december 2020.</span><span class="sxs-lookup"><span data-stu-id="ba082-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="ba082-111">26. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="ba082-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ba082-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="ba082-112">Bug fixes</span></span>

<span data-ttu-id="ba082-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="ba082-113">**Time and Expense**</span></span>

<span data-ttu-id="ba082-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="ba082-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba082-115">Brugerne kan ændre opgaven på en tidspost, der er godkendt/sendt.</span><span class="sxs-lookup"><span data-stu-id="ba082-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="ba082-116">Fejlmeddelelsen "objektreference ikke angivet" vises under lagring af klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="ba082-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="ba082-117">Import af tidsregistrering fra ressourcetildelinger opretter tidsposter med forkerte værdier for dato og klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="ba082-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="ba082-118">Når både Project Service Automation- og Field Service-appen er installeret, vises knappen **Ny** to gange på kommandolinjen for tidsregistreringer i Field Service-appen.</span><span class="sxs-lookup"><span data-stu-id="ba082-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="ba082-119">Cellerne **Tillad enhed** og **Enhedsgruppe** samarbejder nu i gitteret **Udgiftsestimater**.</span><span class="sxs-lookup"><span data-stu-id="ba082-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="ba082-120">Formularen **Opdater redigering af tidsregistrering** indeholder **Tidslinje**.</span><span class="sxs-lookup"><span data-stu-id="ba082-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="ba082-121">Tidsgodkendelse i forbindelse med tidsregistreringer, som ikke er projektrelaterede, blokerer systemet, når der søges efter en rolle som projektgodkender.</span><span class="sxs-lookup"><span data-stu-id="ba082-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="ba082-122">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="ba082-122">**Resource Management**</span></span>

<span data-ttu-id="ba082-123">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="ba082-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba082-124">Der er tilføjet en validering i plug-in **PostProjectCreate** for at kontrollere, om der er et primært krav, før der kan oprettes et.</span><span class="sxs-lookup"><span data-stu-id="ba082-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="ba082-125">Formularen til hurtig oprettelse af **Medlem af projektteam** viser en null-reference-undtagelse, hvis der fjernes felter fra formularen.</span><span class="sxs-lookup"><span data-stu-id="ba082-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="ba082-126">Der kan ikke oprettes krav til 12 timer fordelt over et år.</span><span class="sxs-lookup"><span data-stu-id="ba082-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="ba082-127">Forbedret fejlmeddelelse med null-reference-undtagelse under oprettelse af ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="ba082-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="ba082-128">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="ba082-128">**Project Management**</span></span>

<span data-ttu-id="ba082-129">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="ba082-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba082-130">Forbedret validering til håndtering af null-reference-undtagelse i plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="ba082-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="ba082-131">Projekter, der er udgivet af desktop-tilføjelsesprogrammet Microsoft Project sletter ikke-tildelte tildelinger.</span><span class="sxs-lookup"><span data-stu-id="ba082-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="ba082-132">En ny validering er tilføjet, når en opgaves projektreference er ugyldig pga. null-reference-undtagelse i plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="ba082-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="ba082-133">Teammedlemsgitteret viser ikke særskilte tildelinger i teammedlemsposten.</span><span class="sxs-lookup"><span data-stu-id="ba082-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="ba082-134">Der er tilføjet ny validering og fejlmeddelelser på grund af null-reference-undtagelsen i plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="ba082-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="ba082-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ba082-135">**Sales**</span></span>

<span data-ttu-id="ba082-136">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="ba082-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="ba082-137">Når du vælger en projektbaseret linje i tilbud eller kontrakt, bør knappen **Forslag** kun vises, når du vælger en produktbaseret linje, der er knyttet til et eksisterende produkt.</span><span class="sxs-lookup"><span data-stu-id="ba082-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="ba082-138">Opdel rettigeheden **Opret produkt** fra rettigheden **Opret_Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="ba082-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="ba082-139">Sletning af fakturalinjen medfører fejl i null-referencer på **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="ba082-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]