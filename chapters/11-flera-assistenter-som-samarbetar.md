# Kapitel 11: Flera assistenter som samarbetar

## Varför detta kapitel finns

I de tidigare kapitlen har du byggt och förbättrat enskilda assistenter. Du har också sett att en assistent ofta blir bättre när den får en tydlig roll, tydliga gränser och ett tydligt outputformat.

Nästa steg är att inte försöka göra en enda GPT som gör allt.

När arbetsuppgiften blir större är det ofta bättre att dela upp arbetet i flera mindre steg. Varje steg kan skötas av en specialiserad assistent eller av samma assistent i olika roller. Det gör arbetet lättare att förstå, testa och förbättra.

I det här kapitlet bygger vi vidare på AI-Analytikern och skapar ett flöde där flera assistenter samarbetar:

1. **Researchassistenten** samlar och strukturerar öppet underlag.
2. **Produktjämföraren** jämför alternativ mot tydliga kriterier.
3. **Källkritikern** granskar underlaget och markerar osäkerheter.
4. **Rapportskrivaren** gör en kort och läsbar sammanfattning.

Det här är inte ett avancerat tekniskt agentsystem. Det är ett praktiskt arbetssätt som du kan använda direkt i ChatGPT, med egna GPT:er, Projects eller vanliga chattar.

## Lärandemål

Efter kapitlet ska läsaren kunna:

- förklara vad en pipeline är i ett AI-arbetsflöde
- beskriva vad en handoff är mellan två assistenter
- planera en enkel kedja av flera assistenter
- använda kvalitetskontroll som ett separat steg
- avgöra när flera assistenter är bättre än en enda bred assistent

## Innan vi börjar

Du har redan arbetat med:

- **Specialisering:** att ge en assistent en tydlig roll.
- **Rollgräns:** vad assistenten ska och inte ska göra.
- **Outputformat:** strukturen i assistentens svar.
- **Testfall:** kontrollerade uppgifter som visar om assistenten fungerar.
- **Automation:** ett flöde där vissa steg kan köras mer automatiskt.

I det här kapitlet introducerar vi tre nya huvudbegrepp:

- **Pipeline**
- **Handoff**
- **Kvalitetskontroll**

## Huvudförklaring

### Vad är en pipeline?

En **pipeline** är ett arbetsflöde där resultatet från ett steg används som underlag i nästa steg.

Ett vanligt exempel utanför AI är en redaktionell process:

1. någon samlar fakta
2. någon skriver ett utkast
3. någon granskar utkastet
4. någon publicerar slutversionen

Samma tänk fungerar för AI-assistenter.

För AI-Analytikern kan en enkel pipeline se ut så här:

1. Samla öppet underlag.
2. Sortera underlaget efter ämne.
3. Jämför alternativ.
4. Granska källor och osäkerheter.
5. Skriv en kort rapport.

Det viktiga är att varje steg har ett tydligt syfte. Om ett steg är otydligt blir nästa steg också svagare.

### Varför inte bara skapa en super-GPT?

Det kan kännas lockande att bygga en enda GPT som gör allt:

- hittar information
- analyserar information
- jämför produkter
- granskar källor
- skriver rapporter
- föreslår beslut

Problemet är att en sådan assistent ofta blir svår att styra. Den får för många mål samtidigt. Då blir det också svårare att veta varför resultatet blev bra eller dåligt.

En stor assistent kan fungera för enkla uppgifter, men vid mer krävande arbete är flera mindre roller ofta bättre.

Jämför:

**En bred assistent:**  
“Gör en produktjämförelse och skriv en rapport.”

**Flera assistenter i pipeline:**  
“Samla först underlag. Jämför sedan alternativen. Granska därefter osäkerheter. Skriv till sist en rapport.”

Den andra varianten ger dig fler kontrollpunkter.

### Vad är en handoff?

En **handoff** är överlämningen från ett steg till nästa.

I ett AI-arbetsflöde är handoffen ofta en text, en tabell, en lista eller en rapportmall. Den behöver vara tydlig nog för att nästa assistent ska förstå vad den ska göra.

En dålig handoff kan se ut så här:

> Här är lite information. Gör något bra av den.

En bättre handoff kan se ut så här:

> Här är tre produktalternativ, fem jämförelsekriterier och markerade osäkerheter. Jämför alternativen i en tabell och skilj mellan fakta, bedömning och sådant som behöver verifieras.

En bra handoff innehåller oftast:

- vad som redan är gjort
- vilket material som används
- vad nästa steg ska göra
- vilket format nästa steg ska lämna tillbaka
- vilka osäkerheter som redan är kända

### Kvalitetskontroll som eget steg

I många AI-arbetsflöden blandas analys och granskning ihop. Det gör att svagheter lätt missas.

Därför är det ofta bättre att lägga in **kvalitetskontroll** som ett eget steg.

Kvalitetskontroll betyder inte att AI:n garanterar att allt är sant. Det betyder att du gör en systematisk kontroll av resultatet innan du använder det.

För AI-Analytikern kan kvalitetskontroll handla om att kontrollera:

- om källor saknas
- om något låter mer säkert än underlaget tillåter
- om jämförelsekriterierna är rimliga
- om flera alternativ behandlas rättvist
- om aktuella uppgifter behöver verifieras
- om slutsatsen följer av underlaget

Kvalitetskontroll är särskilt viktig när du arbetar med öppen information. Offentliga källor kan vara gamla, vinklade, ofullständiga eller marknadsförande.

### Fyra roller i AI-Analytikerns arbetsflöde

Nu bygger vi en praktisk pipeline för AI-Analytikern.

#### Roll 1: Researchassistenten

Researchassistentens uppgift är att samla och strukturera underlag.

Den ska inte dra långtgående slutsatser. Den ska framför allt hjälpa dig att få ordning på materialet.

Exempel på instruktion:

```text
Du är Researchassistenten i AI-Analytikern.

Din uppgift är att strukturera öppet källmaterial inför en produktjämförelse.

Gör detta:
1. Lista vilka produkter eller tjänster som ska jämföras.
2. Sammanfatta relevant information från underlaget.
3. Markera vad som verkar vara fakta, marknadsföringspåståenden och oklara uppgifter.
4. Föreslå vilka uppgifter som behöver verifieras.

Gör inte detta:
- Hitta inte på information som saknas.
- Rekommendera inte en vinnare.
- Använd inte känslig eller intern information.
```

#### Roll 2: Produktjämföraren

Produktjämföraren använder det strukturerade underlaget och jämför alternativen mot kriterier.

Exempel på instruktion:

```text
Du är Produktjämföraren i AI-Analytikern.

Din uppgift är att jämföra produkter eller tjänster utifrån givna kriterier.

Använd bara underlaget som finns i handoffen. Om något saknas, skriv "behöver verifieras".

Svarformat:
- Kort sammanfattning
- Jämförelsetabell
- Styrkor per alternativ
- Svagheter per alternativ
- Frågor som återstår
```

#### Roll 3: Källkritikern

Källkritikern granskar jämförelsen.

Den ska inte skriva om allt. Den ska leta efter svagheter, överdriven säkerhet och luckor.

Exempel på instruktion:

```text
Du är Källkritikern i AI-Analytikern.

Din uppgift är att granska en produktjämförelse innan den används.

Kontrollera:
1. Finns det påståenden utan tydligt underlag?
2. Blandas fakta och bedömning ihop?
3. Finns aktuella uppgifter som bör verifieras?
4. Är något alternativ orättvist behandlat?
5. Är slutsatsen rimlig utifrån underlaget?

Svara med:
- Godkänt att använda / Behöver förbättras
- Viktigaste riskerna
- Konkreta förbättringsförslag
```

#### Roll 4: Rapportskrivaren

Rapportskrivaren tar den granskade jämförelsen och gör en läsbar rapport.

Den ska inte lägga till nya fakta. Den ska göra resultatet lättare att förstå.

Exempel på instruktion:

```text
Du är Rapportskrivaren i AI-Analytikern.

Din uppgift är att skriva en kort rapport baserad på en granskad produktjämförelse.

Rapporten ska innehålla:
1. Bakgrund
2. Jämförelsekriterier
3. Sammanfattning av alternativen
4. Viktiga osäkerheter
5. Rekommenderad nästa åtgärd

Lägg inte till nya fakta. Markera tydligt om något behöver verifieras.
```

## Exempel: Från research till rapport

Anta att du vill jämföra tre öppet beskrivna AI-verktyg för mötessammanfattningar. Du vill inte använda interna mötesanteckningar eller kunddata. Du arbetar bara med publik produktinformation, hjälptexter och öppna beskrivningar.

### Steg 1: Research

Du ber Researchassistenten strukturera underlaget.

Resultatet kan bli:

| Alternativ | Relevant information | Osäkerheter |
|---|---|---|
| Verktyg A | Har funktioner för transkribering och sammanfattning enligt offentlig produktbeskrivning | Pris och språkstöd behöver verifieras |
| Verktyg B | Betonar integrationer med kalender och videomöten | Exakta begränsningar per plan behöver verifieras |
| Verktyg C | Fokuserar på teamdelning och sökbara anteckningar | Databehandling och regioner behöver verifieras |

### Steg 2: Jämförelse

Produktjämföraren använder tabellen och jämför utifrån kriterier:

- språkstöd
- enkelhet
- integrationer
- exportmöjligheter
- tydlighet kring dataskydd
- kostnad

Resultatet blir inte en definitiv sanning. Det blir en strukturerad jämförelse med tydliga luckor.

### Steg 3: Källkritik

Källkritikern upptäcker kanske att:

- två prisuppgifter saknar datum
- ett verktyg bedöms som “enkelt” utan tydligt kriterium
- dataskydd jämförs för svagt
- slutsatsen låter mer säker än underlaget tillåter

Det är värdefullt. Målet är inte att få AI:n att verka säker. Målet är att få ett bättre beslutsunderlag.

### Steg 4: Rapport

Rapportskrivaren skapar en kort rapport som du kan använda som arbetsmaterial.

Den kan avslutas med:

> Rekommenderad nästa åtgärd: verifiera aktuella priser, dataskyddsinformation och språkstöd på respektive leverantörs officiella webbplats innan något beslut fattas.

Det är en bra AI-rapport: användbar, men inte överdrivet självsäker.

## När ska man använda flera assistenter?

Flera assistenter passar bra när:

- uppgiften har flera tydliga steg
- du vill kunna kontrollera mellanresultat
- du arbetar med jämförelser eller research
- du vill återanvända samma process flera gånger
- du behöver skilja mellan insamling, analys och granskning

En enda assistent räcker ofta när:

- uppgiften är enkel
- du bara behöver ett snabbt utkast
- resultatet inte ska användas som beslutsunderlag
- du inte behöver spara eller upprepa processen

En bra tumregel:

> Om du behöver kontrollera resultatet i flera steg, använd en pipeline.

## Vanliga misstag

- **Misstag:** alla assistenter får samma instruktion
    - Om varje assistent får ungefär samma instruktion blir de inte specialiserade. Då försvinner poängen med flera roller.
    - **Hur du undviker det:** Ge varje assistent ett eget ansvar, ett eget stoppområde och ett eget outputformat.

- **Misstag:** handoffen är för lös
    - Om överlämningen är otydlig måste nästa assistent gissa.
    - **Hur du undviker det:** Använd en enkel handoffmall.
    ```text
    Handoff till nästa steg
    - Syfte: Underlag: Vad som redan är gjort: Kända osäkerheter: Nästa steg ska göra: Svarformat: ```

- **Misstag:** granskning kommer för sent
    - Om du bara granskar slutrapporten kan många svagheter redan ha byggts in i arbetet.
    - **Hur du undviker det:** Lägg in kvalitetskontroll innan slutrapporten skrivs.

- **Misstag:** aI:n får fatta beslutet
    - En assistent kan hjälpa dig strukturera ett beslut, men den bör inte ensam fatta viktiga beslut.
    - **Hur du undviker det:** Låt AI:n ta fram underlag, alternativ och osäkerheter. Låt människan fatta beslutet.

## Övningar

### Övning 1: Rita din egen pipeline

Välj en öppen researchuppgift, till exempel:

- jämföra tre digitala verktyg
- följa en tekniktrend
- analysera offentliga rapporter
- skapa en kort omvärldsrapport

Skriv en pipeline med 3–5 steg.

Använd mallen:

```text
Steg 1:
Syfte:
Input:
Output:

Steg 2:
Syfte:
Input:
Output:

Steg 3:
Syfte:
Input:
Output:
```

### Övning 2: Skapa en handoffmall

Skapa en handoffmall för överlämning från Researchassistenten till Produktjämföraren.

Mallen ska innehålla:

- vad som jämförs
- vilka källor eller underlag som används
- vilka kriterier som ska användas
- vad som är osäkert
- vad nästa assistent inte ska göra

### Övning 3: Lägg till kvalitetskontroll

Ta en tidigare produktjämförelse från kapitel 5 eller en egen jämförelse.

Lägg till ett separat granskningssteg:

```text
Granska jämförelsen.
Markera påståenden utan tydligt underlag.
Markera aktuella uppgifter som behöver verifieras.
Kontrollera om slutsatsen är rimlig.
Föreslå tre förbättringar innan rapporten används.
```

### Fördjupning: Samma GPT eller flera GPT:er?

Välj ett av dina flöden och bestäm om det ska byggas som:

- en enda GPT med tydliga steg
- flera separata GPT:er
- ett Project med flera chattar
- en kombination av GPT och manuell granskning

Skriv varför.

## Snabb sammanfattning

- En **pipeline** är ett flöde där resultatet från ett steg används i nästa steg.
- En **handoff** är överlämningen mellan två steg eller assistenter.
- **Kvalitetskontroll** bör vara ett eget steg när resultatet ska användas som beslutsunderlag.
- Flera specialiserade assistenter är ofta bättre än en enda bred assistent när uppgiften är komplex.
- AI-Analytikern fungerar bäst när research, jämförelse, källkritik och rapportskrivning hålls isär.
- Människan ska fortfarande fatta beslutet, särskilt när underlaget är osäkert eller aktuella fakta behöver verifieras.

## Nästa steg

I nästa kapitel samlar vi allt du har byggt i boken. Du får skapa ett personligt AI-system: en liten portfölj av assistenter, mallar, instruktioner och underhållsrutiner som du kan fortsätta utveckla efter bokens slut.
