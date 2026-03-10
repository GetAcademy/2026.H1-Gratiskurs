# Gratiskurs JavaScript og canvas — Get Academy (Desember 2025)
<!-- markdownlint-disable MD033 -->
<a href="https://getacademy.no">
<img src="https://getacademy.no/hubfs/GET_RGB_logo-01-2.png" alt="GET Logo" width="200" height="auto">
</a>
<!-- markdownlint-disable MD033 -->

## **Velkommen**: Velkommen til Gratiskurs i JavaScript og canvas!

Dette kurset går over fire korte økter hvor dere lærer å tegne på `canvas`, lage enkle animasjoner, og bruke grunnleggende programmeringsprinsipper i JavaScript.
Vi anbefaler å følge med, stille spørsmål i Discord, og bruke opptakene senere når dere prøver selv.

## **Kort pensum**

- **Enkel tegning i canvas**: linje, firkant, sirkel, bilde, tekst.
- **Enkle animasjoner**: `requestAnimationFrame` og animasjonsløp.
- **Enkel fysikk og matematikk**: tilfeldige tall, fart og retning, sprette i veggen, gravitasjon, kollisjon.
- **Funksjoner og struktur**: lage egne kommandoer (parametre, returverdi), lokale vs globale variabler.
- **Operatorer og kontrollflyt**: tilordning, aritmetiske operatorer, sammenligning, logiske operatorer, `if`-setninger.
- **Feilsøking og input**: vanlige feil, tips til debugging, og tastestyring.

## **Praktisk informasjon**

- Opptak av alle økter deles i etterkant — bruk dem når du øver selv.
- Bli med på Discord for spørsmål og støtte.
- Ikke gjør nøyaktig det instruktøren gjør parallelt — følg med, prøv å forstå, og still spørsmål underveis.

## **Økter og oppgaver**

- **Økt 1 — tirsdag 10.03 kl. 14:00–15:30**: Velkommen, installasjon (VS Code + Live Server), gjennomgang av HTML-skjelett med `canvas` og enkel tegning. Oppgaver og steg-for-steg: `Økt 1.md`.
- **Økt 2 — torsdag 12.03 kl. 14:00–15:30**: Variabler, operatorer, funksjoner med returverdi, enkle animasjoner og grunnleggende fysikk. Oppgaver og øvelser: `Økt 2.md`.
- **Økt 3 — tirsdag 17.03 kl. 14:00–15:30**: Grundig om `if`-setninger, logiske operatorer, tastastyring, gravitasjon og kollisjon. Start på enkel Flappy Bird. Oppgaver: `Økt 3.md`.
- **Økt 4 — torsdag 19.03 kl. 14:00–15:30**: Fullføre enkel Flappy Bird, spørsmål og svar, info om tilbud fra GET Academy. Oppgaver: `Økt 4.md`.

Lykke til — still spørsmål i Discord eller direkte til instruktørene når noe er uklart!


# Intro

- Presentasjon av oss lærerne
- Oppfølging fra Martin, Kenneth og Anita
- Velkommen til Discord-serveren vår (frivillig)
   - Martin eller Kenneth er tilgjengelig i `general` kl. 13 - 14 mandager, onsdager og fredager
   - De er også tilgjengelige på DM - brukernavnene er `waste1` (Martin) og `im.jst.ken` (Kenneth)

Dette repoet inneholder eksempler brukt i GET Academys **gratis kvalifiseringskurs i programmering**, https://github.com/GetAcademy/2026.H1-Gratiskurs

I løpet av kurset bygger vi et lite spill inspirert av **Flappy Bird** ved hjelp av enkel JavaScript og HTML Canvas.

Kurset er laget for personer som lurer på:

> *Kan programmering være noe for meg?*

Det kreves **ingen forkunnskaper**.

---

# Hva vi bygger

Gjennom fire økter bygger vi gradvis opp et lite spill.

Vi starter helt enkelt, og legger til én idé av gangen:

1. Tegne ting på skjermen
2. Få ting til å bevege seg
3. Lage en spillverden
4. Styre en figur
5. Lage et spill

Til slutt har vi et spill hvor:

* en fugl beveger seg opp og ned
* hinder beveger seg mot spilleren
* bakgrunnen beveger seg
* spilleren styrer fuglen med tastaturet

---

# Pedagogisk idé

Koden holdes **så enkel som mulig**.

Vi bruker derfor ikke:

* arrays
* objekter
* klasser
* rammeverk

I stedet bruker vi noen få variabler som representerer spilltilstanden:

```
birdY
pipeX
backgroundX
```

Programmet fungerer slik:

1. Spilltilstanden oppdateres
2. Skjermen tegnes på nytt
3. Dette gjentas mange ganger i sekundet

Dette er i praksis en veldig enkel spillmotor.

---

# Hvordan kurset er strukturert

Kurset går over **fire økter**.

## Økt 1 – Tegne på skjermen

Vi starter med å lære hvordan JavaScript kan tegne grafikk.

Temaer:

* HTML
* `<canvas>`
* koordinater
* tegne former
* variabler

Resultat:
Vi kan tegne grafikk på skjermen.

---

## Økt 2 – Animasjon og spillverden

Vi får ting til å bevege seg og lager en spillscene.

Temaer:

* animasjon
* game loop
* bevegelige elementer
* animert bakgrunn

Resultat:
En enkel spillverden begynner å ta form.

---

## Økt 3 – Spillfigur

Vi lager spillfiguren og lar spilleren styre den.

Temaer:

* tastaturinput
* oppdatere spilltilstand
* tyngdekraft og bevegelse

Resultat:
Spilleren kan styre fuglen.

---

## Økt 4 – Spillmekanikk

Til slutt lager vi selve spillet.

Temaer:

* hinder
* kollisjon
* spillregler

Resultat:
Et enkelt spill inspirert av **Flappy Bird**.

---

# Struktur på repoet

Eksemplene fra undervisningen ligger i:

```
/eksempler
```

Hver økt har sin egen mappe:

```
/eksempler
   /økt 1
   /økt 2
   /økt 3
   /økt 4
```

Hver mappe inneholder flere demoer:

```
demo1.html
demo2.html
demo3.html
...
```

Hver demo viser ett nytt steg i utviklingen av spillet.

Dette gjør det lett å:

* gå tilbake til tidligere steg
* vise progresjon i undervisningen
* forstå hva som ble lagt til når

---

# Hvem kurset er for

Kurset er laget for personer som:

* vurderer programmering eller IT-utvikling
* er usikre på om programmering passer for dem
* ønsker å teste programmering i et trygt miljø

Mange deltakere kommer via **NAV-veiledere** som ønsker å gi kandidater en mulighet til å teste IT-interesse.

---

# Hva skjer etter kurset

Etter kurset får deltakerne en vurdering av progresjon og teknisk interesse.

Mulige veier videre:

* **Realkompetansekurs**
* **Start IT**
* **Intro til IT-utvikling (fagskole)**

Mer informasjon:

Kvalifiseringskurs
https://getacademy.no/kvalifiseringskurs

Realkompetansekurs
https://getacademy.no/realkompetansekurs

---

# Om GET Academy

GET Academy er en sosial entreprenør som hjelper mennesker fra utenforskap til jobb innen IT-utvikling.

Vi kombinerer:

* teknisk kompetanse
* nøkkelkompetanser
* praksisnær læring

Målet er varig jobb i IT-bransjen.
