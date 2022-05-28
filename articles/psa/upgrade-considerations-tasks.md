---
title: Opgradere overvejelser i forbindelse med arbejdsopgavehierarkiet
description: Dette emne indeholder oplysninger om opgradering af arbejdsopgavehierarkiet fra Project Service Automation 2.x til 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 13ad93d5be3c0ab07c81db28d3e13561e9d40017
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599723"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Opgradere overvejelser i forbindelse med arbejdsopgavehierarkiet

[!include [banner](../includes/psa-now-project-operations.md)]

Dette emne indeholder oplysninger om opgradering af arbejdsopgavehierarkiet fra Project Service Automation 2.x til 3.x. I dette emne defineres den korrekte tilstand for et projekt i PSA (Project Service Automation), der skal bruges for at opnå en vellykket opgradering. Der findes også oplysninger om de almindelige blokeringsforhold, der medfører, at opgraderingen ikke lykkes. Du kan finde flere oplysninger om definition af projektopgaver og deres funktioner i en projektplan i [Projektplaner](project-creating.md).

## <a name="key-entities"></a>Nøgleobjekter
Hvis du vil have et nøjagtigt arbejdsopgavehierarki, der allerede er indlæst med ressourcer, skal følgende objekter bruges:

- [Projekt](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektopgave](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Ressourcetildelinger](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Projektopgaveafhængighed](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Reserverbare ressourcer](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Hvis du vil definere en ressources indlæste arbejdsopgavehierarki, skal du udføre følgende trin:

1. Oprette et nyt projekt. Du finder flere oplysninger om, hvordan du opretter et nyt projekt i [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Oprette en eller flere opgaver. Du finder flere oplysninger om, hvordan du opretter en opgave i [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definere opgaveafhængigheder. Du kan finde flere oplysninger i [Projektopgaveafhængighed](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Tildele projektteammedlemmer til projektet. Du kan finde flere oplysninger i [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Tildele projektteammedlemmer til opgaverne. Du kan finde flere oplysninger i [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Projektteamrelationer

Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:
- Alle projektteammedlemmer skal være tilknyttet en reserverbar ressource.
- Alle projektteammedlemmer skal være tilknyttet det samme projekt. 

## <a name="project-task-relationships"></a>Projektopgaverelationer
Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:

- Eventuelle relaterede opgaver skal være knyttet til det samme projekt.
- Alle linjeopgaver skal have en overordnet opgave.
- Alle opgaver skal have et overordnet projekt.

### <a name="valid-conditions"></a>Gældende betingelser.

- Alle opgavevarigheder skal være længere end eller lig med (> =) en time og mindre end 1.800.000 minutter (1.250 dage).*
- Alle opgaver skal have en startdato, der ikke ligger før 1.1.2000.*
- Alle opgaver skal have en startdato senest 17 år fra i dag.*
- Alle opgaver skal have en startdato, der ligger før eller er lig med deres slutdato.
- Alle transaktionstyper for klassificeringer (udgift, materiale, moms og tid) skal indeholde værdier for **Standardenhed** og **Enhedsgruppe**.
- Datoformater med bogstaver skal undgås.

### <a name="potential-mitigation-steps"></a>Potentielle afhjælpningstrin
- Brug avanceret søgning til at identificere projektopgaver, der ikke indeholder et projekt-ID.
- Brug avanceret søgning til at identificere projektopgaver, hvor den planlagte varighed er større end > 1.800.000.
- Før du foretager ændringer i data, skal du undersøge eventuelle tilpasninger, der er knyttet til det objekt, der kan have ført til dataenes dårlige tilstand. Disse tilpasninger skal rettes, før du kan fortsætte med datarelaterede opdateringer.
- I forbindelse med de identificerede opgaver, der er gået tabt, kan du overveje at slette disse opgaver, hvis de ikke er nødvendige, eller hvis de skal knyttes til det korrekte overordnede projekt.
- I forbindelse med opgaver, hvor varigheden er større end 1.250 dage, skal du overveje at tilføje flere opgaver, som tilsammen kan udgøre den samlede varighed, hvis det er muligt.

> [!NOTE]
> Elementer, der er angivet med en stjerne (\*), har grænser, der skyldes, at styring af kunderelationer (CRM) kun understøtter 7.320 gentagelsesudvidelser. Du skal være under denne grænse.

## <a name="resource-assignment-relationships"></a>Ressourcetildelingsrelationer
Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:

- Alle ressourcetildelinger i et arbejdsopgavehierarki skal være relateret til det samme projekt.
- Alle ressourcetildelinger i et arbejdsopgavehierarki skal være knyttet til projektteammedlemmer i det samme projekt.

### <a name="potential-mitigation-steps"></a>Potentielle afhjælpningstrin
- Identificer alle de opgaver, der falder uden for de betingelser, der er beskrevet ovenfor.  
- Eventuelle ressourcetildelinger, der ikke længere er gyldige, skal slettes.

## <a name="project-task-dependency-relationships"></a>Afhængighedsrelationer for projektopgave
Følgende relationer skal vedligeholdes korrekt for at sikre en vellykket opgradering:

- Alle projektopgaveafhængigheder skal være relateret til det samme projekt.
- En opgave kan ikke have samme afhængighed refereret mere end én gang.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
