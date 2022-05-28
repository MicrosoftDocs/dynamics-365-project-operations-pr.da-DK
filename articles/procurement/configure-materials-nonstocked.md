---
title: Konfigurer ikke-lagerførte materialer og afventende leverandørfakturaer
description: Dette emne beskriver, hvordan du kan aktivere ikke-lagerførte materialer og afventende leverandørfakturaer.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592961"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurer ikke-lagerførte materialer og afventende leverandørfakturaer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

## <a name="minimum-version-requirement"></a>Krævet minimumsversion

Brug af ikke-lagerførte materialer og afventende leverandørfakturaer til Dynamics 365 Project Operations ikke-lagerbaserede/ressourcebaserede scenarier kræver følgende versioner:

Dynamics 365 Dataverse-løsninger:

- Project Operations – 4.9.0.221 eller nyere
- Løsning til organisering af program med dobbeltskrivning - 2.2.2.23 eller nyere

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) eller nyere. Kontrollér, at dit Finance-miljø er aktuelt, og at alle kvalitetsopdateringer anvendes, så det overholder minimumversionskravene.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Kør tilknytninger med dobbeltskrivning for ikke-lagerførte materialer og integration af leverandørfakturaer

Dette afsnit indeholder oplysninger om specifikke tilknytninger, der kræves til ikke-lagerførte materialer og leverandørfakturaer. Kontrollér, at de nødvendige tilknytninger, der er angivet i emnet [Klargøring af et nyt miljø](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps), kører i dit miljø.

1. Gå til Lifecycle Services (LCS), navigér til dit LCS-projekt, og gå til siden med **Miljødetaljer**.
2. I afsnittet **Common Data Service miljøoplysninger** skal du vælge **Link til CDS for Apps**. Når du har valgt forbindelsen, bliver du omdirigeret til listen over objekter i tilknytningerne.
3. Kontrollér, at følgende tilknytninger kører. Hvis de ikke kører, skal du starte dem og sørge for at medtage alle relaterede tabeltilknytninger.

    - CDS-udgivne distinkte produkter (produkter)
    - Leverandører v2 (msdyn_vendors)
    - Tabellen for materialeestimater i Project Operations (msdyn_estimatelines)
    - Integrationsobjekt for eksport af projektleverandørfaktura i Project Operations (msdyn_projectvendorinvoices)
    - Integrationsobjekt for eksport af projektleverandørfakturalinje i Project Operations (msdyn_projectvendorinvoicelines)
    - Integration af faktiske oplysninger i Project Operations (msdyn_actuals). Kontrollér, at du kører tilknytningsversion 1.0.0.14 eller nyere. Du kan se den aktive version af tilknytningen i kolonnen **Version** på siden **Dobbelt skrivning**. Du kan aktivere en ny version af tilknytningen ved at vælge **Version af tabeltilknytning** og derefter gemme den valgte version.

Hvis du bruger standarddemonstrationsdata, skal du måske også stoppe og genstarte følgende objekttilknytninger med den første synkronisering:
  - Betalingsdage CDS V2 (msdyn_paymentdays)
  - Betalingsplan (msdyn_paymentschedules)
  - Betalingsbetingelser (msdyn_paymentterms)
  - Leverandørgrupper (msdyn_vendorgroups)
  - Enheder (uom)

> [!NOTE]
> Den første synkronisering for leverandørgrupper og enheder lykkes måske ikke for nogle få poster i det eksisterende demodatasæt. Du kan ignorere fejlene, da de ikke forhindrer dig i at bruge demonstrationsdata i Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurer forudsætninger i Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktivér arbejdsprocessen for at oprette konti baseret på et leverandørobjekt

Løsningen til organisering af dobbeltskrivning leverer [Masterintegration af leverandører](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Som en forudsætning for denne funktion skal der oprettes leverandørdata i objektet **Konti**. Aktivér en arbejdsproces for skabelonen for at oprette leverandører i tabellen **Konti** som beskrevet under [Skift mellem leverandørdesign](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Angiv produkter, der skal oprettes som aktive

Ikke-lagerførte materialer skal konfigureres som **Frigivne produkter** i Finance. Løsningen til organisering af dobbeltskrivning indeholder en standardintegration af [Integration af udgivne produkter i Dataverse-produktkataloget](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Produkter fra Finance synkroniseres som standard med Dataverse i kladdetilstand. Hvis du vil synkronisere produktet med en aktiv tilstand, så det direkte kan bruges i materialebrugsdokumenter eller afventende leverandørfakturaer, skal du gå til **System** > **Administration** > **Systemadministration** > **Systemindstillinger** og i fanen **Salg** for **Opret produkter i aktiv tilstand** angive **Ja**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurer forudsætninger i Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Aktivér funktionsnøglen for afventende leverandørfakturaer

Fuldfør følgende trin for at aktivere funktionaliteten for tilføjelse af projektdetaljer på afventende leverandørfakturalinjer.

1. Gå til arbejdsområdet **Funktionsadministration** i Finance.
2. Find **Aktivér afventende leverandørfakturaer** i funktionslisten i Project Operations for ressourcebaserede/ikke-lagerbaserede scenarier, og vælg **Aktivér**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definér kategorigrupper og projektkategorier for varer

Konfigurér mindst én kategorigruppe for transaktionstypen **Vare**, og mindst én projektkategori ved hjælp af denne gruppe. Du kan finde flere oplysninger under [Konfiguration af produktkategorier](../project-accounting/configure-project-categories.md#category-groups).

Gennemse projektomkostnings- og omsætningsprofilerne, og konfigurer opsætningen af bogføring i hovedbog for varetransaktioner. Du kan finde flere oplysninger under [Konfiguration af regnskab for fakturerbare projekter](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Konfigurer et rekvireret produkt

I Project Operations kan du registrere materialeestimaterne og brugen af katalogprodukter, der er konfigureret i det udgivne produktkatalog og for produkter, der skal rekvireres. Brug af produkter, der skal rekvireres, kræver et enkelt udgivet produkt, der er konfigureret i Finance til dette formål. Fuldfør følgende trin for at konfigurere et produkt, der skal rekvireres. Gentag disse trin i alle juridiske enheder, der bruger Project Operations til scenarier med ressourcer/ikke-lagerførte varer.

1. I Finance skal du gå til **Administration af produktoplysninger** > **Produkter** > **Frigivne produkter** og vælge **Nyt**.
2. I feltet **Produkttype** skal du vælge **Vare** og i feltet **Produktundertype** skal du vælge **Produkt**.
3. Angiv produktnummeret (REKVISITION) og produktnavnet (det produkt, der skal rekvireres).
4. Vælg varens modelgruppe. Kontrollér, at den varemodelgruppe, som du vælger, har feltet **Lagerpolitik for lagerført produkt** angivet til **Falsk**.
5. Vælg værdier i felterne **Varegruppe**, **Lagerdimensionsgruppe** og **Sporingsdimensionsgruppe**. Brug alene **Lager dimensionen** for **Lokation**, og vælg i feltet **Sporingsdimensioner** **Ingen**.
6. Vælg værdier i feltet **Lagerenhed**, **Køb enhed** og **Salgsenhed**, og gem derefter ændringerne.
7. På fanen **Plan** skal du angive standardordreindstillingerne, og på fanen **Lager** skal du angive standardlokationen og lagerstedet.
8. Gå til **Projektstyring og regnskab** > **Opsætning** > **Projektstyrings- og regnskabsparametre**, og åbn **Project Operations på Dynamics 365 Dataverse**. 
9. På fanen **Materialer** skal du i feltet **Rekvireret produkt** vælge det produkt, som du har oprettet.
10. I dit Dataverse-miljø skal du i oversigten over webstedet åbne objektet **Produkter** og finde den produktpost, der skal rekvireres. 
11. Åbn postoplysningerne, og angiv produkttilstanden til **Udgået**. Denne produkttilstand forhindrer, at nogen ved et uheld bruger denne post direkte i materialeestimat og brugsdokumenter.

### <a name="set-up-a-procurement-integration-account"></a>Konfigurer en integrationskonto til indkøb

Integrationskontoen til indkøb bruges som en clearingkonto, når du bogfører en afventende leverandørfaktura med linjer, der tilskrives et projekt.

Når systemet bogfører en afventende leverandørfaktura i systemet, bruges denne konto til projektomkostningerne. Oplysningerne om leverandørfakturaen behandles i Dataverse, og der oprettes et tilsvarende faktisk beløb for projektet. Oplysningerne fra projektets faktiske værdi tilføjes til integrationskladde til Project Operations. Når du bogfører integrationskladden, ryddes beløbet fra indkøbsintegrationskontoen og registreres på projektomkostningerne.

1. For at konfigurere indkøbsintegrationskontoen skal du gå til **Projektstyring og regnskab** > **Opsætning** > **Projektstyrings- og regnskabsparametre**, og åbne **Project Operations på Dynamics 365 Dataverse**. 
2. Vælg fanen **Materialer**, og vælg en værdi i feltet **Indkøbsintegrationskonto**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Konfigurer standardværdier for projektkategorier for en vare

1. I Finance skal du gå til **Projektstyring og regnskab** > **Opsætning** > **Projektstyrings- og regnskabsparametre** og åbne **Project Operations på Dynamics 365 Dataverse**. 
2. På fanen **Standardværdier for projektkategori** skal du i feltet **Vare** vælge en værdi. Denne projektkategori bruges til materialetransaktioner, hvis projektkategorien ikke er angivet på de faktiske værdiposter for projektet.
