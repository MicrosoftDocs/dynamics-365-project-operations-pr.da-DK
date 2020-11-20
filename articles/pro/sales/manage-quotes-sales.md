---
title: Administrer projekttilbud
description: Dette emne indeholder oplysninger om projekttilbud.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177819"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="3b0fd-103">Administrer projekttilbud</span><span class="sxs-lookup"><span data-stu-id="3b0fd-103">Manage project quotes</span></span>

<span data-ttu-id="3b0fd-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3b0fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3b0fd-105">I Dynamics 365 Project Operations er projekttilbud designet til at hjælpe med at udarbejde forslag til projektarbejde.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="3b0fd-106">Strukturen i et projekttilbud i Project Operations er tiltænkt projektforslag med følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="3b0fd-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="3b0fd-107">Tilbudslinjer, der identificerer de separate komponenter i arbejdet, som vil blive præsenteret som komponenter på højt niveau.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="3b0fd-108">Tilbudslinjedetaljer, der identificerer og estimerer arbejdet for de enkelte komponenter eller tilbudslinje på højt niveau.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="3b0fd-109">Planen eller estimerede datoer og de finansielle aspekter for arbejdet er knyttet til den pågældende tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="3b0fd-110">Kontraktmodeller og fakturerbare komponenter konfigureres for hver tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="3b0fd-111">Denne konfiguration hjælper med at vurdere fordelingen af omsætning, forbrug og rentabilitet for de enkelte tilbudslinjer og det overordnede tilbud.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="3b0fd-112">Få vist alle projektbaserede tilbud</span><span class="sxs-lookup"><span data-stu-id="3b0fd-112">View all project-based quotes</span></span>

<span data-ttu-id="3b0fd-113">Du kan se en liste over alle projekttilbud på listesiden **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="3b0fd-114">Gå til **Salg** > **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="3b0fd-115">Der vises en liste over alle dine projekttilbud i systemet.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="3b0fd-116">Brug **Visningsskifteren** til at vælge andre filtrerede visninger for de pågældende tilbud.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="3b0fd-117">Ved hjælp af brugerdefinerede filterkriterier kan du konfigurere dine egne visninger og navigationsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="3b0fd-118">Der kan oprettes eller slettes tilbud fra denne listeside eller detaljesider.</span><span class="sxs-lookup"><span data-stu-id="3b0fd-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
