# Production Playbook

Track-agnostische Werkzeugkiste. Jeder Eintrag folgt dem Prinzip **Aktion → Wirkung**.
Einträge kommen aus Track-Arbeit oder Referenz-Analysen — Theorie-Hintergrund steht in [[Fundamentals/]], nicht hier.

Namensformat: **[Element]-[Wirkung]** — 1–2 Wörter, Bindestrich, Deutsch. Verweis aus Blueprint: `(→ Playbook: Name)`.

---

## Frequenz & Filter

**Filter-Einflug** (→ [[Filter]]): Element mit komplett geschlossenem LP-Filter einsetzen, über 8 Takte öffnen → sanfter Einflug ohne Energie-Bruch, baut Erwartung auf ohne Lautstärke-Sprung

**Telefon-Filter** (→ [[Filter]]): Bandpass isoliert nur die Mitten eines Elements → klingt weit weg, intim, melancholisch; starker Kontrast-Effekt im Breakdown

**Kick-Hochpass** (→ [[Filter]]): Kick ab ca. 4 Takte vor dem Drop mit HP-Filter belegen → entzieht den Bässen das Fundament, erhöht psychoakustische Wucht beim Drop-Einschlag

**Bongo-Filter** (→ [[Filter]]): Durchlaufende Bongo-Spur an einzelnen Stellen mit LP/HP-Filter belegen statt sie den ganzen Song clear durchlaufen zu lassen → verhindert Ermüdung durch Gleichförmigkeit, schafft hörbare Section-Differenzierung bei einem Element das sonst nie pausiert

## Dynamik & Energie

**Piano-Pump** (→ [[Compressor]]): Piano mit hartem Sidechain-Kompressor gegen die Kick → erzeugt Club-Pumpen, drückt Piano im Rhythmus weg und wieder rein; gibt Drop Energie ohne Frequenz-Konkurrenz

**KI-Preset-Falle** (→ [[Compressor]]): Tools wie Neutron AI analysieren das Signal in Isolation — bei Samples mit starkem Eigencharakter macht die AI zu viele Eingriffe die den Charakter verbiegen und Sidechain-Effekte abschwächen; im Zweifel: Sample pur hören, dann minimal und gezielt eingreifen

**Piano-Grit** (→ [[Distortion]]): Tape Saturation / Saturator auf Piano-Sample legen → fügt Obertöne hinzu, macht Sample dreckiger und durchsetzungsfähiger im Mix ohne Lautstärke zu erhöhen

**Piano-Mono** (→ [[Compressor]]): Piano-Stereo auf Mono summen oder Mid stark betonen → mehr Punch in der Mitte, bessere Club-Kompatibilität; Stereobreite dem Pad-Layer überlassen

**Bass-Glättung** (→ [[Filter]]): Aggressiven 808-Bass durch einfachen Sawtooth ersetzen, mit Low-Shelf gezähmt und hart gegen die Kick sidechained (z.B. Kickstart 2) → Bass bleibt clubtauglich druckvoll, verliert aber die polarisierende Aggressivität eines reinen 808; guter Kompromiss zwischen Club-Punch und Mainstream-Tauglichkeit

## Arrangement & Struktur

**Oktav-Drop** (→ [[Oszillator]]): Melodie-Sample um 1 Oktave nach unten pitchen + dezent filtern → melancholischerer, druckvoller Charakter; erzeugt emotionale Differenz zwischen Strophe und Drop ohne neues Element

**Outro-Schnitt** (→ [[Filter]]): Bass sofort auf dem ersten Outro-Takt stumm schalten → DJ-Mix-Ready; verhindert Frequenz-Kollision mit dem nächsten Track

**DJ-Outro**: Outro startet mit Kick-only + Percussion-Abbau über 16 Takte; Bass weg ab Takt 1, Melodie filtert langsam zu, Percussion und Hats fallen in Stufen weg → gibt dem DJ sauberes Mix-Fenster

**Sofort-Intro** (→ [[Envelopes]]): Intro auf ~8 Takte kürzen und direkt mit Kick + Hauptelement + Hook-Fragment starten statt langem Layer-Aufbau → liefert in den ersten Sekunden Song-Identität; optimiert auf Streaming-Retention (Spotify-Skip-Schwelle), bevor der Hörer wegklickt

## Rhythmus & Groove

**Timing-Versatz** (→ [[Envelopes]]): Melodisches Hauptelement startet laut am Taktanfang, Vocals setzen verzögert im Takt ein → beide konkurrieren nicht für denselben Moment; ermöglicht gleichzeitig präsentes Instrument + präsente Vocals ohne Lautstärke-Kompromiss; erzeugt leichten Call-and-Response-Charakter

**Perc-Puls** (→ [[LFO]]): Sparse Percussion-Pattern alle 4 Takte mit kleiner Höhen-Varianz (z.B. extra Güira-Schläge) abschließen → signalisiert dem Hörer unbewusst den Phrasen-Übergang ohne ein neues Element einzuführen

**Clap-Eskalation** (→ [[Envelopes]]): Erste Drop-Hälfte Clap auf 2+4, zweite Hälfte auf 1+2+3+4 → steigert Energie und Dichte innerhalb des Drops ohne neues Element; lässt den Drop größer wirken als er ist

**Bass-Glide** (→ [[Bass]]): Bass-Stimme auf letztem Achtel jedes Schlags eine Oktave hochpitchen → erzeugt Glide-Übergang zwischen Bassnoten; gibt statischem Pattern Bewegung ohne Harmoniewechsel

**Offbeat-Shake** (→ [[LFO]]): Top-Loop mit betontem Shaker auf dem Offbeat erst in der zweiten Hälfte einer Strophe dazuschalten → bringt House-Vibe und Interesse, ohne die Section von Anfang an zu überladen; markiert zugleich den inneren Wechselpunkt der Strophe

## Raumgefühl & Psychoakustik

**Vocal-Stretch** (→ [[Effekte]]): Eigenes Gesangssample über eine ganze Section strecken + Auto-Tune → erzeugt atmosphärische Tiefe und persönliche Identität ohne melodische Konkurrenz zum Hauptelement

**Hook-Teaser** (→ [[Effekte]]): Ein einzelnes Wort aus dem Songtext herauschoppen und repetitiv im Intro spielen, pro Wiederholung mit leicht variierter Auto-Tune-Melodie → setzt den Hook sofort als Ohrwurm, die Melodie-Varianz verhindert Monotonie bei strenger Wiederholung; gut als Aufmerksamkeits-Anker in einem kurzen Intro

**Washout-Kontrast** (→ [[Reverb]]): Build-up-Piano nass (viel Reverb), Drop-Piano trocken → Drop klingt direkt, nah und physisch; Build-up klingt groß und entrückt; starker psychoakustischer Kontrast ohne Arrangement-Änderung

**Echo-Delay** (→ [[Delay]]): Piano-Delay auf 8tel-Note synchronisiert → jeder Akkord-Hit erzeugt rhythmischen Echo; gibt einem statischen Loop Tiefe und Größe; gut als Eskalation zwischen Drop 1 und Drop 2

**Piano-Pan** (→ [[Chorus]]): Piano-Signal mit tempo-synchronisiertem Auto-Pan belegen → Piano wandert rhythmisch im Stereofeld; gibt identischem Sample in einer Folge-Section eine neue räumliche Dimension

**Piano-Wobble** (→ [[Phaser]]): Subtiler Phaser oder Flanger auf Piano-Sample → erzeugt Timbre-Bewegung im statischen Loop ohne das Sample zu verändern; gut für Strophen-Variation

**Oktav-Layer** (→ [[Oszillator]]): Piano-Sample eine Oktave höher pitchen und leise unter Original mischen → mehr Brillanz und wahrgenommene Größe; kaum hörbar als eigenes Element, spürbar als Gesamteindruck

## Spannung & Release

**Bass-Vakuum** (→ [[Filter]]): Bass stumm schalten zu Beginn des Build-ups → entzieht das Fundament über mehrere Takte, erhöht psychoakustische Wucht beim Drop-Einstieg

**Drop-Stille** (→ [[Envelopes]]): Letzter halber Schlag vor dem Drop komplett stumm — Kick, Snare, Reverb-Tail per Automation hart cutten → absolute Stille erzeugt maximale Erwartungsspannung

**Hook-Saat** (→ [[Envelopes]]): Vocal-Phrase die im Drop wiederholt wird genau in die Stille vor dem Drop legen → Hörer hört den Hook einmal solo, bevor er im Drop explodiert; macht die Wiederholung logisch und emotional statt beliebig

**Kick-Eskalation** (→ [[Envelopes]]): Kick-Pattern von 4/4 auf 8tel, dann 16tel verdichten → steigert Energie ohne BPM-Änderung; signalisiert dem Hörer die Eskalation

**Stutter-Cut** (→ [[Delay]]): Sample in 32tel-Fragmente zerhacken im letzten Build-up-Takt → Energie-Entladungs-Signal, unterscheidet Build-up 2 von Build-up 1

**Washout-Cut** (→ [[Reverb]]): Melodie-Reverb im letzten Build-up-Segment massiv aufdrehen, dann hart cutten → erzeugt Gefühl des „Ertrinkens" und macht die Stille davor tiefer

**Sub-Riser** (→ [[Envelopes]]): Tiefer Sinuston steigt während Bass stumm ist → baut physischen Druck im Raum auf ohne Kick; macht den Drop-Einschlag größer
