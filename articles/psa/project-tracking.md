---
title: Projektstatus og -omkostningsforbrug
description: Dette emne indeholder oplysninger om sporing af projektstatus og omkostningsforbrug.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 8bde19fbf1dd9f0c760455ecb7f7f2bd14a358d441bf024ec0cdefa42866f53e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987159"
---
# <a name="project-progress-and-cost-consumption"></a>Projektstatus og -omkostningsforbrug

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Behovet for at spore status i forhold til tidsplanen varierer fra branche til branche. Nogle brancher sporer på et detaljeret niveau, mens andre brancher sporer på et højere niveau. I dette emne vises, hvordan du planlægger for at opfylde din organisations behov.

## <a name="effort-tracking-view"></a>Visning af indsatssporing

Visningen af **Indsatssporing** sporer statussen for opgaver i tidsplanen. Den sammenligner de faktiske timer, der er brugt på en opgave, med opgavens planlagte forbrug af timer. Project Service Automation bruger følgende formler til at beregne sporingsmålepunkter:

Til at begynde med i opgaveoprettelsen: planlagte omkostninger angives til den estimerede omkostning ved fuldførelse. Når der registreres faktiske oplysninger på opgaven, foretages der en beregning af følgende i Visningen af tidsforbrugssporing

- Procentvis fremgang = faktisk tidsforbrug til dato - estimeret ved fuldførelse (EAC) 
- Estimeret tid til fuldførelse (ETC) = estimeret ved fuldfuldførelse (EAC) – faktisk tidsforbrug til dato 
- EAC = resterende tidsforbrug + faktisk tidsforbrug til dato 
- Forventet afvigelse i tidsforbrug = planlagt indsats ÷ EAC

Project Service Automation viser en projektion af afvigelsen i tidsforbruget for opgaven. Hvis EAC er højere end den planlagte indsats, projekteres opgaven til at tage længere tid, end det oprindeligt blev planlagt. Projektet er derfor bagud i forhold til tidsplanen. Hvis EAC er lavere end den planlagte indsats, projekteres opgaven til at tage kortere tid, end det oprindeligt blev planlagt. Projektet er derfor forud i forhold til tidsplanen.

## <a name="reprojecting-effort"></a>Ændre arbejdsindsats

Det er almindeligt, at en projektleder reviderer de oprindelige estimater for en opgave. Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning. Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal, fordi den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.

En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:

- Tilsidesætte standard-ETC med et nyt estimat for den faktiske resterende indsats på opgaven. 
- Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.

Hver af disse fremgangsmåder medfører en genberegning af ETC, EAC og statussen i procent samt den forventede afvigelse i tidsforbrug på en opgave. EAC, ETC og status i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ændring af arbejdsindsatsen på hovedopgaver

Arbejdsindsatsen for hovedopgaver og beholderopgaver kan ændres. Uanset om brugeren ændrer arbejdsindsatsen ved hjælp af den resterende indsats eller statussen i procent på hovedopgaverne, tages følgende beregningssæt i anvendelse:

- EAC, ETC og statussen i procent for opgaven beregnes.
- Den nye EAC fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige EAC på opgaven blev fordelt.
- Den nye EAC for hver af de enkelte opgaver nedad til bladnodeopgaver beregnes. 
- De påvirkede underordnede opgaver ned til bladnoderne får genberegnet deres ETC og status i procent på grundlag af EAC-værdien. Dette medfører, at der laves en ny projektion for afvigelsen i tidsforbruget for opgaven. 
- EAC-værdierne for hovedopgaverne genberegnes helt ned til rodnoden.

### <a name="cost-tracking-view"></a>Visning af omkostningssporing 

Visningen **Omkostningssporing** sammenligner de faktiske omkostninger, der er brugt på en opgave, med de planlagte omkostninger. 

> [!NOTE]
> Denne visning viser kun omkostninger til arbejdsløn og inkluderer ikke omkostninger fra udgiftsestimaterne. 

Project Service Automation bruger følgende formler til at beregne sporingsmålepunkter:

Når en opgave oprettes, er de planlagte omkostninger lig med de anslåede omkostninger ved fuldførelse. Når faktiske oplysninger registreres på opgaven, beregnes følgende i visningen af **Sporing** af omkostninger:

 - Procent af forbrugte omkostninger = faktiske omkostninger brugt til dato ÷ estimerede omkostninger ved fuldførelse af opgaven
 - Omkostninger for at fuldføre (CTC) = estimerede omkostninger ved fuldførelse - faktiske omkostninger brugt til dato
 - Estimerede omkostninger ved fuldførelse = CTC + faktiske omkostninger brugt til dato
 - Anslået omkostningsafvigelse = planlagte omkostninger – estimerede omkostninger ved fuldførelse

Der vises en projektion af afvigelsen i omkostningerne for opgaven. Hvis de estimerede omkostninger ved fuldførelse er højere end de planlagte omkostninger, projekteres opgaven til at blive dyrere, end det oprindeligt var planlagt. Der er derfor en tendens til at ligge over budgettet. Hvis de estimerede omkostninger ved fuldførelse er lavere end de planlagte omkostninger, projekteres opgaven til at blive billigere, end det oprindeligt var planlagt, og har derfor en tendens til at ligge under budgettet.

## <a name="project-managers-reprojection-of-cost"></a>Projektlederens ændring af omkostningerne

Når tidsforbruget ændres, genberegnes CTC, de estimerede omkostninger ved fuldførelse, det procentuelle omkostningsforbrug og den forventede omkostningsafvigelse alle sammen i visningen **Omkostningssporing**.

## <a name="project-status-summary"></a>Projektstatusoversigt

Når du sporer data i visningerne **Indsatssporing** og **Omkostningssporing** vises status og omkostningsforbrug på projektrodsnode-, hovedopgave- og bladnodeopgaveniveau. Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over status på projektniveau.

## <a name="status-summary-fields"></a>Felter for statusoversigt

Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status. Den bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko. Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen. Feltet **Status opdateret den** kan ikke redigeres, og værdien er et tidsstempel, der angiver, hvornår statussen senest blev opdateret.

Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsdatoen. Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, kan du angive disse felter til **Forud** Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, kan du angive dem til **Bagud**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]