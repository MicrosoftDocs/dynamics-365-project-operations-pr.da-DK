---
title: Vælg din udrulningstype
description: Dette emne indeholder oplysninger, som hjælper dig med at fastlægge den korrekte udrulningstype for Project operations for din virksomhed.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 4be8e69c5b6ff1ed65e9484a9b427bb428f7ff3e6dc597c615d5586da52867ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994629"
---
# <a name="determine-your-deployment-type"></a>Vælg din udrulningstype

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

> [!IMPORTANT]
> Når du har købt licensen, skal du starte her for at finde den bedste udrulningsmodel Dynamics 365 Project Operations ved hjælp af [vejledningen til installationsflow](https://aka.ms/provisionprojectoperations).
> Når du har afsluttet det styrede installationsflow, omdirigeres du til den korrekte administrationsportal for at fuldføre installationen. Se detaljerne om udrulning for at fuldføre installationen.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Eksisterende Dynamics-kunder, som anvender Dynamics 365 Project Service Automation
Project operations omfatter de funktioner, der blev leveret sammen med Project Service Automation. Der udgives en opgraderingssti for disse kunder i den første frigivelsesbølge i 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Eksisterende Dynamics 365 Finance-kunder, som anvender projektstyring og regnskab 

Eksisterende Finance-kunder, der benytter funktionen Projektstyring og regnskab, kan fortsætte med at bruge den, som hidtil. Se [Project Operations for lagerbaserede/produktionsordrescenarier](#pma).


## <a name="deployment-regions"></a>Installationsområder
Du kan se, hvilke områder der understøtter udrulningen af Project Operations, under [Geografisk tilgængelighed for Dynamics 365 og i rapporten Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Vælg **Vis rapport**, og udvid **Dynamics 365 > Operations-programmer > Dynamics 365 Project Operations** for at få vist de understøttede områder.

## <a name="deployment-types"></a>Udrulningstyper
Project Operations understøtter forskellige udrulningsmuligheder, så de passer til dine behov. Uanset om du er ny eller eksisterende Dynamics 365-kunde, kan Project Operations opfylde dine behov.

Vores [Spørgeskema vedrørende udrulning](https://aka.ms/provisionprojectoperations) hjælper dig med at finde den rette udrulning. Resultaterne fører dig hen imod en af følgende udrulningstyper:

- [Lille udrulning – aftale til proformafakturering](#lite)
- [Project Operations for ressource/ikke-lagerscenarier](#integrated)
- [Project Operations for lagerbaserede/produktionsordrescenarier](#pma)

Project Operations understøtter scenarier med lagerførte-/produktionsordre og ikke-lagerførte-/ressourcebaserede scenarier i samme miljø via konfigurationer på juridisk enhedsniveau. Contoso kan f.eks. bruge funktionerne til lager-/produktionsordre i deres facilitet til produktion i USA (juridisk enhed = Contoso Manufacturing USA). Contoso kan bruge de ikke-lagerbaserede/ressourcebaserede funktioner i deres serviceringsfacilitet for Contoso Robotics Arms i Storbritannien (juridisk enhed = Contoso Robotics Storbritannien).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lille udrulning - aftale til proformafakturering

Den lille udrulning inkluderer følgende funktioner:

- Salgsproces for projekter, der udvider oplevelserne i programmet Dynamics 365 Sales
- Projektplanlægning ved hjælp af Microsoft Project til internettet
- Flerdimensionel prisfastsættelse
- Fælles ressourcestyring
- Tidssporing
- Grundlæggende udgifter
- Proformafakturering, som projektlederen skal gennemgå og redigere 

#### <a name="deployment-steps"></a>Installationsprocessen
Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).

I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](lite-preview-subscription-sign-up.md) og [Klargøring af nyt miljø](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations for ressource/ikke-lagerscenarier
Project Operations for ressource/ikke-lagerførte scenarier omfatter følgende funktioner:
 
- Salgsproces for projekter, der udvider programmet Dynamics 365 Sales
- Projektplanlægning ved hjælp af Microsoft Project til internettet
- Flerdimensionel prisfastsættelse
- Fælles ressourcestyring
- Tidssporing
- Grundlæggende udgifter
- Fuld udgift
- Optisk tegngenkendelseskvittering
- Proforma og kundeorienteret fakturering 
- Indtægtsføring for projekter

#### <a name="deployment-steps"></a>Installationsprocessen
Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).

I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](resource-sign-up-preview-subscription.md) og [Klargøring af nyt miljø](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations for lagerbaserede/produktionsordrescenarier

- Ofte stillede spørgsmål om brug af WBS
- Ressourcestyring
- Tidssporing
- Fuld udgift
- Optisk tegngenkendelseskvittering
- Fuld fakturering
- Indtægtsanerkendelse
- Produktionsordrer
- Understøttelse af lagerførte materialer med lager

#### <a name="deployment-steps"></a>Installationsprocessen
Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).

I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) og [Klargøring af nyt miljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]