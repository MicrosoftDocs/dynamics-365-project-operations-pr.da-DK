---
title: Få en forståelse for projektstatus
description: Dette emne indeholder oplysninger om den status, der tildeles projekter i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074044"
---
# <a name="understand-project-status"></a><span data-ttu-id="cc37f-103">Få en forståelse for projektstatus</span><span class="sxs-lookup"><span data-stu-id="cc37f-103">Understand project status</span></span>

<span data-ttu-id="cc37f-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="cc37f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="cc37f-105">Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over et projekts tilstand baseret på omkostninger og indsats.</span><span class="sxs-lookup"><span data-stu-id="cc37f-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="cc37f-106">Felter for statusoversigt</span><span class="sxs-lookup"><span data-stu-id="cc37f-106">Status summary fields</span></span>

- <span data-ttu-id="cc37f-107">Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status.</span><span class="sxs-lookup"><span data-stu-id="cc37f-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="cc37f-108">Feltet bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko.</span><span class="sxs-lookup"><span data-stu-id="cc37f-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="cc37f-109">Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen.</span><span class="sxs-lookup"><span data-stu-id="cc37f-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="cc37f-110">Feltet **Status opdateret for** kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="cc37f-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="cc37f-111">Værdien i dette felt er et tidsstempel, der angiver, hvornår statussen senest er opdateret.</span><span class="sxs-lookup"><span data-stu-id="cc37f-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="cc37f-112">Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsgitteret.</span><span class="sxs-lookup"><span data-stu-id="cc37f-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="cc37f-113">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, opdateres disse felter til **Forud**.</span><span class="sxs-lookup"><span data-stu-id="cc37f-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="cc37f-114">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, angives disse felter til **Bagud**.</span><span class="sxs-lookup"><span data-stu-id="cc37f-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
