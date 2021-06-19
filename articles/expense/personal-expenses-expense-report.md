---
title: Arbejd med personlige udgifter i en udgiftsrapport
description: Dette emne indeholder oplysninger om, hvordan du arbejder med personlige udgifter, som medarbejdere afholder sig, mens de rejser i erhvervsmæssige øjemed.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025677"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="8a226-103">Arbejd med personlige udgifter i en udgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="8a226-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="8a226-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="8a226-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8a226-105">I forbindelse med forretningsrejser kan en medarbejder betale personlige udgifter med deres firmakreditkort.</span><span class="sxs-lookup"><span data-stu-id="8a226-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="8a226-106">Hvis der ikke er defineret en proces til håndtering af personlige udgifter, kan godkendelsesprocessen for udgiftsrapporten blive afbrudt, når en medarbejder indsender sin specificerede udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="8a226-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="8a226-107">Der er to metoder, som du kan bruge til at arbejde med en medarbejders personlige udgifter:</span><span class="sxs-lookup"><span data-stu-id="8a226-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="8a226-108">**Betalt af medarbejder**: Din organisation betaler ikke de personlige udgifter, der fremgår af fakturaen for virksomhedens kreditkort.</span><span class="sxs-lookup"><span data-stu-id="8a226-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="8a226-109">I stedet betaler medarbejderen kreditkortleverandøren direkte for udgifterne.</span><span class="sxs-lookup"><span data-stu-id="8a226-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="8a226-110">**Betalt af virksomhed**: Din organisation betaler den fulde faktura for firmakreditkortet og debiterer derefter arbejderens konto for de personlige udgifter.</span><span class="sxs-lookup"><span data-stu-id="8a226-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="8a226-111">Du kan vælge den metode, som din organisation bruger, på siden **Parametre for udgiftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="8a226-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="8a226-112">Aktivér funktionen til opdeling af udgifter, når der er defineret en værdi i et personligt beløbsfelt</span><span class="sxs-lookup"><span data-stu-id="8a226-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="8a226-113">Funktionen **Aktivér omkostningsfordeling, når der er defineret en værdi i et personligt beløbsfelt** gælder kun for udgiftsrapporter, der er godkendt ved hjælp af en arbejdsproces på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="8a226-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="8a226-114">Rapporter godkendes ved at gå til **Behandl udgiftsrapporter** > **Udgiftsrapporter, der er tildelt til mig** > **Åbn udgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="8a226-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="8a226-115">Hvis du vil aktivere denne funktion, skal du gå til **Arbejdsområder** > **Funktionsadministration**, vælge **Aktiver funktionen til opdeling af udgifter, når der er defineret en værdi i et personligt beløbsfelt**, og vælg derefter **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="8a226-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="8a226-116">Når funktionen er aktiveret, opretter de udgiftslinjer, der bruger denne funktion, to linjer, når rapporten indsendes.</span><span class="sxs-lookup"><span data-stu-id="8a226-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="8a226-117">Der oprettes to linjer, så godkenderen kan godkende hver linje separat.</span><span class="sxs-lookup"><span data-stu-id="8a226-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
