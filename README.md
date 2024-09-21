<img src="https://github.com/user-attachments/assets/2ad86f70-12b4-4500-997d-9f8c1874a9b5" alt="Dal logo" width="80"/>
<h1>Associated with Dalhousie University</h1>

## CSCI1110
### TimBot Simulation
This project simulates a survival battle among different types of robots (TimBots) on the planet Doh-Nat. TimBots compete for resources, such as the Spresso plant, and try to eliminate their competitors through various actions like harvesting energy, moving, and attacking. The simulation runs until a maximum number of rounds is reached or only one TimBot remains functional.

### Overview
The planet Doh-Nat is represented as a torus-shaped grid where TimBots move around, harvest energy (Spresso), and engage in battles. Each TimBot has a personality that dictates its behavior, including how it moves, attacks, and defends. The simulation prints the status of the grid and the TimBots after each round, showing the interactions and outcomes.

### TimBot Actions
- **Movement**: A TimBot can move north, south, east, or west across the torus grid.
- **Harvesting**: TimBots collect energy from Spresso plants to survive and perform actions.
- **Combat**: TimBots can engage in battles with other TimBots or use ion cannons to attack from adjacent districts.
- **Defense**: TimBots can use force shields to defend themselves against attacks.

### Simulation Phases
1. **Energy Consumption**: Each round starts by deducting 1 Jolt of energy.
2. **Sensing**: TimBots sense their neighboring districts for Spresso plants and competitors.
3. **Firing**: TimBots with enough energy can fire their ion cannons at adjacent competitors.
4. **Defense**: TimBots can activate force shields to defend against ion shots.
5. **Movement**: TimBots move across the grid according to their strategy.
6. **Battle**: If multiple TimBots are in the same district, they engage in combat until only one survives.
7. **Harvesting**: TimBots harvest Spresso plants if available in their current district.

### TimBot Personalities
1. **ChickenBot**: Avoids combat and prefers moving to empty districts with Spresso. Never attacks.
2. **SpressoBot**: Prioritizes districts with Spresso plants for harvesting.
3. **AngryBot**: Seeks out other TimBots to attack and harvest Spresso.
4. **BullyBot**: Attacks adjacent TimBots using ion cannons but behaves like a ChickenBot otherwise.

### Input Format
The input consists of grid dimensions, simulation parameters, and TimBot configurations:

- **Grid and Simulation Parameters**:
  - `R` (rows), `C` (columns): Dimensions of the Doh-Nat grid.
  - `J`: Number of Jolts provided by harvesting Spresso.
  - `G`: Number of rounds needed for Spresso to regrow after harvest.
  - `N`: Maximum number of rounds for the simulation.
  - `T`: Number of TimBots.

- **TimBot Configuration**:
  - `P`: Personality of the TimBot (`chicken`, `spresso`, `angry`, `bully`).
  - `I`: Unique ID of the TimBot.
  - `X`, `Y`: Initial grid coordinates.
  - `E`: Initial energy (Jolts) of the TimBot.

#### Sample Input----------------------Sample Output
```                          
5 5 5 10 100 4                Round 0    
chicken 1 2 2 1               |           0||           0||           0||           0||           0|
spresso 2 3 3 1               |           0||           0||           0||           0||           0|
angry 3 2 3 1                 |           0||           0||(C  1  5) 10||(B  4  5) 10||           0|
bully 4 3 2 1                 |           0||           0||(A  3  5) 10||(S  2  5) 10||           0|
                              |           0||           0||           0||           0||           0|
```
Here, `C`, `S`, `A`, and `B` refer to ChickenBot, SpressoBot, AngryBot, and BullyBot, respectively, along with their ID and energy level.

#### How to Run
1. **Compile the program**.
2. **Run the program**.
3. **Provide input**: Using the input format to define the grid, simulation parameters, and TimBots.

#### Simulation Flow
The simulation runs for the specified number of rounds or until only one TimBot remains functional. After each round, the state of the grid and the remaining energy of each TimBot is displayed.





