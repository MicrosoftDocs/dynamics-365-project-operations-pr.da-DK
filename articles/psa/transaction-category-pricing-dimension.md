---
title: Bruge en transaktionskategori som en prisdimension
description: Dette emne indeholder oplysninger om, hvordan du bruger en transaktionskategori som en prisdimension.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ede5f95a3ba7e122e28875acad1ecc63ff095e63
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593329"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Bruge en transaktionskategori som en prisdimension

[!include [banner](../includes/psa-now-project-operations.md)]

Dette emne viser, hvordan du bruger en transaktionskategori som en prisdimension. Før du går i gang, skal du oprette en ny prisdimensionsløsning, hvis du ikke allerede har oprettet én. Hvis du allerede har en prisdimensionsløsning, kan du foretage ændringerne i den pågældende løsning. Hvis du ikke har oprettet en ny prisdimensionsløsning for organisationen, skal du fuldføre procedurerne i emnet [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Føje transaktionskategori til formularer og visninger
Hvis du vil gøre transaktionkategori synlig i brugergrænsefladen i prisdimensionsløsningen, skal du gennemgå alle formularerne og visningerne af nøgleobjekter og føje disse felter til formularerne og visningerne for de pågældende objekter.
Den følgende tabel er en omfattende liste over standardformularer og -visninger angivet efter objekt, der skal opdateres med de nye felter. Hvis der er flere visninger eller formularer i tilpasningerne af disse objekter, kan du også føje de nye felter til dem.

|  Objekt        | Formularer     |Visninger        |
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

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Konfigurere en transaktionskategori som en prisdimension

1. Gå til **Project Service** > **Indstillinger** > **Parametre** i webgrænsefladen. 
2. På siden **Parameter** skal du på fanen **Beløbsbaserede prisdimensioner** lægge mærke til, at gitteret på fanen viser posterne i objektet **Prisdimensioner**.
3. Føj **Transaktionskategorien** til denne liste, og angiv felterne **Gælder for Omkostning** og **Gælder for Salg** til **Ja**.
4. I feltet **Dimensionstype** skal du vælge **Beløbsbaseret** og derefter vælge den prioritet for **Transaktionskategori**, der er relateret til omkostning og salg.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
