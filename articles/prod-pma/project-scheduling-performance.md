---
title: Ydeevne for et projekts ressourceplanlægning
description: Dette emne indeholder oplysninger om, hvordan du kan forbedre ydeevnen af ressourceplanlægning for et stort antal projekter.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074155"
---
# <a name="project-resource-scheduling-performance"></a>Ydeevne for et projekts ressourceplanlægning

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Ydeevneproblemer, der er relaterede til ressourceplanlægning, kan forekomme, når antallet af projekter når op i tusinder. Hvis du vil forbedre ydeevnen i ressourceplanlægning, er der en tilgængelig funktion, som gør det muligt for brugerne at reducere den tid, det tager at åbne formularen med ressourcetilgængelighed. Dette fjerner især processen med synkronisering af akkumulering af ressourcekapacitet og bruger tabellen **ResProjectResource** til at gøre søgningen i ressourcer hurtigere. Bemærk, at tabellen **ResRollup** ikke længere skal bruges.

> [!IMPORTANT]
> Hvis der er en afhængighed i enten processen med synkronisering af akkumulering af ressourcekapacitet eller tabellen **ResProjectResource**, skal du ikke bruge denne funktion.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Aktiver forbedring af ydeevnen for ressourceplanlægning
Hvis du vil aktivere forbedring af ydeevnen for ressourceplanlægning, skal du benytte følgende fremgangsmåde.

1. Gå til **Funktionsstyring** > **Alle**, og find **Aktiver funktionen til forbedring af ydeevnen for projektressourceplanlægning** på funktionslisten.
2. Vælg **Aktivér nu**.

> [!NOTE]
> Hvis du ikke kan finde funktionen på listen, skal du vælge **Søg efter opdateringer** for at opdatere listen.

3. Opdater browseren, og gå derefter til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Synkroniser ressourcekalenderes kapacitet på tværs af alle virksomheder**.
4. Angiv **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data. Hvis du vil oprette trinvise data, skal du angive den til **Nej**.
5. I feltet **Periodekode** skal du vælge den periode, hvor der skal genereres data. Hvis du vælger en periodekode, er det ikke nødvendigt at definere en start- og slutdato.
6. Hvis du lader feltet **Periodekode** være tomt, skal du vælge bestemte start- og slutdatoer for at oprette data.
7. Vælg **OK**.

 > [!NOTE]
 > Dette distribuerer generelle data til tabellen **ResCalendarCapacity** på tværs af alle virksomheder i dit miljø, så batchjobbet kun skal køres i én juridisk enhed. Dataene i denne kørsel skal bruges til at beregne ressourcekapaciteten via den tilknyttede kalender.

8. Gå til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Udfyld projektressourcer på tværs af alle virksomheder**, og vælg derefter **OK**. Dette er scriptet til dataopgradering for generelle data i tabellerne **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**. Værdierne for feltet **PSAPRojSchedRole.RootActivity** opdateres også. Hvis den ikke køres, vises der en advarsel, når du forsøger at udføre ressourceplanlægningshandlinger.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Deaktiver forbedring af ydeevnen for ressourceplanlægning

1. Gå til **Funktionsstyring** > **Alle**, og søg efter **Aktiver funktionen til forbedring af ydeevnen for projektressourceplanlægning**.
2. Vælg funktionen, og vælg derefter knappen **Deaktiver**.
3. Opdater browseren.
4. Gå til **Projektstyring og regnskab** > **Periodisk** > **Kapacitetssynkronisering** > **Synkroniser ressourcekapacitetsakkumuleringer**.
5. På siden **Synkronisering af akkumulering af kapacitet** skal du angive **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data. Hvis du vil oprette trinvise data, skal du angive den til **Nej**.
6. I feltet **Periodekode** skal du vælge den periode, hvor der skal genereres data. Hvis du vælger en periodekode, er det ikke nødvendigt at definere en start- og slutdato.
7. Hvis du lader feltet **Periodekode** være tomt, skal du vælge bestemte start- og slutdatoer for at oprette data.
8. Vælg **OK**.

> [!NOTE]
> Dette distribuerer generelle data til tabellen **ResRollup** på tværs af alle virksomheder i dit miljø, så batchjobbet kun skal køres i én juridisk enhed. Denne kørsel er nødvendig for alle visninger af **Ressourcetilgængelighed**. Hvis batchjobbet ikke køres, vil dataene **ResRollup** blive genereret løbende, hvilket kan tage lang tid.
