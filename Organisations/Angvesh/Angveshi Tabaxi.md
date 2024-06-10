## Members
```dataview 
TABLE 
	OrgRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Org/Angveshi-Tabaxi
WHERE 
	contains(file.folder, "Non_Player_Characters") OR contains(file.folder, "Player_Controlled_Characters")
SORT 
	choice(Role = "Captiain", "1", 
	choice(Role = "Clan Leader", "2", 
	choice(Role = "Clan Member", "3", 
	choice(Role = "Youngling", "4", 
	choice(Role = "Associate", "5",
	"other")))))
```
## Info
For more info see here: [https://forgottenrealms.fandom.com/wiki/Tabaxi](https://forgottenrealms.fandom.com/wiki/Tabaxi)

Natives of the sourthern jungles far from the great desert the Tabaxi are a race of jaguar people. Before the fall of Angvesh they had a good relationship with the empire. Their boundeies were respected and terrirory was left alone. Since centaurs now dominate the plain not much has changed on that respect. However roaming groups of Yuan-Ti have been raiding Tabaxi groups and there is the potential for this to escalate in the future.