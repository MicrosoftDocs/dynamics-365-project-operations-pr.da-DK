---
title: Opdater et projekt
description: Dette emne indeholder oplysninger om opdatering af projekter i Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: b0ec03a2c4dd7bc833b22b7a93fed810b4998a2788f4ff40234e3dd163bd9eb6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000884"
---
# <a name="update-a-project"></a>Opdater et projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Nedenfor vises en oversigt over de felter, der kan opdateres i et projekt, efter at det er blevet oprettet, og eventuelle relevante konsekvenser af opdateringerne.

## <a name="project-detail-fields"></a>Felter med projektdetaljer

- **Navn**: Projektets titel.
- **Beskrivelse**: En oversigt over projektet.
- **Kunde**: Den virksomhed, som projektet skal leveres til.
- **Kalenderskabelon**: Projektets arbejdstid. Når feltet ændres, genberegnes hele planen.
- **Valuta**: Valutaen for projektet. Dette felts standardindstillinger er baseret på den valuta, der er defineret i kontraktenheden. Når kontraktenheden opdateres, opdateres feltet også.
- **Kontraktenhed**: Den organisationsenhed, der repræsenterer den virksomhedsgruppe eller division, som primært er ansvarlig for at vinde salg og administrere levering af arbejde og servicer til kunden. 
- **Projektleder**: Det medlem af projektteamet, der har tilladelse til at gennemse og godkende tidsregistreringer og udgifter.

## <a name="estimate-fields"></a>Estimatfelter

- **Estimeret startdato**: Den dato, hvor projektet starter. Når dette felt opdateres, flyttes opgaver i projektet forholdsmæssigt sammen med den nye startdato.
- **Slutdato**: Den dato, hvor projektet er planlagt til at skulle slutte.
- **Indsats**: Projektets anslåede indsats. Når der tilføjes opgaver til projektet, kan du ikke længere redigere dette felt.
- **Estimeret arbejdskraftomkostninger**: De anslåede arbejdskraftomkostninger ved projektet. Når der tilføjes arbejdskraftomkostninger til projektet, kan du ikke længere redigere dette felt.
- **Estimerede udgifter**: De estimerede udgifter til projektet. Når der tilføjes udgifter til projektet, kan du ikke længere redigere dette felt.

## <a name="project-actual-fields"></a>Felter for faktiske projektoplysninger
- **Faktisk starttidspunkt**: Den dato, hvor projektet blev startet.
- **Faktisk sluttidspunkt**: Opdateres, når et projekt er fuldført.

## <a name="project-status-fields"></a>Felter til projektstatus

- **Overordnet projektstatus**: Den overordnede projekttilstand, der er angivet af projektlederen.
- **Kommentarer**: En kommentar om den aktuelle tilstand for projektet, som angives af projektlederen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]