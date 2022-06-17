---
title: Overvejelser om opgradering i forbindelse med moderne godkendelser
description: I denne artikel omtales de punkter, som administratorer skal overveje, når de aktiverer funktionaliteten for moderne godkendelser.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931737"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Overvejelser om opgradering i forbindelse med moderne godkendelser 

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Som en del af første bølge af udgivelsen fra april 2022 aktiveres funktionen moderne godkendelser som standard. Denne funktion forbedrer pålideligheden af godkendelseslogikken og sikrer, at du kan fastslå årsagen, hvis godkendelseslogikken mislykkes.

Som en del af denne ændring opdateres statusændringer for projektgodkendelser. Statussen går nu direkte fra **Indsendt** til **Godkendt**. **Afventende** er ikke længere en status for godkendelser. For at afgøre, om en godkendelse er afventende, skal du kontrollere, at godkendelsen er en del af et godkendelsessæt, og gennemse tilstanden for det vedhæftede godkendelsessæt.

## <a name="before-you-upgrade"></a>Før du opgraderer

Før du opgraderer til moderne godkendelser, skal du sikre dig, at der ikke er nogen afventende godkendelser. Moderne godkendelser bruger ikke statussen **Afventer**. Eventuelle godkendelser, der stadig er markeret som **Afventende** efter opgraderingen, behandles derfor ikke.

## <a name="after-you-upgrade"></a>Efter din opgradering

Når du har opgraderet til moderne godkendelser, skal en administrator kontrollere, at det cloudflow, der behandler godkendelser, er aktiveret.

1. Log på [flow.microsoft.com](https://flow.microsoft.com)
2. Skift dit miljø til det miljø, som du har opgraderet, øverst til højre på siden.
3. Vælg **Løsninger** for at få vist en liste over de løsninger, der installeres i miljøet.
4. Vælg **Project Operations** eller **Project Service** på løsningslisten.
5. Skift filteret fra **Alle** til **Cloudflow**.
6. Kontrollér, at indstillingen **Project Service – Planlæg tilbagevendende projektgodkendelsessæt** er angivet til **Til**. Hvis det ikke er det, skal du vælge flowet og derefter vælge **Slå til**.
7. Kontrollér, at behandlingen sker hvert femte minut, ved at gennemse listen **Systemjob** i området **Indstillinger**.

## <a name="short-term-rollback"></a>Kortsigtet tilbagerulning

Hvis du ikke kan rumme ændringerne, eller hvis du støder på et stort problem med denne funktion, kan du midlertidigt vende tilbage til det oprindelige godkendelsesforløb ved at udføre følgende trin:
1. Log på dit miljø, og kontrollér, at der ikke er nogen afventende godkendelser.
2. Gå til **Indstillinger** > **Projektparametre**.
3. Vælg **Funktionskontrol,** og vælg derefter **Moderne godkendelser** for at slå funktionen fra.

## <a name="removing-the-feature-flag"></a>Fjerne funktionsflaget

I opdateringen med anden bølge i oktober 2022 fjernes muligheden for at slå denne funktion fra.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
