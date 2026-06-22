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

Warp-Modus: **Complex** (auf 128 BPM Clip, Projekt 123 BPM).

> [!warning] Entscheidender Test: Warp ist die dominante Ursache
> Track testweise auf **128 BPM** hochgedreht → Vocals laufen *ungeworpt* → das Robotische ist **wesentlich besser.** Damit ist klar: der **Time-Stretch (Warp Complex) ist der Hauptfaktor**, nicht Auto Shift. Die Pitch-Tools (Auto Shift, Nectar Correction) **verstärken** die Robotik auf dem schon gewarpten Signal, sind aber nicht die Wurzel. → Fix-Priorität liegt auf dem Stretch-Fundament, nicht auf der Effektkette.

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
- **Pitch Correction (eigenes Modul):** **inaktiv/ausgeschaltet** (im Screenshot nur verwirrend dargestellt) — spielt keine Rolle. Tuning macht allein Auto Shift.
- **EQ 1:** Low-Cut ~80–100 Hz + chirurgische Notches bei ~300 / ~600 / ~3 k
- **Compressor 1:** Solid-State, Peak-Modus, Threshold −19,9 dB
- **EQ 2:** tiefe Absenkung um ~300 Hz (zieht Low-Mid-Körper raus) + Höhen-Anhebung ~6 k → dünn/luftig
- **Voices:** Preset „Airy", Modus Unison, Shape/Intensity/Width gesetzt → harmonisierte Zusatzstimmen/Doubling

> [!info] Korrektur: Nectar Correction war nie aktiv
> Frühere Annahme „zweite gestapelte Pitch-Korrektur" war falsch — das Modul ist ausgeschaltet. Es bleiben **zwei** Robotik-Quellen: ① Warp Complex (−4 %, dominant), ② Auto Shift (MIDI-Hardtune @ 100 % wet). Beide durch Re-Pitch + Formant erledigt.

> [!info] EQ dünnt bewusst aus — polarisierend
> EQ 1 + EQ 2 ziehen Low/Mids stark raus (Scoop ~300 Hz), Höhen bleiben → „dosiger"/Lo-Fi-Richtung. Nimmt zugleich den Proximity-Bauch (C) weg, aber wohl zu weit → trägt zu „zu dünn / fehlende Klarheit" (B/C) bei. Nutzer mag den Lo-Fi-Effekt selbst — Hörer empfinden ihn als zu prozessiert. Geschmacks-/Dosierungsfrage, nicht die Robotik-Wurzel.

**Das ist die komplette Live-Kette** — nur zwei Devices: Auto Shift → Nectar. **Kein separater Auto-Tune:** Auto Shift *ist* die Tune-/Pitch-Engine (Abletons neues MIDI-gesteuertes Device, das die Korrektur komplett übernimmt). Etwaiges RX12-Entstören war Offline-Cleanup am Clip, nicht Teil der Live-Robotik-Kette.

→ Damit ist die Robotik-Wurzel eingekreist: **Warp Complex + Auto Shift** (Nectars Correction nur als Verstärker obendrauf). Kurze Kette = wenige Stellschrauben.

---

## 3) Diagnose & Lösungsansätze

**Ursachen-Ranking (nach 128-BPM-Test):**
1. **Warp Complex (−4 %)** — dominante Wurzel.
2. **Auto Shift** (MIDI-Hardtune, 100 % wet) — Verstärker auf dem gewarpten Signal.
3. EQ-Ausdünnung — Geschmack/Dosierung, nicht Robotik. (Nectar Correction = inaktiv, irrelevant.)

### Fix-Reihenfolge — erst die Wurzel

**A — Warp-Modus auf „Re-Pitch" (zuerst testen, gratis):** Re-Pitch stretcht per Resampling (wie Tape) → **kein Granular-Smear**, also keine Stretch-Robotik. Nebenwirkung: Pitch fällt um den Tempo-Faktor (~0,7 Halbton). Das ist hier **egal**, weil Auto Shift die Tonhöhe danach ohnehin per MIDI auf die Zielnoten zwingt — der Versatz wird neutralisiert. Formanten werden minimal dunkler (~0,7 st) → bei Bedarf via Formant in Auto Shift/Nectar kompensieren. *Wenn das funktioniert, ist das Problem mit einem Klick gelöst.*

**B — Complex → Complex Pro:** elastique Pro, formant-erhaltend; bei nur 4 % Stretch meist nahezu transparent. Klassischer Vocal-Fix, falls A klanglich nicht passt.

**C — Offline-Stretch in besserer Engine** (Melodyne / RX / elastique Pro Bounce): höhere Qualität als Abletons Realtime-Complex; Stem rendern und sauber dehnen.

**D — Vocals auf 123 BPM neu einsingen:** nullt den Warp komplett → Goldstandard. Meiste Arbeit, nur falls A–C nicht reichen.

### Danach: Verstärker nachjustieren (erst nach Warp-Fix neu bewerten)

- **Auto Shift Dry/Wet < 100 %:** etwas echte Stimme reinblenden — aber Vorsicht, der Dry-Anteil hat die *Originaltonhöhe*, passt nur dort, wo Ziel ≈ Original. Eher punktuell.
- **Nectar Correction Strength runter / raus:** zweite Korrektur entschärfen, ggf. ganz weg, wenn Auto Shift schon sauber tuned.
- **EQ-Scoop dosieren:** gegen „zu dünn / fehlende Klarheit" (B/C) etwas Low-Mid zurückgeben — aber nimmt Proximity-Bauch mit, also vorsichtig. Geschmack.

### Ergebnis-Log

**A — Re-Pitch getestet (✅ großer Sprung):** Robotik **fast komplett weg**, wesentlich besser. Nebenwirkung wie vorhergesagt: Klangfarbe **dunkler / „gruseliger"** — Re-Pitch senkt Pitch *und* Formanten (~0,7 st); Auto Shift holt nur die Tonhöhe zurück, die Formanten bleiben unten.

**Folge-Fix — Formant kompensieren:**
- **Auto Shift → Formant** (war 0 st) nach Gehör auf ~**+0,5…+1 st** hoch, bis die Original-Helligkeit zurück ist (knapp unter +1 st gleicht die Re-Pitch-Absenkung aus).
- Bei Bedarf **Nectar → Correction → Formant Shift** ergänzend.
- Nicht übertreiben → sonst dünn/Chipmunk. Ziel: klingt wieder „nach dir", nicht heller als das Original.

**✅ Gelöst:** Re-Pitch + Formant nach oben → „klingt nach mir, aber ohne Robotik". Robotik-Wurzel erledigt, ohne die Effektkette anzufassen. Wandert ins Playbook (**Warp-Entrobot**, **Formant-Korrektur**) → [[Formanten]].

### Noch offen (von der Kette / aus dem Feedback)

Nach dem Robotik-Fix neu zu bewerten:
- **EQ-Ausdünnung (Scoop ~300 Hz):** gegen „zu dünn / fehlende Klarheit" (B/C) etwas Low-Mid zurückgeben — Proximity-Bauch im Auge behalten.
- **Pegel (C: „too loud"):** Vocal-Level im Mix runter — *erst −1 dB getestet, prüfen ob genug.*
- **Strophe zu trocken (C):** *Luft, kein Raum* — die Trockenheit passt thematisch zur Outdoor-Lyric („plätschernde Füße, Zehen voll Sand"), ein echter Raum-Reverb würde widersprechen. Ziel: nur die „klebt-vorn"-Kante nehmen. Ansatz: **Mikro-Ambience** (Pre-Delay ~0, Mix niedrig, Reverb-Return high-pass'en) oder **Slapback-Delay** (60–120 ms, leise) / dezenter **Doubler** statt Hall (→ [[Reverb]]). **Einschränkung:** aktueller Reverb hat Decay-Floor **1 s** → über *niedrigen Mix + hartes High-Damping + kleine Size* unauffällig machen, sonst auf Ableton-Standard-Reverb (geht <1 s) oder Slapback ausweichen. *In Arbeit.*
- **Build-up-Vocals (B, Idee):** Harmonie-Layer + Volume-Automation für mehr Hype.

### Chorus — gleicher Fix, später (zurückgestellt)

> [!tip] Chorus-Vocals: Re-Pitch + Formant, aber umgekehrte Richtung
> Chorus wurde bei **120 BPM** aufgenommen, Projekt 123 → Clip wird **hochgewarpt** (+2,5 %, schneller). Auch hier leichtes Robotik-Problem, aber **geringer** (nur 3 BPM). Eigene Chain, separat von der Strophe.
> - **Fix analog:** Warp → Re-Pitch. Achtung: Re-Pitch pitcht hier nach **oben** → Formanten werden **heller/Chipmunk-Richtung** → Formant-Kompensation diesmal **nach unten** (umgekehrt zur Strophe).
> - **Komplikation:** Chorus besteht aus vielen kleinen Snippet-Clips — Warp-Modus muss auf alle gleichzeitig. Lösungsansatz: alle Clips multi-selektieren und Warp-Modus gemeinsam auf Re-Pitch; Formant-Kompensation einmal zentral im Chorus-Chain-Pitch-Tool. *(Vorgehen noch zu prüfen.)*
> - **Status:** bewusst nach hinten geschoben — erst Strophe fertig.
