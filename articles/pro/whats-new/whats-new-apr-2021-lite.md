---
title: Nyheder april 2021 – Project Operations lille udrulning
description: Dette emne giver oplysninger om kvaliteten af de opdateringer, der er tilgængelige i april 2021-udgivelsen af Project Operations lille udrulning.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009389"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Nyheder april 2021 – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

  - Project Operations på Dataverse-miljø version 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

Følgende funktioner er omfattet af denne udgivelse:

- Ikke-lagerbaserede materialer til projekter. Nøglefunktionerne omfatter:
  - Estimering og prisfastsættelse af ikke-lagerførte materialer under et projekts salgscyklus. Du kan finde flere oplysninger i [Konfiguration af omkostnings- og salgssatser for katalogprodukter - lille](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sporing af brugen af ikke-lagerførte materialer under projektlevering. Du kan finde flere oplysninger i [Registrér materialeforbrug på projekter og projektopgaver](../../material/material-usage-log.md).
  - Fakturering af anvendte ikke-lagerførte materialeomkostninger. Du kan finde flere oplysninger under [Administrer faktureringsefterslæbet - lille](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Nye API'er i Dynamics 365 Dataverse gør det muligt at oprette, opdatere og slette handlinger med **Planlægningsobjekter**. Du kan finde flere oplysninger under [Brug planlægnings-API'er til at udføre handlinger med planlægningsobjekter](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kvalitetsopdateringer

| **Funktionsområde** | **Referencenummer** | **Kvalitetsopdatering** |
| --- | --- | --- |
| Fakturering og prisfastsættelse | 2224568 | Logik tilføjet for at aktivere tilpasninger, der indebærer aktivering af plug-in'et til bekræftelse af faktura. |
| Fakturering og prisfastsættelse | 2101098 | Logikken i standardfelterne på en proformafaktura er blevet forbedret: **Faktureringsadresse**, **Fakturamodtagers navn** og **Betalingsbetingelser** bruges nu som standard fra den tilsvarende kundepost i projektkontrakten. |
| Fakturering og prisfastsættelse | 2021413 | Du kan opdatere felterne **Faktiske omkostninger** og **Salg** i objektet **Opgave**, så de inkluderer salgsværdier fra ikke-fakturerede og fakturerede udgifter på opgaver. |
| Fakturering og prisfastsættelse | 2182110 | Når du kopierer en projektkontrakt, gendannes kontraktlinje-id'et i destinationsprojektkontrakten for at sikre, at det er entydigt. |
| Styring af salgsmuligheder | 2186741 | Valideringer tilføjet for at sikre, at feltet **Oprindelse** og **Transaktionstype** ikke opdateres på eksisterende tilbudslinjedetaljer. |
| Styring af salgsmuligheder | 2191353 | Der må ikke oprettes milepæle på en tids- og materialekontraktlinje. |
| Styring af salgsmuligheder | 2216956 | Løst problemer med **Opdatér priser**. |
| Planlægning og sporing | 2182979 | Funktionen projektkopiering er forbedret for at sikre, at omkostningsestimatlinjer kopieres fra det oprindelige projekt. |
| Planlægning og sporing | 2184144 | Funktionen projektkopiering er forbedret for at sikre, at ressourcepositionsnavnet kopieres fra det oprindelige projekt. |
| Planlægning og sporing | 2184799 | Projektkopi: Strengere kontrol for at sikre, at den anslåede startdato ikke ændres, mens kopieringen er i gang. |
| Planlægning og sporing | 2185134 | Projektkopi: Den anslåede startdato for destinationsprojektet angives til dags dato. |
| Planlægning og sporing | 2196373 | Projektkopi: Sikrer, at projektleder- og teammedlemsposter ikke duplikeres i projektteamet. |
| Planlægning og sporing | 2211833 | Projektkopi: Ressourcetildelinger kopieres fra kildeprojektopgaven til destinationsprojektet. |
| Planlægning og sporing | 2186541 | Løste problemer i gitteret **Estimater**, når der grupperes efter ressource. |
| Planlægning og sporing | 2166906 | Transaktionskategorien fra en opgave skal kopieres til objektet **Ressourcetildeling**. |
| Ressourcestyring | 2125362 | Løste problemer med oprettelse af et generisk teammedlem ved hjælp af en timebaseret allokeringsmetode. |
| Tid og udgift | 2113603 | Løste det tilpasningsrelaterede problem med at fjerne attributter fra siden **Tidsregistrering**. Systemet kontrollerer nu, om attributten findes på siden, inden disse tilgås ved hjælp af et script. |
| Tid og udgift | 2204377 | Kopierede timesedler skal vises automatisk, når du vælger **Kopiér uge** i forbindelse med tidsregistrering. |
| Tid og udgift | 2209059 | Feltet **Status** kan redigeres med henblik på tidsregistrering i Dynamics 365 Field Service. |
