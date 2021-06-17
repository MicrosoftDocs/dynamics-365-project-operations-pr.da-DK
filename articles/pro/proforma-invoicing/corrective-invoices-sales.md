---
title: Korrigerende projektfakturaer
description: Dette emne indeholder oplysninger om, hvordan du opretter og bekræfter korrigerende fakturaer i Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004074"
---
# <a name="corrective-project-invoices"></a>Korrigerende projektfakturaer

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

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Faktiske tal, der blev oprettet, da en korrigerende faktura blev bekræftet

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
Fakturering af den fulde kredit for en tidligere faktureret materialetransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførsel af et faktureret salg for mængden og beløbet på den oprindelige fakturalinjedetaljer for materiale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny faktisk værdi for ikke-faktureret salg for mængden og beløbet på den oprindelige fakturalinjedetaljer for materiale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering af den delvise kredit på en materialetransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførsel af et faktureret salg for den fakturerede mængde og beløb på den oprindelige fakturalinjedetaljer for materiale.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny faktisk værdi for ikke-faktureret salg, der kan faktureres for mængden og beløbet på den redigerede fakturalinjedetalje, en tilbageførsel heraf, og et tilsvarende faktureret faktisk salg.
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
Fakturastatussen for milepælen opdateres fra <b>Bogført kundefaktura</b> til <b>Klar til fakturering</b>.
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
