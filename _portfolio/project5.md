---
caption:
  title: Current Game Project
  subtitle: Personal Work
  thumbnail: /assets/img/portfolio/BPLogo.png
  
entry1:
  subtitle: Wave Repulser - Making a Shmup from Scratch
  text: So I decided to make a shmup game. <br>Why? It felt like a doable genre as a solo-dev, and when I was younger I used to lose myself in games like Strikers 1945 3 in my college arcade room, Ikaruga on Gamecube, and R-Type on the SNES; over the years, perhaps even more influentially, there were a handful of 'indie' shmups that were incredible experiences as well. So the first step, of course&#58; research the market. What were successful shmups? What were failures?  Shmups, as a genre, enjoy a relatively small but devoted fanbase, so it was very important for me to understand what it was people were and were not wanting in them. The goals I've settled on are as follows&#58; <style="text-align:left><ul><li>Interesting Scoring System</li><li>No "Real" Momentum</li><li>Bullet Patterns</li><li>Dynamic/Flashy Levels</li><li>Story Mode and Arcade Mode (with non-gameplay elements removed)</li><li>No "Shop"</li><li>Difficulty Settings</li><li>Endless Mode</li></ul><br>After getting my initial actors laid out in a simple environment I had some important choices to make that would shape the rest of the project&#58; vertical vs horizontal, 2d vs 3d, and moving camera vs moving stage. After much research, playing, and mulling I settled on a 3d style with a moving camera and opted to use both vertical and horizontal segments. I didn't want to run into any trouble down the line with different sized monitors and, with my intention to utilize both vertical and horizontal, I opted to make the play area an equal sized square with a locked aspect ratio. What follows are breakdowns of some of the challenges I faced I how I chose to solve for them.

entry2:
  subtitle: CONTINUED
  image: <img src="/assets/img/portfolio/ViewMover.JPG"></img> 
  video:
  text: The very first issue to solve was of course, the play space. After deciding on the aspect ratio, I created an actor called "ViewMover", which would be the center of everything. Intended to be the prime driver that everything else followed. I added box collisions as components and positioned them to act as boundaries at the play space edges, and then gave those each another copy of themselves just a little further out from the center to act as killboxes, just in case the player managed to slip through somehow. In addition to the View Mover, I also created a simple empty actor called "PlayerAnchor" that only holds the player's ship as a child. This was important to give the player freedom of movement around the play space, while still being able to force different types of movement on them without causing unexpected interactions. The ViewMover gets supplied with a variable called "UniversalMovement" that dictates the speed and direction it travels, and disseminates that movement data to other actors that need to move in lockstep with the play space (like the Player Anchor). So then another dilemma&#58; how best to move everything through the stage? The immediate and maybe most obvious answer would be a spline, twisting and curling in a path for everything to follow. Unfortunately, when I tried this I very quickly ran into a problem of some accuracy issues with extremely long splines. I was getting inconsistent location and speed data back from them, which directly affected trying to keep all the various actors in lockstep with the movement. The system I implemented to replace using splines, is a kind of instruction node based point-to-point relay (which, if I'm being honest, is still kinda like a looser spline system).

entry3:
  subtitle: CONTINUED
  image: <img src="/assets/img/portfolio/MovementData.JPG"></img>
  video:
  text: Upon starting play the ViewMover is supplied with an array of InstructionTriggerVolumes, invisible objects that collide only with the ViewMover's root. The ViewMover looks at the active i-value in the array, reads the WorldLocation of the associate volume, and interpolates its current UniversalMovement towards the volume as a target. Each InstructionTriggerVolume is loaded with data dictating things like movement speed, view/player rotation (we'll get into that later), and how quickly it should adjust to it's new target speed/direction. Using this method I can spread the instruction volumes in a loose path throughout the stage, activating or deactivating them at will to create alternate routes through stages based on a player's actions or performance. Every step of the way I am double checking to make sure I make things frame rate independent, and while there may be some very slight variability when the ViewMover changes to a new target, it is always focused on reaching the new instruction volume and never has a chance for these almost imperceptible variations to compound on one another.
  
entry4:
  subtitle: CONTINUED
  image: <img src="/assets/img/portfolio/ExposeQuat.JPG"></img>
  video:
  text: 

entry5:
  subtitle: CONTINUED
  image:
  video: <iframe src="https://drive.google.com/file/d/1kHsYyHkj4Ij8iK9lUlaotpGSZxSFqj6_/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: Camera

entry6:
  subtitle: CONTINUED
  image: <img src="/assets/img/portfolio/EnemyMovement.JPG"></img>
  video:
  text: Enemies

entry7:
  subtitle: CONTINUED
  image: <input type='checkbox' /><img src="/assets/img/portfolio/ModePulse.JPG"></img>
  video:
  text:
  
entry8:
  subtitle: CONTINUED
  image: <img src="/assets/img/portfolio/FormV.JPG"></img>
  video:
  text:

entry9:
  subtitle: CONTINUED
  image: <img src="/assets/img/portfolio/EnemyAttack.JPG"></img>
  video:
  text: Weapon Macros

entry10:
  subtitle: CONTINUED
  image:
  video: <iframe src="https://drive.google.com/file/d/1-SUxI0C7LGH83tBEWEHbjs0-4Q_Ny6p-/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: Current Progress
---
