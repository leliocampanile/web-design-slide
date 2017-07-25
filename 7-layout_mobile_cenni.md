# Differenze tra Desktop e Mobile

## I browser

Anche in ambito mobile esistono vari browser, ognuno con le sue peculiarità, in più nell'ambito mobile le differenze sono anche marcate dal produttore e dal sistema operativo:

1. apple - safari mobile
2. android - chrome mobile
3. microsoft - explorer mobile

---

# Differenze tra Desktop e Mobile

## risoluzione e dimensione dello schermo

I dipositivi mobili hanno una grande varietà di risoluzioni da 480px X 320px fino a risoluzioni HD e retina.

---

# Differenze tra Desktop e Mobile

## risoluzione e dimensione dello schermo

Ma in generale gli schermi sono più piccoli:

- smartphone da 3" a 6"
- tablet da 7" a 11/12"

---

# Differenze tra Desktop e Mobile

## Contesto ambientale e orientamento dello schermo

Gli utenti mobile sono abituati a ruotare il dispositivo in continuazione. Cambio di orientamanto dello schermo da orizzontale (__landscape__) a verticale (__portrait__) e vice versa.

---

# Differenze tra Desktop e Mobile

## Contesto ambientale e orientamento dello schermo

Un dispositivo mobile è utilizzato in contesti ricchi di stimoli esterni, quindi è bene essere diretti nel fornire le informazioni.


---

# Differenze tra Desktop e Mobile

## Caricamento delle pagine

La velocità di navigazione in mobilità è molto varia! 

Potrebbe essere sensibilmente più lenta di una connessione fissa.

Le caraterristiche hardware sono __ridotte e diverse__ rispetto ad un PC

---

# Differenze tra Desktop e Mobile

## I browser mobile

I browser mobile sono snelli ed efficienti, girano su dispositivo con capacità limitate.

L'interazione è diversa, touch o in alcuni casi tramite joystick

I contenuti spesso vengo zoomati per la fruizione.

---

# Pensare il proprio sito responsive

## Primo approccio

__Responsive:__ Adattivo, che si adatta al dispositivo

Uso della direttiva CSS  __viewport__, che in base alla larghezza della finestra del browser cambia i css e il layout

---

# Esempio di CSS Responsive

```css
@media screen and (max-width: 1024) {
    .colonna1,
    .colonna2 { 
        width: 50%;
    }
    .colonna1 {
        float: left;
    }
    .colonna2 { 
        float: right;
    } 
}
```
^ questo css viene applicato a tutti i viewport fino a 1024 px e crea le 2 colonne affiancate
---

# Esempio di CSS Responsive

```css
@media screen and (max-width: 480) {
    .colonna1,
    .colonna2 { 
        width: 100%;
        float: none
    }
}
```

^ questo css invece fa on modo che per i viewport inferiori a 480px le colonne occupino in larghezza il 100% e quindi si dispongano una sotto l'altra

---

# Limiti dell'approccio precedente

## bisogna comunque adattare i css per tutte le larghezze di viewport che si vogliono ottimizzare

---

# Superare i limiti precedenti

1. oltre i media query css (visti primi)
2. griglie fluide
3. Immagini flessibili


---

# Adaptive Design

## Oltre il layout responsive

Un dispositivi mobile ha altre caratteristiche perculiari oltre la dimensione della finesta del browser:

- gps
- telefonate
- sms
- fotocamera
- ecc...

---

# Adaptive design

## Sfuttiamo le caratteristiche del dispositivo per aggiungere funzionalità esclusive della versione mobile.

---
# Obiettivi minimi di un design responsive

1. Adattare il layout al numero maggiore di schermi
2. Adattare le immagini alle dmensioni dello schermo
3. offrire immagini meno pesanti ai dispositivi con banda limitata
4. semplificare il layout su schermi piccoli

---

# Obiettivi minimi di un design responsive

1. nascondere elementi non essenziali su schermi piccoli
2. interfaccia touch
3. sfruttare le caratteristiche peculiari del dispositivo mobile

---

# Mobile first

Nella progettazione di un sito responsive si parte dal layout per i dispositivi mobili.

In questo layout si inseriranno tutti i componenti ed i contenuti essenziali

---

# Progressive Enhancement

Una volta stabilito il minino indispensabile per i dispositivi mobile, si procede ad un arricchimento di funzionalità per i dispositivi con schermi più grandi e maggiori disponibilità.

 



