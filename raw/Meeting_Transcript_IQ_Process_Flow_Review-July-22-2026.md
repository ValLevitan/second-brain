# Raw Transcript — IQ Process flow update
**Date:** July 22, 2026, 5:00–5:59 PM Eastern
**Summary note:** [[Meeting_Notes_IQ_Process_Flow_Review-July-22-2026]]
---
WEBVTT

00:00:03.305 --> 00:00:15.265
<v Val Levitan>you, but I don't have time to really read into it. And it might be just easier for you to tell me what the verdict is. What did you decide on this?</v>

00:00:17.025 --> 00:00:19.745
<v Juan Martinez>Well, I think we're still in the decision process.</v>

00:00:20.025 --> 00:00:20.225
<v Andrei Klimovich>IC.</v>

00:00:21.105 --> 00:00:23.825
<v Val Levitan>Okay, which way are we leaning? I don't know.</v>

00:00:24.625 --> 00:00:31.905
<v Juan Martinez>Well, so are you familiar with the changes? The new process flow, Andrei, is Val aware of all this?</v>

00:00:32.705 --> 00:00:44.065
<v Andrei Klimovich>Yeah, well, I was part of this call and this summary is based on our today's call, Val, in the morning with Pavel.</v>

00:00:43.185 --> 00:00:45.825
<v Val Levitan>I was, I was the architect.</v>

00:00:46.465 --> 00:00:46.945
<v Andrei Klimovich>Yes.</v>

00:00:46.545 --> 00:00:47.105
<v Juan Martinez>Okay.</v>

00:00:50.705 --> 00:00:53.905
<v Juan Martinez>So let me just share my screen here to go through these things.</v>

00:00:56.065 --> 00:00:57.185
<v Juan Martinez>All right, so...</v>

00:00:58.545 --> 00:01:06.145
<v Juan Martinez>I just highlighted here in green and yellow just what I have questions or concerns with and what's okay. So yeah.</v>

00:01:02.865 --> 00:01:03.185
<v Andrei Klimovich>Yeah.</v>

00:01:05.505 --> 00:01:07.505
<v Andrei Klimovich>Yeah, it's so bright, sorry.</v>

00:01:07.985 --> 00:01:08.865
<v Juan Martinez>Ohh, sorry.</v>

00:01:09.345 --> 00:01:09.585
<v Andrei Klimovich>Okay.</v>

00:01:10.705 --> 00:01:11.985
<v Juan Martinez>My screen is so bright.</v>

00:01:11.505 --> 00:01:18.385
<v Andrei Klimovich>I, I don't know, yeah, and just my eyes hurt. OK, it's good.</v>

00:01:16.705 --> 00:01:36.345
<v Juan Martinez>Yes, so MG Oil always prints, IQ does not suppress or intercept the paper ticket. So that's something I wanted, so I'm okay with that. That makes sense. That way, procedurally, anything they do with that ticket, the location can continue to do.</v>

00:01:37.345 --> 00:01:51.905
<v Juan Martinez>Number 2, cashier offers a card, IQ validates it through the cloud, card is issued, done. If card fails, nothing happens. So.</v>

00:01:52.985 --> 00:01:53.265
<v Andrei Klimovich>It.</v>

00:01:52.985 --> 00:02:03.505
<v Juan Martinez>What does that mean if card fails? Because there's a momentary loss of internet communication and there's an outright IQ.</v>

00:01:57.425 --> 00:01:57.665
<v Andrei Klimovich>Big.</v>

00:02:05.185 --> 00:02:09.505
<v Val Levitan>Let me, let me say it differently: You go to a store.</v>

00:02:10.865 --> 00:02:21.265
<v Val Levitan>They hand you a handheld unit to validate your card, credit card, normal transaction. You bought groceries in the store, 50 bucks.</v>

00:02:18.065 --> 00:02:18.305
<v Juan Martinez>Right.</v>

00:02:22.145 --> 00:02:32.865
<v Val Levitan>They put in 50 bucks, they give you the handheld unit. You put in your card, you put in your code, nothing happens. It says transaction failed.</v>

00:02:33.945 --> 00:02:47.985
<v Val Levitan>You say, OK, no problems. You take your card, you put your card again, put your code in, transaction failed. You look at the cashier and you say, I don't know, transaction failed. So the cashier takes the unit, say, sorry, transaction failed.</v>

00:02:48.705 --> 00:02:52.625
<v Juan Martinez>Well, you forgot the part about maybe you should try another card.</v>

00:02:53.105 --> 00:02:55.985
<v Val Levitan>Fine, you try another card, transaction failed.</v>

00:02:56.385 --> 00:02:56.785
<v Juan Martinez>OK.</v>

00:02:57.905 --> 00:03:01.225
<v Val Levitan>You try something else, transaction failed.</v>

00:03:02.345 --> 00:03:03.825
<v Val Levitan>But that's it.</v>

00:03:05.265 --> 00:03:05.825
<v Juan Martinez>Okay.</v>

00:03:08.225 --> 00:03:09.345
<v Juan Martinez>So, understood that.</v>

00:03:08.385 --> 00:03:13.425
<v Val Levitan>And that's why, and that's why we reverted to point #1.</v>

00:03:15.425 --> 00:03:15.865
<v Juan Martinez>OK.</v>

00:03:17.025 --> 00:03:18.305
<v Juan Martinez>Uh, just to note you, though.</v>

00:03:17.265 --> 00:03:26.785
<v Val Levitan>You've got your ticket, location has got its process. It's working the way the location works all the time.</v>

00:03:27.905 --> 00:03:31.905
<v Val Levitan>Transaction failed does not impact your day-to-day work.</v>

00:03:32.705 --> 00:03:39.185
<v Juan Martinez>Okay, I do want to clarify this though. I don't believe the player gets the Mother Goose ticket.</v>

00:03:36.785 --> 00:03:36.985
<v Andrei Klimovich>Sorry.</v>

00:03:40.265 --> 00:03:41.105
<v Juan Martinez>You know that, that.</v>

00:03:40.385 --> 00:03:41.105
<v Andrei Klimovich>I agree.</v>

00:03:41.865 --> 00:03:48.785
<v Val Levitan>We, I didn't pay attention to it. I don't know whether they get a ticket or not. To me, it makes no difference.</v>

00:03:49.585 --> 00:03:50.225
<v Juan Martinez>Okay.</v>

00:03:51.505 --> 00:03:58.225
<v Val Levitan>Transaction failed, transaction failed. If transaction has gone through, transaction has gone through. The reason I...</v>

00:03:57.425 --> 00:04:02.145
<v Andrei Klimovich>Oh, by the way, while what about the term failed for this?</v>

00:04:03.345 --> 00:04:06.465
<v Andrei Klimovich>Not voided, we decided to abandon void.</v>

00:04:06.145 --> 00:04:07.985
<v Val Levitan>Fail, failed is a good term.</v>

00:04:08.785 --> 00:04:09.105
<v Andrei Klimovich>Okay.</v>

00:04:11.265 --> 00:04:11.425
<v Juan Martinez>Um...</v>

00:04:14.705 --> 00:04:23.585
<v Juan Martinez>But now we recorded the incoming cash out from the machine that we got from Mother Goose.</v>

00:04:22.265 --> 00:04:22.625
<v Val Levitan>No.</v>

00:04:23.745 --> 00:04:25.425
<v Val Levitan>No, no.</v>

00:04:25.905 --> 00:04:25.985
<v Andrei Klimovich>It.</v>

00:04:26.865 --> 00:04:31.105
<v Val Levitan>No, we don't record anything. The only thing that we record are those...</v>

00:04:33.185 --> 00:04:35.825
<v Val Levitan>transactions that we convert into a ticket.</v>

00:04:36.705 --> 00:04:39.345
<v Val Levitan>Sorry, sorry, we convert into a card.</v>

00:04:40.625 --> 00:04:45.345
<v Juan Martinez>Okay, but just to clarify, today we get the signal that we've intercepted from Mother Goose.</v>

00:04:45.505 --> 00:04:48.185
<v Val Levitan>We didn't intercept, we don't intercept.</v>

00:04:49.105 --> 00:04:49.745
<v Juan Martinez>Why not?</v>

00:04:52.065 --> 00:05:09.585
<v Val Levitan>Okay, well, again, we're back into that. Technically, we're intercept, but visually, practically, we don't. The ticket gets printed and we get on our screen, we get a transaction.</v>

00:05:11.585 --> 00:05:24.385
<v Val Levitan>transaction needs to say, go ahead, issue a card. Or I don't know what the verbiage exactly is. So unless you say, OK, issue a card and you press, nothing happens.</v>

00:05:25.665 --> 00:05:30.785
<v Juan Martinez>Right, but so we're saying we're momentarily receiving the intercepted data.</v>

00:05:32.865 --> 00:05:39.985
<v Val Levitan>I don't want to call it intercepted because it conveys the wrong message. I'm going to call it Way Mirror.</v>

00:05:37.865 --> 00:05:49.905
<v Juan Martinez>No, but I mean amongst us. Yeah, yeah, that's fair. We mirror the data and we don't instantly record that as a pending, still unopened transaction.</v>

00:05:51.665 --> 00:05:57.025
<v Val Levitan>We, we, what do you mean record it? We display it on the screen.</v>

00:05:57.625 --> 00:05:57.905
<v Juan Martinez>Right.</v>

00:05:58.705 --> 00:06:04.065
<v Val Levitan>And at this point, we have a choice to push the transaction to validation.</v>

00:06:05.505 --> 00:06:07.185
<v Juan Martinez>Right, so let's say...</v>

00:06:06.265 --> 00:06:21.825
<v Val Levitan>So it's a physical motion. So we say, OK, issue a card. Issue a card means transaction should not fail. If transaction does not fail and the card is issued, we record that transaction.</v>

00:06:25.665 --> 00:06:27.585
<v Val Levitan>Or, and only that transaction.</v>

00:06:28.705 --> 00:06:35.025
<v Val Levitan>So basically, we record those transactions to which we validate the card.</v>

00:06:36.945 --> 00:06:53.745
<v Juan Martinez>So if we have a touch screen failure on IQ, I mean, the message is sitting there, Mother Goose ticket number 25 for $50. Isn't it just going to sit there indefinitely until we hit yes or no?</v>

00:06:56.065 --> 00:07:03.185
<v Val Levitan>Well, if we have any sort of failure, it requires a change of a unit.</v>

00:07:04.465 --> 00:07:22.065
<v Val Levitan>So you could unplug this unit and plug a new one in. Let's say we're going to ship you an advanced replacement, or you have another unit sitting under your desk. You unpack it, you put it on your desk, you commission that unit,</v>

00:07:23.185 --> 00:07:30.625
<v Val Levitan>And that unit will have, will start from fresh. It will not have anything on it.</v>

00:07:31.425 --> 00:07:40.785
<v Val Levitan>Those transactions that were sitting on the screen and the unit was broken, they were never pushed to validate. They never issued a ticket. Nothing happened.</v>

00:07:43.185 --> 00:07:50.705
<v Val Levitan>It's exactly the same thing as you have fax on your desk and it's broken. A button is broken.</v>

00:07:56.545 --> 00:08:08.305
<v Juan Martinez>And is it? I mean, so what happened to us sending this information up to the cloud? Like, shouldn't it appear when you get a new IQ installed as a pending transaction?</v>

00:08:06.705 --> 00:08:07.185
<v Val Levitan>No.</v>

00:08:08.785 --> 00:08:09.185
<v Val Levitan>No.</v>

00:08:11.665 --> 00:08:12.545
<v Juan Martinez>So...</v>

00:08:13.385 --> 00:08:17.265
<v Juan Martinez>Now that the store has the paper.</v>

00:08:18.105 --> 00:08:29.985
<v Juan Martinez>in hand and tells the player to come back tomorrow because he's a regular. We can't process that through packs, through IQ, because we don't allow manual entry.</v>

00:08:21.505 --> 00:08:21.825
<v Andrei Klimovich>Yes.</v>

00:08:34.505 --> 00:08:43.265
<v Val Levitan>We don't. What do you mean come back? Right now, but how does it work right now? Does anybody come back?</v>

00:08:39.185 --> 00:08:39.625
<v Juan Martinez>Yeah.</v>

00:08:44.185 --> 00:08:58.625
<v Juan Martinez>Of course, yeah, that's the difference is the PAX is manual. You can come back and they can manually re-enter it when the internet is back up, when the PAX has been replaced. But we don't allow that.</v>

00:08:44.465 --> 00:08:45.425
<v Val Levitan>With the ticket.</v>

00:08:56.625 --> 00:08:57.265
<v Val Levitan>Button.</v>

00:08:59.025 --> 00:09:00.705
<v Val Levitan>But in practicality.</v>

00:09:01.665 --> 00:09:04.705
<v Val Levitan>Does anybody leave the location with a ticket?</v>

00:09:06.545 --> 00:09:25.025
<v Juan Martinez>No, I don't believe so. I think the store keeps the ticket with maybe they make a copy, maybe the player takes a picture of it. But since 2 tickets are not printed, I think the store is more comfortable keeping the thing and giving the customer some sort of IOU or whatever.</v>

00:09:24.505 --> 00:09:27.105
<v Val Levitan>What, which, which two tickets are printed?</v>

00:09:27.825 --> 00:09:33.745
<v Juan Martinez>The only one ticket is printed, the Mother Goose ticket. There is no other, there is no other ticket.</v>

00:09:31.025 --> 00:09:31.505
<v Val Levitan>Right.</v>

00:09:33.905 --> 00:09:34.625
<v Val Levitan>Correct.</v>

00:09:38.065 --> 00:09:40.545
<v Val Levitan>So what is the case that you are highlighting?</v>

00:09:41.585 --> 00:09:42.865
<v Juan Martinez>The case is that.</v>

00:09:44.145 --> 00:09:48.985
<v Juan Martinez>The location, let's say it's $800 cash out.</v>

00:09:50.145 --> 00:10:08.705
<v Juan Martinez>I don't want $800 worth of lottery tickets because that's a 50% loss on average on a lottery ticket. It's not a guaranteed winning lottery ticket. So the guests will want to come back. No, you're going to pay me in a gift card. How do we facilitate that?</v>

00:10:10.105 --> 00:10:11.905
<v Juan Martinez>And then the next day.</v>

00:10:14.305 --> 00:10:22.065
<v Val Levitan>To be honest with you, I never contemplated that somebody will leave with the ticket and come back.</v>

00:10:22.985 --> 00:10:42.625
<v Juan Martinez>No, remember, they're probably not leaving with the ticket. The store is keeping the ticket and the players is given something else. But I know that that happens because in South Dakota, if the location doesn't have enough money to pay a jackpot, they do some sort of manual paperwork and they tell the guests to come back.</v>

00:10:31.585 --> 00:10:31.745
<v Val Levitan>No.</v>

00:10:42.865 --> 00:10:50.625
<v Juan Martinez>We'll have the money to cover that tomorrow. That's a real route scenario in the event of a large win.</v>

00:10:55.865 --> 00:11:13.105
<v Juan Martinez>Question is, if we've lost all electronic history of that transaction, we're counting on the paper, yet we don't allow a manual entry into IQ, so how do they pay the player in our ecosystem?</v>

00:11:11.585 --> 00:11:16.465
<v Val Levitan>I, I never, I never contemplated that as a possibility.</v>

00:11:17.345 --> 00:11:29.345
<v Val Levitan>But if you bring this, if you're highlighting this particular scenario, you're saying that we should, we must allow manual entry of the ticket.</v>

00:11:30.705 --> 00:11:37.425
<v Juan Martinez>I think with the with proper administrator log on, we need to consider that as a possibility.</v>

00:11:39.025 --> 00:11:47.305
<v Juan Martinez>Because otherwise the location might say, oh, well, we need a PAX as a backup, and then we're not getting our $2.</v>

00:11:40.425 --> 00:11:40.785
<v Val Levitan>What?</v>

00:11:41.585 --> 00:11:41.985
<v Val Levitan>What?</v>

00:11:45.345 --> 00:11:46.625
<v Val Levitan>I think it's a.</v>

00:11:47.905 --> 00:11:52.225
<v Val Levitan>I think it's a terrible, I think it's a terrible solution to enter it manually.</v>

00:11:53.345 --> 00:12:05.505
<v Andrei Klimovich>Gentlemen, if we are talking about this pending transaction, it still exists on the IQ locally. So if the customer is back tomorrow, the administrator will find this transaction and he can proceed with this one.</v>

00:12:06.865 --> 00:12:14.385
<v Juan Martinez>But in the scenario we were describing, Flex IQ completely failed. They had to get a new one and it had to be recommissioned.</v>

00:12:14.225 --> 00:12:18.545
<v Andrei Klimovich>It's lost, yeah. In this case, it is lost. So it's a terrible situation.</v>

00:12:19.985 --> 00:12:26.465
<v Juan Martinez>Yeah, why are we losing data in 2026 when it was sent to us electronically?</v>

00:12:27.745 --> 00:12:29.665
<v Juan Martinez>That, that, that doesn't even seem possible.</v>

00:12:31.345 --> 00:12:37.905
<v Val Levitan>We're losing data on purpose because we don't want to keep the data. The moment you keep the data, it...</v>

00:12:39.345 --> 00:12:41.025
<v Val Levitan>It invokes other.</v>

00:12:42.305 --> 00:12:44.425
<v Val Levitan>scenarios that we don't want to live with.</v>

00:12:45.345 --> 00:12:51.825
<v Juan Martinez>But not even short term, like keeping it for a week and then deleting it to make sure everything is reconciled?</v>

00:12:49.985 --> 00:12:53.265
<v Val Levitan>Right, right, right, right.</v>

00:12:54.705 --> 00:12:59.345
<v Val Levitan>Right, I think it's, I think it's good to keep it if we own.</v>

00:12:55.185 --> 00:12:55.745
<v Juan Martinez>Because...</v>

00:13:00.385 --> 00:13:02.065
<v Val Levitan>Uh, end to end.</v>

00:13:03.145 --> 00:13:03.665
<v Val Levitan>Setup.</v>

00:13:05.265 --> 00:13:24.785
<v Val Levitan>If we, let's say, if we are, if we have SMIBs inside of the machines, if we have FlexPay on the location, I think it's good to offer a new set of capabilities, expanded set of capabilities where we keep memory, where we report on performance, on service, on accounting.</v>

00:13:25.945 --> 00:13:32.225
<v Val Levitan>That's a very good thing, but if we're wedging ourselves into somebody else's network.</v>

00:13:34.065 --> 00:13:40.305
<v Val Levitan>If, if we are guest in, if we're guest in their ecosystem.</v>

00:13:41.345 --> 00:13:43.265
<v Val Levitan>I think it's a bad thing to keep.</v>

00:13:45.265 --> 00:13:45.905
<v Val Levitan>Memory.</v>

00:13:48.305 --> 00:14:03.505
<v Juan Martinez>So then all of our reporting tools and all of that, we can't deliver the complete solution of acknowledging that there was a cash out on machine number one for $100 that got lost.</v>

00:14:02.105 --> 00:14:02.425
<v Val Levitan>Yeah.</v>

00:14:03.745 --> 00:14:06.225
<v Val Levitan>And I don't believe that we can deliver.</v>

00:14:08.145 --> 00:14:10.465
<v Val Levitan>I just don't see how we can deliver.</v>

00:14:13.745 --> 00:14:17.265
<v Val Levitan>the entire solution if we wedge ourselves into their network.</v>

00:14:19.585 --> 00:14:29.425
<v Juan Martinez>Yeah, I guess, Andrei, this is almost a master or a location question because what do they do today if they can't issue a gift card?</v>

00:14:29.665 --> 00:14:36.545
<v Val Levitan>And, and I'm sorry, Juan, I think it opens the door for us to offer an expanded.</v>

00:14:38.785 --> 00:14:44.065
<v Val Levitan>set of capabilities by giving away our SMIBs.</v>

00:14:47.185 --> 00:15:04.305
<v Val Levitan>And then if we gave away our SMIPS and offer expanded capabilities, then we can really deliver a proper system. We can keep memory, we can offer, you know, vouchers and anything else.</v>

00:15:06.145 --> 00:15:12.945
<v Juan Martinez>No, no, I understood that, but you're saying give away the smib and keep Mother Goose in place?</v>

00:15:13.345 --> 00:15:13.745
<v Val Levitan>No.</v>

00:15:15.025 --> 00:15:21.105
<v Val Levitan>Because the moment the moment we give away SMIPS, we don't need Mother Goose, then then it's all replaced.</v>

00:15:19.545 --> 00:15:20.385
<v Juan Martinez>No, no, right?</v>

00:15:22.145 --> 00:15:32.225
<v Juan Martinez>Yeah, but I mean, we need to be prepared for that. I mean, that's not something that's going to happen, I don't even say in 2026. You know, there's.</v>

00:15:27.185 --> 00:15:27.825
<v Val Levitan>Correct.</v>

00:15:31.745 --> 00:15:38.545
<v Val Levitan>Well, okay, I don't know whether it will happen in 2026, but I do agree that we need to be prepared.</v>

00:15:46.985 --> 00:15:47.585
<v Juan Martinez>Okay.</v>

00:15:51.425 --> 00:16:02.545
<v Juan Martinez>So on #3 here, we say no local transactions ever, records live in the cloud, but only we're saying only successful transactions live in the cloud.</v>

00:16:03.105 --> 00:16:03.665
<v Andrei Klimovich>Correct.</v>

00:16:06.065 --> 00:16:06.385
<v Juan Martinez>Okay.</v>

00:16:08.865 --> 00:16:17.825
<v Juan Martinez>Only record successful transactions. Everything else we don't know. So again, what I'm we are now the single point of.</v>

00:16:19.025 --> 00:16:21.745
<v Juan Martinez>gift card processing for that location.</v>

00:16:23.105 --> 00:16:26.465
<v Juan Martinez>How, why, why are we choosing not to know?</v>

00:16:23.265 --> 00:16:23.825
<v Val Levitan>But...</v>

00:16:28.785 --> 00:16:34.705
<v Val Levitan>Because we we actually not a single source of processing by.</v>

00:16:36.145 --> 00:16:37.345
<v Val Levitan>By nature, today.</v>

00:16:41.745 --> 00:17:00.625
<v Juan Martinez>Sorry, but we will be once we install the location. The only other option is to have a backup packs device to generate the gift card manually or to attempt to give the player lottery tickets. And if it's a large win, no player will accept that because...</v>

00:17:01.345 --> 00:17:14.305
<v Juan Martinez>Lottery tickets are not worth the face value. They're, you know, 50, 60% loss on average. Every lottery ticket is not a winner. So why would I intentionally lose money by accepting lottery tickets?</v>

00:17:16.385 --> 00:17:33.025
<v Juan Martinez>I just want to stress that. Put yourself in the players' perspective. You just won $500. Why would you accept possibly $300 worth of real lottery tickets when you go and scratch them off in the parking lot and half of them are losers?</v>

00:17:23.825 --> 00:17:23.985
<v Val Levitan>Yeah.</v>

00:17:34.145 --> 00:17:40.385
<v Val Levitan>Because I believe that locations, even with the prepaid card, will get paid cash.</v>

00:17:41.665 --> 00:17:43.945
<v Juan Martinez>No, no, I, I, I understand that.</v>

00:17:43.825 --> 00:17:46.625
<v Val Levitan>I, I don't think anybody buys lottery tickets.</v>

00:17:48.225 --> 00:17:49.265
<v Juan Martinez>Oh, you're right.</v>

00:17:55.025 --> 00:18:05.105
<v Val Levitan>And I actually, and actually even with the prepaid MasterCard, I don't believe that it's a proper.</v>

00:18:06.545 --> 00:18:07.825
<v Val Levitan>Business.</v>

00:18:10.505 --> 00:18:10.625
<v Val Levitan>Um...</v>

00:18:14.705 --> 00:18:17.025
<v Val Levitan>Realistic business scenario.</v>

00:18:18.145 --> 00:18:19.585
<v Val Levitan>Because nobody will.</v>

00:18:22.145 --> 00:18:25.585
<v Val Levitan>No, nobody, nobody will get Mastercards.</v>

00:18:32.225 --> 00:18:36.625
<v Juan Martinez>Well, I mean, we have confirmation from Incon that that is happening.</v>

00:18:34.625 --> 00:18:34.785
<v Andrei Klimovich>Last.</v>

00:18:37.905 --> 00:18:39.265
<v Val Levitan>But to which degree?</v>

00:18:40.985 --> 00:19:00.505
<v Juan Martinez>Yeah, all right now, Georgia, because the lottery is very weak from a regulatory perspective, they're going to locations. If they're seeing they're not issuing gift cards, they're first issuing warnings. I'm going to guess it's two or three warnings and then maybe a fine. I mean, yeah.</v>

00:19:00.705 --> 00:19:06.385
<v Juan Martinez>I mean, you're right. I mean, they're not really enforcing it as much as they should.</v>

00:19:09.425 --> 00:19:10.385
<v Val Levitan>But.</v>

00:19:11.505 --> 00:19:15.745
<v Val Levitan>The case that you brought, I mean, I mean, it's a it's an extreme.</v>

00:19:17.025 --> 00:19:18.545
<v Val Levitan>Edge case extreme.</v>

00:19:19.705 --> 00:19:23.425
<v Val Levitan>But the one that you brought to my attention, I didn't think about it.</v>

00:19:24.545 --> 00:19:28.065
<v Val Levitan>And I, I don't, I don't know.</v>

00:19:24.705 --> 00:19:25.145
<v Andrei Klimovich>And so.</v>

00:19:28.385 --> 00:19:31.265
<v Andrei Klimovich>On Monday? Yeah, see you. Bye, bye, bye.</v>

00:19:32.065 --> 00:19:36.065
<v Val Levitan>I don't know how to react to it, but I see your case.</v>

00:19:37.425 --> 00:19:38.865
<v Val Levitan>I understand your case.</v>

00:19:37.825 --> 00:19:42.065
<v Juan Martinez>Yeah, and I, I, and I'm gonna think about it a little bit more.</v>

00:19:43.985 --> 00:19:44.905
<v Juan Martinez>So, the...</v>

00:19:47.025 --> 00:19:51.425
<v Juan Martinez>Number 5, the any transaction above $1,000.</v>

00:19:53.265 --> 00:20:03.825
<v Juan Martinez>Do we have a technology deficit where we can't auto-create multiple cards to get us to a win of $1,500?</v>

00:20:04.785 --> 00:20:09.825
<v Andrei Klimovich>Oh, we can. I mean, like, we can split the transaction. We can get a voucher for...</v>

00:20:11.105 --> 00:20:13.265
<v Andrei Klimovich>2,500 and split.</v>

00:20:11.585 --> 00:20:11.905
<v Juan Martinez>Yup.</v>

00:20:12.145 --> 00:20:20.065
<v Val Levitan>Wait, wait, wait, we can't just, I'm building on what Andrei is attempting to say. We can, if we.</v>

00:20:22.065 --> 00:20:25.985
<v Val Levitan>Implement manual ticket entry.</v>

00:20:27.785 --> 00:20:30.545
<v Juan Martinez>No, why? Why can't we automate it? I mean,</v>

00:20:29.825 --> 00:20:31.585
<v Andrei Klimovich>No, no, no, why should we do that?</v>

00:20:32.585 --> 00:20:34.545
<v Val Levitan>Yes, I'll explain.</v>

00:20:35.745 --> 00:20:50.465
<v Val Levitan>Because if let's say somebody wins $2500, you could do 1000, 1500. So your first thousand goes through validated, your second thousand goes through validated, and your next 500 you run out of cards.</v>

00:20:56.385 --> 00:20:59.745
<v Andrei Klimovich>So, or where is the manual comes in?</v>

00:21:01.905 --> 00:21:09.665
<v Val Levitan>So there's no manual adjustment. You cannot say I only issued 2000 against this ticket because then the ticket is still valid.</v>

00:21:12.545 --> 00:21:30.945
<v Juan Martinez>I think there's still, the cards are not going to be auto-generated because you have to swipe the card, each card in to have it read. I would argue, Val, that I would run next door to the nearest Kroger and grab some of their cards off the shelf that are free to take, by the way.</v>

00:21:31.345 --> 00:21:33.825
<v Juan Martinez>and get me through this transaction.</v>

00:21:34.385 --> 00:21:36.545
<v Val Levitan>Well, then there is another scenario.</v>

00:21:38.465 --> 00:21:41.345
<v Val Levitan>In the third transaction, the touch screen breaks.</v>

00:21:44.785 --> 00:21:45.825
<v Val Levitan>What, what do you do?</v>

00:21:51.665 --> 00:22:10.665
<v Andrei Klimovich>So, now it's still between the location and the player right now, isn't it? So, the location still owns the player 500 bucks, and it's up to them how they will resolve it. From our side, we've completed two cards with 1K each.</v>

00:21:51.825 --> 00:21:52.105
<v Juan Martinez>Yeah.</v>

00:22:12.465 --> 00:22:13.585
<v Andrei Klimovich>So, maybe it's like...</v>

00:22:12.625 --> 00:22:16.545
<v Juan Martinez>And collected and collected $4.00 in service fees.</v>

00:22:14.785 --> 00:22:14.945
<v Andrei Klimovich>Yeah.</v>

00:22:16.105 --> 00:22:28.705
<v Andrei Klimovich>Correct, correct. So maybe location will take this Mutagus ticket with 2,500 and they will write down manually this ticket still valid for 500.</v>

00:22:29.905 --> 00:22:38.385
<v Andrei Klimovich>and take a picture of it and come back tomorrow when we will have more cards or income will be up again or whatever.</v>

00:22:36.785 --> 00:22:42.865
<v Val Levitan>But, but, but at that point, do you manually enter the 500?</v>

00:22:43.505 --> 00:22:48.145
<v Andrei Klimovich>No, no, no, this transaction still exists on AQ locally.</v>

00:22:48.945 --> 00:22:51.465
<v Val Levitan>But what happens if IQ needs to be replaced?</v>

00:22:53.345 --> 00:23:04.305
<v Andrei Klimovich>This is a problem in case if we are not storing those transactions in cloud as it was designed initially. If we don't do that, we lose those transactions.</v>

00:23:14.745 --> 00:23:23.025
<v Juan Martinez>Yeah, I, I, I, what's the actual concern though, Val, with keeping transactions for three to five days and then deleting them?</v>

00:23:24.145 --> 00:23:28.865
<v Val Levitan>Well, the concern is what to do in other cases.</v>

00:23:30.225 --> 00:23:34.945
<v Val Levitan>Then how do you decommission the machine? How do you commission a new machine?</v>

00:23:36.065 --> 00:23:49.345
<v Val Levitan>I don't remember exactly, but there were probably three or five different scenarios that were brought up to my attention. And the summary of those scenarios made me understand that it's best not to keep a transaction.</v>

00:23:51.345 --> 00:23:55.985
<v Val Levitan>And I'm also, and I'm also uncomfortable keeping the transactions.</v>

00:24:03.345 --> 00:24:14.145
<v Juan Martinez>I mean, the greater than $1,000 wins probably make up 5% of the monthly transactions, but it's going to happen.</v>

00:24:15.225 --> 00:24:15.825
<v Juan Martinez>So.</v>

00:24:17.905 --> 00:24:25.705
<v Juan Martinez>Again, we are basically saying that unlike a packs, our device doesn't support anything over $1,000.</v>

00:24:28.545 --> 00:24:30.945
<v Val Levitan>We haven't said that yet, but...</v>

00:24:32.065 --> 00:24:33.745
<v Val Levitan>It's under contemplation.</v>

00:24:40.105 --> 00:24:52.705
<v Juan Martinez>I mean, can we drill down with the team into what those concerns were with temporarily storing information in the cloud as it was originally specked out?</v>

00:24:53.625 --> 00:24:54.065
<v Val Levitan>Sure.</v>

00:24:55.425 --> 00:24:55.825
<v Juan Martinez>Thanks.</v>

00:24:58.625 --> 00:25:07.585
<v Juan Martinez>Point number six below the $7.00. I agree with that, that if, if, if we we get a.</v>

00:25:09.065 --> 00:25:20.465
<v Juan Martinez>intercept of less than $7, we ignore it. The point though is we need a UI-UX messaging to alert.</v>

00:25:21.585 --> 00:25:28.145
<v Juan Martinez>the cashier that this transaction came in and it must be processed some other way.</v>

00:25:29.305 --> 00:25:39.345
<v Juan Martinez>And then she'll know to handle that Mother Goose ticket differently than the one that came before it for $12.00, you know.</v>

00:25:40.545 --> 00:25:50.225
<v Andrei Klimovich>Yeah, it's the same with 1K. If we do, if we ignore it, there should be the kind of notification telling that process this transaction somehow.</v>

00:25:51.985 --> 00:26:11.585
<v Juan Martinez>Understood, understood. And then the last one, commissioning 1 IQ equals 1 location forever. No decommission process exists. Devices move or connects elsewhere, it's dead, no longer commission. So</v>

00:26:13.865 --> 00:26:16.865
<v Juan Martinez>Are you saying that Flex IQ is a disposable item?</v>

00:26:22.225 --> 00:26:39.265
<v Juan Martinez>I'm just trying to understand when we say we have to replace it, so we have to commission a new one to that location. Are we saying in our cloud data, we just always keep the old IQ assigned to location X forever?</v>

00:26:41.345 --> 00:26:44.865
<v Val Levitan>No, what this, uh, what this is saying is that...</v>

00:26:46.065 --> 00:26:46.785
<v Val Levitan>We.</v>

00:26:47.905 --> 00:26:52.145
<v Val Levitan>automatically decommission anything that is not currently commissioned.</v>

00:26:58.225 --> 00:27:05.025
<v Val Levitan>So for example, we had device 123 commission to location ABC.</v>

00:27:06.385 --> 00:27:09.345
<v Val Levitan>And for whatever reason, it makes no difference why.</v>

00:27:10.625 --> 00:27:23.985
<v Val Levitan>There is a new device, 789, arrives on this location and gets commissioned on this location. The device 123 gets automatically cancelled out.</v>

00:27:26.945 --> 00:27:27.825
<v Val Levitan>It cannot.</v>

00:27:27.425 --> 00:27:30.305
<v Juan Martinez>And it and it cannot be reused anywhere.</v>

00:27:30.785 --> 00:27:35.025
<v Val Levitan>It can't be, but then it has to be commissioned in a new place.</v>

00:27:38.465 --> 00:27:40.225
<v Juan Martinez>OK, no, that that that.</v>

00:27:39.345 --> 00:27:48.545
<v Val Levitan>We, we, we just, I just don't want to have a process by which we are obligated to decommission before we commission.</v>

00:27:51.825 --> 00:28:04.065
<v Juan Martinez>And this automated decommissioning, we also need to notify income that a device is decommissioned, just like we have to request the commissioning itself.</v>

00:28:04.785 --> 00:28:08.225
<v Val Levitan>But I think that's a very mundane process.</v>

00:28:09.265 --> 00:28:09.585
<v Juan Martinez>Yeah.</v>

00:28:10.305 --> 00:28:15.745
<v Val Levitan>Any device that is not longer commissioned, we can send a message that it's decommissioned.</v>

00:28:15.065 --> 00:28:15.225
<v Andrei Klimovich>Max.</v>

00:28:19.345 --> 00:28:19.825
<v Juan Martinez>K.</v>

00:28:22.385 --> 00:28:41.665
<v Juan Martinez>My only concern would be if we, if there was a technician troubleshooting and he keeps a IQ in the van to swap out to rule out a network problem or something else, the minute we plug in the new one, does it automatically disable the old one?</v>

00:28:42.305 --> 00:28:42.985
<v Juan Martinez>And...</v>

00:28:44.065 --> 00:28:49.025
<v Juan Martinez>What problem could that cause? I think it shouldn't be fully automatic. There should be...</v>

00:28:48.705 --> 00:28:54.625
<v Val Levitan>But how can he, but how can he suddenly take a device from his truck and commission it?</v>

00:28:59.025 --> 00:29:02.945
<v Val Levitan>He may, he may plug in, and there might be some tests.</v>

00:29:04.305 --> 00:29:19.745
<v Val Levitan>a hookup in the cloud that may test his device or may test our device, but how can he commission? Suddenly he comes in with an external device, plugs it in and commissions it.</v>

00:29:21.105 --> 00:29:25.985
<v Juan Martinez>Oh no, no, because that, I mean, that there's a process for commissioning and it involves income.</v>

00:29:26.545 --> 00:29:39.265
<v Val Levitan>Okay, so he could do whatever testing he needs to do. Telephone lines, reaching out a server, and do whatever he needs to do, but you know, he's not commissioning a device.</v>

00:29:40.545 --> 00:29:46.065
<v Val Levitan>But if he commissions a device, how can you have two devices commissioned?</v>

00:29:40.905 --> 00:29:41.585
<v Juan Martinez>OK, yeah.</v>

00:29:47.745 --> 00:29:59.505
<v Juan Martinez>But you can. I mean, we don't necessarily want that, but you can. You keep giving income the information and they will commission as many devices per location as you want.</v>

00:29:49.545 --> 00:29:49.745
<v Andrei Klimovich>This.</v>

00:30:00.145 --> 00:30:19.265
<v Val Levitan>Okay, that's not a problem. If in our scheme we're saying, look, we can accept multiple devices commissioned in that location, let's just keep it, but then we'll slightly change the formula. I assume I need to think about it. But we can probably slightly change the rule and say you could have</v>

00:30:19.665 --> 00:30:24.065
<v Val Levitan>Let's say 5 devices maximum or three devices maximum per location.</v>

00:30:25.225 --> 00:30:33.105
<v Val Levitan>But it means that this device cannot appear on another location. If it appears on another location, you should decommission it from this location.</v>

00:30:29.145 --> 00:30:29.345
<v Juan Martinez>Right.</v>

00:30:33.785 --> 00:30:34.145
<v Juan Martinez>Right.</v>

00:30:35.265 --> 00:30:41.745
<v Juan Martinez>Right, and I'm not advocating multiple devices in one location, but I'm just I'm just walking through.</v>

00:30:36.065 --> 00:30:37.105
<v Val Levitan>So, the the point...</v>

00:30:43.065 --> 00:30:43.585
<v Juan Martinez>Yes.</v>

00:30:43.265 --> 00:30:53.665
<v Val Levitan>I'm just against the process, a manual process of decommissioning. I'm saying why to decommission something that if, you know,</v>

00:30:54.425 --> 00:30:54.705
<v Juan Martinez>Sure.</v>

00:30:56.145 --> 00:31:01.665
<v Val Levitan>If, if you, if you connect, if your rule is only one device per location.</v>

00:31:02.865 --> 00:31:15.185
<v Val Levitan>then the moment you connect a different device, a new device in this location, and your rule is still one device per location, then the previous device can be considered decommissioned.</v>

00:31:15.825 --> 00:31:16.145
<v Juan Martinez>Right.</v>

00:31:16.705 --> 00:31:20.145
<v Val Levitan>And that could have an automated workflow.</v>

00:31:22.225 --> 00:31:23.425
<v Juan Martinez>Agreed. Agreed.</v>

00:31:24.265 --> 00:31:24.745
<v Juan Martinez>Okay.</v>

00:31:28.305 --> 00:31:35.425
<v Val Levitan>So the so the only point of contention here is.</v>

00:31:38.665 --> 00:31:44.065
<v Val Levitan>whether or not to allow a manual entry of the ticket.</v>

00:31:46.265 --> 00:31:58.305
<v Val Levitan>Do I understand it correctly or there are other points of contention? I don't know what to do with $1,000. Let's, before we do that, before we do that, let's decide whether manual entry is allowed.</v>

00:31:53.665 --> 00:31:54.145
<v Juan Martinez>Okay.</v>

00:32:02.465 --> 00:32:22.785
<v Juan Martinez>I think under certain conditions, especially high dollar jackpots and a administrator type pin that maybe is controlled by the master, that we should allow a manual process. And this is what Jason referred to as that delay, where</v>

00:32:22.945 --> 00:32:36.465
<v Juan Martinez>you know, income is going to give us, or the lottery is going to allow for the master to phone in saying, hey, did everything check out okay? Okay, use this PIN and manually complete the transaction.</v>

00:32:28.145 --> 00:32:28.625
<v Andrei Klimovich>Yes.</v>

00:32:38.985 --> 00:32:39.305
<v Val Levitan>For me.</v>

00:32:39.985 --> 00:32:54.385
<v Juan Martinez>But I think that I don't want to do manual because we've been selling security and safety, but it's also a detriment to us when we know that the PACS allows for manual.</v>

00:32:55.505 --> 00:33:03.985
<v Juan Martinez>And they may say, well, why can't you, you know, why do we have to call you and deal with this whole mess when this other handheld just lets you override?</v>

00:33:05.105 --> 00:33:08.625
<v Val Levitan>Because I think the full solution comes from...</v>

00:33:09.665 --> 00:33:15.585
<v Val Levitan>owning the entire network and I think that opens up a beautiful opportunity for us to get in.</v>

00:33:16.705 --> 00:33:23.265
<v Val Levitan>And at that point, we can add all automated capabilities. We can, we can.</v>

00:33:25.105 --> 00:33:43.425
<v Val Levitan>interrogate the machine. We can keep the memory indefinitely if we want to, because we have a closed loop system. But if we enter in somebody else's system and already allowing a print, a ticket print,</v>

00:33:44.865 --> 00:33:47.665
<v Val Levitan>Then, in my opinion.</v>

00:33:54.785 --> 00:33:57.585
<v Val Levitan>We should, we should minimize our...</v>

00:33:59.105 --> 00:33:59.905
<v Val Levitan>Intrusion.</v>

00:34:00.865 --> 00:34:01.265
<v Juan Martinez>Sure.</v>

00:34:02.545 --> 00:34:16.625
<v Val Levitan>And then if somebody says, but why don't you provide the whole information, we have a beautiful comeback. We could say, absolutely, not only that, but we will provide these capabilities.</v>

00:34:18.665 --> 00:34:21.025
<v Val Levitan>which makes an operator salivate.</v>

00:34:23.905 --> 00:34:28.665
<v Val Levitan>with a condition that you will install our SMIPS.</v>

00:34:32.545 --> 00:34:37.505
<v Val Levitan>And then a location says, well, how much does it cost? Well, it's for free.</v>

00:34:32.945 --> 00:34:33.185
<v Juan Martinez>Just.</v>

00:34:38.625 --> 00:34:38.865
<v Juan Martinez>Yeah.</v>

00:34:42.145 --> 00:34:43.905
<v Juan Martinez>And my last question, which...</v>

00:34:45.585 --> 00:35:02.625
<v Juan Martinez>I'm not sure how we were doing it before, but in terms of getting the data posted to Microsoft Business Central, now that we're doing it only for a successful transaction, does that change Nathan's flow in anything he's done or was it always that way?</v>

00:34:56.785 --> 00:34:57.065
<v Andrei Klimovich>Scism.</v>

00:35:03.185 --> 00:35:05.025
<v Andrei Klimovich>Not should not change anything.</v>

00:35:03.585 --> 00:35:04.065
<v Val Levitan>No.</v>

00:35:05.585 --> 00:35:05.985
<v Juan Martinez>OK.</v>

00:35:05.825 --> 00:35:06.145
<v Val Levitan>No.</v>

00:35:07.745 --> 00:35:08.065
<v Juan Martinez>But.</v>

00:35:08.625 --> 00:35:17.905
<v Val Levitan>Well, Nathan's flaw was never dependent on whether we reject or validate, because Nathan only is interested in money processing.</v>

00:35:18.705 --> 00:35:20.225
<v Juan Martinez>Okay, that's right, that's right.</v>

00:35:20.945 --> 00:35:29.265
<v Val Levitan>He is not interested in rejections, like he's interested in validating balances. We took the money.</v>

00:35:30.465 --> 00:35:32.225
<v Val Levitan>We processed, we applied it.</v>

00:35:36.145 --> 00:35:36.625
<v Juan Martinez>Stood.</v>

00:35:39.025 --> 00:35:41.825
<v Juan Martinez>Well, all my questions are answered, I guess.</v>

00:35:42.305 --> 00:35:52.145
<v Val Levitan>No, but we're still dwelling on what to do in that, in the two rare cases where we don't understand what to do with</v>

00:35:53.425 --> 00:35:55.745
<v Val Levitan>With the ticket, is this that that's?</v>

00:35:55.985 --> 00:35:56.865
<v Juan Martinez>That's correct.</v>

00:35:59.585 --> 00:36:05.585
<v Val Levitan>Okay, let's examine another, let's examine this scenario again, run it by me again.</v>

00:36:09.425 --> 00:36:11.425
<v Andrei Klimovich>Okay, so there is a cash out.</v>

00:36:12.305 --> 00:36:16.465
<v Andrei Klimovich>Captured by Martinez for, let's say, 2500.</v>

00:36:17.345 --> 00:36:18.745
<v Val Levitan>No, no, no, no.</v>

00:36:20.065 --> 00:36:22.465
<v Val Levitan>No, the small tickets scenario.</v>

00:36:23.705 --> 00:36:27.025
<v Val Levitan>Where, where uh, one said that we should um...</v>

00:36:24.465 --> 00:36:24.505
<v Andrei Klimovich>Ah.</v>

00:36:27.825 --> 00:36:30.145
<v Val Levitan>We must have a manual entry.</v>

00:36:35.105 --> 00:36:40.305
<v Juan Martinez>Yeah, I mean, it basically is, I mean, it really, we, we...</v>

00:36:41.425 --> 00:36:51.105
<v Juan Martinez>The location is supposed to use a gift card as the number one payout preferred per Georgia lottery. So if there's a failure,</v>

00:36:53.105 --> 00:37:13.425
<v Juan Martinez>The Mother Goose ticket is printed. It's in their hand. We state, player keeps the ticket, goes through the standard Mother Goose path. Well, the Mother Goose path changed on July 1st, you know, to now, hey, you have to 1st attempt to give them a lottery.</v>

00:37:14.105 --> 00:37:16.705
<v Juan Martinez>A gift card? How are they doing that?</v>

00:37:18.705 --> 00:37:30.465
<v Juan Martinez>If something happened, but they know that they need to give that customer a $50 gift card, we could allow for a manual entry through an administrator PIN.</v>

00:37:42.225 --> 00:37:44.945
<v Juan Martinez>Because the other devices allow for manual.</v>

00:37:54.305 --> 00:38:01.665
<v Andrei Klimovich>But, Juan, how do you see that in reality? Like, who handles this administrator pin? Who is this person?</v>

00:38:02.545 --> 00:38:03.985
<v Juan Martinez>I should be the master.</v>

00:38:04.945 --> 00:38:08.785
<v Andrei Klimovich>So, the cashier needs to call a master.</v>

00:38:09.545 --> 00:38:30.945
<v Juan Martinez>She needs to call her boss, who would then call the master. I doubt the cashier, unless it's a large master that has a technical 1-800 type of number or team, maybe that relationship exists, but normally it would be her calling her boss at the location who would then contact the master.</v>

00:38:31.505 --> 00:38:37.425
<v Juan Martinez>for some clear instructions and or that PIN number to authorize a manual entry.</v>

00:38:39.745 --> 00:38:49.905
<v Andrei Klimovich>What kind of conversation will it be? Like what kind of data will the cashier provide and how this data will be analyzed by the recipient? I mean,</v>

00:38:50.865 --> 00:38:58.305
<v Andrei Klimovich>I need to issue 500 bucks, but why? The problem is with cards. Cards do not work.</v>

00:38:55.625 --> 00:38:55.865
<v Juan Martinez>Yeah.</v>

00:38:58.945 --> 00:39:00.545
<v Juan Martinez>Yeah, we ran out of cards.</v>

00:38:59.345 --> 00:39:04.065
<v Andrei Klimovich>Okay, okay, I trust you. Yeah, do that. Here's the pin.</v>

00:39:05.185 --> 00:39:06.065
<v Andrei Klimovich>So...</v>

00:39:07.265 --> 00:39:07.985
<v Juan Martinez>Or.</v>

00:39:08.985 --> 00:39:23.665
<v Juan Martinez>It could all be, hey, no, tell the player we apologize. I'll send somebody over with extra cards. He can come back in two hours, make him a copy of the Mother Goose ticket. That could be one of the conversations.</v>

00:39:18.905 --> 00:39:19.025
<v Andrei Klimovich>Yes.</v>

00:39:26.065 --> 00:39:48.265
<v Juan Martinez>The point is, if the transaction is not stored on Flex IQ, they can't re-attempt to do it on a card unless we agree to temporarily store a transaction. If they have not hit anything on our IQ screen, it's technically sitting there waiting to be processed, correct?</v>

00:39:49.345 --> 00:40:02.545
<v Andrei Klimovich>Of course, but the problem is if the IQ itself is dead. If we are not storing, if we are not storing pending transaction into the cloud, they exist only locally. So if something happens with the device, it's lost.</v>

00:39:53.985 --> 00:39:54.585
<v Juan Martinez>Yes, yeah.</v>

00:39:58.385 --> 00:39:58.785
<v Juan Martinez>Right.</v>

00:40:04.225 --> 00:40:07.745
<v Juan Martinez>Right, it's lost, but the Mother Goose printout is not lost.</v>

00:40:09.145 --> 00:40:10.465
<v Andrei Klimovich>Of course, but...</v>

00:40:11.785 --> 00:40:21.185
<v Andrei Klimovich>We already have a partial redemption, right? So part of this ticket has already been issued with card, and the conflict is only around the...</v>

00:40:23.665 --> 00:40:24.785
<v Andrei Klimovich>The last part of it.</v>

00:40:24.865 --> 00:40:26.385
<v Juan Martinez>Yeah, yeah, the fractional part.</v>

00:40:27.025 --> 00:40:27.505
<v Andrei Klimovich>Mhm.</v>

00:40:28.945 --> 00:40:45.585
<v Juan Martinez>No, and the sad thing is, is that's where theft can come in. I have a Mother Goose ticket for 500. You know, I only paid the guest $100 on a gift card. We owe him 400, which is not true. And it's hard to dispute that real time.</v>

00:40:39.665 --> 00:40:39.905
<v Andrei Klimovich>Yes.</v>

00:40:42.385 --> 00:40:42.465
<v Andrei Klimovich>Oh.</v>

00:40:47.105 --> 00:40:54.465
<v Val Levitan>So the whole problem is created because I eliminated memory component.</v>

00:40:55.505 --> 00:40:56.785
<v Val Levitan>Do I read you correctly?</v>

00:40:58.785 --> 00:40:59.065
<v Juan Martinez>Yeah.</v>

00:40:59.185 --> 00:40:59.745
<v Andrei Klimovich>Well...</v>

00:41:00.865 --> 00:41:03.745
<v Andrei Klimovich>It creates additional edge cases, for sure.</v>

00:41:13.985 --> 00:41:34.865
<v Juan Martinez>I mean, because we could have logic to upload to the cloud, and if it's a still open transaction, keep it there for five days. Surely everything would get resolved in five days. But as I say that, no, we didn't have an IQ. It's coming by FedEx. There was a delay.</v>

00:41:14.225 --> 00:41:14.865
<v Andrei Klimovich>I'm in.</v>

00:41:35.105 --> 00:41:46.625
<v Juan Martinez>I mean, we need to think about these are far and rare edge cases, but they are actual cases. You know, when, how long would we keep the transaction in the cloud for before wiping it?</v>

00:41:47.585 --> 00:41:49.665
<v Juan Martinez>You know, there has to be a balance there.</v>

00:41:48.785 --> 00:41:51.905
<v Val Levitan>We can wait from from.</v>

00:41:53.025 --> 00:41:55.505
<v Val Levitan>Technology limitation, there is no limitation.</v>

00:41:56.105 --> 00:42:07.105
<v Juan Martinez>Oh no, Val, I'm trying to meet you halfway on not wanting to keep data. We shouldn't keep it forever. I'm fully aware that the database can keep transactions from five years ago.</v>

00:41:59.185 --> 00:41:59.345
<v Andrei Klimovich>Ohh.</v>

00:42:00.825 --> 00:42:00.905
<v Andrei Klimovich>If...</v>

00:42:07.345 --> 00:42:23.345
<v Val Levitan>One, you know me for many years. I don't mind to be wrong. I actually don't even have, I don't have a remorse of being wrong. It's not in my personality. So I don't care. If I'm wrong, I'm wrong.</v>

00:42:20.225 --> 00:42:20.465
<v Juan Martinez>Yeah.</v>

00:42:25.505 --> 00:42:25.905
<v Val Levitan>But...</v>

00:42:27.105 --> 00:42:32.705
<v Val Levitan>I'm just trying to understand myself whether it's wrong not to keep.</v>

00:42:33.785 --> 00:42:45.585
<v Val Levitan>transactions or whether in my view, it will push the operators to upgrade to our end-to-end system because it bothers them so much.</v>

00:42:48.385 --> 00:42:56.225
<v Juan Martinez>Yeah, the twist there is it bothers them so much, they have other choices. That's my concern.</v>

00:42:56.625 --> 00:42:58.385
<v Val Levitan>But do they have other choices?</v>

00:42:59.665 --> 00:43:09.345
<v Juan Martinez>Sure, there's 100 different suppliers out there. They may be worse than us for sure, but they're not going to know that until they try them or until they call their uncle.</v>

00:43:05.505 --> 00:43:06.465
<v Val Levitan>What if they worse?</v>

00:43:08.065 --> 00:43:09.185
<v Val Levitan>But if they were.</v>

00:43:10.625 --> 00:43:21.825
<v Val Levitan>I know, but if they're worse, do they, I mean, as we, as they start experiencing our product and another supplier comes in and cannot provide what we can provide.</v>

00:43:25.025 --> 00:43:26.465
<v Val Levitan>Is it really a choice?</v>

00:43:29.505 --> 00:43:48.505
<v Juan Martinez>I mean, not necessarily, and I don't know what goes under the table with the other guys' systems and kickbacks and, you know, who knows what else they could offer. But I mean, again, that's far and remote. I think anybody who wants to get into this business because the deadline has already passed,</v>

00:43:48.705 --> 00:44:01.265
<v Juan Martinez>is probably already out there. So we technically would know who everybody is over the next few months anyway. I don't think anyone's going to pop up out of the blue with some miracle solution.</v>

00:44:01.745 --> 00:44:05.585
<v Val Levitan>I think, I think our true competition is packs.</v>

00:44:06.385 --> 00:44:06.625
<v Juan Martinez>Yeah.</v>

00:44:06.745 --> 00:44:10.545
<v Val Levitan>But that's really, in a nutshell, that's our competition.</v>

00:44:11.345 --> 00:44:11.745
<v Juan Martinez>Great.</v>

00:44:12.705 --> 00:44:18.465
<v Val Levitan>Because we're not competing to sell, we're competing for reoccurring revenue for that $2.00.</v>

00:44:18.945 --> 00:44:19.265
<v Juan Martinez>Right.</v>

00:44:20.385 --> 00:44:30.225
<v Val Levitan>And so PAX is already engraved in the market. And PAX is owned by income, who explicitly said that they're not really interested, they're not going to develop anything.</v>

00:44:31.105 --> 00:44:33.105
<v Juan Martinez>Right, yeah, because they don't even make that device.</v>

00:44:31.305 --> 00:44:31.745
<v Val Levitan>It is.</v>

00:44:33.345 --> 00:44:38.625
<v Val Levitan>That's right. I mean, it is what it is. And that's it. And they're not moving forward with it.</v>

00:44:39.345 --> 00:44:39.585
<v Juan Martinez>Right.</v>

00:44:40.465 --> 00:44:46.865
<v Val Levitan>So they provided the initial solution. We are walking in at the same level as Sparks and we're saying, look.</v>

00:44:47.745 --> 00:44:49.025
<v Val Levitan>We can be much better.</v>

00:44:52.505 --> 00:44:52.785
<v Juan Martinez>Yep.</v>

00:44:55.745 --> 00:44:56.145
<v Juan Martinez>Great.</v>

00:44:57.025 --> 00:45:01.905
<v Andrei Klimovich>So what makes IQ better than PAX right now? What is a killer feature?</v>

00:45:04.425 --> 00:45:12.785
<v Val Levitan>Well, I don't believe that we can offer a killer feature if we do not change the network.</v>

00:45:14.945 --> 00:45:22.865
<v Val Levitan>But when we change, but when we change, when we start controlling end-to-end, I think this is when we can truly offer killer features.</v>

00:45:15.185 --> 00:45:16.065
<v Andrei Klimovich>Yeah, it's mhm.</v>

00:45:23.505 --> 00:45:23.985
<v Andrei Klimovich>But...</v>

00:45:41.745 --> 00:45:43.185
<v Val Levitan>Yes, yes.</v>

00:45:43.225 --> 00:45:55.585
<v Juan Martinez>reduced. Ten bucks times 30 days, that's $300 a month getting stolen from me because I don't have the time or resources to track it. So I love the automated.</v>

00:45:44.385 --> 00:45:44.865
<v Val Levitan>Yes.</v>

00:45:56.505 --> 00:45:57.665
<v Juan Martinez>No manual part.</v>

00:45:58.625 --> 00:45:59.505
<v Val Levitan>Yes, me too.</v>

00:46:00.145 --> 00:46:05.585
<v Andrei Klimovich>So, as soon as we introduce manual input, we are disintegrating this advantage.</v>

00:46:04.465 --> 00:46:20.945
<v Juan Martinez>Yeah, but with A twist. There's a PIN. You've got to make calls. It's aware. You now know that attendant Sallie Mae called you and requested a PIN on Monday at 3 P.m. Do what you want with the information, but...</v>

00:46:07.665 --> 00:46:08.145
<v Andrei Klimovich>Ohh.</v>

00:46:10.305 --> 00:46:11.185
<v Andrei Klimovich>It's.</v>

00:46:13.825 --> 00:46:13.985
<v Val Levitan>Yeah.</v>

00:46:18.545 --> 00:46:19.665
<v Andrei Klimovich>Yeah, I know.</v>

00:46:20.785 --> 00:46:39.545
<v Andrei Klimovich>I'm following you, Juan, but me is like, I try to imagine myself a master who has hundreds of locations. And when you say automation, it sounds beautiful to me. It means that I do not worry about anything. I just installed one device and it's beautiful. I don't care about the cache being stolen anymore.</v>

00:46:40.225 --> 00:46:54.385
<v Andrei Klimovich>So, and now you introduce like a situation when someone can call me and start to explain why they need access to manual input and I need to analyze, I need to make a decision. It complicates everything.</v>

00:46:54.465 --> 00:47:14.865
<v Juan Martinez>Yeah, but I'm not forcing it on you. On you as the master, we don't, JVL doesn't dictate your operational policies and procedures. We're providing you a tool, a tool which you can say, dear locations, please don't ever call me for administrative password. We're not supporting that feature. Case closed.</v>

00:47:18.945 --> 00:47:21.985
<v Juan Martinez>The master has that relationship with his locations.</v>

00:47:19.025 --> 00:47:19.425
<v Andrei Klimovich>Ohh.</v>

00:47:26.785 --> 00:47:35.985
<v Andrei Klimovich>I do agree with you, but some beauty is being lost here. Some simplicity and beauty of this solution, which is fully automated.</v>

00:47:36.705 --> 00:47:37.265
<v Val Levitan>True.</v>

00:47:39.025 --> 00:47:43.065
<v Val Levitan>But is it lost because I killed the memory component?</v>

00:47:44.385 --> 00:47:57.025
<v Andrei Klimovich>Well, it's a very specific case. Only if the device itself is dead, then we lose all those transactions. If it's still present in the location, we consider that those pending transactions are still accessible.</v>

00:47:45.825 --> 00:47:46.385
<v Juan Martinez>Pardon me.</v>

00:47:58.145 --> 00:48:00.145
<v Val Levitan>Ohh, no, no, but no, but...</v>

00:47:58.385 --> 00:47:59.025
<v Andrei Klimovich>Well, it.</v>

00:48:02.385 --> 00:48:03.745
<v Val Levitan>Are we saying that...</v>

00:48:05.945 --> 00:48:07.745
<v Val Levitan>No, let me rephrase it. Hold on.</v>

00:48:09.025 --> 00:48:09.585
<v Val Levitan>Oh.</v>

00:48:11.345 --> 00:48:11.905
<v Val Levitan>Hold on.</v>

00:48:17.905 --> 00:48:21.025
<v Val Levitan>The very original thing was...</v>

00:48:21.905 --> 00:48:23.985
<v Val Levitan>We always print the ticket.</v>

00:48:25.665 --> 00:48:34.945
<v Val Levitan>Then I didn't like always printing the ticket. I said we should never print a ticket. We should grab this transaction and...</v>

00:48:35.985 --> 00:48:37.345
<v Val Levitan>Own the transaction.</v>

00:48:38.345 --> 00:48:49.985
<v Val Levitan>And then the last two days I pushed away from it by saying, no, we should always print the ticket because this is where we have the least footprint on the ticket.</v>

00:48:52.305 --> 00:48:52.705
<v Val Levitan>Uh...</v>

00:48:54.385 --> 00:48:57.945
<v Val Levitan>locations, infrastructure, however they were doing business.</v>

00:48:58.145 --> 00:48:58.465
<v Juan Martinez>Right.</v>

00:48:59.025 --> 00:49:00.945
<v Val Levitan>Is this is this a mistake?</v>

00:49:01.545 --> 00:49:14.065
<v Juan Martinez>No, Val, I was always in favor of printing the ticket because we never consulted the location of the master. What if they grab the tickets, staple them, fill out reports? We're denying them.</v>

00:49:09.425 --> 00:49:10.545
<v Val Levitan>I, I know, but...</v>

00:49:13.025 --> 00:49:22.465
<v Val Levitan>I know, I know, I know, I know, but I'm like a pendulum, I'm swinging back and forth, but is that the mistake?</v>

00:49:23.465 --> 00:49:37.665
<v Val Levitan>I know that you were in favor of printing ticket. I was also in favor of printing ticket. Then I became not in favor of printing ticket because I felt that grabbing the ticket and owning it.</v>

00:49:38.785 --> 00:49:42.945
<v Val Levitan>Offers, as Andrei says, certain charm of automation.</v>

00:49:46.065 --> 00:49:56.545
<v Andrei Klimovich>For me, they exist in parallel. One story is if we print ticket right away, and the other if we hold the transaction. So we still can print the ticket and hold the transaction.</v>

00:49:58.465 --> 00:50:01.265
<v Val Levitan>I don't understand this. Can you explain this? I don't understand.</v>

00:50:02.025 --> 00:50:11.745
<v Andrei Klimovich>So the pendulum that you've described was built around the solution if we print tickets right away, or we print tickets only when the transaction is finalized, right?</v>

00:50:11.345 --> 00:50:15.665
<v Val Levitan>No, no, no, or never print the ticket.</v>

00:50:13.265 --> 00:50:13.825
<v Andrei Klimovich>Okay.</v>

00:50:17.665 --> 00:50:21.425
<v Val Levitan>Always print the ticket, always print the ticket, or never print the ticket.</v>

00:50:17.905 --> 00:50:18.465
<v Juan Martinez>It was.</v>

00:50:22.385 --> 00:50:27.425
<v Juan Martinez>And the ticket should not be held. It should print in real time the way it does today.</v>

00:50:22.625 --> 00:50:22.745
<v Andrei Klimovich>Yeah.</v>

00:50:28.505 --> 00:50:37.025
<v Juan Martinez>Remember, we're saying we're, you're gonna keep your Mother Goose system the way it operates today. That's what we've been saying.</v>

00:50:35.545 --> 00:50:36.145
<v Val Levitan>That's.</v>

00:50:37.905 --> 00:50:46.225
<v Val Levitan>No, we have not been saying it. We know that this is 1 school of thinking. We have not been marketing this to an operator.</v>

00:50:47.585 --> 00:50:58.785
<v Val Levitan>So one school of thinking is, and it doesn't matter where I am polarized at, but one school of thinking always print the ticket, keep it in.</v>

00:51:00.465 --> 00:51:04.385
<v Val Levitan>in the same path as the location used to.</v>

00:51:06.145 --> 00:51:11.985
<v Val Levitan>Another school of thinking, never print a ticket, own the transaction right away.</v>

00:51:15.585 --> 00:51:20.785
<v Val Levitan>Everything gets sucked into IQ. Everything's kept in the memory of IQ.</v>

00:51:21.585 --> 00:51:34.785
<v Andrei Klimovich>Then there is an additional solution which came two days ago that if we cannot issue a card, we print a ticket. Do it in your old way, right? So that was like a...</v>

00:51:35.585 --> 00:51:52.065
<v Val Levitan>No, no, no. My switch came from realization that the current solution with MasterCard prepaid card is no go in Georgia.</v>

00:51:35.825 --> 00:51:36.465
<v Andrei Klimovich>Middle ground.</v>

00:51:58.945 --> 00:52:00.865
<v Andrei Klimovich>Not sure if I'm following you.</v>

00:51:59.185 --> 00:51:59.665
<v Val Levitan>Frolov.</v>

00:52:01.905 --> 00:52:17.345
<v Val Levitan>I am contemplating, I'm assuming, that players don't want to have a card and the location does not want to issue a card because it allows a player to walk away with the card and never come back.</v>

00:52:06.345 --> 00:52:06.585
<v Andrei Klimovich>Okay.</v>

00:52:18.265 --> 00:52:18.825
<v Andrei Klimovich>Mhm.</v>

00:52:19.825 --> 00:52:24.065
<v Val Levitan>And the player doesn't want to have a card because he'd rather have cash.</v>

00:52:25.185 --> 00:52:29.905
<v Val Levitan>So in my view, it pushes the location.</v>

00:52:31.665 --> 00:52:34.705
<v Val Levitan>to circumvent the legislative rule.</v>

00:52:35.745 --> 00:52:44.465
<v Juan Martinez>Well, and I would argue that only applies to the smaller guys. An operation like Kroger cannot afford to...</v>

00:52:42.865 --> 00:52:43.345
<v Val Levitan>What?</v>

00:52:44.145 --> 00:52:46.705
<v Val Levitan>Okay, but Kroger is 5% of the market.</v>

00:52:49.585 --> 00:52:56.945
<v Val Levitan>Most of these guys are pop and mom operations. They could be producing a lot of money. They could have multiple locations.</v>

00:52:57.265 --> 00:52:57.585
<v Juan Martinez>Sure.</v>

00:52:57.985 --> 00:53:12.225
<v Val Levitan>But, you know, it's a family-run business and it's an Indian clan that will always find a relative of somebody who they speak their native language and they will always circumvent the situation.</v>

00:53:13.185 --> 00:53:31.665
<v Juan Martinez>But also when I went with Felipe, we were never offered cash. Felipe was wearing a suit and they didn't recognize me. So 50% of the people who make stop by a gas station because they need gas, if I don't know you, I'm not going to give you cash because you could be a state agent.</v>

00:53:18.625 --> 00:53:19.105
<v Val Levitan>And.</v>

00:53:32.065 --> 00:53:34.625
<v Juan Martinez>So, we need to cover that other scenario.</v>

00:53:36.065 --> 00:53:51.585
<v Val Levitan>And in my view, the cards are offered, have offered a perfect solution for gray market. Hey, you have your card. Can I buy it at a discount? I'll give you cash. I'm exchanging cash for cash.</v>

00:53:51.985 --> 00:54:05.185
<v Juan Martinez>I 100% agree with you, but from the lottery perspective, they've convinced their bosses that this solution is safe. We can track cards, we can look at volumes, we've satisfied the risk.</v>

00:54:06.305 --> 00:54:07.905
<v Juan Martinez>But we know what's gonna happen.</v>

00:54:08.305 --> 00:54:18.225
<v Val Levitan>I know, but the reality is a reality. I mean, one bureaucrat could convince another bureaucrat all they want, but when it comes to the street, it will operate the way St. wants it.</v>

00:54:11.705 --> 00:54:12.065
<v Juan Martinez>Great.</v>

00:54:15.185 --> 00:54:15.585
<v Juan Martinez>Yes.</v>

00:54:19.105 --> 00:54:19.985
<v Juan Martinez>No, agreed.</v>

00:54:21.465 --> 00:54:23.985
<v Val Levitan>So, anyways, and for that reason...</v>

00:54:25.665 --> 00:54:30.945
<v Val Levitan>Then I switch to, hey, we don't want to know what's happening. We only...</v>

00:54:32.305 --> 00:54:43.585
<v Val Levitan>process the transaction that we process, the rest we just don't know. And it's better not to know than to keep account of what has transpired.</v>

00:54:44.545 --> 00:54:53.985
<v Val Levitan>And that's why I switched and I said, print your ******* tickets, do whatever you want, but we will only process the transactions that you put through us.</v>

00:54:56.385 --> 00:55:01.425
<v Val Levitan>And okay, so maybe it was a flaw. Maybe, maybe it's incorrect thinking.</v>

00:55:02.625 --> 00:55:06.145
<v Val Levitan>I am happy to, you know, paddle back.</v>

00:55:07.105 --> 00:55:27.625
<v Juan Martinez>But what part, Val? I mean, the printing of the ticket is a fallback to where now the location has a means by which to manually pay that player however they want. And that's what they've always done. If we don't give them the ticket, then we need a user interface.</v>

00:55:19.305 --> 00:55:19.425
<v Andrei Klimovich>Yeah.</v>

00:55:28.225 --> 00:55:36.145
<v Juan Martinez>on packs or I mean on Flex IQ that gives them all the data which we say we're now not keeping. So we're...</v>

00:55:36.225 --> 00:55:46.705
<v Val Levitan>No, no, no, no, hold on a second. We are now saying we're not keeping is the derivative of switching sides from always</v>

00:55:47.585 --> 00:56:07.425
<v Val Levitan>keeping possession of information or never keeping possession of information. If the original assumption of retraction was never to keep information, was erroneous, incorrect, then we can gladly keep all the information. It's not a technological</v>

00:56:07.905 --> 00:56:08.065
<v Val Levitan>Oh.</v>

00:56:10.985 --> 00:56:11.105
<v Val Levitan>Um...</v>

00:56:13.345 --> 00:56:13.825
<v Juan Martinez>Hurtle.</v>

00:56:14.065 --> 00:56:15.825
<v Val Levitan>Yeah, hurdle barrier.</v>

00:56:19.385 --> 00:56:25.665
<v Juan Martinez>Yeah, I think until we iron out all of our bugs, there's a lot of value in keeping that data in the cloud.</v>

00:56:20.065 --> 00:56:20.625
<v Val Levitan>Okay.</v>

00:56:26.905 --> 00:56:27.585
<v Juan Martinez>as a backup.</v>

00:56:26.945 --> 00:56:37.105
<v Val Levitan>I'm pretty tired and I just want to think it through overnight and let's try it again tomorrow. We need another session of brainstorming.</v>

00:56:32.705 --> 00:56:32.945
<v Juan Martinez>Sure.</v>

00:56:35.265 --> 00:56:35.665
<v Juan Martinez>Okay.</v>

00:56:38.145 --> 00:56:38.545
<v Juan Martinez>Okay.</v>

00:56:40.625 --> 00:56:43.585
<v Juan Martinez>When you can, let us know what your morning looks like, Val.</v>

00:56:40.705 --> 00:56:41.505
<v Val Levitan>Okay, let's.</v>

00:56:44.065 --> 00:56:47.265
<v Val Levitan>My morning is actually quite open tomorrow.</v>

00:56:51.705 --> 00:56:51.825
<v Andrei Klimovich>But.</v>

00:57:00.705 --> 00:57:04.145
<v Val Levitan>It's wide open. I can take a call at any time.</v>

00:57:05.425 --> 00:57:05.865
<v Juan Martinez>Okay.</v>

00:57:09.305 --> 00:57:14.185
<v Andrei Klimovich>So maybe we can use our call with you, Juan, and extend it to one hour.</v>

00:57:14.865 --> 00:57:17.705
<v Juan Martinez>Yep, the 8:30 or 9:00.</v>

00:57:18.505 --> 00:57:20.305
<v Val Levitan>Any, anytime, anytime.</v>

00:57:21.185 --> 00:57:21.265
<v Andrei Klimovich>Hey.</v>

00:57:21.225 --> 00:57:24.385
<v Juan Martinez>Hey, is one time better for you, Andrei?</v>

00:57:23.825 --> 00:57:24.705
<v Val Levitan>Makes no difference.</v>

00:57:27.745 --> 00:57:27.905
<v Andrei Klimovich>Mm.</v>

00:57:28.225 --> 00:57:30.705
<v Juan Martinez>Andrei, is 830 or 9 o'clock better for you?</v>

00:57:30.385 --> 00:57:33.505
<v Andrei Klimovich>Yeah, it sort of is beautiful, yeah, sure.</v>

00:57:33.185 --> 00:57:35.505
<v Juan Martinez>Okay, I'll send the invite out right now.</v>

00:57:40.625 --> 00:57:58.225
<v Andrei Klimovich>And may I ask you who want to drop this? What's the name? Yeah, the text. Oh my God, what's the name? I've just forgotten it. The transcript, sorry. Yeah, when it will be ready, sure.</v>

00:57:54.945 --> 00:57:56.465
<v Juan Martinez>The transcript, of course, yeah.</v>

00:57:58.385 --> 00:57:58.545
<v Juan Martinez>Sure.</v>

00:57:59.825 --> 00:58:01.345
<v Val Levitan>Okay, so what time tomorrow?</v>

00:58:01.945 --> 00:58:02.585
<v Juan Martinez>830.</v>

00:58:05.985 --> 00:58:07.985
<v Juan Martinez>Invite just sent. Oops.</v>

00:58:09.265 --> 00:58:09.665
<v Juan Martinez>Val.</v>

00:58:10.545 --> 00:58:10.865
<v Andrei Klimovich>Yeah.</v>

00:58:14.065 --> 00:58:17.745
<v Juan Martinez>Alright, Andrei, see you tomorrow morning. Ohh, there is time.</v>

00:58:17.185 --> 00:58:19.025
<v Andrei Klimovich>Yeah, see you tomorrow. Thank you, sir.</v>

00:58:20.265 --> 00:58:22.065
<v Val Levitan>Excuse me, 830 tomorrow, yeah?</v>

00:58:22.385 --> 00:58:23.825
<v Juan Martinez>Yeah, I just sent the invite. Yep.</v>

00:58:24.305 --> 00:58:25.905
<v Val Levitan>Okay, I'll see you tomorrow later.</v>

00:58:25.785 --> 00:58:26.865
<v Juan Martinez>All right, thanks, everybody.</v>

00:58:27.025 --> 00:58:27.425
<v Val Levitan>But.</v>
