---
title: Tilknyt projekter og opgaver til en projektbaseret kontraktlinje - lille
description: Dette emne indeholder oplysninger om, hvordan du tilføjer og fjerner projekter og opgaver til en kontraktlinje.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c29872ef3d62780eea3c0eda48c8fd2a9af4b1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272786"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a>Tilknyt projekter og opgaver til en projektbaseret kontraktlinje - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

På projektbaserede kontraktlinjer kan du knytte bestemte opgaver i et projekt til kontraktlinjen.

Når du knytter bestemte opgaver til en kontraktlinje, gælder faktureringsmetoden, faktureringsmuligheder, grænser, der ikke må overskrides, og de kunder, der er defineret på kontraktlinjen, kun for bestemte opgaver.

Hvis du har et scenario, hvor en fase i et projekt, f.eks. prototypefasen, er fast pris, og alle andre faser er tid og materiale, kan du knytte prototypefasen og alle de tilknyttede underordnede opgaver til kontraktlinjen for den pågældende fase med en faktureringsmetode med fast pris.

Alle andre faser i dit projekts arbejdsopgavehierarki (WBS) kan knyttes til tids- og materialebaserede kontraktlinjer.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Knyt opgaver til projektbaserede kontraktlinjer

Opgaver kan knyttes til kontraktlinjer under fanen **Fakturerbare opgaver** på siden **Kontraktlinjer** eller fra fanen **Opgavefakturering** på siden **Projekt**.

### <a name="from-the-contract-line-page"></a>Fra kontraktlinjesiden

Benyt følgende fremgangsmåde for at knytte projektopgaver til kontraktlinjen fra fanen **Fakturerbare opgaver** på siden **Kontraktlinje**.

1. På en projektbaseret kontraktlinjes fane med **Generelt** skal du sikre dig, at feltet **Projekt** er udfyldt.
2. I feltet **Inkluder opgaver** skal du vælge **Kun markerede opgaver**.
3. Gem dine ændringer. Formularen opdateres, og fanen **Fakturerbare opgaver** vil være synlig.
4. Vælg fanen **Fakturerbare opgaver**, og vælg **Tilføj en kontraktlinjeopgave** i undert.
5. På siden **Kontraktlinjeopgaver** skal du i rullelisten for **Opgaver** vælge opgaven. 
6. Angiv oplysningerne i feltet **Faktureringstype**, og vælg derefter **Gem og luk**. Den valgte opgave er knyttet til kontraktlinjen.

> [!NOTE]
> Dette er ikke den mest optimale oplevelse til at knytte projektopgaver til kontraktlinjer. De enkelte projekter skal tilknyttes manuelt i denne oplevelse. Den foretrukne måde er at bruge fanen **Opgavefakturering** på siden **Projekt**.

### <a name="from-the-project-page"></a>Fra projektsiden

Dette er den optimale metode til at knytte opgaver til kontraktlinjer. Du kan vælge flere opgaver og knytte alle dem og deres underordnede opgaver til den valgte kontraktlinje. Benyt følgende fremgangsmåde for at knytte opgaver til kontraktlinjen fra siden **Projekt**.

1. På en projektbaseret kontraktlinjes fane med **Generelt** skal du sikre dig, at feltet **Projekt** er udfyldt.
2. I feltet **Inkluder opgaver** skal du vælge **Kun markerede opgaver**.
3. Gem den projektbaserede kontraktlinje. Formularen opdateres, og fanen **Fakturerbare opgaver** vil være synlig. Dette er blot til verificering.
4. På den projektbaserede kontraktlinjes fane med **Generelt** skal du i feltet **Projekt** vælge projektlinket.
5. På siden **Projektoplysninger** skal du vælge fanen **Opsætning af opgavefakturering**.
6. Der vises to gitre: Et gitter er til kontraktlinjer, der gælder for hele projektet. Det andet gitter gælder for en opgavespecifik faktureringsopsætning. Vælg en eller flere opgaver i det andet gitter, og vælg derefter **Tilknyt kontraktlinjer**.
7. Vælg en kontraktlinje på rullelisten på den dialogside, der vises.
8. Brug rullelisten **Faktureringstype** til at markere opgaverne som fakturerbare eller ikke-fakturerbare.
9. Markér afkrydsningsfeltet for at angive, om tilknytningen også skal inkludere underordnede opgaver for de valgte opgaver. Hvis du markerer afkrydsningsfeltet, knyttes de underordnede opgaver for de valgte opgaver til kontraktlinjen.
10. Vælg **OK** for at lukke dialogboksen.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Fjern tilknyttede opgaver fra projektbaserede kontraktlinjer

### <a name="from-the-contract-line-page"></a>Fra kontraktlinjesiden

Benyt følgende fremgangsmåde for at fjerne tilknyttede projektopgaver fra kontraktlinjen på fanen **Fakturerbare opgaver** på siden **Kontraktlinje**.

1. På fanen **Fakturerbare opgaver** skal du vælge **Slet en kontraktlinjeopgave**.
2. En advarselsmeddelelse angiver, at fjernelse af denne tilknytning kan resultere i tilbageførsel af faktiske værdier, der tidligere er blevet registreret på opgaven. Vælg **OK** i dialogboksen for at fjerne tilknytningen mellem opgaven og den projektbaserede kontraktlinje. 

> [!NOTE]
> Dette sletter ikke opgaven fra projektet. I stedet fjernes opgavens tilknytning fra den projektbaserede kontraktlinje.

### <a name="from-the-project-page"></a>Fra projektsiden

Dette er den mest optimale oplevelse til at fjerne tilknyttede opgaver fra kontraktlinjer. Du kan vælge flere opgaver og fjerne tilknytningen for dem alle og deres underordnede opgaver fra den valgte kontraktlinje. Benyt følgende fremgangsmåde for at fjerne tilknyttede opgaver fra kontraktlinjen.

1. Fra den projektbaserede kontraktlinjes fane med **Generelt** skal du i feltet **Projekt** klikke på projektlinket.
2. På siden **Projektoplysninger** skal du vælge fanen **Opsætning af opgavefakturering**.
3. Der findes to gitre på siden. Et gitter bruges til kontraktlinjer, der gælder for hele projektet, og det andet gælder for opgavespecifik faktureringsopsætning. Vælg en eller flere opgaver i det andet gitter, og vælg derefter **Fjern tilknyttede kontraktlinjer**.
4. Vælg en kontraktlinje på rullelisten på den dialogside, der vises.
5. Markér afkrydsningsfeltet for at angive, om tilknytningen også skal fjernes fra eventuelle underordnede opgaver for de valgte opgaver. Hvis du markerer afkrydsningsfeltet, fjernes de tilknyttede underordnede opgaver for de valgte opgaver fra kontraktlinjen.
6. Vælg **OK**. En advarselsmeddelelse angiver, at fjernelse af denne tilknytning kan resultere i tilbageførsel af faktiske værdier, der tidligere er blevet registreret på opgaven. Vælg **OK** i advarselsdialogen for at fjerne tilknytningen mellem opgaven og den projektbaserede kontraktlinje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]