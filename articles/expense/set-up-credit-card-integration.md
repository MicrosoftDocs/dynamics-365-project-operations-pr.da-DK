---
title: Konfigurer integration af kreditkort
description: I dette emne forklares det, hvordan du kan arbejde med udgiftsrelaterede kreditkorttransaktioner.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866676"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="77e5d-103">Konfigurer integration af kreditkort</span><span class="sxs-lookup"><span data-stu-id="77e5d-103">Set up credit card integration</span></span>

<span data-ttu-id="77e5d-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="77e5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="77e5d-105">Udgiftsrelaterede kreditkorttransaktioner kan konfigureres, så de automatisk importeres i forbindelse med en tilbagevendende tidsplan.</span><span class="sxs-lookup"><span data-stu-id="77e5d-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="77e5d-106">Alternativt kan transaktionerne importeres manuelt, efterhånden som behovet herfor opstår.</span><span class="sxs-lookup"><span data-stu-id="77e5d-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="77e5d-107">Kreditkorttransaktionerne importeres via dataobjektet for kreditkorttransaktionerne.</span><span class="sxs-lookup"><span data-stu-id="77e5d-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="77e5d-108">Import af kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="77e5d-108">Import credit card transactions</span></span>

<span data-ttu-id="77e5d-109">Hvis du vil importere kreditkorttransaktioner, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="77e5d-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="77e5d-110">På siden **Kreditkorttransaktioner** skal du vælge **Importer transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="77e5d-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="77e5d-111">Hvis du åbner datastyring for første gang, skal systemet opdatere listen over dataobjekter, før du kan fortsætte.</span><span class="sxs-lookup"><span data-stu-id="77e5d-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="77e5d-112">Angiv en entydig beskrivelse for det importerede job i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="77e5d-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="77e5d-113">I feltet **Dataformat for kilde** skal du vælge formatet for den fil, der indeholder de kreditkorttransaktioner, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="77e5d-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="77e5d-114">Vælg **Upload**, og find og vælg derefter den fil, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="77e5d-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="77e5d-115">Når filen er blevet uploadet, skal du validere tilknytningen af kreditkorttransaktionsfilen og kolonnerne i dataobjektet for kreditkorttransaktioner ved at vælge linket **Vis tilknytning** i feltet.</span><span class="sxs-lookup"><span data-stu-id="77e5d-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="77e5d-116">Hvis der er tilknytningsfejl, eller hvis du skal ændre tilknytningen, skal du foretage tilknytningen fra enten fanen **Tilknytningsvisualisering** eller fanen **Tilknytningsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="77e5d-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="77e5d-117">Hvis du vil automatisere kreditkorttransaktionerne, skal du vælge **Opret gentagende datajob**.</span><span class="sxs-lookup"><span data-stu-id="77e5d-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="77e5d-118">Du kan derefter angive den gentagelse, der definerer, hvor ofte der skal importeres kreditkorttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="77e5d-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="77e5d-119">Vælg **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="77e5d-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="77e5d-120">Hvis du vil importere den valgte fil nu, skal du vælge **Importér**.</span><span class="sxs-lookup"><span data-stu-id="77e5d-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="77e5d-121">Hvis der opstår fejl under importen, kan du få vist logfilen for udførelsen eller midlertidige lagringsdata for at se de fejl, du skal rette for at sikre en vellykket import.</span><span class="sxs-lookup"><span data-stu-id="77e5d-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="77e5d-122">Hvis du skal importere mere end ét filformat, skal du oprette separate importjob for de enkelte formattyper.</span><span class="sxs-lookup"><span data-stu-id="77e5d-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="77e5d-123">Gentildele kreditkorttransaktioner for fratrådte medarbejdere</span><span class="sxs-lookup"><span data-stu-id="77e5d-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="77e5d-124">Når en medarbejderpost er blevet afsluttet, deaktiveres brugerens Active Directory-domæneservices-konto (AD DS).</span><span class="sxs-lookup"><span data-stu-id="77e5d-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="77e5d-125">Der kan dog være aktive kreditkorttransaktioner, der stadig skal udgiftsføres og refunderes.</span><span class="sxs-lookup"><span data-stu-id="77e5d-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="77e5d-126">På siden **Kreditkorttransaktioner** kan du gentildele medarbejderen til enhver kreditkorttransaktion, hvor den tilknyttede medarbejder er blevet afsluttet.</span><span class="sxs-lookup"><span data-stu-id="77e5d-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="77e5d-127">Vælg en eller flere kreditkorttransaktioner, og vælg derefter **Tildel transaktioner igen**.</span><span class="sxs-lookup"><span data-stu-id="77e5d-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="77e5d-128">Du kan derefter vælge en anden medarbejder, som kreditkorttransaktionerne skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="77e5d-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="77e5d-129">Når kreditkorttransaktionerne er blevet tildelt en anden, kan de vælges til en udgiftsrapport og betales via den sædvanlige proces for refusion af udgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="77e5d-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="77e5d-130">Slet kreditkorttransaktioner</span><span class="sxs-lookup"><span data-stu-id="77e5d-130">Delete credit card transactions</span></span> 

<span data-ttu-id="77e5d-131">Når kreditkorttransaktioner er importeret, kan det undertiden være nødvendigt at slette visse transaktioner.</span><span class="sxs-lookup"><span data-stu-id="77e5d-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="77e5d-132">Dette kan skyldes, at transaktionerne er dubletter, eller at dataene muligvis ikke er nøjagtige.</span><span class="sxs-lookup"><span data-stu-id="77e5d-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="77e5d-133">Administratorer kan bruge funktionen **"Slet kreditkorttransaktioner"** til at vælge og slette kreditkorttransaktioner, der **ikke er knyttet til** en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="77e5d-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="77e5d-134">Gå til **Periodiske opgaver** > **Slet kreditkorttransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="77e5d-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="77e5d-135">Vælg **Filter**, og angiv oplysninger for at identificere de poster, der skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="77e5d-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="77e5d-136">Vælg **OK** for at slette posterne.</span><span class="sxs-lookup"><span data-stu-id="77e5d-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
