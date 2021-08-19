---
title: Momsinddrivelse
description: I dette emne forklares det, hvordan du kan opkræve refusioner for momstransaktioner.
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986034"
---
# <a name="vat-recovery"></a>Momsinddrivelse 

For at få refunderet momstransaktioner skal en virksomhed eller organisation identificere, indsamle, kontrollere og indsende nøjagtige oplysninger. Denne proces omfatter flere opgaver, og det kan omfatte flere medarbejdere eller roller, afhængigt af størrelsen på din virksomhed.

Hvis du vil have refunderet moms ved hjælp af Udgiftsstyring, skal følgende forudsætninger være opfyldt:

- Der skal være oprettet momskoder for de lande/områder, der er tildelt til udgiftskategorier.
- Der skal oprettes en momsgruppe for de enkelte momskoder.
- Der skal oprettes en kode for varemoms for de enkelte momsgrupper.

Når forudsætningerne er fuldført, skal medarbejderne følge disse trin for at anmode om refusioner af momstransaktioner.

1. I en udgiftsrapport skal du angive momsoplysninger om kreditkorttransaktioner for at identificere de berettigede momsrefusioner.
2. Sørg for, at alle momsoplysninger er komplette, og bogfør derefter udgiftsrapporten.
3. Behandl udgifter, der er berettiget til international momsopkrævning.
4. Send momsopkrævningsdata til tredjepartsleverandøren for at anmode om internationale opkrævninger.
5. Behandl udgifter for indenlandsk momsopkrævning.

I følgende afsnit er der eksempler på, hvordan medarbejderne i Contoso fuldfører de enkelte trin.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>I en udgiftsrapport skal du angive momsoplysninger om kreditkorttransaktioner for at identificere de berettigede momsrefusioner

Birgitte, en sælger fra Contoso med base i USA, er for nylig kommet tilbage fra en forretningsrejse til Storbritannien. I løbet af turen har hun haft personlige udgifter til måltider, som hun har trukket på sit kreditkort. Birgitte skal nu oprette en udgiftsrapport for at afstemme sine udgifterne.

Når Birgitte angiver oplysninger i hendes udgiftsrapport, vælger hun **Storbritannien** i feltet **Land/område** på siden **Rediger udgiftsrapport**. Listen over momsgrupper filtreres derefter, så der kun vises de grupper, der gælder for Storbritannien. Birgitte vælger momsgruppen **Storbritannien 001** og vælger derefter varemomsgruppen **Måltider**. Derefter tilføjer hun en ny transaktion til inddrivelse. Da der kun er én momsgruppe og varemomsgruppe for indgivelse i Storbritannien, udfyldes disse oplysninger automatisk i Birgittes udgiftsrapport.

Alle udgifter skal have en tilsvarende kvittering ifølge Contoso's politik. Så når Birgitte gemmer sin udgiftsrapport, modtager hun en meddelelse om, at hun skal tilknytte en kvittering for hver enkelt transaktion, hun har angivet i udgiftsrapporten. Birgitte bekræfter, at hun har vedhæftet et digitalt billede af hver enkelt transaktioner til udgiftsrapporten og indsender derefter sin rapport til godkendelse. Hun indsender derefter papirkvitteringerne til administrationsteamet, som behandler dem. Dette team sender momsinddrivelsesdata til den tredjepartsleverandør, der indsender inddrivelser af international moms for Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Sørg for, at alle momsoplysninger er komplette, og bogfør derefter udgiftsrapporten

Mette, kreditorkoordinatoren for Contoso, skal angive alle momsoplysninger, der mangler i en udgiftsrapport, før rapporten kan bogføres. Hun åbner siden **Udgiftsrapportdetaljer** og ser Birgittes godkendte udgiftsrapport. Jane åbner derefter udgiftsrapporten for at få vist detaljer om transaktionerne. Hun kan se, at Birgitte ikke har angivet en varemomsgruppe for en af transaktionerne. Da disse oplysninger ikke er angivet, kan Jane ikke bogføre udgiftsrapporten. Jane kigger derfor på siden **Momskonfiguration** i udgiftsstyring og finder den rette varemomsgruppe for landet/området og transaktionstypen. Jane kan nu bogføre udgiftsrapporten i finanskladden.

Når Jane bogfører udgiftsrapporten, oprettes der et arbejdselement for opkrævning af moms. Dette arbejdselement tildeles et medlem af administrationsteamet. Jane modtager en meddelelse, der bekræfter, at bogføringen blev gennemført. Denne meddelelse viser også antallet af momstransaktioner, der er identificeret til opkrævning.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Behandl udgifter, der er berettiget til international momsopkrævning

Bent, som er medlem af Contoso's administrationsbehandlingsteam, er ansvarlig for at bekræfte, at alle de nødvendige oplysninger om momsinddrivelse er inkluderet i udgiftsrapporter. Han åbner siden **Momsopkrævning af udgift** og vælger den udgiftsrapport, som Birgitte har indsendt. Jens bekræfter, at alle de nødvendige kvitteringer er tilknyttet, og at de korrekte momsgrupper og varemomskoder er angivet.

Når Jens modtager papirkvitteringerne fra Birgitte, afstemmer han papirkvitteringerne i forhold til de digitale kvitteringer og ændrer derefter statussen for udgiftsrapporten til **Klar til opkrævning**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Send momsopkrævningsdata til tredjepartsleverandøren for at anmode om internationale opkrævninger

Når Jens er klar til at indsende udgiftsrapportdataene til den tredjepartsleverandør, der skal indsende momsopkrævningen, åbner han siden **Momsopkrævning for udgifter**. Han filtrerer siden, så der kun vises de udgiftsrapporter, der er markeret som **Klar til opkrævning**. Derefter vælger Jens **Indgiv** &gt; **Eksport til Excel**. Momsoplysningerne fra udgiftsrapporterne eksporteres til et Microsoft Excel-regneark. Jens sender dette regneark til tredjepartsleverandøren og inkluderer en meddelelse, der angiver, at papirkvitteringerne er sendt med kurer.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Behandl udgifter for indenlandsk momsopkrævning

Jens skal bekræfte, at udgiftsrapportens transaktioner er berettiget til momsopkrævning, og at de digitale kvitteringer er knyttet til rapporterne. For at begynde at behandle berettigede udgifter til indenlandsk inddrivelse, åbner Jens siden **Momsopkrævning for udgifter** og vælger den udgiftsrapport, der kræver bekræftelse. Han bekræfter, at kvitteringerne er i firmaets navn i stedet for i medarbejderens. I forbindelse med momsopkrævning skal kvitteringerne være udstedt i virksomhedsnavnet. Jens bekræfter derefter, at de korrekte momsgrupper og varemomskoder er anvendt.

Når Jens modtager papirkvitteringerne, ændrer han statussen for udgiftsrapporten til **Klar til opkrævning**. Han kan derefter indsende opkrævningen til den relevante skattemyndighed. I dette tilfælde er den relevante momsmyndighed i USA "Internal Revenue Service" (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]