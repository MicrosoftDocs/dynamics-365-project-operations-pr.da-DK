---
title: Konfiguration af brugerdefinerede felter som prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om konfiguration af brugerdefinerede prisfastsættelsesdimensioner.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150346"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Konfiguration af brugerdefinerede felter som prisfastsættelsesdimensioner 

[!include [banner](../includes/psa-now-project-operations.md)]

Før du går i gang, forudsætter dette emne, at du har fuldført procedurerne i emnerne [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities.md) og [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](field-references.md). Hvis du ikke har fuldført procedurerne, skal du gå tilbage og fuldføre dem og derefter vende tilbage til dette emne. 

Dette emne indeholder oplysninger om konfiguration af brugerdefinerede prisfastsættelsesdimensioner. I webgrænsefladen for Project Service viser fanen **Beløbsbaserede prisdimensioner** på siden **Parametre** posterne i prisdimensionsobjekterne. Som standard opretter Project Service-installationen 2 rækker i gitteret på denne fane:

- **msdyn_resourcecategory** (Rolle)
- **msdyn_OrganizationalUnit** (Afdeling)

> [!IMPORTANT]
> Du skal ikke slette disse rækker. Men hvis du ikke har brug for dem, kan du gøre dem ikke gældende i en bestemt sammenhæng ved at indstille **Gælder for Omkostning**, **Gælder for Salg** og **Gælder for Køb** alle til **Nej**. Hvis du angiver disse attributter til **Nej**, har det den samme effekt, som hvis feltet ikke var der som en prisdimension.

Hvis et felt skal blive til en prisdimension, skal det være:

- Oprettet som et felt i objekterne **Rollepris** og **Rolleprisavance**. Du finder flere oplysninger om, hvordan du gør dette, i [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](field-references.md).
- Oprettet som en række i tabellen **Prisdimension**. Du kan f.eks. tilføje rækker med prisdimensioner som vist i følgende grafik. 

![Beløbsbaserede prisdimensionsrækker](media/Amt-based-PD.png)

Bemærk, at Arbejdstimer for ressource (**msdyn_resourceworkhours**) er blevet tilføjet som en avancebaseret dimension og er blevet føjet til gitteret på fanen **Avancebaserede prisdimensioner**.

![Avancebaserede prisdimensionsrækker](media/Markup-based-PD.png)

> [!IMPORTANT]
> Eventuelle ændringer af prisdimensionsdata i denne tabel, eksisterende eller nye, overføres kun til forretningslogikken for prisfastsættelse i Project Service, når cachen er opdateret. Det kan tage op til 10 minutter at opdatere cachen. Tillad denne tid for at se ændringerne i standardlogikken for priser, som bliver resultatet efter ændringer i prisdimensionsdataene.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attributter i tabellen med prisdimensioner
I følgende afsnit kan du finde oplysninger om de forskellige attributter i tabellen **Prisdimensioner**.

### <a name="pricing-dimension-name"></a>Prisdimensionsnavn
Denne værdi skal være præcis den samme som skemanavnet på det felt, der føjes til tabellen **Rollepris** for brugerdefinerede prisdimensioner. Du kan finde flere oplysninger om, hvordan du føjer felter til tabellen **Rollepris**, i [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](field-references.md)og transaktions enheder.

### <a name="type-of-dimension"></a>Dimensionstype
Der findes to typer prisdimensioner:
  
  - **Beløbsbaserede dimensioner**: Dimensionsværdierne fra inputkonteksten sættes i forhold til dimensionsværdierne på linjen **Rollepris** og prisen/omkostningerne hentes som standard direkte fra tabellen **Rollepris**.
  - **Avancebaserede dimensioner**: Dette er dimensioner, hvor Project Service udfører følgende proces i tre trin for at få prisen/omkostningerne
 
    1. Project Service får de ikke-avancebaserede dimensionsværdier fra inputkonteksten til at stemme overens med rolleprislinjen for at beregne grundtaksten.
    2. Project Service får alle dimensionsværdierne fra inputkonteksten til at stemme overens med linjen **Rolleprisavance** for at beregne en avanceprocent.
    3. I Project Service anvendes avanceprocenten fra det andet trin på den grundsats, der kom fra tabellen **Rollepris** i det første trin, for at finde frem til den endelige pris/omkostning.
   
   I følgende tabel illustreres beregningen af prisavancer.
  
| Rolle        | Afdeling    |Arbejdssted      |Standardtitel      |Arbejdstimer for ressource      |  Markere|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|På stedet            |                    |Overtid                 |15     |
|             | Contoso India|Lokal             |                    |Overtid                 |10     |
|             | Contoso USA   |Lokal             |                    |Overtid                 |20     |


Hvis en ressource fra Contoso India, hvis grundtakst er 100 USD, arbejder på stedet, og de registrerer 8 timers normal arbejdstid og 2 timers overarbejde for tidsregistreringen, bruger prissætningsfunktionen i Project Service grundtaksten på 100 for de 8 timer og vil registrere 800 USD. For de 2 overarbejdstimer vil der blive lagt en avance på 15 % på grundtaksten på 100, så der fås en enhedspris på 115 USD, og der registreres en samlet omkostning på 230 USD.

### <a name="applicable-to-cost"></a>Gælder for Omkostning 
Hvis denne indstilles til **Ja**, angiver det, at dimensionsværdien fra inputkonteksten skal bruges, så den stemmer overens med **Rollepris** og **Rolleprisavance** for at finde omkostnings- og avancetaksterne.

### <a name="applicable-to-sales"></a>Gælder for Salg
Hvis denne indstilles til **Ja**, angiver det, at dimensionsværdien fra inputkonteksten skal bruges, så den stemmer overens med **Rollepris** og **Rolleprisavance** for at finde fakturerings- og avancetaksterne.

### <a name="applicable-to-purchase"></a>Gælder for Køb
Hvis denne indstilles til **Ja**, angiver det, at dimensionsværdien fra inputkonteksten skal bruges, så den stemmer overens med **Rollepris** og **Rolleprisavance** for at finde købsprisen. I øjeblikket understøtter Project Service ikke scenarier for underleverandører, så dette felt bruges ikke. 

### <a name="priority"></a>Prioritet
Når dimensionsprioriteten er angivet, kan Project Service bruges til at oprette en pris, også selvom der ikke er et nøjagtigt match mellem inputdimensionsværdierne og værdierne fra tabellerne **Rollepris** eller **Rolleprisavance**. I dette scenario bruger Project Service null-værdier til ikke-overensstemmende dimensionsværdier ved at vægte dimensionerne i prioriteret rækkefølge.

- **Omkostningsprioritet**: Værdien for en dimensions omkostningsprioritet angiver den pågældende dimensions vægtning, når den matches i forhold til opsætningen af kostpriser. Værdien for **Omkostningsprioritet** skal være entydig på tværs af dimensioner, der **Gælder for Omkostning**.
- **Salgsprioritet**: Værdien for en dimensions salgsprioritet angiver den pågældende dimensions vægtning, når den matches i forhold til opsætningen af salgspriser eller fakturasatser. Værdien for **Salgsprioritet** skal være entydig på tværs af dimensioner, der **Gælder for Salg**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]