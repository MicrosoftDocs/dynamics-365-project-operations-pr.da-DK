---
title: Gennemse foreslåede ressourcer
description: Denne artikel indeholder oplysninger om, hvordan du foreslår projektressourcer.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183967"
---
# <a name="review-proposed-resources"></a>Gennemse foreslåede ressourcer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Personalechefer kan foreslå en ressource til projektlederen ved hjælp af en ressourceanmodning.

Hvis du vil have vist de foreslåede ressourcer, skal du følge disse trin:

1. I gitteret **Anmodning** eller i selve anmodningen skal du vælge **Find ressourcer**.
2. På siden **Planlægningsassistent** skal du vælge ressourcen og derefter bekræfte, at alle foreslåede timer er inkluderet i den foreslåede reservation.
3. I ruden **Opret ressourcereservation** skal du angive feltet **Reservationsstatus** til **Foreslået** og derefter vælge **Reserver**.

    > [!NOTE]
    > Din angivelse af **Reservationsstatus** til **Foreslået** reserverer ikke ressourcen endeligt, og den generiske ressource erstattes ikke med det navngivne teammedlem.

    Følgende statusopdateringer forekommer:

    - På siden **Planlægningsassistent** opdateres statusindikatorerne for at indikere, at reservationen er foreslået, ikke definitivt reserveret.
    - På ressourceanmodningen bør gennemseeren af anmodningen ændre status til **Skal gennemses**.
    - På fanen **Team** for projektet ændres det generiske teammedlems værdi for **Anmodningsstatus** automatisk til **Skal gennemses**.

Projektlederen kan acceptere eller afvise forslaget.

Når personalechefer behandler ressourceanmodninger, kan de benytte en af følgende fremgangsmåder:

- Foreslå flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig for at imødekomme de påkrævede timer. De foreslåede timer deles derefter mellem flere ressourcer, der kan opfylde de krævede timer. I dette scenario må timerne ikke overlappe hinanden.
- Foreslå færre ressourcer end nødvendigt. I dette scenario er den foreslåede ressourcekapacitet mindre end de krævede timer, som anmoderen har angivet. Når anmoderen accepterer de foreslåede ressourcer, oprettes der et uopfyldt ressourcekrav for at registrere det resterende behov.
- Reservér flere ressourcer for at opfylde efterspørgslen, hvis der ikke er en enkelt ressource tilgængelig til udførelse af arbejdet.
- Reservere færre ressourcer end nødvendigt. I dette scenario er de reserverede timer færre end de krævede timer. Systemet hjælper dig med at foreslå ressourcer i stedet for reservationer, så anmoderen kan kontrollere og holde styr på det resterende behov.

## <a name="resource-availability"></a>Ressourcetilgængelighed

Personalechefer skal kunne få vist tilgængeligheden af ressourcer og opdatere reservationer. I visse tilfælde er der ingen formel efterspørgsel (ressourceanmodning). En personalechef skal dog reagere på en ikke-planlagt efterspørgsel, der kommer via andre kanaler såsom mails, telefonopkald eller chatbeskeder. Personalechefer bruger **Planlægningsområdet** til at opdatere ressourcer og reservationer.

Ressourcens arbejdstimer bruges som udgangspunkt til at beregne tilgængeligheden af en ressource. Ressourcereservationer forbruger ressourcernes kapacitet.

I **Planlægningsområdet** bruges farver og skygge til at vise reservationer, tilgængelighed, overreservationer og statussen for reservationer. En indstilling i **Planlægningsoversigten** giver dig mulighed for at få vist en forklaring.

Hvis der vises en højrepil ud for en enkeltstående ressource i **Planlægningsområdet**, kan ressourcen udvides for at få vist oplysninger om det arbejde, som ressourcen er reserveret til.

Da Dynamics 365 Project Operations bruger Universal Resource Scheduling-programmet, og du også har Dynamics 365 Field Service installeret, kan du få vist oplysninger om ressourcereservationer for projekter, arbejdsordrer og andre objekter, som du har udvidet planlægningen til.

Hvis du vil have vist yderligere oplysninger om en enkelt ressource, skal du højreklikke på den for at åbne ressourcekortet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
