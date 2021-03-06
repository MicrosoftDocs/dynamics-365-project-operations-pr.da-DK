---
title: Definere ressourcekalendere
description: Dette emne indeholder oplysninger om, hvordan du definerer arbejdstidskalendere for ressourcer i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961840"
---
# <a name="define-resource-calendars"></a>Definere ressourcekalendere

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Alle de reserverbare ressourcer, der arbejder på et projekt, skal have en kalender med arbejdstid for at definere deres tilgængelighed. Arbejdstiderne for en ressource kan defineres på to måder: 

   - Definer individuelle kalenderregler for en ressource
   - Anvend en eksisterende kalenderskabelon for ressourcen

## <a name="define-a-resources-working-hours"></a>Definer en ressources arbejdstid

1. I menuen **Ressourcer** skal du vælge **Ressourcer**.
2. I gittervisningen skal du vælge en anvendelig **Reserverbar ressource** .
3. På siden **Ressourcedetaljer** skal du vælge fanen **Arbejdstid**. Som standard er den reserverbare ressourcekalender arbejdstiderne for den standardarbejdsugeskabelon, der er defineret for organisationen.
4. Hvis du vil opdatere arbejdstiderne, skal du højreklikke på startdatoen for den foreslåede kalenderregel, der skal defineres. Brug menuen kalenderregler til at definere en kalenderregel for en bestemt dag, resten af serien eller hele kalenderen.
5. Når indstillingen er valgt, kan du definere følgende:

    - Den ugedag, hvor arbejdstiden træder i kraft.
    - Arbejdstiderne inden for hver dag.
    - Tidszonen for kalenderreglen.
    - Hvis det er relevant, kan ikke-arbejdstiden også angives for reglen.

## <a name="applying-a-calendar-template-to-a-resource"></a>Anvendelse af en kalenderskabelon til en ressource

1. I menuen **Ressourcer** skal du vælge **Ressourcer**.
2. Vælg op til 25 **Reserverbare ressourcer** i gittervisningen, som skal opdateres.
3. Vælg **Angiv kalender** og en dialogboks vises med en liste over tilgængelige arbejdstidsskabeloner.
4. Vælg den til at finde den skabelon, som du vil bruge, og vælg derefter **Anvend**.
