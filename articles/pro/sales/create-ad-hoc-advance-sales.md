---
title: Oprettelse af et ad hoc-forskud på en kontrakt
description: Denne artikel indeholder oplysninger om, hvordan du opretter et forskud på en kontrakt efter behov.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e450a17990c6fc783ddffdb05e1ab5b9429a3c1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922169"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Oprettelse af et ad hoc-forskud på en kontrakt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Microsoft Dynamics 365 Project Operations understøtter faktureringsscenarier, som omfatter forudbetalinger og forskud. Processen til brug af **Forskud** i **Project Operations** svarer til kontrakter med **Forskudshonorar**. 

Benyt følgende fremgangsmåde for at fakturere et forskud til kunden.

1. Gå til siden **Projektkontrakt**, og vælg derefter fanen **Forskud og forskudshonorarer**.
2. I undergitteret, som viser alle de tidligere registrerede forskud og forudbetalinger skal du vælge **+ Nyt forskudshonorarer på projektkontrakt**. 

    Formularen **Hurtig oprettelse** åbnes med henblik på registrering af en forudbetalinger eller et forskud.
    
3. I tabellen nedenfor vises de felter til registrering af forskud og overvejelser, du skal have in mente, når du opretter nye:

    | Felt | Beskrivelse | Downstream-virkning |
    | --- | --- | --- |
    | **Projektkontraktkunde** | Dette feltet angiver, hvilken kunde på kontrakten dette forskud skal faktureres til. | Hvis der er flere kunder på kontrakten, og du vil fakturere hver af dem et bestemt forskudshonorarer eller forskudsbeløb, skal du oprette et forskud for hver enkelt kunde. |
    | **Beskrivelse** | Beskrivelsen af formålet med eller tidspunktet for forskuddet bidrager til at identificere forskuddet. | Beskrivelsen vises på fakturalinjen for denne forskudsbetaling. |
    | **Beløb** | Beløbet for forudbetalingen eller forskuddet. | Dette beløb vises på fakturalinjen for denne forskudsbetaling. |
    | **Fakturadato** | Den dato, hvor dette forskud er faktureret til kunden. | Dette er datoen, hvor processen for automatisk fakturaoprettelse opretter en fakturalinje for forskuddet. |
    | **Fakturastatus** | Dette er en indstilling, der angiver, om dette forskud tilføjes til en kladdefaktura for denne kunde. De mulige værdier er:</br>- **Ikke klar til fakturering**</br>- **Klar til fakturering** | Når et forskud eller en forudbetaling er markeret som **Klar til fakturering**, tilføjes den som en linjetid på en kladdefaktura. Det er kun et fuldt faktureret forskud, der kan bruges til afstemning med projektomkostninger for den næste faktureringsperiode. |

4. Vælg **Gem og luk** i dialogboksen for hurtig oprettelse for at registrere forskuddet eller forudbetalingen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]