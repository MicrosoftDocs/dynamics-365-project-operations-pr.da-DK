---
title: Administrer projekttilbud
description: Denne artikel indeholder oplysninger om projekttilbud.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79da23d83133241204eaad44e39e64c5c6a1591d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826074"
---
# <a name="manage-project-quotes"></a>Administrer projekttilbud

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I Dynamics 365 Project Operations er projekttilbud designet til at hjælpe med at sammensætte forslag til projektarbejde. Strukturen i et projekttilbud i Project Operations er tiltænkt projektforslag med følgende komponenter:

  - Tilbudslinjer, der identificerer de separate komponenter i arbejdet, som vil blive præsenteret som komponenter på højt niveau.
  - Tilbudslinjedetaljer, der identificerer og estimerer arbejdet for de enkelte komponenter eller tilbudslinje på højt niveau. Planen eller estimerede datoer og de finansielle aspekter for arbejdet er knyttet til den pågældende tilbudslinje.
  - Kontraktmodeller og fakturerbare komponenter konfigureres for hver tilbudslinje. Denne konfiguration hjælper med at vurdere fordelingen af omsætning, forbrug og rentabilitet for de enkelte tilbudslinjer og det overordnede tilbud.

## <a name="view-all-project-quotes"></a>Få vist alle projekttilbud

Du kan se en liste over alle projekttilbud på listesiden **Tilbud**. 

1. Gå til **Salg** > **Tilbud**. Der vises en liste over alle dine projekttilbud i systemet. 
2. Brug **Visningsskifteren** til at vælge andre filtrerede visninger for de pågældende tilbud. Ved hjælp af brugerdefinerede filterkriterier kan du konfigurere dine egne visninger og navigationsindstillinger.

Der kan oprettes eller slettes tilbud fra denne listeside eller detaljesider.

 > [!NOTE]
 > Tilbud med tilknyttede projekter, opgaver, estimater, kladder og/eller faktiske værdier kan ikke slettes. Og når et tilbud lukkes som Vundet eller Tabt, kan det ikke længere slettes eller ændres. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
