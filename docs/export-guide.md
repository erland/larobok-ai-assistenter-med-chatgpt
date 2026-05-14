# Exportguide

All export ska utgå från `docs/export-metadata.yaml` och kapitelordningen i metadatafilen.

## Markdown
Sammanfoga kapitlen i ordningen som anges i metadatafilen.

## EPUB
- Använd metadata för titel, undertitel, författare, språk, identifierare, datum och rättigheter.
- Skapa inte en separat innehållsförteckning som textkapitel.
- Använd luftig CSS för brödtext, rubriker, listor, tabeller och kodblock.

## PDF
- Skapa en innehållsförteckning i början, före inledningen.
- Rendera Markdown som riktig formatering.
- Använd titel och författare från metadata.

## DOCX
- Rendera rubriker, fetstil, kursiv, listor, tabeller och kodblock som riktig dokumentformatering.
