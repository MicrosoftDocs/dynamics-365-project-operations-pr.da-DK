---
title: Foreslå projektressourcer
description: Dette emne indeholder oplysninger om forslag til projektressourcer.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: fc18c5cbd1a564e186f533a3c0f972e60229a6d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587441"
---
# <a name="propose-project-resources"></a>Foreslå projektressourcer

[!include [banner](../includes/psa-now-project-operations.md)]

Personalechefer kan foreslå en ressource til projektlederen ved hjælp af en ressourceanmodning.

1. Vælg **Find ressourcer** i anmodningsgitteret eller i selve anmodningen.
2. På siden **Planlægningsassistent** skal du vælge ressourcen og derefter i ruden **Opret ressourcereservation** i feltet **Reservationsstatus** vælge **Reservér**.

    ![Foreslået ressource er valgt.](media/Resource-Management-image62.png)

Følgende statusopdateringer forekommer:

- På siden **Planlægningsassistent** opdateres statusindikatorerne for at indikere, at reservationen er foreslået, ikke definitivt reserveret.

    ![Statusindikatorer for foreslået reservation på siden Planlægningsassistent.](media/Resource-Management-image63.png)

- På ressourceanmodningen ændres status til **Skal gennemses**.

    ![Ressourceanmodningsstatus er ændret til Skal gennemses.](media/Resource-Management-image64.png)

- På fanen **Team** for projektet er det generiske teammedlems værdi for **Anmodningsstatus** ændret til **Skal gennemses**.

    ![Det generiske teammedlems anmodningsstatus ændret til Skal gennemses på fanen Team.](media/Resource-Management-image48.png)

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

![Visning af tidsforbrug for ressource.](media/Resource-Management-image65.png)

Hver celle i gitteret repræsenterer den fakturerbare udnyttelsesprocent for ressourcen i en periode, f.eks. en dag, uge eller måned. Følgende formler bruges til farvning af cellerne:

- **Grøn:** Fakturerbart tidsforbrug \>= Resourcens måltidsforbrug
- **Gul:** Mål-tidsforbrug – 20 \<= Fakturerbart tidsforbrug \< Mål-tidsforbrug
- **Rød:** Fakturerbart tidsforbrug \< Mål-tidsforbrug – 20

Da visningen **Ressourceforbrug** er baseret på planlægningsområdet, kan du bruge filtreringsfunktionerne i planlægningsområdet til at filtrere resultaterne.

Gitteret kræver, at du angiver et mål-tidsforbrug for enten rolle eller den enkelte ressource. Du konfigurerer dette ved at gå til **Ressourcer** \> **Ressourceroller**.

Derudover skal der tildeles en standardrolle til hver af de pågældende reserverbare ressourcer. Gå til **Ressourcer** \> **Ressourcer**. På fanen **Project Service** skal du kontrollere, at der er defineret en ressourcerolle, og at feltet **Er standard** herfor er angivet til **Ja**. Du kan tilføje flere roller, hvor **Er standard =** nej. Den rolle, hvor **Er standard = Ja**, bruges til at evaluere ressourcens tidsforbrug i forhold til destinationen for den pågældende rolle.

![Standardrollesæt.](media/Resource-Management-image67.png)

På fanen **Project Service** kan du også angive en individuel mål-tidsforbrug for ressourcen. I beregningen af tidsforbruget bruger derefter denne mål-tidsforbrug til at evaluere ressourcens mål i stedet for målet for ressourcens standardrolle.

Tidsforbrug vises kun for en ressource, hvis den pågældende ressource har godkendt fakturerbar tid i løbet af den periode, der vises i gitteret.

## <a name="resource-availability"></a>Ressourcetilgængelighed

Det er vigtigt, at personalechefer kan få vist tilgængeligheden af ressourcer og opdatere reservationer. I visse tilfælde er der ingen formel efterspørgsel (ressourceanmodning), men ressourcestyringen skal reagere på et ikke-planlagt behov, der kommer gennem kanaler, f.eks. e-mail, telefonopkald eller onlinemeddelelse. Personalechefer bruger planlægningsområdet til at opdatere ressourcer og reservationer.

Ressourcens arbejdstimer bruges som udgangspunkt for beregning af tilgængeligheden af en ressource. Ressourcereservationer forbruger ressourcernes kapacitet.

![Planlægningsområde.](media/Resource-Management-image68.png)

I planlægningsområdet bruges farver og skygge til at vise reservationer, tilgængelighed og overreservationer samt statussen for reservationer. En indstilling i indstillingerne for planlægningsområdet giver dig mulighed for at få vist en forklaring.

Hvis der vises en højrepil ud for en enkeltstående ressource i planlægningsområdet, kan ressourcen udvides til at få vist oplysninger om det arbejde, som ressourcen er reserveret til.

![Reserverbar ressource udvidet på planlægningsområdet.](media/Resource-Management-image69.png)

Da Dynamics 365 Project Service Automation bruger Universal Resource Scheduling-programmet, og du også har Dynamics 365 Field Service installeret, kan du få vist oplysninger om ressourcereservationer for projekter, arbejdsordrer og andre objekter, som du har udvidet planlægningen til.

![Oplysninger om ressourcereservationer for projekter og arbejdsordrer.](media/Resource-Management-image70.png)

Hvis du vil have vist flere oplysninger om en enkelt ressource, skal du højreklikke på den for at åbne ressourcekortet.

![Ressourcekort.](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
