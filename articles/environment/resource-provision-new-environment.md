---
title: Klargør et nyt miljø
description: Dette emne indeholder oplysninger om, hvordan du klargør et nyt Project Operations-miljø.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727783"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="58844-103">Klargør et nyt miljø</span><span class="sxs-lookup"><span data-stu-id="58844-103">Provision a new environment</span></span>

<span data-ttu-id="58844-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="58844-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="58844-105">Dette emne indeholder oplysninger om, hvordan du klargør et nyt Dynamics 365 Project Operations-miljø til ressource/ikke-lagerbaserede scenarier.</span><span class="sxs-lookup"><span data-stu-id="58844-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="58844-106">Aktivér automatisk klargøring af Project Operations i et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="58844-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="58844-107">Benyt følgende fremgangsmåde for at aktivere den automatiserede klargøring af Project Operations for dit LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="58844-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="58844-108">Gå til [LCS](https://lcs.dynamics.com/v2), og vælg feltet **Administration af prøveversionsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="58844-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="58844-109">I listen **Prøveversionsfunktion** skal du vælge **Funktionen Project Operations** og dernæst vælge **Aktiver prøveversionsfunktion** for at aktivere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="58844-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="58844-110">Dette trin udføres kun én gang pr. LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="58844-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="58844-111">Klargør et Project Operations-miljø</span><span class="sxs-lookup"><span data-stu-id="58844-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="58844-112">Åbn en udrulning af et [demonstrationsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller [sandkasse-/produktionsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="58844-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="58844-113">Gennemgå guiden **Miljøklargøring**.</span><span class="sxs-lookup"><span data-stu-id="58844-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="58844-114">Kontrollér, at den valgte programversion er 10.0.13 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="58844-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="58844-115">Hvis du vil klargøre Project Operations, skal du vælge **Avancerede indstillinger** og vælge **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="58844-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="58844-116">Aktiver **Common Data Service-indstillingen** ved at vælge **Ja** og derefter angive oplysninger i de påkrævede felter:</span><span class="sxs-lookup"><span data-stu-id="58844-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="58844-117">Navn</span><span class="sxs-lookup"><span data-stu-id="58844-117">Name</span></span>
  - <span data-ttu-id="58844-118">Land/område</span><span class="sxs-lookup"><span data-stu-id="58844-118">Region</span></span>
  - <span data-ttu-id="58844-119">Sprog</span><span class="sxs-lookup"><span data-stu-id="58844-119">Language</span></span>
  - <span data-ttu-id="58844-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="58844-120">Currency</span></span>
 
5. <span data-ttu-id="58844-121">I feltet **Common Data Service-skabelon** skal du vælge **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="58844-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="58844-122">Vælg miljøtypen til din udrulning.</span><span class="sxs-lookup"><span data-stu-id="58844-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="58844-123">En abonnementsbaseret prøveversion giver dig mulighed for at installere et CDS-miljø i 30 dage.</span><span class="sxs-lookup"><span data-stu-id="58844-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Udrulningsindstillinger](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="58844-125">Vælg **Accepter** for at bekræfte servicebetingelserne, og vælg derefter **Udfør** for at vende tilbage til udrulningsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="58844-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Samtykke til udrulning](./media/2DeploymentConsent.png)

7. <span data-ttu-id="58844-127">Valgfrit - Anvend demodata på miljøet.</span><span class="sxs-lookup"><span data-stu-id="58844-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="58844-128">Gå til **Avancerede indstillinger**, vælg **Tilpas SQL-databasekonfiguration**, og angiv **Angiv et datasæt for applikationsdatabase** til **Demo**.</span><span class="sxs-lookup"><span data-stu-id="58844-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="58844-129">Udfyld de resterende obligatoriske felter i guiden, og bekræft udrulningen.</span><span class="sxs-lookup"><span data-stu-id="58844-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="58844-130">Den tid, det tager at klargøre miljøet, varierer, afhængigt af miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="58844-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="58844-131">Klargøringen kan tage op til seks timer.</span><span class="sxs-lookup"><span data-stu-id="58844-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="58844-132">Når udrulningen er fuldført, vises miljøet som **Udrullet**.</span><span class="sxs-lookup"><span data-stu-id="58844-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="58844-133">Du kan kontrollere, at miljøet er blevet udrullet korrekt ved at vælge **Logon** og logge på miljøet.</span><span class="sxs-lookup"><span data-stu-id="58844-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detaljer for -miljø](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="58844-135">Anvend opdateringer på Finance-miljøet</span><span class="sxs-lookup"><span data-stu-id="58844-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="58844-136">Project Operations kræver et Finance-miljø med programversion **10.0.13 (10.0.569.20009)** eller nyere.</span><span class="sxs-lookup"><span data-stu-id="58844-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="58844-137">Det kan være nødvendigt at anvende kvalitetsopdateringer i dit Finance-miljø for at modtage denne version.</span><span class="sxs-lookup"><span data-stu-id="58844-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="58844-138">I LCS skal du på siden **Miljødetaljer** i sektionen **Tilgængelige opdateringer** vælge **Vis opdatering**.</span><span class="sxs-lookup"><span data-stu-id="58844-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Vis opdateringer](./media/5ViewUpdates.png)

2. <span data-ttu-id="58844-140">På siden **Binære opdateringer** skal du vælge **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="58844-140">On the **Binary updates** page, select **Save package.**</span></span>

![Gem pakke](./media/6SavePackage.png)

3. <span data-ttu-id="58844-142">Klik på **Vælg alle** og vælg derefter **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="58844-142">Click **Select all** and then select **Save package**.</span></span>

![Gennemse og gem opdateringer](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="58844-144">Angiv et navn for og en beskrivelse af pakken, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="58844-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="58844-145">Afhængigt af internetforbindelsen kan denne proces tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="58844-145">Depending on the internet connection, this process might take some time.</span></span>

![Overfør pakken til aktivbiblioteket](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="58844-147">Når pakken er blevet gemt, skal du vælge **Udført** og gemme denne pakke i aktivbiblioteket i dit LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="58844-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="58844-148">Det kan tage op til mere end 15 minutter at gemme og validere pakken.</span><span class="sxs-lookup"><span data-stu-id="58844-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="58844-149">Hvis du vil anvende opdateringen, skal du gå til siden med **Miljødetaljer** i LCS og vælge **Vedligehold** > **Anvend opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="58844-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vedligehold miljøer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="58844-151">Vælg den pakke, du har oprettet, på listen over opdateringer, og vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="58844-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Anvend opdateringer](./media/10ApplyUpdates.png)

<span data-ttu-id="58844-153">Det vil tage et stykke tid at vedligeholde miljøet.</span><span class="sxs-lookup"><span data-stu-id="58844-153">Environment servicing will take some time.</span></span> <span data-ttu-id="58844-154">Når installationen er fuldført, vil miljøet vende tilbage til en udrullet tilstand.</span><span class="sxs-lookup"><span data-stu-id="58844-154">After it is complete, the environment will return to a deployed state.</span></span>

![Udrullet miljø](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="58844-156">Opret en forbindelse til dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="58844-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="58844-157">I dit LCS-projekt skal du gå til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="58844-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="58844-158">Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="58844-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="58844-159">Når forbindelsen er oprettet, skal du vælge **Forbind til CDS for Apps** igen.</span><span class="sxs-lookup"><span data-stu-id="58844-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="58844-160">Du bliver omdirigeret til dobbelt skrivning i Finance.</span><span class="sxs-lookup"><span data-stu-id="58844-160">You will be redirected to Dual Write in Finance.</span></span>

![Link til CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="58844-162">Vælg **Anvend løsning** for at få adgang til de objekter, der skal tilknyttes i integrationen.</span><span class="sxs-lookup"><span data-stu-id="58844-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Anvend løsninger](./media/13ApplySolutions.png)

5. <span data-ttu-id="58844-164">Vælg begge løsninger, **Dynamics 365 Finance and Operations - dobbeltskrivning af objekttilknytningdobbelt** og **Dynamics 365 Project Operations - dobbeltskrivning af objekttilknytningdobbelt**, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="58844-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekræft løsninger](./media/14ConfirmSolutions.png)

<span data-ttu-id="58844-166">Når løsningerne er anvendt, anvendes dobbelt skrivningsobjekter på miljøet.</span><span class="sxs-lookup"><span data-stu-id="58844-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Anvendelse af løsninger](./media/15ApplyingSolutions.png)

<span data-ttu-id="58844-168">Når objekterne er anvendt, vises alle tilgængelige tilknytninger i miljøet.</span><span class="sxs-lookup"><span data-stu-id="58844-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Dobbelt skrivningstilknytninger](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="58844-170">Opdater dataobjekterne efter opdateringen</span><span class="sxs-lookup"><span data-stu-id="58844-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="58844-171">I Finance skal du gå til arbejdsområdet **Dataadministration**.</span><span class="sxs-lookup"><span data-stu-id="58844-171">In Finance, go to the **Data management** workspace.</span></span>

![Arbejdsområde for Dataadministration](./media/16DataManagement.png)

2. <span data-ttu-id="58844-173">Vælg feltet **Strukturparametre**.</span><span class="sxs-lookup"><span data-stu-id="58844-173">Select the **Framework parameters** tile.</span></span>

![Strukturparametre](./media/17FrameworkParameters.png)

3. <span data-ttu-id="58844-175">På siden **Objektindstillinger** skal du vælge **Opdater objektliste**.</span><span class="sxs-lookup"><span data-stu-id="58844-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Opdater objektliste](./media/18RefreshEntityList.png)

<span data-ttu-id="58844-177">Opdateringen tager ca. 20 minutter.</span><span class="sxs-lookup"><span data-stu-id="58844-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="58844-178">Du modtager en besked, når den er fuldført.</span><span class="sxs-lookup"><span data-stu-id="58844-178">You will receive an alert when it is complete.</span></span>

![Opdater bekræftelse](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="58844-180">Opdater sikkerhedsindstillingerne for Project Operations på Dataverse</span><span class="sxs-lookup"><span data-stu-id="58844-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="58844-181">Gå til Project Operations på dit Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="58844-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="58844-182">Gå til **Indstillinger** > **Sikkerhed** > **Sikkerhedsroller**.</span><span class="sxs-lookup"><span data-stu-id="58844-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="58844-183">På siden **Sikkerhedsroller** skal du fra listen med roller vælge **applikationsbruger med dobbeltskrivning** og vælge fanen **Brugerdefinerede objekter**.</span><span class="sxs-lookup"><span data-stu-id="58844-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="58844-184">Kontrollér, at rollen har tilladelserne **Læse** og **Tilføj til** for:</span><span class="sxs-lookup"><span data-stu-id="58844-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="58844-185">**Type af valutakurs**</span><span class="sxs-lookup"><span data-stu-id="58844-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="58844-186">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="58844-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="58844-187">**Regnskabskalender**</span><span class="sxs-lookup"><span data-stu-id="58844-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="58844-188">**Hovedbog**</span><span class="sxs-lookup"><span data-stu-id="58844-188">**Ledger**</span></span>

5. <span data-ttu-id="58844-189">Når sikkerhedsrollen er blevet opdateret, skal du gå til **Indstillinger** > **Sikkerhed** > **Teams** og vælge standardteamet i teamvisningen **Lokal virksomhedsejer**.</span><span class="sxs-lookup"><span data-stu-id="58844-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="58844-190">Vælg **Administrer roller**, og kontrollér, at sikkerhedsrettigheden **applikationsbruger med dobbeltskrivning** gælder for dette team.</span><span class="sxs-lookup"><span data-stu-id="58844-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="58844-191">Kør Project Operations dobbelt skrivningstilknytninger</span><span class="sxs-lookup"><span data-stu-id="58844-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="58844-192">I dit LCS-projekt skal du gå til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="58844-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="58844-193">Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="58844-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="58844-194">Når du har valgt forbindelsen, bliver du omdirigeret til listen over objekter i tilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="58844-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="58844-195">Start tilknytningerne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="58844-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="58844-196">Sørg for at følge rækkefølgen på listen.</span><span class="sxs-lookup"><span data-stu-id="58844-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="58844-197">**Objekttilknytning**</span><span class="sxs-lookup"><span data-stu-id="58844-197">**Entity Map**</span></span> | <span data-ttu-id="58844-198">**Opdater enhed**</span><span class="sxs-lookup"><span data-stu-id="58844-198">**Refresh entity**</span></span> | <span data-ttu-id="58844-199">**Første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="58844-199">**Initial sync**</span></span> | <span data-ttu-id="58844-200">**Master til første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="58844-200">**Master for initial sync**</span></span> | <span data-ttu-id="58844-201">**Kør forudsætninger**</span><span class="sxs-lookup"><span data-stu-id="58844-201">**Run prerequisites**</span></span> | <span data-ttu-id="58844-202">**Forudsætning for første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="58844-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="58844-203">**Projektressourceroller for alle firmaer (reserverbareressourcekategorier)**</span><span class="sxs-lookup"><span data-stu-id="58844-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="58844-204">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-204">No</span></span> | <span data-ttu-id="58844-205">Ja</span><span class="sxs-lookup"><span data-stu-id="58844-205">Yes</span></span> | <span data-ttu-id="58844-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="58844-206">Common Data Service</span></span> | <span data-ttu-id="58844-207">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-207">No</span></span> | <span data-ttu-id="58844-208">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-208">N\A</span></span> |
| <span data-ttu-id="58844-209">**Juridiske enheder (cdm\_virksomheder)**</span><span class="sxs-lookup"><span data-stu-id="58844-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="58844-210">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-210">No</span></span> | <span data-ttu-id="58844-211">Ja</span><span class="sxs-lookup"><span data-stu-id="58844-211">Yes</span></span> | <span data-ttu-id="58844-212">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="58844-212">Finance and Operations apps</span></span> | <span data-ttu-id="58844-213">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-213">No</span></span> | <span data-ttu-id="58844-214">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-214">N\A</span></span> |
| <span data-ttu-id="58844-215">**Hovedbog (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="58844-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="58844-216">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-216">No</span></span> | <span data-ttu-id="58844-217">Ja</span><span class="sxs-lookup"><span data-stu-id="58844-217">Yes</span></span> | <span data-ttu-id="58844-218">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="58844-218">Finance and Operations apps</span></span> | <span data-ttu-id="58844-219">Ja</span><span class="sxs-lookup"><span data-stu-id="58844-219">Yes</span></span> | <span data-ttu-id="58844-220">Ja, Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="58844-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="58844-221">**Integration af faktiske oplysninger i Project Operations (msdyn\_faktiske oplysninger)**</span><span class="sxs-lookup"><span data-stu-id="58844-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="58844-222">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-222">No</span></span> | <span data-ttu-id="58844-223">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-223">No</span></span> | <span data-ttu-id="58844-224">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-224">N\A</span></span> | <span data-ttu-id="58844-225">Ja</span><span class="sxs-lookup"><span data-stu-id="58844-225">Yes</span></span> | <span data-ttu-id="58844-226">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-226">No</span></span> |
| <span data-ttu-id="58844-227">**Projekkontraktlinjer (salgsordredetaljer)**</span><span class="sxs-lookup"><span data-stu-id="58844-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="58844-228">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-228">No</span></span> | <span data-ttu-id="58844-229">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-229">No</span></span> | <span data-ttu-id="58844-230">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-230">N\A</span></span> | <span data-ttu-id="58844-231">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-231">No</span></span> | <span data-ttu-id="58844-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-232">No</span></span> |
| <span data-ttu-id="58844-233">**Integrationsobjekt for projekttransaktionsrelationer (msdyn\_transaktionsforbindelser)**</span><span class="sxs-lookup"><span data-stu-id="58844-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="58844-234">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-234">No</span></span> | <span data-ttu-id="58844-235">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-235">No</span></span> | <span data-ttu-id="58844-236">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-236">N\A</span></span> | <span data-ttu-id="58844-237">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-237">No</span></span> | <span data-ttu-id="58844-238">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-238">N\A</span></span> |
| <span data-ttu-id="58844-239">**Integration af kontraktlinjemilepæle i Project Operations (msdyn\_kontraktlinjeplanmedværdier)**</span><span class="sxs-lookup"><span data-stu-id="58844-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="58844-240">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-240">No</span></span> | <span data-ttu-id="58844-241">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-241">No</span></span> | <span data-ttu-id="58844-242">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-242">N\A</span></span> | <span data-ttu-id="58844-243">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-243">No</span></span> | <span data-ttu-id="58844-244">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-244">N\A</span></span> |
| <span data-ttu-id="58844-245">**Integrationsobjekt for udgiftsestimater i Project Operations (msdyn\_estimeredelinjer)**</span><span class="sxs-lookup"><span data-stu-id="58844-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="58844-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-246">No</span></span> | <span data-ttu-id="58844-247">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-247">No</span></span> | <span data-ttu-id="58844-248">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-248">N\A</span></span> | <span data-ttu-id="58844-249">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-249">No</span></span> | <span data-ttu-id="58844-250">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-250">N\A</span></span> |
| <span data-ttu-id="58844-251">**Integrationsobjekt for eksport af projektudgiftskategorier i Project Operations (msdyn\_udgiftskategorier)**</span><span class="sxs-lookup"><span data-stu-id="58844-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="58844-252">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-252">No</span></span> | <span data-ttu-id="58844-253">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-253">No</span></span> | <span data-ttu-id="58844-254">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-254">N\A</span></span> | <span data-ttu-id="58844-255">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-255">No</span></span> | <span data-ttu-id="58844-256">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-256">N\A</span></span> |
| <span data-ttu-id="58844-257">**Integrationsobjekt for eksport af projektudgifter i Project Operations (msdyn\_udgifter)**</span><span class="sxs-lookup"><span data-stu-id="58844-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="58844-258">Ja</span><span class="sxs-lookup"><span data-stu-id="58844-258">Yes</span></span> | <span data-ttu-id="58844-259">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-259">No</span></span> | <span data-ttu-id="58844-260">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-260">N\A</span></span> | <span data-ttu-id="58844-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-261">No</span></span> | <span data-ttu-id="58844-262">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-262">N\A</span></span> |
| <span data-ttu-id="58844-263">**Integrationsobjekt for timeestimater i Project Operations (msdyn\_ressourcetildelinger)**</span><span class="sxs-lookup"><span data-stu-id="58844-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="58844-264">Ja</span><span class="sxs-lookup"><span data-stu-id="58844-264">Yes</span></span> | <span data-ttu-id="58844-265">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-265">No</span></span> | <span data-ttu-id="58844-266">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-266">N\A</span></span> | <span data-ttu-id="58844-267">Nr.</span><span class="sxs-lookup"><span data-stu-id="58844-267">No</span></span> | <span data-ttu-id="58844-268">I\R</span><span class="sxs-lookup"><span data-stu-id="58844-268">N\A</span></span> |


4. <span data-ttu-id="58844-269">Hvis du vil opdatere objektet, skal du vælge tilknytningens navn og derefter vælge **Opdater objekter**.</span><span class="sxs-lookup"><span data-stu-id="58844-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Opdater tilknytning](./media/20RefreshMapping.png)

5. <span data-ttu-id="58844-271">Kør tilknytningen, når opdateringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="58844-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="58844-272">Før du aktiverer næste tilknytning, skal du kontrollere, at tilknytningen i tabellen er i tilstanden **Kører**.</span><span class="sxs-lookup"><span data-stu-id="58844-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="58844-273">Det kan tage et stykke tid at køre tilknytningerne med et større antal forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="58844-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="58844-274">Hvis du vil køre en tilknytning med forudsætninger, skal du aktivere funktionen **Vis relaterede objekttilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="58844-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="58844-275">Hvis tabellen indikerer, at **Indledende synkronisering af forudsætning** er **Nej**, skal du kontrollere, at flaget for den **Indledende synkronisering** er **Slået fra** i alle de påkrævede tilknytninger, før du kører programmet.</span><span class="sxs-lookup"><span data-stu-id="58844-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kør tilknytning](./media/21RunMap.png)

6. <span data-ttu-id="58844-277">Valider, at alle projektrelaterede tilknytninger er i kørselstilstand.</span><span class="sxs-lookup"><span data-stu-id="58844-277">Validate all project related maps are in the running state.</span></span>

![Alle tilknytninger kører](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="58844-279">Anvend konfigurationsdata i CDS for Project Operations (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="58844-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="58844-280">Hvis du har anvendt demodata i Finance-miljøet, skal du se [Konfigurere og anvende konfigurationsdata i Common Data Service til Project Operations](resource-apply-pro-setup-config-data.md) for at anvende demodata i CDS-miljøer.</span><span class="sxs-lookup"><span data-stu-id="58844-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="58844-281">Dit Project Operations-miljø er nu klargjort og konfigureret.</span><span class="sxs-lookup"><span data-stu-id="58844-281">Your Project Operations environment is now provisioned and configured.</span></span> 
