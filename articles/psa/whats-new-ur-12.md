---
title: Nyheder eller ændringer i opdateringsudgivelse 12, V3, til Project Service Automation
description: Dette emne indeholder oplysninger om nyhederne i 12. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143821"
---
# <a name="project-service-automation-update-release-12-v3"></a>Opdateringsudgivelse 12 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne offentliggøre den seneste opdatering til applikationen Dynamics 365 Project Service Automation (PSA). Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og gå til siden med løsninger for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 12. opdateringsudgivelse. Denne version har build-nummer V3.10.2.34 og er generelt tilgængelig via en opdatering, du selv skal foretage, i oktober 2019.

## <a name="update-release-12"></a>12. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

- Tid og udgift

    - Løst: Fejlmeddelelser for tidsregistrering er blevet opdateret med mere relevant kontekst.
    - Løst: Tidsregistreringsgitter og -planlægning viser det lodrette rullepanel korrekt, når det er nødvendigt.
    - Løst: Sendte udgifter og tidsregistreringer kan godkendes.
    - Løst: Dialogmeddelelsen for bekræftelse af annullering af godkendelse er blevet rettet, så den nu afspejler statussen for godkendelsen, når den ændres fra **Godkendt** til **Sendt**.
    - Løst: Felterne **Pris**, **Enhed** og **Antal** låses nu på udgiftsposten, når den er godkendt.

- Projektstyring

    - Løst: Handlingen **Nye** på hovedformularen **Teammedlem** er blevet fjernet.
    - Løst: Ressourcetildelinger er blevet opdateret til at redegøre for unøjagtige afrundingsfejl, som har medført et skifte i en opgaves slutdato.
    - Løst: I opgavegitteret vises de relevante fejl på serversiden.
    - Løst: Gruppemedlemmets navn gengives nu i opgavepersonvælgeren i stedet for stillingsnavnet.

- Ressourcestyring

    - Løst: Oplysninger om ressourcekrav for projekter, der er oprettet ud fra en skabelon, anvender nu projektkalenderen.
    - Løst: Færdigheder og kompetencer er nu som standard baseret på det ressourcekrav, der blev oprettet for den pågældende rolle, frem for på rollemasterdata.

- Sales

    - Løst: Der findes identiske objekt-ID'er i formularen **Hovedkontrakt**.
    - Løst: Logikken er blevet opdateret for at gøre fanen **Tilbudsanalyse** synlig, så den viser metadataopsætningen for fanen.
    - Løst: Regnskabsdatoen på den faktiske post kommer nu fra datoen for registrering af tid/udgifter og ikke fra datoen for godkendelsen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]