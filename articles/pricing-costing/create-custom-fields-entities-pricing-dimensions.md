---
title: Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse
description: Dette emne indeholder oplysninger om, hvordan du kan oprette brugerdefinerede grupperede indstillinger eller objekter.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 40a6a4173cb0e4d7ea5bcf24c8954fe9d7e079d1e9ecf4aac252b5133f12d3ff
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003629"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt som en prisfastsættelsesdimension. Se [Oversigt over prisfastsættelsesdimensioner](pricing-dimensions-overview.md) for at få flere oplysninger.  

> [!IMPORTANT]
> Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning. Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov. Den vil også hjælpe til med at genbruge dit arbejde og gøre det nemmere at koble disse ændringer sammen med en anden forekomst. Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som **Administreret løsning** og importere den på andre forekomster for at genbruge din prisfastsættelsesopsætning.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen

En prisdimension kan være en grupperet indstilling eller et objekt. Begge skal være oprettet i din prissætningsløsning. I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.

### <a name="entity-based-dimensions"></a>Objektbaserede dimensioner
Benyt følgende fremgangsmåde for at oprette objektbaserede dimensioner:

1. Gå til **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner**.
2. Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.
3. Vælg **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**. 
4. Angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.

> ![Definition af standardtitelobjekt.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensioner baseret på grupperet indstilling 
Du kan oprette to dimensioner, der er baseret på grupperet indstilling. 

- Brug **Ressourcens arbejdsplacering** til at følge prisen på arbejde på lokationen **Hjemme** og **På stedet**. 
- Brug **Ressourcens arbejdstimer** med værdierne **Almindelig** og **Overarbejde** for at foretage en markering, når arbejdet er fuldført.

Følgende grafik indeholder en oversigt over dimensionen **Ressourcens arbejdslokation**. 

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdssted for ressource.](media/Option-set-PD-called-Resource-Work-Location.png)

Følgende grafik indeholder en oversigt over dimensionen **Ressourcens arbejdstid**. 

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdstimer for ressource.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Gå til **Indstillinger** > **Løsninger** og dobbeltklik på **\<your organization name> prisfastsættelsesdimensioner**. 
2. Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten. 
3. Vælg **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.

## <a name="create-data-for-entity-based-dimensions"></a>Oprette data til objektbaserede dimensioner

Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald. Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**. Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.

1. Vælg **Avanceret søgning**.
2. Vælg objektet **Standardtitel**, og vælg derefter **Resultater**. Alle rækkerne i objektet **Standardtitel** vises.
3. Vælg **Ny**, angiv "Systemtekniker" i feltet **Navn**, og vælg derefter **Gem**.
4. Luk siden. 
5. Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".

> ![Eksempeldata til objektet Standardtitel.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]