# Övningar till kapitel 8: Testning och förbättring

## Övning 1: fem testfall för AI-Analytikern

Skapa fem testfrågor:

1. En normal produktjämförelse.
2. En otydlig fråga.
3. En fråga om aktuell information.
4. En fråga som riskerar känslig information.
5. En fråga som ligger utanför assistentens roll.

För varje testfråga, skriv:

- vad du vill testa
- vilket beteende du förväntar dig
- vad som skulle räknas som ett bra svar
- vad som skulle räknas som ett dåligt svar

## Övning 2: bedöm ett svar

Använd en tabell med följande kriterier:

| Kriterium | Poäng 1–3 | Kommentar |
|---|---:|---|
| Relevans | | |
| Tydlighet | | |
| Källkritik | | |
| Osäkerhet | | |
| Avgränsning | | |
| Handlingsbarhet | | |

Skriv sedan en kort slutsats:

- Vad fungerade bäst?
- Vad behöver förbättras?
- Vilken instruktion bör ändras först?

## Övning 3: förbättra med en liten ändring

Välj ett problem från testningen och gör bara en ändring i instruktionen.

Exempel på ändringar:

- lägg till en regel om tidskänslig information
- lägg till en regel om känsliga uppgifter
- skärp outputformatet
- be assistenten fråga när uppgiften är otydlig

Testa sedan samma fråga igen och jämför svaren.

## Fördjupning: skapa en iterationslogg

Skapa en enkel logg:

| Version | Problem | Ändring | Resultat |
|---|---|---|---|
| 0.1 | | | |
| 0.2 | | | |
| 0.3 | | | |

Målet är att kunna se hur assistenten utvecklas över tid.
