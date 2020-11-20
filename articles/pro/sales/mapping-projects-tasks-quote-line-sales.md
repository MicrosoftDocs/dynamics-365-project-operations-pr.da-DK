---
title: Tilknyt projekter og opgaver til en projektbaseret tilbudslinje
description: Dette emne indeholder oplysninger om, hvordan du knytter projekter og opgaver til en projektbaseret opgavelinje.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130706"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Tilknyt projekter og opgaver til en projektbaseret tilbudslinje

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

På projektbaserede tilbudslinjer kan du tilknytte de specifikke opgaver for et projekt, der allerede er knyttet til en tilbudslinje.

Når du knytter opgaver til en tilbudslinje, finder følgende elementer, du har defineret på tilbudslinjen, kun anvendelse for de pågældende opgaver:

- Faktureringsmetode
- Indstillinger for fakturerbarhed
- Grænser, der ikke må overskrides
- Kunder

Du kan f.eks. have et projekt, hvor den ene fase er fast pris, og alle andre faser er tid og materialer. I dette tilfælde kan du knytte den første fase og alle dens underordnede opgaver til tilbudslinjen for den pågældende fase med en fast pris-faktureringsmetode. Derefter kan du knytte alle de andre faser til den tids- og materialebaserede tilbudslinje.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Tilknyt opgaver til projektbaserede tilbudslinjer

Du kan tilknytte opgaver til tilbudslinjer fra følgende placeringer:

- Siden **Projekt** > fanen **Opgavefakturering** (optimal)
- Siden **Tilbudslinje** > fanen **Fakturerbare opgaver** 

### <a name="from-the-project-page"></a>Fra projektsiden

På siden **Projekt** får du den optimale oplevelse, når du knytter opgaver til tilbudslinjer. Du kan bruge denne side til at vælge flere opgaver og knytte dem alle samt deres underordnede opgaver til den valgte tilbudslinje.

1. På en projektbaseret tilbudslinjes fane **Generelt** kan du verificere, at feltet **Projekt** er udfyldt.
2. I feltet **Medtag opgaver** skal du vælge **Kun valgte opgaver**.
3. Gem den projektbaserede tilbudslinje. Når formularen opdateres, vises fanen **Fakturerbare opgaver**.
4. På fanen **Generelt** skal du vælge linket til projektet fra feltet **Projekt**.
5. På siden **Projekt** skal du vælge fanen **Opgavefakturering**.
6. I det andet gitter, der gælder for opgavespecifik faktureringsopsætning, skal du vælge en eller flere opgaver og derefter vælge **Tilknyt tilbudslinjer**.
7. Vælg en tilbudslinje, der viser projektbaserede tilbudslinjer på tilbuddet, på den dialogside, der vises.
8. I feltet **Faktureringstype** skal du angive, om disse opgaver er fakturerbare eller ikke-fakturerbare.
9. Markér afkrydsningsfeltet for at angive, om tilknytningen skal omfatte underordnede opgaver for de valgte opgaver. Hvis du markerer afkrydsningsfeltet, knyttes de underordnede opgaver for de valgte opgaver til tilbudslinjen.
10. Vælg **OK** for at lukke dialogboksen.

### <a name="from-the-quote-line-page"></a>Fra tilbudslinjesiden

Du kan knytte projektopgaver til tilbudslinjer fra fanen **Fakturerbare opgaver** på siden **Tilbudslinje**.

>[!NOTE]
>Det optimale sted at knytte projektopgaver til tilbudslinjer findes under fanen **Opgavefakturering** på **Projekt**-siden. Hvis du knytter opgaver til fanen **Fakturerbare opgaver** på siden med **Tilbudslinje**, skal du tilknytte hvert enkelt projekt manuelt.

1. På en projektbaseret tilbudslinjes fane **Generelt** kan du verificere, at der er valgt et projekt i feltet **Projekt**.
2. I feltet **Medtag opgaver** skal du vælge **Kun valgte opgaver**.
3. Gem den projektbaserede tilbudslinje. Når formularen opdateres, vises fanen **Fakturerbare opgaver**.
4. På fanen **Fakturerbare opgaver** skal du vælge **Tilføj en tilbudslinjeopgave**.
5. På siden **Tilbudslinjeopgave** skal du i feltet **Opgaver** markere opgaven, og i feltet **Faktureringstype** skal du vælge **Gem**. 
6. Luk siden. Den valgte opgave er nu knyttet til tilbudslinjen.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Fjer tilknytning mellem opgaver og projektbaserede tilbudslinjer

### <a name="from-the-project-page"></a>Fra projektsiden

Denne metode giver dig den mest optimale oplevelse, når du fjerner tilknytningen mellem opgaver og tilbudslinjer. Du kan vælge flere opgaver og fjerne tilknytningen for dem alle samt deres underordnede opgaver til den valgte tilbudslinje.

1. På en projektbaseret tilbudslinjes fane **Generelt** kan du i feltet **Projekt** vælge projektlinket.
2. På siden **Projekt** skal du vælge fanen **Opgavefakturering**.
3. I det andet gitter, der gælder for opgavespecifik faktureringsopsætning, skal du vælge en eller flere opgaver og derefter vælge **Fjern tilknytning til tilbudslinjer**.
4. Vælg en tilbudslinje på den viste dialogside.
5. Markér afkrydsningsfeltet for at angive, hvorvidt tilknytningen også skal fjernes fra underordnede opgaver for de valgte opgaver. Hvis du markerer afkrydsningsfeltet, fjernes tilknytningen mellem de underordnede opgaver for de valgte opgaver og tilbudslinjen også.
6. Vælg **OK**. Der vises en advarsel om, at hvis du fjerner denne tilknytning, kan de faktiske oplysninger, der tidligere er registreret for opgaven, blive tilbageført. 
7. Vælg **OK** for at fortsætte og fjerne tilknytningen mellem opgaven og den projektbaserede tilbudslinje.

### <a name="from-the-quote-line-page"></a>Fra tilbudslinjesiden

Du kan også fjerne tilknytningen mellem projektopgaver og tilbudslinjer fra fanen **Fakturerbare opgaver** på siden **Tilbudslinje**.

1. På fanen **Fakturerbare opgaver** skal du vælge **Slet en tilbudslinjeopgave**.
2. Vælg **OK**. Der vises en advarsel om, at hvis du fjerner denne tilknytning, kan de faktiske oplysninger, der tidligere er registreret for opgaven, blive tilbageført. 
3. Vælg **OK** for at fortsætte og fjerne tilknytningen mellem opgaven og den projektbaserede tilbudslinje.

>[!NOTE]
> Denne procedure sletter ikke opgaven fra projektet. Det er kun opgavetilknytningen, der fjernes fra den projektbaserede tilbudslinje.
