# Kapitel 7: Specialiserade assistenter för olika analysuppgifter

## Varför detta kapitel finns

Hittills har AI-Analytikern vuxit från en enkel idé till en mer användbar GPT med tydligare instruktioner, kunskapsfiler och jämförelsemallar. Den kan hjälpa till med research och produktjämförelser, men det finns en vanlig fälla: man försöker göra en enda assistent som ska klara allt.

Det kan fungera i början. Men ju fler uppgifter du lägger in, desto svårare blir det för assistenten att vara tydlig, konsekvent och enkel att testa. En assistent som ska vara trendspanare, produktjämförare, källkritiker, rapportskrivare och strategisk rådgivare samtidigt kan snabbt bli otydlig.

I det här kapitlet lär du dig att dela upp ett brett behov i flera specialiserade assistenter. Målet är inte att skapa många GPT:er för sakens skull, utan att skapa tydligare arbetsroller.

## Lärandemål

Efter kapitlet ska du kunna:

- förklara varför en specialiserad assistent ofta fungerar bättre än en för bred assistent
- skilja mellan en huvudassistent och en specialiserad assistent
- definiera rollgränser för en GPT
- skapa en återanvändbar mall för specialiserade assistenter
- bygga vidare på AI-Analytikern med flera fokuserade analysroller

## Innan vi börjar

I tidigare kapitel har du redan mött tre viktiga byggstenar:

- **Instruktioner** styr hur assistenten ska agera.
- **Kunskapsfiler** ger assistenten extra underlag.
- **Jämförelsekriterier** hjälper assistenten att arbeta strukturerat.

Nu använder vi samma byggstenar, men organiserar dem på ett nytt sätt. I stället för att lägga allt i en enda GPT skapar vi ett litet team av assistenter, där varje assistent har en tydlig uppgift.

Det här kapitlet introducerar tre nya huvudbegrepp:

- **specialisering**
- **rollgräns**
- **återanvändbar mall**

## Problemet med den alltför breda assistenten

Det är lätt att börja med en instruktion som låter ungefär så här:

> Du är en expertassistent som hjälper mig med research, trendspaning, produktjämförelser, källkritik, rapportskrivning, idéutveckling, strategi, planering och automatisering.

Det kan låta kraftfullt. Men för en nybörjare är det ofta ett varningstecken. Instruktionen säger mycket, men den prioriterar inte. Assistenten får för många roller samtidigt.

En för bred assistent kan ge flera problem:

- Den vet inte vilken typ av svar som är viktigast.
- Den blandar analys, skrivande och rådgivning.
- Den blir svår att testa eftersom varje fråga kan tolkas på många sätt.
- Den kan ge för långa svar eftersom den försöker täcka allt.
- Den kan börja hitta på struktur i stället för att följa en tydlig process.

Det betyder inte att breda assistenter alltid är dåliga. En bred assistent kan fungera som startpunkt eller nav. Men när ett arbetsflöde blir återkommande är det ofta bättre att skapa mer fokuserade roller.

## Vad specialisering betyder

**Specialisering** betyder att en assistent får ett tydligt avgränsat uppdrag.

En specialiserad assistent ska inte försöka vara bäst på allt. Den ska vara bra på en viss typ av uppgift.

Exempel:

| Bred uppgift | Specialiserad assistent |
|---|---|
| Hjälp mig med research | Researchplaneraren |
| Håll koll på trender | Trendspanaren |
| Jämför produkter | Produktjämföraren |
| Granska källor | Källkritikern |
| Skriv en rapport | Rapportbyggaren |

Skillnaden är inte bara namnet. Varje specialiserad assistent har egna instruktioner, egna begränsningar och ett eget outputformat.

## Huvudassistent och specialiserade assistenter

Ett praktiskt sätt att tänka är att AI-Analytikern kan vara huvudassistenten. Den hjälper användaren att välja arbetssätt och strukturera processen.

Sedan kan specialiserade assistenter ta hand om enskilda delar.

Exempel:

1. **AI-Analytikern** hjälper dig formulera analysfrågan.
2. **Trendspanaren** hittar möjliga utvecklingsområden att undersöka.
3. **Produktjämföraren** strukturerar jämförelsen mellan alternativ.
4. **Källkritikern** granskar underlagets styrkor och svagheter.
5. **Rapportbyggaren** gör resultatet läsbart för en mottagare.

Det här är fortfarande ett enkelt arbetssätt. Du behöver inte automatisera något än. Du kan använda en assistent i taget och kopiera över öppet, kontrollerbart underlag mellan stegen.

## Rollgräns: vad assistenten ska och inte ska göra

En **rollgräns** beskriver vad en assistent ansvarar för och vad den ska lämna vidare.

Rollgränsen är viktig eftersom den hindrar assistenten från att göra för mycket.

En bra rollgräns svarar på fyra frågor:

1. Vilken uppgift ska assistenten lösa?
2. Vilken uppgift ska assistenten inte lösa?
3. Vilket underlag behöver assistenten?
4. Vilket resultat ska assistenten lämna ifrån sig?

Här är ett enkelt exempel.

### Rollgräns för Produktjämföraren

**Ska göra:**

- strukturera jämförelser mellan produkter eller tjänster
- föreslå jämförelsekriterier
- skapa beslutstabeller
- markera osäker information
- skilja mellan fakta och bedömning

**Ska inte göra:**

- låtsas veta aktuella priser utan källa
- ge definitiv köprekommendation utan att visa osäkerheter
- använda känslig intern information
- ersätta användarens eget beslut

**Behöver:**

- produktnamn
- länkar, utdrag eller beskrivningar från öppna källor
- användarens prioriteringar
- datum för jämförelsen om informationen kan förändras

**Lämnar ifrån sig:**

- jämförelsetabell
- kort analys
- osäkerheter att verifiera
- rekommenderad nästa kontroll

Det här gör assistenten tydligare både för dig och för läsaren.

## Tre specialiserade assistenter för AI-Analytikern

Vi bygger nu vidare på exempelprojektet med tre specialiserade assistenter.

### 1. Trendspanaren

Trendspanaren hjälper till att undersöka utveckling inom ett öppet område.

Exempel på uppgifter:

- hitta teman i en samling artiklar
- sammanfatta återkommande signaler
- skilja mellan tydliga trender och enstaka observationer
- föreslå frågor för vidare research

Trendspanaren ska inte försöka förutsäga framtiden med säkerhet. Den ska hjälpa användaren att se mönster och formulera osäkerheter.

### 2. Produktjämföraren

Produktjämföraren arbetar med strukturerade jämförelser.

Exempel på uppgifter:

- jämföra verktyg, tjänster eller metoder
- skapa kriterier
- väga fördelar och nackdelar
- markera saknad information
- skapa en beslutstabell

Produktjämföraren passar särskilt bra när användaren har öppna produktbeskrivningar, dokumentation, prislistor eller sammanfattningar som underlag.

### 3. Källkritikern

Källkritikern granskar underlaget.

Exempel på uppgifter:

- kontrollera om källorna är tillräckliga
- skilja mellan primärkällor och andrahandskällor
- identifiera marknadsföringsspråk
- markera påståenden som behöver verifieras
- föreslå bättre källor att leta efter

Källkritikern ska inte avgöra sanningen ensam. Den ska hjälpa användaren att upptäcka var underlaget är starkt, svagt eller ofullständigt.

## En återanvändbar mall för specialiserade assistenter

En **återanvändbar mall** är en struktur som du kan använda varje gång du skapar en ny GPT. Den gör att du inte behöver börja från noll.

Här är en enkel mall:

```text
Namn:
[Assistentens namn]

Syfte:
[Vilken återkommande uppgift assistenten ska hjälpa till med]

Målgrupp:
[Vem som ska använda assistenten]

Ska hjälpa till med:
- [Uppgift 1]
- [Uppgift 2]
- [Uppgift 3]

Ska inte göra:
- [Avgränsning 1]
- [Avgränsning 2]
- [Avgränsning 3]

Arbetssätt:
1. Be om saknat underlag om uppgiften är oklar.
2. Strukturera underlaget.
3. Markera osäkerheter.
4. Ge ett tydligt resultat i bestämt format.
5. Föreslå nästa steg för verifiering eller fördjupning.

Outputformat:
[Beskriv tabell, punktlista, rapportmall eller annan struktur]

Säkerhets- och kvalitetsregler:
- Använd inte känslig information.
- Skilj mellan fakta, tolkning och osäkerhet.
- Säg när underlaget inte räcker.
- Rekommendera verifiering mot aktuella källor när information kan förändras.
```

Mallen kan användas för både enkla och mer avancerade GPT:er. Den viktigaste delen är inte att den är lång. Det viktiga är att den gör assistentens uppdrag tydligt.

## Exempel: instruktion för Trendspanaren

Här är ett utkast till en instruktion för en specialiserad GPT.

```text
Du är Trendspanaren, en AI-assistent som hjälper användaren att analysera öppen information för att hitta möjliga trender, återkommande teman och frågor för vidare research.

Du arbetar endast med information som användaren delar i chatten eller med öppet, kontrollerbart underlag. Du ska inte be om känslig intern information, personuppgifter eller hemliga dokument.

Ditt arbetssätt:
1. Klargör ämnet och syftet med trendspaningen.
2. Fråga efter underlag om det saknas.
3. Identifiera återkommande teman.
4. Skilj mellan tydliga mönster, svaga signaler och osäkra observationer.
5. Föreslå frågor för fortsatt research.

Du ska inte:
- presentera spekulationer som fakta
- ge säkra framtidsprognoser
- hitta på källor
- dra långtgående slutsatser från för lite underlag

Svara normalt med följande struktur:
1. Kort sammanfattning
2. Möjliga trender
3. Svaga signaler
4. Osäkerheter
5. Frågor för vidare research
```

Den här instruktionen är avgränsad. Den säger inte att assistenten ska lösa alla analysproblem. Den har en tydlig roll.

## Exempel: instruktion för Källkritikern

Källkritikern behöver en annan ton och ett annat arbetssätt.

```text
Du är Källkritikern, en AI-assistent som hjälper användaren att granska öppet källmaterial för research och produktjämförelser.

Din uppgift är att bedöma underlagets kvalitet, inte att avgöra alla sakfrågor själv.

Granska underlaget utifrån:
- typ av källa
- aktualitet
- tydlighet
- möjlig partiskhet
- vad som stöds av källan
- vad som saknar stöd
- vad som behöver verifieras

Du ska vara försiktig med säkra slutsatser. När information saknas ska du säga det tydligt.

Svara med:
1. Underlagets styrkor
2. Underlagets svagheter
3. Påståenden som verkar väl stödda
4. Påståenden som behöver verifieras
5. Förslag på bättre eller kompletterande källor
```

Lägg märke till att Källkritikern inte ska skriva den färdiga rapporten. Den ska granska underlaget. Det är dess rollgräns.

## Hur specialiserade assistenter kan användas tillsammans

Du kan använda assistenterna i en enkel kedja.

Anta att du vill jämföra tre AI-verktyg för att skapa presentationer.

Ett möjligt arbetsflöde:

1. **AI-Analytikern** hjälper dig formulera frågan:
   - “Vilka kriterier är viktiga när jag jämför AI-verktyg för presentationer?”

2. **Produktjämföraren** skapar en jämförelsetabell:
   - funktioner
   - användarvänlighet
   - exportformat
   - prisuppgifter att verifiera
   - osäkerheter

3. **Källkritikern** granskar underlaget:
   - vilka uppgifter kommer från produktens egen webbplats?
   - vilka uppgifter behöver oberoende bekräftelse?
   - är informationen aktuell?

4. **AI-Analytikern** sammanfattar resultatet:
   - vad verkar tydligt?
   - vad bör kontrolleras?
   - vilket nästa steg är rimligt?

Det här är ett manuellt arbetsflöde, men det liknar hur mer avancerade AI-system ofta byggs: flera tydliga steg i stället för ett enda otydligt steg.

## Vanliga misstag

- **Misstag:** att skapa för många assistenter för tidigt
    - Det kan kännas lockande att skapa tio GPT:er direkt. Men fler assistenter betyder också mer underhåll.
    - Börja med en huvudassistent och en eller två specialiserade assistenter. Lägg bara till fler när du märker att en uppgift återkommer ofta.

- **Misstag:** att ge olika assistenter nästan samma uppdrag
    - Om två GPT:er gör nästan samma sak blir det svårt att veta vilken du ska använda.
    - Exempel:
    - Researchassistent
    - Analysassistent
    - Informationsassistent
    - Dessa namn säger för lite. Gör i stället rollerna tydligare:
    - Trendspanaren
    - Produktjämföraren
    - Källkritikern

- **Misstag:** att glömma outputformatet
    - En specialiserad assistent blir mycket mer användbar när den alltid lämnar ifrån sig resultat i en förväntad struktur.
    - Utan outputformat får du ofta varierande svar. Med outputformat kan du lättare jämföra resultat över tid.

- **Misstag:** att låta assistenten fatta beslut åt dig
    - En assistent kan hjälpa dig analysera. Den kan föreslå. Den kan visa osäkerheter. Men du bör inte låta den ersätta ditt eget omdöme, särskilt inte när informationen är aktuell, ekonomisk, juridisk, medicinsk eller strategiskt viktig.

## Övningar

### Övning 1: Dela upp AI-Analytikern

Skriv ner tre uppgifter som AI-Analytikern kan hjälpa dig med.

Exempel:

- jämföra produkter
- sammanfatta artiklar
- granska källor

Välj sedan en av uppgifterna och gör den till en specialiserad assistent.

Beskriv:

- namn
- syfte
- vad assistenten ska göra
- vad assistenten inte ska göra
- vilket outputformat den ska använda

### Övning 2: Skriv en rollgräns

Välj en av dessa roller:

- Trendspanaren
- Produktjämföraren
- Källkritikern
- Rapportbyggaren

Skriv en rollgräns med fyra delar:

1. Ska göra
2. Ska inte göra
3. Behöver som underlag
4. Lämnar ifrån sig

Målet är att assistenten ska bli lättare att förstå och testa.

### Övning 3: Skapa en återanvändbar mall

Utgå från mallen i kapitlet och skapa din egen version. Anpassa den till hur du själv vill bygga GPT:er.

Din mall bör minst innehålla:

- namn
- syfte
- målgrupp
- uppgifter
- avgränsningar
- arbetssätt
- outputformat
- kvalitetsregler

Spara mallen så att du kan återanvända den i senare kapitel.

### Fördjupning: Skapa ett litet analysteam

Skapa tre tänkta GPT:er som tillsammans löser ett researchproblem med öppen information.

Exempel:

- en som samlar frågor
- en som jämför alternativ
- en som granskar osäkerheter

Beskriv i vilken ordning de ska användas och vad varje assistent lämnar vidare till nästa steg.

## Snabb sammanfattning

- En bred assistent är enkel att starta med, men kan bli otydlig när uppgifterna växer.
- Specialisering betyder att en assistent får ett tydligt och avgränsat uppdrag.
- En rollgräns beskriver vad assistenten ska göra, inte ska göra, behöver som underlag och lämnar ifrån sig.
- En återanvändbar mall gör det lättare att skapa nya GPT:er med konsekvent kvalitet.
- AI-Analytikern kan utvecklas till ett litet team med Trendspanaren, Produktjämföraren och Källkritikern.
- Specialiserade assistenter blir lättare att testa, förbättra och använda i arbetsflöden.

## Nästa steg

Nu har du lärt dig att dela upp ett större assistentbehov i tydliga roller. Nästa kapitel handlar om testning och förbättring: hur du kontrollerar om en assistent faktiskt fungerar, hur du upptäcker svaga instruktioner och hur du förbättrar en GPT steg för steg.
