---
title: Økonomiske estimater for ressourcetid på projekter
description: Dette emne indeholder oplysninger om, hvordan økonomiske estimater for tid beregnes.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4be4c8087005ae66a54d40ac88017df591c56eca64f04b00cf34b0e5a8a09ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998679"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Økonomiske estimater for ressourcetid på projekter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Økonomiske estimater for tid beregnes på baggrund af tre faktorer: 

- Typen af generiske eller navngivne teammedlemmer, der er tildelt hver enkelt bladnodeopgave i projektplanen. 
- Typen eller kompleksiteten af arbejdet.
- Fordelingen af indsatsen for ressourcens tildeling på opgaven. 

De første to faktorer påvirker enhedsomkostningen eller fakturasatsen for en ressources tildeling. Enhedsomkostningen eller fakturasatsen for en ressourcetildeling bestemmes af attributterne for den tildelte ressource. Disse attributter omfatter den afdeling, som ressourcen tilhører, og ressourcens standardrolle. Du kan også tilføje brugerdefinerede attributter for ressourcen, der er relevante for din virksomhed, såsom standardtitel eller erfaringsniveauet, og få dem til at påvirke enhedsomkostningen eller fakturasatsen for tildelingen.
Ud over ressourcens attributter kan arbejdsattributter såsom opgaven også påvirke enhedens faktureringssats eller omkostningssatsen for tildelingen. Hvis visse opgaver f.eks. er mere komplekse, resulterer ressourcens tildeling til disse specifikke opgaver i en højere enhedsomkostninger eller faktureringssats end opgaver, der er mindre komplekse.   

Den tredje faktor angiver antallet af timer til denne sats. I de tilfælde, hvor en opgave dækker to prisperioder, er det sandsynligt, at omkostningsfastsættelsen og prisfastsættelsen for første del af ressourcetildelingen for den pågældende opgave er forskellig fra den anden del af opgaven. Den anslåede indsats på de enkelte ressourcetildelinger er en kompleks værdi, der lagres med den daglige distribution af indsats pr. dag.

Du kan finde en detaljeret vejledning om, hvordan du konfigurerer brugerdefinerede attributter for arbejde og ressourcer som prisfastsættelses- og kostprisdimension, i [Oversigt over prisfastsættelsesdimensioner](../pricing-costing/pricing-dimensions-overview.md).

Det økonomiske estimat for hver ressourcetildeling beregnes som **sats/time for tildelingerne ganges med antallet af timer.**  På samme måde som den anslåede indsats er det økonomiske estimat for omkostninger og omsætning for hver ressourcetildeling en kompleks værdi, der lagres med den daglige distribution af pengebeløb pr. dag. 

## <a name="summarizing-financial-estimates-for-time"></a>Opsummering af økonomiske estimater for tid
Et økonomisk estimat for tid på en bladnodeopgave er summen af de økonomiske estimater for alle ressourcetildelinger for den pågældende opgave.

Et økonomisk estimat for tid på en hovedopgave eller en overordnet opgave er summen af de økonomiske estimater for alle de tilhørende underordnede opgaver. Dette er den anslåede arbejdsomkostning for projektet. 

![Ressourceestimater.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standarder for kostpris og omkostningsvaluta

Standardkostprisværdien kommer fra de prislister, der er knyttet til den kontraherende enhed i projektet. Et projekts omkostningsvaluta er altid valutaen for den kontraherende enhed, der indgår i projektet. På en ressourcetildeling gemmes det økonomiske omkostningsestimat i projektets omkostningsvaluta. Nogle gange er den valuta, som omkostningssatsen er angivet i på prislisten, en anden end projektets omkostningsvaluta. I disse tilfælde konverterer programmet den valuta, som kostprisen er konfigureret i for projektets valuta. I gitteret **Estimater** vises og opsummeres alle omkostningsestimater i projektets omkostningsvaluta. 

## <a name="default-bill-rate-and-sales-currency"></a>Standarder for faktureringshyppighed og salgsvaluta

Standardsalgsprisen kommer fra de projektprislister, der er knyttet til den relaterede projektkontrakt, hvis aftalen er vundet, eller fra det relaterede projekttilbud, hvis handlen stadig er i før-salgsfasen. Projektets salgsvaluta er altid projekttilbuddets eller projektkontraktens valuta. På en ressourcetildeling gemmes det økonomiske salgsestimat i projektets salgsvaluta. I modsætning til omkostninger kan den salgspris, der er konfigureret på prislisten, aldrig være en anden end projektets salgsvaluta. Der er ingen scenarier, hvor valutakonvertering er nødvendig. I gitteret **Estimater** vises og opsummeres alle salgsestimater i projektets salgsvaluta. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
