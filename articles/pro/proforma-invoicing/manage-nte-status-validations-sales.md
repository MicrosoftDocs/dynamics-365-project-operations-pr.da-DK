---
title: Administrer status, som ikke må¨overskrides, og valideringer
description: Dette emne oplysninger om de kontroller for grænse, der ikke må overskrides, som udføres i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274005"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Administrer status, som ikke må¨overskrides, og valideringer 

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

## <a name="not-to-exceed-on-approvals"></a>Grænse, der ikke må overskrides i forbindelse med godkendelser

Når der sendes en tids- eller udgiftspost, oprettes der en godkendelsespost. Hvis godkendelsen kan faktureres og tilknyttes en kontraktlinje for tid og materialer, gennemfører systemet en valideringskontrol af grænsen, der ikke må overskrides, på følgende niveauer:

  - Kontrol i forhold til den konfigurerede grænse for kunden på projektkontraktlinjen
  - Kontrol i forhold til den konfigurerede grænse på kontraktlinjen
  - Kontrol i forhold til den konfigurerede grænse for kunden
  - Kontrol i forhold til den konfigurerede grænse på kontrakten

Kontrollerne på hvert niveau indebærer, at det sikres, at salgsværdien på denne godkendelse ikke er i strid med grænsen, der ikke må overskrides, på dette niveau efter at have taget højde for det beløb, der allerede er registreret, og det beløb, der er faktureret til dato på det pågældende niveau.

Hvis kontrollen består, får godkendelsen en valideringsstatus som **Vellykket**.

Hvis kontrollen ikke består, får godkendelsen en valideringsstatus som **Mislykket**. Valideringsdetaljerne for grænsen, der ikke må overskrides, informerer brugeren om, på hvilket niveau valideringen mislykkedes.

Når den indsendte tids- eller udgiftspost betragtes som ikke-fakturerbar, angives valideringsstatussen for grænsen, der ikke må overskrides, til **Ikke tilgængelig**, og valideringsdetaljerne er overensstemmende med **Ikke tilgængelig**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Grænse, der ikke må overskrides, for ikke-fakturerede faktiske salgsværdier

Når en tids- eller udgiftspost godkendes, oprettes der poster for omkostninger og ikke-fakturerede faktiske salgsværdier. Hvis de ikke-fakturerede faktiske salgsværdier, der oprettes, kan faktureres og tilknyttes en kontraktlinje for tid og materialer, udfører programmet en valideringskontrol af grænsen, der ikke må overskrides, på følgende niveauer:

  - Kontrol i forhold til den konfigurerede grænse for kunden i projektkontraktlinjen
  - Kontrol i forhold til den konfigurerede grænse på kontraktlinjen
  - Kontrol i forhold til den konfigurerede grænse for kunden
  - Kontrol i forhold til den konfigurerede grænse på kontrakten

Kontrollerne på hvert niveau sikrer, at salgsværdien for den faktiske værdi ikke er i strid med grænsen, der ikke må overskrides, på dette niveau efter at have taget højde for det beløb, der allerede er registreret, og det beløb, der er faktureret til dato på det pågældende niveau.

Hvis kontrollen består, får den ikke-fakturerede saktiske salgsværdi statussen **Bindende**.

Hvis kontrollen ikke består, får den ikke-fakturerede saktiske salgsværdi statussen **Mislykket**. Valideringsdetaljerne informerer brugeren om, på hvilket niveau valideringen mislykkedes.

Når den ikke-fakturerede faktiske salgsværdi betragtes som ikke-fakturerbar eller gratis, hvis der ikke er angivet en grænse, der ikke må overskrides, på et af de fire niveauer, eller hvis den oprettede faktiske værdi er Omkostninger, Forskudshonorar, Ressourceenhed eller Internt salg, skal felterne **Må ikke overskrides-status** og **Må ikke overskrides-valideringsdetaljer** angives til **Ikke tilgængelig**.

## <a name="reset-the-not-to-exceed-status"></a>Nulstil må ikke overskrides-status

Du kan udføre en massenulstilling af må ikke overskrides-status. Dette gør det muligt for projektledere at justere må ikke overskrides-valideringen for at prioritere fakturering af en bestemt mængde arbejde, tid eller udgifter frem for andre, der allerede er bundet i det tilgængelige beløb, der ikke må overskrides.

Når må ikke overskrides-statussen er blevet nulstillet på ikke-fakturerede faktiske salgsværdier, reduceres det bundne beløb. Projektlederen kan vælge en anden brødtekst, tid eller udgifter, hvor valideringskontrollen for må ikke overskrides tidligere mislykkes og revurdere dem. Med reduktionen i det bundne beløb vil disse faktiske værdier nu bestå valideringen. Dette hjælper projektlederen med at udøve større indflydelse på og kontrol over de fakturerbare transaktioner for den pågældende periode.

Hvis du vil nulstille må ikke overskrides-statussen, skal du vælge en eller flere faktiske værdier i visningen **Efterslæb for fakturering af tid og materialer** eller **Faktiske værdier** og derefter vælge **Nulstil må ikke overskrides-status**.

Må ikke overskrides-statussen nulstilles til **Ikke evalueret** på alle de relevante valgte faktiske værdier. Faktiske værdier, hvor må ikke overskrides-statussen er blevet nulstillet, er ikke-fakturerede faktiske salgsværdier, der ikke allerede er blevet faktureret og ikke fremgår af en kladdefaktura, og som er markeret som fakturerbare. Alle andre valgte faktiske værdier ignoreres.

## <a name="reevaluate-not-to-exceed-status"></a>Reevaluer må ikke overskride-status

Du kan udføre en massereevaluering af må ikke overskrides-status. Revurdering af må ikke overskrides-statussen er nyttig, når:

  - Der var en genforhandling af grænser, som ikke må overskrides, med kunden, og de faktiske værdier skal revurderes.
  - Projektlederen ønsker at finjustere faktureringen af efterslæbet af ikke-fakturerede salg ved at prioritere et et arbejdsområde frem for et andet.

Hvis du vil reevaluere må ikke overskrides-statussen, skal du vælge en eller flere faktiske værdier i visningen **Efterslæb for fakturering af tid og materialer** eller **Faktiske værdier** og vælge **Reevaluer må ikke overskrides-status**.

Alle de relevante valgte faktiske værdier med en grænse, der ikke må overskrides, vil blive evalueret i forhold til opsætningen af grænsen, der ikke må overskrides. Faktiske værdier, der er relevante for reevalueringen af må ikke overskrides-statussen, er ikke-fakturerede faktiske salgsværdier, der ikke er blevet faktureret og ikke fremgår af en kladdefaktura, og som er markeret som fakturerbare. Alle andre valgte faktiske værdier, der er markeret.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]