# Riferimenti — ScrivaniaDelPotere-II

## Repository e motore

- [Repository ScrivaniaDelPotere-II](https://github.com/ilfenomeno-gif/ScrivaniaDelPotere-II) — repository del progetto indicato nella conversazione.
- [Godot Engine](https://github.com/godotengine/godot) — motore scelto per il prototipo 3D.

## Risorse citate nella ricerca

Questi link sono stati proposti o consultati nella conversazione; non sono prova che gli strumenti siano stati adottati nel progetto.

- [GD-Agentic-Skills: riferimenti su implementazioni open world](https://github.com/thedivergentai/GD-Agentic-Skills/blob/main/skills/godot-genre-open-world/references/open-world-elite-implementations.md) — panoramica di pattern open world.
- [GD-Agentic-Skills: guida open world per Godot](https://github.com/thedivergentai/GD-Agentic-Skills/blob/main/skills/godot-genre-open-world/SKILL.md) — streaming, prestazioni e architettura.
- [Godot Open World Database](https://github.com/DigitallyTailored/Godot-Open-World-Database) — addon di streaming menzionato.
- [Chunx](https://github.com/SlashScreen/chunx) — plugin Godot 4 per world streaming menzionato.
- [Zenva: Game Overworld Tutorial (Godot)](https://www.gamesinprogress.com/indie-game-developers/zenva/game-overworld-tutorial-godot) — tutorial di overworld citato.

## Concetti tecnici raccolti

- Streaming asincrono a chunk; caricare e scaricare scene in base alla posizione del giocatore.
- Floating origin per mantenere precisione a grandi distanze.
- Isteresi nello scaricamento dei chunk per ridurre il churn ai confini.
- Persistenza delta per conservare lo stato degli oggetti quando i chunk vengono scaricati.
- HLOD/LOD e attenzione alle prestazioni per mondi estesi.
- Possibile integrazione fra Godot e web app tramite stato condiviso (ad esempio JSON) o comunicazione locale (ad esempio WebSocket): opzioni discusse, contratto non deciso.

TODO: Verificare compatibilità/versioni e decidere quali risorse o plugin, se qualcuno, adottare davvero.