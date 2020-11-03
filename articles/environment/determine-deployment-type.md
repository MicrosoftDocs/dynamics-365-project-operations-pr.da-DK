---
title: Vælg din udrulningstype
description: Dette emne indeholder oplysninger, som hjælper dig med at fastlægge den korrekte udrulningstype for Project operations for din virksomhed.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074176"
---
# <a name="determine-your-deployment-type"></a>Vælg din udrulningstype

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

> [!IMPORTANT]
> Når du har købt licensen, skal du starte her for at fastlægge den bedste udrulningsmodel til Dynamics 365 Project operations ved hjælp af det [Styrede installationsflow](https://aka.ms/provisionprojectoperations).
> Når du har afsluttet det styrede installationsflow, omdirigeres du til den korrekte administrationsportal for at fuldføre installationen. Se detaljerne om udrulning for at fuldføre installationen.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Eksisterende Dynamics-kunder, som anvender Dynamics 365 Project Service Automation
Project operations omfatter de funktioner, der blev leveret sammen med Project Service Automation. Der frigives en opgraderingssti for disse kunder på et senere tidspunkt.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Eksisterende Dynamics 365 Finance-kunder, som anvender projektstyring og regnskab 

Eksisterende Finance-kunder, der benytter funktionen projektstyring og regnskab, kan fortsætte med at bruge denne funktion som hidtil. Se [Project Operations for lagerbaserede/produktionsordrescenarier](#pma).


## <a name="deployment-types"></a>Udrulningstyper
Project Operations understøtter forskellige udrulningsmuligheder, så de passer til dine behov. Uanset om du er ny eller eksisterende Dynamics 365-kunde, kan Project Operations opfylde dine behov.

Vores [Spørgeskema vedrørende udrulning](https://aka.ms/provisionprojectoperations) hjælper dig med at finde den rette udrulning. Resultaterne fører dig hen imod en af følgende udrulningstyper:

- [Lille udrulning – aftale til proformafakturering](#lite)
- [Project Operations for ressource/ikke-lagerscenarier](#integrated)
- [Project Operations for lagerbaserede/produktionsordrescenarier](#pma)

Project Operations understøtter scenarier med lagerførte-/produktionsordre og ikke-lagerførte-/ressourcebaserede scenarier i samme miljø via konfigurationer på juridisk enhedsniveau. Contoso kan f eks. bruge egenskaberne for lagerbaserede ordrer/produktionsordre i deres amerikanske produktionsanlæg (juridisk enhed = Contoso Manufacturing USA). Contoso kan bruge de ikke-lagerbaserede/ressourcebasered egenskaber i deres servicevirksomhed Contoso Robotics Arms i Storbritannien (juridisk enhed = Contoso Robotics Storbritannien).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lille udrulning - aftale til proformafakturering

Den lille udrulning inkluderer følgende funktioner:

- Projektplanlægning ved hjælp af Microsoft Project til internettet
- Flerdimensionel prisfastsættelse
- Fælles ressourcestyring
- Tidssporing
- Grundlæggende udgifter
- Fakturaforslag

#### <a name="deployment-steps"></a>Installationsprocessen
Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).

I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](lite-preview-subscription-sign-up.md) og [Klargøring af nyt miljø](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations for ressource/ikke-lagerscenarier
Project Operations for ressource/ikke-lagerførte scenarier omfatter følgende funktioner:
  
- Projektplanlægning ved hjælp af Microsoft Project til internettet
- Flerdimensionel prisfastsættelse
- Fælles ressourcestyring
- Tidssporing
- Grundlæggende udgifter
- Fuld udgift
- Optisk tegngenkendelseskvittering
- Fuld fakturering
- Indtægtsanerkendelse

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
- Materialesupport

#### <a name="deployment-steps"></a>Installationsprocessen
Find den bedste udrulningsmodel til Project Operations ved hjælp af [Spørgeskemaet om udrulning](https://aka.ms/provisionprojectoperations).

I forbindelse med denne installation kan du se [Tilmelding til eksempelabonnementer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) og [Klargøring af nyt miljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

