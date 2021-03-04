---
title: Mobilt arbejdsområde til udgiftsstyring
description: Dette emne indeholder oplysninger om det mobile arbejdsområde for udgiftsstyring. I dette arbejdsområde kan brugerne oprette og overføre en kvittering, så de kan knytte den til en udgiftsrapport senere. Brugerne kan også hurtigt oprette en udgiftslinje ved hjælp af en tilknyttet kvittering og oprette og administrere deres udgiftsrapporter.
author: suvaidya
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b6d577861a6ebfae55b64a8a06143256e0f1ff40
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960465"
---
# <a name="expense-management-mobile-workspace"></a>Mobilt arbejdsområde til udgiftsstyring

Dette emne indeholder oplysninger om det mobile arbejdsområde for **Udgiftsstyring**. I dette arbejdsområde kan brugerne oprette og overføre en kvittering, så de kan knytte den til en udgiftsrapport senere. Brugerne kan også hurtigt oprette en udgiftslinje ved hjælp af en tilknyttet kvittering og oprette og administrere deres udgiftsrapporter. Derudover kan godkendere bruge det mobile arbejdsområde for **Udgiftsstyring** til at få vist udgiftsrapporter, der er tildelt til dem, og enten godkende eller afvise disse udgiftsrapporter.


Dette mobile arbejdsområde er beregnet til at blive brugt sammen med Dynamics 365 Unified Ops-mobilappen.


## <a name="overview"></a>Oversigt

Mange organisationer kræver, at der er knyttet en kopi af en kvittering til en rejserelateret eller forretningsrelateret udgiftsrapport, som medarbejderen indsender med henblik på refusion. Det mobile arbejdsområde for **Udgiftsstyring** gør det muligt for brugere hurtigt at oprette nye udgiftslinjer på den ønskede mobilenhed ved hjælp af et vedhæftet billede af en kvittering. Brugerne kan også tage et billede af en kvittering og derefter knytte det til en udgiftsrapport senere hen. Medarbejderne kan også oprette og administrere deres udgiftsrapporter og derefter indsende dem til godkendelse og refusion ved hjælp af deres mobilenhed.


Det mobile arbejdsområde for **Udgiftsstyring** gør det navnligt muligt for brugere at udføre disse opgaver:

- Tag et billede af en kvittering, og overfør det til Dynamics 365 Finance. Du kan derefter vedhæfte billedet til en udgiftsrapport senere.
- Overføre en fil som en modtaget kvittering. Du kan derefter vedhæfte filen til en udgiftsrapport senere hen.
- Oprette en ny udgiftslinje ved hjælp af en tilknyttet kvittering. Du kan derefter tilføje linjeelementet til en udgiftsrapport senere hen og indsende det til godkendelse og refusion.

Du kan også bruge disse funktioner:

- Oprette en ny udgiftsrapport.
- Vedhæfte kreditkorttransaktioner og andre tidligere oprettede udgifter til en udgiftsrapport.
- Oprette nye udgifter til en udgiftsrapport.
- Vedhæfte en kvittering for en udgift for en udgiftsrapport ved enten at tage et billede af kvitteringen eller ved at overføre en fil som en modtaget kvittering.
- Afhængigt af virksomhedens udgiftspolitik skal du tilføje listen over gæster til en udgift.
- Specificere udgifter afhængigt af virksomhedens udgiftspolitik.
- Indsende en udgiftsrapport til godkendelse og refusion.
- Godkende eller afvise udgiftsrapporter, som du er den tildelte godkender af.

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne varierer på grundlag af den version, der er installeret i din organisation.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Forudsætninger, hvis du bruger Dynamics 365 Finance 
Hvis Finance er blevet udrullet i din organisation, skal systemadministrator publicere det mobile arbejdsområde for **Udgiftsstyring**. Du kan finde en vejledning i [Publicer mobile arbejdsområder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

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
<td>Implementer KB 4019015.</td>
<td>Systemadministrator</td>
<td>KB 4019015 er et hotfix til X++-opdateringen eller metadata, der indeholder det mobile arbejdsområde <strong>Udgiftsstyring</strong>. Hvis du vil implementere KB 4019015, skal systemadministratoren udføre disse trin.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Hent hotfixet til metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Installer hotfixet til metadata</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbare pakke</a>, som indeholder modellerne <strong>ApplicationSuite</strong> og <strong>ExpenseMobile</strong>, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Udgiv det mobile arbejdsområde for <strong>Udgiftsstyring</strong>.</td>
<td>Systemadministrator</td>
<td>Se <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicer et mobilt arbejdsområde</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Hent og installer Dynamics 365 for Operations-mobilappen
Hent og installer mobil-appen Dynamics 365 Unified Ops:

- [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen
1. Start mobilappen på din mobilenhed.
2. Angiv din URL-adresse til Dynamics 365.
4. Første gang, du logger på, bliver du bedt om at angive dit brugernavn og din adgangskode. Angiv dine legitimationsoplysninger.
5. Når du har logget på, vises de tilgængelige arbejdsområder for virksomheden. Bemærk, at hvis systemadministratoren udgiver et nyt arbejdsområde på et senere tidspunkt, skal du opdatere listen over mobile arbejdsområder.


[![Træk ned for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Registrer en kvittering ved hjælp af det mobile arbejdsområde for Udgiftsstyring

1. Åbn arbejdsområdet for **Udgiftsstyring** på din mobilenhed.
2. Vælg **Registrer kvittering**.
3. Vælg **Tag et billede** eller **Vælg et billede**.
4. Følg et af disse trin:

    - Hvis du valgte **Tag et billede**, skal du benytte følgende fremgangsmåde:

        1. Du føres til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du er færdig med at tage et billede, skal du vælge **OK** for at acceptere billedet.
        2. Valgfrit: Angiv et navn til billedet, og angiv eventuelle noter.

    - Hvis du valgte **Vælg et billede**, skal du benytte følgende fremgangsmåde:

        1. Vælg et billede på listen.
        2. Valgfrit: Angiv et navn til billedet, og angiv eventuelle noter.

5. Vælg **Udført**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Angiv hurtigt udgifter ved hjælp af det mobile arbejdsområde for Udgiftsstyring
1. Åbn arbejdsområdet for **Udgiftsstyring** på din mobilenhed.
2. Vælg **Hurtig udgiftsregistrering**.
3. Vælg udgiftskategorien. Du får vist en liste over de udgiftskategorier, der er indlæst i din app til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan som udvikler finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Hvis din kategori ikke findes på listen, skal du vælge **Søg** for at foretage en online søgning. Søg efter udgiftskategori, eller skift til at søge efter udgiftstype.
4. Angiv transaktionsdatoen for udgiften.
5. Valgfrit: Angiv forhandleren for udgiften.
6. Angiv udgiftsbeløbet.
7. Vælg udgiftsvalutaen. Du får vist en liste over de valutakoder, der er indlæst i din app til offlinebrug. Som standard indlæses 400 valutaer, men en udvikler kan ændre dette nummer. Du kan som udvikler finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Hvis din valuta ikke findes på listen, skal du vælge **Søg** for at foretage en online søgning. Søg efter valuta, eller skift til at søge efter navn.
8. Vælg **Tag et billede** eller **Vælg et billede**.
9. Følg et af disse trin:

    - Hvis du valgte **Tag et billede** føres du til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du er færdig med at tage et billede, skal du vælge **OK** for at acceptere billedet.
    - Hvis du har valgt **Vælg et billede**, skal du vælge et billede på listen.

10. Vælg **Udført**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Godkend en udgiftsrapport ved hjælp af det mobile arbejdsområde for Udgiftsstyring (hvis du bruger opdateringen fra juli 2017)
1. Åbn arbejdsområdet for **Udgiftsstyring** på din mobilenhed.
2. **Godkendelse af udgifter** viser antallet af udgiftsrapporter, som du har fået tildelt til godkendelse. Tallet opdateres ca. hvert 30. minut. Vælg **Udgiftsgodkendelser**.

    Du får vist listen med udgiftsrapporter, som du har fået tildelt til godkendelse.
    
3. Vælg en udgiftsrapport for at få vist dens udgiftsdetaljer.
4. Vælg en udgift for at få vist dens detaljer. De oplysninger, der vises for udgiften, omfatter oplysninger om kvittering, gæst og specifikation.
5. Tilbage på siden **Udgiftsrapport** skal du vælge den for at godkende eller afvise udgiftsrapporten.
6. Skriv eventuelle kommentarer til godkendelseshandlingen.
7. Vælg **Udført**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Opret en ny udgiftsrapport og indsende den til godkendelse ved hjælp af det mobile arbejdsområde for Udgiftsstyring (hvis du bruger opdateringen fra juli 2017)
1. Åbn arbejdsområdet for **Udgiftsstyring** på din mobilenhed.
2. Vælg **Udgiftsregistrering**.
3. Vælg **Ny rapport**, eller vælg en eksisterende udgiftsrapport på listen.
4. I forbindelse med nye udgiftsrapporter skal du angive formålet og eventuelle yderligere oplysninger, der er tilgængelige. Oplysningerne kan variere, afhængigt af hvordan udgiftsstyring er konfigureret for din virksomhed.
5. Vælg **Udført**.
6. Hvis du vil tilføje eksisterende udgifter, f.eks. kreditkorttransaktioner, skal du vælge **Vedhæft** til udgiftsrapporten.
7. Vælg en eller flere udgifter på listen.
8. Vælg **Udført**.
9. Hvis du vil tilføje en ny udgift til udgiftsrapporten, skal du vælge **Ny udgift**.
10. Vælg udgiftskategorien. Du får vist en liste over de udgiftskategorier, der er indlæst i din app til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan som udvikler finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Hvis din kategori ikke findes på listen, skal du vælge **Søg** for at foretage en online søgning. Søg efter udgiftskategori, eller skift til at søge efter udgiftstype.
11. Valgfrit: Angiv forhandleren for udgiften.
12. Angiv transaktionsdatoen for udgiften.
13. Angiv udgiftsbeløbet.
14. Vælg udgiftsvalutaen. Du får vist en liste over de valutakoder, der er indlæst i din app til offlinebrug. Som standard indlæses 400 valutaer, men en udvikler kan ændre dette nummer. Du kan som udvikler finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Hvis din valuta ikke findes på listen, skal du vælge **Søg** for at foretage en online søgning. Søg efter valuta, eller skift til at søge efter navn.
15. Vælg **Udført**.
16. Hvis du vil tilføje flere detaljer til udgiften, skal du vælge **Tilføj flere detaljer**. Hvilke felter der er tilgængelige, afhænger af konfigurationen af udgiftsstyring for din virksomhed.
17. Hvis virksomhedens politik er at kræve en kvittering for udgiften, skal du vælge **Kvitteringer** og derefter følge disse trin:

    1. Vælg **Registrer kvittering** eller **Vedhæft kvittering**.
    2. Følg et af disse trin:

        - Hvis du valgte **Registrer kvittering**, skal du benytte følgende fremgangsmåde:

            1. Vælg **Tag et billede** eller **Vælg et billede**.
            2. Følg et af disse trin:

                - Hvis du valgte **Tag et billede**, skal du benytte følgende fremgangsmåde:

                    1. Du føres til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du er færdig med at tage et billede, skal du vælge **OK** for at acceptere billedet.
                    2. Valgfrit: Angiv et navn til billedet, og angiv eventuelle noter.

                - Hvis du valgte **Vælg et billede**, skal du benytte følgende fremgangsmåde:

                    1. Vælg et billede på listen.
                    2. Valgfrit: Angiv et navn til billedet, og angiv eventuelle noter.

            3.  Vælg **Udført**.

        - Hvis du valgte **Vedhæft kvittering**, skal du benytte følgende fremgangsmåde:

            1.  Vælg et eller flere billeder på listen.
            2.  Vælg **Udført**.

    3. Vælg knappen **Tilbage** for at vende tilbage til udgiftsdetaljerne.

18. Hvis virksomhedens politik er at kræve gæster for udgiften, skal du vælge **Gæster** og derefter følge disse trin:

    1. Vælg **Gæst**, **Tidligere gæster** eller **Kollegaer**.
    2. Følg et af disse trin:

        - Hvis du valgte **Gæst**, skal du benytte følgende fremgangsmåde:

            1. Angiv navnet på gæsten.
            2. Valgfrit: Angiv gæstens organisation og/eller land.
            3. Valgfrit: Angiv gæstens titel.
            4. Vælg **Udført**.

        - Hvis du valgte **Tidligere gæster**, skal du benytte følgende fremgangsmåde:

            1. Vælg en eller flere tidligere gæster på listen. Du får vist en liste over tidligere gæster, som du har tilføjet til de forrige udgiftsrapporter, der er indlæst i din app til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan som udvikler finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Hvis din tidligere gæst findes på listen, skal du vælge **Søg** for at foretage en online søgning. Søg efter navn, eller skift for at søge efter organisation, land eller titel.
            2. Vælg **Udført**.

        - Hvis du valgte **Kollegaer**, skal du benytte følgende fremgangsmåde:

            1. Vælg en eller flere kollegaer på listen. Du får vist en liste over de kollegaer, der er indlæst i din app til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan som udvikler finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Hvis din kollega ikke findes på listen, skal du vælge **Søg** for at foretage en online søgning. Søg efter navn, eller skift for at søge efter virksomhed eller titel.
            2. Vælg **Udført**.

    3. Vælg knappen **Tilbage** for at vende tilbage til udgiftsdetaljerne.

19. Hvis virksomhedens politik kræver, at udgiften specificeres, skal du vælge **Specificer** og derefter følge disse trin:

    1. Vælg den første dato, der skal specificeres.
    2. Vælg **Tilføj specifikation**.
    3. Vælg underkategorien for udgiftsspecifikationen. Du får vist en liste over de underkategorier for udgiften, der er indlæst i din app til offlinebrug. Som standard indlæses 50 elementer, men en udvikler kan ændre dette nummer. Du kan som udvikler finde flere oplysninger i [Mobilplatform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Hvis din underkategori ikke findes på listen, skal du vælge **Søg** for at foretage en online søgning. Søg efter underkategorien for udgiftens navn.
    4. Angiv transaktionsbeløbet for specifikationen.
    5. Rediger posteringsdatoen, hvis det er nødvendigt.
    6. Vælg **Udført**.
    7. Gentag de foregående trin, indtil du er færdig med at tilføje alle specifikationer for den valgte dato.
    8. Hvis du vil tilføje flere dage, kan du vælge **Kopier til næste dag** for at kopiere specifikationerne til den næste dag. Du kan også vælge datoen, der skal specificeres, og derefter tilføje specifikationerne, som du gjorde for den første dato.
    9. Når du er færdig med at specificere udgiften, skal du vælge knappen **Tilbage** for at vende tilbage til udgiftsdetaljerne.

20. Vælg knappen **Tilbage** for at vende tilbage til siden **Udgiftsrapport**.
21. Gentag de foregående trin, indtil du er færdig med at tilføje alle udgifter.
22. Vælg **Send**.
23. Skriv eventuelle kommentarer til godkenderen.
24. Vælg **Udført**.
