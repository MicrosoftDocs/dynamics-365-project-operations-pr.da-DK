---
title: Overvejelser i forbindelse med opgradering – Microsoft Dynamics 365 Project Service Automation version 2.x eller 1.x til version 3
description: Dette emne indeholder oplysninger om de overvejelser, du skal gøre dig, når du opgraderer fra Project Service Automation version 2.x eller 1.x til version 3.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 19d6d312c7cedd2d7b9b5649452b85dd24fae761
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074252"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Overvejelser i forbindelse med opgradering – PSA version 2.x eller 1.x til version 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation og Field Service
Både Dynamics 365 Project Service Automation og Dynamics 365 Field Service bruger løsningen Universal Resourcing Scheduling (URS) til ressourceplanlægning. Hvis du både har tjenesten Project Service Automation og Field Service i din forekomst, skal du regne med, at begge løsninger skal opgraderes til den nyeste version (version 3.x for Project Service Automation og version 8.x for Field Service). Hvis du opgraderer Project Service Automation eller Field Service, installeres den nyeste version af URS, hvilket betyder, at inkonsekvent funktionsmåde er mulig, hvis både Project Service Automation- og Field Service-løsningerne i den samme forekomst ikke opgraderes til den nyeste version.

## <a name="resource-assignments"></a>Ressourcetildelinger
I Project Service Automation version 2 og version 1 blev opgavetildelinger gemt som underordnede opgaver (også kaldet linjeopgaver) i **Opgaveobjektet** og indirekte relateret til objektet **Ressourcetildeling**. Linjeopgaven var synlig i pop op-vinduet for tildelinger i arbejdsopgavehierakiet (WBS).

![Linjeopgaver i WBS i Project Service Automation version 2 og version 1](media/upgrade-line-task-01.png)

I version 3 af Project Service Automation er det underliggende skema for tildeling af reserverbare ressourcer til opgaver ændret. Linjeopgaven er forældet, og der er et direkte 1:1 forhold mellem opgaven i **Opgaveobjektet** og teammedlemmet i objektet **Ressourcetildeling.** Opgaver, der tildeles til et teammedlem, lagres nu direkte i objektet Ressourcetildeling.  

Disse ændringer påvirker opgraderingen af eksisterende projekter, der har ressourcetildelinger for navngivne reserverbare ressourcer og generiske ressourcer i et projektteam. Dette emne indeholder de overvejelser, du skal gøre dig for at tage højde for dine projekter, når du opgraderer til version 3. 

### <a name="tasks-assigned-to-named-resources"></a>Opgaver tildelt til navngivne ressourcer
Ved hjælp af det underliggende opgaveobjekt kunne teammedlemmer i version 2 og version 1 portrættere en anden rolle, end den rolle der er defineret som standard. F.eks. kunne Charlotte Jeppesen, der som standard er tildelt rollen som programadministrator, blive tildelt til en opgave med rollen som udvikler. I version 3 er rollen for et navngivet teammedlem altid standardrollen, så alle opgaver, som Charlotte Jeppesen tildeles, bruger hendes standardrolle som programadministrator.

Hvis du har tildelt en ressource til en opgave uden for standardrollen i version 2 og version 1, tildeles den navngivne ressource standardrollen for alle opgavetildelinger uanset rolletildeling i version 2, når du opgraderer. Det betyder, at der er forskelle mellem de beregnede estimater fra version 2 eller version 1 i forhold til version 3, da estimater beregnes på baggrund af ressourcens rolle og ikke linjeopgavetildelingen. I version 2 er der f.eks. tildelt to opgaver til Anne-Marie Jespersen. Rollen på linjeopgaven for opgave 1 er udvikler og for opgave 2, programadministrator. Anne-Marie Jespersen har standardrolle som programadministrator.

![Flere roller tildelt til en ressource](media/upgrade-multiple-roles-02.png)

Da rollerne som udvikler og programadministrator er forskellige, er omkostnings- og salgsestimaterne som følger:

![Omkostningsestimater for ressourceroller](media/upggrade-cost-estimates-03.png)

![Salgsestimater for ressourceroller](media/upgrade-sales-estimates-04.png)

Når du opgraderer til version 3, erstattes linjeopgaver af ressourcetildelinger i forbindelse med opgaven for det reserverbare ressourceteammedlem. Tildelingen bruger standardrollen for den reserverbare ressource. I den følgende illustration er Anne-Marie Jespersen, der har en rolle som programadministrator, ressourcen.

![Ressourcetildelinger](media/resource-assignment-v2-05.png)

Da estimaterne er baseret på standardrollen for ressourcen, kan estimaterne for salg og omkostninger blive ændret. Bemærk, at du i den følgende illustration ikke længere kan se **Udvikler**-rollen, da rollen nu er taget fra den reserverbare ressources standardrolle.

![Omkostningsestimater for standardroller](media/resource-assignment-cost-estimate-06.png)
![Salgsestimat for standardroller](media/resource-assignment-sales-estimate-07.png)

Når opgraderingen er fuldført, kan du redigere et teammedlems rolle til andet end den tildelte standardrolle. Hvis du ændrer et teammedlems rolle, ændres den imidlertid på alle de tildelte opgaver, da teammedlemmer ikke længere kan tildeles flere roller i version 3.

![Opdatering af en ressourcerolle](media/resource-role-assignment-08.png)

Dette gælder også for linjeopgaver, der er tildelt til navngivne ressourcer, når du ændrer ressourcens afdeling fra standardafdelingen til en anden afdeling. Når opgraderingen til version 3 er fuldført, bruger tildelingen ressourcens standardafdeling i stedet for den afdeling, der er angivet for den pågældende linjeopgave.

### <a name="tasks-assigned-to-generic-resources"></a>Opgaver tildelt til generiske ressourcer
I version 2 og version 1 kan du angive rollen og afdelingen for en opgave og derefter bruge funktionen **Generér team** til at generere generiske ressourcer på baggrund af de attributter, der er angivet for opgaven. I version 3 kan du oprette de generiske teammedlemmer med rolle og afdeling og derefter tildele teammedlemmerne til opgaver.

I version 2 og version 1 kan projekter med generiske ressourcer være i to tilstande eller en blanding af begge på opgaveniveau. Du kan f.eks. have følgende scenarier:

- Opgaver med roller og afdelinger angivet, men der er ikke genereret en tilknyttet ressourcetildeling.
- Opgaver med ressourcetildelinger til generiske teammedlemmer, der er tildelt ved at oprette en generisk ressource ved hjælp af funktionen **Generér team**.

Før du går i gang med at udføre en opgradering, anbefales det, at du genererer teamet igen for hvert enkelt projekt, der har opgaver tildelt til generiske ressourcer, eller hvor der endnu ikke er kørt processen Generér team for dem.

I forbindelse med opgaver, der er tildelt til generiske teammedlemmer, som blev genereret vha. **Generér team**, bevarer opgraderingen den generiske ressource i teamet og beholder tildelingen til det generiske teammedlem. Det anbefales, at du genererer ressourcekravet for det generiske teammedlem efter opgraderingen, men før du reserverer eller sender en ressourceanmodning. Derved forbliver eventuelle tildelinger til afdelinger på de generiske teammedlemmer, der er forskellige fra projektets kontraktafdeling.

I Projekt Z-projektet er kontraktafdelingen f.eks. Contoso US. I projektplanen er testopgaver i implementeringsfasen blevet tildelt rollen teknisk konsulent, og den tildelte afdeling er Contoso India.

![Implementeringsfase for tildeling til organisation](media/org-unit-assignment-09.png)

Efter implementeringsfasen tildeles integrationstestopgaven til rollen teknisk konsulent, men organisationen er angivet til Contoso US.  

![Tildeling af integrationstestopgave til organisation](media/org-unit-generate-team-10.png)

Når du genererer et team for projektet, oprettes der to generiske teammedlemmer på grund af de forskellige afdelinger, der er på opgaverne. Teknisk konsulent 1 tildeles Contoso India-opgaverne og teknisk konsulent 2 tildeles Contoso US-opgaverne.  

![Genererede generiske teammedlemmer](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> I Project Service Automation version 2 og version 1 beholder teammedlemmet ikke den afdeling, som angives i linjeopgaven.

![Linjeopgaver i Project Service Automation version 2 og version 1](media/line-tasks-12.png)

Du kan se afdelingen i estimatvisningen. 

![Afdelingsestimater](media/org-unit-estimates-view-13.png)
 
Når opgraderingen er fuldført, føjes afdelingen på linjeopgaven, der svarer til det generiske teammedlem, til det generiske teammedlem, og linjeopgaven fjernes. Det anbefales derfor, at du genererer eller regenererer teamet, før du opgraderer, for hvert projekt, der indeholder generiske ressourcer.

For opgaver, der er tildelt til en rolle med en afdeling, der er anderledes end afdelingen i kontraktprojektet, og der ikke er genereret et team, opretter opgraderingen et generisk teammedlem for rollen, men bruger projektets kontraktenhed til teammedlemmets afdeling. Idet vi igen refererer til eksemplet med Projekt Z, betyder det, at kontraktenheden Contoso US og projektplanens testopgaver i implementeringsfasen er blevet tildelt rollen teknisk konsulent med den afdeling, der er tildelt til Contoso India. Integrationstestopgaven, der udføres efter implementeringsfasen, er blevet tildelt til rollen teknisk konsulent. Afdelingen er Contoso US, og der er ikke genereret et team. Opgraderingen opretter et generisk teammedlem, en teknisk konsulent, der har de tildelte timer for alle tre opgaver, og en afdeling af Contoso US, projektets kontraktafdeling.   
 
Ændringer af standardværdien for de forskellige ressourceafdelinger vedrørende ikke-genererede teammedlemmer er årsagen til, at vi anbefaler, at du genererer eller regenererer teamet på hvert enkelt projekt, der indeholder generiske ressourcer før opgraderingen, så afdelingstildelingerne ikke går tabt.

