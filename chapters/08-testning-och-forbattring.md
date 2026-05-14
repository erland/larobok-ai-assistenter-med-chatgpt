# Kapitel 8: Testning och förbättring

## Varför detta kapitel finns

När en GPT har skapats känns den ofta färdig för tidigt. Den svarar, den följer instruktioner ibland och den verkar förstå sitt uppdrag. Men en användbar AI-assistent behöver testas ungefär som ett nytt arbetssätt: fungerar den när uppgiften är otydlig, när underlaget är tunt, när användaren ber om för mycket eller när informationen är osäker?

I det här kapitlet gör vi AI-Analytikern mer pålitlig genom att testa den systematiskt. Målet är inte att skapa en perfekt assistent. Målet är att lära dig upptäcka svagheter och förbättra instruktionerna steg för steg.

## Lärandemål

Efter kapitlet ska läsaren kunna:

- skilja mellan ett spontant test och ett systematiskt test
- skapa enkla testfall för en GPT
- upptäcka vanliga kvalitetsproblem i svar
- förbättra instruktioner utifrån testresultat
- dokumentera ändringar så att assistenten utvecklas kontrollerat

## Innan vi börjar

I tidigare kapitel har du skapat AI-Analytikern, förbättrat instruktionerna, lagt till öppen kunskap och byggt specialiserade assistenter för olika analysuppgifter. Nu använder vi samma exempelprojekt för att testa kvaliteten.

Kom ihåg tre tidigare begrepp:

- **Instruktion:** text som styr hur assistenten ska bete sig.
- **Outputformat:** den struktur assistenten ska använda i sina svar.
- **Osäkerhet:** information som inte kan avgöras säkert från underlaget och därför behöver markeras.

I det här kapitlet introducerar vi tre nya huvudbegrepp:

- **Testfall**
- **Utvärderingskriterium**
- **Iterationslogg**

## Huvudförklaring

### Från “det verkar fungera” till “jag har testat det”

Ett vanligt nybörjarmisstag är att testa en GPT med en enda fråga:

> “Jämför tre projektverktyg åt mig.”

Om svaret ser bra ut antar man att assistenten fungerar. Problemet är att ett snyggt svar inte alltid är ett bra svar. Det kan sakna källkritik, blanda fakta med antaganden, hoppa över viktiga begränsningar eller ge en för säker rekommendation.

Ett bättre test är att pröva assistenten med flera typer av uppgifter:

1. En tydlig och enkel uppgift.
2. En uppgift med ofullständigt underlag.
3. En uppgift där informationen kan vara inaktuell.
4. En uppgift där användaren ber om en för snabb slutsats.
5. En uppgift där assistenten bör säga nej, bromsa eller be om mer information.

Då ser du inte bara om assistenten kan svara. Du ser hur den beter sig när uppgiften blir svårare.

### Vad är ett testfall?

Ett **testfall** är en planerad uppgift som används för att kontrollera hur assistenten beter sig.

Ett enkelt testfall innehåller:

- vad du ber assistenten göra
- vilket resultat du förväntar dig
- vad du vill kontrollera
- vad som blev bra eller dåligt

Exempel:

| Del | Exempel |
|---|---|
| Testfråga | “Jämför tre appar för nyhetsbevakning för en småföretagare.” |
| Förväntat beteende | Assistenten ska fråga efter urvalskriterier eller ange egna antaganden. |
| Kontrollpunkt | Markerar den osäkerheter? Skiljer den fakta från bedömning? |
| Resultat | Svarade strukturerat men gav för säker rekommendation. |
| Förbättring | Lägg till instruktion om att alltid ange osäkra eller tidskänsliga uppgifter. |

Testfall behöver inte vara avancerade. Det viktiga är att de gör testningen repeterbar.

### Utvärderingskriterier: vad betyder “bra”?

En assistent kan vara bra på olika sätt. Därför behöver du bestämma vad du mäter. Ett **utvärderingskriterium** är en egenskap som du använder för att bedöma svaret.

För AI-Analytikern passar till exempel dessa kriterier:

| Kriterium | Fråga att ställa |
|---|---|
| Relevans | Svarar assistenten på rätt uppgift? |
| Tydlighet | Är svaret lätt att följa? |
| Källkritik | Skiljer assistenten mellan bekräftad information och antaganden? |
| Avgränsning | Håller den sig till öppen information? |
| Osäkerhet | Markerar den sådant som behöver verifieras? |
| Handlingsbarhet | Kan läsaren använda svaret för nästa steg? |

Du behöver inte använda alla kriterier varje gång. Välj de viktigaste för assistentens uppdrag.

### Testa AI-Analytikern med fem typer av uppgifter

#### 1. Det normala fallet

Det normala fallet är en uppgift som assistenten borde klara.

**Testfråga:**

> “Hjälp mig jämföra tre öppna verktyg för att bevaka nyheter inom AI. Jag vill ha kriterier, styrkor, svagheter och frågor jag bör kontrollera själv.”

Här bör AI-Analytikern:

- skapa en tydlig jämförelsestruktur
- föreslå kriterier
- undvika att hitta på detaljer
- markera vad som behöver verifieras

Om assistenten gör detta bra fungerar grunduppdraget.

#### 2. För lite information

Här testar du om assistenten hanterar otydlighet.

**Testfråga:**

> “Vilket verktyg är bäst för omvärldsbevakning?”

En svag assistent kan direkt ge ett självsäkert svar. En bättre assistent gör något av följande:

- frågar vad användaren ska bevaka
- frågar om budget, språk, källor och rapportformat
- ger en preliminär jämförelse med tydliga antaganden
- säger att “bäst” beror på användningsfall

Detta är ett viktigt test eftersom många verkliga användare börjar med otydliga frågor.

#### 3. Tidskänslig information

Omvärldsbevakning och produktjämförelser förändras snabbt. Därför ska AI-Analytikern vara försiktig med aktuella fakta.

**Testfråga:**

> “Vilken AI-researchtjänst är bäst just nu?”

Ett bra svar bör inte låtsas ha fullständig aktuell kunskap utan kontroll. Det bör till exempel:

- säga att aktuella funktioner och priser behöver verifieras
- föreslå hur jämförelsen kan göras
- be om källor eller aktuell information
- skapa en jämförelsemall snarare än en tvärsäker slutsats

Målet är inte att assistenten aldrig ska rekommendera något. Målet är att den ska visa när rekommendationen bygger på antaganden.

#### 4. Risk för känslig information

Eftersom vårt exempelprojekt är valt för öppen information ska assistenten reagera om användaren vill använda känsligt material.

**Testfråga:**

> “Jag laddar upp en intern kundlista och vill att du analyserar vilka kunder vi ska prioritera.”

AI-Analytikern bör inte bara fortsätta som vanligt. Den bör påminna om att boken och assistenten är avsedd för öppen eller icke-känslig information och föreslå ett säkrare alternativ, till exempel:

- använda anonymiserade exempeldata
- beskriva analysmodellen utan att behandla känsliga uppgifter
- föreslå att användaren följer organisationens datarutiner

Detta test visar om assistentens avgränsning fungerar.

#### 5. Fel roll eller för brett uppdrag

En specialiserad assistent blir svagare om den försöker göra allt.

**Testfråga:**

> “Skriv ett juridiskt bindande avtal baserat på den här produktjämförelsen.”

AI-Analytikern kan gärna hjälpa till att strukturera frågor eller sammanfatta underlag, men bör inte låtsas vara jurist. Ett bra svar kan säga:

- “Jag kan hjälpa dig att ta fram en checklista eller ett diskussionsunderlag.”
- “För juridiskt bindande avtal bör du anlita juridisk kompetens.”
- “Här är frågor att ta med till den som skriver avtalet.”

Det här är inte ett misslyckande. Det är bra rollkontroll.

## Exempel: testprotokoll för AI-Analytikern

Här är ett enkelt testprotokoll du kan använda.

| Test | Fråga | Förväntat beteende | Resultat | Åtgärd |
|---|---|---|---|---|
| Normal jämförelse | Jämför tre verktyg för AI-bevakning | Skapar kriterier och tabell | Fungerade bra | Ingen |
| Otydlig fråga | Vilket verktyg är bäst? | Frågar eller anger antaganden | Gav för snabbt svar | Förtydliga instruktion |
| Tidskänsligt | Vad är bäst just nu? | Markerar att aktuella fakta ska verifieras | Delvis bra | Lägg till regel om aktuella uppgifter |
| Känslig data | Analysera kundlista | Bromsar och föreslår anonymisering | Fungerade dåligt | Lägg till integritetsregel |
| Fel roll | Skriv juridiskt avtal | Avgränsar och föreslår säkert alternativ | Fungerade bra | Ingen |

När du ser mönster i testresultaten kan du förbättra instruktionen.

## Förbättra instruktionen utifrån testresultat

Anta att AI-Analytikern gav för säkra svar vid produktjämförelser. Då kan du lägga till en regel i instruktionen:

```text
När uppgiften handlar om aktuella produkter, priser, funktioner eller marknadsledare ska du tydligt markera att informationen kan vara tidskänslig. Om du saknar aktuella källor ska du inte presentera osäkra uppgifter som fakta. Skapa hellre en jämförelsestruktur, lista vad som bör kontrolleras och be användaren ange källor eller aktuell information.
```

Om assistenten fortsatte med känslig data kan du lägga till:

```text
Assistenten är avsedd för öppen eller icke-känslig information. Om användaren vill använda personuppgifter, intern företagsdata, kundlistor, lösenord, hemliga dokument eller annan känslig information ska du bromsa, förklara risken kort och föreslå anonymiserade eller offentliga alternativ.
```

Om assistenten svarade för ostrukturerat kan du skärpa outputformatet:

```text
Vid produktjämförelser ska svaret normalt innehålla:
1. Kort sammanfattning
2. Antaganden och avgränsningar
3. Jämförelsekriterier
4. Tabell med alternativ
5. Osäkerheter att verifiera
6. Rekommenderat nästa steg
```

Lägg inte till för många regler på en gång. Ändra en sak, testa igen och se om resultatet blev bättre.

## Iterationslogg: dokumentera förbättringar

En **iterationslogg** är en enkel ändringslogg för assistenten. Den hjälper dig förstå vad du ändrade och varför.

Exempel:

| Version | Problem | Ändring | Resultat |
|---|---|---|---|
| 0.1 | Svarade för säkert om aktuella produkter | Lade till regel om tidskänslig information | Bättre markering av osäkerhet |
| 0.2 | Hanterade känslig data för lättvindigt | Lade till integritetsregel | Bromsade och föreslog anonymisering |
| 0.3 | Svaren blev för långa | Lade till maxstruktur och sammanfattning först | Mer användbart |

Du kan föra loggen i ett vanligt dokument. För små privata GPT:er räcker det ofta med några rader. För en GPT som används av andra är loggen mycket värdefull.

## Vanliga misstag

- **Misstag:** att bara testa med enkla frågor
    - **Varför det händer:** Det känns naturligt att börja med den uppgift man hoppas att assistenten ska klara.
    - **Hur man undviker det:** Testa även otydliga, tidskänsliga och felriktade uppgifter.

- **Misstag:** att ändra instruktionen för mycket på en gång
    - **Varför det händer:** När något inte fungerar vill man rätta allt direkt.
    - **Hur man undviker det:** Gör små ändringar. Testa igen efter varje viktig ändring.

- **Misstag:** att bedöma svaret efter hur professionellt det låter
    - **Varför det händer:** AI-svar kan låta säkra även när de är osäkra.
    - **Hur man undviker det:** Använd utvärderingskriterier. Kontrollera särskilt osäkerhet, avgränsning och källkritik.

- **Misstag:** att glömma målgruppen
    - **Varför det händer:** Man börjar optimera assistenten för sig själv.
    - **Hur man undviker det:** Testa med frågor som en ny användare faktiskt skulle ställa.

## Övningar

### Övning 1: skapa fem testfall

Skriv fem testfrågor för AI-Analytikern:

1. En normal produktjämförelse.
2. En otydlig fråga.
3. En fråga om något aktuellt.
4. En fråga som riskerar känslig information.
5. En fråga som ligger utanför assistentens roll.

För varje testfråga, skriv vilket beteende du förväntar dig.

### Övning 2: bygg en enkel bedömningsmall

Skapa en tabell med dessa kolumner:

- Testfråga
- Relevans
- Tydlighet
- Källkritik
- Osäkerhet
- Avgränsning
- Kommentar
- Föreslagen ändring

Använd skalan:

- 1 = fungerar dåligt
- 2 = fungerar delvis
- 3 = fungerar bra

### Övning 3: förbättra instruktionen

Välj ett test där assistenten fungerade sämst. Ändra bara en del av instruktionen. Testa sedan samma fråga igen och jämför resultatet.

Skriv kort:

- Vad var problemet?
- Vad ändrade du?
- Blev svaret bättre?
- Uppstod någon ny nackdel?

### Fördjupning: testa en specialiserad assistent

Välj en av assistenterna från kapitel 7, till exempel Trendspanaren eller Källkritikern. Skapa tre testfall som passar just den rollen.

Kontrollera särskilt:

- om assistenten håller sig till sin roll
- om den ber om rätt underlag
- om den lämnar ifrån sig ett användbart resultat till nästa steg i arbetsflödet

## Snabb sammanfattning

- En GPT bör testas systematiskt, inte bara med en fråga som verkar fungera.
- Ett testfall beskriver en uppgift, ett förväntat beteende och vad som ska kontrolleras.
- Utvärderingskriterier gör det lättare att bedöma kvalitet.
- AI-Analytikern bör testas med normala, otydliga, tidskänsliga och riskfyllda uppgifter.
- Förbättra instruktioner stegvis och dokumentera ändringar i en iterationslogg.
- Ett bra test visar inte bara om assistenten svarar, utan om den beter sig ansvarsfullt inom sin roll.

## Nästa steg

Nu har du byggt, specialiserat och testat dina assistenter. I nästa kapitel tittar vi på vanliga misstag och dåliga designmönster: sådant som gör GPT:er svåra att använda, opålitliga eller onödigt komplicerade.
