---
title: Nyheder eller ændringer i opdateringsudgivelse 13, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 13. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121616"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="e8fce-103">Opdateringsudgivelse 13 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="e8fce-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="e8fce-104">Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e8fce-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e8fce-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="e8fce-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e8fce-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e8fce-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e8fce-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="e8fce-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e8fce-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e8fce-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e8fce-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 13. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="e8fce-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="e8fce-110">Denne version har build-nummer V3.10.3.18 og er tilgængelig for følgende plan:</span><span class="sxs-lookup"><span data-stu-id="e8fce-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="e8fce-111">**Almindelig tilgængelighed (egen opdatering):** november 2019</span><span class="sxs-lookup"><span data-stu-id="e8fce-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="e8fce-112">**Automatisk opdatering:** december 2019</span><span class="sxs-lookup"><span data-stu-id="e8fce-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="e8fce-113">13. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="e8fce-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="e8fce-114">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="e8fce-114">Bug fixes</span></span>

- <span data-ttu-id="e8fce-115">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="e8fce-115">Time and Expense</span></span>

     - <span data-ttu-id="e8fce-116">Løst: Søgefunktionaliteten på siden **Udgiftsgodkendelse** fungerer ikke, når der søges efter udgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="e8fce-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="e8fce-117">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="e8fce-117">Resource Management</span></span>

     - <span data-ttu-id="e8fce-118">Løst: Tallene i afstemningen er blevet opdateret, så de er begrundet korrekt.</span><span class="sxs-lookup"><span data-stu-id="e8fce-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="e8fce-119">Løst: De navngivne ressourcer kan ikke tildeles opgaver via fanen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="e8fce-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="e8fce-120">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="e8fce-120">Project Management</span></span>

     - <span data-ttu-id="e8fce-121">Løst: Undtagelsen null-reference i forbindelse med tildeling af et teammedlem, når **TransactionType** mangler oplysninger om konfiguration af **Enhed** og **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="e8fce-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="e8fce-122">Sales</span><span class="sxs-lookup"><span data-stu-id="e8fce-122">Sales</span></span>

     - <span data-ttu-id="e8fce-123">Løst: Dubletter med poster af typen transaktion returnerer en fejl, når der oprettes rolleprisposter.</span><span class="sxs-lookup"><span data-stu-id="e8fce-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="e8fce-124">Løst: Ekstra knapper til **Ny salgsmulighed**, **Tilbud**, **Ordrelinje** og **Tilføj produkt** er synlige i kommandoer for salgsmuligheder, tilbud, bestil produkter og undergitteret for de projektbaserede linjer.</span><span class="sxs-lookup"><span data-stu-id="e8fce-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


