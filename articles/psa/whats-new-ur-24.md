---
title: Nyheder eller ændringer i opdateringsudgivelse 24, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280481"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="470e8-103">Opdateringsudgivelse 24 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="470e8-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="470e8-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="470e8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="470e8-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="470e8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="470e8-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="470e8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="470e8-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="470e8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="470e8-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="470e8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="470e8-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 24. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="470e8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="470e8-110">Denne version har build-nummer V 3.10.42.43 og er generelt tilgængelig via en opdatering, som du selv skal foretage, i oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="470e8-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="470e8-111">24. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="470e8-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="470e8-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="470e8-112">Bug fixes</span></span>

<span data-ttu-id="470e8-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="470e8-113">**Sales**</span></span>

<span data-ttu-id="470e8-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="470e8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="470e8-115">Der opstod en fejl under angivelse af standardprislisten for produkter.</span><span class="sxs-lookup"><span data-stu-id="470e8-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="470e8-116">Tilbuddets ydeevne som vundet er langsom på grund af kopien af posterne for den integrerede prisliste og rollepriser.</span><span class="sxs-lookup"><span data-stu-id="470e8-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="470e8-117">**Projektkontrakt/Salgshub** > **Produktlinjeelement/Ordrelinjemængde** afrundes automatisk til nærmeste heltal.</span><span class="sxs-lookup"><span data-stu-id="470e8-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="470e8-118">Opløft til systemrettigheder, når du læser prislister.</span><span class="sxs-lookup"><span data-stu-id="470e8-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="470e8-119">Kopier kundens adressefelter **address1_freighttermscode** og **address1_shippingmethodcode** til Tilbud/Ordre.</span><span class="sxs-lookup"><span data-stu-id="470e8-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="470e8-120">**Tid og udgift**</span><span class="sxs-lookup"><span data-stu-id="470e8-120">**Time and Expense**</span></span>

<span data-ttu-id="470e8-121">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="470e8-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="470e8-122">**Gitteret for tidsregistrering** understøtter ikke funktionsmåden for **Kun dato**.</span><span class="sxs-lookup"><span data-stu-id="470e8-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="470e8-123">**Tidsregistrering** opdateres ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="470e8-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="470e8-124">Der skal bruges manuel opdatering.</span><span class="sxs-lookup"><span data-stu-id="470e8-124">A manual refresh is required.</span></span>
- <span data-ttu-id="470e8-125">Det er ikke muligt at importere tidsregistreringer fra en tildeling, når der er en pause (0 timer) i en ressources tildelinger.</span><span class="sxs-lookup"><span data-stu-id="470e8-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="470e8-126">Når du opretter en tidsregistrering, skal du angive starttidspunktet til det samme som **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="470e8-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="470e8-127">Aktivér masseredigering for tidsregistrering igen.</span><span class="sxs-lookup"><span data-stu-id="470e8-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="470e8-128">**Ressourcestyring**</span><span class="sxs-lookup"><span data-stu-id="470e8-128">**Resource Management**</span></span>

<span data-ttu-id="470e8-129">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="470e8-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="470e8-130">Hvis du forsøger at opdatere statussen for en intern dagsreservation uden et krav, udløses en null-ref-undtagelse.</span><span class="sxs-lookup"><span data-stu-id="470e8-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="470e8-131">Fejl under indlæsning af **Afstemningsvisningen**.</span><span class="sxs-lookup"><span data-stu-id="470e8-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="470e8-132">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="470e8-132">**Project Management**</span></span>

<span data-ttu-id="470e8-133">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="470e8-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="470e8-134">Automatisk lagring i **Projektplanlægning** kan ikke gennemføres, når man skifter fra **Manuel** til **Automatisk**.</span><span class="sxs-lookup"><span data-stu-id="470e8-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="470e8-135">Udgiftsomkostninger skal ikke beregnes i forhold til variansen i **Projektsporingsgitteret**.</span><span class="sxs-lookup"><span data-stu-id="470e8-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="470e8-136">Uoverensstemmende funktionsmåde for kolonnerne **Estimerer mærker** under indlæsningen i forhold til ændring af typen **Tidsfase**.</span><span class="sxs-lookup"><span data-stu-id="470e8-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="470e8-137">De faktiske omkostninger på et projekt afspejler muligvis ikke totalerne fra de **Faktiske værdier**.</span><span class="sxs-lookup"><span data-stu-id="470e8-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="470e8-138">**Den anslåede slutdato** under fanen **Oversigt** stemmer ikke overens med **WBS-planen**.</span><span class="sxs-lookup"><span data-stu-id="470e8-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="470e8-139">**Opdater faktiske timer** på udrykning fungerer ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="470e8-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="470e8-140">En projektleder uden for **BU**-roden kan ikke oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="470e8-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="470e8-141">Ændringer af opgave eller kategori i **Udgiftsestimater** bevares ikke.</span><span class="sxs-lookup"><span data-stu-id="470e8-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="470e8-142">**Kopi af kontrakt** kopierer fakturaplanerne og kørselsstatus.</span><span class="sxs-lookup"><span data-stu-id="470e8-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="470e8-143">Knappen **Opdater faktiske oplysninger** beregner hovedopgaver ukorrekt.</span><span class="sxs-lookup"><span data-stu-id="470e8-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="470e8-144">Tilføjelsesprogram til Microsoft Project: ret en fejl i null-reference, hvis et teammedlem har en tom ressourceenhed.</span><span class="sxs-lookup"><span data-stu-id="470e8-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]