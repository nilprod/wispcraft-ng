# Wispcraft-ng

Fork of [Mercury Workshop's Wispcraft](https://github.com/MercuryWorkshop/wispcraft), a patch for eaglercraft that allows joining regular online mode minecraft servers from the browser, tunneled over wisp

Uses [epoxy-tls](https://github.com/r58Playz/epoxy-tls) to log in and fetch skins from the Minecraft server, and also connect to online mode minecraft servers

Built with the Web Streams API, using `TransformStream` and pipes to parse the minecraft protocol

## Notes for 1.14.x

Note that 1.14 support is incomplete, `SUpdateRecipesPacket` packet is not fixed but skipped (lmao), the reason is that specific packet can cause the client connection between server unresponsive (tested on [EymenWSMC](https://github.com/eymenwsmc/)'s 1.14.4 build), also including some other packets too (inspect it inside browser's console yourself).

FYI: When creating a new server entry inside multiplayer, you should use `wss://` or `ws://` as a starting protocol prefix, like `wss://settings://` and `wss://java://anyjavaserver.net`.

FYI(2): [EymenWSMC](https://github.com/eymenwsmc/)'s 1.14.4 build is also likely to crash upon ChestScreen on multiplayer servers, idk why.
