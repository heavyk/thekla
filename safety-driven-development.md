# safety-driven-development

### 2024-02-22 12:40 - why not just make all of the things safe?

if I have a piece of code that does something "unsafe" -- then what I want to do is to make an abstraction that makes it safe, and ensures that the thing is being used properly. so for example, let's say I have a thing that creates a context:
1. that context should be uninitialized, which is prolly unsafe. so I want to write: "ctx = Contxt{ null }"
2. that context should also exist inside of a struct somewhere -- which probably is the context of the name of the struct (ie, struct win has a ctx = WinContxt{ null })

so what we have are pieces that are describing a thing. a have an win, and that has to have a context in it, so I need a way to describe the thing (win) and say that it gets a context in it,-- ensuring that the unsafe behaviour of initialisation happens in the right place, and so is therefore, now *safe*. (it's just *that* easy)
