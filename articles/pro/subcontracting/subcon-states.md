---
title: Tilstandsovergange på en underentreprise
description: I dette emne forklares tilstandsovergange på en underentreprise i Microsoft Dynamics 365 Project Operations, efterhånden som underentreprisen oprettes, udføres og lukkes.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c9533d046398c708c55467e6b1a25acf6abade3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579161"
---
# <a name="state-transitions-on-a-subcontract"></a>Tilstandsovergange på en underentreprise 

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I dette emne forklares tilstandsovergange på en underentreprise i Microsoft Dynamics 365 Project Operations. Hver enkelt tilstand repræsenteres enten som kladde, bekræftet, lukket eller annulleret. Følgende billede repræsenterer tilstandsovergange.

![Tilstandsmodel for underentreprise](../media/SubconStates.png)  

Følgende tabel indeholder en beskrivelse af, hvad de enkelte tilstande repræsenterer i livscyklussen for en underentreprise i Project Operations.

| State | Description | Tilladte overgange |
| --- | --- | --- |
| Kladde | Dette repræsenterer den oprindelige tilstand for en underleverandør. Der er igangværende forhandlinger med leverandøren. Linjerne og priserne kan ændres. En underentreprise i denne tilstand kan bruges til at estimere og bemande projektkrav til ressourcer og materialer. Der kan også refereres til dem i forbindelse med tid, udgifter og materialeforbrug i et projekt. En underentreprise i denne tilstand kan redigeres og slettes. | Bekræftet |
| Bekræftet | Dette repræsenterer fasen i en underentreprise, når forhandlingerne med leverandøren om prisfastsættelse og linjeelementer, der købes, er fuldført. Men den faktiske levering af materialer og/eller arbejde ved hjælp af underleverandørressourcer er stadig i gang. En underentreprise i denne tilstand kan bruges til at estimere og bemande projektkrav til ressourcer og materialer. Der kan også refereres til dem i forbindelse med tid, udgifter og materialeforbrug i et projekt. En underentreprise i denne tilstand kan ikke redigeres eller slettes. Knappen **Annuller** giver dig mulighed for at annullere en bekræftet underentreprise. Knappen **Åbn igen** giver dig mulighed for at genåbne underentreprisen igen for at ændre den til statussen **Kladde**. Brug knappen **Luk** til at lukke en bekræftet underentreprise. | Lukket <br> Annullerede <br> Kladde |
| Lukket | Dette repræsenterer fasen i en underentreprise, når den faktiske levering af materialer og/eller arbejde ved hjælp af underleverandørressourcer er fuldført. En underentreprise i denne tilstand kan ikke længere bruges til at estimere og bemande projektkrav til ressourcer og materialer. Der kan heller ikke længere refereres til dem i forbindelse med tid, udgifter og materialeforbrug i et projekt. En underentreprise i denne tilstand kan ikke redigeres eller slettes. | None |
| Annullerede | Dette repræsenterer fasen i en underentreprise, når den faktiske levering af materialer og/eller arbejde ved hjælp af underleverandørressourcer ikke længere er nødvendig. En underentreprise i denne tilstand kan ikke bruges til at estimere og bemande projektkrav til ressourcer og materialer og kan heller ikke refereres til tid, udgifter og materialeforbrug i et projekt. En underentreprise i denne tilstand kan ikke redigeres eller slettes. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
