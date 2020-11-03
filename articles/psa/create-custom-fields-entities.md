---
title: Oprette brugerdefinerede felter og objekter
description: I dette emne beskrives det, hvordan du kan oprette grupperede indstillinger og objekter i din egen løsning i Power Apps-platformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074241"
---
# <a name="create-custom-fields-and-entities"></a>Oprette brugerdefinerede felter og objekter 

Benyt følgende fremgangsmåde, når du vil oprette en brugerdefineret grupperet indstilling eller et objekt på Power Apps-platformen.  
Fremgangsmåderne i dette emne skal udføres ved hjælp af webgrænsefladen i Project Service Automation (PSA).

> [!IMPORTANT]
> Det anbefales, at du foretager alle ændringer af brugerdefinerede prisdimensioner i en separat løsning. Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst. Når du har foretaget alle de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prissætning.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Oprette brugerdefinerede felter og grupperet indstilling i prisdimensionsløsningen

En prisdimension kan være en grupperet indstilling eller et objekt. Begge skal være oprettet i din prissætningsløsning. I fremgangsmåden i denne procedure forklares det, hvordan du kan oprette objektbaserede dimensioner og dimensioner baseret på en grupperet indstilling.

### <a name="entity-based-dimensions"></a>Objektbaserede dimensioner

1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner** i PSA.
2. Vælg **Objekter** i venstre navigationsrude i løsningsoversigten.
3. Klik på **Nyt** for at oprette et nyt objekt med navnet **Standardtitel**. Angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.

> ![Definition af standardtitelobjekt](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensioner baseret på grupperet indstilling 
Du kan oprette to dimensioner, der er baseret på grupperet indstilling. Brug **Arbejdssted for ressource** til at spore prisen på arbejdet på arbejdsstedet **Privat** og **Privat** og brug **Arbejdstimer for ressource** med værdierne **Almindelig** og **Overtid** for at anvende en markering, når arbejdet er fuldført.


1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner** i PSA. 
2. Vælg **Grupperede indstillinger** i venstre navigationsrude i løsningsoversigten. 
3. Klik på **Ny** for at oprette en ny grupperet indstilling, angiv de resterende nødvendige oplysninger, og klik derefter på **Gem**.

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdssted for ressource ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Prisdimension, der er baseret på grupperet indstilling, kaldet Arbejdstimer for ressource ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Oprette data til objektbaserede dimensioner

Du kan oprette data til objektbaserede dimensioner manuelt eller ved hjælp af Microsoft Excel-import eller -serviceopkald. Følg trinnene i denne fremgangsmåde for at oprette to standard titler, **Systemtekniker** og **Seniorsystemtekniker** fra den objektbaserede dimension, **Standardtitel**. Hvis de data, du vil oprette, er små, som i følgende eksempel, kan du bruge en standardformular.

1. Klik på **Avanceret søgning** i PSA. Vælg objektet **Standardtitel** , og klik derefter på **Resultater**. Alle rækkerne i objektet **Standardtitel** vises.
2. Klik på **Ny**. Angiv "Systemtekniker" i feltet **Navn** , og klik derefter på **Gem**.
3. Luk formularen. 
4. Gentag trin 1-3 for at oprette endnu en standardtitel til "Seniorsystemtekniker".

> ![Eksempeldata til objektet Standardtitel ](media/ST-data.png)


