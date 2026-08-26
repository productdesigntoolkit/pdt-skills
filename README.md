# pdt-skills

Claude-Skills für die Methoden des Product Design Toolkit. Ein Skill pro Methode, flach abgelegt, Dateiname gleich der Skill-ID.

**Rolle in der Kette:** Diese Ablage ist die Quelle. Von hier werden die Skills nach `explorer/skills/` gespiegelt, wo der Explorer sie zum Download anbietet, und beim Packen ins Claude-Plugin übernommen.

```
pdt-templates/{id}.yaml   →   pdt-skills/{id}.md   →   explorer/skills/{id}.md
   Feldstruktur                   Dialogführung          Auslieferung
```

## Aufbau eines Skills

```markdown
---
name: pdt:{id}
description: {Methode} nach {Autor}: {was sie leistet}
argument-hint: "[optional: Produkt, Unternehmen oder Kontext]"
---

# PDT: {Name}

## Methode          Quelle, Space, Einordnung, wann einsetzen, verwandte Methoden
## Deine Rolle      Haltung des Agenten, worauf er besteht
## Prozess          Einführung, Kontext erfragen, ein Block je Feld aus dem YAML
## Output-Format    Dateiname und Markdown-Vorlage
## Nach dem Output  Empfehlung für den nächsten Schritt
## Sprache          Antwortsprache folgt dem Nutzer
```

Die `description` trennt Methode und Leistung mit einem Doppelpunkt, nicht mit einem Gedankenstrich.

## Ändern

Checkliste über alle Repos: `gitbook-methods/ADDING-A-METHOD.md`.
Konsistenzprüfung: `explorer/check-methods.py`, prüft unter anderem, ob diese Ablage und `explorer/skills/` deckungsgleich sind.

## Lizenz

CC BY-NC-SA 4.0, Ralph Hutter, productdesigntoolkit.net
