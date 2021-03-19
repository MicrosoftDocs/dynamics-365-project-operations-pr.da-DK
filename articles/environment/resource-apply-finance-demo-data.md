---
title: Anvend demonstrationsdata på et skybaseret Finance-miljø
description: Dette emne beskriver, hvordan du anvender demonstrationsdata fra Project Operations til et skybaseret Dynamics 365 Finance-miljø.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7239301dc8b775dc4a53a1cf6c0bcba3956125a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289857"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="b023c-103">Anvend demonstrationsdata på et skybaseret Finance-miljø</span><span class="sxs-lookup"><span data-stu-id="b023c-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="b023c-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="b023c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b023c-105">Dette emne gælder kun for Microsoft Dynamics 365 Finance version 10.0.13 og kan kun udføres i et skybaseret miljø.</span><span class="sxs-lookup"><span data-stu-id="b023c-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="b023c-106">Gennemfør trinnene i dette emne, **FØR** du anvender kvalitetsopdateringer på miljøet.</span><span class="sxs-lookup"><span data-stu-id="b023c-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="b023c-107">I dit LCS-projekt skal du åbne siden **Miljødetaljer**.</span><span class="sxs-lookup"><span data-stu-id="b023c-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="b023c-108">Bemærk, at det indeholder de oplysninger, der skal bruges for at oprette forbindelse til miljøet ved hjælp af RDP (Fjernskrivebordsprotokol).</span><span class="sxs-lookup"><span data-stu-id="b023c-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detaljer for -miljø](./media/1EnvironmentDetails.png)

<span data-ttu-id="b023c-110">Det første sæt af fremhævede legitimationsoplysninger er legitimationsoplysninger til den lokale konto og indeholder et link til forbindelse til fjernskrivebord.</span><span class="sxs-lookup"><span data-stu-id="b023c-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="b023c-111">Legitimationsoplysningerne omfatter administrators brugernavn og adgangskode for miljøet.</span><span class="sxs-lookup"><span data-stu-id="b023c-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="b023c-112">Det andet sæt legitimationsoplysninger bruges til at logge på SQL Server i dette miljø.</span><span class="sxs-lookup"><span data-stu-id="b023c-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="b023c-113">Opret fjernforbindelse til miljøet ved hjælp af linket i **Lokale Konti**, og brug **Legitimationsoplysningerne** for at autorisere.</span><span class="sxs-lookup"><span data-stu-id="b023c-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="b023c-114">Gå til **Internet Information Services** > **Programgrupper** > **AOSService**, og stands tjenesten.</span><span class="sxs-lookup"><span data-stu-id="b023c-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="b023c-115">Du er ved at stoppe tjenesten på dette tidspunkt, så du kan fortsætte med at erstatte SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b023c-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Stands AOS](./media/2StopAOS.png)

4. <span data-ttu-id="b023c-117">Gå til **Tjenester**, og stop følgende to elementer:</span><span class="sxs-lookup"><span data-stu-id="b023c-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="b023c-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span><span class="sxs-lookup"><span data-stu-id="b023c-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="b023c-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span><span class="sxs-lookup"><span data-stu-id="b023c-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Stop tjenester](./media/3StopServices.png)

5. <span data-ttu-id="b023c-121">Åbn Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b023c-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="b023c-122">Log på med SQL Server-legitimationsoplysninger, og brug axdbadmin-brugeren og -adgangskoden fra siden med LCS-**Miljøoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="b023c-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="b023c-124">I Object Explorer, **Databaser** og find **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="b023c-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="b023c-125">Du skal erstatte databasen med en ny database, der findes i [Downloadcenteret](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="b023c-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="b023c-126">Kopier zip-filen til den VM, du har fjernforbindelse til, og udpak indholdet.</span><span class="sxs-lookup"><span data-stu-id="b023c-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="b023c-127">I SQL Server Management Studio skal du højreklikke på **AxDB** og derefter vælge **Opgaver** > **Gendan** > **Database**.</span><span class="sxs-lookup"><span data-stu-id="b023c-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Gendan database](./media/5RestoreDatabase.png)

9. <span data-ttu-id="b023c-129">Vælg **Kildeenhed**, og naviger til den fil, du har kopieret fra den zip-fil, som du kopierede.</span><span class="sxs-lookup"><span data-stu-id="b023c-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Kildeenheder](./media/6SourceDevice.png)

10. <span data-ttu-id="b023c-131">Vælg **Indstillinger**, og vælg derefter **Overskriv den eksisterende database**, og **Luk eksisterende forbindelser til destinationsdatabasen**.</span><span class="sxs-lookup"><span data-stu-id="b023c-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="b023c-132">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b023c-132">Select **OK**.</span></span>

![Gendan indstillinger](./media/7RestoreSetting.png)

<span data-ttu-id="b023c-134">Du modtager en bekræftelse på, at AXDB-gendannelsen blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="b023c-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="b023c-135">Når du har modtaget denne bekræftelse, kan du lukke SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b023c-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="b023c-136">Gå tilbage til **Internet Information Services** > **Programgrupper** > **AOSService**, og start AOSService.</span><span class="sxs-lookup"><span data-stu-id="b023c-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="b023c-137">Gå til **Tjenester**, og start de to tjenester, du standsede tidligere.</span><span class="sxs-lookup"><span data-stu-id="b023c-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="b023c-138">Find AdminUserProvisioning-værktøjet på denne VM.</span><span class="sxs-lookup"><span data-stu-id="b023c-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="b023c-139">Se under K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="b023c-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="b023c-140">Kør .ext-filen ved hjælp af din brugeradresse i feltet **Mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="b023c-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="b023c-141">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="b023c-141">Select **Submit**.</span></span>

![Administratorbrugerklargøring](./media/8AdminUserProvisioning.png)

<span data-ttu-id="b023c-143">Dette tager et par minutter at fuldføre.</span><span class="sxs-lookup"><span data-stu-id="b023c-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="b023c-144">Du bør modtage en bekræftelsesmeddelelse om, at administratorbrugeren blev opdateret korrekt.</span><span class="sxs-lookup"><span data-stu-id="b023c-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="b023c-145">Endelig skal du køre kommandoprompt som administrator og nulstille IIS</span><span class="sxs-lookup"><span data-stu-id="b023c-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Nulstil IIS](./media/9IISReset.png)

18. <span data-ttu-id="b023c-147">Luk fjernskrivebordssessionen, og brug siden med LCS-**Miljødetaljer** til at logge på miljøet for at bekræfte, at den fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="b023c-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]