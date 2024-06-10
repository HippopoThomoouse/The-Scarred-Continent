# Members
```dataview 
TABLE 
	CountryRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Country/Angvesh
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

# Info
Empire that used to spawl across the entire [[Angvesh Plains]] until about 5 years ago when it fell.