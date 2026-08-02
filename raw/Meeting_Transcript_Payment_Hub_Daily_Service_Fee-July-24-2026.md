# Raw Transcript — Payment Hub Daily Service Fee Meeting
**Date:** July 24, 2026, 10:00 AM – 10:22 AM (Eastern)
**Summary note:** [[Meeting_Notes_Payment_Hub_Daily_Service_Fee-July-24-2026]]
---
WEBVTT

00:00:03.375 --> 00:00:05.575
<v Val Levitan>Discussing this daily fee, right?</v>

00:00:07.175 --> 00:00:07.815
<v Nathan Carver>Yes.</v>

00:00:08.375 --> 00:00:09.815
<v Val Levitan>And so...</v>

00:00:11.815 --> 00:00:23.975
<v Val Levitan>I remember hearing, so I am absent on a number of meetings and therefore I develop a knowledge gap.</v>

00:00:27.015 --> 00:00:30.775
<v Val Levitan>And so I remember hearing about daily fee.</v>

00:00:27.055 --> 00:00:27.335
<v Nathan Carver>Mm.</v>

00:00:27.495 --> 00:00:27.735
<v Andrei Klimovich>So.</v>

00:00:33.415 --> 00:00:53.255
<v Val Levitan>I remember making a mental note of it, but I don't remember what I did with that mental note and how far it went, and I kind of drawing a blank on this. So for my benefit, can we discuss what daily fee is, how it may apply, and what do we want to do with it?</v>

00:00:37.655 --> 00:00:37.775
<v Andrei Klimovich>Yeah.</v>

00:00:39.415 --> 00:00:39.655
<v Andrei Klimovich>Shh.</v>

00:00:53.735 --> 00:01:07.015
<v Val Levitan>because I do not want to give up a daily fee enough. And if I have an opportunity, I'd like to apply it properly and cleverly to...</v>

00:01:09.815 --> 00:01:13.495
<v Val Levitan>secure our reoccurring revenue and possibly offer.</v>

00:01:15.255 --> 00:01:19.095
<v Val Levitan>Maybe daily fee-based.</v>

00:01:22.375 --> 00:01:27.655
<v Val Levitan>equipment sale versus straight out sale.</v>

00:01:28.615 --> 00:01:28.775
<v Nathan Carver>Mm.</v>

00:01:30.455 --> 00:01:42.615
<v Val Levitan>So can somebody give me calls notes on this daily fee and its point of origination and how it could be applied?</v>

00:01:38.455 --> 00:01:38.575
<v Andrei Klimovich>Yeah.</v>

00:01:43.775 --> 00:01:52.375
<v Val Levitan>so I could refresh my memory and eliminate the what I consider knowledge gap.</v>

00:01:55.815 --> 00:01:56.135
<v Nathan Carver>Um...</v>

00:01:57.455 --> 00:02:04.775
<v Nathan Carver>Yes, I don't know, Juan, if you have any notes on that. I don't have a lot other than this is a...</v>

00:02:05.855 --> 00:02:12.215
<v Nathan Carver>a configuration in Payment Hub that can be assigned to a customer location.</v>

00:02:13.575 --> 00:02:16.855
<v Nathan Carver>and it flows through the billing.</v>

00:02:18.935 --> 00:02:24.615
<v Nathan Carver>So whatever we assign that fee, whenever an invoice is generated, that fee will get assigned to the invoice.</v>

00:02:25.975 --> 00:02:28.935
<v Juan Martinez>So I popped up your response to me.</v>

00:02:26.495 --> 00:02:28.655
<v Nathan Carver>Um, that's as much as I know about it.</v>

00:02:30.215 --> 00:02:31.815
<v Nathan Carver>Sorry, go ahead.</v>

00:02:32.255 --> 00:02:37.415
<v Juan Martinez>No, so I just put your response to me on screen so everybody can see it.</v>

00:02:37.295 --> 00:02:37.415
<v Nathan Carver>Yes.</v>

00:02:39.415 --> 00:02:59.135
<v Juan Martinez>Yeah, so, you know, we thought that, you know, we would have up charges for additional services, much like we talked about yesterday, Val, when Smith and Port got deployed, enhanced performance, you know, enhanced reporting, all of that. So I believe all of this.</v>

00:02:59.255 --> 00:03:02.295
<v Juan Martinez>falls under that possible daily fee structure.</v>

00:03:02.215 --> 00:03:02.335
<v Andrei Klimovich>Yes.</v>

00:03:03.335 --> 00:03:21.495
<v Val Levitan>OK, so let me understand. Let me regurgitate this and say it in my statement. So I think what we're talking about here is that we foresee a possible daily fee collected. There is no direct.</v>

00:03:22.775 --> 00:03:29.255
<v Val Levitan>application right now, but because we are developing an automated</v>

00:03:31.495 --> 00:03:31.575
<v Val Levitan>Ohh...</v>

00:03:33.975 --> 00:03:39.015
<v Val Levitan>I guess, automated accounting, we want to...</v>

00:03:40.295 --> 00:03:48.935
<v Val Levitan>secure a GL account for it and we want to test that this fee can be.</v>

00:03:50.455 --> 00:04:14.535
<v Val Levitan>elected in a user setup screen and then passed all the way to GL accounting in Business Central and that's traceable. So if we say, okay, the business deal is to charge a daily fee, we nominate the daily fee being $5 in this case.</v>

00:04:10.095 --> 00:04:10.455
<v Nathan Carver>Yes.</v>

00:04:14.975 --> 00:04:15.175
<v Nathan Carver>Yeah.</v>

00:04:15.095 --> 00:04:20.615
<v Val Levitan>and we see it registered in the GL account in MSBC.</v>

00:04:24.295 --> 00:04:44.855
<v Juan Martinez>What you said is accurate. My question still remains. Just the naming convention, Nathan, is throwing me off. You know, you labeled it ACH service fee revenue. And what I don't see on this chart are the other fees here of the wallet that let's say the customer has</v>

00:04:33.495 --> 00:04:33.615
<v Val Levitan>Yeah.</v>

00:04:45.815 --> 00:05:00.775
<v Juan Martinez>sufficient funds and he balances a payment on us. There's a fee for that. Does that go under this all-inclusive ACH fee or are we still missing those other banking fees?</v>

00:04:59.415 --> 00:04:59.895
<v Nathan Carver>I think.</v>

00:05:01.495 --> 00:05:03.175
<v Nathan Carver>I think we'll need those.</v>

00:05:04.255 --> 00:05:07.015
<v Nathan Carver>Well, I don't know. I think accounting.</v>

00:05:08.215 --> 00:05:10.215
<v Nathan Carver>can give us a better answer there.</v>

00:05:11.735 --> 00:05:22.935
<v Nathan Carver>But yes, we those are the only codes I have right now for location billing. So if we need other fee codes, then we need to create them. So like you said, if they.</v>

00:05:22.455 --> 00:05:33.015
<v Val Levitan>And, and there are, and and there are other fees, like wallet has a fee, rejection income has a fee, so yeah, we want it to be.</v>

00:05:34.375 --> 00:05:35.175
<v Val Levitan>Ohh.</v>

00:05:36.255 --> 00:05:42.695
<v Val Levitan>Transparent, and then we wanna we wanna carry it from charge to G.L.</v>

00:05:38.055 --> 00:05:38.375
<v Nathan Carver>Yeah.</v>

00:05:39.535 --> 00:05:39.655
<v Andrei Klimovich>Yes.</v>

00:05:45.095 --> 00:05:45.335
<v Juan Martinez>Yeah.</v>

00:05:46.055 --> 00:06:06.135
<v Val Levitan>That answers, that's my answer to Juan's question. And as far as daily revenue, I kind of gave myself an answer. Yes, we would like to have a line for that. So in a nutshell, we're missing other fees that we already know.</v>

00:05:53.055 --> 00:05:53.095
<v Andrei Klimovich>I.</v>

00:06:06.535 --> 00:06:10.055
<v Val Levitan>Off, and in order for us not to...</v>

00:06:13.095 --> 00:06:26.215
<v Val Levitan>Go back into redesign again. I suggest maybe adding two reserved lines for potential fees that we may have missed and just allocating proper GL accounts to it.</v>

00:06:28.375 --> 00:06:32.695
<v Juan Martinez>Was it just two though, Val? I thought there was several possible fees.</v>

00:06:33.015 --> 00:06:41.975
<v Val Levitan>No, no, defining all the fields that we missed, plus in addition to it, reserving two additional fields just in case we miss something.</v>

00:06:38.295 --> 00:06:38.695
<v Juan Martinez>Okay.</v>

00:06:42.295 --> 00:06:42.495
<v Nathan Carver>Yeah.</v>

00:06:42.855 --> 00:06:44.215
<v Juan Martinez>Okay, that makes sense.</v>

00:06:50.455 --> 00:06:53.095
<v Val Levitan>So is that a clear? Is that a clear instruction?</v>

00:06:50.535 --> 00:06:51.375
<v Juan Martinez>Something funny.</v>

00:06:53.735 --> 00:06:54.855
<v Juan Martinez>It's clear to me.</v>

00:06:55.815 --> 00:07:02.175
<v Nathan Carver>So, add these new codes, add codes to cover these potential fees, and...</v>

00:07:03.015 --> 00:07:23.815
<v Val Levitan>Add codes to the fees that we already know exist, like duala, like income, cancellation fee, or rejection fee, whatever they call it. I don't know how many fields are there, but add those fields that we already know of, and in addition to it, reserve two more fields just in case we have missed something.</v>

00:07:07.495 --> 00:07:07.655
<v Nathan Carver>Mm.</v>

00:07:12.535 --> 00:07:13.095
<v Nathan Carver>Yes.</v>

00:07:25.255 --> 00:07:25.935
<v Nathan Carver>Okay.</v>

00:07:26.775 --> 00:07:34.535
<v Juan Martinez>And Nathan, could we edit the account name for 41421 and remove AC8?</v>

00:07:32.775 --> 00:07:34.375
<v Nathan Carver>Yeah, yeah, yeah.</v>

00:07:35.655 --> 00:07:38.455
<v Nathan Carver>Yep, that's easy enough. We can.</v>

00:07:37.895 --> 00:07:38.135
<v Juan Martinez>Hey.</v>

00:07:40.255 --> 00:07:41.415
<v Nathan Carver>whatever it needs to be.</v>

00:07:43.655 --> 00:08:01.655
<v Juan Martinez>I mean, I'll go dig back through all my notes and exchanges with the wallet to at least start to put a list together and Nathan to make sure it matches what you may have with all of the other banking related fees regarded to, you know, failed transfers or failed payments.</v>

00:08:02.335 --> 00:08:04.255
<v Nathan Carver>Okay, all right, that sounds good.</v>

00:08:10.535 --> 00:08:12.615
<v Juan Martinez>Short and sweet, I think it's clear to me.</v>

00:08:14.895 --> 00:08:29.735
<v Andrei Klimovich>So, there was another question related to the logic of issuing invoices to our masters, and a specific case when there are no transactions per report day, like...</v>

00:08:31.255 --> 00:08:35.415
<v Andrei Klimovich>It was a really, really slow day. No cars issued.</v>

00:08:36.575 --> 00:08:43.175
<v Andrei Klimovich>Shall we anyways issue an empty invoice, or we skip it?</v>

00:08:43.015 --> 00:08:43.495
<v Juan Martinez>Yes.</v>

00:08:44.375 --> 00:08:52.295
<v Juan Martinez>I think we should, A, reminds the customer of all the potential sort of fees. You know, if you see an invoice and it says...</v>

00:08:53.575 --> 00:09:08.455
<v Juan Martinez>insufficient fund fee. That's a great way to call for them to make sure they've got money in their account, even though it's going to say zero. I just think it's a good visual reminder to, you know, make sure they plan properly to avoid the miscellaneous fees.</v>

00:09:08.935 --> 00:09:10.455
<v Val Levitan>Yeah, I'm in full support of it.</v>

00:09:11.415 --> 00:09:11.895
<v Nathan Carver>Okay.</v>

00:09:11.415 --> 00:09:12.015
<v Andrei Klimovich>Mm-hmm.</v>

00:09:13.255 --> 00:09:25.335
<v Nathan Carver>So, we'll have invoices generated if there is a fee of any kind. So, if they, if they owe insufficient funds, they'll get that invoice. If they have a daily fee, they'll get that. That'll be on the invoice too.</v>

00:09:26.535 --> 00:09:30.215
<v Juan Martinez>Yeah, correct. All with zeros if there's zero for that day.</v>

00:09:28.335 --> 00:09:28.735
<v Nathan Carver>Okay.</v>

00:09:30.855 --> 00:09:31.895
<v Val Levitan>Basically, what the...</v>

00:09:31.015 --> 00:09:31.895
<v Nathan Carver>Okay, so only in the...</v>

00:09:33.575 --> 00:09:34.055
<v Val Levitan>Go ahead.</v>

00:09:33.895 --> 00:09:43.975
<v Nathan Carver>Sorry. Yeah, only in the event of there are no fees and no redeemed cards. So there'd be literally nothing to charge them.</v>

00:09:45.175 --> 00:09:57.415
<v Nathan Carver>at that point, then there would be no invoice because there would be no, obviously there'd be no Dwala transaction. So that would only be in the case of the customer doesn't have a daily fee and has no other fees to pay.</v>

00:09:57.495 --> 00:10:13.175
<v Val Levitan>I don't know. I feel that since we're sending invoices by e-mail and not by physical mail, we should send it on a regular basis for as long as account is open, regardless whether the charge is 0 or something.</v>

00:10:13.495 --> 00:10:15.415
<v Juan Martinez>I, I, that's what I agree.</v>

00:10:13.495 --> 00:10:17.135
<v Nathan Carver>Okay, so there'll still be some reporting. Okay.</v>

00:10:15.615 --> 00:10:22.855
<v Andrei Klimovich>Yeah, I support it. It's transparent, it's consistent, yeah.</v>

00:10:22.615 --> 00:10:23.015
<v Juan Martinez>Yep.</v>

00:10:22.855 --> 00:10:30.375
<v Val Levitan>Yeah, and that's a good way for people to reconcile, make sure that they haven't lost it in a rejected box somewhere.</v>

00:10:31.335 --> 00:10:36.695
<v Nathan Carver>Okay, so we would push that through MSBC as well. There would just be a 0 invoice in there.</v>

00:10:37.255 --> 00:10:41.735
<v Val Levitan>Yeah, yeah, we would, and and it's a it's a good reconciliation for us as well.</v>

00:10:37.575 --> 00:10:38.535
<v Nathan Carver>Or that, okay.</v>

00:10:38.655 --> 00:10:38.775
<v Andrei Klimovich>Yeah.</v>

00:10:42.215 --> 00:10:43.575
<v Nathan Carver>Okay, sounds good.</v>

00:10:42.375 --> 00:10:42.735
<v Juan Martinez>Yeah.</v>

00:10:44.775 --> 00:10:57.975
<v Juan Martinez>And we're, Nathan, we're talking about one consolidated invoice that would contain transactions or cards if they were done, plus all the fees, usually at 0 per day. Okay.</v>

00:10:54.855 --> 00:10:55.415
<v Nathan Carver>Correct.</v>

00:10:57.975 --> 00:10:58.855
<v Nathan Carver>Correct. Yep.</v>

00:11:02.055 --> 00:11:19.175
<v Andrei Klimovich>So, and the last clarification regarding this 41 42 one, which is currently called ACH service fee revenue. So as far as I understand right now, it exists in location settings in payment hub and we simply put zero over there.</v>

00:11:20.135 --> 00:11:26.455
<v Andrei Klimovich>So, um, it's, as far as I said, it's already implemented on a on this level.</v>

00:11:27.735 --> 00:11:38.615
<v Andrei Klimovich>So we just need to make sure until it's decided in any other way, we just need to make sure when we create a new location, we just need to put 0 into this field.</v>

00:11:39.655 --> 00:11:45.015
<v Juan Martinez>Yeah, that zero should be a default and then we have to activate it if a fee applies. Yep.</v>

00:11:48.295 --> 00:11:50.055
<v Nathan Carver>Okay, yeah, so.</v>

00:11:48.695 --> 00:11:49.175
<v Juan Martinez>Definitely.</v>

00:11:52.695 --> 00:12:00.695
<v Nathan Carver>That will be on, we'll have to make sure Pavel knows that, because that'll be on there. His engineers to make sure it's designed that way.</v>

00:11:58.935 --> 00:11:59.415
<v Andrei Klimovich>That's it.</v>

00:12:01.095 --> 00:12:01.175
<v Andrei Klimovich>The.</v>

00:12:01.415 --> 00:12:01.655
<v Juan Martinez>For.</v>

00:12:04.055 --> 00:12:04.455
<v Juan Martinez>Reed.</v>

00:12:12.695 --> 00:12:15.095
<v Andrei Klimovich>I think we are covered. That's it.</v>

00:12:14.855 --> 00:12:15.255
<v Juan Martinez>Yeah.</v>

00:12:15.815 --> 00:12:16.935
<v Nathan Carver>Yep, I think.</v>

00:12:16.375 --> 00:12:22.655
<v Juan Martinez>Um, Val, I think the fees might be on the final Diwala contract.</v>

00:12:23.015 --> 00:12:23.095
<v Andrei Klimovich>You</v>

00:12:23.695 --> 00:12:28.855
<v Juan Martinez>Would it be possible to dig that up and just send that table with the fees?</v>

00:12:29.575 --> 00:12:31.815
<v Val Levitan>Can you ask the wallet to send the table?</v>

00:12:32.295 --> 00:12:32.695
<v Juan Martinez>Sure.</v>

00:12:35.655 --> 00:12:39.415
<v Val Levitan>Okay, thank you. And I recommend the same for income.</v>

00:12:40.535 --> 00:12:40.935
<v Juan Martinez>K.</v>

00:12:44.695 --> 00:12:45.335
<v Juan Martinez>Pick that.</v>

00:12:45.095 --> 00:12:46.615
<v Val Levitan>By, by the way...</v>

00:12:47.775 --> 00:12:49.735
<v Val Levitan>Are there any fees from our bank?</v>

00:12:54.615 --> 00:12:57.895
<v Val Levitan>Okay, something that I need to think about. I don't know.</v>

00:12:55.655 --> 00:12:56.135
<v Nathan Carver>Alright.</v>

00:13:00.775 --> 00:13:01.495
<v Nathan Carver>Yeah, I don't.</v>

00:13:03.615 --> 00:13:09.255
<v Nathan Carver>I don't know if they would go through location billing or through the payment hub, but we may want to have them on there.</v>

00:13:08.135 --> 00:13:08.775
<v Val Levitan>Yeah.</v>

00:13:10.055 --> 00:13:12.375
<v Val Levitan>Yeah, probably it's our cost of doing business.</v>

00:13:14.375 --> 00:13:16.455
<v Val Levitan>It's not a direct charge.</v>

00:13:18.695 --> 00:13:20.855
<v Val Levitan>OK, clear. Thank you very much, everyone.</v>

00:13:21.495 --> 00:13:23.055
<v Nathan Carver>Alright, it's all.</v>

00:13:21.735 --> 00:13:23.175
<v Juan Martinez>All right. Thanks, everybody.</v>

00:13:22.935 --> 00:13:24.135
<v Andrei Klimovich>Thank you. Bye bye.</v>

00:13:23.735 --> 00:13:24.215
<v Val Levitan>Bye.</v>
