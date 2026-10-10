# BRANNBILEN 110

Et brannbilspill for barn fra 6 til 10 år. Kjører i nettleseren på mobil, nettbrett og PC.
Én HTML-fil, ingen installasjon, ingen avhengigheter, ingen sporing.

*A fire truck game for children aged 6–10, in the browser. One HTML file, no install, no dependencies, no tracking. English below.*

**▶ Spill / Play: https://jenoksen.github.io/brannbilen-110/**

<!-- Legg gjerne inn et skjermbilde her: docs/skjermbilde.png -->

---

## Norsk

### Hva går det ut på

Du kjører brannbilen i en liten by sett ovenfra. Når det begynner å brenne, må du komme deg
dit, stoppe og slukke med vannslangen. Hvert hus brenner flere steder, og du må slukke alle
flammene før huset brenner ned. Brenner et hus ned, mister du en brannmannstjerne. Tre
tapte stjerner, så er utrykningen over.

- **Trafikk med regler.** Byen har lyskryss, forkjørsveier med vikepliktskilt, og uskiltede
  kryss der høyreregelen gjelder. Bilene holder avstand, står i kø og venter på grønt.
  Sirenen får dem til å vike i god tid, så den lønner seg å bruke.
- **Døgnsyklus.** Et helt døgn tar fire minutter. Natten er nesten svart, og du ser byen i
  lyset fra frontlyktene, gatelyktene og brannene selv.
- **Vaktordning.** En brannmann går dagvakt, en annen natten. I skumringen og daggryet må du
  kjøre hjem til brannstasjonen og bytte mann — slangen virker ikke før du har gjort det.
- **Vann og bensin.** Vanntanken fylles på røde brannposter. Bensinen varer lenge, men går
  den tom, er runden over. To bensinstasjoner ligger i hvert sitt hjørne av byen.
- **Øvingsmodus** uten stjernetap, for de yngste.

### Kontroller

| | Mobil og nettbrett | PC |
|---|---|---|
| Kjøre / sikte slangen | Virtuell joystick | Piltaster eller WASD |
| Slukke / kjøre videre | SLUKK-knappen | Mellomrom |
| Sirene og blålys | LYD+LYS-knappen | S |
| Bytte joystick-side | Knapp øverst til høyre | H |
| Avslutte runden | Dør-ikonet øverst | Escape |

Joysticken dukker opp der du setter fingeren, på den siden du har valgt. Venstrehendte kan
flytte den til høyre side, enten fra startmenyen eller med knappen under spill.

### Språk

Spillet finnes på norsk og engelsk, og velger språk selv ut fra nettleserens innstilling.
Du kan også velge i startmenyen, eller styre det fra adressen:

```
index.html#en              engelsk
index.html#no              norsk
index.html#venstre         joystick til høyre (for venstrehendte)
index.html#en,venstre      begge deler
```

Valget legges i adressen, så et bokmerke eller en snarvei på hjemskjermen husker det. Ingenting
lagres på enheten.

**Flere språk er veldig velkomment.** Alle tekstene ligger i én tabell øverst i `index.html`,
og det kreves verken byggeverktøy eller programmeringskunnskap for å legge til et språk.
Se [CONTRIBUTING.md](CONTRIBUTING.md).

### Teknisk

- Én selvstendig HTML-fil med HTML5 Canvas og vanilla JavaScript. Ingen rammeverk, ingen
  byggesteg, ingen pakkebehandler.
- Verden tegnes i logisk oppløsning og skaleres opp med heltall, slik at pikselgrafikken
  holder seg skarp. Rullingen skjer i skjermpiksler, så brettet beveger seg jevnt.
- Fast tidssteg på 60 Hz, med frametiden låst til hele steg når skjermen ligger nær 60 Hz.
- Automatisk ytelsesnivå: spillet måler sin egen frametid og trapper ned pikselforhold, lys
  og partikler hvis maskinen ikke henger med — og opp igjen når den gjør det.
- Lyd lages i WebAudio: motor, sirene, vann, brannknitring, biltuting og alarm.
- Ingen `localStorage`, ingen informasjonskapsler, ingen nettverkskall, ingen sporing.
  Spillet fungerer uten internett når filen først er lastet.

### Kjøre lokalt

Last ned `index.html` og åpne den i en nettleser. Det er hele oppskriften.

Vil du heller kjøre den over HTTP:

```bash
git clone https://github.com/jenoksen/brannbilen-110.git
cd brannbilen-110
python3 -m http.server 8000
# åpne http://localhost:8000
```

### Versjoner

`legacy/brannbilen-110-v1.html` er den første versjonen, bevart som den var: bare kjøring,
slukking og stjerner — uten trafikkregler, døgnsyklus, bensin og vaktordning. Den er enklere,
og kan passe bedre for de aller yngste.

### Lisens

[CC BY-NC 4.0](LICENSE) — fri bruk og endring til ikke-kommersielle formål, så lenge opphavet
krediteres. Idé og spilldesign: John Werner Enoksen. Utviklet med Claude (Anthropic).

---

## English

### What it is

You drive a fire truck around a small top-down town. When a fire breaks out, you have to get
there, stop, and put it out with the hose. Each house burns in several places and every flame
must be extinguished before the house burns down. A house burning down costs you a
firefighter's star. Lose three and the call-out is over.

- **Traffic that follows rules.** Signalled junctions, priority roads with give-way signs, and
  unsigned crossings where the right-hand rule applies. Cars keep their distance, queue up and
  wait for green. The siren makes them pull over well in advance, so it pays to use it.
- **Day and night.** A full day lasts four minutes. Night is nearly black, and you see the town
  by your headlights, the street lamps and the fires themselves.
- **Shift changes.** One firefighter works days, another nights. At dusk and dawn you must
  drive home to the station and swap — the hose doesn't work until you have.
- **Water and fuel.** Refill water at red hydrants. Fuel lasts a long time, but running dry
  ends the run. Two petrol stations sit in opposite corners of town.
- **Practice mode** with no stars lost, for the youngest players.

### Controls

| | Phone and tablet | PC |
|---|---|---|
| Drive / aim the hose | Virtual joystick | Arrow keys or WASD |
| Spray / drive on | SPRAY button | Space |
| Siren and blue lights | SIREN button | S |
| Swap joystick side | Button, top right | H |
| Quit the run | Door icon, top | Escape |

The joystick appears wherever you put your thumb, on the side you have chosen. Left-handed
players can move it to the right, from the start menu or with the button during play.

### Languages

Norwegian and English, picked automatically from the browser's language setting. You can also
choose in the start menu, or from the address:

```
index.html#en              English
index.html#no              Norwegian
index.html#venstre         joystick on the right (for left-handers)
index.html#en,venstre      both
```

The choice goes in the address, so a bookmark or home-screen shortcut remembers it. Nothing is
stored on the device.

**More languages are very welcome.** Every string lives in one table at the top of
`index.html`, and adding a language needs no build tools and no programming.
See [CONTRIBUTING.md](CONTRIBUTING.md).

### Technical

- A single self-contained HTML file: HTML5 Canvas and vanilla JavaScript. No framework, no
  build step, no package manager.
- The world is drawn at logical resolution and scaled up by an integer factor, so the pixel art
  stays crisp. Scrolling happens in device pixels, so the board moves smoothly.
- Fixed 60 Hz timestep, with the frame delta snapped to whole steps near 60 Hz.
- Automatic quality levels: the game measures its own frame time and steps pixel ratio, lighting
  and particles down when the machine struggles — and back up when it doesn't.
- Audio is synthesised with WebAudio: engine, siren, water, crackling fire, car horns and alarm.
- No `localStorage`, no cookies, no network requests, no tracking. It works offline once loaded.

### Running locally

Download `index.html` and open it in a browser. That's the whole recipe. Or serve it:

```bash
git clone https://github.com/jenoksen/brannbilen-110.git
cd brannbilen-110
python3 -m http.server 8000
```

### Licence

[CC BY-NC 4.0](LICENSE) — free to use and modify for non-commercial purposes, with credit.
Idea and game design: John Werner Enoksen. Built with Claude (Anthropic).
