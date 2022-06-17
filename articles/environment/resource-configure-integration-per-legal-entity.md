---
title: Konfigurer integration af Project Operations for de enkelte juridiske enheder
description: Denne artikel indeholder oplysninger om, hvordan du konfigurerer integration efter juridisk enhed i Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914671"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurer integration af Project Operations for de enkelte juridiske enheder 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Denne artikel indeholder en gennemgang af de trin, der kræves for at konfigurere Dynamics 365 Project Operations for hver juridisk enhed.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktivér funktionsnøgler i Dynamics 365 Finance

Benyt følgende fremgangsmåde for at aktivere de påkrævede funktioner.

1. Gå til arbejdsområdet **Funktionsstyring** i Dynamics 365 Finance.
2. I **Funktionslisten** skal du finde og aktivere følgende funktioner:
  
    - **Aktiver flere kontraktlinjer for et projekt**
    - **Aktiver Project Operations til Dynamics 365 Customer Engagement**

> [!NOTE]
> Hvis du ikke kan se de anførte **Funktionsnøgler**, skal du kontrollere, at din version af Finance opfylder minimumsversionskravet (programversion 10.0.13 eller højere, hvor alle kvalitetsopdateringer er anvendt). Vælg **Kontroller, om der er opdateringer** for at opdatere funktionslisten.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definer udrulningsscenariet for Project Operations for en juridisk enhed

Du kan aktivere Project Operations på Dynamics 365 Customer Engagement på juridisk enhedsniveau. Du kan have én juridisk enhed, der bruger Project Operations på Dynamics 365 Customer Engagement til ressource/ikke-lagerbaserede scenarier. Du kan i det samme miljø have en anden juridisk enhed, som anvender Project Operations i forbindelse med lagerførte/produktionsordrebaserede scenarier.

1. I Dynamics 365 Finance skal du gå til **Projektstyring og regnskab** > **Opsætning** > **Globale parametre for projektstyring og regnskab**.
2. På listen over tilgængelige juridiske enheder skal du vælge objekter, hvor flere kontraktlinjer og funktioner i Project Operations på Dynamics 365 Customer Engagement aktiveres. Lad være med at vælge de juridiske enheder, der skal bruge Project Operations i forbindelse med lagerbaserede/produktionsordrescenarier.

> [!NOTE]
> Det er kun muligt at vælge en juridisk enhed, hvis den ikke har eksisterende projekter.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurer parametre for Projektstyring og regnskab

Alle juridiske enheder, der bruger Project Operations på Dynamics 365 Customer Engagement, skal bruge et sæt standardparametre. Disse parametre er konfigureret under fanen **Project Operations** på siden **Parametre for projektstyring og regnskab**. Parametrene er:

  - **Standardfaktureringstyper**: Project Operations bruger et fast sæt faktureringstypestandarder, der skal knyttes til linjeegenskaber i Finance. Opret en post for hver faktureringstype: **Ikke angivet**, **Fakturerbar**, **Ikke-fakturerbar**, **Gratis** og **Ikke tilgængelig**.
  - **Standardprojektkategorier**: Vælg de standardprojektkategorier, der skal bruges for de enkelte transaktionstyper. Disse standardindstillinger bruges i **Integrationskladden i Project Operations** og i estimater, hvor der ikke er angivet nogen transaktionskategori for projektets faktiske værdi.
  - **Prognoser**: Vælg den prognosemodel, der skal bruges til estimater for tid og udgifter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]