---
title: Udgiftsoversigt
description: Dette emne indeholder informationer om udgiftsfunktionen i Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074052"
---
# <a name="expense-home-page"></a><span data-ttu-id="d16f1-103">Startsiden for udgift</span><span class="sxs-lookup"><span data-stu-id="d16f1-103">Expense home page</span></span>

<span data-ttu-id="d16f1-104">_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d16f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d16f1-105">Dynamics 365 Project Operations understøtter muligheden for at behandle udgifter.</span><span class="sxs-lookup"><span data-stu-id="d16f1-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="d16f1-106">Udgiftsbehandling udføres sammen med eller uden projekter ved hjælp af en tilpasset arbejdsproces med politikker, transaktionskategorier og godkendelser.</span><span class="sxs-lookup"><span data-stu-id="d16f1-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="d16f1-107">I Project Operations findes der to understøttede udrulningsmodeller for udgifter:</span><span class="sxs-lookup"><span data-stu-id="d16f1-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="d16f1-108">**Fuld** : Fuld udrulning er tilgængelig for **Project Operations for ressource-/ikke-lagerbaserede scenarier** eller **Project Operations for produktionsordrebaserede scenarier**.</span><span class="sxs-lookup"><span data-stu-id="d16f1-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="d16f1-109">**Grundlæggende** : Grundlæggende udrulning er tilgængelig for **Project Operations for ressource-/ikke-lagerbaserede scenarier** og **Let udrulning – aftale om proformafakturering**.</span><span class="sxs-lookup"><span data-stu-id="d16f1-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="d16f1-110">Komplet</span><span class="sxs-lookup"><span data-stu-id="d16f1-110">Full</span></span> 
<span data-ttu-id="d16f1-111">Fuld udgiftsudrulning giver en komplet politikhåndhævelse, der omfatter muligheden for at oprette politikker, såsom:</span><span class="sxs-lookup"><span data-stu-id="d16f1-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="d16f1-112">Grænser for udgiftskategorier</span><span class="sxs-lookup"><span data-stu-id="d16f1-112">Expense category limits</span></span>
  - <span data-ttu-id="d16f1-113">Rejse</span><span class="sxs-lookup"><span data-stu-id="d16f1-113">Travel</span></span>
  - <span data-ttu-id="d16f1-114">Pr. dag</span><span class="sxs-lookup"><span data-stu-id="d16f1-114">Per diem</span></span>
  - <span data-ttu-id="d16f1-115">Import af nyt kreditkort</span><span class="sxs-lookup"><span data-stu-id="d16f1-115">Credit card imports</span></span>
  - <span data-ttu-id="d16f1-116">Kvittering for optisk tegngenkendelse</span><span class="sxs-lookup"><span data-stu-id="d16f1-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="d16f1-117">Basis</span><span class="sxs-lookup"><span data-stu-id="d16f1-117">Basic</span></span> 
<span data-ttu-id="d16f1-118">Med grundlæggende udrulningsscenariet kan du kun registrere grundlæggende udgifter i forhold til et projekt.</span><span class="sxs-lookup"><span data-stu-id="d16f1-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="d16f1-119">Du kan finde flere oplysninger i [Udgiftsregistrering (lille)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="d16f1-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="d16f1-120">Vælg din udgiftsudrulning</span><span class="sxs-lookup"><span data-stu-id="d16f1-120">Determine your Expense deployment</span></span>
<span data-ttu-id="d16f1-121">Du kan finde ud af, om du kører den grundlæggende udrulning af udgiftsstyring, ved at verificere, at URL-adressen slutter med **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="d16f1-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
