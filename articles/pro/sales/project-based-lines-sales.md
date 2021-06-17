---
title: Projektbaserede salgsmulighedslinjer - lille
description: Dette emne indeholder oplysninger om projektbaserede salgsmulighedslinjer. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 90b1b078d51c2842f6406c4455188a4433820a77
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994399"
---
# <a name="project-based-opportunity-lines---lite"></a>Projektbaserede salgsmulighedslinjer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Projektbaserede salgsmulighedslinjer er kun tilgængelige i projektbaserede salgsmuligheder. Projektbaserede salgsmulighedsposter har feltværdien **Type** angivet til **Arbejdsbaseret**.

Projektbaserede salgsmulighedslinjer er de linjeelementer, der skal leveres til kunden ved hjælp af et projekt. Et projekt kan dog ikke bindes til en projektbaseret salgsmulighedslinje. Projekter kan knyttes til linjeelementer fra fasen **Tilbud** og fremefter, da salgsmuligheden typisk er i et tidligt stadium i en handels livscyklus. Beslutningen om, hvor mange projekter der skal bruges til at levere arbejdet til kunden, er en beslutning, der senere træffes i salgsfasen. Du kan bruge salgsmulighedsfasen til at identificere de diskrete leveringskomponenter for kunden. De beslutninger, der omgiver det faktiske antal projekter, der bruges til at levere disse komponenter, kan udskydes, indtil der er flere oplysninger tilgængelige om selve arbejdet.

Nedenfor vises felterne på en projektbaseret salgsmulighedslinje:

| **Felt** | **Placering** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Produkttype | Fanen Generelt (skjult) | Du kan vælge en af følgende indstillinger under:</br>- Projektbaseret tjeneste (kun tilgængelig, når Dynamics 365 Project Operations er installeret)</br>- Produkt (kun tilgængelig, når Project Operations og Dynamics 365 Sales er installeret) | Værdien i dette felt er angivet til **Projektbaseret service**, når du opretter en projektbaserede salgsmulighedslinje fra gitteret for projektbaserede linjer i salgsmuligheden. <br> Hvis du ændrer eller tilsidesætter denne værdi, aktiveres projektfunktionen ikke i dine projektbaserede linjeelementer. |
| Salgsmulighed | Fanen Generelt | Dette felt er skrivebeskyttet og refererer til de overordnede salgsmulighedsposter, som linjeelementet tilhører. | Dette felt har ingen downstream-virkning. |
| Navn | Fanen Generelt | Dette redigerbare tekstfelt kan bruges til at give en kort identitet til linjeelementet. | Denne værdi overføres til tilbudslinjen, når du opretter et tilbud fra denne salgsmulighed. |
| Kundebudget | Fanen Generelt | Dette redigerbare valutafelt kan bruges til at spore det beløb, som kunden er villig til at bruge på dette linjeelement. | Denne værdi overføres til det tilsvarende felt på tilbudslinjen, når du opretter et tilbud fra denne salgsmulighed. |
| Faktureringsmetode | Fanen Generelt | Dette redigerbare felt har følgende værdier:</br>- Tid og materiale</br>- Fast pris | Denne værdi overføres til det tilsvarende felt på tilbudslinjen, når du opretter et tilbud fra denne salgsmulighed. Når tilbudslinjen er oprettet, er feltet låst og kan ikke ændres. Tildel denne feltværdi så præcist som muligt. Hvis du har brug for at ændre værdien i dette felt på tilbudslinjen, skal du slette og oprette tilbudslinjen igen. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]