---
title: Definere ressourcekalendere
description: Dette emne indeholder oplysninger om, hvordan du definerer arbejdstidskalendere for ressourcer i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961840"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="74e7b-103">Definere ressourcekalendere</span><span class="sxs-lookup"><span data-stu-id="74e7b-103">Define resource calendars</span></span>

<span data-ttu-id="74e7b-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="74e7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74e7b-105">Alle de reserverbare ressourcer, der arbejder på et projekt, skal have en kalender med arbejdstid for at definere deres tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="74e7b-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="74e7b-106">Arbejdstiderne for en ressource kan defineres på to måder:</span><span class="sxs-lookup"><span data-stu-id="74e7b-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="74e7b-107">Definer individuelle kalenderregler for en ressource</span><span class="sxs-lookup"><span data-stu-id="74e7b-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="74e7b-108">Anvend en eksisterende kalenderskabelon for ressourcen</span><span class="sxs-lookup"><span data-stu-id="74e7b-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="74e7b-109">Definer en ressources arbejdstid</span><span class="sxs-lookup"><span data-stu-id="74e7b-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="74e7b-110">I menuen **Ressourcer** skal du vælge **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="74e7b-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="74e7b-111">I gittervisningen skal du vælge en anvendelig **Reserverbar ressource** .</span><span class="sxs-lookup"><span data-stu-id="74e7b-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="74e7b-112">På siden **Ressourcedetaljer** skal du vælge fanen **Arbejdstid**. Som standard er den reserverbare ressourcekalender arbejdstiderne for den standardarbejdsugeskabelon, der er defineret for organisationen.</span><span class="sxs-lookup"><span data-stu-id="74e7b-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="74e7b-113">Hvis du vil opdatere arbejdstiderne, skal du højreklikke på startdatoen for den foreslåede kalenderregel, der skal defineres.</span><span class="sxs-lookup"><span data-stu-id="74e7b-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="74e7b-114">Brug menuen kalenderregler til at definere en kalenderregel for en bestemt dag, resten af serien eller hele kalenderen.</span><span class="sxs-lookup"><span data-stu-id="74e7b-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="74e7b-115">Når indstillingen er valgt, kan du definere følgende:</span><span class="sxs-lookup"><span data-stu-id="74e7b-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="74e7b-116">Den ugedag, hvor arbejdstiden træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="74e7b-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="74e7b-117">Arbejdstiderne inden for hver dag.</span><span class="sxs-lookup"><span data-stu-id="74e7b-117">The working times within each day.</span></span>
    - <span data-ttu-id="74e7b-118">Tidszonen for kalenderreglen.</span><span class="sxs-lookup"><span data-stu-id="74e7b-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="74e7b-119">Hvis det er relevant, kan ikke-arbejdstiden også angives for reglen.</span><span class="sxs-lookup"><span data-stu-id="74e7b-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="74e7b-120">Anvendelse af en kalenderskabelon til en ressource</span><span class="sxs-lookup"><span data-stu-id="74e7b-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="74e7b-121">I menuen **Ressourcer** skal du vælge **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="74e7b-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="74e7b-122">Vælg op til 25 **Reserverbare ressourcer** i gittervisningen, som skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="74e7b-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="74e7b-123">Vælg **Angiv kalender** og en dialogboks vises med en liste over tilgængelige arbejdstidsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="74e7b-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="74e7b-124">Vælg den til at finde den skabelon, som du vil bruge, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="74e7b-124">Select the template you want to use, and then select **Apply**.</span></span>
