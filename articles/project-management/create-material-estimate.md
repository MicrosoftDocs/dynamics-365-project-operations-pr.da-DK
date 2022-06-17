---
title: Økonomiske estimater for materialer på projekter
description: Denne artikel indeholder oplysninger om definering eller estimering af projektbaserede materialer.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925679"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Økonomiske estimater for materialer på projekter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations giver projektledere mulighed for at definere projektbaserede materialeomkostninger for de enkelte projekter eller opgaver. Hvert materialeestimat kan knyttes til en bestemt projektopgave. Materiale, der bruges til projekter, kan være produkter, der skal indkøbes, eller produkter fra produktkataloget. For hver kombination af et produkt og en enhed kan der defineres en pris i projektprislisterne for salg og i projektprislisterne for omkostninger.  

Fuldfør følgende trin for at få vist, tilføje eller slette et projektmaterialeestimat.

1. Gå til **Projekter**, og vælg det projekt, du vil opdatere.
2. På fanen **Materialeestimater** skal du gennemgå listen med projektmaterialeestimimater.
3. Vælg **Nyt materialeestimat** for at oprette et nyt materialeestimat. Du kan også vælge et materialeestimat, der skal slettes, og derefter vælge **Slet materialeestimat**.

Følgende tabel giver oplysninger om felterne på siden **Materialeestimatlinje** på et projekt. 

| **Felt** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- |
| Opgave | En liste med opgaver i projektet. Dette omfatter hovedopgaver og bladnodeopgaver. | Når du vælger en opgave til en materialeestimatlinje, påvirkes de anslåede materialeomkostninger og det anslåede materialesalg for en opgave. Hvis dette felt er tomt, spores og opsummeres materialeestimatet kun på projektniveau. |
| Vælg produkt |  Du kan vælge at angive, hvorvidt denne estimatlinje er for et eksisterende (katalog)produkt eller et produkt, der skal rekvireres. | I dette felt bestemmes det, om du vælger et produkt fra kataloget eller et produkt, der skal rekvireres. |
| Produkt | Id'et for produktet fra produktkataloget. Når du vælger et produkt-id, opdateres værdien i feltet **Vælg produkt** automatisk til **Eksisterende produkt**. Id'et bruges til at hente omkostnings- og salgspriserne fra prislisten. | Dette felt har ingen afledt virkning. |
| Beskrivelse af produkt, der skal rekvireres | Et tekstfelt, som produktnavnet skal skrives i. Dette felt bør kun benyttes, når **Rekvireres** er valgt i feltet **Vælg produkt**.| Dette felt har ingen afledt virkning. |
| Startdato | Den forventede dato, hvor materialet forventes at blive brugt. | Dette felt har ingen afledt virkning. |
| Enhedsgruppe | Standardværdien i dette felt kommer fra standardenhedsgruppen på katalogproduktet. Du kan opdatere dette felt for at vælge en anden enhedsgruppe. | Dette felt har ingen afledt virkning. |
| Enhed | Værdien i dette felt kommer fra standardenheden for det valgte produkt. Du kan opdatere dette felt for at vælge en anden enhed. | Hvis du ændrer enheden, resulterer det i en anden standardenhedspris og -omkostning. |
| Antal | Den anslåede mængde af det produkt, der skal bruges på projektet. | Dette felt har ingen afledt virkning. |
| Enhedsomkostning | Enhedsomkostningen for det valgte produkt og den valgte enheds kombination som angivet på den relevante kostprisliste. | Enhedsomkostningen vises altid i projektets omkostningsvaluta. Hvis der ikke er angivet nogen enhedsomkostninger for kombinationen af opsætningen af produktet og enheden på prislisten, angives enhedsomkostningen som standard til 0,00. |
| Enhedspris | Prisen for kombinationen af det valgte produkt og den valgte enhed som angivet på den relevante salgsprisliste. | Enhedsprisen vises altid i projektets salgsvaluta. Hvis der ikke er angivet nogen enhedspris for kombinationen af opsætningen af produktet og enheden på prislisten, så angives enhedsprisen som standard til 0,00.|
| Samlet omkostning | Det omkostningsbeløb, der beregnes som mængde \* enhedsomkostning.| Omkostningsbeløbet vises altid i projektets omkostningsvaluta. |
| Salg i alt | Det salgsbeløb, der beregnes som mængde \* enhedspris. | Salgsbeløbet vises altid i projektets salgsvaluta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
