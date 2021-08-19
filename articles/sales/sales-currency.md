---
title: Valuta
description: Dette emne indeholder oplysninger om, hvordan du kan tilføje og fjerne valutatyper i Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0a5ae29f1a11f62c6edfca64c4751338f42a26f24c4f8230018b0b45a4ee2ddb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999579"
---
# <a name="currency"></a>Valuta

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Valutaer bestemmer prisen på produkter i produktkataloget og omkostningerne ved transaktioner, f.eks. salgsordrer. Hvis dine kunder er spredt over flere lande, tilføjes deres valutaer med henblik på at administrere dine transaktioner. Tilføj de valutaer, der er mest relevante for dine aktuelle og fremtidige virksomhedsbehov.  

> [!NOTE]
> Hvis dit miljø er et Common Data Service-miljø, og du befinder dig i Power Platform Administration samt vælger siden **Valutaer** (**Miljøer** > [vælg miljø] > **Indstillinger** > **Virksomhed** > **Valutaer**), vil siden være tom. Det skyldes, at angivelse af en valuta ikke understøttes i Common Data Service-miljøer.

## <a name="add-a-currency"></a>Tilføj en valutapost  
Før du går i gang med denne procedure, skal du kontrollere, at din sikkerhedsrolle indeholder systemadministratortilladelser. 

1. Vælg et miljø i Power Platform Administration. 
2. Vælg **Indstillinger** > **Virksomhed**.
3. Vælg **Valutaer**.  
4. Vælg **Ny**.  
5. Angiv oplysningerne efter behov.  


   |          Felt          |                                                                                                                                                                                                                                                                                                                                                                            Beskrivelse                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Valutatype**    | - **System** – Vælg denne indstilling, hvis du vil bruge de valutaer, der er tilgængelige i modelbaserede apps i Dynamics 365. Vælg **Opslag** for at søge efter en valuta. Når du vælger en valutakode, føjes **Valutanavn** og **Valutasymbol** automatisk til den valgte valuta.<br />- **Brugerdefineret** – Vælg denne indstilling, hvis du tilføje en valuta, der ikke er tilgængelig i modelbaserede apps i Dynamics 365. I dette tilfælde skal du angive værdierne manuelt for **Valutakode**, **Valutapræcision**, **Valutanavn**, **Valutasymbol** og **Valutaomregning**. |
   |    **Valutakode**    |                                                                                                                                                                                                                                                                                                                                            Forkortelse af valutaen. F.eks. står **USD** for den amerikanske dollar.                                                                                                                                                                                                                                                                                                                                            |
   | **Valutapræcision**  |                                                                                                                                                                                  Angiv det antal decimaler, der skal bruges til valutaen.  Du kan angive en værdi mellem 0 og 4. **Bemærk:** Hvis du har angivet en præcisionsværdi i dialogboksen **Systemindstillinger**, vises værdien her.                                                                                                                                                                                  |
   |    **Valutanavn**    |                                                                                                                                                                                                                                         Hvis du har valgt en valutakode på listen over tilgængelige valutaer i modelbaserede apps i Dynamics 365, vises valutanavnet for den valgte kode her. Hvis du har valgt **Brugerdefineret** som valutatype, skal du skrive navnet på valutaen.                                                                                                                                                                                                                                          |
   |   **Valutasymbol**   |                                                                                                                                                                                                                                                                      Hvis du har valgt en valutakode på listen over tilgængelige valutaer vises symbolet for den valgte valuta her. Hvis du har valgt **Brugerdefineret** som valutatype, skal du angive symbolet for den nye valuta.                                                                                                                                                                                                                                                                       |
   | **Valutakonvertering** |                                                                                                                                                                                                                                     Skriv værdien for den valgte valuta i form af en amerikansk dollar. Det er det beløb, hvormed den valgte valuta konverteres til grundvalutaen. **Vigtigt:** Kontroller, at du opdaterer denne værdi, så ofte som det kræves for at undgå forkerte beregninger i dine transaktioner.                                                                                                                                                                                                                                      |


6. Vælg **Gem** eller **Gem og luk** på kommandolinjen, når du er færdig.  

   > [!TIP]
   >  Hvis du vil redigere en valuta, skal du vælge den og derefter angive og vælge nye værdier.  

## <a name="delete-a-currency"></a>Slette en valuta  

1. Vælg et miljø i Power Platform Administration. 
2. Vælg **Indstillinger** > **Virksomhed**.
3. Vælg **Valutaer**.  
4. Vælg den valuta, der skal slettes, på den viste liste over valutaer.  
5. Vælg **Slet**.  
6. Bekræft sletningen.  

> [!IMPORTANT]
>  Du kan ikke slette valutaer, der bruges af andre poster. Du kan kun deaktivere dem. Hvis du deaktiverer valutaposter for f.eks. salgsmuligheder og ordrer, fjernes de valutaoplysninger, der er lagret i eksisterende poster, ikke. Du kan dog ikke vælge den deaktiverede valuta til nye transaktioner.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]