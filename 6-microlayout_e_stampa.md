footer: Corso Web Design 2016
slidenumbers: true
# Microlayout

## Ovvero l'impaginazione dei contenuti centrali

Proprietà css __Float__ e __Clear__

__Float__: rende un elemento fluttuante a destra o sinistra (_left o right_) del suo contenitore, continuano disponendosi sotto

__Clear__: impedisce ad un elemento di avere dei float, può essere destra, sinistra o entrambi (_left, right, both_)

---

# Microlayout

## Testo + Immagini 

Il primo esempio è una composizione con un titolo, un testo ed un'immagine.

![inline](Testo1.jpg)

---

# Microlayout

## Testo + Immagini: codice html

```html
	<div class=”textimage”>
		<img src=”layout.jpg” alt=””>
		<h2>Layout</h2>
		<p>Qui il testo…</p>
			<div class=”clearer”> </div>
	</div>
```

---

# Microlayout

## Testo + Immagini: codice css

```css
	div.textimage{
		width: 400px;margin-bottom: 10px;     
		border: 1px solid #000;background-color: #eee
	}

	div.textimage img{
		float:left;
		margin: 10px
	}
```

---

# Microlayout

## Testo + Immagini: codice css
	
```css
	div.textimage h2, div.textimage p{
		margin:0 10px;
		padding: 0
	}

	div.textimage h2{
		margin-top: 10px
	}

	div.clearer{clear: left}
```
^ l'immagine viene resa float e distanziata dal contenitore tramite la proprietà margin, poi vengono impostati i margini per testo e titolo

---

# Microlayout

## 2 colonne per i contenuti

vediamo un esempio di testo su 2 colonne

![inline](Testo2.jpg)

---

# Microlayout

## 2 colonne per i contenuti: html

```html
<div class=”split2″>
    <div>
        <h2>Paragrafo 1</h2>
        <p>Testo del paragrafo 1..</p>
    </div>
    <div>
        <h2>Paragrafo 2</h2>
        <p>Testo del paragrafo 2..</p>
    </div>
    <div class=”clearer”> </div>
</div>
```

---

# Microlayout

## 2 colonne per i contenuti: css

```css
div.split2 div{
    float: left;
    width: 45%;
    width: 49%;
    width: 45%;
    padding: 0 2%
    }

div.clearer{
    float: none; clear: left
    }
```

^ Per ora non sono stati previsti stili sul contenitore, ma questi potrebbero coinvolgere larghezza, margini o padding. Il punto centrale di questo approccio è l’uso del selettore discendente: i due div contenuti all’interno del contenitore identificato dalla classe split2 saranno resi float e avranno una larghezza effettiva (padding incluso) pari al 49%

---

# Microlayout

## 3 colonne: solo un esercizio

![inline](Testo3.jpg)

---
# Microlayout

## 3 colonne: html

```html
<div class=”split3″>
    <div>
        <h2>Paragrafo 1</h2>
        <p>Testo del paragrafo 1..</p>
    </div>
    <div>
        <h2>Paragrafo 2</h2>
        <p>Testo del paragrafo 2..</p>
    </div>
    <div>
        <h2>Paragrafo 3</h2>
        <p>Testo del paragrafo 3..</p>
    </div>
    </div>
    <div class=”clearer”> </div>
</div>
```

---
# Microlayout

## 3 colonne:css

```css
div.split3 div{
    float: left;
    width: 29%;
    width: 33%;
    width: 29%;
    padding: 0 2%
    }
```

^ come prima un contenitore semi-fluido. stringendo il browser le colonne si sovrappongono, comportamenti diversi in base ai browser

---

# Il problema della stampa

### Le pagine web non vengono stampata male

### Perchè??

---

# Il problema della stampa

### Il motivo principale è che sono troppo larghe!!

### Le pagine web sono per lo schermo.

---

# Soluzioni

## 1. Definiamo il css solo per lo schermo e lasciamo le stampe senza alcun css.

```html
<meta http-equiv="content-type" content="text/html; charset=iso-8859-1″>              

@import url("stilisito.css"); 
```

---

# Soluzioni

## 2. Definiamo un css solo per la stampa

In questo modo oltre al css per lo schermo ne definiamo uno specifico per la stampa (__molto semplice__)

```html
<meta http-equiv="content-type" content="text/html; charset=iso-8859-1″>              

@import url("stilisito.css") screen;         
@import url("stilistampa.css") print; 
```

---

## Esempio di css per la stampa

```css
body{ font: 10pt arial, sans-serif}
h1,h2,h3,h4,h5,h6{font-family: georgia,serif} 
p{line-height: 1.2em} 
a{font-weight:bold} 
div#navigation, div#extra{display: none}
 /*non stampa le due colonne laterali*/
``` 




