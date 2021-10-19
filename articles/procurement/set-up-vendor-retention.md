---
title: Konfigurere leverandørtilbageholdelse
description: I dette emne forklares, hvordan du konfigurerer leverandørtilbageholdelse.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594576"
---
# <a name="set-up-vendor-retention"></a>Konfigurere leverandørtilbageholdelse

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne indeholder oplysninger om, hvordan du konfigurerer leverandørtilbageholdelse.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Konfigurere en konto for leverandørtilbageholdelse i hovedbogen

1. I Dynamics 365 Finance skal du gå til **Hovedbog** > **Opsætning af bogføring** > **Konti for automatiske transaktioner**.
2. Tilføj en ny linje.
3. I feltet **Bogføringstype** skal du vælge **Leverandørtilbageholdelse**.
4. Vælg hovedkontoen til bogføring af leverandørtilbageholdelse.

## <a name="create-vendor-retention-terms"></a>Opret betingelser for leverandørtilbageholdelse

Brug siden **Betingelser for leverandørtilbageholdelse** for at konfigurere og fastholde tilbageholdelsesbetingelser leverandørbetalinger. Angiv procentdelen af leverandørbetalingen, som du vil tilbageholde, og den procentdel af tidligere tilbageholdte beløb, som du vil frigive. Der tilbageholdes automatisk beløb for leverandørfakturaer, indtil kontrakten når den angivne afslutningstilstand. Når betingelserne for tilbageholdelse er konfigureret for en leverandør, kan du anvende dem i alle de projekter, som leverandøren arbejder på.

1. I Finance skal du gå til **Projektadministration og regnskab** > **Opsætning** > **Tilbageholdelse** > **Betingelser for tilbageholdelse af leverandørbetaling**.
2. Vælg **Ny** for at tilføje en ny betingelse for tilbageholdelse af leverandørbetaling. Værdien i feltet **Regel-id** for den nye betingelse angives automatisk. 
3. Indtast et sigende navn for den nye betingelse i feltet **Beskrivelse**.
4. På fanen **Betingelser** skal du vælge **Tilføj linje** for at angive en periode for leverandørtilbageholdelse.
5. I feltet **Procentdel af leverede enheder** skal du angive en færdiggørelsesprocent for reglen. Beløb tilbageholdes automatisk for leverandørfakturaer, indtil projektstadiet for færdiggørelse er lig med den procentdel, som du angiver. Hvis du f.eks. angiver 50,00, bevares beløb, indtil projektet er 50 procent fuldført.
6. I feltet **Procentdel, der skal tilbageholdes** skal du angive den procentdel af et beløb på en leverandørfaktura, der skal tilbageholdes. Hvis du f.eks. skriver 10,00 i feltet, tilbageholdes 10 procent af beløbet på leverandørfakturaer, indtil projektet når den færdiggørelsesgrad, du har valgt i feltet **Procentdel af leverede enheder**.
7. I feltet **Procentdel, der skal frigives** skal du angive den procentdel af eventuelle tidligere tilbageholdte beløb, der skal frigives på det valgte færdiggørelsesniveau for projektet.

> [!NOTE]
> Hvis du har mere end én milepæl for forskellige niveauer af projektfærdiggørelse, skal du angive en særskilt linje for betingelser for leverandørtilbageholdelse for alle tilbageholdelsesregler. Hver linje kan angive én procentdel, der skal tilbageholdes, og en anden procentdel, der skal frigives, for hvert angivet niveau af projektfærdiggørelse.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Konfigurer en leverandøraftale for projektet

Konfigurer de betingelser for leverandørtilbageholdelse, der gælder for projektet. Betingelserne for tilbageholdelse af leverandørbetaling vises også på de indkøbsordrer, du opretter for leverandøren.

1. I Finance skal du gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter**. 
2. Vælg et projekt, og vælg i handlingsrunden **Projektgruppe** > **Leverandøraftaler**.
3. På siden **Leverandøraftaler** skal du tilføje en ny linje.
4. I feltet **Kontokode** skal du vælge en af følgende indstillinger:
   - **Tabel**: Betingelser for tilbageholdelse af leverandørbetaling gælder for en enkelt leverandør.
   - **Gruppe**: Betingelserne for tilbageholde af leverandørbetaling gælder for alle leverandører i en leverandørgruppe.
   - **Alle**: Betingelser for tilbageholdelse af leverandørbetaling gælder for alle leverandører.
5. I feltet **Leverandør/Leverandørgruppe** skal du vælge den leverandør eller leverandørgruppe, som betingelserne for tilbageholdelse af leverandørbetaling gælder for. Hvis du har valgt **Alle** i det foregående trin, er dette felt ikke tilgængeligt.
6. I feltet **Betingelser for leverandørtilbageholdelse** skal du vælge regel-id'et for de tilbageholdelsesbetingelser, der skal gælde for denne leverandør.

