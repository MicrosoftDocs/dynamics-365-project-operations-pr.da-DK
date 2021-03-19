---
title: Rettede fakturaer - lille
description: Dette emne indeholder oplysninger om rettede fakturaer i Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274226"
---
# <a name="corrected-invoices---lite"></a>Rettede fakturaer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

En bekræftet projektfaktura kan rettes for at behandle ændringer eller kreditter i henhold til forhandlinger mellem kunden og projektlederen.

Hvis du vil foretage ændringer af en bekræftet faktura, skal du åbne den bekræftede faktura og vælge **Ret denne faktura**. 

> [!NOTE]
> Denne markering er ikke tilgængelig, medmindre en projektfaktura er bekræftet.

Der oprettes en ny kladdefaktura ud fra den bekræftede faktura. Alle fakturalinjedetaljer fra den tidligere bekræftede faktura kopieres til den nye kladde. Her følger nogle af de vigtigste punkter om linjedetaljerne i den nye rettede faktura:

- Alle mængder opdateres til nul. Programmet antager, at alle fakturerede varer er helt krediteret. Hvis det er nødvendigt, kan du opdatere mængderne manuelt, så det afspejler det antal, der er ved at blive faktureret, og ikke det antal, der krediteres. På baggrund af det antal, du angiver, beregner programmet det krediterede antal. Beløbet afspejles i de faktiske tal, der oprettes, når den rettede faktura bekræftes. Hvis du foretager ændringer i momsbeløbet, skal du angive det korrekte momsbeløb og ikke det momsbeløb, der krediteres.
- Tidligere bekræftede produktbaserede kontraktlinjer kopieres ikke. Behandling af rettelser på en produktbaseret projektfaktura understøttes ikke.
- Rettelser i relation til milepæle behandles altid som komplette kreditter.
- Forskudshonorar eller forskudsbeløb kan rettes, hvis kunden er faktureret et forkert beløb.
- Afstemninger af forskudshonorarer og forskud kan rettes, hvis der er brugt et forkert beløb til at afstemme i forhold til gebyrerne på en tidligere bekræftet faktura.

> [!IMPORTANT]
> De fakturalinjedetaljer, der er rettelser til andre allerede fakturerede opkrævninger, har feltet **Rettelse** angivet til **Ja**. Fakturaer, der har rettede fakturalinjedetaljer, har et felt kaldet **Indeholder rettelser**, der også er angivet til **Ja**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Faktiske tal, der er oprettede på Bekræftelse af en rettelsesfaktura:

Nedenfor vises de faktiske oplysninger, som er oprettet af programmet ved bekræftelse af rettelse på baggrund af de handlinger, der udføres på kladden for rettelsesfakturaen før bekræftelse.

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
Milepælsfakturaen eller faktureringsstatussen på projektkontraktlinjen opdateres til **Klar til at blive faktureret**.
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
        <tr>
            <td width="216" valign="top">
                <p>
Kreditter og korrektioner for en tidligere faktureret produktbaseret kontraktlinje.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Understøttes ikke </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]