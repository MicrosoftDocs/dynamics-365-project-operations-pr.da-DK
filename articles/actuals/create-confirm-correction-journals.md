---
title: Opret og bekræft rettelseskladder
description: Dette emne indeholder oplysninger om, hvordan du opretter og bekræfter en rettelseskladde.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582796"
---
# <a name="create-and-confirm-correction-journals"></a>Opret og bekræft rettelseskladder

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Det kan ske, at en tids- eller udgiftspost angives forkert. En konsulent kan f.eks. vælge den forkerte dato, når der oprettes en tidspost, eller konsulenten kan vælge det forkerte projekt, når de angiver en udgift. Hvis en konsulent ikke kan opdatere de indsendte poster, kan en back end-administrator direkte rette de faktiske værdier for et projekt.

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

 
## <a name="correct-approved-expense-entries"></a>Ret godkendte udgiftsposter

Benyt følgende fremgangsmåde for at rette en eller flere udgiftsposter. 

1. I området **Salg** skal du under **Transaktioner** i venstre navigationsrude vælge **Godkendte udgifter**.

2. På listen **Godkendte udgifter** skal du vælge det projekt, som du ønsker at rette, og dernæst vælge **Ret poster**. Der oprettes automatisk en ny rettelseskladde med den tildelte type **Udgiftsrettelse**. 

3. På siden **Ny kladde** skal du angive en **Beskrivelse** for rettelsen, og på fanen **Udgiftsrettelse** i sektionen **Nye værdier for udgifter** skal du vælge de datafelter, som du ønsker at rette for de valgte udgiftslinjer. Du kan f.eks. tildele udgiften til et andet **Projekt** eller rette **Udgiftskategorien**, **Udgiftsdatoen** eller den **Reserverbare ressource**.

4. Vælg **Forhåndsvisning**. Vælg **OK** i dialogboksen. 

5. Verificer rettelserne på fanen **Kladdelinjer**. Du kan få vist en liste over de oprindelige faktiske værdier, der er relateret til de valgte udgiftsposter, som er blevet tilbageført, samt de tilsvarende ændrede linjer, der er blevet oprettet.

6. Hvis de rettede værdier er som forventede, skal du vælge **Bekræft**. Vælg **OK** i dialogboksen. Hvis værdierne ikke vises som forventet, skal du vælge **Annuller** for at vende tilbage til listen med **Godkendte udgifter**. Gentag trin 2-5. 

7. Når du har bekræftet rettelseskladden, skal du vende tilbage til det eller de projekter, du har opdateret, for at få vist ændringerne.

8. På projektsiden skal du under fanen **Faktiske værdier** gennemgå listen med **Visning af tilknyttede faktiske værdier**. De oprindelige poster og de rettede poster vises på listen.


## <a name="correct-approved-material-usage-logs"></a>Ret godkendte materialeforbrugslogfiler

Fuldfør følgende trin for at rette en eller flere materialeforbrugslogposter.

1. I området **Salg** skal du i venstre navigationsrude under **Transaktioner** vælge **Faktiske værdier**.

2. På listen **Faktiske værdier** skal du bruge kolonnefiltre til at vælge transaktionsklassen **Materiale**, så det kun er de faktiske værdier for materialer, der vises. Brug andre kolonnefiltre til yderligere at begrænse de faktiske værdier, der vises. Når du har fundet det ønskede sæt af faktiske værdier, skal du vælge de faktiske værdier og derefter vælge **Ret poster**. Der oprettes automatisk en ny korrigeringstype, og typen **Rettelse af materiale** tildeles.

3. På siden **Ny kladde** skal du i feltet **Beskrivelse** angive en beskrivelse for rettelsen. I feltet **Rettelse af materiale** skal du derefter i afsnittet **Nye værdier for materialer** vælge datafelterne for at rette de valgte materialelinjer. Du kan f.eks. tildele materialet til et andet projekt eller rette produktet, materialedatoen eller underleverandøren.

4. Vælg **Forhåndsvisning**. I den næste dialogboks skal du dernæst vælge **OK**.

5. Kontrollér rettelserne under fanen **Kladdelinjer**. Du kan få vist en liste over de oprindelige faktiske værdier, der er relateret til de valgte materialeposter, som er blevet tilbageført, og de korrigerede tilsvarende linjer, der er oprettet.

6. Hvis de rettede værdier er som forventede, skal du vælge **Bekræft**. I den næste dialogboks skal du dernæst vælge **OK**. Hvis værdierne ikke er som forventet, skal du vælge **Annuller** for at vende tilbage til listen **Faktiske værdier**. Gentag derefter trin 2 til 5.

7. Når du har bekræftet rettelseskladden, skal du vende tilbage til det eller de projekter, du har opdateret, for at få vist ændringerne.

8. På projektsiden skal du under fanen **Faktiske værdier** gennemgå listen med **Visning af tilknyttede faktiske værdier**. De oprindelige poster og de rettede poster vises på listen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
