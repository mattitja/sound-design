---
title: Reverb
category: Effekte
difficulty: Grundlagen
status: Fertig
type: Knowledge
aliases: [Hall, Reverberation, Nachhall]
tags: [sounddesign, effekte, raum, mixing]
---

# Reverb (Nachhall)

## 1) Was ist Reverb?

Reverb simuliert, wie Schall in einem Raum an Flächen reflektiert wird, bis er verklingt. Aus einem trockenen Signal entsteht so der Eindruck, dass die Quelle in einem realen Raum steht. Das Gehör liest aus dem Reverb v.a. **Raumgröße, Material und Distanz** der Quelle.

## 2) Die wichtigen Parameter

- **Decay / Reverb Time (RT60):** Wie lange die Fahne braucht, um zu verklingen. **Der dominanteste Größen-Eindruck** — kurz (0,3–0,6 s) = kleiner Raum/Luft, lang (1,5–3 s+) = Halle/Kirche.
- **Pre-Delay:** Lücke zwischen Trockensignal und einsetzendem Reverb (ms). Großes Pre-Delay → Quelle bleibt vorn/nah, Raum wirkt groß und getrennt; kleines → Quelle „klebt" am Raum.
- **Early Reflections (ER):** Die ersten, noch einzeln erkennbaren Rückwürfe naher Flächen. Sie erzeugen den konkreten „Zimmer/Wand"-Eindruck. Viel ER = klar definierter Raum.
- **Diffusion:** Wie schnell die Reflexionen zu einem dichten Klangteppich verschmelzen. Hoch = glatt/wolkig, niedrig = körnig/einzelne Echos.
- **Size:** Simulierte Raumgröße (skaliert ER-Abstände und Decay-Charakter).
- **Damping:** Höhen (manchmal auch Tiefen) verklingen schneller — simuliert absorbierende Materialien (Teppich, Vorhänge) vs. harte (Kachel, Stein).
- **Mix / Dry-Wet (oder Send-Pegel):** Anteil Reverb. Bestimmt wahrgenommene Distanz und wie auffällig der Effekt ist.
- **Width (Stereobreite):** Wie breit die Fahne im Stereofeld liegt. Moderate Breite legt „Luft" um eine mittige Quelle, ohne sie selbst zu verbreitern — gut gegen mono-trockene, vorn klebende Signale. Zu viel = diffus/„swimmy" und in Mono phasenanfällig (immer gegenchecken).
- **Saturation (Sättigung):** Harmonische Verzerrung auf der Fahne → wärmer, „analoger", und **präsenter bei gleichem Pegel** (man kann weniger wet fahren). Sparsam: zu viel macht den Tail grindig und auffällig.

## 3) Reverb-Typen (grob)

- **Room:** kurz, viele ER → natürlicher kleiner Raum.
- **Hall:** lang, diffus → groß, entrückt.
- **Plate:** dichte, helle Kunst-Fahne ohne klare ER → klassisch für Vocals/Snare.
- **Spring:** federnd, charakterstark (Gitarre/Dub).
- **Ambience / Early-Reflections-only:** sehr kurz, kaum Tail → gibt „Luft" ohne hörbaren Raum.

## 4) „Luft, kein Raum" — Trockenheit nehmen ohne Raumeindruck

Wenn eine Stimme zu trocken/zu nah („klebt vorn") sitzt, aber ein Raum thematisch nicht passt (z.B. Outdoor-Lyric), will man **Luft statt Raum**. Der Raum-Eindruck kommt v.a. aus **Decay + Early Reflections + Pre-Delay** — also genau die klein halten:

- Decay sehr kurz (0,3–0,5 s), Pre-Delay ~0, **Mix niedrig** (man soll ihn mehr spüren als hören).
- **Reverb-Return per High-Pass** beschneiden (unter ~300–400 Hz raus) → keine wabbernde Tiefe.
- Highs ggf. dämpfen → Fahne sitzt unauffällig „unter" dem Signal.
- Test: Bypass an/aus — ohne klingt's tot, mit klingt's lebendig, aber keine benennbare Fahne.

**Alternativen ohne Raum:** kurzer **Slapback-Delay** (60–120 ms, leise) oder **Doubler/Stereo-Spread** geben Dimension/Lebendigkeit ganz ohne Hall.

Anwendung im Track → siehe Playbook (Raumgefühl-Einträge) und [[Formanten]] für die Pitch-Seite der Vocal-Bearbeitung.
