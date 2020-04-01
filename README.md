# warbot-jin
An AI for the warbot game we code for a school project

The code is based on the one our teacher gave us, and is meant to work in a [Netlogo](https://ccl.northwestern.edu/netlogo/) project he gave us.
We had to code some turtles of a faction which would evolve in a world with some resources and an ennemy faction.

## Rules
- Code the behaviour of the one faction's turtles
- Do not rely on any color based function, your faction color can change depending on your opponent
- The turtles are of types : bases, explorer, harvester and rocket launcher
- 

## Restrictions
- Turtles have limited memory slots (10 in total)
- Turtles can only access information within their range (they can't memorize another turtle id and access its position using the id if they are not in range)
- We should not base our strategy on an example layout (two bases for each faction aligned on the y axis)

## Our strategy
- Could be described as a kind of [Zerg Rush](https://tvtropes.org/pmwiki/pmwiki.php/Main/ZergRush)
- Continuously produce explorers
- Make explorers share information and monitor its propagation
- Use explorers to find resources and take information to the base
- Once the base knows where to find resources, search for an enemy base
- When found, either commit suicide on it or go share the position based on probablities and wether the base knows this base position
- No use of Rocket Launcher
- Two harvester per base, which try to create farms

## Retrospective
- This strategy was a lot of fun to imagine and code
- It proved quite efficient despite its absolute simplicity
- We had no time to test it against other players, but it seemed quite obvious that it was efficient against factions that use all of their resources at the beginning
- When the rush begins and explorers crash themselves, they produce resources that can easily be transformed into really good farms
- Thus, if the first rush fails, it often enables the enemy's fast growth
- With better farming and a concerted rush, this strategy could be improved (gather all around a base and rush simultaneously for instance)

