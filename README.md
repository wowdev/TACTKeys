# TACT Keys
This repo was created as a central place to store the ever increasing amount of (public) TACT encryption keys Blizzard uses to encrypt data in their games. 

Right now this repo only supports World of Warcraft, but other games might be added in the future.

## Format
The format is a space separated file with the 16-char key lookup (or name) and the 32-char key itself, both encoded as hex. 

`0123456789ABCDEF 0123456789ABCDEF0123456789ABCDEF`

**More fields might be added at the end of the line in the future (e.g. IDs), be sure to only read the necessary data per line.**

## Updates (WoW)
TACT keys in WoW are current distributed in a few ways:
- Client patches, keys are added to TactKey.db2 (with lookups in TactKeyLookup.db2)
- Hotfix pushes to TactKey.db2/TactKeyLookup.db2 sent down by the server to clients (cached in in DBCache.bin)
- As additional data to BroadcastText records sent down by the server as the user plays through content (cached in DBCache.bin)

As such, they can be extracted by reading the relevant [DB2](https://wowdev.wiki/DB2)s as well as [DBCache.bin](https://wowdev.wiki/ADB). 
