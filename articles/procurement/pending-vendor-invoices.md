---
title: Køb ikke-lagerførte materialer ved hjælp af en afventende leverandørfaktura
description: I dette emne forklares det, hvordan afventende leverandørfakturaer registreres.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993778"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="e92ff-103">Køb ikke-lagerførte materialer ved hjælp af en afventende leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="e92ff-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="e92ff-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="e92ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e92ff-105">Når en virksomhed anskaffer ikke-lagerførte materialer til et projekt, kan omkostningerne straks registreres i forhold til projektet.</span><span class="sxs-lookup"><span data-stu-id="e92ff-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="e92ff-106">Som eksempel kan nævnes Contoso Robotics US, der udfører et udstyrsfornyelsesprojekt og har brug for softwarelicenser.</span><span class="sxs-lookup"><span data-stu-id="e92ff-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="e92ff-107">Disse licenser indkøbes fra en tredjepartsleverandør.</span><span class="sxs-lookup"><span data-stu-id="e92ff-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="e92ff-108">Ved hjælp af Dynamics 365 Finance kan kreditormedarbejderen registrere et afventende fakturadokument for leverandøren, og tildele licensomkostningerne direkte på udstyrsfornyelsesprojektet.</span><span class="sxs-lookup"><span data-stu-id="e92ff-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e92ff-109">Før du bruger den funktion, der er beskrevet i dette emne, skal du gennemse og anvende de påkrævede konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e92ff-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="e92ff-110">Du kan finde flere oplysninger i [Aktiver ikke-lagerførte materialer og afventende leverandørfakturaer](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="e92ff-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="e92ff-111">Bogfør en projektrelateret afventende leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="e92ff-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="e92ff-112">Afventende leverandørfakturaer kan registreres på siden **Afventende leverandørfakturaer** (**Kreditor** > **Fakturaer** > **Afventende leverandørfakturaer**).</span><span class="sxs-lookup"><span data-stu-id="e92ff-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="e92ff-113">Udfør følgende trin for at bogføre en projektrelateret afventende leverandørfaktura:</span><span class="sxs-lookup"><span data-stu-id="e92ff-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="e92ff-114">Gå til **Kreditor** > **Fakturaer**, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e92ff-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="e92ff-115">I feltet **Fakturakonto** skal du vælge en leverandør, og i feltet **Nummer** skal du angive leverandørens fakturaidentifikation.</span><span class="sxs-lookup"><span data-stu-id="e92ff-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="e92ff-116">Tilføj en linje til leverandørens faktura, og vælg i feltet **Varenummer** den ikke-lagerførte vare, der er købt hos leverandøren.</span><span class="sxs-lookup"><span data-stu-id="e92ff-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e92ff-117">Leverandørfakturalinjer, der er baseret på en indkøbskategori, kan ikke registreres i forhold til projektet.</span><span class="sxs-lookup"><span data-stu-id="e92ff-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="e92ff-118">Tilføj det købte antal.</span><span class="sxs-lookup"><span data-stu-id="e92ff-118">Add the quantity purchased.</span></span> <span data-ttu-id="e92ff-119">Enhedsprisen udfyldes automatisk af systemet på basis af den ikke-lagerførte varepriskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e92ff-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="e92ff-120">Kontrollér det samlede beløb og andre påkrævede oplysninger på linjen.</span><span class="sxs-lookup"><span data-stu-id="e92ff-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="e92ff-121">På linjedetaljerne skal du på fanen **Projekt** vælge det projekt-id, som denne vare vil blive registreret på.</span><span class="sxs-lookup"><span data-stu-id="e92ff-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="e92ff-122">Du kan også vælge aktivitetsnummeret og opdatere projektkategorien og linjeegenskaben.</span><span class="sxs-lookup"><span data-stu-id="e92ff-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="e92ff-123">Bogfør afventende leverandørfakturaer.</span><span class="sxs-lookup"><span data-stu-id="e92ff-123">Post pending vendor invoice.</span></span> <span data-ttu-id="e92ff-124">Når fakturaen er bogført, registrerer systemet følgende:</span><span class="sxs-lookup"><span data-stu-id="e92ff-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="e92ff-125">Leverandørens saldobeløb.</span><span class="sxs-lookup"><span data-stu-id="e92ff-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="e92ff-126">Momsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="e92ff-126">The sales tax amount.</span></span>
    - <span data-ttu-id="e92ff-127">Omkostningen i forhold til projektet registreres for indkøbsintegrationskontoen.</span><span class="sxs-lookup"><span data-stu-id="e92ff-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="e92ff-128">Den faktiske projekttransaktion i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e92ff-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="e92ff-129">Transaktionen behandles yderligere ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="e92ff-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="e92ff-130">Når du bogfører denne kladde, flyttes beløbet fra indkøbsintegrationskontoen til projektomkostningskontoen.</span><span class="sxs-lookup"><span data-stu-id="e92ff-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
