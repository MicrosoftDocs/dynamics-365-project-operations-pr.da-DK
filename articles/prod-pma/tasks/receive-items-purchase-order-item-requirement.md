---
title: Modtag varer på indkøbsordre fra varebehov
description: I dette emne forklares, hvordan du modtager varer på en indkøbsordre fra et varebehov.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011679"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]