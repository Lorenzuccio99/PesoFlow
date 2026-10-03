# PesoFlow — PWA per GitHub Pages

Questa cartella contiene la versione web installabile di PesoFlow.

## Funzionamento
- GitHub Pages ospita soltanto i file HTML/JS/CSS dell'app.
- Le pesate restano sul dispositivo nel browser (localStorage).
- Dopo il primo caricamento online, il Service Worker consente l'apertura offline.
- Il backup JSON dell'app resta il metodo consigliato per proteggere i dati.

## Pubblicazione su GitHub Pages
1. Carica **il contenuto di questa cartella** nella root del repository.
2. Repository GitHub -> Settings -> Pages.
3. Source: `Deploy from a branch`.
4. Branch: `main`, folder: `/(root)`.
5. Salva e attendi il link GitHub Pages.

## Installazione su iPhone
1. Apri il link GitHub Pages in Safari.
2. Tocca Condividi.
3. Tocca `Aggiungi alla schermata Home`.
4. Apri PesoFlow dalla nuova icona.
5. Aprila almeno una volta con connessione prima di provarla offline.

## Aggiornamenti futuri
Sostituisci `index.html` con la nuova versione e, se modifichi gli asset, cambia il valore di `CACHE_NAME` in `sw.js` (es. `pesoflow-pwa-v2`) per forzare l'aggiornamento della cache.


## v1.4 CLEAN
Ricostruzione pulita del layout iPhone dalla PWA stabile: nessun body fixed, nessuno scroll container interno. Dock ancorato al viewport, data/ora in wrapper dedicati, sfondo full-viewport e modal compatto.


## Aggiornamento v1.4.1
- tastiera numerica/decimale dedicata per il peso con filtro dei caratteri non numerici
- Data e Orario centrati nei controlli iOS
- dock alzato leggermente rispetto al bordo inferiore seguendo la curva dell’iPhone


## v1.4.2
- Data e Orario centrati otticamente su iOS tramite un testo visuale indipendente dal controllo nativo.
- Il tap continua ad aprire il picker nativo iOS.
