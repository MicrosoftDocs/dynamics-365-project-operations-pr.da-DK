---
title: Nyheder i 13. opdateringsudgivelse til Project Service Automation, V3
description: Dette emne indeholder oplysninger om nyhederne i 13. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750544"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="d9beb-103">13. opdateringsudgivelse til Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="d9beb-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="d9beb-104">Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d9beb-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d9beb-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="d9beb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d9beb-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d9beb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d9beb-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="d9beb-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d9beb-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d9beb-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d9beb-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 13. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="d9beb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="d9beb-110">Denne version har build-nummer V3.10.3.18 og er tilgængelig for følgende plan:</span><span class="sxs-lookup"><span data-stu-id="d9beb-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="d9beb-111">**Almindelig tilgængelighed (egen opdatering):** november 2019</span><span class="sxs-lookup"><span data-stu-id="d9beb-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="d9beb-112">**Automatisk opdatering:** december 2019</span><span class="sxs-lookup"><span data-stu-id="d9beb-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="d9beb-113">13. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="d9beb-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="d9beb-114">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="d9beb-114">Bug fixes</span></span>

- <span data-ttu-id="d9beb-115">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="d9beb-115">Time and Expense</span></span>

     - <span data-ttu-id="d9beb-116">Løst: Søgefunktionaliteten på siden **Udgiftsgodkendelse** fungerer ikke, når der søges efter udgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="d9beb-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="d9beb-117">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="d9beb-117">Resource Management</span></span>

     - <span data-ttu-id="d9beb-118">Løst: Tallene i afstemningen er blevet opdateret, så de er begrundet korrekt.</span><span class="sxs-lookup"><span data-stu-id="d9beb-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="d9beb-119">Løst: De navngivne ressourcer kan ikke tildeles opgaver via fanen **Planlægning**.</span><span class="sxs-lookup"><span data-stu-id="d9beb-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="d9beb-120">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="d9beb-120">Project Management</span></span>

     - <span data-ttu-id="d9beb-121">Løst: Undtagelsen null-reference i forbindelse med tildeling af et teammedlem, når **TransactionType** mangler oplysninger om konfiguration af **Enhed** og **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="d9beb-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="d9beb-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d9beb-122">Sales</span></span>

     - <span data-ttu-id="d9beb-123">Løst: Dubletter med poster af typen transaktion returnerer en fejl, når der oprettes rolleprisposter.</span><span class="sxs-lookup"><span data-stu-id="d9beb-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="d9beb-124">Løst: Ekstra knapper til **Ny salgsmulighed**, **Tilbud**, **Ordrelinje** og **Tilføj produkt** er synlige i kommandoer for salgsmuligheder, tilbud, ordreprodukter og undergittret for projektbaserede linjer.</span><span class="sxs-lookup"><span data-stu-id="d9beb-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


