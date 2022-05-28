---
title: Registrering af tid, udgifter og materialeforbrug for komponenter fra underleverandører
description: I dette emne forklares det, hvordan Microsoft Dynamics 365 Project Operations sporer tid, udgifter og materialeforbrug fra underleverandørkomponenter, der er registreret for projekter.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a31b4a1092cc4829cbfc789e8b8e30030b2826b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599217"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registrering af tid, udgifter og materialeforbrug på projekter for komponenter fra underleverandører

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I dette emne forklares det, hvordan Microsoft Dynamics 365 Project Operations sporer tid, udgifter og materialeforbrug fra underleverandørkomponenter, der er registreret for projekter.

## <a name="costing-for-subcontractor-time-on-projects"></a>Omkostninger for underleverandørtid på projekter
I Project Operations kan kontraktmedarbejdere registrere tid på projekter på samme måde som medarbejdere. Når der registreres tid på projekter og/eller projektopgaver, kan en kontraktmedarbejder vælge en bestemt underleverandør og underentrepriselinje.

Når den tid, der registreres af kontraktmedarbejdere, godkendes, registreres projektomkostningerne ved hjælp af den enhedsomkostningssats, der er konfigureret for den pågældende kontraktmedarbejderressource i sektionen **Rollepriser** i købsprislisten på underentreprisen.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Omkostninger for underleverandøromkostninger på projekter
Når du angiver udgifter, der er påløbet på projekter, kan du vælge en underleverandør og underentrepriselinje på udgiftsposten. 

Når denne udgiftsregistrering indsendes og godkendes, registreres udgiftsomkostningen på projektet på grundlag af den enhedsomkostningssats, der er konfigureret for den pågældende transaktionskategori i sektionen **Kategoripriser** i indkøbsprislisten på underentreprisen.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Omkostninger for underleverandørmaterialer på projekter
Når du angiver materialeforbrug på projekter, kan du vælge en underleverandør og underentrepriselinje i logfilen for materialeforbrug. Når logfilen for materialeforbrug indsendes og godkendes, registreres materialeomkostningen på projektet på grundlag af den enhedsomkostningssats, der er konfigureret for det produkt i sektionen **Prislisteelement** i underentreprisens prisliste.

Der kan også registreres materialeforbrug for produkter, der skal indkøbes, på projekter. Denne type materialeforbrug kan også knyttes til en underleverandør og underentrepriselinje. Når du registrerer materialeforbrug for produkter, der skal indkøbes, skal du angive enhedsprisen for det produkt, der skal indkøbes. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
