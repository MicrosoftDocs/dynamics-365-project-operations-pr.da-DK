---
title: Konfigurer hyppigheden for fakturering af arbejdstid - lille
description: Dette emne indeholder oplysninger om konfiguration af faktureringssatser for arbejdskraft i Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 26c3743283dd9032e044071b3127a2885ad5ae49
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004254"
---
# <a name="set-up-labor-bill-rates---lite"></a>Konfigurer hyppigheden for fakturering af arbejdstid - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Hver prisliste har et sæt rollepriser eller satser for arbejdskraft, der er gældende for den kontekst og ikrafttrædelsesdato, der er inkluderet i prislistens overskrift. Fakturapriser for tid i Dynamics 365 Project Operations kan kun konfigureres i én valuta, som er valutaen i prislisteoverskriften.

1. Hvis du vil konfigurere faktureringssatser for arbejdskraft for en salgsprisliste, skal du oprette en prisliste, der er baseret på prislistens overskrift. 
2. På fanen **Rollepriser** skal du i undergitteret vælge **+ Ny rollepris**. 
3. I ruden **Hurtig oprettelse** skal du angive kombinationen af rolle og organisationsenhed, som du vil konfigurere faktureringssatsen for.

  Følgende tabel omfatter de felter på fanen **Generelt** og ruden **Hurtig oprettelse** for en rolleprislinje, som du skal være opmærksom på, når du opretter rollepriser på en salgsprisliste:

  | Felt | Lokation | Beskrivelse | Downstream-virkning |
  | --- | --- | --- | --- |
  | Rolle | Fanen **Generelt** og ruden **Hurtig oprettelse** | Vælg den rolle, som du vil angive faktureringssatsen for. | Rollen på det indgående estimat eller den faktiske oplysning sammenholdelse med denne linje for at angive standardfaktureringssatsen for rollen. |
  | Ressourceenhed | Fanen **Generelt** og ruden **Hurtig oprettelse** | Vælg organisationsenheden eller divisionen for den virksomhed, som rollen stammer fra. En udvikler fra Fabrikams Robotics-afdeling i Indien eller en udvikler fra Fabrikams softwareafdeling i USA. | Ressourceenheden på det indgående estimat eller den faktiske oplysning sammenholdelse med denne linje for at angive standardfaktureringssatsen for rollen. |
  | Pris | Fanen **Generelt** og ruden **Hurtig oprettelse** | Konfigurer faktureringssatsen for kombinationen af rollens ressourcevirksomhed og ressourceenhed. En udvikler fra Fabrikam i Indien har f.eks. en faktureringssats på 100 USD, eller en udvikler fra Fabrikam i USA har en faktureringssats på 150 USD. | Denne pris er standardfaktureringssatsen pr. enhedspris for den indgående estimatlinje eller faktiske linje for tidstransaktionsklassen. |
  | Valuta | Fanen **Generelt** og ruden **Hurtig oprettelse**| Valutaen hentes som standard fra valutaen i overskriften til salgsprislisten. På en salgsprisliste kan valutaen ikke tilsidesættes. | Denne valutas er standardvalutaen pr. enhedspris for den indgående faktiske salgslinje for tidstransaktionsklassen. |
  | Enhedsplan | Fanen **Generelt** og ruden **Hurtig oprettelse** | Standarden for denne enhedsplan er tid, og dette kan ikke ændres på rollens prisobjekt, da det bruges til at udtrykke satser pr. tidsenhed. | Dette felt har ingen afledt virkning. |
  | Enhed | Fanen **Generelt** og ruden **Hurtig oprettelse** | Enhedsværdien hentes fra feltet **Tidsenhed** i overskriften til salgsprislisten. Men værdien kan tilsidesættes. En udvikler fra Fabrikam i Indien har f.eks. en faktureringssats på 1.000 USD pr. **dag i Indien**. En udvikler fra Fabrikam i USA har en faktureringssats på 1.500 USD pr. **dag i USA**. | Når standarderne for pr. enhed vises på en indgående estimatlinje eller en faktisk linje, bruger systemet systemet med enheder og konvertering i basisenheder til at beregne en pris pr. enhed. Estimatet er f.eks. arbejde i 10 **dage i Indien** for en udvikler fra Indien, og enheden dag i Indien er angivet til 10 timer. Når estimatlinjen prisfastsættes, beregner programmet enhedsprisen på estimatet som 1.000 USD/10 timer = 100 USD pr. time. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Prisfastsættelse af overførsel eller konfiguration af faktureringssatser for ressourcer fra andre organisationsenheder eller afdelinger 

Projektbaserede virksomheder, som bruger medarbejdere fra forskellige afdelinger i virksomheden til at arbejde på projekter. Projekter kan udføres fra én afdeling, mens medarbejdere eller konsulenter kommer fra en anden opdeling i virksomheden. Projektet kan også bestå af en kombination af personer fra forskellige afdelinger. I Project Operations kaldes den virksomhed, der ejer leveringen af projektet, for **Kontraktenheden**. Alle de andre afdelinger, der leverer ressourcer, kaldes **Ressourceenheder**. På grund af forskelle i arbejdskraftomkostninger på tværs af forskellige geografier og arbejdsmarkeder over hele verden, er faktureringssatserne for arbejdskraft også konfigureret forskelligt for de forskellige geografier.

En udvikler fra Fabrikam i Indien, som arbejder på et projekt fra USA, faktureres f.eks. til en sats på 100 USD pr. time. En udvikler fra Fabrikam i USA, som arbejder på et projekt fra USA, faktureres 150 USD pr. time.

### <a name="example-set-up-a-bill-rate"></a>Eksempel: konfiguration af en faktureringssats

1. Opret en salgsprisliste med navnet *Faktureringssatser for Fabrikam i USA*, og angiv ikrafttrædelsesdatoen.
2. Angiv følgende satsoplysninger i salgsprislisten:

    | Rolle | Afdeling | Fakturasats |
    | --- | --- | --- |
    | Udvikler | Fabrikam i Indien | 100 $ |
    | Udvikler | Fabrikam i Filippinerne | 90 $ |
    | Udvikler | Fabrikam i USA | 150 $ |

3. Knyt salgsprislisten **Faktureringssatser for Fabrikam i USA** til projektets prisliste for projektkontrakten eller til et bestemt firma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]