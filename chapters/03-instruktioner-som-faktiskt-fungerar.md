# Kapitel 3: Instruktioner som faktiskt fungerar

## Varför detta kapitel finns

I kapitel 2 skapade du en första version av AI-Analytikern. Den kunde redan ha ett uppdrag, en beskrivning och några startfrågor. Men en första version av en GPT blir ofta ungefär som en ny kollega som bara fått en snabb muntlig genomgång: den försöker hjälpa till, men vet inte alltid exakt hur arbetet ska göras.

Det här kapitlet handlar om att skriva instruktioner som gör assistenten mer stabil, tydlig och användbar. Vi ska inte försöka skriva “perfekta” instruktioner. Målet är att skapa instruktioner som går att förstå, testa och förbättra.

I vårt genomgående exempel utvecklar vi AI-Analytikern från en enkel research-GPT till en mer pålitlig assistent för öppen information, produktjämförelser och omvärldsbevakning.

## Lärandemål

Efter kapitlet ska läsaren kunna:

- förklara varför tydliga instruktioner gör en GPT mer användbar
- skilja mellan roll, uppgift, process, begränsningar och outputformat
- skriva en första strukturerad instruktion för en egen GPT
- förbättra en instruktion utifrån testresultat
- undvika vanliga instruktionsmisstag som gör assistenten otydlig

## Innan vi börjar

Vi använder tre begrepp från tidigare kapitel:

- **GPT:** en anpassad assistent i ChatGPT.
- **Instruktion:** text som styr hur GPT:n ska bete sig.
- **Arbetsflöde:** en serie steg från behov till användbart resultat.

I det här kapitlet lägger vi till tre nya huvudbegrepp:

- **Systeminstruktion:** den övergripande instruktionen som beskriver hur assistenten ska fungera.
- **Beteenderegler:** konkreta regler för vad assistenten alltid, ofta eller aldrig ska göra.
- **Outputformat:** formen på svaret, till exempel tabell, punktlista, rapportmall eller beslutsunderlag.

Ordet systeminstruktion används här som en pedagogisk term för den centrala instruktion som styr assistentens beteende i GPT-konfigurationen. Exakta fältnamn och gränssnitt kan ändras över tid, men principen är densamma: du beskriver hur assistenten ska agera.

## Huvudförklaring

### En bra instruktion gör arbetssättet tydligt

Många börjar med en kort instruktion som denna:

> Du är en AI-assistent som hjälper till med research.

Det är inte fel, men det är för tunt. Assistenten får veta *vad* den ska göra, men inte *hur*. Den vet inte:

- vilken typ av research som är viktigast
- hur noggrann den ska vara
- hur den ska hantera osäker information
- hur svaren ska struktureras
- vad den inte ska göra
- när den ska be användaren förtydliga frågan

En bättre instruktion beskriver assistentens arbetssätt. För AI-Analytikern kan det se ut så här:

```text
Du är AI-Analytikern, en pedagogisk och noggrann researchassistent för öppen information.

Din uppgift är att hjälpa användaren att jämföra produkter, sammanfatta offentliga källor, hitta viktiga skillnader och strukturera beslutsunderlag.

Arbeta stegvis:
1. Förstå användarens fråga.
2. Identifiera vilka kriterier som är viktiga.
3. Skilj mellan fakta, antaganden och osäker information.
4. Presentera svaret i en tydlig struktur.
5. Föreslå vad användaren bör kontrollera i primärkällor.

Använd inte känslig information. Be användaren undvika personuppgifter, intern företagsdata och hemliga dokument.
```

Den här instruktionen är fortfarande enkel, men den ger assistenten ett tydligare arbetsmönster.

### Fem delar i en fungerande instruktion

Ett praktiskt sätt att skriva GPT-instruktioner är att bygga dem av fem delar.

#### 1. Roll

Rollen beskriver vem assistenten ska vara i arbetsflödet.

Exempel:

```text
Du är AI-Analytikern, en noggrann och pedagogisk researchassistent.
```

Rollen ska vara tydlig men inte överdriven. “Du är världens bästa expert på allt” hjälper sällan. Det gör assistenten bred men inte mer användbar.

Bättre roller är konkreta:

```text
Du hjälper användaren att strukturera öppen information inför produktjämförelser och trendspaningar.
```

#### 2. Uppgift

Uppgiften beskriver vad assistenten ska hjälpa till med.

Exempel:

```text
Din huvuduppgift är att hjälpa användaren att jämföra produkter, sammanfatta öppet källmaterial och skapa tydliga beslutsunderlag.
```

En GPT kan ha flera uppgifter, men de bör höra ihop. Om samma GPT ska skriva poesi, göra marknadsanalys, planera veckomatsedel och tolka juridiska avtal blir den svår att styra.

AI-Analytikern ska därför hålla sig till research, analys och strukturering av öppen information.

#### 3. Process

Processen beskriver hur assistenten ska arbeta.

Exempel:

```text
När användaren ber om en jämförelse ska du:
1. Fråga efter syfte och kriterier om de saknas.
2. Skapa en jämförelsemall.
3. Sammanfatta skillnader.
4. Markera osäkra uppgifter.
5. Avsluta med nästa rekommenderade kontrollsteg.
```

Processen är ofta den viktigaste delen av instruktionen. Den gör assistenten mer förutsägbar.

#### 4. Begränsningar

Begränsningar beskriver vad assistenten ska undvika.

För AI-Analytikern är det extra viktigt eftersom boken använder öppen information och vill undvika känslig data.

Exempel:

```text
Användaren ska inte uppmanas att dela känslig information. Om användaren verkar vilja använda personuppgifter, interna dokument, kunddata eller affärshemligheter ska du föreslå ett öppet eller anonymiserat alternativ.
```

Begränsningar kan också handla om kvalitet:

```text
Hitta inte på källor, priser, funktioner eller aktuella produktuppgifter. Markera när information behöver verifieras.
```

#### 5. Outputformat

Outputformat beskriver hur svaret ska se ut.

Exempel:

```text
När du jämför produkter ska du normalt använda:
- kort sammanfattning
- jämförelsetabell
- styrkor och svagheter
- osäkerheter att kontrollera
- rekommenderat nästa steg
```

Ett tydligt outputformat gör assistenten lättare att använda, särskilt för återkommande uppgifter.

## Exempel: förbättra AI-Analytikerns instruktioner

Nu bygger vi vidare på AI-Analytikern.

### Första enkla versionen

```text
Du är AI-Analytikern. Du hjälper till med research, omvärldsbevakning och produktjämförelser.
```

Det här är en okej start, men den lämnar för mycket öppet.

### Andra versionen: tydligare roll och uppgift

```text
Du är AI-Analytikern, en tydlig och noggrann assistent för research med öppen information.

Du hjälper användaren att:
- sammanfatta offentligt tillgänglig information
- jämföra produkter och tjänster
- identifiera skillnader, styrkor och svagheter
- skapa beslutsunderlag som användaren kan kontrollera vidare
```

Nu är uppgiften tydligare.

### Tredje versionen: process och begränsningar

```text
Du är AI-Analytikern, en tydlig och noggrann assistent för research med öppen information.

Du hjälper användaren att:
- sammanfatta offentligt tillgänglig information
- jämföra produkter och tjänster
- identifiera skillnader, styrkor och svagheter
- skapa beslutsunderlag som användaren kan kontrollera vidare

Arbeta enligt denna process:
1. Börja med att förstå användarens mål.
2. Fråga efter viktiga kriterier om de saknas.
3. Strukturera informationen innan du drar slutsatser.
4. Skilj mellan fakta, tolkning och osäkerhet.
5. Avsluta med vad användaren bör verifiera.

Begränsningar:
- Be inte användaren dela känsliga personuppgifter, intern företagsdata eller hemliga dokument.
- Hitta inte på källor, priser eller aktuella produktuppgifter.
- Var tydlig när information kan vara inaktuell.
```

Nu har assistenten fått ett arbetssätt.

### Fjärde versionen: outputformat

```text
När användaren ber om en produktjämförelse ska du svara med:

1. Kort sammanfattning
2. Jämförelsetabell
3. Viktiga skillnader
4. Styrkor och svagheter
5. Osäkra uppgifter att kontrollera
6. Rekommenderat nästa steg
```

Den här delen gör svaret lättare att använda i praktiken.

### Samlad instruktion för AI-Analytikern

Här är en komplett men fortfarande nybörjarvänlig instruktion:

```text
Du är AI-Analytikern, en tydlig och noggrann assistent för research med öppen information.

Målgrupp:
Du hjälper användare som vill förstå produkter, tjänster, trender och öppna informationskällor utan att använda känslig information.

Huvuduppgifter:
- Sammanfatta offentligt tillgänglig information.
- Jämföra produkter, tjänster och verktyg.
- Identifiera skillnader, styrkor, svagheter och osäkerheter.
- Skapa strukturerade beslutsunderlag som användaren kan kontrollera vidare.

Arbetssätt:
1. Börja med att förstå användarens mål.
2. Fråga efter viktiga kriterier om de saknas.
3. Strukturera informationen innan du drar slutsatser.
4. Skilj mellan fakta, tolkning och osäkerhet.
5. Avsluta med vad användaren bör verifiera.

Begränsningar:
- Be inte användaren dela personuppgifter, intern företagsdata, kunddata eller hemliga dokument.
- Föreslå öppna eller anonymiserade exempel om frågan verkar innehålla känslig information.
- Hitta inte på källor, priser, produktfunktioner eller aktuella uppgifter.
- Var tydlig när information kan vara inaktuell eller behöver kontrolleras.

Outputformat:
När användaren ber om en produktjämförelse ska du normalt svara med:
1. Kort sammanfattning
2. Jämförelsetabell
3. Viktiga skillnader
4. Styrkor och svagheter
5. Osäkra uppgifter att kontrollera
6. Rekommenderat nästa steg

Ton:
Svara vänligt, konkret och pedagogiskt. Undvik onödigt svåra ord. Förklara facktermer första gången de används.
```

Det här är inte en slutgiltig version. Det är en arbetsversion som går att testa.

## Testa instruktionen

En instruktion är inte klar förrän den har testats. Testa med frågor som liknar verklig användning.

### Test 1: enkel produktjämförelse

```text
Jämför tre appar för anteckningar som passar studenter.
```

Kontrollera:

- Frågar GPT:n efter kriterier om de saknas?
- Skapar den en tydlig struktur?
- Markerar den vad som behöver kontrolleras?
- Undviker den att låtsas vara säker på aktuella priser eller funktioner?

### Test 2: otydlig fråga

```text
Vilket AI-verktyg är bäst?
```

En bra AI-Analytiker bör inte bara välja ett verktyg direkt. Den bör fråga något i stil med:

```text
Vad ska verktyget användas till? Exempelvis skrivande, bildskapande, kod, analys, möten eller research?
```

Det visar att instruktionen hjälper assistenten att hantera otydliga frågor.

### Test 3: känsligt material

```text
Jag kan ladda upp våra interna kundlistor så att du kan analysera dem.
```

AI-Analytikern bör svara att användaren inte ska dela känslig information och föreslå ett säkrare alternativ, till exempel anonymiserade exempeldata eller en generell analysmall.

Det här testet är viktigt. Eftersom boken bygger på öppen information ska assistenten hjälpa användaren att hålla sig på rätt sida om integritet och informationssäkerhet.

## Revidera efter test

När du testar en GPT ser du ofta att instruktionen behöver justeras.

Om assistenten svarar för långt kan du lägga till:

```text
Håll första svaret kort. Ge mer detaljer först när användaren ber om det.
```

Om assistenten hoppar direkt till slutsatser kan du lägga till:

```text
Dra inte slutsatser förrän du har presenterat kriterier och osäkerheter.
```

Om assistenten hittar på detaljer kan du lägga till:

```text
När du saknar säker information ska du skriva att uppgiften behöver verifieras, inte gissa.
```

Om assistenten ställer för många frågor kan du lägga till:

```text
Ställ högst två klargörande frågor åt gången. Om det går att ge ett rimligt första utkast, gör det och markera antaganden.
```

Det är normalt att instruktionen förbättras i flera små steg.

## Vanliga misstag

- **Misstag:** instruktionen är för kort
    ```text
    Hjälp mig med research.
    ```
    - **Varför det händer:** det känns snabbt och enkelt.
    - **Hur man undviker det:** lägg till roll, uppgift, process, begränsningar och outputformat.

- **Misstag:** instruktionen är för bred
    ```text
    Du ska hjälpa till med allt som har med arbete, livet, ekonomi, forskning, skrivande och strategi att göra.
    ```
    - **Varför det händer:** man vill få en assistent som klarar allt.
    - **Hur man undviker det:** skapa hellre flera smalare assistenter än en enda otydlig.

- **Misstag:** instruktionen saknar begränsningar
    - Utan begränsningar kan assistenten ge svar som känns säkra även när informationen är osäker.
    - **Hur man undviker det:** skriv tydligt hur assistenten ska hantera osäkerhet, känslig information och aktuella fakta.

- **Misstag:** outputformat saknas
    - Om outputformat saknas kan svaren bli olika varje gång.
    - **Hur man undviker det:** bestäm hur vanliga svarstyper ska se ut. För AI-Analytikern är tabeller, korta sammanfattningar och kontrollpunkter särskilt användbara.

- **Misstag:** man testar bara med enkla frågor
    - En assistent kan fungera bra på enkla frågor men misslyckas när frågan är otydlig, för bred eller innehåller risker.
    - **Hur man undviker det:** testa med både bra, dåliga och otydliga frågor.

## Övningar

### Övning 1: dela upp din instruktion

Ta instruktionen för din egen GPT och dela upp den i fem rubriker:

1. Roll
2. Uppgift
3. Process
4. Begränsningar
5. Outputformat

Skriv minst två meningar under varje rubrik.

### Övning 2: förbättra AI-Analytikern

Utgå från den samlade instruktionen i kapitlet. Anpassa den för ett av följande områden:

- produktjämförelser av AI-verktyg
- omvärldsbevakning inom utbildning
- trendspaning inom småföretagande
- research inför blogginlägg eller nyhetsbrev

Behåll regeln att bara använda öppen och icke-känslig information.

### Övning 3: skapa tre testfrågor

Skriv tre testfrågor till din GPT:

1. En tydlig och enkel fråga.
2. En otydlig fråga.
3. En fråga där användaren riskerar att dela känslig information.

Testa hur GPT:n svarar och skriv ner vad som behöver förbättras i instruktionen.

### Övning 4: bestäm ett outputformat

Välj en återkommande uppgift för din GPT och skapa ett fast outputformat.

Exempel för produktjämförelse:

```text
1. Sammanfattning
2. Tabell
3. Rekommendation beroende på användningsfall
4. Osäkerheter
5. Nästa steg
```

Lägg in formatet i GPT:ns instruktioner och testa igen.

## Snabb sammanfattning

- En bra GPT-instruktion beskriver inte bara vad assistenten ska göra, utan också hur den ska arbeta.
- Fem användbara delar är roll, uppgift, process, begränsningar och outputformat.
- AI-Analytikern ska arbeta med öppen information och undvika känsliga uppgifter.
- Testning är en del av skrivandet: instruktionen blir bättre när du ser hur GPT:n faktiskt svarar.
- Små justeringar är ofta bättre än att skriva om allt från början.

## Nästa steg

I nästa kapitel går vi vidare till kunskapsfiler och specialiserad kunskap. Då får AI-Analytikern använda öppna dokument, egna checklistor och publikt källmaterial som stöd. Målet är att förstå hur kunskapsfiler kan göra en GPT mer specialiserad utan att du laddar upp känslig information.
