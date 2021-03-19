---
title: Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier
description: Dette emne indeholder oplysninger om, hvordan du abonnerer på og udruller Project Operations for ressource-/ikke-lagerbaserede scenarier.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4c2cd4c5d4dfbb95398932d432864cf0d4d5d54d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276836"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="0070d-103">Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier</span><span class="sxs-lookup"><span data-stu-id="0070d-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="0070d-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="0070d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0070d-105">I dette emne gives en forklaring på, hvordan du abonnerer på prøveversion/partnertilbuddet og udruller Project Operations-miljø for ressource/ikke-lagerbaserede scenarier.</span><span class="sxs-lookup"><span data-stu-id="0070d-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0070d-106">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="0070d-106">Prerequisites</span></span>

- <span data-ttu-id="0070d-107">Du modtager en email, der inviterer dig til at deltage i prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="0070d-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="0070d-108">Du kan anmode om en prøveversion på [Webstedet for Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="0070d-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="0070d-109">Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder.</span><span class="sxs-lookup"><span data-stu-id="0070d-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="0070d-110">Hvis du vil udrulle et Finance-miljø, skal du have et gyldigt Azure-abonnement, der faktureres pr. miljø.</span><span class="sxs-lookup"><span data-stu-id="0070d-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="0070d-111">Du kan bruge virksomhedens eksisterende abonnement eller bruge en [Azure-prøveversion](https://azure.microsoft.com/en-us/free/) til at komme i gang.</span><span class="sxs-lookup"><span data-stu-id="0070d-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="0070d-112">CDS-miljøet er gratis i 30 dage.</span><span class="sxs-lookup"><span data-stu-id="0070d-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="0070d-113">Abonner</span><span class="sxs-lookup"><span data-stu-id="0070d-113">Subscribe</span></span>

<span data-ttu-id="0070d-114">Når din [anmodning om prøveversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) er godkendt, modtager du tre tilbud fra Microsoft via email.</span><span class="sxs-lookup"><span data-stu-id="0070d-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="0070d-115">Disse tilbud giver dig mulighed for at udrulle prøveversionen af Project Operations:</span><span class="sxs-lookup"><span data-stu-id="0070d-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="0070d-116">Dynamics 365 Project Operations (CRM) - prøveversion</span><span class="sxs-lookup"><span data-stu-id="0070d-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="0070d-117">Prøveversion - Office 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0070d-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="0070d-118">Dynamics 365 Finance - prøveversion</span><span class="sxs-lookup"><span data-stu-id="0070d-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0070d-119">Kun én person, lejeradministratoren, i en organisation skal udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="0070d-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="0070d-120">Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0070d-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="0070d-121">Dynamics 365 Project Operations (CRM) - prøveversion</span><span class="sxs-lookup"><span data-stu-id="0070d-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="0070d-122">Før du går i gang, skal du sikre dig, at du er logget på en browser med brugerens arbejdskonto i lejeren, hvor du vil installere prøveversionen af Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0070d-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="0070d-123">Indløs den første tilbudskode, **Dynamics 365 Project Operations (CRM) - prøveversion** ved at indsætte den i browserens URL.</span><span class="sxs-lookup"><span data-stu-id="0070d-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Accepter tilbud](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="0070d-125">Bekræft din ordre..</span><span class="sxs-lookup"><span data-stu-id="0070d-125">Confirm your order.</span></span>

![Bekræft ordren](./media/17ConfirmOrderNew.png)

<span data-ttu-id="0070d-127">Du får vist en bekræftelse på, at tilbuddet blev indløst.</span><span class="sxs-lookup"><span data-stu-id="0070d-127">You will see confirmation offer was successfully redeemed.</span></span>

![Bekræftelse](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="0070d-129">Prøveversion - Office 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0070d-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="0070d-130">Gentag de samme trin som ved den første tilbudskode.</span><span class="sxs-lookup"><span data-stu-id="0070d-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="0070d-131">Sørg for at tilføje den anden tilbudskode ved at anvende den samme brugerkonto, som blev brugt sammen med den første tilbudskode.</span><span class="sxs-lookup"><span data-stu-id="0070d-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="0070d-132">Dynamics 365 Finance-prøveversion</span><span class="sxs-lookup"><span data-stu-id="0070d-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="0070d-133">Gentag de samme trin med det sidste tilbud fra velkomstmailen.</span><span class="sxs-lookup"><span data-stu-id="0070d-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="0070d-134">Tildel licenser</span><span class="sxs-lookup"><span data-stu-id="0070d-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0070d-135">Du skal have administratoradgang til din organisations Microsoft 365-portal for at fuldføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="0070d-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="0070d-136">Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenser til brugerne.</span><span class="sxs-lookup"><span data-stu-id="0070d-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Startside for Administration](./media/14AdminPortal.png)

2. <span data-ttu-id="0070d-138">På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.</span><span class="sxs-lookup"><span data-stu-id="0070d-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Tildel licenser](./media/15AssignLicenses.png)

3. <span data-ttu-id="0070d-140">Kontroller, at licensen **Dynamics 365 Project Operations (CRM) prøveversion** og **Office 365 Project Operations - prøveversion** er valgt, og vælg **Gem ændringer**.</span><span class="sxs-lookup"><span data-stu-id="0070d-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="0070d-141">Tilbuddet om prøveversionen af Finance behøver ikke at være tildelt en bruger.</span><span class="sxs-lookup"><span data-stu-id="0070d-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="0070d-142">Start et nyt projekt i LCS</span><span class="sxs-lookup"><span data-stu-id="0070d-142">Start a new project in LCS</span></span>

<span data-ttu-id="0070d-143">Opret et nyt LCS-projekt som beskrevet i emnet [Start et nyt projekt i LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="0070d-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="0070d-144">Tilføj et Azure-abonnement til et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="0070d-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="0070d-145">Fuldfør denne opgave ved at følge trinnene i emnet [Tilføj et Azure-abonnement til LCS-projekt](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="0070d-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="0070d-146">Udrul Finance-demonstrationsmiljøet med Project Operations for ressource/ikke-lagerførte scenarier</span><span class="sxs-lookup"><span data-stu-id="0070d-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="0070d-147">Følg vejledningen i emnet [Klargør et nyt miljø](resource-provision-new-environment.md) for at fuldføre udrulningen.</span><span class="sxs-lookup"><span data-stu-id="0070d-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="0070d-148">Brug [demonstrationsmiljøets](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) udrulningstype til prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="0070d-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="0070d-149">Installer CDS-konfiguration og konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="0070d-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="0070d-150">Installer CDS-konfiguration og konfigurationsdata som beskrevet i emnet [Konfigurer og anvend konfigurationsdata i Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="0070d-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="0070d-151">Fuldfør kun dette trin, når demonstrationsmiljøet i Finance er udrullet, og demonstrationsdataene i FO er klar.</span><span class="sxs-lookup"><span data-stu-id="0070d-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]