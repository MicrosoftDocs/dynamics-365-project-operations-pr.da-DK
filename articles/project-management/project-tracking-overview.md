---
title: Sporing af indsats på et projekt
description: Denne artikel indeholder oplysninger om, hvordan du sporer projektindsats og arbejdets fremgang.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929253"
---
# <a name="project-effort-tracking"></a>Sporing af indsats på et projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Behovet for at spore status i forhold til tidsplanen varierer fra branche til branche. Nogle brancher sporer på et detaljeret niveau, hvor andre brancher sporer på et højere niveau. I denne artikel vises, hvordan du planlægger for at opfylde din organisations behov.

## <a name="effort-tracking-view"></a>Visning af indsatssporing

Visningen **Indsatssporing** sporer fremgangen for opgaver i tidsplanen ved at sammenligne de faktiske timer anvendt på en opgave med opgavens planlagte tidsforbrug. Dynamics 365 Project Operations bruger følgende formler til at beregne sporingsmålepunkter:

- **Procentvis fremgang**: Det faktiske tidsforbrug til dato - estimeret ved fuldførelse (EAC) 
- **Resterende indsats**: Estimeret indsats ved fuldførelse - faktisk forbrug til dato 
- **EAC**: Resterende tidsforbrug + faktisk tidsforbrug til dato 
- **Forventet afvigelse i tidsforbrug**: Det planlagte tidsforbrug - EAC

Project Operations viser en projektion af afvigelsen i tidsforbruget for opgaven. Hvis EAC er højere end det planlagte tidsforbrug, projekteres opgaven til at ville tage længere tid, end det oprindeligt var planlagt, og er bagud i forhold til planlægningen. Hvis EAC er mindre end det planlagte tidsforbrug, projekteres opgaven til at ville tage kortere tid, end det oprindeligt var planlagt, og er forud i forhold til planlægningen.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Omprojektering af indsats på bladnodeopgaver

Projektledere reviderer ofte de oprindelige estimater for en opgave. Ændringer af arbejdsindsatsen for et projekt er en projektleders opfattelse af estimater, et projekts aktuelle status taget i betragtning. Det anbefales dog ikke, at projektledere ændrer de planlagte indsatsnumre. Dette skyldes, at den planlagte projektindsats repræsenterer den etablerede kilde til sand for projektplanen og omkostningsestimatet, og alle projektinteressenter er blevet enige om det.

En projektleder kan omprojektere indsatsen på opgaver ved at opdatere standardværdien for den **Resterende indsats** med et nyt estimat på opgaven. Denne opdatering medfører, at opgavens estimat ved fuldførelse (EAC), færdiggørelsesprocenten og den forventede omkostningsafvigelse for en opgave genberegnes. EAC, ETC og fremgangen i procenten for hovedopgaver genberegnes også og giver en ny projektion af afvigelsen i tidsforbruget.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Ændring af arbejdsindsatsen på hovedopgaver

Arbejdsindsatsen for hovedopgaver og beholderopgaver kan ændres. Projektledere kan opdatere den resterende indsats på hovedopgaverne. Opdatering af den resterende indsats udløser følgende sæt beregninger i programmet:

- EAC og statussen i procent for opgaven beregnes.
- Den nye EAC fordeles nedad til de underordnede opgaver i samme forhold, som den oprindelige EAC på opgaven blev fordelt.
- Den nye EAC for hver af de enkelte opgaver nedad til bladnodeopgaver beregnes. 
- De påvirkede underordnede opgaver ned til bladnoderne får genberegnet deres resterende indsats og status i procent på grundlag af EAC-værdien. Dette medfører, at der laves en ny projektion for afvigelsen i tidsforbruget for opgaven. 
- EAC-værdierne for hovedopgaverne genberegnes helt ned til rodnoden.
- Den godkendte indsats på en opsummeringsopgave er summen af den godkendte indsats på alle underordnede opgaver samt den godkendte indsats på opsummeringsopgaven.
- Den resterende indsats på en opsummeringsopgave er summen af den resterende indsats på alle underordnede opgaver minus den godkendte indsats på opsummeringsopgaven.

## <a name="project-status-summary"></a>Projektstatusoversigt

Når du sporer data i visningerne **Indsatssporing** og **Omkostningssporing** vises status og omkostningsforbrug på projektrodsnode-, hovedopgave- og bladnodeopgaveniveau. Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over status på projektniveau.

## <a name="status-summary-fields"></a>Felter for statusoversigt

Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status. Den bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko. Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen. Feltet **Status opdateret den** kan ikke redigeres, og værdien er et tidsstempel, der angiver, hvornår statussen senest blev opdateret.

Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsdatoen. Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, kan du angive disse felter til **Forud** Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, kan du angive dem til **Bagud**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
