---
title: Lukke et tilbud
description: Dette emne indeholder oplysninger om, hvordan du lukker tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898884"
---
# <a name="close-a-quote"></a>Lukke et tilbud

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Et projekttilbud kan lukkes som vundet eller tabt. Da funktionerne Aktivér og Revider ikke understøttes i tilbud i Microsoft Dynamics 365 Project Operations, kan du lukke et tilbud i kladdeform.

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
