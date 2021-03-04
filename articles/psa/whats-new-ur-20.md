---
title: Nyheder eller ændringer i opdateringsudgivelse 20, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige i opdateringsudgivelse 20 til Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147106"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="1e6ee-103">Opdateringsudgivelse 20 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="1e6ee-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1e6ee-104">Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1e6ee-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1e6ee-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1e6ee-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1e6ee-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1e6ee-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1e6ee-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 20. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="1e6ee-110">Denne version har buildnummer V 3.10.31.37 og er generelt tilgængelig via en opdatering, du selv har udført i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="1e6ee-111">20. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="1e6ee-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1e6ee-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="1e6ee-112">Bug fixes</span></span>

<span data-ttu-id="1e6ee-113">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="1e6ee-113">**Project Management**</span></span>

<span data-ttu-id="1e6ee-114">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="1e6ee-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1e6ee-115">Import af projektgruppemedlemmer med en fordelingsmetode, der kræver timer, resulterer i en utydelig fejlmeddelelse, når de angivne timer er nul.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="1e6ee-116">Brugerne får vist en fejlmeddelelse om, at der er indsat et maksimum antal tegn i feltet **Beskrivelse** for en projektopgave.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="1e6ee-117">Siden **overførsel af tilføjelsesprogram til Microsoft Dynamics 365 Project Service Automation** omdirigerer til den engelske overførelsesside, når brugerens sprogindstillinger er angivet til japansk.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="1e6ee-118">Når der opstår en serverfejl, beholdes synkroniseringsnavnet på fanen **Planlægning** i formularen **Projekter** til tider.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="1e6ee-119">Overflødige opgaveopdateringer sendes til serveren, når en opgave ændres.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="1e6ee-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1e6ee-120">**Sales**</span></span>

<span data-ttu-id="1e6ee-121">Følgende problemer er blevet løst:</span><span class="sxs-lookup"><span data-stu-id="1e6ee-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="1e6ee-122">På formularen **Kontrakt** bliver der ved at dobbeltklikke på **Opret faktura** oprettet to fakturaer for værdierne af en enkelt post.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="1e6ee-123">I Internet Explorer 11 kan brugere ikke oprette udgiftsposter.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="1e6ee-124">Tilbageførsel af omkostning og tilbageførsel af faktiske værdier for ikke-fakturerede salg er ikke koblet sammen.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="1e6ee-125">Knappen **Opdater de faktiske værdier** i formularen **Projekter** opdaterer ikke **Projektets faktiske timer**.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="1e6ee-126">Plug-in'et **PreValidateProjectTeamMemberCreate** kan oprette duplikerede, generiske reserverbare ressourcer, når attributten **msdyn_isgenericresourceprojectscoped** er angivet til **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="1e6ee-127">**Genberegn** rydder de fakturerbare omkostninger i detaljerne for produktbaserede tilbudslinjer og kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="1e6ee-128">I specifikke scenarier viser plug-in-et **PostEstimateLineUpdate** en undtagelsesfejl i null-reference.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="1e6ee-129">Varighed af tidsfasen i **Rentabilitetsanalysediagrammet** stemmer ikke overens med varigheden for omkostningerne i detaljerne for tilbudslinjerne for fastpris i tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="1e6ee-130">Enheds- og enhedsgruppeværdier nulstilles ikke korrekt for udgiftskategorier i formularerne **Detaljer om kontraktlinje** og **Detaljer om tilbudslinje**.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="1e6ee-131">Listerne **Org enhedskostpris** tillader overlapninger i datoeffektiviteten.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="1e6ee-132">Brugere har ikke tilladelse til at ændre **OrgUnit**, når ordretypen ikke er arbejdsbaseret, fordi den vil resultere i en undtagelsesfejl i null-referencen.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="1e6ee-133">Når du forsøger at navigere fra formularen **Detaljer om tilbudslinjen** tilbage til fanen **Tilbud**, opdateres formularen, og fanen **Oversigt** vises.</span><span class="sxs-lookup"><span data-stu-id="1e6ee-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
