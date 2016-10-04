## The script of the game goes in this file.

## Declare characters used by this game. The color argument colorizes the name
## of the character.
image RusG = "RusGuard.png"
image SpyM = "SpyMaster.png"
define s = Character('Spymaster', color='#2E8B57')
init:
    $ povname = ""
    $ pc = DynamicCharacter("povname", kind=nvl, color='#B22222')
    $ flash = Fade(.25, 0, .75, color="#fff")

## The game starts here.

label start:
"16 years earlier.."
show SpyM
s "Hello, welcome to a world of intrigue."
$ povname = renpy.input("But tell me what is your name?")
pc "My name is %(povname)s."
s "That's a terrible name I'm going to call you 'Pawn'"
pc "But that's..."
$ povname = "Pawn"
s "Silence it's decided!"
"A strange feeling comes over you, its almost as if your mind..."
hide SpyM with flash
jump area2

label area2:
"You stand in the middle of a street.Patchy, distant memories flash before your eyes."
"You have a vague feeling that a lot of time has passed."
"The buildings all around you are on fire, one in particular stands out. Was that the acadmy home?"
"You decide to"
menu:
  "Enter the front door of the building.":
     "The door is blocked and cannot be moved."
  "Try the back door.":
    "The door gives way after a firm shove."
	
	
return
