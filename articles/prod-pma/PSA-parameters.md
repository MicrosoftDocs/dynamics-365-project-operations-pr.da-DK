---
title: Integrationsparametrene for Project Service Automation
description: I dette emne forklares, hvordan du kan konfigurere, hvordan standarddata angives, når du integrerer Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9793b680fc2be3b300689c4aded8005470f30519
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006414"
---
# <a name="project-service-automation-integration-parameters"></a>Integrationsparametrene for Project Service Automation

[!include[banner](../includes/banner.md)]

På siden **Integrationsparametrene for Project Service Automation** kan du konfigurere, hvordan standarddata skal angives, når du integrerer Dynamics 365 Project Service Automation med Dynamics 365 Finance. For at projekter kan synkroniseres fra Project Service Automation til Finance, skal du konfigurere følgende felter.

Hvis du vil åbne siden **Integrationsparametre for Project Service Automation**, skal du gå til **Projektstyring og regnskab** \> **Opsætning** \> **Dynamics 365 for Project Service Automation-integrationsparametre**. 

> [!NOTE]
> - Integration af projektopgaver, kategorier for udgiftsposteringer, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.
> - Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.


| Tabulator                    | Felt                | Beskrivelse |
|------------------------|----------------------|-------------|
| Generelt                | Standardprojekttype | Vælg standardprojekttypen. Når projekter synkroniseres fra Project Service Automation, bruges denne værdi, hvis du ikke har angivet en standardværdi i integrationsskabelonen. Under synkroniseringen angives feltet **Projekttype** for nye projekter til denne værdi. Værdien kan dog opdateres, når projektkontraktlinjerne synkroniseres fra Project Service Automation. |
|                        | Tidskategori        | Vælg standardtidskategorien. Denne værdi bruges, når tidsestimater synkroniseres fra Project Service Automation. Når de tidsestimater og faktiske tidsværdier synkroniseres fra Project Service Automation, angives feltet **Kategori** for nye tidsprognoser for projekter i Finance til denne værdi. |
|                        | Gebyrkategori         | Vælg standardgebyrkategorien. Denne værdi bruges, når de faktiske gebyrer synkroniseres fra Project Service Automation. Når de faktiske gebyrer synkroniseres fra Project Service Automation, angives feltet **Kategori** for nye gebyrtransaktioner i Finance til denne værdi. |
| Projektgruppestandarder | Projekttype         | Klik på **Ny** for at tilføje en række, hvor du kan vælge den projekttype, som standardprojektgruppen skal angives for. Det er kun muligt at vælge en bestemt projekttype én gang i konfigurationen. |
|                        | Projektgruppe        | Vælg standardprojektgruppen for den valgte projekttype. Når nye projekter synkroniseres fra Project Service Automation, angives feltet **Projektgruppe** til standardværdien for projekttypen, hvis du ikke har angivet en standardværdi i integrationsskabelonen. |
| Faktureringstypestandarder  | Faktureringstype         | Klik på **Ny** for at tilføje en række, hvor du kan vælge den faktureringstype, som standardlinjeegenskaben skal angives for. Det er kun muligt at vælge en bestemt faktureringstype én gang i konfigurationen. |
|                        | Linjeegenskab        | Vælg standardlinjeegenskaben for den valgte faktureringstype. Når nye tidsestimater, nye udgiftsestimater eller nye faktiske oplysninger synkroniseres fra Project Service Automation, angives feltet **Linjeegenskaber** til standardværdien for faktureringstypen. |
| Låsning af funktioner  | Ikke tilgængelig       | Vælg den funktionalitet, der skal deaktiveres i Finance for projekter og kontrakter, der kommer fra Project Service Automation. Du kan f.eks. deaktivere muligheden for at redigere kontrakter og projekter, oprette arbejdsopgavehierarkier og angive timesedler i Finance. Regnskabsrelaterede felter aktiveres fortsat, selvom de ikke er tilgængelige i parameterindstillingen. Alle funktioner er som standard aktiveret. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]