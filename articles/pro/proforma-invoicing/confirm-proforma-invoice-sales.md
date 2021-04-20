---
title: Bekræft en proformafaktura på projektet
description: Dette emne indeholder oplysninger om bekræftelse af proformafakturaer på projekter i Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867079"
---
# <a name="confirm-a-proforma-project-invoice"></a>Bekræft en proformafaktura på projektet 

_**Gælder for:** Lille udrulning - aftale til proformafakturering_


Når en proforma-faktura er bekræftet, opdateres statussen for projektfakturaens til **Bekræftet**. Når en faktura er blevet bekræftet, bliver den skrivebeskyttet. Fremover kan fakturaen kun rettes, hvis rettelserne skyldes kundeanmodninger eller krediteringer.

I følgende tabel vises de faktiske oplysninger, som systemet opretter. Disse faktiske oplysninger oprettes, når bestemte operationer udføres på kladdeprojektfakturaen, før den bekræftes.

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
Fakturering af et forskud eller et forskudshonorar </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturering af faktisk salgsværdi af typen <strong>Forskudshonorar</strong> oprettes for det pålydende beløb for forskuddet eller forskudshonoraret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ikke-faktureret faktisk salgsværdi med et negativt pålydende beløb for forskudshonoraret eller forskuddet skal anvendes til afstemningen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Efter at have afstemt et forskudshonorar eller et forskud på en faktura fuldt ud.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning. Dette beløb er positivt, da det skal annullere det negative beløb, der blev oprettet, da forskudshonoraret eller forskuddet blev faktureret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fakturering af en faktisk salgsværdi svarende til beløbet på den pågældende faktura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Efter delvist at have afstemt et forskudshonorar eller et forskud på en faktura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførsel af en ikke-faktureret faktisk salgsværdi i form af et forskudshonorar eller et forskud, der blev oprettet med henblik på afstemning. Dette beløb er positivt, da det skal annullere det negative beløb, der blev oprettet, da forskudshonoraret eller forskuddet blev faktureret.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fakturering af en faktisk salgsværdi svarende til beløbet på den pågældende faktura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En negativ ikke-faktureret faktisk salgsværdi lydende på det resterende beløb for forskudshonoraret eller forskuddet skal anvendes til afstemningen af fremtidige fakturaer.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af en tidstransaktion uden ændringer på kladdefakturaen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En faktureret faktisk salgsværdi af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering af en tidstransaktion, der blev redigeret for at reducere antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der ikke er fakturerbar for de resterende timer og beløb efter at have fratrukket de rettede tal på det redigerede fakturalinjeniveau, en tilbageførsel af de faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af en tidstransaktion, der blev redigeret for at øge antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførelse af tiden og beløbet for ikke-faktureret salg på den oprindelige tidsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for de pågældende timer og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af en udgiftstransaktion uden ændringer på kladdefakturaen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En faktureret faktisk salgsværdi for antallet og beløbet på den oprindelige udgiftsgodkendelse </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering af en udgiftstransaktion, der blev redigeret for at reducere antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for det pågældende antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der ikke er fakturerbar for det resterende antal og beløb efter at have fratrukket de rettede tal på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af en udgiftstransaktion, der blev redigeret for at øge antallet.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførelse af antallet og beløbet for ikke-faktureret salg på den oprindelige udgiftsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af en materialetransaktion uden at redigere kladdefakturaen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførsel af et ikke-faktureret salg for mængden og beløbet på den oprindelige materialeforbrugsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En faktureret faktisk salgsværdi for mængden og beløbet på den oprindelige materialeforbrugsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturering af en materialetransaktion, der er redigeret for at reducere mængden.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførsel af et ikke-faktureret salg for mængden og beløbet på den oprindelige tidsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for det pågældende antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der ikke er fakturerbar for det resterende antal og beløb efter at have fratrukket de rettede tal på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af en materialetransaktion, der er redigeret for at øge mængden.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
En tilbageførsel af et ikke-faktureret salg for mængden og beløbet på den oprindelige materialeforbrugsgodkendelse.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En ny ikke-faktureret faktisk salgsværdi, der er fakturerbart for det pågældende antal og beløb på det redigerede fakturalinjeniveau, en tilbageførsel af de ikke-fakturerede faktiske salgsværdier og en tilsvarende fakturering af faktiske salgsværdier.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturering af et gebyr.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Tilbageførelse af gebyrbeløbet for ikke-faktureret salg på den oprindelige kladdelinje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
En faktureret faktisk salgsværdi for antallet og beløbet på den oprindelige gebyrkladdelinje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering af en milepæl.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturering af en faktisk salgsværdi for milepælsbeløbet på den oprindelige milepæl på projektkontraktlinjen.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturering af en produktbaseret kontraktlinje.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturering af en faktisk salgsværdi for produktlinjen med det antal og beløb, der stammer fra den produktbaserede kontraktlinje.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
