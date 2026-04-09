# Tactical Board — Editor Schemi Calcistici

Editor tattico calcistico interamente client-side, single-file HTML. Nessun backend, nessuna installazione: basta aprire `index.html` nel browser.

## Funzionalità

### Campo
- Campo da calcio con strisce alternate e segnature (aree, cerchio di centrocampo, porte)
- Adattamento automatico alla dimensione della finestra (responsive)

### Giocatori
- Due squadre: **Casa** e **Ospite**, fino a 22 giocatori totali
- Colori personalizzabili per ciascuna squadra (sfondo, testo, bordo)
- Drag & drop per posizionare i giocatori sul campo
- Formazioni preimpostate: `4-4-2`, `4-3-3`, `3-5-2`, `4-2-3-1`, `4-3-1-2`, `3-4-3`

### Linee / Frecce
- Due tipologie: **Passaggio** (tratteggiato) e **Movimento** (continuo)
- Per tracciare una linea: clicca un giocatore → scegli il tipo dal popover → clicca la destinazione
- **Anteprima in tempo reale**: la freccia segue il cursore prima di confermare la destinazione
- Colore personalizzabile per ogni linea

### Modifica linee
Cliccando su una freccia appare un popover con:
- Cambio tipo (Passaggio / Movimento)
- Cambio colore
- **Handle giallo** sulla punta: trascinalo per riposizionare la destinazione; rilascialo su un giocatore per agganciarlo
- Sposta destinazione (ri-disegna la linea dallo stesso punto di partenza)
- Elimina

### Esporta
- **JPG** — immagine ad alta risoluzione (scala 3×)
- **PDF** — foglio A4 con titolo e legenda

### Salva / Carica
- Salva lo schema in formato **JSON**
- Carica uno schema precedentemente salvato
- Reset completo

## Utilizzo

```
Apri index.html nel browser
```

Nessuna dipendenza da installare. Le librerie esterne (html2canvas, jsPDF, Google Fonts) vengono caricate via CDN.

## Struttura

```
index.html   — tutta l'applicazione (HTML + CSS + JS, ~420 righe)
LICENSE
```

## Tecnologie

- HTML5 Canvas (campo)
- SVG (frecce)
- Vanilla JS (nessun framework)
- [html2canvas](https://html2canvas.hertzen.com/) — export immagine
- [jsPDF](https://github.com/parallax/jsPDF) — export PDF
