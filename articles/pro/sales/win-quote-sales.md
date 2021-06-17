---
title: Luk et tilbud - lille
description: Dette emne indeholder oplysninger om, hvordan du lukker et tilbud i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994129"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="84496-103">Luk et tilbud - lille</span><span class="sxs-lookup"><span data-stu-id="84496-103">Close a quote - lite</span></span>

<span data-ttu-id="84496-104">_**Gælder for:** Lille udrulning - aftale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="84496-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84496-105">Et projekttilbud kan lukkes som vundet eller tabt.</span><span class="sxs-lookup"><span data-stu-id="84496-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="84496-106">Et kladdetilbud kan lukkes, fordi handlingerne Aktivér og Revider på tilbud ikke understøttes i Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="84496-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="84496-107">Luk et tilbud som vundet</span><span class="sxs-lookup"><span data-stu-id="84496-107">Close a quote as Won</span></span>

<span data-ttu-id="84496-108">Når du lukker et projekttilbud som Vundet, angives status til Lukket, og statusårsagen er Vundet.</span><span class="sxs-lookup"><span data-stu-id="84496-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="84496-109">Når du lukker tilbuddet, skrivebeskyttes projektilbuddene, og der oprettes en kladde med et udkast til projektkontrakt med tilbudsoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="84496-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="84496-110">Da et lukket tilbud ikke kan åbnes igen, bekræfter en bekræftelsesdialog dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="84496-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="84496-111">Hvis tilbuddet er knyttet til en salgsmulighed, lukkes eventuelle andre projekttilbud på salgsmuligheden automatisk som tabt.</span><span class="sxs-lookup"><span data-stu-id="84496-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="84496-112">Økonomiske konsekvenser af at lukke et tilbud som vundet</span><span class="sxs-lookup"><span data-stu-id="84496-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="84496-113">Hvis der er faktiske oplysninger om tid på et projekt, mens der stadig er tilknyttet et kladdetilbud, registreres kun omkostningerne ved tid eller udgifter.</span><span class="sxs-lookup"><span data-stu-id="84496-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="84496-114">Når et tilbud er lukket som vundet, vil programmet omstrukturere omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger.</span><span class="sxs-lookup"><span data-stu-id="84496-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="84496-115">Programmet behandler de faktiske omkostninger baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="84496-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="84496-116">Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, oprettes der tilsvarende ikke-fakturerede faktiske salgsværdier for, hvornår tilbuddet lukkes, og projektkontrakten oprettes.</span><span class="sxs-lookup"><span data-stu-id="84496-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="84496-117">Hvis de faktiske omkostninger refererer til en fastpriskontraktlinje, stopper programmet med at genbehandle de faktiske omkostninger, der er baseret på de opdelte faktureringsregler for projektkontraktkunderne.</span><span class="sxs-lookup"><span data-stu-id="84496-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="84496-118">Lukning af et tilbud som tabt:</span><span class="sxs-lookup"><span data-stu-id="84496-118">Closing a quote as lost:</span></span>

<span data-ttu-id="84496-119">Når du lukker et projekttilbud som Tabt, angives status til Lukket, og statusårsagen er Tabt.</span><span class="sxs-lookup"><span data-stu-id="84496-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="84496-120">Hvis du lukker tilbuddet, bliver projekttilbuddet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="84496-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="84496-121">Da et lukket tilbud ikke kan genåbnes, før du lukker et tilbud, vil en bekræftelsesdialogboks bekræfte ændringerne.</span><span class="sxs-lookup"><span data-stu-id="84496-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="84496-122">Hvis det projekttilbud, der er lukket som Tabt, refererer til et projekt på en af dets linjer, markeres projektet også som Lukket.</span><span class="sxs-lookup"><span data-stu-id="84496-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="84496-123">De ressourcereservationer, der er gældende fra den pågældende dag og fremefter, annulleres.</span><span class="sxs-lookup"><span data-stu-id="84496-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="84496-124">Hvis du lukker et tilbud som vundet eller tabt i Project Operations, påvirkes statussen for salgsmuligheden ikke, og den vil være åben, indtil den lukkes manuelt.</span><span class="sxs-lookup"><span data-stu-id="84496-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]