# Listini Nuovi

Il modulo dei listini nuovi e' stato creato per rispondere alle esigenze di tutti quei casi particolari che non possono essere gestiti in modo tradizionale dai classici listini. Come vedremo la parola chiave e' flessibilita' dato che un listino puo' essere composto da vari controlli a discrezione dell'utente e puo' comprendere piu' clienti e vettori.


### Configurazione

Perche' il modulo possa essere messo in funzione e' necessario che nelle ConfermeRapide sia presente la voce ListiniNuovi in configurazione applicazione e che sia il modulo dei listini che quello delle conferme siano aggiornati dal server dato che non sono presenti nei moduli standard di TIR.
> \Click\ConfermeRapide
> \Click\Listini
> AggiornaDB, Script

La Stored Procedure dei listini viene caricata al primo avvio del modulo dei listini nuovi.
E' consigliabile fare una voce nel menu del cliente con lo script sottostante
> INSERT [dbo].[MenuPlus] ([Nome], [Gruppo], [Path], [Descrizione], [Visible], [Immagine], [Ordine], [Attivo], [Richiede_Att], [Cod_Lic], [Colore]) VALUES (N'Listini Nuovi', N'ANAGRAFICHE', N'\Click\Listini\Listini.App.exe', NULL, 1, NULL, 20, 1, 0, N'069', N'#2E7D32')

### Tabelle Coinvolte
Nel database TirSQL sono coinvolte tutte le tabelle sotto lo schema **lis.** . Per evitare spreco di dati queste tabelle non salvano righe uguali. Ad esempio se ho un importo di 10 euro presente in 50 righe di dettaglio, verra' salvato solo l'id di richiamo di quel prezzo e non 10 euro per ogni riga.
vediamole nel dettaglio
> **lis.Schemi**

E' alla base di tutto. E' il posto dove vengono salvate le possibili configurazioni dei listini. Questa tabella viene popolata dall'interfaccia utente sotto Altri Dettagli > schemi. Se ad esempio un listino ha fasce e calcoli verranno valorizzati i campi HasFasce e HasCalcoli a true
> **lis.Testate**

Si puo' vedere come il raggruppamento di piu' tipo di listino.

> **lis.Dettagli**

Rappresenta il posto dove vengono salvate le righe del listino. Questa tabelle tiene in memoria tutte le tabelle correlate. Ogni id della tabella corrisponde al suo corrispettivo nella tabella di riferimento.

> **lis.Fasce, lis.Tratte, lis.Prodotti, lis.Trasporti**

Sono tutte le tabelle che compongono la riga del listino, secondo le quali viene selezionata la riga e calcolato il prezzo

>**lis.POI, lis.CategorieMezzo, lis.UnitaDiMisura**

Sono tutte tabelle per la agganciare gli id delle tabelle secondarie
>**lis.Calcoli**

E' sempre una tabella secondaria ma tiene in memoria le regole di calcolo personalizzabili per ritornare il prezzo

>**dbo.ClienteListino**

Collega i clienti con la testata del listino e permette quindi la verifica dell'utilizzo dei listini nuovi o meno

>**dbo.ClienteListinoImporti**

Collega gli importi della riga del dettaglio con il cliente, questo perche' la riga di dettaglio puo'essere associato a piu' importi dentro la stessa testata

## Funzionamento del modulo
Come gia' detto, il segreto di questi listini e' la modularita' delle tabelle e dei dati.
Questa modularita' si ottiene definendo gli schemi nell'apposita sezione, nella quale possiamo definire le specifiche del listino. Si possono usare anche tutte le specifiche assieme.
La stored funziona leggendo tutti i possibili listini ed eliminando passo passo tutti i listini che non corrispondono a definizione.
### Inserimento dei dati
Per prima cosa devo definire la testata dei listini. La **testata rappresenta** un'insieme di tipologie di listini legate da proprieta' comuni da usare con piu' clienti.
Ad Esempio un listino navale o un listino spedizioni hanno sempre e' molto probabile che abbiano sempre le stesse tratte e gli stessi prodotti. In quel caso si crea una sola testata e poi si abbinano ai vari clienti.
Una volta creata la testata si creano appunto **le associazioni del cliente** dall'interno della testata.
A questo punto aggiungo una **nuova tipologia** di listino. Di default sono caricate le tipologie classiche di tir, ma sono sempre definite negli schemi.
Poi si procede all'inserimento vero e proprio del listino che puo' essere fatto o tramite importazione o manualmente.
Se si sta inserendo manualmente vengono i campi da inserire vengono visualizzati a seconda dello schema.
