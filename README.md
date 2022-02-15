<img src="https://img.shields.io/github/issues/50North4West/MSFS-G36-Improvement-Mod?style=for-the-badge" /> <img src="https://img.shields.io/github/forks/50North4West/MSFS-G36-Improvement-Mod?style=for-the-badge" /> <img src="https://img.shields.io/github/stars/50North4West/MSFS-G36-Improvement-Mod?style=for-the-badge" /> <img src="https://img.shields.io/github/license/50North4West/MSFS-G36-Improvement-Mod?style=for-the-badge" />

# MSFS G36 Project version 0.6.7

<img src="https://simulated.flights/public/Git/G36GitReadmeBannerImg.jpg" />

This is the improvement project for the MSFS default G36. It all started as a simple edit of some configuration files but it has since grown into a fully-fledged modification that improves all aspects of the default G36 and introduces new features. This was made possible with the help of the community consisting of both enthusiasts and G36 pilots (for a list of contributors, see the end of this readme).

<img src="https://img.shields.io/discord/860496910367326228?style=for-the-badge" /> <a target="_blank" href="https://forums.flightsimulator.com/t/g36-improvement-project/216094/2198"><img src="https://img.shields.io/badge/Discuss-MSFS%20Forum-blue?style=for-the-badge"  /></a>


## Installation:

1: Download and install the Working Title NXi from the store Marketplace

2: Download and unzip the folder ‘bonanza-g36-improvement-project’ in to your MSFS Community folder

3: The Bonanza G36 Improvement Project is now listed as it's own aircraft in the menu rather than overwriting the default aircraft (please see livery note)

PLEASE NOTE - WE HAVE REMOVED THE 'Z' FROM THE FOLDER NAME, ENSURE YOU REMOVE THE OLD VERSION PRIOR TO USING THIS ONE!!


## Current version: 0.6.7

**Changelog**
* Added functionality to Hangar Module (we now save engine hours, miles flown, and count down to annual and 100hr service per livery) state saving items are shown on the State page (menu link at top)
* Fixed missing altitude alert tone @200ft to go
* Tweaked fuel flow as current flow slightly less than book figures (Rpt by @JayDee6281)
* Fixed missing decimal point to manifold pressure gauge
* Added SU8 Prop Modelling - initial tests show aircraft now at most 1knt and 0.2gph away from book figures

**Liveries**
We have split out the files from modifying the default Bonanza to becoming its own aircraft. This is so we can complete further 3d model changes, and work on the hangar module and deeper systems modelling. Liveries will need to be amended to reflect this new aircraft to work. More information here https://forums.flightsimulator.com/t/g36-improvement-project/216094/1943

**RoadMap**
I though you might like to see the plans I have regarding further development of the mod. None of these are set in stone or confirmed as definitely happening, just things I'd like to try and accomplish. Fee free to add what you'd like to see with the mod in our discord roadmap channel https://discord.gg/JVPMYdKx86
1. Aircraft Persistence (80% Complete)
2. Spark Plug Fouling (In test / tweaking)
3. Hangar Module further development (In progress)
4. Modelling of MP reduction when systems using power to simulate engine efficiencies e.g. alternator load, air-conditioning, spark plug fouling, mixture etc. (Pondering)
5. Oil Simulation (investigating)
6. Electrical System deeper simulation (not started, see this post https://forums.flightsimulator.com/t/understanding-what-systems-the-sim-simulates/488250)
7. Wear and tear on aircraft hardware, e.g. flaps/ailerons etc. (not started)
8. Further Aircraft failures (Investigating)


## Features:

**Bonanza Hangar**
* A custom in game panel where you will manage your aircraft. This is a work in progress feature but aims to replicate some of the features found in the A2A aircraft hangar. This is still very much a WIP feature and will evolve over time.

**Flight dynamics/performance**
* Adjusted climb and cruise performance to match the Bonanza G36 POH charts.
* Adjusted flap and gear drag
* Slightly reduced pitch effect due to elevator deflection + propwash
* Slightly increased nosewheel steering angle
* Added drag due to cowl flaps. This causes a 3-4 kts cruise speed loss.
* Decreased yaw sensitivity by lowering deflection rate as a function of speed
* Increased overall stability: less 'twitchy' feeling

**Engine & Fuel system**
* Completely overhauled engine parameters: realistic fuel flow, mixture-EGT interaction, engine performance at all pressure altitudes. After more than 30hrs of testing and tweaking, the engine performance figures match the POH as close as we can get them and have been verified by real Bonanza pilots. TAS is within 0.22kts on average across the altitude spectrum and fuel flow within 1g/h.
* Simulation of Spark Plugs / Spark Plug Fouling - if you don't lean correctly both on the ground or in the air your plugs will encounter spark fouling, loosing RPM and engine power. Each spark is modelled independently and has its own likelihood to foul; this stays across flights, the spark most likely to foul will foul first followed by the next etc.
* Simulation of the electric fuel pump
* More advanced simulation of engine start-up:
  - Cold starts: correct use of the fuel pump, throttle and mixture required depending on engine and ambient temperature
  - Under some conditions, idling the engine too soon after start may cause it to quit.
  - Flooded engine: pumping too much fuel to the engine may cause it to ignite slower or not at all.
  - Flooded engine start procedure (mixture low/cut, throttle halfway) may resolve this.
  - A hot engine running idle with little airflow may quit because the fuel evaporates.

**Systems**
* Added new working systems and switches:
  - Airco (has a negative effect on engine performance, you will see a few kts lower cruise speed)
  - Airco and ventilator switches are functioning and part of the electrical system
  - Annunciator test
* Electrical system overhaul:
  - Completely revised electrical buses: all individual systems hooked up to the correct bus
  - Bus tie logic added
  - Correct voltage indications of BUS2 due to reverse current blocking diodes
  - Correct alternator loads
  - Made all indications smooth, rather than instant jumps to a new value
* Autopilot tweaks
  - Fixed holding the wrong altitude at non-standard atmospheric pressures
  - Max pitch and bank angles adjusted for smoother AP behaviour
  - Added maximum and minimum IAS_ref speeds for FLC mode
  - Adjusted autopilot PIDs
* Integration with the Working Title NXi mod, with customized ENGINE, LEAN and SYSTEM pages.
* Completely redone G1000 annunciators: all annunciators of the real G36 were implemented (except for door open warnings)
* Corrected fuel gauge scale
* Changed environmental controls to read C° rather than F°

**Textures & effects**
* Including the latest version of Uwajimaya's lighting mod (https://uwajimaya.github.io/FS2020/)
* Corrected decals (e.g. shoulder hardness -> harness)
* Custom Livery provided by @Crispy136 (Thank you!) You can find more of his liveries here https://flightsim.to/profile/Crispy136/uploads
* Integrated @BufordTX's VR Friendly Prop Mod

**Checklists**
* Interactive checklists for every stage of your flight that follow the POH

**ATC**
* You are now referenced as Bonanza > Your Callsign in the game ATC

**SOUNDS**
* Excessive undercarriage wind noise reduced
* Added TAWS system test message

**AIRCRAFT PERSISTENCE / STATE SAVING / MAKING THE PLANE 'REAL' (WORK IN PROGRESS)**
* Your aircraft now remembers how you left it!
* States are saved for each aircraft livery, so you can multiple 'living' Aircraft
* On first flight load of the new 0.6.6, your aircraft is set cold & dark with 64 gallons of fuel.
* The aircraft now saves the following tank levels, switches and levers every 5 seconds.
    * Left & Right Fuel Tank Level
    * Battery 1 & 2 switch
    * Alternator 1 & 2 Switch
    * Parking Brake lever
    * Avionics Switch
    * Airconditioning Switch
    * Blower switch
    * Vent Blower switch
    * Aux Fuel Pump Switch
    * Magneto Switch
    * Pitot Heat Switch
    * Prop De-Ice Switch
    * Strobe Switch
    * Beacon Switch
    * Nav Light Switch
    * Flood Light Switch
    * Panel Light Switch
    * Taxi Light Switch
    * Landing Light Switch
    * Fuel Selector Position
    * Defrost switch
    * Throttle Position
    * Propeller Position
    * Mixture Position
    * Cowl Flap Position
    * Flaps Switch
    * Flaps Physical Position
    * Pitch Trim Position
    * Aileron Trim Position
    * Floodlight Brightness
    * Pilot & Passenger Yoke Visibility

* When you next climb into your aircraft you will find it just as you left it!

NOTE: The aircraft state is only loaded if:
* You are on the ground in a parking spot or
* You are on the ground somewhere else and your engine is off.

This allows the aircraft to load in flight or ready at the end of the runway without messing with the aircraft load. It WILL however, still record switch states and tank levels etc.


## FAQ's:

**Q: I am not seeing the engine pages in the G1000?**

*A: Make sure to install the Working Title NXi (from the Marketplace). Ensure that the old G1000 Working Title mod is no longer installed, we have moved compatabilty to the NXi available from the marketplace.

Please Note: Current version of Working Title NXi 0.7.1 does not have a working reversionary mode and the engine pages are listed on the MFD only. We believe this will change in the future.

There have also been reports of the GNS750 causing issues with the NXi / Our mod.

**Q: The mod isn't working?**

*A: This is usually due to a conflict with another mod in the community folder. The best thing is to remove all other mods and slowly add them to see what causes the conflict. Aircraft, gauge and lighting mods are the prime suspects.*

**Q: The engine won't start?**

*A: Since v0.6, the engine start is modelled. Fuel must be pumped to the engines, cold engines need to warm up and overuse of the fuel pump and throttle prior to engine start may cause it to flood.  If you correctly follow the start procedures, the engine should almost always start on the first try, unless under extreme condtions.*

**Q: My engine quits after landing?**

*A: Fuel may evaporate in a hot engine at low speeds and idle throttle. This could occur on a very hot day when coming to a stop after landing. Use of the cowl flaps on approach and landing is advised under these conditions.*

**Q: My engine quits right away when starting on the runway?**

*A: This mod is designed for cold and dark starts. The sim initializes the CHT as equal to the ambient temperature. Furthermore, the amount of fuel pumped to the engine initializes as 0. Hence, the engine start/run conditions are not met and the engine will shut down. Follow the start-up procedure to restart the engine.*

**Q: The annunciator test button is stuck?**

*A: This happens when you left click outside the clickbox and then hover your mouse over the button and release. Do the same thing to resolve the problem.*

**Q: The AC Blower switch doesn't work?**

*A: Unfortunately there is something wrong with the animation. We have to wait for Asobo to fix this, but since this button was (inop.) by default don't hold your breath. If you click it, it does actually work. You can see it increases the electrical BUS1 load slightly.*


Our contributors (by their MSFS Forum name)
FrettFS, CaptMatto, Coppersens, Uwajimaya, dciskey, Matchrocket, JuiceBox7535, jonasbeaver, Exp232, nickc95, GuiFarias31 and MrTommymxr. Special thanks to the Working Title team for their excellent NXi implementation!
