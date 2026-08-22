---
caption:
  title: Technical Design
  subtitle: Professional Work
  thumbnail: https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/1085660/0ccf0dc0a8c4ec078db7ab99ddc820b2fa884441/header.jpg?t=1781815889
  
entry1:
  subtitle: Driving world state changes from player investment states
  video: <iframe src="https://drive.google.com/file/d/1df-muFtxoukgvZj0_5CZqtKUFFo-d-on/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: I implemented this central courtyard in the main Destiny 2 social hub with multiple states for the final release. When a player loads into the Tower or changes their investment state for in-game Triumphs in particular categories, their local instance of the courtyard updates to reflect their progress. This change to existing content was interesting for me to engineer because, despite being visible to every player, it needed to reflect the proper world state for each of their personal investment states. This meant that I needed to make the change not occur on the world server itself and also needed to make it able to update dynamically on the fly. Luckily, players have to be in their menu to claim Triumphs, so there was a brief moment I was able to use to allow the state change to occur beyond the player's sight.

entry2:
  subtitle: Driving player investment state from collectibles and actions
  video: <iframe src="https://drive.google.com/file/d/1dICWYsKYewGzbutbsslZ6cVsSj1vdgkg/preview" width="100%" height="100%" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: When collecting items in Destiny 2, there needed to be a series of hookups between completing the interact prompt and actually producing the desired results. In this instance, I needed to make the item's interact function broadcast an incident to the server, which then pinged back to the audience specified in the incident (in this case, only the interacting player). I set the incident data up to activate a reward mapping site when it is received by the local player, configured to display the correct information in the loot stream for player feedback and also to flip an unlock expression on the player's investment state. Doing this allowed me to grant them a Triumph completion after interacting with the collectible. Using these hooks was incredibly powerful but could also bog down the server if too many incidents were firing to quickly, so I had to often use them in clever ways.

entry3: 
  subtitle: Driving object VFX from world/player/activity states
  video: <iframe src="https://drive.google.com/file/d/1ew3CFJWJmL8OH4aRoEOSWO3qCH6c1FYv/preview" width="720" height="480" frameborder="0" scrolling="no" seamless="" allowfullscreen></iframe>
  text: For this chest, the request was to make it so it could only be looted once a player had fulfilled certain conditions, and also to provide feedback to the player about when it was ready to be looted. I worked with the VFX team to come up with a thematic 'cage' over the chest that would form or melt away depending on the combined state of the player and activity. I implemented a call in the activity script that would check if the defending enemy squad had been cleared out and also would double check to make sure the local player investment state contained the 'key' they needed. I then added a channel value to the chest itself that would drive a variable between 0 and 1 on signal from the script, lerping the value being fed into the VFX to smoothly add or remove it as needed. The result was a chest that could only be accessed after the conditions were met and clearly communicated its state to the player.
---
