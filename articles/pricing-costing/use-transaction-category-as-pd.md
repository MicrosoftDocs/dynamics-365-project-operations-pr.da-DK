---
title: Anvend en transaktionskategori som en prisfastsættelsesdimension
description: Denne artikel indeholder oplysninger om, hvordan du bruger feltet Transaktionskategori som en prisfastsættelsesdimension.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911687"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Anvend en transaktionskategori som en prisfastsættelsesdimension


_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Denne artikel redegør for, hvordan du bruger feltet **Transaktionskategori** som en prisfastsættelsesdimension. 

## <a name="prerequisites"></a>Forudsætninger
Inden du fuldfører procedurerne i denne artikel, skal du have en ny løsning for prisfastsættelsesdimensioner i din organisation. Hvis du ikke allerede har oprettet en, skal du se [Opret brugerdefinerede felter og objekter som prisfastsættelsesdimensioner](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Tilføj feltet Transaktionskategori til formularer og visninger
Hvis du vil gøre feltet **Transaktionskategori** synligt i prisfastsættelsesdimensionsløsningen, skal du tilføje feltet til alle formularer og visninger som et objekt.

I følgende tabel vises alle indbyggede formularer og visninger efter objekt. Du skal også tilføje det nye felt til eventuelle yderligere formularer eller visninger i de tilpassede objekter.

|  Enhed        | Formularer     |Visninger        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris| Oplysninger |- Aktive ressourcekategoripriser<br> - Tilknyttede ressourcekategoripriser |
|  Rolleprisavance| Oplysninger|- Aktiv rolleprisavance<br>- Tilknyttet rolleprisavance |
|  Tilbudslinjedetaljer|- Projektoplysninger<br>- Hurtig oprettelse af projekt| - Aktiv tilbudslinjedetalje<br>- Kombinerede tilbudslinjedetaljer<br>- Tilknyttet tilbudslinjedetalje |
|  Projektkontraktlinjedetalje|- Projektoplysninger<br>- Hurtig oprettelse af projekt|- Kombinerede kontraktlinjedetaljer<br>- Aktive kontraktlinjedetaljer<br>- Tilknyttet kontraktlinjedetaljer |
|  Projektopgave|- Oplysninger<br>- Ny formular| &nbsp; |
|  Medlem af projektteam|- Oplysninger<br>- Ny formular|- Aktive medlemmer af projektteam<br>- Projektteamets medlemmer<br>- Tilknyttede medlemmer af projektteam |
|  Tidsregistrering|- Oplysninger<br>- Opret tidsregistrering|- Mine tidsregistreringer efter dato<br>- Mine tidsregistreringer for denne uge<br>- Tidsregistreringer til godkendelse|
|  Kladdelinje|- Oplysninger<br>- Hurtig oprettelse|- Aktive kladdelinjer<br>- Visning for tilknyttet kladdelinje|
|  Fakturalinjedetalje|- Oplysninger<br>- Hurtig oprettelse|- Aktive fakturalinjedetaljer<br>- Fakturerbare fakturatransaktioner<br>- Gratis fakturatransaktioner<br>- Tilknyttede fakturalinjedetaljer <br>- Ikke-fakturerbare fakturatransaktioner|
|  Faktisk|- Oplysninger<br>- Aktive faktiske| Tilknyttet faktisk |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Konfigurer feltet Transaktionskategori som en prisfastsættelsesdimension

1. Gå til **Indstillinger** > **Parametre**. 
2. På siden **Parametre** skal du på fanen **Beløbsbaserede prisfastsættelsesdimensioner** godkende, at gitteret viser posterne i objektet **Prisfastsættelsesdimensioner**.
3. Tilføj **Transaktionskategorien** til denne liste, og angiv felterne **Gælder for Omkostning** og **Gælder for Salg** til **Ja**.
4. I feltet **Dimensionstype** skal du vælge **Beløbsbaseret** og derefter vælge den prioritet for **Transaktionskategori**, da det er relateret til omkostning og salg.


[!INCLUDE[footer-include](../includes/footer-banner.md)]