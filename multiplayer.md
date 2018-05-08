## Multiplayer Servers

I've bee playing with the idea of multiplayer servers recently, and I've signed myself up ot use DigitalOcean as a virtual server hosting method. I'm enjoying how easy it was to get set up so far and now its just aboout trying to dodge SSH blocking at my work so I can use git properly (failing to a curl 56).

### Getting the server Copy

In order to do this you just have to nab a server copy of Godot and run it on the VM. I just usd curl to download the engine from a link I ripped from their Downloads section.

https://godotengine.org/download/linux

### Loading source code to the VM

I wanted to have this packed up in a file but this was posing issues for now. I'd really just like to have it all zipped up and sitting next to the running engine.

    ./run.sh
    --------
    export SERVER_CODE=1
    ./godot --path <path/to/game>

### Connecting to a multiplayer game

You should build games with multiplayer in mind, in recent times it is common to keep your game open to the idea of multiplayer.
The exported source code of your game should be looking for any incoming peers and just showing their name in a list. Allow clients to connect and then change their name and send a message. This is a simple function and should be proving to see if you can even handle the process of simple messages.
