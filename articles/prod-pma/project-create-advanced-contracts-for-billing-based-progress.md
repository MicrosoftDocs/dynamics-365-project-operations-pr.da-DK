---
title: Opret avancerede kontrakter for fakturering, der er baseret på status
description: I dette emne forklares det, hvordan du opretter projektkontrakter, så du kan oprette fakturaer for kunder på baggrund af en procentdel af det fuldførte arbejde.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074301"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Opret avancerede kontrakter for fakturering, der er baseret på status
[!include [banner](../includes/banner.md)]

I dette emne forklares det, hvordan du opretter projektkontrakter, så du kan oprette fakturaer for kunder på baggrund af en procentdel af det fuldførte arbejde. Fakturabeløb beregnes automatisk for de budgetkategorier for arbejde, som du konfigurerer for et projekt. Tidspunktet for fakturering angives, når du forhandler projektkontrakten med kunden.

Brug procedurerne i dette emne til at oprette en kontrakt, et tilknyttet projekt og de faktureringsregler, der beregner fakturabeløb for de budgetkategorier af arbejde, som du konfigurerer for projektet.

Når du har oprettet kontrakten og projektet, kan du konfigurerer oplysningerne om projektet. Du kan f.eks. definere aktiviteter og tildele arbejdere til projektet.

## <a name="example"></a>Eksempel

Din organisation er et firma, som arbejder med softwareudvikling. Du indvilliger i at udarbejde en lønningsregnskabspakke for en kunde til en samlet pris på 20.000 dollars (USD). Din organisation indvilliger i at fakturere kunden, efterhånden som du færdiggør projekt på grundlag af procenter. Du skal konfigurere følgende projektkategorier for arbejdet, så du kan bruge dem i faktureringsprocessen:

- Konsulentvirksomhed
- Design
- Installation

Du konfigurerer også faktureringsregler, der automatisk beregner fakturabeløbene for den procentdel af projektarbejdet, der er fuldført i de enkelte kategorier.

Budgetadministratoren opretter et budget for projektkategorierne. Beløbet for fuldført arbejde beregnes automatisk som en procentdel af det faktiske arbejde i forhold til de budgetterede beløb.

## <a name="prerequisites"></a>Forudsætninger

Før du opretter et projekt, der bruger faktureringsregler, skal du oprette nummerserierne til faktureringsregler og en gebyrkladde, der bruges til at bogføre fakturaer, efterhånden som arbejdet færdiggøres.

1. Gå til **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.
2. På siden **Parametre for projektstyring og regnskab** skal du på fanen **Nummerserier** konfigurere den nummerserie, som du vil bruge, når der oprettes faktureringsregler.
3. Gå til **Projektstyring og regnskab** \> **Kladder** \> **Gebyr**.
4. På siden **Gebyrkladde** skal du vælge **Ny** og angive navnet på kladden.

## <a name="create-a-contract-for-progress-billings"></a>Opret en kontrakt for statusfaktureringer

Benyt denne fremgangsmåde til at oprette en projektkontrakt for et fastprisprojekt. Du kan oprette en projektfaktura, når det arbejde, der er færdiggjort på projektet, når en bestemt procentdel.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.
2. På siden **Projektkontrakter** skal du vælge **Ny**.
3. I dialogboksen **Ny projektkontrakt** skal du indstille følgende felter:

    - **Navn**
    - **Finansieringstype**
    - **Finansieringskilde**
    - **Salgsvaluta** – Denne valuta bruges som standard til kundefakturaer, der er knyttet til projektkontrakten. Du kan dog ændre salgsvalutaen på en bestemt kundefaktura.

4. Vælg **OK**. Oplysningerne kopieres til overskriften på siden **Projektkontrakter**.
5. På siden **Projektkontrakter** skal du udfylde resten af de påkrævede oplysninger for projektet.

## <a name="create-a-project-for-progress-billings"></a>Opret et projekt for statusfaktureringer

Benyt følgende fremgangsmåde for at oprette et projekt og eventuelle underprojekter, der er knyttet til en projektkontrakt.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.
2. På siden **Alle projekter** skal du vælge **Nyt**.
3. I dialogboksen **Nyt projekt** skal du i feltet **Projekttype** vælge **Tid og materiale**.
4. Vælg en projektgruppe. En projektgruppe definerer bogføringsoplysningerne for de projekter, der er tildelt til gruppen.
5. Vælg **Opret projekt**.
6. Når projektet er oprettet, skal du angive projektstadiet til **Igangværende**.

## <a name="create-a-budget-for-a-project"></a>Opret et budget for et projekt

Budgetkategorier anvendes til automatisk at beregne fakturabeløbene for den procentdel af arbejdet, der er fuldført for de enkelte kategorier. Følg disse trin for at oprette budgetkategorier for de estimerede omkostninger.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.
2. På siden **Alle projekter** skal du vælge og åbne det ønskede projekt.
3. På siden **Projekter** skal du i handlingsruden på fanen **Plan** i gruppen **Budget** vælge **Projektbudget**.
4. På siden **Projektbudget** skal du angive en estimeret omkostning for hver kategori i projektet.

## <a name="create-billing-rules-for-progress-billings"></a>Opret faktureringsregler for statusfaktureringer

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.
2. Åbn siden med listen **Projektkontrakter**, vælg og åbn en projektkontrakt.
3. På siden med projektkontrakten skal du i oversigtspanelet **Faktureringsregler** vælge **Tilføj**.
4. På siden **Faktureringsregel** skal du i feltet **Linjetype** vælge **Fremgang**.
5. I oversigtspanelet **Linjedetaljer om faktureringsregel** skal du i feltet **Kontraktværdi** angive kontraktens samlede værdi.
6. I feltet **Kategori** skal du vælge den kategori, som gebyrtransaktionen skal bogføres i.
7. I feltet **Projekt** skal du vælge det projekt, der bruger denne faktureringsregel.
8. Valgfrit: Tildel faktureringsreglen til flere projekter. I oversigtspanelet **Projekter** skal du i sektionen **Tilgængelige projekter** vælge et projekt og derefter vælge den højre piletast for at tilføje projektet til sektionen **Valgte projekter**.
9. Valgfrit: Beregn det procentuelle beløb, som kunden tilbageholder fra betalinger på en faktura. I oversigtspanelet **Betingelser for tilbageholdelse af betaling** skal du vælge finansieringskilden og derefter i feltet **Tilbageholdelsesprocent** angive tilbageholdelsesprocenten.
10. Gentag disse trin for at oprette flere faktureringsregler for projektkontrakten.
