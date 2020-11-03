---
title: Oversigt over projektsporing
description: Dette emne indeholder oplysninger om, hvordan du sporer projektstatus og omkostningsforbrug.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074023"
---
# <a name="project-tracking-overview"></a>Oversigt over projektsporing

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Behovet for at spore status i forhold til tidsplanen varierer fra branche til branche. Nogle brancher sporer på et detaljeret niveau, hvor andre brancher sporer på et højere niveau. I dette emne vises, hvordan du planlægger for at opfylde din organisations behov.

## <a name="effort-tracking-view"></a>Visning af indsatssporing

Visningen **Indsatssporing** sporer fremgangen for opgaver i tidsplanen ved at sammenligne de faktiske timer anvendt på en opgave med opgavens planlagte tidsforbrug. Dynamics 365 Project Operations bruger følgende formler til at beregne sporingsmålepunkter:

- **Procentvis fremgang** : Det faktiske tidsforbrug til dato - estimeret ved fuldførelse (EAC) 
- **Anslået tid inden fuldførelse (ETC)** : Det planlagte tidsforbrug - faktisk tidsforbrug indtil dato 
- **EAC** : Resterende tidsforbrug + faktisk tidsforbrug til dato 
- **Forventet afvigelse i tidsforbrug** : Det planlagte tidsforbrug - EAC

Project Operations viser en projektion af afvigelsen i tidsforbruget for opgaven. Hvis EAC er højere end det planlagte tidsforbrug, projekteres opgaven til at ville tage længere tid, end det oprindeligt var planlagt, og er bagud i forhold til planlægningen. Hvis EAC er mindre end det planlagte tidsforbrug, projekteres opgaven til at ville tage kortere tid, end det oprindeligt var planlagt, og er forud i forhold til planlægningen.

## <a name="reprojecting-effort"></a>Ændre arbejdsindsats

Projektledere reviderer ofte de oprindelige estimater for en opgave. Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning. Vi anbefaler dog ikke, at projektledere ændrer de oprindelige tal. Dette skyldes, at den oprindelige projektplan repræsenterer den etablerede sande kilde for projektets tidsplan og omkostningsestimat, og alle projektets interessenter er blevet enige herom.

En projektleder kan ændre arbejdsindsatsen på opgaver på to måder:

- Tilsidesætte standard-ETC med et nyt estimat for den faktiske resterende indsats på opgaven. 
- Tilsidesætte standardstatussen i procent med et nyt estimat for den faktiske indsats på opgaven.

Hver fremgangsmåde medfører en genberegning af ETC, EAC, fremgangen i procent samt den forventede afvigelse i tidsforbrug på en opgave. EAC, ETC og fremgangen i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ændring af arbejdsindsatsen på hovedopgaver

Arbejdsindsatsen for hovedopgaver og beholderopgaver kan ændres. Uanset om brugeren ændrer arbejdsindsatsen ved hjælp af den resterende indsats eller statussen i procent på hovedopgaverne, tages følgende beregningssæt i anvendelse:

- EAC, ETC og statussen i procent for opgaven beregnes.
- Den nye EAC fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige EAC på opgaven blev fordelt.
- Den nye EAC for hver af de enkelte opgaver nedad til bladnodeopgaver beregnes. 
- De påvirkede underordnede opgaver ned til bladnoderne får genberegnet deres ETC og status i procent på grundlag af EAC-værdien. Dette medfører, at der laves en ny projektion for afvigelsen i tidsforbruget for opgaven. 
- EAC-værdierne for hovedopgaverne genberegnes helt ned til rodnoden.

### <a name="cost-tracking-view"></a>Visning af omkostningssporing 

Visningen **Omkostningssporing** sammenligner de faktiske omkostninger, der er brugt på en opgave, med de planlagte omkostninger for en opgave. 

> [!NOTE]
> Denne visning viser kun omkostninger til arbejdsløn og inkluderer ikke omkostninger fra udgiftsestimaterne. Project Operations bruger følgende formler til at beregne sporingsmålepunkter:

- **Procent af forbrugte omkostninger** : De faktiske omkostninger brugt til dato ÷ estimerede omkostninger ved fuldførelse
- **Omkostninger indtil fuldførelse (CTC)** : De planlagte omkostninger - faktiske omkostninger brugt indtil dato
- **EAC** : De resterende omkostninger + de faktiske forbrugte omkostninger til date
- **Forventet omkostningsafvigelse** : Planlagte omkostninger - EAC

Der vises en projektion af afvigelsen i omkostningerne for opgaven. Hvis EAC er højere end de planlagte omkostninger, projekteres opgaven til at have flere omkostninger, end det oprindeligt blev planlagt. Der er derfor en tendens til at ligge over budgettet. Hvis EAC er lavere end de planlagte omkostninger, projekteres opgaven til at have færre omkostninger, end det oprindeligt blev planlagt. Der er derfor en tendens til at ligge under budgettet.

## <a name="project-managers-reprojection-of-cost"></a>Projektlederens ændring af omkostningerne

Når indsatsen ændres, genberegnes CTC, EAC, det procentuelle omkostningsforbrug og den forventede omkostningsafvigelse alle sammen i visningen **Omkostningssporing**.

## <a name="project-status-summary"></a>Projektstatusoversigt

Når du sporer data i visningerne **Indsatssporing** og **Omkostningssporing** vises status og omkostningsforbrug på projektrodsnode-, hovedopgave- og bladnodeopgaveniveau. Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over status på projektniveau.

## <a name="status-summary-fields"></a>Felter for statusoversigt

Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status. Den bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko. Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen. Feltet **Status opdateret den** kan ikke redigeres, og værdien er et tidsstempel, der angiver, hvornår statussen senest blev opdateret.

Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsdatoen. Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, kan du angive disse felter til **Forud** Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, kan du angive dem til **Bagud**.
