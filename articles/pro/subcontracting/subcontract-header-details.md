---
title: Detaljer på hovedsiden for underentrepriser
description: I denne artikel forklares funktionaliteten i underleverandørens overskrift i Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 00b7c08235654d4bed0bcb4053d2044a3d092b54
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522553"
---
# <a name="header-details-for-subcontracts"></a>Detaljer på hovedsiden for underentrepriser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I denne artikel forklares funktionaliteten i underleverandørens overskrift i Dynamics 365 Project Operations.

Da projektleder planlægger og udfører projekter, ansætter de muligvis underleverandører og køber produkter og tjenester fra leverandører. Når en projektleder skal købe produkter eller tjenester, kan de oprette en underentreprise i Project Operations.

Udfør disse trin for at oprette en underentreprise.

1. I navigationsruden skal du vælge **Underentrepriser**, og på siden **Underentreprise** skal du vælge **Ny**.
2. Angiv de nødvendige oplysninger, og vælg derefter **Gem**.

    Følgende tabel indeholder oplysninger om felterne på siden for **Overskrift for underentreprise**.

    | Felt | Beskrivelse |Funktionspåvirkninger |
    |---|------|---| 
    | Navn | Navnet på underentreprisen. | I alle rullelister for underentrepriser vises navnet på underentreprisen i første kolonne for at hjælpe dig med at identificere underentreprisen. | 
    | Beskrivelse | En kort beskrivelse af de tjenester og produkter, der købes på baggrund af underentreprisen. | Intet |
    | Leverandør | Navnet på den virksomhed, som produkterne og tjenesterne købes fra. Denne firmapost har relationstypen **Leverandør** eller **Forsyningsvirksomhed**. | På baggrund af den valgte leverandør angives automatiske standardværdier for følgende felter:<br/> **• Valuta** </br> **• Prislister** </br> **• Betalingsbetingelser**</br> **• Betalingsadresse**</br> **• Faktureringsadresse**</br> **• Faktureringsnavn** </br>**• Account Manager for leverandør**|
    | Underentreprisedato | Den dato, hvor underentreprisen oprettes. | Datoen for underentreprisen bruges til at vælge den rette købsprisliste fra enten de prislister, der er knyttet til den relaterede leverandør, eller fra projektparametrene. |
    | Statusårsag | Statussen for underentreprisen. | Statussen bestemmer, hvor underentreprisen befinder sig i forretningsprocessen, og om den kan redigeres. <br/>Værdierne omfatter:<br>• **Kladde**: Underentreprisen kan redigeres. Du kan kun redigere underentrepriser med statussen **Kladde**.<br/>• **Bekræftet**: Forhandlingen med leverandøren er afsluttet, og underentreprisen godkendes til levering. <br/>• **Lukket**: Underentreprisen er blevet leveret.<br/>• **Annulleret**: Underentreprisen blev annulleret, og der er ikke planlagt levering.  | 
    | Valuta | Den valuta, som produkter og tjenester købes i. Standardværdien angives automatisk fra leverandørens konto, men den kan ændres. | Underentreprisens valuta bruges til at vælge købsprislisten fra enten de prislister, der er knyttet til den relaterede leverandør, eller fra projektparametrene. Prislister i en anden valuta kan ikke knyttes til underentreprisen. Den tid, de udgifter og det materiale, som leverandørressourcerne leverer fra denne underentreprisen, registreres i denne valuta i projektet. Når underentrepriseposten er gemt, kan valutaen for underentreprisen ikke ændres.|
    | Kontraktenhed | Den afdeling af virksomheden, der indgår en købskontrakt eller en underentreprise med leverandøren. | Intet |
    | Betalingsbetingelser | Betalingsbetingelserne på leverandørfakturaer, der er udstedt på denne underentreprise. Standardværdien angives automatisk fra leverandørens firmapost. | Betalingsbetingelser fra underentreprisen kopieres til alle leverandørfakturaer, der er relateret til denne underentreprise. Betalingsbetingelserne kan opdateres, hvis underentreprisen har statussen **Kladde**. | 
    | Betalingsadresse | Adressen på den leverandør, som betalinger skal sendes til. Standardværdien angives automatisk fra leverandørens firmapost. | Betalingsadressen fra underentreprisen kopieres som betalingsadresse til alle de leverandørfakturaer, der er oprettet for denne underentreprise. Betalingsadressen kan opdateres, hvis underentreprisen har statussen **Kladde**.|
    | Faktureringsnavn | Navnet på den person eller afdeling i leverandørens virksomhed, som skal sende fakturaen. Standardværdien angives automatisk fra leverandørens firmapost. | Værdien **Faktureringsnavn** fra underentreprisen kopieres til alle leverandørfakturaer, der er relateret til denne underentreprise. Dette felt kan opdateres, hvis underentreprisen har statussen **Kladde**.|
    | Faktura til Adresse | Den adresse, der bruges på fakturaer fra leverandøren. Standardværdien angives automatisk fra leverandørens firmapost. | Denne adresse er adressen for "faktura fra" på de leverandørfakturaer, der oprettes for denne underentreprise. |
    | Subtotal | Hvis der ikke er nogen linjer for en underentreprise, skal du angive delsummen for ordren eksklusiv moms. Hvis underentreprisen har linjer, er dette felt skrivebeskyttet. Det viste beløb er delsummen for alle linjer på underentreprisen. | Intet |
    | Samlet moms | Hvis der ikke er nogen linjer for en underentreprise, skal du angive den samlede moms for denne underentreprise. Hvis underentreprisen har linjer, er dette felt skrivebeskyttet. Det viste beløb er summen af momsbeløbet for alle linjer på underentreprisen. | Intet |
    | Samlet beløb | I dette beregnede felt vises det samlede beløb for underentreprisen inklusive moms. | Intet |
    | Dato bekræftet | Datoen, hvor underentreprisen blev bekræftet. | Intet |
    | Anmodet af | Som standard angives dette felt til navnet på den bruger, der opretter underentreprisen. Men den person, der har oprettet underentreprisen, kan ændre værdien for at angive den person, som vedkommende opretter underentreprisen på vegne af. | Intet |
    | Kreditorkontochef | Navnet på den primære kontaktperson for leverandørkontoen. Standardværdien angives automatisk fra leverandørens firmapost. Du kan vælge en anden kontaktperson som account manager for leverandøren af underentreprisen. | Du kan konfigurere mailbeskeder for at give kontaktpersonen besked, når der foretages ændringer af underentreprisen som følge af prisforhandlinger. |
