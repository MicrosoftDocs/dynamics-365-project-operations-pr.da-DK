---
title: Forretningstransaktioner
description: Dette emne indeholder oplysninger om forretningstransaktioner.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a8506effc453280177d74f94dcf9310e310c098
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149896"
---
# <a name="business-transactions"></a>Forretningstransaktioner

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Dynamics 365 Project Service Automation er *forretningstransaktion* et abstrakt begreb, der ikke repræsenteres af et objekt. Men nogle almindelige felter og processer på objekter er designet til at bruge konceptet forretningstransaktioner. Følgende objekter bruger dette begreb:

- Tilbudslinjedetaljer
- Kontraktlinjedetaljer
- Estimatlinjer
- Kladdelinjer
- Faktiske

Blandt disse objekter bliver tilbudslinjedetaljer, kontraktlinjedetaljer og estimatlinjer knyttet til estimatfasen i projektets livscyklus. Objekterne Kladdelinjer og Faktiske knyttes til udførelsesfasen i projektets livscyklus.

I PSA behandles poster i disse fem objekter som forretningstransaktioner. Den eneste forskel er, at poster i objekter, der er knyttet til estimatfasen, betragtes som økonomiske prognoser, mens poster i objekter, der er knyttet til udførelsesfasen, betragtes som økonomiske fakta, der allerede er indtruffet.

Der er flere oplysninger under [Estimater](estimates.md) og [Faktiske](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepter, der er entydige for forretningstransaktioner
Følgende koncepter er unikke for konceptet med forretningstransaktioner:

- Transaktionstype
- Transaktionsklasse
- Transaktionsoprindelse
- Transaktionsforbindelse

### <a name="transaction-type"></a>Transaktionstype

Transaktionstype repræsenterer timingen og konteksten af den økonomiske indvirkning på et projekt. Den repræsenteres af en grupperet indstilling, der har følgende understøttede værdier i PSA:
- Omkostning
- Projektkontrakt
- Ikke-faktureret salg
- Faktureret salg
- Organisationsinternt salg
- Ressourceenhedsomkostning

### <a name="transaction-class"></a>Transaktionsklasse

Transaktionsklasse repræsenterer de forskellige typer af omkostninger, der opstår på projekter. Den repræsenteres af en grupperet indstilling, der har følgende understøttede værdier i PSA:

- Tidspunkt
- Udgift
- Materiale
- Gebyr
- Milepæl
- Moms

Værdien af **Milepæl** bruges typisk af forretningslogikken til fastprisfakturering i PSA.

### <a name="transaction-origin"></a>Transaktionsoprindelse

Transaktionsoprindelse er et objekt, som lagrer de enkelte forretningstransaktioners oprindelse. Efterhånden som projekters udførelser bliver igangsat, foranlediger hver forretningstransaktion en anden forretningstransaktion, som herefter opretter en ny osv. Objektet transaktionsoprindelse blev udviklet til at lagre data om de enkelte transaktioner for at bidrage til rapportering og sporbarhed. 

### <a name="transaction-connection"></a>Transaktionsforbindelse

Transaktionsforbindelse er et objekt, der lagrer relationen mellem to lignende forretningstransaktioner, f.eks. omkostninger og relaterede faktiske salgsværdier eller tilbageførsler, der udløses af faktureringsaktiviteter, f.eks. fakturabekræftelse eller fakturakorrektioner.

Tilsammen hjælper Transaktionsoprindelse og Transaktionsforbindelse dig med at spore relationer mellem forretningstransaktioner og handlinger, der har medført oprettelse af en bestemt forretningstransaktion.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Eksempel: Sådan fungerer Transaktionsoprindelse sammen med Transaktionsforbindelse

I følgende eksempel vises den typiske behandling af Transaktionsoprindelse i en PSA-projektlivscyklus.

> ![Behandling af tidsregistreringer i en Project Service-livscyklus](media/basic-guide-17.png)
 
1. Afsendelse af en tidsregistrering medfører, at der oprettes to kladdelinjer: den ene for omkostning og den anden for ikke-faktureret salg.
2. Eventuel godkendelse af en tidsregistrering medfører, at der oprettes to faktiske værdier: den ene for omkostning og den anden for ikke-faktureret salg.
3. Når brugeren opretter en projektfaktura, oprettes transaktionen for fakturalinjen ved hjælp af data fra det faktiske ikke-fakturerede salg. 
4. Når fakturaen er bekræftet, oprettes to nye faktiske værdier: en tilbageførsel af ikke-faktureret salg og en faktisk faktureret salgsværdi.

Hver af disse hændelser udløser oprettelsen af poster i objekterne Transaktionsoprindelse og Transaktionsforbindelse for at hjælpe med at opbygge en sporing af relationer mellem disse poster, der er oprettet på tværs af tidsregistrering, kladdelinje, faktiske værdier og fakturalinjedetaljer.

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

I følgende tabel vises posterne i objektet Transaktionsforbindelse for den foregående arbejdsproces.

| Hændelse                          | Transaktion 1                 | Rolle for transaktion 1 | Type for transaktion 1           | Transaktion 2                | Rolle for transaktion 2 | Type for transaktion 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Afsendelse af tidsregistrering          | GUID for kladdelinje (salg)     | Ikke-faktureret salg     | msdyn_journalline            | GUID for kladdelinje (omkostning)     | Omkostning               | msdyn_journalline  |
| Tidsgodkendelse                  | GUID for faktisk ikke-faktureret (salg)  | Ikke-faktureret salg     | msdyn_actual                 | GUID for faktiske omkostninger (omkostning)       | Omkostning               | msdyn_actual       |
| Oprettelse af faktura               | GUID for fakturalinjedetalje      | Faktureret salg       | msdyn_invoicelinetransaction | GUID for faktisk ikke-faktureret salg   | Ikke-faktureret salg     | msdyn_actual       |
| Bekræftelse af faktura           | GUID for tilbageførsel af faktiske data         | Tilbageførsel          | msdyn_actual                 | GUID for oprindeligt ikke-faktureret salg | Oprindelig           | msdyn_actual       |
| GUID for faktureret salg              | Faktureret salg                  | msdyn_actual       | GUID for faktisk ikke-faktureret salg   | Ikke-faktureret salg               | msdyn_actual       |                    |
| Rettelse af kladdefaktura       | GUID for fakturalinjetransaktion | Erstatning          | msdyn_invoicelinetransaction | GUID for faktureret salg            | Oprindelig           | msdyn_actual       |
| Bekræft rettelse af faktura     | GUID for tilbageførsel af faktureret salg    | Tilbageførsel          | msdyn_actual                 | GUID for faktureret salg            | Oprindelig           | msdyn_actual       |
| GUID for nyt faktisk ikke-faktureret salg | Erstatning                     | msdyn_actual       | GUID for faktureret salg            | Oprindelig                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]