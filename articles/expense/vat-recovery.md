---
title: Momsopkrævning i udgiftsstyring
description: I dette emne forklares det, hvordan du kan få refunderet momstransaktioner.
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 64e9f4091fdf40cc702e83a165fe0a5be5043359348210bbe4afcd8a18055133
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999354"
---
# <a name="vat-recovery-in-expense-management"></a>Momsopkrævning i udgiftsstyring

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

For at få refunderet momstransaktioner skal en virksomhed eller organisation identificere, indsamle, kontrollere og indsende nøjagtige oplysninger. Denne proces omfatter flere opgaver, og det kan omfatte flere medarbejdere eller roller, afhængigt af størrelsen på din virksomhed.

Hvis du vil have gendannet moms i modulet **Udgiftsstyring**, skal følgende forudsætninger være opfyldt:

- Der skal være oprettet momskoder for de lande/områder, der er tildelt til udgiftskategorier.
- Der skal oprettes en momsgruppe for de enkelte momskoder.
- Der skal oprettes en kode for varemoms for de enkelte momsgrupper.

Når forudsætningerne er fuldført, skal følgende trin fuldføres for at anmode om refusioner af momstransaktioner.

1. I en udgiftsrapport skal du angive momsoplysninger om kreditkorttransaktioner for at identificere de berettigede momsrefusioner.
2. Kontroller, at alle momsoplysninger er komplette, og bogfør derefter udgiftsrapporten.
3. Behandl udgifter, der er berettiget til international momsopkrævning.
4. Send momsopkrævningsdata til tredjepartsleverandøren for at anmode om internationale opkrævninger.
5. Behandl udgifter for indenlandsk momsopkrævning.

I følgende afsnit er der eksempler på, hvordan medarbejderne i Contoso fuldfører de enkelte trin.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Angiv momsoplysninger om kreditkorttransaktioner for at identificere de berettigede momsrefusioner

Birgitte, en sælger fra Contoso med base i USA, er for nylig kommet tilbage fra en forretningsrejse til Storbritannien. I løbet af turen har Birgitte haft personlige udgifter til måltider, som hun har trukket på sit kreditkort. Birgitte skal nu oprette en udgiftsrapport for at afstemme udgifterne.

Når Birgitte angiver oplysninger i udgiftsrapporten, vælger hun **Storbritannien** i feltet **Land/område** på siden **Rediger udgiftsrapport**. Listen over momsgrupper filtreres derefter, så der kun vises de grupper, der gælder for Storbritannien. Birgitte vælger momsgruppen **Storbritannien 001** og vælger derefter varemomsgruppen **Måltider**. Derefter tilføjer Birgitte en ny transaktion til inddrivelse. Da der kun er én momsgruppe og én varemomsgruppe for indgivelse i Storbritannien, udfyldes disse oplysninger automatisk i Birgittes udgiftsrapport.

Alle udgifter skal have en tilsvarende kvittering ifølge Contoso's politik. Så når Birgitte gemmer udgiftsrapporten, modtager hun en meddelelse om, at hun skal tilknytte en kvittering for hver enkelt transaktion, hun har angivet i udgiftsrapporten. Birgitte bekræfter, at hun har vedhæftet et digitalt billede af hver enkelt transaktioner til udgiftsrapporten og indsender derefter sin rapport til godkendelse. Hun indsender derefter papirkvitteringerne til administrationsteamet, som behandler dem. Dette team sender momsinddrivelsesdata til den tredjepartsleverandør, der indsender inddrivelser af international moms for Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Bekræft momsoplysninger og bogfør en udgiftsrapport

Før Mette, kreditorkoordinatoren for Contoso, kan bogføre en udgiftsrapport, skal hun angive alle momsoplysninger, der mangler heri. Hun åbner siden **Udgiftsrapportdetaljer** og ser Birgittes godkendte udgiftsrapport. Jane åbner derefter udgiftsrapporten for at få vist detaljer om transaktionerne. Hun kan se, at Birgitte ikke har angivet en varemomsgruppe for en af transaktionerne. Da disse oplysninger ikke er angivet, kan Jane ikke bogføre udgiftsrapporten. Hun kigger derfor på siden **Momskonfiguration** i udgiftsstyring og finder den rette varemomsgruppe for landet/området og transaktionstypen. Jane kan nu bogføre udgiftsrapporten i finanskladden.

Når Jane bogfører udgiftsrapporten, oprettes der et arbejdselement for opkrævning af moms. Dette arbejdselement tildeles et medlem af administrationsteamet. Jane modtager en meddelelse, der bekræfter, at bogføringen blev gennemført. Denne meddelelse viser også antallet af momstransaktioner, der er identificeret til opkrævning.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Behandl udgifter, der er berettiget til international momsopkrævning

Bent, som er medlem af Contoso's administrationsbehandlingsteam, er ansvarlig for at verificere, at alle de nødvendige oplysninger om momsinddrivelse er inkluderet i udgiftsrapporter. Han åbner siden **Momsopkrævning af udgift** og vælger den udgiftsrapport, som Birgitte har indsendt. Jens bekræfter derefter, at alle de nødvendige kvitteringer er tilknyttet, og at de korrekte momsgrupper og varemomskoder er angivet.

Når Jens modtager papirkvitteringerne fra Birgitte, afstemmer han dem i forhold til de digitale kvitteringer og ændrer derefter statussen for udgiftsrapporten til **Klar til opkrævning**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Indsend momsinddrivelsesdata til tredjepartsleverandøren

Når Jens er klar til at indsende udgiftsrapportdataene til den tredjepartsleverandør, der skal indsende momsopkrævningen, åbner han siden **Momsopkrævning for udgifter**. Han filtrerer siden, så der kun vises de udgiftsrapporter, der er markeret som **Klar til opkrævning**. Derefter vælger Jens **Indgiv** &gt; **Eksport til Excel**. Momsoplysningerne fra udgiftsrapporterne eksporteres til et Microsoft Excel-regneark. Jens sender dette regneark til tredjepartsleverandøren og inkluderer en meddelelse, der angiver, at papirkvitteringerne er sendt med kurer.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Behandl udgifter for indenlandsk momsopkrævning

Jens skal bekræfte, at udgiftsrapportens transaktioner er berettiget til momsopkrævning, og at de digitale kvitteringer er knyttet til rapporterne. For at begynde at behandle berettigede udgifter til indenlandsk inddrivelse, åbner Jens siden **Momsopkrævning for udgifter** og vælger den udgiftsrapport, der kræver bekræftelse. Han bekræfter, at kvitteringerne er i firmaets navn i stedet for i medarbejderens. (I forhold momsopkrævning, skal kvitteringerne være udstedt i firmaets navn.) Jens bekræfter derefter, at de korrekte momsgrupper og varemomskoder er angivet.

Når Jens modtager papirkvitteringerne, ændrer han statussen for udgiftsrapporten til **Klar til opkrævning**. Han kan derefter indsende opkrævningen til den relevante skattemyndighed. I dette tilfælde er den relevante momsmyndighed i USA "Internal Revenue Service" (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]