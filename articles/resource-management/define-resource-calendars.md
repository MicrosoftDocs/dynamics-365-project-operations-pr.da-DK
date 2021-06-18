---
title: Definere ressourcekalendere
description: Dette emne indeholder oplysninger om, hvordan du definerer arbejdstidskalendere for ressourcer i Project Operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5ac834e16afc2f559bee6e10434f7015e8a8e51f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012174"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="09b79-103">Definere ressourcekalendere</span><span class="sxs-lookup"><span data-stu-id="09b79-103">Define resource calendars</span></span>

<span data-ttu-id="09b79-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="09b79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09b79-105">Alle de reserverbare ressourcer, der arbejder på et projekt, skal have en kalender med arbejdstid for at definere deres tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="09b79-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="09b79-106">Arbejdstiderne for en ressource kan defineres på to måder:</span><span class="sxs-lookup"><span data-stu-id="09b79-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="09b79-107">Definer individuelle kalenderregler for en ressource</span><span class="sxs-lookup"><span data-stu-id="09b79-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="09b79-108">Anvend en eksisterende kalenderskabelon for ressourcen</span><span class="sxs-lookup"><span data-stu-id="09b79-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="09b79-109">Definer en ressources arbejdstid</span><span class="sxs-lookup"><span data-stu-id="09b79-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="09b79-110">I menuen **Ressourcer** skal du vælge **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="09b79-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="09b79-111">I gittervisningen skal du vælge en anvendelig **Reserverbar ressource** .</span><span class="sxs-lookup"><span data-stu-id="09b79-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="09b79-112">På siden **Ressourcedetaljer** skal du vælge fanen **Arbejdstid**. Som standard er den reserverbare ressourcekalender arbejdstiderne for den standardarbejdsugeskabelon, der er defineret for organisationen.</span><span class="sxs-lookup"><span data-stu-id="09b79-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="09b79-113">Hvis du vil opdatere arbejdstiderne, skal du højreklikke på startdatoen for den foreslåede kalenderregel, der skal defineres.</span><span class="sxs-lookup"><span data-stu-id="09b79-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="09b79-114">Brug menuen kalenderregler til at definere en kalenderregel for en bestemt dag, resten af serien eller hele kalenderen.</span><span class="sxs-lookup"><span data-stu-id="09b79-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="09b79-115">Når indstillingen er valgt, kan du definere følgende:</span><span class="sxs-lookup"><span data-stu-id="09b79-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="09b79-116">Den ugedag, hvor arbejdstiden træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="09b79-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="09b79-117">Arbejdstiderne inden for hver dag.</span><span class="sxs-lookup"><span data-stu-id="09b79-117">The working times within each day.</span></span>
    - <span data-ttu-id="09b79-118">Tidszonen for kalenderreglen.</span><span class="sxs-lookup"><span data-stu-id="09b79-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="09b79-119">Hvis det er relevant, kan ikke-arbejdstiden også angives for reglen.</span><span class="sxs-lookup"><span data-stu-id="09b79-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="09b79-120">Anvendelse af en kalenderskabelon til en ressource</span><span class="sxs-lookup"><span data-stu-id="09b79-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="09b79-121">I menuen **Ressourcer** skal du vælge **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="09b79-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="09b79-122">Vælg op til 25 **Reserverbare ressourcer** i gittervisningen, som skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="09b79-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="09b79-123">Vælg **Angiv kalender** og en dialogboks vises med en liste over tilgængelige arbejdstidsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="09b79-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="09b79-124">Vælg den til at finde den skabelon, som du vil bruge, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="09b79-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]