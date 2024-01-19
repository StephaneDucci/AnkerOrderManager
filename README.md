# AnkerOrderManager
Un file excel per la gestione delle forniture Anker e la vendita ai clienti Coppo.

Update 3.1:

- Passaggio da una formula matriciale a una tabella pivot per il calcolo dell'ordine aggregato
- I riferimenti in "Anker" sono stati aggiornati e riferiscono correttamente alla nuova tabella pivot
- Sono stati ridefiniti tutti i named range e ora sono pochi e più chiari
- E' stato aggiunto lo sku anker al modulo cliente
- E' stato rimosso il tasto in controllo active x con una classica shape

  Bugs da gestire:
  - URGENTE: Eliminare ogni doppione presente nel listone! I doppioni rendono il cerca verticale con il nome della referenza inefficace!
      - Idea: per i formati "strani" (quelli diversi da 0,7 e 1 lt) se c'è un doppione aggiungere il size nella descrizione del prodotto
  - Gestire il bug che porta a non selezionare correttamente il range da copiare quando si importa un ordine cliente su una nuova fornitura 

  Features da aggiungere:
  - Sheet con gli idnirizzi fisici dei clienti
  - Routine per la creazione in automatico della proforma
  - Creare un nuovo pulsante nel pannello di controllo "Nuovo Ordine Negozi". Essendo l'ordine dei negozi più grande e non necessitando di proforma deve avere un layout diverso.
  - Rimodulare il layour del "moduloOrdineMagazzino" in maniera dale che:
      - Chi fa l'ordine (Davide e Lorenzo) possano vedere le quantità in stock del prodotto in questione
      - Eliminare il merge delle celle titolo di categoria



Le principali features da aggiungere alla 3.0 breve sono:

- Uno sheet con il database degli indirizzi fisici dei clienti dove spedire la merce. Gli indirizzi servono per compilare la proforma in automatico.
- Rifare il pulsante "aggiungi a fornitura" con l'utilizzo di una shape dato che il pulsante a controllo active x dà problemi con excel 2007
- Scrivere la sub routine per creare le proforma in automatico partendo dall'ordine. La proforma deve essere salvata come file esterno indipendente facilmente.
