---
title: Analyse af projekttilbud
description: Denne artikel indeholder oplysninger om analysen af projekttilbud.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9db924c16c5eca17e7962ff1d88b09e581347fa5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919271"
---
# <a name="analysis-of-project-quotes"></a>Analyse af projekttilbud

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analyserer projekttilbud for at anslå rentabiliteten. Det analyserer også, hvor godt tilbuddet er justeret i forhold til kundens forventninger om leveringsdato eller færdiggørelsesdato og om budgettet.

## <a name="profitability-analysis"></a>Rentabilitetsanalyse

Project Service Automation analyserer rentabiliteten ved hjælp af bruttoavancen og den justerede bruttoavance.

- Bruttoavance beregnes ved hjælp af følgende formel:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Den justerede bruttoavance beregnes ved hjælp af følgende formel:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Hvis værdierne for bruttoavance og justeret bruttoavance er forskellige med en bred margen, klassificeres meget af arbejdet i tilbuddet som ikke-fakturerbart.

## <a name="analysis-of-customer-expectations"></a>Analyse af kundens forventninger

Du kan analysere tilbud og oprette diagrammer til kundernes forventninger om tidsplanen og budgettet, hvis du har angivet værdier for følgende felter:

- Feltet **Anmodet leveringsdato** i tilbudsoverskriften.
- Feltet **Kundebudget** for hver tilbudslinje (for projektbaserede linjer og produktbaserede linjer).

Analyse af kundeforventninger om tidsplanen sker ved at sammenligne den seneste slutdato for tilbudslinjedetaljerne med den ønskede leveringsdato på tværs af alle tilbudslinjer i tilbuddet.

Analyse af kundernes forventninger om budgettet sker ved at sammenligne summen af det samlede kundebudget med det tilbudte beløb på tværs af alle tilbudslinjer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
