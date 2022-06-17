---
title: Transaktionsoprindelse – Knyt faktiske værdier til deres kilde
description: I denne artikel forklares det, hvordan begrebet transaktionsoprindelse bruges til at knytte faktiske værdier til originale kildeposter, som f.eks. logfiler for tid, udgifter eller materialeforbrug.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921295"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Transaktionsoprindelse – Knyt faktiske værdier til deres kilde

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Transaktionsoprindelsesposter oprettes for at knytte faktiske værdier sammen med deres kilde, som f.eks. tidsposter, udgiftsposter, materialeforbrugslogfiler og projektfakturaer.

I følgende eksempel vises den typiske behandling af tidsregistreringer i et projekts livscyklus i Project Operations.

> ![Behandling af tidsregistreringer i Project Operations.](media/basic-guide-17.png)
 
1. Indsendelse af en tidsregistrering medfører, at der oprettes to kladdelinjer: en for omkostning og en for ikke-faktureret salg.
2. Eventuel godkendelse af en tidsregistrering medfører, at der oprettes to faktiske værdier: en for omkostning og en for ikke-faktureret salg.
3. Når brugeren opretter en projektfaktura, oprettes transaktionen for fakturalinjen ved hjælp af data fra det faktiske ikke-fakturerede salg.
4. Når fakturaen er bekræftet, oprettes to nye faktiske værdier: en tilbageførsel af ikke-faktureret salg og en faktisk faktureret salgsværdi.

Hver hændelse i denne behandlende arbejdsproces udløser oprettelsen af poster i objektet Transaktionsoprindelse for at hjælpe med at opbygge en sporing af relationerne mellem disse poster, der er oprettet på tværs af tidsregistrering, kladdelinje, faktiske værdier og fakturalinjedetaljer.

I følgende tabel vises posterne i objektet Transaktionsoprindelse for den foregående arbejdsproces.

| Hændelse                        | Oprindelse                   | Oprindelsestype                       | Transaktion                       | Transaktionstype         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Afsendelse af tidsregistrering        | Tidsregistreringspost-GUID   | Tidsregistrering                        | GUID for kladdelinjepost (omkostning)   | Kladdelinje             |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for kladdelinjepost (salg)  | Kladdelinje                      |                          |
| Tidsgodkendelse                | GUID for kladdelinjepost | Kladdelinje                      | GUID for ikke-faktureret salgspost        | Faktisk                   |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for ikke-faktureret salgspost        | Faktisk                            |                          |
| GUID for kladdelinjepost     | Kladdelinje             | GUID for faktisk omkostningspost           | Faktisk                            |                          |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for faktisk omkostningspost           | Faktisk                            |                          |
| Oprettelse af faktura             | Tidsregistreringspost-GUID   | Tidsregistrering                        | GUID for fakturalinjetransaktion     | Fakturalinjetransaktion |
| GUID for kladdelinjepost     | Kladdelinje             | GUID for fakturalinjetransaktion     | Fakturalinjetransaktion          |                          |
| Bekræftelse af faktura         | GUID for fakturalinje        | Fakturalinje                      | GUID for faktureret salgspost          | Faktisk                   |
| Faktura-GUID                 | Faktura                  | GUID for faktureret salgspost          | Faktisk                            |                          |
| GUID for fakturalinjedetalje     | Fakturalinjedetalje      | GUID for faktureret salgspost          | Faktisk                            |                          |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for faktureret salgspost          | Faktisk                            |                          |
| GUID for kladdelinjepost     | Kladdelinje             | GUID for faktureret salgspost          | Faktisk                            |                          |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for tilbageførsel af ikke-faktureret salg      | Faktisk                            |                          |
| GUID for kladdelinjepost     | Kladdelinje             | GUID for tilbageførsel af ikke-faktureret salg      | Faktisk                            |                          |
| Rettelse af kladdefaktura     | GUID for gammel fakturalinjetransaktion             | Fakturalinjetransaktion          | GUID for rettelse af fakturalinjetransaktion               | Fakturalinjetransaktion |
| GUID for gammel fakturalinje                  | Fakturalinje             | GUID for rettelse af fakturalinjetransaktion               | Fakturalinjetransaktion          |                          |
| GUID for gammel faktura             | Faktura                  | GUID for rettelse af fakturalinjetransaktion               | Fakturalinjetransaktion          |                          |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for rettelse af fakturalinjetransaktion               | Fakturalinjetransaktion          |                          |
| GUID for kladdelinjepost     | Kladdelinje             | GUID for rettelse af fakturalinjetransaktion               | Fakturalinjetransaktion          |                          |
| Rettelse af bekræftet faktura | GUID for gammel fakturalinjetransaktion             | Fakturalinjetransaktion          | GUID for tilbageført faktisk faktureret salg | Faktisk                   |
| GUID for gammel fakturalinje                  | Fakturalinje             | GUID for tilbageført faktisk faktureret salg | Faktisk                            |                          |
| GUID for gammel faktura             | Faktura                  | GUID for tilbageført faktisk faktureret salg | Faktisk                            |                          |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for tilbageført faktisk faktureret salg | Faktisk                            |                          |
| GUID for kladdelinjepost     | Kladdelinje             | GUID for tilbageført faktisk faktureret salg | Faktisk                            |                          |
| GUID for gammel fakturalinjetransaktion                 | Fakturalinjetransaktion | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |
| GUID for gammel fakturalinje                  | Fakturalinje             | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |
| GUID for gammel faktura             | Faktura                  | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |
| Tidsregistreringspost-GUID       | Tidsregistrering               | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |
| GUID for kladdelinjepost     | Kladdelinje             | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |
| GUID for rettelse af fakturalinjetransaktion          | Fakturalinjetransaktion | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |
| GUID for rettelse af fakturalinje           | Fakturalinje             | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |
| GUID for rettelse af faktura      | Faktura                  | GUID for nyt faktisk ikke-faktureret salg    | Faktisk                            |                          |


I følgende illustration vises de links, der oprettes mellem faktiske værdier og deres kilder ved forskellige hændelser ved hjælp af eksemplet med tidsposter i Project Operations.

> ![Hvordan knyttes de faktiske værdier sammen med kildeposter i Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
