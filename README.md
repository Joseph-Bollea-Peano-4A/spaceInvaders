# SpaceInvaders
classe SpaceInvaders
in questa classe si estende la classe jFrame che ci permette di avere delle funzionalità riguardati l'ambiente grafico, come per esempio cliccare la "x" per chiudere la finestra di gioco.

Per quanto riguarda la classe Space essa estende la classe Canvas che ci permette di catturare gli input dell' utente come per esempio il click di un pulsante della tastiera e aggiungere elementi grafici.

# step1
In questo step abbiamo creato la classe Intro che serve ad aggiungere una scritta e degli elementi grafici,questo è possibile perchè la classe Intro eredita la classe Space che a sua volta ereditala classe Canvas.

# step2
in questo step si vuole dare un' animazione alla scritta che compare facendola venire verso l'interno dello schermo,per far ciò si crea un metodo run all'interno della classe Intro e si richiama il metodo repaint(ereditato dalla classe Canvas) all' interno di un ciclo.Dopo che il medoto paint sviluppa un immagine si chiama il metodo repaint ch richiamerà il metodo paint cancellando l'immagine sviluppata in prcedenza.

# step3
In questo step abbiamo eliminato lo sfarfallio causato dall' animazione del titolo creata nel precedente step. Per far ciò abbiamo creato due Canvas in maniera tale che quand un immagine viene sviluppata la successiva sarà subito pronta per sostituire quella visualizzata in precedenza.A livello di codice per far ciò abbiamo usato la classe BufferStrategy derivata dalla classe Canvas.

A livello hardware per far funzionare questo metodo dobbiamo prendere come esempio un monitor che può avere un refresh rate di 60hz,se non ci fossero 2 classi canvas vedremmo lo sfarfallio questo perchè se la scheda video sviluppasse una immagine con una durata di 5hz e poi la prossima sarà disponible solo dopo 2hz in questi 2hz vedremmo questo effetto di sfarfallio.

Con questa tecnica invece avendo a disposizione queste 2 classi canvas dopo lo sviluppo di una immagine sarà subito pronta la seconda eliminandoo questo effetto di sfarfallio.
