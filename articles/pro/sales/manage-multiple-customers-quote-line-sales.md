---
title: Administrere flere kunder på projekttilbudslinjer
description: I denne artikel beskrives det, hvordan du administrerer flere kunder på projekttilbudslinjer.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 70007499ea61e7d81df071cc6d003896d721555b
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824431"
---
# <a name="manage-multiple-customers-on-project-quote-lines"></a>Administrere flere kunder på projekttilbudslinjer

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Projekttilbudslinjer understøtter scenarier, hvor hver tilbudslinje indeholder en liste over de kunder, der betaler for det. Denne kundeliste på den projektbaserede tilbudslinje kan være den samme som kundelisten i tilbuddet. Du kan også ændre kundelisten, så den afviger herfra. Når et projekttilbud er vundet, kopieres kundelisten på den projektbaserede tilbudslinje til den tilsvarende projektbaserede kontraktlinje for at oprette en eventuel projektkontrakt. Kunder i det projektbaserede tilbud kopieres til projektkontrakten.

Når du fakturerer den eventuelle projektkontrakt, har kundelisten på den projektbaserede kontraktlinje højere prioritet end listen i projektkontrakten. Kundelisten i projektkontrakten bruges kun for standarder på nye projektkontraktlinjer.

Alle tilbudskunder på fanen **Kunder** i projekttilbuddet er som standard tilbudslinjekunder på alle nye projektbaserede tilbudslinjer, der er oprettet for projekttilbuddet. Eventuelle eksisterende projektbaserede tilbudslinjer arver ikke nye tilbudskundeposter, der er oprettet efter dem.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Opret, opdater eller slet en tilbudslinjekundepost

Du kan oprette, opdatere eller slette en tilbudslinjekunde på fanen **Tilbudslinjekunder** på siden **Projektbaseret tilbudslinje**. Når du tilføjer en ny kunde til den projektbaserede tilbudslinje, tilføjes kunden også til det overordnede tilbud som en tilbudskunde med en standardprocent for opdeling af fakturering i det samlede tilbud på 0 %. Procentdelen for opdeling af fakturering i det overordnede tilbud kopieres til nye tilbudslinjer og til den eventuelle projektkontrakt. I forbindelse med fakturering fra kontrakten, bruges procentsatsen for faktureringsopdelingen dog på tilbudslinjeniveau og ikke procentsatsen for faktureringsopdelingen på det overordnede kontraktniveau. 

Følgende tabel viser de felter, findes i tilbudslinjekundeposten for en projektbaseret tilbudslinje.

| Felt | Lokation | Beskrivelse og vejledning | Downstream-virkning |
| --- | --- | --- | --- |
| **Firma** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularer for hurtig oprettelse af en tilbudslinjekunde. | Viser alle aktive firmaer. Dette felt er låst, når posten er oprettet. Hvis du har brug for at opdatere feltet, skal du slette posten og oprette den igen. Hvis du har registreret faktiske oplysninger, kan du ikke slette posten. | Når du vælger et firma på den overordnede liste over firmaer, der skal tilføjes, tilføjes tilbudslinjekunden også som en tilbudskunde, når du gemmer det. Når et tilbud vindes, kopieres tilbudslinjekunder over til projektkontraktlinjekunderne. |
| **Procentdel for opdeling af fakturering** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularer for hurtig oprettelse af en tilbudslinjekunde. | Repræsenterer den procentdel af hver ikke-faktureret salgstransaktion, der skal tilknyttes denne tilbudslinjekunde. | Kopieres til projektkontraktlinjekunder. |
| **Grænse, der ikke må overskrides** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularer for hurtig oprettelse af en tilbudslinjekunde. | Indikerer, hvorvidt der er en forhandlet grænse eller maksimum for det samlede beløb, der vil blive faktureret til denne kunde for denne tilbudslinje. | Kopieret til projektkontraktlinjekunderne, når et tilbud er vundet. |
| **Er afrunding** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularer for hurtig oprettelse af en tilbudslinjekunde. | Angiver, om denne kunde er en standard afrundingskunde for denne projektbaserede tilbudslinje. | Kopieret til projektkontraktkunderne, når et tilbud er vundet. |

## <a name="edit-billing-split-percentages"></a>Rediger opdelingen af faktureringsprocenter

Du kan redigere procentsatsen for opdeling af fakturering i linjen. Når procentsatsen for faktureringsopdeling ikke samlet set udgør 100 %, vises der en fejl. Når du har redigeret procentsatserne for opdeling af fakturering, skal du opdatere tilbudslinjesiden for at fjerne fejlen.

Brug handlingen ligeligt fordelt på tilbudslinjekunders undergitter til at fordele faktureringsopdelinger til alle tilbudslinjekunder. Hvis der er en afrundingsfaktor, vil den blive tilføjet til den afrundede kunde. En af tilbudslinjekunderne vil altid være mærket som en afrundingskunde, hvilket vil sige, at afrundingsflaget er angivet til **Ja** for kundeposten i tilbudslinjen. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
