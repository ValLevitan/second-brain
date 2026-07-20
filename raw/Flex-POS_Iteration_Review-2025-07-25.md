---
tags:
  - meeting
  - architecture-overview
  - transactional-architecture
  - val
  - juan
  - flex-pay
  - flex-port
  - planning
---

**Transcript**

July 25, 2025, 12:01PM

**Nathan Carver** started transcription

**Val Levitan**   0:03  
For the meeting, so we know what the objectives are, so we can try to achieve our objectives and then let's quickly go through the meeting in a in an intense pace.

   0:07  
Yes.

**Nathan Carver**   0:16  
Right.

**Val Levitan**   0:16  
I like pressure in the conversation. I don't like relaxed conversations.

**Nathan Carver**   0:20  
Ha.  
OK, we'll put put the, we'll turn on the pressure cooker. So we repurposed today to focus on the transactional architecture overview, make sure that we understand all the devices.

**Val Levitan**   0:26  
OK.

**Nathan Carver**   0:37  
That we want in that architecture and specifically so we can round out and the architecture structure by Tuesday for another conversation and ideally we have.  
50 to 60% of it fleshed out on the first iteration for Tuesday.

**Val Levitan**   0:59  
And just to make sure that we understand the impact of the architecture in parallel, Pavel is trying to further adapt this architecture for all other transactional devices. So the importance of.  
Nailing the overall architecture is extremely important for us.

**Nathan Carver**   1:19  
OK.  
All right, so the devices as they are now, the the overall impact of the architecture and then the future integration of devices.  
OK.  
All right, so let's start with the devices. So these are all in JBL. They're all returned referred to as a flex, right? So flex tower, flex port, flex pay. These are the devices we're focusing on.

**Juan Martinez**   1:54  
Yes.

**Val Levitan**   1:55  
Flex Flex is kind of um.  
I don't know. I don't know how to call it. Stage name, branding name.

**Nathan Carver**   2:04  
Yes.

**Val Levitan**   2:07  
It represents a time and history of our evolution of thinking about the product, so it's more of a branding thing.  
The the second part of it is more of a designation of a product of how it will be used, and we're trying to use a singular word for describing its main purpose, as in, for example, Smith.

**Nathan Carver**   2:34  
Mhm.

**Val Levitan**   2:35  
Or Tau or POS or port. All of it has a meaning behind it in how it will be utilized. As an example, POS point of sale self-explanatory.

**Nathan Carver**   2:51  
Mhm.

**Val Levitan**   2:54  
Tower.  
Self-explanatory. Well, not really self-explanatory, but when you explain what it does, I mean it's the the name I think fits the purpose. So yeah, just explaining the naming convention.

**Nathan Carver**   3:10  
OK, yeah, that makes sense to me.  
OK, so in an overview, let's run through the Flex devices as they are now. So the Flex tower.  
I'm pulling this stuff from.  
The the JBL confluence.  
Is that the good source of truth for us to define this?

**Val Levitan**   3:34  
Yeah, it's not a bad source of truth.

**Juan Martinez**   3:35  
Yeah.

**Nathan Carver**   3:41  
So let's.

**Juan Martinez**   3:42  
Nathan, would you be all right if we started with the POS device since we sort of prioritize that one as the?

**Nathan Carver**   3:46  
Yeah.  
Yeah, let's do that.  
All right, how would you like to do this? We can just take notes.

**Juan Martinez**   3:59  
I for my own sake, I I just sketched out very basic. I would just like to you know, rattle off to the team, you know how we plan to do XYZ and then obviously we're recording the transactions if that works for everybody.

**Nathan Carver**   4:00  
You're confident.  
Yeah.

**Juan Martinez**   4:19  
Share my screen.  
All right, so starting with the Flex POS at the center here, we know we have our machines. These machines contain a board called the fledgling, which is a Daisy chain from machine to machine.

**Nathan Carver**   4:38  
Mhm.

**Juan Martinez**   4:41  
They end at the Mother Goose and the Mother Goose connects today to a printer. We are going to interject the POS device in between Mother Goose and printer and capture that data.  
From the Mother Goose as a a way to circumvent the manual entry of the gift card creation the way it's actually done today. You know, we we look to eliminate that fraud possibility by going to automated.  
During this week's conversation, you know, we said, hey, Flex POS should be a I'm going to use the word hot swappable device, meaning if it breaks, it just should be instantly replaceable.

**Nathan Carver**   5:21  
No.

**Juan Martinez**   5:30  
By the location and or operator. So with that, how do we envision you know and I put JVLDB server. Nathan, what were you calling it? The control server? Is that the word you used?

**Nathan Carver**   5:48  
Yes, we started calling it the control server.

**Juan Martinez**   5:52  
I'll edit that here, so.  
Oops.

**Nathan Carver**   6:02  
We may want Flex or if it if it tends, if it ends up like being a a server or curator, all the flex ecosystem, maybe Flex server is a a name you could go to. But as of right now, yeah, full server has been the title.

**Juan Martinez**   6:03  
Um, my question. Go ahead.  
Sure.  
Sure, so um.

**Val Levitan**   6:23  
I I also think that in in our last discussion we moved away from paralleling flex POS to move the goose and printer, but rather cut in between the printer and move the goose.  
So in this scenario this would be connected somewhere here.

**Pavel Frolov**   6:48  
Prentice speaking, I do not remember that we agreed on this.

**Juan Martinez**   6:50  
No.

**Val Levitan**   6:52  
No, we did not. We did not agree, but.

**Pavel Frolov**   6:54  
OK.

**Val Levitan**   6:58  
Um.  
I think if we want to bring it up for discussion, then we should probably illustrate it that way.

**Pavel Frolov**   7:00  
At least.  
Yeah.  
Yeah, at least we need to to understand pros and cons for each solution.

**Nathan Carver**   7:10  
Yeah.

**Juan Martinez**   7:13  
So can we just quickly define what we mean by intercepting the straightforward serial communication from Mother Goose versus parallel? Does parallel mean that both the POS and the printer remain functional devices? Is that what we mean by parallel?

**Nathan Carver**   7:18  
Mhm.

**Pavel Frolov**   7:20  
The.

**Nathan Carver**   7:31  
Yes, it would mean they would both get the signal. Ideally they both get the print signal at the same time, and so if one's down, the other still receives the signal.

**Pavel Frolov**   7:31  
Yes.

**Juan Martinez**   7:32  
Yeah.  
OK. So I mean based on that obviously the the pros are we don't, you know it, we don't have a single point of failure. If the POS were to malfunction, the location could do.

**Nathan Carver**   7:43  
Mm.

**Juan Martinez**   7:57  
Manual gift cards the way they do today, by manually entering the amounts from the Mother Goose, the printer and processing it that way. The obvious the con and and it could be a big con is.  
This allows for duplication of a gift card and fraud, and that would be at our expense.

**Val Levitan**   8:25  
Well, no, I don't see it allowing for duplication. I don't see how.  
Uh.

**Juan Martinez**   8:33  
Um, remembers.

**Nathan Carver**   8:34  
So we would we would track the ticket information. Um.

**Val Levitan**   8:37  
There's also there's also what needs to be connected here is the tower for dispense.

**Juan Martinez**   8:44  
Well, yeah, well, yeah, we're gonna. There's there should be a drawing for every single scenario, Val. So in this scenario I've only represented there's only a POS at this setup. Then there'll be a different drawing with POS and tower or flex pay and POS. There's there should be one.  
Drawing for every possible scenario, just so we're clear on what components. I mean, does everybody agree with that?

**Val Levitan**   9:11  
As a matter of fact, as we, yeah, I agree with that statement, but what was running through my head is actually even a further departure from this particular structure is by eliminating printer.

**Juan Martinez**   9:25  
Mhm.

**Val Levitan**   9:30  
No printer, no printer.

**Juan Martinez**   9:31  
OK.  
Sure. So that that is certainly from a fraud that's the that's a very good secure move removing the printer.

**Val Levitan**   9:43  
Not only from the fraud, but just changing people's minds, people's behavior.

**Juan Martinez**   9:50  
Yeah.

**Val Levitan**   9:53  
It seems like Pavel is.  
Thinking about a different solution, why don't we give them the word?  
Word.

**Pavel Frolov**   10:05  
Um.  
Actually actually here it could be 3 different different ways, parallel connection printer plus flex POS, printer connected to flex POS and the third.  
Without printer, in case when the printer is not directly connected to the goose, we will need to fully support printer communication.

**Nathan Carver**   10:31  
Yes.  
Yes.  
Mm.

**Pavel Frolov**   10:42  
Commands from and Flex POS. So for should look look looks like a printer report.

**Nathan Carver**   10:48  
Yes.

**Pavel Frolov**   10:59  
Answers to some commands and so on. In case of parallel connection, we do not need to support fully all printer commands, we just listening everything that related to tickets and that's all.  
It's rather more simpler to implement.

**Juan Martinez**   11:22  
And and Pavel, just just so I understand, connecting the printer on the output of Flex POS, what what is the purpose behind that? What what do you see as an advantage to doing that?

**Pavel Frolov**   11:38  
I don't know. Probably some location needs this tickets for historical data. Probably they take all the tickets right now. I don't know.

**Juan Martinez**   11:53  
Sure, but so why would we just not leave it the printer connected the way it is today and we're just intercepting the signal? I say that because if you also have to connect a printer to the POS, it becomes less and less easily hot swappable.

**Nathan Carver**   11:55  
Yeah.  
Mm.  
Thanks.

**Juan Martinez**   12:10  
You know the device that they have today that packs is Wi-Fi connected to nothing. It just needs power and and a Wi-Fi connection. Now we're we're introducing a more complicated POS that is Ethernet connected and may also require the printer connection. I don't know the skill set.  
Of a 711 employee to do any of this easily and that that's sort of where I'm going.

**Pavel Frolov**   12:40  
Do you see me?

**Juan Martinez**   12:40  
And no right or wrong here, I'm just throwing out the we add a layer of complication by having them have to connect additional components to Flexpay.  
I need the was a third solution, Pavel.

**Pavel Frolov**   13:03  
Um.  
Actually when I uh said uh said uh sort solution when the printer connected to.

**Nathan Carver**   13:07  
Yes.

**Pavel Frolov**   13:15  
POS or I I don't remember what what was the sort of solution or without printer at all.

**Val Levitan**   13:23  
Can you? In the meantime, can you copy this and create a just a parallel board so we can we can redraw it?

**Nathan Carver**   13:32  
Yeah.

**Juan Martinez**   13:33  
Yeah.

**Genadi Peari**   13:37  
I also not clear how what does it mean intercept signal? There are there are two ways to do it. For example, you come to the POS with the wire, right? And let's say.  
If POS doesn't exist, it doesn't work. I mean no power.  
Right. And the the other way is you you plug it in, you read the signals, you convert them and pass them through. So the the full the fully blown.  
An interception.  
I'm not sure we need it.

**Nathan Carver**   14:19  
Look.

**Genadi Peari**   14:22  
In in this case, if even POS out of service, if if the if it's just sneezing the signals and passing them through, even POS doesn't work, it still will be functional.

**Nathan Carver**   14:23  
Yeah.

**Val Levitan**   14:48  
I suggest in this picture remove this.

**Nathan Carver**   14:49  
Yes.

**Juan Martinez**   15:01  
Put it off to the side for.

**Val Levitan**   15:07  
Remove this.

**Juan Martinez**   15:09  
Well, that that that's one of my questions is where is do where do we?

**Val Levitan**   15:12  
Yeah, let me, yeah, let me, yeah, let me, let me, let me take you there.

**Juan Martinez**   15:17  
OK.

**Val Levitan**   15:18  
Take take this line, put it here.  
And take this line, put it here.

**Juan Martinez**   15:33  
The income line.

**Val Levitan**   15:34  
Yeah.  
I suggest this solution for many reasons. Well, this should be bidirectional.

**Juan Martinez**   15:48  
OK, I'll I'll change that.

**Val Levitan**   15:52  
Doesn't matter. We we understand.  
I suggest this topography. This is the for me is the best solution.  
I can defend it. I can defend it.

**Juan Martinez**   16:02  
Yes.  
So this this means that the JVL control server can house the data of what makes Flex POSPOS and make it hot swappable. I think that that's why I do agree with you Val that if we do have a physical server.  
Can swap out POS because the server contains the POS settings that are unique to this location and we can therefore make it hot swappable.  
Babel, you were going to say something.

**Pavel Frolov**   16:37  
Yes, I I see here difficulty without printer at all.

**Nathan Carver**   16:48  
Yes.

**Pavel Frolov**   16:51  
It requires a serial connection to printer that's not only RX and the X line, but two additional lines. So this is more than simple.  
Uh, serial connection. It's more difficult.

**Nathan Carver**   17:11  
OK.

**Juan Martinez**   17:12  
Are you saying that Mother Goose will basically tilt if it does not detect the printer?

**Pavel Frolov**   17:12  
Uh.

**Nathan Carver**   17:15  
Thanks.

**Pavel Frolov**   17:16  
Yes, yes, yes. Even if we connect just receive and transmit transmit lines, it will not detect printer. It requires two additional lines.

**Nathan Carver**   17:20  
Good.  
Oops.

**Juan Martinez**   17:24  
Mm.

**Nathan Carver**   17:26  
Good.

**Val Levitan**   17:29  
OK. But yes, I don't understand the technical difficulty in it, but on a scale of one to 10, like how much of A difficulty is it? It doesn't really seem like an unsurmountable.

**Nathan Carver**   17:31  
Hmm.

**Val Levitan**   17:48  
You should.

**Juan Martinez**   17:48  
You mean to to mimic the printer presence, Val?

**Val Levitan**   17:53  
Yes.

**Pavel Frolov**   18:00  
So highly likely in this solution, we will not be able to use some boards like boards that we have right now because correct ginas me if I wrong, but probably all of the.

**Nathan Carver**   18:03  
Yes.

**Pavel Frolov**   18:16  
Serial ports already existed on this motherboard, just simple serial lines.

**Nathan Carver**   18:17  
Yes.

**Genadi Peari**   18:26  
Sir, I don't understand you. What? What? What boards?

**Nathan Carver**   18:31  
And the mother?

**Pavel Frolov**   18:40  
So.

**Genadi Peari**   18:40  
No, we we we just need the full blown serial connection. That's it. The the serial port. Yeah, I don't. I don't.

**Nathan Carver**   18:42  
No.

**Pavel Frolov**   18:48  
Do we really have full comport on this board? I'm not sure.

**Genadi Peari**   18:51  
Yeah, yeah, yes, yes. You you need two lines, indicator and the.

**Nathan Carver**   18:53  
Oh, up.

**Pavel Frolov**   18:57  
Not not two lines. Once, one more. We need 4 lines.

**Genadi Peari**   18:59  
No, two extra, two extra. Yeah, reading the ring indicator and the.

**Pavel Frolov**   19:03  
OK.

**Juan Martinez**   19:06  
Guys, just to clarify, are we talking about the Mother Goose board or the new ARM board?

**Pavel Frolov**   19:11  
New one.

**Genadi Peari**   19:11  
Onboard.

**Juan Martinez**   19:13  
OK.

**Pavel Frolov**   19:14  
I see all connections with four connectors.  
So it will be power, ground, transmit and receive. I don't know where you see full or probably I am not aware.

**Val Levitan**   19:32  
But again, this this is such a small hurdle to overcome. It's not like it's not an issue really.  
I am sure that there are other arm boards that probably will offer full serial port.

**Pavel Frolov**   19:49  
Yeah, in case when we produce our own board, this is absolutely not a problem.  
Yeah.  
Yeah.

**Val Levitan**   20:06  
Oh.  
Yeah, I I don't see it as a big solution. When we talk about architecture, we cannot bind ourselves into.  
A local obstacle. We're talking about architecture. I suggest that this is probably a better solution, better architecture.  
Because the way to sell it to a location as you say, look, unplug your printer and plug your plug our POS and you don't have to worry about anything.  
It's a very, very easy sell. Neither the location nor the operator really understand this. And then I could further sell to an operator and say, and by the way, what I could do here is to give you an app.  
That will tell you in real time everything that's going on in the POS.  
And then I could further say, hey, by the way.  
When you install new machines, not that you have to cannibalize your locations, but when you install new machines, you know what? Sweet deal.  
You don't need fledgling and you don't need mother goose.

**Nathan Carver**   21:28  
So.

**Val Levitan**   21:29  
And the operator says, Oh my God, and how much would it cost me? And I'm going to say with three-year contract, nothing.  
So that gives me a lot of advantages in.  
Getting my my feet into my my feet into locations.  
Or getting the foot in the door.  
Do you want me to elaborate on anything?

**Pavel Frolov**   22:07  
Just one question about initial installation. For example, we are trying to enter some location according to the schematic on the screen. Are we going to sell Flex POS?

**Nathan Carver**   22:19  
OK.

**Pavel Frolov**   22:26  
Or we we also will provide some plan for for working with operator but free of charge for additional devices like tower and pay.

**Val Levitan**   22:33  
Yes.  
Or.  
I I first of all, I'm a little bit confused about your question.  
But second of all, I don't have all the pricing options in front of me right now. But in general, the way this business operates, operators don't have cash.  
Operators by nature are not wealthy people. It's it's a mature, marginal business. So if they have to retrofit 35,000 machines or six and a half thousand locations.

**Pavel Frolov**   23:21  
Um.

**Val Levitan**   23:25  
I don't see them dishing out cash.  
So I guess what I'm saying is that everything that JVL will provide needs to be provided at some sort of a payment plan.

**Nathan Carver**   23:38  
OK.

**Juan Martinez**   23:42  
Just a question though, Pavel, what? What does the purchase model have to do with the architecture? I just want to make sure I'm not. I'm not missing something.

**Val Levitan**   23:49  
Yeah, yeah. And that was my also question.  
So let's let's continue sketch \#2. Can you please copy paste this again? Create another, save this and create another copy paste please.  
I'm trying to push the meeting through.

**Pavel Frolov**   24:17  
Probably it's better to place all the schematics in one document, but side side by side. And Juan, could you please share a link to this document?

**Val Levitan**   24:26  
Sure.

**Juan Martinez**   24:31  
I'm currently doing it in my own copy of Visio. I was assuming we would move it over into whatever. I'll move it into our OneDrive Visio when when we're done.

**Pavel Frolov**   24:36  
Oh.  
Oh, OK.

**Val Levitan**   24:43  
I I really don't want Visio or any other tools. I really don't want to adopt any other tools. Let's let's use Confluence tool and let's use GitHub for storage.

**Nathan Carver**   24:49  
Yeah.  
OK.  
OK.

**Pavel Frolov**   24:55  
Yeah, in conference, I think we can use boards.

**Nathan Carver**   24:58  
Yeah, we can use the whiteboard, correct?

**Pavel Frolov**   25:01  
Like white whiteboards.

**Val Levitan**   25:10  
And GitHub I know that is very friendly with.  
mermaid diagrams.

**Juan Martinez**   25:18  
So this is the new one. Uh.

**Val Levitan**   25:21  
OK, so so great. Then let's add a tower to it.

**Juan Martinez**   25:27  
Oh well, I I I do already have a tower version.

**Val Levitan**   25:33  
Well.  
It's it's easier for me to work off the logic that you know I already have.

**Juan Martinez**   25:40  
Sure.

**Val Levitan**   25:45  
OK, so the tower.  
I don't know why am I here?

**Juan Martinez**   25:59  
OK.

**Val Levitan**   26:04  
So the tower is here.  
If you could move the stacks down and bring the tower here.  
Thank you.  
And can you make it a different shape if possible?

**Juan Martinez**   26:24  
Oh, wow.

**Val Levitan**   26:29  
Oh.

**Juan Martinez**   26:29  
Is that fine?

**Val Levitan**   26:32  
I was going to use a cylinder of some sort, but you know, it's not my show.  
Yeah, perfect.  
So connected here.

**Juan Martinez**   26:50  
Connected to Flex POS.

**Val Levitan**   26:51  
Yeah, that's your dispensing tower.

**Juan Martinez**   26:56  
Yep.

**Val Levitan**   27:01  
Maybe connected here.

**Pavel Frolov**   27:11  
I suggest to add the router between Flex POS tower and Gmail control server.

**Val Levitan**   27:24  
Yeah, sure.

**Nathan Carver**   27:27  
Yep.

**Juan Martinez**   27:28  
Yeah.

**Pavel Frolov**   27:29  
Because they use this common network.  
Hello.

**Nathan Carver**   27:34  
This.

**Val Levitan**   27:34  
Yeah.  
OK, you'll do it later. Doesn't matter.

**Juan Martinez**   27:43  
Yeah. And what was that, Pavel?

**Pavel Frolov**   27:44  
Yeah.  
Router.

**Val Levitan**   27:47  
So so so cut in here and put a router.  
If you could move this apart, slightly apart.  
Yeah.  
You got to cut these lines.

**Pavel Frolov**   28:19  
In just a note, in case of single device, for example if only Flex POS installed on the location instead of router, it could be 3G or LTE modem.

**Nathan Carver**   28:35  
Right.

**Val Levitan**   28:45  
So that means we have to have a dedicated Internet line. I don't know if location will will want that. In the past we had difficulty with that.

**Pavel Frolov**   28:56  
Again, in this case it could be a rotor with LTE option.

**Juan Martinez**   29:12  
I believe cellular is definitely a little more expensive than Internet these days.  
And I'll move the router where it belongs later, a little rusty with Visio.

**Val Levitan**   29:30  
I I actually maybe to avoid the router, I would connect tower directly to the POS because it's just a dispensing device, there's no brain in it.

**Pavel Frolov**   29:31  
Hmm.

**Val Levitan**   29:46  
The tower has no brain. The tower says, you know, dispense a card.

**Pavel Frolov**   29:48  
Hmm.

**Val Levitan**   29:56  
And we can save $100 on the router.

**Pavel Frolov**   29:57  
Mm.  
Yeah, actually we can utilize serial port for example for communication between power and UOS, but.  
6\.

**Val Levitan**   30:10  
Yeah.

**Pavel Frolov**   30:11  
POS must be a master of all the network network devices.

**Juan Martinez**   30:19  
Well, that.  
The the master, but isn't all of the networking function contained within this control server?

**Val Levitan**   30:27  
Yeah, but this is a cloud. This is a control. This is a cloud control.

**Pavel Frolov**   30:28  
Oh.  
Actually when we previously discussed the tower, it was an option that on location we install only tower that can work in depth independently and in this case it require also network.

**Nathan Carver**   30:34  
Yeah.  
Yeah.  
Yes, if the tower was at.

**Val Levitan**   30:52  
We moved we we we changed the definition of a tower. We initially initially went with a tower concept. We then said a tower concept does not work for our environment.

**Pavel Frolov**   30:57  
Mhm.

**Val Levitan**   31:08  
We need a we need to rename it. We need to call it a countertop dispenser, countertop card dispenser.  
And a redemption center. So the tower branched out into two things, and the tower concept died. So tower died, dead, canceled, but it gave birth to two concepts.

**Pavel Frolov**   31:25  
Hmm.

**Val Levitan**   31:38  
To to concert.  
First one is countertop card dispensing unit.  
And the second one is either mini ATM or a redemption center. I have not nailed the name yet, so please kill the router.

**Nathan Carver**   32:01  
Oh.

**Pavel Frolov**   32:06  
Hmm.

**Val Levitan**   32:08  
And try to connect, try to expressly connect these lines separately so they look separated and rename it into a cloud server.

**Nathan Carver**   32:09  
OK.  
So this is what would come the kiosk that we were discussing the redemption center.

**Val Levitan**   32:37  
This is not a redemption center. This is a countertop card dispensing unit.

**Nathan Carver**   32:44  
OK, so the redemption center is another concept that came out of this on A and it's a now a new individual independent device or its own.

**Juan Martinez**   32:44  
I'm.

**Val Levitan**   32:54  
The concept, the concept of a tower was killed.

**Nathan Carver**   32:59  
Correct.

**Val Levitan**   33:00  
So please rename it into.  
Countertop card dispensing device.

**Pavel Frolov**   33:13  
Well, we still have two options to redeem money to card either manually by swiping card on Flex POS or reading card during dispensing.  
On the card dispenser unit.

**Val Levitan**   33:33  
We are building the card dispensing unit with the capability of magnetic swipe reader, but.  
I practically don't believe that we will ever use the swiping, the magnetic swipe swiper. I just don't want to bind myself without it because I'm afraid, but I don't see.  
The use for magnetic cards for swiper. It's not a good thing. We should dispense the card without a touch of a an attendant.  
Can I please ask you to?  
Here can I please ask you to bring this line over here specifically so it it just.

**Pavel Frolov**   34:27  
Because it either net line or probably LTE line but counter.

**Val Levitan**   34:31  
Yes.  
And can you please rename it into a cloud JVL Cloud Control Server?

**Pavel Frolov**   34:55  
I still think that having a magnetic swipe reader on Flex POS will give us more flexibility, for example if.

**Val Levitan**   35:05  
We are putting it there, but we are putting it there. But again, just for expansion purposes, I would not even make it into an MVP right now.  
So from a hardware perspective, we're designing it with a magnetic swipe reader. Both the countertop card dispensing device and the POS will have.  
The magnetic swipe reader, but simply so we do not get stuck.  
In an expansion and even that I'm questioning, I'm I'm questioning the need of it. And as we narrow the architecture, we can resolve this. But right now, let's just leave it there for now.

**Juan Martinez**   35:52  
And and guys, just to clarify, in this scenario where we have these two devices, this means the location must have both types of cards, the loose cards that go into the dispenser and the prepackaged gift cards that get scanned by the POS device.

**Val Levitan**   36:12  
No, under this scenario I am only suggesting.  
Having the the hardware equipped with the possibility of swiping just because we are making, we are making the molds, we're we're committing, we're committing tools and we're committing to hardware and that's the only reason why I'm putting the swiper.

**Pavel Frolov**   36:29  
Picture.

**Val Levitan**   36:42  
But in in this scenario, the location is intended to operate in fully automated mode where an attendant does not touch a card. So Muda Goose generates a win. Flex POS emulates the printer instead of generating a ticket.  
There is a button, it says issue a card.  
When when an attendant says OK issue a card, it gets automatically dispensed from the countertop card dispensing device.

**Juan Martinez**   37:22  
Um, OK.

**Val Levitan**   37:22  
The attendant. The attendant never touches the card.

**Juan Martinez**   37:28  
OK, so just.

**Val Levitan**   37:29  
The the countertop card dispensing device faces the customer but sits in the cage.

**Pavel Frolov**   37:39  
So for for Gennady, I think countertop car dispenser device is just regular dispenser packaged in a plastic cover and nothing else, no.

**Juan Martinez**   37:41  
I had that.

**Nathan Carver**   37:42  
Yes.

**Pavel Frolov**   37:55  
Display no, no any processor.

**Val Levitan**   37:56  
Display.  
Display. Display. You have to have display because before you I'll explain. Before you dispense a card to a player, there is a disclaimer that a player must say I agree.

**Pavel Frolov**   38:01  
Why?

**Juan Martinez**   38:14  
Yes, basically.

**Pavel Frolov**   38:16  
It can be done on a Flex POS screen.

**Nathan Carver**   38:18  
Yeah.

**Juan Martinez**   38:19  
Yeah, that was going to be one of my questions.

**Val Levitan**   38:21  
We we are putting it in both on the POS. We're also making POS 180 degree rotating. So yes, you're right, but.  
Again, not knowing exactly which what choice will be more convenient for the location, we're still putting a display on the countertop card dispensing device.  
A touch screen display.

**Nathan Carver**   38:53  
It.

**Genadi Peari**   38:54  
And the scanner.

**Val Levitan**   38:55  
And the scanner, yeah.  
So we're slightly over designing it from a hardware perspective, slightly looking forward.  
So the countertop dispensing device will have a screen with touch screen, will have the optical scanner, and we'll have a card dispensing unit built into a plastic.  
Case.  
It will be smaller than initially anticipated the size of a tower. By smaller I'm saying a little bit lower profile.

**Nathan Carver**   39:31  
Yes.

**Val Levitan**   39:40  
And it will house only 170 cards maximum.  
The cards, the cards will be refilled in batches, and I'm hoping that we could get batches of 150 cards.

**Juan Martinez**   39:50  
And and.

**Nathan Carver**   40:00  
So with the scanner and the display, the countertop dispenser can operate independent of a flex POS in the future.  
Or will it always be connected to a flex POS in?  
In.

**Val Levitan**   40:16  
Um, good question.  
Good question.

**Nathan Carver**   40:27  
Because I think what Paul is seeing is redundancy.

**Val Levitan**   40:27  
Oh.

**Pavel Frolov**   40:28  
Without without free experience it it becomes mini ATM.

**Val Levitan**   40:38  
Why then the ATM the the whole? Uh.  
Punctuation. The whole emphasis of the ATM is dispensing of bills, of currency, of money. That's in essence what ATM stands for.

**Pavel Frolov**   40:54  
Am I?

**Juan Martinez**   40:56  
Right.

**Val Levitan**   41:02  
I I think it translates into a automated teller machine.

**Juan Martinez**   41:06  
Yes.

**Nathan Carver**   41:07  
Mhm.

**Val Levitan**   41:09  
So instead of a teller or somebody who counts money for you, it dispenses automatically.

**Juan Martinez**   41:16  
And in this scenario, Paul, that the countertop dispensing device is is basically a dumb device. It just gets its IP address from this network. It doesn't need any other settings.  
Again, just trying to see if we have a POS failure and it gets replaced, does that in any way impact the dispenser unit?

**Pavel Frolov**   41:42  
Yeah, it it can be replaced, but only if it has connection via Ethernet. But as you remember 10 minutes ago we change it.

**Nathan Carver**   41:45  
Yeah.  
Yes.

**Pavel Frolov**   41:59  
Connection line to serial line. In this case it's.

**Nathan Carver**   42:03  
Yes.

**Genadi Peari**   42:03  
Why? Why? Why we change it? You can we can put.

**Val Levitan**   42:04  
Why? No, no, no. Which? No, we we truly changed it. We changed it. But my question why it cannot? Why can't POS be replaced? And like I I don't understand the dedication of a serial port. So what?

**Pavel Frolov**   42:23  
No, my my thought correct one. If I wrong, the original question was are we able to use this type of countertop card dispenser device without pure?

**Val Levitan**   42:24  
And what?

**Pavel Frolov**   42:43  
Who is?

**Val Levitan**   42:44  
No.

**Juan Martinez**   42:45  
No, no, no, just.

**Val Levitan**   42:45  
He's he's saying can I replace a POS? If POS broke down, can I replace a POS? The the answer is quite trivial. You should be able to replace it. I mean it's only a serial device that's connected to it.

**Pavel Frolov**   42:46  
No.  
Oh.

**Juan Martinez**   43:00  
Yeah, the the question is, is the dispenser hot swappable or does it also need to retain some unique settings? I'm sure the answer is that it doesn't, so that when when we reconnect it to a POS and serial connection is established, we're good to go.

**Nathan Carver**   43:23  
Yeah, so the fraud prevention should be in the Flex POS and secured communication to the control server. So even if someone were to take control of the dispensing device and dispense gift cards, it wouldn't be JBLS.  
Account that's being hit, they would have to do it from something else or the cards would be useless without the Flex POS actually activating the card with income or through JBL control server with income.

**Val Levitan**   43:52  
It's it's not even that Flex POS validates the cards.

**Nathan Carver**   43:56  
Correct income.

**Val Levitan**   43:57  
The the Flex POS sends back and forth commands to JVL Cloud Control server that directs POS on what needs to be done.

**Nathan Carver**   44:06  
Correct.

**Val Levitan**   44:11  
And it's conditional upon getting the validation confirmation from income payment gateway.

**Nathan Carver**   44:32  
OK.  
Does this give us enough of an idea of how countertop dispensing is going to integrate with Flex POS? Do we want to break it down further or move into the next components?

**Val Levitan**   44:43  
OK.

**Pavel Frolov**   44:46  
I still I still have some uncertainties here about about design because if counter top card dispensing device more clever device with its own display and with.

**Genadi Peari**   44:46  
Alright.

**Nathan Carver**   44:47  
But.

**Pavel Frolov**   45:05  
So scanner.  
So if you want to scan some tickets, for example, and produce or to redeem value from this ticket to money, we need.  
Communication better than serial port, I think like Ethernet.

**Genadi Peari**   45:28  
Yeah, yeah, it has to be Internet.

**Nathan Carver**   45:30  
Mhm.

**Genadi Peari**   45:32  
And the and the POS needs to be equipped with switch or second just Internet.

**Val Levitan**   45:33  
But.  
Oh, I see what you're saying. So it's not that we need to.  
Put a router in there, but we just have to connect it through an Ethernet port.  
Is this what you're saying?

**Pavel Frolov**   45:58  
Not exactly.  
Um.

**Juan Martinez**   46:05  
But but that does answer your question though, Pavel. If this if all of these devices were just networked together, then we don't have a problem.

**Pavel Frolov**   46:12  
Yes, yes, this is the answer.

**Val Levitan**   46:15  
Yes, but but but I don't want to put a router because it's $100 investment.

**Juan Martinez**   46:16  
Yeah, that.

**Nathan Carver**   46:23  
Well, it should be connected to their existing network, right? So we shouldn't need.

**Juan Martinez**   46:24  
Yeah, but I.  
There there is no existing network that this over here is all serial communication. There is there is no network switch on property that we in in all the models we had discussed we certainly had a.

**Nathan Carver**   46:32  
Oh, I see.

**Juan Martinez**   46:42  
A network to interconnect these devices.  
Unless we want to contemplate Wi-Fi.

**Val Levitan**   46:53  
No, I don't.

**Genadi Peari**   47:05  
2\.

**Juan Martinez**   47:19  
Can can the POS disarm board connect act as a network hub or router?  
Where the end the yes.

**Pavel Frolov**   47:31  
Next POS.

**Nathan Carver**   47:35  
Yes.

**Pavel Frolov**   47:36  
In case if it has two Ethernet ports.

**Nathan Carver**   47:39  
Yeah, correct.

**Genadi Peari**   47:42  
It doesn't.

**Juan Martinez**   47:45  
It does not.  
You said Gennady. It does not.

**Genadi Peari**   47:50  
But but I think we can anyways we'll do interface board. Probably we can put a switch or something.

**Nathan Carver**   47:51  
No.

**Val Levitan**   48:05  
In the beginning.  
This is a dumb setup. This is a dumb.  
Uh, Brainless setup.  
As locations progress.  
They may decide to switch to our Smith board. They may decide to install local server. They may decide to.  
Put additional devices into the location, so there has to be a way to evolve from a dumb.  
Setup like this to a more sophisticated setup where we replace fledgling with our smib.  
Where we get rid of the mother goose and we'll put a local server. Why don't we draw it up in here?  
Just if you copy paste this, let's evolve this into further architecture.

**Juan Martinez**   49:17  
Second.

**Val Levitan**   49:36  
So we're now talking about, OK, location has tried our equipment that's working. They're coming back to us and and they say, look, I'm evolving, I want something more sophisticated.

**Genadi Peari**   50:25  
Yes.

**Pavel Frolov**   50:25  
US.

**Val Levitan**   50:25  
Well, I would like to, I would like to show instead of just flex port, I would like to show one flex port and one SMIP.

**Juan Martinez**   50:35  
OK.  
So here we're gonna just make this.

**Nathan Carver**   50:43  
Oops.

**Juan Martinez**   50:56  
The goose goes away.

**Val Levitan**   51:00  
You need to put a router in there.  
You need to a local local JVL server.  
So now we're operating Tito.

**Juan Martinez**   51:41  
Right.  
We need a.  
We're just going to call this an Ethernet network.

**Val Levitan**   52:10  
Well, if there is a router, that means there is an internal network.  
It should bring the router towards the between the flex POS and the cloud.

**Juan Martinez**   52:36  
It sits here.

**Val Levitan**   52:37  
Yeah.  
You get rid of the Internet network. Don't need it. It's.

**Juan Martinez**   52:49  
But Val, where are we showing to anybody who asks how does Flexport connect to anything in this scenario?

**Val Levitan**   52:57  
It needs to connect to the router.  
So router router represents a network, so snib and flex port is connected to the router.

**Juan Martinez**   53:08  
OK.

**Pavel Frolov**   53:19  
One one idea here for Gennady.  
Can we use Smith board to support power on Ethernet?

**Nathan Carver**   53:25  
Um.

**Val Levitan**   53:27  
Mhm.  
You have to cut the lines between the machines.

**Juan Martinez**   53:36  
Yeah.

**Val Levitan**   53:38  
Each machine now is connected to the router.

**Juan Martinez**   53:51  
Now.  
This scenario.

**Val Levitan**   53:54  
Flex POS is also connected to the router.  
You got to cut the lines between the cloud.  
Yeah.  
Yeah.  
And I'll.  
You need a local server in there too.

**Juan Martinez**   54:27  
Yeah.  
And the local server, same thing just connected to the router as well.

**Val Levitan**   54:32  
Yeah, but just bring it higher, bring, bring it in between the router and the the cloud. Move the cloud out. Yeah, yeah, correct.  
Router connected to the local.  
And the.

**Juan Martinez**   55:08  
And the cloud server connects to the router as well.

**Val Levitan**   55:12  
Yeah.  
And and the countertop card dispenser. Move it. Move the countertop card dispenser between the machines specifically.  
And make multiple.  
So don't connect it to Flex POS.  
Actually, we don't need Flex POS.  
Remove Flex POS.  
And put multiple countertop card dispensers next to each machine.  
And connect it to the router.  
Huge qualifier here. Huge, huge disclaimer. I am not an engineer.  
I'm simply trying to push the meeting forward and create less philosophy and more action.  
So if I'm making a mistake in something, please jump in and kill it.

**Nathan Carver**   56:48  
Yeah, I think the value here, Val, is us getting the ideas out of your head, how you're thinking about it and then engineering side can we can go in and.  
And harden the design.

**Val Levitan**   57:09  
You know, let's just do something else. Can you please create two more machines?  
I just want to show a little bit more busier location please.  
Another flex port and another snip.  
Huh.  
Can you please label port where you placing the port single sauce 1 sauce?

**Juan Martinez**   57:39  
OK.

**Val Levitan**   57:40  
And the SMIB to SAS. I just want it to be obvious.  
Maybe it is obvious already, but just maybe an extra step will help.  
And by the way, I don't mean to use you as a as a draftsman.

**Juan Martinez**   58:04  
No problem.  
It's just reminding me how rusty I am with Vizio. Um.

**Val Levitan**   58:10  
Mhm.

**Juan Martinez**   58:12  
Second.  
It's the other way around, actually.

**Val Levitan**   58:32  
No, no, no, no, you're correct. You're correct.  
Yeah.

**Juan Martinez**   58:47  
Let's see.

**Val Levitan**   59:05  
So this is a Tito configuration.  
And so now these countertop tower countertop dispensing units are smarter. This is where a player scans their own ticket and get their own cards.  
No more POS.

**Juan Martinez**   59:41  
And the reason you added to Val is just because of convenience.

**Val Levitan**   59:47  
Yeah, I want to show that I'm putting it in front of the machine, next to the machine, sitting conveniently next to the machine. You you you got your ticket, you scan it, you got your card and self self-sustained location.

**Juan Martinez**   59:52  
OK.  
Sure. And in this scenario, we may or may not mount these dispensers to the pedestal device, correct?

**Val Levitan**   1:00:11  
Correct.

**Juan Martinez**   1:00:31  
Sure.  
Sure.

**Val Levitan**   1:00:42  
And so if you could copy paste this, let's evolve it into a redemption center or a mini ATM machine.

**Juan Martinez**   1:02:02  
OK.  
Are we saying that in this scenario we have a bill recycler in between machines?

**Nathan Carver**   1:02:56  
OK.  
Yes.

**Val Levitan**   1:03:03  
Yes, well, let's call it, let's call it mini ATM. I want to emphasize this. So this again, may I please request control?

**Juan Martinez**   1:03:14  
Yeah.

**Val Levitan**   1:03:17  
So please change these shapes specifically to something radically different. Let's put a, I don't know, a hexagon or a triangle, anything that has not been used before.

**Nathan Carver**   1:03:28  
The.

**Juan Martinez**   1:03:28  
Yeah.

**Val Levitan**   1:03:32  
OK, so let's call it mini ATM.  
OK, place place it between each of the two machines.

**Juan Martinez**   1:03:46  
Hey.

**Val Levitan**   1:03:55  
So one here and one here.  
And you gotta kill these.

**Juan Martinez**   1:04:32  
Yep.

**Val Levitan**   1:04:57  
Connect both of them to the router.  
Same as these two machines, all of it has to be connected to the router.

**Nathan Carver**   1:05:05  
Yes.

**Juan Martinez**   1:05:16  
Same Val, which one? I'm sorry.

**Val Levitan**   1:05:19  
All of the machines have to be connected to the router and these two devices have to be connected to the router.

**Juan Martinez**   1:05:24  
Yeah.

**Val Levitan**   1:05:28  
They communicate through WSS protocol again.  
Disclaimer, not an engineer.

**Juan Martinez**   1:05:40  
Clean U these lines later.

**Val Levitan**   1:06:09  
So I would call this Tito plus.  
ATM.

**Juan Martinez**   1:06:34  
Um.  
We may want to rethink ATM Val. I I say that because if a location has a true ATM machine, they may perceive that we're trying to get into the revenue stream of an ATM and it's associated transaction fees. So we just need to think about that.

**Nathan Carver**   1:06:37  
Yeah.

**Juan Martinez**   1:06:54  
Uh.  
If we're going to use that name for the customer.

**Val Levitan**   1:07:00  
Well, I specifically call it mini ATM. So we understand that there is cash dispensing. I'm not trying to, I'm not trying to give it a marketing name right now.

**Juan Martinez**   1:07:06  
Yes, yes.  
No, no, understood.

**Val Levitan**   1:07:19  
So here's the solution where some of the machines are old.

**Nathan Carver**   1:07:22  
Yeah.

**Val Levitan**   1:07:24  
And they have single SAS port and this is where we install our flex port.  
Those machines that have dual SAS port, we install SMIB.  
We remove, specifically remove.  
A bill acceptor and a printer from each of the machines.  
And we equip each of the machines with an optical sensor only.

**Nathan Carver**   1:07:58  
OK.

**Juan Martinez**   1:08:18  
So just to confirm, an optical sensor, meaning a scanner.

**Nathan Carver**   1:08:22  
Mhm.

**Val Levitan**   1:08:24  
Yes.

**Juan Martinez**   1:08:26  
OK, so then so the SMIB from yesterday was a fully internal device. Now we have a flex port light panel added back onto these machines.  
Right. I mean, we need a metal plate where to mount this scanner to. The machine may or may not have that.

**Val Levitan**   1:08:49  
Well, actually, now that you're saying this, maybe Smith is no longer going to work and maybe we'll have to put flex port because we also need to communicate with the player.

**Juan Martinez**   1:09:02  
Yes.  
To or.

**Val Levitan**   1:09:12  
Please appreciate. Appreciate the fact that I'm thinking on my feet. I didn't have. I didn't have the luxury of sitting and thinking about all the intricacies of every single device.

**Juan Martinez**   1:09:17  
Oh, no, absolutely.

**Nathan Carver**   1:09:18  
Mhm.

**Val Levitan**   1:09:29  
So it is possible that I'm not seeing certain scope gaps. Maybe there are holes in my thinking something is incomplete. By all means, you know, come in and.  
You know.  
Critique each each of the solutions possible, but I'm not seeing something.

**Nathan Carver**   1:09:51  
Yeah.

**Juan Martinez**   1:09:51  
Sure, sure. Gennady, on on that note, the dimensions of the SMIB versus the hardware mounted to the back of the flex port, is it identical?  
Um.

**Val Levitan**   1:10:07  
Snip Snip is a tiny tiny single digit dollar wise board under $10. It is tiny. It's a tiny board and a port is roughly.

**Juan Martinez**   1:10:14  
OK.  
So then.

**Val Levitan**   1:10:23  
It's a a port is a three-layer cake that is approximately the same size as a 5 inch monitor.

**Juan Martinez**   1:10:39  
So I guess the question is do we, and I've got to walk through the scenarios too, not doing it on the fly here, but is there a new Flexport S which is a flex port with a display, the optical and a SMIB like board that's lower cost?  
Or we kind of keep a physical SMID and then just add a screen and optical card reader. And if so, that's more hardware because something has to drive that screen so that it looks like and functions like every other flex port.

**Nathan Carver**   1:10:59  
Mhm.

**Val Levitan**   1:11:14  
I would use Flexport. It's it's a it's a non expensive device and there's no point making a third product.

**Juan Martinez**   1:11:22  
So then Flexport can fully act as a SMID.

**Val Levitan**   1:11:26  
Yes it can.

**Juan Martinez**   1:11:28  
OK, that that's the point I was making, OK.

**Val Levitan**   1:11:40  
Again.  
Disclaimer, I'm I'm acting. I'm acting as though I know, but number one, I'm shooting from my hip. \#2 I'm not an engineer, so very important to understand where I'm coming from simply.

**Juan Martinez**   1:11:44  
Oh, absolutely though.  
Sure.

**Val Levitan**   1:11:58  
Pushing the meeting forward, otherwise it will take too long.

**Juan Martinez**   1:12:29  
To me that this this is clear, I just got to clean it up a little bit. We want to jump to a scenario where we still or do we want to still consider the Flexpay kiosk under a specific scenario?

**Val Levitan**   1:12:51  
Say it again, please.

**Juan Martinez**   1:12:52  
Flexpay does does the actual Flexpay kiosk. Do you envision that product moving forward under a specific scenario?

**Val Levitan**   1:13:06  
I I don't see Flexpay functioning outside of electronic wallet.  
So the moment you deviate from the concept of electronic wallet, I don't see Flex pay. As a matter of fact, I, you know, I don't see Flex pay progressing further. I think I think most like most likely it found its end of life.

**Juan Martinez**   1:13:14  
Right.  
OK. No, that that that was my question.  
OK.

**Val Levitan**   1:13:32  
Please continue. I need 2 minutes.

**Pavel Frolov**   1:13:35  
Actually, actually it will uh uh deviate to mini ATM I think.

**Juan Martinez**   1:13:44  
No, no, no. Because DV not in size, just in functionality.

**Pavel Frolov**   1:13:48  
Yes, yes.  
So if for our current flex, we just add in cheater operation mode plus money recycler.  
And left graphic user interface practically the same. It will will be moving to mini ATM I think.

**Juan Martinez**   1:14:16  
Sure. OK. So as a as just an action item, Flex pay kiosk as we know it will will will will become an obsolete product and it'll morph into this the mini ATM slash redemption tower.

**Pavel Frolov**   1:14:33  
Uh, but Juan, I think, uh, Flex POS has some.  
Advantages versus all other devices. For example, for some location it could be applicable. For example, we can remove bill acceptors and.

**Nathan Carver**   1:14:55  
Mhm.

**Pavel Frolov**   1:14:58  
A printers from all the machines.

**Nathan Carver**   1:14:59  
Yes.

**Juan Martinez**   1:15:03  
Um, we we with flex POS.

**Pavel Frolov**   1:15:07  
Yes. Oh, no, this this flex pay.

**Juan Martinez**   1:15:11  
Oh, no, no, I I definitely understand that. But I guess the the size of the Flexpay kiosk is going to be somewhat prohibitive. You know, it's it's going to be our most, our second most expensive device. But but you're right, I mean we we have been pitching that to the customer.

**Pavel Frolov**   1:15:23  
Mhm.

**Juan Martinez**   1:15:31  
Customers that hey, you don't have to add a printer, you don't have to upgrade any bill acceptor if you use the Flexpay kiosk, but it sounds like we want to go away from that scenario.

**Nathan Carver**   1:15:36  
OK.

**Juan Martinez**   1:15:49  
So yeah, Val, are we officially going to put Flexpay Kiosk to bed, just so we're clear?

**Val Levitan**   1:15:58  
Flex pay is an integral part of e-wallet business architecture.

**Nathan Carver**   1:15:59  
Yes.  
Yeah.

**Juan Martinez**   1:16:06  
Yes.

**Val Levitan**   1:16:08  
So.  
In this meeting right now, we're not discussing a wallet architecture. We are evolving a set of transactional products under a Tito setup.  
Which logically shaped differently from a business perspective.

**Nathan Carver**   1:16:24  
Yes.

**Juan Martinez**   1:16:31  
Sure.

**Val Levitan**   1:16:33  
Simply because Tito commands and dictates all transactions at the device, at the machines. So the philosophy here is that a player comes into the location.  
And goes towards the machine right away, and this is where all the transactions take place. Under e-wallet, a player enters a location, approaches a Flexpay device.

**Nathan Carver**   1:17:03  
Yes.

**Val Levitan**   1:17:05  
And starts the transaction there, receives a temporary wallet and travels through the location with the temporary wallet and only at the point of exit cashes in or.  
And transfers funds from the electronic wallet onto our card and further may be an ATM transaction. But that's a that's a different transactional philosophy. We do not necessarily have to kill one.

**Nathan Carver**   1:17:35  
Yes.

**Val Levitan**   1:17:40  
In order to progress another, we don't need to do anything for for E wallet.  
Transactions. We have our MV PS for E wallet transactions that will be completed within two weeks.

**Nathan Carver**   1:17:51  
No.

**Val Levitan**   1:18:00  
Yes, Paul.

**Pavel Frolov**   1:18:01  
Oh, not not exactly. I think in order when we switch to cloud server for income payments, we will need to make some minor changes in communication to support the same approach with cloud.  
Hopefully explain, yes.

**Juan Martinez**   1:18:19  
Or flex pay.

**Val Levitan**   1:18:26  
I don't understand.

**Pavel Frolov**   1:18:30  
Currently, currently Flex Pay perform income communication directly from kiosk from Flex Pay. If you want more secure transactions, we are we are going to introduce.

**Nathan Carver**   1:18:33  
Mhm.  
Mhm.

**Pavel Frolov**   1:18:50  
A cloud payment server that communicates to Incom and our kiosk do not make direct communication to Incom but a proxy connection to over the our cloud server Incom cloud server.

**Nathan Carver**   1:18:57  
OK.

**Val Levitan**   1:19:07  
Yes, yes. And that's why I specifically refer to E wallet MVP.  
Uh, features.  
The way it is designed right now, we do not rely on a cloud server.  
But shall we decide to develop E wallet architecture further and?  
Add to the MV PS and move into or add a feature of having a cloud server. Then yes, we would have to do further modifications to the E wallet business architecture or business.  
Thinking, but right now it's not a part of our discussion. We're discussing a totally different business logic, business logic that is based on a Tito set up.  
Sorry, we we we're kind of, we're parallel, we're we're evolving. If you go to our schematic \#1 where there's only a POS, our reliance on the serial community existing serial communication.  
Existing topography of having serial communication between the fledged link to Muda goose and we're only wedging ourselves between Muda goose and the income payment solution.

**Nathan Carver**   1:20:34  
M.

**Val Levitan**   1:20:39  
But there's no reliance here on Tito or any of the advanced communication of any sort.  
This is what exists today in the location. We're then saying, OK, we now have an operator on our site. We have his ear and we are saying, hey, Mr. Operator, here's a step up, connect a dispensing unit, a card dispensing unit.  
And that takes us to the second join.  
Yes, this one.  
But still, it's largely serial. Well, it's it's the existing serial communication between the fledgling to Mother Goose to POS and then to dispensing tower.  
And then an operator says I want to make a further step. Now I want to evolve into a Tito architecture.

**Nathan Carver**   1:21:44  
Mm.

**Val Levitan**   1:21:52  
And so we offer a third topography.  
No, that's that's the 4th 1:00.  
Yeah, this one.  
This is where we use dispensing towers.  
In Tito application in Tito topography.  
So here's every machine that's equipped with.  
A printer, a bill validator and the card is dispensed at the machines.  
Automatically.  
And then an operator is ready to make the final stop. It says I want to dispense cash.  
At my location.  
An operator has two choices to dispense cash. It's got a conventional way he can contract with an ATM provider and put a put a full-blown ATM here.

**Nathan Carver**   1:23:53  
Mm.

**Val Levitan**   1:24:03  
At a location.  
So he could run a.  
Full Tito and the previous topography as we outlined with our.  
Countertop dispensing devices. A player would receive a card and take this card to a freestanding ATM.  
Or an operator may say look.  
I want to immediately dispense cash at the machine.  
So income will provide us with the two step process.

**Nathan Carver**   1:24:44  
But.

**Val Levitan**   1:24:46  
Of graduating from.

**Nathan Carver**   1:24:49  
OK.

**Val Levitan**   1:24:52  
Their debit card to their price card and that price card immediately. The third step transitions to a cash dispensing.  
So this is the topography \#4. In this scenario, an operator needs to must remove a printer from the machine.

**Nathan Carver**   1:25:18  
M.

**Val Levitan**   1:25:27  
And must install flex port into every machine.

**Juan Martinez**   1:25:33  
Not just remove printer, remove bill acceptor too.

**Val Levitan**   1:25:37  
That's what I said. Printer and ability.

**Juan Martinez**   1:25:38  
OK, Sir.

**Val Levitan**   1:25:41  
Correct. I agree.  
Remove BV, remove printer and install Flexport.  
So minus BV minus printer plus flexport.

**Juan Martinez**   1:26:01  
Yep.

**Nathan Carver**   1:26:07  
2\.

**Val Levitan**   1:26:21  
I feel like I suppressed everybody's creativity with my.

**Nathan Carver**   1:26:25  
Yes.

**Val Levitan**   1:26:27  
We're taking over the meeting.

**Juan Martinez**   1:26:34  
No, I think that just clarified our our marching orders. I mean I it's it's somewhat clear to me now Nathan, you you're clear.

**Nathan Carver**   1:26:35  
Yeah.  
Yeah, I think the important thing is we're mining up all the ideas of the devices, how they're going to conceptually fit together and then we can refine that architecture and design, but it's important to see where the business.

**Pavel Frolov**   1:26:56  
It.

**Nathan Carver**   1:26:59  
domain.

**Pavel Frolov**   1:26:59  
It.

**Juan Martinez**   1:26:59  
Yeah.

**Pavel Frolov**   1:27:01  
Actually it looks like a good description for layer one of C4 from Nathan.

**Nathan Carver**   1:27:12  
Yeah.

**Pavel Frolov**   1:27:13  
When we need to understand the top level of each possible architectures.

**Nathan Carver**   1:27:23  
Correct.

**Val Levitan**   1:27:36  
I am. I am not 100% certain that I can see every step in use cases in.

**Juan Martinez**   1:27:37  
So then.

**Val Levitan**   1:27:47  
And the topography that we see in front of us right now on the screen.  
Where we remove the BV and printer from the machine and install flex port into every machine. So maybe it's worth our while to talk through these use cases.  
Let me give it a shot first. So our player approaches the.  
Mini ATM and inserts a $20 bill.  
From there comes out a barcoded or Tito ticket.  
So a player takes the Tito ticket, scans it at the machine.  
Or at our flexport.  
And the machine gets.  
The the deposits the value of the ticket.  
A player plays a number of games, gets a win. Let's say he won $100. He now says what print.  
A ticket or scan the same ticket.  
Because on the normal, on the normal Tito architecture, the printer, the the the machine has a printer and a bill acceptor.

**Juan Martinez**   1:29:12  
It's scanned.

**Pavel Frolov**   1:29:12  
3\.  
Yeah.

**Val Levitan**   1:29:24  
And so the bill acceptor kind of grabs the ticket, and the ticket is not longer in the hands of the player.  
So maybe we should leave. Maybe we should leave printers and tickets sitting inside of each machine.

**Juan Martinez**   1:29:35  
Yeah, the.  
Or the ticket.

**Val Levitan**   1:29:44  
But the moment, but the moment we do the the the moment we leave the bill acceptor sitting in front of in the machine, then we are depleting.  
Cash from ATM.

**Juan Martinez**   1:30:01  
Correct. And that would lead to player confusion. Do I go to the machine? Do I go to the mini ATM? And the easiest and the most common is to go to the machine because that's what they're used to.

**Val Levitan**   1:30:12  
And the moment they go into the machine and and insert money into the machine or into the bill acceptor, then we do not replenish money in the ATM.

**Juan Martinez**   1:30:22  
Right.

**Val Levitan**   1:30:23  
So that defeats the purpose.

**Juan Martinez**   1:30:27  
Yes.

**Pavel Frolov**   1:30:30  
And also for teeter operation, if the player has a teeter ticket and scans it, we need to remember that the value printed on the ticket and player do not know exactly where the money is on the ticket or on the machine.

**Juan Martinez**   1:30:52  
Right. Yeah, that that's why it almost we need to re-establish the e-wallet concept here from what we've just described.

**Val Levitan**   1:30:52  
Right.

**Pavel Frolov**   1:31:03  
Yeah, it looks like a wallet.

**Val Levitan**   1:31:04  
Or.  
Or or to put.  
Or to put a dispenser, not the dispenser, but the recycler into every machine.

**Juan Martinez**   1:31:23  
So that that becomes tough, Val, because we don't have knowledge of the inside of everyone's machines, and let's just say it won't fit inside 50% of the games.

**Val Levitan**   1:31:30  
Oh.  
Stalled and do do the side mount.  
For every machine.  
I'm not saying that I like it, I'm just saying.

**Juan Martinez**   1:31:45  
Sure, sure. Yeah, yeah.

**Val Levitan**   1:31:47  
Yeah, don't don't kill the messenger. I I know that I I don't like the side boxes.

**Juan Martinez**   1:31:49  
OK, OK, yeah.  
Sure, sure.  
Yeah, that would be visually like we've traveled back in time to the 90s when the sidemount bill acceptors first came into the markets.  
So yeah, I I think I need to brainstorm on the mini AT this this particular mini ATM redemption drawing just to fine tune the use case that we just talked about.  
I need a tall Starbucks and then I need to start thinking.

**Val Levitan**   1:32:35  
OK, so let's conclude the meeting with the undertaking of brainstorm on use cases for this particular topography, because everything else I think works.

**Juan Martinez**   1:32:51  
Uh, agreed. And Nathan, I will clean all these up and then I'll send them to you to move them into Mermaid or GitHub, whatever we're gonna do with them.

**Nathan Carver**   1:32:52  
Look.  
Perfect. Alright, that sounds good.

**Val Levitan**   1:33:03  
OK. Can we conclude the meeting?

**Juan Martinez**   1:33:06  
think so. Appreciate it. Thanks everybody.

**Nathan Carver**   1:33:07  
Yes.  
Alright, thanks all.

**Val Levitan**   1:33:11  
OK, thank you. Can you please circulate, circulate the dot M dot MD, OK.

**Juan Martinez**   1:33:11  
Bye.

**Pavel Frolov**   1:33:11  
Thank you. Bye.  
I'm not.

**Nathan Carver**   1:33:18  
Yes, absolutely.

**Val Levitan**   1:33:19  
Thank you. Bye.

**Nathan Carver** stopped transcription