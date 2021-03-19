---
title: Konfigurer og anvend konfigurationsdata i Common Data Service
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer og anvender demonstrationskonfiguration og konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289812"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="d461a-103">Konfigurer og anvend konfigurationsdata i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d461a-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="d461a-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="d461a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="d461a-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="d461a-105">Prerequisites</span></span>

<span data-ttu-id="d461a-106">Før du begynder at konfigurere data i Common Data Service (CDS), skal følgende forudsætninger være opfyldt:</span><span class="sxs-lookup"><span data-stu-id="d461a-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="d461a-107">Klargør et CDS-miljø og et Dynamics 365 Finance-miljø til Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d461a-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="d461a-108">Oplysninger om juridiske enheder fra Dynamics 365 Finance deles med CDS-miljøet.</span><span class="sxs-lookup"><span data-stu-id="d461a-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="d461a-109">Dette betyder, at objektet **Virksomehd** i CDS indeholder følgende firmaposter:</span><span class="sxs-lookup"><span data-stu-id="d461a-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="d461a-110">THPM</span><span class="sxs-lookup"><span data-stu-id="d461a-110">THPM</span></span>
  - <span data-ttu-id="d461a-111">USPM</span><span class="sxs-lookup"><span data-stu-id="d461a-111">USPM</span></span>
  - <span data-ttu-id="d461a-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="d461a-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="d461a-113">Installer konfiguration og konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="d461a-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="d461a-114">Hent, fjern blokeringen af, og udpak [Installations- og konfigurationsdatapakken](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="d461a-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="d461a-115">Naviger til den zippede mappe og kør den eksekverbare fil *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d461a-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d461a-116">På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="d461a-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d461a-118">På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.</span><span class="sxs-lookup"><span data-stu-id="d461a-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d461a-119">Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="d461a-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d461a-120">Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg **Logon**.</span><span class="sxs-lookup"><span data-stu-id="d461a-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Log på konfiguration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d461a-122">På side 3 skal du på lejeren vælge den organisation, som du vil importere demonstrationsdataene til, på listen over organisationer og vælge **Login**.</span><span class="sxs-lookup"><span data-stu-id="d461a-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="d461a-123">På side 4 skal du vælge zip-filen *SampleSetupAndConfigData* fra den udpakkede mappe.</span><span class="sxs-lookup"><span data-stu-id="d461a-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Valg af zip-fil](./media/3ZipFile.png)

![Vælg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="d461a-126">Når zip-filen er valgt, skal du vælge **Importér data**.</span><span class="sxs-lookup"><span data-stu-id="d461a-126">After the zip file is selected, select **Import Data**.</span></span>

![Importér data](./media/5ImportData.png)

10. <span data-ttu-id="d461a-128">Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden.</span><span class="sxs-lookup"><span data-stu-id="d461a-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d461a-129">Afslut CMT-guiden, når importen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="d461a-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d461a-130">Kontrollér, om der er data i organisationen i følgende 19 objekter:</span><span class="sxs-lookup"><span data-stu-id="d461a-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="d461a-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="d461a-131">Currency</span></span>
  - <span data-ttu-id="d461a-132">Afdeling</span><span class="sxs-lookup"><span data-stu-id="d461a-132">Organizational Unit</span></span>
  - <span data-ttu-id="d461a-133">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="d461a-133">Contact</span></span>
  - <span data-ttu-id="d461a-134">Momsgruppe</span><span class="sxs-lookup"><span data-stu-id="d461a-134">Tax Group</span></span>
  - <span data-ttu-id="d461a-135">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="d461a-135">Customer Group</span></span>
  - <span data-ttu-id="d461a-136">Enhed</span><span class="sxs-lookup"><span data-stu-id="d461a-136">Unit</span></span>
  - <span data-ttu-id="d461a-137">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="d461a-137">Unit Group</span></span>
  - <span data-ttu-id="d461a-138">Prisliste</span><span class="sxs-lookup"><span data-stu-id="d461a-138">Price List</span></span>
  - <span data-ttu-id="d461a-139">Prisliste for projektparameter</span><span class="sxs-lookup"><span data-stu-id="d461a-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="d461a-140">Fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="d461a-140">Invoice Frequency</span></span>
  - <span data-ttu-id="d461a-141">Kategori af reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="d461a-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="d461a-142">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="d461a-142">Transaction Category</span></span>
  - <span data-ttu-id="d461a-143">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="d461a-143">Expense Category</span></span>
  - <span data-ttu-id="d461a-144">Rollepris</span><span class="sxs-lookup"><span data-stu-id="d461a-144">Role Price</span></span>
  - <span data-ttu-id="d461a-145">Transaktionskategoripris</span><span class="sxs-lookup"><span data-stu-id="d461a-145">Transaction Category Price</span></span>
  - <span data-ttu-id="d461a-146">Egenskab</span><span class="sxs-lookup"><span data-stu-id="d461a-146">Characteristic</span></span>
  - <span data-ttu-id="d461a-147">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="d461a-147">Bookable Resource</span></span>
  - <span data-ttu-id="d461a-148">Tilknytning for reserverbar ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="d461a-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="d461a-149">Egenskab for reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="d461a-149">Bookable Resource Characteristic</span></span>

![Fuldført import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="d461a-151">Opdater konfigurationer for Project Operations</span><span class="sxs-lookup"><span data-stu-id="d461a-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="d461a-152">Naviger til CE-miljø.</span><span class="sxs-lookup"><span data-stu-id="d461a-152">Navigate to the CE environment.</span></span> <span data-ttu-id="d461a-153">Du kan finde det ved at åbne [Power Platform Administration](https://admin.powerplatform.microsoft.com/environments), vælge miljøet og derefter vælge **Åbn miljø**.</span><span class="sxs-lookup"><span data-stu-id="d461a-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Åbn miljø](./media/7OpenEnvironment.png)

2. <span data-ttu-id="d461a-155">Gå til **Projekter** > **Ressourcer**, og vælg derefter **Ny** for at oprette en reserverbar ressource til brugeren.</span><span class="sxs-lookup"><span data-stu-id="d461a-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Reserverbare ressourcer](./media/8BookableResources.png)

3. <span data-ttu-id="d461a-157">På fanen **Generelt** skal du vælge din administratorbruger.</span><span class="sxs-lookup"><span data-stu-id="d461a-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="d461a-158">Kontroller, at tidszonen stemmer overens med den, du befinder dig i.</span><span class="sxs-lookup"><span data-stu-id="d461a-158">Verify that the time zone matches the one you are in.</span></span> 

![Ny reserverbar ressource](./media/9NewBookableResource.png)

4. <span data-ttu-id="d461a-160">På fanen **Planlægning** skal du i feltet **Virksomhed** vælge virksomheden **USPM** og derefter vælge **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d461a-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planlægningsfane](./media/10SchedulingTab.png)

5. <span data-ttu-id="d461a-162">Vælg fanen **Arbejdstid**.</span><span class="sxs-lookup"><span data-stu-id="d461a-162">Select the **Work hours** tab.</span></span>  

![Arbejdstimer](./media/11WorkHours.png)

6. <span data-ttu-id="d461a-164">Dobbeltklik på en vilkårlig værdi i kalenderen, og vælg **Rediger** > **Alle arrangementer i serien**.</span><span class="sxs-lookup"><span data-stu-id="d461a-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbejdskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="d461a-166">Skift arbejdstid til en otte (8) timer arbejdsdag, markér weekender som ikke-arbejdsdage, og kontrollér, at tidszonen stemmer overens med din.</span><span class="sxs-lookup"><span data-stu-id="d461a-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="d461a-167">Vælg **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="d461a-167">Select **Save and close**.</span></span>

![Opdater kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="d461a-169">Gå til **Indstillinger** > **Kalenderskabeloner**, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d461a-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalenderskabeloner](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="d461a-171">Angiv et navn, vælg den skabelonressource, du har oprettet, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d461a-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Gem kalenderskabelon](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="d461a-173">Gå til **Parametre**, og dobbeltklik på posten.</span><span class="sxs-lookup"><span data-stu-id="d461a-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparametre](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="d461a-175">Opdater følgende felter:</span><span class="sxs-lookup"><span data-stu-id="d461a-175">Update the following fields:</span></span>

 - <span data-ttu-id="d461a-176">**Standardvirksomhed**: USPM</span><span class="sxs-lookup"><span data-stu-id="d461a-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="d461a-177">**Standardafdeling**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="d461a-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="d461a-178">**Fakturafrekvens**: Hver syvende og sidste dag</span><span class="sxs-lookup"><span data-stu-id="d461a-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="d461a-179">**Arbejdstidsskabelon**: Skift til den skabelon, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="d461a-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="d461a-180">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d461a-180">Select **Save**.</span></span> 

![Opdater projektparametre](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]