---
title: Luk et tilbud - lille
description: Dette emne indeholder oplysninger om, hvordan du lukker et tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175704"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="5d327-103">Luk et tilbud - lille</span><span class="sxs-lookup"><span data-stu-id="5d327-103">Close a quote - lite</span></span>

<span data-ttu-id="5d327-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5d327-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5d327-105">Et projekttilbud kan lukkes som vundet eller tabt.</span><span class="sxs-lookup"><span data-stu-id="5d327-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="5d327-106">Operationerne Aktivér og Revider på tilbud understøttes ikke i Microsoft Dynamics 365 Project Operations, hvorfor et tilbud i kladdeform kan lukkes.</span><span class="sxs-lookup"><span data-stu-id="5d327-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="5d327-107">Luk et tilbud som vundet</span><span class="sxs-lookup"><span data-stu-id="5d327-107">Close a quote as Won</span></span>

<span data-ttu-id="5d327-108">Hvis du lukker et projekttilbud som vundet, lukkes tilbuddet med statussen Lukket, og statusårsagen angives til Vundet.</span><span class="sxs-lookup"><span data-stu-id="5d327-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="5d327-109">Når du lukker tilbuddet, skrivebeskyttes projektilbuddene, og der oprettes en kladde med et udkast til projektkontrakt med tilbudsoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="5d327-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="5d327-110">Da et lukket tilbud ikke kan genåbnes, vises der en bekræftelsesdialogboks i dialogboksen, før ændringerne er foretaget, da et lukket tilbud ikke kan åbnes igen, og ændringerne ikke kan fortrydes.</span><span class="sxs-lookup"><span data-stu-id="5d327-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="5d327-111">Hvis tilbuddet er knyttet til en salgsmulighed, lukkes eventuelle andre projekttilbud på salgsmuligheden automatisk som tabt.</span><span class="sxs-lookup"><span data-stu-id="5d327-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="5d327-112">Økonomiske konsekvenser af at lukke et tilbud som vundet</span><span class="sxs-lookup"><span data-stu-id="5d327-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="5d327-113">Hvis der har været faktiske oplysninger for den tid, der er registreret på et projekt, mens det stadig er knyttet til et kladdetilbud, registreres kun omkostningerne for tiden eller udgiften.</span><span class="sxs-lookup"><span data-stu-id="5d327-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="5d327-114">Når et tilbud er lukket som vundet, vil programmet omstrukturere omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5d327-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="5d327-115">Programmet behandler de faktiske omkostninger baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="5d327-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="5d327-116">Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, oprettes der automatisk tilsvarende faktiske ikke-fakturerede salg for tidspunktet, hvor tilbuddet blev lukket, og projektkontrakten oprettes i systemet.</span><span class="sxs-lookup"><span data-stu-id="5d327-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="5d327-117">Hvis der henvises til omkostningerne i forbindelse med en fastpriskontraktlinje, stopper programmet med at genbehandle de faktiske omkostninger på baggrund af reglerne for opdeling af fakturering for projektkontraktkunderne.</span><span class="sxs-lookup"><span data-stu-id="5d327-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="5d327-118">Lukning af et tilbud som tabt:</span><span class="sxs-lookup"><span data-stu-id="5d327-118">Closing a quote as lost:</span></span>

<span data-ttu-id="5d327-119">Hvis du lukker et projekttilbud som tabt, angives status til Lukket, og statusårsag til Tabt.</span><span class="sxs-lookup"><span data-stu-id="5d327-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="5d327-120">Hvis du lukker tilbuddet, bliver projekttilbuddet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="5d327-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="5d327-121">Da et lukket tilbud ikke kan genåbnes, før du lukker et tilbud, vil en bekræftelsesdialogboks bekræfte ændringerne.</span><span class="sxs-lookup"><span data-stu-id="5d327-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="5d327-122">Hvis det projekttilbud, der er lukket som tabt, er et projekt, der refereres til på nogen af sine linjer, er det projekt også markeret som lukket, og eventuelle ressourcereservationer fra den pågældende dag annulleres.</span><span class="sxs-lookup"><span data-stu-id="5d327-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="5d327-123">Hvis du lukker et tilbud som vundet eller tabt i Project Operations, påvirkes statussen for salgsmuligheden ikke, og den vil være åben, indtil den lukkes manuelt.</span><span class="sxs-lookup"><span data-stu-id="5d327-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
