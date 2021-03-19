---
title: Opret brugerdefinerede løsninger til prisfastsættelsesdimensioner
description: I dette emne beskrives det, hvordan du kan oprette en brugerdefineret løsning, når du opretter brugerdefinerede prisfastsættelsesdimensioner.
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284981"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Opret brugerdefinerede løsninger til prisfastsættelsesdimensioner

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Alle ændringer af brugerdefineret prisfastsættelsesdimensioner bør være i en separat løsning. Denne vigtige bedste praksis giver større fleksibilitet i fremtiden til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til en anden forekomst. Når du har foretaget de nødvendige ændringer, skal du eksportere løsningen som en **Administreret løsning** og importere den i andre forekomster for at genbruge din prisfastsættelse.

1. Vælg **Indstillinger** > **Løsninger**, og vælg derefter **Ny**. 
2. Navngiv løsningen **\<your organization name> prisfastsættelsesdimensioner**, angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.

> ![Oprettelse af en brugerdefineret løsning til prisdimensioner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tilføj alle nødvendige objekter og relaterede komponenter i løsningen til prisfastsættelsesdimensionen
Du skal føje følgende Project Service-objekter til din prissætningsløsning. Fuldfør trinnene i denne fremgangsmåde for at foretage nogle vigtige skemaændringer i prisfastsættelsesløsningen, så enhederne bliver opmærksomme på de nye prisfastsættelsesdimensioner.

1. Vælg **Indstillinger** > **Løsninger** og dobbeltklik derefter på **\<your organization name> prisfastsættelsesdimensioner**. 
2. Vælg **Tilføj eksisterende** > **Objekter** i venstre navigationsrude i løsningsoversigten.
3. Vælg følgende objekter i dialogboksen **Løsningskomponenter**:

- Faktisk
- Reserverbar ressource
- Estimatlinje
- Projektopgave
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

4. Vælg **Nej**, når du bliver bedt om at inkludere afhængige objekter for de valgte objekter.

> ![Inkluder ikke alle relaterede komponenter](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]