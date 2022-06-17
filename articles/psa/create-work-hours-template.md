---
title: Opret en arbejdstidsskabelon
description: I denne artikel beskrives det, hvordan du kan oprette en arbejdstidsskabelon i Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916051"
---
# <a name="create-a-work-hours-template-project-service"></a>Oprette en arbejdstimeskabelon (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Hvis du vil oprette og administrere et projekt, skal du anvende en kalenderskabelon på projektet. I kalenderskabelonen defineres følgende projektattributter:

- Arbejdstider, herunder start- og sluttid
- Arbejdsdage
- Kalenderundtagelser, f.eks. ikke-arbejdsdage

Den kalenderskabelon, der anvendes på et projekt, er en kopi af den kalenderskabelon, der er defineret i organisationens indstillinger.

> [!NOTE]
> Hvis du ændrer kalenderskabelonen, overføres disse ændringer ikke til projektets arbejdstider. Hvis du vil ændre projektets arbejdstimer, skal der anvendes en ny skabelon.

Hvis du vil oprette en kalenderskabelon for din organisation, er der to nøglekrav:

- Definér skabelonens ønskede arbejdstimer ved hjælp af en ny eller eksisterende ressource, der kan reserveres.
- Opret en ny kalenderskabelon, og knyt skabelonen til den ressource, der kan reserveres.

**Definér arbejdstimerne for skabelonen**

1. Gå til **Ressourcer** \> **Ressourcer**.
2. Opret en ny ressource, der skal refereres til i kalenderskabelonen, eller vælg en eksisterende ressource.
3. Vælg fanen **Arbejdstimer** for ressourcen, og fuldfør instruktionerne i [Angiv arbejdstimer for en ressource](/dynamics365/field-service/set-work-hours-resource) for at konfigurere kalenderreglerne.

**Opret en ny kalenderskabelon**

1. Gå til **Indstillinger** \> **Kalenderskabelon**.
2. Vælg **Ny**, og angiv et navn, en beskrivelse og en skabelonressource.


> [!NOTE]
> Når der refereres til en ressource i en kalenderskabelon, knyttes der en kopi af ressourcens kalender til kalenderskabelonen. Hvis arbejdstimerne i den kopierede skabelon ændres, vil disse ændringer ikke blive overført til kalenderskabelonen.


### <a name="see-also"></a>Se også  
 [Konfigurer ressourcer](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
