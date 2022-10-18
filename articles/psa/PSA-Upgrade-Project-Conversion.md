---
title: Konverteringsproces fra Project Service Automation til Project Operations-projektplanlægning
description: Denne artikel indeholder en oversigt over funktionsændringerne for Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642561"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Konverteringsproces fra Project Service Automation til Project Operations-projektplanlægning

Når et projekt er opgraderet fra Microsoft Dynamics 365 Project Service Automation 3.X til Dynamics 365 Project Operations Lite, er det ikke muligt at redigere projektopgaver i arbejdsopgavehierarkiet (WBS) for opgavegitteret. Kunder kan gennemse WBS'er i sporingsgitteret, hvor der er tilføjet nye felter, for at angive alle detaljer, der er relateret til opgaven. I forbindelse med projekter, hvor der kræves redigering af WBS, kan du vælge at konvertere kvalificerede projekter til den nye Project for the Web-planlægningsoplevelse.

## <a name="project-conversion-process"></a>Projektkonverteringsproces

Hvis du vil konvertere et projekt, skal du følge disse trin.

1. Åbn projektets hovedside, og vælg **Konvertér** i handlingsruden.
1. Vælg **OK** i bekræftelsesfeltet for at starte projektkonverteringen. Følgende handlinger forekommer:

    1. En meddelelseslinje, der vises på projektets hovedside, med teksten "Projektplanen konverteres. Du kan ikke foretage ændringer af projektet, før konverteringen er fuldført".
    1. Du bliver omdirigeret til projektlisten.

    Når projektkonverteringen er fuldført, udføres følgende handlinger:

    1. Den tilknyttede projektleder modtager en meddelelse i højre side af programmet.
    1. Den meddelelseslinje, der oplyser, at konverteringen er i gang, fjernes.
    1. Under fanen **Planlæg** vises den nye planlægningsoplevelse med Project for the Web. Alle brugere med de rette licenser og sikkerhedsroller kan redigere WBS.
    1. Feltet **Planlægningsprogram** opdateres til **Project for the Web**.
    1. Knappen **Konvertér** fjernes fra handlingsruden.

> [!IMPORTANT]
> Massekonvertering af projekter er ikke tilladt. Ethvert forsøg på at opdatere et stort antal projekter samtidig er begrænset. Denne begrænsning er med til at sikre høj ydeevne for alle kunder.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuelle opgaver vs. automatiske opgaver

Når et miljø opgraderes fra Project Service Automation til Project Operations, opfattes alle opgaver i WBS som automatisk planlagte opgaver. Begrebet manuelt planlagte opgaver er ikke tilgængeligt i Project for the Web. Du kan dog definere den foretrukne planlægningsfunktionsmåde for dine projekter ved hjælp af indstillingen for [planlægningstilstand](/project-management/scheduling-modes.md), når du opretter nye projekter.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Begrænsede handlinger i forbindelse med projekter før konvertering

I dette afsnit beskrives de funktionelle forskelle, du kan forvente, når projekter ikke er konverteret.

### <a name="copy-project"></a>Kopiér projekt

Handlingen **Kopiér** understøttes kun i konverterede projekter. Opgraderede projekter kan ikke kopieres før konverteringen.

### <a name="move-project"></a>Flyt projekt

Hvis du ændrer startdatoen for et projekt, flyttes starttidspunktet ikke automatisk tilsvarende, medmindre projektet er konverteret.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Hvad er forskellene mellem konverterede projekter og nye projekter, der oprettes, efter at opgraderingen er fuldført?

I forbindelse med projekter, der konverteres, efter at miljøet er opgraderet, angives der et flag, som giver tidsplanen besked om kun at overholde projektkalenderen. Denne funktionsmåde svarer til funktionsmåden i Project Service Automation. Flaget angives dog ikke for nye projekter, der er oprettet efter opgraderingen. Tidsplanen vil derfor overholde ressourcernes arbejdstimer, når de tildeles til en opgave.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Hvad skal jeg gøre, hvis mit projekt ikke kan konverteres?

Hvis dit projekt ikke kan konverteres, skal du som det første gennemse fejlloggene for at identificere eventuelle almindelige problemer, der er relateret til din WBS. Hvis loggene ikke angiver en bestemt fejl, som du kan løse, kan du kontakte kundesupport, så din sag kan gennemses yderligere.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Hvordan håndteres lukketider i Project for the Web?

I Project for the Web overholdes ikke de lukketider, som virksomheden definerer på organisationsniveau. Det vil dog overholde andre typer fridage, der er defineret i en given arbejdstidsskabelon.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Hvilke begrænsninger er der for Project for the Web?

Se [Oprette et arbejdsopgavehierarki til et projekt](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Kan jeg forvente ændringer af mine omkostnings- og salgsestimater?

I sjældne tilfælde, hvor ressourcetildelinger genberegnes, eller hvor de falder på en anden datogrænse end kildeprojektet, kan der være forskelle i salgs- og omkostningsestimater. Som en del af opgraderingsprocessen forventes kunderne at teste et repræsentativt udsnit af projekter, så de kan forstå eventuelle ændringer i tidsplanen.
