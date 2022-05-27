---
title: Standarder for økonomiske dimensioner
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer standarder for økonomiske dimensioner.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9f43fed57a1411a55dcd7929f34e87aed136a6b5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579483"
---
# <a name="financial-dimension-defaults"></a>Standarder for økonomiske dimensioner

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_



Dynamics 365 Project Operations bruger rammen [Økonomiske dimension](/dynamics365/finance/general-ledger/financial-dimensions) i Dynamics 365 Finance til at give yderligere indsigt i delregnskaber for projekter og hovedbogstransaktioner.

Økonomiske standarddimensioner kan angives for en kunde, et projekts finansieringskilde, en milepæl, en projektkontraktlinje eller et projekt.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definer økonomiske standarddimensioner for en kunde

Standardværdier for kundedimensioner angives i Finance. Gennemfør følgende trin for at konfigurere dimensionsstandarder .

1. Gå til **Debitor** > **Kunder** > **Alle kunder**.
2. På siden **Kunder** skal du på fanen **Økonomiske dimensioner** angive de økonomiske dimensionsværdier for bestemte kunder.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definer økonomiske standarddimensioner for projektkontrakter

Projektkontrakter oprettes og vedligeholdes i Common Data Service (CDS). Regnskabsattributter for projektkontrakter angives i modulet **Projektstyring og regnskab** i Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Angiv økonomiske dimensioner for en finansieringskilde for et projekt

1. Gå til **Projektstyring og regnskab** > **Projekter** > **Projektkontrakter**.
2. Vælg den post, som du vil opdatere, og på fanen **Projektkontrakt** skal du vælge **Vis standardregnskab**.
3. Udvid **Relaterede oplysninger**, og vælg fanen **Finansieringskilder**.
4. Angiv standarderne for økonomiske dimensioner. Bemærk, at de økonomiske dimensioner hentes som standard fra kundekontoen.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Angiv økonomiske dimensioner for en projektkontraktlinje

1. Gå til **Projektstyring og regnskab** > **Projekter** > **Projektkontrakter**.
2. Vælg den post, som du vil opdatere, og på fanen **Projektkontrakt** skal du vælge **Vis standardregnskab**.
3. Udvid **Relaterede oplysninger**, og vælg fanen **Kontraktlinjer**.
4. Angiv standarderne for økonomiske dimensioner. Standarderne for den økonomiske dimension er gældende og kan kun bruges sammen med kontraktlinjer med fast pris (milepæl).

Disse standardindstillinger bruges på relaterede linjer for aconto transaktioner for projekt og fakturaer.

## <a name="define-default-financial-dimensions-for-projects"></a>Definer økonomiske standarddimensioner for projekter

Projekter oprettes og vedligeholdes i CDS. Regnskabsattributter for projekter angives i modulet **Projektstyring og regnskab** i Finance.

1. Gå til **Projektstyring og regnskab** > **Projekter** > **Alle projekter**.
2. Vælg den post, som du vil opdatere, og på fanen **Projekt** skal du vælge **Vis standardregnskab**.
3. Udvid **Relaterede oplysninger**, og vælg fanen **Opsætning**.
4. Angiv standarderne for økonomiske dimensioner. Bemærk, at økonomiske dimensioner hentes som standard fra kundekontoen. Hvis projektet er knyttet til en kontraktlinje med flere projektkontraktkunder, bruges den primære kunde som standard som den økonomiske dimensioner.

Projektets standarder for økonomiske dimensioner bruges til at angive standarder for kladdelinjer for tid, udgifter og gebyrtransaktioner i **Integrationskladden i Project Operations** og på relaterede projektfakturalinjer.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
