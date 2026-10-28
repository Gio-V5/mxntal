# Changelog

**Italiano** · [English](CHANGELOG.en.md)

Scarica l'ultima versione: <https://github.com/Gio-V5/mxntal/releases/latest/download/MxntalTweaks.bat>

## 2.7 — 2026-10-27

- Voce **Sfondo del desktop Mxntal** in Windows e interfaccia: la M e la scritta sull'aurora, disegnate alla risoluzione dello schermo; lo sfondo di prima torna dal ripristino. AnyDesk fra le app installabili.

## 2.6 — 2026-10-27

- Scelta della lingua alla prima apertura, con le bandiere: italiano, inglese, francese, spagnolo. Si cambia dal pulsante in basso a destra. Tradotti finestra, catalogo e check-up; la console resta in italiano.

## 2.8 — 2026-10-28

- Pagina App: 106 programmi in 10 categorie (prima 33 in 7), ognuno con la sua icona ufficiale, e una casella per cercarli. In console le app si scelgono per categoria.
- "Installata" ora la decide Programmi installati di Windows (più i pacchetti MSIX), con winget come secondo controllo: Chrome, CrystalDiskInfo e Visual Studio Code non risultano più "da installare" quando ci sono.

## 2.5 — 2026-10-27

- Finestra **Novità** alla prima apertura dopo un aggiornamento: le righe del changelog delle versioni saltate e le voci nuove di Ottimizza (segnate "nuova"), con il pulsante per vederle. Vale anche se sostituisci il file a mano.
- Il motore usa `findstr` al posto di `find`: con Git Bash o MSYS nel PATH la selftest e i controlli di servizi, OneDrive ed Esplora risorse non sbagliano più.

## 2.4 — 2026-10-27

- Sei voci nuove: app del produttore per i dispositivi, Termina attività dalla barra, Edge senza popup e senza MSN, WPBT, percorsi lunghi

## 2.3 — 2026-10-26

- Controllo degli aggiornamenti a ogni avvio e, a finestra aperta, ogni ora: prima una volta al giorno.
- L'avviso di una versione nuova compare una volta sola; in basso resta "Aggiornamento X.Y" con il pulsante Aggiorna.

## 2.2 — 2026-10-26

- Pulsante **Controlla aggiornamenti** in basso a destra: dice se sei aggiornato, cosa è andato storto, oppure apre le novità con **Aggiorna**.
- Barra in basso su due colonne: con poco spazio niente più testi sotto i pulsanti.

## 2.1 — 2026-10-26

- **Widgets OFF** bloccato da Windows (driver UCPD): Mxntal lo spiega e porta all'alternativa che Windows accetta, invece di un errore secco.
- Gli errori di scrittura riportano il motivo dato da reg.exe; dopo un errore niente backup fantasma e niente proposta di riavvio.
- Barre di avanzamento a pillola; nomi e barre allineati in Panoramica e Ottimizza.

## 2.0 — 2026-10-26

- Nuovo nome **Mxntal** e interfaccia grafica nello stesso unico file: Panoramica con check-up, Ottimizza, Profili, App, Pulizia, Macchina del tempo, Miti sfatati. I menu in console restano (`/console`).
- Aggiornamenti firmati: la finestra controlla l'ultima release su GitHub e installa con un clic, solo se la firma è valida.
- PC in dominio: le voci delicate spiegano il motivo e chiedono conferma; profili e "applica tutte" le saltano.
- File, cartella dei backup, log e variabili restano quelli di Mxntal.tweaks: i backup vecchi funzionano.

## 1.8 — 2026-10-20

- Backup a prova di caratteri speciali (`! % ^ "` e barra finale), che prima potevano corrompere il valore salvato.
- Ogni scrittura viene riletta e confrontata con il valore voluto; se non coincide la voce risulta in errore.
- Nuovi `/doctor` e `/verify`, log in `%LOCALAPPDATA%\MxntalTweaks`, controllo di integrità ed export `.reg` dei backup.
- Oltre 30 bug corretti in menu, anteprima e blocchi PowerShell; selftest, lint e driver dei menu ampliati.
