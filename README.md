# Football Schemes — Editor Schemi Calcistici

Editor tattico calcistico interamente client-side, single-file HTML. Nessun backend, nessuna installazione: basta aprire `index.html` nel browser.

## Funzionalità

### Campo
- Campo da calcio con strisce alternate e segnature (aree, cerchio di centrocampo, porte)
- Adattamento automatico alla dimensione della finestra (responsive)
- Supporto immagine di sfondo personalizzata al posto del campo disegnato

### Giocatori
- Due squadre: **Casa** e **Ospite**, fino a 22 giocatori totali
- Colori personalizzabili per ciascuna squadra (sfondo, testo, bordo)
- Drag & drop per posizionare i giocatori sul campo (touch-friendly)
- **Doppio click** sul pallino per modificare il numero direttamente inline
- Formazioni preimpostate: `4-4-2`, `4-3-3`, `3-5-2`, `4-2-3-1`, `4-3-1-2`, `3-4-3`

### Pallone
- Pallone ⚽ draggabile aggiungibile/rimuovibile dal campo
- Salvato nello schema JSON e visibile nell'export

### Linee / Frecce
- Due tipologie: **Passaggio** (tratteggiato) e **Movimento** (continuo)
- Per tracciare: clicca un giocatore → scegli il tipo dal popover in basso a destra → clicca la destinazione
- **Anteprima in tempo reale**: la freccia segue il cursore prima di confermare
- **Linee curve**: handle rosso al centro della linea selezionata — trascinalo per curvare
- Colore personalizzabile per ogni linea

### Modifica linee
Cliccando su una freccia si apre il pannello in basso a destra con:
- Cambio tipo (Passaggio / Movimento)
- Cambio colore
- **Handle giallo** sulla punta: trascinalo per riposizionare la destinazione, rilascialo su un giocatore per agganciarlo
- Elimina

### Esporta
- **JPG** — immagine ad alta risoluzione (scala 3×)
- **PDF** — foglio A4 con titolo, legenda, nomi squadre, nome allenatore e link GitHub

### Salva / Carica
- Salva lo schema in formato **JSON** (include titolo, allenatore, giocatori, linee, pallone)
- Carica uno schema precedentemente salvato
- Reset completo

## Utilizzo

```
Apri index.html nel browser
```

Nessuna dipendenza da installare. Le librerie esterne (html2canvas, jsPDF, Google Fonts) vengono caricate via CDN.

## Struttura

```
index.html   — tutta l'applicazione (HTML + CSS + JS)
LICENSE
```

## Tecnologie

- HTML5 Canvas (campo)
- SVG (frecce bezier)
- Vanilla JS (nessun framework)
- [html2canvas](https://html2canvas.hertzen.com/) — export immagine
- [jsPDF](https://github.com/parallax/jsPDF) — export PDF
