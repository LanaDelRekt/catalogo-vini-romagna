# Catalogo vini di Romagna — pagina protetta

Questo repository contiene **un solo file**, `index.html`: una pagina statica
il cui contenuto e' cifrato con AES-256-GCM (chiave derivata dalla password
con PBKDF2-HMAC-SHA256, 600.000 iterazioni). Senza la password il file e'
soltanto testo cifrato: si apre, ma non mostra nulla.

La pagina viene pubblicata con GitHub Pages. I dati di partenza, gli script
che generano il catalogo e la password non stanno qui.
