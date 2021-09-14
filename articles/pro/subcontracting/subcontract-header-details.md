---
title: Detaljer på hovedsiden for underentrepriser
description: I emne forklares funktionaliteten på hovedsiden for underentrepriser i Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323634"
---
# <a name="header-details-for-subcontracts"></a>Detaljer på hovedsiden for underentrepriser

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Dette emne forklarer funktionaliteten på hovedsiden for underentrepriser i Dynamics 365 Project Operations.

Da projektleder planlægger og udfører projekter, ansætter de muligvis underleverandører og køber produkter og tjenester fra leverandører. Når en projektleder skal købe produkter eller tjenester, kan de oprette en underentreprise i Project Operations.

Udfør disse trin for at oprette en underentreprise.

1. I navigationsruden skal du vælge **Underentrepriser**, og på siden **Underentreprise** skal du vælge **Ny**.
2. Angiv de nødvendige oplysninger, og vælg derefter **Gem**.

    Følgende tabel indeholder oplysninger om felterne på hovedsiden for underentrepriser.

    | **Felt** | **Beskrivelse** |
    | --- | --- | 
    | Navn | Navnet på underentreprisen. |
    | Beskrivelse | En kort beskrivelse af de tjenester og produkter, der købes på baggrund af underentreprisen. |
    | Leverandør | Navnet på den virksomhed, som produkterne og tjenesterne købes fra. Denne firmapost har relationstypen **Leverandør** eller **Forsyningsvirksomhed**. |
    | Underentreprisedato | Datoen for oprettelse af underentreprisen. |
    | Statusårsag | Statussen for underentreprisen. |
    | Valuta | Den valuta, som produkter og tjenester købes i. Værdien i dette felt hentes som standard fra leverandørkontoen, men den kan ændres. Projektprislister, der bruges til prisfastsættelse af produkter og tjenester i underentreprisen, skal være i denne valuta. Prislister i andre valutaer kan ikke knyttes til underentreprisen. De påløbne omkostninger for underentreprisens produkter og tjenester registreres i denne valuta på projektet. |
    | Kontraktenhed | Den afdeling af virksomheden, der indgår en købskontrakt eller en underentreprise med leverandøren. |
    | Betalingsbetingelser | Betalingsbetingelserne på de leverandørfakturaer, der er udstedt for denne underentreprise. Værdien i dette felt hentes som standard fra leverandørens firmapost. |
    | Betalingsadresse | Den adresse, hvortil betalingen for leverandørfakturaer sendes. Værdien i dette felt hentes som standard fra leverandørens firmapost. |
    | Faktureringsnavn | Navnet på den person eller afdeling i leverandørens virksomhed, som skal sende fakturaen. Værdien i dette felt hentes som standard fra leverandørens firmapost og bruges som navnet på den primære kontaktperson på de leverandørfakturaer, der er oprettet for denne underentreprise. |
    | Faktureringsadresse | Den adresse, der bruges på fakturaer fra denne leverandør. Værdien i dette felt hentes som standard fra leverandørens firmapost. Denne adresse bruges også som afsenderadressen på de leverandørfakturaer, der er oprettet for denne underentreprise. |
    | Subtotal | Hvis en underentreprise ikke har nogen linjer, skal du indtaste en værdi i dette felt, der angiver ordrens delsum før moms. Hvis underentreprisen har linjer, er dette felt skrivebeskyttet. Det viste beløb er delsummen fra alle linjer i underentreprisen. |
    | Samlet moms | Hvis en underentreprise ikke har nogen linjer, skal du indtaste en værdi i dette felt, der angiver momsen for denne underentreprise. Hvis underentreprisen har linjer, er dette felt skrivebeskyttet. Det viste beløb er summen af momsbeløber fra alle linjer i underentreprisen. |
    | Samlet beløb |  I dette beregnede felt vises det samlede beløb for underentreprisen inklusive moms.  |
    | Dato bekræftet | Datoen, hvor underentreprisen blev bekræftet.  |
    | Anmodet af | Værdien i dette felt henter som standard til navnet på den bruger, der opretter underentreprisen. Denne værdi kan ændres af den person, der har oprettet underentreprisen, for at angive, hvem vedkommende opretter underentreprisen for.  |
    | Kreditorkontochef | Navnet på den primære kontaktperson for leverandørkontoen. Værdien i dette felt hentes som standard fra leverandørens firmapost. Denne feltværdi kan ændres af brugeren, så brugeren kan vælge en anden kontaktperson som administrator af underentreprisens leverandørkonto. Mailbeskeder og prisforhandlinger kan konfigureres og fremsendes af denne kontakt. |


