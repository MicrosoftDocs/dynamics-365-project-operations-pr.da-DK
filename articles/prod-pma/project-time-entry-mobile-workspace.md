---
title: Mobilt arbejdsområde for tidsregistrering på projekter
description: Dette emne indeholder oplysninger om det mobile arbejdsområde for tidsregistreringer på projekter. I dette arbejdsområde kan brugere indtaste og spare tid i løbet af et projekt ved at anvende deres mobilenhed.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f087e15780272fd376a14b42ed9e00420f86a61f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009924"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobilt arbejdsområde for tidsregistrering på projekter

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om det mobile arbejdsområde for **Tidsregistrering på projekter**. I dette arbejdsområde kan brugere indtaste og spare tid i løbet af et projekt ved at anvende deres mobilenhed.

Dette mobile arbejdsområde er beregnet til at blive brugt sammen med Dynamics 365 Unified Ops-mobilappen. 

## <a name="overview"></a>Oversigt
Projektressourcer tildeles ofte på stedet eller rejser som led i deres daglige arbejde. Det mobile arbejdsområde for **Tidsregistrering på projekter** gør det muligt for brugerne at angive deres fakturerbare eller ikke-fakturerbare tid i forhold til et projekt på den ønskede mobilenhed. Projektressourcer kan derfor registrere tidspunkter når som helst og hvor som helst. Du kan også få vist tidsregistreringer, der allerede er blevet registreret. 

Derudover kan brugere i det mobile arbejdsområde for **Tidsregistrering på projekter** udføre disse opgaver:

-   På en given dato kan du angive det antal timer, som du har brugt på en bestemt opgave.
-   Søg efter projektnavn eller kunde for at finde det projekt, der skal angives tid for.
-   Angiv kategorien og aktiviteten for den tid, du har brugt.
-   Registrer tiden som fakturerbar eller ikke-fakturerbar på projektet.
-   Du kan eventuelt angive eksterne eller interne kommentarer.

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne er forskellige, afhængigt af den version af Microsoft Dynamics 365, der er installeret i din organisation.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Forudsætninger, hvis du bruger Dynamics 365 Finance
Hvis Finance er blevet udrullet i din organisation, skal systemadministrator publicere det mobile arbejdsområde for **Tidsregistrering på projekter**. Du kan finde en vejledning i [Publicer et mobilt arbejdsområde](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Forudsætninger, hvis du bruger version 1611 sammen med platformsopdatering 3 eller nyere
Hvis version 1611 med platformsopdatering 3 eller nyere er blevet udrullet i din organisation, skal følgende forudsætninger fuldføres af systemadministratoren. 

<table>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementer KB 4018050.</td>
<td>Systemadministrator</td>
<td>KB 4018050 er et hotfix til X++-opdateringen eller metadata, der indeholder det mobile arbejdsområde <strong>Tidsregistrering på projekter</strong>. Hvis du vil implementere KB 4018050, skal systemadministratoren udføre disse trin.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Hent hotfixet til metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installer hotfixet til metadata</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbare pakke</a>, som indeholder modellerne <strong>ApplicationSuite</strong> og <strong>ProjectMobile</strong>, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicer det mobile arbejdsområde for <strong>Tidsregistrering på projekter</strong>.</td>
<td>Systemadministrator</td>
<td>Se <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicer et mobilt arbejdsområde</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Hent og installer mobilappen

Hent og installer Finance and Operations-mobilappen:

-   [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen
1.  Start mobilappen på din mobilenhed.
2.  Angiv din URL-adresse til Dynamics 365.
3.  Første gang, du logger på, bliver du bedt om at angive dit brugernavn og din adgangskode. Angiv dine legitimationsoplysninger.
4.  Når du har logget på, vises de tilgængelige arbejdsområder for virksomheden. Bemærk, at hvis systemadministratoren udgiver et nyt arbejdsområde på et senere tidspunkt, skal du opdatere listen over mobile arbejdsområder.

[![Træk ned for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Angiv tid ved at bruge det mobile arbejdsområde for tidsregistrering på projekter
1.  Vælg arbejdsområdet **Tidsregistrering på projekter** på din mobilenhed.
2.  Vælg **Tidsregistrering**. Kalenderdatoerne for den aktuelle uge vises.
3.  Vælg **Handlinger** &gt; **Ny registrering** for en angivet dato.
4.  Angiv antallet af timer, der skal registreres.
5.  Vælg projektet for tidsregistreringen. På en liste vises de projekter, der er indlæst i appen til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan finde flere oplysninger i [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Hvis projektet ikke findes på listen, skal du vælge **Søg**. Søg efter navn, eller skift for at søge efter projektnavn eller kunde.
7.  Vælg en kategori. På en liste vises de kategorier, der er indlæst i appen til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan finde flere oplysninger i [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Hvis kategorien ikke findes på listen, skal du vælge **Søg**. Søg efter kategori, eller skift til at søge efter kategorinavn.
9.  Vælg en aktivitet. På en liste vises de aktiviteter, der er indlæst i appen til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan finde flere oplysninger i [Mobilplatform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Hvis aktiviteten ikke findes på listen, skal du vælge **Søg**. Søg efter aktivitetsnummer, eller skift til at søge efter formål.

11. Vælg linjeegenskaben.
12. Valgfrit: Angiv eksterne og interne kommentarer.
13. Vælg **Udført**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]