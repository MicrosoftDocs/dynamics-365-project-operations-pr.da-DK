---
title: Ekstern planlægning
description: Denne artikel indeholder oplysninger om ekstern planlægning.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736958"
---
# <a name="external-scheduling"></a>Ekstern planlægning

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I den eksterne planlægningstilstand kan du oprette, opdatere og slette indbyggede objekter, der er relateret til WBS'er (arbejdsopgavehierarkier), men uden de aktuelle grænser, der håndhæves af Microsoft Project for the Web. Det giver også begrænset validering. Denne tilstand skal kun bruges af følgende kunder:

- Kunder, der har de værktøjer, der kræves for at definere en WBS uden for den planlægningslogik, der leveres af Project Operations
- Kunder, der skal administrere planlægningshierarki, afhængigheder eller opgavevarighed

> [!IMPORTANT]
> Data, der ikke er angivet korrekt i WBS-relaterede objekter, gengives måske ikke i gitteret til ressourceafstemning, overslagsgitteret, sporingsgitteret eller ressourcetildelingsgitteret.

## <a name="configuration"></a>Configuration

Denne funktion er som standard aktiveret. Men på den hovedside, der er standard for projekter, er det relaterede felt ikke synligt som standard. Hvis du vil aktivere feltet, skal du åbne hovedsiden for projektobjektet på Maker Portal, vælge feltet **Planlægningsprogram** og derefter ændre feltet til **Synlig som standard**. Hvis du ikke bruger standardhovedsiden for projektet, skal du redigere den eksisterende side og føje feltet **Planlægningsprogram** til det.

## <a name="settings"></a>Indstillinger

Hvis du vil bruge den eksterne planlægningstilstand, skal du først oprette et nyt projekt og vælge planlægningsprogrammet **Planlagt eksternt** på rullelisten på hovedsiden for projektet. Når denne tilstand er konfigureret for et projekt, kan den ikke ændres.

## <a name="viewing-the-wbs"></a>Få vist WBS

Hvis et projekt planlægges eksternt, er der begrænset adgang til Project for the Web for det pågældende projekt. Hvis du vil have vist WBS, skal du gå til det sporingsgitter, hvor den fulde WBS vises.

## <a name="creating-and-editing-the-wbs"></a>Oprette og redigere WBS'en

Hvis ekstern planlægning er aktiveret for et projekt, skal du definere dataene for alle WBS-relaterede objekter, herunder opgaver, teammedlemmer, ressourcetildelinger og afhængigheder.

I følgende illustration vises datamodellen for projektplanlægning.

![Datamodel for projektplanlægning.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funktionsbegrænsninger

Følgende handlinger er ikke tilladt i eksternt planlagte projekter.

### <a name="project-planning"></a>Projektplanlægning

- **Kopiér projekt** – Denne handling understøttes ikke i eksternt planlagte projekter.
- **Flyt projekt** – Ændringer af startdatoen for et projekt flytter ikke starten af opgaver eller ressourcetildelinger i WBS.
- **Opdatering af projektlederen** – Ændringer af projektlederen på projektets hovedside vil ikke automatisk oprette et nyt medlem af projektteamet, før projektet er konverteret.
- **Opdatering af projektets skabelon for arbejdstid** – Ændringer af projektets arbejdstidsskabelon genberegnes ikke i projektets tidsplan.
- **Profiler for ressourcetildeling** – Oprettelse af ressourcetildelinger opdaterer ikke automatisk feltet **mdyn\_PlannedWork**. Dette felt bruges til at gemme profiler for ressourcetildelingsindsatsen. Hvis der vises tidsfaseinddelte indsatser i ressourcetildelingsgitteret eller gitteret til ressourceafstemning, skal du definere gyldige ressourcetildelingsprofiler. Disse profiler skal formateres korrekt, så de udløser beregningen af både omkostningsprofiler og salgsprisprofiler. Det anbefales, at du opretter et testprojekt, der er planlagt af Project for the Web, og derefter gennemser de tilknyttede data for at bekræfte kravene og formateringen.

### <a name="resource-management"></a>Ressourcestyring

- **Generisk ressourceopfyldelse** – Generisk ressourceopfyldelse understøttes ikke i eksternt planlagte projekter. Hvis du forsøger at opfylde aktive åbne krav, oprettes der nye medlemmer af projektteamet, men det generiske teammedlem slettes ikke, og det generiske teammedlem erstattes ikke i eksisterende ressourcetildelinger.
- **Slet teammedlem** – Hvis du sletter et teammedlem, slettes der ikke automatisk ressourcetildelinger.

### <a name="quoting-and-contracting"></a>Tilbud og kontrakter

- **Importer detaljer om tilbudslinjer og kontraktlinjer** – Når detaljer om tilbuds- eller kontraktlinje importeres fra et projekt, er programmet blevet testet til kun at understøtte højst 500 opgaver i WBA baseret på en grænse på 20 tildelinger pr. opgave.

### <a name="actuals-and-invoicing"></a>Faktiske omkostninger og fakturering

- Selvom der ikke er ændringer af eksisterende valideringer mellem WBS og økonomiske transaktioner, er det vigtigt, at du overholder standarddatamodellen for at sikre, at alle downstreamtransaktioner kører som forventet.
