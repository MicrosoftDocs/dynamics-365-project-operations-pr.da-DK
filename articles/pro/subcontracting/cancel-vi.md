---
title: Annuller en projektleverandørfaktura
description: I dette emne forklares det, hvordan du kan annullere en projektleverandørfaktura i Microsoft Dynamics 365 Project Operations og den økonomiske effekt af at annullere en projektleverandørfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580633"
---
# <a name="cancel-a-project-vendor-invoice"></a>Annuller en projektleverandørfaktura

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Når en leverandørfaktura er blevet bekræftet, kan den ikke redigeres eller slettes. Hvis der opstod en fejl på en leverandørfaktura, der blev bekræftet, kan du bruge handlingen Annuller til at fortryde påvirkningen af leverandørfakturaen og oprette en ny leverandørfaktura.

Når du vælger **Annuller** på en leverandørfaktura, indtræffer følgende funktionsmåde:

1. Tilstanden for leverandørfakturaen opdateres til **Annulleret**.
2. Den annullerede leverandørfaktura og de relaterede poster bliver skrivebeskyttet og kan ikke redigeres eller slettes.
3. Alle faktiske omkostninger, der er oprettet på grundlag af leverandørfakturalinjer som led i bekræftelsen af leverandørfaktura, tilbageføres.
4. Hvis faktiske omkostninger var knyttet til leverandørfakturalinjerne som en del af afstemningsprocessen, bliver de tilbageført af den oprindelige leverandørfakturabekræftelse. Under annullering af leverandørfakturaen oprettes de faktiske omkostninger igen. Oprindelsen peger på tids-, udgifts- eller materialeforbrugsposterne.
5. Når leverandørfakturaen er annulleret, kan du igen oprette rettelseskladder, behandle tilbagekaldelser af tidsregistreringer og annullere godkendelse af de oprindelige værdier for tid, udgifter eller materialer.

> [!NOTE]
> Det er kun bekræftede projektleverandørfakturaer, der kan annulleres. Leverandørfakturaer i andre tilstande kan ikke annulleres.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
