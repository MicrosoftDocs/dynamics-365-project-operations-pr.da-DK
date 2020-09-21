---
title: Konfigurer standardomkostninger for arbejde og udgifter
description: I dette emne beskrives det, hvordan du kan konfigurere standardomkostninger for arbejdskraft og udgifter i et projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750636"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurer standardomkostninger for arbejde og udgifter

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives det, hvordan du kan konfigurere standardomkostninger for arbejdskraft og udgifter i et projekt. Denne opgave anvender datasættet USSI.

1. Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (time)** i navigationsruden.
2. Vælg **Ny**.
3. Angiv en dato i feltet **Ikrafttrædelsesdato**.
4. Angiv et nummer i feltet **Kostpris**. Du kan oprette en standardkostpris for projektkategorien, eller du kan konfigurere en kostpris pr. arbejdernummer, projektnummer, kategori, dato eller en hvilken som helst kombination af disse. Den anvendte kostpris er kostprisen med det højeste detaljeringsniveau.  
5. Vælg **Gem**.
6. Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (time)** i navigationsruden.
7. Vælg **Ny**.
8. Angiv en dato i feltet **Ikrafttrædelsesdato**.
9. Vælg en indstilling i feltet **Gyldig til**.
10. Angiv et nummer i feltet **Prisfastsættelse**. Du kan oprette en standardsalgspris for timetransaktioner eller for en projektkategori. Du kan også konfigurere salgspriser pr. arbejdernummer, projektnummer, kategori, transaktionsdato eller en hvilken som helst kombination heraf. Den faktiske salgspris, som anvendes, når en arbejder angiver en transaktion i timekladden, er den salgspris, der har det højeste detaljeringsniveau. Hvis du f.eks. både konfigurerer en generel salgspris og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.  
11. Vælg **Gem**.
12. Luk siden.
13. Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Kostpris (udgifter)** i navigationsruden.
14. Vælg **Ny**.
15. Angiv en dato i feltet **Ikrafttrædelsesdato**.
16. Angiv et nummer i feltet **Kostpris**. Det er muligt at udfylde flere felter, men dette er minimumskravet for at gemme posten.  
17. Vælg **Gem**.
18. Gå til **Moduler > Projektstyring og regnskab > Opsætning > Priser > Salgspris (udgifter)** i navigationsruden.
19. Vælg **Ny**.
20. Angiv en dato i feltet **Ikrafttrædelsesdato**.
21. Vælg en indstilling i feltet **Gyldig til**.
22. Angiv et nummer i feltet **Prisfastsættelse**. Den faktiske salgspris, som anvendes, når en arbejder angiver transaktioner i en udgiftskladde, er den salgspris, der har det højeste detaljeringsniveau. Hvis du f.eks. både konfigurerer en generel og en arbejderspecifik salgspris, bruges den arbejderspecifikke salgspris.  
23. Vælg **Gem**.

