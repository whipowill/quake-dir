# Quake

A directory of files for playing Quake multiplayer w/ [Frikbot4](https://github.com/whipowill/quake-mod-frikbot4).

This was one of the first multiplayer games I played as a kid.  I was probably around 12 years old, and we played on a service called [MPlayer](https://www.engadget.com/2015-10-22-mplayer-relaunch.html).  I played the heck out of this game back then.  I wanted to relive the memories.

This repository includes my files for playing the game.  I don't have any expansions or campaign mods in here, this is straight Quake w/ emphasis on multiplayer.

## Install

- Download this respository to a ``Quake`` directory.
- Download the game engine [QSS-M](https://qssm.quakeone.com/) and put it in that directory.
- Find a copy of the game files from the original game (I use the 2021 remaster).
- Put the pak files into the ``id1`` directory.
- Put the music files into the ``id1/music`` directory.
    - You might want to use the music files from Q2, I think it's better.
- Setup your game shortcuts.

To launch the game w/ Frikbot4 you have to make a game shortcut that includes ``-game frikbot4``.

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

I'm trying to compile a list of the "best" multiplayer maps.  The goal is to have a map rotation where every single map makes you say, "oh yeah I love this map!"  Open a support ticket if you think I missed one!

Of the maps that come preloaded w/ the game:

- ``dm3`` - [The Abandoned Base](https://www.quakeworld.nu/wiki/Dm3) (Id 1996)
- ``dm6`` - [The Dark Zone](https://www.quakeworld.nu/wiki/Dm6) (Id 1996)
- ``e1m1`` - Slipgate Complex (Id 1996)
- ``e1m2`` - [Castle of the Damned](https://www.quakeworld.nu/wiki/E1m2) (Id 1996)
- ``e1m3`` - Necropolis (Id 1996)
- ``e1m4`` - Grisly Groto (Id 1996)
- ``e1m5`` - Gloom Keep (Id 1996)
- ``e1m7`` - House of Chthon (Id 1996)

Of the 500+ community maps included w/ this repo:

- ``aerowalk`` - [Aerowalk](https://www.quakeworld.nu/wiki/Aerowalk) (Preacher 1998) :star:
- ``auhdm1`` - [Forgotten](https://www.quakeworld.nu/wiki/Auhdm1) (Auhsan 1999)
- ``chesdm1`` - [Primal Etchings](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=59.htm) (Cheshire 1998)
- ``dad2`` - [Dad's Playground II](https://www.quakeworld.nu/wiki/Dad2) (Zaka 2008)
- ``doomed`` - [Doomed](https://www.quakeworld.nu/wiki/Doomed) (Record 2009) :star:
- ``efdm9`` - [Tangerine Dream](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Mr. Fribbles 1999)
- ``fribdev1_2 ``- [Powder Keg](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=17108.htm) (Mr. Fribbles 1998) :star:
- ``imp1dm6`` - [Daedalous Revisited](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=17605.htm) (Biff 2002)
- ``naked7b2`` - [Deutsch Maschine](https://www.quakeworld.nu/wiki/Cmt3) (Baby Roo 2000)
- ``q1edge`` - Edge (Id 1999)
- ``schloss`` - [Schloss Adler](https://www.quakeworld.nu/wiki/Schloss) (Zaka 2004)
- ``skull`` - [Skull Hunt](https://www.quakeworld.nu/wiki/Skull) (Zaka 2003)
- ``spinev2`` - [Spine](https://www.quakeworld.nu/wiki/Spinev2) (Headshot 1998) :star:
- ``strafin6`` - [Quake Addiction](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Peej 1999)
- ``travelert6`` - [Le Voyageur Cosmique](https://www.quakeworld.nu/wiki/Travelert6) (VoodooChopstiks 2007) *
- ``ultrav`` - [Ultra Violence](https://www.quakeworld.nu/wiki/Ultrav) (Escher 1997) :star: :heart:
- ``ztndm3`` - [Blood Run](https://www.quakeworld.nu/wiki/Ztndm3) (Ztn 1997) :star:
- ``zxcdm1`` - [Shine](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=17386.htm) (Zxc 2001)

I think this is a solid list.  Maps marked w/ an * indicate missing bot waypoint files, so the bots may not perform well.  There are still new maps being developed, among them the maps created by [Alice](https://www.quakeworld.nu/wiki/Alice) are quite impressive.

You can skip to any map you want to play via the console:

```
map <MAPCODE>
```

You can edit ``frikbot4/maps.cfg`` to control what maps are included in the automatic map rotation.

## Notes

- When playing teamplay or coop games you have to have the same color pants as your teammates or else you will have friendly fire issues.

## Credits

- Original Frikbot mod by FrikaC, Igor9, and JLaw

## References

- [QSS-M](https://qssm.quakeone.com/) - open source port of the original ID Software Quake.
- [Quake Console Commands](https://docs.google.com/spreadsheets/d/1ubOuromaXpZonfL-eJ-KA7q-xSRiBBuSvxahzF-uFOY/edit#gid=0) - a list of all available console commands.
- [Quake Official Archive](https://github.com/Jason2Brownlee/QuakeOfficialArchive) - an archive of all Quake versions w/ a little history.
- [Quake Bot Archive](https://github.com/Jason2Brownlee/QuakeBotArchive) - an archive of all Quake bot versions w/ a little history.
- [Frikbot4 for Quake](https://github.com/whipowill/quake-mod-frikbot4) - my repo for the source code of the bot mod.
- [Classic Custom Quake DM Levels](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) - a list of favorite DM maps w/ history of each.
- [Category: Maps](https://www.quakeworld.nu/wiki/Category:Maps) - a list of maps w/ articles on QuakeWorld.
- [r/Quake on Reddit](https://www.reddit.com/r/quake/search/?q=best%20maps&restrict_sr=1&sr_nsfw=) - searching for discussions on best deathmatch maps.
- [MPQ Archive: List of Reviews](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=SHOWMAP.htm#_top) - a vintage 90s era site rating all the community maps.
- [QuakeWorld Maps Index](https://maps.quakeworld.nu/all/) - downloadable links to all the maps ever made.