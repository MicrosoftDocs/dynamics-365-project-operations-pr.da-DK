---
title: Faktisk værdiers påvirkning i en fast prisengagement
description: Dette emne indeholder oplysninger om, hvordan en aftale med fastpris påvirker tabellen for faktiske værdier ved forskellige hændelser i løbet af en livscyklus i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579221"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Faktisk værdiers påvirkning i en fast prisengagement

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I følgende tabel vises de faktiske værdier for forskellige transaktionstyper, der oprettes ved forskellige hændelser i en aftale med fast pris.

| Hændelse | Faktisk omkostning | Ikke-faktureret faktisk salg | Faktureret faktisk salg | Eksempel |
|---|---|---|---|---|
| Tid oprettes. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | <p>Bob Kozack, fra afdelingen Fabrikam i USA, som har en omkostningssats på 100 amerikanske dollar (100 USD) i timen, arbejder på et projekt med navnet "Installation af arm ved Adatum". Dette projekt er tilknyttet en faktureringsmetode med fast pris på kontraktlinjen. Her er et eksempel på Bob Kozaks tidsregistrering:</p><p>Bob Kozack,- otte timer</p> |
| Tid er indsendt. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | Der oprettes en omkostningslinje for tidsposten. Standardomkostningssatsen angives i kladdeposteringen. |
| Tidsposten tilbagekaldes, før den godkendes. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | |
| Tiden godkendes. | Der oprettes en faktisk omkostning. | Ikke tilgængelig | Ikke tilgængelig | <p>Ny faktisk værdi, der oprettes:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD</li></ul> |
| Tidsgodkendelsen annulleres. | <p>Statussen for den oprindelige faktiske omkostningsværdi opdateres til **Justeret**.</p><p>Der oprettes en modpost til en faktisk omkostningsværdi, som har en tilpasningsstatus **Kan ikke justeres**.</p> | Ikke tilgængelig | Ikke tilgængelig | <p>Eksisterende faktisk værdi opdateres:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD, *Justeret*</li></ul><p>Ny faktisk værdi, der oprettes som modpost til den tidligere økonomiske påvirkning:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, (8 timer), (800 USD), *Kan ikke justeres*</li></ul> |
| Tidsposten tilbagekaldes, efter den godkendes. | <p>Statussen for den oprindelige faktiske omkostningsværdi opdateres til **Justeret**.</p><p>Der oprettes en modpost til en faktisk omkostningsværdi, som har en tilpasningsstatus **Kan ikke justeres**.</p> | Ikke tilgængelig | Ikke tilgængelig | <p>Eksisterende faktisk værdi opdateres:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD, *Justeret*</li></ul><p>Ny faktisk værdi, der oprettes som modpost til den tidligere økonomiske påvirkning:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, (8 timer), (800 USD), *Kan ikke justeres*</li></ul> |
| Kontrakten bekræftes. | <p>Statussen for den gamle faktiske omkostningsværdi opdateres til **Justeret**.</p><p>Der oprettes en modpost til faktiske omkostningsværdier, som har en tilpasningsstatus **Kan ikke justeres**.</p><p>Nye faktiske omkostningsværdier oprettes, når de kontraktmæssige regler revurderes.</p> | Ikke tilgængelig | Ikke tilgængelig | <p>Eksisterende faktisk værdi opdateres:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD, *Justeret*</li></ul><p>Ny faktisk værdi, der oprettes som modpost til den tidligere økonomiske påvirkning:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, (8 timer), (800 USD), *Kan ikke justeres*</li></ul><p>Ny faktisk værdi, der oprettes for den reevaluerede økonomiske påvirkning:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD</li></ul> |
| Der oprettes en faktura. | Ikke tilgængelig | Ikke tilgængelig | Ikke tilgængelig | |
| Fakturaen bekræftes med en milepæl. | Ikke tilgængelig | Ikke tilgængelig | Der oprettes nye faktiske værdier for milepælsbaserede fakturerede salg. | <p>Eksisterende faktisk værdi, der forbliver uændret:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD</li></ul><p>Ny faktisk værdi, der oprettes for at registrere de fakturerede salgsværdier:</p><ul><li>**Faktisk faktureret salg:** Milepæl, 5.000 USD</li></ul> |
| Fakturaen korrigeres, så milepælen krediteres. | Ikke tilgængelig | Ikke tilgængelig | Der oprettes modsvarene fakturerede faktiske salgsværdier. | <p>Eksisterende faktisk værdi, der forbliver uændret:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD</li></ul><p>Eksisterende faktisk værdi opdateres:</p><ul><li>**Faktisk faktureret salgsværdi**: Milepæl, 5.000 USD *Justeret*</li></ul><p>Ny faktisk værdi, der oprettes for at modsvare de forrige fakturerede salgsværdier:</p><ul><li>**Faktisk faktureret salgsværdi**: Milepæl, (5.000 USD) *Kan ikke justeres*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
