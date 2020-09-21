---
title: Konfigurere ressourceroller
description: Sådan konfigurerer du ressourceroller i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0a180069-17d9-40fd-b4af-9b8d50f373ea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6a32ec4380e847b897931b6691fa8f9784d0cee7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750509"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="fdee9-103">Konfigurere ressourceroller (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fdee9-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fdee9-104">Roller er vigtige i projektplanlægningen, når ressourcekrav eller omkostninger for et projekt fastsættes.</span><span class="sxs-lookup"><span data-stu-id="fdee9-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="fdee9-105">For hver rolle, som dit projekt kræver, skal du oprette en ressourcerolle og knytte færdigheder og kompetencer til denne rolle.</span><span class="sxs-lookup"><span data-stu-id="fdee9-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="fdee9-106">For eksempel kan du oprette roller for udvikler, projektleder eller spiltester.</span><span class="sxs-lookup"><span data-stu-id="fdee9-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="fdee9-107">Du skal også angive de færdigheder og kompetenceniveauer, der kræves til rollen.</span><span class="sxs-lookup"><span data-stu-id="fdee9-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="fdee9-108">Konfigurer ressourceroller for at sikre et effektivt projektestimat for organisationen.</span><span class="sxs-lookup"><span data-stu-id="fdee9-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="fdee9-109">Kontroller også, at du faktisk har angivet faktureringstypen.</span><span class="sxs-lookup"><span data-stu-id="fdee9-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="fdee9-110">Et element med en ikke-fakturerbar faktureringstype vises ikke på kontrakt- eller tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="fdee9-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="fdee9-111">Når du har oprettet ressourceroller, kan du konfigurere kost- og salgspriser med en prisliste.</span><span class="sxs-lookup"><span data-stu-id="fdee9-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="fdee9-112">For hver rolle, du vil tilføje, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="fdee9-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="fdee9-113">Gå til **Project Service > Ressourceroller**.</span><span class="sxs-lookup"><span data-stu-id="fdee9-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="fdee9-114">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fdee9-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="fdee9-115">I området **Generelt** skal du angive et navn for rollen i **Navn** og derefter udfylde de øvrige felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="fdee9-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="fdee9-116">Klik på **Gem** for at oprette posten, så du kan fortsætte med at redigere den.</span><span class="sxs-lookup"><span data-stu-id="fdee9-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="fdee9-117">Klik på **+** i området **Færdigheder** for at tilføje en færdighed.</span><span class="sxs-lookup"><span data-stu-id="fdee9-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="fdee9-118">I ruden **Kompetencekrav for rolle** skal du klikke på feltet **Færdigheder**, klikke på knappen **Søg** og vælge en færdighed.</span><span class="sxs-lookup"><span data-stu-id="fdee9-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="fdee9-119">Vælg en kompetence for færdigheden, og klik derefter på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fdee9-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="fdee9-120">Fortsæt med at tilføje færdigheder efter behov.</span><span class="sxs-lookup"><span data-stu-id="fdee9-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="fdee9-121">Når du er færdig med redigeringen, skal du klikke på knappen **Gem** i nederste højre hjørne af skærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="fdee9-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="fdee9-122">For at gøre denne ressourcerolle tilgængelig, så den kan bruges af projekter, skal du klikke på **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="fdee9-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fdee9-123">Se også</span><span class="sxs-lookup"><span data-stu-id="fdee9-123">See Also</span></span>  
 [<span data-ttu-id="fdee9-124">Konfigurere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fdee9-124">Set up resources</span></span>](../project-service/set-up-resources.md)
