# ScrivaniaDelPotere-II — Istruzioni di progetto

## Obiettivo

La conversazione descrive **ScrivaniaDelPotere-II** come un gioco di simulazione gestionale e politica in prima persona, originariamente associato a una web app JavaScript. L'obiettivo dichiarato è esplorare la realizzazione di un'esperienza 3D open world con Godot, mantenendo la logica gestionale e il prototipo 3D come layer distinti finché non verrà definito un contratto d'integrazione.

## Stato noto riportato nella conversazione

- Il prototipo Godot è isolato in `godot_open_world/` nel repository.
- Sono descritti un controller in prima persona, interazione con `E`, streaming asincrono dei chunk e floating origin.
- Il contenuto iniziale comprende una piazza/municipio con scrivania fisica; in seguito sono citati `chunk_1_0`, `chunk_2_0` e `office_district_chunk.gd`.
- Sono riportati test automatici e avvio del renderer non-headless. Questi risultati non sono stati rieseguiti durante la creazione di questa piramide.
- La verifica visiva manuale di mouse, tastiera, prompt, rebase e framerate è ancora indicata come aperta.
- La persistenza delta, il popolamento con NPC/POI e l'integrazione con la web app sono indicate come milestone non completate nell'ultimo stato descritto.

## Target

TODO: Chi è il giocatore/utente finale previsto? La conversazione parla del progetto e delle sue meccaniche, ma non definisce un target demografico o commerciale.

## Criteri per un risultato fatto bene

- Tenere separati il prototipo Godot e la web app JS finché il contratto fra i due layer non è deciso.
- Non dichiarare il gioco visivamente giocabile basandosi solo su test headless o sull'avvio del renderer.
- Verificare load/unload/reload dei chunk, floating origin e isteresi con test ripetibili; la conversazione riporta questi controlli come effettuati.
- Fare una prova manuale in gioco: mouse catturato/rilasciato con `Esc`, movimento e pitch della camera, prompt `E`, attraversamento dei confini dei chunk e stabilità del framerate.
- Registrare separatamente ciò che è implementato, ciò che è stato testato e ciò che è solo una proposta.
- Non annunciare una data di uscita: la conversazione non riporta una data concordata e distingue la demo tecnica da un gioco completo.

## Cosa evitare

- Confondere architettura suggerita con funzionalità effettivamente implementate.
- Popolare il mondo con stato persistente prima di definire e testare come lo stato sopravvive allo scaricamento dei chunk.
- Modificare o danneggiare la web app esistente mentre si sviluppa il prototipo 3D isolato.
- Presentare stime di lavoro o tempi di uscita come impegni.

## Indice dei materiali

- `../Voce/voce.md` — indicazioni provvisorie sul registro tecnico.
- `../Riferimenti/riferimenti.md` — repository, motore e risorse citate.
- `../Esempi/esempi.md` — implementazioni e controlli riportati.
- `../Diario/diario.md` — tappe e stato aperto.

TODO: Confermare il target, le piattaforme di rilascio e se l'obiettivo è convertire il gioco esistente o affiancargli un'esperienza 3D.