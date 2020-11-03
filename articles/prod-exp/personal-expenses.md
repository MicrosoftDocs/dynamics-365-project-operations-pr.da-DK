---
title: Personlige udgifter i en udgiftsrapport
description: I dette emne beskrives de to metoder til håndtering af en arbejders personlige udgifter i Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074321"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="141fc-103">Personlige udgifter i en udgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="141fc-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="141fc-104">På forretningsrejser betaler arbejdere ofte personlige udgifter med virksomhedens kreditkort.</span><span class="sxs-lookup"><span data-stu-id="141fc-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="141fc-105">Hvis du ikke definerer en proces til håndtering af personlige udgifter, kan godkendelsesprocessen for udgiftsrapporter blive afbrudt, når arbejdere indsender deres specificerede udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="141fc-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="141fc-106">Der findes to metoder til håndtering af en arbejders personlige udgifter:</span><span class="sxs-lookup"><span data-stu-id="141fc-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="141fc-107">**Betalt af medarbejder** – Din organisation betaler ikke de personlige udgifter, der fremgår af fakturaen for virksomhedens kreditkort.</span><span class="sxs-lookup"><span data-stu-id="141fc-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="141fc-108">I stedet opretter den en rapport, der viser personlige udgifter sammen med de virksomhedsudgifter, der blev opkrævet på virksomhedens kreditkort.</span><span class="sxs-lookup"><span data-stu-id="141fc-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="141fc-109">**Betalt af virksomhed** – Din organisation betaler hele fakturaen for virksomhedens kreditkort og debiterer derefter arbejderens konto for de personlige udgifter.</span><span class="sxs-lookup"><span data-stu-id="141fc-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="141fc-110">Du kan vælge den metode, som din organisation bruger, på siden **Parametre for udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="141fc-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
