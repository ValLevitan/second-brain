# Raw Transcript — NCR Atleos / ReadyCode — cardless ATM payout for JVL's Georgia amusement business
**Date:** September 22, 2026, 1:01 PM – 2:17 PM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026]]
---
00:00:16 Speaker 1
Hello, Bob. Carlos
00:00:17 Speaker 2
How are you doing? I'm doing well. Thank you for asking.
00:00:22 Speaker 3
What about you? I'm doing good, man. It's been a — you know — if you were to tell me, we're already this deep into September. I know. I just feel like the whole year just went like that.
00:00:32 Speaker 2
That's exactly my sentiment.
00:00:34 Speaker 3
I know what you're saying. It's been a blur. It's been a blur over here. I guess that's a good thing. We're not looking at the clock.
00:00:44 Speaker 2
I guess. Life flows. Nobody's asking for our opinion.
00:00:50 Speaker 3
Exactly. Well, well, good to connect. I'm uh, I'm here to chat with you about, you know, maybe what we can do with ReadyCode and learn a little bit more about your business. I'm gonna drop our agenda of the chat just to keep us, I guess, aligned with kind of some of the points we want to cover on today's call. I'm the commercial rep for ReadyCode, and I run our fintech portfolio. Portfolio for our fintech all point surcharge free customers, and so I've been with the organization a little bit over four years, and I'm looking forward to getting into this discussion. I'll pivot over to Sean so he can tell you what he does for us.
00:01:31 Speaker 4
I'm the product manager for this product called Waypoint, the partner solution that allows a customer to go into a machine, get cash, cash out. I think Carlos will have a presentation, then we can go from there.
00:01:48 Speaker 3
Sounds good, thank you, John. How about you, Val? Can you share with me what you do for JVL, or maybe share a little bit about the business, and let's dive into the use case and discuss that.
00:02:01 Speaker 2
Our family is a controlling shareholder of JVL. JVL is a forty-three-year-old, second-generation, privately-owned company that is an amusement games, business, and transactional equipment company. My family also owned and sold a company called CashCode, and CashCode was in the transactional business. We sold it in two thousand and six. We owned it for fifteen years. We sold it to CPI Crane National Vendors.
00:02:48 Speaker 2
So that CashCode used to manufacture currency acceptance devices.
00:02:54 Speaker 3
Are you based in Canada?
00:03:00 Speaker 2
We are making a move to the U.S. We're now a Florida-based company. We are in the process of exiting Canada and establishing ourselves in the U.S. But that's just the geographical presence. In essence, we never did any business in Canada. Our business has always been Latin America and Latin and North America.
00:03:36 Speaker 3
I used to work on the gaming side years ago, and it wasn't uncommon for people to ask, when they saw your name, what you guys do a little bit, just like an overview. They were like, okay, well, does he know where, in the U.S.? Our solution is isolated to the U.S. And so I said, well, a lot of these Canadian operators, they really do their business not in Canada, but it's just for ease of use and in terms of setting up shop, it's much easier in Canada.
00:04:10 Speaker 2
No. My family geographically lived in Canada. We were in Canada. We never had business in Canada, but we resided in Toronto. We now have. We're in process of my family's in process of exiting Canada, personally, and the company has exited Canada already. We're a U.S.
00:04:38 Speaker 3
Entity now. I tell you what, you're.
00:04:47 Speaker 3
States like Texas and Florida. I'm sorry.
00:04:51 Speaker 1
Yeah. Yeah.
00:04:52 Speaker 3
I saw your strategic selection of Florida, so I thought it was very purposeful on your part.
00:04:59 Speaker 2
We like it here.
00:05:01 Speaker 3
Good. When you say you do amusement games, is that so? You guys sell the hardware? That's what you provide?
00:05:10 Speaker 2
Is that your we provide hardware and software solutions for transactional equipment and for amusement equipment.
00:05:19 Speaker 3
Okay, and when you're saying amusement equipment, just so we understand each other in terms of like ready cook, because you know there's a compliance and regulatory piece of what we do. We do that via third party, and I'll explain what the process looks like once we inject that into our conversation. But is it primarily gaming, or do you guys do like other types of like I don't know, like Dave and Buster's?
00:05:45 Speaker 2
We We provide we provide gaming for gaming jurisdictions and we provide amusement for amusement jurisdictions. Right right now right now this particular conversation is for amusement and namely for the state of Georgia, Georgia okay very good and the particular conversation deals with competing with a company that you probably compete head to head.
00:06:16 Speaker 2
And we get partial service from them, and the company is called InComm.
00:06:22 Speaker 3
Oh, yeah. Okay, very familiar with them. Yeah, yeah. So you kind of like go into that that next pivot.
00:06:31 Speaker 2
And before and before we proceed, this conversation is this conversation recorded on your side.
00:06:41 Speaker 2
No, not as such. Okay. So for the record, I want to ask you a question. When we talk about InComm, are you competing with them or cooperating with them.
00:06:51 Speaker 3
They do — they do business with us. They have a prop. They have our surcharge - free platform today. So you know, and that's all public knowledge. I mean, if somebody wanted to get an InComm card, they you know set up a card and and they actually you know use a physical card. They transact on our ATMs surcharge - free today.
00:07:11 Speaker 2
So I want to so I want to make sure that. Is this information going to get to them? Is this conversation getting to them?
00:07:19 Speaker 3
No, we sign an NDA, you know. So we're these are confidential conversations we're having with.
00:07:25 Speaker 2
You. So if you provide your service to them, does it mean that you may not want to provide this service to me.
00:07:33 Speaker 3
No, we're we're you reached out.
00:07:49 Speaker 2
Is The is the exclusivity between you and InComm for those services that you provide to them.
00:07:56 Speaker 3
Well, the way we perceive our our interaction is, you've reached out to us as any customer would have reached out to us. Now, if you've heard of us through any intermediary, then that's beside the point. There's people that do that all the time, right? People can look and use our name for a product and say, " Well, who do you have it with?" And okay, it's with with you know NCR Outlets.
00:08:20 Speaker 3
So we've had no discussions with with them in relation to your business whatsoever. As a matter of fact, yeah, there's been no conversations with you guys.
00:08:31 Speaker 2
And the NCR, the the part of NCR is the is the the the NCR that manufactures cash related equipment, cash processing.
00:08:46 Speaker 3
Yes, yes, correct, correct, correct. We we do.
00:08:55 Speaker 3
Yes,
00:08:57 Speaker 2
And I dealt with NCR on the cash card side of.
00:09:00 Speaker 3
The business. Yes, yes. And formally, the way the way just structurally, so you kind of have a little bit of an idea of how we operate. Years ago, I'd say about eight years ago, they bought out Cardtronics. NCR, obviously National Cash Register, they've been around for 140 years, and so they wanted to, I guess, elevate the profile of what their product offering was. So they bought up.
00:09:28 Speaker 3
Not the NCR side of the fence, and so we, you know, became one company. Unfortunately, Wall Street didn't eventually find that very attractive, and so we, we hope to have done better. But eventually, that split, and now we've been, you know, bought out by Brinks, and and that that transaction is in flight, and you know, we've everything's been approved, and we expect, I guess, in the new year to maybe some logo changes at some point, but name changes for sure.
00:10:02 Speaker 2
And what is the prime nature of your business? Is it the ATM side or ATM processing.
00:10:08 Speaker 3
It's the ATM side, right? And specifically, my patch is for surcharge - free partnerships. I work on the fintech side of the business, and we also have a banking side and commercial banking enterprise as well. And so we work with both with the hardware, and then obviously, you know, the bank has its products, and you know, our fintechs have their additional products. My segment is specifically on the fintech side.
00:10:35 Speaker 2
Okay, all of this is new to me, so I might I'm not understanding a lot of things, and I might might be asking silly questions or repeating myself. So forgive me in advance.
00:10:51 Speaker 2
No problem. My last point. Well, so are you familiar with the business in Georgia?
00:11:02 Speaker 3
Like your business in Georgia? No, no, no. Is this amusement product? No.
00:11:06 Speaker 2
InComm's business in Georgia.
00:11:08 Speaker 3
Not specifically. They have a lot of business throughout the country. So, specifically in Georgia, what do they have that?
00:11:19 Speaker 2
So InComm has offered a transfer of.
00:11:29 Speaker 2
Transfer of funds from amusement games to a Mastercard prepaid card, and then from Mastercard prepaid card, it's a digital transaction in the background to to a card called Prize Play or Prize Play. I don't I don't remember Price Prize Play. I think. Okay, I can look it up.
00:12:01 Speaker 2
Yeah, something like this, and then the and then price play card specifically could be validated in any ATM machine.
00:12:13 Speaker 3
Okay. So basically, it's a prepaid card. I go up to it's a physical card, though, right? We're talking about a physical card, not a virtual card. So basically, is.
00:12:34 Speaker 3
Dump some funds into the account, and they send me a card, like a physical card, and then I go use it and maybe get some discounts or something aligned with you know amusement as well or points or how does how does that work.
00:12:49 Speaker 2
So you take the points from amusement, you deposit on Mastercard prepaid.
00:12:57 Speaker 1
Ah,
00:13:00 Speaker 2
Okay. You take the you take the Mastercard prepaid. Paid in the background, it's a digital transaction, and it becomes and it becomes opaque to to a player. He doesn't see, and all he sees is the issuance, physical issuance, of the second card, which is price, price,
00:13:28 Speaker 1
Play. That makes sense.
00:13:31 Speaker 2
And he and he takes. And He takes this card physically. It's issued. It's dispensed by a kiosk. Okay. Or by a life attendant. Doesn't matter. Okay. It gets validated through InComm. Some sort of a cycle. Okay. And we have an API to it, so we process it. We call we call the API.
00:14:02 Speaker 2
They validated. The cashier behind the counter, using our point of sale kiosk, or our attendant-free kiosk, dispenses the card or physically hands the card to a player. The player now is in possession of a plastic card. He can take this plastic card, go to an ATM machine, pay a fee. Swipe the card and get cash.
00:14:34 Speaker 3
So I'm a cardholder. I walk up to this machine. I just want to make sure I understand. I walk up to the machine. So basically, the more I play,
00:14:45 Speaker 2
The use the use case is different. So these machines are located in gas stations. Okay. The state of Georgia has seven four hundred locations. c-store type of locations in gas stations. Okay, forty-seven thousand amusement licensed machines. There are regulated by GLC, Georgia Lottery Corporation. So the points that you win on the machine. Sorry. So the use case is this: so the player enters a location, comes to a cashier or to a to a freestanding kiosk, inserts inserts twenty dollars.
00:15:32 Speaker 2
In exchange of twenty dollars, gets a barcoded e-wallet, a ticket, like a printed ticket the size of a dollar bill. It has a has a barcode on it. Comes up to an amusement machine, scans the ticket. The machine understands that it's twenty dollars. It plays through the games. He earns credits. He scans the QR code again.
00:16:02 Speaker 2
Now let's say he won thirty dollars. So the total value is fifty. Okay. It goes back to to the cashier. The cashier has a point of sale, or alternatively, to a kiosk, which has an optical scanner, scans the scans the temporary e-wallet. It shows them the value of fifty dollars. Offers the card. Okay. Point of sale, or the unattended kiosk, calls InComm through an API. InComm approves the transaction. The card gets dispensed or handed to a player. Okay. A player can take the card, walk up to an ATM machine, insert a card into an ATM machine, and get.
00:17:00 Speaker 2
Fifty dollars minus the service fee.
00:17:04 Speaker 1
Okay.
00:17:07 Speaker 3
I appreciate the explanation, and I know it was pretty detailed. Thank you very much. And so that makes sense. So I, as you said, so I walk up. Sean walks up. We hand him hundred bucks. We want to, we want to gamble. We we win a hundred.
00:17:32 Speaker 3
There's no.
00:17:32 Speaker 2
And I encourage you not to call it gambling because the state of Georgia prohibits gambling. The legislation explicitly prohibits gambling. We explicitly approve our machine through a testing laboratory to ensure that it's not a gambling device, but rather an amusement device. It's called a skill amusement device. Skill feature.
00:18:01 Speaker 3
Amusement device, okay. Skill amusement device, okay. So, I take the QR code or the the the the like as you said, I get almost like a almost like a dollar, but it's got a QR code on it. It's got some monetization behind it, whether it's twenty dollars, as you said, or a hundred dollars. I go, I put it into a machine or put it into multiple machines. I finish my skill amusement play, and I walk out with a hundred and forty bucks. I take that. Point of sale, or individual, or kiosk. There's an API call that's made. What's offered is a card at that point, and then an API call happens on the backend between InComm and yeah, between InComm and this card or that machine. And then a card is a card dispensed at that moment, or is it sent via mail?
00:19:00 Speaker 2
It's dispensed or handed over, yeah, at that time.
00:19:03 Speaker 3
Okay. Okay. Okay. That makes sense. So, how do you see? Now, we've talked about. You kind of have an understanding of our product. Yeah, it's ready code.
00:19:14 Speaker 2
I don't understand your product. I actually so my my question is because I don't understand your product. What? What? How do you see yourself fit into this relationship, if anything at all? And what services can you provide in in this in this link in this chain? And can your services replace InComm services.
00:19:40 Speaker 3
So the way so we have already put products right. So you you'd ask us about our carded network, right, and how we work with our surcharge - free partners. Well, what we also developed here in the last five years was a a product within the NCR umbrella.
00:20:06 Speaker 3
Leverage our already like robust infrastructure of ATMs that are out there today. When I first started, there was like seventeen thousand. Now there's almost thirty thousand. And so what we do is we do it all via code. Is the way our our transactions are initiated. So rather than hand over a physical card that could get lost, misplaced, most of our customer interactions and the way it works, at least from from like your level, the operator level, to the card to that.
00:20:34 Speaker 2
I need a card. I need a card.
00:20:38 Speaker 2
I need. I need. Advant. I understand advantages of not having cards. You don't have to convince me. The law says you must have a card. So it.
00:20:49 Speaker 3
So it doesn't matter. Okay. So it doesn't matter. So at the end of the day, however they want to transact. In other words, as an option. So think of us as like almost a menu option of how you want to get your cash. So much the same way somebody could say, take those funds and say on this card or that's there.
00:21:08 Speaker 3
Bank account, or I want to go to the ATM and take it out physically by putting my card into that machine, or I, you know, want to let the funds sit there until I play the next time, or if I need to access those funds in any kind of way, they could through Ready Code end this card. Doesn't matter if they still have a card; they can say, "Well, if I either don't have the card in my possession."
00:21:42 Speaker 3
It would be a tile that would sit on the app. They'd hit it, and then they would request the amount of funds that they would want to retrieve. So that could be from twenty dollars all the way to you know four hundred dollars, or you know we can talk about amounts that are higher than that as well, and even lower than that if you will. So it's all customized in terms of that regard. The code is as active for as long as you want it, and and then I'm able to transact, and so. So that's the way, I mean, conceptually, would work. You're just giving somebody another way that they can access their cash. We deal with like DoorDash and Uber and other gig economies where people say, okay, well, it's nice that I can take these funds and push them to my account, or but I want the immediacy of the cash in my hand, and so that's where we come in. We can say, okay, well, we'll give you this menu option.
00:22:42 Speaker 3
And so it's two-point authentication. It's via your phone number, and then via the code that's been issued. And on the back end, what happens is it's a pre-staged transaction. And so you know they can access the cash at their at their discretion, if you will. And and so they can you know determine that they can you know make multiple requests. And so if I wanted to get.
00:23:13 Speaker 3
Couple of codes, the two things that happen on the back end on the API side are verifying the code and then the dollar amount, and that's it. It's all done via API as well. So in terms of functionality, that's I guess how I would perceive it working in your.
00:23:33 Speaker 4
Space. Do you have.
00:23:46 Speaker 4
Prepaid card, or you don't have that today for for this game, because what happens? What what we are talking about is more on app integration, right, through an API and getting the code for cardless transaction in ready code. But if you already have a card today, then it could be something that could supplement that card for the amusement.
00:24:17 Speaker 2
I think I understand what you're saying, and I understand. Because this is a new concept for me, it's almost like I need to let it simmer a little.
00:24:37 Speaker 3
Bit. Val, I've got a deck. I can share with you if that'll be easier for you.
00:24:45 Speaker 2
And and and and Sean. Sean, just to just to answer your question, because I don't want you to think that I that I'm avoiding your question. I'm not avoiding your question. I'm just trying to think along the lines of your question. A player does not have a card. He doesn't carry a card with him. And a player is always a cash player.
00:25:16 Speaker 2
So he doesn't have a permanent card, and they are reluctant to give us their phone number. I mean, we will encourage them, and the business eventually will move into the direction of give me your phone number. And so, the the only phone numbers that, or the only known entity today that. Processes that transaction locally at the locations themselves, and these locations themselves are licensed entities. So, in order, in order for us to be sure that we comply with KYC, we register the location as a processor.
00:26:17 Speaker 2
I'm not sure, Sean, that I've answered your question.
00:26:20 Speaker 4
Or yeah, no, I.
00:26:24 Speaker 2
Understand. And and Carlos, when you saying that, you kind of need the identification, and you know, I'm assuming, give me your phone number, and that's that's how you get your. Or maybe I misread you.
00:26:38 Speaker 3
I don't know. Yeah, the the KYC that that you know, and I guess this is just.
00:26:48 Speaker 3
The way that KYC is typically done is obviously you're you're getting the the PPI the personal identification information from somebody. Like even when they set up this card, right? This is without us being injected into your mix, right? When people set up a card, I'm sure they have to you know provide who they are. Well, in that process, you know they you know we can use an account number or in terms of the entry into the ATM, right? Because I mean somebody has to put in.
00:27:18 Speaker 3
Usually comes in the form of a phone number in our world, and so somebody can utilize it and put input in their phone number because they know their phone number. They're not going to know their account number. I've been using Chase for twenty years. I don't know my account number, but I know my phone number, and so I put in my phone number into the machine. That's the identification that we, that you know, most customers quantify for. You know, people using our our card or our ready code transaction, and then it's the code that's issued by.
00:27:50 Speaker 3
With you, or with Uber, or with DoorDash, or whoever that may be, they are initiating the code. We're not initiating the code, but it's all done via API, is the way it works. So we're not collecting any anything else that's not already present. So if you guys, you know, issue an account number, whatever is the like, I guess the first identifier at our ATM is what you know fits in your world and.
00:28:21 Speaker 3
An account number or a phone number, then certainly that's the way that they would initially access the ATM once they walk up to it. When I was,
00:28:30 Speaker 4
Yeah. Well, just a quick question. Earlier you mentioned that in the state of Georgia you need a card, right? So for the card issuer to provide a card, don't they need the phone number and the name at least to provide the card, or do not need this?
00:28:47 Speaker 2
No, no, they don't because they ship their, So they ship their cards. Well, InComm. InComm ships their cards to a licensed location that has the amusement devices inside. And because the a player comes in with cash, there is no reliance on the player for KYC. The reliance is on the licensed location to to know to know their player.
00:29:22 Speaker 2
And so, because the location first, first there is a process of registering a location. The location gets registered. Then, InComm ships blank cards with barcode on it, which is probably similar to your ready code, but now they have the physical barcode. And so, at the point of pairing, the amount of money. With the blank card, they scan the barcode on the card. They now know the amount of money to be transferred on that card. There is a call to an API. There is a sorry. There is an API call to InComm. Then there is a pairing process. So now they married a barcode with the amount of money, and the transaction ends.
00:30:22 Speaker 2
So now they have a physical card, with which they could come up to an ATM and redeem it through an.
00:30:32 Speaker 1
ATM. So, balance.
00:30:38 Speaker 2
Did I answer your Did I answer your question,
00:30:40 Speaker 4
Sean? Yes. So in this case, you are actually validating the the merchant, right? You are not validating the end customer. You are validating the.
00:30:54 Speaker 4
You are getting that,
00:30:55 Speaker 2
Yes, correct.
00:30:56 Speaker 4
You are KYCing that basically, and all the cards are their responsibility. Correct,
00:31:03 Speaker 2
Correct, and all and all the cards are blank, sitting inside of a dispenser or covered in the sealed envelope. Understood. But they're blank.
00:31:23 Speaker 3
We used to do something like this years ago when I was doing the. We used to work doing employer programs when I was with prepaid, very similar environment. And before somebody got like their permanent card, but this is different in that regard. You're basically saying because in our world the way it used to work is somebody, let's say for example, got hired as a we would partner with like day labor companies like on a national level, and they would say, okay, I just had Sean come in, I just hired.
00:31:57 Speaker 3
Next week for the work he's done. Here's a card. There's nobody's name on it. I'm just giving you a physical card because I've got to deliver payment to you, and you can use that card. I'm as the as the person that's considered the registrar, or in your environment, the way you explained it, the licensed entity. I've validated who Sean is already.
00:32:24 Speaker 2
And So the maximum value in order to fall under KYC is a thousand dollars.
00:32:30 Speaker 3
I knew, yeah, I knew there was going to be a maximum. I knew there was going to be a maximum. Okay, so it's a thousand dollars. Okay, okay. So is that card, is that card from your experience, or is that card going to be, it's purposed for almost like a one - time use card, or is it purposed for I'm going to. I really like this card. I'm going to keep using it, and then maybe even put some money into it. Or is it? Does it not have any method for putting money into it?
00:33:02 Speaker 2
Right now, it does not. For some reason,
00:33:06 Speaker 1
But I know that technology is already available from multiple sources to put money into it. So I don't. I don't understand why InComm is truncating this functionality. I'm not sure. Maybe it's their own.
00:33:23 Speaker 2
Limitations, but it's certainly not a technological limitation.
00:33:29 Speaker 3
No, no. This sounds more like um maybe there's some compliance reason or some regulatory yeah something something along the regulatory lines that maybe they don't allow that. But so so this thousand dollar card, if I just leave the let's say okay the max is a thousand. Two or three hundred that I won. I I guess now that I've been given a card, this is where I want to understand for me about as well. So now that I've been given a card, does the card go into the machine so I can play? I can do the amusement, or do I have to go back and get another QR code with another redeemable amount to to use?
00:34:17 Speaker 2
No, there is cashback program.
00:34:21 Speaker 2
So the card offers either ATM redemption, or cash or cashback program, or partial redemption.
00:34:29 Speaker 1
Okay,
00:34:32 Speaker 3
That's right. Okay, or partial. Okay, partial. Okay. So really, it's almost if a it almost sounds like a one - time use card is almost what it sounds like. Or is that that sound about right? It's like a one - time use card.
00:34:47 Speaker 2
Correct. Correct. It is.
00:34:49 Speaker 3
Okay. That that gives me a lot of perspective. Okay, so if you go ahead and and I'm sure like people like misplaced the card and what have you. So I don't know the the way. I'm just trying to think of how it would work in your world. Is nobody's going to remember their card number, right? And so you know if as part of this program to get their cash, it's optional.
00:35:20 Speaker 3
That you know, I guess it's a phone number. They would have to know the person's phone number that's carrying the the card. Otherwise, it's just provided as an option on the app. Is there any? Is there any connection, Val? To I know that there's a physical card, but is there like an app that's connected to this today, or or how does that work for the cardholder?
00:35:40 Speaker 2
Today, in the Incomes business scheme, there is no connection to any app.
00:35:52 Speaker 3
So this is one hundred percent a card program that they offer. There is nothing else.
00:36:00 Speaker 4
That helps. Okay, and and you said the state of Georgia requires you to have card and not cardless,
00:36:08 Speaker 2
Right? Ah, I cannot say it with hundred percent reliance. But I can tell you that InComm that has two thirds of the, maybe more than two thirds of the market. That's what they do.
00:36:30 Speaker 3
But they provide the card.
00:36:38 Speaker 2
Okay. There is there is a competitor program that that is fully digital. Okay.
00:36:51 Speaker 2
But I don't know much about it.
00:36:52 Speaker 3
Okay. But for your for your purposes, do you have do you have any connection to the customer at all? Does JVL have any connection to that customer other than the hardware that they're that they're using, or you don't have an app, or there's no app today, for for the customer.
00:37:17 Speaker 2
So.
00:37:20 Speaker 2
At this moment, as we speak, we don't. But, but what our hardware does, and this is an important element, we offer an insert inside of a machine that we, in the industry, called AFT, Automated Fund Transfer. Now, I'm taking this out of a casino business, so the. The casino calls it, or casino in casino business, it's called AFT, Automated Funds Transfer. Okay. So by the way, the connection works. It connects to machine counters, and one of the counters is obviously, you know, cash counter. Then there's a promo counter, and and on and on. There's probably a list of thirty some counters inside of every machine.
00:38:20 Speaker 2
They're virtual counters. They used to be mechanical, but now they're virtual. So through that AFT device, we can build various programs, digital programs that connects us to a customer. That's our way to the customer. And so, of course, our intent is to build.
00:38:49 Speaker 3
Automated Funds transfer and pay. Build out the programs.
00:39:02 Speaker 4
So, I also checked internally with my compliance department if they know that in the state of Georgia it requires to have card or cardless. I'll check that separately.
00:39:18 Speaker 3
That's going to be important. That piece, the automated fund transfer. You're talking about that? So you're open to at some point. You kind of built the business in such a way to where you want to do. You want to do this AFT to back to JVL? Is that safe to say?
00:39:41 Speaker 2
I'm not sure. I understand the question. Can you rephrase your question?
00:39:49 Speaker 3
Yes. So this AFT allows them to offer promos within the machine. It's a virtual counter. Are you? Is there going to be? The reason I'm asking is I just want to understand. Is there a future where an app is going to be something that JVL develops because that's what I understood from what you shared.
00:40:22 Speaker 2
We're absolutely on that path. However, just to be sure, we don't need to develop it. We could ride on your app and just put a layer of our own thing in it. We're quite open.
00:40:40 Speaker 3
To that. We don't have an app. Just all we are is
00:40:49 Speaker 2
Then we're definitely moving in that direction. There's no questions about it. There will be a JVL app, and there will be a touch point with the client, direct with the client.
00:41:01 Speaker 3
And this is great because it is helping me understand. It does give you a method for you to do more business. I'm sure there's a multiple. I'm sure you can put a locator.
00:41:19 Speaker 3
There are.
00:41:21 Speaker 2
There are many ways we could utilize it. It's only limited by one's imagination.
00:41:29 Speaker 3
Of course. Okay, okay, okay. This is really helpful. Okay, so in terms of ready code, it can. I guess the way it functions today. Let's talk about maybe the way it functions today, or or the way you can. Maybe inject this into your into your way of doing business today. Is it could just be a menu item of the way that people retrieve their their funds on without they they have to have a card. Or I guess we may find out. You know, Sean's going to find out whether we do need to have a card or we don't need to have a card. But there's going to be a way for them to transact cardless with ReadyGo if that's an option you want to you wanted to give them.
00:42:17 Speaker 3
As you move forward, as you develop the app, you know the app, and you start building towards more touch points with this person that went and got this card. Then you can put the ready code tile on the app, and it's just another way that they transact, and it's creating another touch point as well with the cardholder.
00:42:44 Speaker 2
So what I'm what I'm trying to understand, and maybe Carlos and Sean, maybe you could help me understand this. When we transact, when we have this massive amount of cash going through our account, where do we deposit this money? And and and maybe my second question now that we've deposited this money for however. Long or short period of time that money is in direct, in direct, account. Number one, what influence do we have over this money, and how how how do we make money on this money? Because I mean, there has to be some business out of transacting. Otherwise, why would I be transacting if I cannot make money on transacting.
00:43:39 Speaker 3
Sure. Sure. So there's a couple of, So you asked just from almost like I mean, it's a real critical question in terms of the way you transact. So there.
00:43:52 Speaker 2
It could be a stupid question. Maybe I don't understand what I'm asking.
00:43:58 Speaker 3
No, no, no. You're asking a great question. So the way the way we settle and the way our our backend works, if you will, is somebody sets up. In this case, if you were looking for cash in or cash out, we have what's called an FBO account. For the benefit of is what it just stands for, and basically it's two it's two accounts. One for these are pre-staged transactions, right? So if I'm initiating a code right through this ready code system, we're pre-staging the delivery of those funds, and so there's there's two accounts that sit in the back end that our partners set up, and what happens is those funds are.
00:44:43 Speaker 3
We keep funds in the account for cash out, right? Because we're pulling cash out. That's pulling from an account. It's got to pull from some account. So what our issuers do, or what our partners do, is they set up what they call an FBO account. That's that would be a pre-staged account. So I go to the app, or I make a request for this cashless or cardless transaction. I say, okay, I'm going to select two hundred dollars. That's what I want to take out of the account. So we pull those funds from the FBO account, and we do what's called a Pre-staged transaction, so that code is valid for as long as you can make it for until it's redeemed, or you can give it a time window of like 24 hours or whatever you want to provide in terms of the customization around that. We can work with you, but that's a pre-staged transaction. Same occurs for cash in. There's an account for cash in, and as funds are going into that account, because I'm on my ready code, whether it's the app or I've made a ready code request.
00:45:43 Speaker 3
Cash in. You know, I've got a hundred dollars, and I've got a hundred dollars, and I want to put it towards this account. Well, I'm going to go up to the ATM, and I said, okay, I want to, you know, I want to play with, you know, two or three hundred dollars today. I'm going to put it into your ATM via this code that I was given. They put in the information, they put in the code that they just generated, and they're putting now cash into the account. And that's also a pre-staged account. So on the back end, there's one account. That's receiving funds, and there's one count that's dispensing funds, if you will, that our partners set up on the back end, and those because we have to settle daily is the way it works, and so by one thirty every day we settle, and so those funds are you know closed out that day or the following day based off of when they they the transaction was initiated at the ATM.
00:46:37 Speaker 2
This is assuming that ATM is the source for incoming and outgoing.
00:46:44 Speaker 3
Correct. Sir.
00:46:46 Speaker 2
And and it has to be the same ATM or various ATMs doesn't matter. ATM. Any any ATM on the network based on the ready code. So if I want to input the money, I put my ready code. I put in the money. That's the incoming funds. If I want to take out the money. I put my code; it checks my in whether I have money in the account within that code, and says, " Yeah, you could take out twenty dollars." Correct. And for and for every transaction in and out, it charges me a fee.
00:47:25 Speaker 3
I assume. Correct. And you can monetize that fee. Today, I'll give you a good example. Today, if I go to a green dot location, it's not usually a great experience because I'm having to deal with an individual, and that individual may know how to take the cash and process the transaction or may not know how to do it. The customer experience can be pretty good or pretty bad. With ours, it's self-service. What we've got enabled today is thirty thousand machines that are ready code enabled for cash out. As I shared with you when I first came on board four years ago, it was seventeen.
00:48:07 Speaker 3
Thousand and so now it's grown up to thirty thousand. And for cash in, we're around thirty eight hundred machines that have cash in capability. Right, not all of them are the same, but that's where the geo locator that we that we provide you in terms of the API will help support that transaction. So me, who's been issued a code, whether it's for cash in or cash out, I can say, okay, where's the nearest location? You can identify it in one of three ways: the address. The longitude or latitude, or the zip code, and so it'll isolate for that user where the locations that they can transact.
00:48:44 Speaker 2
It's actually okay. Can I ask you a question? Sure. If it's not green dot, then you cannot transact. It has to be green dot.
00:48:58 Speaker 3
No. I just brought up green dot as an example because for that experience, it's like five dollars.
00:49:09 Speaker 3
What I'm saying is, you can monetize that experience, and it's a much better experience. I just brought that up as an example. Green Dot's pretty expensive, and the customer experience is all over the place. It can be good, it can be bad on our network.
00:49:23 Speaker 2
Gotcha. So Green Dot is a competitor. I didn't realize that. I'm bad with names.
00:49:31 Speaker 3
No, no, it's okay. And if you went to a Green Dot location today, if if you looked online, you you're not you know talking to Carlos. You you we hang up the phone and go. Deposit money into my account. Let me look at the Green Dot locations. Oh, it's like five dollars and fifty cents is the average transaction cost. It's very expensive, and it's not usually a very good experience. And and that's the difference. So we're completely different. It's our ATMs. It's self service, and you know, self service doesn't make mistakes typically. Okay, gotcha.
00:50:01 Speaker 2
Gotcha. What's the name of your service?
00:50:04 Speaker 3
Ready code. Ready code. So it's ready code for cash in. Ready code cash.
00:50:09 Speaker 2
So JVL, I assume I'm hypothesizing here. This is more of a question: Can JVL subscribe to ReadyCode service to receive that code so we could transact under the ReadyCode logo or ReadyCode business model?
00:50:34 Speaker 1
Correct. Yes.
00:50:39 Speaker 2
And so, being a subscriber to Ready Code Service, what do I need to implement on my side?
00:50:53 Speaker 3
Okay, so let's delineate a couple of things, right? So, Ready Code is our is our product, right? Ready Code is our product. the The people that we partner with, like the companies that we partner with, they're they're, They put their own brand. We're agnostic, so basically, it's you know, yes, it is ReadyCode. That's the you know, that's the you know, the logo and the label that's ReadyCode. But we do that for you know, DoorDash or Uber or whoever. So they have their branding sitting over that. It's their it's their solution. We're a solution on the back end to help support their program.
00:51:34 Speaker 4
So it's not like, right? So Paulo, I think is. Question was what you need to do. Basically, what you need to do is you have an app, and your app should be able to do API integration to our Redigo backend in order to implement Redigo, basically.
00:51:51 Speaker 2
Okay, so when I integrate it through your API, let's go through use cases.
00:52:04 Speaker 2
So a player comes into the location and comes in front of a machine. Inserts or how does he get your code?
00:52:22 Speaker 4
Carlos, if you go back to the slides where the PlayStation transaction, so so in this, just imagine this is a JVL app. You have logged into the app, and then you have your balance there. For example, the customer has about two hundred dollars, and he wants to take out sixty dollars, right? So he clicks on the ready code button for cashing out, and then he will put in the amount, which is probably sixty dollars. The next screen is your JVL app can also show the nearest ATM where he can get cash out. So if there's one ATM next to him, for for example, it's not so far.
00:53:04 Speaker 4
He just decided to say, "Okay, I'm going to go to that ATM. I'm not so far from it." And then your app will actually generate an eight-digit code. Okay, so this is all done by your side, right? You will do all this part over here. We can give you an API to get the nearest location. That does. We can give you that access, or we can give you all our locations to your IT department, and then they can populate it into your app. Now, next slide, Carlos. Once they are in the, Once they have reached the ATM location, all they have to do is click on verify code. They will put in an account number or a phone number, depending on your user, right? If you think you you are collecting users a phone number based on your app, then you can put a phone number, right? So something that they already know. So they put in their phone number and then they click next, and then their eight-digit unique code that that will define that money that's being pre-staged by your app.
00:54:01 Speaker 4
So when you put in that eight-digit code, right, the ATM will know. Oh, this is a JVL transaction, right? Let me go and check with JVL backend. So we will check with your API, and your API will say, "Hey, with this phone number and this code, what is the value?" Then your API will say, "Yeah, that's a valid transaction. The value is sixty dollars. The guy just created the code. Okay, then he was responded to the ATM. Now in the front of the ATM, the guy will just have to press confirm, because they cannot they cannot modify.
00:54:31 Speaker 4
Because they created sixty dollars in their app, they want to withdraw. They can confirm and get their cash and walk out. So that's basically it for cash out.
00:54:39 Speaker 2
Carlos, Sean, will I be able to get this presentation or should I take screenshots?
00:54:46 Speaker 3
Or no, no, no. I'll send you the deck file, and that's not a problem.
00:54:51 Speaker 2
So how many ATMs do you have in the state of Georgia?
00:55:02 Speaker 3
Off the top, I don't know, but I can give you that when we wrap up this call.
00:55:05 Speaker 2
And so, can I send my customers to your ATMs?
00:55:10 Speaker 3
With the API connection? Correct.
00:55:16 Speaker 2
Yes. So then, what is the charge for incoming and withdrawals.
00:55:22 Speaker 3
Those are the commercials. We haven't dived into the commercials today's call.
00:55:28 Speaker 2
Give me. Give me ballpark. Give me a retail price.
00:55:33 Speaker 3
Ballpark for two dollars and seventy five cents. Two dollars, about two seventy five.
00:55:40 Speaker 2
For withdrawal or for deposits.
00:55:43 Speaker 3
That's for withdrawal. Great question. Deposits are normally based off of. It's roughly going to range anywhere between. It can be as low because we do it off of a transaction cost plus. An interchange, and so it can be fairly low. It just depends on you know what what your volumes are. I have to get you get back to you on that specifically, but it's going to range. It can be as low as a you know a dollar ten or eighty five cents, or it can be as high as you know three dollars. It just depends on what dollar amount is going to be your maximum, and what they're going to input. The higher the more money they put in, obviously the more risk, the more times we have to send trucks to go pick up the cash.
00:56:29 Speaker 3
So you know we got to factor those things in, but I would give you a range of you know between, and I know I've hemmed and hawed a little bit on the price on deposits because it is a little bit different, but we've come up with some unique commercial schemes that I think will help keep it a little bit more simplified. But let me take back what you shared and give you more of a specific dollar amount. But it could range between a dollar twenty-five to you know four dollars. Depends on the dollar amount that's input, but like I said, we can come up with something unique for you that's a little bit more streamlined. So we have about a.
00:57:07 Speaker 4
Thousand thirty - two machines in Georgia.
00:57:09 Speaker 2
Okay, thank you. So if so, if I was going to no before before we go there, and this is so Carlos, when you're saying roughly and you're throwing numbers around, and those are retail numbers, and I'm not really, Paying much attention to it, let's call it five dollars for combined cost of deposit and withdrawal. I don't know how to judge it. Okay, does it include the cash pickup? Does it include the the secure secure truck round?
00:57:54 Speaker 4
Yeah. So well, we take care of everything on the cash.
00:57:59 Speaker 4
So when when the person puts in the cash, cash loading into the ATM, what we do is the next business day we will transfer funds to your bank account based on the cash in. We will do an ACH transfer. It includes that as well, and and it goes the other way as well. If somebody takes out cash, we would then pull funds from your bank.
00:58:21 Speaker 2
Account. No, Sean. Hold on a second.
00:58:28 Speaker 2
The five - dollar charge does it include the the drinks refill, the manual labor of servicing the ATM machine, or is there an additional weekly or monthly charge to fill and to collect cash and to no.
00:58:46 Speaker 1
No so.
00:58:49 Speaker 2
So that five dollars is taken care of all the cash handling.
00:58:57 Speaker 2
Okay, okay, hold on. I I have another meeting. I'm going to postpone the other meeting because the conversation is developing. One second, please.
00:59:39 Speaker 3
And I check my calendar too, and I'm fine for like.
00:59:44 Speaker 2
Twenty minutes. Thank you, I appreciate it. Um, this is great. This is actually great. Uh, so, what if I could? What would it be for you? Is it important for you if I could add to your?
01:00:09 Speaker 2
Set of ATMs in the state of Georgia, another let's say two thousand ATM machines of my own, or will you not accept my machines? It has to be your machines.
01:00:21 Speaker 3
It has to be our machines, just because it's a regulated transaction through the FDIC, and there's a different.
01:00:30 Speaker 2
But if I sent you my machine for approval and inspection, would you work with me? To produce my machines, I would produce them. Can I put it on your network?
01:00:44 Speaker 3
You know, I would have to. That would be like, I guess, like a mini network is what you're proposing. And in our space, that does happen with with other providers. So I would have to, I would have to, you know, share that that that piece of information with the team, and then we'd have to have a deeper discussion on on what that means. But, We do take on other what we call mini networks, if you will, and so we'd have to look at you know what what that entails, and so I wouldn't be able to give you an answer today. But I'll you know I will say this: we we have had other partnerships that have like their mini networks with our surcharge - free product that's carded. Having a a red code one present itself as an opportunity, we'd have to have a discussion about it.
01:01:37 Speaker 2
Understood. So let's go back to your ATMs. Do you put your ATMs for free?
01:01:47 Speaker 3
Yes. So so what happens at our machine? So this is where where I thought like Sean was going, and where I thought you were going, and that's why I was like, okay, well, where where where's the conversation going? Just for just a second. It's uh we don't take uh it's a surcharge - free network, right? So when somebody walks up to our machine, there's not a cost associated.
01:02:09 Speaker 3
You partner with us, right? So nobody will walk up to our machine. That's your customer. That's you know been told, hey, that's a ready code machine, and they will not pay a fee at the terminal, if you will. So what's going to happen is on the back end, what our partners do. There's two things that they do. Sometimes they go, okay, we're going to make that one hundred percent surcharge free for my cardholder. Which in this case, if if Sean was my cardholder, I'll pay that cost. It's worth it to me. I have this benefit by giving it to him for free.
01:02:39 Speaker 3
Go okay. Well, I want to do that one time a month, but not more than one time. I'll charge them this dollar amount for every subsequent transaction. And then we have some partners that just say, no. I'm going to go ahead and I'm going to charge Sean every time that he takes money out or he puts money in. But the cardholder at the machine will not see that fee. What gets pre-staged at that point is the amount that you've determined you want to collect. So if I, in this example, we've used five dollars multiple times, so I'll just stay with that.
01:03:09 Speaker 3
If Sean wanted to take out that sixty dollars, it would be a pre-staged sixty-five dollar transaction. So that would be the funds that are held, so you know you can cover your cost of that.
01:03:22 Speaker 2
Transaction. I mean, I think I understand what you're answering, but let me let me repeat that. Sure. So my choices are for you to put your ready code ATM machine. In a location where either an end customer pays that five dollar fee, and then it would cost nothing to a location, or alternatively, the player pays nothing, so there is zero processing charge, and you charge a location a monthly.
01:04:02 Speaker 3
Fee. Correct. We don't necessarily do it.
01:04:14 Speaker 2
What would that fee be?
01:04:17 Speaker 3
That's what we were talking about. So it can be. We've talked about it being five dollars in this conversation. You can make it whatever you want. There is a cost, obviously, to do the transaction.
01:04:31 Speaker 2
No. What would be the monthly
01:04:32 Speaker 3
Fee? There's not a monthly fee that's set. It's based off of transaction. So if somebody does one transaction or thirty transactions, it's cumulative. It's an aggregate total, and we can't connect two dots. We don't have the customer's information. We hold no information. They're simply redeeming the code on our network.
01:04:55 Speaker 2
Are you saying to me that because you know how much money the machine has, you can basically break it into a per transaction fee and it doesn't have to be monthly?
01:05:17 Speaker 3
Fee. No
01:05:20 Speaker 2
So services cost money. If you are filling machines with cash and emptying machines of cash, you have to charge for it. Your crew will be circling around the locations, handling cash. So that costs money. You're not gonna eat that cost. You're gonna make money on it. That's normal for any business. So what do you charge for it?
01:05:59 Speaker 3
That's included in that dollar amount that we gave you. So that dollar amount of 275 that I gave you earlier. That's included in. So all of that is included. So the transaction cost for for our partners is, you know, it's it's a set amount. It's like okay, you know, we're typically the way our agreements work is maybe we're getting a little bit too far downfield on that piece because that's the commercials. But really, it's there's a transaction cost. We don't, you know, we're not going to come back and say, well, we've got to charge you more because this month you did, you know, we sent the truck out.
01:06:38 Speaker 3
Three times. No, there's a there's a flat fee that we determine. That's why these conversations, typically, at least on on the commercial side, do take some time to understand, like what kind of volumes you're going to do, because that helps me understand. Oh, okay, well, this is what it's going to cost to do this transaction for us, and so that that's where we factor that in. So there there is a per transaction cost, and then to your point, you know, yeah, obviously there's a margin that you can leverage for yourself, or you can make that free for.
01:07:13 Speaker 2
I need to get to that point. So what's next?
01:07:20 Speaker 3
Great question. In terms of projections, if you know what you're doing with your business, that's why we have these conversations.
01:07:31 Speaker 2
So, how much money do you transact per week per location?
01:07:35 Speaker 3
That's what I would ask you. What do you do today? Where do you project it to be? Not just in the next 12 months, but 24 months and 36 months out.
01:07:47 Speaker 2
I'm actually trying to get this information out of you because I don't know where to start. Do you have a typical location that you could share with me? What do you transact per location? I'm sure this data is available to you and it's at your fingertips.
01:08:06 Speaker 3
It's actually not. We have to every time, every opportunity we.
01:08:14 Speaker 3
We have to sit down with them and say, " Hey, Val and JVL's organization has projected that they're going to do this type, these types of volumes, and based off of these types of volumes, this is what we think makes the most economic sense for us." I don't know how to.
01:08:29 Speaker 2
I don't know how to project. I'm just starting in it.
01:08:33 Speaker 3
What are you doing today in terms of the transaction? Zero. Zero. Zero. Zero. So right now in Georgia, with these.
01:08:43 Speaker 2
Zero, zero. It's it's a new legislation. This legislation just went into going into effect. Zero right now. Okay. So I'm trying.
01:08:52 Speaker 1
That's context.
01:08:53 Speaker 2
I'm trying to understand what you do in your average location.
01:08:58 Speaker 3
You keep saying average location. We don't like it when you said amusement machines. Our speak is we don't do it by location. We just do it by customer.
01:09:08 Speaker 2
By.
01:09:10 Speaker 2
You have thirty thousand machines. What do you do in the machine? One machine? What? How much does it do per week or per month?
01:09:19 Speaker 3
We wouldn't be able to. We don't even have that information. Like, we don't even have that information.
01:09:25 Speaker 2
How is it? How is it possible? I mean, you have thirty thousand machines.
01:09:29 Speaker 1
How is it possible? Sure.
01:09:31 Speaker 2
Yeah. I mean, I mean, I'm I'm I'm okay if you don't want to share. If you're going to say this information is confidential, fine. But, I'm sure I could get it on on on on your annual report. I mean, it's not like all I need to do is to go into your annual report. I will probably get this information.
01:09:52 Speaker 3
Yeah, there's no report that will give you that information in terms of the machines. I will tell you this. So right here, what you see. So every location that you see yellow in, right? Those are our cash - in locations, right? That we've got throughout the country. Okay, everything that you see yellow. So Seattle up here. Los Angeles, Miami, over here, Houston, Dallas, New York. Those are our cash in locations. The reason those are our cash in locations is because eighty percent of our traffic for our network happens in those little areas, in those little cities. Right. So yes, we've got all the green coverage here for ReadyCo, but the majority of our traffic happens right where these yellow dots are. We can't. We can't. Nor do we have analytics. At least at our.
01:10:40 Speaker 3
An organization that's different. I probably it's it's different, but in a company like ours, I can never go. Okay, tell me how many transactions are happening here this month at this location. We'll never do that. We'll no. We'll not. We'll not only we'll never. We'll we never do that. We'll never provide that to anybody. That's really confidential information, and you know, I don't have access to it. You know, but in terms of where we do our volumes as a business, eighty percent of our.
01:11:10 Speaker 3
Yellow bubbles, and so as a you know, Atlanta, Georgia, of course, you know we've got Atlanta here covered, and so we do a lot of business in Atlanta. And it's not relative to the machine itself; it's relative to the partnership. So your partnership, you said, hey, I'm looking at a new product. I'm looking at launching. I don't have any transactions today. Well, that's a different discussion. So I'll take that information back, and I'll say, hey, isolated to Atlanta, Georgia, because that's important. You didn't say, Carlos. Hey, I want to open up in all fifty states. Do you see why it's important for us to have this conversation? I can't just say, "Hey, here's a price," and you know, you went to McDonald's or Burger King, and you can see the price up there. I have to go. Okay, you know, Finance Committee. They're really looking at expanding just in Atlanta right now. They don't have any projections to go beyond Atlanta or Georgia. And this is what we think they're going to do based off of what you.
01:12:10 Speaker 3
Have to work with right now, and I'm happy to have that conversation. But that's the reason we we have these discussions at length because we need to better understand what you're trying to do. So we have to we have to.
01:12:23 Speaker 2
Arrive to a price, Carlos. It doesn't matter how many circles we're gonna we're gonna make. Sure. Unless I get unless I understand the price, I don't know where to take this discussion any further.
01:12:40 Speaker 3
My team and say, " Hey, this is what you know. This is what JVL is is considering. They're they're basically green grass. It's brand new territory for them. They're not looking at all fifty states. They're just looking at at Georgia for now. And this is how this is what we we think would make the most sense in terms of pricing. I gave you an estimate two seventy five because that's what you asked and said, 'Well, just give me an estimate.
01:13:02 Speaker 2
' But I don't understand. But I don't understand two seventy five for money in or money out. Or combined to seventy five.
01:13:12 Speaker 3
No, that's that's what I was saying. So money out two seventy five, money in. If that's a consideration, because not everybody tells us, hey, we want to do money in. But they did tell us. I I know that, but you just told me that now. We didn't know that when we just started the call, though. We had to like find out what your goals were, right? So now that I know that it's money in, I'm going to take this back because we we sometimes what we do for relationships like these that are brand, As we say, okay, well, let's look at something that's more streamlined, and we can present you with something that's a little bit, a little bit easier to consume, right? And so, I'm going to do that. That's part of the next call. These are commercial calls. This, like I said, we're not McDonald's, we're not Burger King. You're not going to see the price, you know, because that's not the way we work. We have to better understand what you're, what you want. You know, you go to the doctor.
01:14:08 Speaker 3
Okay, Carl.
01:14:12 Speaker 2
Okay, Carlos. I think that I disagree with you, but I mean, it's your business. You can disagree all you want. Yeah, exactly, exactly. It's irrelevant what my opinion is. So, mine too.
01:14:24 Speaker 1
To be honest with you, mine too.
01:14:26 Speaker 2
So, next step. Can you propose, please?
01:14:28 Speaker 3
Next step. Yeah, I said we do this. I'll meet with with our internal teams, and we'll make some determinations on on what makes the most sense in terms of, That's the next discussion. It's a commercial discussion, and I look forward to having it. I'm excited about the solution you're talking about because we can do a lot of great stuff with this. Now, adding machines to it—that's a different element. I didn't know that when you opened up the call. Now I do. We can talk about that too, as well, and what that would entail. Right now, we don't do that for ReadyCode. As I said, we have many networks with other our carded business, but not with our cardless business, which is ReadyCode.
01:15:07 Speaker 3
Let me find out what the what the flavor for that is, and what the requirements would be because we've not had that presented. This product's only been around for five years commercially. It's been around for about three years, so it's a it's not a old product, but it's you know it's definitely kind of new still. So I'll find out for you, and and on the next call that we do, I'll we'll have a better discussion around that. Okay. Does that sound fair?
01:15:33 Speaker 2
Sounds great. Yeah.
01:15:35 Speaker 3
Okay. Okay.
01:15:42 Speaker 2
Thank you, and could you please send me the deck so I have it in front of me.
01:15:45 Speaker 3
Absolutely, yes, sir. I'll get that over to you.
01:15:48 Speaker 2
Thank you so much, Sean and Carlos. Thank you for your time. I appreciate it.
01:15:52 Speaker 3
Thank you.