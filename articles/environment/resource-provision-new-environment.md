---
title: Klargør et nyt miljø
description: Dette emne indeholder oplysninger om, hvordan du klargør et nyt Project Operations-miljø.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 03626cb1579fad7f8d8eb501905056cd13092754
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594801"
---
# <a name="provision-a-new-environment"></a>Klargør et nyt miljø

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_



Dette emne indeholder oplysninger om, hvordan du klargør et nyt Dynamics 365 Project Operations-miljø til ressource/ikke-lagerbaserede scenarier.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Aktivér automatisk klargøring af Project Operations i et LCS-projekt

Benyt følgende fremgangsmåde for at aktivere den automatiserede klargøring af Project Operations for dit LCS-projekt.

1. Gå til [LCS](https://lcs.dynamics.com/v2), og vælg feltet **Administration af prøveversionsfunktion**.
2. I listen **Prøveversionsfunktion** skal du vælge **Funktionen Project Operations** og dernæst vælge **Aktiver prøveversionsfunktion** for at aktivere Project Operations.

   > [!NOTE]
   > Dette trin udføres kun én gang pr. LCS-projekt.

## <a name="provision-a-project-operations-environment"></a>Klargør et Project Operations-miljø

1. Åbn et nyt [demomiljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) til Dynamics 365 Finance eller en udrulning af [et sandkasse-/produktionsmiljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Gennemgå guiden **Miljøklargøring**. 

   > [!IMPORTANT]
   > Kontrollér, at den valgte programversion er 10.0.13 eller nyere.

3. Hvis du vil klargøre Project Operations, skal du vælge **Avancerede indstillinger** og vælge **Common Data Service**. 
4. Aktiver **Common Data Service-indstillingen** ved at vælge **Ja** og derefter angive oplysninger i de påkrævede felter:

  - Navn
  - Land/område
  - Sprog
  - Valuta
 
5. I feltet **Common Data Service-skabelon** skal du vælge **Project Operations** 
6. Vælg miljøtypen til din udrulning. En abonnementsbaseret prøveversion giver dig mulighed for at installere et CDS-miljø i 30 dage. 

     ![Indstillinger for udrulning.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Vælg **Accepter** for at bekræfte servicebetingelserne, og vælg derefter **Udfør** for at vende tilbage til udrulningsindstillingerne.
    >
    >![Samtykke til udrulning.](./media/2DeploymentConsent.png)

7. Valgfrit - Anvend demodata på miljøet. Gå til **Avancerede indstillinger**, vælg **Tilpas SQL-databasekonfiguration**, og angiv **Angiv et datasæt for applikationsdatabase** til **Demo**.
8. Udfyld de resterende obligatoriske felter i guiden, og bekræft udrulningen. Den tid, det tager at klargøre miljøet, varierer, afhængigt af miljøtypen. Klargøringen kan tage op til seks timer.

   Når udrulningen er fuldført, vises miljøet som **Udrullet**.

9. Du kan kontrollere, at miljøet er blevet udrullet korrekt ved at vælge **Logon** og logge på miljøet.

    ![Oplysninger om miljø.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Anvend opdateringer på Finance-miljøet

Project Operations kræver et Finance-miljø med programversion **10.0.13 (10.0.569.20009)** eller nyere.

Det kan være nødvendigt at anvende kvalitetsopdateringer i dit Finance-miljø for at modtage denne version.

1. I LCS skal du på siden **Miljødetaljer** i sektionen **Tilgængelige opdateringer** vælge **Vis opdatering**.

    ![Vis opdateringer.](./media/5ViewUpdates.png)

2. På siden **Binære opdateringer** skal du vælge **Gem pakke**.

    ![Gem pakke.](./media/6SavePackage.png)

3. Klik på **Vælg alle** og vælg derefter **Gem pakke**.

    ![Gennemse og gem opdateringer.](./media/7ReviewAndSaveUpdates.png)

4. Angiv et navn for og en beskrivelse af pakken, og vælg derefter **Gem**. Afhængigt af internetforbindelsen kan denne proces tage et stykke tid.

    ![Overfør pakken til aktivbiblioteket.](./media/8UploadPackageToAssetsLibrary.png)

5. Når pakken er blevet gemt, skal du vælge **Udført** og gemme denne pakke i aktivbiblioteket i dit LCS-projekt.

   Det kan tage op til mere end 15 minutter at gemme og validere pakken.

6. Hvis du vil anvende opdateringen, skal du gå til siden med **Miljødetaljer** i LCS og vælge **Vedligehold** > **Anvend opdateringer**.

    ![Vedligehold miljøer.](./media/9MaintainEnvironment.png)

7. Vælg den pakke, du har oprettet, på listen over opdateringer, og vælg **Anvend**.

    ![Anvend opdateringer.](./media/10ApplyUpdates.png)

   Det vil tage et stykke tid at vedligeholde miljøet. Når installationen er fuldført, vil miljøet vende tilbage til en udrullet tilstand.

    ![Udrullet miljø.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Opret en forbindelse til dobbelt skrivning 

1. I dit LCS-projekt skal du gå til siden **Miljødetaljer**.
2. Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps**.
3. Når forbindelsen er oprettet, skal du vælge **Forbind til CDS for Apps** igen. Du bliver omdirigeret til dobbelt skrivning i Finance.

    ![Link til CDS.](./media/12LinktoCDS.png)

4. Vælg **Anvend løsning** for at få adgang til de objekter, der skal tilknyttes i integrationen.

    ![Anvend løsninger.](./media/13ApplySolutions.png)

5. Vælg begge løsninger, **Tilknytningsobjektet til Dynamics 365 Finance and Operations med dobbelt skrivning** og **Tilknytningsobjektet til Dynamics 365 Project Operations med dobbelt skrivning**, og vælg derefter **Anvend**.

    ![Bekræft løsninger.](./media/14ConfirmSolutions.png)

    Når løsningerne er anvendt, anvendes dobbelt skrivningsobjekter på miljøet.

    ![Anvendelse af løsninger.](./media/15ApplyingSolutions.png)

    Når objekterne er anvendt, vises alle tilgængelige tilknytninger i miljøet.

    ![Tilknytninger for dobbeltskrivning.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Opdater dataobjekterne efter opdateringen

1. I Finance skal du gå til arbejdsområdet **Dataadministration**.

    ![Arbejdsområdet Dataadministration.](./media/16DataManagement.png)

2. Vælg feltet **Strukturparametre**.

    ![Strukturparametre.](./media/17FrameworkParameters.png)

3. På siden **Objektindstillinger** skal du vælge **Opdater objektliste**.

    ![Opdater objektliste.](./media/18RefreshEntityList.png)

Opdateringen tager ca. 20 minutter. Du modtager en besked, når den er fuldført.

  ![Opdater bekræftelse.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Opdater sikkerhedsindstillingerne for Project Operations på Dataverse

1. Gå til Project Operations på dit Dataverse-miljø. 
2. Gå til **Indstillinger** > **Sikkerhed** > **Sikkerhedsroller**. 
3. På siden **Sikkerhedsroller** skal du fra listen med roller vælge **applikationsbruger med dobbeltskrivning** og vælge fanen **Brugerdefinerede objekter**.  
4. Kontrollér, at rollen har tilladelserne **Læs** og **Tilføj til** for følgende objekter:
      
      - **Type af valutakurs**
      - **Kontoplan**
      - **Regnskabskalender**
      - **Hovedbog**
      - **Firma**
      - **Udgift**

5. Når sikkerhedsrollen er blevet opdateret, skal du gå til **Indstillinger** > **Sikkerhed** > **Teams** og vælge standardteamet i teamvisningen **Lokal virksomhedsejer**.
6. Vælg **Administrer roller**, og kontrollér, at sikkerhedsrettigheden **applikationsbruger med dobbeltskrivning** gælder for dette team.

## <a name="run-project-operations-dual-write-maps"></a>Kør Project Operations dobbelt skrivningstilknytninger

1. I dit LCS-projekt skal du gå til siden **Miljødetaljer**.
2. Under **Common Data Service-miljøoplysninger** skal du vælge **Forbind til CDS for Apps.** Når du har valgt forbindelsen, bliver du omdirigeret til listen over objekter i tilknytningerne.
3. Start tilknytningerne. Du kan finde flere oplysninger i [Versioner af tilknytning af dobbeltskrivning i Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Valider, at alle projektrelaterede tilknytninger er i kørselstilstand.

    ![Alle tilknytninger kører.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Anvend konfigurationsdata i CDS for Project Operations (valgfrit)

Hvis du har anvendt demodata i Finance-miljøet, skal du se [Konfigurere og anvende konfigurationsdata i Common Data Service til Project Operations](resource-apply-pro-setup-config-data.md) for at anvende demodata i CDS-miljøer.


Dit Project Operations-miljø er nu klargjort og konfigureret. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
