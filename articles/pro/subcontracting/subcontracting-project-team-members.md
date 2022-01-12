---
title: Projektteammedlemmer, som er omfattet af en underentreprise
description: I dette emne forklares det, hvordan du hyrer projektteammedlemmer, der er omfattet af en underentreprise, i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: b98fc356d7de77fa7f05667acaa5569a7053e4d1
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903373"
---
# <a name="subcontracting-project-team-members"></a>Projektteammedlemmer, som er omfattet af en underentreprise

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I Microsoft Dynamics 365 Project Operations kan du vælge at hyre ubemandede eller bemandede projektteammedlemmer fra en underleverandør.

- Ubemandede projektteammedlemmer har fået tildelt en generisk ressource.
- Bemandede teammedlemmer har fået tildelt en navngivet ressource.

Når du knytter et projektteammedlem til en underentrepriselinje, skal alle omkostninger for tildeling af opgaver til teammedlemmet genberegnes på grundlag af den indkøbsprisliste, der er knyttet til underentreprisen.  På fanen **Estimater** på siden **Projektdetaljer** skal du vælge knappen **Opdater priser** for at se opdateret prisfastsættelse og/eller omkostninger, der er resultatet af beslutningen om at anvende en underleverandør. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Ansættelse af et ubemandet projektteammedlem fra en underleverandør
Siden **Teammedlemsoplysninger** indeholder felter til underleverandører og underentrepriselinjer, hvor en projektleder kan give udtryk for, hvordan han eller hun vil udnytte den kapacitet, der kræves fra en underentreprise. For at hyre et projektteammedlem fra en underleverandør som en generisk ressource, skal du følge disse trin:

1.  Vælg en underleverandør på siden **Teammedlemsoplysninger**.

2.  Du kan kun vælge underleverandører med statussen **Kladde** eller **Bekræftet**. **Lukkede** eller **Annullerede** underentrepriser kan ikke vælges. 

3.  Feltet **Underentrepriselinje** bliver synligt, når du har valgt en underleverandør.

4.  I feltet **Underentrepriselinje** kan du kun vælge de underentrepriselinjer, der er for tid. Du kan ikke vælge underentrepriselinjer for udgifter eller materiale.

5.  Rollen for projektteammedlemsposten skal svare til rollen på underentrepriselinjen. Derved sikres det, at den tid, der estimeres for rollen i projektet, er den samme rolle, som den, der købes på underentrepriselinjen. 

Når et generisk teammedlem knyttes til en underleverandør og underentrepriselinje, opdateres feltet **Medarbejdertype** i rækken for det generiske teammedlem til **Kontraktmedarbejder**, og **Validering af underleverandør** angives til **Gyldig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Ansættelse af et bemandet projektteammedlem fra en underleverandør
På samme måde som ved kapacitet for generiske eller ubemandede teammedlemmer kan den medarbejderkapacitet, der kræves til et projekt, også knyttes til en underleverandør. For at hyre et navngivet projektteammedlem fra en underleverandør, skal du følge disse trin:

1.  Kontrollér, at den navngivne ressource er konfigureret som en kontraktmedarbejdertype for den ressource, der kan reserveres. Du skal også kontrollere, at feltet **Leverandør** på den reserverbare ressource svarer til leverandøren på den underleverandør, du vælger. 

2.  Du kan kun vælge underleverandører med status som **Kladde** eller **Bekræftet**. **Lukkede** eller **Annullerede** underentrepriser kan ikke vælges. 

3.  Feltet **Underentrepriselinje** bliver synligt, når du har valgt en underleverandør.

4.  I feltet **Underentrepriselinje** kan du kun vælge de underentrepriselinjer, der er for tid. Du kan ikke vælge underentrepriselinjer for udgifter eller materiale.

5.  Rollen for projektteammedlemsposten skal svare til rollen på underentrepriselinjen. Derved sikres det, at den tid, der estimeres for rollen i projektet, er den samme rolle, som den, der købes på underentrepriselinjen. 

Navngivne projektteammedlemmer, der er konfigureret som kontraktmedarbejdere af typen **Reserverbar ressource**, vises med statussen for gyldighed af underentreprisen som **Ikke gyldig**, hvis de ikke er knyttet til en underleverandør. Når et navngivet projektteammedlem knyttes til en underleverandør og underentrepriselinje, opdateres feltet **Medarbejdertype** i rækken for teammedlemmet til **Kontraktmedarbejder**, og **Validering af underleverandør** angives til **Gyldig**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
