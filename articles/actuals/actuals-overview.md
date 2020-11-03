---
title: Faktiske
description: Dette emne indeholder oplysninger om, hvordan du arbejder med faktiske oplysninger i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074162"
---
# <a name="actuals"></a>Faktiske 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Faktiske oplysninger er mængden af arbejde, der er udført på et projekt. De oprettes som et resultat af tids- og udgiftsposter samt kladdeposteringer og fakturaer.

## <a name="journal-lines-and-time-submission"></a>Kladdelinjer og tidsregistrering

Du kan finde flere oplysninger om tidsregistrering under [Oversigt over tidsregistrering](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en afsendt tidsregistrering hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.

### <a name="fixed-price"></a>Fast pris

Når en indsendt tidsregistrering er forbundet med et projekt, der er knyttet til en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostninger.

### <a name="default-pricing"></a>Standardprisfastsættelse

Logikken for oprettelse af standardpriser findes på kladdelinjen. Feltværdierne fra tidsregistreringen kopieres til kladdelinjen. Disse værdier inkluderer datoen for transaktionen, den kontraktlinje, som projektet er knyttet til, og valutaresultatet i den rette prisliste.

De felter, der påvirker standardprisfastsættelser som f.eks **Rolle** og **Organisationsenhed** , anvendes til at fastsætte en passende pris på kladdelinjen. Du kan tilføje et brugerdefineret felt på tidsregistreringen. Hvis du ønsker, at feltværdien skal overføres til faktiske værdier, skal du oprette feltet på objektet Faktiske og bruge felttilknytninger til at kopiere feltet fra tidsregistreringen til den faktiske værdi.

## <a name="journal-lines-and-basic-expense-submission"></a>Kladdelinjer og indsendelse af grundlæggende udgifter

Du kan finde flere oplysninger om udgiftsregistrering under [Oversigt over udgifter](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Tid og materialer

Når en grundlæggende udgiftspost hænger sammen med et projekt, der er knyttet til en tids- og materialekontraktlinje, oprettes der to kladdelinjer i systemet, en for kostpris og én for ikke-faktureret salg.

### <a name="fixed-price"></a>Fast pris

Når en grundlæggende udgiftspost er forbundet med et projekt, der er knyttet til en kontraktlinje med fastpris, opretter systemet en kladdelinje for omkostninger.

### <a name="default-pricing"></a>Standardprisfastsættelse

Logikken for angivelse af standardpriser for udgifter er baseret på udgiftskategorien. Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste. Det beløb, som brugeren har indtastet, for selve prisen er dog som standard angivet direkte på de relaterede udgiftskladdelinjer for omkostning og salg.

Den kategoribaserede angivelse af standardpriser pr. enhed for udgiftsposter er ikke tilgængelig.

## <a name="use-entry-journals-to-record-costs"></a>Brug posteringskladder til registrering af omkostninger

Du kan anvende posteringskladder til at registrere omkostningerne eller indtægterne i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser. Kladder kan bruges til følgende formål:

- Registrering af de faktiske omkostninger til materialer og salg i et projekt.
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
