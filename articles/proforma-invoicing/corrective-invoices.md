---
title: Rettede fakturaer
description: Dette emne indeholder oplysninger om rettede fakturaer.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898074"
---
# <a name="corrected-invoices"></a><span data-ttu-id="c2046-103">Rettede fakturaer</span><span class="sxs-lookup"><span data-stu-id="c2046-103">Corrected invoices</span></span>

<span data-ttu-id="c2046-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c2046-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c2046-105">Bekræftede fakturaer kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="c2046-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="c2046-106">Når en rediger en bekræftet faktura, oprettes der en ny kladde for den rettede faktura.</span><span class="sxs-lookup"><span data-stu-id="c2046-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="c2046-107">Da det er en forudsætning, at du vil tilbageføre alle transaktioner og antal fra den oprindelige faktura, inkluderer denne rettede faktura alle transaktioner fra den oprindelige faktura, og alle antal på fakturaen angives til nul (0).</span><span class="sxs-lookup"><span data-stu-id="c2046-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="c2046-108">Når der ikke skal rettes i nogen transaktioner, kan du fjerne dem fra rettelsesfakturakladden.</span><span class="sxs-lookup"><span data-stu-id="c2046-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="c2046-109">Hvis du vil tilbageføre eller returnere en delmængde, kan du redigere feltet Antal i linjedetaljen.</span><span class="sxs-lookup"><span data-stu-id="c2046-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="c2046-110">Hvis du åbner fakturalinjedetaljen, kan du se det oprindelige fakturaantal.</span><span class="sxs-lookup"><span data-stu-id="c2046-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="c2046-111">Du kan derefter redigere det aktuelle fakturaantal, så det er mindre eller større end det oprindelige fakturaantal.</span><span class="sxs-lookup"><span data-stu-id="c2046-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="c2046-112">Når du bekræfter en rettelsesfaktura, tilbageføres det oprindeligt fakturerede salgstal, og der oprettes et nyt faktureret faktisk salgstal.</span><span class="sxs-lookup"><span data-stu-id="c2046-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="c2046-113">Hvis mængden blev reduceret, medfører differencen, at der også oprettes et nyt ikke-faktureret faktisk salgstal.</span><span class="sxs-lookup"><span data-stu-id="c2046-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="c2046-114">Hvis det oprindelige fakturerede salg f.eks. var otte timer, og linjedetaljen i den rettede faktura har et reduceret antal på seks timer, tilbageføres den oprindeligt fakturerede salgslinje, og der oprettes to nye faktiske salgstal:</span><span class="sxs-lookup"><span data-stu-id="c2046-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="c2046-115">Et faktureret faktisk salgstal for seks timer.</span><span class="sxs-lookup"><span data-stu-id="c2046-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="c2046-116">Et ikke-faktureret faktisk salgstal for de resterende to timer.</span><span class="sxs-lookup"><span data-stu-id="c2046-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="c2046-117">Denne transaktion kan enten faktureres senere eller markeres som ikke-fakturerbar, afhængigt af forhandlingerne med kunden.</span><span class="sxs-lookup"><span data-stu-id="c2046-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
