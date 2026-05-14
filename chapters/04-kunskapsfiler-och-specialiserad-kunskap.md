# Kapitel 4: Kunskapsfiler och specialiserad kunskap

## Varför detta kapitel finns

I de tidigare kapitlen har AI-Analytikern fått en tydlig roll, bättre instruktioner och ett mer stabilt svarsmönster. Nu är nästa steg att ge den ett mer konkret underlag att arbeta med.

En GPT kan bli mer användbar när den får tillgång till kunskapsfiler: dokument som beskriver ämnet, reglerna, begreppen, mallarna eller referensmaterialet den ska använda. Men kunskapsfiler är inte samma sak som att “göra GPT:n smartare i allmänhet”. De fungerar bäst när de används för avgränsat referensmaterial.

I den här boken använder vi bara öppen information. Det gör kapitlet tryggare att öva med. Du ska alltså inte ladda upp interna dokument, kunduppgifter, personuppgifter, avtal, lösenord, affärshemligheter eller annat känsligt material.

## Lärandemål

Efter kapitlet ska du kunna:

- förklara vad en kunskapsfil är och när den är användbar
- välja öppet och lämpligt källmaterial till en GPT
- strukturera kunskapsfiler så att de blir lättare för GPT:n att använda
- skriva instruktioner som säger hur assistenten ska använda filerna
- testa om AI-Analytikern faktiskt använder sitt källmaterial

## Innan vi börjar

Vi bygger vidare på tre begrepp från tidigare kapitel:

- **GPT:** den anpassade assistent du skapar i ChatGPT.
- **Instruktion:** texten som styr hur assistenten ska bete sig.
- **Outputformat:** den struktur assistenten ska använda när den svarar.

Nu lägger vi till tre nya huvudbegrepp:

- **Kunskapsfil:** en uppladdad fil som GPT:n kan använda som referens.
- **Källmaterial:** den information som används som underlag för ett svar.
- **Kontext:** den relevanta bakgrundsinformation som hjälper GPT:n förstå uppgiften.

## Vad är en kunskapsfil?

En kunskapsfil är ett dokument som du laddar upp till din GPT för att ge den ett särskilt referensmaterial. Det kan till exempel vara:

- en checklista
- en ordlista
- en mall
- en sammanfattning
- en publik rapport
- ett produktblad
- en egen guide baserad på öppen information

För AI-Analytikern kan kunskapsfiler användas för att göra arbetet mer konsekvent. I stället för att varje gång förklara hur en produktjämförelse ska göras kan du ladda upp en jämförelsemall. I stället för att varje gång beskriva vilka kriterier som är viktiga kan du skapa ett dokument med fasta analyskriterier.

Det viktiga är att förstå begränsningen: en kunskapsfil är ett stöd, inte en garanti. GPT:n kan använda filen som underlag, men du behöver fortfarande testa, granska och verifiera resultatet.

## När kunskapsfiler passar bra

Kunskapsfiler passar särskilt bra när du vill att en assistent ska använda samma underlag om och om igen.

Exempel:

| Behov | Lämplig kunskapsfil |
|---|---|
| Jämföra produkter på samma sätt varje gång | En jämförelsemall med kriterier |
| Använda samma begrepp konsekvent | En ordlista |
| Följa en viss arbetsprocess | En steg-för-steg-checklista |
| Skriva rapporter i samma format | En rapportmall |
| Sammanfatta öppna källor på ett kontrollerat sätt | En källkritisk arbetsmetod |

För AI-Analytikern börjar vi med tre enkla filer:

1. en ordlista
2. en jämförelsemall
3. en källkritisk checklista

De kan vara korta. Det är ofta bättre med tydliga och korta dokument än långa dokument där viktig information drunknar.

## När kunskapsfiler inte passar

Kunskapsfiler är inte rätt lösning för allt.

Använd inte kunskapsfiler för:

- information som ändras varje dag
- känsligt eller konfidentiellt material
- instruktioner som egentligen borde ligga i GPT:ns instruktioner
- stora mängder ostrukturerade dokument utan tydligt syfte
- bilder eller komplex layout där viktig information inte finns som text

En praktisk tumregel är:

**Lägg beteende i instruktionerna. Lägg referensmaterial i kunskapsfiler.**

Om du vill att AI-Analytikern alltid ska svara med rubrikerna “Sammanfattning”, “Källor”, “Osäkerheter” och “Nästa steg”, ska det stå i instruktionerna. Om du vill att den ska använda en viss jämförelsemall som underlag, kan mallen ligga som kunskapsfil.

## Bygg öppna kunskapsfiler för AI-Analytikern

Nu skapar vi en liten kunskapsbas med material som inte innehåller känslig information.

### Fil 1: Ordlista

Skapa ett dokument med rubriken:

```markdown
# Ordlista för AI-Analytikern

## Produktjämförelse
En strukturerad jämförelse mellan två eller flera produkter, tjänster eller verktyg.

## Kriterium
En egenskap som används för att jämföra alternativ, till exempel pris, funktioner, användarvänlighet eller integrationsmöjligheter.

## Källa
Den plats där informationen kommer ifrån, till exempel en officiell produktsida, dokumentation, rapport eller artikel.

## Osäkerhet
Något som inte kan bekräftas utifrån tillgängligt material eller som kan ha förändrats.
```

Syftet är inte att skapa en komplett ordlista. Syftet är att ge GPT:n dina definitioner.

### Fil 2: Jämförelsemall

Skapa ett dokument med rubriken:

```markdown
# Mall för produktjämförelser

När AI-Analytikern jämför produkter ska analysen innehålla:

1. Kort sammanfattning
2. Vilka produkter som jämförs
3. Jämförelsekriterier
4. Tabell med styrkor och svagheter
5. Osäkerheter och saker som behöver verifieras
6. Rekommendation beroende på användningsfall

Föreslagna jämförelsekriterier:
- Syfte
- Målgrupp
- Viktiga funktioner
- Begränsningar
- Pris eller prismodell, om informationen är offentlig och aktuell
- Integrationsmöjligheter
- Lämpligast för
```

Här får GPT:n en tydlig struktur att följa.

### Fil 3: Källkritisk checklista

Skapa ett dokument med rubriken:

```markdown
# Källkritisk checklista för öppen information

AI-Analytikern ska vara försiktig med information som kan vara inaktuell.

Vid research ska assistenten:
- skilja mellan bekräftad information och antaganden
- ange när något bör verifieras
- prioritera officiella källor när det är möjligt
- undvika att presentera uppskattningar som fakta
- varna när information kan ha förändrats
- inte hitta på exakta priser, datum, funktioner eller villkor
```

Den här filen förstärker bokens viktiga princip: AI kan hjälpa dig strukturera information, men aktuella fakta måste kontrolleras.

## Lägg till filerna i GPT:n

I GPT Builder finns en konfigurationsdel där du kan lägga till kunskap eller filer. Gränssnittet kan förändras, men arbetsprincipen är densamma:

1. öppna din GPT för redigering
2. gå till konfigurationsläget
3. hitta området för kunskap eller uppladdade filer
4. ladda upp dina dokument
5. spara eller uppdatera GPT:n
6. testa i förhandsgranskningen

Eftersom ChatGPT och GPT Builder utvecklas över tid bör du alltid kontrollera aktuella gränssnittssteg mot OpenAI:s hjälptexter när något ser annorlunda ut.

## Uppdatera instruktionerna

När du har laddat upp kunskapsfilerna behöver AI-Analytikern få veta hur de ska användas. Lägg till något i stil med detta i instruktionerna:

```text
Använd uppladdade kunskapsfiler som referensmaterial när de är relevanta för användarens fråga.

Om användaren ber om en produktjämförelse ska du följa jämförelsemallen om den finns i kunskapsfilerna.

Om information saknas i kunskapsfilerna ska du säga det tydligt i stället för att gissa.

Skilj mellan:
- information från kunskapsfiler
- information från användaren
- egna resonemang eller slutsatser

Markera alltid osäkerheter och sådant som bör verifieras mot aktuella källor.
```

Det här är ett exempel på hur instruktioner och kunskapsfiler samspelar. Filerna innehåller underlaget. Instruktionen säger hur underlaget ska användas.

## Testa om filerna används

Ett vanligt misstag är att ladda upp filer och anta att allt fungerar. Testa alltid.

Börja med en enkel fråga:

```text
Vilka jämförelsekriterier ska du använda när du jämför produkter?
```

Ett bra svar bör spegla jämförelsemallen.

Testa sedan en mer praktisk fråga:

```text
Hjälp mig jämföra tre öppet beskrivna verktyg för nyhetsbevakning. Använd din jämförelsemall och markera sådant som behöver verifieras.
```

Här ska AI-Analytikern inte bara svara fritt. Den ska använda strukturen från mallen och vara tydlig med osäkerheter.

Testa till sist en kontrollfråga:

```text
Vilka delar av ditt svar bygger på uppladdade kunskapsfiler, och vilka delar är egna slutsatser?
```

Detta hjälper dig se om assistenten kan skilja mellan olika typer av underlag.

## Vanliga misstag

- **Misstag:** att ladda upp för mycket material
    - **Varför det händer:** Det känns lockande att ge GPT:n “allt”.
    - **Hur du undviker det:** Börja med få, tydliga filer. Lägg hellre till mer senare när du vet vad som saknas.

- **Misstag:** att använda kunskapsfiler som instruktioner
    - **Varför det händer:** Man skriver regler i ett dokument och tror att GPT:n alltid kommer följa dem.
    - **Hur du undviker det:** Lägg viktiga beteenderegler i GPT:ns instruktioner. Använd filer för referensmaterial.

- **Misstag:** att ladda upp känslig information
    - **Varför det händer:** Man vill göra assistenten mer användbar för verkligt arbete.
    - **Hur du undviker det:** Använd bara material du har rätt att dela och som inte innehåller personuppgifter, affärshemligheter eller intern information.

- **Misstag:** att inte testa
    - **Varför det händer:** GPT:n verkar fungera efter första svaret.
    - **Hur du undviker det:** Testa med enkla frågor, praktiska uppgifter och kontrollfrågor.

## Övningar

### Övning 1: Skapa tre öppna kunskapsfiler

Skapa tre korta dokument:

1. en ordlista
2. en jämförelsemall
3. en källkritisk checklista

Använd exemplen i kapitlet som grund, men skriv om dem så att de passar ditt eget intresseområde.

### Övning 2: Ladda upp och testa

Lägg till dokumenten i AI-Analytikern och testa med frågan:

```text
Vilka regler och mallar ska du följa när du gör en produktjämförelse?
```

Spara svaret. Om svaret är otydligt, förbättra instruktionerna.

### Övning 3: Gör en enkel öppen jämförelse

Välj tre produkter, tjänster eller verktyg där informationen finns öppet på webben. Be AI-Analytikern skapa en jämförelse enligt din mall.

Kontrollera sedan:

- Följer svaret mallen?
- Markerar assistenten osäkerheter?
- Skiljer den mellan fakta och rekommendation?
- Finns något som borde verifieras?

### Övning 4: Förbättra kunskapsbasen

Lägg till en kort regel i din checklista som saknades i första testet. Testa igen och se om AI-Analytikern beter sig mer konsekvent.

## Snabb sammanfattning

- Kunskapsfiler är referensmaterial som en GPT kan använda.
- De passar bäst för mallar, ordlistor, checklistor och stabilt underlag.
- De ska inte användas för känsligt material.
- Viktiga beteenderegler hör hemma i instruktionerna.
- AI-Analytikern bör alltid markera osäkerheter och visa vad som behöver verifieras.
- Börja med få och tydliga filer, testa ofta och förbättra stegvis.

## Nästa steg

Nu har AI-Analytikern både bättre instruktioner och en liten öppen kunskapsbas. I nästa kapitel använder vi detta för att göra mer strukturerade produktjämförelser. Då får du se hur kriterier, tabeller och rekommendationer kan kombineras till ett praktiskt arbetsflöde.
