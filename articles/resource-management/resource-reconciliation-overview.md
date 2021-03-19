---
title: Oversigt over ressourceafstemning
description: Dette emne indeholder oplysninger, der kan hjælpe dig med at sikre, at ressourcereservationer og tildelinger for projekter stemmer overens.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0416e93944e7b6686a0e4da1d633188dd51e590b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279356"
---
# <a name="resource-reconciliation-overview"></a>Oversigt over ressourceafstemning

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

For teammedlemmer er reservationer og tildelinger løst sammenkædet. Med andre ord kan ressourcer have tildelinger og ingen reservationer, eller de kan have reservationer og ingen tildelinger. Ideelt set skal reservationer og tildelinger justeres, så ressourcer har bindende kapacitet til at udføre opgavetildelingerne. Reservationerne kan dog muligvis være baseret på tilgængelighed, og opgavetidspunkter kan ændres, efterhånden som projektet fortsætter. Derfor giver den løse sammenkædning mellem reservationer og tildelinger fleksibilitet.

Fanen **Afstemning** på siden **Projekter** gør, at projektledere kan afstemme teammedlemmernes reservationer og tildelinger til projektgrupper.

Fanen **Afstemning** viser reservationer og tildelinger helt ned til niveauet for de enkelte opgavetildelinger for hvert teammedlemmer. Timer vises i celler, der repræsenterer tidsperioder fra måneder til dage. Fanen viser også en nettototal for projektet sammen med en kolonne med **Total**.

For hver ressource beregner fanen **Afstemning** forskellen mellem teammedlemmets reservationer og en akkumulering af teammedlemmets opgavetildelinger. Ideelt skal forskellen være 0 (nul). Det vil sige, at der ikke bør være nogen forskel mellem reservationer og tildelinger. Forskelle er farvede og nedtonede for at henlede opmærksomheden på to forhold:

- **Manglende reservation** – der opstår manglende reservation, når en ressource har flere tildelinger end reservationer. Da kapaciteten ikke er reserveret, vil en projektleder muligvis rette dette forhold ved at forlænge reservationer af ressourcen for at dække underskuddet.
- **Overskydende reservationer** – Der forekommer overskydende reservationer, når en ressource er blevet reserveret til projektet, men ikke er tildelt opgaver. Dette forhold kan være acceptabelt i tilfælde, hvor ressourcen blev reserveret til projektet, før opgavetildeling fandt sted. I andre tilfælde, hvor der ikke er planer om at tildele ressourcen til opgaver, bør projektlederen overveje at annullere ressourcens reservationer. På den måde kan kapaciteten bruges til et andet projekt.

Når du i visse tilfælde får vist tiden på et højere niveau end dagsniveau (f.eks. månedsniveau), kan du muligvis se en nettoforskel på nul for en ressource (med andre ord er reservationer lige med tildelinger). Men hvis du får vist tiden på ugeniveau, kan du muligvis se, at der er tildelinger på 0 timer og reservationer på 40 timer i den første uge, men tildelinger på 40 timer og reservationer på nul timer i løbet af den anden uge. Generelt afstemmes reservationerne og tildelingerne, men de er forskellige fra den ene uge til den næste.

Når du får vist tiden på højere niveauer, har celler på fanen **Afstemning** en indikator, der giver dig besked om, at der er forskelle på lavere niveauer. Ved at dobbeltklikke på en celle, kan du zoome ind for at få vist forskellen. Du kan derefter vælge og trykke på (eller højreklikke) for at zoome ud. Hvis du vælger en ressource og derefter bruger kontrolelementet **Næste difference** på værktøjslinjen for gitteret, kan du gå til den næste forskel mellem reservationer og tildelinger for den pågældende ressource. Du kan derefter bruge kontrolelementet **Forrige difference** til at gå tilbage. Du kan også slå differenceindikatoren og funktionsmåden for navigation fra under **Indstillinger**.

Hvis du har opgavetildelinger for en ressource men ingen reservationer, skal du under fanen **Afstemning** på siden **Projekter** vælge den manglende reservation og derefter vælge **Udvid reservation**. Den dialogboks for **Udvid reservation**, der vises, angiver den reservation, der er nødvendig for at løse manglen på ressource. Dialogboksen viser også ressourcens eksisterende reservationer på tværs af alle projekter eller andre objekter, der kan planlægges. Hvis du vælger **OK** for at oprette reservationen for ressourcen, uanset den pågældende ressources tilgængelighed, kan det medføre overreservation.

Reservationer, der oprettes via handlingen **Udvid reservation**, er knyttet til det primære projektkrav. Når en udvidelse startes, kan det specifikke krav, der skal udvides, ikke bestemmes, da ressourcen kan være knyttet til mere end ét krav til projektet.

Projektlederen eller ressourceadministratoren kan derefter bruge planlægningsområdet til at administrere de situationer, hvor en ressource overreserveres i forhold til dens kapacitet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]