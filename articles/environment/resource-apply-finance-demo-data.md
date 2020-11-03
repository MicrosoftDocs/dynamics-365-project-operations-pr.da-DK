---
title: Anvend demonstrationsdata for Project Operations på et skybaseret Finance-miljø
description: Dette emne beskriver, hvordan du anvender demonstrationsdata fra Project Operations til et skybaseret Dynamics 365 Finance-miljø.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096615"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Anvend demonstrationsdata for Project Operations på et skybaseret Finance-miljø

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

> [!IMPORTANT]
> Dette emne gælder kun for Microsoft Dynamics 365 Finance version 10.0.13 og kan kun udføres i et skybaseret miljø. Gennemfør trinnene i dette emne, **FØR** du anvender kvalitetsopdateringer på miljøet.

1. I dit LCS-projekt skal du åbne siden **Miljødetaljer**. Bemærk, at det indeholder de oplysninger, der skal bruges for at oprette forbindelse til miljøet ved hjælp af RDP (Fjernskrivebordsprotokol).

![Detaljer for -miljø](./media/1EnvironmentDetails.png)

Det første sæt af fremhævede legitimationsoplysninger er legitimationsoplysninger til den lokale konto og indeholder et link til forbindelse til fjernskrivebord. Legitimationsoplysningerne omfatter administrators brugernavn og adgangskode for miljøet. Det andet sæt legitimationsoplysninger bruges til at logge på SQL Server i dette miljø.

2. Opret fjernforbindelse til miljøet ved hjælp af linket i **Lokale Konti** , og brug **Legitimationsoplysningerne** for at autorisere.
3. Gå til **Internet Information Services** > **Programgrupper** > **AOSService** , og stands tjenesten. Du er ved at stoppe tjenesten på dette tidspunkt, så du kan fortsætte med at erstatte SQL-databasen.

![Stands AOS](./media/2StopAOS.png)

4. Gå til **Tjenester** , og stop følgende to elementer:

- Microsoft Dynamics 365 Unified Operations: Batch Management Service
- Microsoft Dynamics 365 Unified Operations: Data Import Export Framework

![Stop tjenester](./media/3StopServices.png)

5. Åbn Microsoft SQL Server Management Studio. Log på med SQL Server-legitimationsoplysninger, og brug axdbadmin-brugeren og -adgangskoden fra siden med LCS- **Miljøoplysninger**.

![SQL Server Management Studio](./media/4SSMS.png)

6. I Object Explorer, **Databaser** og find **AXDB**. Du skal erstatte databasen med en ny database, der findes i [Downloadcenteret](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopier zip-filen til den VM, du har fjernforbindelse til, og udpak indholdet.
8. I SQL Server Management Studio skal du højreklikke på **AxDB** og derefter vælge **Opgaver** > **Gendan** > **Database**.

![Gendan database](./media/5RestoreDatabase.png)

9. Vælg **Kildeenhed** , og naviger til den fil, du har kopieret fra den zip-fil, som du kopierede.

![Kildeenheder](./media/6SourceDevice.png)

10. Vælg **Indstillinger** , og vælg derefter **Overskriv den eksisterende database** , og **Luk eksisterende forbindelser til destinationsdatabasen**. 
11. Vælg **OK**.

![Gendan indstillinger](./media/7RestoreSetting.png)

Du modtager en bekræftelse på, at AXDB-gendannelsen blev fuldført. Når du har modtaget denne bekræftelse, kan du lukke SQL Services Management Studio.

12. Gå tilbage til **Internet Information Services** > **Programgrupper** > **AOSService** , og start AOSService.
13. Gå til **Tjenester** , og start de to tjenester, du standsede tidligere.

14. Find AdminUserProvisioning-værktøjet på denne VM. Se under K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Kør .ext-filen ved hjælp af din brugeradresse i feltet **Mailadresse**. 
16. Vælg **Send**.

![Administratorbrugerklargøring](./media/8AdminUserProvisioning.png)

Dette tager et par minutter at fuldføre. Du bør modtage en bekræftelsesmeddelelse om, at administratorbrugeren blev opdateret korrekt.

17. Endelig skal du køre kommandoprompt som administrator og nulstille IIS

![Nulstil IIS](./media/9IISReset.png)

18. Luk fjernskrivebordssessionen, og brug siden med LCS- **Miljødetaljer** til at logge på miljøet for at bekræfte, at den fungerer som forventet.

![Finance and Operations](./media/10FinanceAndOperations.png)
