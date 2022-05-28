---
title: Konfigurer standardomkostninger for arbejde og udgifter
description: I dette emne beskrives det, hvordan du kan konfigurere standardomkostninger for arbejdskraft og udgifter i et projekt.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd74da69986a73e933f8cfedce40158555c2ac60
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685325"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurer standardomkostninger for arbejde og udgifter

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]