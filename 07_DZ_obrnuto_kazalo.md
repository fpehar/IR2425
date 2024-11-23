# Domaća zadaća

Implementirajte Booleovo pretraživanje koristeći obrnuto kazalo.

Bilješke:
---

```
Unesite upit, pritisnite Enter za izlaz:

? this text
['resources/1.txt', 'resources/2.txt', 'resources/3.txt']

Unesite upit, pritisnite Enter za izlaz:

? another Text
['resources/2.txt']

Unesite upit, pritisnite Enter za izlaz:

? Words
['resources/1.txt']

Unesite upit, pritisnite Enter za izlaz:

? blubbergurken
[]

Unesite upit, pritisnite Enter za izlaz:
?
```
<!-- .element: class="stretch" -->

Notes:
---
#<!-- .element: class="stretch" -->

Bilješke:
---
# Domaća zadaća

* Izgradite **obrnuto kazalo** iz tekstualnih datoteka
* [Koristite priloženu postavku](#), obavezno pročitajte [`README.md`](#)
* Čitajte `resources/*.txt`
    * Samo jednom prilikom pokretanja aplikacije, ne za svaki upit
* Pretraživanje koristi implicitni AND (`this text` &rarr; `this AND text`)
* Vaša aplikacija treba moći učinkovito rukovati milijunima datoteka
    * Pažljivo razmotrite što možete unaprijed izračunati tijekom indeksiranja kako biste uštedjeli vrijeme tijekom pretraživanja
* **Fokusirajte se na točnu implementaciju zahtijevanih algoritama i struktura podataka**
  * Izbjegavajte dugačke iteracije; dohvat treba biti brz.
* Koristite priloženi CLI za ručno testiranje vaše aplikacije (vidi `README.md`)
* Provjerite da svi priloženi testni slučajevi uspješno prolaze (vidi `README.md`)

Bilješke:

