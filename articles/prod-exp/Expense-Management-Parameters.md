---
title: Parametre for udgiftsstyring
description: Følgende parametre styrer funktionsmåden i udgiftsstyring.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ef48f844656ff5197ae1731fb3f9bdf91a1a906b16f35bb2124469743a9e954
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991344"
---
# <a name="expense-management-parameters"></a>Parametre for udgiftsstyring


Parametrene styrer den generelle funktionsmåde i udgiftsstyring.

### <a name="general"></a>Generelt

| **Felt**                                                | **Beskrivelse**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardsats for kørsel**                             | Angiv refusionssatsen for kørselsudgifter. Satsen multipliceres med den kilometerværdi, der angives på udgiften, for at beregne det beløb, der refunderes for rejseudgiften.                       |
|**Personlige udgifter betalt af**                             | Vælg, hvem der er ansvarlig for at betale de kreditkortstransaktioner, der er kategoriseret som personlige.                                                                                                     |
|**Vis hele udgiftsrapporten på drillback**               | Vælg denne indstilling for at se alle udgifter til en udgiftsrapport, når du ser oplysningerne i det oprindelige dokument for et bestemt bilag, der blev oprettet, da udgiftsrapporten blev bogført.              |
|**Rejser skal godkendes på forhånd**                 | Vælg denne indstilling for at kræve, at en rejserekvisition indsendes og godkendes, før en medarbejder kan indsende en udgiftsrapport.                                                                    |
|**Tillad redigering af fordelinger før bogføring**            | Vælg, om fordelingen i en udgiftsrapport kan redigeres før bogføring.                                                                                                                 |
|**Evaluer politikker for udgiftsstyring**                     | Vælg, hvornår udgifter evalueres for at afgøre, hvorvidt en udgiftspolitik er overtrådt. Udgifter kan kontrolleres i forbindelse med overtrædelser, når udgiftsposten angives og gemmes, eller når udgiften sendes til godkendelse. De krævede politikregler for kvitteringer kontrolleres, når udgiftslinjen gemmes.                   |
|**Tillad interne udgiftslinjer**                         | Vælg, om der må indtastes udgifter for andre juridiske enheder i en udgiftsrapport.                                                                                                          |
|**Tillad redigering af valutakurser for udgifter til kreditkort** | Vælg denne indstilling for at give brugeren mulighed for at redigere valutakursen for importerede kreditkortudgifter.                                                                        |
|**Der vises hierarkifelter med flere niveauer**                  | Vælg, hvilke godkenderfelter der skal vises, når tildelingstypen for arbejdsprocessen for udgiftsrapporten er angivet til et hierarki, og valg af hierarki er angivet til at bruge godkendelseshierarkiet på flere niveauer for udgifter. Når godkendelseshierarkiet på flere niveauer bruges til en arbejdsproces, vises de valgte og redigerbare felter i udgiftsrapporten. |
|**Angiv medarbejderens kreditkortnummer (opdatering i juli 2017)**     | Vælg, om der kan angives et tal på 15 eller 16 cifre, og om det skal angives og gemmes i feltet **Kort-id** på siden **Kreditkort** for en medarbejder.                                                                          |

### <a name="financial"></a>Finansiel

| **Felt**                                                            | **Beskrivelse**     |
|----------------------------------------------------------------------|------------------------------------|
|**Dagligt kladdenavn for hovedbog**                                         | Vælg navnet på den hovedbogskladde, som godkendte udgiftsrapporter skal bogføres på.            |
|**Aktivér momsopkrævning fra udgifter**                                  | Vælg denne indstilling, hvis du vil aktivere momsopkrævning for berettigede udgifter. Denne indstilling kan ikke aktiveres, hvis reglerne for amerikansk moms og importmoms er aktiveret.      |
|**Bogfør kontantforskud med det samme**                                     | Vælg denne indstilling for at bogføre et godkendt kontantforskud, når processen for betaling og overførsel er fuldført. Hvis denne indstilling ikke er valgt, oprettes der en ikke-bogført finanskladde under processen for betaling og overførsel. |
|**Korrekt bogføringsdato under bogføring**                             | Vælg denne indstilling, hvis du vil opdatere regnskabsdatoen, når du bogfører udgifter, hvis den aktuelle periode er i venteposition eller lukket. Regnskabsdatoen angives til den næste åbne periode.   |
|**Tillad gruppering af transaktioner baseret på modkonto angivet i betalingsmetode**      | Vælg denne indstilling for at opsummere udgiftstransaktioner for en udgiftsrapport på baggrund af den modkonto, der er angivet i betalingsmetoden for udgifterne.   
|**Inklusiv moms**                                                   | Vælg denne indstilling, hvis du som standard vil inkludere moms i udgiftsbeløbet.             |
|**Frigiv behæftelser for lukning af rejserekvisitioner**            | Vælg denne indstilling for at frigive behæftede midler, når en godkendt rejserekvisition lukkes.                                                                                   |
|**Tillad indsendelse af rejserekvisition ved budgetoverskridelse for budgetregister og projektbudget** | Vælg denne indstilling for at gøre det muligt for medarbejdere at indsende rejserekvisitioner til godkendelse, som overstiger enten det tilladte budget, der er angivet i budgetregistret, eller det tilladte budget for et projekt.            |
|**Tillad indsendelse af udgiftsrapporter ved budgetoverskridelse for budgetregister og projektbudget**    | Vælg denne indstilling for at gøre det muligt for medarbejdere at indsende udgiftsrapporter til godkendelse, som overstiger enten det tilladte budget, der er angivet i budgetregistret, eller det tilladte budget for et projekt.                |
|**Tillad kun godkendelse af udgiftsrapporter ved budgetoverskridelse for budgetregister**                | Vælg denne indstilling for at give godkendere mulighed for at godkende udgiftsrapporter, der overstiger det tilladte budget, der er angivet i budgetregistret.                                                                       |

### <a name="per-diem"></a>Pr. dag

| **Felt**                             | **Beskrivelse**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimum antal timer for diæter**           | Angiv det minimumantal timer, en medarbejder skal arbejde på en dag for at få ret til diæt for rejserelaterede udgifter.  Denne værdi bruges kun som standardværdi for feltet Minimum timer på diætsatsniveauer.                                                                                      |
|**Måltidsprocent**                          | Angiv standardprocenten for diæter til måltider, der bruges på den første og sidste dag i den rejserelaterede udgift, når feltet **Beregn måltidsreduktion efter** er angivet til enten **Måltidstype pr. dag** eller **Antal måltider pr. dag**. Arbejdsdagen for den første og sidste dag kan være kortere end en standardarbejdsdag. Diætbeløbet i disse dage kan derfor variere fra standardbeløb. Hvis procenten er angivet til 0 (nul), vil fradragene for den første og sidste dag være 0,00. |
|**Hotelprocent**                        | Angiv standardprocenten for diæter for hoteller, der bruges på den første og sidste dag i den rejserelaterede udgift. Arbejdsdagen for den første og sidste dag kan være kortere end en standardarbejdsdag. Diætbeløbet i disse dage kan derfor variere fra standardbeløb. Hvis procenten er angivet til 0 (nul), vil fradragene for den første og sidste dag være 0,00.                                              |
|**Anden procentsats**                        | Angiv standardprocenten for diæter for andre udgifter, der bruges på den første og sidste dag i den rejserelaterede udgift. Arbejdsdagen for den første og sidste dag kan være kortere end en standardarbejdsdag. Diætbeløbet i disse dage kan derfor variere fra standardbeløb. Hvis procenten er angivet til 0 (nul), vil fradragene for den første og sidste dag være 0,00.                                                                                                     |
|**Reduktion i procenten for morgenmad** | Angiv det beløb, som diæten reduceres med for morgenmad. Hvis en medarbejder f.eks. får morgenmad, kan det være en god idé at reducere mængden af diæter med 10 procent.                               |
|**Reduktion i procenten for frokost**    | Angiv det beløb, som diæten reduceres med for frokost. Hvis en medarbejder f.eks. får frokost, kan det være en god idé at reducere mængden af diæter med 15 procent.                                       |
|**Reduktion i procenten for aftensmad**   | Angiv det beløb, som diæten reduceres med for aftensmad. Hvis en medarbejder f.eks. får aftensmad, kan det være en god idé at reducere mængden af diæter med 25 procent.                                     |
|**Beregn måltidsreduktion efter**         | Vælg, hvordan systemet skal beregne måltidsreduktionen af diæter, ved at vælge, om reduktionen skal være baseret på måltidstypen pr. tur eller pr. dag, eller om reduktionen skal være baseret på antallet af tilladte måltider pr. dag.|
|**Afrunding af diæter**                  | Vælg den afrundingstype, der bruges til udgifter til diæter. Hvis du vælger normal afrunding, rundes eventuelle diætudgifter, der har et beløb på 0,50, op til 1,00, og eventuelle diætudgifter med et beløb, der er mindre end 0,50, rundes ned til 0,00.                                                                                              |
|**Baser beregning af diæter på**         | Vælg, om et diætbeløb er baseret på en kalenderdag eller en 24-timers periode.       |

### <a name="fax-cover-pages"></a>Faxforsider

| **Felt**                      | **Beskrivelse**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instruktioner**                   | Angiv de instruktioner, medarbejderne skal følge, når de opretter en forside til en fax, der bruges til at sende kvitteringer, som er relateret til en udgiftsrapport. Klik på knappen **Oversættelser** for at angive en sprogspecifik tekst, der skal vises på baggrund af brugersproget. |
|**Bruger-id (oplysninger om stregkode)** | Vælg denne indstilling, hvis du vil gemme en medarbejders entydige id i den stregkode, der bruges på forsiden af faxen.                 |
|**Stregkode**                      | Vælg den stregkode, der bruges på forsiden af faxen. Stregkoderne 39 og 128 understøttes i Udgiftsstyring.               |

### <a name="anti-corruption"></a>Bekæmpelse af korruption

|                 <strong>Felt</strong>                 |                                                                                                                                                                                            <strong>Beskrivelse</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Vis attestation mod korruption</strong>  | Vælg denne indstilling for at se teksten vedrørende bekæmpelse af korruption, når der oprettes en ny udgiftsrapport. Der kan derefter aktiveres bestemte udgiftskategorier, som kræver, at attestationen vedrørende bekæmpelse af korruption er valgt i udgiftsrapporten. Et gavekort, der er relateret til en offentlig officiel udgift, kan f.eks. kræve, at medarbejderen bekræfter, at udgiften overholder firmapolitikken, der er knyttet til offentlige embedsmænd. |
| <strong>Meddelelse om bekæmpelse af korruption, der skal sendes til indsenderen</strong> |                                                                                             Angiv den tekst, der skal vises til medarbejderen, når der oprettes en ny udgiftsrapport. Klik på knappen <strong>Oversættelser</strong> for at angive en sprogspecifik tekst, der skal vises på baggrund af brugersproget.                                                                                             |
| <strong>Meddelelse om bekæmpelse af korruption, der skal sendes til godkenderen</strong>  |                                                                                             Angiv den tekst, der skal vises godkenderen, når der oprettes en ny udgiftsrapport. Klik på knappen <strong>Oversættelser</strong> for at angive en sprogspecifik tekst, der skal vises på baggrund af brugersproget.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]