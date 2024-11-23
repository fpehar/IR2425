# Korjenovanje (eng. Stemming)

Bilješke:
---
# Stemming

* Reducira završetke riječi kako bi se pronašao zajednički korijen:
    * *housing*, *houses*, *house* &rarr; *hous*
* Heuristički pristup, nije lingvistički
* Može pronaći zajednički korijen za različite koncepte:
    * *organic* &rarr; *organ*

Bilješke:
---
# Porterov algoritam za korjenovanje

Implementiran u Snowball Stemming DSL

| Podudaranje | Zamjena | Primjer                            |
|-------------|---------|------------------------------------|
| SSES        | SS      | caresses &rarr; caress             |
| IES         | I       | ponies &rarr; poni, ties &rarr; ti |
| SS          | SS      | caress &rarr; caress               |
| S           | _prazno_ | cats &rarr; cat                   |

… i tako dalje

Isključivo algoritamski, bez lingvističkog znanja. No, obično dovoljno dobar.

Bilješke:
---
# Lemmatizacija

* Određuje korijen na temelju lingvističkih pravila
* Zadržava vrstu riječi:
    * *A saw* &rarr; *saw*, *I saw* &rarr; *see*
* Može generirati fleksije, npr., što je množina od *house*?
* Prednosti lematizacije nad korjenovanjem su upitne

Bilješke:
