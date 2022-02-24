---
title: Konfigurer integration af Project Operations for de enkelte juridiske enheder
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer integrationen af juridiske enheder i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122876"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurer integration af Project Operations for de enkelte juridiske enheder 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne gennemgår de trin, der er nødvendige for at konfigurere Dynamics 365 Project Operations pr. juridisk enhed.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktiver funktionsnøgler i Dynamics 365 Finance

Benyt følgende fremgangsmåde for at aktivere de påkrævede funktioner.

1. I Dynamics 365 Finance skal du gå til arbejdsområdet **Funktionsstyring**.
2. I **Funktionslisten** skal du finde og aktivere følgende funktioner:
  
    - **Aktiver flere kontraktlinjer for et projekt**
    - **Aktiver Project Operations på Dynamics 365 Customer Engagement**

> [!NOTE]
> Hvis du ikke kan se de anførte **Funktionsnøgler**, skal du kontrollere, at din version af Finance opfylder minimumsversionskravet (programversion 10.0.13 eller højere, hvor alle kvalitetsopdateringer er anvendt). Vælg **Kontroller, om der er opdateringer** for at opdatere funktionslisten.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definer udrulningsscenariet for Project Operations for en juridisk enhed

Du kan aktivere Project Operations på Dynamics 365 Customer Engagement på juridisk enhedsniveau. Du kan have én juridisk enhed, som anvender Project Operations på Dynamics 365 Customer Engagement til ressource/ikke-lagerbaserede scenarier. Du kan i det samme miljø have en anden juridisk enhed, som anvender Project Operations i forbindelse med lagerførte/produktionsordrebaserede scenarier.

1. I Dynamics 365 Finance skal du gå til **Projektstyring og regnskab** > **Opsætning** > **Globale parametre for projektstyring og regnskab**.
2. Vælg objekter på listen over tilgængelige juridiske objekter, hvor funktioner vedrørende flere kontraktlinjer og Project Operations på Dynamics 365 Customer Engagement er aktiveret. Lad være med at vælge de juridiske enheder, der skal bruge Project Operations i forbindelse med lagerbaserede/produktionsordrescenarier.

> [!NOTE]
> Det er kun muligt at vælge en juridisk enhed, hvis den ikke har eksisterende projekter.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurer parametre for Projektstyring og regnskab

De enkelte juridiske objekter, der bruger lagerbaserede/produktionsordrescenarier på Dynamics 365 Customer Engagement, skal have et sæt standardparametre. Disse parametre er konfigureret under fanen **Project Operations** på siden **Parametre for projektstyring og regnskab**. Parametrene er:

  - **Standardfaktureringstyper**: Project Operations bruger et fast sæt faktureringstypestandarder, der skal knyttes til linjeegenskaber i Finance. Opret en post for hver faktureringstype: **Ikke angivet**, **Fakturerbar**, **Ikke-fakturerbar**, **Gratis** og **Ikke tilgængelig**.
  - **Standardprojektkategorier**: Vælg de standardprojektkategorier, der skal bruges for de enkelte transaktionstyper. Disse standardindstillinger bruges i **Integrationskladden i Project Operations** og i estimater, hvor der ikke er angivet nogen transaktionskategori for projektets faktiske værdi.
  - **Prognoser**: Vælg den prognosemodel, der skal bruges til estimater for tid og udgifter.
