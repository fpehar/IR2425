# Zaustavne riječi

Bilješke:
---

# Zaustavne riječi

* Nemaju značenje: *table* treba pronaći *a table* i *the table*
* Povećavaju veličinu kazala
* Ručno uređeni popis
* [Zadane engleske zaustavne riječi za Elasticsearch](https://github.com/apache/lucene/blob/main/lucene/analysis/common/src/java/org/apache/lucene/analysis/en/EnglishAnalyzer.java#L48)
* Počnite s najčešćim pojmovima u zbirci
* Mogu biti specifične za domenu
    * Npr., *doctor*, *patient* u medicinskim dokumentima

Bilješke:

* Koji bi problem mogao biti sa zaustavnim riječima?

---

<!-- .slide: class="audience-question" -->

# Zaustavne riječi, ali...

* &shy;<!-- .element: class="fragment" -->*The Police* će pronaći *police car*
* &shy;<!-- .element: class="fragment" -->*The President of Croatia* će pronaći *President of Albania visits Croatia*
* &shy;<!-- .element: class="fragment" -->*To be or not to be* će pronaći sve / ništa

Bilješke:
Koji su neki primjeri gdje su zaustavne riječi relevantne?
---

# Zaustavne riječi u stvarnom životu

* Veličina kazala više nije problem
* Elasticsearch: Zaustavne riječi su opcionalne, ali povećavaju bodove ako su podudarne
    * *The Police* će pronaći *police car*, ali će rangirati *The Police* više
* Nema posebnog rukovanja zaustavnim riječima kada se upit sastoji samo od zaustavnih riječi
    * *To be or not to be* pretražuje `[to, be, or, not]`

Bilješke:
