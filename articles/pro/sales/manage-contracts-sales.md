---
title: Administrer projektkontrakter
description: Dette emne indeholder oplysninger om visning af projektbaserede kontrakter.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273191"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="e8308-103">Administrer projektkontrakter</span><span class="sxs-lookup"><span data-stu-id="e8308-103">Manage project contracts</span></span>

<span data-ttu-id="e8308-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="e8308-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e8308-105">Projektkontrakter i Dynamics 365 Project Operations indlæser og administrerer de i henhold til kontrakterne aftalte oplysninger om forpligtelser og fakturering for et projekt.</span><span class="sxs-lookup"><span data-stu-id="e8308-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="e8308-106">Strukturen i en projektkontrakt i Project Operations er skræddersyet til projektbaseret arbejde med følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="e8308-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="e8308-107">Kontraktlinjer, der identificerer de separate komponenter i arbejdet, som vil blive præsenteret som komponenter på højt niveau på en projektfaktura.</span><span class="sxs-lookup"><span data-stu-id="e8308-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="e8308-108">Oplysninger om kontraktlinjer, der identificerer og estimerer arbejdet for de enkelte komponenter eller kontraktlinjer på højt niveau.</span><span class="sxs-lookup"><span data-stu-id="e8308-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="e8308-109">Estimatet omfatter planlægningen og de finansielle aspekter for arbejdet, der er knyttet til kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="e8308-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="e8308-110">De kontraherende modeller og fakturerbare komponenter konfigureres for hver kontraktlinje, der indeholder faktureringsarrangementet for hver kontraktlinje og den overordnede kontrakt.</span><span class="sxs-lookup"><span data-stu-id="e8308-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="e8308-111">Få vist alle projektbaserede kontrakter</span><span class="sxs-lookup"><span data-stu-id="e8308-111">View all project-based contracts</span></span>

<span data-ttu-id="e8308-112">Du kan se en liste over alle projektkontrakter på listesiden **Kontrakter**.</span><span class="sxs-lookup"><span data-stu-id="e8308-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="e8308-113">Gå til **Salg** > **Kontrakter**.</span><span class="sxs-lookup"><span data-stu-id="e8308-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="e8308-114">Der vises en liste over alle dine projektkontrakter i systemet.</span><span class="sxs-lookup"><span data-stu-id="e8308-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="e8308-115">Vælg **Skift visning** (rullepilen ud for navnet på visningen) for at vælge andre filtrerede visninger.</span><span class="sxs-lookup"><span data-stu-id="e8308-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="e8308-116">Du kan oprette dine egne visninger med brugerdefinerede filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="e8308-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="e8308-117">Der kan oprettes eller slettes kontrakter fra denne listeside eller detaljesider.</span><span class="sxs-lookup"><span data-stu-id="e8308-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]