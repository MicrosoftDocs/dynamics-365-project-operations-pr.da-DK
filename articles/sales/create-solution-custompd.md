---
title: Opret en løsning til brugerdefinerede prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om, hvordan du opretter løsninger for brugertilpassede prisfastsættelsesdimensioner.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010329"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Opret en løsning til brugerdefinerede prisfastsættelsesdimensioner

 _**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_ 

>[!IMPORTANT]
>Alle ændringer af brugerdefineret prisfastsættelsesdimensioner bør være i en separat løsning. Denne vigtige bedste praksis tillader større fleksibilitet til at opdatere eller fjerne ændringer efter behov, hjælper dig med at genbruge dit arbejde og gør det nemmere at overføre disse ændringer til andre forekomster. Når du foretager de nødvendige ændringer, skal du eksportere løsningen som en **Administreret** løsning og derefter importere den i andre forekomster for at genbruge den.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Opret en løsning til brugerdefinerede prisfastsættelsesdimensioner

1.  Vælg **Indstillinger** > **Løsninger**, og vælg derefter **Ny**.
2.  Navngiv løsningen *<your organization name> prisfastsættelsesdimensioner*.
3. Angiv de resterende nødvendige oplysninger, og vælg derefter **Gem**.

  ![Oprettelse af en løsning til brugerdefinerede prisfastsættelsesdimensioner](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Tilføj alle nødvendige objekter og relaterede komponenter i løsningen til prisfastsættelsesdimensionen

Tilføj følgende Project Service-objekter til din prisfastsættelsesløsning for at foretage vigtige skemaændringer i prisfastsættelsesløsningen. Når du har fuldført denne procedure, genkender objekterne de nye prisfastsættelsesdimensioner.

1.  Vælg **Indstillinger** > **Løsninger**, og dobbeltklik derefter på **<*dit organisationsnavn*> prisfastsættelsesdimensioner**.
2.  Vælg **Tilføj eksisterende** > **Objekter** i venstre navigationsrude i løsningsoversigten.
3.  Vælg følgende objekter i dialogboksen **Løsningskomponenter**:
 
   - **Faktisk**
   - **Reserverbar ressource**
   - **Estimatlinje**
   - **Projektopgave**
   - **Fakturalinjedetalje**
   - **Kladdelinje**
   - **Projektkontraktlinjedetalje**
   - **Medlem af projektteam**
   - **Tilbudslinjedetaljer**
   - **Rolleprisavance**
   - **Rollepris**
   - **Tidsregistrering**
 
   ![Tilføj eksisterende løsning for brugertilpasset prisfastsættelsesdimension](./media/Existing-entities-to-PD-solution.png)
 
 4. Gennemgå for hvert objekt de komponenter, der tilføjes, og den endelige liste over enhedsaktiver for hver enhed. 

   >[!NOTE]
   > Inkluder alle formularer og visninger for hvert af de valgte objekter.

  ![Objekter tilføjet](./media/solution-component-selection.png)


5.  Når du bliver bedt om at medtage eventuelle afhængige objekter for de valgte objekter, skal du vælge **Nej, medtag ikke de påkrævede komponenter.**

    ![Herunder afhængige enheder](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]