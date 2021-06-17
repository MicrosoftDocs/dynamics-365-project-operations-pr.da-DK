---
title: Oversigt over tidsforbrug for ressource
description: Dette emne indeholder oplysninger om ressourceforbrug i Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000789"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="79dc5-103">Oversigt over tidsforbrug for ressource</span><span class="sxs-lookup"><span data-stu-id="79dc5-103">Resource utilization overview</span></span>

<span data-ttu-id="79dc5-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="79dc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="79dc5-105">Ressourcer kan have et fakturerbart tidsforbrug for et mål.</span><span class="sxs-lookup"><span data-stu-id="79dc5-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="79dc5-106">Dette mål-tidsforbrug er defineret som en attribut i en ressources standardrolle eller angivet på posten for den individuelle, reserverbare ressource.</span><span class="sxs-lookup"><span data-stu-id="79dc5-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="79dc5-107">Beregningerne af tidsforbrug er baseret på det faktiske antal timer, som ressourcer har rapporteret ved hjælp af godkendte tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="79dc5-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="79dc5-108">Følgende formler bruges til at beregne forbrug:</span><span class="sxs-lookup"><span data-stu-id="79dc5-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="79dc5-109">Fakturerbart tidsforbrug = fakturerbare faktiske timer ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="79dc5-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="79dc5-110">Ikke-fakturerbar tidsforbrug = faktisk tid med faktureringstype-ID = ikke-fakturerbar, komplementær eller ikke tilgængelig ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="79dc5-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="79dc5-111">Intern = faktisk tid uden salgskontrakt ÷ ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="79dc5-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="79dc5-112">Ressourcekapacitet = ressourcens arbejdstimer – ikke til stede – fridage</span><span class="sxs-lookup"><span data-stu-id="79dc5-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="79dc5-113">Du kan finde visningen **Ressourceforbrug** i ruden **Ressourcer.**</span><span class="sxs-lookup"><span data-stu-id="79dc5-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="79dc5-114">Hver celle i gitteret repræsenterer den fakturerbare udnyttelsesprocent for ressourcen i en periode, f.eks. en dag, uge eller måned.</span><span class="sxs-lookup"><span data-stu-id="79dc5-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="79dc5-115">Følgende formler bruges til farvning af cellerne:</span><span class="sxs-lookup"><span data-stu-id="79dc5-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="79dc5-116">**Grøn**: Fakturerbart tidsforbrug > = ressourcens måltidsforbrug</span><span class="sxs-lookup"><span data-stu-id="79dc5-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="79dc5-117">**Gul**: Måltidsforbrug – 20 < = fakturerbart tidsforbrug < måltidsforbrug</span><span class="sxs-lookup"><span data-stu-id="79dc5-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="79dc5-118">**Rød**: Fakturerbart tidsforbrug < måltidsforbrug – 20</span><span class="sxs-lookup"><span data-stu-id="79dc5-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="79dc5-119">Da visningen **Ressourceforbrug** er baseret på planlægningsområdet, kan du bruge filtreringsfunktionerne i planlægningsområdet til at filtrere resultaterne.</span><span class="sxs-lookup"><span data-stu-id="79dc5-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="79dc5-120">Gitteret kræver, at du angiver et mål-tidsforbrug for enten rolle eller den enkelte ressource.</span><span class="sxs-lookup"><span data-stu-id="79dc5-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="79dc5-121">Du konfigurerer dette ved at gå til **Ressourcer** > **Ressourceroller**.</span><span class="sxs-lookup"><span data-stu-id="79dc5-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="79dc5-122">Derudover skal der tildeles en standardrolle til hver af de pågældende reserverbare ressourcer.</span><span class="sxs-lookup"><span data-stu-id="79dc5-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="79dc5-123">Gå til **Ressourcer** > **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="79dc5-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="79dc5-124">På fanen **Project Service** skal du kontrollere, at der er defineret en ressourcerolle, og at feltet **Er standard** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="79dc5-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="79dc5-125">Du kan tilføje flere roller, hvor **Er standard** = **Nej**.</span><span class="sxs-lookup"><span data-stu-id="79dc5-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="79dc5-126">Den rolle, hvor **Er standard** = **Ja**, bruges til at evaluere ressourcens tidsforbrug i forhold til destinationen for den pågældende rolle.</span><span class="sxs-lookup"><span data-stu-id="79dc5-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="79dc5-127">På fanen **Project Service** kan du også angive en individuel mål-tidsforbrug for ressourcen.</span><span class="sxs-lookup"><span data-stu-id="79dc5-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="79dc5-128">I beregningen af tidsforbruget bruger derefter denne mål-tidsforbrug til at evaluere ressourcens mål i stedet for målet for ressourcens standardrolle.</span><span class="sxs-lookup"><span data-stu-id="79dc5-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="79dc5-129">Tidsforbrug vises kun for en ressource, hvis den pågældende ressource har godkendt fakturerbar tid i løbet af den periode, der vises i gitteret.</span><span class="sxs-lookup"><span data-stu-id="79dc5-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]