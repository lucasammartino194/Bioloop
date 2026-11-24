BioLoop

AVVIO CONSIGLIATO (Windows)
1. Estrai tutto il contenuto dello ZIP in una cartella.
2. Installa Node.js LTS se non è già presente sul computer. (https://nodejs.org/en/download)
3. Fai doppio clic su “Avvia BioLoop.bat”.
4. Il browser aprirà automaticamente http://127.0.0.1:8765.
5. All'avvio scegli “Sì, consenti e continua” oppure “No, continua senza salvare sul disco”.

Video dimostrativo per la funzionalità del sito: 


ARCHIVIO FISICO AUTOMATICO
- La cartella “Cartelle pazienti” è già inclusa nel progetto e contiene la gerarchia dimostrativa: Regione / Ospedale / Codice paziente.
- L'utente non deve selezionare alcun percorso e non viene aperto alcun selettore di directory.
- Con il consenso, il server locale scrive esclusivamente dentro la cartella “Cartelle pazienti” contenuta nel progetto BioLoop.
- Le nuove schede paziente creano automaticamente la propria sottocartella nella regione e nell'ospedale selezionati.
- Se la persona esiste già, BioLoop riutilizza la scheda e non crea un duplicato.
- Quando si esporta il PDF, il file viene scritto direttamente nella cartella del relativo codice paziente. Il download browser può essere conservato come copia ulteriore solo se richiesto dalle impostazioni del browser; il salvataggio nella directory BioLoop avviene sul server locale.
- Il server ascolta solo su 127.0.0.1 e non espone la cartella a dispositivi della rete locale. Gli endpoint accettano soltanto i campi previsti e normalizzano i nomi delle directory.

MODALITÀ ALTERNATIVA
- Se l'utente rifiuta, oppure apre index.html direttamente senza avviare il server, BioLoop utilizza l'archivio interno persistente del browser (IndexedDB/localStorage).
- In questa modalità i PDF restano nella sezione “Cartelle pazienti” del sito e possono essere scaricati da lì.

OSPEDALI E PAZIENTI
- Le denominazioni ospedaliere sono state sostituite con nomi reali di strutture sanitarie italiane note, mantenendo le strutture pugliesi già presenti.
- I nominativi, i codici demo aggiunti e i dati anagrafici dei pazienti generati sono sintetici e non identificano persone reali.
- L'elenco integrato è una selezione dimostrativa, non un censimento esaustivo di tutte le strutture di ricovero italiane. La fonte istituzionale per l'elenco completo e aggiornato è il Ministero della Salute: https://www.salute.gov.it/new/it/banche-dati/elenco-aziende-sanitarie-locali-e-strutture-di-ricovero/ .

ALTRE NOTE
- Non cancellare né spostare la cartella “Cartelle pazienti” se si desidera mantenere i PDF salvati sul disco.

- ## Avvertenze, Limiti Operativi e Considerazioni Etiche

**Bioloop** è un prototipo dimostrativo sviluppato esclusivamente per scopi educativi e di ricerca. **Non è un dispositivo medico certificato** e non deve essere utilizzato in alcun caso per diagnosi cliniche, screening su pazienti reali o decisioni terapeutiche.

### Limiti Noti e Modalità di Errore
* **Dati Esclusivamente Sintetici:** Il sistema è stato testato solo su immagini simulate e phantom anatomici; le prestazioni su tessuti umani reali non sono state validate clinicamente.
* **Sensibilità alle Condizioni di Acquisizione:** Riflessi, scarsa illuminazione, sfocatura o variazioni nella posizione della scansione possono causare falsi positivi (segnalazione di masse inesistenti) o falsi negativi (mancato rilevamento di anomalie).
* **Incertezza nel Monitoraggio Temporale:** Il confronto tra scansioni successive si basa su allineamenti visivi semplificati e potrebbe interpretare variazioni posturali o prospettiche come cambiamenti morfologici della massa.
* **Potenziali Bias:** I modelli utilizzati possono mostrare cali di precisione in presenza di fototipi, corporature o condizioni non adeguatamente rappresentati nei dati dimostrativi.

### Principi di Utilizzo Sicuro
* **Supervisione Umana (Human-in-the-Loop):** Ogni risultato generato dal sistema ha valore puramente indicativo e richiede sempre l'interpretazione e la verifica di un professionista sanitario qualificato.
* **Tutela della Privacy:** Il prototipo elabora i dati in modo effimero senza salvare immagini o metadati identificativi su database permanenti.




PRIVACY E ACCESSO PER OSPEDALE (MODALITA' DIMOSTRATIVA)
BioLoop include una schermata di accesso con codici medico dimostrativi. Ogni codice medico ordinario limita la banca dati, le cartelle visibili e il salvataggio fisico a un solo ospedale. Il codice maestro demo consente la visualizzazione dell'intera rete esclusivamente per mostrare il concetto di supervisione multi-struttura.

I codici mostrati nell'interfaccia sono pubblici e condivisibili: NON sono credenziali di sicurezza e non devono essere utilizzati per proteggere dati sanitari reali. In un prodotto completo occorrerebbero account personali, autenticazione forte, autorizzazioni gestite lato server, cifratura, registri di audit, regole di conservazione e verifiche di conformita' al GDPR e alla normativa sanitaria. Eventuali accessi investigativi dovrebbero essere autorizzati da un titolo giuridico valido, limitati allo scopo e tracciati.

Tutti i nominativi e i dati presenti nel prototipo sono sintetici. Non inserire dati sanitari reali o informazioni personali identificabili. La schermata Privacy nel sito descrive il modello concettuale e non certifica la conformita' o la sicurezza di un sistema sanitario reale.
