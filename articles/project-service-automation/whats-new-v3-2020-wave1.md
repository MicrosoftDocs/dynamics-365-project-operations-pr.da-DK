---
title: Nyheder eller ændringer i Project Service Automation version 3.x, bølge 1 2020
description: Dette emne indeholder oplysninger om nyheder og ændringer i Project Service Automation version 3, bølge 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750540"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="25529-103">Nyheder eller ændringer i Project Service Automation version 3, bølge 1 2020</span><span class="sxs-lookup"><span data-stu-id="25529-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="25529-104">Dette emne fremhæver centrale overvejelser i forbindelse med opgraderinger, når du flytter over til den nyeste version af Project Service Automation (PSA) version 3.x, bølge 1 2020.</span><span class="sxs-lookup"><span data-stu-id="25529-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="25529-105">Tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="25529-105">Time entry</span></span>
<span data-ttu-id="25529-106">Tidsregistreringsoplevelsen er blevet udvidet med henblik på at levere funktioner til udvidelse af tidsregistrering i flere kundescenarier.</span><span class="sxs-lookup"><span data-stu-id="25529-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="25529-107">Dette omfatter muligheden for at tilføje posttyper, som nu er drivkraften bag en specifik adfærd, som er baseret på skemanavnsfeltet **Indstillinger for tidsregistrering**, der vises som **Tidskilde**.</span><span class="sxs-lookup"><span data-stu-id="25529-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="25529-108">Overvejelse i forbindelse med opgradering</span><span class="sxs-lookup"><span data-stu-id="25529-108">Upgrade consideration</span></span>
<span data-ttu-id="25529-109">Med henblik på at yde support for denne funktion er rollerne i PSA blevet opdateret, så de indeholder nye rettigheder.</span><span class="sxs-lookup"><span data-stu-id="25529-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="25529-110">Disse rettigheder giver læseadgang til det nye objekt **Indstillinger for tidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="25529-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="25529-111">Brugere, der har behov for at kunne logge tid, bør tildeles brugerrollen **Tidsregistreringsbruger** som supplement til eksisterende roller.</span><span class="sxs-lookup"><span data-stu-id="25529-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="25529-112">Denne rolle inkluderer den nye funktionalitet og sikrer, at tidsregistreringerne fortsat fungerer.</span><span class="sxs-lookup"><span data-stu-id="25529-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="25529-113">Aktuelle ændringer i udvidet tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="25529-113">Currently extended time entry changes</span></span>
<span data-ttu-id="25529-114">Hvis du vil minimere virkningen for aktuelle brugere af tidsregistreringen, er denne rolleændring det eneste kernekrav, der er nødvendigt for at fortsætte med at bruge tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="25529-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="25529-115">Hvis du har oprettet brugerdefinerede visninger eller separate tidsregistreringsoplevelser, skal du i felterne **Indstillinger for tidsregistrering** angive de korrekte PSA-værdier.</span><span class="sxs-lookup"><span data-stu-id="25529-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
