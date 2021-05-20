---
title: Nyheder eller ændringer i opdateringsudgivelse 16, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33a711816e8cca34c4595aa0929de9a808a48b0f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949368"
---
# <a name="project-service-automation-update-release-16-v3"></a>Opdateringsudgivelse 16 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed.  Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater en foretrukket løsning](/dynamics365/project-service/upgrade-psa-home-page).
I dette emne vises de funktioner og rettelser, der er nye eller ændrede for PSA V3, 16. opdateringsudgivelse. Denne version har build-nummer V3.10.6.34 og er generelt tilgængelig via en opdatering, du selv skal foretage, i januar 2020.


## <a name="update-release-16"></a>16. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

-   Tid og udgift

    -   Løst: Brugere, der forsøger at fremsende slettede tids- og udgiftsposter til godkendelse, modtager nu relevante fejlmeddelelser.

-   Projektstyring

    -   Løst: De ressourceenheder, der er defineret for gruppemedlemmer i skabeloner, overholdes, når skabelonerne anvendes på et nyt projekt.

    -   Løst: Forbedret håndtering af ny tildeling af postejerskab.

    -   Løst: Projekter, der er ved at blive kopieret, kan ikke kopieret, før alle kopioperationer er fuldført.

-   Ressourcestyring

    -   Løst: Udvid reserveringer kan nu håndtere korte varigheder korrekt og opretter ikke længere nul timer for udvidede reservationer.

    -   Løst: Afstemningsvisningen gengives nu, når tidszonen for projektet er +5:30 GMT, og brugerens tidszone er anderledes.

-   Sales

    -   Løst: Når et projekt, der er knyttet til en kontraktlinje, fjernes, og der tilknyttes et nyt projekt, blev de faktiske poster i det nye projekt ikke evalueret igen på baggrund af de regler for fakturering og prissætning, der er defineret på kontraktlinjen. Dette er blevet løst i denne udgivelse. Prisfastsættelsen og de faktiske poster i det netop tilknyttede projekt bliver tilbageført og genoprettet korrekt baseret på kontraktlinjens regler for prisfastsættelse og fakturering. De faktiske poster for det ikke-tilknyttede projekt vil også blive evalueret igen og genoprettet som følge heraf.

    -   Løst: Der er blevet føjet yderligere validering til en estimeret linjes **Beløb**-felt for at sikre, at null-værdier ikke bevares.

    -   Løst: Når de faktiske værdier er blevet opdateret for et projekt, tilføjes der en opdateringsknap til hovedformularen for projektet for at give brugere mulighed for at synkronisere de faktiske værdier igen.

    -   Løst: Når brugere opgraderer fra 2.X til 3.X, tillades projekter med en NULL-værdi for projektnavn.



[!INCLUDE[footer-include](../includes/footer-banner.md)]