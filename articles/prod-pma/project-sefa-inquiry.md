---
title: Forespørgsel om plan for udgifter til føderale priser
description: Dette emne indeholder oplysninger om forespørgsel om planen for udgifter til føderale priser.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d0cc3db3fd05fa809f707b15a50380753ac8f9f779f45c13f707321d2b0e0841
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007229"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Forespørgsel om plan for udgifter til føderale priser

[!include [banner](../includes/banner.md)]

Ifølge cirkulære A-133 fra Office of Management and Budget (kontoret for styring og kontrol) er de agenturer, der modtager føderale midler, underlagt overvågningskrav, også kaldet enkelte overvågninger. Overvågningsprocessen anvendes til at rapportere om indtægter og udgifter for føderale tilskud på et tilbagevendende grundlag. En del af den enkelte overvågningsrapport omfatter planen for udgifter til føderale priser (SEFA).

Forespørgsel om planen for udgifter til føderale priser omfatter kataloget over titlen og nummeret på Federal Domestic Assistance (CFDA), tilskudsnummer, tilskudsåret, navnet på det føderale agentur, der stiller midlerne til rådighed, samt navnet på pass-through-objektet. Forespørgslen gælder for en bestemt periode. Denne periode er som regel den samme som regnskabsperioden, som er et regnskabsår.

Forespørgslen inkluderer de tilskud, der har projektionsdatoer i det valgte datointerval. I kolonnen **Tilskudsgivende agentur** i forespørgslen vises tilskudskunden eller, for et pass-through-tilskud, det tilskudsgivende agentur. I forbindelse med pass-through-tilskud viser kolonnen **Pass-through-agentur** tilskudskunden. Hvis tilskuddet ikke er et pass-through-tilskud, er kolonnen **Pass-through-agentur** tom.

## <a name="set-up-the-cfda-clusters"></a>Konfigurer CFDA-klyngerne

Du skal konfigurere CFDA-klyngerne, der kan knyttes til CFDA-numre i forespørgsel om planen for udgifter til føderale priser.

1. Gå til **Projektstyring og regnskab \> Opsætning \> Tilskud \> Katalog over klynger af Federal Domestic Assistance**.
2. Vælg **Ny** for at oprette en CFDA-klynge.
3. Angiv klyngens navn.
4. Vælg **Gem** for at gemme dine ændringer.

## <a name="set-up-cfda-numbers"></a>Konfigurer CFDA-numre

Du skal konfigurere CFDA-numre, der kan tilføjes til tilskud og medtages i forespørgsel om planen for udgifter til føderale priser.

1. Gå til **Projektstyring og regnskab \> Opsætning \> Tilskud \> Katalog over numre til Federal Domestic Assistance**.
2. Vælg **Ny** for at oprette et CFDA-nummer.
3. Angiv CFDA-nummeret i kolonnen **Nummer**.
4. Tryk på tasten **Tab**.
5. Angiv CFDA-titlen i kolonnen **Beskrivelse**.
6. Tryk på tasten **Tab**.
7. Valgfrit: I feltet **Programklynge** kan du tilføje den relevante CFDA-klynge.
8. Vælg **Gem** for at gemme dine ændringer.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Konfigurer tilskud, der skal rapporteres i forespørgsel om planen for udgifter til føderale priser

1. Gå til **Projektstyring og regnskab \> Tilskud \> Tilskud**, og vælg et eksisterende tilskud.
2. I oversigtspanelet **Opsætning** skal du i feltet **Katalog over Federal Domestic Assistance** tildele CFDA-nummeret. CFDA-nummeret på tilskuddet bestemmer CFDA-klyngen med henblik på rapportering.
3. I oversigtspanelet **Kontaktoplysninger** skal du angive oplysningerne på tilskudsgiver ved at benytte følgende fremgangsmåde:

    1. I feltet **Tilskudskunde** skal du angive den kunde, der er ansvarlig for tilskuddet. For et eksisterende tilskud er disse oplysninger muligvis allerede angivet.
    2. Angiv, om tilskudskunden er stifteren. Hvis tilskudskunden er stifteren, skal du fjerne markeringen i afkrydsningsfeltet **Pass-through**. Hvis en anden kunde er stifteren, og tilskudskunden er ansvarlig for forbrug og sporing af pengene, skal du markere afkrydsningsfeltet **Pass-through**.

4. Hvis du har markeret afkrydsningsfeltet **Pass-through** i forrige trin, skal du i feltet **Tilskudsgivende agentur** angive den kunde, der har ydet tilskuddet. Det tilskudsgivende agentur og tilskudskunden må ikke være den samme kunde.

Her er et eksempel på et pass-through-tilskud:

De føderale offentlige myndigheder finansierede et infrastrukturprojekt for en stat. De føderale offentlige myndigheder gav penge til staten, som den kunne bruge. I dette tilfælde er de føderale offentlige myndigheder det tilskudsgivende agentur, og staten er tilskudskunden.

> [!NOTE] 
> Første gang du aktiverer funktionen, angives de oprindelige CFDA-numre ved hjælp af de eksisterende numre, der findes på tilskuddene.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Udeluk tilskud fra SEFA-rapportering baseret på tilskudstype

1. Gå til **Projektstyring og regnskab \> Opsætning \> Tilskud \> Tilskudstyper**.
2. I oversigtspanelet **Standardoplysninger** skal du vælge afkrydsningsfeltet **Udeluk fra plan for udgifter til føderale priser**.
3. Vælg **Gem** for at gemme dine ændringer.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Kør forespørgslen for planen for udgifter til føderale priser

1. Gå til **Projektstyring og regnskab \> Forespørgsler og rapporter \> Tilskudsforespørgsel \> Plan for udgifter til føderale priser**.
2. I sektionen **Parametre** skal du følge disse trin:

    1. I feltet **Datointerval** skal du vælge koden for datointervallet. Du kan også definere datointervallet i felterne **Fra dato** og **Til dato**.
    2. Valgfrit: Hvis du kun vil inkludere de fakturerede transaktioner som indtægt i forespørgslen, skal du angive indstillingen **Inkluder kun fakturerede indtægter** til **Ja**.

## <a name="columns"></a>Kolonner

Forespørgsel om planen for udgifter til føderale priser omfatter følgende kolonner:

- Klyngenavn for katalog over Federal Domestic Assistance
- Tilskudsgivende agentur
- Gennemgående agentur
- Navn på tilskud
- Tilskuds-id
- Id for tilskudsansøgning
- Katalog over Federal Domestic Assistance
- Kvitteringer
- Udgifter


[!INCLUDE[footer-include](../includes/footer-banner.md)]