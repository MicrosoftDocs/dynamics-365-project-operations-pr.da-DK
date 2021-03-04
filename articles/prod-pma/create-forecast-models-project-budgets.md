---
title: Opret prognosemodeller for projektbudgetter
description: I dette emne beskrives det, hvordan du kan oprette en prognosemodel for resterende budgetter.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074308"
---
# <a name="create-forecast-models-for-project-budgets"></a>Opret prognosemodeller for projektbudgetter 

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan du kan oprette en prognosemodel for resterende budgetter. I et projekt, der er underlagt budgetstyring, bruges der to typer budgetter: oprindelig og resterende. Når du opretter et projektbudget, skal du angive de oprindelige og resterende budgetprognosemodeller, der er oprettet på siden **Prognosemodeller**. Projektbudgetter, der er baseret på de angivne modeller, oprettes, når du bekræfter projektbudgettet.

> [!NOTE]
> En prognosemodel, der bruges til budgetstyring, kan ikke have en undermodel eller bruges som undermodel.

1. Vælg **Projektstyring og regnskab** > **Opsætning** > **Prognoser**  > **Prognosemodeller**.
2. Vælg **Ny** for at oprette en ny budgetmodel, og angiv derefter et model-id-nummer og et navn for den nye model. 
3. Angiv indstillingen **Afbrudt** til **Ja** for at forhindre ændringer af prognoselinjerne i prognosemodellen. 
4. Hvis de prognoselinjer, som modellen er knyttet til, skal oprette likviditetsprognoser i finansbogholderiet, skal du angive **Inkluder i likviditetsprognoser** til **Ja.** 
5. Hvis du vil bruge projektdatoen som fakturadatoen, skal du angive **Prognosefakturadato** til **Ja**. 
6. I feltet **Budgettype** skal du vælge en af følgende modeltyper:

   - **Oprindeligt budget** : Brug de oprindelige budgetbeløb, der er bindende, når det første budget oprettes og godkendes.
   - **Resterende budget** : Brug de resterende budgetbeløb i projektets levetid. Saldiene i denne prognosemodel reduceres med faktiske transaktioner og forøges eller formindskes via budgetrevisioner.
   - **Overfør** : Brug overførte budgetbeløb til projektet. Overførsel er en valgfri proces, der kan køres for at overføre ubrugte budgetbeløb fra et regnskabsår til et andet.

7. Angiv følgende indstillinger efter behov:

   - Aktiver **Prognosefakturadato** for at bruge projektdataene som fakturadato.
   - Aktivér **Prognose med IGVA** for at udarbejde en prognose, der er baseret på igangværende arbejde, og vælg derefter typen af IGVA. 
   - Du kan bevare standarden **Budgettype** som **Ingen** eller angive en ny type. Budgettypen kan ikke ændres, når du har ændret en post.     
    > [!NOTE]
    > Hvis du ændrer standardbudgettypen, vil alle andre indstillinger ikke være tilgængelige for opdateringer, og du kan ikke genbruge denne prognosemodel. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]