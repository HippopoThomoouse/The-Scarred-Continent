# Cities
```dataview 
TABLE Population
FROM #City
WHERE contains(file.folder, "Places/The Crossing")
SORT Population DESC
```
# Bridges
```dataview
TABLE 
FROM #Fortress
WHERE contains(file.folder, "Places/The Crossing")
SORT Population DESC
```
# Members
```dataview 
TABLE 
	CountryRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Country/Realm-of-the-Crossing
WHERE 
	contains(file.folder, "Non_Player_Characters") OR contains(file.folder, "Player_Controlled_Characters")
SORT 
	choice(Role = "Captiain", "1", 
	choice(Role = "President", "2", 
	choice(Role = "Counciler", "3", 
	choice(Role = "General", "4", 
	choice(Role = "Noble", "5",
	"other")))))
```