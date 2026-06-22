# Latin House – Externes Feedback

Rohes, vollständiges Feedback zum Track. Archiv — die destillierte, handlungsrelevante Fassung steht im [[track_blueprint|Blueprint]] unter „Feedback".

Neues Feedback als neue Datums-Sektion (`## TT.MM.JJJJ`) anlegen, darin pro Reviewer ein `###`-Block mit Server-Quelle. **Immer die Versions-ID** (= Ableton-Dateiname, z.B. `dembow4_3`) angeben, auf die sich die Runde bezieht.

Unter jedem Post ein **Status-Block**, der die handlungsrelevanten Punkte verfolgt: `🔲 offen` / `✅ gelöst` (mit Version, in der's gefixt wurde). Wird beim Bearbeiten eines Punkts direkt aktualisiert.

> [!info] Referenzier-Regel
> Jede Feedback-Runde gilt für genau eine Versions-ID. Ein Kritikpunkt ist nur dann offen, wenn er nicht in einer **späteren** Version adressiert wurde. Abgleich: Feedback-Version gegen „Aktuelle Version" im [[track_blueprint|Blueprint]]-Header prüfen; primär gegen den Live-Zustand des Blueprints abgleichen (zeigt den aktuellen Stand). Reicht das nicht, `git log`/`git diff` als „was-änderte-sich-seitdem"-Quelle nutzen — **kein** manuelles Versions-Log führen (dupliziert die Git-History).

---

## 21.06.2026 — Version `dembow4_3`

**Gestellte Fragen:** Voice, Build-ups, Trompeten, Mix
**Quellen:** Discord *We Suck At Producing* (A, C) · Discord *In the Mix* (B)

### A — PHNX (`prodphnx`)

14 y/o Producer · LA · Boom-Bap · „Looking to Connect & Learn" · he/him
Server: *We Suck At Producing* · [Nachrichtenlink](https://discord.com/channels/417029410622013441/417381800717975564/1518355843593142303)

> I haven't ever listened to latin house before, so I wasn't too sure what to expect. It's a super unique vibe and does remind me of Latin music that I listen to. The track has a great energy and the piano loop is definitely my favorite part. Even though I don't speak the language, it's very catchy and I like the hook.
>
> Regarding your questions,
>
> The Voice: Your voice fits the song well, I like your tone, but I feel like the voice feels too 'robotic' at times. It sounds like there is too much processing or pitch correction happening. Maybe try pulling back on the effects and letting your natural voice come through - it would probably feel more authentic.
>
> The Build-Ups: The build-ups work well and keep the energy moving smoothly.
>
> The Trumpets: I really like the trumpets - they definitely add to the Latin energy I was looking for. They fit the vibe perfectly.
>
> Honestly, I think the mix is well done. Everything sounds balanced, and nothing feels like it's fighting for space or getting buried. It's a clean sounding track, however you should take this advice with a grain of salt because I'm still learning mixing and the things about it. From a listeners perspective, I would say that it is really good for your first track ever.

**Status (Stand: dembow4_3):**
- ✅ Gelöst (Fix gesetzt, ab nächstem Bounce): Vocals „robotic" — Ursache war der Warp (Complex), nicht die Effekte. Fix: Warp → Re-Pitch + Formant-Kompensation (siehe [[vocal_fix]])
- *Build-ups, Trompeten, Mix: positiv, keine Aktion*

### B — john skibidi (`hirasawafan`)

20 y/o · Lofi · komponiert, mixt und mastert selbst · etwas erfahrener
Server: *In the Mix* · [Nachrichtenlink](https://discord.com/channels/485460967224770590/808674439561609216/1518469281262731264)
[SoundCloud](https://soundcloud.com/monstajohnx) · [Instagram](https://instagram.com/daytripp1ng) · [Spotify](https://open.spotify.com/intl-de/artist/7s2JSBxb8ZGp860f20qdkv?si=CqTKGUhyTPuOA5hTY6eY0Q&nd=1)

> Congrats on making your first track! i have never really listened to this kind of genre before. So can take my words with a pinch of salt. Answering your question:
>
> The melody does fits the music. But yes, I feel like it's a bit too processed. I would like it if there's slightly less effects on the vocals. Also I feel like it's lacking some clarity? might need to play around wit the EQ a bit.
>
> It feels like a build up to me. Maybe to build the hype more, I would try to layer the vocals with harmonies. maybe try volume automation throughout the build up also.
>
> fits well. I feel like it compliments your track and make it unique and stand out. To me, it sounds fine.
>
> Not my kind of genre, but I'd say this would appeal to people who listens to this. It also sounds like what you're trying to convey as well. beachy, summer vibes. So good job on that 👍

**Status (Stand: dembow4_3):**
- ✅ Gelöst (Fix gesetzt, ab nächstem Bounce): Vocals zu prozessiert — Robotik-Wurzel war der Warp; Re-Pitch + Formant (siehe [[vocal_fix]])
- 🔲 Offen: Vocals fehlt Klarheit → EQ (Nectar-Scoop ggf. zu weit)
- 🔲 Offen (Idee): Build-up-Vocals mit Harmonien layern + Volume-Automation für mehr Hype
- *Trompeten, Vibe: positiv, keine Aktion*

### C — Lévy 🎶 (`levyleibnitzloiusius`)

Erfahrener, anderes Genre
Server: *We Suck At Producing* · [Nachrichtenlink](https://discord.com/channels/417029410622013441/618112554635362345/1518679924393906317)
[Spotify](https://open.spotify.com/intl-fr/album/1ROp6Z319QxwhUo6qxwOhr) · [SoundCloud](https://soundcloud.com/leiblouis-music/tracks)

> btw i don't know if he told you that but the voice is a bit too loud and it might have been rec too close to the mic (proximity effect) it feels pretty dry too sometimes chorus are fine, verse feels dry

**Status (Stand: dembow4_3):**
- 🔲 Offen: Stimme stellenweise zu laut → Pegel runter
- 🔲 Offen: zu nah am Mikro / Proximity-Effekt → Low-Mids per EQ zähmen
- 🔲 Offen: Strophe zu trocken → Raum/Reverb (Chorus okay)
