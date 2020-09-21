---
title: Konfigurer intern projektfakturering
description: I dette emne beskrives det, hvordan du kan konfigurere projektfakturering mellem to firmaer i din organisation.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750503"
---
# <a name="configure-intercompany-project-invoicing"></a>Konfigurer intern projektfakturering

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives det, hvordan du kan konfigurere projektfakturering mellem to firmaer i din organisation. Denne opgave anvender datasættet USSI.

1. Gå til **Moduler > Kreditor > Leverandører > Alle leverandører** i navigationsruden.
2. På listen **Alle leverandører** skal du finde og vælge den ønskede post.
3. Vælg **Generelt** i handlingsruden.
4. Vælg **Intern**.
5. Angiv **Aktiv** til **Ja** for at aktivere intern handel.
6. I feltet **Kundevirksomhed** skal du angive eller vælge en værdi.
7. I feltet **Min konto** skal du angive eller vælge en værdi.
8. Vælg **Gem**.
9. Luk siderne for at vende tilbage til startsiden.
10. Gå til **Moduler > Projektstyring og regnskab > Opsætning > Projektstyring og regnskabsparametre** i navigationsruden.
11. Vælg fanen **Intern**.
12. Flyt skyderen til **Ja** for at aktivere intern ressourceplanlægning og timesedler.
13. Marker den valgte række på listen.
14. Vælg **Ny**.
15. I feltet **Låntagende juridisk enhed** skal du angive eller vælge en værdi.
16. Marker afkrydsningsfeltet **Akkumuler omsætning**.
17. I feltet **Standardkategori for timesedler** skal du angive eller vælge en værdi.
18. I feltet **Standardkategori for udgifter** skal du angive eller vælge en værdi.
19. Vælg **Gem**.
20. Luk siden.
21. Gå til **Moduler > Projektstyring og regnskab > Opsætning > Bogføring > Konfiguration af bogføring i hovedbogen** i navigationsruden.
22. I feltet **Kontotyper i hovedbogen** skal du vælge en indstilling.
23. Vælg **Ny**.
24. I feltet **Hovedkonto** i den nye række skal du angive de ønskede værdier.
25. Vælg **Gem**.
26. Luk siden.
27. Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Overfør pris** i navigationsruden.
28. Vælg **Ny**.
29. Angiv en dato i feltet **Ikrafttrædelsesdato**.
30. I feltet **Låntagende juridisk enhed** skal du angive eller vælge en værdi.
31. I feltet **Model for overførsel af pris** skal du vælge en indstilling.
32. Angiv et nummer i feltet **Prisfastsættelse**.
33. Vælg **Gem**.

