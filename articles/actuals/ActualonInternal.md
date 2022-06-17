---
title: Faktiske værdiers konsekvens for et internt projekt
description: Denne artikel indeholder oplysninger om, hvordan forskellige hændelser påvirker tabellen for faktiske værdier i forbindelse med et internt projekt i Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921341"
---
# <a name="actuals-impact-for-an-internal-project"></a>Faktiske værdiers konsekvens for et internt projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I følgende tabel vises de faktiske værdier for forskellige transaktionstyper, der oprettes ved forskellige hændelser i et internt projektengagement.

| Hændelse | Faktisk omkostning | Eksempel |
|---|---|---|
| Tid oprettes. | Ikke tilgængelig | <p>Bob Kozack, fra afdelingen Fabrikam i USA, som har en omkostningssats på 100 amerikanske dollar (100 USD) i timen, arbejder på et projekt med navnet "Installation af arm ved Adatum". Dette projekt er tilknyttet en faktureringsmetode med fast pris på kontraktlinjen. Her er et eksempel på Bob Kozaks tidsregistrering:</p><p>Bob Kozack,- otte timer</p> |
| Tid er indsendt. | Ikke tilgængelig | Der oprettes en omkostningslinje for tidsposten. Standardomkostningssatsen angives i kladdeposteringen. |
| Tidsposten tilbagekaldes, før den godkendes. | Ikke tilgængelig | |
| Tiden godkendes. | Der oprettes en faktisk omkostning. | <p>Ny faktisk værdi, der oprettes:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD</li></ul> |
| Tidsgodkendelsen annulleres. | <p>Statussen for den oprindelige faktiske omkostningsværdi opdateres til **Justeret**.</p><p>Der oprettes en modpost til en faktisk omkostningsværdi, som har en tilpasningsstatus **Kan ikke justeres**.</p> | <p>Eksisterende faktisk værdi opdateres:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD, *Justeret*</li></ul><p>Ny faktisk værdi, der oprettes som modpost til den tidligere økonomiske påvirkning:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, (8 timer), (800 USD), *Kan ikke justeres*</li></ul> |
| Tidsposten tilbagekaldes, efter den godkendes. | <p>Statussen for den oprindelige faktiske omkostningsværdi opdateres til **Justeret**.</p><p>Der oprettes en modpost til en faktisk omkostningsværdi, som har en tilpasningsstatus **Kan ikke justeres**.</p> | <p>Eksisterende faktisk værdi opdateres:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, 8 timer, 800 USD, *Justeret*</li></ul><p>Ny faktisk værdi, der oprettes som modpost til den tidligere økonomiske påvirkning:</p><ul><li>**Faktisk omkostningsværdi:** Bob Kozack, (8 timer), (800 USD), *Kan ikke justeres*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
