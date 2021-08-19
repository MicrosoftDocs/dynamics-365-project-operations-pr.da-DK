---
title: Vigtige begreber inden for underleverancer
description: I denne emne forklares nogle vigtige begreber, der gælder for underleverancer i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994269"
---
# <a name="key-concepts-in-subcontracting"></a>Vigtige begreber inden for underleverancer

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I emnet forklares nogle vigtige begreber, som du skal være opmærksom på, før du begynder at bruge underleverandørfunktionen i Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Ordregivende enhed for underleverancen

Ordregiveren repræsenterer den afdeling eller praksis, der står for leveringen af det endelige projekt. Ordregiveren er også den afdeling, der indgår kontraktforholdet med leverandøren.

## <a name="purchase-currency"></a>Købsvaluta

I Project Operations er købsvalutaen den valuta, som underleverancen oprettes i. Det er også den valuta, som underleverandøromkostninger for et projekt registreres i. Købsvalutaen kan afvige fra projektvalutaen, og projektvalutaen kan igen afvige fra salgsvalutaen.

## <a name="billing-methods-on-subcontract-lines"></a>Faktureringsmetoder for underleverancelinjer

For projekter findes der typisk kontraktmodeller, der henholdsvis er baseret på faste gebyrer og forbrug. Project Operations understøtter disse faktureringsmetoder i salgs- og købskonteksterne. Ved et køb fungerer faktureringsmetoder på følgende måde:

- **Tid og materiale** – Når en underleverancelinje bruger faktureringsmetoden **Tid og materiale**, registreres tidsomkostningerne på projektet, når underleverandører arbejder på det pågældende projekt og registrerer tid. Disse omkostningsposteringer fra underleverandører matches derefter med linjeelementerne på leverandørens fakturaer. I denne model kan projektledere, der bruger Project Operations, sammenholde og kontrollere leverandørfakturalinjer i forhold til den underleverandørtid, der registreres og godkendes. Når bekræftelsen er fuldført, tilbageføres tidligere omkostningsoplysninger, som er registreret efter godkendelsen, og der oprettes nye faktiske omkostningsoplysninger, der er baseret på leverandørfakturaen for projektet.
- **Fast pris** – I denne kontraktmodel baseret på faste gebyrer er leverandørens fakturaer baseret på faste milepæle. Underleverandørressourcer kan dog også rapportere tid. Tiden gennemgås og godkendes derefter af projektlederen. Når den er godkendt, opretter Project Operations godkendes midlertidige omkostningsoplysninger for projektet. Når leverandøren har sendt en faktura for en milepæl, kan projektlederen sammenholde tidligere registrerede faktiske omkostninger med milepælen. Når bekræftelsen er fuldført, tilbageføres de faktiske omkostninger, og de milepælsbaserede omkostninger registreres.

## <a name="project-price-lists-on-subcontracts"></a>Projektprislister for underleverancer

Projektprislister er prislister, der bruges til at konfigurere købspriser for tid, udgifter og andre projektrelaterede komponenter. Der kan være flere prislister, som kan have hver sin underleverandør for et datointerval i Project Operations. Project Operations understøtter ikke overlappende datointervaller for projektprislister for en underleverance.

## <a name="transaction-classes-on-subcontracts"></a>Posteringsklasser for underleverancer

Project Operations understøtter fire typer transaktionsklasser:

- Tid
- Udgift
- Materiale
- Gebyr

Købsomkostninger kan kun estimeres og pålægges for posteringsklasserne **Tid**, **Udgift** og **Materiale**. **Gebyr** er en transaktionsklasse, der kun gælder for omsætning, og er ikke tilgængelig angående køb.

## <a name="purchase-pricing-dimensions"></a>Dimensioner for prisfastsættelse ved køb

Med dimensioner for prisfastsættelse kan du bestemme, hvilke attributter der bruges til at opsætte købspriser og standardtidsfrister for transaktioner. I forbindelse med indkøb understøtter Project Operations kun faste dimensioner ved opsætning af købspriser og standardindstillinger. I forbindelse med opsætning af købspriser og standardindstillinger for underleverancelinjer og underleverancers tidstransaktioner er de tilgængelige attributter **Rolle** og **Reserverbar ressource**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]