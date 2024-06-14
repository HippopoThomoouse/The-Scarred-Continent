## Members
```dataview 
TABLE 
	OrgRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Org/The-Ladies-Men
WHERE 
	contains(file.folder, "Non_Player_Characters") OR contains(file.folder, "Player_Controlled_Characters")
SORT 
	choice(Role = "Captiain", "1", 
	choice(Role = "First Mate", "2", 
	choice(Role = "Second Mate", "3", 
	choice(Role = "Navigator", "4", 
	choice(Role = "Crewmember", "5",
	"other")))))
```
