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


