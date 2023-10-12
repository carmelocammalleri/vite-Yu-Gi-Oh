# Vite Yu-Gi-Oh*

**Descrizione:**
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Al caricamento della pagina, effettuate una chiama ajax all’API di Yu Gi Oh: https://db.ygoprodeck.com/api/v7/cardinfo.php
e con i dati restituiti, stampate una card per ogni carta.
**ATTENZIONE**: l’api restituisce tutti i risultati in un colpo solo. Per evitare attese e/o rallentamenti nelle richieste, potete diminuire il numero di risultati sfruttando i parametri *num* e *offset*
https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0
**Bonus:**
Creare un componente loader da visualizzare fintantoché i risultati non sono pronti.

1. creare html composto da due elementi:
  a- header (lavorare nel file header.vue)
  b- main (lavorare nel file main.vue)
2. importare elementi ricreati in app.vue
3. stilare tramite scss le varie parti della pagina
4. creare una sezione, che serva poi per ciclare gli elementi dell'array che arriva dall'API url, per le cards che conterranno le singole card
5. stampare in app.vue le card
6. creare una funzione per la ricerca di quello che ci serve (?) 