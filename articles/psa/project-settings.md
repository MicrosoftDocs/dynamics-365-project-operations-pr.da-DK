---
title: Projektindstillinger
description: Dette emne indeholder oplysninger om indstillinger for projektstyring.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148141"
---
# <a name="project-settings"></a>Projektindstillinger

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Brug følgende indstillinger for at få adgang til funktionerne til projektplanlægning.

## <a name="work-template"></a>Arbejdsskabelon

Du opretter en projektplan ved at oprette en projektkalenderskabelon, der definerer antallet af arbejdstimer pr. dag og eventuelle lukketider. Du opretter en projektkalenderskabelon ved at knytte en arbejdsskabelon til feltet **Kalenderskabelon** for projektet. Følg disse trin for at oprette en arbejdsskabelon.

1. I venstre navigationsrude i PSA skal du klikke på **Ressourcer**. 
2. På listesiden **Ressourcer** skal du åbne en brugerpost og derefter vælge **Vis arbejdstimer**.

  > [!NOTE]
  > Sørg for at tillade pop op-vinduer på browsersiden. Her kan du se de arbejdstimer, der er angivet for ressourcen.
  
3. På fanen **Månedsvisning** skal du klikke på **Konfigurer**. Der vises en liste med tre valgmuligheder: 

  - Ny ugeplan
  - Arbejdsplan for én dag
  - Fri

> ![Konfigurer indstillinger](media/project-13.png)

4. Vælg **Ny ugeplan**, og angiv derefter indstillingerne for denne ressourceplanlægning. Du kan angive en tilbagevendende ugentlig tidsplan, parametre for daglige timer, lukketider og meget mere.
5. Angiv datointervallet, vælg **Gem**, og klik derefter på **Luk**. 
6. Gå tilbage til listesiden **Ressourcer**, og vælg den ressource, du vil angive arbejdstimer for. 
7. Vælg **Angiv kalender som** for at angive arbejdsskabelonen. 
8. I dialogboksen **Arbejdsskabelon** skal du angive et navn for arbejdsskabelonen og derefter vælge **Anvend.** 

Du kan nu knytte arbejdsskabelonen til en skabelon for projektkalenderen.

## <a name="resource-roles"></a>Ressourceroller

Udtrykket *Ressourcerolle* refererer til det sæt færdigheder, kompetencer og certificeringer, som en person skal have for at kunne udføre et bestemt sæt opgaver på et projekt. PSA giver dig mulighed for at omkostningsbestemme og fakturere en ressources tid baseret på den rolle, ressourcen er knyttet til. De enkelte organisationer skal konfigurere disse roller ved hjælp af den venstre navigationsrude i menuen **Project Service**.

De enkelte organisationer skal konfigurere disse roller på siden **Aktive ressourcekategorier**. Hvis du vil åbne denne side, skal du vælge **Ressourceroller** i venstre navigationsrude.

## <a name="price-lists"></a>Prislister

Prislisterne giver dig mulighed for at indstille kost- og salgspriser for ressourceroller, udgiftskategorier, produkter og andre elementer i en organisation. Inden du angiver økonomiske estimater for det arbejde, der skal leveres til et projekt, skal du oprette en sikkerhedskopi af omkostnings- og prisliste. I sektionen parametre skal du også konfigurere en standard omkostnings- og prisliste, der gælder for alle de projekter, der oprettes i organisationen. På siden **Aktive projektparametre** skal du sørge for at konfigurere en omkostnings- og prisliste.


[!INCLUDE[footer-include](../includes/footer-banner.md)]