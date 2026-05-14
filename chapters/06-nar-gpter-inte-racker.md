# Kapitel 6: När GPT:er inte räcker

## Varför detta kapitel finns

Hittills har AI-Analytikern byggts som en egen GPT: först med grundinstruktioner, sedan med bättre beteenderegler, kunskapsfiler och en tydlig metod för produktjämförelser.

En egen GPT är ofta ett mycket bra val när du vill skapa en återanvändbar assistent för en viss uppgift. Men den är inte alltid rätt verktyg. Ibland behöver du bara en vanlig chatt. Ibland vill du ha ett större arbetsutrymme där flera chattar, filer och spår hänger ihop. Ibland vill du att ChatGPT alltid ska känna till dina personliga preferenser.

Det här kapitlet hjälper dig välja mellan fyra vanliga arbetssätt:

- vanlig chatt
- egen GPT
- Project
- Custom Instructions

Målet är inte att hitta ett verktyg som alltid är bäst. Målet är att välja det enklaste arbetssättet som löser uppgiften.

## Lärandemål

Efter kapitlet ska läsaren kunna:

- förklara skillnaden mellan en vanlig chatt, en egen GPT, ett Project och Custom Instructions
- välja rätt arbetssätt för olika typer av AI-uppgifter
- avgöra när AI-Analytikern bör vara en GPT och när den hellre bör användas i ett Project
- undvika att skapa för många speciallösningar i onödan
- beskriva vad som bör vara personlig standardinställning och vad som bör vara uppgiftsspecifik instruktion

## Innan vi börjar

I tidigare kapitel har du arbetat med tre viktiga delar:

- **Instruktioner**: text som styr hur assistenten ska bete sig.
- **Kunskapsfiler**: öppet material som assistenten kan använda som referens.
- **Outputformat**: strukturen på assistentens svar, till exempel en jämförelsetabell.

Nu ska vi placera dessa delar i rätt sammanhang. Samma instruktion kan ibland höra hemma i en GPT, ibland i ett Project och ibland bara i en enskild chatt.

## Fyra arbetssätt i ChatGPT

### 1. Vanlig chatt

En vanlig chatt passar när uppgiften är tillfällig, enkel eller unik.

Exempel:

- “Sammanfatta den här artikeln.”
- “Ge mig fem rubrikförslag.”
- “Förklara skillnaden mellan två begrepp.”
- “Hjälp mig tänka igenom en inköpsfråga.”

En vanlig chatt är snabbast att starta. Du behöver inte bygga något, konfigurera något eller tänka på långsiktig struktur.

Nackdelen är att chatten inte automatiskt blir en återanvändbar assistent. Om du ofta gör samma typ av uppgift behöver du upprepa instruktionerna eller spara dem någon annanstans.

**Använd vanlig chatt när:**

- uppgiften är engångsbaserad
- du inte vet ännu om arbetsflödet ska återanvändas
- du vill experimentera snabbt
- instruktionen är kort och enkel

### 2. Egen GPT

En egen GPT passar när du har en återkommande uppgift och vill att assistenten ska bete sig på ett liknande sätt varje gång.

Exempel:

- en researchassistent för produktjämförelser
- en skrivcoach för nyhetsbrev
- en intern utbildningsassistent med bestämda instruktioner
- en analysassistent som alltid använder samma rapportstruktur

För AI-Analytikern är en GPT ett bra val när du vill att assistenten alltid ska:

- be om jämförelsekriterier
- markera osäker information
- skilja mellan fakta och bedömning
- använda en återkommande rapportmall
- påminna om att aktuell information bör verifieras

**Använd egen GPT när:**

- uppgiften återkommer ofta
- assistenten ska ha en tydlig roll
- du vill spara instruktioner och startfrågor
- flera användare kan ha nytta av samma arbetssätt
- du vill minska behovet av att skriva om samma prompt varje gång

### 3. Project

Ett Project passar när arbetet är större än en enskild fråga eller en enskild assistent. Ett Project kan ses som en arbetsyta där flera chattar, filer och instruktioner hör ihop kring ett ämne eller mål.

Exempel:

- bevaka en bransch över flera veckor
- samla research inför en rapport
- arbeta med en produktjämförelse som består av flera steg
- skapa material till en kurs, kampanj eller analysrapport

För AI-Analytikern kan ett Project vara bättre än en fristående GPT när du arbetar med ett längre researchspår, till exempel:

> “Jämför öppna AI-verktyg för småföretagare och samla underlag till en rapport.”

I ett sådant arbete kan du behöva flera chattar:

- en chatt för att definiera kriterier
- en chatt för att samla frågor
- en chatt för att analysera alternativ
- en chatt för att skriva en rapport
- en chatt för att skapa en presentationsstruktur

Då är projektet själva arbetsytan, medan GPT:n kan vara ett verktyg inne i arbetet.

**Använd Project när:**

- arbetet sträcker sig över flera samtal
- du samlar filer, anteckningar eller öppet källmaterial
- du vill hålla ihop ett större researchområde
- flera deluppgifter hör till samma mål
- sammanhanget är viktigare än en enskild assistentroll

### 4. Custom Instructions

Custom Instructions passar för sådant som du vill att ChatGPT ska känna till generellt, oavsett vilken enskild chatt du öppnar.

Exempel:

- “Svara på svenska om jag inte ber om annat.”
- “Förklara tekniska begrepp enkelt.”
- “Ge alltid praktiska exempel.”
- “Undvik onödigt långa svar.”

Det här är personliga grundinställningar, inte ett specialiserat arbetsflöde.

För AI-Analytikern bör du normalt inte lägga hela researchmetoden i Custom Instructions. Då riskerar alla dina ChatGPT-svar att färgas av researchlogik, även när du bara vill skriva ett mejl, förstå ett begrepp eller brainstorma idéer.

**Använd Custom Instructions när:**

- instruktionen gäller nästan alla dina samtal
- det handlar om ton, språk eller allmän svarsstil
- du vill slippa upprepa personliga preferenser
- instruktionen inte är knuten till ett särskilt projekt

## En enkel beslutsmodell

När du är osäker kan du använda den här frågan:

> Är detta en engångsuppgift, en personlig standard, en återkommande assistent eller ett större arbete?

| Behov | Välj oftast |
|---|---|
| Snabb engångsfråga | Vanlig chatt |
| Personlig stil eller språkpreferens | Custom Instructions |
| Återkommande assistent med tydlig roll | Egen GPT |
| Större arbete med flera steg, filer eller chattar | Project |

Det viktiga är att inte överbygga. Börja enkelt. Flytta uppgiften till en GPT eller ett Project först när du märker att den återkommer eller växer.

## AI-Analytikern som exempel

Tänk att du vill jämföra tre öppna AI-verktyg för omvärldsbevakning.

### Scenario A: snabb jämförelse

Du vill bara få en första överblick.

**Bäst val:** vanlig chatt

Du kan skriva:

```text
Jämför tre typer av verktyg för omvärldsbevakning: nyhetsbevakning, social listening och AI-baserad sammanfattning. Håll svaret övergripande och markera vad som behöver verifieras.
```

Här behövs ingen egen GPT. Du testar bara en idé.

### Scenario B: återkommande produktjämförelser

Du gör ofta produktjämförelser och vill alltid ha samma struktur.

**Bäst val:** egen GPT

AI-Analytikern kan då ha instruktioner som säger:

```text
När användaren ber om en produktjämförelse ska du:
1. fråga vilka kriterier som är viktigast
2. skapa en beslutstabell
3. skilja mellan fakta, bedömning och osäkerhet
4. föreslå vilka uppgifter som bör verifieras mot primärkällor
5. avsluta med en kort rekommendation baserad på angivna behov
```

Här sparar GPT:n tid eftersom samma arbetssätt återkommer.

### Scenario C: längre research inför rapport

Du ska skapa en rapport om trender inom AI-verktyg för småföretagare.

**Bäst val:** Project

Projektet kan innehålla:

- en chatt för mål och avgränsning
- en chatt för källfrågor
- en chatt för jämförelsekriterier
- en chatt för rapportutkast
- öppna filer med egna anteckningar och jämförelsemallar

Här är arbetet större än en GPT. GPT:n kan fortfarande användas, men projektet håller ihop helheten.

### Scenario D: personlig svarsstil

Du vill att ChatGPT alltid ska svara på svenska med praktiska exempel.

**Bäst val:** Custom Instructions

Det är inte en researchmetod. Det är en personlig preferens.

## Vanlig fallgrop: att skapa en GPT för allt

När man lär sig skapa GPT:er är det lätt att vilja skapa en ny GPT för varje idé:

- en GPT för artiklar
- en GPT för listor
- en GPT för rubriker
- en GPT för beslutsunderlag
- en GPT för mötesfrågor
- en GPT för trendspaning

Det kan snabbt bli rörigt.

En bättre start är att skapa färre, tydligare GPT:er. AI-Analytikern kan till exempel täcka flera närliggande uppgifter:

- omvärldsbevakning
- produktjämförelser
- källsammanfattning
- enkel trendanalys
- beslutsunderlag

Om en deluppgift senare blir mycket viktig kan du bryta ut den till en egen GPT.

## Vanlig fallgrop: att lägga för mycket i Custom Instructions

Custom Instructions ska inte bli en gömd handbok för alla tänkbara uppgifter.

Undvik instruktioner som:

```text
Du ska alltid agera som en researchanalytiker, alltid skapa beslutstabeller, alltid bedöma källor och alltid avsluta med en rekommendation.
```

Det låter användbart, men blir störande i samtal där du inte gör research.

Bättre:

```text
Svara normalt på svenska. Förklara nya tekniska begrepp kort innan du använder dem. Använd konkreta exempel när det passar.
```

Den instruktionen hjälper i många sammanhang utan att tvinga alla samtal in i samma mall.

## Praktisk mall: välj rätt arbetssätt

Använd den här mallen innan du bygger något nytt:

```text
1. Vad är uppgiften?
2. Är den engångsbaserad eller återkommande?
3. Behöver uppgiften en tydlig assistentroll?
4. Behöver arbetet samla flera chattar, filer eller delspår?
5. Är instruktionen personlig och generell, eller specifik för en uppgift?
6. Vilket är enklaste fungerande arbetssätt?
```

Exempel:

```text
1. Uppgift: Jämföra verktyg för AI-baserad nyhetsbevakning.
2. Återkommande: Ja, jag vill göra detta flera gånger.
3. Assistentroll: Ja, researchanalytiker.
4. Flera chattar/filer: Inte just nu.
5. Personlig eller specifik: Specifik för research.
6. Val: Egen GPT.
```

## Rekommenderad struktur för AI-Analytikern

För bokens fortsättning rekommenderas denna uppdelning:

| Del | Rekommenderat arbetssätt |
|---|---|
| Personlig svarsstil | Custom Instructions |
| Själva researchassistenten | Egen GPT |
| Större omvärldsbevakning över tid | Project |
| Snabba testfrågor | Vanlig chatt |
| Senare automatiseringar | Externa verktyg eller agentflöden |

Det betyder att AI-Analytikern inte behöver bära allt själv. Den är en central assistent, men den kan ingå i ett större arbetssätt.

## Övningar

### Övning 1: Sortera tre uppgifter

Välj rätt arbetssätt för varje uppgift:

1. Du vill snabbt sammanfatta en artikel.
2. Du vill bygga en återkommande assistent för produktjämförelser.
3. Du vill samla research inför en rapport under flera veckor.

Skriv ditt svar i formen:

```text
Uppgift 1: ...
Motivering: ...

Uppgift 2: ...
Motivering: ...

Uppgift 3: ...
Motivering: ...
```

### Övning 2: Granska AI-Analytikern

Titta på din nuvarande idé för AI-Analytikern och svara:

```text
Vilka delar ska ligga i GPT:n?
Vilka delar passar bättre i ett Project?
Vilka personliga preferenser hör hemma i Custom Instructions?
Vilka uppgifter kan göras i vanlig chatt?
```

### Övning 3: Förenkla innan du bygger

Välj en AI-idé du har och fyll i beslutsmallen:

```text
1. Vad är uppgiften?
2. Är den engångsbaserad eller återkommande?
3. Behöver uppgiften en tydlig assistentroll?
4. Behöver arbetet samla flera chattar, filer eller delspår?
5. Är instruktionen personlig och generell, eller specifik för en uppgift?
6. Vilket är enklaste fungerande arbetssätt?
```

## Snabb sammanfattning

- Vanlig chatt passar bäst för snabba engångsuppgifter.
- En egen GPT passar bäst för återkommande uppgifter med tydlig roll och metod.
- Ett Project passar bäst för större arbeten med flera chattar, filer eller delspår.
- Custom Instructions passar bäst för personliga grundinställningar som språk, ton och förklaringsnivå.
- AI-Analytikern bör vara en GPT när du vill återanvända researchmetoden, men ett Project passar bättre när arbetet växer till en längre omvärldsbevakning eller rapport.
- Börja enkelt och bygg bara mer struktur när uppgiften kräver det.

## Nästa steg

Nu har du en modell för att välja rätt arbetssätt. I nästa kapitel använder vi den modellen för att skapa mer specialiserade assistenter för olika analysuppgifter, till exempel trendspaning, källsammanfattning och beslutsunderlag.
