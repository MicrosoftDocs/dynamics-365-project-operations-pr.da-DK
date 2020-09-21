---
title: Oprette tidsregistreringer
description: Dette emne indeholder oplysninger om, hvordan du opretter tidsregistreringer.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750587"
---
# <a name="create-time-entries"></a>Oprette tidsregistreringer

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I tidligere versioner af Dynamics 365 Project Service Automation blev tidsregistreringer bogført ugentligt. I version 3 af Project Service Automation bogføres tidsregistreringerne dagligt. Men efter at der er oprettet nogle få tidsregistreringer, kan du oprette eller kopiere dem samlet.

## <a name="create-a-time-entry"></a>Oprette en tidsregistrering

Følg disse trin for at oprette en tidsregistrering.

1. På siden **Tidsregistreringer** skal du vælge **Ny**.
2. I dialogboksen **Hurtig oprettelse: Tidsregistrering** skal du angive varigheden af tidsregistreringen i minutter, timer eller dage. Varigheden skal angives i følgende format: *x* minutter, *x* timer eller *x* dage. Timer og dage kan også angives som decimaler, f.eks. *x,x* timer eller *x,x* dage.
3. Vælg tidsregistreringstype og det projekt, du vil angive tidsregistreringen for.
4. I feltet **Projektopgave** skal du finde opgaven for denne tidsregistrering.

    > [!NOTE]
    > Hvis du opretter en tidsregistrering for en opgave, der ikke er tildelt til en bruger, skal du i feltet **Projektopgave** vælge knappen **Søg**, vælge **Skift visning** og derefter **Alle aktive projektopgaver** for at få vist alle opgaver.

5. Angiv evt. en beskrivelse, hvis det er nødvendigt, og vælg derefter **Gem og Luk**.

Når tidsregistreringen er oprettet og gemt, kan du redigere den i gitteret for tidsregistrering. Gitteret for tidsregistreringer understøtter to formater:

- Du kan angive tidsregistreringer i **tt:mm**-format. Dette format konverteres derefter til timer og brøkdele.
- Du kan angive timer og brøkdele direkte.

Bemærk, at brøkdele af en time ikke er minutter. Derfor er 1,5 timer lig med 1 time og 30 minutter. Den samme regel gælder for brøkdele af en dag. En dag er 24 timer, og 0,5 dage er lig med 12 timer.

## <a name="bulk-create-time-entries"></a>Oprette flere tidsregistreringer samtidigt

Når der er oprettet nogle få tidsregistreringer, kan du kopiere dem for at oprette flere tidsregistreringer samlet.

1. På siden **Tidsregistreringer** skal du vælge **Kopiér uge**.
2. I feltgruppen **Fra periode** skal du bruge felterne **Startdato** og **Slutdato** til at definere det datointerval, der skal kopieres tidsregistreringer fra.
3. I feltgruppen **Til periode** skal du i feltet **Startdato** angive den dato, der skal oprettes tidsregistreringer for.
4. Vælg **Kopiér** for at oprette en kopi af de tidsregistreringer, der svarer til den ugedag, der er angivet i feltgruppen **Til periode**. Tidsregistreringen for mandag i sidste uge kopieres f.eks. til mandag i den uge, der er angivet i feltgruppen **Til periode**.

## <a name="import-data-for-time-entries"></a>Importere data for tidsregistreringer

Du kan importere data fra projektreservationer og tildelinger. Når du importerer data, kan du angive datointervallet for de reservationer, der skal importeres, og derefter eksplicit vælge de reservationer, der skal oprettes som **Kladde**-tidsregistreringer.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Funktioner for gruppering efter, sortering, søgning og filtrering

Du kan gruppere og filtrere tidsregistreringer efter de dimensioner, der er angivet i kolonnerne. I feltet **Gruppér efter** skal du vælge den dimension, der skal bruges til at filtrere tidsregistreringer. Du kan også sortere tidsregistreringsposterne i stigende eller faldende rækkefølge ved hjælp af sorteringspilen på kolonneoverskrifterne. Du kan også få vist eller skjule poster ved at vælge knappen **Filtrer** på kolonneoverskrifterne og derefter i boksen **Søg** angive den tekst, der skal bruges til at søge efter tidsregistreringer ud fra projektnavn, projektopgave, tidsregistrering eller ressourcen.
