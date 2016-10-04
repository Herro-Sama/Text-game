## The script of the game goes in this file.

## Declare characters used by this game. The color argument colorizes the name
## of the character.

define s = Character('Spymaster', color='#2E8B57')
init:
    $ povname = ""
    $ pc = DynamicCharacter("povname", kind=nvl, color='#B22222')


## The game starts here.

label start:
"16 years earlier.."
s "Hello, welcome to a world of intrigue."
$ povname = renpy.input("But tell me what is your name?")
pc "My name is %(povname)s."
s "That's a terrible name I'm going to call you 'Pawn'"
pc "But that's..."
$ povname = "Pawn"
s "Silence it's decided!"
"A strange feeling comes over you, its almost as if you're being possessed.."
jump area2

label area2:
"Today, Now."
"You wake up in the middle of the street. Your home of the last 16 years is on fire."
"The spymaster has been murdered. The Russian Embassy have attacked."
menu
  "" 
return
