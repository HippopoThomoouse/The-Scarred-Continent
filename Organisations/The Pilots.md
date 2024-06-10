## Members
```dataview
TABLE 
	OrgRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Org/The-Pilots 
WHERE 
	contains(file.folder, "Non_Player_Characters") OR contains(file.folder, "Player_Controlled_Characters")
SORT
	choice(Role = "Captiain", "Leader", 
	choice(Role = "First Mate", "Smuggler", 
	"other"))
```

