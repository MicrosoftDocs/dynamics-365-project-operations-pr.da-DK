---
title: Tilføj et Azure-abonnement til et LCS-projekt
description: Denne artikel indeholder oplysninger om, hvordan du opretter forbindelse mellem dit Azure-abonnement og et LCS-projekt.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64ee8cfa7394a08c3d588c0e8f4a73185d9496cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912141"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Tilføj et Azure-abonnement til et LCS-projekt

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Cloud-hostede miljøer skal installeres ved hjælp af et eksisterende Azure-abonnement. Denne artikel redegør for, hvordan du opretter forbindelse mellem eksisterende dit Azure-abonnement og et LCS-projekt. 

## <a name="grant-admin-consent"></a>Giv administratorsamtykke

1. I dit LCS-projekt skal du i sektionen **Miljøer** vælge **Microsoft Azure-indstillinger**.

![Microsoft Azure-indstillinger.](./media/1MicrosoftAzureSettings.png)

2. På siden **Projektindstillinger** skal du på fanen **Azure-forbindelser** vælge **Autoriser**. Det gør det muligt at udrulle miljøer på dette projekt.

![Azure-forbindelser.](./media/2AzureConnectors.png)

3. Vælg **Autoriser** igen for at give administratorsamtykke.

![Giv administratorsamtykke.](./media/3GrantAdminConsent.png)

4. Accepter anmodningen om tilladelse.

![Accepter anmodning om tilladelse.](./media/4AcceptPermissionRequest.png)

Autorisationen er nu fuldført. 

![Autorisation er fuldført.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Give Dynamics Deployment Services adgang til dit Azure-abonnement

1. Gå til [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade), og vælg dit abonnement. Dynamics Deployment Services skal have adgang til dette abonnement for at kunne udrulle miljøer.

![Oplysninger om Azure-abonnement.](./media/6AzureSubscription.png)

2. Vælg **Adgangskontrol (IAM)** i navigationsruden, og vælg derefter **Tilføj rolletildeling**.
3. Vælg **Bidragyderrolle** i skyderen på højre side, og find og vælg **Dynamics Deployment Services** på listen. 
4. Vælg **Gem**.

![Abonnementsadgang.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Tilføj en abonnementsforbindelse til et LCS-projekt

1. I dit LCS projekt på siden **Microsoft Azure-indstillinger** skal du vælge **Tilføj** for at tilføje en ny forbindelse.
2. Angiv dit Azure-abonnements-id. Du kan finde dit abonnements-id for Azure i [Azure-portalen](https://ms.portal.azure.com/) under **Indstillinger** nederst til venstre på skærmen.
3. I feltet **Konfigurer til at bruge Azure Resource Manager** skal du vælge **Ja**.
4. Kontroller, at Azures abonnement-AAD-lejerdomæne stemmer overens med det domæne, som ejer Azure-abonnementet, du bruger, og vælg **Næste**.
5. På skærmen **Microsoft Azure-opsætning** skal du vælge **Næste** for at bekræfte. Hvis du modtager en fejlmeddelelse på dette skærmbillede, skal du gå tilbage til afsnittet [Giv Dynamics Deployment Services adgang til Azure-abonnementet](#provide) i denne artikel og sikre dig, at du har fuldført samtlige trin.
6. Hent Azure Management Certificate til en lokal mappe på din computer. Bed din Azure-abonnementsadministrator om at overføre certifikatet til Azure Management Portal ved at vælge abonnementet og gå til **Indstillinger** > **Administrationscertifikater**. Med dette certifikat kan LCS kommunikere med Azure på dine vegne. Du kan springe dette trin over, hvis brugeren har adgang til abonnementet.
7. Vælg **Næste**.
8. Vælg det Azure-område, det skal udrulles i, og vælg et datacenter, der ligger tæt på det sted, hvor du vil bruge dette system.
9.  Vælg **Opret forbindelse**.

Du har oprettet forbindelse til dit Azure-abonnement. Du kan nu udrulle cloudværtsmiljøer til Dynamics 365 Finance.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
