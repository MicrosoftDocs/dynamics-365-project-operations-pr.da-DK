---
title: Indkøbsordrer for et projekt
description: I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer til et projekt. Den anvendte metode afhænger af formålet med indkøbsordren, og hvornår de indkøbte varerne forbruges samt tilskrives et projekt.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49ca1f9af715dcb1beb7932f7c484abc7b183dcd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684981"
---
# <a name="purchase-orders-for-a-project"></a>Indkøbsordrer for et projekt

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de forskellige metoder, du kan bruge til at oprette indkøbsordrer til et projekt. Den anvendte metode afhænger af formålet med indkøbsordren, og hvornår de indkøbte varerne forbruges samt tilskrives et projekt.

### <a name="methods-for-creating-a-purchase-order"></a>Metoder til oprettelse af en indkøbsordre

Du kan benytte en af følgende fremgangsmåder for at oprette en købsordre i projektstyring og regnskab. Formålet med indkøbsordren afgør, hvornår indkøbsordren forbruges, og derfor hvornår varerne kan tilskrives et projekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Formål</th>
<th>Forbrug af varer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Opret en indkøbsordre direkte fra et projekt.</td>
<td>Brug denne metode til at købe varer fra en ekstern leverandør, som skal forbruges i et projekt. Du kan oprette indkøbsordren på to måder:
<ul>
<li>Fra selve projektet. I dette tilfælde er projektet allerede defineret for indkøbsordren.</li>
<li>Ved at gå til projektets indkøbsordre. Du skal både vælge den leverandør og det projekt, som du vil oprette indkøbsordren for.</li>
</ul></td>
<td>Varer forbruges, når leverandørfakturaen opdateres.</td>
</tr>
<tr class="even">
<td>Opret en indkøbsordre fra en salgsordre.</td>
<td>Brug denne metode til at købe varer, når du opretter en salgsordre fra et projekt.</td>
<td>Varerne forbruges, når salgsordren faktureres til kunden.</td>
</tr>
<tr class="odd">
<td>Opret en indkøbsordre ud fra et varebehov.</td>
<td>Brug denne metode til at købe varer, når du opretter et varebehov fra et projekt.</td>
<td>Varer forbruges, når følgesedlen til varebehovet opdateres.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Når du opdaterer leverandørfakturaen eller følgesedlen, bliver du bedt om at opdatere følgesedlen for varebehovet.

Du kan finde flere oplysninger i [Modtag varer på købsordre fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]