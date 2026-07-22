# Carl Weische Summarizer

Cron GitHub Actions che ogni ora controlla il canale YouTube di [Carl Weische](https://www.youtube.com/@carlweische) (conversion rate optimization, landing page, direct response ed e-commerce), riassume i nuovi video via Claude Sonnet 4.5 e manda la sintesi strutturata via mail.

Replica dell'output di [omar-bragantini-summarizer](https://github.com/PierpaoloMaggio/omar-bragantini-summarizer) e [nate-herk-summarizer](https://github.com/PierpaoloMaggio/nate-herk-summarizer) — **stessa identica struttura email (5 sezioni)**, framing system adattato a contenuto CRO/e-commerce e prompt configurato per trascrizioni in inglese con output in italiano.

## Struttura del riassunto (5 sezioni)

1. **Argomento principale** — una frase
2. **Concetti chiave o novità introdotte** — 4-8 punti
3. **Step tecnici o framework operativi** — obiettivo + passaggi/leve + dettagli (oppure "Nessun framework pratico in questo video")
4. **Strumenti, tattiche e principi menzionati** — nome + spiegazione
5. **Vantaggi pratici** — 2-4 frasi sui benefici per chi ottimizza landing page, funnel o e-commerce

## Canale

- Handle: `@carlweische`
- Channel ID: `UCIgbiNZFqHZqIQ2Uoxxfu6w`

## Secrets

Stessi 4 degli altri summarizer: `APIFY_TOKEN`, `OPENROUTER_KEY`, `GMAIL_USER`, `GMAIL_APP_PASSWORD`.

## Primo avvio

1. Push del repo con i secrets configurati.
2. Actions → "Carl Weische Summarizer" → Run workflow.
3. Prima run = seed dei videoId correnti senza mandare mail. Dalla seconda processa i nuovi.

## Costo

~$0.05-0.10/video Sonnet 4.5. A regime ~$1-2/mese.
