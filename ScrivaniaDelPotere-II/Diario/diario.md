# Diario — ScrivaniaDelPotere-II

## Cronologia ricostruita dalla conversazione

1. **Obiettivo iniziale:** usare Godot per realizzare un gioco 3D open world collegato al progetto `ScrivaniaDelPotere-II`, descritto come simulazione gestionale e politica in prima persona.
2. **Prototipo minimo:** viene riportato un prototipo Godot 4 isolato in `godot_open_world/`, con controller in prima persona, interazione `E`, scena piazza/municipio e streaming asincrono. Sono riferiti import, runtime headless, smoke test, `npm run runtime:check` (10/10) e `git diff --check` pulito. Godot 4.7.2 è indicato come scaricato con hash SHA256 verificato.
3. **Passi 2 e 3:** viene riferita l'aggiunta di `chunk_1_0`, ciclo di streaming, floating origin e test dedicati. È anche riportato l'avvio non-headless con OpenGL 3.3 su NVIDIA; all'inizio resta aperta la prova manuale di mouse e tastiera.
4. **Chiusura degli edge case:** sono descritti offset riletto all'attach per i chunk in-flight, rebase dopo `move_and_slide()` nello stesso tick fisico, isteresi di un chunk e test per richieste pendenti/oscillazione/reload. Viene citato anche `chunk_2_0`/`office_district_chunk.gd`.
5. **Scelta di design:** l'utente sceglie una rete di sicurezza sul tick fisico, invece che affidarsi solo alla chiamata esplicita nel controller. La conversazione riporta un watchdog sul tick fisico, test a soglia di 3.000 unità e i quattro casi tecnici coperti.
6. **Ultimo stato descritto:** rimane da fare la verifica visiva manuale. Persistenza delta, contenuti (NPC/POI) e integrazione con la web app sono ancora milestone future; non è indicata una data di uscita.

## Cosa ha funzionato secondo quanto riportato

- Test ripetibili e test da cache pulita per verificare lo streaming.
- Tenere il prototipo Godot separato dalla web app JS.
- Trattare in modo esplicito chunk in-flight, tick del rebase e isteresi.
- Distinguere l'avvio tecnico del renderer dalla verifica visiva dell'esperienza.

## Cosa non è ancora noto o verificato

- Esito della prova manuale di mouse/tastiera, prompt, pop al rebase e framerate.
- Persistenza dello stato durante unload/reload dei chunk.
- Presenza e comportamento di NPC, POI, dialoghi o missioni nel prototipo descritto.
- Contratto e modalità di integrazione fra Godot e la web app JS.
- Target di rilascio, data e piano commerciale.

## Stime e ambiguità

La conversazione non stabilisce una data di uscita. Le stime di settimane per una demo end-to-end sono indicative e dipendono da cosa si intende per “giocabile”; il prototipo tecnico descritto non equivale a un gioco completo o a una build distribuibile.

TODO: Aggiornare questa cronologia con date/commit verificabili e con l'esito dei test manuali.