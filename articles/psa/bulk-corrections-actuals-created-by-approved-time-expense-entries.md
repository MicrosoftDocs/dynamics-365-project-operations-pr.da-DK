---
title: Massekorrektioner af de faktiske værdier, der er oprettet af godkendte tids- og udgiftsposter
description: I dette emne beskrives det, hvordan en administrator kan foretage enkeltvise korrektioner eller massekorrektioner af tidligere godkendte tids- eller udgiftsposter, hvis faktureringen ikke er fuldført.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144946"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Massekorrektioner af de faktiske værdier, der er oprettet af godkendte tids- og udgiftsposter

[!include [banner](../includes/psa-now-project-operations.md)]

Det kan ske, at en tids- eller udgiftspost registreres forkert. En konsulent kan f.eks. vælge den forkerte dato, når han/hun opretter en tidspost, eller konsulenten kan transponere tallene, når der angives en udgift. Hvis en konsulent ikke kan opdatere de indtastede poster, kan en administrator rette i posten for et projekt direkte.

For at fuldføre procedurerne i dette emne skal du have administratortilladelser.

## <a name="correct-approved-time-entries"></a>Ret godkendte tidsposter     

Benyt følgende fremgangsmåde for at rette enkelte eller flere tidsangivelser for et projekt.

1. I området **Salg** skal du vælge **Transaktioner** og dernæst vælge **Godkendt tid**. 

2. På listen **Godkendt tid** skal du finde og vælge en eller flere af de godkendte tidsposter, der skal rettes. Du kan bruge filteret til at finde relaterede poster. Du kan f.eks. filtrere efter et projekt-id og vælge alle de godkendte tidsposter med det pågældende projekt-id.

3. Vælg **Ret poster**. Der oprettes automatisk en ny rettelseskladde med den tildelte type **Tidskorrektion**. De valgte poster føjes til kladden. 

4. På siden **Ny kladde** skal du angive en **Beskrivelse** af rettelseskladden og derefter vælge fanen **Rettelser af tidsposter**.  
5. I sektionen **Nye værdier for tidsposter** skal du opdatere felterne med de korrekte oplysninger efter behov. Du kan f.eks. ændre det tildelte projekt eller den reserverbare ressource.

6. Vælg **Forhåndsvisning**. Vælg **OK** i dialogboksen. Under fanen **Kladdelinjer** kan du få vist en liste over de oprindelige faktiske værdier, der er relateret til de valgte tidsposter, som er blevet tilbageført, samt de tilsvarende ændrede linjer, der er blevet oprettet. Hvis der skal foretages yderligere rettelser, skal du gentage trin 5 og 6. 

> [!NOTE]
> Alle de korrigerede faktiske værdier får de samme værdier, som du har valgt i sektionen **Nye værdier for tidsposter**.

7. Hvis rettelserne vises som forventet, skal du vælge **Bekræft**. Vælg **OK** i dialogboksen.

8. Gå tilbage til området **Salg**, og vælg **Projekter**, og åbn derefter det projekt, som du lige har opdateret tidsposterne for. 

9. På siden **Projekter** kan du under fanen **Faktiske værdier** få vist de ændringer, du har foretaget. 

> [!NOTE]
> Hvis fanen **Faktiske værdier** ikke er synlig, skal du vælge **Relaterede** > **Faktiske værdier**.  

10. På listen **Visning af faktisk tilknytning** kan du se, at de oprindelige tidsposter, der er blevet tilbageført, stadig findes på listen, hvilket også er tilfældet for de tilsvarende rettede tidsposter. 

I følgende illustration er der f.eks. to linjeelementer med et antal på 8,00, som har angivet debiteringer i kolonnen "Beløb". Derudover er der to linjeelementer med et antal på -8,00, som viser de krediterede beløb i kolonnen "Beløb". De rettelser ændrer mængden til nul.

![Visningsliste med tilknyttede faktiske værdier](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Ret godkendte udgiftsposter

Benyt følgende fremgangsmåde for at rette en eller flere udgiftsposter. 

1. I området **Salg** skal du under **Transaktioner** i venstre navigationsrude vælge **Godkendte udgifter**.

2. På listen **Godkendte udgifter** skal du vælge det projekt, som du ønsker at rette, og dernæst vælge **Ret poster**. Der oprettes automatisk en ny rettelseskladde med den tildelte type **Udgiftsrettelse**. 

3. På siden **Ny kladde** skal du angive en **Beskrivelse** for rettelsen, og på fanen **Udgiftsrettelse** i sektionen **Nye værdier for udgifter** skal du vælge de datafelter, som du ønsker at rette for de valgte udgiftslinjer. Du kan f.eks. tildele udgiften til et andet **Projekt** eller rette **Udgiftskategorien**, **Udgiftsdatoen** eller den **Reserverbare ressource**.

4. Vælg **Forhåndsvisning**. Vælg **OK** i dialogboksen. 

5. Verificer rettelserne på fanen **Kladdelinjer**. Du kan få vist en liste over de oprindelige faktiske værdier, der er relateret til de valgte udgiftsposter, som er blevet tilbageført, samt de tilsvarende ændrede linjer, der er blevet oprettet.

6. Hvis de rettede værdier er som forventede, skal du vælge **Bekræft**. Vælg **OK** i dialogboksen. Hvis værdierne ikke vises som forventet, skal du vælge **Annuller** for at vende tilbage til listen med **Godkendte udgifter**. Gentag trin 2-5. 

> [!NOTE]
> De korrigerede faktiske værdier får de samme værdier, som du har valgt i sektionen **Nye værdier for udgifter**.

7. Når du har bekræftet rettelsesjournalen, skal du gå tilbage til det projekt eller de projekter, du har opdateret, for at få vist ændringerne.  

8. På projektsiden skal du under fanen **Faktiske værdier** gennemse **Oversigt over faktiske tilknytninger**. De oprindelige poster og de rettede poster vises på listen. I følgende illustration vises de oprindelige beløb for udgiftsposter og de tilsvarende korrigerede udgiftsposter. 

![Faktiske udgifter](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
