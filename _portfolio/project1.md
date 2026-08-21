---
caption:
  title: Technical Design
  subtitle: Professional Work
  thumbnail: https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1085660/0ccf0dc0a8c4ec078db7ab99ddc820b2fa884441/header.jpg?t=1781815889
  
entry1:
  subtitle: Driving world state changes from player investment states
  video: <iframe width="720" height="480" src="https://www.youtube.com/embed/aDTHrTOrw1s" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: This central courtyard if the main social hub in Destiny 2 was created with multiple states for the final release. When a player loads into the Tower or changes their investment state for in-game Triumphs in particular categories, their local instance of the courtyard updates to reflect their progress. This change was interesting to engineer, because despite being visible to every player, they all had different investment states and needed to see the proper world state for them personally. This meant that the change could not occur on the world server itself, and also needed to be able to update dynamically on the fly. Luckily, players had to be in their menu to claim the Triumphs, so there was a brief moment to allow the state change to occur beyond the player's sight.

entry2:
  subtitle: Driving player investment state from collectibles and actions
  video: <iframe width="720" height="480" src="https://www.youtube.com/embed/-0vv_odCiGU" allowfullscreen></iframe>
  text: When collecting items in Destiny 2, there needed to be a series of hookups between completing the interact prompt, and actually producing the desired results. In this instance, the item's interact function is set to broadcast an incident to the server, which then pings back to the audience specified in that incident (in this case, only the interacting player). When that incident is received by the local player it activates a reward mapping site that is configured to display the correct information in the loot stream for player feedback, and also flips an unlock expression on the player's investment state, granting them a Triumph completion. Using these hooks was incredibly powerful but could also bog down the server if too many incidents were firing to quickly, so they had to be used in clever ways.

entry3: 
  subtitle: Driving object VFX from world/player/activity states
  video: <iframe width="720" height="480" src="https://www.youtube.com/embed/iwK9vBM1Ias" allowfullscreen></iframe>
  text: I'm describing this thing I did and, frankly, it's the most amazing thing you've ever seen. The subtleties and implied meaning and lore behind it are mindblowing, and you really can't think of anything else except how to get me on your team ASAP. <br>I understand, I'm amazing.
---
