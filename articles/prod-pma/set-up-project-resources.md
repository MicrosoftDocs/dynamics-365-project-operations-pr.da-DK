---
title: Konfigurer projektressourcer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer eller anmoder om projektressourcer.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997684"
---
# <a name="set-up-project-resources"></a>Konfigurer projektressourcer

[!include [banner](../includes/banner.md)]

Du skal konfigurere en kalender og knytte den til en medarbejder eller en arbejder. Kalenderen bruges til at planlægge projektet og arbejdstiden for de ressourcer, der er reserveret til projektet. I forbindelse med kalenderkonfigurationen kan projektledere udføre ressourceudjævning som led i ressourceoptimering. Afhængigt af kalenderplanen kan der indføres begrænsninger for ressourcer. Du kan konfigurere en kalender på siden **Kalendere**.

Når du konfigurerer en arbejder som en projektressource, kan du vælge mellem arbejdere, der arbejder i den virksomhed, som du opretter ressourcer for. Du kan også vælge arbejdere fra andre firmaer i organisationen. Disse arbejdere kaldes interne ressourcer.

I følgende procedurer får du beskrevet, hvordan du kan konfigurere en arbejder som en projektressource i virksomheden, og hvordan du kan konfigurere en intern projektressource.

## <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbejder som en projektressource

1. På siden **Arbejdere** i listen **Arbejdere** skal du vælge den arbejder, som du tilføjer som en projektressource, og åbne arbejderposten.
2. Vælg **Projekt** &gt; **Opsætning** &gt; **Projektopsætning** i handlingsruden.
3. Vælg en kalender, og luk derefter siden.

Du kan også angive standardprojekter for en ressource som en slags forhåndstildeling. Forhåndstildelinger kan bruges, når ressourceledere eller projektleder på forhånd ved, hvilke projekter, som ressourcen skal arbejde på. Forhåndstildelinger kan også være baseret på anmodningen fra en projektsponsor eller kunde. Hvis du vil forhåndstildele et projekt, skal du på siden **Tildel projekter** under fanen **Projekter** i listen **Resterende projekter** vælge det relevante projekt.

## <a name="set-up-an-intercompany-resource"></a>Konfigurer en intern ressource

Når du konfigurerer en arbejder som en intern ressource, skal du fuldføre opsætningen i udlånsvirksomheden og den låntagende virksomhed.

### <a name="in-the-lending-company"></a>I udlånsvirksomheden

1. I Finance skal du kontrollere, at udlånsvirksomheden er valgt, og derefter fuldføre proceduren i forrige afsnit "Konfigurer en arbejder som en projektressource".
2. På siden **Internt regnskab** skal du vælge **Ny**.
3. I feltet **Juridisk enheds-id** skal du vælge udlånsvirksomheden. Udfyld de resterende felter efter behov, og vælg derefter **Gem**.
4. På siden **Overførelsespris** skal du vælge **Ny**.
5. I feltet **Juridisk låneenhed** skal du vælge den passende virksomhed.
6. Hvis du kun vil låne den låntagende virksomhed den ressource, som du oprettede i starten af denne sektion, skal du i feltet **Ressource** vælge navnet på den ressource, som du oprettede. Lad feltet **Ressource** være tomt, hvis alle ressourcer i udlånsvirksomheden skal være tilgængelige for den låntagende virksomhed.
7. På siden **Projektstyring og regnskabsparametre** skal du under fanen **Internt** angive indstillingen **Aktiver planlægning af intern ressource og timesedler** til **Ja**.

### <a name="in-the-borrowing-company"></a>I den låntagende virksomhed

- På siden **Ressourceliste** skal du i søgefiltret angive navnet på den ressource, som du oprettede til udlånsvirksomheden, for at verificere, at navnet er inkluderet i ressourcelisten for den låntagende virksomhed.

## <a name="request-project-resources"></a>Anmod om projektressourcer
Funktionaliteten i planlægningen af projektressourcer giver kun de ressourceansvarlige distribuere personaleressourcer til aftaler eller projekter. Hvis du vil aktivere denne funktion, skal du udføre følgende opgaver eller kontrollere, at de er blevet fuldført:

- Konfigurer nummerserier.
- Konfigurer arbejdsgange for projektstyring og regnskab.
- Aktivér arbejdsprocesser for ressourceanmodninger.

Når de foregående opgaver er fuldført, kan du udføre følgende opgaver, som du har brug for:

- Opret en ressourceanmodning på baggrund af en midlertidigt reserveret personaleressource.
- Overvåg ressourceanmodninger.
- Opfyld ressourcekrav.
- Anmod om en personaleressource fra et WBS.
- Reserver ressourcer til et projekt, uden at der skal anmodes om en personaleressource.


[!INCLUDE[footer-include](../includes/footer-banner.md)]