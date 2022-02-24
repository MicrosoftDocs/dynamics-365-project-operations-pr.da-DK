---
title: Gennemse foreslåede ressourcer
description: Dette emne indeholder oplysninger om, hvordan du foreslår projektressourcer.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401166"
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

## <a name="resource-availability"></a>Ressourcetilgængelighed

Det er vigtigt, at personalechefer kan få vist tilgængeligheden af ressourcer og opdatere reservationer. I visse tilfælde er der ingen formel efterspørgsel (ressourceanmodning), men ressourcestyringen skal reagere på et ikke-planlagt behov, der kommer gennem kanaler, f.eks. e-mail, telefonopkald eller onlinemeddelelse. Personalechefer bruger planlægningsområdet til at opdatere ressourcer og reservationer.

Ressourcens arbejdstimer bruges som udgangspunkt for beregning af tilgængeligheden af en ressource. Ressourcereservationer forbruger ressourcernes kapacitet.

I planlægningsområdet bruges farver og skygge til at vise reservationer, tilgængelighed og overreservationer samt statussen for reservationer. En indstilling i indstillingerne for planlægningsområdet giver dig mulighed for at få vist en forklaring.

Hvis der vises en højrepil ud for en enkeltstående ressource i planlægningsområdet, kan ressourcen udvides til at få vist oplysninger om det arbejde, som ressourcen er reserveret til.

Da Dynamics 365 Project Operations bruger Universal Resource Scheduling-programmet, og du også har Dynamics 365 Field Service installeret, kan du få vist oplysninger om ressourcereservationer for projekter, arbejdsordrer og andre objekter, som du har udvidet planlægningen til.

Hvis du vil have vist flere oplysninger om en enkelt ressource, skal du højreklikke på den for at åbne ressourcekortet.

