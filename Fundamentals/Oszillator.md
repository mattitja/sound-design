---
title: Oszillator
category: Synthese
difficulty: Grundlagen
status: In Arbeit
type: Knowledge
aliases: [Oszillatoren, Oscillator]
tags: [sounddesign, synthesis, oscillator]
---

# Oszillatoren im Sound-Design

Oszillatoren sind die grundlegenden Klangerzeugungseinheiten in der Synthesizer-Technologie und bilden das **Herzstück** jedes elektronischen Sounds.

## Grundlegende Wellenformen

- **Sinuswelle:** Die purste Wellenform ohne Obertöne, erzeugt einen weichen, fundamentalen Klang
- **Sägezahnwelle (Sawtooth):** Enthält alle **harmonischen Obertöne**, klingt hell und voll - ideal für Streicher und Bass-Sounds
- **Rechteckwelle (Square):** Enthält nur ungerade Obertöne, erzeugt einen hohlen, nasalen Klang
- **Dreieckswelle (Triangle):** Ähnlich der Sinuswelle, aber mit sanften Obertönen - weicher als Square, voller als Sinus
- **Pulswelle:** Variable Square-Wave mit einstellbarer Pulsbreite (PWM) für lebendige, modulierbare Klänge

## Wichtige Parameter

- **Frequenz/Pitch:** Bestimmt die Tonhöhe des erzeugten Signals
- **Pulsbreite (PWM):** Bei Pulswellen - verändert das Verhältnis zwischen hohem und niedrigem Pegel
- **Phase:** Startpunkt der Wellenform, wichtig bei Mehrfach-Oszillatoren
- **Sync:** Synchronisiert einen Oszillator mit einem anderen für harmonisch komplexe Klänge

## Oszillator-Typen

- **Analog-Oszillatoren:** Erzeugen kontinuierliche elektrische Signale mit natürlichen Schwankungen
- **Digital-Oszillatoren:** Berechnen Wellenformen mathematisch mit präziser Stabilität
- **Wavetable-Oszillatoren:** Spielen gespeicherte Wellenformen ab und können zwischen ihnen morphen
- **FM-Oszillatoren:** Modulieren die Frequenz eines Oszillators durch einen anderen für komplexe Obertonstrukturen
- **Granular-Oszillatoren:** Zerlegen Audio in winzige Partikel für experimentelle Texturen

## Anwendungsbereiche

- **Subtraktive Synthese:** Oszillatoren erzeugen obertonreiche Signale, die dann durch [[Filter]] geformt werden
- **FM-Synthese:** Oszillatoren modulieren einander für metallische, glockenartige Klänge
- **Additive Synthese:** Mehrere Sinuswellen-Oszillatoren werden kombiniert
- **Sound-Design:** Basis für Pads, Leads, Bässe und Effekte

## Oszillator-Modulation

Oszillatoren können durch verschiedene Quellen moduliert werden:

- **LFO (Low Frequency Oscillator):** Langsame Modulation für Vibrato, Tremolo oder rhythmische Effekte
- **[[Envelopes]]:** Zeitbasierte Modulation der Tonhöhe (Pitch Envelope)
- **Velocity:** Spielstärkeabhängige Kontrolle
- **Modulation-Wheel:** Manuelle Echtzeitkontrolle

## Multi-Oszillator-Techniken

- **Unison:** Mehrere leicht verstimmte Oszillatoren für breitere, vollere Klänge
- **Detune:** Verstimmung zwischen Oszillatoren für Schwebungen und Dicke
- **Layering:** Kombination verschiedener Wellenformen für komplexe Klangfarben
- **Hard Sync:** Ein Oszillator erzwingt den Reset eines anderen für aggressive, metallische Sounds

## Zusammenspiel mit Filtern

Oszillatoren und [[Filter]] arbeiten eng zusammen: Während Oszillatoren das Rohmaterial erzeugen, formen Filter den Klang durch gezielte Frequenzbearbeitung. Diese Kombination bildet die Grundlage der subtraktiven Synthese.