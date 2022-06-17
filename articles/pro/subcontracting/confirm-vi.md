---
title: Bekræft en projektleverandørfaktura
description: I denne artikel forklares det, hvordan du kan bekræfte en projektleverandørfaktura i Microsoft Dynamics 365 Project Operations og den økonomiske effekt af at bekræfte en projektleverandørfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932427"
---
# <a name="confirm-a-project-vendor-invoice"></a>Bekræft en projektleverandørfaktura

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Når du har kontrolleret alle linjer på en leverandørfaktura i Microsoft Dynamics 365 Project Operations, kan du bruge handlingen Bekræft til at bekræfte leverandørfakturaen.

Når du vælger **Bekræft** på en leverandørfaktura, indtræffer følgende funktionsmåde:

1. Tilstanden for leverandørfakturaen opdateres til **Bekræftet**.
2. Den bekræftede leverandørfaktura og de relaterede poster bliver skrivebeskyttet og kan ikke redigeres eller slettes.
3. Hvis en faktisk omkostning refererer til leverandørfakturalinjen som en del af afstemningsprocessen, tilbageføres alle faktiske omkostninger, der er knyttet til den refererede leverandørfakturalinje.
4. Nye faktiske omkostninger oprettes ved hjælp af oplysningerne på leverandørfakturalinjen.
5. Når leverandørfakturaen er bekræftet, kan du ikke længere oprette rettelseskladder, behandle tilbagekaldelser af tidsregistreringer eller annullere godkendelse af de oprindelige værdier for tid, udgifter eller materialer, der blev tilbageført.

> [!NOTE]
> Hvis en linje på en leverandørfaktura har en anden verifikationsstatus end **Fuldført**, kan leverandørfakturaen ikke bekræftes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
