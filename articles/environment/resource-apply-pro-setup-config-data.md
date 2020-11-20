---
title: Konfigurer og anvend konfigurationsdata i Common Data Service
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer og anvender demonstrationskonfiguration og konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401121"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigurer og anvend konfigurationsdata i Common Data Service 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

## <a name="prerequisites"></a>Forudsætninger

Før du begynder at konfigurere data i Common Data Service (CDS), skal følgende forudsætninger være opfyldt:

1.  Klargør et CDS-miljø og et Dynamics 365 Finance-miljø til Project Operations.
2.  Oplysninger om juridiske enheder fra Dynamics 365 Finance deles med CDS-miljøet. Dette betyder, at objektet **Virksomehd** i CDS indeholder følgende firmaposter:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Installer konfiguration og konfigurationsdata

1. Hent, fjern blokeringen af, og udpak [Installations- og konfigurationsdatapakken](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Naviger til den zippede mappe og kør den eksekverbare fil *DataMigrationUtility*.
3. På side 1 af konfigurationsguiden til migration af Common Data Service (CMT) skal du vælge **Importer data** og derefter vælge **Fortsæt**.

![Konfigurationsoverførsel](./media/1ConfigurationMigration.png)

4. På side 2 i CMT-guiden skal du vælge **Microsoft 365** som **Udrulningstypen**.
5. Marker afkrydsningsfelterne **Vis en liste over tilgængelige organisationer** og **Vis avancerede**.
6. Vælg lejerens område, angiv dine legitimationsoplysninger, og vælg **Logon**.

![Log på konfiguration](./media/2ConfigurationSignin.png)

7. På side 3 skal du på lejeren vælge den organisation, som du vil importere demonstrationsdataene til, på listen over organisationer og vælge **Login**.
8. På side 4 skal du vælge zip-filen *SampleSetupAndConfigData* fra den udpakkede mappe.

![Valg af zip-fil](./media/3ZipFile.png)

![Vælg en fil](./media/4SelectAFile.png)

9. Når zip-filen er valgt, skal du vælge **Importér data**.

![Importér data](./media/5ImportData.png)

10. Importen kører i cirka to til ti minutter, afhængigt af netværkshastigheden. Afslut CMT-guiden, når importen er fuldført. 
11. Kontrollér, om der er data i organisationen i følgende 19 objekter:

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

## <a name="update-project-operations-configurations"></a>Opdater konfigurationer for Project Operations

1. Naviger til CE-miljø. Du kan finde det ved at åbne [Power Platform Administration](https://admin.powerplatform.microsoft.com/environments), vælge miljøet og derefter vælge **Åbn miljø**. 

![Åbn miljø](./media/7OpenEnvironment.png)

2. Gå til **Projekter** > **Ressourcer**, og vælg derefter **Ny** for at oprette en reserverbar ressource til brugeren.

![Reserverbare ressourcer](./media/8BookableResources.png)

3. På fanen **Generelt** skal du vælge din administratorbruger. Kontroller, at tidszonen stemmer overens med den, du befinder dig i. 

![Ny reserverbar ressource](./media/9NewBookableResource.png)

4. På fanen **Planlægning** skal du i feltet **Virksomhed** vælge virksomheden **USPM** og derefter vælge **Gem**. 

![Planlægningsfane](./media/10SchedulingTab.png)

5. Vælg fanen **Arbejdstid**.  

![Arbejdstimer](./media/11WorkHours.png)

6. Dobbeltklik på en vilkårlig værdi i kalenderen, og vælg **Rediger** > **Alle arrangementer i serien**. 

![Arbejdskalender](./media/12WorkCalendar.png)

7. Skift arbejdstid til en otte (8) timer arbejdsdag, markér weekender som ikke-arbejdsdage, og kontrollér, at tidszonen stemmer overens med din. 
8. Vælg **Gem og luk**.

![Opdater kalender](./media/13UpdateCalendar.png)

9. Gå til **Indstillinger** > **Kalenderskabeloner**, og vælg **Ny**.
 
 ![Kalenderskabeloner](./media/14CalendarTemplates.png)
 
 10. Angiv et navn, vælg den skabelonressource, du har oprettet, og vælg derefter **Gem**. 
 
 ![Gem kalenderskabelon](./media/15SaveCalendarTemplate.png)
 
 11. Gå til **Parametre**, og dobbeltklik på posten. 
 
 ![Projektparametre](./media/16ProjectParameters.png)
 
12. Opdater følgende felter:

 - **Standardvirksomhed**: USPM
 - **Standardafdeling**: Contoso Robotics Global
 - **Fakturafrekvens**: Hver syvende og sidste dag
 - **Arbejdstidsskabelon**: Skift til den skabelon, du har oprettet.

13. Vælg **Gem**. 

![Opdater projektparametre](./media/17UpdatedProjectParameters.png)
