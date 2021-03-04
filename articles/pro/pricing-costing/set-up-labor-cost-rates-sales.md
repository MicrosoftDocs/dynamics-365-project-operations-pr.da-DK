---
title: Konfigurer satser for arbejdskraftomkostninger - lille
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer omkostningssatser for arbejdskraft i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e79dde867833fb952349c073ce8975381029dcf
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180700"
---
# <a name="set-up-labor-cost-rates---lite"></a>Konfigurer satser for arbejdskraftomkostninger - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Hver prisliste har et sæt satser for arbejdskraft (rollepriser), der stemmer overens med indholdet og ikrafttrædelsesdatoen for prislisten.

1. Opret en prisliste, og vælg på fanen **Rollepris** i undergitteret **Ny rolle**.
2. På siden **Hurtig oprettelse** skal du vælge rollen og organisationsenheden.
3. Angiv eventuelle andre krævede feltoplysninger.

Følgende tabel indeholder nogle af de felter, der er vigtige, når du opretter arbejdskraftsatser på en kostprisliste.

| Felt | Lokation | Beskrivelse | Downstream-virkning |
| --- | --- | --- | --- |
| Rolle | Fanen **Generelt** og siderne **Hurtig oprettelse** | Vælg den rolle, som omkostningssatsen finder anvendelse for. | Rollen på det indgående estimat eller den faktiske oplysning sammenholdelse med denne linje for at angive standarden for rollens omkostning. |
| Ressourceenhed | Fanen **Generelt** og siderne **Hurtig oprettelse** | Vælg organisationsenheden eller afdelingen i den virksomhed, hvor denne rollen skal anvendes. En udvikler fra Fabrikams Robotics-afdeling i Indien eller en udvikler fra Fabrikams softwareafdeling i USA. | Ressourceenheden på det indgående estimat eller den faktiske oplysning sammenholdelse med denne linje for at angive standarden for rollens omkostning. |
| Pris | Fanen **Generelt** og siderne **Hurtig oprettelse** | Konfigurer omkostningssatsen for kombinationen rolle, ressourcevirksomhed og ressourceenhed. En udvikler fra Fabrikam i Indien koster eksempelvis 1.000 INR eller en udvikler fra Fabrikam i USA, som koster 150 USD. | Prisen er den omkostningssats, hvis standard er baseret på pr. enhedsomkostning for det indgående estimat eller den faktiske linje for transaktionsklassen **Tid**. |
| Valuta | Fanen **Generelt** og siderne **Hurtig oprettelse** | Valutaen hentes som standard fra valutaen i overskriften til omkostningsprislisten, men kan tilsidesættes. En udvikler fra Fabrikam i Indien koster f.eks. 1.000 INR. En udvikler fra Fabrikam i USA koster 150 USD. | Denne valutas standard hentes fra pr. enhedsomkostningen for den indgående faktiske omkostningsbasis for transaktionsklassen **Tid**. I et projektestimat konverteres valutaværdien til projektvalutaen og vises på estimatets tidsinddelte visning. |
| Enhedsplan | Fanen **Generelt** og siderne **Hurtig oprettelse** | Standarden for enhedsplanen er tid, og dette kan ikke ændres på rollens prisobjekt, da det bruges til at udtrykke satser pr. tidsenhed. | Dette har ingen afledt indvirkning. |
| Enhed | Fanen **Generelt** og siderne **Hurtig oprettelse** | Værdien hentes som standard fra feltet **Tidsenhed** i overskriften til omkostningsprislisten. Værdien kan tilsidesættes. En udvikler fra Fabrikam i Indien koster f.eks. 1.000 INR pr. **dag i Indien**. En udvikler fra Fabrikam USA koster 150 USD pr. **dag i USA**. | Systemet bruger systemet med enheder og konvertering i basisenheder til at beregne en pris pr. enhed for at beregne standardprisen pr. enhed på en indgående estimatlinje eller en faktisk linje. Et estimat er f.eks. arbejde i 10 **dage i Indien** for en udvikler fra Indien, og enheden **dag i Indien** er angivet til 10 timer. I forbindelse med omkostningsfastsættelse af den pågældende estimatlinje beregner programmet enhedsomkostningen på estimatet som: 1.000 INR/10 timer = 100 INR pr. time, hvilket konverteres til USD og vises som enhedsomkostningen på siden **Projektestimater**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Overførsel af priser og omkostninger for ressourcer uden for din afdeling eller juridiske enhed

I projektbaserede virksomheder er det almindeligt at anvende medarbejdere fra andre juridiske enheder eller afdelinger på projekter. Et projekt kan udføres af en bestemt juridisk enhed, men medarbejdere eller konsulenter, der arbejder på projektet, kan komme fra samme juridiske enhed eller en anden eller måske en kombination af begge. I Dynamics 365 Project Operations er den juridiske enhed, der ejer leveringen af projektet, den **Ejende virksomhed**, og den afdeling, der ejer leveringen, er **Kontraktenheden**. Andre juridiske enheder, der leverer ressourcer, kaldes **Ressourcevirksomheder**, og de afdelinger, der leverer ressourcer, kaldes **Ressourceenheder**. I de fleste lande er virksomheder forpligtet til at sikre, at den juridiske ressourceenhed eller afdeling opkræver betaling ved den ejende virksomhed og kontraktenheden for at bruge ressourcerne.

Fabrikam-koncernen skal f.eks. sikre, at Fabrikam Robotics i Indien har forhandlet en omkostningssatstabel med Fabrikam Robotics i USA eller Fabrikam Robotics i Storbritannien.

En udvikler fra Fabrikam Robotics i Indien opkræver 100 $, når denne udlånes til Fabrikam Robotics i USA, og 150 $, når denne udlånes til Fabrikam Robotics i Storbritannien.

### <a name="set-up-costs-for-outside-resources"></a>Konfigurer omkostninger for eksterne ressourcer

1. Opret en kostprisliste kaldet *Omkostningssatser for Fabrikam Robotics i USA*, og angiv et interval for ikrafttrædelsesdatoen.
2. Konfigurer satser i kostpriselisten ved hjælp af oplysninger fra følgende tabel. 

| Rolle | Ressourcevirksomhed | Ressourceenhed | Omkostningssats |
| --- | --- | --- | --- |
| Udvikler | Fabrikam i Indien | Fabrikam i Indien-Robotics | 100 $ |
| Udvikler | Fabrikam i Filippinerne | Fabrikam i Filippinerne-Robotics | 90 $ |
| Udvikler | Fabrikam i USA | Fabrikam i USA-Robotics | 150 $ |

3. Knyt denne kostprisliste til organisationsenheden Fabrikam Robotics i USA.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Konfigurer prisfastsættelse af overførsler for en ressource i den relevante valuta 

I Project Operations er det muligt at konfigurere prisfastsættelse af ressourcer i alle valutaer. Valutaen er som standard angivet til det, der er angivet i prislistens overskriften, men den kan ændres.

Når eksemplet med overførselspriser er konfigureret, kan oplysningerne ændres til:

Fabrikam-koncernen skal at Fabrikam Robotics i Indien har forhandlet en omkostningssats med Fabrikam Robotics i USA eller Fabrikam Robotics i Storbritannien.

En udvikler fra Fabrikam Robotics i Indien koster 5.000 INR, når denne udlånes til Fabrikam Robotics i USA, og 5.500 INR, når denne udlånes til Fabrikam Robotics i Storbritannien.

På kostprislisten for Fabrikam i USA-Robotics kan omkostningssatser udtrykkes som:

| Rolle | Ressourcevirksomhed | Omkostning |
| --- | --- | --- |
| Udvikler | Fabrikam i Indien | 5.000 INR |
| Udvikler | Fabrikam i USA | 115 USD |

På kostprislisten for Fabrikam i Storbritannien-Robotics kan omkostningssatser udtrykkes som nedenfor angivet:

| Rolle | Ressourcevirksomhed | Omkostning |
| --- | --- | --- |
| Udvikler | Fabrikam i Indien | 5.500 INR |
| Udvikler | Fabrikam i Storbritannien | 115 GBP |

Kostprislisten kan levere satser for arbejdskraft i flere valutaer. Når der genereres et omkostningsestimat for projektet, konverterer Project Operations disse omkostningssatser til projektvalutaen og viser dem til brugeren. Når en tidsregistrering godkendes, og der oprettes et faktisk omkostningsbeløb, prisfastsættes den faktiske omkostning i den valuta, der gælder for den tilsvarende rolleprislinje på kostprislisten. Faktiske omkostninger for tid på et enkelt projekt kan registreres i flere valutaer. Når Project Operations akkumulerer eller opsummerer de faktiske omkostninger til arbejdskraft på projektniveau, konverteres alle omkostninger til arbejdskraft til projektvalutaen, som brugeren kan få vist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]