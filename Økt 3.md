# Gratiskurs – Økt 3 (Ny versjon mars 2026)

## Mål for økten

I denne økten går vi fra enkel animasjon til et faktisk spill.

Vi bygger steg for steg en enkel versjon av **Flappy Bird** ved å kombinere noen få, viktige konsepter:

* tastestyring
* fart og gravitasjon
* kollisjon
* hindringer
* enkel spill‑logikk

Rød tråd:

> Vi bygger litt → tester → forbedrer koden underveis (refaktorering)

---

# Del 1 – Repetisjon: game loop og enkel bevegelse

Vi starter med en enkel firkant og repeterer:

* `x` og `y`
* game loop
* tegning i canvas

Rød tråd:

> update → draw → requestAnimationFrame

Kort spørsmål til deltakerne:

* Hva styrer bevegelsen?
* Hva skjer hvis vi endrer en variabel?

---

# Del 2 – Tastestyring (to måter)

## 2.1 Styre posisjon direkte (naiv løsning)

Vi starter enkelt:

* piltaster endrer `x` og `y` direkte

Poeng:

* lett å forstå
* men ikke slik spill vanligvis bygges

---

## 2.2 Styre fart i stedet for posisjon

Vi forbedrer modellen:

* introduserer `vx` og `vy`
* tastene påvirker fart
* farten påvirker posisjon

Rød tråd:

> input → fart → posisjon

Dette er samme modell vi bruker videre.

---

# Del 3 – Gravitasjon

Vi lager noe som faller.

```js
vy += 0.3
y += vy
```

Forklaring:

* objektet får mer og mer fart nedover
* dette er akselerasjon

Visualisering:

* firkant starter midt på skjermen
* faller nedover

---

# Del 4 – Flappy-hopp (space)

Vi kobler tastestyring til fysikk.

```js
document.addEventListener("keydown", handleKeyDown)

function handleKeyDown(e){
    if(e.code === "Space"){
        vy = -8
    }
}
```

Forklaring:

* space gir et "kick" oppover
* gravitasjon trekker ned igjen

Dette er kjernen i Flappy Bird.

---

# Del 5 – Bakken

Vi legger til en bakke.

```js
if(y > groundY){
    y = groundY
    vy = -vy * 0.8
}
```

Koble til tidligere:

* samme idé som sprett i vegg
* gjenbruk av mønster

Mulig variasjon:

* bakken kan være *game over* i stedet for sprett

---

# Del 6 – Første hindring

Vi starter enkelt.

Én variabel:

```js
let pipeX = 800
```

Tegn to firkanter:

* topp
* bunn

Alt styres av `pipeX`.

Bevegelse:

```js
pipeX -= 2
```

---

# Del 7 – Flere hindringer

Når én fungerer:

```js
let pipe2X = 1200
```

Begge flytter seg.

Poeng:

* vi kopierer og tilpasser
* senere kunne vi gjort dette mer generelt (refaktorering)

---

# Del 8 – Kollisjon mellom firkanter

Vi bruker en viktig idé:

Det finnes **fire måter to firkanter IKKE kolliderer på**:

1. Den ene er til venstre
2. Den ene er til høyre
3. Den ene er over
4. Den ene er under

Hvis ingen av disse stemmer → kollisjon.

```js
function isColliding(r1, r2){
    const noCollision =
        r1.x + r1.width < r2.x ||
        r1.x > r2.x + r2.width ||
        r1.y + r1.height < r2.y ||
        r1.y > r2.y + r2.height

    return !noCollision
}
```

Pedagogisk grep:

* tegn to firkanter
* spør: "Når treffer de ikke hverandre?"

Viktig poeng:

> Kollisjon handler bare om tall – ikke grafikk

---

# Del 9 – Game over

Ved kollisjon:

* stopp spillet
* eller nullstill

Samme gjelder for bakken hvis vi velger det.

---

# Del 10 – Score (hvis tid)

```js
score++
```

Vis på skjermen.

Gir ekstra spillfølelse.

---

# Del 11 – Refaktorering underveis

Underveis stopper vi og forbedrer koden.

Eksempler:

* bedre variabelnavn
* samle logikk
* lage små funksjoner

Eksempel:

```
update()
draw()
checkCollision()
```

Poeng:

> Vi rydder litt og litt – ikke alt på en gang

---

# Del 12 – Oppsummering

Vi har laget et lite spill med:

* fysikk (gravitasjon)
* input (tastatur)
* hindringer
* kollisjon
* regler

Dette er de samme byggesteinene som brukes i ekte spill.

Neste økt:

Vi ser på veien videre i GET Academy og hvordan man kan lære mer programmering.
