---
title: Underentreprise i udgivelsen af tidlig afgang i oktober 2021
description: Dette emne giver en oversigt over underentreprisefunktionerne i Project Operations, som er en del af udgivelsen af tidlig adgang i oktober 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383688"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Underentreprise i udgivelsen af tidlig afgang i oktober 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dette emne giver en oversigt over underentreprisefunktionerne i Dynamics 365 Project Operations, som er en del af udgivelsen af tidlig adgang i oktober 2021. Dette funktionssæt er ikke klar til produktion eller live miljøer, så disse funktioner frigives fortsat i tidlig adgang, indtil den fulde funktion udgives. Det anbefales på det kraftigste, at du ikke bruger den underentreprisefunktion, der er angivet for scenarier med live produktion, før banneret med forhåndsversion er fjernet. 

Følgende liste indeholder en oversigt over, hvad der i øjeblikket er tilgængeligt i udgivelsen af tidlig adgang i oktober 2021:

1. Projektlederen opretter en underleverance med en leverandør. De prislister, der er tilknyttet kreditorposten, bruges som standard til underleverancen. Leverandørkontoen har relationstypen **Kreditor** eller **Leverandør**.

2. Projektlederen kan specificere alle køb som linjeelementer i underleverancen. Underleverancelinjer kan indeholde tid, udgifter eller produkter. Transaktionsklassen for underentrepriselinjen, bestemmer, hvad linjen er beregnet til.

3. Administratoren af leverandørkontoen og projektlederen kan gentage valget for hele underleverancen. Prisfastsættelse kan justeres i købsprislister, der er tilknyttet underleverancen.

4. Hvis underentrepriselinjen på dette tidspunkt eller senere i processen omhandler tid, knytter administratoren af leverandørkontoen leverandørkontakter til hver underentrepriselinje. Denne tilknytning indeholder oplysninger til den projektleder, der arbejder med underleverancen. Når en leverandørkontakt er knyttet til en underentrepriselinje, opretter systemet automatisk en reserverbar ressource ud fra kontaktpersonen, hvis der ikke allerede findes en reserverbar ressource.

5. Faktureringsmetoden på hver underleverancelinje kan være **Fast pris** eller **Tid og materiale**. Der konfigureres en milepælsbaseret faktureringsplan for underentrepriselinjer med faste priser.

De resterende trin i forretningsprocesforløb for underentrepriser, der er skitseret i oversigten, er ikke tilgængelige i øjeblikket. Dette emne opdateres i takt med at der tilføjes nye funktioner. 

I følgende illustration vises udgivelsen af underentreprise i udgivelsen for tidlig adgang i modsætning til forretningsprocessen fra start til slut.

![Procesflow for underleverancer](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Mængdebaserede underentrepriselinjer og arbejdsbaserede underentrepriselinjer i udgivelsen af tidlig adgang
I udgivelsen for tidlig adgang i oktober 2021 understøttes kun mængdebaserede underentrepriselinjer. Dette betyder, at en underentrepriselinje kan bruges til at købe tid, udgifter eller materialer fra en leverandør, men ikke til et helt projektarbejde. Dette betyder også, at den mængde, der købes (enheder af tid, udgifter eller materialemængder) på en underentrepriselinje, kan bruges på et hvilket som helst projekt i systemet.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
