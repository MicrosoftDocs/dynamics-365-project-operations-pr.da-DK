---
title: Anvend demonstrationskonfiguration og konfigurationsdata
description: Dette emne indeholder oplysninger om, hvordan du anvender demonstrationskonfiguration og konfigurationsdata i forbindelse med Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948807"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="0fee5-103">Anvend demonstrationskonfiguration og konfigurationsdata for lille udrulning af Project Operations - aftale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="0fee5-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="0fee5-104">_\*\*Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0fee5-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="0fee5-105">Hent [Masterdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="0fee5-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="0fee5-106">Naviger til mappen *ProjOpsDemoDataSetupAndMaster - Integreret CMT*, og kør den eksekverbare fil *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="0fee5-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="0fee5-107">På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="0fee5-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="0fee5-109">På side 2 i CMT-guiden skal du vælge **Office 365** som **Udrulningstypen**.</span><span class="sxs-lookup"><span data-stu-id="0fee5-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="0fee5-110">Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="0fee5-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="0fee5-111">Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg derefter **Logon**.</span><span class="sxs-lookup"><span data-stu-id="0fee5-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Log på konfiguration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="0fee5-113">På side 3 skal du på lejeren vælge, hvilken organisation du vil importere demonstrationsdataene til, på listen over organisationer og derefter vælge **Login**.</span><span class="sxs-lookup"><span data-stu-id="0fee5-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="0fee5-114">På side 4 skal du vælge zip-filen *MasterAndSetupData* fra den udpakkede mappe *ProjOpsDemoDataSetupAndMaster - integreret CMT*.</span><span class="sxs-lookup"><span data-stu-id="0fee5-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fil](./media/3ZipFile.png)

![Vælg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="0fee5-117">Når zip-filen er valgt, skal du vælge **Importér data**.</span><span class="sxs-lookup"><span data-stu-id="0fee5-117">After the zip file is selected, select **Import Data**.</span></span>

![Importér data](./media/5ImportData.png)

10. <span data-ttu-id="0fee5-119">Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden.</span><span class="sxs-lookup"><span data-stu-id="0fee5-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="0fee5-120">Afslut CMT-guiden, når den er fuldført.</span><span class="sxs-lookup"><span data-stu-id="0fee5-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="0fee5-121">Kontrollér, om der er data i organisationen i følgende 20 objekter:</span><span class="sxs-lookup"><span data-stu-id="0fee5-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="0fee5-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="0fee5-122">Currency</span></span>
- <span data-ttu-id="0fee5-123">Afdeling</span><span class="sxs-lookup"><span data-stu-id="0fee5-123">Organizational Unit</span></span>
- <span data-ttu-id="0fee5-124">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="0fee5-124">Contact</span></span>
- <span data-ttu-id="0fee5-125">Momsgruppe</span><span class="sxs-lookup"><span data-stu-id="0fee5-125">Tax Group</span></span>
- <span data-ttu-id="0fee5-126">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="0fee5-126">Customer Group</span></span>
- <span data-ttu-id="0fee5-127">Enhed</span><span class="sxs-lookup"><span data-stu-id="0fee5-127">Unit</span></span>
- <span data-ttu-id="0fee5-128">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="0fee5-128">Unit Group</span></span>
- <span data-ttu-id="0fee5-129">Prisliste</span><span class="sxs-lookup"><span data-stu-id="0fee5-129">Price List</span></span>
- <span data-ttu-id="0fee5-130">Prisliste for projektparameter</span><span class="sxs-lookup"><span data-stu-id="0fee5-130">Project Parameter Price List</span></span>
- <span data-ttu-id="0fee5-131">Fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="0fee5-131">Invoice Frequency</span></span>
- <span data-ttu-id="0fee5-132">Detalje for fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="0fee5-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="0fee5-133">Kategori af reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="0fee5-133">Bookable Resource Category</span></span>
- <span data-ttu-id="0fee5-134">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="0fee5-134">Transaction Category</span></span>
- <span data-ttu-id="0fee5-135">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="0fee5-135">Expense Category</span></span>
- <span data-ttu-id="0fee5-136">Rollepris</span><span class="sxs-lookup"><span data-stu-id="0fee5-136">Role Price</span></span>
- <span data-ttu-id="0fee5-137">Transaktionskategoripris</span><span class="sxs-lookup"><span data-stu-id="0fee5-137">Transaction Category Price</span></span>
- <span data-ttu-id="0fee5-138">Egenskab</span><span class="sxs-lookup"><span data-stu-id="0fee5-138">Characteristic</span></span>
- <span data-ttu-id="0fee5-139">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="0fee5-139">Bookable Resource</span></span>
- <span data-ttu-id="0fee5-140">Tilknytning for reserverbar ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="0fee5-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="0fee5-141">Egenskab for reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="0fee5-141">Bookable Resource Characteristic</span></span>

![Fuldført import](./media/6CompleteImport.png)
