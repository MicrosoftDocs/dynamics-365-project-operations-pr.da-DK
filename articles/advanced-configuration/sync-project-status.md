---
title: Synkroniser projektstatus for at forhindre indtastning i forbindelse med lukkede projekter
description: I denne artikel forklares, hvordan du synkroniserer Projektstatus for at forhindre indtastning i forhold til inaktive eller lukkede projekter.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348004"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Synkroniser projektstatus for at forhindre indtastning i forbindelse med lukkede projekter

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

## <a name="scenario"></a>Scenarie

Contoso gå live med Microsoft Dynamics 365 Project Operations i ressource/ikke-lagerbaserede scenarier. Som led i normale forretningsaktiviteter kan projekter fuldføres eller sættes i venteposition. Du kan deaktivere projektet for at sikre, at der ikke genereres udgifter eller fakturaer.

## <a name="solution"></a>Løsning

### <a name="prerequisites"></a>Forudsætninger

-   Microsoft Dynamics 365 Finance 10.0.29 eller nyere skal installeres.
-   Dual Write Map 1.0.0.3 for Projects V2 (msdyn\_projects) skal installeres eller konfigureres manuelt som beskrevet nedenfor.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Opret en opdateret version af integrationsprojekter af Project Operations V2 med dobbelt skrivningstilknytning

Opdatering af tilknytning af dobbeltskrivning i Project Operations-projekter V2:

1. Gå til **Dataadministration**, og vælg **Dobbeltskrivning**.
2. Vælg feltet **Dobbeltskrivning**.
3. fra T **Tabeltilknytning**-kolonnen skal du finde og vælge **Projekt V2 (msdyn\_projekter)**, og derefter vælge Stop.
4. Vælg tilknytningsnavnet for at åbne tilknytningen, og vælg derefter **[Ingen]**.
5. Vælg **statecode \[Project Status\]** i dialogboksen Vælg kolonne , og vælg derefter OK. Du kan skrive **tilstand** i filterværdien for at indsnævre listen.
6.  Vælg **Tilføj eller rediger transformering** i kolonnen af typen **Tilknytning** for at redigere transformeringen.
7.  I feltet **Transformeringstype** skal du vælge **ValueMap**.
8.  Vælg **Tilføj værditilknytning**, og tilføj derefter følgende **Nøgler** og **Værdier**:

   Key       | Værdi 
   ----------|-------
   InProcess | 0     
   Fuldført | 0     

![Skærmbillede af oplysninger om dobbeltskrivningstilknytning](media/projectstage-dw-mapping.png)

9. Vælg **Gem**.
10. Vælg **Gem som** øverst på siden **Dobbeltskrivning > Projekter V2 (msdyn_projects)**.
11. I ruden **Tilføj tabel** i feltet **Publisher** skal du vælge **CDS Standardpublisher**.
12. Angiv feltet **Version** til 1.0.0.3.
13. Angiv **Beskrivelse**, og vælg **Gem**.
14. Vælg **Kør** øverst på siden **Dobbeltskrivning > Projekter V2 (msdyn_projects)** for at starte kortet, og klik derefter på **Ja**, hvis du bliver bedt om at bekræfte, før du kører. 

### <a name="close-a-newly-completed-project"></a>Lukke et projekt, der netop er fuldført

Dynamics 365 Finance bruger feltet til **projektfasen** til at skelne mellem projekter **i proces** eller **færdige**. **Færdige** projekter kan ikke dække udgifter eller faktureres til kunder.

1. Åbn et projekt, der skal deaktiveres.
2. Vælg **Deaktiver** på båndet.

> [!NOTE]
> Du kan enten deaktivere eller lukke et projekt, da de begge fungerer på samme måde i forbindelse med Økonomi.

3. Åbn listesiden **Alle projektlister** i Økonomi.
4. Kontrollér, at det deaktiverede projekt ikke vises på listen.
5. Skift værdien fra **Aktiv** til **Alle** i filteret til **vis projekter** oven over listen.
6. Du kan nu se det deaktiverede projekt.

Hvis du forsøger at registrere tid eller udgifter i forhold til dette projekt i Økonomi, bør du ikke kunne se det valgte projekt. Hvis du angiver projektnummeret manuelt på en udgiftspost, kan du se en meddelelse som "Afsluttet projektfasen tillader ikke registrering i projektet". Faktureringsfunktioner og andre faktureringsfunktioner skal deaktiveres, da de vil være i forbindelse med et lukket projekt.

