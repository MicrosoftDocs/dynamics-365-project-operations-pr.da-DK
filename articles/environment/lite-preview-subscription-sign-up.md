---
title: Tilmelding til et prøveversionsabonnement
description: Dette emne indeholder oplysninger om, hvordan du abonnere på og udruller den lille udrulning af Project Operations - aftale til proformafakturering.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948809"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Tilmeld dig et prøveabonnement på den lille udrulning – aftale med proformafakturering

Dette emne forklarer, hvordan du abonnere på prøveversionen af partnertilbuddet og udruller den lille udrulning af Dynamics 365 Project Operations - aftale til proformafakturering.

> [!NOTE]
> Denne proces ændres i de kommende versioner af Project Operations.

## <a name="prerequisites"></a>Forudsætninger

- Du modtager en email, der inviterer dig til at deltage i prøveversionen. Du kan anmode om en prøveversion på [Webstedet for Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder.
- Den bruger, der installerer prøveversionen, skal have et telefonnummer og et gyldigt kreditkort. Under tilmeldingen vil der ikke blive trukket beløb på kortet i seks måneder. Efter seks måneder er du nødt til at annullere abonnementet. 
- Gennemse alle vilkår og betingelser.

## <a name="subscribe"></a>Abonner

Når du modtager en godkendelse af din [anmodning om prøveversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), modtager du to tilbud fra Microsoft via email. Disse tilbud giver dig mulighed for at udrulle prøveversionen af Project Operations:

- Prøveversion af Dynamics 365 Customer Service – engangskode
- Dynamics 365 Project Operations – prøveversion

### <a name="dynamics-365-customer-service-paid-offer"></a>Betalt tilbud på Dynamics 365 Customer Service

1. Ved hjælp af et InPrivate/Incognito-browservindue skal du indløse den første tilbudskode for Dynamics 365 Customer Service. Hvis du vil tilmelde dig Customer Service, skal du bruge følgende:

- Et telefonnummer
- Et kreditkort. Når du tilmelder dig, vil der ikke blive trukket beløb på kortet i seks måneder. Efter seks måneder er du nødt til at annullere abonnementet.
- Gennemse alle vilkår og betingelser.

2. Angiv dine kontaktoplysninger.

![Oplysninger om kontaktperson](./media/1ContactInformation.png)

3. Angiv de nye oplysninger om lejeren.

![Opret bruger-id](./media/2CreateUserID.png)

4. Bekræft din identitet, gem dit nye bruger-id, og vælg **Konfigurer**.

![Gem oplysninger](./media/3SaveInfo.png)

5. Gennemfør tilmeldingen med kreditkortet, og gennemgå alle vilkår og betingelser. 

![Gennemfør kreditkort](./media/4CompleteCreditCard.png)

![Udtjekning med kreditkort](./media/5CreditCardCheckout.png)

![Gem ordre](./media/6SaveOrder.png)

![Bekræftelse af kreditkort](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Annuller tilbuddet vedrørende Dynamics 365 Customer Service Enterprise

Tilbuddet vedrørende Dynamics 365 Customer Service Enterprise er gratis i seks måneder. Tilbuddet bliver fornyet til fuld pris i slutningen af perioden på seks måneder. Hvis du vil annullere før fornyelsesdatoen, skal du benytte følgende fremgangsmåde. 

> [!NOTE]
> Når du har fuldført disse trin, kan du ikke længere bruge den offentlige prøveversion af Project Operations-miljøet.

1. Gå til [Administrationsportalen](https://admin.microsoft.com/), og under **Fakturering** skal du **Dine produkter**.

![Administrationsportal, siden med Dine produkter](./media/8AdminPortal.png)

2. Vælg **Tilbuddet vedrørende Dynamics 365 Customer Service Enterprise**.

![Opsig abonnement](./media/9CancelSubscription.png)

3. Vælg **Indstillinger** > **Handlinger** > **Annuller abonnement**.
4. På formularen **Annuller abonnement** skal du angive oplysninger i de påkrævede felter.
5. Vælg **Annuller** > **Abonnement**.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – prøveversion

1. Accepter det andet tilbud om en prøve på Dynamics 365 Project Operations med den URL-adresse, som blev angivet i din velkomstmail.

![Accepter tilbud 2](./media/10RedeemOffer2.png)

2. Kontroller, at du er logget på som den bruger, der tilhører den samme organisation som den, der abonnerede ved hjælp af den første tilbudskode, og fortsæt derefter med at acceptere tilbuddet. 
3. Vælg **Ja, tilføj det til min konto**.

![Tilføj til firma](./media/11AddToAccount.png)

![Skærmbilledet Prøv nu](./media/12TryNow.png)

![Ordredetaljer](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Tildel licenser

> [!IMPORTANT]
> Du skal have administratoradgang til din organisations Office 365-portal for at fuldføre følgende trin.

1. Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenser til brugerne.

![Startside for Administration](./media/14AdminPortal.png)

2. På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.

![Tildel licenser](./media/15AssignLicenses.png)

3. Kontroller, at licensen til **Customer Service Enterprise** og **Project Operations** er valgt, og vælg **Gem ændringer**.

## <a name="create-a-new-cds-environment"></a>Opret et CDS-miljø

Klargør et nyt CDS-udrulningsmiljø for Project Operations ved at følge vejledningen i emnet [CDS-udrulningsmodel](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installer en CDS-konfiguration og konfigurer demonstrationsdata

Installer CDS-konfigurationen, og konfigurer demonstrationsdata ved at følge vejledningen i emnet [Anvend demonstrationskonfiguration og konfigurationsdata](lite-apply-demo-setup-config-data.md).
