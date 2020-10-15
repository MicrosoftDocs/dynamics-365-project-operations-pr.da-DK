---
title: Pr. dag
description: Dette emne indeholder oplysninger om de diætregler, der bruges i udgiftsstyring.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908014"
---
# <a name="per-diems"></a><span data-ttu-id="c1ac0-103">Pr. dag</span><span class="sxs-lookup"><span data-stu-id="c1ac0-103">Per diems</span></span>

<span data-ttu-id="c1ac0-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="c1ac0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="c1ac0-105">En diæt er en godtgørelse, der udbetales til en arbejder, der rejser i forbindelse med arbejde.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="c1ac0-106">I udgiftsstyring kan du oprette diætregler for forskellige rejsesituationer.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="c1ac0-107">Diætsatser kan være baseret på tidspunktet for året, rejselokationen eller begge.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="c1ac0-108">Når du opretter en diætregel, kan du angive, at en procentdel af diætsatsen skal tilbageholdes, hvis en arbejder modtager gratis måltider eller servicer.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="c1ac0-109">Du kan også angive en nedre og øvre grænse for antallet af timer, hvor diætsatsen skal finde anvendelse på en arbejders rejse.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="c1ac0-110">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c1ac0-110">Configuration</span></span> 

1. <span data-ttu-id="c1ac0-111">Hvis du vil tilføje diætlokationer, skal du gå til **Konfigurer** > **Beregninger og koder** > **Diætlokation**.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="c1ac0-112">Vælg en diætsats og valuta, der er gyldig i perioden mellem en bestemt start- og slutdato, for hotel, måltider og andre udgifter for hver af de lokationer, der er tilføjet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="c1ac0-113">Diætsatser og valutaer konfigureres under **Konfigurer** > **Beregninger og koder** > **Diæter**.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="c1ac0-114">På siden **Diætlokationer** skal du konfigurere niveauerne for diætsatser.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="c1ac0-115">Diætsatsniveauer giver dig mulighed for at definere den procentvise opdeling af et dagligt tilskud til hotel, måltider og andre udgifter.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="c1ac0-116">Hvis du vil angive den procentvise måltidsreduktion for morgenmad, frokost eller aftensmad, skal du opdatere felterne på siden med **Parametre til udgiftsstyring** under fanen **Diæter**.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="c1ac0-117">Indsend udgifter ved hjælp af diæter</span><span class="sxs-lookup"><span data-stu-id="c1ac0-117">Submit expenses using per diem</span></span>
<span data-ttu-id="c1ac0-118">Hvis du vil indsende udgifter, der anvender diæter, skal du bruge udgiftskategorien **Diæter**, når du opretter en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="c1ac0-119">Angiv **Diæt fra dato**, **Diæt til dato** og **Diætlokation**.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="c1ac0-120">Beløbet vil blive beregnet på baggrund af diætsatserne for den valgte lokation, og reduktionen af måltid beregnes på baggrund af diætsatsniveauerne.</span><span class="sxs-lookup"><span data-stu-id="c1ac0-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
