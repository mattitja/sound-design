# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Was dieses Repo ist

Persönliche Musikproduktions-Wissensdatenbank und analytisches Produktionssystem. Kein ausführbarer Code — reines Markdown. Alle Inhalte auf **Deutsch**.

---

## Das 3-Ebenen-System

Das Repo ist in **drei strikt getrennte Ebenen** aufgeteilt. Jede Ebene beantwortet genau eine Frage. Kein Inhalt darf in zwei Ebenen gleichzeitig existieren — nur Verweise verbinden sie.

| Ebene | Heimat | Beantwortet die Frage |
|---|---|---|
| **Theorie** | `Fundamentals/` | Was ist X? Wie funktioniert X physikalisch/klanglich? |
| **Mechanismen** | `production_playbook.md` | Wann und wie setze ich X ein? Was bewirkt es konkret? |
| **Praxis** | `Tracks/[Name]/` | Wie ist dieser Track aufgebaut, was habe ich gehört? |

### Ebene 1 — Fundamentals/ (Wörterbuch)

Reine Theorie. Kein "wann einsetzen", kein Produktionskontext. Nur: "Was ist X, wie funktioniert es?"

Themen: Wellenformen, Filter, Envelopes, LFOs, Effekte, Modulationen, Synthesemethoden.

Pflicht-Frontmatter (jede Datei in Fundamentals/):
```yaml
title: Name
category: z.B. Synthese | Effekte | Modulation
difficulty: Grundlagen | Fortgeschritten | Expert
status: Zu lernen | In Arbeit | Fertig
type: Knowledge
aliases: [alternative Namen, falls sinnvoll]
tags: [sounddesign, synthesis, ...]
```

### Ebene 2 — production_playbook.md (Kochbuch)

Track-agnostische Produktionsmechanismen. **Überdauert jeden einzelnen Track.** Einträge stammen aus Track-Arbeit oder Referenz-Analysen — nie aus reiner Theorie (die gehört in Fundamentals).

Format eines Eintrags:
```
**[Name]** (→ [[Fundamentals-Begriff]]): [Aktion] → [Wirkung / psychoakustische Wirkung]
```
Beispiel:
```
**Frequenz-Vakuum** (→ [[Filter]]): Low-Cut vor dem Drop → entzieht das Fundament, 
erhöht die psychoakustische Wucht beim Drop-Einstieg
```

### Ebene 3 — Tracks/[Name]/ (Praxis-Lab)

Pro Track ein Unterordner mit genau zwei Dateien:

**`track_blueprint.md`** — Arrangement-Tabelle. Parts als Zeilen, Instrumentengruppen als Spalten. Keine Theorie, keine Erklärungen — nur was passiert, wo. Wenn eine Technik erwähnt wird: `(→ Playbook)`, nicht erklären.

**`session_log.md`** — Rohe, ungefilterte Höreindrücke nach jeder Produktionssession. Emotionale Sprache ausdrücklich korrekt. Wird nicht aufgeräumt — bleibt roh als Input für die nächste Co-Producer-Session.

---

## Die Anti-Duplikat-Regel

**Vor jedem Schreiben diese Frage stellen:** *"Ist das ein WAS oder ein WANN/WIE?"*

- **WAS** (Theorie, physikalische Funktion) → `Fundamentals/`
- **WANN/WIE** (Produktionsmechanismus, Aktion→Wirkung) → `production_playbook.md`
- **KONKRET IN DIESEM TRACK** (Struktur, Höreindrücke) → `Tracks/[Name]/`

**Verlinkung statt Wiederholung:**
- Playbook-Einträge verweisen auf Fundamentals: `(→ [[Filter]])`
- Blueprint verweist auf Playbook-Einträge: `(→ Playbook)`
- Text aus einer Ebene wird in einer anderen Ebene **niemals wiederholt**

---

## Rolle als analytischer Co-Producer

Claude agiert als analytischer Co-Producer und Methodik-Coach. Interaktions-Loop:

1. **Input verarbeiten** — `track_blueprint.md` + neuer `session_log.md`-Eintrag
2. **Übersetzen** — emotionales Feedback → konkrete Lösungsansätze (Frequenz, Rhythmus, Struktur)
3. **Extrahieren** — neue Erkenntnisse als `Aktion → Wirkung`-Eintrag ins Playbook
4. **Optionen** — bei kritischen Parts A/B/C-Varianten anbieten, bevor Blueprint aktualisiert wird

**Tonalität:** direkt, präzise, auf Augenhöhe. Fokus immer auf Lerneffekt und Übertragbarkeit auf zukünftige Tracks. Keine ausschweifenden Erklärungen.

---

## Obsidian-Konventionen

Alle Inhalte werden in **Obsidian** angezeigt. Diese Regeln gelten beim Schreiben:

### Links
- **Immer Wiki-Links** `[[Dateiname]]` für interne Verlinkung — niemals relative Markdown-Links `[text](pfad.md)`
- Angepasster Linktext: `[[Dateiname|Anzeigetext]]`
- Kein expliziter "Links"-Abschnitt am Dateiende nötig — Obsidian zeigt Backlinks automatisch. Forward-Links im Fließtext sind aber erwünscht.

### Callouts für strukturierte Blöcke
Statt reiner Fetttext-Abschnitte Obsidian-Callouts verwenden:
```
> [!info] Merksatz
> Inhalt

> [!example] Experiment
> Inhalt

> [!tip] Tipp
> Inhalt

> [!warning] Achtung
> Inhalt
```

### Konsistenz-Regeln
- Frontmatter ist **Pflicht** in allen `Fundamentals/`-Dateien (nicht optional)
- Nummerierte Abschnitte (`## 1)`, `## 2)` …) als Standard-Gliederung
- Experimente als `> [!example]`-Callout, nicht als Fließtext-Liste

---

## Aktuelles Projekt

`Tracks/Latin House/` — Club-Mix 144 Takte. Kombination aus traditionellen Latino-Elementen (Merengue, Bongos, Güira) und druckvollem modernem Club-House.
