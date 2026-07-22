**Aaron + Val-20251021_084922-Meeting Recording**

21 October 2025, 12:49pm

55m 48s

**Aaron Bockelie** 0:03  
Branch is subdirectories, right? So the concept repo with subdirectories for every game concept ever being developed or whatever is in here when a decision is made to work on.  
Creating a uh on developing that that concept.  
Then the concept repository is forked sparsely. What that means by sparsely?  
The weird word is that we only fork the directory that's in there that we're worried about. All of the history exists for that repo. It just it's that one fork that we're gonna move forward.

**Val Levitan** 0:51  
And so that is called what?

**Aaron Bockelie** 0:54  
That becomes a new repository for the next hase of development that is called forking.

**Val Levitan** 1:06  
So we we start from game concept, new new game concept repository, so.

**Aaron Bockelie** 1:13  
No, the game concept repository is eternal. It's always existing.  
And we keep adding to it. When the time comes to work on one of those concepts to promote it and to do it into it as a game design, we're going to fork a copy of that of that concept repository, but we're going to only.  
Fork one directory path inside of that concept repository that is the one representing the game that we're going to do design work on.  
That makes sense.  
Let me let me draw. Let me do it in a thing here.

**Val Levitan** 1:57  
100.

**Andrei Bosik** 2:00  
Uh, yeah.  
That's right. Yeah, we have one game concept repository which include all concepts for all games and this repository will live forever when we finish work.  
On concept game we create a new repository from this with shrink history and create game.  
Uh, game design repository. After I finish work in game design repository, we create a game production repository.

**Aaron Bockelie** 2:47  
So here.

**Andrei Bosik** 2:47  
Designs. This is our assets repository productions. This is our gaming.

**Aaron Bockelie** 2:54  
So so here is.  
Uh.  
Here is the concept repository.

**Andrei Bosik** 3:05  
I can find you your.  
On last meeting we create some documentation about one second I found this.  
Sent in chat for flow.

**Val Levitan** 4:08  
Well, I'm I'm moving. I'm moving past the.  
I'm I'm talking about a release.  
Um.

**Aaron Bockelie** 5:58  
O Here's the rogression.  
So we this is our concept repository.  
And here's our main directory and the concepts and all of our game concepts.  
When we're ready to work on Concept 3, we sparsely clone or fork the concept repository into Game 3 Design repository. Here's the original file Game 3 description.  
From here, so the path is actually just literally just moved over.  
Um, to make it clear, let's do this.  
Oops, let's name it.  
Just exactly the same.  
So we see that concept 3 from the main directory is main directory concept 3. So this this is sparsely forked from the big concept folder. Then to develop the design, all of these new things are added to the design in this repo.  
O We have a clean separation of concepts.  
Worked into the design.  
And then we end U with a roduction repository which includes all of the design work.  
And then we start adding more items in here, so source libraries, et cetera, release artifacts which are meta meta objects in in GitHub, action pipelines and so forth.

**Val Levitan** 7:46  
Andrew, do you understand this?

**Andrei Bosik** 7:49  
Yes, uh, but it's not uh.  
Yes, I understand. But Aaron, if a mistake, when we finish work with game concept, we create two new repository from not from.

**Val Levitan** 8:05  
Mhm.

**Andrei Bosik** 8:11  
Oh.  
Excuse me, when we finish work with game design repository, we not created from this repository game production repository. Game production repository creates from template because we not needed.

**Aaron Bockelie** 8:22  
OK.

**Andrei Bosik** 8:32  
Many information from game design repo we created clear to clear repositories for game production stage.

**Aaron Bockelie** 8:38  
OK.  
But.  
Either way is fine. So I am what I'm trying to promote more than anything else is a clean separation of the of the production repository from the other work as much as possible.  
I'm also trying to promote a lineage or traceability from the production work to the design work to the concept.  
O When we talk about this, this could very easily be done in a slightly different way here.  
So let's just keep the design repository like this and what we could do.  
Is we can call this a git submodule inside of the production repository. This means that this repository still exists as a design repository. People can still commit to the design repository if they want, but you can eventually lock it down so no more commits or whatever.  
Then you just include the design work as a submodule of the production repository. This means that the submodule is not actually stored with this git repo.  
It's a.  
It's a reference to the design work. So you know how in Windows. So this is kind of for both of you, just to be clear. In Windows, when you make a shortcut to another location, like if you create a shortcut to another a shared drive or another location on your computer.  
This is a symbolic link. This is a shortcut to another git repo, and So what happens is that nobody can commit to the design work here as a separate copy. It's actually a reference or a symbolic link back to the design repository, which still remains standing on its own.

**Andrei Bosik** 10:48  
Yeah, yeah, OK.

**Aaron Bockelie** 11:01  
Own and still has traceability back to the concept stage.  
O we we start, we keep concet for forever with all of our concets. We sarsely fork out a concept into the design and build that out.  
Then when it comes time to roduction, you use your master roduction temlate with all of its machinery and rocesses and stuff, and you add the submodule for the concept good.  
It's like you have a generic template with no colors in it. It's called production master production template. You clone a copy of master production template and you stick onto the side of it the sub module for the design work and it infuses the color of that.  
With this design now to continue on moving forward like putting droppers of color, food color into the into the water.  
Does that sort of feel like a good description?

**Andrei Bosik** 12:09  
Yes, for me, yes, uh, it's uh same as that I mean.

**Aaron Bockelie** 12:14  
Or or maybe more apt is here's my coffee and then when I put my Creamer in it, it becomes not coffee colored anymore, right? It's lighter with all the color of the of the design work.

**Andrei Bosik** 12:35  
But I think we'll have another question, so.  
So.

**Aaron Bockelie** 12:37  
Of course.

**Val Levitan** 12:39  
So after production is done and Monica says my work is done.  
I'm ready to release the game.

**Aaron Bockelie** 12:49  
Mhm.

**Val Levitan** 12:50  
Then it goes to release management.

**Aaron Bockelie** 12:55  
Doesn't go to release management because it's already release managed as soon as we start that roduction repository.

**Val Levitan** 13:03  
Well, somebody needs to take this and.  
Move it to GLI. Monica will not. Lena will not do it. Pavel will not do it. Irina will not do it. Val will not do it. Andrei will not do it. So you, Aaron.

**Aaron Bockelie** 13:11  
Right.

**Val Levitan** 13:25  
A few years ago called this cycle release management.

**Aaron Bockelie** 13:30  
Yes.

**Val Levitan** 13:31  
Is is it the same name now? We're still using the same name.

**Aaron Bockelie** 13:36  
So, so to be clear, JVL has a concept of release management and so we use that term, but.

**Val Levitan** 13:45  
We didn't. We didn't have concept over this management as.

**Aaron Bockelie** 13:47  
Well, Ivan manages the releases right to to to to GLI.

**Val Levitan** 13:52  
We we didn't. We didn't have Ivan in that position and we didn't have the concept of release management because we actually nobody even knew what it was. So you created the name for it and we took the least.

**Aaron Bockelie** 14:02  
All right.

**Val Levitan** 14:08  
The least wrong guy and assigned them to this position as release management, release manager and gave him a responsibility of saying this is now ready.

**Aaron Bockelie** 14:11  
Yeah.  
OK.

**Val Levitan** 14:23  
Here's GLI. Here's the thing. Go and certify it. So we call you called it release management. If the name is still the same and if the guy is still in charge, what happens?

**Aaron Bockelie** 14:39  
Yeah, it's the same thing. So. So in this example of a production repository, there's this thing that I've called down here. I call it GitHub metadata. OK, and inside of this.  
Let's let's make this a little more realistic.  
There's actually a literally a directory called dot GitHub.  
And then there's a directory called actions.  
And inside of here.  
Are various actions that can occur in GitHub.  
And what happens then?  
When I publish a particular thing to GitHub in a particular way, these actions are programmed to watch for these files to be pushed into GitHub.  
And when they watch and they see a change, they will do different things. So in this case, there is an action called linting, right? So linting is like literally picking the lint off of your clothes. It's picking the lint off of your code, the bad pieces that can be automated and identified.  
Right.  
We have tests that run all the time. Anytime somebody commits code, the tests run to make sure that the changes that were done to the code still work continuously.  
When somebody commits to the code, the build system is constantly building the code all the time. Every time a commit is changed to the source directory, the build happens in this order. It starts by linting and finding errors, and if there's errors there.  
It stops everything else from happening. If linting is passing, it goes to test. If tests are passing, it goes to build. If builds are passing, it releases it, it can deploy or release the code.  
So we can now release a copy of it, or we can build an artifact. Artifacts are not part of the action pipeline. They're a separate thing where GitHub allows you to actually maintain a Gzip file or a zip file or an ISO image or whatever.  
Whatever way you package it in GitHub, this process happens automatically.  
Then optionally, you can tag an item for a version and you could potentially publish it. Now GLI is not going to be ready to accept the continuous delivery process from from from JVL right now.  
So what would happen is that Ivan would be watching all this stuff and making sure all this works as part of the build manager, the release manager process. Maybe Ivan's only focusing on these two, right?

**Andrei Bosik** 17:56  
That would be my solution to most of the one there.

**Aaron Bockelie** 18:08  
But Ivan can grow into managing these because he's holding hands with Andrei now. Andrei and Ivan are friends because they're working on these action space in here for the DevOps approach.

**Andrei Bosik** 18:12  
So I mean.

**Aaron Bockelie** 18:19  
When Ivan sees a viable release that has passed linting, testing and building, and maybe even more testing.

**Andrei Bosik** 18:20  
I think.

**Aaron Bockelie** 18:31  
Then and then maybe we it just sits here and release and then Ivan goes and brings it off into manual testing land for humans to play the games just to see how it goes.  
But he knows that this particular version uh.  
I'm just making up a version number this version.  
Some sort of commit hash, right?  
This is identified uniquely. There is no way to reproduce this version number and this commit tag ever again. It is absolutely immutable and never you can't build that again. So Ivan knows that this particular tag version is the one he's going to download from the release artifacts.  
And e-mail it off to GLI and GLI is gonna go test that, certify that exact commit and release tag version.  
That's a manual process because it's now, you know, it's an e-mail, it's phone calls, it's whatever it is. If at this point, this is where we can step back and go GLI. We have an automated process to deliver this to your inbox.  
Do you want it in an FTP server? Do you want to give it? Do you want it in this other thing? Do you want us to deliver it via Postal Service? Whatever. I don't know. I mean, there's lots of ways to do that.  
But this is still release management right here, and this is still Ivan's job of managing this.

20:28  
OK.

**Val Levitan** 20:30  
Andrei, do you know how to do it?

20:31  
OK.

**Andrei Bosik** 20:35  
I think it's not a big clear for me because I have many questions. First question, what about project? We speak, we speak about what final artifact? And artifact is is a image.  
This artifact built from many, many another artifacts.

**Aaron Bockelie** 21:02  
Sure. So every other thing's gonna have other artifacts. You're gonna have a build system that's gonna be. It's gonna be as complicated as it needs to be, right?

**Andrei Bosik** 21:05  
Oh.  
Or we speak about just a part of these artifacts. For example, we speak only about how Michael Juan or something else can view.  
Uh game on their PC for example.

**Aaron Bockelie** 21:33  
Mhm.

**Andrei Bosik** 21:34  
It's a different way to. It's a different. Uh, it's fast to build this.

**Aaron Bockelie** 21:42  
How do they get a game on their PC to play it right now?

**Andrei Bosik** 21:45  
We have a builder which work on Windows because we need the Windows libraries for build as a and then start this game on Windows machine.

**Aaron Bockelie** 22:00  
But but.

**Andrei Bosik** 22:01  
When build is finished, this build is upload to Dropbox and they download this from Dropbox to their PC and run as a simple binary file.

**Aaron Bockelie** 22:14  
So you get an EXE file that they just double click and play. So why do you need Dropbox? You have GitHub artifacts. Just have a builder on GitHub. Build the thing into an effect tool. Is it faster really?

**Andrei Bosik** 22:17  
Yes, yes.  
Uh, it's more faster.  
It's more fast. Yes, yes, the box more faster.

**Val Levitan** 22:29  
Stop. Stop. Stop. Stop. Stop. Stop. Stop. Stop. Stop. Stop. Stop.  
We had Dropbox U until we will have GitHub implemented.

**Aaron Bockelie** 22:44  
Yeah.

**Val Levitan** 22:45  
So don't confuse two things. Dropbox was a gut measure.

**Aaron Bockelie** 22:51  
H.

**Val Levitan** 22:52  
GitHub imlemented Drobox. No UN intended drops.

**Andrei Bosik** 22:59  
When we start build our all our or when we can build the artifact for for for Juan and Michael for example on GitHub.  
Sure we can stop use Dropbox, but now this build created on another builder.

**Aaron Bockelie** 23:22  
It's built on Jenkins, right? So when's Jenkins gonna go away?

**Andrei Bosik** 23:24  
Yes.

**Aaron Bockelie** 23:31  
So here's the thing. I'm I'm trying to lay this out as GitHub.

**Andrei Bosik** 23:35  
I think Jenkins will go away when uh all the all uh part of uh.  
Game production will be moved to GitHub. Now games created not only in GitHub.

**Aaron Bockelie** 23:49  
So.  
Here's here's the thing I'm I'm noticing there's.

**Val Levitan** 23:55  
We we we are running. Please stop.

**Aaron Bockelie** 23:58  
Sorry.

**Val Levitan** 24:00  
We are running two parallel ecosystems. We have a legacy ecosystem and we have a new ecosystem that we are emerging into.

**Aaron Bockelie** 24:13  
Mhm.

**Val Levitan** 24:15  
Michael and Juan never refer to an old ecosystem. They've released the game. They're done. They're not going back to it. They're only looking at the new games to be released.  
The new games are migrating onto Omni. Omni is only available on Git, sorry GitHub, so any new game that will be developed on Omni on a moving forward basis.  
Will be compiled in GitHub and will be distributed in GitHub.  
So let's keep this in perspective. And when we talk about things, future and past, I do not want to modify past. Whatever is being developed in the old ecosystem, it will live itself out of relevance.  
And will stop being relevant and eventually we will stop using it and it will just disappear. We are not modifying the old ways of doing things for the sake of this conversation.

**Aaron Bockelie** 25:20  
Yes.  
Yep.

**Val Levitan** 25:26  
We are focused on defining new ways of how we will be working. When we define new ways, we now understand that all files or artifacts submitted to GitHub will have to be in.  
Markdown format. The knowledge base will have to reside next to code the.  
ISO image will have to be assembled through actions in GitHub. It will have to be distributed instead of using Dropbox using GitHub.  
So for the sake of this conversation, please let's focus, concentrate and focus on the efforts dealing with the new ecosystem.

**Aaron Bockelie** 26:28  
So.  
I think the thing I I'm observing right here I am.  
Jenkins is is pivotal to everything working right now. There's been some exploration on how to make this stuff build inside of GitHub, but nobody's really put forth the time because no one has the time. Or maybe there's not a clear indication of how to begin building the game.  
Completely on GitHub.  
And I don't.

**Andrei Bosik** 27:03  
No, no, no. All new product created on GitHub, Omni created on GitHub, new current product created on GitHub. And my question, So what about product we speak when we speak about?

**Val Levitan** 27:03  
Yes, good.

**Aaron Bockelie** 27:07  
OK, so if all new product.  
You.  
So.

**Andrei Bosik** 27:20  
Release. It's a final easy image, or we speak just about part of this easy image. For example, we speak about only one game, about only one game, for example, Kale Ocean.

**Aaron Bockelie** 27:38  
Mhm.

**Andrei Bosik** 27:40  
And we would like Juan and Michael can view how this game work.

**Aaron Bockelie** 27:46  
Mm-hmm. So there's lots of released artifacts that can be created, so.

**Andrei Bosik** 27:49  
They not needed to ISO.

**Val Levitan** 27:52  
When again, let me let me answer this question.

**Aaron Bockelie** 27:54  
Yeah.

**Val Levitan** 27:56  
Oh.  
In during during the concept stage.  
We discuss. Let me be exact. Let me open this.  
We we we discuss initiatives.  
And one of the initiatives for Omni originally was a Class 3 single game Kaya Ocha.  
You following me so far?  
Andrei froze. I lost you. Andrei, you're you're you're half asleep. You know you gotta you gotta do this. Just get just get up. Get up a little bit. Do some push-ups.

**Andrei Bosik** 28:38  
Uh, I I think.  
No, no, no, no.  
Uh.

**Val Levitan** 28:49  
Because because you're too relaxed, I I I need, I need a tempo in this meeting.

**Andrei Bosik** 28:55  
I just think what you you say.

**Val Levitan** 28:56  
When there is nothing, there is nothing to think, nothing to think. It's very basic. When we started the project and initiative Omni, we said that we cannot move everything that we had in the Rage studio.

**Andrei Bosik** 29:01  
OK.

**Val Levitan** 29:15  
Into Omni by snapping our finger. It's just impossible. So what is it that we're doing first in Omni? OK, we're going to finish Omni framework.  
That encapsulates in it all the core subjects and then we will only implement one game.  
That game is Kaya Ocho. So now we will install this Kaya Ocho on the machine. What do you have? You have one game, you turn on the switch, the machine goes through power up cycle and you see Kaya Ocho.  
Simple. Yes. What's next? Well, next let's go into it. Where do we bring Omni first? Where do we migrate Omni first?  
We could do it in Class 3, or we could do it in Georgia, Coam in the state of Georgia or South Dakota.  
Or South Dakota.  
Well, let's move it, hypothetically speaking, to Georgia.  
What do we need for Georgia? We need multi games. We cannot release one game in Georgia. We need multi game.  
Uh, OK, back to game concept stage. So conceptually we need the screen for Omni that is able to select multiple games. We need multiple buttons.  
These buttons have to reflect the theme of each of the games. We call it multi game screen. So in the concept stage we add multi game screen, then we'll bring it to design stage, we'll bring it to production stage and we manufacture.  
Artifact for handling multi games. Then we start adding games. Kayaochu is already developed. We developed game two, game three-game four-game five, game six. We now have six games and we have multi screen. We can put it together.  
All of it comes out from production under a certain version number.  
Go back to Aaron's screen when he shows a release certain number. This is a bunch of things, bunch of artifacts that include multi screen, multi multi game selection and include six games.  
So all of that together answer to the initiative of introducing Omni with Six Game Pad.  
So that is the release.  
This release now has to be managed. It needs to be released to Eclipse. Eclipse is similar.  
Organization has GLI and when it's approved it goes into the market. But now it's a multi game. It's just another collection of artifacts.

**Aaron Bockelie** 32:34  
Jim I, yes.

**Andrei Bosik** 32:54  
OK, uh, then uh, our final artifacts. It's uh uh.  
For example is a image with which can be installed on machine.

**Val Levitan** 33:08  
That's correct.

**Andrei Bosik** 33:10  
OK, it's not artifacts that we can take to for example, Juan, Michael, something else to see how games work. OK, it's a it's a image that we can install on machine, OK.

**Val Levitan** 33:25  
No.

**Aaron Bockelie** 33:25  
You can have more than one artifact in a repo. You could have 10 artifacts. You could have an EXE and an ISO and a zip file and another full transformation if you have the Omni framework that can compile for an online posting to an online play site.  
Multiple, multiple artifacts, you know, exist simultaneously.  
And they can all be tagged with that same version.

**Val Levitan** 33:57  
Andrew, do you do you understand?

**Aaron Bockelie** 33:57  
Version 6.5.

**Andrei Bosik** 33:58  
Yes, yes, yes, but questions about how we can have, as I understand, have the release documentation to this artifact, not only.  
It is, uh, just the artifact. We need to have a documentation to this, uh, release artifact.

**Aaron Bockelie** 34:19  
There could be a DF file that builds the documentation as an instruction book for it that can be downloadable and rintable.  
You could take the markdown content and compile it directly into a PDF. That's just another artifact tag along with that with the EXE and everything else.  
And when you go browse the artifacts and you look for the releases, you'll see a bundle of files, a zip file, an ISO, an EXE, a PDF, a link to some internal cloud hosted private thing to play the online version of it, and so forth.  
But you have to design the flow for that.

**Val Levitan** 35:07  
We're we're not, we're not hitting the target. We're throwing darts, but it's not hitting the target. Andrei, what's what's blocking you? There's there's something you have a bunch of other things in your mind that we're we're not getting through.

**Andrei Bosik** 35:24  
Oh uh.

**Aaron Bockelie** 35:35  
Yes.

**Andrei Bosik** 35:47  
You stop.

**Val Levitan** 35:51  
I don't have any questions.  
My I only have one question. Do you understand what Aaron is guiding where Aaron is telling you to go?

**Andrei Bosik** 36:03  
Yes.

**Val Levitan** 36:03  
I am not an engineer. I am not an IT specialist.  
I don't understand 70% of what's been said.  
I am lucky enough if I can orientate myself somehow by sounds and bites.  
But technically I know, and I have enough trust in Aaron to know that if he says that something needs to be done a certain way after working with him for nearly three years or whatever the time is, I know tested by trial.  
That he knows what he's saying.  
But who needs to understand? Like all the crumbs, everything, every single little bit of what Aaron is saying is you. You need to understand this.  
So do you understand what he says?

**Andrei Bosik** 37:03  
I all understand what Aaron say. Aaron say very simple and easy things. It's uh, I know about this but.

**Val Levitan** 37:09  
So, so, so what I what I'm saying or or what I am asking or what where I'm going could be complete ****.  
It could be worthless **** because I have no ******* idea what I'm saying.  
Do you understand that I don't understand?

**Andrei Bosik** 37:31  
I understand.

**Val Levitan** 37:32  
So I'm using either you or Aaron to orientate me where I need to be so I could push. I could force everyone. I could go behind my bulldozer and force everyone to go that way because you cannot.  
So you need a guy like me who says **** you, do it that way.  
Is that clear to you or not?

**Andrei Bosik** 38:01  
Yes, it's clear.

**Aaron Bockelie** 38:05  
Andrei, this might help with the visual thing here. This is a project on GitHub. It's called OBS Studio. It's a very popular piece of software. It's complicated. We'll just leave it at that.

**Andrei Bosik** 38:17  
I know the solution in the software, yes.

**Aaron Bockelie** 38:21  
When we look at the releases.

**Andrei Bosik** 38:24  
Yeah, yeah, I I understand. What about you speak? Yes.

**Aaron Bockelie** 38:25  
Here's the latest release.  
Here's all the versions of the release by assets, everything from a Mac OS installer to zip files to source code to Debian whatevers. Here's another thing called Rustdesk. Rustdesk has quite nice.  
Pictures here with all of the change log and everything else and all the other links and nightly builds and whatever and all sorts of different installable formats as well.  
That's essentially what we're just talking about doing for any of the games that we're building.  
Like that's the vision right there.

**Val Levitan** 39:09  
Uh.

**Andrei Bosik** 39:11  
But in this is just little part of all product.

**Aaron Bockelie** 39:21  
OK, so you have a bundle, right?

**Andrei Bosik** 39:24  
For example bundle but game it's a little part because we have bundle of game but in this but in this image we add not only game we add.

**Aaron Bockelie** 39:37  
You have the Linux operating system and the whole image. Yeah, all the other pieces, right?

**Andrei Bosik** 39:40  
Oh, something.  
Yes, yes, yes.

**Aaron Bockelie** 39:45  
Yep. And so.  
At the top you have your game as a product, individually runnable. You have an operating system, individually runnable. You have the, I don't know, the CMS or whatever it is, the back end, whatever thing that runs.  
Stop.  
Each of these is individually runnable. I can go grab the base OS for a machine and install it onto a game machine, but it's not going to have any games. It's just going to sit there and do nothing, right?  
I have releases for games. They're internal releases that are internally individually playable, but they're designed to hook into the bigger ecosystem.  
You have just another layer right underneath it, right here. Here is another product, an integrator product. So you have a git repo for each seven or whatever it is. I don't know, it's some collection of games.  
So then that thing is always looking for new releases from the games and always looking for new releases from the Linux OS and always looking for the back end CMS or whatever it is or whatever those things are, and grabbing those and assembling those into an ISO file and putting everything in the right spot there.  
And then that puts out the ISO file that you have to load. Maybe it's got the installer, the bootstraps, cold bootstraps, the game machine when you plug the thumb drive into it and and run the installer. So now you are cascading the output from the next, from the next to the next.  
So Val had said how we're switching from an older way of doing things to a newer way of doing things. We're not taking the old stuff with us. We're just building a concurrent pipeline, a a separate factory assembly line, right? It's like I I had said a long time ago, we got the north, the north assembly line and the South assembly line.  
Line we're building the north, we're building the new S assembly line now, OK.  
So in an actual factory building actual products.  
Let's just say you're building.  
Game machines or or maybe computers or blenders. I don't know. There's just it doesn't really matter. Product.  
The product must go through its stages of assembly, the output of producing a.  
Producing the widget does not have it in a box or package, it just produces the widget. It is a series of assembly steps to put it together and at the end of this you're going to have the sub assemblies.  
The game, the OS, the this, the that inside of these assemblies and they're going to get packaged into a bigger box and then that box could puts into a bigger box. That's all that this is doing and So what you have is a bunch of git repos.  
Watching for valid releases from the pieces and automatically assembling all of the constituent parts into the bigger assembly and then putting that into the bigger assembly as you need to if one part one game.  
It's a valid new release tag attached to it.  
It's going to cause the next line to detect that that release tag changed and it's going to rebuild all this assembly, and this assembly is going to detect that this thing released a new version of this and it's going to rebuild its assembly so it ripples through the production chain.  
By posting one change U here in the game.  
This amplifies the release manager and the whole DevOps process to the point of giving you viable, ready packaged releases anytime you want, anytime something's committed. This is continuous delivery. This is the DevOps approach to producing the software.

**Andrei Bosik** 43:59  
Oh, I have no questions. It's basically things. Yes, I know about this, but.

**Aaron Bockelie** 43:59  
So.  
Yeah.

**Andrei Bosik** 44:07  
Uh.

**Aaron Bockelie** 44:08  
Well, I think the thing that you've got, the problem you've got, Andrei, is, is that everybody else needs to know that this is how this works too. Right now they think it's all wrapped into one gigantic thing inside of of of Jenkins right now.  
And nobody's thinking it's like a trapped in this monolithic Jakins thing with all these buttons to push to do stuff. And it's like, now we're not doing that anymore. We're gonna build in a flow of we're doing a flow rather than a single Singleton of of of a build thing.

**Andrei Bosik** 44:31  
Mhm.  
Maybe.

**Aaron Bockelie** 44:45  
It's a rearchitecture.

**Andrei Bosik** 44:48  
But uh, who?  
Create final this image. This is a Pavel and uh you know which uh things will be need include to final is image and uh.  
I think if we want to speak about how we can work with the releases, we need to also add file to this talk.

**Aaron Bockelie** 45:16  
Of course it can be added, but I don't know if it's a language thing or not, but I interpreted your statement as like I imagine in my mind Pavel's to make a release happen. In my mind, when you said that just now, I'm just being very literal.  
I imagine Pavel sitting at his computer and downloading a bunch of stuff and typing a bunch of commands or running a batch file to create one gigantic ISO image and then uploading it to an FTP server or something. That's what I imagine in my head.  
Because that's how I imagine how JVL has been doing stuff for a while. Maybe it's Ivan, not Pavel, but.

**Andrei Bosik** 45:55  
No, it's all work, all work automatically. It's we do not have manual operations.

**Aaron Bockelie** 45:56  
The reality is.  
OK, just I'm just being very clear. I'm making a cart. I'm making a cartoon because when you say Pavel does this, Pavel does not do this. Nobody does this. It's automated in the automation process in GitHub.  
Pavel might program the automation. He might define the steps, and he might define the specification and the requirements for what the packaging is supposed to look like when it's done. But it's the code in GitHub that actually does all of this work.  
Just like it does it right now in Jenkins.

**Andrei Bosik** 46:41  
All product it's work on Jenkins for new product it's work on GitHub yes but but why I say we need to add pile because pile know which which part need be included to is because for example.

**Aaron Bockelie** 46:48  
Yeah.

**Andrei Bosik** 47:01  
We need to include the driver for build data for example or we need to add for this machine something driver for display on this machine we need another driver for display.

**Aaron Bockelie** 47:15  
Earth.

**Andrei Bosik** 47:16  
Many things which need to include this image in.

**Aaron Bockelie** 47:17  
So you're gonna have, you'll have, you'd have manifests for hardware, right? Like this system kernel driver is gonna go for this build target and that build target. You might have multiple image images, you might have multiple build actions for different machine lines too, right?  
Like this is a vertical, this is a horizontal, blah blah blah, whatever, I don't know.

**Val Levitan** 47:37  
Is there is there a job for Ivan here or his job becomes obsolete and we don't need a release manager? I'm just trying to understand the process where we can.  
Understand the release number and manage the handoff, physical handoff because there is a human coordination, which by the way, I'd like to eliminate eventually.  
Between JDL and GLI.  
So GLI, we we need to say, hey, GLI, we're giving you this, these things, quotas on it. They give us a quote, we give them a purchase order, then there is a submission process.

**Aaron Bockelie** 48:16  
For now, I haven't if.

**Val Levitan** 48:31  
Witness compilation that has gone away. Now we do without it, but all this process.  
Somebody needs to carry through the finish line.  
And right now we pile it on Ivan, and Ivan used to put his.  
Release numbers inside of Jira plans as a project. It's gone now finished, but Ivan needs to reference a point somewhere. We tell him no, no, no, no more referencing in Jira.  
And no more confluence. Go to GitHub. Where do we send Ivan? What? We tell Ivan, look at this. When this appears, here's your number. Carry this through the finish line to GLI.  
That's my question for you.

**Aaron Bockelie** 49:29  
Let's.  
Let's blur our vision for justice a little bit so we can see see the pattern, not the details. Here is a release of a product. It is a bundle of a game. It has these fixes and changes and features in it.  
Here is the checksums uniquely for all of the binaries. You can never build this binary again. Well, you could rerun the action again and create the same binary exactly with the same checksum, but you can't change anything inside of this without having a checksum change Ivan's job.  
Is now to watch for these and understand and ask the questions. Is this one really ready? Is this is this thing actually available for for submittal?  
And maybe he is the liaison between the the hands on test saying this one's a candidate for the expensive hands on test aspects of stuff and if this passes all the hands on game play tests.  
We're now ready to submit this to GLI, and he'll download these files and put a packet together for GLI and send it off to them and negotiate and be the relationship glue between GLI and JVL for this particular release.  
If they reject it or they say we we don't, we we found problems, then Ivan can take this and he knows that these were the things we found in this particular version of our game and we need to go back to the team and say let's fix these things and then a new version of this will get popped up.  
3202 and then Ivan will then go, OK, we're going to do the thing and Ivan's job is now very important from a cost management situation because he has to be able to say.  
We're about to submit spend the money for July submittal.  
And his brain is being used to negotiate and ensure that he's asking all the right questions for this.

**Val Levitan** 51:34  
So where is it in not a GitHub?

**Aaron Bockelie** 51:36  
This is a release in GitHub. If we look at releases, we see all of the releases.  
So each one of these how they're different release and this one's tagged pre release.  
And this one's tagged pre release beta two and this one's release candidate one.  
And this one's 3200, and they're like, confident this is our major release. Let's actually let it out to the people. And then they're like, oh ****, we need to do a 3001 because we found some other problems and here's the latest. So basically 3200.  
Would be the send it off to GLI and this one is the GLI is giving us feedback on the stuff they found. Let's make a some hot fixes for 3201 and then resubmit.  
And that way, if GLI wants the old version and the new version to do a differential comparison of every single little file in there, they can see exactly what changed because we still have all the older artifacts right here.

**Val Levitan** 52:41  
So let's let's work with Kayo Ocho in real environment. Point me to what is Ivan looking at and what can Ivan grab? Let's let's it.

**Aaron Bockelie** 52:53  
I don't know. Andrei, I'll need you to show that because you're saying that we have stuff in GitHub building built.

**Val Levitan** 52:58  
Right. So let's let's take Kayocho through submission to GLI. Where is it?

**Aaron Bockelie** 53:06  
What is being built in Kyoto right now?

**Val Levitan** 53:09  
You said Kyocho is being built in GitHub and we have actions in GitHub and we can create an image ISO image. We don't use Jenkins anymore. OK, let's work with Kyocho. Let's pretend that we're putting Kyocho through GLI submission.  
And let's pretend that I'm Ivan and you're telling me Ivan slash Val, this is your, this is your domain. You look at this, show me.  
Sorry, Andrei, can you hear me?

**Andrei Bosik** 53:48  
Yes, uh, but uh.

**Val Levitan** 54:00  
New, new, new, new. Begin up.

**Andrei Bosik** 54:25  
Спросить, что он себя включает, я без понятия.  
Полегче это же только маленькая часть всей самого большого, там же операционная система там драйвера для работы с валидаторами для драйвера, для работы дисплеев. Там много много компонентов и.  
Куда должен смотреть ваня, чтобы увидеть релиз, я не могу ответить, я не знаю этого.

**Val Levitan** 55:03  
Он продуктов а?  
Пластика боях.  
А мои соц миту формирует мои соц он говорит на ура entering, и он придаст интервью.

**Andrei Bosik** 55:25  
OK, no, I'm just the primary. So the bar is possible, so you must.

**Val Levitan** 55:29  
And I got I I I I got it from the first time. Thank you.  
OK.

**Andrei Bosik** 55:38  
OK, goodbye.

**Val Levitan** stopped transcription