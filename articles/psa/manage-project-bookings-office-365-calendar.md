---
title: Administrere projekter og reservationer i din Office 365-kalender
description: Sådan administreres projekter og reservationer i din Office 365-kalender
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: fd4119693875fb851c7bd3f34287db7d81237140
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074206"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="17df5-103">Administrere projekter og reservationer i din kalender (Project Service)</span><span class="sxs-lookup"><span data-stu-id="17df5-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="17df5-104">UDFASET: Denne funktion er blevet udfaset og er ikke længere tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="17df5-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="17df5-105">Få vist private aftaler, reservationer til projektarbejde og tildelinger af arbejdsordrer til teknisk service ved hjælp af [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.</span><span class="sxs-lookup"><span data-stu-id="17df5-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="17df5-106">Med alt på ét sted er det nemt at administrere din dag.</span><span class="sxs-lookup"><span data-stu-id="17df5-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="17df5-107">Dine møder, aftaler, reservationer og opgaver er alle tilgængelige i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.</span><span class="sxs-lookup"><span data-stu-id="17df5-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="17df5-108">Hvis du bruger [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], du kan også angive dine personlige aftaler i Project Service-tidsregistreringsvisningen.</span><span class="sxs-lookup"><span data-stu-id="17df5-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="17df5-109">På denne måde kan projekt- og ressourceledere se din tilgængelighed for projekter.</span><span class="sxs-lookup"><span data-stu-id="17df5-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="17df5-110">Du sparer også tid, fordi du ikke behøver at indtaste oplysninger om dine personlige aftaler to gange.</span><span class="sxs-lookup"><span data-stu-id="17df5-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="17df5-111">Du kan blot importere dine private aftaler fra din kalender til Project Service-tidsregistreringsvisningen.</span><span class="sxs-lookup"><span data-stu-id="17df5-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="17df5-112">Kalenderen synkroniserer projekt- og arbejdsordrereservationer fra dags dato og fire uger frem.</span><span class="sxs-lookup"><span data-stu-id="17df5-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="17df5-113">Denne indstilling kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="17df5-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="17df5-114">Synkronisering understøttes kun én vej, fra PSA til din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender.</span><span class="sxs-lookup"><span data-stu-id="17df5-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="17df5-115">Du kan synkronisere i den omvendte rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="17df5-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="17df5-116">Hvis du vil lære at bruge din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, skal du se under [Kalender i Outlook på internettet til forretningsbrug](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span><span class="sxs-lookup"><span data-stu-id="17df5-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="17df5-117">Installation</span><span class="sxs-lookup"><span data-stu-id="17df5-117">Setup</span></span>  
 <span data-ttu-id="17df5-118">Før du kan få vist og administrere dine reservationer i din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, skal du konfigurere et par ting.</span><span class="sxs-lookup"><span data-stu-id="17df5-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="17df5-119">Du skal have legitimationsoplysninger som [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-organisationsadministrator eller -systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="17df5-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="17df5-120">Din administrator skal konfigurere mailserverprofilen, og de enkelte brugere skal konfigurere deres postkasse.</span><span class="sxs-lookup"><span data-stu-id="17df5-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="17df5-121">[Opsæt mailbehandling via synkronisering på serversiden](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="17df5-121">[Set up email processing through server-side synchronization](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="17df5-122">Slå synkronisering til for din organisationen (administratoropgave)</span><span class="sxs-lookup"><span data-stu-id="17df5-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="17df5-123">Fra hovedmenuen skal du klikke på **Indstillinger** > **Administration**.</span><span class="sxs-lookup"><span data-stu-id="17df5-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="17df5-124">Klik på **Systemindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="17df5-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="17df5-125">Klik på fanen **Synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="17df5-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="17df5-126">Under **Vælg, om synkronisering af ressourcereservationer med** skal du markere **Synkroniser ressourcereservation med Outlook**.</span><span class="sxs-lookup"><span data-stu-id="17df5-126">Under **Select whether to enable syncing of resource booking with** , check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="17df5-127">Slå synkronisering for din brugerprofil til (brugeropgave)</span><span class="sxs-lookup"><span data-stu-id="17df5-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="17df5-128">Klik på knappen **Indstillinger** i det øverste højre hjørne af skærmen.</span><span class="sxs-lookup"><span data-stu-id="17df5-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="17df5-129">Klik på **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="17df5-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="17df5-130">Klik på fanen **Synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="17df5-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="17df5-131">Under **Synkronisering af ressourcereservation med Outlook** skal du markere **Synkroniser ressourcereservation med Outlook**.</span><span class="sxs-lookup"><span data-stu-id="17df5-131">Under **Resource booking sync with Outlook** , check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="17df5-132">Importere dine private aftaler (brugeropgave)</span><span class="sxs-lookup"><span data-stu-id="17df5-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="17df5-133">Du kan importere dine private aftaler fra din kalender til Project Service Automation-tidsregistreringsvisningen.</span><span class="sxs-lookup"><span data-stu-id="17df5-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="17df5-134">Åbn [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen, og klik på **Importér data**.</span><span class="sxs-lookup"><span data-stu-id="17df5-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="17df5-135">I vinduet Filtre skal du vælge **Aftaler fra Exchange** og derefter klikke på **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="17df5-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="17df5-136">Systemet vil trække aftaler til tidsregistreringsvisningen som foreslåede poster fra den aktuelle uge.</span><span class="sxs-lookup"><span data-stu-id="17df5-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="17df5-137">Hvis du vil tilføje poster for en anden uge, skal du klikke på **Forrige** eller **Næste**.</span><span class="sxs-lookup"><span data-stu-id="17df5-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="17df5-138">Vælg den aftale, du vil føje til Project Service Automation-tidsregistreringsvisningen.</span><span class="sxs-lookup"><span data-stu-id="17df5-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="17df5-139">I pop op-feltet **Tidsregistrering** skal du vælge de relevante indstillinger for at konvertere aftalen til en Project Service Automation-tidsregistreringsvisning.</span><span class="sxs-lookup"><span data-stu-id="17df5-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="17df5-140">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="17df5-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="17df5-141">Se også</span><span class="sxs-lookup"><span data-stu-id="17df5-141">See Also</span></span>  
 [<span data-ttu-id="17df5-142">Tids-, udgifts- og samarbejdsvejledning</span><span class="sxs-lookup"><span data-stu-id="17df5-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)