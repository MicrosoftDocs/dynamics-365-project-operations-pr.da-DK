---
title: Rejserekvisitioner
description: Dette emne indeholder oplysninger om rejserekvisitioner.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: e05f54349eaa09dd22331ff07950542dd326e711
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001734"
---
# <a name="travel-requisitions"></a>Rejserekvisitioner

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En rejserekvisition viser de udgifter, der vil blive afholdt i forbindelse med rejsen. En rejserekvisition er indsendt til gennemsyn og kan bruges til at autorisere udgifter.

Du skal muligvis indsende en rejserekvisition, før du afholder en eventuel udgift, der skal betales af organisationen. Dette krav gælder, uanset om du opkræves udgifterne på et af firmaets kreditkort, betaler med kontanter, som du har modtaget fra et kontantforskud, eller afholder udgifter af egen lomme, som refunderes af organisationen.

Rejserekvisitioner og -politikker kan bruges til at administrere organisationens udgifter. Hvis din organisation f.eks. arbejder på et fastprisprojekt, der kræver rejse, skal rejseudgifterne for projektets teammedlemmer være inden for projektbudgettet. Ved at kræve, at rejseudgifter godkendes, før de afholdes, kan organisationen være med til at sikre, at projektet forbliver inden for budgettet.

## <a name="configuration"></a>Konfiguration 

Rejserekvisitioner kan konfigureres som "obligatoriske" ved at aktivere parameteren "Forhåndsgodkendelse af rejser er obligatorisk" i parametrene for udgiftsstyring. 

## <a name="create-and-submit-a-travel-requisition"></a>Opret og indsend en rejserekvisition

1. Gå til **Mine udgifter: rejserekvisition**, og vælg **Ny rejserekvisition**.
2. Angiv et formål og en destination for rekvisitionen.
3. I feltet **Rejsebeskrivelse** skal du angive eventuelle yderligere oplysninger. 
4. Opret et udgiftslinjeelement for hver af de forventede udgifter, f.eks. fly, måltider eller billeje. Medtag den skønnede dato, beløb og valutaen for de enkelte udgifter. 
5. Vælg **Gem**, når du er færdig med at tilføje de forventede udgifter.
6. Når du er klar til at indsende rejserekvisitionen, skal du vælge **Arbejdsproces** > **Indsend**.

Du kan få vist dine godkendte rejserekvisitioner under **Mine udgifter: rejserekvisition**. 

## <a name="view-available-travel-requisitions"></a>Få vist tilgængelige rejserekvisitioner

Du kan få vist alle dine godkendte rejserekvisitioner under **Mine udgifter: rejserekvisitioner**.

## <a name="approve-travel-requisitions"></a>Godkend rejserekvisitioner

Vælg den rejserekvisition, du vil godkende, og vælg derefter **Arbejdsproces** > **Godkend**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Indsend en udgiftsrapport ved hjælp af den godkendte rejserekvisition

1. Opret en ny udgiftsrapport og vælg i udgiftsrapportens overskrift, og fra listen over godkendte rejserekvisitioner **Tilknyt til rejserekvisition**.
2. Feltet **Rejserekvisitionsbeløb** opdateres automatisk i udgiftsrapportens overskrift.
3. Tilføj de omkostninger, der er påløbet under rejsen. Hvis feltet **Forhåndsgodkendt** er aktiveret, opdateres det afstemte beløb og det godkendte beløb for den specifikke udgiftsart.

> [!NOTE]
> Når du tilknytter en udgiftsrapport til en godkendt rejserekvisition, kan transaktionsbeløbet ikke være større end det godkendte beløb. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]