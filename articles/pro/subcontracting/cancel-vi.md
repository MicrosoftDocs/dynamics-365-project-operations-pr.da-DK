---
title: Annuller en projektleverandørfaktura
description: Denne artikel redegør for, hvordan du kan annullere en projektleverandørfaktura i Microsoft Dynamics 365 Project Operations og den økonomiske effekt af at annullere en projektleverandørfaktura.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261083"
---
# <a name="cancel-a-project-vendor-invoice"></a>Annuller en projektleverandørfaktura

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
