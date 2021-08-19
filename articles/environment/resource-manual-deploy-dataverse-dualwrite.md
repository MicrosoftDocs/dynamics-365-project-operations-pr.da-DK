---
title: Udrul Project Operations Dataverse-appen manuelt med understøttelse af dobbelt skrivning
description: I dette emne forklares det, hvordan du udruller Project Operations Dataverse-appen manuelt, så den understøtter dobbelt skrivning.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986439"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Udrul Project Operations Dataverse-appen manuelt med understøttelse af dobbelt skrivning

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

I dette emne forklares det, hvordan du udruller Microsoft Dynamics 365 Project Operations i Microsoft Dataverse manuelt, så den understøtter dobbelt skrivning. Project Operations registrerer miljøets konfiguration og tilføjer yderligere understøttelse af dobbelt skrivning, hvis forudsætningerne opfyldes.

Hvis du har fulgt instruktionerne i dette emne under udrulningen af Microsoft Dynamics Lifecycle Services (LCS), kan du springe udrulningen af Microsoft Power Platform-integrationen over (tidligere kendt som Common Data Service-miljøet) over.

Udrulningsprocessen for Project Operations i Dataverse, således at den understøtter dobbeltskrivning, har fire hovedtrin:

1. [Opret et nyt miljø i Dataverse, der understøtter dobbelt skrivning](#create).
2. [Tilføj forudsætninger for dobbelt skrivning i miljøet](#prerequisites).
3. [Tilføj appen Project Operations Dataverse](#dataverse).
4. [Link til dine miljøer](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Opret et nyt miljø i Dataverse, der understøtter dobbelt skrivning

Du skal logge på som en administrator for at fuldføre denne procedure.

1. Åbn [Power Platform Administration](https://admin.powerplatform.com), og log på som en administrator.
2. Opret et nyt miljø, og navngiv det.
3. Vælg miljøtypen. Hvis du tilmeldte dig prøvetilbuddet, skal du vælge **Prøveversion (abonnementsbaseret)**.
4. Bekræft udrulningsområdet.
5. Aktivér muligheden **Opret en database for dette miljø**. 
6. Bekræft sproget, og kontrollér derefter, at valutaen stemmer overens med valutaen for dine Finance and Operations-apps.
7. Aktivér muligheden **Dynamics 365-apps**, og bekræft, at feltet **Automatisk udrulning af disse apps** er angivet til **Ingen**.
8. Tilføj en sikkerhedsgruppe, hvis der kræves en sikkerhedsgruppe.
9. Vælg **Gem** for at oprette miljøet.
10. Vent, indtil udrulningen er fuldført, og miljøet når tilstanden **Klar**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Tilføj forudsætninger for dobbelt skrivning i miljøet.

Understøttelse af dobbelt skrivning omfatter yderligere felter, der tilføjes til nøgleobjekter såsom objektet **Virksomhed**. Hvis du tilføjer understøttelse af dobbelt skrivning til et eksisterende miljø, skal du måske opdatere dataene for at aktivere supporten. Du kan få flere oplysninger om, hvordan du bootstrapper dataene under [Bootstrap virksomhedsdata](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Du kan finde flere oplysninger om systemkrav til dobbelt skrivning under [Systemkrav til dobbelt skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Fuldfør denne procedure for at tilføje forudsætningerne for dobbelt skrivning til dit miljø.

1. Åbn det miljø, som du netop har oprettet, og gå derefter til **Resource** \> **Dynamics 365-apps**.
2. Vælg **Kerneløsning til dobbelt skrivning** på listen over apps, og installer den.
3. Vent, indtil installationen er fuldført. Vælg dernæst **Organisering af dobbelt skrivningsapplikation** på listen over apps, og installer den.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Tilføj appen Project Operations Dataverse

Du kan kun fuldføre denne procedure, hvis du har fuldført de tidligere procedurer, før du installerede Project Operations. Under installationen analyserer systemet miljøkonfigurationen og tilføjer understøttelse af dobbelt skrivning, hvis det er nødvendigt.

1. Åbn det miljø, som du oprettede tidligere, og gå derefter til **Resource** \> **Dynamics 365-apps**.
2. Vælg **Microsoft Dynamics 365 Project Operations** på applisten, og installer det.

## <a name="link-your-environments"></a><a name="link"></a>Link til dine miljøer

Når Dataverse-miljøet er udrullet, kan du konfigurere linket i dine Finance and Operations-apps. Følg trinnene i [Guiden til anvendelse af dobbelt skrivning for at linke til dine miljøer](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
