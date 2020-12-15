---
title: Nyheder eller ændringer i opdateringsudgivelse 26, V3, til Project Service Automation
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643256"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="d69b2-102">Opdateringsudgivelse 26 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="d69b2-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="d69b2-103">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d69b2-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d69b2-104">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="d69b2-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d69b2-105">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d69b2-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d69b2-106">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="d69b2-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d69b2-107">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d69b2-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d69b2-108">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 26. opdateringsudgivelse, V3.</span><span class="sxs-lookup"><span data-stu-id="d69b2-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="d69b2-109">Denne version har et build-nummer V3.10.44.59 og er generelt tilgængelig via egen opdatering i december 2020.</span><span class="sxs-lookup"><span data-stu-id="d69b2-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="d69b2-110">26. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="d69b2-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="d69b2-111">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="d69b2-111">Bug fixes</span></span>

<span data-ttu-id="d69b2-112">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="d69b2-112">**Time and Expense**</span></span>

<span data-ttu-id="d69b2-113">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="d69b2-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="d69b2-114">Brugerne kan ændre opgaven på en tidspost, der er godkendt/sendt.</span><span class="sxs-lookup"><span data-stu-id="d69b2-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="d69b2-115">Fejlmeddelelsen "objektreference ikke angivet" vises under lagring af klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="d69b2-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="d69b2-116">Import af tidsregistrering fra ressourcetildelinger opretter tidsposter med forkerte værdier for dato og klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="d69b2-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="d69b2-117">Når både Project Service Automation- og Field Service-appen er installeret, vises knappen **Ny** to gange på kommandolinjen for tidsregistreringer i Field Service-appen.</span><span class="sxs-lookup"><span data-stu-id="d69b2-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="d69b2-118">Cellerne **Tillad enhed** og **Enhedsgruppe** samarbejder nu i gitteret **Udgiftsestimater**.</span><span class="sxs-lookup"><span data-stu-id="d69b2-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="d69b2-119">Formularen **Opdater redigering af tidsregistrering** indeholder **Tidslinje**.</span><span class="sxs-lookup"><span data-stu-id="d69b2-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="d69b2-120">Tidsgodkendelse i forbindelse med tidsregistreringer, som ikke er projektrelaterede, blokerer systemet, når der søges efter en rolle som projektgodkender.</span><span class="sxs-lookup"><span data-stu-id="d69b2-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="d69b2-121">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="d69b2-121">**Resource Management**</span></span>

<span data-ttu-id="d69b2-122">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="d69b2-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="d69b2-123">Der er tilføjet en validering i plug-in **PostProjectCreate** for at kontrollere, om der er et primært krav, før der kan oprettes et.</span><span class="sxs-lookup"><span data-stu-id="d69b2-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="d69b2-124">Formularen til hurtig oprettelse af **Medlem af projektteam** viser en null-reference-undtagelse, hvis der fjernes felter fra formularen.</span><span class="sxs-lookup"><span data-stu-id="d69b2-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="d69b2-125">Der kan ikke oprettes krav til 12 timer fordelt over et år.</span><span class="sxs-lookup"><span data-stu-id="d69b2-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="d69b2-126">Forbedret fejlmeddelelse med null-reference-undtagelse under oprettelse af ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="d69b2-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="d69b2-127">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="d69b2-127">**Project Management**</span></span>

<span data-ttu-id="d69b2-128">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="d69b2-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="d69b2-129">Forbedret validering til håndtering af null-reference-undtagelse i plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="d69b2-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="d69b2-130">Projekter, der er udgivet af desktop-tilføjelsesprogrammet Microsoft Project sletter ikke-tildelte tildelinger.</span><span class="sxs-lookup"><span data-stu-id="d69b2-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="d69b2-131">En ny validering er tilføjet, når en opgaves projektreference er ugyldig pga. null-reference-undtagelse i plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="d69b2-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="d69b2-132">Teammedlemsgitteret viser ikke særskilte tildelinger i teammedlemsposten.</span><span class="sxs-lookup"><span data-stu-id="d69b2-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="d69b2-133">Der er tilføjet ny validering og fejlmeddelelser på grund af null-reference-undtagelsen i plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="d69b2-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="d69b2-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d69b2-134">**Sales**</span></span>

<span data-ttu-id="d69b2-135">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="d69b2-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="d69b2-136">Når du vælger en projektbaseret linje i tilbud eller kontrakt, bør knappen **Forslag** kun vises, når du vælger en produktbaseret linje, der er knyttet til et eksisterende produkt.</span><span class="sxs-lookup"><span data-stu-id="d69b2-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="d69b2-137">Opdel rettigeheden **Opret produkt** fra rettigheden **Opret_Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="d69b2-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="d69b2-138">Sletning af fakturalinjen medfører fejl i null-referencer på **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="d69b2-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
