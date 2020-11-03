---
title: Fakturer et forskudshonorar eller et forskud
description: Dette emne indeholder oplysninger om, hvordan du fakturerer et forskudshonorar eller et forskud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ed3b71d5f0ac035403de9fa213f3f45d14038e0
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087865"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Fakturer et forskudshonorar eller et forskud

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dynamics 365 Project Operations understøtter kontrakter baseret på forskudshonorarer og engangsforskud. I en projektkontrakt kan du registrere en plan for forskudshonorarer eller engangsforskud. Selvom du angiver det på projektkontraktniveau, bliver et forskudshonorar eller et forskud dog ikke øjeblikkeligt tilgængelig for brug. Hvis du vil bruge et forskudshonorar eller et forskud på en faktura, der rent faktisk fakturerer kunden, skal forskudshonoraret eller forskuddet først være faktureret.

Fuldfør følgende trin for at fakturer et forskudshonorar eller et forskud.

1. Vælg **Salg** > **Fakturering** > **Forskudshonorarer og forskud**. 
2. På siden **Forskudshonorarer og forskud** skal du bruge filtret for at vælge det specifikke forskudshonorar eller forskud, der skal faktureres, og markere det som **Klar til fakturering**.
3. Opret en faktura enten manuelt fra listesiden med **Projektkontrakt** eller detaljesiden. Forskudshonoraret eller forskuddet vises på kladdefakturaen i sektionen **Forskudshonorarer og forskud** på siden **Faktura**.
4. Bekræft fakturaen. Dette vil gøre forskudshonoraret eller forskuddet tilgængelig til brug. Du kan kontrollere fakturaen på listesiden **Forskudshonorarer og forskud**. Det disponible beløb vises i gitteret for et faktureret forskudshonorar eller forskud.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Opret et forskudshonorar eller forskud fra fakturagitteret

Du kan oprette et forskudshonorar eller forskud direkte på en faktura.

1. På en kladdefaktura skal du i undergitteret **Forskudshonorarer og forskud** vælge **Nyt** for at oprette et nyt forskudshonorar eller forskud. 
2. Angiv de fornødne oplysninger på siden **Hurtig oprettelse** , og vælg derefter **Gem**. Forskudshonoraret eller forskuddet oprettes i den projektkontrakt, der er knyttet til fakturaen. Forskudshonoraret eller forskuddet markeres automatisk som **Klar til fakturering** og tilføjes derefter til undergitteret **Forskudshonorarer og forskud** på siden **Faktura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Afstem et faktureret forskudshonorar eller et forskud

Når et forskudshonorar eller forskud faktureres, kan de bruges eller afstemmes på en faktura med tid, udgifter, milepæle eller andre projektbaserede opkrævninger. Kunden får vist sit fakturabeløb, som er reduceret med det forskudshonorar eller forskud, der bruges på fakturaen.

På alle de fakturaer, der er genereret for en projektkontrakt, og som har fakturerede forskudshonorarer eller forskud, anvender Project Operations automatisk forskudshonoraret eller forskuddet på fakturaen.

Dette kan ses i gitteret **Anvendte forskudshonorarer og forskud** på siden **Faktura**. Følgende tabel indeholder oplysninger om felterne i gitteret **Anvendte forskudshonorarer og forskud** på siden **Projektfaktura**.

| Felt | Lokation | Relevans, formål og vejledning | Downstream-virkning |
| --- | --- | --- | --- |
| Beskrivelse | Gitteret **Anvendte forskudshonorarer og forskud** på siden **Projektfaktura** |Dette skrivebeskyttede felt indeholder en beskrivelse af det forskudshonorar eller forskud, der bruges på fakturaen. Denne værdi kan ikke ændres på fakturaen. Denne værdi kan opdateres i undergitteret på siden **Projektkontrakt**. | Dette felt kan vises for kunden på den udskrevne faktura for at angive, hvilket forskudshonorar eller forskud, der anvendes på fakturaen. |
| Leveret d. | Gitteret **Anvendte forskudshonorarer og forskud** på siden **Projektfaktura**  | Dette skrivebeskyttede felt indeholder fakturadatoen for det forskudshonorar eller forskud, der bruges på fakturaen. Denne værdi kan ikke ændres på fakturaen. Denne værdi kan opdateres i undergitteret på siden **Projektkontrakt**. | Dette felt kan vises for kunden på den udskrevne faktura for at angive datoen for, hvornår forskudshonoraret eller forskuddet første gang blev faktureret til kunden. |
| Beløb | Gitteret **Anvendte forskudshonorarer og forskud** på siden **Projektfaktura**  | Dette skrivebeskyttede felt indeholder beløbet for det forskudshonorar eller forskud, der bruges på fakturaen. Denne værdi kan ikke ændres på fakturaen. Denne værdi kan opdateres i undergitteret på siden **Projektkontrakt**. | Dette felt kan vises for kunden på den udskrevne faktura for at angive det oprindelige beløb for forskudshonoraret eller forskuddet, som blev betalt af kunden. |
| Anvendt beløb | Gitteret **Anvendte forskudshonorarer og forskud** på siden **Projektfaktura**  | Dette skrivebeskyttede felt indeholder den beregnede værdi, som opsummerer, hvor meget af forskudshonoraret eller forskuddet, der er blevet brugt. | Dette felt kan vises for kunden på den udskrevne faktura for at angive den del af forskudshonoraret eller forskuddet, der allerede er blevet brugt. |
| Samlet beløb | Gitteret **Anvendte forskudshonorarer og forskud** på siden **Projektfaktura**  | Dette redigerbare felt indeholder beløbet for det forskudshonorar eller forskud, der bruges på denne projektfaktura. Dette beløb kan ikke være højere, end det beløb, der er disponibelt i forskuddet. Systemet beregner automatisk dette som differencen mellem felterne **Beløb** og **Brugt beløb** i gitteret. Du kan reducere dette beløb for at bruge mindre end det, der er tilgængeligt, men du kan ikke forøge beløbet for at bruge mere end det, der er tilgængeligt. | Dette felt kan vises for kunden på den udskrevne faktura for at angive den del af forskudshonoraret eller forskuddet, der blev brugt på fakturaen. |
| Saldobeløb for forskudshonorar. | Gitteret **Anvendte forskudshonorarer og forskud** på siden **Projektfaktura**  | Dette skrivebeskyttede felt indeholder værdien for, hvor meget af forskudshonoraret eller forskuddet der er tilbage, når fakturaen er bekræftet. | Dette felt kan vises for kunden på den udskrevne faktura for at angive den del af forskudshonoraret eller forskuddet, der vil være tilbage, når fakturaen er bekræftet og betalt. |
