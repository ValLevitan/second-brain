**Transcript**

August 20, 2025, 12:04PM

**Juan Martinez** started transcription

**Will Jones** 0:03  
Don't want to attract us later, but pleased to meet you, Nathan. I know we met in the other call, but I'm just trying to understand too what you're what you're doing for JVL right now. So I get an idea of you know what your position is that way.

**Nathan Carver** 0:15  
Sure. So Val's asked me to be the technical product, I guess manager at this point. So I focus more on the the technical documentation side and you use case writing and capability writing.

**Will Jones** 0:24  
Hmm.

**Nathan Carver** 0:32  
Where? And then Pavel and I will talk through and negotiate that. And then obviously Pavel's in charge of the engineering side of that. So it was just really a piece that Val felt he needed more, more.  
Momentum in is building up the requirements and capabilities from a technical perspective.

**Will Jones** 0:53  
OK.  
Yep. So are you writing user stories or use cases or both?

**Nathan Carver** 0:58  
And so I'm focused on use cases and capability grouping requirements under capabilities for the system. And this is really we're laser focused on flex POS at the moment, but this will bleed into all the the work obviously that we're going to do holistically for the flex systems.

**Will Jones** 1:19  
OK. And you have a casino background, is that true or is that the case? OK.

**Nathan Carver** 1:24  
No. So I'm learning a lot about the casino side. I have a software engineering background, so that's why Val brought me in for this this role.

**Will Jones** 1:29  
OK.  
OK, got it. Thanks for that. And I I don't know if my introduction was if you've heard otherwise too, but I do have a casino background working with Juan for many, many years anyway and I what I've been.  
What I've have contributed, I don't know exactly call that what I've been asked to, but what I have been able to contribute is the requirements for the historical horse racing. And then we had a stint where we went through the bingo side, the central terminent systems.  
So I suppose you'd call it more like the regulated game focus on on that point and most of I we took the regulations, extracted requirements from them and then wrote user stories from that and the user stories. An interesting thing that I hadn't done before, the user stories ended more.

**Nathan Carver** 2:11  
Yeah.

**Will Jones** 2:25  
With actual users of our system and started only briefly, but started with writing user stories from developers perspectives, which is not my traditional background would be to take those user stories and transition into tasks for developers.

**Nathan Carver** 2:35  
It.

**Will Jones** 2:43  
So but in any case it was that that's that was where we kind of left off with what I contributed I suppose last time in the in that space and then I went on to help with you know guide if you will with the.  
Architectural discussion on HHR. So again, much more not CMS, much more focused on game function interaction with the HHR system that that provides all the actual outcomes.

**Nathan Carver** 3:00  
OK.  
Got it.

**Will Jones** 3:13  
So in any case, there just threw that out there so that we could get maybe on the same page understanding what we can contribute that way. I'm not entirely sure what my best role is with this discussion here, but I'll certainly ask a lot of questions and learn.

**Nathan Carver** 3:15  
Yeah.  
All right, sounds good.

**Juan Martinez** 3:31  
Absolutely. Great. Thanks for that. Well, let me share my screen here. So just let me go over some points here.  
Everybody see my screen there?

**Pavel Frolov** 3:52  
Yes.

**Will Jones** 3:52  
Yes.

**Juan Martinez** 3:53  
Yeah, so I I just want to.  
Go over first, but based on all of our availabilities, the next two weeks are just a bit rough. But I do we and I want to adjust these timelines. So I'm in Georgia this week, I'm in South Dakota the next two weeks.  
This meeting on the 28th, I have a meeting with the state lottery in the morning and then the 29th. I just don't know my availability yet, so I'm gonna, I'm gonna go through my calendar in deep detail.  
Number one, October 15th for the deep dive session for CMS, I think that that's fair, that's far out enough. November 15th for HHR reporting, I do believe that that that's fair based on what how far we've already gotten and and continue to move.  
But obviously our our main focus continues to be the beta testing of the Flexpay devices for January and and that is we want to deliver these to a set of partner customers in Georgia.  
So that we will have a functional product and several flavors of the product and analyzing gathering data from our partner customers and then July 1st that date is when the.  
Regulations that drive this Georgia product are in full effect, meaning the only way a player can get paid in Georgia after July 1st of next year is by their cash out being transferred on to.  
One or more types of MasterCard gift cards. There is legally no allowable cash processing. Everything has to go on to a MasterCard, which is accepted everywhere. MasterCard is accepted to further distance this product from anything that's like it.

**Nathan Carver** 6:02  
Yeah.

**Juan Martinez** 6:06  
Casino and involves cash. So Will, since you were out, I I don't know if we even had Flexpay conversations at all when you were here. So I just want to so the entire Flexpay ecosystem and Val did put up the good link with detail, but basically JVL is creating a series of.

**Will Jones** 6:15  
So.

**Juan Martinez** 6:27  
Devices for the Georgia market that will allow for player and location slash operator interaction to facilitate the cashing out of funds from the E GM onto the gift cards.

**Will Jones** 6:44  
OK.

**Juan Martinez** 6:44  
We're going to offer an e-wallet solution, we're going to offer a Tito solution, and the Flexpay device itself is a kiosk which can accept cash, scan a ticket and also dispense.  
A gift card and our really our main driving focus is the point of sale device Flex POS, which as the name says it all, we we hope to have a small tabletop device that will allow for the redemption of these cashouts.  
Through the existing system at these locations and it'll be an automated process to minimize fraud and transfer those cash outs onto the gift card. So that that is really our driving force is to get this hardware defined and made.  
And ready for customer trials in January of 2026.

**Will Jones** 7:46  
OK.

**Juan Martinez** 7:46  
I'm in Georgia this week. The product is operational even though it's in show mode. I'll I'll leave it at that. But the Flex pay kiosk physically exists. We have a the equivalent of a player tracking bracket or an I view Will as you know it, which is our flex port.

**Will Jones** 7:51  
Mm-hmm.  
Mhm.

**Juan Martinez** 8:06  
Device, which is a player facing device with a scanner and a display. And on the other side we've got the Tido, a mini Tido server operational with a SMB inside handling the SAS communications between our Flexpay kiosk and the EGM.

**Will Jones** 8:11  
Mm-hmm.

**Juan Martinez** 8:26  
To generate and redeem these Tito tickets. So the ecosystem is functional and we're displaying it this week at the George's show, which starts in about two hours, so.  
So you are just wanted you to be clear on that component.

**Will Jones** 8:41  
OK.  
So, but you're just you're you're doing it, it's actually live in casinos or it's live only in this demo environment for for customers during the show. Yeah, great.

**Juan Martinez** 8:49  
No, no.  
Correct. Just during the show and then back to our offices in Georgia for refinement and fine tuning and continued testing.

**Will Jones** 9:02  
So a couple question or a few questions on that. One is it is the the, you know, use of a SAS SMIB in order to connect it to third-party games. Is that what the purpose is there?

**Juan Martinez** 9:17  
Yes, ours and third party games, yes.

**Will Jones** 9:20  
OK. And then you mentioned a tabletop device. What is that tabletop device?

**Juan Martinez** 9:28  
Yes. So if if you've ever been to a gas station or any trendy coffee shop where they've got a little handheld square device that lets you pay with your Apple Pay or or or tap or whatever, we have a point of sale device.

**Will Jones** 9:40  
Mm-hmm.

**Juan Martinez** 9:43  
That will take the cash out from the EGM and convert it onto a gift card by also having a built-in gift card dispenser. So this device will allow a cashier or an attendant at a 711 to.

**Will Jones** 9:43  
M.  
Interesting. OK.

**Juan Martinez** 10:02  
11 to take this ticket, scan it, or receive the automated information from the ticket and then transfer those monies onto a MasterCard gift card to complete the guest's cash out ability.

**Will Jones** 10:19  
OK, so in the the system is interacting with some third party service that then is the gift card. I don't know to call it the the one who holds the funds for the gift card.

**Juan Martinez** 10:30  
Correct. There's two systems in place here. There's an existing system managing the machines, which is the legacy Georgia system. If you go back five years, everybody had it. We still believe that 90% of the market has it and it's called the Mother Goose.

**Will Jones** 10:37  
Yeah.  
Oh, OK.  
Mother goose.

**Juan Martinez** 10:49  
And basically, yeah, it's really cute. It's a serial Daisy chained machine to machine device that connects to multiple manufacturers and takes the pulses from the hard meters upon cash out.  
And can transfers that data onto the final interface board, which then talks to a thermal printer that says, hey, EGM #1 on this day at this time cashed out $20 and here's a reference.

**Will Jones** 11:05  
Yeah.  
Mm.

**Juan Martinez** 11:24  
We are going to intercept that output to that printer and then allow our point of sale device to say OK, machine #4, $20.00 this day and time. I will now print a MasterCard for $20.

**Will Jones** 11:25  
OK.

**Juan Martinez** 11:43  
There'll be a service fee for that privilege of $2.00. The guests will have to acknowledge that on the POS device, accept the terms and conditions, and then he can print.

**Will Jones** 11:44  
I think.  
Uh.  
Then take it. Yeah, the card. Yeah, OK, yeah, these cards are all just pre-printed. And of course it's just using the ID or the information that's embedded on the card to associate it with that account that now has the funds deposited.

**Juan Martinez** 11:59  
And take the card, yes.  
No, the the account is on the card. There's a bar code on the back and you can go online. These cards are blank when the locations get them and they're encoded by swiping it at the point of sale device or.

**Will Jones** 12:23  
Yeah.

**Juan Martinez** 12:30  
As part of the card dispenser device, it's scanning and encoding the amount onto the card and we're dealing with a processor called Incom that has the exclusive MasterCard contract through an API and we say, hey, we just put 20.

**Will Jones** 12:38  
And.

**Juan Martinez** 12:49  
Dollars on this barcode please you know track, store and approve and and then they do that.

**Will Jones** 12:56  
Yeah, got it. But no chip, just the just the the strip on the card. Really similar to like a Starbucks gift card or things like that that that are cheap, cheap cards.

**Nathan Carver** 12:57  
OK.

**Juan Martinez** 13:06  
Correct, correct, correct. OK.

**Will Jones** 13:07  
Yeah, so OK.  
Do we interface any player tracking? Is there any other information that we store about the player and issuing these cards? Are they completely anonymous?

**Juan Martinez** 13:15  
Yeah.  
No. So today in Georgia, there is no such thing as player tracking. Well, today by by definition. So the regulator doesn't govern the devices that facilitate this gift card program.

**Will Jones** 13:24  
Mm-hmm.

**Juan Martinez** 13:35  
But some of the operators have introduced A pseudo player tracking where you have to 1st get a card, the card belongs to you, and then the card is how you move monies from one machine to the other. But it's very clunky, so it's still anonymous because you pick up.

**Will Jones** 13:45  
Mm.  
Yeah.  
Yeah.

**Juan Martinez** 13:55  
The card when you walk into the location, although you could take it home and bring it back at no time have you said this card belongs to Juan Martinez or you don't sign up for it, or you can get a different one every time you arrive, so.  
Player tracking and player rewarding has been thrown out there, but the the legislation behind that is still very vague. And you know, these are transient players at gas stations and restaurants and there's no loyalty reward programs today to.

**Nathan Carver** 14:11  
OK.

**Will Jones** 14:15  
Mhm.

**Juan Martinez** 14:30  
Incentivize them to come back because they already come back. That's my gas station next to my house. I always go to that 711 for whatever reason because it's close to the office. So that that's still an evolving market here for player tracking.

**Will Jones** 14:33  
Yeah.  
OK, park this question or park this, but maybe just say yes or no. Any concern with like I think it was federal regulations where you have to register people's have have all the information about a person to create an actual funds account.

**Nathan Carver** 14:45  
No.

**Will Jones** 15:02  
So at least with like I I remember in say early 2000s we had to ensure that when we created a transact a actual account with front funds at a casino, we had enough information on the player to meet with the federal regulations on in creating these accounts. Otherwise it was.

**Juan Martinez** 15:14  
Mhm.

**Will Jones** 15:22  
Is considered a potential money laundering account. Is there any any rule like that that it's applying?

**Juan Martinez** 15:25  
Yes.  
No, because these are the this is in essence a prepaid card, identical to what you can go to a CVS or Walgreens to give somebody a $50 gift card. You're able to put 50 bucks on it.

**Will Jones** 15:41  
Yeah.  
Mhm.  
Mm.

**Juan Martinez** 15:47  
Anonymously, and it's the same premise. So because the these are amusement slash skill games in Georgia, they're not considered casino or true gaming devices. So while there's some mild PCI compliance.

**Nathan Carver** 15:56  
OK.

**Juan Martinez** 16:00  
They're still anonymous and and there's no W2G for taxes for jackpots that doesn't even exist in Georgia. So the answer is no, not for right now.

**Will Jones** 16:03  
Yeah.  
And what was the limit on starting a card?

**Juan Martinez** 16:15  
The limit, I I believe it's either five or seven dollars. I believe it's 5 dollars, $7.00 because oh, the Max limit right now is $1000.

**Will Jones** 16:16  
Like how much can you put on? Yeah.  
Max limit. Max limit actually.  
OK.

**Juan Martinez** 16:29  
Yep, and that's set by Incom, the MasterCard provider, and they will be applying velocity thresholds and security checks, checking for excessive card creations at a location that usually does three cards a day and all of a sudden they did 200 cards. So they have algorithms.

**Will Jones** 16:33  
Hmm.

**Juan Martinez** 16:49  
To track that and we will have to come up with our own as well for added security.

**Will Jones** 16:54  
OK, got it. Thank you for all those questions.

**Juan Martinez** 16:58  
No, no, no problem. So yes, Sir.

**Nathan Carver** 17:00  
Hey Juan, but on the flex pay, the line says flex pay is already added to the legacy CMS. Is that?  
Is that gonna come into the Flex POS side of this? Because I see July 1st is really the Flex POS, right, that we're really focused on and maybe we'll talk about that when we scope and improve.

**Juan Martinez** 17:16  
Uh, yeah, I'm good.  
Well, well, now July 1st is the true customer go live where no operator in Georgia after July 1st will be allowed to cash out a player without some device.  
That can transfer it directly to a MasterCard. Doesn't have to be a JVL device, any device that's that's allowed that that's what July 1st means. January 1st is when we want our units out in the field gathering data so we can react accordingly modify.

**Nathan Carver** 17:43  
Right.  
Sure.  
Yes.

**Juan Martinez** 18:00  
If needed to be ready for the final July 1st date.

**Nathan Carver** 18:01  
Mm.

**Juan Martinez** 18:05  
Yep, and I'm glad. So wait, let's jump to that question. So I I put on here Flexpay already added into legacy. What does this track? So this is a terrible screenshot here, but Pavel, this is from our CMS and you've since added a Flexpay manager tab and.  
I see several test kiosks here. You know, a key, a lease expiration date, software version, Mac address and their statuses. And there's two online. Are these two online, the ones currently in Georgia?

**Pavel Frolov** 18:46  
Oh, I think so. Yeah, I think so.

**Juan Martinez** 18:52  
OK, to my knowledge, this is the only addition regarding Flex pay or any flex ecosystem device in CMS, correct? There's nothing else in here.

**Pavel Frolov** 19:08  
Yeah.

**Juan Martinez** 19:08  
So can you just for all of our knowledge, what do you do with this? Why did you have to enter this into legacy CSM to support the Flex pay kiosks that are shown here?

**Pavel Frolov** 19:23  
Because we want to support remote initial setup feature, we want to apply or withdrawal visas the mechanisms that allows this kiosk to to work on the location.  
So if you press action with pencil it will open management screen that will give set of settings that can be applied.

**Juan Martinez** 19:49  
Mhm.

**Pavel Frolov** 19:59  
Remotely on the kiosk, for example to to change credential data related to income.

**Juan Martinez** 20:04  
Mhm.

**Pavel Frolov** 20:09  
To set some settings.  
And additional option to disable some device or enable it until some specified date.

**Juan Martinez** 20:24  
OK, so I guess in in a simple definition, this is the internal JVL administrator screen for the Flexpay kiosk.

**Pavel Frolov** 20:37  
Actual actual this screen will also be changed in future adding new new features, for example firmware update for Flex port.  
We will be able to send updated version of Flexport or Flexmip a firmware directly to the location to the final device.

**Juan Martinez** 21:04  
Right.  
OK. So yeah, and and Will you, you probably deep down already know this from your background, but so all of these devices, everything in the Flexpay ecosystem because we have to interact with income and via the Internet.  
All of these devices are essentially online for us where either the local Georgia team eventually or today Pavel's team has remote access to these devices when they get deployed at locations. So.

**Nathan Carver** 21:34  
Yeah.

**Juan Martinez** 21:43  
You know, the future CMS will have to facilitate a dashboard for the tracking and administration of these devices, firmware updates, all sorts of things like that.  
OK.

**Pavel Frolov** 22:02  
Remote access I I will I will make some some correction. Remote access is limited just an API that implemented between our CMS serial.

**Will Jones** 22:03  
Yeah, understood.

**Juan Martinez** 22:10  
Yes.

**Pavel Frolov** 22:20  
And the master device on location. So we have some proprietary WSS protocol to exchange data and also we have an option to.  
Request logs from the remote device and get this logs from the device and that's all for now.

**Juan Martinez** 22:42  
OK.  
OK, OK. So going back, let's go back to here. So current CMS documentation, you know, where is it located if available? Pavel, you know, Val always referred to CMS as tribal knowledge you guys created.  
You know about it. It's in the back of your head. You live and breathe CMS everyday. Are there official documentation scattered in many locations? In one location? Is there something for myself, Nathan and Will to start reading to understand?

**Nathan Carver** 23:17  
Mhm.

**Juan Martinez** 23:25  
And what CMS is and does.

**Pavel Frolov** 23:30  
Very difficult question. Actually I saw some.  
Not obsolete, but quite old API in self hosted phone plans many years ago. Don't know is it useful right now or not?  
And so I think probably more useful just to get last schematics diagrams that we probably updated last year.

**Nathan Carver** 24:08  
Cool.

**Pavel Frolov** 24:12  
To give the common understanding what features, what modules are used for the CMS as we already closed using.  
Miro boards where it was presented. I will need to find exported data probably until next meeting. I will prepare some schematics related to current implementation.

**Juan Martinez** 24:33  
Yeah.

**Pavel Frolov** 24:45  
Or probably we can just to create a new design from the scratch, keeping in mind that we are going to switch to new architecture.  
And I see it as a as a separate server. The first features of this server I think will be management of different payment.  
Terminals practically the same as you just shown us.  
From current CMS, but it will work based on yes this one, but probably it will be hosted on different server supporting POS towers.

**Juan Martinez** 25:27  
I mean this.

**Pavel Frolov** 25:40  
Dispenser devices. So the first feature will be to provide dashboard of all the devices. Also in my understanding it could be a management screen.  
Uh, with all the locations.

**Juan Martinez** 26:01  
Mhm.

**Pavel Frolov** 26:02  
This option to provide access for different operator to locations that belongs to them. So it it will be like a client portal.

**Juan Martinez** 26:13  
Correct.

**Pavel Frolov** 26:17  
But for each operator, it will be a different of you with the allocations, this ability to create new locations.  
To manage devices that belongs to them.

**Juan Martinez** 26:35  
Right. And yeah, so, yeah, so Will just so you're clear. Yeah. So I mean the the goal is once we start deploying and selling or leasing the flex pay devices is that they're self-administered by the.

**Pavel Frolov** 26:36  
And so on.

**Juan Martinez** 26:55  
The operators themselves, you know, we we would assist, but that they they have their own dashboard, they can log in, they can create and add users and and all sorts of things on their own to facilitate their their installations. In Georgia, you know there's this.  
4000 plus or 6000 plus locations. So it's almost impossible to manage from our perspective where the operators already have the infrastructure and technicians doing these multi location installations for many years now.  
So that that's our goal.

**Will Jones** 27:36  
Do yeah, have we captured the the requirements that are for this purpose? You know what what actions those users are actually gonna gonna do at the at those properties? Why they have to manage users and not just, you know, issue cards? What's the?  
What's the what? What's the purpose in allowing them to have more control over these devices as well?

**Juan Martinez** 28:00  
So this market today is set up where no manufacturer, including JVL, is allowed to directly sell to 711 number 2240.  
Georgia has a set up in their legislature, a middle man called a master location or master operator, and that is the person that we sell to. That master in turn services.

**Nathan Carver** 28:31  
Yeah.

**Juan Martinez** 28:34  
That's 711, a CVS, a Wild Wings restaurant. Those are his customers. So they're not open. And by design, the Georgia State Lottery reports, we JBL don't even know where our machines are installed.  
Because they're not obligated to tell us the the intralot reports mask our machine serial number with a state generated ID number that means nothing to us. So when I look at a report machine number 272240.  
Made this much money. I don't know where that machine is. I don't know if it's a vertical or horizontal. I don't know what game software it is in. It's on a different report, but I have very limited access on purpose to tracking the machines because by the definition of the legislature.  
Here, we're not Privy to that information. Our business technically ends when we've sold the machines to the master operator, who then deploys them in locations. Now that's changing a bit with the MasterCard process, what we're going to be allowed to contract with the location.  
For the fees and and installing of Internet lines and that kind of stuff, but the bulk of the information still is hidden from us per SE and we can only gather what we can gather.

**Will Jones** 30:22  
Mhm.  
Mm.

**Juan Martinez** 30:23  
You know, Light and Wonder and Aristocrats said we don't make kiosks. We're not getting in the business. We'll partner with whoever else other companies. IGT has partnered with the kiosk maker M3T. This company, Access out of Las Vegas and Easylink are supplying.  
Smith boards to do Tito and they're using a traditional cash dispensing kiosk or a cash dispensing kiosk that's been converted into a gift card dispensing kiosk. But there's there it's wild Wild West for lack of control and it.

**Will Jones** 30:56  
Mm.

**Juan Martinez** 31:03  
Where anyone is able to put something out there as long as it's it's somewhat credible and reliable.

**Will Jones** 31:09  
OK, so this master operator is both responsible for the kiosks that are going to just facilitate the cash to, you know, gaming funds transaction and then the the actual games themselves too and ensuring that the games stay up.

**Juan Martinez** 31:27  
That that is correct. Today, the JBL or any other manufacturer's technicians do not touch the machines. That is the function of the master and his employees and service technicians.

**Will Jones** 31:40  
Are these all these machines too?

**Juan Martinez** 31:42  
The lease, long-term payments and sales, all three models, no, no revenue sharing, only a a flat fee. We're not allowed to share in the revenue.

**Will Jones** 31:50  
OK.  
Yeah, OK. And that's still nice. You get the built-in network of service technicians through the master operator and don't have to obviously deal with any of that. These when we talk about a kiosk, you know, my original thought was a kiosk that looks like an ATM, but.

**Juan Martinez** 32:03  
Yes.

**Will Jones** 32:11  
Obviously you mentioned the the desktop or tabletop variant of it. Are there different manifestations of this kiosk that are beyond that too?

**Juan Martinez** 32:16  
Yeah.  
Absolutely. I mean, so others are installing what you would know as a traditional ticket redemption kiosk that you would see at any casino. Only instead of dispensing cash, it's dispensing the gift card. So these are the vertical, you know.

**Will Jones** 32:41  
Yeah.

**Juan Martinez** 32:41  
4-5 feet tall kiosks with large screens. And that's what most people are doing because they're being pushed into the concept of Tito that, hey, you need Tito, this is a kiosk that does it.

**Will Jones** 32:49  
Hmm.  
Hmm.

**Juan Martinez** 32:58  
And it can just do card dispensing on the side in addition to your your ticket redemption stations. So they're big and bulky and we we have let me just stop sharing this screen and I'll pull up our Flex pay device also is a small footprint kiosk.  
That is meant to facilitate that as well. Let me just pull that picture up here. So we we have, we we want to service all of the customer scenarios and give them whatever they want and that could be a.

**Will Jones** 33:30  
Mm.

**Juan Martinez** 33:35  
Uh, Vertical kiosk. Um.  
Share here.

**Will Jones** 33:42  
Ava, where's all this back end infrastructure hosted?

**Juan Martinez** 33:53  
So if you can see here's our EGM right next to it. We have two kiosks that we're displaying at the show this week. This this guy over here is configured to do e-wallet so it will produce what looks like a Tito ticket.

**Will Jones** 34:00  
Mhm.

**Juan Martinez** 34:08  
But the Tito ticket is a digital wallet storing the information and it does not actually go into the bill acceptor of the machine. We have an optical scanner on our player tracking interface that scans the ticket and the monies go onto and back off of.  
This E wallet ticket and then the software on the guy over here on the right is a traditional Tito server where the ticket does go in and out of the machine's bill acceptor and out of its printer and then comes back to the kiosk to be converted onto the.

**Will Jones** 34:30  
OK.

**Juan Martinez** 34:47  
Gift card which the device has a built in dispenser for a MasterCard gift card.

**Will Jones** 34:52  
So where this front money account, meaning the the the Tito tickets, that's all on Prem. There's a server there that that's managing the funds that each ticket is worth.

**Juan Martinez** 35:06  
I'll let Pavel answer, but I yeah, we don't have anything. The database for the tickets are inside of each flex pay right now.

**Pavel Frolov** 35:14  
Yeah, actually we just discuss how can we work with different types of tickets in the future, keeping in mind that we are going to support different types of devices. For example, I posted some of them.  
In the chat you can see Flex POS is a table top for small device. Flex tower it's self dispensing unit of self dispensing cards unit.  
And Flex pay our currently implemented device, but we assume that in future we can combine a bank equipment in any order, for example to place one POS device plus one tower.  
Flex POS plus POS, Flex pay plus POS and and so on. So keeping in mind that all of these devices contain smart hardware, each of them can work as a master device. Master device means.

**Will Jones** 36:09  
Mm.

**Pavel Frolov** 36:26  
Works with database, works with set of all tickets. Doesn't matter what the tickets are, either regular Tita or evaluate temporary, temporary valid ticket.  
So this master device can process all the tickets and all of these devices can support transferring these tickets into a card in different order. Probably some of them can.  
Directly provide to the player a card. For POS it it could be a manual procedure by swiping cards during redemption process.

**Will Jones** 37:16  
OK.

**Juan Martinez** 37:22  
2.  
So.  
Going back to oh, go ahead.

**Will Jones** 37:33  
So, but yeah, I guess I'm, I'm, I originally I was thinking that this was gonna be that you were trying to actually transfer funds to and from the card itself, but in this case you're still just using somewhat like a, you know, a.

**Nathan Carver** 37:35  
OK.

**Will Jones** 37:49  
Just a Tito system with a a live ticket that's that's functioning as the the mechanism for getting funds to and from machines and then at the end of the the session, that's when we're actually going to.  
Issue a new gift card. Is it ever? Are these these gift cards are only issued, correct? They're never. There's never a a mechanism for adding new funds to a previously issued.

**Juan Martinez** 38:18  
Yes. So today what you described is 100% correct that the final, final cash out of your gaming day gets done at a device directly onto the gift card and then you take the gift card and leave.  
Again, because the legislation is so loose, income is working on multiple solutions on what can be done with future gift cards and still be compliant within, you know, MasterCard safety protocols. But there is.  
A conversation going on about allowing the gift cards to be reloadable at the gaming devices through a scanner. So the those that's being sketched out now to allow you to move from machine to machine with the gift card.

**Will Jones** 39:01  
Mm-hmm.  
It's like.  
Yeah, I mean, I'm just looking to thinking through the, you know, do away with the gift card, make it a an e-card, make it so that it's either through a QR code or the or just through NFC at the terminal to be able to just walk around your mobile device. It's just a.

**Juan Martinez** 39:14  
Uh.

**Will Jones** 39:32  
Just a front money account completely.

**Juan Martinez** 39:35  
Yes. So the the problem is, is the Georgia Lottery picked income and the MasterCard network as one of two or three only authorized users. So right now the original cards even were a bright yellow with the Georgia Lottery logo on them, so.

**Will Jones** 39:45  
Yeah.

**Juan Martinez** 39:55  
That it was no mistaking that this was a specific card authorized by the lottery. That's since been done away with, and literally many changes have occurred within the last 12 months surrounding the cards.  
And that's because of the lack of true regulations that have allowed the MasterCard provider to to experiment with technologies.  
Yeah.

**Will Jones** 40:28  
A more practical way of walking around and not having to have a card all the time.

**Juan Martinez** 40:32  
Oh, no, absolutely. But yeah, the in the model today, there's even gift cards that are blank but hanging in their prepackaged envelopes. And the attendant at a 711 would just grab it off the shelf and then manually enter the amount that was won by the player. And that that leads to a lot of fraud.

**Will Jones** 40:49  
Yeah.  
Yeah, of course.

**Juan Martinez** 40:52  
When you're doing stuff manually, but a lot of that is what happens today is they're encoding those cards on the fly with little to no systems check as to what the dollar amount on the card should be.

**Will Jones** 41:06  
So what in the solution that you're showing today is, you know the are are the MVP items that have to be done before January? Like what's what isn't? What isn't there? Why are we talking about redoing things?

**Nathan Carver** 41:07  
Yes.

**Will Jones** 41:24  
In some new way, if you're showing something that is really close to what they want.

**Pavel Frolov** 41:30  
First of all, first of all, right now we just support current Flex pay that is directly communicates to in call.  
Um.  
Until January, we do show us that we need to switch communication to income to some cloud server to move it to to cloud due to security reasons.  
And Incomm advised us to to do this.  
Uh.

**Will Jones** 42:09  
And that's cloud server. So that means that the device is speaking to some cloud service and the cloud service is what's communicating with income, meaning that there's AB to B connection in the cloud.

**Pavel Frolov** 42:09  
All's, yeah.  
Yes, yes.

**Juan Martinez** 42:23  
Yes.

**Will Jones** 42:24  
OK. And and that's OK.

**Pavel Frolov** 42:28  
This is number one. Number two, we are going to produce Flex POS that will utilize absolutely different CPU architecture based on ARM.  
Processor. Actually I think the same platform will be used for dispenser unit or flex tower, probably something else. That's that is #2.  
Uh.  
Also we need to keep in mind actually three different models of operation. First of all, to use current Mutogus schema.  
So all all the location right now is using Mutakus and quite obsolete Smith boards to get data from the machine when it cash outs.  
Transfers this data to Mutagusa central device that can print receipt with the values that the player redeemed from the machine and now it's manually changed this.  
Piece of paper to get goods or yeah, lottery ticket or something else.

**Nathan Carver** 43:58  
OK.

**Juan Martinez** 44:04  
Or lottery tickets or whatever.

**Will Jones** 44:06  
Like, but like the piece of paper is proof. That's it. It's just that that little thing you just showed me. Yeah, I could easily print one of those with the machine, no problem. But is there on that piece of paper? Is there a barcode?

**Juan Martinez** 44:10  
Yes.

**Pavel Frolov** 44:12  
Yeah, just this one.

**Juan Martinez** 44:13  
Yeah, yeah, it's a receipt.  
No, no.

**Pavel Frolov** 44:22  
No, actually this device is placed on the cashier desk, so player do not have this piece of paper, it just goes directly to cashier.

**Will Jones** 44:24  
So if it.  
OK, but the cashier could enter what they want for this because they're reading something that's on there.

**Juan Martinez** 44:38  
Oh yeah.

**Nathan Carver** 44:38  
Yeah.

**Juan Martinez** 44:41  
Yeah, Will, on on that link to Confluence that Pavel shared, there's a picture of the ticket below the two. And yeah, that that is it. It's this is the craziest thing ever where, yeah, you're taking this receipt and they're paying you off that and and then manually typing in the matching or not matching.

**Nathan Carver** 44:41  
Correct.

**Will Jones** 44:45  
Yeah, picture of it, yeah.  
Wow.  
This.

**Juan Martinez** 45:01  
Amount onto the gift card.

**Will Jones** 45:01  
That's that's yeah it's it's funny this is this is sorry. This is a very quick aside then I'll let you back Pavel that yeah this this is very reminiscent of me walking into a you know it wasn't a double eyed trailer. It was a nicer casino than that. But in Oklahoma walking right by a Lambo who that was there for the the.  
General manager of the property, the the Indian, you know, is an Indian tribe and then going inside them saying that they can't get things to reconcile. And then they were taking all the Tito tickets or the tickets we produced and literally giving cash for the tickets and just putting them in a drawer, never even scanning the ******* ticket.  
You're like, well, no wonder why. Who's skimming? I wonder what's happening here. So anyway.

**Juan Martinez** 45:43  
Oh yeah, yeah, yeah.

**Pavel Frolov** 45:45  
So this this is schema number one. We just want to insert intercept signals from the muta goose, get this data to flex POS and provide.

**Will Jones** 45:55  
Yeah.

**Pavel Frolov** 46:02  
A way for the player to generate the card based on the data printer printed on this receipts.

**Will Jones** 46:13  
OK, and the Mother Goose is it was listening to a Sass pulse off of the game to do this.

**Pavel Frolov** 46:15  
The next, uh, yeah, yeah.

**Juan Martinez** 46:19  
No, no, no, no, no. You wish Will that these are old machines that predate SAS, so they they're intercepting the pulses from the bill acceptor on the input and listening to the pulses.

**Will Jones** 46:21  
Yeah.  
Yeah.

**Nathan Carver** 46:35  
OK.

**Juan Martinez** 46:38  
Going to the the out hard meter.

**Will Jones** 46:40  
Got it. Yeah.

**Juan Martinez** 46:41  
Yes, yeah, it's think, you know, think about 1990. We're in the 90s again.

**Will Jones** 46:46  
Yeah, yeah. OK. Got it.

**Pavel Frolov** 46:50  
So the the next schema that we want to support, we name it your bullet, your bullet it.

**Will Jones** 46:54  
No.  
E wallet like the letter E.  
OK.

**Nathan Carver** 47:07  
Correct.

**Pavel Frolov** 47:10  
So currently it's implemented in the form of Flex pay kiosk plus Flex port devices Flex port.  
Looks like a player tracking system installed internally on each machine on the bank and connected via Ethernet to our Flexpay kiosk.

**Will Jones** 47:39  
So the E wallet protocol is our own proprietary protocol. Yeah, OK.

**Pavel Frolov** 47:40  
S.  
Yes, yes. Actually the use case for the player started on the Flex POS. He inserted money into kiosk, a press button generate a wallet ticket.  
And he is pin code to protect this piece of paper from using of third parties, so only the person who generates this ticket.

**Nathan Carver** 48:07  
Yes.

**Pavel Frolov** 48:17  
This barcode I can use it on machine because player goes to machine, scans this barcode.

**Will Jones** 48:28  
Mhm.

**Pavel Frolov** 48:30  
On the Flex port, he will need to enter a pin code to validate. Actually this ticket looks like original.

**Will Jones** 48:37  
Mhm.

**Pavel Frolov** 48:46  
Tita ticket but it will not show actual value because it we don't know exactly what's the value currently because it exists only in database.

**Will Jones** 48:48  
Hm.

**Juan Martinez** 48:59  
Right.

**Pavel Frolov** 48:59  
So the value can be credited on on machine and after the player cash outs money from the machine, this data this amount return back to this temporary wallet and.

**Will Jones** 49:00  
OK.

**Pavel Frolov** 49:19  
Be redeemed on the Flex pay device again.

**Will Jones** 49:24  
OK, yeah, so but it's still just a one time, one time use instrument, just like a Tito ticket. It's not something where you're putting money in and out.

**Pavel Frolov** 49:25  
To produce a card.  
It's just a temporary, really temporary wallet. You place money on it, you move it to the machine. Now it's blank or half blank and then he take money on this.

**Will Jones** 49:39  
Mhm.

**Pavel Frolov** 49:49  
So you want it and move it back to the kiosk and produce a card finally.

**Will Jones** 49:54  
OK.

**Nathan Carver** 49:54  
Yeah.

**Will Jones** 49:57  
OK, is the is the third protocol SAS?

**Pavel Frolov** 50:01  
Yes, yes, the the sort schema. You name it Tita or Tita Sass.

**Will Jones** 50:02  
Yeah.

**Juan Martinez** 50:11  
Yeah.

**Pavel Frolov** 50:13  
In this case we can use instead of a flex port device that looks like player tracking system. This touch screen this LCD display on each on each machine but.  
For Cheetah we just need to put Smith board flex Smith board that can communicate to machine via SAS and can communicate to our master.

**Nathan Carver** 50:35  
Yes.  
OK.

**Pavel Frolov** 50:46  
Cheetah server on the location via Ethernet.

**Will Jones** 50:49  
Hmm.  
Is it? So in the the SAS host configuration, there's there's two different, there's there's anyways, there's two different types that you can install with it or two different modes, let's say. One is the controlling one where obviously it's going to have some interaction with the game, can disable it and do things like that.  
Is this a just purely listening only interface board so that it's getting pulses off or are you actually trying to do SAS control mechanisms as well?

**Pavel Frolov** 51:25  
You're saying about what schema?

**Will Jones** 51:29  
So, so when we use SASS, we can make it a it just the owner of the actual terminal, meaning that it has control, it can do different functions or it can be just simply listening. So in other words, there can be a second SASS host that actually controls it and we're just sitting there listening on top of it because I assume we're.

**Pavel Frolov** 51:31  
Mhm.

**Will Jones** 51:49  
Talking about third party games that we're gonna be interacting via SAS, I mean, why would we be doing it with our own games? I guess it's my question. So in this case where we're trying to be compliant with the SAS protocol, is that for control over the actual game or is it for some just?

**Nathan Carver** 52:02  
Mhm.

**Will Jones** 52:06  
Being able to listen and get what I would refer to when one was talking about pulses, be able to get the exceptions in SAS and be able to use them.

**Pavel Frolov** 52:13  
I would say to control not only support money minimal data, but at least we will be able to to synchronize time for example.

**Will Jones** 52:16  
To control.  
So in, you know, facilitate the funds transfers to and from the game, do everything that we need to do in that way. Yep. OK.

**Pavel Frolov** 52:27  
Oh.

**Juan Martinez** 52:28  
Yeah.  
Right.  
Yeah. And then Will just so you're clear, Georgia mandated dual SAS a couple years back, but only the newer machines have that. But primary SAS is reserved to Intralot. That's the state monitoring system. So they're the ones that can disable the game.

**Will Jones** 52:50  
Mm-hmm.

**Nathan Carver** 52:50  
OK.

**Juan Martinez** 52:53  
If there's a pay table malfunction or whatever, we're using the secondary SAS port with slightly limited functionality. Slightly, yeah.

**Will Jones** 53:01  
OK, Yep. OK. So we are second on there. Got it. Is that is that facilitating progressives for any of these games too? Are we doing anything other than just transactions the the two from?

**Pavel Frolov** 53:06  
We do not.  
No, no, just transaction and I think we will be prohibited to use lock and unlock functions on the device.

**Juan Martinez** 53:14  
Yeah.  
Yeah, we have a progressive controller Will for our own games for that, but we don't do anything with anybody else's games like that.

**Will Jones** 53:25  
Yeah, our our systems based functions, our system based award functions permitted such as like a mystery progressive on top of a bank of machines. Is that even a, you know, is that even a a a case that we should consider?

**Juan Martinez** 53:43  
Mm.

**Pavel Frolov** 53:45  
Fairly lightly, no.

**Juan Martinez** 53:47  
Yeah.

**Will Jones** 53:48  
OK, so we can't offer like a free car in kind transfer, things like that, OK.

**Juan Martinez** 53:52  
No, no, no, no, no, no.

**Will Jones** 53:58  
Is that that that means you get a a piece of the piece of the action then too. But I don't. I don't.

**Juan Martinez** 54:02  
Exactly. Which, yeah, which we're not allowed to do. Yeah, I also I posted a really quickly thrown together a block diagram on on to the chat.

**Will Jones** 54:07  
Yeah, so.

**Juan Martinez** 54:17  
Can we formalize that into something prettier? I think to you know that the block diagram was certainly a topic for for this agenda and I that's just I threw that together as a starting point, but there's definitely better, more qualified people than me to do block diagrams. So if you guys can just take a look at that when you can.

**Will Jones** 54:30  
Hmm.

**Juan Martinez** 54:37  
And and see how I I think we all agree that HHR needs to sit. HHR is a standalone entirely separate system from our CMS as as you know it will.

**Nathan Carver** 54:40  
Mm.

**Will Jones** 54:54  
Mhm.

**Juan Martinez** 54:55  
However, we we have some controls today on our own E GMs through the RIS function and I believe that we want to maintain that ability.  
Going forward. So that's why HHREGM management outside of the functions of HHR race tickets, any of that. Pavel, can you just explain Passport to everybody so we understand what Passport does?

**Pavel Frolov** 55:31  
So actually passport feature is just relates to all the machines right now during initial installation I would say.  
When the software installed on the machine, it detects all the hardware.  
Takes this this fingerprint of all the devices, transfers this to the server, validates that no changes from previous time and.  
Practically that's all. So if some devices change it and additional option in the area set monitor passport change.  
If it enabled, then the machine will show the screen that you have a changed hardware. You need to validate your changes. Please scan this QR and to the.  
Activation codes that you get from the server and a server understands that particular machine changes its equipment. So in in general it controls the hardware installed on the machine.

**Will Jones** 56:59  
And not not firmware or software, though it's only the hardware.

**Pavel Frolov** 56:59  
Uh.

**Juan Martinez** 57:03  
Physical change hardware, yeah.

**Pavel Frolov** 57:05  
Actually actually in passport we also place a firmware version. So if the firmware version I change it on IO board or else EG board any any.  
Our boards. Then we also understand that then the fingerprint of some hardware has been changed.

**Juan Martinez** 57:32  
But but not not a bill acceptor and a printer firmware change, correct? Yeah. So Will, this is very useful in scenarios where we're operating, releasing our machines and imagine I gave you a machine with $1000 bill acceptor and then you're going to return it because you didn't want it and you conveniently swap.

**Will Jones** 57:33  
Then.

**Pavel Frolov** 57:35  
Yes.

**Juan Martinez** 57:52  
Drop it out with a $200 bill acceptor. You know we can detect all that and and respond accordingly so that the.

**Will Jones** 58:01  
OK.  
Situation hasn't happened before.

**Juan Martinez** 58:07  
Maybe in in Mexico, Colombia, Peru. Those kinds of things happen all the time, I'm sure.

**Will Jones** 58:16  
Yeah.

**Juan Martinez** 58:18  
Guys line.

**Will Jones** 58:18  
I wanna, I want, I wanna get $1000 like a a bill that's $1000. I'll be pretty happy with that.

**Juan Martinez** 58:25  
Exactly, exactly. I just want to share my screen. So because we're we're just over the time right now. So Pavel, does the legacy CMS system need to survive to support older machines?  
Meaning, let's, you know, we have games in Colombia that today they're connected to the system. Does this mean that that system and those legacy products will not be compatible with the new CMS? So both systems have to be in parallel?  
Or OK, so then it OK.

**Pavel Frolov** 59:02  
Yes, yes, but for some time we will need to to have two systems in parallel because first of all we are not able to to do this very fast to to produce all.

**Nathan Carver** 59:10  
Mhm.

**Juan Martinez** 59:16  
Of course.

**Pavel Frolov** 59:18  
All the features that why probably this is a a good time to switch to new architecture and new CMS starting from payment devices. Of course we will need.

**Will Jones** 59:19  
Number, yeah.

**Pavel Frolov** 59:35  
To get probably some data related to machines and so on from our current CMS. So I see this starting from next year, some data will be moved from current CMS.  
And transfer it in some way to to newer CMS and add in new features, add in for example new areas that we discussed previously with new graphic user interface.

**Nathan Carver** 59:56  
Yes.  
Yes.

**Juan Martinez** 1:00:08  
Mhm.

**Pavel Frolov** 1:00:10  
To control machines with new features.

**Juan Martinez** 1:00:15  
OK. And so that that that's my third question or I I believe I heard on our last call that legacy CMS is on a SQL database. So it is is the goal with the new CMS to in theory just point it to this old SQL database or?  
Is that database so old and full of machines that don't apply and all that that we don't want to use it? I just want to visualize what you think we are going to do, or are we going to start importing only what we want from the old SQL database?

**Pavel Frolov** 1:00:53  
Yeah, I think it's better to export only export and import data only when we need them, actually need them because current database full of many unnecessary data, already unnecessary.  
Supports in some machines that's already not actual.

**Will Jones** 1:01:11  
Yeah.

**Juan Martinez** 1:01:12  
OK.

**Will Jones** 1:01:15  
Yes.  
So is, yeah, there's actually, sorry.

**Nathan Carver** 1:01:18  
Yeah, I think the pattern the would be to just create an adapter between the two systems and slowly move the source of truth to the cloud. So yeah, so whatever CMS.

**Pavel Frolov** 1:01:31  
Yeah, yeah. Oh.

**Nathan Carver** 1:01:34  
One, whatever CMS maintains source of truth off, we would push data to it. Otherwise, yeah, it's gonna be like what Pavel is saying. It's a very slow migration and ideally all the new stuff goes in the cloud. So even the data persistence mechanisms would be in the cloud.

**Juan Martinez** 1:01:38  
Right. Sure.  
Sure.

**Will Jones** 1:01:53  
Definitely, definitely throw out there that we'd want to choose the right data storage mechanism for what we're doing and a relational database and SQL may not be for these transactional things. It doesn't seem to me logical at all. You know, so we can we can find.

**Juan Martinez** 1:01:53  
OK.

**Pavel Frolov** 1:01:54  
Yeah.

**Will Jones** 1:02:11  
The right place to store it and it doesn't have to be the same for all. We can have many different data stores for the different purposes and the different services. But I was going to ask a question on on this envisioned evolution is there so from the I I know maybe for Nathan's ears too if he doesn't know this already.

**Juan Martinez** 1:02:17  
Sure.

**Will Jones** 1:02:31  
The SAS is a is a serial protocol, so there's going to have to be a physical device on the machine to be able to convert that and then send something that's like an Ethernet message to the system. So is the, you know, the Mother Goose, is that a serial protocol as well? Because of how it was dealing with the pulses, there must be some SMIB.  
Ish device on the machine that then is sending information to whatever the mother Mother Goose and in a in an Ethernet packet.

**Juan Martinez** 1:02:53  
Yes.  
Yeah, wait, wait for it. Will. It's called the no, no, it's called the fledgling.

**Will Jones** 1:03:02  
The double mother.  
The fledgling. There you go. I like it. We would, yeah, we have to probably have to work on how you say mother too. It's it's definitely there's you need that kind of. I don't know. There's a colloquialism there. Yeah, you need soul. Sorry, man. You need that. So anyway, then E wallet.

**Juan Martinez** 1:03:09  
Yeah, so.  
Need a little more soul?

**Will Jones** 1:03:27  
That's our proprietary protocol. So is that just going off the processor of the the terminal and sending a message directly to some server so there's no serial component to it?

**Pavel Frolov** 1:03:41  
Currently we communicate from Flex pay to Flexport using secure web socket over the Internet.

**Will Jones** 1:03:53  
Yeah.  
OK, so and then, but there isn't, there's no physical other component than our processor board on the the gaming terminal to communicate, right? There's no other third device or second device.

**Pavel Frolov** 1:04:11  
Flexport installed the same as SMIP port internally on machine in in case of current implementation when no SAS we still use pulses to get.

**Will Jones** 1:04:18  
OK.

**Pavel Frolov** 1:04:30  
To show message from the machine.

**Will Jones** 1:04:31  
OK.  
Yeah, and then we push.

**Pavel Frolov** 1:04:35  
And mimic mimic as a bill acceptor to transfer money from a ticket to a machine.

**Will Jones** 1:04:43  
Yeah. OK. And then of course SAS is a serial protocol that's it's again using a second processor on the on the machine that's translating that protocol into something else, correct. And that probably Ethernet, do we have like 1 protocol for all our devices in terms of communicating from?

**Pavel Frolov** 1:04:56  
Yeah.

**Will Jones** 1:05:02  
The actual terminal to our server.  
Or these different rotocols as well.

**Pavel Frolov** 1:05:10  
It's a a different protocol.

**Will Jones** 1:05:15  
No.

**Pavel Frolov** 1:05:15  
So we can say that Flex pay communicates to our server, same using security web socket, but this is a different protocol than internal protocol for location.

**Will Jones** 1:05:29  
So.  
So in this this evolution, are we throwing on the table we can change these protocols? Are we saying these protocols have to can stay consistent? We can't.

**Pavel Frolov** 1:05:47  
It's a open question. Actually yes, yesterday we have discussed one different approach not to support SAS.  
A host uh application.  
On Flex pay or Flexport and Flex snip, but probably just to make conversion from a serial protocol to to network on the snip board.  
And then uh.  
Flex pay or Flex tower should work as actual SAS host, getting data about SAS in form of reserve net, but not in form of serial.

**Nathan Carver** 1:06:29  
Yeah.

**Will Jones** 1:06:45  
I didn't quite, I didn't follow that one, but I'm not going to dive down the hole yet in that way. So so then if we have different protocols, we have different endpoints on the the server that can be able to receive these protocols.

**Nathan Carver** 1:06:53  
Yes.

**Will Jones** 1:07:01  
And then we're talking about behind that facade changing the system to be this new manifestation that's hosted in the cloud. Is that, is that the picture?

**Pavel Frolov** 1:07:14  
Ideally if we just implement.  
A protocol that we will never change in the future or just add in new endpoints do not touch an existing.

**Will Jones** 1:07:37  
Yeah. So OK, leave the existing, only add new endpoints or new capabilities features through the different mechanisms. So we've there's a integration event bus we're talking about for event bus to be able to send the new protocol information to some other.

**Pavel Frolov** 1:07:45  
Yes.

**Will Jones** 1:07:57  
Or end point that is in the cloud.  
Kind of. No, maybe. OK.

**Pavel Frolov** 1:08:03  
Yes, yes, yes, yes, maybe.

**Will Jones** 1:08:06  
Right. OK. Just getting a bigger picture of what the ask is. So I'm I I I agree that. I mean you can't wipe out an ecosystem and rewrite an ecosystem without creating a huge unknown, right? Something that's that's on in that should be unacceptable to any business.  
Right. We got to pick a a more transitional way of doing it and starting with what's new and then potentially eliminating what can't be modified to support what we need, but always having the vision of how that ecosystem can work better so that they they interrupt.  
Did you use the? You know you don't have to reinvent the wheel each time. They use their their services wisely.  
Have you chosen a cloud provider?

**Pavel Frolov** 1:09:00  
Um, no.

**Juan Martinez** 1:09:01  
No.

**Will Jones** 1:09:03  
OK.  
Is there any any preference? Is there a cloud provider right now that that that JBL is using?

**Pavel Frolov** 1:09:12  
Hmm.  
Actually, I think we can just ask our admins because they use something for different projects.  
Very likely they will advise something.

**Will Jones** 1:09:35  
So yeah, there's there's so many more bigger questions to sort of talk about that are that I I realize what I have to understand the problem first to to to provide any kind of guidance on where to land. But you know we have the capability of creating something that's really proprietary that's.

**Juan Martinez** 1:09:35  
Alright guys, we uh, go ahead Will.

**Nathan Carver** 1:09:36  
So.

**Will Jones** 1:09:54  
Our own services and running on something that's more like a hosted server and then call it a day. Then obviously we can move it more easily off of the cloud and onto Prem if we need to, but then we lose all kinds of capabilities and probably.  
Some cost savings, probably not necessarily if we actually ran it in a serverless environment and then we get the scalability and the default tolerance and a lot more security right away too, and most likely when.  
These this company's talking about AB2B solution. The who is the one who does the gift cards again? What's their name?

**Juan Martinez** 1:10:33  
Uh, in calm.

**Will Jones** 1:10:34  
Incom, yeah. So when we talk about a B2B solution for Incom, they're probably picturing something that's, you know, either an AWS ecosystem or or another where they can have a very secure tunnel between the two. So VPC or something to connect our service to theirs.  
And anyway, I think we'll we'll want to really know what their expectations are too when we choose our provider and how we how we think about laying out the future. So but.  
Yeah, very intriguing, you know, but I think it's going to, you know, from what Pavel's words were before that, you know, we can't, we can't assume that we can, that we can jettison the legacy. I'm using my words there, but you know we can't with the the legacy is is going to have to come along with us for baggage.

**Juan Martinez** 1:11:21  
Right.

**Will Jones** 1:11:26  
For a while.

**Juan Martinez** 1:11:28  
Yeah.

**Will Jones** 1:11:28  
And and the ability to have all these functions, right? Legacy does great functions with known defects. The future is unknown all the defects and you know we got to negotiate that.

**Juan Martinez** 1:11:35  
Definitely.  
Yeah.  
Yeah, definitely. Well, guys, I got to start prepping for for my conference here for for Friday and and Nathan, I think that we, you know the the MVP number one is is Flex pay POS.  
And it's necessary integration into CMS. So I I think we we do need to define it as we'll put it exactly and we should over define it and then we can refine it maybe on Friday. But what exactly if we put on our master operator hats would we?  
Want to see in a portal for managing these devices, Flex pay, Flex tower, card dispensers, ports, administration of multiple locations and all of that. I think that that would be.  
Good for our Friday meeting is just to understand that you know Flex and CMS are the most important things on our timeline and and what are the actual needs for the customer from that portal.  
That sound good to everybody?

**Pavel Frolov** 1:12:50  
Yeah, perfect.

**Juan Martinez** 1:12:52  
OK.

**Nathan Carver** 1:12:53  
OK, so you want to review that Friday morning?

**Juan Martinez** 1:12:54  
OK.  
Yeah, yeah.

**Pavel Frolov** 1:12:56  
Yeah. Thank you. Bye.

**Nathan Carver** 1:12:57  
OK.

**Juan Martinez** 1:12:58  
Alright, thanks everybody. Bye, bye. Thanks, bye.

**Will Jones** 1:13:00  
Yeah, thanks.

**Nathan Carver** 1:13:00  
Alright, thanks all.

**Juan Martinez** stopped transcription