## Members
```dataview 
TABLE 
	OrgRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Org/Angveshi-YuanTi
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
For more info see here: [https://forgottenrealms.fandom.com/wiki/Yuan-ti](https://forgottenrealms.fandom.com/wiki/Yuan-ti)

Natives of the northern jungle near the great desert the Yuan-Ti are a race that is currently on the up. Ever since the fall of Angvesh the Angveshi that used to cull their people, in order to protect their farms & logging industry, have dissapeared. This has resulted in a population boom. M
