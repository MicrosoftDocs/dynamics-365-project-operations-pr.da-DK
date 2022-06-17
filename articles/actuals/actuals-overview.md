---
title: Faktiske værdier
description: Denne artikel indeholder oplysninger om, hvordan du arbejder med faktiske værdier i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924791"
---
# <a name="actuals"></a>Faktiske

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Faktiske værdier repræsenterer den gennemgåede og godkendte økonomiske og planlægningsmæssige status for et projekt. De oprettes, når tids-, udgifts- og materialeforbrugsposter, kladdeposteringer og fakturaer godkendes.

> [!IMPORTANT]
> Faktiske værdier bør ikke redigeres eller slettes i systemet. I modsat fald kan den økonomiske integritet og enhver integration med andre økonomiske systemer og regnskabssystemer blive berørt. Microsoft Dynamics 365 Project Operations giver dig mulighed for at tilbageføre og erstatte faktiske værdier på forskellige tidspunkter i forretningsprocessen for dine projekters livscyklus.

## <a name="recording-actuals-based-on-project-events"></a>Registrering af faktiske oplysninger baseret på projekthændelser

I Project Operations registreres de økonomiske transaktioner, der indtræffer i løbet af en projektaftales livscyklus, som faktiske værdier. Oprettelsen af faktiske værdier ved forskellige hændelser i livscyklussen varierer, afhængigt af om projektengagementet bruger tids- og materialefaktureringsmodellen eller faktureringsmodellen med fast pris, og om det er i fasen før salg eller er et internt projekt.

I følgende artikler forklares konsekvensen for tabellen Faktiske værdier af forskellige hændelser for forskellige variationer:

- [Faktiske værdiers påvirkning i forbindelse med tids- og materialeengagement](ActualsonTM.md)
- [Faktisk værdiers påvirkning i en fast prisengagement](ActualonFP.md)
- [Faktisk værdiers påvirkning i forbindelse med en aftales førsalgsfase](ActualonPreSales.md)
- [Faktiske værdiers konsekvens for et internt projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
