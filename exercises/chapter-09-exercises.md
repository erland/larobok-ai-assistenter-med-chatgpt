# Övningar till kapitel 9: Vanliga misstag och dåliga designmönster

## Övning 1: identifiera en för bred GPT

Utgå från denna instruktion:

```text
Du är en hjälpsam AI som kan hjälpa mig med research, skrivande, strategi, analys, marknadsföring, produktval, planering och beslutsfattande.
```

Svara på:

1. Vilka delar gör assistenten för bred?
2. Vilka uppgifter passar AI-Analytikern?
3. Vilka uppgifter bör flyttas till en annan assistent?
4. Hur kan instruktionen skrivas om med tydligare rollgräns?

## Övning 2: skriv en bättre osäkerhetsregel

Skriv en regel som säger hur AI-Analytikern ska hantera information som kan vara inaktuell.

Regeln bör nämna:

- priser
- produktfunktioner
- villkor
- källor
- när användaren bör verifiera informationen

## Övning 3: skapa en felsökningschecklista

Skapa en kort checklista som du kan använda när en GPT svarar dåligt.

Checklistan ska innehålla minst sex frågor, till exempel:

- Är rollen tydlig?
- Är uppgiften för bred?
- Finns outputformat?
- Finns gränser?
- Finns krav på osäkerhet?
- Behöver uppgiften delas i steg?

## Övning 4: dela upp AI-Analytikern

Skapa tre specialiserade varianter av AI-Analytikern:

1. Research-GPT
2. Jämförelse-GPT
3. Rapport-GPT

För varje variant, skriv:

- huvuduppgift
- vad den inte ska göra
- ett enkelt outputformat
- en startfråga

## Fördjupning: skapa en anti-pattern-logg

Skapa en enkel logg med dessa kolumner:

| Anti-pattern | Hur det märktes | Trolig orsak | Förbättring |
|---|---|---|---|

Fyll i minst tre rader baserat på egna test av AI-Analytikern.
