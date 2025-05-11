# IT265 Design Treatment Checkpoint

---

## Title

Commandant


---

## Concept Statement

A randomly generated hexagonal map with a radius of 7 tiles serves as the battlefield between two commandants with various troops.


---

## Genre and Style

### Genre

Strategy 


### Style

A top down view of a simplistic landscape, with  the game mechanics taking front and center.


---

## Target Audience

### Demographics

Commandant targets players of all ages, as the strategic depth allows for many styles of play. 


### Accessibility

As the prototype currently stands, there is limited accessibility, but a voiceover of the tiles and the troops within range, as well as tooltips could help impaired players.


### Inclusivity Strategies

As the visuals are not completely done, the intended plan was to have a diverse cast of characters representing the individual troop types.


---

## Core Gameplay Mechanics

### Primary Mechanics

Hex‑Based Movement
Units occupy a hex grid and spend movement points to traverse tiles. Each unit type has a unique move range (Infantry 1, Cavalry 3, Scouts 3, Archers 1, Commandant 1), and terrain (forests, rivers, mountains) imposes additional costs or benefits.

Action Economy
On your turn you have 3 actions, each consumed by either moving one unit along a valid path or attacking an enemy in range. Managing these limited actions creates tension and forces trade‑offs between offense, defense, and positioning.

Unit Diversity & Combat
Five unit types (Infantry, Cavalry, Archer, Scout, Commandant) each bring a role:

Infantry: high defense, ideal for holding chokepoints

Cavalry: high attack and mobility, excellent for flanking

Archers: long‑range strikes but vulnerable in melee

Scouts: ignore full‑tile blocking, useful for infiltration

Commandant: inspires nearby allies, granting +2 attack
Combat is resolved by adjacent melee (range 1) or ranged (archers), subtracting defense from attack (+inspire bonus if buffed), with a floor of 1 damage.

Terrain Effects

Mountains: adjacent attackers gain +1 attack

Rivers: cost 2 moves (1 for Scouts)
-->

### Goals and Challenges

Surround the enemy Commandant’s hex on all six sides Or Eliminate the Commandant to win!
Players must juggle controlling chokepoints, advancing their own Commandant to buff troops, and denying terrain advantages to the opponent.


### Progression

The troop number and board size can be customized to increase difficulty.


### Game Rules

Setup

Place each Commandant on opposing map edges (one tile in).

Other four units for each player deploy on the six adjacent hexes around their Commandant.

Turn Structure

Players alternate turns, White first.

On your turn, take up to 3 actions: move 1 unit along a valid path or attack 1 enemy within range.

After 3 actions, the camera flips and play passes to the opponent.

Movement & Blocking

No more than 4 units may occupy a hex (Scouts ignore this limit).

Terrain movement costs and buffs apply per unit type.

Combat

Units may attack adjacent hexes (range 1) or, for Archers, hexes at range 2–3.

Damage = max (1, Attack + InspireBonus – DefenderDefense).

If a unit’s health drops to 0, it is removed; killing a Commandant ends the game immediately.

Map Shrink

Every 2 full turns, the outer ring of hexes is removed; any unit or Commandant caught on a removed tile is eliminated (Commandant’s elimination also triggers game end).


---

## Story and Setting

### Setting

A temperate climate with mountains, rivers, fields and forests.
### Plot

The main characters for the two opposing sides, the commandants, are at war.


### Characters

The game will have two playable characters, the leaders of each army. The army consists of multiple types of troops, with one leader that serves as a win condition, as well as the homebase city. The insignia of each army will be a distinct medieval coat of arms.


---

## Unique Selling Points (USP)

The randomized board, as well as the shrinkage of the game surface and customizable rules offer a unique selling point.


---

## Inspiration

### Sources

The fictional game called towers from the fantasy series “The Stormlight Archive” by Brandon Sanderson.


### Why It Matters

Inspired the theme and a loose interpretation off the mechanics

---

## Player Experience Goals

The game invokes thought and creativity when coming up with new strategies.


---

## Technical Requirements

### Platform

Played on PC or mobile 


### Tools

Made in unity, using C# and a unity store assets.


---

## Art and Sound Direction

### Visual Style
A simplistic art style with cleanly styled hexagons.

### Sound Design

Sound design is extremely important, but unfortunately i was unable to implement audio design in this prototype.


---

## Monetization Strategy

Custom skins for different troop types allowing for personalization, as well as animations for attacks.


---

## Treatment Details

### Gameplay Example


Board Setup
White Commandant at (0, –3) with four troops on its adjacent hexes:

Infantry at (1, –3)

Cavalry at (1, –4)

Archer at (0, –4)

Scout at (–1, –3)

Black Commandant mirrored at (0, +3) with the same troop types around it.

A mountain stands at (2, –2), a river runs between (0, –1)→(1, –1), forests and fields elsewhere.

White Turn 1
Actions Remaining: 3

Select White Cavalry (at 1, –4)

Movement (cyan): highlights all hexes ≤ 3 movement away, respecting river cost (2 moves) and mountain adjacency.

Attack (red): any enemy within range 1 (none in range).

Inspire (gold): all hexes within 2 of Commandant at (0, –3) light up gold.

Action 1: Move Cavalry → Mountain (to 2, –2)

Pays 1 move to leave (1, –4) → (2, –3), 1 more to (2, –2).

Ends on mountain: next attack adjacency gets +1 mountain buff.

Select White Archer (at 0, –4)

Moves only 1; highlights possible hexes.

Attack range 2–3 (red) shows no targets within range.

Action 2: Move Archer → (1, –3)

Moves into Commandant’s inspire zone (gold), now at (1, –3).

Select White Infantry (at 1, –3)

Movement 1 (cyan) and no enemies adjacent yet.

Action 3: Move Infantry → (0, –2)

Enters range of the Black Archer at (0, +2)? No—still out of range.

End of White’s actions → camera flips, now Black’s turn.

Black Turn 1
Actions Remaining: 3

Select Black Scout (at –1, +3)

Scouts ignore full‑tile blocking; can cross river in 1 move.

Action 1: Move Scout → (–1, +1) (across river in one action)

Select Black Cavalry (at 1, +3)

Moves 3; mountains give no benefit here.

Action 2: Move Cavalry → (0, +1)

Now adjacent to White Infantry at (0, –2)? Distance 3 only—no attack yet.

Select Black Archer (at 0, +4)

Range 2–3 encloses White Infantry at (0, –2) (distance 4)? Just out of range.

Action 3: Move Archer → (0, +2)

Ends within range 2 of White Infantry at (0, –2). (No attack left)

End of Black’s actions → camera flips, back to White.

Turn 2 & Map Shrink
After Black’s turn, MapShrinker detects two completed turns and calls ShrinkMap().

The outer ring at distance 3 is removed; any units caught there (e.g. White Scout at –1, –3 or Black Cavalry at 1, +3) are eliminated—if a Commandant is on one of those tiles, the other player immediately wins.




---

### Challenges and Considerations

#### Potential Risks

I think balancing issues could be difficult, as well as stagnation with the limited environment tiles.


#### Feasibility

Making sure the game is attractive to  all audiences, as well as marketbale, as well as a robust tutorial.


---

## Visualizing the Game Concept

### Concept Sketches or Storyboards
- Provide at least **two sketches**  
- Ensure sketches accurately represent the game’s concept and theme  
- Maintain coherence with the game’s style and theme  


![Commandant1](https://github.com/user-attachments/assets/4f8311f7-712b-49a1-b476-fa538b3c8524)

![CommandantSketch](https://github.com/user-attachments/assets/af1d3dce-7179-4f4c-90e0-ae296d0ad943)


---

## Pitch Preparation

### Pitch Summary

Commandant is a medieval strategy game that takes place on a hexagonal board of varying terrain. The dueling feudal lords launch everything they have in order to take each other out and finally claim the land they believe is rightfully theirs. The terrain can change from game to game and navigating the terrain is essential to victory. Combining traditional strategy with more modular design and beautiful medieval art, Commandant caters to players of all skill levels.




### Target Audience Appeal

The rich strategy of Commandant, as well as the fresh board everytime the game starts allows strategy fans to pour endless hours into developing strategies around an ever morphing terrain.


### Market Differentiation

Commandant breaks down the barriers of entry in most strategy games, and instead communicates the mechanics in a way for the player to morph to their own needs, instead of forcing the player to learn the starting protocol for the same map over and over.


---

## External Feedback


### Feedback 1
Sam - Girlfriend

Likes design and idea, concerned about doing mental math for troop interactions.

Add troop value to the front of troop cards.



### Feedback 2
Greyson - roomate

worried about the 2 win conditions and the fact that the capitol must be surronded on three sides.

I will evalute the win conditions and potentially make it by only capturing the commandant.

### Feedback 3
Luke - roomate

concerned about the Scout troop class, as stealth is hard when both players get a top down god view of the board.

evaluate the class, I may replace it with a heavy artillery class, such as trebuchets.




---

