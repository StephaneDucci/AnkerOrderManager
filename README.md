# AnkerOrderManager
Un file excel per la gestione delle forniture Anker e la vendita ai clienti Coppo.

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

  
Update 3.1:

- Passaggio da una formula matriciale a una tabella pivot per il calcolo dell'ordine aggregato
- I riferimenti in "Anker" sono stati aggiornati e riferiscono correttamente alla nuova tabella pivot
- Sono stati ridefiniti tutti i named range e ora sono pochi e più chiari
- E' stato aggiunto lo sku anker al modulo cliente
- E' stato rimosso il tasto in controllo active x con una classica shape

  Bugs da gestire:
  FATTO - URGENTE: Eliminare ogni doppione presente nel listone! I doppioni rendono il cerca verticale con il nome della referenza inefficace!
      - Idea: per i formati "strani" (quelli diversi da 0,7 e 1 lt) se c'è un doppione aggiungere il size nella descrizione del prodotto
  FATTO - Gestire il bug che porta a non selezionare correttamente il range da copiare quando si importa un ordine cliente su una nuova fornitura 

  Features da aggiungere:
  - Sheet con gli indirizzi fisici dei clienti
  - Routine per la creazione in automatico della proforma
  FATTO - Creare un nuovo pulsante nel pannello di controllo "Nuovo Ordine Negozi". Essendo l'ordine dei negozi più grande e non necessitando di proforma deve avere un layout diverso.
  - Rimodulare il layout del "moduloOrdineMagazzino" in maniera dale che:
      - Chi fa l'ordine (Davide e Lorenzo) possano vedere le quantità in stock del prodotto in questione (DIFFICILE DA IMPLEMENTARE SERVIREBBE UN DATASET CON GLI INCROCI TRA GLI SKU COPPO E QUELLI ANKER)
      FATTO - Eliminare il merge delle celle titolo di categoria
  - Pulsante salva e chiudi una fornitura. Permette il salvataggio delle forniture per avere dati storici sugli acquisti, prezzi ecc ecc. Inoltre permetterebbe di creare il link tra SKU Coppo e Sku Anker.
  - Eliminare i named range che non hanno scope workbook che vengono creati ogni qual volta si duplica un sheet.
