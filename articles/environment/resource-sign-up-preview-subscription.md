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
ms.openlocfilehash: a6dfa51f59119834230b7c9f8859a9d85eaae999
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642944"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne gives en forklaring på, hvordan du abonnerer på prøveversion/partnertilbuddet og udruller Project Operations-miljø for ressource/ikke-lagerbaserede scenarier.

## <a name="prerequisites"></a>Forudsætninger

- Du modtager en email, der inviterer dig til at deltage i prøveversionen. Du kan anmode om en prøveversion på [Webstedet for Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder.
- Hvis du vil udrulle et Finance-miljø, skal du have et gyldigt Azure-abonnement, der faktureres pr. miljø. Du kan bruge virksomhedens eksisterende abonnement eller bruge en [Azure-prøveversion](https://azure.microsoft.com/en-us/free/) til at komme i gang. CDS-miljøet er gratis i 30 dage.

## <a name="subscribe"></a>Abonner

Når din [anmodning om prøveversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) er godkendt, modtager du tre tilbud fra Microsoft via email. Disse tilbud giver dig mulighed for at udrulle prøveversionen af Project Operations:

- Dynamics 365 Project Operations (CRM) - prøveversion
- Prøveversion - Office 365 Project Operations
- Dynamics 365 Finance - prøveversion

> [!IMPORTANT]
> Kun én person, lejeradministratoren, i en organisation skal udføre denne opgave. Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - prøveversion 

Før du går i gang, skal du sikre dig, at du er logget på en browser med brugerens arbejdskonto i lejeren, hvor du vil installere prøveversionen af Project Operations.

1. Indløs den første tilbudskode, **Dynamics 365 Project Operations (CRM) - prøveversion** ved at indsætte den i browserens URL.

![Accepter tilbud](./media/16RedeemFirstOfferNew.png)

2. Bekræft din ordre..

![Bekræft ordren](./media/17ConfirmOrderNew.png)

Du får vist en bekræftelse på, at tilbuddet blev indløst.

![Bekræftelse](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Prøveversion - Office 365 Project Operations

Gentag de samme trin som ved den første tilbudskode. Sørg for at tilføje den anden tilbudskode ved at anvende den samme brugerkonto, som blev brugt sammen med den første tilbudskode.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance-prøveversion

Gentag de samme trin med det sidste tilbud fra velkomstmailen.

## <a name="assign-licenses"></a>Tildel licenser

> [!IMPORTANT]
> Du skal have administratoradgang til din organisations Microsoft 365-portal for at fuldføre følgende trin.

1. Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenser til brugerne.

![Startside for Administration](./media/14AdminPortal.png)

2. På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.

![Tildel licenser](./media/15AssignLicenses.png)

3. Kontroller, at licensen **Dynamics 365 Project Operations (CRM) prøveversion** og **Office 365 Project Operations - prøveversion** er valgt, og vælg **Gem ændringer**.

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
Fuldfør kun dette trin, når demonstrationsmiljøet i Finance er udrullet, og demonstrationsdataene i FO er klar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]