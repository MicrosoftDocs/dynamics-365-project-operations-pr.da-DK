---
title: Se det fakturerbare tidsforbrug for ressourcer
description: Dette emne indeholder oplysninger om visningen ressourceforbrug.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992827"
---
# <a name="view-chargeable-utilization-for-resources"></a>Se det fakturerbare tidsforbrug for ressourcer

[!include [banner](../includes/psa-now-project-operations.md)]
 
Visningen **Tidsforbrug** på siden **Tidsforbrug for ressource i Project Service** viser fakturerbart tidsforbrug for hver reserverbar ressource. Da visningen er baseret på planlægningsområdet, finder du mange af de samme funktioner.

> ![Skærmbillede af visningen Tidsforbrug](media/FAQ-utilization-1.png)
 

Beregningen af fakturerbart tidsforbrug fungerer på følgende måde:

   Fakturerbart tidsforbrug = (fakturerbare faktiske timer)/(ressourcens kapacitet)

Cellerne repræsenterer det beregnede fakturerbare tidsforbrug for den periode, der er valgt (dage, uger eller måneder).

Farverne i hver celle viser det fakturerbare tidsforbrug for en ressource i forhold til ressourcens fakturerbare tidsforbrug, der er målet. 

Det tidsforbrug, der er målet, kan indstilles i enten ressourcens standardrolle eller i den enkelte ressource. Beregningen ser først på personen for målet og derefter på ressourcens standardrolle.

## <a name="set-target-on-a-resource"></a>Angive målet for en ressource

1. Gå til **Ressourcer** \> **Ressourcer**. 
2. Vælg en ressource for at åbne posten. 
3. Under fanen **Project Service** kan du angive ressourcens mål-tidsforbrug.

> ![Skærmbillede, hvor fanen Projektstyring bruges til at angive det tidsforbrug, der er målet](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Angive mål-tidsforbrug for en rolle

1. Gå til **Ressourcer** \> **Ressourceroller**. 
2. Vælg en rolle og åbn posten. 
3. Indstil måltidsforbruget for rollen.

> ![Skærmbillede, hvor Ressourceroller indstilles til det tidsforbrug, der er målet](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Beregne det fakturerbare tidsforbrug for en ressource?

For at beregne det fakturerbare tidsforbrug for en ressource skal du opfylde nogle forudsætninger. 

### <a name="set-default-role-for-individual-resource"></a>Angive standardrolle for individuel ressource

For det første skal mål-tidsforbruget angives i enten den enkelte ressource eller i ressourceroller. Hvis du bruger ressourceroller til mål, skal hver enkelt ressource have en standardrolle. 

1. Du kan angive rollen ved at gå til **Ressourcer** \> **Ressourcer**. 
2. Vælg en ressource, åbn posten, og vælg derefter fanen **Project Service**. 
3. I gitteret **Resourcerolle** skal du sørge for, at der er en rolle til ressourcen, og at **Er standard** er angivet til **Ja**.
 
### <a name="change-billing-type-for-resource-role"></a>Skift faktureringstype for ressourcerolle

Ressourcerollerne skal indstilles til faktureringstypen **fakturerbar**. 

1. Gå til **Ressourcer** \> **Ressourceroller**. 
2. Åbn den post, du ønsker at opdatere, og indstil derefter faktureringstypens standard til **Fakturerbar**.

### <a name="set-working-hours-for-resource-role"></a>Angive arbejdstimer for ressourcerolle
 
Ressourcen skal have arbejdstimer til kapacitetsberegningen. 

1. Gå til **Ressourcer** \> **Ressourcer**. 
2. Vælg en ressource for at åbne posten, og vælg derefter **Vis arbejdstimer**. 
3. Du kan masseopdatere listen over ressourcer ved at anvende en **arbejdstimeskabelon** fra visningen **Ressourceliste**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Fejlfinding af fakturerbare faktiske timer

De faktiske fakturerbare timer er hentet fra objektet **Faktiske**. Faktiske med faktureringstypen **fakturerbar** medtages i beregningen, og derfor skal du have projekter, hvor de faktiske værdier er fakturerbare.

Hvis du ikke kan se fakturerbart tidsforbrug, er her nogle ting, du kan kontrollere:

- Ressourcen har definerede arbejdstimer for kapacitet.
- Ressourcen er enten et individuelt definerede tidsforbrugmål eller har en standardrolle tildelt til den. Rollen med et defineret tidsforbrugmål.
- Faktiske har faktureringstypen **fakturerbar** for den periode, du forventer en beregning af tidsforbrug for. Kontrollér følgende, hvis du får vist faktiske med andre faktureringstyper end fakturerbar:

  - Den rolle, der er brugt på den faktiske indeholder en anden standardfaktureringstype end fakturerbar.
  - Rollen i den projektkontraktlinje, der sikkerhedskopierer projektet, er indstillet til ikke-fakturerbar.
  - Projektet har ikke en tilknyttet kontraktlinje.



[!INCLUDE[footer-include](../includes/footer-banner.md)]