---
title: Nyheder eller ændringer i opdateringsudgivelse 24, V3, til Project Service Automation
description: I dette emne angives de funktioner og rettelser, der er tilgængelige til Project Service Automation, opdateringsudgivelse 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 63bf96bfeed30ceefab072640172a6a0dafd20f5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581553"
---
# <a name="project-service-automation-update-release-24-v3"></a>Opdateringsudgivelse 24 til Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for at kunne annoncere den seneste opdatering til programmet Project Service Automation til Dynamics 365. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Denne version er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til Administrationen for Dynamics 365 online og herefter til løsningssiden for at installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation V3, 24. opdateringsudgivelse. Denne version har build-nummer V 3.10.42.43 og er generelt tilgængelig via en opdatering, som du selv skal foretage, i oktober 2020.

## <a name="update-release-24"></a>24. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

**Sales**

Følgende problemer er blevet løst:

- Der opstod en fejl under angivelse af standardprislisten for produkter.
- Tilbuddets ydeevne som vundet er langsom på grund af kopien af posterne for den integrerede prisliste og rollepriser.
- **Projektkontrakt/Salgshub** > **Produktlinjeelement/Ordrelinjemængde** afrundes automatisk til nærmeste heltal.
- Opløft til systemrettigheder, når du læser prislister.
- Kopier kundens adressefelter **address1_freighttermscode** og **address1_shippingmethodcode** til Tilbud/Ordre. 


**Tid og udgift**

Følgende problemer er blevet løst:

- **Gitteret for tidsregistrering** understøtter ikke funktionsmåden for **Kun dato**.
- **Tidsregistrering** opdateres ikke automatisk. Der skal bruges manuel opdatering.
- Det er ikke muligt at importere tidsregistreringer fra en tildeling, når der er en pause (0 timer) i en ressources tildelinger.
- Når du opretter en tidsregistrering, skal du angive starttidspunktet til det samme som **msdyn_date**.
- Aktivér masseredigering for tidsregistrering igen.

**Ressourcestyring**

Følgende problemer er blevet løst:

- Hvis du forsøger at opdatere statussen for en intern dagsreservation uden et krav, udløses en null-ref-undtagelse.
- Fejl under indlæsning af **Afstemningsvisningen**.


**Projektstyring**

Følgende problemer er blevet løst:

- Automatisk lagring i **Projektplanlægning** kan ikke gennemføres, når man skifter fra **Manuel** til **Automatisk**.
- Udgiftsomkostninger skal ikke beregnes i forhold til variansen i **Projektsporingsgitteret**.
- Uoverensstemmende funktionsmåde for kolonnerne **Estimerer mærker** under indlæsningen i forhold til ændring af typen **Tidsfase**.
- De faktiske omkostninger på et projekt afspejler muligvis ikke totalerne fra de **Faktiske værdier**.
- **Den anslåede slutdato** under fanen **Oversigt** stemmer ikke overens med **WBS-planen**.
- **Opdater faktiske timer** på udrykning fungerer ikke korrekt.
- En projektleder uden for **BU**-roden kan ikke oprette et projekt.
- Ændringer af opgave eller kategori i **Udgiftsestimater** bevares ikke.
- **Kopi af kontrakt** kopierer fakturaplanerne og kørselsstatus.
- Knappen **Opdater faktiske oplysninger** beregner hovedopgaver ukorrekt.
- Tilføjelsesprogram til Microsoft Project: ret en fejl i null-reference, hvis et teammedlem har en tom ressourceenhed.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
