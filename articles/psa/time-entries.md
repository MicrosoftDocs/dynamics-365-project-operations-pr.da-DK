---
title: Oprette tidsregistreringer
description: Dette emne indeholder oplysninger om, hvordan du opretter tidsregistreringer.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131258"
---
# <a name="create-time-entries"></a><span data-ttu-id="1549d-103">Oprette tidsregistreringer</span><span class="sxs-lookup"><span data-stu-id="1549d-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1549d-104">I tidligere versioner af Dynamics 365 Project Service Automation blev tidsregistreringer bogført ugentligt.</span><span class="sxs-lookup"><span data-stu-id="1549d-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="1549d-105">I version 3 af Project Service Automation bogføres tidsregistreringerne dagligt.</span><span class="sxs-lookup"><span data-stu-id="1549d-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="1549d-106">Men efter at der er oprettet nogle få tidsregistreringer, kan du oprette eller kopiere dem samlet.</span><span class="sxs-lookup"><span data-stu-id="1549d-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="1549d-107">Oprette en tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="1549d-107">Create a time entry</span></span>

<span data-ttu-id="1549d-108">Følg disse trin for at oprette en tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="1549d-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="1549d-109">På siden **Tidsregistreringer** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1549d-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="1549d-110">I dialogboksen **Hurtig oprettelse: Tidsregistrering** skal du angive varigheden af tidsregistreringen i minutter, timer eller dage.</span><span class="sxs-lookup"><span data-stu-id="1549d-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="1549d-111">Varigheden skal angives i følgende format: *x* minutter, *x* timer eller *x* dage.</span><span class="sxs-lookup"><span data-stu-id="1549d-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="1549d-112">Timer og dage kan også angives som decimaler, f.eks. *x,x* timer eller *x,x* dage.</span><span class="sxs-lookup"><span data-stu-id="1549d-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="1549d-113">Vælg tidsregistreringstype og det projekt, du vil angive tidsregistreringen for.</span><span class="sxs-lookup"><span data-stu-id="1549d-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="1549d-114">I feltet **Projektopgave** skal du finde opgaven for denne tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="1549d-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1549d-115">Hvis du opretter en tidsregistrering for en opgave, der ikke er tildelt til en bruger, skal du i feltet **Projektopgave** vælge knappen **Søg**, vælge **Skift visning** og derefter **Alle aktive projektopgaver** for at få vist alle opgaver.</span><span class="sxs-lookup"><span data-stu-id="1549d-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="1549d-116">Angiv evt. en beskrivelse, hvis det er nødvendigt, og vælg derefter **Gem og Luk**.</span><span class="sxs-lookup"><span data-stu-id="1549d-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="1549d-117">Når tidsregistreringen er oprettet og gemt, kan du redigere den i gitteret for tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="1549d-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="1549d-118">Gitteret for tidsregistreringer understøtter to formater:</span><span class="sxs-lookup"><span data-stu-id="1549d-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="1549d-119">Du kan angive tidsregistreringer i **tt:mm**-format.</span><span class="sxs-lookup"><span data-stu-id="1549d-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="1549d-120">Dette format konverteres derefter til timer og brøkdele.</span><span class="sxs-lookup"><span data-stu-id="1549d-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="1549d-121">Du kan angive timer og brøkdele direkte.</span><span class="sxs-lookup"><span data-stu-id="1549d-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="1549d-122">Bemærk, at brøkdele af en time ikke er minutter.</span><span class="sxs-lookup"><span data-stu-id="1549d-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="1549d-123">Derfor er 1,5 timer lig med 1 time og 30 minutter.</span><span class="sxs-lookup"><span data-stu-id="1549d-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="1549d-124">Den samme regel gælder for brøkdele af en dag.</span><span class="sxs-lookup"><span data-stu-id="1549d-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="1549d-125">En dag er 24 timer, og 0,5 dage er lig med 12 timer.</span><span class="sxs-lookup"><span data-stu-id="1549d-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="1549d-126">Oprette flere tidsregistreringer samtidigt</span><span class="sxs-lookup"><span data-stu-id="1549d-126">Bulk create time entries</span></span>

<span data-ttu-id="1549d-127">Når der er oprettet nogle få tidsregistreringer, kan du kopiere dem for at oprette flere tidsregistreringer samlet.</span><span class="sxs-lookup"><span data-stu-id="1549d-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="1549d-128">På siden **Tidsregistreringer** skal du vælge **Kopiér uge**.</span><span class="sxs-lookup"><span data-stu-id="1549d-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="1549d-129">I feltgruppen **Fra periode** skal du bruge felterne **Startdato** og **Slutdato** til at definere det datointerval, der skal kopieres tidsregistreringer fra.</span><span class="sxs-lookup"><span data-stu-id="1549d-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="1549d-130">I feltgruppen **Til periode** skal du i feltet **Startdato** angive den dato, der skal oprettes tidsregistreringer for.</span><span class="sxs-lookup"><span data-stu-id="1549d-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="1549d-131">Vælg **Kopiér** for at oprette en kopi af de tidsregistreringer, der svarer til den ugedag, der er angivet i feltgruppen **Til periode**.</span><span class="sxs-lookup"><span data-stu-id="1549d-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="1549d-132">Tidsregistreringen for mandag i sidste uge kopieres f.eks. til mandag i den uge, der er angivet i feltgruppen **Til periode**.</span><span class="sxs-lookup"><span data-stu-id="1549d-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="1549d-133">Importere data for tidsregistreringer</span><span class="sxs-lookup"><span data-stu-id="1549d-133">Import data for time entries</span></span>

<span data-ttu-id="1549d-134">Du kan importere data fra projektreservationer og tildelinger.</span><span class="sxs-lookup"><span data-stu-id="1549d-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="1549d-135">Når du importerer data, kan du angive datointervallet for de reservationer, der skal importeres, og derefter eksplicit vælge de reservationer, der skal oprettes som **Kladde**-tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="1549d-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="1549d-136">Funktioner for gruppering efter, sortering, søgning og filtrering</span><span class="sxs-lookup"><span data-stu-id="1549d-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="1549d-137">Du kan gruppere og filtrere tidsregistreringer efter de dimensioner, der er angivet i kolonnerne.</span><span class="sxs-lookup"><span data-stu-id="1549d-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="1549d-138">I feltet **Gruppér efter** skal du vælge den dimension, der skal bruges til at filtrere tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="1549d-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="1549d-139">Du kan også sortere tidsregistreringsposterne i stigende eller faldende rækkefølge ved hjælp af sorteringspilen på kolonneoverskrifterne.</span><span class="sxs-lookup"><span data-stu-id="1549d-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="1549d-140">Du kan også få vist eller skjule poster ved at vælge knappen **Filtrer** på kolonneoverskrifterne og derefter i boksen **Søg** angive den tekst, der skal bruges til at søge efter tidsregistreringer ud fra projektnavn, projektopgave, tidsregistrering eller ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1549d-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
