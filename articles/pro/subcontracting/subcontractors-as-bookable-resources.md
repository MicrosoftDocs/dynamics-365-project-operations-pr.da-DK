---
title: Konfigurere underleverandører som reserverbare ressourcer
description: I denne artikel forklares det, hvordan du konfigurerer og vedligeholder underleverandørressourcer, der er oprettet ud fra brugere og kontaktpersoner i systemet, så de kan knyttes til underleverandører i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67df514cd1a0bd07d4ff2582e1a7738d913e0ac5
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261316"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Konfigurere underleverandører som reserverbare ressourcer

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Følg disse trin for at konfigurere underleverandører som reserverbare ressourcer i Microsoft Dynamics 365 Project Operations.

1. Gå til **Projekt** \> **Ressourcer**, og vælg **Ny**.
2. Vælg en af følgende indstillinger i feltet **Ressourcetype** på siden **Ny reserverbar ressource**:

    - **Bruger** – Vælg denne ressourcetype, hvis underleverandøren skal have adgang til Project Operations for at angive tid eller udgifter. Hvis du vælger **Bruger**, skal underleverandøren have en gyldig licens for at få adgang til systemet.
    - **Kontakt** eller **Firma** – Vælg en af disse ressourcetyper, hvis underleverandøren ikke kræver adgang til Project Operations, men skal være tilgængelig for opgavetildelinger eller reservationer for projekter. Ingen af disse ressourcetyper giver adgang til systemet. Vælg **Firma** for at repræsentere leverandørens virksomhed som en reserverbar ressource. Vælg **Kontakt** for at repræsentere de enkelte medarbejdere hos leverandøren.

3. Afhængigt af den ressourcetype, du har valgt, bliver du bedt om at vælge den tilsvarende bruger-, firma- eller kontaktpost.
4. Vælg "Kontraktmedarbejder" i feltet **Type af arbejder** for at konfigurere underleverandøren som en reserverbar ressource.

    > [!NOTE]
    > Hvis feltet **Type af arbejder** er tomt, betragtes den reserverbare ressource som en medarbejder.

5. Hvis du har **valgt Kontraktmedarbejder** som arbejdertype, skal du vælge den leverandør, som ressourcen arbejder for.
6. Vælg ressourcens tidszone, og vælg derefter **Gem**. Hvis du vil tildele en skabelon for arbejdstimer til den reserverbare ressource, kan du vælge **Angiv kalender** på listesiden **Reserverbar ressource**.

For at knytte en reserverbar ressource til en underleverancelinje, skal ressourcen opfylde følgende betingelser:

- Den reserverbare ressource skal være en kontraktmedarbejder.
- En reserverbar ressource af ressourcetypen **Kontakt** skal være tilknyttet leverandørens konto som en kontakt. En reserverbar ressource af ressourcetypen **Bruger** skal ikke være tilknyttet leverandørens konto som en kontakt.
- Værdien i feltet **Leverandør** for den reserverbare ressource skal svare til værdien i feltet **Leverandør** for underleverancen.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Opdatere typen af arbejder- og leverandørtilknytning for reserverbare ressourcer

Feltet **Type af arbejder** for en reserverbar ressource bestemmer, om den reserverbare ressource er en kontraktmedarbejder eller en medarbejder. I feltet **Leverandør** defineres den leverandørkonto, som den reserverbare ressource er knyttet til. Hvis du knytter en reserverbar ressource til en leverandør som en kontakt, angiver du, at kontakten er en medarbejder i leverandørens virksomhed.

Hvis felterne **Type af arbejder** og **Leverandør** for en reserverbar ressource ændres, påvirker ændringerne eventuelle fremtidige valideringer af nye poster, som den reserverbare ressource opretter, f.eks. tidsposter. Ændringerne gør dog ikke eksisterende poster ugyldige.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
