---
title: Luk tilbud
description: Dette emne indeholder oplysninger om, hvordan du lukker et tilbud i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074093"
---
# <a name="close-quotes"></a>Luk tilbud 

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Et projekttilbud kan lukkes som vundet eller tabt. Operationerne Aktivér og Revider på tilbud understøttes ikke i Microsoft Dynamics 365 Project Operations, hvorfor et tilbud i kladdeform kan lukkes.

## <a name="close-a-quote-as-won"></a>Luk et tilbud som vundet

Hvis du lukker et projekttilbud som vundet, lukkes tilbuddet med statussen Lukket, og statusårsagen angives til Vundet. Når du lukker tilbuddet, skrivebeskyttes projektilbuddene, og der oprettes en kladde med et udkast til projektkontrakt med tilbudsoplysningerne. Da et lukket tilbud ikke kan genåbnes, vises der en bekræftelsesdialogboks i dialogboksen, før ændringerne er foretaget, da et lukket tilbud ikke kan åbnes igen, og ændringerne ikke kan fortrydes.

Hvis tilbuddet er knyttet til en salgsmulighed, lukkes eventuelle andre projekttilbud på salgsmuligheden automatisk som tabt.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Økonomiske konsekvenser af at lukke et tilbud som vundet

Hvis der har været faktiske oplysninger for den tid, der er registreret på et projekt, mens det stadig er knyttet til et kladdetilbud, registreres kun omkostningerne for tiden eller udgiften. Når et tilbud er lukket som vundet, vil programmet omstrukturere omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger. Programmet behandler de faktiske omkostninger baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje. Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, oprettes der automatisk tilsvarende faktiske ikke-fakturerede salg for tidspunktet, hvor tilbuddet blev lukket, og projektkontrakten oprettes i systemet. Hvis der henvises til omkostningerne i forbindelse med en fastpriskontraktlinje, stopper programmet med at genbehandle de faktiske omkostninger på baggrund af reglerne for opdeling af fakturering for projektkontraktkunderne.

## <a name="closing-a-quote-as-lost"></a>Lukning af et tilbud som tabt:

Hvis du lukker et projekttilbud som tabt, angives status til Lukket, og statusårsag til Tabt. Hvis du lukker tilbuddet, bliver projekttilbuddet skrivebeskyttet. Da et lukket tilbud ikke kan genåbnes, før du lukker et tilbud, vil en bekræftelsesdialogboks bekræfte ændringerne.

Hvis det projekttilbud, der er lukket som tabt, er et projekt, der refereres til på nogen af sine linjer, er det projekt også markeret som lukket, og eventuelle ressourcereservationer fra den pågældende dag annulleres.

> [!NOTE]
> Hvis du lukker et tilbud som vundet eller tabt i Project Operations, påvirkes statussen for salgsmuligheden ikke, og den vil være åben, indtil den lukkes manuelt.
