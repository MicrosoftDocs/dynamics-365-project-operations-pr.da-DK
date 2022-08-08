---
title: Overfør fuldt fakturerede faktureringsmilepæle ved overgang
description: I denne artikel beskrives det, hvordan du overfører faktureringsmilepæle for fast pris, som er faktureret til kunden på åbne projektkontrakter inden startdatoen.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028695"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Overfør fuldt fakturerede faktureringsmilepæle ved overgang

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

## <a name="scenario"></a>Scenarie

Contoso aktiveres med Microsoft Dynamics 365 Project Operations i ressource/ikke-lagerbaserede scenarier. Som en del af overgangsaktiviteterne skal implementeringsteamet overføre åbne projektkontrakter fra det gamle system. Nogle af projektkontrakterne indeholder kontraktlinjer, der bruger fastprisfaktureringsmetoden, og som allerede er delvist faktureret til slutbrugeren. Implementeringsteamet skal overføre disse faktureringsmilepæle som **Bogført kundefaktura**, da de skal medtages i den samlede kontraktværdi i forbindelse med omsætningsgenkendelse. Kundesaldi i Debitor og Hovedbog må dog ikke påvirkes.

## <a name="solution"></a>Løsning

### <a name="prerequisites"></a>Forudsætninger

- Dynamics 365 Finance 10.0.24 eller nyere skal installeres.
- Det miljø, hvor overførselstrinnene skal udføres, skal være i vedligeholdelsestilstand. Der bør ikke udføres andre aktiviteter, mens milepælene overføres.
- Overførselstrinnene skal følges nøjagtigt som beskrevet her, og de kan kun bruges til overgangsaktiviteten. Microsoft understøtter ikke anden brug af denne funktion.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Opret en overgangsversion af integrationskontraktlinjemilepælene til Project Operations med dobbelt skrivningstilknytning 

1. Kontrollér, at destinationstilknytningen for objektet **Integrationskontraktlinjemilepæle til Project Operations** er opdateret. 

    1. I Finance skal du gå til **Dataadministration** \> **Dataposteringer** og vælge objektet **Integrationskontraktlinjemilepæle til Project Operations**. 
    2. Vælg **Rediger destinationstilknytninger**. 
    3. På siden **Midlertidig tilknytning til destination** skal du vælge **Opret tilknytning** og derefter bekræfte, at du vil oprette tilknytningen.

2. Stop og opdater **Integrationskontraktlinjemilepæle til Project Operations** (**msdyn\_contractlinescheduleofvalues**) med dobbelte skrivetilknytninger. 

    1. Gå til **Dataadministration** \> **Dobbelt skrivning**, vælg tilknytningen, og åbn dens detaljer. 
    2. Vælg **Stop**, og vent, indtil tilknytningen stoppes af systemet. 
    3. Vælg **Opdater tabeller**.

3. Tilføj en tilknytning for transaktionsstatus.

    1. Vælg **Tilføj tilknytning**.
    2. På den nye linje skal du i kolonnen **Programmer til finans og drift** vælge feltet **TRANSSTATUS \[TRANSSTATUS\]**.
    3. I kolonnen **Microsoft Dataverse** skal du vælge **msdyn\_invostatus \[Faktureringsstatus\]**.
    4. I kolonnen **Tilknytningstype** skal du vælge den højre pil (**\>**).
    5. I den dialogboksen, der vises, skal du i feltet **Synkroniser retning** vælge **Dataverse til Programmer til finans og drift**.
    6. Vælg **Tilføj transformering**.
    7. I feltet **Transformeringstype** skal du vælge **ValueMap**.
    8. Vælg **Tilføj værditilknytning**.
    9. Angiv **4** i vestre felt. Angiv **192350001** i højre felt. 
    10. Vælg **Gem**, og luk derefter dialogboksen.

4. Vælg **Gem som** for at gemme versionen af tilknytningen med dobbelt skrivning. 
5. I ruden **Tilføj tabel** i feltet **Publisher** skal du vælge **Standardpublisher**.
6. Angiv versionen i feltet **Version**.
7. I feltet **Beskrivelse** skal du angive en note om denne overgangsversionen af tilknytningen. 
8. Vælg **Gem**.
9. Start tilknytningen.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Overfør fakturerede milepæle til Dataverse-miljøet

1. I Project Operations Dataverse-miljø skal du oprette milepæle, der har fakturastatussen **Klar til fakturering**. Du skal ikke overflytte milepæle, der ikke er faktureret.

    > [!NOTE]
    > Før du overfører faktureringsmilepælene, skal du kontrollere, at de økonomiske dimensioner, der er relateret til projektkontraktlinjen, er angivet som forventet. Økonomiske dimensioner kan ikke redigeres, når overførslen er fuldført.

2. Når alle milepælene er blevet overført, skal du stoppe følgende tilknytninger med dobbelt skrivning:

    - Milepæle for integration af kontraktlinje i Project Operations (msdyn\_contractlinescheduleofvalues)
    - Integration af faktiske oplysninger i Project Operations (msdyn\_faktiske)
    - Projektfakturaforslag V2 (fakturaer)

    Du kan standse tilknytningerne ved at benytte følgende fremgangsmåde:

    1. I Finance skal du gå til **Dataadministration** \> **Dobbelt skrivning**, vælge en tilknytning og åbne dens detaljer.
    2. Vælg **Stop**, og vent, indtil tilknytningen stoppes af systemet.

3. Opret og bekræft pro-formafakturaerne for faktureringsmilepælene i Project Operations Dataverse-miljø. 

    1. I oversigten over webstedet skal du gå til projektkontrakterne, vælge kontrakterne og derefter vælge **Opret fakturaer**.
    2. Når fakturaerne er oprettet, skal du åbne dem i menuen **Fakturaer** i oversigten over webstedet og derefter vælge **Bekræft**.

    I dette trin oprettes de påkrævede poster i Dataverse-miljøet. Det påvirker dog ikke økonomi og debitorer, da de tidligere angivne tilknytninger med dobbelt skrivning blev stoppet.

4. Når alle pro-formafakturaerne er bekræftet, skal du returnere alle tilknytninger med dobbelt skrivning til den oprindelige tilstand.

    1. Opdater versionen for **Integrationskontraktlinjemilepæle til Project Operations** (**msdyn\_contractlinescheduleofvalues**) med dobbelte skrivetilknytninger tilbage til originalen. 
    2. Vælg den dobbelte tilknytning på tilknytningslisten, vælg **Tabeltilknytningsversion**, og vælg derefter den oprindelige version af tabeltilknytningen.
    3. Vælg **Gem**.
    4. Genstart følgende tilknytninger med dobbelt skrivning:

        - Milepæle for integration af kontraktlinje i Project Operations (msdyn\_contractlinescheduleofvalues)
        - Integration af faktiske oplysninger i Project Operations (msdyn\_faktiske)
        - Projektfakturaforslag V2 (fakturaer)

Milepælene er nu overført, og systemet er parat til de næste trin i overgangsaktiviteten.
