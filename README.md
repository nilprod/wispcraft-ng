# Wispcraft-ng

Fork of [Mercury Workshop's Wispcraft](https://github.com/MercuryWorkshop/wispcraft), a patch for eaglercraft that allows joining regular online mode minecraft servers from the browser, tunneled over wisp

Uses [epoxy-tls](https://github.com/r58Playz/epoxy-tls) to log in and fetch skins from the Minecraft server, and also connect to online mode minecraft servers

Built with the Web Streams API, using `TransformStream` and pipes to parse the minecraft protocol

## Notes for 1.14.x

When creating a new server entry inside multiplayer, you should use `wss://` or `ws://` as a starting protocol prefix, like `wss://settings://` and `wss://java://anyjavaserver.net`.

[EymenWSMC](https://github.com/eymenwsmc/)'s 1.14.4 build is likely to crash upon ChestScreen on multiplayer servers, idk why.
