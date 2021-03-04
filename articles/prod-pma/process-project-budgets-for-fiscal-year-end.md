---
title: Overfør projektbudgetter ved afslutning af regnskabsåret
description: Denne artikel indeholder oplysninger om, hvordan du kan overføre resterende budgetbeløb til fremtidige år og oprette detaljer om budgetregistrering.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074305"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Overfør projektbudgetter ved afslutning af regnskabsåret

[!include [banner](../includes/banner.md)]

Når du arbejder på et flerårigt projekt, kan du have et overskydende budget i slutningen af regnskabsåret. Du kan overføre de resterende budgetbeløb til et fremtidigt år og oprette detaljer budgetregistrering for beløbene i de tilknyttede finanskonti. Før du overfører de resterende beløb, skal du gennemgå og analysere de resterende budgetbeløb.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Gennemgå og analysere de resterende budgetbeløb

Benyt følgende fremgangsmåde for at gennemgå budgetbeløbene ved årsafslutning for projekter uden at overføre beløbene.

1. Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overfør budgetter**. 
2. På siden **Proces for overførsel af projektbudget** skal du på fanen **Indstillinger for årsafslutning** kontrollere, at **Overfør de resterende projektbudgetbeløb** ikke er aktiveret.
3. På fanen **Parametre** skal du i feltet **Projektbudgetår** vælge det regnskabsår, som du vil have vist det resterende budgetbeløb for. 
4. I feltet **Første regnskabsår** skal du vælge det regnskabsår, som du vil have vist det resterende budgetbeløb for. 
5. I feltet **Fra prognosemodel** skal du vælge **Resterende buget**. 
6. Hvis du vil inkludere projekter, der opfylder de valgte kriterier, og som ikke har et resterende budget, skal du vælge **Vis ingen resterende**.  
7. På fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder de valgte kriterier og derefter vælge **Behandl**. 
8. Hvis du vil designe en databaseforespørgsel, der indlæser et bestemt sæt budgetter i ruden, skal du vælge **Hent valgte budgetter**.

Du kan finde flere oplysninger om en bestemt linje i ruden ved at markere linjen og derefter vælge **Se budgetdetaljer** eller **Se konti**.

## <a name="carry-forward-remaining-budget-amounts"></a>Overfør de resterende budgetbeløb 

Når du behandler de resterende budgetbeløb, kan du oprette transaktioner i finanskladden for de beløb, som du overfører. Hvis du vil oprette transaktioner i finanskladden, skal du udføre trinnene i sektionen [Overfør budgetbeløb og opret transaktioner i finanskladden](#carry-forward). 

> [!NOTE]
> De budgetbeløb, der overføres, overføres til den prognosemodel, der er valgt på siden **Prognosemodeller** som den overførte prognosemodel.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Overfør budgetbeløb og opret transaktioner i finanskladden

1.  Vælg **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overfør budgetter**. 
2. På siden **Proces for overførsel af projektbudget** skal du vælge **Årsafslutning** og derefter aktivere **Overfør de resterende projektbudgetbeløb** og **Opret budgetregisterposter i finanskladden**. 
3. På fanen **Parametre** skal du i feltgruppen **Projektparametre** vælge følgende:

   - **Projektbudgetår** : Vælg starten af det regnskabsår, som du vil have vist de resterende budgetbeløb for. 
   - **Drift** : Opret driftstransaktioner i finanskladden. 
   -  **IGVA** : Opret transaktioner for IGVA (igangværende arbejde) i finanskladden.
   -  **Løn** : Opret lønfordelingstransaktioner i finanskladden. 

5. I feltgruppen **Finanskladde** skal du angive følgende oplysninger: 

   - I feltet **Første regnskabsår** skal du vælge det regnskabsår, som du vil overført det resterende budgetbeløb til for projekterne. Standardværdien er ét år efter værdien i feltet **Projektbudgetår**.
   -  I feltet **Overførelsesperiode** skal du vælge den periode, som du vil oprette budgetregisteroplysningerne for i finanskladden. Dette er typisk den første periode i det første regnskabsår.

6. I feltgruppen **Kopier fra/til** skal du angive følgende oplysninger:

   - I feltet **Fra prognosemodel** skal du vælge den prognosemodel for projektbudgettet, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne. 
   - I feltet **til finansbudgetmodel** skal du vælge den finansbudgetmodel, der er knyttet til de budgetbeløb, som du vil overføre til finanskladden. 
   -  Vælg **Overfør salgsvaluta** , hvis du vil bruge projektets salgsvaluta til de transaktioner i finanskladden, der oprettes, når du overfører budgetbeløbene for projekterne. Hvis indstillingen ikke er valgt, bruger transaktionerne regnskabsvalutaen. 
   -  Vælg **Vis ingen resterende** for at inkludere projekter, der ikke har nogen resterende budgetbeløb, men opfylder de øvrige kriterier, som du har valgt i de projekter, der vises i den nederste rude.

7. På fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle de budgetter, der opfylder de valgte kriterier. Hvis du foretrækker at designe en databaseforespørgsel, der indlæser et bestemt sæt projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.
8. For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af linjen for projektet.

    > [!TIP]
    > Hvis du vil markere alle eller de fleste af projekterne, skal du markere afkrydsningsfeltet øverst til venstre. Hvis du vil udelade behandlingen af et projekt, skal du fjerne markeringen i dette projekt.

9. Hvis du vil overføre de resterende budgetbeløb for de valgte projekter til det valgte regnskabsår og oprette budgetregisterdetaljer i finanskladden, skal du vælge **Behandl**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Overfør budgetbeløb uden at oprette transaktioner i finanskladden

1. Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overfør budgetter**.
2. På siden **Proces for overførsel af projektbudget** skal du i feltet **Indstillinger for årsafslutning** vælge **Overfør de resterende projektbudgetbeløb**.
3. I gruppen **Parametre** skal du i feltet **Projektbudgetår** vælge det regnskabsår, som du vil have vist de resterende budgetbeløb for.
4. I gruppen **Kopier fra/til** skal du angive følgende oplysninger:

   - I feltet **Fra prognosemodel** skal du vælge den prognosemodel for projektbudgettet, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne. 
   - Hvis du vil inkludere projekter, der opfylder de valgte kriterier, og som ikke har et resterende budget, skal du vælge **Vis ingen resterende**.
   - I gruppen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle de budgetter, der opfylder de valgte kriterier. Hvis du vil designe en databaseforespørgsel, der indlæser et bestemt sæt projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.

5. For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af linjen for projektet. 
6. Vælg **Behandl** for at overføre de resterende budgetbeløb for de valgte projekter til det valgte regnskabsår.



[!INCLUDE[footer-include](../includes/footer-banner.md)]