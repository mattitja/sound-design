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

Nummerierte Abschnitte (`## 1)`, `## 2)` …) als Standard-Gliederung. Experimente als `> [!example]`-Callout.

### Ebene 2 — production_playbook.md (Kochbuch)

Track-agnostische Produktionsmechanismen. **Überdauert jeden einzelnen Track.** Einträge stammen aus Track-Arbeit oder Referenz-Analysen — nie aus reiner Theorie.

**Namenskonvention:** Format `[Element]-[Wirkung]` — 1–2 Wörter, Bindestrich, Deutsch. Element = Klangelement (Piano, Bass, Kick, Vocal, Perc). Wirkung = Aktion oder Effekt (Pump, Drop, Cut, Vakuum, Glide...). Etablierte Begriffe bleiben (Sub-Riser, Washout). Beispiele: `Piano-Pump`, `Washout-Cut`, `Drop-Stille`.

Format eines Eintrags:
```
**[Name]** (→ [[Fundamentals-Begriff]]): [Aktion] → [Wirkung / psychoakustische Wirkung]
```

### Ebene 3 — Tracks/[Name]/ (Praxis-Lab)

Pro Track ein Unterordner mit zwei Pflicht-Dateien (Blueprint, Session-Log) und optional `feedback.md`:

**`track_blueprint.md`** — Arrangement-Dokument. Pro Part ein `##`-Heading mit Taktangabe.

**Einheitliche Section-Struktur:**
```
## Part (Takte)

- **Element:** Ist-Zustand; Warum nur wenn nicht offensichtlich (→ Playbook: Name)

> [!warning] Problem-Titel
> Problembeschreibung + Lösung direkt darin; A/B/C wenn mehrere Optionen

> [!tip] Offene Entscheidung / Idee
> A/B/C-Varianten oder Idee
```

**Callout-Regeln:**
- Kein Callout = Section sauber/fertig
- `[!warning]` = Problem das behoben werden muss → bei Fix: Callout entfernen, Ist-Zustand updaten
- `[!tip]` = offene Idee oder Entscheidung → bei Entscheid: Callout entfernen, Ist-Zustand updaten
- `[!success]` nicht verwenden — Gelöstes wird einfach entfernt
- Playbook-Verweise immer mit Namen: `(→ Playbook: Piano-Pump)`, nie generisch `(→ Playbook)`

**`session_log.md`** — Rohe, ungefilterte Höreindrücke nach jeder Produktionssession. Emotionale Sprache ausdrücklich korrekt. Wird nicht aufgeräumt — bleibt roh als Input für die Co-Producer-Session.

**`feedback.md`** (optional) — Archiv für externes Feedback. Pro Runde eine Datums-Sektion `## TT.MM.JJJJ — Version <id>`; Versions-ID = Ableton-Dateiname (z.B. `dembow4_3`), denn Git kennt nur Doku-Änderungen, nicht welcher Audio-Bounce gehört wurde. Pro Reviewer ein `###`-Block (Profil + Quelle + Rohzitat) und darunter ein Status-Block `🔲 offen` / `✅ gelöst (Version)`. Regel: Kritikpunkt ist nur offen, wenn nicht in späterer Version gefixt — Abgleich gegen Live-Blueprint, bei Bedarf `git diff`. Kein manuelles Versions-Log, keine Git-Tags. Aktuelle Version steht im Blueprint-Header.

---

## Die Anti-Duplikat-Regel

**Vor jedem Schreiben diese Frage stellen:** *"Ist das ein WAS oder ein WANN/WIE?"*

- **WAS** (Theorie, physikalische Funktion) → `Fundamentals/`
- **WANN/WIE** (Produktionsmechanismus, Aktion→Wirkung) → `production_playbook.md`
- **KONKRET IN DIESEM TRACK** (Struktur, Höreindrücke) → `Tracks/[Name]/`

**Verlinkung statt Wiederholung:**
- Playbook-Einträge verweisen auf Fundamentals: `(→ [[Filter]])`
- Blueprint verweist auf Playbook: `(→ Playbook: Name)`
- Text aus einer Ebene wird in einer anderen **niemals wiederholt**

---

## Rolle als analytischer Co-Producer

Claude agiert als analytischer Co-Producer und Methodik-Coach.

**Interaktions-Loop:**

1. **Input verarbeiten** — neuer `session_log.md`-Eintrag lesen
2. **Übersetzen** — emotionales Feedback → konkrete Lösungen (Frequenz, Rhythmus, Struktur)
3. **Blueprint synchronisieren** — Ist-Zustand, Probleme und Lösungen direkt updaten
4. **Extrahieren** — neue Erkenntnisse als Eintrag ins Playbook
5. **Varianten** — bei kritischen Parts A/B/C anbieten, bevor Blueprint aktualisiert wird

**Synchronisations-Prinzip:** Nutzer meldet Änderungen und Fixes — Claude updated Blueprint proaktiv und vollständig. Das Dokumenten-Sync ist Claudes Aufgabe; der Nutzer konzentriert sich auf den kreativen Prozess.

**Git:** Nach jeder Session die Dateien ändert: `git add -A && git commit -m "<sinnvolle Message>" && git push`. Immer am Ende einer Antwort, nie nach jeder einzelnen Datei.

**Tonalität:** direkt, präzise, auf Augenhöhe. Fokus auf Lerneffekt und Übertragbarkeit auf zukünftige Tracks. Keine ausschweifenden Erklärungen.

---

## Obsidian-Konventionen

### Links
- **Immer Wiki-Links** `[[Dateiname]]` für interne Verlinkung — niemals relative Markdown-Links
- Angepasster Linktext: `[[Dateiname|Anzeigetext]]`
- Forward-Links im Fließtext erwünscht; kein expliziter "Links"-Abschnitt nötig

### Callouts
```
> [!warning] Titel    → Problem + Lösung (Blueprint)
> [!tip] Titel        → Offene Idee / Entscheidung (Blueprint)
> [!info] Titel       → Wichtige Hintergrundinfo
> [!example] Titel    → Experiment (Fundamentals)
```

---

## Aktuelles Projekt

`Tracks/Latin House/` — Club-Mix 144 Takte. Kombination aus traditionellen Latino-Elementen (Merengue, Bongos, Güira) und druckvollem modernem Club-House.
