# Bidra til BRANNBILEN 110 / Contributing

Takk for at du vil bidra. Det mest verdifulle bidraget er **et nytt språk** — spillet er laget
for barn, og barn leser best på sitt eget morsmål.

*Thanks for wanting to help. The most valuable contribution is **a new language**.*

---

## Legge til et språk / Adding a language

Du trenger ingen byggeverktøy og ingen programmeringskunnskap. Alt skjer i én fil.

*No build tools and no programming knowledge needed. Everything happens in one file.*

### 1. Finn språktabellen

Åpne `index.html` i en teksteditor og søk etter `SPRAAKDRAKT`. Rett under ligger tabellen
`STRINGS` med ett avsnitt per språk — `no` for norsk og `en` for engelsk.

### 2. Kopier `en`-blokken

Kopier hele blokken fra `en: {` til og med den avsluttende `}`, lim den inn rett etter, og sett
inn et komma mellom dem. Bytt så nøkkelen til språkkoden din — to bokstaver etter
[ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes), for eksempel `de`,
`fr`, `pl`, `sv`, `uk` eller `so`.

```js
en: {
  langName:'English',
  play:'PLAY',
  ...
},

de: {
  langName:'Deutsch',
  play:'SPIELEN',
  ...
}
```

### 3. Oversett høyresiden

Oversett bare teksten mellom fnuttene. La nøklene til venstre stå urørt.

- `langName` skal være språkets eget navn, slik det skrives på det språket.
- `{v}`, `{n}` og `{side}` er plassholdere som fylles med tall eller ord mens du spiller.
  De må stå igjen i teksten, men kan flyttes dit setningen trenger dem.
- Nøkler du ikke oversetter, faller automatisk tilbake til norsk. Du kan altså levere en
  halvferdig oversettelse, og noen andre kan fullføre den.
- Spillet heter `BRANNBILEN 110` på alle språk. `title1` og `title2` bør stå som de er.

### 4. Hold tekstene korte

Tekstene tegnes på et lite lerret, mange av dem i store varselbokser. Spillet krymper for lang
tekst automatisk, men da blir den vanskeligere å lese for et barn. Sikt mot å holde deg
innenfor lengden på den norske eller engelske versjonen.

### 5. Prøv den

Åpne `index.html` i en nettleser og legg språkkoden din bak en skigard i adressen:

```
index.html#de
```

Språket dukker også opp som en knapp i startmenyen av seg selv — du trenger ikke registrere
det noe annet sted. Gå gjennom startmenyen, «Slik spiller du», «Om spillet», avsluttdialogen
og en hel runde, og se etter tekst som er klipt av eller som fortsatt står på norsk.

### 6. Send inn

Lag en pull request med én fil endret: `index.html`. Skriv gjerne i beskrivelsen hvilket språk
det gjelder og om noe mangler.

Har du ikke lyst til å bruke Git? Opprett heller en sak (issue) med oversettelsene som tekst,
så legger vi dem inn.

---

## Andre bidrag / Other contributions

- **Feil og forslag:** opprett en sak. Si gjerne hvilken enhet og nettleser det gjelder, og
  hva som skjedde — det er som regel nok til å finne feilen.
- **Kode:** hold deg til prinsippene under. Spillet skal fortsatt være én fil som kan sendes
  som vedlegg og åpnes med dobbeltklikk.

### Prinsipper for koden

1. **Én fil.** Alt ligger i `index.html`. Ingen avhengigheter, ingen byggesteg, ingen
   pakkebehandler.
2. **Ingen lagring og ingen nettverkskall.** Spillet er laget for barn og skal ikke lagre noe
   på enheten eller sende noe noe sted. Valg som skal huskes, legges i adressen.
3. **Barnevennlig vanskegrad.** Straff skal komme med varsel og god tid, aldri brått.
4. **Ytelse måles, ikke antas.** Endrer du noe som kan påvirke bildeflyten, så mål før og
   etter. Spillet skal gå i 60 bilder i sekundet på en vanlig mobil.
5. **Kommentarer** kan skrives på norsk eller engelsk. Begge deler er velkomment.

---

## English summary

Open `index.html`, find `SPRAAKDRAKT`, copy the whole `en: { ... }` block, give it your
ISO 639-1 language code, and translate the right-hand side of each line. Keep `{v}`, `{n}` and
`{side}` placeholders in place. Untranslated keys fall back to Norwegian, so partial
translations are fine. Test with `index.html#yourcode` — the language appears as a button in
the start menu automatically. Send a pull request touching only `index.html`, or open an issue
with the text and we'll add it.

For code changes: one file, no dependencies, no build step, no storage, no network calls, and
measure performance before and after.
