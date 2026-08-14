# ACE Setup Tool

[English](README.md) | **Italiano** | [Español](README.es.md)

ACE Setup Tool è un'applicazione desktop per Windows che consente di gestire,
confrontare e analizzare i setup delle vetture in **Assetto Corsa EVO**. Legge e
scrive file `.carsetup`, importa telemetria MoTeC e fornisce diagnostica sulle
prestazioni.

> Repository ufficiale di distribuzione binaria. Il codice sorgente non è distribuito.

## Download

Scarica installer, versione portable e checksum dalla pagina
[Releases](https://github.com/agastal/AceSetupTool-Release/releases).

- `AceSetupTool-<versione>-setup.exe` — installer consigliato;
- `AceSetupTool-<versione>-portable.zip` — versione senza installazione;
- `AceSetupTool-<versione>-setup-net.exe` — installer più leggero per chi ha già
  .NET 10;
- `AceSetupTool-<versione>-portable-net.zip` — la stessa versione senza installazione;
- `SHA256SUMS.txt` — impronte SHA-256 degli asset.

GitHub Releases è l'unico canale di distribuzione ufficiale. Non scaricare eseguibili
da mirror o collegamenti indicati da terzi.

## Funzionalità

- lettura, modifica e backup dei file `.carsetup`;
- confronto tra setup ed esportazione CSV;
- importazione e archivio locale della telemetria MoTeC;
- diagnostica su pressioni, temperature, sospensioni, camber e altezza;
- grafici e mappe del circuito;
- interfaccia in italiano, inglese e spagnolo;
- tema chiaro/scuro coordinato con Windows.

## Requisiti

- Windows 10/11 x64;
- Assetto Corsa EVO;
- nessun runtime separato: .NET e Windows App SDK sono inclusi.

L'installazione è per utente e non richiede privilegi di amministratore. La versione
portable deve essere estratta integralmente: non copiare soltanto l'eseguibile.

Gli asset `-net` sono lo stesso programma senza il runtime .NET incorporato: 158 MB
installati invece di 235, e richiedono
[.NET 10 (x64)](https://dotnet.microsoft.com/download/dotnet/10.0) sul computer. Il
Windows App SDK è incluso anche in quelli, quindi .NET è l'unico prerequisito;
l'installer `-net` lo verifica e si ferma con un messaggio invece di installare qualcosa
che non partirebbe. Nel dubbio, scegli la versione standard.

Per sapere se .NET 10 c'è, apri il terminale e digita `dotnet --list-runtimes`: se
compare una riga `Microsoft.NETCore.App 10.x` gli asset `-net` funzionano. Se non compare,
o se il comando non esiste, usa la versione standard. Windows non include .NET 10: quello
preinstallato è .NET Framework, che è un'altra piattaforma.

## Approvato da Red Kongs

<p align="left">
  &nbsp;&nbsp;<img src="media/red-kongs.png" alt="Red Kongs Racing Team" width="245" hspace="16" vspace="6"/>
</p>

ACE Setup Tool è uno strumento **approvato da Red Kongs**.

## Anteprima

### Setup e parametri degli pneumatici

<p align="center">
  <img src="media/01-setup-gomme.png" alt="Editor del setup e dei parametri degli pneumatici" width="70%"/>
</p>

Seleziona auto, circuito e setup, quindi modifica pressione, campanatura e convergenza
per ogni ruota in unità reali. La schermata riporta anche giro migliore, mediana e giri
utili e permette di salvare o ricaricare le modifiche e scambiare i dati in formato CSV.

### Confronto affiancato tra setup

<p align="center">
  <img src="media/04-confronto.png" alt="Confronto affiancato tra due setup" width="70%"/>
</p>

Scegli due configurazioni e confrontane i parametri in un'unica tabella, con unità,
valori e delta evidenziati. Il filtro limita la vista alle sole differenze, il riepilogo
indica parametri modificati e totali e il risultato può essere esportato in CSV.

### Riepilogo delle prestazioni per setup

<p align="center">
  <img src="media/06-risultati-segnalazioni.png" alt="Metriche delle prestazioni raggruppate per setup" width="70%"/>
</p>

Confronta per ogni setup giro migliore, mediana, numero di giri, pressione a caldo dei
quattro pneumatici e percentuale del giro trascorsa sui tamponi di fine corsa. La vista
riunisce in una tabella passo, costanza e indicatori essenziali di gomme e sospensioni.

### Tracce di acceleratore, freno e sterzo

<p align="center">
  <img src="media/07-risultati-grafici.png" alt="Tracce di acceleratore, freno e sterzo lungo il giro" width="70%"/>
</p>

Visualizza acceleratore e freno in percentuale e angolo di sterzo in gradi lungo la
distanza del giro. La selezione del giro e del riferimento di confronto aiuta a
individuare punti di frenata, applicazione del gas e correzioni di sterzo.

### Preparazione gara e calcolo della strategia

<p align="center">
  <img src="media/08-preparazione.png" alt="Calcolatore per preparazione gara e strategia" width="70%"/>
</p>

Inserisci durata di gara e qualifica, soste previste, tempo perso ai box, capacità del
serbatoio e margine carburante. Il calcolo usa auto e circuito selezionati per produrre
un riepilogo strategico basato sul setup scelto e sul suo tempo mediano.

## Dati e privacy

Impostazioni e archivio della telemetria sono conservati localmente:

| Dato | Percorso |
|---|---|
| Impostazioni | `%APPDATA%\AceSetupTool\` |
| Archivio telemetria | `%LOCALAPPDATA%\AceSetupTool\` |

ACE Setup Tool non implementa telemetria dell'utente né trasmissione remota di setup o
dati di guida. Le interazioni con GitHub per download, Issues o altre funzioni del sito
sono esterne all'applicazione e soggette alle condizioni di GitHub. Non pubblicare in
una Issue log, setup o telemetria contenenti informazioni che vuoi mantenere private.

## Licenza

ACE Setup Tool è **freeware proprietario**, distribuito soltanto in forma binaria. Può
essere usato gratuitamente alle condizioni della [licenza italiana](LICENSE.it.txt) e
della [EULA italiana](EULA.it.txt). Il testo inglese della [licenza](LICENSE.txt) e
della [EULA](EULA.en.txt) prevale nei limiti consentiti dalla legge applicabile.
È disponibile anche la traduzione [spagnola](LICENSE.es.txt) con la relativa
[EULA](EULA.es.txt).

Le licenze e attribuzioni dei componenti inclusi sono disponibili in
[THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt) e nella cartella
[`third-party`](third-party/). I testi delle licenze di terze parti restano nella
lingua originale.

## Supporto

Per segnalare un problema usa le [Issues](https://github.com/agastal/AceSetupTool-Release/issues),
indicando versione dell'applicazione, versione di Windows e passaggi per riprodurlo.

## Marchi e affiliazione

ACE Setup Tool è un progetto indipendente e non ufficiale. Non è affiliato, approvato
né supportato da Kunos Simulazioni o dall'editore di Assetto Corsa EVO. Nomi di
prodotti e marchi appartengono ai rispettivi proprietari.

Copyright © 2026 Adriano Gastaldello. Tutti i diritti riservati.
