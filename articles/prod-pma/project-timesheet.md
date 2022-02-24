---
title: Mobilappen Project Timesheet
description: Dette emne indeholder oplysninger om Microsoft Dynamics 365 Project Timesheet-mobilprogrammet. Mobilappen til Project Timesheet gør brugerne i stand til at sende og godkende timesedler for projekter på deres mobilenheder.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b9cbd84ecb0d71a99982e158d7e0ea1e236fb369
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074345"
---
# <a name="project-timesheet-mobile-application"></a>Mobilappen Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Oversigt

Mobilappen Microsoft Dynamics 365 Project Timesheet gør brugerne i stand til at sende og godkende timesedler for projekter på deres mobilenheder (iPhone eller Android). Denne mobilapp indeholder de timeseddelfunktioner, der findes i området for projektstyring og regnskab i Dynamics 365 Finance, hvorved brugernes produktivitet og effektivitet forbedres samt gør det muligt at tidsregistrere og godkende projekttimesedler.

## <a name="download-and-install-the-mobile-app"></a>Hent og installer mobilappen

Hent og Installer Microsoft Dynamics 365 Project Timesheet-mobilappen til Android eller iPhone fra din enheds mobilbutik.

## <a name="enable-the-app"></a>Aktivér appen 

Appen Project Timesheet skal være aktiveret i Finance. Hvis du vil aktivere funktionaliteten, skal du gå til **Projektstyring og regnskabsparametre \> Timesedler** og vælge parameteren **Aktiver Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Log på appen

1.  Start mobilappen på din mobilenhed.

2.  Angiv din URL-adresse til Finance.

3.  Første gang, du logger på, bliver du bedt om at angive dit brugernavn og din adgangskode. Angiv dine legitimationsoplysninger.

4.  Du bliver logget på din standardvirksomhed.

## <a name="submit-a-project-timesheet"></a>Indsend en timeseddel for projekt

Du kan oprette og indsende en timeseddel for projektet i appen. Du kan basere en ny timeseddel på oplysninger fra en tidligere timeseddel, gemte linjer eller projekttildelinger. Hvis du er udpeget som stedfortræder, kan du også angive en timeseddel for en anden arbejder. Hvis du vil oprette en timeseddel som stedfortræder, skal du vælge knappen **Menu** og derefter vælge et ressourcenavn.

På timeseddelsiden oprettes der en ny timeseddel for timeseddelperioden på baggrund af den aktuelle dato. Arbejdsugen vises. Hvis der er flere uger i timeseddelperioden, kan du vælge en anden arbejdsuge i arbejdsugens faner.
Hvis der findes en timeseddel for den aktuelle dato, vises den. Hvis du har brug for at oprette en ny timeseddel i en anden timeseddelperiode, skal du vælge knappen **Menu** og derefter vælge **Ny timeseddel**.

Du kan angive projektoplysninger ved at klikke på handlingen **Tilføj tid** eller handlingen **Kopier tid fra**. Handlingen **Kopier tid fra** kopierer projektlinjeoplysninger, men ikke disse timer. Menuen **Kopiér tid fra** indeholder følgende indstillinger:

- **Kopier fra eksisterende timeseddel** - Kopier timeseddellinjer fra en eksisterende timeseddel.

- **Kopiér fra favoritter** – Opret nye timeseddellinjer ved hjælp af de timeseddelindstillinger, du har valgt som favoritter.

- **Kopier fra tildeling** – Opret nye timeseddellinjer fra tildelte projekter.

De projektoplysninger, der vises, afhænger af de mobilparametre, du har defineret på siden **Projektstyring og regnskabsparametre**.

I feltet **Juridisk enhed** skal du vælge den juridiske enhed, som du har udført projektarbejde for. Feltet **Juridisk enhed** er kun tilgængeligt, hvis understøttelse af interne timesedler er aktiveret for din juridiske enhed.

Vælg den kunde, der er knyttet til projektet for timesedlen. For den første udgivelse til Android understøttes kundens registrering ikke, da du først skal vælge projektet. Hvis du har valgt projektet først, udfyldes feltet **Kunde** automatisk.

I feltet **Projekt** skal du vælge det projekt, som du angiver tid for. Feltet **Kunde** udfyldes automatisk.

Du kan bruge søgningerne for kunde- og projektopslag til at søge på tværs af både kunder og projekter.

Vælg oplysninger i felterne **Kategori**, **Aktivitet**, **Linjeegenskab**, **Momsgruppe** og **Momsgruppe for varesalg** efter behov. Disse felter kan tilsidesættes.

Feltet **Linjeegenskab** angives til en standardværdi, der er baseret på projektstyring og regnskabsparametre. Når parametrene projekt/kategori og kategori/ressource er aktiverede, angives værdien for **Linjeegenskab** til den standardværdi, som du har angivet for denne validering. Når parametrene projekt/kategori og kategori/ressource ikke er aktiverede, vil værdien for **Linjeegenskab** som standard være baseret på feltet **Aktivér standardlinjeegenskab** på siden **Projektstyring og regnskabsparametre**. Værdien **Linjeegenskab** kan tilsidesættes.

Vælg en dag for at tilføje tid. Angiv det antal timer, du har arbejdet hver dag.

Hvis du vil tilføje kommentarer om de timer, du angiver, skal du klikke på **Tilføj kommentarer** og derefter skrive kommentarer til en internt målgruppe, en kundemålgruppe eller begge dele.
Interne kommentarer kan ses af projektledere. Kundekommentarer inkluderes i fakturaer.

Hvis du vil gemme linjen som en favorit, skal du markere afkrydsningsfeltet og derefter klikke på **Gem som favorit**.

Økonomiske dimensioner og vedhæftning af filer understøttes ikke i mobilprogrammet.

Fortsæt med at tilføje projektlinjer efter behov for at fuldføre timesedlen.

Klik på **Indsend** for at sende timesedlen til godkendelsesarbejdsgangen.

## <a name="review-timesheets"></a>Gennemse timesedler

Der findes en liste over de timesedler, der skal gennemgås, i menuen. Denne indstilling er kun tilgængelig, hvis du er angivet som godkender af arbejdsproces. Både overskrifts- og linjegodkendelser understøttes. Godkendelse på linjeniveau giver mulighed for at markere en eller flere linjer til godkendelse. Når du har gennemgået oplysningerne i timesedlen, skal du klikke på **Godkend**, **Deleger** eller **Vend tilbage** for at fortsætte arbejdsprocessen.
