---
title: Projektprognoser og budgetter
description: Microsoft Dynamics 365 Finance indeholder projektprognoser og projektbudgetter, så du kan administrere og kontrollere dine projekter.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2685e99800ef6fd0b613377271259da0da805aad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289407"
---
# <a name="project-forecasts-and-budgets"></a>Projektprognoser og budgetter

[!include [banner](../includes/banner.md)]

Du kan administrere og styre dine projekter på to måder: projektprognoser og projektbudgetter. 

Brug projektprognoser, hvis din organisation har et operationelt perspektiv, og hvis den fokuserer på indtægter og omkostninger, der er afledt af bestemte transaktioner. Brug projektbudgettering hvis din organisation fokuserer mere på de økonomiske beløb. 

I både projektprognoser og projektbudgetter bruges der prognosemodeller til at opbevare de projekterede transaktionsbeløb. 

Hver metode har sine fordele. Du skal overveje følgende punkter, før du vælger en metode for din organisation.

|   Allokeringsmetode       |           Projektprognose            |        Projektbudgettering                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Periodefordeling**     | Du kan ikke eksplicit tildele transaktioner over en regnskabsperiode. I stedet er prognosen og kontrollen over prognosen baseret på projektets levetid. Da prognoserne er baseret på en bestemt dato, skal perioden udledes fra datoen. | Du kan tildele transaktioner over hele projektet eller en regnskabsperiode. Hvis du allokerer over en periode, kan du overføre ubrugte beløb til næste regnskabsperiode. |
| **Få vist transaktioner**  | Du kan få vist transaktioner i prognoseformularerne, hvor du kan se prognoser for hele virksomheden og for alle projekter uanset hierarkiet. Hvis du vil fokusere på et bestemt projekt, skal du filtrere dataene.                                       | Du kan få vist budgetterede transaktioner for et enkelt projekthierarki. Du kan derfor få vist transaktionsdetaljer for et overordnet projekt eller dets underprojekter.                 |
| **Transaktionsvariabler** | Når du angiver prognosetransaktioner, kan du bruge alle de attributter, der findes for en faktisk transaktion. Dette gør det muligt at få flere detaljer i prognosen. Du kan f.eks. angive oplysninger om antal, arbejdere, varer eller linjeegenskaber.         | Når du angiver budgetdetaljer, kan du kun bruge beløb, kategorier og aktiviteter.                    |
| **Sikkerhed**              | Prognoser er baseret på de transaktioner, du angiver i prognoseformularerne, og kræver ingen processtyringsmekanisme. Alle arbejdere, der har rettigheder til en prognoseformular, kan revidere oplysninger uden godkendelse.                                        | Budgettering bruger arbejdsprocessystemet, som gør det muligt at administrere ændringer og giver dig mulighed for at beholde en oversigt over rettelserne.         |
| **Indtastningstyper**           | Prognosetransaktioner er baseret på antallet af enheder, omkostnings-og salgs enhedspriser.  | Budget detaljer er baseret på beløb, som er opdelt mellem omkostninger og indtægter.                                          |
| **Prognosemodeller**       | Da hver enkel prognose skal knyttes til en model, kan du oprette flere prognosemodeller og også konfigurere undermodeller.           | Projektbudgettering begrænser de prognosemodeller, der bruges til budgettering. Færre prognosemodeller kan være med til at øge ensartetheden i projektioner.                           |
| **Overskridelse af omkostninger**         | Du kan kun tillade eller forbyde angivelse af transaktioner, der medfører omkostningsoverskridelse.   | I projektbudgettering får brugerne flere kontrolmuligheder. Du kan tillade advarsler og overskridelser.                    |
| **Kontrolelement**               | Prognosebaseret kontrol udføres ved hjælp af prognosereduktion. De faktiske beløb trækkes fra de anslåede transaktionssaldi uden et revisionsspor. Dette kan gøre det sværere at spore, hvor de faktiske transaktioner stammer fra.                   | I projektbudgetstyring trækkes de faktiske beløb fra beløbene i det resterende budget. Dette giver et klarere revisionsspor.                                   |

## <a name="project-forecasts"></a>Projektprognoser
Når du bruger projektprognoser, kan du angive prognosetransaktioner i prognoseformularer for de enkelte transaktionstyper. Alle de attributter, der er tilgængelige for en faktisk transaktion, kan bruges til en prognosetransaktion, f.eks. linjerentabilitet, linjeattributter, arbejdere eller beskrivelser. Du kan også projektere, hvor længe efter, at du har afholdt en omkostning, du vil fakturere en kunde. 

Prognosetransaktioner for projektet er baseret på enheder og beløb. 

Du skal knytte de enkelte projektprognoser til en prognosemodel. Når du angiver en prognosetransaktion, foreslås der automatisk en prognosemodel. Prognosemodellen fungerer som en container for prognosetransaktionerne. 

Du kan angive prognosemodeller som undermodeller for en model. Dette gør det muligt for dig at udarbejde prognoser efter region, tidsperiode eller afdeling. Du kan kopiere prognosetransaktionerne i en model for at oprette en ny model, og du kan også overføre transaktionerne til finansregnskabet. Da der findes en en-til-en-relation mellem en prognose og en model, udgør hver prognosemodel et separat budget for et projekt. 

Prognosemodeller kan bruge prognosereduktion som kontrolmekanisme for projekter. I prognosereduktion reducerer de faktiske transaktioner transaktionssaldi i prognoserne. Da prognosereduktion anvendes på det højeste projekt i hierarkiet, giver det dog en begrænset oversigt over ændringer i prognosen. Hvis en arbejder f.eks. er knyttet til et underprojekt, bogføres de faktiske transaktioner for arbejderen i det overordnede projekt. Dette kan gøre det vanskeligt at spore ændringer, da det ikke er nemt at afgøre, hvilken transaktion i et underprojekt der medførte en reduktion af prognosebeløbet. Det er derfor en god ide at oprette en kopi af en prognosemodel til brug for prognosereduktion. Du kan derefter bruge rapporter til at få vist, hvad der oprindeligt blev planlagt. 

Du kan revidere, kopiere, slette eller overføre projektprognoser til et finansregnskabsbudget. Der er dog ingen processtyring. Alle arbejdere, der har rettighed til en prognoseformular, kan revidere den uden gennemgang.

-   **Revision** – Du kan revidere en prognosetransaktion i de samme formularer, som de oprindelige poster blev oprettet i.
-   **Kopiér eller slet** – Når du kopierer prognosetransaktioner, kan du kopiere transaktionslinjerne i én prognosemodel til en anden prognosemodel. Når du sletter en prognose, skal du slette prognosetransaktionerne fra en prognosemodel. Hvis du vil begrænse de prognosetransaktioner, der kopieres eller slettes, skal du vælge bestemte transaktionstyper og datoer. På denne måde kan du kun kopiere eller slette bestemte dele af en prognose.
-   **Overførsel** – Når du overfører en projektprognose til et finansregnskabsbudget, overfører du prognosetransaktionerne for en prognosemodel til et finansregnskabsbudget. Du kan overskrive eventuelle tidligere overførte transaktioner i det finansregnskabsbudget, som du overfører din projektprognose til.

## <a name="project-budgets"></a>Projektbudgetter
Projektbudgettering er en mere enkel metode end prognosticering, selvom den integreres med prognosemodeller. Der bruges en enkelt postformular til oprindelige budgetdetaljer og -revisioner, og gør det muligt at foretage projektioner, der kun er baseret på beløb, kategorier eller aktiviteter. 

I projektbudgettering skal alle oprindelige budgetter og revisioner sendes til en projektarbejdsgang til godkendelse. Arbejdsprocesser giver dig større kontrol over processen og opretter en post over ændringshistorikken. 

Projektbudgettering ligner finansbudgettering, men er hurtigere og nemmere at konfigurere. Mange af indstillingerne i finansbudgettering, som f.eks. nummerserier eller valuta, behøver ikke at blive konfigureret separat for projekter.

Projektbudgetter knyttes automatisk til to prognosemodeller, én til det oprindelige budget og én til det resterende budget. Derfor kan rapporter, der er baseret på prognosemodeller, bruge budgetdata. Når et projektbudget er bindende, oprette systemet prognosetransaktioner på grundlag af de tilknyttede modeller, som bruges til rapporterings- og kontrolformål.

## <a name="forecast-models"></a>Prognosemodeller
Prognosemodeller har et hierarki med en enkelt lag. Dette betyder, at én projektprognose skal knyttes til én prognosemodel.

Hvis du bruger projektprognosticering, kan du identificere modellerne som undermodeller. Du kan derefter oprette prognoser efter afdeling, tidsperiode eller region. Du kan f.eks. oprette en prognosemodel for et år og derefter oprette undermodeller for de nordøstlige, sydøstlige, nordvestlige og sydvestlige regionale prognoser, som lederne i regionerne indsender. Hvis du vælger forskellige indstillinger i de tilgængelige rapporter, kan du få vist oplysninger efter samlet prognose eller undermodel.





[!INCLUDE[footer-include](../includes/footer-banner.md)]