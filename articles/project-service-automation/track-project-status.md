---
title: Spore et projekts status
description: Sådan sporer du et projekts status i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750616"
---
# <a name="track-a-projects-status-project-service"></a>Spore et projekts status (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Brug [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] til at spore status for en klients projekt.  

Som engagementet skrider frem, opdateres projektets faser, så de afspejler fasen i engagementet:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Ny**    | Når du opretter et projekt, indstilles fasen til **Ny**. Hvis du har oprettet projektet fra en skabelon, kan projektet i denne fase have en tidsplan, estimater og teamdata. Ellers vil det være projektets disposition, og du skal manuelt angive resten af projektkomponenterne. |
|  **Tilbud**   |      Når du knytter et projekt til et tilbud eller opretter det fra et tilbud, angives projektfasen til **Tilbud**, og de forventede start- og slutdatoer opdateres også. Når projektet er i fasen tilbud, vises oplysninger om tilbuddet under fanen **Salg** på siden **Projekt**.      |
|   **Planlæg**   |                                     Når du vinder et tilbud, der er knyttet til et projekt, og når engagementet går videre til kontraktfasen, opdateres projektfasen til **Plan**. Kontraktoplysninger vises under fanen **Salg** på siden **Projekt**.                                      |
| **Fuldført** |                    Når projektarbejdet er fuldført, kan du vende fasen til **Fuldført**. Når projektfasen er angivet til Fuldført, er det underforstået, at arbejdet er 100 % færdigt, men at projektet holdes åbent for alle ventende tids- eller udgiftsposteringer, der skal registreres.                     |
|  **Luk**   |           Når alle transaktioner er blevet registreret på projektet, og du ikke forventer at logge mere, kan du manuelt indstille fasen til **Luk**. Når projektet er indstillet til **Luk**, kan du ikke logge flere posteringer på projektet, og projektet vil være skrivebeskyttet.           |

## <a name="to-track-a-projects-status"></a>Sådan spores et projekts status  

1.  Gå til **Project Service > Projekter**.  

2.  Klik på det projekt, som du vil arbejde på.  

3.  Vælg pil ned ud for projektnavnet på linjen øverst på skærmen, og klik derefter på **Projektsporing**.  

4.  Vælg **Indsatssporing** eller **Omkostningssporing** på rullelisten over opgavelisten.  

5.  Dobbeltklik på en opgave for at redigere den. Du kan også flytte eller tilpasse størrelsen på søjlerne i Gantt-diagrammet for at ændre klokkeslæt og status for en opgave.  

### <a name="see-also"></a>Se også  
 [Vejledning til projektledere](../project-service/project-manager-guide.md)
