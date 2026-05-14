# Pedagogisk canon

## Språk
Svenska med etablerade engelska AI-termer när de behövs.

## Svårighetsgrad
Nybörjare till grundnivå.

## Läsarprofil
Läsaren har använt ChatGPT men aldrig skapat egna GPT:er. Läsaren vill bygga praktiska assistenter utan att behöva programmera.

## Ton
Vänlig, tydlig, praktisk och coachande.

## Repetitionstakt
Begrepp introduceras i små steg och återkommer i praktiska exempel.

## Genomgående exempelprojekt
### Namn
AI-Analytikern

### Syfte
Att visa hur man bygger en AI-assistent för research, omvärldsbevakning och produktjämförelser med öppen information.

### Regler
- Använd inte känsliga personuppgifter, intern företagsdata eller hemliga dokument i exemplen.
- Markera osäker information som osäker.
- Be läsaren verifiera aktuella fakta i primärkällor.
- Strukturera output tydligt så att den går att kontrollera.

### Hittills använda delar
- Kapitel 1: Projektet introduceras och assistentens uppdrag skissas.
- Kapitel 2: Första versionen av AI-Analytikern skapas som en privat GPT med grundinstruktioner och startfrågor.
- Kapitel 3: AI-Analytikerns instruktioner förbättras med roll, uppgift, process, begränsningar och outputformat.
- Kapitel 4: AI-Analytikern får en liten öppen kunskapsbas med ordlista, jämförelsemall och källkritisk checklista.
- Kapitel 5: AI-Analytikern används för strukturerade produktjämförelser med kriterier, beslutstabeller och tydlig markering av osäkerheter.
- Kapitel 6: Läsaren lär sig välja mellan GPT:er, Projects, Custom Instructions och tillfälliga chattar.
- Kapitel 7: AI-Analytikern delas upp i specialiserade assistenter som Trendspanaren, Produktjämföraren och Källkritikern.
- Kapitel 8: AI-Analytikern testas systematiskt med testfall, utvärderingskriterier och iterationslogg.
- Kapitel 9: Vanliga designmisstag och anti-patterns identifieras och repareras.
- Kapitel 10: AI-Analytikern planeras som ett öppet omvärldsbevakningsflöde med trigger, automation och mänsklig kontroll.
- Kapitel 11: AI-Analytikern delas in i en pipeline med Researchassistenten, Produktjämföraren, Källkritikern och Rapportskrivaren.
- Kapitel 12: AI-Analytikern sammanfattas som ett personligt AI-system med systemkarta, underhållsrutin och tydliga gränser.

## Versions- och faktaval
Funktioner i ChatGPT, GPT Builder, Projects, Custom Instructions, AI-agenter och automationsverktyg kan förändras. Boken ska undvika exakta gränssnittsdetaljer när de riskerar att bli inaktuella och markera att läsaren bör verifiera aktuella steg mot officiell dokumentation.


## Käll- och versionsnoteringar
- Kapitel 2 bygger på OpenAI Help Center-artiklar om GPTs in ChatGPT och Creating and editing GPTs, kontrollerade 2026-05-14.
- Exakta gränssnittssteg hålls medvetet generella eftersom ChatGPTs gränssnitt och funktioner kan förändras.

## Kapitel 3-noteringar
- Kapitel 3 introducerar systeminstruktion, beteenderegler och outputformat.
- Exempelprojektet fortsätter använda endast öppen information och betonar att känsliga uppgifter inte ska delas.

## Kapitel 4-noteringar
- Kapitel 4 introducerar kunskapsfil, källmaterial och kontext.
- Kunskapsfiler används som referensmaterial, inte som ersättning för instruktioner.
- Exemplen ska fortsätta undvika känslig information och använda öppna, kontrollerbara underlag.
- Aktuella fakta om ChatGPT-funktioner bör verifieras mot OpenAI Help Center.


## Kapitel 5-noteringar
- Kapitel 5 introducerar jämförelsekriterier, beslutstabell och osäkerhet.
- AI-Analytikern ska skilja mellan fakta, bedömning och osäkerhet vid produktjämförelser.
- Prisuppgifter, planer och aktuella produktfunktioner ska alltid markeras som sådant läsaren bör verifiera mot aktuella källor.


## Kapitel 6-noteringar
- Kapitel 6 introducerar Project, Custom Instructions och tillfällig chatt som alternativ eller komplement till egna GPT:er.
- Pedagogisk huvudregel: välj det enklaste arbetssättet som löser uppgiften.
- AI-Analytikern bör fortsätta vara en GPT för återkommande researchmetod, men större omvärldsbevakning över tid kan organiseras som ett Project.
- Kapitel 6 bygger på OpenAI Help Center-artiklar om Projects, Custom Instructions och GPTs in ChatGPT, kontrollerade 2026-05-14.


## Kapitel 7-noteringar
- Kapitel 7 introducerar specialisering, rollgräns och återanvändbar mall.
- AI-Analytikern kan fungera som huvudassistent, medan specialiserade assistenter tar hand om trendspaning, produktjämförelse och källkritik.
- Kapitlet fortsätter principen att arbeta med öppen information och att markera osäkerhet tydligt.
- Inga nya verktygsfunktioner kräver aktuell gränssnittsbeskrivning i detta kapitel.


## Kapitel 8-noteringar
- Kapitel 8 introducerar testfall, utvärderingskriterium och iterationslogg.
- Testning ska visa hur assistenten beter sig vid ofullständigt underlag, tidskänslig information och för snabba slutsatser.
- AI-Analytikern förbättras iterativt i små ändringar, inte genom stora otestade omskrivningar.

## Kapitel 9-noteringar
- Kapitel 9 introducerar designmönster, anti-pattern och felsökningsfråga.
- AI-Analytikern används för att visa hur för breda instruktioner, för säkra svar och bristande rollgränser kan upptäckas och rättas.
- Kapitlet förstärker att exempelprojektet ska bygga på öppen information och undvika känslig, intern eller personlig information.


## Kapitel 10: AI-agenter och automatisering utanför ChatGPT
- Kapitel 10 introducerar AI-agent, trigger och automation på praktisk introduktionsnivå.
- AI-Analytikern används för ett öppet scenario: veckovis omvärldsbevakning med publika källor.
- Kapitlet betonar att automatisering bör börja med manuellt förstådda och testade flöden.
- Mänsklig granskning, källkontroll och markering av osäkerhet ska alltid finnas i agent- och automationsflöden.
- Aktuella funktioner kring ChatGPT-agent, Tasks, appar/connectors och externa automationsverktyg bör verifieras mot officiell dokumentation före skarpa instruktioner eller export.


## Kapitel 11-noteringar
- Kapitel 11 introducerar pipeline, handoff och kvalitetskontroll.
- Huvudprincipen är att komplexa uppgifter ofta blir bättre när de delas upp i specialiserade steg.
- AI-Analytikern använder öppna informationsflöden och markerar osäkerheter innan rapport skrivs.
- Officiella OpenAI-källor kontrollerades 2026-05-14 för att hålla beskrivningar av GPT:er, Projects, Tasks och agentfunktioner generella och aktuella.


## Kapitel 12-noteringar
- Kapitel 12 introducerar AI-system, systemkarta och underhållsrutin.
- Boken avslutas med att AI-Analytikern organiseras som ett enkelt personligt AI-system för öppen information.
- Pedagogisk huvudregel: börja smalt, testa ofta och bygg bara ut systemet när det hjälper i praktiken.
- Automatisering beskrivs som stödarbete med fortsatt mänsklig kontroll över beslut och publicering.


## Kapitel 13: Nästa steg efter första versionen

### Introducerade begrepp
- Utvecklingslogg: kort dokumentation över problem, ändringar och resultat.
- Förbättringsbacklogg: lista över möjliga förbättringar som prioriteras efter nytta och risk.
- Beslutsregel: enkel regel för att välja mellan vanlig chatt, Project, GPT och automation.

### Kontinuitetsregel
Kapitel 13 behandlas som ett fördjupningskapitel efter den ursprungliga kapitelplanen. Det ska inte göra boken mer tekniskt avancerad, utan hjälpa läsaren vidareutveckla AI-Analytikern på ett kontrollerat sätt.
