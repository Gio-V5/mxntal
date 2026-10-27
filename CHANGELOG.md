# Changelog

**Italiano** · [English](CHANGELOG.en.md)

Scarica l'ultima versione: <https://github.com/Gio-V5/mxntal/releases/latest/download/MxntalTweaks.bat>

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
