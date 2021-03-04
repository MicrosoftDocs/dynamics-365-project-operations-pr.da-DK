---
title: Oversigt over tilstande for ressourcestyring
description: Dette emne indeholder oplysninger om funktionaliteten Ressourcestyring i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118511"
---
# <a name="resource-management-modes-overview"></a>Oversigt over tilstande for ressourcestyring

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Dynamics 365 Project Operations understøtter to tilstande, for at du kan udføre det overordnede reservationsflow. Administrationstilstanden defineres som en projekt parameter og kan ændres, hvis din virksomhed har behov for at skifte.    

## <a name="central-mode"></a>Central tilstand
For organisationer, der centraliserer fordelingen for ressourcer til projekter, er den centrale tilstand en måde, hvorpå det sikres, at projektledere kan definere ressourcekrav på projektniveau. Opfyldelsen af ressourcekravene er uddelegeret til en Resource Manager. Projektledere kan acceptere eller afvise ressourcer, der er foreslået af Resource Manager.

![Central tilstand](./media/resource-management-central.png)

Hvis du vil administrere ressourcer med den centrale tilstand, skal du se:

- [Tildel generiske reserverbare ressourcer til en opgave og generering af ressourcekrav](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserver navngivne ressourcer fra ressourcekrav](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Send en anmodning om ressource(r)](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Opfyld en ressourceanmodning](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptere eller afvise en foreslået projektressource i en ressourceanmodning](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridtilstand
For organisationer, der har behov for fleksibilitet i fordelingen af ressourcer, giver hybridtilstanden mulighed for, at både projektledere og Resource Manager kan reservere ressourcer.

![Hybridtilstand](./media/resource-management-hybrid.png)

Ud over den understøttede centrale tilstand skal du se følgende emner for at administrere alle andre understøttede reservationsflows i hybridtilstanden:

Reserver en ressource direkte til et projekt:
- [Reservere navngivne reserverbare ressourcer til et projektteam og tildele opgaver](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Reserver en ressource fra et ressourcekrav:
- [Tildel generiske reserverbare ressourcer til en opgave og generering af ressourcekrav](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserver navngivne ressourcer fra ressourcekrav](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]