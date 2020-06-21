# Toontown-Infinite-Remastered
The goal of this project was to take the stable Toontown Infinite source from 2015 and remove some of the flaws. This server is a combination of the Toontown-Infinite code from January 2015 and the retro code from August 2014.

The repository for the 2015 code is now deleted. Luckily, it was archived [here](https://github.com/CrankySupertoon/Toontown-Infinite-Early-2015)

The resources for the above repository can be found on the WayBackMachine [here](http://web.archive.org/web/20150104025550/https://github.com/ToontownInfinite/resources/archive/master.zip).

The retro repository is currently still up, and can be found [here](https://github.com/ToonTownInfiniteRepo/ToontownInfinite).

Anyways, there are several changes made to this version:

- The fire cost no longer increments every time one is used.
- Suits are back to level 50 max instead of 12, and the CJ and CEO function based on this tier. Facilities other than the factory no longer reward suit parts upon completion.
- The hands on the cogs are now the correct color (for some reason most of them were white)
- Animations for Toons Hit, Cogs Miss, and Restock SOS have been restored.
- The CFO no longer softlocks when the reward is a dance unite.
- Removed black, white, and grey toon colors to fix the DNA of certain NPCs; including Mata Hairy, Good ol' Gil Giggles, Sid Sonata, (whose DNA has been modified to match that of Toontown Online) and Doctor Drift.
- Removed Magic Cat and Trap Cat SOS
- Removed throwing cancelations -- this means that pies and evidence are no longered interrupted by pressing an arrow or jump key.
- Added a cooldown timer that appears after the CJ cogs have been stunned.
- The maximum laff is back to 137.
- Toontasks are back to the way they were in the original game, with Professor Flake and Shep Ahoy giving tasks for the final two cog suits. I wasn't able to fix the jellybean jar back to 250, so the max is still 10,000 no matter what tier you're in. For this reason the game still crashes when turning in a "Carry %s jellybeans" task.
- The *~trackBonus* command is fixed, and if you use the value -1 it will make all gags un-organic.
- Added restart commands to all the bosses. - *~restartPie*, *~restartCrane*, *~restartScale*, *~restartSeltzer* (*~restartSeltzer* will not readjust the tables to face forward, and I have no clue how to fix it, but it does unflatten them if the CEO is on top.)
- Removed the *~disguise* command and replaced it with *~cogSuit*, for usage see this post - http://www.mmocentralforums.com/forums/showpost.php?p=4154926&postcount=844
- Added *~fillJury* and *~stun* commands to the CJ. *~fillJury* can also be followed by the number of seats you want to fill in the cannon round if you don't want to seat all 12. It only works during the cannon round, and only once you're inside a cannon.
- Fixed the factory back to its original difficulty.
- There are no cogs walking around in Bossbot HQ.
- Debugs for boss health are included. For those who don't know how they work, (if enabled) every time you damage a boss, a [debug whisper](https://imgur.com/cUlO0Qj) will alert you how much health the boss has left. To enable this feature, once in-game type "**~config suite debugs-on**". Additionally to turn them off again, type "**~config suite debugs-off**".

For anyone who still wants the server from January of 2015, [here's](http://www.mediafire.com/file/p0k35q5pqhaz6gr/%255BTTI_Fresh%255D_-_Final.rar/file) the file in a .rar format.
You'll need a file archiver program to extract it. I recommend [7-Zip](https://www.7-zip.org/download.html). In addition, a few of the modifications from this redesigned server have been implemented into this one.

And [here's](http://www.mediafire.com/file/xdws5sbdbrnxb1s/Panda3D-1.9.0.rar/file) the Panda3D you'll need to run it, it already has *PYYAML* and *semidbm* included.
You'll need to extract the folder and put it on the C drive, if you'd prefer to put it somewhere else you can change the directory of the Python file in PPYTHON_PATH. Please note that the remastered version uses this same Panda3D, but it does not need to be moved since it works from inside the ```src``` folder.

And lastly, [here's](https://www.mediafire.com/file/xx3fsvwq6p9rwnx/Toontown_Infinite_Retro.rar/file) the old retro source. The only modifications worth mentioning for this one are a few bug fixes so that the game client will launch, oddly it was originally working from 2 different resource directories and had no 'databses' folder. Also, the default accessLevel for all accounts has been set to 700 (making everyone an administrator,) and the Toontorial will prompt rather or not to skip it, regardless of rather or not you're making your first toon.

To run these servers, follow these instructions:

Retro: First run ```start_astron_server```. Then run ```start_uberdog_server``` and press enter once. Then run ```start_ai_server``` and press enter twice. Finally run ```start_game_localhost```, put in a username, and press enter.

Remastered or Original: Navigate to the ```astron``` folder in the main directory and find the ```win32``` folder (inside the ```astron``` directory). Run ```start_all.bat``` and then find the Command Prompt labeled ```start_uberdog_server``` and press enter once. Then find the Command Prompt labeled ```start_ai_server``` and press enter twice. Lastly navigate back to the main directory (the level before ```astron```) and inside the ```win32``` folder, run ```start_game_localhost```. Type a username and press enter. The client should launch.

And lastly, [here's](http://www.mediafire.com/file/zf6dxu09gqad01b/Toontown-School-House-neatsketched.rar/file) a new server from 2019 November. This one is designed using Panda3D-1.11.0. To use it, install either the [32](http://www.mediafire.com/file/w1p6g1yg4nqjcya/Panda3D-1.11.0.exe/file) or [64-bit](http://www.mediafire.com/file/jd64nzvtdvnyw5z/Panda3D-1.11.0-x64.exe/file) version to your C root directory depending on your architecture, and run ```start_all.bat``` inside the ```win32``` folder. In addition, if you're installing the 32-bit version, you'll need to change the directory of the python copy inside the Panda3D folder, which is defined as a variable inside **PPYTHON_PATH** to be ```"C:\Panda3D-1.11.0\python\ppython.exe"```

Here's a list of commands (apart from the ones mentioned above) that you can use in-game by typing them in the chat box - https://pastebin.com/7qG3PrB5. Most of them work for all four servers seen here, but some are exclusive to the Retro game.


I give all the glory to God for using me to make this server.
