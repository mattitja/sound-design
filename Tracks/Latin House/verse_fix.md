# Latin House – Verse-Fix (Arbeitsdokument)

Separates Arbeits-Doc für die **Strophe**. Bezug: [[feedback]] (23.06., Cooper, Version `dembow4_3`). Schwester-Doc zu [[vocal_fix]] (dort: Robotik/Pitch erledigt) — hier geht's um **Raum, Breite und Frequenzfülle** im Verse, *ohne* die Outdoor-Szene zu zerstören.

> Status: **offen / in Arbeit.** Noch keine Fixes gesetzt — erst Ist-Stand + Strategie aufdröseln, dann committen.

---

## 1) Der Kern-Konflikt (warum das nicht trivial ist)

Cooper (technisch versiertester Reviewer) zielt mit **drei** Punkten direkt auf die Strophe. Sein Hauptverschreibung: *„too dry → add delay/reverb."*

**Aber:** Die Trockenheit des Verse ist **bewusst und gewollt**, aus zwei Gründen:

1. **Die Szene.** Der Text malt eine Draußen-Natur-Szene: *„Plätschernde Füße, Zehen voll Sand / Dös auf der Liege, Drink in der Hand."* Strand, offene Luft. Akustische Wahrheit: **offene Luft = keine Reflexionen, kein Tail** — der trockenste natürliche Raum überhaupt. Ein Hall auf dieser Stimme würde die Szene *kaputtmachen* (klingt nach Halle/Indoor, nicht nach Strand).
2. **Der Kontrast.** Build-up/Refrain („ich will noch nicht heim") läuft bewusst **extrem breit + hallig + wabernd**. Der trockene, intime Verse ist der *Gegenpol* dazu — das ist Teil des Vocal-Arcs ([[track_blueprint|Blueprint]]: „Verse = Stimme im Fokus … Build-up = Stimme wabernd"). Trockenheit *macht* hier dramaturgische Arbeit.

→ **Cooper wörtlich auszuführen (Reverb auf den Verse) wäre falsch.** Die Aufgabe: herausfinden, *was Cooper wirklich gehört hat*, und das beheben — ohne Szene und Kontrast zu opfern.

---

## 2) Was Cooper wirklich hört (Symptom vs. Verschreibung)

Cooper sagt „dry" — aber im selben Satz „mono":

> „The vocal is also too dry in sections like that intro verse. I would fill it out with some delay/reverb and also suggest creating other takes (maybe harmonies) to pan and fill out the stereo field **since the higher mids and treble are pretty much mono there**."

Er bündelt **zwei verschiedene Defekte in ein Wort**:

| Was er sagt | Was real los ist | Achse |
|---|---|---|
| „too dry" | zu **nah/eng/leblos** (Proximity-Nähe, klebt vorn) | Tiefe |
| „pretty much mono" | Stereofeld **schmal** in oberen Mitten/Höhen | Breite |

„Reverb" ist nur Coopers *Verschreibung* gegen das Gefühl von Leere. Der **echte** Mangel ist nicht „zu wenig Hall", sondern **„zu mono + zu eng"**. Und *das* lässt sich beheben, ohne die Stimme nass zu machen.

> [!info] Karol-G-Kompass
> Referenz-Vibe (Nutzer): Karol-G-Verses sind **trocken, präsent, vorne** — und trotzdem breit + lebendig. Die Breite kommt **nicht aus Hall**, sondern aus **Doubles/Harmonien hart L/R gepannt**, ggf. Micro-Slapback + Sättigung. Genau das ist Coopers eigener „pan harmonies"-Punkt — nur dass *das* der Fix ist, nicht sein „add reverb".

---

## 3) Die dritte Cooper-Front: die Piano-Lücke (instrumental, nicht vokal)

> „the piano in the first verse is low-passed to the point it almost disappears … if you were to open that filter a bit, the track could feel repetitive … Instead, some **synth stabs with a long reverb** could do a lot to fill this space … any instrument to help fill out that gap in the **mid and upper mid range**."

Wichtig: Cooper **rät vom Filter-Öffnen ausdrücklich ab** — der Loop läuft fast den ganzen Song, offen würde er zu repetitiv. Seine Lösung ist **additiv**: ein *neues* Element in der Mid/Upper-Mid-Lücke.

→ Das ist die saubere Stelle für Coopers langen Reverb: **auf einem Instrument (Synth-Stab), nicht auf der Stimme.** Cooper kriegt seinen Raum, die Stimme bleibt draußen + trocken.

---

## 4) Ist-Zustand der Strophe (Blueprint Strophe 1, Takte 17–32)

- **Piano:** 1 Oktave runter + LP-Filter → laut Cooper „almost disappears" (Mid/Upper-Mid fast weg).
- **Vocals:** entrobotisiert (Re-Pitch + Formant, [[vocal_fix]]); Low-Cut, Höhen leicht an, Proximity-Bauch raus, −1 dB; **dezente Ambience („Luft, kein Raum")** sitzt schon drauf.
- **Stereofeld:** obere Mitten/Höhen der Stimme = **mono** (Coopers Befund).
- **Kick** 4/4, **Bass** Viertel G–A–B–D, **Bongos** + ab Takt 25 Top-Loop/Shake.

> [!warning] Offen zu prüfen am neuen Bounce
> Cooper hörte `dembow4_3` — **vor** der Vocal-Session (22.06.). Die „Luft, kein Raum"-Ambience war da noch nicht drauf. → Am neuen Bounce gegenchecken: Reicht die dezente Ambience gegen das „dry"-Gefühl, oder bleibt der Eindruck? Erst danach entscheiden, wie viel von unten dazukommt.

---

## 5) Lösungs-Strategie (Vocal bleibt trocken — Breite + Frequenz statt Tiefe/Hall)

Leitsatz: **Die Stimme bleibt draußen.** Wir gehen Coopers *echtes* Problem (mono/eng/leer) mit Breite und Frequenzfülle an, nicht mit Raum.

- **A — Breite ohne Raum (Kern-Fix gegen „mono"):** 1–2 zusätzliche Vocal-Takes oder Harmonien, hart L/R gepannt. Löst Coopers Mono-Punkt *und* füllt obere Mitten — bleibt staubtrocken. Der Karol-G-Move. *(= Cooper-Punkt „pan harmonies", = Feedback B)*
- **B — Leben ohne Room (optional, testen):** dezenter **Slapback-Delay** statt Reverb (sehr kurz, kaum Feedback, mono-kompatibel). Gibt Dimension/„Leben", klingt nicht nach Halle. Nur wenn A allein noch zu nackt wirkt.
- **C — Frequenzlücke separat (instrumental, ohne die Stimme anzufassen):** **Synth-Stabs mit langem Reverb** gegen die weggefilterte Piano-Lücke. Hier wohnt Coopers langer Hall — auf dem *Instrument*. Füllt Mid/Upper-Mid, ohne den Loop zu öffnen (kein Repetitions-Problem).

**Reihenfolge:** A + C zuerst (decken Coopers Substanz: Breite + Frequenz). B nur, falls danach noch was fehlt.

> [!tip] Was wir bewusst NICHT tun
> Kein Reverb-Tail auf die Verse-Stimme (zerstört Strand-Szene + Kontrast zum Refrain). Kein Filter-Öffnen am Piano (Cooper warnt selbst vor Repetition). Trockenheit ist hier **Feature, kein Bug** — künftiges „too dry"-Feedback nicht reflexartig umsetzen, sondern gegen diesen Konflikt prüfen.

---

## 6) Offene Entscheidungen / nächste Schritte

- [ ] **Neuen Bounce gegenchecken:** ob die „Luft, kein Raum"-Ambience das „dry"-Gefühl schon ausreichend nimmt (Cooper hörte sie noch nicht).
- [ ] **A umsetzen:** Harmonie-/Double-Takes aufnehmen + hart pannen. Wie viele Stimmen? Echte zweite Aufnahme vs. künstliches Doubling?
- [ ] **C umsetzen:** Synth-Stab-Sound wählen (was passt klanglich zum Merengue-Piano?) + langer Reverb. Welcher Rhythmus — auf der Piano-Lücke oder als Gegenstimme?
- [ ] **B nur bei Bedarf:** Slapback testen, A/B gegen „ohne".
- [ ] Bei Erfolg: Playbook-Eintrag-Kandidat **`Vocal-Trockenheit`** (Außen-Szene → Breite statt Hall) + Blueprint Strophe 1 um „trocken ist gewollt"-Begründung ergänzen.
