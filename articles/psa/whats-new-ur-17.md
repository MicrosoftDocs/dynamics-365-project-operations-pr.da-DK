---
title: Nyheder eller ændringer i opdateringsudgivelse 17, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074128"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="a4671-103">Opdateringsudgivelse 17 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="a4671-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="a4671-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a4671-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a4671-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="a4671-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="a4671-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a4671-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a4671-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="a4671-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="a4671-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a4671-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a4671-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 17. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="a4671-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="a4671-110">Denne version har build-nummer V3.10.6.34 og er generelt tilgængelig via en opdatering, du selv skal foretage, i marts 2020.</span><span class="sxs-lookup"><span data-stu-id="a4671-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="a4671-111">17. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="a4671-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a4671-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="a4671-112">Bug fixes</span></span>

<span data-ttu-id="a4671-113">**Generelt**</span><span class="sxs-lookup"><span data-stu-id="a4671-113">**General**</span></span>

- <span data-ttu-id="a4671-114">Løst: Opdater Project service Automation for at gennemtvinge licenser til gruppemedlemmer (Projektressourcehub inkluderer metadata for serviceplanen for gruppemedlemmerne 3.x)</span><span class="sxs-lookup"><span data-stu-id="a4671-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="a4671-115">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="a4671-115">**Time and Expense**</span></span>

- <span data-ttu-id="a4671-116">Løst: Det er ikke muligt at ændre et udgiftsestimat fra en pris, der ikke er nul, til nul (0).</span><span class="sxs-lookup"><span data-stu-id="a4671-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="a4671-117">Ændringen ignoreres.</span><span class="sxs-lookup"><span data-stu-id="a4671-117">The change is ignored.</span></span>

<span data-ttu-id="a4671-118">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="a4671-118">**Project Management**</span></span>

- <span data-ttu-id="a4671-119">Løst: Der er blevet tilføjet en kontrol af, om der er null-værdier i et gruppemedlems stillingsbetegnelse.</span><span class="sxs-lookup"><span data-stu-id="a4671-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="a4671-120">Løst: Feltet **msdyn_userresourceid** i objektet **msdyn_resourceassignment** er blevet frarådet.</span><span class="sxs-lookup"><span data-stu-id="a4671-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="a4671-121">Løst: Ved at opgradere fra 2.x til 3.x kan du nu håndtere de tomme indsatsprofiler på opgavetildelinger.</span><span class="sxs-lookup"><span data-stu-id="a4671-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="a4671-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a4671-122">**Sales**</span></span>

- <span data-ttu-id="a4671-123">Løst: **Faktura.ForhåndsgodkendelseAfOpdateringAfFaktura** håndterer nu scenariet for gentildeling af postejere korrekt.</span><span class="sxs-lookup"><span data-stu-id="a4671-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="a4671-124">Løst: Når transaktionsklassen er **Tid** , er **UnitGroup** ikke redigerbar for alle objekter, herunder **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** og **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="a4671-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="a4671-125">Men **Enhed** kan ikke alene redigeres for **JournalLine** og **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="a4671-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


