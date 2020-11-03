---
title: Nyheder eller ændringer i opdateringsudgivelse 16, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 16, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074131"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="83328-103">Opdateringsudgivelse 16 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="83328-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="83328-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="83328-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="83328-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="83328-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="83328-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="83328-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="83328-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="83328-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="83328-108">Du kan finde flere oplysninger i [Installer, opdater en foretrukket løsning](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="83328-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="83328-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 16. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="83328-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="83328-110">Denne version har build-nummer V3.10.6.34 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2020.</span><span class="sxs-lookup"><span data-stu-id="83328-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="83328-111">16. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="83328-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="83328-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="83328-112">Bug fixes</span></span>

-   <span data-ttu-id="83328-113">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="83328-113">Time and Expense</span></span>

    -   <span data-ttu-id="83328-114">Løst: Brugere, der forsøger at fremsende slettede tids- og udgiftsposter til godkendelse, modtager nu relevante fejlmeddelelser.</span><span class="sxs-lookup"><span data-stu-id="83328-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="83328-115">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="83328-115">Project Management</span></span>

    -   <span data-ttu-id="83328-116">Løst: De ressourceenheder, der er defineret for gruppemedlemmer i skabeloner, overholdes, når skabelonerne anvendes på et nyt projekt.</span><span class="sxs-lookup"><span data-stu-id="83328-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="83328-117">Løst: Forbedret håndtering af ny tildeling af postejerskab.</span><span class="sxs-lookup"><span data-stu-id="83328-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="83328-118">Løst: Projekter, der er ved at blive kopieret, kan ikke kopieret, før alle kopioperationer er fuldført.</span><span class="sxs-lookup"><span data-stu-id="83328-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="83328-119">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="83328-119">Resource Management</span></span>

    -   <span data-ttu-id="83328-120">Løst: Udvid reserveringer kan nu håndtere korte varigheder korrekt og opretter ikke længere nul timer for udvidede reservationer.</span><span class="sxs-lookup"><span data-stu-id="83328-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="83328-121">Løst: Afstemningsvisningen gengives nu, når tidszonen for projektet er +5:30 GMT, og brugerens tidszone er anderledes.</span><span class="sxs-lookup"><span data-stu-id="83328-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="83328-122">Sales</span><span class="sxs-lookup"><span data-stu-id="83328-122">Sales</span></span>

    -   <span data-ttu-id="83328-123">Løst: Når et projekt, der er knyttet til en kontraktlinje, fjernes, og der tilknyttes et nyt projekt, blev de faktiske poster i det nye projekt ikke evalueret igen på baggrund af de regler for fakturering og prissætning, der er defineret på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="83328-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="83328-124">Dette er blevet løst i denne udgivelse.</span><span class="sxs-lookup"><span data-stu-id="83328-124">This has been fixed in this release.</span></span> <span data-ttu-id="83328-125">Prisfastsættelsen og de faktiske poster i det netop tilknyttede projekt bliver tilbageført og genoprettet korrekt baseret på kontraktlinjens regler for prisfastsættelse og fakturering.</span><span class="sxs-lookup"><span data-stu-id="83328-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="83328-126">De faktiske poster for det ikke-tilknyttede projekt vil også blive evalueret igen og genoprettet som følge heraf.</span><span class="sxs-lookup"><span data-stu-id="83328-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="83328-127">Løst: Der er blevet føjet yderligere validering til en estimeret linjes **Beløb** -felt for at sikre, at null-værdier ikke bevares.</span><span class="sxs-lookup"><span data-stu-id="83328-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="83328-128">Løst: Når de faktiske værdier er blevet opdateret for et projekt, tilføjes der en opdateringsknap til hovedformularen for projektet for at give brugere mulighed for at synkronisere de faktiske værdier igen.</span><span class="sxs-lookup"><span data-stu-id="83328-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="83328-129">Løst: Når brugere opgraderer fra 2.X til 3.X, tillades projekter med en NULL-værdi for projektnavn.</span><span class="sxs-lookup"><span data-stu-id="83328-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>
