---
title: Administrer flere kunder i projektbaserede tilbudslinjer
description: Dette emne indeholder oplysninger om, hvordan du administrerer flere kunder på projektbaserede tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffb89a954b8af9d726c64cceeafca638c3393130
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965755"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Administrer flere kunder i projektbaserede tilbudslinjer

Projektbaserede tilbudslinjer understøtter scenarier, hvor hver tilbudslinje indeholder en liste over de kunder, der betaler for det. Denne kundeliste på den projektbaserede tilbudslinje kan være den samme som kundelisten i tilbuddet. Du kan også ændre kundelisten, så den afviger herfra. Hvis du vil oprette en eventuel projektkontrakt, når et projekttilbud er vundet, kopieres kundelisten på den projektbaserede tilbudslinje til den tilsvarende projektbaserede kontraktlinje. Kunder i det projektbaserede tilbud kopieres til projektkontrakten.

Når du fakturerer den eventuelle projektkontrakt, har kundelisten på den projektbaserede kontraktlinje højere prioritet end listen i projektkontrakten. Kundelisten i projektkontrakten bruges kun som standard for nye projektkontraktlinjer.

Alle tilbudskunder på fanen **Kunder** i projekttilbuddet er som standard tilbudslinjekunder på alle nye projektbaserede tilbudslinjer, der er oprettet for projekttilbuddet. Eventuelle eksisterende projektbaserede tilbudslinjer arver ikke nye tilbudskundeposter, der er oprettet efter dem.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Opret, opdater eller slet en tilbudslinjekundepost

Du kan oprette, opdatere eller slette en tilbudslinjekunde på fanen **Tilbudslinjekunder** på siden **Projektbaseret tilbudslinje**. Når du tilføjer en ny kunde til den projektbaserede tilbudslinje, tilføjes kunden også til det overordnede tilbud som en tilbudskunde med en standardprocent for opdeling af fakturering i det samlede tilbud på 0 %. Procentdelen for opdeling af fakturering i det overordnede tilbud kopieres til nye tilbudslinjer og til den eventuelle projektkontrakt. Men når du fakturerer fra kontrakten, bruges procentsatsen for faktureringsopdelingen på tilbudslinjeniveau og ikke procentsatsen for faktureringsopdelingen på det overordnede kontraktniveau. 

Følgende tabel viser de felter, findes i tilbudslinjekundeposten for en projektbaseret tilbudslinje.

| Felt | Lokation | Beskrivelse og vejledning | Downstream-virkning |
| --- | --- | --- | --- |
| **Firma** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularen for hurtig oprettelse af en tilbudslinjekunde. | Viser alle aktive firmaer. Dette felt er låst, når posten er oprettet. Hvis du har brug for at opdatere feltet, skal du slette posten og oprette den igen. Hvis du har registreret faktiske oplysninger, kan du ikke slette posten. | Når du vælger et firma på den overordnede liste over firmaer, der skal tilføjes, tilføjes tilbudslinjekunden også som en tilbudskunde. Tilbudslinjekunder kopieres over til projektkontraktlinjekunderne, når et tilbud er vundet. |
| **Procentdel for opdeling af fakturering** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularen for hurtig oprettelse af en tilbudslinjekunde. | Repræsenterer den procentdel af hver ikke-faktureret salgstransaktion, der skal tilknyttes denne tilbudslinjekunde. | Kopieres til projektkontraktlinjekunder. |
| **Grænse, der ikke må overskrides** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularen for hurtig oprettelse af en tilbudslinjekunde. | Indikerer, hvorvidt der er en forhandlet grænse eller maksimum for det samlede beløb, der vil blive faktureret til denne kunde for denne tilbudslinje. | Kopieret til projektkontraktlinjekunderne, når et tilbud er vundet. |
| **Ejerselskab** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularen for hurtig oprettelse af en tilbudslinjekunde. | Den juridiske enhed, som denne kunde er konfigureret i, i modulet **Projektstyring og regnskab**. Dette felt er skrivebeskyttet og er angivet til ejerselskabet i selve tilbuddet. Kundelisten, der skal tilføjes i feltet **Firma**, er allerede filtreret til listen fra ejerselskabet i modulet **Projektstyring og regnskab** under Project Operations. | Ejerselskabet svarer til begrebet juridisk enhed. Der redegøres for alle omkostninger og indtægter, der påløber i forbindelse med dette projekt i finanskladden i ejerselskabet. |
| **Er afrunding** | Et redigerbart gitter under fanen **Tilbudslinjekunder** og den primære formular samt formularen for hurtig oprettelse af en tilbudslinjekunde. | Angiver, om denne kunde er en standard afrundingskunde for denne projektbaserede tilbudslinje. | Kopieret til projektkontraktkunderne, når et tilbud er vundet. |

## <a name="edit-billing-split-percentages"></a>Rediger opdelingen af faktureringsprocenter

Du kan redigere procentsatsen for opdeling af fakturering i linjen. Når procentsatsen for faktureringsopdeling ikke samlet set udgør 100 %, vises der en fejl. Når du har redigeret procentsatserne for opdeling af fakturering, skal du opdatere tilbudslinjesiden for at fjerne fejlen.

Brug handlingen ligeligt fordelt på tilbudslinjekunders undergitter til at fordele faktureringsopdelinger til alle tilbudslinjekunder. Hvis der er en afrundingsfaktor, vil den blive tilføjet til den afrundede kunde. En af tilbudslinjekunderne vil altid være mærket som en afrundingskunde, hvilket vil sige, at afrundingsflaget er angivet til **Ja** for kundeposten i tilbudslinjen. 
