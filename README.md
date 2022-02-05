# ![logo](https://raw.githubusercontent.com/azerothcore/azerothcore.github.io/master/images/logo-github.png) AzerothCore

## mod-skip-dk-starting-area

- Latest build status with azerothcore: [![Build Status](https://github.com/azerothcore/mod-skip-dk-starting-area/workflows/core-build/badge.svg?branch=master&event=push)](https://github.com/azerothcore/mod-skip-dk-starting-area)

## Description

- Skips the Death Knight starting zone, for those who want to make a Death Knight without having to go through the starting area.

## How to use ingame

1. Enable in conf
2. Go into conf and set any features you want to enable or modify
3. Make a Death Knight and login.

## Notice

Due to the uniquiness of the module you will get this message on the worldconsole, but nothing is broken. It is due to the npc not exactly having a gossip menu in the database, the script handles the gossip menu because of the additional locales.
![image](https://user-images.githubusercontent.com/16887899/152654078-7b94c62c-a5e8-42ed-96ed-39ffaacf38b1.png)

Please add the adjustment to the conf to have that error message not show up:
```
#    Creatures.CustomIDs
#        Description: The list of custom creatures with gossip dialogues hardcoded in core,
#                     divided by "," without spaces.
#                     It is implied that you do not use for these NPC dialogs data from "gossip_menu" table.
#                     Server will skip these IDs during the definitions validation process.
#        Example:     Creatures.CustomIDs = "190010,55005,999991" - Npc for Transmog, Guild-zone and 1v1-arena modules
#        Example:     Creatures.CustomIDs = "190010,55005,999991,25462,98888" - Npcs for Transmog, Guild-zone, 1v1-arena modules
#                                                                               Skip Dk Module, Racial Trait Swap Modules
#        Default:     ""

Creatures.CustomIDs = "190010"
Creatures.CustomIDs = "190010,55005,999991,25462,98888"
```

## Requirements

- Latest AzerothCore Wotlk commit

## Installation

1. Simply place the module under the `modules` directory of your AzerothCore source. 
1. Re-run CMake and rebuild the AzerothCore source.

## Edit module configuration (optional)

If you need to change the module configuration, go to your server configuration folder (where your worldserver or worldserver.exe is), copy SkipDKModule.conf.dist to SkipDKModule.conf and edit that new file.

### Credits ###
------------------------------------------------------------------------------------------------------------------
- [acidmanifesto (MDic)](https://github.com/acidmanifesto/TC-Custom-Scripts/tree/main/335%20TC/Official%20Trinitycore%20Custom%20Scripts/Official%20Merged/Skip%20Death%20Knight%20Starter%20Area%20Module)
- [Jinnaix](https://github.com/Jinnaix)
- AzerothCore: [repository](https://github.com/azerothcore) - [website](http://azerothcore.org/) - [discord chat community](https://discord.gg/PaqQRkd)
