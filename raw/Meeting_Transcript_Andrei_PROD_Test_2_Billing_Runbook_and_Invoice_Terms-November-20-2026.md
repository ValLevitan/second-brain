# Raw Transcript — PROD test 2 with InComm kickoff
**Date:** November 20, 2026, ~10:02 AM – ~10:35 AM Eastern (recording)
**Summary note:** [[Meeting_Notes_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026]]
---
WEBVTT

00:00:03.278 --> 00:00:06.758
<v Andrei Klimovich>Continue eager, yeah, in person, yeah.</v>

00:00:04.758 --> 00:00:06.518
<v Igor Donis>Nice, nice to meet you, yeah.</v>

00:00:09.398 --> 00:00:11.158
<v Igor Donis>Hi Pavel, good morning.</v>

00:00:15.078 --> 00:00:15.958
<v Val Levitan>Hello.</v>

00:00:16.838 --> 00:00:17.478
<v Felipe Miranda Giorgi>Morning.</v>

00:00:17.238 --> 00:00:17.798
<v Pavel Frolov>Good morning.</v>

00:00:17.878 --> 00:00:18.678
<v Nathan Carver>Good morning.</v>

00:00:18.238 --> 00:00:18.918
<v Igor Donis>Good morning.</v>

00:00:21.718 --> 00:00:22.998
<v Andrei Klimovich>Okay, so...</v>

00:00:24.118 --> 00:00:45.158
<v Andrei Klimovich>I have initiated this call because we have a number of open items for our prod test 2 and actually the going live with our first real location. And I'd like to go through those points. Let me open this e-mail that I've sent yesterday and we can go.</v>

00:00:45.718 --> 00:00:56.118
<v Andrei Klimovich>point by point to make sure that it is either already implemented or if it's not done yet, we need to end up with exact date and responsible person.</v>

00:00:58.918 --> 00:01:05.798
<v Igor Donis>Yeah, but maybe we need we need a way a waiting for Lev. I don't know if we need a...</v>

00:01:06.998 --> 00:01:07.598
<v Igor Donis>For Lev.</v>

00:01:09.318 --> 00:01:16.678
<v Andrei Klimovich>Oh yeah, good point. Lev is invited. He is in the list, but I'm not sure if he's going to join us.</v>

00:01:18.998 --> 00:01:20.038
<v Igor Donis>Okay.</v>

00:01:20.358 --> 00:01:27.958
<v Val Levitan>Send a message to Lev that he may need a reminder. He's an important contributor. Very smart guy.</v>

00:01:32.758 --> 00:01:34.358
<v Andrei Klimovich>Let me send him a message.</v>

00:01:43.238 --> 00:01:44.598
<v Felipe Miranda Giorgi>Lev is there now.</v>

00:01:47.078 --> 00:01:49.078
<v Andrei Klimovich>Oh, okay. So we are all here.</v>

00:01:52.238 --> 00:01:53.398
<v Val Levitan>Is the recording on?</v>

00:01:54.278 --> 00:01:55.718
<v Andrei Klimovich>Yes, it's on.</v>

00:01:55.678 --> 00:01:57.238
<v Val Levitan>Thank you. Let's begin.</v>

00:02:00.118 --> 00:02:08.118
<v Andrei Klimovich>Okay, so let's take it piece by piece. So the first one, location, billing, settings, and production confirmed.</v>

00:02:09.998 --> 00:02:10.118
<v Andrei Klimovich>Um...</v>

00:02:11.878 --> 00:02:15.478
<v Andrei Klimovich>I'm not sure about the specific part of it, like Nathan.</v>

00:02:16.598 --> 00:02:18.598
<v Andrei Klimovich>Can you give us more details on that?</v>

00:02:20.998 --> 00:02:30.598
<v Nathan Carver>So I, okay, so I think it's going to be me meeting with Pavel's team and just figuring out if this has been deployed recently. So I have a...</v>

00:02:31.558 --> 00:02:45.878
<v Nathan Carver>I have two runbooks, one for deployment and verification of configuration, and then the second is to recover the invoice from our first test run. So those two things have to happen.</v>

00:02:46.958 --> 00:02:54.518
<v Nathan Carver>before this would be ready to run another customer, another test, or run any invoice through the system.</v>

00:02:58.198 --> 00:03:05.238
<v Andrei Klimovich>So again, like, let me apologize if I will sound a little bit pushy here, but can we...</v>

00:03:07.638 --> 00:03:17.318
<v Andrei Klimovich>like get a date when you would expect it to be done. So you have a call with Pavel and then you update us with the release date.</v>

00:03:20.198 --> 00:03:26.598
<v Nathan Carver>So we can do that right away. So like I've shared the runbooks. I just need feedback that.</v>

00:03:27.678 --> 00:03:34.678
<v Nathan Carver>you know, this will work and that they're ready to go. The piece that I'm working on now is...</v>

00:03:36.598 --> 00:03:39.878
<v Nathan Carver>the invoice side. So the automated distribution of the invoice.</v>

00:03:41.278 --> 00:03:56.758
<v Nathan Carver>And that's at the tail end, so that's all MSBC, sending out the invoice. And the last, at the very end of this, is the reconciliation with CIBC. That still needs to be integrated with the bank.</v>

00:03:58.438 --> 00:04:02.118
<v Nathan Carver>So I have that scoped out and I can reprioritize that.</v>

00:04:04.198 --> 00:04:17.398
<v Nathan Carver>But as of right now, it's been deprioritized on my list of work. But we can change that. And if you need a timeline, do you have a timeline where you want to run? Or is it as soon as we get done? Like what is our...</v>

00:04:17.238 --> 00:04:39.398
<v Andrei Klimovich>Yes, as soon as we get done, and I would even say as soon as possible, because we already have everything ready for installations, and we've been honest with you, we've already postponed the release a couple of times with our customer. So in a perfect world, I would expect that we go to the location next week,</v>

00:04:39.478 --> 00:04:58.878
<v Andrei Klimovich>let's say Wednesday or Thursday, and we are sure that everything in the back end is ready. Like the invoices are being issued, they have been sent, the wallet is being paid, money go all the way like from income, sorry, from JVL to income, from location to JVL. Everything works like a charm.</v>

00:05:02.118 --> 00:05:06.198
<v Nathan Carver>Okay, so you has, I don't know if this has gone through testing.</v>

00:05:09.238 --> 00:05:09.958
<v Nathan Carver>So...</v>

00:05:09.638 --> 00:05:27.238
<v Andrei Klimovich>So testing is the same testing as we did last time, right? So we can agree with incomes that we activate a number of test cards on a production environment. We see the invoice from income, we drag money from...</v>

00:05:28.518 --> 00:05:31.798
<v Andrei Klimovich>a bank account or the location, right? This test.</v>

00:05:33.718 --> 00:05:42.198
<v Nathan Carver>Okay, so is this, has the QA team tested the location billing module? Like, I really don't know what's going on with this.</v>

00:05:44.278 --> 00:05:54.758
<v Nathan Carver>So I sent messages last month with the runbooks, with my status. Since that time, I've been reprioritized to other JVL work.</v>

00:05:55.878 --> 00:06:02.998
<v Nathan Carver>And I'm totally happy to get back into this. I just, it's not been on my radar with the limited time I have.</v>

00:06:04.998 --> 00:06:19.558
<v Nathan Carver>So I don't know if location billing has been pushed into QA, if QA has looked at it, if they've reviewed the runbooks that I have. And it's fine either way. I just need to know what's the status so I know how to respond and start planning.</v>

00:06:20.198 --> 00:06:21.878
<v Andrei Klimovich>Yeah, so puddle.</v>

00:06:21.198 --> 00:06:36.118
<v Pavel Frolov>Actually, actually, our QA tested only until the moment when the real money is actually started to move.</v>

00:06:37.158 --> 00:06:56.398
<v Pavel Frolov>So this part is tested, but what Andrei is describing when we are using real cards and real invoices and these invoices need to go through the workflow.</v>

00:06:56.518 --> 00:07:07.478
<v Pavel Frolov>and up to Business Central. This part is not on our site. I mean, it's impossible to test on QA.</v>

00:06:56.998 --> 00:06:57.478
<v Nathan Carver>Okay.</v>

00:07:06.838 --> 00:07:14.838
<v Nathan Carver>Correct. Correct. Okay. So the module has gone to QA, but we haven't integrated with Incom and Duala yet.</v>

00:07:14.198 --> 00:07:14.598
<v Pavel Frolov>Yes.</v>

00:07:17.558 --> 00:07:18.038
<v Nathan Carver>All right.</v>

00:07:20.998 --> 00:07:34.278
<v Pavel Frolov>So at least we need to pass additional testing, the same as we tried previous time, when Andrei tried to issue some cards and to see what is going on with all the steps.</v>

00:07:27.838 --> 00:07:28.318
<v Nathan Carver>Mmh.</v>

00:07:36.038 --> 00:07:40.278
<v Pavel Frolov>location billing, location manager, statuses, and so on.</v>

00:07:38.918 --> 00:07:39.398
<v Nathan Carver>Okay.</v>

00:07:42.918 --> 00:07:44.118
<v Nathan Carver>And so...</v>

00:07:45.198 --> 00:07:50.438
<v Nathan Carver>What we need to do for location billing is the recovery.</v>

00:07:51.638 --> 00:08:10.518
<v Nathan Carver>runbook and what that includes, so the first pass, the invoice was stuck for a number of reasons. One was MSBC didn't have the proper configurations, which I've gone through with Igor and we've agreed upon those.</v>

00:08:10.838 --> 00:08:13.158
<v Nathan Carver>I do have a question that I saw. There was some...</v>

00:08:14.358 --> 00:08:17.558
<v Nathan Carver>conversation on the terms net 10 versus</v>

00:08:18.758 --> 00:08:30.998
<v Nathan Carver>Immediate, I don't know if that was invoice only, so I still need, we don't need to unpack that now, but I do need to understand that a little bit more, make sure we're not changing any MSPC settings before we go.</v>

00:08:33.718 --> 00:08:36.518
<v Nathan Carver>So anyway, to get the invoice unstuck, we...</v>

00:08:38.198 --> 00:08:52.998
<v Nathan Carver>We have to update MSBC. We created the services that would allow a signal from Payment Hub to reprocess invoices that have failed for non...</v>

00:08:54.518 --> 00:09:12.998
<v Nathan Carver>banking reasons. So they fail to initiate because of communication issues, right? Failures due to insufficient funds are a different matter. But so this invoice failed because of a bug or, you know, technical reasons. So the runbook will have us</v>

00:09:13.478 --> 00:09:18.278
<v Nathan Carver>re-initiate the payment process for that invoice so it'll go through income.</v>

00:09:19.398 --> 00:09:29.798
<v Nathan Carver>Or, or, I'm sorry, through Diwala and get and get processed, and then we'll go, the invoice will be sent, and it'll basically finish its journey flowing through MSPC.</v>

00:09:31.078 --> 00:09:34.838
<v Nathan Carver>So once we've done that, then the system would be ready for...</v>

00:09:36.758 --> 00:09:39.398
<v Nathan Carver>another test. So...</v>

00:09:40.758 --> 00:09:59.238
<v Nathan Carver>Again, I've been away from this. I need to get back into that runbook. I have shared it, so the team has it. And it describes everything we need to do. So once we do that, runbook will actually be a kind of an initial integration test within, or I'm sorry, with Duala and MSPC.</v>

00:09:59.678 --> 00:10:02.758
<v Nathan Carver>because that will get the invoice moving again and we'll see that flow.</v>

00:10:03.638 --> 00:10:03.878
<v Nathan Carver>Um...</v>

00:10:05.038 --> 00:10:14.598
<v Nathan Carver>So that would be a good first test to complete that runbook. And then you would be, in my opinion, ready to run another end-to-end.</v>

00:10:16.918 --> 00:10:33.798
<v Andrei Klimovich>So, Nathan, do I understand it correctly that this runbook that you mentioned, it also involves A Minsk team, Pavel or QA team to do their part of job? Or it's who are the people involved into resolving this?</v>

00:10:33.238 --> 00:10:37.638
<v Nathan Carver>Yeah, so it lists that. Let me, um, let me grab the link and share it.</v>

00:10:39.038 --> 00:10:43.878
<v Nathan Carver>So it's in the e-mail I had sent out, but I'm going to grab.</v>

00:10:45.798 --> 00:10:48.118
<v Nathan Carver>Grab the link to it and share it here.</v>

00:10:51.838 --> 00:10:52.838
<v Nathan Carver>Apologies.</v>

00:10:56.518 --> 00:10:59.798
<v Nathan Carver>But yes, so it calls out what needs to be done and who can do that.</v>

00:11:02.278 --> 00:11:11.918
<v Nathan Carver>And one of that is the actual the re-initiation of the processing would actually go through, it's a signal sent from payment hub, either the</v>

00:11:13.438 --> 00:11:21.878
<v Nathan Carver>I don't know, not sure which module the team decided to send that from, but that's where that signal would come from, to location billing, indicating it should reprocess.</v>

00:11:22.998 --> 00:11:24.198
<v Nathan Carver>Um, the invoice.</v>

00:11:34.678 --> 00:11:36.838
<v Nathan Carver>See that e-mail? Let me just go get it.</v>

00:11:41.238 --> 00:11:47.398
<v Nathan Carver>So that part is just us coordinating together, getting that executed. Then the second part is...</v>

00:11:49.558 --> 00:11:53.558
<v Nathan Carver>the end of the chain of reconciliation with the bank.</v>

00:11:55.638 --> 00:12:08.358
<v Nathan Carver>You can go without that if you only have a few, right? But we want to get to full automated reconciliation so that there's nobody in MSBC having to do the reconciliation.</v>

00:12:16.438 --> 00:12:20.678
<v Andrei Klimovich>Sorry, do you want to share this runbook you're referring to or?</v>

00:12:20.838 --> 00:12:28.038
<v Nathan Carver>Yeah, I didn't see the e-mail offhand, so I'm going to go grab the runbook. So apologies, I'll share it here in a second.</v>

00:12:30.478 --> 00:12:31.798
<v Nathan Carver>As soon as I find a spot.</v>

00:12:33.998 --> 00:12:34.838
<v Pavel Frolov>Probably this one.</v>

00:12:37.638 --> 00:12:38.678
<v Nathan Carver>Yeah, Pavel found it.</v>

00:12:40.998 --> 00:12:41.478
<v Nathan Carver>That's it.</v>

00:12:42.558 --> 00:12:43.158
<v Nathan Carver>Thank you, Pavel.</v>

00:13:10.598 --> 00:13:18.918
<v Andrei Klimovich>Unfortunately, I do not have access to this part of GitHub, so Nathan, if you can share the screen, that will be...</v>

00:13:22.918 --> 00:13:24.918
<v Nathan Carver>OK, let me see if...</v>

00:13:24.358 --> 00:13:24.678
<v Pavel Frolov>Of.</v>

00:13:26.678 --> 00:13:31.238
<v Pavel Frolov>Nathan, are you okay to meet with our team tomorrow, for example?</v>

00:13:33.798 --> 00:13:34.198
<v Pavel Frolov>Of...</v>

00:13:36.998 --> 00:13:41.078
<v Pavel Frolov>What's A suitable day for our common discussion?</v>

00:13:41.638 --> 00:13:42.278
<v Nathan Carver>Um...</v>

00:13:43.158 --> 00:13:44.518
<v Nathan Carver>I can do Monday morning.</v>

00:13:46.198 --> 00:13:48.838
<v Nathan Carver>Or are you guys working on this through the weekend? Like, what's the...</v>

00:13:49.078 --> 00:13:51.718
<v Pavel Frolov>Yes, we were working on our weekends.</v>

00:13:53.958 --> 00:13:59.398
<v Pavel Frolov>I can invite Tsimanov Chudzinau and Tsimanov both these days.</v>

00:14:01.318 --> 00:14:02.198
<v Pavel Frolov>Like this.</v>

00:14:01.638 --> 00:14:03.158
<v Nathan Carver>Um, let's do it.</v>

00:14:05.558 --> 00:14:08.438
<v Nathan Carver>Yeah, let's do it early tomorrow. It'd be fine.</v>

00:14:19.558 --> 00:14:38.398
<v Andrei Klimovich>So do I understand it correctly that the first, the whole block of system, like all those open items, there will be covered tomorrow. You will reconciliate all open items and as a result, you will update us with...</v>

00:14:39.238 --> 00:14:42.758
<v Andrei Klimovich>expected date when it all will be fixed and deployed.</v>

00:14:44.518 --> 00:14:58.518
<v Pavel Frolov>At least we need to understand this runbook to go through the points. Actually, right now, I do not see any dependency on other services except for Business Central, dual and location building.</v>

00:14:59.878 --> 00:15:00.838
<v Pavel Frolov>Probably is.</v>

00:15:01.718 --> 00:15:02.198
<v Nathan Carver>Correct.</v>

00:15:01.998 --> 00:15:02.838
<v Pavel Frolov>Me too.</v>

00:15:03.798 --> 00:15:05.718
<v Pavel Frolov>Need more time to investigate.</v>

00:15:08.598 --> 00:15:19.238
<v Nathan Carver>Yes, definitely, because there was a service contracts that we had between payment hub and location billing, or I believe the...</v>

00:15:20.998 --> 00:15:24.198
<v Nathan Carver>Location Manager and Location Billing, so...</v>

00:15:25.158 --> 00:15:25.638
<v Nathan Carver>Um...</v>

00:15:26.998 --> 00:15:28.598
<v Pavel Frolov>Okay, I will ask.</v>

00:15:27.318 --> 00:15:29.798
<v Nathan Carver>We need to make sure that that handshake is good.</v>

00:15:30.358 --> 00:15:38.358
<v Pavel Frolov>I will ask Dima and Serge to go through this document to be prepared for tomorrow's call.</v>

00:15:40.238 --> 00:15:51.958
<v Pavel Frolov>Probably, if if you find something related to our internal services, they need to understand what is going on and what should they do to fix.</v>

00:15:54.358 --> 00:15:56.518
<v Nathan Carver>Yes, okay. That sounds good.</v>

00:15:59.878 --> 00:16:08.998
<v Andrei Klimovich>Okay, so the next one is about location invoice. So it's in a different e-mail thread, but...</v>

00:16:10.518 --> 00:16:11.878
<v Andrei Klimovich>As far as I see it.</v>

00:16:13.118 --> 00:16:33.718
<v Andrei Klimovich>As of today, the mock-up of this invoice is provided the latest version, and wordings need to be approved by Igor and Lev, and if it's all good, it should be implemented on a Business Central site, so it will be generated exactly in this way as we approve it.</v>

00:16:34.438 --> 00:16:51.078
<v Andrei Klimovich>For the terms, based on Val's feedback, we are not providing 10 days net or anything like that. So it works immediately. So the date is issued, it is the date when we expect the funds to be received.</v>

00:16:55.318 --> 00:17:04.278
<v Igor Donis>I tried to explain it, but I prefer explaining in Spanish to Felipe, help me to the translate, please.</v>

00:17:06.358 --> 00:17:06.798
<v Felipe Miranda Giorgi>Okay.</v>

00:17:09.078 --> 00:17:27.878
<v Igor Donis>OK, corrector los terminos y los terminos y la direction el testo en cuanto los testos terminos y direction de aquedo lo que approval y'll already say he implemented a ser el cambion el systema you're not you're not possibly a ser el cambion.</v>

00:17:28.118 --> 00:17:52.718
<v Igor Donis>Yo Tia Cuerdo con lo que de finio Val. E puest case implemented. Si puercer a Lev King. I can be a la Ultima version can be O Andrei de Los Nuevos terminos que Mencia no Val que a pro mobile. Hey, it's so looking at your so de la de financia encuanto a terminos y texto la direction.</v>

00:17:52.838 --> 00:17:55.318
<v Igor Donis>David, I said.</v>

00:17:56.558 --> 00:17:58.118
<v Igor Donis>Okay.</v>

00:18:00.998 --> 00:18:01.798
<v Igor Donis>Hey.</v>

00:18:09.238 --> 00:18:22.598
<v Felipe Miranda Giorgi>Okay, so Igor said that regarding the terms and direction on what's on his plates as per Val's approval, there needs to be some changes in the system. He does not.</v>

00:18:23.798 --> 00:18:42.438
<v Felipe Miranda Giorgi>He cannot make those changes in the system, so he would ask, or Lev would be the person responsible to making those changes agreed by Val, and that he agrees also, that should be the direction. But basically, in order to change the terms, he needs Lev's assistance.</v>

00:18:42.598 --> 00:18:44.798
<v Felipe Miranda Giorgi>To change the terms as profiles direction.</v>

00:18:46.438 --> 00:19:05.718
<v Igor Donis>I will drop on Tomas que se mention no correct pector of terminus que Val mention no or a provo por que no tabaclaro estonio a commercial que civa general interest sinos epaga de intro periodo de en simiento and to say que okay so the saline album.</v>

00:19:05.798 --> 00:19:24.198
<v Igor Donis>Factura or siesta dentro contractor cliente pero en el compunto de Saberel cliente que si vences of Factura E MPs activate lo interesa de acuerdor con venue.</v>

00:19:25.158 --> 00:19:44.758
<v Felipe Miranda Giorgi>Okay. Also something that was discussed in the invalid proof regarding terms is the fact that if the invoice is not paid on due date, it will generate interest. And this interest must be, I mean, the fact that there will be</v>

00:19:45.078 --> 00:19:52.438
<v Felipe Miranda Giorgi>Interest generated, if not paid on time, should be somewhere in the invoice or in the contract with the customer.</v>

00:19:53.398 --> 00:19:54.358
<v Igor Donis>No Ivan.</v>

00:19:54.358 --> 00:19:56.198
<v Felipe Miranda Giorgi>Val, you are muted. Yeah.</v>

00:19:57.318 --> 00:20:08.358
<v Val Levitan>That's a good point on interest. I think invoice payment is on the date of invoices not negotiable.</v>

00:20:09.238 --> 00:20:11.958
<v Val Levitan>But interest should probably start.</v>

00:20:13.558 --> 00:20:15.718
<v Val Levitan>Five days later, or seven days later.</v>

00:20:17.038 --> 00:20:17.878
<v Val Levitan>That's a good point.</v>

00:20:18.598 --> 00:20:25.878
<v Felipe Miranda Giorgi>What Igor is saying is that it should be written somewhere in the agreement or somewhere in the invoice or the agreement with the with the master.</v>

00:20:26.838 --> 00:20:38.758
<v Val Levitan>Yes, correct. We don't have any agreements in place yet. So as a point of interest, it should be decoupled from</v>

00:20:39.638 --> 00:20:41.478
<v Val Levitan>The date when the payment is due.</v>

00:20:43.238 --> 00:20:43.718
<v Igor Donis>Okay.</v>

00:20:48.358 --> 00:20:52.278
<v Igor Donis>That is all my points about this blog, Andrei.</v>

00:20:54.198 --> 00:20:54.758
<v Andrei Klimovich>Okay.</v>

00:20:56.918 --> 00:21:05.398
<v Nathan Carver>So, the thing of note here, sorry, when it comes to MSPC, my understanding, which is...</v>

00:20:57.278 --> 00:21:00.038
<v Andrei Klimovich>Again, is it sorry?</v>

00:21:06.558 --> 00:21:14.438
<v Nathan Carver>still pretty new to it, is it can apply interest based on the term you set on the invoice. However...</v>

00:21:15.398 --> 00:21:17.958
<v Nathan Carver>It doesn't see that money until that.</v>

00:21:20.038 --> 00:21:31.078
<v Nathan Carver>It's been that transaction has been added to MSBC, and that won't occur until the timeline of the transaction ACH transactions has finished.</v>

00:21:31.718 --> 00:21:33.558
<v Val Levitan>Which is, which is probably.</v>

00:21:31.958 --> 00:21:34.838
<v Nathan Carver>So we may initiate, I'm sorry.</v>

00:21:34.438 --> 00:21:36.118
<v Val Levitan>Which is probably 3 days, right?</v>

00:21:37.798 --> 00:21:42.998
<v Nathan Carver>Well, it could be up to five days, depending on if we hit holiday or weekend, yeah.</v>

00:21:40.278 --> 00:21:41.798
<v Val Levitan>Well, that's one, but...</v>

00:21:43.478 --> 00:21:51.958
<v Val Levitan>That's why I said five days, seven days. I mean, if you want to be safe, let's pick seven days and start your interest count. The interest is daily.</v>

00:21:46.598 --> 00:21:47.158
<v Nathan Carver>It cracked.</v>

00:21:53.158 --> 00:21:53.638
<v Andrei Klimovich>Mhm.</v>

00:21:53.478 --> 00:21:58.918
<v Val Levitan>Based on 35% per year, divided the number of days, non-compounded.</v>

00:22:01.238 --> 00:22:02.038
<v Nathan Carver>Okay, yep.</v>

00:22:01.558 --> 00:22:03.958
<v Val Levitan>So it's a simple daily interest.</v>

00:22:05.478 --> 00:22:05.798
<v Igor Donis>Yeah.</v>

00:22:07.078 --> 00:22:16.918
<v Andrei Klimovich>Okay, so from my side, I'll make sure that I will update this invoice mock. And I will also send a message to Monica, who is working on the contract, that it should be stated there too.</v>

00:22:17.558 --> 00:22:18.198
<v Val Levitan>Yes, Sir.</v>

00:22:19.398 --> 00:22:19.798
<v Andrei Klimovich>Um...</v>

00:22:21.038 --> 00:22:34.918
<v Andrei Klimovich>Okay, so Igor, thank you for this update and overview. One last question from my side. Can we convert it into expected date when it will be covered and ready?</v>

00:22:36.038 --> 00:22:39.678
<v Val Levitan>I think he asked the lever question: when can lever?</v>

00:22:40.878 --> 00:22:44.598
<v Val Levitan>to the internal work inside of.</v>

00:22:45.798 --> 00:22:49.158
<v Val Levitan>I must be so Igor could do his part.</v>

00:22:54.438 --> 00:22:54.918
<v Andrei Klimovich>I will.</v>

00:22:54.598 --> 00:22:57.158
<v Igor Donis>Felipe, may you, may you, Felipe?</v>

00:22:56.438 --> 00:23:13.358
<v Felipe Miranda Giorgi>Say, was it coming to the study? Sendo Andrei que entos para cuando on timeline on official limit on the two-part the poster termina pero a la grego que to depend this and la pregunta Kelly system left on the left there can be a loose terminus in the system.</v>

00:23:11.558 --> 00:23:12.518
<v Igor Donis>Wait, wait.</v>

00:23:14.838 --> 00:23:15.158
<v Felipe Miranda Giorgi>Yeah.</v>

00:23:18.118 --> 00:23:26.038
<v Felipe Miranda Giorgi>Yeah, so Andrei, it really depends on when or better said, Igor.</v>

00:23:25.318 --> 00:23:28.038
<v Val Levitan>Yeah, yeah, yeah, guys, guys, guys, stop.</v>

00:23:29.238 --> 00:23:41.718
<v Val Levitan>Lev understands the question, he's thinking about it. I can read his mind because his bioenergy is very strong, he's staring at the screen. So now he's going to unmute himself and vocalize what he thinks.</v>

00:23:46.678 --> 00:23:47.718
<v Val Levitan>Lev, you are on mute.</v>

00:23:49.678 --> 00:23:51.558
<v Lev Rudky>No, I'm not, am I?</v>

00:23:52.118 --> 00:23:55.158
<v Val Levitan>Yeah, no, you're good now. When can you make the change?</v>

00:23:56.478 --> 00:24:10.278
<v Lev Rudky>Okay, there are no problems to create an appropriate payment term in the system. It's practically immediate. But in terms of invoice layout.</v>

00:24:13.638 --> 00:24:14.038
<v Lev Rudky>I...</v>

00:24:16.358 --> 00:24:23.638
<v Lev Rudky>Why can't we use the existing layout like the standard layout? Can we?</v>

00:24:22.838 --> 00:24:30.518
<v Andrei Klimovich>We can, we can, no issues. It's a question only about the content of the invoice, that it should be approved content, not the layout itself.</v>

00:24:32.598 --> 00:24:36.518
<v Val Levitan>The content you're talking about, description of the service, right?</v>

00:24:37.078 --> 00:24:41.238
<v Andrei Klimovich>Description of the service, terms of payment, all this stuff.</v>

00:24:42.678 --> 00:24:52.278
<v Val Levitan>And by a preview, by a preview, basically saying produce the test invoice and show it to you.</v>

00:24:43.158 --> 00:24:44.038
<v Andrei Klimovich>Address.</v>

00:24:53.438 --> 00:24:59.798
<v Val Levitan>So you could approve the company. Did I understand you correctly?</v>

00:25:00.678 --> 00:25:20.718
<v Andrei Klimovich>Yeah, so from my side, we already have a mock-up with approved content. So now it's the task to implement it on MSBC side that the content will be exactly as approved mock-up, but not the layout. Then we generate this invoice from...</v>

00:25:01.078 --> 00:25:01.198
<v Val Levitan>Yeah.</v>

00:25:20.838 --> 00:25:24.598
<v Andrei Klimovich>MSBC, send it back to me and you, and we approve it.</v>

00:25:25.238 --> 00:25:31.958
<v Val Levitan>You're basically saying, Lev Igor, show me the mock-up invoice. That's what you're asking.</v>

00:25:33.318 --> 00:25:34.838
<v Lev Rudky>Just for starters, yeah.</v>

00:25:36.198 --> 00:25:40.998
<v Val Levitan>So, point well taken, yes, please show it, show, show the mock-up invoice.</v>

00:25:42.038 --> 00:26:02.838
<v Igor Donis>Yeah, well, a last question, Andrei, in your last e-mail before the last e-mail, you sent to all us the points discussed with you and Val accordingly to the terms, the final terms. If I understand good.</v>

00:26:04.518 --> 00:26:08.438
<v Igor Donis>In your previously e-mail, you sent to...</v>

00:26:07.558 --> 00:26:08.678
<v Andrei Klimovich>Yes, yes, we, we...</v>

00:26:09.558 --> 00:26:19.798
<v Igor Donis>That is the terms that they appear of showing the invoice, because it's the final version from Val, according to your discussion, yes?</v>

00:26:09.998 --> 00:26:10.838
<v Andrei Klimovich>Which is it?</v>

00:26:20.718 --> 00:26:27.238
<v Andrei Klimovich>Yes, correct, but now we have one more change that this interest should start with day 7, not immediately.</v>

00:26:26.038 --> 00:26:29.478
<v Igor Donis>Exactly. Right. Exactly. Okay.</v>

00:26:36.278 --> 00:26:37.158
<v Andrei Klimovich>OK, so.</v>

00:26:39.438 --> 00:26:46.358
<v Andrei Klimovich>When shall we expect this invoice to be presented for review and approval? Like Monday?</v>

00:26:47.518 --> 00:26:47.958
<v Andrei Klimovich>Tuesday.</v>

00:26:49.078 --> 00:26:49.638
<v Andrei Klimovich>Tomorrow?</v>

00:26:51.198 --> 00:26:52.118
<v Lev Rudky>Are you asking me?</v>

00:26:54.838 --> 00:26:58.998
<v Andrei Klimovich>I'm not sure about who's going to implement the invoice itself, so...</v>

00:27:00.038 --> 00:27:02.038
<v Andrei Klimovich>It's either you or Igor, I don't know.</v>

00:27:02.518 --> 00:27:09.478
<v Igor Donis>Allow me, allow me a a for the school the the final version with Lev and and send it.</v>

00:27:08.758 --> 00:27:13.638
<v Val Levitan>No, no, no, no, no, no, no, no, no, no, we don't have time.</v>

00:27:14.198 --> 00:27:17.878
<v Igor Donis>Okay, well Lev, what you time? What you time?</v>

00:27:17.318 --> 00:27:20.038
<v Val Levitan>One hour, one hour, get back to me in one hour.</v>

00:27:20.678 --> 00:27:21.158
<v Igor Donis>Okay.</v>

00:27:25.318 --> 00:27:31.638
<v Lev Rudky>If it requires customizations, I won't be able to tell you. OK.</v>

00:27:28.038 --> 00:27:32.278
<v Val Levitan>No customization. No, we don't need customization. Don't need customization.</v>

00:27:32.998 --> 00:27:33.638
<v Lev Rudky>Okay.</v>

00:27:35.318 --> 00:27:37.478
<v Val Levitan>Present an invoice to Andrei in one hour.</v>

00:27:38.518 --> 00:27:42.838
<v Igor Donis>After this meeting, Blev and I meeting.</v>

00:27:38.838 --> 00:27:39.078
<v Val Levitan>Yeah.</v>

00:27:43.958 --> 00:27:46.038
<v Andrei Klimovich>Okay, beautiful. Thank you so much.</v>

00:27:46.918 --> 00:27:55.398
<v Andrei Klimovich>So the last part is about the monthly fee, which slipped under our radar and...</v>

00:27:57.558 --> 00:27:58.918
<v Andrei Klimovich>The current system.</v>

00:28:00.038 --> 00:28:13.398
<v Andrei Klimovich>As far as I understand, we don't have a specific invoice type right now, which will be billed on a monthly basis for amount of $90, which</v>

00:28:13.238 --> 00:28:33.478
<v Val Levitan>The amount depends on what we charge. The description should be a reoccurring monthly connection service. The reoccurring invoice is a standard procedure for every accounting package. I suspect, I don't know for sure, subject for less confirmation.</v>

00:28:33.958 --> 00:28:46.198
<v Val Levitan>Recurring invoice is just a matter of setup in Microsoft Business Central. This invoice has to be produced at the same day, on the first day of the month. It has to be...</v>

00:28:47.398 --> 00:29:06.078
<v Val Levitan>For a minimum of 30 days, sorry, for a minimum of one day, if the connection service was rendered only for one day, it would take 90 days divided by the number of days in the month.</v>

00:29:06.598 --> 00:29:08.198
<v Val Levitan>And we charge in that invoice.</v>

00:29:09.638 --> 00:29:21.238
<v Val Levitan>The invoices have to be reoccurring. The marker for connection is when connection is made with with income or date of installation, I'm sorry.</v>

00:29:23.478 --> 00:29:38.118
<v Val Levitan>So, we need to catch the date of installation, and we need that marker. We need that marker reflected in Microsoft Business Central. From there, we count number of full number of days, 24 hours.</v>

00:29:26.718 --> 00:29:27.318
<v Andrei Klimovich>Mm-hmm.</v>

00:29:39.958 --> 00:29:44.678
<v Val Levitan>And minimum billing period is 24 hours.</v>

00:29:47.078 --> 00:29:51.038
<v Andrei Klimovich>Okay, what is the interest rate again? Like the same, 35%?</v>

00:29:50.598 --> 00:29:53.318
<v Val Levitan>Same, same, pay, pay on invoice.</v>

00:29:54.118 --> 00:29:57.398
<v Andrei Klimovich>Okay, okay, and the seven days.</v>

00:29:56.278 --> 00:29:56.838
<v Val Levitan>Ohh.</v>

00:29:58.198 --> 00:30:05.078
<v Val Levitan>Forgive me, we're charging the operator different. Everything changes to...</v>

00:30:07.238 --> 00:30:12.198
<v Val Levitan>net 15 days and interest starts at day 31.</v>

00:30:16.278 --> 00:30:18.198
<v Felipe Miranda Giorgi>Are we always charging the master Val?</v>

00:30:20.038 --> 00:30:21.398
<v Felipe Miranda Giorgi>I don't think that's the case.</v>

00:30:22.038 --> 00:30:28.758
<v Val Levitan>I'm 99% sure that this is the case. If it's not, we'll meet again and we'll adjust again.</v>

00:30:29.238 --> 00:30:29.638
<v Felipe Miranda Giorgi>Okay.</v>

00:30:30.558 --> 00:30:48.998
<v Andrei Klimovich>Okay, so the good news is that on the payment hub side, there is already capabilities and requirements describing exactly the way how you described it right now, with additional features that we can choose, either it's master or location, but we can simplify it, make master only for now.</v>

00:30:49.878 --> 00:30:53.798
<v Val Levitan>If that feature, I'm very sorry for interruption, if that feature is already in, keep it.</v>

00:30:50.598 --> 00:30:50.678
<v Andrei Klimovich>Uhh...</v>

00:30:55.318 --> 00:31:13.078
<v Andrei Klimovich>It's not implemented, it's described in the document. Great. Okay, okay, okay. Net 15 interest starts with day 31. Okay, I will create the same mock-up with the content for the invoice and I will share it with the team. Okay, done.</v>

00:30:58.278 --> 00:31:00.518
<v Val Levitan>Keep, keep it, keep, keep it.</v>

00:31:14.238 --> 00:31:33.718
<v Andrei Klimovich>Great. So action points, right? So Nathan and Pavel, you meet tomorrow, you go through all the opened items, and then you just provide us with expected dates, right? Very simple, very straightforward. Lev and Igor, I'm waiting for...</v>

00:31:34.798 --> 00:31:56.398
<v Andrei Klimovich>an invoice to approve with Val that everything looks good. From my side, I need to provide a content mock-up for a new invoice, which will go to a master location for monthly fee. Okay, then we see when we will be ready to run the test.</v>

00:31:58.438 --> 00:32:07.158
<v Felipe Miranda Giorgi>Just one correction. I understand that mock-up you're doing is for master exclusively, not master or location at the moment, but because of the terms.</v>

00:32:07.638 --> 00:32:18.598
<v Andrei Klimovich>I think that it should be business type agnostic. So it just goes to a specific pay, someone who will pay for it. And it's a, yeah, okay.</v>

00:32:10.918 --> 00:32:11.558
<v Felipe Miranda Giorgi>Oh, okay.</v>

00:32:16.038 --> 00:32:17.078
<v Felipe Miranda Giorgi>OK, understood.</v>

00:32:21.878 --> 00:32:31.798
<v Andrei Klimovich>Great. So no more questions from my side. I really appreciate your time and we've covered most of them. If you guys have any open questions, let's discuss them right now.</v>

00:32:38.038 --> 00:32:48.278
<v Pavel Frolov>Oh, Nathan, I already created the meeting. Please check, is it suitable time for you at 9 A.m.?</v>

00:32:39.238 --> 00:32:39.718
<v Andrei Klimovich>Okay.</v>

00:32:41.798 --> 00:32:42.038
<v Nathan Carver>Yeah.</v>

00:32:47.238 --> 00:32:47.718
<v Nathan Carver>Um...</v>

00:32:48.758 --> 00:32:52.358
<v Nathan Carver>Yes, that looks good. I saw it. So we're all set.</v>

00:32:49.438 --> 00:32:49.718
<v Pavel Frolov>So.</v>

00:32:53.918 --> 00:33:01.558
<v Andrei Klimovich>OK, so thank you so much, everyone, and enjoy the rest of your Friday. Take care.</v>

00:33:01.318 --> 00:33:02.998
<v Val Levitan>Thank you very much. Bye-bye.</v>

00:33:02.598 --> 00:33:03.238
<v Pavel Frolov>Thank you.</v>

00:33:02.598 --> 00:33:03.638
<v Nathan Carver>All right, thanks all.</v>

