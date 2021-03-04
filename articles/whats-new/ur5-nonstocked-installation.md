---
title: Opdater Project Operations i dit Finance-miljø
description: Dette emne indeholder oplysninger om, hvordan du opdaterer Project Operations i dit Dynamics 365 Finance-miljø.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816618"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Opdater Project Operations i dit Finance-miljø

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


Dette emne indeholder oplysninger om, hvordan du opdaterer Dynamics 365 Project Operations i dit Dynamics 365 Finance-miljø. Det kræver tre procedurer at opdatere Project Operations til opdatering 5 (UR5):

- [Importér pakken til dit eksempelprojekt](#import)
- [Anvend opdateringen](#apply)
- [Opdater dit Dataverse-miljø](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importér pakken til dit LCS-projekt

1. Log på [Lifecycle Services (LCS)](https://lcs.dynamics.com/) som projektejer eller miljøadministrator.
2. Vælg dit LCS-projekt fra listen over projekter.
3. På siden **Projekt** skal du i gruppen **Miljø** åbne det miljø, som du ønsker at opdatere.
4. Kontrollér, at miljøet kører. Start miljøet, hvis det ikke er startet.
5. I afsnittet **Ny udgivelse** under **Tilgængelige opdateringer** skal du vælge **Se opdatering** for 10.0.15.

![Knappen Se opdatering](media/view-update.png)

6. På siden **Binære opdateringer** skal du vælge **Gem pakke**.
7. På siden **Gennemse og gem opdateringer** skal du vælge **Gem pakke**.
8. I ruden **Gem pakke i aktivbibliotek**, der åbnes, skal du angive pakkens navn og derefter vælge **Gem pakke**.
9. Når LCS er færdig med at gemme pakken, aktiveres knappen **Udført**. Vælg **Udført**. LCS kontrollerer pakken. Det kan tage et par minutter eller op til en time at kontrollere.


## <a name="apply-the-package-update"></a><a name="apply"></a>Anvend pakkeopdateringen

1. I LCS skal du på siden **Miljødetaljer** vælge **Vedligehold** > **Anvend opdateringer**.
2. Markér den pakke, du har gemt tidligere, på listen, og vælg derefter **Anvend**.
3. Vælg **Ja** for at bekræfte, at du vil installere pakken.

![Dialogboksen Bekræft pakkeudrulning](media/confirm-package-deployment.png)

4. Vælg **Ja** for at bekræfte, at du vil opdatere applikationen.

![Dialogboksen Bekræft opdatering af applikation](media/confirm-application-update.png)

Udrulningen og opdateringen af applikationen starter. 

På siden **Miljødetaljer** opdateres miljøstatus til **Servicering** i øverste højre hjørne. Om ca. to timer er opdateringen gennemført. Oplysningerne om programudgivelsen opdateres til **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, og miljøstatussen opdateres til **Udrullet**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Opdater dit Dataverse-miljø

1. Log på [Power Platform Administration](https://admin.powerplatform.com/).
2. I listen skal du finde og åbne det miljø, som du anvendte til at installere Project Operations.
3. På siden **Miljøer** skal du vælge **Ressource** > **Dynamics 365-applikationer**.
4. Du skal finde **Microsoft Dynamics 365 Project Operations** på listen og derefter i kolonnen **Status** vælge **Tilgængelig opdatering**.
5. Markér afkrydsningsfeltet **Jeg accepterer servicebetingelserne**, og vælg derefter **Opdater**. Den nyeste version af løsningen installeres.

Når installationen er fuldført, er versionen 4.5.0.134 blevet installeret.

## <a name="configure-new-features"></a>Konfigurer nye funktioner

### <a name="enable-dual-write-mapping"></a>Aktiver tilknytning med dobbelt skrivning

Når du har fuldført opdateringen i Finance- og Dataverse-miljøerne, kan du aktivere de påkrævede tilknytninger med dobbelt skrivning. Følg følgende procedurer for at aktivere tilknytninger med dobbelt skrivning.

- [Opdater sikkerhedsindstillinger i Customer Engagement-miljøet](#security)
- [Opdater dataobjekter](#refresh)
- [Opdater og kør tilknytninger med dobbelt skrivning](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Opdater sikkerhedsindstillinger i Dataverse-miljøet

Følgende opdateringer af sikkerhedsrettighederne for objekter er påkrævet som en del af opdateringen til UR5.

1. I dit Dataverse-miljø skal du gå til **Indstillinger**, og i gruppen **System** skal du vælge **Sikkerhed**.

![Dataverse-miljøindstillinger](media/Picture21.png)

2. Vælg **Sikkerhedsroller**.
3. I listen med roller skal du vælge **applikationsbruger med dobbeltskrivning** og vælge fanen **Brugerdefinerede objekter**. 
4. Kontrollér, at rollen har tilladelserne **Læse** og **Tilføj til** for:

      - **Type af valutakurs**
      - **Kontoplan** 
      - **Regnskabskalender** 
      - **Hovedbog**

5. Når sikkerhedsrollen er opdateret, skal du gå til **Indstillinger** > **Sikkerhed** > **Teams**. Kontrollér, at rollen **applikationsbruger med dobbeltskrivning** er blevet anvendt på teamet. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Opdater dataobjekter fra opdateringen

1. I dit Finance-miljø skal du åbne arbejdsområdet **Dataadministration**, og derefter åbne siden **Rammeparametre**.
2. På fanen **Objektindstillinger** skal du vælge **Opdater objektliste**.
3. Vælg **Luk** for at bekræfte opdatering af objektet.

 > [!NOTE]
 > Processen tager ca. 20 minutter at gennemføre. Når opdateringen er fuldført, får du besked.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Opdater tilknytninger med dobbelt skrivning

1. I arbejdsområdet **Dataadministration** skal du vælge **Dobbeltskrivning**.
2. Vælg **Anvend løsninger**, vælg begge løsninger på listen, og vælg derefter **Anvend**.
3. På siden **Dobbeltskrivning** skal du vælge følgende tabeltilknytninger og derefter vælge **Stop**.

    - **Integration af faktiske oplysninger i Project Operations (msdyn_actuals)**
    - **Integration af projektomkostningskategorier i Project Operations (msdyn_expensecategories)**
    - **Eksport af objektet integration af faktiske projektomkostninger i Project Operations (msdyn_expenses)**

4. På siden **Tabeltilknytningsversion** skal du anvende en ny version af tilknytningen på hver af de tre objekter.
5. På siden **Dobbeltskrivning** skal du vælge kør for at genstarte tilknytningerne.
6. Markér listet med tilknytning, vælg tilknytningen **Hovedbog (msdyn_ledgers)** med alle forudsætninger, og markér afkrydsningsfeltet **Oprindelig synkronisering**. 
7. I feltet **Master for oprindelig synkronisering** skal du vælge **Finance and Operations-applikationer** og derefter vælge **Kør**.
 
 ![Synkronisering af tilknytning i hovedbog](media/DW6.png)
 
