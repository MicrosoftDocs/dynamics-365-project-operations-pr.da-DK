---
title: Levere arbejdsestimater for et projekt under salgsprocessen
description: Sådan leverer du arbejdsestimater for et projekt under salgsprocessen i Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: acb1e5f598e3e057be78a70bc4f5c66c510053a08f4efb0a1595cf4853171662
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002459"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Levere arbejdsestimater for et projekt under salgsprocessen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Under salgsprocessen kan du udarbejde salgsestimater fra bunden med tilbudslinjer. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funktioner i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] giver en mere videnskabelig og fremsynet måde at fremsætte salgsestimater på ved at opdele arbejdselementer og knytte de relevante attributter, der bidrager til estimater for projektet, til arbejdsopgavehierarkiet.  
  
 Når du har vundet salget, kan du bruge det tilknyttede arbejdsopgavehierarki i projektplanen og raffinere det efter dine behov til gennemførelse af projektet.  
  
## <a name="link-a-project-to-a-quote-line"></a>Sammenkæde et projekt med en tilbudslinje  
 Når du opretter en projektbaseret tilbudslinje, kan du oprette et nyt projekt fra tilbudslinjen. Du kan derefter bruge projektskabeloner, der enten er forudkonfigurerede standardprojektplaner og økonomiske estimater, der er fælles for din organisation, eller en kopi af en projektplan og estimater fra et tidligere projekt. Når du opretter et projekt, kan du vælge en projektskabelon for at få et grundlag for at tilpasse projektplanen, estimater og rollekrav. Når projektet oprettes fra tilbuddet, knyttes det automatisk til tilbudslinjen.  
  
## <a name="project-estimate-components"></a>Projektestimatkomponenter  
 Arbejdsopgavehierarkiet i et projekt er en måde at opdele arbejdet i opgaver, vedligeholde et hierarki af opgaver og tildele et estimat over den indsats, der kræves for at fuldføre hver opgave. Du kan også knytte roller til en opgave for at angive en vurdering af den ressourcetype, der kræves for at fuldføre en opgave og en tidsplan.  
  
 Med arbejdsopgavehierarkiet kan du bestemme arbejdsindsats og planlægge estimater. Som standard bruger projektet standardprislister, som du definerede tidligere. De kost- og salgspriser, der er defineret i prislisterne, hjælper med at bestemme økonomiske estimater for projektets arbejdsopgavehierarki.  
  
 Hvis dit projekt er knyttet til et tilbud, og tilbuddet har en anden prisliste end standardprislisten, bruges tilbuddets prisliste til økonomiske estimater.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importere estimater fra et projekt til et tilbud  
 Når du har projektestimater i projektet, kan du importere disse estimater til tilbudslinjen:  
  
-   I **Tilbudslinjedetaljer** skal du klikke på **Importér fra estimat**. 

-   Vælg, om projektestimater, der er opsummeret efter transaktionstype, rolle eller nodeniveau for arbejdsopgavehierarki, skal importeres.  
  
### <a name="see-also"></a>Se også  
 [Vejledning til projektledere](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]