---
title: Lukke projekttilbud
description: Denne artikel indeholder oplysninger om at lukke et tilbud i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826168"
---
# <a name="close-project-quotes"></a>Lukke projekttilbud

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Et projekttilbud kan lukkes som vundet eller tabt. Et kladdetilbud kan lukkes, fordi handlingerne Aktivér og Revider på tilbud ikke understøttes i Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Luk et tilbud som vundet

Når du lukker et projekttilbud som Vundet, angives status til Lukket, og statusårsagen er Vundet. Når du lukker tilbuddet, skrivebeskyttes projektilbuddene, og der oprettes en kladde med et udkast til projektkontrakt med tilbudsoplysningerne. Da et lukket tilbud ikke kan åbnes igen, bekræfter en bekræftelsesdialog dine ændringer.

Hvis tilbuddet er knyttet til en salgsmulighed, lukkes eventuelle andre projekttilbud på salgsmuligheden automatisk som tabt.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Økonomiske konsekvenser af at lukke et tilbud som vundet

Hvis der er faktiske oplysninger om tid på et projekt, mens der stadig er tilknyttet et kladdetilbud, registreres kun omkostningerne ved tid eller udgifter. Når et tilbud er lukket som vundet, vil programmet omstrukturere omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger. Programmet behandler de faktiske omkostninger baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje. Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, oprettes der tilsvarende ikke-fakturerede faktiske salgsværdier for, hvornår tilbuddet lukkes, og projektkontrakten oprettes. Hvis de faktiske omkostninger refererer til en fastpriskontraktlinje, stopper programmet med at genbehandle de faktiske omkostninger, der er baseret på de opdelte faktureringsregler for projektkontraktkunderne.

## <a name="closing-a-quote-as-lost"></a>Lukke et tilbud som tabt

Når du lukker et projekttilbud som Tabt, angives status til Lukket, og statusårsagen er Tabt. Hvis du lukker tilbuddet, bliver projekttilbuddet skrivebeskyttet. Da et lukket tilbud ikke kan genåbnes, før du lukker et tilbud, vil en bekræftelsesdialogboks bekræfte ændringerne.

Hvis det projekttilbud, der er lukket som Tabt, refererer til et projekt på en af dets linjer, markeres projektet også som Lukket. De ressourcereservationer, der er gældende fra den pågældende dag og fremefter, annulleres.

> [!NOTE]
> Hvis du lukker et tilbud som vundet eller tabt i Project Operations, påvirkes statussen for salgsmuligheden ikke, og den vil være åben, indtil den lukkes manuelt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
