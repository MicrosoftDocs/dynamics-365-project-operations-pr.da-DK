---
title: Oversigt over tilstande for ressourcestyring
description: Dette emne indeholder oplysninger om funktionaliteten for ressourcestyring i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 5c0f98a6f08129ebef9b6d3fed1cc85969aa347c815a643d3c8dd639b42c0e8c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008219"
---
# <a name="resource-management-modes-overview"></a>Oversigt over tilstande for ressourcestyring

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Dynamics 365 Project Operations understøtter to tilstande, således at du kan udføre den overordnede reservationsstrøm. Administrationstilstanden defineres som en projekt parameter og kan ændres, hvis din virksomhed har behov for at skifte.    

## <a name="central-mode"></a>Central tilstand
For organisationer, der centraliserer fordelingen for ressourcer til projekter, er den centrale tilstand en måde, hvorpå det sikres, at projektledere kan definere ressourcekrav på projektniveau. Opfyldelsen af ressourcekravene er uddelegeret til en Resource Manager. Projektledere kan acceptere eller afvise ressourcer, der er foreslået af Resource Manager.

![Central tilstand.](./media/resource-management-central.png)

Hvis du vil administrere ressourcer med den centrale tilstand, skal du se:

- [Tildel generiske reserverbare ressourcer til en opgave og generering af ressourcekrav](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserver navngivne ressourcer fra ressourcekrav](/dynamics365/project-service/book-named-resource)
- [Send en anmodning om ressource(r)](/dynamics365/project-service/submit-resource-request)
- [Opfyld en ressourceanmodning](/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptere eller afvise en foreslået projektressource i en ressourceanmodning](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridtilstand
For organisationer, der har behov for fleksibilitet i fordelingen af ressourcer, giver hybridtilstanden mulighed for, at både projektledere og Resource Manager kan reservere ressourcer.

![Hybridtilstand.](./media/resource-management-hybrid.png)

Ud over den understøttede centrale tilstand skal du se følgende emner for at administrere alle andre understøttede reservationsflows i hybridtilstanden:

Reserver en ressource direkte til et projekt:
- [Reservere navngivne reserverbare ressourcer til et projektteam og tildele opgaver](/dynamics365/project-service/assign-named-bookable-resource)

Reserver en ressource fra et ressourcekrav:
- [Tildel generiske reserverbare ressourcer til en opgave og generering af ressourcekrav](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserver navngivne ressourcer fra ressourcekrav](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]