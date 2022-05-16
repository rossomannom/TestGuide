# App E-TIR		

Introduzione
Lo scopo della app E-TIR è quello di poter creare un collegamento tra l’azienda e l’autista, dando la possibilità di inviare viaggi direttamente sulla app che verranno poi chiusi dall’autista.  
In questo modo è possibile tener traccia dell’attività dell’autista senza nessun contatto diretto, ricevendo degli esiti in tempo reale. 
Una volta che un viaggio è chiuso attraverso la app, gli esiti vengono direttamente passati sul software TIR Horizon. 
È consigliabile effettuare dei test di funzionamento, ricezione e chiusura viaggi prima di passare all’utilizzo della app in produzione. Per fare ciò, è possibile utilizzare la versione della app per Windows. 
La seguente guida è composta da una prima parte puramente tecnica ed una seconda parte nella quale viene descritto il funzionamento della app. Pertanto, se vi occorre esclusivamente conoscere il funzionamento della App, potete saltare il paragrafo “Operazioni tecniche preliminari”. 
N.B.: l’app funziona ESCLUSIVAMENTE su Smartphone Android (che abbiano preinstallato il Play Store) che sono connessi alla rete. Non è possibile installare la app su iPhone o su altri sistemi operativi. 

N.B.: E’ presente un’appendice che permette l’integrazione dell’app con il PTV Navigator, la quale carica le mappe e permette la stessa navigazione che è stata programmata nel PVI. 



Operazioni tecniche preliminari
Affinché l’applicazione funzioni correttamente è necessario svolgere delle operazioni preliminari che permettano la corretta attivazione delle funzionalità.
1)	Download APP
a.	Occorre scaricare la app su uno smartphone Android che abbia almeno la versione 6.0. L’applicazione è presente sul Play Store e vengono costantemente rilasciati aggiornamenti; pertanto, è necessario assicurarsi di avere sempre l’ultima versione disponibile. 
2)	Impostare Endpoint
Una volta scaricata la app, occorre impostare l’endpoint che permette la sincronizzazione con il database:

![etir accesso](https://user-images.githubusercontent.com/105659714/168635470-1038c686-9bca-4dda-aca8-e45fa31e205b.PNG)
 	 
I link di connessione vengono rilasciati direttamente dalla software house una volta stipulato il contratto. Il cliente deve custodire i parametri di connessione oppure salvare il QR-code. Ogni terminale o smartphone deve essere configurato singolarmente. 
3)	Impostare email autista 	
Nel modulo “Autisti”, occorre impostare l’email che verrà poi utilizzata per accedere all’app. La password viene invece generata e comunicata direttamente dalla software house. 

