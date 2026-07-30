**Claude_advancement_review_implimentation-20260413_093216-Meeting Recording**

13 April 2026, 01:32pm

15m 17s

**\
Aaron Bockelie** 0:03\
So the question that Val is asking me is, if we\'re going to switch from a big monorepo to submodules, and the main module that holds the submodules in Git is itself maybe a meta module or a meta repo. And what I mean by meta repo is

**\
Val Levitan** 0:14\
In.

**\
Aaron Bockelie** 0:23\
It doesn\'t contain a lot of the actual executable code for the platform. It just kind of holds everything else as like a scaffolding.\
What\'s the process of going from a large monorepo with all the concerns into a bunch of submodules?\
And so the answer is, like all consultants, they tend to say, is it depends. I\'ll say that with the joke first.\
The reality is, is that it depends on what the mono repo\'s doing.\
So, what I mean by this is, let\'s say you have a multi-concern sprawling monorepo of a full application platform. It has\...\
user interface conventions. It has a core engine, it has a database, it has connectors and modules and plugins for all sorts of stuff. It has all these different things that it does. And it\'s all tightly woven together over 15 years of staying together as one.\
Big thing.\
O.\
The natural instinct a lot of people will say is, because they\'ve heard the word hammered for the last two decades, is obviously it needs to be microservices. And I couldn\'t disagree with that more, that microservices is potentially a terrible, terrible pattern to pick up.\
So it\'s not microservices.\
Instead.\
What we want to do is we want to say, how do we structure this code in a way that allows us to understand what types of code it is?\
So.\
As an example, you may have a bunch of protocol processing things for your product, and you may have other products that also use the same protocol. Let\'s use SAS as a specific example of this. The SAS protocol.\
has a specific implementation, a specific dictionary, a specific way of interacting, and all the data types for the protocol.\
protocol for SAS is not something that you have to actually concern with the serial port interface.\
The protocol is the language spoken over the transport.\
So the transport could be serial, it could be Ethernet, it could be, I don\'t know, RS485, it could be whatever.\
So\...\
What this means is, is that if SAS as a functional capability of your platform is baked into the monorepo.\
The move to get it away from the monorepo to start to shift into submodules is to abstract the SAS capability into a set of libraries, which probably already exist as this in the monorepo.\
but instead of deliberately storing it with the monorepo itself.\
you move it into another Git repo. And the Git repo becomes a resource, a submodule resource for any application that wants to communicate with the SAS protocol.\
The SAS protocol can be reused over and over again against any other tool or platform that uses SAS.\
Another example would be historical horse racing, in my opinion.\
I don\'t know how it\'s actually implemented, so nobody can hold this against me for being wrong.\
But if you have to pull the horse race information from a service provider, and you have to have a game simulation for it to run to present the deterministic math that comes out of it.\
Why would you ever bake that into the game, as a hard-coded piece of the game, when you can build essentially A submodule that facilitates historical horse racing as a plugin that can be added? This is like in Rust, we call them crates. You create a crate for HHR.\
That, when loaded, becomes a resource available for the main application game that runs it.\
If you have a determinist, if you have a completely non-deterministic game engine module for math, load that one instead. You don\'t have to have the rust, the horse rust crate, you have the horse race crate, you have a random math crate, or whatever it is. And\
This way, you are pulling modules in that are their own Git repos to facilitate these services, and they have all of these modules, all of these Git submodules.\
have specific data contracts promising what they do.\
These are not microservices. It\'s a promise that they do these things. I provide a set of interfaces. I provide some sort of data feed, given configuration, and so forth. This starts to break it down into the pieces of data.

**\
Val Levitan** 5:37\
But.\
I, I, I understand this, but if there is, if we\'re working with mono repo or some sort of a mixed large repo, I don\'t know, maybe it\'s multiple, I don\'t know, five different repos, how do you determine what needs to be?

**\
Aaron Bockelie** 5:40\
Code.\
Mhm.\
Right.

**\
Val Levitan** 5:59\
Pulled from there.

**\
Aaron Bockelie** 6:02\
You determine it by what is the best bang for your buck by peeling it away.

**\
Val Levitan** 6:07\
Okay, and when you determine to pull a portion of it away, how do you surgically separate it so it doesn\'t break anything and then reassembles it again into a\...\
A good working product.

**\
Aaron Bockelie** 6:22\
O.

**\
Val Levitan** 6:23\
Let\'s say out of monorepo you said I\'m going to have 15 repos and they are\...\
Independent and I am going to pull them all apart. It\'s like a picture. I\'m going to pull it into 15. Yeah, so how do you how do you?

**\
Aaron Bockelie** 6:39\
Expand out.\
Yeah, so the very first thing you\'re doing is you have the architecture mod understanding of what the whole application does.\
What does the full monorepo do from an architectural standpoint?\
If you can\'t describe that, then you\'ve gotta, you\'ve got to start there.\
So if the code is so interwoven that everything\'s all inlined and everything\'s all mixed into place and you have all of these privates all over the place.\
The very first thing you need to do is you need to stop looking at the code and ask the step back and ask, what does this application actually concern itself with?\
So if it\'s a huge hairball of a bunch of stuff that\'s been added and glued into it, like a big deco collage.\
Then the first thing you need to do is you need to ask, what does this deco collage actually do when I look at it in the hole?\
And from there, you can form an opinion on how you might restructure some of this stuff.\
It\'s like.

**\
Val Levitan** 7:51\
And what is the what is the test whether you restructured it correctly or incorrectly?

**\
Aaron Bockelie** 7:56\
So\...\
This is where dry principles and solid principles come into code play, for example.\
When you ask yourself, how many lines of code is this? How many different functions does it have?\
What\'s the cyclomatic complexity of this code? How many times does it iterate through things? These are all sort of\...\
complexity measures that you can look at code and go, yeah, this is really hard to follow. Or actually, this is very, very straightforward to follow.

**\
Val Levitan** 8:31\
Well, it\'s a subjective judgment. It depends who looks at it.

**\
Aaron Bockelie** 8:34\
No, it\'s not subjective. It is absolutely computable. You can compute the cyclomatic complexity of functions by looking at how many nested functions you have calling each other.

**\
Val Levitan** 8:45\
Okay, so how do you do that? What\'s\...

**\
Aaron Bockelie** 8:47\
It depends on the language. So Java has different ways to lint and understand this versus TypeScript versus C and whatever.

**\
Val Levitan** 8:56\
Okay, but there is a machine definition of what is acceptable and what is not.

**\
Aaron Bockelie** 9:01\
You can absolutely lint and measure most different code bases in waves.

**\
Val Levitan** 9:05\
Okay, so as I\'m pulling things apart, I could put it in a machine and the machine will tell me, eh, still complicated.

**\
Aaron Bockelie** 9:14\
It\'s the machine will give you a statistical measure of what\'s written. It is up to the human to make the judgment call as to whether that complexity is necessary or not.

**\
Val Levitan** 9:19\
Right.\
Well, but if this particular individual constantly makes a judgment that this excessive complexity based on the machine judgment is acceptable, then this human is probably either lazy or superhuman.

**\
Aaron Bockelie** 9:27\
And.\
The human needs to have empathy for their peers. The person needs to empathize, does the entire engineering group.\
Understand what the \*\*\*\* that they\'re doing is.\
Yeah.

**\
Val Levitan** 10:17\
And the machine judgment of complexity is probably the right thing to measure, and even if you think that it\'s still acceptable, dumb it down to what machine to what machine.

**\
Aaron Bockelie** 10:28\
I\'m going to use\...\
I\'m gonna use.\
But I\'m going to use a theme park, an amusement park analogy here.\
You must be at least this tall to ride this ride.\
Okay, we\'ve all seen that sign and we\'ve all seen the disappointment when you\'re not tall enough, right?\
There are several reasons why that thing is\...\
Has the type?\
The first is the ride sucks. It\'s very boring and won\'t make any money if it\'s for everybody. If it\'s dumbed down to be a kid ride, it\'ll be safe for everybody, but it won\'t make enough money.\
If it\'s too high, it\'s dangerous.\
except for that small number of people, and you won\'t make enough revenue because not enough people will ride the ride.\
There\'s a sweet spot in the middle.\
where you have to do this and the machine measurement is literally that measuring thing. It just sits there and just measures it.\
Active things called customers walk through it. So, yeah.

**\
Val Levitan** 11:30\
Okay, I understood. And what is this measurement called?

**\
Aaron Bockelie** 11:36\
It\'s linting or it\'s static analysis. There\'s there is 100 ways to static analyze. There\'s there\'s.\
There\'s countless ways to measure the way code works. There\'s all these tools that developers build, and some of them are more popular and some of them are less popular. It depends on what you\'re measuring.

**\
Val Levitan** 11:57\
Understood.

**\
Aaron Bockelie** 11:59\
So, and it\'s and it\'s per language too, so\...

**\
Val Levitan** 12:02\
And how long how long would it take to pull apart a mono repo code into multiple? I understand this is a difficult difficult answer.

**\
Aaron Bockelie** 12:11\
Yeah.\
Yeah, so, so it could take anywhere from\...

**\
Val Levitan** 12:16\
But for somebody like Biratko, for example, who has worked on Omni and he really knows it, what does it take for him to pull it apart?

**\
Aaron Bockelie** 12:25\
It would take a\...\
If you have a strong loop of being able to measure your change and run all the tests and verify the code runs and does all its things, it\'s really not as bad as it sounds. It\'s A refactoring job.\
It is a\...\
take these concerns, so there\'s a couple pieces you have to kind of think about. One is, how are you going to add the code back in after you take it out? Because at compile time, you end up with possibly a big mono application still.\
This also means that you might end up with several applications that interop with each other. What I mean interoperate with each other is maybe they talk to common bus, or maybe they talk over a network to each other. And as soon as you have things that are\...\
executing their own binary in separate contexts, but they need to stay connected. Now you need to have shared libraries for them to talk to each other. So now you have\...\
one side, the other, and the conduit between them. These are three different concerns. And when you start thinking about these transports and conduits, you start to realize that these are the modules that make up your product.\
And so one of the first things you can do is you might say, you know what?\
We\'ve written the transport, the communication protocol for this four different times. They all speak the same pattern, but it\'s written specifically in the code in four different places.\
Let\'s remove all four of these and build one copy of it that we can instance everywhere.

**\
Val Levitan** 14:13\
And that takes time.

**\
Aaron Bockelie** 14:14\
And that takes time, and that that untangles that little piece of the of the knot.\
The next time you go, what else is common between all these things? Well, a formatter is common. Well, let\'s fix that formatter. Now we\'ve got to fix it everywhere. You\'re going to find all these places where you have your own formatting and inconsistencies. And the only way you find this stuff is by running tests.\
So if you have tests for everything that you\'ve got, you can start to find the inconsistencies.

**\
Val Levitan** 14:41\
And.\
And so that obviously takes time.

**\
Aaron Bockelie** 14:47\
Yes.

**\
Val Levitan** 14:49\
But again, are we looking at half a year or we\'re looking at three weeks?

**\
Aaron Bockelie** 14:54\
I think that if you have a coding agent and you use it highly effectively, you can collapse it down to weeks or months.\
It now is how fast is the slowest part of your company that allows this product to go out the door? That\'s the limiter.\
Yep.

**\
Val Levitan** stopped transcription
