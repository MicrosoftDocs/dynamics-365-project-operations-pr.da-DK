---
title: Analyse af projekttilbud
description: Denne emne indeholder oplysninger om analyse af projekttilbud.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750486"
---
# <a name="analysis-of-project-quotes"></a>Analyse af projekttilbud

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
