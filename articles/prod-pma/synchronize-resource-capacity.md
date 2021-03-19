---
title: Synkroniser ressourcekapacitet
description: Dette emne indeholder oplysninger om, hvordan du synkroniserer en ressources kapacitet på tværs af kalendere og projekter.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288552"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="25b08-103">Synkroniser ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="25b08-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25b08-104">Processerne for ressourcesynkronisering er med til at sikre, at oplysninger til kalenderen og basiskalenderen når frem til projektets ressourceplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="25b08-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="25b08-105">Hvis kalenderen ændres, foretager processerne de påkrævede opdateringer i planlægningen af projektressourcer.</span><span class="sxs-lookup"><span data-stu-id="25b08-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="25b08-106">Processerne er også med til at forbedre ydeevnen, da kalenderens ressourceoplysninger er blevet synkroniseret på forhånd.</span><span class="sxs-lookup"><span data-stu-id="25b08-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="25b08-107">Opdateringer af oplysninger om ressourceplanlægning sker derfor hurtigere.</span><span class="sxs-lookup"><span data-stu-id="25b08-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="25b08-108">Det anbefales, at du planlægger processerne som et batch i stedet for en ad gangen.</span><span class="sxs-lookup"><span data-stu-id="25b08-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="25b08-109">I modsat fald er der risiko for, at en bruger glemmer de inkluderede datoer, da oplysningerne sidst blev synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="25b08-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="25b08-110">Hvis der ikke bruges inkluderede datoer, kan der opstå huller under datosynkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="25b08-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synkronisering af kalendere](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="25b08-112">Synkronisering af akkumulering af ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="25b08-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="25b08-113">Synkroniseringsprocessen er tiltænkt at skulle synkronisere alle ressourcekalenderoplysninger.</span><span class="sxs-lookup"><span data-stu-id="25b08-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="25b08-114">Disse oplysninger inkluderer basiskalenderoplysninger om eventuelle ændringer af tabellen for projektets ressourcekalenderkapacitet.</span><span class="sxs-lookup"><span data-stu-id="25b08-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="25b08-115">Hvis der tilføjes nye ressourcer i projektet, kan synkroniseringen hjælpe dig med at sikre, at de opdaterede kalenderoplysninger er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="25b08-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="25b08-116">Denne synkronisering kan udføres på et hvilket som helst tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="25b08-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="25b08-117">Vi anbefaler, at du bruger en batch .</span><span class="sxs-lookup"><span data-stu-id="25b08-117">We recommend that you use a batch.</span></span> <span data-ttu-id="25b08-118">Indstillingerne er tilgængelige under synkronisering af kapacitetsreservationer.</span><span class="sxs-lookup"><span data-stu-id="25b08-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="25b08-119">Vælg **Projektstyring og regnskab** &gt; **Periodisk** &gt; **Kapacitetssynkronisering** &gt; **Synkroniser ressourcekapacitetsakkumuleringer**.</span><span class="sxs-lookup"><span data-stu-id="25b08-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="25b08-120">Angiv mulighederne i den følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="25b08-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="25b08-121">Indstilling</span><span class="sxs-lookup"><span data-stu-id="25b08-121">Option</span></span>      | <span data-ttu-id="25b08-122">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="25b08-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="25b08-123">Periodekode</span><span class="sxs-lookup"><span data-stu-id="25b08-123">Period code</span></span> | <span data-ttu-id="25b08-124">Du kan evt. vælge intervalkoden for finanskladden for at angive start- og slutdatoer for synkroniseringsprocessen for akkumulering af ressourcekapacitet.</span><span class="sxs-lookup"><span data-stu-id="25b08-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="25b08-125">Startdato</span><span class="sxs-lookup"><span data-stu-id="25b08-125">Start date</span></span>  | <span data-ttu-id="25b08-126">Angiv startdatoen for synkroniseringsprocessen for akkumuleringer af ressourcekapacitet.</span><span class="sxs-lookup"><span data-stu-id="25b08-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="25b08-127">Slutdato</span><span class="sxs-lookup"><span data-stu-id="25b08-127">End date</span></span>    | <span data-ttu-id="25b08-128">Angiv slutdatoen for synkroniseringsprocessen for akkumuleringer af ressourcekapacitet.</span><span class="sxs-lookup"><span data-stu-id="25b08-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="25b08-129">[![Synkroniseringsproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="25b08-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]