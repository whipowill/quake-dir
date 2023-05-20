# Quake

A directory of files for playing Quake multiplayer w/ bots.  Checkout my [channel](https://www.youtube.com/@wscarlet) showcasing videos from the development of the [Scarlet](https://github.com/whipowill/quake-mod-scarlet) mod.

This was one of the first multiplayer games I played as a kid.  I was probably around 12 years old, and we played on a service called [MPlayer](https://www.engadget.com/2015-10-22-mplayer-relaunch.html).  I played the heck out of this game back then.  I wanted to relive the memories.

This repository includes my files for playing the game.  I don't have any expansions or campaign mods in here, this is straight Quake w/ emphasis on multiplayer.

### What's Included

- [Scarlet](https://github.com/whipowill/quake-mod-scarlet) - adds bots, blood, guts, and gore to the game (``/scarlet/progs.dat``)
- [HUD](https://github.com/whipowill/quake-mod-hud) - custom HUD layouts and team scoreboards (``/id1/csprogs.dat``)
- [AMI](https://github.com/NightFright2k19/quake_authmdl) - authentic model improvements (``/id1/pak1.pak``)
- [RHW](https://www.moddb.com/games/quake/addons/quake-right-handed-weapons) - right-handed weapon models (``/id1/pak2.pak``)
- [UAM](https://www.moddb.com/games/quake/addons/upgraded-armor-for-quake-1) - upgraded armor models (``/id1/gfx/`` and ``/id1/progs/``)
- [Q2S](https://github.com/whipowill/quake-mod-q2sounds) - sounds from Quake2 (``/id1/sounds/``)
- **Multiplayer Maps** - all the good maps to play (``/id1/maps/*.bsp``)
- **Waypoint Files** - stuff the bots need to work (``/id1/maps/*.way``)

## Install

- Download this [zipfile](https://github.com/whipowill/quake-dir/archive/master.zip)
- Extract to ``/path/to/quake/``
- Download the game engine [QSS-M](https://qssm.quakeone.com/) and put it in that directory
- Find a copy of the game files from the original game (I use the 2021 remaster)
- Put the pak files into the ``/path/to/quake/id1/`` directory
- Put the music files into the ``/path/to/quake/id1/music/`` directory
- Setup your game shortcut to include ``-game scarlet -particles 99999 -listen 16``
- Consult ``/path/to/quake/scarlet/autoexec.cfg`` to customize your keybinds

If you use terminal you can use GIT clone to make future updates super easy:

```
$ cd /your/path/to/games/
$ git clone https://github.com/whipowill/quake-dir.git Quake

$ cd /your/path/to/games/Quake
$ git pull origin master
```

On Linux I use this command line alias in my ``~/.bashrc`` file:

```
alias quake="cd ~/Games/Linux/Quake && __NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia __VK_LAYER_NV_optimus=NVIDIA_only ./QSS-M-l64 -game scarlet -particles 99999 -listen 16 -condebug"
```

## Settings

The Scarlet mod allows for customizing the game in some interesting ways.  Included in this repository are my [custom](https://github.com/whipowill/quake-dir/blob/master/scarlet/settings/custom.cfg) play settings.

### Vision & Goals

This is an attempt to preserve an FPS classic. In a world where real-life players have moved on, I wanted to capture and keep the multiplayer experience of the past.

What [Brutal](https://brutal-doom.com/) is for singleplayer Doom, I want Scarlet to be for multiplayer Quake. More blood, more gore, more guts, and maybe a little more glory than it had before.

- **Multiplayer** — preserve the deathmatch experience of the past
- **Blood & Gore** — dial up the gore to gratify my thirst for blood and violence
- **Fixes & Tweaks** — fix all the little broken things that bothered me
- **Weapons Balance** — improve combat w/ weapon damage and pacing
- **Fun Factor** — add melee attack, grenades, glory kills, and randomness
- **Customization** — unlock the game w/ extensive console variables

## Maps

I've put together a list of the "best" maps from multiplayer, both from the little I can remember of the 90's as well as the maps used in competitive play since that time.

### S Tier

- ``aerowalk`` - [Aerowalk](https://www.quakeworld.nu/wiki/Aerowalk) (Preacher 1998)
- ``fribdev1_2`` - [Powder Keg](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=17108.htm) (Mr. Fribbles 1998)
- ``maldm6`` - Malevolent Marmalade (Molevola 2006)
- ``nova`` - [Nova](https://www.quakeworld.nu/wiki/Nova) (Alice 2022)
- ``spinev2`` - [Spine](https://www.quakeworld.nu/wiki/Spinev2) (Headshot 1998)
- ``ultrav`` - [Ultra Violence](https://www.quakeworld.nu/wiki/Ultrav) (Escher 1997)

### A Tier

- ``doomed`` - [Doomed](https://www.quakeworld.nu/wiki/Doomed) (Zaka 2009)
- ``dm6_fp`` - [Dark Zone](https://www.slipseer.com/index.php?resources/the-dark-zone.99/) (Willits 1996, Fancypants 2022)
- ``e1m2`` - [Castle of the Damned](https://www.quakeworld.nu/wiki/E1m2) (Willits 1996)
- ``matdm2`` - Body Count (Mati 2006)
- ``q1edge`` - [The Edge](https://www.doomworld.com/idgames/idstuff/quakeworld/maps/q1edge) (Willits 1999)
- ``skull`` - [Skull Hunt](https://www.slipseer.com/index.php?resources/skull-hunt-by-zaka.100/) (Zaka 2003, Fancypants 2022)
- ``strafin6`` - [Quake Addiction](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Peej 1999)
- ``zxcdm1`` - [Shine](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=17386.htm) (Zxc 2001)

### B Tier

- ``auhdm1`` - [Forgotten](https://www.quakeworld.nu/wiki/Auhdm1) (Auhsan 1999)
- ``chesdm1`` - [Primal Etchings](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=59.htm) (Cheshire 1998)
- ``dm3_fp`` - [Abandoned Base](https://www.slipseer.com/index.php?resources/the-abandoned-warehouse.98/) (Romero 1996, Fancypants 2022)
- ``e1m7`` - [House of Chthon](https://quake.fandom.com/wiki/E1M7:_The_House_of_Chthon) (McGee 1996)
- ``effigy`` - Effigy of the Forgotten (Moloch 1999)
- ``imp1dm6`` - [Daedalous Revisited](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=17605.htm) (Biff 2002)
- ``naked7b2`` - [Deutsch Maschine](https://www.quakeworld.nu/wiki/Cmt3), aka ``cmt3`` (Baby Roo 2002)
- ``travelert6`` - [Le Voyageur Cosmique](https://www.quakeworld.nu/wiki/Travelert6) (VoodooChopstiks 2007)
- ``ztndm1`` - Smile, It Gets Worse (Ztn 1997)
- ``ztndm2`` - Show No Mercy (Ztn 1997)
- ``ztndm3`` - [Blood Run](https://www.quakeworld.nu/wiki/Ztndm3) (Ztn 1997)
- ``ztndm4`` - The Steeler (Ztn 1997)

### C Tier

- ``a2`` - [Return to Atlantis](https://www.quakeworld.nu/wiki/A2) (Pingu 1999)
- ``baldm6`` - [Scrap Metal](https://www.slipseer.com/index.php?resources/bals-classic-deathmatch-maps.58/) (Bal 1999)
- ``bovine`` - [Bovine Intervention](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=VIEWCOMMENTS&REVIEW_LINK=17646.htm) (Laerth 2002)
- ``bravado`` - [Bravado](https://www.quakeworld.nu/wiki/Bravado) (Foogs 2012)
- ``catalyst`` - [Catalyst](https://www.quakeworld.nu/wiki/Catalyst) (Tehace 2019)
- ``dad2`` - [Dad's Playground 2](https://www.quakeworld.nu/wiki/Dad2) (Zaka 2008)
- ``edc`` - [Eternal Dismemberment Complex](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Tyrann 1999)
- ``efdm9`` - [Tangerine Dream](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Mr. Fribbles 1999)
- ``fcastle`` - Forgotten Castle (Qurnel 2006)
- ``lilith`` - Lilith (Lilith 2006)
- ``locomoto`` - [Locomoto](https://www.quakeworld.nu/wiki/Locomoto), aka ``qwdm5`` (Quaker 2018)
- ``mjdm1pro`` - Expendable Youth (Mickey 2006)
- ``monsoon`` - [Monsoon](https://www.quakeworld.nu/wiki/Q1q3monsoon) (Mick 2017)
- ``naked5`` - [Kinky Afro](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Baby Roo 2002)
- ``pinion2`` - [Clockwork](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Retinal 2005)
- ``rapture1`` - [Imminent Boom](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Danimal 1997)
- ``rwild`` - [Running Wild](https://www.quakeworld.nu/wiki/Rwild) (Qurnel 2009)
- ``schloss`` - [Schloss Adler](https://www.quakeworld.nu/wiki/Schloss) (Zaka 2003)
- ``shifter`` - [Shifter](https://www.quakeworld.nu/wiki/Shifter) (Foogs 2015)
- ``toxicity`` - [Toxicity](https://www.quakeworld.nu/wiki/Toxicity) (Thuriam 2015)
- ``ukpak2`` - [UKPak2](https://www.quakeworld.nu/wiki/Ukpak2) (Zor 1999)
- ``zed`` - [Zed](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) (Vondur 1999)
- ``zed2`` - Zed2 (Vondur 2006)

## External Links

- [Slipseer](https://www.slipseer.com/index.php) - where all the cool Quake kids hangout
- [QSS-M](https://qssm.quakeone.com/) - open source port of the original ID Software Quake
- [Quake Console Commands](https://docs.google.com/spreadsheets/d/1ubOuromaXpZonfL-eJ-KA7q-xSRiBBuSvxahzF-uFOY/edit#gid=0) - a list of all available console commands
- [Quake Official Archive](https://github.com/Jason2Brownlee/QuakeOfficialArchive) - an archive of all Quake versions w/ a little history
- [Quake Bot Archive](https://github.com/Jason2Brownlee/QuakeBotArchive) - an archive of all Quake bot versions w/ a little history
- [Classic Custom Quake DM Levels](https://www.quaddicted.com/articles/10_classic_custom_quake_deathmatch_maps_that_scampie_likes) - a list of favorite DM maps w/ history of each
- [MPQ Archive: List of Reviews](https://mpqarchive.pauked.com/mpqold/MPQCGI.EXE-VIEW=SHOWMAP.htm#_top) - a vintage 90s era site rating all the community maps
- [QuakeWorld Maps Wiki](https://www.quakeworld.nu/wiki/Category:Maps) - a list of maps w/ articles on QuakeWorld
- [QuakeWorld Maps Playcount](http://stats.quakeworld.nu/index.php?a=maps&order=&page=1&sort=totalffaMatches&sortOrder=desc) - list of all the maps by playcount
- [QuakeWorld Maps Pics](https://www.quakeone.com/q1files/img/maps/) - if they made a photo it must have mattered
- [QuakeWorld Maps Index](https://maps.quakeworld.nu/all/) - downloadable links to all the maps ever made
- [Quaddicted Maps Index](https://www.quaddicted.com/files/maps/multiplayer/) - useful to find dates of map creation
- [Quaketastic](https://www.quaketastic.com/) - not sure what this is but might be useful somehow
- [Quake2 Weapons](https://quake.fandom.com/wiki/Weapons_(Q2)) - useful for mimicking settings
