# Kapitel 5: Produktjämförelser med AI-Analytikern

## Varför detta kapitel finns

AI-Analytikern har nu en tydlig roll, bättre instruktioner och en liten öppen kunskapsbas. I det här kapitlet använder vi allt detta för en praktisk uppgift: att jämföra produkter, tjänster eller verktyg på ett mer strukturerat sätt.

Produktjämförelser är ett bra övningsområde eftersom de ofta bygger på öppen information. Du kan jämföra publika produktsidor, hjälptexter, prisinformation, funktionslistor, recensioner eller dokumentation. Samtidigt tränar du på något viktigt: att skilja mellan fakta, tolkning och osäkerhet.

Målet är inte att låta AI-Analytikern “välja åt dig”. Målet är att låta den hjälpa dig göra jämförelsen tydligare, mer spårbar och lättare att granska.

## Lärandemål

Efter kapitlet ska du kunna:

- formulera tydliga jämförelsekriterier innan du ber AI:n jämföra något
- använda en beslutstabell för att strukturera produktjämförelser
- skilja mellan fakta, bedömningar och osäkerheter
- förbättra AI-Analytikern så att den inte låter säkrare än den bör
- skapa en återanvändbar mall för egna produktjämförelser

## Innan vi börjar

Vi bygger vidare på tidigare begrepp:

- **Instruktion:** styr hur AI-Analytikern ska arbeta.
- **Kunskapsfil:** ger stödmaterial, till exempel en jämförelsemall.
- **Källmaterial:** den information som används som underlag för jämförelsen.
- **Outputformat:** bestämmer hur svaret ska presenteras.

I det här kapitlet introduceras tre nya huvudbegrepp:

- **Jämförelsekriterier:** de frågor eller egenskaper som produkterna ska bedömas mot.
- **Beslutstabell:** en tabell som hjälper dig se skillnader, styrkor, svagheter och osäkerheter.
- **Osäkerhet:** sådant som inte går att avgöra säkert från tillgängligt underlag.

## Börja inte med produkterna, börja med beslutet

Ett vanligt misstag är att börja med frågan:

> Vilket verktyg är bäst?

Det är nästan alltid för otydligt. Bäst för vem? För vilket arbete? Med vilken budget? För en nybörjare eller en expert? För en ensam person eller ett team?

En bättre fråga är:

> Vilket av dessa verktyg passar bäst för en person som vill bevaka öppna källor, sammanfatta artiklar och skapa enkla jämförelser utan programmering?

Nu finns ett sammanhang. AI-Analytikern kan då jämföra utifrån ett faktiskt behov, inte utifrån en allmän popularitetstävling.

Innan du ber assistenten jämföra något bör du därför skriva tre saker:

1. vad du försöker välja mellan
2. vem valet gäller
3. vilka kriterier som betyder mest

## Jämförelsekriterier

Jämförelsekriterier är de egenskaper du vill bedöma. För AI-verktyg kan kriterierna till exempel vara:

- användarvänlighet
- pris eller prisnivå
- stöd för svenska
- möjlighet att spara arbetsflöden
- stöd för filer
- stöd för webbsökning eller externa källor
- exportmöjligheter
- lämplighet för nybörjare
- risker eller begränsningar
- dokumentation och support

Alla kriterier är inte lika viktiga. Om du bygger en assistent för omvärldsbevakning är källhantering viktigare än design. Om du bygger en assistent för snabba idéer är enkelhet kanske viktigare än avancerade inställningar.

Ett bra första steg är därför att dela upp kriterierna i tre grupper:

| Grupp | Betydelse | Exempel |
|---|---|---|
| Måste finnas | Krav som inte kan kompromissas bort | Fungerar utan programmering |
| Viktigt | Påverkar beslutet tydligt | Kan hantera källor och sammanfattningar |
| Bonus | Bra om det finns, men inte avgörande | Snygg export eller många mallar |

Detta gör jämförelsen mer rättvis. En produkt ska inte vinna bara för att den har många funktioner. Den ska passa behovet.

## En första prompt för produktjämförelse

Här är en enkel prompt du kan använda med AI-Analytikern:

```text
Jag vill jämföra tre verktyg för omvärldsbevakning och research.

Målgrupp:
En van ChatGPT-användare som inte programmerar.

Uppgift:
Jämför verktygen utifrån öppet tillgänglig information som jag klistrar in eller sammanfattar.

Kriterier:
1. Enkelhet för nybörjare
2. Stöd för att arbeta med källor
3. Möjlighet att skapa återanvändbara arbetsflöden
4. Kostnads- eller prisnivå, om informationen finns
5. Risker, begränsningar och osäkerheter

Svara med:
- kort sammanfattning
- beslutstabell
- tydliga osäkerheter
- rekommendation för olika användartyper

Viktigt:
Gissa inte fakta. Markera sådant som behöver kontrolleras.
```

Lägg märke till att prompten inte säger “sök upp allt själv”. Den säger att assistenten ska arbeta med information som du tillhandahåller eller som är öppet kontrollerbar. Det gör övningen säkrare och mer pedagogisk.

## Beslutstabellen

En beslutstabell är ett sätt att göra jämförelsen överblickbar. Den kan se ut så här:

| Kriterium | Verktyg A | Verktyg B | Verktyg C | Kommentar/osäkerhet |
|---|---|---|---|---|
| Enkelhet | Hög | Medel | Hög | Bygger på produktbeskrivningar, bör testas praktiskt |
| Källhantering | Medel | Hög | Låg | Oklart om alla funktioner ingår i billigaste planen |
| Återanvändbara flöden | Hög | Medel | Medel | Kräver kontroll i aktuell version |
| Prisnivå | Oklar | Hög | Låg | Priser kan ändras |
| Passar nybörjare | Ja | Delvis | Ja | Beror på hur mycket stöd användaren behöver |

Det viktiga är inte att tabellen är perfekt. Det viktiga är att den synliggör vad jämförelsen bygger på.

En bra beslutstabell gör tre saker:

1. visar skillnader mellan alternativen
2. visar varför en bedömning görs
3. visar vad som fortfarande är osäkert

## Fakta, bedömning och osäkerhet

När AI hjälper till med produktjämförelser blandas ofta tre typer av påståenden:

| Typ | Exempel | Hur du bör hantera det |
|---|---|---|
| Fakta | “Verktyget har en gratisplan enligt produktsidan.” | Kontrollera mot aktuell källa |
| Bedömning | “Verktyget verkar lätt för nybörjare.” | Testa eller jämför med egna behov |
| Osäkerhet | “Det är oklart om funktionen ingår i alla planer.” | Markera och undersök vidare |

AI-Analytikern ska tränas att skilja på dessa. Det är en av de viktigaste förbättringarna du kan göra.

Lägg därför till denna regel i instruktionerna:

```text
När du gör produktjämförelser ska du tydligt skilja mellan:
1. fakta som framgår av källmaterialet
2. bedömningar du gör utifrån källmaterialet
3. osäkerheter som användaren bör kontrollera själv
```

Det gör assistenten mer pålitlig, eftersom den inte försöker låta mer säker än underlaget tillåter.

## Förbättra AI-Analytikerns instruktioner

Nu kan vi uppdatera AI-Analytikern med ett nytt avsnitt i instruktionerna:

```text
Vid produktjämförelser ska du arbeta så här:

1. Börja med att fråga efter målgrupp, användningsfall och viktigaste kriterier om de saknas.
2. Använd bara den information som användaren ger dig eller som tydligt anges som kontrollerbar öppen information.
3. Skapa en beslutstabell med kriterier, alternativ och osäkerheter.
4. Skilj tydligt mellan fakta, bedömning och osäkerhet.
5. Ge inte en enda generell vinnare om olika alternativ passar olika behov.
6. Avsluta med vilka uppgifter användaren bör verifiera innan beslut.
```

Detta är ett exempel på hur en GPT växer genom boken. Vi gör inte om hela assistenten. Vi lägger till en tydlig förmåga.

## Exempel: jämförelse av tre researchverktyg

Anta att du vill jämföra tre typer av verktyg:

1. en egen GPT i ChatGPT
2. ett Project i ChatGPT
3. ett separat verktyg för automatiserad omvärldsbevakning

Frågan är inte vilket som är “bäst”. Frågan är vilket som passar olika behov.

AI-Analytikern kan då skapa en jämförelse som denna:

| Behov | Egen GPT | Project | Externt automationsverktyg |
|---|---|---|---|
| Återanvändbar assistent med tydlig roll | Stark | Medel | Varierar |
| Samla material kring ett större arbete | Medel | Stark | Varierar |
| Automatiska återkommande flöden | Svagare | Svagare | Starkare |
| Bra för nybörjare | Stark | Stark | Ofta mer avancerat |
| Kräver teknisk vana | Låg | Låg | Ofta medel |

En sådan tabell förbereder också senare kapitel. I kapitel 6 kommer vi att titta mer på när GPT:er inte räcker och när andra arbetssätt passar bättre. I kapitel 10 kommer vi tillbaka till automatisering utanför ChatGPT.

## Vanliga misstag

- **Misstag:** att låta AI välja utan kriterier
    - **Varför det händer:** Det känns snabbt och bekvämt att fråga “vilket är bäst?”.
    - **Hur du undviker det:** Bestäm först målgrupp, användningsfall och kriterier. Be sedan AI-Analytikern jämföra utifrån dem.

- **Misstag:** att blanda ihop fakta och bedömning
    - **Varför det händer:** AI kan formulera bedömningar med samma självsäkra ton som fakta.
    - **Hur du undviker det:** Kräv att assistenten markerar fakta, bedömning och osäkerhet separat.

- **Misstag:** att använda gamla prisuppgifter
    - **Varför det händer:** Priser, planer och funktioner ändras ofta.
    - **Hur du undviker det:** Be AI-Analytikern markera prisuppgifter som något som alltid ska kontrolleras mot aktuell produktsida.

- **Misstag:** att jämföra för många saker samtidigt
    - **Varför det händer:** Det är frestande att lägga in tio produkter och tjugo kriterier.
    - **Hur du undviker det:** Börja med tre alternativ och fem till sju kriterier. Utöka först när grundjämförelsen är begriplig.

## Övningar

### Övning 1: Skapa dina kriterier

Välj ett område där du vill jämföra tre produkter, tjänster eller verktyg. Det kan till exempel vara AI-verktyg, anteckningsappar, projekthanteringsverktyg eller nyhetsbrevstjänster.

Skriv:

- vilka tre alternativ du vill jämföra
- vem jämförelsen gäller
- tre krav som måste finnas
- tre viktiga kriterier
- två bonuskriterier

### Övning 2: Bygg en beslutstabell

Använd kriterierna från övning 1 och be AI-Analytikern skapa en tom beslutstabell.

Tabellen ska innehålla:

- kriterium
- alternativ A
- alternativ B
- alternativ C
- kommentar eller osäkerhet

Fyll sedan i tabellen med öppen information som du själv samlar in.

### Övning 3: Förbättra instruktionerna

Lägg till produktjämförelsereglerna i AI-Analytikerns instruktioner.

Testa sedan med denna prompt:

```text
Hjälp mig jämföra tre verktyg för att bevaka nyheter inom AI. Börja med att fråga mig efter målgrupp, användningsfall och kriterier innan du gör jämförelsen.
```

Kontrollera om assistenten ställer följdfrågor i stället för att börja gissa.

### Fördjupning: Skapa en jämförelsemall som kunskapsfil

Skapa ett kort dokument med rubriken “Mall för produktjämförelser”.

Ta med:

- syfte
- målgrupp
- användningsfall
- jämförelsekriterier
- beslutstabell
- osäkerheter
- rekommendation för olika användartyper
- uppgifter som bör verifieras

Ladda upp dokumentet som kunskapsfil till AI-Analytikern om du vill göra jämförelsearbetet mer återanvändbart.

## Snabb sammanfattning

- Produktjämförelser blir bättre när du börjar med beslutet, inte med produkterna.
- Jämförelsekriterier gör bedömningen tydligare och mer rättvis.
- En beslutstabell hjälper dig se skillnader, styrkor och osäkerheter.
- AI-Analytikern ska skilja mellan fakta, bedömningar och osäkerheter.
- Pris, funktioner och planer bör alltid kontrolleras mot aktuella källor.
- En bra AI-assistent hjälper dig tänka klarare, men den ska inte ersätta din egen granskning.

## Nästa steg

Nu har AI-Analytikern fått en tydligare praktisk användning: strukturerade produktjämförelser med öppen information. I nästa kapitel går vi vidare till en viktig fråga: när är en egen GPT rätt lösning, och när passar Projects, Custom Instructions eller en vanlig chatt bättre?
