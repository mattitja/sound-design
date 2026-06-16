# Production Playbook

Track-agnostische Werkzeugkiste. Jeder Eintrag folgt dem Prinzip **Aktion → Wirkung**.
Einträge kommen aus Track-Arbeit oder Referenz-Analysen — Theorie-Hintergrund steht in [[Fundamentals/]], nicht hier.

---

## Frequenz & Filter

**LP-Filter-Einflug** (→ [[Filter]]): Element mit komplett geschlossenem LP-Filter einsetzen, über 8 Takte öffnen → sanfter Einflug ohne Energie-Bruch, baut Erwartung auf ohne Lautstärke-Sprung

**Telefon-Effekt** (→ [[Filter]]): Bandpass isoliert nur die Mitten eines Elements → klingt weit weg, intim, melancholisch; starker Kontrast-Effekt im Breakdown

**Kick-HP im Build-up** (→ [[Filter]]): Kick ab ca. 4 Takte vor dem Drop mit HP-Filter belegen → entzieht den Bässen das Fundament, erhöht psychoakustische Wucht beim Drop-Einschlag

## Dynamik & Energie

**Piano-Sidechain zur Kick** (→ [[Compressor]]): Piano mit hartem Sidechain-Kompressor gegen die Kick → erzeugt Club-Pumpen, drückt Piano im Rhythmus weg und wieder rein; gibt Drop Energie ohne Frequenz-Konkurrenz

**AI-Mixing-Preset auf Charakter-Samples vermeiden** (→ [[Compressor]]): Tools wie Neutron AI analysieren das Signal in Isolation — bei Samples mit starkem Eigencharakter (z.B. Merengue-Piano) macht die AI zu viele Eingriffe die den Charakter verbiegen und Sidechain-Effekte abschwächen; im Zweifel: Sample pur hören, dann minimal und gezielt eingreifen

**Saturator auf Sample-Piano im Drop** (→ [[Distortion]]): Tape Saturation / Saturator auf Piano-Sample legen → fügt Obertöne hinzu, macht Sample dreckiger und durchsetzungsfähiger im Mix ohne Lautstärke zu erhöhen

**Piano mono summen im Drop** (→ [[Compressor]]): Piano-Stereo auf Mono summen oder Mid stark betonen → mehr Punch in der Mitte, bessere Club-Kompatibilität; Stereobreite dem Pad-Layer überlassen

## Arrangement & Struktur

**Oktav-Trick (Strophe)** (→ [[Oszillator]]): Melodie-Sample um 1 Oktave nach unten pitchen + dezent filtern → melancholischerer, druckvoller Charakter; erzeugt emotionale Differenz zwischen Strophe und Drop ohne neues Element

**Bass-Cut im Outro** (→ [[Filter]]): Bass sofort auf dem ersten Outro-Takt stumm schalten → DJ-Mix-Ready; verhindert Frequenz-Kollision mit dem nächsten Track

**DJ-Outro-Struktur**: Outro startet mit Kick-only + Percussion-Abbau über 16 Takte; Bass weg ab Takt 1, Melodie filtert langsam zu, Percussion und Hats fallen in Stufen weg → gibt dem DJ sauberes Mix-Fenster

## Rhythmus & Groove

**Intra-Takt Timing-Versatz Instrument/Vocal** (→ [[Envelopes]]): Melodisches Hauptelement startet laut am Taktanfang, Vocals setzen verzögert im Takt ein → beide konkurrieren nicht für denselben Moment; ermöglicht gleichzeitig präsentes Instrument + präsente Vocals ohne Lautstärke-Kompromiss; erzeugt leichten Call-and-Response-Charakter ohne echtes Call-and-Response-Arrangement

**Percussion-Phrasen-Varianz** (→ [[LFO]]): Sparse Percussion-Pattern alle 4 Takte mit kleiner Höhen-Varianz (z.B. extra Güira-Schläge) abschließen → signalisiert dem Hörer unbewusst den Phrasen-Übergang ohne ein neues Element einzuführen

**Clap-Eskalation innerhalb des Drops** (→ [[Envelopes]]): Erste Drop-Hälfte Clap auf 2+4, zweite Hälfte auf 1+2+3+4 → steigert Energie und Dichte innerhalb des Drops ohne neues Element; lässt den Drop größer wirken als er ist

**808-Oktav-Glide** (→ [[Bass]]): 808-Sample auf letztem Achtel jedes Schlags eine Oktave hochpitchen → erzeugt Glide-Übergang zwischen Bassnoten; gibt statischem Pattern Bewegung ohne Harmoniewechsel

## Raumgefühl & Psychoakustik

**Gestreckes Vocal-Sample als Texture-Layer** (→ [[Effekte]]): Eigenes Gesangssample über eine ganze Section strecken + Auto-Tune → erzeugt atmosphärische Tiefe und persönliche Identität ohne melodische Konkurrenz zum Hauptelement

**Reverb Raum-Kontrast Build-up vs. Drop** (→ [[Reverb]]): Build-up-Piano nass (viel Reverb), Drop-Piano trocken → Drop klingt direkt, nah und physisch; Build-up klingt groß und entrückt; starker psychoakustischer Kontrast ohne Arrangement-Änderung

**8tel-Delay sync auf Piano** (→ [[Delay]]): Piano-Delay auf 8tel-Note synchronisiert → jeder Akkord-Hit erzeugt rhythmischen Echo; gibt einem statischen Loop Tiefe und Größe; gut als Eskalation zwischen Drop 1 und Drop 2

**Auto-Pan sync auf Piano** (→ [[Chorus]]): Piano-Signal mit tempo-synchronisiertem Auto-Pan belegen → Piano wandert rhythmisch im Stereofeld; gibt identischem Sample in Section 2 eine neue räumliche Dimension

**Phaser / Flanger für Piano-Animation** (→ [[Phaser]]): Subtiler Phaser oder Flanger auf Piano-Sample → erzeugt Timbre-Bewegung im statischen Loop ohne das Sample zu verändern; gut für Strophen-Variation

**Oktave-drüber-Layer** (→ [[Oszillator]]): Piano-Sample eine Oktave höher pitchen und leise unter Original mischen → mehr Brillanz und wahrgenommene Größe; kaum hörbar als eigenes Element, spürbar als Gesamteindruck

## Spannung & Release

**Frequenz-Vakuum im Build-up** (→ [[Filter]]): Bass stumm schalten zu Beginn des Build-ups → entzieht das Fundament über mehrere Takte, erhöht psychoakustische Wucht beim Drop-Einstieg

**Stille vor dem Drop** (→ [[Envelopes]]): Letzter halber Schlag vor dem Drop (z.B. „4 und") komplett stumm — Kick, Snare, Reverb-Tail per Automation hart cutten → absolute Stille erzeugt maximale Erwartungsspannung

**Drop-Hook in der Pre-Drop-Stille säen** (→ [[Envelopes]]): Vocal-Phrase die im Drop wiederholt wird genau in die Stille vor dem Drop legen → Hörer hört den Hook einmal solo, bevor er im Drop explodiert; macht die Wiederholung logisch und emotional statt beliebig

**Kick-Dichte im Build-up** (→ [[Envelopes]]): Kick-Pattern von 4/4 auf 8tel, dann 16tel verdichten → steigert Energie ohne BPM-Änderung; signalisiert dem Hörer die Eskalation

**Stutter-Effekt vor Drop** (→ [[Delay]]): Sample in 32tel-Fragmente zerhacken in letztem Build-up-Takt → Energie-Entladungs-Signal, unterscheidet Build-up 2 von Build-up 1

**Sub-Riser im Build-up** (→ [[Envelopes]]): Tiefer Sinuston steigt/fällt während Bass stumm ist → baut physischen Druck im Raum auf ohne Kick; macht den Drop-Einschlag größer

**Reverb-Washout vor Drop** (→ [[Reverb]]): Melodie-Reverb im letzten Build-up-Segment massiv aufdrehen, dann hart cutten → erzeugt Gefühl des „Ertrinkens" und macht die Stille davor tiefer
