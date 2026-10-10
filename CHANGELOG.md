# Endringslogg / Changelog

Alle merkbare endringer i spillet. Datoene er utgivelsesdatoer.

## [2.1] – 2026-10-10

- **Språkdrakt.** Norsk og engelsk, valgt automatisk fra nettleserens språk, med velger i
  startmenyen og styring fra adressen (`#en`, `#no`). Nye språk legges til i én tabell.
- **Joystick-side.** Venstrehendte kan flytte joysticken til høyre side. Joysticken starter
  bare på sin egen halvdel av skjermen, og valget huskes i adressen.
- **Jevnere rulling.** Kameraet lå på hele logiske piksler og flyttet brettet i rykk på 0, 5
  eller 10 skjermpiksler. Nå forskyves oppskaleringen med restbrøken, slik at brettet ruller i
  skjermpiksler. Frametiden låses dessuten til hele logikksteg nær 60 Hz.
- **Ytelse.** Verden tegnes i logisk oppløsning og skaleres opp én gang. Antall fylte piksler
  per frame falt fra 16,9 til 3,5 millioner om dagen og fra 20,0 til 6,9 om natten.
  Automatisk ytelsesnivå trapper ned pikselforhold, lys og partikler på svake enheter.
- **Rettet:** brannbilen kunne bli stående fast mellom en bil og en husvegg. Bilene skyver den
  ikke lenger inn i vegger, og står den fast, slipper de taket.
- **Rettet:** bygningenes kollisjonsboks stakk 7 piksler ut fra veggen, akkurat der skiltene
  sto. Marginen er nede i 3, og skilt og lysstolper er flyttet ut til kantsteinen.

## [2.0] – 2026-09-14

- **Trafikk med regler.** Lyskryss med rødt, gult og grønt, forkjørsveier med vikepliktskilt,
  og høyreregel i uskiltede kryss. Køer, følgeavstand og varierende trafikkmengde gjennom
  spillet. Sirenen får bilene til å vike i god tid.
- **Døgnsyklus** på fire minutter med dag, skumring, natt og daggry, og dynamisk lys fra
  gatelykter, frontlykter, stasjoner og brannene selv.
- **Vaktordning.** Dagvakt og nattvakt, med vaktbytte på brannstasjonen i skumringen og
  daggryet. Slangen virker ikke før byttet er gjort.
- **Bensin** med to bensinstasjoner. Tom tank avslutter runden.
- **Brannstasjon** midt på brettet, med forplass der brannbilen starter parkert.
- **Store innrammede varsler** for vann, bensin og vaktbytte.
- Avsluttknapp med bekreftelse, og bytte mellom høyre- og venstrehendt oppsett.

## [1.0] – 2026-09-13

Første versjon, bevart i `legacy/brannbilen-110-v1.html`.

- Kjøring med virtuell joystick, sirene og blålys.
- Slangemodus med fri sikting og flere brannsoner per hus.
- Vanntank og brannposter.
- Tre brannmannstjerner, øvingsmodus, hjelpeside og om-side.
