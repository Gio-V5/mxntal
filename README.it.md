<p align="center"><img src="docs/brand/mxntal-logo-128.png" width="96" height="96" alt="Mxntal"></p>
<h1 align="center">Mxntal</h1>
<p align="center"><strong>Lavora nell'ombra. Tu giochi.</strong></p>
<p align="center">
  <a href="https://github.com/Gio-V5/mxntal/releases/latest"><img src="https://img.shields.io/github/v/release/Gio-V5/mxntal?label=versione&color=8A4FD8" alt="Ultima versione"></a>
  <a href="https://github.com/Gio-V5/mxntal/releases"><img src="https://img.shields.io/github/downloads/Gio-V5/mxntal/total?label=download&color=8A4FD8" alt="Download"></a>
</p>
<p align="center"><a href="README.md">English</a> · <strong>Italiano</strong> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a></p>

Mxntal ottimizza Windows 10 e 11 senza scatole nere: ogni modifica ha un motivo scritto, un backup del
valore di prima e un ripristino con un clic. È un solo file, `MxntalTweaks.bat`, con un'interfaccia
grafica e, per chi li preferisce, i menu classici in console. Niente da installare.

![La pagina Ottimizza di Mxntal](docs/screenshot-ottimizza.png)

## Scarica e avvia

1. Scarica l'ultima versione: **[MxntalTweaks.bat](https://github.com/Gio-V5/mxntal/releases/latest/download/MxntalTweaks.bat)**
   (circa 640 KB).
2. Doppio clic: Windows chiede i permessi di amministratore e si apre la finestra. Se rifiuti, Mxntal si
   chiude senza cambiare nulla.
3. Al primo avvio Windows può avvisare che l'editore è sconosciuto: succede con ogni file `.bat` scaricato
   da internet.

Requisiti: Windows 10 o 11 con un account amministratore; Windows PowerShell 5.1 (già in Windows); per la
pagina App, winget ("Programma di installazione app" dal Microsoft Store).

## Cosa fa

- **Panoramica**: un check-up con punteggio e le cose da sistemare, ognuna con il pulsante per farlo; CPU,
  memoria, scheda video e disco in tempo reale; la scheda del PC.
- **Ottimizza**: 30 voci in 7 categorie (Energia e CPU; Gaming e input; Windows e interfaccia; Avvio, RAM
  e background; Disco e servizi; Internet e rete; Avanzate). Ogni voce spiega cosa cambia, quelle rischiose
  chiedono conferma; "Applica le sicure" e "Ripristina categoria" per fare tutto in un colpo.
- **Profili** rapidi: Gaming e Lavoro.
- **App**: 32 programmi comuni installati con winget, dai pacchetti ufficiali dei produttori.
- **Pulizia**: file inutili (temporanei, dump, log e, se lo scegli, il Cestino), misurati prima di
  toglierli; app preinstallate (43 nell'elenco), tolte per l'utente corrente e rimettibili con un clic;
  programmi che partono con Windows.
- **Backup**, la macchina del tempo: ogni valore salvato con il suo ripristino, i punti di ripristino di
  Windows, il riavvio programmato.
- **Miti sfatati**: i tweak famosi che Mxntal non applica, e perché.

## Cosa non tocca mai

- Microsoft Store, Windows Update, Delivery Optimization, servizi Xbox, Xbox Game Bar e registrazione
  Game DVR.
- Niente tweak placebo: Win32PrioritySeparation, NetworkThrottlingIndex, HPET e simili restano fuori; la
  pagina Miti sfatati spiega perché.
- Le impostazioni che Windows protegge con il driver UCPD (per esempio i Widgets su alcuni PC): Mxntal non
  lo aggira, spiega il blocco e porta all'alternativa che Windows accetta.
- Su un PC in dominio aziendale il DNS resta quello dell'azienda, e le voci delicate (indicizzazione,
  protezioni di sicurezza, esclusioni Defender, TCP) spiegano il motivo e chiedono conferma.

## Backup e ripristino

- Prima di ogni modifica il valore originale va in `%LOCALAPPDATA%\MxntalTweaks\Backup\originali`, un file
  per valore, e resta quello di prima di Mxntal anche se applichi una voce più volte.
- Ogni scrittura viene riletta: se il valore non è quello voluto, Mxntal lo dice e la voce risulta in
  errore.
- Ripristino dalla finestra: Backup, un valore alla volta o tutto insieme; Ottimizza, spegni
  l'interruttore o Ripristina categoria; Pulizia, Rimetti le app tolte. In console: menu 9.
- Il log in `%LOCALAPPDATA%\MxntalTweaks\MxntalTweaks.log` registra data, azione, valore prima e dopo ed
  esito.
- Senza ritorno solo la pulizia dei file: per questo Mxntal misura prima e chiede conferma.

## Aggiornamenti

La finestra controlla a ogni avvio, e ogni ora finché resta aperta, se c'è una versione nuova (una
richiesta HTTPS da 1 KB, nessun dato inviato) e la installa con un clic, solo se è firmata. Il pulsante
**Controlla aggiornamenti** cerca subito; "Non controllare più gli aggiornamenti" spegne il controllo
automatico. Le novità di ogni versione sono nel [changelog](CHANGELOG.md).

## Console classica

| Comando | Cosa fa |
|---|---|
| `MxntalTweaks.bat /console` | i menu classici in console, con i permessi di amministratore |
| `MxntalTweaks.bat /dryrun` | anteprima: mostra cosa cambierebbe, non tocca nulla e non chiede i permessi |
| `MxntalTweaks.bat /doctor` | diagnostica dell'ambiente: admin, Windows, PowerShell, strumenti, spazio, backup |
| `MxntalTweaks.bat /verify` | stato di ogni voce e controllo dei backup, in sola lettura |
| `MxntalTweaks.bat /?` | elenco delle modalità |

Dalla finestra, il pulsante "Console classica" in basso a destra apre gli stessi menu. Se l'interfaccia
grafica non può partire (per esempio PowerShell in modalità limitata su un PC aziendale), si aprono i menu
in console.

## Problemi e idee

Apri una [issue](https://github.com/Gio-V5/mxntal/issues) con la versione di Mxntal e, se serve, le
righe del log che riguardano il problema.
