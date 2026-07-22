**Introduction to Knowledge Graph Tool-20260202_100057-Meeting Recording**

2 February 2026, 03:00pm

55m 29s

**Val Levitan** started transcription

**Val Levitan** 0:03  
OK, the floor is yours, Aaron.

**Aaron Bockelie** 0:03  
How are you doing?  
Yeah.  
So, um, today's topic is uh.  
Discussing and introducing a platform that I've been building for a while now, and I want you guys to attempt to run it. Not necessarily direct. It's not going to be ready to go on the first try. Don't expect it to be.  
Perfect. It's good enough right now and I need to get you guys to run it because I believe there's going to be a lot of value in using this type of tool to do knowledge management.  
Knowledge understanding and data understanding. And what I mean by this is that.  
Language models like BOD in our tools or other things are OK at holding on to data. So like you can use the built-in history data inside of the desktop application or you have a whole bunch of files.  
In a directory and you say go search these files, right? That can happen. Or you have a bunch of complex ideas, things written down and it is.  
Tough to go through all of them because there could be hundreds of ideas or thousands of ideas, right? And they're all connected and mean different things to each other. And so with this platform I'm going to show you and you can just download it and deploy it pretty quickly.  
Gives reasoning, conceptual reasoning as a as a as a service. Essentially it is. It is considered a reasoning as a service sort of category of system. It is a thing that actually exists.  
So you know when you're using ChatGPT or Claude and it shows the thinking steps, like I'm going to think this and then that and then you can see it talk through its thinking, right?  
So this is a system that provides additional thinking on top of that, and so I'll just start with a demo of kind of what it actually looks like when you use it first of all.  
And then we'll get into the details of of kind of how it works here.

**Val Levitan** 2:36  
Just maybe explain what what became a catalyst for the design of this thing.

**Aaron Bockelie** 2:42  
Sure. Yeah, that's a good point. So Val, as we all know, loves to keep meticulous notes on his conversations, right? You know what the word meticulous means, right? So yeah, and he has hundreds and hundreds and hundreds of of of transcripts.

**Val Levitan** 2:54  
Detailed.

**Aaron Bockelie** 3:01  
And they're all ordered by essentially when they happen, date and time.  
He has a bunch of problems where during a particular meeting there might be three or four different topics that have to go through, just because it's the nature of reality is, is that we don't talk about one thing and trying to quantify or classify where that stuff should go.  
Is challenging and actually just turns all of the transcripts into transcript soup. The the soup is impossible to understand when you start breaking it up.  
So this turned into using the Obsidian platform, Obsidian MCP, and it works very well for what what he's got. Obsidian. Have you guys used that at all now? Have you seen how that works?

**Dmitri Kovalchuk** 4:02  
I didn't use it.

**Aaron Bockelie** 4:02  
Foundry.

**Andrei Bosik** 4:03  
Yes, I know about Obsidian. I use this.

**Aaron Bockelie** 4:06  
OK.  
And you understand how Obsidian can show relationships between documents if you put labels and tags and things into the documents, right? OK, so if we think about Obsidian showing the graph of relationships at the document level.

**Andrei Bosik** 4:15  
Yeah, yes.

**Aaron Bockelie** 4:24  
This system can show the graph of relationships between documents at the concept level.  
So if you think about a transcript or several people are talking and they talk about a whole bunch of different stuff, each of the things they talk about is a concept. And so like this conversation we're having right now that's being transcribed, when we're done, it's going to have multiple concepts I'm going to be talking.  
Talking about Val's documents, I'm going to talk about the graph, I'm gonna talk about obsidian, we're gonna talk about deployment and so forth. These concepts, right? And more importantly is that we talk about these concepts multiple times throughout the document or throughout the conversation.

**Dmitri Kovalchuk** 5:00  
Mhm.

**Aaron Bockelie** 5:08  
So already I've just referenced Obsidian twice, and then by just saying it just now, I said it a third time. You see what I mean? What's going on here? Like as I'm actually talking, this is happening.  
So this gets recorded in the transcription. The transcription is the reality of what actually was said.  
And it's written down. It's immutable. It's like it's the truth. And So what we want to do is extract that out of that.

**Andrei Bosik** 5:33  
Mhm.

**Aaron Bockelie** 5:37  
Assemble it in such a way that has relationship. D duplicate it so it doesn't keep creating multiple documents about obsidian. Instead just sort of pushes it all together into this thing called obsidian in this conversation.  
So that's what this platform basically does, but at a very large scale, hundreds or thousands of documents that can be put together to then classify all sorts of information everywhere.  
So what we'll do is I'm going to start with just the Claude MCP view of this rather than the user interface and anything else, and I think that'll really help get an understanding of kind of what it does and why.  
One second here.

**Andrei Bosik** 6:24  
And finally document store in Obsidian.

**Aaron Bockelie** 6:25  
Yeah.  
It can actually work with Obsidian, so it's very interesting how this whole thing goes together. We'll we'll get through what we can in the architecture to read you into this because nobody's seen this yet. This is something that is never existed this way.  
So we'll see what happens. So here we are in Cloud Desktop and we can see the connectors. I have one called Knowledge Graph turned on right now. That's the connector that it's called right now and in the Knowledge Graph I have loaded.

**Andrei Bosik** 6:50  
Or desktop.  
Mhm.

**Aaron Bockelie** 7:02  
You know the ways from the cloud code config that I talked about last week? Remember that?  
All the the Waze documents.  
I loaded all the ways. I don't know if you remember. So I took all of those ways, those files and loaded them into the graph system. I also took a whole discussion about operating the the the enterprise as a graph and some other conceptual ideas too.

**Andrei Bosik** 7:13  
Uh, yeah, yeah, yeah, yeah.

**Aaron Bockelie** 7:32  
And so all this stuff is now loaded into the system now and allows us to essentially query this graph. Now I will caution I am actively like literally right now.  
Vodcode is editing the system we're going to connect to, so it could crash or break, but if it does, just give me a second and I can get it going. But I should be OK.  
I'm going to start with a simple question. We organize the.  
We organize the data inside of the graph data store as what we call ontologies.  
So we can see that we have an ontology called first principles.  
And we have an ontology called Hooks and Ways. So the first principles is these big books that I've written on things. There's two big documents. The 2nd is literally all the hooks and ways from cloud code that I had talked about, and these ones are actual tests that I made.  
Or testing the software. So it's actually these are irrelevant right now. So what I'm going to do is I'm going to ask it.  
Uh, let's see how the.  
I'm going to ask this question now. This is going to feel like a kind of an abstract question. I'm going to say, can you tell me how the code review way might be supported by the graph as an operating model? And the reason I asked that question is because I know what's in this data right now.  
We have a code review way that you've seen it. It's a file that's in there. And then there's another thing that's graph is an operating model for the enterprise.  
Is a large idea or set of concepts that you can run a business through a graph representation. Anyway, I'm just going to show you what happens to the MCP server when it does this. So we can see it's going to start with a search.  
Hopefully.  
So we can see it's looking for code review way.  
You way.  
I may need to pause another thing here in just a minute.  
So, OK, so on the second one, it looked for code review and it found a response. It said it found 10 concepts and it found these ideas and they're connected in particular ways. So we don't have to really look at all this. I'm just letting it load all of this stuff. So it's making these queries.  
It's traversing the graph. It's it's like a think about like a subway station or train routes, right? You're at this train station, this city, and you need to get to that city, and there's a bunch of paths and trains that you have to take between the two points to connect the dots.

**Andrei Bosik** 10:48  
Mhm, yeah.

**Aaron Bockelie** 10:50  
This is doing this thinking for us inside of it, and it's a little slow right now because I'm literally developing it as we're talking here. But be patient. It'll get finished here, hopefully.  
O Now it's kind of looking at the individual pieces of information about this.  
So it's it's like in a way it is a type of data graph rag. It's like a rag retrieval, but way different than a normal rag retrieval so.

**Andrei Bosik** 11:35  
Uh, what uh this graph use as a data store?

**Aaron Bockelie** 11:40  
It uses uh Postgres.  
And custom extensions and a graph extension.

**Andrei Bosik** 11:45  
Mhm.

**Aaron Bockelie** 11:49  
So currently we're we're using what's called Apache Age.  
No.  
Let me send you a link to that.  
And let me also, while this is running, I'm apologize it's taking so long right now, but I I'm letting benchmark tests run at the same time and I can't stop them without breaking a lot of things. So just give me one minute here.  
This is the link to the repo for the project itself.

**Andrei Bosik** 12:29  
Uh-huh. Thank you.

**Aaron Bockelie** 12:33  
I would recommend just working off of this repo path because basically it has ready to go docker images and everything else to install. If you try to fork this you'll be immediately out of date on things, so just use it from the repo for now.  
Um.  
Let's see here.  
Back while that's running.  
I'm going to walk through this just slightly.  
You can see me looking.  
In here, right. OK, so cloud's done in the meantime, so we'll just, we'll just, I'll just show you this for a minute. So in this case, it's actually quite straightforward to deploy. There are two different deployment patterns that you have to have. The first one is to install the back end.  
And it has an installer right here and then the other one is the front end, the client and the tools and that's this installer right here. The client and the tools can be installed in a different machine than the back end. They don't have to be on each other.  
So the front end has a command line toolkit and an MCP server and a Fuse driver. I'll talk about Fuse driver in a minute. The back end has several containers that it that are custom to this platform.  
A web container, the API container, an operator container. It also pulls down a storage container like S3 style storage container and it also pulls down the Apache container. So the back end platform consists of five.  
Docker containers that run with an orchestrated environment.  
My guess is for your testing you probably want to set up a a virtual machine running probably Debian.  
Ubuntu something like that or Arch Linux, whichever one you prefer. I use Arch in my environment, but you know, yeah, whatever you want to do and then instantiate the back end platform and only put this on the back end platform.

**Andrei Bosik** 14:38  
Mhm, mhm.  
No, I like DBM.

**Aaron Bockelie** 14:54  
The back end platform and we can on another session I can we can sit together and talk through the installation steps for it. It has a full installer system that can set up certificates and everything else too. So just depends on how you have your. I don't know what you're.  
Your SSL infrastructures like or how you do DNS and anything else like that, but you can set it up so it can be correctly domain have have a valid domain name inserts and things like that once.  
The back end is deployed. It has user management, Oauth roles, RBAC permissions, all this other stuff in it.  
Um, so let's just go back to Cloud Desktop for a minute because it's complete.  
So here's the response. This is a really rich question, and the graph has a lot to say about it, though it's worth noting up front there isn't a single concept literally named the code review way. Instead, code review surfaces is a recurring structural pattern that connects several concepts across the hooks and ways.  
And the first principles ontologies. The picture that emerges is more interesting than a single way would be.  
So the code review is a micro practice and it talks about this and it talks about how we understand code review as enterprise governance. So this is essentially getting more out of the data than actually exists in the data because the graph is able to assemble a bunch of relational information.  
That is not really coded in any one of those documents, but as the graph ingests this information, we begin to see more of what's happening in this. So it's a.  
Has a lot of emergent properties from a A I systems, a machine intelligence system, and we want to be able to leverage those emergent properties surfacing through a tool like or another A I language model tool.  
Is there any questions about what you're seeing in this response here right now? Like, how did you understand how it came up to this opinion?

**Dmitri Kovalchuk** 17:19  
To show to us how we can read information, but how we can upload our knowledge.

**Andrei Bosik** 17:19  
Visual, but they're not.

**Aaron Bockelie** 17:26  
Absolutely. That's an excellent question. There are multiple ways to do it. First is you can just ask Claude to do it for you. It can actually create new things and it can just write them and store them. So you could just say, so actually let's do this.

**Andrei Bosik** 17:26  
Yes, I have the same questions.

**Aaron Bockelie** 17:42  
So you mentioned first principles, right?  
I can say something like this.  
So basically what I'm telling Claude is this is interesting. You found that these things tell a story. Where could we store this at? This isn't really a first principle. Maybe it's something else. Can you go ahead and do this for me? I'm not gonna let it try anything particular. I'm not gonna.  
Tell it what to do. I'm gonna let it figure it out. So what it's gonna do is it's going to write a new document and it's going to push it back into the graph. And as soon as it pushes it into the graph, these concepts will attach to the graph in various ways and connect together.  
To be able to understand we're building new learning from this by by bringing this together.  
O It's now going to create the ontology, a new ontology.  
This is good. The ontology is created. Now let me create the concept and edges. I'll batch this with a queue action. So in this case it's going to deliberately create several actions rather than do a general upload.  
We can see it's creating these connectors. It's it's thinking and learning something new by doing this. It's creating these ideas here and storing them.  
And after it's done doing this, we're going to go switch to a different viewpoint that shows kind of the web perspective view of this.  
And says done. Now here's what exists in the graph. A new ontology called emergent patterns, new concepts, code review as recursive governance and connects a bunch of things together. So we're going to stop this view for a minute and I'm going to open.  
What is the Web Workstation version of this thing? I'll show you the Web Workstation, then I'll show you the command line version, OK?

20:36  
Yeah.

**Aaron Bockelie** 20:44  
So I'm just going to I'm running this local host without a valid a URL because this is a development environment. Can you see the the interface right now?

**Andrei Bosik** 20:56  
Yeah.

**Aaron Bockelie** 20:57  
OK, let me um.  
Back to this normal view. So we can see that there is some relationships in the environment. We then have some other there's there's. I'm building some other tools here, but there's essentially a searching tool.  
There's a query editing tool. There's a ingest tool. So this allows us to drag files. We can just drag a file right into here into an existing ontology. So here's the new first principles ontology, for example.  
Here's one called emergent or I'm sorry, emergent patterns with one concept in here, first principles and so forth. We can see the jobs that have ran over time for ingestion of jobs. Remember this is a dev environment, so it looks a little weird.  
We can get reports on information that might have been discussed.  
And then under administration we have our Oauth clients, we have users.  
And their clients attached to them. We have role management, so we can manage our roles. We have the system kind of environment that shows various graph metrics and things of that nature. So we're gonna go look at this idea.  
Of this one concept, so I'm going to find this as.  
I'm going to search for a thing called code review. Code review.  
Maybe.  
Yeah, it's going to be a little slow, so pardon me for a minute. I'm in the middle of doing this performance refactor, so it's a little slow. So we see code review as recursive governance. That's the thing that was just created, concept just created by that. We'll open this.  
And we're going to load this into the graph and we can see that it's just got a single item here, right?  
It has a bunch of relationship's though right here. See it.  
O Let's start a new query.  
Give me a minute.  
I'm going to load 3 hops into the graph.  
And so we can see when we look at the way graph, there's a bunch of relationships with each other and we look at the way we have the same concept with details, but we have a lot of relationships, enterprise offering, operating model.  
Just in time, guidance, all sorts of other stuff. This map or web of knowledge becomes complex quickly because knowledge is complex and what we can then do is we can see how different things can come together for systems and tools.  
O Now when I'm looking at this as just a workstation view, it's very, very limited. It's like looking through a little tiny tube because I can only look at certain things. This is for people to introspect this so we can see this how?  
Different information, see how the relationships between contains and enhances and so forth. These all are about the way of doing things. That's because that's from those documents that I uploaded. We can see this in a three-dimensional view if we want to because it's kind of helpful sometimes to see it.  
In a more sort of, you know, different way, but we can also still understand and view this.  
And then finally we can do other things like this is like I said, this is a workstation for kind of introspecting. It's not the main tool. This is like a diagnostics of your knowledge, right? This is understanding why your knowledge is shaped the way it is on things.  
So we can look at for instance the edges of connections, the what happened here. So this is unfortunately English language based right now. I haven't built this for Russian or other languages, but it should work similarly. So what we can think about is around this.  
Circle of these edges here is different major ways things are structured in knowledge. Think about how and I say this causes that right. The word causes is a very specific word if I say evidence.  
That's a very specific word as well. If I say modifies, modifies is different than causes, right? Causes just make something happen. Modifies changes something and so these these words and things.  
Can can mean different things and this is a way to understand the relationship between these different concepts that are existing in this graph right now. And as this graph grows, these this data becomes richer and richer when we look at the embedding landscape for what this starts to look like.  
We start to see a set of relationships of regions of information for this. We can see that first principles is generally in this side of the graph. We can see the hooks and ways is generally over here on this side of the graph, but there is some overlap.  
More of the hooks and ways into first principles rather than first principles into hooks and ways. So we can kind of visualize how this looks and kind of get an idea and we can always highlight over something. And then finally going back to thinking about tracing paths for a minute.  
We can sort of look for a connection between things O we can say I want to look for things like olicy.  
I'm going to search for olicy first hoefully.  
The other tools are now on the accelerated model, so the web workstation is very slow still right now. So I'm going to look at policy layer and then I'm going to connect to the other end of it, which is going to be governance.  
So just the same as I'm searching for these terms, Val could search for flex pay IT operations as one thing and market monetization as another thing, right? And then he would be able to connect the dots and see how things go together.  
And see that O what we're going to do is we're going to load this path.  
Give it a minute O we're going to find this. You see how it's now found five paths with three hops, olicy layer to documentation to governance interpretation. O we're going to load this into a clean graph.  
So now what we can see here is the see if we can. It may not have loaded this into the graph properly. Just a minute.

**Val Levitan** 28:25  
Yeah.

**Aaron Bockelie** 28:28  
So obviously I'm I'm the only developer on this, so it's a little bit, you know, and that's actually something I would hope you you can do is you can use cloud code and other tools to to.  
Sort of imrove this when you find things. Let's try this again O we're going to look for governance.

**Andrei Bosik** 28:47  
It's work on CPU or GPU?

**Aaron Bockelie** 28:50  
Both. It supports both.  
Um.

**Dmitri Kovalchuk** 28:56  
Uh, currently you use SPU or GPU or both?

**Andrei Bosik** 28:56  
No good.

**Aaron Bockelie** 29:01  
So it it does not require a GPU, but if you want to have a GPU accelerate some of the the work you can.  
Oh.

**Andrei Bosik** 29:13  
But now it's working CPU only.

**Aaron Bockelie** 29:16  
But in this case, right, what you're seeing right now is CPU only, just because of some of the work I'm doing. It doesn't really make a huge difference. Honestly, the size of the models that it uses internally are.

**Andrei Bosik** 29:19  
Oh.

**Aaron Bockelie** 29:32  
Pretty small and then for most of the inference it uses either anthropic or open a I API calls to for the intelligence. It does also support a local Ollama compatible inference, so if you do want to run it fully on local infrastructure never leaving, you can do that too.

**Andrei Bosik** 29:42  
Mhm.

**Aaron Bockelie** 29:54  
Let me.  
Try to load this path here.  
OK, so I've got some problems with loading things right now, so don't worry about that too much.  
So let's go to finally the command line.  
9.  
So.  
It's just called KG as the command line, and then the command line lets you have a lot of different things to control it with. So for instance, if I were to do KG search query ways.  
I would get that same query, right? Here's the way. Here's the evidence.  
If I were to.  
Worry.  
So I'm going to ask to connect two concepts together, ways and governance.  
Right now it's running that query against the graph and what we see is several paths found five paths.  
The first one is way appears in the documentation and enables governance interpretation. The 2nd path connecting ways to governance is.  
Away appears in the documentation, enables governance interpretation and then so forth. So way goes to skills, goes to governance interpretation, way goes to ontology, goes to this.  
Basically, it's thinking about different ways these things connect to each other, and this data can be many different types of data. So just as seeing abstract sort of governance and thinking about how to do work.  
Problems. You could load every single commit message from a git repo into the system and it would dissect all of the commit messages, understanding why they were connected and what they did for every single pull request could be put into this.  
Or the entire documentation set for a project to be put into this and it would be able to reason out how it all connects to each other.  
Anyway, that's essentially what it does.  
So it's it's a general purpose knowledge.  
System that self regulates how the information is connected to each other. Oh, I forgot to show you the fuse driver. Just a minute.  
Uh.  
On it.  
I just need to reinstall the client, so I've been working on this essentially.  
A lot, like many, many hours recently trying to get this to a point to where it's usable for you. Um.  
Any questions so far while I'm getting this fixed up? Any questions so far on what you're seeing?

**Andrei Bosik** 34:18  
Yes, you say you have role budget access control on this product. This mean different users can use one this service.

**Aaron Bockelie** 34:26  
Yes.  
Yes.

**Andrei Bosik** 34:35  
You have authorization forum on this solutions, yes.  
OK. And next questions, I think it's working Docker, yeah.

**Aaron Bockelie** 34:49  
Yes.

**Andrei Bosik** 34:51  
And if I create a new virtual machine for example to set up uh this uh.  
To uh, I need to install Docker in this machine and then run uh your scripts to install. OK can start.

**Aaron Bockelie** 35:04  
Correct.  
OK.  
Right, so So what you can do is to start with you could install the back end on this virtual machine, then you could simply install the front end on this same virtual machine. So you have the back end and front end right there the the KG command line tool, right?

**Andrei Bosik** 35:26  
Mhm.  
Yeah.

**Aaron Bockelie** 35:29  
Once you've got that set up, the next thing I would do is from your local workstation, I'd log in via the web workstation into it, the web interface, and then from there you can use most of it from the web interface. This is typically how I would expect Val to kind of use.  
It to begin with is he'll have the web interface. The next thing I expect probably that needs to happen is an MCP server needs to be set up. So essentially Val can use Cloud desktop with it or cloud code and it can manage.  
Engine documents and the next thing after that is probably the Fuse driver, the Fuse file system driver specifically for Linux, where he can use this to just browse the files locally on a computer. So let me show you.  
What that looks like from just?  
A regular file system. Let me share my screen again for this.  
Can you see my screen share?

**Andrei Bosik** 36:46  
Yeah.

**Aaron Bockelie** 36:48  
OK so this is just off the root of my home home folder. So this is just my regular home folder. I've mounted the the graph file system in a directory called knowledge and we can see that there is a ontology folder.  
And you can see here how it has those same ontologies, emergence patterns, first principles, books and ways. And when we go into one of these folders, we can see documents. So first principles, documents, and these are the original files I uploaded. There's nothing special about this other than it being.  
Just a text file and literally here is the text file. This is the content of that text file. If I open this in maybe not that, but like a nicer like mark text right? Here is the same markdown rendered nicely, right?  
Document enterprises code and so forth and blah blah blah as it goes on.  
O.  
What we also have is this outside of the ontology directory. We have a directory called Emergence and Emergence is a special way of querying. What you do is you just make a directory.  
So I'm going to make a new directory here. I'm going to just make a new folder and I'm going to call this one operating model. OK, when I create the directory and I go into the directory.  
What we I'm hearing my computer doing this. It's fan spin up for a minute, so it takes a second on this first query. So once again I'm building optimization for this.  
And what we'll end U with is a bunch of files in here hoefully.  
We really picked the the wrong time to kind of do this because it's.  
Very, very delicate right now. Let me try opening it just real quick here.  
Well, it's just acting super slow right now, so um.  
Yeah.

**Andrei Bosik** 39:25  
I have another questions. If I create a separated users for example, can one user have access to data?

**Aaron Bockelie** 39:34  
Yes.

**Andrei Bosik** 39:40  
Second user for example, I create account for me and for Valve for example, Val store his data, I store my data. Can I have access to data in another user?

**Aaron Bockelie** 39:45  
Mhm.  
OK.  
Yes. So by default all information is shared and the system actually must have the system must have access to all knowledge and all information. What you can do is by ontology.  
By grouping of ontology you can prevent other people from seeing things, or you can prevent people from adding to an ontology. So basically you can you can prevent the viewing or creating or editing of other. You can isolate by ontology.  
Apology.  
So if Val has an ontology about.  
Financial details, financial strategy, something he doesn't want you to see. He can keep that to himself, and you might have a thing that you don't want to share with Val about his food preferences, let's just say.

**Andrei Bosik** 40:40  
Yes.

**Aaron Bockelie** 40:52  
So you don't want Val to know that you have an idea about his food preferences. So your two sets of ontologies actually are connected in some ways, Val's gonna say.  
Concepts get created as Andre has really expensive taste in food, and Andre's concepts say Val doesn't like to pay for lunch, let's just say. Now you guys would see those on your own, but you wouldn't see the connection between the two because you've permissioned the ontologies to.  
Be separate.  
But the system itself, the the super administrator, the graph administrator, would see everything, the full truth. So you have to decide why are you hiding it or why are you showing it and so forth. There are legitimate reasons, that's why it's been built into it, but I'm just.  
Trying to play with a fun example of how you can prevent things. So OK, so here we go. It's just slow still because I'm on the slow mode right now. When we look at, I guess operating model didn't bring up anything. We'll use emergence instead.

**Andrei Bosik** 41:46  
Yeah, I understand.

**Aaron Bockelie** 42:02  
So this directory called Emergence here you can see it has a bunch of markdown files in here and these individual markdown files, they're all four kilobytes in size because they haven't been loaded from the system. But if I were to open one of these.  
It shows up as an actual document. We can see here as the the front matter. Here's the description of the concept, and here's the evidence of the concept. And the evidence is the actual a clip, a small piece of the original document from where it came from.  
One of the cool things about using the the Fuse file system, the driver for the file system that makes it look like just regular folders on a computer, is that I can open Obsidian now.  
Let me open Obsidian. Give me a minute.  
And when we point Obsidian at the same directory, we get the same files because Obsidian sees it just as files, right? Except we also get all of the connections between things. So we can start to see the same concepts connected and viewed in here.

**Andrei Bosik** 43:07  
Mhm.

**Aaron Bockelie** 43:18  
As we would in the web workstation, but it's actually in Obsidian instead.  
O We can open the file and view it in Obsidian just the same way.  
And you have to remember that when you drop a new file into this, all of the concepts reshuffle because it's a very large data set that is dynamic. And so we're seeing the constant change of knowledge over time in this system.  
Finally, I want to add on just on the top of all of this, most of the interfaces that you're seeing, these files, the querying, the obsidian, the workstation, they're secondary to the principle reason of having it, which is to use tools like Cloud, Cloud and Cloud Code.  
To do deep introspective reasoning. This is like having a persistent front brain for these tools to be able to know how things are and and use them.  
Overtime and stay consistent. It's not rag, it's not a document store. It is a conceptual memory of understanding for for a platform.  
So there's a lot to absorb in what I just showed you. There's like a whole platform that I've been working on for months and months and you guys are basically, congratulations, the first people to kind of really get to understand or have me show you this in sort of a structured way as a platform.  
And I'm not expecting you to be able to run it immediately right now. I would have hoped that you would try to run it though by following the documentation and get it started. It's quite straightforward to set up and once set up it has an entire lifecycle management. You can just update.  
The containers it just restarts itself. Perhaps what I could do is show you just the Docker environment. So here is the containers as they are running so we see the API.  
Container is here. We can see it how it has reviously retrieved a bunch of documents from the storage system. If I restart the API container, we can see it starting U let me.

**Andrei Bosik** 45:27  
Mhm.

**Aaron Bockelie** 45:40  
This here it's fitting so we can see here from a from a cold startup.  
Right here.  
Using watch files because it's in dev mode. We're in debug view as well. We can see it's starting the service, starting the API, starting the job queue, loading the embedder model. The embedder model is running in CPU mode, not GPU mode right now.  
And we can see it making a connection to validate all the API keys to different tools and we can see it making sure that Open AI worker is used for the Open AI connection to be able to do the concept management stuff.  
When we look at the web interface, I don't know if it's going to show anything good here. Probably not. It's just it's a static front end web environment that's served. So it could be put on a caching accelerator. We can see the storage container. So this is garage. It's kind of like an S3 compatible.  
Storage bucket. So garage is used in that way and we can see Postgres, the database. We can see there's some errors and stuff going on here cuz I'm in the middle of doing development work with it right now, but we can see it querying on stuff and trying to find things.  
So let me give you a couple other interesting examples of what this tool I've found that it can do. First of all, you can upload pictures to it too. It's not just documents, you can upload a bunch of pictures. So if you had photos of.  
A space or of a product or pictures of a slide deck. You can upload all these to it and it will create concepts based on those pictures. It'll narrate the picture, write it up.  
Find all the parts. You can then search for photo similarity too. Like you could if you upload a bunch of pictures of dogs and then you show it a picture of a cat, it'll say there are no cats in this, but this is the closest cat looking dog that you've got and describe it.  
If you upload live transcriptions, so this is something I'm working on right now. This entire conversation as we've been talking right now is being recorded in one big GLOB.  
But it's possible that in the near future I'm building some tools that can run on the desktop that when you hit the go button from your desktop, word by word, it's going to collect a statement. We'll talk here for a couple minutes and then it'll be a paragraph or two, right?  
It'll load that paragraph into the same ontology over and over again, and literally, as you're talking, it's assembling a knowledge concept graph of what has been said so far, and simultaneously you could then ask Claude about what's going on live, what's actually going on. So Claude becomes an active participant.  
In the conversation that you're working with.  
This can give you an advantage when having conversations with other people, because one, you can track exactly what was said. Two, you can actually say, hey, so-and-so said whatever, what do you think? And then it'll go, it'll connect the dots. And if you had a lot of other information about it too, it'll connect all those dots too.  
So I would say that we're in a barely alpha stage for this platform right now and you guys are being introduced to it.

**Val Levitan** 49:13  
Uh.

**Andrei Bosik** 49:15  
It's a really interesting project, really.

**Aaron Bockelie** 49:17  
Yeah, that's why I keep working on it.

**Andrei Bosik** 49:21  
Uh.  
My question is can I use for authorization for example and as a source authorization?

**Aaron Bockelie** 49:31  
It's it's planned. So Oauth I I have not added a Entra or Google or Okta providers yet, but it's planned to add integration providers for those so you can get those things from there. The the trick with that.

**Andrei Bosik** 49:41  
Mhm.  
Mhm.

**Aaron Bockelie** 49:48  
Is that I'll have to do the whole Oauth registration flow for them, but it's it's it's architected to support that when the time comes.

**Andrei Bosik** 49:58  
Uh, how uh?  
How is?  
Oh.  
Security is this UI? Can I take into Internet or maybe I need use of proxy for example to not shows this UI in Internet?

**Aaron Bockelie** 50:21  
I think for now it would be smart to not allow it to be out on the open Internet. However, I've done my best so far to make it secure.

**Andrei Bosik** 50:32  
Mm-hmm. OK, I understand.

**Aaron Bockelie** 50:32  
The only the only exposed API endpoint when you're not logged in that works is literally the the the auth login page and the health health endpoint. That's it.

**Andrei Bosik** 50:46  
If I for example if I use our proxy to show UI how for example Cloud code or Cloud desktop.  
Uh can connect to the API uh your graph.

**Aaron Bockelie** 51:05  
Sure.  
That's a good question. Let me let me show you.  
Minute.  
So I'll show you the the 1st way that I would want you to do it, which is the.  
Just through the web workstation is the fastest way. So you go to administration and if you have the right role, if your role supports administrating this under.  
Oauth clients create, delete, read, right? So you could make a custom role to manage clients if you wanted to. But we go to this view. I can create a new one. Let's call it my Clouddesktop.  
I'm going to click create and it will give us the client ID and the client secret. And if you want to, it'll give you examples to copy and paste for command line for cloud code and a desktop config to enter into here.  
With the correct URL and everything for this latform O. It should be fairly straightforward to do this.

**Andrei Bosik** 52:21  
Uh, how? How? How is this is secure? For example, uh if I open uh.

**Aaron Bockelie** 52:22  
And so, oh, go ahead.

**Andrei Bosik** 52:30  
On some URL this API interface is the security for users in in Internet or not?

**Aaron Bockelie** 52:39  
So this is only showing local host right now because this is the developer environment for it.

**Andrei Bosik** 52:43  
Yeah, I understand why you use local host. It's run on your local machine. But if I run this on server and I would like share access for example to Val, I need to share this to Internet.

**Aaron Bockelie** 52:58  
Yes. So Val would need to. I'm not sure how you're going to get a connection between where Val's at and your environment. So that's something that I have not thought about. But let me, I just want to show you one other thing here.  
Um.  
This environment here is actually configured for a routable domain name.  
So KG dot broccoli dot house is the full on domain name is behind the firewall in private right now.  
And this is a much older version I need to update to make it be current, but it should in provide you the correct full URL. So if I were to copy this here.  
And look at this.  
We can see that because my browser has a session session cookie for this, I'm logged in already to this.  
See I have the the API doctrine point.

**Andrei Bosik** 54:07  
Try opening Incognito.

**Aaron Bockelie** 54:14  
I'll just do one better. Let me just log out.  
Could invalidate the cookie.  
Yeah.  
I might not be doing session invalidation right now, so I it's not doing what I would expect it to do. So like I'm saying, don't open this on the open Internet yet. You'll need to do something like the VPN or some other more private way to do this.  
And I just need to, you know, I'm only one guy doing the work, so the infrastructure's there. It's likely this endpoint is not.

**Andrei Bosik** 54:53  
Mhm, mhm.

**Aaron Bockelie** 55:05  
Clearing properly for the for the tokens.

**Andrei Bosik** 55:06  
Can you send me this link? Uh, I try open on my browser and see what I can.

**Aaron Bockelie** 55:11  
Yeah, it it won't open because here you can try, but it's not routable.

**Andrei Bosik** 55:21  
But I can see.  
OK.

**Val Levitan** stopped transcription