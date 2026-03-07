# GET Academy – Gratiskurs i programmering

Dette repoet inneholder eksempler brukt i GET Academys **gratis kvalifiseringskurs i programmering**.

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
