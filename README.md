# Independent-Study
Independent research project, single credit hour, may turn into a long term project

This file is to keep track of research done throughout the project and have timestamps for when it was done

# Jan 31 - Feb, 6, 2024

Tetris gym, the rom that I would be editing to complete the current idea, is based on a disassembly descended from TAUS, which is a tetris rom  primarily to add more useful statistics in game, TAUS uses flips and cc65 to build their rom as detailed in the "How to Build" section at https://github.com/ejona86/taus

The first ways I found to disasseble an nes ROM were to use the Ghidra decompiler plugin found at https://github.com/ilyakharlamov/Ghidra-Nes-Rom-Decompiler-Plugin or to do so directly with da65, I will most likely use the latter option but we will see what happens as we move along, at this point I will definitely be doing something with the nes, but what exactly is yet to be determined

the da65 users guide https://cc65.github.io/doc/da65.html#s4
there is no proper tutorial on using it but here are some useful links that I have found:
https://forums.nesdev.org/viewtopic.php?t=21342 (forum crawling already, always a good sign)
https://www.lemon64.com/forum/viewtopic.php?t=69582

Some great info can be found on this page 
https://forums.nesdev.org/viewtopic.php?p=241882&sid=6195c5ef7d8ef9cd3a38517de9f4d8a0#p241882 

As far as modifying games go not everyone has the same approach, but since my main goal here is to improve how comfortable I am with assembly, I will most likely be modifying the disassembly directly

After making the changes you then create an ips file that can be used to patch the rom it appears the main way to do this is simply to feed the unmodified and modified files to lunar ips and it will do the rest
Lunar IPS: https://www.romhacking.net/utilities/240/

Lunar is also the main tool used to apply patches to roms

Unfortunately I was not able to find any kind of list of seeds of professional matches, I could likely get some of them by asking around, but to my knowledge I'm not even sure if seeds are generally made public or tracked at all, I believe it is possible to reverse engineer a seed by going through a peice set, but I have no idea how to do so and it would likely be a painfully time consuming and tedious task. 

With a project like this I be able to get some other community members on board to help with things, but given the timeframe for the independant study I would likely have little to nothing to actually show off by the time I'm supposed to be done

# Feb 7 - Feb 12, 2024 update

For patching I have ultimately ended up using floating ips, or flips, which is a newer ips program built as a replacement for lunar ips, the one that i was using before, flips is the one that is used by TAUS as mentioned earlier and the romhacking.net page for it can be found here, https://www.romhacking.net/utilities/1040/

I have gotten comfortable with dissasembling (and theorhetically assemblimg) with da65 and cc65.

https://cc65.github.io/doc/da65.html
https://cc65.github.io/doc/cc65.html

I'm only unsure about assemblimg with cc65 since I haven't been able to get anything to assemble yet, but that is a problem with the stuff that is being assembled, not with the process that I am using to do so. Obviously when you disassemble something it isn't able to just be reassembled without modification, and while I have been doing a lot of pouring over documentation and tutorials to familiarize myself with 6502 assembly, I have yet to actually succeed in compiling anything large, at this point it may be a good idea to find a version that is already properly disassembled so that I can modify that, but finding what I need, knowing which is correct, and knowing what to do with it, are all currently proving to be separate tasks

For the project idea I'm ultimately working towards, it would be a modification of the tetris gym romhack, the github for which can be found here, https://github.com/kirjavascript/TetrisGYM, and the patch for which can be found in the patches folder.

Though for the purposes of working with a disassembly done by someone who knows what they are doing, I have found it much easier to find one for the base rom of the game rather than the hack, so my endgoal for the project within the scope of the class may end up being simplt modifications of the base game, since the gamemode project was never going to be realistic from the start anyway, the goal here is to improve my skills and familiarity with the process.

some stuff that I've found useful in the learning process

a series of 6502 tutorials
https://www.youtube.com/watch?v=yEiNs7pKNh8&list=PLgvDB6LWam2WvoFvh8tlUqbqw92qWM0aP

a manual disassembling guide, explains stuff really thoroughly
https://www.youtube.com/watch?v=mR1G9ZA2UfQ

a collection of resources, including a variety of books taken straight from the 80s
http://www.6502.org/tutorials/

I'm also sure the ghidra tool could be useful in a number of ways, but while I have it working and have poked around a bit, I still find myself completely lost in ghidra and have even less of an idea of whats going on

# Feb 13 - Feb 20 update
This week has not been particularly productive as I have been quite busy, it's just been some reading through the documentation that I have already found

I have added a 6502 notes file for myself so that I can take notes on syntax and things to easily look back at

# Feb 21 - Feb 27 update
This week has once again been a lot of familiarization with assembly and the disassemblies that I have access to, but there has been some more major discoveries than last week

The largest thing that has happened this week is my discovery of the Mesen emulator, which supports various types of games, the nes included, the thing that sets Mesen apart from a more standard emulator is that it includes some really neat developer tools, there is a debugger and assembler, which provide partial disassemblies of the rom that you have open, not only that, but it has a database of known rom files that it can pull header names and comments from, so you can look at what some of the variables do without having to look through and figure it out yourself. 

There are also a variety of other tools available so that you can watch exactly whats happening in real time as the game is running, including an event viewer, memory viewer, register viewer, and trace logger, to name a few. It has been an awesome tool for helping me actually understand what it happening within the game as it is running, and I'm sure it would be even more useful if I had any idea what I was actually doing.

The other thing that I found was this github page https://github.com/CelestialAmber/TetrisNESDisasm/tree/master, which provides a usable disassembly to look at, of course, it's in a very different form from what I'm working with as the people who made it have infinitely more experience in the matter than I do, but that's exactly why it has been such a big help to look at.

# Feb 28 - March 5 update
I started the week by looking at ghidra again for about an hour, I feel like I gained as little as I did last time, I went through some online resources such as the ghidra class on the official github, but I still feel lost so I decided to pivot a bit since I feel like I'm running into a bit of a wall

Now that I have a better understanding of what it is that the nes is doing and how it works, as well as 6502 assembly and architecture in general, I've looked more into the aspects of actually modifying games, one resource I've had on the radar for awhile is this youtube video: https://www.youtube.com/watch?v=alg6hS70h8E

which also links to a variety of other resources that I have seen but not used so far, 

A general resources guide: https://emulation.gametechwiki.com/index.php/ROM_hacking_resources

the fceux emulator has a lot of similar tools to mesen, right now I'm not familiar enough with the 2 of them and the process here to say which is better or worse, but fceux feels more beginner friendly and has less sensory overload in any given tool or tab: https://github.com/TASVideos/fceux

if I were to edit any kind of tile is seems like tile molester is essentially the only option that I've found: https://www.romhacking.net/utilities/109/

There's a variety of hex editors, I've used gHex in the past, the video recommends windhex, and the article recommends XVI32 and translhexation, I don't know much about the differences between them at this point, we will figure out more about that in the future I'm sure

# March 6 - March 18
With spring break there wasn't a whole lot accomplished in this period, I worked on familiarizing myself with some of the software that I discovered last time and watching through some tutorials on youtube, nothing really major to report.

# March 19 - March 26
Coming out of spring break and into midterms has made finding up until this weekend very hard, I worked on it for about an hour on friday and an hour yesterday, as well as for about the last hour or so

So far for hex viewing I've just been using Ghex, since I'm doing everything on my laptop on linux, I'm not sure how windhex will run through wine and haven't bothered to try, I haven't really seen any reason why I should use one over the others, though since I haven't dove too far in yet I may find out about some feature in the future.

I have also downloaded and played around with Tile Molester a bit, Like many of these tools to work with old games, the final executable is simply a jar, so no problems with using it on linux, or anything else for that matter. Since I don't have anything in particular in mind that needs to be done yet, it's more been just to see what the software is like since it seems to be more or less unavoidable. Overall the program is really simple and doesn't really need to be anything else, you select a size and then color pixels, nothing too groundbreaking here.

Apart from this I have still had difficulties getting anything to recompile but feel like I've gotten a little closer, Ghidra seems a little less angry at me as does ca65, so I think I've made some kind of progress, but I make no promises.
