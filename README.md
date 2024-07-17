Ciao ragazzi,
Esercizio di oggi: *Vue Slider*
nome repo: vue-slider
*Descrizione:*
Partendo dal markup della versione svolta in js plain, rifare lo slider ma questa volta usando Vue.
*Bonus:*
1- al click su una thumb, visualizzare in grande l'immagine corrispondente
2- applicare l'autoplay allo slider: ogni 3 secondi, cambia immagine automaticamente
3- quando il mouse va in hover sullo slider, bloccare l'autoplay e farlo riprendere quando esce
*Consigli del giorno:*
- regola d'oro: riciclare ovunque possibile! Questo significa che per la parte di markup possiamo recuperare html e css dell'esercizio svolto qualche giorno fa: è già tutto pronto!
- il riciclo spesso va a braccetto con le funzioni! Sapendole sfruttare bene, l'esercizio si riduce a poche righe ;)
Buon lavoro e buon divertimento!

soluzione

1.creo l'istanza vue dentro js e inserisco l'array di oggetti dentro data
2.inserisco all'interno del return un active con indice pari a 0
3.dentro methods creo 2 funzioni per far si che quando arrivo all'ultima slide e clicco ancora per andare a destra mi torni all'inizio e viceversa
4.dentro la prima funzione (previmage) inserisco una condizione
5.se l'active dell'immagine è uguale a 0 allora assegno ad active l'indice dell'ultimo elemento
7.altrimenti decremento active
8.dentro la seconda funzione (nextimage) faccio il contrario, se l'active dell'immagine è uguale all'indice dell'ultimo elemento allora assegno ad active indice 0
9.altrimenti incremento active
10.richiamo le funzioni tramite evento click direttamente nel dom
11.ciclo le immagini e thumb tramite l'attributo v-for
12.aggiungo l'operatore ternario dentro la classe img delle thumb e controllo se l'active è uguale all'indice
13.se risulta vera gli inserisco la classe .active altrimenti stringa vuota