---
title: Konfigurer integration af kreditkort
description: I dette emne forklares det, hvordan du kan importere og vedligeholde udgiftsrelaterede kreditkorttransaktioner.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120851"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="316a2-103">Konfigurer integration af kreditkort</span><span class="sxs-lookup"><span data-stu-id="316a2-103">Set up credit card integration</span></span>

<span data-ttu-id="316a2-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="316a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="316a2-105">Udgiftsrelaterede kreditkorttransaktioner kan konfigureres, så de automatisk importeres i forbindelse med en tilbagevendende tidsplan.</span><span class="sxs-lookup"><span data-stu-id="316a2-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="316a2-106">Alternativt kan transaktionerne importeres manuelt, efterhånden som behovet herfor opstår.</span><span class="sxs-lookup"><span data-stu-id="316a2-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="316a2-107">Kreditkorttransaktionerne importeres via dataobjektet for kreditkorttransaktionerne.</span><span class="sxs-lookup"><span data-stu-id="316a2-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="316a2-108">Import af kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="316a2-108">Import credit card transactions</span></span>

1. <span data-ttu-id="316a2-109">På siden **Kreditkorttransaktioner** skal du vælge **Importer transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="316a2-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="316a2-110">Hvis du åbner datastyring for første gang, skal systemet opdatere listen over dataobjekter, før du kan fortsætte.</span><span class="sxs-lookup"><span data-stu-id="316a2-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="316a2-111">Angiv en entydig beskrivelse af det importerede job i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="316a2-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="316a2-112">I feltet **Dataformat for kilde** skal du vælge formatet for den fil, der indeholder de kreditkorttransaktioner, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="316a2-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="316a2-113">Vælg **Upload**, og find og vælg derefter den fil, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="316a2-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="316a2-114">Når filen er blevet uploadet, skal du validere tilknytningen af kreditkorttransaktionsfilen og kolonnerne i dataobjektet for kreditkorttransaktioner ved at vælge linket **Vis tilknytning** i feltet.</span><span class="sxs-lookup"><span data-stu-id="316a2-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="316a2-115">Hvis der er tilknytningsfejl, eller hvis du skal ændre tilknytningen, skal du foretage tilknytningen fra enten fanen **Tilknytningsvisualisering** eller fanen **Tilknytningsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="316a2-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="316a2-116">Hvis du vil automatisere kreditkorttransaktionerne, skal du vælge **Opret gentagende datajob**.</span><span class="sxs-lookup"><span data-stu-id="316a2-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="316a2-117">Du kan derefter angive den gentagelse, der definerer, hvor ofte der skal importeres kreditkorttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="316a2-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="316a2-118">Vælg **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="316a2-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="316a2-119">Hvis du vil importere den valgte fil nu, skal du vælge **Importér**.</span><span class="sxs-lookup"><span data-stu-id="316a2-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="316a2-120">Hvis der opstår fejl under importen, kan du gennemgå kørselsloggen eller de midlertidige data for at se de fejl, du skal løse for at sikre en vellykket import.</span><span class="sxs-lookup"><span data-stu-id="316a2-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="316a2-121">Hvis du skal importere mere end ét filformat, skal du oprette separate importjob for de enkelte formattyper.</span><span class="sxs-lookup"><span data-stu-id="316a2-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="316a2-122">Gentildele kreditkorttransaktioner for fratrådte medarbejdere</span><span class="sxs-lookup"><span data-stu-id="316a2-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="316a2-123">Når en medarbejderpost er blevet afsluttet, deaktiveres brugerens Active Directory-domæneservices-konto (AD DS).</span><span class="sxs-lookup"><span data-stu-id="316a2-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="316a2-124">Der kan dog være aktive kreditkorttransaktioner, der stadig skal udgiftsføres og refunderes.</span><span class="sxs-lookup"><span data-stu-id="316a2-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="316a2-125">På siden **Kreditkorttransaktioner** kan du gentildele medarbejderen i forbindelse med alle de kreditkorttransaktioner, hvor den tilknyttede medarbejder er blevet afsluttet.</span><span class="sxs-lookup"><span data-stu-id="316a2-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="316a2-126">Vælg en eller flere kreditkorttransaktioner, og vælg derefter **Tildel transaktioner igen**.</span><span class="sxs-lookup"><span data-stu-id="316a2-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="316a2-127">Du kan derefter vælge en anden medarbejder, som kreditkorttransaktionerne skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="316a2-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="316a2-128">Når kreditkorttransaktionerne er blevet tildelt en anden, kan de vælges til en udgiftsrapport og betales via den sædvanlige proces for refusion af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="316a2-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
