---
tags:
  - user-authentication
  - two-factor-authorization
  - workflow-diagram
  - val
  - pavel
  - technical
---

**Transcript**

June 20, 2025, 10:36AM

**Val Levitan** started transcription

**Val Levitan**   0:03  
Right now on a short notice.

**Nathan Carver**   0:04  
OK.  
Yeah.

**Val Levitan**   0:10  
OK, let's before every meeting, let's set out an objective of what we want to achieve and let's focus on the conversation.

**Nathan Carver**   0:11  
Yes.  
All right, so I have where I'd like to take this is I have all the use cases that we just started discussing yesterday. I have the redeem ticket flushed out in the in the workflow diagram.  
And I started looking at the user authentication use case. Um.  
So I think those two things will be valuable to talk through cause it's gonna show us the communication between the JVL system and income.  
So share my screen.  
Yeah, OK, so.  
We can come back to the authorized if we we can talk through the Um.  
The redeem first doesn't really matter to me, but the So what I have here is essentially the four.  
The four actors systems involved in this and just shows the flow of responsibility through throughout the journey and so.  
This is to help us see where these requests are going and kind of layout the the state of the system as as the user's going through the journey.  
So I took the some the basic concept of entering the pin, which is what we have in the setup.  
And so the user's gonna enter their pin.  
That's gonna essentially open up Flex POS. If it accepts the pin, it's going to then. In this case, it would somehow verify this pin is active with JBL Cloud in order to initiate.  
A2 factor authorization.  
Um.  
And my thinking here is we want to some way associate the user at that device. We want to be able to identify them as well as not just identifying that that flex POS is now active.  
So the only way that I was thinking we could do, or one way I should say that we can do this is if we use like a two-factor auth, either sending the code to the users to that specific user's cell phone or them using an authenticator app.  
Uh, but some way to identify this user.  
And this may lead us to the question of in our setup we we describe how the device is initiated and the device itself is given a pin.  
We may have to and and for audited reasons, right? We may wanna go deeper and be able to identify each user that's actually going to be.  
Enabled to use that device, which will lead us to more questions is who sets up those users and how do we manage those accounts?  
Yes.

**Val Levitan**   4:00  
Maybe one of the directions could be instead of entering a PIN, swipe a card, an admin card.  
And and if it's an admin card, then you could identify the user by the admin card and the POS that the card has been swiped at.  
in the same, in the same notion.

**Nathan Carver**   4:25  
Yeah.

**Pavel Frolov**   4:35  
Will it be enough to authenticate to to authorize a cashier or it still requires some additional way of communication to get activation code to enter?

**Nathan Carver**   4:55  
So we could, yeah, if we issued a card to a user, then we would associate that card, for example in a two-factor auth, associate that card with that user's phone number.

**Val Levitan**   5:09  
I I.

**Nathan Carver**   5:09  
So they swipe the card which identifies them, activates the device and then initiates the two factor.

**Val Levitan**   5:18  
I think there has to be multiple levels of how the card is issued. So this particular cashier card should be issued by by an administrator who is a higher of a rank.  
Let's say a location owner or a manager, regional manager, IT manager, somebody who's got a higher rank.

**Nathan Carver**   5:45  
Mhm.

**Val Levitan**   5:46  
And that should probably be done also through the terminal or through a mobile app. I I happen to love mobile apps, but I'm trying to make a set of MVPS that are achievable for September.  
And in particular for September, I suggest that there would be a three stage management.  
Group associated with any location.

**Nathan Carver**   6:16  
OK.

**Val Levitan**   6:20  
And the cashier or the cage attendant being the lowest.  
So anybody who's rank ranks \#2 or \#1 could in fact issue a card using his.  
Uh.  
Rights. So for \#2 and \#1 ranking.  
I would make it a two-step process, including a QR code scan or including a higher pin number.  
Again, the key here is to start operating in September. I don't want to burden this team with designing a mobile app.  
So I would suggest to authenticate on the on the POS.

**Nathan Carver**   7:23  
OK, so in September, um, we authenticate.  
Just with the card for example, or even just the PIN, right? Enter the PIN for the POS for the device.

**Pavel Frolov**   7:36  
Yeah.

**Nathan Carver**   7:45  
And then we'll defer A2 factor off for later. Here's some other off mechanism.  
OK.  
All right, so essentially that would be it. We enter, enter the pinner, swipe the card, do the two factor auth.  
And that creates a session between the Flex POS and and the JVL cloud and places the user at their idle screen which is ready to receive ticket information.  
Um, OK.  
So for the redeem ticket.  
Uh, took the discussion we had yesterday in diagram that workflow.  
Of what it might look like so.  
Starts with the user having been authenticated and authorized to use the device. They have a ticket. They're gonna enter in the ticket information, so the metadata from that ticket and the value.  
And that will go into the Flex POS, which will then initiate a conversation with JVL Cloud.  
And the idea here is this previous session we've just initiated, we're going to tie this whole conversation together to that session so that we have a a way to go back and and audit this process.  
So this starts the concept of a ticket redemption and.  
This this will create this. Ideally in the JBL system we create this ticket redemption record and initially we're just identifying some basic information of.  
The device that's doing this, the cashier ID, the the person who authorized the device and the ticket ID and the dollar amount. And we start this record in our system that this ticket has been swiped in the happy path. This isn't really going to do much for us, but.  
In off nominal cases of.  
The ticket being swiped again for a reason of maybe it failed to get print out a gift card the last time, but we'll already have a record out here that can help us make decisions in the future.  
So they swipe the ticket. This initiates the process and then the user's going to swipe the gift card.

**Pavel Frolov**   10:32  
OK.

**Nathan Carver**   10:39  
And again, the user will swipe the gift card. The the POS will inform JVL Cloud of this gift card ID. However, that card specifically is identified. That information will be added to.  
The um the ticket process here.  
So we now can associate the session, the user and the gift card and the ticket.  
So once that association is made, that information will go back to the POS and that enables the POS then to authenticate with.  
Uh, it.  
So at this point, there's no more activity for the user. They've they swipe their card. Now the user's just going to wait for the two systems to negotiate a payout for that card. OK, so the first step is we initially authenticate Flex POS with income.  
And then once that's authentication is done, we're gonna make another request to pre-authorize the gift card.  
And once we have pre-authorization, we're going to notify, we would notify JVO cloud of successful pre-authorization and so any metadata that we would want to to.  
Archive we would send to the cloud as soon as we get that pre-authorization approval from Incom.  
So after that approval, we can then after we've recorded it, we can then request an authorized an authorization to put the amount on the gift card.

**Pavel Frolov**   12:24  
Mm.

**Nathan Carver**   12:31  
So this another two-step process is we communicate with income, we ask them to authorize the gift card. Now when they're successful, we're assuming that now the money has been transferred.  
We need to record this in our cloud that we've succeeded. Whatever metadata they give us back, we want to make sure that we store that.  
I've created a bound box here because this is this two step. We really wanna make sure we stay In Sync so if for some reason.  
The authorization of the gift card succeeds, but we fail to record it on ours.  
In the in the future, I'm assuming it's not just income looks at their transactions and they they they bill us, right. And then we look at our transactions and we bill the client. I would think that we would want some type of.  
Audit of the two and I'm not sure we can audit what income sends us, but if we record all of our activity with income, then we can do our own internal audit.  
And basically what that means is when we run our, when we run our batch job to.  
Essentially pull the funds from the client or from the from the location.  
We would go out, we would look at all of our redemption, redeemed tickets and we would know how much money right to pull. Ideally this would give us an audit log of all the money that we need to pull. Another thing we could look at is.  
Just the tickets that were not completed. So if we see that there's a ticket out here that was pre-authorized, but there's no final completion, that's a signal that either for whatever reason the process was.  
Failed or canceled or potentially a gift card was issued by Incom and we don't have our own internal record of that gift card being issued.  
So that's what this bounding box is representing. It's just we could also if this were to fail, for example, if if this message succeeds and this message fails, flex POS.  
Should internally have perhaps a retry mechanism or the ability to send a signal that there was a failure.  
And if it loses, there's other off nominal failure modes that we might want to consider, and that is.  
If Flex POS succeeds with Incom but then fails to, it then loses connection to the cloud and is not able to complete the transaction on with JBL.  
So those are things that we'll consider in the future.  
And OK, so after the ticket has been marked completed in the cloud, we then come back to the PLS and going to print a receipt or e-mail or text or whatever our option is, and then the cashier can present the gift card.

**Pavel Frolov**   15:53  
Uh, here I can uh.  
Just to uh to correct.  
Yeah, request not authorization of gift card, but correct word will be activate request card activation. This request named activate.

**Nathan Carver**   16:15  
OK.  
OK.  
Has the amount already been placed on the card at this time? Is that what the?

**Pavel Frolov**   16:34  
I think yes.

**Nathan Carver**   16:36  
OK.  
OK, so in this case we have.  
So cache a client.  
OK, that makes sense.  
OK.  
And see any other questions with this this flow?

**Pavel Frolov**   17:40  
Mm.  
Um, not now looks.  
Looks correct.

**Nathan Carver**   17:53  
OK.

**Pavel Frolov**   18:01  
OK.

**Val Levitan**   18:03  
I just want to make a note that this is a.  
Um.  
Part of our critical system that cannot fail because if this fails, the entire location stops functioning.  
And so couple of things come to mind.  
Recovery.  
What happens if the transaction got, I don't know, we in administration use the word frozen.  
You know, cannot complete for some reason.  
Uh, what happens if uh?  
What's the recovery of communication between income and?  
And the POS? How does JVL get notified that you know the system hung up?  
And it requires immediate service. What if the service was reported? How do we attempt to recover over a long distance?  
What happens if?  
For example, a location says no, I'm afraid to depend on just one POSI want to have two POS in in in operation in parallel simultaneously.

**Pavel Frolov**   19:41  
T.

**Val Levitan**   19:52  
Is there a priority issue? Can what if the location has? If it's a larger location and has two cage operators, could two systems work in parallel and how do they prioritize between themselves?

**Pavel Frolov**   20:05  
Yes.

**Val Levitan**   20:10  
And is there any interference or noise between the systems when they contact almost simultaneously from the same location to in home trying to validate a card? What happens if?  
A validated card got dropped on the floor, fell through the cracks.  
Cannot be recovered, but never reach the player.  
What happens if?  
A card is issued for the wrong amount.  
By mistake, is there a recovery screen before the issuing a credit card?  
Uh, sorry, not a credit card, but uh.  
Prepaid card.  
Can you retrace your steps?

**Pavel Frolov**   21:21  
Oh.

**Val Levitan**   21:21  
Again, I want you. I want you to picture a location, not an average location, not a smaller location, but a larger location with 10 machines.  
That is really, you know, humming and functioning as a dedicated gaming location. And you know, things cannot stop and they need to function, function, function at a high speed. Can this system function?  
So.

**Nathan Carver**   21:51  
Yes. Um.  
So what I.

**Val Levitan**   21:55  
Yeah, these are these questions that pop into my mind.

**Pavel Frolov**   21:55  
6\.

**Nathan Carver**   21:58  
Yeah, So what I'd like to do. So this is essentially a failure mode analysis which I would I want to add to this use case so we can do a full.  
Essentially what we would do in a an analysis like that is we would go through each of these points and look for the possible failure modes in the recover and how do we recover.  
And another thing we we want to identify is like the type of connections we're making. Are we just doing HTTPS?  
Requests to JVL cloud and and income? Or are we opening sockets and maintaining A socket connection to one or both?  
And.

**Pavel Frolov**   22:50  
A HTTPS connection to Incom and Websocket security connection to our cloud.

**Nathan Carver**   23:00  
OK.

**Val Levitan**   23:00  
I I do not propose to resolve all the issues. I'm I'm just throwing questions and it's possible that you need to think about it. Another question that I forgot to mention is, is there a?

**Pavel Frolov**   23:07  
Uh.

**Nathan Carver**   23:08  
Correct.

**Val Levitan**   23:16  
A conclusion? A sign off screen? What if there was no sign off? Is is the screen still open? Can somebody communicate? Because I've seen some of the POS for processing requires a full insert card.  
And the the POS locks up immediately when the card is yanked out.  
What happens if this system remains open? Is there any danger to it? Should we have a, you know, full insert card and then?  
On a on a leash of some sort and then you're you're made, you're made to remove the card and then does it lock up the the POS? I I don't know any of these things. I'm I'm asking questions. I don't have any answers.  
Maybe the right way is to ask all these questions from income because they seen a lot of cases and they know how it should work and they're not really a competitor. So to me it would be logical to ask all these questions.  
Luckily, this session is being recorded, so you could get all the.

**Nathan Carver**   24:34  
Yeah, OK.  
Alright, and we have the Incomp API I assume.

**Val Levitan**   24:45  
We do have income API, yes, of course. I don't know if income deals with it or cares about it because they make us responsible for collection of the of the funds.

**Nathan Carver**   24:50  
Mm.

**Val Levitan**   25:02  
And from our perspective, we better be able to collect the funds.

**Nathan Carver**   25:06  
Yes, and be able to audit everything that occurs on the machine.

**Val Levitan**   25:08  
Yes.  
Exactly. And and that brings me to the next subject. What if something goes wrong between us and and the location? We need to be able to lock up the server, sorry, lock up the processing.

**Nathan Carver**   25:27  
Yes.

**Val Levitan**   25:27  
So that that means for every processing aside from income, the initiation have to be from a permission to process should be ours.  
And it cannot be a functioning on simply lock up of the POS.  
It should be per processing per each processing.  
We should be the first. JVL should be the first one to allow the processing to continue.

**Nathan Carver**   26:00  
Correct.  
So one design note, and I think we briefly discussed this yesterday, was to.  
To have to give JVL better control over any communication to Incom is to rather than the Flex POS talking directly to Incom server, it has to route through the JVL cloud.  
And that way deactivating a a device's ability to issue a card can be done in the cloud. It it doesn't have to be a signal that goes back to the device. The device can just be blocked in the cloud.  
That allows all the auditing to be done automatically in the cloud.  
As opposed to how that would change here is.  
These action taken by Flex POS and then Flex POS notifies the cloud of that action. It would rather be Flex POS takes the action, it goes to the cloud, the cloud then sends that information to Incom.  
And the device just becomes a little more dumb in that regard. It it it doesn't really know what goes on, it just has a single point that it communicates with.  
The the trade off is that puts more.  
Puts more work in the cloud.  
So there's more, there's more of a lift on the cloud side, but the device becomes the device logic becomes simpler.  
So that's a trade off worth discussing.

**Val Levitan**   27:49  
Continue the.  
Continue without me.

**Nathan Carver**   27:53  
Yeah.  
OK.

**Pavel Frolov**   27:57  
But in this case it's important to our server to be all the time up and we need to to keep in mind.  
How many operations should we immediately support?  
That's why I I prefer the way where the POS directly communicates to income.

**Nathan Carver**   28:29  
Mm-hmm. OK.

**Pavel Frolov**   28:34  
In in this case, actually it can work without the cloud server, but cloud service is just a least server that gives rights for the location for.  
Terminal to work.

**Nathan Carver**   28:54  
OK, got it.

**Pavel Frolov**   28:54  
Um.  
And uh.  
Yeah, I understand that locking the location from our cloud.  
Uh, simpler to to implement it in your schema.  
But really if you if you have Internet connection all the time for the terminal, then actually we can directly push message to to lock location in case of.

**Nathan Carver**   29:15  
Hmm.  
OK.

**Pavel Frolov**   29:32  
Any fraud or something like this? I think we we can't control all the communications.

**Nathan Carver**   29:42  
Correct. OK. And OK, did you say this this connection to the cloud that's gonna be socket and HTTPS to?  
Income correct.

**Pavel Frolov**   29:58  
Yes.

**Nathan Carver**   29:59  
OK, oops.

**Pavel Frolov**   30:20  
Sh.

**Nathan Carver**   30:20  
OK.  
All right, so I know one goal was to, aside from going through a full, you know, like the failure mode analysis, we want to start building out the backlog for next week.  
Does this happy path flow give us?  
Um us the foundation to start to start that.

**Pavel Frolov**   30:51  
Yes.  
Yes, I think we can.  
Start writing the features.

**Nathan Carver**   31:02  
OK.

**Pavel Frolov**   31:02  
Problem.

**Nathan Carver**   31:08  
OK. And then for all right, so just simplify the authentication piece for September 1\.  
We would just do a pin or, yeah.

**Pavel Frolov**   31:22  
One stage, I assume it will be one stage authentication either by team or by magnetic card. So I see that we need to specify.  
Probably this tool features.  
Like card authentication on POS and PIN authentication.  
On POS.

**Nathan Carver**   31:55  
OK.

**Pavel Frolov**   31:58  
Uh, gosh.  
Um.  
In in addition to this, it will be some API. It will need some API to our cloud server.

**Nathan Carver**   32:17  
Yes.

**Pavel Frolov**   32:18  
Um.  
To to send.  
Pin on this POS device so it will be additional field in remote initial setup files that we share this POS pin.  
And or magnetic card data that will be used for access.  
The next uh feature I think.  
We'll be uh.  
Access the rights levels to provide different options for.  
Uh, for users who has pin one, pin two and pin three level.

**Nathan Carver**   33:21  
OK.

**Pavel Frolov**   33:22  
Uh, it it it gives me an idea that actually we need to specify 3 pins and to assign the three, three pins levels and 3/3.  
Cards level to be able to add cards and pins for each level of access.

**Nathan Carver**   33:49  
OK. What are your, what are those roles that you're thinking of like an admin, a cashier?

**Pavel Frolov**   33:55  
Yes.  
And manager.

**Nathan Carver**   33:58  
In manager OK.

**Pavel Frolov**   34:00  
Yeah, actually I think manager will have ability to work as a cashier plus access to reports, reports to to see information about.  
Tickets and about cards issued and at the mean I think all the rights.

**Nathan Carver**   34:19  
OK.

**Pavel Frolov**   34:26  
Access everything with ability to change some parameters.  
But probably without option to answer a working mode prohibit issue in the cards probably for being.

**Nathan Carver**   34:33  
OK.  
OK, so the September 1 feature is we can.  
We can authorize with one of three cards or pins, so admin, manager, cashier.  
So there's gonna be a API service in the cloud that takes that either the pin or the magnetic card data.  
Um.  
So for the.  
I guess for this for September one, we aren't actually gonna look at any reports, but do we want to create some report use cases?  
Or at the very least show that that um.  
That manager access can actually go view a report screen.

**Pavel Frolov**   35:43  
We definitely need until September 1st reports.

**Nathan Carver**   35:43  
Maybe.

**Pavel Frolov**   35:53  
Reports by issue with cards on our cloud server.

**Nathan Carver**   36:01  
OK, so this is something the cloud would generate.  
OK.  
All right.  
Um, then for let's see here.  
So for setup mode, um.  
OK, so the setup mode is something we'll go through for this September one as well. So let's see network configuration income credentials.  
Manually update the firmware via USB. Do we wanna do that on September 1, manually updating the firmware?

**Pavel Frolov**   37:02  
Uh, not sure. Not sure.

**Nathan Carver**   37:06  
Mm.

**Pavel Frolov**   37:07  
But at least at least actually we'll have some procedure. I assume we need to be able to somehow install software. Highly likely it will be via the USB stick, so it will be automatically.  
Implemented, but again, we still do not have an actual platform. We do not know this 100%.

**Nathan Carver**   37:35  
OK, got it.  
Oh, and then the lease feature.  
So we do want to let's see.  
Do you want to do a termination of the lease feature on September 1 where we can lock out?

**Pavel Frolov**   38:07  
Yeah, I think we will do this because we already have.  
Like the same feature for Flex POSI think probably with minor changes and it will be applicable.

**Nathan Carver**   38:26  
OK.

**Pavel Frolov**   38:31  
Here you see that there is no passport capability specified in this document.  
And uh.  
This could be also a problem. Not a problem, but.  
A difficulty to implement the passport because before before this project we used one wire E prom.  
That is not directly connected to motherboard and we use our I/O board same as used on all the cabinets, but for POS you do not need to specify additional hardware.  
And uh, we do need to decide on hardware le level.

**Nathan Carver**   39:28  
Yes.

**Pavel Frolov**   39:33  
How to treat? How to write some?  
Some data to some EEPROM or adjust to to some special storage. I don't know right now. Also need to to investigate.

**Nathan Carver**   39:54  
OK.  
All right.  
OK, so.  
We're gonna have, so I see the use cases for setup.  
So we'll have the setup use case and then features to work on.  
So I see a priority of setup, authenticate, simple authentication and then redeem gift card.

**Pavel Frolov**   40:30  
It.

**Nathan Carver**   40:34  
And then after that we have um.  
The ability to generate a report and the ability to terminate the lease of a device.  
OK. Those are the priorities that I see for the September one.

**Pavel Frolov**   40:47  
Yeah.  
Yep.

**Nathan Carver**   40:52  
OK.

**Pavel Frolov**   40:58  
Yes.

**Nathan Carver**   40:59  
All right.  
That makes sense to me. I'm gonna continue. Um.  
Let's see. So I started flushing these out here.  
And I will continue creating. I'll create those other use cases in here. Um.  
Just to capture them in confluence and then.  
All's I need is a JRO location and we can do that now or we can start on that Monday. Just need a JRO location to start placing work items.

**Pavel Frolov**   41:34  
Do you have access to our Jira?

**Nathan Carver**   41:39  
Yes.

**Pavel Frolov**   41:41  
So I think we can work on under the Flex payment project. I will share a link with you right now and there I think we we will need to create infrastructure meaning.  
Uh oh features.  
In plans, I think we need to create initiative level POS or probably to already created.  
So.

**Nathan Carver**   42:23  
OK.

**Pavel Frolov**   42:25  
Sure.

**Val Levitan**   42:29  
We're on a very, we're on a very tight schedule. I strongly recommend to have everything in place and set up now and especially Nathan has some free time, well free, I mean has some time to dedicate to this project.

**Pavel Frolov**   42:30  
This is a flip.

**Nathan Carver**   42:33  
Oh.

**Val Levitan**   42:46  
So I'm trying to drive it as hard as I can.

**Nathan Carver**   42:49  
OK, yeah, all's I need is a and a sandbox to get into and I can start.

**Val Levitan**   42:57  
I also recommend. I also recommend moving away as much as we can from Confluence into GitHub.

**Nathan Carver**   42:58  
Start dude.  
Moving the the documentation.

**Val Levitan**   43:23  
If possible, it's not. It's not a mission critical, but if possible, let's do.

**Pavel Frolov**   43:24  
Mhm.  
Oh, we already have a Flex POS. This is a IP 902\.  
So here actually we can.  
Eight features at at least just just the least in plans.  
So.

**Nathan Carver**   44:02  
OK. And how do I get to that company portfolio?

**Pavel Frolov**   44:03  
Spring.  
This is a link.

**Nathan Carver**   44:23  
OK, it does look like I have access to that.  
Yeah, I'll need access to those things, to those projects.

**Pavel Frolov**   44:58  
Thank you.

**Val Levitan**   45:04  
Do you need the? Do you need me to call Andre Pavel?

**Pavel Frolov**   45:10  
Yeah, yeah it it it will easily to add credentials, but I will try to start creating some some records here.  
Yes.

**Val Levitan**   51:27  
So.

**Pavel Frolov**   51:30  
OK.

**Val Levitan**   51:31  
No.

**Pavel Frolov**   56:26  
And.  
Nathan, any ideas? Is it? Is it OK?

**Nathan Carver**   56:30  
Yes.

**Pavel Frolov**   56:34  
Some some other features, probably one second.

**Val Levitan**   56:41  
I just want to put my $0.05 into it. I think it's important to develop a set of capabilities before we develop features.

**Nathan Carver**   56:56  
Yeah. So with the two main capabilities we've flushed out is the ability to.  
Authenticate and authorize a user and then the 2nd is the redeem a card.

**Val Levitan**   57:10  
And also, these features are extremely long. They're not a week long things and we won't be able to test them, nor will be able. I mean, it's too much to test them, too many things. It's very difficult to monitor this. It's going to stretch out for weeks.  
Upon weeks upon weeks.

**Nathan Carver**   57:32  
Yeah, so um.  
We'll want to create some slices on the the main priorities that we have and what can we do it? What can we do in a week? What can we get feedback on in a week or two weeks?  
So Pavel, is this? I know this is all new Greenfield, but is there a testing environment where we can test the system or does it have to be deployed to a device? Like how do we iterate on the development of the application?

**Val Levitan**   58:09  
I think talking about tests is a good thing. It's a very healthy approach.

**Pavel Frolov**   58:21  
Actually, I think.  
We can run tests based on current platform.  
Current I mean Flex pay device as we are going to develop everything. I mean logic, not everything logic of POS.  
In Java.  
So at least it can be tested on developers machine first of all and then on the hardware that we already have.

**Nathan Carver**   58:55  
Hmm.  
OK.  
OK, so we can reasonably do. Um.  
Iterative demos from.  
The development environment so we can see the evolution of the features.

**Pavel Frolov**   59:26  
OK.

**Nathan Carver**   59:35  
So is this is this timeline here? So the flex POS and then these items, what are the developers work from? Are these the the items that are pull these like FP359? Someone would pull this?  
Or Igor would like pull this entire feature and start working on it? Or is there more granular tasks that we break them?

**Pavel Frolov**   59:57  
No, no, he will create stories under this features.  
And the same throughout.

**Val Levitan**   1:00:05  
It it used to, it used to be that way. We used to do that up until now. We're we're very much contemplating right now.  
Reading stories within GitHub instead of here.

**Nathan Carver**   1:00:25  
OK, I got it. Yeah, create issues in GitHub.

**Val Levitan**   1:00:26  
So in in my view again administrators view the way I look at at at the plans because this serves as an alignment between us and the engineer and the and the developers I to me this is kind of a lost.  
Mile.  
Alignment and this is where Pavel, can you demonstrate? When a developer takes this into development, they open a feature branch in GitHub.

**Pavel Frolov**   1:01:02  
Yeah, we we agreed.

**Val Levitan**   1:01:02  
And so now, now it resolves. Go ahead.

**Pavel Frolov**   1:01:06  
We agreed to on the level when the developer takes his task to work stories that attach to this feature is creating a branch and then works under this branch and.  
When all the stories are ready for this feature, we we make a pull request to to join this work into main.

**Nathan Carver**   1:01:32  
But.

**Val Levitan**   1:01:37  
But the changes and the advancement in thinking is in real time.  
We're talking about it as we develop the entire company habits. So it used to be it still is under each of the feature which is the purple marker.  
The purple, the purple task we used to write. We still write stories which are green.  
Mark, just introduce a story, please. Pavel here. Any story. You don't have to even save it.

**Nathan Carver**   1:02:09  
Mhm.

**Val Levitan**   1:02:17  
OK, so that's a story, but it's extremely inefficient for overall alignment because it the feature becomes very polluted.

**Pavel Frolov**   1:02:18  
Yeah.

**Nathan Carver**   1:02:34  
Yeah.

**Val Levitan**   1:02:34  
And it's very difficult to monitor. So the the suggestion here Aaron and I have been discussing and we brought Pavel into this discussion too, is to stop at the level of feature here.  
And then from here, when a feature branch is open in GitHub, the rest of the micromanagement to run it in GitHub.  
Because we really, as far as the company alignment, it's hard to align ourselves more frequently than, you know, on the feature level.

**Nathan Carver**   1:03:17  
Yeah.

**Val Levitan**   1:03:17  
So having having features sit here in Jira and the developers really don't go.  
On that level within Jira, it becomes nuisance for developers because the developers really they their ecosystem is is GitHub.

**Nathan Carver**   1:03:34  
I agree.

**Val Levitan**   1:03:43  
And I would be absolutely, perfectly fine not seeing any of the stories. I don't even understand them. They're too technical for me and they're not negotiated with me. The only, the only level of negotiation and the only level of.  
Influence that I could comprehend is the alignment between capabilities and features. So to me, capability is something on the product level that is developed at this stage right now. This is the negotiations of capabilities.  
And then it moves from user experience or user story perspective of application of a feature.  
The feature as Pavel demonstrated here in Jira, there is a there is a link there you open feature in GitHub.  
And that's the end of it. The rest should be negotiated, should be monitored, should be done on the level of GitHub.  
We don't need anymore labor.  
At this level, because this labor right now, this labor lies on Pavel and I want to free him from that.

**Nathan Carver**   1:05:08  
Got it.

**Val Levitan**   1:05:08  
Because it's a now Pavel acts as an administrator for all of the developers. It's extremely counterproductive for me to use my director of engineering as an administrator for my developers.  
It's really stupid.  
I don't want to do that.

**Nathan Carver**   1:05:31  
OK, this makes sense to me.

**Val Levitan**   1:05:33  
So this is I'm I'm envisioning that this is where you, Nathan and Pavel. This is your last point of an interaction.

**Nathan Carver**   1:05:38  
Mhm.

**Val Levitan**   1:05:45  
And then it goes to Pavel and Pavel says OK, what do I need to do? Then it's negotiation between Pavel and the developers and Pavel now pushes for a feature to be completed within a week.  
Complete it, pull it into main and test it before you pull it in.  
And I I envision now you Nathan saying hold on this capability will have 123 features assigned to it. How do we test all these capabilities or or this capability with throughout these three features?  
Before it is pulled into main, show me that it works.

**Nathan Carver**   1:06:33  
OK, so the so the JIRA board, so this right here what we're looking at these features in this board would more closely align with the the capabilities that we're discussing.  
So they may be a little bit bigger because they're defining an entire set of capability.  
um and then from here.

**Val Levitan**   1:06:58  
They're they're a little bit bigger right now because we are not used to thinking about completing a feature and pulling it into main. We we used to have this long snake, long fat snake.  
Crawling and crawling and crawling and feeding into feeding onto a lot of stories and becoming fatter and fatter and bigger. We don't want this. We want to collapse a feature as soon as it becomes testable.

**Nathan Carver**   1:07:22  
Yes.

**Val Levitan**   1:07:35  
And deliverable and we want to deliver a feature, close it and then say OK, the capability is still not fulfilled.  
We need additional progression of the features to continue developing this capability. So the capability becomes this long living substance of a product and it's easy for administrators to understand the development, future development of capability.

**Pavel Frolov**   1:07:48  
See.

**Val Levitan**   1:08:04  
capabilities and we can understand the MVPs or features.  
But we cannot get down on the level of the stories and we want to see features constantly a completion of constant completion and revolution of features, evolution of features.

**Nathan Carver**   1:08:10  
So.

**Val Levitan**   1:08:24  
So our capability grows in its.  
Definition of it being capable of delivering something more.

**Nathan Carver**   1:08:38  
So I agree with the moving the engineering work into GitHub, I think.  
I think what that's going to do is.  
If the lowest piece of the smallest piece of work that the engineer is pulling is an issue in GitHub, and that issue has a defined, I guess.  
A piece of the feature or a contribution to the feature, or maybe an entire feature, it doesn't really matter. But the issue that the engineer, the issues are designed to be completed within a week or less.  
And ideally there's a branch for that issue, and when that issue is completed, that branch is merged in and it's actually testable right at the end of the week.  
The level of granularity if if that's like a whole feature or a piece of a feature.

**Val Levitan**   1:09:33  
And it.  
No, it's the whole, no, it's the whole feature, but it's a piece of capability.

**Nathan Carver**   1:09:40  
M.  
OK, I see. I see where the terminology is aligning. OK.

**Val Levitan**   1:09:45  
We we understand the fulfillment. We we understand that a capability is this large bucket. It's a bucket and when a product is introduced.

**Nathan Carver**   1:09:57  
Yeah.

**Val Levitan**   1:10:01  
Not every capability is at at its full implementation.

**Nathan Carver**   1:10:06  
Correct. Yeah.

**Val Levitan**   1:10:07  
So, so we understand that this bucket might be growing and that the the product may grow in capability, sorry the product may grow in in the defined capabilities and or.  
Another revision of a product may open up new capabilities.  
We also understand that the negotiation between the developers and administrator or administration lies in negotiating.

**Nathan Carver**   1:10:31  
Yep.

**Val Levitan**   1:10:42  
The features that will that would add to capabilities and it's the language that we can understand and our our ear can comprehend and we don't have to be engineers.

**Nathan Carver**   1:10:55  
Correct. So if.

**Val Levitan**   1:10:56  
And especially bringing you into the picture, negotiating with Pavel and both of you are engineers. Both of you could close the gap for administration to say we are discussing this particular subject.  
Are we aligned here and we can align ourselves?  
But then our comprehension is not enough anymore. We cannot speak on the granular level of stories with the developers and we don't need to. But what we want to ensure is that when you deliver a feature for a capability.  
show me that my capability grew in its fulfillment.

**Nathan Carver**   1:11:45  
OK, got it. So if.

**Val Levitan**   1:11:47  
And to show me in to show me is the completion of 1235 store features.  
And therefore the features themselves become shorter. The developer on the other side clearly, with no obscurity, understands what set of features he or she is working on.  
And they can close the feature by a virtue of passing it through a a set of tests.

**Nathan Carver**   1:12:19  
Correct.  
So my thought here is to break away from the Jara terminology and focus on.  
So for example, we take the capabilities that we want for September one, we put them under each capability goes. Oh, sorry.

**Val Levitan**   1:12:40  
I just just just before, just before you go, before you go further, Aaron and I, we already realized that in in this particular view we need to add another level. So it has to be a level of product which is what you see in blue in this case.

**Nathan Carver**   1:12:47  
Hmm.

**Pavel Frolov**   1:12:52  
OK.

**Val Levitan**   1:13:00  
That's IP 902, that's your product. And then between the blue and the purple, there has to be a layer of capabilities. It doesn't show right now. So we are if you and Pavel and I, we all agree on this level then.  
All I need to do is to trigger Aaron to restructure it.

**Nathan Carver**   1:13:27  
Um.  
That makes sense to me. I don't know if if we need that level like. So where I'm thinking is if this the purple here, let's say the purple defines the capability and the capability is that redeem gift card workflow that.  
We looked at.  
And in that workflow is all those essentially all those communications that is happening to fulfill to to enable that capability completely for September one and.  
So if that is defined fully in here in in one of these purple cards in JIRA.  
And then it's basically we create issues in GitHub and these each issue is a a block of functionality that's implemented to fulfill that capability.  
But each issue is designed to only live a week. It's implemented at the end of the week, so that means the engineer would pull an issue. They would understand exactly what they're implementing for the larger capability defined here in JIRA.  
And the workflow for the engineer would be pull the issue, understand the issue, create a branch for that issue at the end of the week, test merge completed, right? It merges back into the main line and it can now be tested as a whole with all of the other contributions.

**Val Levitan**   1:15:08  
So I tell you, so you're not wrong. And I'm not saying that you're wrong. I'm not. I'm not even implying this. I'm just saying the the gap that will exist then.  
On the administration side.  
We as administrators have difficult time imagining or visualizing the progression of a capability unless we see features adding to capability.  
So that's why in this view, fine, you could call purple marker, you could call it capability, but then I need another level of a feature. I need multiple features for capabilities. I need features to start and close on a weekly basis.  
And I need the bucket of capability always remain the same, but capability growing in its in its fulfillment in in what it can do, what the product can actually do. So to me a set of implementation of the.

**Nathan Carver**   1:16:05  
Yes.

**Val Levitan**   1:16:14  
MVP features is the visual attraction of seeing capabilities improve or capability doing more, and this is what's missing for me.

**Nathan Carver**   1:16:26  
Correct.

**Val Levitan**   1:16:29  
And this is what right now is a nuisance for a developer. So developers don't need, they cannot, they do not want to. We're forcing them, but it's not working. They cannot work in Jira. They need their tasks in GitHub.  
And they need the GitHub to be their residents.

**Nathan Carver**   1:16:52  
Hmm. Yep, I agree with that.

**Val Levitan**   1:16:55  
For me, I don't care where they work. All I need to know, all I need to have is the accountability for their deposits of artifacts.  
Let them put their artifacts into GitHub and I am absolutely comfortable of using the GitHub counters. I'm using the word counters loosely as a metaphor for controls.  
So the artifacts are deposited. I can go and see what's deposited. I can account for any sort of speed.  
Of accomplishment or velocities.  
Within GitHub.

**Nathan Carver**   1:17:47  
Mhm.

**Val Levitan**   1:17:48  
But then my thing is OK, you pull this feature into a branch. You open a feature branch in GitHub. The feature branch cannot stay open.  
For too long.  
It needs to close. OK, if the feature branch stays open. What the \*\*\*\*? What happened? Why is it open?  
The feature branch. You keep on opening feature branch, but it doesn't add anything to capability. My capability is not becoming more capable. What the \*\*\*\*?  
So these things are very easy to detect for me, for any any administrator, and I said it sets for a very easy conversation. Another conversation is you keep on adding features, you're not testing them. Where are my tests?

**Nathan Carver**   1:18:34  
Hmm.

**Val Levitan**   1:18:47  
These things are very observable and very testable and very in front of you and very easy language to communicate between administrators and developers.

**Nathan Carver**   1:18:52  
Yeah.  
OK.

**Val Levitan**   1:19:06  
Pavel, do you have any objections to what I'm saying?

**Pavel Frolov**   1:19:09  
No, no, it's quite obvious. Just just one thing. I I think nobody in our team worked with issues in GitHub needs some.  
Learning.

**Val Levitan**   1:19:28  
But I don't care. I don't care whether they break out the feature into additional stories in GitHub or not. I I don't care about it if they don't need more granular exposure.

**Pavel Frolov**   1:19:28  
What is this?

**Val Levitan**   1:19:44  
Then let them work with it in the future. I don't care that I understand you correctly what you said or no.

**Pavel Frolov**   1:19:49  
Yes, yes, yes.

**Val Levitan**   1:19:52  
I mean, this is if if a developer says, hey, I understand what I need to do for a week of work, I don't need more granularity. I will bring that feature into life. It will be testable. I don't need any more questions and if they do.

**Pavel Frolov**   1:19:52  
Yes, so.

**Val Levitan**   1:20:11  
They come to you and they negotiate how to do it. To me, it's important that the feature gets closed and gets pulled into the main.  
Because the if the if features do not get close, there is, there is unclarity, there is a fog, there is a obscurity of some sort.  
And and I want to kill it. I want to kill it on its roots immediately.

**Nathan Carver**   1:20:46  
OK, so we can, so we'll have Aaron value and Aaron can create that, right? I I can jump in too, it doesn't matter, but we can add that capability layer.  
And the the way the granularity will work is I will take for example the redeem gift card for September one will be a a capability and.  
And.  
I will then build um.  
Features under that that build out that capability and a feature will be intentionally designed to be done within the week, right?

**Val Levitan**   1:21:29  
So.  
So let let me make it even easier. Let me make it easier.

**Nathan Carver**   1:21:33  
Hmm.

**Val Levitan**   1:21:36  
A. A capability, let's say redeem a card. I I understand the capability. I understand that it needs to be delivered to September. But maybe first of all, who develops features? I think development of a feature is a.  
Point of negotiation between you and Pavel, Nathan and Pavel, right?

**Nathan Carver**   1:21:56  
Mm-hmm.

**Val Levitan**   1:21:58  
But maybe you guys don't see all of the features that go into development of this capability. Yeah, you don't see it in the beginning.  
I don't need.  
5050 features.  
To be written out at the same, you know at one instance.  
If you see five, if you say OK, right now we see that far, we don't see any further, but write out five features as they start working through them. Keep on adding more features.

**Nathan Carver**   1:22:41  
Correct. Yep.

**Val Levitan**   1:22:43  
Because sometimes engineers don't see from A to Z, they only see from A to B to C to D.  
And maybe it's a it's a zigzag a little bit, but at least I understand that it's how the capability will grow.

**Nathan Carver**   1:23:04  
Um, OK, so the.  
So our our the desired outcome is features that are incremental right done within the week time. Branches are not long running. We close those out at the end of the feature, ideally within a week.  
This is showing us progression of. So if we have a rough estimate of there's 10 features in this capability, we may add five more, we may not right. So now we can see an incremental progression towards completion.  
Um.  
I think having that capability, it's really, it's just how are we using JIRA. Like I don't think we need one capability to one JIRA ticket. I think like if we use September 1 capabilities, there's gonna be September 15 capability and that's probably gonna be.  
Updating right the the redeem gift card, higher level capability. It's just like the phases that it's going through.

**Val Levitan**   1:24:14  
It I mean you could grow a capability or the product may gain a capability. Maybe I'll say OK, a POS right now has only one screen, the attendant facing screen and that's the capability of the POS.

**Nathan Carver**   1:24:20  
Correct.  
Hmm.

**Val Levitan**   1:24:32  
Next year, please add the second opposite screen that would face a customer.

**Nathan Carver**   1:24:41  
And you want to, you want to see that in JIRA, right? You want to see those capabilities represented in the JIRA structure knowing that that's going to grow. It's not officially done, but we do have like a time box deliverable that we want to track to which is.

**Val Levitan**   1:24:41  
And.  
Look, look.  
Look.

**Nathan Carver**   1:24:58  
The capability for September 1, for example.

**Val Levitan**   1:25:02  
I do not want artificial.  
Satisfaction. I want normality of how we work and if we can foresee a capability that we want, if we can talk about a capability that we want.  
Well, let's say for next year. And if we say yes, we want the POS with two screens, but we cannot develop it for September 1st. But what we should develop is we should have the hardware and we should have our.  
Hardware components that could drive the second screen and the industrial design should have a housing capable of housing 2 screens.

**Nathan Carver**   1:25:52  
Mm-hmm.

**Val Levitan**   1:25:53  
But we are not going to put it on the Linux level or hardware abstraction level or we don't need to talk about a user experience right now for the second screen.  
We can talk about it in November, so I don't need you to write out features for this capability, but you should probably put a capability of having second screen.

**Nathan Carver**   1:26:20  
Got it. OK.

**Val Levitan**   1:26:22  
But there will, but there will not be any features around that or the feature will be right now on the hardware side have insert the IC chips.  
Onto the board, populate the board with IC chips to run the second monitor, provide LVDS output.

**Pavel Frolov**   1:26:46  
Yeah.

**Nathan Carver**   1:26:52  
Correct. OK.

**Val Levitan**   1:26:53  
And test it. Make sure that we can power up the second screen.  
But maybe nothing else.

**Nathan Carver**   1:27:02  
OK. I think this is making a little more sense to me. I I get the sense that the structure we're looking at in JIRA is more of a system of record. So we have capabilities and we have features within those capabilities.  
And those are going to evolve because our capability could evolve and we're going to create new ones.  
And then there's a second piece of project predictability and tracking progression, and the Jira structure doesn't really align to that because of what the Jira structure is trying to do is.  
This is the capability, this is the evolution of that capability and feature. So we need like if we if we use GitHub and put the engineers in GitHub and we had because in GitHub we can set up a project.  
And we can just have the issues in GitHub and we can put all those issues in that project and we can start planning and tracking progression towards our deliverable.  
That way that decouples the engineering planning from that JIRA hierarchy and gives them some flexibility in in how they're planning to implement that. So I think the trade-off there is.  
If we use GitHub for project tracking and JIRA for like the actual capability and feature system of record, I think that gives engineers a lot of flexibility in GitHub. It's going to be easier for them to do issues and branching.

**Val Levitan**   1:28:33  
Alignment.

**Nathan Carver**   1:28:43  
Issues. There's going to be more administration between the two systems just to make sure that the project plan aligns with the features, but I think that's where my role could come in and that lets Pavel play more in the in the engineers just focus in GitHub and and issues.  
And it gives them more flexibility on controlling their branches. They don't have to tie their branches back to to JIRA necessarily and.

**Val Levitan**   1:29:10  
They do. They they do. They actually do. And this is where the alignment and synchronisation comes in. They they they tie themselves by virtue of grabbing a feature branch.  
Into work.

**Nathan Carver**   1:29:27  
Correct.

**Val Levitan**   1:29:29  
And so when that feature branch is complete and they pull it into main, they issue a pull request in GitHub. It is approved, let's say after tests and when when when it is pulled into main, the feature needs to be marked complete.  
So that means there is a signal in Jira now that says it's complete, it's done.

**Nathan Carver**   1:29:57  
Correct.

**Val Levitan**   1:29:57  
And that sets out a flag for administration that things are moving correctly or incorrectly.

**Nathan Carver**   1:30:05  
So if we let them work in, if they were, if they want to use GitHub issues, then ideally their branches would be tracked to those GitHub issues and not directly tracked to the JIRA feature.

**Pavel Frolov**   1:30:15  
Yes.

**Val Levitan**   1:30:21  
It is because Pavel show please again.

**Nathan Carver**   1:30:25  
I know, I know it is now, but if we if we have them work with GitHub as opposed to having them work in JIRA, then their branches would be tied to the GitHub issue. That would be a change from how we work now.

**Val Levitan**   1:30:30  
You.  
No, because they initiate a GitHub.  
Uh, start of work by pulling a feature.  
Into a GitHub branch.

**Nathan Carver**   1:30:53  
Correct. That's what they do right now.

**Val Levitan**   1:30:56  
And I would like to keep it the same way.

**Nathan Carver**   1:30:58  
OK, OK. So if we keep that the way it is then.  
Then.  
They would not be. Well, there may be less value for them using GitHub issues to track their tasks.

**Val Levitan**   1:31:14  
Why?

**Nathan Carver**   1:31:16  
Because there's still if the branch is tied to the feature.  
Um.  
It still creates, it kind of creates some. It more tightly couples their work to the feature than it does to their tasks. So if I have a feature in JIRA and I'm going to implement it and I may task that feature out to six different tasks.  
There's no reason I can't create a branch for a task, implement the task, close that branch and that branch, that task is now testable. The feature isn't, you know, holistically implemented, but my tasks may be completed, implemented, and testable.  
And that allows the engineer to break down that feature in a in a iterative sense. And so it's more, it's measurable at a more granular level.

**Pavel Frolov**   1:32:10  
OK.

**Nathan Carver**   1:32:11  
I think the trade-off there is it's highly flexible and efficient for the engineering side, but we're losing the direct traceability of a branch, you know, being tracked in Jira and you being able to see.  
The completion of that, you may not easily see the completion of tasks that are rolling up into that feature, so there's more administrative work to create that traceability.  
And I think staying with the method now is the trade-off is traceability is much easier. We can see that, but the the the negative is it's less flexible for the engineers.  
And a side effect is features could be running longer on their branches, right? So I think those are the trade-offs we're dealing with.

**Val Levitan**   1:33:04  
I cannot. Maybe Pavel can, but I don't have enough knowledge, practical knowledge, and I have. I don't know how to appraise the difficulty of.  
Keeping this alignment alive in GitHub and JIRA, but from what I have seen so far, there's absolutely no overhead or hardly any overhead in marking a feature as complete.

**Nathan Carver**   1:33:23  
Hmm.

**Val Levitan**   1:33:39  
When the branch is pulled, when the development branch is pulled into the main, and I actually think that even further that could be automated.

**Nathan Carver**   1:33:44  
Yes, that should be automatic.  
Correct.

**Val Levitan**   1:33:53  
So to me, a signal of branch has gone into a feature has gone into work by virtue of.  
Opening a development branch in GitHub is a signal, and another signal is that the development branch was pulled into the main. That means it has been tested and the feature is closed.  
And that's another signal. So between these two signals I can see how I can function.  
And these signals is hardly any overhead. I mean, I Pavel, do you see any overhead for developers?

**Pavel Frolov**   1:34:38  
Frankly speaking, this is already automatically work in Jira when you perform all the operation related to creating feature branches.  
Creating pull request merging to main. When the developer perform all the steps it it will automatically reflected in Jira if correct issue.  
Uh number specified in Uh commit message.

**Nathan Carver**   1:35:18  
Correct. Yep.  
So when we when we say that we wanted the engineers to work in GitHub because that's kind of their that's more native right to what they're what they're doing.  
Is it we just continue? It's not issue tracking in GitHub, it's basically just the continuation of running branches in GitHub.  
It might not. Maybe I'm not understanding that correctly.

**Val Levitan**   1:35:53  
Now Pavel, can you go through one cycle and show exactly? Please share your screen.  
So if you go in that view in the lans view.

**Pavel Frolov**   1:36:11  
Mhm.

**Val Levitan**   1:36:16  
Pick any branch. I mean, you don't have to commit afterwards, but.

**Pavel Frolov**   1:36:22  
Let's.

**Val Levitan**   1:36:22  
Let's say to do, to do, yeah. So let's say you want to work on this branch.  
Sorry, you want to work on this feature, so you open the feature.

**Pavel Frolov**   1:36:33  
Yeah.

**Val Levitan**   1:36:39  
And here here comes the the development branch. You create a branch.

**Nathan Carver**   1:36:41  
Yep.

**Val Levitan**   1:36:46  
So now you're going into GitHub. This is what a developer does. So Pavel is simulating an act of grabbing a branch into taking a branch into work.

**Nathan Carver**   1:36:50  
Correct. Yep.

**Pavel Frolov**   1:36:58  
Yeah, yeah, I select from what branch. I create a new branch from mine or from different branch, then create, then work with the sources when everything is done and tested.

**Nathan Carver**   1:37:07  
Correct. Yep.

**Pavel Frolov**   1:37:16  
Uh, I can create a pull request.  
Then check this request, check the differences if if I need and make merge to the main.

**Nathan Carver**   1:37:33  
OK. And we're going to keep this in JIRA because this is the same, this is the same workflow that you would go through if you were doing issue tracking in JIRA or I'm sorry, if you're doing issue tracking in GitHub, you would do the same thing. You would pull your issue, you would create a branch for that issue and then when the issue is closed.  
The OR when the branches merge, the issue's closed. That's how the engineers would be working in GitHub as opposed to JIRA, so.  
But that's not what we're saying. We're saying we're going to keep this workflow the way it is, but the the change we want to make is that these branches here and because of the feature scope of the feature is going to be more narrowed down to a one week.  
Increment.  
And so that we can track the progression towards completion.

**Val Levitan**   1:38:29  
Well, I I don't know if it's if it's if you want to call it a change or if you want to call it.  
Normalization.  
Uh.  
It is very difficult for.  
An engineer who is.

**Pavel Frolov**   1:38:55  
Hey.

**Val Levitan**   1:38:57  
Goal oriented to foresee or to develop or to explain a very large feature.

**Nathan Carver**   1:38:59  
OK.

**Val Levitan**   1:39:08  
Because no matter how good an engineer is.  
His scope of comprehension is still limited to something, so it's easier for a developer to comprehend something that is shorter rather than something that is longer, because a longer thing is harder to define and it creates a lot of obscurity.  
The our goal is to remove as much obscurity as possible and so we want to provide a shorter cycle for an engineer and therefore instead of developing a larger feature that will.  
Fill up the capability bucket faster.  
I'd rather have more fractional development of capability, but allowing a developer to comprehend it easier.  
So it's not that we need to change how we work. I think we need to.  
Perfect.

**Pavel Frolov**   1:40:25  
It.

**Val Levitan**   1:40:26  
The explanation or the comprehension of.  
A capability, full capability, but the deliverables have to be more defined and in order to define something better, we need to make it shorter.

**Nathan Carver**   1:40:48  
OK.  
Yep, so we can run with this. Um, so.  
Until we get, we need the capability structure in in Jira, right? So the capability to feature is the Jira change we want to make with Aaron.

**Val Levitan**   1:41:08  
Yes, we want to create a level of capability.  
Leaving the future level the way it is.

**Nathan Carver**   1:41:18  
OK.

**Val Levitan**   1:41:20  
So we need to wedge a level of capability.  
Which is higher than the feature.  
Sure.  
We want to wedge it between the feature and the product.  
This level doesn't exist right now.  
So.  
You and Juan, meaning Nathan and Juan are working on the level of product capability. Then Nathan shifts his attention to working with Pavel on the level between capability.

**Pavel Frolov**   1:41:44  
Yes.

**Nathan Carver**   1:41:52  
Correct.

**Val Levitan**   1:42:00  
And feature and then Pavel takes all takes over and works on a level between feature.  
Feature testing stories.

**Nathan Carver**   1:42:18  
OK.

**Pavel Frolov**   1:42:25  
Yeah.

**Nathan Carver**   1:42:26  
That works.

**Val Levitan**   1:42:32  
OK, so.  
Refocusing ourselves on the next or or refocusing ourselves on the action list or the undertakings for the next step of developing.  
The POS for September 1st delivery. What do we need? Where do we need to go from here?

**Nathan Carver**   1:43:03  
So the next step is going to be we want to get the capabilities that we discussed into JIRA and start breaking down those into incremental features that are you know.  
Individual features that we can implement.  
So that that's our next step. And then we we identify, we prioritize those features for implementation and get the get the team working on it.

**Val Levitan**   1:43:37  
OK, so the the POS is many things. One of the things is the industrial design and the hardware design.

**Nathan Carver**   1:43:44  
Mhm.

**Val Levitan**   1:43:53  
So right now there is another group of people that is working in parallel, selecting a an appropriate hardware and working on the industrial design of how the POS will look like when industrial design is developed.  
Hello.  
We need to make a set of drawings for molds, so plastic molds, metal fabrication, fabrication of metal parts.

**Pavel Frolov**   1:44:27  
3\.

**Val Levitan**   1:44:27  
And before that is done, there's a, you know, there are a number of things that need to be answered, for example.  
Uh.  
Authentication of a user.

**Pavel Frolov**   1:44:39  
Yeah.

**Nathan Carver**   1:44:40  
8\.

**Pavel Frolov**   1:44:40  
I.

**Nathan Carver**   1:44:41  
Mhm.

**Val Levitan**   1:44:42  
Because if the authentication of the user is through a pin code, it's one thing. If it's through a swipe of some unique access card, then it's another thing. But if the privileges.  
Or the functionality.  
Of the POS is through a full insert of a of a card.  
Then it will change the design and it will need slightly different hardware. So before we move move into resolving that issue, you need to conduct a discovery call with income.  
Or maybe look at how other POS are made. Or maybe interview one or two.

**Nathan Carver**   1:45:33  
Yes.

**Val Levitan**   1:45:40  
Individuals that we may choose to test the product for us in September.

**Nathan Carver**   1:45:47  
Mhm.

**Val Levitan**   1:45:51  
But we're at the point where we need to rush with.  
Finalizing of the mechanical design.  
So that becomes a pressing priority. Why am I rushing with this? Because simple, we need approximately a a few weeks of mechanical design. We need approximately a month for tooling.  
Design.  
And we need a couple of weeks to fly in the samples of the plastic covers, and we need to bring in relevant hardware to Minsk and to Toronto.  
So we're ready for assembly.  
Assembly. I'm talking about assembly of the samples. So right now we're practically in July. We only have two full months to work on it. We really are very much pressed for time.

**Nathan Carver**   1:46:42  
Yes.

**Val Levitan**   1:46:54  
So maybe this afternoon, maybe Monday, you, Nathan, needs need to speak to income because you never spoke to them. That meeting needs to be facilitated.

**Nathan Carver**   1:47:06  
Mm.

**Val Levitan**   1:47:10  
So Pavel, you need to facilitate this meeting as soon as possible.  
Maybe now.

**Pavel Frolov**   1:47:28  
M.

**Val Levitan**   1:47:29  
You're sharing your screen in case you don't know.

**Pavel Frolov**   1:47:34  
Mhm.  
You mean that we need to discuss this income possible architectures how to?

**Val Levitan**   1:47:51  
Use cases.

**Pavel Frolov**   1:47:51  
Authenticate authenticate the users.

**Val Levitan**   1:47:59  
OK, let me repeat again.  
A POS is sitting on somebody's.  
Uh, counter.  
It's. Is it idle? Can I immediately validate the ticket or is it in some locked format?  
If it's open, are there any?  
Concerns that.  
A fraud could be committed of any sort.  
Maybe. Maybe it's OK if it's open. I I don't know.  
Or maybe it's OK that it's open for September, but in the future maybe we'll want it locked if at some point we want it locked.  
How do we unlock it quickly?  
So if the natural state of POS is to be locked.  
Whether we want it for September or for next year, if we want this capability of quick unlock.  
Then how do we unlock? We can enter a PIN.  
We can swipe a card.  
Or.  
So let's say we address the unlock this way, but is there a capability? Is there a requirement? Sorry, is there a requirement for the POS to be locked after the operation is complete?  
If it needs to be locked, then couple of things. If it remains idle, it could go and lock itself.  
Or if let's say you swipe a key and say lock it now, very impractical.  
Or if you.  
If the state of lock unlock is dictated by a presence of an attendant card.

**Pavel Frolov**   1:50:21  
Yes.  
OK.

**Val Levitan**   1:50:24  
Or some touch thing, maybe a Dallas chip that needs to be inserted and then when attendant moves away from POS it gets popped out.  
Or maybe some sort of a plastic key that inserts itself. Whatever that is, I don't know what it is.  
But if that if if there is a requirement to have the POS locked.  
We need to think how to lock it and unlock it.  
And that may become either a mechanical solution or some sort of proximity solution. I don't know what it is.  
But whatever that solution is, when the case for the POS is made, the molds are made, you cannot change it afterwards.

**Pavel Frolov**   1:51:26  
Yes.

**Val Levitan**   1:51:34  
So we need to ask a question. Is there a requirement for the POS to be unlocked to be locked after a successful session?

**Pavel Frolov**   1:51:49  
Uh, I know the answer. It's up to you.

**Val Levitan**   1:51:55  
Yeah, so.

**Pavel Frolov**   1:51:55  
100% not not 999, but 100% they will answer. It's up to you.

**Val Levitan**   1:52:04  
They will, but that allows me to ask them a question. What do others do? What would the market prefer? From your experience in all of your markets, you are a $6 billion company. You obviously service a lot of markets. What is the preference?  
And then somebody with experience could say, Oh my God, people are really annoyed with the function of swiping the card, but people are OK with inserting a card. So then we're saying \*\*\*\*, we need an insert. How does insert work? We need to make an opening in the mold.  
Is it in the front? Is it on top?  
Is that a full insert? Is that a partial insert?

**Pavel Frolov**   1:52:51  
Actually I do not see what's the problem solved by inserting a car.  
For me, it's useless.

**Val Levitan**   1:53:03  
Because.  
It could be. I'm not arguing. It could be useless.  
But my concern.

**Pavel Frolov**   1:53:10  
Because.  
So because we need to authenticate cashier, not the card.

**Val Levitan**   1:53:20  
Of course.  
That card, the identification card, when it's issued, it creates a set of privileges.  
So if one of the privileges is to operate the POS.  
Then when that card, when did that access card is issued?

**Pavel Frolov**   1:53:51  
Mhm.

**Val Levitan**   1:53:51  
How does it? How does it enable an individual who now has these privileges to operate the POS? So OK, I have the privileges.  
But what happens? The POS doesn't know that I have privileges. The card knows that you know on the card there are my privileges. It could be door access card, it could be some other thing. But now I'm at the POS.  
From what I've seen some operations, each operator carries his card or her card.  
On a on a pulley, on a retractable pulley.  
And then they insert the card into the POS and POS instantly becomes operable. Then every transaction that is made is registered to this particular individual as this individual distance himself or herself away from the POS.

**Pavel Frolov**   1:54:48  
Mhm.

**Val Levitan**   1:54:55  
The card comes out with it, the POS locks and that's it. And then the next attendant could come in, insert his card and operate the POS and all the transactions now are tied to a different.

**Pavel Frolov**   1:55:09  
Mm.

**Val Levitan**   1:55:12  
Attendant.  
So if we need, if this is a requirement, if this could be an operational requirement, it needs to be addressed.  
In the mechanical design that is being pushed forward faster than the software design.

**Pavel Frolov**   1:55:39  
Yeah, it's it's clear.

**Val Levitan**   1:55:41  
Is it? Is it clear now or was it clear before?

**Pavel Frolov**   1:55:45  
No, no, it's clear now because before I thought that you're saying about income card inserted.

**Val Levitan**   1:55:56  
No, no, I'm talking about the privilege card, the privilege access card.

**Pavel Frolov**   1:56:00  
OK.  
Yeah, for for this design we will need two different reader, one for income and one for access card. In case of swipe card reader we just need only one and.  
Cashir can use his card to start session and then use uh uh income card to read the money.

**Val Levitan**   1:56:35  
So if this could be a feasible requirement, not for September 1st, but in the future, our mechanical design needs to include.  
this design.

**Pavel Frolov**   1:56:47  
Mhm.  
Yeah.

**Val Levitan**   1:56:50  
So aside from this being written into requirements, although it's not MVP, but it should be part of the mechanical design now.

**Pavel Frolov**   1:57:05  
Mhm.  
Actually I can share probably some experience from different terminals. So usually when the session is started or day is open.  
POS holder usually enter PIN. This PIN is usually provided by a third party provider who.  
Who gets money for operation of this terminal, so usually they use it just.

**Nathan Carver**   1:57:52  
Yeah.

**Pavel Frolov**   1:57:55  
A predefined pin number.

**Val Levitan**   1:58:00  
I I think that could be a part of a different requirement.  
Nathan, you're awfully quiet.

**Nathan Carver**   1:58:19  
Yeah. So question on the on the timing.  
So the hardware is going to be essentially.  
close to being finalized by September 1, is that our goal or is there going to be some expected changes to the design that the specifically the industrial and hardware design?  
Uh.

**Val Levitan**   1:58:48  
Well, I think, I think it will be finalized. Will all the features or all sorry, will all the capabilities be engaged at that point? Maybe not, but the hard work should be finalized.

**Nathan Carver**   1:59:02  
But the the hardware, we'll we'll pretty much know what we want by then. So on the card swipe. So let's say that we.  
We go with um access card swipe.  
And the the the the card reader is when we scan gift cards, right? We also do a swipe. Can that reader do both gift cards and and access cards? Does it can it differentiate or is that just a software decision?  
Or do we have to have different card readers?

**Pavel Frolov**   1:59:42  
In case of swipe reader, we don't need to separate.

**Nathan Carver**   1:59:45  
OK.  
So from a software capability, if we have the swipe in there, we still have the option of either swiping an access card or using a pin, right? Because that's just software driven.  
The thing we couldn't do is insert right 'cause that would be a new physical.  
Component added. Would we have both insert and swipe at that point if we said if we decided we're going to put an access card in and that has to stay in there during the whole process. So we still need a swipe capability because the access card will remain inserted.

**Val Levitan**   2:00:25  
Correct.  
We could, we could probably resolve this issue by saying each.  
The the terminal locks automatically after transaction is completed.  
And if we and if we do that, then a swipe card to validate the transaction is needed and then the swipe card needs to be the attendant card.

**Nathan Carver**   2:00:45  
Yeah.  
Correct. Yeah. I think we we have idle points at any point in time. If the screen is idle for a given period, a minute or whatever it is, then it should automatically lock.  
And I think even if there's a card inserted and the screen is idle, I think we still want that same behavior. I think we should still lock the screen because if they put their card in and walk away and go do something, we don't want it sitting there indefinitely open. We still want it locking on a timeout.  
With or without an inserted card. So I don't know if that changes the behavior a whole lot.

**Val Levitan**   2:01:38  
No, my, my, my.

**Nathan Carver**   2:01:39  
Then when you get the automatic when you pull the card, we can automatically lock. That is a feature that the insert gives us.

**Val Levitan**   2:01:46  
I I think, I think what I'm saying is being taken literally right now. My my point is slightly broader. My point is this the mechanical design, mechanical and hardware design, mechanical and electronic hardware design.  
Must be completed extremely urgently and quickly that that is the most bottleneck that we have the software and implementation of various capabilities, software capabilities.

**Nathan Carver**   2:02:04  
Yes.

**Pavel Frolov**   2:02:07  
She.

**Val Levitan**   2:02:17  
Could be addressed as a matter of immediate second priority.

**Nathan Carver**   2:02:23  
Yeah, and I I think thinking through because the software can adapt to the different things quickly, really the only the decision it seems to be is do we add the hardware of an inserting a card, right? We either have that or we don't.  
'Cause the software can handle a swipe or a pin, right?

**Val Levitan**   2:02:42  
Adding it now is nothing and actually even if there is an opening in the plastic in the housing.  
It could be plugged, decoratively plugged in the product that doesn't require it.

**Nathan Carver**   2:03:00  
I see.

**Val Levitan**   2:03:00  
But but making that opening after the design is finished is extremely difficult. It will most likely require a rework of molds that is expensive.

**Nathan Carver**   2:03:12  
Yeah.

**Val Levitan**   2:03:15  
So my suggestion is.  
To create a requirement for a full insert card.  
Uh.  
That that allows us to develop this capability further. If we don't want it, we'll simply not put the reader and plug in the opening with a decorative cover.  
What make it us of the requirement right now for the mechanical and for for the electro mechanical design?

**Nathan Carver**   2:03:48  
Yeah.  
OK, so the hardware, yeah, so the box can be designed to accommodate it, but we don't have to actually implement it on the board if we don't.

**Val Levitan**   2:04:06  
And as a matter of fact, for and as a matter of fact, for September, we will not do it. It we will not, we will not even put it on the MVP, but as part of the requirement for electro-mechanical design, we must put it.

**Nathan Carver**   2:04:10  
OK.  
Yeah, that makes sense to me.

**Pavel Frolov**   2:04:22  
Absolutely. Agree.

**Val Levitan**   2:04:26  
OK, so back to the undertakings and the action list. The undertaking is to complete a.  
Set of requirements for the electromechanical design.  
As a matter of first priority.

**Nathan Carver**   2:04:56  
So for for this for the electromechanical design the requirements. So this these would be the software requirements that we would that would be dependent on that electromechanical design correct. So like the the the.

**Pavel Frolov**   2:04:56  
Mhm.

**Val Levitan**   2:04:57  
I.  
Hello.  
More more of a functional design. How will it function? So more more of use cases, use cases rather for a cashier or.

**Nathan Carver**   2:05:18  
Yeah.

**Val Levitan**   2:05:30  
Um.  
Location management.

**Nathan Carver**   2:05:37  
OK.

**Val Levitan**   2:05:38  
Not not really applicable to use cases for the players, so I would look at other persona, other personas that are related to the use of the POS.

**Nathan Carver**   2:05:45  
Got it.  
Got it.

**Val Levitan**   2:05:59  
So that would be my objective for today and for Monday. I will try to nail that.

**Nathan Carver**   2:06:08  
OK.  
All right. Yeah, that sounds good. We'll work on that.

**Pavel Frolov**   2:06:15  
Thank you.

**Nathan Carver**   2:06:19  
So use cases focus on use cases from the different personas. So that would be well the three that we've identified. So we've admin, manager, cashier in addition to the the player which is I guess far less impact on this.  
Um and the Uh support specialist, right? Technical.  
So that the Technical Support, the admin, the manager and the cashier, those are the four personas that I'm thinking of that would directly impact.  
The design.

**Val Levitan**   2:06:55  
The electric, the electro-mechanical portion of the design, yes. And then so if we nail all the requirements from the those persona views.

**Nathan Carver**   2:06:59  
OK.

**Val Levitan**   2:07:07  
Then we can intelligently discuss the electromechanical requirements for the POS.

**Nathan Carver**   2:07:17  
OK.

**Pavel Frolov**   2:07:23  
Oh.

**Nathan Carver**   2:07:23  
OK, that sounds good.

**Val Levitan**   2:07:23  
So, so in order for you to accomplish this in in a short possible shortest possible time, I suggest that at least you pick the brains of income, John from income.

**Pavel Frolov**   2:07:25  
OK.

**Nathan Carver**   2:07:41  
Yes.

**Val Levitan**   2:07:42  
He's got a wealth of experience and I would just have at least one conversation with him.

**Nathan Carver**   2:07:47  
OK. Can we set that up for Monday works unless we can do it later today, but I'll be more prepared for it on Monday.

**Val Levitan**   2:07:57  
OK, Pavel, can you set it up for Monday?

**Pavel Frolov**   2:08:01  
Uh, meeting.

**Val Levitan**   2:08:03  
Meeting with John.

**Pavel Frolov**   2:08:06  
This is John, OK.

**Val Levitan**   2:08:06  
Income, you know.

**Pavel Frolov**   2:08:09  
OK, we will write a message to him.

**Val Levitan**   2:08:20  
OK, that's it for for this meeting.

**Pavel Frolov**   2:08:24  
Yep.

**Nathan Carver**   2:08:26  
Right.

**Pavel Frolov**   2:08:26  
Thank you.

**Nathan Carver**   2:08:27  
All right. Thanks. See ya.

**Val Levitan**   2:08:28  
Thank you.

**Pavel Frolov**   2:08:29  
Bye.

**Val Levitan** stopped transcription