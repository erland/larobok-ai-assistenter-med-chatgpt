# Övningar till kapitel 4: Kunskapsfiler och specialiserad kunskap

## Övning 1: Skapa en öppen mini-kunskapsbas

Skapa tre korta dokument:

1. `ordlista-ai-analytikern.md`
2. `mall-produktjamforelse.md`
3. `kallkritisk-checklista.md`

Dokumenten ska bara innehålla öppen och icke-känslig information.

## Övning 2: Testa om GPT:n använder filerna

Fråga AI-Analytikern:

```text
Vilka jämförelsekriterier ska du använda enligt dina kunskapsfiler?
```

Notera om svaret följer din mall.

## Övning 3: Förbättra instruktionen

Lägg till denna princip i GPT:ns instruktioner:

```text
Om relevant information finns i kunskapsfilerna ska du använda den. Om information saknas ska du säga det tydligt och inte gissa.
```

Testa samma fråga igen.

## Övning 4: Gör en kontrollerad produktjämförelse

Välj tre öppet beskrivna produkter eller tjänster. Be AI-Analytikern jämföra dem enligt mallen.

Kontrollera särskilt:
- om kriterierna används
- om osäkerheter markeras
- om aktuella fakta behöver verifieras
- om rekommendationen är tydligt kopplad till användningsfall
