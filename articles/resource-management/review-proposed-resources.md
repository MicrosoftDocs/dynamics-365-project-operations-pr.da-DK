---
title: Gennemse foreslåede ressourcer
description: Dette emne indeholder oplysninger om, hvordan du foreslår projektressourcer.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897354"
---
# <a name="review-proposed-resources"></a>Gennemse foreslåede ressourcer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Personalechefer kan foreslå en ressource til projektlederen ved hjælp af en ressourceanmodning.

1. Vælg **Find ressourcer** i anmodningsgitteret eller i selve anmodningen.
2. På siden **Planlægningsassistent** skal du vælge ressourcen og derefter i ruden **Opret ressourcereservation** i feltet **Reservationsstatus** vælge **Reservér**.

Følgende statusopdateringer forekommer:

- På siden **Planlægningsassistent** opdateres statusindikatorerne for at indikere, at reservationen er foreslået, ikke definitivt reserveret.
- På ressourceanmodningen ændres status til **Skal gennemses**.
- På fanen **Team** for projektet er det generiske teammedlems værdi for **Anmodningsstatus** ændret til **Skal gennemses**.

Projektlederen kan enten acceptere eller afvise forslaget.

Når personalechefer behandler ressourceanmodninger, kan de benytte en af følgende fremgangsmåder:

- Foreslå flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig for at imødekomme de påkrævede timer. De foreslåede timer deles derefter mellem flere ressourcer, der kan opfylde de krævede timer. I dette scenario må timerne ikke overlappe hinanden.
- Foreslå færre ressourcer end nødvendigt. I dette scenario er den foreslåede ressourcekapacitet mindre end de krævede timer, som anmoderen har angivet. Når anmoderen accepterer de foreslåede ressourcer, oprettes der derfor et uopfyldt ressourcekrav for at registrere det resterende behov.
- Reservér flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig til udførelse af arbejdet.
- Reservere færre ressourcer end nødvendigt. I dette scenario er de reserverede timer færre end de krævede timer. Systemet hjælper dig med at foreslå ressourcer i stedet for reservationer, så anmoderen kan kontrollere og holde styr på det resterende behov.

## <a name="billable-utilization"></a>Fakturerbart tidsforbrug

Ressourcer kan have et fakturerbart tidsforbrug for et mål. Dette mål-tidsforbrug er enten defineret som en attribut i en ressources standardrolle eller angivet på posten for den individuelle, reserverbare ressource. Beregningerne af tidsforbrug er baseret på det faktiske antal timer, som ressourcer har rapporteret ved hjælp af godkendte tidsregistreringer.

Følgende formler bruges til at beregne forbrug:

- Fakturerbart tidsforbrug = fakturerbare faktiske timer ÷ ressourcekapacitet
- Ikke-fakturerbar tidsforbrug = faktisk tid med faktureringstype-ID = ikke-fakturerbar, komplementær eller ikke tilgængelig ÷ ressourcekapacitet
- Intern = faktisk tid uden salgskontrakt ÷ ressourcekapacitet
- Ressourcekapacitet = ressourcens arbejdstimer – ikke til stede – fridage

Du kan finde visningen **Ressourceforbrug** i ruden **Ressourcer.**

Hver celle i gitteret repræsenterer den fakturerbare udnyttelsesprocent for ressourcen i en periode, f.eks. en dag, uge eller måned. Følgende formler bruges til farvning af cellerne:

- **Grøn:** Fakturerbart tidsforbrug \>= Resourcens måltidsforbrug
- **Gul:** Mål-tidsforbrug – 20 \<= Fakturerbart tidsforbrug \< Mål-tidsforbrug
- **Rød:** Fakturerbart tidsforbrug \< Mål-tidsforbrug – 20

Da visningen **Ressourceforbrug** er baseret på planlægningsområdet, kan du bruge filtreringsfunktionerne i planlægningsområdet til at filtrere resultaterne.

Gitteret kræver, at du angiver et mål-tidsforbrug for enten rolle eller den enkelte ressource. Du konfigurerer dette ved at gå til **Ressourcer** \> **Ressourceroller**.

Derudover skal der tildeles en standardrolle til hver af de pågældende reserverbare ressourcer. Gå til **Ressourcer** \> **Ressourcer**. På fanen **Project Service** skal du kontrollere, at der er defineret en ressourcerolle, og at feltet **Er standard** herfor er angivet til **Ja**. Du kan tilføje flere roller, hvor **Er standard =** nej. Den rolle, hvor **Er standard = Ja**, bruges til at evaluere ressourcens tidsforbrug i forhold til destinationen for den pågældende rolle.

På fanen **Project Service** kan du også angive en individuel mål-tidsforbrug for ressourcen. I beregningen af tidsforbruget bruger derefter denne mål-tidsforbrug til at evaluere ressourcens mål i stedet for målet for ressourcens standardrolle.

Tidsforbrug vises kun for en ressource, hvis den pågældende ressource har godkendt fakturerbar tid i løbet af den periode, der vises i gitteret.

## <a name="resource-availability"></a>Ressourcetilgængelighed

Det er vigtigt, at personalechefer kan få vist tilgængeligheden af ressourcer og opdatere reservationer. I visse tilfælde er der ingen formel efterspørgsel (ressourceanmodning), men ressourcestyringen skal reagere på et ikke-planlagt behov, der kommer gennem kanaler, f.eks. e-mail, telefonopkald eller onlinemeddelelse. Personalechefer bruger planlægningsområdet til at opdatere ressourcer og reservationer.

Ressourcens arbejdstimer bruges som udgangspunkt for beregning af tilgængeligheden af en ressource. Ressourcereservationer forbruger ressourcernes kapacitet.

I planlægningsområdet bruges farver og skygge til at vise reservationer, tilgængelighed og overreservationer samt statussen for reservationer. En indstilling i indstillingerne for planlægningsområdet giver dig mulighed for at få vist en forklaring.

Hvis der vises en højrepil ud for en enkeltstående ressource i planlægningsområdet, kan ressourcen udvides til at få vist oplysninger om det arbejde, som ressourcen er reserveret til.

Da Dynamics 365 Project Operations bruger Universal Resource Scheduling-programmet, og du også har Dynamics 365 Field Service installeret, kan du få vist oplysninger om ressourcereservationer for projekter, arbejdsordrer og andre objekter, som du har udvidet planlægningen til.

Hvis du vil have vist flere oplysninger om en enkelt ressource, skal du højreklikke på den for at åbne ressourcekortet.

