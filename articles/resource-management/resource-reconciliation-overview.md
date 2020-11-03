---
title: Oversigt over ressourceafstemning
description: Dette emne indeholder oplysninger om, hvordan du sikrer, at reservation af ressourcer og tildelinger til opgaver er afstemt.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074114"
---
# <a name="resource-reconciliation-overview"></a>Oversigt over ressourceafstemning

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

For teammedlemmer er reservationer og tildelinger løst sammenkædet. Med andre ord kan ressourcer have tildelinger men ingen reservationer, eller de kan have reservationer men ingen tildelinger. Ideelt set skal reservationer og tildelinger justeres, så ressourcer har bindende kapacitet til at udføre opgavetildelingerne. Reservationerne kan dog muligvis være baseret på tilgængelighed, og opgavetidspunkter kan ændres, efterhånden som projektet fortsætter. Derfor giver den løse sammenkædning mellem reservationer og tildelinger fleksibilitet.

Fanen **Afstemning** på formularen **Projekt** gør det muligt for projektledere at afstemme teammedlemmernes reservationer og tildelinger af disse til projektteams.

Fanen **Afstemning** viser også reservationer og tildelinger helt ned på niveauet for de enkelte opgavetildelinger for hvert teammedlemmer. Timer vises i celler, der repræsenterer tidsperioder fra måneder og ned til dage.

Fanen viser også en nettototal for projektet sammen med en kolonne med **Total**.

For hver ressource beregner fanen forskellen mellem teammedlemmets reservationer og en akkumulering af teammedlemmets opgavetildelinger. Ideelt skal forskellen være 0 (nul). Det vil sige, at der ikke bør være nogen forskel mellem reservationer og tildelinger. Forskelle er farvede og nedtonede for at henlede opmærksomheden på to forhold:

- **Manglende reservation** – der opstår manglende reservation, når en ressource har flere tildelinger end reservationer. Da denne kapacitet ikke er reserveret, vil en projektleder muligvis rette dette forhold ved at forlænge reservationer af ressourcen for at dække underskuddet.
- **Overskydende reservationer** – Der forekommer overskydende reservationer, når en ressource er blevet reserveret til projektet, men ikke er tildelt opgaver. Dette forhold kan være acceptabelt i de tilfælde, hvor ressourcen blev reserveret til projektet, før opgavetildeling fandt sted. I andre tilfælde er ressourcen dog ikke planlagt til at blive tildelt til opgaver. I disse tilfælde skal projektlederen overveje at annullere reservationerne af ressourcen, så kapaciteten kan bruges til et andet projekt.

Når du i visse tilfælde får vist tiden på et højere niveau end dagsniveau (f.eks. månedsniveau), kan du muligvis se en nettoforskel på nul for en ressource (med andre ord reservationer = tildelinger). Men hvis du får vist tiden på ugeniveau, kan du muligvis se, at der er tildelinger på 0 timer og reservationer på 40 timer i den første uge, men tildelinger på 40 timer og reservationer på nul timer i løbet af den anden uge. Generelt afstemmes reservationerne og tildelingerne, men de er forskellige fra den ene uge til den næste.

Når du får vist tiden på højere niveauer, har fanen **Afstemning** en indikator, der giver dig besked om, at der er forskelle på lavere niveauer. Når du dobbeltklikker på en celle, kan du zoome ind for at få vist forskellen. Du kan derefter højreklikke for at zoome ud. Hvis du vælger en ressource og derefter bruger kontrolelementet **Næste difference** på værktøjslinjen for gitteret, kan du gå til den næste forskel mellem reservationer og tildelinger for den pågældende ressource. Du kan derefter bruge kontrolelementet **Forrige difference** til at gå tilbage. Du kan også slå differenceindikatoren og funktionsmåden for navigation fra under **Indstillinger**.


Hvis du har opgavetildelinger for en ressource men ingen reservationer, skal du under fanen **Afstemning** på siden **Projekter** vælge den manglende reservation og derefter vælge **Udvid reservation**. Dialogboksen **Udvid reservation** vises og angiver den reservation, der skal bruges for at løse manglen på ressource. Den viser også ressourcens eksisterende reservationer på tværs af alle projekter eller andre objekter, der kan planlægges. Hvis du vælger **OK** for at oprette reservationen for ressourcen, uanset den pågældende ressources tilgængelighed, kan det medføre overreservation.

Projektlederen eller ressourcestyringen kan derefter bruge planlægningsområdet til at administrere de situationer, hvor en ressource overreserveres i forhold til dens kapacitet.

