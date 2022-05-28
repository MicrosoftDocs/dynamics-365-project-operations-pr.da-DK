---
title: Opret en arbejdstidsskabelon
description: Dette emner beskriver, hvordan du opretter en arbejdstimeskabelon i Project Service.
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
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598941"
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
