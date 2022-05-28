---
title: Godkendelsessæt i Project Service Automation
description: Dette emne indeholder oplysninger om godkendelsessæt, forespørgsler og undergrupper af disse handlinger.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583301"
---
# <a name="approval-sets-in-project-service-automation"></a>Godkendelsessæt i Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Godkendelsessæt grupperer forespørgsler om godkendelse i mindre undergrupper af handlinger. Denne gruppering gør det muligt at behandle godkendelser i projektrækkefølge og giver mulighed for at forsøge igen og sekvensering. Gruppering forbedrer pålideligheden og sporbarheden af godkendelsesbehandling for store mængder godkendelser.

Godkendelsessæt angiver den overordnede behandlingstilstand for de relaterede poster. Når en godkendelsespost behandles ved hjælp af et godkendelsessæt, flyttes posten fra **Indsendt** til **Godkendt**, og forbindelsen til godkendelsessættet fjernes. Hvis det ikke lykkes at godkende en post, når den er indsendt til godkendelse, har posten fortsat status som **Indsendt**, og godkendelsessættet er markeret som mislykket. Godkendelsessættet registrerer fejlmeddelelsen, der opstår.

## <a name="processing-approvals-and-approval-sets"></a>Behandling af godkendelser og godkendelsessæt
Godkendelser, der er sat i kø til behandling, er synlige i visningen **Behandling af godkendelser**. Systemet forsøger at behandle alle objekter flere gange asynkront, herunder at køre en godkendelse igen, hvis tidligere forsøg mislykkedes.

Feltet **Levetid for godkendelsessæt** registrerer det resterende antal forsøg til at behandle sættet, før det er markeret som mislykket.

## <a name="failed-approvals-and-approval-sets"></a>Mislykkede godkendelser og godkendelsessæt
Visningen **Mislykkede godkendelser** indeholder alle godkendelser, der kræver brugerintervention. Åbn logfilerne for det tilknyttede godkendelsessæt for at identificere årsagen til fejlen.
Hvis du vælger **Prøv igen**, tilføjes levetidstallet for godkendelsessættet, godkendelsen flyttes tilbage til statussen **Behandling**, og det forsøges at behandle de resterende poster.

## <a name="configure-approval-sets"></a>Konfigurer godkendelsessæt

###  <a name="enable-the-approval-sets-feature"></a>Aktiver funktionen for godkendelsessæt
Før du aktiverer funktionen Godkendelsessæt, skal du kontrollere, at der ikke er nogen godkendelser, der behandles i øjeblikket.

- Gå til siden **Projektparametre**, og vælg **Funktionskontrol** > **Aktiver moderne godkendelser**.

### <a name="turn-off-the-approval-sets-feature"></a>Deaktiver funktionen for godkendelsessæt
Før du deaktiverer funktionen Godkendelsessæt, skal du kontrollere, at der ikke er nogen godkendelser, der behandles i øjeblikket.

- Gå til siden **Projektparametre**, og vælg **Funktionskontrol** > **Deaktiver moderne godkendelser**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguration af den asynkrone tærskelværdi 
Når der oprettes godkendelsessæt, flyttes behandlingen til baggrunden, når det valgte antal poster til godkendelse overskrider den angivne tærskelværdi. Brug feltet **Asynkron tærskelværdi** til at konfigurere, hvornår godkendelsesbehandling bør køres synkront eller asynkront.
De gyldige værdier er:

  - Nul: Alle forespørgsler skal behandles asynkront. 
  - Tal, der er større end nul: Godkendelser behandles kun asynkront, når det indsendte antal godkendelser overskrider denne værdi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
