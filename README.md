# tutor-pooyan
Disassembled, buildable source for the game Pooyan (Tomy Tutor version)

The file pooyan.a99 is a an assembler program for the not very well known home computer, the Tomy Tutor.

It is the result of the disassembly of the game Pooyan from konami.

I choosed the syntax from a cross-assembler called A99.

What to say ? This program is really compact: 8 kilo bytes of code and data, with only 88 unused bytes.

The code in itself is not easy to read nor interesting, but my point was to clear some issues related to cartridge development on the Tutor.
So here are some comments:  
. the rom starts at address $8000 with the 16-bit word $5555 (though only the first byte is checked by the bios)  
. the entry point is at address $8002  
. hardware (sound chip, video chip, vram, ...) is never accesed directly, but only through functions offered by the BIOS  
. BIOS functions are called through a jump table found between addresses $0020~$028A (functions starting at $0254 are not found in the japanese version)  
. The program freely uses the main RAM found between adresses $f000~$f050  


My point is, since the game was developped by Konami, it is reasonable to assume that their programer(s) where handled some kind of guidelines/developement documentation by Tomy. Don't you think so ?  
For instance, this documentation would have documented each functions from the bios, explaining what it does, and how to call it.  
So far, I could not find any evidence of such a documentation on the web, so if anyone has a clue, or picture, feel free to create an issue or something.


Good retro-developement  
2024/04/01 ergonomy_joe
