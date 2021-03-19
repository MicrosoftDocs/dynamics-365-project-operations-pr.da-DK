---
title: Opret og anvend betingelser for tilbageholdelse af leverandørbetaling
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer og vedligeholder tilbageholdelsesbetingelser for leverandørbetalinger.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270941"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="b4c92-103">Opret og anvend betingelser for tilbageholdelse af leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="b4c92-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="b4c92-104">Konfiguration af betingelser for tilbageholdelse af leverandørbetalinger for et projekt er nyttig, når organisationen ønsker at tilbageholde en del af de betalinger, der foretages til en leverandør.</span><span class="sxs-lookup"><span data-stu-id="b4c92-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="b4c92-105">Det kan f.eks. være, hvis du vil have tilbageholde betalingen til en leverandør, indtil de leverede produkter opfylder dine forventninger.</span><span class="sxs-lookup"><span data-stu-id="b4c92-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="b4c92-106">Du kan angive betingelser for tilbageholdelse af leverandørbetalinger, når du forhandler en leverandørkontrakt.</span><span class="sxs-lookup"><span data-stu-id="b4c92-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="b4c92-107">Opret betingelser for tilbageholdelse af leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="b4c92-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="b4c92-108">Du kan angive procentdelen af leverandørbetalingen, som skal tilbageholdes, og den procentdel af tidligere tilbageholdte beløb, der skal frigives.</span><span class="sxs-lookup"><span data-stu-id="b4c92-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="b4c92-109">Der tilbageholdes automatisk beløb for leverandørfakturaer, indtil kontrakten når den angivne afslutningstilstand.</span><span class="sxs-lookup"><span data-stu-id="b4c92-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="b4c92-110">Når du har konfigureret betingelserne for tilbageholdelse, kan du anvende dem på alle projekter for den pågældende leverandør.</span><span class="sxs-lookup"><span data-stu-id="b4c92-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="b4c92-111">Benyt følgende fremgangsmåde for at konfigurere og vedligeholde tilbageholdelsesbetingelser for leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="b4c92-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="b4c92-112">Gå til **Projektstyring og regnskab** > **Tilbageholdelse** > **Betingelser for tilbageholdelse af leverandørbetaling**.</span><span class="sxs-lookup"><span data-stu-id="b4c92-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="b4c92-113">Vælg **Ny** for at tilføje en ny betingelse for tilbageholdelse af leverandørbetaling.</span><span class="sxs-lookup"><span data-stu-id="b4c92-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="b4c92-114">Værdien **Regel-id** for den nye betingelse angives automatisk.</span><span class="sxs-lookup"><span data-stu-id="b4c92-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="b4c92-115">Angiv en kort beskrivelse i feltet **Beskrivelse**, og i oversigtspanelet **Betingelser** skal du vælge **Tilføj linje** for at angive betingelsesværdier for følgende:</span><span class="sxs-lookup"><span data-stu-id="b4c92-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="b4c92-116">**Procentdel af leverede enheder**: Angiv en færdiggørelsesprocent for betingelsen.</span><span class="sxs-lookup"><span data-stu-id="b4c92-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="b4c92-117">Der tilbageholdes automatisk beløb for leverandørfakturaer, indtil projektets fuldførelsesfase svarer til den angivne procentdel.</span><span class="sxs-lookup"><span data-stu-id="b4c92-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="b4c92-118">Hvis du f.eks. angiver 50,00, bevares beløb, indtil projektet er 50 procent fuldført.</span><span class="sxs-lookup"><span data-stu-id="b4c92-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="b4c92-119">**Procentdel, der skal tilbageholdes**: Angiv en procentdel af beløbet på leverandørfakturaen, der skal tilbageholdes.</span><span class="sxs-lookup"><span data-stu-id="b4c92-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="b4c92-120">Hvis du f.eks. skriver 10,00, tilbageholdes 10 procent af beløbet på en leverandørfaktura, indtil projektet når den i feltet **Procentdel af leverede enheder** angivne fuldførelsesgrad.</span><span class="sxs-lookup"><span data-stu-id="b4c92-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="b4c92-121">**Procentdel, der skal frigives**: Vælg **Tilføj linje** for at angive en procentdel af alle tidligere tilbageholdte beløb, der skal frigives for det valgte niveau for projektets færdiggørelse.</span><span class="sxs-lookup"><span data-stu-id="b4c92-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="b4c92-122">Hvis du har mere end én milepæl for forskellige niveauer af projektets færdiggørelse, skal du angive en separat betingelseslinje for tilbageholdelse af leverandørbetaling for hver tilbageholdelsesregel.</span><span class="sxs-lookup"><span data-stu-id="b4c92-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="b4c92-123">Hver linje kan angive en anden tilbageholdelsesprocent og en anden frigivelsesprocent for hvert enkelt angivet niveau af projektets fuldførelse.</span><span class="sxs-lookup"><span data-stu-id="b4c92-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="b4c92-124">Når du har oprettet betingelserne for tilbageholdelse af leverandørbetaling for en leverandør, kan du anvende betingelserne på et projekt.</span><span class="sxs-lookup"><span data-stu-id="b4c92-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="b4c92-125">Anvend betingelser for tilbageholdelse af leverandørbetaling på et projekt</span><span class="sxs-lookup"><span data-stu-id="b4c92-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="b4c92-126">Gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter**, og åbn et projekt på projektlistesiden.</span><span class="sxs-lookup"><span data-stu-id="b4c92-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="b4c92-127">I oversigtspanelet **Leverandøraftaler** skal du vælge **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="b4c92-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="b4c92-128">I **Kontokodefelt** skal du vælge en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="b4c92-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="b4c92-129">**Tabel**: Betingelser for tilbageholdelse af leverandørbetaling gælder for en enkelt leverandør.</span><span class="sxs-lookup"><span data-stu-id="b4c92-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="b4c92-130">**Gruppe**: Betingelserne for tilbageholde af leverandørbetaling gælder for alle leverandører i en leverandørgruppe.</span><span class="sxs-lookup"><span data-stu-id="b4c92-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="b4c92-131">**Alle**: Betingelser for tilbageholdelse af leverandørbetaling gælder for alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="b4c92-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="b4c92-132">I **feltet Leverandør/Leverandørgruppe** skal du vælge den leverandør eller leverandørgruppe, som betingelserne for tilbageholdelse af leverandørbetaling gælder for.</span><span class="sxs-lookup"><span data-stu-id="b4c92-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="b4c92-133">Hvis du har valgt **Alle** i det foregående trin, er dette felt ikke tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="b4c92-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="b4c92-134">I feltet **Betingelser for tilbageholdelse af leverandørbetaling** skal du vælge de tilbageholdelsesbetingelser, som du oprettede i forrige procedure.</span><span class="sxs-lookup"><span data-stu-id="b4c92-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="b4c92-135">Hvis projektet også har betingelserne betal ved betaling (PWP) konfigureret for leverandøren, skal du angive tærskelprocenten for projektet i feltet **Tærskelprocent for betal ved betaling**.</span><span class="sxs-lookup"><span data-stu-id="b4c92-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="b4c92-136">Betingelserne for tilbageholdelse af leverandørbetaling vises også på de indkøbsordrer, du opretter for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="b4c92-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]