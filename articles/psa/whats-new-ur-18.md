---
title: Nyheder eller ændringer i opdateringsudgivelse 18, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: bd6038b3594e8507c4a441b00ddc2eb240f796dc
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949177"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="5c365-103">Opdateringsudgivelse 18 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="5c365-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5c365-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5c365-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5c365-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="5c365-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5c365-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5c365-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5c365-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="5c365-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="5c365-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5c365-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5c365-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 18. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="5c365-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="5c365-110">Denne version har buildnummer V3.10.8.12 og er generelt tilgængelig via en opdatering, du selv har udført i april 2020.</span><span class="sxs-lookup"><span data-stu-id="5c365-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="5c365-111">18. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="5c365-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5c365-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="5c365-112">Bug fixes</span></span>

<span data-ttu-id="5c365-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="5c365-113">**Time and Expense**</span></span>

- <span data-ttu-id="5c365-114">Løst: Processerne **Tilbagekald**, **Anmodning** og **Annuller godkendelse** udløser undtagelser med fejlmeddelelser, der ikke er tydelige.</span><span class="sxs-lookup"><span data-stu-id="5c365-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="5c365-115">Løst: Når det ikke er muligt at **Annullere godkendelse** af en udgift, udløses der ikke en relevant undtagelsesfejl.</span><span class="sxs-lookup"><span data-stu-id="5c365-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="5c365-116">Løst: Tidsregistreringsgitteret håndterer fejlagtigt ikke-arbejdsdage i Australien efter parameteren for sommertid (sommertid) i oktober.</span><span class="sxs-lookup"><span data-stu-id="5c365-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="5c365-117">Løst: Forkert standardlogik forhindrer indsendelse af udgifter.</span><span class="sxs-lookup"><span data-stu-id="5c365-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="5c365-118">Løst: Når godkendelsen af tidsregistreringen mislykkes, forbliver godkendelsen i tilstanden **Afventende**.</span><span class="sxs-lookup"><span data-stu-id="5c365-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="5c365-119">Løst: SQL-fejl for massegodkendelser (baglås/timeout).</span><span class="sxs-lookup"><span data-stu-id="5c365-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="5c365-120">Løst: Væsentlige problemer med ydeevnen i brugeroplevelsen, som skyldes en opdatering af gruppemedlemmer under godkendelse af tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="5c365-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="5c365-121">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="5c365-121">**Project Management**</span></span>

- <span data-ttu-id="5c365-122">Løst: Tidszonemeddelelse, der flyttes fra visningen **Afstemning** til hovedformularen **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="5c365-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="5c365-123">Løst: Kalenderskabelonen bruges ikke korrekt, når der åbnes en ny projektformular.</span><span class="sxs-lookup"><span data-stu-id="5c365-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="5c365-124">Løst: Det er i chrom-baserede browsere ikke muligt for brugere ubesværet at kunne vælge de foregående opgaver, der skal slettes.</span><span class="sxs-lookup"><span data-stu-id="5c365-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="5c365-125">Løst: Oprettelse eller kopiering af et **Projekt fra en tom skabelon** henter ikke-relaterede tildelinger.</span><span class="sxs-lookup"><span data-stu-id="5c365-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="5c365-126">Løst: I bestemte grænsesager resulterer oprettelsen af en ny tildeling fra opgavegitteret i dubletter af de poster, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="5c365-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="5c365-127">Løst: I manuel tilstand kan brugerne ikke opdatere opgavernes startdatoer, så de ligger efter den aktuelle gemte dato.</span><span class="sxs-lookup"><span data-stu-id="5c365-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="5c365-128">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="5c365-128">**Resource Management**</span></span>

- <span data-ttu-id="5c365-129">Løst: I subtotalrækken i visningen **Afstemning** beregnes reservationsvariansen ikke korrekt, når reservationen er blevet forlænget.</span><span class="sxs-lookup"><span data-stu-id="5c365-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="5c365-130">Løst: Visningen **Afstemning** vises ikke ressourcetildelinger korrekt, når den reserverbare ressource har en kalender, der ikke stemmer overens med projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="5c365-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="5c365-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="5c365-131">**Sales**</span></span>

- <span data-ttu-id="5c365-132">Løst: Når tidsangivelser godkendes igen (**Godkend > Annuller >** Godkend igen), oprettes der en dublet, der ikke kan faktureres.</span><span class="sxs-lookup"><span data-stu-id="5c365-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]