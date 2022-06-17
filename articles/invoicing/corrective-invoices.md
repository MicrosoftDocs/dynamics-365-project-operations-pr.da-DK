---
title: Opret korrigerende projektbaserede fakturaer
description: Denne artikel indeholder oplysninger om korrigerende fakturaer i Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 86bb05242c74e97533c7555ffa645278c8519430
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927873"
---
# <a name="create-corrective-project-based-invoices"></a>Opret korrigerende projektbaserede fakturaer 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En bekræftet projektfaktura kan rettes for at behandle ændringer eller kreditter i henhold til forhandlinger mellem kunden og projektlederen.

Hvis du vil foretage ændringer af en bekræftet faktura, skal du åbne den bekræftede faktura og vælge **Ret denne faktura**. 

> [!NOTE]
> Denne markering er ikke tilgængelig, medmindre en projektfaktura er bekræftet.

Der oprettes en ny kladdefaktura ud fra den bekræftede faktura. Alle fakturalinjedetaljer fra den tidligere bekræftede faktura kopieres til den nye kladde. Følgende er nogle af de vigtige punkter, der kan hjælpe dig med bedre at forstå linjedetaljerne på den nye korrigerede faktura:

- Alle mængder opdateres til nul. Dette forudsætter, at alle fakturerede elementer er fuldt krediteret. Hvis det er nødvendigt, kan du opdatere mængderne manuelt, så det afspejler det antal, der er ved at blive faktureret, og ikke det antal, der krediteres. På baggrund af det antal, du angiver, beregner programmet det krediterede antal. Beløbet afspejles i de faktiske tal, der oprettes, når den rettede faktura bekræftes. Hvis du foretager ændringer i momsbeløbet, skal du angive det korrekte momsbeløb og ikke det momsbeløb, der krediteres.
- Rettelser i relation til milepæle behandles altid som komplette kreditter.
- Forskudshonorar eller forskudsbeløb kan rettes, hvis kunden er faktureret et forkert beløb.
- Afstemninger af forskudshonorarer og forskud kan rettes, hvis der er brugt et forkert beløb til at afstemme i forhold til gebyrerne på en tidligere bekræftet faktura.

> [!IMPORTANT]
> Fakturalinjedetaljer, der er rettelser til andre allerede fakturerede opkrævninger, har feltet **Korrektion** angivet til **Ja**. Fakturaer, der har rettede fakturalinjedetaljer, har et felt kaldet **Indeholder rettelser**, der også er angivet til **Ja**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Faktiske tal, der er oprettede på Bekræftelse af en rettelsesfaktura

I følgende tabel vises de faktiske værdier, der oprettes, når en korrigerende faktura bekræftes.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenarie</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>De faktiske oplysninger, der blev oprettet i forbindelse med bekræftelse</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Bekræfte rettelsen af et faktureret forskudshonorar eller forskud.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning. Dette beløb er positivt, fordi det skal annullere det negative beløb, der blev oprettet, da forskudshonoraret eller forskuddet blev faktureret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Der oprettes en tilbageførelse af et faktureret faktisk salg lydende på beløbet for forskudshonoraret eller forskuddet for at tilbageføre det oprindelige fakturerede salg.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Der oprettes en ny fakturering for faktisk salgsværdi for det rettede beløb på den rettede fakturalinje for forskudshonoraret eller forskuddet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb for den forskudshonorarbaserede eller forskudsbaserede fakturalinje, som skal anvendes til afstemningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Bekræftelse af rettelsen af et tidligere afstemt forskudshonorar eller forskud.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning. Dette beløb er positivt og skal udligne det negative beløb, der blev oprettet, da den tidligere afstemning blev foretaget.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Tilbageførelse af fakturering af en faktisk salgsværdi svarende til beløbet på den forrige faktura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny fakturering for faktisk salgsværdi for det rettede beløb for forskudshonoraret, som anvendes på den rettede faktura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb fra det resterende beløb af forskudshonoraret eller forskuddet skal anvendes til afstemning af efterfølgende fakturaer.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af den fulde kredit for en tidligere faktureret tidstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførelse af faktureret salg for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi for tiden og beløbet på den oprindelige fakturalinjedetalje for tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering af den delvise kredit på en tidstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførelse af faktureret salg for tiden og beløbet faktureret på den oprindelige fakturalinjedetalje for tid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for de resterende timer og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af den fulde kredit for en tidligere faktureret udgiftstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for udgiften.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering af den delvise kredit for en tidligere faktureret udgiftstransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for en udgift.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbar for det resterende antal og beløb, efter at de rettede tal på fakturalinjedetaljen er blevet trukket fra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af den fulde kredit for en tidligere faktureret gebyrtransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførelse af faktureret salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi salg for antallet og beløbet på den oprindelige fakturalinjedetalje for gebyret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af den delvise kredit for en tidligere faktureret gebyrtransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførelse af faktureret salg for antallet og beløbet faktureret på den oprindelige fakturalinjedetalje for gebyr.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antallet og beløbet på den redigerede rettede fakturalinjedetalje, en tilbageførsel heraf og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering af den fulde kredit for en tidligere faktureret milepæl.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførelse af faktureret salg for beløbet på den oprindelige fakturalinjedetalje for milepælen.
                </p>
                <p>
Fakturastatussen på milepælen opdateres fra <b>Bogført kundefaktura</b> til <b>Klar til fakturering</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering af den delvise kredit for en tidligere faktureret milepæl.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Understøttes ikke </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
