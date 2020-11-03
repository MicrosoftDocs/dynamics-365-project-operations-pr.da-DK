---
title: Konfigurer regnskab for interne projekter
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer regnskabspraksis for interne projekter i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074106"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="df1cb-103">Konfigurer regnskab for interne projekter</span><span class="sxs-lookup"><span data-stu-id="df1cb-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="df1cb-104">_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_</span><span class="sxs-lookup"><span data-stu-id="df1cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="df1cb-105">Interne projekter gør det muligt for virksomheder at spore omkostninger i forbindelse med aktiviteter, der ikke faktureres til en kunde.</span><span class="sxs-lookup"><span data-stu-id="df1cb-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="df1cb-106">Som eksempel på interne projekter kan nævnes:</span><span class="sxs-lookup"><span data-stu-id="df1cb-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="df1cb-107">Udvikling af et produkt, f.eks. en mobilapp, og sporing af de omkostninger, der er forbundet med udviklingen.</span><span class="sxs-lookup"><span data-stu-id="df1cb-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="df1cb-108">Administrering af tid og omkostninger før salg.</span><span class="sxs-lookup"><span data-stu-id="df1cb-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="df1cb-109">Dette interne før salgsprojekt kan senere konverteres til et fakturerbart projekt, hvis tilbuddet bliver vundet.</span><span class="sxs-lookup"><span data-stu-id="df1cb-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="df1cb-110">Alle projekter, der ikke er knyttet til en kontrakt i Dynamics 365 Project Operations, behandles som interne.</span><span class="sxs-lookup"><span data-stu-id="df1cb-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="df1cb-111">Projektomkostnings- og indtægtsprofiler anvendes ikke til at fastsætte regnskabsreglerne for projektet.</span><span class="sxs-lookup"><span data-stu-id="df1cb-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="df1cb-112">Interne projektomkostninger bogføres altid ved hjælp af driftsprincipper.</span><span class="sxs-lookup"><span data-stu-id="df1cb-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="df1cb-113">Hovedbogskonti til bogføring defineres på siden **Opsætning af bogføring i hovedbog**.</span><span class="sxs-lookup"><span data-stu-id="df1cb-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="df1cb-114">Tidstransaktioner bogføres ved at debitere kontoen **Omkostning** og kreditere kontoen **Lønfordeling**.</span><span class="sxs-lookup"><span data-stu-id="df1cb-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="df1cb-115">Udgiftstransaktioner bogføres ved at debitere kontoen **Omkostning** og kreditere kontoen **Modkontoen for udgifter**.</span><span class="sxs-lookup"><span data-stu-id="df1cb-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="df1cb-116">Hvis projektet er knyttet til en projektkontrakt, tilbageføres alle akkumulerede transaktioner automatisk, når der er bogført transaktioner, og der oprettes nye fakturerbare transaktioner i systemet.</span><span class="sxs-lookup"><span data-stu-id="df1cb-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="df1cb-117">De fakturerbare transaktioner følger de regnskabsregler, der er defineret i de respektive udgifts- og indtægtsprofiler for projektet.</span><span class="sxs-lookup"><span data-stu-id="df1cb-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


