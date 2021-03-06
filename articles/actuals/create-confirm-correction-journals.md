---
title: Opret og bekræft rettelseskladder
description: Dette emne indeholder oplysninger om, hvordan du opretter og bekræfter en rettelseskladde.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896949"
---
# <a name="create-and-confirm-correction-journals"></a>Opret og bekræft rettelseskladder

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

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


