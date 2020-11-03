---
title: Tilmelding til et prøveversionsabonnement
description: Dette emne indeholder oplysninger om, hvordan du abonnere på og udruller den lille udrulning af Project Operations - aftale til proformafakturering.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074035"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Tilmeld dig et prøveabonnement på den lille udrulning – aftale med proformafakturering

Dette emne forklarer, hvordan du abonnere på prøveversionen af partnertilbuddet og udruller den lille udrulning af Dynamics 365 Project Operations - aftale til proformafakturering.

> [!NOTE]
> Denne proces ændres i de kommende versioner af Project Operations.

## <a name="prerequisites"></a>Forudsætninger

- Du modtager en mail, der inviterer dig til at deltage i prøveversionen. Du kan anmode om en prøveversion på [Webstedet for Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder.
- Gennemse alle vilkår og betingelser.

## <a name="subscribe"></a>Abonner

Når du modtager en godkendelse af din [anmodning om prøveversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), modtager du to tilbud fra Microsoft via email. Disse tilbud giver dig mulighed for at udrulle prøveversionen af Project Operations:

- Dynamics 365 Project Operations (CRM) - prøveversion
- Prøveversion - Office 365 Project Operations

> [!IMPORTANT]
> Kun én person, lejeradministratoren, i en organisation skal udføre denne opgave. Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - prøveversion 

Før du går i gang, skal du sikre dig, at du er logget på en browser med brugerens arbejdskonto i lejeren, hvor du vil installere prøveversionen af Project Operations.

1. Indløser den første tilbudskode, **Dynamics 365 Project Operations (CRM) - prøveversion** ved at indsætte den i browserens URL-adresse.

![Accepter tilbud](./media/16RedeemFirstOfferNew.png)

2. Bekræft din ordre..
![Kontrollér ordren](./media/17ConfirmOrderNew.png)

Du får en bekræftelse på, at tilbuddet blev indløst.

![Bekræftelse](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Prøveversion - Office 365 Project Operations

Gentag de samme trin som ved den første tilbudskode. Sørg for at tilføje den anden tilbudskode ved at anvende den samme brugerkonto, som blev brugt sammen med den første tilbudskode.

## <a name="assign-licenses"></a>Tildel licenser

> [!IMPORTANT]
> Du skal have administratoradgang til din organisations Microsoft 365-portal for at fuldføre følgende trin.


1. Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenser til brugerne.

![Startside for Administration](./media/14AdminPortal.png)

2. På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.

![Tildel licenser](./media/15AssignLicenses.png)

3. Kontroller, at licenserne **Dynamics 365 Project Operations (CRM) prøveversion** og **Office 365 Project Operations - prøveversion** er valgt. 
4. Vælg **Gem ændringer**.

## <a name="create-a-new-cds-environment"></a>Opret et CDS-miljø

1. Klargør et nyt CDS-udrulningsmiljø for Project Operations ved at følge vejledningen i emnet [CDS-udrulningsmodel](lite-deployment.md). Når du vælger miljøtypen, skal du sørge for at bruge **Prøveversion (abonnementsbaseret)**.
![Nyt miljø](./media/19CreateEnvironment.png)

2. Vælg indstillingen **Aktivér Dynamics 365-apps** , og lad **Udrul automatisk disse apps** være tom.  
3. Vælg **Gem** for at oprette miljøet.

![Tilføj database](./media/20CreateEnvironment1.png)

4. Når miljøet er oprettet, skal du installere løsningen **Microsoft Dynamics 365 Project Operations**. 

![Installer løsningen](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installer en CDS-konfiguration og konfigurer demonstrationsdata

Installer CDS-konfigurationen, og konfigurer demonstrationsdata ved at følge vejledningen i emnet [Anvend demonstrationskonfiguration og konfigurationsdata](lite-apply-demo-setup-config-data.md).
