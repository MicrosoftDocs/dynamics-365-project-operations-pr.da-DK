---
title: Nyheder i 12. opdateringsudgivelse til Project Service Automation, V3
description: Dette emne indeholder oplysninger om nyhederne i 12. opdateringsudgivelse til Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750545"
---
# <a name="project-service-automation-v3-update-release-12"></a>12. opdateringsudgivelse til Project Service Automation V3
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
