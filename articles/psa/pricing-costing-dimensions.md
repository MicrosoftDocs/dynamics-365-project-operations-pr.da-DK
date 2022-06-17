---
title: Startside med dimensioner for prisfastsættelse og efterkalkulation
description: Denne artikel indeholder en oversigt over prisfastsættelsesdimensioner.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 88c77d90bccaa5f10e8f75d60ae121d699bc0976
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925435"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Startside med dimensioner for prisfastsættelse og efterkalkulation

[!include [banner](../includes/psa-now-project-operations.md)]

De dimensioner, der bruges til at angive prisfastsættelsen af arbejdskraft og omkostninger i projektbaserede organisationer, påvirkes af følgende attributter:

- Personer, der arbejder med opgaver svarende til deres erfaring, rolle eller geografi
- Arbejde, der skal udføres på en måde, som svarer til dets kompleksitet eller tidspunkt på dagen

Som følge af disse attributters typiske karakteristika for arbejdet og de personer, der er nødvendige for at udføre arbejdet, findes der to typer prisfastsættelsesdimensionsværdier i Project Service Automation: 

- **Grupperede indstillinger**: - Attributter, der er fasttekster for et værdisæt.
- **Objektbaserede værdier** - Attributter, der kan have varierende værdisæt, som er begrænsede, men som kan ændres med tiden.

## <a name="pricing-dimensions"></a>Dimensioner for prisfastsættelse

PSA-leverancer med et standardsæt af prisdimensioner. Du kan få vist disse ved at gå til **Project Service** > **Parametre**. I parameterposten på fanen **Beløbsbaserede prisdimensioner** skal du kontrollere, at rollen **msdyn_resourcecategory** og ressourceafdelingen, **msdyn_organizationalunit** har felterne **Gælder for Salg** og **Gælder for Omkostning** angivet til **Ja**. Det giver dig mulighed for at konfigurere prisen og omkostningerne for de enkelte kombinationer af rolle og afdeling.

![Skærmbillede af Project Service-parametre, hvor "Gælder for Salg" er markeret.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Hvis du har brugt standardfelterne for både rolle og afdeling som prisdimensioner før version 3 af PSA, er der ingen bemærkelsesværdige ændringer. Du kan fortsætte med at bruge Project Service, som du plejer. 

Hvis du har brug for at fastsætte priser eller omkostninger for dine ressourcer ved hjælp af ekstra attributter, kan du oprette brugerdefinerede felter, objekter og dimensioner. Du kan finde flere oplysninger i følgende artikler, men vær opmærksom på, at du skal udføre procedurerne i den rækkefølge, der er angivet nedenfor:

- [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities.md)
- [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](field-references.md)
- [Konfigurer brugerdefinerede felter som prisfastsættelsesdimensioner ](set-up-pricing-dimensions.md)
- [Opdatere plug-in-attributter, så de indeholder nye prisfastsættelsesdimensioner](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Prisfastsættelse af HR-tid
Hvordan en organisation prisfastsætter HR-tid er ofte en vigtig strategisk overvejelse, der direkte påvirker organisationens rentabilitet. Arbejd sammen med økonomiteamene og praksischeferne, når organisationen er klar til at identificere, hvordan man vil konfigurere fakturerings- og omkostningssatser for HR-tid.

Andre overvejelser i forbindelse med prisfastsættelse omfatter, om du vil genbruge felter eller objekter, der ikke i øjeblikket er prisdimensioner, men gælder som en prisdimension for organisationen. Felter som **Transaktionskategori** (**msdyn_transactioncategory**) og **Reserverbar ressource** (**bookableresource**) er eksempler på kandidatdimensioner. 

Overvej, om din prisfastsættelsesdimension skal være en tabel eller en grupperet indstilling. Hvis du forventer at foretage ændringer af værdierne i en dimension, som vil overstige 10 eller 12, og du har brug for flere attributter til disse værdier, skal du oprette et objekt i stedet for en grupperet indstilling. Hvis du bevarer en grupperet indstilling, f.eks. tilføjelse eller fjernelse af værdier, kræver det en administrator eller udvikler, og det er derfor muligt for de fleste erhvervsbrugere at tilføje nye rækker i en tabel.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
