# Primjer analize

Bilješke:
---
<table class="stretch">
    <tr>
        <th style="border-right: 1px solid rgb(34, 34, 34);"></th>
        <th colspan="7" style="border-right: 1px solid rgb(34, 34, 34);">Dokument</th>
        <th colspan="2">Upit</th>
    </tr>
    <tr>
        <td style="border-right: 1px solid rgb(34, 34, 34);"></td>
        <td colspan="7" style="border-right: 1px solid rgb(34, 34, 34);"><span class="fragment"
                                                                               data-fragment-index="1">A Wi-Fi Router</span>
        </td>
        <td colspan="2"><span class="fragment" data-fragment-index="1">wireless routers</span></td>
    </tr>
    <tr>
        <td style="border-right: 1px solid rgb(34, 34, 34);">Tokenizacija</td>
        <td><span class="fragment" data-fragment-index="2">A</span></td>
        <td><span class="fragment" data-fragment-index="2">Wi-Fi</span></td>
        <td colspan="5" style="border-right: 1px solid rgb(34, 34, 34);"><span class="fragment"
                                                                               data-fragment-index="2">Router</span>
        </td>
        <td><span class="fragment" data-fragment-index="9">wireless</span></td>
        <td><span class="fragment" data-fragment-index="9">routers</span></td>
    </tr>
    <tr>
        <td style="border-right: 1px solid rgb(34, 34, 34);">Pretvaranje u mala slova</td>
        <td><span class="fragment" data-fragment-index="4">a</span></td>
        <td><span class="fragment" data-fragment-index="4">wi-fi</span></td>
        <td colspan="5" style="border-right: 1px solid rgb(34, 34, 34);"><span class="fragment" data-fragment-index="4">router</span>
        </td>
        <td><span class="fragment" data-fragment-index="10">wireless</span></td>
        <td><span class="fragment" data-fragment-index="10">routers</span></td>
    </tr>
    <tr>
        <td style="border-right: 1px solid rgb(34, 34, 34);">Zaustavne riječi</td>
        <td></td>
        <td><span class="fragment" data-fragment-index="5">wi-fi</span></td>
        <td colspan="5" style="border-right: 1px solid rgb(34, 34, 34);"><span class="fragment" data-fragment-index="5">router</span>
        </td>
        <td><span class="fragment" data-fragment-index="11">wireless</span></td>
        <td><span class="fragment" data-fragment-index="11">routers</span></td>
    </tr>
    <tr>
        <td style="border-right: 1px solid rgb(34, 34, 34);">Razdjelnici riječi<br>(samo za indeks)</td>
        <td></td>
        <td><span class="fragment" data-fragment-index="6">wi-fi</span></td>
        <td><span class="fragment" data-fragment-index="6">wi</span></td>
        <td><span class="fragment" data-fragment-index="6">fi</span></td>
        <td><span class="fragment" data-fragment-index="6">wifi</span></td>
        <td colspan="2" style="border-right: 1px solid rgb(34, 34, 34);"><span class="fragment" data-fragment-index="6">router</span>
        </td>
        <td><span class="fragment" data-fragment-index="12">wireless</span></td>
        <td><span class="fragment" data-fragment-index="12">routers</span></td>
    </tr>
    <tr>
        <td style="border-right: 1px solid rgb(34, 34, 34);">Stemming</td>
        <td></td>
        <td><span class="fragment" data-fragment-index="7">wi-fi</span></td>
        <td><span class="fragment" data-fragment-index="7">wi</span></td>
        <td><span class="fragment" data-fragment-index="7">fi</span></td>
        <td><span class="fragment" data-fragment-index="7">wifi</span></td>
        <td colspan="2" style="border-right: 1px solid rgb(34, 34, 34);"><span class="fragment" data-fragment-index="7">router</span>
        </td>
        <td><span class="fragment" data-fragment-index="13">wireless</span></td>
        <td><span class="fragment" data-fragment-index="13">router</span></td>
    </tr>
    <tr>
        <td style="border-right: 1px solid rgb(34, 34, 34);">Sinonimi<br>wifi &rarr; wireless<br>(samo za indeks)</td>
        <td></td>
        <td><span class="fragment" data-fragment-index="8">wi-fi</span></td>
        <td><span class="fragment" data-fragment-index="8">wi</span></td>
        <td><span class="fragment" data-fragment-index="8">fi</span></td>
        <td><span class="fragment" data-fragment-index="8">wifi</span></td>
        <td><span class="fragment" data-fragment-index="8">
            <span class="fragment highlight-blue" data-fragment-index="15">wireless</span>
        </span></td>
        <td style="border-right: 1px solid rgb(34, 34, 34);"><span class="fragment" data-fragment-index="8">
            <span class="fragment highlight-blue" data-fragment-index="15">router</span>
        </span></td>
        <td><span class="fragment" data-fragment-index="14">
            <span class="fragment highlight-blue" data-fragment-index="15">wireless</span>
        </span></td>
        <td><span class="fragment" data-fragment-index="14">
            <span class="fragment highlight-blue" data-fragment-index="15">router</span>
        </span></td>
    </tr>
</table>

Bilješke:
Povećava relevantnost, ali smanjuje preciznost
---
![analysis](images/analysis.png)

Bilješke:
---

<!-- .slide: class="audience-question" -->

# Ishod

* &shy;<!-- .element: class="fragment" --> Pronađite više rezultata: _wireless_ &rarr; _wi-fi_
* &shy;<!-- .element: class="fragment" --> Pronađite više nepreciznih rezultata: _wi-fi_ &rarr; _wireless_
* &shy;<!-- .element: class="fragment" --> Propustite neke rezultate: _to be or not to be_

Bilješke:

* Hoće li ovo pronaći više rezultata?
* Hoće li ovo pronaći manje točne rezultate?
