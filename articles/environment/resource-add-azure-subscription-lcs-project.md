---
title: Tilføj et Azure-abonnement til et LCS-projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter forbindelse mellem Azure-abonnementet og et LCS-projekt.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175794"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Tilføj et Azure-abonnement til et LCS-projekt

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Cloud-hostede miljøer skal installeres ved hjælp af et eksisterende Azure-abonnement. Dette emne forklarer, hvordan du opretter forbindelse mellem dit eksisterende Azure-abonnementet og et LCS-projekt. 

## <a name="grant-admin-consent"></a>Giv administratorsamtykke

1. I dit LCS-projekt skal du i sektionen **Miljøer** vælge **Microsoft Azure-indstillinger**.

![Indstillinger for Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. På siden **Projektindstillinger** skal du på fanen **Azure-forbindelser** vælge **Autoriser**. Det gør det muligt at udrulle miljøer på dette projekt.

![Azure-forbindelser](./media/2AzureConnectors.png)

3. Vælg **Autoriser** igen for at give administratorsamtykke.

![Giv administratorsamtykke](./media/3GrantAdminConsent.png)

4. Accepter anmodningen om tilladelse.

![Accepter anmodningen om tilladelse](./media/4AcceptPermissionRequest.png)

Autorisationen er nu fuldført. 

![Autorisation er fuldført](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Give Dynamics Deployment Services adgang til dit Azure-abonnement

1. Gå til [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade), og vælg dit abonnement. Dynamics Deployment Services skal have adgang til dette abonnement for at kunne udrulle miljøer.

![Abonnementsoplysninger for Azure](./media/6AzureSubscription.png)

2. Vælg **Adgangskontrol (IAM)** i navigationsruden, og vælg derefter **Tilføj rolletildeling**.
3. Vælg **Bidragyderrolle** i skyderen på højre side, og find og vælg **Dynamics Deployment Services** på listen. 
4. Vælg **Gem**.

![Abonnementsadgang](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Tilføj en abonnementsforbindelse til et LCS-projekt

1. I dit LCS projekt på siden **Microsoft Azure-indstillinger** skal du vælge **Tilføj** for at tilføje en ny forbindelse.
2. Angiv dit Azure-abonnements-id. Du kan finde dit abonnements-id for Azure i [Azure-portalen](https://ms.portal.azure.com/) under **Indstillinger** nederst til venstre på skærmen.
3. I feltet **Konfigurer til at bruge Azure Resource Manager** skal du vælge **Ja**.
4. Kontroller, at Azures abonnement-AAD-lejerdomæne stemmer overens med det domæne, som ejer Azure-abonnementet, du bruger, og vælg **Næste**.
5. På skærmen **Microsoft Azure-opsætning** skal du vælge **Næste** for at bekræfte. Hvis du modtager en fejl på skærmen, kan du gå tilbage til sektionen [Giv Dynamics Deployment Services adgang til Azure-abonnementet](#provide) i dette emne og sikre dig, at du har fuldført alle trinene.
6. Hent Azure-administrationscertifikatet ned i en lokal mappe på computeren, og overfør det derefter til Azure Management Portal ved at gå til **Indstillinger** > **Administrationscertifikater**. Dette certifikat vil give LCS mulighed for at kommunikere med Azure på dine vegne. Du kan springe dette trin over, hvis brugeren har adgang til abonnementet.
7. Vælg **Næste**.
8. Vælg det Azure-område, det skal udrulles i, og vælg et datacenter, der ligger tæt på det sted, hvor du vil bruge dette system.
9.  Vælg **Opret forbindelse**.

Du har oprettet forbindelse til dit Azure-abonnement. Du kan nu udrulle skybaserede Dynamics 365 Finance-miljøer.




[!INCLUDE[footer-include](../includes/footer-banner.md)]