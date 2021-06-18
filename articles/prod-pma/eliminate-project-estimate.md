---
title: Eliminer et projektestimat
description: Dette emne indeholder oplysninger om, hvordan du eliminerer et projektestimat, efter at det er fuldført.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006909"
---
# <a name="eliminate-a-project-estimate"></a>Eliminer et projektestimat

[!include [banner](../includes/banner.md)]

Projektestimater giver en økonomisk visning af det arbejde, der er estimeret og planlagt i et projekt. Hvis du vil arbejde med estimater for et projekt, skal du knytte projektet til et estimatprojekt. Et estimatprojekt er altid baseret på et eksisterende projekt, men flere projekter kan referere til et enkelt estimatprojekt. Det er kun fastprisprojekter og investeringsprojekter, der kan tilknyttes estimatprojekter, og de pågældende projekter skal tilhøre samme projektgruppe som det estimerede projekt.

Hvis du vil eliminere et estimatprojekt, skal det være fuldført. Følgende fremgangsmåde beskriver, hvordan du kan eliminerer et estimat.

1. Gå til **Projektstyring og regnskab** > **Alle projekter**, og åbn projektet. 
2. På fanen **Administrer** skal du vælge **Estimater**, og på siden **Estimer** skal du vælge **Eliminer**.
3. På siden **Eliminer estimat** skal du på fanen **Generelt** angive følgende indstillinger:

   - **Periodekode**: Vælg periodekoden for at vælge de relevante estimatprojekter. 
   - **Estimatdato**: Vælg den relevante estimatdato, der skal elimineres.
   - **Fjern med IGVA-advarsler**: Aktivér denne indstilling for at give besked, når et estimat, der er knyttet til igangværende arbejde (IGVA), elimineres. Hvis denne indstilling ikke er aktiveret, kan elimineringen ikke fortsætte, hvis der findes ikke-estimerede transaktioner. 
   > [!NOTE]
   > Denne indstilling er kun tilgængelig, når elimineringen finder anvendelse på et estimatprojekt. Den er ikke tilgængelig, hvis du bruger periodiske bogføringer. Denne indstilling fungerer sammen med indstillingerne under fanen **Estimat** på siden **Projektparametre** i feltgruppen **Tillad eliminering, når der findes ikke-estimerede transaktioner**.
   - **Angiv stadie for afslutning**: Aktivér denne indstilling for at angive, at estimatprojektets fase skal **Afsluttes**, når du har kørt elimineringen.
   - **Udskriv estimatliste**: Vælg de oplysninger, der skal medtages, når estimatlisten udskrives.
   - **Vis infolog**: Aktivér denne indstilling for at få vist infologgen.
   - **Bogføringsdato**: Vælg estimatets bogføringsdato i hovedbogen.

4.  Vælg **OK**.
5. Når elimineringsprocessen er fuldført, vises det eliminerede estimatprojekt med en negativ værdi. 

Hvis du ikke har tænkt dig at eliminere et estimat, kan du vælge det eliminerede estimat og vælge **Tilbagefør eliminering**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]