---
title: Lukke et tilbud
description: Dette emne indeholder oplysninger om, hvordan du lukker tilbud i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2314444dfdbd4d1a2f38c7de55e2070011e51a86f1e074dd6667d54393c641fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993414"
---
# <a name="close-a-quote"></a>Lukke et tilbud

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Et projekttilbud kan lukkes som vundet eller tabt. Da funktionerne Aktiver og Revider ikke er understøttet for tilbud i Microsoft Dynamics 365 Project Operations, kan du lukke en tilbudskladde.

## <a name="close-a-quote-as-won"></a>Luk et tilbud som vundet

Hvis du lukker et projekttilbud som vundet, angives tilbuddets status til **Lukket**, og statusårsag til **Vundet**. Når du lukker tilbud, skrivebeskyttes de, og der oprettes en kladde med et udkast til projektkontrakt med alle tilbudsoplysninger. Da et lukket tilbud ikke kan genåbnes, før du lukker et tilbud, vil en bekræftelsesdialogboks bekræfte ændringerne.

Den projektkontrakt, der er oprettet ud fra et projekttilbud, gøres også tilgængelig i modulet Projektstyring og regnskab i Project Operations. Hvis en projektkontrakt ikke er knyttet til et projekt på nogen af sine linjer, gøres denne projektkontrakt tilgængelig som en inaktiv projektkontrakt, og den bliver aktiv, så snart der er knyttet et projekt til mindst en af kontraktlinjerne.

Hvis tilbuddet er knyttet til en salgsmulighed, lukkes eventuelle andre projekttilbud på salgsmuligheden automatisk som tabt.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Økonomiske konsekvenser af at lukke et tilbud som vundet

Hvis der har været faktiske oplysninger for den tid, der er registreret på et projekt, mens det stadig er knyttet til et kladdetilbud, registreres kun omkostningerne for tiden eller udgiften. Når et tilbud er lukket som vundet, vil programmet omstrukturere omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger. Programmet behandler de faktiske omkostninger baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje. Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, oprettes der automatisk tilsvarende faktiske ikke-fakturerede salg for tidspunktet, hvor tilbuddet blev lukket, og projektkontrakten oprettes i systemet. Hvis der henvises til omkostningerne i forbindelse med en fastpriskontraktlinje, stopper programmet med at genbehandle de faktiske omkostninger på baggrund af reglerne for opdeling af fakturering for projektkontraktkunderne.

Alle genindhentede faktiske oplysninger er tilgængelige i modulet Projektstyring og regnskab, så projektbogholderen kan gennemgå, opdatere og bogføre dem i finanskladden. 

## <a name="close-a-quote-as-lost"></a>Luk et tilbud som tabt

Hvis du lukker et projekttilbud som tabt, angives status til **Lukket**, og statusårsag til **Tabt**. Når tilbuddet lukkes, er det skrivebeskyttet. Da et lukket tilbud ikke kan genåbnes, før du lukker et tilbud, vil en bekræftelsesdialogboks bekræfte ændringerne.

Hvis det projekttilbud, der er lukket som tabt, er et projekt, der refereres til på nogen af sine linjer, er det projekt også markeret som lukket, og eventuelle ressourcereservationer fra den pågældende dag annulleres.

> [!NOTE]
> Hvis du lukker et tilbud som vundet eller tabt i Project Operations, påvirkes statussen for salgsmuligheden ikke, og den vil være åben, indtil den lukkes manuelt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]