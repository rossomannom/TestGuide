# App E-TIR		

# Introduzione

Lo scopo della app E-TIR è quello di poter creare un collegamento tra l’azienda e l’autista, dando la possibilità di inviare viaggi direttamente sulla app che verranno poi chiusi dall’autista.  
In questo modo è possibile tener traccia dell’attività dell’autista senza nessun contatto diretto, ricevendo degli esiti in tempo reale. 
Una volta che un viaggio è chiuso attraverso la app, gli esiti vengono direttamente passati sul software TIR Horizon. 
È consigliabile effettuare dei test di funzionamento, ricezione e chiusura viaggi prima di passare all’utilizzo della app in produzione. Per fare ciò, è possibile utilizzare la versione della app per Windows. 
La seguente guida è composta da una prima parte puramente tecnica ed una seconda parte nella quale viene descritto il funzionamento della app. Pertanto, se vi occorre esclusivamente conoscere il funzionamento della App, potete saltare il paragrafo “Operazioni tecniche preliminari”. 
N.B.: l’app funziona ESCLUSIVAMENTE su Smartphone Android (che abbiano preinstallato il Play Store) che sono connessi alla rete. Non è possibile installare la app su iPhone o su altri sistemi operativi. 


N.B.: E’ presente un’appendice che permette l’integrazione dell’app con il PTV Navigator, la quale carica le mappe e permette la stessa navigazione che è stata programmata nel PVI. 



# Operazioni tecniche preliminari

Affinché l’applicazione funzioni correttamente è necessario svolgere delle operazioni preliminari che permettano la corretta attivazione delle funzionalità.

1)	Download APP
a.	Occorre scaricare la app su uno smartphone Android che abbia almeno la versione 6.0. L’applicazione è presente sul Play Store e vengono costantemente rilasciati aggiornamenti; pertanto, è necessario assicurarsi di avere sempre l’ultima versione disponibile. 

2)	Impostare Endpoint
Una volta scaricata la app, occorre impostare l’endpoint che permette la sincronizzazione con il database:

![etir accesso](https://user-images.githubusercontent.com/105659714/168635470-1038c686-9bca-4dda-aca8-e45fa31e205b.PNG)
 	 
I link di connessione vengono rilasciati direttamente dalla software house una volta stipulato il contratto. Il cliente deve custodire i parametri di connessione oppure salvare il QR-code. Ogni terminale o smartphone deve essere configurato singolarmente. 

3)	Impostare email autista 	
Nel modulo “Autisti”, occorre impostare l’email che verrà poi utilizzata per accedere all’app. La password viene invece generata e comunicata direttamente dalla software house. 


![Immagine3](https://user-images.githubusercontent.com/105659714/168639679-bb0886ba-829c-4e88-8281-5318bb2b5573.png)

Ogni autista deve avere la sua mail (anche fittizia), perché l’accesso alla app è univoco e ogni autista vedrà esclusivamente i viaggi di sua competenza.


4.1)	 Invio viaggio alla app da Viaggi
Dopo aver creato un viaggio, è necessario che questo venga inviato manualmente alla app. Per fare ciò occorre, dal modulo Viaggi, selezionare il viaggio da inviare all’autista e premere su “Ordina Viaggio”. 

![Immagine4](https://user-images.githubusercontent.com/105659714/168746472-e5daac72-ab86-40f2-8abb-e69f53bc1961.png)

A questo punto l’utente può ordinare i carichi e gli scarichi che l’autista deve effettuare. Se ad esempio il viaggio è un carico da punto A e scarico verso punto B, è possibile premere sulla funzione “carichi prima”, poi su “raggruppa punti”. 


4.2)	 Invio viaggi da PVTS2

5.	Dopo aver creato una serie di viaggi, è possibile inviarli in modo massivo attraverso il PVTS2. Per fare ciò occorre, dal modulo PVTS2, premere su File e selezionare “Invia Tutto App”.  

![Immagine5](https://user-images.githubusercontent.com/105659714/168746971-7fdded07-3c38-4340-83ed-81dd23e927ec.png)

Se invece si vuole inviarli singolarmente, è possibile cliccare con il tasto destro sul viaggio e selezionare l’opzione “gestisci ordini”.  Da questo menu è possibile ordinare gli ordini ed inviare all’app.



![Immagine6](https://user-images.githubusercontent.com/105659714/168748275-2848f160-aa8c-467f-bf46-5811a6b89c8e.png)

<h1 id="utilizzo-della-app-e-tir">Utilizzo della APP E-TIR</h1>

1)	Una volta aperta la app, occorre effettuare il login con le credenziali che sono state fornite dalla software house. 

![Immagine7](https://user-images.githubusercontent.com/105659714/168749985-faf4da3f-595d-4f4c-8a90-f77b5e238bae.jpg)


2)	Fatto il login, il menu principale si presenta come sotto. Occorre dunque scegliere la funzione che si vuole utilizzare.


![Immagine14](https://user-images.githubusercontent.com/105659714/168749849-1448b035-2a7b-47f5-8b6a-e0f4d37d9900.jpg)

•	**Modalità Viaggi**

La modalità viaggi è la base dell’app. Da qui è possibile per l’autista visualizzare l’elenco dei viaggi che gli sono stati assegnati. 

![Immagine9](https://user-images.githubusercontent.com/105659714/168750621-dd7634e7-97d2-4e1e-b56d-2ddbbd99e302.jpg)

Se la targa reale è differente da quella assegnata dall’operatore, è possibile per l’autista fare tap sul simbolo del QR-Code e scansionare il QR-Code che identifica la targa reale.

**N.B.: La targa inserita nel QR-Code deve essere inserita nel formato che comincia con T prima della targa. Ad esempio: TGJ999TT.**

Per poter aprire un viaggio, l’autista deve fare tap sulla riga desiderata. Così facendo appariranno i carichi e gli scarichi assegnati all’interno del viaggio. 

![Immagine10](https://user-images.githubusercontent.com/105659714/168751072-182e38cb-462b-4350-bb48-a191676bb7eb.png)

Facendo tap sul primo punto (in questo caso il carico), vengono mostrati i dettagli di quello che l’autista dovrà fare. 

![Immagine11](https://user-images.githubusercontent.com/105659714/168751329-de0d01f7-a433-4ac4-8d27-4c463b8d58e5.png)
 

Con i tasti in alto è possibile:

-	Chiamare il cliente;

-	Chiamare il punto indicato per effettuare un preavviso;

-	Navigare verso il punto indicato. 


Con i tasti in fondo è possibile invece inviare degli esiti/foto che verranno salvati nella conferma. 

**Il corretto funzionamento dell'app prevede che l'autista prema su "Partito" una volta che comincia il viaggio verso il punto indicato; quando il viaggio verso il punto termina, preme su "Arrivato".**

Nel caso invece in cui ci sia un problema durante il viaggio, può premere il tasto “problema” e scrivere una breve descrizione. Se invece il viaggio viene sospeso, l’autista può premere il tasto “sospendi”. 

**N.B.: Per tutti i mezzi che hanno un collegamento con il sistema satellitare, quest'ultima operazione è fondamentale per poter attribuire il corretto numero di km e valutare il tempo effettivo che ci ha messo il mezzo per fare una tratta.**

Una volta terminato il viaggio, l’autista può aggiungere una foto (scansione della bolla o foto della merce ad esempio). 
Per chiudere definitivamente il viaggio, occorre premere il tasto “Salva”.  

Nel caso in esempio, l’autista dovrà (come operazioni essenziali) nell’ordine:

1)	Selezionare il punto di carico;

2)	Premere il tasto partito (ad inizio viaggio);

3)	Premere il tasto arrivato (una volta arrivato sul punto di carico);

4)	Selezionare il punto di scarico;

5)	Premere tasto partito (quando ha caricato ed è ripartito);

6)	Premere il tasto arrivato;

7)	Premere il tasto “Salva” per chiudere il viaggio.

***Ricezione dati da importer app***

A questo punto occorre ricevere i dati attraverso l’applicativo “Importer App”. 
Fare doppio click sull’eseguibile e premere il tasto sincronizza in alto. Infine premere “Ricevi Tutto” in basso, per effettuare una sincronizzazione completa.

![gestioneapp](https://user-images.githubusercontent.com/105659714/168753617-f0d4bd9f-5f77-4947-b9bf-7116e4bbe95a.png)

**N.B.: Fin quando i dati non vengono scaricati da "ImporterApp", nessun esito viene passato.**

***Ricezione dati da PVTS2***

È anche possibile scaricare i dati attraverso il Pvts2.
 
Occorre cliccare su “File” e poi premere su Ricevi da App. Selezionare il periodo di riferimento e poi cliccare su “Ricevi/Esporta”. 

![Immagine13](https://user-images.githubusercontent.com/105659714/168763548-69ab85c5-1bc9-4343-815e-40c956bb00c9.png)
 

**•	Modalità Rifornimenti**

La modalità rifornimenti permette all’autista di caricare un rifornimento effettuato, passando l’informazione in tempo reale all’azienda. 

Dal menu principale, occorre selezionare la modalità “Rifornimenti”. 

![Immagine14](https://user-images.githubusercontent.com/105659714/168749849-1448b035-2a7b-47f5-8b6a-e0f4d37d9900.jpg)

Nel menu rifornimenti, occorre inserire le informazioni circa il rifornimento che è stato effettuato. Una volta terminato, fare tap su “Conferma”. In alto a destra, è possibile aprire un menu a tendina che riporta l’elenco di tutti i rifornimenti che sono stati salvati e non ancora scaricati. Facendo tap sul rifornimento, è possibile modificare le informazioni immesse. 

![Immagine15](https://user-images.githubusercontent.com/105659714/168765964-ebf668c3-e0b8-4f36-a53a-06681580182d.jpg)


L’azienda deve poi scaricare questi dati attraverso l’applicativo “Importer App”.  
 
Portarsi sul simbolo del rifornimento in alto a sinistra e premere su Importa. È possibile per l’operatore modificale eventuali dati errati. Terminata questa operazione, cliccare su “Registra rifornimenti” per importare i dati in TIR Horizon. 

![Immagine16](https://user-images.githubusercontent.com/105659714/168766500-905fe111-1d23-4b3b-bbe1-c0fb5ecc46e4.png)

 
**•	Modalità Inserimento Ordini**

La modalità inserimento ordini permette ad un autista o ad un operatore di inserire gli ordini direttamente attraverso la app. 
 
Dal menu principale, occorre selezionare la modalità “Inserimento Ordini”. 
 	 
![Immagine14](https://user-images.githubusercontent.com/105659714/168749849-1448b035-2a7b-47f5-8b6a-e0f4d37d9900.jpg)

Nel menu Nuovo Ordine occorre inserire le informazioni circa l’ordine che si desidera inserire. Una volta terminato, fare tap su “Conferma”. In alto a destra, è possibile aprire un menu a tendina che riporta l’elenco di tutti gli ordini che sono stati salvati e non ancora scaricati. Facendo tap sull’ordine, è possibile modificare le informazioni immesse. 


L’azienda deve poi scaricare questi dati attraverso l’applicativo “Importer App”.  

![ordini importer](https://user-images.githubusercontent.com/105659714/168810887-676c9305-e9fa-407e-b5ed-45aaf6f95156.png)


Portarsi sul simbolo degli ordini in alto a sinistra e premere su Importa. È possibile per l’operatore modificale eventuali dati errati. Terminata questa operazione, cliccare su “Registra ordini” per importare i dati su TIR Horizon. 


 
# Appendice

**Integrazione con PTV Navigator**



PTV Navigator permette di utilizzare il sistema di navigazione PTV anche sulla app. In questo modo è possibile mantenere lo stesso percorso che è stato impostato sul viaggio senza che venga ricalcolato da Maps. 

Per poter utilizzare il servizio, è necessario scaricare sullo smartphone di ogni autista la app PTV Navigator. 
Dopo aver fatto il login, la app è pienamente utilizzabile e può essere integrata con E-TIR. 

![ptv](https://user-images.githubusercontent.com/105659714/168811338-4b39fb82-7a75-4002-918e-e56a19ff9360.png)

 
Una volta fatto tap su “Naviga”, l’applicazione vi chiederà con quale strumento aprire la navigazione. 

Scegliere “PTV Navigator” (facendo attenzione a fare tap su “ricorda la mia scelta”, in modo da non doverlo selezionare nuovamente). 

A questo punto si aprirà la app PTV Navigator e partirà la navigazione verso il punto desiderato. 





