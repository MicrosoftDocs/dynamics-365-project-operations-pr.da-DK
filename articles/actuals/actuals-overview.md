---
title: Faktiske
description: Dette emne indeholder oplysninger om, hvordan du arbejder med faktiske værdier i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368604"
---
# <a name="actuals"></a>Faktiske 

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Faktiske værdier repræsenterer den gennemgåede og godkendte økonomiske og planlægningsmæssige status for et projekt. De oprettes som følge af godkendelse af registreringer af tid, udgifter, materialeforbrug samt kladdeposteringer og fakturaer.

## <a name="journal-lines-and-time-submission"></a>Kladdelinjer og tidsregistrering

Du kan finde flere oplysninger om tidsregistrering under [Oversigt over tidsregistrering](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en afsendt tidsregistrering hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.

### <a name="fixed-price"></a>Fast pris

Når en indsendt tidsregistrering er forbundet med et projekt, der er knyttet til en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostninger.

### <a name="default-pricing"></a>Standardprisfastsættelse

Logikken for oprettelse af standardpriser findes på kladdelinjen. Feltværdierne fra tidsregistreringen kopieres til kladdelinjen. Disse værdier inkluderer datoen for transaktionen, den kontraktlinje, som projektet er knyttet til, og valutaresultatet i den rette prisliste.

De felter, der påvirker standardprisfastsættelse som f.eks **Rolle** og **Ressourceenhed**, anvendes til at fastsætte den passende pris på kladdelinjen. Du kan tilføje et brugerdefineret felt på tidsregistreringen. Hvis feltværdien skal overføres til faktiske værdier, skal du oprette feltet i tabellerne **Faktiske** og **Kladdelinje**. Brug brugerdefineret kode til at overføre den valgte feltværdi fra Tidindtastning til Faktiske via kladdelinjen ved hjælp af transaktionsoprindelser. Du kan finde flere oplysninger om transaktionsoprindelser og forbindelser under [Tilknytning af faktiske til oprindelige poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Kladdelinjer og indsendelse af grundlæggende udgifter

Du kan finde flere oplysninger om udgiftsregistrering under [Oversigt over udgifter](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en grundlæggende udgiftspost hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.

### <a name="fixed-price"></a>Fast pris

Når en indsendt grundlæggende udgiftsposten knyttes sammen med et projekt, der er tilknyttet en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostning.

### <a name="default-pricing"></a>Standardprisfastsættelse

Logikken for angivelse af standardpriser for udgifter er baseret på udgiftskategorien. Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste. De felter, der påvirker standardprisfastsættelse som f.eks **Transaktionskategori** og **Enhed**, anvendes til at fastsætte den passende pris på kladdelinjen. Dette fungerer dog kun, når prisfastsættelsesmetoden på prislisten er **Pris pr. enhed**. Hvis prisfastsættelsesmetoden er **Omkostning** eller **Avance før omkostning**, bruges den pris, der blev angivet ved oprettelse af udgiftsposten, til omkostning, og prisen på salgslinjen beregnes på grundlag af prisfastsættelsesmetoden. 

Du kan tilføje et brugerdefineret felt på udgiftsposten. Hvis feltværdien skal overføres til faktiske værdier, skal du oprette feltet i tabellerne **Faktiske** og **Kladdelinje**. Brug brugerdefineret kode til at overføre den valgte feltværdi fra Tidindtastning til Faktiske via kladdelinjen ved hjælp af transaktionsoprindelser. Du kan finde flere oplysninger om transaktionsoprindelser og forbindelser under [Tilknytning af faktiske til oprindelige poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Indsendelse af kladdelinjer og materialeforbrugslog

Du kan finde flere oplysninger om udgiftsregistrering i [Materialeforbrugslog](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en indsendt registrering af en materialeforbrugslog forbindes med et projekt, der er tilknyttet en tids- og materialekontraktlinje, opretter systemet to kladdelinjer, én for omkostning og én for ikke-faktureret salg.

### <a name="fixed-price"></a>Fast pris

Når en indsendt registrering af materialeforbrugslog forbindes med et projekt, der er tilknyttet en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostning.

### <a name="default-pricing"></a>Standardprisfastsættelse

Logikken for registrering af standardpriser for materiale er baseret på kombinationen af produkt og enhed. Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste. De felter, der påvirker standardprisfastsættelse som f.eks **Produkt-id** og **Enhed**, anvendes til at fastsætte den passende pris på kladdelinjen. Dette fungerer dog kun for katalogprodukter. For produkter, der skal rekvireres, anvendes den pris, der blev angivet, da registreringen af materialeforbrugsloggen blev oprettet, som kostpris og salgspris på kladdelinjerne. 

Du kan tilføje et brugerdefineret felt på registreringen af **Materialeforbrugslog**. Hvis feltværdien skal overføres til faktiske værdier, skal du oprette feltet i tabellerne **Faktiske** og **Kladdelinje**. Brug brugerdefineret kode til at overføre den valgte feltværdi fra Tidindtastning til Faktiske via kladdelinjen ved hjælp af transaktionsoprindelser. Du kan finde flere oplysninger om transaktionsoprindelser og forbindelser under [Tilknytning af faktiske til oprindelige poster](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Brug posteringskladder til registrering af omkostninger

Du kan anvende posteringskladder til at registrere omkostningerne eller indtægterne i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser. Kladder kan bruges til følgende formål:

- Flyt faktiske transaktionsoplysninger fra et andet system til Microsoft Dynamics 365 Project Operations.
- Registrer omkostninger, der er opstået i et andet system. Disse omkostninger kan inkludere udgifter til indkøb eller underleverandører.

> [!IMPORTANT]
> Applikationen validerer ikke kladdelinjetypen eller den relaterede prisfastsættelse, der er angivet på kladdelinjen. Derfor er det kun en bruger, der er fuldt bekendt med den regnskabsmæssige indvirkning, som faktiske værdier har på projektet, der skal bruge posteringskladder til at oprette faktiske værdier. Som følge af virkningen af denne kladdetype skal du omhyggeligt vælge, hvem der har adgang til at oprette posteringskladder.

## <a name="record-actuals-based-on-project-events"></a>Registrer faktiske oplysninger baseret på projekthændelser

Project Operations registrerer de økonomiske transaktioner, der sker i løbet af et projekt. Disse transaktioner registreres som faktiske oplysninger. I følgende tabel vises de forskellige typer af faktiske oplysninger, der oprettes, afhængigt af, om projektet er tid-og-materiale- eller fastprisprojekt, er i fasen presales eller er et internt projekt.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Ressourcen tilhører samme afdeling som projektets kontraktenhed

<table>
<thead>
<tr>
<th rowspan="3">Hændelse</th>
<th colspan="4">Faktureret eller solgt projekt</th>
<th rowspan="3">Projekt i fasen presales</th>
<th rowspan="3">Internt projekt</th>
</tr>
<tr>
<th colspan="2">Tid og materialer</th>
<th colspan="2">Fast pris</th>
</tr>
<tr>
<th>Faktiske</th>
<th>Transaktionsvaluta</th>
<th>Fast pris</th>
<th>Transaktionsvaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Der oprettes en tidsregistrering.</td>
<td colspan="6">Ingen aktivitet i objektet Faktiske</td>
</tr>
<tr>
<td>Der indsendes en tidsregistrering.</td>
<td colspan="6">Ingen aktivitet i objektet Faktiske</td>
</tr>
<tr>
<td rowspan="2">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</td>
<td>Faktisk omkostning</td>
<td>Valuta for kontraktenhed</td>
<td rowspan="2">Faktisk omkostning</td>
<td rowspan="2">Valuta for kontraktenhed
<td rowspan="2">Faktisk omkostning</td>
<td rowspan="2">Faktisk omkostning</td>
</tr>
<tr>
<td>Faktisk ikke-faktureret salg – Fakturerbart</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="3">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</td>
<td>Faktisk omkostning</td>
<td>Valuta for kontraktenhed</td>
<td rowspan="3">Faktisk omkostning</td>
<td rowspan="3">Valuta for kontraktenhed</td>
<td rowspan="3">Faktisk omkostning</td>
<td rowspan="3">Faktisk omkostning</td>
</tr>
<tr>
<td>Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="2">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</td>
<td>Tilbageførsel af ikke-faktureret salg</td>
<td>Projektkontraktvaluta</td>
<td rowspan="2">Faktureret salg for milepæl</td>
<td rowspan="2">Projektkontraktvaluta</td>
<td rowspan="2">Ikke tilgængelig</td>
<td rowspan="2">Ikke tilgængelig</td>
</tr>
<tr>
<td>Faktureret salg</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="3">En faktura bekræftes, og der sker et fald i fakturerbare timer.</td>
<td>Tilbageførsel af ikke-faktureret salg</td>
<td>Projektkontraktvaluta</td>
<td rowspan="3">Ikke tilgængelig</td>
<td rowspan="3">Ikke tilgængelig</td>
<td rowspan="3">Ikke tilgængelig</td>
<td rowspan="3">Ikke tilgængelig</td>
</tr>
<tr>
<td>Fakturerbart salg – Fakturerbart for det nye antal</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Fakturerbart salg – Ikke-fakturerbart for differencen</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="2">En faktura er blevet rettet for at øge fakturerbart antal.</td>
<td>Faktureret salg – Tilbageførsel</td>
<td>Projektkontraktvaluta</td>
<td rowspan="5">
<ul>
<li>Tilbageførsel af faktureret salg for milepæl</li>
<li>Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></li>
</ul>
</td>
<td rowspan="5">Projektkontraktvaluta</td>
<td rowspan="5">Ikke tilgængelig</td>
<td rowspan="5">Ikke tilgængelig</td>
</tr>
<tr>
<td>Faktureret salg</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="3">En faktura er blevet rettet for at reducere fakturerbart antal.</td>
<td>Faktureret salg – Tilbageførsel</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Fakturerbart salg for det nye antal</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Ikke-fakturerbart salg – Fakturerbart for differencen</td>
<td>Projektkontraktvaluta</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Ressourcen tilhører en afdeling, som er forskellig fra projektets kontraktenhed

<table>
<thead>
<tr>
<th rowspan="3">Hændelse</th>
<th colspan="4">Faktureret eller solgt projekt</th>
<th rowspan="3">Projekt i fasen presales</th>
<th rowspan="3">Internt projekt</th>
</tr>
<tr>
<th colspan="2">Tid og materialer</th>
<th colspan="2">Fast pris</th>
</tr>
<tr>
<th>Faktiske</th>
<th>Transaktionsvaluta</th>
<th>Fast pris</th>
<th>Transaktionsvaluta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Der oprettes en tidsregistrering.</td>
<td colspan="6">Ingen aktivitet i objektet Faktiske</td>
</tr>
<tr>
<td>Der indsendes en tidsregistrering.</td>
<td colspan="6">Ingen aktivitet i objektet Faktiske</td>
</tr>
<tr>
<td rowspan="4">Tiden godkendes, og der sker ingen ændringer af eller stigninger i fakturerbare timer under godkendelsen.</td>
<td>Faktisk omkostning</td>
<td>Valuta for kontraktenhed</td>
<td rowspan="4">Faktisk omkostning</td>
<td rowspan="4">Valuta for kontraktenhed</td>
<td rowspan="4">Faktisk omkostning</td>
<td rowspan="4">Faktisk omkostning</td>
</tr>
<tr>
<td>Faktisk ikke-faktureret salg – Fakturerbart</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Ressourceenhedsomkostning</td>
<td>Ressourceenhedsvaluta</td>
</tr>
<tr>
<td>Internt salg</td>
<td>Valuta for kontraktenhed</td>
</tr>
<tr>
<td rowspan="5">Tiden godkendes, og der sker et fald i fakturerbare timer under godkendelsen.</td>
<td>Faktisk omkostning</td>
<td>Valuta for kontraktenhed</td>
<td rowspan="5">Faktisk omkostning</td>
<td rowspan="5">Valuta for kontraktenhed</td>
<td rowspan="5">Faktisk omkostning</td>
<td rowspan="5">Faktisk omkostning</td>
</tr>
<tr>
<td>Ressourceenhedsomkostning</td>
<td>Ressourceenhedsvaluta</td>
</tr>
<tr>
<td>Internt salg</td>
<td>Valuta for kontraktenhed</td>
</tr>
<tr>
<td>Faktisk ikke fakturerbart salg – Fakturerbart for det nye antal</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Faktisk ikke fakturerbart salg – Ikke-fakturerbart for differencen</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="2">En faktura bekræftes, og der sker ingen ændring af eller stigning i fakturerbare timer.</td>
<td>Tilbageførsel af ikke-faktureret salg</td>
<td>Projektkontraktvaluta</td>
<td rowspan="2">Faktureret salg for milepæl</td>
<td rowspan="2">Projektkontraktvaluta</td>
<td rowspan="2">Ikke tilgængelig</td>
<td rowspan="2">Ikke tilgængelig</td>
</tr>
<tr>
<td>Faktureret salg</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="3">En faktura bekræftes, og der sker et fald i fakturerbare timer.</td>
<td>Tilbageførsel af ikke-faktureret salg</td>
<td>Projektkontraktvaluta</td>
<td rowspan="3">Ikke tilgængelig</td>
<td rowspan="3">Ikke tilgængelig</td>
<td rowspan="3">Ikke tilgængelig</td>
<td rowspan="3">Ikke tilgængelig</td>
</tr>
<tr>
<td>Fakturerbart salg – Fakturerbart for det nye antal</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Fakturerbart salg – Ikke-fakturerbart for differencen</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="2">En faktura er blevet rettet for at øge fakturerbart antal.</td>
<td>Faktureret salg – Tilbageførsel</td>
<td>Projektkontraktvaluta</td>
<td rowspan="5">
<ul>
<li>Tilbageførsel af faktureret salg for milepæl</li>
<li>Ændring af milepælsstatus fra <strong>Faktureret</strong> til <strong>Klar til fakturering</strong></li>
</ul>
</td>
<td rowspan="5">Projektkontraktvaluta</td>
<td rowspan="5">Ikke tilgængelig</td>
<td rowspan="5">Ikke tilgængelig</td>
</tr>
<tr>
<td>Faktureret salg</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td rowspan="3">En faktura er blevet rettet for at reducere fakturerbart antal.</td>
<td>Faktureret salg – Tilbageførsel</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Fakturerbart salg for det nye antal</td>
<td>Projektkontraktvaluta</td>
</tr>
<tr>
<td>Ikke-fakturerbart salg – Fakturerbart for differencen</td>
<td>Projektkontraktvaluta</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
