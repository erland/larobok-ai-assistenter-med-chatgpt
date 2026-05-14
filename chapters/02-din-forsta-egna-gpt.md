# Kapitel 2: Din första egna GPT

## Varför detta kapitel finns

I kapitel 1 skissade vi idén bakom **AI-Analytikern**: en assistent som hjälper dig arbeta med öppen information, till exempel produktjämförelser, trendspaning och omvärldsbevakning.

Nu ska du göra idén mer konkret genom att bygga den första versionen av en egen GPT.

Målet är inte att skapa en perfekt assistent direkt. Målet är att förstå byggstenarna: vad assistenten ska göra, vilka instruktioner den behöver och hur du testar om den beter sig som du tänkt.

Gränssnitt och knappar i ChatGPT kan förändras över tid. Därför fokuserar det här kapitlet på arbetssättet snarare än på exakta knappnamn.

## Lärandemål

Efter kapitlet ska du kunna:
- förklara vad GPT Builder används till
- skapa en första enkel GPT med ett tydligt uppdrag
- skriva grundläggande instruktioner för AI-Analytikern
- lägga till startfrågor som hjälper användaren komma igång
- testa om din GPT följer sitt uppdrag

## Innan vi börjar

Du behöver:
- ett ChatGPT-konto med tillgång till att skapa GPT:er
- ett tydligt men enkelt användningsområde
- ett ämne som bygger på öppen information

I det här kapitlet använder vi ett återkommande exempel:

> AI-Analytikern ska hjälpa användaren att jämföra produkter, tjänster eller verktyg utifrån öppet tillgänglig information.

Vi använder alltså inte:
- interna företagsdokument
- kundlistor
- personuppgifter
- sekretessbelagd information
- känsliga beslut där AI:n ensam får avgöra resultatet

Det är en viktig vana redan från början: bygg assistenter som är användbara, men också rimligt avgränsade.

## Tre nya begrepp

I det här kapitlet använder vi tre huvudbegrepp.

**GPT Builder** är verktyget i ChatGPT där du skapar och ändrar en egen GPT.

**Instruktioner** är texten som beskriver hur din GPT ska bete sig. Instruktionerna kan handla om roll, uppdrag, ton, arbetsmetod, begränsningar och svarens struktur.

**Startfrågor** är förslag på frågor eller uppgifter som visas för användaren. De hjälper användaren förstå vad GPT:n kan användas till.

## Steg 1: Bestäm assistentens uppdrag

En vanlig nybörjarfälla är att börja bygga innan man vet vad assistenten ska vara bra på.

Skriv därför först en enkel uppdragsmening.

För AI-Analytikern kan den se ut så här:

> AI-Analytikern hjälper användaren att strukturera och jämföra öppen information om produkter, tjänster och trender.

Det är kort, men tillräckligt tydligt för en första version.

Jämför med en för bred formulering:

> AI-Analytikern hjälper till med allt som rör analys.

Den andra formuleringen låter kraftfull, men den är svår att styra. En assistent som ska göra “allt” får ofta otydliga svar. En assistent som har ett avgränsat uppdrag blir lättare att testa och förbättra.

## Steg 2: Formulera en första instruktion

Nu behöver assistenten få sina grundinstruktioner.

En första version kan vara:

```text
Du är AI-Analytikern, en pedagogisk och noggrann GPT som hjälper användaren att analysera öppen information.

Ditt huvuduppdrag är att hjälpa användaren med produktjämförelser, omvärldsbevakning och trendspaning.

Du ska:
- strukturera information tydligt
- skilja mellan fakta, antaganden och osäkerheter
- föreslå jämförelsekriterier när användaren inte har några
- be om förtydligande när uppgiften är för bred
- påminna användaren om att kontrollera aktuella fakta i källor

Du ska inte:
- be användaren ladda upp känslig information
- behandla personuppgifter
- låtsas ha verifierat fakta som du inte har kontrollerat
- fatta beslut åt användaren utan att visa osäkerheter och alternativ

Svara på svenska, med tydliga rubriker och korta stycken.
```

Det här är inte den slutliga instruktionen för hela boken. Den är en fungerande start.

Lägg märke till strukturen:
- först roll
- sedan huvuduppdrag
- sedan vad assistenten ska göra
- sedan vad assistenten inte ska göra
- till sist form och språk

Den strukturen gör instruktionen lättare att läsa och förbättra.

## Steg 3: Skapa GPT:n i GPT Builder

Öppna funktionen för att skapa en GPT i ChatGPT. Eftersom gränssnitt kan ändras bör du tänka i dessa moment snarare än exakta knappnamn:

1. Starta skapandet av en ny GPT.
2. Ge den namnet **AI-Analytikern**.
3. Lägg in en kort beskrivning, till exempel:
   > Hjälper till med öppen research, produktjämförelser och trendspaning.
4. Klistra in instruktionen från föregående avsnitt.
5. Lägg till några startfrågor.
6. Spara GPT:n privat medan du testar den.

Första versionen bör vara privat. Då kan du experimentera utan att behöva tänka på publicering, delning eller hur andra användare tolkar assistenten.

## Steg 4: Lägg till startfrågor

Startfrågor hjälper användaren komma igång. De fungerar som exempel på vad assistenten är byggd för.

För AI-Analytikern kan du använda dessa:

```text
Hjälp mig jämföra tre öppet beskrivna AI-verktyg.
```

```text
Skapa en jämförelsemall för två produkter jag vill undersöka.
```

```text
Hjälp mig strukturera en omvärldsbevakning inom ett ämne.
```

```text
Vilka frågor bör jag ställa innan jag litar på en produktjämförelse?
```

Bra startfrågor är konkreta. De ska inte försöka visa allt assistenten kan göra. De ska visa typiska startpunkter.

## Steg 5: Testa med en enkel uppgift

Nu är det dags att prova GPT:n.

Använd en uppgift som inte kräver känslig information:

```text
Jag vill jämföra tre typer av verktyg för AI-baserad mötessammanfattning. Hjälp mig skapa jämförelsekriterier innan jag börjar samla in information.
```

Ett bra svar från AI-Analytikern bör:
- föreslå relevanta kriterier
- inte hitta på specifika produktfakta
- förklara vad som behöver kontrolleras
- ge en tydlig struktur
- gärna föreslå nästa steg

Exempel på jämförelsekriterier:
- pris och licensmodell
- språkstöd
- dataskydd och integritet
- integrationer
- sammanfattningskvalitet
- exportmöjligheter
- användarvänlighet
- begränsningar och risker

Här ser du en viktig princip: assistenten behöver inte börja med att ge svar på allt. Den kan börja med att hjälpa dig ställa bättre frågor.

## Exempel: ett första bra svarsmönster

Ett användbart svar från AI-Analytikern kan ha den här formen:

```text
Här är ett förslag på jämförelsestruktur.

1. Syfte
Vad ska verktyget hjälpa dig med?

2. Jämförelsekriterier
- Funktioner
- Pris
- Språkstöd
- Integritet
- Integrationer
- Begränsningar

3. Information som behöver kontrolleras
- Aktuella priser
- Villkor för datalagring
- Vilka plattformar som stöds
- Om funktionerna ingår i den valda planen

4. Nästa steg
Samla in öppna källor från varje leverantör och fyll i en enkel tabell.
```

Det här är inte spektakulärt. Men det är stabilt, kontrollerbart och lätt att bygga vidare på. För en första GPT är det viktigare än att den verkar avancerad.

## Vanliga misstag

- **Misstag:** att göra assistenten för bred
    - **Varför det händer:** Det är lockande att skriva att assistenten ska hjälpa till med “analys, strategi, research, skrivande, planering och allt annat”.
    - **Hur du undviker det:** Börja med ett tydligt huvuduppdrag. Du kan alltid bredda senare.

- **Misstag:** att sakna begränsningar
    - **Varför det händer:** Många instruktioner beskriver bara vad assistenten ska göra, inte vad den ska undvika.
    - **Hur du undviker det:** Lägg alltid till en kort “ska inte”-del. För AI-Analytikern handlar det särskilt om känslig information, personuppgifter och overifierade fakta.

- **Misstag:** att testa med för svår uppgift direkt
    - **Varför det händer:** Man vill se vad assistenten klarar och börjar med en komplex verklig fråga.
    - **Hur du undviker det:** Börja med ett litet test. Kontrollera först om assistenten följer sin roll och svarar i rätt format.

- **Misstag:** att tro att första versionen ska vara färdig
    - **Varför det händer:** En GPT känns som en produkt, och därför vill man göra den komplett från början.
    - **Hur du undviker det:** Se första versionen som en prototyp. Den ska vara tillräckligt bra för att testas, inte perfekt.

## Övningar

### Övning 1: Skapa första versionen av AI-Analytikern

Skapa en ny GPT med:
- namnet **AI-Analytikern**
- en kort beskrivning
- grundinstruktionen från kapitlet
- minst tre startfrågor

Spara den privat.

### Övning 2: Testa om uppdraget är tydligt

Ställ denna fråga till din GPT:

```text
Vad är du bäst på att hjälpa mig med, och vad bör jag inte använda dig till?
```

Bedöm svaret:
- Är uppdraget tydligt?
- Nämner GPT:n öppen information?
- Varnar den för känslig information?
- Svarar den på svenska?
- Är svaret lätt att förstå?

### Övning 3: Gör ett första produktjämförelsetest

Använd denna prompt:

```text
Jag vill jämföra tre verktyg inom ett område, men jag har inte valt verktygen än. Hjälp mig skapa en jämförelsemall och en plan för hur jag samlar in öppen information.
```

Spara svaret. Du kommer kunna använda det senare när vi förbättrar instruktionerna.

### Fördjupning: Skriv en egen variant

Skriv om uppdraget så att AI-Analytikern passar ett ämne du själv bryr dig om, till exempel:
- utbildningsteknik
- hållbarhetsrapporter
- produktivitetsverktyg
- offentliga rapporter
- konsumentprodukter
- branschtrender

Behåll regeln att assistenten ska arbeta med öppen information.

## Snabb sammanfattning

I det här kapitlet har du:
- skapat första versionen av AI-Analytikern
- lärt dig vad GPT Builder används till
- skrivit en enkel men tydlig instruktion
- lagt till startfrågor
- testat assistenten med en säker och avgränsad uppgift

Den viktigaste lärdomen är att en bra GPT börjar med ett tydligt uppdrag. Det är bättre att bygga en liten assistent som fungerar än en stor assistent som är oklar.

## Nästa steg

I nästa kapitel går vi djupare in i instruktioner. Då förbättrar vi AI-Analytikern så att den får tydligare roll, bättre arbetsmetod och mer konsekventa svar.
