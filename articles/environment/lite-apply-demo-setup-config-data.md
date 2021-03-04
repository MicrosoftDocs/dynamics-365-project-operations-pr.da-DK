---
title: Anvend demonstrationskonfiguration og konfigurationsdata - lille
description: Dette emne indeholder oplysninger om, hvordan du anvender demonstrationskonfiguration og konfigurationsdata i forbindelse med Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089112"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Anvend demonstrationskonfiguration og konfigurationsdata for Project Operations - lille 

_**Lille udrulning - aftale til proformafakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang med konfigurationen, skal du have et Common Data Service-miljø (CDS), der er klargjort til Dynamics 365 Project Operations.


## <a name="instructions"></a>Vejledninger

1. Hent [Masterdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Naviger til mappen *ProjOpsDemoDataSetupAndMaster - Integreret CMT*, og kør den eksekverbare fil *DataMigrationUtility*.
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

    -   Valuta
    -   Konto
    -   Afdeling
    -   Kontakt
    -   Enhed
    -   Enhedsgruppe
    -   Prisliste
    -   Prisliste for projektparameter 
    -   Fakturahyppighed
    -   Kategori af reserverbare ressourcer
    -   Transaktionskategori
    -   Udgiftskategori
    -   Rollepris
    -   Transaktionskategoripris
    -   Egenskab
    -   Reserverbar ressource
    -   Tilknytning for reserverbar ressourcekategori
    -   Egenskab for reserverbar ressource

    ![Fuldført import](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]