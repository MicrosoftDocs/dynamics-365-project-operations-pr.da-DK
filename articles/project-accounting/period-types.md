---
title: Periodetyper
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere periodetyper for omsætningsestimeringer.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287276"
---
# <a name="period-types"></a><span data-ttu-id="78269-103">Periodetyper</span><span class="sxs-lookup"><span data-stu-id="78269-103">Period types</span></span>

<span data-ttu-id="78269-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="78269-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="78269-105">En periodetype definerer, hvor ofte omsætningen på et projekt estimeres.</span><span class="sxs-lookup"><span data-stu-id="78269-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="78269-106">Dette emne indeholder oplysninger om, hvordan du kan konfigurere periodetyper for omsætningsestimeringer.</span><span class="sxs-lookup"><span data-stu-id="78269-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="78269-107">Opret og arbejd med periodetyper</span><span class="sxs-lookup"><span data-stu-id="78269-107">Create and work with period types</span></span>
<span data-ttu-id="78269-108">Hvis du vil oprette og arbejde med periodetyper, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="78269-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="78269-109">I dit Dynamics 365 Finance-miljø skal du gå til **Projektstyring og regnskab** > **Opsætning** > **Estimater** > **Periodetyper**.</span><span class="sxs-lookup"><span data-stu-id="78269-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="78269-110">Vælg **Ny** for at oprette nye periodetyper.</span><span class="sxs-lookup"><span data-stu-id="78269-110">Select **New** to create new period type.</span></span> <span data-ttu-id="78269-111">Angiv et navn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="78269-111">Enter a name and description.</span></span>
3. <span data-ttu-id="78269-112">Vælg en værdi i feltet **Hyppighed**:</span><span class="sxs-lookup"><span data-stu-id="78269-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="78269-113">Hvis du vælger **Uge**, **Halvugelig**, **Halvmånedlig**, **Måned**, **Dag**, **Kvartal** eller **År**, bruges kalenderen til at oprette perioderne.</span><span class="sxs-lookup"><span data-stu-id="78269-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="78269-114">Hvis du vælger **Finansperiode**, bruges regnskabsperioder fra konfigurationen af finanskladden til at oprette perioder.</span><span class="sxs-lookup"><span data-stu-id="78269-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="78269-115">Hvis du vælger **Ubegrænset**, kan du angive brugerdefinerede perioder.</span><span class="sxs-lookup"><span data-stu-id="78269-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="78269-116">Vælg periodetypeposten, og vælg derefter **Opret perioder** for at oprette perioder til periodetypen.</span><span class="sxs-lookup"><span data-stu-id="78269-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="78269-117">Afhængigt af den periodefrekvens, du har valgt, har du måske mulighed for at angive en startdato eller det antal perioder, der skal genereres.</span><span class="sxs-lookup"><span data-stu-id="78269-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="78269-118">Vælg **Perioder** for at gennemse genererede perioder.</span><span class="sxs-lookup"><span data-stu-id="78269-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]