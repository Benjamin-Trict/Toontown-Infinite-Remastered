# Toontown-Infinite-Remastered
The goal of this project was to take the stable Toontown Infinite source from 2015 and remove some of the flaws.  This server is a combination of the Toontown-Infinite code from January 2015 and the retro code from August 2014.

The repository for the 2015 code is now private.  Luckily, it was archived here - https://github.com/CrankySupertoon/Toontown-Infinite-Early-2015

The retro repository is currently still up, and can be found here - https://github.com/ToonTownInfiniteRepo/ToontownInfinite

Anyways, there are several changes made to this version:

- The fire cost no longer increments every time one is used.
- Suits are back to level 50 max instead of 12, and the CJ and CEO function based on this tier.  Facilities other than the factory no longer reward suit parts upon completion.
- The hands on the cogs are now the correct color (for some reason most of them were white)
- Animations for Toons Hit, Cogs Miss, and Restock SOS have been restored.
- The CFO no longer softlocks when the reward is a dance unite.
- Removed black, white, and grey toon colors to fix the DNA of certain NPCs; including Mata Hairy, Good ol' Gil Giggles, Sid Sonata, (whose DNA has been modified to match that of Toontown Online) and Doctor Drift.
- Removed Magic Cat and Trap Cat SOS
- Removed throwing cancelations -- this means that pies and evidence are no longered interrupted by pressing an arrow or jump key.
- Added a cooldown timer that appears after the CJ cogs have been stunned.
- The maximum laff is back to 137.
- Toontasks are back to the way they were in the original game, with Professor Flake and Shep Ahoy giving tasks for the final two cog suits.  I wasn't able to fix the jellybean jar back to 250, so the max is still 10,000 no matter what tier you're in.  For this reason the game still crashes when turning in a "Carry %s jellybeans" task.
- The ~trackBonus command is fixed, and if you use the value -1 it will make all gags un-organic.
- Added restart commands to all the bosses. - ~restartPie, ~restartCrane, ~restartScale, ~restartSeltzer (~restartSeltzer will not readjust the tables to face forward, and I have no clue how to fix it, but it does unflatten them if the CEO is on top.)
- Removed the ~disguise command and replaced it with ~cogSuit, for usage see this post - http://www.mmocentralforums.com/forums/showpost.php?p=4154926&postcount=844
- Added ~fillJury and ~stun commands to the CJ.  ~fillJury can also be followed by the number of seats you want to fill in the cannon round if you don't want to seat all 12.  It only works during the cannon round, and only once you're inside a cannon.
- Fixed the factory back to its original difficulty.
- There are no cogs walking around in Bossbot HQ.
- Debugs for boss health are included.  For those who don't know how they work, (if enabled) every time you damage a boss, a debug whisper will alert you how much health the boss has left. - https://imgur.com/cUlO0Qj  To enable this feature, once in-game type "~config suite debugs-on".  Additionally to turn them off again you can type "~config suite debugs-off".

For anyone who still wants the server from January of 2015, here's the file in a .7z format:
https://www.mediafire.com/file/mushfxwaqv7yxxh/Toontown-Infinite.7z/file
You'll need a file archiver program to extract it.  I recommend 7-Zip.  The source in the link is optimized for soloing bosses, gags are set to always hit and elevator timers for bosses are set to 0.

And here's the Panda3D you'll need to run it, it already has PYYAML and semidbm included:
https://www.mediafire.com/file/xvo7i80ao47uzgd/Panda3D-1.9.0.7z/file
You'll need to extract the folder and put it on the C drive, if you'd prefer to put it somewhere else you can change the directory of the Python file in PPYTHON_PATH.  Please note that the remastered version uses this same Panda3D, but it does not need to be moved since it works from inside the 'src' folder.

And lastly, here's the old retro source:
https://www.mediafire.com/file/ygqczswwjrmsfoh/ToontownInfinite-Retro.7z/file
The only modifications worth mentioning for this one are a few bug fixes so that the game client will launch, oddly it was originally working from 2 different resource directories and had no 'databses' folder.

To run these servers, follow these instructions:

Retro: First run start_astron_server.  Then run start_uberdog_server and press enter once.  Then run start_ai_server and press enter twice.  Finally run start_game_localhost, put in a username, and press enter.

Remastered or Original: Navigate to the astron folder in the main directory and find the win32 folder (inside the astron directory).  Run start_all.bat and then find the Command Prompt labeled start_uberdog_server and press enter once.  Then find the Command Prompt labeled start_ai_server and press enter twice.  Lastly navigate back to the main directory (the level before astron) and inside the win32 folder, run start_game_localhost.  Type a username and press enter.  The client should launch.

Here's a list of commands (apart from the ones mentioned above) that you can use in-game by typing them in the chat box - https://pastebin.com/7qG3PrB5

If you have any questions regarding any of this, feel free to contact me on Discord: Benjamin#8777

I give all the glory to God for using me to make this server.
