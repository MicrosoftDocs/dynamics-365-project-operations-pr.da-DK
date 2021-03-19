---
title: Projekttilskud
description: I dette emne forklares det, hvordan du kan oprette eller redigere et tilskud.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289362"
---
# <a name="project-grants"></a><span data-ttu-id="ab661-103">Projekttilskud</span><span class="sxs-lookup"><span data-stu-id="ab661-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab661-104">Et tilskud er en pengegave til et bestemt formål eller projekt.</span><span class="sxs-lookup"><span data-stu-id="ab661-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="ab661-105">Som regel er der begrænsninger på, hvordan et tilskud kan bruges.</span><span class="sxs-lookup"><span data-stu-id="ab661-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="ab661-106">I Projektstyring og regnskab kan du angive og spore tilskud og definere deres relationer til projekter og projektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="ab661-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="ab661-107">Du kan f.eks. udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="ab661-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="ab661-108">Tilknyt tilskud til projekter og finansieringskilder via links til siderne **Projekt** og **Projektkontraktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="ab661-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="ab661-109">Du kan angive og spore ændringer i et tilskud, når det flyttes fra én status til en anden.</span><span class="sxs-lookup"><span data-stu-id="ab661-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="ab661-110">Angiv og spor omkostninger, anmodede beløb og tildelte beløb.</span><span class="sxs-lookup"><span data-stu-id="ab661-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="ab661-111">Opret overordnede tilskud, og knyt dem sammen med underordnede tilskud.</span><span class="sxs-lookup"><span data-stu-id="ab661-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="ab661-112">Du kan oprette et tilskud ved at angive samtlige detaljer i en ny post, eller du kan kopiere oplysningerne fra et eksisterende tilskud og derefter opdatere dem.</span><span class="sxs-lookup"><span data-stu-id="ab661-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="ab661-113">Opret et nyt tilskud</span><span class="sxs-lookup"><span data-stu-id="ab661-113">Create a new grant</span></span>

1. <span data-ttu-id="ab661-114">Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.</span><span class="sxs-lookup"><span data-stu-id="ab661-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="ab661-115">Vælg **Nyt** \> **Tilskud**.</span><span class="sxs-lookup"><span data-stu-id="ab661-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="ab661-116">På siden med tilskudsoplysninger skal du i oversigtspanelet **Generelt** i feltet **Tilskuds-id** angive et alfanumerisk id for tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="ab661-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="ab661-117">Angiv et navn for tilskuddet i feltet **Tilskudsnavn**.</span><span class="sxs-lookup"><span data-stu-id="ab661-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="ab661-118">I feltet **Beskrivelse** kan du tilføje oplysninger det nye tilskud.</span><span class="sxs-lookup"><span data-stu-id="ab661-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="ab661-119">De fleste af de andre felter på siden er valgfrie, og du kan angive så få eller mange oplysninger, som du vil.</span><span class="sxs-lookup"><span data-stu-id="ab661-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="ab661-120">På følgende liste beskrives de oplysninger, der er angivet i hvert oversigtspanel på siden med tilskudsoplysninger:</span><span class="sxs-lookup"><span data-stu-id="ab661-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="ab661-121">**Generelt** – Angiv tilskuddets navn, status, beskrivelse, formål og beløb.</span><span class="sxs-lookup"><span data-stu-id="ab661-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="ab661-122">t **Kontaktoplysninger** – Angiv oplysninger om medarbejdere, den afdeling, der administrerer tilskuddet, samt tilskudskunden eller organisationens tilskudskilde.</span><span class="sxs-lookup"><span data-stu-id="ab661-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="ab661-123">Du kan også angive, om organisationen er et gennemgående objekt, der modtager tilskuddet og derefter overfører det til en anden modtager.</span><span class="sxs-lookup"><span data-stu-id="ab661-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="ab661-124">Vælg **Tilføj** for at tilføje kontaktoplysninger, f.eks. telefonnumre og e-mail-adresser på den organisation, der yder tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="ab661-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="ab661-125">**Datoer og frister** – Angiv datoer, der er relateret til tilskuddet og tilskudsansøgningen.</span><span class="sxs-lookup"><span data-stu-id="ab661-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="ab661-126">Som eksempel kan nævnes datoen for ansøgningsfristen, indsendelsesdatoen og den dato, hvor tilskuddet er blevet godkendt eller afvist.</span><span class="sxs-lookup"><span data-stu-id="ab661-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="ab661-127">**Tilknyttede projekter og projektkontrakter** – Du kan kun angive oplysninger i dette oversigtspanel, hvis feltet **Tilskudsstatus** i oversigtspanelet **Generelt** er angivet til **Aktiv** eller **Tildelt**.</span><span class="sxs-lookup"><span data-stu-id="ab661-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="ab661-128">Vælg mellem følgende indstillinger for at fuldføre den relaterede opgave:</span><span class="sxs-lookup"><span data-stu-id="ab661-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="ab661-129">**Tilføj finansieringskilde** – Tilføj en ny finansieringskilde for tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="ab661-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="ab661-130">Du kan angive samtlige detaljer nu, eller du kan bruge standardoplysninger og derefter opdatere dem senere.</span><span class="sxs-lookup"><span data-stu-id="ab661-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="ab661-131">**Tilføj projektkontrakt** – Tilføj eller opdater projektkontraktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="ab661-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="ab661-132">**Tilføj projekt** – Tilføj eller opdater projektdetaljer.</span><span class="sxs-lookup"><span data-stu-id="ab661-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="ab661-133">**Opsætning** – Angiv detaljer om tilsvarende midler, hvis disse oplysninger er nødvendige.</span><span class="sxs-lookup"><span data-stu-id="ab661-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="ab661-134">Mange organisationer, der tildeler tilskud, kræver, at modtagerne bruger et bestemt beløb af deres egne penge eller ressourcer, så de svarer til det beløb, der tildeles i tilskuddet.</span><span class="sxs-lookup"><span data-stu-id="ab661-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="ab661-135">I feltet **Lokalt projekt eller sporings-id** kan du angive et id, der adskiller sig fra projekt-id'et.</span><span class="sxs-lookup"><span data-stu-id="ab661-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ab661-136">Hvis en del af tilskuddet skal tildeles til en anden organisation, skal du angive indstillingen **Underordnet tilskudsmodtager** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ab661-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="ab661-137">I forbindelse med tilskud, der tildeles i USA, kan du angive, om et tilskud skal tildeles under et statsligt mandat eller et føderal mandat.</span><span class="sxs-lookup"><span data-stu-id="ab661-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="ab661-138">**Trækningsdetaljer** – Tilføj eller opdater oplysninger om, hvor ofte tilskudsmidlerne kan trækkes ud, faktureres eller bruges.</span><span class="sxs-lookup"><span data-stu-id="ab661-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="ab661-139">Opret et nyt tilskud fra en kopi</span><span class="sxs-lookup"><span data-stu-id="ab661-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="ab661-140">Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.</span><span class="sxs-lookup"><span data-stu-id="ab661-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="ab661-141">Vælg **Ny** \> **Kopier fra tilskud**.</span><span class="sxs-lookup"><span data-stu-id="ab661-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="ab661-142">Angiv et alfanumerisk id og et navn for det nye tilskud, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab661-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="ab661-143">Gennemse oplysningerne om det kopierede tilskud på siden med tilskudsoplysninger, og foretag eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="ab661-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="ab661-144">De fleste felter på siden er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="ab661-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="ab661-145">Få vist eller rediger oplysninger om tilskuddet</span><span class="sxs-lookup"><span data-stu-id="ab661-145">View or modify grant details</span></span>

1. <span data-ttu-id="ab661-146">Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.</span><span class="sxs-lookup"><span data-stu-id="ab661-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="ab661-147">Vælg det tilskud, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="ab661-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="ab661-148">I handlingsruden skal du på fanen **Tilskud** i gruppen **Bevar** vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ab661-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="ab661-149">Gennemse tilskudsoplysningerne, og foretag eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="ab661-149">Review the grant details, and make any changes that are required.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]