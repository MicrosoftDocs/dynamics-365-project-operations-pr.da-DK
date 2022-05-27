---
title: Administration af kreditorer og købsprislister i Project Operations
description: Denne emne indeholder oplysninger, der kan hjælpe dig med at oprette og vedligeholde kreditordata og købsprislister for underleverancer.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576723"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Administration af kreditorer og købsprislister i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

## <a name="vendors-in-project-operations"></a>Leverandører i Project Operations

I Microsoft Dynamics 365 Project Operations har leverandørkonti relationstypen **Kreditor** eller **Leverandør**. Du kan kun vælge en firmapost, hvor en af disse relationstyper er angivet som leverandør for en underleverance.

Du kan knytte en eller flere købsprislister til en leverandørpost. Hver købsprisliste, der er knyttet til en leverandørpost, skal dog have et tydeligt datointerval. Project Operations understøtter ikke overlappende datointervaller for købsprislister.

Følgende felter og begreber for en leverandørpost bruges som standard til alle underleverancer, der oprettes for leverandøren:

- Betalingsbetingelser
- Faktura til kontaktnavn
- Primær kontakt

    > [!NOTE]
    > Leverandørens primære kontaktperson bruges som standard som leverandørkontoadministrator for underleverancen.

- Valuta
- Aktuelle købsprislister

## <a name="purchase-price-lists-in-project-operations"></a>Købsprislister i Project Operations

En prisliste, hvor feltet **Kontekst** er angivet til **Køb**, betragtes som en købsprisliste. Købsprislister kan defineres til at repræsentere et katalog over købspriser for tid, udgifter og materialer. Købsprislister ligner kost- og salgsprislister i Project Operations. Følgende begreber gælder for købsprislister på samme måde, som de gælder for kost- og salgsprislister:

- **Datointerval** – Købsprislister har datointervaller. Datointervaller er defineret af start- og slutdatofelter for hver prisliste. Tiden mellem startdatoen og slutdatoen er det omfattede datointerval.
- **Valuta** – Valutaen i prislistehovedet bruges som den valuta, som købspriser udtrykkes i for arbejdskraft, udgiftskategorier og produkter i kataloget.
- **Standardtidsenhed** – Standardtidsenheden angiver arbejdskraftpriser for køb. Tidsenhedsfeltet på en prisliste bruges kun til at angive en standardværdi. Denne værdi kan ændres på individuelle rolleprisrækker.

Købsprislister kan knyttes til leverandørposter som tilknytninger, der kaldes projektprislister. Disse prislister bruges til at angive standardpriser på underleverancelinjer. Når der knyttes flere købsprislister til en leverandørpost, bruges den nyeste prisliste som standard til underleverancer, der oprettes for leverandøren. Det er kun prislister, hvor feltet **Kontekst** er angivet til **Køb**, der kan knyttes til leverandørposter.

### <a name="subcontract-specific-purchase-price-lists"></a>Underleverandørspecifikke købsprislister

Købsprislister kan også knyttes til underleverancer som tilknytninger, der kaldes projektprislister. Disse prislister bruges til at angive standardpriser på underleverancelinjer. Når der er knyttet flere købsprislister til en underleverance, skal hver af dem som standard have et særskilt datointerval. Project Operations understøtter ikke købsprislister med overlappende datointervaller. Det er kun prislister, hvor feltet **Kontekst** er angivet til **Køb**, der kan knyttes til underleverancer.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
