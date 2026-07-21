**Transcript**

10 September 2025, 01:34pm

**Val Levitan** started transcription

**Val Levitan** 0:05  
For.  
Oh.  
Git repository, so let's give it 100% that our effort just to conclude the meeting now.  
Are you looking at the Excel? Sorry for logging in late. I'm not sure what stage of the meeting we're at.

**Aaron Bockelie** 0:27  
I'm looking at the spreadsheet and I asked about game versus games and Andrei, I think you're gonna change it to game pack instead of games.

**Val Levitan** 0:36  
Did you change it, Andrei?

**Andrei Bosik** 0:39  
Yeah, sure, we can do it.

**Val Levitan** 0:41  
Yeah, let's do it quickly, a little bit faster. Let's pick up the pace. I want it to be our fast meeting, our last meeting.

**Andrei Bosik** 0:55  
Done.

**Val Levitan** 0:58  
What other comments do you have, Aaron?

**Aaron Bockelie** 1:03  
It's looking.  
I think you need to figure out why you have game local gaming server and local gaming server GUI. When you also have GUI inside of component on its own, there's some mixed up things in there.

**Val Levitan** 1:22  
Pavel, that's probably a question for you.

**Pavel Frolov** 1:27  
Actually, I don't think that I have a good answer for this. Initially it was more flexible for developers to have two different repositories.

**Val Levitan** 1:42  
What should be the decision now? Let's get to the decision, please.

**Pavel Frolov** 1:46  
Um.

**Andrei Bosik** 1:46  
One SEC.

**Val Levitan** 1:47  
But also pretend, pretend that you are a dictator. So now we want to dictate the rules. No, no more, no more democracy. This is how it's going to be.

**Pavel Frolov** 1:52  
Mhm.  
OK, in this yeah I I prefer to mix them under one repository to remove a local game and server GUI and to just to add this part of work internally under the server.

**Val Levitan** 2:04  
OK.  
Let's do it.  
Aaron.

**Aaron Bockelie** 2:16  
Here's here's how I act. Here's how I act as dictator. I just go like this for now. I'll I'll you just cross them out like this instead of actually delete them. I'm gonna just start crossing stuff out that I don't think you should have.

**Pavel Frolov** 2:24  
Mhm.

**Val Levitan** 2:26  
OK.  
OK.

**Aaron Bockelie** 2:32  
I think you should get rid of that.

**Andrei Bosik** 2:32  
About.  
About games, maybe.

**Val Levitan** 2:36  
Please share, please share the link in the in the chat again. I want to participate in this.  
So you understand, Pavel, now you're the local dictator, so you will have to enforce the rule, right?

**Aaron Bockelie** 2:51  
I think you need.

**Pavel Frolov** 2:57  
Mm-hmm. OK.

**Aaron Bockelie** 2:59  
We don't have any funny hats for you, unfortunately.  
Uh.

**Andrei Bosik** 3:07  
One second please about games. Uh, maybe use game bundle.  
Instead Game Park.

**Aaron Bockelie** 3:17  
As long as it represents what you're trying to do.  
And I want you to go back and do the test. You have to go back and test the name. If you have game bundle or game pack working assembling to the left to the top, do I have?  
Game Pack Progressive AWS. So if I go AWS Progressive Game Pack, is that what's? What's the name that makes sense?  
Is it a platform something game pack? Is it a tools something game pack? Is it a knowledge something game pack? Is it an infrastructure something's game pack or is it an AWS something's game pack? Because that's the order you can build stuff in from left to right.  
Taxonomy structure is big to small.  
What's happening is column E is growing and growing and growing and turning into what you had before.

**Pavel Frolov** 4:40  
Actually I do not see any differences between pack and bundle.

**Andrei Bosik** 4:44  
And we can move this name to the variant. What do you think about this? If we move to bundle is variant, game is companion.

**Pavel Frolov** 4:47  
It.

**Val Levitan** 4:54  
We got, we got stuck. We got stuck. We got stuck. Stuck. I need to get through this. Stop philosophy. Dictatorship. Name. Move on.

**Pavel Frolov** 5:02  
She.

**Val Levitan** 5:09  
Stop philosophy.

**Aaron Bockelie** 5:12  
Stick with stick with the bigger names first.  
Your categories, AWS Infrastructure, Knowledge, Latform, Tools. Technically you could get away with five repos and be done technically.  
As soon as you add your subcategory, you have five times whatever the number of categories are in C, column C. That's a ton of repositories to manage.  
They're not saying you're building all of these. I'm saying valid cases, right?

**Pavel Frolov** 5:50  
Yes.

**Aaron Bockelie** 5:50  
So.  
I think you have way too much detail and component.  
And you wouldn't ever slit U all of these that tightly.  
You have to just this is a filter for valid names, not defining every possible repo you're gonna have.

**Val Levitan** 6:18  
I will try to cut down on things because from here we we will only grow, so try to cut down.

**Aaron Bockelie** 6:35  
I'm gonna start crossing. I'm just gonna kinda go through and and not give a reason quite right, quite right away, but just sort of.  
Cross some stuff out here.  
If you see a yellow line, that means I moved it from another area from another column.

**Pavel Frolov** 7:56  
Seems so we're trying to switch the philosophy on again.  
We will never finish this work.

**Aaron Bockelie** 8:05  
O.  
So then my question is this.  
Why is it so detailed? Why do you feel that you need to have so many tight classifications for everything?  
Why?

**Pavel Frolov** 8:26  
Because it was suggested by by you and we tried to rename everything that we have right now to a kabob structure, nothing else.

**Aaron Bockelie** 8:36  
Right, but but but I didn't say try to force it into four layers deep. I just said these are valid terms for a kebab structure supporting U to a variant level.  
The reality is, is that you're trying to force every of your existing repos into a four level kebab structure, necessitating all of this. And so what's going to end up happening is you'll have just as many repos as you did before, and more so.  
Now when my goal for you is to actually while understanding that you can't just do this.  
To collapse multiple repos into one to merge some of these code bases together because they're complex an all over the place.  
And unfortunately, the process of providing the taxonomical space for these four layers here also makes it very, very convenient to continue to propagate a whole bunch of repos.  
So I guess all I'm trying to say is try to do a little bit of forcing to force the reduction of the variations of these things.  
O local gaming server versus local gaming server GUI is a really great one that you can. Let's cross out that right?

**Pavel Frolov** 10:14  
Mhm.

**Aaron Bockelie** 10:15  
Um.  
We already have GUI in there and you should take local gaming server.  
So I so for instance why I have remote gaming server in the subcategory but local gaming server is a component. So my my thinking is you need to move it over to here.  
I'm going to put local gaming server as a subcategory instead.

**Pavel Frolov** 10:50  
Um.

**Aaron Bockelie** 10:51  
And then if you need to look now you can say column C local gaming server and you can pick column E GUI and you have local gaming server GUI and local gaming server. It validates both repo names.  
Without having to add a special carve out for it under column E.

**Pavel Frolov** 11:26  
Yeah, it it can be implemented this way, but right now it was suggested name for repository, for example a platform Omni local gaming server.

**Andrei Bosik** 11:41  
Local gaming service. This is a part of only butter GS. This is a separated product.

**Aaron Bockelie** 11:50  
Why do you need to call it Omni local gaming server? Can't you just call it local gaming server?

**Pavel Frolov** 11:56  
Yes, if we can keep in mind that it relates to Omni, but if we want to say by the name of the repository that it relates to Omni group.  
Then it will be self-explanatory.

**Andrei Bosik** 12:22  
O.

**Aaron Bockelie** 12:24  
Is there two complete code bases for local gaming server then?

**Pavel Frolov** 12:30  
Uh, so.

**Aaron Bockelie** 12:31  
Separate from each other.

**Pavel Frolov** 12:34  
You mean local gaming center for Omni and local gaming center for something else?

**Aaron Bockelie** 12:40  
Yeah.

**Pavel Frolov** 12:41  
Right now, no.

**Aaron Bockelie** 12:43  
There's only one code base for local gaming server.

**Pavel Frolov** 12:47  
Yes.

**Aaron Bockelie** 12:49  
So why would we encourage the growth of another local gaming server?  
Is that is that planned or is that sort of like maybe gonna happen?

**Pavel Frolov** 13:03  
It can happen in future, but.  
You don't know exactly right now.

**Aaron Bockelie** 13:09  
OK, so I think that right there. Let's use that as an example of what to avoid, which is to plan for things that haven't happened yet.  
So I understand that there might be a differentiation between local gaming server and an Omni variant of it or something like that, but let's not promote A validation of a name that is like that.  
The the the purpose of forcing these columns like these is to make sure that we're naming things in the right umbrella of size. So subcategory is a pretty big thing and local gaming server is a pretty big thing.  
So there's not really a reason to then chop it U into even more and more smaller pieces and less you need to in the future.

**Val Levitan** 14:07  
Let's make a decision. If we need it in the future, we'll create it. Right now, we don't. Let's move on. Chop, chop.

**Pavel Frolov** 14:15  
OK, question to Aaron. In this approach it will be something like platform, local gaming server, for example core platform, local gaming server.  
GUI or you suggest to just a limit using local gaming server and everything related to components will leave under this repository.

**Aaron Bockelie** 14:41  
Yeah, I would say start with platform local gaming server and that's it. And then if you have to, if if it grows into some massive complexity and you got to switch some concern into a whole other repo, then you do platform local gaming server core.

**Pavel Frolov** 14:46  
Mhm.  
OK.  
And go at it.

**Aaron Bockelie** 15:12  
O for instance, central authentication server. That feels more like a subcategory than a component.  
I'm just going to kind of move stuff around.

**Andrei Bosik** 15:34  
This is a part of central notification service. This is a part of CMS.  
Part of Casino management system.

**Aaron Bockelie** 15:46  
Does it exist? Is there central authentication server is a very very broad term.

**Andrei Bosik** 15:53  
I understand this, but currently.

**Aaron Bockelie** 15:56  
Does CMS current does? Does CMS currently have a separate repository for central authentication server?

**Pavel Frolov** 16:05  
Yes.

**Aaron Bockelie** 16:08  
And is that intentional or did it just turn out that way?

**Pavel Frolov** 16:13  
Um.  
Actually, I don't know.

**Aaron Bockelie** 16:21  
So remember this is a forcing function I'm forcing.

**Pavel Frolov** 16:22  
It's highly, highly, highly likely it was just moved from SVM to Git, keeping the same structure as it was in CMS.

**Andrei Bosik** 16:29  
And get, yeah.  
Yeah.

**Aaron Bockelie** 16:36  
I have a feeling somebody decided it makes sense to make it separate and we're accidentally following someone's random decision.  
That's my guess. Someone extracted a portion of SVN, put it into its own git repo, and called it that.  
OK, let's keep going.  
Let's look at the subcategories for a minute. Cluster, you know, management system, several flex things, hardware, Incom, Jenkins.

**Val Levitan** 17:08  
Other.

**Aaron Bockelie** 17:12  
Math configs and engine.  
And that, if I recall correctly, was that other discussion about the abstraction for math so people don't see it directly. Is that right?  
That's why it's two different repos.

**Pavel Frolov** 17:31  
Mhm.

**Andrei Bosik** 17:32  
Not only this, because it must have another repository, for example mass engine core, mass engine API, mass engine packages.  
Something else.  
And uh, API core packages. This is companion.

**Aaron Bockelie** 17:52  
And those are all separate repos.

**Andrei Bosik** 17:54  
Yes, this is for it's because.

**Aaron Bockelie** 17:56  
Are these repos separated? Are these repos separated for technical engineering efficiencies or for politics?

**Andrei Bosik** 17:58  
OK.  
First this repositories contains different things and 2nd in some repository we can give access to people. For example people use repository mass.  
Configs and mass packages, but for repository mass engine, mass engine core access have only one person. This is if you.

**Aaron Bockelie** 18:34  
So that's a blend of both politics and and convenience. And do these repos exist independently from each other because you actually are treating the repo as also where the artifacts are stored?

**Andrei Bosik** 18:42  
Yes.

**Pavel Frolov** 18:50  
No.  
I think this is not an intention.

**Aaron Bockelie** 18:57  
OK, because that's another anti pattern that a lot of orgs do is they try to check in the actual distributable into the code repo rather than creating a artifact out of it.

**Andrei Bosik** 19:09  
No, no, no. This is, uh, code repo. Just code repo.

**Aaron Bockelie** 19:15  
OK.  
Are you comfortable with having it being a subcategory then?

**Andrei Bosik** 19:23  
I think it's a good solution.

**Aaron Bockelie** 19:27  
We'll leave it as it is then for now.

**Andrei Bosik** 19:28  
It's uh.

**Aaron Bockelie** 19:34  
OK, I deleted MCP from subcategory because no, that's that's not where you want to keep that and I don't believe you're actually writing MCP servers right now.

**Andrei Bosik** 19:48  
OK.

**Aaron Bockelie** 19:50  
Test 360 Are you? Do you actually have Test 360? Is it actually a product or is it an idea?

**Pavel Frolov** 20:00  
Actually we have a code under this repository.

**Aaron Bockelie** 20:05  
And is it being used?

**Pavel Frolov** 20:09  
Yes it it is in in use right now because QA engineers trying to create to to learn and to write some test related to this platform.

**Aaron Bockelie** 20:29  
OK, I'm going to uncross it out.  
I want to make sure you don't accidentally give the test the team of an infinite toy to to spend time in. They should be putting their test work into the product, not into their own thing. OK, texture Packer Vivian local gaming server.  
So let's look at the component column for a minute. Are there any items in the component column that don't pass the smell are a little smelly and actually should be a subcategory rather than a component?  
As an example, I feel like RG Data Importer is a little smelly and probably is actually a subcategory rather than a component, but I'm not sure.

**Val Levitan** 21:26  
I tend to agree.

**Pavel Frolov** 21:26  
Yeah, I think this is quite.

**Aaron Bockelie** 21:26  
And it could actually.

**Pavel Frolov** 21:30  
It it looks quite small.

**Aaron Bockelie** 21:33  
OK, just I.

**Pavel Frolov** 21:33  
To move, move it on the subcategory.  
Actually I don't like to have such component as applications for example. Quite strange.

**Aaron Bockelie** 21:49  
Why don't we just call it data importer?

**Pavel Frolov** 21:55  
'Cause it only relates to LGS.

**Aaron Bockelie** 21:56  
Then.  
Well, So what we can do is just, we'll just call it the.

**Pavel Frolov** 22:03  
Move RGS on the subcategory.

**Aaron Bockelie** 22:07  
Yeah, so RGS is already under there. Yeah, so I remove. So if I remove the word RGS from data importer, now you can go infrastructure remote gaming server data importer.

**Pavel Frolov** 22:08  
Oh, you will, yeah.

**Val Levitan** 22:11  
Well.

**Andrei Bosik** 22:24  
But that importer, this is a part of.

**Aaron Bockelie** 22:25  
Allowing the data importer pattern to be used elsewhere. What?

**Pavel Frolov** 22:25  
Yeah.

**Andrei Bosik** 22:29  
Data importer. This is a part of CMS casino management system.

**Aaron Bockelie** 22:34  
Great, so then you can do infrastructure concedo management system data imorter. Multiple systems can have a data imorter.

**Pavel Frolov** 22:44  
Mm.  
Then if we add CMS then we need somehow to inform that this data importer relates to remote gaming server.

**Aaron Bockelie** 22:59  
So you're going to have, remember it's kebab case, so you're going to have infrastructure, casino management system, data importer and that's a special repo name specifically with that if you needed it to. To be frank, I think it should just be a directory under the casino management system.  
Git or git repo and not a separate thing, but you know.

**Pavel Frolov** 23:23  
OK, how to treat the situation if we have different application under this repository application? I mean artifacts that can be produced by this repository.  
For example, we need an applications that import data from RGS and needs data importer for something else.

**Aaron Bockelie** 23:49  
Do you wanna move data importers to subcategory and just have a whole bunch of different data importers separated by purpose and code format and and things?

**Andrei Bosik** 23:49  
Thanks.

**Pavel Frolov** 24:03  
So for for each particular implementation it will be different repository.

**Aaron Bockelie** 24:08  
Why though, do you need to have? So what we're talking about now is edging in the reusability of code. So if you have a data importer that imports from X to Y, can you reuse that data importer multiple times?  
Elsewhere.  
If the answer is yes.

**Pavel Frolov** 24:28  
Highly, highly likely. No. Highly likely, no.

**Aaron Bockelie** 24:33  
OK, so it's highly specific to something.

**Pavel Frolov** 24:36  
Yes, yes.

**Aaron Bockelie** 24:38  
And then that also starts to imply that why would you have a separate code repo for RGS importers? Why wouldn't it just be part of RGS?

**Pavel Frolov** 24:51  
Because actually this is code mostly related to CMS, not to RGS.

**Aaron Bockelie** 24:57  
OK, so CMS and RGS do share code bases.

**Pavel Frolov** 25:06  
Um.

**Aaron Bockelie** 25:06  
So that I I'm trying to, I'm trying to make it a black and white distinction between an importer for CMS and an importer for RGS.

**Andrei Bosik** 25:07  
Yes.

**Aaron Bockelie** 25:16  
Do you need both as separate repos or is code data importer just worthless and we can just drop it and just say hey data importer is just a path inside of the RGS code base?  
And the CMS code base.

**Pavel Frolov** 25:32  
Actually this is not two two different importer. This is 1 importer of data from Air JS.  
To CMS known format and to put it under the database same as CMS is using.  
So this is part of CMS.  
Not part of our JS.

**Aaron Bockelie** 26:00  
So, OK.  
So let us assume for a minute that we could put this just in CMS as a directory inside of the CMS repo.

**Pavel Frolov** 26:08  
Mhm.  
Mhm.

**Aaron Bockelie** 26:11  
We don't even need to say that Data Importer is a component anywhere because we're never going to actually create a special repo specifically for data importing. The other part of it is this, if you do have a special repo for it.

**Pavel Frolov** 26:17  
OK.

**Aaron Bockelie** 26:28  
We need to just justify why it needs to be a special repo, and I'm not hearing that justification yet. It sounds very much like it just sits under the something, and it's OK also to not have perfect on the first try, so like we could do.

**Pavel Frolov** 26:39  
I would answer.  
I would answer.

**Aaron Bockelie** 26:44  
What's that?

**Pavel Frolov** 26:45  
I I I will answer your question. Kindly likely it was created as a separate repository because we need to produce artifact.

**Aaron Bockelie** 26:47  
OK.  
OK.

**Pavel Frolov** 26:59  
Using actions from GitHub. So if you make a decision to produce multiple binary artifacts from 1 repository, if it's suitable, yeah, we can go this way.

**Aaron Bockelie** 27:12  
Then I think that we should cross it off the list and then you can have it. You can create a a separate action pipeline for that inside of and just do that like we don't need to allow this.

**Pavel Frolov** 27:29  
Yeah, it it it works.

**Aaron Bockelie** 27:30  
Yeah. OK, so.  
I like that components are starting to sound very generic. Do you see this? How components? If you read through the list of components that we're allowing now, they're becoming very generalized. It could apply for any kind of software, not just JVL software.  
So for instance, I would probably want to have do you see where it says game test protocol?

**Pavel Frolov** 28:05  
Mhm.

**Aaron Bockelie** 28:08  
I think we should just call it test rotocol.  
Because you could go Latform test 360 test rotocol if you really needed to have a separate repo for it.  
And the idea of test protocol is kind of weird too. If you really start thinking about it, it's more like test.  
Specifications.  
Repository containing applications and tools for testing game communication with data center, ensuring correct data, blah blah blah. That actually sounds like it should just be tests inside of one of the inside of one of the other subcategories.

**Pavel Frolov** 29:13  
Mhm.

**Aaron Bockelie** 29:14  
Like why would you ever separate your test from the code like that?  
All right, I'm changing it again, changing my mind. I'm going to cross it out for now. I'm not going to cross out the description, but I'm going to cross out that asect of it.  
Let's talk about Qraid for a minute.  
Qrapid as a component sounds a lot more like a subcategory than a component, so maybe let's put this back over here. I might have moved that over there the other day.

**Pavel Frolov** 29:48  
It's quite, it's quite small.

**Aaron Bockelie** 29:51  
Yeah, the problem is, is that Q rapid is extremely opinionated and it's not really a component.  
We could call it QR codes. I think I'd be OK with that.  
But when you say Q Rapid, that sounds like a highly specific little tool. Even if it's a made, even if it's a subcategory, it's still its own little bubble of concern that runs on its own. So tiny product that you build.

**Pavel Frolov** 30:22  
I feel like it's a libraries that can be used in different products.

**Aaron Bockelie** 30:30  
So is it a library you created?

**Pavel Frolov** 30:34  
Yes.

**Andrei Bosik** 30:34  
Yes.

**Aaron Bockelie** 30:35  
Then it's AI think it's a subcategory. I really do.  
Something you maintain is a type of product that's used in multiple places.  
I would rather it be called tools Q rapid than tools blah blah blah something QQ rapid.

**Andrei Bosik** 31:07  
About test game test protocol, this is a part of only.  
If we move for test protocol test specifications to the sub category.  
It's separated part.

**Pavel Frolov** 31:22  
Actually I would agree with Aaron. I think this is more related to Omni repository as a additional feature that can be built from different.  
Excellent.  
To perform some testing of current state of repository and APIs and communications.

**Andrei Bosik** 31:41  
Yeah.

**Aaron Bockelie** 31:53  
So look what we've got now. I think I'm actually really getting close to being happy with what I see under component. Everything that's left are generally are generalized. I I don't know about personas. That's kind of a weird one, but.  
The rest of these.  
We could go switch companies to something else and then the components would still make sense.  
We could go to, I could go to another company and at the component level of this taxonomy, the components would still be appropriate, which is what I'm hoping for.  
Now at the subcategory level, now what we have is actually what your roducts are. Your subcategory is essentially your major product concerns that JVL owns.  
And the variance is sort of the leftover little bits and pieces that you might have. Did you add, did you add bundle there Andrei at the end of it under under variant?

**Andrei Bosik** 33:01  
Yeah, I move bundle to.

**Aaron Bockelie** 33:03  
Erfect O that way you could have like.  
AWS something's game bundle is what you're that is. Yeah, OK.

**Andrei Bosik** 33:12  
Yes.

**Aaron Bockelie** 33:17  
And I think the variant what's?

**Pavel Frolov** 33:17  
Applications Applications bundle.

**Aaron Bockelie** 33:23  
I mean, you could.

**Andrei Bosik** 33:24  
OK.

**Pavel Frolov** 33:24  
So.  
Yes.

**Andrei Bosik** 33:26  
Change your name.

**Pavel Frolov** 33:28  
Yes.

**Aaron Bockelie** 33:28  
I'm not saying every combination is makes sense, I'm saying it every combination is allowed.  
That's why we have a a notes attached to it. And you'll need to start to refine your notes because your notes are written in the understanding of what they are right now. And what eventually we'll do is we'll refactor these notes to be more generalized what it is.

**Pavel Frolov** 33:38  
Mhm.  
Actually when I wrote this description, I tried to make to make them more general than current implementation.

**Aaron Bockelie** 34:04  
Yeah, but like for instance, Scene Viewer is the way it's written is Scene Viewer is a component of the Omni game framework. So instead you could say Scene Viewer is a just pick a more generic name. Scene Viewer is a.  
System for viewing game scenes, for example.

**Pavel Frolov** 34:23  
Mhm.

**Aaron Bockelie** 34:27  
It's good enough. Like we don't have to. I'm more interested to make sure we can validate against all of these names. So let's talk about the rules of what it's going to take now to fit everything into these. I'm just going to just pick.  
A section in the sheet down here. I'm going to. I'm going to make a line.  
OK.  
And I'm basically rules for naming.  
And I think The thing is, is we can basically say rule #1.  
So the first rule I think that is going to be obvious is match obvious, match obvious names with the least number of kebabs.

**Pavel Frolov** 35:22  
From left to right.  
2.

**Aaron Bockelie** 35:29  
Right.

**Pavel Frolov** 35:30  
Mhm.

**Aaron Bockelie** 35:31  
Rule #2.  
OK, so the next one is one of the most important ones. If you have a repo you must have, but it doesn't fit in the allowed name filter or structure we've got. Discuss why it even exists and see if it should actually be merged as a branch.  
Or a path in an existing repository.  
So the test one is a really good example of this. If you've got a separate test set for Omni, why does it exist as a separate repo when it should be actually in the Omni repo?

**Pavel Frolov** 36:45  
Mm-hmm.

**Aaron Bockelie** 36:48  
And #3 rule 3 is this.  
OK, so here's the next one. If you find that you have work to do, merging 2 code bases together, directory structure and commit wise.  
Commit to that work in a positive way, understanding that reducing the number of repositories generally results in more clarity.  
And then let's do the inverse of that.  
In some cases, repositories become catchall and should be split. Just like merging can sometimes promote clarity, sometimes splitting repositories also promotes clarity. Separation of concerns is a valuable approach to maintain.  
Let's let's actually split that rule up, Speaking of separation of concerns.  
There we go, separate rule.  
Separation of concerns is a valuable approach to maintain when either when merging or slitting repositories.  
O You may merge repositories in order to maintain separation of concerns. You may join them as well.  
There.  
So if you take these rules, let's do one last rule here.  
OK, last rule, I promise.  
Some repository actions will be deferred. It is understandable that merging 2 repos together may be technically complex and require remediation or changes. If this is the case, set a deadline or due date.

**Pavel Frolov** 42:03  
What does it mean?

**Aaron Bockelie** 42:03  
Don't, don't. So OK, let's let's say we wanted to merge the tests from a separate test repo for Omni into Omni. OK, you can't just do that because it'll break everybody's tests and no one will know what's going on and it's be confusing.

**Pavel Frolov** 42:13  
Mhm.

**Aaron Bockelie** 42:20  
So you have to take some time to do it, right? Right. Like you got to talk to the people that own the tests. You got to fix, create actions in the pipeline and blah, whatever it takes. It's going to take a month to do it, right? Don't just like, Oh yeah, we'll get to that eventually. Set a deadline for it.  
And say that on this date this will be moved. It's very easy to lose track of that and this becomes work that the DevOps team can now focus on to make changes. So Andrei, as soon as you take rule number six under consideration.  
And realize that it has a a a due by date.  
This can encourage a developer who might own a repository to ask for help from the DeVos team to help merge the code bases together.

**Pavel Frolov** 43:17  
E.

**Aaron Bockelie** 43:19  
As an example.  
So you as in the DevOps team hear about this ask of let's merge the test for Omni into the Omni core repo together so we can delete the Omni test repo and have one repo, but no developer is actually available or has time to do that.  
Therefore, it's still important who does it? Well, it can land onto the DevOps team who can be focused and specializing and ensuring that continuity of capability from the one repo into the merged one still exists, and that means.  
Making sure credentials move over. Making sure actions are created or moved over. Making sure the messaging and all the other stuff is edited to make sure it works. A perfect use case of a DevOps team for managing your repos.  
That.  
Land. Well, like, do you understand what I mean by this?

**Val Levitan** 44:27  
Yes.

**Pavel Frolov** 44:28  
Yes.

**Aaron Bockelie** 44:34  
Right.  
So I think these are kind of the guidance.  
What we can now do is take all the existing repos.  
Go back to your plan. OK, here's the old repo. It's either gonna directly convert to this new name or it's going to need to be merged into some new named repo. And that's your action plan, right? That's literally your.

**Andrei Bosik** 45:07  
Yes.

**Aaron Bockelie** 45:11  
Your backlog of of actions to do.  
So where is that tab? Is that under the Final Draft tab?

**Pavel Frolov** 45:23  
Yes.

**Aaron Bockelie** 45:26  
OK, so given that we have this repo name change around here.  
At this point, now I have that code that I use that converted this list into Jason and made a nice little tool. I don't think you're going to really need or you'd be able to consume it yet. You can just stick with spreadsheets right now.  
Um, do you want me to copy that somewhere? Like I don't know.  
I don't want to force random work on you guys for stuff like.  
O what I'm seeing here is.  
Under the repo naming tab, clean U the crossed out items, then go under your final draft. Make sure everything fits the convention that we've got for now.  
And for things that don't fit, like I don't know where this is going to go, it's probably going to be a repo merge. You're going to merge something into something else and you can tag those as outliers. We're not trying to hit 100% perfect coverage on our first renaming pass.  
We're going to have some outliers about things we've got to merge and you can then plan that work.

**Pavel Frolov** 46:43  
Yeah, I I agree with planning this work because we can not do this immediately for all repositories because it will require to rewrite.  
Many actions.  
That can take more than one week for all the repositories, probably this more difficult work. So I I think the direction here can be.  
When we need to create a new repository, then we follow the rules and we set for some repositories that cannot be converted directly final date.  
When we are planning to rework this repository or to merge this repository?

**Aaron Bockelie** 47:48  
Uh, I don't know if you want to get into this level of detail, but I think you could do like a look up.  
Uh.  
Let's see look up vector.  
How do you specify another sheet? Is it exclamation point sheet 2A1A3?  
Not sure how you do that.

**Val Levitan** 48:18  
Yeah.

**Aaron Bockelie** 48:21  
But you could have a planned action on final draft. Basically, are you going to?  
Where did that go? Sheet 3.  
Um.  
You can merge, rename, or delete your repos, right? Those are your. Those are your choices.

**Pavel Frolov** 48:50  
Oh, or create new.  
Yes.

**Aaron Bockelie** 49:24  
Oh, it's V looked up.  
Vlookup.  
I am terrible at Excel.  
I don't know. Anyway, whatever.

**Val Levitan** 51:54  
Click.

**Aaron Bockelie** 52:08  
So on the final draft tab, I've got plan move date, plan to action, and optional plan target repo. So for those repos that you're planning on merging, you need to specify the target repo that you're going to merge it into.  
This basically becomes your backlog of work. When are you going to do this stuff?

**Val Levitan** 52:34  
I.

**Aaron Bockelie** 52:40  
I'll add responsible person as another column, so that's who's going to actually be responsible for the work.  
So like Andrei, are you going to move this or is it Pavel that's going to merge that or is it Sasha that's going to move this thing or whatever it is?  
Any questions?

**Pavel Frolov** 53:10  
No, no. But right now I see probably some.

53:10  
No.

**Pavel Frolov** 53:16  
Some possible problems because actually you do not know about.  
Um.  
About particular repository, is it easily can be switched to new repository? What's the dependency?  
Where this repository is used different actions.  
So highly likely it will look like you just take one repository, rename it to something else and try to find what is broken.

**Aaron Bockelie** 54:03  
So that's kind of all wrapped into the planned move date, right?  
O What you're going to do is.  
We put your plan out there. Just start with that. Well, we want to move things by these dates, OK?  
Then you're going to look at your action. Well, we're going to merge these two repos, and then you can go, OK, what is the actual plan for moving these things and merging them together? Oh ****, we have 57 actions. We have to rename these other things.

**Pavel Frolov** 54:21  
Mhm.

**Aaron Bockelie** 54:37  
This other reo actually is a resource for this one O. We actually have to rename the other repo 1st and change the date to which we're going to actually do stuff.

**Pavel Frolov** 54:45  
OK.

**Aaron Bockelie** 54:48  
You should be able to structure that inside of this here.  
Kind of negotiate it.  
This is the next step after having a naming convention.

**Pavel Frolov** 55:05  
So probably first of all we need to find dependencies for some repository understands that it can be dependent on something.

**Aaron Bockelie** 55:19  
Yeah, how would you?

**Pavel Frolov** 55:21  
Somebody.

**Andrei Bosik** 55:21  
Uh.  
I think we need to write in line each repository. The person who is working with this repository and he can this is first column.  
Second column, yes, no. Uh, this is repository use it in another actions for example or no.  
You need to change something, yes or no. I think this is the first step.

**Aaron Bockelie** 55:50  
I think if you structure it, if you structure it that way, you're going to create a massive boulder of work that's going to be hard to accomplish. I think you should be looking at them individually.  
It's not a yes or no answer, it's a it's a Gray area about how it all goes together when it comes time for changing them.  
O.  
I think the only yes no answer you could ask is does this repo have dependencies?  
And you could basically say inward dependencies or outward dependencies, right? Does something depend on this repo or does this repo depend on somebody else?

**Pavel Frolov** 56:33  
Mm-hmm.

**Aaron Bockelie** 56:36  
Other than that, I think you're going to ask for trouble if you try to resolve it in this table here. At some point this table needs to turn into Jira issues.

**Pavel Frolov** 56:47  
Yes.

**Aaron Bockelie** 56:48  
This is going to be become planned work inside of Jira with dates and targets for stuff with descriptions of the actual what you're going to do, the actions you have to remediate, the other repo dependencies, and the order of everything.  
That's planning the workout.

**Pavel Frolov** 57:06  
Hmm.

**Aaron Bockelie** 57:08  
And then you have your your repo naming convention sheet which allows you to have validated all the work for all of these repo names.

**Pavel Frolov** 57:09  
OK.  
Actually I have a question to Val.  
As we discussed yesterday, we need a new repository that covers all our top level architecture related to distributed server.  
A replacement for CMS and all entire system.

**Aaron Bockelie** 57:47  
Is the new replacement also called CMS?

**Pavel Frolov** 57:48  
So we need.  
I I don't think so.  
Uh, actually.

**Aaron Bockelie** 57:56  
Do you have a name for it yet?

**Pavel Frolov** 58:00  
I'm not sure.

**Val Levitan** 58:02  
Well, I believe that we all agree that the entire system should be called should be split into orchestration platform and observation platform and it will take the amount of services.

**Pavel Frolov** 58:16  
Split this.

**Aaron Bockelie** 58:20  
That's like a category level item. You could say observation is a category, but I wouldn't call it something like that. It's the it's the nature of the product though. It's definitely an observation platform or an orchestration platform.  
I would try to give it something more specific of a name.

**Val Levitan** 58:42  
Like a like a you mean like a product name?

**Aaron Bockelie** 58:45  
Yeah.

**Pavel Frolov** 58:46  
Yes, because actually orchestration observability, it looks like top level categories or capabilities of the product. It could be implemented in one application.

**Aaron Bockelie** 59:00  
Mhm.  
O if we have a.

**Val Levitan** 59:06  
So like like a flex backhand.

**Aaron Bockelie** 59:11  
Sure. I mean you could call it that if it was, if you wanted to use the flex naming convention. So you could go, you could call it platform flex back end.

**Val Levitan** 59:24  
Isn't that the most clearest form?

**Aaron Bockelie** 59:27  
I yeah.  
I mean, if you wanted to call it something cooler, I know you have a product called Miranda, which was always. I remember that was kind of an interesting name path to calling it the name, but it's kind of abstract. But if we just call it, let's just add it in the list and subcategory flex.  
Back end O now you have flex back end latform.

**Val Levitan** 59:47  
Or or we could do Omni. We could also do Omni. Omni feeds well in here.

**Aaron Bockelie** 59:54  
I think Omni has more to do with the framework that you're working on than the actual uh.  
Flex system in my opinion.

**Pavel Frolov** 1:00:06  
Uh.

**Aaron Bockelie** 1:00:06  
Omni games run on the Flex system.  
That's a statement that I think is true. So let's just run with flex back end for just a moment and talk about this. Flex back end is probably the only repo you need right now because you will have an architecture.  
Tree directory structure inside of it, and if it gets sufficiently complicated and you need to break it out into a component, then you can have there's literally a third row down. You could do platform flex back end architecture. That's a component.  
Component level name and then you would fork the platform flex back end into that. Keep your architecture definitions here and your code base and tests and stuff in flex back end.  
So it's about planting the seed, letting it grow, and then if it eventually gets too big, work it off, plant it a separate place, give it a different name that's more specific. Start with the least number of repos you can.

**Pavel Frolov** 1:01:21  
Actually today I tried to ask AI to advise what the name could be.  
Actually quite interesting suggestion example this one.

**Aaron Bockelie** 1:01:35  
Yeah.  
Oh, that's fun. See, that's that's kind of interesting.

**Pavel Frolov** 1:01:45  
Oh, probably something like this.

**Aaron Bockelie** 1:01:50  
Yeah.  
As long as there's a space in the name, this a carve out of of purpose in it, then I think you're OK.

**Val Levitan** 1:02:17  
OK, let's go with platform flex back end.

**Pavel Frolov** 1:02:24  
Mhm.  
OK.

**Val Levitan** 1:02:27  
OK.

**Pavel Frolov** 1:02:31  
OK.

**Aaron Bockelie** 1:02:36  
All right.

**Val Levitan** 1:02:37  
When can we have an absolute clean final excel?

**Aaron Bockelie** 1:02:46  
Well, I actually believe that the repo naming, aside from crossing stuff out, just needs to be deleted. I'll leave that to you guys to clean those off. And actually we're now at the point of defining on the final draft tab.  
Let's let's rename Final Draft to Planning.  
So I renamed that first tab to planning and now you need to start making sure that the validated repository names are all there from the from the original current repo names, and then you're gonna need to populate the plan move date, the action.  
The optional target repo, the responsible person, and you'll need to workout what's the complexity of these. Let's add. What was that other one I added as?  
Has dependencies, you could just say yes or no.

**Pavel Frolov** 1:03:45  
Or just a list of dependencies comma separated?

**Aaron Bockelie** 1:03:49  
Well, remember inwards and outwards dependencies, right?

**Pavel Frolov** 1:03:54  
Mhm.

**Val Levitan** 1:03:54  
We want to turn it into JIRA tasks, right?

**Aaron Bockelie** 1:03:58  
Yeah, so populate this first, get this planned out, then we'll load them into JIRA and each one of these will have in JIRA the specific details to be worried about for the each of the moves.  
Then you can knock the mall out one at a time. Here's the cool part.  
An AI tool with GitHub repo ermissions to move things and rename could look at the Jira issues and do it for you. You just supervise it. This is how you structure this out.

**Val Levitan** 1:04:25  
OK.

**Aaron Bockelie** 1:04:36  
I've I've done this several Times Now this way.

**Val Levitan** 1:04:42  
OK, when can?

**Aaron Bockelie** 1:04:43  
You know that I can bill, I can bill $30,000 for migrating 500 repos from from one place to another for a company and and basically spend only a week doing it.

**Pavel Frolov** 1:04:55  
How many changes? Repeat please.

**Aaron Bockelie** 1:04:58  
500 repos had to be moved and renamed from from data center to cloud GitHub and basically I let the AI agent supervise the work and got it done in a week. The fastest money I made in a long time.

**Pavel Frolov** 1:05:05  
Hmm.

**Aaron Bockelie** 1:05:14  
Not for me, unfortunately. I made it for another for another consulting company, but maybe someday I'll land those sweet, cushy contracts that way. I don't know.  
The point is, is that this is a migration of of sorts and we're doing the planning for the migration right now and making sure that we're we're doing it correctly.

**Val Levitan** 1:05:39  
OK, when can we present this final Excel?  
OK, I would like it to be polished final, so we could now migrate. We could trigger the button and say OK, migrate.

**Pavel Frolov** 1:05:56  
Andrei, can we do this until tomorrow?

**Andrei Bosik** 1:06:00  
Yeah, if you can, oh.

**Pavel Frolov** 1:06:00  
I need. I need two days.

**Val Levitan** 1:06:04  
I will book us for. I will book us for Friday.

**Andrei Bosik** 1:06:04  
I have a question.  
OK, but I have questions. We rename repository and we move this repository to your organization. It's a double step process or it's a one step process.

**Pavel Frolov** 1:06:10  
OK.

**Andrei Bosik** 1:06:25  
How about organization?

**Pavel Frolov** 1:06:29  
For me it looks like one way.  
One step.  
Create Actually we can create a new organisation, new organisations, I assume 2 organisations currently and then.  
Just move for currently existing repositories to new organization and then remove currently existing organization.

**Aaron Bockelie** 1:07:07  
Kind of arranging the drawing some lines around your stuff here. So you have target organization, target validated repository name, targeted plan move date.  
Planned action Optional plan target repo.  
Responsible person has dependencies inwards or outwards and description of work. These all need to be populated for each of the repos. Once you have that, these can be converted to JIRA issues and we can not track them in the spreadsheet because the spreadsheet can be thrown in the trash.  
And then we also want to make sure that we retain the repo naming convention system somewhere in a git repo, not a spreadsheet. And I can provide that code that I created or regenerate it for you or whatever you want to do there. But let's get out of spreadsheet plan for the naming convention and put it into.  
Functioning artifact.  
And at that point, it's just a matter of beginning to do the work.  
Once you've gotten this good enough with columns D through I populated on the planning tab, move them into JIRA and any further refinement of the work needs to be done in JIRA, not the spreadsheet anymore.  
We're preplanning to load the work into JIRA to get the work done.

**Pavel Frolov** 1:08:39  
Mhm.

**Val Levitan** 1:08:42  
OK, I sent an invite for one hour final revision of the Excel. That's what we're looking for.

**Aaron Bockelie** 1:08:52  
Let's not make it a revision. Let's make it a review. It should be populated fully at that point.

**Val Levitan** 1:08:57  
Yeah, I agree.  
We're good to go, guys.

**Pavel Frolov** 1:09:04  
Yes.

1:09:05  
Yeah.

**Val Levitan** 1:09:06  
See you Friday. Thank you very much.

**Aaron Bockelie** 1:09:07  
Cool. Thanks. Bye.

**Val Levitan** 1:09:10  
Yes.

**Andrei Bosik** stopped transcription