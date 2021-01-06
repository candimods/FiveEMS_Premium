# FiveEMS Premium beta v1.7b
for Premium Only
This is an Expansive mod meant to bring realisim to EMS Roleplay. 
Thanks to the contributing devs without you this mod would not be possible.
This mod is still in Beta but is in a stage where it can be released to the general public for improvements

To unlock this mod get it here https://store.candimods.com
also check out the Wiki https://github.com/candimods/FiveEMS_Premium/wiki

:new: features in version 1.7b
> 1. :fire: License key is now required, one per server
> 2. menu white list, fix bug where menu opens up in vehicle, improve sync 

to update to newest version remove previous install and install new files. clear your cache of FiveEMS files and restart the resource, resource Folder **Must be Named FiveEMS to work** 

1. new chat commands  /delhaztent and /delbluetent use this to delete the tents!!
2. script will now place the closet ped or a.i on the stretcher, for those who want to RP with the ped or on FivePD servers
Ped placement is buggy this is to be expected if you play lspdfr. working on a fix for this.


# Install 

1. Drag and Drop <b><p color='red'>FiveEMS</p></B> folder fo your resources folder, rename or make sure the folder is named <p color='red'>FiveEMS</p>
<B>FOLDER MUST BE NAMED FiveEMS or it wont work!!!</B>

`
**Install for ESX Servers** remove UI folder and the entries in fxmanifest.lua that refer to the UI, also may need to adjust or add es_extended reference, now load the items.sql and the items can now be pulled from players item inventory and returned. because inventory is mangaged via this system ESX servers dont get an F7 menu only the stretcher menu and Vehicie UI Menu will work for them. Other install issues that may arrise is menu conflict with item inventory, you can comment out these sections in the config.lua`

2. edit the config.lua and add perms/keys
3. add ``` ensure FiveEMS``` to your server.cfg
Please remove any previous versions of this script
4. Press ```F7``` to open menu, edit controls in config.lua 
5. walk up to any compatible vehicle or stretcher to get a menu display option.
 enjoy! 

follow for updates!!!
for support and compatible ambulances and stretchers please visit https://discord.io/candimods

# Config.lua 
Set up your config, input your license key, whitelist ids, and set wheather you want to use perms or set the script to public use.
```lua
Config              = {}
Config.Key = 'XXXXXX' -- enter the key given you by staff

Config.WhiteListOnly = {
  ['Spawn_Stretcher'] = true, -- Can anyone spawn a stretcher or only the whitelisted players ?
  ['Take_Bed'] = true,
  ['Do_Action'] = true,
}

Config.WhiteList     = {
  ['ip:127.0.0.1'] = true,
  ['licence:123']  = true,
  ['xbl:123']      = true,
  ['live:123']     = true,
  ['discord:123'] = true, 
  ['steam:123']    = true,
--- This area is for staff id enter whatever id you want you van get this from txadmin
```
# Five EMS Menu
F7 Menu, change keys and add more stretchers and vehicles in the config.lua.
will spawn compatibile stretchers, you can also change menu location on your screen and the design.
and Hazmat Tent setup, be sure to setup on a flat ground or surface. 

```xml
  -- {hash = `name of vehicle`, item = 'es_extend item name', remove = how many item to remove on use},
  {hash = `Stretcher`,          type = 'veh',  item = 'stretcher',  remove = 1}, -- When using the stretcher  item, it will spawn a Stretcher vehicle and remove 1x item
  {hash = `stryker_M1`,         type = 'veh',  item = 'stretcher2', remove = 1},
  {hash = `stryker_M1_coroner`, type = 'veh',  item = 'stretcher3', remove = 1},
  {hash = `prop_ld_binbag_01`,  type = 'prop', item = 'stretcher4', remove = 1}, <--hazmat tent-->  -- When using the stretcher  item, it will spawn a prop_ld_binbag_01 prop and remove 1x item
  {hash = `mxpro`,			    type = 'veh',  item = 'stretcher5', remove = 1},
  {hash = `stretcher_basket`,	type = 'veh',  item = 'stretcher5', remove = 1},
  ```
if you follow the above convention you can add more props to this menu and restrict it 
to ems only.  

everytime you  spawn a new onject the script will remove the last closet object
as a result any iteams you have equiped may fold back into your  inventory

# Stretcher Menu
Allows you to toggle on/off extras on the stretcher it is setup for the main stretcher, with the following menu options 
To return items to your inventory select FOLD BED in the menu, this will return any close objects to your inventory
` Walking up to a compaitble stretchers displays the following UI options`

1. Longboard
2. Scoop Stretcher 
3. EKG Monitor 
4. IV Pole
5. Lucas3
6. Scoop
7. Lay flat
8. Lay still
9. sit on left side
10. sit on right side
11. CPR convulsions  animation
12. Get out of bed
13. Fold Bed 

# Vehicle UI
` Walking up to a compaitble vehicles displays the following HUD options`

1. toggle compartment doors open/close and scene lights
2. extend poweload
3. stow stretcher
4. opwn/close rear doors 

transport players to the hospital for authenthic roleplay.  

edit the controls in the config.lua

Old version requires warmenu, this version does not

# ESX inventory management 
compaibility was added by contributing dev
more stretchers and prop spawining ability added, Only works in ESX

For ESX Server you must remove the UI folder edit the FxManifest.lua to reflect this, 
as adding items.sql to your database will allow players to pull these new EMS items 
from there inventory and return it. 

This mod is othercompatible with all other server bases and is a standalone script otherwise not
dependent on using the inventory management system. 

ESX Features Preview
https://youtu.be/lNZhb-iV0ak

# Included Stretchers:
`abiility to have more than one compatible stretcher`

1. Stryker M1 Stretcher 
2. Stryker M1 Coroner Stretcher :new:
3. Ferno Stretcher - crashes :broken_heart:
4. Ferno Coroner Stretcher - crashes :broken_heart:
5. Coronavirus Stretcher 
6. Rugged MX Pro Stretcher - buggy 
7. Basket Stretcher :new:

# Props Spawning
1. Hazmat Tent Set up -  prop_ld_binbag_01
WIP looks like this https://www.youtube.com/watch?v=gHTuxDsa438
2. Blue small tent for smaller operations
3. For Medical Props use Dp emotees download here 
https://forum.cfx.re/t/dpemotes-1-7-390-emotes-walkingstyles-keybinding-dances-expressions-and-shared-emotes/843105/111

https://forum.cfx.re/t/dpemotes-1-7-390-emotes-walkingstyles-keybinding-dances-expressions-and-shared-emotes/843105/111

# Using DpEmotes 
to spawn EKG Monitor, Medical bags

Press U to pass out Animation 
`/e backpack - puts on lucas backpack
/e breif3 - EKG Monitor in right hand
/e suitcase - Medical bag in right hand

only have one animation per player at a time. player can carry the stretcher with the medical bags on back.`

# Compatible vehicles:
Check out the wiki page for more information on how to make your mod compatible
https://github.com/candimods/stretchermod/wiki

1. 2020 Rambulance
2. 2020 Ford F450 Ambulance
3. EMS John Deer Gator & Trailer *
4. E450 Ambulance
5. https://www.lcpdfr.com/downloads/gta5mods/vehiclemodels/26170-2015-2016-ford-f450-superduty-single-cab-ambulance-als-11/
-  more compaibility to be added later

Helo Pictured in Screenshots is made by medic909 get it here ==>> https://discord.gg/FqXmby86Fy

# EMS Gator and CoTrailer
1. Please use a comparable script to attach the gator to the trailer, or it will fly offf when you drive away
Here is an example https://forum.cfx.re/t/release-c-vehicle-attachment-and-tow-resource/1808658

# Custom EUP Clothing
FiveEMS EUP Clothing by Novo get it here https://discord.gg/cGGnRpw




# CandiMods Terms and Conditions 
OPEN FOR COLLABOARTION WITH OTHER VEHICLE AND SCRIPT DEVS, ONLY A GOOD TEAM CAN GET THIS MOD FINISHED.
SUBMIT A PULL REQUEST OR ISSUE TO GET COLLAB.

Candi Mods Terms and Conditions For Public Mods >> you may use my models in fivem or SP, 
you are NOT allowed to rip, re upload, redistribute, or repackage this modification. you
are not allowed to upload this file and claim it as your own on any site, server, local, 
drives, cloud drives, or otherwise.  you are NOT allowed to UNLOCK the vehicles files. texture 
devs may link to public downloads only. Exceptions apply to script developers who use 
EMS Medical Props mods as part of there Script. Note you may not receive updates. 
its good to just link to the original download. Please credit the authors of this mod 
where appropriate on your website, blog, or download. 

FiveEMS Terms and Conditions    Do not share the drive links they are unique to you  , you may use the FiveEMS Premium and Legacy versions in 5M, on your server or  you are a trusted member of a server ad wish to share or donte the file, you are responsible for the files. You may not resale, they may not resale, you may collaborate in this discord only. You may use on your stream and take screenshot and video showcases, link to my server here, you are not allowed to upload this file and claim it as your own on any site, server, local, drives, cloud drives, or otherwise.
Every owner must have @FiveEMS Premium User tag for Premium Version or @FiveEMS User tag for Legacy Version  to utilize this mod, its your license, removal of the tag or leaving the server suspends your access to this pack.  if you need help  post in the channels below for assistance.   DO NOT LEAK OR SHARE YOUR FILES WITH ANYONE CONTACT AN ADMIN IF YOU NEED HELP OF HAVE ANY QUESTIONS For help #support or #🚒-safd-general.  Users of the legacy free edition must abide by the same rules.  [ex. you can only get support or help from someone with the same tags as you. ]


You are not allowed to upload this file and claim it as your own on any site, server, local, drives, cloud drives, or otherwise.  you are NOT allowed to UNLOCK this file. texture devs may link to public downloads only
