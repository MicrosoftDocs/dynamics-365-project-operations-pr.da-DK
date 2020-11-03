---
title: Bekræft en projektkontrakt
description: Dette emne indeholder oplysninger om, hvordan du bekræfter en kontrakt i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074292"
---
# <a name="confirm-a-project-contract"></a>Bekræft en projektkontrakt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

En projektkontrakt i Dynamics 365 Project Operations kan være aktiv med en årsag angivet til **Bekræftet** eller være lukket med en årsag angivet til **Tabt**. Når du bekræfter en projektkontrakt, opdateres statussen fra **Kladde** til **Aktiv** , og statusårsagen angives til **Bekræftet**. En aktiv eller lukket kontrakt kan ikke redigeres eller genåbnes. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Økonomisk indvirkning af at bekræfte en projektkontrakt

Når en projektkontrakt er bekræftet, genberegner programmet omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger. De nye faktiske omkostninger behandles derefter baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje. Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, opretter programmet automatisk tilsvarende ikke-fakturerede faktiske oplysninger for salg. Hvis de faktiske omkostninger refererer til en kontraktlinje med fast pris, holder programmet op med at behandle de faktiske omkostninger.

Grænser, der ikke må overskrides, konfiguration af fakturerbarhed og prisfastsættelse samt omkostningsfastsættelse på de faktiske oplysninger evalueres og opdateres derefter som en del af bekræftelsesprocessen.

## <a name="close-a-project-contract-as-lost"></a>Luk en projektkontrakt som tabt

Når du lukker en projektkontrakt som tabt, opdateres kontraktstatussen til **Lukket** og statusårsagen til **Tabt**. Projektkontrakten bliver skrivebeskyttet. Der vises en bekræftelsesdialogboks, før ændringerne fuldføres, fordi du ikke kan genåbne en lukket projektkontrakt.

Hvis den projektkontrakt, der lukkes som værende tabt, refererer til et projekt på de enkelte linjer, bliver det pågældende projekt også markeret som lukket. De ressourcereservationer, der er gældende fra den pågældende dag og fremefter, annulleres. Alle ikke-fakturerede faktiske salgsværdier i projektkontrakten, som ikke allerede er blevet faktureret, tilbageføres.

> [!NOTE]
> I Dynamics 365 Project Operations påvirkes statussen for den tilknyttede salgsmulighed ikke ved, at du lukker et projekt som værende tabt. Salgsmuligheden er stadig åben og skal lukkes manuelt.
