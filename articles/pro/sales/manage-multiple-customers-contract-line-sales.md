---
title: Administrer flere kunder i projektbaserede kontraktlinjer - lille
description: Dette emne indeholder oplysninger om administration af flere kunder på projektbaserede kontraktlinjer.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 565ae4d2c639b3933c0a05c04f27367ef16fece7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593099"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Administrer flere kunder i projektbaserede kontraktlinjer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Projektbaserede kontraktlinjer kan inkludere en liste over de kunder, der er ansvarlige for betalingen. Denne liste over kunder på den projektbaserede kontraktlinje kan være den samme som listen over kunder i kontrakten, men det er ikke et krav. Når et projekttilbud er vundet, og der oprettes en projektkontrakt, kopieres kundelisten på tilbudslinjen til den tilsvarende kontraktlinje. Kunder i tilbuddet kopieres til kontrakten.

Når projektkontrakten er faktureret, prioriteres kundelisten på projektbaseret kontraktlinje over den kundeliste, der findes på kontrakten. Kundelisten på projektkontrakten bruges kun som standard til nye kontraktlinjer.

Alle kontraktkunder på fanen **Kunder** i projektkontrakten er som standard kontraktlinjekunder i alle nye kontraktlinjer, der oprettes for projektkontrakten. De eksisterende kontraktlinjer arver ikke de nye kontraktkundeposter, der er oprettet efter dem.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Opret, opdater eller slet en kontraktlinjekundepost

Du kan oprette, opdatere eller slette en kontraktlinjekunde fra fanen Kontraktlinjekunder på siden Projektbaseret kontraktlinje. Når der tilføjes en ny kunde på den projektbaserede kontraktlinje, tilføjes denne også i den overordnede kontrakt som en kontraktkunde med en standardprocent for fakturaopdeling på nul. Faktureringsopdelingsprocenten i den overordnede kontrakt kopieres til nye kontraktlinjer og til en eventuel projektkontrakt. Men ved fakturering fra kontrakten er det opdelingsprocenten for fakturering på kontraktlinjeniveauet, der bruges, og ikke for opdelingsprocenten for fakturering på det overordnede kontraktniveau.

Nedenfor vises de felter på **Kontrakt**-linjens kundepost for en projektbaseret kontraktlinje, som du skal huske, når du arbejder med den:

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| **Firma** | Redigerbart gitter på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Alle aktive konti. Dette felt er låst, når posten er oprettet. Hvis du vil opdatere feltet, skal du slette posten og oprette en ny post. Hvis du har registreret faktiske værdier, kan du ikke slette posten. Du kan dog markere opdelingsprocentdelen for fakturering som nul for den pågældende konto. Når posten er markeret med nul, påvirkes eventuelle fremtidige faktiske værdier for omkostninger og indtægter, der skyldes eller opdeles til denne kunde. | Når du vælger en konto på den overordnede liste over konti for at tilføje og gemme dem, tilføjes kontraktlinjekunden også som en kontraktkunde. Kontraktlinjekunder bruges, når der genereres fakturaer. |
| **Procentdel for faktureringsopdeling** | Redigerbart gitter på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | I dette felt vises procentdelen af hver ikke-faktureret salgstransaktion, der skal tildeles denne kontraktlinjekunde. | Kontraktlinjekunder og faktureringsopdelingsprocenter bruges, når faktiske værdier oprettes efter godkendelsen, og når fakturaen genereres. |
| **Grænse, der ikke må overskrides** | Redigerbart gitter på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Angiver, om der er en forhandlet grænse eller loft for det samlede beløb, der faktureres denne kunde for kontraktlinjen. | Grænsen, der ikke må overskrides for kontraktlinjekunden, bruges, når der oprettes faktiske værdier og genereres fakturaer. |
| **Er afrunding** | Redigerbart gitter på fanen **Kontraktkunder** og **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Feltet angiver, om denne kunde er en standardafrundingskunde for denne projektbaserede kontraktlinje. | Når du opretter en faktisk værdi i henhold til den faktureringsopdelingsprocenten, kan der være visse afrundingsdifferencer. Denne kunde er i dette tilfælde blevet tilskrevet afrundingsdifferencerne. |

## <a name="edit-billing-split-percentages"></a>Rediger opdelingen af faktureringsprocenter

Faktureringsopdelingsprocenter kan redigeres i gitteret. Når faktureringsopdelingsprocenterne ikke udgør 100 procent i alt, opstår der en fejl. Når du har redigeret faktureringsopdelingsprocenterne, skal du opdatere siden for at fjerne fejlen.

Du kan også vælge **Fordel ligeligt** på kontraktlinjekundens undergitter. Denne handling allokerer faktureringsopdelinger til alle kontraktlinje kunder ligeligt. Hvis der er en afrundingsfaktor, vil den blive føjet til den afrundede kunde. En kontraktlinjekunde er altid mærket som den **Afrundede** kunde, hvor **Afrundingsflaget** er angivet til **Ja**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]