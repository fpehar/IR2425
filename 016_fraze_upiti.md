# Fraze u upitima

<!-- .slide: class="audience-question" -->

`"FFZG Zagreb"` ne bi se trebao podudarati s

> U Zagrebu se nalazi Sveučilište s mnogim fakultetima, uključujući FFZG.

Kako?

---

# Fraze u upitima

<!-- .slide: class="audience-question" -->

* &shy;<!-- .element: class="fragment" --> `FFZG Zagreb` ne bi se trebao
  podudarati s `U Zagrebu se nalazi Sveučilište s mnogim fakultetima, uključujući FFZG.`
* &shy;<!-- .element: class="fragment" --> Pretraživanje imena i pojmova: `"FFZG Zagreb"`, `"brdski bicikl"`, `"mountain bike"`
* &shy;<!-- .element: class="fragment" --> Dobro prihvaćeno od strane korisnika
* &shy;<!-- .element: class="fragment" --> Zahtijeva napredniji indeks s pozicijskim informacijama

Bilješke:

* Kako bismo ovo mogli implementirati?
* Može li trenutni indeks podržati ovakve upite?

---
# Pozicijski indeks

<!-- .slide: class="audience-question" -->

* \#1: _retrieving more information about information retrieval_
* \#2: _searching and retrieving a book about the search for information_
* \#3: _a book about information_

***

| Terms (excluding stop words) | Doc IDs                                                       |
|------------------------------|---------------------------------------------------------------|
| book                         | #2:[3], #3:[1] <!-- .element: class="fragment" -->            |
| information                  | #1:[2, 3], #2:[5], #3:[2] <!-- .element: class="fragment" --> |
| retriev                      | #1:[1, 4], #2:[2]         <!-- .element: class="fragment" --> |
| search                       | #2:[1, 4]         <!-- .element: class="fragment" -->         |

Bilješke:

* Pitanje za publiku

---

# Algoritam za presjek

<!-- .slide: class="audience-question" -->

`"information retrieval"`

1. <!-- .element: class="fragment" data-fragment-index="1" --> Dohvatite objave za svaki pojam iz upita:
    * &shy;<!-- .element: class="fragment" data-fragment-index="1" --> *information*: #1:[2, 3], #2:[5], #3:[2]
    * &shy;<!-- .element: class="fragment" data-fragment-index="1" --> *retriev*: #1:[1, 4], #2:[2]
2. &shy;<!-- .element: class="fragment" data-fragment-index="2" --> Izračunajte udaljenost između parova pojmova po dokumentu,
   npr. `retrieval - information`:
    * &shy;<!-- .element: class="fragment" data-fragment-index="3" --> _#1: <span>
      retrieving</span><!-- .element: class="highlight-blue" --> more <span>
      information</span><!-- .element: class="highlight-blue" --> about information retrieval_
        *
      &shy;<!-- .element: class="fragment" data-fragment-index="3" --> [<span>1</span><!-- .element: class="highlight-blue" -->, 4] - [<span>2</span><!-- .element: class="highlight-blue" -->, 3] =
      -1 != 1
    * &shy;<!-- .element: class="fragment" data-fragment-index="4" --> _#1: <span>
      retrieving</span><!-- .element: class="highlight-blue" --> more information about <span>
      information</span><!-- .element: class="highlight-blue" --> retrieval_
        *
      &shy;<!-- .element: class="fragment" data-fragment-index="4" --> [<span>1</span><!-- .element: class="highlight-blue" -->, 4] - [2, <span>3</span><!-- .element: class="highlight-blue" -->] =
      -2 != 1
    * &shy;<!-- .element: class="fragment" data-fragment-index="5" --> _#1: retrieving more <span>
      information</span><!-- .element: class="highlight-blue" --> about information <span>
      retrieval</span><!-- .element: class="highlight-blue" -->_
        *
      &shy;<!-- .element: class="fragment" data-fragment-index="5" --> [1, <span>4</span><!-- .element: class="highlight-blue" -->] - [<span>2</span><!-- .element: class="highlight-blue" -->, 3] =
      2 != 1
    * &shy;<!-- .element: class="fragment" data-fragment-index="6" --> _#1: retrieving more information about <span>
      information</span><!-- .element: class="highlight-blue" --> <span>
      retrieval</span><!-- .element: class="highlight-blue" -->_
        *
      &shy;<!-- .element: class="fragment" data-fragment-index="6" --> [1, <span>4</span><!-- .element: class="highlight-blue" -->] - [2, <span>3</span><!-- .element: class="highlight-blue" -->] =
      1 &rarr; podudaranje

Skupa kalkulacija

Bilješke:

* Može li se ovo koristiti za blizinu bez obzira na redoslijed, npr. podudarati se s "retrieval information"?
* Može li ovo podržati razmake u frazi, npr. `information … retrieval`?

---

# Pozicijski indeks

<!-- .slide: class="audience-question" -->

Podržava razmake u frazama: `"dwayne johnson"~2` podudara se s *dwayne the rock johnson*

Bilješke:

* Najčešći slučaj je pretraživanje za dvije uzastopne riječi. Algoritam za presjek je malo skuplji. Možemo li ovo
  ubrzati?

---

# Indeks parova riječi (Biword index)

* Ubrzava pretraživanje uobičajenih fraza
* Pomoćni indeks
* Indeksira parove pojmova
* Brzo dohvaćanje parova pojmova

#1: "Studiraj na FFZG u Zagrebu"

&darr;

| Pojam        | ID-ovi dokumenata |
|--------------|-------------------|
| studiraj na  | #1                |
| na ffzg      | #1                |
| ffzg zagreb  | #1                |

***  

&shy; <!-- .element: class="fragment" --> `ffzg zagreb` &rarr; \#1

Bilješke:

