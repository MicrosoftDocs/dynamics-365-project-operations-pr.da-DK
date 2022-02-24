---
title: Administrer omsætningsestimater
description: Dette emne indeholder oplysninger om, hvordan du arbejder med omsætningsestimater for projekter.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531393"
---
# <a name="manage-revenue-estimates"></a>Administrer omsætningsestimater

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Du kan oprette, beregne, bogføre, tilbageføre eller eliminere omsætningsestimater. Du kan gøre dette enten manuelt eller ved hjælp af en periodisk proces. Dette emne indeholder oplysninger om, hvordan du arbejder med omsætningsestimater for projekter.

### <a name="manage-revenue-estimates-manually"></a>Administrer omsætningsestimater manuelt

På projektet med omsætningsestimat for fast pris eller siden **Estimer forespørgsel** (**Projektstyring og regnskab** > **Rapporter og forespørgsler** > **Estimatforespørgsler og rapporter**) skal du vælge **Estimater**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Administrer omsætningsestimater ved hjælp af en periodisk proces

Gå til **Projektstyring og regnskab** > **Periodisk** > **Estimater**, og vælg den tilsvarende proces.

## <a name="create-a-revenue-estimate"></a>Opret et omsætningsestimat

Fuldfør følgende fremgangsmåde for at oprette et omsætningsestimat. 

1. Gå til **Projektstyring og regnskab** > **Periodisk** > **Estimater**.
2. Vælg **Ny**. Vælg følgende parametre på siden **Estimatoprettelse**:

   - **Periodekode**: Denne kode bestemmer, hvor ofte estimater bogføres.
   - **Estimatdato**: Den dato, hvor estimatet behandles.
   - **Fortløbende**: Markér dette afkrydsningsfelt for kun at oprette estimater, hvis der er bogført estimater i den forrige periode, eller hvis estimatet er det første estimat, der er oprettet. Hvis dette ikke er valgt, oprettes der estimater, selvom der ikke er bogført estimater i den forrige periode.
   - **Metode til færdiggørelsesomkostninger**: Definer, hvordan det resterende projektarbejde skal estimeres. Yderligere oplysninger finder du i [Metoder til færdiggørelsesomkostninger](cost-complete-methods.md).
   - **Færdiggørelsesmetode**: Vælg en færdiggørelsesmetode ud fra følgende indstillinger:
     - **Automatisk**: Færdiggørelsesprocenten beregnes automatisk og på grundlag af de omkostningslinjer, der er inkluderet i beregningen. Omkostningsskabelonen definerer de omkostningslinjer, der er inkluderet.
     - **Manuel**  Færdiggørelsesprocenten er lig med færdiggørelsesprocenten for det sidste estimat. Når estimatet er oprettet, kan du ændre **Manuel beregning** på siden **Estimater**.
     - **Fra omkostningsskabelon**: En kombination af de automatiske og manuelle metoder. Denne indstilling angives automatisk eller manuelt, afhængigt af standardværdien i omkostningsskabelonen.
   - **Prognosemodel**: Vælg en prognosemodel for estimatet.
   - **Udskriv estimatliste**: Opret og vis en estimatliste. Listen indeholder statussen for den aktuelle funktion. Du kan udskrive eventuelle advarsler om estimatet i rapporten. Følgende betingelser medfører, at advarsler vises på estimatlisten:
     - En færdiggørelsesprocent på mere end 100 procent.
     - En færdiggørelsesprocent på mindre end 0 procent.
     - Et negativt beløb i kolonnen **Skal færdiggøres**.
     - Et estimat uden tilsvarende kontraktbeløb.
     - Et estimat uden vedhæftet omkostningsestimat.
   - **Vis infolog**: Vælg denne indstilling for at modtage en meddelelse, der indeholder oplysninger om de estimerede projekter, der blev behandlet, da jobbet blev kørt.


## <a name="post-wip-or-accruals"></a>Bogfør IGVA eller periodiseringer

Når estimaterne er evalueret, vedligeholdes, formindskes eller forhøjes de. Du kan derefter bogføre IGVA, når du arbejder med vurderingsprincippet **Færdiggjort kontrakt** eller bogføre periodiseringerne, når du arbejder med vurderingsprincippet **Procent for færdiggørelse**.
  
Status for estimatperioden ændres fra **Oprettet** til **Bogført**.

## <a name="reverse-wip-or-accruals"></a>Tilbagefør IGVA eller periodiseringer

Brug tilbageførelsesindstillingen til at kreditere allerede bogførte IGVA eller periodiseringer, og opret derefter estimater for perioden.

> [!NOTE]
> Hvis du vil tilbageføre en periode, der ligger inden for andre perioder, skal du tilbageføre de nødvendige estimatperioder og derefter bogføre dem igen. Da alle efterfølgende perioder er afhængige af estimaterne fra den foregående periode, skal du ikke springe nogle af perioderne over.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Eliminer det estimerede projekt, og afslut projektet

Det sidste trin i estimeringsprocessen er at fjerne det estimerede projekt og afslutte projektet med fast pris, når den procentvise færdiggørelse når 100 procent.

Der sker følgende, når du kører eliminering:

- For et fastprisprojekt med en færdiggjort kontrakt, ryddes IGVA-værdierne fra saldokontiene og bogføres til driftskonti.
- For et fastprisprojekt, der har en færdiggørelsesprocent, fjernes periodiseringerne fra driftskontiene.

I estimatetet ændres statussen til **Elimineret**.

> [!NOTE]
> I særlige tilfælde kan procentsatsen stige til mere end 100 procent. Når dette sker, skal du reducere færdiggørelsesprocenten ved hjælp af **Metoden til angivelse af omkostninger til færdiggørelse til nul** for at få nå 100 procent.

## <a name="reverse-elimination"></a>Tilbagefør eliminering

1. Gå til **Projektstyring og regnskab** > **Periodisk** > **Estimater** > **Tilbagefør eliminering**. 
2. I handlingsruden skal du på fanen **Behandling** i gruppen **Bevar** vælge **Estimat**. 
3. Vælg **Tilbagefør eliminering**.

Brug denne side til at tilbageføre alle elimineringer med en bestemt estimatdato og med estimatstatussen **Elimineret**. Transaktionsstatussen ændres, når du har valgt de relevante felter.

Derved ændres projektstatus også automatisk til **Igangværende**, hvis projektstadiet er angivet til afsluttet. Estimatstatus for projektperioden ændres tilbage til **Bogført**.
