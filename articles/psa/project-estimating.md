---
title: Projektomkostninger og -omsætning
description: Dette emne indeholder oplysninger om estimering af projektomkostninger og -omsætning.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 279c1119d334a7f60906e33b3fc7ca22ff9a360d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148321"
---
# <a name="project-costs-and-revenue"></a>Projektomkostninger og -omsætning

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektestimater giver en økonomisk visning af det arbejde, der er estimeret og planlagt i projektplanen. Fanen **Estimater** på siden **Projekter** indeholder en konsekvensberegning over omkostninger og omsætning for det arbejde, du planlægger. Den indeholder også oplysninger om mange foruddefinerede dimensioner. 

> ![Fanen Estimater](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Omkostnings- og salgstal for projektet

Prislister definerer omkostnings- og fakturasatser for roller, som bruges i projektet. Du kan bestemme omkostnings- og indtægtseffekten af arbejdet baseret på de roller, der er knyttet til stillingsnavnet, og den navngivne ressource, der er tildelt til en opgave. Hvis der er opgaver, der ikke har nogen tildelinger (generiske eller navngivne), kan du ikke få omkostnings- eller salgsestimater. Omkostnings- og salgsværdier gælder for den dato, der er angivet i prislisterne.

### <a name="default-cost-price"></a>Standardkostpris  

Alle projekter tilhører en organisation. Denne organisation vises i feltet **Kontraktenhed** i projektet. Den prisliste, der er knyttet til kontraktenheden, bruges til at bestemme enhedens kostpris. Hvis du ønsker at bestemme de korrekte kostpriser for roller for den dato, der er defineret på estimatlinjerne, skal du søge efter kombinationen af rolle, enhed og afdeling på kostprislisten. 

For at kunne beregne kostpriserne for alle opgaver skal alle opgaver tildeles en ressource. Alle ikke-tildelte opgaver har en kostpris på 0,00.

Hvis kombinationen af rolle, enhed og afdeling ikke returnerer en kostpris fra den kontraherende enheds prisliste, ignoreres enheden i systemet. I stedet søges der kun efter kombinationen af rolle og afdeling. Hvis der findes en kostpris, bruges omregningsfaktorer til at konvertere dem til den enhed, du valgte på estimatlinjen.

Hvis kombinationen af rolle og afdeling ikke returnerer en kostpris, ignoreres enheden i systemet. Der søges i stedet efter kombinationen af rolle og enhed for at angive standardprisen (når der er foretaget en konvertering).

Hvis systemet ikke finder en pris for rollen, skal kostprisen som standard være **0,00** på estimatlinjen. Alle beløb for omkostninger på projektets linjer med omkostningsestimater registreres i valutaen for kontraktenheden.

> [!NOTE]
> Som standard gemmer Microsoft Dynamics 365 omkostningsbeløb i grundvalutaen. De omkostningsbeløb, der vises under fanen **Estimater**, vises dog i valutaen for kontraktenheden.  

### <a name="default-sales-price"></a>Standardsalgspris 

Salgsprislisten bestemmes af enten det salgsobjekt, som projektet er knyttet til, eller projektets kunde. Når et salgsobjekt, f.eks. salgsmulighed, tilbud eller kontrakt, er knyttet til projektet, bestemmes salgsobjektets salgspris af den prisliste, der er knyttet til tilbuddet eller kontrakten. Hvis der er en brugerdefineret prisliste for tilbuddet eller kontrakten, vil dette være standardsalgsprislisten for projektestimater. Hvis der ikke er en tilknytning til salgsobjekter, bruges standardsalgsprislisten fra parametrene som projektets standardsalgsprisliste, der stemmer overens med den kundevaluta, der er defineret for projektet.

De enkelte estimatlinjer har tilknyttet en ressourceenhed. Ressourceenheden angiver den afdeling, hvorfra ressourcer er reserveret til at fuldføre opgaven. Du kan bestemme salgsprisen for de tilknyttede roller ved at søge efter kombinationen af rolle, enhed og ressourceenhed på salgsprislisten. Hvis der ikke er nogen tildelinger i opgaven, er salgsprisen for opgaven 0,00.

Hvis kombinationen af rolle, enhed og ressourceenhed ikke returnerer en salgspris fra salgsprislisten, ignoreres enheden i systemet. I stedet søges der kun efter kombinationen af rolle og ressourceenhed. Hvis der findes en salgspris, bruges omregningsfaktorer til at konvertere den til den enhed, som du valgte på salgsestimatlinjen. 

Hvis kombinationen af rolle og ressourceenhed ikke returnerer en salgspris fra salgsprislisten, ignoreres ressourceenheden i systemet. Der søges i stedet efter kombinationen af rolle og enhed for at angive standardprisen (når der er foretaget en konvertering).

Hvis systemet ikke finder en pris for rollen, skal salgsprisen som standard være **0,00** på estimatlinjen.

Fanen **Estimater** indeholder en gittervisning, der viser estimatlinjer. Gitteret indeholder kolonner for enheden, den samlede kostpris og den samlede salgspris, som vist i følgende illustration. 

> ![Gittervisning på fanen Estimater](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Visning med tidsfaser af projektestimater

I visningen med tidsfaser for projektestimater vises estimatdataene fra gittervisningen på tværs af tidslinjen i en tidsskala, du vælger. Estimatdataene er som standard pivoteret i dimensionen **Rolle.**

> ![Visning med tidsfaser af projektestimater](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Fordeling af indsatsestimat baseret på opgavetilstand

I visningen med tidsfaser distribueres den samlede estimerede indsats for opgaven ved at fordele indsatstimer pr. enhedstidsperiode i den valgte tidsskala. Opgavetilstanden bestemmer, hvordan indsatsen fordeles hen over opgavens varighed. De to former for fordeling er **Ligelig fordeling** og **Arbejdstidsbaseret** fordeling.

### <a name="work-hours-based-allocation"></a>Arbejdstidsbaseret fordeling
 
I opgavetilstanden automatisk planlægning angives de daglige standardtimer for opgaveressourcer til hele timesatsen for arbejdet. Denne adfærd gælder, når indsatsen fordeles ved at opdele den hen over varigheden af opgaven i visningen med tidsfaser. Hvis du f.eks. vurderer, at en opgave bliver udført af én ressource i tidsskalaen **Dag**, vil den indsats, der er allokeret pr. dag, ikke overstige arbejdstimer pr. dag defineret i projektets kalender. Indsatsfordelingen sikrer derfor altid, at ressourcerne estimeres til at blive brugt hele dagen.

### <a name="even-allocation"></a>Ligelig fordeling

I planlagt manuelt opgavetilstand bruges arbejdstimerne fra projektkalenderen ikke. Opgaveplanlægningen er i stedet baseret på input fra brugeren. For sådanne opgaver har indsatsfordelingen pr. tidsenhedsperiode i den valgte tidsskala ikke nogen begrænsende faktor. Den samlede indsats på opgaven er ligeledes opdelt og fordelt for hver enhedstidsperiode i den valgte tidsskala. Derfor bestemmer den opgavetilstand, der er defineret for opgaven, indsatsdistributionen eller -allokeringen pr. enhedstidsperiode i tidsfaseinddelte estimater.

## <a name="grouping-and-time-phasing-options"></a>Indstillinger for gruppering og tidsfaser

Visningen med tidsfaser viser fordelingen af indsats-, omkostnings- og salgsestimaterne pr. dag, uge, måned eller år. Estimatdataene er som standard pivoteret i dimensionen **Rolle.** Du kan dog bruge indstillingen **Gruppér efter** til at pivotere på to andre dimensioner: **Kategori** og **Ressource.**

I både gittervisningen og visningen med tidsfaser kan du vælge, hvilke felter der skal vises. Der vises totaler for hver tidsblok nederst i projektet. De indeholder den samlede anslåede indsats, omkostninger og salg for dagen, ugen, måneden eller året. Standardkostpris og salgspris er pr. ikrafttrædelsesdato. De ændres med andre ord for hver ressource på basis af den tidsfaseinddelte visning, du vælger.

## <a name="expense-estimates"></a>Udgiftsestimater

Du kan bruge knappen **Tilføj et nyt udgiftsestimat** i gittervisningen til at registrere eventuelle udgifter, der opstår i projektet, men som ikke er direkte relateret til arbejdskraften. Du kan registrere udgiftsestimater for en bestemt opgave eller for hele projektet. Vælg udgiftskategorier og den foreløbige dato for, hvornår du forventer at betale udgiften. Hvis den tilknyttede kostpris- og salgsprisliste har standardpriser (eller hvis avanceprocentsatser er defineret for udgiftskategorier), bliver de automatisk angivet i estimatlinjen ved tilknytning.


[!INCLUDE[footer-include](../includes/footer-banner.md)]