---
title: Bekræft en projektkontrakt
description: Dette emne indeholder oplysninger om, hvordan du bekræfter en kontrakt i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128276"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="76dda-103">Bekræft en projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="76dda-103">Confirm a project contract</span></span>

<span data-ttu-id="76dda-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="76dda-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="76dda-105">En projektkontrakt i Dynamics 365 Project Operations kan være aktiv med en årsag angivet til **Bekræftet** eller være lukket med en årsag angivet til **Tabt**.</span><span class="sxs-lookup"><span data-stu-id="76dda-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="76dda-106">Når du bekræfter en projektkontrakt, opdateres statussen fra **Kladde** til **Aktiv**, og statusårsagen angives til **Bekræftet**.</span><span class="sxs-lookup"><span data-stu-id="76dda-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="76dda-107">En aktiv eller lukket kontrakt kan ikke redigeres eller genåbnes.</span><span class="sxs-lookup"><span data-stu-id="76dda-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="76dda-108">Økonomisk indvirkning af at bekræfte en projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="76dda-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="76dda-109">Når en projektkontrakt er bekræftet, genberegner programmet omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger.</span><span class="sxs-lookup"><span data-stu-id="76dda-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="76dda-110">De nye faktiske omkostninger behandles derefter baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="76dda-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="76dda-111">Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, opretter programmet automatisk tilsvarende ikke-fakturerede faktiske oplysninger for salg.</span><span class="sxs-lookup"><span data-stu-id="76dda-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="76dda-112">Hvis de faktiske omkostninger refererer til en kontraktlinje med fast pris, holder programmet op med at behandle de faktiske omkostninger.</span><span class="sxs-lookup"><span data-stu-id="76dda-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="76dda-113">Grænser, der ikke må overskrides, konfiguration af fakturerbarhed og prisfastsættelse samt omkostningsfastsættelse på de faktiske oplysninger evalueres og opdateres derefter som en del af bekræftelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="76dda-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="76dda-114">Luk en projektkontrakt som tabt</span><span class="sxs-lookup"><span data-stu-id="76dda-114">Close a project contract as lost</span></span>

<span data-ttu-id="76dda-115">Når du lukker en projektkontrakt som tabt, opdateres kontraktstatussen til **Lukket** og statusårsagen til **Tabt**.</span><span class="sxs-lookup"><span data-stu-id="76dda-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="76dda-116">Projektkontrakten bliver skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="76dda-116">The project contract becomes read-only.</span></span> <span data-ttu-id="76dda-117">Der vises en bekræftelsesdialogboks, før ændringerne fuldføres, fordi du ikke kan genåbne en lukket projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="76dda-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="76dda-118">Hvis den projektkontrakt, der lukkes som værende tabt, refererer til et projekt på de enkelte linjer, bliver det pågældende projekt også markeret som lukket.</span><span class="sxs-lookup"><span data-stu-id="76dda-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="76dda-119">De ressourcereservationer, der er gældende fra den pågældende dag og fremefter, annulleres.</span><span class="sxs-lookup"><span data-stu-id="76dda-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="76dda-120">Alle ikke-fakturerede faktiske salgsværdier i projektkontrakten, som ikke allerede er blevet faktureret, tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="76dda-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="76dda-121">I Dynamics 365 Project Operations påvirkes statussen for den tilknyttede salgsmulighed ikke ved, at du lukker et projekt som værende tabt.</span><span class="sxs-lookup"><span data-stu-id="76dda-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="76dda-122">Salgsmuligheden er stadig åben og skal lukkes manuelt.</span><span class="sxs-lookup"><span data-stu-id="76dda-122">The opportunity will remain open and must be manually closed.</span></span>
