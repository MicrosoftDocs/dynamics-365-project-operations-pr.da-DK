---
title: Varekrav for projektkontrakter med flere finansieringskilder
description: Denne artikel indeholder oplysninger om, hvordan du konfigurerer og bruger varekrav med flere finansieringskilder.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028466"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Varekrav for projektkontrakter med flere finansieringskilder

_**Gælder for:** Project Operations for lagerbaserede/produktionsbaserede scenarier_

I visse kontraktmæssige aftaler for projektbaserede leverancer kan der være brug for flere finansieringskilder. I denne artikel forklares det, hvordan du vælger og konfigurerer de ønskede finansieringskilder, når der kræves flere kilder i forbindelse med et projekt eller en projektkontrakt.

## <a name="terminology"></a>Terminologi

- **Finansieringskilde** – Det objekt, der finansierer projektkontraktarbejdet. Dette objekt kan være en intern organisation eller en ekstern fakturakonto (kunde eller tildeling).
- **Projektkunde** – Det objekt, som projektarbejdet leveres til.
- **Fakturakonto** – Det eksterne objekt, der betaler for projektarbejdet.

## <a name="example"></a>Eksempel

Contoso har vundet en kontrakt om fornyelse af udstyr med to af sine kunder: Adaudstyr USA og Adaudstyr Corporate. Kontrakten omfatter hardware- og installationsservicer, der leveres til Adafiler USA (projektkunden). Hardwaren skal anvendes af Adaplatform Corporate (fakturakonto 1), og installationsarbejdet vil blive faktureret af Adafiler US (fakturakonto 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Konfigurer standardregler for fakturakonti for varekrav

### <a name="prerequisites"></a>Forudsætninger

- Microsoft Dynamics 365 Finance **version 10.0.27 eller nyere** er påkrævet for at bruge varekrav, der har flere fakturakonti.
- Din systemadministrator skal aktivere kravene til funktionen **Tillad varekrav med flere finansieringskilder til Project Operations i lager-/produktionsbaserede scenarier** i arbejdsområdet **Funktionsstyring**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Konfigurer standardregler for fakturakontoen

Hvis du vil konfigurere standardreglerne for fakturakontoen, skal du følge disse trin.

1. Gå til **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.
1. På fanen **Generelt** skal du i afsnittet **Salgsordre og flere varekrav** angive muligheden **Tillad projekter med flere finansieringskilder** til **Ja**.
1. I feltet **Standardkunde** skal du angive, hvor projektleveringskunden på varekravet kommer fra som standard:

    - **Fra finansieringskilde** – Standardleveringskunden kommer fra finansieringskilden. Hvis der knyttes flere finansieringskilder til projektkontrakten, anvendes den første finansieringskilde på listen.
    - **Fra projekt** – Standardkunden til projektlevering kommer fra den kunde, der er valgt i feltet **Projektpostkonto**.

1. Valgfrit: Angiv eller ændr standardfakturakontoen for projektposter:

    1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**, og åbn projektpostdetaljerne.
    2. På fanen **Generelt** skal du angive eller opdatere feltet **Standardfakturakonto**. Den konto, som du angiver, bruges som standardfakturakonto for nye varekrav, der oprettes for projektet. Hvis feltet ikke udfyldes, bruges fakturakontoen for den første finansieringskilde til projektkontrakten som standard. Brugere kan dog ændre kontoen, når de gemmer posten.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Vælg den fakturakonto, der skal bruges, når du opretter et varekrav

Hvis du vil vælge den fakturakonto, der skal bruges, når du opretter et varekrav, skal du følge disse trin.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**, og vælg projektposten.
1. På fanen **Plan** skal du vælge **Varekarv**.
1. Opret en ny post for varekrav.

    - Feltet **Fakturakonto** i posten angives som standard til det fakturakonto, der er angivet for projektet. Du kan ændre værdien i feltet **Fakturakonto** og derefter gemme posten. Når posten er gemt, kan du ikke længere opdatere værdien for **Fakturakontoen**. Hvis du skal opdatere værdien for **Fakturakontoen** for varekravet, skal du slette det eksisterende varekrav og derefter oprette et nyt, der har den ønskede værdi.
    - Feltet **Kunde** for varekravet er som standard angivet på grundlag af værdien **Standardkunde**, der fremgår af siden **Parametre for projektstyring og regnskab**.

    Når varekravsposten gemmes, knytter systemet den sammen med overskriftsposten **Varekrav til salgsordre**. Hvis der ikke er valgt en åben overskrift for salgsordre for det valgte fakturakonto, opretter systemet en, og varekravslinjen knyttes til det.

> [!NOTE]
> Varekrav faktureres altid fuldt ud til det fakturakonto, der er angivet i posten. Systemet understøtter i øjeblikket ikke finansieringsfordeling, der har varekrav, og det vil ikke opdele bogføringen på baggrund af konfigurationen af finansieringstildelingsregler.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Opret et varekrav ud fra en vareprognoserapport

Hvis du vil oprette et varekrav ud fra en vareprognosepost, skal du følge disse trin.

1. Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**, og vælg projektposten.
1. På fanen **Plan** skal du vælge **Vareprognoser**.
1. Opret en ny vareprognosepost.
1. Valgfrit: På fanen **Projekt** skal du i feltet **Finansieringskilde** vælge den ønskede fakturakonto.
1. Vælg **Opret varekarv**, og bekræft den meddelelse, du modtager.

    > [!NOTE]
    > I systemet kopieres værdien **Finansieringskilde** fra vareprognoseposten til den nyligt oprettede varekravspost.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Standardfakturakonto, når systemet automatisk opretter et varekrav fra en købsordrelinje

Hvis indstillingen **Opret varekrav** er angivet til **Ja** på siden **Projektstyring og regnskabsparametre**, oprettes der automatisk et varekrav, når en ny projektordrelinje gemmes. Felterne **Fakturakonto** og **Varekrav** angives som standard til værdien i feltet **Standardfakturakonto** i projektposten. Systemet understøtter i øjeblikket ikke opdatering eller ændring af fakturakontoen for poster af denne type.
