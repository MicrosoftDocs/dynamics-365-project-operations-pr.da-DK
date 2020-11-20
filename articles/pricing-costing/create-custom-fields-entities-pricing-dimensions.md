---
title: Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse
description: Dette emne indeholder oplysninger om, hvordan du kan oprette brugerdefinerede grupperede indstillinger eller objekter.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130886"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Opret brugerdefinerede felter og objekter som dimensioner for prisfastsættelse

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt.

> [!IMPORTANT]
> Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning. Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst. Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prissætning.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Oprette en brugerdefineret løsning til prisdimensioner
1. Gå til **Indstillinger** > **Løsninger**, og vælg derefter **Ny** for at oprette en ny løsning. 
2. Navngiv løsningen **\<your organization name> prisfastsættelsesdimensioner**, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen

En prisdimension kan være en grupperet indstilling eller et objekt. Begge skal være oprettet i din prissætningsløsning. I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.

### <a name="entity-based-dimensions"></a>Objektbaserede dimensioner

1. Gå til **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner**.
2. Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.
3. Vælg **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**. 
4. Angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.


### <a name="option-set-based-dimensions"></a>Dimensioner baseret på grupperet indstilling 
Du kan oprette to dimensioner, der er baseret på grupperet indstilling. Brug **Arbejdssted for ressource** til at spore prisen på arbejdet på arbejdsstedet **Privat** og **Privat** og brug **Arbejdstimer for ressource** med værdierne **Almindelig** og **Overtid** for at anvende en markering, når arbejdet er fuldført.


1. Gå til **Indstillinger** > **Løsninger** og dobbeltklik på **\<your organization name> prisfastsættelsesdimensioner**. 
2. Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten. 
3. Vælg **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.

## <a name="create-data-for-entity-based-dimensions"></a>Oprette data til objektbaserede dimensioner

Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald. Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**. Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.

1. Vælg **Avanceret søgning**, Vælg objektets **Standardtitel**, og vælg derefter **Resultater**. Alle rækkerne i objektet **Standardtitel** vises.
2. Vælg **Ny**, angiv "Systemtekniker" i feltet **Navn**, og vælg derefter **Gem**.
3. Luk formularen. 
4. Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tilføje alle nødvendige objekter og relaterede komponenter i løsningen til prisfastsættelsesdimensionen
Du skal føje følgende objekter til din prisfastsættelsesløsning. Følg trinnene i denne fremgangsmåde for at foretage nogle vigtige skemaændringer i prissætningsløsningen, så objekterne bliver opmærksomme på de nye prisdimensioner.

1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik på **\<your organization name> prisfastsættelsesdimensioner**. 
2. Vælg **Tilføj eksisterende** > **Objekter** i venstre navigationsrude i løsningsoversigten.
3. Vælg følgende objekter i dialogboksen **Løsningskomponenter**:

  - Faktisk
  - Reserverbar ressource
  - Estimatlinje
  - Fakturalinjedetalje
  - Kladdelinje
  - Projektkontraktlinjedetalje
  - Medlem af projektteam
  - Tilbudslinjedetaljer
  - Rolleprisavance
  - Rollepris 
  - Tidsregistrering 


> [!NOTE]
> Sørg for at inkludere alle formularer og visninger for hvert af de valgte objekter.

4. Vælg **Nej**, når du bliver bedt om at inkludere afhængige objekter for de objekter, der er valgt ovenfor.

