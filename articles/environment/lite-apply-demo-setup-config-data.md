---
title: Anvend demonstrationskonfiguration og konfigurationsdata - lille
description: Dette emne indeholder oplysninger om, hvordan du anvender demonstrationskonfiguration og konfigurationsdata i forbindelse med Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ecb5da3bccf35f8ed7e2246f68dd4da2b145c6be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586981"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Anvend demonstrationskonfiguration og konfigurationsdata for Project Operations - lille 

_**Lille udrulning - aftale til proformafakturering_



## <a name="prerequisites"></a>Forudsætninger

Før du går i gang med konfigurationen, skal du have et Common Data Service-miljø (CDS), der er klargjort til Dynamics 365 Project Operations.


## <a name="instructions"></a>Vejledninger

1. Hent [Masterdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Naviger til mappen *ProjOpsSampleSetupData – kun CE-CMT*, og kør den eksekverbare fil *DataMigrationUtility*.
3. På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.

    ![Konfigurationsmigrering.](./media/1ConfigurationMigration.png)

4. På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.
5. Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.
6. Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg derefter **Logon**.

   ![Logon for konfiguration.](./media/2ConfigurationSignin.png)

7. På side 3 skal du på lejeren vælge, hvilken organisation du vil importere demonstrationsdataene til, på listen over organisationer og derefter vælge **Login**.
8. På side 4 skal du vælge zip-filen *SampleSetupAndConfigData* fra den udpakkede mappe *ProjOpsSampleSetupData – kun CE-CMT*.

   ![Zip-fil.](./media/3ZipFile.png)

   ![Vælg en fil.](./media/4SelectAFile.png)

9. Når zip-filen er valgt, skal du vælge **Importér data**.

   ![Importér data.](./media/5ImportData.png)

10. Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden. Afslut CMT-guiden, når den er fuldført. 
11. Kontrollér, om der er data i organisationen i følgende 18 objekter:

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

    ![Fuldført import.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
