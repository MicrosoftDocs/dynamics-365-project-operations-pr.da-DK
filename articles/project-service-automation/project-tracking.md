---
title: Projektstatus og -omkostningsforbrug
description: Dette emne indeholder oplysninger om, hvordan du sporer projektstatus og omkostningsforbrug.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750603"
---
# <a name="project-progress-and-cost-consumption"></a>Projektstatus og -omkostningsforbrug

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Behovet for at spore status i forhold til tidsplanen varierer fra branche til branche. Nogle brancher sporer på et detaljeret niveau, mens andre brancher sporer på et højere niveau. I dette emne vises, hvordan du planlægger for at opfylde din organisations behov.

## <a name="effort-tracking-view"></a>Visning af indsatssporing

Visningen af **Indsatssporing** sporer statussen for opgaver i tidsplanen. Den sammenligner de faktiske indsatstimer, der er brugt på en opgave, med de planlagte indsatstimer for den pågældende opgave. PSA bruger følgende formler til at beregne sporingsmålepunkter:

- Status i procentsats = faktisk forbrug brugt indtil dato ÷ planlagt indsats for opgaven 
- Anslået tid inden fuldførelse (ETC) = planlagt indsats ÷ faktisk forbrug brugt indtil dato 
- Estimat ved fuldførelse (EAC) = resterende indsats + faktisk forbrug brugt indtil dato 
- Forventet afvigelse i tidsforbrug = planlagt indsats ÷ EAC

PSA viser en projektion af afvigelsen i tidsforbruget for opgaven. Hvis EAC er højere end den planlagte indsats, projekteres opgaven til at tage længere tid, end det oprindeligt blev planlagt. Projektet er derfor bagud i forhold til tidsplanen. Hvis EAC er lavere end den planlagte indsats, projekteres opgaven til at tage kortere tid, end det oprindeligt blev planlagt. Projektet er derfor forud i forhold til tidsplanen.

## <a name="re-projecting-effort"></a>Ændre arbejdsindsats

Det er almindeligt, at en projektleder reviderer de oprindelige estimater for en opgave. Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning. Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal, fordi den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.

En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:

- Tilsidesætte standard-ETC med et nyt estimat for den faktiske resterende indsats på opgaven. 
- Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.

Hver af disse fremgangsmåder medfører en genberegning af ETC, EAC og statussen i procent samt den forventede afvigelse i tidsforbrug på en opgave. EAC, ETC og status i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Ændring af arbejdsindsatsen på hovedopgaver

Arbejdsindsatsen for hovedopgaver og beholderopgaver kan ændres. Uanset om brugeren ændrer arbejdsindsatsen ved hjælp af den resterende indsats eller statussen i procent på hovedopgaverne, tages følgende beregningssæt i anvendelse:

- EAC, ETC og statussen i procent for opgaven beregnes.
- Den nye EAC fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige EAC på opgaven blev fordelt.
- Den nye EAC for hver af de enkeltstående opgaver nedad til bladnodeopgaver beregnes. 
- De påvirkede underordnede opgaver ned til bladnoderne får genberegnet deres ETC og status i procent på grundlag af EAC-værdien. Dette medfører, at der laves en ny projektion for afvigelsen i tidsforbruget for opgaven. 
- EAC-værdierne for hovedopgaverne genberegnes helt ned til rodnoden.

### <a name="cost-tracking-view"></a>Visning af omkostningssporing 

Visningen **Omkostningssporing** sammenligner de faktiske omkostninger, der er brugt på en opgave, med de planlagte omkostninger for en opgave. 

> [!NOTE]
> Denne visning viser kun omkostninger til arbejdsløn og inkluderer ikke omkostninger fra udgiftsestimaterne. 

PSA bruger følgende formler til at beregne sporingsmålepunkter:

- Procent af forbrug af omkostninger = faktiske omkostninger brugt indtil dato ÷ planlagte omkostninger for opgaven
- Omkostninger indtil fuldførelse (CTC) = planlagte omkostninger ÷ faktiske omkostninger brugt indtil dato
- EAC = CTC + faktiske omkostninger brugt indtil dato
- Forventet omkostningsafvigelse = Planlagte omkostninger ÷ EAC

Der vises en projektion af afvigelsen i omkostningerne for opgaven. Hvis EAC er højere end de planlagte omkostninger, projekteres opgaven til at have flere omkostninger, end det oprindeligt blev planlagt. Der er derfor en tendens til at ligge over budgettet. Hvis EAC er lavere end de planlagte omkostninger, projekteres opgaven til at have færre omkostninger, end det oprindeligt blev planlagt. Der er derfor en tendens til at ligge under budgettet.

## <a name="project-managers-re-projection-of-cost"></a>Projektlederens ændring af omkostningerne

Når indsatsen ændres, genberegnes CTC, EAC, det procentuelle omkostningsforbrug og den forventede omkostningsafvigelse alle sammen i visningen **Omkostningssporing**.

## <a name="project-status-summary"></a>Projektstatusoversigt

Når du sporer data i visningerne **Indsatssporing** og **Omkostningssporing** vises status og omkostningsforbrug på projektrodsnode-, hovedopgave- og bladnodeopgaveniveau. Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over status på projektniveau.

## <a name="status-summary-fields"></a>Felter for statusoversigt

Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status. Den bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko. Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen. Feltet **Status opdateret den** kan ikke redigeres, og værdien er et tidsstempel, der angiver, hvornår statussen senest blev opdateret.

Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsdatoen. Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, kan du angive disse felter til **Forud** Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, kan du angive dem til **Bagud**.
