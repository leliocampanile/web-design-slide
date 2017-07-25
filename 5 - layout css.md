# Layout dei siti senza tabelle

- Semplice è meglio
- layout a singola colonna
- layout a due colonne
- layout a tre colonne

---

# Per creare impaginazioni senza tabelle è fondamentale l'uso dei __CSS__

---

# Layout con i css (fogli di stile)

- le tabelle sono per i dati tabellari non per i layout!!
- separazione tra contenuti e presentazione
	- codice html più pulito
	- rapidità del caricamento
	- manutenzione più semplice

---

# Layout con i css (fogli di stile)

- con i css è più facile mantenere la coerenza grafico/stilistica del sito
- Possibilità di realizzare siti responsive
- delineano maggiore professionalità

---

# Contenuto e presentazione

## Il contenuto è nella pagina HTML
## La presentazione è affidata ai CSS

---

# Elemento DIV

DIV: _generic block-level element_ 
- può contenere qualsiasi blocco html
- presentazione di default neutra
- contenitore ideale per impostare layout senza tabelle

---

# Le sezioni logiche di una pagina web

- Header (Testata)
- La Navigazione
- I Contenuti
- Il Footer (piè di pagina)
- Extra

---

# Testata (Header)

- si estende orizzontalmente in alto 
- tipicamento alto c.a 80, 100, 150px
- riporta il logo ed il nome del sito
- a volte riporta anche un sottotitolo
- è linkabile e il link riporta alla home page

---

# Navigazione (Menù)

- Permette l'accesso ai contenuti
- rende "utilizzabile" l'albero di navigazione agli utenti
- visibile e distinguibile dal resto del sito
- consente di raggiungere i contenuti con pochi click (idealmente max 3)

---

# Navigazione (Menù)

- I contenuti devono essere accedibili senza l'uso dei tasti avanti e dietro del browser
- utilizzare un breadcrumb per evidenziare all'utente dove è
- per alberi molto complessi prevedere un __menù secondario__
- I link esterni al sito se presenti nel menù devono essere ben distinguibili dagli interni

---

# Contenuti (Main)

### La parte principale del sito, dove risiede l'interesse di un sito.

---

# Pié di Pagina (Footer)

- Sezione finale di un sito
- si estende orizzontalmente in basso alla pagine
- in genere contiene informazioni di servizio: nome dello sviluppatore, indirizzo, partita iva, ecc...

---

# Extra

Sezione non obbligatoria che può contenute varie informazioni:

- sezioni o aticoli in evidenza
- News
- sponsor e/o pubblicità
- sondaggi
- form di iscrizione newsletter ...

---

#Tipi di Layout

Il layout mappa le sezioni logiche in corrispondenti sezioni fisiche della pagina web.

- Layout a singola colonna
- Layout a 2 colonne
- Layout a 3 colonne

---

# Estenzione orizzontale di un layout

- Layout fisso
- Layout fluido 
- Layout elastico

---

# Layout fluido

Sono i layout che variano la larghezza al variare della finestra del browser.

è stato un tipo di layout molto utilizzato e tuttora, con alcune varianti è utilizzato. 

è adatto le i contenuti web che devono essere stampati.

---

# Layout fisso

- un layout fluido è generalmente studiato su una risoluzione standard:  1024 x 768
- in genere si lasciano 40/50 pixel com margine
- quindi si ottiene la larghezza standard di __960px__

---

# Layout fisso

## Codice di esempio

	body{
    	text-align: center;   /*centra in IE */
    	}

	div#container{
    	width: 960px;
    	margin: 0px auto;   /*centra negli altri browsers*/
    	text-align: left;   /*ripristina l’ allineamento*/
    	}
    	
---
# Layout elastico

Utilizza il dimensionamento in __em__ per gli elementi della pagina.

__em__: unità di misura di ampio utilizzo per impostare le dimensioni di font e div box con una unità di misura relativa.

Si inizio impostando il font del body in em, quindi si imposta in em anche gli altri elementi.

l'effetto finale è che il sito si ridimensiona in base alle dimensioni del font impostato nel browser.

---

# Layout elastico

## Codice d'esempio

	body{
    	font-size: 76%;   /*dimensionamento percentuale del font 	*/
    	text-align: center;   /*centra in IE */
    	}

	div#container{
    	width: 60em;   /*dimensionamento in em del container principale */
    	margin: 0px auto;   /*centra negli altri browsers*/
    	text-align: left;   /*ripristina l’ allineamento*/
    	}

---

# Layout monolitico (1 Colonna)

Layout sempice:

1. header
2. navigazione
3. contenuti
4. footer

---

# Layout monolitico (1 Colonna)

## Esempio di codice

	<body>
    	<div id=”container”> 
    	/* contenitore padre, serve per poter 
    	modifica l'estensione orizzontale tramite css*/
        	<div id=”header”></div>
        	<div id=”navigation”></div>
        	<div id=”content”></div>
        	<div id=”footer”></div>
    	</div>
	</body>

---

# Layout monolitico (1 colonna)

![monolitico](http://html.it/guide/img/layout_css/mono.gif)

---
# Layout a 2 o 3 colonne

In un layout a 2 colonne la colonna dovrebbe essere posizionata a sinistra.

Se si necessità di aggiungere un'ulteriore colonna, verrà posizionata a destra.

Si possono posizionare in 2 modi:

- attraverso il posizionamento: assoluto o relativo
- attraverso la proprietà __float__ ed i margini.

---

# La larghezza delle colonne

- larghezza percentuali
- larghezza fissa
- elastiche

---

# La larghezza delle colonne

L'approccio da utilizzare è quello a larghezza fissa

Gli altri 2 approcci sono decisamente poco utilizzati

---

# Layout a 2 colonne

Elementi logici della pagina:

1. header
2. navigazione
3. contenuti
4. footer

---


# Layout a 2 colonne 

![2colonne](http://html.it/guide/img/layout_css/duecolonne.gif)

---

# Layout a 2 colonne

## codice di esempio

    <body>
       <div id=”container”>
        <div id=”header”></div>
        <div id=”navigation”></div>
        <div id=”content”></div>
        <div id=”footer”></div>
    </div>
</body>

---

# Layout a 3 colonne

- header
- navigazione
- contenuti
- __extra__
- footer

---

![3colonne](http://html.it/guide/img/layout_css/trecolonne.gif)

---

# Larghezza delle colonne

In genere le colonne laterali sono fisse: 150/200px

La colonna centrale si lascia fluida

