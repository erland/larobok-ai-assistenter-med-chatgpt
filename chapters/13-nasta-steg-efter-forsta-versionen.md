# Kapitel 13: Nästa steg efter första versionen

## Varför detta kapitel finns

Den ursprungliga kapitelplanen avslutades med kapitel 12, där du byggde ditt personliga AI-system. Men när ett AI-system börjar användas i verkligheten uppstår nästa fråga:

Hur går man vidare utan att bygga för stort, för snabbt eller för osäkert?

Det här kapitlet är ett fördjupningskapitel. Det hjälper dig att ta AI-Analytikern från en fungerande första version till ett arbetssätt som kan utvecklas över tid.

Fokus ligger fortfarande på öppen information. Vi undviker känsliga uppgifter och arbetar med sådant som kan delas, granskas och kontrolleras.

## Lärandemål

Efter kapitlet ska du kunna:

- skilja mellan en första version och en förbättrad version av en AI-assistent
- prioritera vilka förbättringar som är värda att göra
- skapa en enkel utvecklingsplan för AI-Analytikern
- dokumentera förändringar utan att göra arbetet tungt
- avgöra när en idé bör bli en GPT, ett Project, en vanlig chatt eller en automation

## Innan vi börjar

Vi använder flera begrepp som du redan mött:

- **AI-system**: en organiserad samling assistenter, mallar och rutiner
- **Underhållsrutin**: ett återkommande sätt att testa och förbättra systemet
- **Kvalitetskontroll**: ett separat steg där resultat granskas innan det används
- **Automation**: ett flöde där vissa steg utförs automatiskt

I det här kapitlet introducerar vi tre nya huvudbegrepp:

- **Utvecklingslogg**
- **Förbättringsbacklogg**
- **Beslutsregel**

## Huvudförklaring

### Första versionen är inte slutmålet

En vanlig missuppfattning är att en GPT ska bli “färdig”.

I praktiken fungerar bra AI-assistenter mer som arbetsrutiner. De används, testas, justeras och ibland förenklas.

Det viktiga är inte att AI-Analytikern blir perfekt. Det viktiga är att den blir:

- tydlig nog att använda
- enkel nog att underhålla
- säker nog för sin uppgift
- användbar nog för återkommande arbete

En bra första version svarar på frågan:

> Kan den hjälpa mig med uppgiften?

En förbättrad version svarar på frågan:

> Hjälper den mig på ett stabilt, begripligt och kontrollerbart sätt?

### Utvecklingslogg: skriv ned vad som ändras

En **utvecklingslogg** är en enkel lista över ändringar du gör i en GPT, mall eller arbetsprocess.

Den behöver inte vara avancerad. Syftet är att du ska kunna förstå vad som ändrats och varför.

Exempel:

| Datum | Del | Problem | Ändring | Resultat |
|---|---|---|---|---|
| 2026-05-14 | Produktjämföraren | Svaren blev för långa | Lade till max 5 kriterier och kort slutsats | Mer användbara jämförelser |
| 2026-05-14 | Källkritikern | Missade osäkra påståenden | Lade till krav på “behöver verifieras” | Tydligare risklista |

En utvecklingslogg gör två saker:

1. Den hjälper dig att lära av dina ändringar.
2. Den hindrar dig från att ändra för mycket på en gång.

Om du ändrar fem saker samtidigt och resultatet blir bättre vet du inte vilken ändring som hjälpte.

### Förbättringsbacklogg: samla idéer utan att bygga allt

En **förbättringsbacklogg** är en prioriterad lista över möjliga förbättringar.

Det är inte en att-göra-lista där allt måste bli gjort. Det är en plats där du samlar idéer så att du kan välja klokt.

Exempel för AI-Analytikern:

| Förbättring | Nytta | Risk | Prioritet |
|---|---|---|---|
| Tydligare mall för produktjämförelser | Hög | Låg | Hög |
| Automatisk veckorapport | Medel | Medel | Vänta |
| Fler specialist-GPT:er | Medel | Risk för komplexitet | Vänta |
| Bättre källkritisk checklista | Hög | Låg | Hög |
| Integration med externa verktyg | Hög | Högre krav på kontroll | Senare |

En bra backlogg hjälper dig att säga nej. Det är viktigt, eftersom AI-verktyg ofta gör det lätt att bygga mer än man faktiskt behöver.

### Beslutsregel: välj rätt form för nästa idé

En **beslutsregel** är en enkel regel som hjälper dig välja hur en idé ska genomföras.

När du får en ny idé för AI-Analytikern kan du fråga:

1. Är detta en engångsuppgift?  
   Använd en vanlig chatt.

2. Behöver arbetet ett längre sammanhang med många filer eller flera steg?  
   Använd ett Project.

3. Är detta en återkommande uppgift med tydlig roll och process?  
   Skapa eller förbättra en GPT.

4. Ska något starta automatiskt vid en tidpunkt eller händelse?  
   Överväg automation.

5. Kräver uppgiften känslig information, beslut med stor påverkan eller expertbedömning?  
   Förenkla, avgränsa eller låt bli att automatisera.

Beslutsregeln gör att systemet inte växer okontrollerat.

### När en GPT bör delas upp

AI-Analytikern kan med tiden bli för bred.

Tecken på att en GPT bör delas upp:

- den får mycket långa instruktioner
- den ska hantera flera helt olika uppgifter
- den blandar research, analys, skrivande och granskning på ett otydligt sätt
- den ger svar som är svåra att kontrollera
- du måste förklara uppgiften på nytt varje gång

Då kan det vara bättre att skapa flera mindre assistenter:

- en för att samla underlag
- en för att jämföra alternativ
- en för att granska källor
- en för att skriva rapporter

Mindre assistenter är ofta lättare att testa.

### När systemet bör förenklas

Utveckling betyder inte alltid att lägga till mer.

Ibland är nästa steg att ta bort.

Du bör förenkla AI-systemet när:

- du inte längre vet vilken assistent du ska använda
- flera GPT:er gör nästan samma sak
- instruktionerna är så långa att du inte själv orkar läsa dem
- resultatet kräver mer efterarbete än tidigare
- du bygger funktioner som sällan används

En bra regel är:

> Om systemet blir svårare att använda än uppgiften det ska hjälpa med, är systemet för stort.

## Exempel: AI-Analytikerns utvecklingsplan

Anta att AI-Analytikern används för att jämföra öppet tillgängliga AI-verktyg.

Efter några tester märker du detta:

- jämförelserna är användbara
- men kriterierna varierar för mycket
- källkritiken kommer ibland för sent
- rapporterna blir olika långa från gång till gång

En rimlig utvecklingsplan kan då se ut så här:

### Steg 1: Standardisera jämförelsemallen

Skapa en fast mall:

1. Syfte med jämförelsen
2. Alternativ som jämförs
3. Kriterier
4. Styrkor
5. Svagheter
6. Osäkra eller overifierade påståenden
7. Kort slutsats

Det gör resultatet mer förutsägbart.

### Steg 2: Lägg in källkritik tidigare

I stället för att granska först i slutet kan AI-Analytikern markera osäkerhet direkt i tabellen.

Exempel:

| Påstående | Status |
|---|---|
| Produkten har gratisversion | Behöver verifieras |
| Verktyget är webbaserat | Troligen, kontrollera aktuell källa |
| Priset är lägre än konkurrentens | Beror på plan och datum |

Det gör det tydligt att öppen information kan förändras.

### Steg 3: Skapa en kort rapportmall

Rapporten kan få en fast struktur:

- Sammanfattning
- Rekommendation
- Viktigaste skillnader
- Osäkerheter
- Nästa kontrollsteg

Det hjälper läsaren att använda resultatet utan att tro att AI:n har fattat beslutet.

### Steg 4: Vänta med automation

Det kan vara lockande att automatisera veckorapporter direkt.

Men innan du automatiserar bör du kunna svara ja på tre frågor:

1. Är arbetsflödet stabilt när jag gör det manuellt?
2. Vet jag vilka källor och kontroller som behövs?
3. Kan jag upptäcka när resultatet blir fel?

Om svaret är nej bör du vänta.

## Vanliga misstag

- **Misstag:** att automatisera för tidigt
    - **Varför det händer:** Automation känns effektivt och modernt.
    - **Hur du undviker det:** Automatisera först när det manuella arbetsflödet fungerar stabilt.

- **Misstag:** att skapa en ny GPT för varje idé
    - **Varför det händer:** Det är enkelt att skapa nya assistenter.
    - **Hur du undviker det:** Använd beslutsregeln: engångsuppgift, Project, GPT eller automation?

- **Misstag:** att aldrig dokumentera ändringar
    - **Varför det händer:** Små ändringar känns oviktiga i stunden.
    - **Hur du undviker det:** Skriv en kort rad i utvecklingsloggen varje gång du ändrar instruktioner, mallar eller arbetssätt.

- **Misstag:** att glömma källkritiken när systemet blir smidigt
    - **Varför det händer:** När assistenten ger snygga svar kan de kännas mer tillförlitliga än de är.
    - **Hur du undviker det:** Behåll ett separat granskningssteg, särskilt vid omvärldsbevakning och produktjämförelser.

## Övningar

### Övning 1: Skapa en förbättringsbacklogg

Gör en tabell med minst fem möjliga förbättringar av din egen AI-Analytiker.

Använd kolumnerna:

- Förbättring
- Nytta
- Risk
- Prioritet

Välj sedan två förbättringar som är värda att göra först.

### Övning 2: Skriv en beslutsregel

Skriv en enkel regel som hjälper dig välja mellan:

- vanlig chatt
- Project
- egen GPT
- automation

Regeln ska vara så tydlig att du kan använda den nästa gång du får en ny idé.

### Övning 3: Gör en utvecklingslogg

Välj en GPT eller promptmall som du redan har arbetat med.

Skriv tre rader i en utvecklingslogg:

1. ett problem du såg
2. en ändring du gjorde eller vill göra
3. hur du ska testa om ändringen hjälpte

### Fördjupning: förenkla systemet

Titta på din systemkarta från kapitel 12.

Markera:

- en del som är viktig
- en del som kan vänta
- en del som kanske bör tas bort

Målet är inte att få ett större system. Målet är att få ett mer användbart system.

## Snabb sammanfattning

- En AI-assistent blir bättre genom små, testbara förbättringar.
- En utvecklingslogg hjälper dig förstå vad som ändrats.
- En förbättringsbacklogg samlar idéer utan att allt måste byggas.
- En beslutsregel hjälper dig välja mellan chatt, Project, GPT och automation.
- Automation bör komma efter att det manuella arbetsflödet fungerar.
- Ett bra AI-system är inte störst, utan lättast att använda och kontrollera.

## Nästa steg

Du har nu en första bokversion med ett praktiskt exempelprojekt och ett extra kapitel om vidareutveckling.

Ett naturligt nästa steg är att granska helheten:

- Är kapitelordningen tydlig?
- Håller boken rätt nivå för nybörjare?
- Finns det tillräckligt många praktiska övningar?
- Behöver några kapitel kortas, förtydligas eller slås ihop?
- Ska boken exporteras till PDF, DOCX eller EPUB?

När du är nöjd med innehållet kan boken gå vidare till granskning och export.
