---
title: Konfigurer planlægningsområdet til at vise kontraktmedarbejdere og underleverandørkapacitet
description: I dette emne beskrives det, hvordan du kan konfigurere planlægningsområdet i Microsoft Dynamics 365 Project Operations til at vise ressourcekapacitet, der er omfattet af en underentreprise, når projektressourcekravene skal bemandes.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902837"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurer planlægningsområdet til at vise kontraktmedarbejdere og underleverandørkapacitet 

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Planlægningsområdet i Microsoft Dynamics 365 Project Operations kan bruges til at søge efter ressourcer på to måder:

- Generel ressourcesøgning uden konteksten af et specifikt projektbaseret ressourcekrav.
- Kravspecifik ressourcesøgning, hvor projektkravet giver konteksten for de foreslåede ressourcer.

For at underrette de planlægningsansvarlige for en ressourcekapacitet og kontraktmedarbejdere, der er omfattet af en underentreprise, skal du opdatere indstillingerne i planlægningsområdet. Disse opdateringer omfatter: 
- Opdatering af indstillingerne for planlægningsområdet for generel ressourcesøgning.
- Opdatering af indstillingerne for planlægningsområdet for kravbaseret ressourcesøgning.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Opdatering af indstillingerne for planlægningsområdet for generel ressourcesøgning
### <a name="update-filters-for-general-resource-search"></a>Opdater filtre for generel ressourcesøgning
Når du søger efter en ressource, skal de filtre, der er tilgængelige i planlægningsområdet, opdateres, så du også kan søge efter eksterne ressourcer ved at angive en eller flere af følgende:
  - Medarbejdertype, uanset om de viste ressourcer skal være kontraktmedarbejdere eller ansatte.
  - Den leverandør, hvortil en ressource bør tilhøre.
  - Ressourcer, der tilhører en bestemt underleverandør eller underentrepriselinje.
    
### <a name="update-retrieve-resource-query"></a>Opdatere forespørgslen for at hente ressourcer
Den forespørgsel, der bruges til søgning, skal også opdateres, så den bruger disse ekstra filterattributter. Brug følgende trin til at opdatere konfigurationen af planlægningsområdet for generel ressourcesøgning:  
1. Åbn **Indstillinger for planlægningsområdet** for et bestemt planlægningsprogram.
2. Åbn fanen **Generelle indstillinger**, og rul til **Andre indstillinger**.
3. I listen med indstillinger i dette afsnit skal du opdatere **Filterlayout** til **Standardfilterlayout for Project Operations lille**.
4. Opdater **Hent ressourceforespørgsel** til **Standardforespørgsel for hentning af ressourcer til Project Operations lille**.

![Opdatering af indstillingerne for planlægningsområdet for generel ressourcesøgning](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Opdatering af indstillingerne for planlægningsområdet for kravbaseret ressourcesøgning
### <a name="update-filters-for-requirement-specific-resource-search"></a>Opdater filtre for kravspecifik ressourcesøgning 
Når du søger efter en ressource, skal de filtre, der er tilgængelige i planlægningsområdet, opdateres, så du også kan søge efter eksterne ressourcer ved at angive en eller flere af følgende:
 - Medarbejdertype, uanset om de viste ressourcer skal være kontraktmedarbejdere eller ansatte.
 - Den leverandør, hvortil en ressource bør tilhøre.
 - Ressourcer, der tilhører en bestemt underleverandør eller underentrepriselinje.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Opdater forespørgslen for hentning af en ressource for en kravspecifik ressourcesøgning 
Den forespørgsel, der bruges til søgning, skal også opdateres, så den bruger disse ekstra filterattributter. Brug følgende trin til at opdatere konfigurationen af planlægningsområdet for kravbaseret ressourcesøgning:

1. Åbn **Indstillingerne for planlægningsområdet** for et bestemt planlægningsprogram, og vælg derefter **Åbn standardindstillinger** for at åbne indstillingerne for kravspecifik søgning.
2. Åbn fanen **Generelle indstillinger**, og rul til **Andre indstillinger**.
3. I listen med indstillinger i dette afsnit skal du opdatere **Filterlayout** til **Standardfilterlayout for Project Operations lille**.
4. Opdater **Hent ressourceforespørgsel** til **Standardforespørgsel for hentning af ressourcer til Project Operations lille**.
5. Åbn fanen **Planlægningstyper**, og gå til **Projekt**.
6. Under indstillingerne for **Projekt** skal du opdatere **Forespørgslen Hent ressourcer til Planlægningsassistent** til **Standardforespørgsel for hentning af ressourcer til Project Operations lille** og opdatere **Forespørgslen Hent begrænsninger til Planlægningsassisten** til **Standardforespørgsel om hentning af begrænsninger for Project Operations lille**.

![Opdatering af indstillingerne for planlægningsområdet for kravbaseret ressourcesøgning](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
