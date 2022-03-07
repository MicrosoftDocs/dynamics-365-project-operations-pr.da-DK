---
title: Opret og anvend betingelser for tilbageholdelse af leverandørbetaling
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer og vedligeholder tilbageholdelsesbetingelser for leverandørbetalinger.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 4ff725512aa0bcc87ff4670d6bb072f3bf780786c1f71b332914887f4d4ccf13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991209"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Opret og anvend betingelser for tilbageholdelse af leverandørbetaling

[!include [banner](../includes/banner.md)] 

Konfiguration af betingelser for tilbageholdelse af leverandørbetalinger for et projekt er nyttig, når organisationen ønsker at tilbageholde en del af de betalinger, der foretages til en leverandør. Det kan f.eks. være, hvis du vil have tilbageholde betalingen til en leverandør, indtil de leverede produkter opfylder dine forventninger. Du kan angive betingelser for tilbageholdelse af leverandørbetalinger, når du forhandler en leverandørkontrakt.

## <a name="create-vendor-payment-retention-terms"></a>Opret betingelser for tilbageholdelse af leverandørbetaling

Du kan angive procentdelen af leverandørbetalingen, som skal tilbageholdes, og den procentdel af tidligere tilbageholdte beløb, der skal frigives. Der tilbageholdes automatisk beløb for leverandørfakturaer, indtil kontrakten når den angivne afslutningstilstand. Når du har konfigureret betingelserne for tilbageholdelse, kan du anvende dem på alle projekter for den pågældende leverandør.

Benyt følgende fremgangsmåde for at konfigurere og vedligeholde tilbageholdelsesbetingelser for leverandørbetalinger. 

1. Gå til **Projektstyring og regnskab** > **Tilbageholdelse** > **Betingelser for tilbageholdelse af leverandørbetaling**.
2. Vælg **Ny** for at tilføje en ny betingelse for tilbageholdelse af leverandørbetaling. Værdien **Regel-id** for den nye betingelse angives automatisk. 
3. Angiv en kort beskrivelse i feltet **Beskrivelse**, og i oversigtspanelet **Betingelser** skal du vælge **Tilføj linje** for at angive betingelsesværdier for følgende:

   - **Procentdel af leverede enheder**: Angiv en færdiggørelsesprocent for betingelsen. Der tilbageholdes automatisk beløb for leverandørfakturaer, indtil projektets fuldførelsesfase svarer til den angivne procentdel. Hvis du f.eks. angiver 50,00, bevares beløb, indtil projektet er 50 procent fuldført.
   - **Procentdel, der skal tilbageholdes**: Angiv en procentdel af beløbet på leverandørfakturaen, der skal tilbageholdes. Hvis du f.eks. skriver 10,00, tilbageholdes 10 procent af beløbet på en leverandørfaktura, indtil projektet når den i feltet **Procentdel af leverede enheder** angivne fuldførelsesgrad.
   - **Procentdel, der skal frigives**: Vælg **Tilføj linje** for at angive en procentdel af alle tidligere tilbageholdte beløb, der skal frigives for det valgte niveau for projektets færdiggørelse.

> [!NOTE]
> Hvis du har mere end én milepæl for forskellige niveauer af projektets færdiggørelse, skal du angive en separat betingelseslinje for tilbageholdelse af leverandørbetaling for hver tilbageholdelsesregel. Hver linje kan angive en anden tilbageholdelsesprocent og en anden frigivelsesprocent for hvert enkelt angivet niveau af projektets fuldførelse.

Når du har oprettet betingelserne for tilbageholdelse af leverandørbetaling for en leverandør, kan du anvende betingelserne på et projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Anvend betingelser for tilbageholdelse af leverandørbetaling på et projekt

1. Gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter**, og åbn et projekt på projektlistesiden.
2. I oversigtspanelet **Leverandøraftaler** skal du vælge **Tilføj linje**.
3. I **Kontokodefelt** skal du vælge en af følgende indstillinger: 

   - **Tabel**: Betingelser for tilbageholdelse af leverandørbetaling gælder for en enkelt leverandør.
   - **Gruppe**: Betingelserne for tilbageholde af leverandørbetaling gælder for alle leverandører i en leverandørgruppe.
   - **Alle**: Betingelser for tilbageholdelse af leverandørbetaling gælder for alle leverandører.

4. I **feltet Leverandør/Leverandørgruppe** skal du vælge den leverandør eller leverandørgruppe, som betingelserne for tilbageholdelse af leverandørbetaling gælder for. Hvis du har valgt **Alle** i det foregående trin, er dette felt ikke tilgængeligt.
5. I feltet **Betingelser for tilbageholdelse af leverandørbetaling** skal du vælge de tilbageholdelsesbetingelser, som du oprettede i forrige procedure.
6. Hvis projektet også har betingelserne betal ved betaling (PWP) konfigureret for leverandøren, skal du angive tærskelprocenten for projektet i feltet **Tærskelprocent for betal ved betaling**.

Betingelserne for tilbageholdelse af leverandørbetaling vises også på de indkøbsordrer, du opretter for leverandøren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]