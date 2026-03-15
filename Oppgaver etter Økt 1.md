# Oppgaver etter Økt 1

Disse oppgavene bygger på det vi gjorde i **økt 1**.

Målet er å gi deg litt mer trening i å:

* bruke `canvas`
* tegne figurer med JavaScript
* endre tall og se hva som skjer
* lage og bruke en funksjon

Start med å kopiere `canvas_mal.html` til en ny fil, for eksempel `oppgave1.html`.

Skriv all koden din i `<script>`-delen.

---

## Før du begynner

Det viktigste i disse oppgavene er ikke å bli fort ferdig.

Det viktigste er at du:

* skriver koden selv
* tester små endringer
* ser hva tallene gjør
* prøver igjen hvis noe ikke virker

---

## Oppgave 1 – Tegn ett rektangel

Tegn ett rektangel på skjermen.

```js
ctx.fillStyle = "green";
ctx.fillRect(200, 200, 200, 200);
```

Når det virker, kan du prøve å endre:

* fargen
* x-posisjonen
* y-posisjonen
* bredden
* høyden

---

## Oppgave 2 – Tegn flere rektangler

Tegn minst tre rektangler på ulike steder.

```js
ctx.fillStyle = "green";
ctx.fillRect(200, 200, 200, 200);

ctx.fillStyle = "red";
ctx.fillRect(100, 100, 100, 100);

ctx.fillStyle = "blue";
ctx.fillRect(450, 120, 120, 250);
```

Målet er å bli tryggere på koordinater og størrelser.

---

## Oppgave 3 – Tegn en sirkel

Legg til en sirkel.

```js
ctx.fillStyle = "orange";
ctx.beginPath();
ctx.arc(400, 300, 50, 0, Math.PI * 2);
ctx.fill();
```

Prøv gjerne å endre:

* plassering
* radius
* farge

---

## Oppgave 4 – Lag funksjonen `drawFace(x, y)`

Lag en funksjon som tegner et enkelt ansikt.

```js
function drawFace(x, y) {
    ctx.fillStyle = "yellow";
    ctx.beginPath();
    ctx.arc(x, y, 50, 0, Math.PI * 2);
    ctx.fill();

    ctx.fillStyle = "black";
    ctx.beginPath();
    ctx.arc(x - 20, y - 10, 8, 0, Math.PI * 2);
    ctx.arc(x + 20, y - 10, 8, 0, Math.PI * 2);
    ctx.fill();
}
```

Når funksjonen er ferdig, test den slik:

```js
drawFace(200, 200);
```

---

## Oppgave 5 – Bruk funksjonen flere ganger

Bruk `drawFace(x, y)` flere ganger for å tegne flere ansikter.

```js
drawFace(200, 200);
drawFace(400, 300);
drawFace(600, 180);
```

Målet er å oppleve hvorfor funksjoner er nyttige.

---

## Oppgave 6 – Endre funksjonen

Når `drawFace()` virker, kan du endre på ansiktet.

Du kan for eksempel:

* endre fargen på ansiktet
* gjøre øynene større
* flytte øynene
* legge til en munn
* lage et rart eller morsomt ansikt

Forslag til munn:

```js
ctx.beginPath();
ctx.arc(x, y + 10, 20, 0, Math.PI);
ctx.stroke();
```

---

## Oppgave 7 – Lag din egen tegning

Bruk det du har lært til å lage en enkel tegning.

Du kan for eksempel lage:

* et ansikt-galleri
* en enkel robot
* et hus
* en liten by med firkanter og en sol

Bruk gjerne:

* rektangler
* sirkler
* funksjoner

---

## Hvis du blir ferdig tidlig

Du kan utforske litt videre.

### Tegn tekst

```js
ctx.font = "30px Arial";
ctx.fillText("Hei!", 300, 100);
```

### Tegn et bilde

```js
const img = new Image();
img.src = "bird.png";

img.onload = function () {
    ctx.drawImage(img, 300, 200, 100, 100);
};
```

### Lag en ny funksjon

For eksempel:

* `drawHouse(x, y)`
* `drawRobot(x, y)`
* `drawSun(x, y)`

---

## Tips hvis noe ikke virker

* sjekk at du har skrevet alt riktig
* sjekk store og små bokstaver
* sjekk parenteser og komma
* prøv å angre siste endring
* spør om hjelp

---

## Oppsummering

Etter økt 1 er det viktigste at du har fått trening i å:

* skrive litt JavaScript selv
* tegne på et `canvas`
* bruke koordinater
* lage og bruke en funksjon

Det holder lenge.

I neste økt skal vi få ting til å **bevege seg**.
