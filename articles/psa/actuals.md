---
title: Oversigt over faktiske
description: Dette emne indeholder oplysninger om faktiske projektoplysninger.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7ab2638d82eb5ba928d95ca6a524a1566f21e1ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587579"
---
# <a name="actuals-overview"></a>Oversigt over faktiske

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faktiske oplysninger er mængden af arbejde, der er udført på et projekt. Faktiske projektoplysninger kan spores tilbage til deres kildedokumenter. De pågældende kildedokumenter omfatter tids-, udgifts- og kladdeposteringer samt fakturaer.

![Sådan spores faktiske projektoplysninger til kildedokumenter.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Indsendelse af en tidsregistrering

Når der i PSA indsendes en tidsregistrering for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer. Én linje er til omkostning, og den anden linje er til ikke-faktureret salg. Når der indsendes en tidsregistrering for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning. 

Logikken for angivelse af standardpriser findes på kladdelinjen. Samtlige feltværdier fra en tidsregistrering kopieres til kladdelinjen. Disse felter inkluderer datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaresultatet i den rette prisliste. 

De felter, der påvirker standardpriser som f.eks **Rolle** og **Organisationsenhed**, medfører, at der som standard angives en passende pris på kladdelinjen. Hvis du tilføjer et brugerdefineret felt på tidsregistreringen, og feltværdien skal overføres til faktiske værdier, skal du oprette feltet på objektet Faktiske og bruge felttilknytninger til at kopiere feltet fra tidsregistreringen til den faktiske værdi.

## <a name="submitting-an-expense-entry"></a>Indsendelse af en udgiftspost

Når der i PSA indsendes en udgiftspost for et projekt, der er knyttet til en tids-og-materiale-kontraktlinje, oprettes der to kladdelinjer. Én linje er til omkostning, og den anden linje er til ikke-faktureret salg. Når der indsendes en udgiftsposten for et projekt, der er knyttet til en kontraktlinje med fastpris, oprettes der kun en kladdelinje for omkostning.

Logikken for angivelse af standardpriser for udgifter er baseret på den udgiftskategori, der er valgt på siden **Udgiftspost**. Datoen for transaktionen, den kontraktlinje, projektet er knyttet til, og valutaen bruges alle til at fastlægge den rette prisliste. Men for selve prisen er det beløb, som brugeren har indtastet, som standard angivet direkte på de relaterede udgiftskladdelinjer for omkostning og salg.

I den aktuelle version af PSA er kategoribaseret angivelse af standardpriser pr. enhed for udgiftsposter ikke tilgængelig.

## <a name="using-entry-journals-to-record-costs"></a>Brug af Registreringskladder til registrering af omkostninger

I PSA giver Registreringskladder dig mulighed for at registrere omkostningen eller indtægten i materiale-, gebyr-, time-, udgifts- eller momstransaktionsklasser. En kladde indeholder et hoved, linjer og en **Bekræft**-handling. Her er nogle scenarier, hvor du kan bruge en kladde:

- Du skal registrere de faktiske omkostninger og salget af materialer i et projekt.
- Du skal flytte faktiske transaktionsoplysninger fra et andet system til PSA.
- Du skal registrere omkostninger, der er opstået i et andet system, f.eks. omkostninger til indkøb eller underleverandørarbejde.

> [!IMPORTANT]
> Brug af Registreringskladder til at oprette faktiske oplysninger bør kun ske af en bruger, der fuldt ud bevidst om den regnskabsmæssige indvirkning, de faktiske oplysninger har på projektet. Dette skyldes, at programmet ikke validerer kladdelinjetypen eller de relaterede priser, der angives på kladdelinjen. På grund af virkningen af denne kladdetype skal du udvise behørig omhu med, hvem der har adgang til at oprette Registreringskladder.     


## <a name="recording-actuals-based-on-project-events"></a>Registrering af faktiske oplysninger baseret på projekthændelser

PSA registrerer de økonomiske transaktioner, der sker i løbet af et projekt. Disse transaktioner registreres som **faktiske oplysninger**. I følgende tabel vises de forskellige typer af faktiske oplysninger, der oprettes, afhængigt af, om projektet er tid-og-materiale- eller fastprisprojekt, er i fasen presales eller er et internt projekt.

**Ressourcen tilhører samme afdeling som projektets kontraktenhed**

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

**Ressourcen tilhører en afdeling, som er forskellig fra projektets kontraktenhed**

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
