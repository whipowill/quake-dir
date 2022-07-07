# Quake

A directory of files for playing Quake multiplayer w/ bots.

This was one of the first multiplayer games I played as a kid.  I was probably around 12 years old, and we played on a service called [MPlayer](https://www.engadget.com/2015-10-22-mplayer-relaunch.html).  I played the heck out of this game back then.  I wanted to relive the memories.

This repository includes my files for playing the game.  I play w/ [FrikBot4](https://github.com/whipowill/quake-mod-frikbot4), which I've modified to my tastes:

- Play multiplayer deathmatch games w/ bots (very fun).
- Play multiplayer coop games where all items respawn over time (very helpful).

I don't have any expansions or campaign mods in here, this is straight Quake w/ emphasis on multiplayer.

## Install

- Download this respository to a ``Quake`` directory.
- Download the game engine [QSS-M](https://qssm.quakeone.com/) and put it in that directory.
- Find a copy of the [game files](https://archive.org/search.php?query=quakeresources&sin=) (I use the 2021 remaster).
- Put the pak files into the ``id1`` directory.
- Put the music files into the ``id1/music`` directory.
    - You might want to use the music files from Q2, I think it's better.
- Setup your game shortcuts.

To launch the game w/ FrikBot4 you have to make a game shortcut that includes ``-game frikbot4``.

On Linux I use this command line alias in my ``~/.bashrc`` file:

```
alias quake="cd ~/Games/Linux/Quake && __NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia __VK_LAYER_NV_optimus=NVIDIA_only ./QSS-M-l64 -game frikbot4 -listen 16"
```

You have to have the ``cd /path/to/your/quake/folder`` or else the music files won't play.

## Bots

You can control the bots via the console.  Press the ~ key to bring down the console screen.

- ``teamplay 1`` - turn on teamplay games
- ``impulse 100`` - add a bot to the game
- ``impulse 101`` - add a bot to the other team
- ``impulse 102`` - remove most recently added bot
- ``impulse 103`` - spectate other players (use ``kill`` to exit)

I've included my ``frikbot4/autoexec.cfg`` which binds ``INSERT``, ``DELETE``, and ``BACKSPACE`` to add team bots, add enemy bots, and remove bots.

## Rules

Note that my ``frikbot4/autoexec.cfg`` file includes a huge game change: it slows the maximum movement speed by 20%.

```
sv_maxspeed 256 // 320 is default
```

Maybe it's bc I'm getting older, maybe it's because I played Halo for so many years, but the movement speed in Quake is insanely fast.  I find the game more fun to slow it down.

This has a secondary effect of making "strafe jumping" not really a thing.  If you're an old school Quake player you know what that means.

You may not want this change, and if so you would remove this line from the file and run ``sv_maxspeed 320`` in the console to restore the original setting.

## Maps

This is a list I'm trying to compile of the "best" multiplayer maps.

Of the maps that come preloaded w/ the game:

- ``dm3`` - [The Abandoned Base](https://www.quakeworld.nu/wiki/Dm3) (Id 1996)
- ``dm6`` - [The Dark Zone](https://www.quakeworld.nu/wiki/Dm6) (Id 1996)
- ``e1m1`` - Slipgate Complex (Id 1996)
- ``e1m2`` - [Castle of the Damned](https://www.quakeworld.nu/wiki/E1m2) (Id 1996) :star:
- ``e1m3`` - Necropolis (Id 1996)
- ``e1m4`` - Grisly Groto (Id 1996)
- ``e1m5`` - Gloom Keep (Id 1996)
- ``e1m7`` - House of Chthon (Id 1996)

Of the 500+ community maps included w/ this repo:

- ``aerowalk`` - [Aerowalk](https://www.quakeworld.nu/wiki/Aerowalk) (Preacher 1998) :star:
- ``auhdm1`` - [Forgotten](https://www.quakeworld.nu/wiki/Auhdm1) (Auhsan 1999)
- ``cmt3`` - [Deutsch Machine](https://www.quakeworld.nu/wiki/Cmt3) (Baby Roo 2002)
- ``cmt5b`` - [Dreamweaver](https://www.quakeworld.nu/wiki/Cmt5b) (Qurnel 2003)
- ``dad2`` - [Dad's Playground II](https://www.quakeworld.nu/wiki/Dad2) (Zaka 2008)
- ``doomed`` - [Doomed](https://www.quakeworld.nu/wiki/Doomed) (Record 2009) :star:
- ``efdm9`` - [Tangerine Dream](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Mr. Fribbles 1999)
- ``q1edge`` - Edge (Id 1999) :star:
- ``rwild`` - [Running Wild](https://www.quakeworld.nu/wiki/Rwild) (Qurnel 2007) *
- ``schloss`` - [Schloss Adler](https://www.quakeworld.nu/wiki/Schloss) (Zaka 2004)
- ``skull`` - [Skull Hunt](https://www.quakeworld.nu/wiki/Skull) (Zaka 2003)
- ``spinev2`` - [Spine](https://www.quakeworld.nu/wiki/Spinev2) (Headshot 1998)
- ``strafin6`` - [Quake Addiction](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Peej 1999)
- ``travelert6`` - [Le Voyageur Cosmique](https://www.quakeworld.nu/wiki/Travelert6) (VoodooChopstiks 2007) *
- ``ultrav`` - [Ultra Violence](https://www.quakeworld.nu/wiki/Ultrav) (Escher 1997) :star: :heart:
- ``ztndm2`` - Show No Mercy (Ztn 1997)
- ``ztndm3`` - [Blood Run](https://www.quakeworld.nu/wiki/Ztndm3) (Ztn 1997) :star:
- ``ztndm4`` - Steeler (Ztn 1997)

Honorable mentions:

- ``ava`` - [Ava](https://www.quakeworld.nu/wiki/Ava) (Alice 2020) *
- ``catalyst`` - [Catalyst](https://www.quakeworld.nu/wiki/Catalyst) (Tehace 2015) * :star:
- ``fabrik`` - [Mammoth Fabrik](https://www.quakeworld.nu/wiki/Fabrik) (Alice 2021) *
- ``hex`` - [Hex](https://www.quakeworld.nu/wiki/Hex) (Alice 2020) *
- ``monsoon`` - [Monsoon](https://www.quakeworld.nu/wiki/Q1q3monsoon) (Mick 2017) *
- ``nova`` - [Nova](https://www.quakeworld.nu/wiki/Nova) (Alice 2022) * :star:
- ``obsidian`` - [Obsidian](https://www.quakeworld.nu/wiki/Obsidian) (Lurq 2020) *
- ``panzer`` - [Panzerfaust](https://www.quakeworld.nu/wiki/Panzer) (Alice 2021) *
- ``rock`` - [Rock](https://www.quakeworld.nu/wiki/Rock_(Map)) (Alice 2020) *
- ``shifter`` - [Shifter](https://www.quakeworld.nu/wiki/Shifter) (Foogs 2015) *
- ``toxicity`` - [Toxicity](https://www.quakeworld.nu/wiki/Toxicity) (Thuriam 2015) *

I think this is a solid list.  The maps marked w/ an * mean they are newer maps and don't have the bot waypoint files, but the bots can still play them.

You can skip to any map you want to play via the console:

```
map <MAPCODE>
```

You can edit ``frikbot4/maps.cfg`` to control what maps are included in the automatic map rotation.

## Notes

- When playing teamplay or coop games you have to have the same color pants as your teammates or else you will have friendly fire issues.

## Credits

- Original FrikBot mod by FrikaC, Igor9, and JLaw

## References

- [QSS-M](https://qssm.quakeone.com/) - open source port of the original ID Software Quake.
- [Quake Console Commands](https://docs.google.com/spreadsheets/d/1ubOuromaXpZonfL-eJ-KA7q-xSRiBBuSvxahzF-uFOY/edit#gid=0) - a list of all available console commands.
- [Quake Official Archive](https://github.com/Jason2Brownlee/QuakeOfficialArchive) - an archive of all Quake versions w/ a little history.
- [Quake Bot Archive](https://github.com/Jason2Brownlee/QuakeBotArchive) - an archive of all Quake bot versions w/ a little history.
- [Classic Custom Quake DM Levels](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) - a list of favorite DM maps w/ history of each.
- [Category: Maps](https://www.quakeworld.nu/wiki/Category:Maps) - a list of maps w/ articles on QuakeWorld.
- [Quake2 Soundtrack](https://archive.org/search.php?query=quakeresources&sin=) - shredding metal music which works w/ Quake1.
- [Quake2 N64 Soundtrack](https://www.moddb.com/games/quake-2/addons/nintendo-64-soundtrack-ogg-format) - creepy ambience music which works w/ Quake1.
- [r/Quake on Reddit](https://www.reddit.com/r/quake/search/?q=best%20maps&restrict_sr=1&sr_nsfw=) - searching for discussions on best deathmatch maps.
- [QuakeWorld Maps Index](https://maps.quakeworld.nu/all/) - downloadable links to all the maps ever made.