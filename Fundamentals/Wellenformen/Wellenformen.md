---
title: Wellenformen
category: Synthese
difficulty: Grundlagen
status: Zu lernen
type: Knowledge
tags:
- sounddesign
- synthesis
- waveform
- oscillators
---
# Wellenformen – Übersicht

**Wellenformen** sind die grundlegenden Ausgangssignale eines Oszillators. Ihre Form im Zeitbereich bestimmt maßgeblich das **Spektrum** (Obertöne) und damit den Klangcharakter.

## 1) Zeitbereich vs. Frequenzbereich (Denkmodell)
- **Zeitbereich:** Wie die Welle “aussieht” (Sinus, Sägezahn, Rechteck …)
- **Frequenzbereich:** Welche Frequenzen enthalten sind (Grundton + Obertöne)

Faustregel:
- **Je “eckiger”/sprunghafter** die Wellenform, desto **mehr hohe Obertöne** (heller/rauer).
- **Je glatter** die Wellenform, desto **weniger Obertöne** (weicher/purer).

## 2) Die klassischen Grundformen

### [[Sinus]] (Sine)
- Klang: sehr rein, weich, “tonal”
- Spektrum: nur **Grundton**, keine Obertöne (ideal als Sub-Bass)
- Typische Nutzung:
  - Sub-Bass
  - FM/Modulation (saubere Modulatoren)

### Dreieck ([[Triangle]])
- Klang: weich, leicht “hohl”
- Spektrum: nur **ungerade Obertöne**, deren Pegel stark abfällt
- Nutzung:
  - weiche Leads, Flöten-ähnliche Sounds
  - dezente Bass-Sounds

### Sägezahn ([[Saw]])
- Klang: hell, reich, “klassischer Synth”
- Spektrum: **alle Obertöne** (harmonische Reihe)
- Nutzung:
  - Pads, Strings, Brasses
  - Leads, Techno/House-Basics
- Hinweis: sehr filter-freundlich (Cutoff-Modulation wirkt stark)

### Rechteck / Puls ([[Square]] / Pulse)
- Klang: hohl, nasal, klar “digital/retro” je nach Kontext
- Spektrum: vor allem **ungerade Obertöne** (bei 50% Duty)
- Nutzung:
  - Chiptune/Retro, Leads, Bässe
  - mit PWM sehr lebendig

## 3) Pulsbreite & PWM ([[Pulse Width Modulation (PWM)]])
- **Pulse Width/Duty Cycle:** Verhältnis von “High” zu “Low” bei einer Pulswelle
  - 50% = Square (klassisch)
  - <50% oder >50% = “dünner”, nasal, beweglicher
- **PWM:** Modulation der Pulsbreite (oft via [[LFO]])
  - ergibt animierte, “chorusartige” Bewegung ohne echten Chorus

## 4) Varianten & erweiterte Wellenformen

### Noise (Rauschen)
- **White Noise:** gleichmäßige Energie pro Hz (sehr hell)
- **Pink Noise:** weniger Höhenanteil (pro Oktave gleichmäßiger)
- Nutzung:
  - HiHats/Snares, Wind/FX
  - Transienten layern, “Air” in Pads

### [[Wavetable]] / Complex Waves
- bestehen aus vielen spektral unterschiedlichen Einzelwellen (Frames)
- Modulation der Position erzeugt starke Timbre-Bewegung
- Nutzung:
  - moderne Bässe/Leads, morphende Pads, Motion-Sounds

## 5) Wellenformen im LFO-Kontext (Modulation statt Audio)
Viele der gleichen Shapes tauchen bei LFOs wieder auf – die Bedeutung ist dann “Bewegung” statt “Klangfarbe”:

- Sine/Triangle: smoothes Wobble/Vibrato
- Saw/Ramp: zyklische Rise/Fall-Bewegung
- Square: Gate/On-Off
- Random/S&H: “unstet”, glitchy, drift

Verknüpfung: [[LFOs]]

## 6) Praxis: welche Waveform wofür? (Startpunkte)
- **Sub-[[Bass]]:** Sinus (oder Triangle), ggf. Sättigung für Obertöne
- **“Fetter” [[Lead]]/[[Pad]]:** Saw (gern detuned/unison) + Filter
- **Hohle/retro [[Lead]]:** Square/Pulse + (PWM)
- **Percussion/Transient:** Noise-Layer + kurze [[Envelopes]]
- **Moderne Bewegung:** Wavetable + LFO auf Position/Filter

## 7) Häufige Missverständnisse
- “Mehr Obertöne = besser”: Nicht immer. Mehr Obertöne bedeutet auch schnellerer Mix-Konflikt mit Vocals/HiHats.
- “[[Sinus]] ist langweilig”: Oft perfekt als Fundament; Charakter kommt dann durch Distortion/Filter/Layering.
- “PWM = immer Chorus”: PWM kann chorusartig wirken, ist aber spektral/zeitlich etwas anderes als ein echter Chorus-Effekt.

## 8) Experimente (für dein Experiment-Log)
- **Experiment – Spektrum hören:** gleiche Note, gleiche Lautstärke, nacheinander Sine/Triangle/Saw/Square; beschreibe “hell/hohl/rau”.
- **Experiment – Filter reagiert auf Waveform:** gleiche Filter-Envelope, einmal mit Sine vs. Saw; Wirkung vergleichen.
- **Experiment – PWM:** Pulse + langsamer LFO auf Pulse Width; Tiefe/Rate dokumentieren.
- **Experiment – Noise als Transient:** Noise sehr kurz mit Envelope auf Amp; unter Kick/Snare layern.

## 9) Links & verwandte Notizen
- [[Oszillator]]
- [[Envelopes]]
- [[LFO]]
- [[Filter]]