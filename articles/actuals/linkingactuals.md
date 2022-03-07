---
title: Knyt faktiske tal til oprindelige poster
description: I dette emne forklares det, hvordan du kan knytte faktiske poster til oprindelige poster, som f.eks. logfiler for tidsregistrering, udgiftsregistrering eller materialeforbrug.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991749"
---
# <a name="link-actuals-to-original-records"></a>Knyt faktiske tal til oprindelige poster

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


I Dynamics 365 Project Operations er en *forretningstransaktion* et abstrakt begreb, der ikke repræsenteres af et objekt. Men nogle almindelige felter og processer på objekter er designet til at bruge konceptet forretningstransaktioner. Følgende objekter bruger dette begreb:

- Tilbudslinjedetaljer
- Kontraktlinjedetaljer
- Estimatlinjer
- Kladdelinjer
- Faktiske

Blandt disse objekter bliver **Tilbudslinjedetaljer**, **Kontraktlinjedetaljer** og **Estimatlinjer** knyttet til estimatfasen i projektets livscyklus. Objekterne **Kladdelinjer** og **Faktiske tal** knyttes til udførelsesfasen i projektets livscyklus.

Project Operations genkender poster i disse fem objekter som forretningstransaktioner. Den eneste forskel er, at poster i de objekter, der er knyttet til estimatfasen, betragtes som økonomiske prognoser, mens poster i objekter, der er knyttet til udførelsesfasen, betragtes som økonomiske fakta, der allerede er indtruffet.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepter, der er entydige for forretningstransaktioner
Følgende koncepter er unikke for konceptet med forretningstransaktioner:

- Transaktionstype
- Transaktionsklasse
- Transaktionsoprindelse
- Transaktionsforbindelse

### <a name="transaction-type"></a>Transaktionstype

Transaktionstype repræsenterer timingen og konteksten af den økonomiske indvirkning på et projekt. Dette repræsenteres af en grupperet indstilling, som har følgende understøttede værdier i Project Operations:

  - Omkostning
  - Projektkontrakt
  - Ikke-faktureret salg
  - Faktureret salg
  - Organisationsinternt salg
  - Ressourceenhedsomkostning

### <a name="transaction-class"></a>Transaktionsklasse

Transaktionsklasse repræsenterer de forskellige typer af omkostninger, der opstår på projekter. Dette repræsenteres af en grupperet indstilling, som har følgende understøttede værdier i Project Operations:

  - Tid
  - Udgift
  - Materiale
  - Gebyr
  - Milepæl
  - Skat

**Milepæl** bruges typisk af forretningslogikken til fastprisfakturering i Project Operations.

### <a name="transaction-origin"></a>Transaktionsoprindelse

**Transaktionsoprindelse** er et objekt, som lagrer de enkelte forretningstransaktioners oprindelse. Efterhånden som et projekt udvikler sig, vil hver enkelt forretningstransaktion give anledning til endnu en forretningstransaktion, som igen vil oprette en anden og så videre. Transaktionsobjektets oprindelse er designet til at lagre data om hver enkelt transaktions oprindelse for at gøre det lettere at rapportere og spore dataene. 

### <a name="transaction-connection"></a>Transaktionsforbindelse

**Transaktionsforbindelse** er et objekt, der lagrer forholdet mellem to lignende forretningstransaktioner, som f.eks. omkostninger og relaterede faktiske salgsværdier, eller transaktionstilbageførsler, der udløses af faktureringsaktiviteter såsom faktureringsbekræftelser eller fakturakorrektioner.

Tilsammen hjælper **Transaktionsoprindelse** og **Transaktionsforbindelse** dig med at spore relationer mellem forretningstransaktioner og handlinger, der har resulteret i en bestemt forretningstransaktion.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Eksempel: Sådan fungerer Transaktionsoprindelse sammen med Transaktionsforbindelse

I følgende eksempel vises den typiske behandling af tidsregistreringer i et projekts livscyklus i Project Operations.

> ![Behandling af tidsregistreringer i en Project Service-livscyklus.](media/basic-guide-17.png)
 
1. Indsendelse af en tidsregistrering opretter to kladdelinjer: en linje for omkostninger og en linje for ikke-faktureret salg.
2. Eventuel godkendelse af tidsregistreringen opretter to faktiske værdier: en faktisk værdi omkostning og en faktisk værdi for ikke-faktureret salg.
3. Når der oprettes en ny projektfaktura, oprettes fakturalinjetransaktionen ved hjælp af data fra det faktiske ikke-fakturerede salg. 
4. Når fakturaen er bekræftet, oprettes to nye faktiske værdier: en tilbageførsel af ikke-faktureret faktisk salg og en faktureret faktisk salgsværdi.

Hver af disse hændelser opretter en post i objekterne **Transaktionsoprindelse** og **Transaktionsforbindelse**. Med disse nye poster kan du opbygge en oversigt over forhold mellem de poster, der er oprettet på tværs af tidsregistrering, kladdelinjer, faktiske tal og fakturalinjedetaljer.

I følgende tabel vises posterne i objektet **Transaktionsoprindelse** for arbejdsprocessen.

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

I følgende tabel vises posterne i objektet **Transaktionsforbindelse** for arbejdsprocessen.

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
