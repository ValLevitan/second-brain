---
tags:
  - meeting-transcript
  - project-review
  - business-side
  - val
  - juan
  - pavel
  - github
  - rgs
---

**Transcript**

July 23, 2025, 12:01PM

**Nathan Carver** started transcription

**Nathan Carver**   0:03  
So mid midweek review, anyone would like to kick off with an update or questions on on what we're doing?

**Val Levitan**   0:15  
Well, maybe it's worth your while just summarizing last week. I mean, I read through meeting notes recording briefly. I understand that the dialogue with RKS is ongoing and they're, you know, offering their support.  
But is there anything I'm missing in general?

**Nathan Carver**   0:41  
No, I think that's the long and short of it. We getting documentation on Mother Goose and the dev team exploring that and I'm on my side creating requirement documentation. That's all in GitHub.  
Um and um, Juan, I don't know if you have an update on the business side or about.

**Juan Martinez**   1:06  
No, just like you said, once once Pavel confirms exactly what we need, I'm assuming we just want one old Mother Goose and one new version of the Mother Goose just to be covered. We'll get that order placed and RKS is on standby to complete that.

**Nathan Carver**   1:07  
No.

**Juan Martinez**   1:23  
Just need to let them know exactly what we want, and I'm assuming that that is what we want. One old and one new set, Paul.

**Pavel Frolov**   1:31  
Yeah, good to know from my side to to share works at that in progress right now in there.  
Is doing modification of graphic user interface. I mean design of graphic user interface to support option of getting data from ticket.  
And to provide user interface list of all tickets with different statuses with option to redeem value related to particular ticket. Actually today in the morning he already showed.  
Yeah, uh, this mockups.  
So if if you want, probably on Friday we can make a short presentation of what is done.

**Val Levitan**   2:38  
Correct me, correct me if I'm wrong. When I left, I think I made conscientious push to emphasize the importance of creating the architecture. So when I left, on one side there was the.

**Pavel Frolov**   2:38  
Yeah.  
Definitely.

**Val Levitan**   2:57  
RKS tasks, whether or not we could get information from RKS directly or do we have to kind of reverse engineer their design?  
So that was one thing that we wanted to tackle. And the second thing was to tackle the overall architectural design, not just the POS part of it, but overall architectural design of the transactional products.

**Nathan Carver**   3:33  
Mhm.

**Val Levitan**   3:35  
So.  
I understand what has been done on the RKS side.  
I am not clear what is done on the architectural side, if anything.

**Nathan Carver**   3:50  
OK, so let me.

**Val Levitan**   3:54  
Nathan, your camera is off, at least for me.

**Nathan Carver**   3:57  
Um, yeah, it just went crazy on me. I'm trying to fix it. Um.

**Juan Martinez**   3:57  
Yeah.

**Nathan Carver**   4:04  
Um, share.  
It's OK, Nope.

**Val Levitan**   4:13  
Yeah, we see it.

**Juan Martinez**   4:14  
There we go.

**Nathan Carver**   4:14  
OK.  
Alright, there we go.  
Um, so architecture. So we have.  
Um.  
We have our model diagrams here, just giving an overall reference to the the main components in the architecture and what that looks like what I'm driving out right now and I've started a use case to help.  
To help clarify this, so I have this main use case that's going to take us through the entire journey and as I'm building this out, I'm tagging the requirements that are going to be part of implementing that and what this is leading to is if we go into these.  
Individual flows this primary flow.  
This is showing us how the components are going to communicate and where they are in that journey of that use case. So I have a couple of main.  
So these are kind of the beginning of the ticket redemption flow, but I believe it's yeah. So this is our main flow, this gift card processing flows and what this is starting to do is show us the communication points.  
Between the components and this will help us define the API and determine how both Flex POS and JVL Control Server will maintain internal state and how they'll manage communications. So if you come into gift card processing, this kind of be your launch board to other parts of how the system will work.

**Val Levitan**   5:48  
OK.  
Right. Let me interrupt you at this moment. I don't think we want to dedicate this meeting to reviewing the architecture, but I personally, I don't know who wants to be in this meeting, but I personally want to have a deep dive into the overall architecture.  
And for that reason, I want to be a part of a dedicated meeting for reviewing the architecture. I think everybody in this in this meeting that are here right now should be in this meeting.

**Nathan Carver**   6:11  
OK.

**Val Levitan**   6:27  
But if anybody feels that they don't need it, then it's OK.

**Juan Martinez**   6:33  
No, I I agree. We need it.

**Nathan Carver**   6:34  
OK.

**Val Levitan**   6:35  
So with that in mind, I would like to have a I need approximately 2 hours to dive into architecture.

**Nathan Carver**   6:45  
OK.

**Val Levitan**   6:45  
So can we schedule a meeting please? And and and by the way, how much time do you need to move it to a point where we we can discuss the architecture? Maybe, I don't know.

**Nathan Carver**   6:49  
Yeah, I can put that on the calendar.

**Val Levitan**   7:02  
506070% ready.

**Nathan Carver**   7:05  
OK, let's let's plan for.  
Let me look at the calendar. It's planned for, I would say Monday, but I think Monday morning is busy for me. How about Tuesday morning?

**Val Levitan**   7:14  
Yes.  
The 29th.

**Nathan Carver**   7:23  
Yeah, the 29th.

**Val Levitan**   7:25  
Yeah, what time?

**Nathan Carver**   7:27  
8:00 is good for me. We want to keep this.  
But the morning's open.

**Val Levitan**   7:37  
So 8 to 10\.

**Nathan Carver**   7:38  
Yep, 8 to 10 is good.

**Val Levitan**   7:40  
OK, that's good. Can you please? Should I or you send them again?

**Nathan Carver**   7:43  
I'll I'll actually put that on the board and I'll just invite everyone here as and you know self select out if it's not needed.  
OK, sounds good.

**Val Levitan**   8:03  
OK, great. So the review is clear to me. We can now focus on the agenda of this meeting.

**Nathan Carver**   8:11  
OK, so the agenda is so updates. Juan, Pavel, Ian, I think you were giving your updates. Did you have anything more?

**Pavel Frolov**   8:21  
I have, I have. Yeah, I have more more ideas. Just just common information mostly for Val. We managed to make dump of several types of tickets from Mutabus.  
And I decided to make, let's say, Multagus emulator for development purposes that will produce necessary tickets for our developers.  
Actually it's quite quite easy with artificial intelligence and I think take probably half a day to finish this this work.

**Val Levitan**   9:06  
Sorry, not clear, Pavel. I think you're trying to say that you will be going through certain spikes for a proof of concept.

**Pavel Frolov**   9:17  
Yes.  
Yes, yes, definitely.

**Val Levitan**   9:20  
Which spikes? What exactly are you trying to prove? What concept?

**Pavel Frolov**   9:26  
The concept when we connect in parallel to existing a printer between motor goose and printer take this.

**Val Levitan**   9:37  
In parallel, in parallel, or we wedge our we wedge ourselves in between both the goose and the printer.

**Pavel Frolov**   9:44  
In in parallel.  
We do not need any additional hardware, we will use just serial port on our hardware. Connect one cable.

**Val Levitan**   9:49  
So you.

**Pavel Frolov**   10:00  
These two signals ground and data from a mutagons. We will make we will take or dump of all printed tickets, processes data and create events in our system.  
Power up events, ticket printed events, last 25 vouchers, events, daily statistic and bookkeeping statistic. Everything we will.

**Val Levitan**   10:23  
It's OK.

**Pavel Frolov**   10:35  
Dump and store in our POS device.

**Val Levitan**   10:42  
But just to be clear, our architectural goal is not to keep any information on POS. We want it to be captured and to be outside of human touch. Am I correct on this?  
From an architectural perspective, I mean, as far as the spike is concerned, that's a different story. I assume that if we can capture something and keep on POS, we could probably just as conveniently move it outside of the location.  
Or is our or is our goal to keep things on the POS?

**Pavel Frolov**   11:14  
Oh.  
Well, actually I need to clarify some some thoughts about this. Actually we.

**Val Levitan**   11:28  
OK.

**Pavel Frolov**   11:33  
When you say about architecture, you mean entire architecture. It's also for Nathan to understand. Entire architecture means that we have lots of different devices and we can set up location.  
Using different devices in one network that can communicate to each other.

**Val Levitan**   11:56  
That that is exactly right. As a matter of fact, when I talk about the architecture, I specifically say architecture of the transactional devices. So this array of POS port server.  
Uh, Redemption Center Tower.  
The the the collection of the of the products that are new for JVLI gave them a name of transactional devices.

**Pavel Frolov**   12:26  
Mhm.

**Val Levitan**   12:32  
So.  
We could go, we could offer a solution as primitive as a POS only, or as an array of various devices working in parallel or in conjunction with one another.  
And this architecture could be as concise and narrow and compressed or as elaborate as well. You have a multiple set of multiple devices on locations, multiple POS, multiple.  
Redemption centers multiple.  
And on and on and on, and they all seamlessly connect to one another right now for the sake of rolling out.

**Pavel Frolov**   13:17  
Yes.

**Val Levitan**   13:30  
Devices on time and on schedule. We prioritized the POS.  
But it's still it has to be thought of as a group of transactional devices that we will continue rolling out not only in Georgia core market, but throughout the markets in the US and possibly elsewhere.  
As a matter of fact, my ambitions now are looking at the current casino.  
Uh, market.  
Where?  
The ATM's on the casino floors might be minimized.  
And might even come close to a slot machine or adjacent to a slot machine, just like at some point 30 years ago or 40 years ago, people talked about bill acceptors in the side mount boxes.  
And then eventually they migrated into slot machines. So now I'm saying, well, maybe there is a sidebound to an ATM next to a slot machine, specifically saying to an ATM ATM.  
Specifically next to a slot machine.  
I don't know whether it's possible legislatively or not, in all markets or not. Maybe some Native American gaming markets, maybe none at all. I don't know. But as far as thinking about transactional products, JVL transactional products.  
I do not set the limit of transactional products in Georgia only. I'm seeing it now in.  
Georgia, Nebraska and Texas at a very minimum.  
And just for the group to understand, Texas is not a state. Texas is a country.  
So just to be clear, no matter how high your ambitions are, you feel.  
Have a market in Texas. You're good.  
Financially and spiritually, and you have a good stake as well. That was a joke for artificial intelligence, not to weave it into the market to a transcript. OK, but moving on.

**Juan Martinez**   15:44  
Yeah.

**Pavel Frolov**   15:53  
So so my next my next sentence will be we have different direction that we can go either to create a full architecture, discuss everything how it can be built between each other.

**Val Levitan**   15:54  
Yes.

**Pavel Frolov**   16:08  
And then start coding and the second direction to to understand that the minimal possible solution can be said either via our flex.  
Port plus POS either to install just only Flex POS device and nothing else.

**Val Levitan**   16:33  
I would like to respond to exactly what you're saying. So to me, number one importance is the overall architectural solution as \#1. So that's an MV MVP of MV PS.  
And then narrow down to a very primitive solution. What if a customer wants only POS? Are we saying that we are comfortable in keeping data on the POS? Is this a minimum viable product for us?  
Or does it mean that if a customer wants a POS, it cannot come by itself? It will still include a cloud server of some sort?  
And hence full circle back 360 degrees back to discussing total architecture and why certain architectural solutions versus other architectural solutions as an example.

**Pavel Frolov**   17:27  
Mhm.

**Val Levitan**   17:39  
There is a grave concern of cheating and we don't want any data sitting on a local device, whether it's true or not, whether it could be protected, cannot be protected. I'm not an engineer. I don't understand the complexity of moving data into a cloud. I don't know what's involved.

**Pavel Frolov**   17:42  
Uh.

**Val Levitan**   17:59  
I don't know cost involved, but I can tell you that I would lose lose my sleep at night by knowing that we are processing hundreds of thousands of dollars.  
And there is a possible easy way of cheating.  
Uh, intentional or unintentional?  
So if this is a number one concern for all of us and we're saying whoa, whoa, whoa, whoa, whoa, hold on a second. We're all concerned with this. Cheating is our number one thing here and.  
As we all realize that.  
A location attendant is not our ally in this solution.  
Then what is the architectural solution for a minimum viable product?

**Pavel Frolov**   19:02  
Mhm.

**Val Levitan**   19:05  
So again, full circle emphasis made on providing architectural solution for the transactional products company wide, then narrowing it down to.  
the MVPs in terms of  
Roducts and in terms of architecture.  
And and capabilities and features.

**Pavel Frolov**   19:30  
Yeah, no, just just we'll add some some other notes that in case when we.  
Uh, discuss architecture.  
We can split for example POS development into two stages, first stage for example until September 1st to present something for customer.  
Just using local redemption server within the OS device and the next step.  
Keeping in mind that we are doing in parallel because I understand that it's impossible to do it in one month, but to redo all the transactions related to income to cloud and it it could be a MVP.  
Stage stage two, for example until October, something like this.

**Val Levitan**   20:39  
Or maybe stage one should be an actor.

**Pavel Frolov**   20:43  
Yeah, probably.

**Val Levitan**   20:47  
So again, let's get to architectural solution, architectural design.

**Nathan Carver**   20:51  
Mhm.

**Val Levitan**   20:54  
Thinking about that counterfeit and fraud is \#1 concern, not the not the technology, but protecting ourselves against counterfeit and fraud is a priority \#1.  
And then all functional things need to flow from there.

**Pavel Frolov**   21:13  
No.

**Val Levitan**   21:14  
And and that may depend you, you may come back and say, Val, the month of October is unrealistic for MV PS for for stage one. It needs to be five years from now and we're going to make decisions accordingly.

**Pavel Frolov**   21:34  
Mm-hmm. Yeah.

**Nathan Carver**   21:34  
OK, so for our Tuesday meeting then, what we want to focus on then is the overall architecture, how all the components would work together with a focus on security and fraud detection and prevention.

**Val Levitan**   21:49  
Yeah, go ahead. Carry on.

**Nathan Carver**   21:51  
OK.

**Juan Martinez**   21:56  
And so I mean based on what we discussed, Nathan, I I think I'd like to suggest that we take our currently scheduled Friday iteration meeting and change that into the technical maybe just you, myself and Pavel Gennati if you.  
If you want to join as well, just to shift the architectural pre layout call to go over that. So we're ready for Tuesday.

**Nathan Carver**   22:17  
Yeah.  
Yes, I agree. I've been focused very in the details of flex POS, so it'll help me step out and then we can align on Friday if we're gonna have the, you know, the 50% mark that Val wants to discuss on Tuesday and if we need a little more time, we can.  
Yeah, a few more days.

**Pavel Frolov**   22:46  
Um.

**Juan Martinez**   22:49  
Perfect.

**Nathan Carver**   22:50  
OK, that works for me. We'll repurpose Friday.  
Anything else to review for today?

**Juan Martinez**   23:03  
I didn't have anything else.

**Pavel Frolov**   23:06  
Me too.

**Nathan Carver**   23:07  
All right, Kunani.

**Val Levitan**   23:11  
Oh.

**Genadi Peari**   23:14  
The the that Pavel mentioned right now that we connect the printer in parallel to the POS. This is very important point for me. Is it the right thing to do to make it parallel or?  
Not to allow parallel connection.  
Just to go straight to POS.  
And then we can.

**Juan Martinez**   23:46  
Well.

**Genadi Peari**   23:47  
Make the signals. Well, we can cannot do too much, but.  
But at least I mean the same idea like flick sport works.

**Pavel Frolov**   24:01  
In case when we connect in parallel, doesn't matter where where it's implemented inside of our box or outside. If our device is power in power off mode, then Multagoose plus printer will continue working.

**Val Levitan**   24:20  
So, so I have a.  
I have a thing about it.  
And that's why I asked your question whether it should be in parallel or we should be wedged in between.  
I personally need to think about it. Maybe somebody has a more definitive statement on this subject, but I feel that if RPOS not, if RPOS is not working.

**Juan Martinez**   24:41  
Yeah, I have a concern with fraud.

**Val Levitan**   24:48  
It should cut everything off, so we should take a central stage of validating, transferring money, etcetera. So if POS goes out of service.  
You know.  
That's the end of things which.

**Genadi Peari**   25:04  
This can be additional point of security like.

**Val Levitan**   25:09  
Which brings me to a point in our architectural solution. What happens if the if a device goes out of service? We touched briefly with Gennady yesterday in the meeting.  
I believe that our devices should not be.  
Uh, fixable. They should be replaceable.  
So send the replacement. So then from an architectural standpoint of view, what happens if a replacement device arrives on a location and it needs to be configured? Well, we can't afford sitting on the phone with each of the locations and taking them through steps.  
So the replacement, the configuration, the transfer of settings, etcetera, that cannot be manual.  
So from an architectural solution, where do you keep this critical data? I don't know how you call it from a technology perspective, your Mac addresses, your device IDs or something else. So I yank one thing out of the.  
Circuit. I stick another device as a replacement. How does it find itself? What happens next? So you turn the the only thing that a customer does, it turns the power switch on. The device says oh.  
Where am I?

**Juan Martinez**   26:48  
I mean what?

**Val Levitan**   26:48  
And some and something needs to take care of the setting. Don't worry, you're here. Here's a new setting.  
And all and all and all.

**Juan Martinez**   26:58  
I mean Val, what you just described is almost a the POS needs to be a hot swappable device. That also means though that the key settings for the POS because I at some point in time we talked about a mini server not too dissimilar from the Tito server that could retain.  
All of the local settings and that is less likely to fail than a POS device that's being manhandled on a daily basis. So if we do have a server to that would allow the reconnection of a new POS, I think that that's something we need.  
To consider.

**Val Levitan**   27:41  
So that brings me back to the subject of Pavel thinking. Should it be in parallel or should it be wedged in between? What happens if the PO and do we agree with this scenario and if the POS is in between, we got to, we got to do.

**Juan Martinez**   27:41  
Whether it's good.  
I have a concern.

**Val Levitan**   28:00  
A little bit of market stall searching. What happens if POS is in the center of everything? And I mean theoretically it could create, could create certain.  
Inconveniences will the market, will the market.

**Pavel Frolov**   28:17  
Yeah, it it it really depends. It really depends on schematic how flex POS is working. Is it connected to Mutagus? What is actually a central part of location right now?  
Or it will be a different approach without Mutagus, but with our redemption center.

**Nathan Carver**   28:43  
Mhm.  
There's gonna be use cases where if if a location has just flex POS and for some reason we lock them out because of fraud detection or suspicious pay, they still have to be able to print their tickets if they're gonna have an alternative to that. So either.  
I think the parallel solution makes sense for that those types of use cases.

**Val Levitan**   29:08  
Yeah.  
Or do we build the POS with?  
Devices that never break.

**Nathan Carver**   29:37  
Yeah, I think in a sense, if if the Flex POS intercepts and we lock them out of redeeming a gift card, if they still want to give store credit, they can access the tickets on the Flex POS in the same way they would a printed ticket.  
And we would just need the Flex POS active in the sense it can still record tickets, store them locally.  
But due to the lockout, it wouldn't have any ability to send anything to the JVL control server.  
Or perhaps I think we still, I think we have options there. It'll just to be it'll. I think the use cases will be.  
How does the how does the location access their ticket if we blocked out their Flex POS due to no payment or fraud detection?  
Makes sense.  
Makes sense.

**Juan Martinez**   30:52  
Yeah.

**Val Levitan**   30:52  
The operator may say look as long as you provide me with the with a reliable POS and an easier replacement and configuration, then I'm willing to do that because it it improves my operation it.  
Creates some more accountability for me.  
And maybe an operator is starving for this. I I don't know.

**Nathan Carver**   31:21  
Mhm.

**Genadi Peari**   31:23  
So basically operator doesn't need a ticket.

**Val Levitan**   31:28  
Not, not anymore.

**Genadi Peari**   31:31  
Yeah, and that makes sense.  
Unless we want to create ability to POS to print the ticket.

**Pavel Frolov**   31:44  
Actually right now move the goose in case when no printer connected will produce a sound and will go out of service.

**Genadi Peari**   31:45  
So.

**Val Levitan**   31:58  
Well, if Muda Goose goes out of service, does it take all of the machines out of service?  
Or just one machine out of service.

**Genadi Peari**   32:12  
All of them.

**Juan Martinez**   32:17  
Yeah, you you end up it.

**Pavel Frolov**   32:17  
I I I don't think, I I don't think so. Actually merchant will continue working, but they will not be able to produce a cashout.  
Oh, reduce cash out, but is.  
Uh.

**Val Levitan**   32:42  
Delete the ticket printer.

**Pavel Frolov**   32:44  
Delay it. Yeah, it was the way it's ticket print.

**Juan Martinez**   32:48  
Yeah, but that that also then means that the location turns into manual mode. If the player cashes out, I want to leave right now the the the printer malfunctioned. Maybe they just been paying them on the honor system. You know, I walk over the machine, I I look at the history. OK, yeah, you cashed out $20.

**Nathan Carver**   32:53  
Mm.

**Juan Martinez**   33:07  
Here's your your lottery tickets worth $20.00 or whatever they give them and and or a $20.00 gift card and then they walk out.

**Val Levitan**   33:22  
Look, I don't know how much Muda goose.  
The the the central board and the our reiteration of the Smith boards cost an operator, but there could be a play here for JBL where we give away our Smith boards.  
And they connect.  
Easily, quickly, seamlessly to a POS and that becomes the MVP.  
For a location.  
There is no operator in the world that I have ever met that would reject a free problem.  
So with a subscription of POS, you give them away the Smith boards.  
If the Smith boards are easily connected in the machine, it may take off.  
Maybe not, I don't know.

**Juan Martinez**   34:30  
Yeah, yeah, we need to think about that cause the the least amount of work for the operator is to not even have to open the machine. You know, if we're intercepting Mother Goose, nobody has to touch the machine, you just connect.  
Ahead of the printer and away you go. Now with the Smith boards, every single machine has to be opened and we need to connect to 1015 different manufacturers setups and it's a little bit more complicated for us in the beginning to map that Smith functionality out.  
times that many different machines versus just leaving everything status quo.

**Val Levitan**   35:11  
100%.  
Just keep in mind that SMIP board the difficulty of mapping it out is only for the machines with single with a single SAS port.

**Juan Martinez**   35:30  
Sass here.

**Val Levitan**   35:32  
In case of a dual SAS port, there is no complexity of mapping out SNIP because it connects to standard SAS port and the other end is connected to.

**Juan Martinez**   35:37  
Right.

**Val Levitan**   35:47  
To our POS so.

**Juan Martinez**   35:50  
Understood.

**Val Levitan**   35:50  
It's a really minimal effort and right now for every machine that they install in a location they're paying, I don't know, but probably double digit.

**Juan Martinez**   35:53  
Yep.

**Val Levitan**   36:03  
Number of dollars per machine just to install.  
The equivalent of a Smith board.

**Juan Martinez**   36:15  
I believe the easy links is $600.

**Val Levitan**   36:20  
Well, there you go versus free.  
So we know that approximately the market is good for approximately 2000 machines per year. So 2000 machines times 600, that's $1.2 million being spent on Smith board.  
And with our solution it could be free.  
Yeah.

**Pavel Frolov**   36:55  
I have one more question probably let let's assume that location is using Mutogus and our Flex POS seem it seems that probably for cashier is more interesting to.

**Val Levitan**   37:01  
Oh.

**Pavel Frolov**   37:13  
Uh, a regime, uh, in goods that he he sell.  
So probably he will keen on out of service for our POS in this case.  
And mainly to redeem to winnings from the player to goods.

**Juan Martinez**   37:41  
No, but remember the law says on on June 1st of next year, all winnings have to go to the gift cards.

**Pavel Frolov**   37:49  
OK.  
If this is a rule, then cashier will be interested in quick service and replacement of POS.  
So probably Nathan, you can write the additional requirement to monitor online all our POS devices. If they lose a connection to Internet, do not report connection.  
Then probably we need to understand that probably this location is out of.

**Nathan Carver**   38:48  
Correct. We'll need, Yep, monitoring of the locations, connection information, and then a way to escalate if the connection is down for, you know, what is it? Minutes, whatever we need.

**Val Levitan**   39:05  
So are we saying that a PO there has to be an ongoing ping between the POS and the cloud server and if that ping is lost?

**Nathan Carver**   39:05  
Yeah, I think that's a good use case.

**Pavel Frolov**   39:17  
Yes.

**Val Levitan**   39:21  
Then POS enters auto reset auto recovery.

**Nathan Carver**   39:26  
Mhm.

**Val Levitan**   39:28  
Is this what we're saying? Just want to make sure that it's standard.

**Pavel Frolov**   39:30  
Not this is not about recovery, but this is more about reporting to somebody. So probably we have a problem on location.

**Val Levitan**   39:41  
But maybe we should initiate a self recovery first before reporting.

**Pavel Frolov**   39:48  
Recovery of what if?

**Val Levitan**   39:49  
Of the of the POL.

**Juan Martinez**   39:50  
Like a POS reboot as an example.

**Nathan Carver**   39:51  
Right.

**Pavel Frolov**   39:56  
Um.

**Nathan Carver**   39:57  
Well, we may not know what the issue is. If it's just a connectivity issue, Flex POS could be fine. It just goes dark from the JVL perspective.

**Pavel Frolov**   40:02  
Yeah.  
So this is a this is just this is just a feature of cloud server to report about possible issues.

**Val Levitan**   40:17  
I would wait with reporting I would allow.  
A POS to self recover, reconnect and if it cannot then I would report.

**Nathan Carver**   40:30  
Yes, and from the JVL side, it would be if that recovery cycle, let's say it takes less than 5 minutes. If this control server loses contact for the Flex POS for longer than 5 minutes, then we assume it can't recover at that point.

**Juan Martinez**   40:46  
Right.

**Val Levitan**   40:47  
Alright, nothing.

**Nathan Carver**   40:48  
And whatever the threshold is, if it's 2 minutes, whatever the.

**Val Levitan**   40:54  
That's exactly what I'm saying. Yeah, correct. Agree.

**Nathan Carver**   41:05  
OK, we're coming up on time. Anything else we want to kind of discuss in the last few minutes?

**Pavel Frolov**   41:15  
OK.

**Nathan Carver**   41:16  
OK, so the action is we're going to repurpose Friday's meeting with a focus on architectural discussion. It'll be Juan, Pavel and Gennady optional if you want to join and and the the goal of Friday will be to prep for the Tuesday conversation and make sure.  
Sure that we're going in the right direction to be ready for that.

**Val Levitan**   41:38  
Well, I'm sorry. If it's an architectural meeting, I believe Gennady must join.

**Nathan Carver**   41:44  
OK.

**Val Levitan**   41:45  
And Gennady, I understand that you like to take Fridays off.

**Genadi Peari**   41:51  
Yeah, that's fine. This right there. No worries.

**Val Levitan**   41:55  
OK, so are we saying that we are repurposing Friday's meeting to discuss the architecture?

**Nathan Carver**   42:03  
Yes, we want to focus on the this, the additional scope of the entire architectural transactional architecture.

**Juan Martinez**   42:14  
It's brainstorming before we get to Tuesday.

**Val Levitan**   42:15  
OK.  
OK, OK.  
OK, then that's it for me.

**Nathan Carver**   42:27  
Alright.

**Val Levitan**   42:29  
Thank you everyone. Bye-bye.

**Nathan Carver**   42:30  
Thanks everyone.

**Juan Martinez**   42:30  
Thanks, everybody. Bye.

**Pavel Frolov**   42:31  
Thank you. Bye.

**Val Levitan**   42:32  
OK.

**Nathan Carver** stopped transcription