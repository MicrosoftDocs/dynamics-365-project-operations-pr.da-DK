---
title: Korrigerende projektbaserede fakturaer
description: Denne artikel indeholder oplysninger om, hvordan du opretter og bekræfter korrigerende projektbaserede fakturaer i Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931093"
---
# <a name="corrective-project-based-invoices"></a>Korrigerende projektbaserede fakturaer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En bekræftet projektfaktura kan rettes for at behandle ændringer eller kreditter i henhold til forhandlinger mellem kunden og projektlederen.

Hvis du vil foretage ændringer af en bekræftet faktura, skal du åbne den bekræftede faktura og vælge **Ret denne faktura**. 

> [!NOTE]
> Dette valg er ikke tilgængeligt, medmindre en projektfaktura er bekræftet, eller den projektbaserede faktura har forskud eller forskudshonorarer eller afstemninger af forskud eller forskudshonorarer.

Der oprettes en ny kladdefaktura ud fra den bekræftede faktura. Alle fakturalinjedetaljer fra den tidligere bekræftede faktura kopieres til den nye kladde. Her følger nogle af de vigtigste punkter om linjedetaljerne i den nye rettede faktura:

- Alle mængder opdateres til nul. Dynamics 365 Project Operations antager, at alle fakturerede elementer er fuldt krediteret. Hvis det er nødvendigt, kan du opdatere mængderne manuelt, så det afspejler det antal, der er ved at blive faktureret, og ikke det antal, der krediteres. På baggrund af det antal, du angiver, beregner programmet det krediterede antal. Beløbet afspejles i de faktiske tal, der oprettes, når den rettede faktura bekræftes. Hvis du foretager ændringer i momsbeløbet, skal du angive det korrekte momsbeløb og ikke det momsbeløb, der krediteres.
- Rettelser i relation til milepæle behandles altid som komplette kreditter.


> [!IMPORTANT]
> Hvis det drejer sig om fakturalinjedetaljer, der er rettelser til andre allerede fakturerede opkrævninger, angives feltet **Korrektion** til **Ja**. For så vidt angår fakturaer med korrigerede fakturalinjedetaljer, angives feltet **Indeholder rettelser** til **Ja**.

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
Dette scenarie understøttes ikke.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
