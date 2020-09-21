---
title: Startside med dimensioner for prisfastsættelse og efterkalkulation
description: Dette emne indeholder en oversigt over prisdimensioner.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750526"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Startside med dimensioner for prisfastsættelse og efterkalkulation

De dimensioner, der bruges i de menneskelige ressourcer til at konfigurere priser og omkostninger, falder i to kategorier:

- Personer
- Planlagt arbejde

Derfor findes der to typer dimensionsværdier for prisfastsættelse i PSA (Project Service Automation): 

- **Grupperede indstillinger** – Indstillinger, der er fasttekster for et værdisæt.
- **Objektbaserede værdier** – Dimensioner, der kan være et varieret sæt værdier.

## <a name="pricing-dimensions"></a>Prisdimensioner

PSA-leverancer med et standardsæt af prisdimensioner. Du kan få vist disse ved at gå til **Project Service** > **Parametre**. I parameterposten på fanen **Beløbsbaserede prisdimensioner** skal du kontrollere, at rollen **msdyn_resourcecategory** og ressourceafdelingen, **msdyn_organizationalunit** har felterne **Gælder for Salg** og **Gælder for Omkostning** angivet til **Ja**. Det giver dig mulighed for at konfigurere prisen og omkostningerne for de enkelte kombinationer af rolle og afdeling.

![Skærmbillede af Project Service-parametre, hvor "Gælder for Salg" er markeret](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Hvis du har brugt standardfelterne for både rolle og afdeling som prisdimensioner før version 3 af PSA, er der ingen bemærkelsesværdige ændringer. Du kan fortsætte med at bruge Project Service, som du plejer. 

Hvis du har brug for at fastsætte priser eller omkostninger for dine ressourcer ved hjælp af ekstra attributter, kan du oprette brugerdefinerede felter, objekter og dimensioner. Du kan finde flere oplysninger i følgende emner, men vær opmærksom på, at du skal udføre procedurerne i den rækkefølge, der er angivet nedenfor:

- [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities.md)
- [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](field-references.md)
- [Konfigurere brugerdefinerede felter som prisfastsættelsesdimensioner](set-up-pricing-dimensions.md)
- [Opdatere plug-in-attributter, så de indeholder nye prisfastsættelsesdimensioner](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Prisfastsættelse af HR-tid
Hvordan en organisation prisfastsætter HR-tid er ofte en vigtig strategisk overvejelse, der direkte påvirker organisationens rentabilitet. Arbejd sammen med økonomiteamene og praksischeferne, når organisationen er klar til at identificere, hvordan man vil konfigurere fakturerings- og omkostningssatser for HR-tid.

Andre overvejelser i forbindelse med prisfastsættelse omfatter, om du vil genbruge felter eller objekter, der ikke i øjeblikket er prisdimensioner, men gælder som en prisdimension for organisationen. Felter som **Transaktionskategori** (**msdyn_transactioncategory**) og **Reserverbar ressource** (**bookableresource**) er eksempler på kandidatdimensioner. 

Du skal også overveje, om prisdimensionen skal være en tabel eller en grupperet indstilling. Hvis du forventer ændringer af værdierne i en dimension, som vil overstige 10 eller 12, og du har brug for flere attributter til disse værdier, kan du oprette et objekt i stedet for en grupperet indstilling. Hvis du vedligeholder en grupperet indstilling, f.eks. tilføjelse eller fjernelse af værdier, kræves en administrator eller udvikler, og det er derfor muligt for de fleste brugere at tilføje nye rækker i en tabel.

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
