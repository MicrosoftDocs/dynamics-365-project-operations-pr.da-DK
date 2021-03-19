---
title: Administrer faktureringsefterslæbet
description: Dette emne indeholder oplysninger om, hvordan du kan få vist og arbejde med faktureringsefterslæbet i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287726"
---
# <a name="manage-the-billing-backlog"></a>Administrer faktureringsefterslæbet

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations har to dedikerede visninger, der kan hjælpe dig med at arbejde med og administrere faktureringsefterslæbet. De er **Fast pris-milepæle** og **Faktureringsefterslæb for tid og materiale** Hvis du vil vælge en visning, skal du i området **Salg** i Project Operations vælge **Fakturering** i venstre navigationsside. Links til faktureringsefterslæbet gemmes der.

## <a name="fixed-price-milestones"></a>Milepæle for fast pris

Her vises alle fast pris-milepæle på tværs af alle projektkontraktlinjer i systemet. Enkelte eller flere milepæle kan markeres som **Klar til fakturering** eller **Ikke-klar til fakturering** fra denne visning. Når du markerer en milepæl som **Klar til fakturering**, bliver milepælen tilgængelig for en kladdefaktura.

Når der er angivet en fast pris-faktureringsmetode for kontraktlinjer med flere kunder, oprettes der en milepæl for hver kunde på kontraktlinjen. Brugeren opretter en milepæl, og den pågældende milepæl opdeles i henhold til kunder = specifikke interne milepælsposter i henhold til den faktureringsprocentopdeling, der er defineret for de enkelte kunder på kontraktlinjen. I visningen **Fast pris-milepæle** kan du se de enkelte kundespecifikke milepælsposter. Hver af disse milepælsposter kan særskilt markeres som **Klar til fakturering** fra denne visning. Når en eller flere af de relaterede milepælsopdelinger er markeret som **Klar til fakturering**, konverteres overskriften til statussen **Igangværende** fra **Ikke påbegyndt**. Når alle milepælsopdelinger er blevet faktureret, bliver statussen for overskriftsmilepælen konverteret til **Fuldført**.

En milepæl på en kladdefaktura vises i denne visning med en faktureringsstatus angivet til **Kundefaktura oprettet**. Når kladdefakturaen er bekræftet, opdateres faktureringsstatussen for denne post til **Faktura er bogført**. Det anbefales ikke at opdatere denne statusværdi ved hjælp af brugerdefineret kode. Project Operations fungerer ikke korrekt, hvis disse statusværdier opdateres med brugerdefineret kode.

## <a name="time-and-material-billing-backlog"></a>Ordrebeholdning for fakturering af tid og materiale

I denne visning vises alle ikke-fakturerede faktiske salgsværdier, der ikke er blevet faktureret, på tværs af alle projektkontrakter i systemet. Enkelte eller flere ikke-fakturerede faktiske salgsværdier kan markeres som **Klar til fakturering** eller **Ikke-klar til fakturering** fra denne visning. Hvis du markerer en ikke-faktureret faktisk salgsværdi som **Klar til fakturering**, bliver den tilgængelig til brug i en kladdefaktura.

Ikke-fakturerede faktiske salgsværdier med en status med **Må ikke overskrides** angivet til **Mislykket** kan ikke markeres som **Klar til fakturering**. Hvis disse faktiske oplysninger skal markeres som sådanne, skal du nulstille statussen på andre faktiske oplysninger på den kontraktlinje, der er blevet bekræftet, og derefter evaluere statussen **Må ikke overskrides**.

Hvis der er tale om kontraktlinjer med flere kunder med faktureringsmetoden tid og materialer, oprettes der en ikke-faktureret salgsværdi for hver kunde på kontraktlinjen, når tid og udgifter godkendes, i henhold til faktureringsprocentopdelingen, der er defineret for de enkelte kunder på kontraktlinjen. I visningen **Faktureringsefterslæb for tid og materiale** kan du se de enkelte kundespecifikke ikke-fakturerede faktiske salgsværdier. Hver af disse ikke-fakturerede faktiske salgsposter kan særskilt markeres som **Klar til fakturering** fra denne visning.

En ikke-faktureret faktisk salgsværdi på en kladdefaktura vises i denne visning med en **Faktureringsstatus** angivet til **Kundefaktura oprettet**. Når kladdefakturaen er bekræftet, opdateres faktureringsstatussen for denne post til **Kundefaktura er bogført**. Det anbefales ikke at opdatere denne statusværdi, når den er i denne tilstand, ved hjælp af brugerdefineret kode. Project Operations fungerer ikke korrekt, når disse statusværdier opdateres med brugerdefineret kode.


[!INCLUDE[footer-include](../includes/footer-banner.md)]