---
title: Bekræft en projektleverandørfaktura
description: I denne artikel forklares det, hvordan du kan bekræfte en projektleverandørfaktura i Microsoft Dynamics 365 Project Operations og den økonomiske effekt af at bekræfte en projektleverandørfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261504"
---
# <a name="confirm-a-project-vendor-invoice"></a>Bekræft en projektleverandørfaktura

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
