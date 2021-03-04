---
title: Konfigurere ressourceroller
description: Sådan konfigurerer du ressourceroller i Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: deaff0977ebb50382a28494fba2a1c34ed5cc9b4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144901"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="3c2c9-103">Konfigurere ressourceroller (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3c2c9-103">Configure resource roles (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3c2c9-104">Roller er vigtige i projektplanlægningen, når ressourcekrav eller omkostninger for et projekt fastsættes.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="3c2c9-105">For hver rolle, som dit projekt kræver, skal du oprette en ressourcerolle og knytte færdigheder og kompetencer til denne rolle.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="3c2c9-106">For eksempel kan du oprette roller for udvikler, projektleder eller spiltester.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="3c2c9-107">Du skal også angive de færdigheder og kompetenceniveauer, der kræves til rollen.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="3c2c9-108">Konfigurer ressourceroller for at sikre et effektivt projektestimat for organisationen.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="3c2c9-109">Kontroller også, at du faktisk har angivet faktureringstypen.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="3c2c9-110">Et element med en ikke-fakturerbar faktureringstype vises ikke på kontrakt- eller tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="3c2c9-111">Når du har oprettet ressourceroller, kan du konfigurere kost- og salgspriser med en prisliste.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="3c2c9-112">For hver rolle, du vil tilføje, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="3c2c9-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="3c2c9-113">Gå til **Project Service > Ressourceroller**.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="3c2c9-114">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="3c2c9-115">I området **Generelt** skal du angive et navn for rollen i **Navn** og derefter udfylde de øvrige felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="3c2c9-116">Klik på **Gem** for at oprette posten, så du kan fortsætte med at redigere den.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="3c2c9-117">Klik på **+** i området **Færdigheder** for at tilføje en færdighed.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="3c2c9-118">I ruden **Kompetencekrav for rolle** skal du klikke på feltet **Færdigheder**, klikke på knappen **Søg** og vælge en færdighed.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="3c2c9-119">Vælg en kompetence for færdigheden, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="3c2c9-120">Fortsæt med at tilføje færdigheder efter behov.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="3c2c9-121">Når du er færdig med redigeringen, skal du klikke på knappen **Gem** i nederste højre hjørne af skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="3c2c9-122">For at gøre denne ressourcerolle tilgængelig, så den kan bruges af projekter, skal du klikke på **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="3c2c9-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3c2c9-123">Se også</span><span class="sxs-lookup"><span data-stu-id="3c2c9-123">See Also</span></span>  
 [<span data-ttu-id="3c2c9-124">Konfigurere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3c2c9-124">Set up resources</span></span>](../psa/set-up-resources.md)
