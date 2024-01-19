# AnkerOrderManager
Un file excel per la gestione delle forniture Anker e la vendita ai clienti Coppo.

Update 3.1:

- Passaggio da una formula matriciale a una tabella pivot per il calcolo dell'ordine aggregato
- I riferimenti in "Anker" sono stati aggiornati e riferiscono correttamente alla nuova tabella pivot
- Sono stati ridefiniti tutti i named range e ora sono pochi e più chiari
- E' stato aggiunto lo sku anker al modulo cliente
- E' stato rimosso il tasto in controllo active x con una classica shape

  Features e/o bugs ancora da aggiungere e/o gestire:
  - Sheet con gli idnirizzi fisici dei clienti
  - Routine per la creazione in automatico della proforma
  - Gestire il bug che porta a non selezionare correttamente il range da copiare quando si importa un ordine cliente su una nuova fornitura


Le principali features da aggiungere alla 3.0 breve sono:

- Uno sheet con il database degli indirizzi fisici dei clienti dove spedire la merce. Gli indirizzi servono per compilare la proforma in automatico.
- Rifare il pulsante "aggiungi a fornitura" con l'utilizzo di una shape dato che il pulsante a controllo active x dà problemi con excel 2007
- Scrivere la sub routine per creare le proforma in automatico partendo dall'ordine. La proforma deve essere salvata come file esterno indipendente facilmente.
