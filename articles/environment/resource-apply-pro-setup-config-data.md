---
title: Konfigurer og anvend konfigurationsdata i Common Data Service for Project Operations
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer og anvender demonstrationskonfiguration og konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074045"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="c5c41-103">Konfigurer og anvend konfigurationsdata i Common Data Service for Project Operations</span><span class="sxs-lookup"><span data-stu-id="c5c41-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="c5c41-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="c5c41-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="c5c41-105">Installer konfiguration og konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="c5c41-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="c5c41-106">Hent, fjern blokeringen af, og udpak [Installations- og konfigurationsdatapakken](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="c5c41-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="c5c41-107">Naviger til den zippede mappe og kør den eksekverbare fil *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="c5c41-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="c5c41-108">På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="c5c41-110">På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="c5c41-111">Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="c5c41-112">Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg **Logon**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Log på konfiguration](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="c5c41-114">På side 3 skal du på lejeren vælge den organisation, som du vil importere demonstrationsdataene til, på listen over organisationer og vælge **Login**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="c5c41-115">På side 4 skal du vælge zip-filen *SampleSetupAndConfigData* fra den udpakkede mappe.</span><span class="sxs-lookup"><span data-stu-id="c5c41-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Valg af zip-fil](./media/3ZipFile.png)

![Vælg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="c5c41-118">Når zip-filen er valgt, skal du vælge **Importér data**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-118">After the zip file is selected, select **Import Data**.</span></span>

![Importér data](./media/5ImportData.png)

10. <span data-ttu-id="c5c41-120">Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden.</span><span class="sxs-lookup"><span data-stu-id="c5c41-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="c5c41-121">Afslut CMT-guiden, når importen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="c5c41-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="c5c41-122">Kontrollér, om der er data i organisationen i følgende 19 objekter:</span><span class="sxs-lookup"><span data-stu-id="c5c41-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="c5c41-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="c5c41-123">Currency</span></span>
  - <span data-ttu-id="c5c41-124">Afdeling</span><span class="sxs-lookup"><span data-stu-id="c5c41-124">Organizational Unit</span></span>
  - <span data-ttu-id="c5c41-125">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="c5c41-125">Contact</span></span>
  - <span data-ttu-id="c5c41-126">Momsgruppe</span><span class="sxs-lookup"><span data-stu-id="c5c41-126">Tax Group</span></span>
  - <span data-ttu-id="c5c41-127">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="c5c41-127">Customer Group</span></span>
  - <span data-ttu-id="c5c41-128">Enhed</span><span class="sxs-lookup"><span data-stu-id="c5c41-128">Unit</span></span>
  - <span data-ttu-id="c5c41-129">Enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="c5c41-129">Unit Group</span></span>
  - <span data-ttu-id="c5c41-130">Prisliste</span><span class="sxs-lookup"><span data-stu-id="c5c41-130">Price List</span></span>
  - <span data-ttu-id="c5c41-131">Prisliste for projektparameter</span><span class="sxs-lookup"><span data-stu-id="c5c41-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="c5c41-132">Fakturahyppighed</span><span class="sxs-lookup"><span data-stu-id="c5c41-132">Invoice Frequency</span></span>
  - <span data-ttu-id="c5c41-133">Kategori af reserverbare ressourcer</span><span class="sxs-lookup"><span data-stu-id="c5c41-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="c5c41-134">Transaktionskategori</span><span class="sxs-lookup"><span data-stu-id="c5c41-134">Transaction Category</span></span>
  - <span data-ttu-id="c5c41-135">Udgiftskategori</span><span class="sxs-lookup"><span data-stu-id="c5c41-135">Expense Category</span></span>
  - <span data-ttu-id="c5c41-136">Rollepris</span><span class="sxs-lookup"><span data-stu-id="c5c41-136">Role Price</span></span>
  - <span data-ttu-id="c5c41-137">Transaktionskategoripris</span><span class="sxs-lookup"><span data-stu-id="c5c41-137">Transaction Category Price</span></span>
  - <span data-ttu-id="c5c41-138">Egenskab</span><span class="sxs-lookup"><span data-stu-id="c5c41-138">Characteristic</span></span>
  - <span data-ttu-id="c5c41-139">Reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="c5c41-139">Bookable Resource</span></span>
  - <span data-ttu-id="c5c41-140">Tilknytning for reserverbar ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="c5c41-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="c5c41-141">Egenskab for reserverbar ressource</span><span class="sxs-lookup"><span data-stu-id="c5c41-141">Bookable Resource Characteristic</span></span>

![Fuldført import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="c5c41-143">Opdater konfigurationer for Project Operations</span><span class="sxs-lookup"><span data-stu-id="c5c41-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="c5c41-144">Naviger til CE-miljø.</span><span class="sxs-lookup"><span data-stu-id="c5c41-144">Navigate to the CE environment.</span></span> <span data-ttu-id="c5c41-145">Du kan finde det ved at åbne [Power Platform Administration](https://admin.powerplatform.microsoft.com/environments), vælge miljøet og derefter vælge **Åbn miljø**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Åbn miljø](./media/7OpenEnvironment.png)

2. <span data-ttu-id="c5c41-147">Gå til **Projekter** > **Ressourcer** , og vælg derefter **Ny** for at oprette en reserverbar ressource til brugeren.</span><span class="sxs-lookup"><span data-stu-id="c5c41-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Reserverbare ressourcer](./media/8BookableResources.png)

3. <span data-ttu-id="c5c41-149">På fanen **Generelt** skal du vælge din administratorbruger.</span><span class="sxs-lookup"><span data-stu-id="c5c41-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="c5c41-150">Kontroller, at tidszonen stemmer overens med den, du befinder dig i.</span><span class="sxs-lookup"><span data-stu-id="c5c41-150">Verify that the time zone matches the one you are in.</span></span> 

![Ny reserverbar ressource](./media/9NewBookableResource.png)

4. <span data-ttu-id="c5c41-152">På fanen **Planlægning** skal du i feltet **Virksomhed** vælge virksomheden **USPM** og derefter vælge **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planlægningsfane](./media/10SchedulingTab.png)

5. <span data-ttu-id="c5c41-154">Vælg fanen **Arbejdstid**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-154">Select the **Work hours** tab.</span></span>  

![Arbejdstimer](./media/11WorkHours.png)

6. <span data-ttu-id="c5c41-156">Dobbeltklik på en vilkårlig værdi i kalenderen, og vælg **Rediger** > **Alle arrangementer i serien**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbejdskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="c5c41-158">Skift arbejdstid til en otte (8) timer arbejdsdag, markér weekender som ikke-arbejdsdage, og kontrollér, at tidszonen stemmer overens med din.</span><span class="sxs-lookup"><span data-stu-id="c5c41-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="c5c41-159">Vælg **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-159">Select **Save and close**.</span></span>

![Opdater kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="c5c41-161">Gå til **Indstillinger** > **Kalenderskabeloner** , og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalenderskabeloner](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="c5c41-163">Angiv et navn, vælg den skabelonressource, du har oprettet, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Gem kalenderskabelon](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="c5c41-165">Gå til **Parametre** , og dobbeltklik på posten.</span><span class="sxs-lookup"><span data-stu-id="c5c41-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparametre](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="c5c41-167">Opdater følgende felter:</span><span class="sxs-lookup"><span data-stu-id="c5c41-167">Update the following fields:</span></span>

 - <span data-ttu-id="c5c41-168">**Standardvirksomhed** : USPM</span><span class="sxs-lookup"><span data-stu-id="c5c41-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="c5c41-169">**Standardafdeling** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="c5c41-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="c5c41-170">**Fakturafrekvens** : Hver syvende og sidste dag</span><span class="sxs-lookup"><span data-stu-id="c5c41-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="c5c41-171">**Arbejdstidsskabelon** : Skift til den skabelon, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="c5c41-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="c5c41-172">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c5c41-172">Select **Save**.</span></span> 

![Opdater projektparametre](./media/17UpdatedProjectParameters.png)
