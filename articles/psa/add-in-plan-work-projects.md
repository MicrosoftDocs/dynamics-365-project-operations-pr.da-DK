---
title: Planlæg dit arbejde i Microsoft Project med tilføjelsesprogrammet Project Service
description: Dette emne indeholder oplysninger om, hvordan du kan bruge Microsoft Project-tilføjelsesprogrammet til Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145936"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planlæg dit arbejde i Microsoft Project med tilføjelsesprogrammet Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gør det lettere for dig at foretage din projektplanlægning, herunder estimater. Du kan definere arbejdet, så omkostninger, indsats og salgsværdi kan ses, når det endelige forslag er sendt.  

Du kan installere [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] og foretage dit planlægningsarbejde i det velkendte miljø i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Brug de effektive planlægnings- og styringsfunktioner i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og opdater derefter din projektplan i Project Service Automation.  

> [!IMPORTANT]
> - Hvis du vil bruge funktionen dokumentstyring i SharePoint til at gemme dine [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekter, skal din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-administrator slå dokumentstyring til. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] er kun kompatibel med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Hent og installer tilføjelsesprogrammet.  
 Hav dine [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-logonoplysninger ved hånden. Du skal bruge disse oplysninger til at oprette forbindelse fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  I Download Center kan du hente tilføjelsesprogrammet til din understøttede version af Project Service, enten [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Vælg overførelseslinket.  

3.  Når overførslen er fuldført, skal du vælge **Ja** for at installere tilføjelsesprogrammet.  

## <a name="configure-the-add-in"></a>Konfigurer tilføjelsesprogrammet.  

1. Åbn [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og vælg fanen **Project Service**.  

2. Vælg **Opret forbindelse**.  

3. Angiv dine logonoplysninger, og vælg derefter **Log på**.  

   Nu kan du gå i gang med at bruge tilføjelsesprogrammet.  

## <a name="read-from-a-template"></a>Læs fra en skabelon  
 Læs fra en skabelon, du har oprettet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] og kopieret til [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], for at starte projektplanlægningen. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Opret en projektskabelon (Project Service Automation)](../psa/create-project-template.md)  

1.  Fra fanen **Project Service** skal du vælge **Læs** > **Project Service Automation-projektskabelon**.  

2.  Vælg en skabelon på listen, og vælg derefter **Åbn**.  

    > [!NOTE]
    >  De opgaver, der kopieres fra skabelonen til projektet, er som standard manuelt planlagte.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Tildel [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller til projektressourcer  

1.  Åbn et projekt, og vælg båndet **Opgave**.  

2. Vælg menuen **Gantt-diagram**, og vælg derefter **Ressourceark**.  

3. Vælg rullemenuen **Project Service-ressourcerolle** på ressourcearket, og vælg en Project Service Automation-rolle.  

## <a name="staff-your-project-with-resources"></a>Tildel personaleressourcer til projektet  

1.  Vælg en række under fanen Project Service, og vælg **Find ressourcer**.  

2.  På skærmen **Reservér ressource** skal du vælge den ressource, du vil bruge til projektet.  

3.  Vælg **Reserver**, og vælg derefter **OK**.  

## <a name="publish-your-project"></a>Udgiv dit projekt  
Når projektplanlægningen er afsluttet, er næste trin at importere og udgive projektet til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projektet importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Processen til generering af pris og team anvendes. Åbn projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for at se, at gruppen, projektestimaterne og arbejdsopgavehierarkiet er blevet genereret. I følgende tabel vises, hvor du kan finde resultaterne.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt-diagrammer**   | Importeres i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Arbejdsopgavehierarki**-skærmbilledet. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ressourceark** |   Importeres i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Medlemmer af projektteam**-skærmbilledet.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Bruge anvendelse**    |    Import til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektestimater**-skærmbilledet.     |

**Sådan importerer og udgiver du projektet**  
1. På fanen **Project Service** skal du gå til **Udgiv** > **Nyt Project Service Automation-projekt**.  

2. I dialogboksen **Publicer til et nyt projekt i Project Service** skal du angive **Projektnavn** og vælge **Kunde**.  

3. Du kan også vælge **Sammenkæd projektplan med Project Service Automation** for at sammenkæde planens projektfil med Project Service Automation.  

4. Vælg **Udgiv**.  

   Hvis projektfilen sammenkædes med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bliver projektfilen master, og den angiver arbejdsopgavehierarkiet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til skrivebeskyttet.  Hvis du vil foretage ændringer i projektplanen, skal du foretage dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og udgive dem som opdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Rediger et projekt, der er blevet importeret  
 Hvis du vil foretage ændringer i en projektplan, der er importeret i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], har du to muligheder:  

- Åbn masterfilen, og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Fjern sammenkædning til filen, og rediger den direkte i Project Service. Som standard er et projekt, der er overført fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], låst og kan kun redigeres i Project. Hvis du vil redigere filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], skal sammenkædningen til filen være fjernet.  

### <a name="edit-in-pn_microsoft_project"></a>Rediger i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. I hovedmenuen skal du gå til **Project Service** > **Projekter**.  

2. Åbn det projekt, som du har oprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], på listen over projekter.  

3. Vælg **Åbn i MS Project** fra båndet. Derved åbnes den sammenkædede masterfil i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Fjern sammenkædning til en fil, og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. I hovedmenuen skal du gå til **Project Service** > **Projekter**.  

2. Åbn det projekt, som du har oprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], på listen over projekter.  

3. Vælg **Fjern link til MS Project** fra båndet.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Sende en Project-fil til SharePoint eller Office Grupper  
 Du kan overføre Project-filen til SharePoint og finde den under de tilknyttede dokumenter for dit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  Du skal bede din administrator om at konfigurere dokumentstyring i SharePoint og aktivere det for Project-enheden. 

 Du kan også overføre Project-filen til [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], hvis du har konfigureret Office Groups.

### <a name="upload-a-file-for-sharepoint"></a>Uploade en fil til SharePoint  

1. I hovedmenuen skal du gå til **Project Service** > **Upload**.  

2. Vælg **Til Project Service Automation-projektdokumenter**.  

3. I dialogboksen **Aktiver Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** skal du vælge **Ja** eller **Nej**.  

   - Hvis du vælger **Ja**, kan du vælge **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation, køre [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og indlæse Project-filen fra SharePoint-dokumentbiblioteket.  

   - Hvis du vælger **Nej**, fungerer linket for **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ikke.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen findes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det specifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  

### <a name="upload-a-file-for-office-groups"></a>Overfør en fil til Office Groups  

1. I hovedmenuen skal du gå til **Project Service** > **Upload**.  

2. Vælg **Til Project Service Automation-projektdokumenter**.  

3. I dialogboksen **Aktiver Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** skal du vælge **Ja** eller **Nej**.  

   - Hvis du vælger **Ja**, kan du vælge **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation, køre [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og indlæse Project-filen fra SharePoint-dokumentbiblioteket.  

   - Hvis du vælger **Nej**, fungerer linket for **Åbn i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ikke.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen findes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det specifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  

## <a name="publish--your-project-as-a-template"></a>Udgiv et projekt som en skabelon  
 Du kan gemme dit projekt og genbruge det ved at gemme det som en projektskabelon i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Projektskabeloner er projektplaner, der kan genbruges i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Du kan finde flere oplysninger under [Opret en projektskabelon (Project Service Automation)](../psa/create-project-template.md). 

1. På fanen **Project Service** skal du gå til **Udgiv** > **Ny projektskabelon i Project Service Automation**.  

2. I dialogboksen **Publicer til et nyt projekt i Project Service-skabelon** skal du angive **Navn på projektskabelon**.  

3. Du kan også vælge **Sammenkæd projektplan med Project Service Automation** for at sammenkæde projektfilen med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Vælg **Udgiv**.  

Hvis projektfilen sammenkædes med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bliver projektfilen master, og den angiver arbejdsopgavehierarkiet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-skabelonen til skrivebeskyttet.  Hvis du vil foretage ændringer i projektplanen, skal du foretage dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og udgive dem som opdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Læs en ressourceindlæst plan

Når du læser et projekt fra Project Service Automation, synkroniseres ressourcens kalender ikke med skrivebordsklienten. Hvis der er forskelle i opgavevarigheden, indsats eller sluttidspunkt, er det sandsynligvis fordi, at ressourcerne og skrivebordsklienten ikke har den samme arbejdstidsskabelon, som er anvendt på projektet.


## <a name="data-synchronization"></a>Datasynkronisering
Tabellerne i dette afsnit indeholder oplysninger om synkroniseringen af objektdata mellem Project Service Automation og tilføjelsesprogrammet Microsoft Project til skrivebordet.

### <a name="project-task-entity-table"></a>Tabel over projektopgaveobjekt
I følgende tabel beskrives det, hvordan objektdata for projektopgaven synkroniseres mellem Project Service Automation og tilføjelsesprogrammet Microsoft Project til skrivebordet.

| **Objekt** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Projektopgave | Forfaldsdato | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Anslået indsats | Synkroniseret | Ikke synkroniseret |
| Projektopgave | MS Project-klient-id | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Overordnet opgave | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Project | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Projektopgave | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Navn på projektopgave | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Ressourceenhed (udfaset i v3.0) | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Planlagt varighed | Synkroniseret | Ikke synkroniseret |
| Projektopgave | Startdato | Synkroniseret | Ikke synkroniseret |
| Projektopgave | WBS-id | Synkroniseret | Ikke synkroniseret |

### <a name="team-member-entity-table"></a>Tabel over teammedlemsobjektet
I følgende tabel beskrives det, hvordan objektdata for teammedlemmer synkroniseres mellem Project Service Automation og tilføjelsesprogrammet Microsoft Project til skrivebordet.

| **Objekt** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Teammedlem | MS Project-klient-id | Synkroniseret | Ikke synkroniseret |
| Teammedlem | Stillingsnavn | Synkroniseret | Ikke synkroniseret |
| Teammedlem | projekt | Synkroniseret | Synkroniseret |
| Teammedlem | Projektteam | Synkroniseret | Synkroniseret |
| Teammedlem | Ressourceenhed | Ikke synkroniseret | Synkroniseret |
| Teammedlem | Rolle | Ikke synkroniseret | Synkroniseret |
| Teammedlem | Arbejdstimer | Ikke synkroniseret | Ikke synkroniseret |

### <a name="resource-assignment-entity-table"></a>Tabel over ressourcetildelingsobjekt
I følgende tabel beskrives det, hvordan objektdata for ressourcetildeling synkroniseres mellem Project Service Automation og tilføjelsesprogrammet Microsoft Project til skrivebordet.

| **Objekt** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Ressourcetildeling | Fra-dato | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | Timer | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | MS Project-klient-id | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | Planlagt arbejde | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | Project | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | Projektteam | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | Ressourcetildeling | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | Opgave | Synkroniseret | Ikke synkroniseret |
| Ressourcetildeling | Til-dato | Synkroniseret | Ikke synkroniseret |

### <a name="project-task-dependencies-entity-table"></a>Tabel over objektet projektopgaveafhængigheder
I følgende tabel beskrives det, hvordan objektdata for projektopgaveafhængigheder synkroniseres mellem Project Service Automation og tilføjelsesprogrammet Microsoft Project til skrivebordet.

| **Objekt** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Projektopgaveafhængigheder | Projektopgaveafhængighed | Synkroniseret | Ikke synkroniseret |
| Projektopgaveafhængigheder | Linktype | Synkroniseret | Ikke synkroniseret |
| Projektopgaveafhængigheder | Foregående opgave | Synkroniseret | Ikke synkroniseret |
| Projektopgaveafhængigheder | Project | Synkroniseret | Ikke synkroniseret |
| Projektopgaveafhængigheder | Efterfølgende opgave | Synkroniseret | Ikke synkroniseret |

### <a name="additional-resources"></a>Flere ressourcer
 [Vejledning til projektledere](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]