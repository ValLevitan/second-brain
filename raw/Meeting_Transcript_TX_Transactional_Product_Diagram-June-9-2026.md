**TX - Transactional product Diagram-20260609\_141742-Meeting Recording**

June 9, 2026, 6:17PM

1h 42m 7s

**  
Val Levitan** started transcription

**  
Andrei Klimovich** 0:07  
Okay, so.  
Could you please let me know if you can see my screen?

**  
Juan Martinez** 0:14  
I can see the screen, but I cannot read any of the labels. You're going to have to zoom in.

**  
Andrei Klimovich** 0:18  
Yeah, sure. Okay.

**  
Val Levitan** 0:20  
Yeah, neither can I.

**  
Andrei Klimovich** 0:21  
Yeah, so basically what I built here is an overview of player flow on one of our solutions, where...  
Flex IQ is installed and every single machine is installed with upgraded with Flex port. So it's split into swim lines where each swim line represents one standalone piece of this ecosystem. But let's focus on a player experience and when we will go through the main flow, we will see all the details.  
how other parts of the system are involved. So player starts with entering the game room, then he sits at any game machine in the room, and starts with inserting cache into the build validator. So obviously, build validator validates the cache. If everything is fine, it gives a command to.  
Game machine, it grants credits, and player starts to play with an opportunity to top up any time through the same build validator. I need to mention here that, at this point, Flexport is, let's call it in an idle mode, displaying a message.  
With a saying, is a scan you or you will it? It's not an exact wording, but just an idea.  
Hello? Yes.

**  
Val Levitan** 1:49  
Sorry, sorry, sorry, please forgain the interruption. What build acceptors are used in the market?

**  
Andrei Klimovich** 1:58  
What bill acceptors are currently used in the market in Texas?

**  
Val Levitan** 2:01  
Yeah, what brand? Is it JCM or MAI?

**  
Andrei Klimovich** 2:04  
Uhh.  
I'm not sure really, I don't know details on this site.

**  
Juan Martinez** 2:13  
And JCM is more common in Las Vegas, so at least for the class 3 products, I would say that they have a casino-style bill except they're most likely a JCM.

**  
Andrei Klimovich** 2:27  
Yeah, it might be like...  
If they get these machines like a retired machines from different.  
Jurisdictions, they probably come with build validators already installed, so they do not do that on site.

**  
Val Levitan** 2:44  
Okay, I'm sorry for interruption. Go ahead.

**  
Andrei Klimovich** 2:46  
Okay, yeah. So, Flexport at this stage is in an idle mode, so it sends, displays a message, either scan your wallet or start a new game session by inputting cash. Exact, not exact wording, but just a message that you have two options.  
Either scan your wallet if you got one, or go and upload cash.  
So player plays, tops up any time, and at some point he decides to hit redeem. Redeem button is a part of electronic game machine, so it receives a message and sends a redeem comment to a flex port.  
where actually I came to decision that we would need a touch screen for our flex port. Because there is definitely a fork over here that it's either create new or update.  
Yeah, so otherwise it will not work. So basically if we are...

**  
Val Levitan** 3:51  
And, and there, and there you go, cost.

**  
Andrei Klimovich** 3:57  
Yeah.  
I mean, like, if we exclude the point that...  
Player should be able to create an e-wallet at the game machine. If we exclude it, we can go with a simplified port. But I don't think that we should exclude this value. It's really, really valuable. So as soon as we have this requirement, it requires a touchscreen.

**  
Juan Martinez** 4:19  
Absolutely.  
Yeah.

**  
Andrei Klimovich** 4:28  
Yes.

**  
Juan Martinez** 4:28  
Flexport today has a touch screen, so not a problem.

**  
Andrei Klimovich** 4:30  
Yeah, that's good, but I, again, like it just kills the previous assumptions that we can simplify it, make it cheaper, make it simpler. No, we need a touchscreen.  
So.  
Okay, JVL host receives a comment that we need to create a new e-wallet with redeemed balance. Player goes through touch screen confirmations that, yes, I would like to create a new one. Printer, which we are connected with, gets a comment from us to create a QR code.  
receipt with the e-wallet data. But when I say data, it's some general information we will figure out, but it does not contain a value. It doesn't contain the balance information. So as soon as the ticket is printed.  
Player takes the QR receipt, goes to another electronic game machine, and he decides to continue playing with the same balance. So he scans the QR code receipt. At this point.  
It's an idea like if we would like to offer a player a partial cache in option. So you're scanning a QR code, we know the balance, and you've got an option which is probably a default one, cache in all or just partial.  
question, what is it like?

**  
Juan Martinez** 5:58  
And I, I'm and I'm against partial cash in.

**  
Andrei Klimovich** 6:02  
Okay.

**  
Juan Martinez** 6:03  
Yeah, today your Tito ticket, you insert it, and the entire Tito ticket is consumed by the machine.

**  
Andrei Klimovich** 6:10  
Okay.

**  
Val Levitan** 6:10  
Boom!

**  
Juan Martinez** 6:10  
I know what, so I know customers have mentioned that feature to Felipe in Georgia, but I don't know what's driving that. You know, you always want the player's entire wallet poured into the machine. That's the dream scenario.

**  
Val Levitan** 6:12  
Game.

**  
Andrei Klimovich** 6:27  
Mhm.

**  
Juan Martinez** 6:27  
He can cash out at any time and either go to another machine or go to the cash out to go home.

**  
Val Levitan** 6:27  
Bing.  
And not only that, in your particular scenario, you must kill that QR code immediately.  
You must drain it and kill it at the same time. It's not valid, cannot be used again.  
In your scenario. In in the normal E wallet scenario, you don't, but in your particular scenario, you must kill it.

**  
Juan Martinez** 7:02  
In the scenario I described or what Andrei describes?

**  
Andrei Klimovich** 7:02  
K.

**  
Val Levitan** 7:03  
Okay.  
No, what Andrei is describing.  
You must kill the current QR code.  
A number.

**  
Andrei Klimovich** 7:16  
Why should I? Please explain.

**  
Val Levitan** 7:20  
You cannot let it circulate.  
You need to pretend that it was absorbed by the bill itself, just like the Tito scenario. It cannot circle it.  
It can only be used once in your scenario.  
And then it must be clear. It must be absolutely.  
Because if you start issuing another. QR code is going to be a running.

**  
Juan Martinez** 7:53  
No, but if we kill it, you have to issue another QR code when they cash out.

**  
Val Levitan** 7:58  
He does, he does. Every time look at his diagram, he does, because every machine has a has a printer and every time he presses cache out, that printer prints a new QR code.

**  
Juan Martinez** 8:06  
Mmh.

**  
Val Levitan** 8:12  
In in in in his scenario. In the e-wallet, in the normal e-wallet scenario that FlexPay was designed for. There is only one e-wallet.

**  
Andrei Klimovich** 8:13  
No, no.

**  
Val Levitan** 8:27  
that circulate the entire session.

**  
Juan Martinez** 8:31  
And I think that that's what we want to get to, correct, Andrei?

**  
Andrei Klimovich** 8:31  
What is the?  
Correct, and it's.

**  
Val Levitan** 8:34  
No, no, no. His point is that every machine has a printer, and every time.

**  
Juan Martinez** 8:41  
No, but remember that that point came from because they already have the printer.

**  
Val Levitan** 8:46  
I know, so I'm supporting him on that point. I'm not fighting him. His last statement yesterday was quite clever, which I like.  
You said that.  
The market.  
The footprint is already there.  
So, how he said, how do we utilize the current footprint with the least amount of?  
then.  
To the footprint.  
So, I found this, I found this statement yesterday is quite clever.

**  
Juan Martinez** 9:19  
Correct and.

**  
Val Levitan** 9:24  
So, I'm building on what you said yes.

**  
Juan Martinez** 9:27  
Yeah, but I think the unknown with his final statement was it would be ideal to not print out a QR code and use it like a wallet where you can just move with one ticket from machine to machine with added logic from Flexport.

**  
Andrei Klimovich** 9:28  
O.

**  
Val Levitan** 9:28  
Yeah.

**  
Juan Martinez** 10:07  
Is true.

**  
Val Levitan** 10:08  
If you hold on, I should believe me. I thought about it the whole night.  
If you do that, you have to kill the predecessor.  
Otherwise, you will have multiple tickets circulated, and you will never balance.  
So every time you present the ticket to a QR scan, you absorb the entire value of it, and the ticket becomes garbage. Rip it up and throw it away.  
Then when you finish playing, you print the printout, the payout ticket, that becomes your transporting ticket.  
You could transport it.  
to the counter or you could transport it to the next machine and present it to a QR scheme.  
This is, this is what he's going.  
This is what he's presenting for us.  
He, I mean, Andrew, but Andrei, I don't mean to be impolite, I'm just quickly driving through.

**  
Andrei Klimovich** 11:17  
No, no, actually, while the key point is here that as soon as we have a flex port with touch screen and the player performs redeem action over here, we can ask him an option if you'd like to create a new e-wallet or update an existing one.

**  
Val Levitan** 11:38  
Okay, look, I understand where you're going with it. But

**  
Juan Martinez** 11:49  
The more I thought about it too, that introduces a delay into the process where the player has to make a decision that they don't have to make today.

**  
Val Levitan** 11:58  
No, no.  
Not not only the not only a delay. OK, let's say we can cope with the delay, but it.  
It creates a question, a hesitation, an interpretation.  
It just it creates a bunch of things that are not good for gambling.  
And not good for processing.

**  
Juan Martinez** 12:26  
If you kill that QR code once it's scanned, that mimics what a Tito ticket does. And I think it's easier for us to properly reconcile. This ticket went into machine number one. It is now redeemed and no longer valid. And when the player cashed out from machine number one,

**  
Val Levitan** 12:34  
Yes.

**  
Juan Martinez** 12:45  
This is the new ticket with a new value, new time stamp that is live.

**  
Andrei Klimovich** 12:56  
Um...  
So, if we print out a ticket each time when you redeem.  
Do we really need any touchscreen over here?  
I don't feel like...

**  
Val Levitan** 13:14  
On.  
Okay, yes, yes, okay, good point.  
Maybe, yes, maybe not.  
But you need a screen.

**  
Andrei Klimovich** 13:31  
Yes, of course, you need a screen.

**  
Val Levitan** 13:36  
Then, it's margin, whether you have the touch.

**  
Andrei Klimovich** 13:42  
Val.

**  
Juan Martinez** 13:44  
Yeah, because it's not just a player device. I think the screen is also used during setup of the port.

**  
Val Levitan** 13:52  
Not only that, but you need to communicate to the player.

**  
Andrei Klimovich** 13:55  
Of course, yeah, I need the screen as a question if it should be touched or not, so...

**  
Val Levitan** 14:00  
And now please, please consider that you you're removing the printer out of its nested location. And you rerouting it into the flex port.  
So, whatever instructions flow in the machine, you're taking it all, and you need to communicate that.  
And, and the screen, the screen and the touch screen becomes your only means of communication configuration.  
Set up and everything else, but otherwise you're...  
Can't really do it.

**  
Andrei Klimovich** 14:46  
So, it's a really, really important fork here, like what you said.

**  
Val Levitan** 14:49  
And uh, and I'm sorry, Andrei, just to uh go back for a second.  
Ahh.  
You have a host, right? So you have an IQ in the location, plus you have a cloud host, right?

**  
Andrei Klimovich** 15:04  
Mhm.  
Correct.

**  
Val Levitan** 15:07  
Let's call it Tito server.  
or let's call it instead of Tito server, ticket server.

**  
Andrei Klimovich** 15:17  
Okay.

**  
Val Levitan** 15:18  
So, so we just don't get confused.  
But it's a it's a post.  
You must have it, otherwise you're going to have a massive fraud. I think they have massive fraud right now.

**  
Juan Martinez** 15:33  
Yeah.

**  
Andrei Klimovich** 15:33  
Yeah, yeah, of course. Anything works with host only. Like if there is no host, it doesn't work, obviously. So.

**  
Val Levitan** 15:40  
Okay, so, so in order for you to have a host, it's connected to where?

**  
Andrei Klimovich** 15:41  
Mhm.

**  
Val Levitan** 15:47  
It's connected to what to the IQ, right?

**  
Andrei Klimovich** 15:50  
It's connected to IQ, correct? And IQ is connected to a hub where each single flex port is connected.

**  
Val Levitan** 15:53  
Slope.  
Exactly, exactly. Connected how?

**  
Andrei Klimovich** 16:03  
So, uh, Flexport, they're using some kind of Ethernet that goes to a hub.

**  
Juan Martinez** 16:04  
Ohh.

**  
Val Levitan** 16:12  
Correct, so it's connected by a wire.

**  
Andrei Klimovich** 16:15  
Mm-hmm.

**  
Val Levitan** 16:16  
So, you need to wire the location.

**  
Andrei Klimovich** 16:19  
Of course.

**  
Juan Martinez** 16:19  
Yes.

**  
Val Levitan** 16:21  
Ohh.

**  
Andrei Klimovich** 16:26  
So my, just, let's touch this point over here again, because it's a really important fork in logic over here. Like, what you say is that we do not need to offer a player a choice. Would you like to create a new e-wallet or update an existing one?  
So, you are...

**  
Val Levitan** 16:47  
No, no, I'm saying that it's wrong to offer a choice.

**  
Juan Martinez** 16:55  
Yeah. And today they don't have a choice and why change the player methodology when we can consume the QR code ticket and create a new one on CashOut, which is how they know the flow today.

**  
Val Levitan** 16:56  
I'm not.

**  
Andrei Klimovich** 17:09  
Yeah, I mean.  
It's it's it simplifies everything; it simplifies it a lot, the only.  
Let's say disadvantage of this solution, which is probably minimal, is that we are...  
keep using the same amount of paper as they use nowadays. So we are not saving any maintenance efforts, we are not saving any costs over here, but probably this is so minimal that it doesn't really have a value.

**  
Juan Martinez** 17:43  
Yeah.  
Yes, this roll paper that's used by the pyramids is extremely inexpensive compared to true Tito tickets.

**  
Andrei Klimovich** 17:54  
OK, so if we agree on that, it definitely simplifies everything. We can, I will review this flow and it will be much easier, so...  
Okay.  
So now we have...  
We have our QR receipt with...  
scan it with a new machine and the e-wallet is totally consumed, so there is no partial caching, obviously. So it works very straightforward here. And one more point to mention here that actually if by some reason you have more than one.  
e-wallets, you can all cash in them one by one without any problem, because Flexport itself is stateless. So it just works as a transaction of states. So once the ticket is scanned, it gets its value from host, and this value is being transferred to the machine right away.  
And that's it. There is no intermediate state here.  
Then it, it's all quite simple here, so he performs a redemption again, redeem.  
What we do, like it changes everything, we print a new ticket again.  
Then he goes to...  
Um...  
to a counter where the IQ is located, right?  
So we're excluding a huge piece of logic over here, so we don't need this loop for updating the E-balance, et cetera. So, okay. So player presents this QR receipts as the last one he has to a cashier. Cashier scans it.  
With IQ with optical reader, IQ reads the e-wallet and...  
Sorry, schedule the QR code, sends the information to a host. Host returns e-wallet status with a balance. IQ displays it on the screen for a cashier. And this response contains basic information on the wallet, just something, but the main part is the balance itself. So it's actually the payout amount.  
So, what the cashier is doing? He goes, she he opens the bank.  
Accounts the amount of cash, handles it to a player.  
So now the player can leave the game room. He has a cash in his hands. But the next step for cashier is to...  
Update the this transaction as paid out, so he taps the screen. We need this action from his from him, and this comment updates the e-wallet on host side, so it marks it as paid out or voided.  
And the play is a it discards the QR receipt.

**  
Juan Martinez** 21:08  
Open.  
Why do you believe we need a manual acknowledgement that the ticket was paid?

**  
Andrei Klimovich** 21:19  
Because we need to void it somehow in the system, unless if we don't do that, the e-wallet will contain a balance on it.

**  
Juan Martinez** 21:28  
Right, but can't the process of scanning the ticket and before you pay the player or as you're paying the player, you just hit paid. Is that what you mean?

**  
Andrei Klimovich** 21:29  
It.  
You can do that in this way, but in this, yeah, I know, but in this case, you don't have an option to cancel the payout. I don't know, by some reason, he decided to go back to the game machine.

**  
Juan Martinez** 21:39  
They should be in separate process.

**  
Andrei Klimovich** 21:52  
Or again, like if you'd like to make it simpler, we can do that. In this case, there is no need in manual confirmation. You're right.

**  
Juan Martinez** 22:00  
Yeah, because I would say if once you pay him, he can go back to the machine. He doesn't need the ticket. He needs his cash.

**  
Andrei Klimovich** 22:08  
Yeah, you're right, so we can simplify it. That's a good point.

**  
Juan Martinez** 22:10  
Yeah.  
Be perfect.

**  
Andrei Klimovich** 22:12  
So, scan on the IQ side equals, by the way, just a real void as we do it on game machine side.

**  
Juan Martinez** 22:23  
Well, I would still say that there should be a button that says pay or paid that the employee does have to do following the scan. The scan produces the amount of confirmation, and then you press a button, paid or close, and then you pay the player.

**  
Andrei Klimovich** 22:42  
But it's exactly what I described initially, but as far as I understand you, you suggest that by the moment when you scan a scan a ticket.

**  
Juan Martinez** 22:50  
No, no, no, because the scanning, there may be an incorrect amount, there may be a dispute, or that's not my ticket. Yeah, you definitely want that button to be pressed, but it's part of the one single process.

**  
Andrei Klimovich** 22:56  
Correct, yeah, yeah.  
Yeah, it's exactly how it's described here. So you see, like after the cashier scans the QR code.

**  
Juan Martinez** 23:08  
Okay.

**  
Andrei Klimovich** 23:13  
Right, the Flex IQ screen is updated with information, but at this point, Flex IQ is waiting for cashier action.  
So the paid out or redeemed button should be pressed by the cashier. Only by this action we really void this e-wallet. Until then, until then, then there is no status change. There is just a display of the current status.

**  
Juan Martinez** 23:32  
Yes.  
Yep.  
Yes. Great.

**  
Andrei Klimovich** 23:45  
Okay, so no changes here, good. The only fork over here, like if you would like to offer a partial redemption, but if we are avoiding...

**  
Val Levitan** 23:56  
We were, we were, we won't. We're all not. It's a it's a long moment.

**  
Juan Martinez** 23:57  
I want to do that.

**  
Andrei Klimovich** 23:59  
Yes, yes.  
Yes, right, so no partial redemption.  
So.

**  
Val Levitan** 24:07  
It's really, it's really the bad part.

**  
Andrei Klimovich** 24:14  
Okay.  
So with this approach, it's really simple and straightforward. And in case if your wallet is created on IQ side, there will be a special separate interface on IQ where the person comes to a cashier and says, I'd like to create an account to play your games.  
He handles cash, the cashier goes into IQ interface, there is like a create new whatever, tabs, inputs the amount manually, and IQ sends this information to host. Host creates e-wallet with a required balance.  
returns the confirmation, and IQ sends a common to connected printer, which will be a really simple printer, just exactly the same as installed on game machines. And we got a QR ticket printed. So  
The player gets this ticket and he goes to machines, and then we this circle.  
Repeats, and it's the same with recycler.  
So...  
With recycler, it's a self-service, so there is no need in cashier. So the player cashes in, inserts bills into recycler. Recycler communicates to a host to create a new wallet, receives a reply, and prints out a QR ticket.  
So the starting point is then player goes to game machine. It's a closed circle, the complete loop of the complete ecosystem, I would say. The only thing that if there is a dispenser, not a recycler, dispenser, dispenser.  
will not provide an option to create an e-wallet, but it will provide an option to redeem e-wallet.

**  
Val Levitan** 26:16  
Not going up.

**  
Andrei Klimovich** 26:19  
Sorry.

**  
Val Levitan** 26:20  
No, no, it will not, it will not.

**  
Juan Martinez** 26:22  
Val, yeah, for some reason you sound like you're really far away from your microphone and I could barely hear you.

**  
Val Levitan** 26:29  
I'm sorry, can you hear me now?

**  
Andrei Klimovich** 26:31  
Yes.

**  
Juan Martinez** 26:31  
A little better, but yeah.

**  
Andrei Klimovich** 26:38  
So, with this approach, uh...

**  
Val Levitan** 26:38  
Ivan.

**  
Andrei Klimovich** 26:42  
It looks quite.

**  
Val Levitan** 26:42  
You, it will not, it will not create, it will not create, you won't be able to use it in the dispenser.  
I mean, if it's if it's our dispenser, you'll be able to use it, but if it's not our dispenser, you will not be able to use it.

**  
Andrei Klimovich** 27:01  
You will not be able to use it to redeem.

**  
Val Levitan** 27:04  
Already?

**  
Andrei Klimovich** 27:05  
Oh.

**  
Val Levitan** 27:07  
In the dispenser, in the dispenser.

**  
Andrei Klimovich** 27:07  
Yeah.  
Correct, in a in a simple.

**  
Juan Martinez** 27:13  
But can you clarify, Andrei, are you talking about a JVL dispenser or an existing dispenser?

**  
Andrei Klimovich** 27:19  
So if it's a JVL dispenser, it's 100% that it should be integrated in this ecosystem and it should work with our e-wallets. When it comes to third-party dispensers, it's a different story. And there is a slight opportunity. We have never discussed it with anyone, but it might be an opportunity that they will agree.  
To open us a gate.  
To their dispenser, so we'll send them a comment.

**  
Val Levitan** 27:43  
They will not, they, they, they will not do it.

**  
Juan Martinez** 27:44  
Yeah, yeah, they won't do that, yeah.

**  
Andrei Klimovich** 27:46  
Of course, I mean, like, we haven't had those conversations, but it's...  
out of the table right now.

**  
Juan Martinez** 27:52  
Yeah.  
Yeah, because the location might own it, but the technology belongs to Vanilla Pace, a competitor of ours, and they won't open that up. That's, while that's common practice in the casino world, I can't see those guys doing that.

**  
Andrei Klimovich** 28:10  
Yeah, so the low hanging fruit for us are those game rooms that do not have a dispenser, that do not have a kiosk. They are fully manual and there are quite a lot of them.

**  
Juan Martinez** 28:23  
That's good news.

**  
Andrei Klimovich** 28:34  
There are some edge cases, like minimal payout, but as far as I understand, it's being controlled by the game machine itself.  
like the minimal redemption, sorry, the minimal redemption requirement. So you cannot redeem less than 20 bucks, for example. There were a couple locations like that. But it is not something that we need to manage on our side.  
What do you think? Like, it should be blocked by game machine itself. So it was a total balance right now is less than 20 bucks and you hit redeem. The machine itself should not.  
Launch the redeem.  
Operation.

**  
Juan Martinez** 29:23  
But is that what they do? The money stays on the machine? You cannot cash it out if it's less than $20? Or do they deal with that at the time of redemption at the window?  
Because...

**  
Andrei Klimovich** 29:38  
Being honest with you, I haven't seen automatic redemption control over here. Like, there were no case when I hit redeem and the machine told me that the minimal payout is 20 bucks.

**  
Juan Martinez** 29:52  
Yeah, because that's complicated. Every manufacturer would have to comply with that in their game software, which the used games that they bought from Vegas, you can't modify those. You're not even supposed to have them in Texas as an example. So there can't be game level automatic control.

**  
Andrei Klimovich** 29:52  
Yes.

**  
Juan Martinez** 30:25  
Yeah.  
Right, yeah.

**  
Andrei Klimovich** 30:32  
And another really specific requirement, well, it's not a requirement, but it's something that they do is so-called match, like we've touched it with Felipe. So basically the mechanics is that you input 10 bugs and the location is doing the same, 10 more.  
And the agreement is that the minimal redemption is at least $20 or $40, whatever you agree on that with the location. But again, it's not something that we can and we shall handle on our side. It's just.  
if they'd like to do it with our e-wallet system in a place. So it may work in a really simple way. Like you use your e-wallet and she comes in and inserts additional cash from their side through the bill validator and that's it. That's the match.

**  
Juan Martinez** 31:31  
But we don't know how it's being done today by the competition.

**  
Andrei Klimovich** 31:37  
Yeah, it was very simple. Like I said, let's match. She said, okay, these machines are part of this match. Other machines, they do not participate. So I picked up one of those machines and she said a minimal match bet is $20. So I said, okay, so Ivan put it my $20 and she inputted her $20.

**  
Juan Martinez** 31:56  
Oh, okay, okay. So it is fully manual. Okay.

**  
Andrei Klimovich** 31:59  
Yeah.

**  
Val Levitan** 32:00  
Can you, can you hear me?

**  
Juan Martinez** 32:03  
Yes.

**  
Andrei Klimovich** 32:03  
Yes.

**  
Val Levitan** 32:04  
Better now.

**  
Juan Martinez** 32:07  
A little better.

**  
Andrei Klimovich** 32:08  
Sounds like yes.

**  
Val Levitan** 32:11  
So when I speak, can you hear me?

**  
Andrei Klimovich** 32:13  
Yes.

**  
Juan Martinez** 32:13  
Yeah.

**  
Val Levitan** 32:15  
Okay.

**  
Andrei Klimovich** 32:22  
So.

**  
Val Levitan** 32:22  
I, I, I didn't catch that $20 match.  
Can you repeat that, please?

**  
Andrei Klimovich** 32:30  
Yeah, it's just the mechanics they have over there in Texas, where the allocation offers you a bet. Like if you invest as a player, you invest $20, the allocation will support you with another $20 in top. And you input those $40 into a specific machine.  
and you stop playing it. But the rule is that the minimal redemption is 40, 50, whatever. So you're forced to play until you get the agreed redemption minimum.  
Or you just lose your $20.

**  
Juan Martinez** 33:16  
But so if I have $20 on the credit meter, I just need to insert another $20 to get to the 40 and then press cash out.

**  
Andrei Klimovich** 33:25  
That's right, that was the first idea that I got in my head, but I decided not to do that. Just like, but honestly, it should work.

**  
Juan Martinez** 33:30  
Yeah.

**  
Andrei Klimovich** 33:36  
In this way, so you basically get the $20 in this way.

**  
Juan Martinez** 33:39  
But.

**  
Val Levitan** 33:43  
The normal way to do it is the promo credits that go in SAS mirror as promo credit.

**  
Juan Martinez** 33:50  
Yeah.

**  
Andrei Klimovich** 33:51  
Yeah, but it's not in place at all. There's nothing like that. And it's a good point.

**  
Val Levitan** 33:56  
Well, it's wonderful. It's like I said, you know, to salespeople go to India.

**  
Juan Martinez** 34:03  
OK, thank you.

**  
Val Levitan** 34:03  
You know, people don't wear any shoes. Perfect opportunity.

**  
Andrei Klimovich** 34:09  
And.

**  
Val Levitan** 34:10  
To me, it sounds like paradise.

**  
Andrei Klimovich** 34:17  
Yeah, of course. I mean, like, for the opportunity in the market is huge. It's definitely like that.

**  
Val Levitan** 34:24  
Let's discuss something else. Let's take a couple of steps back. Let's pretend to erase this board. Let's just discuss something.

**  
Andrei Klimovich** 34:34  
Okay.

**  
Val Levitan** 34:37  
Okay, so...  
We walk into a location.  
And location is equipped with...  
The printer and the bill acceptor.  
And the printer is.  
is a QR code printer and you take this QR code and you go to the counter and you can redeem your win.  
So, we know that you could duplicate this, and there are no checks.  
But are we saying that we can read this QR code or are we saying that right now we don't know whether we can read it or not?  
Or right now we're saying we cannot read it.

**  
Juan Martinez** 35:22  
No.  
We're saying that we don't know, but that the intention is to replace the QR code. The source data now comes from JVL. So the QR code will be commanded to be printed by JVL, and JVL owns the data of the QR code.

**  
Val Levitan** 35:27  
Yeah.

**  
Juan Martinez** 35:48  
That's the end goal.

**  
Val Levitan** 35:51  
Okay, so how are we going to overcome aside from cost of bill of material?  
How are we going to overcome?  
The installation.  
job, the wiring job. So there are 25 machines and locations. How are we going to wire it up?

**  
Juan Martinez** 36:14  
My guess is they're probably, at least in those larger game rooms, they have to be wired today of some sort, but that's part of the entire setup. You know, the customer normally supplies the networking cables because every bank  
is a different size known to them, not known to us. We give them a specification. Perhaps we provide the network switch or switches, or we provide the specifications for them to buy. But I can tell you in the casino world, Val, and I've had both Val and IGT systems,  
The networking equipment is on the onus of the casino, not the system supplier.

**  
Andrei Klimovich** 37:00  
Mhm.

**  
Juan Martinez** 37:00  
They work with you to tell you what's needed, and then you go out and get it and buy it.

**  
Andrei Klimovich** 37:08  
Mhm.

**  
Juan Martinez** 37:09  
Now, do we want to offer it because these guys don't even have an IT department? Certainly a possibility.

**  
Andrei Klimovich** 37:18  
It's a good point, like I feel like they should have some kind of IT department or at least a technician who sets up everything because they already have it in place. But it will be a nice service if you can provide everything, like if we can.  
calculate it and say, okay, here is a...

**  
Val Levitan** 37:35  
This is a, this is a swamp.  
We're going to drown on this one.

**  
Andrei Klimovich** 37:43  
Ohh...

**  
Juan Martinez** 37:43  
Yeah, yeah, that's why I would say we provide a detailed network diagram of what's needed and that they know their casino, they know the distances, they know the bank sizes, and that they, that is something they buy. You know, obviously network cables are cheap, they're available everywhere.  
Same thing with the network switch. I mean, it's not overly complicated as long as we guide them on what's needed rather than supplying it. For a smaller setup, we could, but, you know, this larger game rooms with, you know, north of 50 games, they probably would want to do that and own it and maintain it themselves.

**  
Andrei Klimovich** 38:26  
With the pilot release, when we say about the test release, which is potentially free for customers, it will be easier for us to do everything on our side, just to make sure that it happens quicker and promptly. If we will expect them to prepare everything, it may take some time.

**  
Juan Martinez** 38:35  
Yeah.  
Agreed.

**  
Andrei Klimovich** 38:45  
Quite some time.

**  
Juan Martinez** 38:47  
Yeah, no, I would say that the deal there is that they purchased the equipment that we supplied after a successful trial. But I agree with that statement that yes, we don't want to count on them for a go live for the trial portions.

**  
Andrei Klimovich** 39:22  
Can we discuss the financial part of this? Like, obviously, there is a hardware sale or lease part, but do we consider any fees, any...  
I don't know, revenue share, et cetera, any additional source of income for JVL in this model.

**  
Juan Martinez** 39:48  
My only, the simple answer would be I think so, but because of the grayness of this market, you know, I don't know what legal repercussions we have if, you know, 60 days into the trial, the machines disappear, you know,  
Can we even legally go after somebody in this great business? I don't know.  
So subscription models we talked about, and yes, that makes complete sense. But, you know, longer term extended payments, I think Val you would agree that it's just risky. You know, maybe with a trusted Georgia operator, we could, but  
I, I, I just don't know.

**  
Andrei Klimovich** 40:42  
And what is your vision of a subscription model? How do you see it right now?

**  
Juan Martinez** 40:48  
Oh, we were talking about...

**  
Val Levitan** 40:48  
For which market?

**  
Juan Martinez** 40:51  
This is for Texas, I guess, as an example for Texas.

**  
Andrei Klimovich** 40:51  
Sorry.

**  
Juan Martinez** 40:56  
where, you know, if they want reporting, expanded reporting from the FlexIQ network, that could be paid through flat daily fees.  
If you just want the system, here it is. If you want expanded reporting, here's plan A. If you want better reporting, here's plan B. If you want it all, here's plan C. Those are just possibilities.

**  
Andrei Klimovich** 41:41  
Just like another idea, I don't know. So we may charge them a certain percentage for either cash in or cash out serviced. They will never agree for that. Okay.

**  
Val Levitan** 41:53  
Never.

**  
Andrei Klimovich** 41:56  
So, it's a flat view.

**  
Val Levitan** 41:56  
You have to, you have to, you have to stay out of their business.

**  
Andrei Klimovich** 42:01  
Yeah.  
So, if it's a setup of IQ and flex ports.  
One source of income for JVL is just hardware itself, maybe service for installation if you would like to do that, but probably not. And then you say that it's like a flat fee for...  
For additional services.  
So redemption, all this cycle is included with hardware, obviously, but reporting.  
Mm.

**  
Juan Martinez** 42:45  
That there might be a basic set, the minimum required for them to operate reporting, but you know, now that port is connected to the machines, we can also do basic slot performance, which they may or may not have today.

**  
Andrei Klimovich** 43:06  
Well, yeah, so basic report is just money in, money out to compare it and to see, maybe to track different cashier shifts and make sure that reported bank amounts since the very beginning of shift, end of shift, correlates with money actually redeemed, etc.  
It's something basic, but additionally we can split it by game, by yeah, game machines to see.

**  
Juan Martinez** 43:34  
Yeah.  
And I don't, I never envisioned us having access to their bank amount. Because that does put a little bit more liability on us.  
you know, to do reconciliation, counting on a human person saying, yes, I loaded $5,000 in this drawer. You know, I thought it would be offline reconciliation. You guys know what's in your bank. Here's what we say went in and out and should equal what's in your bank.

**  
Andrei Klimovich** 44:05  
Yeah, so my suggestion is that we can offer this option over there in the IQ. So they may not use it if they don't want to, but if they agree, it will give them additional leverage to reconcile.

**  
Juan Martinez** 44:19  
Yep.

**  
Andrei Klimovich** 44:20  
What is our responsibility here? We are just writing down the numbers that are being input by the cashiers. That's it.

**  
Juan Martinez** 44:30  
Yeah.

**  
Val Levitan** 44:42  
I'm having a difficult time with all of this.  
I don't understand how to wire up the location.

**  
Juan Martinez** 44:53  
I have diagrams from the casino. It's the same thing. You know, wherever the network switch is going to sit, there's just an Ethernet run.  
from each machine, from each port to this network switch. And if it's one of these larger game rooms, then most likely every bank will have a network switch from as small as five ports to a 10 or 20 port type of switch, depending on the bank size.  
A couple of the drawings that are pictures Felipe posted, I can tell they're running power and data down poles from the ceiling since they didn't want to cut into the floor. So there is some sort of connectivity going to banks now.

**  
Andrei Klimovich** 45:45  
That's true.

**  
Val Levitan** 45:55  
No, I no, I understand. I understand the.  
the mechanics of installation. I just don't understand.

**  
Juan Martinez** 46:04  
Room.

**  
Val Levitan** 46:11  
how to physically sell it.  
The machines are somebody's machines, right?

**  
Juan Martinez** 46:24  
Yes.

**  
Val Levitan** 46:26  
So.  
And, and some of the machines might be on on participation.

**  
Juan Martinez** 46:36  
Yes.

**  
Val Levitan** 46:37  
So it's a guy like Rich, for example.

**  
Juan Martinez** 46:41  
Mhm.

**  
Val Levitan** 46:41  
Rich would have to come in and wire up his machines.

**  
Juan Martinez** 46:46  
Yes.

**  
Val Levitan** 46:47  
And it could be a couple of guys in the locations that...  
Ohh.

**  
Juan Martinez** 46:59  
I would argue, Val, that if you, you know, judging by the size of these operations based on those pictures, these guys have to have a handful of techs and plugging in a network cable to a switch is child's play for somebody who repairs machines on a daily basis.  
I don't think it would be too complicated. But yeah, unless the location does not have a partnership with an operator, it is the operator that we would be pitching this whole concept to, because it is their machines most likely, if there's any on rev share.  
or participation.

**  
Andrei Klimovich** 47:43  
But how do you plan the flex port itself to be installed in the game machine? It should be done by someone.  
So, it's probably one of those technicians, or so if they can install a flex port, they can, obviously, they can plug in Ethernet cable.  
without any issues over there. But again, I don't know all the details and I don't have this experience, but I feel like it could be a great service package. Like if you'd like us to come and install Flexports and connect them with Ethernet, we can do that.  
Here's the price.  
And I can imagine some operators, they would prefer to buy it from us, because it's our product, and we will integrate it better than anyone, other than teach their technician how to do that and spend some time on that.

**  
Juan Martinez** 48:34  
Mmh.  
Problem is, right now there is no us to install it.

**  
Andrei Klimovich** 48:58  
Yeah, sorry if it's something that I don't see the whole picture, but if we will...  
If we will charge them for this service equivalent of time to hire a higher person, so it should be it shouldn't be a problem, like...

**  
Juan Martinez** 49:16  
Yeah.

**  
Andrei Klimovich** 49:29  
And Sebastian is going to move to Texas, so this can be Sebastian, for example.

**  
Juan Martinez** 49:36  
Yeah, but like, I mean, if you landed one large game room with 100 machines, I mean, that's multi-day work if it's only one person.

**  
Andrei Klimovich** 49:51  
Well, I would say that I would be happy if we will face this problem.

**  
Juan Martinez** 49:56  
I agree with you.

**  
Val Levitan** 50:08  
It's a large commitment for an operator.  
To wire up the Room to install.

**  
Andrei Klimovich** 50:13  
It is.

**  
Val Levitan** 50:18  
Uh, ports.

**  
Juan Martinez** 50:20  
Yeah, but Val, this is a...  
The only thing that has changed here is the potential size of the project. But if we were going to pitch FlexPay in ports in a Georgia gas station with five machines, it still does similar components, just on a larger scale. It was going to have to happen anyway.

**  
Val Levitan** 50:44  
Well, I'm not sure that I agree, because Georgia is all wired up already. We don't have to wire anything. We just come in and we wedge ourselves between Mo the Goose.  
And, uh, and uh, the printers.

**  
Juan Martinez** 51:04  
Yeah, but if we talked about having flex pay and flex port as a possible option in Georgia, and obviously flex port would need to be wired, and that is not serial, it's Ethernet, and those wires don't exist today.

**  
Val Levitan** 51:04  
Yeah.  
And I agree, but in those cases, you deal with one particular operator.

**  
Juan Martinez** 51:24  
Yeah.

**  
Val Levitan** 51:25  
In Texas, I am not sure who you deal with, and I have not.  
Gotten my bearings yet?

**  
Juan Martinez** 51:33  
Right, right. And that's the unknown for me too, Andrei, is that the owner of Billy Bob's BBQ Restaurant go to Vegas, buy machines and do it himself? Or is there an operator that he's sharing revenue with who did all the work on his behalf?  
and they know what they're doing. That's the unknown.

**  
Andrei Klimovich** 51:56  
It's an unknown. There were a couple of operators we talked to at the expo and they mentioned that they have a location. I didn't ask them explicitly, like, do you own a location?

**  
Juan Martinez** 52:10  
Right.

**  
Andrei Klimovich** 52:11  
But they used words telling that I have a location here and there, and here is the setup. This is the kind of machines I have. But yes, I don't know this information yet. Hopefully, while talking to them again, in more details, we will get a clearer picture. But it's just 10 operators right now, so it's not the whole.

**  
Juan Martinez** 52:20  
Yeah.  
Sure, sure.

**  
Andrei Klimovich** 52:33  
So, whole state.  
Do I understand it correctly that a potential bottleneck or an issue might be a location where there was a couple of operators? And we definitely, I think that we've seen locations where there are machines provided, it looked like it was provided by different operators because...  
There was a bank of machines.  
which was serviced by one type of kiosk, and there was another bank of the machines, which was serviced by another type of kiosks. And it was explicitly said that those machines, they can be cashed out only here, these machines can be cashed out over there.

**  
Juan Martinez** 53:06  
Oh.  
And.  
Yeah, that means the one set of machines has supported SAS and the older ones did not, hence the different incompatibility there. Very interesting.

**  
Val Levitan** 53:19  
Yeah.

**  
Juan Martinez** 53:28  
Wow, this is the wild of W.

**  
Val Levitan** 53:34  
So it's crazy opportunity. I mean, the opportunity is endless. I just really don't know how to tackle this.

**  
Juan Martinez** 53:37  
Yeah.

**  
Val Levitan** 53:42  
Very, very, very interesting.

**  
Andrei Klimovich** 53:46  
So, if we will...

**  
Val Levitan** 53:47  
Alert, I don't know which way to move.

**  
Andrei Klimovich** 53:51  
Again, like...

**  
Val Levitan** 53:51  
Can you, can you hear me?

**  
Juan Martinez** 53:53  
Yeah.

**  
Andrei Klimovich** 53:53  
Yes, yes. My feeling is that we are moving in a proper direction with approaching game rooms instead of guest stations. It's the first step we are doing here. And secondly, I think that is the right decision for us is to move with those game rooms with.  
which don't have any solution in place, which is fully manual.  
Again, I might be mistaken, but I feel like it's a low-hanging fruit for us to test this approach, to test the whole ecosystem.

**  
Juan Martinez** 54:28  
Sure.  
Yeah, to start with the smaller, fully manual locations. Yeah.  
I have all my old budgets for all my old Hard Rock projects, so I can certainly carve out the IT section just to start putting some numbers on a piece of paper so we get an idea. And granted, you know, these numbers are slightly elevated because IT was always trying to get more money than they needed for every project.  
but just as a talking point.  
so we can see what all is involved.  
Good can of worms you opened up, Andrei.

**  
Andrei Klimovich** 55:37  
Scism.

**  
Juan Martinez** 55:38  
I said a good can of worms that you've opened up. This is a...  
It's just potentially huge, but it is a daunting task.

**  
Andrei Klimovich** 55:49  
Hmm.  
Maybe we shall just start, not start, continue talking to operators. So now we have, I have much more clear vision of what we can offer, how it may work. I can tell them the beautiful story of how the experience will change and what kind of advantages they will get. And  
I will ask them more specific questions about their setups, if they see any locations where we can try out this approach, etc. And again, like it's, they will ask questions about cost for sure, but I think that I will be able to avoid them for now.  
Kiss.  
We need to, as far as understand, that the problem is that we are missing some pieces of information to make a final decision, but...  
The question is...  
If tomorrow I have a call with operator who says, okay, I have a location for 20 machines, which is fully manual, let's try your Flexport plus IQ approach. I'm ready to go. What stops us? Like what kind of?

**  
Val Levitan** 57:04  
We don't have, we don't have the host.

**  
Andrei Klimovich** 57:09  
Yeah, technically, IQ cannot work with ports either, right? So it needs to be upgraded for sure. But I mean, like, if we...

**  
Val Levitan** 57:16  
No, no, no, I mean IQ does not work with ports and we don't have a host to connect the IQ to, so we cannot, we cannot have an issue validation number.

**  
Andrei Klimovich** 57:24  
Yeah.

**  
Juan Martinez** 57:28  
Right, yeah.

**  
Val Levitan** 57:28  
And, and we also don't have the reconciliation piece, the the accounting piece.

**  
Andrei Klimovich** 57:35  
Correct, I mean, yeah, sure.

**  
Val Levitan** 57:36  
So, we, we don't have a lot, we don't have a lot of things, and...

**  
Juan Martinez** 57:40  
And we need to map out, we need to basically create a bill of materials based on five machines, 10 machines, 20 machines, so that we internally know what you could pitch to the customer, because you mentioned a 20 machine location. Well, that's 20 network cables of assorted lengths.  
It could be one, it could be 3 network switches, depending on how the machines are broken out. What are those cost? Does he want to buy them? Does he want to buy them from us? That helps us understand that picture.

**  
Val Levitan** 58:11  
What are the distances? I mean, who's going to install it? Which machines? I'm not even sure whether machines could be wired correctly. For example, we have one machine from Georgia that just doesn't wire up to, the port doesn't wire up to.

**  
Juan Martinez** 58:14  
Yeah.  
Right, yeah.

**  
Andrei Klimovich** 58:31  
OK, yeah, I understand it, like you're moving into the direction of a detailed offer, something that can really be signed and paid.

**  
Val Levitan** 58:32  
Ohh.  
Well, the first, well, the first thing you're going to be asked is how much. That's, you're not going to, you're not going to escape the answer, right? So, and even at the end of our conversation yesterday, you asked me what the price is. So you're going to be asked the same thing.

**  
Juan Martinez** 58:45  
Yeah.

**  
Andrei Klimovich** 58:49  
Of course, yeah, but...

**  
Juan Martinez** 58:57  
Yeah.

**  
Andrei Klimovich** 58:58  
I, I, I don't understand it, but...

**  
Juan Martinez** 58:59  
And the document you're talking about is for us to sign off on, not the customer, because we're not ready for the customer yet.

**  
Andrei Klimovich** 59:06  
Yeah, but from product point of view, I feel like we're missing a very important decision here. Like, do we believe in this solution that we've just discussed with you? And are we ready to start implementing it? Or before making the decisions that yes, let's invest time and money into implementing it,  
let's get more information. And my feeling is it will be really nice to check out this, to compare this solution against market interest. And the only way to do that is just to talk to operators.  
And of course, they will ask questions about money, but I guess that we can just dance around, say, yeah, here is a ballpark, but we are still working on that. But the solution needs to be validated. Or there is another approach. Like we agree that we believe in this approach.  
and we start implementing it, and as soon as it is ready, we just go to the market, but it might be an unpleasant surprise over there.

**  
Juan Martinez** 1:00:09  
I know that. We may not recover from a surprise like that. I mean, we, you can't jump from, we definitely believe in it. We can't jump to implementing it without making sure we've walked all of the processes in between before implementation.

**  
Andrei Klimovich** 1:00:27  
Like what? What kind of processes?

**  
Juan Martinez** 1:00:30  
Hey, the network cables, who's buying them? How much are they? Are we using a TP-Link? Are we using a Cisco network switch? Is the switch unmanaged? If the casino has their own networking equipment, you know, they may insist we use HP brand equipment. There's all of these scenarios that I've run into.  
over the years that may come up. We may run into a customer, what is a switch? I have no idea what you're talking about.

**  
Val Levitan** 1:00:55  
I just...  
I just had a crazy idea.

**  
Juan Martinez** 1:00:59  
Mm.

**  
Val Levitan** 1:01:03  
Yesterday, well, not yesterday, a couple of days ago, I discussed with our engineers.  
A possible solution of...  
You know how bill acceptors, well, Juan, you will know, right? Andrei doesn't know, but it's good for him to know. But for sure, Juan, you know that when you buy bill acceptors, you buy the nozzle separately.

**  
Juan Martinez** 1:01:30  
Yeah.

**  
Val Levitan** 1:01:32  
And the nozzle comes, it's kind of a pairing nozzle, right? It fits into the bill acceptor with exactly like grooves like this.

**  
Juan Martinez** 1:01:41  
Right.

**  
Val Levitan** 1:01:42  
Okay, but on the other side, it sticks out.

**  
Juan Martinez** 1:01:46  
Yes.

**  
Val Levitan** 1:01:47  
So when I have Cash Code, we at Cash Code manufactured a nozzle for our bill acceptor.  
which was...  
You know, wide.  
Like, chunky.

**  
Juan Martinez** 1:02:03  
Right.

**  
Val Levitan** 1:02:04  
Right, because it sticks out, so it doesn't matter.  
And it sits on the door.  
Right, so you could manufacture whatever piece you want.  
So we manufactured the nozzle that had a small tiny display and that had a buttons, like 3 buttons on it, made out of silicon.  
A membrane switch.  
Like if you remember in the 80s we had Keno games with membrane switches.

**  
Juan Martinez** 1:02:36  
Yeah.

**  
Val Levitan** 1:02:38  
So, very similar, but like a rubberized membrane switch.  
but a big nozzle, a display, so the display was not touchscreen. It was a very primitive display, but it had three.  
Switches.  
Three buttons.  
You could put more bulbs, but three is enough.

**  
Juan Martinez** 1:03:02  
I'm sorry, those buttons were for players or employee use?

**  
Val Levitan** 1:03:03  
And.  
No players because it was a directional button. Like it was a display and kind of a yes, no, red, green, whatever.

**  
Juan Martinez** 1:03:08  
Okay.  
Oh.

**  
Val Levitan** 1:03:18  
And it had an arrow towards the bottom. This one or this one, and the small display was instructional.

**  
Juan Martinez** 1:03:23  
Yeah.

**  
Val Levitan** 1:03:26  
And the display is on the outside of the machine, sitting on the nozzle.  
So, imagine that...  
The nozzle has had a slot for putting the bills. On top where you put the bills, there's a display with buttons, but underneath there is a QR code scanner.  
Right.  
So, you could scan it.  
So.  
Instead of wiring the whole thing.  
You put a chip inside the nozzle, like a RFID chip.  
which gives it a unique number.  
Let's say nozzle.  
and you could scramble the number.  
Make it secret.  
And, through...  
Ohh.  
Some sort of a pairing mechanism.  
This nozzle could prepare to.  
Ohh.  
To.  
IQ.  
And we consider whatever is validated by this nozzle is sacred.  
Scorcher.  
So, this way...  
It becomes a secure gate.  
So you don't need to wire anything. You don't need to run a wire because it's secure.

**  
Andrei Klimovich** 1:05:13  
But how does it communicate to IQ?

**  
Juan Martinez** 1:05:19  
Yeah, the RFID portion, you're saying that this QR code was generated by this nozzle, which is an approved nozzle, and it contains the amount of the ticket and maybe the date and time that it was produced.

**  
Val Levitan** 1:05:34  
Right.

**  
Juan Martinez** 1:05:34  
G.

**  
Andrei Klimovich** 1:05:34  
Mhm.

**  
Juan Martinez** 1:05:36  
The only problem there though is for the machine performance, if we're only using this nozzle for bill acceptor activity, we don't have anything else to provide the casino or location with in terms of performance reports.

**  
Val Levitan** 1:05:46  
Right.  
Correct.

**  
Juan Martinez** 1:05:56  
The.

**  
Andrei Klimovich** 1:05:56  
And I can understand how IQ can verify those nozzles, but how one nozzle can verify another nozzle if we are talking about player going from one machine to another.

**  
Juan Martinez** 1:06:05  
No, no.

**  
Val Levitan** 1:06:07  
Well, all nozzles on the locations.

**  
Andrei Klimovich** 1:06:10  
Know each other.

**  
Val Levitan** 1:06:11  
Know each other.

**  
Andrei Klimovich** 1:06:13  
Okay.

**  
Juan Martinez** 1:06:16  
And that, that's not you; you probably never saw it in action. Actually, I can send you a video, but that's how the pyramid printer works.  
With a more archaic technology, it prints out a demo QR code. You then take it to the kiosk and scan it, and now they're married.  
That's how the pyramid printer works.

**  
Andrei Klimovich** 1:06:39  
Okay.  
And as I did, another thought that it might be challenging to install this type of nozzle to every single type of machine, because there were...

**  
Val Levitan** 1:06:50  
No, no, it's not challenging.

**  
Andrei Klimovich** 1:06:52  
Totally different, yeah.

**  
Val Levitan** 1:06:54  
No, no.  
Um...  
I don't know.

**  
Andrei Klimovich** 1:07:05  
So it leads to another solution, sorry.

**  
Val Levitan** 1:07:06  
I, I, I don't know, but, but hold on, but hold on a second, hold on, it, it doesn't have to be a nozzle.

**  
Andrei Klimovich** 1:07:11  
Mhm.

**  
Val Levitan** 1:07:14  
I mean, it could be a different nozzle. It doesn't matter. We actually, we already have just a nozzle, just a nozzle by itself. All we need to do is to put our FID in there.

**  
Andrei Klimovich** 1:07:29  
So, RFID might be integrated in our current flex port, right?

**  
Val Levitan** 1:07:33  
Yes, but...  
I mean, we have to do a redesign, but it's not a complicated redesign. It's very simple.  
Wow.  
We we can do the pairing, that's not.  
The only thing we're missing is the QR code, the sorry, the printer part.

**  
Andrei Klimovich** 1:08:03  
What do you mean by missing, like...

**  
Val Levitan** 1:08:06  
The payout.

**  
Juan Martinez** 1:08:08  
the payout portion. There's no nozzle necessarily on the printer, you know, so we almost would need two per device.

**  
Andrei Klimovich** 1:08:09  
Yeah.

**  
Juan Martinez** 1:08:17  
One to carry the in, one to carry the out. Is that what you mean, Val?

**  
Val Levitan** 1:08:25  
No, I'm trying to, I'm trying to remove a printer.

**  
Juan Martinez** 1:08:26  
Yeah, just think about it.  
Yeah.

**  
Val Levitan** 1:08:34  
I know where Andrei is going with this. I mean, we have the location is formed already. This is it. But these locations need to be wired up. It's A tremendous expense.

**  
Andrei Klimovich** 1:08:46  
Yeah, and they need to be wired up only to communicate, to establish a communication between ports and IQ, right? And it can be done without wiring up. It can be done if IQ can talk to, sorry, if port can talk to IQ wirelessly. And it'd be, I don't know, like mini.

**  
Val Levitan** 1:08:54  
Yeah.  
Yeah.

**  
Andrei Klimovich** 1:09:05  
Mini modem.

**  
Val Levitan** 1:09:06  
Could be, could, could be wirelessly, wirelessly a solution could be, but...

**  
Juan Martinez** 1:09:15  
Yeah, and that would only work in Texas. Most regulated wireless is scary. Wireless implies hackers. Wireless implies someone's going to break in or intercept the signal. So it's always been fought, but it could work in Texas.

**  
Val Levitan** 1:09:32  
It could work in Texas, it could work in Nebraska.

**  
Juan Martinez** 1:09:34  
Yeah.  
Yeah.

**  
Val Levitan** 1:09:37  
But it's not going to work in, let's say, highly regulated places. But we're not going there for now. And in the highly regulated places, we could offer a different solution. But any external device, we could theoretically make wireless.

**  
Juan Martinez** 1:09:44  
Bye.  
Yeah.

**  
Val Levitan** 1:09:57  
I mean, this is a standard technology today, secure wireless. It's standard.

**  
Juan Martinez** 1:10:01  
Yeah.  
You know that that you had previously mentioned the card idea.  
You know, if we went NFC or low power Bluetooth.

**  
Val Levitan** 1:10:10  
So.

**  
Juan Martinez** 1:10:14  
Maybe, you know, now we only have to transmit to the card in the player's hand, that's their virtual wallet.

**  
Val Levitan** 1:10:22  
So, so yeah, so as I said, remove printers, put our QR scanner, which is dirt cheap.  
Each QR scanner, we can make it.  
Kind of a...  
secure through our FID, right?

**  
Juan Martinez** 1:10:43  
Yeah, or Bluetooth or NFC. I mean, there's different different ways to secure that.

**  
Val Levitan** 1:10:49  
Well, let's not call it secure. Let's call it pre-validated.

**  
Juan Martinez** 1:10:54  
Mhm.

**  
Val Levitan** 1:10:58  
I think it's much easier to sell to a Texas operator to say, hey, dude, you're spending a shitload of money on service and paper on printers, dump it. Here's a little non-mechanical nozzle, install it and put these

**  
Juan Martinez** 1:11:09  
Yeah.

**  
Val Levitan** 1:11:19  
And the cards, and the cards, we could just say, don't even buy plastic here, here's printed cards.

**  
Juan Martinez** 1:11:28  
Right, right.

**  
Val Levitan** 1:11:29  
Sorry, not printed. We could install a printer and print paper QR codes.

**  
Andrei Klimovich** 1:11:41  
It can be a digital QR code generated by some simple web application secured by us. So you come into the location, you scan a QR code on the wall with your mobile phone, and you get a QR code.  
I'm ready to go.

**  
Juan Martinez** 1:12:00  
I guess to your point though, Andrei, Val, it would be interesting to talk to a couple of operators, as you mentioned, Andrei, because even with that Chinese knockoff version of Mother Goose, there's still serial cabling.  
being run there and maybe they're already used to having to run cables and we're overthinking it, but it's normal to them. I mean, to me, it's always normal in a casino to have miles and miles of Ethernet network cable and fiber optics, but, you know, maybe it's not that.  
Dissimilar for these Texas operators.

**  
Andrei Klimovich** 1:12:39  
From, from my God, I would...

**  
Val Levitan** 1:12:40  
Let's, let's, let's, let's just pinpoint this idea a little more.  
Let's just not rush into cables.  
Running cables in a casino where you have floating floors.  
Versus.

**  
Juan Martinez** 1:12:59  
Yeah, 100% agree, Val.

**  
Val Levitan** 1:13:00  
It.  
I mean, it's hard, you know.

**  
Juan Martinez** 1:13:03  
Yeah, yeah.

**  
Andrei Klimovich** 1:13:05  
So the obvious solution is just to make a communication between Flexport and IQ Wireless and any type of wireless, but the solution where we do not need physical cables over there, right? So it can be done.

**  
Val Levitan** 1:13:19  
And we, and we could have, we already have these SMIP boards that we could put inside a slot machine.  
But I prefer not. I prefer just to...  
Build inside the nozzle, make the nozzle that pre-validated.  
So, we know that this is a secure remote nozzle.  
And that it, and it, and the IQ is secured.  
So if we could encrypt the QR code, printed QR code that only our nozzle reads.  
then we secured the carrying transaction that, you know, that even if you duplicate it, it's encrypted.

**  
Juan Martinez** 1:14:08  
Yeah.  
Yeah, let me think about that too. I mean, definitely interesting. And then this is the market to try that.

**  
Val Levitan** 1:14:19  
So the question is...  
Can a printed QR code be encrypted that can only be decrypted by the pre-approved nozzle?  
That's the, that's the essence of the question.

**  
Juan Martinez** 1:14:38  
Yeah.

**  
Andrei Klimovich** 1:14:44  
But isn't it just how it works right now with optical scanner and printed QR code which is verified by host?  
Is it just that that how it works right now?  
So...  
Do you mean that host can be excluded and the whole verification can be done on game machines level only without talking to host?  
That's something you're trying to achieve?

**  
Juan Martinez** 1:15:33  
What was that again, Andrei? Sorry, I got a message from South Dakota.

**  
Andrei Klimovich** 1:15:38  
Oh.  
So it is all about a wallet record. And this record needs to be stored somewhere to be verified by machine, by IQ, et cetera. And this record right now is being kept on a host site. It's a cloud server. That's what the point of truth is.

**  
Juan Martinez** 1:15:52  
Yeah.  
Yes.

**  
Andrei Klimovich** 1:16:01  
So how it works, like right now, the port talks to IQ, IQ makes a request to host, host returns a reply if this e-wallet exists, what is the balance, and IQ talks back to a port, and port gets an information if.  
There are credits or no, if there are, it talks to the game machine, please.  
grant this account over here on this specific machine a specific amount of credits. This is the communication of how it's being designed right now.  
And one of the weakest points here is a communication between port and IQ, not port and host, because only IQ talks to host. IQ is our hub, actually. So the question is, how can we make port talk to IQ without wires?

**  
Juan Martinez** 1:16:59  
Yeah, just wirelessly.

**  
Andrei Klimovich** 1:17:00  
So, wirelessly, so it's something that is already in place. So, when I mean wirelessly, it's something like there is a modem which can connect to the locations network and talk to IQ through the locations network. It's very simple. The question is...

**  
Juan Martinez** 1:17:05  
Yeah.

**  
Andrei Klimovich** 1:17:19  
How much does it increase the price of Flexport if we are adding this piece of modem over there? I don't know, but I don't think that is something expensive.

**  
Juan Martinez** 1:17:28  
Well, no, no, no. The ports don't need a modem. Think of each flex as a laptop on a network.  
Hub does all of the communication with the cloud.  
Each port or laptop just connects to the hub and does full transmission of data over Wi-Fi, like any laptop does today over a wireless network. You don't need, the laptop doesn't need to connect to anything other than Flex IQ.

**  
Andrei Klimovich** 1:18:00  
Yeah, that's what I'm talking about, like, but there is should be some piece of hardware which will allow ports to connect to IQ wirelessly.

**  
Juan Martinez** 1:18:00  
And select.  
Yeah, just why with a normal Wi-Fi.

**  
Val Levitan** 1:18:10  
Let listen, let let we we don't need any of it. We don't need it at the point of printing a ticket. We can encrypt the QR code. The QR code looks gibberish to another reader. If you present it to another reader, it doesn't know what it is. It's gibberish.  
Only our novels will be able to read it.

**  
Juan Martinez** 1:18:36  
But Val, when you say...

**  
Val Levitan** 1:18:36  
And the reason our nozzles and the reason our nozzles are able to read it because they have been paired to the IQ that's in this location.

**  
Andrei Klimovich** 1:18:51  
Yeah, so okay.

**  
Val Levitan** 1:18:54  
So that becomes your e-wallet. You come in, the only inconvenience, and I submit to it, I agree with that. The only inconvenience is that you won't be able to.  
No, sorry.  
Yeah, you won't be able to print at the machine. That is the only one inconvenience.  
The initial ticket, the initial wallet needs to be obtained.  
First time, as you come in into the location.

**  
Andrei Klimovich** 1:19:24  
Well, actually, it can still be possible if we are not keeping e-wallet records on host side at all. And everything happens just in the location itself.

**  
Val Levitan** 1:19:37  
No, you cannot because the printers in the machine.  
Will not print encrypted.

**  
Andrei Klimovich** 1:19:47  
Mm.  
Just let me ask you the question. Like, I'm following your idea here, and it sounds to me like it is possible. So here is the scenario. A player comes into the location, goes to the game machine. He inputs money into the game machine, he redeems, and flex port or something, you may call it a nozzle, whatever.  
right? It has some kind of algorithm which works fully offline, an encryption algorithm, and it sends a...

**  
Val Levitan** 1:20:17  
De decryption.

**  
Andrei Klimovich** 1:20:20  
Encryption and decryption, it, it, no, no, please follow, please follow my idea, like the the flex port can encrypt and decrypt, right? So, when you redeem.

**  
Val Levitan** 1:20:22  
No, no, no decryption.

**  
Andrei Klimovich** 1:20:33  
It sends encryption command to printer to create a QR code which has an encrypted information about the value, nothing more. Then you print.

**  
Val Levitan** 1:20:43  
Oh, oh, hold on, hold on one moment. That's interesting. That's very interesting. I like it.  
I forgot.  
that we are plugging the printer back into the QR code nozzle.

**  
Andrei Klimovich** 1:21:00  
Right. Printer works with us only. It has no direct communication to the game anymore as soon as a port appears over there. So the communication is game talks to port, port talks to printer.

**  
Val Levitan** 1:21:12  
Yeah, yeah, yeah, yeah.

**  
Andrei Klimovich** 1:21:15  
So if we can encrypt and decrypt, port sends a command to print it to create a QR code with encrypted value, nothing more. Then you get this ticket, go to another machine, you scan it with a port, now port decrypts it. Only port knows what the algorithm is.  
And it gets a single value, nothing more. It sends it to machine, then you redeem again. It repeats, and you go to IQ finally. You scan it with IQ. There is the same encryption-decryption algorithm over there. We get the value. After it is redeemed and fully paid, that's where we can create a record in host.  
Finally, that a specific amount was paid, nothing more.  
But what we lose here, we are losing information about games, machines itself. We cannot track it, but still, maybe we can track it. If we can encrypt 1 digit, sorry, one value.

**  
Val Levitan** 1:22:11  
We, we can, we, we can, we could, we could absolutely offer a connection to a SAS port.

**  
Andrei Klimovich** 1:22:19  
Or we can use a MAC address, yeah, MAC address or the machine.

**  
Val Levitan** 1:22:19  
You know, from a ship, from a...  
No, you cannot. No, no, you cannot. You gotta connect to SAS port.

**  
Andrei Klimovich** 1:22:27  
Okay, okay.

**  
Val Levitan** 1:22:28  
In the machine, and then you'll get all the information, of course.

**  
Juan Martinez** 1:22:32  
Right.

**  
Andrei Klimovich** 1:22:33  
Or I will tell you, like, we know every single port installed in every single machine, and we know our ports IDs, right? Well, let's call it an ID or mark address, whatever, the port. And there is a collection where each single port is linked to a specific machine, which is...

**  
Val Levitan** 1:22:45  
But...  
But...

**  
Andrei Klimovich** 1:22:51  
Initially, it's managed manually, but after that, it's an automatic system.

**  
Val Levitan** 1:22:56  
Yes, but you know, in Russian, was the way to.  
I, I understand.

**  
Andrei Klimovich** 1:23:05  
So, in this case, we don't need, yeah.

**  
Val Levitan** 1:23:06  
I understand, I understand, but this is not the goal. The goal is right now.  
Ah.  
how not to wire up the location. It works for me.

**  
Andrei Klimovich** 1:23:18  
Sounds like it works, yeah, agreed.  
Uhh...

**  
Val Levitan** 1:23:22  
I forgot that printers could be connected to...  
To the port, yes.

**  
Andrei Klimovich** 1:23:36  
Sorry for the stupid question, but do ports contain any kind of brain that can do this operation?

**  
Val Levitan** 1:23:44  
Well, actually, the actually the full port is quite sophisticated. It's a it's a full-fledged computer.

**  
Juan Martinez** 1:23:44  
It's a it's a.  
Yeah.

**  
Andrei Klimovich** 1:23:51  
Okay.

**  
Val Levitan** 1:23:51  
Full port, the full port with touchscreen and display, the whole thing is a computer.  
So it's very, very sophisticated.  
But I don't want to put the full port. I want to put a small nozzle. Very inexpensive.  
Kind of a throwaway \*\*\*\*.

**  
Andrei Klimovich** 1:24:17  
We still need some display over there to talk to a player to explain what's going on and what, what, what's like if is if there is an error, if there QR code that is not readable, etc.

**  
Val Levitan** 1:24:30  
I can try to put a tiny display, and I could put a red and green flashing button.

**  
Andrei Klimovich** 1:24:36  
Okay, makes sense.

**  
Val Levitan** 1:24:44  
It's not, it's not a fantastic solution, but...  
It allows us to move very, very fast, very fast.

**  
Andrei Klimovich** 1:24:55  
And just to speak it out, it will also work if the account, sorry, if e-wallet is being created on IQ first or on the recycler side, it's just the same logic. So it's encryption, decryption, you print out a ticket.  
Yeah, makes sense.  
How can it be?

**  
Val Levitan** 1:25:19  
As long as we share the same encryption key per location, we're fine.

**  
Andrei Klimovich** 1:25:31  
How can it be broken? How can someone fraud the system? Can they read the code somehow?  
By connecting to a port, I guess so.

**  
Val Levitan** 1:25:42  
Listen, Andrei, everything is possible, but not in this business. And not in Texas.  
I mean, I mean, your enemy is a bartender, but not a sophisticated thief. A sophisticated thief is going to get gunned down and killed.

**  
Andrei Klimovich** 1:26:03  
Yeah.

**  
Val Levitan** 1:26:04  
But that's gonna be sophisticated thief in Texas. Your problem is a cashier.  
you know, some alcoholic that, you know, works for an operator or a penny thief, you know, you know, it's not going to be a sophisticated decryption specialist.  
Not A mathematician.  
It's not a bad system.

**  
Andrei Klimovich** 1:26:49  
You know, like, it might be that...  
No, just an ideal, but it might be that.  
The systems that we've seen are in Texas where the redemption kiosk is present. It might be done in the same pretty, pretty simple way. So maybe there is no host, there is no cloud verification at all. So just printing QR codes.

**  
Val Levitan** 1:27:12  
Yes, yes, I'm not, yes, yes, I'm not inventing anything new. I'm actually...  
borrowing an idea from pyramid. That's how pyramid operates.

**  
Juan Martinez** 1:27:28  
And even JCM, they tried to deploy an e-wallet solution by inserting an NFC tag in their bill acceptor entry, and you would supposedly tap your phone to that to transfer funds, but it never really took off.

**  
Val Levitan** 1:27:45  
And MEI had a vending head where you tap your phone through NFC. I mean, I'm not reinventing your wheel here.

**  
Juan Martinez** 1:27:50  
The.  
Yeah.  
Right, right.

**  
Andrei Klimovich** 1:27:59  
Okay, so again, the backbone of our idea is here is that there is a certain landscape already in place and they have printers over there. So we are reusing something they already have and we are doing it.

**  
Val Levitan** 1:28:13  
Or, or, or removing it.  
I'm not advocating a removal. I understand that you want to reuse it and I'm going with that idea. But if somebody says I'm sick and tired of this stupid paper floating around, we could offer him a solution. Well, a player comes in, gets himself one wallet.

**  
Andrei Klimovich** 1:28:19  
Okay.  
Yeah, beautiful week.

**  
Val Levitan** 1:28:40  
And moves around with this wallet.  
Through the location, until he is ready to cash out, and then he would come to either.  
I mean, if it's manual system, then he comes to the counter, and then at the counter there is an IQ.  
Or if it's fully automated system, he could come to a recycler.  
So he starts operation from a recycler and ends his operation at the recycler.

**  
Andrei Klimovich** 1:29:13  
And if he wants to create an, oh yeah, here we go. By the way, like recycler or IQ as a starting point, it can also start with an empty wallet. If by some reason, I don't know, but by some reason he would like to cash in at the machine specifically, he may push just one button on the screen.  
print me a ticket. So it's just a QR code with 0 value. Then you go to the machine, you feed money into the machine. When you redeem, you scan your QR code. That's it. You don't need it.

**  
Val Levitan** 1:29:44  
No, no, no, no, if a machine, if a machine in a location has a build acceptor and a printer, then...

**  
Juan Martinez** 1:29:45  
But remember, IQ?

**  
Andrei Klimovich** 1:29:53  
No printer.

**  
Val Levitan** 1:29:55  
Mm.

**  
Andrei Klimovich** 1:29:55  
He wants to remove printers.

**  
Val Levitan** 1:29:58  
Hold on a second. I just want to make something very clear. If you use a recycler in the location, you cannot have bill acceptors inside of the machines.

**  
Andrei Klimovich** 1:30:09  
You can.

**  
Val Levitan** 1:30:11  
You cannot.

**  
Juan Martinez** 1:30:13  
Yeah, you will never fill the recycler if they, if they can insert money anywhere else except the recycler.

**  
Andrei Klimovich** 1:30:22  
That's right, but we cannot.

**  
Juan Martinez** 1:30:23  
Or, to keep the recycler full of money, it needs to receive all the money.

**  
Andrei Klimovich** 1:30:28  
You cannot have bill validate or you cannot have a ticket, sorry, printer on the.

**  
Juan Martinez** 1:30:33  
Bill Val dinner.

**  
Val Levitan** 1:30:33  
You'll validate.

**  
Andrei Klimovich** 1:30:34  
Build the data, but I can hardly imagine that anyone will agree for that, because it's a crucial part of game player experience.

**  
Val Levitan** 1:30:40  
Many, many, many, many, many locations in Texas will opt out.  
Many.  
As a matter of fact, I can bet right now, and I know that I'm going against Juan's belief, he feels differently. I believe that in Texas specifically, it will mostly be recyclers.  
But whichever way, I'm fine with that, because we offer solution either a recycler or an IQ. It doesn't matter.

**  
Andrei Klimovich** 1:31:13  
Or a dispenser, if they don't want to hit her attendant.

**  
Val Levitan** 1:31:15  
Or, or, or, yeah, yeah, or a dispenser, yes, yes, yes.  
Yes.

**  
Andrei Klimovich** 1:31:22  
So, about the actually is a recycler.

**  
Val Levitan** 1:31:25  
So with the dispenser, just to be clear, with the dispenser, the manual operation will be at night. You have to empty out all the cash boxes. You need to sort cash. And you need to refill the recycler.

**  
Andrei Klimovich** 1:31:43  
Dispenser.

**  
Val Levitan** 1:31:45  
Sorry, a dispenser. Yes. And it's done manually on a daily basis. So it has to be a part of a person touching money.

**  
Andrei Klimovich** 1:31:55  
Yeah, and let's say...

**  
Val Levitan** 1:31:56  
Every time, every time, with no exception, just a matter of time, when a human touches money, money sticks to fingers.

**  
Andrei Klimovich** 1:32:08  
So, it.

**  
Val Levitan** 1:32:08  
And you know what you know what happens when when cash sticks to fingers, do you?

**  
Andrei Klimovich** 1:32:13  
Yeah, it disappears from my song, Magic Scism.  
Slope.

**  
Val Levitan** 1:32:18  
This is where this is where recycler is indispensable.

**  
Andrei Klimovich** 1:32:26  
May I ask you one question? Let me describe if you still have some time, because I was thinking about that. About the recycler. We have not a problem, but there is a potential friction over here. Like we are ready to introduce a recycler and it obviously can benefit.

**  
Val Levitan** 1:32:31  
I have, I have. Go ahead.

**  
Andrei Klimovich** 1:32:43  
a lot of locations in Texas. But we have another requirement that people, players, would really love to keep build validators at the machines because they really love to cash in when they're in rush. I felt it myself like while playing in Texas. So it's like a hybrid.

**  
Val Levitan** 1:33:03  
Fully, fully agree.

**  
Andrei Klimovich** 1:33:06  
And it's like a hybrid situation, like recycler can really benefit operator, but at the same time, they need to keep building the data on the machine size. So, and I was thinking like the whole idea is just recycler needs to get a flow of cash in money to be fully operational. That's the whole idea of recycler.  
And how can we increase a flow of money going into recycling instead of going into machines? And then like an idea, we'd be incentivize players at least to start their gaming sessions, their game day in the location with a recycler.  
So, at least you...

**  
Val Levitan** 1:33:46  
You will not, you cannot put a recycler in a location where bill acceptors are inside the machine.  
You cannot. You should not offer it. It's not an award.

**  
Andrei Klimovich** 1:33:57  
So.

**  
Juan Martinez** 1:33:57  
And incentivized means it's costing somebody money. How are you incentivizing the player for free?

**  
Andrei Klimovich** 1:34:02  
So.

**  
Val Levitan** 1:34:06  
It's not gonna work.

**  
Andrei Klimovich** 1:34:06  
Not for free, not for free. I'm just leading to the situation when you, as an operator, as a clever operator.

**  
Val Levitan** 1:34:12  
Use your your your right now, you're up to here in the swamp already.  
Get out.  
It's not gonna work.

**  
Andrei Klimovich** 1:34:21  
Okay, okay, you don't want to discuss it, I get it, so...

**  
Val Levitan** 1:34:24  
No, no, take the old timer, take the old timer suggestions, not gonna work.

**  
Juan Martinez** 1:34:25  
Oh, okay.

**  
Andrei Klimovich** 1:34:35  
Okay, no problem.

**  
Val Levitan** 1:34:36  
You want to build your gaming operation, number one thing you always do, you remove confusion.  
confusion for the player, confusion for the operator, confusion for bartender, for whatever who minds the location, remove confusion.  
And direct the traffic.  
So where do you want the player to go? You want them to start by getting a QR code first, or you want them to go to the machine and insert the money first?  
That's a that's a strategic decision that a location needs to make.  
The best thing is to insert the money.  
That's the best thing. Come to the machine, insert the money.  
That is the best for gambling.  
gambling operation benefits from partying with money.  
However, casinos are equipped with cameras, with supervisions, with tight bookkeeping, with reconciliation. It's a fortress. Casino is a fortress. Location is a hall full of  
Problems.  
So.  
You will be dealing with shortages, you will be dealing with thieves. The location, look, I didn't want to go there, but...  
Imagine you're running a gray operation. It's a cache gray operation.  
Right.  
You have this groundful employee who is stealing from you. You fired this employee who was getting...  
Very, very nice, sticky, sticky, sticky stuff.  
Start to his fingers.  
He is very upset.  
Let me guess, what is he gonna do first?  
Maybe he's gonna go to a sheriff and testify against you.  
It's a problem.  
So eventually, I have no doubt that, I mean, if I speak to an operator and I know what I'm talking about, and I tell them about all of these things, because I come from a great business,  
He'll put a recycler.  
Because recycler removes sticky fingers, removes potential complaint, removes disgruntled employee, removes the potential closure or location, removes conflicts.  
Whenever you touch catch, you always have conflict.  
Casinos run because they're legitimate, they're fortresses, they they're they have.  
Irant, you know.  
Claude, Claude.  
Locked operations.  
Cycles.  
Not locations.

**  
Juan Martinez** 1:38:07  
That doesn't.

**  
Val Levitan** 1:38:08  
Not locations of twenty-five machines, and and the...  
Bartender who doubles for a machine mechanic and...

**  
Andrei Klimovich** 1:38:26  
Okay, so...  
May we discuss our next steps? So, first one, won't you mind if I'll quickly talk to Pavel about this encryption-decryption?

**  
Val Levitan** 1:38:37  
Absolutely, Mike. I already told you once. Please don't do it.

**  
Andrei Klimovich** 1:38:37  
Yeah.  
Yeah, okay, but how can we handle it?

**  
Val Levitan** 1:38:45  
Very simple, we have a transcript of this call. Let's...  
Create a.  
Brief.  
I'll take the brief, I'll speak to the engineers, I'll figure out what we can do because we have other priorities.  
Let me understand what's possible and what not.  
I'll get back to.

**  
Andrei Klimovich** 1:39:10  
Okay, Gary.

**  
Val Levitan** 1:39:10  
Definitely.

**  
Andrei Klimovich** 1:39:12  
So, for next steps with operators from Texas.

**  
Val Levitan** 1:39:16  
What you can do for me, what you can do for me is to create that brief.

**  
Andrei Klimovich** 1:39:23  
I can do that.

**  
Val Levitan** 1:39:24  
So that will save me time. And please, it needs to be short, very primitive already. Make sure that a 12th grader can read it. Nothing technical. Don't find technical solution for anything.

**  
Andrei Klimovich** 1:39:38  
Okay, I can do that.

**  
Val Levitan** 1:39:41  
Half a page, it needs to be 3 to 5 minutes read maximum for people that don't speak English.  
presented in two languages, English and Russian, that would be a great help for me.

**  
Andrei Klimovich** 1:40:00  
Okay, I'll do that.  
So for operators again, like let's put it on hold for now. We are not 100% sure what we are offering.

**  
Val Levitan** 1:40:10  
No, no, no, no, no, no. You should listen. These operators will not open up to you. It's going to take a while. It's okay to take another trip. It's okay to say, I'm on market research. We're thinking of this. What do you think of the recycler? What do you think if printers are removed? What do you think of?  
Let's say you validate your QR code first. How would you like this? It's a relationship. And then you start talking about...  
location test and then you start probing the price. It's going to take time.  
Absolutely talk to operators. And especially now that you saw operators, make sure you contact them within, you know, reasonable time, two, three weeks, so they remember you, of course.

**  
Juan Martinez** 1:40:47  
Yeah.

**  
Andrei Klimovich** 1:40:49  
Okay.

**  
Val Levitan** 1:41:03  
Very important.

**  
Andrei Klimovich** 1:41:03  
Okay, agreed.

**  
Val Levitan** 1:41:08  
But everything we discussed is valid. You are a product manager. You're here to do your research. You're not committing to anything. You're not selling anything. You're just trying to find a solution for these operators and put technology into their hands. What do you want, Mr. Operator? What if this? What if that? Have you thought of this? And have you tried this?  
We're thinking of this, and what do you think about it?  
And we heard that this may work.  
Less concrete, less conversation, ask question, listen.

**  
Andrei Klimovich** 1:41:45  
Yep.

**  
Juan Martinez** 1:41:51  
Val, we have an issue in South Dakota. I'm going to copy you on my response to Ivan, but I got to drop off the calls of Denis right now. He's at the location.

**  
Val Levitan** 1:42:00  
All right. Okay. So yeah, we're done anyways. Thank you. Bye.

**  
Juan Martinez** 1:42:04  
Okay, thanks everybody.

**  
Andrei Klimovich** 1:42:05  
Thank you. Thank you.

**  
Val Levitan** stopped transcription
