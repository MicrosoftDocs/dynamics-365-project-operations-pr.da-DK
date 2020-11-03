---
title: Bruge planlægningsområdet til at reservere projektressourcer
description: Dette emne indeholder oplysninger om, hvordan du reserverer ressourcer.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: fa7e34b12f3767e89cc13ddde930e5c9f8ebc565
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074394"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="93ca4-103">Bruge planlægningsområdet til at reservere projektressourcer</span><span class="sxs-lookup"><span data-stu-id="93ca4-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="93ca4-104">Ud over at reservere ressourcer til et projekt inde fra et projekt er det muligt at reservere ressourcer definitivt eller foreløbigt i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="93ca4-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="93ca4-105">Før du kan reservere fra planlægningsområdet, skal du oprette eller generere ressourcekrav.</span><span class="sxs-lookup"><span data-stu-id="93ca4-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="93ca4-106">Følg disse trin for at oprette ressourcekrav i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="93ca4-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="93ca4-107">Hvis ruden **Krav til reservationer** nederst på siden er skjult, skal du markere kontrolelementet for udvidelse for at åbne den.</span><span class="sxs-lookup"><span data-stu-id="93ca4-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="93ca4-108">I ruden **Krav til reservationer** på fanen **Projekt** skal du vælge det krav, der skal reserveres.</span><span class="sxs-lookup"><span data-stu-id="93ca4-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![Krav er valgt på fanen Projekt](media/Resource-Management-image73.png)

3. <span data-ttu-id="93ca4-110">Vælg **Find tilgængelighed** for at filtrere de reserverbare ressourcer og få vist de tilgængelige ressourcer.</span><span class="sxs-lookup"><span data-stu-id="93ca4-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="93ca4-111">Vælg en eller flere ressourcer i planlægningsområdet.</span><span class="sxs-lookup"><span data-stu-id="93ca4-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="93ca4-112">I ruden **Opret ressourcereservation** til højre på siden skal du angive reservationsoplysningerne og derefter vælge **Reservér og afslut.**</span><span class="sxs-lookup"><span data-stu-id="93ca4-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Opret ruden Ressourcereservation for den valgte reserverbare ressource](media/Resource-Management-image74.png)

6. <span data-ttu-id="93ca4-114">Når kravet er valgt i ruden **Opret ressourcereservation** , skal du vælge en eller flere celler i en ressource for at oprette reservationen.</span><span class="sxs-lookup"><span data-stu-id="93ca4-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Flere celler valgt til en ressource](media/Resource-Management-image75.png)

7. <span data-ttu-id="93ca4-116">Vælg **Reservér**.</span><span class="sxs-lookup"><span data-stu-id="93ca4-116">Select **Book**.</span></span>

<span data-ttu-id="93ca4-117">Kravet opfyldes ved hjælp af den valgte ressource.</span><span class="sxs-lookup"><span data-stu-id="93ca4-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="93ca4-118">Bemærk, at i ruden **Krav til reservationer** er kravet blevet opdateret, og ressourcen vises som reserveret til projektet.</span><span class="sxs-lookup"><span data-stu-id="93ca4-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Ressource reserveret til projektet](media/Resource-Management-image76.png)
