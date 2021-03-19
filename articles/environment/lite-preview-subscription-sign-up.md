---
title: Tilmelding til et prøveversionsabonnement - lille
description: Dette emne indeholder oplysninger om, hvordan du abonnere på og udruller den lille udrulning af Project Operations - aftale til proformafakturering.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290037"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Tilmelding til et prøveversionsabonnement - lille 

I dette emne beskrives det, hvordan du abonnerer på partnertilbuddet om en forhåndsversion og udruller Dynamics 365 Project Operations lille udrulning – aftale til proformafakturering.

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

1. Indløs den første tilbudskode, **Dynamics 365 Project Operations (CRM) - prøveversion** ved at indsætte den i browserens URL.

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

3. Kontrollér, at licenserne til **Dynamics 365 Project Operations (CRM) forhåndsversion** og **Office 365 Project Operations – forhåndsversion** er valgt. 
4. Vælg **Gem ændringer**.

## <a name="create-a-new-cds-environment"></a>Opret et CDS-miljø

1. Klargør et nyt CDS-udrulningsmiljø for Project Operations ved at følge vejledningen i emnet [CDS-udrulningsmodel](lite-deployment.md). Når du vælger miljøtypen, skal du sørge for at bruge **Prøveversion (abonnementsbaseret)**.
![Nyt miljø](./media/19CreateEnvironment.png)

2. Vælg indstillingen **Aktivér Dynamics 365-apps**, og lad **Udrul automatisk disse apps** være tom.  
3. Vælg **Gem** for at oprette miljøet.

![Tilføj database](./media/20CreateEnvironment1.png)

4. Når miljøet er oprettet, skal du installere **Microsoft Dynamics 365 Project Operations**-løsningen. 

![Installer løsningen](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installer en CDS-konfiguration og konfigurer demonstrationsdata

Installer CDS-konfigurationen, og konfigurer demonstrationsdata ved at følge vejledningen i emnet [Anvend demonstrationskonfiguration og konfigurationsdata](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]