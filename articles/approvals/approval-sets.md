---
title: Godkendelsessæt
description: I dette emne forklares det, hvordan du kan arbejde med godkendelsessæt, anmodninger og undersæt for disse handlinger.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323229"
---
# <a name="approval-sets"></a>Godkendelsessæt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Godkendelsessæt grupperer forespørgsler om godkendelse i mindre undergrupper af handlinger. Denne gruppering gør det muligt at behandle godkendelser i henhold til projekter i en bestemt rækkefølge, og gør nye forsøg og sekvensering muligt. Når godkendelsesanmodningerne grupperes, forbedres pålideligheden og sporingen af godkendelsesbehandlingen for store mængder godkendelser.

Godkendelsessæt angiver den overordnede behandlingstilstand for de relaterede poster. Når en godkendelsespost behandles ved hjælp af et godkendelsessæt, flyttes posten fra **Indsendt** til **Godkendt** og er ikke længere knyttet til godkendelsessættet. Hvis det ikke lykkes at godkende en post, når den er indsendt til godkendelse, har posten fortsat status som **Indsendt**, og godkendelsessættet er markeret som mislykket. Godkendelsessættet registrerer fejlmeddelelsen, der opstår.

## <a name="processing-approvals-and-approval-sets"></a>Behandling af godkendelser og godkendelsessæt
Godkendelser, der er sat i kø til behandling, er synlige i visningen **Behandling af godkendelser**. Systemet behandler alle objekter flere gange asynkront, herunder nye forsøg på at opnå godkendelse, hvis tidligere forsøg mislykkedes.

Feltet **Levetid for godkendelsessæt** registrerer det resterende antal forsøg til at behandle sættet, før det er markeret som mislykket.

## <a name="failed-approvals-and-approval-sets"></a>Mislykkede godkendelser og godkendelsessæt
Visningen **Mislykkede godkendelser** indeholder alle de godkendelser, der kræver brugerintervention. Åbn logfilerne for det tilknyttede godkendelsessæt for at identificere årsagen til fejlen.
Hvis du vælger **Prøv igen**, tilføjes levetidstallet for godkendelsessættet, godkendelsen flyttes tilbage til statussen **Behandling**, og det forsøges at behandle de resterende poster.

## <a name="configure-approval-sets"></a>Konfigurer godkendelsessæt

### <a name="enable-the-approval-sets-feature"></a>Aktiver funktionen for godkendelsessæt
Før du aktiverer funktionen Godkendelsessæt, skal du kontrollere, at der ikke er nogen godkendelser, der behandles i øjeblikket.

- Gå til siden **Projektparametre**, og vælg **Funktionskontrol** > **Aktiver moderne godkendelser**.

### <a name="turn-off-the-approval-sets-feature"></a>Deaktiver funktionen for godkendelsessæt
Før du deaktiverer funktionen Godkendelsessæt, skal du kontrollere, at der ikke er nogen godkendelser, der behandles i øjeblikket.

- Gå til siden **Projektparametre**, og vælg **Funktionskontrol** > **Deaktiver moderne godkendelser**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguration af den asynkrone tærskelværdi 
Når der oprettes godkendelsessæt, flyttes behandlingen til baggrunden, når det valgte antal poster til godkendelse overskrider den angivne tærskelværdi. Brug feltet **Asynkron tærskelværdi** til at konfigurere, hvornår godkendelsesbehandling bør køres synkront eller asynkront. Vælg en af følgende værdier:

  - Nul: Alle forespørgsler skal behandles asynkront. 
  - Tal, der er større end nul: Godkendelser behandles kun asynkront, når det indsendte antal godkendelser overskrider denne værdi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
