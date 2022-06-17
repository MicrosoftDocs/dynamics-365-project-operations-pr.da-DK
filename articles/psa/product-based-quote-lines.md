---
title: Produktbaserede tilbudslinjer.
description: Denne artikel indeholder oplysninger om produktbaserede tilbudslinjer.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a5385e1bb0f18a7cc1d23f4e46c86d8340ba951d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922675"
---
# <a name="product-based-quote-lines"></a>Produktbaserede tilbudslinjer.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Du kan oprette produktbaserede tilbudslinjer i Dynamics 365 Project Service Automation. Produktbaserede tilbudslinjer kan være "linjer, der skal rekvireres", eller de kan være elementer fra produktkataloget.

## <a name="product-catalog"></a>Produktkatalog

Produkterne i et Dynamics 365-produktkatalog har en standardenhed og enhedsgruppe. Hvis flere produkter deler det samme sæt attributter, kan du oprette en produktfamilie, der også har de pågældende attributter. Alle produkter i én produktfamilie arver det samme sæt attributter.

Et firma sælger f.eks. abonnementslicenser til forskellige typer programmer. Alle abonnementsprogrammer har følgende to attributter:

- Antal brugere 
- Abonnements varighed (i måneder)

En god måde at vedligeholde denne type katalog på er at oprette en produktserie med navnet **Abonnementsprogrammer**, og som har **Antal brugere** og **Abonnements varighed** som attributter. Du kan derefter føje individuelle produkter, f.eks. **Dynamics 365 Sales** eller **Dynamics 365 Field Service**, til produktserien **Abonnementsprogrammer**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Tilføjelse af produktkatalogelementer til et projekttilbud

Siderne for projekttilbud og projektkontrakter indeholder afsnit til to typer linjer: projektbaserede linjer og produktbaserede linjer. I forbindelse med produktbaserede linjer bruges Dynamics 365 til at føje elementer fra et produktkatalog til et tilbud. Rullelisten på tilbudslinjen eller på projektkontraktlinjen indeholder alle de produkter og enheder i produktprislisten, der er knyttet til tilbuddet eller projektkontrakten. Du kan også tilføje produkter, der ikke er en del af et tilbuds produktprisliste.

Derudover kan du vælge produkter fra andre prislister, eller du kan vælge produkter direkte fra produktkataloget. Når du vælger produkter direkte fra et produktkatalog, bruges standardprislisten for produktet til at beregne produktets salgspris. Hvis der ikke er angivet en standardprisliste, angives prisen til 0 (nul).

Hvis en tilbudslinje er baseret på et produktkatalog, kan du tilsidesætte salgsprisen direkte på tilbudslinjen. Bemærk, at en tilbudslinje i Dynamics 365 har feltet **Prisfastsættelse**. Der findes følgende to værdier:

- Tilsidesæt prisfastsættelse  
- Benyt som standard

Hvis du angiver dette felt til **Tilsidesæt prisfastsættelse**, angives der ikke en standardpris i Dynamics 365. Du skal angive en pris for produktet på tilbudslinjen. Hvis du angiver dette felt til **Benyt som standard**, bruger Dynamics 365 standardsalgsprisen og låser feltet for at forhindre, at der redigeres.

Når du har installeret PSA, angives standardsalgspriserne på de produktbaserede linjer i et tilbud. Feltet **Prisfastsættelse** indstilles derefter til **Tilsidesæt prisfastsættelse**, så du kan redigere standardprisen i tilbudslinjerne.

> ![Indstilling af tilsidesæt prisfastsættelse.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Mængdefaktorer for produkter

I PSA bruges mængdefaktorer til at understøtte salget af abonnementsbaserede produkter. I forbindelse med abonnementsbaserede produkter udtrykkes antallet i tilbuds- eller projektkontraktlinjen som antallet af brugermåneder.

Prisen for abonnementsprogrammer gemmes som regel i kataloget som pris pr. bruger pr. måned. Men du kan også bruge andre tidsbeskrivelser i stedet. Under salgsprocessen er prisen i tilbudslinjen som regel den pris pr. bruger, pris pr. måned, som blev forhandlet og fratrukket af IT-salgsagenten. Hver handel har et forskelligt antal brugere og et forskelligt antal abonnementsmåneder. Det antal, der bruges til at beregne beløbet i tilbudslinjen, er et produkt af antallet af brugere og antallet af abonnementsmåneder.

For at understøtte denne type salg introduceres konceptet med mængdefaktorer i PSA. Mængdefaktorer er baseret på produktattributterne i Dynamics 365. Når du konfigurerer bestemte egenskaber for et produkt, giver PSA dig mulighed for at markere et undersæt af disse egenskaber eller alle egenskaberne som mængdefaktorer.

PSA validerer, at kun numeriske egenskaber eller produktegenskaber med numerisk datatype markeres som mængdefaktorer. Når et produkt, som der konfigureres mængdefaktorer for, føjes til en tilbudslinje, bliver feltet **Antal** i tilbudslinjen et skrivebeskyttet felt. Når du har angivet værdier for produktegenskaber, der er mængdefaktorer, beregner PSA antallet i tilbudslinjen.

Dynamics 365 kan f.eks. have følgende egenskaber: 

- **Antal brugere** – Antallet af brugere 
- **Antal måneder** – Antallet af abonnementsmåneder
- **Produkt-SKU** 

Egenskaberne **Antal brugere** og **Antal måneder** kan mærkes som mængdefaktorer ved at redigere egenskaberne for produktlinjen. 

> ![Mærkning af Antal brugere og Antal måneder som kvalitetsfaktorer.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
