---
tags:
  - product-development
  - banking-technology
  - fraud-prevention
  - val
  - juan
  - pavel
  - flex-pay
  - technical
---

**Transcript**

July 10, 2025, 12:03PM

**Nathan Carver** started transcription

**Nathan Carver**   0:04  
Alright, sounds good.

**Val Levitan**   0:08  
OK, I made another reiteration of the product bank that.  
You know.  
I I think, I think we have. I think we're making. I don't know if you had a chance to look at it, but I cleaned that up a little bit.

**Juan Martinez**   0:34  
It.

**Val Levitan**   0:35  
The the question, the question that I have is uh.

**Nathan Carver**   0:37  
Yes, I did.

**Val Levitan**   0:42  
The question that I have is.  
I separated Flex Tower from Flex Redemption Center.  
Or what we call a mini ATM. I did it on purpose, at least for this conversation right now. If we want to merge these two products afterwards, we can.  
But at least for now, I'm keeping a mental separation between the two, and the flex tower is a very simple device. It has a.  
Customer facing screen.  
And a card dispensing mechanism inside of it only.

**Pavel Frolov**   1:33  
Yes.

**Val Levitan**   1:37  
Where redemption center houses a bill recycler, so we may choose to make it.  
One one of the same, just to have a different option.  
Or we may choose to do the tower even more simplistic maybe.  
Just as a dispensing tower, very inexpensive, more simplistic and beef up the redemption center a little more, making a visual separation between the two devices.  
We need to think about it. I I don't know how to approach it right now. I feel that maybe this should be a separation.  
But I'm open for discussion.

**Nathan Carver**   2:38  
I I think it makes sense to start talking about it as a separation. That's fine.

**Val Levitan**   2:39  
Uh, I'm.  
I'm also uh.  
Mentally now realizing how complex the back office system or the validation system or the processing system. I don't know what how to call it yet, but that processing end of it.  
I'm now realizing how important and how sophisticated it should be, and how well designed it should be and how protected it should be.  
We're talking about potentially millions dollars per hour of fraud.  
And um.  
I honestly, I did not appreciate this subject fully until the meeting with Incom, but even even after that.  
I dismiss some of it and as I think it think it through, I realize more and more that I question JVL's capability in designing such a product.  
In Minsk.  
And I'm always almost thinking of maybe you.  
Going outside of our internal team for.  
For designing, for designing of this thing, it's it's a very, I think it's a very specialized thing.  
I need to sign in and it's gonna kick me out, so I'll be back in 30 seconds.  
OK, I'm back.

**Juan Martinez**   4:58  
Val, quick question regarding your last statement and your concerns, should we also be looking at some third party system technology now or?  
You're just that that's your early feeling and we're not, we're not there yet. Like you know, should we talk to easy links for for their SAS and Tito that they do already today as an example and that they're already entering the market.

**Val Levitan**   5:31  
SAS and Tito, I have zero concern. This is not an issue for me, but Easylinks is not a processing company.

**Juan Martinez**   5:43  
You're talking about the transactional processing part, OK?

**Val Levitan**   5:46  
I'm talking about give you an example. We we're validating your ticket. We're putting the money on the card. The operator is small.

**Nathan Carver**   5:47  
Read.

**Val Levitan**   6:03  
Hard to reinforce anything with this operator. I want to wipe my money from his account, or at least validate that he has enough money on his account prior to validating the card.  
So it should be possible for us to do because these sort of things, depending on the contract that we sign with an operator, should be available to us.

**Pavel Frolov**   6:25  
OK.

**Val Levitan**   6:32  
But I don't think we know the technologies and then out and all the intricacies of banking implementation.

**Nathan Carver**   6:32  
Mhm.

**Pavel Frolov**   6:41  
Oh.

**Val Levitan**   6:41  
Also, when we swipe somebody's account, the money needs to come in into our account. We need to. We need to have instant validation that the money appeared on our account. It cannot be delayed over a couple of days until we're able to.  
Reconcile all the deposits and we cannot reconcile deposits manually. It has to be an automated reconciliation and we have to see all of it almost instantaneously. And JVL is not capable of designing something like this.  
And if we are, we're going to make so many mistakes and it's going to cost us so much money.  
But the SAS and Tito is not my issue. I, you know, we're quite capable of designing all the intricacies.

**Juan Martinez**   7:27  
Yeah.

**Nathan Carver**   7:45  
So we have several specialties coming in in the application server. This is all outside the hardware. So financial transactions, fraud detection, right, are the two specialties and then you have the security specialty.  
And that expands beyond just authorizing the device, but also security internally, because you want to create your own internal audit trails so you don't have malicious actor on the inside.

**Pavel Frolov**   8:14  
Yes.

**Nathan Carver**   8:18  
Helping someone commit fraud on the outside.  
So yeah, it's a significant amount of, I guess, structure to put in place.

**Val Levitan**   8:29  
So just like you expressed yourself, we should probably.  
Frame this piece of software in a separate application, and if we can frame it and define it separately, then we should probably subcontract it to somebody else. If we are not able to subcontract it to somebody else, we should.

**Pavel Frolov**   8:53  
OK.

**Val Levitan**   8:55  
Just like we discussed in the meeting with subscribe to this service, the existing service already, and have somebody else process it for us, at least for the time being.  
Until we design this, design and test this application properly and maybe a year after substitute for an application.  
But when when you guys think through architecture of the entire system.  
This application needs to stand on its own, in my view.

**Nathan Carver**   9:39  
Correct. Independent of any of the devices, all of its modules can work independently.

**Pavel Frolov**   9:42  
It.

**Val Levitan**   9:45  
Well, this module has to be described as a separate application or separate module.  
Um.

**Nathan Carver**   9:52  
Yeah.  
Like fraud detection, transaction management, is that that's all you're thinking?

**Val Levitan**   10:02  
I'm thinking as transaction processing and call it transaction processing. Within this transaction processing there's probably a number of sub modules.

**Nathan Carver**   10:05  
Transaction processing. Mm-hmm.

**Val Levitan**   10:18  
But the entire processing, I'm I'm scared of taking on the the processing part of it right now upon ourselves. It's just we are going to be extremely overwhelmed.  
I I just don't think that JVL has internal whereabouts or internal knowledge or internal expertise of handling the transactional part.

**Pavel Frolov**   10:43  
OK.

**Nathan Carver**   10:44  
Correct.

**Val Levitan**   10:45  
I mean, I mean in theory, in theory, yeah, I mean, you know, debit this, credit that, we can probably comprehend this, but it comes with so many intricate industry.  
Yeah, specific. I I don't think you should be a.

**Nathan Carver**   11:02  
There's, yeah.  
It's industry knowledge that the people just don't have experience with yet.

**Val Levitan**   11:12  
And I'm sure that today in North America, there are companies that exist that, you know, do only that part of the business, just do the processing.

**Nathan Carver**   11:25  
So the components we have is income processing the gift cards, so JBL just handling the communication and then a third party would process the transaction of taking money from the customer's account.

**Pavel Frolov**   11:30  
Yes.

**Nathan Carver**   11:41  
That's the kind of the critical piece that we're missing.  
So if if it was speed to market, then I think purchasing a SAS right, having another company process that is the quickest path.  
And then a decision of whether you want to build up this the capabilities in house to to build your own system and manage it or if.  
Outsourcing that is is profitable enough and there's no need to bring it in house.

**Val Levitan**   12:16  
Yeah, yeah, I would. You're saying let's subscribe to this service for now and see if we want to design it.

**Nathan Carver**   12:26  
Right, because it gives us exposure to the market and to the industry. It gives us, we start to learn and mitigates the risk by having, right. We're paying another company to take on the risk. So just figure out what that liability is with them.  
I think that makes sense to me. It's gonna be that's a lot of complexity if we want to get it out to market quickly for the in-house team to to scale up and and build it.  
I think long term if we want to bring the skill in house is contract a specialist to come in so the internal team learns from that specialist.  
Um, so they build it up together. That's much more long term plan.

**Juan Martinez**   13:14  
OK.

**Val Levitan**   13:16  
Yeah, I agree. So as we.  
Build or visualize the building blocks of the architecture of the entire system. Let's single this module out and get it serviced by somebody else.  
So that means we're going to have to get an API from this third party provider, etcetera.

**Nathan Carver**   13:49  
Correct.

**Val Levitan**   13:51  
It's a much safer.  
Much safer Rd.

**Pavel Frolov**   13:55  
She.

**Val Levitan**   13:59  
Or remove a major risk associated with.  
Not knowing the transactional part of the business.  
And and then as a second step, yeah, let's hire.

**Nathan Carver**   14:10  
OK.

**Val Levitan**   14:18  
A knowledgeable company that can.  
Help us out with this.

**Juan Martinez**   14:27  
Val, do in the interest of speed and time, should I just reach out to the normal casino industry suppliers that that do this technology for most of the casinos in the US today just to gather some data? I think that would be helpful for me to.  
Just leverage some of my connections and at least get some information from the the top two or three companies that do this for the casinos today.

**Val Levitan**   14:58  
Look, these companies are looking for business and they're usually very aggressive. I don't want to give up this intelligence of what we're doing and where we're going with this because I don't want to create a casino born competitor.  
Story depends how you're going to discuss it and what you're going to tell them. But and I also don't think that we need it because John from income pointed us to one or two companies that specialize in the processing business.  
And they're already in this market, they're already in this business. I think it just makes sense to deal with them and they already know income and they already process payments through income.

**Juan Martinez**   15:44  
Which company though?

**Pavel Frolov**   15:46  
OK.

**Val Levitan**   15:48  
Um, I can look at.

**Juan Martinez**   15:50  
I apologize, but I I miss that.

**Val Levitan**   15:53  
I I I made a picture of it. One second. Let me uh, let me go into my.

**Juan Martinez**   15:58  
You don't mean that whole sung kiosk?

**Pavel Frolov**   16:00  
Yeah.

**Val Levitan**   16:01  
No, I don't mean that.

**Juan Martinez**   16:03  
OK.

**Val Levitan**   16:06  
Give me a second, please. I'll tell you who it is exactly.

**Pavel Frolov**   16:40  
Correct me if I if I'm wrong, this processor transaction processor company just a controller controlling center, but not the proxy between our communication to income.  
But visibility to block POS device in case when we have some concerns about, yeah, about fraud.

**Juan Martinez**   17:13  
Brog.

**Val Levitan**   17:17  
I think blocking the POS device is up to us.

**Pavel Frolov**   17:23  
Yes, but how can we understand? We can request some API from third party. They go, they analyze each day or probably each minute of transactions and.

**Val Levitan**   17:38  
So, so just to let let me go back and answer one's question. In the presentation on the board, John highlighted the following companies, he says RWJ, Lunix Telecom.

**Pavel Frolov**   17:40  
Yes.  
OK.  
Yes.  
OK.

**Val Levitan**   17:53  
And in law.  
spelled with a Y.

**Juan Martinez**   17:57  
Yes, yes, yeah, those listed as resellers.

**Val Levitan**   17:59  
And.  
Yes, they are, but the RWJ or Lunex or in law specialize in.  
Specifically processing transactions and they actually offer their services to third party or I think one of them does it for another. I just have to get back to.

**Pavel Frolov**   18:17  
Thank you.

**Juan Martinez**   18:28  
Sure.

**Val Levitan**   18:30  
My transcript and find out what John.  
Which company John from Incom referred to? It was either RWJ or Lunex Telecom or Inlaw, one of those three, and they offered their services to third party.

**Juan Martinez**   18:54  
OK, yeah, it's probably not gonna be Lunix because I do recall him saying that they have been reported for bad customer service.

**Val Levitan**   19:03  
That that customer service, yes, I I we're talking about two services, front service, yes, but I think one of these three companies have a processing segment.

**Juan Martinez**   19:10  
Sure.

**Pavel Frolov**   19:19  
Goodbye.

**Val Levitan**   19:19  
That they offer to a third party at a fee. I I gotta get back to my transcript. I will.

**Juan Martinez**   19:26  
Understood.

**Val Levitan**   19:32  
Also, I think that if we highlight our concern of not being able to design proper transactional module to John, I think he will help us find a solution.

**Nathan Carver**   19:47  
Mhm.

**Juan Martinez**   19:48  
OK.

**Nathan Carver**   19:50  
Yeah, I agree. I'm sure he'll have contacts.

**Pavel Frolov**   20:00  
So as I understand the key point here for GVL not to make manual everyday validation of of all transactions with all the operators and all the locations.

**Val Levitan**   20:15  
Yeah, the key point is not to have manual reconciliation at all, but that's point \#1. I'm making a a super point, another point above all of this.

**Pavel Frolov**   20:15  
This is a key point.  
Mhm.

**Val Levitan**   20:30  
We need to have an ability to transact in real time on the street.

**Pavel Frolov**   20:31  
OK.

**Val Levitan**   20:39  
The street business versus let's say 711 business are different businesses.  
And when we deal with an operator, operator is a it's it's very hard to take possession of his business or enforce something or street business is different. So in the street business it's important to validate and swipe somebody's account.

**Pavel Frolov**   20:54  
OK.

**Val Levitan**   21:06  
Faster than you apply credit on the credit card.  
And because you're almost applying credit on the credit card or debit card instantaneously, although the you could reverse a transaction, but you want to swipe the master's account.  
For that value instantaneously.

**Pavel Frolov**   21:34  
So the answer to my first question will be we are looking for proxy proxy company to validate all the transaction before we transfer money to income card.

**Nathan Carver**   21:46  
Um.

**Val Levitan**   21:47  
Ideally.

**Pavel Frolov**   21:48  
It.

**Nathan Carver**   21:49  
Yeah, I think the flow would be.

**Val Levitan**   21:50  
Yeah.

**Pavel Frolov**   21:50  
If it possible in the real time, yes.

**Val Levitan**   21:52  
Or for that proxy to take risk on.  
Dealing with collecting money on their own. If the proxy says don't worry, it doesn't have to be in real time, I'll collect the money. God bless you, go out and collect the money as long as it's not me.

**Pavel Frolov**   22:16  
Yeah.

**Val Levitan**   22:16  
And there are some operators that you could establish a certain credit line with them and say, look, we will continue processing your transactions up to let's say $100,000 a day, but when it reaches $100,000 a day, we need to swipe your account.  
While ensuring that the $100,000 comes in or we're shutting, shutting off all your services. There's another dilemma here if an operator has only one location with you and you're shutting all the services.  
That's, let's say, 100 locations. That's a big damage to an operator, and an operator will immediately find a solution to satisfy you financially. But if you only have one location with an operator and it's a mediocre location.  
And and and the operator doesn't really care. OK, so you shut down his location. OK, So what? How much of A damage is it? His other 20 locations are still making money and.  
You know, let's sit down, talk, let's find a solution. You're getting into incredible difficulty.  
So I would rather have a higher risk, but with an operator who's got 100 locations that I could say, listen, you defaulted on one transaction, I'm shutting down 100 locations and it seizes all of his operation then.  
With some micro oerator.  
So yes, the as you call them a proxy processing company right now I think is a good idea for us. Either they process in real time or we don't care how they process as long as they take the risk of collecting upon themselves.

**Pavel Frolov**   23:58  
OK.  
Mm.

**Juan Martinez**   24:17  
But.

**Val Levitan**   24:17  
At least for now, until we learn the ropes and until we're comfortable and we could, you know, sufficiently implement our system, not under stress, and we can understand all the weak points and the issues with transactions. Let somebody else take a risk, even if we don't make money.

**Nathan Carver**   24:19  
Mm.

**Val Levitan**   24:37  
And at least we're not losing money on it.

**Nathan Carver**   24:39  
Correct.  
I think the way this looks in our flow is a customer comes, they redeem a $50 ticket. We authorize, we pre-authorize the gift card for the 50 \-, $4.00 service fees.  
So we authorized the gift card for our pre-authorized gift card for $46. Then we send a message to this transaction processing service to deduct $50 or transfer $50 from the customer to JDL.  
If they say yes, success money transferred, then we activate the gift card. If that service says money is not transferred, then we cancel the activation and.  
Deactivate the device or whatever we need to do at that point.

**Val Levitan**   25:31  
I think this problem I'm.

**Nathan Carver**   25:31  
Thank you, pinpoints. Sorry, go ahead.

**Val Levitan**   25:36  
Sorry, you didn't finish and I I didn't realize you didn't.

**Nathan Carver**   25:39  
I think it for JVL that I think we can very much pinpoint a very precise how we interact with that transaction processing that really simplifies our development workflow and reduces a lot of risk for us.

**Val Levitan**   26:00  
Yes, and and also defines our server capability a little more clear.

**Nathan Carver**   26:10  
Correct.

**Pavel Frolov**   26:19  
At least right now, when we think about all the procedure to activate card, we can add books to third party service. We don't know exactly what will be this.

**Nathan Carver**   26:31  
Mhm.

**Pavel Frolov**   26:36  
Service, but this API should provide some information for us either to provide this transaction further or cancel the transaction. That's all.

**Val Levitan**   26:54  
There's an interesting point here that in the case of the JVL flex redemption center, it amplifies the problem even further.  
Because now you're dispensing live cash.  
So you cannot reverse the transaction. The cash has left the center.

**Nathan Carver**   27:24  
Mhm.

**Juan Martinez**   27:25  
Thank you.

**Val Levitan**   27:25  
It the transaction is irreversible.

**Juan Martinez**   27:30  
Yeah, I mean we we need to shift the liability at the point of card creation to that third party. That's the only way to that to resolve it where they would owe us cash reimbursement for whatever.  
Illegal transaction was done with that card that started the journey, I guess.

**Val Levitan**   27:56  
I almost feel like we have to get the.  
Uh, not sure what the proper name for it. Uh, something like a location agreement.  
Between, first of all, we have to have two agreements, competitors agreements. One is the transactional agreement.  
You know between the clearing house and the location.  
That would be, let's say between keep forgetting the name of these companies between let's say RWJ and the location or Lunix and allocation. So we need a copy of that agreement.  
Somehow.  
And step \#2, we need to look at the location agreement between an ATM provider and a location.  
Anybody has an idea of how to get that?

**Juan Martinez**   29:09  
Well, for reference, I can certainly get the casino equivalent of those. We would have signed a contract with every or NRT that just as a starting point. I'll get with Felipe to see if there's a.  
A trusted master or somebody else that could facilitate that those documents to us. And I mean, I don't know if John would be willing to share those with us from income, but John as well.

**Val Levitan**   29:39  
So as a point of undertaking, I cannot delegate this to anybody else except to you one. So can you please assume this undertaken upon yourself?

**Juan Martinez**   29:46  
Yep.  
Absolutely.

**Val Levitan**   29:55  
OK. I think Nathan, your undertaking should be to speak to John about this processing module. Try to sink your teeth into that.  
Because we need more intelligence or not.

**Nathan Carver**   30:14  
Sounds good.

**Val Levitan**   30:15  
And Nathan, you should start working with Pavel on the overall architecture, at least in block diagram of how the whole system will look like now that we have an established array of our products that we want to introduce the transactional products.  
You should start discussing a block diagram architecture.

**Nathan Carver**   30:38  
OK.

**Pavel Frolov**   30:39  
Hmm.

**Val Levitan**   30:39  
When I come back, I would like to sink my teeth into that.

**Nathan Carver**   30:45  
OK, Yep, we can have that ready.

**Val Levitan**   30:48  
And Gennady and you and I, Gennady, we need to work. We should also one and Gennady and I, we should probably decide on whether we will have one tower.  
Single tower or we'll have two products as one is a dispensing tower.  
And the second one is a redemption center.

**Juan Martinez**   31:16  
Val, in your vision of the redemption center, if it's not at near the machines, how do you envision money going in?

**Pavel Frolov**   31:19  
OK.

**Val Levitan**   31:26  
You're you're exactly correct. Not only that it's need another important point, not only that it needs to be next to the machine or wedged between the machines, or exactly adjacent to the machine.  
Specifically using those adjectives, a machine should not have a bill acceptor in it.  
A bill acceptor must be removed, must be removed from a machine in order for this to work.  
All of the money, all of the circulation needs to initiate at the redemption center or we could call it transaction center, redemption center.

**Pavel Frolov**   32:13  
Thank you.

**Juan Martinez**   32:17  
Right.

**Val Levitan**   32:19  
But the point is that money in must go through the center in order for the center to accumulate the money. By center I mean the redemption center or the mini ATM, however we're going to call it, needs to accumulate the float in order to.  
Dispense money out because if there's no constant money in, it's it's like the hopper. Remember the old hoppers, coin hoppers.

**Juan Martinez**   32:48  
Sure, yeah, of course.

**Val Levitan**   32:50  
We had to have our field fill with initial fill and the hoppers were never emptied out. Remember there was a drop bucket underneath the machine, so any any overflow would go into the drop bucket and on and.

**Juan Martinez**   32:53  
Yes.  
Absolute.

**Val Levitan**   33:06  
And the drop team would only collect the drop bucket, but not the hoppers. Hoppers would constantly remain full unless you had an audit of some sort. They would never, they would never empty out the hoppers. It's the same thing instead of calling bill bill recycler initially when we were at cash.

**Juan Martinez**   33:16  
For big payout.

**Val Levitan**   33:26  
So designing this product, we called it. We called it Bill Hopper. This was the initial name for it, or at least code name for it.  
As we conceptualize the idea, we led the market with the billhopper. We actually model, model the recycling recycling cassette after a.

**Pavel Frolov**   33:48  
Yes.

**Val Levitan**   33:51  
Ending patent Japanese ending patent from a company called Maka.  
So the patent was dying within the the remaining three years and we started our design based on that recycling hopper and then their patent, they called it a recycling cassette. So we adopted the name recycling cassette.  
Hence moved away from a bill hopper to recycler.

**Juan Martinez**   34:24  
Still.

**Val Levitan**   34:24  
So back full, full circle, back to your .1, it must be wedged between the machines and a machine must not have a build validator in it. Just I just wanted to make a full circle and conclude my conversation.

**Genadi Peari**   34:26  
Sorry.

**Juan Martinez**   34:43  
Sure.

**Val Levitan**   34:44  
With what you what you had started.

**Genadi Peari**   34:46  
In case the redemption center serving two machines, is it? Is it possible to work without redeeming the card?

**Juan Martinez**   34:46  
Sure.

**Val Levitan**   34:53  
Right.  
Yes.

**Genadi Peari**   35:00  
Can you go through the how how it works?

**Val Levitan**   35:06  
Well, it could work a couple of ways. We could have a printer built into a redemption center.  
And so you issue a ticket.  
QR code. I'm specifically calling it QR code. It could be a barcode, but I'm separating the reason I'm calling it QR codes. So you treat it as a temporary wallet.  
And then having this QR code you could move around the machines.

**Juan Martinez**   35:32  
Right.

**Val Levitan**   35:39  
And then presented to a redemption center and it will go through a cycle.  
So that's that's scenario \#1. Scenario \#2, you could insert a bill and you could put the money on the card, like actually physically pair it on the card.  
The initial money, I'll come back. There are concerns with it.

**Pavel Frolov**   36:09  
S.

**Val Levitan**   36:10  
And then use this card barcode card to scan it on the machine.  
And use it as your temporary wallet.  
The problem, the concern that I see with it is that it's open to.  
Well, potentially could be open to.  
Money laundering scheme like you you let let's say you fill $1000 with it and and you go and use it somewhere else so.  
And and unless you have a value on the on the card, you cannot play with it. So it's a little bit uncomfortable. I I I don't like that scenario. So the the the medium, the carrying medium should be.

**Juan Martinez**   37:00  
Yeah.

**Val Levitan**   37:06  
A printed ticket. The problem with this I know where one's head is going now. Well, you have to refill paper.  
It's uncomfortable, so it's a it's a it's an issue.

**Genadi Peari**   37:18  
It's better than refill the cards.

**Val Levitan**   37:23  
True.

**Juan Martinez**   37:24  
Yeah.

**Genadi Peari**   37:25  
My point is if we want to put and the printer and the dispenser and the bill recycler, it's become a robust unit close to flex to pay station.

**Val Levitan**   37:26  
I.

**Juan Martinez**   37:27  
Yeah.

**Val Levitan**   37:39  
It's it.

**Genadi Peari**   37:42  
It's almost the PlayStation.

**Val Levitan**   37:44  
Yeah.  
Yeah.  
Look, we we could, we could do it primitively as as old time. We could put a slightly larger screen, wedge a device between the two machines.

**Genadi Peari**   37:49  
Um.

**Pavel Frolov**   37:53  
Yes.

**Val Levitan**   38:04  
And to say credit machine on the left or credit machine on the right.  
It's uh it.  
You know, I've seen systems like this. It's.

**Genadi Peari**   38:15  
Older fashion.

**Val Levitan**   38:16  
Yeah.  
Old fashioned, yeah, the.

**Juan Martinez**   38:18  
Yeah, but I I I think that you know that Tito, the word Tito is the buzz word in Georgia these days. A lot of systems are already using it. I think that you know going that the the virtual ticket where we've turned Flex pay into Flex Tower is.  
Probably the safer solution where we're creating that virtual wallet on the ticket and they can move from machine to machine and you know, start their gaming session at the tower or redemption center and end it there as well.

**Val Levitan**   38:57  
Yes, and and after all, your location has one printer for two machines versus 2 printers for two machines, one recycler versus two bill acceptors.

**Pavel Frolov**   38:57  
Looks good.

**Val Levitan**   39:13  
So the cost is actually offsets to be honest with you. And as Juan said, the the upgrade associated with a Tito operation is preserved. So now the operator says, look, I got my Tito operation.

**Juan Martinez**   39:17  
Yeah.

**Pavel Frolov**   39:19  
Yeah.

**Val Levitan**   39:32  
Tito upgrade. I got this extra security. I have my server installed in the location.  
And it's costing me roughly the same amount of money.

**Juan Martinez**   39:46  
So I guess Gennady, what what we've just described is modifying Flexpay to now include a bill recycler at the at the highest level.

**Pavel Frolov**   39:58  
You said exactly exactly that, I think.

**Val Levitan**   39:59  
Well.

**Juan Martinez**   40:02  
Yes.

**Genadi Peari**   40:05  
Yes and no.

**Pavel Frolov**   40:17  
OK.

**Juan Martinez**   40:18  
Yes, yes.

**Pavel Frolov**   40:18  
OK.

**Val Levitan**   40:18  
Exemption number.

**Pavel Frolov**   40:19  
Yes.

**Genadi Peari**   40:22  
It it's not what John was talking about, right? The redemption center, the idea is exactly what Wal said. Put it beside the machine, between the machines, not somewhere at the entry.

**Val Levitan**   40:32  
So no, no. But what these guys are saying, instead of having a flex space sitting somewhere outside in the corner, you're now bringing flex pay, wedging it between the two machines, changing the shape of it, but functionality remains almost.

**Pavel Frolov**   40:36  
She.

**Val Levitan**   40:52  
The same. I understand what these guys are saying, but it doesn't matter. We're all saying the same thing here.

**Juan Martinez**   40:53  
Right and.

**Genadi Peari**   40:57  
And Flexpay cannot accommodate bill recycle today.

**Juan Martinez**   40:57  
Right, but but from a from a.  
Well, I use Flex Pay the name, not the physical device we know today. It needs to be a new one. But remember that in very in most cases, there is no such thing as the space between the machines. The machines are right next to each other. They're in.

**Val Levitan**   41:07  
Yeah.

**Pavel Frolov**   41:20  
Yes.

**Juan Martinez**   41:22  
Already a tight corner, but there's always room for a redemption center slash Flexpay device close to the machine. So we need to think about the practicality that there is no space in the machines, especially for something that's going to be.  
At least 20 inches wide to accommodate all these peripherals. That's almost the width of a machine.

**Genadi Peari**   41:47  
I I think we.

**Val Levitan**   41:49  
No, no, no, no. Juan, you're mistaken. We can fit in a critical. We can for sure fit everything into 8 to 10 inches.

**Pavel Frolov**   42:01  
So.  
So.

**Val Levitan**   42:04  
There's no questions about it.

**Juan Martinez**   42:06  
So now it's going to be a an insanely tall unit.

**Val Levitan**   42:10  
No, it might be slightly deeper by probably.  
Maximum 4 inches deeper, but the depth you just you don't see the depth.

**Juan Martinez**   42:22  
Yeah.

**Genadi Peari**   42:28  
It should be taller, well.  
But uh, we have tall machine is tall.

**Juan Martinez**   42:31  
Yeah.

**Val Levitan**   42:32  
No, no, guys, hold on a second. The the height has never been an issue because flex tower was designed to be mounted on a pedestal. So if you take the total height of the tower plus the.

**Genadi Peari**   42:45  
Step.

**Pavel Frolov**   42:49  
OK.

**Val Levitan**   42:51  
Pedestal, the overall height will remain the same.

**Juan Martinez**   42:57  
No, but remember that the current design of Flex Tower does not have a bill recycler in it.

**Val Levitan**   43:04  
Right. So by putting bill recycler, you will remain at the same height. What you really need to add is the depth.  
We we measured it out on Ginari's desk. So you know, I can tell you for sure we can.

**Juan Martinez**   43:25  
Yeah. So the recycler would go where the pedestal is on the tower today as an example.

**Pavel Frolov**   43:32  
So.

**Val Levitan**   43:32  
No, it will go above a card dispenser. The card dispenser has an L shape. It's an L-shaped device, so you mount it and and the.  
Recycler is usually the the dispensing. The drop cassette is at the bottom, so it's usually 1000 bill cassette at the bottom, so it's a skinny bottom.

**Juan Martinez**   44:03  
Right.

**Val Levitan**   44:03  
It's like A1 legged fat lady and on top you have these bunch of cassettes, so if you elevate.  
The dispensing device hovering above the L shape.  
Card dispenser.  
Because the card dispenser, you don't need a tall card dispenser anymore. You need 250 cards because most people will not take cards.  
So you could elevate or levitate the.  
Uh.  
The bill recycler above the card dispensing unit.

**Juan Martinez**   44:52  
Right, plus plus the ticket printer.

**Genadi Peari**   44:57  
Ticket is very low. Ticket printer is very low.

**Val Levitan**   45:00  
It's a.  
It's a very narrow device.

**Genadi Peari**   45:03  
I I see recycler at the bottom with the bezel on the top because the recycler all the cassettes going down right? So if you position it at the bottom you will have the bezel right on the right height, comfortable height above this.  
Dispenser with the bezel close to the bezel of the dispense recycler because it's not very high now, so it's also will be fitting well.

**Juan Martinez**   45:39  
I I would warn that though, if we actually envision this going between the machines, then the tower must be front serviceable, meaning in order, everything has to pull forward, OK?

**Genadi Peari**   45:39  
And and.  
Yeah.  
Yeah, yes, yes, front service and the 9 inches width.  
Big screen, 8 inch screen.  
Devices one above each other. We just need to spec more how many denominations really we need because we won't be able to add the height after all, right?

**Juan Martinez**   46:18  
Sure, sure.

**Genadi Peari**   46:19  
So.

**Val Levitan**   46:19  
You you cannot recycle or you cannot go above 4 denominations. It has to be 1510 and 20 and then you you must allocate 4 cassettes. You allocate two or three to the 20th and one or two to the 10th.

**Juan Martinez**   46:27  
Right.

**Genadi Peari**   46:40  
4 drums, 2 cassettes.

**Val Levitan**   46:44  
A drum is a recycling cassette.

**Juan Martinez**   46:50  
It's the four cassettes.

**Val Levitan**   46:52  
O4 drums or 4 cassettes is the same.  
So each drum or a cassette, whatever you want to call it, is designated to a single denomination.  
So preferably you want to have four drums or call them cassettes, and you want to nominate them as 20/20/20/10.  
Because your main payout will be in 20s. Let's say if you're paying out $200, you'll dispense 1020s.  
But if the payout, let's say, is $50.00, you'll dispense two 20s and 110\.  
And if the payout is $55, you'll dispense 20/20/10 and you leave 5 on the card or on the ticket.

**Pavel Frolov**   47:53  
But how? How to behave in case of big winning higher than 1000?

**Val Levitan**   47:59  
If it's a jackpot, you always put it on the card.  
Jackpots, jackpots, even in a casino, will never be paid out in cash. A casino will write out a check or some other process. They will not give you cash.  
I mean, they'll give you a cash if it's $2500, but they're not going to give you $50,000 in cash.

**Nathan Carver**   48:19  
7\.

**Val Levitan**   48:28  
So jackpots is always a, you know, a separate issue.

**Genadi Peari**   48:36  
In in case of device as you expect now, I don't see any benefits to have additional product flex tower because from the point of price wise it's the same just.

**Val Levitan**   48:51  
I.

**Genadi Peari**   48:53  
Just piece of.

**Val Levitan**   48:54  
I do. I I do. I have a point because and here's my point because a redemption tower, the I'm only referring to enclosure right now and not cost. Don't think about cost. Think about the size.  
So the tower had two purposes. It was standing freestanding in the game room or counter mounted in the cage.  
Because the scenario could be mounted on the counter in the cage, customer facing, so the attendant never touches the card. So you have your POS which is wedged between.  
The.  
The RKS board and the printer. You have your POS, so you captured the signal from the RKS board.  
It shows the value. You say OK issue, issue a card.  
You print the ticket, you give the ticket to the customer as a receipt, or you put it in your cash register if you want. I I don't know what the process is and the card dispenses facing the customer.  
And so you need a little screen there where a customer says I agree, press OK and the card dispenses.  
So size wise you need a tiny device.  
So I think actually what we're saying is that the tower device gets a little bit smaller.  
Where a redemption center gets slightly larger, especially deeper.

**Genadi Peari**   51:00  
Right.

**Val Levitan**   51:01  
And maybe in maybe we put a larger screen in the redemption center just to beef it up so it becomes a little.  
More presence about it.

**Genadi Peari**   51:26  
Understood.

**Val Levitan**   51:28  
So that's that's my contemplation. I I mean, I also went through the same process. If it's the same enclosure, why do we need two different enclosures? Is it only a separation in the name only or is there separation from for form and fit perspective?  
And I'm.

**Genadi Peari**   51:48  
Different purposes, yeah.

**Val Levitan**   51:50  
Yeah, and I'm arriving to the point that it's probably more of a form fit differentiation rather than.  
It's not an aesthetic issue, it's a form fit issue.

**Genadi Peari**   52:05  
It also with different purposes in terms of tower doesn't have cache inside, doesn't need to be locked and secured.

**Val Levitan**   52:16  
Exactly.  
So a tower is a discard dispensing unit. There's nothing to secure, there's no value, and the redemption center now needs to be designed differently because it's going to be out of sight.  
From the attendant and a lot of crafty people will, you know, with a big screwdriver, will try to break into it.  
But you're probably using a different gauge of steel. You're probably using different locking mechanism. We probably need some sort of end switches signaling forceful entry or something.

**Pavel Frolov**   52:55  
3\.  
D.

**Genadi Peari**   53:09  
Yeah, we need locable cache for the cache, yeah.

**Juan Martinez**   53:20  
Just a quick question today, Flexpay uses a machine style CPU. Is the redemption center going to use the same or this is this new ARM based board you showed us Kanati?

**Genadi Peari**   53:37  
Yeah, it should be ARM based as soon we validated this platform.

**Val Levitan**   53:47  
It should be ARM based. We should also have a ping going between all of the devices. If any of the of the devices hang up or do not reply to a ping, we should go through.  
Probably some sort of a watchdog timer or we should be able to restart the device. If the ping didn't appear, we should trigger a service, so they have to be alarm procedures.

**Juan Martinez**   54:17  
Like keep alive.

**Val Levitan**   54:19  
We keep alive, yeah.  
Especially when it comes to a local server, if that hangs up for any reason, that's a major alarm. This needs to be fixed.  
I'm just curious whether with all the devices we should not have a server redundancy built in into the architecture.  
Because we have plenty of storage.  
Even if we have a server and now I'm overstepping my boundaries, you know I'm playing it playing engineering architect, which I shouldn't be, but I'm just curious whether why not to make server redundancy between all the CPUs that we.  
Have one allocation.

**Juan Martinez**   55:15  
Yeah, I agree. On our call yesterday with Incom, with Incom, they they made a point that you know to prevent that that handheld device, that packs unit that they supplied, you know the the brains of it are not in the device. So if the device gets stolen.  
Or walks out of the building. The processing engine is somewhere else and not inside the device, so agree with the local server to manage all this.

**Val Levitan**   55:48  
Well, same as our brain for processing brain should not be on on any of the local devices. We already spoke about it in terms of architecture that should be a cloud-based.

**Juan Martinez**   55:54  
Yeah.

**Val Levitan**   56:03  
Even even on the Tito side of it, we should move it offside.  
We should accept. We should accept zero trust policy.

**Juan Martinez**   56:12  
My my.  
Yeah, but so in the casino industry, the notion of Tito off-site has always been fearful because of latency. Now technology has changed, the casinos haven't, but there's, you know, there's always been a local Tito server so that you don't have to wait for your ticket to be.  
Be redeemed instantly. I don't know if that's been overcome or if we would need a much faster cloud connection to achieve that same experience. I mean, Pavel, that might be a question for you.

**Pavel Frolov**   56:49  
She.  
Mhm.  
Yeah, good question.

**Juan Martinez**   57:09  
Also, in theory, if we lose our Internet connection and we have a local Tito server, maybe it can issue up to \*\* number of tickets locally without that Internet connection.  
So we have time to reboot things or power to get restored at the location because they got hit by lightning. All these actual scenarios that can happen.

**Pavel Frolov**   57:44  
Yeah.

**Genadi Peari**   58:18  
Cloud server, it's a very, I mean it's it's not easy. I mean it's might be problematic.  
It's um.  
It's nice feature to sell but.

**Pavel Frolov**   58:37  
But it will reduce reliability.

**Juan Martinez**   58:40  
Yes, I agree.  
In these types of environments, yes.

**Genadi Peari**   58:46  
I'm not sure what's the advantage.

**Pavel Frolov**   58:47  
OK.  
To protect from stealing of pure ears.

**Genadi Peari**   58:59  
The OS not related to no if you can have server beside in the locked room beside the printer or.

**Juan Martinez**   59:09  
No, a properly managed cloud server is redundant. You know, think about Amazon, AWS type of setup. You know, it's backed up real time. It's moved around to different servers at different locations.  
It's certainly high availability, but if you lose Internet connection then you are down and that happens and and has happened. So it can go both ways, I mean.  
The larger companies are pitching that it's way more reliable because it it's it's not a physical box in one location, it's virtual in many locations and they can instantly spin up a copy of it if something happened to that primary one, which you can't do with a physical server.

**Pavel Frolov**   59:48  
Mhm.

**Juan Martinez**   59:58  
But again, I I still prefer physical with maybe a cloud backup, but a physical server given these types of of low technology locations in Georgia.

**Pavel Frolov**   1:00:11  
Yeah, I I also prefer to to have redemption server, let's say redemption server on the location, but with the ability to share functionality with different devices, for example if we have a tower.

**Juan Martinez**   1:00:22  
Yeah.

**Pavel Frolov**   1:00:31  
Power plus POS in case of problems with POS to switch to different device. This is good idea.

**Juan Martinez**   1:00:36  
Sure.

**Genadi Peari**   1:00:40  
No, no, but not to have a server on the POS.  
On the other devices, yes, but why on the POS?

**Pavel Frolov**   1:00:48  
Right now, as we discussed the first release of POS.  
We assumed.

**Genadi Peari**   1:00:56  
Yeah, but if you steal this, if you steal TOS, you have server in here on hand.

**Pavel Frolov**   1:01:01  
Yes.

**Juan Martinez**   1:01:09  
Yeah.

**Genadi Peari**   1:01:09  
So what? Why would you run run server on the?

**Pavel Frolov**   1:01:13  
Because it's set the the cheapest solution when we do not need any additional equipment except for POS plus current moto goose infrastructure and that's all.

**Juan Martinez**   1:01:14  
No, not on the field.

**Genadi Peari**   1:01:17  
Is it?  
Put the server, put the server separately.

**Juan Martinez**   1:01:27  
No, but I I thought we we definitely talked about a a separate server, Pavel.

**Genadi Peari**   1:01:35  
Yeah.

**Juan Martinez**   1:01:35  
Just so the POS can't be carried out of the building and it's a functional device. If you pull it out of the building, it won't work without that server.

**Pavel Frolov**   1:01:46  
Mm-hmm. So in any case, we are thinking about a separate server.

**Juan Martinez**   1:01:52  
Yes, I think so.

**Genadi Peari**   1:01:53  
POS is the cheapest way, right? But it has a server, but more sophisticated. If you have the tower for example, yes, you can migrate between, migrate between tower and the server. I mean as a backup, but.  
But not the POS.

**Pavel Frolov**   1:02:12  
OK.

**Genadi Peari**   1:02:14  
And another question about POS. We do not spare any wireless communication.  
Did we miss it or we don't want it? I mean.

**Juan Martinez**   1:02:28  
No, from a safety standpoint, I I think it should be a physical connection to that server.

**Genadi Peari**   1:02:35  
OK and compare and compare to all this.

**Nathan Carver**   1:02:36  
Yeah.

**Genadi Peari**   1:02:40  
What's their name?  
The whatever competitors use today, the $300.00 device.

**Juan Martinez**   1:02:56  
Over the packs, yes, yes.

**Genadi Peari**   1:02:57  
Fox.  
They do only wireless.

**Juan Martinez**   1:03:02  
Yeah, I mean, basically it's a cheap Android phone with a swiper on the side, which has Wi-Fi by design.

**Genadi Peari**   1:03:07  
Yeah, yeah, so.  
No, this is perfect for me in better.

**Juan Martinez**   1:03:13  
Yeah. And I think when we write up our sales brochure, we will say unlike your unsecured packs, which allows manual entry and has Wi-Fi, our device is better for these other reasons.

**Genadi Peari**   1:03:26  
OK, so we spec it as agreed. We put it on the table on the stands, the stationary stand which not easy to, I mean turn in facing customer if you need and this allows you to.  
Good service without any handheld hand handheld capability.

**Juan Martinez**   1:03:49  
Yes.

**Genadi Peari**   1:03:53  
OK.

**Pavel Frolov**   1:04:09  
Yes.

**Juan Martinez**   1:04:21  
Do we want to start, I think Nathan, defining the more simple devices such as the port and the SMIB now?

**Nathan Carver**   1:04:34  
Oh, go into the flex port discussion.

**Juan Martinez**   1:04:38  
Yeah, flex port and Smith, you know.

**Nathan Carver**   1:04:40  
Yeah.

**Juan Martinez**   1:04:43  
So just a a key difference between port and SMIB. The SMIB does not have any display on it. It sits inside the machine and it is enabling these older machines to connect to.

**Nathan Carver**   1:04:43  
Yeah, we can.

**Juan Martinez**   1:05:01  
Our our network per SE.  
Whereas Flexport does have the Flexport is is creating that virtual wallet, so it does have a display because the player has to accept a interact with the display to transfer their amounts.  
Uh, scan their tickets, so forth and so on.  
Oh.

**Pavel Frolov**   1:05:29  
Mhm.

**Nathan Carver**   1:05:31  
OK.

**Genadi Peari**   1:05:32  
SMIB connected over SAS.

**Pavel Frolov**   1:05:38  
Yes.

**Juan Martinez**   1:05:42  
We would, we would share, we would share the primary SAS with intralot like AY splitter.

**Genadi Peari**   1:05:42  
And then goes to server.

**Juan Martinez**   1:05:52  
That would be the ideal scenario. These machines may not have a secondary SAS port.  
Also, I guess your your question, Gennady, is can Smib just intercept the printer and bill acceptor pulses? Is that what your question's gonna be?

**Genadi Peari**   1:06:22  
No, it won't.

**Juan Martinez**   1:06:25  
So then it's definitely SAS.

**Genadi Peari**   1:06:32  
Yeah, my question was basically how do we share this?  
One port.

**Juan Martinez**   1:06:39  
Like AY splitter.

**Pavel Frolov**   1:06:42  
Initially we agreed that in case when a machine has only one serial port for SAS to use flex port, but if you have two SAS options then we can use SMIP.

**Juan Martinez**   1:07:01  
So in in the latest document that Val attached his transactional product portfolio, he the purpose of Smith is to enable machines with only one SAS port to connect.

**Pavel Frolov**   1:07:06  
Mhm.

**Genadi Peari**   1:07:17  
First time I hear it.

**Juan Martinez**   1:07:17  
So we.

**Nathan Carver**   1:07:20  
Yeah.  
Right, because it's the one SAS port is in use, so the second is needed to connect to chain it to the server right to flex.

**Genadi Peari**   1:07:28  
Um.  
I thought for the one one port we always use flex ports.

**Val Levitan**   1:07:31  
Sh.

**Genadi Peari**   1:07:39  
Well, was it the in your transcript you you posted you you use when the old machine was the one port only?

**Val Levitan**   1:07:50  
SMIP is SMIP is used for two ports.

**Genadi Peari**   1:07:50  
To enable it.

**Juan Martinez**   1:07:56  
OK, so we just need to modify \#5 in Val's last post.

**Genadi Peari**   1:08:00  
Yeah.

**Juan Martinez**   1:08:02  
Purpose enable machines with only one SAS port and it needs to be changed to two.

**Val Levitan**   1:08:09  
Sorry that I make a mistake.

**Juan Martinez**   1:08:13  
Like you could blame AI for that one.

**Val Levitan**   1:08:16  
I do. I blame AI for it.

**Pavel Frolov**   1:08:23  
OK.

**Val Levitan**   1:08:27  
Yes, I I do blame my eye.  
Let me edit this.  
Point \#5.  
Yeah, it changed.

**Juan Martinez**   1:09:01  
So.  
I guess let's say that the this new swipe card at the machine becomes extremely popular.  
This means that if we had previously deployed the SMIB solution in the location.  
Since SMID has no external player interaction device.  
We would have to convert it back to a port in order to have that card swipeability.  
Is that how we envision this?  
Or does Smib does have a card swiper only and no display?

**Val Levitan**   1:09:47  
Does not have a display.

**Juan Martinez**   1:09:50  
Yeah, we agreed on that one. Does it have a card, an optical scanner or card swiper ability?

**Genadi Peari**   1:10:00  
No, it just hidden inside the machine.

**Juan Martinez**   1:10:04  
OK, so then that so if if if the location decides they want to go to the card swipe option at the machine because it's become popular, we need to revert from SMIB to Flexport.

**Genadi Peari**   1:10:04  
Small box.

**Val Levitan**   1:10:21  
Yes, but not only that, if if you suddenly want to add the functionality to a machine that machine does not support, you need a front end device communicating to a player.

**Juan Martinez**   1:10:22  
Org.  
Correct.

**Val Levitan**   1:10:47  
The machine natively does not support it.

**Juan Martinez**   1:10:53  
Right. So does that mean?

**Val Levitan**   1:10:53  
So if you want a new functionality that is not supported by a machine, you need flex port.

**Juan Martinez**   1:11:03  
But we do we need Flexport? If we already installed the SMIB, can we just add a screen and or player tracking panel with a card reader and scanner to the SMIB?

**Val Levitan**   1:11:16  
You you can of course you remove the SMIP, you throw it away and you put port because port is expanded SMIP.

**Pavel Frolov**   1:11:23  
Sure.

**Juan Martinez**   1:11:26  
No, but port in by our own definition is not for a dual SAS machine.

**Val Levitan**   1:11:33  
Oh, it could be used for dual files. There's no issue.

**Juan Martinez**   1:11:36  
OK.

**Val Levitan**   1:11:38  
I mean, I don't see any issue using port with two SUS. What's the difference?

**Juan Martinez**   1:11:45  
No, no, you're right.

**Val Levitan**   1:11:47  
But Pavel, you fell asleep alone.

**Pavel Frolov**   1:11:48  
No, no. Actually right now flex port. When we say flex port, we means that we take pulses signals.  
But not the SA support actually. Probably the second version of Flexport can be introduced.  
To utilize SAS.

**Val Levitan**   1:12:16  
But but my understanding that the revised flex port included the second SAS connection.

**Juan Martinez**   1:12:16  
So.

**Pavel Frolov**   1:12:26  
Board yes, but software is not scheduled to support this port.

**Genadi Peari**   1:12:34  
But you have the software, you need to import it, right?

**Pavel Frolov**   1:12:40  
Uh.

**Val Levitan**   1:12:40  
OK, so we we need to expand the software capability on flex port to support the communication with the second SAS, second SAS on the machine.

**Pavel Frolov**   1:12:51  
Exactly.

**Genadi Peari**   1:12:55  
It will be easy because it's exactly the same architecture.

**Juan Martinez**   1:12:59  
It's but but when we say expand, isn't the software in theory on the SMIB and port identical or just enabling or disabling? No.

**Genadi Peari**   1:13:09  
And.

**Pavel Frolov**   1:13:10  
No, no, no. They use different CPUs, microcontrollers.

**Juan Martinez**   1:13:14  
OK, OK. OK.

**Genadi Peari**   1:13:16  
But same family. It's software is basically the same, same architecture.

**Pavel Frolov**   1:13:21  
Same architecture, but absolutely different software.

**Juan Martinez**   1:13:28  
OK.

**Pavel Frolov**   1:13:29  
Yeah, it it can be reusable some modules just to take implemented module and insert it into flex port, but not interchangeable.

**Juan Martinez**   1:13:44  
Understood.

**Genadi Peari**   1:13:50  
Not sure about it.

**Pavel Frolov**   1:13:52  
No, just ask uh for Evgenia.

**Genadi Peari**   1:13:55  
Because there was no reason to put a different MCU just to save $1.00 maybe would be to use better to use the same software.

**Pavel Frolov**   1:14:12  
For me, yes, it's better to use one CPU, one family with with exactly the same peripheral. Yeah, just ask him.

**Genadi Peari**   1:14:19  
Oh, I'll ask him.

**Juan Martinez**   1:14:23  
Yeah, yeah. I mean, I don't, I don't. I haven't physically seen the SMIB. So if we're not past the point of no return, shouldn't it be the same software as as the new Flexport 2?

**Val Levitan**   1:14:38  
But keep in mind that we want Smith extremely inexpensive.

**Juan Martinez**   1:14:43  
Right. That was gonna be my next question, as long as it doesn't cross that 10 or $20 cost.

**Pavel Frolov**   1:14:50  
He.

**Val Levitan**   1:14:52  
No, it has to be a single digit. Like it has to be a hundred dollars. It cannot be 20\.

**Juan Martinez**   1:14:53  
I don't. I don't know how that's possible, Val. My, my this pet. This pet cost more than that.

**Pavel Frolov**   1:14:57  
Yeah.

**Val Levitan**   1:15:00  
For sure.  
No, no, no, no, no, no.  
No, no, it has to be a single digit thing.

**Genadi Peari**   1:15:11  
Two coffee or three coffee?

**Val Levitan**   1:15:13  
Two coffee. Well, two coffee. Two coffee.

**Juan Martinez**   1:15:14  
Yeah.  
Office.  
That sounds that sounds like 2 resistors and a wire, but I'm I'm not I'm that's magic, Nadi. I'll I'll leave you to it.

**Val Levitan**   1:15:27  
No, no, two coffee. You know, stick with two coffee.

**Juan Martinez**   1:15:29  
OK.

**Pavel Frolov**   1:15:29  
Yes.

**Val Levitan**   1:15:32  
Two coffees or three tea cups?

**Juan Martinez**   1:15:36  
Yeah.

**Pavel Frolov**   1:15:40  
Mhm.

**Val Levitan**   1:15:40  
But Nathan is thinking to himself, what the hell are these people going with this?

**Nathan Carver**   1:15:44  
Yeah.

**Juan Martinez**   1:15:44  
OK.

**Nathan Carver**   1:15:46  
Off the chain.

**Pavel Frolov**   1:15:52  
Good.

**Val Levitan**   1:15:52  
OK.  
Those are good comments. I appreciate it. Thank you.  
When I was away, was there anything worthwhile for me to understand? Any any particulars?

**Juan Martinez**   1:16:11  
No, we just shifted to addressing the the smaller items which are the the SMIB in the port in the grand scheme of things, so.

**Genadi Peari**   1:16:18  
We spoke about the POS capability. We I asked if we thinking about wireless communication for the for the POS. One answer definitely not. We want to position the wired.

**Juan Martinez**   1:16:23  
Mhm.

**Genadi Peari**   1:16:34  
Save. Um.  
Installation and also we were concerned about the server.

**Pavel Frolov**   1:16:43  
Server position of the server. Can we inject?

**Genadi Peari**   1:16:48  
And we don't want to have server on the POS.

**Pavel Frolov**   1:16:51  
And we inject a server application within POS to have the cheapest solution for motor goods locations or not, or we still need two separate devices.

**Val Levitan**   1:17:04  
OK. What was the decision on that?

**Genadi Peari**   1:17:08  
Not to run server on the POS.

**Juan Martinez**   1:17:08  
So.

**Nathan Carver**   1:17:11  
So two separate devices.

**Juan Martinez**   1:17:14  
Yes.

**Nathan Carver**   1:17:15  
Mhm.

**Val Levitan**   1:17:17  
And so if we label something a server on the location, this will be a major target of attack.  
Either vandalism or theft or attack. So we got to make sure that there is no sensitive data sitting on that server.  
And if it is, it's very temporary and it's it. It disappears if there's no ping.

**Juan Martinez**   1:17:57  
Well, I mean that.

**Val Levitan**   1:17:58  
So basically you don't write anything into non volatile memory.  
And if there's no pain, then.

**Nathan Carver**   1:18:08  
Yeah, it can still, even though we call it a server on the site, it can still rely heavily on remote processing. So in the conceptual JBL control server, right, we can still defer data storage, processing, whatever as much as we can.  
Offsite.

**Val Levitan**   1:18:30  
So then we adding to adding to our.  
Naming product naming offsite server.  
I I don't know how you want to call it processing server outside or offsite JVL processing server.

**Juan Martinez**   1:18:46  
Oh.

**Nathan Carver**   1:18:49  
Yeah, we.  
I started referencing it as JVL control server when we were in reference to Flex POS and that's the conceptual JVL server in the cloud that Flex POS will communicate with so.  
But yes, that's the offsite server is what that would be.

**Juan Martinez**   1:19:09  
And.  
On on Val's sheet number six, there's a flex server where this is all in one the same thing. We can call this also the JVL control server, correct?

**Nathan Carver**   1:19:27  
Number six. OK, yeah. Is flex server, is that the that's not the physical device that is a.  
Software server I guess.

**Juan Martinez**   1:19:38  
Yeah, but it I mean physical and local is preferred with some redundancy to the cloud.

**Nathan Carver**   1:19:48  
I see Flex server is the physical device OK.

**Juan Martinez**   1:19:59  
So and you.

**Nathan Carver**   1:19:59  
Yeah, we'll probably want a dictionary, a naming convention for onsite, offsite.

**Pavel Frolov**   1:19:59  
OK.

**Nathan Carver**   1:20:07  
Nay uh designation.

**Juan Martinez**   1:20:12  
But Nathan, you agree that we we can interchangeably call Flex Server the JBL control server?

**Nathan Carver**   1:20:12  
And.

**Pavel Frolov**   1:20:19  
I I think when when Nathan said a control server, he means our current server.

**Nathan Carver**   1:20:20  
Um.

**Pavel Frolov**   1:20:32  
That is responsible for leases to set up all the other devices and so on.

**Nathan Carver**   1:20:40  
Correct. It's in the cloud one.

**Juan Martinez**   1:20:42  
So you're saying CMS basically?

**Pavel Frolov**   1:20:43  
Quote.  
Yeah.

**Juan Martinez**   1:20:48  
OK.

**Pavel Frolov**   1:20:54  
So I think the key points the key.  
Key uh.  
Solution or decision to for us to make either we're going to introduce a cloud.  
Uh, cloud server to operate with Incom.  
Or to perform income communication from on-site server. I prefer a second way.

**Juan Martinez**   1:21:27  
On site server.

**Nathan Carver**   1:21:30  
The Incom's recommendation is that the processing is not done on site, but done by our.

**Pavel Frolov**   1:21:30  
Yes.

**Nathan Carver**   1:21:40  
Servers offsite.  
And the reason income.  
Suggest that is because if a customer has multiple storefronts.  
And Incomm has to disable their account. That would disable every store, not just a single store in which.  
There may be some type of fraud detection or issue.

**Juan Martinez**   1:22:14  
Just to clarify, so in the cloud based solution income can disable by unique site ID versus if it's local they cannot.

**Nathan Carver**   1:22:14  
And they had another go ahead.  
Um, so.  
Incomm identifies the the when a request comes in for the gift card and I have the I just got the API docs so I'm going to go through them again. But based on our conversation yesterday they they identify the request when it comes in.  
And so if.  
It's gonna be. So JVL is the identity, but the site ID identifies the site that's making the request. So it has to do with how in income can disable the ability.  
For an account to make a request to activate a gift card and they can't do pinpoint disabling. They can't disable, you know, a specific flex POS. We have to do the disabling of those individual devices.  
Because when Incom disables, they disable the entire account, so multiple stores would be disabled. Not just a single store is what not just a single site is what Incom was saying.  
So the recommendation was our cloud server would do the actual gift card activation, it'd just be a pass through. So the the Flex POS does not have any knowledge or ability to communicate directly with income. It sends the request to the cloud, the cloud.  
Communicates.  
With income, which gives us more precise control over the combination of pre-authorizing a gift card, calling the transaction processing service provider to transfer the money.  
Validating that that transfer is good and then finalizing the activation of the gift card. If all that's done in the cloud server, we have more far more precise control.  
Over all, you know all of those transactions, right? So the flex POS is just removed from that, from that whole thing.

**Pavel Frolov**   1:24:32  
So this is a dramatic change in our current architecture.

**Nathan Carver**   1:24:42  
Yeah, I think I agree. And that's probably a a Val. That's a point that following Incom's recommendation to do all the processing in the cloud is gonna be is a change in our architecture from the original approach that.  
The team had.

**Juan Martinez**   1:25:00  
And but we can't do a physical server to cloud handoff per say.  
Where we still have a physical server that that is then talking to the cloud? Is that less less of reengineering Pablo? I don't know.

**Pavel Frolov**   1:25:19  
No, in in any case we we will need to redo all the communication during the issuance card, not to perform direct communication to income, but.  
To make a proxy communication to our server. Doesn't matter where it's placed on physical server or on cloud server and then return response back to device flex POS or flex.  
Tower or any other device.

**Val Levitan**   1:25:59  
OK.

**Pavel Frolov**   1:26:03  
S.  
It require lots of rework for our team.

**Juan Martinez**   1:26:15  
Understood.

**Val Levitan**   1:26:16  
I am not willing to sacrifice security. This is this is paramount.

**Pavel Frolov**   1:26:39  
In this approach, I think probably we can remove.  
Server.  
Uh, inside server at all. Just to left cloud server for all communication, but that need to sync with our team discuss it.

**Juan Martinez**   1:27:23  
Nathan, I just forwarded you an invite from a call that we have today at 11 with Incom and maybe we can just fine tune this particular question again if you're able to join at 11, I don't know your schedule.

**Pavel Frolov**   1:27:32  
Stop.  
And with this, so with this approach we do need to introduce a cloud server application to be 24\.

**Nathan Carver**   1:27:39  
Oh, with you, OK.

**Pavel Frolov**   1:27:54  
Hours available.

**Nathan Carver**   1:28:02  
Yes.

**Pavel Frolov**   1:28:02  
Yeah, because I I think.

**Nathan Carver**   1:28:04  
Yep, we'll need an SLA on the availability of the of of the JVL control server.

**Pavel Frolov**   1:28:13  
8\.

**Nathan Carver**   1:28:16  
Yeah, there's more complexity now in the in the cloud side. The trade off is it's more secure because none of the hardware devices will have any.  
Any awareness of income, that income is even in the loop. So if these devices were compromised, there's no information on there for income. But you're right, Pavel, it's going to be more work in the heavy lifting on the cloud side.

**Pavel Frolov**   1:28:28  
Mhm.  
Yeah, it.  
Yes.  
It's it's solves a situation when the POS is stolen, has been stolen from the location. It will not work if you understand that this is not not on location device.

**Nathan Carver**   1:28:52  
Yeah.

**Val Levitan**   1:29:06  
It's the right approach.  
I recognize that it's more work to beef up the cloud side, but that's relatively marginal to the rest of the project.

**Pavel Frolov**   1:29:25  
Mhm.

**Juan Martinez**   1:29:32  
And also, doesn't this cloud solution allow us to push out software updates or enhancements?

**Pavel Frolov**   1:29:45  
The POS device or to other device?

**Juan Martinez**   1:29:47  
Yeah, yeah. Any device that we could envision requiring a software upgrade on our side, on our hardware.

**Pavel Frolov**   1:29:59  
Actually I think it's independent from cloud server because when when we say about cloud servers, this is an application for transactions is income in general, but all other functionality for example firmware update can be.  
Done from different server, not from this conduction server.  
Yes.

**Nathan Carver**   1:30:57  
So what's next in our?  
Product list? Is that everything for Flex Server? Is it Flex pay kiosk is next?  
Thanks.

**Pavel Frolov**   1:31:15  
Mhm.

**Juan Martinez**   1:31:21  
Yeah, and I I think Flex pay.  
Kiosk has morphed into the redemption center.  
Is that is that how we we left this conversation?

**Nathan Carver**   1:31:41  
Oh, yes. But we were discussing with John, right, as a as a larger scope of what this will be able to do becoming the redemption center. Yeah, I I believe you're right.

**Val Levitan**   1:31:51  
I think the redemption center is expanding in terms of functionality and capabilities in comparison to the former formerly formerly known tower.  
And in my view, tower is shrinking in terms of capabilities comparing to how I used to think about it.  
So Tower to me now is becoming a desktop.  
Dispensing enclosure.  
So it should probably be a little more elegant desktop mounted.  
Solely made out of plastic. There's no need for security of any sort. It's just to groom the desktop.  
So it doesn't have cards laying around.  
So it will have a screen for validation of operation, customer facing screen and convenient way to refill cards.

**Pavel Frolov**   1:33:05  
Oh.

**Val Levitan**   1:33:12  
Uh, don't need from service anymore.  
Probably some.  
Other way of refilling cards.  
Don't need to change the mechanism inside or don't need to service the mechanism inside. It has to be, you know, fully plastic enclosed.  
And it will always be sitting on one sort of a pedestal or a desktop or a counter.  
And the redemption service requires an expansion out of the concept of a tower.

**Pavel Frolov**   1:34:05  
S.

**Val Levitan**   1:34:08  
The only bounding.  
Restrain on it is the width.

**Pavel Frolov**   1:34:18  
She.

**Val Levitan**   1:34:19  
It cannot be more than, I don't know, 8 or 9 inches.  
The depth is relative depth of the machine itself.  
And the height is just the convenient level between the floor and let's say the normal height of individual.

**Pavel Frolov**   1:34:39  
Yeah.

**Val Levitan**   1:34:42  
And it must be front service.  
And it must be theft proofed or vandal proofed, I should say.  
Yeah, heavily, heavily vandal proof.

**Pavel Frolov**   1:35:15  
Yes.

**Juan Martinez**   1:35:19  
You mentioned theft proof and Pavel went and closed the window.

**Pavel Frolov**   1:35:27  
Yes, the rain started very, very big.

**Juan Martinez**   1:35:31  
Oh.

**Pavel Frolov**   1:35:40  
Yeah.  
Mm.

**Nathan Carver**   1:35:52  
All right. Are we at the last moving into skill pay card anything?  
To discuss room \#8.

**Val Levitan**   1:36:02  
No, nothing to discuss. I don't think so, but we should probably have it as a, you know, stand on its own as its own product nomination, just for clear clarity and taxonomy.

**Juan Martinez**   1:36:03  
I.

**Pavel Frolov**   1:36:10  
Yes.

**Nathan Carver**   1:36:19  
OK.

**Val Levitan**   1:36:21  
I think the next step we should probably apply or think about capabilities for each of those products as well as.  
The clearly defined personas. The personas are already defined by the way Nathan. It's in GitHub in the knowledge base under personas.

**Nathan Carver**   1:36:43  
Knowledge base in GitHub OK.

**Val Levitan**   1:36:46  
GitHub knowledge base personas. GitHub knowledge base personas.

**Nathan Carver**   1:36:52  
OK.

**Pavel Frolov**   1:36:55  
So right now I see number one priority to understand capabilities and architecture for cloud income transaction servers.

**Val Levitan**   1:37:11  
I think you should guys work on simultaneously on the architecture as well as use cases. I don't think you can define architecture without use cases.

**Pavel Frolov**   1:37:27  
Yes.

**Juan Martinez**   1:37:44  
Yeah, Nathan, let's kind of get together on use cases and and break these, you know, just one component at a time. So we understand all of its dependencies and and what we intended to do. I think that'll be helpful in in finalizing the use case.

**Nathan Carver**   1:38:02  
OK, it looks like we're putting these into the this knowledge base grouping of repositories is where we're going to keep.  
Uh, documentation.  
System level documentation.  
In the design and then the use cases, do we wanna put? I guess one we can figure that out, but we can start working with them in Confluence to collaborate on.

**Juan Martinez**   1:38:29  
Sure.

**Nathan Carver**   1:38:31  
And then move them into a repo at some point.  
OK.  
Um. I guess so far we have action items. Um.  
For myself, going to explore this processing module and I will connect with John to get his input in whatever industry advice he has there for the processing transaction processing module.  
Um.  
Pavel and I will start putting together the architecture documentation and for Val's review when he returns from vacation. And Juan, you were going to start exploring the the agreement on what was it, I believe the ATM.

**Juan Martinez**   1:39:22  
Yes.

**Nathan Carver**   1:39:24  
OK.

**Juan Martinez**   1:39:25  
Yeah, I I there's two large casino suppliers that do this today and I'll dig up old contracts I have from them just so we can understand at least how they deal with it, with the casinos and liability and all those legal language pages. Yeah, I'll have two from the large companies.

**Val Levitan**   1:39:44  
And same with Felipe, right? Felipe needs to go hunting for.

**Nathan Carver**   1:39:45  
OK.

**Juan Martinez**   1:39:48  
Correct.

**Val Levitan**   1:39:50  
Yeah, for the the local existing agreement between the location and keep forgetting the name of that terminal.

**Juan Martinez**   1:39:51  
Local.  
The packs, German.

**Val Levitan**   1:40:03  
PAX, yes, P-A-X, yeah, PAX.

**Pavel Frolov**   1:40:07  
And.

**Val Levitan**   1:40:08  
So that's our undertakings.

**Juan Martinez**   1:40:10  
Yep.  
Sure.

**Nathan Carver**   1:40:13  
OK.

**Val Levitan**   1:40:14  
And I think Gennadi, I think we're kind of.  
Decided on having two items, right? I think it makes sense, right?

**Genadi Peari**   1:40:23  
Yeah, I'll start the sketch it try to to see what we have.  
Special special like kind of design.

**Val Levitan**   1:40:36  
Spatial planning.

**Genadi Peari**   1:40:39  
Um.  
Do we keep a magnetic stripe reader on both devices?

**Val Levitan**   1:40:46  
Yes.  
For sure, 100%.  
And and the and the optical sensor.

**Genadi Peari**   1:40:54  
Yeah.  
Yeah, for sure. Yeah, optical for sure. Just.

**Val Levitan**   1:40:59  
Yeah, yeah, yeah, keep the strike, yeah. And with the same light inside, remember that we talked, that feature should always be there.  
The you need light controller for both devices.  
OK guys, I think we accomplished quite a bit. I'm quite happy with the meeting. A lot of good definitions. Nathan, when when the transcript is saved, please post the dot MD file in the chat. I I need it for for my for my knowledge base.

**Nathan Carver**   1:41:30  
Yep, we'll do that.

**Val Levitan**   1:41:34  
OK. Thank you all. And one, I'll see you in an hour.

**Pavel Frolov**   1:41:35  
Yes.  
Thank you. Bye.

**Val Levitan** stopped transcription