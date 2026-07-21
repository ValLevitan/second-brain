**Transcript**

9 September 2025, 01:23pm

**Val Levitan** started transcription

0:07  
Um.  
Um.

**Pavel Frolov** 0:08  
Next note, I would say that.

**Val Levitan** 0:11  
So, so, so the category, so I'm sorry, powerful interruption, but a category can be added additionally later on.

**Pavel Frolov** 0:16  
Yes.

**Aaron Bockelie** 0:24  
Yes.

**Pavel Frolov** 0:24  
Not only category, subcategory component, everything can be added by this negotiation that actually it meet our requirements. It's really necessary for new category or subcategory.

**Aaron Bockelie** 0:25  
Yeah.  
So I hate to do this, but I want you to take all these notes so I can actually get to them, because adding notes like this is about the most inaccessible data type you can possibly do in Excel.  
I'm trying to highlight the notes, but it's like there's no. If you export this as a a spreadsheet or whatever, it doesn't work.  
And the notes are extremely valuable.

**Pavel Frolov** 1:16  
Sure.

**Aaron Bockelie** 1:17  
Now I have to write a VBA macro to be able to extract the notes.  
In a group.

**Val Levitan** 1:23  
Oh.  
So so you want a note in uh in the adjacent uh column.

**Aaron Bockelie** 1:30  
I think we should do adjacent column or a look U or something on another sheet.  
Just go ahead and try to get the note out of there. It's like very difficult.

**Andrei Bosik** 1:59  
Uh.

**Aaron Bockelie** 2:01  
We can fix these columns.

**Andrei Bosik** 2:01  
Maybe do it on another uh uh tab.

**Aaron Bockelie** 2:05  
Let's do this.

**Andrei Bosik** 2:07  
On another tab, not on this tab maybe.

**Aaron Bockelie** 2:10  
No, we'll go like this. Watch you take these columns.  
And you format those columns differently.

**Pavel Frolov** 2:41  
Yes.

**Aaron Bockelie** 2:58  
Just turn off wra text on those.  
And then you can then you'll have them.  
I'm going to move these columns out of here.  
But the Munchera source.  
Well, that was not what I wanted.

**Val Levitan** 4:28  
It.  
8.

**Aaron Bockelie** 4:29  
Try again.

**Val Levitan** 7:16  
Why do you want to expose the comments? I'm sorry, maybe it's a stupid question and natural for everyone, but I don't understand it.

**Aaron Bockelie** 7:26  
Because with the thing that we're going to do next is turn this into a tool that we load into GitHub that validates REO names and revents bat wrong names from being created.

**Val Levitan** 7:37  
That would be clever if we can do that. I cannot imagine how to make this tool.  
I guess wait and see.

**Aaron Bockelie** 8:09  
Basically what you can have is a management repository in GitHub with actions that looks at all of the other repos that you have in your enterprise and checks them and flags them for various properties, everything from.  
Poorly named repos to permissions that are wrong to.  
Whatever you want actually activity user accounts.  
When you have the data trapped inside of a Microsoft proprietary format like this, it's very difficult to have an AI agent help you do things too.

**Val Levitan** 9:15  
It.  
But I.

**Aaron Bockelie** 10:22  
OK, is that it? Oh, you almost got it all.  
Persona is next.

**Val Levitan** 10:35  
It.

**Aaron Bockelie** 10:40  
OK.  
Oh.

**Pavel Frolov** 10:58  
So I assume in case when somebody decided to create new repository, first of all he will need to describe what will be put in this repository and then ask for AI.  
Do you have ready to use categories, subcategories for my repo? If not, then suggest to create a new one.

**Aaron Bockelie** 11:25  
So I don't even want to invoke AI, honestly. I want to just make it so it's an easy to use way to understand this.  
So AI or not, let's make a a system or a document that has sources that make this simple to work on is basically what I'm getting at.  
So.  
Otherwise, what we end up with is managing A spreadsheet that's listed somewhere, and that's difficult. But if we have an actual git repo in for management of repos of the entire git platform, it.  
Transforms get repos into sort of its own administrative interface for things. So when it comes time to creating new repos, perhaps you can create them, but you're going to be flagged for an incorrect name almost immediately.  
And then there should be clean, clean and lain documentation about how this actually looks, for example.  
Let me just quickly kind of give you an example of what I'm thinking of here.  
So.  
One of the things that we can do here, I want to, I want to ask you, Andrei, in your mind, how would you now go about?  
Looking at the repos that you've got now and verifying these names are correct.

**Pavel Frolov** 14:52  
Oh.

**Andrei Bosik** 15:01  
Mhm.  
Just look in the table now.

**Aaron Bockelie** 15:08  
OK.  
So for the repos that you have right now we have on the.  
On the repo the source sheet for example.  
Is that going to be your mapping to where you start or are you just going to start in GitHub and kind of roduce them from there?  
O these.

**Pavel Frolov** 15:37  
Actually this list was created from the repositories that we currently using only only from this list, yeah.

**Aaron Bockelie** 15:45  
Right and so final.  
O finalreo name final namereo is your is your new list, right?

**Andrei Bosik** 15:53  
Yeah.

**Aaron Bockelie** 15:54  
Yeah.  
So now let me just do this really quick.  
Uh.  
This is where we can begin to build a library of tools.  
That we can use to validate our terms. So here is that spreadsheet in Jason format instead. So we have the naming format, we have the different terms, so your descriptions in here, right?  
O When we start to view these here, let's try it out.  
So what we then can say is a WS cluster API, so it's a valid repository name. So categories repositories for this subcategory is that and component is this and this is the purpose of it.

**Pavel Frolov** 17:59  
It's right to use something that contains dashes, for example Flex POS or probably what else? Mass engine, but mass engine is.

**Aaron Bockelie** 18:13  
And that's, well, we didn't resolve that yet, right? So we need to find out how that's going to work because.

**Pavel Frolov** 18:16  
Yes.  
Yes.

**Aaron Bockelie** 18:21  
There may This is why I want to understand. Do you want to use dashes in that or do we use underscores?  
So obviously I haven't tested that case yet. I'm going to guess it's going to break.  
Yeah, see.  
'Cause the dashes are simplistic. I mean, I just put it together just now, so.  
We could probably resolve this in a certain way, but.  
Let's do this.  
O We'll fix the naming convention to use under score for justice a minute.

**Pavel Frolov** 20:19  
Aaron, I suppose you're using a terminal, something like C Lion AI client, yeah.

**Aaron Bockelie** 20:21  
Yeah.  
Yes, Yep.

**Pavel Frolov** 20:34  
Oh.  
Sure.

**Val Levitan** 20:47  
OK.

**Aaron Bockelie** 20:58  
This will take just a little bit of time because it's a retty big Jason file.  
The other thing that's nice is that if it's in Jason format, for example, VS Code would let us have a nice view of that.

**Val Levitan** 21:33  
Yeah.

**Aaron Bockelie** 21:36  
Just going to wait until it's finished before I.  
Look in here.  
I guess we could try.  
O Now you can have.  
It's like I might have messed U on some of these a little bit.  
AWS is a category.  
But the point is, is that we can have sort of a structure that's more defined this way.  
So I'm not trying to build it all in front of you right now. I'm just trying to point out that by taking a more structured consumable approach that is not a spreadsheet or CSV.  
You're going to open yourself to a lot of possibilities for better tooling in the future.

**Pavel Frolov** 22:38  
Yes.  
Agree. Agree. If we have all this categories with description in form of Jason and manage it in the future, it will help us to automatically validate them and newly created repositories, yeah.

**Aaron Bockelie** 22:56  
Right.  
A really good example of this Andrei is that when it's in Jason format, you could consume it in JIRA and when someone needs a new repo name, they can just file a support request and it will automatically make sure their name is correct before.

**Val Levitan** 23:07  
Hello.

**Aaron Bockelie** 23:16  
Even allowing the support request to happen and then the support request can trigger a web hook in GitHub and the repo can be created automatically so you don't even have to worry about it.

**Andrei Bosik** 23:30  
Yeah, it's a good idea.  
Oh.

**Aaron Bockelie** 23:36  
This also allows you to um.  
Kind of.  
I guess in a way you could use AI to accelerate your work because you can if you have a command line version of the tool then AI tools can also use that as well and and work with you to to validate and fix things.

**Pavel Frolov** 24:02  
Mhm.

**Andrei Bosik** 24:03  
Uh.  
I would like.  
Proposition about create separate organization. It's next questions. It's not about naming about create separate organization for knowledge, for example, because we have repositories which.

**Aaron Bockelie** 24:18  
Sure. Yeah, yeah, of course.

**Andrei Bosik** 24:29  
Create while for example for example Personas or CBSA and I think in future repositories like this is add more and this name is not.  
Convenience table.

**Aaron Bockelie** 24:50  
I'm not sure if I follow.  
I I need to. I need further explanation.

**Andrei Bosik** 25:01  
Uh, I show one second.  
For example oh wait, for example we have now, for example now we have repositories personas. She may say about GVL and this repositories is not.  
Convene with our table. It's not is a subcategory of companions in our real development process, but we all want to use GitHub as confidence.

**Pavel Frolov** 25:32  
Right.

**Andrei Bosik** 25:46  
And with without JIR without confidence like is confluence in GitHub and don't use confidence in Atlassian and maybe for this repositories we need to create another separate organization to create knowledge for example.

**Aaron Bockelie** 26:01  
My suggestion would be to just make one called Knowledge JVL for now.

**Andrei Bosik** 26:07  
We use Julian as the first name in organization because organization name in GitHub is Unicom.

**Aaron Bockelie** 26:19  
So.

**Andrei Bosik** 26:33  
My question is what we need to do with this because I think we have more repositories with names.  
For example HR or.  
Thompson calls.  
Ideas Lance.  
Accounting.

**Aaron Bockelie** 26:59  
O.  
It seems to me that.  
It's very easy for you guys to chop things too fine.  
Kind of tend to do that a lot and I would say realistically for now.  
If we're taking a knowledge major category called knowledge.  
That I would want to see.  
It's probably possible that we have.  
Just a generalized subcategory for that, and then everything else under that is actually part of the repo itself.  
Like I don't. I don't know how finely grained you want to actually make that.  
For example, you could have in a subcategory you have knowledge base as a subcategory and you have a a knowledge called a category called knowledge.

**Andrei Bosik** 28:03  
Yeah, yeah. Now I create categoric knowledge and add this repositories to this category. But as I say, maybe we need move this repository to separate organization, not as a part of GVL.  
Technology organization.

**Aaron Bockelie** 28:23  
Let me ask why?

**Andrei Bosik** 28:26  
It's this repositories is not a part of development process.

**Aaron Bockelie** 28:27  
What's the justification?

**Andrei Bosik** 28:33  
In my vision, real technologies, this is development repositories. This is not uh.

**Aaron Bockelie** 28:34  
S.  
I want you to consider. I want you to consider for a moment what the word organization implies.

**Andrei Bosik** 28:41  
Vicky.

**Aaron Bockelie** 28:53  
In in my opinion, you almost could just go with one organization, but I know that you guys want to have a few slightly different ones.

**Andrei Bosik** 29:03  
Yeah, I think about this.

**Aaron Bockelie** 29:06  
Because here's what's going to happen.  
You're going to have two organizations. There's no knowledge base is going to be apparent for the ones that are working in the one, and then they're going to start stashing notes and ideas and documents and things in various places and it's going to get broken.  
And now you're shifting, shifting content potentially between organizations to stay coherent, which is more difficult than moving things into another repo or cloning within a repo and things like that.

**Pavel Frolov** 29:31  
Yes.  
Yes.

**Andrei Bosik** 29:51  
Yes, I know.  
That's why I ask these questions I.  
Don't know how it's currently. OK, let's place it in our.

30:31  
So.

**Aaron Bockelie** 30:34  
Let's think about knowledge now for a minute if we were to create a a a single major repository for knowledge.  
Would it be knowledge knowledge base?  
Because you have a category called Knowledge and a subcategory called Knowledge Base.

**Andrei Bosik** 30:53  
Knowledge base. This is subcategory because this is different product. It's a old product which we create yeah ago.

**Aaron Bockelie** 31:02  
OK.  
O There's actually a product called Knowledge Base.

**Andrei Bosik** 31:08  
Yeah.

**Aaron Bockelie** 31:08  
What does it do?

**Andrei Bosik** 31:10  
Um, use I for.  
Transcribe uh voice to.

**Val Levitan** 31:16  
No, no, we we we gave up this product. It's it's gone finished.

**Andrei Bosik** 31:21  
Yeah, we finished, but we have a quote and I think we need to start this code for future. Maybe not delete this.

**Val Levitan** 31:28  
We don't need to store the code. It's a it's a waste. You could archive it and remove it.

**Aaron Bockelie** 31:39  
O.  
Um.  
I'm just thinking about knowledge still right now, so if you have a category called knowledge.  
That's technically a allowed repo is to call it just knowledge.  
And so then what I would do is I would basically toss all of that under knowledge as directories inside of a structure and justice start maintaining that.  
And then you can divide it U as you want to from there.

**Pavel Frolov** 32:28  
Actually the question here I think would be do we need different access rights for different repositories like knowledge, GVL persona, knowledge, GVL, CBSA, knowledge, GVL and and so on.  
So if we don't need different rights, then all these entities can be put just on the knowledge in different.  
Um, directories and that's all.

**Aaron Bockelie** 33:05  
Right.  
So I would say that CBSA probably needs to have a more private thing. So you'd have to have something that more is you could have a a subcategory called business operations for example.

**Pavel Frolov** 33:08  
6.  
Right.

**Andrei Bosik** 33:25  
Wait a minute.

**Pavel Frolov** 33:26  
Mhm.

**Aaron Bockelie** 33:27  
You could also then play with that, play with the term for a minute. Platform, business operations, infrastructure, business operations. Those all start to relate to managing billing and costs and other things like that that might exist in there, for example.

**Pavel Frolov** 33:27  
But.

**Aaron Bockelie** 33:43  
That's where I would suppose the name like that would go.  
Or biz OS or something like that.

**Pavel Frolov** 33:55  
Yes, and for me a knowledge JVL personas is just a directory within about JVL or knowledge JVL.

**Val Levitan** 34:05  
Hello. How's it going? Welcome. Thanks. I'm going to find recipe. Yes, I'm actually able to.

**Aaron Bockelie** 34:12  
Yeah.

**Pavel Frolov** 34:17  
Because this this rep data from this rep I think will be open for all the employees in the JVL.

**Val Levitan** 34:18  
For what? I don't know for a while. Yeah, it's. These two are here. OK. For these, Yeah. Um, for here. Yeah, she requested 4, so.

**Aaron Bockelie** 34:30  
Yep.

**Val Levitan** 34:35  
Good. I don't see your timer. Hold on, Monica. I know.

**Aaron Bockelie** 34:40  
How would you like me to give you guys a copy of the tool that I just kind of whipped up?

**Val Levitan** 34:45  
So that is right there.

**Pavel Frolov** 34:51  
Oh.  
Andy.

**Andrei Bosik** 34:56  
When you when you finish work on this tool.

**Aaron Bockelie** 34:57  
So.  
Well, it's. I think it kind of works right now. Yeah, exactly.

**Pavel Frolov** 35:01  
It's almost done.

**Aaron Bockelie** 35:05  
That's the thing is it's it's almost done now.

**Pavel Frolov** 35:08  
I think we just need to make a decision either to use underscores within subcategories.

**Aaron Bockelie** 35:20  
I think you should.

**Pavel Frolov** 35:20  
And uh.  
And use dashes to mix categories, subcategories, component and variant. But everything within a category should should use underscores. Is it a rule?

**Aaron Bockelie** 35:33  
So the.  
Any word? Yeah, any word within a category is a is that has a separator, uses an under score and your dashes are kebab are strict kebab case, so you only use dashes for kebab case management.

**Pavel Frolov** 35:45  
Mm-hmm.  
OK.

**Aaron Bockelie** 35:55  
This way when you list the repos through the GitHub tool or otherwise, it also will be easy to parse.

**Val Levitan** 36:02  
Do you guys know what kebab is?

**Pavel Frolov** 36:04  
Yeah.  
It's a category of subcategory companion to variants.

**Andrei Bosik** 36:09  
M.

**Val Levitan** 36:12  
Just like.

**Andrei Bosik** 36:13  
No sample.

**Aaron Bockelie** 36:13  
I think, I think that's one of those the classic human things. Every every culture has meat on a stick.

**Val Levitan** 36:15  
Russell.  
Sure sleep.

**Andrei Bosik** 36:23  
Yeah.  
And another questions what I have, how about short naming? We want to type for example local games error.

**Pavel Frolov** 36:26  
So.

**Andrei Bosik** 36:42  
Or we would like use short name of GS for example.  
This is like RGS and uh.  
Another things for example GUI. We want to type graphical user interface or use GUI.

**Aaron Bockelie** 37:02  
I think as long as you don't get too.  
Too obscure. It's probably OK, but I don't know what that judge is for obscurity, because when I started working with you guys several years ago, I had no idea what LGS meant.

**Val Levitan** 37:22  
I I hate abbreviations.  
I I never remember them. I feel like a ****** when I look at abbreviations.

**Aaron Bockelie** 37:32  
My suggestion would be to get rid of the naming the abbreviations.  
That's what Tab is for. Tab is your friend and auto completes everything.  
But not my choice. You guys's choice.  
I I've told you what I think.

**Pavel Frolov** 37:50  
But again, I think abbreviations like GUI or OS.  
Should be known for everybody.

**Aaron Bockelie** 38:04  
Yeah, there's some, there's some conventions that are pretty, pretty well known API, GUI, OS.

**Pavel Frolov** 38:08  
API, yeah.

**Aaron Bockelie** 38:13  
But highly specific things, especially ones coined by, you know, within JVL might be a a a mistake. And then the Gray area is generally known gaming terminology.  
So, but here's The thing is RGS and LGS actually a thing that the industry knows right off the bat? Or is that something specific to JVL?

**Pavel Frolov** 38:40  
Um.  
LGS definitely specific.

**Aaron Bockelie** 38:50  
Then I would I would name those out.

**Pavel Frolov** 38:54  
Mhm.

**Aaron Bockelie** 38:55  
But OS GUI API.  
I think those are OK.  
Roto should be rotocol, for example.  
QR Rapid. That's kind of a terrible name.  
I would call it QR code or rapid QR code or something like that or you know, that's the kind of the thing.

**Pavel Frolov** 39:21  
It.

**Aaron Bockelie** 39:30  
RGS Data Importer is an interesting one too, because now you've got a packed name, right? Remote Gaming Services Importer.

**Val Levitan** 39:36  
Oh.

**Aaron Bockelie** 39:42  
I would, I would rather you call it Remote Gaming Services Data Importer or something like that.  
And the reality is, is that when you start naming things super crazy long like that, you start to realize that then it shouldn't have their own repo anyway. They should be collapsed into a larger repo as just part of a regular project. So I would rather you expose the long, horrible names.  
And then you can go, wow, this is a real pain in the *** and we shouldn't have this as a separate thing. Let's put this into a monorepo or a repo beginning to look like a monorepo for a product.  
It's a way to be honest with what you've got.

**Val Levitan** 40:21  
Good test for us.

**Aaron Bockelie** 40:26  
It's just it's it's so easy to over classify things.

**Val Levitan** 40:32  
It's called Undressing the Truth.

**Aaron Bockelie** 40:39  
I will. I got to go. If you guys would please undress these short names in the spreadsheet and I will update the Jason file to match it and make sure the tool sort of works. I'll I'll mess around with it and kind of.  
Give it a nice sort of interface to deal with and then I can commit it somewhere so you guys can try it out from there.

**Pavel Frolov** 41:06  
Mhm.  
OK.  
OK.

**Val Levitan** 41:11  
So what's the What's our undertakings?

**Aaron Bockelie** 41:14  
So we need to undress the short terms for these names.  
Also, I think there's some mistakes. I think right here on 16 you accidentally copied over this one twice. See how it says it here and here.

**Pavel Frolov** 41:29  
Oh yeah, yeah.

**Aaron Bockelie** 41:30  
When you unpack the notes.  
So there's some stuff we've got to fix, but let's let's do this for example.  
Right O that turns into local gaming server GUI.

**Andrei Bosik** 41:53  
Local games. OK, OK, continue.

**Aaron Bockelie** 41:53  
And so you can.  
So you can see how I personally think this is a bad practice to have two of these in here like this. You should just have the GUI inside of local gaming server. Why is it a separate repo? I don't know. Maybe there's a reason for it. I'm not saying it's terrible, I'm just saying.

**Pavel Frolov** 42:10  
OK.

**Aaron Bockelie** 42:13  
It brings. It makes me pause to question why they're divorced.

**Val Levitan** 42:21  
So what's our what's our next target?

**Aaron Bockelie** 42:25  
So we need to fix all of these names that have abbreviations or hyphens and things in the names with underscores so we can maintain our kebab case.  
We want to validate that all of our conversion of notes still make sense for the terms.  
And then let's remove the note from here just so it's clean and this allows me to do a clean import of this CSV into Jason conversion and then we will maybe.  
Maybe a little later in the week we can meet again for half hour to play with a naming convention validation tool, and this will be the beginning of having tooling rather than a dead document that allows us to manage GitHub.

**Val Levitan** 43:16  
Fantastic. Let's, uh, let's plan for later this week, OK?

**Pavel Frolov** 43:17  
OK.

**Aaron Bockelie** 43:20  
OK.

**Pavel Frolov** 43:20  
Um.

**Val Levitan** 43:21  
Thank you, Aaron. Thank you guys. Bye.

**Aaron Bockelie** 43:23  
Thanks. Bye.

**Pavel Frolov** 43:23  
Thank you. Bye.

**Andrei Bosik** stopped transcription