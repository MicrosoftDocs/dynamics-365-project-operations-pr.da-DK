---
title: Implementer brugerdefinerede felter til Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android
description: Dette emne indeholder almindelige mønstre for anvendelse af udvidelser til at implementere brugerdefinerede felter.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270986"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="fbe8d-103">Implementer brugerdefinerede felter til Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android</span><span class="sxs-lookup"><span data-stu-id="fbe8d-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbe8d-104">Dette emne indeholder almindelige mønstre for anvendelse af udvidelser til at implementere brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="fbe8d-105">Følgende emner er omfattet:</span><span class="sxs-lookup"><span data-stu-id="fbe8d-105">The following topics are covered:</span></span>

- <span data-ttu-id="fbe8d-106">De forskellige datatyper, som den brugerdefinerede feltstruktur understøtter</span><span class="sxs-lookup"><span data-stu-id="fbe8d-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="fbe8d-107">Sådan får du vist skrivebeskyttede eller redigerbare felter i timeseddelposter og gemmer brugerangivne værdier i databasen igen</span><span class="sxs-lookup"><span data-stu-id="fbe8d-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="fbe8d-108">Sådan får du vist skrivebeskyttede felter i overskriften for timesedlen</span><span class="sxs-lookup"><span data-stu-id="fbe8d-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="fbe8d-109">Sådan integreres anden brugerdefinerede forretningslogik for at angive standardværdier i felter og foretage yderligere validering</span><span class="sxs-lookup"><span data-stu-id="fbe8d-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="fbe8d-110">Målgruppe</span><span class="sxs-lookup"><span data-stu-id="fbe8d-110">Audience</span></span>

<span data-ttu-id="fbe8d-111">Dette emne er tiltænkt udviklere, der integrerer deres brugerdefinerede felter i den Microsoft Dynamics 365 Project Timesheet-mobilapp, der er tilgængeligt for Apple iOS og Google Android.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="fbe8d-112">Det antages, at læserne kender funktionerne for X++-udvikling og funktionaliteten for projekttimesedler.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="fbe8d-113">Datakontrakt – TSTimesheetCustomField X++klasse</span><span class="sxs-lookup"><span data-stu-id="fbe8d-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="fbe8d-114">Klassen **TSTimesheetCustomField** er den X++-datakontraktklasse, der repræsenterer oplysninger om et brugerdefineret felt til timeseddelfunktionaliteten.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="fbe8d-115">Lister over brugerdefinerede feltobjekter overføres både til TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten for at få vist brugerdefinerede felter i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="fbe8d-116">**TSTimesheetDetails** – Kontrakten for overskrifter til timesedlen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="fbe8d-117">**TSTimesheetEntry** – Kontrakt for timeseddeltransaktion.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="fbe8d-118">Grupper af disse objekter, der har samme projektoplysninger og den samme værdi i **timesheetLineRecId**, udgør en linje.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="fbe8d-119">fieldBaseType (typer)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="fbe8d-120">Egenskaben **FieldBaseType** i objektet **TsTimesheetCustom** bestemmer, hvilken type felt der vises i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="fbe8d-121">Følgende værdier for **Typer** understøttes.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="fbe8d-122">Typer af værdi</span><span class="sxs-lookup"><span data-stu-id="fbe8d-122">Types value</span></span> | <span data-ttu-id="fbe8d-123">Skriv</span><span class="sxs-lookup"><span data-stu-id="fbe8d-123">Type</span></span>              | <span data-ttu-id="fbe8d-124">Noter</span><span class="sxs-lookup"><span data-stu-id="fbe8d-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="fbe8d-125">0</span><span class="sxs-lookup"><span data-stu-id="fbe8d-125">0</span></span>           | <span data-ttu-id="fbe8d-126">Streng (og enum)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-126">String (and Enum)</span></span> | <span data-ttu-id="fbe8d-127">Feltet vises som et tekstfelt.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="fbe8d-128">0</span><span class="sxs-lookup"><span data-stu-id="fbe8d-128">1</span></span>           | <span data-ttu-id="fbe8d-129">Integer</span><span class="sxs-lookup"><span data-stu-id="fbe8d-129">Integer</span></span>           | <span data-ttu-id="fbe8d-130">Værdien vises som et tal uden decimaler.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="fbe8d-131">2</span><span class="sxs-lookup"><span data-stu-id="fbe8d-131">2</span></span>           | <span data-ttu-id="fbe8d-132">Reelle tal</span><span class="sxs-lookup"><span data-stu-id="fbe8d-132">Real</span></span>              | <span data-ttu-id="fbe8d-133">Værdien vises som et tal med decimaler.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="fbe8d-134">Hvis du vil have vist den reelle værdi som en valuta i appen, skal du bruge egenskaben **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="fbe8d-135">Du kan bruge egenskaben **numberOfDecimals** til at angive det antal decimaler, der skal vises.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="fbe8d-136">3</span><span class="sxs-lookup"><span data-stu-id="fbe8d-136">3</span></span>           | <span data-ttu-id="fbe8d-137">Date</span><span class="sxs-lookup"><span data-stu-id="fbe8d-137">Date</span></span>              | <span data-ttu-id="fbe8d-138">Datoformater bestemmes af brugerens indstilling for **Dato, klokkeslæt og talformat**, der er angivet under **Præference for sprog og land/område** under **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="fbe8d-139">4</span><span class="sxs-lookup"><span data-stu-id="fbe8d-139">4</span></span>           | <span data-ttu-id="fbe8d-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="fbe8d-140">Boolean</span></span>           | |
| <span data-ttu-id="fbe8d-141">15</span><span class="sxs-lookup"><span data-stu-id="fbe8d-141">15</span></span>          | <span data-ttu-id="fbe8d-142">GUID</span><span class="sxs-lookup"><span data-stu-id="fbe8d-142">GUID</span></span>              | |
| <span data-ttu-id="fbe8d-143">16</span><span class="sxs-lookup"><span data-stu-id="fbe8d-143">16</span></span>          | <span data-ttu-id="fbe8d-144">Int64</span><span class="sxs-lookup"><span data-stu-id="fbe8d-144">Int64</span></span>             | |

- <span data-ttu-id="fbe8d-145">Hvis egenskaben **stringOptions** ikke findes i objektet **TSTimesheetCustomField**, stilles et fritekstfelt til rådighed for brugeren.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="fbe8d-146">Egenskaben **stringLength** kan bruges til at angive den maksimale strenglængde, som brugere kan angive.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="fbe8d-147">Hvis egenskaben **stringOptions** er angivet på objektet **TSTimesheetCustomField**, er listeelementerne de eneste værdier, som brugere kan vælge ved hjælp af alternativknapper (alternativknapper).</span><span class="sxs-lookup"><span data-stu-id="fbe8d-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="fbe8d-148">I dette tilfælde kan strengfeltet fungere som en enum-værdi med henblik på brugerangivelse.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="fbe8d-149">Hvis du vil gemme værdien i databasen som en enum, skal strengværdien knyttes til enum-værdien manuelt, før du gemmer den i databasen, ved hjælp af kommandokæden (se f.eks. afsnittet "Brug af en kommandokæde i TSTimesheetEntryService-klassen for at gemme en timeseddelpost fra appen til databasen igen" senere i dette emne).</span><span class="sxs-lookup"><span data-stu-id="fbe8d-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="fbe8d-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="fbe8d-151">Du kan bruge denne egenskab til at formatere reelle værdier som valuta.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="fbe8d-152">Denne fremgangsmåde kan kun anvendes, hvis værdien for **fieldBaseType** er **Reel**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="fbe8d-153">**TSCustomFieldExtendedType:None** – Der anvendes ingen formatering.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="fbe8d-154">**TSCustomFieldExtendedType::Valuta** – Formatér værdien som valuta.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="fbe8d-155">Når valutaformatering er aktiv, kan feltet **stringValue** bruges til at overføre den valutakode, der skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="fbe8d-156">Værdien er en skrivebeskyttet værdi.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-156">The value is a read-only value.</span></span>

    <span data-ttu-id="fbe8d-157">Feltet **realValue** indeholder det pengebeløb, der skal gemmes i databasen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="fbe8d-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="fbe8d-159">Du kan bruge denne egenskab til at angive, hvor det brugerdefinerede felt skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="fbe8d-160">**TSCustomFieldSection::Overskrift** – Feltet vises i sektionen **Vis flere detaljer** i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="fbe8d-161">Disse felter er altid skrivebeskyttede.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-161">These fields are always read-only.</span></span>
- <span data-ttu-id="fbe8d-162">**TSCustomFieldSection::Linje** – Feltet vises, når alle de linjefelter, der er standard, er baseret på timeseddelposter.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="fbe8d-163">Disse felter kan enten være redigerbare eller skrivebeskyttede.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="fbe8d-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="fbe8d-165">Denne egenskab identificerer feltet, når de værdier, som appen leverer, gemmes i databasen igen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="fbe8d-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="fbe8d-167">Denne egenskab identificerer feltet, når de værdier, som appen leverer, gemmes i databasen igen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="fbe8d-168">erRedigerbar (NejJa)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-168">isEditable (NoYes)</span></span>

<span data-ttu-id="fbe8d-169">Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelpostering skal kunne redigeres af brugerne.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="fbe8d-170">Angiv egenskaben til **Nej** for at gøre feltet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="fbe8d-171">erObligatorisk (NejJa)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="fbe8d-172">Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelpostering skal være obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="fbe8d-173">navn (str)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-173">label (str)</span></span>

<span data-ttu-id="fbe8d-174">Denne egenskab specificerer det navn, der vises ud for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="fbe8d-175">stringOptions (liste over strenge)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="fbe8d-176">Denne egenskab kan kun anvendes, når **fieldBaseType** er angivet til **Streng**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="fbe8d-177">Hvis **stringOptions** er angivet, er de strengværdier, der kan markeres via alternativknapperne (alternativknapper), angivet med strengene på listen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="fbe8d-178">Hvis der ikke angives en streng, tillades fritekst i strengfeltet (se f.eks.sektionen "Brug en kommandokæde i TSTimesheetEntryService-klassen for at gemme en timeseddelpostering fra appen i databasen igen" senere i dette emne).</span><span class="sxs-lookup"><span data-stu-id="fbe8d-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="fbe8d-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-179">stringLength (int)</span></span>

<span data-ttu-id="fbe8d-180">Denne egenskab specificerer maksimumlængden for et strengfelt.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="fbe8d-181">Den kan kun anvendes, når **fieldBaseType** er angivet til **Streng**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="fbe8d-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="fbe8d-183">Denne egenskab angiver det antal decimaler, der vises for et reelt felt.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="fbe8d-184">Den kan kun anvendes, når **fieldBaseType** er angivet til **Reel**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="fbe8d-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-185">orderSequence (int)</span></span>

<span data-ttu-id="fbe8d-186">Denne egenskab styrer den rækkefølge, som de brugerdefinerede felter vises i i appen, når der er angivet mere end ét brugerdefineret felt.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="fbe8d-187">Der vises først felter med lavere tal.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="fbe8d-188">booleanValue (boolesk)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-188">booleanValue (boolean)</span></span>

<span data-ttu-id="fbe8d-189">For felter af typen **Boolesk** overfører denne egenskab den booleske værdi for feltet mellem serveren og app'en.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="fbe8d-190">guidValue (GUID)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-190">guidValue (guid)</span></span>

<span data-ttu-id="fbe8d-191">For felter af typen **GUID** overfører denne egenskab feltets globale entydige id-værdi mellem serveren og app'en.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="fbe8d-192">int64Value (Int64)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-192">int64Value (int64)</span></span>

<span data-ttu-id="fbe8d-193">For felter af typen **Int64** overfører denne egenskab int64-værdien for feltet mellem serveren og app'en.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="fbe8d-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-194">intValue (int)</span></span>

<span data-ttu-id="fbe8d-195">For felter af typen **Int** overfører denne egenskab int-værdien for feltet mellem serveren og app'en.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="fbe8d-196">realValue (reel)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-196">realValue (real)</span></span>

<span data-ttu-id="fbe8d-197">For felter af typen **Reel** overfører denne egenskab den reelle værdi for feltet mellem serveren og app'en.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="fbe8d-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-198">stringValue (str)</span></span>

<span data-ttu-id="fbe8d-199">For felter af typen **Streng** overfører denne egenskab strengværdien for feltet mellem serveren og app'en.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="fbe8d-200">Den bruges også til felter af typen **Reel**, der formateres som valuta.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="fbe8d-201">I forbindelse med disse felter bruges egenskaben til at sende valutakoden til appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="fbe8d-202">dateValue (dato)</span><span class="sxs-lookup"><span data-stu-id="fbe8d-202">dateValue (date)</span></span>

<span data-ttu-id="fbe8d-203">For felter af typen **Dato** overfører denne egenskab datoværdien for feltet mellem serveren og app'en.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="fbe8d-204">Få vist og gem et brugerdefineret felt i sektionen for timeseddelpostering</span><span class="sxs-lookup"><span data-stu-id="fbe8d-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="fbe8d-205">Nedenfor vises et skærmbillede fra mobilappen til oprettelse af en timeseddelpostering.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="fbe8d-206">Den viser standardfelterne og et brugerdefineret felt i sektionen "Tidsregistrering", der kaldes "Teststreng", hvor en enum-værdi på "Anden mulighed" allerede er angivet.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Brugerdefineret felt til teststreng i appen](media/timesheet-entry.jpg)



<span data-ttu-id="fbe8d-208">Nedenfor vises et skærmbillede fra mobilapp'en, hvor brugeren vælger en af de enum-indstillinger, der er tilgængelige for det brugerdefinerede felt "Teststreng".</span><span class="sxs-lookup"><span data-stu-id="fbe8d-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="fbe8d-209">De to indstillinger er "Første mulighed" og "Anden mulighed", som vises som alternativknapper.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="fbe8d-210">Den anden mulighed er valgt i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-210">The second option is currently selected.</span></span>

![Alternativknapper (alternativknapper) for det brugerdefinerede felt Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="fbe8d-212">Udvide tabellen TSTimesheetLine, så den indeholder et brugerdefineret felt</span><span class="sxs-lookup"><span data-stu-id="fbe8d-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="fbe8d-213">I typiske scenarier er det sandsynligt, at dataene for et brugerdefineret felt i sektionen til timeseddelposteringer gemmes i tabellen TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="fbe8d-214">Men andre tabeller kan bruges, hvis dataene kan hentes på baggrund af en TSTimesheetTrans-post, der er angivet, eller hvis den ikke har en bestemt postkontekst (f.eks. hvis feltet er angivet som skrivebeskyttet i projektparametrene).</span><span class="sxs-lookup"><span data-stu-id="fbe8d-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="fbe8d-215">Bemærk, at brugerdefinerede felter ikke behøver at have nogen sikkerhedskopi af databaseposter.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="fbe8d-216">De kan oprettes dynamisk på baggrund af X++-logikken.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="fbe8d-217">Denne fremgangsmåde kan være nyttig i skrivebeskyttede scenarier (Se f.eks. sektionen "Brug af en kommandokæde i TSTimesheetDetails-klassen, buildCustomFieldListForHeader-metode til at udfylde oplysningerne i timesedlen" for at få vist et eksempel på dynamisk genererede brugerdefinerede feltværdier).</span><span class="sxs-lookup"><span data-stu-id="fbe8d-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="fbe8d-218">Nedenfor vises et skærmbillede fra Visual Studio af applikationsobjekttræet.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="fbe8d-219">Den viser en udvidelse af TSTimesheetLine-tabellen med TestLineString-feltet tilføjet som et brugerdefineret felt.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="fbe8d-221">Brug en kommandokæde til metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i sektionen timeseddelpostering</span><span class="sxs-lookup"><span data-stu-id="fbe8d-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="fbe8d-222">Denne kode styrer visningsindstillingerne for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="fbe8d-223">Den styrer f.eks. felttypen, navnet, om feltet er obligatorisk, og hvilken sektion feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="fbe8d-224">Følgende eksempel viser et strengfelt for tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="fbe8d-225">Dette felt indeholder to indstillinger, **Første mulighed** og **Anden mulighed**, der er tilgængelige via alternativknapper (alternativknapper).</span><span class="sxs-lookup"><span data-stu-id="fbe8d-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="fbe8d-226">Feltet i appen er knyttet til feltet **TestLineString**, som føjes til tabellen TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="fbe8d-227">Bemærk, at brugen af metoden **TSTimesheetCustomField::newFromMetatdata()** gør det nemmere at initialisere egenskaberne for det brugerdefinerede felt: **fieldBaseType**, **tableName**, **feltnavn**, **navn**, **erRedigerbar**, **erObligatorisk**, **strengLængde** og **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="fbe8d-228">Du kan også angive disse parametre manuelt, som du foretrækker.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="fbe8d-229">Brug en kommandokæde til metoden buildCustomFieldListForEntry i klassen TSTimesheetEntry til at angive værdierne i en timeseddelpostering</span><span class="sxs-lookup"><span data-stu-id="fbe8d-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="fbe8d-230">Metoden **buildCustomFieldListForEntry** bruges til at angive værdier for de gemte timeseddellinjer i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="fbe8d-231">Det tager en TSTimesheetTrans-post som parameter.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="fbe8d-232">Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="fbe8d-233">Brug en kommandokæde i klassen TSTimesheetEntryService til at gemme en timeseddelpostering fra appen i databasen igen</span><span class="sxs-lookup"><span data-stu-id="fbe8d-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="fbe8d-234">Hvis du vil gemme et brugerdefineret felt i databasen igen, der anvendes normalt, skal du udvide flere metoder:</span><span class="sxs-lookup"><span data-stu-id="fbe8d-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="fbe8d-235">Metoden **timesheetLineNeedsUpdating** bruges til at afgøre, om linjeposten er blevet ændret af brugeren i appen og skal gemmes i databasen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="fbe8d-236">Hvis ydeevnen ikke er et problem, kan denne metode forenkles, så den altid returnerer **sand**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="fbe8d-237">Metoderne **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan udvides, så de angiver værdier i TSTimesheetLine-databaseposten fra den TSTimesheetEntry-datakontraktpost, der leveres.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="fbe8d-238">I eksemplet nedenfor kan du se, hvordan tilknytningen mellem databasefeltet og posteringsfeltet manuelt udføres via X++-kode.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="fbe8d-239">Metoden **populateTimesheetWeekFromEntry** kan også udvides, hvis det brugerdefinerede felt, der er knyttet til objektet **TSTimesheetEntry**, skal skrive tilbage til TSTimesheetLineweek-databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="fbe8d-240">I følgende eksempel gemmes værdien for **firstOption** eller **secondOption**, som brugeren vælger, til databasen som en rå strengværdi.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="fbe8d-241">Hvis databasefeltet er et felt af typen **Enum**, kan disse værdier knyttes manuelt til en enum-værdi og derefter gemmes i et enum-felt i databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="fbe8d-242">Få vist et brugerdefineret felt i sektionen for timeseddeloverskrift</span><span class="sxs-lookup"><span data-stu-id="fbe8d-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="fbe8d-243">Nedenfor vises et skærmbillede fra mobilappen af en bruger, som får vist en timeseddel.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="fbe8d-244">Knappen "Flere oplysninger" er valgt i øverste højre hjørne for at få vist indstillingen "Vis flere detaljer".</span><span class="sxs-lookup"><span data-stu-id="fbe8d-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Kommandoen "Se flere detaljer"](media/show-more.png)

<span data-ttu-id="fbe8d-246">Nedenfor vises et skærmbillede fra mobilappen, som viser sektionen "Mere" i en timeseddel.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="fbe8d-247">Der er tilføjet et brugerdefineret felt med navnet "Tidsforbruget for denne timeseddel (beregnet brugerdefineret felt)" til sektionen med timeseddeloverskriften.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="fbe8d-248">En skrivebeskyttet værdi på "0,667" angives i det brugerdefinerede felt.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sektionen "Mere"](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="fbe8d-250">Udvide tabellen TSTimesheetTable, så den indeholder et brugerdefineret felt</span><span class="sxs-lookup"><span data-stu-id="fbe8d-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="fbe8d-251">I typiske scenarier er det sandsynligt, at dataene for et brugerdefineret felt i overskriftsektionen hentes fra tabellen TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="fbe8d-252">Men andre tabeller kan bruges, hvis dataene kan hentes på baggrund af en TSTimesheetTable-post, der er angivet, eller hvis den ikke har en bestemt postkontekst (f.eks. hvis feltet er angivet som skrivebeskyttet i projektparametrene).</span><span class="sxs-lookup"><span data-stu-id="fbe8d-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="fbe8d-253">Bemærk, at brugerdefinerede felter ikke behøver at have nogen sikkerhedskopi af databaseposter.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="fbe8d-254">De kan oprettes dynamisk på baggrund af X++-logikken.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="fbe8d-255">I eksemplet nedenfor vises denne fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="fbe8d-256">Felter i overskriftsektionen er altid skrivebeskyttet i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="fbe8d-257">Brug en kommandokæde til metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i overskriftsektionen</span><span class="sxs-lookup"><span data-stu-id="fbe8d-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="fbe8d-258">Denne kode styrer visningsindstillingerne for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="fbe8d-259">Den styrer f.eks. felttypen, navnet, om feltet er obligatorisk, og hvilken sektion feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="fbe8d-260">I følgende eksempel vises en beregnet værdi i overskriftsektionen i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="fbe8d-261">Brug en kommandokæde til metoden buildCustomFieldListForHeader i klassen TSTimesheetDetails til at udfylde detaljerne i en timeseddel</span><span class="sxs-lookup"><span data-stu-id="fbe8d-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="fbe8d-262">Metoden **buildCustomFieldListForHeader** bruges til at udfylde detaljerne i timeseddeloverskriften i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="fbe8d-263">Det anvender en TSTimesheetTable-post som parameter.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="fbe8d-264">Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="fbe8d-265">Følgende eksempel læser ikke værdier fra databasen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="fbe8d-266">I stedet bruger den X++-logik til at oprette en beregnet værdi, der derefter vises i appen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="fbe8d-267">Andre konfigurationsmuligheder/udvidelsesmuligheder</span><span class="sxs-lookup"><span data-stu-id="fbe8d-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="fbe8d-268">Tilføjelse af yderligere validering for appen</span><span class="sxs-lookup"><span data-stu-id="fbe8d-268">Adding additional validation for the app</span></span>

<span data-ttu-id="fbe8d-269">Eksisterende logik for timeseddelfunktionalitet på databaseniveau fungerer stadig som forventet.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="fbe8d-270">Hvis du vil afbryde fuldførelsen af handlinger til lagring eller afsendelse og se en bestemt fejlmeddelelse, kan du tilføje **vis fejl ("meddelelse til bruger")** til koden via en udvidelse af kommandokæden.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="fbe8d-271">Her er tre eksempler på nyttige, udvidede metoder:</span><span class="sxs-lookup"><span data-stu-id="fbe8d-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="fbe8d-272">Hvis **validateWrite** i tabellen TSTimesheetLine returnerer **falsk** under en lagringshandling for en timeseddellinje, vises der en fejlmeddelelse i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="fbe8d-273">Hvis **validateSubmit** i tabellen TSTimesheetTable returnerer **falsk** under en indsendelse af en timeseddel i appen, vises brugeren en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="fbe8d-274">Logik, der udfylder felter (f.eks. **Linjeegenskab**) under metoden **indsæt** i TSTimesheetLine-tabellen, kører stadig.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="fbe8d-275">Skjul og marker standardfelterne som skrivebeskyttede via konfiguration</span><span class="sxs-lookup"><span data-stu-id="fbe8d-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="fbe8d-276">Fra projektparametrene kan du gøre standardfelter skrivebeskyttede eller skjulte i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="fbe8d-277">Angiv indstillingerne i sektionen **Mobile timesedler** under fanen **Timeseddel** på siden **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektparametre](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="fbe8d-279">Ændring af de aktiviteter, der er tilgængelige for markering via udvidelser</span><span class="sxs-lookup"><span data-stu-id="fbe8d-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="fbe8d-280">De aktiviteter, der kan vælges til et projekt, udfyldes via metoderne **getActivitiesForProject()** og **getActivityQuery()** i klassen **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="fbe8d-281">Du kan bruge kommandokæden til at ændre denne funktionsmåde, så den stemmer overens med virksomhedens scenario for de aktiviteter, der kan vælges til et bestemt projekt.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="fbe8d-282">Angiv en standardprojektkategori på timeseddelposter</span><span class="sxs-lookup"><span data-stu-id="fbe8d-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="fbe8d-283">Indtastning af en standardprojektkategori på timeseddelposteringer sker på tre niveauer.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="fbe8d-284">Du kan bruge kommandokæden til at udvide funktionsmåden på et eller flere af disse niveauer for at opnå den ønskede funktionsmåde.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="fbe8d-285">Følgende hierarki anvendes:</span><span class="sxs-lookup"><span data-stu-id="fbe8d-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="fbe8d-286">Appen forsøger at anbringe standardkategorien fra projektressourcen.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="fbe8d-287">Denne standardkategori er angivet i metoderne **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="fbe8d-288">Hvis standardkategorien ikke er angivet på projektressourceniveau, forsøger appen at hente den fra projektaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="fbe8d-289">Denne standardkategori er angivet i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="fbe8d-290">Hvis standardkategorien ikke er angivet på projektressourceniveau, hentes standardkategorien fra projektparametrene.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="fbe8d-291">Denne standardkategori er angivet i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="fbe8d-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]