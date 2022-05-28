---
title: Opret interne transaktioner
description: Dette emne indeholder oplysninger om, hvordan du opretter interne transaktioner.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 88e5658c9087fdb19adce1c23bc5cad0ad0fa434
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599955"
---
# <a name="create-intercompany-transactions"></a>Opret interne transaktioner

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Interne transaktioner er tids- og udgiftstransaktioner fra en projektkontrakt, der er knyttet til én virksomhed eller organisationsenhed, mens ressourcerne i projektkontrakten er en del af en anden virksomhed eller organisationsenhed.

Når en intern transaktion godkendes, oprettes følgende faktiske transaktioner

| **Transaktionstype** | **Prisliste, der anvendes** | **Transaktionsvaluta** |
| --- | --- | --- |
| Omkostning | Liste over kontraherende enhedskostpriser | Valuta på prislinjen |
| Ikke-fakturerede salg. Disse oprettes kun til faktiske oplysninger, der er knyttet til en kontraktlinje med faktureringstypen, tid og materialer. | Salgsprisliste for kontraktprojekt | Kontraktvaluta |
| Ressourceenhedsomkostning | Liste over ressourcens enhedskostpriser | Valuta på prislinjen |
| Interne enhedssalg | Liste over kontraherende enhedskostpriser | Valuta på prislinjen |

Pris, ressourceenhedens omkostninger og prisfastsættelse for transaktioner vedrørende interne enhedssalg og valuta styres af **Organisationsenheden**. Dette er vigtigt at huske, når du beslutter, hvordan virksomheder og organisationsenheder skal struktureres i implementeringen.

Når du opretter poster for salgsmulighed, tilbud, projektkontrakt og projekt, kontrollerer systemet, at den kontraherende enheds valuta stemmer overens med den kontraherende virksomheds regnskabsvaluta. Når de ikke er ens, kan disse poster ikke oprettes. Valutaen for organisationsenheden defineres i Dynamics 365 Project Operations ved at gå til **Dataverse** > **Indstillinger** > **Organisationsenheder**. En virksomheds regnskabsvaluta defineres i Dynamics 365 Finance ved at gå til **Generel hovedbog** > **Opsætning af hovedbog** > **Hovedbog**. Valutaen synkroniseres med dit Dataverse-miljø ved hjælp af tilknytningen til hovedbogens dobbeltskrivning.

Systemet opretter ressourcens kostpris og de organisationsenhedens faktiske salgsværdier i følgende situationer:

  - Når ressourceenheden afviger fra den ordregivende enhed
  - Når virksomheden med ressourceenheden afviger fra den ordregivende virksomhed

Det er dog kun transaktioner, der har et andet kildefirma end kontraktfirma, der overføres til Dynamics 365 Finance-miljøet med henblik på yderligere regnskab.

Regnskabsføring for projektets faktiske værdier registreres i integrationskladden til Project Operations i Finance. Følgende kladdelinjer oprettes i systemet.

| **Transaktionstype** | **Juridisk enhed** | **Opretter projekttransaktion ved bogføring** | **De økonomiske dimensioner er baseret på standarderne for** | **Standard for faktureringsmomsgruppe og faktureringsvaremomsgruppe** |
| --- | --- | --- | --- | --- |
| Omkostning | Bliver ikke tilføjet til integrationskladden | I\R | I\R | I\R |
| Ikke-faktureret salg | Integrationskladden for den juridiske låneenhed | Ja | Project | **Faktureringsmomsgruppe**: baseret på **kontraktkunden** <br/> **Faktureringsmomsgruppe for vare**: fra den aktuelle projektkategori for den juridiske enhed på kladdelinjen |
| Ressourceenhedsomkostning | Integrationskladden for den juridiske udlånsenhed | Nr. | Interne kunde | **Faktureringsmomsgruppe**: baseret på **intern kunde** <br/> **Faktureringsmomsgruppe for vare**: fra den aktuelle projektkategori for den juridiske enhed på kladdelinjen |
| Interne salg i organisationen | Integrationskladden for den juridiske udlånsenhed | Nr. | Interne kunde | **Faktureringsmomsgruppe**: baseret på **intern kunde** <br/> **Faktureringsmomsgruppe for vare**: fra den aktuelle projektkategori for den juridiske enhed på kladdelinjen |

### <a name="example-intercompany-transactions"></a>Eksempel: interne transaktioner

Freja Jacobsen, som er beskæftiget i GBPM, registrerer 10 timers arbejde på et USPM Adventure Works-projekt, som er godkendt af projektlederen. Udvikleromkostningerne i GBPM er 88 GBP pr. time. GBPM vil fakturere USPM 120 USD pr. udvikler time. USPM vil fakturere kunden Adventure Works, 200 USD for arbejde, der er udført af GBPM-ressourcen. Du kan finde flere oplysninger under [Konfigurer intern fakturering](configure-intercompany-invoicing.md).

1. I Project Operations skal du gå til **Ressourcer** og vælge **Freja Jacobsen** på listen. Under fanen **Planlægning** skal du i feltet **Virksomhed** vælge **GBPM**.
2. Gå til **Salg** > **Kunder**, og vælg **Ny** for at oprette en ny kundepost for Adventure Works.
    1. Angiv virksomheden til **USPM**.
    2. Angiv **Relationstype** til **Kunde**.
    3. Vælg **Kundegruppe 10 – indland**.
    4. Angiv valutaen til **USD**.
    5. Gem posten.
3. Gå til **Salg** > **Projektkontrakter**, og opret en ny projektkontrakt for Adventure Works.
    1. Angiv den ejende virksomhed til **USPM**, og den ordregivende enhed til **Contoso Robotics US**.
    2. Vælg Adventure Works som kunde.
    3. Vælg en produktprisliste, og gem posten.
    4. På fanen **Kontraktlinjer** skal du pårette en ny kontraktlinje. Angiv et navn, og vælg **Tid og materialer** som faktureringsmetode.
    5. Opret et nyt projekt, og knyt det til denne kontraktlinje.
4. Log på som ressourcen **Freja Jacobsen**. Gå til **Projekter** > **Tidsposter**, og opret en tidspost for Adventure Works-projektet.
5. Log på som projektleder. Gå til **Projekter** > **Godkendelser**, og godkend den tidsposttransaktion, der er registreret af Freja Jacobsen.
6. Naviger til Adventure Works-projektet, og vælg **Relaterede** > **Faktiske værdier**. Følgende faktiske transaktioner oprettes.

| **Transaktionstype** | **Pris** | **Transaktionsvaluta** | **Beløb** |
| --- | --- | --- | --- |
| Omkostning | 120 | USD | 1200 |
| Ikke-faktureret salg | 200 | USD | 2000 |
| Ressourceenhedsomkostning | 88 | GBP | 880 |
| Internt salg i organisationen | 120 | USD | 1200 |

7. Log på som en USPM-bogholder. Åbn Finance-forekomsten med Project Operations, og vælg virksomheden **USPM**. 
8. Gå til **Projektstyring og regnskab** > **Periodisk** > **Project Operations på Customer Engagement** > **Importer fra midlertidig lagring**, og vælg at køre den periodiske proces. Denne periodiske proces vil udfylde integrationskladden til Project Operations.
9. Gå til **Projektstyring og regnskab** > **Kladder** > **Integrationskladde til Project Operations**, og gennemse kladdelinjerne. Følgende kladdelinje oprettes i systemet.

    | **Transaktionstype** | **Pris** | **Transaktionsvaluta** | **Beløb** |
    | --- | --- | --- | --- |
    | Ikke-faktureret salg | 200 | USD | 2000 |

    Hvis systemet er konfigureret til at periodisere omsætning for projektet, bogføres følgende:

    - Debet: projekt – salgsværdi for IGVA 200 USD
    - Kredit: projekt – periodiseret omsætning 200 USD

    Dette ikke-fakturerede salg er nu klar til fakturering. Fakturaen for kunden Adventure Works kan bogføres økonomisk, når det er nødvendigt.

10. Log på som **GBPM**-bogholder. Åbn Finance-forekomsten med Project Operations, og åbn virksomheden **GBPM**. 
11. Gå til **Projektstyring og regnskab** > **Periodisk** > **Integration af Project Operations** > **Import fra midlertidig lagringstabel**, og kør den periodiske proces for at udfylde integrationskladden i Project Operations.
12. Gå til **Projektstyring og regnskab** > **Kladder** > **Integrationskladde til Project Operations**, og gennemse linjerne. Følgende kladdelinjer oprettes i systemet.

    | **Transaktionstype** | **Pris** | **Transaktionsvaluta** | **Beløb** |
    | --- | --- | --- | --- |
    | Ressourceenhedsomkostning | 88 | GBP | 880 |
    | Internt salg i organisationen | 120 | USD | 1200 |

    Når disse poster bogføres, medfører det følgende bilagstransaktioner:

    - Debet: projektomkostninger 88 GBP
    - Kredit: lønfordeling 88 GBP

    Hvis systemet er konfigureret til at periodisere intern omsætning bogføres følgende:

    - Debet: projekt – salgsværdi for IGVA 120 USD
    - Kredit: projekt – periodiseret omsætning 120 USD

    Systemet er nu klar til at oprette en intern kundefaktura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
