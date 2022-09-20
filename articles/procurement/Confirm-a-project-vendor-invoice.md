---
title: Bekræfte projektleverandørfakturaer
description: Denne artikel forklarer, hvordan du kan bekræfte en projektleverandørfaktura i Microsoft Dynamics 365 Project Operations, og den økonomiske effekt af at bekræfte en projektleverandørfaktura.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475413"
---
# <a name="confirm-project-vendor-invoices"></a>Bekræfte projektleverandørfakturaer

**Finder anvendelse på:** Project Operations til ressource-/ikke-lagerbaserede scenarier

Når parameteren **Manuel bekræftelse fra PM er påkrævet** er aktiveret, har de leverandørfakturaer, der er oprettet i Microsoft Dataverse, status af **Kladde**. Leverandørfakturaer, der oprettes på denne måde, skal gennemses og bekræftes manuelt. Når parameteren **Manuel bekræftelse fra PM er påkrævet** er deaktiveret, er de leverandørfakturaer, der er oprettet i Dataverse, automatisk bekræftet. Ingen yderligere handling er nødvendig. 

Når du har kontrolleret alle linjer på en leverandørfaktura i Dynamics 365 Project Operations, skal du vælge **Bekræft** for at bekræfte leverandørfakturaen.

Når du vælger **Bekræft** på en leverandørfaktura, indtræffer følgende funktionsmåde:

1. Status for leverandørfakturaen opdateres til **Bekræftet**.
1. Den bekræftede leverandørfaktura og de relaterede poster bliver skrivebeskyttet og kan ikke redigeres eller slettes.
1. Hvis en faktisk omkostning refererer til leverandørfakturalinjen som en del af afstemningsprocessen, tilbageføres alle faktiske omkostninger, der er knyttet til den refererede leverandørfakturalinje.
1. Nye faktiske omkostninger oprettes ved hjælp af oplysningerne på leverandørfakturalinjen.
1. Du kan ikke længere oprette rettelseskladder, behandle tilbagekaldelser af tidsregistreringer eller annullere godkendelse af de oprindelige værdier for tid, udgifter eller materialer, der blev tilbageført.
1. I Dynamics 365 Finance opdateres **Projektomkostning**-værdien ved hjælp af projektintegrationskladden, og integrationskontoen for indkøb *tilbageføres*, efter at projektintegrationskladden er bogført.

> [!NOTE]
> Hvis en linje på en leverandørfaktura har en anden verifikationsstatus end **Fuldført**, kan leverandørfakturaen ikke bekræftes.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
