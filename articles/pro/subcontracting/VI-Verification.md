---
title: Kontrol af leverandørfakturaer med godkendte faktiske værdier
description: I dette emne forklares det, hvordan Microsoft Dynamics 365 Project Operations lader projektledere kontrollere leverandørfakturaer med de faktiske værdier, der blev godkendt som arbejde, der er udført af kontraktansatte, og som disse har registrert tid for, og de udgifter og materiale, der blev brugt af medlemmer af projektteamet.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585463"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Kontrol af leverandørfakturaer med godkendte faktiske værdier

[!include [banner](../../includes/dataverse-preview.md)]

**Gælder for:** Lille udrulning - aftale om proformafakturering

Microsoft Dynamics 365 Project Operations lader projektledere kontrollere leverandørfakturalinjer på følgende måder:

- Brug feltet **Verificeringsstatus** på leverandørfakturalinjerne.
- Hvis leverandørfakturalinjerne refererer til en underentrepriselinje, skal du knytte de faktiske omkostninger fra underleverandøraktiviteten til de pågældende leverandørfakturalinjer. Linket oprettes ved at sammenholde de faktiske omkostninger med leverandørfakturalinjerne.

    > [!NOTE]
    > Selvom bekræftelsesstatus kan spores for leverandørfakturalinjer, der ikke refererer til en underentreprise, kan de faktiske omkostninger ikke knyttes til de pågældende leverandørfakturalinjer.

## <a name="verification-status"></a>Bekræftelsesstatus

feltet **Verificeringsstatus** på en leverandørfakturalinje angiver denne status for verifikationen. Følgende statusser understøttes:

1. Ikke startet
2. I gang
3. Afsluttet

Leverandørfakturalinjer med en verifikationsstatus som **Ikke påbegyndt** kan redigeres.

Leverandørfakturalinjer med en verifikationsstatus som **Igangværende** kan ikke længere redigeres. For en leverandørfakturalinje, der refererer til en underentreprise, angives verifikationsstatussen automatisk til **Igangværende**, så snart den første faktiske omkostning er afstemt med leverandørfakturalinjen.

Leverandørfakturalinjer med en verifikationsstatus som **Fuldført** kan ikke længere redigeres. Når alle leverandørfakturalinjerne har denne verifikationsstatus, kan leverandørfakturaen bekræftes.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Afstem faktiske omkostninger med leverandørfakturalinjer

Afstemning af faktiske omkostninger kan hjælpe dig med bekræftelsesprocessen på en leverandørfakturalinje. Hvis du vil tilpasse de faktiske omkostninger til en leverandørfakturalinje, skal du følge disse trin.

1. Åbn leverandørfakturalinjen, og vælg fanen **Ikke-afstemte faktiske omkostninger**. I et gitter vises en liste over faktiske omkostninger, der refererer til samme underentrepriselinje som leverandørfakturalinjen.
2. Vælg en eller flere faktiske omkostninger, og vælg derefter **Afsted** på værktøjslinjen over gitteret. Det kontrolleres, at de valgte faktiske omkostninger kan afstemmes. Når valideringen er gennemført, knyttes de faktiske omkostninger til leverandørfakturalinjen.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Valideringskriterier, der bruges til at knytte faktiske omkostninger til leverandørfakturalinjer

Under afstemningsprocessen kan der kun oprettes et link mellem en faktisk omkostning og en leverandørfakturalinje, hvis begge følgende betingelser er opfyldt:

- Feltet **Justeringsstatus** for alle valgte faktiske omkostninger skal være tomt. De faktiske omkostninger må med andre ord ikke være erstattet af andre faktiske omkostninger under en proces med tilbagekaldelse, godkendelse, annullering eller rettelser af kladden.
- Værdierne i følgende felter afstemmes mellem leverandørfakturalinjen og de valgte faktiske omkostninger. Hvis et bestemt felt ikke er angivet på leverandørfakturalinjen, tages der ikke hensyn hertil ved afstemning.

    - Projektkontrakt
    - Projektkontraktlinje
    - Transaktionsklasse
    - Project
    - Opgave
    - Ressourcekategori
    - Transaktionskategori
    - Produkt
    - Underentrepriselinje
    - Reserverbar ressource

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Ikke-afstemte faktiske omkostninger fra en leverandørfakturalinje

Manglende afstemning af faktiske omkostninger, kan det også gøre det lettere at kontrollere en leverandørfaktura ved at gøre det muligt at fjerne tidligere oprettede links. Afstemningen af faktiske omkostninger kan kun fjernes fra leverandørfakturalinjer, der har bekræftelsesstatussen **Igangværende**. Hvis du vil fjerne afstemningen af faktiske omkostninger med en leverandørfakturalinje, skal du følge disse trin.

1. Åbn leverandørfakturalinjen, og vælg fanen **Afstemte faktiske omkostninger**. I et gitter vises en liste over faktiske omkostninger, der refererer til leverandørfakturalinjen.
2. Vælg en eller flere faktiske omkostninger, og vælg derefter **Fjern afstemning** på værktøjslinjen over gitteret.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
