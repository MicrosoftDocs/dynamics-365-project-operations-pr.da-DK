---
title: Opdatere plug-in-attributter, så de indeholder nye prisdimensioner
description: Dette emne indeholder oplysninger om opdatering af plug-in-attributter til prisdimensioner.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074255"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Opdatere plug-in-attributter, så de indeholder nye prisdimensioner

> [!NOTE]
> Hvis du ikke bruger tilbudsgivningsfunktionen eller kontraktenheden i PSA (Project Service Automation), kan du springe dette emne over.

Dette emne forudsætter, at du har fuldført procedurerne i emnerne [Oprette brugerdefinerede felter og objekter](create-custom-fields-entities.md), [Føje brugerdefinerede felter til prisopsætning og transaktionsobjekter](field-references.md) og [Konfigurere brugerdefinerede felter som prisfastsættelsesdimensioner](set-up-pricing-dimensions.md). Hvis du ikke har fuldført procedurerne, skal du gå tilbage og fuldføre dem og derefter vende tilbage til dette emne.

Når der oprettes en tilbudslinjedetalje på siden **Tilbudslinje** for en produkttilbudslinje, opretter systemet to estimatlinjer i baggrunden – en linje for estimatets omkostningsside og én for salgssiden. Det samme gælder for projektkontraktlinjer.

Når du foretager en ændring af mængden eller et felt på omkostningssiden, overføres denne ændring til salgssiden. Dette er muligt på grund af følgende plug-ins, der skal registreres igen, efter at der er foretaget en ændring i prisdimensionerne.

- PreOperationContractLineDetailUpdate – Opdateringer **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – Opdateringer **msdyn_quotelinetransaction**.

I følgende trin forklares, hvordan du kan registrere plug-ins.

1. Åbn **PluginRegistrationTool** og opret forbindelse til din online-forekomst.
2. Klik på **Søg** , og søg efter den plug-in, der skal opdateres.

 ![Skærmbillede af søgetræet](media/PRT-1.png)

3. Når plug-in'en er fundet, skal du markere den og derefter klikke på **Vælg i hovedformular**.

4. Vælg trinnet for den plug-in, du vil opdatere, højreklik, og vælg derefter **Opdater**.

 ![Skærmbilledet af plug-in'en, der skal opdateres](media/PRT-2.png)
 
5. I opdateringsvinduet skal du klikke på ellipseknappen ( **...** ) i filtreringsattributterne.

 ![Skærmbillede af opdatering af oplysningerne om konfiguration af eksisterende trin](media/PRT-3.png)
 
6. Markér afkrydsningsfelterne for prisattributter.

 ![Skærmbillede, der viser det markerede afkrydsningsfelt for prisattributter](media/PRT-4.png)

7. Klik på **OK** for at lukke siden, og vælg derefter **Opdater trin**.

 ![Skærmbillede, der viser knappen "Opdater trin"](media/PRT-5.png)
 
8. Gentag denne proces for den anden plug-in, **PreOperationQuoteLineDetail – Opdatering af msdyn_quotelinetransaction**.

9. Luk Plug-in Registration Tool.

