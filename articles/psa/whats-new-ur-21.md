---
title: Nyheder eller ændringer i opdateringsudgivelse 21, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 21, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074123"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="9f16b-103">Opdateringsudgivelse 21 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="9f16b-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="9f16b-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9f16b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9f16b-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="9f16b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9f16b-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9f16b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9f16b-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="9f16b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9f16b-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9f16b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9f16b-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 21. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="9f16b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="9f16b-110">Denne version har buildnummer V 3.10.32.50 og er generelt tilgængelig via en opdatering, du selv har udført i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="9f16b-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="9f16b-111">21. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="9f16b-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9f16b-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="9f16b-112">Bug fixes</span></span>

<span data-ttu-id="9f16b-113">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="9f16b-113">**Time and Expense**</span></span>

<span data-ttu-id="9f16b-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9f16b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9f16b-115">Når du hoster **Kontrolelementet for tidsregistreringsgitteret** i Dashboards, anvender gitteret ikke hele bredden på objektbeholderen for Dashboardgitteret.</span><span class="sxs-lookup"><span data-stu-id="9f16b-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="9f16b-116">I forbindelse med bestemte tidszoner viser gitterkontrolelementet for **Tidsregistrering** ikke poster.</span><span class="sxs-lookup"><span data-stu-id="9f16b-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="9f16b-117">Tidsregistreringer, der ligger efter kl. 21:00, vises på den forkerte dag.</span><span class="sxs-lookup"><span data-stu-id="9f16b-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="9f16b-118">Brugere kan ikke sende udgifter, hvis udgiftskategorien **Kvittering for udgift påkrævet** ikke ar en værdi.</span><span class="sxs-lookup"><span data-stu-id="9f16b-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="9f16b-119">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="9f16b-119">**Resource Management**</span></span>

<span data-ttu-id="9f16b-120">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9f16b-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="9f16b-121">Inaktive bookinger vises i oversigten **Afstemning**.</span><span class="sxs-lookup"><span data-stu-id="9f16b-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="9f16b-122">Generisk ressourceopfyldelse manglede validering for at sikre, at der findes en gyldig bookingstatus.</span><span class="sxs-lookup"><span data-stu-id="9f16b-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="9f16b-123">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="9f16b-123">**Project Management**</span></span>

<span data-ttu-id="9f16b-124">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9f16b-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="9f16b-125">Formulargitterne for **Projekt** ( **Ressourcetildeling** , **Opgave** , **Afstemning** , **Udgiftsestimater** ) er fortsat redigerbare, også selvom et projekt ikke er aktivt.</span><span class="sxs-lookup"><span data-stu-id="9f16b-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="9f16b-126">Duplikerede kunder kan ikke flettes med kunder, der er knyttet til bekræftede projektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="9f16b-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="9f16b-127">Når en ressource, der ikke har en gyldig kalender, er tilføjet, returnerer systemet ikke en brugervenlig fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="9f16b-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="9f16b-128">Knappen **Tilføj opgave** i opgavegitteret aktiveres, når projektet sammenkædes med et **Microsoft Project-tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="9f16b-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="9f16b-129">Indsatsen stiger ukontrollerbart, når en opgave med en kategori tildeles en ressource, som har en angivet kostpris.</span><span class="sxs-lookup"><span data-stu-id="9f16b-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="9f16b-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9f16b-130">**Sales**</span></span>

<span data-ttu-id="9f16b-131">Der er blevet foretaget følgende forbedringer:</span><span class="sxs-lookup"><span data-stu-id="9f16b-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="9f16b-132">**Fakturafrekvens** og **Faktureringsstart** er blevet flyttet til fanen **Fakturaplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="9f16b-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="9f16b-133">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="9f16b-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="9f16b-134">**Den samlede salgspris** er nul (0) for **Kategorien** , også selvom **Rollen** har en samlet salgspris, der ikke er nul.</span><span class="sxs-lookup"><span data-stu-id="9f16b-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="9f16b-135">Kunderne kan ikke ændre værdien i feltet **Fakturastatus** til **Klar til fakturering** , når en anden tilpasset proces opdaterer et ekstra felt.</span><span class="sxs-lookup"><span data-stu-id="9f16b-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="9f16b-136">Knappen **Opdater fakturalinjer** kan oprette flere duplikerede linjer, hvis den er valgt flere gange.</span><span class="sxs-lookup"><span data-stu-id="9f16b-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="9f16b-137">Knappen **Opdater priser** virker ikke på undergitteret **Rollepriser** i formularen **Hurtig visning**.</span><span class="sxs-lookup"><span data-stu-id="9f16b-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="9f16b-138">Logikken **Løsningen til salgsprislisten** , håndterer ikke tidszoner korrekt, hvilket medfører et forkert udvalg af prislister.</span><span class="sxs-lookup"><span data-stu-id="9f16b-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="9f16b-139">Beløbet for et projekts **Samlede faktiske omkostninger** kan fravige med en brøkdel, når en enkelt post er godkendt.</span><span class="sxs-lookup"><span data-stu-id="9f16b-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="9f16b-140">Logikken **Prisløsning** indeholder ikke en brugervenlig fejlmeddelelse, hvis den **Hentede Rollepris** ikke indeholder værdier i felterne **"Primær enhed"** og **"Pris i primær enhed"**.</span><span class="sxs-lookup"><span data-stu-id="9f16b-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>