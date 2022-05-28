---
title: Nyheder i december 2021 – Project Operations lille udrulning
description: Dette emne giver oplysninger om de kvalitative opdateringer, der er tilgængelige i december 2021-udgivelsen af Project Operations lille udrulning.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585371"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Nyheder i december 2021 – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Dette emne gælder for følgende komponenter og versioner af Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø version 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

### <a name="subcontract-management"></a>Administration af underentrepriser 

- [Ansættelse af projektteammedlemmer via underentreprise](../subcontracting/subcontracting-project-team-members.md): En projektleder kan oprette navngivne eller generiske teammedlemmer med underleverandører og underentrepriselinjer for at påvirke bemanding og estimering.
- [Indstillinger for ansættelse af projektteammedlemmer via underentreprise](../subcontracting/subcon-options.md): Når der skal træffes valg mellem navngivne eller generiske projektteammedlemmer, kan projektlederen gennemse eksisterende underentrepriser eller oprette nye underentrepriser for et eller flere projektteammedlemmer. 
- [Omkostningsestimering i forbindelse med ressourcetildelinger via underentrepriser](../subcontracting/costing-subcon-ra.md): Projektomkostningsestimeringen tager højde for underleverandørressourcer og beregner deres pris ved hjælp af de indkøbsprislister, der er knyttet til underentrepriser. 
- [Konfigurer planlægningsområdet til at vise kontraktmedarbejdere og underleverandørkapacitet](../subcontracting/configure-sb-subcon.md): Planlægningsområdet i Project Operations kan nu konfigureres til at søge efter og foreslå kontraktmedarbejdertyper af reserverbare ressourcer og underleverandørkapacitet sammen med medarbejdere. Denne konfiguration kan anvendes, når der søges efter ressourcer inden for konteksten af bemanding for et bestemt projektkrav, eller når der søges uden for konteksten af et projektkrav.
- [Bemanding af et projekt med kontraktmedarbejdere og underleverandørkapacitet](../subcontracting/staffing-cw.md): Kontraktmedarbejdere kan nu reserveres på projekter ved hjælp af erfaringer fra planlægningsområdet.
- [Registrer tid, udgifter og materialeforbrug på projekter i forbindelse med komponenter fra underleverandører](../subcontracting/recording-subcon-actuals.md): Kontraktmedarbejdere kan registrere tid og udgifter, og projektteammedlemmer kan også registrere brugen af materialer, der er købt ved hjælp af en underentreprise i et projekt. Dette vil resultere i registrering af nøjagtige omkostninger for projekter, hvor der bruges købt kapacitet eller materialer.
- [Tilstandsovergange i en underentreprise](../subcontracting/subcon-states.md): Underentrepriser kan bekræftes til at udføre forhandlinger med leverandøren, lukkes for at indikere, at leveringen er fuldført, eller at den er annulleret for at angive, at kontrakten med leverandøren er afsluttet, før leveringen er fuldført.

### <a name="task-planning"></a>Opgaveplanlægning
- Forbedret fejlfinding for systemadministratorer. Når en bruger ikke kan åbne et projekt, kan administrator gennemse ikke-licensrelaterede fejl, der er genereret fra Project for the Web, i [Logfilerne for projektplanlægningen](../../project-management/schedule-api-logs.md).
- [Brug opgavechecklister i Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). I Microsoft Project for the Web kan du tilføje en kontrolliste til en opgave for at holde styr på bestemte elementer.

## <a name="quality-updates"></a>Kvalitetsopdateringer

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Planlægning og sporing | 2392596 | Planlægnings-API'er tillader nu opdateringer af felterne **Resterende indsats**, **Fuldført indsats** og **% fuldført**. |
| Planlægning og sporing | 2478497 | Planlægnings-API'erne for felterne **Aktivitetsnummer** og **Opgave-id** kan være tomme i input, da systemet udfylder dem ved hjælp af automatiseret nummerering.|
| Tid og udgift | 2468135 | Antallet af godkendelsesforsøg reduceres fra fem til tre. |
| Tid og udgift | 2468188 | Løst problemet med tekst i logfiler, der overskrider maksimumlængden i attributten **notetekst** for objektet **anmærkning**. |
