---
title: Oprette en projektreservation fra planlægningsområdet
description: Denne emne indeholder oplysninger om, hvordan du kan oprette en projektreservation fra planlægningsområdet.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992959"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Oprette en projektreservation fra planlægningsområdet

[!include [banner](../includes/psa-now-project-operations.md)]

Du kan reservere en ressource til et projekt direkte fra fanen **Team** i projektet eller ved at generere et ressourcekrav fra en tildeling af et generisk teammedlem og derefter indfri genererede krav med et projektteammedlem.

Du kan også reservere en ressource til et projekt direkte fra planlægningsområdet. Der er tre måder, du kan gøre det på:

- **Reservere fra et genereret ressourcekrav:** Du kan oprette et ressourcekrav, når du har oprettet en generisk ressource og tildelt opgaver i et projekt.

- **Reservere fra det primære krav:** De primære krav vises i planlægningsområdet under fanen **Projekt**. 

- **Reservere fra et nyt ressourcekrav:** Du kan oprette et ressourcekrav fra bunden og knytte det til et projekt. I planlægningsområdet vises ressourcekravet under fanen **Åbn Krav**.

## <a name="book-from-a-generated-resource-requirement"></a>Reservere fra et genereret ressourcekrav

Du kan oprette en generisk ressource og tildele den en eller flere opgaver i et projekt. Derefter kan du oprette et ressourcekrav ud fra det generiske teammedlem. 

1.  I planlægningsområdet vises denne ressource under fanen **Åbn Krav**. Det kan være nødvendigt at bruge kolonnefiltre på gitteret, hvis du har mange åbne krav. 

    ![Åbn fanen Krav i planlægningsområdet](media/FAQ-Project-Booking-Schedule-Board-1.png "Skærmbillede af reservations- og tildelingstabel")

2. Vælg kravet. Fanen **Find tilgængelighed** vises over den valgte række.
 
3. Når du vælger fanen, åbnes tilstanden Planlægningsassistent i planlægningsområdet, og derefter filtreres de tilgængelige ressourcer, der opfylder ressourcekravet. Derefter kan du reservere en ressource.

4. Du kan også trække og slippe den markerede række fra bunden af planlægningsområdet til en ressourcecelle i gitteret ovenfor. Når du slipper kravet, åbnes panelet **Opret ressourcereservation** til højre.

    Hvis du vælger **Reservér**, reserveres ressourcen til projektteamet.

![Panelet Opret ressourcereservation](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Reservere fra det primære krav

Når du opretter et projekt i Project Service, oprettes der automatisk et ressourcekrav, der kaldes det primære krav. Det er et tomt krav, der bruges til hurtigt at reservere en ressource i planlægningsområdet uden at generere et krav eller oprette et fra bunden. Da kravet er tomt, skal du angive datoer samt fordelingsmetoden og timer, hvis det er relevant. 

1. Du kan reservere en ressource med det primære krav ved i planlægningsområdet at vælge fanen **Projekt**. Hvis du har mange projekter, skal du muligvis bruge kolonnefilteret i kolonnen **Projekt**.

   ![Kolonnefiltre i planlægningsområdet](media/FAQ-Project-Booking-Schedule-Board-2.png "Skærmbillede af reservations- og tildelingstabel")

2. Vælg det krav, der kun har projektnavnet som navn og har en varighed på nul (0).

3. Vælg fanen **Find tilgængelighed**, der vises i rækken. Dette aktiverer tilstanden Planlægningsassistent i planlægningsområdet og viser tilgængelige ressourcer, der kan reserveres til projektet.

4. Da et **Primært krav** er et tomt krav med nul (0) varighed, skal du angive varigheden i panelet **Opret ressourcereservation**, når du vælger og reserverer en ressource.

5. Du kan også vælge det **primære projektkrav** nederst i planlægningsområdet og trække og slippe det på en ressource for at reservere det.
 
    Da **Primært krav** er et tomt krav med nul (0) varighed, skal du angive varigheden i panelet **Opret ressourcereservation**, når du vælger og reserverer en ressource.
 
    Når du reserverer en ressource ved hjælp af **Primært krav** i planlægningsområdet, kan du tilføje det i projektteamet uden tildelinger.
 
## <a name="book-from-a-new-resource-requirement"></a>Reservere fra et nyt ressourcekrav
Benyt følgende fremgangsmåde til at reservere fra et nyt ressourcekrav. 

1. Gå til **Ressourcekrav**, og vælg derefter **Ny** for at oprette et nyt ressourcekrav.

2. Vælg et projekt, som kravet skal knyttes til i projektet, under fanen **Projekt**.
 
    Det nyoprettede krav vises i planlægningsområdet som et **åbent krav**, som du kan opfylde.

3. Reservér ressourcen for at føje den til projektteamet.

4. Nu, hvor ressourcen er reserveret, skal du tildele opgaver manuelt.



[!INCLUDE[footer-include](../includes/footer-banner.md)]