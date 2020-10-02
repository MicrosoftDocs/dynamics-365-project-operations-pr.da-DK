---
title: Oversigt over dimensioner for prisfastsættelse
description: Dette emne indeholder oplysninger om prisfastsættelsesdimensioner i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898209"
---
# <a name="pricing-dimensions-overview"></a>Oversigt over dimensioner for prisfastsættelse

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

De dimensioner, der bruges i de menneskelige ressourcer til at konfigurere priser og omkostninger, falder i to kategorier:

- Personer
- Planlagt arbejde

Derfor findes der to typer værdier for prisfastsættelsesdimensioner:

- **Grupperede indstillinger**: Dimensioner, der er fasttekster for et værdisæt.
- **Objektbaserede værdier**: Dimensioner, der kan være et varieret sæt værdier.

## <a name="pricing-dimensions"></a>Dimensioner for prisfastsættelse

Dynamics 365 Project Operations leveres med et standardsæt af prisfastsættelsesdimensioner. Du kan få vist disse prisfastsættelsesdimensioner ved at gå til **Project Operations** > **Parametre**. I parameterposten på fanen **Beløbsbaserede prisdimensioner** skal du kontrollere, at rollen **msdyn_resourcecategory** og ressourceafdelingen, **msdyn_organizationalunit** har felterne **Gælder for Salg** og **Gælder for Omkostning** angivet til **Ja**. Ved at aktivere disse felter får du mulighed for at konfigurere prisen og omkostningerne for de enkelte kombinationer af rolle og afdeling.

Hvis du har brug for at fastsætte priser eller omkostninger for dine ressourcer ved hjælp af ekstra attributter, kan du oprette brugerdefinerede felter, objekter og dimensioner.

## <a name="pricing-human-resource-time"></a>Prisfastsættelse af HR-tid
Hvordan en organisation prisfastsætter HR-tid er ofte en vigtig strategisk overvejelse, der direkte påvirker organisationens rentabilitet. Arbejd sammen med økonomiteamene og praksischeferne, når organisationen er klar til at identificere, hvordan man vil konfigurere fakturerings- og omkostningssatser for HR-tid.

Andre overvejelser i forbindelse med prisfastsættelse omfatter, om du vil genbruge felter eller objekter, der ikke i øjeblikket er prisdimensioner, men gælder som en prisdimension for organisationen. Felter som **Transaktionskategori** (**msdyn_transactioncategory**) og **Reserverbar ressource** (**bookableresource**) er eksempler på kandidatdimensioner. 

Overvej, om din prisfastsættelsesdimension skal være en tabel eller en grupperet indstilling. Hvis du forventer ændringer af værdierne i en dimension, som vil overstige 10 eller 12, og du har brug for flere attributter til disse værdier, kan du oprette et objekt i stedet for en grupperet indstilling. Hvis du vedligeholder en grupperet indstilling, f.eks. tilføjelse eller fjernelse af værdier, kræves en administrator eller udvikler, og det er derfor muligt for de fleste brugere at tilføje nye rækker i en tabel.

I følgende eksempel vises de fakturarater, der er konfigureret på baggrund af den rolle og den organisationsenhed, som ressourcen tilhører. Omkostningssatser er typisk baseret på medarbejderens lønområde og den afdeling, de er knyttet til. I dette eksempel vil tabellerne over faktura- og omkostningssatser se ud som følger:

**Eksempler på fakturasatser**

| Rolle        | Afdeling    |Enhed      |Pris      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Udvikler   | Contoso USA  |Hour | 200|USD     |
| Udvikler   | Contoso India |Hour|   112|USD     |


**Eksempel på omkostningssatser**

| Lønområde     | Afdeling    |Enhed      |Pris      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso USA  |Hour | 145|USD     |
| My company_Band2 | Contoso India |Hour|   67|USD     |
