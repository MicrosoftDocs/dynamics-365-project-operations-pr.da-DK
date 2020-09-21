---
title: Installation af eksempeldata
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750470"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="80f76-102">Installation af eksempeldata til programmet Project Service</span><span class="sxs-lookup"><span data-stu-id="80f76-102">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="80f76-103">For at hjælpe dig med at udvikle dine egne demonstrationsmiljøer leverer Microsoft eksempeldata, som du kan downloade, og som præsenterer funktionerne i dine apps.</span><span class="sxs-lookup"><span data-stu-id="80f76-103">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="80f76-104">Der findes to typer eksempeldatapakker:</span><span class="sxs-lookup"><span data-stu-id="80f76-104">There are two types of sample data packages:</span></span>
- <span data-ttu-id="80f76-105">reference/installationsdata</span><span class="sxs-lookup"><span data-stu-id="80f76-105">reference/setup data</span></span>
- <span data-ttu-id="80f76-106">demonstrationsdata (reference/installations- og transaktionsdata som arbejdsordrer og projekter)</span><span class="sxs-lookup"><span data-stu-id="80f76-106">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="80f76-107">Pakkerne med eksempeldata til **reference** kan hentes i tre separate pakker, så du kan vælge kun at installere data for Project Service eller kun for Field Service, eller du kan installere eksempeldata for begge programmer på samme tid.</span><span class="sxs-lookup"><span data-stu-id="80f76-107">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="80f76-108">Der er følgende eksempelinstallations-/referencedatapakker:</span><span class="sxs-lookup"><span data-stu-id="80f76-108">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="80f76-109">**V902PSMasterData** - Kun Project Service version 3.x</span><span class="sxs-lookup"><span data-stu-id="80f76-109">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="80f76-110">**V902FSMasterData** - Kun Field Service version 8.x</span><span class="sxs-lookup"><span data-stu-id="80f76-110">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="80f76-111">**V902FPSMasterData** - Field Service 8.x og Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="80f76-111">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="80f76-112">Den nyeste **demo** datapakke er:</span><span class="sxs-lookup"><span data-stu-id="80f76-112">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="80f76-113">**FPSDemoData** - Field Service 8.x og Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="80f76-113">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="80f76-114">Installationsvejledningen har lidt forskellige afsnit om brugeroprettelse og -konfiguration, men resten er det samme som i det forrige [**blogindlæg**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="80f76-114">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="80f76-115">Denne pakke indeholder et reduceret demonstrationsdatasæt og tager ca. 3 timer at installere.</span><span class="sxs-lookup"><span data-stu-id="80f76-115">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="80f76-116">Disse eksempeldatapakker er kun tilgængelige på engelsk.</span><span class="sxs-lookup"><span data-stu-id="80f76-116">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80f76-117">**Det er ikke muligt at afinstallere eksempeldataene.**</span><span class="sxs-lookup"><span data-stu-id="80f76-117">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="80f76-118">Derfor skal du kun installere disse pakker på demonstrations-, evaluerings-, øvelses- eller testsystemer.</span><span class="sxs-lookup"><span data-stu-id="80f76-118">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="80f76-119">Bemærk også, at du ikke kan installere en individuel pakke og derefter installere den anden individuelle pakke.</span><span class="sxs-lookup"><span data-stu-id="80f76-119">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="80f76-120">(Med andre ord kan du ikke installere **FSMasterData** efterfulgt af **PSMasterData** eller omvendt). Hvis du tror, at du kommer til at mangle eksempeldata til begge programmer på et senere tidspunkt, skal du installere **v902FPSMasterData**-pakken.</span><span class="sxs-lookup"><span data-stu-id="80f76-120">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="80f76-121">Når du installerer en eksempeldatapakke, udfører installationsprocessen følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="80f76-121">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="80f76-122">Opretter eller angiver standardparametre til brug af Project Service, Field Service eller begge programmer (hvis relevant).</span><span class="sxs-lookup"><span data-stu-id="80f76-122">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="80f76-123">Importerer eksempeldata til programmerne, f.eks. reserverbare ressourcer, programspecifikke roller, salgs- og kostprislister, organisationsenheder, salgsprocesposter og andre objekter, der viser vigtige egenskaber.</span><span class="sxs-lookup"><span data-stu-id="80f76-123">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="80f76-124">Med **demonstrationsdata**-pakken får du ovennævnte og yderligere transaktionsdata som f.eks. arbejdsordrer og projekter.</span><span class="sxs-lookup"><span data-stu-id="80f76-124">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="80f76-125">Vil du vide, hvilke funktioner du kan bruge i demoudgaver med eksempeldataene?</span><span class="sxs-lookup"><span data-stu-id="80f76-125">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="80f76-126">Se det fiktive Fabrikam Robotics-scenario nedenfor i [Tekniske bemærkninger](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="80f76-126">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="80f76-127">Hvis du har spørgsmål om installation af disse data eksempelpakker, kan du [sende en e-mail til fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="80f76-127">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="80f76-128">Krav</span><span class="sxs-lookup"><span data-stu-id="80f76-128">Requirements</span></span>

<span data-ttu-id="80f76-129">Installationsprotokollen antager følgende om din målforekomst (organisation):</span><span class="sxs-lookup"><span data-stu-id="80f76-129">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="80f76-130">Udgangssproget er engelsk, og grundvalutaen er amerikanske dollar (USD, $).</span><span class="sxs-lookup"><span data-stu-id="80f76-130">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="80f76-131">Organisationen har på forhånd ingen Project Service- eller Field Service-data eller har kun barebone-standarddata, der følger med enhver ny organisation.</span><span class="sxs-lookup"><span data-stu-id="80f76-131">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="80f76-132">Den korrekte version af virksomhedsprogrammet er allerede installeret:</span><span class="sxs-lookup"><span data-stu-id="80f76-132">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="80f76-133">**For FPSDemoData eller v902FPSMasterData:** Organisationen har Field Service version 8.x og Project Service version 3.x installeret.</span><span class="sxs-lookup"><span data-stu-id="80f76-133">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="80f76-134">**For v902PSMasterData:** Organisationen har Project Service version 3.x installeret.</span><span class="sxs-lookup"><span data-stu-id="80f76-134">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="80f76-135">**For v902FSMasterData:** Organisationen har Field Service version 8.x installeret.</span><span class="sxs-lookup"><span data-stu-id="80f76-135">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="80f76-136">Hvis du har brug for at installere eksempeldataene oven på en eksisterende Project Service- eller Field Service-prøveversion eller -demomiljø, der allerede har data (anbefales ikke), skal du deaktivere de forhåndskontroller af sikkerheden, der udføres af installationsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="80f76-136">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="80f76-137">Du kan finde flere oplysninger under Tekniske bemærkninger nedenfor.</span><span class="sxs-lookup"><span data-stu-id="80f76-137">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="80f76-138">Gøre klar til installation</span><span class="sxs-lookup"><span data-stu-id="80f76-138">Prepare for installation</span></span>

<span data-ttu-id="80f76-139">Du skal køre installationsprogrammet på en computer med en nyere version af Windows (Windows 10 foretrækkes).</span><span class="sxs-lookup"><span data-stu-id="80f76-139">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="80f76-140">Du skal sørge for, at computeren fortsat kan have forbindelse til et netværk, og at installationen kan køre i op til **1 time** for **installations-/referencedata**.</span><span class="sxs-lookup"><span data-stu-id="80f76-140">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="80f76-141">(Normalt tager installationen ca. 30 minutter for **FPSMasterData**, som indeholder eksempeldata til begge programmer). For **FPSDemoData** tager installationen omkring **3 timer**.</span><span class="sxs-lookup"><span data-stu-id="80f76-141">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="80f76-142">Computerens pauseskærm skal være slået fra.</span><span class="sxs-lookup"><span data-stu-id="80f76-142">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="80f76-143">I modsat fald kan sessionslegitimationsoplysningerne for installationen gå tabt, når pauseskærmen aktiveres (medmindre du holder sessionen aktiv under hele forløbet).</span><span class="sxs-lookup"><span data-stu-id="80f76-143">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="80f76-144">![Skærmbillede af indstillinger for pauseskærm med pauseskærmen slået fra](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="80f76-144">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="80f76-145">Hente og pakke ud</span><span class="sxs-lookup"><span data-stu-id="80f76-145">Download and unpack</span></span>

<span data-ttu-id="80f76-146">Installationsprogrammet til Project Service- og Field Service-eksempeldata distribueres som en selvudpakkende eksekverbar fil.</span><span class="sxs-lookup"><span data-stu-id="80f76-146">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="80f76-147">Filnavnene kan variere afhængigt af pakken med eksempeldata, men ellers er trinnene de samme, uanset hvilken pakke du installerer.</span><span class="sxs-lookup"><span data-stu-id="80f76-147">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="80f76-148">Når du har hentet en pakke, skal du køre exe-filen og derefter acceptere vilkår og betingelser for at pakke den komprimerede zip-fil ud.</span><span class="sxs-lookup"><span data-stu-id="80f76-148">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="80f76-149">Derefter skal du pakke indholdet af den pågældende fil ud i en mappe på computeren.</span><span class="sxs-lookup"><span data-stu-id="80f76-149">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="80f76-150">Afhængigt af operativsystemet og sikkerhedsindstillingerne skal du evt. udføre følgende trin efter udpakningen af zip-filen:</span><span class="sxs-lookup"><span data-stu-id="80f76-150">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="80f76-151">Find og højreklik på filen **FPSDemoData.dll** i mappen **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="80f76-151">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="80f76-152">Vælg **Fjern blokering**.</span><span class="sxs-lookup"><span data-stu-id="80f76-152">Choose **Unblock**.</span></span>

3. <span data-ttu-id="80f76-153">Vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="80f76-153">Select **Apply**.</span></span>

4. <span data-ttu-id="80f76-154">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80f76-154">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="80f76-155">Oprette eller konfigurere brugere</span><span class="sxs-lookup"><span data-stu-id="80f76-155">Create or configure users</span></span>

<span data-ttu-id="80f76-156">Pakken **FPSDemoData** kræver seks brugere, mens **FPSMasterData**-pakker kræver én bruger.</span><span class="sxs-lookup"><span data-stu-id="80f76-156">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="80f76-157">Referer til den rigtige for eksempeldatapakken.</span><span class="sxs-lookup"><span data-stu-id="80f76-157">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="80f76-158">Oprette eller konfigurere brugere – installations-/referencedatapakker</span><span class="sxs-lookup"><span data-stu-id="80f76-158">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="80f76-159">Pakken **FPSMasterData** er beregnet til installation med én bruger, der hedder Spencer Low, med de indstillinger, der er beskrevet her.</span><span class="sxs-lookup"><span data-stu-id="80f76-159">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="80f76-160">For at installere pakken korrekt skal du oprette (eller midlertidigt omdøbe) brugere i dit miljø, så de passer til den indgående konfiguration for eksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="80f76-160">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="80f76-161">Når du vil oprette eller konfigurere brugere, skal du gå til **Indstillinger** > **Sikkerhed** > **Brugere** og gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="80f76-161">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="80f76-162">Angiv UserFullname = "Spencer Low" med brugernavnet "spencerl" (**små bogstaver**) til rollerne Projektleder og Praksisleder.</span><span class="sxs-lookup"><span data-stu-id="80f76-162">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="80f76-163">Vælg brugeren **Spencer Low**, og vælg derefter **Administrer roller**.</span><span class="sxs-lookup"><span data-stu-id="80f76-163">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="80f76-164">Find og vælg rollen **Systemadministrator**, og vælg derefter **OK** for at tildele fulde administratorrettigheder til Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="80f76-164">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="80f76-165">Dette trin er nødvendigt for at sikre, at eksempelposter oprettes med det korrekte brugerejerskab og derfor udfylder visninger korrekt.</span><span class="sxs-lookup"><span data-stu-id="80f76-165">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="80f76-166">Fra den hentede pakke skal du opdatere en datatilknytningsfil med e-mailadresser for standardbrugerkonteksten.</span><span class="sxs-lookup"><span data-stu-id="80f76-166">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="80f76-167">Det gør du ved at åbne **PkgFolder** og derefter finde og åbne filen **ImportUserMapFile.xml** i Notesblok (eller Visual Studio eller en anden XML-editor).</span><span class="sxs-lookup"><span data-stu-id="80f76-167">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="80f76-168">Indstil feltet **DefaultUserToMapTo =** til e-mailadresse for brugeren Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="80f76-168">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="80f76-169">Hvis du ikke bruger Spencer Low med brugernavnet **spencerl**, skal du opdatere endnu en fil.</span><span class="sxs-lookup"><span data-stu-id="80f76-169">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="80f76-170">Åbn filen **DemoDataPreImportConfig.xml**, og find derefter mærket **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="80f76-170">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="80f76-171">Opdater **\<logon\>**-mærket med brugernavnet på din Spencer Low-bruger.</span><span class="sxs-lookup"><span data-stu-id="80f76-171">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="80f76-172">Du kan finde flere oplysninger under [Tekniske bemærkninger](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="80f76-172">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="80f76-173">Oprette eller konfigurere brugere - demodatapakke</span><span class="sxs-lookup"><span data-stu-id="80f76-173">Create or configure users - demo data package</span></span>

<span data-ttu-id="80f76-174">Demodatapakken kræver seks brugere.</span><span class="sxs-lookup"><span data-stu-id="80f76-174">The demo data package requires six users.</span></span> <span data-ttu-id="80f76-175">For at pakken skal blive installeret korrekt, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="80f76-175">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="80f76-176">Oprette eller midlertidigt omdøbe eksisterende brugere, så de svarer til konfigurationen af indgående eksempeldata, ved at gå til **Indstillinger** > **Sikkerhed** > **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="80f76-176">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="80f76-177">Disse roller er kun nødvendige i forbindelse med personligt baserede demoer.</span><span class="sxs-lookup"><span data-stu-id="80f76-177">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="80f76-178">Brugers Fullname="David So" som servicetekniker</span><span class="sxs-lookup"><span data-stu-id="80f76-178">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="80f76-179">Brugers Fullname="Jamie Reding" som koordinator af kundeservice og teknisk service</span><span class="sxs-lookup"><span data-stu-id="80f76-179">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="80f76-180">Brugers Fullname="Molly Clark" som regnskabschef</span><span class="sxs-lookup"><span data-stu-id="80f76-180">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="80f76-181">Brugers Fullname= "Spencer Low" som praksis- og projektleder</span><span class="sxs-lookup"><span data-stu-id="80f76-181">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="80f76-182">Brugers Fullname="Veronica Quek" som teammedlem</span><span class="sxs-lookup"><span data-stu-id="80f76-182">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="80f76-183">Brugers Fullname="William Contoso"</span><span class="sxs-lookup"><span data-stu-id="80f76-183">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="80f76-184">Hvad angår import af demonstrationsdata, skal du tildele de seks brugere over Administrator-rollen, så eksempelposterne importeres korrekt.</span><span class="sxs-lookup"><span data-stu-id="80f76-184">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="80f76-185">Åbn **PkgFolder**, og find og åbn derefter **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="80f76-185">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="80f76-186">Opdater **New=** felterne til mailadresserne på de tilsvarende brugere i systemet.</span><span class="sxs-lookup"><span data-stu-id="80f76-186">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="80f76-187">![Skærmbillede af UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="80f76-187">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="80f76-188">Hvis "Spencer Low" full name-brugeren har et andet bruger-id end **"spencerl"**, skal du opdatere endnu en fil.</span><span class="sxs-lookup"><span data-stu-id="80f76-188">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="80f76-189">Åbn **DemoDataPreImportConfig.xml**, og find mærket **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="80f76-189">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="80f76-190">Opdater **\<login\>**-mærket med loginId'et (der skelnes mellem store og små bogstaver).</span><span class="sxs-lookup"><span data-stu-id="80f76-190">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="80f76-191">Den første brugers kalender (i mærket **userstocreateandconfigure**) bruges til at angive arbejdstimerne for alle reserverbare ressourcer ved import af demonstrationsdata.</span><span class="sxs-lookup"><span data-stu-id="80f76-191">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="80f76-192">Naviger til **Indstillinger** > **Sikkerhed** > **Brugere**, søge efter brugeren "Spencer Low", og åbn indstillingen "Arbejdstimer".</span><span class="sxs-lookup"><span data-stu-id="80f76-192">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="80f76-193">Rediger de eksisterende arbejdstimer ved at vælge indstillingen **Hele den gentagne ugeplan fra start til slut**.</span><span class="sxs-lookup"><span data-stu-id="80f76-193">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="80f76-194">Sørg for, at **Arbejdstimer er indstillet til 8 AM - 5 PM (9 timer), mandag til fredag og med tidszonen indstillet til Pacific Time (USA og Canada)**.</span><span class="sxs-lookup"><span data-stu-id="80f76-194">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="80f76-195">Dette er nødvendigt for at sikre, at området med projektplanen og tidsplanen vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="80f76-195">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="80f76-196">**Anbefaling:** Overvej at oprette en sikkerhedskopi af din organisation nu, som du kan bruge, hvis du får brug for at vende tilbage til udgangspunktet, hvis noget går galt under installationen af eksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="80f76-196">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="80f76-197">Du kan finde flere oplysninger under [Sikkerhedskopiering og gendannelse af forekomster](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="80f76-197">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="80f76-198">Køre Package Deployer</span><span class="sxs-lookup"><span data-stu-id="80f76-198">Run the Package Deployer</span></span>

1. <span data-ttu-id="80f76-199">Find og kør **PackageDeployer.exe** i mappen **v902FPSMasterData** ELLER mappen **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="80f76-199">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="80f76-200">Acceptér vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="80f76-200">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="80f76-201">I det næste vindue:</span><span class="sxs-lookup"><span data-stu-id="80f76-201">On the next window:</span></span>

   <span data-ttu-id="80f76-202">a.</span><span class="sxs-lookup"><span data-stu-id="80f76-202">a.</span></span> <span data-ttu-id="80f76-203">Vælg installationstype **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="80f76-203">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="80f76-204">b.</span><span class="sxs-lookup"><span data-stu-id="80f76-204">b.</span></span> <span data-ttu-id="80f76-205">Brug brugeren og adgangskoden for den systemadministrator, der er konfigureret i "Oprette eller konfigurere brugere" ("Spencer Low" med brugernavnet "spencerl").</span><span class="sxs-lookup"><span data-stu-id="80f76-205">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="80f76-206">c.</span><span class="sxs-lookup"><span data-stu-id="80f76-206">c.</span></span> <span data-ttu-id="80f76-207">Kontroller, at **Vis en liste over tilgængelige organisationer** er valgt.</span><span class="sxs-lookup"><span data-stu-id="80f76-207">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="80f76-208">![Skærmbillede af Package Deployer-vinduet med valg af "Viser listen over tilgængelige organisationer"](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="80f76-208">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="80f76-209">Vælg den organisation, hvor du vil installere eksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="80f76-209">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="80f76-210">Vælg **Næste**, indtil du ser dialogen **Opsætning af demodata**.</span><span class="sxs-lookup"><span data-stu-id="80f76-210">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="80f76-211">![Skærmbillede af vinduet med status for installation af demodata](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="80f76-211">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="80f76-212">Før du fortsætter, skal du lægge mærke til, at installation af eksempeldata kan tage op til én time (normalt ~ 10 minutter).</span><span class="sxs-lookup"><span data-stu-id="80f76-212">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="80f76-213">Du skal først sikre, at computeren forbliver tændt og har forbindelse til et netværk under hele installationen, og, at din session forbliver aktiv.</span><span class="sxs-lookup"><span data-stu-id="80f76-213">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="80f76-214">Når du er færdig, skal du klikke på **Næste** for at starte installationsprocessen for eksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="80f76-214">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="80f76-215">Når eksempeldataene er indlæst, skal du klikke på **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="80f76-215">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="80f76-216">Kontrollere installationen af eksempeldataene</span><span class="sxs-lookup"><span data-stu-id="80f76-216">Verify the sample data installation</span></span>

<span data-ttu-id="80f76-217">For en sikkerheds skyld skal du kontrollere, at antallet af poster og typer af objekter, der vises i det fiktive Fabrikam Robotics-scenario, vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="80f76-217">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="80f76-218">Når eksempeldataene er helt indlæst, skal du logge på som brugeren Spencer Low og kontrollere følgende:</span><span class="sxs-lookup"><span data-stu-id="80f76-218">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="80f76-219">Hvis programmet Project Service er installeret, skal du gå til **Project Service** > **Indstillinger** > **Prislister**.</span><span class="sxs-lookup"><span data-stu-id="80f76-219">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="80f76-220">Bekræft, at faktureringssatser og omkostningssatser findes med den rette valuta for hvert land/område i datasættet.</span><span class="sxs-lookup"><span data-stu-id="80f76-220">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="80f76-221">Hvis programmet Project Service er installeret, skal du gå til **Universal Resource Scheduling** > **Indstillinger** > **Afdelinger**.</span><span class="sxs-lookup"><span data-stu-id="80f76-221">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="80f76-222">Bekræft, at en kostprisliste med den rette valuta er knyttet til hver organisationsenhed (undtagen by-poster).</span><span class="sxs-lookup"><span data-stu-id="80f76-222">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="80f76-223">Hvis der mangler nogen, kan du søge efter og tilknytte den korrekte kostprisliste.</span><span class="sxs-lookup"><span data-stu-id="80f76-223">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="80f76-224">Hvis programmet Field Service er installeret, skal du gå til **Project Service** > **Indstillinger** > **Prislister**.</span><span class="sxs-lookup"><span data-stu-id="80f76-224">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="80f76-225">Bekræft, der er angivet fakturasatser og omkostningssatser.</span><span class="sxs-lookup"><span data-stu-id="80f76-225">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="80f76-226">Gå til **Field Service** > **Indstillinger** > **Prislister**, og se, at fakturasatser og omkostningssatser er angivet, med den rette valuta for hvert land/område, i datasættet.</span><span class="sxs-lookup"><span data-stu-id="80f76-226">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="80f76-227">![Skærmbillede af aktive prislister](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="80f76-227">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="80f76-228">![Skærmbillede af aktive organisationsenheder](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="80f76-228">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="80f76-229">Tekniske bemærkninger</span><span class="sxs-lookup"><span data-stu-id="80f76-229">Technical notes</span></span>

<span data-ttu-id="80f76-230">Se flere tekniske oplysninger om installationen af disse data nedenfor.</span><span class="sxs-lookup"><span data-stu-id="80f76-230">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="80f76-231">Installation af eksempeldata oven på eksisterende data (anbefales ikke)</span><span class="sxs-lookup"><span data-stu-id="80f76-231">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="80f76-232">Hvis du har brug for at installere eksempeldata oven på en eksisterende Field Service eller Project Service-prøveversion eller -demomiljø, der allerede har data, skal du deaktivere de forhåndskontroller af sikkerheden, der udføres af installationsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="80f76-232">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="80f76-233">For at gøre det skal du gå til mappen **PkgFolder** for at søge efter og åbne filen **DemoDataPreImportConfig.xml** med Notesblok (eller en anden XML-editor).</span><span class="sxs-lookup"><span data-stu-id="80f76-233">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="80f76-234">Find følgende værdi, og rediger derefter indstillingen fra sand til falsk:</span><span class="sxs-lookup"><span data-stu-id="80f76-234">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="80f76-235">Denne ændring medfører, at installationsprogrammet omgår nogle vigtige sikkerhedskontroller, herunder:</span><span class="sxs-lookup"><span data-stu-id="80f76-235">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="80f76-236">Bekræfter, at der findes mere end én aktiv **Afdeling**-post og omdøber den derefter til **Fabrikam USA**.</span><span class="sxs-lookup"><span data-stu-id="80f76-236">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="80f76-237">Bekræfter, at der ikke findes mere end én aktiv **Arbejdsskabelon**-post.</span><span class="sxs-lookup"><span data-stu-id="80f76-237">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="80f76-238">Bekræfter, at der ikke findes mere end én aktiv **Projektparameter**-post og omdøber derefter posten til **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="80f76-238">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="80f76-239">Konfigurationskomponenter</span><span class="sxs-lookup"><span data-stu-id="80f76-239">Configuration components</span></span>

<span data-ttu-id="80f76-240">Der findes en række andre konfigurationskomponenter i denne konfigurationsfil før import.</span><span class="sxs-lookup"><span data-stu-id="80f76-240">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="80f76-241">Følgende komponenter kan bruges af tekniske brugere:</span><span class="sxs-lookup"><span data-stu-id="80f76-241">For technical users, some of these include:</span></span>

- <span data-ttu-id="80f76-242">**\<RequiredSolutions\>** angiver nødvendige løsningsinstallationer og versionsnumre.</span><span class="sxs-lookup"><span data-stu-id="80f76-242">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="80f76-243">**\<InstallSampleData\>** styrer, om standardeksempeldata til appsene er installeret.</span><span class="sxs-lookup"><span data-stu-id="80f76-243">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="80f76-244">false - undlader at foretage installationen af disse indbyggede data (som kan fjernes)</span><span class="sxs-lookup"><span data-stu-id="80f76-244">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="80f76-245">true - installerer de indbyggede data, der svarer til installationen af FS- og PSA-eksempeldataene</span><span class="sxs-lookup"><span data-stu-id="80f76-245">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="80f76-246">**\<PreImportDataCollection\>** angiver datatilknytninger i fil, der ikke kan redigeres, og de tilknyttede poster, der skal importeres forud for installationen af hovedeksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="80f76-246">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="80f76-247">**\<EntitiesToEnableScheduling\>** angiver, hvilke objekter der skal aktiveres til reservation i Microsoft Dynamics-planlægning (også kaldet Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="80f76-247">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="80f76-248">**\<UsersToCreateAndConfigure\>** angiver reserverbare ressourcer, der bliver oprettet (hvis de ikke allerede findes), før importen af eksempeldata køres.</span><span class="sxs-lookup"><span data-stu-id="80f76-248">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="80f76-249">Vær opmærksom på, at kildesystemets eksempeldata for Reserverbare ressource stemmer overens med målsystemet Reserverbare ressource-poster på FullName og logon for de enkelte ressourcer.</span><span class="sxs-lookup"><span data-stu-id="80f76-249">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="80f76-250">Det er derfor IKKE muligt at ændre navnene i denne forudkonfigurationsfil, medmindre du først importerer eksempeldata til et målsystem og bruger disse navne og derefter omdøber den Reserverbare ressource til det ønskede navn, som er angivet sammen med aktiverede brugerposter, og derefter eksporterer dataene igen, så de kan importeres til det endelige destinationssystem (opdatering af Gamle og Ny poster for **ImportUserMapFile.xml** tilsvarende).</span><span class="sxs-lookup"><span data-stu-id="80f76-250">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="80f76-251">**\<PluginsToDisable\>** angiver meget dedikeret linjeelementtilføjelsesprogrammer, der skal deaktiveres under importen af eksempeldataene og derefter aktiveres igen bagefter.</span><span class="sxs-lookup"><span data-stu-id="80f76-251">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="80f76-252">Fiktivt Fabrikam Robotics-scenario</span><span class="sxs-lookup"><span data-stu-id="80f76-252">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="80f76-253">Field Service- og Project Service-eksempelreferencedatapakker installerer **Fabrikam Manufacturing Master Data (v3.0.0.0)-løsningen**sammen med ca. 4.000 poster og ca. 40 forskellige objekter.</span><span class="sxs-lookup"><span data-stu-id="80f76-253">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="80f76-254">De separat eksempeldatapakker til Field Service eller Project Service indeholder et delsæt af **v902FPSMasterData**-eksempeldataene for det pågældende program.</span><span class="sxs-lookup"><span data-stu-id="80f76-254">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="80f76-255">**Demonstrationsdata** pakken installerer **Fabrikam Manufacturing Demo Data (v3.0.0.7)-løsningen** med ca. 22.000 poster på tværs af 148 enheder.</span><span class="sxs-lookup"><span data-stu-id="80f76-255">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="80f76-256">Det fiktive firma, Fabrikam Robotics, er forhandler af assemblylinjerobotter til elektroniske enheder og er kendt for deres produktkvalitet, fornyelse og solide kundeservice, herunder planlægning af installation, implementering og løbende vedligeholdelsestjenester.</span><span class="sxs-lookup"><span data-stu-id="80f76-256">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="80f76-257">Fabrikam har hovedkontor i USA (Fabrikam US) og har projektbaserede serviceoperationer i Frankrig, Indien, Østrig og Schweiz.</span><span class="sxs-lookup"><span data-stu-id="80f76-257">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="80f76-258">Field Service-handlinger er centreret i USA for det meste i området omkring Seattle.</span><span class="sxs-lookup"><span data-stu-id="80f76-258">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="80f76-259">Virksomheden har fokus på at udnytte Tingenes internet-forbindelser (loT) til at overvåge ydeevnen af kundeaktiver og levere stadigt mere proaktive tjenester hos virksomheden.</span><span class="sxs-lookup"><span data-stu-id="80f76-259">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="80f76-260">En detaljeret oversigt over eksempeldataene er som følger:</span><span class="sxs-lookup"><span data-stu-id="80f76-260">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="80f76-261">Almindelige eksempeldataelementer (inkluderet for begge programmer)</span><span class="sxs-lookup"><span data-stu-id="80f76-261">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="80f76-262">1 bruger</span><span class="sxs-lookup"><span data-stu-id="80f76-262">1 user</span></span>

    - <span data-ttu-id="80f76-263">71 firmaer</span><span class="sxs-lookup"><span data-stu-id="80f76-263">71 accounts</span></span>

    - <span data-ttu-id="80f76-264">137 kontakter</span><span class="sxs-lookup"><span data-stu-id="80f76-264">137 contacts</span></span>

    - <span data-ttu-id="80f76-265">Forskellige transaktionstyper og -kategorier</span><span class="sxs-lookup"><span data-stu-id="80f76-265">Various transaction types and categories</span></span>

    - <span data-ttu-id="80f76-266">50 produkter med 1 produktprisliste</span><span class="sxs-lookup"><span data-stu-id="80f76-266">50 products with 1 product price list</span></span>

    - <span data-ttu-id="80f76-267">14 pris/kostlister</span><span class="sxs-lookup"><span data-stu-id="80f76-267">14 price/cost lists</span></span>

    - <span data-ttu-id="80f76-268">31 egenskaber (ressourcernes kvalifikationer) i 2 klassificeringsmodeller med 3 niveauer (klassificeringsværdier)</span><span class="sxs-lookup"><span data-stu-id="80f76-268">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="80f76-269">Project Service</span><span class="sxs-lookup"><span data-stu-id="80f76-269">Project Service</span></span>

    - <span data-ttu-id="80f76-270">8 afdelinger</span><span class="sxs-lookup"><span data-stu-id="80f76-270">8 organizational units</span></span>

    - <span data-ttu-id="80f76-271">6 rollespecifikke niveauer for tidsforbrug</span><span class="sxs-lookup"><span data-stu-id="80f76-271">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="80f76-272">2,8 k + rolleprisspecifikationer</span><span class="sxs-lookup"><span data-stu-id="80f76-272">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="80f76-273">Field Service</span><span class="sxs-lookup"><span data-stu-id="80f76-273">Field Service</span></span>

    - <span data-ttu-id="80f76-274">4 distrikter</span><span class="sxs-lookup"><span data-stu-id="80f76-274">4 territories</span></span>

    - <span data-ttu-id="80f76-275">5 arbejdsordretyper</span><span class="sxs-lookup"><span data-stu-id="80f76-275">5 work order types</span></span>

    - <span data-ttu-id="80f76-276">22 kundeaktiver</span><span class="sxs-lookup"><span data-stu-id="80f76-276">22 customer assets</span></span>

    - <span data-ttu-id="80f76-277">9 hændelsestyper med et udvalg af tilknyttede ressourceegenskaber (9), services (13) og serviceopgaver (13)</span><span class="sxs-lookup"><span data-stu-id="80f76-277">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="80f76-278">Pakken med **Demonstrationsdata** installerer ca. 179 arbejdsordrer, 12 projekter og tilknyttede transaktionsdata.</span><span class="sxs-lookup"><span data-stu-id="80f76-278">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="80f76-279">Ændre arbejdstimerne for eksempelressourcer</span><span class="sxs-lookup"><span data-stu-id="80f76-279">Change the work hours for sample resources</span></span>

<span data-ttu-id="80f76-280">Som standard har alle reserverbare ressourcer en 24 timers kalender.</span><span class="sxs-lookup"><span data-stu-id="80f76-280">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="80f76-281">Hvis du vil ændre arbejdstimerne for reserverbare eksempelressourcer, skal du gå til **Universal Resource Scheduling** > **Planlægning** > **Ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="80f76-281">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="80f76-282">Vælg en bruger (f.eks. Spencer Low), og skift Spencers arbejdstimer til de timer, du vil anvende til flere brugere.</span><span class="sxs-lookup"><span data-stu-id="80f76-282">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="80f76-283">Gå til **Universal Resource Scheduling** > **Indstillinger** > **Arbejdstidsskabeloner**, og rediger posten **Standardarbejdssskabelon**.</span><span class="sxs-lookup"><span data-stu-id="80f76-283">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="80f76-284">I feltet **Skabelonressource** skal du vælge en bruger med arbejdstimer, som du vil anvende på andre ressourcer.</span><span class="sxs-lookup"><span data-stu-id="80f76-284">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="80f76-285">Gå til **Universal Resource Scheduling** > **Planlægning** > **Ressourcer** > **Aktive reserverbare ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="80f76-285">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="80f76-286">Vælg de ressourcer, du vil ændre, og vælg derefter **Angiv kalender**.</span><span class="sxs-lookup"><span data-stu-id="80f76-286">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="80f76-287">På rullelisten **Arbejdsskabelon** skal du vælge skabelonen **Standardarbejdstime** eller en anden skabelon med den korrekte skabelonressource.</span><span class="sxs-lookup"><span data-stu-id="80f76-287">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="80f76-288">Når du skifter til planlægningsområdet, bør du kunne se ressourcerne, der nu har opdaterede arbejdstimer.</span><span class="sxs-lookup"><span data-stu-id="80f76-288">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="80f76-289">![Skærmbillede af aktive reserverbare ressourcer](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="80f76-289">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
