# Free project 1

## The user and a language
This section describes who the project would serve and why a language might be a
good way to meet their needs.

A CAOS (Computer Aided Organic Synthesis) DSL.

### What's the need?
_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help 
them?_

Currently, chemists have one of three ways in which they can predict how a 
reaction will occur, given certain molecules and conditions.

1. Map it out by hand
2. Look it up
3. Use expensive, proprietary software

For common, straightforward reactions, the first two are relatively easy to do.
Unfortunately (actually this is a good thing for humanity, but lots of work
for chemists) many professional chemists and researchers are interested in 
new, difficult reactions that haven't been seen before.  Thus they either have
to use expensive software that eats up their grant money (and may not meet 
their needs) or they have to take a long time to work it out by hand.  With a
free tool (language) designed to be both expressive and intuitive, this process
could be greatly improved (especially if the tool/language were designed to work
alongside existing databases of reaction pathways).


### Why a language?
_Why is a DSL appropriate for your user(s)? How does it address the need?_

A reaction is generally predicted using well-specified rules that apply to 
specific molecules and conditions.  This lends itself well to an imperative 
style such as

```
Molecule hydronium = OH-
Molecule hydroxide = H30+
Molecule[] products = react(hydronium, hydroxide, conditions)
products == [(Molecule) H20, (Molecule) H20]
```

ALternatively, when seeking synthesis pathways (i.e. a known endpoint) recursion 
works well, such as

```
Molecule endproduct = <something complicated>
Molecule startingpoint = synthesize(endproduct)
```

where `synthesize` is some sort of recursive function.

It meshes well with existing programming language paradigms and designs.


### Why you?
_What excites you about this idea? How did you come up with it?_

What excites me about this is that I've been working on something similar since 
my sophomore year, when I was still a premed student taking Organic Chemistry.

I thought to myself that these rules were relatively straightforward, and it was
very much an algorithmic process.  I've been working on it off and on since 
then.

### Domain
_Describe the project's domain in five words._

Predicting organic chemistry reaction pathways


### Interface (syntax)
_How might the user interact with the language? What does programming look 
like? Why is this the right way to interact with the problem domain?_ 

They could use an internal DSL; a library could be written using some preferred
language and then provide hooks for some end-user to interact with.

They could use an external DSL; a friendlier syntax that provides more 
constraints on what can be done, and how.

They could use a GUI-based external DSL; they draw molecules and conditions and
then press a big "react" button.  This is probably the most end-user friendly,
especially for chemists who aren't great with programming.  

Overall I think each of these should be provided and well linked, if the DSL
was well funded and supported.  This allows users of many technical backgrounds
to interact with the software and customize it to meet their needs.  In context 
to 111, the best is probably internal - this is the easiest to write and test
because there are fewer layers between the algorithms and the user, and it 
allows the most technical users to use it intimately and find the pain points.


### Operation (semantics)
_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

It should provide (optionally) verbose output describing what step in the 
reaction is happening, and how it is determining what step happens.  Errors 
include invalid molecules (i.e. ones that couldn't possibly exist under those
conditions), as well as invalid reactions (where nothing would happen there).
Potentially safety messages as well; i.e. that byproducts are produced that are
explosive or toxic, or what have you.  These should be exceptions with good 
informative names and error messages so the user can programmatically handle
them if they want to.


### Expressiveness
_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to predict and test reactions.  It should be possible to 
push the limits of the program; i.e. things it thinks should be impossible but 
the user might know is not.  It should be impossible to break fundamental laws
of physics/chemistry, as well as do anything that goes beyond organic chemistry.)


### Related work
_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well 
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

Yes, the one I've been working on [here](https://github.com/Dannnno/Chemistry).
There are some other ones too, that I learned about asking 
[this question](http://chemistry.stackexchange.com/questions/7765/program-that-simulates-basic-reactions-in-organic-chemistry)
on the Chemistry Stack Exchange.  I know little about them; they are of varying
usefulness and popularity:

- [WODCA from the Gasteiger group](http://www2.chemie.uni-erlangen.de/software/wodca/index.html)
- [CHIRON from the Hanessian group](http://osiris.corg.umontreal.ca/chiron.shtml)
- [LHASA from the Corey group](http://cheminf.cmbi.ru.nl/cheminf/lhasa/)
- [SYLVIA](https://www.molecular-networks.com/products/sylvia)
- [ArChem - also called Route Designer](http://www.simbiosys.ca/archem/)
- [Chematica](https://en.wikipedia.org/wiki/Chematica)
- [Some guy's pet project](http://www.dimuthu.org/blog/2008/11/22/organic-chemistry-reaction-simulator/)

None of them appear to have widespread use or support, and have varying levels
of functionality.

## The Project
This section examines whether the idea makes for a good CS 111 project.


### Suitability
_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

Probably upwards of 70% of their time on the systems aspect.  While many of 
the reaction mechanisms are straightforward, data structure design would be
very non-trivial, as would be transcribing the mechanisms to algorithms.  The 
language would probably be relatively trivial.


### Scope
_How big an idea is this? How ambitious is this project?_

Very big and ambitious.  It takes a ton of domain knowledge and programming
expertise.


### Benefits and drawbacks
_Why might this be a good idea for a project? Why might this not be a good idea 
project?_

This is probably not a great idea for a project.  It is very large-scale, and 
really hard.  Furthermore, most of the time working on it would not be focused
on the language design.  That being said, the complexity of it all could lend 
itself to a very interesting project, and the language design decisions to make
everything work flexibly but also be easily extensible would be very interesting
as well.
