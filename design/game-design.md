 Medieval Fantasy 4X Strategy Game - Complete Design Overview

## Core Concept
A competitive 1v1 4X strategy game featuring simultaneous turns set in a medieval fantasy world. Games are designed to last 30-45 minutes maximum, combining elements of classic 4X games with modern competitive design.

## Game Structure
### Map
- Square grid (initial size 5x4, subject to iteration)
- Each square contains:
  - Terrain type
  - Up to 3 buildings
  - Units (if present)
  - Resource generation type (Gold or Crystal)

### Victory Conditions
- Primary: Control 4 cities for 2 consecutive turns
- Secondary: Eliminate all enemy cities
- Tiebreaker: Most cities after 30 rounds
- Game length cap: 30 rounds maximum

### Turn Structure
#### Phase 1: Advisors
- Both players simultaneously presented with 4 identical advisor options
- Each advisor provides 3 actions in a specific order
- Algorithm ensures all 5 possible actions appear at least once
- Players choose one advisor without knowing opponent's choice
- Choices revealed simultaneously

#### Phase 2: Action Execution
Turn sequence:
1. Combat Resolution (for squares in combat state)
   - Automated AI-controlled combat
   - No player input during combat
   - Survivors can move after combat (if movement was ordered)

2. Players execute their 3 actions in advisor-defined order from:
   - Move
     - Order units to move to adjacent squares
     - Movement resolved after all actions are declared
     - Larger armies push smaller ones when movement conflicts occur
   - Build
     - Construct buildings in controlled squares
     - Maximum 3 buildings per square
   - Produce
     - Generate additional resources
     - Can exploit squares even without buildings
   - Research
     - Advance in technology tree
     - Unlock new units, spells, and upgrades
   - Recruit
     - Create new units in cities or barracks

### Combat System
- Occurs when opposing units end a turn in the same square
- Square enters "Combat State" for the next turn
- Combat resolves at start of next turn, before any actions
- Basic unit AI:
  - Units move toward nearest enemies
  - Attack when in range
  - Cavalry units flank through sides

## Game Elements
### Resources
1. Gold
   - Primary currency
   - Used for units and buildings
2. Crystals
   - Special ability currency
   - Used for advisor bonuses
3. Workers
   - Required for building operation
   - Recoverable when buildings destroyed

### Terrain Types
1. Plains
   - Cavalry advantage
   - Free movement for all-cavalry groups
2. Forest
   - Infantry advantage
   - Blocks ranged attacks
3. Hills
   - Ranged unit advantage
   - Elevation mechanics
4. Mountains/Water
   - Impassable except for special units
5. Cities
   - Defensive advantages
   - Built-in walls
   - Archer positions

### Buildings
1. Production Buildings
   - Resource generation multipliers
   - Type based on square's resource generation (Gold or Crystal)
2. Combat Buildings
   - Towers
   - Walls
   - Counter: Siege units
3. Military Buildings
   - Barracks for unit recruitment

### Technology System
- 4 vertical technology levels
- 4 building slots per level
- Buildings can be upgraded
- Example: STABLE unlocks cavalry units and horse-related technologies

## Faction Design
Initial faction: Humans
### Unit Categories (Levels 1-4)
Level 1:
- Footman (General Infantry)
- Archer (Anti-Infantry/Flyer)
- Cavalry (Anti-Archer)
- Pikeman (Anti-Cavalry)

Level 2:
- Knight (Heavy Cavalry)
- Catapult (Anti-Siege/Ranged)
- Light Priest (Support)

Level 3:
- Griffon (Air Assault)
- Red Mage (Crowd Control)

Level 4:
- Angel (Epic Unit)

### Leaders
1. General
   - +1 Unit Damage
   - 25% crystal discount on movement specials
2. Merchant
   - Enhanced trading
   - 20% increased gold production
3. Paladin
   - 50% discount on white spells
   - 50% discount on combat actions
4. Wizard
   - 33% crystal cost reduction
   - Reduced spell cooldowns
   - 25% cheaper Mage Guild research

## Visual Style
- Pixel art style similar to Avianos
- NES/early PC game aesthetic
- Clear, readable unit designs
- Distinct territory control indicators

## Platform Considerations
- Designed for both PC and gamepad control
- Grid-based design facilitates cross-platform play
- UI must accommodate both control schemes
