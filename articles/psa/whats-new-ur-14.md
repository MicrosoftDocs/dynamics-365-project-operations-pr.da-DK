---
title: Nyheder eller ændringer i opdateringsudgivelse 14, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 14. opdateringsudgivelse til Project Service Automation V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074130"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="a3411-103">Opdateringsudgivelse 14 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="a3411-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="a3411-104">Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a3411-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a3411-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="a3411-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a3411-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a3411-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a3411-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="a3411-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a3411-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a3411-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a3411-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 14. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="a3411-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="a3411-110">Denne version har build-nummer V3.10.4.21 og er tilgængelig for følgende plan:</span><span class="sxs-lookup"><span data-stu-id="a3411-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="a3411-111">**Almindelig tilgængelighed (egen opdatering):** januar 2020</span><span class="sxs-lookup"><span data-stu-id="a3411-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="a3411-112">**Automatisk opdatering:** februar 2020</span><span class="sxs-lookup"><span data-stu-id="a3411-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="a3411-113">14. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="a3411-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="a3411-114">Forbedringer</span><span class="sxs-lookup"><span data-stu-id="a3411-114">Enhancements</span></span>

- <span data-ttu-id="a3411-115">Sales</span><span class="sxs-lookup"><span data-stu-id="a3411-115">Sales</span></span>

     - <span data-ttu-id="a3411-116">Brugerdefinerede feltværdier fra **Detaljer for tilbudslinjer** kopieres til **Detaljer om projektkontraktlinjer** , når et tilbud opdateres til **Lukkes som vundet**.</span><span class="sxs-lookup"><span data-stu-id="a3411-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="a3411-117">Bekræftede projekter kan **Lukkes som tabt**.</span><span class="sxs-lookup"><span data-stu-id="a3411-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="a3411-118">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="a3411-118">Resource Management</span></span>

     - <span data-ttu-id="a3411-119">Når du udvider reservationer, får brugerne vist en bekræftelsesdialogboks, hvor det er muligt at opsummere reservationsresultaterne og oprette et link til at vedligeholde reservationer.</span><span class="sxs-lookup"><span data-stu-id="a3411-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="a3411-120">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="a3411-120">Bug fixes</span></span>

- <span data-ttu-id="a3411-121">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="a3411-121">Time and Expense</span></span>

     - <span data-ttu-id="a3411-122">Løst: Forbedret brugeroplevelse, når brugeren ikke har valgt, hvilke poster der skal rettes.</span><span class="sxs-lookup"><span data-stu-id="a3411-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="a3411-123">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="a3411-123">Resource Management</span></span>

     - <span data-ttu-id="a3411-124">Løst: Reservation af en ressource flere gange skaber overløb for navnet på den reserverbare ressource.</span><span class="sxs-lookup"><span data-stu-id="a3411-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="a3411-125">Sales</span><span class="sxs-lookup"><span data-stu-id="a3411-125">Sales</span></span>

     - <span data-ttu-id="a3411-126">Løst: Den samlede salgspris beregnes ikke, før brugeren også opretter en kostpris for udgiftsestimater på et projekt.</span><span class="sxs-lookup"><span data-stu-id="a3411-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="a3411-127">Løst: Lukning af et tilbud som **Vundet** mislykkes, hvis den tilknyttede projektkontrakt ikke er i tilstanden **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="a3411-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

