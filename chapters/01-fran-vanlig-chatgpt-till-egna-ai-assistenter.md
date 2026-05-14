# Kapitel 1: Från vanlig ChatGPT till egna AI-assistenter

## Varför detta kapitel finns

Många börjar med ChatGPT genom att skriva en fråga, läsa svaret och sedan ställa en följdfråga. Det är ett bra sätt att komma igång. Men när du återkommer till samma typ av uppgift flera gånger märker du snart en begränsning: du måste förklara samma sak om och om igen.

En egen AI-assistent löser en del av det problemet. I stället för att börja från noll varje gång skapar du en assistent med ett tydligt uppdrag, ett arbetssätt och vissa regler.

I det här kapitlet ska vi reda ut skillnaden mellan vanlig ChatGPT-användning och en mer genomtänkt AI-assistent.

## Lärandemål

Efter kapitlet ska du kunna:
- förklara vad en AI-assistent är
- beskriva vad en egen GPT är på en grundläggande nivå
- förstå skillnaden mellan en enskild chatt och ett återanvändbart arbetsflöde
- skissa första versionen av bokens exempelprojekt, AI-Analytikern

## Innan vi börjar

Du behöver bara ha använt ChatGPT tidigare. Du behöver inte ha skapat en GPT, laddat upp filer eller arbetat med några avancerade inställningar.

Vi börjar med tre begrepp:

**AI-assistent** betyder i den här boken en AI som är utformad för att hjälpa till med en återkommande uppgift eller roll.

**GPT** betyder en anpassad assistent i ChatGPT. En GPT kan ha egna instruktioner och ibland även kunskapsfiler eller särskilda funktioner.

**Arbetsflöde** betyder en ordnad serie steg som leder från ett behov till ett resultat.

## Vanlig chatt jämfört med AI-assistent

En vanlig chatt fungerar ofta så här:

1. Du skriver en fråga.
2. ChatGPT svarar.
3. Du förtydligar.
4. ChatGPT svarar igen.
5. Du justerar tills svaret blir användbart.

Det kan fungera utmärkt för tillfälliga frågor. Men om du ofta gör samma typ av arbete blir det ineffektivt.

Tänk dig att du varje vecka vill sammanfatta nyheter inom ett område, jämföra nya produkter eller skapa en kort trendrapport. Då behöver du kanske varje gång förklara:

- vilken roll ChatGPT ska ta
- vilken typ av källor du vill använda
- hur svaret ska struktureras
- vilken nivå svaret ska ligga på
- vad AI:n inte ska göra
- hur osäkerhet ska markeras

En AI-assistent låter dig samla sådana instruktioner på ett mer återanvändbart sätt.

## En enkel analogi

En vanlig chatt är som att be en kunnig kollega om hjälp i korridoren. Det går snabbt, men du behöver ge sammanhanget där och då.

En AI-assistent är mer som att skapa en arbetsbeskrivning för en återkommande roll. Personen, eller i det här fallet AI:n, vet redan vilket uppdrag den har, vilken ton den ska använda och vilken typ av resultat du förväntar dig.

Det betyder inte att assistenten alltid har rätt. Det betyder bara att starten blir tydligare.

## Exempel: AI-Analytikern

I den här boken bygger vi ett genomgående exempelprojekt som heter **AI-Analytikern**.

AI-Analytikern ska hjälpa till med öppen information. Den ska inte hantera hemliga dokument, interna kundlistor, personuppgifter eller känsliga beslut. Den ska i stället arbeta med sådant som går att kontrollera och dela.

Ett första enkelt uppdrag kan vara:

> Du är AI-Analytikern, en assistent som hjälper användaren att strukturera öppen information om produkter, trender och marknader. Du ska sammanfatta material tydligt, skilja mellan fakta och antaganden och föreslå vad användaren bör kontrollera vidare.

Det här är inte en färdig GPT-instruktion. Det är bara en första skiss. Men redan nu ser vi flera viktiga delar:

- assistenten har en roll
- den har ett ämnesområde
- den har en metod
- den har en begränsning
- den ska hjälpa användaren att kontrollera information

## Varför öppen information är ett bra startområde

När du lär dig skapa AI-assistenter är det klokt att börja med uppgifter som inte kräver känslig information.

Öppen information kan till exempel vara:
- offentliga webbsidor
- produktbeskrivningar
- pressmeddelanden
- hjälptexter
- öppna rapporter
- egna icke-känsliga anteckningar
- publika jämförelser och sammanställningar

Det gör övningarna säkrare. Du kan experimentera, göra fel, förbättra instruktioner och dela exempel utan att riskera att exponera något som inte borde delas.

Det betyder inte att all öppen information är korrekt. Tvärtom är källkritik fortfarande nödvändigt. Men riskerna blir lättare att hantera medan du lär dig.

## Vad gör en assistent användbar?

En AI-assistent blir användbar när den har ett tydligt syfte. Ett vanligt nybörjarmisstag är att försöka skapa en assistent som kan allt.

En assistent som ska “hjälpa mig med jobbet” blir ofta för bred. En assistent som ska “jämföra öppna produktbeskrivningar och sammanfatta skillnader i en tabell” är mycket lättare att styra.

Jämför dessa två uppdrag:

**För brett:**

> Hjälp mig med research.

**Tydligare:**

> Hjälp mig jämföra tre publika produktbeskrivningar. Sammanfatta målgrupp, viktigaste funktioner, prisinformation om den finns, tydliga skillnader och frågor jag bör undersöka vidare.

Det andra uppdraget ger AI:n ett tydligare arbete. Det gör också resultatet lättare att bedöma.

## Arbetsflöde: från fråga till resultat

Ett arbetsflöde är en serie steg. För AI-Analytikern kan ett enkelt arbetsflöde se ut så här:

1. Användaren beskriver vad som ska undersökas.
2. Assistenten frågar efter avgränsning om uppgiften är otydlig.
3. Assistenten sammanfattar informationen.
4. Assistenten markerar vad som är fakta, antaganden och osäkra punkter.
5. Assistenten föreslår nästa kontrollfrågor.
6. Användaren avgör vad som ska göras vidare.

Det här är viktigt: AI-assistenten ska inte bara ge ett snabbt svar. Den ska hjälpa användaren genom ett återkommande arbetssätt.

## Första skissen av AI-Analytikern

Nu skissar vi den första versionen. Den behöver inte vara perfekt.

### Namn
AI-Analytikern

### Syfte
Hjälpa användaren att strukturera och jämföra öppen information.

### Typiska uppgifter
- sammanfatta en produktbeskrivning
- jämföra två eller tre alternativ
- identifiera frågor som behöver kontrolleras
- skapa en enkel researchöversikt
- föreslå struktur för en rapport

### Ska inte göra
- hantera känslig information
- låtsas vara säker när information saknas
- fatta beslut åt användaren
- ersätta källkontroll

### Önskat svarssätt
- tydliga rubriker
- kort sammanfattning först
- tabeller när jämförelser behövs
- osäkerheter markerade
- förslag på nästa steg

Det här är grunden vi kommer att bygga vidare på i kommande kapitel.

## Vanliga misstag

- **Misstag:** assistenten får ett för brett uppdrag
    - **Varför det händer:** Det är lockande att vilja skapa en assistent som klarar allt.
    - **Hur man undviker det:** Börja med en återkommande uppgift. Gör assistenten bra på den innan du lägger till mer.

- **Misstag:** man blandar in känslig information för tidigt
    - **Varför det händer:** Många vill direkt använda AI i verkliga arbetsuppgifter.
    - **Hur man undviker det:** Börja med öppen information och ofarliga exempel. Lägg till känsligare användning först när du förstår riskerna och reglerna.

- **Misstag:** man litar för mycket på första svaret
    - **Varför det händer:** AI-svar kan låta säkra även när de innehåller fel.
    - **Hur man undviker det:** Be assistenten markera osäkerheter och kontrollera viktiga fakta mot källor.

## Övningar

### Övning 1: Välj ett öppet researchområde

Välj ett område där du kan använda öppen information. Det kan vara:
- AI-verktyg för skrivande
- projektverktyg
- elcyklar
- bokföringsprogram
- digitala utbildningsplattformar
- trender inom en bransch
- jämförelse av appar eller tjänster

Skriv tre meningar:
1. Vad vill du undersöka?
2. Varför är området intressant?
3. Vilken typ av resultat vill du få?

### Övning 2: Skissa din egen AI-Analytiker

Fyll i följande mall:

```text
Namn på assistenten:
Syfte:
Typiska uppgifter:
Ska inte göra:
Önskat svarssätt:
```

Håll det enkelt. Målet är inte att skriva perfekta instruktioner än. Målet är att förstå uppdraget.

### Övning 3: Gör uppdraget smalare

Skriv först ett brett uppdrag, till exempel:

```text
Hjälp mig med research om AI-verktyg.
```

Skriv sedan en smalare version:

```text
Hjälp mig jämföra tre AI-verktyg för mötessammanfattningar utifrån målgrupp, funktioner, integrationsmöjligheter, prisinformation och frågor som behöver kontrolleras.
```

Gör samma sak för ditt eget område.

## Snabb sammanfattning

- En vanlig chatt passar bra för tillfälliga frågor.
- En AI-assistent passar bättre för återkommande uppgifter.
- En GPT är en anpassad assistent i ChatGPT.
- Ett arbetsflöde beskriver stegen från behov till resultat.
- Bokens exempelprojekt, AI-Analytikern, använder öppen information för att minska riskerna.
- En bra assistent börjar med ett tydligt och avgränsat uppdrag.

## Nästa steg

I nästa kapitel bygger vi den första enkla versionen av AI-Analytikern som en egen GPT. Då går vi från idé och skiss till något du faktiskt kan testa.
