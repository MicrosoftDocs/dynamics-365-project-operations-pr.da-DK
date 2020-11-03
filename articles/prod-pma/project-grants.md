---
title: Projekttilskud
description: I dette emne forklares det, hvordan du kan oprette eller redigere et tilskud.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074353"
---
# <a name="project-grants"></a>Projekttilskud

[!include [banner](../includes/banner.md)]

Et tilskud er en pengegave til et bestemt formål eller projekt. Som regel er der begrænsninger på, hvordan et tilskud kan bruges. I Projektstyring og regnskab kan du angive og spore tilskud og definere deres relationer til projekter og projektkontrakter. Du kan f.eks. udføre følgende opgaver:

- Tilknyt tilskud til projekter og finansieringskilder via links til siderne **Projekt** og **Projektkontraktdetaljer**.
- Du kan angive og spore ændringer i et tilskud, når det flyttes fra én status til en anden.
- Angiv og spor omkostninger, anmodede beløb og tildelte beløb.
- Opret overordnede tilskud, og knyt dem sammen med underordnede tilskud.

Du kan oprette et tilskud ved at angive samtlige detaljer i en ny post, eller du kan kopiere oplysningerne fra et eksisterende tilskud og derefter opdatere dem.

## <a name="create-a-new-grant"></a>Opret et nyt tilskud

1. Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.
2. Vælg **Nyt** \> **Tilskud**.
3. På siden med tilskudsoplysninger skal du i oversigtspanelet **Generelt** i feltet **Tilskuds-id** angive et alfanumerisk id for tilskuddet.
4. Angiv et navn for tilskuddet i feltet **Tilskudsnavn**.
5. I feltet **Beskrivelse** kan du tilføje oplysninger det nye tilskud.

    De fleste af de andre felter på siden er valgfrie, og du kan angive så få eller mange oplysninger, som du vil.

    På følgende liste beskrives de oplysninger, der er angivet i hvert oversigtspanel på siden med tilskudsoplysninger:

    - **Generelt** – Angiv tilskuddets navn, status, beskrivelse, formål og beløb.
    - t **Kontaktoplysninger** – Angiv oplysninger om medarbejdere, den afdeling, der administrerer tilskuddet, samt tilskudskunden eller organisationens tilskudskilde. Du kan også angive, om organisationen er et gennemgående objekt, der modtager tilskuddet og derefter overfører det til en anden modtager. Vælg **Tilføj** for at tilføje kontaktoplysninger, f.eks. telefonnumre og e-mail-adresser på den organisation, der yder tilskuddet.
    - **Datoer og frister** – Angiv datoer, der er relateret til tilskuddet og tilskudsansøgningen. Som eksempel kan nævnes datoen for ansøgningsfristen, indsendelsesdatoen og den dato, hvor tilskuddet er blevet godkendt eller afvist.
    - **Tilknyttede projekter og projektkontrakter** – Du kan kun angive oplysninger i dette oversigtspanel, hvis feltet **Tilskudsstatus** i oversigtspanelet **Generelt** er angivet til **Aktiv** eller **Tildelt**. Vælg mellem følgende indstillinger for at fuldføre den relaterede opgave:

        - **Tilføj finansieringskilde** – Tilføj en ny finansieringskilde for tilskuddet. Du kan angive samtlige detaljer nu, eller du kan bruge standardoplysninger og derefter opdatere dem senere.
        - **Tilføj projektkontrakt** – Tilføj eller opdater projektkontraktoplysninger.
        - **Tilføj projekt** – Tilføj eller opdater projektdetaljer.

    - **Opsætning** – Angiv detaljer om tilsvarende midler, hvis disse oplysninger er nødvendige. Mange organisationer, der tildeler tilskud, kræver, at modtagerne bruger et bestemt beløb af deres egne penge eller ressourcer, så de svarer til det beløb, der tildeles i tilskuddet. I feltet **Lokalt projekt eller sporings-id** kan du angive et id, der adskiller sig fra projekt-id'et.

        > [!NOTE]
        > Hvis en del af tilskuddet skal tildeles til en anden organisation, skal du angive indstillingen **Underordnet tilskudsmodtager** til **Ja**. I forbindelse med tilskud, der tildeles i USA, kan du angive, om et tilskud skal tildeles under et statsligt mandat eller et føderal mandat.

    - **Trækningsdetaljer** – Tilføj eller opdater oplysninger om, hvor ofte tilskudsmidlerne kan trækkes ud, faktureres eller bruges.

## <a name="create-a-new-grant-from-a-copy"></a>Opret et nyt tilskud fra en kopi

1. Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.
2. Vælg **Ny** \> **Kopier fra tilskud**.
3. Angiv et alfanumerisk id og et navn for det nye tilskud, og vælg derefter **OK**.
4. Gennemse oplysningerne om det kopierede tilskud på siden med tilskudsoplysninger, og foretag eventuelle nødvendige ændringer. De fleste felter på siden er valgfrie.

## <a name="view-or-modify-grant-details"></a>Få vist eller rediger oplysninger om tilskuddet

1. Gå til **Projektstyring og regnskab** \> **Tilskud** \> **Tilskud**.
2. Vælg det tilskud, der skal ændres.
3. I handlingsruden skal du på fanen **Tilskud** i gruppen **Bevar** vælge **Rediger**.
4. Gennemse tilskudsoplysningerne, og foretag eventuelle nødvendige ændringer.
