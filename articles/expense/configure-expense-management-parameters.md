---
title: Konfigurer parametre for udgiftsstyring
description: Dette emne beskriver de parametre, der styrer den generelle funktionsmåde i Udgiftsstyring.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1cabb0be624f7f6c12761e4fb6d5a095396a5940a37616bb3a304798e1f97808
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007769"
---
# <a name="configure-expense-management-parameters"></a>Konfigurer parametre for udgiftsstyring

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne beskriver de parametre, der styrer den generelle funktionsmåde i Udgiftsstyring.

## <a name="general"></a>Generelt

| Felt                                                    | Beskrivelse |
|----------------------------------------------------------|-------------|
| Standardsats for kørsel                                 | Angiv refusionssatsen for kørselsudgifter. Denne sats multipliceres med den kilometerværdi, der angives for udgiften, til at beregne det beløb, der refunderes for rejseudgiften. |
| Valider udgiftsformål                                 | Aktivér denne indstilling for at begrænse brugerne til et eksisterende sæt værdier, der er konfigureret i feltet **Formål med udgiftsrapport**, når de opretter udgiftsrapporter. |
| Personlige udgifter betalt af                                | Vælg, hvem der er ansvarlig for at betale de kreditkortstransaktioner, der er kategoriseret som personlige. |
| Vis hele udgiftsrapporten på drillback               | Vælg denne indstilling, hvis du vil have vist alle udgifter for en udgiftsrapport, når oplysningerne i det oprindelige dokument vises for et bestemt bilag, der blev oprettet, da udgiftsrapporten blev bogført. |
| Rejser skal godkendes på forhånd                 | Vælg denne indstilling for at kræve, at en rejserekvisition indsendes og godkendes, før en medarbejder kan indsende en udgiftsrapport. |
| Tillad redigering af fordelinger før bogføring            | Vælg, om fordelingen i en udgiftsrapport kan redigeres, før den bogføres. |
| Evaluer politikker for udgiftsstyring                     | Vælg, hvornår udgifter evalueres for at afgøre, om en udgiftspolitik er overtrådt. Udgifter kan evalueres i forbindelse med overtrædelser, når udgiftsposten angives og gemmes, eller når udgiften sendes til godkendelse. De politikregler for kvitteringer, der skal bruges, evalueres, når udgiftslinjen gemmes. |
| Tillad interne udgiftslinjer                         | Vælg, om der kan angives udgifter for andre juridiske enheder i en udgiftsrapport. |
| Tillad redigering af valutakurser for udgifter til kreditkort | Vælg denne indstilling for at give brugeren mulighed for at redigere valutakursen for importerede kreditkortudgifter. |
| Der vises hierarkifelter med flere niveauer                  | Vælg, hvilke godkenderfelter der skal vises, når tildelingstypen for arbejdsprocessen er angivet til et hierarki, og valg af **Hierarki** er angivet til at bruge godkendelseshierarkiet på flere niveauer for udgifter. Når godkendelseshierarkiet på flere niveauer bruges til en arbejdsproces, vises de valgte felter i udgiftsrapporten og kan redigeres. |
| Angiv medarbejderens kreditkortnummer                        | Vælg, om der kan angives et tal på 15 eller 16 tegn, og om det skal angives og gemmes i feltet **Kort-id** på siden **Kreditkort** for en medarbejder. |
| Valider formål med rejserekvisition                      | Aktivér denne indstilling for at begrænse brugerne til et eksisterende sæt værdier, der er konfigureret i feltet **Formål med udgiftsrapport**, når de opretter rejserekvisitioner. |

## <a name="financial"></a>Finansiel

| Felt                                                                                    | Beskrivelse |
|------------------------------------------------------------------------------------------|-------------|
| Dagligt kladdenavn for hovedbog                                                                | Vælg navnet på den hovedbogskladde, som godkendte udgiftsrapporter skal bogføres på. |
| Aktivér momsopkrævning fra udgifter                                                        | Vælg denne indstilling, hvis du vil aktivere momsopkrævning for berettigede udgifter. Denne indstilling kan ikke vælges, hvis reglerne for amerikansk moms og importmoms er aktiveret. |
| Bogfør kontantforskud med det samme                                                           | Vælg denne indstilling for at bogføre et godkendt kontantforskud, når processen til løn og overførsel er fuldført. Hvis denne indstilling ikke er valgt, oprettes der en ikke-bogført finanskladde under processen til løn og overførsel. |
| Korrekt bogføringsdato under bogføring                                                   | Vælg denne indstilling, hvis du vil opdatere regnskabsdatoen, når udgifter bogføres, hvis den aktuelle periode er i venteposition eller lukket. Regnskabsdatoen angives til den næste åbne periode. |
| Tillad gruppering af transaktioner baseret på modkonto angivet i betalingsmetode       | Vælg denne indstilling for at opsummere udgiftstransaktioner for en udgiftsrapport på baggrund af den modkonto, der er angivet i betalingsmetoden for udgifterne. |
| Inklusiv moms                                                                             | Vælg denne indstilling, hvis du som standard vil inkludere moms i udgiftsbeløbet. |
| Frigiv behæftelser for lukning af rejserekvisitioner                                      | Vælg denne indstilling for at frigive behæftede midler, når en godkendt rejserekvisition lukkes. |
| Tillad indsendelse af rejserekvisition ved budgetoverskridelse for budgetregister og projektbudget | Vælg denne indstilling for at gøre det muligt for medarbejdere at indsende rejserekvisitioner til godkendelse, selvom de overstiger enten det tilladte budget, der er angivet i budgetregistret, eller det tilladte budget for et projekt. |
| Tillad indsendelse af udgiftsrapporter ved budgetoverskridelse for budgetregister og projektbudget     | Vælg denne indstilling for at gøre det muligt for medarbejdere at indsende udgiftsrapporter til godkendelse, selvom de overstiger enten det tilladte budget, der er angivet i budgetregistret, eller det tilladte budget for et projekt. |
| Tillad kun godkendelse af udgiftsrapporter ved budgetoverskridelse for budgetregister                 | Vælg denne indstilling for at give godkendere mulighed for at godkende udgiftsrapporter, der overstiger det tilladte budget, der er angivet i budgetregistret. |

## <a name="per-diem"></a>Pr. dag

| Felt                                 | Beskrivelse |
|---------------------------------------|-------------|
| Minimum antal timer for diæter            | Angiv det minimumantal timer, en medarbejder skal arbejde på en dag for at få ret til diæt for rejserelaterede udgifter. Denne værdi bruges kun som standardværdi for feltet **Minimum timer** for diætsatsniveauer. |
| Måltidsprocent                          | Angiv standardprocenten for diæter til måltider, der bruges på den første og sidste dag i den rejserelaterede udgift, når feltet **Beregn måltidsreduktion efter** er angivet til enten **Måltidstype pr. dag** eller **Antal måltider pr. dag**. Arbejdsdagen for den første og sidste dag kan være kortere end en standardarbejdsdag. Diætbeløbet i disse dage kan derfor variere fra standardbeløb. Hvis procentsatsen er angivet til **0** (nul), er fradragene for den første og sidste dag 0,00. |
| Hotelprocent                         | Angiv standardprocenten for diæter for hoteller, der bruges på den første og sidste dag i den rejserelaterede udgift. Arbejdsdagen for den første og sidste dag kan være kortere end en standardarbejdsdag. Diætbeløbet i disse dage kan derfor variere fra standardbeløb. Hvis procentsatsen er angivet til **0** (nul), er fradragene for den første og sidste dag 0,00. |
| Anden procentsats                         | Angiv standardprocenten for diæter for andre udgifter, der bruges på den første og sidste dag i den rejserelaterede udgift. Arbejdsdagen for den første og sidste dag kan være kortere end en standardarbejdsdag. Diætbeløbet i disse dage kan derfor variere fra standardbeløb. Hvis procentsatsen er angivet til **0** (nul), er fradragene for den første og sidste dag 0,00. |
| Reduktion i procenten for morgenmad | Angiv det beløb, som diæten reduceres med for morgenmad. Hvis en medarbejder f.eks. får morgenmad, kan det være en god idé at reducere mængden af diæter med 10 procent. |
| Reduktion i procenten for frokost     | Angiv det beløb, som diæten reduceres med for frokost. Hvis en medarbejder f.eks. får frokost, kan det være en god idé at reducere mængden af diæter med 15 procent. |
| Reduktion i procenten for aftensmad    | Angiv det beløb, som diæten reduceres med for aftensmad. Hvis en medarbejder f.eks. får aftensmad, kan det være en god idé at reducere mængden af diæter med 25 procent. |
| Beregn måltidsreduktion efter           | Angiv, hvordan systemet skal beregne måltidsreduktionen af diæter, ved at vælge, om reduktionen skal være baseret på måltidstypen pr. tur eller pr. dag, eller om den skal være baseret på antallet måltider, der er tilladt pr. dag. |
| Afrunding af diæter                     | Vælg den afrundingstype, der bruges til udgifter til diæter. Hvis du vælger normal afrunding, rundes eventuelle diætudgifter, der har et beløb på 0,50, op til 1,00, og eventuelle diætudgifter med et beløb, der er mindre end 0,50, rundes ned til 0,00. |
| Baser beregning af diæter på          | Vælg, om et diætbeløb er baseret på en kalenderdag eller en 24-timers periode. |

## <a name="fax-cover-pages"></a>Faxforsider

| Felt                          | Beskrivelse |
|--------------------------------|-------------|
| Instruktioner                   | Angiv de instruktioner, medarbejderne skal følge, når de opretter en forside til en fax, der bruges til at sende kvitteringer, som er relateret til en udgiftsrapport. Hvis du vil angive en sprogspecifik tekst, der skal vises på baggrund af brugersproget, skal du vælge **Oversættelser**. |
| Bruger-id (oplysninger om stregkode) | Vælg denne indstilling, hvis du vil gemme en medarbejders entydige id i den stregkode, der bruges på forsiden af faxen. |
| Stregkode                       | Vælg den stregkode, der bruges på forsiden af faxen. Stregkoderne 39 og 128 understøttes i Udgiftsstyring. |

## <a name="anti-corruption"></a>Bekæmpelse af korruption

| Felt                                 | Beskrivelse |
|---------------------------------------|-------------|
| Vis attestation mod korruption   | Vælg denne indstilling for at få vist teksten vedrørende bekæmpelse af korruption, når der oprettes en udgiftsrapport. Der kan derefter aktiveres bestemte udgiftskategorier, som kræver, at attestationen vedrørende bekæmpelse af korruption er valgt i udgiftsrapporten. Et gavekort, der er relateret til en offentlig officiel udgift, kan f.eks. kræve, at medarbejderen bekræfter, at udgiften overholder firmapolitikken, der er knyttet til offentlige embedsmænd. |
| Meddelelse om bekæmpelse af korruption, der skal sendes til indsenderen | Angiv den tekst, der skal vises en medarbejder, som opretter en udgiftsrapport. Hvis du vil angive en sprogspecifik tekst, der skal vises på baggrund af brugersproget, skal du vælge **Oversættelser**. |
| Meddelelse om bekæmpelse af korruption, der skal sendes til godkenderen  | Angiv den tekst, der skal vises godkenderen, når en udgiftsrapport bliver oprettet. Hvis du vil angive en sprogspecifik tekst, der skal vises på baggrund af brugersproget, skal du vælge **Oversættelser**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]