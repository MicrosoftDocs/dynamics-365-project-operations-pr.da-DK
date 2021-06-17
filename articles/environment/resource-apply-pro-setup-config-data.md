---
title: Konfigurer og anvend konfigurationsdata i Common Data Service
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer og anvender demonstrationskonfiguration og konfigurationsdata i Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001284"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="5629a-103">Konfigurer og anvend konfigurationsdata i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5629a-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="5629a-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="5629a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="5629a-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="5629a-105">Prerequisites</span></span>

<span data-ttu-id="5629a-106">Før du begynder at konfigurere data i Common Data Service (CDS), skal følgende forudsætninger være opfyldt:</span><span class="sxs-lookup"><span data-stu-id="5629a-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="5629a-107">Klargør et CDS-miljø og et Dynamics 365 Finance-miljø til Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5629a-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="5629a-108">Oplysninger om juridiske enheder fra Dynamics 365 Finance deles med CDS-miljøet.</span><span class="sxs-lookup"><span data-stu-id="5629a-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="5629a-109">Dette betyder, at objektet **Virksomehd** i CDS indeholder følgende firmaposter:</span><span class="sxs-lookup"><span data-stu-id="5629a-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="5629a-110">THPM</span><span class="sxs-lookup"><span data-stu-id="5629a-110">THPM</span></span>
  - <span data-ttu-id="5629a-111">USPM</span><span class="sxs-lookup"><span data-stu-id="5629a-111">USPM</span></span>
  - <span data-ttu-id="5629a-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="5629a-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="5629a-113">Installer konfiguration og konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="5629a-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="5629a-114">Hent, fjern blokeringen af, og udpak [Installations- og konfigurationsdatapakken](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="5629a-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="5629a-115">Naviger til den zippede mappe og kør den eksekverbare fil *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="5629a-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="5629a-116">På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="5629a-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="5629a-118">På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.</span><span class="sxs-lookup"><span data-stu-id="5629a-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="5629a-119">Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="5629a-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="5629a-120">Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg **Logon**.</span><span class="sxs-lookup"><span data-stu-id="5629a-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Log på konfiguration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="5629a-122">På side 3 skal du på lejeren vælge den organisation, som du vil importere demonstrationsdataene til, på listen over organisationer og vælge **Login**.</span><span class="sxs-lookup"><span data-stu-id="5629a-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="5629a-123">På side 4 skal du vælge zip-filen *SampleSetupAndConfigData* fra den udpakkede mappe.</span><span class="sxs-lookup"><span data-stu-id="5629a-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Valg af zip-fil](./media/3ZipFile.png)

![Vælg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="5629a-126">Når zip-filen er valgt, skal du vælge **Importér data**.</span><span class="sxs-lookup"><span data-stu-id="5629a-126">After the zip file is selected, select **Import Data**.</span></span>

![Importér data](./media/5ImportData.png)

10. <span data-ttu-id="5629a-128">Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden.</span><span class="sxs-lookup"><span data-stu-id="5629a-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="5629a-129">Afslut CMT-guiden, når importen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="5629a-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="5629a-130">Kontrollér, om der er data i organisationen i følgende 26 objekter:</span><span class="sxs-lookup"><span data-stu-id="5629a-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="5629a-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="5629a-131">Currency</span></span>
  - <span data-ttu-id="5629a-132">Kontoplan</span><span class="sxs-lookup"><span data-stu-id="5629a-132">Chart of Accounts</span></span>
  - <span data-ttu-id="5629a-133">Regnskabskalender</span><span class="sxs-lookup"><span data-stu-id="5629a-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="5629a-134">Typer af valutakurser</span><span class="sxs-lookup"><span data-stu-id="5629a-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="5629a-135">Betalingsdag</span><span class="sxs-lookup"><span data-stu-id="5629a-135">Payment Day</span></span>
  - <span data-ttu-id="5629a-136">Betalingsplan</span><span class="sxs-lookup"><span data-stu-id="5629a-136">Payment Schedule</span></span>
  - <span data-ttu-id="5629a-137">Betalingsbetingelse</span><span class="sxs-lookup"><span data-stu-id="5629a-137">Payment Term</span></span>
  - <span data-ttu-id="5629a-138">Afdeling</span><span class="sxs-lookup"><span data-stu-id="5629a-138">Organizational Unit</span></span>
  - <span data-ttu-id="5629a-139">Kontakt</span><span class="sxs-lookup"><span data-stu-id="5629a-139">Contact</span></span>
  - <span data-ttu-id="5629a-140">Momsgruppe</span><span class="sxs-lookup"><span data-stu-id="5629a-140">Tax Group</span></span>
  - <span data-ttu-id="5629a-141">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="5629a-141">Customer Group</span></span>
  - <span data-ttu-id="5629a-142">Leverandørgruppe</span><span class="sxs-lookup"><span data-stu-id="5629a-142">Vendor Group</span></span>
  - <span data-ttu-id="5629a-143">Enhed</span><span class="sxs-lookup"><span data-stu-id="5629a-143">Unit</span></span>
  - <span data-ttu-id="5629a-144">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="5629a-144">Unit Group</span></span>
  - <span data-ttu-id="5629a-145">Prisliste</span><span class="sxs-lookup"><span data-stu-id="5629a-145">Price List</span></span>
  - <span data-ttu-id="5629a-146">Prisliste for projektparameter</span><span class="sxs-lookup"><span data-stu-id="5629a-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="5629a-147">Fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="5629a-147">Invoice Frequency</span></span>
  - <span data-ttu-id="5629a-148">Kategori af reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="5629a-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="5629a-149">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="5629a-149">Transaction Category</span></span>
  - <span data-ttu-id="5629a-150">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="5629a-150">Expense Category</span></span>
  - <span data-ttu-id="5629a-151">Rollepris</span><span class="sxs-lookup"><span data-stu-id="5629a-151">Role Price</span></span>
  - <span data-ttu-id="5629a-152">Transaktionskategoripris</span><span class="sxs-lookup"><span data-stu-id="5629a-152">Transaction Category Price</span></span>
  - <span data-ttu-id="5629a-153">Egenskab</span><span class="sxs-lookup"><span data-stu-id="5629a-153">Characteristic</span></span>
  - <span data-ttu-id="5629a-154">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="5629a-154">Bookable Resource</span></span>
  - <span data-ttu-id="5629a-155">Tilknytning for reserverbar ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="5629a-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="5629a-156">Egenskab for reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="5629a-156">Bookable Resource Characteristic</span></span>

![Fuldført import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="5629a-158">Opdater konfigurationer for Project Operations</span><span class="sxs-lookup"><span data-stu-id="5629a-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="5629a-159">Naviger til CE-miljø.</span><span class="sxs-lookup"><span data-stu-id="5629a-159">Navigate to the CE environment.</span></span> <span data-ttu-id="5629a-160">Du kan finde det ved at åbne [Power Platform Administration](https://admin.powerplatform.microsoft.com/environments), vælge miljøet og derefter vælge **Åbn miljø**.</span><span class="sxs-lookup"><span data-stu-id="5629a-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Åbn miljø](./media/7OpenEnvironment.png)

2. <span data-ttu-id="5629a-162">Gå til **Projekter** > **Ressourcer**, og vælg derefter **Ny** for at oprette en reserverbar ressource til brugeren.</span><span class="sxs-lookup"><span data-stu-id="5629a-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Reserverbare ressourcer](./media/8BookableResources.png)

3. <span data-ttu-id="5629a-164">På fanen **Generelt** skal du vælge din administratorbruger.</span><span class="sxs-lookup"><span data-stu-id="5629a-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="5629a-165">Kontroller, at tidszonen stemmer overens med den, du befinder dig i.</span><span class="sxs-lookup"><span data-stu-id="5629a-165">Verify that the time zone matches the one you are in.</span></span> 

![Ny reserverbar ressource](./media/9NewBookableResource.png)

4. <span data-ttu-id="5629a-167">På fanen **Planlægning** skal du i feltet **Virksomhed** vælge virksomheden **USPM** og derefter vælge **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5629a-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planlægningsfane](./media/10SchedulingTab.png)

5. <span data-ttu-id="5629a-169">Vælg fanen **Arbejdstid**.</span><span class="sxs-lookup"><span data-stu-id="5629a-169">Select the **Work hours** tab.</span></span>  

![Arbejdstimer](./media/11WorkHours.png)

6. <span data-ttu-id="5629a-171">Dobbeltklik på en vilkårlig værdi i kalenderen, og vælg **Rediger** > **Alle arrangementer i serien**.</span><span class="sxs-lookup"><span data-stu-id="5629a-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbejdskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="5629a-173">Skift arbejdstid til en otte (8) timer arbejdsdag, markér weekender som ikke-arbejdsdage, og kontrollér, at tidszonen stemmer overens med din.</span><span class="sxs-lookup"><span data-stu-id="5629a-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="5629a-174">Vælg **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="5629a-174">Select **Save and close**.</span></span>

![Opdater kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="5629a-176">Gå til **Indstillinger** > **Kalenderskabeloner**, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5629a-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalenderskabeloner](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="5629a-178">Angiv et navn, vælg den skabelonressource, du har oprettet, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5629a-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Gem kalenderskabelon](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="5629a-180">Gå til **Parametre**, og dobbeltklik på posten.</span><span class="sxs-lookup"><span data-stu-id="5629a-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparametre](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="5629a-182">Opdater følgende felter:</span><span class="sxs-lookup"><span data-stu-id="5629a-182">Update the following fields:</span></span>

 - <span data-ttu-id="5629a-183">**Standardvirksomhed**: USPM</span><span class="sxs-lookup"><span data-stu-id="5629a-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="5629a-184">**Standardafdeling**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="5629a-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="5629a-185">**Fakturafrekvens**: Hver syvende og sidste dag</span><span class="sxs-lookup"><span data-stu-id="5629a-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="5629a-186">**Arbejdstidsskabelon**: Skift til den skabelon, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="5629a-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="5629a-187">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5629a-187">Select **Save**.</span></span> 

![Opdater projektparametre](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
