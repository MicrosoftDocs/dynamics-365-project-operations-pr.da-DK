---
title: Få en forståelse for projektstatus
description: Dette emne indeholder oplysninger om den status, der er tildelt til projekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993409"
---
# <a name="understand-project-status"></a><span data-ttu-id="0b931-103">Få en forståelse for projektstatus</span><span class="sxs-lookup"><span data-stu-id="0b931-103">Understand project status</span></span>

<span data-ttu-id="0b931-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0b931-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0b931-105">Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over et projekts tilstand baseret på omkostninger og indsats.</span><span class="sxs-lookup"><span data-stu-id="0b931-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="0b931-106">Felter for statusoversigt</span><span class="sxs-lookup"><span data-stu-id="0b931-106">Status summary fields</span></span>

- <span data-ttu-id="0b931-107">Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status.</span><span class="sxs-lookup"><span data-stu-id="0b931-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="0b931-108">Feltet bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko.</span><span class="sxs-lookup"><span data-stu-id="0b931-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="0b931-109">Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen.</span><span class="sxs-lookup"><span data-stu-id="0b931-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="0b931-110">Feltet **Status opdateret den** kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="0b931-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="0b931-111">Værdien i dette felt er et tidsstempel, der angiver, hvornår statussen senest er opdateret.</span><span class="sxs-lookup"><span data-stu-id="0b931-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="0b931-112">Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsgitteret.</span><span class="sxs-lookup"><span data-stu-id="0b931-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="0b931-113">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, opdateres disse felter til **Ahead**</span><span class="sxs-lookup"><span data-stu-id="0b931-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="0b931-114">Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, angives disse felter til **Bagud**.</span><span class="sxs-lookup"><span data-stu-id="0b931-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]