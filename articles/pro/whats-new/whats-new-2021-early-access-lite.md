---
title: Nyheder i anden bølge i 2021 for tidlig adgang – Project Operations lille udrulning
description: Dette emne indeholder oplysninger om de funktioner, der er tilgængelige i anden bølge i 2021 af udgivelsen af tidlig adgang til Project Operations lille udrulning.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323904"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Nyheder i anden bølge i 2021 for tidlig adgang – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Dette emne gælder for følgende Dynamics 365 Project Operations-komponenter og -versioner:

  - Project Operations på Dataverse-miljø version 4.23.0.4

Udgivelsen anvendes kun, når et miljø har [tilvalgt tidlig adgang](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funktioner omfattet af denne udgivelse

[Administration af underentreprise](../subcontracting/subcontracting_EA_scope.md) - Denne funktion giver bedre synlighed og kontrol over alle aspekter af arbejdet på et projekt. Forhåndsvisning af administration af underentreprise omfatter følgende funktioner:

  - En projektleder kan oprette en underentreprise med en leverandør. De prislister, der er tilknyttet kreditorposten, bruges som standard til underleverancen. Leverandørkontoen har relationstypen **Kreditor** eller **Leverandør**.
  - En projektleder kan specificere alle købene som linjeelementer i underentreprisen. Underleverancelinjer kan indeholde tid, udgifter eller produkter. Transaktionsklassen for underentrepriselinjen, bestemmer, hvad linjen er beregnet til.
  - Administratoren af leverandørkontoen og projektlederen kan gentage valget for hele underleverancen. Prisfastsættelse kan justeres i købsprislister, der er tilknyttet underleverancen.
  - Hvis underentrepriselinjen er for tid kan administratoren af leverandørkontoen knytte leverandørkontakter sammen med hver underentrepriselinje i forbindelse med processen. Denne tilknytning indeholder oplysninger til den projektleder, der arbejder med underleverancen. Når en leverandørkontakt er knyttet til en underentrepriselinje, opretter systemet automatisk en reserverbar ressource ud fra kontaktpersonen, hvis der ikke allerede findes en reserverbar ressource.
  - Faktureringsmetoden på hver underentrepriselinje kan være fast pris eller tid og materialer. Der konfigureres en milepælsbaseret faktureringsplan for underentrepriselinjer med faste priser.
