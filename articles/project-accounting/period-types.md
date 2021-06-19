---
title: Periodetyper
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere periodetyper for omsætningsestimeringer.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013479"
---
# <a name="period-types"></a>Periodetyper

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En periodetype definerer, hvor ofte omsætningen på et projekt estimeres. Dette emne indeholder oplysninger om, hvordan du kan konfigurere periodetyper for omsætningsestimeringer. 

## <a name="create-and-work-with-period-types"></a>Opret og arbejd med periodetyper
Hvis du vil oprette og arbejde med periodetyper, skal du udføre følgende trin:

1. I dit Dynamics 365 Finance-miljø skal du gå til **Projektstyring og regnskab** > **Opsætning** > **Estimater** > **Periodetyper**.
2. Vælg **Ny** for at oprette nye periodetyper. Angiv et navn og en beskrivelse.
3. Vælg en værdi i feltet **Hyppighed**:

    - Hvis du vælger **Uge**, **Halvugelig**, **Halvmånedlig**, **Måned**, **Dag**, **Kvartal** eller **År**, bruges kalenderen til at oprette perioderne. 
    - Hvis du vælger **Finansperiode**, bruges regnskabsperioder fra konfigurationen af finanskladden til at oprette perioder.
    - Hvis du vælger **Ubegrænset**, kan du angive brugerdefinerede perioder.
4. Vælg periodetypeposten, og vælg derefter **Opret perioder** for at oprette perioder til periodetypen. Afhængigt af den periodefrekvens, du har valgt, har du måske mulighed for at angive en startdato eller det antal perioder, der skal genereres.
5. Vælg **Perioder** for at gennemse genererede perioder.



[!INCLUDE[footer-include](../includes/footer-banner.md)]