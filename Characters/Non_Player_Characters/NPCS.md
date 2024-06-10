---
cssclasses:
  - wide-page
---
## All NPCs
```dataview 
TABLE WITHOUT ID 
	file.link as " ", 
	Location as "##### Current Location", 
	map(filter(file.etags, (x) => contains(x,"#Org") OR contains(x,"#Country")), (x) => regexreplace(split(x, "/")[1],"-"," ")) as Allegiance, 
	regexreplace(regexreplace(Race, ".*\/([^\/]+)$", "$1"),"-"," ")  as Race 
FLATTEN 
	regexreplace(regexreplace(file.folder, "Characters\/Non_Player_Characters\/", ""), "\/", " → ") as Location
FLATTEN 
	filter(file.etags, (x) => contains(x,"#Race")) as Race
WHERE 
	contains(file.folder, "Non_Player_Characters") AND this.file.folder != file.folder
SORT 
	Location
```
