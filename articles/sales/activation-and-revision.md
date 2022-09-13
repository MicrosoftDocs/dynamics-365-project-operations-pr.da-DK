---
title: Aktivere og revidere et projekttilbud
description: Denne artikel indeholder oplysninger om, hvordan du aktiverer og reviderer tilbud i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410316"
---
# <a name="activate-and-revise-a-project-quote"></a>Aktivere og revidere et projekttilbud

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan bruge aktiverings- og revisionsfunktioner til at holde styr på versionerne for projektbaserede tilbud i estimerings- og forhandlingsfaserne. Når en kladde til et tilbud aktiveres, bliver den skrivebeskyttet.

Aktiverings- og revisionsfunktionerne giver dig mulighed for at udføre følgende opgaver:

- Først vinde eller miste tilbud efter aktivering.
- Revidere et tilbud for enten at foretage ændringer af det eksisterende tilbud eller oprette en ny version.

> [!NOTE]
> Når funktionen til aktivering og revision af tilbud er aktiveret, kan den ikke deaktiveres.

Følg disse trin for at aktivere og revidere projektbaserede tilbud.

1. Gå til **Indstillinger** \> **Parametre**.
1. Åbn posten **Parametre**.
1. Vælg **Aktivér aktivering og revisioner af tilbud** under fanen **Funktionskontrol** i handlingsruden.
1. Vælg **OK** i bekræftelsesdialogboksen.
1. Efter et øjeblik skal du opdatere browseren. Aktiverings- og revisionsfunktionerne skulle nu være tilgængelige. Du ved, at disse funktioner er aktiveret, hvis knappen **Aktivér aktivering og revisioner af tilbud** ikke længere vises i handlingsruden.

## <a name="activating-a-quote"></a>Aktivering af et tilbud

Når funktionen til aktivering og revision af tilbud er aktiveret, er knapperne **Luk tilbud som vundet** og **Luk tilbud som tabt** i handlingsruden ikke tilgængelige for kladdeprojekttilbud. De er først tilgængelige, når et tilbud er aktiveret.

Aktivering repræsenterer fasen i tilbudsprocessen, når du vil forhindre flere ændringer af tilbuddet. På nuværende tidspunkt sendes tilbuddet til intern gennemgang eller til kunden.

Knapperne **Luk tilbud som vundet** og **Luk tilbud som tabt** i handlingsruden er tilgængelige for aktiverede tilbud. Afhængigt af resultatet af den interne gennemgang eller kundegennemgang kan du bruge en af disse knapper til at lukke et aktiveret tilbud. Du kan foretage forhandlinger og ændringer af aktiverede tilbud ved at vælge **Revider tilbud**.

## <a name="revising-a-quote"></a>Revidering af et tilbud

Hvis du skal foretage ændringer af et aktiveret tilbud, skal du vælge **Revider tilbud**. Tilbuddet lukkes, og årsagskoden **revideret** bruges. Der oprettes derefter et nyt tilbud, der har samme id og et højere revisionsnummer. Alle detaljer fra det oprindelige tilbud kopieres til det nye tilbud. Det nye tilbud er i kladdestatus og kan redigeres efter behov.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
