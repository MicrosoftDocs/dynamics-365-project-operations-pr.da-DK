---
title: Bekræft en projektkontrakt
description: Denne artikel indeholder oplysninger om, hvordan du bekræfter en kontrakt i Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929989"
---
# <a name="confirm-a-project-contract"></a>Bekræft en projektkontrakt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

En projektkontrakt i Dynamics 365 Project Operations kan være aktiv med en årsag angivet til **Bekræftet** eller lukket med årsagen **Tabt**. Når du bekræfter en projektkontrakt, opdateres statussen fra **Kladde** til **Aktiv**, og statusårsagen angives til **Bekræftet**. En aktiv eller lukket kontrakt kan ikke redigeres eller genåbnes. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Økonomisk indvirkning af at bekræfte en projektkontrakt

Når en projektkontrakt er bekræftet, genberegner programmet omkostningerne ved at tilbageføre de gamle faktiske omkostninger og oprette nye faktiske omkostninger. De nye faktiske omkostninger behandles derefter baseret på faktureringsmetoden for den tilknyttede projektkontraktlinje. Hvis de faktiske omkostninger refererer til en tids- og materialekontraktlinje, opretter programmet automatisk tilsvarende ikke-fakturerede faktiske oplysninger for salg. Hvis de faktiske omkostninger refererer til en kontraktlinje med fast pris, holder programmet op med at behandle de faktiske omkostninger.

Grænser, der ikke må overskrides, konfiguration af fakturerbarhed og prisfastsættelse samt omkostningsfastsættelse på de faktiske oplysninger evalueres og opdateres derefter som en del af bekræftelsesprocessen.

## <a name="close-a-project-contract-as-lost"></a>Luk en projektkontrakt som tabt

Når du lukker en projektkontrakt som tabt, opdateres kontraktstatussen til **Lukket** og statusårsagen til **Tabt**. Projektkontrakten bliver skrivebeskyttet. Der vises en bekræftelsesdialogboks, før ændringerne fuldføres, fordi du ikke kan genåbne en lukket projektkontrakt.

Hvis den projektkontrakt, der lukkes som værende tabt, refererer til et projekt på de enkelte linjer, bliver det pågældende projekt også markeret som lukket. De ressourcereservationer, der er gældende fra den pågældende dag og fremefter, annulleres. Alle ikke-fakturerede faktiske salgsværdier i projektkontrakten, som ikke allerede er blevet faktureret, tilbageføres.

> [!NOTE]
> I Dynamics 365 Project Operations vil lukning af en projektkontrakt som tabt ikke påvirke denne status for den tilknyttede salgsmulighed. Salgsmuligheden er stadig åben og skal lukkes manuelt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]