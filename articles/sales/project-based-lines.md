---
title: Projektbaserede salgsmulighedslinjer
description: Dette emne indeholder oplysninger om at arbejde med projektbaserede salgsmulighedslinjer.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cceb175210f7b597d682e9e4e910c79280211293
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600919"
---
# <a name="project-based-opportunity-lines"></a>Projektbaserede salgsmulighedslinjer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


Projektbaserede salgsmulighedslinjer er kun tilgængelige i projektbaserede salgsmuligheder. Projektbaserede salgsmulighedsposter har feltværdien **Type** angivet til **Arbejdsbaseret**.

Projektbaserede salgsmulighedslinjer er de linjeelementer, der skal leveres til kunden ved hjælp af et projekt. Et projekt kan dog ikke bindes til en projektbaseret salgsmulighedslinje. Projekter kan knyttes til linjeelementer fra fasen **Tilbud** og fremefter, da salgsmuligheden typisk opstår i et tidligt stadium i en handel. Beslutningen om, hvor mange projekter der skal bruges til at levere arbejdet til kunden, er en beslutning, der senere træffes i salgsfasen. Brug salgsmulighedsfasen til at identificere de diskrete leveringskomponenter for kunden. De beslutninger, der omgiver det faktiske antal projekter, der bruges til at levere disse komponenter, kan udskydes, indtil der er flere oplysninger tilgængelige om selve arbejdet.

Nedenfor vises felterne på en projektbaseret salgsmulighedslinje:

| **Felt** | **Placering** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Produkttype | Fanen Generelt (skjult) | Dette er et felt med grupperet indstilling. Hvis der er installeret Dynamics 365 Operations, er en af de tilgængelige indstillinger **Projektbaseret service**.  | Værdien i dette felt er angivet til **Projektbaseret service**, når du opretter den projektbaserede salgsmulighedslinje fra gitteret for projektbaserede linjer i salgsmuligheden. <br> Hvis du ændrer eller tilsidesætter denne værdi, aktiveres projektfunktionen ikke i dine projektbaserede linjeelementer. |
| Salgsmulighed | Fanen Generelt | Dette felt er skrivebeskyttet og refererer til den overordnede salgsmulighedspost, som linjeelementet tilhører. | Dette felt har ingen downstream-virkning. |
| Navn | Fanen Generelt | Dette er et redigerbart tekstfelt, der kan bruges til at give en kort identitet til dette linjeelement | Denne værdi overføres til tilbudslinjen, når du opretter et tilbud fra denne salgsmulighed |
| Kundebudget | Fanen Generelt | Dette redigerbare valutafelt kan bruges til at spore det beløb, som kunden er villig til at bruge på dette linjeelement. | Denne værdi overføres til det tilsvarende felt på tilbudslinjen, når du opretter et tilbud fra denne salgsmulighed |
| Faktureringsmetode | Fanen Generelt | Dette redigerbare felt har følgende værdier:</br>- Tid og materiale</br>- Fast pris | Denne værdi overføres til det tilsvarende felt på tilbudslinjen, når du opretter et tilbud fra denne salgsmulighed. Når tilbudslinjen er oprettet, er feltet låst og kan ikke ændres. Tildel denne feltværdi så præcist som muligt. Hvis du har brug for at ændre værdien i dette felt på tilbudslinjen, skal du slette og oprette tilbudslinjen igen. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]