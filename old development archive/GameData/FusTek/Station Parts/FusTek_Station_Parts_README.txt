FusTek Station Parts - Mod Parts Pack

Version:	X0.04-4 DEV BUILD	(KSP 0.23.5)

Author: 	Robin "sumghai" Chang	techadv@alphacompanyforums.com

Derived from:	FusTek Station Parts by Alex "fusty" Sterling	

License:	Creative Commons Attribution-ShareAlike 4.0 Unported (CC BY-SA 4.0)
		http://www.creativecommons.org/licenses/by-sa/4.0/

Disclaimer:	This is an alpha parts pack for an alpha game - Use at own risk. 
		If your computer blows up, it's not my (or fusty's) problem.



===Dependencies===

 - Connected Living Spaces (CLS) plugin (codepoet), for determining which compartments are habitable/traversable

 - Firespitter plugin v6.4 pre-release (Snjo), for various tweakable part animations and texture switching
 
 - Modular Fuel Tanks, for reconfigurable propellant tank in the Resupply module

 - ModuleManager plugin (sarbian), for applying patches for functionality/features provided by dependencies and third-party add-ons

 - Ship Manifest plugin (Papa_joe), for transferring crew between non-airlock compartments without EVA
 
 
===Supported Third-Party Addons===

 - Deadly Re-entry Continued (Station parts will burn up during atmospheric re-entry if not shielded properly)
 
 - TAC Life Support (Station parts will provide varying life support provision storage / resource processing capabilities)



===How To Install===

1. Ensure that you have all of the aforementioned dependencies installed

2. Remove any previous version of the FusTek Station Parts add-on

3. Download

4. Extract the .ZIP archive and copy the GameData folder provided into your KSP root directory

The parts should then be located under the FusTek/Station Parts folder



===Usage===

 - Most of the provided parts are crew-habitable modules that can be used for building space stations or planetary outposts, and come in both flat 2.5m and tapered 1.25m variants.

 - Karmony Utilities Modules are essentially the "core" module of your space station or planetary outpost, and can be operated with or without Kerbal crew

 - The FusTek Resupply module is essentially a large probe core designed to be reconfigured by users for carrying supplies to and from stations. For best results, use with the SDHI Service Module System (also by sumghai)

 - Only the Kuest Airlock and Kuest Legacy Airlock permit EVA. Movement between other modules requires both the Ship Manifest and Connected Living Spaces (CLS) plugins

 - Structual end rings included in the pack can transform a flat 2.5m module into its tapered 1.25m version, or allow two or more modules of different types to be combined together as one monolithic "extra-length" module.

 - Bulkheads converts any 2.5m fuselage or fuel tank into ones that match the FusTek aesthetic, and are also compatible with the end rings

 - Special docking ports (IACBMs) come with built-in lights and animated guidance fins (cosmetic, non-functional)



===Uninstallation Instructions===

Remove the FusTek folder and all its contents from the GameData folder.

If you have other FusTek part packs you wish to keep, just remove the Station Parts subfolder.



===Release Notes===
X0.04-4 DEV BUILD  5 May 2014
---------------------------
Features:
 - New Parts
    - Karmony Payload Bay Module
    - Karmony Payload Bay Module Adapter
 - The Payload Bays are genericized variants of the Warehouse module that will be designed without the rotating payload rack magazine
 - Deadly Re-entry Continued support added
	- All FusTek parts will burn up during atmospheric re-entry (specifically, above 800°C)
	- If you're planning on building surface bases on Duna and Laythe, be sure to install heat shields properly
	- A Module Manager config, FusTek_MMPatch_DeadlyReentry.cfg, can be found under GameData\FusTek\Station Parts\Parts\MM_configs, and is used to define maximum heat tolerances for all FusTek parts
 - TAC Life Support integration finalized
	- Each module will have varying amounts of crew provision / waste storage tanks and resource processing capabilities, depending on their intended purpose
	- A Module Manager config, FusTek_MMPatch_TACLifeSupport_ModularFuelTanks.cfg, can be found under GameData\FusTek\Station Parts\Parts\MM_configs, and is used to define life support resource quantities for each FusTek part
 - The FusTek Resupply Module is now pre-configured to carry both life support crew provisions and various types of spacecraft fuel for resupplying space stations / planetary outposts
	- Crew provision quantities can be altered using the stock KSP tweakables system
	- Varying combinations of LiquidFuel/Oxidizer/Monopropellant/Xenon can be filled using Modular Fuel Tanks, up to a maximum total mass of 800 kg
	
Changes:
 - Crew habitable modules now have unique IVAs
	- At present, they are only used to test layouts and crew seating positions
 - Karmony Utilities Modules can now hold up to 500 units of ElectricCharge
 - Some Karmony module viewports have been repositioned to match up with the WIP internals
 - Kirs Docking Module hatches have been resized to match up with the WIP internals
 - Inner bay textures for Karmony Warehouse and Payload Modules finalized
 
Fixes:
 - Kuest / Kuest Legacy Airlocks will now store science reports acquired from EVA
 - Alternative texture switching now supports multiple objects with the same name on the same part
	- This requires the experimental v6.4 pre-release of the Firespitter plugin
	
Issues:
 - IVAs are still a work in progress
    - Models and textures are placeholders
	- RasterPropMonitors are not yet implemented
 - KSO Phase II Alternative Textures have not been updated to coincide with changes / new parts
	- That's Sippyfrog's responsibility, not mine :P
 - Warehouse has incomplete functionality
    - Work will on this will continue in R0.05a


X0.04-3-1 DEV BUILD Hotfix 11 May 2014
---------------------------
Fixes
 - Compatibility patch for Connected Living Spaces 1.0.4.1 update
    - Specifically, adding "passable = true" to the Kuest Airlocks and Kupola


X0.04-3 DEV BUILD  24 April 2014
---------------------------

Features:
 - Modules now (tentatively) support alternative texture packs
    - These can be placed under GameData\FusTek\Station Parts\Parts\AltTexturePacks
    - A Module Manager config, FusTek_MMPatch_TextureSwitch.cfg, can be found under GameData\FusTek\Station Parts\Parts\MM_configs, and is used to define custom texture sets for each FusTek part
    - A sample implementation of Sippyfrog's "KSO Phase II FusTek Retexture" is included for reference
 - Connected Living Space (CLS) integration finalized
    - Parts that can hold crew and are traversable:
        - Karmony Habitation Module
        - Karmony Habitation Module Adapter
        - Karmony Science Module
        - Karmony Science Module Adapter
        - Karmony Utilities Module
        - Karmony Utilities Module Adapter
        - Kirs Docking Module
        - Kuest Airlock 
            - No access via top node, as that is where the external airlock door is located
        - Kuest Legacy Airlock
            - No access via top node, as there is no hatch object there
        - Kupola Observation Module
            - No access via top node, as that is where the main viewport is located
    - Parts that cannot hold crew, but are traversable:
        - IACBM 1.25m
        - IACBM 2.5m
        - Karmony Bulkhead
        - Karmony compactNode Mk III
        - Karmony compactNode Mk III Adapter
        - Karmony End Ring
        - Karmony Node Mk III
        - Karmony Node Mk III Adapter
        - Karmony Logistics Module
        - Karmony Logistics Module Adapter     
    - Parts that are not traversable under any circumstances:
        - Karmony Node Cover
        - Karmony Node Cover - Viewport Variant
        - Karmony Warehouse Modules
        - Karmony Warehouse Modules Adapter
        - FusTek Resupply Module
    - A Module Manager config, FusTek_MMPatch_ConnectedLivingSpaces.cfg, can be found under GameData\FusTek\Station Parts\Parts\MM_configs, and is used to define CLS settings for each FusTek part

Changes:
 - All parts, models and KSP internal names have been changed to ensure compatibility with dependencies such as Firespitter and CLS
    - WARNING: This is a craft-breaking change!

Issues:
 - Alternative texture switching isn't 100% functional, 
     - Firespitter plugin currently cannot update multiple objects sharing the same name
     - Snjo is already aware of this and is working on a fix
 - Warehouse has incomplete textures and functionality
     - Work will on this will continue in R0.05a
 - IVAs are still a work in progress
     - For now, most will borrow stock KSP internals


X0.04-2 DEV BUILD  11 April 2014
---------------------------

Features:
 - New Parts
    - Karmony compactNode Mk III
    - Karmony compactNode Mk III Adapter
    - FusTek Resupply Module
 - The compactNode Mk IIIs are six-way nodes that area approximately half the length of the standard Node Mk IIIs, ideal for crowded station designs
 - The FusTek Resupply Module is essentially a oversized probe core that users can reconfigure to carry whatever resources they need for station resupply

Changes:
 - Compatibility Patch for KSP 0.23.5
 - Removed FusTek_Sumghai.dll plugin
    - This parts pack now has Firespitter.dll as a dependency, which is more regularly updated and supports tweakables
 - Reworked common texture atlases to 4096 x 4096 px
    - The updated UV island maps will now allow non-tiled alternate textures
    - Also removed ENG TEST ARTICLE watermarks
    - Texture switching will be supported in a future release
 - Removed airlock functionality from majority of crew-habitable modules
    - Modules affected:
        - Karmony Node Mk III
        - Karmony Node Mk III Adapter
        - Karmony Logistics Module
        - Karmony Logistics Module Adapter
        - Karmony Habitation Module
        - Karmony Habitation Module Adapter
        - Karmony Science Module
        - Karmony Science Module Adapter
        - Karmony Utilities Module
        - Karmony Utilities Module Adapter
        - Kirs Docking Module
        - Kupola Observation Module
    - Kuest Airlock and Kuest Legacy Airlock will retain said functionality for obvious reasons
 - Shifted part origins of majority of modules back to 0,0,0 and removed CoMoffset hack
    - WARNING: This is a craft-breaking change!
    - Modules affected:
        - Karmony Node Mk III
        - Karmony Node Mk III Adapter
        - Karmony Logistics Module
        - Karmony Logistics Module Adapter
        - Karmony Habitation Module
        - Karmony Habitation Module Adapter
        - Karmony Science Module
        - Karmony Science Module Adapter
        - Karmony Utilities Module
        - Karmony Utilities Module Adapter
 - Removed crew-carrying capacity and IVAs for selected crew-habitable modules
    - Modules affected:
        - Karmony Node Mk III
        - Karmony Node Mk III Adapter
        - Karmony Logistics Module
        - Karmony Logistics Module Adapter
    - These modules are essentially junctions and passegeways, have no seats and are thus not intended for long-term occupation
    - Connected Living Spaces (CLS) API will be supported in a future release
 - Removed RocketParts capacity from Karmony Warehouse Module / Karmony Warehouse Module Adapter
    - Official support for OrbitalConstruction and all forks has been terminated; Users will need to apply their own ModuleManager configs at their own risk
 - IACBM 1.25m / IACBM 2.5m
    - Removed hatch mode toggle as most FusTek modules no longer have airlocks (making the EVA-through capability for docking ports redundant)
    - Tweaked docking collider to mitigate wobbly docking port issue
    - Fixed docking port lights by updating spotlight definitions to Unity 4.3 (no more cyan lights)
 - Custom placeholder IVA added for Kirs Docking Module

Issues:
 - Warehouse has incomplete textures and functionality
     - Further updates depends on KASPAR/FLEXrack being released
 - IVAs are still a work in progress
     - For now, most will borrow stock KSP internals


X0.04-1 DEV BUILD  4 November 2013
---------------------------

Changes
 - Compatibility Patch for KSP 0.22+
 - All parts assigned to the Composites node in the R&D Tech Tree
 - Overhauled and optimized all parts to take advantage of MODEL{} node calls as well as common texture atlases
    - All crewed compartments also now temporarily use stock SQUAD internals
    - Proper FusTek internals will be implemented in X0.04-2 DEV BUILD
 - Renamed Karmony Parts Warehouse Modules to Karmony Warehouse Modules, and revised model
    - Warehouses now come with animated bay doors, toggleable both when directly controlling the vessel and when on EVA
    - These are just placeholders; rotating KASPAR rack functionality will come in future updates


R0.03.5a          2 September 2013
---------------------------

Fixes
 - Tweaked Karmony End Ring attachment points to accomodate new IACBMs
 - Reworked animation toggling behaviour for IACBM 1.25m, IACBM 2.5m and Kupola
     - The IACBM guidance fin rotary positions and Kupola blast shutters are now also toggleable inside the VAB


R0.03.4a          30 August 2013
---------------------------

Features:
 - New Parts
    - IACBM 1.25m
    - IACBM 2.5m
 - The Improved Androgynous Common Berthing Mechanism (IACBM) is a docking port system designed to be directly compatible with FusTek Karmony modules and any generic 1.25m/2.5m diameter fuselages
    - Built-in LED illumninators allow long-distance visual identification / orientation marking of target docking ports
        - LEDS will consume ElectricCahrge and automatically shut down if deprived of power
    - Active/Passive mode toggles rotate guidance fins to appropriate positions for docking
        - Recommendation: The target docking port should be set to Passive, while the docking port on the actively-controlled vessel should be set to Active
    - Hatch mode toggle allows the IACBMs to "unblock" Karmony hatches that are otherwise obstructed, allowing Kerbals to EVA right through them
        - Remember to switch back to Docking mode for docking; weirdness may occur if docking is attempted while in Hatch mode

Changes:
 - Karmony Parts Warehouse Module stats updated to correspond to latest version of OrbitalConstruction Redux (4.2)
    - Dry mass is now 2.5t
    - Maximum RocketParts capacity increased to 1600, in line with RocketParts density reduction.
        - Warehouse preloaded with 100 RocketParts, which can be replenished by supply missions using the OrbitalConstruction Redux mod
    - Total in-flight mass of fully-stocked Warehouse will end up as 6.5t, the same as any other Karmony full-length module
        - The old settings would have resulted in a (ridiculous) 100t warehouse

Issues:
 - IACBM guidances fins don't actually collide
    - This is due to technical limitations of KSP's ModuleDockingNode at the time of writing, which causes terminal docking sequences to ignore part colliders
    - For precise rotational alignment, use in conjunction with Sarbian's MechJeb 2 fork.
 - Transient "Start Deployed" GUI inconsistencies in FusTek_Sumghai.dll animation modules
    - NOT craft or functionality-breaking, just a little annoying


R0.03.3a          8 August 2013
---------------------------

Fixes
 - Corrected typo in CFGs from breakintTorque to breakingTorque
    - All parts have been reviewed by our Quality Assurance (QA) department at great expense and at the last minute


R0.03.2a          2 August 2013
---------------------------

Changes:
 - Compatibility Patch for KSP 0.21+
 - Karmony series modules and Kupola now use SAS and Reaction Wheels
    - No change to monopropellant reserves; future releases will include RCS thrusters built into selected modules
 - Karmony Parts Warehouse Module now uses RocketParts resource, to reflect changes in the OrbitalConstruction Redux mod by its author


R0.03.1a          24 July 2013
---------------------------

Fixes
 - Tweaked CoM of Karmony series modules so that they line up much with the part's geometric centre
    - This should fix the Center-of-Mass balancing issues, especially with MechJeb
    - No change to actual part origins, though


R0.03a          22 July 2013
---------------------------

Features:
 - New Parts
    - Karmony Parts Warehouse Module
    - Karmony Node Cover
    - Karmony Node Cover - Viewport Variant
    - Kirs Docking Module
    - Kuest Legacy Airlock
    - Kupola Observation Module
 - Karmony Parts Warehouse Module is designed for use with the OrbitalConstruction Redux mod, and can store up to 100 units of SpareParts
 - Kirs Docking Module acts as a 1.25m diameter standoff for docking space stations with vessels that are unable to approach closer
 - Kuest Legacy Airlock is functionally equivalent to the standard Kuest Airlock, but is cheaper and lighter, at the expense of not rated for use on planetary surfaces
 - Kupola Observation Modules come with animated blast shutters to protect occupants from space debris. Most of the time.
 - The FusTek_Sumghai.dll plugin, specifically compiled to handle multiple animations per part, is now included in the pack
    - This was developed with the assistance of Snjo, and uses portions of his Firespitter.dll code

Fixes
 - Tweaked rendering and collision meshes
    - This should greatly reduce the "freeze-on-drag" issue some users experience in the VAB and especially in the SPH
    - Model file sizes have consequently been reduced by up to 50%
 - Reverted to using PNG textures, which reduces texture file sizes and memory usage (according to some users)
    - Those responsible for sacking the people who have just been sacked have been sacked
 - Lowered ElectricCharge rate of Utility Modules to 15.0 / min
    - Older value was far too overpowered and had made Solar panels useless
    - Newer value now forces players to add their own solar panels and/or RTGs if more than three other modules are connected in the same structure

Bugs/Known Issues
 - All crew-capable modules currently STILL use either the default generic "UniKarmony" or the stock KSP Cupola internal model
    - Work on module-specific unique internals will begin in the next version (R0.04a)
 - Karmony Parts Warehouse Module will be outfitted with animated cargo bay doors and internal payload magazine rack once nothke finishes making his KASPAR mod


R0.02.1a BUGFIX	19 June 2013
---------------------------

Fixes
 - Resolved exploding hatch issue with all Karmony modules
    - Consequently, part origins / attachment nodes MAY be affected. Backup your persistence/quicksave files and crafts before installing this fix


R0.02a		19 June 2013
---------------------------

Features:
 - New Parts
    - Karmony Habitation Module
    - Karmony Habitation Module Adapter
    - Karmony Science Module
    - Karmony Science Module Adapter
    - Karmony Utilities Module
    - Karmony Utilities Module Adapter
    - Karmony Bulkhead (2.5m cosmetic structural part)
 - Karmony Habitation, Science and Utilities modules come with MechJeb2 support and toggleable window lights
 - Karmony Utilities module come with RemoteTech (RemoteCommand) and Chatterer support, and also has a small RTG for powering small stations / outposts with less than four connected modules (Solar panels will be required for larger structures)
 - Karmony Bulkhead converts any 2.5m fuselage or fuel tank into ones that match the FusTek aesthetic
    - Can also be used in conjunction with the Karmony End Ring

Changes:
 - Cost of Karmony module variants and Kuest Airlock increased to 8500 and 2500 respectively
    - This makes them comparable to the half-sized stock PPD-10 Hitchhiker Storage Container (4000), as Karmony module variants are twice the Hitchhiker's length and (allegedly) use superior construction techniques
 - Monopropellant capacity in the Habitatation, Science, Logistics and Node modules reduced from 180 to 100
    - Original value was considered too overpowered
 - All models now use compressed TGA textures, due to a Unity bug that causes PNG images to load very slowly
    - Those responsible for painting all the modules have been sacked
 - Crew capacities for all modules have been adjusted:
    - Nodes:      2 Kerbals
    - Logistics:  2 Kerbals
    - Habitation: 4 Kerbals
    - Science:    4 Kerbals
    - Utilities:  2 Kerbals
    - Airlock:    1 Kerbal (Unchanged)

Bugs/Known Issues
 - All crew-capable modules currently STILL use the default generic "UniKarmony" internal model
    - Module-specific unique internals will come at a later date
 - Karmony Habitation, Science and Utilities modules may have incorrectly-formatted resource outputs/requirements in the VAB/SPH part description
    - This is due to various KSP internal PartModules not combining nicely in the part description
    - Part functionality is not affected


R0.01a		8 June 2013
---------------------------

Features:
 - Initial release
 - New parts
    - Karmony Node Mk III (4 recessed nodes + 2.5m flat ends)
    - Karmony Node Mk III Adapter (6 recess nodes + 1.25m tapered ends)
    - Karmony Logistics Module
    - Karmony Logistics Module Adapter
    - Karmony End Ring (2.5 to 1.25m cosmetic adapter ring)
    - Kuest Airlock
 - Karmony Nodes and Logistic modules come with MechJeb2 support
 - Kuest Airlock features C-shaped EVA handle loop, which Kerbals can fully traverse around
 - Main difference between fusty's Mk II and this pack's Mk III is the removal of the "emergency hatch" from all modules and redesignating the forward hatches as EVA-able

Bugs/Known Issues
 - All crew-capable modules currently use the default generic "UniKarmony" internal model
    - Module-specific unique internals will come at a later date
 - Stacked modules may block the forward EVA-able hatches
    - This is working as intended; use Kerbal Crew Manifest to transfer crew between modules
    - Occasionally, a Kerbal may break free and cause the modules to explode. This bit is NOT intended and will be fixed to properly obstruct the hatches of modules connected adjacently.
 - Crew capacity, power and monopropellant subject to further adjustment

