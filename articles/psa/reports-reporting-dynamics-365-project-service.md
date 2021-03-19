---
title: Startside for rapportering
description: Dette emne indeholder oplysninger om rapportering i Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 78c62f69c6529669789a461f1ded8e3ea5f8219e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283271"
---
# <a name="reporting-home-page"></a><span data-ttu-id="7c553-103">Startside for rapportering</span><span class="sxs-lookup"><span data-stu-id="7c553-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7c553-104">Microsoft Dynamics 365 Project Service Automation giver projektbaserede organisationer mulighed for effektivt at administrere deres aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="7c553-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="7c553-105">På et hvilket som helst projekt skal teammedlemmerne administrere salgsmuligheden, tilbuddet og planlægge arbejdet, give projekter ressourcer, administrere arbejdet i henhold til planen, fakturere arbejdet og derefter udføre arbejdet for at fuldføre projektet.</span><span class="sxs-lookup"><span data-stu-id="7c553-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="7c553-106">Muligheden for at rapportere om operationer er vigtig for at bestemme organisationens tilstand og udføre eventuelle korrigerende handlinger, der er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="7c553-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="7c553-107">PSA bruger Microsoft Dynamics 365-rapporteringsmetoder og -teknologier til al rapportering.</span><span class="sxs-lookup"><span data-stu-id="7c553-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="7c553-108">Du kan finde flere oplysninger om indstillinger for rapportering i [Vejledning til rapportskrivning i Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="7c553-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="7c553-109">Guiden Rapport</span><span class="sxs-lookup"><span data-stu-id="7c553-109">Report Wizard</span></span>

<span data-ttu-id="7c553-110">I guiden Rapport kan brugere, der ikke er udviklere, oprette simple rapporter.</span><span class="sxs-lookup"><span data-stu-id="7c553-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="7c553-111">Eftersom appen er bygget på en eksisterende platform, er oplevelsen den samme som den oplevelse, der er dokumenteret i [Oprette eller redigere en rapport ved hjælp af guiden Rapport](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="7c553-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="7c553-112">Men du vil bruge de Project Service Automation-specifikke objekter.</span><span class="sxs-lookup"><span data-stu-id="7c553-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="7c553-113">Tilpassede rapporter i SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="7c553-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="7c553-114">Hvis din virksomhed kræver en bestemt rapport, der ikke kan oprettes ved hjælp af guiden Rapport, kan du oprette en brugerdefineret rapport.</span><span class="sxs-lookup"><span data-stu-id="7c553-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="7c553-115">Microsoft Visual Studio skal være installeret sammen med de nødvendige Microsoft SQL Server Data Tools og Report Authoring-udvidelser.</span><span class="sxs-lookup"><span data-stu-id="7c553-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="7c553-116">Du kan finde flere oplysninger om værktøjer og versioner i [Rapportskrivningsmiljø ved hjælp af SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="7c553-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="7c553-117">Du kan finde oplysninger om, hvordan du opretter en brugerdefineret rapport i [Sådan oprettes en ny rapport ved hjælp af SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="7c553-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="7c553-118">Power BI Indsigt-apps</span><span class="sxs-lookup"><span data-stu-id="7c553-118">Power BI insights apps</span></span>

<span data-ttu-id="7c553-119">Kombinationen af Microsoft Power BI og Dynamics 365 giver dig en effektiv måde til at arbejde med dine data på i form af Insight-apps.</span><span class="sxs-lookup"><span data-stu-id="7c553-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="7c553-120">Du finder oplysninger om tilgængeligheden af Insight-apps på siden om [Power BI Insight-apps](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="7c553-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="7c553-121">Flere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7c553-121">Additional resources</span></span>
<span data-ttu-id="7c553-122">Du finder flere oplysninger om rapportering i PSA under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="7c553-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="7c553-123">Arbejde med Project Service-datamodellen</span><span class="sxs-lookup"><span data-stu-id="7c553-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="7c553-124">Dashboards</span><span class="sxs-lookup"><span data-stu-id="7c553-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]