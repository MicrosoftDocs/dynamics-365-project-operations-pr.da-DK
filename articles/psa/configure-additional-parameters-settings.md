---
title: Konfigurere yderligere parameterindstillinger
description: Sådan konfigurerer du yderligere parameterindstillinger i Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001104"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="f10bf-103">Konfigurere yderligere parameterindstillinger (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f10bf-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f10bf-104">Når du har konfigureret elementerne i tidligere emner, skal du angive supplerende projektparametre til brug i dine projekter.</span><span class="sxs-lookup"><span data-stu-id="f10bf-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="f10bf-105">Da du installerede [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], oprettede du en parameterindstilling for at oprette alle de poster, der kræves, for at [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kan fungere.</span><span class="sxs-lookup"><span data-stu-id="f10bf-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="f10bf-106">Nu er det tid til at gå tilbage og konfigurere yderligere felter til disse indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f10bf-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="f10bf-107">Du skal have konfigureret følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f10bf-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="f10bf-108">Afdeling:</span><span class="sxs-lookup"><span data-stu-id="f10bf-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="f10bf-109">Fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="f10bf-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="f10bf-110">Arbejdstimeskabelon</span><span class="sxs-lookup"><span data-stu-id="f10bf-110">Work hours template</span></span>  
  
-   <span data-ttu-id="f10bf-111">Prisliste</span><span class="sxs-lookup"><span data-stu-id="f10bf-111">Price list</span></span>  
 
<span data-ttu-id="f10bf-112">I dette trin skal du også angive, hvilken type ressourceallokering du ønsker:</span><span class="sxs-lookup"><span data-stu-id="f10bf-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="f10bf-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="f10bf-113">**Central**.</span></span> <span data-ttu-id="f10bf-114">Kun ressourceledere kan allokere ressourcer til projekter.</span><span class="sxs-lookup"><span data-stu-id="f10bf-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="f10bf-115">**Hybrid**.</span><span class="sxs-lookup"><span data-stu-id="f10bf-115">**Hybrid**.</span></span> <span data-ttu-id="f10bf-116">Ressourceledere, projektledere og firmaadministratorer kan allokere ressourcer til projekter.</span><span class="sxs-lookup"><span data-stu-id="f10bf-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="f10bf-117">Sådan indstilles projektparametre:</span><span class="sxs-lookup"><span data-stu-id="f10bf-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="f10bf-118">Gå til **Project Service > Parametre**.</span><span class="sxs-lookup"><span data-stu-id="f10bf-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="f10bf-119">Klik på den parameterindstilling, du vil konfigurere (den, du oprettede, da du installerede [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), eller klik på **Ny** for at oprette en ny.</span><span class="sxs-lookup"><span data-stu-id="f10bf-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="f10bf-120">I området **Generelt** skal du angive alle indstillinger for projektparametrene.</span><span class="sxs-lookup"><span data-stu-id="f10bf-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="f10bf-121">I området **Prisliste** skal du klikke på **+** for at tilføje en prisliste, vælge en prisliste på rullelisten **Prisliste** for projektparameter og derefter klikke på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f10bf-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="f10bf-122">Klik på knappen **Gem** i nederste højre hjørne af skærmen.</span><span class="sxs-lookup"><span data-stu-id="f10bf-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="f10bf-123">Projektparameterposten skal bibeholdes, for at Project Service kan fungere korrekt.</span><span class="sxs-lookup"><span data-stu-id="f10bf-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="f10bf-124">Denne post bør ikke slettes.</span><span class="sxs-lookup"><span data-stu-id="f10bf-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="f10bf-125">Se også</span><span class="sxs-lookup"><span data-stu-id="f10bf-125">See Also</span></span>  
 [<span data-ttu-id="f10bf-126">Konfigurere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f10bf-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]