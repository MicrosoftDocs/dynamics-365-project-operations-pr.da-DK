---
title: Aktivere funktionerne i Project Finder Mobile-appen
description: Sådan aktiverer du funktionerne i Project Finder Mobile-appen til Project Service
author: JohnPBurrows
ms.prod: ''
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
ms.openlocfilehash: 8651ba591853faf648587dcbd4c50625ba94360958d7b418e89aa0bf09464a89
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004889"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Aktivér funktionerne i Project Finder Mobile-appen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Dine ressourcer kan bruge Project Finder Mobile-appen på deres telefon med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til at finde nye projekter til at arbejde med og opdatere deres færdigheder.  
  
 Appen er tilgængelig til [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner og [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 For at gøre det muligt for brugere at se kravene til projektressourcer skal valgmuligheder være markerede i parameterindstillinger for din afdeling.
  
> [!NOTE]
>  Project Finder Mobile-appen fungerer kun sammen med [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (ikke med lokale installationer).  
  
1. Gå til **Project Service > Parametre**.  
  
2. Klik på de parameterindstillinger, du vil bruge til at tillade Project Finder Mobile-appens funktioner.  
  
3. I området **Generelt** skal du sætte **Ressourcekrav, som er synlige for ressourcer** til **Ja**.  
  
4. Sæt **Tillad, at ressourcen opdaterer sine færdigheder** til **Ja**.  
  
   ![ProjectService_ProjectFinderEnable.](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Dette er en global indstilling. Projektledere kan angive, om et enkelt projekt kan ses på det pågældende projekts **projektteam**-side.  
  
   ![ProjectService_ProjectTeamVisible.](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Mailmeddelelser  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sender mails om ressourceanmodninger til følgende modtagere på følgende tidspunkter:  
  
|Modtager|Hændelse|  
|---------------|-----------|  
|Projektleder|- En ressource tilmelder sig et projekt med Project Finder Mobile-appen.|  
|Ressource|- Projektarbejdet, som ressourcen har tilmeldt sig, er allerede udfyldt af en anden ressource.<br />- Anmodningen om godkendelse af færdigheden er blevet godkendt eller afvist.<br />- Anmodningen om tilmelding til projektet er blevet godkendt eller afvist.|  
  
## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Se også  
 [Konfigurere ressourcer](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]