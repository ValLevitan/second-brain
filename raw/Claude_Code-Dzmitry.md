**Claude_Code-Dzmitry-20260209_091643-Meeting Recording**

9 February 2026, 02:16pm

1h 46m 7s

**Val Levitan** started transcription

**Pavel Frolov** 0:11  
K.  
Yes.

**Val Levitan** 0:20  
Over then.

**Aaron Bockelie** 0:39  
Hello guys.

**Val Levitan** 0:41  
Good morning, Aaron.  
Hello.

**Pavel Frolov** 0:42  
Hello.  
Yeah.

**Aaron Bockelie** 0:43  
How you doing?

**Val Levitan** 0:45  
Everybody's doing well. Thank you. And you?  
All good. I hope that you have a good weekend.

**Aaron Bockelie** 0:50  
Fine.  
Yeah, it was busy doors and cleaning and stuff.

**Val Levitan** 1:02  
Well, no composting.

**Aaron Bockelie** 1:04  
Nope, none of that.

**Val Levitan** 1:06  
Right.

**Aaron Bockelie** 1:07  
The winter time.

**Val Levitan** 1:09  
Got you. Nothing to compose.

**Pavel Frolov** 1:10  
Just snow, snow, snow and snow.

**Aaron Bockelie** 1:14  
Or mud.

**Val Levitan** 1:18  
Wichita, I imagine, is very similar climate to Belarus.

**Aaron Bockelie** 1:24  
It probably is in a lot of ways, like it's snowy and icy, but then yesterday it was actually quite warm, but everything was really wet and soppy, so you need to wear boots everywhere, otherwise you'd get gross. And then in a few days it's going to go drop to 20 below Celsius again.

**Val Levitan** 1:41  
Yeah.

**Pavel Frolov** 1:42  
Same in Belarus. Yesterday it was quite, quite warm, I would say minus -4, but today -15 and tomorrow will be -2025.

**Aaron Bockelie** 1:45  
Yeah.  
OK.  
Yeah, I think you definitely have a colder winter here. It'll go to 20 one day and then -20 the next day.

**Pavel Frolov** 2:01  
Sure.

**Aaron Bockelie** 2:08  
So.  
Yeah.  
Anyway, all right. Um.

**Pavel Frolov** 2:15  
Yes.

**Aaron Bockelie** 2:16  
Let's talk about cloud code and how to get going with things a little bit. So Dmitri, you've seen. What have you seen so far?  
Where where is your configuration at right now as well?

**Dzmitry Chudzinau** 2:30  
Talk.

**Pavel Frolov** 2:34  
No.

**Dzmitry Chudzinau** 2:38  
Yeah, it's available to now is a Dechu.

**Pavel Frolov** 2:57  
Uh, divide, divide.

**Dzmitry Chudzinau** 3:03  
Oh.  
No Sunday, my Nastro.

**Pavel Frolov** 3:18  
Log in.

**Dzmitry Chudzinau** 3:25  
Knowledge base.

**Pavel Frolov** 3:29  
Mhm.

**Dzmitry Chudzinau** 3:40  
Uh.  
Is there some more of that show?

**Pavel Frolov** 3:45  
Mhm.  
Mm.  
Sure.

**Dzmitry Chudzinau** 4:23  
Most of.

**Pavel Frolov** 4:25  
OK, I will translate for Aaron. Actually Dima is set up. He's cloud code installed necessary MC PS try to to work. So he's first.

**Val Levitan** 4:34  
OK.

**Aaron Bockelie** 4:39  
OK.

**Pavel Frolov** 4:44  
A feature was to implement Uh.  
Client connect to to the server from the non registered terminal like flex POS.  
Uh.  
Is it?  
Mm-hmm. OK, every every sense that that relates to communication of not registered Flex POS terminal to the server. How to get the keys? How to manage it?  
And Jima described this task was a cloud code set up environment using build with Docker.  
As I assume he fixed everything and now quote quote generated all the code including built or built with.  
Don't care and tests.  
Looks like everything, but right now, yeah.

**Val Levitan** 6:13  
Dima Dima specifically said that he did not allow cloud cloud code to generate code. He did it manually.

**Pavel Frolov** 6:22  
No, no, no, no, no. He he, as I assume code generated.  
Yeah.

**Val Levitan** 6:40  
Oh.  
Cloud code generated code and demos manually looking over to ensure that all dependencies are correct.

**Dzmitry Chudzinau** 6:48  
8.

**Pavel Frolov** 6:52  
Yeah, not not done any pull request yet. Want to check everything.

**Aaron Bockelie** 6:52  
OK.

**Val Levitan** 6:54  
Sorry.

**Aaron Bockelie** 7:01  
Um.

**Pavel Frolov** 7:01  
Um.

**Aaron Bockelie** 7:04  
So, so we don't. It's good to hear this because I don't want to have another yet another session of telling you to type this and that and other thing in a terminal like I don't need to go there. Sounds like, which is good.  
What we should be talking about and and Pavel, I think this is where I need you to help translate this and everybody knows what's going on and I think this is a real fundamental thing that everybody needs to know as we get comfortable with using.  
Coding agents.

**Pavel Frolov** 7:36  
Mhm.

**Aaron Bockelie** 7:37  
It's good to be reviewing the source code manually, right? Like that's a that's good being able to read it and and therefore look at it. On the other hand, it's also a limitation.  
When you have a, when you develop a habit to directly read the source code all the time, it will slow things down a lot. And sometimes it's OK to do this, especially if it's something that's specific or particular. I do it still, you know, I look at a.  
Maybe a database call or something like that. That's really important. It will break everything if it's done wrong, but I also need to tell you that.

**Pavel Frolov** 8:18  
Yes.

**Aaron Bockelie** 8:22  
Given the right sort of structure or framework of thinking, writing it down and describing it kind of thinking, it's very possible to allow these tools to help summarize and catch anything, and in fact catch things that you don't even catch when you're reading the source code directly.  
And all of the tools are actually available for us already. It's just a matter of assembling them in a way that makes sense. So for instance, I work a lot in Python. I use Vulture. Have you ever heard of Python Vulture?  
It's a tool that it's a tool that traverses the abstract syntax tree of Python and looks for dead code blocks and then scores them as either high or low on the scoring of this code is no longer necessary or it's dead or has no route or path, right?

**Pavel Frolov** 9:03  
No.  
Yes.  
Some static analysis for Python.

**Aaron Bockelie** 9:20  
It's a type of static analysis, yeah. And another one might be looking at the overall cyclomatic complexity of the code itself. You guys know what you heard that phrase before.

**Pavel Frolov** 9:33  
Not exactly.

**Aaron Bockelie** 9:35  
OK, so cyclomatic complexity is how many cycles deep does your code go in recursion before it comes back up again, right? So if you have a main function and then it calls somebody and it calls somebody and it calls somebody.  
How many deep is that, right? And some and it's it's not a bad or good that it's deep or wide. It's more of a understanding of what's the shape that you generally want.  
Right. What's a good shape for your thinking to be able to see it? And sometimes the problems have to go outside of the spec and sometimes they end the spec and you're thinking about stuff. Anyway, my point is, is what feels good or bad in that kind of way.  
The issue is, is that feeling how a code works, right? Like, so say you write some function or some piece of software and you're writing through it and you're like, yeah, I like how this reads. It feels simple. It feels obvious, right? Like you kind of.  
You kind of know it. I don't know. I need to get a reading on whether you're running with me or not on this. Does this connect like you? It's emotional almost, right? And then.

**Pavel Frolov** 10:48  
Yeah, yes.

**Aaron Bockelie** 10:54  
You run it and it works great and you move on. You commit it. I like that. The problem is, is coding agents are not emotional, they're just logical. And so the way we substantiate that, the way we have the equivalent of that for a coding agent.  
Is to give it some bounds of tools that can check it and reinforce or deinforce their patterns. So that's linters, that's static analysis, that's testing, that's integration tests, that's all these pieces running as often as you can.  
For when you're operating and doing the doing this work. So in this case, Dmitri, if you wanted to go through all the code by hand, that is perfectly acceptable or you know, go through and read it, but it would be better.  
To build the correct developer experience tools, the linters, the static analysis, the this and the that to cover the entire code base and give access or grant knowledge to.  
The coding agent access to those tools.  
It's never going to fully cover reading the code itself, and so then the remaining mystery in the code that you normally would do by reading the code itself then becomes things like doc strings.  
And also running potentially live debugging analysis and getting output from everything. Like if you have a log level for your code, you can also have it look at these things. The point I'm trying to get at is that it it starts to feel like it's.  
If you were in school and being told the instructor was telling you now do every single thing that normally you would do for the best practice for code, right? Like that often feels too much or too burdensome because we begin to internalize it, right? Like.  
We obviously know we can write comments. We obviously know that we should be running debug and checking the stack and watching the do it the thing. But this activity that we dismiss or assume is now coming back.  
And it's extremely valuable for coding agents because what happens is even if you do all this busy work, this overhead that you used to do, that you'd avoid by hand because you don't need to because you're an experienced developer.  
By bringing it and folding it into the the project, it gives the coding agent the ability to use all this information as context, and it still lets you go several times faster than if you were doing it by hand with your experience.  
And I'm being vague because there's 100 different ways that all three of us could do stuff with code, right? We all have different upbringings in how we manage and deal with this, so they're all different.  
So I'd like to just hear from you guys. Like, what are your thoughts on that? Where do you feel like you have moved beyond the basic, like, oh, we always do that, so it's fine versus no, we have to have a strict practice of executing this.  
Maybe, Pavel, you go 1st and do it in a little bit of English, but mostly Russian and talk to Dmitri about this.

**Dzmitry Chudzinau** 14:30  
Hmm.  
I had a good boy. No, no, I may just commentary in that moment.

**Pavel Frolov** 14:57  
Mhm.  
No.

**Dzmitry Chudzinau** 15:04  
Durst to your spill, but probably trusted. I'm viscose.

**Pavel Frolov** 15:10  
So.

**Dzmitry Chudzinau** 15:11  
What's the specification platform?

**Pavel Frolov** 15:21  
Mhm.

**Dzmitry Chudzinau** 17:01  
Mm.

**Pavel Frolov** 17:08  
Inipitatat is the resolutional.  
Uh.  
So Dima said that it wasn't an intention to to work all the time manually. It was first approach to use cloud code as an.

**Aaron Bockelie** 17:26  
Yeah.

**Pavel Frolov** 17:32  
Main a programmer in the pair. That's why Dima started to to to to see entirely what what is what was what code was produced.

**Aaron Bockelie** 17:37  
Sure, I mean.

**Pavel Frolov** 17:48  
And actually it was quite interesting approach from Dima to give a piece of code that was quite strange, strangely generated to a separate AI that made an estimation that if this approach was correct.

**Aaron Bockelie** 17:48  
OK.

**Pavel Frolov** 18:07  
Probably my approach is better and.  
Open AI said that no, your approach is better than suggested by cloud code.

**Val Levitan** 18:21  
I need.

**Aaron Bockelie** 18:21  
So I think The thing is, is that we need to not discount or throw away our own skilling, but also we need to strike the balance between.

**Val Levitan** 18:32  
Mhm.

**Aaron Bockelie** 18:37  
Perfect hand built code and moving faster. There's a there's some dimensions to this, right?

**Pavel Frolov** 18:44  
Yes.

**Aaron Bockelie** 18:45  
So there is the pride of building perfect code and I think that that's it's nice to see that this is this is like hand built furniture, right? But then there's.  
They're built in a factory by robots. It's also perfectly serviceable and gets the job done and does whatever we need it to do. It's actually more about building it to the spec than it is anything else.  
And I first of all, let me just rewind for a minute and say, Dmitri, it's good to hear that you're just trying it out. And I think it's that if you've never really done it before, you got to start somewhere and that that sounds like a very excellent place to start. Second, we need to be thinking about.

**Val Levitan** 19:26  
I'm sorry.

**Aaron Bockelie** 19:29  
Um.  
What is the specification? Because I think The thing is, is that and I'm going to, I'm going to, I'm creating a little visual image for us here to discuss this for a minute. This is a learning thing is that language model tools like cloud code.  
RA uh.  
They're they're a type of compiler, actually. They're a type of transpiling capability to compile not code, but structured thinking into code.

**Val Levitan** 19:51  
No.  
E.

**Aaron Bockelie** 20:03  
Now.  
When we could write regular code and we compile the code into object code and whatever, we don't go and hand optimize the intermediary objects. We don't. We don't hand optimize the machine code that's created from our from our compiled output, right? We just sort of trust it.  
Check it, measure it a whole bunch of different ways and then.  
Let it ship. In certain aspects we still open up an assembly language tool and we still write language. We still write assembly. We'll still do machine assembly for a particular architecture to make something faster than the than the compiler optimizer can create can do.  
And I think that's the exact same pattern that we're thinking about for tools like Cloud Code. And Dmitri, the fact that you asked another language model to look at and compare the output of the code from one versus the other is also.  
The smart way to do this because you're taking different training sets and and essentially battling them against each other.  
Um.  
Let me see here.  
The.  
Goal then is to actually be curating the specifications form. If we were able to define the specs for the entire product, then writing the code that was generally acceptable but not perfectly optimized would get us.  
Most of the way there to a functional piece of software.  
And now it's actually defining how acceptable is the software. Dmitri, can you put a finger on how acceptable the code is, or is it just a thing you have to look at and decide?

**Pavel Frolov** 22:07  
Aaron, can you please rephrase what should Dima?

**Aaron Bockelie** 22:16  
Absolutely. So let's say that you are putting together.  
A worker or an API server of some kind and you have to have it provide a some sort of interface out to the real world. Let's let's say it's, I don't know, Jason output or something like that.

**Pavel Frolov** 22:40  
Mhm.

**Aaron Bockelie** 22:41  
Would it be acceptable to hard code everything inside of that and make it all a bunch of individual non reusable types or config inside of that and just say yeah it works? Or is it acceptable only to reuse the common interface for all of the workers so you don't duplicate your code? Which one's better?

**Pavel Frolov** 23:03  
Yep, Yep.

**Aaron Bockelie** 23:04  
Obviously the second one, right? Yeah. So how do you define that? Normally you just look at it and you go, well, that's wrong because all these other ones use the same common interface and now this one's not. So I'm not accepting this code until we go and work it into the bigger picture.  
But is that written down anywhere? Where is it defined that that's wrong?  
Because it's functional, it's it does exactly what it's supposed to do, but it's going to devolve into a disaster, right?  
This is the difference between the experience developer and the junior developer. The junior developer says it works, it passes all the tests, ship it.  
The experience developer says, Oh my God, what were you thinking when they say that so?

**Pavel Frolov** 23:56  
Mhm.

**Aaron Bockelie** 23:58  
How? How would? Let me pose this question to both of you. How would you detect, Oh my God, that's not what we were thinking without reading it directly. How? What? What software tools exist to do that?

**Pavel Frolov** 24:19  
No in in my in my understanding if this the code implemented for.

**Dzmitry Chudzinau** 24:19  
Yep.

**Pavel Frolov** 24:29  
Um.  
To do some uh some feature.

**Aaron Bockelie** 24:35  
Mm-hmm.

**Pavel Frolov** 24:37  
Then we need to make step, uh, step back.  
And make some some operations to check how it module will be.  
Injected into common code or micro services infrastructure and so on. So the cloud code need to have some context, separate context.  
To know about other modules, how they behave and how, how, how they communicate to each other, what's the dependencies and so on, and then try to estimate.  
If this code was correctly implemented, or probably it implements the same logic as as previously was implemented by other modules and so on.

**Aaron Bockelie** 25:39  
OK, well that's definitely the the reasoning behind it, but I was also thinking about more specific things like if you were to use Simian or Sonarcube or copy paste detection.  
Things like that inside of the code to do analysis, right?  
So if you if you were to run that every single time you committed code like that would be, that'd be a good check for that, right? And if you ran that as a person, it would get really old really fast because you're constantly doing that. So you would probably script the thing and so it would become.  
Part of an acceptance static analysis, acceptance testing, right?

**Pavel Frolov** 26:25  
Mhm.

**Aaron Bockelie** 26:26  
So if we could say that running this gauntlet, all these tests and checks all the way through every time and could cover the entire code base.  
It would take a long time to create that by hand, right? But it would also help everybody solve the problem when they commit the code. But it would also cause everybody to go really slow. Because imagine what's going to happen. You're going to write some code.  
It needs to be done in an hour or next or tomorrow or soon. Some deadline, right? And it's not passing a couple stubborn tests on the thing. So what do you do? You do slash bypass for those things, right? And he's like, I just got to get this thing.  
Done. I'll write a bug and get to it eventually. And then suddenly your technical debt increases a little notch, a little bit more, and you move on and maybe the QA team will catch it or you'll refactor later, right?  
This is the reason why we don't put all of these extremely comprehensive testing and checks in our code classically in the past historically, because they would cause everybody to grind to a halt. Everybody would stop.  
Because they're trying to erfect their code all the time, yeah.

**Pavel Frolov** 27:47  
Yeah, yeah, you're right.

**Aaron Bockelie** 27:49  
So what we But what we have now is this magic genie that can complete this stuff in minutes.  
And so we actually need to really double down into creating the framework that does all these checks for us.  
And does it in a way that allows us as humans to sort of use it and sort of bypass it. But you can actually write code by hand in a way that says this is how I want it to work. It's not perfect, but it's close. Now, coding agent, understand what I mean.  
And go make it pass all the tests.  
It's like forcing it through the hole and it'll come out perfectly shaped on the other side. And if you have the spec and the quality measures for it, you'll end up with code that's really, really good at the end of this. And that's what I'm encouraging you to to think about from a systems perspective right now.

**Pavel Frolov** 28:41  
Mhm.

**Aaron Bockelie** 28:48  
It's now not really about writing the code directly, it's about creating the tools and dies in the factory to allow the robots to create the code for you.

**Pavel Frolov** 29:00  
And and ideally to use already existent best practices implemented by.

**Aaron Bockelie** 29:05  
Yeah, they already exist. They are already defined. We have and we have 100 things that we can use that already are acceptable and known and and are well engineered and built to do this. We just have to grab them and start using them and incorporate them in our assembly line essentially.  
Uh, let's see here.  
Me. I just realized I really should do this in a bilingual thing.  
So I'm I've got this kind of thing called. It's the language models of the new compiler layer and it's just a little helpful document and just give me one second. I'm going to give it a copy to it.  
Or to you to have this, and I want to spend a few minutes just thinking about this. And then what we're going to do is we're going to talk about tangible next steps in your code base that you can do that move towards this tooling process like this.  
OK, sorry, I'm kind of a little bit. It's a little running a little slow. Sorry, I'm magically translating this thing I created into another language that I would never be able to do myself. So some days it it's magic feels very general.  
Mm.

30:44  
Mhm.

**Dzmitry Chudzinau** 31:42  
MB quota.

**Pavel Frolov** 31:55  
No statistic scandal is at our code at a at a at a service.  
No, besides.

**Dzmitry Chudzinau** 32:10  
Hmm.

**Pavel Frolov** 32:26  
Right here in this pools on you.

**Aaron Bockelie** 32:32  
Dmitri, to be clear, I'm reading into the translation. I'm I'm understanding you're wondering how do we avoid writing a MB worth of code in something and and prevent this sort of anti pattern from a from.

**Dzmitry Chudzinau** 32:35  
Yeah.

**Aaron Bockelie** 32:48  
Growing. Is that what you're asking?

**Dzmitry Chudzinau** 32:49  
Yeah.

**Aaron Bockelie** 32:51  
OK, let me give you an example of what that kind of looks like and how you do that with tooling you build and built into a system.  
So this is the biggest project that I'm working on right now. It's mine, this graph system and what I'm going to do is I'm going to just ask the agent.  
Let's use lint to make our to lint our Let's use make to lint our line counts. What are our biggest offenders?  
This is the line of reasoning right now.  
No.  
Here is our linting of coverage. We're running some make looking at sort of the way this works. This is the full lint output doc string coverage use imports. We're going to kind of find all this here.  
We're looking at the line count of the highest size of these files, the largest of these files. So here's the biggest offenders by line count. 2000 lines, 1900, three thousand, whatever.  
So why would I do this? Well, it's an accepted practice to keep your line countdown, right? We don't want to write monoliths, yeah.

**Pavel Frolov** 34:30  
Yes.

**Aaron Bockelie** 34:30  
Why do we not want to write monoliths?  
Give me a couple of reasons, guys.

**Pavel Frolov** 34:38  
Why not to use some monoliths?

**Aaron Bockelie** 34:40  
Why? Why do we avoid code blocks code monoliths like this?

**Pavel Frolov** 34:46  
Because it's too too difficult to manage this code.

**Aaron Bockelie** 34:49  
Absolutely. Is there anything else besides why it's difficult to manage that we we don't want this? Let's imagine you were a superhero and you could just pick it up and just do it.

**Dzmitry Chudzinau** 35:06  
No, the question. A passion. Slowly. Probably new. Chill a become. Marcinia, most bit of a princip.

**Pavel Frolov** 35:51  
We would grasp the Hoosier robot. It's charms.

**Aaron Bockelie** 35:59  
So I kind of caught the bit of that, Pavel. It's essentially that large files take up lots of context if you're a language model, and large files take up a lot of brain space if you're a human too. It's the same thing.

**Pavel Frolov** 36:03  
Yeah.

**Aaron Bockelie** 36:13  
The same problem. I cannot remember everything going on in a 3000 line block of code. It is me focusing on this one little bit and it becomes really challenging. And if we go too far, if it's a single file for a single function, we have 1000 files in here. It's just as impossible to find things as well.

**Pavel Frolov** 36:14  
Mhm.

**Aaron Bockelie** 36:33  
Right. Like there is a, there is a a ratio where it feels correct for what you're doing.  
And then once you have this ratio of code blocks to files, there's another depth that's this way. So you have you have function count and line count for files, and then you have this way, which is architectural complexity is kind of going this way.  
What is your code even do right? Why is it even doing its thing? And at some point you need to actually take the function or the purpose of that block of code and you set that aside. Now you have a new sort of structure and you have another hierarchy of structure.  
And you can either decide that you're a hierarchal layout of of your entire platform or tool, or you're sort of a interconnected graph layout of your entire tool. It's a bunch of services that do these things and eventually define the purpose.  
So when we start thinking about it in this way and remembering that this is how the entire platform is kind of set up, it allows us to scope in a coding agent to a particular concern and have essentially data contracts for what goes in and out.  
Of of that particular function or that piece of the software.  
And if we can define contractually the data that needs to go in and out, then the language model can follow that to follow the rules. And then furthermore, even lower on the stack is the governance and understanding rules of why.  
That it needs to happen. So here look at this text here.  
Let me zoom in it bigger.  
Biggest offenders Ython, TypeScript, web front end.  
These stand out as horrible offenders. Sorry, Claude. But then what I ask is, do we have any regulatory reasons these should be broken up? I wanted to go into a regulatory perspective as one example of why.  
And so we're actually able to look for the different types of concerns in our patterns. There's nothing in the project's ADRS ways, governance controls, or lint configuration that sets file size or line count thresholds.  
No Max lines per file in a linter config. No architectural decisions about module size. No NIST, O swap, SOC 2 controls and maps files must be under N lines. Therefore, there's no reason that these files can't just grow, right? There's no control for it.  
And the honest answer is there is no regulatory reason. The case for breaking things up is pragmatic maintainability, code review, difficulty, and relevant agent context window efficiency, right?  
So this is implicit right now. Implicit internal. We have to make these explicit external.

**Pavel Frolov** 39:39  
Mhm.

**Aaron Bockelie** 39:49  
If we can make these rules explicit.  
Then you don't have to go through and manually look at all this code, Dmitri. I mean, I'm making a little tiny narrow version of this, but what I'm saying is, is when you make the rules explicit, when I ask when I when I tap on your shoulder, Dmitri, and I say.  
What are you looking over on the code? And you tell me I'm looking for this, that and the other thing, right? They might be specific to this piece of code, but they come from a common understanding of how Dmitri likes code to look.  
And you need to externalize those and make them explicit, because as soon as you do, the coding agent will be helping you look for those things in the code which allows it to you to be the higher level on the stack.  
OK, let me show this.  
Thing here.  
I'll I'll send you a copy while I screen share it too.  
A minute.  
I can't find it. Hang on one second.  
Teams is sometimes rough.  
There we go.  
Let me send this to you.  
You should be able to download it. You can double click it. It's a static web page.  
So I'll do you want to just spend a few minutes reading this so I don't have to blab it?

41:46  
Yes.

**Aaron Bockelie** 42:10  
We're taking your intentions and we're we're able to compile our intentions now, essentially.  
And I want you to ask questions about this if you don't understand what I mean by things like latent space intermediate representation. Do you want me to explain this to you?

**Pavel Frolov** 42:35  
What? What exactly?

**Aaron Bockelie** 42:38  
So the language model. This is the new layer, right? Like let's let's look past the human intent in language model for a minute. OK, imagine the blue area didn't exist. Human intent. The developer knows what the system could do. You.

**Pavel Frolov** 42:40  
Mm-hmm.  
Mhm.

**Aaron Bockelie** 42:53  
You know what the program is? Requirements, conversations, specs. Just like you know your your experience of doing this before. It's ambiguous and it's trapped in here in a lot of places, and it's trapped in emails and trapped in whiteboards and everywhere else, right?  
Before language models, the very first thing you would do is you would take what was trapped in your head in the emails and the conversations as you write source code, right?

**Pavel Frolov** 43:09  
Mhm.

**Aaron Bockelie** 43:21  
And then the source code goes to the compiler, and the compiler goes to the linker, and the linker is ran. The software there is ran on the hardware, right? And we have to consider the whole stack. Dmitri, your concern about memory footprint for code.

**Pavel Frolov** 43:26  
Uh huh.

**Aaron Bockelie** 43:40  
Means that Java byte code, when compiled, physically takes up so much space, and the tighter it is, the better it runs, right? And that turns actually into cost optimization if I have an AWS Lambda function running Java code by byte code.  
It might cost fractions of a cent less over a year's worth of execution and save a lot of money, actually, than to just let it be unoptimized. Yeah, like that's that's your instinct. That's what you learn and that's what you're trying to actually push for.  
And that's way U here at the stack at the human intention. Dmitri's intention is to write good otimized code that doesn't cost a lot to run overtime and is understandable.  
So what we need to do is we can go, well, wait a minute. We have this new technology called language models. They are not really intelligent, but they kind of feel like that sometimes. But what they do is they compile the natural language of intent into source code.  
It's the new source code.  
And So what happens is that we have to now as humans catch up to the fact that we've been bubbled, we've been promoted. We we used to be just, you know, software developers and now we're we're intention developers essentially.  
And we still have to dip into the machine code, the the, the, the source code layer all the time. That's our training for the last 25 years, right? That's where we have our experience at. And so there's a lot of value we contribute to dealing with the source code still.  
But we need to recognize we've been promoted, whether we like it or not. We've been voluntold that these language tools exist now. If we reject these language tools, everybody else is going to just basically use them and you'll be moving slow. You'll be crafting very quality, high quality.  
Quality code in certain areas, but overall you're gonna miss out on the bigger picture. So as soon as we start thinking about that the language model is here, we have to immediately start thinking about how do we adjust our practices to support this model.  
And that's where I was saying about static analysis tools, a continuous integration pipeline, all the tests and checks, all of those tricks that we typically used when things went wrong, when our intuition went sideways and what we thought we did right did not match reality, then we usually bust open.  
In the toolbox and start running the static analysis, start counting the lines of code and start looking for broken stuff using these tools, right? That's kind of the pattern, cuz most of the time we're correct. But in this case, we're gonna not do that. We're literally gonna do that all the time. That toolbox, we're gonna dump it out.  
And integrate it into the assembly line for code for the foreseeable future now.  
This is the big change.  
I know it's a lot of big talk, so you know, I'm just trying to, but what I'm trying to tell you is, is that practically it means begin to develop a higher quality set of developer experience tools.  
Uh.  
Have you?  
Let me find this here.  
I'm gonna put this in the chat. This is just the Wikipedia article on developer experience.  
And I think it's very relevant here because developer experience doesn't tell you what kind of developer it is, it just says developer.  
O when we start considering what a developer experience is.  
Our language model is the developer.  
Also, I don't know if everybody here is old enough to have layed with actual film cameras in the past. Have you? Have you ever used real cameras like not?

**Pavel Frolov** 47:52  
What's?  
Of what camera?

**Aaron Bockelie** 47:57  
Like film, like analog, you know, non-digital. Yeah. Literally the phrase developer to develop the film. It's just one layer and a whole bunch of layers of of work to get to a photograph, yeah.

**Pavel Frolov** 47:58  
Yes, yes, yes, yes.

**Aaron Bockelie** 48:13  
So I'm just using this sort of an as an analogy to think about it. It's just another layer in the system now, and it's always has been when we think of being developers, that's actually what we're doing. We're developing the human intent into code.

**Pavel Frolov** 48:13  
Yeah.

**Aaron Bockelie** 48:30  
And now we're pushing the development onto a language model, and we need to drive what we actually do much stronger, which is the human intent. That's actually what we actually do now. We've been doing it all along. We just didn't have the words for it. Now suddenly we have words because.  
Something not human can do development.

**Pavel Frolov** 48:54  
Yeah, exactly. Actually, several days ago I also.  
Mentioned that yeah, using AI, it's a new approach to to compiling something from from intention, from my intention or from.

**Aaron Bockelie** 49:16  
Mhm.

**Pavel Frolov** 49:21  
Customer intention to produce code, but on the different layer. Yeah, it was mentioned that you just described.

**Aaron Bockelie** 49:31  
Yeah.  
Yep, Yep. And so this pattern then becomes the way we have to think about it. It doesn't mean we have to throw away the old ways. It means we add it on top of everything else we're already doing because like any system or process you build, like a factory, right? Or a assembly line.

**Pavel Frolov** 49:41  
2.

**Aaron Bockelie** 49:54  
To produce product, you still have to remember why it's done that way.

**Pavel Frolov** 49:55  
Mhm.

**Aaron Bockelie** 50:02  
So in the assembly line and whatever products rolling down and there's a stage where it the the thing does something to the product, a little, just a little tweak as it goes along the way. Every single one of those steps is intentional because at some point in the past.

**Pavel Frolov** 50:05  
Is.

**Aaron Bockelie** 50:17  
That's how people did it, or they think about it, or it's a necessary step to get to the outcome. This is also how you think about optimization too. Well, we've always done it this way with these weird little steps. Well, that was because we had human fingers. What if we didn't have human hands anymore? We could do it differently, right? And so this is.  
This is the way to think now, because we're saying we can collapse the amount of time, the bureaucracy it takes to run through a bunch of static analysis, linting and code reviews and everything else, and we can shrink it down to an instantaneous.  
Amount of time. Dmitri, I want to ask you, how did you?  
How did you resent your changes to the code and the proposed changes to the code and review them? What did you specifically actually do?  
Did you copy and paste it into like Gemini or something or to open a or ChatGPT? Or how did you how did you make that work?

**Pavel Frolov** 51:25  
Mhm.

**Dzmitry Chudzinau** 51:26  
Uh.

**Aaron Bockelie** 51:27  
Maybe I'm misunderstanding, but that's what I thought you'd had done earlier is what you're telling me.

**Dzmitry Chudzinau** 51:31  
Can you translate?

**Pavel Frolov** 51:52  
The characters of the wall slow.

**Aaron Bockelie** 51:54  
Is.

**Pavel Frolov** 51:58  
Mhm.

**Aaron Bockelie** 51:58  
It's not necessary. I'm I'm I'm asking how how you did approach it.

**Pavel Frolov** 52:06  
So another priority, United Kusok.  
OK.

**Aaron Bockelie** 52:50  
Could you, could you share your screen for the relevant thing that you were talking about? O you're talking about some sort of multithreading situation you had, so it is what I'm catching, yeah.

**Pavel Frolov** 52:56  
Mhm.

**Dzmitry Chudzinau** 53:00  
One moment.

**Pavel Frolov** 53:06  
Sure.

**Aaron Bockelie** 53:24  
If you're sharing your screen, we don't see it yet, so.

**Dzmitry Chudzinau** 53:32  
Yeah, it's not. It's not going to be, no otherwise problem.

**Aaron Bockelie** 53:37  
OK, now it's.

**Dzmitry Chudzinau** 53:43  
Before, after.

**Pavel Frolov** 53:50  
So the left side is what what was proposed by Claude Court.

**Dzmitry Chudzinau** 53:51  
8.

**Aaron Bockelie** 53:56  
Mhm.

**Dzmitry Chudzinau** 53:58  
This is Human and Chad DPT review.

**Aaron Bockelie** 53:59  
And the right side.  
OK, and and and there's actually a third block, third listing of code that I don't think we have, which is what would you have written if you didn't have either of these to help you?  
How would you have approached this problem?

**Pavel Frolov** 54:23  
Good.

**Dzmitry Chudzinau** 54:26  
Stay pretty real.  
Spring framework.  
Dependency injection of property.

**Aaron Bockelie** 55:16  
So.

**Dzmitry Chudzinau** 55:27  
No, but what? Yes, but what? Prosto bureau shop. It's Proserbuch Kokadori to night, but what today?

**Pavel Frolov** 55:34  
So.  
So originally, originally, as I understand, this post construct was an initial point for Dima to to try to to dig deeper.  
And analyze it.

**Aaron Bockelie** 55:53  
OK, so before before Claude Code had wrote the first line of code.  
What was the pattern? What did the pattern look like in this? I'm assuming you already had something or was this fresh new material for the?

**Pavel Frolov** 56:08  
It's a, it's a fresh, it's a fresh material.

**Dzmitry Chudzinau** 56:10  
Fresh, fresh, not butter.

**Aaron Bockelie** 56:12  
OK. And as I understand as well, you're using Spring framework, yeah? And you're also trying to establish a constructor dependency injection pattern. Is that also right?

**Dzmitry Chudzinau** 56:16  
Yeah, yeah.

**Pavel Frolov** 56:17  
Yes.

**Dzmitry Chudzinau** 56:24  
Yeah, yeah.

**Aaron Bockelie** 56:27  
Have you written that down anywhere?  
Is that written down anywhere in like an architectural decision or anything else like that?

**Pavel Frolov** 56:35  
Uh.

**Dzmitry Chudzinau** 56:38  
Now, oh, oh, Kakadan, more just a beside that ****.

**Pavel Frolov** 56:39  
No.  
Our more, more, more Dima at the at the scrape that is Troy's project. No later is at the file like cloud dot MD.  
Injection of.

**Dzmitry Chudzinau** 57:22  
A.

**Pavel Frolov** 57:23  
Yeah, I think it it looks like.  
Dilemma. Who was the first egg or chicken?  
Because before you start developing, you don't know what will be the result of working with Cloud code. If you already have some projects written in pair programming approach, then you need to what to ask.

**Aaron Bockelie** 57:45  
Yep.

**Pavel Frolov** 57:55  
To develop you you you know what specify in the cloud MD. Please use this, don't use this, use newer libraries and so on and so on.

**Aaron Bockelie** 58:08  
Yeah, it's a moving target, right? Because libraries change and approach changes and things like that. So OK, I am going to point out that what we're discussing here are essentially the architectural decisions for the product.

**Pavel Frolov** 58:11  
Yes.

**Aaron Bockelie** 58:25  
And it's OK to hatch the first egg and have no idea how it's gonna go together, because often we don't, right? We just start throwing some code out there and look, it compiles. Yay, you know, kind of thing until it does what we want it to do. And then we generally will start then writing tests after.  
After we've written code that actually works to follow up with what that is, and then we'll kind of keep growing and stuff. And then before you know it, you got like 3 or 4 developers contributing to it and they're all following the patterns that everybody else did. But there's still no architectural guidance about what's going on, yeah.  
And those this goes on for years. Before you know it, you've got a mostly the herd mentality of coding. It mostly works and it's in the right direction, but it's it's it's only it's very organic in the way it grows, not sort of principled and and tightly.  
Define.  
And what we're talking about now is another aspect of language model coding, which is that it's an amplifier. Yeah. So like, you have your intentions of what you want to do and you say, I want to do this thing.  
And then it's like, cool, I'll do that for you. It looks at everything in the code base and then you end up with literally an amplified version of whatever is already there.  
And it's it's kind of like the evil genie. It did the it did the work for you, but no, not like that. That's kind of kind of like what you end up telling it sometimes. And so you have to back away from it and reguide it again.  
And So what we have to do is we need to step back and think, why is it saying, why do we keep saying no, no, not like that. Why do we keep course correcting it? And that's because the code patterns themselves are incorrect that it's.  
Getting context on predicting the next likely piece of code to create or the intentions that we have written down the the high level thing, you know this new stack layer, right? The human intent is not clear or it's incorrect.  
We've written it down and it and it aged out, right? Maybe a year ago we wrote our intentions down, yeah. And then when you say make me a new thing, it looks on your old intentions written down in the code base somewhere and write something and you're like, no, not like that because the code base is literally too big for any.  
One human to keep in their brain at all times.  
So now we have to start treating the the tracking of intentions as almost another piece of the code base.  
And what I would suggest we do is we start.  
Architecting that as a new part of any software development code base, right?  
So let me.  
Kind of give you an example of the detail that we're looking for. And this is a new thing that I don't. I think it's only really existed since coding agents have really jumped into things. So this is I I at least don't see it a lot.  
We will again use this complex roject to look at it.  
And and don't like think I'm trying to show this as some exemplary piece of software art here. It's just literally just a project that's complicated. So give me one second here.  
OK.  
Can you see this page like I can? I'm scrolling U and down.

**Pavel Frolov** 1:02:18  
Mhm.

**Aaron Bockelie** 1:02:19  
OK, good.

**Dzmitry Chudzinau** 1:02:20  
Yeah.

**Aaron Bockelie** 1:02:21  
I want to go into the documentation and I want to go into the architecture area and I want to show you how the architecture is split up by various concerns for this particular project. Yours will be different.  
Database schemas, authentication, queries, user interfaces, visualization, this thing called vocabulary relationships. Let's go with something simple. Database schema. Simple, right?  
So when we think about the database architecture that we have to have, we have really old ones from a long time ago, 16 numbered really low. We have more modern ones, 201.  
Here's one that's pretty recent in memory graph acceleration extension. This is a Rust based binary that caches in RAM a graph database that is formed from a bunch of SQL queries and presents it for accelerated purposes, right?  
So how did we come up with this? Why are we doing this? We need to define this. So we look at thinking about the benchmarks of possibly what it was. What's the prior art of what we're patterning after? We talk about the decision.  
Why we're making this decision? We talk about the general design of what we do. We're loading all these things, these, these, these edges and nodes into RAM. We define the core design. We then write about triggers.  
To run it, we talk about the SQL interface. We talk about the targets and how we're going to build this and what's what's the actual performance target look like, right? Then we talk about how do we mount it and copy it and and generally describe it, error handling, threading, all that stuff.  
So how did we come up with all this? I sure didn't do it all myself. I had a dialogue with it exploring the specification and intent. My intention started out very simple.  
Database queries against Postgres for graph actions are incredibly slow. I want them to go faster. How do we do this? What does everybody else do? I'm not trying to invent anything new, I'm just literally looking at the entire Internet and going.  
What's better? And then I I develop. I'm not even. I'm a developer still, but you know what I'm doing is I'm not developing code, I'm developing intentions.  
And then I develop my intentions clearer and clearer and clearer and cross-reference it. And I do exactly what you did, Dmitri. I go ask Gemini. Gemini, am I crazy? Does this even make sense? And Gemini? I'll go. It's mostly OK, but this part's really lacking of of thing. You should consider XY and Z. And then I just literally copy and paste that.  
And go, my friend Gemini said this. What do you think, Claude? And Claude goes, that's a really good idea. Let me integrate that in the thing and then I'll take that and I go back to Gemini and go, Gemini, I fixed my stuff. What do you think? Does this address what we're concerned about? And it goes, yeah, but now you did this other thing, so now you gotta fix that. So literally it's like a three-way conversation between.  
Two different agent frameworks and developping an architectural specification about how we're going to do this.  
I haven't written any code yet. Then when it comes time to write the code, then it's essentially create a plan from the architecture. So we read the architectural description. We create a plan, which means a large several sessions of.  
Reading the architectural description, looking at the existing code base and understanding how we're going to weave it into this, and also respecting all the other conventions. No monoliths, or at least try to avoid them.  
Code quality, naming conventions, blah blah blah, all the other stuff we normally do for good well written code. And then finally we get to the point of writing the code and all the code gets written in a pass that takes about 30 minutes.  
Maybe an hour and then we can go through the testing pass and validation and integration checks and everything else. We try it out. Version .1 is now published, right? We use it up. Hey, this is cool. I get some feedback from the humans. Hey, this is good except.

**Pavel Frolov** 1:06:52  
Yes.

**Aaron Bockelie** 1:06:57  
This query is still slow and this one doesn't work either. And then so we just write those as bugs inside of GitHub and we go back and do another pass on it. We do another pass. We have that guidance still as the original guidance to keep us on track about how we're going to do stuff.  
And that's literally the the pattern that you want to start following. Because now, Dmitri, you can still review the code manually, but you can ask questions about what you want to see in that review, and that's going to go really fast. You're not.

**Pavel Frolov** 1:07:18  
Yes.

**Aaron Bockelie** 1:07:32  
Fully relinquishing control of code reviews. Here you're simply saying these are the stated goals of the architectural guidance. The the intentions that I have take my intention file description.  
Take the actual code, make sure they match, and we only can. It's only really viable to do that if you can actually test it. So here's here's the other thing that we do here. Let me.  
Let me just give you an example of what this starts to look like.  
Yeah.  
All right, so if I go into.  
This is that same ADR that I was just talking about, right?  
If I run the benchmark for this, I can literally now run this test code and get actual tangible real numbers running against different tests, right? So here's 5 million nodes for an L system tree generative thing of a graph.  
We're going to try to find the shortest path and the shortest this and the shortest that in this space. This gives me actual repeatable testing to understand the performance targets for this particular way of loading this stuff, but it's not really for me.  
I it's cool. I I like that. I like that it does it. But what it is, is it's a way to cross reference the actual code from a performance perspective to make sense rather than ******** performance. Oh yeah, I just made it up. It just worked like I don't. That's not fair. We can't do that.  
We're going to have real actual test harness for validating it in the ways, because what it really means that my intention was to have a graph accelerator and that test directly supports my intentions. How fast can we make that go? What optimizations can we make?  
If I want to get into it and adjust it by hand, if I want to go write some assembly language or whatever, fine, I can go do that. But I have a baseline I can integrate it against still. So this is actually has nothing to do with language models. Now it just has everything to do with engineering the software and using the correct tests and values.  
Validation and hypothesis for this. This is more about the scientific theory than it is about actually writing software.  
And we're just codifying this into the agent loop.  
Could you could would you be able to share your screen with quad code for the area that you were working like back on that on the on the those two branches you were showing me Dmitri?  
I'd like to ask it a question.  
Start by sharing the screen so I can see the commit hash IDs for them and I'm gonna write up a prompt for you to type in.

**Dzmitry Chudzinau** 1:10:46  
Oh.  
Will you see my screen?

**Aaron Bockelie** 1:10:54  
Yes, I can. Can you go to your IDE for a minute?

**Pavel Frolov** 1:10:54  
Mhm.

**Dzmitry Chudzinau** 1:10:59  
What?

**Aaron Bockelie** 1:10:59  
Where you were comparing you were comparing the code between the two.  
Between the two.

**Dzmitry Chudzinau** 1:11:04  
Oh.

**Aaron Bockelie** 1:11:06  
OK, no, no, no. Make the IDE full screen please.

**Dzmitry Chudzinau** 1:11:07  
OK.

**Aaron Bockelie** 1:11:15  
OK, one second here. I'm gonna just. I need to copy a few things off here.

**Dzmitry Chudzinau** 1:11:32  
I can copy.

**Pavel Frolov** 1:11:33  
She.

**Aaron Bockelie** 1:11:35  
No, no, no. I don't want to do that. We do not want to do it that way.  
I want you to paste that into cloud code.  
And let's see what happens on a new session too, not an existing session.

**Dzmitry Chudzinau** 1:12:33  
What paste?

**Aaron Bockelie** 1:12:34  
I put it into the meeting chat.

**Pavel Frolov** 1:12:35  
Oh, chat too.

**Dzmitry Chudzinau** 1:12:37  
Oh.

**Aaron Bockelie** 1:12:45  
That's, uh, that your wallpaper background. That looks like Turkey.

**Dzmitry Chudzinau** 1:12:47  
Oh, OK.

**Aaron Bockelie** 1:12:49  
OK, so copy that new session. So do not use the existing session, but it should be inside of wherever your that source is at, like wherever the git repo is the the top level branch. OK.

**Pavel Frolov** 1:13:01  
Uh, no, you know that, Chris.

**Dzmitry Chudzinau** 1:13:02  
3.  
OK.

**Aaron Bockelie** 1:13:11  
OK, so.  
And it and is that the git root that directory in there?  
Is that the repo route?

**Pavel Frolov** 1:13:20  
But uh uh route uh to projecta.

**Dzmitry Chudzinau** 1:13:24  
The yes.

**Pavel Frolov** 1:13:25  
Mm-hmm. Yes.

**Aaron Bockelie** 1:13:25  
What branch are you on right now?

**Dzmitry Chudzinau** 1:13:30  
Name branch.

**Aaron Bockelie** 1:13:31  
Is it is the are both branches available in this repo right now?

**Dzmitry Chudzinau** 1:13:46  
No, no dog.

**Aaron Bockelie** 1:13:47  
I saw your diff, yeah.

**Pavel Frolov** 1:13:48  
The the.

**Dzmitry Chudzinau** 1:13:49  
One branch. One branch.

**Aaron Bockelie** 1:13:52  
OK, so I just to be clear, I saw your diff in the IDE. There's a commit here and a commit there and either different commits or same or somewhere, right?  
OK, so go ahead and open Claude, start a new session.  
I want to revise the chat. Just go back to chat and copy it one more time please.  
I no clear that out. I modified the the chat slightly. Can you go recopy it please?  
You just hit escape a few times, it'll clear it in cloud.

**Dzmitry Chudzinau** 1:14:39  
Uh huh.

**Aaron Bockelie** 1:14:42  
OK, so recopy from the chat, paste again.  
Yes.  
OK.  
OK, yes.  
This is what we're doing right here is what I call cross-examination.

**Pavel Frolov** 1:15:57  
Uh.

**Aaron Bockelie** 1:16:02  
All right, let's scroll up a little bit to see how it started. It just at the top. I want to see its its entire summary, so we need to scroll up a little higher.  
OK, stop right there. So here's the comparison. E87 field injection plus post post construct characteristics. OK, Yep. OK, now Scroll down.

**Dzmitry Chudzinau** 1:16:29  
Yeah.

**Aaron Bockelie** 1:16:33  
Why the change?  
Standard spring best practice for several reasons. OK, so now here's where we need to take what we've learned and harvested from this comparison. Because obviously, Dmitri, you have a preference. You have an opinion, yeah?

**Dzmitry Chudzinau** 1:16:52  
Yeah.

**Aaron Bockelie** 1:17:13  
Actually, let me edit this slightly further.  
OK, so now I want you to take that next message I just shared with you and I want you to paste that in there.

**Dzmitry Chudzinau** 1:17:45  
This.

**Aaron Bockelie** 1:17:46  
Yes, please.

**Pavel Frolov** 1:17:47  
You know.

**Aaron Bockelie** 1:18:00  
So do you see what I'm doing is I'm giving it constrained guidance. I'm giving it my intentions. My intentions are I want to just remember this. I want this to be a guiding way that we think about how we do work.  
And I want to memorialize it, right?  
Where should we put the spring coding conventions?  
Docs reference.  
I don't think I would put it in Claude MD because that'll get too big.

**Dzmitry Chudzinau** 1:18:28  
Docs.

**Pavel Frolov** 1:18:34  
Mhm.

**Aaron Bockelie** 1:18:36  
I agree with that.  
O Now we have a spring coding conventions markdown file. Let's open that U after it's done writing it and look and review it.  
So what we've done is.  
Are you guys familiar with the phrase latent space? You know what I mean by that?

**Pavel Frolov** 1:18:59  
No, I guess not.

**Aaron Bockelie** 1:19:02  
OK, so so let me talk about it in direct specificity right now first, then I'll use some other examples. Latent space is that it's very likely that anthropic has trained this model of cloud code on every single book about spring.  
And thousands and thousands of files and projects on that are written with Spring Framework. Yeah, like it's ingested it all. It has slowly adjusted trillions of weights in its neuron space.  
To be able to understand how to redict the next best thing if you use spring.  
But you can't get it back out of it. It's all compressed and sort of representational. Yeah, we call that the latent space.

**Pavel Frolov** 1:19:47  
Mm-hmm.

**Aaron Bockelie** 1:19:51  
All I have to do, Pavel, to invoke something in your latent space in Pavel's brain. It's it's crazy. I can just say this one word and invoke it. I just say composting and then suddenly every conversation that we've talked about in roughly.  
All of the things that you do and all the jokes we've made about it all spring forth from your brain, and I know they do. I can't see it, but I know they do.  
And so when we say Spring Boot at the right time or Spring framework, we activate the latent space to the language model to be good at working with Spring.  
And so this is sort of the same thing here.  
O Now let's look at these conventions. Is this is this acceptable to you? Dmitri? Would you want your code to follow these rules?

**Dzmitry Chudzinau** 1:20:44  
Maybe, yeah.  
8.  
Let's see him in the.  
No, I can't be a convinced.

1:21:13  
Yes.

**Dzmitry Chudzinau** 1:21:17  
Mirror Winston Dart now of a file you but not this my year on the.

**Aaron Bockelie** 1:21:21  
I will send you a link to the documentation, Dmitri.

**Dzmitry Chudzinau** 1:21:39  
Uh.

**Aaron Bockelie** 1:21:40  
I'm going to give you 2 examples of how this actually can fit. Now Dmitri, the 1st is the actual product for cloud code. Look at the skills first.

**Pavel Frolov** 1:21:54  
Mhm.

**Dzmitry Chudzinau** 1:21:56  
Oh.

**Aaron Bockelie** 1:21:57  
Put a spring skill in into place.

**Dzmitry Chudzinau** 1:21:57  
Mhm.

**Aaron Bockelie** 1:22:02  
Right. Structure it in a directory structure however you'd like, because there's probably more than just Spring.  
The 2nd way is this here. This is a little bit more sophisticated and beyond the scope of this meeting today, but I would like to explain how it works at some point soon. Go ahead and click into.  
Performance.  
This is my way of talking about erformance.  
This is different than a skill. A way is the way we do stuff. A skill is a very specific thing that we implement. So in your situation where we just saw that thing about spring, that's most likely.  
A skill adding a skill to Claude to write good spring code.  
This is the way we do it. This is why we do it.  
So in your situation we would have a way of working with Spring because we do this for consistency, for repeatability, for compatibleness with with the other code that we have and so forth. So I could create a Spring way in here.  
To have that as well and then the two complement each other. Now we have between if you go over to the other tab or go back to your go back to the spring convention that was created, the file that was just created.

**Pavel Frolov** 1:23:42  
That's.

**Aaron Bockelie** 1:23:44  
If you read through that, that's a skill. We deal with we we we want to write exception handling like this. We want to write configuration like that. We want to do dependency injection this like this. This is a skill of of skillful application of spring spring conventions.  
And then we have a way that's also related to skills or to to Spring, which is why we use Spring. We use Spring because it simplifies the framework, it offloads the this to that, it does the other thing and the two combos of this.  
Get injected into the context automatically while you're working on stuff.  
So skills get injected semantically matching and then Claude picks up the skill and it says do this to make it work and it gets this information in it the way happens when you tell it hey we need to.  
Code against this particular piece of the software. Here's the ADR. The ADR mentions spring. Maybe you say spring or you say something spring adjacent similar to it, and the way gets injected as well.  
And between those two things, you never had to think about adding these files. They just got added because they were in the in the context space and now it's writing the code according to this.  
Now if we have this here, so let's let's imagine these are our conventions, right? This is the intention. The intent is all written out. Now we can verify the intent with actual static analysis.  
We can look for those injection patterns. We can lint the code. We can find these things and find evidence of them.  
And we can start flagging them.  
And we're establishing the cycle now because the coding agent can run the linting and the static analysis and checks incredibly fast and see all the output instant instantly. The actual time to take static analysis is very quick and you have now steering from intention.  
Rather than in the in the middle of it, trying to read all the code directly.  
And we let existing patterns for support like unit tests, functional tests, integration tests, manual testing, all these things can catch the other pieces that we were missing.  
For certain critical areas, say security or transactions of tokens or things that open ports to the Internet or whatever it might be. For those, you can continue to hand optimize those. You can review them because you are ultimately responsible for all the code that goes out the door, yeah.  
So at the end of the day, certain things will get more scrutiny and certain things will get less. And by abstracting your intentions to written prose rather than fixing it in the code, you free up the time to improve the quality of the areas that you really need to be focusing on more.

**Dzmitry Chudzinau** 1:27:04  
Yeah.

**Aaron Bockelie** 1:27:11  
I know this has been quite the lecture today, so I'm sorry for talking so much, but also.

**Pavel Frolov** 1:27:17  
But now now we know that the second project implemented with cloud code, but with using of some rules.

**Aaron Bockelie** 1:27:18  
This is kind of the direction it has to go.

**Pavel Frolov** 1:27:32  
Will produce rather better quality of code if it were properly, if it was properly documented, I mean added into rules.

**Aaron Bockelie** 1:27:37  
Predictable.  
Yes, so so let me um show you kind of an example of.  
Uh, let's see here.  
This is a pattern that you could easily borrow. I you know the you know the repos out there, so you can just take it. It's it's yours for the taking. If I run ADR, you see this tool it's called ADR.  
Architectural record command line tool.

**Pavel Frolov** 1:28:23  
OK.

**Aaron Bockelie** 1:28:27  
Let's just for just a second, everybody on the call, reminisce how many hours we've spent agonizing over Atlassian frameworks to be able to write down what we want to do.  
It's done a lot of work over the years and it's all trapped over in Confluence and the amount of steps it takes to go from here is the repo that we're literally in with potentially A coding engine to retrieving an architectural decision record from some place.

**Pavel Frolov** 1:28:42  
Mhm.

**Aaron Bockelie** 1:28:56  
There's a lot of steps. If we can reduce it to literally one step, all I have to do is Tye ADR list.  
ADR list.  
Here's my ADRS by group. Now remember, this is text, right? And text is highly compatible with language models. So if I just say, hey, go look at all the ADRS, it's just going to run this tool and look at this and it's going to go ADR.  
Four. Oops, got to do the little thing. ADR 04.  
You.  
So here's the ADR. I'm printing it out and you see how I actually messed up first how I said ADR for usage this error command use this. Use your commands. Literally this output helps the language model figure out what to do. It might mess up on the.  
First try and it's a very small amount of tokens being used and it goes, that's how it works. And for the remainder of the session processing ADRS, it corrects. It's like when you're driving your car, there's kind of like the bigger picture of staying on the lane, but there's the minor corrections.  
The wind blows, there's another car, there's an animal or whatever. You have these minor unconscious corrections that occur during that time, and we're steering the language model agent to just kind of course correct on the fly. There's.  
The bigger picture and then there's the smaller picture O. What we could do is I could invoke this.  
And basically say.  
Come out a little bit.  
Use the docsadr tool to tell me how we optimize graph calls.  
I didn't even give it the right path, but look it, it's making the same call with the same tool.  
And it's finding this and it's reading it and it's viewing it.  
And within only a just a few tool calls has exactly told me why the architectural decisions exist for erformance for this.  
It's extremely focused and won't deviate and make **** U because it doesn't have to look at all the code and go through all the steps. Here's why.  
So we've got things about parallelization, we've got matching things, we've got graph acceleration and everything else like that. And so that's kind of the.  
The purpose of this. So what I want you to do, Dmitri, is think about how we got with those prompts that I just, you know that we did the first one, which is I have a file here, can you compare it? And the second prompt was I want to learn from this. Let's put together generally acceptable rules.  
Think of them like an investigation. I'm going to write these words in English. I need help. Maybe we can move them to Russian as well, but cross reference.  
Crosscheck and um.  
Cross-examine those three activities is a way to audit or understand how you're doing something. There's is there a Russian version of these that makes sense?  
I'm relying on you, Pavel, a little bit.

**Pavel Frolov** 1:32:48  
If.  
Highly likely. In Russian we use something like cross reference.

**Dzmitry Chudzinau** 1:32:56  
Yeah.

**Aaron Bockelie** 1:32:56  
Yeah.  
So, so there's not really a a a Russian word for that.

**Pavel Frolov** 1:33:03  
Yes.

**Aaron Bockelie** 1:33:07  
If I ask Claude Claude to describe this, let's see what it comes with. I'm curious.

**Pavel Frolov** 1:33:12  
Yes.

**Aaron Bockelie** 1:33:22  
Here's what it's saying and I'm glad that it kind of went into a legal perspective because it is in a lot of ways to cross examine something is to look at it.  
And this is this is what you should be doing to develop your understanding, your intention to grow it. OK, so if you can grow your intentions of how you want your code to look, they become the reference for the architecture. They become the reference.  
For how you do things, if Spring is a very important part of the platform, which I believe it is, you ought to have some written conventions for how Spring is supposed to work.  
And if you have them written down now, everybody, human and AI, can agree to them.  
And if you have them written down, you have the the the foundation upon which all tests can be written.  
So if you have software testing unit tests.  
How do we, how do we test the new piece of software? What's one of the aspects? Well, actually Dmitri wrote all of these way we actually want to code our code and we can write our test to verify that.  
And now, if you've got the baseline of what you're doing, you don't have to write them all by hand either. You define all this and you say, hey Claude, I want to write unit tests for this piece of software. This is my way that I like to have spring written. Can we make sure that we can test?  
All that, and there's a bunch of ways to introspect the code to be able to do that.

**Pavel Frolov** 1:35:05  
Yes.

**Aaron Bockelie** 1:35:10  
So I think that if if you could, you guys could work together to kind of define some baseline conventions of how you want the code to be written, commit that into the docs.  
Use that to create a little whole bubble of static analysis, test definitions, architecture, reference all the way back around to itself. Just pick one small concern and kind of work on that.  
And I think you're going to find is is that you can use that as a point to grow, because now you have this this complete cycle for that piece of the code. But if it's how you want it to work, you're going to take the pattern, the meta pattern, the pattern of the pattern.  
And alley it to all the other parts of the of the repo now too.  
This means that you can say, hey, you know, for this other thing that has zero guidance, let's take these patterns here and transpose them over there, and you can begin to align the entire repository into having your well-grounded intentions.  
When can we meet again to kinda maybe?  
I mean, do you think you have this? Do you need help with setting up the tools more? Is it clear?

**Dzmitry Chudzinau** 1:36:42  
Dove should find out.

**Aaron Bockelie** 1:36:44  
Does it feel a little weird to talk about codebase this way? Because it does to me still.  
But it works and that's the thing that I'm finding.

**Pavel Frolov** 1:36:58  
I think quite quite useful to have one more layer of abstraction.

**Aaron Bockelie** 1:37:04  
Yeah.  
We think of ourselves as develoers of intention rather than develoers of code.

**Pavel Frolov** 1:37:12  
Mhm.

**Aaron Bockelie** 1:37:14  
And where there is no, there is not enough evidence of intention. Then we fall down one layer and we have to write the code manually, and we don't want to be there. That's an uncomfortable place to be now. So we figure out how to define our intentions and get back up to that upper layer again.  
Any last thoughts? We're just a few minutes towards the end of the hour here.  
That was a lot. You guys look worn out and bewildered from an entire day of work, so I sorry for keeping you so late.

**Pavel Frolov** 1:37:57  
So I think just need to to agree on undertakings and define the next meeting day.

**Aaron Bockelie** 1:38:10  
Documentation, developer experience, tooling, static analysis in some way to verify your intentions.  
Yeah, I think that's essentially it. If you want to adopt the Waze system I have for cloud code, make sure that's working well. I'm updating it constantly and kind of improving it as I go.  
Doesn't mean you have to grab it every day, but just, you know, start running that tool as yours.

**Pavel Frolov** 1:38:42  
Mhm.

**Aaron Bockelie** 1:38:44  
Start looking into, yeah.

**Pavel Frolov** 1:38:45  
OK.  
Solar.

**Aaron Bockelie** 1:38:48  
Think about making tools that work from a command line for code coding agents.  
Good Val.

**Val Levitan** 1:38:56  
So, Pavel, from a corporate perspective.  
The instructions to my consultants.  
Is to allow me an executive to put to put out my tentacles.  
Sure.  
Into everybody's developer and graphic designer's GitHub.  
And to provide me with a summary on a daily basis of.  
Uh.  
Each person's.  
Uh, productivity.  
It's not going to happen overnight, but this is where we're going.  
And so imagine that there will be an intelligent system sitting on top of it with lines extending to each GitHub.  
For each developer.  
And providing intelligent information. That information I am making available to you.  
So it's not my exclusive thing. You know, I'm going to, I'm not, I'm not going to hold it and not let you see it. I'm building it for the company so I can step aside while the company is functioning.  
And so.  
This will be your panels, your intelligence center.

**Pavel Frolov** 1:40:46  
Mhm.

**Val Levitan** 1:40:50  
And you will be. I am going to make you responsible for that.

**Pavel Frolov** 1:40:58  
OK, let's let's try to build the system.

**Val Levitan** 1:41:03  
So this is this is your intelligence center.  
I will look at it, but I will never be able to own it to the extent that I want you to own it.  
So these meetings are aimed at providing this information center to you and so how you build it with the developers and how you extend your intelligent.  
Intelligence tentacles out.  
Is really going to be the result of the information you're getting.  
Technologically, we already know that it's possible. That's no longer a future. It's today. We know that it's possible today, and we know that companies already work that way.  
It's just not JVL.  
So every meeting, every meeting that Aaron is occupied with teaching the developers how to organize their GitHub and their.  
Productivity centers are aimed to improve your intelligence flow.  
Information.  
That means these have to be your meetings benefiting the entire company and you specifically, and so you have to schedule them. You have to make sure that they're efficient, make sure that after the meeting is over.  
You understand what needs to be done and you continuously speak to the developers in instituting those items that we agreed in the meeting. It's not my meetings, it's not Aaron's meetings.  
It's your meetings. You need to take ownership of these meetings. You need to line up your calendar with the developers. You need to shrink these meetings to hopefully half an hour.  
Today it was an hour and 45 minutes. Those are the first meetings that Aaron talks about. We need to cut it off. We need to get it to half an hour, squeeze it to half an hour. Very, very productive information and move on.  
Next developer, Next developer. You also have to identify your leaders.  
For example, Haretsky is showing you a lot of interest in it. Fantastic. Embrace him.  
I don't know if he's the right guy or not. Maybe not. I have no idea. But you need to identify one or two leaders.

**Pavel Frolov** 1:44:10  
Mhm.

**Aaron Bockelie** 1:44:10  
Can I? I want to add a just a little bit of direction to what you're saying, Val.  
I'm trying to teach why it is and how it works and lead through the concepts. This is a very expensive endeavor to do it this way. I'm conveying it to you guys.

**Pavel Frolov** 1:44:21  
Yes.

**Aaron Bockelie** 1:44:29  
The sooner you can sort of reproduce what I'm saying and essentially say and believe what I'm saying or your own flavour of it, now you can codify all of this in literally and get repos in ways of work in examples that you own and so forth.  
And one of the really amazing superpowers of this whole loop that we've got now is that you can use the very system that you build to teach the people how to use as well. If you've got it defined, you can literally set up a program to have people be led through it with the.  
AI tool to teach them themselves.

**Val Levitan** 1:45:10  
I don't know if you guys read an announcement. Probably you didn't read an announcement by Goldman Sachs. Do you know who Goldman Sachs is?  
Yes.

**Aaron Bockelie** 1:45:23  
I get my paycheck from Goldman Sachs. One of my paychecks.

**Val Levitan** 1:45:23  
Goldmark.  
Gold Goldman Goldman Sachs is probably the leading investment banker in the world.  
Every large deal investment deal comes through Goldman Sachs.  
Tim, I'm explaining to you specifically. Do you know what investment banker is?

**Dzmitry Chudzinau** 1:45:44  
So.

**Val Levitan** 1:45:50  
When I come.

**Aaron Bockelie** 1:45:50  
I've actually got a run, Val. I got. I have another call I gotta jump on. See you guys.

**Val Levitan** 1:45:55  
For the company, when a company, when a company raises money.

**Pavel Frolov** 1:45:55  
Thank you. Bye.

**Dzmitry Chudzinau** 1:45:58  
Bye.

**Val Levitan** 1:46:03  
Stop the recording.

**Val Levitan** stopped transcription