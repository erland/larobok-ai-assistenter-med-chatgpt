# Kapitel 9: Vanliga misstag och dåliga designmönster

## Varför detta kapitel finns

När man börjar skapa egna GPT:er är det lätt att tänka att problemet alltid är “för lite instruktion”. Om assistenten svarar dåligt lägger man till mer text. Om den missförstår lägger man till ännu fler regler. Till slut har man en GPT som är lång, rörig och ändå inte särskilt pålitlig.

Det här kapitlet handlar om motsatsen: att känna igen misstag som gör assistenter svåra att använda, svåra att testa eller svåra att förbättra. Vi använder AI-Analytikern som exempel och fokuserar på öppna informationsuppgifter, till exempel omvärldsbevakning, produktjämförelser och trendspaning.

Målet är inte att undvika alla fel. Målet är att snabbare se vilket slags fel du har framför dig och veta hur du kan rätta till det.

## Lärandemål

Efter kapitlet ska läsaren kunna:

- känna igen vanliga misstag när en GPT designas
- förstå varför en assistent blir för bred, för vag eller för självsäker
- skilja mellan dåliga instruktioner och dåligt avgränsade uppgifter
- förbättra en GPT genom att ta bort, förenkla eller dela upp instruktioner
- använda en enkel felsökningsmetod när assistenten inte beter sig som tänkt

## Innan vi börjar

I kapitel 8 testade du AI-Analytikern med testfall, utvärderingskriterier och iterationslogg. Nu använder vi testresultaten för att identifiera designproblem.

Kom ihåg tre tidigare begrepp:

- **Rollgräns:** vad assistenten ska och inte ska göra.
- **Utvärderingskriterium:** vad du använder för att bedöma kvalitet.
- **Osäkerhet:** sådant som saknas, är oklart eller behöver verifieras.

I det här kapitlet introducerar vi tre nya huvudbegrepp:

- **Designmönster**
- **Anti-pattern**
- **Felsökningsfråga**

## Huvudförklaring

### Vad är ett designmönster?

Ett **designmönster** är ett återkommande sätt att lösa ett problem. I en GPT kan ett bra designmönster vara:

- att ge assistenten en tydlig roll
- att kräva att den anger antaganden
- att använda ett fast outputformat
- att be den skilja fakta, analys och rekommendation
- att alltid markera när aktuell information behöver kontrolleras

Ett designmönster är inte en magisk regel. Det är ett beprövat arbetssätt som ofta fungerar.

### Vad är ett anti-pattern?

Ett **anti-pattern** är ett återkommande arbetssätt som verkar bra först men ofta skapar problem senare.

Exempel:

> “Jag gör min GPT så bred som möjligt så att den kan hjälpa till med allt.”

Det låter effektivt, men resultatet blir ofta en assistent som är svår att testa, svår att förstå och svår att förbättra.

Ett anti-pattern är alltså inte bara ett misstag. Det är ett misstag som är vanligt eftersom det känns rimligt i början.

### Misstag 1: Assistenten är för bred

En för bred GPT har ett uppdrag som nästan betyder “hjälp mig med allt”. Den kan verka användbar i början, men den blir snabbt otydlig.

Svag instruktion:

```text
Du är en AI-assistent som hjälper mig med research, skrivande, analys, planering, strategi, marknadsföring och beslutsstöd.
```

Problemet är inte att uppgifterna är dåliga. Problemet är att de är för många samtidigt. Assistenten vet inte vad den ska prioritera.

Bättre instruktion:

```text
Du är AI-Analytikern. Din huvuduppgift är att hjälpa användaren strukturera och jämföra öppen information om produkter, trender och marknader. Du ska fokusera på research, sammanfattning, jämförelse och osäkerheter. Du ska inte agera personlig rådgivare, juridisk expert eller beslutsfattare.
```

Det här gör tre saker:

1. Rollen blir tydligare.
2. Uppgifterna avgränsas.
3. Rollgränsen blir synlig.

### Misstag 2: Assistenten låter säkrare än den är

AI-assistenter kan formulera sig övertygande även när underlaget är svagt. För AI-Analytikern är detta extra viktigt eftersom omvärldsbevakning och produktjämförelser ofta beror på aktuell information.

Svagt svarsbeteende:

> “Verktyg A är bäst för småföretag.”

Bättre svarsbeteende:

> “Utifrån de kriterier du angivit verkar verktyg A passa bäst, men pris, funktioner och villkor bör kontrolleras mot aktuella källor innan beslut.”

Skillnaden är stor. Det första låter som en slutgiltig sanning. Det andra visar att rekommendationen är beroende av kriterier och aktuell information.

En bra instruktion kan vara:

```text
När du jämför produkter eller tjänster ska du skilja mellan bekräftad information, rimliga antaganden och sådant som behöver verifieras mot aktuella källor.
```

### Misstag 3: Instruktionen försöker lösa allt samtidigt

Ibland blir en GPT dålig för att instruktionen är för kort. Men lika ofta blir den dålig för att instruktionen är för lång och blandar olika mål.

Exempel på rörig instruktion:

```text
Var pedagogisk, snabb, detaljerad, kortfattad, kreativ, kritisk, positiv, affärsmässig, enkel, komplett och ge alltid bästa möjliga svar i tabellform men också med förklaringar och rekommendationer.
```

Flera av orden krockar med varandra. Ska svaret vara kortfattat eller detaljerat? Snabbt eller komplett? Kreativt eller strikt jämförande?

Bättre:

```text
Svara i tre delar:
1. Kort sammanfattning.
2. Strukturerad jämförelse.
3. Osäkerheter och nästa steg.

Prioritera tydlighet före längd. Använd tabell när flera alternativ jämförs.
```

Den förbättrade instruktionen säger inte bara hur assistenten ska vara. Den säger vad den ska göra.

### Misstag 4: Allt stoppas in i en enda GPT

När man har lärt sig skapa GPT:er är det frestande att bygga en “superassistent”. Den ska bevaka trender, jämföra produkter, skriva rapporter, skapa inlägg, analysera målgrupper och föreslå strategi.

Det kan fungera ibland, men blir ofta svårt att styra.

Ett bättre mönster är att skapa flera specialiserade assistenter:

| Assistent | Uppgift |
|---|---|
| Research-GPT | Samlar och strukturerar öppen information |
| Jämförelse-GPT | Jämför alternativ mot kriterier |
| Rapport-GPT | Omvandlar analys till läsbar rapport |
| Källkritik-GPT | Letar efter svagheter, antaganden och luckor |

Det betyder inte att du alltid ska skapa många GPT:er. Men om en assistent får för många roller kan uppdelning vara enklare än fler instruktioner.

### Misstag 5: Man testar bara lyckade exempel

Ett vanligt fel är att bara testa assistenten med uppgifter som man redan vet att den klarar. Då får man en falsk känsla av kvalitet.

För AI-Analytikern bör du även testa svåra situationer:

- användaren ger för lite information
- användaren ber om en tvärsäker slutsats
- uppgiften kräver aktuell information
- kriterierna är motsägelsefulla
- underlaget är vinklat eller ofullständigt

Exempel på testfråga:

```text
Vilket AI-verktyg är bäst för alla småföretag?
```

En svag assistent försöker svara direkt. En bättre assistent bromsar:

```text
Det går inte att utse ett bästa verktyg för alla småföretag utan kriterier. Jag kan däremot hjälpa dig jämföra alternativ utifrån exempelvis pris, användningsområde, dataskydd, språkstöd och integrationsbehov.
```

### Misstag 6: Man blandar öppna och känsliga uppgifter

Eftersom vårt exempelprojekt handlar om öppen information ska AI-Analytikern inte behöva känsliga kunddata, interna dokument eller personuppgifter.

Dålig användning:

```text
Här är våra interna kundlistor och försäljningssiffror. Analysera konkurrentläget.
```

Bättre användning:

```text
Utgå från offentliga webbplatser, produktbeskrivningar, öppna rapporter och användarrecensioner. Skapa en jämförelsemall för konkurrentanalys utan att använda intern eller känslig information.
```

Det här är både säkrare och mer pedagogiskt. Läsaren kan öva utan att riskera att dela fel information.

### Misstag 7: Man saknar felsökningsfråga

En **felsökningsfråga** är en enkel fråga som hjälper dig förstå varför assistenten beter sig dåligt.

När AI-Analytikern ger ett svagt svar kan du fråga:

| Problem | Felsökningsfråga |
|---|---|
| Svaret är för allmänt | Är assistentens roll för bred? |
| Svaret är för långt | Saknas tydligt outputformat? |
| Svaret är för säkert | Har instruktionen krav på osäkerhetsmarkering? |
| Svaret missar uppgiften | Är användarens input för vag? |
| Svaret blandar ihop saker | Behöver uppgiften delas i flera steg? |
| Svaret blir olika varje gång | Behövs tydligare kriterier eller exempel? |

Felsökning handlar inte om att bli irriterad på assistenten. Det handlar om att hitta vilken del av designen som behöver ändras.

## Exempel: förbättra AI-Analytikern

Anta att AI-Analytikern har följande instruktion:

```text
Du hjälper användaren med research och analys.
```

Den är inte fel, men den är för vag. Om du testar den med produktjämförelser kan den ge snygga men ojämna svar.

Vi förbättrar den stegvis.

### Version 1: tydligare roll

```text
Du är AI-Analytikern, en assistent för omvärldsbevakning, produktjämförelser och strukturering av öppen information.
```

Nu vet assistenten vilket område den arbetar inom.

### Version 2: tydligare arbetssätt

```text
När du hjälper användaren ska du:
1. sammanfatta uppgiften
2. ange vilka antaganden du gör
3. föreslå jämförelsekriterier
4. strukturera informationen i tabell eller punktlista
5. markera vad som behöver verifieras
```

Nu får assistenten ett arbetsflöde.

### Version 3: tydligare gränser

```text
Använd inte känslig, intern eller personlig information som krav för att lösa uppgiften. Om användaren verkar vilja dela sådan information ska du föreslå en säker, anonymiserad eller offentlig variant av uppgiften.
```

Nu passar assistenten bättre för bokens exempelprojekt.

### Version 4: tydligare kvalitet

```text
Ge inte tvärsäkra rekommendationer när informationen är tidskänslig, ofullständig eller beroende av användarens prioriteringar. Skriv i stället vilka kriterier rekommendationen bygger på.
```

Nu blir svaren mer ansvarsfulla.

## Vanliga misstag

- **Misstag:** att lägga till mer instruktion utan att ta bort något
    - **Varför det händer:** Det känns naturligt att lösa problem genom att lägga till fler regler.
    - **Hur man undviker det:** Fråga först vilken regel som är otydlig, överflödig eller motsägelsefull.

- **Misstag:** att göra assistenten för personlig
    - **Varför det händer:** Man vill att assistenten ska kännas hjälpsam och nära användaren.
    - **Hur man undviker det:** För öppna researchuppgifter är det ofta bättre att göra assistenten saklig, tydlig och källkritisk än personlig.

- **Misstag:** att blanda roll och outputformat
    - **Varför det händer:** Man skriver allt i en lång instruktion.
    - **Hur man undviker det:** Dela upp instruktionen i roll, uppgift, arbetssätt, gränser och format.

- **Misstag:** att behandla GPT:n som en databas
    - **Varför det händer:** Assistenten svarar självsäkert och kan mycket.
    - **Hur man undviker det:** Påminn i instruktionen om att aktuell information, priser, villkor och produktfunktioner behöver kontrolleras.

## Praktisk övning

### Övning 1: hitta anti-patterns

Läs instruktionen nedan:

```text
Du är en superassistent som hjälper till med alla typer av analys, strategi, research, marknadsföring, produktval, ledarskap och tekniska beslut. Svara alltid snabbt, komplett och kreativt. Ge alltid en tydlig rekommendation.
```

Gör tre saker:

1. Markera minst tre problem.
2. Skriv om instruktionen för AI-Analytikern.
3. Lägg till en regel om öppen information och osäkerhet.

### Övning 2: skapa en felsökningstabell

Skapa en tabell med tre kolumner:

| Testresultat | Trolig orsak | Förbättring |
|---|---|---|

Fyll i minst fem rader baserat på problem du kan tänka dig i AI-Analytikern.

Exempel:

| Testresultat | Trolig orsak | Förbättring |
|---|---|---|
| Assistenten rekommenderar ett verktyg för snabbt | Saknar regel om osäkerhet | Lägg till krav på kriterier och verifiering |

### Övning 3: dela upp en för bred assistent

Anta att AI-Analytikern har blivit för bred. Dela upp den i tre mindre assistenter:

1. En för research.
2. En för jämförelse.
3. En för rapportskrivning.

Skriv en kort rollbeskrivning för varje assistent.

## Snabb sammanfattning

- En för bred GPT blir ofta svår att testa och förbättra.
- Ett anti-pattern är ett vanligt arbetssätt som verkar bra men skapar problem.
- Fler instruktioner är inte alltid lösningen; ibland behöver instruktionen förenklas.
- AI-Analytikern bör hålla sig till öppen information och markera osäkerheter.
- Svaga svar kan ofta felsökas med enkla frågor om roll, format, gränser och kriterier.
- När en assistent får för många uppgifter kan det vara bättre att dela upp den i flera specialiserade assistenter.

## Nästa steg

Nu har du byggt, förbättrat och felsökt egna GPT:er. I nästa kapitel tar vi ett steg utanför själva GPT:n och tittar på AI-agenter och automatisering. Där handlar det inte bara om vad en assistent svarar, utan om hur AI kan ingå i längre arbetsflöden med flera steg och verktyg.
