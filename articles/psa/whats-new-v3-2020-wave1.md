---
title: Nyheder eller ændringer i Project Service Automation version 3.x, bølge 1 2020
description: Dette emne indeholder oplysninger om nyheder og ændringer i Project Service Automation version 3, bølge 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996829"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="547e1-103">Nyheder eller ændringer i Project Service Automation version 3, bølge 1 2020</span><span class="sxs-lookup"><span data-stu-id="547e1-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="547e1-104">Dette emne fremhæver centrale overvejelser i forbindelse med opgraderinger, når du flytter over til den nyeste version af Project Service Automation (PSA) version 3.x, bølge 1 2020.</span><span class="sxs-lookup"><span data-stu-id="547e1-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="547e1-105">Tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="547e1-105">Time entry</span></span>
<span data-ttu-id="547e1-106">Tidsregistreringsoplevelsen er blevet udvidet med henblik på at levere funktioner til udvidelse af tidsregistrering i flere kundescenarier.</span><span class="sxs-lookup"><span data-stu-id="547e1-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="547e1-107">Dette omfatter muligheden for at tilføje posttyper, som nu er drivkraften bag en specifik adfærd, som er baseret på skemanavnsfeltet **Indstillinger for tidsregistrering**, der vises som **Tidskilde**.</span><span class="sxs-lookup"><span data-stu-id="547e1-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="547e1-108">Der er tilføjet en ny løsning kaldet Tid, Udgift, Statusangivelse og Godkendelser (TESA) for at understøtte denne funktion.</span><span class="sxs-lookup"><span data-stu-id="547e1-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="547e1-109">Overvejelse i forbindelse med opgradering</span><span class="sxs-lookup"><span data-stu-id="547e1-109">Upgrade consideration</span></span>
<span data-ttu-id="547e1-110">Med henblik på at yde support for denne funktion er rollerne i PSA blevet opdateret, så de indeholder nye rettigheder.</span><span class="sxs-lookup"><span data-stu-id="547e1-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="547e1-111">Disse rettigheder giver læseadgang til det nye objekt **Indstillinger for tidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="547e1-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="547e1-112">Brugere, der har behov for at kunne logge tid, bør tildeles brugerrollen **Tidsregistreringsbruger** som supplement til eksisterende roller.</span><span class="sxs-lookup"><span data-stu-id="547e1-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="547e1-113">Denne rolle inkluderer den nye funktionalitet og sikrer, at tidsregistreringerne fortsat fungerer.</span><span class="sxs-lookup"><span data-stu-id="547e1-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="547e1-114">Hvis du har brugerdefinerede app-moduler, der omfatter alle formularer for objektet tidsangivelse, skal du også fjerne **Formularen til hurtig oprettelse af TESA-tidsangivelse** fra modulet.</span><span class="sxs-lookup"><span data-stu-id="547e1-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="547e1-115">Aktuelle ændringer i udvidet tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="547e1-115">Currently extended time entry changes</span></span>
<span data-ttu-id="547e1-116">Hvis du vil minimere virkningen for aktuelle brugere af tidsregistreringen, er denne rolleændring det eneste kernekrav, der er nødvendigt for at fortsætte med at bruge tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="547e1-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="547e1-117">Hvis du har oprettet brugerdefinerede visninger eller separate tidsregistreringsoplevelser, skal du i felterne **Indstillinger for tidsregistrering** angive de korrekte PSA-værdier.</span><span class="sxs-lookup"><span data-stu-id="547e1-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]