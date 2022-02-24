---
title: Arbejdsproces for udgiftsstyring
description: I dette emne forklares det, hvordan du kan bruge arbejdsprocessystemet i Microsoft Dynamics 365 Finance til at oprette en revisionsproces for udgiftsrapporter i udgiftsstyring.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271661"
---
# <a name="expense-management-workflow"></a>Arbejdsproces for udgiftsstyring

Du kan bruge arbejdsprocessystemet til at oprette en revisionsproces for udgiftsrapporter i udgiftsstyring. Du kan konfigurere en arbejdsproces, der bruger følgende kriterier til at afgøre, hvem der skal godkende udgiftsrapporter:

- Medarbejderens rapporteringshierarki og foruddefinerede godkendelsesgrænser
- Godkendelse på flere niveauer, der understøtter midlertidige godkendere og en endelig godkender
- Økonomiske dimensioner og projektansvar
- Tildeling til bestemte brugere eller brugergrupper

Det er muligt at oprette arbejdsprocesgodkendelser for udgiftsrapporter, rejserekvisitioner, kontantforskud og momsopkrævning.

**Eksempel**

Følgende proces er et eksempel på arbejdsprocessen for udgiftsstyring for en udgiftsrapport.

1. En medarbejder opretter og gemmer en udgiftsrapport.
2. Medarbejderen indsender udgiftsrapporten til godkendelse. Godkenderen identificeres på baggrund af de regler, der blev defineret under opsætningen af arbejdsprocessen.
3. Godkenderen modtager en meddelelse om, at en udgiftsrapport er klar til godkendelse. Godkenderen gennemser udgiftsrapporten og bekræfter, at følgende betingelser er opfyldt:

    - Udgifterne overtræder ikke nogen udgiftspolitikker. Hvis en udgift overtræder en politik, kontrollerer godkenderen, at udgiftsrapporten indeholder en gyldig forretningsmæssig berettigelse.
    - Elektroniske kvitteringer er vedhæftet udgiftsrapporten.

4. Godkenderen godkender udgiftsrapporten.
5. Udgiftsrapporten tildeles kreditorkoordinatoren med henblik på bogføring.
6. Et af følgende trin indtræffer, afhængigt af om der er konfigureret automatisk bogføring:

    - Hvis der er konfigureret automatisk bogføring, behandles udgiftsrapporten med henblik på betaling, og udgiftsrapportens status opdateres.
    - Hvis der ikke er konfigureret automatisk bogføring, bekræfter kreditorkoordinatoren, at alle oprindelige kvitteringer er blevet indsendt, og at kvitteringerne er afstemt med udgifterne i udgiftsrapporten. Alle de momskoder, der er angivet i udgiftsrapporten, skal også verificeres som værende korrekte.

Når disse krav er kontrolleret, bogføres udgiftsrapporten.

Når udgiftsrapporten er bogført, godkendes betalingen i udgiftsrapporten, og medarbejderen refunderes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]