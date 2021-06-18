---
title: Nyheder eller ændringer i opdateringsudgivelse 30, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010419"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="199bd-103">Nyheder eller ændringer i opdateringsudgivelse 30, V3, til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="199bd-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="199bd-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="199bd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="199bd-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="199bd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="199bd-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="199bd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="199bd-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="199bd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="199bd-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="199bd-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="199bd-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 30. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="199bd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="199bd-110">Denne version har buildnummer V3.10.51.61 og er generelt tilgængelig via en opdatering, du selv har udført i april 2021.</span><span class="sxs-lookup"><span data-stu-id="199bd-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="199bd-111">30. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="199bd-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="199bd-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="199bd-112">Bug fixes</span></span>

<span data-ttu-id="199bd-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="199bd-113">**Time and Expense**</span></span>

<span data-ttu-id="199bd-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="199bd-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="199bd-115">Der opstår en fejl, når du opretter og gemmer en tidsregistrering på siden **Hurtig oprettelse**, hvis feltet **Rolle** fjernes.</span><span class="sxs-lookup"><span data-stu-id="199bd-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="199bd-116">Filteret for tidsregistrering anvender den forkerte filteroperator.</span><span class="sxs-lookup"><span data-stu-id="199bd-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="199bd-117">Kopierede timesedler vises ikke automatisk, når du vælger **Kopiér uge** i tidsregistreringskontrollen.</span><span class="sxs-lookup"><span data-stu-id="199bd-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="199bd-118">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="199bd-118">**Resource Management**</span></span>

<span data-ttu-id="199bd-119">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="199bd-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="199bd-120">Når du udvider en reservation, er den reservationsstatus, der er tildelt den faste reservation, forkert.</span><span class="sxs-lookup"><span data-stu-id="199bd-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="199bd-121">Hvis en reservation udvides, respekteres den reservationsstatus, der er defineret som **Bindende** i metadataene for reservationen.</span><span class="sxs-lookup"><span data-stu-id="199bd-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="199bd-122">Når der ikke er angivet en gyldig reservationsstatus, er fejlmeddelelsen ikke korrekt oversatte.</span><span class="sxs-lookup"><span data-stu-id="199bd-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="199bd-123">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="199bd-123">**Project Management**</span></span>

<span data-ttu-id="199bd-124">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="199bd-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="199bd-125">Projekter kan ikke oprettes i én valuta og medtage relaterede opgaver i en anden valuta.</span><span class="sxs-lookup"><span data-stu-id="199bd-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="199bd-126">**Salg**</span><span class="sxs-lookup"><span data-stu-id="199bd-126">**Sales**</span></span>

<span data-ttu-id="199bd-127">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="199bd-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="199bd-128">Når en prisliste kopieres, opdateres priser ikke.</span><span class="sxs-lookup"><span data-stu-id="199bd-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="199bd-129">Det lykkes ikke at lukke et tilbud som vundet, når omkostningsdetaljerne har en værdi for oprindelse.</span><span class="sxs-lookup"><span data-stu-id="199bd-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="199bd-130">I objektet **Projektopgave** er **Estimerede omkostninger** blevet omdøbt til **Planlagte omkostninger (basis)**.</span><span class="sxs-lookup"><span data-stu-id="199bd-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="199bd-131">Der oprettes en nulreferenceundtagelse, når fakturaer oprettes eller slettes.</span><span class="sxs-lookup"><span data-stu-id="199bd-131">A null reference exception is generated when invoices are created or deleted.</span></span>
