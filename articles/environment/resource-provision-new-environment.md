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
ms.openlocfilehash: 50e623d3716c9dd03ce34ec293ba57b5d966d39e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276881"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="22e80-103">Klargør et nyt miljø</span><span class="sxs-lookup"><span data-stu-id="22e80-103">Provision a new environment</span></span>

<span data-ttu-id="22e80-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="22e80-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="22e80-105">Dette emne indeholder oplysninger om, hvordan du klargør et nyt Dynamics 365 Project Operations-miljø til ressource/ikke-lagerbaserede scenarier.</span><span class="sxs-lookup"><span data-stu-id="22e80-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="22e80-106">Aktivér automatisk klargøring af Project Operations i et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="22e80-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="22e80-107">Benyt følgende fremgangsmåde for at aktivere den automatiserede klargøring af Project Operations for dit LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="22e80-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="22e80-108">Gå til [LCS](https://lcs.dynamics.com/v2), og vælg feltet **Administration af prøveversionsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="22e80-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="22e80-109">I listen **Prøveversionsfunktion** skal du vælge **Funktionen Project Operations** og dernæst vælge **Aktiver prøveversionsfunktion** for at aktivere Project Operations.</span><span class="sxs-lookup"><span data-stu-id="22e80-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="22e80-110">Dette trin udføres kun én gang pr. LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="22e80-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="22e80-111">Klargør et Project Operations-miljø</span><span class="sxs-lookup"><span data-stu-id="22e80-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="22e80-112">Åbn en udrulning af et [demonstrationsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller [sandkasse-/produktionsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="22e80-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="22e80-113">Gennemgå guiden **Miljøklargøring**.</span><span class="sxs-lookup"><span data-stu-id="22e80-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="22e80-114">Kontrollér, at den valgte programversion er 10.0.13 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="22e80-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="22e80-115">Hvis du vil klargøre Project Operations, skal du vælge **Avancerede indstillinger** og vælge **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="22e80-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="22e80-116">Aktiver **Common Data Service-indstillingen** ved at vælge **Ja** og derefter angive oplysninger i de påkrævede felter:</span><span class="sxs-lookup"><span data-stu-id="22e80-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="22e80-117">Navn</span><span class="sxs-lookup"><span data-stu-id="22e80-117">Name</span></span>
  - <span data-ttu-id="22e80-118">Land/område</span><span class="sxs-lookup"><span data-stu-id="22e80-118">Region</span></span>
  - <span data-ttu-id="22e80-119">Sprog</span><span class="sxs-lookup"><span data-stu-id="22e80-119">Language</span></span>
  - <span data-ttu-id="22e80-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="22e80-120">Currency</span></span>
 
5. <span data-ttu-id="22e80-121">I feltet **Common Data Service-skabelon** skal du vælge **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="22e80-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="22e80-122">Vælg miljøtypen til din udrulning.</span><span class="sxs-lookup"><span data-stu-id="22e80-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="22e80-123">En abonnementsbaseret prøveversion giver dig mulighed for at installere et CDS-miljø i 30 dage.</span><span class="sxs-lookup"><span data-stu-id="22e80-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Udrulningsindstillinger](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="22e80-125">Vælg **Accepter** for at bekræfte servicebetingelserne, og vælg derefter **Udfør** for at vende tilbage til udrulningsindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="22e80-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Samtykke til udrulning](./media/2DeploymentConsent.png)

7. <span data-ttu-id="22e80-127">Valgfrit - Anvend demodata på miljøet.</span><span class="sxs-lookup"><span data-stu-id="22e80-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="22e80-128">Gå til **Avancerede indstillinger**, vælg **Tilpas SQL-databasekonfiguration**, og angiv **Angiv et datasæt for applikationsdatabase** til **Demo**.</span><span class="sxs-lookup"><span data-stu-id="22e80-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="22e80-129">Udfyld de resterende obligatoriske felter i guiden, og bekræft udrulningen.</span><span class="sxs-lookup"><span data-stu-id="22e80-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="22e80-130">Den tid, det tager at klargøre miljøet, varierer, afhængigt af miljøtypen.</span><span class="sxs-lookup"><span data-stu-id="22e80-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="22e80-131">Klargøringen kan tage op til seks timer.</span><span class="sxs-lookup"><span data-stu-id="22e80-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="22e80-132">Når udrulningen er fuldført, vises miljøet som **Udrullet**.</span><span class="sxs-lookup"><span data-stu-id="22e80-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="22e80-133">Du kan kontrollere, at miljøet er blevet udrullet korrekt ved at vælge **Logon** og logge på miljøet.</span><span class="sxs-lookup"><span data-stu-id="22e80-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detaljer for -miljø](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="22e80-135">Anvend opdateringer på Finance-miljøet</span><span class="sxs-lookup"><span data-stu-id="22e80-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="22e80-136">Project Operations kræver et Finance-miljø med programversion **10.0.13 (10.0.569.20009)** eller nyere.</span><span class="sxs-lookup"><span data-stu-id="22e80-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="22e80-137">Det kan være nødvendigt at anvende kvalitetsopdateringer i dit Finance-miljø for at modtage denne version.</span><span class="sxs-lookup"><span data-stu-id="22e80-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="22e80-138">I LCS skal du på siden **Miljødetaljer** i sektionen **Tilgængelige opdateringer** vælge **Vis opdatering**.</span><span class="sxs-lookup"><span data-stu-id="22e80-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Vis opdateringer](./media/5ViewUpdates.png)

2. <span data-ttu-id="22e80-140">På siden **Binære opdateringer** skal du vælge **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="22e80-140">On the **Binary updates** page, select **Save package.**</span></span>

![Gem pakke](./media/6SavePackage.png)

3. <span data-ttu-id="22e80-142">Klik på **Vælg alle** og vælg derefter **Gem pakke**.</span><span class="sxs-lookup"><span data-stu-id="22e80-142">Click **Select all** and then select **Save package**.</span></span>

![Gennemse og gem opdateringer](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="22e80-144">Angiv et navn for og en beskrivelse af pakken, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="22e80-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="22e80-145">Afhængigt af internetforbindelsen kan denne proces tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="22e80-145">Depending on the internet connection, this process might take some time.</span></span>

![Overfør pakken til aktivbiblioteket](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="22e80-147">Når pakken er blevet gemt, skal du vælge **Udført** og gemme denne pakke i aktivbiblioteket i dit LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="22e80-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="22e80-148">Det kan tage op til mere end 15 minutter at gemme og validere pakken.</span><span class="sxs-lookup"><span data-stu-id="22e80-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="22e80-149">Hvis du vil anvende opdateringen, skal du gå til siden med **Miljødetaljer** i LCS og vælge **Vedligehold** > **Anvend opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="22e80-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vedligehold miljøer](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="22e80-151">Vælg den pakke, du har oprettet, på listen over opdateringer, og vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="22e80-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Anvend opdateringer](./media/10ApplyUpdates.png)

<span data-ttu-id="22e80-153">Det vil tage et stykke tid at vedligeholde miljøet.</span><span class="sxs-lookup"><span data-stu-id="22e80-153">Environment servicing will take some time.</span></span> <span data-ttu-id="22e80-154">Når installationen er fuldført, vil miljøet vende tilbage til en udrullet tilstand.</span><span class="sxs-lookup"><span data-stu-id="22e80-154">After it is complete, the environment will return to a deployed state.</span></span>

![Udrullet miljø](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="22e80-156">Opret en forbindelse til dobbelt skrivning</span><span class="sxs-lookup"><span data-stu-id="22e80-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="22e80-157">I dit LCS-projekt skal du gå til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="22e80-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="22e80-158">Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="22e80-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="22e80-159">Når forbindelsen er oprettet, skal du vælge **Forbind til CDS for Apps** igen.</span><span class="sxs-lookup"><span data-stu-id="22e80-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="22e80-160">Du bliver omdirigeret til dobbelt skrivning i Finance.</span><span class="sxs-lookup"><span data-stu-id="22e80-160">You will be redirected to Dual Write in Finance.</span></span>

![Link til CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="22e80-162">Vælg **Anvend løsning** for at få adgang til de objekter, der skal tilknyttes i integrationen.</span><span class="sxs-lookup"><span data-stu-id="22e80-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Anvend løsninger](./media/13ApplySolutions.png)

5. <span data-ttu-id="22e80-164">Vælg begge løsninger, **Dynamics 365 Finance and Operations - dobbeltskrivning af objekttilknytningdobbelt** og **Dynamics 365 Project Operations - dobbeltskrivning af objekttilknytningdobbelt**, og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="22e80-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Bekræft løsninger](./media/14ConfirmSolutions.png)

<span data-ttu-id="22e80-166">Når løsningerne er anvendt, anvendes dobbelt skrivningsobjekter på miljøet.</span><span class="sxs-lookup"><span data-stu-id="22e80-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Anvendelse af løsninger](./media/15ApplyingSolutions.png)

<span data-ttu-id="22e80-168">Når objekterne er anvendt, vises alle tilgængelige tilknytninger i miljøet.</span><span class="sxs-lookup"><span data-stu-id="22e80-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Dobbelt skrivningstilknytninger](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="22e80-170">Opdater dataobjekterne efter opdateringen</span><span class="sxs-lookup"><span data-stu-id="22e80-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="22e80-171">I Finance skal du gå til arbejdsområdet **Dataadministration**.</span><span class="sxs-lookup"><span data-stu-id="22e80-171">In Finance, go to the **Data management** workspace.</span></span>

![Arbejdsområde for Dataadministration](./media/16DataManagement.png)

2. <span data-ttu-id="22e80-173">Vælg feltet **Strukturparametre**.</span><span class="sxs-lookup"><span data-stu-id="22e80-173">Select the **Framework parameters** tile.</span></span>

![Strukturparametre](./media/17FrameworkParameters.png)

3. <span data-ttu-id="22e80-175">På siden **Objektindstillinger** skal du vælge **Opdater objektliste**.</span><span class="sxs-lookup"><span data-stu-id="22e80-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Opdater objektliste](./media/18RefreshEntityList.png)

<span data-ttu-id="22e80-177">Opdateringen tager ca. 20 minutter.</span><span class="sxs-lookup"><span data-stu-id="22e80-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="22e80-178">Du modtager en besked, når den er fuldført.</span><span class="sxs-lookup"><span data-stu-id="22e80-178">You will receive an alert when it is complete.</span></span>

![Opdater bekræftelse](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="22e80-180">Opdater sikkerhedsindstillingerne for Project Operations på Dataverse</span><span class="sxs-lookup"><span data-stu-id="22e80-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="22e80-181">Gå til Project Operations på dit Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="22e80-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="22e80-182">Gå til **Indstillinger** > **Sikkerhed** > **Sikkerhedsroller**.</span><span class="sxs-lookup"><span data-stu-id="22e80-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="22e80-183">På siden **Sikkerhedsroller** skal du fra listen med roller vælge **applikationsbruger med dobbeltskrivning** og vælge fanen **Brugerdefinerede objekter**.</span><span class="sxs-lookup"><span data-stu-id="22e80-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="22e80-184">Kontrollér, at rollen har tilladelserne **Læse** og **Tilføj til** for:</span><span class="sxs-lookup"><span data-stu-id="22e80-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="22e80-185">**Type af valutakurs**</span><span class="sxs-lookup"><span data-stu-id="22e80-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="22e80-186">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="22e80-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="22e80-187">**Regnskabskalender**</span><span class="sxs-lookup"><span data-stu-id="22e80-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="22e80-188">**Hovedbog**</span><span class="sxs-lookup"><span data-stu-id="22e80-188">**Ledger**</span></span>

5. <span data-ttu-id="22e80-189">Når sikkerhedsrollen er blevet opdateret, skal du gå til **Indstillinger** > **Sikkerhed** > **Teams** og vælge standardteamet i teamvisningen **Lokal virksomhedsejer**.</span><span class="sxs-lookup"><span data-stu-id="22e80-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="22e80-190">Vælg **Administrer roller**, og kontrollér, at sikkerhedsrettigheden **applikationsbruger med dobbeltskrivning** gælder for dette team.</span><span class="sxs-lookup"><span data-stu-id="22e80-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="22e80-191">Kør Project Operations dobbelt skrivningstilknytninger</span><span class="sxs-lookup"><span data-stu-id="22e80-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="22e80-192">I dit LCS-projekt skal du gå til siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="22e80-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="22e80-193">Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="22e80-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="22e80-194">Når du har valgt forbindelsen, bliver du omdirigeret til listen over objekter i tilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="22e80-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="22e80-195">Start tilknytningerne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="22e80-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="22e80-196">Sørg for at følge rækkefølgen på listen.</span><span class="sxs-lookup"><span data-stu-id="22e80-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="22e80-197">**Objekttilknytning**</span><span class="sxs-lookup"><span data-stu-id="22e80-197">**Entity Map**</span></span> | <span data-ttu-id="22e80-198">**Opdater enhed**</span><span class="sxs-lookup"><span data-stu-id="22e80-198">**Refresh entity**</span></span> | <span data-ttu-id="22e80-199">**Første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="22e80-199">**Initial sync**</span></span> | <span data-ttu-id="22e80-200">**Master til første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="22e80-200">**Master for initial sync**</span></span> | <span data-ttu-id="22e80-201">**Kør forudsætninger**</span><span class="sxs-lookup"><span data-stu-id="22e80-201">**Run prerequisites**</span></span> | <span data-ttu-id="22e80-202">**Forudsætning for første synkronisering**</span><span class="sxs-lookup"><span data-stu-id="22e80-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="22e80-203">**Projektressourceroller for alle firmaer (reserverbareressourcekategorier)**</span><span class="sxs-lookup"><span data-stu-id="22e80-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="22e80-204">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-204">No</span></span> | <span data-ttu-id="22e80-205">Ja</span><span class="sxs-lookup"><span data-stu-id="22e80-205">Yes</span></span> | <span data-ttu-id="22e80-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="22e80-206">Common Data Service</span></span> | <span data-ttu-id="22e80-207">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-207">No</span></span> | <span data-ttu-id="22e80-208">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-208">N\A</span></span> |
| <span data-ttu-id="22e80-209">**Juridiske enheder (cdm\_virksomheder)**</span><span class="sxs-lookup"><span data-stu-id="22e80-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="22e80-210">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-210">No</span></span> | <span data-ttu-id="22e80-211">Ja</span><span class="sxs-lookup"><span data-stu-id="22e80-211">Yes</span></span> | <span data-ttu-id="22e80-212">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="22e80-212">Finance and Operations apps</span></span> | <span data-ttu-id="22e80-213">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-213">No</span></span> | <span data-ttu-id="22e80-214">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-214">N\A</span></span> |
| <span data-ttu-id="22e80-215">**Hovedbog (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="22e80-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="22e80-216">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-216">No</span></span> | <span data-ttu-id="22e80-217">Ja</span><span class="sxs-lookup"><span data-stu-id="22e80-217">Yes</span></span> | <span data-ttu-id="22e80-218">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="22e80-218">Finance and Operations apps</span></span> | <span data-ttu-id="22e80-219">Ja</span><span class="sxs-lookup"><span data-stu-id="22e80-219">Yes</span></span> | <span data-ttu-id="22e80-220">Ja, Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="22e80-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="22e80-221">**Integration af faktiske oplysninger i Project Operations (msdyn\_faktiske oplysninger)**</span><span class="sxs-lookup"><span data-stu-id="22e80-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="22e80-222">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-222">No</span></span> | <span data-ttu-id="22e80-223">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-223">No</span></span> | <span data-ttu-id="22e80-224">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-224">N\A</span></span> | <span data-ttu-id="22e80-225">Ja</span><span class="sxs-lookup"><span data-stu-id="22e80-225">Yes</span></span> | <span data-ttu-id="22e80-226">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-226">No</span></span> |
| <span data-ttu-id="22e80-227">**Projekkontraktlinjer (salgsordredetaljer)**</span><span class="sxs-lookup"><span data-stu-id="22e80-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="22e80-228">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-228">No</span></span> | <span data-ttu-id="22e80-229">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-229">No</span></span> | <span data-ttu-id="22e80-230">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-230">N\A</span></span> | <span data-ttu-id="22e80-231">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-231">No</span></span> | <span data-ttu-id="22e80-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-232">No</span></span> |
| <span data-ttu-id="22e80-233">**Integrationsobjekt for projekttransaktionsrelationer (msdyn\_transaktionsforbindelser)**</span><span class="sxs-lookup"><span data-stu-id="22e80-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="22e80-234">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-234">No</span></span> | <span data-ttu-id="22e80-235">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-235">No</span></span> | <span data-ttu-id="22e80-236">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-236">N\A</span></span> | <span data-ttu-id="22e80-237">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-237">No</span></span> | <span data-ttu-id="22e80-238">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-238">N\A</span></span> |
| <span data-ttu-id="22e80-239">**Integration af kontraktlinjemilepæle i Project Operations (msdyn\_kontraktlinjeplanmedværdier)**</span><span class="sxs-lookup"><span data-stu-id="22e80-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="22e80-240">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-240">No</span></span> | <span data-ttu-id="22e80-241">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-241">No</span></span> | <span data-ttu-id="22e80-242">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-242">N\A</span></span> | <span data-ttu-id="22e80-243">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-243">No</span></span> | <span data-ttu-id="22e80-244">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-244">N\A</span></span> |
| <span data-ttu-id="22e80-245">**Integrationsobjekt for udgiftsestimater i Project Operations (msdyn\_estimeredelinjer)**</span><span class="sxs-lookup"><span data-stu-id="22e80-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="22e80-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-246">No</span></span> | <span data-ttu-id="22e80-247">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-247">No</span></span> | <span data-ttu-id="22e80-248">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-248">N\A</span></span> | <span data-ttu-id="22e80-249">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-249">No</span></span> | <span data-ttu-id="22e80-250">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-250">N\A</span></span> |
| <span data-ttu-id="22e80-251">**Integrationsobjekt for eksport af projektudgiftskategorier i Project Operations (msdyn\_udgiftskategorier)**</span><span class="sxs-lookup"><span data-stu-id="22e80-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="22e80-252">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-252">No</span></span> | <span data-ttu-id="22e80-253">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-253">No</span></span> | <span data-ttu-id="22e80-254">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-254">N\A</span></span> | <span data-ttu-id="22e80-255">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-255">No</span></span> | <span data-ttu-id="22e80-256">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-256">N\A</span></span> |
| <span data-ttu-id="22e80-257">**Integrationsobjekt for eksport af projektudgifter i Project Operations (msdyn\_udgifter)**</span><span class="sxs-lookup"><span data-stu-id="22e80-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="22e80-258">Ja</span><span class="sxs-lookup"><span data-stu-id="22e80-258">Yes</span></span> | <span data-ttu-id="22e80-259">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-259">No</span></span> | <span data-ttu-id="22e80-260">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-260">N\A</span></span> | <span data-ttu-id="22e80-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-261">No</span></span> | <span data-ttu-id="22e80-262">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-262">N\A</span></span> |
| <span data-ttu-id="22e80-263">**Integrationsobjekt for timeestimater i Project Operations (msdyn\_ressourcetildelinger)**</span><span class="sxs-lookup"><span data-stu-id="22e80-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="22e80-264">Ja</span><span class="sxs-lookup"><span data-stu-id="22e80-264">Yes</span></span> | <span data-ttu-id="22e80-265">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-265">No</span></span> | <span data-ttu-id="22e80-266">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-266">N\A</span></span> | <span data-ttu-id="22e80-267">Nr.</span><span class="sxs-lookup"><span data-stu-id="22e80-267">No</span></span> | <span data-ttu-id="22e80-268">I\R</span><span class="sxs-lookup"><span data-stu-id="22e80-268">N\A</span></span> |


4. <span data-ttu-id="22e80-269">Hvis du vil opdatere objektet, skal du vælge tilknytningens navn og derefter vælge **Opdater objekter**.</span><span class="sxs-lookup"><span data-stu-id="22e80-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Opdater tilknytning](./media/20RefreshMapping.png)

5. <span data-ttu-id="22e80-271">Kør tilknytningen, når opdateringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="22e80-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="22e80-272">Før du aktiverer næste tilknytning, skal du kontrollere, at tilknytningen i tabellen er i tilstanden **Kører**.</span><span class="sxs-lookup"><span data-stu-id="22e80-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="22e80-273">Det kan tage et stykke tid at køre tilknytningerne med et større antal forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="22e80-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="22e80-274">Hvis du vil køre en tilknytning med forudsætninger, skal du aktivere funktionen **Vis relaterede objekttilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="22e80-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="22e80-275">Hvis tabellen indikerer, at **Indledende synkronisering af forudsætning** er **Nej**, skal du kontrollere, at flaget for den **Indledende synkronisering** er **Slået fra** i alle de påkrævede tilknytninger, før du kører programmet.</span><span class="sxs-lookup"><span data-stu-id="22e80-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Kør tilknytning](./media/21RunMap.png)

6. <span data-ttu-id="22e80-277">Valider, at alle projektrelaterede tilknytninger er i kørselstilstand.</span><span class="sxs-lookup"><span data-stu-id="22e80-277">Validate all project related maps are in the running state.</span></span>

![Alle tilknytninger kører](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="22e80-279">Anvend konfigurationsdata i CDS for Project Operations (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="22e80-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="22e80-280">Hvis du har anvendt demodata i Finance-miljøet, skal du se [Konfigurere og anvende konfigurationsdata i Common Data Service til Project Operations](resource-apply-pro-setup-config-data.md) for at anvende demodata i CDS-miljøer.</span><span class="sxs-lookup"><span data-stu-id="22e80-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="22e80-281">Dit Project Operations-miljø er nu klargjort og konfigureret.</span><span class="sxs-lookup"><span data-stu-id="22e80-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]