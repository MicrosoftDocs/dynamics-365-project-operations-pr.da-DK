---
title: Tilføj et Azure-abonnement til et LCS-projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter forbindelse mellem Azure-abonnementet og et LCS-projekt.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880531"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="1d85f-103">Tilføj et Azure-abonnement til et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="1d85f-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="1d85f-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="1d85f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1d85f-105">Cloud-hostede miljøer skal installeres ved hjælp af et eksisterende Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d85f-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="1d85f-106">Dette emne forklarer, hvordan du opretter forbindelse mellem dit eksisterende Azure-abonnementet og et LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="1d85f-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="1d85f-107">Giv administratorsamtykke</span><span class="sxs-lookup"><span data-stu-id="1d85f-107">Grant admin consent</span></span>

1. <span data-ttu-id="1d85f-108">I dit LCS-projekt skal du i sektionen **Miljøer** vælge **Microsoft Azure-indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Indstillinger for Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="1d85f-110">På siden **Projektindstillinger** skal du på fanen **Azure-forbindelser** vælge **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="1d85f-111">Det gør det muligt at udrulle miljøer på dette projekt.</span><span class="sxs-lookup"><span data-stu-id="1d85f-111">This allows environments to be deployed to this project.</span></span>

![Azure-forbindelser](./media/2AzureConnectors.png)

3. <span data-ttu-id="1d85f-113">Vælg **Autoriser** igen for at give administratorsamtykke.</span><span class="sxs-lookup"><span data-stu-id="1d85f-113">Select **Authorize** again to provide admin consent.</span></span>

![Giv administratorsamtykke](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="1d85f-115">Accepter anmodningen om tilladelse.</span><span class="sxs-lookup"><span data-stu-id="1d85f-115">Accept the permissions request.</span></span>

![Accepter anmodningen om tilladelse](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="1d85f-117">Autorisationen er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="1d85f-117">The authorization is now complete.</span></span> 

![Autorisation er fuldført](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="1d85f-119">Give Dynamics Deployment Services adgang til dit Azure-abonnement</span><span class="sxs-lookup"><span data-stu-id="1d85f-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="1d85f-120">Gå til [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade), og vælg dit abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d85f-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="1d85f-121">Dynamics Deployment Services skal have adgang til dette abonnement for at kunne udrulle miljøer.</span><span class="sxs-lookup"><span data-stu-id="1d85f-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Abonnementsoplysninger for Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="1d85f-123">Vælg **Adgangskontrol (IAM)** i navigationsruden, og vælg derefter **Tilføj rolletildeling**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="1d85f-124">Vælg **Bidragyderrolle** i skyderen på højre side, og find og vælg **Dynamics Deployment Services** på listen.</span><span class="sxs-lookup"><span data-stu-id="1d85f-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="1d85f-125">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-125">Select **Save**.</span></span>

![Abonnementsadgang](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="1d85f-127">Tilføj en abonnementsforbindelse til et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="1d85f-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="1d85f-128">I dit LCS projekt på siden **Microsoft Azure-indstillinger** skal du vælge **Tilføj** for at tilføje en ny forbindelse.</span><span class="sxs-lookup"><span data-stu-id="1d85f-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="1d85f-129">Angiv dit Azure-abonnements-id.</span><span class="sxs-lookup"><span data-stu-id="1d85f-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="1d85f-130">Du kan finde dit abonnements-id for Azure i [Azure-portalen](https://ms.portal.azure.com/) under **Indstillinger** nederst til venstre på skærmen.</span><span class="sxs-lookup"><span data-stu-id="1d85f-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="1d85f-131">I feltet **Konfigurer til at bruge Azure Resource Manager** skal du vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="1d85f-132">Kontroller, at Azures abonnement-AAD-lejerdomæne stemmer overens med det domæne, som ejer Azure-abonnementet, du bruger, og vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="1d85f-133">På skærmen **Microsoft Azure-opsætning** skal du vælge **Næste** for at bekræfte.</span><span class="sxs-lookup"><span data-stu-id="1d85f-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="1d85f-134">Hvis du modtager en fejl på skærmen, kan du gå tilbage til sektionen [Giv Dynamics Deployment Services adgang til Azure-abonnementet](#provide) i dette emne og sikre dig, at du har fuldført alle trinene.</span><span class="sxs-lookup"><span data-stu-id="1d85f-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="1d85f-135">Hent Azure Management Certificate til en lokal mappe på din computer.</span><span class="sxs-lookup"><span data-stu-id="1d85f-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="1d85f-136">Bed din Azure-abonnementsadministrator om at overføre certifikatet til Azure Management Portal ved at vælge abonnementet og gå til **Indstillinger** > **Administrationscertifikater**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="1d85f-137">Med dette certifikat kan LCS kommunikere med Azure på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="1d85f-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="1d85f-138">Du kan springe dette trin over, hvis brugeren har adgang til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="1d85f-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="1d85f-139">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-139">Select  **Next**.</span></span>
8. <span data-ttu-id="1d85f-140">Vælg det Azure-område, det skal udrulles i, og vælg et datacenter, der ligger tæt på det sted, hvor du vil bruge dette system.</span><span class="sxs-lookup"><span data-stu-id="1d85f-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="1d85f-141">Vælg **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="1d85f-141">Select  **Connect**.</span></span>

<span data-ttu-id="1d85f-142">Du har oprettet forbindelse til dit Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d85f-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="1d85f-143">Du kan nu udrulle skybaserede Dynamics 365 Finance-miljøer.</span><span class="sxs-lookup"><span data-stu-id="1d85f-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
