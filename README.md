# AnkerOrderManager
Un file excel per la gestione delle forniture Anker e la vendita ai clienti Coppo.


PROPOSTE DARIO
- Arrotondare i prezzi delle bottiglie (con prezzo superiore ai 10€):
  - da 0,96 a 0,50 -----> 0,5
  - da 0,51 a 0,95 -----> 0,95
Aumento medio del prezzo delle bottiglie di 25 centesimi (1,1% di media in più).
Su 1.000 bottiglie sono 250€ in più.
Su 10.000 bottiglie sono 2.500€ in più 

V4.0
- implementazione di email automatiche per la gestione del rapporto con i clienti

V3.6
DONE
- Aggiunta la possibilità di modificare e salvare un ordine anche in modalità "CONCLUSO"
TO DO
- aggiungere la gestione del post ordine
- la gestione delle disponibilità delle bottigli ordinate

V3.5
DONE:
- in ORDER FORM sostituire la colonna TOTAL con:
  - TOTAL COSTO ANKER
  - TOTAL COSTO IMPORT
  - TOTAL PREZZO VENDITA
- Eliminati altri bug minori:
  - Arrotondamento scorretto nel calcolo del prezzo nelle proforme e nell'ORDER FORM. Ora si segue il metodo di calcolo utilizzato nello sheet LISTONE
  - Prima del salvataggio rimozione di filtri e righe nascoste in ORDER FORM
  - Proforma automatica sempre in fase di test ma corretti ancora alcuni piccoli dettagli
- Aggiunti 3 sheet per l'analisi dati:
  - ANALISI FORNITURA
    - Utile per avere alcune insights sulla fornitura nel suo complesso. Dovrebbe dare un stima ESATTA del totale della proforma Anker
  - ANALISI ORDINI
    - Per vedere a colpo d'occhio la situazione degli ordini.
  - ANALISI PRODOTTI
    - Da vedere se utili. L'idea è capire quali sono i prodotti più richiesti e di quale categoria appartengono
  - DAA CALCULATOR (è solo un'idea)
    - Per creare in automatico il DAA in entrata in uscita?
IN TEST
- Aggiunto il blocco dello sheet ORDER FORM per evitare che un utente lo modifichi e lo rompa.
- Sono state quindi sbloccate tutte le celle di cui l'utente ha bisogno per effettuare il data entry.
- DA VERIFICARE CHE TUTTE LE MACRO E IL CODICE VBA NON SI SCONTRI CON IL BLOCCO. IN QUEL CASO O SI SBLOCCANO LE CELLE CHE INTERAGISCONO CON IL CODICE VBA O AGGIUNGERE NEL CODICE VBA LO SBLOCCO DEL FOGLIO E IL RIBLOCCO.

  
V3.4
- eliminate le schede dei clienti.
- eliminate il modulo negozi
- ora tutti gli ordini si gestiscono dal modulo cliente che verra rinominato "ORDER FORM" da cui sarà possibilie salvare, caricare, modificare ordini sia di clienti che dei negozi.
- Creato un "dbOrdini" ossia un grande dataset dove vengono registrati tutti gli ordini.
  - Ogni record del dataset rappresenta una referenza ordinata da uno dei nostri clienti o dai negozi Coppo.
  - Ogni record ha specifici campi per l'identificazione e l'associazione al corretto cliente e alla corretta fornitura
  - Alle forniture è stato associato un dodice riconoscitivo del tipo MMMYY
  - Il dataset che si verrà così a formare sarà utile per fare delle analisi su: PRODOTTI, CLIENTI, INCROCIO PREZZI FORNITORI ESTERI E NAZIONALI
- aggiunto un "trova lo sku vinolux" per facilitare l'abbinamento dello sku vinolux e quindi il prezzo del concorrente
- Aggiunti tutta una serie di piccole features per rendere l'esperienza utente più fluida:
  - select distinct dei clienti sulla base della fornitura selezionata
  - pulsanti: REIMPOSTA FORMULE, CLIENTI, SHOW STORICO
- Implementata la generazione di proforma (ancora in test)
- Creato un pulsante per generare un backup del dbOrdini

V3.3 BUG FIXES 
- Aggiunto il filtro per i prodotti non available in powerquery.
- Corretti il "modulo cliente" e il "modulo negozi" per tenere conto dei prezzi di acquisto piuttosto che dei prezzi di vendita.
- Corretti il "modulo cliente" e il "modulo negozi" in modo tale che gli ordini vengano inseriti con il conteggio delle bottiglie e non dei cartoni.


OBIETTIVI PIENAMENTE RAGGIUNTI ALLA 3.2
- Creazione in maniera rapida dei listini necessari per richiedere gli ordini ai clienti e ai nostri negozi.
- Registrazione degli ordini ricevuti dai clienti

OBIETTIVI ANCORA DA RAGGIUNGERE
- Test prolungato dell'applicazione
- Aggiunta di un sistema per la gestione delle disponibilità e adeguamento degli ordini a queste
- Creazione di relazione tra anker sku e geko sku
- Invio mail automatiche
- Completamento della black list (cecilia's list) con più referenze possibili da eliminare
- Capire se i liquori misti sono da includere o meno nel listino da proporre alle enoteche/grossisti (ai negozi vanno sicuramente proposti)
- Nel modulo cliente aggiungere una colonna con il prezzo di costo. In maniera tale che quando si calcola l'ordine aggregato si sa già quanto si andrà a spendere.


Update 3.2

Fixed Bugs
- Eliminare ogni doppione presente nel listone! I doppioni rendono il cerca verticale con il nome della referenza inefficace!
- Gestire il bug che porta a non selezionare correttamente il range da copiare quando si importa un ordine cliente su una nuova fornitura 

Features Deployed
- Creare un nuovo pulsante nel pannello di controllo "Nuovo Ordine Negozi". Essendo l'ordine dei negozi più grande e non necessitando di proforma deve avere un layout diverso.
- Eliminare il merge delle celle titolo di categoria nel listone magazzino

Other
- Fatta pulizia tra i named ranges (sarà da verificare se ne verranno ricreati altri)
- piccole ottimizzazione negli scripts

  
STILL TO BE FIXED AND IMPROVED:
  - Sheet con gli indirizzi fisici dei clienti
  - Nuovo modello proforma
  - Routine per la creazione in automatico della proforma
  - Chi fa l'ordine (Davide e Lorenzo) possano vedere le quantità in stock del prodotto in questione (DIFFICILE DA IMPLEMENTARE SERVIREBBE UN DATASET CON GLI INCROCI TRA GLI SKU COPPO E QUELLI ANKER)
  - Pulsante salva e chiudi una fornitura. Permette il salvataggio delle forniture per avere dati storici sugli acquisti, prezzi ecc ecc. Inoltre permetterebbe di creare il link tra SKU Coppo e Sku Anker.
  - Eliminare i named range che non hanno scope workbook che vengono creati ogni qual volta si duplica un sheet.
