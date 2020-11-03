---
title: Anvend demonstrationskonfiguration og konfigurationsdata
description: Dette emne indeholder oplysninger om, hvordan du anvender demonstrationskonfiguration og konfigurationsdata i forbindelse med Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074037"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Anvend demonstrationskonfiguration og konfigurationsdata for lille udrulning af Project Operations - aftale til proformafakturering

_**Lille udrulning - aftale til proformafakturering_

1. Hent [Masterdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Naviger til mappen *ProjOpsDemoDataSetupAndMaster - Integreret CMT* , og kør den eksekverbare fil *DataMigrationUtility*.
3. På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.

![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.
5. Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.
6. Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg derefter **Logon**.

![Log på konfiguration](./media/2ConfigurationSignin.png)

7. På side 3 skal du på lejeren vælge, hvilken organisation du vil importere demonstrationsdataene til, på listen over organisationer og derefter vælge **Login**.
8. På side 4 skal du vælge zip-filen *MasterAndSetupData* fra den udpakkede mappe *ProjOpsDemoDataSetupAndMaster - integreret CMT*.

![Zip-fil](./media/3ZipFile.png)

![Vælg en fil](./media/4SelectAFile.png)

9. Når zip-filen er valgt, skal du vælge **Importér data**.

![Importér data](./media/5ImportData.png)

10. Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden. Afslut CMT-guiden, når den er fuldført. 
11. Kontrollér, om der er data i organisationen i følgende 20 objekter:

- Valuta
- Afdeling
- Kontaktperson
- Momsgruppe
- Kundegruppe
- Enhed
- Enhedsgruppe
- Prisliste
- Prisliste for projektparameter
- Fakturahyppighed
- Detalje for fakturahyppighed
- Kategori af reserverbare ressourcer
- Transaktionskategori
- Udgiftskategori
- Rollepris
- Transaktionskategoripris
- Egenskab
- Reserverbar ressource
- Tilknytning for reserverbar ressourcekategori
- Egenskab for reserverbar ressource

![Fuldført import](./media/6CompleteImport.png)
