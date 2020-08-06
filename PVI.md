# Pianificatore Intermodale

### Distribuzione

La modalita' distribuzione permette di gestire gli ordini in modo piu'efficente per le consegne di una sede per utente

Si accede aprendo un poi e cliccando l'iconcina distribuzione (quella con il pacco aperto). A questo punto la schermata si dividera' in 4 riquadri spiegati sotto.
Le movimentazioni possono essere effettuate solo dagli ordini da gestire e da quelli arrivati, per quanto riguarda i ritiri in corso e gli ordini in partenza si cambia solo l'esito.

### Ordini Da Gestire
Sono tutti gli ordini che l'operatore deve gestire per quel magazzino. Viene fatto un controllo per gli ordini da visualizzare che lega il poi (tabella PVI_POI) con le province che gestisce quel punto (Tabella [ord].[ZonePunti])

### Ritiri In Corso
Qui vengono visualizzate le conferme che sono state movimentate da quel magazzino. Nello specifico quelle che nella tabella [ord].[PercorsoOrdini] hanno IdEsito del percorso di carico maggiore di zero.

### Arrivati
Sono gli ordini che invece hanno [ord].[PercorsoOrdini] con IdEsito di scarico maggiore di zero.

### In Partenza
Visualizza gli ordini che stanno partendo da quel magazzino
