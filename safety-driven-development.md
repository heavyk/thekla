# safety-driven-development

### 2024-02-22 12:40 - why not just make all of the things safe?

if I have a piece of code that does something "unsafe" -- then what I want to do is to make an abstraction that makes it safe, and ensures that the thing is being used properly. so for example, let's say I have a thing that creates a context:

1. that context should be uninitialized, which is prolly unsafe. so I want to write: "ctx = Contxt{ null }"
2. that context should also exist inside of a struct somewhere -- which probably is the context of the name of the struct (ie, struct win has a ctx = WinContxt{ null })

so what we have are pieces that are describing a thing. a have an win, and that has to have a context in it, so I need a way to describe the thing (win) and say that it gets a context in it,-- ensuring that the unsafe behaviour of initialisation happens in the right place, and so is therefore, now *safe*. (it's just *that* easy)

(12:59) ok so thinking about it more, the next thing I want to have is a way to just write a narrative intro to the piece: "an app with a win" should be all I need to ensure that there's an app struct and a win struct pre built for me, and any app or win struct definitions I make, get appended to the safely built ones. (01:04) in addition to this, it's pretty easy to parse out things like "add touch, themes, undo array, etc." and it'll just do it. there also needs to be a visual interface where I can see the actual c++/d/lua/v/asm/whatever syntax that is output by my textual intro. we'll consider that intro there to be piped into one of those wizards that putputs all of the boilerplate stuff for me. man, I totally can't remember what those get started programs are called. ne4vrmind.
	anyway, so thinking about this a bit further -- I'm going to call them boilingplaters are just outputting code to the file, when really they don't need to be output to the file at all -- because say I have 40 apps I've built with wins, and micrsoft goes and adds on a new feature (or something idoitic like touch happens) and suddenly that old win/mouse code has to be updated in 40 apps. ---- well, if it were just known as a touch, mouse, or win,-- then all that would be updated already from the new safety guidelines.
	guidelines is actually a good word, because it would be optimal if the wizard could have access to the code, and so therefore knows, that if you never touch, just the mouse is fine. I'd also like to think of them kinda like traffic signals in that it can the guidelines can optimise flows for optimal performance (like doing two or three initialisations in a place where the data is available for free), and generally *conduct* or *orchestrate* the whole program together (so, more than a boilingplater, actually).
