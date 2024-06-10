## Members
```dataview 
TABLE 
	OrgRole AS Role, 
	regexreplace(file.folder, ".*\/([^\/]+)$", "$1") AS "Location"
FROM 
	#Org/Angveshi-Centaurs
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
## Culture

### Coming of age
To be accepted as an adult centaurs here must perform an act deemed worthy. These act are then reviewed at the next Evermeet.
Acts worthy of adulthood:

##### Killing a threatening party to centaur kind
This involves killing a group of non-centaurs
This can be done as a member of a group/warband as long as the centaur in question is involved
Wording is done such to discourage killing of noncombatants (e.g. children, traders) however depending on the elder (some elders are racist and hate other races) who is judging and the situation they may still count
##### Protecting something/one from danger
Killing centaurs is only permissible in “self defence” hence why its separate
“Self-Defence” is a very loose definition and not the same as on earth
E.g. X glared at Y funny so Y killed X. X could count this as “self defence” as they were provoked 
##### Other important less violent and militant acts 
- Act of learning
- Act of teaching
- Act of childbirth (this would apply to both parents)
- Clan specific acts
- e.t.c.
### Structure
Clan like structure. Clans consisting of anywhere from 100-5000 centaurs. Many of these numbers may consist of children or non combative members and smaller Groups tend to have a greater proportion of combative members.
### The Evermeet
They meet once every 4 years on the autumn equinox to commune, forge alliances, compete and find mates. It also serves as the backdrop for lots of political manoeuvring. The meet usually lasts for around a month but clans are allowed to come and go as they wish.

## Generic Racial Relationships
Adapted from: https://forgottenrealms.fandom.com/wiki/Centaur  

Heavily superstitious creatures centaurs find it hard to form alternate opinions on races and cultures they fear/dislike.

| Like                        | Hate    | Dislike | Neutral   | Fear        |
| --------------------------- | ------- | ------- | --------- | ----------- |
| Elves                       | Humans  | Yuan-Ti | Gnomes    | Dragons<br> |
| Firbolgs                    | Dwarves |         | Halflings | Giants      |
| Tabaxi                      |         |         |           |             |
| Other nature inclined races |         |         |           |             |
## Clans
- [[Naimans]]
- Small blooding clans
	- Roaming clan consisting of young centaurs. 
	- Their goal is to traverse the plain and perform an act worthy to be accepted into adulthood.
