# Latin House – Vocal-Fix (Arbeitsdokument)

Separates Debugging-Doc für das Vocal-Problem. Bezug: [[feedback]] (21.06., Version `dembow4_3`). Wenn gelöst → Erkenntnis ggf. ins [[production_playbook]], Status in [[feedback]] auf ✅.

---

## 1) Das Problem (aus dem Feedback destilliert)

Drei unabhängige Reviews, ein Cluster: **die Vocals.** Alles andere (Vibe, Piano, Trompeten, Mix) wurde gelobt. Die Symptome:

- **„Robotic" / zu viel Processing + Pitch-Correction** (A + B) — der künstliche Charakter kippt von „gewollter Auto-Tune-Vibe" in „maschinell". Klingt nach Artefakten, nicht nach Sound-Design.
- **Fehlende Klarheit** (B) — Stimme wirkt undefiniert/verwaschen, Hinweis Richtung EQ.
- **Zu laut** (C) — Stimme steht zu weit vorn im Mix.
- **Zu nah am Mikro / Proximity-Effekt** (C) — Nahbesprechung pumpt die Low-Mids auf, Stimme klingt dick/bauchig.
- **Strophe zu trocken, Chorus okay** (C) — der Strophe fehlt Raum; im Chorus/Drop maskiert der Kontext (mehr Effekte, dichteres Arrangement) das Problem.

**Meine Arbeitshypothese (noch zu prüfen):** Das ist nicht *ein* Fehler, sondern eine Kette, die sich gegenseitig verstärkt — und sie trifft v.a. die **Strophe**:

1. Nah am Mikro aufgenommen → Low-Mid-Bauch + zu präsent/laut → Stimme klebt vorn im Gesicht.
2. Trocken (kein Raum) → es gibt nichts, was die Stimme einbettet → jedes Processing-Artefakt liegt nackt frei.
3. Mehrfache Pitch-Tools gestapelt (Auto-Shift fürs Shiften + iZotope + Auto-Tune) → Artefakte summieren sich → „robotic".

→ Trocken + nah + laut + gestapeltes Pitch = die Artefakte werden *hörbar gemacht* statt versteckt. Der Chorus ist fine, weil dort der dichtere Kontext + mehr Effekte die gleiche Stimme maskieren.

Das ist aber nur die Theorie aus dem Feedback. Was wirklich los ist, sehen wir erst an der echten Chain.

---

## 2) Ist-Zustand der Vocal-Chain

### Fundament: Aufnahme-Tempo ≠ Track-Tempo

- Vocals wurden bei **128 BPM** aufgenommen, der Track läuft inzwischen auf **123 BPM** (bleibt so).
- Die Vocals werden also um ~4 % verlangsamt (Faktor 123/128 ≈ 0,96) ins Tempo gewarpt.
- **Befund:** Schon mit *allen* Plugins aus ist im reinen Vocal-Sample ein leicht robotisches Verlangsamungs-Artefakt hörbar — kommt vom Time-Stretch/Warp selbst, nicht von der Effektkette.

> [!warning] Wurzel könnte tiefer liegen als gedacht
> Das „robotic" aus dem Feedback entsteht (mindestens teilweise) schon beim Warpen — *bevor* irgendein Pitch-Tool greift. Das verschiebt den Fokus: nicht nur Effekte zurückfahren, sondern zuerst das Stretch-Fundament sauber kriegen (z.B. Warp-Modus prüfen, oder Vocals neu auf 123 BPM einsingen).

### Plugin-Kette

**1. Auto Shift (Ableton)** — MIDI-gesteuert, treibt die Stimme auf die Noten der MIDI-Spur „Verse Mel".
Settings aus dem Screenshot:
- **MIDI On**, Routing „Verse Mel", **Post FX**
- **Mono**, **Voices 4**, **Glide 0.00 ms**
- Input-Detection: **Mid**, Root D −20 ct, Gain 0.0 dB, L 34.8 ms
- **Attack 20 ms / Release 20 ms**, Note Latch, PB 6 st
- **Pitch 0 st, Fine 0, Formant 0 st, F. Follow 0 %**
- Vibrato 0 ct (aus), Rate 6 Hz, „Natural"
- Mod Routing: alles None
- **Dry/Wet 100 %**

**Pitch-Distanz:** meist nur wenige Halbtöne neben dem Original → noch im Bereich der echten Stimmfarbe. Vereinzelt werden sehr hohe Noten (die so nie gesungen wurden) via Vocal-Shift/Auto-Tune weiter weggepitcht — **laut Nutzer aber nicht das Kernproblem**, denn das Robotische ist auch da, wo fast richtig gesungen wurde.

> [!warning] Prime Suspect: Auto Shift voll resynthetisiert
> Zwei Settings erklären „robotic auch bei richtig gesungenen Stellen":
> 1. **Dry/Wet 100 %** → man hört *ausschließlich* das resynthetisierte Signal, kein Anteil der echten Stimme. Genau dort sitzen die synthetischen Artefakte.
> 2. **MIDI-gesteuert + Mono** → die Stimme wird hart auf MIDI-Notenwerte gezwungen (Hardtune-Charakter), die natürliche Pitch-Mikro-Bewegung verschwindet → quantisiert = robotisch.
>
> Das ist unabhängig von der Pitch-Distanz und passt deshalb zum Symptom. Test (kommt später): Dry/Wet runter, Formant beobachten — erst die Chain vollständig auslegen.

> [!info] Zwischen-Befund: Auto Shift an, Nectar aus
> Auto Shift solo (Nectar bypassed) klingt **noch robotischer** als mit Nectar an. → bestätigt: **Auto Shift ist die primäre Robotik-Quelle.** Nectar *mildert* sie eher, statt sie zu erzeugen — v.a. durch das Ausdünnen der Low/Mids (s.u.).

**2. iZotope Nectar Advanced** — interne Modulkette:
- **Auto-Level** (Learn aktiv), Output-Pegel ~−14,5 dB; Pan C, Width 8, Limiter am Ende
- **Modul-Reihenfolge:** Gate → EQ 1 → De-Esser → Compressor 1 → EQ 2 → Voices → Dimension (*aus*) → Limiter; Analog-Delay (*aus*)
- **Pitch Correction (eigenes Modul):** Strength **100**, Speed **20**, Key **D-Dur**, Transpose 0, Formant Shift 0 / Scale 10, Register Medium
- **EQ 1:** Low-Cut ~80–100 Hz + chirurgische Notches bei ~300 / ~600 / ~3 k
- **Compressor 1:** Solid-State, Peak-Modus, Threshold −19,9 dB
- **EQ 2:** tiefe Absenkung um ~300 Hz (zieht Low-Mid-Körper raus) + Höhen-Anhebung ~6 k → dünn/luftig
- **Voices:** Preset „Airy", Modus Unison, Shape/Intensity/Width gesetzt → harmonisierte Zusatzstimmen/Doubling

> [!warning] Dritte Robotik-Quelle: zweite gestapelte Pitch-Korrektur
> Nectars **Correction (Strength 100, Speed 20)** läuft *zusätzlich* zu Auto Shifts MIDI-Hardtune. Zwei harte Tuner in Serie → Artefakte addieren sich. Damit haben wir drei gestapelte Robotik-Quellen, alle **vor** dem eigentlichen Auto-Tune: ① Warp Complex (−4 %), ② Auto Shift (MIDI-Hardtune @ 100 % wet), ③ Nectar Correction (Strength 100).

> [!info] EQ dünnt bewusst aus — polarisierend
> EQ 1 + EQ 2 ziehen Low/Mids stark raus (Scoop ~300 Hz), Höhen bleiben → „dosiger"/Lo-Fi-Richtung. Nimmt zugleich den Proximity-Bauch (C) weg, aber wohl zu weit → trägt zu „zu dünn / fehlende Klarheit" (B/C) bei. Nutzer mag den Lo-Fi-Effekt selbst — Hörer empfinden ihn als zu prozessiert. Geschmacks-/Dosierungsfrage, nicht die Robotik-Wurzel.

**Das ist die komplette Live-Kette** — nur zwei Devices: Auto Shift → Nectar. **Kein separater Auto-Tune:** Auto Shift *ist* die Tune-/Pitch-Engine (Abletons neues MIDI-gesteuertes Device, das die Korrektur komplett übernimmt). Etwaiges RX12-Entstören war Offline-Cleanup am Clip, nicht Teil der Live-Robotik-Kette.

→ Damit ist die Robotik-Wurzel eingekreist: **Warp Complex + Auto Shift** (Nectars Correction nur als Verstärker obendrauf). Kurze Kette = wenige Stellschrauben.

---

## 3) Diagnose & Lösungsansätze

> *Folgt, sobald die Chain steht.*
