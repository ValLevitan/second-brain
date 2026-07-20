**Transcript**

July 29, 2025, 12:03PM

**Val Levitan** started transcription

**Nathan Carver**   0:06  
All right, let me just do.  
I'm just gonna call architecture discussion.  
Um, I can't quickly pull in those diagrams, one correct from the Visio, I don't think.

**Juan Martinez**   0:25  
You may have to download them.

**Nathan Carver**   0:27  
OK, that's OK. I think we can quickly recreate what we need. It's not a big deal.  
All right, let me share. Let me share the link and then we can also share my screen.  
So this is just a blank board and we can talk. I'd like to start at the the kiosk and just and work our way out.  
Because in my mind that seems to be like the hub, right? Where the all the new, at least from what we discussed with John, right? This is where.  
This is the new tech or the new component.  
The new device.

**Juan Martinez**   1:17  
Yeah, since since we have a kiosk, can you just add the word redemption or in front of it?

**Nathan Carver**   1:23  
Oh, gotcha. Good.  
All right, so.  
OK.  
So the I guess this.

**Val Levitan**   1:48  
OK.

**Nathan Carver**   1:51  
For my own sake, let's call it the capabilities. So the kiosk will have the ability to dispense cash, right? It has the internal.  
Cache system right?

**Juan Martinez**   2:02  
That is right.

**Nathan Carver**   2:06  
Will it also dispense possible to do the gift cards or just cash?

**Val Levitan**   2:11  
Yes.

**Juan Martinez**   2:13  
Yes.

**Nathan Carver**   2:17  
OK.  
And then this is also the ability to interact with the e-wallet, and that's how they'll get cash from their winnings.

**Juan Martinez**   2:24  
Yeah.  
Yeah, so you can put dispense a ticket and it's a slightly different ticket, but.

**Nathan Carver**   2:27  
Yeah.  
Right. And that's what they'll carry with them to each machine, right? And scan.  
At the Um.  
What is it? The which flex device will scan the ticket at the machine? Flex port?

**Juan Martinez**   2:48  
Hm.  
Oops.  
The ticket disappeared.

**Pavel Frolov**   3:14  
Accept bills.

**Nathan Carver**   3:19  
Exit bills, yeah.

**Juan Martinez**   3:22  
Did did you purposely remove the dispenser ticket?

**Nathan Carver**   3:22  
Yes.  
Uh, no, I think it.  
I think I got out of sync.

**Juan Martinez**   3:38  
And I would put in parentheses E wallet just so we know the type of ticket that it is.

**Nathan Carver**   3:39  
OK.  
OK.

**Juan Martinez**   3:46  
Right after the word ticket there.

**Val Levitan**   3:52  
Are you sharing your screen or no?

**Nathan Carver**   3:55  
Um, I I can share my screen.

**Val Levitan**   3:57  
No, no, because I'm I'm comfortable.

**Nathan Carver**   4:03  
About the shared desk.

**Pavel Frolov**   4:04  
It's it's it's better to to share screen uh uh because of uh recording of this.

**Nathan Carver**   4:10  
Oh yeah, let's do that. I I didn't. Thank you, Pavel. I'm gonna kick that off. Oh, almost got it going. Good. All right. I will share the screen for that reason.

**Pavel Frolov**   4:23  
And the scanning the wallet ticket additional feature.

**Nathan Carver**   4:32  
Yeah.

**Pavel Frolov**   4:33  
Not feature but capability.

**Nathan Carver**   4:48  
OK, there we go.  
I'm going to widen this.  
All right, so dispense a ticket, scan E wallet. What was the last one, Paula? Was that it?

**Genadi Peari**   5:04  
So.  
Dispense the ticket means print the ticket, right?

**Pavel Frolov**   5:09  
Um.

**Val Levitan**   5:12  
Yes.

**Pavel Frolov**   5:14  
Scan your wallet. I would add some administrational set up using scanner.  
For example, right now we have some procedures like lease.  
Please apply using.  
QR scanner also device registration using a QR scanner. I think probably we we will be able if it's necessary to apply some settings or provide special access.  
For some person using a special QR scan.

**Nathan Carver**   6:06  
Yeah.  
OK.  
I'll add that in. Alright, so this is like the configuration or administrative access.

**Juan Martinez**   6:15  
Um.  
Uh, Pavel, in the scenario you just described, where is the ticket?  
Generated that could contain this data.

**Pavel Frolov**   6:36  
Uh, it will be not a ticket. It will be a uh application on mobile phone for example.

**Juan Martinez**   6:41  
OK, OK, understood, understood.

**Pavel Frolov**   6:44  
Um.

**Val Levitan**   6:45  
It's it's actually an interesting idea. Maybe we should also do it through a ticket.

**Juan Martinez**   6:51  
Well, no. The reason I I asked is because then we rely on a second piece of hardware like the Flexpay kiosk. You know, where was this ticket gonna come from if it had to be printed on site? You know where we we would end up in a scenario where we don't just have a redemption kiosk and.  
The OS.

**Pavel Frolov**   7:14  
But it's new, awesome. It's finished now when we look at the.

**Nathan Carver**   7:16  
Right, so the redemption kiosk shouldn't print its own special access ticket.  
OK, so this is for specifically this is for a site administrator, some type of JBL administrator who has special access to the kiosk. So that could be through their phone.

**Pavel Frolov**   7:32  
But.

**Nathan Carver**   7:42  
Can we do is like face recognition? Is that an acceptable access as well? Do we want to get that sophisticated?

**Pavel Frolov**   7:54  
Probably we'll need to add some reporting or event management.

**Juan Martinez**   7:55  
The.

**Nathan Carver**   8:02  
Reported.

**Pavel Frolov**   8:03  
Reporting to our cloud configuration server.

**Nathan Carver**   8:05  
OK.  
OK.

**Juan Martinez**   8:12  
And Nathan, the scanner itself is down facing, so not readily available for face scanning.

**Nathan Carver**   8:20  
OK, so there would need to be some type of camera attachment.  
OK.  
I think.  
OK.

**Pavel Frolov**   8:40  
Um.

**Nathan Carver**   8:44  
So for this um.  
No, I'm assuming to do the gift cards. We're still, we still have a dependency on.  
Income and.  
And some type of ACH.  
Either our own internal API, but some type of ACH API.

**Juan Martinez**   9:19  
Yes.

**Nathan Carver**   9:26  
OK, so we still have a dependency here.  
Um for?  
OK, so for other, so all the inputs and the outputs, let's say that.

**Val Levitan**   9:42  
What does? What does ACH stand for?  
In banking, in banking industry, it stands for automated clearing house.

**Nathan Carver**   9:54  
So this would be, yeah, what like?

**Juan Martinez**   9:58  
Yeah, I.

**Nathan Carver**   9:58  
ACA is how they refer to the transfers.

**Juan Martinez**   10:05  
Yeah.

**Nathan Carver**   10:05  
Network.

**Juan Martinez**   10:06  
I think we we can collectively probably just call it the income payment gateway.

**Nathan Carver**   10:14  
So does income now income does?  
This would be an ACH transfer from the location and extensive in the for the purpose of gift card. I guess maybe this just applies in Georgia, but from the location to JVL, right? So when the gift card is.  
Redeemed.  
We're gonna initiate that transfer from the location that's accountable to pay winning, correct?

**Juan Martinez**   10:47  
Yes.

**Nathan Carver**   10:50  
And that's not necessarily through income, that's a separate.  
Provider as far as I know. Does that sound right?

**Juan Martinez**   11:02  
Yeah, it does. Yeah, Val, this is after a transaction has happened. Location XYZ owes us $5. They transfer the money to the JVL bank account as payment for the month, the week, whatever.  
Frequency we set U.

**Val Levitan**   11:19  
Yeah, it's automated clearinghouse.

**Juan Martinez**   11:21  
Yep.

**Nathan Carver**   11:22  
It.  
Alright, so um.  
Uh, let's see. Let's I'm gonna do just inputs simple.  
Input, output type thing so we have a clear.  
Change the color. Um.  
All right, so the player is going to interact with the kiosk.  
And through the use of a ticket and.  
And cash, correct?

**Juan Martinez**   12:02  
Uh, yes.

**Nathan Carver**   12:03  
Yeah.  
Do they have any other? Go ahead.

**Pavel Frolov**   12:07  
Probably in in the future, probably will accept the credit cards.

**Nathan Carver**   12:19  
OK.  
So when they deposit cash.  
That balance is kept correct, so they can go.  
What's the boundary of that? They can take that ticket in Georgia? I'm assuming it's the boundary of the location.

**Juan Martinez**   12:45  
Yeah, the the part part of the ticket. The part of the ticket will have a site ID that is only valid at that location.

**Nathan Carver**   12:45  
But as could go beyond that.  
Yeah.  
OK.

**Juan Martinez**   12:57  
You insert a ticket, you insert $20.00 and you get a e-wallet ticket that says $20.00 on it. But unlike a Tito ticket, the money.  
Is in the wallet, not necessarily the ticket.

**Nathan Carver**   13:20  
OK, and the site ID could be um.  
Well, it may not be a physical boundary, but it could be. It's just a group of game machines that are part of that site ID essentially. OK, because this obviously is going to be used beyond Georgia, correct? Like.

**Juan Martinez**   13:35  
Correct.

**Nathan Carver**   13:41  
Going to Texas, this same thing would be used and that may change how we view.

**Juan Martinez**   13:48  
Yeah, the the.

**Nathan Carver**   13:48  
Um collection of.

**Juan Martinez**   13:52  
Yeah, the tickets have to be unique to each location, so they they cannot be processed at any other location. That just keeps the finances locally and that's just the preferred method.

**Nathan Carver**   14:16  
OK. Or basically, who's paying paying the winnings?  
OK, so for when this cash gets deposited.  
Where do we want to keep that balance?  
And I'm thinking this is where the JBL server comes in, correct?

**Juan Martinez**   14:51  
Correct. Yeah. I mean, whether I, in my opinion, whether it's backed up to the cloud, it should remain locally and wherever the server is inside the kiosk or external, but that that will allow for some functionality in the event that we lose.  
Internet connection.

**Nathan Carver**   15:13  
Right.  
Oh, I see it, yeah.

**Pavel Frolov**   15:15  
Yeah.  
Actually it it can be physically be run on redemption kiosk or it can be run on separate hardware just to process ticket operations.  
To have its own database.  
And then to communicate to cloud servers.

**Nathan Carver**   15:39  
Yes.  
OK.  
So internally.

**Pavel Frolov**   15:46  
Oh.

**Nathan Carver**   15:48  
It's going to have, so it has its internal database.  
And so this will.  
OK, so it's gonna maintain maintain internal state.  
Uh, we may need to. Actually, let's move these to a different spot.  
We'll put them here.  
Um.  
Internal hard drives.  
And this will maintain.  
So this will maintain cash balances.  
And sync balances with.

**Juan Martinez**   16:58  
Are are you using cash balance and E wallet balance as one?

**Nathan Carver**   17:03  
Uh.  
Yeah, that's a good point. So we have different balances, right? We have, there's an actual physical cash balance in the machine.

**Juan Martinez**   17:14  
Yes.

**Nathan Carver**   17:16  
OK. And then E wallet is the balance of a player that they have in their E wallet account.  
And then OK, I'm just gonna do simplify this maintain internal state and sync with column.  
OK.  
So.  
Ewallet.  
Um.  
So for the E wallets.  
Is this?  
This is something that JVL that we would maintain in in the cloud, right? This is a.  
Is the e-wallet the player can take anywhere with them? Is can they go across locations and access their wallet or is it only tied to a redundant kiosk location?

**Juan Martinez**   18:26  
Oh, yeah.  
It's tied only to a redemption kiosk location. Yeah, the cross location financial reconciliation is would become a mess. So most casinos don't allow that and and we certainly shouldn't hear either the the the money should stay.

**Pavel Frolov**   18:38  
Yeah.

**Juan Martinez**   18:47  
At each location and all definitions of of money.

**Nathan Carver**   18:51  
OK.  
All right, so this is a direct link and it will not.  
OK, so the e-wallet is bound to the kiosk.  
OK, so the kiosk is going to maintain this wallet internally.  
So it's going to maintain the e-wallet.  
So this would also have OK, so by maintaining the balance, just maintaining the e-wallet is gonna have, it's going to be a database of all the players who've interacted with this.  
On.  
Do we identify anything with the player or is it simply a pin number with?  
Like how do we, how do we, how does a player access their e-wallet? This is gonna be.

**Juan Martinez**   20:10  
They they must remember their pin.

**Nathan Carver**   20:13  
OK.  
Um, is it? Is that the only?  
Like they just walk up, enter a PIN and that opens up their e-wallet.

**Juan Martinez**   20:28  
No, during the scan process at the Flexport device, they will be prompted to enter their PIN before transferring the funds in or out.

**Val Levitan**   20:28  
Yes.

**Nathan Carver**   20:42  
OK, do they scan their ticket? Like is there some way for the kiosk to know?

**Val Levitan**   20:44  
1\.

**Nathan Carver**   20:51  
Who the player is in order to match the pin they enter with that player's record like they scan the ticket or.

**Juan Martinez**   21:01  
Nope.

**Nathan Carver**   21:05  
OK.  
OK, so it maintains internal state, so it has um.  
And.  
Let's see, Player X by.  
2\.  
OK, so if we don't have anything, how big of a pin number are we having them do?

**Pavel Frolov**   21:43  
Phone numbers.

**Nathan Carver**   21:45  
OK, so there must is.  
So my thought is when do they when do they create the pin?

**Pavel Frolov**   21:54  
Right now when the player insert banknotes on kiosk.  
And decided that this amount enough was E wallet. He presses button generate E wallet. Then he will be asked to enter pin code.  
Repeat his numbers and after this he wallet is printed.  
So when the player want to use his wallet, he scans it on any device either flex port or kiosk to see available balance. Confirm that this is his number his.

**Nathan Carver**   22:37  
Oh, got it.

**Pavel Frolov**   22:46  
Bullet with a pin code and then decided what amount need to be transferred.

**Nathan Carver**   22:50  
Mhm.

**Pavel Frolov**   22:59  
Or redeemed in case of kiosk.

**Nathan Carver**   23:03  
OK.  
OK, so they.  
So player creates the wallet so that basically they insert amount of cash.

**Pavel Frolov**   23:16  
So right now only only one place to initiate a wallet on the kiosk.

**Nathan Carver**   23:17  
Uh, into the.

**Pavel Frolov**   23:27  
It it cannot be created uh from the Flex port.

**Nathan Carver**   23:27  
OK.  
OK, so the the thing that ties the pin, the pin is bound to the printed ticket e-wallet ticket.

**Pavel Frolov**   23:42  
Yes.

**Juan Martinez**   23:46  
Correct.

**Pavel Frolov**   23:46  
Yes.

**Nathan Carver**   23:47  
Got it.  
And that has a bar code right to identify it OK.  
I'm right. Bar code will identify that, so they'll scan it and the kiosk now knows which bar code to challenge the pin number against. OK.

**Juan Martinez**   23:59  
That's correct.

**Nathan Carver**   24:15  
OK, so if they lose the ticket then the cache is in there. As far as the player concerned, the cache is lost.

**Pavel Frolov**   24:25  
Yes.

**Nathan Carver**   24:30  
OK, so architecturally, um.  
I like this is all pretty, I think straightforward to keep In Sync, but if we want everything to work on the kiosk.  
It's basically going to be treated as an ATM, right? It's going to be.  
That's something that's easily movable, accessible simply because it has the cache in there for one thing.

**Pavel Frolov**   24:58  
I think in case if it contains lots of bank notes, it should not be easily movable.

**Juan Martinez**   24:58  
Right.

**Nathan Carver**   25:06  
Yeah.  
OK.  
OK, this makes sense.  
OK, so the other when they go to the machines down here, these the flex ports is what is going to allow that player to scan their e-wallet ticket out of the machine.

**Val Levitan**   26:05  
Mm.

**Juan Martinez**   26:07  
Yes.

**Nathan Carver**   26:07  
OK.  
All right, so the physical requirements then, right? So basically what you had in your diagram. So all these flex ports are going to have to be wired up to the redemption kiosk if that's becoming the hub, which makes sense because.  
It's already designed to be secure, so.  
Having it be the hub is 1 less device. I guess hub be the master.  
The server I guess to to the location.  
And then there may be physical routers.  
Right, to get all the wires hooked up, but essentially they're gonna be wired up to this redemption kiosk, which acts as the the host, the location host.

**Juan Martinez**   27:13  
Mhm.  
Correct.

**Nathan Carver**   27:56  
OK, so the services.  
Um.  
So we obviously have the E wallet component, we have the a server location server component.  
We have a synchronization service.

**Pavel Frolov**   28:41  
What do you mean synchronization service?

**Nathan Carver**   28:43  
I guess this would be us whatever needs to sync with JVL control server.  
Um.  
I don't know if you have another name for it. That's what I'm thinking of. It's just a service that keeps the the data In Sync between these two.

**Pavel Frolov**   29:02  
Mhm.

**Nathan Carver**   29:23  
So for this to be that, yeah, so this is so I know we have all our devices to be hot swappable, I'm assuming that.  
Is more complicated with the redemption kiosk just because of the physical size of it, but we should be able to replace it with a new kiosk at a location.  
And if we are syncing everything from this kiosk to the cloud, we should be able to reimage it remotely.  
Or at least reconfigure and restore the database.  
Remotely.

**Juan Martinez**   30:04  
Pavel, do you envision the redemption kiosk setup to be somewhat similar to a machine where you install software and then there's an equivalent of an RIS file?  
File.

**Pavel Frolov**   30:19  
Um.  
In some cases yes, but right now there is not so much settings that can be used same as machine.

**Juan Martinez**   30:32  
OK.

**Pavel Frolov**   30:33  
Actually right now settings for kiosk is quite quite not so so big and we are able to transfer this data just as answer to.

**Juan Martinez**   30:43  
Yeah.

**Pavel Frolov**   30:49  
At least come.

**Juan Martinez**   30:52  
OK.

**Pavel Frolov**   30:53  
We actually do not need even USB stick to apply the settings.

**Nathan Carver**   31:14  
Actually they do get their E wallet ticket from this.  
OK.  
Um, all right, so it's making sense.

**Juan Martinez**   32:00  
Should probably also add a POS here just as a backup to every site.

**Nathan Carver**   32:09  
Oh, I see what you're saying, yeah.  
Let's do that.  
So this would be um.  
OK, so the Flex POS is a is a backup.  
Um.  
Does it also have access to e-wallet or is it just going to be for the purpose of um?  
Dispensing that a winnings gift card.  
In this setup.

**Juan Martinez**   33:04  
I believe that it should Pavel. You should be able to take your ticket and scan it at the POS and then create a gift card, correct?

**Pavel Frolov**   33:13  
Yes.

**Nathan Carver**   33:15  
OK, got it.

**Val Levitan**   33:16  
Yeah, you don't need POS because you could still get a gift card from the kiosk.

**Juan Martinez**   33:23  
Now this is a POS as a backup if something were malfunctioning with the redemption kiosk.

**Pavel Frolov**   33:33  
It's optional in the schematic, but it it can be used, yeah.

**Nathan Carver**   33:39  
OK, so all right, I get it. So the player has his e-wallet and puts his cash in a redemption kiosk has a wallet.

**Val Levitan**   33:48  
Then you have to dispenser.  
Connected to POS.

**Nathan Carver**   33:55  
Oh, the dispenser.

**Val Levitan**   33:57  
Yeah, the tabletop dispenser.

**Nathan Carver**   34:00  
OK.  
Um, OK, so these are.  
And this will do for dispensing of the cash or gift card.

**Juan Martinez**   34:33  
The gift card. Yeah, gift card only.

**Nathan Carver**   34:35  
OK.  
All right, so the the backup. Go ahead.

**Pavel Frolov**   34:39  
OK.  
Actually I I would insist to to have an option for Flex POS to work without tabletop dispenser but using manual magnetic swiper.

**Juan Martinez**   34:52  
Right.

**Pavel Frolov**   34:57  
In case when we have for example redemption kiosk in parallel this XPOS or just location who want to cashier to to make it absolutely manual process.  
Or it will add us additional functionality, for example when the player redeemed a card on redemption kiosk and want to confirm that he correctly.

**Nathan Carver**   35:24  
M.

**Pavel Frolov**   35:34  
Transferred his money to the card, then Kashir can take his card already dispensed. A swipe it on Flex POS and get all the records related to this card.  
What ticket? What electronic ticket it was related to and so on.

**Juan Martinez**   35:55  
Right. Yeah, Nathan, I I would just like duplicate the tabletop dispenser box, put one below it with the second arrow from Flex POS and then rename that second one manual gift card swipe.

**Nathan Carver**   36:17  
OK, perfect.

**Pavel Frolov**   36:20  
Um.

**Nathan Carver**   36:33  
OK.  
So the Flex OS will come in if.  
Um, in this setup if the kiosk is.  
Um.  
Out of service for whatever reason it's not able to.  
Accept the gift card or accept the E wallet and the player's not able to redeem.  
From the kiosk, so they will go to the counter where they'll interact with the flex PLS through the cashier.  
So the Flex OS would.  
Um, assuming that the kiosk is down, the Flex POS is then going to.  
Interact with the Um.

**Juan Martinez**   37:21  
The controls, the control server.

**Nathan Carver**   37:21  
I'm gonna call this.  
I'm gonna call this JVL Gateway.  
Do that later. Um.  
So this is going to interact with the gateway because we're going to assume that it it can't access the redemption kiosk at this point, right? So then that means that.

**Juan Martinez**   38:00  
Right, yes.

**Nathan Carver**   38:06  
It's gonna have access, so the JVL control server will have access to only data that's been synced from the kiosk as it's been.  
So the user comes, the player comes up, gets their E wallet and then goes to the machine and during that time.  
We want to immediately sync that transaction to the cloud so that that wallet balance is also available in the cloud. That way when let's say the kiosk goes down while they're at the game, they come back. That data has been pushed up to the cloud and available.

**Juan Martinez**   38:53  
Great.

**Val Levitan**   39:07  
This is more realistic scheme.

**Nathan Carver**   39:12  
OK, I got it.  
Let's move the gateway down here like this.  
I'm gonna do this.  
Clean it up a bit.  
E-wallet really sits inside this machine as a digital artifact.  
And then this is going to.  
Interact with the cloud gateway.  
OK, perfect.  
And then um.  
And.  
As an aside, as a backup to these is the flex PLS which has the.  
Ability to interact with the cloud gateway.  
And then we have our two.  
External.  
API is sitting on here.

**Pavel Frolov**   41:01  
May I ask a question? Well, when you added?

**Nathan Carver**   41:04  
Yes.

**Pavel Frolov**   41:11  
Oh, you already changed the export. Yeah, because it was a question related to SMIP because it not.

**Val Levitan**   41:19  
Yeah, it requires it needs all flex flex ports. Smith will not work here.

**Pavel Frolov**   41:19  
Able to. Mm-hmm. Yeah, I see.  
Sit.  
Mhm.  
So I I postponed my question.

**Val Levitan**   41:36  
I read your mind.

**Pavel Frolov**   41:39  
Um.

**Nathan Carver**   41:46  
So Val with this, this would represent two locations, correct?

**Juan Martinez**   41:51  
No, just one location.

**Nathan Carver**   41:52  
That.  
OK, so one location I see. So we could have a scenario where.  
I see.  
Let's do this. Let's create the scenario layer goes to.  
Kiosk A.  
Uh huh.  
Deposits cache or add cache uh received.  
To get.  
And then?  
The player goes to location B to cash out.  
So he interacts with two separate kiosks in the location.  
Um.

**Juan Martinez**   42:55  
Oh, we lost the manual redemption option. If the tabletop dispenser is not wanted by the location or doesn't fit or whatever, we need to make sure we show that second option.

**Val Levitan**   43:09  
I created a cage here.

**Juan Martinez**   43:12  
Yeah.

**Val Levitan**   43:13  
The flex POS and the tabletop are within the cage wrench.  
And the player needs to approach the cage.

**Nathan Carver**   43:23  
Yeah.

**Juan Martinez**   43:23  
Yeah, we just need to slide up that manual gift swipe that's there in the bottom back inside the cage.

**Nathan Carver**   43:32  
Got it. We can. That makes sense.  
OK, so the player will also interact with the cage.  
Mhm.

**Val Levitan**   43:59  
What is a manual gift swipe? I don't understand.

**Juan Martinez**   44:02  
If the location does not have room or does not want a tabletop dispenser, we always said that Flex POS could. They could manually swipe the card and encode it that way without a dispenser.

**Val Levitan**   44:20  
Oh, I see.

**Juan Martinez**   44:24  
And then I I know we we said we didn't want a network switch or network hub, but right now we do not have any of the machines or their flex ports connected to the network.

**Val Levitan**   44:36  
Yes, I put a router in here.

**Nathan Carver**   44:42  
OK, yeah, so this they're all gonna be connected.

**Val Levitan**   44:49  
Yeah.  
And I think what's maybe what we should do is to bring flex sport.  
Within the machine.  
I think what's important to show here is that it's not a flex port that's connected here, but rather a machine is connected. Flex port is within a machine.

**Juan Martinez**   46:10  
Right.

**Nathan Carver**   46:12  
OK. Yeah.  
OK.  
OK.

**Val Levitan**   47:12  
Does the redemption key off connect to the router?

**Pavel Frolov**   47:17  
Definitely.

**Juan Martinez**   47:18  
Yeah, definitely.

**Nathan Carver**   47:19  
Yes.

**Juan Martinez**   47:21  
And just most routers only have 5 ports, so we're probably still going to need a network switch.

**Nathan Carver**   47:42  
Yeah, that would make sense.

**Pavel Frolov**   47:51  
And also we will need to connect the tabletop dispenser and Flex POS also to the same router.

**Genadi Peari**   48:39  
What will be the difference between 2 SAS and one SAS machine?

**Nathan Carver**   48:40  
Mhm.

**Val Levitan**   48:43  
I want to show that either one SAS or two SAS are applicable here.

**Genadi Peari**   48:48  
Yeah, so basically we don't need second sauce.

**Val Levitan**   48:55  
Uh.

**Genadi Peari**   48:55  
Oh, we don't need machine with two sauce, right?

**Pavel Frolov**   48:56  
Mhm.

**Juan Martinez**   49:03  
Oh no, I guess the statement is we we support a machine with two SAS, not that we need it or not, but that a more modern machine could be connected as well.

**Val Levitan**   49:16  
That's that's the exact statement, yes.

**Pavel Frolov**   49:25  
You know, in this case we will use same free export but with different software that supports communication via SAS instead of pulses.

**Juan Martinez**   49:38  
OK.

**Genadi Peari**   49:39  
Right. Yeah, understood.

**Nathan Carver**   50:13  
OK.  
All right. Any other devices that we need to add to the?  
Into the.

**Genadi Peari**   50:24  
I I put here the square which is.  
It it seems that flex port is different flex port. I mean much simple. It's simplified device, just needs a GUI for interaction with the player in the scanner.  
Doesn't have to be robust.  
Big device.

**Nathan Carver**   50:49  
OK.

**Genadi Peari**   50:50  
I.  
It seems like one board device, OCD and the.  
Couple connectors.

**Pavel Frolov**   51:12  
OK.

**Genadi Peari**   51:15  
Do you want to call it differently? Flexport?

**Val Levitan**   51:19  
Well, I I guess.

**Genadi Peari**   51:20  
For for for no BV machine.  
Because the whole idea of the flex port to get signals from the block center, right?

**Juan Martinez**   51:25  
OK.  
Yeah. Is it a significant price difference? I mean, does it, is it worth managing two different flavors of the unit or just having the one robust unit that can do it all?

**Nathan Carver**   51:36  
Yes.

**Genadi Peari**   51:45  
It's will be price wise it's will be similar to right the.

**Nathan Carver**   51:48  
OK.

**Val Levitan**   51:52  
No, no, it can't be because you need the touch screen controller.

**Genadi Peari**   51:57  
Yeah, yeah, I I mean electronics. I mean the the board is like a similar to Smith.

**Val Levitan**   52:03  
No, but you need a video.

**Genadi Peari**   52:05  
Yeah, you need to add the on this board you need to add the monitor with touch screen and you need scanner, but the electronics will be one board only.

**Nathan Carver**   52:08  
2\.

**Val Levitan**   52:16  
I know, but the price will be more, I mean cost will be more or less the same.  
There will be very small difference in cost. So the question is.  
For this difference, should we have two devices, 2 flavors?

**Juan Martinez**   52:38  
Well, and then if in this scenario we're doing e-wallet, so you have to verify your PIN at the device. Every machine needs a display.  
There is no PIN verification and scanning without the complete Flexport device, right?  
You need the the GUI that Pavel introduced there that you know everything needs a GUI because you have to enter your pin number.

**Pavel Frolov**   53:08  
Yes, yes.

**Juan Martinez**   53:11  
Hence the reason is that we have the one flexport device across everything.

**Genadi Peari**   53:11  
Hey.  
I would say it's much it's the flex port is 3 boards needs to be connected and assembled and all them the three boards needs to be tested. One is definitely.

**Pavel Frolov**   53:21  
I.

**Nathan Carver**   53:26  
Yes.

**Genadi Peari**   53:36  
Much simpler.  
Let's say at least 115 minutes in assembly.

**Val Levitan**   53:47  
Well, let's let's talk about it later. Let's let's not.

**Genadi Peari**   53:51  
Yeah, yeah.

**Nathan Carver**   54:02  
All right, so these are going to connect to.  
JBL cloud, right?

**Val Levitan**   54:22  
What does SSL stand for?

**Nathan Carver**   54:25  
And that's gonna be our.  
And I think this is where what Paul is using, but our secured socket layer connection to the control servers.  
So the.  
Because not all the devices in now are going to be able to communicate with the control server, so just the two key redemption kiosk and the flex POS.  
So they'll create, they'll establish an SSL connection to the control server.  
Um, but we'll want some type of.  
What type of communication will the flex ports be using with the kiosk?

**Pavel Frolov**   55:18  
Uh, security web socket.  
VSS.

**Nathan Carver**   55:25  
What was it?

**Pavel Frolov**   55:29  
Uh, Websocket. This secure security level layer are over it.

**Nathan Carver**   55:31  
Websocket OK.  
OK, since it here works out.

**Pavel Frolov**   55:40  
You can write it as VSS.

**Val Levitan**   55:45  
WSS.

**Pavel Frolov**   55:47  
Oh, sorry, double.

**Nathan Carver**   55:50  
OK. And that's.

**Pavel Frolov**   55:51  
Web socket secure.

**Nathan Carver**   55:55  
OK. And this is still SSL for the others, correct? Or is it also WSS?

**Pavel Frolov**   56:01  
Yes.

**Nathan Carver**   56:05  
Yes, it's still SSL.

**Val Levitan**   56:10  
Yes, yes, WSS, I understand.

**Nathan Carver**   56:10  
OK, uh.  
OK, got it. Perfect. OK, so the whole ecosystem will be using.  
OK.  
OK, so these boards, um.  
Are these?  
Are these running? Are they small Linux boards? Are they the what is it? The STM?

**Juan Martinez**   56:43  
The arm.

**Pavel Frolov**   56:44  
That's Tim.

**Nathan Carver**   56:44  
STM OK.

**Val Levitan**   56:44  
Yes.

**Juan Martinez**   56:51  
I I saw in the documentation we noted a flex port 2\. Does that change anything for this flex port two or is it still gonna be a STM?

**Genadi Peari**   57:04  
Still listening.

**Pavel Frolov**   57:05  
That's Tim.

**Juan Martinez**   57:06  
OK.

**Nathan Carver**   59:42  
OK, so any other components we need to add in here?

**Juan Martinez**   1:00:04  
Have it covered.  
I think we have everything, Nathan.

**Nathan Carver**   1:00:47  
OK.  
Oops.  
OK, so maybe the next thing is we start poking at.  
The vulnerabilities.  
Like what are what are the failure points?  
In the system.  
These could be what? What's the risk of a component going down or becoming disabled or the risk of?  
Uh, someone attempting to commit fraud on the system.  
So I think, um, just the Flex POS seems to be probably the biggest point because that's where.  
Um.  
The cashier is gonna have access to to the Flex POS, you know, regularly.

**Juan Martinez**   1:02:42  
Yeah, but even you know from a starting point, when you insert your cash into a redemption kiosk, you've created your pin, you you then get your e-wallet ticket. What?  
The synchronization that you mentioned earlier, what active security do we we have in place that prevents me from making a quick photocopy of that ticket and trying to scan the same ticket at two machines?

**Nathan Carver**   1:03:23  
Gotcha. OK.

**Pavel Frolov**   1:03:23  
Actually in this case if we have transaction approach to all the tickets, it doesn't matter what you are scanning, you will not be able to double take.  
Double take money from ticket.  
Because when the second device will do this, it will get the message that this ticket contains 0 amount if it if it all if it was already transferred.

**Juan Martinez**   1:04:00  
Right, Pavel, but that scenario, let's just say you simultaneously enter the tickets. There has to be a little time gap there, correct? I mean when when you when the first machine accepted, you know one nanosecond before the second one.

**Pavel Frolov**   1:04:15  
But.  
But all the time we have only one processor who process all the money and one of the device.  
Will be a first and the second will be the second in this approach, yeah.

**Juan Martinez**   1:04:39  
OK, understood. Understood. OK.

**Pavel Frolov**   1:04:42  
It's impossible to to do it immediately for two machines.

**Nathan Carver**   1:04:48  
So if kiosk A is the designated transaction processor, kiosk B is just forwarding.  
All requests to a for processing.

**Juan Martinez**   1:05:05  
No, no. Both A\&B can work simultaneously in the sense of you have two lines of players inserting cash into the redemption kiosk, each one getting their own e-wallet ticket, and both kiosks are communicating with the control server.

**Nathan Carver**   1:05:20  
Correct.  
In this in the event that the control server isn't available.  
Internet is down. Both kiosks are still operational.  
Is when probably referring to the processor is that that's one of the kiosks becomes the main processor for the location.

**Pavel Frolov**   1:05:51  
As I have already said, it's the main application who process all the tickets can be installed on one of the redemption kiosk or on Flex POS.

**Nathan Carver**   1:06:04  
I see. I see.

**Pavel Frolov**   1:06:06  
Or on separate hardware location server, location server. That's why I put two different boxes, location and cloud. So probably as optional device we can.

**Nathan Carver**   1:06:10  
Got it.  
I see.

**Val Levitan**   1:06:21  
Yeah.

**Pavel Frolov**   1:06:24  
Uh, add location server, location ticket server for example.

**Nathan Carver**   1:06:30  
OK, so there's this I see.

**Juan Martinez**   1:06:33  
I I thought that's what the the control server was that that was on on property physical.

**Val Levitan**   1:06:40  
Right. That's what I thought as well.

**Nathan Carver**   1:06:44  
So it's it's an application so.  
And what Pavel's saying is that this application can could run on any of the devices, so it's.

**Val Levitan**   1:06:55  
E.

**Nathan Carver**   1:06:59  
So for example, if we set up the site and we install this application here, then redemption kiosk A becomes.  
Essentially the processor host for the location.  
But it can be installed on any. It can be installed on Flex POS or Redemption Chaos B is what Paul's is my understanding.  
The other option is to have an another device or just a PC in in sense that acts as this processor for the location.  
And this.  
Is a mitigation.  
For this, um, I'll take its.  
Process through central application.

**Juan Martinez**   1:07:57  
Yeah, if if we don't have a physical hardware that's doing the processing application, then the location and or Felipe's team always has to know which kiosk is acting as the processor if you're doing any service or replacement.

**Nathan Carver**   1:07:57  
Yes.

**Juan Martinez**   1:08:16  
Versus them being plug and play minus some mild setup because we have an external piece of hardware doing the processing.

**Pavel Frolov**   1:08:26  
Yeah, or probably we need the flexible graphic user interface on control on GVL control server gateway as it will show for each location.  
Who is master?  
On this location and easily swap device to be master if if you have several devices that can work as master.

**Nathan Carver**   1:08:50  
Mm.

**Juan Martinez**   1:08:59  
Sure.

**Pavel Frolov**   1:09:03  
And able to do this remotely ideally.

**Nathan Carver**   1:09:25  
So if it was, yeah, if this was installed on its own device, then that becomes much easier to hot swap right to to replace it.

**Juan Martinez**   1:09:35  
No, not on the contrary. So the my concern is the remote part sounds wonderful, but in practicality, Pavel, you know the this unit's going to go down on a Friday night at 10:00 PM when you and the team are dead asleep. So there is.

**Pavel Frolov**   1:09:36  
Yeah.

**Juan Martinez**   1:09:55  
There's no remote, you know, there's that gap where we're just going to be down for an extended period of time due to resources.

**Pavel Frolov**   1:10:07  
Mhm.

**Juan Martinez**   1:10:09  
I'm just. I just need to brainstorm on that.  
Whereas if the processing application was on that robust server that we talked about, just something that's a little more sturdy that we can count on, that's just it makes it easier.  
Uh to deal with from a location perspective.

**Nathan Carver**   1:10:31  
Mhm.

**Pavel Frolov**   1:10:44  
Yeah.

**Nathan Carver**   1:10:54  
Could it be that both kiosks have a processing application, but it has the ability to designate one as the?  
The primary, and if the primary is not available, it falls back to a secondary.

**Pavel Frolov**   1:11:09  
I I hope you can support different operations for location who require more reliability then we can add additional device with.  
Ability to operate like a server.

**Nathan Carver**   1:11:29  
Hmm.

**Pavel Frolov**   1:11:30  
And all devices will connect there and all other devices will be hot swappable without any additional I I assume operation. If location want to to have as cheap solution as possible then.  
We can install everything on one device like kiosk.  
And it's always.

**Juan Martinez**   1:12:00  
Yeah, Paul, just to confirm those. So the processing application by default it will be on every kiosk and it will be on the POS you you will just enable or disable it. OK, OK.

**Pavel Frolov**   1:12:02  
So.  
Yes, yes, yes, yes.  
Yes, yes, definitely.

**Juan Martinez**   1:12:18  
Nathan, I think that's what your question was.

**Nathan Carver**   1:12:20  
Yeah, OK, that makes sense.  
OK.

**Pavel Frolov**   1:12:26  
During installation we can select either to enable or disable this option.

**Juan Martinez**   1:12:33  
OK.

**Val Levitan**   1:12:34  
So in the event, Pavel, I have a question in the event of this diagram where there are multiple kiosks and point of sale and it's a busy location.  
And I'm reimagining the question that Juan had asked is Friday night, 8:00 PM, Minska sound asleep. There's nobody to provide emergency service.  
Nobody understands how things really work.  
Are you saying that the processing application is installed on every device and if one device goes down then the other application becomes automatically redundant and takes up?  
No.

**Pavel Frolov**   1:13:30  
No, not as MVD. Probably we can review the schematic to to have a distributed database and see syncing on the fly between all the devices.  
But as MVPI think we can support during installation to select either to have a separate server with processor or to set one of the device as a master.  
For such location with lots of different devices, I think to have a separate server probably will be a good idea.

**Val Levitan**   1:14:22  
But if it's a good idea to have.  
A server.  
A dedicated server for a busy location. Why is it a bad idea to have?  
A dedicated server for a small location.

**Pavel Frolov**   1:14:41  
Just to save money.

**Juan Martinez**   1:14:59  
Yeah, the the more unique scenarios we create, the harder it is to manage.

**Val Levitan**   1:15:06  
Or how difficult is it to manage a distributed database?

**Pavel Frolov**   1:15:13  
Actually, I don't know.  
I I think it at least needs some experimenting.

**Nathan Carver**   1:15:21  
Yeah, so you would. It's essentially a cluster. You would cluster a the for example a kiosk a kiosk B.

**Pavel Frolov**   1:15:21  
Out.

**Nathan Carver**   1:15:31  
You would have set up an application that manages a database cluster across the two. Um.

**Val Levitan**   1:15:38  
But is the architecture of cluster database design a known entity or does it require some sort of a space agent engineering?

**Nathan Carver**   1:15:56  
It's it's been it's it's a known entity, so it's been around for quite some time. So the databases will essentially manage their own replication. There's different types that we could different complexities, but if we chose a common known type for our solution.

**Val Levitan**   1:16:07  
So.

**Nathan Carver**   1:16:16  
The engineering cost would be to implement the database replication would be, you know, acceptable I think.

**Val Levitan**   1:16:26  
So it's just a matter of setting.  
The correct requirements from the beginning for the engineering team. I mean if it's not a space age engineering and this is a known entity and the design points are all known even if we don't have the.  
In-house expertise, I'm sure that this particular design could be borrowed somewhere or subcontracted, and that piece could probably be given to us somehow. We can probably buy it somewhere.  
And say here's the cluster database cluster module that needs to be embedded and the rest is could be written by our own team. So my point is that if we properly set the requirements for design.  
Then.  
Uh, it becomes a known entity from the start.  
And we design accordingly. So then processing application versus processing server makes sense to me.  
Because it's it offers 2 advantage points, cost saving and redundancy in data.

**Nathan Carver**   1:17:57  
Um, yes.  
Yes, I think we could that I I believe that's worth exploring. I think that is an option. Um.  
So replicating the database and then there's the the centralized processing would be is not automatically part of that replication. So that's still an application that has to be managed.  
The essentially you have A\&B negotiating on who's the central processor. If A takes on that role, then A goes down, B has the ability to pick up that processing role and maintain it, so they would switch back and forth depending on events in the system.  
But with database replication, ideally it doesn't matter which one is the processor at that point, you just fail over to the other server.

**Val Levitan**   1:18:55  
So I'm just going to repeat just for clarity. I think that if cluster database design is a known entity, I suggest pointing to a processing application.  
Capability on every single device that we manufacture.  
Well, no, I should rephrase it. Instead of saying every single device, main products like redemption kiosk, like point of sale device, it should have a capability of having a processing application.  
Installed on it.  
And as part of the overall design requirement for the design architecture, we should immediately talk about.  
Database cluster design and cluster management and etcetera. I am not sure that I'm using proper engineering taxonomy, but I hope I'm being understood.

**Nathan Carver**   1:20:07  
Yeah, no, that makes sense to me.

**Val Levitan**   1:20:11  
Because the session, because this session is recorded, maybe Nathan should verbalize this in a in a proper with proper engineering taxonomy for the recording purposes as I'm afraid that I may may be introducing a mistake.

**Nathan Carver**   1:20:26  
No, I so you said it well. So the idea is that the systems are have the ability to take over. So we have two systems that have replicated databases.  
And they're on a cluster. The databases themselves are on a cluster. So system A goes down, B is able to take on the role of processing application. System A comes up, B will retain processing application until.  
A is able to now re all the data on B will be resynced back to A so that A's database is is now In Sync with B and then the system can decide that B should remain processing application or A takes on that role again.  
So that's the the basic approach we would take. Ideally we'll we can select database, most databases, no, I shouldn't say that except many databases will support clustering to some extent out-of-the-box. So it would just be as an engineering team picking the one that makes sense.  
And then designing the application system to work with that.

**Val Levitan**   1:21:46  
OK, so let's not forget to make it a requirement, a design requirement for a database engineering team.

**Pavel Frolov**   1:21:57  
James.

**Nathan Carver**   1:22:27  
Oh, I should say host.  
OK.  
All right.  
Um.  
OK, so that was the risk scenario that brought that up was player copies a ticket and attempts to scan 2 tickets or two people are scanning the same ticket.  
At Kiosk A and Kiosk B.  
In an attempt to get a double redemption.  
And in this setup.  
If they're scanned simultaneously, B would request A to process the ticket.  
And because A will be processing sequentially, one of those tickets will go through 1st and allowing A to detect a duplicate scan when the second one is processed.  
So that will be the mitigation.

**Genadi Peari**   1:23:37  
What is the GVL control server physically?  
What is the device?

**Nathan Carver**   1:23:48  
The.

**Pavel Frolov**   1:23:48  
It will be a cloud based uh server the.

**Genadi Peari**   1:23:52  
Oh, it's a cloud based.

**Pavel Frolov**   1:23:53  
It's.

**Nathan Carver**   1:24:00  
Yeah.  
OK, another risk scenario.

**Val Levitan**   1:24:18  
Um.

**Juan Martinez**   1:24:21  
Just at at the POS, if if this location does not have a table top dispenser or it's malfunctioning and they switch to manual gift card processing, I mean they must scan the ticket. It can't be fully manual. There must be a.  
Ticket from the guest and PIN verification must must take place. So while they're manually creating the gift card, it's still at least 50% automated by the scanning of the ticket. We just need to make sure that.

**Nathan Carver**   1:24:47  
Mhm.

**Juan Martinez**   1:24:56  
There there is no true full manual.  
Gift card creation.

**Nathan Carver**   1:25:04  
OK, so the a cashier is trying to create a gift card.

**Val Levitan**   1:25:07  
Maybe, maybe, maybe.  
Maybe we should just prohibit manual issues.

**Juan Martinez**   1:25:14  
Yeah, but Val, there there's gonna simply be locations that say I don't have room for the tabletop, I don't even want that. And I prefer to have that interaction with the guest and try to upsell them on store stuff. I just think that that's gonna be a real scenario.

**Pavel Frolov**   1:25:31  
We can support this prohibition by configuration, but still have this option for some locations. Give us more flexibility.

**Juan Martinez**   1:25:52  
Value muted. I don't know if you were gonna.  
OK.  
Uh.  
And I guess we we need to understand what happens, what remains operational if the Internet goes down.  
That may take a little bit of processing, but I think we need to understand what happens if if the Internet connection goes down.

**Nathan Carver**   1:26:21  
OK.  
All right, so the things I heard was 1A cashier attempting to create a a gift card using Flex POS.

**Pavel Frolov**   1:26:28  
What?

**Juan Martinez**   1:26:36  
Yes.

**Nathan Carver**   1:26:42  
What's that? Tense 2 create a fraudulent gift card redemption.  
A.

**Pavel Frolov**   1:26:58  
Mhm.

**Nathan Carver**   1:26:59  
take ticket and  
Oh.  
OK.  
And we said the mitigation for this was they're required to scan.  
Uh, and from.

**Juan Martinez**   1:27:20  
Or yeah, we're we're not gonna allow the manual entry. If you know today, in today's world, the player says, hey, I just cashed out $20.00 from machine four, they would type in $20 into their PAX device and generate a gift card. We're not gonna allow any manual entry. There must be a ticket.  
that is scanned, verified, and then the gift card would follow.

**Nathan Carver**   1:27:48  
OK, take it very.

**Val Levitan**   1:27:50  
But why? Why do we need to scan the ticket if we are wedging our POS between the printer and and the mother goose or the printer and our Smith board?

**Pavel Frolov**   1:28:06  
This is absolutely a different schematic describing us right now evolate architecture, but Muta goose is absolutely different.

**Val Levitan**   1:28:16  
Oh, I'm.

**Juan Martinez**   1:28:17  
Yeah, yeah.

**Val Levitan**   1:28:19  
Yes, yes, yes. I I apologize. I apologize.

**Nathan Carver**   1:28:26  
OK.

**Val Levitan**   1:28:27  
So we we are insisting on scanning the electronic wallet.

**Juan Martinez**   1:28:32  
Yes. And I I just think that that adds a layer of security that the player goes, Oh yeah, they're always scanning and verifying this ticket, you know, as well as the.

**Pavel Frolov**   1:28:34  
Yes.

**Val Levitan**   1:28:39  
Yeah.  
Yeah, no, that's. Oh, yeah, that's absolutely clear. I, you know, I totally understand this. Sorry, I made a.  
Unreasonable assumption.

**Nathan Carver**   1:29:01  
OK. And then Ron, you said Internet connection lost.

**Juan Martinez**   1:29:08  
Yeah, we we, I I think we just need to understand what components continue to work with 0 Internet connection.  
Or temporary tech.

**Pavel Frolov**   1:29:17  
Actually bank, yeah, bank will continue to operate except for regime meetings.

**Juan Martinez**   1:29:21  
Bye.

**Nathan Carver**   1:29:32  
Hmm.

**Juan Martinez**   1:29:32  
So I can I you can still go and insert your $20.00 and generate an e-wallet. You can take the e-wallet, scan it at the machine, you can play and then you you cash out your e-wallet and then you can go back to the kiosk and redeem the e-wallet.

**Pavel Frolov**   1:29:37  
Yes, yes.

**Juan Martinez**   1:29:51  
Uh, no, because Incomm's connection is down.

**Pavel Frolov**   1:29:56  
Yes.

**Juan Martinez**   1:29:56  
So you have to hold on to your ticket and come back later.

**Pavel Frolov**   1:30:01  
Yes.

**Juan Martinez**   1:30:01  
Or do we offer some sort of manual emergency solution? No. OK.  
Fire holds on to ticket until Internet is restored. You know that we we would recommend that the location take their information and they can contact them when the Internet connection has been restored.

**Pavel Frolov**   1:30:20  
Yes.

**Nathan Carver**   1:30:25  
OK.

**Pavel Frolov**   1:30:28  
Unless location will, yeah.

**Val Levitan**   1:30:29  
Or or we could or we could switch the location or location could switch themselves automatically on 3G or LTE modem.

**Pavel Frolov**   1:30:40  
Or probably they will still have option to.  
Uh, to avoid this ticket and provide some goods instead of uh winning.  
No, it will not be allowed next year.

**Juan Martinez**   1:30:59  
Yeah.

**Val Levitan**   1:31:00  
No, no.

**Juan Martinez**   1:31:01  
Not next year, no. Lottery tickets, yes, but no goods.

**Val Levitan**   1:31:06  
I know, but there's no validation process. You cannot validate the winnings. So let's let's not even go there because it's very easy for us to insist to switch the connection to LTE or 3G communication.

**Juan Martinez**   1:31:11  
Right, right, right.

**Val Levitan**   1:31:24  
We shouldn't. We shouldn't. We shouldn't even fall into that trap.

**Juan Martinez**   1:31:38  
So and not necessarily a risk but more of a recommendation based on what Val said Nathan is you know during our our sales pitch to locations we as part of this we need to recommend that they have a cellular backup solution that.

**Nathan Carver**   1:31:39  
OK.

**Juan Martinez**   1:31:55  
We could either piggyback on or or that they have available on an as needed basis.

**Nathan Carver**   1:32:07  
OK.  
OK, alright.  
OK, all right. Another risk scenario.  
Let's see.

**Juan Martinez**   1:32:45  
The scenario would be.  
I I cashed out my gift card, but I don't think I have all my money. Can the player Pavel immediately swipe the gift card on the redemption kiosk to verify balance?  
Or do they need to go to the POS to do this?

**Pavel Frolov**   1:33:08  
Uh mm-hmm.  
Actually it depends on if we really install a magnetic swiper on redemption kiosk.  
Probably we can implement this feature.

**Juan Martinez**   1:33:31  
Yeah, Gennady, I I I think we would want to do that. I mean, it's supposed to be a full-service kiosk. So if they want to verify their gift card amount before they leave, you know, we should not make them have to go to the cage.

**Pavel Frolov**   1:33:45  
Uh.

**Genadi Peari**   1:33:49  
Yeah, I think we need to edit.

**Pavel Frolov**   1:33:49  
Actually, actually, as I remember when we spoke to in calm, as they said something that in the future probably different type of cards will be able to use on location.  
To pay for games, so the same card can be used to enter money into redemption kiosk and to produce.  
You want a ticket?

**Juan Martinez**   1:34:24  
And actually though Pavel, in that scenario, we want them to go directly to the flex port and swipe there to transfer the monies to the machine. The problem is though, they don't have an e-wallet.

**Pavel Frolov**   1:34:40  
Hello.

**Juan Martinez**   1:34:40  
That might be a different scenario.

**Pavel Frolov**   1:34:42  
Yeah, yeah. Initially I think we have support and ability to install card reader on flex port.

**Juan Martinez**   1:34:59  
Mhm.

**Pavel Frolov**   1:35:01  
Yes.  
But I think this is not an MVP for nearest fusion.

**Genadi Peari**   1:35:09  
So do we add the swipe magnetic creator on the redemption key? It's to be added here.

**Juan Martinez**   1:35:17  
Yeah, I think so because if the location does not have a flex POS, they that that is the only place where they can swipe and verify the amount on the card.  
Plus that also allows them to come back tomorrow with the card and and convert the gift card into an e-wallet.  
You know, if they're not able to swipe it at the kiosk, then that's money we're not getting.

**Genadi Peari**   1:35:56  
OK, right.

**Nathan Carver**   1:36:01  
OK, so for verifying the amount and the player would swipe the card at.  
Um.  
And a kiosk or the Flex PLS or both?

**Juan Martinez**   1:36:15  
I.  
Believe it would be both problem though.

**Nathan Carver**   1:36:19  
So anywhere they.

**Pavel Frolov**   1:36:21  
Actually I'm not sure that right now it will work with current currently used cards, but I think we need to take this in mind and try to to investigate.

**Juan Martinez**   1:36:38  
OK.

**Pavel Frolov**   1:36:39  
If we really have have API to get amount from uh redeemed card.

**Nathan Carver**   1:36:39  
So in this case they would have to.  
And does income? Is there a number on the cards for to call income and it gives them a a balance?

**Juan Martinez**   1:36:54  
Yes.  
There is. There's a number and with a website on the back of the card.

**Nathan Carver**   1:36:59  
OK.  
OK.

**Juan Martinez**   1:37:03  
But that that means they leave the location often to do that, or, you know, go outside or whatever. Ideally we would want them to be able to verify their card amount on the redemption kiosk, because that also means in the future they could swipe.  
The gift card at the redemption kiosk and convert it directly into E wallet funds and play.

**Pavel Frolov**   1:37:28  
Mhm.

**Juan Martinez**   1:37:30  
I'll take that as an action item and I'll follow up with income if if we can swipe to verify gift card balance.

**Nathan Carver**   1:37:46  
Well, if we so Incomm has a service I believe that we can call to get the balance. So we would just have to identify the card when they swipe it and then ask Incomm for the balance of that card I think is how it would work.

**Juan Martinez**   1:38:02  
Yes, in principle, yes, yeah.

**Nathan Carver**   1:38:02  
I believe, yeah, yeah. So it's just if we can read that card and get its ID.  
OK.  
OK.  
Um.  
Is there any risk to players or?  
Uh, anyone? Um, actually.  
Disconnecting one of the wires and attempting to plug it into there.  
To their laptop to try to gain access to the closed network or to directly attack a kiosk across the network.

**Pavel Frolov**   1:39:03  
Mm.  
Yeah, it's always possible. It's always possible.

**Juan Martinez**   1:39:15  
I guess, Nathan, we we if we end up with a network switch in addition to the router, I mean we could enable port security so that you know you'd literally have to disconnect one device to reconnect or another.  
So we we could do port security at a switch level.

**Pavel Frolov**   1:39:34  
Probably on switch level we can monitor all mark addresses, addresses and fix them during installation or reinstallation.

**Juan Martinez**   1:39:48  
Sure.

**Nathan Carver**   1:39:49  
Hmm, I see.  
So we we would like we would register Mac.  
Addresses.  
Um.

**Juan Martinez**   1:40:02  
Pavel, how does that MAC address registration affect hot swapping?

**Pavel Frolov**   1:40:07  
Yeah, it it will make more difficult to to hot swap device in this case, yeah.  
Actually we can monitor Mac addresses of devices connected to process an application.  
It it will be easier to replace list of available Mac addresses on processing application via remote server.

**Nathan Carver**   1:40:51  
Yeah, and it could be similar to some of the.  
Um.  
Yeah, if we can register the Mac address or some other hardware key on the device when it is added to the network, that has to be.  
Um, for example, the processing application would.  
Register that.  
Device as a valid or as an accepted.  
Device on the network. So that would have to be done when the new when a device is swapped, that registration process would have to happen.

**Pavel Frolov**   1:41:36  
In any case, hot swap procedure will require some confirmation.

**Nathan Carver**   1:41:44  
Mhm.

**Pavel Frolov**   1:41:45  
In some form I think scanning QR code, entering some personal data on mobile phone and scan.  
Response on the machine to to enable hot swap for example.

**Nathan Carver**   1:42:19  
All right.  
OK, any other scenario we want to review?

**Juan Martinez**   1:42:48  
To digest this one.

**Nathan Carver**   1:42:53  
Uh, what's that?

**Juan Martinez**   1:42:55  
I said I think we need to digest this one first.

**Nathan Carver**   1:42:57  
Yeah, it's a lot.

**Pavel Frolov**   1:43:03  
Important scenario I think to think about the installation. So what procedures will need to be done during installation of the bank?

**Nathan Carver**   1:43:22  
Yeah.

**Juan Martinez**   1:43:38  
Oh yeah, on that note, Nathan, I'll share with you the income form which needs to be completed for each location because they require to know our terminal ID numbers for all the devices that they're gonna enable.

**Nathan Carver**   1:43:46  
It.  
OK.

**Juan Martinez**   1:44:13  
And that that process income has a disclaimer that it can take up to 36 hours to authorize a new location.

**Nathan Carver**   1:44:23  
OK.

**Val Levitan**   1:44:25  
We're coming on to the second hour of the of the meeting. I would like to suggest cancelling our mid iteration sync tomorrow.  
And instead for Thursday or Friday, maybe for Thursday, Boquinanada.  
Architectural discussion points.

**Juan Martinez**   1:44:54  
Agreed.

**Nathan Carver**   1:44:55  
Yep, that sounds good.

**Val Levitan**   1:45:01  
So let's do that. Let's wrap up this meeting, do the changes in the calendar. So cancel the meeting for tomorrow and book the meeting for Thursday for two hours.

**Nathan Carver**   1:45:03  
OK.  
OK, I can do that.  
All right, I will update the calendar and send out the transcript once it's.  
Once it's downloaded.

**Val Levitan**   1:45:33  
OK.  
Yeah, transcript in dot MD. OK.

**Juan Martinez**   1:45:34  
Good.

**Nathan Carver**   1:45:39  
Yep, sounds good.

**Val Levitan**   1:45:41  
OK.

**Genadi Peari**   1:45:42  
May may I just before we finish about the redemption center, how we envision this beside the machines between the machines still or it's stand alone similar to Flex pay?

**Val Levitan**   1:45:57  
It must be.

**Juan Martinez**   1:45:57  
It has to be all.

**Val Levitan**   1:45:59  
But the the design between the machine must be prevalent design because the machines don't have bill acceptors and printers, so we have to bring this device next to the machine.

**Juan Martinez**   1:46:00  
No.  
But Ral, if if room permits, I I agree that the ideal scenario was to make it as narrow as possible to fit in between machines. But if the location simply doesn't have room, then it needs to go wherever it'll fit. And psychologically, Val, I think the player.

**Nathan Carver**   1:46:20  
OK.

**Val Levitan**   1:46:29  
Yeah.

**Juan Martinez**   1:46:34  
It's easier to tell them through signage. Go here to start your journey like we did with Flexpay Kiosk is to direct them to the redemption kiosk when they walk in instead of attempting to 1st go directly to a machine.

**Pavel Frolov**   1:46:43  
Yeah.

**Juan Martinez**   1:46:50  
If it's not next to the machine, so we just need to be open about that.

**Val Levitan**   1:46:58  
Does it mean that are you suggesting different size devices depending on the location?

**Juan Martinez**   1:47:06  
No, no, no. We we we try to make the smallest device that we can, but that knowing that it may not be able to go in between two machines at a certain location and it has to be off to the side and when it is off to the side.  
You know that that helps train the player. Hey, when you walk in here, first go to that unit over there to start your journey for the day.

**Val Levitan**   1:47:31  
Yeah, OK. But I mean, I really don't see much of a difference in terms of in terms of a design.

**Nathan Carver**   1:47:33  
No.

**Juan Martinez**   1:47:40  
No.  
No, no. In terms of design, there's no difference. We should shoot for the smallest footprint we can and that we envision it being front loading and front servicing and that it be something that can be bolted to the floor, to the wall or to a machine.  
Slot base because you know if the smaller we make it, the easier it is to pick up and run out with it.

**Val Levitan**   1:48:13  
Well, the design of this device.  
There are a couple of constraints that we're working with. First of all, the width of the device, we want to make it approximately 8 inches.  
And the height of the device needs to be made in a way that.  
The number one, it's frontal service.

**Genadi Peari**   1:48:40  
Yeah.

**Val Levitan**   1:48:43  
And \#2 because it's.  
The the inner working so that it's heavy.  
It needs to.  
Because it's frontal service, you need to wheel it out. It kind of. It needs to roll out that you're using the floor for support, otherwise it will tip forward. It cannot overhang.

**Juan Martinez**   1:49:16  
So.

**Val Levitan**   1:49:16  
So it needs.  
It it needs, it needs to be wheeled out.

**Juan Martinez**   1:49:25  
So you're talking about sort of a a foot rest, foot pedestal mechanism that's somehow bolted to the floor, but then the unit slides out on some sort of track or rail?

**Val Levitan**   1:49:39  
It has rail internally, but as it slides out it becomes heavy, front loaded heavy, so aside from being fastened to the floor.

**Juan Martinez**   1:49:49  
Right.

**Val Levitan**   1:49:55  
Or having a rigid pedestal sitting on the floor. It needs to be supported like there has to be a front wheel that.  
Instead of counter delivering it.  
It needs to be supported in the front, so it needs to have frontal space.

**Juan Martinez**   1:50:22  
What the only what I only problem my envision here is while the unit can be limited to 8 inches wide, an 8 inch wide pedestal is not big enough to support that unit. So but the pedestal could be wedged in between underneath machines if if they're.

**Nathan Carver**   1:50:41  
OK.

**Juan Martinez**   1:50:42  
Those are not fixed to the floor, but I can't see a pedestal only being 8 inches wide to support such a heavy unit.

**Val Levitan**   1:50:51  
Well, how deep is it?  
I mean 88 inches will just, you know, make sure that it doesn't fall, but the depth, but the depth is what makes it stable.

**Juan Martinez**   1:51:00  
Right.  
Yeah.

**Genadi Peari**   1:51:20  
But the stand alone machine, if we would be able to put the recycler inside the flex pay, would it be good solution?

**Juan Martinez**   1:51:32  
Mm.

**Val Levitan**   1:51:33  
You don't understand. Say it again.

**Genadi Peari**   1:51:35  
If we would put the recycler inside the flex Bay, our existing flex Bay.

**Nathan Carver**   1:51:43  
OK.

**Genadi Peari**   1:51:45  
Would it be good for a standalone solution as it's it's heavy, it's nice.

**Val Levitan**   1:51:52  
But we're talking about locations that don't have room.  
And we're putting a larger unit. How does it?  
Makes sense.

**Juan Martinez**   1:52:11  
Gennady, I I would only suggest is if if we were to consider flex pay that if the monitor were able to be shifted to be portrait instead of landscape to make it a little more narrower.  
Perhaps. But yeah, I I'm just having a hard time envisioning it going between the machines. Val, now that I've seen several locations and you know, they're we're fighting for space in a lot of these locations. It's just.

**Nathan Carver**   1:52:34  
Oh.

**Juan Martinez**   1:52:45  
It's tough.

**Genadi Peari**   1:52:47  
I'm not saying to put in beside between the machines.

**Juan Martinez**   1:52:51  
No, no, absolutely. Yeah. Like if you're thinking about Flexpay, then definitely it's not in between the machines.

**Genadi Peari**   1:53:03  
I'm not saying the device we will do will be instead of flex pay. I'm saying in addition because if we do flex pay, we can give an option. If it's stand alone, we can put flex pay with the recycler if it's no space location so we can do narrow.  
Power redemption, maybe just.  
Just the flexibility.

**Nathan Carver**   1:53:29  
OK.

**Val Levitan**   1:53:34  
Um.

**Nathan Carver**   1:53:49  
Sure.

**Juan Martinez**   1:53:51  
I mean, yeah, Flex pay kiosk, the way it stands today is represents the width of most kiosks that others are doing. But obviously that footprint also means that there's no way it's ever going to fit in between machines.

**Nathan Carver**   1:53:54  
Yeah.

**Juan Martinez**   1:54:11  
And we would, we would commit to having it separate from the machines if that's the route we want to go.

**Genadi Peari**   1:54:22  
Not questioning this, just saying for the standalone device it's better than to have standalone very narrow 8 inches device.

**Val Levitan**   1:54:33  
Kanati is saying to have two devices, one is 8 inch device and another one is the width of the current kiosk.

**Genadi Peari**   1:54:41  
Yeah.  
If you want to to fit in between the machines, yes, you'll have a narrow device, but if it's a big location, you want stand-alone nice machine.  
I mean, we already have it. Just just feed the recycling, so.

**Juan Martinez**   1:54:57  
Yeah.  
I guess. Could you sketch it out, Kanati, just to see dimensionally? Do you think it's just gonna get a little taller, basically?

**Nathan Carver**   1:55:11  
OK.

**Genadi Peari**   1:55:18  
Oh no, it's same.

**Juan Martinez**   1:55:20  
It'll fit.

**Genadi Peari**   1:55:21  
I I mean if we will be able to feed the recycler, I'm not sure yet, but.

**Juan Martinez**   1:55:25  
OK.  
The only advantage there, Val, is certainly Flexpay kiosk is heavier. It's harder for someone to try to steal. It's more in line with what other kiosks normally look like, so there is that advantage.

**Val Levitan**   1:55:54  
I just want to make sure that we understand each other. You're saying that a smaller location.  
Most likely will not be able to accommodate and an 8 inch.  
Wedge.  
Or a a device wedged into an 8 inch space between the machine and you you would you are imagining a device that is not.

**Juan Martinez**   1:56:23  
Correct.

**Val Levitan**   1:56:31  
Adjacent to the machine, but somewhere, you know, few steps away or opposite to the machines.

**Juan Martinez**   1:56:41  
Correct. And and that's the typical of of what you see is the kiosks are either at the end of the machines or somewhere else. It's a network device and you can put it wherever it might even be placed next to the casinos or the locations existing ATM machine or whatever.  
And and where there might be room. It's just that where the machines are themselves, there's usually not that kind of room because the machines are butted up against each other with limited space.

**Nathan Carver**   1:57:11  
OK.

**Val Levitan**   1:57:14  
OK, so personally, I look at it differently, but it's not a matter of my opinion versus yours. Let's go with your opinion and let's.  
Approach it from this perspective. So would you rather see an 8 inch?  
With device stand alone or instead of the 8 inch device.  
The current width of the kiosk, let's say 30 inch device or.

**Juan Martinez**   1:57:49  
Well, I would say the only reason we came up with eight inches was because we envisioned putting it between the machines. I would let me rephrase it. I I prefer the 8 inch solution because it's always easier to place a narrower device than a wider device, no matter where it goes.

**Val Levitan**   1:57:58  
And that's it.  
OK, so in this case.  
It will be essential to bolt the pedestal to the floor.

**Juan Martinez**   1:58:20  
Yes.

**Val Levitan**   1:58:21  
And from what I understand in many cases locations opposed to that, but then if we are manufacturing an 8 inch device that could sit.  
Uh could stand alone in the location.  
The condition of placing this device must be to bolt it to the floor.

**Juan Martinez**   1:58:47  
Bolted to the floor, or if the pedestal is wide enough and it's next to something heavy like an ATM, you could wedge it under the weight of the ATM that would hold the pedestal. I mean, there's a few options that.

**Val Levitan**   1:59:00  
We could, we could then we could also then make it as part of the requirement to have two separate shapes of pedestal.

**Juan Martinez**   1:59:10  
OK.

**Pavel Frolov**   1:59:10  
Mhm.

**Val Levitan**   1:59:10  
One pedestal with files or imitates the profile of the machine and another one is just larger profile, just like you know, heavy purpose.  
Purposely design large, large foot.

**Juan Martinez**   1:59:31  
Right.  
Or even a weighted foot where you know we add a, you know, 80 lbs for the pedestal.

**Nathan Carver**   1:59:34  
It.

**Val Levitan**   1:59:39  
Yeah, large weighted foot, yeah.

**Genadi Peari**   1:59:42  
Convert you to the back wall.

**Juan Martinez**   1:59:49  
Yeah, we don't have, you know, the location determines where they want that device and that that's the tough part.

**Val Levitan**   1:59:49  
Understand.

**Genadi Peari**   1:59:50  
Yes.

**Juan Martinez**   2:00:15  
We have any other questions guys?

**Pavel Frolov**   2:00:18  
Yeah.

**Val Levitan**   2:00:19  
No, that's it.

**Juan Martinez**   2:00:22  
All right. Thanks everybody.

**Val Levitan**   2:00:25  
So on Thursday, right?

**Pavel Frolov**   2:00:25  
Thank you.

**Nathan Carver**   2:00:26  
Yep, I just sent out. You should have the invite for Thursday at same time.

**Juan Martinez**   2:00:27  
Yeah.

**Pavel Frolov**   2:00:34  
Well, I I need 5 minutes to talk with you.

**Genadi Peari**   2:00:37  
Thank you.

**Val Levitan**   2:00:38  
Hey, let's let's take it in a different meeting.

**Pavel Frolov**   2:00:42  
Yeah.

**Nathan Carver**   2:00:43  
Thank you, everybody. Bye.

**Genadi Peari**   2:00:44  
Thanks, all.

**Val Levitan**   2:00:44  
Bye.

**Pavel Frolov**   2:00:45  
Right.

**Val Levitan** stopped transcription