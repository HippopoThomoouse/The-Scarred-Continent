# Cities
```dataview 
TABLE Translation, Population
WHERE contains(file.folder, "Places/Eshreek Kingdom")
SORT Population DESC
```

# Members
```dataview 
TABLE 
	CountryRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Country/Eshreek
WHERE 
	contains(file.folder, "Non_Player_Characters") OR contains(file.folder, "Player_Controlled_Characters")
SORT 
	choice(Role = "Ruler", "1", 
	choice(Role = "Noble", "2", 
	"other"))
```