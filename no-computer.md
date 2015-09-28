# No computer project

Chemical reactions

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.


### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

While I was thinking about my first free-response question, I realized that
(written) chemical reactions are already a DSL.  Thus the group served by them
is chemists, and their experience is that they can look at chemical reactions
in isolation and more academically than in a lab setting.


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

This DSL is necessary because it allows for a clear, unambiguous way of 
describing a reaction and how it should occur without having to actually
observe or test the reaction.  It meets that need by showing exactly what is
or should be happening in the reaction.


### Why you?
_What excites you about this idea? How did you come up with it?_

I really like this because I love chemistry, and I love programming.  It came to
me when I was thinking of my first DSL, which seems like it would be a superset
of typical chemical reactions.


### Domain
_Describe the project's domain in five words._

Chemical reactions and their products


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

Written on paper/typed in some way/drawn out.  Programming looks like depicting
the molecules on some 2D surface and describing what they should result in.  
This is the right way because it simplifies and abstracts away a lot of the 
important, but not necessarily directly related stuff associated with chemistry.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

You don't really run the reaction (on paper), although when you run it in a lab
you usually see (or can test for) some change in chemical property.  The reaction
interacts with the user by changing some aspect of their environment.  Errors 
occur when something goes wrong in the reaction, and can be communicated by
nasty side effects, unknown/unwanted products, or simply nothing at all.

### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It is easy to describe simple reactions.  It is difficult to describe complex
reactions.  It is impossible to describe something that isn't a chemical
reaction.


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Not sure.  I'd argue that there are a number of different ways of depicting the
reaction, however I'd say in general the format/syntax isn't substantially 
different.  More like different dialects, not different languages.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Very little time would be spent on the language aspects - it's already done! I
suppose if someone has a revolutionary idea for transcribing chemical reactions
they could do so, but I don't know that there is a much better system.

### Scope
_How big an idea is this? How ambitious is this project?_

Fairly ambitious - there are lots of kinds of chemistry that use lots of kinds
of notation.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

It could be a good idea because you'd have to think really, really hard about 
language design in order to improve it.  It might be a bad idea because that 
might end up being too hard.
