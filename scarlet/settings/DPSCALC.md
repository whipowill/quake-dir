# Weapon DPS

Worked out from the settings that are live on this install, i.e. what you get after `autoexec.cfg` runs
`settings/custom.cfg`, which runs `init.cfg` and then `v4.cfg` (v4 wins wherever both set a value).
Read from the mod's weapon code in `src/weapons.qc`.  Quad damage, powerups and armor are left out unless stated.

**DPS = damage per shot / seconds between shots**, every shot landing.  The first shot of a fight lands at once,
so the time to kill is `(shots - 1) x rate of fire`.

## Settings used

| Setting | Value |
| --- | --- |
| `scarlet_dmg_axe` | 240 |
| `scarlet_dmg_bullets` | 4 (per pellet) |
| `scarlet_bullets_in_shell_sg` / `_ssg` | 6 / 24 |
| `scarlet_dmg_nails` | 3 |
| `scarlet_dmg_rockets` | 100 (rockets, grenades, hand grenades) |
| `scarlet_dmg_cells` | 100 |
| `scarlet_rof_*` | axe 0.6, sg 0.6, ssg 1.2, ng 0.075, sng 0.075, gl 0.6, rl 1.2, tb 1.6, hg 1.2 |
| `scarlet_spr_*` | sg 4, ssg 12, ng 0, sng 6 |
| `scarlet_axe_frametime` | 0.09 (four frames, so a swing is 0.36 s and the hit lands on the third frame, 0.18 s after the press) |
| `scarlet_ammo_spd_ng` / `_sng` | 4000, so both nailguns are hitscan, and each nail does half of `dmg_nails` (1.5) |
| `scarlet_ammo_dec_*` | all 1 (a super shotgun shot uses 2 shells, a super nailgun shot 2 nails) |
| `scarlet_ammo_max_*` | shells 24, nails 480, rockets 12, cells 6 |
| `scarlet_absorb_*` | green 0.3, yellow 0.5, red 0.7 |

## Damage and DPS

| Weapon | Damage per shot | Seconds per shot | DPS | Shots to kill 100 hp | Time to kill 100 hp |
| --- | --- | --- | --- | --- | --- |
| Axe | 240 | 0.6 | **400** | 1 | 0.00 s |
| Shotgun | 24 | 0.6 | **40** | 5 | 2.40 s |
| Super Shotgun | 96 | 1.2 | **80** | 2 | 1.20 s |
| Nailgun | 3 | 0.075 | **40** | 34 | 2.48 s |
| Super Nailgun | 6 | 0.075 | **80** | 17 | 1.20 s |
| Grenade Launcher | 100 | 0.6 | **166.7** | 1 | 0.00 s |
| Rocket Launcher | 100 | 1.2 | **83.3** | 1 | 0.00 s |
| Thunderbolt | 100 | 1.6 | **62.5** | 1 | 0.00 s |
| Hand Grenade | 100 | 1.2 | **83.3** | 1 | 0.00 s |

Average DPS across all nine: **115**.  Without the axe and hand grenade (the guns only): **79**.

Notes:
- Axe and hand grenade fire from the melee key, on their own timers, and don't use the weapon's ready time.
- The axe is the same 400 DPS as before (240 every 0.6 s instead of 120 every 0.3 s), but each swing now does 240, so it is one swing against no armor, green or yellow armor, and two against red armor (300 needed).  The hit lands 0.18 s after the press.
- Melee spam is 1 and the lunge is always on, with no cooldown, so a swing can lunge you 480 units a second into range.
- The rocket and grenade numbers are the peak: a rocket that lands beside someone does `100 - distance / 2` (a direct hit is the full 100 and doesn't also splash that target), and the blast reaches 140 units.  Your own blasts do half to you.
- Nailguns are tiny per shot but fire 13 times a second.  Being hitscan, there is no travel time to lead, so they only miss from aim.
- The thunderbolt fires once every 1.6 s as a single 100 damage beam, so it is a railgun in practice.

## What a full load of ammo is worth

| Weapon | Ammo per shot | Max ammo | Shots from full | Damage from full | Seconds of fire from full |
| --- | --- | --- | --- | --- | --- |
| Axe | none | - | unlimited | unlimited | - |
| Shotgun | 1 shells | 24 shells | 24 | 576 | 14.4 |
| Super Shotgun | 2 shells | 24 shells | 12 | 1152 | 14.4 |
| Nailgun | 1 nails | 480 nails | 480 | 1440 | 36.0 |
| Super Nailgun | 2 nails | 480 nails | 240 | 1440 | 18.0 |
| Grenade Launcher | 1 rockets | 12 rockets | 12 | 1200 | 7.2 |
| Rocket Launcher | 1 rockets | 12 rockets | 12 | 1200 | 14.4 |
| Thunderbolt | 1 cells | 6 cells | 6 | 600 | 9.6 |
| Hand Grenade | 1 grenades | 4 grenades | 4 | 400 | 4.8 |

The rocket launcher and thunderbolt run dry fast (12 rockets, 6 cells), while nails hold the most damage of any ammo: 1440 from a full 480, in the nailgun or the super nailgun.

## Pellet spread

The shotguns and super nailgun spread their pellets across a box `spr / 100` wide and `spr / 200` tall per unit of
distance (so `spr 4` is +/-4% across and +/-2% up and down).  A player is about 32 wide and 56 tall.  This is the share of
pellets landing on one player standing dead centre of the crosshair, and what that does to DPS:

| Distance | Shotgun (spr 4) | Super Shotgun (spr 12) | Super Nailgun (spr 6) |
| --- | --- | --- | --- |
| 128 | 100% = 40 DPS | 100% = 80 DPS | 100% = 80 DPS |
| 256 | 100% = 40 DPS | 52% = 42 DPS | 100% = 80 DPS |
| 512 | 78% = 31 DPS | 24% = 19 DPS | 52% = 42 DPS |
| 1024 | 39% = 16 DPS | 6% = 5 DPS | 24% = 19 DPS |

Aim assist (2 degrees plus 2 more per 1000 units, up to 6) pulls instant-hit shots onto a target near the crosshair, so
real hit rates on a player you are aiming at are higher than this at range.  The plain nailgun has no spread, so it hits
every pellet it aims.

## How much damage it takes to kill with armor

Armor soaks a share of every hit and health takes the rest.  With your absorb values, the raw damage needed to kill someone at 100 health:

| Armor | Holds | Absorbs | Raw damage to kill |
| --- | --- | --- | --- |
| none | - | - | 100 |
| green | 100 | 30% | 143 |
| yellow | 150 | 50% | 200 |
| red | 200 | 70% | 300 |

That is one rocket (100) against an unarmored player, two against yellow armor, and three against red.  One axe swing (240) kills through green and yellow armor, and two are needed against red.
