---
title: Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier
description: Denne artikel indeholder oplysninger om, hvordan du abonnerer på og udruller Project Operations til ressource/ikke-lagerbaserede scenarier.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842008"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Tilmeld dig abonnement på prøveversion af Project Operations for ressource/ikke-lagerførte scenarier

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_



Denne artikel redegør for, hvordan du abonnerer på prøvetilbuddet og udruller Project Operations-miljøet til ressource/ikke-lagerbaserede scenarier.

## <a name="prerequisites"></a>Forudsætninger
- Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder. Du kan oprette en lejer under indløsningen af første tilbud. 
- Hvis du vil udrulle et Finance-miljø, skal du have et gyldigt Azure-abonnement, der faktureres pr. miljø. Du kan bruge virksomhedens eksisterende abonnement eller bruge en [Azure-prøveversion](https://azure.microsoft.com/free/) til at komme i gang. CDS-miljøet er gratis i 30 dage.

> [!IMPORTANT]
> Kun én person, lejeradministratoren, i en organisation skal udføre denne opgave. Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.
> 
> Prøveversioner er til engangsbrug i lejeren. Du kan kun køre en prøveversion én gang. Det anbefales, at du opretter en ny lejer med henblik på prøveversionen.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – prøveversion 

Før du går i gang, skal du sikre dig, at du er logget på en browser med brugerens arbejdskonto i lejeren, hvor du vil installere prøveversionen af Project Operations.

1. Indløs første tilbudskode **Dynamics 365 Project Operations** her [Project Operations-prøveversion](https://aka.ms/try-po).
2. Bekræft din ordre..

  Du får vist en bekræftelse på, at tilbuddet blev indløst.

### <a name="dynamics-365-finance-preview-trial"></a>Prøveversion af Dynamics 365 Finance

Gå til [Prøveversion af Dynamics 365 til Finance](https://aka.ms/trypoche), og gentag trinnene fra forrige sektion med tilbuddet Tilmeld dig cloudværtsmiljøet.  

## <a name="assign-licenses"></a>Tildele licenser

> [!IMPORTANT]
> Du skal have administratoradgang til din organisations Microsoft 365-portal for at fuldføre følgende trin.

1. Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenserne til brugerne.

2. På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.

3. Kontrollér, at **Dynamics 365 Project Operations**-licensen er valgt, og vælg **Gem ændringer**.

> [!NOTE]
> Tilbuddet om prøveversionen af Finance behøver ikke at være tildelt en bruger.

## <a name="start-a-new-project-in-lcs"></a>Start et nyt projekt i LCS

Opret et nyt LCS-projekt som beskrevet i artiklen [Start et nyt projekt i LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Tilføj et Azure-abonnement til et LCS-projekt

Fuldfør denne opgave ved at følge trinnene i artiklen [Tilføj af et Azure-abonnement til LCS-projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Udrul Finance-demonstrationsmiljøet med Project Operations for ressource/ikke-lagerførte scenarier

Følg vejledningen i artiklen [Klargør et nyt miljø](resource-provision-new-environment.md) for at fuldføre installationen. Brug [demonstrationsmiljøets](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) udrulningstype til prøveversionen. 

## <a name="install-cds-setup-and-configuration-data"></a>Installer CDS-konfiguration og konfigurationsdata

Installer CDS-konfiguration og konfigurationsdata som beskrevet i artiklen [Konfigurer og anvend konfigurationsdata i Common Data Service](resource-apply-pro-setup-config-data.md).
Fuldfør først dette trin, når demomiljøet Finance er udrullet, og demodataene er klar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
