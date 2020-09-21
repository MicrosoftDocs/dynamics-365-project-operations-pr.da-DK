---
title: Implementer brugerdefinerede felter til Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android
description: Dette emne indeholder almindelige mønstre for anvendelse af udvidelser til at implementere brugerdefinerede felter.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750505"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementer brugerdefinerede felter til Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android

[!include [banner](../includes/banner.md)]

Dette emne indeholder almindelige mønstre for anvendelse af udvidelser til at implementere brugerdefinerede felter. Følgende emner er omfattet:

- De forskellige datatyper, som den brugerdefinerede feltstruktur understøtter
- Sådan får du vist skrivebeskyttede eller redigerbare felter i timeseddelposter og gemmer brugerangivne værdier i databasen igen
- Sådan får du vist skrivebeskyttede felter i overskriften for timesedlen
- Sådan integreres anden brugerdefinerede forretningslogik for at angive standardværdier i felter og foretage yderligere validering

## <a name="audience"></a>Målgruppe

Dette emne er tiltænkt udviklere, der integrerer deres brugerdefinerede felter i den Microsoft Dynamics 365 Project Timesheet-mobilapp, der er tilgængeligt for Apple iOS og Google Android. Det antages, at læserne kender funktionerne for X++-udvikling og funktionaliteten for projekttimesedler.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datakontrakt – TSTimesheetCustomField X++klasse

Klassen **TSTimesheetCustomField** er den X++-datakontraktklasse, der repræsenterer oplysninger om et brugerdefineret felt til timeseddelfunktionaliteten. Lister over brugerdefinerede feltobjekter overføres både til TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten for at få vist brugerdefinerede felter i mobilappen.

- **TSTimesheetDetails** – Kontrakten for overskrifter til timesedlen.
- **TSTimesheetEntry** – Kontrakt for timeseddeltransaktion. Grupper af disse objekter, der har samme projektoplysninger og den samme værdi i **timesheetLineRecId**, udgør en linje.

### <a name="fieldbasetype-types"></a>fieldBaseType (typer)

Egenskaben **FieldBaseType** i objektet **TsTimesheetCustom** bestemmer, hvilken type felt der vises i appen. Følgende værdier for **Typer** understøttes.

| Typer af værdi | Skriv              | Noter |
|-------------|-------------------|-------|
| 0           | Streng (og enum) | Feltet vises som et tekstfelt. |
| 0           | Integer           | Værdien vises som et tal uden decimaler. |
| 2           | Reelle tal              | Værdien vises som et tal med decimaler.<p>Hvis du vil have vist den reelle værdi som en valuta i appen, skal du bruge egenskaben **fieldExtenededType**. Du kan bruge egenskaben **numberOfDecimals** til at angive det antal decimaler, der skal vises.</p> |
| 3           | Date              | Datoformater bestemmes af brugerens indstilling for **Dato, klokkeslæt og talformat**, der er angivet under **Præference for sprog og land/område** under **Brugerindstillinger**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Hvis egenskaben **stringOptions** ikke findes i objektet **TSTimesheetCustomField**, stilles et fritekstfelt til rådighed for brugeren.

    Egenskaben **stringLength** kan bruges til at angive den maksimale strenglængde, som brugere kan angive.

- Hvis egenskaben **stringOptions** er angivet på objektet **TSTimesheetCustomField**, er listeelementerne de eneste værdier, som brugere kan vælge ved hjælp af alternativknapper (alternativknapper).

    I dette tilfælde kan strengfeltet fungere som en enum-værdi med henblik på brugerangivelse. Hvis du vil gemme værdien i databasen som en enum, skal strengværdien knyttes til enum-værdien manuelt, før du gemmer den i databasen, ved hjælp af kommandokæden (se f.eks. afsnittet "Brug af en kommandokæde i TSTimesheetEntryService-klassen for at gemme en timeseddelpost fra appen til databasen igen" senere i dette emne).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Du kan bruge denne egenskab til at formatere reelle værdier som valuta. Denne fremgangsmåde kan kun anvendes, hvis værdien for **fieldBaseType** er **Reel**.

- **TSCustomFieldExtendedType:None** – Der anvendes ingen formatering.
- **TSCustomFieldExtendedType::Valuta** – Formatér værdien som valuta.

    Når valutaformatering er aktiv, kan feltet **stringValue** bruges til at overføre den valutakode, der skal vises i appen. Værdien er en skrivebeskyttet værdi.

    Feltet **realValue** indeholder det pengebeløb, der skal gemmes i databasen.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Du kan bruge denne egenskab til at angive, hvor det brugerdefinerede felt skal vises i appen.

- **TSCustomFieldSection::Overskrift** – Feltet vises i sektionen **Vis flere detaljer** i appen. Disse felter er altid skrivebeskyttede.
- **TSCustomFieldSection::Linje** – Feltet vises, når alle de linjefelter, der er standard, er baseret på timeseddelposter. Disse felter kan enten være redigerbare eller skrivebeskyttede.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Denne egenskab identificerer feltet, når de værdier, som appen leverer, gemmes i databasen igen.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Denne egenskab identificerer feltet, når de værdier, som appen leverer, gemmes i databasen igen.

### <a name="iseditable-noyes"></a>erRedigerbar (NejJa)

Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelpostering skal kunne redigeres af brugerne. Angiv egenskaben til **Nej** for at gøre feltet skrivebeskyttet.

### <a name="ismandatory-noyes"></a>erObligatorisk (NejJa)

Indstil denne egenskab til **Ja** for at angive, at feltet i sektionen til timeseddelpostering skal være obligatorisk.

### <a name="label-str"></a>navn (str)

Denne egenskab specificerer det navn, der vises ud for feltet i appen.

### <a name="stringoptions-list-of-strings"></a>stringOptions (liste over strenge)

Denne egenskab kan kun anvendes, når **fieldBaseType** er angivet til **Streng**. Hvis **stringOptions** er angivet, er de strengværdier, der kan markeres via alternativknapperne (alternativknapper), angivet med strengene på listen. Hvis der ikke angives en streng, tillades fritekst i strengfeltet (se f.eks.sektionen "Brug en kommandokæde i TSTimesheetEntryService-klassen for at gemme en timeseddelpostering fra appen i databasen igen" senere i dette emne).

### <a name="stringlength-int"></a>stringLength (int)

Denne egenskab specificerer maksimumlængden for et strengfelt. Den kan kun anvendes, når **fieldBaseType** er angivet til **Streng**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Denne egenskab angiver det antal decimaler, der vises for et reelt felt. Den kan kun anvendes, når **fieldBaseType** er angivet til **Reel**.

### <a name="ordersequence-int"></a>orderSequence (int)

Denne egenskab styrer den rækkefølge, som de brugerdefinerede felter vises i i appen, når der er angivet mere end ét brugerdefineret felt. Der vises først felter med lavere tal.

### <a name="booleanvalue-boolean"></a>booleanValue (boolesk)

For felter af typen **Boolesk** overfører denne egenskab den booleske værdi for feltet mellem serveren og app'en.

### <a name="guidvalue-guid"></a>guidValue (GUID)

For felter af typen **GUID** overfører denne egenskab feltets globale entydige id-værdi mellem serveren og app'en.

### <a name="int64value-int64"></a>int64Value (Int64)

For felter af typen **Int64** overfører denne egenskab int64-værdien for feltet mellem serveren og app'en.

### <a name="intvalue-int"></a>intValue (int)

For felter af typen **Int** overfører denne egenskab int-værdien for feltet mellem serveren og app'en.

### <a name="realvalue-real"></a>realValue (reel)

For felter af typen **Reel** overfører denne egenskab den reelle værdi for feltet mellem serveren og app'en.

### <a name="stringvalue-str"></a>stringValue (str)

For felter af typen **Streng** overfører denne egenskab strengværdien for feltet mellem serveren og app'en. Den bruges også til felter af typen **Reel**, der formateres som valuta. I forbindelse med disse felter bruges egenskaben til at sende valutakoden til appen.

### <a name="datevalue-date"></a>dateValue (dato)

For felter af typen **Dato** overfører denne egenskab datoværdien for feltet mellem serveren og app'en.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Få vist og gem et brugerdefineret felt i sektionen for timeseddelpostering

Nedenfor vises et skærmbillede fra mobilappen til oprettelse af en timeseddelpostering. Den viser standardfelterne og et brugerdefineret felt i sektionen "Tidsregistrering", der kaldes "Teststreng", hvor en enum-værdi på "Anden mulighed" allerede er angivet.

![Brugerdefineret felt til teststreng i appen](media/timesheet-entry.jpg)



Nedenfor vises et skærmbillede fra mobilapp'en, hvor brugeren vælger en af de enum-indstillinger, der er tilgængelige for det brugerdefinerede felt "Teststreng".  De to indstillinger er "Første mulighed" og "Anden mulighed", som vises som alternativknapper. Den anden mulighed er valgt i øjeblikket.

![Alternativknapper (alternativknapper) for det brugerdefinerede felt Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Udvide tabellen TSTimesheetLine, så den indeholder et brugerdefineret felt

I typiske scenarier er det sandsynligt, at dataene for et brugerdefineret felt i sektionen til timeseddelposteringer gemmes i tabellen TSTimesheetLine. Men andre tabeller kan bruges, hvis dataene kan hentes på baggrund af en TSTimesheetTrans-post, der er angivet, eller hvis den ikke har en bestemt postkontekst (f.eks. hvis feltet er angivet som skrivebeskyttet i projektparametrene).

Bemærk, at brugerdefinerede felter ikke behøver at have nogen sikkerhedskopi af databaseposter. De kan oprettes dynamisk på baggrund af X++-logikken. Denne fremgangsmåde kan være nyttig i skrivebeskyttede scenarier (Se f.eks. sektionen "Brug af en kommandokæde i TSTimesheetDetails-klassen, buildCustomFieldListForHeader-metode til at udfylde oplysningerne i timesedlen" for at få vist et eksempel på dynamisk genererede brugerdefinerede feltværdier).

Nedenfor vises et skærmbillede fra Visual Studio af applikationsobjekttræet. Den viser en udvidelse af TSTimesheetLine-tabellen med TestLineString-feltet tilføjet som et brugerdefineret felt.

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Brug en kommandokæde til metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i sektionen timeseddelpostering

Denne kode styrer visningsindstillingerne for feltet i appen. Den styrer f.eks. felttypen, navnet, om feltet er obligatorisk, og hvilken sektion feltet vises i.

Følgende eksempel viser et strengfelt for tidsregistreringer. Dette felt indeholder to indstillinger, **Første mulighed** og **Anden mulighed**, der er tilgængelige via alternativknapper (alternativknapper). Feltet i appen er knyttet til feltet **TestLineString**, som føjes til tabellen TSTimesheetLine.

Bemærk, at brugen af metoden **TSTimesheetCustomField::newFromMetatdata()** gør det nemmere at initialisere egenskaberne for det brugerdefinerede felt: **fieldBaseType**, **tableName**, **feltnavn**, **navn**, **erRedigerbar**, **erObligatorisk**, **strengLængde** og **numberOfDecimals**. Du kan også angive disse parametre manuelt, som du foretrækker.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Brug en kommandokæde til metoden buildCustomFieldListForEntry i klassen TSTimesheetEntry til at angive værdierne i en timeseddelpostering

Metoden **buildCustomFieldListForEntry** bruges til at angive værdier for de gemte timeseddellinjer i mobilappen. Det tager en TSTimesheetTrans-post som parameter. Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen.

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Brug en kommandokæde i klassen TSTimesheetEntryService til at gemme en timeseddelpostering fra appen i databasen igen

Hvis du vil gemme et brugerdefineret felt i databasen igen, der anvendes normalt, skal du udvide flere metoder:

- Metoden **timesheetLineNeedsUpdating** bruges til at afgøre, om linjeposten er blevet ændret af brugeren i appen og skal gemmes i databasen. Hvis ydeevnen ikke er et problem, kan denne metode forenkles, så den altid returnerer **sand**.
- Metoderne **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan udvides, så de angiver værdier i TSTimesheetLine-databaseposten fra den TSTimesheetEntry-datakontraktpost, der leveres. I eksemplet nedenfor kan du se, hvordan tilknytningen mellem databasefeltet og posteringsfeltet manuelt udføres via X++-kode.
- Metoden **populateTimesheetWeekFromEntry** kan også udvides, hvis det brugerdefinerede felt, der er knyttet til objektet **TSTimesheetEntry**, skal skrive tilbage til TSTimesheetLineweek-databasetabellen.

> [!NOTE]
> I følgende eksempel gemmes værdien for **firstOption** eller **secondOption**, som brugeren vælger, til databasen som en rå strengværdi. Hvis databasefeltet er et felt af typen **Enum**, kan disse værdier knyttes manuelt til en enum-værdi og derefter gemmes i et enum-felt i databasetabellen.

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Få vist et brugerdefineret felt i sektionen for timeseddeloverskrift

Nedenfor vises et skærmbillede fra mobilappen af en bruger, som får vist en timeseddel. Knappen "Flere oplysninger" er valgt i øverste højre hjørne for at få vist indstillingen "Vis flere detaljer".  

![Kommandoen "Se flere detaljer"](media/show-more.png)

Nedenfor vises et skærmbillede fra mobilappen, som viser sektionen "Mere" i en timeseddel. Der er tilføjet et brugerdefineret felt med navnet "Tidsforbruget for denne timeseddel (beregnet brugerdefineret felt)" til sektionen med timeseddeloverskriften. En skrivebeskyttet værdi på "0,667" angives i det brugerdefinerede felt.

![Sektionen "Mere"](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Udvide tabellen TSTimesheetTable, så den indeholder et brugerdefineret felt

I typiske scenarier er det sandsynligt, at dataene for et brugerdefineret felt i overskriftsektionen hentes fra tabellen TSTimesheetHeader. Men andre tabeller kan bruges, hvis dataene kan hentes på baggrund af en TSTimesheetTable-post, der er angivet, eller hvis den ikke har en bestemt postkontekst (f.eks. hvis feltet er angivet som skrivebeskyttet i projektparametrene).

Bemærk, at brugerdefinerede felter ikke behøver at have nogen sikkerhedskopi af databaseposter. De kan oprettes dynamisk på baggrund af X++-logikken. I eksemplet nedenfor vises denne fremgangsmåde.

Felter i overskriftsektionen er altid skrivebeskyttet i appen.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Brug en kommandokæde til metoden buildCustomFieldList i klassen TSTimesheetSettings til at få vist et felt i overskriftsektionen

Denne kode styrer visningsindstillingerne for feltet i appen. Den styrer f.eks. felttypen, navnet, om feltet er obligatorisk, og hvilken sektion feltet vises i.

I følgende eksempel vises en beregnet værdi i overskriftsektionen i appen.

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Brug en kommandokæde til metoden buildCustomFieldListForHeader i klassen TSTimesheetDetails til at udfylde detaljerne i en timeseddel

Metoden **buildCustomFieldListForHeader** bruges til at udfylde detaljerne i timeseddeloverskriften i mobilappen. Det anvender en TSTimesheetTable-post som parameter. Felter fra den pågældende post kan bruges til at udfylde den brugerdefinerede feltværdi i appen. Følgende eksempel læser ikke værdier fra databasen. I stedet bruger den X++-logik til at oprette en beregnet værdi, der derefter vises i appen.


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

## <a name="other-configurabilityextensibility-opportunities"></a>Andre konfigurationsmuligheder/udvidelsesmuligheder

### <a name="adding-additional-validation-for-the-app"></a>Tilføjelse af yderligere validering for appen

Eksisterende logik for timeseddelfunktionalitet på databaseniveau fungerer stadig som forventet. Hvis du vil afbryde fuldførelsen af handlinger til lagring eller afsendelse og se en bestemt fejlmeddelelse, kan du tilføje **vis fejl ("meddelelse til bruger")** til koden via en udvidelse af kommandokæden. Her er tre eksempler på nyttige, udvidede metoder:

- Hvis **validateWrite** i tabellen TSTimesheetLine returnerer **falsk** under en lagringshandling for en timeseddellinje, vises der en fejlmeddelelse i mobilappen.
- Hvis **validateSubmit** i tabellen TSTimesheetTable returnerer **falsk** under en indsendelse af en timeseddel i appen, vises brugeren en fejlmeddelelse.
- Logik, der udfylder felter (f.eks. **Linjeegenskab**) under metoden **indsæt** i TSTimesheetLine-tabellen, kører stadig.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Skjul og marker standardfelterne som skrivebeskyttede via konfiguration

Fra projektparametrene kan du gøre standardfelter skrivebeskyttede eller skjulte i mobilappen. Angiv indstillingerne i sektionen **Mobile timesedler** under fanen **Timeseddel** på siden **Parametre for projektstyring og regnskab**.

![Projektparametre](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Ændring af de aktiviteter, der er tilgængelige for markering via udvidelser

De aktiviteter, der kan vælges til et projekt, udfyldes via metoderne **getActivitiesForProject()** og **getActivityQuery()** i klassen **TsTimesheetProjectService**. Du kan bruge kommandokæden til at ændre denne funktionsmåde, så den stemmer overens med virksomhedens scenario for de aktiviteter, der kan vælges til et bestemt projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Angiv en standardprojektkategori på timeseddelposter

Indtastning af en standardprojektkategori på timeseddelposteringer sker på tre niveauer. Du kan bruge kommandokæden til at udvide funktionsmåden på et eller flere af disse niveauer for at opnå den ønskede funktionsmåde. Følgende hierarki anvendes:

1. Appen forsøger at anbringe standardkategorien fra projektressourcen. Denne standardkategori er angivet i metoderne **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.
2. Hvis standardkategorien ikke er angivet på projektressourceniveau, forsøger appen at hente den fra projektaktiviteten. Denne standardkategori er angivet i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.
3. Hvis standardkategorien ikke er angivet på projektressourceniveau, hentes standardkategorien fra projektparametrene. Denne standardkategori er angivet i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.
