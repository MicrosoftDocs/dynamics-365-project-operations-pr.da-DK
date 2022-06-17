---
title: Fejlfinding i forbindelse med arbejde i opgavegitteret
description: Denne artikel indeholder oplysninger om fejlfinding, der er nødvendige, når du arbejder i gitteret Opgave.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911037"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Fejlfinding i forbindelse med arbejde i opgavegitteret 


_**Gælder for:** Project Operations til ressource/ikke-lagerbaserede scenarier, Lille udrulning – aftale om proformafakturaren, Project for the web_

Det opgavegitter, der bruges i Dynamics 365 Project Operations, er en værtsbaseret iFrame i Microsoft Dataverse. Som følge af denne brug skal der specifikke krav være opfyldte for at sikre, at godkendelse og autorisation fungerer korrekt. I denne artikel beskrives de almindelige problemer, der kan påvirke muligheden for at gengive gitteret eller administrere opgaver i arbejdsopgavehierarkiet (WBS).

Almindelige problemer omfatter:

- Fanen **Opgave** i opgavegitteret er tom.
- Når du åbner projektet, indlæses projektet ikke, og brugergrænsefladen sidder fast på skalaen.
- Administration af rettigheder for **Project for the Web**.
- Ændringer gemmes ikke, når du opretter, opdaterer eller sletter en opgave.

## <a name="issue-the-task-tab-is-empty"></a>Problem: Fanen Opgaver er tom

### <a name="mitigation-1-enable-cookies"></a>Afhjælpning 1: Aktivering af cookies

Project Operations kræver, at tredjepartscookies aktiveres for at gengive arbejdsopgavehierarkiet. Når tredjepartscookies ikke er aktiveret, kan du i stedet for at få vist opgaver se en tom side, når du vælger fanen **Opgaver** på siden **Projekt**.

I Microsoft Edge eller Google Chrome-browsere beskriver følgende procedurer det, hvordan du kan opdatere din browserindstilling for at aktivere tredjepartscookies.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Åbn din Edge-browser.
2. I øverste højre hjørne skal du vælge **ellipsen** (...) og dernæst vælge **Indstillinger**.
3. Under **Cookies og sidetilladelser** skal du vælge **Cookies og websitedata**.
4. Slå **Blokering af tredjepartscookies** fra.
5. Opdater browseren. 

#### <a name="google-chrome"></a>Google Chrome

1. Åbn din Chrome-browser.
2. Vælg de tre vertikale prikker i øverste højre hjørne, og vælg derefter **Indstillinger**.
3. Under **Sikkerhed og privatliv** skal du vælge **Cookies og websitedata**.
4. Vælg **Tillad alle cookies**.
5. Opdater browseren. 

> [!NOTE]
> Hvis du blokerer tredjepartscookies, blokeres alle cookies og websitedata fra andre websteder, også selvom websitet er tilladt på din undtagelsesliste.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Afhjælpning 2: Validér, at PEX-slutpunktet er blevet konfigureret korrekt

Project Operations kræver, at en projektparameter refererer til PEX-slutpunktet. Dette slutpunkt er nødvendigt for at kommunikere med den tjeneste, der bruges til at gengive arbejdsopgavehierarkiet. Hvis parameteren ikke er aktiveret, modtager du fejlmeddelelsen "Projektparameteren er ikke gyldig". Hvis du vil opdatere PEX-slutpunktet, skal du udføre følgende trin.

1. Tilføj feltet **PEX-slutpunkt** til siden **Projektparametre**.
2. Identificer den produkttype, du bruger. Denne værdi bruges, når PEX-slutpunktet er angivet. Ved hentning er produkttypen allerede defineret i PEX-slutpunktet. Behold denne værdi.
3. Opdater feltet med følgende værdi: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. I følgende tabel findes den typeparameter, der skal bruges på grundlag af produkttypen.

      | **Produkttype**                     | **Parametertype** |
      |--------------------------------------|--------------------|
      | Project for the Web på standardafdeling   | type=0             |
      | Project for the Web på CDS-navngivet afdeling | type=1             |
      | Project Operations                   | type=2             |

4. Fjern feltet fra siden **Projektparametre**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Afhjælpning 3: Log på project.microsoft.com.
I din Microsoft Edge-browser skal du åbne en ny fane, gå til project.microsoft.com og logge på ved hjælp af den brugerrolle, du bruger til at få adgang til Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: Projektet indlæses ikke, og brugergrænsefladen sidder fast på skalaen

Med henblik på godkendelse skal pop op-vinduer aktiveres, for at opgavegitteret kan indlæses. Hvis pop op-vinduer ikke er aktiverede, bliver skærmen stående på indlæsningspineren. I følgende grafik vises URL-adressen med en blokeret pop op-etikette i adresselinjen, hvilket resulterer i, at skalaen bliver ved med at forsøge at indlæse siden. 

   ![Fastlåst skala og blokering af pop op-vindue.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Afhjælpning 1: Aktivering af pop op-vinduer

Når dit projekt sidder fast på skalaen, er det muligt, at pop op-vinduer ikke er aktiveret.

#### <a name="microsoft-edge"></a>Microsoft Edge

Du kan aktivere pop op-vinduer i Edge-browseren på to måder.

1. Vælg meddelelsen i øverste højre hjørne af Edge-browseren.
2. Vælg **Tillad altid pop op-vinduer og omdiriger fra** det pågældende Dataverse-miljø.
 
     ![Blokerede pop op-vinduer.](media/enablepopups.png)

Du kan også fuldføre følgende trin:

1. Åbn din Edge-browser.
2. Vælg **ellipsen** (...) i øverste højre hjørne, og vælg derefter **Indstillinger** > **Sidetilladelser** > **Pop op-vinduer og omdirigeringer**.
3. Slå **Pop op-vinduer og omdirigeringer** fra for at blokere pop op-vinduer, eller slå dem til for at tillade pop op-vinduer på enheden.
4. Når du har aktiveret pop op-vinduer, skal du opdatere browseren. 

#### <a name="google-chrome"></a>Google Chrome
1. Åbn din Chrome-browser.
2. Naviger til en side, hvor pop op-vinduer er blokerede.
3. Vælg **Blokering af pop op-vinduer** på adresselinjen.
4. Vælg linket til det pop op-vindue, som du vil have vist.
5. Når du har aktiveret pop op-vinduer, skal du opdatere browseren. 

> [!NOTE]
> Hvis du altid vil se pop op-vinduer for webstedet, skal du vælge **Tillad altid pop op-vinduer og omdirigeringer fra [websted]** og derefter vælge **Udført**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problem 3: Administration af rettigheder for Project for the Web

Project Operations er afhængig af en ekstern planlægningstjeneste. Tjenesten kræver, at en bruger har fået tildelt flere roller, som giver brugeren mulighed for at læse og skrive til objekter, der er relateret til WBS. Disse objekter omfatter projektopgaver, ressourcetildelinger og opgaveafhængigheder. Hvis en bruger ikke kan få gengivet WBS'et, når de navigerer til fanen **Opgaver**, skyldes det sandsynligvis, at **Projekt** i **Project Operations** ikke er blevet aktiveret. En bruger modtager måske enten en sikkerhedsrolle eller en fejl, der er relateret til en nægtelse af adgang.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Afhjælpning 1: Validér sikkerhedsrollerne for programbrugere og slutbrugere

1. Gå til **Indstilling** > **Sikkerhed** > **Brugere** > **Applikationsbruger**.  

   ![Applikationslæser.](media/applicationuser.jpg)
   
2. Dobbeltklik på applikationsbrugerposten for at kontrollere følgende:

     - Brugeren har adgang til projektet. Det kan du gøre ved at kontrollere, at brugeren har sikkerhedsrollen **Projektadministrator**.
     - Microsoft Project-applikationsbrugeren findes og er konfigureret korrekt.
 
3. Hvis denne bruger ikke findes, skal du oprette en ny brugerpost. 
4. Vælg **Nye brugere**, rediger adgangsformularen til **Applikationsbruger**, og tilføj derefter **Applikations-id**.

   ![Oplysninger om applikationsbruger.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problem 4: Ændringer gemmes ikke, når du opretter, opdaterer eller sletter en opgave

Når du foretager en eller flere opdateringer af WBS, mislykkes ændringerne, og de gemmes ikke. Der opstår en fejl i planlægningsgitteret med meddelelsen, der lyder som følger: "Den seneste ændring, du har foretaget, kunne ikke gemmes".

### <a name="mitigation-1-validate-the-license-assignment"></a>Afhjælpning 1: Validér licenstildelingen

1. Kontrollér, at brugeren er blevet tildelt den korrekte licens, og at tjenesten er aktiveret under detaljer om licensens serviceplaner.  
2. Kontrollér, at brugeren kan åbne **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Afhjælpning 2: Valideringskonfiguration af projektapplikationsbrugeren
1. Kontroller, at projektapplikationsbrugeren er blevet oprettet.
2. Anvend følgende sikkerhedsroller på brugeren:
  
  - Dataverse-bruger eller basisbruger
  - Systemet Project Operations
  - Projektsystem
  - Project Operations med dobbelt skrivningssystem. Denne rolle kræves i forbindelse med det ressourcebaserede/ikke-lagerbaserede udrulningsscenarie for Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
