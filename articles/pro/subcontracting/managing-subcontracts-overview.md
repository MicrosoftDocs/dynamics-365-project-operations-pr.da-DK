---
title: Administration af underleverandører i Project Operations
description: Dette emne giver et overblik over den komplette proces for administration af underleverandører i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994224"
---
# <a name="subcontract-management-in-project-operations"></a>Administration af underleverandører i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Underleverancer i Microsoft Dynamics 365 Project Operations understøtter følgende forretningsprocesforløb.

![Procesflow for underleverancer](../media/SubcontractingProcessFlow.png)

Her er en trinvis beskrivelse af processen for underleverancer.

1. Projektlederen opretter en underleverance med en leverandør. De prislister, der er tilknyttet kreditorposten, bruges som standard til underleverancen. Leverandørkontoen har relationstypen **Kreditor** eller **Leverandør**.
2. Projektlederen kan specificere alle køb som linjeelementer i underleverancen. Underleverancelinjer kan indeholde tid, udgifter eller produkter. Den transaktionsklasse, der vælges på hver underleverancelinje, bestemmer, hvad linjen er beregnet til.
3. Administratoren af leverandørkontoen og projektlederen kan gentage valget for hele underleverancen. Prisfastsættelse kan justeres i købsprislister, der er tilknyttet underleverancen.
4. Hvis underleverancelinjen er til tiden på dette tidspunkt eller senere i processen, knytter kreditorkontoadministratoren kontakter til hver underleverancelinje. Denne tilknytning indeholder oplysninger til den projektleder, der arbejder med underleverancen. Når en kontaktperson er knyttet til en underleverancelinje, oprettes der automatisk en reserverbar ressource ud fra kontaktpersonen, hvis der ikke allerede findes en reserverbar ressource.
5. Faktureringsmetoden på hver underleverancelinje kan være **Fast pris** eller **Tid og materiale**. I forbindelse med underleverancelinjer med faste priser kan du oprette en milepælsbaseret faktureringsplan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
