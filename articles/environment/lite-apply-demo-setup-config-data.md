---
title: Anvend demonstrationskonfiguration og konfigurationsdata - lille
description: Dette emne indeholder oplysninger om, hvordan du anvender demonstrationskonfiguration og konfigurationsdata i forbindelse med Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401256"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="a5c7c-103">Anvend demonstrationskonfiguration og konfigurationsdata for Project Operations - lille</span><span class="sxs-lookup"><span data-stu-id="a5c7c-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="a5c7c-104">_\*\*Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a5c7c-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a5c7c-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="a5c7c-105">Prerequisites</span></span>

<span data-ttu-id="a5c7c-106">Før du går i gang med konfigurationen, skal du have et Common Data Service-miljø (CDS), der er klargjort til Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="a5c7c-107">Instruktioner</span><span class="sxs-lookup"><span data-stu-id="a5c7c-107">Instructions</span></span>

1. <span data-ttu-id="a5c7c-108">Hent [Masterdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="a5c7c-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="a5c7c-109">Naviger til mappen *ProjOpsDemoDataSetupAndMaster - Integreret CMT*, og kør den eksekverbare fil *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a5c7c-110">På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a5c7c-112">På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a5c7c-113">Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a5c7c-114">Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg derefter **Logon**.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Log på konfiguration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a5c7c-116">På side 3 skal du på lejeren vælge, hvilken organisation du vil importere demonstrationsdataene til, på listen over organisationer og derefter vælge **Login**.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="a5c7c-117">På side 4 skal du vælge zip-filen *MasterAndSetupData* fra den udpakkede mappe *ProjOpsDemoDataSetupAndMaster - integreret CMT*.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fil](./media/3ZipFile.png)

![Vælg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="a5c7c-120">Når zip-filen er valgt, skal du vælge **Importér data**.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-120">After the zip file is selected, select **Import Data**.</span></span>

![Importér data](./media/5ImportData.png)

10. <span data-ttu-id="a5c7c-122">Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a5c7c-123">Afslut CMT-guiden, når den er fuldført.</span><span class="sxs-lookup"><span data-stu-id="a5c7c-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a5c7c-124">Kontrollér, om der er data i organisationen i følgende 20 objekter:</span><span class="sxs-lookup"><span data-stu-id="a5c7c-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="a5c7c-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="a5c7c-125">Currency</span></span>
-   <span data-ttu-id="a5c7c-126">Konto</span><span class="sxs-lookup"><span data-stu-id="a5c7c-126">Account</span></span>
-   <span data-ttu-id="a5c7c-127">Afdeling</span><span class="sxs-lookup"><span data-stu-id="a5c7c-127">Organizational Unit</span></span>
-   <span data-ttu-id="a5c7c-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="a5c7c-128">Contact</span></span>
-   <span data-ttu-id="a5c7c-129">Momsgruppe</span><span class="sxs-lookup"><span data-stu-id="a5c7c-129">Tax Group</span></span>
-   <span data-ttu-id="a5c7c-130">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="a5c7c-130">Customer Group</span></span>
-   <span data-ttu-id="a5c7c-131">Enhed</span><span class="sxs-lookup"><span data-stu-id="a5c7c-131">Unit</span></span>
-   <span data-ttu-id="a5c7c-132">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="a5c7c-132">Unit Group</span></span>
-   <span data-ttu-id="a5c7c-133">Prisliste</span><span class="sxs-lookup"><span data-stu-id="a5c7c-133">Price List</span></span>
-   <span data-ttu-id="a5c7c-134">Prisliste for projektparameter</span><span class="sxs-lookup"><span data-stu-id="a5c7c-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="a5c7c-135">Fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="a5c7c-135">Invoice Frequency</span></span>
-   <span data-ttu-id="a5c7c-136">Kategori af reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="a5c7c-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="a5c7c-137">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="a5c7c-137">Transaction Category</span></span>
-   <span data-ttu-id="a5c7c-138">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="a5c7c-138">Expense Category</span></span>
-   <span data-ttu-id="a5c7c-139">Rollepris</span><span class="sxs-lookup"><span data-stu-id="a5c7c-139">Role Price</span></span>
-   <span data-ttu-id="a5c7c-140">Transaktionskategoripris</span><span class="sxs-lookup"><span data-stu-id="a5c7c-140">Transaction Category Price</span></span>
-   <span data-ttu-id="a5c7c-141">Egenskab</span><span class="sxs-lookup"><span data-stu-id="a5c7c-141">Characteristic</span></span>
-   <span data-ttu-id="a5c7c-142">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="a5c7c-142">Bookable Resource</span></span>
-   <span data-ttu-id="a5c7c-143">Tilknytning for reserverbar ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="a5c7c-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="a5c7c-144">Egenskab for reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="a5c7c-144">Bookable Resource Characteristic</span></span>

![Fuldført import](./media/6CompleteImport.png)
