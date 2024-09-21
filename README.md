<img src="https://github.com/user-attachments/assets/2ad86f70-12b4-4500-997d-9f8c1874a9b5" alt="Dal logo" width="80"/>
<h1>Associated with Dalhousie University</h1>

## CSCI1110
## TimBots
- TimBot is essentially a simulation-based strategy game. In this game, robots (TimBots) compete on a grid-like planet, Doh-Nat, by harvesting energy (Spresso) and fighting each other to survive. The goal is for a TimBot to outlast all others by managing resources, engaging in combat, and making strategic moves across the grid. It's not a real-time game that is directly played, but a simulation that runs based on specific rules and inputs, showcasing different strategies for each type of TimBot.
### Specification
* This is a robot simulation where robots compete for supremacy of the Doh-Nat Planet.
#### Overview
TimBots are robots competing for supremacy on Doh-Nat, a torus-shaped planet with limited resources. The primary energy source, Spresso plants, grows in the districts of a grid. TimBots must roam, gather energy, and eliminate rivals to survive.

#### Simulation Rules
The planet's surface is an m×n grid with edges connected (a torus).
The simulation proceeds in rounds, with each round involving:
* Energy Use: TimBots consume 1 Jolt to remain operational.
* Sensing: Bots detect neighboring districts for Spresso or other TimBots.
* Combat: Bots may fire ion cannons at adjacent enemies, costing 1 Jolt per shot.
* Defense: Bots can defend with a force shield if attacked, costing 1 Jolt per defense.
* Movement: Bots can move to adjacent districts, using 1 Jolt.
* Battles: If multiple bots occupy a district, they engage until only one survives.
* Harvesting: Bots harvest Spresso, which regrows after a set number of rounds.

#### TimBot Types
* ChickenBot: Avoids combat, focusing on empty districts with Spresso.
* SpressoBot: Prioritizes harvesting Spresso.
* AngryBot: Seeks combat and tries to gather Spresso if available.
* BullyBot: Fires at any nearby TimBots if energy permits, otherwise behaves like ChickenBot.

#### Input Format
The simulator takes 6 integers followed by TimBot configurations:

R, C, J, G, N, T (Grid size, Spresso yield, growth time, max rounds, number of bots).
Each TimBot is defined by its personality, ID, coordinates (X, Y), and initial energy.

#### Sample Input----------------------Sample Output
```                          
5 5 5 10 100 4                Round 0    
chicken 1 2 2 1               |           0||           0||           0||           0||           0|
spresso 2 3 3 1               |           0||           0||           0||           0||           0|
angry 3 2 3 1                 |           0||           0||(C  1  5) 10||(B  4  5) 10||           0|
bully 4 3 2 1                 |           0||           0||(A  3  5) 10||(S  2  5) 10||           0|
                              |           0||           0||           0||           0||           0|

