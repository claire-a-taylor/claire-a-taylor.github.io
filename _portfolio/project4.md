---
caption:
  title: Prototype Mechanics
  subtitle: Personal Work
  thumbnail: /assets/img/portfolio/BPLogo.png
  
entry1:
  subtitle: Realtime Menu Battles Actions + Act Record/Replay
  video: <iframe src="https://drive.google.com/file/d/1RMfFmi_zk2VG93drl-_JcCiu3tWDBzmf/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: The inspiration for this concept was the movie "Final Fantasy 7: Advent Children". I wanted to create a type of action battle system where players could engineer complex strings of movements and attacks that they didn't have time to plan out in a traditional action game. The result is a prototype where a player opens a menu loaded with basic commands, causing time to slow down (time is slowed much more dramatically in combat). I also wanted the player to be able to create their own custom commands, so I created a system where an Act Record function can be toggled on which keeps track of the commands a player enters and their state when they do (such as being in the air). After creating a queue of actions and toggling Act Record back off, players are given the option to name and save their new action combo in the menu. In this way, a player can build out a suite of combos as they play to minimize how often they need to actually open the menu, and achieve a complex high action battle experience.

entry2:
  subtitle: Lock-On Targeting + Parry/Disarm
  video: <iframe src="https://drive.google.com/file/d/1LGZBa1kGGjuhLSsjbdVyUMPpREEom4N1/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: These mechanic protos came from wanting to implement my own "Soulslike" framework. I started with the basics of movement and locking on to targets, but when I came to the idea of parrying, I wanted to make it a little more interesting. Rather than a single omnidirectional parry, I thought it might be interesting to have to read where an opponent's attacks were coming from and parry in the correct direction to knock them off balance. The result is a 4-direction parry system that would overlap with a character's 4-direction attacks. By attacking in a direction to meet an enemy's attack with good timing, a clash would be initiated that could block or repel the attack. The final piece came when I considered what the difference between such a clash would mean with large size or stat differences, and I created the parry-disarm. Instead of just repelling an attack, a player could conceivably disarm an enemy completely, detaching the weapon actor and sending it spinning off in a direction based on the player's orientation and the direction the parry was activated in.

entry3:
  subtitle: Mini-Dungeon Framework + Homage Battle System
  video: <iframe src="https://drive.google.com/file/d/1uoUGN8JgH3J6v_ubLyaVpefy--yB9YEX/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: The intent with this proto was to make a battle system that emulated the PS1 game "Xenogears". On a character's turn, choosing to attack moves them into position with the selected enemy where the player can queue up various types of attacks. Once triggered, the attacks dequeue against the targeted enemy one by one until either there are none left, or the enemy's HP is expended. While dequeuing, more attacks can be queued up dynamically to keep the combo flowing. The framework I decided to build around it was a concept for a sort of mini-dungeon dive, choosing to form a party of various classes that each have their own skills, strengths, and weaknesses to see how far they can progress in a series of escalating battles. Depending on the position a particular character is placed into, they can execute different types of skills or have effects on the party as a whole. The battle was structured into distinct phases but started to grow too convoluted in execution, so I'd want to rework that if I revisited the concept.

entry4:
  subtitle: Niagara Particle Absorption Exploration
  video: <iframe src="https://drive.google.com/file/d/1-8Q7rAtc0o56giyZScojazDexORZgI6u/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: For this exploration, I wanted to make an absorption system similar to that seen in the classic PS2 version of "Onimusha". At first I used physical actors to represent the orbs to be absorbed, drawing any of them within a range to a specified socket created on the player character's skeleton. Once contact was made, I reduced their size until they reached a minimum and deleted them. Over time I started to try diving into the Niagara particle system to get familiar and make some simple effects to go along with the proto, creating an effect on the target socket to denote when the absorption was active. I also made a system to represent a kind of swirling void and set the the emitted particles from it to be attracted to the absorption socket, while also reducing the void's emission volume to make it appear that the energy was being drawn into the player and off of it's source. The next time the player attempts to absorb afterwards, the void is released and ramps back up to full strength again.

entry5:
  subtitle: Grapple Points
  video: <iframe src="https://drive.google.com/file/d/1Ux8wQwqOftXKFnCuF1VLwx7myxFEmKFp/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: In the same project as my Absorption protos, I also decided to attempt a 2d version of grapple points using the grapple ability "Sekiro" as a touchstone. I created invisible objects that searched for the player in an area around them. When the player is detected, the closest grapple point to the player that is also located in front of them is designated as the target point and is overlayed with a widget feedback layer that changes its appearance based on the distance from the player. When fully activated and the correct input is pressed, the player will attach to the point with a Cable Component before being launched by a physics impulse at the target. After use, the grapple point has a cooldown before it is ready to be used again. While this did work at a very basic level, I think I'd put a lot more thought into the method of launching the character, as the system now was far to unreliable for the player to go where they wanted to. For a prototype though, it did the job I wanted it to and laid the groudwork for future iteration.

entry6:
  subtitle: Campfire Character Select + Point/Click Battle
  video: <iframe src="https://drive.google.com/file/d/1iyUYfEe4JaW9dM1aTDfGnFpAEZS8U4zf/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: UNDER CONSTRUCTION
---
