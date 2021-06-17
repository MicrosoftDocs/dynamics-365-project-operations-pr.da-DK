---
title: Anvend demonstrationskonfiguration og konfigurationsdata - lille
description: Dette emne indeholder oplysninger om, hvordan du anvender demonstrationskonfiguration og konfigurationsdata i forbindelse med Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997144"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="cdd21-103">Anvend demonstrationskonfiguration og konfigurationsdata for Project Operations - lille</span><span class="sxs-lookup"><span data-stu-id="cdd21-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="cdd21-104">_\*\*Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="cdd21-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="cdd21-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="cdd21-105">Prerequisites</span></span>

<span data-ttu-id="cdd21-106">Før du går i gang med konfigurationen, skal du have et Common Data Service-miljø (CDS), der er klargjort til Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cdd21-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="cdd21-107">Vejledninger</span><span class="sxs-lookup"><span data-stu-id="cdd21-107">Instructions</span></span>

1. <span data-ttu-id="cdd21-108">Hent [Masterdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="cdd21-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="cdd21-109">Naviger til mappen *ProjOpsSampleSetupData – kun CE-CMT*, og kør den eksekverbare fil *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="cdd21-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="cdd21-110">På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="cdd21-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="cdd21-112">På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.</span><span class="sxs-lookup"><span data-stu-id="cdd21-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="cdd21-113">Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="cdd21-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="cdd21-114">Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg derefter **Logon**.</span><span class="sxs-lookup"><span data-stu-id="cdd21-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Log på konfiguration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="cdd21-116">På side 3 skal du på lejeren vælge, hvilken organisation du vil importere demonstrationsdataene til, på listen over organisationer og derefter vælge **Login**.</span><span class="sxs-lookup"><span data-stu-id="cdd21-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="cdd21-117">På side 4 skal du vælge zip-filen *SampleSetupAndConfigData* fra den udpakkede mappe *ProjOpsSampleSetupData – kun CE-CMT*.</span><span class="sxs-lookup"><span data-stu-id="cdd21-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Zip-fil](./media/3ZipFile.png)

   ![Vælg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="cdd21-120">Når zip-filen er valgt, skal du vælge **Importér data**.</span><span class="sxs-lookup"><span data-stu-id="cdd21-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importér data](./media/5ImportData.png)

10. <span data-ttu-id="cdd21-122">Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden.</span><span class="sxs-lookup"><span data-stu-id="cdd21-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="cdd21-123">Afslut CMT-guiden, når den er fuldført.</span><span class="sxs-lookup"><span data-stu-id="cdd21-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="cdd21-124">Kontrollér, om der er data i organisationen i følgende 18 objekter:</span><span class="sxs-lookup"><span data-stu-id="cdd21-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="cdd21-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="cdd21-125">Currency</span></span>
    -   <span data-ttu-id="cdd21-126">Konto</span><span class="sxs-lookup"><span data-stu-id="cdd21-126">Account</span></span>
    -   <span data-ttu-id="cdd21-127">Afdeling</span><span class="sxs-lookup"><span data-stu-id="cdd21-127">Organizational Unit</span></span>
    -   <span data-ttu-id="cdd21-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="cdd21-128">Contact</span></span>
    -   <span data-ttu-id="cdd21-129">Enhed</span><span class="sxs-lookup"><span data-stu-id="cdd21-129">Unit</span></span>
    -   <span data-ttu-id="cdd21-130">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="cdd21-130">Unit Group</span></span>
    -   <span data-ttu-id="cdd21-131">Prisliste</span><span class="sxs-lookup"><span data-stu-id="cdd21-131">Price List</span></span>
    -   <span data-ttu-id="cdd21-132">Prisliste for projektparameter</span><span class="sxs-lookup"><span data-stu-id="cdd21-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="cdd21-133">Fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="cdd21-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="cdd21-134">Kategori af reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="cdd21-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="cdd21-135">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="cdd21-135">Transaction Category</span></span>
    -   <span data-ttu-id="cdd21-136">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="cdd21-136">Expense Category</span></span>
    -   <span data-ttu-id="cdd21-137">Rollepris</span><span class="sxs-lookup"><span data-stu-id="cdd21-137">Role Price</span></span>
    -   <span data-ttu-id="cdd21-138">Transaktionskategoripris</span><span class="sxs-lookup"><span data-stu-id="cdd21-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="cdd21-139">Egenskab</span><span class="sxs-lookup"><span data-stu-id="cdd21-139">Characteristic</span></span>
    -   <span data-ttu-id="cdd21-140">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="cdd21-140">Bookable Resource</span></span>
    -   <span data-ttu-id="cdd21-141">Tilknytning for reserverbar ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="cdd21-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="cdd21-142">Egenskab for reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="cdd21-142">Bookable Resource Characteristic</span></span>

    ![Fuldført import](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
