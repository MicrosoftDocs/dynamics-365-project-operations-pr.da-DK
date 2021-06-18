---
title: Opret projekttilbud ud fra salgsmuligheder
description: Dette emne indeholder oplysninger om oprettelse af et projekttilbud fra en salgsmulighed.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d678fce7a6b52522500a77daecc46353ff17fbf2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009789"
---
# <a name="create-project-quotes-from-opportunities"></a>Opret projekttilbud ud fra salgsmuligheder

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Der kan oprettes tilbud fra projektsalgsmuligheder på følgende måder:

- Fra fanen **Tilbud** på siden **Projektsalgsmulighed**
- Fra flowet for salgsprocessen for salgsmulighed
- Ved at opdatere salgsmulighedsreferencen i et eksisterende tilbud

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Fra fanen Tilbud på siden Projektsalgsmulighed

Hvis du vil oprette et projekttilbud ud fra en salgsmulighed, skal du benytte følgende fremgangsmåde.

1. Åbn siden **Projektsalgsmulighed**, og vælg derefter fanen **Tilbud**. 
2. I undergitteret **Tilbud** skal du vælge **+** for at oprette et nyt projekttilbud, der er baseret på en salgsmulighed. Alle salgsmulighedslinjer og relaterede projektprislister kopieres til det nye tilbud fra salgsmuligheden.

## <a name="from-the-opportunity-sales-process-flow"></a>Fra flowet for salgsprocessen for salgsmulighed

Hvis du vil oprette et tilbud ud fra salgsprocesflowet for salgsmuligheden, skal du benytte følgende fremgangsmåde.

1. Åbn salgsmuligheden fra salgsprocesflowet for salgsmuligheden.
2. Vælg fasen **Kvalificer**. 
3. Vælg **Næste**, og vælg derefter **+ Opret** for at oprette et nyt tilbud. De fleste oplysninger under fanen **Oversigt** for dette nye tilbud vil være angivet som standard fra salgsmuligheden. 
4. Angiv de påkrævede oplysninger, der mangler, eller opdater standardværdier efter behov under fanen **Oversigt**,
5. Vælg **Gem**. Det nye tilbud oprettes og knyttes til salgsmuligheden. Du kan nu få vist tilbudsoplysningerne under fanen **Tilbud** på siden **Salgsmulighed**. 

   Salgsprocessen for salgsmuligheden flyttes til næste fase, **Foreslå**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Ved at opdatere salgsmulighedsreferencen i et eksisterende tilbud

Et eksisterende tilbud kan knyttes til en salgsmulighed. Benyt følgende fremgangsmåde for at opdatere oplysningerne om salgsmuligheder i et eksisterende tilbud.

1. Åbn siden **Tilbud**, og vælg derefter fanen **Oversigt**.
2. I feltet **Salgsmulighed** skal du vælge den salgsmulighed, som du vil knytte til tilbuddet. Du kan se tilbuddet i gitteret **Tilbud** for salgsmuligheden. 
3. Ved hjælp af salgsprocessen for salgsmuligheden kan salgsmuligheden flyttes til næste fase, **Foreslå**. 

   Når du flytter en salgsmulighed til denne fase, kan du vælge dette tilbud på en liste over tilbud, der er knyttet til salgsmuligheden. Hvis du vælger dette tilbud, betyder det, at du fortsætter med det.

   Alle de andre tilbud, der er knyttet til salgsmuligheden, er stadig tilgængelige og aktive, indtil et af dem er vundet. Du kan flytte salgsprocessen tilbage til forrige fase **Kvalificer** og vælge et andet tilbud, som du ønsker at fortsætte med.


[!INCLUDE[footer-include](../includes/footer-banner.md)]