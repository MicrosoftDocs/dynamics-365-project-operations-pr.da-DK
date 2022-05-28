---
title: Forretningstransaktioner i Project Operations
description: Dette emne indeholder en oversigt over begrebet forretningstransaktioner i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582197"
---
# <a name="business-transactions-in-project-operations"></a>Forretningstransaktioner i Project Operations

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I Microsoft Dynamics 365 Project Operations er *forretningstransaktion* et abstrakt begreb, der ikke repræsenteres af et objekt. Men nogle almindelige felter og processer på objekter er designet til at bruge konceptet forretningstransaktioner. Følgende objekter bruger dette begreb:

- Tilbudslinjedetaljer
- Kontraktlinjedetaljer
- Estimatlinjer
- Kladdelinjer
- Faktiske

Blandt disse objekter bliver tilbudslinjedetaljer, kontraktlinjedetaljer og estimatlinjer knyttet til *estimatfasen* i projektets livscyklus. Objekterne Kladdelinjer og Faktiske værdier knyttes til *udførelsesfasen* i projektets livscyklus.

I Project Operations behandles poster i alle fem af disse objekter som forretningstransaktioner. Den eneste forskel er, at poster i de objekter, der er knyttet til estimatfasen (tilbud, linjedetaljer, kontraktlinjedetaljer og estimatlinjer), betragtes som *økonomiske prognoser*, mens poster i de objekter, der er knyttet til udførelsesfasen (kladdelinjer og faktiske værdier), betragtes som *økonomiske fakta*, der allerede er indtruffet.

Der er flere oplysninger under [Estimater](../project-management/estimating-projects-overview.md) og [Faktiske](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepter, der er entydige for forretningstransaktioner

Følgende koncepter er unikke for konceptet med forretningstransaktioner:

- Transaktionstype
- Transaktionsklasse
- Transaktionsoprindelse
- Transaktionsforbindelse

### <a name="transaction-type"></a>Transaktionstype

Transaktionstype repræsenterer timingen og konteksten af den økonomiske indvirkning på et projekt. Den defineres af en grupperet indstilling, der har følgende understøttede værdier i Project Operations:

- Omkostning
- Projektkontrakt
- Ikke-faktureret salg
- Faktureret salg
- Organisationsinternt salg
- Ressourceenhedsomkostning

### <a name="transaction-class"></a>Transaktionsklasse

Transaktionsklasse repræsenterer de forskellige typer af omkostninger, der opstår på projekter. Den defineres af en grupperet indstilling, der har følgende understøttede værdier i Project Operations:

- Tid
- Udgift
- Materiale
- Gebyr
- Milepæl
- Skat

> [!NOTE]
> Værdien af **Milepæl** bruges typisk af forretningslogikken til fastprisfakturering i Project Operations.

### <a name="transaction-origin"></a>Transaktionsoprindelse

Transaktions oprindelse er et objekt, der gemmer oprindelsen af hver enkelt forretningstransaktion for at hjælpe med rapportering og sporing. Når projektkørslen starter, opretter hver forretningstransaktion en anden forretningstransaktion, der igen vil oprette endnu en forretningstransaktion osv.

### <a name="transaction-connection"></a>Transaktionsforbindelse

Transaktionsforbindelse er et objekt, der lagrer relationen mellem to lignende forretningstransaktioner, f.eks. omkostninger og relaterede faktiske salgsværdier, eller tilbageførsler, der udløses af faktureringsaktiviteter, f.eks. fakturabekræftelse eller fakturakorrektion.

Tilsammen hjælper objekterne Transaktionsoprindelse og Transaktionsforbindelse dig med at spore relationer mellem forretningstransaktioner og handlinger, der medførte, at der blev oprettet en bestemt forretningstransaktion.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
