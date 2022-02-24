---
title: Bruge reserverbar ressource som en prisdimension
description: Denne emne indeholder oplysninger om, hvordan du bruger en reserverbar ressource som en prisdimension.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: d9b25a768f892d83c09d37ce76291d6c8e75b1be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144991"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Bruge reserverbar ressource som en prisdimension

[!include [banner](../includes/psa-now-project-operations.md)]

Denne emne indeholder oplysninger om, hvordan du bruger en reserverbar ressource som en prisdimension. Før du går i gang, skal du oprette en ny prisdimensionsløsning, hvis du ikke allerede har oprettet én. Hvis du allerede har en prisdimensionsløsning, kan du foretage ændringerne i den pågældende løsning. Hvis du ikke har oprettet en ny prisdimensionsløsning for organisationen, skal du fuldføre procedurerne i emnet [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Føje reserverbar ressource til formularer og visninger
Hvis du vil gøre felterne synlige i brugergrænsefladen i prisdimensionsløsningen, skal du gennemgå alle formularerne og visningerne for de vigtige Project Service-objekter og føje disse felter til formularerne og visningerne for de pågældende objekter.
Følgende tabel indeholder en omfattende liste over standardformularer og -visninger, opstillet efter objekt, der skal opdateres. Hvis der er flere visninger eller formularer i tilpasningerne af disse objekter, kan du også føje de nye felter til dem.
Åbn Løsningsoversigt for prisdimensionsløsningen, og klik derefter på **Publicer alle tilpasninger**.


|   Objekt        | Formularer   |Visninger        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris|• Oplysninger |• Aktive ressourcekategoripriser<br> • Visning for tilknyttede ressourcekategoripriser|
|  Rolleprisavance|• Oplysninger|• Aktiv rolleprisavance<br>• Visning for tilknyttet rolleprisavance|
|  Tilbudslinjedetaljer|• Projektoplysninger<br>• Hurtig oprettelse af projekt|• Aktiv tilbudslinjedetalje<br>• Kombinerede tilbudslinjedetaljer<br>• Visning for tilknyttet tilbudslinjedetalje|
|  Projektkontraktlinjedetalje|• Projektoplysninger<br>• Hurtig oprettelse af projekt|• Kombinerede kontraktlinjedetaljer<br>• Aktive kontraktlinjedetaljer<br>• Tilknyttet visning af kontraktlinjedetaljer|
|  Projektopgave|• Oplysninger<br>• Ny formular||
|  Medlem af projektteam|• Oplysninger<br>• Ny formular|• Aktive medlemmer af projektteam<br>• Medlemmer af projektteam<br>• Visning for tilknyttede medlemmer af projektteam|
|  Tidsregistrering|• Oplysninger<br>• Oprette tidsregistrering|• Mine tidsregistreringer efter dato<br>• Mine tidsregistreringer for denne uge<br>• Tidsregistreringer til godkendelse.|
|  Kladdelinje|• Oplysninger<br>• Hurtig oprettelse:|• Aktive kladdelinjer<br>• Visning for tilknyttet kladdelinje|
|  Fakturalinjedetalje|• Oplysninger<br>• Hurtig oprettelse:|• Aktive fakturalinjedetaljer<br>• Fakturerbare fakturatransaktioner<br>• Gratis fakturatransaktioner<br>• Visning for tilknyttede fakturalinjedetaljer<br>• Ikke-fakturerbar fakturatransaktion|
|  Faktisk|• Oplysninger<br>• Aktive faktiske|• Visning for tilknyttet faktisk|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Konfigurere reserverbar ressource som en prisdimension

1. Gå til **Project Service** > **Indstillinger** > **Parametre** i webgrænsefladen. På siden **Parameter** skal du under fanen **Beløbsbaserede prisdimensioner** læg mærke til, at gitteret under fanen viser posterne i prisdimensionsobjektet. 
2. Føj **Reserverbar ressource** til denne liste over prisdimensioner som **msdyn_bookableresource**. 
3. Angiv den kontekst, hvori den reserverbare ressource fungerer som en prisdimension, og angiv værdierne af **Gælder for Omkostning** og **Gælder for Salg**.
4. Vælg **Beløbsbaseret** i feltet **Dimensionstype**. 
5. Vælg omkostnings- og salgsprioritet for den reservarbare ressource. Når en reservarbar ressource er medtaget som en prisdimension, har den typisk højest prioritet, så hvis denne indstilling angives til **1** (eller **0** afhængigt af, hvordan du beregner prioriteten) , vil det sikre, at det fungerer.

## <a name="set-up-pricing-dimension-field-names"></a>Konfigurere feltnavne for prisdimensioner

Når feltnavnet for en prisdimension i tabellen **Rollepris** adskiller sig fra feltnavnet i et af de andre objekter, hvor prisstandard skal fungere, skal prisdimensionsposten gøres opmærksom på de forskellige navne.    
I forbindelse med en reserverbar ressource har objektet **Medlemmer af projektteam** et lidt andet feltnavn (**msdyn_bookableresourceid**) end på objektet **Rollepris** (**msdyn_ bookableresource**). Prisdimensionsposten for **msydn_bookableresource** skal gøres opmærksom på dette. 
1. Det kan du gøre ved at dobbeltklikke på rækken i gitteret **Prisdimensioner** for at åbne dimensionssiden i **msdyn_bookableresource**.
2. Klik på **Feltnavne for prisdimensioner** under fanen **Relaterede**.

 ![Fanen Feltnavne for prisdimensioner](media/PD-fieldname.png)

4. Klik på **Tilføj nyt feltnavn for prisdimension** i den tilknyttede visning, der åbnes.

 ![Tilføje nye feltnavne for prisdimensioner](media/Add-NewPD-fieldname.png)


Derved åbnes siden **Nyt feltnavn for prisdimension** for **msdyn_bookableresource**. 

5. Føj **msdyn_projectteam** til feltet **Objektets logiske navn** og **msdyn_bookableresourceid** til feltet **Feltnavn**. Gem posten.

 ![Formular til nyt feltnavn for prisdimension](media/PD-fieldname-Added.png)
