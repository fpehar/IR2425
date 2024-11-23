# Tokenizacija

Bilješke:
---

# Tokenizacija

> a book about information retrieval <!-- .element: class="fragment" data-fragment-index="1" -->

&darr; <!-- .element: class="fragment" data-fragment-index="2" -->

`[a, book, about, information, retrieval]` <!-- .element: class="fragment" data-fragment-index="2" -->

> "Information Retrieval": Also available as e-book! <!-- .element: class="fragment" data-fragment-index="3" -->

&darr; <!-- .element: class="fragment" data-fragment-index="4" -->

`[Information Retrieval]? [Information, Retrieval]?` <!-- .element: class="fragment" data-fragment-index="4" -->

`[e-book]? [eBook]? [e, book]?` <!-- .element: class="fragment" data-fragment-index="4" -->

Bilješke:
---

# Izazov

Obrnuto kazalo može pronaći samo točne tokene

| Pojam        | ID-ovi dokumenata |
|--------------|-------------------|
| book         | #1, #2, #3        |
| information  | #1, #2, #3        |
| retrieval    | #1                |
| search       | #2                |

_e-book_ neće uzvratiti nikakve rezultate!

Bilješke:
---

<!-- .slide: class="audience-question" -->

# Izazov

* Kako _books_ može pronaći _book_?
* _wi-fi_ &leftrightarrow; _wifi_?
* &shy;<!-- .element: class="fragment" --> _Jack's_ &leftrightarrow; _Jack_?
* &shy;<!-- .element: class="fragment" --> _Unizd_ &leftrightarrow; _University of Zadar_?
* &shy;<!-- .element: class="fragment" --> _U.S.A._ &leftrightarrow; _USA_?
* &shy;<!-- .element: class="fragment" --> _running_ &leftrightarrow; _run_?

Bilješke:
Koji su drugi primjeri?
---

# Analiza teksta

* Analizirajte dokumente i upite
* Dodajte, uklonite ili izmijenite pojmove

Bilješke:
---

# Terminologija

<dl>
    <dt>Token</dt><!-- .element: class="fragment" data-fragment-index="1" -->
    <dd>
        <ul>
            <li>Slijed znakova, značajna semantička jedinica</li>
            <li>Još nema analize</li>
            <li><em>the</em>, <em>routers</em>, <em>the</em></li>
        </ul>
    </dd><!-- .element: class="fragment" data-fragment-index="1" -->
    <dt>Vrsta</dt><!-- .element: class="fragment" data-fragment-index="2" -->
    <dd>
        <ul>
            <li>Jedinstveni tokeni, isti token broji se samo jednom</li>
            <li><em>the</em>, <em>routers</em></li>
        </ul>
    </dd><!-- .element: class="fragment" data-fragment-index="2" -->
    <dt>Pojmovi</dt><!-- .element: class="fragment" data-fragment-index="3" -->
    <dd>
        <ul>
            <li>Tokeni za indeksiranje</li>
            <li><em>router</em></li>
        </ul>
    </dd><!-- .element: class="fragment" data-fragment-index="3" -->
</dl>
