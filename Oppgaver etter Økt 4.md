# 🎮 Oppgaver etter Økt 4 – Fullføre spillet

Dette oppgavesettet bygger direkte på det dere gjorde i økt 4:

* Game state (gameOver / isRunning)
* Score
* Restart
* Helhet i spillet

Målet nå er ikke å lære masse nytt – men å **forstå og videreutvikle det dere allerede har laget**.

---

## 🧩 Oppgave 1 – Forstå state (viktig!)

Gå gjennom koden din og svar på disse spørsmålene:

1. Hvilke variabler beskriver **tilstanden (state)** i spillet?

   * Eksempler:

     * posisjon (x, y)
     * fart (speedY)
     * score
     * gameOver / isRunning

2. Hva skjer hvis du:

   * fjerner `gameOver`?
   * ikke nullstiller score ved restart?

👉 Skriv gjerne kommentarer i koden din som forklarer hva hver variabel representerer.

---

## 🧩 Oppgave 2 – Gjør Game Over tydeligere

Du har allerede en Game Over-tekst.

Utvid dette:

1. Gjør teksten større og tydeligere
2. Legg til en ekstra tekst:

   * "Trykk SPACE for å starte på nytt"
3. Tegn gjerne en bakgrunn bak teksten (f.eks. en mørk firkant)

👉 Tips:

```js
ctx.fillStyle = 'rgba(0,0,0,0.5)'
ctx.fillRect(50,150,500,200)
```

---

## 🧩 Oppgave 3 – Bedre restart

Se på restart-logikken din.

1. Samle alt i én funksjon:

```js
function restartGame() {
  // reset alt
}
```

2. Sørg for at dette resettes:

* posisjon
* fart
* score
* hindringer (pipes)

3. Kall funksjonen når spilleren trykker SPACE etter game over

👉 Poeng: Restart = bare sette state tilbake til start

---

## 🧩 Oppgave 4 – Forbedre score

Du har allerede score.

Utvid dette:

1. Vis score midt på skjermen når spillet er over
2. Lag en variabel for **highscore**

```js
let highscore = 0;
```

3. Oppdater highscore når spillet slutter:

```js
if(score > highscore) {
  highscore = score;
}
```

4. Tegn highscore på skjermen

---

## 🧩 Oppgave 5 – Gjør spillet litt vanskeligere

Velg én eller flere:

* Øk hastigheten gradvis
* Gjør gapet mellom hindringer mindre
* La hindringene få tilfeldig høyde

👉 Tips (tilfeldig høyde):

```js
let pipeHeight = Math.random() * 300;
```

---

## 🧩 Oppgave 6 – Små forbedringer (velg selv)

* Legg til lyd når du hopper
* Legg til fargeendringer
* Legg til en "startskjerm"
* Tegn bakken tydelig

---

## 🚀 Bonusoppgave – Gjør det til ditt eget spill

Endre tema:

* Bytt ut fuglen med noe annet
* Bytt bakgrunn
* Lag nye hindringer

Eksempler:

* Bil som kjører mellom hindringer
* Person som hopper over ting
* Romskip som flyr gjennom asteroider

---

## 🧠 Viktigste læring fra hele kurset

Hvis du forstår dette, har du kommet langt:

* Game loop:

  ```js
  update()
  draw()
  ```

* State:

  > Variabler som beskriver hvordan spillet er akkurat nå

* Input → påvirker state

* State → brukes til å tegne

---

## 💬 Refleksjon (valgfritt)

Svar for deg selv:

* Var dette gøy?
* Hva var vanskelig?
* Hva fikk du til?

👉 Hvis du synes dette var interessant, så er du akkurat i målgruppen for å lære mer 🚀

---

Lykke til videre! 🙌
