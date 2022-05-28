---
title: Administrer flere kunder i projektkontrakter
description: Dette emne indeholder oplysninger om, hvordan du administerer flere kunder på en projektkontrakt.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bf8b0d313b2b07924d730fe8923b05559bbcc244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591305"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Administrer flere kunder i projektkontrakter

Dette emne indeholder oplysninger om, hvordan du administerer flere kunder på en projektkontrakt. Du kan bruge en projektkontrakt, når der er behov for en kontraktaftale for flere kunder i forbindelse med finansiering af en handel. På siden **Projektkontrakt** indeholder fanen **Oversigt** oplysninger om den primære kunde for en handel. Andre kunder, der deltager i handlen, kan tilføjes til fanen **Kunder**.

Alle kontraktkunder på fanen **Kunder** i projektkontrakten er som standard kontraktlinjekunder i alle nye projektbaserede kontraktlinjer, der oprettes for projektkontrakten. Eventuelle eksisterende projektbaserede kontraktlinjer arver ikke nye kontraktkundeposter, som oprettes senere.

Du kan altid tilføje, opdatere eller slette kontraktkunder og kontraktlinjekunder, før kontrakten er vundet. En kunde i projektkontrakten skal konfigureres som en kunde i den ejende virksomhed eller juridiske enhed på siden **Kunder**. Juridiske enheder konfigureres i modulet **Projektstyring og regnskab** i Dynamics 365 Project Operations og er tilgængelige som virksomheder i modulerne **Projektsalg** og **Levering** i Project Operations.

## <a name="primary-customers"></a>Primære kunder

Den potentielle kunde, der vises under fanen **Oversigt** i projektkontrakten, er den primære kunde i kontrakten. Du kan ikke opdatere den primære kunde fra listen med kontraktkunder. Hvis du forsøger at slette den primære kunde fra en kundeliste på kontrakten, opstår der en fejl, som siger, at en primær kundepost i en kontrakt ikke kan slettes. Du kan i stedet ændre kunden i feltet **Potentiel kunde** under fanen **Oversigt** i projektkontrakten. Når du opdaterer dette felt, tilføjes den nyligt valgte kunde som en ny kontraktkunde med flaget **Primær** angivet til **Ja**. Den forrige primære kunde er stadig kunde i kontrakten, men er ikke længere den primære kunde.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Opret, opdater eller slet en kontraktkundepost

Du kan oprette, opdatere eller slette en kontraktkunde via fanen **Kontraktkunder** på siden **Kontrakt**. Der findes følgende felter i en projektkontrakts kontraktkundepost.

| **Felt** | **Placering** | **Beskrivelse** | 
| --- | --- | --- | 
| Konto | Redigerbart gitter på fanen **Kontraktkunder** og de primære sider og sider til hurtig oprettelse af en kontraktkunde. | Viser alle aktive firmaer. Dette felt er låst, når posten er oprettet. Hvis du vil opdatere posten, skal du slette den og derefter oprette den på ny. Hvis du har registreret faktiske værdier, eller hvis kontraktkundeposten er en primær kunde, kan du ikke slette posten. Kontraktkunder kopieres over som kontraktlinjekunder, når der oprettes en kontraktlinje. |
| Procentdel for faktureringsopdeling | Redigerbart gitter på fanen **Kontraktkunder** og de primære sider og sider til hurtig oprettelse af en kontraktkunde. | Viser procentdelen af hver ikke-faktureret salgstransaktion, som tildeles kontraktkunden. Når der oprettes nye projektkontraktlinjer, kopieres faktureringsopdelingsprocenten til eventuelle nye kontraktlinjer, der oprettes, og til projektkontraktlinjekunder. |
| Faktura til Kontaktnavn | Redigerbart gitter på fanen **Kontraktkunder** og de primære sider og sider til hurtig oprettelse af en kontraktkunde. | Dette tekstfelt bør bruges til at identificere fakturaens kontaktperson for kunden. Standardværdierne stammer fra den relaterede firmapost. Kontraktnavnet kopieres over til **Faktureres til kontraktnavn** på den faktura, der genereres for kunden. |
| Faktureringsnavn | Redigerbart gitter på fanen **Kontraktkunder** og de primære sider og sider til hurtig oprettelse af en kontraktkunde. | Brug dette tekstfelt til at identificere fakturaens kontaktperson for kunden. Standardværdierne stammer fra den relaterede firmapost. Navnet kopieres over til feltet **Faktureres til kontraktnavn** på den faktura, der genereres for kunden. |
| Bet.betingelser | Redigerbart gitter på fanen **Kontraktkunder** og primære sider og sider til hurtig oprettelse af en kontraktkunde. | Standardværdierne stammer fra den relaterede firmapost. Begreberne kopieres over til **Faktureres til kontraktnavn** på den faktura, der genereres for kunden. |
| Ejende virksomhed | Redigerbart gitter på fanen **Projektkontraktkunder** og de primære sider og sider til hurtig oprettelse af en projektkontraktkunde. | Den juridiske enhed, som kunden er konfigureret i i modulet **Projektstyring og regnskab**. Dette felt er skrivebeskyttet og angives til det ejende firma i projektkontrakten.</br>Kundelisten, der skal tilføjes i feltet **Firma**, er allerede filtreret til listen fra ejerselskabet i modulet **Projektstyring og regnskab** under Project Operations. Den ejende virksomhed svarer til den juridiske enhed i modulet **Projektstyring og regnskab** i Project Operations. Der redegøres for alle omkostninger og indtægter afledt af projektet i finanskladden i den ejende virksomhed. |
| Er afrunding | Redigerbart gitter på fanen **Kontraktkunder** og de primære sider og sider til hurtig oprettelse af en kontraktkunde. | Angiver, om kunden er en standardafrundingskunde for handlen. Der kan kun være én afrundingskunde i en projektkontrakt. Når omkostninger og ikke-fakturerede salg opdeles på antallet og fører til en afrundingsdifference, gælder denne forskel for den faktiske værdi, der er knyttet til kunden. |
| Grænse, der ikke må overskrides | Redigerbart gitter på fanen **Kontraktkunder** og de primære sider og sider til hurtig oprettelse af en kontraktkunde. | Angiver, om der er en forhandlet grænse eller loft for det samlede beløb, der faktureres denne kunde for aftalen. Den grænse, der ikke må overskrides som er konfigureret på kontraktkundeniveau, evalueres på grundlag af ikke-fakturerede faktiske salgsværdier, som refererer til kontraktkunden. |

## <a name="edit-billing-split-percentages"></a>Rediger opdelingen af faktureringsprocenter

Du kan redigere faktureringsopdelingsprocenter i gitteret. Når faktureringsopdelingsprocenter ikke udgør 100 procent i alt, opstår der fejl. Når du har redigeret en faktureringsopdelingsprocent, skal du opdatere siden **Projektkontrakt** for at fjerne fejlen.

Du kan også vælge **Fordel ligeligt** på undergitteret for projektkontraktkunder. Faktureringsopdelinger fordeles ligeligt til alle kunderne i projektkontrakten. Hvis der er en afrundingsfaktor, vil faktoren blive føjet til den afrundede kunde. En af kkontraktkunderne har altid flaget for **Afrunding** angivet til **Ja**. Kunden er den afrundede kunde. Den afrundingskunde er som regel også den primære kunde i kontrakten, men det er ikke et krav.


[!INCLUDE[footer-include](../includes/footer-banner.md)]