---
title: Nyheder eller ændringer i opdateringsudgivelse 36, V3, til Project Service Automation
description: Dette emne angiver en liste over de funktioner og løsninger, der er tilgængelige i Microsoft Dynamics 365 Project Service Automation opdateringsversion 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 108c75598dc7dd3dd0cdb9ce68e30423d051a4cf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586659"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Nyheder eller ændringer i opdateringsudgivelse 36, V3, til Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Vi kan med glæde offentliggøre den seneste opdatering til Microsoft Dynamics 365 Project Service Automation-appen. Denne version indeholder nogle vigtige forbedringer i kvalitet, ydeevne og anvendelighed. Den er kompatibel med Dynamics 365 9.x. Hvis du vil opdatere til denne version, skal du gå til løsningsside med administrationscenteret for Dynamics 365 online og installere opdateringen. Du kan finde flere oplysninger i [Installer, opdater eller fjern en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

I dette emne vises de funktioner og rettelser, der er nye eller ændrede for Project Service Automation, 36. opdateringsudgivelse, V3. Denne version har build-nummer V3.10.57.152 og er generelt tilgængelig via en opdatering, du selv skal foretage, i oktober 2021.

## <a name="update-release-36"></a>36. opdateringsudgivelse

### <a name="bug-fixes"></a>Fejlrettelser

Følgende problemer er blevet løst.

**Generelt**
- Feltnavnet for **Standardskabelon for arbejdstid** oversættes ikke korrekt på siden **Projektparametre**.
- Asynkrone plug-ins håndterer ikke undtagelser, der er relateret til **SharedVariableService**, korrekt.

**Tid og udgift**
- Når der mangler kladdelinjer, eller brugeren ikke har de korrekte rettigheder til at læse kladdelinjer, opstår der en fejl, når projektgodkendelser annulleres.
- Brugere kan ikke annullere en godkendelse, når en omkostnings- eller tidsregistrering har mere end én tilknyttet projektgodkendelse.
- **Fravær** og **Ferie** er ikke oversat korrekt til det kinesiske sprog i et opslag på siden for hurtig oprettelse af **Tidsregistrering**.

**Ressourcestyring**
- Brugeren kan ikke søge efter ressourcer i **Planlægningsassistent**, når visningstilstanden er angivet til **Dag**, **Uge** eller **Måned**.
- Generiske ressourcer må ikke have tomme placeringsnavne. 
- Hvis du lukker en kontrakt som tabt, annulleres fremtidige reservationer ikke.

**Salg**
- Når der er en stor mængde produkter i et miljø, forringes ydeevnen i gitteret **Materialeestimat**.
- Når du opretter et projekt ud fra en skabelon, bruges projektvalutaen ikke som standard for den pågældende projektleders kontraktenhed.
- Faktiske beløb stemmer ikke altid overens med det, der afspejles i det projekts forfaldne beløb, eller beløbene bliver negative i bestemte scenarier.
- Der opstår en fejl, når du knytter et projekt, der er oprettet fra projektskabelonen, til en kontraktlinje.
- Brugerne kan slette en kontraktlinje med milepælene **Klar til fakturering** og **Faktura oprettet**. Det bør ikke være tilladt.
- Når der importeres estimater fra et projekt, angives oplysninger om tilbudslinjens fakturerbarhed ikke korrekt, når opgavebaseret fakturering er aktiveret for tilbudslinjen.
- Når du tilføjer en faktureringsmilepæl for fast pris, afspejles milepælen først i milepælens undergitter, indtil siden opdateres.
- Der oprettes en nulreferenceundtagelse, når du opretter en projektkontrakt med et tilbudsnavn, der er null.
- Manuelle tilstandsopgaver, hvor projektvalutaen er forskellig fra ressourcens valuta, resulterer i forkerte prisestimater.
- Brugere kan ikke gennemføre en transaktion, der er blevet korrigeret korrekt af en korrigerende faktura.
- Deaktiverede transaktionskategorier vises i gitteret **Udgiftsestimater**.



