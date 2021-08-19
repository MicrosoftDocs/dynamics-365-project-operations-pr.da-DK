---
title: Fejlfinding i forbindelse med arbejde i opgavegitteret
description: Dette emne indeholder oplysninger om de nødvendige fejlfindingsoplysninger, når du arbejder i opgavegitteret.
author: ruhercul
ms.date: 08/02/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 07e7bd42db48842edee17fdfdd22fdcd8207644c1751f453ec29c3194aac625e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989094"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Fejlfinding i forbindelse med arbejde i opgavegitteret 

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dette emne beskriver, hvordan du kan løse de problemer, du eventuelt støder på, når du arbejder med omkostningsstyring.

## <a name="enable-cookies"></a>Aktiver cookies

Project Operations kræver aktivering af tredjepartscookies med henblik på at gengive arbejdsopgavehierarkiet. Når tredjepartscookies ikke er aktiveret, kan du i stedet for at få vist opgaver se en tom side, når du vælger fanen **Opgaver** på siden **Projekt**.

![Der vises en tom fane, når tredjepartscookies ikke er aktiveret.](media/blankschedule.png)


### <a name="workaround"></a>Løsning
I Microsoft Edge eller Google Chrome-browsere beskriver følgende procedurer det, hvordan du kan opdatere din browserindstilling for at aktivere tredjepartscookies.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Åbn din Edge-browser.
2. I øverste højre hjørne skal du vælge **ellipsen** (...) og dernæst vælge **Indstillinger**.
3. Under **Cookies og sidetilladelser** skal du vælge **Cookies og websitedata**.
4. Slå **Blokering af tredjepartscookies** fra.

#### <a name="google-chrome"></a>Google Chrome

1. Åbn din Chrome-browser.
2. Vælg de tre vertikale prikker i øverste højre hjørne, og vælg derefter **Indstillinger**.
3. Under **Sikkerhed og privatliv** skal du vælge **Cookies og websitedata**.
4. Vælg **Tillad alle cookies**.

> [!IMPORTANT]
> Hvis du blokerer tredjepartscookies, blokeres alle cookies og websitedata fra andre websteder, også selvom websitet er tilladt på din undtagelsesliste.

## <a name="pex-endpoint"></a>PEX-slutpunkt

Project Operations kræver, at en projektparameter refererer til PEX-slutpunktet. Dette slutpunkt er nødvendigt for at kommunikere med den service, der bruges til at gengive arbejdsopgavehierarkiet. Hvis parameteren ikke er aktiveret, modtager du fejlmeddelelsen "Projektparameteren er ikke gyldig". 

### <a name="workaround"></a>Løsning

1. Tilføj feltet **PEX-slutpunkt** til siden **Projektparametre**.
2. Identificer den produkttype, du bruger. Denne værdi bruges, når PEX-slutpunktet er angivet. Ved hentning er produkttypen allerede defineret i PEX-slutpunktet. Behold denne værdi. 
   
    ![Feltet PEX-slutpunkt på projektparameteren.](media/pex-endpoint.png)

3. Opdater feltet med følgende værdi: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`.

   
   | Produkttype                         | Parametertype |
   |--------------------------------------|----------------|
   | Project for the Web på standardafdeling   | type=0         |
   | Project for the Web på CDS-navngivet afdeling | type=1         |
   | Project Operations                   | type=2         |
   
4. Fjern feltet fra siden **Projektparametre**.

## <a name="privileges-for-project-for-the-web"></a>Rettigheder til projekt til internettet

Project Operations er afhængig af en ekstern planlægningstjeneste. Tjenesten kræver, at en bruger har fået tildelt flere roller og kan læse og skrive til objekter, der er relateret til arbejdsopgavehierarkiet. Disse objekter omfatter projektopgaver, ressourcetildelinger og opgaveafhængigheder. Hvis en bruger ikke kan få vist arbejdsopgavehierarki under fanen **Opgaver**, skyldes det sandsynligvis, at projekter til Project Operations ikke er aktiveret. En bruger modtager måske enten en sikkerhedsrolle eller en fejl, der er relateret til en nægtelse af adgang.


## <a name="workaround"></a>Løsning

1. Gå til **Indstilling > Sikkerhed > Brugere > Applikationsbruger**.  

   ![Applikationslæser.](media/applicationuser.jpg)
   
2. Dobbeltklik på applikationsbrugerposten for at kontrollere følgende:

 - Brugeren har adgang til projektet. Denne verificering foretages typisk ved at sikre, at brugeren har sikkerhedsrollen **Projektleder**.
 - Microsoft Project-applikationsbrugeren findes og er konfigureret korrekt.
 
3. Hvis denne bruger ikke findes, kan du oprette en ny brugerpost. Vælg **Nye brugere**. Rediger postformularen til **Applikationsbruger**, og tilføj derefter **Applikations-ID'et**.

   ![Oplysninger om applikationsbruger.](media/applicationuserdetails.jpg)

4. Kontrollér, at brugeren er blevet tildelt den korrekte licens, og at tjenesten er aktiveret under detaljer om licensens serviceplaner.
5. Kontrollér, at brugeren kan åbne project.microsoft.com.
6. Kontrollér via projektparametrene, at systemet peger på det rigtige projektslutpunkt.
7. Kontroller, at projektapplikationsbrugeren er oprettet.
8. Anvend følgende sikkerhedsroller på brugeren:

  - Dataverse-bruger
  - Systemet Project Operations
  - Projektsystem

## <a name="error-when-updating-the-work-breakdown-structure"></a>Fejl under opdatering af arbejdsopgavehierarkiet

Når der foretages en eller flere opdateringer af arbejdsopgavehierarkiet, mislykkes ændringerne i sidste ende, og de gemmes ikke. Der opstår en fejl i planlægningsgitteret med teksten "Den seneste ændring, du har foretaget, kunne ikke gemmes".

### <a name="workaround"></a>Løsning

1. Kontrollér, at brugeren er blevet tildelt den korrekte licens, og at tjenesten er aktiveret under detaljer om licensens serviceplaner.
2. Kontrollér, at brugeren kan åbne project.microsoft.com.
3. Kontrollér, at systemet peger på det rigtige projektslutpunkt.
4. Kontroller, at projektapplikationsbrugeren er blevet oprettet.
5. Anvend følgende sikkerhedsroller på brugeren:
  
  - Dataverse-bruger eller basisbruger
  - Systemet Project Operations
  - Projektsystem
  - Dobbeltskrivningssystemet til Project Operations (denne rolle er nødvendig, hvis du installerer det ressourcebaserede/ikke-lagerbaserede scenario for Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
