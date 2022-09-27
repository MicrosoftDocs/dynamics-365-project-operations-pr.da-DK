---
title: Indstillinger for underleverandører for medlemmer af projektteam
description: I denne artikel forklares indstillingerne for underleverandører for projektteammedlemmer i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522271"
---
# <a name="subcontracting-options-for-project-team-members"></a>Indstillinger for underleverandører for medlemmer af projektteam

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I Microsoft Dynamics 365 Project Operations kan du evaluere de indstillinger for underleverandører, der er tilgængelige for et eller flere medlemmer af projektteamet. De tilgængelige indstillinger for underleverandører giver dig mulighed for at:

- Oprette en ny underleverandør, og/eller oprette nye linjer på en eksisterende underleverandør for de valgte medlemmer af projektteamet. 
- Reservere i forhold til en allerede eksisterende underleverandør og underentrepriselinje. 

Du kan vælge mellem de tilgængelige indstillinger for underleverandører for generiske projektteammedlemmer eller vælge mellem de projektteammedlemmer, der er bemandet med en navngivet ressource, som er en kontraktmedarbejder. 

Der findes ingen indstillinger for underleverandører til følgende:

- Medlemmer af projektteamet, der er bemandet med en medarbejder. 
- Projektteammedlemmer, som allerede er tilknyttet en underleverandør og en underentrepriselinje. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Ansættelse af et ubemandet projektteammedlem fra en underleverandør

Hvis du vil gennemse og vælge mellem de tilgængelige indstillinger for underleverandører for et generisk eller ikke-bemandet projektteammedlem, skal du følge disse trin:

1. Vælg en eller flere projektgruppemedlemsposter, hvor ressourcen er en generisk ressource.
2. Sørg for, at ingen af de valgte teammedlemsposter i projektet allerede er omfattet af en underentreprise. 
3. Vælg **Indstillinger for underleverandører** i undergitteret for medlemmer af projektteamet. Dialogboksen **Indstillinger for underleverandører** åbnes. 
4. Hvis du kun har valgt én post for projektteammedlemmer i trin 1, er følgende muligheder tilgængelige:
    - Opret nye underentrepriselinjer. 
    - Reserver i forhold til en eksisterende underleverandør. Hvis du har valgt flere projektgruppemedlemsposter i trin 1, er den eneste tilgængelige indstilling at oprette nye underleverandørlinjer.
5. Hvis du reserverer i forhold til en eksisterende underentrepriselinje, kan du vælge en underleverandør- og underentrepriselinje, som du vil reservere mod. Når du vælger en underentrepriselinje for at reservere kapacitet, skal du sikre dig, at den valgte underentrepriselinje er for tid, og at den rolle, der kræves af projektteammedlemmet, svarer til den rolle, der blev købt på underentrepriselinjen.
6. Når du vælger at oprette nye underentrepriselinjer for projektteammedlemmerne, kan du i systemet vælge den underleverandør, som du vil have til at oprette disse linjer. Den underleverandør, som du vælger for at oprette nye linjer i, skal have statussen **Kladde**. Med denne indstilling kan du oprette nye underentrepriselinjer for de valgte medlemmer af projektteamet, og der oprettes én underentrepriselinje for hver enkelt projektgruppemedlems tid. Rollen, timerne og datoerne kopieres fra projektteammedlemmet til hver enkelt underentrepriselinje, der oprettes. 
7. Når et generisk teammedlem knyttes til en underleverandør og underentrepriselinje, opdateres feltet **Medarbejdertype** i rækken for det generiske teammedlem til **Kontraktmedarbejder**, og værdien for **Validering af underleverandør** angives til **Gyldig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Ansættelse af et bemandet projektteammedlem fra en underleverandør

På samme måde som ved generiske eller ikke-bemandede teammedlemmer kan du også få vist indstillinger for underleverandører for en medarbejder i et projektteam, hvis den bemandende medarbejder er kontraktmedarbejder. Hvis du vil gennemse og vælge mellem de tilgængelige indstillinger for underleverandører for et bemandet eller navngivet projektteammedlem, skal du følge disse trin:

1. Vælg en eller flere projektgruppemedlemsposter, hvor ressourcen er en navngivet kontraktmedarbejder.
2. Sørg for, at ingen af projektteammedlemsposterne allerede er valgt af en underentreprise. 
3. Vælg **Indstillinger for underleverandører** i undergitteret for medlemmer af projektteamet. Dialogboksen **Indstillinger for underleverandører** åbnes. 
4. Hvis du kun har valgt én post for projektteammedlemmer i trin 1, er følgende muligheder tilgængelige:
      - Opret nye underentrepriselinjer.
      - Reservér i forhold til en eksisterende underentreprise.
  Hvis du har valgt flere projektgruppemedlemsposter i trin 1, er den eneste tilgængelige indstilling at oprette nye underleverandørlinjer.
5. Hvis du reserverer i forhold til en eksisterende underentrepriselinje, kan du vælge en underleverandør- og underentrepriselinje, som du vil reservere mod. Når du vælger en underentrepriselinje for at reservere kapacitet, skal du sikre dig følgende:
      - Den valgte underentrepriselinje er for tid. 
      - Den rolle, der kræves for projektteammedlemmerne, svarer til den rolle, der er købt på underentrepriselinjen. 
      - Den leverandør, som kontraktmedarbejderen er tilknyttet, er den samme som leverandøren i underentreprisen.
6. Når du vælger at oprette nye underentrepriselinjer for projektteammedlemmerne, kan du i systemet vælge den underleverandør, som du vil have til at oprette disse linjer. Med denne indstilling skal du sikre, at den leverandør, som kontraktmedarbejderen tilhører, er den samme som leverandøren i underentreprisen. 
7. Den underleverandør, som du vælger for at oprette nye linjer i, skal have statussen **Kladde**. Med denne indstilling kan du oprette nye underentrepriselinjer for de valgte medlemmer af projektteamet, og der oprettes én underentrepriselinje for hver enkelt projektgruppemedlems tid. Rollen, timerne og datoerne kopieres fra projektteammedlemmet til hver enkelt underentrepriselinje, der oprettes.  
8. Når et navngivet teammedlem knyttes til en underleverandør og underentrepriselinje, opdateres feltet **Medarbejdertype** i rækken for det navngivne teammedlem til **Kontraktmedarbejder**, og værdien for **Validering af underleverandør** angives til **Gyldig**.

## <a name="re-costing-subcontractor-assignments"></a>Omfordeling af omkostninger i underentrepriser

Når et medlem af et projektteam (generisk eller navngivet) knyttes til underentrepriselinjer ved hjælp af dialogboksen **Indstillinger for underleverandører**, skal omkostninger for tildelinger til opgaver, som teammedlemmet har, genberegnes på grundlag af den købsprisliste, der er knyttet til underleverandøren. På fanen **Estimater** på siden **Projektdetaljer** skal du vælge knappen **Opdater priser** for at se opdateret prisfastsættelse og/eller omkostninger, der er resultatet af beslutningen om at anvende en underleverandør.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
