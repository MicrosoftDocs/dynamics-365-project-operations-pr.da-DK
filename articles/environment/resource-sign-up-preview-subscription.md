---
title: Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier
description: Dette emne indeholder oplysninger om, hvordan du abonnerer på og udruller Project Operations for ressource-/ikke-lagerbaserede scenarier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948812"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="0d06c-103">Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier</span><span class="sxs-lookup"><span data-stu-id="0d06c-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="0d06c-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="0d06c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0d06c-105">I dette emne gives en forklaring på, hvordan du abonnerer på prøveversion/partnertilbuddet og udruller Project Operations-miljø for ressource/ikke-lagerbaserede scenarier.</span><span class="sxs-lookup"><span data-stu-id="0d06c-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d06c-106">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="0d06c-106">Prerequisites</span></span>

- <span data-ttu-id="0d06c-107">Du modtager en email, der inviterer dig til at deltage i prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="0d06c-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="0d06c-108">Du kan anmode om en prøveversion på [Webstedet for Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="0d06c-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="0d06c-109">Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder.</span><span class="sxs-lookup"><span data-stu-id="0d06c-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="0d06c-110">Hvis du vil udrulle et Finance-miljø, skal du have et gyldigt Azure-abonnement, der faktureres pr. miljø.</span><span class="sxs-lookup"><span data-stu-id="0d06c-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="0d06c-111">Du kan bruge virksomhedens eksisterende abonnement eller bruge en [Azure-prøveversion](https://azure.microsoft.com/en-us/free/) til at komme i gang.</span><span class="sxs-lookup"><span data-stu-id="0d06c-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="0d06c-112">CDS-miljøet er gratis i 30 dage.</span><span class="sxs-lookup"><span data-stu-id="0d06c-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="0d06c-113">Abonner</span><span class="sxs-lookup"><span data-stu-id="0d06c-113">Subscribe</span></span>

<span data-ttu-id="0d06c-114">Når din [anmodning om prøveversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) er godkendt, modtager du to tilbud fra Microsoft via email.</span><span class="sxs-lookup"><span data-stu-id="0d06c-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="0d06c-115">Disse tilbud giver dig mulighed for at udrulle prøveversionen af Project Operations:</span><span class="sxs-lookup"><span data-stu-id="0d06c-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="0d06c-116">Dynamics 365 Project Operations – prøveversion</span><span class="sxs-lookup"><span data-stu-id="0d06c-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="0d06c-117">Dynamics 365 for Finance and Operations-prøveversion.</span><span class="sxs-lookup"><span data-stu-id="0d06c-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d06c-118">Kun én person, lejeradministratoren, i en organisation skal udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="0d06c-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="0d06c-119">Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0d06c-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="0d06c-120">Dynamics 365 Project Operations – prøveversion</span><span class="sxs-lookup"><span data-stu-id="0d06c-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="0d06c-121">Accepter det første tilbud om **Dynamics 365 Project Operations-prøveversion** med den URL-adresse, som blev angivet i din velkomstmail.</span><span class="sxs-lookup"><span data-stu-id="0d06c-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Første tilbud](./media/1FirstOffer.png)

2. <span data-ttu-id="0d06c-123">Kontroller, at du er logget på med den bruger, der tilhører den organisation, som abonnerer på tjenesten.</span><span class="sxs-lookup"><span data-stu-id="0d06c-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="0d06c-124">Fortsæt med at acceptere tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="0d06c-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="0d06c-125">Vælg **Ja, tilføj det til min konto**.</span><span class="sxs-lookup"><span data-stu-id="0d06c-125">Select **Yes, add it to my account**.</span></span>

![Accepter tilbud](./media/2RedeemFirstOffer.png)

![Bekræft tilbud](./media/3ConfirmFirstOffer.png)

![Tilbud accepteret](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="0d06c-129">Dynamics 365 Finance-prøveversion</span><span class="sxs-lookup"><span data-stu-id="0d06c-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="0d06c-130">Gentag de samme trin med det andet tilbud fra velkomstmailen.</span><span class="sxs-lookup"><span data-stu-id="0d06c-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="0d06c-131">Tildel licenser</span><span class="sxs-lookup"><span data-stu-id="0d06c-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d06c-132">Du skal have administratoradgang til din organisations Office 365-portal for at fuldføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="0d06c-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="0d06c-133">Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenser til dine brugere.</span><span class="sxs-lookup"><span data-stu-id="0d06c-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Administrationsportal for Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="0d06c-135">På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.</span><span class="sxs-lookup"><span data-stu-id="0d06c-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Tildel licenser](./media/6AssignLicenses.png)

3. <span data-ttu-id="0d06c-137">Kontroller, at Project Operations-licensen er valgt, og vælg **Gem ændringer**.</span><span class="sxs-lookup"><span data-stu-id="0d06c-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0d06c-138">Tilbuddet om prøveversionen af Finance behøver ikke at være tildelt en bruger.</span><span class="sxs-lookup"><span data-stu-id="0d06c-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="0d06c-139">Start et nyt projekt i LCS</span><span class="sxs-lookup"><span data-stu-id="0d06c-139">Start a new project in LCS</span></span>

<span data-ttu-id="0d06c-140">Opret et nyt LCS-projekt som beskrevet i emnet [Start et nyt projekt i LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="0d06c-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="0d06c-141">Tilføj et Azure-abonnement til et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="0d06c-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="0d06c-142">Fuldfør denne opgave ved at følge trinnene i emnet [Tilføj et Azure-abonnement til LCS-projekt](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="0d06c-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="0d06c-143">Udrul Finance-demonstrationsmiljøet med Project Operations for ressource/ikke-lagerførte scenarier</span><span class="sxs-lookup"><span data-stu-id="0d06c-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="0d06c-144">Følg vejledningen i emnet [Klargør et nyt miljø](resource-provision-new-environment.md) for at fuldføre udrulningen.</span><span class="sxs-lookup"><span data-stu-id="0d06c-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="0d06c-145">Brug [demonstrationsmiljøets](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) udrulningstype til prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="0d06c-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="0d06c-146">Installer CDS-konfiguration og konfigurationsdata</span><span class="sxs-lookup"><span data-stu-id="0d06c-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="0d06c-147">Installer CDS-konfiguration og konfigurationsdata som beskrevet i emnet [Konfigurer og anvend konfigurationsdata i Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="0d06c-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

