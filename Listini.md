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
Nel database TirSQL sono coinvolte tutte le tabelle sotto lo schema **lis.**
vediamole nel dettaglio

> **lis.Schemi**

E' alla base di tutto. E' il posto dove vengono salvate le possibili configurazioni dei listini. Questa tabella viene popolata dall'interfaccia utente sotto Altri Dettagli > schemi. Se ad esempio un listino ha fasce e calcoli verranno valorizzati i campi HasFasce e HasCalcoli a true
> **lis.Testate**

Si puo' vedere come il raggruppamento di piu' tipo di listino.

> **lis.Dettagli**

rappresenta il posto dove vengono salvate le righe del listino. Questa tabelle tiene in memoria tutte le tabelle correlate. Ad esempio se ho una riga con 


## Funzionamento del modulo

