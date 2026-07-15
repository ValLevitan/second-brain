---
tags:
  - payment-options
  - meeting-recording
  - business-strategies
  - juan
  - val
  - technical
---

# JVL Payment Options-20250403_104210-Meeting Recording

**Date:** April 3, 2025, 5:42PM  
**Duration:** 36m 28s

*Allen Lee started transcription*

**John Houseal (0:04):** OK.

**Juan Martinez (0:04):** It and it'll save it to your teams network and you'll have to send us the summary later when you can.

**John Houseal (0:10):** OK.

**Allen Lee (0:10):** Yeah, we can. We can do that.

**Juan Martinez (0:13):** Great.

**John Houseal (0:13):** Yeah.

**Val Levitan (0:13):** So John, so John, if you could, if you could start from addressing discussing the problem we're trying to solve 1st and maybe then going to use case and then maybe into solution.

**John Houseal (0:13):** So the so the. Eat. Yeah. So. So Juan's original question was, have we heard any feedback from the the industry that merch, that adoption of kiosks is slowed because merchants fear she asked reduces in-store spend of coamings, is that right? Is that a fair summary one?

**Juan Martinez (0:49):** Yeah, that, that's fair.

**John Houseal (0:51):** Yeah. And so, um, my response. Val was that we have not heard that. But what we have heard, yeah, can repeatedly from multiple operators in the industry is that they are that merchants are concerned that when a player redeems to a gift card that the gift card cannot be subsequent subsequently used to play at the Coam game machines. So in a simple use case, I went $100 at the convenience store I had it loaded onto the MasterCard, and then I walk out the door and that $100 has no way to make it its way back to the Coam gaming machine, whether it's through the game machine, through a kiosk, however, um.

**Val Levitan (1:41):** OK, so so the problem we're trying to resolve is how to make the payout money. Fine. That's way back into the machine.

**John Houseal (1:51):** You got it.

**Val Levitan (1:53):** Understood. And what's the solution?

**John Houseal (1:56):** So there's at least three Solutions. Technically, I'll start with one we haven't talked about previously. Juan, technically the player could walk up to the clerk at the store and say please swipe my card for $100 and give me $100. There's there's nothing to stop that from happening today and then they take that $100 and they walk over to the kiosk or to the game machine and they insert the money and they play as they normally would back.

**Juan Martinez (2:12):** OK.

**John Houseal (2:23):** That is likely done today, although you know we're not able to see that, but that's the easiest way with no changes today to the system, you could do it the second easiest way that you could do it. Um is to contract with a merchant acquirer, so that is someone who acquires MasterCard and Pulse transactions. Um, so in this case the location would have to sign up with a merchant acquirer and example of them. I think one of the folks in market is using Passport Inc. If you're familiar with them, they demo it G2 E um. But in that case you contract with a merchant acquirer. You install a card reader on your kiosk or on your game machines, or on both. That's up to you. And then when a user swipes their card, the machine will prompt them to enter their pin, and then the machine will send a transaction across the network to process. You know however much money you wanna add back off of the payout instrument into the Gaming environment, so off of the card and into the machines you can do that today. The challenge with that, or the reason I don't believe we've seen wide adoption in the redemption terminal kiosks. Um is because there's a cost associated with it, so each merchant would have to pay a monthly maintenance fee. If somewhere between 50 and $200.00 it varies by who you work with. On top of that, every transaction that, that, that they conducted with their merchant acquirer, the merchant acquirer will charge the location 3%. So if a player inserts, you know, tries to take $100 off of their coam gift card and add it to the machine, the location as opposed to getting credit for $100, will actually only get $97. And so the downside of going that route today is that. The merchant has the cost of 50 to $200.00 ongoing, and they're potentially a getting less money. So today, when $100 bill is inserted, they get $100 like give $100 credit on these debit cards. Uh, they would have to give $100 credit, but they're only gonna get $97.00 back from the network the way you could potentially address that in your UX is to just say to the player. Even though I'm taking $100 off of your card, I'm giving you $97.00 on this Tito ticket or on this machine, and that's reflective of, you know, a $3 surcharge to use a debit card, something like that. You.

**Juan Martinez (5:37):** And in that scenario, the scanning of the card does not require a PIN number.

**John Houseal (5:43):** No, you still need the pen, but those all of those what I've just described broadly in option two is using the mag stripe on the card. So you're using the payment credentials on the card. You'd also you know that barked the card reading device has to be PCI compliant, as does the communication between you and the acquirer. Um, but you do not scan a barcode. You swipe the card and you read the magnetic strip. Because most of the kiosks and none of the game machines have card readers, and card readers are not cheap or easy to deploy at scale, and most of these locations have never contemplated PCI compliance, and most of these locations don't want to pay an additional 50 to $200.00 per month in service fees. Nor do they want to pay the 3% in interchange. We went to MasterCard and asked them to allow us to run the transactions off network or what's referred to as on us, which means in this scenario option three, you don't use the mag stripe on the card. Use the barcode printed on the back of the card and you'd have to have an optical scanner on the machine or the kiosk and you scan that barcode and then instead of sending it through a merchant acquirer to MasterCard, you would just send it directly to income and then we would process the the removal of the funds off the card and respond back to you, giving you an authorization to proceed with giving the player credit. In that model, there's no interchange. There's No 3% tacked on, so we solve that problem, and there's only a modest monthly fee. We're still working on it, but it'll be probably something like 20 or 25 bucks and that's really for us to handle the accounting that's required to settle with the store because what we have to do now in addition to settling with the store for the loads of gift cards, we have to pay the store because what happens when the money is taken off the card, that $100 that store owner has not received a cash like they would have if the cash was handed over.

**Juan Martinez (7:55):** It is.

**John Houseal (8:14):** So we Incomm like we processed a gift card activations, now have to process the gift card redemptions or the spend and then route that money back to the 7000 merchants in Cohen.

**Val Levitan (8:22):** Hmm.

**John Houseal (8:28):** And so that's.

**Juan Martinez (8:28):** I guess, John real quick, I'm I must be missing a step. When I scan this card in the optical scanner and the monies are deducted, where do they go that this location owner doesn't have access to them? Didn't they go onto a Tito ticket? Or perhaps even directly onto a machine.

**John Houseal (8:46):** You know, keep in mind the funds are on the gift card.

**Juan Martinez (8:50):** Yes.

**John Houseal (8:51):** The funds are on a gift card that has an account at Sutton Bank.

**Val Levitan (8:56):** Yeah.

**John Houseal (8:58):** That income manages that holds the funds the transaction has occurred again, the funds are at Incomm the transaction has occurred and the merchant has given the player $100 in credit to play, but no physical currency or electronic remittance has occurred at that point. The merchant is extending credit to the Blair on the belief that income will then later pay the merchant for extending that credit because we hold the balance for that gift card.

**Val Levitan (9:22):** You.

**John Houseal (9:32):** So let's walk through 2 examples to illustrate what that means in practice. If, if if I swipe the car, if I scan the card and I authorize the transaction for $100, income says great.

**Val Levitan (9:38):** You.

**John Houseal (9:47):** You're good for $100. They give the player $100 credit a day later. Income wires them $100 to their bank account to make them whole. The merchant.

**Juan Martinez (10:02):** Like at the merchant has to do this. This cannot be an automated thing at a kiosk or machine.

**John Houseal (10:08):** Well, I'm referring to the merchant in the sense of the location, how it happens could be the kiosk could be the game machine or conceptually could be the clerk.

**Juan Martinez (10:21):** OK, understand.

**John Houseal (10:23):** Like you have to separate how it happens from what's happening, and then how it happens is really up to you, right?

**Val Levitan (10:28):** Yeah.

**John Houseal (10:31):** So you could install. You could create a JVL redemption kiosk that has a scanner in corporated that it works seamlessly with JVL gaming machines and others Gaming machines, and you can operate and you know. And it's a Tito system and it operates there, right? So that's one configuration. Another configuration might be that you sell your JVL redemption kiosk. To somebody that uses the access card system or something like that or, you know, Ultras tighten system um. So in that case you have a different sequence of events that will take place.

**Juan Martinez (11:15):** Understood.

**John Houseal (11:17):** And then and then you think about it, thinking about it in terms of money, let's say that the, the store, you know, try to run a transaction at the machine by scanning the bar code for $200.00. But the balance on the bar code was only $100. If we responded back to your system and said that transactions only good for $100. And I'm not saying you would do this. I'm just using it as an example, but you went ahead and gave them $200.00. The merchant effectively just gave them a free $100 in credit, cause the only thing Incomm that's gonna do is transmit the available balance that's on the card. That $100.

**Juan Martinez (12:02):** So during that initial optical scan, there is no balance check. That the guest, a guest facing balance check.

**John Houseal (12:14):** I think you're looking at it slightly different. You can configure a balance check. A balance check is a different transaction type. If you wanted to orchestrate a balance check, you could do that, but the purchase transaction is a different transaction. So what you're I think what you're conflating a little bit while on is these are all individual transactions that can be wrapped into a customer experience. SO1 customer experience might be I'm standing at a game machine.

**Juan Martinez (12:42):** Right.

**John Houseal (12:46):** I wanna play $100. I know I have $100 on my card scan my card for $100 process processes through income, $100 is on my machine. I might be a player that doesn't know what the balance of the card I'm holding is, and so I might say I wanna check the balance on the card and so I checked the balance on the card and it says 97. So then you know I enter a 90 and play with 90 bucks or it may be the case that you kind of combined those two scenarios and you say well, I always wanna check the balance before I attempt a transaction in the eye. In that case, is the JVL technology, in which case a player enters 100 bucks and then they swipe their card and then you conduct a balance check transaction within COM. That balance comes back above 100 and you say, OK, I'm good to go with 100 and then you submit a purchase transaction for 100. So these are all the street transactions and then you just have to decide, you know based on the user experience how you wanna orchestrate them. So produce ultimately the the product you guys are bringing to market?

**Juan Martinez (13:59):** Understood. And the I certainly have worked with a PCI compliance. So even though there's technically no spec on the design and functionality of the kiosk at the highest level from just, we do need PCI compliance because we're interacting with the MasterCard network.

**John Houseal (14:22):** No. So in the so in PCI rarely relates to the payment card data. Um, so in not the network. So compare and contrast. So if you an option two, you're putting a card reader, a magnetic stripe card reader on your kiosk. The magnetic stripe is reading the card reader is reading the magnetic stripe and it's extracting the 16 digit card number, the expiration date and the the card verification values. TV and it, and it communicates back to MasterCard with those. So that's what PCI covers when you're communicating with somebody using actual the actual card data you have to encrypt it and be in compliance with PCI. If we move to option 3, which is why we're building option three, you're using a bar code that is not the payment card information. That barcode only means something to income. It means nothing to MasterCard. It means nothing to you. It means nothing to anyone except for income. So when you communicate purchase transactions using our barcode on the back of the card, you're outside of PCI scope because it's not actually payment information and we only make it payment information once it gets inside our walls.

**Juan Martinez (15:45):** Understood.

**John Houseal (15:49):** So we insulate the entire industry from having even to contemplate it that way. So that's why we're doing this is because it just you don't have to worry about being PCI compliant in that scenario.

**Juan Martinez (16:02):** Sure, sure.

**John Houseal (16:03):** Does that make sense?

**Juan Martinez (16:04):** Absolutely not.

**John Houseal (16:07):** Val, is that track or you or is that good?

**Juan Martinez (16:07):** And.

**Val Levitan (16:11):** Uh, yeah, I have additional questions, if I may.

**John Houseal (16:14):** Sure.

**Val Levitan (16:16):** So starting from, I guess a simple question, somebody picked up a card lane on a floor and brought it to to a machine that has an optical sensor. Presents the barcode to an optical sensor. Is it all that is required just to show a bar code to get the information on the value?

**John Houseal (16:44):** Well, today to, you know, ultimately, yes, Alan, where I talked with Jared about the IB balance check thing, but we haven't implemented that yet, correct.

**Val Levitan (16:45):** Or or or is the.

**Allen Lee (17:02):** Com I I think the they're looking at security now if you you know add yeah.

**John Houseal (17:07):** Yeah, we, we he he's fine with it if we just do it. If we do pin based, I got Jared to agree that PIN based.

**Allen Lee (17:11):** Exactly. Yeah, right.

**John Houseal (17:13):** OK, so the the the answer is we cannot do it today.

**Juan Martinez (17:14):** But.

**John Houseal (17:20):** By the time you would deploy this, we will be able to do it, but it will require the user entering a pin. The reason for that is because. The card will be exposed. You know the bar code on the back of the card will be exposed, so roommates can take photos of it and do other things with it. And so we want a light protection mechanism to protect the recipients of these cards from bad actors stealing their funds. So the sequence in that event would be. They scanned the back of the barcode. They enter their pen and then you would get a balance. The pin on these cards is set on 1st use. What does that mean? It means the very first time they use a PIN based transaction whatever 4 numbers they enter become their pen. So if they're standing there, and that balance check is the first transaction they've ever done, whatever 4 numbers they enter will become their pin. Um it?

**Juan Martinez (18:26):** And that's their pin only for that bar code, correct?

**John Houseal (18:30):** Correct.

**Juan Martinez (18:31):** OK.

**John Houseal (18:31):** And they can change the pen anytime they want by calling the IVR or going to the website. But the pin, as opposed to being said in an advance, is set on the very first time they use it.

**Juan Martinez (18:44):** OK.

**Val Levitan (18:46):** So that what it means is that if I would like to deposit $100 on this card, I use my PIN 1234, that pin becomes married to this particular card forever unless I go on your website and change it. Is that correct?

**Allen Lee (19:09):** John your mute.

**Val Levitan (19:13):** John, you're on mute.

**John Houseal (19:14):** Yeah, that's that's correct. Yes, sorry, I don't know how I got on mute. That's weird.

**Val Levitan (19:19):** OK. So. Uh. So the card now becomes a rechargeable card, so I can now put additional winnings on the card.

**John Houseal (19:39):** No, that's not what we're saying.

**Val Levitan (19:45):** No. So let's go through user case now. I. Got the card? I put $100 on it. I assigned the pen I play on the machine. I win another $200.00, so the $200.00 goes on the card. Now I have $200.00 on the on the card. Now I go and play on the other machine and I win additional $100.00, so I'll becomes $300.00 card. Now I go back to to a kiosk and I put additional $100 on the same card. So now it's $400.00 card. Is that correct?

**John Houseal (20:32):** No, you're not reloading the cards, you just get a new card every time you cash out right now.

**Val Levitan (20:41):** So I have $100 initial $100 on the card, which is a sign that PIN number 1234, I come up to the machine and I deposit the entire $100 from this card on the machine. Now I have a winning do I need a new card?

**John Houseal (21:05):** Correct. Yeah, that's the. Those are the rules in two until 2026.

**Val Levitan (21:14):** This web what?

**Juan Martinez (21:18):** Broke up there though.

**John Houseal (21:18):** Pardon me.

**Val Levitan (21:20):** Sorry. Sorry, I apologize.

**John Houseal (21:28):** Yeah, you'll have to repeat that. Well, I didn't hear it.

**Val Levitan (21:32):** What happens past 2026? There's becomes a rechargeable card.

**John Houseal (21:38):** A potentially but rechargeable Val introduces a whole bunch of challenges that you have to do actual KYC. Uh. On the on the player, which I don't think anybody wants to do.

**Val Levitan (21:54):** OK, so let's assume it's not rechargeable. It's one time use card so again I obtain a card. I put $100 on it. I put $100 on the machine from the card, so the card is essentially 0 now and now I have a weaning on this machine of $200.00. Why I need to? Uptain a new card and put a new and I put $200.00 on this new card.

**John Houseal (22:28):** Yeah, you always get a new card.

**Val Levitan (22:28):** The yes.

**John Houseal (22:32):** When you cash out, that's sweet, aka.

**Val Levitan (22:34):** And so these cards are just these cards are just laying around.

**Juan Martinez (22:39):** Yeah. Well, they're currently like at krogers or the Ultra Max locations.

**John Houseal (22:42):** Well, they're not just laying around. I mean like it, it all comes back to how you want to design your solution guys. So in a kiosk the cards are in the kiosk. Right.

**Juan Martinez (22:55):** Correct.

**John Houseal (22:55):** That's the whole point of the kiosk is to distribute the cards.

**Val Levitan (23:00):** Well, I questioned the point of the kiosk. I I don't know what the point of kiosk is. Yeah, I mean, I mean, you could go back and window where the cashier is and say, can I have the car?

**John Houseal (23:16):** Yeah, but most people, I will tell you, Val, most people in general are trying to limit the interactions with the clerk and keep the Gaming environment self sufficient.

**Val Levitan (23:31):** No. OK, fine. So the this is kind of 7575% resolved if I have any other questions I will ask, but let me let me switch to another subject.

**John Houseal (23:41):** OK.

**Val Levitan (23:42):** So the role of the participants. Let me name the participants. So it's the location where the machines are at. It's the master. That's the guy who brings the machines into the locations and it's JVL supplier of machines or kiosk and it's income saw four participants. What is the role of? In calm and all of this. In in the case where you can add additional or you, you can. You can use the same card for our Gaming production.

**John Houseal (24:33):** They say that again, Val, I'm not sure I followed.

**Val Levitan (24:37):** There are 4 participants in this business scheme. A location. This is a place that houses the machines. It's the monster that's the owner of the machines. JVL is supplier of machines or kiosks and Incomm, a clearing house.

**John Houseal (25:01):** M.

**Val Levitan (25:01):** So what is the role of? In calm in all of this.

**John Houseal (25:10):** We are the program manager for the gift card product and where the technology provider for the API's. Uh that allow the other parties to put together kind of their desired solutions?

**Val Levitan (25:29):** So is JVL still needed as a kiosk provider in all of this, or Will income design A complete solution kiosk? Less solution for the location.

**John Houseal (25:50):** So income does not do kiosks we we we do not, we don't build equipment.

**Val Levitan (25:53):** Well, no, no.

**John Houseal (25:56):** We don't that, I mean that will that will not happen. So you can be, uh, what? You know our our focus is is really. The financial technology, the products themselves and the money movement. Between parties because all of this money movement is regulated in the US. So that's that's the core of what we do the operators. They come up whatever. In my experience with kind of what I'll call the the concept of operations for how they want the stores and their route to be set up. So you have folks like Excel, for example, that own Bulldog Entertainment and Georgia, they fully believe that everyone of their locations needs to be 100% self sufficient and that to accomplish that, they're putting a kiosk and every single location. And that kiosk is is using Tito to communicate with the game machines and to manage the money moving in and out of the game machines. And it's using the kiosk to manage, um, the redemption to a gift card. So you accumulate winnings. You can have the kiosk spit out and activated gift card, or if you don't want to cash out and you just wanna stop playing, they provide a digital wallet where you can then store your winnings. You can think of it as a digital Tito repository where they record your open balances and then the next time you come to one of their kiosks, you sync with the kiosk via process. They design and then you transfer funds out of your digital wallet to the kiosk and then the kiosk gives you a Tito ticket to continue play. So that was their design, other folks, because I heard Juan mention in a Max Ultra at Kroger, they didn't wanna have to pay $15,000 for a kiosk cause they weren't sure they were gonna get values. So what they did was they said we're not gonna have a kiosk, which means they can't use coam kiosk cards. They have to use the package kiosk cards, so they elected to hang the cards as I think Juan pointed out, and then they installed optical readers on their gaming machines and and using the little screen similar to the access screen for the Titan system, they have the player activate the gift cards at each machine, so there's no kiosk involved and those are being activated at each machine.

**Juan Martinez (28:13):** Yeah.

**John Houseal (28:38):** Now the problem. They ran into problems with that, for reasons I won't go into, but they're now looking at a kiosk solution, but my my my point in describing that and then and then there are other folks like United that are just deploying handheld devices to the associates because they don't believe they, you know they have 1300 locations. They don't wanna spend 10 or 15 grand a pop. Her location across our network. So they're looking at, you know, how do we, you know, use readers similar to what Intermax did at Kroger.

**Val Levitan (29:14):** What?

**John Houseal (29:18):** And so there they haven't arrived at a final design. But what I you know what I'm trying to communicate here is that the operators really come up with what they think is the best mode of operation for their stores and and and and for closing new stores.

**Val Levitan (29:33):** The.

**John Houseal (29:36):** And you know that's that's their business. They come to us and they say this is what we think would be best, you know? So like in the case of Kroger, they said we gotta hang these up. And we said we're really worried about that for this reason. And they said, well, we wanna try it. We said, OK, they tried it. They said you're, you know, we don't wanna do this anymore. We said that's great. And then you know, somebody like Excel came to us and said, well, we wanna do it this way because this is how we want our stores to run. And so we, you know, we help them with that in terms of this is how we can achieve that. So you know, as we think about JVL, you know the way we would typically support you is is that you would either working with one of your you know largest installed customers or similar. So you figure out what we think is the most common. Approach to the redemption terminal for the you know to support both the sale of JBOD kiosk but also the sale of JVL game machines. Um, you know what? That solution looks like and so um, I don't. I don't feel that I'm qualified to know your business for your customers well enough to necessarily weigh in on that, but I'm definitely ready and willing and super excited to help you navigate kind of that conversation. So we can get you exactly what you need.

**Val Levitan (30:58):** OK, OK. It's all clear for now. I don't have any more questions.

**Juan Martinez (31:05):** On I I'm good as well.

**John Houseal (31:05):** OK. OK. Yeah. Well, and so just. Yeah, just let me know as you guys think about it. I mean again we we're also open to development or if if you have an idea that you know, no one thought of, I mean we wanna make you as successful as you you know as JVL can be um you know not just in Georgia but beyond. You know, we're also looking to expand into some other markets which we can talk about, but you know we're we're here to help. I. So just let us know how we can.

**Juan Martinez (31:37):** You know, we'll do thank you guys. I appreciate it. And and as soon as that teams AI summary is available on your side of this call. Please, please send us that summary you can.

**Val Levitan (31:49):** It's a well, it will show up automatically, I think.

**John Houseal (31:49):** Yeah, sure thing.

**Juan Martinez (31:53):** Yeah.

**Val Levitan (31:53):** Um, John, what are the markets? Are you were spending to?

**John Houseal (31:58):** Well, we're looking at Texas given the founding Fannin County rule ruling now. We're looking at trying to reopen Florida to make it a little less Gray. We're looking. We already support Pennsylvania, but we're looking at we've we've just kind of casually supported it as the way I would describe it. But we have a product that we use in Pennsylvania that actually is a card, but the card can immediately be used at an ATM. Um. And so it's just a lot better product. It's basically handing a player cache without having to have the cash on hand, so we're looking at using that further in Pennsylvania, but also in Nebraska, uh, and potentially Iowa, Nebraska specifically because and you guys know this better than me, but it it appears to me that most of the winnings are distributed either between kind of 500 or less or 2000 or more. There don't appear to be a lot of middle winning ones, so when somebody hits a jackpot in Nebraska and wins 5 grand, the store doesn't have the money. And so it creates a very negative customer experience where the operator has to drive a check out there. And sometimes it's a day or two later, and so we're looking at using some of these products for the larger wins to to be able to support those gaps. And then in merchandise markets, we have a print on receipt product. So basically in merchandise markets, if you wanted to award somebody with a gift card, we could make it to where your redemption terminal just prints out a receipt with a card number on it, and then they go to a website and they can pick from like 500 different a gift card providers. You know everything from Applebee's to Starbucks to Home Depot to whatever. And then. You know, have those gifts certificates delivered digitally to them. A lot of it. We're looking at damage just in full transparency and under our NDA is you know how we structure these to navigate. Some of the grey markets so that we can deliver some of the same benefits in the Georgia market, you know, so reduce dependence on cash, better player experience, ensuring the the, the, the winnings go back into some form that benefits the community via sales tax, stuff like that. And so, you know, I'd say we're really trying to look more in the Gray markets, um or the OR the Gray markets that are starting to look a little more black than red, if you will.

**Juan Martinez (34:45):** Sure.

**Val Levitan (34:45):** We're, we're in Texas. Did you say I didn't catch the name?

**John Houseal (34:49):** It's Fannin, Fannin County. It's a pace Omatic sued the Sheriff's Office to get their machines back, and a judge issued a ruling that pays thematics. Machines were skilled machines, not gambling machines, which is the first time a court in the state of Texas has ever issued an opinion on these devices. And so it's opening up a lot of.

**Juan Martinez (35:18):** Yeah, they they got that same ruling in Pennsylvania from the Sheriff's Department there.

**John Houseal (35:18):** I think there are a lot of joy. Yeah. So in Texas, I think it's generating a little more interest, one because of the
