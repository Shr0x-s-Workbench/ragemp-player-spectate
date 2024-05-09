# RAGEMP Player Spectate

A simple 'admin' script that allows players to spectate other players.

# Installation

> This code requires you to have at least basic typescript knowledge

**Clientside**
Simple import `spectate.client.ts` to your main file initializer:
`import "./spectate.client"`

**Server Side**
Simply import `spectate.server.ts` to your main file initializer

Example command usage:

```
/spectate 1 //start spectating player id 1
/spectate off //stop spectating
```

Useful methods (client-side)

```ts
import Spectator from "./modules/spectate.client";

/*
Checks, useful variables to keep track of whether a player is in spectate mode or 
is_spectating -> true/false, returns whether the local player is in spectator mode or not.
spectating_player -> returns the target player handle which the local player is spectating
spectating_player_id -> returns the target player remote id which the local player is spectating.
*/
const { is_spectating, spectating_player, spectating_player_id } =
  Spectator.getSpectatingData;

/*
 Start spectating a target player given the target's remote id.
*/
Spectator.start(target);

/*
 Stop spectating.
*/
Spectator.stop();
```
