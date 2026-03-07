# Gratiskurs i programmering – Økt 2

I forrige økt lærte vi å **tegne ting på skjermen**.

I denne økten skal vi gjøre noe mye mer spennende:

* få ting til å **bevege seg**
* lage en enkel **animasjon**
* begynne å bygge **spillverdenen vår**

Vi gjør dette ved å la programmet gjenta to ting mange ganger:

1. oppdatere variabler
2. tegne alt på nytt

Når dette skjer mange ganger i sekundet, får vi **animasjon**.

---

# Før vi begynner

Vi fortsetter på samme måte som i økt 1.

Når vi lager en ny demo:

1. kopierer vi forrige demo
2. gir filen nytt navn

For eksempel:

```
demo1.html
→ kopier
→ demo2.html
```

Dette gjør at vi kan bygge programmet **steg for steg**.

---

# Steg 1 – Variabler styrer tegningen

Start med å kopiere forrige demo og lag:

```
demo1.html
```

La oss lage en variabel som bestemmer hvor et rektangel tegnes.

```js
let x = 100;

ctx.fillStyle = "green";
ctx.fillRect(x, 200, 50, 50);
```

Hvis du endrer verdien til `x`, flytter rektangelet seg.

```js
let x = 300;
```

Dette viser en viktig idé:

```
tall bestemmer hva som tegnes
```

---

# Steg 2 – Flytte objektet

La oss endre variabelen før vi tegner.

```js
let x = 100;

x = x + 20;

ctx.fillStyle = "green";
ctx.fillRect(x, 200, 50, 50);
```

Nå flytter rektangelet seg litt.

Hvis vi gjør dette mange ganger etter hverandre, vil rektangelet fortsette å flytte seg.

---

# Steg 3 – Lage funksjonene draw og update

For å gjøre programmet tydeligere deler vi koden i to funksjoner.

```js
function update() {
}

function draw() {
    ctx.fillStyle = "green";
    ctx.fillRect(x, 200, 50, 50);
}
```

`update()` skal endre variabler.

`draw()` skal tegne alt på skjermen.

---

# Steg 4 – Lage animasjon

Nå lager vi en funksjon som kjører igjen og igjen.

```js
function loop() {

    update();

    draw();

    requestAnimationFrame(loop);
}

loop();
```

Dette gjør at programmet hele tiden gjentar:

```
oppdater
tegn
oppdater
tegn
oppdater
tegn
```

Dette er grunnideen bak nesten alle spill.

---

# Steg 5 – Oppdatere variabler

Nå kan vi flytte rektangelet i `update()`.

```js
function update() {
    x = x + 2;
}
```

Når programmet kjører vil rektangelet bevege seg bortover skjermen.

---

# Steg 6 – Tegne bakgrunn

La oss legge til en enkel bakgrunn.

```js
function drawBackground() {

    ctx.fillStyle = "lightblue";
    ctx.fillRect(0, 0, 800, 600);

}
```

Og bruk den i `draw()`.

```js
function draw() {

    drawBackground();

    ctx.fillStyle = "green";
    ctx.fillRect(x, 200, 50, 50);

}
```

---

# Steg 7 – Scrollende bakgrunn

La oss lage en variabel for bakgrunnen.

```js
let backgroundX = 0;
```

Oppdater den i `update()`.

```js
backgroundX = backgroundX - 2;
```

Og tegn bakgrunnen basert på denne variabelen.

Dette gjør at bakgrunnen begynner å **bevege seg**.

---

# Spillmodellen vi bruker

Gjennom resten av kurset kommer programmene våre til å følge samme mønster.

```
variabler (modell)

update()
    endrer variabler

draw()
    tegner modellen

loop()
    gjenta mange ganger i sekundet
```

Dette er en veldig enkel **spillmotor**.

---

# Hva vi har lært i dag

I denne økten har vi lært:

* at variabler kan styre tegningen
* at vi kan endre variabler
* at vi kan tegne mange ganger i sekundet
* hvordan vi lager animasjon

Dette er grunnlaget for resten av spillet.

---

# Neste økt

I neste økt skal vi gjøre spillet mer interessant.

Da skal vi:

* legge til en **fugl**
* styre den med **tastaturet**
* begynne å nærme oss et ekte spill.
