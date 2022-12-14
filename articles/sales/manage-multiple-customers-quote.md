---
title: Administrere flere kunder i et projektbaseret tilbud
description: Denne artikel indeholder oplysninger om, hvordan du arbejder på tilbud, der omfatter flere kunder, som skal finansiere projektet.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b9c82ababdb9a588a0d28cae60a49d0594378d9
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825141"
---
# <a name="manage-multiple-customers-on-a-project-based-quote"></a>Administrere flere kunder i et projektbaseret tilbud

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Projektbaserede tilbud understøtter det scenarie, hvor forslaget omfatter flere kunder, som skal finansiere handlen. Fanen **Oversigt** for tilbuddet indeholder feltet **Potentiel kunde**, som identificerer den primære kunde for handlen. Du kan oprette andre kunder i forbindelse med handlen under fanen **Kunder** i projekttilbuddet.

Alle tilbudskunder på fanen **Kunder** i projekttilbuddet er som standard tilbudslinjekunder på alle **nye** projektbaserede tilbudslinjer, der er oprettet for tilbuddet. Eventuelle eksisterende projektbaserede tilbudslinjer arver ikke nye tilbudskundeposter, der er oprettet efter dem.

Tilbudskunder og tilbudslinjekunder kan tilføjes, opdateres eller slettes når som helst, før tilbuddet er vundet. En gyldig kunde på tilbuddet skal være oprettet som kunde i ejerselskabet eller den juridiske enhed på siden **Kunder**. Juridiske enheder konfigureres i modulet **Projektstyring og regnskab** i Dynamics 365 Project Operations og er tilgængelige som virksomheder i modulerne **Projektsalg og levering** i Project Operations.

## <a name="concept-of-a-primary-customer"></a>Begrebet en primær kunde

Den kunde, der vises under fanen **Oversigt** i projekttilbuddet som den potentielle kunde, er den primære kunde for tilbuddet. Hvis du forsøger at slette den primære kunde på kundelisten i tilbuddet, modtager du en fejlmeddelelse om, at en primær kundepost i et tilbud ikke kan slettes.

Den primære kunde skal ikke opdateres fra kundelisten på tilbuddet. Du kan dog få indflydelse på den primære kunde ved at ændre den potentielle kunde under fanen **Oversigt** i tilbuddet. Når dette felt opdateres i **Tilbudsoversigten**, tilføjes den netop valgte potentielle kunde som en ny tilbudskunde med angivelse af flaget **Primær**. Den gamle potentielle kunde vil stadig være kunde i tilbuddet.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Opret, opdater eller slet en tilbudskundepost

Du kan oprette, opdatere eller slette en tilbudskunde under fanen **Tilbudskunder** på siden **Tilbud**. De felter, der vises i følgende tabel, findes i tilbudskundeposten for et projekttilbud.

| **Felt** | **Placering** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Konto | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Viser alle aktive firmaer. Dette felt er låst, når posten er oprettet. Hvis du vil opdatere den, skal du slette posten og oprette den igen. Hvis du har registreret faktiske oplysninger, eller hvis tilbudskundeposten er en primær kunde, får du tilladelse til at slette posten. | Tilbudskunder kopieres på samme måde som tilbudslinjekunder, når der oprettes en tilbudslinje. Tilbudskunder kopieres også over til projektkontraktkunderne, når et tilbud er vundet. |
| Procentdel for opdeling af fakturering | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Repræsenterer den procentdel af hver ikke-faktureret salgstransaktion, der skal tilknyttes denne tilbudskunde. | Kopieret til nye tilbudslinjer, der er oprettet, og til projektkontraktkunder. |
| Faktura til Kontaktnavn | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Dette er et tekstfelt, der bruges til at identificere fakturakontaktpersonen for denne kunde. Disse hentes som standard fra den relaterede firmapost | Kopieret til projektkontraktkunder, når et tilbud er vundet, og tilbage igen til feltet Faktureres til kontraktnavn på den faktura, der er genereret for denne kunde. |
| Fakturering til navn | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Dette tekstfelt bruges til at identificere fakturakontaktpersonen for denne kunde. | Kopieret til projektkontraktkunderne, når et tilbud er vundet, og tilbage igen til feltet **Faktureres til kontraktnavn** på den faktura, der er genereret for denne kunde. |
| Bet.betingelser | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Dette er en grupperet indstilling med værdier, der som standard er hentet fra den relaterede firmapost. | Kopieret til projektkontraktkunderne, når et tilbud er vundet, og tilbage igen til feltet **Faktureres til kontraktnavn** på den faktura, der er genereret for denne kunde. |
| Er afrunding | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Angiver, om denne kunde er en standard afrundingskunde for denne handel. | Kopieret til projektkontraktkunderne, når et tilbud er vundet. |
| Ejende virksomhed | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Den juridiske enhed, som denne kunde er konfigureret med i modulet **Projektstyring og regnskab**. Dette felt er skrivebeskyttet og er angivet til ejerselskabet i selve tilbuddet. Listen over kunder, der skal tilføjes i feltet **Firma**, er allerede filtreret til listen fra ejerselskabet i modulet **Projektstyring og regnskab** under Project Operations. | Ejerselskabet svarer til begrebet juridisk enhed i modulet **Projektstyring og regnskab** under Project Operations. Der redegøres for alle omkostninger og indtægter i forbindelse med dette projekt i finanskladden i ejerselskabet. |
| Grænse, der ikke må overskrides | Redigerbart gitter under fanen **Tilbudskunder** og formularerne **Primær** og **Hurtig oprettelse** for en tilbudskunde. | Indikerer, om der er en forhandlet grænse eller maksimum for det samlede beløb, der vil blive faktureret til denne kunde for denne aftale. | Kopieret til projektkontraktkunderne, når et tilbud er vundet. |

## <a name="editing-billing-split-percentages"></a>Redigering af opdelingen af faktureringsprocenter

Du kan redigere procenter for opdeling af fakturering ved hjælp af redigeringsoplevelsen på det indbyggede gitter. Når procentsatsen for faktureringsopdeling ikke samlet set udgør 100 %, opstår der en fejl. Når du har opdateret procenter for opdeling af fakturering, skal du opdatere siden for at fjerne fejlen.

Du kan også vælge **Fordel ligeligt** på tilbudskunders undergitter. Denne handling tildeler faktureringsopdelinger til alle tilbudskunder. Hvis der er en afrundingsfaktor, vil den blive tilføjet til den afrundede kunde. En af tilbudskunderne er altid mærket som den afrundede kunde. Dette betyder, at tilbudskundeposten har flaget for **Afrunding** angivet til **Ja**. Dette er som regel den primære kunde for tilbuddet, men det kan ændres.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
