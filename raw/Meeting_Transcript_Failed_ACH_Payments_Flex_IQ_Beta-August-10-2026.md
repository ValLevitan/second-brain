# Raw Transcript — Failed ACH payments: business needs and approach
**Date:** August 10, 2026, 8:30–9:32 AM Eastern
**Summary note:** [[Meeting_Notes_Failed_ACH_Payments_Flex_IQ_Beta-August-10-2026]]
---
WEBVTT

00:00:04.249 --> 00:00:05.369
<v Nathan Carver>The question came up.</v>

00:00:06.329 --> 00:00:06.369
<v Nathan Carver>Uh...</v>

00:00:07.689 --> 00:00:16.089
<v Nathan Carver>recently on how to handle retry payments within payment hub. And this would be for...</v>

00:00:17.209 --> 00:00:22.649
<v Nathan Carver>We invoice the location, we debit their account, and we get insufficient funds.</v>

00:00:24.729 --> 00:00:38.649
<v Nathan Carver>So just a very specific code. This is specifically in Naqsh, this is an R01 code. There is an R09 that's similar, but it has a little bit of different meaning. Oh, here's Val.</v>

00:00:40.169 --> 00:00:41.369
<v Val Levitan>Hey guys, good morning.</v>

00:00:41.369 --> 00:00:41.929
<v Nathan Carver>Igor.</v>

00:00:41.769 --> 00:00:42.009
<v Pavel Frolov>Val.</v>

00:00:42.969 --> 00:00:43.449
<v Andrei Klimovich>The Wyk.</v>

00:00:44.729 --> 00:00:45.289
<v Nathan Carver>Van.</v>

00:00:46.529 --> 00:01:06.329
<v Nathan Carver>So, we just just started, Val, so real quick, the question recently came up on retry or what's Naqsh refers to as re-initiation of payments. This would be we invoice at location, we debit their account, we get insufficient funds.</v>

00:01:06.369 --> 00:01:08.729
<v Nathan Carver>which is in R01 code.</v>

00:01:10.889 --> 00:01:19.369
<v Nathan Carver>Naqsh has regulations on how to retry that payment or reinitiate it is the actual term.</v>

00:01:21.289 --> 00:01:23.289
<v Nathan Carver>The caveat to that is...</v>

00:01:24.729 --> 00:01:37.769
<v Nathan Carver>Because we use DWALA, JVL doesn't actually initiate the transfers. DWALA initiates the transfers. So they treat all initiation as a new transfer.</v>

00:01:38.809 --> 00:01:40.249
<v Juan Martinez>Or re-initiations.</v>

00:01:41.849 --> 00:01:52.729
<v Nathan Carver>Correct. So we can't, according to the Naqsh regulations, we don't, we aren't capable of re-initiating. So the only difference is</v>

00:01:54.729 --> 00:02:03.529
<v Nathan Carver>It's not a different transaction. It's just an ACH transaction stamped with a retry payment.</v>

00:02:04.889 --> 00:02:09.049
<v Nathan Carver>code, just a text that you put in the field. That's all Naqsh requires.</v>

00:02:11.609 --> 00:02:18.969
<v Nathan Carver>So I asked, I did reach out to Nancy and asked her about that. She said they don't reinitiate payments, but if we...</v>

00:02:20.089 --> 00:02:23.689
<v Nathan Carver>resubmit that payment, they will run it through again as a new transaction.</v>

00:02:26.569 --> 00:02:27.689
<v Nathan Carver>So, the question...</v>

00:02:29.049 --> 00:02:34.729
<v Nathan Carver>to the business side is the current flow is we</v>

00:02:35.849 --> 00:02:36.889
<v Nathan Carver>Initiate A debit.</v>

00:02:38.009 --> 00:02:46.169
<v Nathan Carver>They would, let's say they have insist funds and we get a code. The proposal is, because right now we don't reinitiate. It goes straight to.</v>

00:02:47.689 --> 00:02:51.369
<v Nathan Carver>Um, what would be, you know, pay with their credit card?</v>

00:02:52.489 --> 00:02:54.409
<v Nathan Carver>So, the proposed flow would be...</v>

00:02:55.769 --> 00:03:00.809
<v Nathan Carver>We initiate the debit, we get the R1 insufficient funds.</v>

00:03:01.929 --> 00:03:08.729
<v Nathan Carver>So then Payment Hub would flag that customer as a verify balance.</v>

00:03:09.729 --> 00:03:13.369
<v Nathan Carver>And then that transaction will get queued up again for the next day.</v>

00:03:14.409 --> 00:03:29.849
<v Nathan Carver>But we would run the verify balance through, is it Stripe? I forget who's, who we go through. So we would run the verify balance before running that, before initiating the debit.</v>

00:03:31.209 --> 00:03:39.049
<v Nathan Carver>The caveat then is going to be, because it's the next day, we most likely have a second invoice from that customer.</v>

00:03:40.249 --> 00:03:42.009
<v Nathan Carver>So we would have two invoices.</v>

00:03:43.369 --> 00:03:43.609
<v Nathan Carver>Um...</v>

00:03:45.049 --> 00:03:49.769
<v Nathan Carver>And they would have to be initiated separately because according to Naqsh, we have to match.</v>

00:03:52.009 --> 00:03:55.849
<v Nathan Carver>the invoice that we're re-initiating, we would have to match that invoice.</v>

00:03:56.729 --> 00:04:01.769
<v Nathan Carver>I think there's other things we can do from a business side, but that's the general flow.</v>

00:04:02.969 --> 00:04:04.409
<v Nathan Carver>that we're thinking for this.</v>

00:04:05.609 --> 00:04:25.769
<v Juan Martinez>So a couple questions, Nathan. We had previously discussed doing a daily account balance check with every customer at 8 AM, giving them enough time for us to get the results and send them a courtesy e-mail.</v>

00:04:26.009 --> 00:04:40.489
<v Juan Martinez>saying, hey, your account balance shows $100. We're about to invoice you for $2,000, and they can just jump on their phone and top off their account. Is that still not something in the works?</v>

00:04:42.889 --> 00:04:48.569
<v Nathan Carver>So we don't currently check. We can do balance checks. It's not active.</v>

00:04:50.809 --> 00:05:03.289
<v Nathan Carver>A lot of this was, I think, deferred until after this initial alpha testing that we had planned. So we don't do that, but yes, we can. We can do that.</v>

00:05:03.609 --> 00:05:06.249
<v Juan Martinez>And is there a cost to do the balance check?</v>

00:05:06.809 --> 00:05:09.609
<v Nathan Carver>Yes, there is a little cost.</v>

00:05:07.209 --> 00:05:09.449
<v Val Levitan>Minimal, minimal, minimal.</v>

00:05:10.569 --> 00:05:11.529
<v Juan Martinez>Okay, okay.</v>

00:05:11.529 --> 00:05:12.889
<v Val Levitan>Negligible.</v>

00:05:14.329 --> 00:05:20.729
<v Val Levitan>But along the same lines as Juan is asking, I also recall us thinking about...</v>

00:05:22.569 --> 00:05:32.489
<v Val Levitan>And especially in light that we are dealing not really directly with the location per se, but with the master operator.</v>

00:05:38.169 --> 00:05:38.889
<v Val Levitan>Is it?</v>

00:05:39.769 --> 00:05:44.409
<v Val Levitan>Is there a possibility for us to charge?</v>

00:05:46.009 --> 00:05:48.409
<v Val Levitan>Master Operator Credit Card.</v>

00:05:50.489 --> 00:05:52.329
<v Val Levitan>for this transaction.</v>

00:05:53.929 --> 00:06:00.169
<v Val Levitan>And I'm asking, I'm asking a question from a technical perspective, as well as...</v>

00:05:54.729 --> 00:05:55.049
<v Nathan Carver>Rama.</v>

00:06:01.289 --> 00:06:12.889
<v Val Levitan>just a business perspective. Maybe my question is addressed to Andrei and Juan on one side and then to Nathan from the other side. So I don't know the answer to that question.</v>

00:06:14.649 --> 00:06:33.129
<v Juan Martinez>So my question is, with today's banking apps, and you have to assume everybody has them, you can instantly move money around in a matter of seconds. So getting or requiring their credit card should be like the last resort, obviously.</v>

00:06:32.409 --> 00:06:36.009
<v Val Levitan>Yes, it is. Yes, yes. As a last resort, yes.</v>

00:06:38.009 --> 00:06:38.209
<v Juan Martinez>Okay.</v>

00:06:38.969 --> 00:06:47.889
<v Val Levitan>But does this, but does this even a valid solution for us? And I'm asking a question from a perspective of...</v>

00:06:39.369 --> 00:06:40.889
<v Nathan Carver>Um, technically, yes, we can.</v>

00:06:49.849 --> 00:06:56.809
<v Val Levitan>I guess it's a multi-faceted question. Should we even contact a master operator, say, hey.</v>

00:06:58.969 --> 00:07:04.249
<v Val Levitan>Mr. Smith, your location, XYZ, is out of funds.</v>

00:07:05.969 --> 00:07:21.529
<v Val Levitan>What would you like us to do? Reject A transaction? Will you transfer money? Can I charge your credit card? I mean, not in this fashion, obviously, but somehow interactively get to that point. Is it even ethical for us to</v>

00:07:15.849 --> 00:07:16.169
<v Juan Martinez>Yeah.</v>

00:07:22.809 --> 00:07:30.969
<v Val Levitan>revert to master operator versus the location itself. I don't know the intricacies of...</v>

00:07:32.969 --> 00:07:35.849
<v Val Levitan>Yeah, I'm asking a question that really I'm not suggesting anything.</v>

00:07:36.569 --> 00:07:54.249
<v Juan Martinez>Yeah, Val, I think that that's a case-by-case basis where, you know, if it's one of those top, top masters, you know, he wants to control his entire business and all dealings are through him because he doesn't want us going to his customer, which is the location.</v>

00:07:56.089 --> 00:08:20.049
<v Juan Martinez>We sort of, they're not going to tell us, but you know, the master collects the money from the machine and it's split, you know, 40% to him, 40% to the location. So somebody controls the 40% and that could easily cover the day's transactions due to us. So it's almost on a case-by-case basis to understand</v>

00:08:20.569 --> 00:08:27.769
<v Juan Martinez>who our customer actually is going to be for each Flex IQ installation.</v>

00:08:28.329 --> 00:08:29.049
<v Val Levitan>Well...</v>

00:08:30.329 --> 00:08:40.009
<v Val Levitan>I mean, yes and no. I mean, who are we selling to? It seems like we're not even going to a location. We're selling actually to a master operator.</v>

00:08:41.049 --> 00:08:53.689
<v Juan Martinez>Correct. But I mean, Andrei, we don't know if that master says, yeah, you're selling it to me, but in terms of the payments, you know, the location's going to pay you directly. I don't know if that's how it works.</v>

00:08:57.129 --> 00:09:04.809
<v Andrei Klimovich>So while talking to AKS, I got the initial feeling and understanding that.</v>

00:09:06.489 --> 00:09:12.009
<v Andrei Klimovich>They will use locations, bank accounts, and they are not.</v>

00:09:13.209 --> 00:09:16.729
<v Andrei Klimovich>They're not going to be involved into any payments.</v>

00:09:18.929 --> 00:09:22.489
<v Andrei Klimovich>From location to JVL, so they didn't want to be part of it.</v>

00:09:23.449 --> 00:09:28.969
<v Juan Martinez>Right, so as I finish up all of our sales agreements and all that,</v>

00:09:30.409 --> 00:09:46.409
<v Juan Martinez>Legally, then, if we've entered into a contract with the master, he owes us the money and we can't go after the location who, according to the master, is going to pay us. It's very, very dangerous territory.</v>

00:09:47.009 --> 00:09:47.529
<v Andrei Klimovich>Mhm.</v>

00:09:52.169 --> 00:09:56.329
<v Nathan Carver>Who's signing up their account in Payment Hub then to...</v>

00:09:57.529 --> 00:10:01.929
<v Nathan Carver>with Dwala, right? Who's creating the wallet for us to debit? Is that?</v>

00:10:03.369 --> 00:10:04.169
<v Andrei Klimovich>Yeah, so...</v>

00:10:03.689 --> 00:10:07.649
<v Nathan Carver>The location going in and signing up? Or the master signing them up?</v>

00:10:08.009 --> 00:10:09.009
<v Val Levitan>No.</v>

00:10:09.929 --> 00:10:09.969
<v Val Levitan>Oh.</v>

00:10:12.729 --> 00:10:13.849
<v Val Levitan>That's a good question.</v>

00:10:14.329 --> 00:10:27.369
<v Andrei Klimovich>It's right now designed in the ways that there is a master who owns multiple locations and actually only master has access to dweller and played account assigning.</v>

00:10:28.529 --> 00:10:39.529
<v Andrei Klimovich>which is maybe not a proper way to handle it. Because if it's locations account, I don't think that they will share it with master to.</v>

00:10:40.409 --> 00:10:41.129
<v Andrei Klimovich>To input.</v>

00:10:42.969 --> 00:10:43.449
<v Andrei Klimovich>Ohh.</v>

00:10:45.129 --> 00:11:07.649
<v Juan Martinez>I mean, but remember, these guys do have a financial business relationship. The master and location owe each other money. And you know, they're probably doing transfers today, whether it's the same account or not. But my fear is the location can argue. I never signed a contract with JVL.</v>

00:11:07.769 --> 00:11:12.409
<v Juan Martinez>I don't owe you anything. Go talk to the master. And then, of course, they would win.</v>

00:11:13.609 --> 00:11:32.809
<v Andrei Klimovich>Well, with this approach, the only way for this system to work is that master have to assign, masters have to assign a bank account per each location. And we don't know what kind of bank account it is. Is it master's account or?</v>

00:11:33.129 --> 00:11:40.489
<v Andrei Klimovich>They're in a really close relations with location and they shared their bank account by some reason, whatever.</v>

00:11:41.609 --> 00:11:48.249
<v Andrei Klimovich>But if we have an agreement with master, it's master who we shall actually invoice.</v>

00:11:52.889 --> 00:11:59.689
<v Juan Martinez>But by your own statement where he said, oh no, the all the billing goes to the location that that's you know</v>

00:12:00.729 --> 00:12:13.129
<v Andrei Klimovich>It's well, if they want us to build location, we need to have an agreement with location, or at least the location, or at least the location should give consent to the wallet to charge their bank account.</v>

00:12:06.289 --> 00:12:06.729
<v Juan Martinez>Correct.</v>

00:12:06.329 --> 00:12:06.769
<v Nathan Carver>Correct.</v>

00:12:13.609 --> 00:12:14.169
<v Juan Martinez>Yes.</v>

00:12:13.689 --> 00:12:14.249
<v Nathan Carver>Correct.</v>

00:12:16.969 --> 00:12:21.129
<v Nathan Carver>Yeah, it would be very easy for the location to say, we didn't authorize this.</v>

00:12:21.689 --> 00:12:22.089
<v Andrei Klimovich>Yeah.</v>

00:12:21.969 --> 00:12:22.169
<v Juan Martinez>Yep.</v>

00:12:22.729 --> 00:12:23.369
<v Nathan Carver>And.</v>

00:12:24.649 --> 00:12:26.569
<v Andrei Klimovich>OK, so I am.</v>

00:12:28.649 --> 00:12:35.769
<v Andrei Klimovich>I've sent you a message, Juan, in the morning today is that probably we need to get to AKS, for example.</v>

00:12:36.169 --> 00:12:36.649
<v Juan Martinez>Yes.</v>

00:12:38.849 --> 00:12:43.769
<v Andrei Klimovich>Unwind it into more into more details to understand how it shall work.</v>

00:12:42.009 --> 00:12:42.809
<v Juan Martinez>Yes, yes.</v>

00:12:44.529 --> 00:12:45.129
<v Juan Martinez>Definitely.</v>

00:12:56.489 --> 00:13:00.729
<v Nathan Carver>Okay, so the current state then is kind of now asking the question of...</v>

00:13:02.169 --> 00:13:07.609
<v Nathan Carver>Who's entering the agreement with Dwala and JBL to move the money?</v>

00:13:09.689 --> 00:13:10.329
<v Nathan Carver>And then...</v>

00:13:10.009 --> 00:13:15.209
<v Val Levitan>I think this, I think this agreement must be between the location and JVL.</v>

00:13:11.489 --> 00:13:11.609
<v Nathan Carver>Okay.</v>

00:13:16.329 --> 00:13:19.049
<v Nathan Carver>Correct. Whoever's putting their bank account in there.</v>

00:13:19.609 --> 00:13:26.169
<v Val Levitan>I just think that there is a cute, cute way here.</v>

00:13:27.689 --> 00:13:31.529
<v Val Levitan>to put an operator as a guarantor.</v>

00:13:36.409 --> 00:13:47.929
<v Juan Martinez>I mean, we are contracting with the operator for the hardware side of things. It's the ambiguity of the banking side of things.</v>

00:13:50.889 --> 00:14:09.729
<v Juan Martinez>Yeah, because the master may have that relationship with the location today. They already may share a banking account where the location moves money there, and that's what the master intends to give us. But based on what Andrei said, it sounded like AKS, this particular customer, wants us to deal</v>

00:14:10.009 --> 00:14:13.449
<v Juan Martinez>Directly with the location for for funding.</v>

00:14:14.289 --> 00:14:29.369
<v Juan Martinez>which is a separate contract with the location and a separate sort of entry into our UI for all of the agreements that they have to review and agree to and enter the banking information.</v>

00:14:31.929 --> 00:14:35.209
<v Pavel Frolov>Who is taking the cash from the cash boxes?</v>

00:14:36.009 --> 00:14:36.649
<v Andrei Klimovich>Location.</v>

00:14:36.129 --> 00:14:37.289
<v Pavel Frolov>Locations.</v>

00:14:38.209 --> 00:14:38.889
<v Juan Martinez>Patients.</v>

00:14:43.929 --> 00:14:44.889
<v Val Levitan>Not all the time.</v>

00:14:45.449 --> 00:14:50.889
<v Juan Martinez>Yeah, not all the time. And technically they're not supposed to, but we know it happens.</v>

00:14:47.609 --> 00:14:47.929
<v Val Levitan>Okay.</v>

00:14:53.049 --> 00:15:05.129
<v Juan Martinez>Yeah, Georgia Lottery once told me that the location is not supposed to have only main door keys and that's it. They're not supposed to access anything else in the machine, but we know they do.</v>

00:15:08.089 --> 00:15:11.929
<v Val Levitan>I think, I think location definitely has a float.</v>

00:15:13.449 --> 00:15:18.009
<v Val Levitan>I don't see operator cruising around collecting cash.</v>

00:15:20.249 --> 00:15:23.449
<v Val Levitan>from a saving perspective, but you never know.</v>

00:15:25.209 --> 00:15:41.609
<v Andrei Klimovich>I don't know if it's a right approach, but if we will take a look to the situation from income point of view, actually income registers allocation as an entity which is eligible for issuing debit cards.</v>

00:15:42.649 --> 00:15:57.049
<v Andrei Klimovich>It registers the location totally in relation to master, because there is a master license number, location license number, etc., which, as far as I understand, has nothing to do with the location itself. It's up to master.</v>

00:15:56.569 --> 00:16:01.449
<v Val Levitan>This is, this also doesn't make any sense to me, because...</v>

00:16:03.689 --> 00:16:05.769
<v Val Levitan>Master cell locations.</v>

00:16:06.969 --> 00:16:10.569
<v Val Levitan>And they change masters very, very frequently.</v>

00:16:11.369 --> 00:16:16.009
<v Andrei Klimovich>But do they change the location license number in this case, or it's only?</v>

00:16:15.529 --> 00:16:15.929
<v Val Levitan>No.</v>

00:16:17.449 --> 00:16:24.089
<v Val Levitan>To the best of my knowledge, location license stays with the location.</v>

00:16:25.209 --> 00:16:39.609
<v Val Levitan>But I know that locations renegotiate agreements with master. And although the split may remain the same, masters go in and which they're not supposed to do, pay key money.</v>

00:16:32.969 --> 00:16:33.089
<v Andrei Klimovich>Yeah.</v>

00:16:42.169 --> 00:16:46.089
<v Val Levitan>And, and uh, and they buy smaller operators.</v>

00:16:47.689 --> 00:16:55.209
<v Val Levitan>So let's say, you know, a larger operator may acquire a route of 10 locations.</v>

00:16:56.969 --> 00:17:03.689
<v Val Levitan>And so what's the relevance of registering master with the location?</v>

00:17:04.649 --> 00:17:07.849
<v Val Levitan>Even for income, I just don't understand the point of it.</v>

00:17:11.529 --> 00:17:13.369
<v Val Levitan>Do you understand? Do you understand what I'm saying?</v>

00:17:14.249 --> 00:17:14.729
<v Andrei Klimovich>Yeah.</v>

00:17:26.249 --> 00:17:28.329
<v Juan Martinez>Well, I think we should get back to Nathan's.</v>

00:17:29.689 --> 00:17:30.489
<v Juan Martinez>Wyk, so.</v>

00:17:34.729 --> 00:17:34.969
<v Nathan Carver>Um...</v>

00:17:36.889 --> 00:17:39.369
<v Nathan Carver>Yeah, I guess, yeah, so from the business side then.</v>

00:17:40.449 --> 00:17:42.409
<v Nathan Carver>on the options we have available to us.</v>

00:17:43.689 --> 00:17:52.329
<v Nathan Carver>for handling an NSF is we move them straight to, you know, reconcile this with your credit card payment.</v>

00:17:53.529 --> 00:17:59.849
<v Nathan Carver>We flag them as a retry or re-initiation, but we do balance check before.</v>

00:18:02.489 --> 00:18:04.489
<v Nathan Carver>Initiating that transaction.</v>

00:18:06.209 --> 00:18:06.889
<v Juan Martinez>That had cool.</v>

00:18:06.249 --> 00:18:18.809
<v Nathan Carver>Because as of right now, we don't run a balance check before. We are set up to do it, but it was decided not to do it at the moment. So it's an easy switch to go back to that if we just blanket every.</v>

00:18:13.609 --> 00:18:13.689
<v Andrei Klimovich>Ohh.</v>

00:18:20.249 --> 00:18:20.569
<v Nathan Carver>Um...</v>

00:18:22.409 --> 00:18:26.009
<v Nathan Carver>Every debit right with a balance with a balance check.</v>

00:18:24.969 --> 00:18:25.929
<v Val Levitan>Yeah, but uh...</v>

00:18:27.089 --> 00:18:45.849
<v Val Levitan>Excuse me for an interruption, but let's not change the MVPs. My utmost concern is that the MVPs we designed for the release of beta test, this particular beta test, I just want those MVPs to work flawlessly.</v>

00:18:46.569 --> 00:18:46.969
<v Nathan Carver>Okay.</v>

00:18:46.929 --> 00:18:52.009
<v Val Levitan>I don't want new MVPs re-injected into it under.</v>

00:18:52.969 --> 00:18:54.329
<v Val Levitan>Auspices of.</v>

00:18:56.089 --> 00:19:02.649
<v Val Levitan>you know, let's reconcile something else. Because a couple of locations we can reconcile manually.</v>

00:18:57.489 --> 00:18:57.609
<v Nathan Carver>Yeah.</v>

00:18:59.049 --> 00:19:00.569
<v Nathan Carver>So I believe credit card.</v>

00:19:03.929 --> 00:19:04.329
<v Nathan Carver>Okay.</v>

00:19:04.089 --> 00:19:09.449
<v Val Levitan>And I don't care if we lose a couple of dollars here and there. I just want the device to work properly.</v>

00:19:10.809 --> 00:19:18.169
<v Nathan Carver>Okay. So then for MVP, it would be manual reconciliation through credit card payment or other means.</v>

00:19:18.649 --> 00:19:32.649
<v Val Levitan>For now, for now, for this beta test. I mean, next month we could add something and add five additional devices and move on. But let's just not panic. Let's focus for this particular one test.</v>

00:19:20.169 --> 00:19:20.409
<v Nathan Carver>Yeah.</v>

00:19:26.729 --> 00:19:27.129
<v Nathan Carver>Okay.</v>

00:19:33.929 --> 00:19:53.449
<v Juan Martinez>Yeah. And Nathan, one thing you said is they would receive 2 invoices the next day. If we're giving an alert to the customer saying insufficient funds, and they can quickly move money into that account via their banking app in 10 minutes,</v>

00:19:43.089 --> 00:19:43.209
<v Nathan Carver>And.</v>

00:19:53.849 --> 00:19:58.489
<v Juan Martinez>Why could we not re-invoice the same day?</v>

00:20:01.129 --> 00:20:01.289
<v Nathan Carver>And.</v>

00:20:02.729 --> 00:20:04.649
<v Nathan Carver>OK, so a couple of questions, so...</v>

00:20:05.769 --> 00:20:05.929
<v Nathan Carver>Uh.</v>

00:20:07.449 --> 00:20:14.809
<v Nathan Carver>In that scenario, so we don't, because we don't do a balance check right now, we have no way of sending them that message to say, you don't have enough funds.</v>

00:20:16.649 --> 00:20:21.769
<v Nathan Carver>The second invoice was simply because it's the next day. So we...</v>

00:20:22.889 --> 00:20:26.889
<v Nathan Carver>So on Tuesday, we run Monday's invoice. It gets an NSF.</v>

00:20:28.049 --> 00:20:33.209
<v Nathan Carver>that on Wednesday, we have the re-initiation of Monday, but we also have Tuesday's invoice now.</v>

00:20:34.729 --> 00:20:38.889
<v Nathan Carver>because we've processed another day. That's where the second one comes from.</v>

00:20:40.209 --> 00:20:45.769
<v Juan Martinez>Okay, except that on Wednesday's invoice, there is now a balance check because they're in that state.</v>

00:20:46.809 --> 00:20:49.129
<v Nathan Carver>Right, that would be the proposal. Do we want to?</v>

00:20:50.889 --> 00:20:57.929
<v Nathan Carver>So that I think that's what I'm hearing from Val is that's a proposal, but it's a post MVP.</v>

00:20:59.449 --> 00:21:00.809
<v Nathan Carver>decision implementation.</v>

00:21:02.489 --> 00:21:19.969
<v Pavel Frolov>May I ask a question? Correct me if I'm wrong, but I think for the pilot run, we do not block any locations. We are trying to generate invoices each day and send them.</v>

00:21:20.089 --> 00:21:28.169
<v Pavel Frolov>to the customers and never block locations due to not enough funds.</v>

00:21:32.249 --> 00:21:32.729
<v Juan Martinez>Reed.</v>

00:21:32.569 --> 00:21:33.209
<v Pavel Frolov>Okay, yeah.</v>

00:21:33.929 --> 00:21:34.169
<v Juan Martinez>Yep.</v>

00:21:34.449 --> 00:21:52.809
<v Pavel Frolov>The answer is yes. Okay, and next probably we can think about manual process of re-initiating ACH transactions. For example, if it was a manual call from the customer and he said, okay, I filled my...</v>

00:21:54.969 --> 00:22:16.889
<v Pavel Frolov>banking source, please reinitiate ACH transfer. And then probably we can add manual button on dashboard where our internal user like Juan or Andrei can press manual button, try again for particular invoice.</v>

00:22:17.289 --> 00:22:30.489
<v Pavel Frolov>And it will send message to Billing, and Billing will initiate this ACH withdrawal during next open ACH window.</v>

00:22:36.569 --> 00:22:40.569
<v Andrei Klimovich>It's not for MVP, right? It's like for the next version.</v>

00:22:41.369 --> 00:22:47.929
<v Pavel Frolov>Probably next week, I don't know. It looks not so difficult.</v>

00:22:50.729 --> 00:23:04.409
<v Andrei Klimovich>Well, the good point is that it does not create any duplicates. So invoice stays only in single version and it awaits for reconciliation for final decision, which is straightforward and easy to track.</v>

00:23:05.929 --> 00:23:15.929
<v Andrei Klimovich>It's a good point. The downside is that manual labor, but again, we do not expect hundreds of invoices per week to have issues.</v>

00:23:17.129 --> 00:23:20.089
<v Andrei Klimovich>So it sounds pretty solid.</v>

00:23:21.449 --> 00:23:34.729
<v Juan Martinez>And just one point to clarify, Nathan, just because the customer's account to us had insufficient funds, Diwala is expecting JVL to pay them the money, correct?</v>

00:23:33.449 --> 00:23:33.689
<v Andrei Klimovich>Efim.</v>

00:23:37.609 --> 00:23:38.249
<v Nathan Carver>And.</v>

00:23:38.809 --> 00:23:39.289
<v Val Levitan>Yes.</v>

00:23:38.889 --> 00:23:40.249
<v Juan Martinez>This breaks that flow.</v>

00:23:40.489 --> 00:23:43.449
<v Val Levitan>If, if, if we validate the card.</v>

00:23:44.529 --> 00:23:45.209
<v Val Levitan>Then, yes.</v>

00:23:47.449 --> 00:23:52.289
<v Nathan Carver>Oh, you mean income is still going to collect? Okay, correct.</v>

00:23:49.369 --> 00:23:50.489
<v Andrei Klimovich>Income, no dweller.</v>

00:23:50.489 --> 00:23:52.089
<v Juan Martinez>Income, sorry, yeah, income.</v>

00:23:51.449 --> 00:23:58.249
<v Val Levitan>Yeah, I understood your, I understood your question. Yes. If we validate the card, then we pay the money.</v>

00:23:59.049 --> 00:24:01.929
<v Val Levitan>They're actually removing themselves from this cycle.</v>

00:24:05.289 --> 00:24:05.529
<v Andrei Klimovich>Yeah.</v>

00:24:05.289 --> 00:24:09.129
<v Pavel Frolov>Uh, and they they give us uh how many days?</v>

00:24:10.649 --> 00:24:11.369
<v Andrei Klimovich>Warehousing.</v>

00:24:11.329 --> 00:24:12.969
<v Pavel Frolov>One day or three days?</v>

00:24:13.209 --> 00:24:13.769
<v Andrei Klimovich>All right.</v>

00:24:13.369 --> 00:24:17.129
<v Juan Martinez>I thought it was three days, if I'm not mistaken, from income.</v>

00:24:17.609 --> 00:24:21.689
<v Val Levitan>Three days only until the end of the year, but in actuality it's one day.</v>

00:24:25.209 --> 00:24:27.849
<v Val Levitan>But why are we establishing ourselves three days?</v>

00:24:31.209 --> 00:24:48.329
<v Val Levitan>I would suggest focusing on rolling out one, two, 5 products, and then revisiting this question. I mean, we don't know anything about the operation. We don't know how things work, and it's just virtually impossible to predict things.</v>

00:24:56.729 --> 00:24:57.129
<v Juan Martinez>Reed.</v>

00:24:57.769 --> 00:24:59.289
<v Nathan Carver>Okay, that makes sense.</v>

00:24:59.929 --> 00:25:19.849
<v Pavel Frolov>But we still need solution. So I understand we will not block any location, but we need some logic to either initiate invoices or void invoices in case when money got to GVL account somehow.</v>

00:25:00.569 --> 00:25:00.769
<v Nathan Carver>And.</v>

00:25:20.329 --> 00:25:22.089
<v Pavel Frolov>Outside of ACH.</v>

00:25:26.249 --> 00:25:35.289
<v Juan Martinez>And just quick, is the payment, the dashboard that's been referenced, that Pavel referenced, is this a payment hub dashboard?</v>

00:25:36.969 --> 00:25:44.609
<v Juan Martinez>Okay, and okay, so we'll have full visibility via payment hub as to what's going on customer by customer.</v>

00:25:50.009 --> 00:26:07.969
<v Andrei Klimovich>So for MVP, let's say we have one location, one unit, and at the beginning it goes smooth. All the invoices are being paid properly. Then we got the first invoice that was not funded because there is insufficient funds on location, bank account.</v>

00:26:08.089 --> 00:26:18.249
<v Andrei Klimovich>side, what happens if we do not change anything right now? What happens with this invoice? What happens the next day? Just let me know the case, what happens.</v>

00:26:19.369 --> 00:26:23.609
<v Nathan Carver>So the current state, the invoice would be an MSBC as unpaid.</v>

00:26:25.969 --> 00:26:30.009
<v Nathan Carver>and there would be no further activity on it. So from there, you could...</v>

00:26:30.969 --> 00:26:35.209
<v Nathan Carver>You know, call them, say, you know, pay by your credit cards to mail us a check.</v>

00:26:37.129 --> 00:26:39.209
<v Nathan Carver>However, you would normally collect money.</v>

00:26:39.689 --> 00:26:40.169
<v Andrei Klimovich>Mhm.</v>

00:26:40.329 --> 00:26:41.449
<v Nathan Carver>Your customers.</v>

00:26:42.809 --> 00:26:44.449
<v Nathan Carver>It just wouldn't go through Payables.</v>

00:26:43.129 --> 00:26:43.689
<v Andrei Klimovich>Works.</v>

00:26:44.729 --> 00:26:47.369
<v Andrei Klimovich>Works for me, sounds manageable.</v>

00:26:49.529 --> 00:27:00.889
<v Pavel Frolov>But the payment hub must know about any money got outside of billing system.</v>

00:26:55.609 --> 00:26:57.809
<v Andrei Klimovich>I will be there to make job next week.</v>

00:27:02.489 --> 00:27:04.369
<v Nathan Carver>Correct, yeah, we would end up with a...</v>

00:27:06.329 --> 00:27:16.569
<v Nathan Carver>So in MSBC, you would receive the money and the only place you would enter that is in MSBC, you would update that invoice as having been paid.</v>

00:27:17.529 --> 00:27:21.449
<v Nathan Carver>Payment Hub would have no currently doesn't know that's happening.</v>

00:27:24.249 --> 00:27:30.409
<v Nathan Carver>And maybe that's okay in this first MVP, right? Because we may or may not have a lot. Yeah.</v>

00:27:27.689 --> 00:27:45.369
<v Andrei Klimovich>It's perfectly okay, unless we block the location, which we do not do, as we've agreed. There is no issue with that. There will be an invoice which says that it's unpaid on the payment hub side, which is fine, because...</v>

00:27:46.409 --> 00:27:49.369
<v Andrei Klimovich>Later, we can think of the process how we reconcile it.</v>

00:27:53.129 --> 00:28:02.209
<v Nathan Carver>Yeah, and it would be just the billing part of Payment Hub could re-sync with MSBC if it had to and update it in terms of that.</v>

00:28:03.609 --> 00:28:19.209
<v Pavel Frolov>So, for this reaction, it will not be available any reconciliation data from Payment Hub versus data on MSBC versus data on invoice income.</v>

00:28:21.849 --> 00:28:23.529
<v Andrei Klimovich>Not in MVP.</v>

00:28:24.329 --> 00:28:24.809
<v Pavel Frolov>Mmh.</v>

00:28:25.289 --> 00:28:32.169
<v Andrei Klimovich>Yeah, okay. So the major question we have to AKS is to understand.</v>

00:28:34.169 --> 00:28:34.889
<v Andrei Klimovich>How they?</v>

00:28:37.529 --> 00:28:38.329
<v Andrei Klimovich>How's the?</v>

00:28:39.529 --> 00:28:40.409
<v Andrei Klimovich>Would like.</v>

00:28:43.369 --> 00:29:03.289
<v Andrei Klimovich>this process of assigning a bank account for each single location to work. I mean, if they will use their bank account, which is perfectly fine and it solves a lot of questions, or they really would prefer each single location to assign their own bank account, which creates a different flow for us.</v>

00:29:04.809 --> 00:29:05.049
<v Juan Martinez>Yeah.</v>

00:29:05.929 --> 00:29:07.849
<v Andrei Klimovich>Okay, yeah, makes sense.</v>

00:29:09.529 --> 00:29:22.489
<v Andrei Klimovich>Okay, yeah. So I will do my best to talk to AKS today. I don't know if they are in touch, but me and Felipe will do our best to reach out to them.</v>

00:29:27.169 --> 00:29:27.689
<v Nathan Carver>All right.</v>

00:29:28.009 --> 00:29:38.569
<v Val Levitan>You know what, let me suggest by just, let's just focus on placing one unit in location. I would not even talk to AKS.</v>

00:29:30.729 --> 00:29:30.849
<v Nathan Carver>Yeah.</v>

00:29:41.049 --> 00:29:46.329
<v Andrei Klimovich>Anyways, it's the case which bank account will be used for this one unit. Anyways, it's...</v>

00:29:47.849 --> 00:29:55.449
<v Val Levitan>The bank account? No, I don't think so. Because we need to use locations bank account.</v>

00:30:13.129 --> 00:30:29.689
<v Juan Martinez>Yeah, I mean, then we have to take the same approach income did. Income went behind the backs of the masters and sold the PAX device or enter into agreement for the PAX device through their resellers and the locations directly.</v>

00:30:30.809 --> 00:30:51.529
<v Juan Martinez>That's how their workaround was. However, the masters are our customers, so we didn't want to offend them by approaching the location directly. But things have changed now, and I think the masters understand that. So, okay, I'll work on the location draft for the banking information.</v>

00:30:54.249 --> 00:31:02.409
<v Val Levitan>And our full position is that this is mandated by income. We don't care. I mean, it's not our thing.</v>

00:31:03.609 --> 00:31:08.889
<v Val Levitan>We were told by Incom that we need location bank account and that's what we're getting.</v>

00:31:17.209 --> 00:31:17.529
<v Andrei Klimovich>Okay.</v>

00:31:19.209 --> 00:31:20.889
<v Val Levitan>And, and again, so...</v>

00:31:22.609 --> 00:31:27.689
<v Val Levitan>What's holding us from placing one machine in location?</v>

00:31:29.449 --> 00:31:31.369
<v Val Levitan>Sorry, one IQ in location.</v>

00:31:33.849 --> 00:31:51.769
<v Andrei Klimovich>So on AKS, which is our hottest opportunity here, hottest master we're currently talking to, there is no document signed yet. So it's up to Felipe, me and Juan to push this and make sure that we have a sealed agreement. On the other side,</v>

00:31:50.809 --> 00:32:04.569
<v Val Levitan>Well, it's not it's not up to Felipe, UN one. It's basically up to Felipe mostly to get the agreement. Let's not dilute the issue. Let's just point the finger at what it is.</v>

00:32:05.529 --> 00:32:08.889
<v Val Levitan>So, Felipe must get us the agreement.</v>

00:32:05.969 --> 00:32:06.489
<v Andrei Klimovich>Okay.</v>

00:32:10.169 --> 00:32:16.089
<v Val Levitan>With AKS for their location, so Felipe must execute that.</v>

00:32:18.009 --> 00:32:19.449
<v Val Levitan>Agreement with the location.</v>

00:32:20.329 --> 00:32:35.729
<v Andrei Klimovich>Okay, and from technical point of view, we still need to run this production test, which I described to you on Friday, like step by step. And step one is we need to have a contract signed with between JVL and Waller.</v>

00:32:36.569 --> 00:32:41.849
<v Val Levitan>But that I believe I already said. I think that has already been signed.</v>

00:32:43.129 --> 00:32:45.289
<v Val Levitan>To the best of my knowledge, it has been signed.</v>

00:32:47.529 --> 00:32:54.729
<v Andrei Klimovich>Yeah, I, I don't know that. I mean, like, Pavel, do you see any changes in the wallet dashboard? Do we have access to?</v>

00:32:55.689 --> 00:32:56.409
<v Andrei Klimovich>Setup.</v>

00:32:58.409 --> 00:32:59.049
<v Andrei Klimovich>Production.</v>

00:32:59.369 --> 00:33:04.809
<v Pavel Frolov>Last time when I checked, it was on Friday, not checked today.</v>

00:33:05.769 --> 00:33:06.649
<v Val Levitan>Please check.</v>

00:33:07.169 --> 00:33:07.369
<v Pavel Frolov>Uh-huh.</v>

00:33:08.569 --> 00:33:28.169
<v Andrei Klimovich>Well, if it's done, then we are ready to move and it's up to one day to run this production tests, issue cards, make sure that we are being invoiced by income to see how the payment hub slash MSBC integration works, to test everything end to end, and if it's fine,</v>

00:33:28.289 --> 00:33:29.129
<v Andrei Klimovich>We are ready to go.</v>

00:33:35.769 --> 00:33:52.889
<v Andrei Klimovich>So Nathan, by the way, like the test I'm talking about is to run the full cycle card issue on a production server. So we will be issuing a real debit cards through income. We expect income to issue invoice the next day.</v>

00:33:37.689 --> 00:33:37.849
<v Nathan Carver>Yuri.</v>

00:33:53.369 --> 00:34:12.809
<v Andrei Klimovich>We expect to see exactly the same transactions that we've completed. We expect this invoice to be processed by Payment Hub and MSBC. So we expect Payment Hub and MSBC to issue an invoice to bank accounts that will be linked to this location to see that it was properly paid.</v>

00:34:13.129 --> 00:34:15.769
<v Andrei Klimovich>Et cetera, et cetera, so this is the full cycle.</v>

00:34:14.329 --> 00:34:15.049
<v Val Levitan>The insure.</v>

00:34:16.729 --> 00:34:20.569
<v Val Levitan>Yeah, interesting. I want to ask the I want to ask a question.</v>

00:34:22.409 --> 00:34:29.369
<v Val Levitan>If we don't have dweller in this loop, what's stopping us from?</v>

00:34:30.489 --> 00:34:32.409
<v Val Levitan>Running this one experiment.</v>

00:34:33.929 --> 00:34:35.209
<v Andrei Klimovich>I cannot.</v>

00:34:34.169 --> 00:34:36.249
<v Val Levitan>To the best of my knowledge, nothing.</v>

00:34:37.209 --> 00:34:48.649
<v Andrei Klimovich>No, I cannot register a production location without providing bank account. And I cannot provide a bank account without Duolo. That's the way how it designs.</v>

00:34:47.369 --> 00:34:51.609
<v Val Levitan>You, you can, you, you can, you can, you absolutely can.</v>

00:34:52.969 --> 00:35:02.489
<v Val Levitan>We have a bank account. The wallet just wedges itself in between our bank account and the operator. And sorry, and the location.</v>

00:35:04.089 --> 00:35:05.769
<v Val Levitan>But we have a bank account.</v>

00:35:04.249 --> 00:35:04.729
<v Andrei Klimovich>Ohh.</v>

00:35:07.049 --> 00:35:15.769
<v Val Levitan>The CIBC bank account has been opened. This is where money needs to be transferred. But for income purposes,</v>

00:35:17.129 --> 00:35:18.329
<v Val Levitan>It's where they.</v>

00:35:19.289 --> 00:35:22.569
<v Val Levitan>swipe their money from. This is what they need.</v>

00:35:23.849 --> 00:35:35.129
<v Val Levitan>Income is saying, when I validate your card, where do I, which account do I swipe? And the account that they swipe physically,</v>

00:35:36.569 --> 00:35:40.489
<v Val Levitan>is the CIBC account that Nathan has.</v>

00:35:43.849 --> 00:35:53.849
<v Andrei Klimovich>So, if I'm if I understand you correctly, you're describing the side between income and JVL, but we have another part of it we have between.</v>

00:35:53.049 --> 00:35:55.129
<v Val Levitan>Optional, optional.</v>

00:35:55.529 --> 00:35:58.009
<v Andrei Klimovich>Between JVL and operator.</v>

00:36:00.409 --> 00:36:01.049
<v Val Levitan>Yes.</v>

00:36:00.569 --> 00:36:02.969
<v Andrei Klimovich>And the and in.</v>

00:36:02.889 --> 00:36:10.649
<v Val Levitan>We we don't have to swipe it the the automation between JVL and.</v>

00:36:11.849 --> 00:36:16.089
<v Val Levitan>Location exists for the convenience of...</v>

00:36:17.209 --> 00:36:17.929
<v Val Levitan>JVL.</v>

00:36:21.289 --> 00:36:35.849
<v Val Levitan>But it doesn't need to exist. It could be totally manual. We could call an operator, we could call a location and say, gas station XYZ, we need you to transfer the money.</v>

00:36:38.089 --> 00:36:39.209
<v Andrei Klimovich>Yeah, but the way hot.</v>

00:36:38.329 --> 00:36:40.169
<v Val Levitan>Income, income doesn't care.</v>

00:36:41.449 --> 00:36:52.809
<v Andrei Klimovich>Yeah, I'm not talking about income. Basically, my idea is that while testing the flow, we should test it in a way how it will work in reality, right? And...</v>

00:36:49.289 --> 00:36:50.929
<v Val Levitan>We should, we we should.</v>

00:36:52.569 --> 00:36:57.369
<v Val Levitan>We should, we should, but I'm anxious of testing other things.</v>

00:36:53.929 --> 00:36:54.409
<v Andrei Klimovich>Yes.</v>

00:36:58.329 --> 00:37:16.569
<v Andrei Klimovich>Of course, but the point is that to register location, just to register, to make it, to bind a unit IQ to a specific location which is in a production, the whole flow is designed right now in the way that I need to assign a bank account to the location.</v>

00:37:16.889 --> 00:37:19.449
<v Val Levitan>I, I've answered, I've answered that question.</v>

00:37:17.129 --> 00:37:17.369
<v Andrei Klimovich>Um...</v>

00:37:20.089 --> 00:37:24.169
<v Andrei Klimovich>So I need a workaround in this case. I need to talk to Pavel how we can.</v>

00:37:25.769 --> 00:37:26.569
<v Andrei Klimovich>Fake.</v>

00:37:26.049 --> 00:37:31.769
<v Val Levitan>You can talk, you can talk to me. I'm also, I have ears. Go ahead, say what you need to say.</v>

00:37:30.969 --> 00:37:35.689
<v Andrei Klimovich>So, we need we need to find the workaround in our currently designed process.</v>

00:37:34.329 --> 00:37:36.729
<v Val Levitan>Which work, which workaround?</v>

00:37:37.209 --> 00:37:51.129
<v Andrei Klimovich>So to register a location, to make a unit work in this location, the process is designed in the way that I have to, there is no other way, I have to assign a bank account to this location first.</v>

00:37:52.729 --> 00:37:56.809
<v Andrei Klimovich>Unless the bank account is assigned, the location is not active.</v>

00:37:56.969 --> 00:38:02.569
<v Val Levitan>You're talking about to run a test that is that is in...</v>

00:38:03.809 --> 00:38:07.929
<v Val Levitan>where the IQ unit sits in our office in Georgia.</v>

00:38:08.409 --> 00:38:08.969
<v Andrei Klimovich>Correct.</v>

00:38:09.969 --> 00:38:12.249
<v Val Levitan>Okay, so you are...</v>

00:38:13.329 --> 00:38:16.169
<v Val Levitan>Simulating your own account.</v>

00:38:17.449 --> 00:38:25.769
<v Val Levitan>Your personal account as as a location, not not operator location.</v>

00:38:19.129 --> 00:38:19.689
<v Andrei Klimovich>Yes.</v>

00:38:21.529 --> 00:38:23.209
<v Andrei Klimovich>Operators, yes.</v>

00:38:26.009 --> 00:38:27.609
<v Andrei Klimovich>Locations bank account, correct?</v>

00:38:28.009 --> 00:38:43.449
<v Val Levitan>Yes, so supposedly we place machines, sorry, IQ in your location and you give us your account. So we'll, so you is the location account.</v>

00:38:44.649 --> 00:38:50.249
<v Val Levitan>Income does not care about location account to the best of my knowledge.</v>

00:38:51.049 --> 00:39:05.929
<v Val Levitan>To the best of my knowledge, and correct me if I'm wrong, income is only interested in JVL account because they want to have an account where they swipe money off of. Am I wrong?</v>

00:39:07.289 --> 00:39:08.169
<v Val Levitan>In assuming.</v>

00:39:07.369 --> 00:39:10.409
<v Andrei Klimovich>No, no, you're correct. This side is absolutely right.</v>

00:39:10.809 --> 00:39:16.169
<v Val Levitan>Okay, so we need to achieve 2 things. We need to test.</v>

00:39:17.449 --> 00:39:19.849
<v Val Levitan>Swiping, not not swiping.</v>

00:39:20.889 --> 00:39:27.449
<v Val Levitan>Getting money from you, from your account to GVLCIBC account.</v>

00:39:28.729 --> 00:39:49.769
<v Val Levitan>that loop and from CIBC account to income. Dwalla is an optional wedge that it's not optional, optional automation wedge. This is what makes things easier to function. We want Dwalla to swipe your account, put it into their intermediary account.</v>

00:39:50.169 --> 00:39:56.569
<v Val Levitan>transfer it to CIBC account, then the whole loop functions automatically.</v>

00:39:58.529 --> 00:40:07.849
<v Andrei Klimovich>And besides this, to make those locations to become active, which be available for issuing credit debit cards.</v>

00:40:08.729 --> 00:40:19.209
<v Andrei Klimovich>The process is designed in the way that I have to assign this bank account in Payment Hub, right? So if we would like to do that manually somewhere in the background.</v>

00:40:20.569 --> 00:40:24.409
<v Andrei Klimovich>We can fake it, probably we can fake it, we can, we can.</v>

00:40:20.649 --> 00:40:21.289
<v Val Levitan>Yes.</v>

00:40:22.409 --> 00:40:30.249
<v Val Levitan>Yes, yes, for one location, for one location, yes. Even if, I mean, I believe that Dual is signed.</v>

00:40:31.929 --> 00:40:32.729
<v Val Levitan>I, I mean...</v>

00:40:34.169 --> 00:40:40.969
<v Val Levitan>You should probably call the wallet today and say, look, to the best of my knowledge, the contract has been signed. What's holding you up?</v>

00:40:42.089 --> 00:40:52.449
<v Val Levitan>And I think they will say, yeah, indeed, or Monica signed, and it's our legal department that hasn't signed yet, but it has been fully negotiated and should be signed.</v>

00:40:53.929 --> 00:40:56.089
<v Val Levitan>But let's say, let's say it's not.</v>

00:40:58.569 --> 00:41:01.689
<v Val Levitan>Nothing, nothing is stopping us running the test.</v>

00:41:03.129 --> 00:41:08.409
<v Val Levitan>And, and installing the machine and the live location, unless I'm missing something.</v>

00:41:13.049 --> 00:41:13.449
<v Andrei Klimovich>So...</v>

00:41:15.209 --> 00:41:33.329
<v Andrei Klimovich>We can do that. I mean, it's a question of how much time it will take to finalize the agreement with Dwola and make sure it's signed and activate our account. If it's a question of couple hours or half of a day, I would say that it's better to do that first, other than to work on the workaround doing some stuff.</v>

00:41:33.409 --> 00:41:52.489
<v Andrei Klimovich>under the hood. If it's a question of couple days, of course we can go with a workaround, but the cavity over here is that we are not testing the real flow. We are testing a manually prepared flow, which will be totally different in reality. So</v>

00:41:52.569 --> 00:41:56.649
<v Andrei Klimovich>I'm a little bit concerned about that, that we are not actually testing the real flow.</v>

00:41:59.449 --> 00:42:09.289
<v Val Levitan>The only thing that we will not be testing under this proposal is the automation cycle, which should become easier.</v>

00:42:07.049 --> 00:42:07.769
<v Andrei Klimovich>Correct.</v>

00:42:10.649 --> 00:42:16.249
<v Andrei Klimovich>I don't know. We've never seen it in life. So that's why I would like to test it first, at least with three cards.</v>

00:42:19.209 --> 00:42:30.569
<v Juan Martinez>And one thing on the timing, next week is the Georgia show. Are we actually contemplating on trying to get a unit out next week during the show?</v>

00:42:31.529 --> 00:42:32.409
<v Val Levitan>This Wyk.</v>

00:42:33.849 --> 00:42:43.049
<v Juan Martinez>Even worse, I mean, who's available next week? If the customers at the show and Andrei and Felipe at the show, it just seems a bit risky.</v>

00:42:51.049 --> 00:42:59.449
<v Andrei Klimovich>You mean, like, if it's if it will require any physical assistance, like to come to the location to do the unit replacement, et cetera?</v>

00:42:59.209 --> 00:43:05.609
<v Juan Martinez>Yeah, exactly. Something's not working. You know, you're at the show, Felipe is at the show.</v>

00:43:02.489 --> 00:43:02.849
<v Andrei Klimovich>No.</v>

00:43:04.569 --> 00:43:12.729
<v Andrei Klimovich>Yeah, I can always jump off to my car and run to this location. I mean, it's a priority in comparison to the expo, I guess.</v>

00:43:13.929 --> 00:43:17.209
<v Val Levitan>But the expo in Georgia is only one day, truly.</v>

00:43:18.729 --> 00:43:23.209
<v Val Levitan>This is where, and it's not even one day, it's kind of a...</v>

00:43:24.289 --> 00:43:25.689
<v Val Levitan>Six-hour fragment.</v>

00:43:29.609 --> 00:43:32.889
<v Val Levitan>So to lose 2 weeks over a six-hour fragment?</v>

00:43:36.569 --> 00:43:49.529
<v Andrei Klimovich>No, no, we shouldn't do that, of course. So, Pavel, I see you send us a screenshot, so it's the wall account is not active yet. May I ask you to send a message to Dwola asking what's still needed?</v>

00:43:44.489 --> 00:43:45.049
<v Pavel Frolov>Mhm.</v>

00:43:51.369 --> 00:43:52.249
<v Pavel Frolov>Okay, no problem.</v>

00:44:22.329 --> 00:44:28.489
<v Juan Martinez>And Andrei, do you think AKS is in a position to execute contracts this week?</v>

00:44:29.129 --> 00:44:35.849
<v Andrei Klimovich>I don't know. I mean, like, I'm not the major contact point here, so it's definitely up to Felipe and...</v>

00:44:37.129 --> 00:44:40.889
<v Andrei Klimovich>I will talk right away after our call and see where we are.</v>

00:44:42.969 --> 00:44:44.009
<v Juan Martinez>Yeah, let, let.</v>

00:44:43.689 --> 00:44:57.849
<v Val Levitan>Okay, so what did we decide? We decide not to delay the test. We decided that, let's say, Dwalla will be signed up to, let's say, Wednesday, we should be able to close this deal.</v>

00:45:00.329 --> 00:45:18.889
<v Val Levitan>And until Wednesday, I don't think you will sign up the location. So it's kind of hand in hand. You need to sign up the location. You need to, we need to sign up the walla. And let's assume that Thursday, we're able to place the machine in the location.</v>

00:45:19.369 --> 00:45:21.049
<v Val Levitan>My machine, I mean IQ.</v>

00:45:21.849 --> 00:45:24.329
<v Val Levitan>So, let's assume that this is the schedule.</v>

00:45:25.289 --> 00:45:27.849
<v Val Levitan>So, from a technological perspective.</v>

00:45:28.889 --> 00:45:30.729
<v Val Levitan>Only the function of technology.</v>

00:45:33.529 --> 00:45:43.369
<v Val Levitan>And only as it concerns the MVPs. What is not working technically, physically, technically. Crashes, bugs.</v>

00:45:47.369 --> 00:45:49.609
<v Val Levitan>What needs to be fixed? Can somebody...</v>

00:45:52.649 --> 00:45:53.609
<v Pavel Frolov>On.</v>

00:45:52.969 --> 00:45:54.489
<v Val Levitan>List, list it.</v>

00:45:55.769 --> 00:46:02.649
<v Pavel Frolov>On our side, I assume only remote software update left to be implemented.</v>

00:46:04.689 --> 00:46:06.489
<v Juan Martinez>What was that, Pavel? I'm sorry.</v>

00:46:07.009 --> 00:46:08.809
<v Pavel Frolov>Remote software update.</v>

00:46:12.249 --> 00:46:20.969
<v Andrei Klimovich>Yeah, so from my perspective, the last build I tested, there are no crashes, there are no errors, there is one minor issue with motor goods detection.</v>

00:46:13.049 --> 00:46:13.289
<v Nathan Carver>Yeah.</v>

00:46:21.929 --> 00:46:41.969
<v Andrei Klimovich>So if Mutagus powers on before IQ, IQ doesn't see Mutagus and it always says that Mutagus is not detected, which might be the case if the power goes off on the location. Mutagus is always powering up quicker than IQ.</v>

00:46:42.169 --> 00:46:44.489
<v Andrei Klimovich>We may, we may have this tilt.</v>

00:46:47.129 --> 00:47:02.969
<v Andrei Klimovich>So, it's reported, and Ivan knows about that, and the strange thing that is that it doesn't it cannot be reproduced on Minsk machine, but it's but it's 100% reproduced here in Georgia.</v>

00:46:57.449 --> 00:46:58.009
<v Pavel Frolov>It means.</v>

00:47:05.649 --> 00:47:14.489
<v Juan Martinez>What that if you power down both devices, IQ takes significantly longer to come online than Mother Goose? Is that what you're saying?</v>

00:47:15.209 --> 00:47:15.769
<v Pavel Frolov>Yes.</v>

00:47:15.769 --> 00:47:34.489
<v Andrei Klimovich>So if in any case, IQ is powered on after Mutagus, IQ doesn't see Mutagus and always says Mutagus is not detected. So the only fix is you need to power off Mutagus, power on it again, and then we can see it.</v>

00:47:34.569 --> 00:47:44.729
<v Andrei Klimovich>On the power on stage, or you can you have to disconnect the cable and connect it back, and when Mutagus comes up, we can see it on IQ.</v>

00:47:49.049 --> 00:48:01.609
<v Andrei Klimovich>But Pavel, we have different EVO boards and we have different motherboards. We've compared it with Ivan and you have older versions. I don't know if it's the case, but at least it's the difference.</v>

00:48:04.569 --> 00:48:04.729
<v Pavel Frolov>Mm.</v>

00:48:06.169 --> 00:48:07.169
<v Pavel Frolov>So this is.</v>

00:48:09.609 --> 00:48:23.289
<v Pavel Frolov>result of our switching to different approach to mirroring comport goes to printer from Mutabus.</v>

00:48:25.289 --> 00:48:34.409
<v Pavel Frolov>In case when it was a cut cable and connecting between, it wasn't a problem.</v>

00:48:35.609 --> 00:48:37.209
<v Pavel Frolov>You always correcting?</v>

00:48:38.569 --> 00:48:44.169
<v Pavel Frolov>Uh, detected connection and printer connection, but right now.</v>

00:48:45.689 --> 00:48:46.809
<v Pavel Frolov>This is a case.</v>

00:48:49.289 --> 00:49:01.449
<v Juan Martinez>And Andrei, the cellular modem is fully, we have a provider, we have a SIM card, we have a modem, and have we tested running it on modem only?</v>

00:49:02.569 --> 00:49:15.049
<v Andrei Klimovich>Yeah, yeah, it runs on the modem only for the last couple of weeks and it's stable, it works well. I have no idea about the coverage if we are talking about somewhere really far away point.</v>

00:49:13.609 --> 00:49:16.649
<v Val Levitan>It's AT. It's AT&T, right?</v>

00:49:19.369 --> 00:49:26.649
<v Andrei Klimovich>I guess so, I don't remember. Sorry. Let me see. Yeah, no, it's T-Mobile. T-Mobile. Right now.</v>

00:49:25.489 --> 00:49:29.849
<v Val Levitan>Okay, so it's a national, it's a national carrier.</v>

00:49:30.649 --> 00:49:49.449
<v Andrei Klimovich>Of course, I've seen the map and they have a coverage, like the full Giorgi is perfectly covered. If it's not 5G, it's 3G at least. Yeah, so it works. It constantly works. No issues with LTE, at least I haven't seen any. So 2 issues from software.</v>

00:49:49.609 --> 00:50:03.449
<v Andrei Klimovich>slash hardware is this Mutagus tilt. Secondly is remote software update. And for Nathan's part, I don't know, maybe Nathan, you can give us an update, like if you are fully ready.</v>

00:50:03.209 --> 00:50:04.009
<v Nathan Carver>Putting ready.</v>

00:50:06.569 --> 00:50:08.689
<v Nathan Carver>So, we're we're testing the...</v>

00:50:11.209 --> 00:50:21.609
<v Nathan Carver>The flipping of, or I should say, we're testing the ledger side and MSPC, making sure that all of those, that the proper</v>

00:50:22.729 --> 00:50:22.809
<v Nathan Carver>Uh.</v>

00:50:24.169 --> 00:50:27.369
<v Nathan Carver>Values are applied in the ledger, and...</v>

00:50:30.329 --> 00:50:34.169
<v Nathan Carver>And I owe QA a couple of things on that that I'm finishing up today.</v>

00:50:36.089 --> 00:50:39.769
<v Nathan Carver>But as far as I know, I believe that's it. There's some...</v>

00:50:40.809 --> 00:50:45.449
<v Nathan Carver>They're still testing just that flow at the at the very end with MSPC.</v>

00:50:49.249 --> 00:50:51.209
<v Nathan Carver>Is that right, Pavel? Is there anything I missed?</v>

00:50:52.089 --> 00:50:53.849
<v Pavel Frolov>Nothing, nothing more.</v>

00:50:53.969 --> 00:50:54.169
<v Nathan Carver>Yeah.</v>

00:50:57.609 --> 00:51:09.449
<v Nathan Carver>From the business side, for the invoice that goes to the customer, that's via e-mail, correct? Is that, is there an invoice example or anything you want to send?</v>

00:51:12.409 --> 00:51:25.849
<v Nathan Carver>Because Payment Hub itself doesn't e-mail that, I think we'll have to set it up within MSBC. I'm assuming MSBC can do that, but if not, we'll need to add some type of mechanism to send the e-mail.</v>

00:51:35.289 --> 00:51:55.209
<v Andrei Klimovich>Technically, we have an e-mail, so every single location has a dedicated e-mail, so we have an address where we can send this invoice. The question is about the form, the shape of the invoice, the design itself. I don't know, like Juan, maybe you have an example or...</v>

00:51:45.289 --> 00:51:45.769
<v Nathan Carver>Okay.</v>

00:51:57.529 --> 00:52:04.369
<v Andrei Klimovich>I don't have any requirement to that, or maybe we have a standard standard JVL invoice, something like that.</v>

00:52:00.729 --> 00:52:01.209
<v Nathan Carver>Okay.</v>

00:52:08.809 --> 00:52:09.929
<v Andrei Klimovich>You, you're on mute.</v>

00:52:09.849 --> 00:52:10.569
<v Pavel Frolov>Mute it.</v>

00:52:14.049 --> 00:52:21.369
<v Juan Martinez>No, I don't have any sample. I was kind of waiting for this production test to generate that actual invoice to see what we're getting.</v>

00:52:20.089 --> 00:52:20.249
<v Andrei Klimovich>Yeah.</v>

00:52:23.929 --> 00:52:29.529
<v Nathan Carver>Well, if we send what's in MSVC, we may not want, I guess it depends on how we want.</v>

00:52:30.609 --> 00:52:39.129
<v Nathan Carver>fees to be broken down to the customer. Do we want them in a single service fee? Do we want them to see line item fees? Because in our ledger, we have...</v>

00:52:40.089 --> 00:52:41.369
<v Nathan Carver>Obviously, multiple fees.</v>

00:52:40.649 --> 00:52:43.129
<v Val Levitan>Like line item, line item.</v>

00:52:42.569 --> 00:52:43.769
<v Juan Martinez>Yeah, line item, yeah.</v>

00:52:42.809 --> 00:52:43.289
<v Nathan Carver>Okay.</v>

00:52:44.489 --> 00:52:47.369
<v Nathan Carver>All right, so just what's in the ledger will get sent.</v>

00:52:48.089 --> 00:52:56.249
<v Andrei Klimovich>So maybe you can generate the current version with line item and send it to us for review. Maybe it's fine and we are ready to go with this version.</v>

00:52:57.929 --> 00:52:58.329
<v Nathan Carver>Okay.</v>

00:53:00.009 --> 00:53:01.129
<v Val Levitan>Okay, so...</v>

00:53:00.089 --> 00:53:01.289
<v Nathan Carver>Alright, I'll go look at.</v>

00:53:02.249 --> 00:53:06.089
<v Val Levitan>So, I'm hearing there are no technical issues that could...</v>

00:53:07.169 --> 00:53:10.249
<v Val Levitan>Prohibit us to start on Thursday, am I?</v>

00:53:11.369 --> 00:53:17.209
<v Val Levitan>Hearing it correct, I'm referring only to one single beta location.</v>

00:53:18.409 --> 00:53:22.169
<v Val Levitan>Only with MVPs, adding nothing more.</v>

00:53:23.209 --> 00:53:23.729
<v Andrei Klimovich>Correct.</v>

00:53:23.529 --> 00:53:26.089
<v Val Levitan>And, and allowing Pavel.</v>

00:53:27.209 --> 00:53:34.729
<v Val Levitan>To finish, the most important thing that I am after is the flawless.</v>

00:53:28.089 --> 00:53:28.569
<v Nathan Carver>Mhm.</v>

00:53:37.129 --> 00:53:39.449
<v Val Levitan>Remote updates.</v>

00:53:40.569 --> 00:53:42.969
<v Val Levitan>That has to work like Swiss Watch.</v>

00:53:44.489 --> 00:53:46.409
<v Val Levitan>With all the error checks.</v>

00:53:47.929 --> 00:53:52.969
<v Val Levitan>pings and parks getting there and like it has to be perfect.</v>

00:53:53.929 --> 00:53:54.169
<v Pavel Frolov>Mm.</v>

00:53:53.929 --> 00:53:54.249
<v Juan Martinez>Yeah.</v>

00:53:55.609 --> 00:53:56.809
<v Juan Martinez>I guess.</v>

00:53:55.769 --> 00:54:06.969
<v Val Levitan>So that I assume will, we don't need it at the point of installation, but somewhere between a week or two weeks, Pavel, can you finish it for us?</v>

00:54:07.849 --> 00:54:08.729
<v Pavel Frolov>I hope so.</v>

00:54:09.769 --> 00:54:11.049
<v Val Levitan>Okay, so...</v>

00:54:13.369 --> 00:54:17.769
<v Val Levitan>When you install Andrei, correct me if I'm wrong, you'll be...</v>

00:54:20.409 --> 00:54:22.409
<v Val Levitan>Experiencing all the...</v>

00:54:23.449 --> 00:54:25.449
<v Val Levitan>Little things that you don't like.</v>

00:54:27.449 --> 00:54:31.849
<v Val Levitan>And based on what you see and what you're experiencing, you could...</v>

00:54:33.049 --> 00:54:42.089
<v Val Levitan>Create another set of MVPs that probably within two weeks we can make them and because we already have</v>

00:54:43.849 --> 00:54:48.729
<v Val Levitan>Modem updates working perfectly at that time, we could download them.</v>

00:54:51.609 --> 00:55:10.249
<v Val Levitan>and move on, right? And when you get that second set of MVPs, which is something that was really bothering you and you had to get them done, this is the time when we can install another, let's say, two, three, 5 units. Do I understand us correctly?</v>

00:55:10.729 --> 00:55:12.489
<v Val Levitan>Are we aligned on this or not?</v>

00:55:13.449 --> 00:55:33.769
<v Andrei Klimovich>Yes, we are. We are. And meanwhile, when the remote software update is not ready, it's not a problem to come with a SD card and run the update if it's needed. The only thing that I'm a little bit, not a little bit, I'm concerned about this tilt. And it's a real situation because many locations, they do power off.</v>

00:55:14.769 --> 00:55:15.369
<v Juan Martinez>Yeah, babe.</v>

00:55:32.249 --> 00:55:32.649
<v Pavel Frolov>Accounts.</v>

00:55:34.729 --> 00:55:35.769
<v Andrei Klimovich>At the end of the day.</v>

00:55:35.129 --> 00:55:45.409
<v Pavel Frolov>Let me let me talk with Genadi today about this. Probably we will invent something.</v>

00:55:45.929 --> 00:55:47.169
<v Andrei Klimovich>Okay, sounds good.</v>

00:55:48.809 --> 00:56:01.529
<v Juan Martinez>And then lastly, Val, the only hang up is for this one single beta test, if the customer does not sign off on the agreements, do we still want to go ahead and move forward?</v>

00:56:04.169 --> 00:56:07.049
<v Val Levitan>I don't understand the question. Can you explain that to me?</v>

00:56:07.249 --> 00:56:26.769
<v Juan Martinez>Sure. So the agreements are mainly done. The customer has yet to see what he's signing. One of the documents is 10 pages. He could say, oh, I need my lawyers to review. I'll get it back to you on Friday or next week. Do we move forward without the signed document?</v>

00:56:28.489 --> 00:56:37.049
<v Val Levitan>I don't need the signed document right now. I don't need it at all right now for this one location.</v>

00:56:34.089 --> 00:56:34.489
<v Juan Martinez>Okay.</v>

00:56:38.049 --> 00:56:39.369
<v Juan Martinez>I wanted to clarify that.</v>

00:56:41.529 --> 00:56:43.049
<v Val Levitan>Why is it 10 pages?</v>

00:56:44.409 --> 00:56:48.969
<v Juan Martinez>It's a giant master agreement there in indemnific.</v>

00:56:48.009 --> 00:56:48.649
<v Val Levitan>It's not.</v>

00:56:49.529 --> 00:56:50.569
<v Val Levitan>It's not ours.</v>

00:56:51.089 --> 00:56:54.249
<v Juan Martinez>It is ours. I did send it out for review.</v>

00:56:52.769 --> 00:56:55.929
<v Val Levitan>So, we invented that, we invented that agreement.</v>

00:56:56.249 --> 00:56:56.889
<v Juan Martinez>Yes.</v>

00:56:58.809 --> 00:57:16.809
<v Juan Martinez>That's why I also think we need to re-review that agreement. I've attempted to shorten it as much as I can, but the one-time master agreement is 10 pages. Subsequent agreements just refer to the master and are much shorter, but that one-time master agreement</v>

00:57:17.129 --> 00:57:18.649
<v Juan Martinez>Has to cover everything.</v>

00:57:19.769 --> 00:57:21.929
<v Val Levitan>No, I agree, but is it...</v>

00:57:24.729 --> 00:57:30.889
<v Val Levitan>I mean, if PAGS doesn't have any agreements and we have a 10-page agreement.</v>

00:57:30.969 --> 00:57:31.529
<v Nathan Carver>Mhm.</v>

00:57:32.009 --> 00:57:33.529
<v Val Levitan>And we're not gonna get anywhere.</v>

00:57:35.529 --> 00:57:47.929
<v Juan Martinez>I have no way of knowing what income, I'm sure, has some agreement. I mean, we're talking about thousands of dollars every day, potentially. Who would not provide a proper agreement?</v>

00:57:50.489 --> 00:57:56.489
<v Val Levitan>So are we okay for this particular one test without the agreement?</v>

00:57:57.929 --> 00:58:09.689
<v Juan Martinez>As long as you say we are, I am, I mean, we're going to try to get into the customer's hands right away here, but, you know, there's no guarantee. They're just going to say, OK, I'll sign it. Here it is.</v>

00:58:12.409 --> 00:58:21.369
<v Val Levitan>Yeah, I mean, I, the risk is so minimal, I just cannot even guess what the risk is. I mean, it's just extremely minimal.</v>

00:58:30.329 --> 00:58:49.089
<v Andrei Klimovich>So for Dwola, I've sent the e-mail from Pavel right now that we've asked Dwola if there is anything still needed to be signed before we can finally register the location. So hopefully they will reply today. If they are not in touch with us by the end of today, tomorrow we will go</v>

00:58:49.369 --> 00:58:51.529
<v Andrei Klimovich>With A workaround scenario, I guess.</v>

00:58:59.849 --> 00:59:00.409
<v Val Levitan>Okay.</v>

00:59:03.209 --> 00:59:03.929
<v Val Levitan>Andrei.</v>

00:59:05.289 --> 00:59:08.649
<v Val Levitan>We need the location nailed.</v>

00:59:12.169 --> 00:59:14.969
<v Andrei Klimovich>Okay, I got it. I know. I understand it. I mean...</v>

00:59:16.329 --> 00:59:17.209
<v Andrei Klimovich>I'll do my best.</v>

00:59:19.609 --> 00:59:20.969
<v Andrei Klimovich>I'll talk to Felipe right now.</v>

00:59:22.249 --> 00:59:25.929
<v Val Levitan>I think you should start negotiating with another operator as well.</v>

00:59:28.729 --> 00:59:34.969
<v Andrei Klimovich>Yeah, we got a short list. We're constantly talking to other operators. We're showing the machine. So we have a short list.</v>

00:59:36.449 --> 00:59:42.009
<v Andrei Klimovich>Let me talk to Felipe and we will get back to you with an update of where we are and what other options we have.</v>

00:59:42.889 --> 00:59:45.129
<v Val Levitan>Okay, okay, thank you very much.</v>

00:59:45.609 --> 00:59:46.169
<v Juan Martinez>Thanks.</v>

00:59:47.849 --> 00:59:48.649
<v Val Levitan>Thank you, bye-bye.</v>

00:59:49.169 --> 00:59:49.609
<v Pavel Frolov>Fine.</v>

00:59:49.209 --> 00:59:50.169
<v Nathan Carver>All right, thank you.</v>

00:59:49.289 --> 00:59:50.089
<v Andrei Klimovich>Thank you. Bye.</v>

