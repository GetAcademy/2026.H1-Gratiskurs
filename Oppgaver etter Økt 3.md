# Oppgaver etter økt 3 (revidert versjon)

Disse oppgavene tar utgangspunkt i det vi faktisk gjorde i **Økt 3**, hvor vi bygde en enkel versjon av *Flappy Bird* steg for steg.

Målet er at du skal eksperimentere videre med ideene vi brukte:

* gravitasjon
* fart
* hindringer
* kollisjon
* enkel spill‑logikk

Du trenger ikke få til alt. Velg én eller flere oppgaver og prøv deg frem.

---

# Oppgave 1 – Gravitasjon og sprett

Start med denne enkle koden:

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<style>
canvas { border:1px solid black }
</style>
</head>
<body>

<canvas id="canvas" width="800" height="600"></canvas>

<script>
const c = document.getElementById("canvas")
const ctx = c.getContext("2d")

let x = 200
let y = 100

let vy = 0
let gravity = 0.3

function gameLoop(){

    ctx.clearRect(0,0,c.width,c.height)

    vy += gravity
    y += vy

    ctx.fillRect(x,y,40,40)

    requestAnimationFrame(gameLoop)
}

gameLoop()

</script>
</body>
</html>
```

### Oppgaver

1. Få firkanten til å **sprette på bakken**
2. Pass på at firkanten **ikke synker gjennom gulvet**
3. La firkanten miste litt energi når den spretter

Hint:

```js
if(y > c.height - 40){
    y = c.height - 40
    vy = -vy * 0.8
}
```

---

# Oppgave 2 – Flappy‑hopp

I Flappy Bird hopper figuren opp når vi trykker på en tast.

Legg til dette i programmet ditt:

```js
document.addEventListener("keydown", handleKeyDown)

function handleKeyDown(e){
    if(e.code === "Space"){
        vy = -8
    }
}
```

### Oppgaver

1. Test hoppet
2. Juster verdiene så det føles bra
3. Hva skjer hvis gravitasjonen blir større?

---

# Oppgave 3 – Lag en hindring

Nå skal vi lage en enkel hindring.

Lag en variabel:

```js
let pipeX = 800
```

Tegn et rør:

```js
ctx.fillRect(pipeX,0,80,250)
ctx.fillRect(pipeX,400,80,200)
```

### Oppgaver

1. Få røret til å **bevege seg mot venstre**

```js
pipeX -= 2
```

2. Når røret går ut av skjermen – start på nytt på høyre side

Hint:

```js
if(pipeX < -80){
    pipeX = c.width
}
```

---

# Oppgave 4 – Kollisjon

Nå skal vi sjekke om spilleren treffer røret.

En enkel versjon:

* sjekk om X overlapper
* sjekk om Y er utenfor hullet

Eksempel:

```js
if(
    x + 40 > pipeX &&
    x < pipeX + 80 &&
    (y < 250 || y + 40 > 400)
){
    alert("Game over!")
}
```

### Oppgaver

1. Test kollisjonen
2. Hva skjer hvis du gjør hullet større eller mindre?

---

# Oppgave 5 – To hindringer

Legg til en ny variabel:

```js
let pipe2X = 1200
```

Tegn et nytt rør på samme måte.

### Oppgaver

1. Få begge rørene til å bevege seg
2. Pass på at de starter på forskjellige steder

---

# Oppgave 6 – Score

Lag en variabel:

```js
let score = 0
```

Øk scoren når spilleren passerer et rør.

Vis scoren på skjermen:

```js
ctx.font = "30px Arial"
ctx.fillText("Score: " + score, 20, 40)
```

---

# Bonusoppgaver

Hvis du vil eksperimentere mer:

* tegn en **sirkel i stedet for firkant**
* bruk et **bilde av en figur**
* gjør hullene i rørene **random**
* lag **flere hindringer**
* refaktorer koden – del opp i funksjoner

Eksempel:

```
update()
draw()
checkCollision()
```

---

# Viktig poeng

Programmering handler ikke om å skrive perfekt kode første gang.

Vi bygger litt, tester, og **forbedrer strukturen underveis**.

Det er akkurat slik ekte utviklere jobber.
