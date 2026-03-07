# Gratiskurs i programmering – Økt 1

Dette notatet brukes både **i undervisningen** og som **gjennomgang etter timen**.
Vi skriver all kode **fra bunnen av** i timen. Etterpå kan du bruke dette notatet for å gå gjennom stegene igjen.

I dag skal vi:

* lage vår første JavaScript-fil
* tegne grafikk på skjermen
* lage en enkel funksjon

Dette er starten på spillet vi skal bygge gjennom kurset.

---

# Før vi begynner

Vi starter alltid med en enkel malfil:

`canvas_mal.html`

Når vi lager første demo, **kopierer vi denne filen** og gir den nytt navn.

For eksempel:

```
demo1.html
```

Malfilen inneholder allerede et canvas og litt startkode.

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Canvas</title>
<style>
canvas {
border: 1px solid black;
}
</style>
</head>

<body>

<canvas id="canvas" width="800" height="600"></canvas>

<script>

const c = document.getElementById('canvas');
const ctx = c.getContext('2d');

// Skriv kode her ↓

</script>

</body>
</html>
```

To linjer er spesielt viktige:

```js
const c = document.getElementById('canvas');
const ctx = c.getContext('2d');
```

Her gjør vi to ting:

1. finner canvas-elementet i HTML
2. får et **tegneverktøy** (`ctx`) som lar JavaScript tegne grafikk

All koden vår skrives under kommentaren:

```js
// Skriv kode her ↓
```

---

# Hvordan programmer vi lager i dette kurset fungerer

Gjennom kurset kommer programmene våre stort sett til å gjøre to ting:

```
1. Vi har noen variabler (en modell)
2. Vi tegner modellen på skjermen
```

I spill gjøres dette mange ganger i sekundet.

Senere i kurset vil modellen vår for eksempel være:

```
birdY
pipeX
backgroundX
```

Men i dag begynner vi helt enkelt:
vi skal bare **tegne ting på skjermen**.

---

# Steg 1 – Lag demo1.html

1. Kopier `canvas_mal.html`
2. Gi kopien navnet

```
demo1.html
```

Åpne filen i nettleseren.

---

# Første tegning

Legg til denne koden i `<script>`:

```js
ctx.fillStyle = "green";
ctx.fillRect(200, 200, 200, 200);
```

Lagre filen og oppdater nettleseren.

Du skal nå se et grønt kvadrat.

---

## Hva betyr tallene?

```js
ctx.fillRect(200, 200, 200, 200);
```

Tallene betyr:

```
x-posisjon
y-posisjon
bredde
høyde
```

Rektangelet tegnes altså:

* 200 piksler fra venstre
* 200 piksler fra toppen
* 200 piksler bredt
* 200 piksler høyt

---

# Steg 2 – Lag demo2.html

Når vi lager neste demo gjør vi alltid dette:

1. Kopier forrige demo
2. Gi den nytt navn

```
demo2.html
```

Dette gjør at vi kan bygge programmet **steg for steg**.

---

# Tegne flere figurer

I `demo2.html` kan vi tegne flere rektangler.

```js
ctx.fillStyle = "green";
ctx.fillRect(200, 200, 200, 200);

ctx.fillStyle = "red";
ctx.fillRect(100, 100, 100, 100);

ctx.fillStyle = "blue";
ctx.fillRect(400, 200, 150, 150);
```

Nå har vi flere figurer på skjermen.

---

# Tegne en sirkel

Canvas kan også tegne sirkler.

```js
ctx.beginPath();
ctx.arc(400, 300, 50, 0, Math.PI * 2);
ctx.fill();
```

Parameterne betyr:

```
x
y
radius
```

---

# Steg 3 – Lag demo3.html

Vi fortsetter på samme måte:

1. Kopier `demo2.html`
2. kall kopien

```
demo3.html
```

I denne demoen skal vi bruke **funksjoner**.

---

# Funksjoner

Når vi programmerer gjør vi ofte det samme flere ganger.

Da kan vi samle koden i en funksjon.

Lag denne funksjonen:

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

Denne funksjonen tegner et enkelt ansikt.

---

# Bruke funksjonen

Vi kan nå tegne flere ansikter slik:

```js
drawFace(200, 200);
drawFace(400, 300);
drawFace(600, 200);
```

Fordelen med funksjoner er at vi kan **gjenbruke kode**.

---

# Hva vi har gjort i dag

I denne økten har vi:

* brukt en canvas-mal
* laget våre egne demo-filer
* tegnet grafikk med JavaScript
* laget en funksjon

Dette er grunnlaget for resten av kurset.

---

# Neste økt

I neste økt skal vi gjøre noe mye mer spennende.

Vi skal få ting til å **bevege seg**.

Da begynner vi å bygge spillet vårt.
