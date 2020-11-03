---
title: Administration af flere kunder i projekttilbud
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med tilbud med flere kunder, som skal finansiere projektet. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074072"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Administration af flere kunder i projekttilbud (Sales)

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Projekttilbud understøtter det scenario, hvor forslaget omfatter flere kunder, som skal finansiere handlen. Fanen **Oversigt** for tilbuddet indeholder feltet **Potentiel kunde** , der identificerer den primære kunde for handlen. Du kan oprette andre kunder i forbindelse med handlen under fanen **Kunder** i projekttilbuddet.

Alle tilbudskunder på fanen **Kunder** i projekttilbuddet er som standard tilbudslinjekunder på alle **nye** projektbaserede tilbudslinjer, der er oprettet for tilbuddet. Eventuelle eksisterende projektbaserede tilbudslinjer arver ikke nye tilbudskundeposter, der er oprettet efter dem.

Produktbaserede tilbudslinjer knyttes automatisk til den primære kunde, der også er kunden i feltet **Potentiel kunde** under fanen **Oversigt** for tilbuddet.

Tilbudskunder og tilbudslinjekunder kan tilføjes, opdateres eller slettes når som helst, før tilbuddet er vundet.

## <a name="concept-of-a-primary-customer"></a>Begrebet en primær kunde

Den kunde, der er angivet under oversigtsfanen i projekttilbuddet som den potentielle kunde, er den primære kunde for tilbuddet. Når du forsøger at slette den primære kunde på kundelisten i tilbuddet, får du vist du en fejlmeddelelse om, at en primær kundepost i et tilbud ikke kan slettes.

Den primære kunde skal ikke opdateres fra kundelisten på tilbuddet. Du kan dog få indflydelse på den primære kunde ved at ændre den potentielle kunde under fanen **Oversigt** i tilbuddet. Når dette felt opdateres i **Tilbudsoversigten** , tilføjes den netop valgte potentielle kunde som en ny tilbudskunde med angivelse af flaget **Primær**. Den gamle potentielle kunde vil stadig være kunde i tilbuddet.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Opret, opdater eller slet en tilbudskundepost

Du kan oprette, opdatere eller slette en tilbudskunde under fanen **Tilbudskunder** på siden **Tilbud**. De felter, der vises i følgende tabel, findes i tilbudskundeposten for et projekttilbud.

| **Felt** | **Placering** | **Relevans, formål og vejledning** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Konto | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Viser alle aktive firmaer. Dette felt er låst, når posten er oprettet. Hvis du vil opdatere den, skal du slette posten og oprette den igen. Hvis du har registreret faktiske oplysninger, eller hvis tilbudskundeposten er en primær kunde, får du tilladelse til at slette posten. | Tilbudskunder kopieres på samme måde som tilbudslinjekunder, når der oprettes en tilbudslinje. Tilbudskunder kopieres også over til projektkontraktkunderne, når et tilbud er vundet. |
| Procentdel for opdeling af fakturering | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Repræsenterer den procentdel af hver ikke-faktureret salgstransaktion, der skal tilknyttes denne tilbudskunde. | Kopieret til nye tilbudslinjer og til projektkontraktkunder. |
| Faktura til Kontaktnavn | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Dette er et tekstfelt, der bruges til at identificere fakturakontaktpersonen for denne kunde. Disse hentes som standard fra den relaterede firmapost | Kopieret til projektkontraktkunder, når et tilbud er vundet, og tilbage igen til feltet Faktureres til kontraktnavn på den faktura, der er genereret for denne kunde. |
| Fakturering til navn | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Dette tekstfelt bruges til at identificere fakturakontaktpersonen for denne kunde. | Kopieret til projektkontraktkunderne, når et tilbud er vundet, og tilbage igen til feltet **Faktureres til kontraktnavn** på den faktura, der er genereret for denne kunde. |
| Bet.betingelser | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Dette er en grupperet indstilling med værdier, der som standard er hentet fra den relaterede firmapost. | Kopieret til projektkontraktkunderne, når et tilbud er vundet, og tilbage igen til feltet **Faktureres til kontraktnavn** på den faktura, der er genereret for denne kunde. |
| Er afrunding | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Angiver, om denne kunde er en standard afrundingskunde for denne handel. | Kopieret til projektkontraktkunderne, når et tilbud er vundet. |
| Grænse, der ikke må overskrides | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Indikerer, om der er en forhandlet grænse eller maksimum for det samlede beløb, der vil blive faktureret til denne kunde for denne aftale | Kopieret til projektkontraktkunderne, når et tilbud er vundet. |

## <a name="editing-billing-split-percentages"></a>Redigering af opdelingen af faktureringsprocenter

Du kan redigere procenter for opdeling af fakturering ved hjælp af redigeringsoplevelsen på det indbyggede gitter. Når procentsatsen for faktureringsopdeling ikke samlet set udgør 100 %, opstår der en fejl. Når du har opdateret procenter for opdeling af fakturering, skal du opdatere siden for at fjerne fejlen.

Du kan også prøve at vælge **Ligeligt fordel** på tilbudskundens undergitter. Denne handling tildeler faktureringsopdelinger til alle tilbudskunder. Hvis der er en afrundingsfaktor, vil den blive tilføjet til den afrundede kunde. En af tilbudskunderne er altid mærket som den afrundede kunde. Dette betyder, at tilbudskundeposten har flaget for **Afrunding** angivet til **Ja**. Dette er som regel den primære kunde for tilbuddet, men det kan ændres.
