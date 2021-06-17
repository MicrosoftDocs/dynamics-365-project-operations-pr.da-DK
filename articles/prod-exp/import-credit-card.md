---
title: Importer og vedligehold kreditkorttransaktioner
description: I dette emne forklares det, hvordan du kan importere og vedligeholde udgiftsrelaterede kreditkorttransaktioner. Disse transaktioner kan konfigureres, så de automatisk importeres i en tilbagevendende tidsplan, eller de kan importeres manuelt, efterhånden som der er behov for dem.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005154"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="a3c1f-104">Importer og vedligehold kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="a3c1f-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="a3c1f-105">Udgiftsrelaterede kreditkorttransaktioner kan konfigureres, så de automatisk importeres i forbindelse med en tilbagevendende tidsplan.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="a3c1f-106">Alternativt kan transaktionerne importeres manuelt, efterhånden som behovet herfor opstår.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="a3c1f-107">Kreditkorttransaktionerne importeres via dataobjektet for kreditkorttransaktionerne.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="a3c1f-108">Du kan finde flere oplysninger om dataobjekter i [Dataobjekter](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="a3c1f-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="a3c1f-109">Import af kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="a3c1f-109">Import credit card transactions</span></span>

1. <span data-ttu-id="a3c1f-110">På siden **Kreditkorttransaktioner** skal du vælge **Importer transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="a3c1f-111">Hvis du åbner datastyring for første gang, skal systemet opdatere listen over dataobjekter, før du kan fortsætte.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="a3c1f-112">Angiv en entydig beskrivelse af det importerede job i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="a3c1f-113">I feltet **Dataformat for kilde** skal du vælge formatet for den fil, der indeholder de kreditkorttransaktioner, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="a3c1f-114">Vælg **Upload**, og find og vælg derefter den fil, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="a3c1f-115">Når filen er blevet uploadet, skal du validere tilknytningen af kreditkorttransaktionsfilen og kolonnerne i dataobjektet for kreditkorttransaktioner ved at vælge linket **Vis tilknytning** i feltet.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="a3c1f-116">Hvis der er tilknytningsfejl, eller hvis du skal ændre tilknytningen, skal du foretage tilknytningen fra enten fanen **Tilknytningsvisualisering** eller fanen **Tilknytningsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="a3c1f-117">Hvis du vil automatisere kreditkorttransaktionerne, skal du vælge **Opret gentagende datajob**.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="a3c1f-118">Du kan derefter angive den gentagelse, der definerer, hvor ofte der skal importeres kreditkorttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="a3c1f-119">Vælg **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="a3c1f-120">Hvis du vil importere den valgte fil nu, skal du vælge **Importér**.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="a3c1f-121">Hvis der opstår fejl under importen, kan du gennemgå kørselsloggen eller de midlertidige data for at se de fejl, du skal løse for at sikre en vellykket import.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="a3c1f-122">Hvis du skal importere mere end ét filformat, skal du oprette separate importjob for de enkelte formattyper.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="a3c1f-123">Gentildele kreditkorttransaktioner for fratrådte medarbejdere</span><span class="sxs-lookup"><span data-stu-id="a3c1f-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="a3c1f-124">Når en medarbejderpost er blevet afsluttet, deaktiveres brugerens Active Directory-domæneservices-konto (AD DS).</span><span class="sxs-lookup"><span data-stu-id="a3c1f-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="a3c1f-125">Der kan dog være aktive kreditkorttransaktioner, der stadig skal udgiftsføres og refunderes.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="a3c1f-126">På siden **Kreditkorttransaktioner** kan du gentildele medarbejderen i forbindelse med alle de kreditkorttransaktioner, hvor den tilknyttede medarbejder er blevet afsluttet.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="a3c1f-127">Vælg en eller flere kreditkorttransaktioner, og vælg derefter **Tildel transaktioner igen**.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="a3c1f-128">Du kan derefter vælge en anden medarbejder, som kreditkorttransaktionerne skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="a3c1f-129">Når kreditkorttransaktionerne er blevet tildelt en anden, kan de vælges til en udgiftsrapport og betales via den sædvanlige proces for refusion af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="a3c1f-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]