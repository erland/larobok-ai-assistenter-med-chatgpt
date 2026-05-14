# Kapitel 10: AI-agenter och automatisering utanför ChatGPT

## Varför detta kapitel finns

Hittills har boken handlat om egna GPT:er i ChatGPT: hur du skapar dem, instruerar dem, testar dem och avgränsar dem. Det är en bra grund, men det finns en närliggande fråga som ofta dyker upp:

Kan en AI-assistent göra mer än att svara i en chatt?

Svaret är ja, men det kräver att vi skiljer på tre saker:

- en **GPT** som hjälper dig i ChatGPT
- en **AI-agent** som kan ta flera steg mot ett mål och ibland använda verktyg
- en **automation** som kör ett förbestämt flöde automatiskt

Det här kapitlet ger en introduktion. Du ska inte bygga ett avancerat agentsystem ännu. Målet är att förstå vad som är möjligt, vad som är rimligt för en nybörjare och hur du kan planera enkla flöden utan att riskera känslig information.

Vi fortsätter med AI-Analytikern och använder ett öppet scenario: en veckovis omvärldsbevakning om offentliga AI-nyheter, produktförändringar eller trender.

## Lärandemål

Efter kapitlet ska läsaren kunna:

- förklara skillnaden mellan en GPT, en AI-agent och en automation
- känna igen när automatisering är användbar och när man bör behålla manuell kontroll
- beskriva ett enkelt agent- eller automationsflöde med trigger, steg och resultat
- planera en omvärldsbevakning som använder öppen information
- identifiera risker med automatiserade AI-flöden, särskilt kring källor, fel och ansvar

## Innan vi börjar

Du har redan arbetat med:

- **GPT:** en anpassad assistent med instruktioner och ibland kunskapsfiler.
- **Arbetsflöde:** en ordnad serie steg från behov till resultat.
- **Testfall:** en planerad uppgift som hjälper dig kontrollera kvaliteten.
- **Osäkerhet:** information som behöver markeras, kontrolleras eller verifieras.

I det här kapitlet introducerar vi tre nya huvudbegrepp:

- **AI-agent**
- **Trigger**
- **Automation**

Vi använder begreppen praktiskt, inte tekniskt. Du behöver inte programmera för att följa kapitlet.

## Huvudförklaring

### Vad är en AI-agent?

En **AI-agent** är ett AI-baserat system som kan arbeta mer självständigt än en vanlig chatt. En enkel chatt väntar på att du skriver något och svarar sedan. En agent kan ofta följa ett mål, dela upp uppgiften i steg, använda verktyg och återkomma med ett resultat.

Ett enkelt sätt att tänka är:

> En GPT hjälper dig när du frågar.  
> En agent kan hjälpa till att ta flera steg mot ett mål.

Exempel:

- En vanlig GPT kan hjälpa dig skriva en jämförelsemall.
- En mer agentliknande lösning kan hämta öppet material, sammanfatta det, sortera det och föreslå vad som är viktigast.
- En automation kan köra samma typ av uppgift varje måndag morgon.

Skillnaden är inte alltid knivskarp. Många moderna AI-funktioner ligger mellan “chatt” och “agent”. Därför är det bättre att fråga:

- Hur mycket självständighet får systemet?
- Vilka verktyg får det använda?
- När ska en människa kontrollera resultatet?
- Vad händer om systemet gör fel?

### Vad är en trigger?

En **trigger** är något som startar ett flöde.

En trigger kan till exempel vara:

- att du skriver en instruktion
- att en viss tidpunkt inträffar
- att en ny fil läggs till
- att ett formulär skickas in
- att en rad läggs till i ett kalkylblad
- att en ny artikel hittas i ett bevakningsflöde

I den här boken använder vi framför allt enkla triggers:

- “Varje fredag eftermiddag”
- “När jag har samlat fem länkar”
- “När jag vill jämföra tre produkter”
- “När jag har en lista med källor”

En trigger är viktig eftersom den hjälper dig se var arbetsflödet börjar. Utan en tydlig startpunkt blir automatisering lätt rörig.

### Vad är en automation?

En **automation** är ett flöde där ett eller flera steg sker automatiskt enligt en regel.

Exempel:

1. Varje måndag morgon startar ett flöde.
2. Flödet samlar länkar från valda öppna källor.
3. AI sammanfattar innehållet.
4. Resultatet sparas i ett dokument.
5. Du granskar dokumentet innan något skickas vidare.

Det sista steget är viktigt: du granskar. För nybörjare är det ofta klokt att automatisera förberedelser, inte beslut.

Automatisera gärna:

- insamling av öppet material
- sortering av länkar
- första sammanfattningar
- utkast till rapporter
- bevakningslistor
- checklistor

Var försiktig med att automatisera:

- publicering utan granskning
- beslut som påverkar andra människor
- hantering av känslig information
- ekonomiska eller juridiska slutsatser
- svar som ser säkra ut men bygger på osäkra källor

### GPT, agent eller automation?

Här är en praktisk jämförelse:

| Behov | Bäst startpunkt | Varför |
|---|---|---|
| Jag vill ha en återkommande researchmetod | Egen GPT | Instruktioner och format kan återanvändas |
| Jag arbetar länge med samma ämne | Project | Filer, chattar och kontext kan samlas |
| Jag vill ha samma bevakning varje vecka | Automation | Tid eller händelse kan starta flödet |
| Jag vill att AI tar flera steg med verktyg | Agent | Agenten kan planera och använda verktyg mer aktivt |
| Jag vill bara ställa en snabb fråga | Vanlig chatt | Minst struktur behövs |

En bra tumregel:

> Börja med en GPT.  
> Gå vidare till automation när uppgiften är återkommande.  
> Tänk agent först när uppgiften kräver flera steg, verktyg och kontrollpunkter.

### Varför detta kommer efter testning

Det är frestande att automatisera direkt. Men automatisering förstärker både bra och dåliga beteenden.

Om AI-Analytikern är otydlig i en vanlig chatt blir den ännu mer problematisk i ett automatiserat flöde. Om den inte markerar osäkerhet när du ber den manuellt, kommer den troligen inte göra det bättre bara för att flödet körs automatiskt.

Därför behöver du först:

- tydliga instruktioner
- avgränsade uppgifter
- testfall
- kontroll av källor
- tydliga outputformat

När de delarna fungerar kan du börja automatisera små delar.

## Exempel: Veckovis omvärldsbevakning med AI-Analytikern

Vi bygger inte ett tekniskt system här. Vi designar flödet.

### Målet

AI-Analytikern ska hjälpa dig skapa en veckovis översikt över öppna nyheter och produktförändringar inom ett valt område, till exempel:

- nya AI-verktyg för skrivande
- förändringar i ChatGPT-funktioner
- produktnyheter från tre leverantörer
- trender inom AI för utbildning
- nya publika rapporter inom ett branschområde

### Viktig avgränsning

Flödet ska inte använda:

- intern företagsinformation
- personuppgifter
- kunddata
- sekretessbelagda dokument
- opublicerade beslut
- privata mejl eller meddelanden

Det ska bara använda information som är öppen, publik och rimlig att sammanfatta.

### Flödet i fem steg

#### Steg 1: Välj bevakningsområde

Exempel:

> “AI-verktyg för produktivitet och research.”

Det är bättre än:

> “Allt nytt om AI.”

Ett smalt område ger bättre resultat.

#### Steg 2: Välj källtyper

Du kan börja med källtyper i stället för exakta verktyg:

- officiella produktbloggar
- hjälpcenter och dokumentation
- större teknikmedier
- forskningsrapporter
- öppna nyhetsbrev
- pressmeddelanden
- offentliga jämförelsesidor

AI-Analytikern ska inte behandla alla källor som lika säkra. En officiell produktsida är bättre för produktfunktioner. En oberoende recension kan vara bättre för användarupplevelse. Ett forum kan ge signaler, men bör inte användas som ensam källa.

#### Steg 3: Samla länkar eller underlag

För en nybörjarvänlig version gör du detta manuellt:

1. Samla 5–10 länkar.
2. Klistra in länkarna i ChatGPT eller i ditt Project.
3. Be AI-Analytikern strukturera materialet.

Det är inte helt automatiserat, men det är säkert och lätt att kontrollera.

En senare automation kan samla länkar automatiskt, men manuell insamling är en bra start.

#### Steg 4: Låt AI-Analytikern skapa ett utkast

Exempel på instruktion:

```text
Du är AI-Analytikern. Jag ger dig öppna källor om [område].

Gör en veckosammanfattning med följande struktur:

1. Kort översikt
2. De 5 viktigaste observationerna
3. Vad som verkar nytt
4. Vad som är osäkert eller behöver verifieras
5. Möjliga konsekvenser för en nybörjare som bygger AI-assistenter
6. Källista

Regler:
- Skilj mellan fakta från källorna och din egen bedömning.
- Markera osäker information tydligt.
- Gör inga påståenden om pris, tillgänglighet eller funktioner utan att ange att de bör verifieras.
- Använd bara öppen information.
```

#### Steg 5: Granska innan du använder resultatet

Din granskning bör kontrollera:

- Finns källor?
- Har assistenten blandat fakta och bedömning?
- Är något påstående för säkert?
- Saknas viktiga perspektiv?
- Är sammanfattningen användbar för målgruppen?
- Behöver något dubbelkollas i primärkällor?

Detta är mänsklig kontroll. Den är särskilt viktig när AI används för omvärldsbevakning, eftersom information snabbt blir gammal.

## Ett enkelt automationsflöde på papper

Innan du bygger något tekniskt kan du rita flödet så här:

```text
Trigger:
Varje fredag kl. 14.00

Input:
Lista med öppna källor och länkar från veckan

AI-steg:
1. Sammanfatta varje källa kort
2. Hitta återkommande teman
3. Markera osäkra uppgifter
4. Skapa en veckorapport

Mänsklig kontroll:
Granska källor, påståenden och slutsatser

Output:
En kort veckorapport i dokumentform
```

Den här typen av skiss gör två saker:

1. Den visar vad som kan automatiseras.
2. Den visar var mänsklig kontroll behövs.

För en nybörjare är det ofta bättre att ha ett tydligt halvautomatiserat flöde än ett otydligt helautomatiserat flöde.

## Tre nivåer av automatisering

Du kan tänka på automatisering i tre nivåer.

### Nivå 1: Manuell men strukturerad

Du samlar länkar själv och använder AI-Analytikern för att strukturera, sammanfatta och jämföra.

Passar när:

- du är nybörjare
- ämnet är viktigt
- du vill förstå processen
- du vill undvika felaktiga automatiska steg

### Nivå 2: Delvis automatiserad

Ett verktyg hjälper dig samla material, skapa påminnelser eller starta ett flöde. Du granskar fortfarande allt innan det används.

Passar när:

- uppgiften återkommer ofta
- källorna är ganska stabila
- du har testat instruktionerna
- du vill spara tid men behålla kontroll

### Nivå 3: Mer agentliknande flöde

AI kan själv ta flera steg, använda verktyg, navigera i information och skapa ett resultat. Du granskar resultatet och kan behöva godkänna viktiga steg.

Passar när:

- uppgiften kräver flera steg
- verktygsanvändning är nödvändig
- konsekvenserna av fel är hanterbara
- du har tydliga kontrollpunkter
- du förstår begränsningarna

Börja inte på nivå 3. Börja på nivå 1 och gå vidare när du vet att arbetsflödet fungerar.

## Vanliga misstag

- **Misstag:** att automatisera innan uppgiften är förstådd
    - Om du inte kan beskriva uppgiften manuellt kan du sällan automatisera den bra.
    - Bättre fråga:
    > Vilka steg gör jag själv idag?
    - När stegen är tydliga kan du välja vilka som lämpar sig för AI.

- **Misstag:** att låta AI välja källor helt fritt
    - AI kan hitta eller föreslå källor, men du behöver styra vilken typ av källor som är acceptabla.
    - Skriv hellre:
    > Prioritera officiella produktbloggar, dokumentation och välkända nyhetskällor. Markera forumdiskussioner och sociala medier som svagare signaler.
    - än:
    > Hitta allt viktigt om detta.

- **Misstag:** att hoppa över granskning
    - Automatisering kan ge en känsla av kontroll eftersom allt ser prydligt ut. Men ett snyggt dokument kan fortfarande innehålla fel.
    - Lägg därför alltid in ett granskningssteg, särskilt när resultatet ska användas i beslut, publicering eller rådgivning.

- **Misstag:** att använda känslig information av bekvämlighet
    - Det kan vara frestande att ladda upp interna dokument för att få bättre svar. I den här bokens exempel undviker vi det helt.
    - Använd i stället:
    - öppna källor
    - egna testdata
    - fiktiva exempel
    - publika produktbeskrivningar
    - egenformulerade sammanfattningar utan känsliga detaljer

- **Misstag:** att kalla allt för agent
    - Alla AI-flöden är inte agenter. En återkommande påminnelse är inte nödvändigtvis en agent. En GPT med bra instruktioner är inte automatiskt en agent.
    - Begreppet är användbart, men bara om det hjälper dig designa bättre arbetsflöden.
    - Fråga hellre:
    - Startar flödet automatiskt?
    - Använder AI verktyg?
    - Tar AI flera steg utan att jag styr varje steg?
    - Finns mänskliga kontrollpunkter?
    - Vad händer om något blir fel?

## Praktiskt exempel: från GPT till enkel automation

Tänk att du redan har en GPT som heter AI-Analytikern. Den fungerar bra när du ger den länkar manuellt.

Nästa steg kan vara att skapa ett återkommande arbetsflöde:

### Version A: Manuell veckorutin

Varje fredag:

1. Du samlar fem länkar.
2. Du öppnar AI-Analytikern.
3. Du klistrar in länkarna.
4. AI-Analytikern skapar en sammanfattning.
5. Du granskar och sparar resultatet.

Detta är inte avancerat, men det är stabilt.

### Version B: Påminnelsebaserad rutin

Varje fredag får du en påminnelse:

> “Samla veckans fem viktigaste länkar om AI-verktyg och kör dem genom AI-Analytikern.”

Nu är triggern automatiserad, men själva innehållet styrs fortfarande av dig.

### Version C: Delvis automatiserad rutin

Ett automationsverktyg samlar länkar från valda öppna källor och placerar dem i ett dokument. Du öppnar dokumentet och ber AI-Analytikern sammanfatta.

Nu är insamlingen delvis automatiserad, men du granskar fortfarande.

### Version D: Agentliknande rutin

Ett AI-verktyg hämtar, sammanfattar, sorterar, föreslår prioriteringar och skapar ett rapportutkast. Du granskar och godkänner.

Detta kan vara kraftfullt, men kräver tydligare kontroll.

## Säkerhets- och kvalitetsregel för AI-Analytikern

Lägg gärna till denna regel i AI-Analytikerns instruktioner:

```text
När du arbetar med omvärldsbevakning eller produktjämförelser:
- använd endast öppen information som användaren tillhandahåller eller uttryckligen ber dig analysera
- skilj mellan källbaserade fakta, tolkningar och rekommendationer
- markera information som kan vara inaktuell
- be användaren verifiera aktuella produktfunktioner, priser och tillgänglighet i primärkällor
- skapa aldrig en slutsats som kräver känsliga, privata eller interna uppgifter om användaren inte uttryckligen har gett ett säkert och godkänt underlag
```

Den här instruktionen gör assistenten mer användbar, men också mer försiktig.

## Övningar

### Övning 1: Rita ett enkelt automationsflöde

Välj ett öppet bevakningsområde, till exempel:

- AI-verktyg för skrivande
- AI i skolan
- nya funktioner i produktivitetsverktyg
- trender inom e-handel
- offentliga rapporter om hållbarhet

Skriv sedan:

```text
Bevakningsområde:
Trigger:
Input:
AI-steg:
Mänsklig kontroll:
Output:
Risker:
```

Målet är inte att bygga flödet tekniskt. Målet är att se hur flödet bör fungera.

### Övning 2: Välj rätt nivå

För varje scenario, välj nivå 1, 2 eller 3:

1. Du vill ibland jämföra två produkter.
2. Du vill varje vecka få en lista med fem nyheter inom ett ämne.
3. Du vill att AI ska samla, sortera och skriva en rapport från flera öppna källor.
4. Du vill göra en engångssammanfattning av en artikel.
5. Du vill följa tre leverantörers publika produktnyheter över tid.

Skriv en mening om varför du valde nivån.

### Övning 3: Lägg till kontrollpunkter

Ta flödet från övning 1 och lägg till minst tre kontrollpunkter.

Exempel:

- kontrollera att källorna är relevanta
- kontrollera att datum framgår
- kontrollera att prisuppgifter inte presenteras som säkra utan verifiering
- kontrollera att slutsatser skiljs från fakta
- kontrollera att inga känsliga uppgifter används

### Fördjupning: Förbättra AI-Analytikerns instruktion

Lägg till ett avsnitt i AI-Analytikerns instruktioner som heter:

```text
Regler för omvärldsbevakning och automatisering
```

Det ska innehålla:

- vilka källtyper som är lämpliga
- hur osäkerhet ska markeras
- vad assistenten inte får göra
- när användaren måste granska resultatet
- hur resultatet ska struktureras

## Snabb sammanfattning

- En GPT är ofta bästa startpunkten för en återkommande metod.
- En AI-agent kan ta flera steg mot ett mål och ibland använda verktyg.
- En automation startas av en trigger och följer ett förbestämt flöde.
- Automatisera inte en uppgift innan du förstår den manuellt.
- För omvärldsbevakning är öppna källor, tydliga avgränsningar och mänsklig kontroll extra viktiga.
- Börja med halvautomatiserade flöden innan du går mot mer självständiga agentflöden.
- Snygga AI-rapporter måste fortfarande granskas.

## Nästa steg

I nästa kapitel bygger vi vidare på detta genom att titta på hur flera assistenter kan samarbeta. AI-Analytikern kan då fungera som huvudflöde, medan specialiserade assistenter tar hand om research, produktjämförelse, källkritik och rapportstruktur.
