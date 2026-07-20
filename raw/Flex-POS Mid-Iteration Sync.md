---
tags:
  - FTP-communication
  - POS-device
  - Mother-Goose-board
  - juan
  - github
  - rgs
---

**Transcript**

July 9, 2025, 12:05PM

**Nathan Carver** started transcription

**Nathan Carver**   0:06  
All right, so we'll get this started. So action item update dates for work in progress this week AS meeting as as Juan has sent out information on that.  
Jim and we're in the process of requesting more documentation and waiting to hear back him back from him and we've shared out. I put in GitHub the some of the architecture stuff that I went through and in Confluence for everyone to review.  
And I believe Juan uploaded the the meeting transcript for everyone.  
Anything that I missed there, Juan, that we need to?

**Juan Martinez**   0:49  
No, we like he said, we we reached out to Jim at at RKS and included Felipe in the loop on us purchasing the parts and on getting this new Mother Goose, which Nathan will touch on in a second here.

**Nathan Carver**   0:51  
OK.

**Val Levitan**   1:08  
Was he receptive to the idea?

**Nathan Carver**   1:09  
OK.

**Juan Martinez**   1:12  
Yeah, well, once we explain. Yeah, go ahead, Nathan.

**Nathan Carver**   1:13  
Uh, yes.  
Oh, sorry. Yes, he was. He was very receptive and he's also seems willing to help make changes for us specifically around if we wanted to hash or encrypt the files or if we needed it, you know, any other.  
Extra work from him. They're willing to work with us.

**Val Levitan**   1:36  
And how will they retrofit the the product in the field?  
If if what if you require any encryption or any additional software changes?

**Nathan Carver**   1:44  
That I'm not sure I.  
Right. So that we're not clear on. So we need to understand if that's a new board roll out for them or if they're gonna push an update to a board and then roll it out or if they can update remotely, which is possible.

**Pavel Frolov**   2:06  
OK.

**Genadi Peari**   2:09  
Are we?

**Val Levitan**   2:09  
Is it? Is it possible to update from our POS? Is it the two way communication?

**Juan Martinez**   2:18  
It's not even a direct communication.  
You want to touch on the FTP function, Nathan?

**Nathan Carver**   2:26  
Yes, so let me um.

**Juan Martinez**   2:30  
So while he's pulling that up, so this new Mother Goose board replaces the existing Mother Goose board. This new Mother Goose board is based on an FTP upload, so it doesn't even necessarily need to talk to the printer.

**Nathan Carver**   2:32  
And.

**Juan Martinez**   2:48  
And that information is uploaded to FTP for us to grab and then interact with our our POS device. So there is nothing serial here per se it it we're grabbing information from the FTP.

**Val Levitan**   3:07  
Is that us? What a safe form of communication and it be?

**Nathan Carver**   3:07  
And.  
And yeah.

**Val Levitan**   3:14  
Yeah.

**Nathan Carver**   3:16  
Um, yes. So what it does is it.  
Removes the between the Mother Goose and Flex POS.  
So replacing the Mother Goose with the RKS, they're gonna send a file through a secure FTP connection to a JBL FTP server that we would create. We would create this instance.  
And then from that server we could then pick those files up with the cloud.

**Val Levitan**   3:45  
But I'm sorry.  
But I'm sorry, hold on a second. Are we saying that it requires a replacement of the board? Who's going to pay for it? How does it work?

**Nathan Carver**   3:57  
Correct. It would require replacing the existing board out there.

**Val Levitan**   4:02  
But it's not part of our architecture, that's not.

**Genadi Peari**   4:08  
Exactly.

**Val Levitan**   4:09  
If we because if we have to replace their board, we may as well replace it with our Smith board and put an end to all of it. And by the way, our Smith boards are so inexpensive that we could truly give it away.  
You know, if somebody subscribes to to our P purchasing of our POS, we can give away our Smith boards.  
This is how in my mind I would structure all the deals.

**Nathan Carver**   4:38  
Yeah, that makes sense.

**Genadi Peari**   4:41  
Did.

**Juan Martinez**   4:42  
Yeah, but Val, I mean, so if if we're sniffing serial at the printer, that is always less secure than grabbing this uploaded file from an FTP server, so.

**Nathan Carver**   4:44  
Yeah.

**Val Levitan**   4:57  
I'm not, I'm not arguing that point. I'm just saying that if we have to replace boards.

**Juan Martinez**   5:03  
Yep, it's one board per location, and I believe that since we don't own this board today, it's something that we could say to the master. Hey, as part of deploying our system, you need to upgrade to the latest Mother Goose board.  
Which is $466 and is 1 board per location, not per machine.

**Val Levitan**   5:30  
But we may as well then install our Tito server.  
And it it would be much better solution.  
If if master is already saying I will invest $466 into this stupid board, then we may as well sell them on our server and we can tell them, look, you don't have to put $466, you could just pay us monthly.  
We're talking about a bill of material of, I don't know, under $100.

**Nathan Carver**   6:15  
Because what this just showed us wasn't different.

**Genadi Peari**   6:17  
They're trying to sell it to everybody, right?  
They're trying to sell it to everybody. How come we will be better than others?

**Nathan Carver**   6:21  
What's that?

**Juan Martinez**   6:30  
They're. I don't believe they're selling this. They're not necessarily advertising this because this takes some development work. Remember, almost everybody else is deploying a physical kiosk with the Tito server that dispenses cash.

**Genadi Peari**   6:46  
I think they did it. I I think they did it exactly for the purpose towards the new legislation. It's not a new development. They he pulled up from his mind for sure they already have a almost ready product.

**Juan Martinez**   6:47  
There would necessarily be none. What's that?

**Genadi Peari**   7:04  
And this is exactly because they're losing the market. If they don't introduce this board, nobody needs them.  
They want to stay on the market.

**Juan Martinez**   7:16  
I I understand, but what wasn't our initial goal for the operators and small locations who wanted to spend as little as possible and to for us just to deploy POS, this is all we would need at a location.

**Nathan Carver**   7:18  
Mhm.

**Genadi Peari**   7:30  
It.  
And our initial goal, sorry.

**Val Levitan**   7:33  
If we.  
I'm not saying, I'm not saying that we don't need it or need it. I'm not, I'm not judging what we need. I'm just saying that if we need it, if if we're saying we need it or an operator needs it.  
Then there has to be a willingness to purchase something for $466. And if there is willingness to purchase something for $466, we may as well tell the operator, hey, buy our server.  
And you don't have to pay $466 upfront. We can rent it to you for, I don't know, X, you know, couple of dollars per day and you don't have to worry about it.

**Juan Martinez**   8:25  
Sure. I guess Val, my my point was that at the FTP data, this is we're on the hook. If somebody intercepts that printer signal, you know it's still serial, it's still right there. It's hidden behind the counter, easy to get to.

**Nathan Carver**   8:26  
Yep.

**Juan Martinez**   8:44  
This is just so much more secure, in my opinion, than risking the sniffing of serial traffic on that printer port from a liability perspective, which is a JVL liability.

**Val Levitan**   8:58  
The the way I I want to address the liability because it's a white elephant in the room. I think liability is a huge issue.

**Pavel Frolov**   8:58  
Oh.

**Val Levitan**   9:11  
And if we were to say, look, whatever the current architecture is in the location allows us for very little tolerance to risk.  
And.  
By improving.  
Hardware security hardware in location it will allow us.  
And expand it.

**Pavel Frolov**   9:41  
Yes.

**Val Levitan**   9:41  
Risk profile.  
Then it's it's up to the operator either to comply with one risk profile or the other.  
Let me elaborate and practice what I'm saying. If we are saying that using serial port is unsafe and we feel uncomfortable, we should in our documents we should say look.  
We will swipe your account immediately upon transaction, like within 5 minutes.  
And we want you to make sure that you have funds available on your account because we're not taking any risks with you. And an operator may say, yeah, I'm OK with that. You know, I don't want to invest any money into infrastructure. I, you know, my operation is running smoothly.  
And I'm OK with them.  
And so before we validate the transaction on our server, we swipe the account.  
And we transfer the money, same money that we now fronting to income.  
So this is case point \#1. Case point \#2 if an operator says well, no, I prefer some leeway and I want you to front your money for me.  
Then great, then install our server. We want to make sure that the money is coming from the machine, that there was a genuine payout. We want to validate it and then we will give you, let's say.  
Two working days.  
to transfer the money.  
So I think this is how it should be handled with the operators.  
I realized that the current situation with serial port is.  
You know an increase risk profile.  
But I think it's relatively limited, I mean.  
An operator should condone to committing legitimate fraud on a regular basis by tapping into serial port.  
I could some.

**Pavel Frolov**   12:10  
Yeah.

**Nathan Carver**   12:15  
Yeah, and we just need to identify the risk and create detection, create detection methods and prevention methods.

**Val Levitan**   12:15  
I'm not seeing. I'm not seeing.

**Nathan Carver**   12:24  
For the risk that we're taking on, it's just a trade-off in my in my perspective. So I I don't think the FTP versus serial, I think this is just an option of perspective and we we I don't think we're proposing to go with this other than this is an option the competitors are doing.

**Pavel Frolov**   12:30  
Uh.  
OK.

**Nathan Carver**   12:43  
Someone's trying. People are trying to find the solution.  
Around the printer connection.

**Val Levitan**   12:51  
I I think, I think our goal or objective for conversing with RKS, I'm assuming that RKS is the maker maker of Moto Goose.

**Pavel Frolov**   13:00  
Weh

**Juan Martinez**   13:01  
Yes.

**Val Levitan**   13:03  
So I think the objective for that conversation was not to.

**Pavel Frolov**   13:04  
8\.

**Val Levitan**   13:10  
Usher him into promoting new hardware or help him sell new hardware, but to get his communication protocol for the existing hardware so we can validate A legitimate payout with possible.  
Uh.  
Some digital signature of some sort if possible through existing mother goose without increasing any of the hardware from RTS and so we could wedge our POS.  
Between the machine and a printer instead of us trying to sniff those signals through some sort of back channel, you know, re-engineering efforts.  
If that is not possible, then we have multiple solutions to go with. We could say, look an operator, if you want to install our POS, we're going to give you for free or the minimal cost cost our Smith boards.

**Nathan Carver**   14:09  
Mhm.

**Val Levitan**   14:17  
That will replace the full fully replace the functionality of Mother Goose. It will not cost you any money.  
And you will be able to use secure transactions between the machine and the POS and we can install our server on your location at a minimal cost to further increase.  
Security, etc. We have ways to go. We don't need our key RKS.  
It just get temporarily.  
Convenience for us and we can we can reverse engineer the serial signals. It's not. I mean instead of implementing it, that should take us maybe a week or two. It will take us maybe 30 days to reverse engineer it and test it.

**Pavel Frolov**   15:07  
This.

**Genadi Peari**   15:16  
More more than that.

**Nathan Carver**   15:16  
So Jim is willing to help with that. He he did say that because we did ask about implementing the serial sniffing and they are willing to help with that. And then the FTP side was offered up as a alternative. So I think we're OK. We're gonna get their help is.  
Is my read on Jim.

**Juan Martinez**   15:36  
Mhm.  
Yeah, he he wasn't trying to sell it to us. He just says, oh, I understand what you want to do, but guess what? I've already got done this solution and it's more secure. So that that's what led to that conversation.

**Genadi Peari**   15:40  
But.  
But.  
I I'm, I'm sorry, I don't. What do we ask from him? Because there are two points where we can intercept with the with the system.

**Val Levitan**   15:50  
OK, OK.

**Genadi Peari**   16:01  
Are we are we clear that in in each machine has a yellow board right from RKS. Then this yellow board is connected Daisy chain and there is a go in one cable RS485 to the mother goose to the motor goose.

**Juan Martinez**   16:08  
Yes.

**Genadi Peari**   16:18  
And the from the mutagus it goes to the rinter.

**Juan Martinez**   16:21  
OK.

**Genadi Peari**   16:22  
So RS485 goes to the Mutagus and from Mutagus it goes to serial communication to the printer. There are two different protocols.

**Juan Martinez**   16:33  
Yep, yeah, forward.

**Val Levitan**   16:34  
So thank you for thank you for explaining this. I was not aware of it.

**Genadi Peari**   16:40  
Now there are advantages and disadvantages in both. If we for example in interfere in in the RS485 after yellow boards, it goes directly to our POS, we basically.  
Can I print the tickets? Then we people don't need the Mother Goose at all.  
We can get the signal.  
Display and print the ticket or transfer it back to the mother goose.  
We can also. The other point is we can interfere after muta goose between printer and the muta goose. It's easier for us to do it because it's just a printer commands, right? Well set of printer commands.

**Pavel Frolov**   17:27  
G.  
Yeah, exactly.

**Genadi Peari**   17:34  
And we just need to know what is the line on the ticket itself. What does it mean each character? And in this case, I think it's more secure because the mutagus stays in the cage, right? You don't touch it.  
You don't do anything, you just take a cable from the from this to you and back to printer.

**Pavel Frolov**   17:56  
Yeah.  
And cashier can validate each ticket by printing a report on his.

**Juan Martinez**   18:09  
But let me ask you guys though, from a from a service perspective, you believe it to be easier. You showed me several failure points, the yellow board, the Mother Goose, the cable, you know both.

**Genadi Peari**   18:09  
Right.

**Nathan Carver**   18:10  
Mhm.

**Genadi Peari**   18:24  
Yellow board you don't touch.

**Juan Martinez**   18:26  
None of those are items that we have direct access to. They're owned and controlled by the master. If one of those fails, our entire system goes down. Yet we can't support those products. We can't really touch them. I just want to make sure that we're all thinking about it.  
Post go live that you know that that's if we're sniffing and intercepting at those points and something goes wrong, that's not our hardware. We we can't take a service call. We can't tell them what to do.  
We've got to shut down the the location and the master has to deal with it because it because we've, you know, not made that necessarily clear up front.

**Val Levitan**   19:11  
Correct, but.  
You you are correct, but the benefit to an operator is that he's dealing with the with a familiar system, familiar architecture. He is used to servicing that architecture and detecting the failure points.  
And he's not investing any money.  
If they want a single point of failure and single point of service, we are happy to step in. But now an operator is looking at changing a bunch of hardware, rewiring a lot of things.  
Investing money and I think that the majority of operators and maybe I'm wrong, doesn't matter whether I'm wrong or right, but I think the majority of operators will opt out.  
Opt out of investing money.  
And it seems, and it seems that this is what we're observing today and it became even more clear to me why the market is so unmoved and so unworried about.  
The rapidly approaching date.  
Of June 1st, 2026\. Why nobody's gravitating towards purchasing.  
The new equipment if the mark if the if the D date was approaching so quickly.  
This is because they have a solution.  
They don't need a solution. Nobody wants to invest money. The market is validating our own theory.

**Juan Martinez**   21:00  
Right. You're talking about the handheld PAX device. You're right. I mean, that could be that $300.00 is so cheap for these operations that that is the ideal solution. It's all manual. Nobody cares about security, so.

**Val Levitan**   21:04  
Yes, yes.

**Juan Martinez**   21:18  
No, I I understand.

**Val Levitan**   21:23  
And so if we want to wedge ourselves into this market and hypothetically speaking, there is another 50% of the market still untapped and I don't know whether it's controlled by those that are looking for a fuller solution, then we have a couple of things going for us. First of all, we're looking for.  
Those that are dissatisfied with the, I'm going to call it last mile validation which is offered currently not offered by pack solution and those 50% of the market that are not looking for full kiosk or full blown solution that is offered by.  
The competitors and would still go for a POS system.  
Because the our POS solution offers that last mile validation, which is reconciliation between what's printed on the ticket and the the the POS.  
So just to repeat, just to refocus our conversation on what market is telling us, we know factually that the market is not worried. Nobody is rushing to purchase anything. The deadline date is approaching. The market is not worried.  
We should take it as our cue of the mindset of the market. The market doesn't want to spend the money.  
So.  
I think that RKS is here to say what we should do is to wedge ourselves between the the very last board, the Mutagus and the printer.  
And so we will offer a step up to PAX solution, which is.  
You don't need to enter manual.  
Validation or manual figures of any sort into the packs, but POS will see the payout and will immediately by pressing 1 button it will issue a ticket. We then have a path.  
From POS to.  
An operator may grow his system further by adding a tower dispensing unit, et cetera, et cetera. And I think our our ace in the deck.  
Is by offering the mini ATM solution, the redemption center at the machine. This is what we discussed in our last meeting and this was kind of an aha moment for everyone.  
Unfortunately, Pavel was not at the meeting. At some point I should regurgitate this to Pavel, but that, you know, for the rest of us that understand what I'm talking about, that's the ultimate, in my opinion, ultimate.

**Pavel Frolov**   24:27  
OK.

**Val Levitan**   24:34  
You know, game changer.  
Pavel, for your awareness, the when we talk about mini ATM, the legislation, the law provides for a conversion of this.  
Card in two steps. Sorry, in three steps into cash.

**Pavel Frolov**   24:59  
Mm-hmm.

**Val Levitan**   25:02  
So first and and it's and it's seamless to to the player but behind the scene from a legislative perspective there are three-step conversion. So first legislative.  
Step or approval is to put money on the prepaid card, then to buy a price card for a nominal fee, which converts.  
Debit into.  
Redeemable, redeemable cash and the final solution is to take this to an ATM machine and receive cash.

**Juan Martinez**   25:38  
And.

**Val Levitan**   25:53  
So what we are saying is let's bring the ATM type of fuel right in front of the machine by utilizing our tower combination where we put our a a build to build recycler.  
Inside of the ATM.

**Pavel Frolov**   26:18  
So.

**Val Levitan**   26:18  
Inside of the tower, I meant to say.  
I don't know if you fully visualize this thing or not. If you require more explanation was this as these meetings are objectives of the of these meetings is to bring a total alignment in the group. If you require more explanation then let's do it. But I'm actually.

**Nathan Carver**   26:37  
Mhm.

**Val Levitan**   26:42  
Very happy with the format of these meetings because.  
We we will see such distractions like just like RKRKS threw at us in the last meeting. Hey, I have this FTP enabled board. I already thought about the solution. I'm actually very happy. This is a fantastic piece of information.  
I'm glad that we reached out to RKS because as Gennari said, OK, we're now understanding where his mind is going and what solution he foresees.

**Pavel Frolov**   27:07  
OK.  
It.  
Let me express some some ideas. First of all, idea with FTP server. For me it's it's a wrong direction. It's it will decrease reliability of the system.  
It doesn't matter for us or for any other director who will use it. And then the key point I posted my question here in chat if we able.  
To decode the field confidence number from the ticket, we will be 100% protected from fraud.

**Nathan Carver**   28:10  
So I I think an action item based on Pavel's comment is 1 is we can connect Jim with Gennady or Pavel or the engineering team directly so they can start getting these questions and we're not in the middle.

**Juan Martinez**   28:11  
Soy.

**Val Levitan**   28:22  
We, we, we don't, we don't want that. I think Nathan, you are an engineer yourself and you can get to the bottom of this thing and you're on the same time zone. I would like to unload Pavel and Gennari from this interaction.

**Nathan Carver**   28:32  
OK.  
OK.

**Val Levitan**   28:40  
It's it's culturally not compatible.

**Nathan Carver**   28:45  
All right, I will take Pavel's question in in chat, but Pavel Ganadi, please send for your question list to me and I'll I'll start communicating with Jim.

**Pavel Frolov**   28:57  
OK.  
Actually I made some some investigation related to to this field and I see first number 15 is amount and then the second part.  
9 or 10 numbers. If it converted to hex to hexadecimal number, it contains 2\.  
I I would say field 2 bytes, some SHA. Oh no, not SHA. I I don't know exactly some number, cache number and the rest 2 bytes.  
Also value of the ticket. So we just need to understand what's this two bytes. How how can we calculate bytes from other data to validate this ticket?

**Nathan Carver**   29:57  
OK.  
OK, so these two bytes within the pack total payload is what the the mystery for us. OK.

**Pavel Frolov**   30:00  
8\.  
Yes.  
Yes.  
He he.  
And also we already talked to Gennady and we we think that they will never share a real protocol RS485.  
Five, because in this case we can replace Mutagus and they don't like this.

**Nathan Carver**   30:45  
Yes.

**Pavel Frolov**   30:47  
We prefer to to have this proprietary.

**Juan Martinez**   30:48  
Yes.  
Yeah, so we we need to focus on the RS232 to the printer protocol.

**Genadi Peari**   30:59  
Um.  
Do you want to try to or there is no even point to to take a look on this?

**Juan Martinez**   31:13  
Ask him.

**Pavel Frolov**   31:19  
So it was an idea from United to give for yellow board and Mutagus to Evgeny try to understand the protocol RS485.

**Juan Martinez**   31:34  
OK.

**Val Levitan**   31:35  
I absolutely have zero doubt zero that Evgenia will not be able to.

**Nathan Carver**   31:36  
Oh.

**Val Levitan**   31:45  
Reverse engineer it like literally 0 concern.  
I actually, I almost feel that communicating with Jim is a is a waste of time.

**Juan Martinez**   31:52  
Still.

**Val Levitan**   31:58  
I think it's a good thing, but part of me says it's almost a waste of time, but.

**Pavel Frolov**   31:58  
OK.

**Juan Martinez**   32:02  
We have all the documentation from RKS in confluence. Pavel has Yevgeny seen all that. It's very detailed documentation actually.

**Pavel Frolov**   32:17  
Actually this documentation tried to pass through this documentation yesterday and currently speaking I only found one I one informations that I've.  
Known before about a protocol from Mutagus to configure Mutagus from a personal PC. I've never.  
I know about knew about this, but I don't know is it possible to use this protocol to to get some data from the Nutagus?

**Nathan Carver**   33:00  
OK.

**Pavel Frolov**   33:02  
Yeah.

**Val Levitan**   33:04  
OK, so the action item from this meeting is to contact Jim and ask him to help us to give us the protocol for validation of that hex number.

**Pavel Frolov**   33:06  
So.  
3\.

**Juan Martinez**   33:18  
Yes.

**Val Levitan**   33:20  
OK, if he says no, it's not a, it's not a, it's not an issue for us. We can reverse engineer it.

**Pavel Frolov**   33:32  
No, I think we will not be able to reverse engineer this particular verification, but we still able to to get value on the ticket but without 100% validation.  
Sure that nobody tried to make a fraud.

**Val Levitan**   33:55  
Well, my my point was that if RKS doesn't cooperate with us, we can find a solution for improving the security of the validation. But I I detect that.

**Pavel Frolov**   34:03  
Yes.

**Val Levitan**   34:12  
We would prefer to wedge ourselves between the final Muda goose and the printer, so we're kind of contained within the cage solution.

**Genadi Peari**   34:27  
In this case they have to provide this information because it's not proprietary, it's between it's for the printer. They have to do the provide the format format of their ticket.

**Pavel Frolov**   34:41  
And in this case we need to understand what printer market using.  
Because I think we do not need to support six of them in case if they use just two models.

**Nathan Carver**   34:57  
Yeah.

**Val Levitan**   34:59  
OK. So that's the next undertaking probably for Felipe is to tell us what's the majority of the printers in the market?

**Juan Martinez**   35:10  
Yeah, I mean from the documentation, I think we know that it's a Citizens 33541 printer for all of their documentation.  
But we'll have him confirm.

**Pavel Frolov**   35:25  
OK.

**Genadi Peari**   35:27  
I saw documents on the Epson as well, I think.

**Nathan Carver**   35:27  
OK.

**Pavel Frolov**   35:27  
Thanks.

**Juan Martinez**   35:31  
Yeah.

**Pavel Frolov**   35:34  
Probably some of some of them, probably some of them use the same common set.

**Genadi Peari**   35:34  
And did the car.

**Nathan Carver**   35:36  
OK.

**Juan Martinez**   35:40  
Yeah.

**Nathan Carver**   35:44  
OK.  
All right, so the action items we have is I will connect with Jim. We are looking for information on the two bytes there for the valid for the to understand that validation number and how to use that to verify that the ticket is.  
Uh, not fraudulent.  
And we're also going to.  
Gather information with Felipe on the printer market to understand the printers used with Mother Goose.  
OK, I know we're coming up on time, so we can blast through the last few action items or to to get updates on. We have the income API meeting today or Juan and I are meeting with income.  
And that's at 2:00, so we'll have some information updates later today on that.  
Uh, we also had the let's see our action items reviewed the second mother competitor. Um, so we do you have anything you wanna um add on that?

**Juan Martinez**   36:54  
Yeah, Elipa, the other Mother Goose competitor is is manufactured by Omega Games, but it is mainly done for their operations and it it's it's less than.  
1% of the market. Felipe has never actually seen one in use and he believes that if we focus on RKS, we're gonna.

**Pavel Frolov**   37:16  
This.  
Sure.

**Val Levitan**   37:18  
M.

**Juan Martinez**   37:24  
Gonna be fine and that we should not focus on anything other than our chaos.

**Nathan Carver**   37:30  
OK.  
All right, next item is the hardware shipping.

**Pavel Frolov**   37:33  
Thank you.

**Nathan Carver**   37:37  
That was was at Juan and Felipe.

**Juan Martinez**   37:37  
Uh, yeah, so.  
Yeah, same thing. I e-mailed Jim, copied Felipe. Because Ganani, you have one set already. Do we just need three or do we actually want 4?

**Nathan Carver**   37:42  
Or yeah, go ahead one.

**Genadi Peari**   38:01  
Once we position ourselves between Mutagus and the printer, I think the only thing we need the different printers.  
And if there are different mutagus options or maybe Oh no, it's the same command set.

**Pavel Frolov**   38:19  
Yes, but I'm not. I'm not sure that different modules, mod models of Muto Goose produces the same tickets.

**Juan Martinez**   38:20  
Of further documentation.

**Genadi Peari**   38:29  
And ask Jim, right, if they have different versions of Mutago, so we might need it.

**Juan Martinez**   38:31  
Yeah.  
There there there are two old versions plus this new one which the documents are not on their website for. So yes, there there are currently 2 plus the third one.

**Nathan Carver**   38:39  
OK.

**Pavel Frolov**   38:40  
OK.

**Genadi Peari**   38:50  
So I I'll send the model what we have and probably we'll need to get two others.

**Nathan Carver**   38:51  
OK, yeah, so.

**Juan Martinez**   38:59  
And these that should include printers.

**Genadi Peari**   39:07  
It's nice to have different models of printer. I'll send the the one we have if it's any other on the market, so we probably need it.

**Juan Martinez**   39:16  
OK.  
And Val, just to confirm, in the essence of time, are we trying to get these free from partners, masters or should we just buy these from RKS?

**Val Levitan**   39:30  
We should just buy them from RKS in order to save time.

**Juan Martinez**   39:34  
OK.

**Genadi Peari**   39:37  
Once you buy from them, you you can get some portals.

**Pavel Frolov**   39:38  
OK.

**Juan Martinez**   39:41  
Yeah.

**Genadi Peari**   39:42  
Yeah.

**Juan Martinez**   39:45  
Yeah.

**Nathan Carver**   39:45  
OK, so the two additional actions is make sure that we ask Jim about the variation signals with different versions of the board and we're going to send the different printers to Gennady, either just purchase them directly or however we obtain them.

**Juan Martinez**   40:02  
Yep.

**Nathan Carver**   40:04  
OK.  
Um.  
All right, great. Anything else on hardware shipping or we can quickly move through the rest here?

**Juan Martinez**   40:13  
I think we're clear there.

**Nathan Carver**   40:16  
OK. We talked a little bit about architecture and development. Pavel, is there anything additional you want to update on development or architecture?

**Pavel Frolov**   40:27  
Not anything about architecture, but we'll inform all of you that our developers already started some preparation for this project.  
Preparation. I mean to produce template application back end application for POS and start some screen layouts changes for POS keeping in mind different monitoring.

**Nathan Carver**   40:46  
OK.

**Pavel Frolov**   41:03  
Of size.

**Val Levitan**   41:06  
I think, I think it's important for us to handle this development in a slightly more official way than how we used to do it in JVL without formal paperwork, et cetera.  
And and actually that's main reason I brought in Nathan to help you to put together the architecture and the proper repositories etcetera. It's really my test case for how to do things.  
Better than what we used to do, so I would like to have the architecture resolved first.  
And then moving into design second, I also would like to understand the.  
What hardware we're gonna be using? What?  
Technology stock we're going to be using and I would like to have it resolved first. I would like to have requirements built up aggressively.  
Uh.  
And capabilities of the product.  
It's a it's a showcase development for me. I really would like to do it correctly.

**Pavel Frolov**   42:24  
Yeah.

**Nathan Carver**   42:31  
OK, so create a.

**Val Levitan**   42:32  
So, so Pavel, I think that you should rein back, hold back the developers, let them do. For example, I know that Dima jumps into solution right away. I don't want it.  
And if Dima has spare time right now, it's important for him to finish the Tableau integration because we are.  
We we need that functionality and you know.  
He promised that within 30 days.  
30 days are fast approaching. I think it's got a week left on the 30 day cycle.  
And I really need that Tableau integration.  
So, so refocus them, rein them back. Let's discuss capabilities on a on a per product basis. So we have our lineup of products already agreed upon.

**Pavel Frolov**   43:18  
Mhm.

**Val Levitan**   43:33  
We now want capabilities for each of the products and we want requirements. We want persona and use cases.  
When this is done, I would like to have a complete architecture discussed.

**Pavel Frolov**   43:51  
Yes.  
Mhm.  
OK.

**Val Levitan**   44:00  
So I'm going on vacation. This is where the least of my time is required. So for for you, Pavel overall, please use this time until August 1st to iron out those things.

**Nathan Carver**   44:01  
OK.

**Val Levitan**   44:17  
On August 1st.  
We need to.  
We're going to have two major streams of development. We're going to have Omni HHR on Omni started and we want to start development of the transactional products that we spoke about.  
I have few days left in this week. I will not. You will not have access to me during the vacation, so I have only a few days left this week when we can discuss.  
Uh, the actual product.  
And this is where you might need my time. So unless you don't need, you don't have any questions on that.

**Pavel Frolov**   44:59  
Yup.  
Yes.

**Val Levitan**   45:07  
Which, you know, I'm fine with that.  
Then spend the rest.

**Nathan Carver**   45:13  
When does your vacation start, Val?

**Val Levitan**   45:16  
From 12 to the 22nd.

**Pavel Frolov**   45:17  
OK.

**Nathan Carver**   45:22  
OK.

**Val Levitan**   45:24  
I will not have my laptop on me.

**Nathan Carver**   45:33  
OK.  
So we have one more meeting on Friday as a time slot that we can make discuss. We can discuss these with Val before his vacation. So we'll schedule time for tomorrow if if we need that.  
I guess, um, Pavel, if that's something you wanna do, go ahead and schedule or let me know when I can throw it out there.

**Pavel Frolov**   45:59  
Yeah, I I think we can meet tomorrow to discuss requirements and capabilities to make at least list of all of them.

**Nathan Carver**   46:09  
OK, I'll I'll put a time slots tomorrow then.

**Val Levitan**   46:14  
Only on a on a per product basis, am I right?

**Pavel Frolov**   46:20  
Yeah, right now for POS.

**Val Levitan**   46:27  
When when you when you deal with overall architecture of the transactional business, you should probably see the horizon of the products that we already have in mind, at least the line up of products.

**Pavel Frolov**   46:42  
Mhm.

**Val Levitan**   46:44  
So I think it's important to summarize the list of products that we envision. For each product, I would like to discuss at least a set of initial capabilities.

**Pavel Frolov**   46:46  
Yes.

**Val Levitan**   46:57  
So you could start wrapping the overall architecture around your mind and the tech stack for how we are going to handle it.

**Pavel Frolov**   47:07  
OK.

**Val Levitan**   47:16  
So I would like to dedicate the next two days discussing the lineup of products and the capability of those products. When I'm on vacation, you are more than capable in this team discussing.

**Pavel Frolov**   47:26  
Yes.  
OK.

**Val Levitan**   47:32  
Use cases, the persona, use cases and the requirements.

**Pavel Frolov**   47:38  
OK.

**Val Levitan**   47:39  
When you have all of them nailed, you can then move on into architecture.  
The overall system architecture for this transactional section of our business.  
So the objective for for the meeting for tomorrow is to validate products and its capabilities.

**Nathan Carver**   47:58  
OK.

**Pavel Frolov**   48:02  
Skip.  
Mhm.  
This.

**Val Levitan**   48:17  
Let's have a 2 hour meeting tomorrow.

**Nathan Carver**   48:26  
All right. Do you all want to do 7 or 8:00?

**Val Levitan**   48:35  
It's whatever, whatever everyone wants. I don't care.

**Juan Martinez**   48:39  
Yeah, seven side with me.

**Val Levitan**   48:42  
Seven or eight doesn't matter. I think Gennadi prefers it if I'm not mistake.

**Genadi Peari**   48:49  
Doesn't it?

**Nathan Carver**   48:50  
OK, we'll do 8:00.

**Val Levitan**   48:53  
OK, 8:00. I'll see you every.

**Nathan Carver**   48:55  
All right, we'll do 8 o'clock. Yep.

**Val Levitan**   48:58  
Can you can you please post? Can you please post the full transcript of this meeting in the MD format?

**Nathan Carver**   48:59  
Alright, that's.  
Yes, I will do that.

**Val Levitan**   49:10  
Thank you. Okay, bye bye.

**Nathan Carver**   49:12  
All right. Thanks, everyone.

**Genadi Peari**   49:14  
Thank you.

**Pavel Frolov**   49:15  
Take a bite.

**Nathan Carver** stopped transcription