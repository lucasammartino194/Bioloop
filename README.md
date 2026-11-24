BioLoop

AVVIO CONSIGLIATO (Windows)
1. Estrai tutto il contenuto dello ZIP in una cartella.
2. Installa Node.js LTS se non è già presente sul computer.
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
- Le funzionalità cliniche e i risultati IA restano dimostrativi: BioLoop non è un dispositivo medico e non fornisce diagnosi reali.
- Non cancellare né spostare la cartella “Cartelle pazienti” se si desidera mantenere i PDF salvati sul disco.
