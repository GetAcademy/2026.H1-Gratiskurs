# Gratiskurs – Økt 3 (Oppdatert mars 2026)

## Mål for økten

I denne økten går vi fra enkel animasjon til et faktisk spill. Vi bygger steg for steg en enkel versjon av **Flappy Bird**.

Fokus:

* Gravitasjon
* Kollisjon
* Hindringer
* Score
* Refaktorering underveis slik at koden holder en god struktur

Målet er ikke perfekt kode, men å vise hvordan man **tenker som utvikler**: vi bygger litt, tester, og forbedrer strukturen underveis.

---

# Del 1 – Kort repetisjon

Vi starter med koden fra forrige økt.

Repetisjon av konsepter:

* variabler
* if-setninger
* animasjon i game loop
* sprett i vegg

Spørsmål til deltakerne:

* Hvor styres farten?
* Hva gjør if-setningen?
* Hvorfor spretter objektet?

Poenget er å minne deltakerne på hvordan **game loop** fungerer:

update → draw → requestAnimationFrame

---

# Del 2 – Gravitasjon

Nå lager vi noe som **faller nedover**.

Vi introduserer en ny variabel:

* vertical velocity (vy)

Eksempel:

vy += 0.3

y += vy

Forklaring:

* Objektet får mer og mer fart nedover
* Dette kalles akselerasjon
* Gravitasjon er bare en konstant som legges til farten

Visualisering:

* Tegn en enkel firkant eller sirkel
* Den starter midt på skjermen
* Den faller nedover

---

# Del 3 – Bakken og sprett

Vi legger til en bakke.

Hvis objektet treffer bakken:

if (y > groundY) {
y = groundY
vy = -vy
}

Dette er samme idé som **sprett i vegg**, men nå vertikalt.

Snakk litt om hvordan vi:

* gjenbruker idéer
* bruker samme mønster flere steder

---

# Del 4 – Første hindring

Nå begynner vi å bygge **Flappy Bird**.

Vi starter veldig enkelt.

Vi lager én variabel:

pipeX

Denne styrer hele hindringen.

Alt annet er hardkodet.

Eksempel:

* topp-rør
* bunn-rør
* hull i midten

Begge tegnes basert på samme X-posisjon.

---

# Del 5 – To hindringer

Når én fungerer, legger vi til en til.

pipeX1
pipeX2

Begge flytter seg mot venstre.

pipeX -= speed

Dette gir følelsen av at spilleren flyr fremover.

---

# Del 6 – Kollisjon

Nå sjekker vi om spilleren treffer hindringen.

En enkel tilnærming:

* sjekk om X overlapper
* sjekk om Y er utenfor hullet

Hvis kollisjon skjer:

* stopp spillet
* eller nullstill

Poenget er å vise hvordan spill kan avgjøre hva som skjer.

---

# Del 7 – Score (hvis tid)

Hvis spilleren passerer en hindring:

score++

Vis scoren på skjermen.

Dette gir en liten ekstra spillfølelse.

---

# Del 8 – Refaktorering underveis

Underveis stopper vi noen ganger og forbedrer koden.

Eksempler:

* samle variabler
* rydde i navn
* trekke ut små funksjoner

Poenget er å vise at utviklere hele tiden spør:

"Kan denne koden bli litt bedre?"

Dette er en viktig del av programmering.

---

# Del 9 – Oppsummering

Vi har nå laget en enkel spillmotor med:

* gravitasjon
* hindringer
* kollisjon
* score

Dette er mange av de samme idéene som brukes i ekte spill.

Neste økt:

Vi snakker mer om veien videre i GET Academy og hvilke muligheter deltakerne har hvis de ønsker å lære mer programmering.
