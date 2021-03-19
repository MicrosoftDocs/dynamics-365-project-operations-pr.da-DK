---
title: Opdatering af plug-in-attributter med nye prisfastsættelsesdimensioner
description: Dette emne indeholder oplysninger om, hvordan du opdaterer plug-in-attributter til prisfastsættelsesdimensioner.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274676"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Opdater plug-in-attributter med nye prisfastsættelsesdimensioner

Dette emne indeholder oplysninger om, hvordan du opdaterer plug-in-attributter til prisfastsættelsesdimensioner.

> [!NOTE]
> Dette emne kan kun anvendes på tilbuds- og kontraktfunktionerne i Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Forudsætninger
Før du fuldfører trinnene i dette emne, skal du have fuldført procedurerne under følgende emner:

  - [Opret brugerdefinerede felter og objekter](create-custom-fields-entities-pricing-dimensions.md) 
  - [Tilføj brugerdefinerede felter til prisopsætning og transaktionsobjekter](add-custom-fields-price-setup-transactional-entities.md)
  - [Konfigurer brugerdefinerede felter som prisfastsættelsesdimensioner](set-up-custom-fields-pricing-dimensions.md). 
  
Hvis du ikke har fuldført procedurerne, skal du fuldføre dem og derefter vende tilbage til dette emne.

## <a name="register-a-plug-in"></a>Registrer en plug-in
Når der oprettes en tilbudslinjedetalje på siden **Tilbudslinje** for en linje i en projekttilbud, oprettes der to estimatlinjer i systemet. En linje til omkostningssiden af estimatet, og en anden linje til salgssiden. Det samme gælder for projektkontraktlinjer.

Når du foretager en ændring af mængden eller et felt på omkostningssiden, foretages denne ændring også på salgssiden. Dette er muligt, fordi plug-ins til forudhandling i objekterne tilbudslinjedetalje og kontraktlinedetalje knytter bestemte attributter på omkostningssiden til salgssiden i transaktionen. Hvis du har brug for at foretage ændringer i prisfastsættelsesdimensionsværdierne på salgssiden, som også skal udføres på omkostningssiden, skal følgende plug-ins registreres igen, når du har foretaget ændringer af en prisfastsættelsesdimension.

Disse plug-ins bruges til at opdatere og registrere data igen:

- PreOperationContractLineDetailUpdate - **Opdater msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Opdaterer msdyn_quotelinetransaction**

Udfør følgende trin for at opdatere og registrere plug-ins igen.

1. Åbn **PluginRegistrationTool**, og opret forbindelse til Project Operations Dataverse-miljøet.
2. Vælg **Søg**, og skriv de første bogstaver i det plug-in, der skal opdateres.
3. Når plug-in'en er fundet, skal du markere den og derefter vælge **Vælg i hovedformular**.
4. Vælg trinnet **Opdater msdyn_orderlinetransaction**, højreklik på det, og vælg derefter **Opdater**.
5. På dialogsiden **Opdater** skal du klikke på ellipseknappen (**...**) i filtreringsattributterne.
6. Vinduet med filtreringsattributter åbnes, og der vises en liste over alle attributter i objekt- og prisfastsættelsesdimensionerne. Markér afkrydsningsfelterne ud for prisfastsættelsesdimensionsattributterne.
7. Vælg **OK** for at lukke siden, og vælg derefter **Opdater trin**.
8. Gentag trin 2-7 for den anden plug-in **PreOperationQuoteLineDetail**. For denne plug-in skal du opdatere trinnet **Opdatering af msdyn_quotelinetransaction**.
9. Luk **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]