# Armonia – sito demo con assistente Claude

## Pubblicare su Netlify (5 minuti)
1. Crea un account gratuito su netlify.com.
2. Carica questa cartella su un repository GitHub e collegalo a Netlify con "Add new site > Import an existing project".
   (Il trascinamento della cartella su app.netlify.com/drop pubblica solo la pagina, senza la funzione AI.)
3. In Site configuration > Environment variables aggiungi ANTHROPIC_API_KEY con la key presa da platform.claude.com.
   Facoltative: ANTHROPIC_MODEL (predefinito claude-haiku-5-5) e ANTHROPIC_VERSION (predefinito 2023-06-01; se l'API risponde con un errore di versione, usa quella indicata nella documentazione).
4. Fai un nuovo deploy. L'assistente ora risponde con Claude; senza key risponde dalle domande frequenti.

Consiglio: nella Console metti un limite di spesa basso sulla key e cancellala dopo l'hackathon.

## Prova veloce senza server
Apri index.html e scrivi la key in apiKey dentro ARMONIA_CONFIG, in cima al file.
Solo per prove sul tuo computer: chiunque apra la pagina può leggere la key. Non pubblicarla così.

## Senza key
Su una pagina Claude condivisa l'assistente usa l'account Claude di chi la apre.
Ovunque altrove, senza key, risponde dalle domande frequenti.

## Dopo il deploy: anteprima del link su WhatsApp
WhatsApp mostra l'immagine solo con un indirizzo completo. In index.html cambia
`<meta property="og:image" content="og.png">` in
`<meta property="og:image" content="https://IL-TUO-SITO.netlify.app/og.png">`
e fai un nuovo deploy.

## Area CIAS (demo)
In fondo alla pagina, link «Area CIAS (demo)» nel piè di pagina.
Il lunedì si segnano le quantità che avanzano: il raccolto della settimana si aggiorna subito.
«Scrivi il messaggio con Claude» prepara il testo per WhatsApp; senza AI mostra un esempio già pronto.
Le prenotazioni fatte nella demo compaiono nei ritiri di giovedì.
È una demo: quantità e prenotazioni ripartono da capo quando ricarichi la pagina.
