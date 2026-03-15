# Oppgaver etter Økt 2

Disse oppgavene bygger på det vi gjorde i **økt 2**.

I denne økten lærte vi at animasjon i et program egentlig bare er tre ting:

```
1. Oppdater variabler
2. Tegn alt på nytt
3. Gjenta
```

Vi brukte tre funksjoner for å gjøre dette:

```js
update()
draw()
loop()
```

I oppgavene under skal du øve på akkurat denne modellen.

Start alltid med å kopiere **forrige demo** eller `canvas_mal.html` til en ny fil.

---

# Oppgave 1 – Et rektangel som styres av en variabel

Lag en variabel som bestemmer hvor et rektangel tegnes.

```js
let x = 100;

ctx.fillStyle = "green";
ctx.fillRect(x, 200, 50, 50);
```

Endre verdien i `x` flere ganger og oppdater nettleseren.

Målet er å forstå at:

```
tall bestemmer hva som tegnes
```

---

# Oppgave 2 – Del opp koden i funksjoner

Lag funksjonene `update()` og `draw()`.

```js
function update() {
}

function draw() {
    ctx.fillStyle = "green";
    ctx.fillRect(x, 200, 50, 50);
}
```

Dette gjør programmet mer oversiktlig.

---

# Oppgave 3 – Lag en spill‑loop

Lag en funksjon som kjører igjen og igjen.

```js
function loop() {

    update();

    draw();

    requestAnimationFrame(loop);
}

loop();
```

Programmet vil nå gjenta:

```
oppdater
tegn
oppdater
tegn
```

mange ganger i sekundet.

---

# Oppgave 4 – Få rektangelet til å bevege seg

Flytt rektangelet i `update()`.

```js
function update() {
    x = x + 2;
}
```

Rektangelet skal nå bevege seg bortover skjermen.

---

# Oppgave 5 – Tegn en bakgrunn

Lag en funksjon som tegner en bakgrunn.

```js
function drawBackground() {
    ctx.fillStyle = "lightblue";
    ctx.fillRect(0, 0, 800, 600);
}
```

Bruk den i `draw()`.

```js
function draw() {

    drawBackground();

    ctx.fillStyle = "green";
    ctx.fillRect(x, 200, 50, 50);

}
```

---

# Oppgave 6 – Flere objekter

Lag en ny variabel.

```js
let x2 = 300;
```

Tegn et nytt rektangel.

```js
ctx.fillStyle = "red";
ctx.fillRect(x2, 300, 50, 50);
```

Flytt også dette rektangelet i `update()`.

---

# Oppgave 7 – Endre hastighet

Lag en variabel for fart.

```js
let speed = 2;
```

Bruk den i stedet for tallet direkte.

```js
x = x + speed;
```

Prøv ulike verdier.

---

# Oppgave 8 – Få rektangelet til å snu

Lag en enkel sjekk slik at rektangelet snur når det når kanten av canvas.

Eksempel:

```js
if (x > 800) {
    speed = -speed;
}
```

Nå skal rektangelet begynne å gå tilbake.

---

# Oppgave 9 – Lag din egen animasjon

Bruk det du har lært til å lage en liten animasjon.

For eksempel:

* to objekter som beveger seg
* et objekt som går frem og tilbake
* et objekt som beveger seg opp og ned

Målet er å øve på modellen:

```
variabler
update()
draw()
loop()
```

---

# Hvis du blir ferdig tidlig

Her er noen ting du kan prøve:

* la to objekter bevege seg i ulik fart
* la et objekt bevege seg vertikalt
* lag en variabel for størrelse
* prøv å tegne en sirkel i stedet for et rektangel

---

# Oppsummering

Etter disse oppgavene bør du være komfortabel med:

* variabler som styrer tegning
* funksjonene `update()` og `draw()`
* `requestAnimationFrame()`
* enkel animasjon

Dette er grunnlaget for resten av spillet vi skal lage i de neste øktene.
