---
title: Tilmeld dig prøveversioner af Project Operations
description: Dette emne indeholder oplysninger om, hvordan du udruller en prøveversion af Dynamics 365 Project Operations.
author: ruhercul
ms.date: 12/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e40b4ac23241730f5c2db89f0dc674083f9e7abe
ms.sourcegitcommit: 8f970b46d0303dafaa75fc7d00567d232e1e600b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901610"
---
# <a name="sign-up-for-project-operations-trials"></a>Tilmeld dig prøveversioner af Project Operations 

_**Gælder for:** Project Operations for ressource/ikke-lagerbaserede scenarier, lille udrulning - aftale om proformafakturering og Project Operations for lagerbaserede/produktionsbaserede scenarier_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emne forklarer, hvordan du abonnerer på vores partneres tilbud om forhåndsvisning og udrulning af et Dynamics 365 Project Operations-miljø.

Med den nye prøveversion af Project Operations kan du automatisk udrulle et af de tre understøttede udrulningsscenarier ved at udfylde et spørgeskema, som anbefaler den bedste udrulningsmetode. Dette emne indeholder oplysninger om, hvordan du:

- Accepterer dit prøvetilbud.
- Starter klargøring.
- Konfigurer dobbeltskrivning.
- Få mere at vide om Project Operations. 

I følgende tabel beskrives detaljerne i det nye prøvetilbud.

| **Tilbudselement**               | **Oplysninger**                                  |
|------------------------------|----------------------------------------------|
| Tilbudstype                   | Denne tilbudstype er et administratorkundeemne, hvorfor kun en lejeradministrator kan accepterer tilbuddet. |
| Tilbuddets anvendelse                    | Én gang pr. lejer                          |
| Tilbuddets varighed               | 30 kalenderdage                             |
| Accepter pr. lejer       | 0                                            |
| Antal brugere              | 25                                           |
| Filtypenavn                    | En udvidelse, 30 kalenderdage               |
| Antal prøveversionsmiljøer | 3                                            |


## <a name="admin-trial-details"></a>Oplysninger om administrationsprøveversioner
I følgende tabel vises detaljerne om prøveversionen, og hvordan de finder anvendelse for hver udrulningstype.

| **Punkt**                      | **Lille**                                     | **Ikke-lagerførte materialer** | **Lagerførte materialer** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Konfigurer leverede data           | Ja                                          | Ja                       | Ja (USSI)            |
| Transaktionsdata            | Nr.                                           | Nr.                        | Nr.                    |
| Klargøringstid i minutter  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Forudsætninger
Følgende forudsætninger skal være opfyldt, før du kan udrulle en prøveversion af Dynamics 365 Project Operations.

- Tilmeld dig [Dynamics 365 Project Operations - prøveversion](https://www.aka.ms/try-po).
- Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder.

> [!IMPORTANT]
> Denne opgave skal kun udføres af én person i en organisation, nemlig administratoren for lejere. Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations- prøveversion 

Inden du begynder, skal du logge på en browser med brugerkontoen i den lejer, hvor du ønsker, at forhåndsversionens af Project Operations skal installeres.

1. Accepter den første tilbudskode, **Dynamics 365 Project Operations -prøveversion** ved at indsætte den i browserens URL.

    ![Accepter tilbud](./media/16RedeemFirstOfferNew.png)

2. Bekræft din ordre..

    ![Bekræft ordren](./media/17ConfirmOrderNew.png)

  Du vil dernæst se, at bekræftelsestilbuddet blev gennemført korrekt.

   ![Bekræftelse](./media/18OrderConfirmationNew.png)

  Du vil blive omdirigeret til [Power Platform Administration](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Spørgeskema og klargøring

1.  Gå til [Power Platform Administration](https://admin.powerplatform.com/projectoperationstrial), og udfyld spørgeskemaet.  
2.  Gennemse den anbefalede udrulningstype, og vælg **Start konfiguration** for at starte klargøring.
3.  Gennemse vilkårene og betingelserne, og vælg derefter **Start**.

   Når klargøring er startet, omdirigeres du til miljølisten i Power Platform Administration. Mens klargøring er i gang, er tilstanden for dit miljø **PreparingInstance**.
 
  Når klargøring er fuldført, er tilstanden for miljøet **Klar**. Klargøring af miljøet omfatter udrulning af demodata.
 
4.  Vælg den respektive URL-adresse for Microsoft Dataverse og for Finance and Operations- apps for at validere udrulningen.

## <a name="configuring-dual-write"></a>Konfiguration af dobbeltskrivning
- Hvis du vil konfigurere sikkerhedsroller for dobbelt skrivning, skal du se [Opdatering af sikkerhedsindstillinger for Project Operations i Dataverse](resource-provision-new-environment.md).
- Hvis du vil konfigurere tilknytninger med dobbelt skrivning, skal du se [Kør tilknytninger af dobbelt skrivning i Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Tildele licenser

Du skal have administratoradgang til din organisations Microsoft 365-portal for at fuldføre følgende trin.

1. Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenserne til dine brugere.

   ![Startside for Administration](./media/14AdminPortal.png)

2. På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.

   ![Tildel licenser](./media/15AssignLicenses.png)

3. Kontrollér, at licensen til **Dynamics 365 Project Operations-forhåndsvisning** er valgt, og vælg derefter **Gem ændringer**.

## <a name="additional-resources"></a>Flere ressourcer

Følgende ressourcer indeholder nyttige vejledninger, når du starter arbejdet med Project Operations:

- [Videoserie - Oversigt over Project Operations med detaljeret gennemgang og oversigt](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Vælg din udrulningstype](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Hvad skal jeg gøre, hvis jeg har brug for ALM eller ELM til mine Finance and Operations-apps-miljøer?

- For partnere, der har brug for alle funktioner til administration af miljøets livscyklus, se [Anmodning til partnerlicens til sandkasse](https://experience.dynamics.com/requestlicense) for at gennemgå det nye partnertilbud. 
- For partnere, der ønsker flere oplysninger om interne brugsrettigheder, se [Interne brugerrettighedscloud og softwarefordele (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Kan jeg forlænge min prøveversion efter 30 dage?
Hvis du vil forlænge din prøveperiode, skal du fuldføre følgende trin.

1. I **Microsoft 365 Administration** skal du gå til **Fakturering** > **Dine produkter**.
2. Vælg **Dynamics 365 Project Operations (ce) - prøveversion**.
3. Under **Udløbsdato** skal du vælge **Forlæng dato**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Kan jeg opgradere fra den lille udrulning til ressource-/ikke-lagerbaseret scenarieudrulning?
I øjeblikket understøttes opgraderingen af et miljø fra en lille til en ikke-lagerbaseret udrulning ikke.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Kan jeg få adgang til Lifecycle Services (LCS) til mine Finance-miljøer?  
Nej. I disse prøveversioner håndteres udrulning via Power Platform Administration. Der er begrænset adgang til Finance-miljøet.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Kan jeg installere min prøveversion i et eksisterende miljø?
Hvis du har et eksisterende miljø, kan du få tilladelse til at installere den lille udrulning i et eksisterende Dataverse-salgsmiljø fra Power Platform Administration.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
