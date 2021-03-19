---
title: Analyse af projekttilbud
description: Denne emne indeholder oplysninger om analyse af projekttilbud.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291252"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="18222-103">Analyse af projekttilbud</span><span class="sxs-lookup"><span data-stu-id="18222-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="18222-104">Dynamics 365 Project Service Automation analyserer projekttilbud for at anslå rentabiliteten.</span><span class="sxs-lookup"><span data-stu-id="18222-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="18222-105">Det analyserer også, hvor godt tilbuddet er justeret i forhold til kundens forventninger om leveringsdato eller færdiggørelsesdato og om budgettet.</span><span class="sxs-lookup"><span data-stu-id="18222-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="18222-106">Rentabilitetsanalyse</span><span class="sxs-lookup"><span data-stu-id="18222-106">Profitability analysis</span></span>

<span data-ttu-id="18222-107">Project Service Automation analyserer rentabiliteten ved hjælp af bruttoavancen og den justerede bruttoavance.</span><span class="sxs-lookup"><span data-stu-id="18222-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="18222-108">Bruttoavance beregnes ved hjælp af følgende formel:</span><span class="sxs-lookup"><span data-stu-id="18222-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="18222-109">Den justerede bruttoavance beregnes ved hjælp af følgende formel:</span><span class="sxs-lookup"><span data-stu-id="18222-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="18222-110">Hvis værdierne for bruttoavance og justeret bruttoavance er forskellige med en bred margen, klassificeres meget af arbejdet i tilbuddet som ikke-fakturerbart.</span><span class="sxs-lookup"><span data-stu-id="18222-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="18222-111">Analyse af kundens forventninger</span><span class="sxs-lookup"><span data-stu-id="18222-111">Analysis of customer expectations</span></span>

<span data-ttu-id="18222-112">Du kan analysere tilbud og oprette diagrammer til kundernes forventninger om tidsplanen og budgettet, hvis du har angivet værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="18222-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="18222-113">Feltet **Anmodet leveringsdato** i tilbudsoverskriften.</span><span class="sxs-lookup"><span data-stu-id="18222-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="18222-114">Feltet **Kundebudget** for hver tilbudslinje (for projektbaserede linjer og produktbaserede linjer).</span><span class="sxs-lookup"><span data-stu-id="18222-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="18222-115">Analyse af kundeforventninger om tidsplanen sker ved at sammenligne den seneste slutdato for tilbudslinjedetaljerne med den ønskede leveringsdato på tværs af alle tilbudslinjer i tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="18222-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="18222-116">Analyse af kundernes forventninger om budgettet sker ved at sammenligne summen af det samlede kundebudget med det tilbudte beløb på tværs af alle tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="18222-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]