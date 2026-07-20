**Transcript**

14 August 2025, 12:04pm

**Val Levitan** 0:06  
OK, in in the chat I placed my high level understanding of what I would like to see accomplished today. That's my agenda. That's how I see things and this is my view.  
Of how HHR.  
The transactional products are current.  
CMS.  
And our TITCMMI framework needs to come together.  
Again, I'm not an engineer, so if I see something incorrectly, this is an executive summary of where I think we are, but by all means this is not.  
An engineering recap of any sort. I would like to draw your attention that there are GitHub, GitHub repositories created one for CMS.  
The CMS code located here.  
And uh.  
Aaron took a first path at taking all my recordings.  
And synthesizing those recordings into Uh.  
Uh, knowledge base of the subject.

**Aaron Bockelie** 1:42  
Kind of a collection of concerns that you know have been talked about over over the while, the while being like like what the last six months year I would say.

**Val Levitan** 1:42  
Do you?

**Nathan Carver** 1:56  
OK.

**Val Levitan** 1:57  
This does not include any of the HHR subjects because the recording recordings came in just recently and that does not include any transactional products.

**Aaron Bockelie** 2:02  
OK.

**Val Levitan** 2:14  
Because I wanted Nathan to be a part of this summary before I even.  
Brought it into in this sort of knowledge base. OK, so I would like to set the objectives of today. Today's meeting as the following. I'd like to review our current state of.  
Knowledge or ownership of things. I'd like us to be able to define our next steps.  
Determine the best way to integrate all of the above single pipelines.  
Establish MVP's. Assign responsible owners for each aspect.  
And then move forward.  
It seems like um.  
Nathan has a good grip of technical aspect of the transactional products, and Nathan and Pavel are slowly moving towards discussing the architecture.

**Aaron Bockelie** 3:26  
OK.

**Val Levitan** 3:37  
It seems like Will has a very strong grip on HHR.  
Um.  
I think that CMS we have extremely reliable and strong tribal knowledge.  
But we probably have very poor state of organizational.  
Aspect of it. I'm sure that all documentation is available, it just needs to be.  
Brought to light or groomed or brought in the corresponding repository and so this group that is here now could get a hold of this knowledge. So brought it out from.

**Aaron Bockelie** 4:14  
Yes.  
Yes.

**Val Levitan** 4:29  
Um.  
Tribal to.  
You know, for for use, for proper use.

**Aaron Bockelie** 4:41  
So I I'd like to take a take a pass at sort of describing what I've what I've seen Val as well, just just to kind of maybe, yeah, yeah.

**Val Levitan** 4:41  
Uh, we. Yeah.  
By all means, this is an open meeting that don't expect me to to lead you through the meeting. I'm I'm pretty well done. So let me let me pass on the torch now.

**Aaron Bockelie** 4:55  
So.  
Sure. So basically as far as I've been aware of the CMS tool and sort of how it's defined and how it works has been functioning and doing its thing for a long time, a decade, let's say there are now concerns about how the back end architecture of.  
How it holds data might live, for example. So it's sitting on a Microsoft SQL Server. It's sitting on infrastructure that is on the iron. It is a big monolithic code base, which I am not casting as good or bad. I'm just saying that's what it is.  
And there is a lot of inherited assumptions about why it is the way it is. And I think, and I don't want to speak for Dmitri on the call, but it's difficult to read into understanding the purpose and intent of what's going on in that code base.  
So when we want to then talk about changing it or adding to it like say an HHR feature or refactor the back end or take the whole thing and push it on to some other system or platform, it's sort of it's very difficult to do that and I think as we all have looked at large mature code bases, that's just sort of the way.  
Those things are, and I think that we're in this group together to try to figure out.  
How much we're willing to to to talk and change? How much are we willing to extend from there? And what's the general consensus for moving forward with this code base to make sure that continuity of capabilities with JVL still happens because.  
Without this code base, none of the games work properly. O Will, you got your hand raised.

**Will Jones** 6:45  
Yep. Oops, sorry I wasn't muted either. But my question is actually because I'm a little bit, you know, removed and now coming back in, where does Omni fit into this? Or I don't understand how Omni is related at this point.

**Aaron Bockelie** 6:57  
So.

**Val Levitan** 6:58  
All of it will be. All of it will be built on Omni. The the legacy, the legacy system is what we have today. As of now, moving forward, everything is built on top of Omni. Omni becomes an integral part of everything.

**Will Jones** 7:01  
OK, OK, so.

**Aaron Bockelie** 7:05  
Yeah.  
Yeah.

**Val Levitan** 7:13  
Of everything that we're discussing here.

**Aaron Bockelie** 7:14  
Hm.  
I'm gonna, I'm gonna point towards Dmitri and Pavel a little bit to add some clarity on how this currently interacts and how it will interact with Omni style games, the newer game framework for the games and also.

**Will Jones** 7:16  
OK. Thank you.

**Aaron Bockelie** 7:31  
I don't know, did we get all copy of the the Ng CMS Ng get repo to kind of just look at the synthesized concerns from your knowledge base Val. I don't know if that got shared out or not.

**Val Levitan** 7:44  
The link was shared. Of course the link was shared and was part of invite and now it's part of our chat. It's in the chat.

**Aaron Bockelie** 7:46  
OK.  
Right.  
So, so in, yeah, in that CMSNG space is.  
I'm not going to call them correct, but I'm not going to call them wrong. They are inferred things and challenges that probably exist based on all of the discussions that have been recorded over the last basically year or so of of thinking about what's going on with the tool.

**Val Levitan** 8:17  
Oh, no, it's actually close. It's closer to over 2 years. So we we managed to synthesize various meetings that deal with various subjects of the CMS and synthesize this knowledge with basically the effort was to.

**Aaron Bockelie** 8:17  
And I think.  
OK.

**Val Levitan** 8:36  
To highlight things, bring it to the surface. Aaron is right. It's not necessarily right, but it's not necessarily wrong. It's something that would be healthy for us to even start conversing about.

**Aaron Bockelie** 8:42  
Yes.  
Yeah, I would. I would consider it almost like an a set of inspirational. Like what could we and what should we be doing with this kind of thing? I'm not seeing all of the things in there, Val, but.

**Juan Martinez** 9:08  
Put in.

**Aaron Bockelie** 9:09  
Yeah, so there's basically it looks like there's just an architectural design doc in there. I don't know if the rest of the Oh yeah, there are there's set up as your issues or as GitHub issues. So look at the GitHub issues and.

**Will Jones** 9:20  
2.

**Aaron Bockelie** 9:24  
Understand that all of these are technically speculative things that we could be doing and considering and I think that as a working group going forward and that this is where I'm gonna stop and I want to hear Nathan and Will.  
Give some some direction here. We need to really think about. We can't redocument everything that's existed for 10 years, but what we can do is sort of make assumptions on how certain pieces of this work and decide.  
Where we're going to focus the next set of effort for this and then slowly eat the elephant a little bit at a time over the next couple years, basically.

**Val Levitan** 10:14  
As a matter of priority, let me start by saying that the transactional products need to be in the market by July 1st, 2026. Let me elaborate on this date.

**Aaron Bockelie** 10:28  
Yes.

**Val Levitan** 10:30  
July 1st, 2026 is when Georgia legislation turns on the key and says as of this date you must transact a certain way in order for us to have our products even considered by the operators in Georgia.  
On July 1st, it needs to hit or it needs to start hitting the market approximately January of 2026. That means the beta discussions or beta transactions. By beta I mean.

**Aaron Bockelie** 10:54  
It.  
Yes.

**Val Levitan** 11:09  
Having our warehouse in Georgia showroom in Georgia acting as a showroom.  
As a touch and feel for our operators, it needs to happen sometimes.  
Some of the products are at that stage and some of the products are behind, but the priority here is on transactional architecture.

**Nathan Carver** 11:46  
OK. So if my understanding is the the priority of the transactional architecture coming up July 1st of next year and the CMS has to be part of that to some degree. So how do we integrate CMS support into that transactional architecture between?

**Val Levitan** 12:03  
I don't know.

**Nathan Carver** 12:06  
Here and now, is that where the push for CMS is coming from?

**Val Levitan** 12:11  
Well.  
Yes, but the short answer is yes, but.

**Nathan Carver** 12:14  
OK.

**Val Levitan** 12:21  
I mean the short, the shorter answer is I think it's possible, but I'm guessing.  
Uh.  
A little bit longer answer is why don't I leave it with you and you start poking at it and.

**Aaron Bockelie** 12:33  
Yes.

**Val Levitan** 12:37  
We we we can come together again and hear what you're saying instead of me speculating.

**Nathan Carver** 12:45  
Is the CMS? Is there something in CMS that is required for the transactional system to function? Like is there information that we have to bridge like?

**Juan Martinez** 12:46  
And.

**Nathan Carver** 12:58  
Or can a transactional system exist without the CMS being involved? I I don't know enough of the the workings of the business in the back office to know what data exists and what needs to support each other.

**Juan Martinez** 13:17  
I I would say Nathan, your current customer management is done through CMS. The the the tracking of a master, the tracking of a a location or client, the assignment of that terminal ID we discussed earlier today.

**Nathan Carver** 13:22  
OK.

**Juan Martinez** 13:35  
But I I guess my question to the team, because the transactional products are new, why? I don't know how far along we are on Omni as in terms of the CMS replacement, but would we not launch a new CMS?  
Specifically targeting the transactional products in our meetings we discussed you know the need for a player dashboard which today a a customer dashboard which today customers don't really interact with the legacy CMS to create their own.  
Warehouses and locations and and managed products. Does it make more sense to just start on Omni for this implementation and only keep CMS for the legacy machines that need it?

**Pavel Frolov** 14:27  
Yes, Juan, good question and in short I will answer yes, it it will be easier to start new development for transactional product.

**Aaron Bockelie** 14:37  
OK.

**Pavel Frolov** 14:41  
In new server in new approach because actually for this product we do not need any knowledge about currently existing machines. It's absolutely independent.  
Some some statements related to current design. It was initially based on the statement that the only internal user is available on the system in CMS.  
Internal, I mean only user created by JVL and most of them just employee, JVL's employee, but we already had lots of requirement to switch.  
To client portal first, but right now it's renamed to observability and orchestration platform that you require as different users.  
Just some, some of them just operator. We need access to all of machines here to rate, probably some customer just buy.  
Some machines and want to to change settings but for transactional.  
Oh.  
Devices, as we already talked today and yesterday, I think we need to provide access for operator who has its own Flex POS, Flex Tower, Flex other devices.  
And want to set up his locations, assign different devices to this location and operate his flex transactions.

**Aaron Bockelie** 16:57  
Um.

**Juan Martinez** 16:59  
So just to echo a similar product, you know every makes ticket redemption ATM kiosk and and they allow locations to manage their own equipment and infrastructure but through a locally running.  
Application and at the higher level, us, the manufacturer would control user log ons and that and even then that's all done through Active Directory without us necessarily getting into the business. So do we believe that?  
That the master location needs to actually connect to our instance of Omni or sort of a local application of Omni to self manage their products. It's just a bit scary. I can't think of a situation.  
Where me as a customer has been able to log on to the manufacturer's master system with this level of access versus just downloading game brochures and par sheets and that kind of stuff. I've just had any concerns with with.  
How we would isolate, you know, the third parties now logging in directly to Omni.

**Pavel Frolov** 18:20  
Omni is just framework via switching for new land based game design.  
But answering your question.  
About operator and what's the best way for operator to manage his machines?  
I assume that probably it will be simpler if he just logins to our system and see only his location, only his machines, only his devices and.  
Change everything he want without actual setup screens on the devices.  
So it's better to for me it looks like it's simpler to to have only one place where all the settings are located instead of moving.  
Go into location, find device, switch it to setup mode and pass through the settings on this screens and so on.

**Juan Martinez** 19:48  
OK. And and you envision that this would just be a a web site per SE that the client could just go to to do this, OK.

**Pavel Frolov** 19:55  
Yes.

**Val Levitan** 19:58  
But also using the Active Directory protected by Microsoft, that's how we separate our customers, isn't it?

**Aaron Bockelie** 20:08  
So I'm going to interject here for a minute and I'm going to, I'm not going to add any direction. I'm just going to tell you what I observe. We're invoking Microsoft Active Directory, which actually isn't even Active Directory, it's entrepreneur.

**Val Levitan** 20:13  
Mhm.

**Aaron Bockelie** 20:23  
So we're actually saying we're talking about an identity management system. That's one of the major components. Another thing that we're invoking is we're talking about a web interface. So we're basically saying we need some sort of interface that's going on here.

**Nathan Carver** 20:25  
So.

**Aaron Bockelie** 20:39  
Another thing that we're invoking is what is essentially machine management. So what patterns do we have that are that we have that are unique to uniquely qualified for managing these casino machines?  
And to what degree of control do we exert over them, over other frameworks or things that exist in the world to manage machines like this? Because what I'm ultimately thinking about is what other patterns exist to manage, say, point of sales machines at scale.  
Or point of sale software. That's like one of the very similar things that I see this happens to have. Like if you could go to any point of sale system in a modern large retail environment and add a slot machine game module to it, you almost have a slot machine system that's managed in the same way.  
So I I'm not trying to push any direction here, I'm just asking is this the level we want to be thinking at or do we want to be thinking at a higher system scale level to understand what the what this thing's supposed to do?

**Juan Martinez** 21:50  
Aaron, just to clarify, are you sort of saying why if there there's definitely platforms out there today that are managing all sorts of, you know, think of Square as an example, you're saying why don't we use an existing platform and just modify as needed?

**Aaron Bockelie** 22:01  
Right.  
That's potentially One Direction, but what I'm also asking is why are those things easier or potentially more effective to manage systems than the problems that we've identified with the one with the system we've got?  
What architectural differences are there that cause those things to scale better, to be cheaper to operate, to provide better reporting, to provide better activity, whatever those, whatever those deficiencies are that we've identified so far?

**Juan Martinez** 22:37  
Sure.

**Will Jones** 22:39  
And if I can add just maybe to to get clarity to that, I'm trying to understand the requirement space. I definitely don't. I don't know that yet from this discussion what's expectations. Obviously I've heard there's a you know the expectation of of control these machines, the configuration of these machines and.  
Allowing the customer to do that, but also having that you know in the presence or at least knowledge of JBL exactly what the configurations are. But beyond that too, I don't know if is is this envisioned as offering some form of player tracking to a casino that doesn't have the ability to track players? Is this only talking about?  
You know, transactions in terms of monetary transactions at the machine itself or are we going to be offering some kind of ticket redemption in in a casino that doesn't have it. So I guess I want to know this space. I imagine the CMS right now may have many of these features and you guys have an idea of what we're talking about.  
To offer based on our current offerings. But what is what's being asked of this is an MVP anyway. What are we thinking? You know, what are the primary functions of this system?

**Juan Martinez** 23:50  
I I would say, Will, good points. It's not necessarily player tracking the the particular markets where this transactional products are gonna go are, you know, bars, restaurants, gas stations where there's only.  
You know that best case scenario, 9 machines allowed by law typically. So these are smaller environments with a lot of transient play going through them and there is no player tracking done today and I don't think that that's something that we would need to be concerned with at least for right now, but.  
Transactional money transactions, gift card, debiting and crediting the tracking of associated service fees with those transactions.  
And the device status? Is this point of sale device up and running? Is it down? If I need to replace it, how do I auto configure the new device to minimize work? Those are some of the key points.  
Of you know, and by location we would want to know, hey, OK, everything is green at this 711, so all the devices are are up and running and maybe we can hover over one of them and see the volume it has.  
Done for the day. And when I say, you know, the customer should be able to do that and we would, you know, there's a balance there where you know they need to understand that we know everything they're doing now because these devices are all connected to the cloud.  
So there's there has to be a balance there where we're protecting some of the operators privacy, yet we do retain access to that information.

**Will Jones** 25:42  
Is so in terms of the accounting was one of the categories I gathered from what you you were saying. So reporting capabilities of the site to report against what happened at their own property of JBL to know exactly what happened at a property.

**Juan Martinez** 25:46  
Yes.  
Yeah, but very, very important because the transactional fees directly hit the JVL wallet. So we want to know exactly what happened when it happened in the event of a dispute, a mispayment, an overpayment or some apparent attempt at fraud.  
And then to truly reconcile with our customer to say, hey, for this month you owe me, you know, $10,000 and here's all the data to support that.

**Will Jones** 26:27  
OK. And when you were talking about devices on this, I obviously can gather terminals of device. Are there other devices for ticket redemption that are roughly terminals with just some kind of ticket printer and bill acceptor?

**Juan Martinez** 26:44  
Yeah, there there that will be two instances of a device with an E wallet that's in the physical form of a of a ticket and then the traditional Tito ticket as you know it will will be in play and then there's a a smib.  
Type device at the machine as well that's gathering the transactional data and the cash outs and insurance at the machine level.

**Will Jones** 27:10  
And that's interacting with another system beyond JVL as well.

**Juan Martinez** 27:15  
Um.

**Will Jones** 27:15  
This bit.

**Juan Martinez** 27:17  
There the financial output is is sent to Georgia Lottery and then the Georgia model. So there is a SAS connected system that's recording the games transactional information, but not this financial transaction.  
Directly, that system will know that a cash out of $10 occurred, but not necessarily that we move that $10 to a MasterCard gift card and that we charged a $2.00 service fee to do that.

**Val Levitan** 27:48  
Well, we also interact with a payment clearance house.

**Juan Martinez** 27:55  
Yes.

**Val Levitan** 27:56  
But that's another interaction.

**Will Jones** 28:04  
So we've got two, is that that was only two right that we have right now, one interacting with some form of regulatory body or a extra accounting piece and the other one interacting with a transactional, you know, financial transactional system.

**Val Levitan** 28:21  
There is a third one. I don't know how you want to treat it, but right now 90% in 90% of locations in Georgia have a pre-established architecture and so as a point of entry for us and the cheapest.  
Point of entry entry for an operator is for us to tap into this existing architecture, this system that exists today.  
We're grabbing a set of signals coming out of a machine and we are based on those, based on that information, we're going to issue a validated transaction issue.  
A card.  
And print the ticket. So we wedging ourselves in that system forcefully, but it's not really a true interaction per se.

**Will Jones** 29:16  
Mhm.

**Juan Martinez** 29:17  
Yeah.

**Will Jones** 29:21  
But that's like that's like a third party CMS system that we would be interacting with from the terminal, no?

**Juan Martinez** 29:27  
It's a serial. Think of a low cost slot accounting system that is all serial based that just collects the cash out signals and sends them serially.  
To a printer today and and we will intercept that final output to the printer, which includes some data fields that we will then verify to say, OK, legacy system, you said that machine #4 had a cash out of $10. Here's the transactional number, here's the dollar amount.  
The date and time and we verify that and then we now have the ability to convert that data into a gift card through one of our transactional point of sale devices.

**Will Jones** 30:13  
OK, got it. So in that that existing system is running on some proprietary serial protocol. Maybe it's a standard, but something outside of casino, normal casino standards. Yeah, OK.

**Juan Martinez** 30:22  
Yes.  
Yeah, yeah, yeah. RS485 and RS232. So the the most hackable, insecure thing.

**Will Jones** 30:31  
OK, but that's it.  
But that's, yeah, exactly. But that's at the actual terminal, correct? It's like within the locked cabinet.

**Juan Martinez** 30:38  
Yeah, it's, yeah, there it's a Daisy chain device from machine to machine and then the the final board communicates with the printer.

**Will Jones** 30:43  
Yeah.  
OK.  
So is it assumed in this in this requirement or you know in in what we're talking about for this architecture is it assumes that we can definitely have our services hosted somewhere in a cloud service that there may be an on Prem device that needs to be there but.

**Juan Martinez** 31:18  
Yes.

**Will Jones** 31:20  
Beyond that, our services do not have to run in some type of server room that's located in Georgia or some other place.

**Juan Martinez** 31:26  
Correct. I mean we're we're the the restrictions or regulations governing this transactional product are are very loose and and favorable to us. So yeah we we've discussed as much as having a a beautiful Cisco grade looking on premise server to the more realistic cloud based.  
Solution, both options are available to us. So yeah, I think we're leaning towards the cloud solution with some processing being done on site by one of our devices in a master slave sort of configuration.

**Will Jones** 32:01  
And for the evolution or the the utility of this back end system, the existing one, but obviously I'm making the assessment. This is not just Georgia, this is something that's greater good when it moves to other markets.

**Juan Martinez** 32:15  
OK.

**Will Jones** 32:17  
Is it safe to assume that the cloud environment is going to be acceptable there or do we have to have an on Prem solution as well?

**Juan Martinez** 32:25  
The Val jump in if you want, but I think that the markets that we're looking at today are do not regulate this component. Their regulations end at the skill machine and accessories like this are unregulated for lack of a better word.

**Val Levitan** 32:45  
Yes, correct. But I would like to remind this group that we're not dealing with the the subject of transactional equipment only. We are saying that we we're we're going into the market from a number of angles. Transactional equipment is only one angle.  
I don't know what architecture will be required by HHR or we have built a significant.  
Technological debt in the current CMS. Some of the applications that we are using are not longer available or cannot be updated anymore or needs to be changed.  
So that subject needs to be addressed at some point because we do have traditional slot machines in the field and we want to.  
Interact with them at some in some way. So yeah, I mean the transactional.  
Products.  
State priority. I mean calendar priority, but not architectural priority.

**Will Jones** 34:07  
Hmm.

**Juan Martinez** 34:10  
Yeah. And and yeah, we'll just jump on what Val did say the, yeah, our component which are the machines, those we we continue to have to adhere to whatever the governing regulatory rules are as well as the GLI approvals and all that that remains as is.

**Pavel Frolov** 34:12  
Oh.

**Juan Martinez** 34:29  
Val and then all all go ahead.

**Pavel Frolov** 34:30  
Oh.

**Val Levitan** 34:31  
And and that.  
Just to just to continue with what you said and that component has accumulated significant technological debt in it.

**Juan Martinez** 34:41  
Yes.

**Pavel Frolov** 34:42  
Uh, actually, um.  
I think we we need to to understand that current system and future system will reuse lots of common components like passport.  
Management, remote initial setup management, leases management, user operator, location management, what else? Analytics reporting.  
So this is a common modules that can be used both for machine separation and payment devices operation.

**Val Levitan** 35:31  
And maybe this this is not a timely comment, but simply because the way the conversation flows. I just want to say that Pavel skillfully.  
Identify, identify those things as modules. I don't know whether to call call the modules or applications or products. I don't know what the right word for or features or capabilities. I don't know what it is, but they're not identified and as Aaron.

**Pavel Frolov** 35:54  
Or features.

**Val Levitan** 36:03  
Said in the beginning of the conversation. Right now CMS sits in GitHub as one monolithic repository of code with heavy tribal knowledge and and luckily we have this tribal knowledge and we have people that.  
We retained the developers that were retained, but that needs to be extracted, extrapolated, divided and presented in a form that.  
Executives and developers could relate to each other in some verbal concession.

**Juan Martinez** 36:43  
And then Aaron, a few of those modules that Pavel mentioned are part of the main driving force while that these we could not use an existing off the shelf POS type of management system, the the ability to disable a device.  
To, you know, detect if hardware has been swapped out by the customer or to lock it down for non-payment or other issues. That is normally not something I've ever seen in in in the POS administration.  
Tools that I've ever dealt with.

**Will Jones** 37:26  
Think to sorry, Aaron, I'm going to put one word in to say something to lead you that we have to consider what components are going to have potential regulations on top of them or have to go through approval as well, so.  
If there's things that are living on the device itself, you know, they're already in an area that we should call like the the red zone. We need to make sure that they're not going to be, you know, require approval every time we make a change. So at least the interaction with the device itself that is regulated.  
We didn't flag anything that's going to be that's not going to be able to live off the machine, that's not going to be able to be changed easily and make sure that that stays stable and that hopefully then is, you know, done once successfully and kept outside of it. I believe that that leads into the logic.  
Question of what kinds of modules or what features are we going to have available? What's available right now? What can we pick apart? And if we need to evolve it into something new, we do it without disrupting the rest of the features that continue to work. There may be a lot of.  
Spaghetti going on. So that's the, you know, that will be the place to understand how intertwined it is before we know what how you evolve. So anyways, I'll step back.

**Aaron Bockelie** 38:49  
And I yeah, and I just want to add that I have. I am very aware of my bias of not knowing these systems and not knowing kind of what is going into them. I'm talking about the best fit that I have experienced in my life, which is.

**Juan Martinez** 38:49  
Yeah.

**Aaron Bockelie** 39:07  
Point of sales and payment systems of that nature, and that's the best pattern that I've got. There's clearly a set of necessary components that make up a CMS to be able to make this work. I think that.  
Also, my other bias is that I have nowhere to read about understanding how JVLCMS has been put together and it's it's functional components. I don't know if Nathan.  
If you've got a better grasp on that, or you know Will, if you've seen enough to know this, I see Juan kind of nodding because I think Juan, you've touched enough stuff over your career so far to know what it's supposed to look like, but I think there is no.

**Will Jones** 39:53  
Totally.

**Aaron Bockelie** 39:55  
Place that describes the the topological concerns of all of the pieces that are necessary to make this work correctly, and that makes it incredibly difficult to even discuss what we could change and what's going on, because what it means is the only people who can operate it and fix it.  
Are the ones aware of how it's supposed to work to begin with, which is a very small circle.

**Val Levitan** 40:18  
But just in response to what you said, and I agree with everything you said, however, just one caveat.  
All this knowledge and I'm going to say and the documentation for the most part exists. It's just not.  
Organized in a form that you would like to have it. It it's not organized in the form of proper repositories and there is no storyboard that could somebody could say OK.  
Press read me uh uh.

**Aaron Bockelie** 41:00  
Yes.

**Val Levitan** 41:03  
File and it would outline the whole story of it, but it exists, it just we need to bring it to surface. For example, if I ask Dima where is the block diagram or where is the schematic for something, it most likely exists.  
Or most likely could be put together very quickly.  
And the team is very willing to bring it to surface. Nobody is holding information. It's just these guys are super busy.  
Super dedicated, super knowledgeable and they have everything available to us. I mean, if Will and Nathan will start pulling.  
You know, pulling the rope and will eventually come out from the hole. It's it's just I I have no doubt about it. I will jump in if you have something to add. Maybe from an engineering perspective, maybe I'm not seeing something, but that's that's my perspective.

**Pavel Frolov** 42:02  
Yeah.  
You're right. I think we can get lots of information, schematics and so on, but not structured, not placed in one report. It exists in many places, especially keeping in mind that most of.  
Of course was done more than 10 years ago and lots of information posted to obsolete conference page that nobody looks right now.

**Aaron Bockelie** 42:36  
OK.  
So from kind of an advisory.

**Val Levitan** 42:41  
But but but it's like but but but it's available. It's it's there. It's available.

**Aaron Bockelie** 42:46  
From kind of an advisory perspective of just telling people how to organise their software projects and talk about how to share organisational efficiencies, one of the patterns that we probably should consider adoption is how can we bring?  
The documentation closer to the code base. I think that having that in that space would be sort of a way to.  
Remember that how things are put together. You know, we have potentially efficiencies to be found from AI coding tools that didn't exist before to be able to read these documents and help us understand what's going on.  
It also gives us the ability to maybe.  
Tie in unit tests and integration tests and functional testing and all the other types of testing that should be going on with this platform a little closer to reality too. Closing the loop with requirements, closing the loop with understanding.  
How everything's sort of tied together and working. I'm not saying we need to throw the code base away and start over again. I'm just saying we need to make sure that however it is built, we understand what the purpose of those are, because if we can understand the purpose.  
Then we can have a conversation about, say, changing the database back end, right? It's like I've clicked around through the repo, I see all these SQL scripts and I thinking from the perspective of, well, someone has talked about maybe changing the database infrastructure slightly. OK, well, all of these are of a particular.  
Another type of flavor of SQL. A lot of these SQL instructions are specific to single thread locking transactions and so forth, and that you can't just change that one piece and hope the rest changes. It's a whole holistic approach has to occur.

**Juan Martinez** 44:53  
Read.

**Val Levitan** 44:56  
I I think everybody's nodding, nodding their head in full agreement, and now it's just a matter of rolling up the sleeves and getting things done.

**Pavel Frolov** 44:57  
It.

**Juan Martinez** 45:15  
And go ahead. OK. No, I I was just gonna point out also, you know, one, one of the things that are different at JVL versus all of the other manufacturers, Val, is in fact that passport.

**Aaron Bockelie** 45:16  
So yeah, no, no, go for it.

**Juan Martinez** 45:31  
Lease and control of the RIS function. Are we open to considering as we move to Omni to do away with that with regards to the EGM and keeping it only for transactional?  
You know, the managing of somebody else's machines is not something as we focus on the US market, I think you know, having to have a lease expire or to track that a customer removed hardware that becomes less and less.  
Of value to us that that that's just no one else is doing it and I think it's it slows down our ability to support things.

**Val Levitan** 46:19  
I I just would like to comment that I I don't think it's a matter of removing these features as the the problem with this is that we we didn't connect the last element of design to it.  
And the last point of this feature or this capability should be when a slot machine has been fully paid, then the lease feature should be.  
Turned off.  
Or set to indefinite and and management passed on to an operator.

**Aaron Bockelie** 47:00  
And I and I think that when you to to interrupt because I want to, I want to take a side journey on that leasing operation that you're talking about for a minute, Val. When you talk about leasing, you are extremely comfortable with that as just being part of the system that makes sense.

**Val Levitan** 47:01  
And not to say.

**Aaron Bockelie** 47:18  
But the phrase separation of concerns is floating in the back of my mind right now. We're not.  
I'm not sure if we're clear about the separation of concerns about how these things work, because what we've talked about now is a seamless process of going from owning a machine, not owning a machine to owning a machine to converting a lease to an ownership kind of thing.  
And yet the actual functional distinction between the two is removing some sort of control from the machine to allow other people to use it as they as they wish, and so connecting the dots between those two things.

**Val Levitan** 47:57  
To, to, to, to a point.

**Aaron Bockelie** 48:01  
To a point, right. But there's some level of control. And so therefore, actually, we're not talking about the technical process of leasing at all. We're talking about the technical process of managing the machine state and defining what that machine state's supposed to be.

**Val Levitan** 48:18  
I agree. I I agree.

**Aaron Bockelie** 48:19  
and being very clear about those.

**Val Levitan** 48:22  
I agree that the taxonomy is erroneous.

**Aaron Bockelie** 48:27  
Oh, it it's not that it's erroneous. It's that it doesn't. It's not clear.

**Val Levitan** 48:33  
No, it's it's simply erroneous. It was. I actually remember how the term lease came to life. It was done between Efim and Boris, our VP of engineering at that time, and both of them hardly spoke English.

**Aaron Bockelie** 48:40  
Mhm.  
Yeah.

**Val Levitan** 48:50  
So the first thing that came to their mind that was closest to a description was lease. And so they called it lease because it was a single word and they both understood what it meant. And you know it the the the the capability was packed as lease.  
But yes, it's totally erroneous. You know, it got stuck. It got stuck at JVL, but it doesn't mean that it's the right taxonomy.

**Aaron Bockelie** 49:07  
Yep.  
Well, that's.  
Having having been digging through a lot of archaeological expeditions at JVL over the last couple of years, I can say that language terminology confusion is a significant factor when it comes to understanding why things aren't working.

**Pavel Frolov** 49:27  
OK.  
It's like, no, you need to buy.

**Juan Martinez** 49:31  
Yeah.

**Val Levitan** 49:34  
Let's focus on the future.

**Aaron Bockelie** 49:35  
Yes, Will, your hand is raised.

**Juan Martinez** 49:35  
Yep, yeah. But just to, I mean Valvo, the the function of lease does match the the word lease that if the machine doesn't yet belong to the customer, it's technically still property of JVL, but when we switch from.  
100% paid to the customer owns the machine. The customer cannot pick up his own machine, move it to another location and disable the dollar denomination because this is a low wager without our intervention.  
And the question is why? Why do we want to? Why do we want to take that workload on?

**Val Levitan** 50:15  
We don't. We we don't one. We don't. I can assure you that we don't. These are JVL did not come from Class 3 gaming and these are.

**Juan Martinez** 50:19  
OK.

**Val Levitan** 50:29  
Inheritory.  
Logical deficiencies in design, but there's no desire to control something that doesn't belong to us. I mean, yeah, we came from communist country, but we're not really communist. We don't want to control anything.

**Juan Martinez** 50:35  
Sure.

**Val Levitan** 50:48  
When machine belongs to somebody else, we don't want to retain any ownership. We don't want to be bothered. These things should stop to exist, but the design logic stems from the previous.

**Juan Martinez** 50:48  
Yeah, yeah.

**Val Levitan** 51:05  
Sense of we operate machines. We were the company that were operating machines in Latin America. It was a different mindset. Everything was hinged to a contract.

**Juan Martinez** 51:13  
Yep.

**Val Levitan** 51:21  
Operational contract and the contract was in the center of all the movement of the machine. So it was just totally different logic. And then we started snipping pieces apart and because we didn't need this and we didn't need the contract and we started.

**Juan Martinez** 51:30  
Sure.

**Val Levitan** 51:40  
To disjoining them. So there is a lot of legacy architecture thinking that we're dealing with right now. And when I talk about technological debt, maybe I should also talk about architectural debt.  
That needs to be addressed, but definitely you're 100% correct. I'm with you on it. There's absolutely no desire. I can assure you this meeting is recorded here. I'm going on the record. I'm saying there is no desire to control machines that do not belong to us.

**Juan Martinez** 52:17  
Can you repeat that for series?

**Pavel Frolov** 52:20  
Yes.

**Juan Martinez** 52:22  
Oh, no. So good. So I I I'll interject this as a footnote then. So Pavel, we we need to be mindful of Omni removing the RIS.

**Val Levitan** 52:23  
It.  
Well, well, Omni, it the way Omni is, we're approaching the design of Omni is all the setup screens are basically emulating the.

**Juan Martinez** 52:47  
Emulating the what, Val? I'm sorry. Oh, OK, OK.

**Val Levitan** 52:48  
So remote initial setup or any sort of lease passport, everything could be done manually on the machine without remote access to the machine. So when machine is sold, all of that access could be.

**Juan Martinez** 53:01  
Yeah.

**Val Levitan** 53:05  
Or or passed on to an operator and an operator could do whatever they want. Interestingly enough, I believe that in a route environment in America like in where is it in Pennsylvania, Michigan.  
Whatever that exists, I think that the same features would be great for individual operators.

**Juan Martinez** 53:30  
Yeah, as long as 100% agree with you, as long as that RIS USB is not tied to the serial number. If if me as an operator, these are my 10 favorite settings. Give me an RIS that I can move from machine to machine.  
That's a dream, Val, but.

**Val Levitan** 53:48  
However, it should be designed. I I don't know. I'm not getting into the design. I'm not designing right now for Pennsylvania or Michigan. All I'm saying that a lot of those interesting features that came.  
From in our legacy products might be of an interest to an operator to 1 degree or the other, I I don't know, but this is something that we need to address at a different meeting.

**Juan Martinez** 54:14  
Yep, great.

**Val Levitan** 54:15  
But as a.

**Aaron Bockelie** 54:15  
Speculative speculative feature development's very expensive.  
Basically.

**Val Levitan** 54:23  
Here comes the voice of reason.

**Juan Martinez** 54:25  
When you say speculative.

**Will Jones** 54:27  
Yeah, but it is very expensive, Aaron. But these ideas of having a route operator in the middle to be able to do, you know, additional control, they are, I think so good for the architects ears because they understand the extensibility that's going to come in the future. Don't develop it today.  
You've got to understand that to lay it out so that it's much more adaptable to what comes next, so that you've actually already realized the future environment or future requirements that have never been asked how they fit into the system. So anyway, speak them. They're wonderful news to hear those things, but don't expect them.

**Val Levitan** 55:00  
J.  
Just just like just go ahead, go ahead.

**Aaron Bockelie** 55:05  
Yeah, I and I and I think, I think that's really well said and I and I say that as a challenge to change it from speculative to concrete. Let's make sure that we really understand.  
How these potential operators would consume this seemingly valuable feature right now? Let's let's not make, yeah.

**Val Levitan** 55:26  
Just like I just like I think that as a manufacturer these features isn't over design. I feel that the the Class 3 manufacturers like IGT and Bally's of the world never thought about these features from an operating perspective.  
There are as much as they are under designed or under thought.  
The the operators would appreciate these features, would the the.

**Will Jones** 55:55  
I I'll say that. I'll say that for sure. That is exactly right from coming from a larger, you know, organization and what was spoken in the room. If I can take the moment just to say the two things I was going to add that what was mentioned just a moment ago were one, I think you were challenging the idea.  
The lease and the features that are in the existing system and not necessarily needing them in the future system, at least for certain situations. I would say it's important to identify what is going to be an integral function, what's an optional feature and make sure that we adapt to that. So if this isn't a required feature, then I would in all market.

**Juan Martinez** 56:34  
No, no, it is a required feature in the sense of I 100% agree with the transactional products having the feature, but now knowing that the intent with Omni is to on the EGM side to not necessarily force.

**Will Jones** 56:35  
It's.

**Juan Martinez** 56:51  
The RIS concept that that you can manually modify the machine after the fact that satisfies everything that we keep passport lease management tools for transactional products and that it's optional on the EG Ms. That would be ideal.

**Will Jones** 56:54  
Mhm.

**Val Levitan** 57:08  
Optional only optional only if AGM does not EGM does not belong to JVL. But let me let me now put my legal hat on and to say that if EGM is financed.

**Will Jones** 57:09  
So.

**Val Levitan** 57:23  
It technically is JVL's EGM up until last dollar is paid against the invoice and the remaining amount of invoiced value is equal to 0.

**Juan Martinez** 57:36  
Great.  
Agreed. Yeah.

**Val Levitan** 57:38  
I'm being extremely technical and that period might be, from our experience, as much as three years.

**Juan Martinez** 57:47  
Uh, yeah, most casino leases are. Yeah, can go that long, absolutely.

**Val Levitan** 57:51  
And during three years, we do care what bill acceptor they put into it.

**Juan Martinez** 58:01  
Yes and no, Val. I would agree. In South America we care, but I I can tell you that myself and Felipe, the first button we uncheck is hardware tracking because it becomes a big pain in the ****.

**Val Levitan** 58:14  
No, because it's no, because it's not. The design was never finished. But if you finish the design and you can truly auto detect the hardware that's being put on and you put permissions which hardware is allowed, it's a very useful feature when you own the machine.

**Juan Martinez** 58:20  
OK.

**Val Levitan** 58:33  
Chains.  
For example, one of the features on the bill acceptor is the acceptance rate.

**Juan Martinez** 58:42  
Yeah.

**Val Levitan** 58:43  
When the acceptance rate on the bill acceptor is falling.  
Your machine is making less money for sure and and and that the acceptance rate from my experience could fall by 30% very quickly.  
So you want to know that a certain software, sorry, the certain firmware on that bill acceptor was not updated and you and and when somebody wants to put a bill validator head, let's say from an approved vendor.

**Aaron Bockelie** 59:10  
Mhm.

**Val Levitan** 59:18  
Into my machine that I own.  
Still own and the firmware on that validation head is not updated. I shouldn't be accepting.

**Juan Martinez** 59:31  
Right.

**Val Levitan** 59:31  
Except the feature was not properly designed. We should have had. We should have had a message stating please update the firmware. Maybe we should have updated firmware on the fly, but the feature that the thinking of the feature itself is a is a valid feature.  
I mean, in my opinion, of course, but by far you know more about operation than I do of casinos.

**Juan Martinez** 59:58  
Yeah, it it it just becomes tough Alamy. From the customer standpoint, their goal every day is to get that machine up and running and if the machine next to it who makes 50% less money, I I need to take the bill acceptor from that one to put it in a better performing game.  
That's the tactic that all operators do today, because their goal is to get the machine up and running as soon as possible.

**Val Levitan** 1:00:22  
You know what manufacturers say about operators, do you?

**Juan Martinez** 1:00:26  
Yeah, yeah, I know, I know.

**Val Levitan** 1:00:27  
They they make operators make money in spite of themselves.

**Juan Martinez** 1:00:30  
Yes.

**Val Levitan** 1:00:31  
Having having an exclusive license in the area to operate slot machines as a gift.

**Juan Martinez** 1:00:37  
Oh yeah.

**Val Levitan** 1:00:39  
But when you sell machines and you compete on the floor against 20 other manufacturers, you want to squeeze every single drop of juice out of it.  
And so the acceptance rate on the bill acceptor, when I'm being judged on an average performance of my machine on the floor among all these giants, I want to protect that domain and maybe even send my technician. Maybe I should have said, you know, the acceptance rate on bill acceptor is low.

**Aaron Bockelie** 1:01:01  
Yeah.

**Val Levitan** 1:01:08  
You know what? Screw it. I'm going to put my own head in it and just operate it this way. Or find a way. Maybe with an operational manager. Say, hey buddy, you know what? Why don't I take you out for a drink and you put a better head in my machine?

**Juan Martinez** 1:01:23  
Sure, but the only thing, Val, is that we can only get the data on the bill acceptor on Internet connected or QR scan locations, which is is not the norm in the US.

**Val Levitan** 1:01:35  
Or yeah, yeah, I agree. I I agree. Or for example, Light and Wonder had their own server installed in in casinos.

**Juan Martinez** 1:01:44  
Yes, but yeah, they obviously they don't collect that sort of data.  
But you're right, they could.

**Val Levitan** 1:01:54  
They should have.

**Juan Martinez** 1:01:55  
Yeah.  
If Will would have finished the the GSA protocol like he promised that we would be in a bit.

**Val Levitan** 1:02:05  
GSA, by the way, is a great protocol.

**Juan Martinez** 1:02:09  
I I agree.

**Val Levitan** 1:02:15  
OK, moving on.  
Where do I begin?

**Juan Martinez** 1:02:24  
Want to jump to hour well?

**Will Jones** 1:02:29  
Certainly I don't see the segue point, so I'll I'll have to sort of abrupt stop. Then I'll I'll make one more comment that I was trying to, you know, collect my the my notes into more formed observation. So it's just the the classical feature sets I believe we've just been talking about.  
Were the terminal enablement and set up and I think that was somewhat to do with leasing and control that way, the terminal operational management, you know being able to see facilitate things are online, offline and get get them back up and running by dispatch and things that that might come beyond that.  
Terminal accounting, facilitating the financial transactions and integration with third party services, both reporting and I assume there's potentially control, you know, to shut off things in some jurisdictions, though obviously not mentioned for what we just spoke about.  
And did I miss any key feature sets that we didn't talk about? I don't have player tracking here, which it sounds like that is a.  
Feature set that has been it's right. That's something that's in the CMS currently.

**Juan Martinez** 1:03:36  
Uh, no.

**Val Levitan** 1:03:37  
No.

**Will Jones** 1:03:37  
No, there is none. OK. Is that a future desire to have that part?

**Val Levitan** 1:03:39  
Remote.

**Juan Martinez** 1:03:41  
Sorry, customer tracking, yes. Player and player tracking, no.

**Will Jones** 1:03:47  
No, OK.

**Val Levitan** 1:03:49  
Remote initial setup. This is when we remotely send setup to machines.  
We obviously monitor that the setup has not been changed.

**Aaron Bockelie** 1:04:01  
Oh.

**Val Levitan** 1:04:06  
Or disallow any local change but.

**Will Jones** 1:04:09  
Mhm.

**Pavel Frolov** 1:04:12  
Probably for HHR we need to keep in mind that it will be additional hardware installed on the location related to Class 2 operation that we never used before.

**Val Levitan** 1:04:31  
And also on a broader scale as we and and I don't want to jump into HHR just yet, I just want to be a little bit broader.  
Uh, the.  
IT capabilities, we we gotta make sure that IT capabilities are brought to the standard where?  
We will need on the implementation of our transactional architecture.  
Whatever that capability may be, and maybe we already have it, I don't know.  
OK.  
But just keep in mind that it it cannot happen overnight. I mean they need time, they need to also.  
Get their ducks in the row.

**Pavel Frolov** 1:05:28  
Actually related to payment product products, we think that in addition to everything that we discussed right now, we need a separate sort.

**Val Levitan** 1:05:40  
OK.

**Pavel Frolov** 1:05:45  
Not so patch, but separate cloud server that performs in form payment operations.  
Probably, probably it will be some other server if we switch from income to something else. So we require a separate cloud payment processing server.  
That works with third party.  
And it should leave for separately from our orchestration platform. You'll be able to indefinitely independently update, reinstall, scale, probably need two different servers instead of 1.  
So.

**Will Jones** 1:06:48  
One other question I guess in this this CMS tool set, I assume it could be a communications aggregator so that we're no longer going disparately from terminal to cloud. We're going from terminal to some on Prem server that then aggregates that information or communication into one stream.  
Stream back and forth with the cloud. It could obviously also have offline capabilities for enabling progressives to continue and things like that. Is that part of the system currently? Is that any feature set that's that's been discussed?

**Pavel Frolov** 1:07:25  
Actually we do not have a final architecture for for the solution, but yes, we discussed this and agreed that on the location it will be.  
Uh, one of the device will work as a master.  
So it will be a server application on each device and will be will will be able to to take all internal transactions and finally in.  
In communication with this income payment cloud server, it will be only one device from the location.

**Juan Martinez** 1:08:14  
One device at a time, just to clarify, so that that master will be active until it fails over to a second device on site that was the slave and it now became the master.

**Pavel Frolov** 1:08:16  
Yes.

**Will Jones** 1:08:47  
Um.

**Val Levitan** 1:08:47  
Server master slave applications within.  
A certain hardware. There were a number of things. There are a number of things that thrown around loosely as a conceptual approach, but there's no decision on the architecture. This needs to be very clear for everybody in this meeting.

**Juan Martinez** 1:09:14  
Yeah.

**Will Jones** 1:09:18  
Yeah, I would consider that more like the deployment decision on to where it would run on a server versus a terminal. But obviously magic if it all could work on terminals and you don't have to support a server at the site, but obviously you don't. You lose a lot of fault tolerance when you start running on a terminal.

**Val Levitan** 1:09:34  
But what comes as a business requirement preceding the the architecture is driven by a business requirement is that we need an ability to replace.

**Will Jones** 1:09:42  
Hmm.

**Val Levitan** 1:09:50  
A non working hardware replace and by replaced by a non-technical individual. So we ship, let's say a point of sale, it arrives in a box, it gets unpacked.

**Will Jones** 1:09:53  
Mhm.

**Val Levitan** 1:10:07  
Sets on the countertop, turn on and it finds itself in in in the network. It it configures itself and basically, you know, prompts the individual put the old.

**Will Jones** 1:10:08  
Hmm.  
The world, yeah.

**Val Levitan** 1:10:23  
The the the replaced POS back in the box and prints a shipping label and sends it out.

**Will Jones** 1:10:29  
Yeah.

**Val Levitan** 1:10:32  
So that's the requirement that drives the architecture of a server. Because what happens if you have a server, a dedicated server and location, and that server dies then.

**Will Jones** 1:10:46  
Mhm.

**Val Levitan** 1:10:47  
It's dead. I mean, the location is dead. It's non-functioning. All nine machines are not working. And it's, you know, paraphrasing one because he loves that expression. And it's Friday 11:00 PM.

**Will Jones** 1:10:51  
Yep.  
Never been there with Juan, never been there. So yeah, I would say also, yeah, I'd also say that you know that I think you know the pattern obviously if we wanted to pull in patterns as Aaron was Speaking of is the progressive controller, the main controller and obviously finding a way to.

**Juan Martinez** 1:11:06  
Yeah.

**Val Levitan** 1:11:07  
I'm I'm sure. I'm sure.

**Pavel Frolov** 1:11:08  
Mhm.

**Will Jones** 1:11:22  
Support that hopefully having an offline mode too to where all functions that don't require cloud services can be supported with servered connection.  
But OK.

**Val Levitan** 1:11:31  
There's a there's another there's another business requirement that drives the architecture is we have two days to submit our payment to the payment processor.  
That means we have to swipe the accounts in many cases within one day.

**Will Jones** 1:11:56  
Good.

**Val Levitan** 1:11:56  
So we need that immediate reconciliation and you know PNL and reporting posted immediately per transaction and we must ACH.  
The respective accounts within one day.  
There is another business requirement that is important as the lockout. If we find any form of fraud, any suspect of fraud, immediate lockout.  
And then processes associated with it. Those are business requirements that are driving architecture. What happens if? What happens if a piece of hardware breaks during that time?

**Juan Martinez** 1:12:42  
I'll just.

**Will Jones** 1:12:48  
Mm-hmm.

**Juan Martinez** 1:12:49  
Val, are you saying we should be looking at fraud or the ability to lock out in addition to what income is proposing?

**Val Levitan** 1:13:00  
Absolutely 100%. I I actually, I I actually totally ignore income, income's capability and to me it's of of no relevance.

**Juan Martinez** 1:13:01  
OK.  
OK.

**Val Levitan** 1:13:11  
This this is how I look at income. No, no relevance to me.  
Because it's our own money, it's our own skin in the game. I want to be able to tornado.  
Anything in my way if if I detect fraud?

**Juan Martinez** 1:13:32  
Nathan, we'll sidebar on that velocity threshold concept then.

**Nathan Carver** 1:13:37  
Yeah, that sounds good.

**Val Levitan** 1:13:43  
Again, I just want to bring to your attention the point that I stated before our internal IT infrastructure has to be.  
Fast enough, agile enough to provide that capability.  
So, you know, I suspect no local servers, no hardware that we have to take care of. You know, it's more or less a.  
Modern infrastructure.  
I would also say that scale up might be important in terms of processing power and architecture because of July 1st date.

**Will Jones** 1:14:26  
Hmm.

**Val Levitan** 1:14:28  
And so if our product shows itself well, we may have a Stampede of customers.  
So the uh.  
Enrolling customers into the program becomes a bottleneck if that happens.  
So administrative subject of enrolling customers into a program managing customers that needs to be well thought of.

**Juan Martinez** 1:15:11  
We can actually do the enrollments well before July 1st, kind of like those other resellers did that income mentioned Val.

**Val Levitan** 1:15:20  
OK, whatever, you know, practical Rd. we accept. Yeah, that's fine.

**Will Jones** 1:15:33  
Oh.

**Pavel Frolov** 1:15:33  
I I just want to share my my my concern about automatically swapping devices. Actually I do not see reliable way without additional confirmation procedure.  
How to change one device to another and to assign it exactly to this location?

**Val Levitan** 1:15:53  
Mhm.

**Pavel Frolov** 1:15:59  
Any automatic way will be not reliable.

**Juan Martinez** 1:16:06  
um Aaron, do you do you have any any background on what POS replacement today? Does a new POS that's replacing a defective one come pre-configured from the manufacturer for that specific location? Or is there some sort of automated  
It it recognizes the SSID, the IP address, merchant ID number, something that says OK, you're plug and play. I I picked up on a few things. We're just trying to determine if that's acceptable or if that's not secure to Pavel's concern.  
I can't hear you.

**Aaron Bockelie** 1:16:50  
Sorry, I don't know why that was. I must have bumped that back before the earth cooled. When I was working with point of sale systems, I was typically working on sled back style mobile device point of sale. So like an iPhone with a with a sled back.  
This integrated into an existing point of sale stack. Both the existing point of sale stack and the sled back systems. They basically were completely replaceable. They were. You could just kick it out in the hallway and out into the trash can.  
And a replacement would be simply a cryptographically signed approved variant of that piece of hardware again. And in fact the key was protected in a space that was tamped. It was supposed to be tamper resistant and basically if you.  
Touch it in any way that the key got deleted and the keys were then registered. So the private key was known during registration. So we kept the master list of all of those and that was all it was. So if you could.  
Somehow make a a forgery of it. It would have to have been done with significant hardware expertise to be able to do so, and then even then you would have seen irregularities in the audit log and the way the machine was not there and then there again.  
Or if you discharge the machine during the life cycle, so during and then basically there was things like key rolling, so we would have cryptographic key rolling and updates. So there was a process for doing that where point of sales was in regular operation and once it was enrolled.

**Val Levitan** 1:18:28  
Mm.

**Aaron Bockelie** 1:18:37  
Key key rotation occurred all the time, so the the lists were constantly changing on the in the master database that the that we owned in corporate. This meant it was extremely difficult to forge any operations. You would lose connection with the key in 10 minutes after if if it was not running.

**Juan Martinez** 1:18:39  
OK.

**Aaron Bockelie** 1:18:56  
Running. If there was an event where network was not available, then those key rotations were basically cached until network operations returned online and then that would also replay transaction logs and everything else that occurred because the entire site was offline.  
And operating independently until we caught up with the transaction log. So The thing is, I mean, it's a Long story short, was none of the hardware was unique. It was all it of course had its own serial numbers and components and stuff to self register.

**Val Levitan** 1:19:19  
Right, but.

**Aaron Bockelie** 1:19:32  
But we didn't have any concern about that particular unique machine anymore. It was just a matter of tossing it out and adding another uniquely identified machine back to the site.

**Juan Martinez** 1:19:46  
Right. But that that key concept, though, means that corporate had to manage all of that.

**Aaron Bockelie** 1:19:48  
Mm.

**Juan Martinez** 1:19:55  
And and you were probably staffed to do so.

**Aaron Bockelie** 1:19:56  
So.  
So yes and no. The machines would work just fine. They just couldn't post anything back if they didn't have a key. So you could easily use them as a local register for whatever you want, but they had no way to communicate with the mothership, basically.  
If they didn't have a valid key.

**Juan Martinez** 1:20:18  
Right. In our scenario, they they their only function is to print to the gift card. So if that part didn't work, there there is no other function for the POS. It's just a doorstop.

**Aaron Bockelie** 1:20:30  
Yeah. And we've got to remember the point of sale system that I'm talking about did more than just handle transactions. It was a system that kept understood, understood inventory. It understood it was on site in the store. It would even bring up a product catalog and provide people with access to things as well. So there was a lot of.

**Juan Martinez** 1:20:36  
Yeah.

**Aaron Bockelie** 1:20:49  
Other functions the system did.

**Juan Martinez** 1:20:51  
Yeah.

**Aaron Bockelie** 1:20:52  
So there was a lot of data exchange back and forth and basically they just acted somewhere between a point of sales and a kiosk that a retail employee in the site would operate.

**Juan Martinez** 1:21:07  
Yeah.

**Pavel Frolov** 1:21:08  
But in in any case, this device initially need to know what location or to to what operator it need to be.

**Aaron Bockelie** 1:21:21  
No.

**Pavel Frolov** 1:21:22  
No.

**Aaron Bockelie** 1:21:23  
No, as soon as as soon as all we did is we set the identity on the back office. You could send any machine you want.

**Pavel Frolov** 1:21:31  
Yeah.

**Aaron Bockelie** 1:21:32  
So maybe it maybe we're saying the same thing, but basically the distribution of the machine, you know, they would write down the serial number. The serial number was associated with a key in our database and then we had nothing else to do. And then as soon as that you turn that machine on and gave it an Internet connection.

**Pavel Frolov** 1:21:33  
Yeah.

**Aaron Bockelie** 1:21:51  
It would use its signature to connect, hold down its identity, apply its identity, and away it went.

**Pavel Frolov** 1:22:00  
So you you're saying about preconfigured device?

**Aaron Bockelie** 1:22:05  
Yeah.

**Val Levitan** 1:22:11  
I I don't understand why device has to be preconfigured and why can't we send a configuration?

**Aaron Bockelie** 1:22:11  
Oh.

**Val Levitan** 1:22:21  
Or for the device.  
Post connection.

**Aaron Bockelie** 1:22:26  
Yeah. And and I think that's actually an interesting thing as well. When we wanted to switch out software stacks or features or changes, all we did was made a change at the back office end with the prepared. We'd obviously test it first. We'd have a new software load package ready to go.

**Nathan Carver** 1:22:27  
Right.

**Aaron Bockelie** 1:22:44  
And we just changed the we had like AB switch kind of thing like here's version this. Now we're going to assign that unique identity to that and the next time it called home, it picked up a change and then reflashed the whole machine again and basically the register would go offline for 5 minutes while it rebooted itself and came back.  
Again, and it had a new identity with whatever changes we made.

**Juan Martinez** 1:23:10  
I guess that Aaron and what you described, what what if I'm a store owner and I have a spare POS on the shelf, what prevents me from taking it home, plugging it into my Comcast Internet and it attempting to configure itself? Is that even?

**Aaron Bockelie** 1:23:25  
Because we didn't have it, we didn't activate the provisioning for it. So you could plug it into the Internet all you want, but the first thing it does is tries to get its provisioning information. And because it cannot, it just sits there and says I'm not provisioned, so I don't have, I don't even have the software on my.  
On my machine to run it, nor can I even decrypt the software to run from the key that I need to get given to have the beginning to make it work. Like literally the software's on the disk encrypted.

**Val Levitan** 1:23:54  
And so.  
And so if you remember our conversation yesterday, I mentioned to you that that element of provisioning is when when I knew POS.  
Uh is connected.  
The message goes to the master. The operator says we're about to switch your POS. Do you allow us to do it or not? And then master says yeah, go ahead or no. I have no idea that you know.  
The O is out of service.

**Aaron Bockelie** 1:24:33  
Yeah, in in our situation, I was gonna say. So in our situation, let's say you did take the on, you know, a box that machine ready to be turned on and it wasn't part of the provisioning in the provision list like it was known, but it wasn't provisioned, right?

**Juan Martinez** 1:24:34  
So in this scenario, go ahead, Aaron.

**Aaron Bockelie** 1:24:51  
So what would happen is you would turn that machine on at your bootleg office at home trying to use it to have a garage sale. And what would happen is, is that as soon as it connected to the Internet, the.  
Key the the no key would. Basically the key would authenticate and then the the upstream would say I don't have any authorization to decrypt the software for you to load. Like it would boot its initial software and it would have an encrypted disk image on the machine ready to go.  
But until that disk image was given the key to decrypt, because it's a it's a many to one a relationship on the encryption, it wouldn't even be able to boot the register stack. So it just kind of sit there and go waiting for provisioning and then as soon and it would check every, you know, 5 minutes or whatever.  
And then as soon as you were on the back end, if you were to turn on provisioning for it and say you're assigned to software X, which is for store Y, which is for register position Z or whatever, then it would be able to decrypt the software, which then loaded it, which then connected, and then pulled down its new copy of its own software because it was in a.  
Its own decrypted container, update its software, do its thing, and then when it shuts off, everything's encrypted at rest again as well. So every time you turn the machine off, all the data is encrypted at rest as well.  
It's a pretty secure system and made it so it was very difficult to break into stuff.

**Juan Martinez** 1:26:28  
Yeah, so obviously Pavel, this implies a live database with every serial number of every POS produced so that we can respond accordingly.

**Pavel Frolov** 1:26:40  
Yeah, if again it it describes, uh, additional step.  
That enable this device to operate on particular location.

**Juan Martinez** 1:26:54  
Right.

**Aaron Bockelie** 1:26:55  
The other, the other ways we were able to maintain PCI compliance was to have a secure enclave defined as network network space. So we have it had to originate from a particular IP address for things which were declared unknown network space. That was the stuff we did for our stores because we could, you know.

**Will Jones** 1:26:57  
Good.

**Pavel Frolov** 1:27:17  
Very unreliable.

**Aaron Bockelie** 1:27:19  
Yeah, well, there was multiple factors, right? It's the Swiss cheese model of security.

**Pavel Frolov** 1:27:25  
Yeah.

**Juan Martinez** 1:27:26  
Will, you got a question?

**Will Jones** 1:27:29  
Yeah, I just want to establish from my understanding, I guess that certainly these are very interesting, you know, ideas and concepts to apply to casino environments too. Is that intentional right now that we're talking about things that are outside the box that we may need to apply? You know, I can say that.  
Leaving the the, you know, the the disk encrypted at rest, or making it so that the any device needs to acquire a key from a central server before it can decrypt the device is something outside the bounds of any device that I've ever worked with at a casino and I believe really goes.  
Against the grain because those devices can't just boot and be playable. So I'm I'm just wondering, is this just a healthy discussion on other avenues or other other industries or is this something that we're really considering them to apply to this product?

**Aaron Bockelie** 1:28:13  
Right.  
Well, remember what I'm describing is a payment processing system that we had to have. We had significant auditing and oversight of of handling people's PII and yeah.

**Juan Martinez** 1:28:25  
No, I mean.  
Yeah, so it's real world Will in in the this 90% of that Georgia mark as an example has that Mother Goose cereal board and you know it's gonna have just this our single flex point of sale device.

**Nathan Carver** 1:29:08  
Hmm.

**Juan Martinez** 1:29:08  
Employee replace a point of sale with minimal amount of effort and I use the word hot swappable, auto configurable. You know what? What can we get to in today's world that's safe yet requires the least amount of effort, you know?  
Basically plug it into the Ethernet, give it power and and stand back and and how do we get that unit operational?

**Nathan Carver** 1:29:37  
Yeah, we're balancing our trade off of our timeline, um, resources, right, to develop and then um.  
The ease of use, right? How easy is it for, as Juan was saying, for the end users to actually do the swap?  
I'm assuming the system Aaron's describing was developed over a long period of time with several with a rather large team to make all those pieces work.

**Aaron Bockelie** 1:30:02  
Well, yeah, this was with Fujitsu Retail Systems as well as Verifone. So between the two, these are very large vendors and we had our own integration stack that worked between it, which basically was the.  
Provisioning data system and all the other pieces that went into play to be able to operate it. And then of course we had to manage the operating system itself, which was a bunch of Windows embedded systems running on things and then the Apple iOS.  
On the on the sled back for the so Verifone was the sled backs, Fujitsu was the Windows in Windows embedded stack and then the two of them talked to each other. But they all both had the same secure enclave virtualized environment to be able to run the register platform.

**Nathan Carver** 1:30:52  
Yeah, and I think we can take ideas from that model and apply it to ours with the advantages of we have a single device or two to start with, like the the POS and the dispenser.  
And we can take the ideas on provisioning and encryption and and see if that works for our purpose and then still go through the trade-offs of what's what's simple and what's secure and what can we finish in the timeline.

**Juan Martinez** 1:31:26  
It.

**Will Jones** 1:31:36  
So I know I don't remember who asked this. If you would you like me to speak a little on HHR and at least have an idea of how to bring it back into this conversation.  
So, OK, I'm going to start with where I'm going to integrate us back with the OR or get us back with the conversation here. And I believe a question that we would be interesting to explore, at least discuss a little bit about what was.  
What was found before previously when we had architectural discussions on HHR is how do we integrate with the game engine? So where we're using a third party service to determine actual outcomes, how do we integrate that in our game? So going back to the beginning or at least talking about the last six months of HHR.  
So we have opened up conversations with Ainsworth and from what I understand, we now have a working terminal and server in the Georgia office. So through those, OK.

**Juan Martinez** 1:32:37  
Yes and no. And I'll, I'll clarify when you're done.

**Will Jones** 1:32:40  
OK, we'll put a we'll put that in the parking lot for now. Anyway, in those discussions, Ainsworth helped us understand what the expectations are, both with the integration and both with the final product. We've used that information and additional information that we gathered on HHR to compile a list.  
Of requirements and establish some user stories from the perspective of the player or the casino or even the the regulator, how they will be, you know how their needs will be met. So we have the what's defined for, I don't know to throw out a number that's just a a guess.  
Is to say we have the what's defined for probably somewhere 80% up to 90 or even 95%. There's obviously always a few what's that that we missed that we'll figure out along the way, but we were in a good place I believe for our user story definitions.  
Element of requirements behind that. Through that time period of the last six months, there was a good amount of discussion on the, you know, what I would say is more either architectural or functional implementation, understanding how the pieces layout within our game currently.  
I believe the direction was already set to say it was going to be in the Omni frameworks. There's some assumptions made there, but how it was, how it was laid out currently and how it would piece together or how we would piece together a solution for HHR and getting to that, you know, coming back where I was saying to integrate.  
With the game engine, Historical horse racing is based on oh, let me remember, is it Ainsworth? Is it three games for Ainsworth? I can't remember. Is it 8? Sorry, I need to check notes again, but they will have a certain number of races.

**Juan Martinez** 1:34:31  
It's 8 I think.

**Will Jones** 1:34:36  
And the races will depict patterns based on the horses that the player picks and the results that come, you know, come from that. So you could kind of figure it looking roughly like a bingo card with hits and misses.  
Those player picked horses or the you know predicted ending positions then determine the the pattern that is on that card when we get the race results. This is normally done through this the game auto picking based on the horse ranking.  
And then the outcomes of the, you know, the pattern can be used to derive a actual payment to the the player. So anyway, this is integral to the decision of when the game is played, how much are we going to pay the player at the end based on their wager?

**Aaron Bockelie** 1:35:15  
Yes.

**Will Jones** 1:35:29  
Not necessarily to get into finer details of it because I don't think it's particularly important for this discussion, but the the the meetings that we had had identified the points at which or the the actual areas of code that would be changing that would need to integrate with an HHR server.  
We had multiple discussions on whether that server was going to be on Prem or off Prem, realizing it's most likely going to be on Prem for that and having the ability for our system to actually function for some period of time when it is disconnected from.  
An HHR server the from the the place that it gets these race ticket sets. So that was that was integral and definitely complicated, but I think provided a more resilient solution in the end and that was what we were predicting would be.  
Ended those meetings, I think at the point where we would now have to really place some kind of action to creating a plan, deciding who, who and when, what you know was going to be accomplished and then getting them the information they needed, having those discussions with them to make sure that they understood the.  
The functions that we needed to provide and add that other 10 to 15% of detail that we might have missed going through the first time. So now back to I guess where I started the question I guess I might have from this discussion we're talking about a CMS, we're talking about at least some.  
Remote service that's providing the the transactional logic for the game. Then I think the the question is I guess how in you know how in the world of Omni does this fit together? So I'll leave that you know first to to Pavel to correct me if I said anything that was not.  
It's not correct for our our discussions and my observations for where we got to, but then maybe to start us out with the, you know, finer points of the integration with our, you know, with our existing architecture, our existing services to the HHR server.

**Pavel Frolov** 1:37:46  
OK.  
Actually I think uh said about.

**Aaron Bockelie** 1:38:03  
Mm.

**Pavel Frolov** 1:38:05  
Uh, new orchestration orchestration platform.

**Aaron Bockelie** 1:38:06  
Yeah.

**Pavel Frolov** 1:38:11  
So the main differences is currently existing. We are going to to provide access to third party.  
Operator.  
Be able to monitor and to manage his locations, his machines.  
Then I think the major changes should be for all repositories that need to to produce our orchestration platform.  
To be.

**Aaron Bockelie** 1:38:55  
Yeah.

**Pavel Frolov** 1:38:58  
Well described, all documentation should be on the same repository described in the structure, architecture, use cases.  
And so on.  
And we need to understand architecturally how all of our IT infrastructure should be built, how many servers, cloud service versus on Prem.  
Uh, relationship between servers.  
Probably.

**Aaron Bockelie** 1:39:43  
Well, and I think that what you're saying, Pavel, we're we're starting with the high level. What are we trying to accomplish? What do we want things to look like? And that's going to ultimately drive, you know, the lower level supporting blocks, the the the foundation of all of this.  
And then we need to also not let that be unpinned and flapping the breeze because.  
We may get push back and say Oh well, we we don't know how to do that and actually there are requirements that say no, you have to be able to have multi-tenant, you have to be able to shift your workload, you have to be able to have resilience in the space. So therefore running it on a server in a physical space is not allowed. You have to do it in a cloud environment.  
Or it needs to be this or that. So it's we we I think that for the next you know as we start to clarify these look we should try to play the game of don't create the solution during writing the specification.  
We got to, we got to really, really be careful with that. I think that there's a lot of, you know, it's it's easier when you've ran the engineering stack or ran the the software stack for a long time to just do that and and not recognize you're saying that.  
So for instance, when we talk about database, OK, I understand we need a database. Is it really a database or can we just call it data lake? Let's let's let's use the wording, the phrasing, and because I think language here is the biggest.  
Obstacle to success that we've got right now. Defining this language has got to be really careful. I would say data lake when we talk about it, for instance. Or maybe we do need to say database because it's some sort of transaction processing thing or.  
We have to have some information store for for state and transactions and whatever. I'm I'm just calling out that the the semantic intent of the words we picked right now have a lot of meaning right now and we probably are going to need to step back and say OK.  
Let's try to say this without secifying technical details for a little while.

**Pavel Frolov** 1:42:01  
Yeah, agreed. And probably I can rephrase probably all your speech that we need during our new design or architecture design.  
Need to focus on capabilities driven approach. What? What should we reach? What? What should the new architecture, new design do?

**Aaron Bockelie** 1:42:26  
Yeah.

**Pavel Frolov** 1:42:33  
In general.

**Aaron Bockelie** 1:42:35  
Right.  
Because I think it's it's a really dangerous thing to just try to throw away everything you've learned, but it's also dangerous to hold on to all of it either. So we've got to just take what we've got from the current learnings of things.  
And make sure that we've deliberately assigned the migration path for migrating to a different platform that may end up looking just like the old one, except with a bunch of carve outs or pieces removed all the way to it's just inspired from what you did previously.  
And sufficiently serves what the previous infrastructure you had, but it's radically different than how it used to be. So I think that's that's kind of be one of the things in a in the migration world from migration migrating big platforms from one thing to the other, the concept of extract, transform and load.  
Code ETL can be actually set for the software stack itself, not just the data that's inside of it. So when we think about your source project and how things are and how things have been for a long time, when we sit down and understand the concerns that are inside of the software now and.  
This is, I think, where that inventory has to really be made of what the stack looks like as it is. So we can explicitly say this thing serves our purposes still. Same with this, same with that, same with this other thing, and ask the questions from an architectural perspective of which ones do not serve our purposes.  
That's once we've surveyed that, then we can begin the question of asking picking this up and transforming it and setting it down again will take this amount of effort or will cause this much of the platform to change.  
And I think that's the kind of abstracted think meta thinking, metacognition about approaching this problem that we've got to do now. So that means understanding the purpose of the code base, making sure we have some written understanding that the other people on this call, the Will, the Nathan, the Juan.  
The Aaron potentially to kind of be able to see and understand why those pieces are there and what the purpose they serve without needing to go into the absolute detail of the code itself. It doesn't mean like massive documentation project, it means.  
How is that architecture built right now? And then once we understand that, we can then demand of the Dimas and the Pavel and the Andrei about how the architecture of the backing platform works and the code and the application.  
Does it do these things and be able to be be specific about the new requirements that we're going to impose on this thing?

**Nathan Carver** 1:45:23  
Hey everyone, I have to sign off here a little early, so the transcript will be made for this available, made available for this meeting.

**Aaron Bockelie** 1:45:36  
Yeah.

**Val Levitan** 1:45:36  
I I will do that.

**Nathan Carver** 1:45:37  
OK.  
All right. Thanks. All right. Thanks, everyone.

**Aaron Bockelie** 1:45:41  
Thanks, Nathan.

**Pavel Frolov** 1:45:42  
Yeah, bye.

**Val Levitan** 1:45:43  
Thank you, Nathan. If.

**Will Jones** 1:45:43  
Aaron, if I can just, yeah, I was just gonna add to Aaron's just to, you know, maybe put a period in the end of that sentence that he had. I believe the, you know, or the attempt was made, let's put it that way, at writing use cases or user scenarios that that really defined the what and didn't get into the.

**Pavel Frolov** 1:45:43  
So.

**Nathan Carver** 1:45:52  
Mm.

**Will Jones** 1:46:03  
The how, you know, very cognizant of that. But definitely our conversations for the past six months have dwelled on how greatly, probably 5050. And that was with the expertise of Ethan Pavel, you know, deciding how they would accommodate the the what that was described.  
As we went through these use cases, so those architectural discussions, maybe they were had in the back room and and needed to be with more participants. But anyways, there were a good deal, there there was a good deal of call it, you know, ideas.  
That that should be resurfaced for the greater good talking about you know any more significant architectural changes. But anyway I hope that that the the what and the how are you know how you look or or or something that you resonate with you as well.

**Juan Martinez** 1:47:00  
Just to I interrupted you Will earlier with the Ainsworth machine being up and down. So this might be for Andrei, but when the Georgia office plugs in the machine, the objective was to leave it running overnight.  
In case Mints needed access in off hours, but after a few days of turning it on, it was crashing or corrupting or messing with the office's Internet connection, so we're not sure what that's about. So currently the machine has been turned off in favor of them needing their Internet access in the office.  
So I don't know if that's an Ainsworth issue, an AT&T, the Internet provider issue, but it just sounds like during working hours it would be difficult to leave that machine up and running because the Internet connection for the office is affected.

**Val Levitan** 1:47:56  
We could always get another Internet connection that's only, you know, 100 dollars per month. That's not a big deal. Just to summarize.

**Juan Martinez** 1:48:01  
OK.

**Val Levitan** 1:48:08  
So.  
What has been said, I think that we want to focus on general and and I I think this is the undertaking or objectives coming out of this meeting is for this team to focus on the overall block diagram architecture that focuses.  
On what needs to be done rather than how it needs to be done, and when that block diagram is presented, we can then define MVP's out of this block diagram and start talking more narrowly on.  
Use cases.  
Further refining the architecture and then the use cases will probably lead us to a discussion. Well, how do we do it? And from there we narrow on exact architecture on the MVP components of the overall blow diagram.  
Is this how we see the process evolving from here?

**Juan Martinez** 1:49:12  
Makes sense to me.

**Aaron Bockelie** 1:49:14  
I think that.  
That block diagram and the understanding of what the system does.  
Will help us have further discussions about asking of what it can do.

**Val Levitan** 1:49:28  
OK, can we schedule a set of regular meetings by we? I do not necessarily see myself as part of the engineering group discussing architecture, but it should definitely involve at a very minimum.  
Pavel, Will, Nathan and I don't know to some extent Juan, maybe yes, maybe not, maybe not, not in all of the meetings, but that's probably the the minimum group that's required.

**Juan Martinez** 1:50:01  
Sure.

**Will Jones** 1:50:02  
Yeah, especially I think if we focus on the what or the what comes out a lot, I definitely think Juan would be very important to have there. I feel like that and we see, I think that's a that's something that we need.

**Val Levitan** 1:50:17  
OK. So then the minimum group will consist of Juan, Will, Nathan and Pavel. And so with that in mind, can we please set schedule set of meetings discussing?  
The block diagram. The architectural block diagram.

**Juan Martinez** 1:50:37  
Absolutely.

**Will Jones** 1:50:37  
He's and I asked Pavel a question. Sasha was involved with some of those other discussions too, would be particular, I think in the integration with HHR server, if I'm not mistaken. Wasn't that the case?

**Pavel Frolov** 1:50:52  
Yeah, in case when we need to discuss just HHR for example, yeah, we can invite Alex, but I think right now we are focusing on entire approach to new architecture, new.  
Yeah, new architecture schematics, probably we do not need Alex right now.

**Val Levitan** 1:51:20  
I I would also find it useful every so often. I don't know every three meetings or every six meetings to have a broader presentation on what has been achieved.

**Pavel Frolov** 1:51:21  
Because.

**Val Levitan** 1:51:36  
I would like to be in that meeting for sure. I I think Aaron would serve a purpose. Maybe it should be a broader group, I don't know. Would that be acceptable?

**Juan Martinez** 1:51:48  
Yeah, absolutely.

**Aaron Bockelie** 1:51:50  
I I would like to try to hold hold accountable for the way that we document things. So I put in the chat. I had to go Google them to remember the numbers, but basically there's I Triple E specifications that have been around for a long time about how to write documentation of architecture of platforms.  
I'm not saying we need to conform to it perfectly to to have acceptance, but I think we should be understanding of these specifications and expectations for what we actually are trying to build.  
Because without this, we'll end up with yet another spreadsheet of a list of things inside of it that's completely useless. We got to be able to really be able to hand this to an engineer or a software engineering group who's not JBL.  
Not, I'm not saying we do, I'm just saying this is kind of the test.  
To be able to let, they should be able to understand what this product does.  
If we were to independently verify.

**Val Levitan** 1:52:52  
I think some sort.  
I think some sort of a frame work for discussion is useful. I don't know to which degree we want to embrace the complete set of documentation. It might be overwhelming for a company of our size.  
But some sort of a framework discussion discipline that's probably welcome.  
Regardless, currently we are committed to GitHub and Jira combination. We're trying to move away slowly from using Confluence.

**Aaron Bockelie** 1:53:20  
I'll.

**Val Levitan** 1:53:34  
Um, so those are preferred tools.

**Will Jones** 1:53:39  
What are we using right now for creating our diagrams?

**Val Levitan** 1:53:44  
We use Confluence right now.

**Will Jones** 1:53:47  
And is, is there a, yeah, because I know it was Mira before and obviously Confluence then and is if we are moving away from Confluence, is there another tool that we're envisioning?

**Val Levitan** 1:54:00  
Today, Confluence is a de facto package that we use, so.

**Aaron Bockelie** 1:54:06  
So my my inclination, my my direction I would advise us to think about is something that can be viewable and usable and get.

**Val Levitan** 1:54:07  
Yeah.

**Aaron Bockelie** 1:54:18  
Not a bespoke platform inside of Confluence or something, because that means it could be packaged with the code, right? The docs and the code go together and that sort of begets things like mermaid script for example inside of a document, because if you have that.  
Then you can view it directly in the Git repo alongside of the software itself. There are many different editors available to to make those diagrams, and we all know that AI tools can help us refine those diagrams too. So there's just, I think there's a lot of good.  
Good inertia in that direction.

**Val Levitan** 1:54:53  
We're almost one minute away from the hour. I would like to ask you individually, please open your calendar and let's set a date for your narrower.  
Internal meeting or meetings, maybe plural.  
And then let's set up a recap meeting for broader group.  
Will, you probably should set the tone for that.

**Will Jones** 1:55:26  
Yeah, I would say that I was just thinking Tuesdays are a very almost impossible for me to make time to to fit it in on Tuesdays. Thursdays are the second least good day for me. So Monday, Wednesday, Friday are definitely the days that fit best for me in the morning 6:00 AM. So that's.  
Hopefully that has the best overlap for, you know, it's East Coast 8:00 AM overlap for Minsk as well. So I would strike Monday, Wednesdays, Fridays. I can make this a regular meeting if we want to make it twice a week. Start to discuss that too.

**Val Levitan** 1:56:04  
I would suggest Mondays and Fridays.  
Format.

**Will Jones** 1:56:11  
It's a between Monday and Friday. I've done that before, Val. It's so tough to get exactly. You just don't get much momentum then because you come back on Friday or Monday and you talk about what you wanted to do on Friday. You know, it's like, OK, so I I would say either a Monday is not a problem, but a more Monday.

**Aaron Bockelie** 1:56:11  
Yes.

**Val Levitan** 1:56:14  
Yeah, it doesn't work.

**Will Jones** 1:56:29  
Wednesday cadence would be more natural or a Wednesday, Friday if we're more orientated to other work on Mondays.

**Val Levitan** 1:56:37  
I prefer Wednesday and Friday.

**Will Jones** 1:56:46  
Yeah, I can accomplate that.

**Juan Martinez** 1:56:46  
Yeah, well, we're correct.

**Val Levitan** 1:56:46  
How many? How many meetings? How many meetings in between do we need until a a broader meeting 246?

**Aaron Bockelie** 1:56:47  
Yeah.

**Will Jones** 1:56:57  
Could we, could we set that agenda as our first meeting? At the end we could discuss what when our when we'd be confident of that rather than set it now saying that six would be a long time out, but let's look at seeing what we think we could.  
You know when we would have something that we could present, we can discuss what we want to present and when.

**Val Levitan** 1:57:18  
Well, let let me let me go by saying we can always adjust, but let me do three meetings. So one, can you please take charge of setting up Wednesday, Friday, Wednesday?

**Juan Martinez** 1:57:30  
Huh.

**Val Levitan** 1:57:31  
And then Friday, a recap for a broader group.  
By broader group, I suggest this group, including Nathan.

**Juan Martinez** 1:57:36  
Sure.

**Val Levitan** 1:57:44  
At the end of every meeting, when transcript is ready, I would like to get a file of unedited dot VTT.

**Pavel Frolov** 1:57:45  
I wish you.

**Val Levitan** 1:57:55  
I will convert it myself and circulate the transcript.

**Juan Martinez** 1:58:01  
50.

**Will Jones** 1:58:04  
So I do have the ability to do it Val too. I'm now. I'm now capable after that long spell.

**Val Levitan** 1:58:05  
OK, So what? What?  
OK, no problems.  
It's just that I would like a particular form that we finalized. Well, Aaron finalized for me in the the the tool that I sent you.  
One please for every meeting invite me as an option. I will stand by. I will not attend.

**Juan Martinez** 1:58:38  
Will do.

**Val Levitan** 1:58:41  
OK. Thank you everyone and we will see you in a week and a half and good luck with the discussion. I'm always sending you back.

**Pavel Frolov** 1:58:53  
OK.

**Juan Martinez** 1:58:54  
Thanks.  
Thanks everybody. Bye. Good day.

**Val Levitan** 1:58:56  
Thank you. Bye bye. Bye bye.

**Aaron Bockelie** 1:58:57  
Thanks.

**Pavel Frolov** 1:58:57  
Thank you. Bye.

**Juan Martinez** 1:58:59  
Hi.

**Dzmitry Chudzinau** stopped transcription