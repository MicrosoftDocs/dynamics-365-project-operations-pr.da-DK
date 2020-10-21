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
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

I dette emne gives en forklaring på, hvordan du abonnerer på prøveversion/partnertilbuddet og udruller Project Operations-miljø for ressource/ikke-lagerbaserede scenarier.

## <a name="prerequisites"></a>Forudsætninger

- Du modtager en email, der inviterer dig til at deltage i prøveversionen. Du kan anmode om en prøveversion på [Webstedet for Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder.
- Hvis du vil udrulle et Finance-miljø, skal du have et gyldigt Azure-abonnement, der faktureres pr. miljø. Du kan bruge virksomhedens eksisterende abonnement eller bruge en [Azure-prøveversion](https://azure.microsoft.com/en-us/free/) til at komme i gang. CDS-miljøet er gratis i 30 dage.

## <a name="subscribe"></a>Abonner

Når din [anmodning om prøveversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) er godkendt, modtager du to tilbud fra Microsoft via email. Disse tilbud giver dig mulighed for at udrulle prøveversionen af Project Operations:

- Dynamics 365 Project Operations – prøveversion
- Dynamics 365 for Finance and Operations-prøveversion.

> [!IMPORTANT]
> Kun én person, lejeradministratoren, i en organisation skal udføre denne opgave. Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – prøveversion

1. Accepter det første tilbud om **Dynamics 365 Project Operations-prøveversion** med den URL-adresse, som blev angivet i din velkomstmail.

![Første tilbud](./media/1FirstOffer.png)

2. Kontroller, at du er logget på med den bruger, der tilhører den organisation, som abonnerer på tjenesten.
3. Fortsæt med at acceptere tilbuddet. 
4. Vælg **Ja, tilføj det til min konto**.

![Accepter tilbud](./media/2RedeemFirstOffer.png)

![Bekræft tilbud](./media/3ConfirmFirstOffer.png)

![Tilbud accepteret](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance-prøveversion

Gentag de samme trin med det andet tilbud fra velkomstmailen.

## <a name="assign-licenses"></a>Tildel licenser

> [!IMPORTANT]
> Du skal have administratoradgang til din organisations Office 365-portal for at fuldføre følgende trin.

1. Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenser til dine brugere.

![Administrationsportal for Office](./media/5OfficeAdminPortal.png)

2. På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.

![Tildel licenser](./media/6AssignLicenses.png)

3. Kontroller, at Project Operations-licensen er valgt, og vælg **Gem ændringer**. 

> [!NOTE]
> Tilbuddet om prøveversionen af Finance behøver ikke at være tildelt en bruger.

## <a name="start-a-new-project-in-lcs"></a>Start et nyt projekt i LCS

Opret et nyt LCS-projekt som beskrevet i emnet [Start et nyt projekt i LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Tilføj et Azure-abonnement til et LCS-projekt

Fuldfør denne opgave ved at følge trinnene i emnet [Tilføj et Azure-abonnement til LCS-projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Udrul Finance-demonstrationsmiljøet med Project Operations for ressource/ikke-lagerførte scenarier

Følg vejledningen i emnet [Klargør et nyt miljø](resource-provision-new-environment.md) for at fuldføre udrulningen. Brug [demonstrationsmiljøets](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) udrulningstype til prøveversionen.

## <a name="install-cds-setup-and-configuration-data"></a>Installer CDS-konfiguration og konfigurationsdata

Installer CDS-konfiguration og konfigurationsdata som beskrevet i emnet [Konfigurer og anvend konfigurationsdata i Common Data Service](resource-apply-pro-setup-config-data.md).

