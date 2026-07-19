---
tags:
  - meeting-transcript
  - product-roadmap
  - implementation
  - juan
  - pavel
  - flex-port
---

**Transcript**

*Note: Juan Martinez is the VP Product Owner for flex-port and related products.*

June 27, 2025, 12:32PM

**Juan Martinez** started transcription

**Juan Martinez**   0:34  
That coffee smells good, Pavel.

**Pavel Frolov**   0:39  
It's just water.

**Juan Martinez**   0:40  
Oh, no.

   0:40  
Uh.

**Pavel Frolov**   0:42  
OK.

**Juan Martinez**   0:43  
I'm in an empty office. I don't even have water right now and I'm I'm dying for a coffee.

**Nathan Carver**   0:49  
Gosh.

**Genadi Peari**   0:50  
The office looks nice though.

**Juan Martinez**   0:53  
Oh yeah, I wish it was that nice. Yeah, we we're actually moving out today. So we pretty much moved out and I got to turn the keys over as soon as we're done with this call.

**Nathan Carver**   1:06  
Yeah, you got nice beachfront property there, so.

**Juan Martinez**   1:09  
Yeah, we're actually only two or three miles from the ocean, but not quite with that view, even though we're on the 4th floor here.

**Nathan Carver**   1:15  
Oh.  
No.

**Juan Martinez**   1:23  
Oh, did was Val going to join or do we start with Adam? Let me send.

**Nathan Carver**   1:27  
Um, he did accept.

**Juan Martinez**   1:29  
OK.

**Nathan Carver**   1:33  
No.  
But we may just want to get started.

**Juan Martinez**   1:41  
Sending up a message now.

**Nathan Carver**   1:45  
OK.  
Yeah, he accepted and we're almost 5 minutes in. So I dropped the Confluence doc into the into this meeting chat. If everyone can't open it, I can go ahead and share my screen and walk through it.  
Maybe I'll do that just to think it's on the recording.  
OK, is the document.  
Coming through, make sure I share the right window.

**Juan Martinez**   2:28  
Yes.

**Nathan Carver**   2:29  
OK.  
So for this meeting, what I I really wanted, I know Pablo and I discussed last week getting these requirements in the Jira so the team can get started.  
I wanted us to agree on the road map that we have in here, the a cadence for us to to meet regularly and start the implementation and then we can select a few. We can select the first.  
Few requirements to really zero in on and the requirements we select would be obviously driving us towards initially the September 1\.  
Beta release there.  
So I see Val's joining us.  
I've been using this doctors to drop my own comments and questions in, so please feel free to comment and question here so we just have a living notes.

**Pavel Frolov**   3:20  
Mm.

**Juan Martinez**   3:33  
Absolutely.

**Nathan Carver**   3:33  
Um.  
So hey Bill, I was just letting them know the.  
The focus of this will be to get us ready to start driving implementation next week. So we would just want to agree upon our release of the road map, specifically the September one and then.  
Agree upon the cadence and then select some requirements to focus on 1st.

**Val Levitan**   4:02  
Yeah. Good morning, everyone. Good to see you.

**Juan Martinez**   4:04  
Good morning.

**Pavel Frolov**   4:05  
Good morning.

**Nathan Carver**   4:05  
Morning.

**Val Levitan**   4:07  
This meeting is recorded, am I correct?

**Juan Martinez**   4:10  
Yes.

**Pavel Frolov**   4:10  
Yes.

**Val Levitan**   4:12  
OK, great.  
Yeah, I had a chance to comment on some of the things. Didn't have enough time to finish everything, but yeah, whatever I did.

**Nathan Carver**   4:15  
OK.  
OK.  
So is for the most part, does the September 1 release as defined here, is that have enough maturity for us to start moving in this direction? Is there anything in here that?  
Um, we really need to change it and talk through before we get started.

**Val Levitan**   4:47  
Well, let's go in details of what this release will be.  
I think you describe it quite well at the bottom there.

**Nathan Carver**   5:01  
OK.

**Val Levitan**   5:03  
Maybe we should start from the bottom so we understand what September 1st release is.

**Nathan Carver**   5:10  
Um, OK, so you're right here at this September 1 beta release.

**Val Levitan**   5:14  
Right.

**Nathan Carver**   5:15  
OK.  
Yes. So um, yeah, thank you for adding the content 'cause that helps with the clarity. Um.  
So the three machines. So these this now identifies the three specific machines that are part of this.  
The printer. So the three-game machines, the printer and the Flex POSI think the setup's pretty straightforward.

**Val Levitan**   5:45  
So let's just let's just regurgitate this again. In our Georgia facility, we will set up a test site with income. So it's a fully live site. We're emulating a location.  
And in our showroom, we will have one of our JVL machines, which is Flex S.  
We need to show IGT because it's the machine that is most prevalent in the market and we need to show a vanilla machine.  
All three machines will have Muda goose hardware fitted.  
From Mutagus, it will have a cable running to a printer, so we'll have a printer sitting on the counter. Next to the printer we will position our POS.  
If our.  
Final plastics will not arrive by then. We will 3D print plastics.  
And we will have a POS sitting on a counter with limited capabilities of the POS. We will play off a couple of games.  
Uh.  
Get a payout on the machine. Trigger a payout.  
On the counter, printer will start printing a ticket, will pick up this ticket and emulate a pairing over ticket value with a card.  
And emulate issuance of the card. That's what I want to see in general.  
On September 1st.  
Let me pause. Anybody has any concerns? Well, right away I understand the concern of plastic not being ready. That's OK. It doesn't bother me 3D.

**Juan Martinez**   8:05  
No.  
Oh, sorry. Yeah, just that we we definitely need to acquire the Mother Goose, the fledgling, and all the related hardware to make sure that we have this connection.

**Val Levitan**   8:19  
It will probably take us about two weeks to set everything up in our office.  
So I would recommend we start early setting up machines early.  
Which we probably should bring an operator with whom we work with.  
That we can borrow these machines. We don't have them in in the warehouse.  
I think we're working with United, am I correct?

**Juan Martinez**   8:54  
Yes, yes. Now in term, we're working with United. In terms of being the machine supplier, they have mostly switched to the access system. So I don't even know if they use Mother Goose in most of their locations anymore and I'll confirm that with Felipe.

**Nathan Carver**   9:11  
the right.

**Val Levitan**   9:14  
Oh, I wasn't aware that the access system was competing with Mother Goose.

**Juan Martinez**   9:19  
But yeah.

**Val Levitan**   9:23  
OK.  
Is Mutagus still prevalent?

**Juan Martinez**   9:28  
Yeah, I mean per per the Gomoa meeting, if only 300 locations out of 4000 have deployed kiosks, that means the majority of the market, you know, 90% or greater is still using Mother Goose as of four or five months ago.

**Val Levitan**   9:47  
Oh, OK. I think there is a confusion here. I'm referring to Muda Goose as the current dominating system in the market for printing tickets. Access, I understand, is already a new system that is shifting towards a card.  
Of some sort of a card.

**Juan Martinez**   10:08  
Correct. What? What I'm not clear on is if they actually co-exist inside of the same location, because if they do, they could lead to duplication. You know you've got a ticket coming out of Mother Goose, yet you've processed a transaction through the access system, so.  
We just need to sit down with the operator and clarify that point.

**Val Levitan**   10:30  
I recommend not bothering with access right now. Just focus on Mother Goose. It represents good 90% of the market.

**Juan Martinez**   10:36  
Yep.  
Yes, agreed.

**Val Levitan**   10:40  
If not, if not more and just as point of verification, you said 4000 locations, my understanding that it's over 6000 locations.

**Juan Martinez**   10:46  
Hmm.  
That you're probably right. Well, yes.

**Val Levitan**   10:52  
OK, so.  
OK, good. So we should start couple of weeks earlier. That probably will take us third week of August. We should start configuring the machines. Let's talk a little bit about the POS.

**Juan Martinez**   11:12  
OK.

**Val Levitan**   11:17  
Um.  
Mainly the question is to you, Gennady, so to.  
Get a POS to a point of.  
Oh.  
I don't know having a.  
CPU, touch screen, screen, I don't know, swipe card reader, some other features.  
Can you take me through steps of how it needs to work?

**Genadi Peari**   11:58  
We'll have all the devices this week, so I mean I believe we will choose and finalize the devices after this.  
The the the development you mean, right? So, so we need the this motherboard to be working and the working with the.  
Uh, current swipe reader in the scanner.  
And we need to do the.  
The video connections to support the monitor through this motherboard.  
What and?  
I I believe Pavel will do.  
The the the integration in the software.  
And I'm from my side. We'll do packing of all these devices. We'll we'll need to do the the stand and the the.

**Val Levitan**   13:12  
Housing.

**Genadi Peari**   13:12  
There is the lazy. Maybe we have fewer things to do right for the.

**Val Levitan**   13:18  
The housing you're referring to the housing of the of the POS.

**Genadi Peari**   13:23  
Yeah, yeah. Housing and the the stand and the lazy shoes, the the rotations thing, right. So for the September, I believe we'll do the rapid prototypes.  
2-3 pieces.  
I I believe we'll do the housing.  
By in July, mostly July it will be finished, so we'll have enough time to assemble in August.

**Val Levitan**   13:55  
OK and so.  
Will it be what did we decide? Will it be an ARM based processor?

**Genadi Peari**   14:05  
We received the yesterday evening these boards need the few days to work just to to make sure it's. Means will receive these boards I believe in a week.  
And the it.

**Val Levitan**   14:24  
But these these boards you're talking about ARM, ARM based processor. So on top of that we layer a Linux.

**Genadi Peari**   14:27  
Yes, yes, yes.

**Val Levitan**   14:36  
The operating system and who's going to be responsible for doing that? Evgeny.  
Or Pavel.

**Pavel Frolov**   14:47  
I think Eugenia will just try to use out-of-the-box software package just to install and try to probably connect a reader.  
To be sure that everything is working, but then we will integrate here in Minsk. When I say integrate, I mean adjust Linux operating system.  
To run necessary scripts on boot up and running Java application.  
Uh, run in browser.  
And to integrate everything in correct order.  
To run in to finally run browser with necessary application.

**Val Levitan**   15:48  
And this is this is on you, right?

**Pavel Frolov**   15:52  
Mijima.  
Yeah, me, Dima and graphic user interface from Igor, Grip, Core and Anton.

**Val Levitan**   16:08  
And how much time do you need after the arrival of the PCB?

**Pavel Frolov**   16:15  
To confirm that everything is work and able to release until September 1st, I think I I will meet about one week.

**Val Levitan**   16:31  
OK, so my point is that 1st of September is a realistic date for a trial.  
And we would have to coordinate this trial with income as well.  
Which seems to be a good process right now. OK, so yeah, we're we're probably good to go.  
O Let's continue.

**Genadi Peari**   17:01  
OK.

**Nathan Carver**   17:03  
All right, so for the tested features, the non MVP for September, we can reprioritize those at later dates to actually be tested. They'll probably be. They may or may not be tested indirectly.  
But we won't add them to our tested outcomes for success.

**Val Levitan**   17:24  
But what? What should we consider as a successful test on September 1st?  
In my opinion.  
We execute a payout on each of the machines. We successfully generated a ticket from Mothergoose connection.  
And we successfully redeem 123 samples of tickets of payouts and credit the wins on a credit on a MasterCard.  
Prepaid card. To me, that signifies a win. I mean a.  
Positive test.

**Juan Martinez**   18:14  
Successful test Val, one question when when just so I'm clear, when you say we print a ticket from the Mother Goose, that's the normal ticket that is produced today by Mother Goose. So we're we're intercepting the signal. There isn't a second ticket that we need to print.

**Nathan Carver**   18:16  
OK.

**Juan Martinez**   18:31  
On our side, OK, just making sure.

**Val Levitan**   18:34  
We're we're at this stage. We're not even intercepting a signal. We're just printing a ticket just like it's done today. We're manually holding the ticket in our hand. Here's a ticket. We're holding it in our hand. We're going to look at the data, what it says. Let's say the win is $100.

**Juan Martinez**   18:48  
Yep.

**Val Levitan**   18:54  
We enter $100 into the POS and we go through income pairing cycle and issue a card and verify that this card has a value of $100 \-, 298 dollars.

**Juan Martinez**   19:11  
Perfect.

**Val Levitan**   19:11  
That's that. To me, that signifies a successful test for September 1st.

**Juan Martinez**   19:19  
Yes.

**Pavel Frolov**   19:19  
I I would add something something more to this test. Actually we need to support this POS on our server. We need to be able to push active lease for this device and active parameters.  
Related to income, location, credential and so on.

**Nathan Carver**   19:48  
OK, so.

**Val Levitan**   19:49  
OK.

**Nathan Carver**   19:52  
Critical here is the site set up, pushing the cloud, pushing configuration from the cloud.  
Is operator card provisioning because of the non MVP of the authentication? Do we want this particular piece of the setup to be non MVP as well?  
Because we may or may not have a level of maturity in the authentication mechanism. It may be very basic and maybe isn't required to swipe a card yet.

**Pavel Frolov**   20:33  
So.  
I don't probably do not understand what they're saying, but if if it relates to how we need to to communicate to income to make authentication.  
To enable location or to enable current operation. Seems that we already can do this, so each location set up.  
I would say manually we need to sign all the documents, get credential settings for each location, then we can enter this data on our server.  
Then push settings to particular terminal POS and after this seems we are ready to issue a card.  
During each operation of issuing a card, we perform in some general communication message to income to get token to make pre-authorization and to activate the card. That's all.

**Nathan Carver**   21:39  
Yeah.  
OK, so to activate the gift card and then for activating.  
I'm referring to this as the operator card, which is what the cashier would swipe to activate.  
As opposed to the cashier entering a pin, do we want that particular setup? So provisioning an operator card, do we want that to be part of MVP?  
Um, or do we want to defer? It may or may not be used on September 1, so we may not have to test it necessarily.

**Val Levitan**   22:36  
When you refer to operator cart, what does it mean?

**Nathan Carver**   22:41  
So I'm the operator card would be the cashier, the manager or the admin to access the flex POS that would swipe their card.  
To authorize.

**Val Levitan**   22:51  
I suggest making it a non MVP for for for September 1st.

**Nathan Carver**   22:54  
OK.  
OK, sounds good.

**Pavel Frolov**   23:00  
Or or at least if we we have enough time until September 1st, I think it could be a pin code protection and two different roles, pin code 1, number one pin code \#2.

**Val Levitan**   23:13  
We.  
We're not rolling anything out in the market.  
On September 1st, I suggest that don't.

**Nathan Carver**   23:22  
Right.

**Val Levitan**   23:27  
Don't. Don't make your life unnecessarily difficult.

**Pavel Frolov**   23:38  
OK, clear.

**Val Levitan**   23:40  
Correct. Not exactly. Non market release, yeah.

**Nathan Carver**   23:44  
OK.  
OK, so still testing the lease and the kill switch in September 1\.

**Val Levitan**   23:59  
No.

**Nathan Carver**   24:00  
OK.  
OK. So based on this is obviously our section that we're gonna be laser focused on then. So that will help us prioritize the requirements that we get started on.

**Val Levitan**   24:12  
That's right.  
That's correct.  
So if you could bold that section, put it as MVP.

**Nathan Carver**   24:32  
OK, perfect.  
Let's see failure modes. These are just notes that I basically put in here for things we'll look at next, and we'll start shifting these around and prioritizing them for later iterations.  
Um, OK.

**Val Levitan**   24:51  
I would I I would move most of the non MVP or some of non MVP for September 1st, start moving them on to September 15th making them MV PS. So you need to reshuffle September.

**Nathan Carver**   25:05  
Correct.

**Val Levitan**   25:07  
1st and 15th and the 30th. So those are the steps we want. We want continuous integrating every two weeks and just negotiate with Pavel of what is possible.  
Between September 1st and September 30th.

**Nathan Carver**   25:29  
Correct. Sounds good.

**Val Levitan**   25:31  
But that September 30th, we want something more substantial than of course we had on September 1st.

**Nathan Carver**   25:42  
Is there so we did label the 1st as a non market is in December 15th is a market release or is did we have a market release earlier?

**Val Levitan**   25:49  
I would say, I would say it has to be the the worst case scenario market release should be November 1st and I'm talking about worst case scenario. We're really, really running late if we are behind November 1st and we don't have.

**Nathan Carver**   26:02  
OK.

**Juan Martinez**   26:03  
Yeah.

**Val Levitan**   26:09  
I'm going to say if we don't have 10 installations on November, we are behind like dramatically, dramatically.

**Nathan Carver**   26:15  
OK, do we have an ideal?

**Val Levitan**   26:20  
Hmm.

**Nathan Carver**   26:21  
Do we have an ideal market release deadline?

**Val Levitan**   26:25  
It's not gonna happen, so there's no point.  
November 1st is a is a critical day.  
I would I would put market uh release critical date.

**Nathan Carver**   26:49  
Alright.  
OK. And then we'll start shuffling around. Um.  
We will start shuffling features or requirements around within these release.  
Um, within the release cadence.  
OK.

**Val Levitan**   27:06  
But let's say Juan and I should participate in it only after you negotiate it with Pavel.

**Nathan Carver**   27:16  
OK.

**Val Levitan**   27:21  
And also I would consider certain administrative and housekeeping elements as non MVP for October for November 1st release.

**Nathan Carver**   27:38  
So non housekeeping elements on the.

**Val Levitan**   27:42  
On the contrary, administrative and housekeeping features.

**Nathan Carver**   27:45  
Mm.

**Val Levitan**   27:51  
As non MVPS.  
That will remove considerable pressure.

**Nathan Carver**   28:03  
OK.

**Val Levitan**   28:05  
I would move administrative and housekeeping features on to January 1st.

**Nathan Carver**   28:39  
OK.  
All right, so that's.

**Val Levitan**   28:45  
And and and and I'm sorry, administrative housekeeping and full Tito validation that that would be January 1st.  
Yeah.  
Full Tito validation for old and new machines.  
Would you agree with that one?

**Juan Martinez**   29:16  
Yeah, definitely.

**Val Levitan**   29:20  
Because if we don't have it by January 1st, people will doubt our capability.

**Juan Martinez**   29:25  
Agree.

**Pavel Frolov**   29:30  
Um.

**Nathan Carver**   29:30  
OK, perfect.

**Pavel Frolov**   29:32  
I I have two two questions. First of all, are we installing QR scanner on the first release of the device?

**Val Levitan**   29:48  
By by device, what do you explain the device?

**Pavel Frolov**   29:53  
Yours.

**Val Levitan**   29:55  
You are you saying that QR scan and barcode scan are different?

**Pavel Frolov**   30:01  
Your scanner and barcode scanner is the same same device.

**Val Levitan**   30:05  
Uh, yes, we are installing it, yeah.

**Pavel Frolov**   30:10  
But for first Uh execution, we do not need Uh to to be operational.

**Juan Martinez**   30:15  
But.  
Co correct.

**Val Levitan**   30:16  
No, we just need. We just need it to be fitted.

**Pavel Frolov**   30:20  
Mm-hmm. OK.

**Val Levitan**   30:23  
And we also, I think Gennari missed that point. We're contemplating that the POS may need a full insert.  
Attendant card, so somebody who's in front of our POS.  
In order to make the POS operational, may may need to have a full insert card constantly in.

**Juan Martinez**   30:51  
Sure.

**Val Levitan**   30:54  
So when you design your housing, you should have a provision for a full insert card.

**Juan Martinez**   31:03  
So this is the operator card that Nathan mentioned earlier.

**Val Levitan**   31:07  
Administrative card, yeah.

**Juan Martinez**   31:09  
Yes, we are not contemplating having both a full insert and a swipe card reader do limited space. We're just going to have one, correct?

**Val Levitan**   31:20  
No, no, we're contemplating both, yeah.

**Juan Martinez**   31:21  
We are OK.

**Genadi Peari**   31:24  
Yeah, I I wasn't aware about this.

**Nathan Carver**   31:26  
Oh.

**Val Levitan**   31:28  
No, you were not. In the conversation that we had, there is a necessity.  
Some of the cash register can only be unable to work with a fully insert card.

**Genadi Peari**   31:34  
But.

**Pavel Frolov**   31:40  
Oh.

**Genadi Peari**   31:41  
But but full insert, you mean the you mean the contactless card, right?

**Val Levitan**   31:46  
Monpecliff card, yeah.

**Pavel Frolov**   31:49  
Probably it could be like this, a smaller card with. I think it's wireless wireless data like NFC.

**Juan Martinez**   32:04  
Um, I.

**Val Levitan**   32:05  
It could be. It needs to be some sort of a chip card. It's an administrative chip card.

**Juan Martinez**   32:09  
Correct. That's what I was going to say because of the PCI compliance that income mentioned, we might as well make the POS future proof and have it capable of reading a chip in the event that that full swipe applies to future gift cards.

**Pavel Frolov**   32:31  
But this readers will be a different devices. I mean swipe and fully inserted for different purposes.

**Val Levitan**   32:42  
Yes.

**Juan Martinez**   32:49  
And is there a reason that one can't do both?  
Oh, because one, I'm sorry, one may need to remain inside at all times when the employee is doing some administrative work. Never mind understood.

**Val Levitan**   33:05  
I'm thinking that there might be a provision where a cash register, sorry, not cash register, the POS is normally in a locked mode.  
It's up, it's running, but it's locked. It gets unlocked with attendant near it because attendant may turn around, may leave, may go to some other service, and in that instant the POS should be operational.  
But locked.

**Juan Martinez**   33:37  
Right.

**Val Levitan**   33:39  
Well, there are a couple of ways to lock a POS. You could have it lock out automatically, let's say within, I don't know, X amount of minutes. That will require for an attendant either to reinsert the card or swipe a card.  
Or enter a PIN number.  
You could make it operational that way. Uh.  
None of the things seem to be practical enough or.  
Relative, relatively speaking, uncomfortable, inconvenient, unless it's some sort of a touch or insert, either RFID or some sort of a.  
Proximity sensor of any sort and a full insert card seems to be a well accepted.  
Mode of unlocking a POS system.  
The swie card, on another hand, is an action card. This is where you want to air U, let's say.  
A prepaid MasterCard with a ticket value, winning ticket value. So a swipe operation is quite appropriate.  
And that's why I look at it as two different readers.

**Juan Martinez**   35:18  
Understood.

**Val Levitan**   35:19  
If we are now talking that at some point.  
Incom may move into a full secure contactless card that would require probably a second full insert.  
Reader mind you that all of it is optional and only relevant for the point of design of the housing.  
But not really.  
Location ready at the moment.

**Juan Martinez**   36:05  
Makes sense.

**Pavel Frolov**   36:10  
So the question is, are we really ready to make this monster right now to support all the options for card readers?

**Val Levitan**   36:24  
I don't think we are ready in terms of.  
Full product design, but if we are discussing just the housing, making provisions for these readers, I don't see really an issue with it.

**Pavel Frolov**   36:56  
So this is mostly a question to.

**Juan Martinez**   37:00  
OK.

**Genadi Peari**   37:03  
Well, housing. I don't think I'm ready to discuss housing. For sure we'll do something, but like, I'm thinking we need to interfaces for all these devices better we.  
Check it now before it's too late because we might need the provision for the interfaces additional some adapters to create or.  
So we say in the 33 readers altogether the the one for the swiping it one for the contactless.  
And sorted in one optional for the income purposes.

**Val Levitan**   37:54  
Yes.  
I'm saying, I'm saying that this is a maximum configuration.

**Pavel Frolov**   38:01  
You know, just swipe card reader and the second insert card reader could utilize the same channel. Yes, the same. So we can either to install swipe reader or second.

**Genadi Peari**   38:11  
See this.  
Well.

**Pavel Frolov**   38:19  
Well, fully insert that card.  
So it would be a solution not to exceed for additional port.

**Juan Martinez**   38:32  
Sure. So I I think, so Gennady, think about that swipe reader on the right side of the POS as a snap on, snap off type unit where you could replace it with this full card reader and there'd be a separate full card reader. Is that?

**Genadi Peari**   38:47  
So swipe swipe is will be installed 100% because you always need swipe card. You always need the the issue plastic cards.

**Pavel Frolov**   39:01  
No, no, not exactly. Juan. Juan said that in future this card would be changed by in call to use cheaper card instead of magnetic card.

**Juan Martinez**   39:02  
Do we?  
Yeah.  
And we'll know this next week when we speak to income in Toronto, but that has been mentioned. Whether it happens or not, we don't know. We just want to don't, you know, we don't want to get caught off guard.

**Pavel Frolov**   39:26  
Mm.

**Genadi Peari**   39:33  
OK, we'll decide later if it will be snapping or it will be different housing. It's I think it's cheaper to make two different housings than to start is to do one part instead of doing 3 parts.

**Juan Martinez**   39:36  
Yeah.

**Genadi Peari**   39:51  
I'm not sure.

**Juan Martinez**   39:53  
OK.

**Genadi Peari**   39:54  
But yes.  
And this is our decision or it came from Deancom to to have the car to.  
The operator card.  
Enable the machine.

**Pavel Frolov**   40:14  
For now, we do not talk this, discuss this approach with income.

**Juan Martinez**   40:26  
Yeah, that's internal, Gennady.

**Genadi Peari**   40:28  
So, So what is it like pin and it's not sufficient?  
Because because if if attendant let's let's say leave the stations right. So he we freeze the screen, I mean make it not operational. When he comes back he need to activate it back anyways, right? Or he will take it.  
The cart every time with him.  
With both.

**Juan Martinez**   41:09  
Yeah, I I guess Gennady's question, if I understand correctly, is why do we need a physical operator card in lieu of a PIN number to access the admin screens?

**Genadi Peari**   41:27  
It's a more elegant or.

**Nathan Carver**   41:31  
No, I had that same question in this doc is do we need to have? Does the admin use an operator card or do we have a password set on the device?  
That would make sense to me because it's gonna be an we have a chicken or egg, right? If the admin needs a card, how does that card get provisioned if the admin's provisioning cards from the machine?

**Genadi Peari**   41:59  
Yeah, one time he will forget his card and well, what I.

**Nathan Carver**   42:04  
Yeah, yeah, just go back and get it, yeah.

**Juan Martinez**   42:08  
Yeah, I mean, from an operational perspective, certainly there's less managing and with just PIN rather than tracking and supplying employee cards because employees quit, they get fired. As he said, they forget their cards. You know, a PIN has been trusted.  
For a while, do we just feel there's an added layer of security with using a physical operator card or like what led us to the operator card concept, which I know it is in use in some devices?

**Genadi Peari**   42:44  
'Cause pin you will need anyways.  
Exactly for the purpose when attendant went to the washroom, he he he disabled the POS right when he came back, he comes back, he he activated by pin.

**Juan Martinez**   42:59  
Yes.

**Genadi Peari**   43:00  
You won't be taking card every time.

**Nathan Carver**   43:08  
So I think the clarity then is of the different roles who can use a PIN access and who must use a card access.  
So the cashiers, for example, must use a card access. Or can they also have an alternate PIN?

**Juan Martinez**   43:29  
Well, and can't the unique pin numbers have different levels of access? I E could there be a master pin versus a low level pin?

**Nathan Carver**   43:36  
Yes.  
Yes.

**Juan Martinez**   43:42  
OK then I.

**Nathan Carver**   43:43  
Yeah, yeah, I think a pin should be tied to a user or a an individual.

**Juan Martinez**   43:49  
Absolutely.

**Nathan Carver**   43:51  
Um, and it can even be controlled by the cloud as opposed to controlled by the device.

**Genadi Peari**   43:57  
But but by the way he he can use swipe card for activate the POS as well. He's master card, master swipe card.

**Nathan Carver**   44:11  
OK, so we could take the approach of a uh individual user. We'll have both a pin.  
We'll have a pin for sure and then an optional operator card or something to that effect.

**Genadi Peari**   44:22  
I think, I think operational card Valerie likes this idea. I think we should cannot do it with.

**Nathan Carver**   44:32  
OK.

**Val Levitan**   44:37  
Sorry, I removed myself from this conversation. Is there anything I should know?

**Juan Martinez**   44:42  
We're talking about the operator card and how that concept came to be versus just a standard PIN that's unique to every employee and one PIN could be full admin rights and all of the other cashiers with their own PIN numbers could just have limited access.

**Nathan Carver**   44:43  
So we're just.

**Val Levitan**   45:03  
It could be my. My point is that.

**Juan Martinez**   45:05  
OK.

**Val Levitan**   45:10  
The observations that I had with the point of sale.  
Um.  
I am. I personally observe that.  
Those that that are security conscious, they go for an ID card.  
I I think that it the the software could evolve. It's easy to evolve the software. What will be difficult is to replace the terminals.  
And the the the problem that I'm seeing here in this market is that unless the regulator gives an extension.  
Uh, past June 1st.  
And stands his grounds, which I don't see why he wouldn't.  
Each operation will have to get equipped with a minimum a POS.  
They would have to pair up the winnings.

**Juan Martinez**   46:21  
Right.

**Val Levitan**   46:25  
On June 1st, 2026\.  
And I don't know any other way to pair up a winning unless you have some sort of a.  
AOS or a mobile device or some handheld device that could.  
Interact with income.

**Pavel Frolov**   46:47  
Oh.

**Val Levitan**   46:50  
Because income is the only clearinghouse for that purpose.

**Juan Martinez**   46:54  
Right.  
Well, and I'm definitely not questioning the POS device. I mean I think that that definitely that we're in the right.

**Val Levitan**   47:01  
Well, so if June 1st is the day.  
Then.  
There will be a massive amount of devices distributed in the last day. I I don't know what to call it in the last day, last week, last month, but in the last moment there will be a lot of devices thrown out in the market and connected.

**Juan Martinez**   47:18  
Sure. Mm-hmm.  
Yes.

**Val Levitan**   47:27  
And there will be some sort of a panic.

**Juan Martinez**   47:29  
Yes.

**Val Levitan**   47:30  
So if our software has minimal capabilities.  
It's OK as long as the hardware is equipped with future proof expansion, then we can.  
Extend software capabilities.  
But if our hardware is not equipped with potential expansion slots.  
Then we will be forced to change the hardware. That will be costly.

**Pavel Frolov**   48:03  
Uh.

**Val Levitan**   48:11  
But possible.

**Juan Martinez**   48:12  
Sure.  
So that just so I understand, so a full full operator card and the the the reader to support that should be immediately available in the event a customer decides that a PIN is insufficient security for their operation.

**Nathan Carver**   48:21  
OK.

**Juan Martinez**   48:32  
And we don't have to revisit a physical hardware swap out in the field. We would just activate it via software, but that that full card operator card is present on the POS from day one.

**Val Levitan**   48:46  
Well, if it's not even a reader, but at least a cavity in the plastic that could be retrofitted, we could hypothetically send the technician and stole a reader, expand the software capability.

**Juan Martinez**   48:52  
Sure.

**Val Levitan**   49:02  
And uh, move on.

**Juan Martinez**   49:05  
OK.

**Val Levitan**   49:05  
Look, it is I I can accept the fact that we can also swap the the POS.  
I mean it's it's also a doable model. It's just it will, it will just be more expensive.

**Juan Martinez**   49:23  
Sure.

**Val Levitan**   49:25  
Because when you swap, you're pretty well committed to throwing away the cavity, you know, reformatting the hardware, repurposing the hardware of some sort, changing it.  
I mean, it's possible we can do it.

**Juan Martinez**   49:45  
But you're right, Val, where we we acknowledge that the POS becomes a single point of failure for an operation. We don't want to take it out of service that that's a, you know, we want to limit that. So having everything ready for provision from day one just makes more sense.

**Genadi Peari**   49:46  
Oh.  
Um.  
I'm sorry.

**Val Levitan**   50:05  
Sometimes provision, sometimes provision is very difficult to provide.

**Genadi Peari**   50:11  
But.

**Val Levitan**   50:12  
And maybe Gelini right now will say, but I don't know which card reader and I, you know, I need to do research on the suppliers and I don't have time for that and maybe it's more reasonable just to.  
Swap a POS at some point.  
Uh.  
Oh, I mean, yeah, I can. I can understand that too.

**Juan Martinez**   50:41  
Sure.

**Genadi Peari**   50:41  
Guys, I'm not questioning the making provisions. I like to make provisions as well. I just want to can we discuss use case? One use case, for example, attendant goes to the washroom. What does he do?  
Because heaven for me.

**Val Levitan**   50:58  
The the attendant, the attendant has on his on his uniform. He clips on a card, either a belt level or a chest level, clips a card. It's attached to an attendant.  
And it's attached with kind of a.

**Juan Martinez**   51:19  
A lanyard.

**Val Levitan**   51:21  
A what?

**Juan Martinez**   51:23  
It's called a lanyard, just like a casino player tracking card, a lanyard. It's a little elastic, springy thing that just hangs from their neck or or clips onto their shirt.

**Val Levitan**   51:27  
Yeah.  
Or a belt. And so in the normal condition, when an attendant is next to a POS, he takes this card attached to the lanyard. Is it?

**Juan Martinez**   51:38  
Well.  
Mhm.

**Val Levitan**   51:51  
And inserts it into a POS and it's fully inserted. It stays there when attendant needs to leave the the desk.  
He yanks the card out, it hangs on the lanyard attached to him and he moves around the premise.

**Genadi Peari**   52:14  
Or to believe somebody can leash the attendant. It's it's literally leasing him to the station.

**Val Levitan**   52:22  
It's it's. I'm actually surprised that you're surprised because this is actually a normal way of operating.

**Genadi Peari**   52:30  
Oh.

**Val Levitan**   52:31  
I'm actually, I'm actually surprised that you're surprised.

**Juan Martinez**   52:34  
Yeah.

**Genadi Peari**   52:35  
I'm surprised, honestly, because it's like.

**Val Levitan**   52:39  
Maybe, maybe we'll start paying attention to it, but it's it's normal way of operating. Pins are in unsecure.

**Genadi Peari**   52:49  
Because for because for me attendant goes, we have to put the screen in the freeze or I don't know, disable it and when he comes back he can swipe the card to enable or.

**Val Levitan**   53:05  
How do you how do you put the screen to disable?  
How do you disable the screen after? So time limit or you you tell the attendant when you leave disable the screen? What do you do?

**Juan Martinez**   53:10  
That.  
Correct that that would be a procedural step where it times out after 3 minutes. Or if you're going on a bathroom break, you must re-enter your pin to lock the kiosk the POS down before you leave it.

**Val Levitan**   53:33  
OK, so if if it locks out every 3 minutes, then the attendant curses at you every freaking time that they have to put their pin in every 3 minutes.

**Juan Martinez**   53:45  
Yes.

**Val Levitan**   53:48  
So then you say, no, no, no, let's make it 5 minutes. 5 minutes is also too short. Let's make it half an hour. OK, make it half an hour. So he leaves, he turns around and the POS is live.

**Juan Martinez**   54:05  
Yeah, Valvo, what you what what you just described.

**Val Levitan**   54:06  
And somebody and somebody and somebody pairs up a fake ticket.  
And validates a card.  
Sorry, sorry, Juan, I I I interrupted you.

**Juan Martinez**   54:16  
Yeah, did the.  
Oh no, no. It's it's just that what I I understand the level of security and since JVL is on the hook for the MasterCard transaction, we should be secure. But I guess most employees will take the card off their belt and leave it in there because.  
In reality, when you work at a convenience store, customer comes in, give me $5 of gas and go back there and reach for a pack of cigarettes. So I need to disconnect from the POS to do these things for lottery tickets, for cigarettes, for whatever else they want. So you know if we put our.

**Val Levitan**   54:57  
Next.

**Juan Martinez**   54:58  
Operator hat on. It's difficult to keep them locked into the O.

**Val Levitan**   55:04  
They will disconnect, correct. They will disconnect under the circumstances that it takes long for a POS to come alive. But if POS comes alive, the moment the cart is inserted, they're less relaxed.

**Juan Martinez**   55:19  
Right.

**Val Levitan**   55:24  
Them to disconnect.

**Juan Martinez**   55:25  
Yes.

**Val Levitan**   55:26  
But they will do everything to gain efficiency.  
That's why sometimes they use just a touch, like a canister, like a Dallas chip that sits on top so it's easy to attach, no insert.

**Juan Martinez**   55:42  
Yeah.  
Yeah, that that RFID kind of concept that that can get expensive.

**Val Levitan**   55:57  
But, but, but let's let's just review liability because one touched on on an important factor, liability.

**Nathan Carver**   55:57  
So we're.

**Val Levitan**   56:07  
So JVL is liable to income for collecting of the money.  
So if each machine generates in Georgia $100 per day, that means this machine pays out approximately $900 per day. Let's call it 1000 to be even.  
Six machines per location. That's $6000 in payouts. So JVL needs to collect 6000 per day in payouts and transfer it to income every single day for every single machine.

**Juan Martinez**   56:53  
And and Val, I did, I thought about that is the process we're introducing is no different for a location in principle of what they do today. Today they trust this piece of paper that comes out of a Mother Goose printer that says machine \#4, pay them $40.

**Genadi Peari**   56:55  
Oh.

**Juan Martinez**   57:13  
And then they go to the register and they get $40 or a gift card or merchandise and they pay the player and we're repeating the same step with an added level of security. So from Mike, my opinion is that if we collect $6000 a day, we build that master.  
$6000, he owes it to us. If there was a theft that's between the master and location owner and that you have some sort of procedural problem. So I think we need to look at that too, just to to reduce some of our concerns from the security side.

**Val Levitan**   57:50  
I fully agree with you, but if we do not provide basic security to to a master or to a location owner, he's just going to say I can't use it.

**Juan Martinez**   57:56  
Great.  
Yes.  
Absolutely.

**Nathan Carver**   58:06  
So we're coming up on time here. I I do have more time. I can go a little longer, but I have a hard break at about 10 or 9950 I think.

**Val Levitan**   58:06  
Are you free? You free?

**Nathan Carver**   58:20  
I think we would benefit from just a risk analysis focused meeting specifically on the on the security or the access to the device.

**Val Levitan**   58:29  
I don't know. I don't know if it requires because it seems like it the last use case that we gave hit home to Gennady. I don't know if you require more dwelling on the point.

**Nathan Carver**   58:45  
Well, I don't. I think what we would have is just a very focused discussion on identifying failure modes, for example, the cashier walking away from an active device.  
Identify all those failure modes and then we can go through and and identify what are the effects they have and how do we mitigate those effects. So it'd just be an ongoing process. It's not something we want to do in one sitting.  
We would want to do this regularly, but a living document we can go back to and I think it'd be very helpful for the engineering team because it's they're gonna have to have a lot of nonfunctional requirements to support these.  
OK, so for this I threw together this product team cadence.  
And identified Juan Pablo myself with Val is optional. I can add more people. This would just be our weekly cadence meet three times a week and how we would focus on prepping the work and ensuring that the following week the engineering team has a backlog ready to go.  
Is there anyone you want me to add or remove? I think at the very minimum it was going to be Pavel and I and so Juan I added you in, but you can certainly be optional.

**Juan Martinez**   1:00:13  
No, I definitely is. When I can attend, I certainly definitely want to.

**Nathan Carver**   1:00:16  
OK.

**Val Levitan**   1:00:18  
I think, I think Gennady at this point should be a mandatory.

**Nathan Carver**   1:00:22  
OK.  
Perfect.  
OK. So the cadence is very simple. Day one, I'm assuming Mondays, it could be any day, but day one will be we go through the requirements that we want to focus on for that week. Any final negotiation and acceptance criteria, we'll work through that and then we just prioritize the backlog.  
For the engineering team, the midweek sync will be review current progress, primarily focus on any blockers that might need to adjust priorities around and we also want to preview the next week.  
Um, so we get a sense of what we want to focus on the next week, and that's to keep, um, the day one meeting from getting too large and having too much work to go through.  
And then the day five is just the review. That can be a demo. Um, that can be whatever we agreed on. How do we accept this?

**Val Levitan**   1:01:29  
I really like the schedule.

**Juan Martinez**   1:01:31  
Mhm.

**Nathan Carver**   1:01:32  
OK, I can throw those meetings on the calendar if we have a preference Monday being day one if but we like I said we can choose any day that works better with the engineering teams current.

**Val Levitan**   1:01:37  
Yes, please.

**Nathan Carver**   1:01:46  
Current way of working.  
Um.

**Val Levitan**   1:01:53  
I think Monday, Wednesday, Friday is is good, good pattern. I strongly suggest keeping the meeting under 45 minutes.

**Juan Martinez**   1:01:57  
Yeah, yeah.

**Nathan Carver**   1:02:04  
Perfect.

**Pavel Frolov**   1:02:05  
Um, next week we will be uh.  
Only on Monday and Wednesday.  
Because of the holidays in Belarus on Fridays and I think actually on Friday we can invite Igor and probably he will present us first approach to traffic user interface for.

**Nathan Carver**   1:02:21  
The holiday? Yep.

**Pavel Frolov**   1:02:38  
Yours.

**Nathan Carver**   1:02:40  
Oh, OK, perfect. Yep. So we'll add the UX.  
For Friday.

**Pavel Frolov**   1:02:47  
Yes.  
Not for Friday, for Wednesday.

**Nathan Carver**   1:02:51  
A website. OK, perfect.

**Val Levitan**   1:02:54  
But only this Wednesday, right? Or everyday?

**Juan Martinez**   1:02:55  
Oh yeah.

**Nathan Carver**   1:03:00  
For this Wednesday.  
OK.  
Perfect.

**Val Levitan**   1:03:12  
Wednesday will be the second only for July the 2nd.

**Genadi Peari**   1:03:19  
I don't believe next Friday any from state will come to the meeting.

**Pavel Frolov**   1:03:24  
Uh, also, yes.

**Nathan Carver**   1:03:25  
Oh.  
OK. Yeah. So next week, we'll start on this on Monday and then.  
For next week, we will just either move that day five to to Thursday or do it Monday morning. We'll just tactically decide what to do.  
Um, due to the holiday.

**Juan Martinez**   1:03:53  
And I'm flying to Toronto Monday from 8:00 to 11:00, so.

**Nathan Carver**   1:03:54  
OK.

**Juan Martinez**   1:04:01  
I I will be able to be on the call.

**Nathan Carver**   1:04:04  
OK.  
All right. So based on our discussion of the September 1\.  
We will use this to prioritize to prioritize our backlog targeting the remote initial setup, specifically cloud push configurations and.  
Activating the gift card. These are our two focus, so we'll pull requirements from here.  
And so I started.  
As a.  
A way to iterate on these requirements. I've started adding them in here. The focus is very specifically to keep each one small and and focus in order to fit within a week's cadence.  
And the way I'm doing this here is they will eventually go into JIRA and that will become their source of truth, but they'll get defined here and then each one will have sub requirements. This is the approach I'm taking to keep them small so that a single requirement doesn't have.  
A full list of alternate and failure modes that the engineer has to implement. So we'll break these apart to implement them iteratively and fit within our cadence.

**Val Levitan**   1:05:31  
Very, very good.

**Nathan Carver**   1:05:34  
Yeah.

**Juan Martinez**   1:05:36  
Hopefully.

**Nathan Carver**   1:05:36  
Excellent.

**Val Levitan**   1:05:36  
This, this has been a full meeting. I think we moved forward. We're getting more aligned. I remain open for any of the questions. Otherwise, I'll see you Monday.

**Nathan Carver**   1:05:38  
OK.

**Juan Martinez**   1:05:51  
Yeah.

**Val Levitan**   1:05:51  
Thank you.

**Juan Martinez**   1:05:52  
All right. Thanks, everybody.

**Pavel Frolov**   1:05:52  
Perfect. Thank you. Bye.

**Nathan Carver**   1:05:53  
All right, good.  
Thanks all.

**Juan Martinez** stopped transcription