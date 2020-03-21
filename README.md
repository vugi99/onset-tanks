# onset-tanks

#### Informations
* Custom Models by Kemro#0182
* there is 2 tanks atm , the first tank is the green tank and the second tank is the desert tank
#### Commands
* /stank (id) to spawn a tank
#### Developers
* The onset-tanks package need to be loaded BEFORE your package if you want to use onset-tanks functions
* Objects 52,53,54,55,56,57 are replaced
* To check if the vehicle is a tank :
```
   --server,client
   if GetVehiclePropertyValue(vehicleid, "istank") == true then
      -- code
   end
```
* Don't forget to import the onset-tanks package before using functions
```
   --server
   local tanks = ImportPackage("edit_me") -- put the onset-tanks package name here
```
* Spawn a tank
```
   --server
   local vehicleid,cannonobject,turretobject,tank_base_object = tanks.SpawnTank(tankid,x,y,z(,yawangle))
```
* transform a vehicle to a tank ( Please use vehicles models 13,14,15,16 for better collisions )
```
   --server
   local cannonobject,turretobject,tank_base_object = tanks.TransformToTank(tankid,vehicleid)
```
#### Known bugs
* bad turret pitch and roll rotation