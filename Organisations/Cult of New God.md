## Members
```dataview 
TABLE 
	OrgRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Org/Cult-Of-Brian
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

- The members are an agitative force pressing to gain access to [[The Crossing]] to spread the good word.
- They rob travel passes and get in fights with [[Frontier]] guards.
# Info
This god is unknow and will reveal themselves when its followers show their worth under the guidance of Brian.

This god sort of exists. They are [[The Clown of Curiosity]]. However they may not pay any attention to the cult. At least not yet…..


