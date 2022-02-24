---
title: Opsætning af omkostningsskabeloner
description: Dette emne indeholder oplysninger om, hvordan du opretter og anvender omkostningsskabeloner i Project Operations.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642716"
---
# <a name="set-up-cost-templates"></a>Opsætning af omkostningsskabeloner

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_


Dette emne indeholder oplysninger om, hvordan du opretter og anvender omkostningsskabeloner i Project Operations. En omkostningsskabelon bestemmer:

- Projektkategorierne for de prognoser og faktiske transaktioner, der skal inkluderes i en procentdel af beregningen af projektets færdiggørelse. Den procentvise værdi bruges derefter til at beregne, hvor meget omsætning der anerkendes.
- Om færdiggørelsesgraden kan ændres, hvis den beregnes automatisk.
- Om færdiggørelsesgraden beregnes på baggrund af beløb eller enheder.

## <a name="cost-template-example"></a>Eksempel på omkostningsskabelon

Du arbejder på et projekt med design af et websted for en kunde, hvor du opkræver et fladt gebyr på 10.000 USD. Din prognose forudsiger, at det vil tage 100 timer (5.000 USD) at fuldføre projektet. Du forudser også to flybilletter og fire overnatning på et hotel for rejser til kundens lokation (1.800 USD). Dette medfører en prognoseomkostning på 6.800 USD.

Når du kører processen for fast pris-omsætningsanerkendelse for at oprette et estimat i slutningen af måneden, finder du ud af, at du har arbejdet 35 timer på projektet. Dette inkluderer ikke flyvninger eller hotelomkostninger. Du har også haft en medhjælper til at udføre fem timers forskning på projektet til en pris på 100 USD, som du havde planlagt.

Når du beregner værdien for færdiggørelsesprocenten for projektet, har du følgende muligheder:

- Vil du medtage alle omkostninger (timer og udgifter) eller kun timer?
- Vil du medtage alle timer eller kun kun planlagt timer?
- Vil du beregne den færdiggørelsesprocenten baseret på omkostningerne i dollar for de planlagte timer (5.000 USD) eller bare på antallet af timer (100)?

Dine svar på disse spørgsmål bestemmer de indstillinger, du angiver i omkostningsskabelonen og de kategorier, du vælger på omkostningsskabelonlinjerne.

I følgende tabel illustreres resultaterne af forskellige metoder til beregning af værdien for færdiggørelsesgraden i dette scenario.

| Fuldførelse baseret på | Dollaromkostninger eller enheder | Procent fuldført | Beregning |
| --- | --- | --- | --- |
| Alle timer, ingen udgifter | Dollaromkostninger | 37 % 35 x 50 USD + 100 USD = 1.850 USD 1.850 USD/5.000 USD |
| Alle timer, ingen udgifter | Enheder | 40 % | 40 timer/100 timer (herunder fem ikke-planlagte timer) |
| Planlagte timer, ingen udgifter | Dollaromkostninger eller enhed | 35 % | 35/100 timer eller 35 x 50 USD/5.000 |
| Alle timer og udgifter | Dollaromkostninger | 27,2 % | 1.850 USD/6.800 USD |

Fastlæggelse af, hvilken fremgangsmåde du skal følge for at oprette en omkostningsskabelon kan afhænge af flere overvejelser:

- Hvis du medtager ikke-planlagte timer i omkostningsskabelonen, risikerer du at nå op på 100 % færdigt, før projektet er fuldført. Dette skyldes, at de faktiske timer vil væree højere end planlagte timer. Hvis du bruger en af de første to metoder, der er angivet i tabellen, skal du ændre planen (budgetterede enheder), når du bliver opmærksom på afvigelser. I dette tilfælde ville du tilføje eller fratrække timer på grundlag af din viden om, hvad der kræves for at afslutte projektet. Hvis der kræves yderligere 65 timer, før projektet kan fuldføres, skal der tilføjes fem timer til planen, i alt 105. Hvis du ved, at din assistenten vil undersøge i endnu fem timer, bliver det samlede antal 110 timer.
- Hvis du bruger den tredje metode, der er angivet i tabellen, skal du kun opdatere de planlagte timerne for din egen tid for at forhindre, at beregningen af færdiggørelsesprocenten er nøjagtig. Din rentabilitet ændres, når der logføres ikke-planlagte timer, men du vil fortsat være på have en kurs med en kendt færdiggørelsesprocent.
- Hvis du bruger den fjerde metode, der er angivet i tabellen, er der risiko for, at udgifterne vil opstå på uregelmæssige tidspunkter, og at de muligvis ikke afspejles i din færdiggørelsesfremgang. Hvis udgifterne er inkluderet, kan de derfor bevirke, at din færdiggørelsesprocent svinger mere, end du ønsker. Da du f.eks. ikke har fløjet endnu, er din færdiggørelsesprocent 27 procent i stedet for 35 procent eller 37 procent, hvis du baserer beregningen på tid alene. Hvis du har taget én tur med to overnatninger og har budgetteret dine omkostninger til fly og hotel præcist, ville færdiggørelsesprocenten være 40,4 % (1.850 USD for arbejdsløn og 900 USD for udgifter = 2.750 USD/6.800 USD = 40,4 procent). Det betyder derfor, at udgifterne for kun én flyrejse vil ændre færdiggørelsesprocenten fra 27 procent til 40 procent.

## <a name="create-cost-templates"></a>Opret omkostningsskabeloner
Følg disse trin for at oprette omkostningsskabeloner:

1. Hvis du vil have adgang til omkostningsskabeloner, skal du i Dynamics 365 Finance-miljøet gå til **Projektstyring og regnskab** > **Opsætning** > **Estimater** > **Omkostningsskabelon**.
2. Vælg **Ny** for at oprette en ny omkostningsskabelon. Angiv et navn og en beskrivelse.
3. Angiv omkostningslinje-ID for hver enkelt transaktionstype.
4. Vælg en standardfuldførelsesmetode:

  - **Automatisk**: færdiggørelsesgraden beregnes automatisk på et projekt. Den beregnede værdi kan ikke ændres.
  - **Manuel**: færdiggørelsesgraden beregnes automatisk på et projekt. Den beregnede værdi kan ændres.

  > [!NOTE]
  > I manuelle beregninger bevares færdiggørelsesgraden i **Manuel beregning** på fanen **Generelt** på siden **Estimat**.

5. I **Fuldførelse baseret på** skal du vælge en af følgende værdier:

  - **Beløb**: beløbet i regnskabsvalutaen beregnes i den færdiggørelsesgraden.
  - **Enhed**: antallet beregner færdiggørelsesgraden.
  - **Lige linje**: systemet beregner færdiggørelsesgraden på et proportionalt grundlag ved hjælp af projektets start- og slutdatoer for at bestemme projektets varighed.

6. Vælg **Omkostningslinjer** for at gennemgå omkostningslinjerne i omkostningsskabelonen. Der skal angives mindst én omkostningslinje for alle transaktionstyper. Men du kan oprette flere omkostningslinjer for de samme transaktionstyper og angive de ønskede attributter for disse linjer.
7. På fanen **Kategorier** skal du vælge de projektkategorier, der skal inkluderes i omkostningsskabelonlinjen.
8. Under fanen **Generelt** skal du vælge, om linjen skal inkluderes i beregningen af færdiggørelsesgraden.
9. Vælg den metode for færdiggørelsesomkostninger, der skal bruges ved beregning af færdiggørelsesgraden.
