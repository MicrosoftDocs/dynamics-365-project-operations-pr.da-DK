---
title: Konfigurer brugerdefinerede felter som prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer prisfastsættelsesdimensioner ved hjælp af brugertilpassede felter.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d40a80f80bd766bfc19e831ea805a4043baf0030
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004704"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Konfigurer brugerdefinerede felter som prisfastsættelsesdimensioner

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Før du går i gang, forudsætter dette emne, at du har fuldført procedurerne i emnerne [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities-pricing-dimensions.md) og [Tilføj krævede brugerdefinerede felter til prisopsætning og transaktionsobjekter](add-custom-fields-price-setup-transactional-entities.md). Hvis du ikke har fuldført procedurerne, skal du gå tilbage og fuldføre dem og derefter vende tilbage til dette emne. 

Dette emne indeholder oplysninger om konfiguration af brugerdefinerede prisfastsættelsesdimensioner. På siden **Parameter** viser fanen **Beløbsbaserede prisfastsættelsesdimensioner** posterne i objekterne for prisfastsættelsesdimensioner. Der er som standard to rækker i gitteret under denne fane:

- **msdyn_resourcecategory** (Rolle)
- **msdyn_OrganizationalUnit** (Afdeling)

> [!IMPORTANT]
> Du skal ikke slette disse rækker. Men hvis du ikke har brug for dem, kan du gøre dem ikke gældende i en bestemt sammenhæng ved at indstille **Gælder for Omkostning**, **Gælder for Salg** og **Gælder for Køb** alle til **Nej**. Hvis du angiver disse attributter til **Nej**, har det den samme effekt, som hvis feltet ikke var der som en prisdimension.

Hvis et felt skal blive til en prisdimension, skal det være:

- Oprettet som et felt i objekterne **Rollepris** og **Rolleprisavance**. Du finder flere oplysninger om, hvordan du gør dette, i [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](add-custom-fields-price-setup-transactional-entities.md).

- Oprettet som en række i tabellen **Prisdimension**. Du kan f.eks. tilføje rækker med prisdimensioner som vist i følgende grafik. 

![Beløbsbaserede prisdimensionsrækker](media/Amt-based-PD.png)

Arbejdstimer for ressource (**msdyn_resourceworkhours**) tilføjes som en avancebaseret dimension og er blevet tilføjet gitteret på fanen **Avancebaserede prisdimensioner**.

![Avancebaserede prisdimensionsrækker](media/Markup-based-PD.png)


> [!IMPORTANT]
> Eventuelle ændringer af prisdimensionsdata i denne tabel, eksisterende eller nye, overføres kun til forretningslogikken for prisfastsættelse, når cachen er opdateret. Det kan tage op til 10 minutter at opdatere cachen. Tillad denne tid for at se ændringerne i standardlogikken for priser, som bliver resultatet efter ændringer i prisdimensionsdataene.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attributter i tabellen med prisdimensioner
I følgende afsnit kan du finde oplysninger om de forskellige attributter i tabellen **Prisdimensioner**.

### <a name="pricing-dimension-name"></a>Prisdimensionsnavn
Denne værdi skal være præcis den samme som skemanavnet på det felt, der føjes til tabellen **Rollepris** for brugerdefinerede prisdimensioner. Du kan finde flere oplysninger om, hvordan du føjer felter til tabellen **Rollepris**, i [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](add-custom-fields-price-setup-transactional-entities.md)og transaktions enheder.

### <a name="type-of-dimension"></a>Dimensionstype
Der findes to typer prisdimensioner:
  
  - **Beløbsbaserede dimensioner**: Dimensionsværdierne fra inputkonteksten sættes i forhold til dimensionsværdierne på linjen **Rollepris** og prisen/omkostningerne hentes som standard direkte fra tabellen **Rollepris**.
  - **Avancebaserede dimensioner**: Dette er dimensioner, hvor følgende proces i tre trin for at få prisen/omkostningerne anvendes:
 
    1. De ikke-avancebaserede dimensionsværdier fra inputkonteksten afstemmes med rolleprislinjen for at få grundtaksten.
    2. Dimensionsværdierne fra inputkonteksten afstemmes med linjen **Rolleprisavance** for at beregne en avanceprocent.
    3. Avanceprocenten fra det andet trin anvendes på den grundtakst, der blev hentet fra tabellen **Rollepris** i det første trin, for at finde frem til den endelige pris/omkostning.
   
   I følgende tabel illustreres beregningen af prisavancer.
  
| Rolle        | Afdeling    |Arbejdssted      |Standardtitel      |Arbejdstimer for ressource      |  Markere|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso Indien|På stedet            |                    |Overtid                 |15     |
|             | Contoso Indien|Lokal             |                    |Overtid                 |10     |
|             | Contoso US   |Lokal             |                    |Overtid                 |20     |


Hvis en ressource fra Contoso Indien, hvis grundtakst er 100 USD, arbejder på stedet, og de registrerer 8 timers normal arbejdstid og 2 timers overarbejde for tidsregistreringen, bruger prisfastsættelsesprogrammet grundtaksten på 100 for de 8 timer og vil registrere 800 USD. For de 2 overarbejdstimer vil der blive lagt en avance på 15 % på grundtaksten på 100, så der fås en enhedspris på 115 USD, og der registreres en samlet omkostning på 230 USD.

### <a name="applicable-to-cost"></a>Gælder for Omkostning 
Hvis denne indstilles til **Ja**, angiver det, at dimensionsværdien fra inputkonteksten skal bruges, så den stemmer overens med **Rollepris** og **Rolleprisavance** for at finde omkostnings- og avancetaksterne.

### <a name="applicable-to-sales"></a>Gælder for Salg
Hvis denne indstilles til **Ja**, angiver det, at dimensionsværdien fra inputkonteksten skal bruges, så den stemmer overens med **Rollepris** og **Rolleprisavance** for at finde fakturerings- og avancetaksterne.

### <a name="applicable-to-purchase"></a>Gælder for Køb
Hvis denne indstilles til **Ja**, angiver det, at dimensionsværdien fra inputkonteksten skal bruges, så den stemmer overens med **Rollepris** og **Rolleprisavance** for at finde købsprisen. Scenarier for underleverandører understøttes ikke, så dette felt bruges ikke. 

### <a name="priority"></a>Prioritet
Opsætning af dimensionsprioritet hjælper prisfastsættelse med at oprette en pris, også selvom der ikke er et nøjagtigt match mellem inputdimensionsværdierne og værdierne fra tabellerne **Rollepris** eller **Rolleprisavance**. I dette scenario bruges null-værdier til ikke-overensstemmende dimensionsværdier ved at vægte dimensionerne i prioriteret rækkefølge.

- **Omkostningsprioritet**: Værdien for en dimensions omkostningsprioritet angiver den pågældende dimensions vægtning, når den matches i forhold til opsætningen af kostpriser. Værdien for **Omkostningsprioritet** skal være entydig på tværs af dimensioner, der **Gælder for Omkostning**.
- **Salgsprioritet**: Værdien for en dimensions salgsprioritet angiver den pågældende dimensions vægtning, når den matches i forhold til opsætningen af salgspriser eller fakturasatser. Værdien for **Salgsprioritet** skal være entydig på tværs af dimensioner, der **Gælder for Salg**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]