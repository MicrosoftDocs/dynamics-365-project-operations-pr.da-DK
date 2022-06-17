---
title: Tilstandsovergange på en leverandørfaktura
description: I denne artikel forklares tilstandsovergange på en leverandørfaktura i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934313"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Tilstandsovergange på en leverandørfaktura

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I denne artikel forklares tilstandsovergange på en leverandørfaktura i Microsoft Dynamics 365 Project Operations. Følgende tilstande bruges: **Kladde**, **Under gennemsyn**, **Bekræftet**, **Afventer** og **Annulleret**.

Følgende illustrationer viser tilstandsovergangene.

![Model for tilstandsovergang i en underentreprise.](../media/VI_State_Model.jpg)

Følgende tabel forklarer, hvad de enkelte tilstande repræsenterer i livscyklussen for en leverandørfaktura i Project Operations.

| State | Description | Tilladte overgange |
| --- | --- | --- |
| Kladde | Denne tilstand er den første tilstand for en leverandørfaktura. Linjerne og priserne kan ændres. En leverandørfaktura med denne status kan redigeres og slettes. | Igangværende |
| Til gennemsyn | Denne tilstand repræsenterer behandlingstilstand for en leverandørfaktura. Mindst én leverandørfakturalinje har statussen som **Igangværende**. | Bekræftet, afventer |
| Bekræftet | Denne tilstand repræsenterer den fase for en leverandørfaktura, hvor programmet har oprettet faktiske omkostninger for hver enkelt leverandørfakturalinje. Alle tilknyttede faktiske omkostninger, der blev afstemt med leverandørfakturalinjerne, er blevet tilbageført og erstattet med de faktiske omkostninger fra de pågældende leverandørfakturalinjer. En leverandørfaktura med denne tilstand kan ikke redigeres eller slettes. Du kan bruge knappen **Annuller** til at annullere en bekræftet leverandørfaktura. Handlingen Annuller tilbagefører påvirkningen fra handlingen Bekræft. | Annullerede |
| I venteposition | <p>Denne tilstand repræsenterer en fase i en leverandørfaktura, hvor leverandørfakturaen ikke kan flyttes på grund af et problem med fakturaen eller leverandørens status. En leverandørfaktura i denne tilstand kan ikke bekræftes, annulleres, redigeres eller slettes.</p><p>Du kan bruge handlingen Åbn igen til at flytte leverandørfakturaen til tilstanden **Kladde** eller **Under gennemgang**. Hvis mindst én linje på leverandørfakturaen har statussen **Igangværende** eller **Fuldført**, åbnes leverandørfakturaen igen i tilstanden **Under gennemgang**. Hvis alle linjer på leverandørfakturaen har bekræftelsesstatus **Ikke påbegyndt**, åbnes leverandørfakturaen igen i tilstanden **Kladde**.</p> | Kladde, under gennemgang |
| Annullerede | Denne tilstand repræsenterer fasen i en underentreprise, hvor den faktiske levering af materialer og/eller arbejde ved hjælp af underleverandørressourcer ikke længere er påkrævet. En underentreprise i denne tilstand kan ikke bruges til at estimere og bemande projektkrav til ressourcer og materialer og kan heller ikke refereres til tid, udgifter og materialeforbrug i et projekt. En underentreprise i denne tilstand kan ikke redigeres eller slettes. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
