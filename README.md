# Catalogo vini di Romagna — pagina protetta

**➡️ https://lanadelrekt.github.io/catalogo-vini-romagna/**

Schede vino, vitigni, temperature di servizio e abbinamenti gastronomici
dei produttori della Romagna. **Serve una password** per aprirla: se non
ce l'hai, questa pagina non ti serve a niente.

## Cos'e' questo repository

Contiene **un solo file**, `index.html`: una pagina statica il cui
contenuto e' cifrato con AES-256-GCM (chiave derivata dalla password con
PBKDF2-HMAC-SHA256, 600.000 iterazioni). Senza la password il file e'
soltanto testo cifrato: si apre, ma non mostra nulla. La decifratura
avviene nel browser, con WebCrypto — nessun server vede la password.

Lo sblocco richiede qualche secondo: e' il costo della derivazione della
chiave, ed e' voluto. E' cio' che rende impraticabile provare password a
tappeto su una copia scaricata del file.

I dati di partenza, gli script che generano il catalogo e la password
**non stanno qui**: vivono in un repository privato separato, da cui
questa pagina viene rigenerata e ripubblicata.

## Aggiornare la pagina

Non si modifica a mano. Si rilancia il workflow "Pagina web catalogo
(cifrata)" nel repository privato, che rigenera il catalogo, lo cifra e
committa qui il risultato. Il deploy di GitHub Pages richiede poi meno di
un minuto.
