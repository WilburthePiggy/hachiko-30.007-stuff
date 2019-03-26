# hachiko-30.007-stuff
for me to share the basic stuff that i passed off as a project.

# User.html
What does it do? 
1. You put in your shipping ID (no authentication at this point because idk what I'm doing)
2. It pulls from a firestore database.
3. It returns your shipping details

# hachiko database
Schema for parcel as follows:
document name is *shipping number of parcel*
* parPass -> customer's Password [in this case, we're using a face-id prog by Methyldragon, so it'll be a list of numbers]
* parAdd -> customer's home address
* parPup -> customer's assigned pickup point, where the hachiko will wait for them
* parMod -> associated hachiko model = hachiko.hachiMod
* parPer -> customer's assigned collection period = hachiko.hachiPer
* parLoc -> parcel's current location = hachiko.hachiLoc
* parStat -> hachiko status = hachiko.hachiStat
* parHachi ->id of hachiko
  

Schema for hachiko as follows:
document name is *hachiko id* this is referenced in the parHachi

* hachiLoc -> location of parcel 
* hachiParX -> document name of the parcel X
* hachiPer -> period of hachiko assigned
* hachiMod -> model of hachiko, because we have dreams too yeah?
* hachiStat -> status of hachiko
