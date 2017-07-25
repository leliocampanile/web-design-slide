# Il web design con le griglie

La moderna tendenza nel mondo del web design è quella di utilizzare le griglie per la visualizzazioni dei contenuti.

![inline](grid1.png)

---

# Vediamo come si fà

## 1 Impostiamo il box-sizing 

```css
* {
    box-sizing: border-box;
}
```

---

# Approfondiamo il box-sizing

Di default la dimensione di un elemento è calcolata come:

__element total width =  width + padding + border__

questo significa che la dimensione effettiva di un elemento è maggiore del width e questo può creare dei problemi.

---

# Approfondiamo il box-sizing

impostando la regola: _box-sizing: box-border_

__element total width =  width__

il padding ed il border vengono inclusi nel width.

---

# 2. impostiamo le colonne

```css
.col-1 {width: 8.33%;}
.col-2 {width: 16.66%;}
.col-3 {width: 25%;}
.col-4 {width: 33.33%;}
.col-5 {width: 41.66%;}
.col-6 {width: 50%;}
.col-7 {width: 58.33%;}
.col-8 {width: 66.66%;}
.col-9 {width: 75%;}
.col-10 {width: 83.33%;}
.col-11 {width: 91.66%;}
.col-12 {width: 100%;}
```

---

# 3. proprietà comuni per le colonne

```css
[class*="col-"] {
    float: left;
    padding: 15px;
    border: 1px solid red;
}
```

---

# 4. le righe

Le righe servono a contenere le colonne per avere maggiore flessibilità nel layout

```css
.row::after {
    content: "";
    clear: both;
    display: block;
}
```

ˆ serve poiche le colonne sono tutte float a sinistra e per evitare che altri elementi occupino lo spazio delle colonne


---

# HTML per un layout a 2 colonne con le griglie

```html
<div class="row">
  <div class="col-3">...</div>
  <div class="col-9">...</div>
</div>
```

---

![fit](grid2.png)

---

# Adattiamolo per il mobile: Media Query

La nostra griglia adesso è fluida è si ridimensiona correttamente,

__Cosa manca??__

Ridefinire il layout per i dispositivi con lo schermo più piccoli

---

![fit](grid3.png)


---
# Aggiungiamo in breackpoint

```css
@media only screen and (max-width: 768px) {
    /* For mobile phones: */
    [class*="col-"] {
        width: 100%;
    }
}
```

---

# Aggiungiamo un'altro breackpoint (es. tablet)

@media only screen and (min-width: 600px) {
    /* For tablets: */
    .col-m-1 {width: 8.33%;}
    .col-m-2 {width: 16.66%;}
    .col-m-3 {width: 25%;}
    .col-m-4 {width: 33.33%;}
    .col-m-5 {width: 41.66%;}
    .col-m-6 {width: 50%;}
    .col-m-7 {width: 58.33%;}
    .col-m-8 {width: 66.66%;}
    .col-m-9 {width: 75%;}
    .col-m-10 {width: 83.33%;}
    .col-m-11 {width: 91.66%;}
    .col-m-12 {width: 100%;}
}

---

# Ma è uguale a prima??

Queste regole sono identiche a quelle scritte per il desktop!!

Cambia solo il nome:  __.col-m-x__

A cosa serve??  Serve a poter devidere nell'html una diversa disposizione delle colonne per questa dimensione dello schermo.

---

# Es. HTML

```html
<div class="row">
<div class="col-3 col-m-3">...</div>
<div class="col-6 col-m-9">...</div>
<div class="col-3 col-m-12">...</div>
</div>
```

---
# Nota sul container

La griglia che abbiamo preparato è fluida e quindi se non oppotunamente vincolata utilizzerà comunque tutto lo spazio orizzontale disponibile.

Questo su schermi grandi è sgradevole, risolviamo utilizzando un div contenitore che imposya i margini:

```css
    .grid-container {
        width : 100%;
        max-width : 1200px; 
    }
```

---

# HTML

```html
<div class="grid-container">
    <div class="row">
        <div class="col-1"><p>col-1</p></div> 
        <div class="col-1"><p>col-1</p></div> 
        <div class="col-1"><p>col-1</p></div> 
        <div class="col-1"><p>col-1</p></div> 
        <div class="col-1"><p>col-1</p></div> 
        <div class="col-1"><p>col-1</p></div> 
    </div> 
</div>
```
---

# Rendere responsive le immagini.

Il nostro layout è responsive, le nostre immagini no.

Le immagini sono statiche e di dimensioni fisse, come possiamo farle scalare insieme al layout??

---

# Soluzione 1

```css
img {
    width: 100%;
    height: auto;
}
```

---
# Soluzione 2

```css
img {
    max-width: 100%;
    height: auto;
}
```

---
# cosa cambia tra le 2 soluzioni?

Nella prima soluzione la nostra immagine scalera verso l'alto all'infinito, potendo quindi diventare un'immagine sgranata.

Nella seconda soluzione, invece scalerà verso l'alto fino alla sua dimensione massima.

In entrambi i casi scal verso il basso correttamente.




