# AnkerOrderManager
Un file excel per la gestione delle forniture Anker e la vendita ai clienti Coppo.


PROPOSTE DARIO
- Arrotondare i prezzi delle bottiglie (con prezzo superiore ai 10€):
  - da 0,96 a 0,50 -----> 0,5
  - da 0,51 a 0,95 -----> 0,95
Aumento medio del prezzo delle bottiglie di 25 centesimi (1,1% di media in più).
Su 1.000 bottiglie sono 250€ in più.
Su 10.000 bottiglie sono 2.500€ in più 


OBIETTIVI PIENAMENTE RAGGIUNTI ALLA 3.2
- Creazione in maniera rapida dei listini necessari per richiedere gli ordini ai clienti e ai nostri negozi.
- Registrazione degli ordini ricevuti dai clienti

OBIETTIVI ANCORA DA RAGGIUNGERE
- Test prolungato dell'applicazione
- Aggiunta di un sistema per la gestione delle disponibilità e adeguamento degli ordini a queste



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
