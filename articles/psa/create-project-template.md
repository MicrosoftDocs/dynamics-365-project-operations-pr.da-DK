---
title: Oprette en projektskabelon
description: Sådan opretter du en projektskabelon i Project Service
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
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997234"
---
# <a name="create-a-project-template-project-service"></a>Oprette en projektskabelon (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektskabeloner sparer dig tid, hvis virksomheden regelmæssigt afgiver bud på lignende typer projekter. De indeholder er standardsæt af roller og estimerede timer for en type projekt. Kontoadministratorer og projektledere kan oprette projekter, der er baseret på en skabelon, eller de kan kopiere skabelonen og foretager en af deres egne.  
  
## <a name="components-of-project-template"></a>Komponenter af projektskabelon
 En projektskabelon består af tre komponenter:  
  
- **Arbejdsopgavehierarki**: Et arbejdsopgavehierarki i en projektskabelon har det samme sæt af elementer som i projektet. Du kan oprette et opgavehierarki, knytte roller til opgaven, definere planlægningsattributter, angive afhængigheder og få vist alle data i Gantt. Arbejdsopgavehierarkier i projektskabeloner understøtter også opgavetilstande for alle opgaver. Der er ingen forskel mellem en projektskabelon og et projekt, når du opretter arbejdsplan.  
  
- **Projektestimater**: Projektestimater i skabeloner fungerer på samme måde som de gør i projekter, bortset fra prislister for standardomkostninger og salgspriser altid er standardomkostninger og salgsprislister, der er defineret i parametrene for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Resten af funktionaliteten er den samme som i et projekt.  
  
- **Projektteamdannelse**: Når du danner en projektgruppe for en projektskabelon, kan du ikke reservere en navngivet ressource i en skabelon. Du kan bruge **Opret projektteam** i arbejdsopgavehierarkier til at generere en række standardressourcer. Du kan også angive de nødvendige færdigheder og kompetencer for standardressourcer. Du kan ikke erstatte en standardressource med en reserverbar ressource i projektskabeloner.  
  
## <a name="create-a-project-from-a-template"></a>Oprette et projekt på grundlag af skabelon  
 Du kan oprette et projekt fra en skabelon på følgende måder:  
  
-   Når du opretter et projekt fra tilbuddet, kan du vælge en projektskabelon i projektets formular til hurtig oprettelse.  
  
-   Når du opretter et projekt ved at klikke på **Nyt projekt**, vises projektformularen, før du gemmer posten. Herfra kan du klikke på feltet **Vælg en skabelon** og vælge fra listen over foruddefinerede projektskabeloner i organisationen.  
  
-   Klik på **Opret projekt fra en skabelon** på siden **Projektskabelon** for at oprette et projekt fra skabelonen.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopiere komponenter fra en skabelon til et projekt  
 Når du kopierer komponenter i en skabelon til et projekt, er der et par ting, du bør vide.  
  
 **Kopiere et arbejdsopgavehierarki**: Når du kopierer arbejdsopgavehierarkiet fra en projektskabelon, anvendes arbejdstimer fra projektets kalender til planlægning af opgaver, hvis projektet har en anden projektkalender end skabelonen. Dette justerer planen for sikkerhedskopiering af projektkalenderen. Den første opgave på arbejdsopgavehierarkiet tager ligeledes projektets startdato, så resten af opgavehierarkiplanlægningen opdateres baseret på varigheden og afhængigheder, der er angivet i skabelonens arbejdsopgavehierarki.  
  
 **Kopiere projektestimater**: Når du kopierer på tværs af projektestimatlinjer, opdateres prislister baseret på den objekt, der er ejer af projektet, for kostprisliste og kunden for salgsprislisten. Kostprisen og salgspriserne bestemmes fra disse prislister på projekter, der er knyttet til et salgsobjekt.  
  
 **Kopiere en projektgruppe**: Når du kopierer projektgruppen fra skabelonen til et projekt, kopieres standardressourcerne på tværs af, sammen med de færdigheder og kompetencer, der er defineret i skabelonen. Standardressourcetildelinger bevares også i projektskabelonen.  
  
### <a name="see-also"></a>Se også  
 [Vejledning til projektledere](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]