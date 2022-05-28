---
title: Leverandørfaktura – koncept og oprettelse
description: I dette emne beskrives begrebet leverandørfakturaer, scenarier for brug, og hvordan du kan oprette leverandørfakturaer i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580541"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Leverandørfaktura – koncept og oprettelse

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Fakturering af leverandører i Microsoft Dynamics 365 Project Operations kan bruges til at registrere omkostninger fra leveringer af tjenester og/eller materialer på et projekt efter leverandør.

Når tjenester og/eller materialer udbydes til en underleverandør, repræsenterer en underentreprise den kontraktmæssige aftale med den pågældende leverandør. Når leverandøren leverer tjenesten, eller materialerne modtages og bruges på projektopgaver, registreres omkostningerne for projektet. Leverandøren sender jævnligt fakturaer, der er kontrolleret og sammenholdt med de omkostninger, der er registreret for projektet. Når bekræftelsesprocessen er fuldført, bekræftes og frigives leverandørfakturaen til betaling.

## <a name="scenarios-for-use"></a>Scenarier for brug

Leverandørfakturaer i Project Operations kan bruges til at understøtte to separate scenarier.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunder bruger alle erfaringer med underleverandører

Erfaringer med leverandørfakturaer gør det muligt at kontrollere og tilpasse tidsposter, materialeforbrug og udgifter, som refererer til komponenter fra underleverandører med leverandørfakturalinjer. Denne proces kan bruges til at kontrollere, om leverandørfakturalinjerne er korrekte. Når verifikationsprocessen er fuldført, og leverandørfakturaen er bekræftet, modposteres de faktiske værdier, der blev registreret ved hjælp af godkendte tids-, udgifts- og materialeforbrugslogfiler, og der oprettes nye faktiske omkostninger ved hjælp af leverandørfakturalinjer.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunder bruger ikke alle erfaringer fra underleverandører, men vil have et ensartet billede af omkostningerne til projekter i Project Operations

Hvis du sporer underentrepriseprocessen i et tredjepartssystem, kan du registrere omkostninger fra det pågældende tredjepartssystem i Project Operations ved at oprette leverandørfakturaer, der ikke refererer til underentrepriser. På denne måde kan dine projektledere få én samlet visning af alle omkostninger for et bestemt projekt.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Oprettelse af leverandørfakturaer i Project Operations

Leverandørfakturaer kan oprettes på to måder:

- Fra listesiden for leverandørfakturaer eller detaljesiden for en enkelt leverandørfaktura
- Fra listesiden for underentrepriser eller detaljesiden for en enkelt underentreprise

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Oprettelse fra listesiden for leverandørfakturaer eller siden med detaljer

1. Gå til **Køb** \> **Leverandørfakturaer**.
2. På listesiden for leverandørfakturaer eller detaljesiden for en enkelt leverandørfaktura skal du vælge **Ny** for at oprette en ny leverandørfaktura.

De leverandørfakturaer, der oprettes på denne måde, kan også henvise til en underentreprise.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Oprettelse fra listesiden for en underentreprise eller siden med detaljer

1. Gå til **Køb** \> **Underleverandører**.
2. Vælg én eller flere underentrepriser.
3. På listesiden for underentrepriser eller detaljesiden for en enkelt underentreprise skal du vælge **Opret leverandørfaktura** for at oprette en ny leverandørfaktura.

Der oprettes en ny leverandørfaktura i statussen **Kladde** for hver underentreprise, du har valgt.

De leverandørfakturaer, du opretter på denne måde, henviser altid til underentreprisen i overskriften på leverandørfakturaen. Hver linje i underentreprisen, der har en tids- og materialefaktureringsmetode, medfører, at der oprettes en linje på leverandørfakturaen. Hver linje i underentreprisen, der har en fast pris-faktureringsmetode, medfører, at der oprettes en linje på leverandørfakturaen for alle milepæle på underentrepriselinjen, der har statussen **Klar til at fakturere**.

Følgende felter og relaterede poster kopieres fra underentreprisen til overskriften på leverandørfakturaen:

- Leverandør.
- Relaterede prislister kopieres til leverandørfakturaen som prislister.
- Valuta.
- Kontraktenhed.
- Betalingsbetingelser.

I forbindelse med tids- og materialekontraktlinjer kopieres følgende felter og relaterede poster fra underentrepriselinjen til leverandørfakturalinjen:

- Referencer til underentrepriser og underentrepriselinjer
- Transaktionsklasse
- Rolle
- Transaktionskategori
- Produktfelter
- Project
- Opgave
- Reserverbar ressource

I forbindelse med underentrepriselinjer for fast pris kopieres følgende felter fra underentrepriselinjen og underentrepriselinjemilepæle til leverandørfakturalinjen:

- Referencer til underentrepriser og underentrepriselinjer.
- Transaktionsklasse. Værdien er som standard **Milepæl**.
- Navnet på og beløbet for milepælen kopieres fra den relaterede underentrepriselinjemilepæl.
- Brugeren kan vælge et projekt og en opgave på leverandørfakturalinjen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
