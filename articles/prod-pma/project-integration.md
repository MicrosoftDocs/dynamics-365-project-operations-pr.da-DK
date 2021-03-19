---
title: Integration med Microsoft Project Client
description: Planlægning og vedligeholdelse af en projektplan kan være kompliceret, så projektlederne har brug for værktøjer, der hjælper dem med at administrere denne opgave. Integration med Microsoft Project Client understøtter oprettelse og administration af et projekts arbejdsopgavehierarki.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289317"
---
# <a name="microsoft-project-client-integration"></a>Integration med Microsoft Project Client

[!include [banner](../includes/banner.md)]

Planlægning og vedligeholdelse af en projektplan kan være kompliceret, så projektlederne har brug for værktøjer, der hjælper dem med at administrere denne opgave. Integration med Microsoft Project Client understøtter oprettelse og administration af et projekts arbejdsopgavehierarki. Projektlederen kan publicere eventuelle ændringer tilbage til Dynamics 365 Finance-projektets arbejdsopgavehierarki.

> [!NOTE]
> Hvis du bruger opdateringen fra juli (version 10.0.4), skal du installere KB 4054797 og 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurer Microsoft Project Client-tilføjelsesprogrammet
Hvis du vil aktivere integrationen med Microsoft Project Client, skal du installere et Microsoft Dynamics 365-tilføjelsesprogram i brugerens klient til Microsoft Project-programmet. Det kan du gøre ved at åbne **Arbejdsområdet for projektstyring**.

• Klik på **Konfigurer tilføjelsesprogrammet for projektklient** fra arbejdsområdesektionen **Links** > **Opsætning**.

• Klik på **Åbn**, og klik derefter på **Kør**, når du bliver bedt om det.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Åbn og rediger et eksisterende udkast til et arbejdsopgavehierarki i Microsoft Project Client
Hvis et projekt i Dynamics 365 Finance allerede har et arbejdsopgavehierarki, kan arbejdsopgavehierarkiet åbnes i Microsoft Project Client-programmet, hvis arbejdsopgavehierarkiet er i kladdestatus. Hvis du vil åbne siden **Projekt**, skal du klikke på linket **Åbn i Microsoft Project** fra fanen **Plan**. Du kan også åbne denne side fra Microsoft Project Client-programmet ved at klikke på **Åbn** i fanen **Microsoft Dynamics 365**. Vælg den **Juridiske enhed** og **Projektet** på listen.

> [!NOTE]
> Hvis du bruger Internet Explorer som browser, skal du klikke på **Gem** for at åbne den manuelt fra den placering, hvor filen er overført til. Du kan også klikke på **Gem og Åbn** for at åbne filen i Microsoft Project Client. Du skal ikke omdøbe filnavnet, når du gemmer.

Før du foretager ændringer af filen ved hjælp af Microsoft Project Client, skal du tjekke den ud. Klik på **Tjek ud** under fanen **Microsoft Dynamics 365**. Derved forhindres andre brugere i at redigere arbejdsopgavehierarkiet i Finance på samme tid. Hvis du vil publicere arbejdsopgavehierarkiet, når du har fuldført redigeringen, skal du klikke på **Tjek ind** på fanen **Microsoft Dynamics 365**.

Hvis der allerede er tilføjet en projektgruppe til projektet i Finance, udfyldes ressourcelisten med teammedlemmerne. Hvis et projektteam endnu ikke er blevet tilføjet til projektet, kan du vælge ressourcer og oprette teamet i Microsoft Project Client ved at klikke på knappen **Ressourcer** under fanen **Microsoft Dynamics 365**. 

Følgende data er synkroniseret tilbage til Finance som en del af indtjekningsprocessen:

• Opgavenavn

• Startdato

• Slutdato

• Foregående

• Ressourcenavne

• Kategori

• Ressourcekategori

• Arbejdstimer

• Noter

• Prioritet

> [!NOTE]
> Hvis du tilføjer andre kolonner til din Microsoft Project Client-fil, bliver de ikke gemt i filen, og de vises ikke, når filen åbnes igen.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Opret arbejdsopgavehierarkiet for et eksisterende projekt ved hjælp af Microsoft Project Client
Hvis du vil oprette et nyt arbejdsopgavehierarki ved hjælp af Microsoft Project Client, skal du følge disse trin:


1.  Åbn Microsoft Project Client.

2.  På fanen **Microsoft Dynamics 365** skal du klikke på **Åbn** .

3.  Vælg projektets **Juridiske enhed**.

4.  Vælg **Projektet**.

5.  Klik på **Tjek ud** under fanen **Microsoft Dynamics 365**.

6.  Når du er klar til at publicere til Finance, skal du klikke på **Tjek ind** under fanen **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Erstat det eksisterende arbejdsopgavehierarki for et eksisterende projekt ved hjælp af Microsoft Project Client
Hvis du vil oprette et nyt arbejdsopgavehierarki ved hjælp af Microsoft Project Client og erstatte et eksisterende arbejdsopgavehierarki for et eksisterende projekt, skal du følge disse trin:

1.  Åbn Microsoft Project Client.

2.  Opret skemaet i Microsoft Project Client.

3.  På fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Erstat eksisterende projekt**.

4.  Vælg projektets **Juridiske enhed**.

5.  Vælg **Projektet**.

6.  Klik på **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Opret et nyt projekt fra Microsoft Project Client


1.  Åbn Microsoft Project Client.

2.  Opret skemaet i Microsoft Project Client.

3.  På fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Gem som nyt projekt**.

4.  Vælg projektets **Juridiske enhed**.

5.  Angiv eventuelt **Projekt-id**.

6.  Angiv **Projektnavnet**.

7.  Vælg **Projekttype**, **Projektgruppe** og **Projektkontrakt-id**. Du kan også oprette en ny projektkontrakt ved at klikke på **Ny**.

8.  Vælg den **Kalender**, der skal bruges til ressourcer.

11. Klik på **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]