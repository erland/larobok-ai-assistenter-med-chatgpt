# Kapitel 12: Bygg ditt personliga AI-system

## Varför detta kapitel finns

Du har nu byggt, förbättrat och testat flera typer av AI-assistenter. Du har också sett hur GPT:er kan ingå i större arbetsflöden med flera steg, flera roller och ibland automation.

Det här kapitlet binder ihop boken.

Målet är inte att du ska skapa ett komplicerat system. Målet är att du ska kunna organisera dina assistenter, mallar och arbetsflöden så att de blir användbara över tid.

I kapitlet använder vi det genomgående exempelprojektet **AI-Analytikern** och gör om det från en samling idéer till ett enkelt personligt AI-system för öppen research, omvärldsbevakning och produktjämförelser.

## Lärandemål

Efter kapitlet ska du kunna:

- beskriva vad ett personligt AI-system är
- välja vilka assistenter som ska ingå i ett eget system
- organisera instruktioner, mallar, kunskapsfiler och arbetsflöden
- skapa en enkel underhållsrutin för dina GPT:er
- avgöra när ett AI-system behöver förenklas i stället för byggas ut

## Innan vi börjar

Vi repeterar några begrepp från tidigare kapitel:

- En **GPT** är en anpassad assistent i ChatGPT.
- Ett **arbetsflöde** är en serie steg från behov till resultat.
- En **pipeline** är ett arbetsflöde där varje steg lämnar vidare ett tydligt resultat till nästa steg.
- En **handoff** är själva överlämningen mellan steg.
- En **kvalitetskontroll** är ett separat granskningssteg innan resultat används.

I det här kapitlet introducerar vi tre nya huvudbegrepp:

- **AI-system**
- **Systemkarta**
- **Underhållsrutin**

## Huvudförklaring

### Vad är ett personligt AI-system?

Ett **personligt AI-system** är en organiserad samling av assistenter, instruktioner, mallar och rutiner som hjälper dig med återkommande arbete.

Det behöver inte vara tekniskt avancerat.

Ett enkelt AI-system kan bestå av:

- två eller tre egna GPT:er
- några återanvändbara promptmallar
- en mapp med öppna kunskapsfiler
- en enkel checklista för kvalitet
- en rutin för när assistenter ska uppdateras

Skillnaden mellan “några chattar” och ett AI-system är att systemet är genomtänkt. Du vet vad varje del gör, när den ska användas och hur resultatet ska kontrolleras.

### AI-Analytikern som system

I början av boken var AI-Analytikern bara en idé: en assistent som hjälper med öppen research.

Nu kan AI-Analytikern beskrivas som ett litet system:

1. **Researchassistenten** samlar och strukturerar öppet underlag.
2. **Produktjämföraren** jämför alternativ mot tydliga kriterier.
3. **Källkritikern** markerar osäkerheter och sådant som behöver verifieras.
4. **Rapportskrivaren** skapar en kort och läsbar sammanfattning.
5. **Användaren** gör den slutliga bedömningen.

Det viktiga är att människan fortfarande äger beslutet. AI-systemet hjälper till att strukturera arbetet, men det ersätter inte omdöme, källkritik eller ansvar.

### Systemkarta: rita upp dina delar

En **systemkarta** är en enkel översikt över vilka delar som ingår i ditt AI-system.

Den kan vara mycket enkel:

| Del | Syfte | Input | Output |
|---|---|---|---|
| Researchassistenten | Samla öppet underlag | Fråga, ämne, källor | Sorterad underlagslista |
| Produktjämföraren | Jämföra alternativ | Alternativ och kriterier | Jämförelsetabell |
| Källkritikern | Granska osäkerheter | Underlag och tabell | Lista över risker och kontrollpunkter |
| Rapportskrivaren | Skriva sammanfattning | Granskat underlag | Kort rapport |

En systemkarta hjälper dig att se om något saknas. Den hjälper dig också att upptäcka om en assistent försöker göra för mycket.

Om en rad i kartan har för många syften är det ofta ett tecken på att assistenten bör delas upp.

### Börja smalt

Ett vanligt misstag är att försöka bygga ett stort AI-system direkt.

Det är bättre att börja med ett litet system som fungerar ofta än ett stort system som fungerar ibland.

En bra första version kan vara:

- en GPT för research
- en GPT för granskning
- en rapportmall
- en enkel checklista för verifiering

När det fungerar kan du lägga till fler delar.

Frågan är inte: “Hur mycket kan jag automatisera?”

En bättre fråga är: “Vilka delar återkommer så ofta att de förtjänar en tydlig rutin?”

### Ordning bland instruktioner och mallar

När du har flera assistenter behöver du ordning.

Du kan använda en enkel struktur:

```text
AI-system/
├── assistenter/
│   ├── researchassistenten.md
│   ├── produktjamforaren.md
│   └── kallkritikern.md
├── mallar/
│   ├── jamforelsetabell.md
│   ├── rapportmall.md
│   └── handoff-mall.md
├── kunskapsfiler/
│   ├── ordlista.md
│   └── kallkritisk-checklista.md
└── underhall/
    ├── testfall.md
    └── andringslogg.md
```

Det här är bara ett exempel. Du behöver inte skapa exakt dessa mappar. Poängen är att dina instruktioner, mallar och testfall inte ska försvinna i gamla chattar.

### En enkel underhållsrutin

En **underhållsrutin** är ett återkommande sätt att kontrollera att dina assistenter fortfarande fungerar.

För AI-Analytikern kan rutinen vara:

1. Välj tre gamla testfall.
2. Kör dem igen.
3. Jämför svaren med dina utvärderingskriterier.
4. Notera vad som blivit bättre eller sämre.
5. Uppdatera instruktioner eller mallar vid behov.
6. Skriv en kort rad i ändringsloggen.

En ändringslogg kan se ut så här:

| Datum | Assistent | Problem | Ändring | Resultat |
|---|---|---|---|---|
| 2026-05-14 | Produktjämföraren | Blandade fakta och bedömning | Lade till tydligare outputformat | Tabellerna blev lättare att granska |
| 2026-05-14 | Källkritikern | Missade osäkra prisuppgifter | Lade till regel om aktuella priser | Fler kontrollpunkter markerades |

Det behöver inte vara mer avancerat än så.

### Vad ska inte automatiseras?

Allt som kan automatiseras bör inte automatiseras.

Var extra försiktig med:

- beslut som påverkar människor
- känslig information
- publicering utan mänsklig granskning
- ekonomiska rekommendationer
- juridiska, medicinska eller säkerhetskritiska frågor
- innehåll där aktuella fakta snabbt kan förändras

I AI-Analytikern är det rimligt att automatisera delar av sortering, sammanfattning och rapportutkast. Det är däremot inte rimligt att låta systemet publicera slutsatser automatiskt utan granskning.

En bra regel är:

> Automatisera förberedelser. Behåll mänsklig kontroll över beslut och publicering.

### När systemet behöver förenklas

Ett AI-system kan bli för stort.

Tecken på att du bör förenkla:

- du minns inte vilken assistent du ska använda
- flera assistenter gör nästan samma sak
- handoffarna är krångligare än själva arbetet
- du litar mindre på resultatet än tidigare
- du lägger mer tid på att underhålla systemet än på att använda det

Då är lösningen inte fler instruktioner. Lösningen är ofta att ta bort, slå ihop eller förenkla.

Ett bra AI-system känns tydligt. Du ska förstå varför varje del finns.

## Exempel: Slutversion av AI-Analytikern

Här är en enkel slutversion av AI-Analytikern som personlig researchmiljö.

### Syfte

AI-Analytikern ska hjälpa användaren att arbeta med öppen information på ett strukturerat och källkritiskt sätt.

### Systemdelar

| Del | När den används | Resultat |
|---|---|---|
| Researchassistenten | När ett nytt ämne ska undersökas | Sorterad lista över underlag och frågor |
| Produktjämföraren | När flera alternativ ska jämföras | Beslutstabell med kriterier |
| Källkritikern | Innan resultat används | Kontrollpunkter, osäkerheter och verifieringsbehov |
| Rapportskrivaren | När materialet ska sammanfattas | Kort rapport med tydliga avsnitt |

### Grundregler

AI-Analytikern ska:

- använda öppen information
- markera osäkerheter
- skilja mellan fakta och bedömning
- föreslå vad användaren bör verifiera
- undvika känslig information
- inte fatta beslut åt användaren

### Exempel på arbetsflöde

Användaren vill jämföra tre projektverktyg.

1. Researchassistenten tar fram en första struktur.
2. Produktjämföraren skapar en jämförelsetabell.
3. Källkritikern markerar vilka påståenden som behöver kontrolleras.
4. Rapportskrivaren skriver ett kort beslutsunderlag.
5. Användaren kontrollerar aktuella källor och gör sin egen bedömning.

Det här är ett komplett men fortfarande enkelt AI-system.

## Vanliga misstag

- **Misstag:** Att bygga för många assistenter direkt.
    - **Varför det händer:** Det känns effektivt att specialisera allt.
    - **Hur man undviker det:** Börja med två eller tre assistenter och bygg ut först när behovet återkommer.

- **Misstag:** Att sakna tydliga handoffs.
    - **Varför det händer:** Man tänker på varje assistent separat.
    - **Hur man undviker det:** Bestäm vad varje assistent ska lämna vidare.

- **Misstag:** Att inte underhålla instruktionerna.
    - **Varför det händer:** En GPT känns färdig när den fungerar första gången.
    - **Hur man undviker det:** Använd en enkel ändringslogg och några återkommande testfall.

- **Misstag:** Att automatisera publicering eller beslut för tidigt.
    - **Varför det händer:** Automation känns som slutmålet.
    - **Hur man undviker det:** Automatisera stödarbete, men behåll mänsklig granskning.

## Övningar

### Övning 1: Skapa din systemkarta

Rita eller skriv en enkel systemkarta för ditt eget AI-system.

Använd tabellen:

| Del | Syfte | Input | Output |
|---|---|---|---|
| | | | |

Börja med högst fyra delar.

### Övning 2: Välj vad som ska ingå i första versionen

Markera vilka delar som ska ingå i version 1:

- research
- jämförelse
- källkritik
- rapportskrivning
- omvärldsbevakning
- automatisering
- publicering
- arkivering

Välj hellre färre delar än för många.

### Övning 3: Skapa en underhållsrutin

Skriv en enkel rutin med fem steg för hur du ska testa och förbättra dina assistenter.

Exempel:

1. Välj två testfall.
2. Kör assistenten.
3. Kontrollera svaret mot kriterier.
4. Justera instruktionen.
5. Skriv ändringen i loggen.

### Fördjupning: Din första systemversion

Skriv en kort beskrivning av ditt personliga AI-system:

- Vad ska systemet hjälpa dig med?
- Vilka assistenter ingår?
- Vilka uppgifter får systemet inte göra?
- Vilken information får användas?
- När ska en människa granska resultatet?

## Snabb sammanfattning

- Ett personligt AI-system är en organiserad samling assistenter, mallar, kunskapsfiler och rutiner.
- Systemet behöver inte vara tekniskt avancerat för att vara användbart.
- En systemkarta visar vilka delar som ingår och hur de hänger ihop.
- Underhållsrutiner gör att assistenter kan förbättras över tid.
- Det är ofta bättre att börja smalt och bygga ut gradvis.
- Automatisering passar bäst för stödarbete, inte för beslut utan granskning.
- AI-Analytikern kan fungera som ett tryggt exempel eftersom den bygger på öppen information.

## Nästa steg

Du har nu en grund för att skapa egna GPT:er, bygga arbetsflöden och tänka mer systematiskt kring AI-assistenter.

Ett bra nästa steg är att välja ett verkligt, men ofarligt, område där du vill använda AI. Det kan vara en hobby, ett öppet researchområde, en produktkategori eller en återkommande informationsuppgift.

Börja litet. Testa ofta. Skriv ner vad du lär dig. Bygg bara ut systemet när det hjälper dig på riktigt.
