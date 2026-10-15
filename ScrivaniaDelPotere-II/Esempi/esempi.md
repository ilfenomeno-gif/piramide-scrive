# Esempi e risultati riportati — ScrivaniaDelPotere-II

> Gli esempi sotto riassumono quanto dichiarato negli allegati e nella conversazione condivisa; non sono stati riprodotti o verificati in questo workspace.

## Prototipo iniziale

- `world_streamer.gd` usa `ResourceLoader.load_threaded_request` per il caricamento asincrono del chunk iniziale.
- `player_controller.gd` gestisce il movimento in prima persona e l'interazione con `E`.
- `city_hall_chunk.gd` rappresenta la piazza/municipio e una scrivania fisica.
- Sono riportati import e runtime headless riusciti e uno smoke test che controlla caricamento del chunk, abilitazione del movimento ed emissione del segnale d'interazione.
- Sono riportati `npm run runtime:check` con 10/10 esiti positivi e `git diff --check` pulito; il prototipo è descritto come isolato per lasciare intatta la web app.

## Streaming e floating origin

- È riportato il ciclo load → unload → reload di `chunk_1_0`, con `queue_free` verificato.
- È riportato un secondo chunk (`chunk_2_0`) e un test dello streaming; il nome `office_district_chunk.gd` è citato nella conversazione.
- Il floating origin trasla player e chunk attivi mantenendo gli ID logici.
- Una scena di chunk caricata in-flight rilegge l'offset corrente al momento dell'attach.
- Il rebase avviene nello stesso tick fisico dopo `move_and_slide()`, con un watchdog sul tick fisico per coprire spostamenti esterni al controller.
- `unload_hysteresis` è indicato con default di un chunk.
- Sono riportati test per richieste pendenti durante il rebase, oscillazione/identità dell'istanza, scaricamento oltre la fascia di isteresi e raycast/reload.

## Verifica ancora da fare

- Avviare la build con rendering e provare di persona mouse, rilascio con `Esc`, pitch, prompt `E`, eventuali pop al rebase e FPS attraversando i confini dei chunk.
- L'assenza di pop, la stabilità del prompt e le prestazioni percepite non sono dimostrate dai test automatici descritti.

TODO: Aggiungere screenshot/video o log di una sessione manuale e linkare i test effettivi nel repository.