# Server Scenarios 🚶‍♂️

---------------------
---------------------

A FiveM resource by TayMcKenzieNZ allowing custom and modified scenarios to work in your servers.

I have modified and provided the following, as they would spawn peds on the street clapping, cheering, taking photos and other strange anomalies, feel free to modify them if your MLO or whatever is in these areas:

* alamo_sea

* bolingbroke_penitentiary

* cypress_flats

* del_perro_beach

* del_perro_carpark

* del_perro_shops

* downtown

* east_vinewood

* facility_main (Player online doomsday facility, requires bob74_ipl to be configured)

* farmers_market

* lsia_terminal

* pacific_bluffs

* race_course (Diamond Casino & Resort)

* sandy_shores (Police station scenarios and more)

* senora_hills

* south_los_santos

* stablescustom (Tay's own personal scenario, replacing Madrazo's Ranch scenarios)

* vespucci

* vespucci_beach

* vespucci_beach_north

* vespucci_beach_south

* vespucci_police_dept

* vinewood


----------

Stables scenario to work alongside https://github.com/TayMcKenzieNZ/Ranch-De-Caniche and https://github.com/TayMcKenzieNZ/fivem-scenarios

----------

# This resource requires **gamebuild 2189 (Cayo Perico) or higher**, as the sp_manifest was taken from the **latest gamebuild.**

If you find any bugs, try noclipping or teleporting elsewhere, then coming back.

You can join the codewalker discord and grab the latest codewalker version to modify and / or add custom scenarios.

You may be able to run this resource on older gamebuilds by simply removing the following from `sp_manifest.ymt` as this is the scenarioss related to Cayo Perico;



----------

You may find triathlon related scenarios lurking in the following locations, I am yet to be able to delete/disable them all completely, however if you somehow manage to, feel free to send me a pull request. The scenario files are as followed:

* alamo_sea

* del_perro_beach

* del_perro_carpark

* pacific_bluffs

* sandy_shores

* senora_hill

* vespucci

* vespucci_beach_north

* vespucci_beach_south

* vespucci_police_dept

* vinewood

----------


This is by all means a "work in progress" release, and is a test of my abilities streaming and overriding scenarios in FiveM.

If you would like to addon to this resource and modify existing scenarios in the world, open the `sp_manifest.ymt` file and rename the scenario to

`<Name>compcache:/server_scenarios/xxxxxxx</Name>` If you rename the resource, you will need to rename `server_scenarios`

For example, `<Name>compcache:/nopixel_scenarios/downtown</Name>`.

----------

# Installation ⚙️:


The resource and the scenarios must be in lowercase and must match what is written in the sp_manifest file.

* Download the resource and rename the folder to server_scenarios.

* Add `start server_scenarios` to your server.cfg

Again, if you rename the resource, you must change the file paths in the sp_manifest as stated above.

----------

I have personally tested the following scenarios alongside this repository, and can confirm that they are working in FiveM after renaming them in the sp_manifest:

https://www.gta5-mods.com/scripts/scenario-groups


-----------

# FAQ:

**How can I tell if this is working?**

- Visit Madrazo's Ranch and you should see that there are deer, pigs, chickens, cows and Poodles. If you don't see them, try noclipping or teleporting somewhere else, set time to midday and come back.
You can then rename `stablescustom` back to `stables` and revert it back to:

```lua
   <Name>platform:/levels/gta5/scenario/stables</Name>
```

You will then need to delete `events.meta`, `relationships.dat`, and remove the following from `fxmanifest.lua`

```lua
files {
	'events.meta',
	'relationships.dat'
}

data_file 'FIVEM_LOVES_YOU_4B38E96CC036038F' 'events.meta'
```

---------------------
---------------------

**When I go to a (certain area) my game crashes?**

- The scenario file may be corrupt or you've done something to it ie deleting chains or path nodes. 
If you wish to delete or modify chains, try `CW 26 dev 7` (available from codewalker discord) as this seems to work for editing chains and deleting them without running into crashes.

-----------------
---------------------

**Please make this work with XXXX DLC!**

- You can simply search for new scenario entries in your own copy of sp_manifest using OpenIV or Codewalker's RPF explorer and copying those entries to the sp_manifest file which I have provided.
However, if you are trying to run this on DLC older than Cayo Perico, try removing the following entry from the `sp_manifest.ymt` file, as this is responsible for Cayo Perico scenarios that your DLC doesn't have, which will cause crashes and issues:

```lua
 <Item type="CScenarioPointRegionDef">
   <Name>platform:/levels/gta5/scenario/island_drug_fields</Name>
  <AABB>
    <min x="4357.971" y="-5667.243" z="0.442734" />
    <max x="5484.739" y="-4338.396" z="67.04505" />
   </AABB>
  </Item>
```

