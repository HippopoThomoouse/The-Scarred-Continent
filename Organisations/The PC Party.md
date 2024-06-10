## Members
```dataview 
TABLE Player
FROM 
	#Org/PCParty
WHERE 
	contains(file.folder, "Non_Player_Characters") OR contains(file.folder, "Player_Controlled_Characters")
```
