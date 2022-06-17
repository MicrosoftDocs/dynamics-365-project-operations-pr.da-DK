---
title: Godkendelsessæt
description: I denne artikel forklares det, hvordan du kan arbejde med godkendelsessæt, forespørgsler og undergrupper af disse handlinger.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 5e030c1aa4a41b428a0f4541fd204a7a3deaba08
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918075"
---
# <a name="approval-sets"></a>Godkendelsessæt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Godkendelsessæt grupperer forespørgsler om godkendelse i mindre undergrupper af handlinger. Denne gruppering gør det muligt at behandle godkendelser i henhold til projekter i en bestemt rækkefølge, og gør nye forsøg og sekvensering muligt. Når godkendelsesanmodningerne grupperes, forbedres pålideligheden og sporingen af godkendelsesbehandlingen for store mængder godkendelser.

Godkendelsessæt angiver den overordnede behandlingstilstand for de relaterede poster. Når en godkendelsespost behandles ved hjælp af et godkendelsessæt, flyttes posten fra **Indsendt** til **Godkendt** og er ikke længere knyttet til godkendelsessættet. Hvis det ikke lykkes at godkende en post, når den er indsendt til godkendelse, har posten fortsat status som **Indsendt**, og godkendelsessættet er markeret som mislykket. Godkendelsessættet registrerer fejlmeddelelsen, der opstår.

## <a name="processing-approvals-and-approval-sets"></a>Behandling af godkendelser og godkendelsessæt
Godkendelser, der er sat i kø til behandling, er synlige i visningen **Behandling af godkendelser**. Systemet behandler alle objekter flere gange asynkront, herunder nye forsøg på at opnå godkendelse, hvis tidligere forsøg mislykkedes.

Feltet **Levetid for godkendelsessæt** registrerer det resterende antal forsøg til at behandle sættet, før det er markeret som mislykket.

Godkendelsessæt behandles via den periodiske aktivering, der er baseret på et **Cloudflow** kaldet **Project Service – Planlæg tilbagevendende projektgodkendelsessæt**. Det kan du se i **Løsningen** kaldet **Project Operations**. 

Kontrollér, at flowet er aktiveret ved at fuldføre følgende trin.

1. Log som administrator på [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Skift til det miljø, du bruger til Dynamics 365 Project Operations, i øverste højre hjørne.
3. Vælg **Løsninger** for at få vist en liste over de løsninger, der installeres i miljøet.
4. Vælg **Project Operations** på listen med løsninger.
5. Skift filteret fra **Alle** til **Cloudflow**.
6. Kontrollér, at flowet **Project Service – Planlæg tilbagevendende projektgodkendelsessæt** er angivet til **Til**. Hvis det ikke er det, skal du vælge flowet og derefter vælge **Slå til**.
7. Kontrollér, at behandlingen sker hvert femte minut, ved at gennemse listen **Systemjob** i området **Indstillinger** i Project Operations Dataverse-miljøet.

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
