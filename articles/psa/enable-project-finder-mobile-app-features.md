---
title: Aktivere funktionerne i Project Finder Mobile-appen
description: Sådan aktiverer du funktionerne i Project Finder Mobile-appen til Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132956"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Aktivér funktionerne i Project Finder Mobile-appen (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Dine ressourcer kan bruge Project Finder Mobile-appen på deres telefon med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til at finde nye projekter til at arbejde med og opdatere deres færdigheder.  
  
 Appen er tilgængelig til [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner og [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Du skal angive nogle indstillinger i parameterindstillingerne for din afdeling for at tillade brugere at få vist projektets ressourcekrav og opdatere deres viden.  
  
> [!NOTE]
>  Project Finder Mobile-appen fungerer kun sammen med [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] (ikke med lokale installationer).  
  
1. Gå til **Project Service > Parametre**.  
  
2. Klik på de parameterindstillinger, du vil bruge til at tillade Project Finder Mobile-appens funktioner.  
  
3. I området **Generelt** skal du sætte **Ressourcekrav, som er synlige for ressourcer** til **Ja**.  
  
4. Sæt **Tillad, at ressourcen opdaterer sine færdigheder** til **Ja**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Dette er en global indstilling. Projektledere kan angive, om et enkelt projekt kan ses på det pågældende projekts **projektteam**-side.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Mailmeddelelser  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sender mails om ressourceanmodninger til følgende modtagere på følgende tidspunkter:  
  
|Modtager|Hændelse|  
|---------------|-----------|  
|Projektleder|- Når en ressource tilmelder sig et projekt med Project Finder Mobile-appen.|  
|Ressource|- Når projektarbejdet, ressourcen har tilmeldt sig, allerede er udfyldt af en anden ressource.<br />- Når deres anmodning om godkendelse af færdigheden er godkendt eller afvist.<br />- Når deres anmodning om tilmelding til projekt er godkendt eller afvist.|  
  
## <a name="privacy-notice"></a>Meddelelse om beskyttelse af personlige oplysninger  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Se også  
 [Konfigurere ressourcer](../psa/set-up-resources.md)
