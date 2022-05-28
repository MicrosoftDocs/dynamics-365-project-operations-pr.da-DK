---
title: Transaktionsforbindelser – Sammenkæd de faktiske værdier for forskellige transaktionstyper
description: I dette emne forklares det, hvordan en transaktionsforbindelse bruges til at sammenkæde faktiske værdier af forskellige typer for at spore på rentabilitet, faktureringsbeholdning og fakturerede versus ikke-fakturerede omsætningsberegninger.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580771"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transaktionsforbindelser – Sammenkæd de faktiske værdier for forskellige transaktionstyper

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Transaktionsforbindelsesposter oprettes for at knytte faktiske værdier af forskellige typer, efterhånden som tid, udgifter eller materialeforbrug bevæger sig i livscyklussen fra tilbuddet eller førsalgsfasen til kontraktfasen, godkendelser og/eller tilbagekaldelser, fakturering og potentielt kreditering eller korrigerende fakturering.

I følgende eksempel vises den typiske behandling af tidsregistreringer i et projekts livscyklus i Project Operations.

> ![Behandling af tidsregistreringer i Project Operations.](media/basic-guide-17.png)

Behandlingen af tidsregistreringer i et Project Operations-projekts livscyklus følger disse trin: 

1. Indsendelse af en tidsregistrering medfører, at der oprettes to kladdelinjer: en for omkostning og en for ikke-faktureret salg. 
2. Eventuel godkendelse af en tidsregistrering medfører, at der oprettes to faktiske værdier: en for omkostning og en for ikke-faktureret salg. Disse to faktiske værdier sammenkædes ved hjælp af transaktionsforbindelser.
3. Når brugeren opretter en projektfaktura, oprettes transaktionen for fakturalinjen ved hjælp af data fra det faktiske ikke-fakturerede salg.
4. Når fakturaen er bekræftet, oprettes to nye faktiske værdier: en tilbageførsel af ikke-faktureret salg og en faktisk faktureret salgsværdi. Tilbageførelsen af det ikke-fakturerede salg og det oprindelige ikke-fakturerede faktiske salg sammenkædes ved hjælp af omvendte transaktionsforbindelser. De faktiske fakturerede salgsværdier og de oprindelige ikke-fakturerede salgsværdier er også forbundet for at vise forbindelserne mellem omsætningen for det, der engang var efterslæb eller igangværende arbejde, med den nu fakturerede omsætning.   

Hver hændelse i behandlingsarbejdsprocessen udløser oprettelsen af poster i tabellen **Transaktionsforbindelser**. Dette er med til at oprette en sporing af relationer mellem de poster, der er oprettet på tværs af tidsregistrering, kladdelinjer, faktiske værdier og fakturalinjedetaljer.

I følgende tabel vises posterne i objektet **Transaktionsforbindelse** for den foregående arbejdsproces.

|Hændelse                   |Transaktion 1                 |Rolle for transaktion 1 |Type for transaktion 1       |Transaktion 2          |Rolle for transaktion 2 |Type for transaktion 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Afsendelse af tidsregistrering   |GUID for kladdelinje (salg)     |Ikke-faktureret salg |msdyn_journalline            |GUID for kladdelinje (omkostning)     |Omkostning            |msdyn_journalline  |
|Tidsgodkendelse           |GUID for faktisk ikke-faktureret (salg)  |Ikke-faktureret salg |msdyn_actual                 |GUID for faktiske omkostninger (omkostning)       |Omkostning            |msdyn_actual       |
|Oprettelse af faktura        |GUID for fakturalinjedetalje      |Faktureret salg   |msdyn_invoicelinetransaction |GUID for faktisk ikke-faktureret salg   |Ikke-faktureret salg  |msdyn_actual       |
|Bekræftelse af faktura    |GUID for tilbageførsel af faktiske data         |Tilbageførsel      |msdyn_actual                 |GUID for oprindeligt ikke-faktureret salg |Oprindelig        |msdyn_actual       |
|                        |GUID for faktureret salg             |Faktureret salg   |msdyn_actual                 |GUID for faktisk ikke-faktureret salg   |Ikke-faktureret salg  |msdyn_actual       |
|Rettelse af kladdefaktura |GUID for fakturalinjetransaktion|Erstatning      |msdyn_invoicelinetransaction |GUID for faktureret salg            |Oprindelig        |msdyn_actual       |
|Bekræft rettelse af faktura|GUID for tilbageførsel af faktureret salg  |Tilbageførsel      |msdyn_actual                 |GUID for faktureret salg            |Oprindelig        |msdyn_actual       |
|                        |Nyt ikke-faktureret salgs-GUID |Erstatning            |msdyn_actual                 |GUID for faktureret salg            |Oprindelig        |msdyn_actual       |


I følgende illustration vises de links, der oprettes mellem forskellige typer faktiske værdier ved forskellige hændelser ved hjælp af eksemplet med tidsposter i Project Operations.

> ![Hvordan knyttes de faktiske værdier for forskellige typer sammen med hinanden i Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
