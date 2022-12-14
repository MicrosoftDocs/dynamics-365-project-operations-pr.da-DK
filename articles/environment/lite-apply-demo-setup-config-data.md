---
title: Anvend demonstrationskonfiguration og konfigurationsdata - lille
description: Denne artikel indeholder oplysninger om, hvordan opsætning og konfiguration af demodata i Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811018"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Anvend demonstrationskonfiguration og konfigurationsdata for Project Operations - lille 

_**Lille udrulning - aftale til proformafakturering_



## <a name="prerequisites"></a>Forudsætninger

Før du går i gang med konfigurationen, skal du have et Dataverse-miljø, der er klargjort til Dynamics 365 Project Operations.


## <a name="instructions"></a>Vejledninger

1. Hent [konfigurationsdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Naviger til mappen *ProjOpsSampleSetupData – kun CE-CMT*, og kør den eksekverbare fil *DataMigrationUtility*.
1. På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.

    ![Konfigurationsmigrering.](./media/1ConfigurationMigration.png)

1. På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.
1. Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.
1. Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg derefter **Logon**.

   ![Logon for konfiguration.](./media/2ConfigurationSignin.png)

1. På side 3 skal du på lejeren vælge, hvilken organisation du vil importere demonstrationsdataene til, på listen over organisationer og derefter vælge **Login**.
1. På side 4 skal du vælge zip-filen *SampleSetupAndConfigData* fra den udpakkede mappe *ProjOpsSampleSetupData – kun CE-CMT*.

   ![Zip-fil.](./media/3ZipFile.png)

   ![Vælg en fil.](./media/4SelectAFile.png)

1. Når zip-filen er valgt, skal du vælge **Importér data**.

   ![Importér data.](./media/5ImportData.png)

1. Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden. Afslut CMT-guiden, når den er fuldført. 
1. Kontrollér, om der er data i organisationen i følgende 18 objekter:

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
