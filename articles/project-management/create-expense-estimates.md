---
title: Økonomiske estimater for udgifter på projekter
description: Dette emne indeholder oplysninger om, hvordan du definerer eller estimerer projektbaserede udgifter.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589465"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Økonomiske estimater for udgifter på projekter
_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations giver projektledere mulighed for at definere projektbaserede udgifter for hvert projekt eller en opgave. Hvert udgiftselement kan knyttes til en bestemt projektopgave. Udgifter kategoriseres i forskellige udgiftskategorier, som er defineret på organisationsniveau. Prisfastsættelse og omkostningsfastsættelse for de enkelte udgiftskategorier defineres i prislisten. 

Fuldfør følgende fremgangsmåde for at få vist, tilføje eller slette en projektudgift.

1. Gå til **Projekter**, og vælg det projekt, som du vil arbejde på.
2. Vælg fanen **Projektestimater**, og få vist listen over projektudgifter.
3. Vælg **Ny udgift** for at tilføje en udgift. Du kan også vælge en udgift, du vil slette, og derefter vælge **Slet udgift**.

Følgende tabel giver oplysninger om felterne på siden **Udgiftsestimatlinje** på et projekt. 

| **Felt** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- |
| Opgave | En liste med opgaver i projektet. Dette omfatter hovedopgaver og bladnodeopgaver. | Hvis du vælger en opgave til en udgiftsestimatlinje, påvirkes den anslåede udgiftsomkostning og det anslåede udgiftssalg for en opgave. Hvis dette felt ikke udfyldes, spores og opsummeres udgiftsestimatet kun på projektniveau. |
| Kategori | En liste over transaktionskategorier, der har tilknyttede udgiftskategorier i programmet. | Dit valg af en kategori styrerprisfastsættelse og omkostningsfastsættelse på udgiftsestimatlinjen. |
| Startdato | Den forventede dato, hvor udgifterne skal afholdes. | Dette felt har ingen afledt virkning. |
| Enhedsgruppe | Standardværdien i dette felt kommer fra den enhedsgruppe, der er konfigureret som standard for den valgte kategori. Du kan opdatere dette felt for at vælge en anden enhedsgruppe. | Dette felt har ingen afledt virkning. |
| Enhed | Værdien i dette felt gendannes til standardenheden for den valgte kategori. Du kan opdatere dette felt for at vælge en anden enhed. | Hvis du ændrer enheden, resulterer det i en anden standardenhedspris og -omkostning. |
| Antal | Mængden af den anslåede udgift, som du skal afholde. | Dette felt har ingen afledt virkning. |
| Enhedsomkostning | Omkostningen ved kombinationen af den valgte kategori og enhed som angivet på den relevante kostprisliste | Enhedsomkostningen vises altid i projektets omkostningsvaluta. |
| Enhedspris | Prisen for kombinationen af den valgte kategori og den valgte enhed som konfigureret på den relevante salgsprisliste. | Enhedsprisen vises altid i projektets salgsvaluta. |
| Samlet omkostning | Det omkostningsbeløb, der beregnes som mængde \* enhedsomkostning.| Omkostningsbeløbet vises altid i projektets omkostningsvaluta. |
| Salg i alt | Det salgsbeløb, der beregnes som mængde \* enhedspris. | Salgsbeløbet vises altid i projektets salgsvaluta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
