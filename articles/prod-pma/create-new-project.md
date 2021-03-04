---
title: Oprette et nyt projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter et nyt projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074307"
---
# <a name="create-a-new-project"></a>Oprette et nyt projekt

[!include [banner](../includes/banner.md)]

Benyt følgende fremgangsmåde for at oprette et nyt projekt.

1. På siden **Projektstyring** skal du vælge **Nyt projekt** og angive følgende værdier:

    - **Projekttype:** Tid og materiale
    - **Projektnavn:** XYZ-opgraderingsfase 2
    - **Projektgruppe:** TM\_IGVA
    - **Projektkontrakt-id:** 00000002

2. Vælg **Opret projekt**.

## <a name="assign-a-resource-to-a-project"></a>Tildel en ressource til et projekt

1. På siden **Arbejdere** i listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere konfigurerede kompetencer for, og åbne arbejderposten.
2. I handlingsruden skal du på fanen **Projekt** i gruppen **Opsætning** vælge **Tildel projekter**.
3. På siden **Projekttildelinger til ressourcevalidering** skal du på fanen **Projekter** i feltet **Tilføj projektet til valgte projekter** filtrere efter projektet **XYZ-opgraderingsfase 2**.
4. I ruden **Resterende projekter** skal du vælge et projekt og derefter vælge pileknappen for at tilføje det til ruden **Valgte projekter**.

Du kan også tildele kategorierne for en ressource, efterhånden som du har brug for det. Kategoritypen er enten **Omkostning** eller **Omsætning**. Kategoritypen bestemmes af din organisation. Hvis der ikke er tildelt nogen kategorier for en ressource, søges Finance i standardkategorien efter timepriser for omkostninger og omsætning.

## <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurer egenskaberne for projektressourcer og roller

En projektleder kan bruge funktionen projektressource til at oprette de roller, der kræves for projektet. Roller kan bruges, hvis bekræftede ressourcer stadig ikke er kendte, når ressourcerne reserveres. Roller kan reserveres midlertidigt som planlagte ressourcer, så du kan fortsætte med projektplanlægningsfaserne.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarie:** Contoso blev hyret til at fuldføre et tids- og materialeprojekt, der har et godkendt projektcharter. Den underordnede projektleder fuldfører stadig omfanget af projektet. Den ressourceansvarlige identificerer i øjeblikket bestemte ressourcer, der skal reserveres til at arbejde på det nye projekt. På grund af projektets vigtigste karakter anmoder projektsponsor om, at en af rollerne er den overordnede projektleder. Den ressourceansvarlige skal erhverve den nye ressource og definere rollen i systemet i tilfælde af, at den underordnede projektleder kræver ressourceoplysningerne i forbindelse med projektplanlægningen.

I følgende trin vises, hvordan den ressourceansvarlige kan konfigurere den overordnede projektleders rolle og knytte ressourceegenskaber til den. Senere kan rollen bruges til at søge efter tilgængelige ressourcer, der matcher de nødvendige ressourcekompetencer.

1. På siden **Opsætning af roller** skal du vælge **Ny** og angive følgende værdier:

    - **Rolle-id:** Overordnet projektleder
    - **Beskrivelse:** Overordnet projektleder

2. Vælg **Opret**.
3. Vælg rollen **Overordnet projektleder** , og vælg derefter **Konfigurer egenskaber**.
4. I feltet **Egenskabstype** skal du vælge **Færdighed**.
5. I feltet **Tilgængelige egenskaber** skal du angive den færdighed, der skal søges efter.
6. I feltet **Egenskabstype** skal du vælge **Certifikat**.
7. I feltet **Tilgængelige egenskaber** skal du angive den certifikattype, der skal søges efter.

## <a name="assign-a-project-resource-to-a-project"></a>Tildel en projektressource til et projekt

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgraderingsfase 2**.
2. På fanen **Projektteam og planlægning** skal du vælge **Tilføj**.
3. I feltet **Rolle** skal du vælge **Teammedlem**.
4. Vælge **Reserver fra kalenderen**.
5. På siden **Ressourcetilgængelighed** skal du vælge **Vis indstillinger**.
6. På siden **Tilpasning visningsindstillinger** skal du angive følgende værdier:

    - **Format for visnings af datointerval:** Dag
    - **Vis beskrivelser af tilgængelighed:** Ja
    - **Vis resterende kapacitet:** Ja

7. Vælg en ressource på listen over ressourcer.
8. Vælg **Reserver definitivt** og **Fuld kapacitet**.

## <a name="assign-a-resource-to-a-default-role"></a>Tildel en ressource til en standardrolle

For at hjælpe projektledere eller ressourceansvarlige med yderligere detailudledning om de ressourcer, der kan reserveres til et projekt. Du kan knytte en standardrolle til en eksisterende ressource eller en nyerhvervet ressource. F.eks. da Daniel blev ansat, havde han den erfaring og de færdigheder, der var nødvendige for at udfylde rollen som forretningsanalytiker. Den ressourceansvarlige har tildelt denne rolle som Daniel standardrolle. Den ressourceansvarlige har derfor føjet Daniel til en gruppe med forretningsanalytikere, som er til rådighed til at kunne arbejde med projekter.

I forbindelse med ressourcereservationen kan projektledere filtrere de rolleressourcer, der er tilgængelige til at kunne arbejde på projekter. De kan bruge disse oplysninger som et kriterium, når de udfører beslutningsanalyse med flere kriterier under ressourceopfyldning. De kan også tilføje andre ressourceegenskaber til filteret for at søge efter ressourcer, der har bestemte færdigheder, uddannelser og erfaring i forbindelse med et bestemt projekt.

**Scenarie:** Et godkendt projekt er påbegyndt, og rollen som overordnet projektleder blev reserveret som en planlagt ressource i projektplanlægningsfasen. Den ressourceansvarlige har nu erhvervet en ressource, der skal udføre rollen overordnet projektleder.

1. På siden **Ressourceliste** skal du vælge **Daniel Goldschmidt**.
2. På siden **Ressourcerolle** skal du vælge **Ny** og angive følgende værdier:

    - **Ikrafttrædelse:** Angiv den aktuelle dato.
    - **Udløb:** Angiv **Aldrig**.
    - **Rolle:** Angiv **Overordnet projektleder**.

3. Vælg **Gem** , og luk derefter siden.
4. På fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og certifikatet **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]