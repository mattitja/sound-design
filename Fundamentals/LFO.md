---
title: LFOs
category: Synthese
difficulty: Grundlagen
status: Zu lernen
type: Knowledge
core_framework: true
created: 2026-02-17
tags:
- sounddesign
- modulation
- lfo
---

# LFOs (Low Frequency Oscillators) – Übersicht

Ein **LFO** (Low Frequency Oscillator) ist ein Oszillator im **niederfrequenten Bereich**, der typischerweise **nicht hörbar** ist, sondern als **Modulationsquelle** dient. Er verändert einen oder mehrere Parameter **über die Zeit** – zyklisch, rhythmisch oder frei laufend.

## 1) Wofür nutzt man LFOs?
Typische Ziele/Parameter (Modulationsziele):

- **Lautstärke** → Tremolo
- **Filter-Cutoff/Resonanz** → Wobble, Movement, Sweeps
- **Tonhöhe** → Vibrato, Sirenen, “Analog Drift”
- **Panning** → Auto-Pan
- **[[Wavetable]]-Position / PWM / FM-Amount** → “Lebendige” Timbre-Bewegung
- **FX-Parameter** (Chorus/Flanger/Phaser/Delay-Time/Mix) → Motion, Pulsing, Glitches

Merksatz: 
- **[[Envelopes]] = einmaliger Verlauf pro Note/Trigger**, 
- **LFO = wiederholte Bewegung** (meist periodisch).

## 2) Kernparameter eines LFO (Bedienelemente verstehen)
- **Rate/Frequency:** Wie schnell der Zyklus ist  
  - in **Hz** (frei) oder **Sync** zu Tempo (z.B. 1/4, 1/8T, 1/16)
- **Shape/Waveform:** Form der Modulation (siehe unten)
- **Depth/Amount:** Modulationsstärke (Wie weit wird der Parameter bewegt?)
- **Offset/Bias:** Verschiebt die LFO-Kurve nach oben/unten (zentriert vs. einseitig)
- **Phase:** Startposition innerhalb der Wellenform
- **Delay/Fade-In:** LFO startet verzögert oder blendet langsam ein
- **Smoothing/Glide:** Rundet harte Kanten ab (wichtig bei Square/Random)
- **Key Tracking / Rate Tracking:** LFO-Geschwindigkeit abhängig von gespielter Tonhöhe (nicht überall vorhanden)

## 3) Wellenformen & musikalischer Charakter
- **Sine (Sinus):** weich, natürlich → Vibrato, subtile Bewegung
- **Triangle (Dreieck):** linearer Auf/Abstieg → gleichmäßige Sweeps
- **Saw (Sägezahn):** schneller Fall/Anstieg → “Riser”-artige Bewegung, Pumping
- **Ramp (umgekehrter Saw):** schneller Anstieg/Abfall → Variation von Sweeps
- **Square (Rechteck):** an/aus → Trance-Gates, harte Switching-Modulation
- **Sample & Hold / Random:** zufällige Stufen → “Analog”-Wackeln, Glitch, Sci-Fi
- **Custom/Draw:** eigene Kurven → komplexe Grooves, Sequencer-ähnliche Modulation

## 4) Sync vs. Free-Running
- **Tempo-Sync:** LFO-Zeit basiert auf musikalischen Notenwerten  
  - gut für **rhythmische Modulation** (Sidechain-ähnliches Pumping, Gates)
- **Free-Running (Hz):** unabhängig vom Tempo  
  - gut für **organische Bewegung** und “nicht exakt wiederholende” Feelings

## 5) Trigger-Modi (sehr wichtig für Verhalten im Kontext)
Je nach Synth/Plugin heißen diese Modi unterschiedlich, die Idee ist aber meist:

- **Free-Run:** LFO läuft dauerhaft weiter (jede Note “steigt irgendwo ein”)
- **Retrigger (per Note-On):** LFO startet bei jeder Note gleich (präziser Groove/Attack-Design)
- **One-Shot:** LFO läuft **einmal** durch (LFO wird zur “Envelope-ähnlichen” Modulation)
- **Poly vs. Mono LFO:**  
  - **Mono:** ein LFO für alle Stimmen (Akkorde bewegen sich gemeinsam)  
  - **Poly:** pro Stimme eigener LFO (Akkorde “leben”/phasen sich auseinander)

## 6) LFOs vs. Envelopes (Zusammenhang)
- **Envelope:** zeitlicher Verlauf mit Phasen (z.B. ADSR), oft an Note-On/Off gebunden  
- **LFO:** periodische Modulation, oft synchronisierbar, kann aber auch **one-shot** sein  
- Kombi-Idee: Envelope setzt den “Makro-Verlauf”, LFO liefert “Mikro-Bewegung”.

Verknüpfung: [[Envelopes]]

## 7) Modulations-Routing (wie man systematisch denkt)
Ein praktisches Modell:

- **Source** (LFO) → **Destination** (z.B. Cutoff) → **Amount** (Tiefe) → **Polarity** (uni-/bipolar) → **Scaling** (z.B. via Mod Wheel/Velocity)

Wichtige Begriffe:
- **Bipolar:** Modulation geht um einen Mittelpunkt (z.B. -1 bis +1)
- **Unipolar:** Modulation geht nur in eine Richtung (z.B. 0 bis +1)
- **Modulation Matrix:** zentrale Routing-Tabelle in vielen Synths

## 8) Typische “Rezepte” (Startpunkte)
- **[[Vibrato]] (Pitch):**
  - Shape: Sine
  - Rate: 4–7 Hz (free) oder schnell synced
  - Depth: sehr klein, ggf. via Mod Wheel steuerbar
- **Tremolo (Amp):**
  - Shape: Sine/Triangle für weich, Square für Gate
  - Sync: 1/8 oder 1/16
- **[[Wobble]] Bass (Filter):**
  - Shape: Triangle/Square/Custom
  - Sync: 1/4 → 1/16 je nach Stil
  - Depth: groß, Resonanz nach Geschmack
- **Analog Drift (Pitch/Filter minimal):**
  - Shape: Random (smooth) oder sehr langsamer Sine
  - Rate: sehr langsam (z.B. 0.05–0.3 Hz)
  - Depth: extrem subtil

## 9) Häufige Fehler / Debugging
- **Zu viel Depth:** Sound wirkt “krank” oder out-of-tune (besonders bei Pitch)
- **Falscher Trigger-Modus:** Groove “schwimmt”, weil Free-Run statt Retrigger
- **Zu harte Kanten:** Square/Random ohne Smoothing erzeugt Klicks bei Cutoff/Amp
- **Zu viele Ziele gleichzeitig:** lieber eine Modulation klar hörbar machen und dann layern

## 10) Experimente (Vorschläge für deinen Experiment-Log)
- **Experiment – LFO Shapes hören lernen:** gleiche Rate/Depth, nur Shape wechseln; beschreibe den Charakter.
- **Experiment – Retrigger vs Free-Run:** Akkorde spielen, Unterschied in “Zusammenhalt” dokumentieren.
- **Experiment – Uni- vs Bipolar:** Cutoff-Modulation einmal zentriert, einmal nur nach oben; Unterschiede notieren.
- **Experiment – One-Shot LFO als Envelope:** Filter-Pluck nur mit One-Shot LFO nachbauen.

## 11) Offene Fragen (zum Weiterarbeiten)
- Wann klingt **sync** musikalischer als **free** (und umgekehrt)?
- Welche Parameter eignen sich für **subtile** vs. **dramatische** LFO-Modulation?
- Wie lassen sich LFOs “performbar” machen (Mod Wheel/Macro/Aftertouch)?

## 12) Links & verwandte Notizen
- [[Envelopes]]
- [[Filter]]
- [[Oszillator]]
- (Optional: eigene Notiz) [[Modulation Matrix]] / [[Modulationsquellen & -ziele]]