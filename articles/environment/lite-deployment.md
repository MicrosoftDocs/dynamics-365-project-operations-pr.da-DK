---
title: Udrul Project Operations - lille
description: Dette emne indeholder oplysninger om, hvordan du installerer den lille udrulning af Project Operations - aftale til proformafakturering.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950257"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="6f019-103">Udrul Project Operations - lille</span><span class="sxs-lookup"><span data-stu-id="6f019-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="6f019-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6f019-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6f019-105">Project Operations understøtter flere udrulningsmodeller.</span><span class="sxs-lookup"><span data-stu-id="6f019-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="6f019-106">Du kan finde den bedste udrulningsmodel under [Udrulningstyper](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="6f019-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="6f019-107">Denne udrulning, lille udrulnings – aftale til proformafakturering, resulterer en **Common Data Service-udrulning kun med Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="6f019-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="6f019-108">Installer Project Operations i et nyt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="6f019-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="6f019-109">Installer i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="6f019-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="6f019-110">Installer Project Operations i et nyt CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="6f019-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="6f019-111">Som [Global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations -licens kan du oprette et nyt CDS-miljø i [PowerPlatform Administration](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="6f019-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="6f019-112">Kontroller, at **CDS-database** og **Dynamics 365-apps** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="6f019-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="6f019-113">For flere oplysninger se [Opret og administrer miljøer i Power Platform Administrationen](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="6f019-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="6f019-114">Vælg **Microsoft Dynamics 365 Project Operations** fra udrulningslisten for Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="6f019-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="6f019-115">Installer Project Operations i et eksisterende CDS-miljø</span><span class="sxs-lookup"><span data-stu-id="6f019-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="6f019-116">Som [Global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens skal du finde det miljø i [PowerPlatform Administration](https://admin.powerplatform.com), hvor du vil installere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6f019-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="6f019-117">Installer **Microsoft Dynamics 365 Project Operations** fra udrulningslisten for Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="6f019-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="6f019-118">Du kan finde flere oplysninger i [Administrer Dynamics 365-apps](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="6f019-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]