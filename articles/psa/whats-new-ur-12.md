---
title: Nyheder eller ændringer i opdateringsudgivelse 12, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 12. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f29eaf7c471104ad3e319d8f4e1cbc70e44fc1ca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000339"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="4cbfa-103">Opdateringsudgivelse 12 til Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="4cbfa-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4cbfa-104">Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="4cbfa-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="4cbfa-105">Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4cbfa-106">Denne version er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4cbfa-107">Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="4cbfa-108">Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4cbfa-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4cbfa-109">I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 12. opdateringsudgivelse.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="4cbfa-110">Denne version har build-nummer V3.10.2.34 og er generelt tilgængelig via en opdatering, du selv skal foretage, i oktober 2019.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="4cbfa-111">12. opdateringsudgivelse</span><span class="sxs-lookup"><span data-stu-id="4cbfa-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4cbfa-112">Fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="4cbfa-112">Bug fixes</span></span>

- <span data-ttu-id="4cbfa-113">Tid og udgift</span><span class="sxs-lookup"><span data-stu-id="4cbfa-113">Time and Expense</span></span>

    - <span data-ttu-id="4cbfa-114">Løst: Fejlmeddelelser for tidsregistrering er blevet opdateret med mere relevant kontekst.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="4cbfa-115">Løst: Tidsregistreringsgitter og -planlægning viser det lodrette rullepanel korrekt, når det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="4cbfa-116">Løst: Sendte udgifter og tidsregistreringer kan godkendes.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="4cbfa-117">Løst: Dialogmeddelelsen for bekræftelse af annullering af godkendelse er blevet rettet, så den nu afspejler statussen for godkendelsen, når den ændres fra **Godkendt** til **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="4cbfa-118">Løst: Felterne **Pris**, **Enhed** og **Antal** låses nu på udgiftsposten, når den er godkendt.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="4cbfa-119">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="4cbfa-119">Project Management</span></span>

    - <span data-ttu-id="4cbfa-120">Løst: Handlingen **Nye** på hovedformularen **Teammedlem** er blevet fjernet.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="4cbfa-121">Løst: Ressourcetildelinger er blevet opdateret til at redegøre for unøjagtige afrundingsfejl, som har medført et skifte i en opgaves slutdato.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="4cbfa-122">Løst: I opgavegitteret vises de relevante fejl på serversiden.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="4cbfa-123">Løst: Gruppemedlemmets navn gengives nu i opgavepersonvælgeren i stedet for stillingsnavnet.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="4cbfa-124">Ressourcestyring</span><span class="sxs-lookup"><span data-stu-id="4cbfa-124">Resource Management</span></span>

    - <span data-ttu-id="4cbfa-125">Løst: Oplysninger om ressourcekrav for projekter, der er oprettet ud fra en skabelon, anvender nu projektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="4cbfa-126">Løst: Færdigheder og kompetencer er nu som standard baseret på det ressourcekrav, der blev oprettet for den pågældende rolle, frem for på rollemasterdata.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="4cbfa-127">Sales</span><span class="sxs-lookup"><span data-stu-id="4cbfa-127">Sales</span></span>

    - <span data-ttu-id="4cbfa-128">Løst: Der findes identiske objekt-ID'er i formularen **Hovedkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="4cbfa-129">Løst: Logikken er blevet opdateret for at gøre fanen **Tilbudsanalyse** synlig, så den viser metadataopsætningen for fanen.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="4cbfa-130">Løst: Regnskabsdatoen på den faktiske post kommer nu fra datoen for registrering af tid/udgifter og ikke fra datoen for godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="4cbfa-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]