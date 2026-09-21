# Come si aggiunge un articolo

1. Crea una cartella con lo **slug** dell'articolo:
   `approfondimenti/<slug>/index.html`
   Lo slug è il titolo in minuscolo, senza accenti né parole di servizio:
   `perche-ho-iniziato-a-costruire-ai-brand-system`

2. Copia dentro il file di un articolo esistente e cambia:
   - `<title>` e `<meta name="description">`
   - i tre `og:` (titolo, descrizione, immagine)
   - `<span class="tag">` (Metodo · Note di progetto · Esempi)
   - `<time datetime="AAAA-MM-GG">` e la data scritta
   - la durata di lettura (circa 180 parole al minuto)
   - `<h1>`, il sommario `.somm`, la copertina e il corpo

3. **Copertina**: 1600×900, webp, in `assets/blog-NN-<slug-corto>.webp`.
   Si compone con un file HTML temporaneo: fondo `#1a2b1e`, titolo in
   Augustina Light crema con il nome del servizio in `#d14124`, illustrazione
   isometrica a destra su fondo trasparente. L'illustrazione senza testo va
   archiviata in `90. Illustrazioni-sorgente/`.

4. **Aggiungi la scheda in cima all'elenco** in `approfondimenti/index.html`:
   duplica il blocco `<a class="pezzo">` e aggiorna link, immagine, tag, data,
   durata, titolo e occhiello. Il più recente sta per primo.

5. Lo stile è tutto in `approfondimenti/_stile.css`, condiviso fra indice e
   articoli. Non serve toccarlo per pubblicare.

## Da sapere

- Le pagine sono in **`noindex,nofollow`** e **non sono linkate dalle due
  landing**: è una scelta di Alessio del 21 settembre 2026. Per aprirle ai
  motori di ricerca basta togliere la riga `<meta name="robots">` da ogni
  pagina e aggiungere un link nella navigazione delle landing.
- I percorsi sono **assoluti** (`/assets/…`), non relativi: un articolo sta
  due livelli sotto la radice e i percorsi relativi si romperebbero.
- Prima di pubblicare: passare le larghezze 390/600/900/1280 e controllare che
  `document.documentElement.scrollWidth` non superi la finestra.
