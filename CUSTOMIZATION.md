# Guida rapida — profilo GitHub di Marco Amantea

## Pubblicazione

1. Apri il repository **`MarcoAmantea/MarcoAmantea`**: deve essere **pubblico** e contenere `README.md` nella root.
2. Carica i file del pacchetto mantenendo esattamente le cartelle. I file rimasti nella vecchia repository non vengono rimossi automaticamente dal caricamento: elimina manualmente i vecchi workflow duplicati.
3. Vai nella scheda **Actions**, seleziona **Update contribution snake**, poi **Run workflow** per forzare il primo aggiornamento.
4. Se il job non riesce a effettuare il commit, verifica in **Settings → Actions → General → Workflow permissions** che sia consentita la scrittura a GitHub Actions, e verifica eventuali branch protections.
5. Apri `https://github.com/MarcoAmantea` da desktop e da smartphone per controllare banner, collegamenti e progetti.

## File che guidano il design

- `README.md`: contenuti, sezioni, link, anteprime e interazioni `<details>`.
- `assets/hero-dark.svg` e `assets/hero-light.svg`: banner vettoriali, con piccoli effetti CSS e fallback statico; il colore si adatta al tema di GitHub.
- `assets/process-dark.svg` e `assets/process-light.svg`: grafica del processo.
- `assets/projects/*.png`: quattro cover dei progetti create a partire dalle immagini originali caricate.
- `.github/workflows/snake.yml`: **unico** workflow snake, giornaliero/manuale, scrive su `output/` del branch principale.
- `output/github-contribution-grid-snake*.svg`: immagini già incluse per apparire anche prima della prima esecuzione dell'Action.

## Limiti tecnici di GitHub README

Un README non è un sito web: **JavaScript, `<script>`, `<iframe>`, CSS arbitrario e veri pulsanti applicativi non sono utilizzabili direttamente.** Sono supportati link cliccabili, immagini SVG/GIF e sezioni espandibili con `<details>`. Animazioni SVG possono dipendere dal client e dalla cache delle immagini GitHub; per questo i banner sono leggibili anche da fermi.

Le statistiche `github-readme-stats` e `github-readme-activity-graph`, nonché i badge e le icone, vengono caricati da servizi esterni; i contenuti principali e i banner sono locali.

## Link e contenuti da controllare

- I link Google Play sono stati conservati dal README originale e risultano pubblici alla verifica del 19 novembre 2026; la disponibilità dipende dal paese e dallo store.
- Titoli e descrizioni riprendono quelli presenti nel pacchetto originale. Evita indicatori di performance non misurati.
- Il file preesistente `public/index.html` nello ZIP contiene una pagina personale **non correlata al profilo professionale**. Non è stato modificato e può risultare accessibile pubblicamente se la repository è pubblica. Valuta se tenerlo online.
- Sono stati conservati i materiali originali non utilizzati e le immagini già presenti, per non rompere eventuali riferimenti di altri progetti.

## Personalizzazioni rapide

- Colori: blu `#0E79F2`, verde `#2CD562`, fondo navy `#06111F`.
- Testi in italiano in `README.md`.
- Se cambiano i progetti, modifica le due righe HTML della griglia `Selected work`.
- In `.github/workflows/snake.yml` trovi la frequenza di aggiornamento (`cron`).

## Nota sulla privacy

Il vecchio README includeva un collegamento WhatsApp con numero di telefono; il restyling mantiene email, sito, Instagram e LinkedIn come canali pubblici, ma non ripubblica il numero di telefono.
