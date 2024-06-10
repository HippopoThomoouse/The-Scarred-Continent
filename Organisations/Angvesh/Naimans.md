## Members
```dataview 
TABLE 
	OrgRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Org/Naimans
WHERE 
	contains(file.folder, "Non_Player_Characters") OR contains(file.folder, "Player_Controlled_Characters")
SORT 
	choice(Role = "Clan Leader", "1", 
	choice(Role = "Runner", "2", 
	choice(Role = "Youngling", "3",
	"other")))
```
## Info
The [[Naimans]] are the largest nomadic clan on the plains. They are lead by [[Orion]]  and consist of many archers and raiders.

They have a unique coming of age ritual called the storm race. In this ritual young adults will race through thunderstorms while carrying lightning rods. Those that survive will become full adults. Special praise is given to those who survive whilst taking the most number of lightning strikes (this leads many strong members to be resistant to lightning damage).