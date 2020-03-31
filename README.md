# onset-tanks

#### Tanks
* [Sherman](https://sketchfab.com/3d-models/sherman-00ec6397c1634430a828c22101abfad5) by [Daniel Campos](https://sketchfab.com/danielpinhocampos)
* [Tank](https://sketchfab.com/3d-models/tank-a16de8a3c888482e9c49ccf8cb9896e1) by [J_](https://sketchfab.com/moha1)
* [Panzer IV](https://sketchfab.com/3d-models/panzer-iv-medium-tank-toshueyi-14c74d148326448c8edb5fee81be3894) by [Shue-Yi To](https://sketchfab.com/Toshueyi)
* [M1 Abrams](https://sketchfab.com/3d-models/m1-abrams-2577a4eccbc74b2da6dba5bfd09b7511) by [Artem Goyko](https://sketchfab.com/Artem.Goyko)
* [Т-34](https://sketchfab.com/3d-models/-34-8782ae511c5d40d087c520d5a150e427) by [Petr Vorobey](https://sketchfab.com/vorobey.petr)
* [Tank T-10M](https://sketchfab.com/3d-models/tank-t-10m-9aeda33a945c42f0bdebe3d1ef91da06) by [yanix](https://sketchfab.com/yanix)
* [Tiger I](https://sketchfab.com/3d-models/tiger-i-pzkpfw-vi-ausf-e-5dde7ae017584613a823784f744935fc) by [M1RON](https://sketchfab.com/M1RON)
* Ayanokōji#0413 splited the models into 3 parts : cannon, turret and base
#### Commands
* /stank (id) to spawn a tank
#### Developers
* The onset-tanks package need to be loaded BEFORE your package if you want to use onset-tanks functions
* Objects 43 to 64 are replaced by default
* To check if the vehicle is a tank :
```
   --server,client
   if GetVehiclePropertyValue(vehicleid, "istank") then
      -- code
   end
```
* Get tank id
```
   --server,client
   GetVehiclePropertyValue(vehicle, "tankid")
```
* Get turret , cannon and base models of a tank
```
   --server,client
   local turret = GetVehiclePropertyValue(vehicle, "tourelleobj")
   local cannon = GetVehiclePropertyValue(vehicle, "canonobj")
   local base = GetVehiclePropertyValue(vehicle, "baseobj")
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
* Some cannons flying when rotating on the pitch axis
* Bad collisions