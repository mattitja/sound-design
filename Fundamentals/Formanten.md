---
title: Formanten
category: Synthese
difficulty: Grundlagen
status: Fertig
type: Knowledge
aliases: [Formant, Formants, Formant Shift]
tags: [sounddesign, vocals, pitch, resampling]
---

# Formanten

## 1) Was ist ein Formant?

Eine Stimme (oder jedes akustische Instrument) besteht aus zwei unabhängigen Schichten:

- **Tonhöhe (Pitch):** Schwingungsrate der Quelle — bei Stimme die Frequenz der Stimmbänder. Das ist die gesungene Note.
- **Klangfarbe (Timbre):** Welche Obertöne der Resonanzraum (bei Stimme: Rachen, Mund, Nase) aus diesem Grundton verstärkt. Die verstärkten Frequenzbänder heißen **Formanten**.

Formanten sind feste Resonanz-Frequenzbereiche des Vokaltrakts. Sie hängen von **Form und Größe** des Resonanzraums ab, nicht von der gesungenen Note. Sie sind der „Fingerabdruck" einer Stimme.

## 2) Wofür Formanten hörbar verantwortlich sind

- **Vokal-Identität:** Die ersten zwei Formanten (F1, F2) bestimmen, ob ein Laut als „A", „E", „O" gehört wird — unabhängig von der Tonhöhe.
- **Körpergröße/Charakter:** Tiefe Formanten = großer, dunkler Resonanzraum (große Person). Hohe Formanten = kleiner Raum (Kind, helle Stimme).
- **Wer-ist-das-Erkennung:** Die individuelle Formantenlage macht, dass eine Stimme nach *dieser* Person klingt.

## 3) Pitch vs. Formant sind unabhängig — und warum das wichtig ist

Tonhöhe und Formanten kann man getrennt verschieben:

- **Pitch verschoben, Formant fix** → andere Note, gleiche Klangfarbe (sauberes Pitch-Shifting mit Formant-Erhalt).
- **Pitch fix, Formant verschoben** → gleiche Note, anderer Vokal-/Stimmcharakter.
- **Beide zusammen verschoben** (= naives Resampling, „Tape-Effekt") → „Chipmunk" (hoch) bzw. „Dämon" (tief), weil der Fingerabdruck mitwandert, obwohl er nicht sollte.

> [!info] Resampling/Re-Pitch zieht beide zusammen
> Ein Sample schneller/langsamer abspielen (Tape, Vinyl, Ableton-Warp-Modus **Re-Pitch**) ändert Pitch **und** Formanten im selben Verhältnis. Will man nur das Tempo (oder nur die Tonhöhe) ändern, ohne die Klangfarbe zu verbiegen, braucht es formant-erhaltendes Processing oder eine nachträgliche **Formant-Kompensation** (Formant-Regler gegenläufig verschieben).

## 4) Wo der Formant-Regler in Tools sitzt

- **Ableton Auto Shift:** eigener `Formant`-Parameter (in st) + `F. Follow`.
- **iZotope Nectar (Pitch/Correction):** `Formant Shift` + `Scale`.
- **Antares Auto-Tune, Little AlterBoy, Melodyne:** jeweils dedizierter Formant-/Throat-Parameter.

Praktische Anwendung aus der Track-Arbeit → siehe Playbook (**Warp-Entrobot**, **Formant-Korrektur**).
