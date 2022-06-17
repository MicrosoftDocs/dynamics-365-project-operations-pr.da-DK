---
title: Administrer flere kunder i projektkontrakter - lille
description: Denne artikel indeholder oplysninger om at administrere flere kunder på projektkontrakter.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17cd464bad81a01f5f334524a542104d6f25717b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917198"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Administrer flere kunder i projektkontrakter - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Projektkontrakter i Dynamics 365 Project Operations understøtter scenariet, hvor en kontraktaftale omfatter flere kunder, som finansierer en handel. Fanen **Oversigt** på siden **Projektkontrakt** indeholder feltet **Kunde**. I dette felt identificeres den primære kunde i handlen. Du kan oprette andre kunder i forbindelse med handlen under fanen **Kunder** på siden **Projektkontrakt**.

Alle kontraktkunder, der er angivet på projektkontrakten, er som standard kontraktlinjekunder i alle nye projektbaserede kontraktlinjer, der oprettes for projektkontrakten. Eksisterende projektbaserede kontraktlinjer arver ikke nye kontraktkunder, når der oprettes nye poster.

Produktbaserede kontraktlinjer knyttes automatisk til den primære kunde.

Det er muligt at tilføje, opdatere eller slette kontraktkunder og kontraktlinjer, før kontrakten er vundet.

## <a name="primary-customer"></a>Primær kunde

Kunden, der vises under fanen **Oversigt** i projektkontrakten som den potentielle kunde, er den primære kunde i kontrakten. Når du forsøger at slette den primære kunde fra kundelisten på kontrakten, modtager du en fejlmeddelelse om, at en primær kundepost i en kontrakt ikke kan slettes.

Den primære kunde kan ikke opdateres fra listen med kontraktkunder. Du kan i stedet ændre den potentielle kunde under fanen **Oversigt** i kontrakten. Når dette felt opdateres på siden **Kontraktoversigt**, tilføjes den nye kunde som en ny kontraktkunde ved at angive det **Primære** flag. Den forrige primære kunde vil stadig være kunde i kontrakten.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Opret, opdater eller slet en kontraktkundepost

Du kan oprette, opdatere eller slette en kontraktkunde under fanen **Kunder** på siden **Projektkontrakt**. Felterne i følgende tabel findes i en kontraktkundepost for en projektkontrakt og bør haves in mente, når du arbejder med kontrakten.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| **Firma** | Gitter kan redigeres på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Viser alle aktive firmaer. Dette felt er låst, når posten er oprettet. Hvis du vil opdatere kontoen, skal du slette posten og oprette den på ny. Hvis du har registreret faktiske værdier, eller hvis kontraktkundeposten er en primær kunde, kan du ikke slette posten. | Kontraktkunder kopieres over som kontraktlinjekunder, når der oprettes en kontraktlinje. |
| **Procentdel for faktureringsopdeling** | Gitter kan redigeres på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Viser procentdelen af hver ikke-faktureret salgstransaktion, der tildeles denne kontraktkunde. | Kopieret til nye kontraktlinjer og til projektkontraktlinjekunder på nye projektkontraktlinjer. |
| **Faktura til Kontaktnavn** | Gitter kan redigeres på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Dette tekstfelt bruges til at identificere fakturakontaktpersonen for denne kunde. Dette felt angives som standard på grundlag af den relaterede firmapost. | Kopieres over til feltet **Faktureres til kontraktnavn** på den faktura, der genereres for denne kunde. |
| **Faktureringsnavn** | Gitteret kan redigeres på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde | Dette tekstfelt bruges til at identificere fakturakontaktpersonen for denne kunde. Dette felt angives som standard på grundlag af den relaterede firmapost. | Kopieres over til feltet **Faktureres til kontraktnavn** på den faktura, der genereres for denne kunde. |
| **Betalingsbetingelser** | Gitter kan redigeres på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Værdierne angives som standard på grundlag af den relaterede firmapost. | Kopieres over til feltet **Faktureres til kontraktnavn** på den faktura, der genereres for denne kunde. |
| **Er afrunding** | Gitter kan redigeres på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde. | Angiver, om denne kunde er en standard afrundingskunde for denne handel. Der kan kun være én afrundingskunde i en projektkontrakt. | Når omkostninger og ikke-fakturerede salg opdeles på antallet af potentielle kunder til en afrundingsdifference, gælder denne forskel for den faktiske værdi, der er knyttet til denne kunde. |
| **Grænse, der ikke må overskrides** | Gitteret kan redigeres på fanen **Kontraktkunder** og de **Primære** formularer samt formularer til **Hurtig oprettelse** for en kontraktlinjekunde | Angiver, om der er en forhandlet grænse eller loft for det samlede beløb, der faktureres denne kunde for denne aftale. | Den **Grænse, der ikke må overskrides** som konfigureres på kontraktkundeniveau, evalueres på **Ikke-fakturerede faktiske salgsværdier**, som refererer til denne kontraktkunde. |

## <a name="edit-billing-split-percentages"></a>Rediger opdelingen af faktureringsprocenter

Faktureringsopdelingsprocenter kan redigeres ved hjælp af oplevelsen med direkte redigering af gitteret. Når faktureringsopdelingsprocenterne ikke udgør 100 procent i alt, modtager du en fejlmeddelelse. Når du har redigeret faktureringsopdelingsprocenterne, skal du opdatere siden for at afvise fejlen.

Du kan også vælge **Ligelig fordeling** i undergitteret **Kontraktkunder** for at allokere faktureringsopdelingen ligeligt for alle kontraktkunder. Hvis der er en afrundingsfaktor, vil den blive føjet til den afrundede kunde. En af kontraktkunderne er altid mærket som en **afrundings**-kunde, hvilket betyder, at afrundingsflaget er angivet til **Ja** for den pågældende kontraktkundepost. Det er som regel den primære kunde i kontrakten, men dette kan også ændres.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]