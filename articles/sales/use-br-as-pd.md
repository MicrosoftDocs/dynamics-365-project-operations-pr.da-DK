---
title: Anvend en reserverbar ressource som en prisfastsættelsesdimension
description: Dette emne indeholder oplysninger om, hvordan du bruger en reserverbar ressource som en prisdimension.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dcd01d80236f0218bc6fa3a1fe1389f8314f3c9b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598620"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Anvend en reserverbar ressource som en prisfastsættelsesdimension

 _**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_ 

Dette emne indeholder oplysninger om, hvordan du bruger en reserverbar ressource som en prisdimension. Hvis din prisfastsættelsesstrategien er konfigureret, så hver enkelt ressource skal have en bestemt pris- eller omkostningssats, skal du bruge en reserverbare ressource som en prisfastsættelsesdimension.

## <a name="prerequisites"></a>Forudsætninger
Før du fuldfører procedurerne i dette emne, skal du have en ny prisfastsættelsesdimensionsløsning til organisationen. Hvis du ikke allerede har oprettet en, kan du se [Opret brugerdefinerede felter og objekter](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Tilføj feltet Reserverbar ressource til formularer og visninger
Hvis du vil gøre feltet **Reserverbar ressource** synligt i prisfastsættelsesdimensionsløsningen, skal du tilføje feltet til alle formularer og visninger som et objekt.

I følgende tabel vises alle indbyggede formularer og visninger efter objekt. Du skal også tilføje det nye felt til eventuelle yderligere formularer eller visninger i de tilpassede objekter.

|   Enhed        | Formularer   |Visninger        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris| Oplysninger | - Aktive ressourcekategoripriser<br> - Tilknyttede ressourcekategoripriser |
|  Rolleprisavance| Oplysninger| - Aktiv rolleprisavance<br>- Tilknyttet rolleprisavance |
|  Tilbudslinjedetaljer| - Projektoplysninger<br>- Hurtig oprettelse af projekt| - Aktiv tilbudslinjedetalje<br>- Kombinerede tilbudslinjedetaljer<br>- Tilknyttet tilbudslinjedetalje |
|  Projektkontraktlinjedetalje| - Projektoplysninger<br>- Hurtig oprettelse af projekt| - Kombinerede kontraktlinjedetaljer<br>- Aktive kontraktlinjedetaljer<br>- Tilknyttet kontraktlinjedetaljer |
|  Projektopgave| - Oplysninger<br>- Ny formular| &nbsp; |
|  Medlem af projektteam| - Oplysninger<br>- Ny formular| - Aktive medlemmer af projektteam<br>- Projektteamets medlemmer<br>- Tilknyttede medlemmer af projektteam |
|  Tidsregistrering| - Oplysninger<br>- Opret tidsregistrering| - Mine tidsregistreringer efter dato<br>- Mine tidsregistreringer for denne uge<br>- Tidsregistreringer til godkendelse|
|  Kladdelinje| - Oplysninger<br>- Hurtig oprettelse| - Aktive kladdelinjer<br>- Visning for tilknyttet kladdelinje |
|  Fakturalinjedetalje| - Oplysninger<br>- Hurtig oprettelse| - Aktive fakturalinjedetaljer<br>- Fakturerbare fakturatransaktioner<br>- Gratis fakturatransaktioner<br>- Tilknyttede fakturalinjedetaljer <br>- Ikke-fakturerbare fakturatransaktioner|
|  Faktisk| - Oplysninger<br>- Aktive faktiske| Tilknyttet faktisk |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Konfigurer en reserverbar ressource som en prisfastsættelsesdimension
For at konfigurere en reserverbar ressource som en prisfastsættelsesdimension skal du gøre følgende:

1. Gå til **Indstillinger** > **Parametre**. 
2. På siden **Parameter** skal du på fanen **Beløbsbaserede prisdimensioner** godkende, at gitteret viser posterne i objektet **Prisdimensioner**. 
2. Føj **Reserverbar ressource** til denne liste over prisdimensioner som **msdyn_bookableresource**. 
3. I **Gælder for omkostning** og **Gælder for salg** skal du vælge en værdi.
4. Vælg **Beløbsbaseret** i **Dimensionstype**. 
5. Vælg omkostnings- og salgsprioritet for den reservarbare ressource. En reserverbar ressource har som regel den højeste prioritet, når den inkluderes som en prisfastsættelsesdimension. Angiv prioriteten til **1** (eller **0** afhængigt af, hvordan du tæller prioriteten) for at sikre denne funktionsmåde.

## <a name="set-up-pricing-dimension-field-names"></a>Konfigurere feltnavne for prisdimensioner

Når feltnavnet for en prisfastsættelsesdimension i tabellen **Rollepris** adskiller sig fra feltnavnet i et af de andre objekter, hvor standardprisen anvendes, skal prisfastsættelsesdimensionsposten underrettes om de forskellige navne.  

For en reserverbar ressource er objektet **Projektteammedlemmer** navngivet en smule anerledes på baggrund af, hvad det kaldes i objektet **Rollepris**: 

 - **Projektteammedlemmer**-objekt = **msdyn_bookableresourceid**
 - **Rollepris**-objekt = **msdyn_bookableresource**

Prisfastsættelsesdimensionsposten for **msydn_bookableresource** skal underrettes om forskellen.

1. Dobbeltklik på rækken i gitteret **Prisfastsættelsesdimensioner** for at åbne dimensionssiden i **msdyn_bookableresource**.
2. På dimensionssiden skal du på fanen **Relaterede** vælge **Feltnavne for prisfastsættelsesdimenstioner**.

  ![Fanen Feltnavne for prisdimensioner.](media/PD-fieldname.png)

3. Vælg **Tilføj nyt feltnavn for prisfastsættelsesdimension** i den tilknyttede visning, der åbnes.

  ![Tilføj nye feltnavne for prisdimensioner.](media/Add-NewPD-fieldname.png)

  Derved åbnes siden **Nyt feltnavn for prisdimension** for **msdyn_bookableresource**. 

4. På siden **Nyt feltnavn for prisfastsættelsesdimension** skal du tilføje **msdyn_projectteam** til **Logisk objektnavn**.
5. Tilføj **msdyn_bookableresourceid** til **Feltnavn**.

 ![Formular til nyt feltnavn for prisdimension.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]