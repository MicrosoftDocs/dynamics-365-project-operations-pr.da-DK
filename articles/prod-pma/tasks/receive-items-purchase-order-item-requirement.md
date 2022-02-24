---
title: Modtag varer på indkøbsordre fra varebehov
description: I dette emne forklares, hvordan du modtager varer på en indkøbsordre fra et varebehov.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074339"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Modtag varer på indkøbsordre fra varebehov

[!include [banner](../../includes/banner.md)]

I dette emne forklares, hvordan du modtager varer på en indkøbsordre fra et varebehov.

Hvis du bruger et varebehov i stedet for en varetransaktion, kan du planlægge leveringen lige før varen faktisk anvendes, oprette en indkøbsordre, inkludere varen i handelsaftalestrukturen og inkludere varebehovet i produktionsplanlægningen. 

Denne opgave anvender datasættet USSI.

1. Gå til **Moduler > Projektstyring og regnskab > Projekter > Alle projekter** i navigationsruden.
2. Vælg linket i den ønskede række på listen.
3. Vælg **Plan** i handlingsruden.
4. Vælg **varebehov**.
5. Vælg **Ny**.
6. Angiv eller vælg en værdi i feltet **Varenummer** i den nye række.
7. Angiv et nummer i feltet **Antal**.
8. Vælg **Gem**.
9. Vælg **Administrer** i handlingsruden.
10. Vælg **Funktioner**.
11. Vælg **Opret en indkøbsordre**.
12. Markér afkrydsningsfeltet **Inkluder alle**.
13. I feltet **Leverandørkonto** skal du angive eller vælge en værdi.
14. Vælg **OK**.
15. Gå til **Moduler > Kreditor > Indkøbsordrer > Alle indkøbsordrer** i navigationsruden.
16. Vælg linket i den ønskede række på listen.
17. Vælg **Køb** i handlingsruden.
18. Vælg **Bekræft**.
19. Vælg **Modtag** i handlingsruden.
20. Vælg **Produktkvittering**.
21. Skriv en værdi i feltet **Produktkvittering**.
22. Vælg **OK**.

