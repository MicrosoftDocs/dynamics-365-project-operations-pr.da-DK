---
title: Oversigt over intern fakturering
description: Dette emne indeholder oplysninger om og eksempler på intern fakturering for projekter.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369369"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="2864f-103">Oversigt over intern fakturering</span><span class="sxs-lookup"><span data-stu-id="2864f-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="2864f-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="2864f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2864f-105">Din organisation kan have flere afdelinger, datterselskaber og andre juridiske enheder, som overfører produkter og tjenester til hinanden i forbindelse med projekter.</span><span class="sxs-lookup"><span data-stu-id="2864f-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="2864f-106">Den juridiske enhed, der leverer servicen eller produktet, kaldes *den juridiske udlånsenhed*.</span><span class="sxs-lookup"><span data-stu-id="2864f-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="2864f-107">Den juridiske enhed, der modtager servicen eller produktet, kaldes *den juridiske låneenhed*.</span><span class="sxs-lookup"><span data-stu-id="2864f-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="2864f-108">I følgende illustration vises et typisk scenario, hvor to juridiske enheder, Contoso Robotics USA (den låntagende juridiske enhed) og Contoso Robotics UK (den udlånende juridiske enhed) deler ressourcer med henblik på at levere et projekt til kunden, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="2864f-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="2864f-109">I dette scenario får Contoso Robotics USA til opgave at levere arbejdet til Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="2864f-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Intern fakturering](./media/IntercompanyScenario.png) 

<span data-ttu-id="2864f-111">Dynamics 365 Project Operations bruger følgende flow til at behandle interne transaktioner:</span><span class="sxs-lookup"><span data-stu-id="2864f-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="2864f-112">Ressourcer fra den juridiske udlånsenhedspost for interne tids- eller udgiftstransaktioner ved at reservere tid og udgifter mod projekter i den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="2864f-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="2864f-113">Omkostninger til tid og udgifter registreres i udlånsvirksomheden ved hjælp af det låntagende selskabs liste med enhedskostpris.</span><span class="sxs-lookup"><span data-stu-id="2864f-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="2864f-114">Ikke-fakturerede interne salgstransaktioenr registreres i det långivende selskab ved hjælp af det låntagende selskabs liste med enhedskostpris.</span><span class="sxs-lookup"><span data-stu-id="2864f-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="2864f-115">Ikke-faktureret omsætning registreres i det låntagende selskab ved hjælp af projektkontraktens salgsprisliste.</span><span class="sxs-lookup"><span data-stu-id="2864f-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="2864f-116">Kunden kan faktureres, når der registreres ikke-faktureret omsætning.</span><span class="sxs-lookup"><span data-stu-id="2864f-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="2864f-117">Kunden behøver ikke at vente til behandlingen af den interne faktura er fuldført.</span><span class="sxs-lookup"><span data-stu-id="2864f-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="2864f-118">Interne kundefakturaer oprettes periodisk i det långivende selskab.</span><span class="sxs-lookup"><span data-stu-id="2864f-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="2864f-119">Fakturaerne oprettes manuelt eller ved hjælp af en periodisk automatiseret proces.</span><span class="sxs-lookup"><span data-stu-id="2864f-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="2864f-120">Der kan oprettes en enkelt faktura for hver juridisk låneenhed, eller der kan oprettes separate fakturaer på hvert projekt.</span><span class="sxs-lookup"><span data-stu-id="2864f-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="2864f-121">Når den juridiske udlånsenhed bogfører den interne kundefaktura, oprettes den tilsvarende afventende leverandørfaktura i den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="2864f-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="2864f-122">Omkostningerne i den afventende leverandørfaktura registreres på projektets underfinanskonto, når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="2864f-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="2864f-123">I følgende diagram illustreres den interne fakturering i sin sammenhæng med regnskabshændelser og de forventede posteringer i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="2864f-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Internt flow](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="2864f-125">Flere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2864f-125">Additional resources</span></span>

- [<span data-ttu-id="2864f-126">Konfigurer intern fakturering</span><span class="sxs-lookup"><span data-stu-id="2864f-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="2864f-127">Registrer interne transaktioner</span><span class="sxs-lookup"><span data-stu-id="2864f-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="2864f-128">Opret interne kunde- og kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="2864f-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]