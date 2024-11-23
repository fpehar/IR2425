# Obrnuto kazalo*


Bilješke:
---

* Ista informacija kao u matrici pojam-dokument, ali
* Nema pohrane nula
* Pohranjuje popis dokumenata koji odgovaraju svakom pojmu

Bilješke:
---

<!-- .slide: class="audience-question" -->

* \#1: _a book about information retrieval_
* \#2: _a book about the search for information_
* \#3: _a book about information_

&darr;

| Pojam        | ID-ovi dokumenata                              |
|--------------|------------------------------------------------|
| Book         | #1, #2, #3 <!-- .element: class="fragment" --> |
| Information  | #1, #2, #3 <!-- .element: class="fragment" --> |
| Retrieval    | #1         <!-- .element: class="fragment" --> |
| Search       | #2         <!-- .element: class="fragment" --> |

Bilješke: 

# Terminologija

<dl>
  <dt>Rječnik / Leksikon / Vokabular</dt><!-- .element: class="fragment" data-fragment-index="1" -->
  <dd>Popis pojmova</dd><!-- .element: class="fragment" data-fragment-index="1" -->

  <dt>Objava (eng. posting)</dt><!-- .element: class="fragment" data-fragment-index="2" -->
  <dd>Dokument u kojem se pojam pojavljuje</dd><!-- .element: class="fragment" data-fragment-index="2" -->

  <dt>Popis objava (eng. posting list)</dt><!-- .element: class="fragment" data-fragment-index="3" -->
  <dd>Svi dokumenti u kojima se pojam pojavljuje</dd><!-- .element: class="fragment" data-fragment-index="3" -->

  <dt>Objave (eng. postings)</dt><!-- .element: class="fragment" data-fragment-index="4" -->
  <dd>Svi popisi objava</dd><!-- .element: class="fragment" data-fragment-index="4" -->
</dl>

Bilješke:
---

# Vrijeme indeksiranja

1. Ekstrakcija pojmova iz dokumenata
2. Abecedno sortiranje rječnika
3. Sortiranje popisa objava prema ID-ovima dokumenata

Bilješke:
---

<!-- .slide: class="audience-question" -->

# Vrijeme pretraživanja

1. Pronađite svaki pojam iz upita u rječniku
2. Dohvatite popise objava
3. Presjek / Unija

*Samo točni pojmovi se mogu pronaći!*

Bilješke: Zašto se mogu pronaći samo točni pojmovi?
---

<!-- .slide: class="audience-question" -->

| Pojam                                                                                               | ID-ovi dokumenata                                                                           |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Book                                                                                               | #1, #2, #3                                                                                |
| <span>Information</span><!-- .element: class="fragment highlight-blue" data-fragment-index="2" --> | #1, #2, #3 <!-- .element: class="fragment highlight-blue" data-fragment-index="2" -->     |
| Retrieval                                                                                          | #1                                                                                        |
| <span>Search</span><!-- .element: class="fragment highlight-blue" data-fragment-index="3" -->      | #2 <!-- .element: class="fragment highlight-blue" data-fragment-index="3" -->             |

&darr;

&shy;<!-- .element: class="fragment" data-fragment-index="1" -->**Upit**:
<span>Information</span><!-- .element: class="fragment highlight-blue" data-fragment-index="2" -->
AND
<span>Search</span><!-- .element: class="fragment highlight-blue" data-fragment-index="3" -->

(#1, #2, #3) AND (#2)<!-- .element: class="fragment fade-in" -->

**&rarr; #2**<!-- .element: class="fragment fade-in" -->

Bilješke: Pitanje za publiku
---

# Vremenska kompleksnost

$$O(\text{broj pojmova u upitu} \times \text{broj jedinstvenih pojmova})$$<!-- .element: class="fragment" data-fragment-index="1" -->

#### <!-- .element: class="fragment" data-fragment-index="1" -->Primjer

* &shy;<!-- .element: class="fragment" data-fragment-index="1" -->*Engleska Wikipedija*: 6 milijuna članaka, 12 milijardi znakova, 1,2 milijuna
  jedinstvenih pojmova
* &shy;<!-- .element: class="fragment" data-fragment-index="1" -->Matrica pojam-dokument: 2 pojma iz upita &times; 1,2 milijuna
  jedinstvenih pojmova = **2,4 milijuna pretraga**
* &shy;<!-- .element: class="fragment" data-fragment-index="2" -->Obrnuto kazalo: 2 pojma iz upita &times; 1,2 milijuna
  jedinstvenih pojmova = **2,4 milijuna pretraga**

---

<!-- .slide: class="audience-question" -->

## Veličina

$$O(\text{broj jedinstvenih pojmova} \times \text{prosječna duljina popisa objava} \times \text{bajtova po ID-u dokumenta})$$<!-- .element: class="fragment" data-fragment-index="1" -->

#### <!-- .element: class="fragment" data-fragment-index="2" -->Primjer

* &shy;<!-- .element: class="fragment" data-fragment-index="2" -->*Engleska Wikipedija*: 6 milijuna članaka, 12 milijardi znakova, 1,2 milijuna
  jedinstvenih pojmova
* &shy;<!-- .element: class="fragment" data-fragment-index="2" -->Matrica pojam-dokument: 1,2 milijuna jedinstvenih pojmova &times; 6 milijuna
  članaka = 7.200.000.000.000 ćelija = 7,2 terabita = **900 gigabajta**
* &shy;<!-- .element: class="fragment" data-fragment-index="3" -->Obrnuto kazalo: 1,2 milijuna jedinstvenih pojmova &times; 10.000
  objava po pojmu &times; 4 bajta po ID-u dokumenta = 48.000.000.000 bajtova = **48 gigabajta**
