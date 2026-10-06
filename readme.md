# Diagramma delle classi - Agenzia interinale

Nel diagramma ho rappresentato le classi dell'applicazione dell'agenzia interinale.

Ho creato una classe astratta Utente che contiene i dati in comune, cioè id, email e password, e i metodi per registrarsi e fare il login. Da Utente ereditano Azienda e Cliente, perché tutti e due sono utenti del sito ma hanno dati diversi: l'azienda ha la ragione sociale e la partita IVA, il cliente ha nome e cognome.

L'azienda può inserire le offerte di lavoro con il metodo inserisciOfferta. Ogni offerta ha la tipologia, il titolo richiesto, la data di inizio e di fine e il compenso orario. Un'azienda può avere tante offerte, mentre un'offerta appartiene a una sola azienda.

Il cliente può inviare le richieste di occupazione con il metodo inviaRichiesta. Ogni richiesta ha la tipologia, i titoli posseduti e le date in cui il cliente è disponibile. Anche qui un cliente può fare tante richieste, ma ogni richiesta è di un solo cliente.

ServerOfferte è un'interfaccia che rappresenta il server già esistente. Ha due metodi: uno per memorizzare le offerte e uno per elaborare le richieste, che restituisce la lista delle offerte compatibili. Azienda e Cliente sono collegati al server con una linea tratteggiata perché lo usano solo quando devono salvare un'offerta o mandare una richiesta.
