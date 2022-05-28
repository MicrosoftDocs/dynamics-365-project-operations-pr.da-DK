---
title: Administrere projekter og reservationer i din Office 365-kalender
description: Sådan administreres projekter og reservationer i din Office 365-kalender
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
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cf51333179d2d972af84de7adb4b718b6e17d038
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598895"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Administrere projekter og reservationer i din kalender (Project Service)

> [!Note]
> UDFASET: Denne funktion er blevet udfaset og er ikke længere tilgængelig.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Få vist private aftaler, reservationer til projektarbejde og tildelinger af arbejdsordrer til teknisk service ved hjælp af [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.  
  
 Med alt på ét sted er det nemt at administrere din dag. Dine møder, aftaler, reservationer og opgaver er alle tilgængelige i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.  
  
 Hvis du bruger [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], du kan også angive dine personlige aftaler i Project Service-tidsregistreringsvisningen. På denne måde kan projekt- og ressourceledere se din tilgængelighed for projekter. Du sparer også tid, fordi du ikke behøver at indtaste oplysninger om dine personlige aftaler to gange. Du kan blot importere dine private aftaler fra din kalender til Project Service-tidsregistreringsvisningen.  
  
 Kalenderen synkroniserer projekt- og arbejdsordrereservationer fra dags dato og fire uger frem. Denne indstilling kan ikke ændres.  
  
 Synkronisering understøttes kun én vej, fra PSA til din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender. Du kan synkronisere i den omvendte rækkefølge. 
  
 Hvis du vil lære at bruge din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, skal du se under [Kalender i Outlook på internettet til forretningsbrug](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Installation  
 Før du kan få vist og administrere dine reservationer i din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, skal du konfigurere et par ting.  
  
- Du skal have legitimationsoplysninger som [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-organisationsadministrator eller -systemadministrator.  
  
- Din administrator skal konfigurere mailserverprofilen, og de enkelte brugere skal konfigurere deres postkasse. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Opsæt mailbehandling via synkronisering på serversiden](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Slå synkronisering til for din organisationen (administratoropgave)  
  
1.  Fra hovedmenuen skal du klikke på **Indstillinger** > **Administration**.  
  
2.  Klik på **Systemindstillinger**.  
  
3.  Klik på fanen **Synkronisering**.  
  
4.  Under **Vælg, om synkronisering af ressourcereservationer med** skal du markere **Synkroniser ressourcereservation med Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Slå synkronisering for din brugerprofil til (brugeropgave)  
  
1.  Klik på knappen **Indstillinger** i det øverste højre hjørne af skærmen.  
  
2.  Klik på **Indstillinger**.  
  
3.  Klik på fanen **Synkronisering**.  
  
4.  Under **Synkronisering af ressourcereservation med Outlook** skal du markere **Synkroniser ressourcereservation med Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importere dine private aftaler (brugeropgave)  
 Du kan importere dine private aftaler fra din kalender til Project Service Automation-tidsregistreringsvisningen.  
  
1. Åbn [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen, og klik på **Importér data**.  
  
2. I vinduet Filtre skal du vælge **Aftaler fra Exchange** og derefter klikke på **Anvend**.  
  
3. Systemet vil trække aftaler til tidsregistreringsvisningen som foreslåede poster fra den aktuelle uge. Hvis du vil tilføje poster for en anden uge, skal du klikke på **Forrige** eller **Næste**.  
  
4. Vælg den aftale, du vil føje til Project Service Automation-tidsregistreringsvisningen.  
  
5. I pop op-feltet **Tidsregistrering** skal du vælge de relevante indstillinger for at konvertere aftalen til en Project Service Automation-tidsregistreringsvisning.  
  
6. Klik på **Gem**.  
  
### <a name="see-also"></a>Se også  
 [Tids-, udgifts- og samarbejdsvejledning](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
