---
title: Konfigurer roller for skabeloner til arbejdsopgavehierarki
description: Dette emne indeholder oplysninger om, hvordan du kan konfigurere rolleoplysninger for skabeloner til arbejdsopgavehierarki.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997594"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Konfigurer roller for skabeloner til arbejdsopgavehierarki

[!include [banner](../includes/banner.md)]

Projektledere kan konfigurere skabeloner til arbejdsopgavehierarki (WBS), som de kan anvende, når de opretter et WBS for nye projekter. Projektledere kan tilføje roller, når de opretter en skabelon. Benyt følgende fremgangsmåde for at tildele en rolle til en WBS-skabelon.

1. Vælg **Projektstyring og regnskab** > **Opsætning** > **Projekter** > **Skabeloner til arbejdsopgavehierarki**.
2. Vælg **Detaljer** for en valgt WBS-skabelon.
3. Markér en opgave på listen, og vælg derefter i feltet **Rolle** en rolle, der skal tildeles til opgaven.

## <a name="work-with-a-wbs"></a>Arbejde med et WBS

Du kan oprette et nyt WBS, eller du kan kopiere et WBS fra en eksisterende WBS-skabelon. En projektleder kan nemt administrere ressourcerne ved at tildele roller til nye opgaver i WBS. Roller kan erstattes, enten efter at en ressource er erhvervet, eller når en ressource, der er bekræftet til at skulle arbejde på opgaven, er blevet identificeret. Denne fleksibilitet gør det muligt for projektledere at udføre følgende opgaver:

- Angiv det antal ressourcer, der kræves til WBS-arbejdspakker.
- Estimer projektomkostninger.
- Fastlæg et foreløbigt budget.
- Estimer aktivitetens varighed baseret på roller og ressourcer.
- Opret nogle projektstyringsplaner baseret på tilgængelige projektoplysninger.

Der er tilføjet yderligere muligheder i WBS for at opnå en bedre anvendelse af ressourcefunktionaliteten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indstilling</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressourcetildelinger</td>
<td>Få vist de tildelte ressourcer, datoer, antallet timer og reservationstype for opgaver i WBS.</td>
</tr>
<tr class="even">
<td>Opret team automatisk</td>
<td>Tilføj automatisk planlagte ressourcer ved hjælp af de roller, der er knyttet til en opgave. Finance foreslår automatisk planlagte ressourcer ved hjælp af beslutningsanalyse med flere kriterier, der er baseret på roller. Når der er angivet roller og tidsforbrug (timer) for opgaverne i et WBS, og efter, at strukturen er blevet frigivet, skal du vælge <strong>Opret team automatisk</strong>. Det nødvendige antal planlagte ressourcer tilføjes til WBS og fanen <strong>Projekt- og teamplanlægning</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (rulleliste)</td>
<td>På siden <strong>Start ressourcetildeling</strong> kan du vælge at reservere ressourcer definitivt eller midlertidigt på grundlag af den angivne varighed. Du kan justere visningsindstillingerne for at få vist og angive varigheden af ressourceaktiviteter. Du kan vælge og tildele ressourcer på arbejdspakkeniveau ved hjælp af følgende indstillinger:
<ul>
<li><strong>Accepter</strong> – Bekræft ændringer af den ressource, der er tildelt til en opgave.</li>
<li><strong>Annuller</strong> – Annuller ændringer af den ressource, der er tildelt til en opgave.</li>
<li><strong>Tildel automatisk</strong> – En tilgængelig personaleressource, der har en tilsvarende rolle, vælges automatisk og tildeles den valgte opgave.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgraderingsfase 2**.
2. Vælg **Plan** > **Aktiviteter** > **Arbejdsopgavehierarki**.
3. Vælg **Ny** for at tilføje følgende niveau-et-aktiviteter til WBS:

    - Påbegynder
    - Planlægning
    - Udfører
    - Overvågning og kontrol
    - Luk

4. Angiv datoerne og tidsforbruget (timer) som vist i følgende illustration.

    [![Angivelse af datoer og tidsforbrug](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vælg opgavelinjen **Påbegynd**, og du skal derefter i feltet **Rolle** vælge **Overordnet projektleder**.
6. Vælg **Udgiv**.
7. På den samme linje skal du i feltet **Ressource** vælge **Daniel Goldschmidt** og derefter vælge **Accepter**.
8. Markér opgavelinjen **Planlægning**, og vælge derefter i feltet **Rolle** **Forretningsanalytiker**.
9. Vælg **Publicer**, og vælg **Opret team automatisk**.
10. I bekræftelsesfeltet, der vises, skal du vælge **Ja**.
11. I feltet **Ressource** skal du kontrollere, at værdien er **Forretningsanalytiker 1**.
12. For ressourcen **Forretningsanalytiker 1** skal du åbne opslaget og vælge **Start ressourcetildelinger**. Vælg derefter en arbejder til opgaven.
13. Vælg **Reserver midlertidigt** &gt; **Fuld kapacitet**.

    > [!NOTE] 
    > Du modtager ikke en advarsel om, at den angivne ressource nu er 2, da antallet af ressourcer stadig er 1.

14. På siden **Arbejdsopgavehierarki** skal du kontrollere ressourcetildelingen i WBS og derefter vælge **Gem**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]