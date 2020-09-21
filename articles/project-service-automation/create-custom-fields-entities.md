---
title: Oprette brugerdefinerede felter og objekter
description: I dette emne beskrives det, hvordan du kan oprette grupperede indstillinger og objekter i din egen løsning i Power Apps-platformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750610"
---
# <a name="create-custom-fields-and-entities"></a>Oprette brugerdefinerede felter og objekter 

Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt på Power Apps-platformen.  
Fremgangsmåderne i dette emne skal udføres ved hjælp af webgrænsefladen i Project Service Automation (PSA).

> [!IMPORTANT]
> Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning. Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst. Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prissætning.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Oprette en brugerdefineret løsning til prisdimensioner
1. Klik i PSA på **Indstillinger** > **Løsninger**, og klik derefter på **Ny** for at oprette en ny løsning. 
2. Navngiv løsningen **\<navnet på din organisation > prisdimensioner**, angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.

> ![Oprettelse af en brugerdefineret løsning til prisdimensioner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen

En prisdimension kan være en grupperet indstilling eller et objekt. Begge skal være oprettet i din prissætningsløsning. I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.

### <a name="entity-based-dimensions"></a>Objektbaserede dimensioner

1. I PSA skal du klikke på **Indstillinger** > **Løsninger** og derefter dobbeltklikke på **\<organisationens navn> prisdimensioner**.
2. Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.
3. Klik på **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**. Angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.

> ![Definition af standardtitelobjekt](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensioner baseret på grupperet indstilling 
Du kan oprette to dimensioner, der er baseret på grupperet indstilling. Brug **Arbejdssted for ressource** til at spore prisen på arbejdet på arbejdsstedet **Privat** og **Privat** og brug **Arbejdstimer for ressource** med værdierne **Almindelig** og **Overtid** for at anvende en markering, når arbejdet er fuldført.


1. I PSA skal du klikke på **Indstillinger** > **Løsninger** og derefter dobbeltklikke på **\<din organisations navn> prisdimensioner**. 
2. Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten. 
3. Klik på **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdssted for ressource ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdstimer for ressource ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Oprette data til objektbaserede dimensioner

Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald. Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**. Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.

1. Klik på **Avanceret søgning** i PSA. Vælg objektet **Standardtitel**, og klik derefter på **Resultater**. Alle rækkerne i objektet **Standardtitel** vises.
2. Klik på **Ny**. Angiv "Systemtekniker" i feltet **Navn**, og klik derefter på **Gem**.
3. Luk formularen. 
4. Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".

> ![Eksempeldata til objektet Standardtitel ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tilføje alle nødvendige PSA-objekter og relaterede komponenter i en prisdimensionsløsning
Du skal føje følgende Project Service-objekter til din prissætningsløsning. Følg trinnene i denne fremgangsmåde for at foretage nogle vigtige skemaændringer i prissætningsløsningen, så objekterne bliver opmærksomme på de nye prisdimensioner.

1. I PSA skal du klikke på **Indstillinger** > **Løsninger** og derefter dobbeltklikke på **\<organisationens navn> prisdimensioner**. 
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

> ![Tilføje eksisterende objekter i prisdimensionsløsningen](media/Existing-entities-to-PD-solution.png)

> ![Vælge løsningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> Sørg for at inkludere alle formularer og visninger for hvert af de valgte objekter.

4. Klik på **Nej**, når du bliver bedt om at inkludere afhængige objekter for de objekter, der er valgt ovenfor.

> ![Inkluder ikke alle relaterede komponenter](media/Do-not-include-required.png)


