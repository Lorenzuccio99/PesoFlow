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


## Aggiornamento v1.1
- eliminato l'effetto di aree bianche durante lo scroll su iPhone usando uno scroll container interno full-screen
- rimossa la barra esterna del dock: restano solo i pulsanti/glass cluster
- ottimizzato il foglio "Registra peso" per iPhone 15 con altezza adattiva e spazi più compatti


## Aggiornamento v1.2
- sfondo esteso fino alle safe-area inferiori, senza fascia quasi nera
- dock abbassato verso il bordo inferiore su iPhone
- header data/orario spostato leggermente più in basso
- finestra Registra peso limitata al 76% del viewport con scroll interno
- zoom/pinch e doppio tap zoom disabilitati nell'interfaccia PWA
- cache PWA aggiornata a v12 per forzare il refresh della nuova UI


## v1.3.1 STABLE
- rollback della modifica `body: fixed` che poteva rompere la PWA installata su iOS
- eliminato il doppio handler JavaScript per il blocco zoom
- mantenuto scroll nativo della pagina e hide/show del dock
- campi Data/Orario dimensionati senza disabilitare i controlli nativi iOS
- sfondo/theme color uniformati per ridurre bande diverse nelle safe-area
