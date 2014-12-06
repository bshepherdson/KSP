﻿--------------------------------------------
SyncFlameouts addin for Kerbal Space Program
--------------------------------------------
KSP Version: 0.25
by Robert Hofhauser aka LordFjord

Forum thread: http://forum.kerbalspaceprogram.com/threads/100782-0-25-WIP-Synced-Jet-Flameouts-0-2

This mod reorders the intakes and jet engines of a craft loaded in the SPH in a way that jet flameouts are (almost) syncronized, hence a deadly spin when exiting the athmosphere is a lot less likely.
In case of multiple jet engines, it allows them to run at higher altitudes befor any of them suffers a flame-out.
To understand this in detail: please read http://forum.kerbalspaceprogram.com/threads/64362-Fuel-Flow-Rules-%280-24-2%29 
How this works:
It takes all intakes and jets from the craft and adds them again in a specified order. It does not alter links between parts, parts or any other game behaviour at all. It saves you the hassle to build your SSTOs in a specific way to prevent early jet flameouts.
Now you can just build ahead in any order, press the magic keys and your jets will flame out synced. More or less at least.
If the numbers of intakes and their intake areas simply do not match up, the mod will try to do its best to still assign the intakes to the engines as equally as possible. This makes the vessel still perform better than doing nothing regarding this matter.

Usage:
in the SPH with a loaded craft, press alt-F
A message will display what intakes are assigned to what engines, and the sum of the area intakes for this engine

A few rules, otherwise the mod won't do anything:
- number of intakes > 0
- number of airbreather engines > 0

Warnings and stuff:
If for any reason, the mod messes up your vessel or does not work as expected, please send me a copy of your ksp.log (in your KSP directory) and the vessel's craft file that it messed up. Have I mentioned to backup your craft files often?

Thanks and stuff:
- Kashua for finding out this stuff and (beside many others) teaching me how to SSTO
- MachXXV for taking his awesome mod Editor Extensions as a template to get me started. Sorry dude, you got selected by random ;) And this mod could easily be integrated in Editor Extensions. The code to display a message in the editor is also from you.
- Squad for making KSP

version history:
0.3 (2014.11.26)
----------------
New algorithm based on distributing intakes based on their intake area. Biggest intakes are distributed first, smaller ones after this. The engine with the least amount of assigned intakearea will get the next intake assigned.
A message will be displayed after hitting alt-F showing what the mod did. Either nothing (no intakes or airbreather engine) or a list of assigned intakes to engines with the total intake area assigned to the engine.
I find that this algorithm works very well. I would like to have more feedback on this from YOU :)

0.2 (2014.11.22)
----------------
Improved intake detection via resources, improved engine detection via propellant (intakeair + liquidfuel required).
Intakes are now assigned by type. Algorithm works best with matching intakes per type to engines, for example 4 shock cores, 2 radial intakes for 2 RAPIERS.

0.1 (2014.11.21)
----------------
Proof of concept, only shock cone intakes and turbojet engines are handled, don't try with RAPIER or basic jets (will come soon, don't worry)



License
-------
https://en.wikipedia.org/wiki/Beerware
/*
 * ----------------------------------------------------------------------------
 * "THE BEER-WARE LICENSE" (Revision 42):
 * <lordfjord78@hotmail.com> wrote this file.  As long as you retain this notice you
 * can do whatever you want with this stuff. If we meet some day, and you think
 * this stuff is worth it, you can buy me a beer in return.   Robert Hofhauser
 * ----------------------------------------------------------------------------
 */