**Val_Aaron-April-3-2026-20260403_090606-Meeting Recording**

3 April 2026, 01:06pm

11m 4s

**\
Aaron Bockelie** 0:03\
Through the first pass, which is.\
To translate the code into prose to describe what it does.\
By saying pros, I mean regular words that doesn\'t look like code anymore, like this code function does this thing and you state it very plainly. It doesn\'t need to go swirling into the entire ecosystem of the whole product. It just says this code does this.\
That code does that and so forth.\
And then what happens is that you now have this.\
It\'s like you\'ve described the code in a different way. The original description is the executable programming language itself that can be compiled into something that runs on a computer. The 2nd is essentially a miniature specification of what this code is supposed to do. It is text. It is regular written stuff.\
If you accidentally deleted the computer code and left all the descriptions, you could literally go back and rewrite the code again because you have a description of what it\'s supposed to do. You see how that they\'re they\'re kind of reinforcing each other, right? And if you collect enough of all of these descriptions.\
You start to have a whole hierarchy of description\'s. This thing\'s inside of this module and has all these bits. This thing has those modules, all those bits, and so forth and so now.

**\
Val Levitan** 1:24\
So these descriptions in essence are. If you do it the other way, it would be requirements, capabilities, ADRS, spec, architectural schematic, schematic diagrams and all of.

**\
Aaron Bockelie** 1:37\
Right, we\'re reverse engineering the code.

**\
Val Levitan** 1:43\
The decision ladder that was taken from an executive order saying build me this thing.

**\
Aaron Bockelie** 1:50\
Right O if you have a bunch of rose describing something about.

**\
Val Levitan** 1:54\
Rose.

**\
Aaron Bockelie** 1:56\
Prose PRO SE is the English word for what is. Yeah, you bunch of have a bunch of prose in a bunch of files and that prose has some sort of.

**\
Val Levitan** 2:00\
Uh, rose. Yeah, yeah.

**\
Aaron Bockelie** 2:10\
Intent encoded in the prose. This is for managing billing. This is for managing connections to some other system. This is for managing a database or whatever it is. You can then generally find all of the code related to that type of concern for that thing going on.\
And you can actually just read the prose as sort of a big sort of set of descriptors of what it\'s supposed to do. I would, I would actually call them stories, but I hesitate to call them stories because I hate how Agile has co-opted the word story.\
I I hate the fact that story, customer story or user story is a thing.\
But you, for better or for worse, you have a bunch of prose that describes the story of what that code\'s supposed to do. And when you sort of look at it in a in a collection, you begin to form a mental image or understanding of what it is you\'re doing.

**\
Val Levitan** 3:09\
I\'m almost, I\'m I\'m almost reading what what you\'re saying is that draws is, I don\'t know, a literal description of what a feature branch would be doing.

**\
Aaron Bockelie** 3:09\
Now I\'m gonna.\
Well, yeah, in in the coding context it can be. But prose in general is just the very generalized idea that something is written out in a plain language that you and I can speak and communicate. Like I don\'t. I don\'t go.\
Hey Val, open curly brace for I equals 1 to 27 plus N + 1 close curly brace semi colon. I don\'t tell. I don\'t talk to you like that. That\'s crazy, right? Nobody is stupid. I just say hey.\
Let\'s go through these 27 items and make sure that we go through every single one of them. Those are the same thing, right? And so we have to be able to because it\'s eventually the whole point of programming languages like going back to like Jacquard looms that are printing.\
Fricking patterns and rugs in France with punch cards. Programming something is taking the intention of what you\'re wanting to do and feeding it into a machine that follows a pattern, and programming is still that.\
Is the patterns are incredibly complicated now, incredibly complex and detailed. And so when you have a programmer who\'s trying to make something happen, the programming language, all languages have benefits and drawbacks to the way they\'re written and how they\'re engineered and designed to support some sort of.\
Model.\
So by switching it back to rose, we\'re kind of bringing it back to the person, the human element of what was supposed to have done here.\
And you will find a lot of software engineers who will absolutely scoff at that notion. They will be like, that is the dumbest \*\*\*\* I\'ve ever heard. The best description is the code itself, because they that\'s the way they were grown born. They were raised to think that way and and taught.\
To think that the best description of the system is the code itself. And yet they never took humanities or philosophy when they were engineer, and we didn\'t realize that actually it\'s the semantic intent of what the prose is that describes the language and the thing.\
I could just as easily write it directly in machine language assembly if I had the rose to describe what I wanted it to do.\
And and so that\'s kind of the the change that we have here is because we have a large language model that can understand code as prose just as much as prose as prose. And when we start realizing that there\'s this.\
Open-ended system that allows us to convert this to that however we want. We can get really creative about ensuring that our intentions are correct, and in some cases this goes the other way too. There may not be prose human languages for what you\'re trying to describe.\
Try to do.\
Think about math languages for a minute. When you talk about actual specific symbolic language in math, summations, sigmas, describing how an integral function might work, describing series and things like that.\
These are all words and and and symbols and notations that don\'t really have English language equivalent. This is why math is so hard for certain people, because you\'re actually learning a language that\'s not English or not your native speaking language, but eventually if you get used to using it.\
It becomes sort of first nature. You just speak it and you talk and you become a mathematician is basically what happens at that point, because you can speak that language. I\'ve never been a mathematician, probably won\'t be. I just know enough to kind of get by. It\'s like me learning about 6 language, 6 words of Spanish and trying to go to Mexico or something, right?\
It\'s kind of the same thing.\
So when we have a language model that can intuitively grasp all of the language for math and turn that back into prose too, now we have something that is able to basically be the Tower of Babel here a little bit. We can take anything we can possibly think of and throw it at this.\
Turn it into a different language to describe it with the understanding that certain languages that it converts to have less fidelity to describe it than the original language it has. And now the engineer that\'s steering this thing has to then.\
Kind of decide which language described it the most clearly.\
So now, going back to the programming question, programmers speak in software engineering languages. They\'ll pick a language. Let\'s say they\'re a Rust developer again, or TypeScript. They\'ll write their stuff in TypeScript and TypeScript to compile TypeScript and have it run.

**\
Val Levitan** 7:59\
OK.

**\
Aaron Bockelie** 8:15\
The most efficient language that you can use for TypeScript to describe TypeScript is its own language. If I convert TypeScript to prose, to just native text, it will, by the very definition of this translation, take more words and more effort.\
To describe it in a human language than in a rogramming language.\
If you have a function here that\'s 10 lines, it might take 100 lines of descriptive prose to describe those 10 lines of code.\
And so we then need to decide where the trade-off is for how much description we have, because there\'s now a matching or inference that\'s going on. If I I don\'t mean inference like the the A I computation inference, I mean like infer.\
When you and I are walking down the street to go grab some lunch and I\'m like, I tell you, you know what would be nice is a nice hot soup, Val. You\'re able to infer that I\'m interested in that type of meal without me saying anything else, because you know in your head what that is tasting like, just like you told me I should be drinking.\
Hot beverages in the morning instead of cold. And so the inferring model is what\'s so important. That\'s how developers can then infer the intentions of here\'s my code doing this, and there\'s your code doing that.\
And I can infer by the same language structure that these will work together if I join them together in this way. And so we\'re essentially using the language model to to refactor the code to be able to infer how they work to each other better than they did before.

**\
Val Levitan** 9:57\
Oh.

**\
Aaron Bockelie** 10:00\
I wrote it thinking this way. He wrote it thinking that way. They\'re kind of not compatible. We decompose them into the intentions, into the pros. We go look at the pros and go, oh, I see what\'s going on. You described it this way, and I\'m describing it that way, and that\'s why they don\'t fit to each other.\
We don\'t need to look at the code. We can understand the intention and now that I know the intention is written in the same way because this is the common language that we have, I\'m going to go back to my corners and rewrite this and you rewrite that and when we connect the code now it works properly.\
That\'s basically a specification at that point. Like there\'s a lot of other words that can be used to describe how this goes together. But that\'s in a nutshell, that\'s what a team of programmers is doing. They\'re following the specification, trying to solve the problem to.

**\
Val Levitan** stopped transcription
