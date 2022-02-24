---
title: Kopier prislister
description: Dette emne indeholder oplysninger om, hvordan du kopierer prislister i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67a69d521ac0a5632371138bd4fbb9dd00fe34ee
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181490"
---
# <a name="copy-price-lists"></a>Kopier prislister

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan oprette kopier af prislister i Dynamics 365 Project Operations. Du kan f.eks. oprette prislister for det kommende år ved hjælp af en prisliste fra det aktuelle år.  Du kan også kopiere en prisliste for faktureringssatser og salgspriser fra prislisterne for omkostninger. 

Hvis du vil oprette en kopi af prislisten, skal du benytte følgende fremgangsmåde.

1. Åbn den prisliste, som du vil oprette en kopi af, og vælg **Kopier**.
2. Angiv de nødvendige oplysninger for at kopiere prislisten. I følgende tabel vises overvejelser, du skal huske, når du angiver oplysninger.

| Felt | Beskrivelse | Downstream-virkning |
| --- | --- | --- |
| Navn | Navnet på kildeprislisten, hvor der er tilføjet **-kopien**. | Prislisten inkluderer denne værdi på alle listesider og indstillinger for rullelister. |
| Sammenhæng | Angiv den kontekst, der skal vises for destinationsprislisten. | En prisliste med konteksten **Omkostninger** bruges til at slå prisen for omkostningsestimater og faktiske omkostningsværdier op. En prisliste med konteksten **Salg** bruges til at slå prisen for salgsestimater og faktiske salgsværdier op. Kun prislister med konteksten **Salg** kan tilknyttes en projektprisliste for en kunde, tilbud eller kontrakt. |
| Startdato | Startdatoen for den periode, hvor prislisten er gældende. | Sammen med **Slutdato** bruges dette felt til at afgøre, hvilken prisliste der gælder for en bestemt estimatlinje eller faktisk linje. |
| Slutdato | Slutdatoen for den periode, hvor prislisten er gældende. | Sammen med **Startdato** bruges dette felt til at afgøre, hvilken prisliste der gælder for en bestemt estimatlinje eller en faktisk linje. |
| Valuta | Destinationsprislistens valuta. Denne kan ændres. | Når denne ændring er foretaget, konverteres alle elementer i de nye prislinjer for arbejdskraft, udgifter og produktkatalog til destinationsprislistens valuta i forbindelse med kopieringen. |
| Tidsenhed | Destinationsprislistens valuta. Denne kan ændres. | Når denne ændring er foretaget, konverteres alle de nye prislinjer for arbejdskraftselementer til destinationsprislistens undermodul i forbindelse med kopieringen. Konverteringen fra opsætningen af undermodulet for tid i kildeprislisten og destinationsprislistens undermodul for tid bruges. |
| Beskrivelse | En beskrivelse af kildeprislisten med tilføjelsen **-kopien**. Dette er et tekstfelt, som giver dig mulighed for at få en beskrivelse af prislisten på flere linjer. | Dette felt vises i de **Tilknyttede** visninger på prislisten i forskellige objekter, der har relaterede prislister. |

3. Gem prislisten. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Opdater en prisliste ved at anvende en avance for alle priser

1. På fanerne **Rolle**, **Kategori** og **Prislisteelement** for en prisliste kan du vælge **Opdater priser** for at anvende en avance for alle priser i undergitteret. 
2. Angiv en avance på den dialogside, der vises. Du kan også angive en negativ avanceprocent for at reducere priserne med en bestemt procentdel. 
3. Vælg **OK** på dialogsiden, og kontrollér derefter, at priserne i undergitteret afspejler de ændringer, du har foretaget.
