# Raw Transcript — Review Payment Hub MSBC Configurations
**Date:** July 20, 2026, 2:07–2:40 PM Eastern
**Summary note:** [[Meeting_Notes_Payment_Hub_MSBC_Configurations-July-20-2026]]
---
WEBVTT

00:00:03.571 --> 00:00:23.011
<v Igor Donis>I don't, I don't have credential for configure 8 in Avatax that is related with Mister Lab, that is a regarding to the e-mail points from Nathan and.</v>

00:00:23.171 --> 00:00:43.091
<v Igor Donis>Last one, points related with the dimensions is I put I agree with Nathan, the only dimension code is dimension 0, code dimension 0, 0701.</v>

00:00:43.571 --> 00:01:05.011
<v Igor Donis>Sorry, sorry, sorry, sorry. Code dimensions is 0107, dimension by G1 and dimension by G2 is related to the intercompany is should be 0 code because all of this operation is only by</v>

00:00:49.171 --> 00:00:49.651
<v Nathan Carver>Mhm.</v>

00:01:05.811 --> 00:01:24.931
<v Igor Donis>by GBL system. It's not related with internet companies. OK? And they put in the code 0. Zero is nothing intercompany. And the dimension posted G1 shall be 0107. Do you in your</v>

00:01:24.451 --> 00:01:24.491
<v Nathan Carver>I.</v>

00:01:25.131 --> 00:01:32.531
<v Igor Donis>Previously, general entries, Nathan, take it the 0107. He said only one, okay?</v>

00:01:31.331 --> 00:01:31.571
<v Nathan Carver>Yeah.</v>

00:01:33.491 --> 00:01:34.931
<v Nathan Carver>0107.</v>

00:01:35.171 --> 00:01:36.291
<v Igor Donis>Yes, yes.</v>

00:01:36.131 --> 00:01:36.251
<v Nathan Carver>Yeah.</v>

00:01:37.891 --> 00:01:58.691
<v Igor Donis>Well, I don't know if I, that is, I think, Sean and Nathan related on my scope, but related with this code related with the other tax configuration, I can configuration related with the other tax.</v>

00:01:59.811 --> 00:02:05.251
<v Igor Donis>Maybe let help to us to the right configuration in other attacks.</v>

00:02:05.651 --> 00:02:18.851
<v Lev Rudky>I don't think so. I can, I can, I think if I have all all permissions to do anything there, you're talking about live environment or test environment.</v>

00:02:19.891 --> 00:02:27.171
<v Igor Donis>An environment, I using all checking the environment testing from Nathan in the sandbox.</v>

00:02:27.731 --> 00:02:31.891
<v Lev Rudky>I, I can, I can give you all permissions there, it's...</v>

00:02:33.411 --> 00:02:36.451
<v Lev Rudky>So, it's not it's not a problem, because...</v>

00:02:37.651 --> 00:02:44.051
<v Lev Rudky>I don't feel comfortable like messing with taxes and things like that.</v>

00:02:47.171 --> 00:02:48.051
<v Igor Donis>Okay, Val.</v>

00:02:49.651 --> 00:03:07.091
<v Igor Donis>But I think it with all terms relating with the Avalara tax or configuration in taxes is related with the address from the customers from using the payment hub, no?</v>

00:02:58.291 --> 00:02:58.451
<v Nathan Carver>Yeah.</v>

00:03:08.691 --> 00:03:09.251
<v Nathan Carver>Yes.</v>

00:03:10.731 --> 00:03:11.731
<v Nathan Carver>Yes, so.</v>

00:03:13.451 --> 00:03:13.731
<v Nathan Carver>Um...</v>

00:03:16.211 --> 00:03:21.811
<v Nathan Carver>Correct. So we're going to use AvaTax, but they're all non-taxable and that's how each line item.</v>

00:03:23.491 --> 00:03:26.291
<v Nathan Carver>will be added as non-taxable.</v>

00:03:27.331 --> 00:03:37.651
<v Igor Donis>Yeah, it's not taxable. All this, maybe Sean confer to us to this point. All this relate, all these.</v>

00:03:33.811 --> 00:03:33.891
<v Nathan Carver>Oh.</v>

00:03:39.491 --> 00:03:42.211
<v Sean Riley>It was, it was Juan that, yeah.</v>

00:03:40.931 --> 00:03:41.491
<v Igor Donis>Dance.</v>

00:03:42.851 --> 00:03:45.971
<v Igor Donis>It's 0 taxes now, it's no taxes.</v>

00:03:43.091 --> 00:03:43.811
<v Sean Riley>One.</v>

00:03:46.691 --> 00:03:48.211
<v Sean Riley>Yeah, Juan confirmed that.</v>

00:03:48.771 --> 00:03:49.811
<v Nathan Carver>Yeah, correct.</v>

00:03:52.291 --> 00:04:11.291
<v Igor Donis>Maybe in the batching, putting, I don't know, Nathan, maybe in the batching for translate to productive, is that all all operation under this payment hub is 0 or blocked to taxes related, you know?</v>

00:04:04.731 --> 00:04:04.851
<v Nathan Carver>Yes.</v>

00:04:13.091 --> 00:04:14.611
<v Nathan Carver>Yes, correct. So...</v>

00:04:15.811 --> 00:04:17.251
<v Nathan Carver>Let me.</v>

00:04:19.011 --> 00:04:19.731
<v Nathan Carver>Ashlee.</v>

00:04:24.171 --> 00:04:25.491
<v Nathan Carver>Let me see if I have this.</v>

00:04:31.491 --> 00:04:31.611
<v Igor Donis>Yeah.</v>

00:04:35.891 --> 00:04:37.011
<v Nathan Carver>957.</v>

00:04:48.131 --> 00:04:51.011
<v Nathan Carver>All right, let me check the other server.</v>

00:06:01.731 --> 00:06:03.571
<v Nathan Carver>Okay, so...</v>

00:06:09.571 --> 00:06:10.571
<v Nathan Carver>What is the?</v>

00:06:12.611 --> 00:06:14.691
<v Nathan Carver>What is the link again for closed?</v>

00:06:15.891 --> 00:06:17.091
<v Nathan Carver>or posted.</v>

00:06:18.931 --> 00:06:19.811
<v Nathan Carver>Orders.</v>

00:06:21.491 --> 00:06:24.451
<v Igor Donis>We can hear your screen, Nathan.</v>

00:06:23.731 --> 00:06:23.851
<v Nathan Carver>Yeah.</v>

00:06:27.011 --> 00:06:28.531
<v Igor Donis>We don't see your screen.</v>

00:06:29.251 --> 00:06:30.971
<v Nathan Carver>Oh, okay. And...</v>

00:06:34.291 --> 00:06:38.931
<v Nathan Carver>Let me pull up, let me share that then. Yeah, let me try this again.</v>

00:06:45.411 --> 00:06:45.731
<v Nathan Carver>Come on.</v>

00:07:05.571 --> 00:07:07.651
<v Nathan Carver>Okay, is the screen coming up?</v>

00:07:08.131 --> 00:07:08.611
<v Sean Riley>Yeah.</v>

00:07:08.851 --> 00:07:09.171
<v Lev Rudky>Yeah.</v>

00:07:09.731 --> 00:07:10.131
<v Igor Donis>Yeah.</v>

00:07:10.051 --> 00:07:10.171
<v Nathan Carver>Yes.</v>

00:07:11.491 --> 00:07:12.451
<v Nathan Carver>So.</v>

00:07:18.291 --> 00:07:20.691
<v Nathan Carver>Okay, so for customer.</v>

00:07:23.331 --> 00:07:23.571
<v Nathan Carver>Um...</v>

00:07:27.251 --> 00:07:28.611
<v Nathan Carver>No, this doesn't have any.</v>

00:07:30.131 --> 00:07:30.691
<v Nathan Carver>Okay.</v>

00:07:37.971 --> 00:07:38.131
<v Igor Donis>But.</v>

00:07:44.931 --> 00:07:46.611
<v Nathan Carver>OK, let me.</v>

00:07:48.531 --> 00:07:51.931
<v Nathan Carver>Posted sales invoices.</v>

00:07:57.091 --> 00:07:57.651
<v Nathan Carver>There they are.</v>

00:08:08.931 --> 00:08:10.891
<v Nathan Carver>That's in the far future.</v>

00:08:13.371 --> 00:08:14.611
<v Igor Donis>957.</v>

00:08:14.611 --> 00:08:14.691
<v Nathan Carver>The.</v>

00:08:23.331 --> 00:08:27.251
<v Nathan Carver>Okay, so for the invoices,</v>

00:08:30.291 --> 00:08:34.371
<v Nathan Carver>We are applying this non-taxable code here.</v>

00:08:35.651 --> 00:08:36.011
<v Igor Donis>Yeah.</v>

00:08:35.651 --> 00:08:39.971
<v Nathan Carver>And I believe the customer, if I go into...</v>

00:08:42.571 --> 00:08:44.531
<v Nathan Carver>Let's see, who is this customer?</v>

00:08:56.531 --> 00:09:03.171
<v Nathan Carver>They don't have dimensions set. Is it on the, it must be on the template. I always have to relearn how I'm doing this.</v>

00:09:01.891 --> 00:09:02.331
<v Igor Donis>But.</v>

00:09:06.931 --> 00:09:07.811
<v Nathan Carver>Okay.</v>

00:09:12.691 --> 00:09:19.171
<v Nathan Carver>Okay, so the terms we had to set was, this is set at COD.</v>

00:09:20.451 --> 00:09:26.051
<v Nathan Carver>But I think we have to set it at net 7 in order for invoices to renew.</v>

00:09:20.611 --> 00:09:22.291
<v Igor Donis>Oh, okay.</v>

00:09:24.131 --> 00:09:43.891
<v Igor Donis>No, no, no, no, no, sorry, sorry, Nathan. I I confirmed the the dimension for for normally in the in the in the customer requested, for example, no knowing in the terms in the terms.</v>

00:09:43.971 --> 00:09:57.571
<v Igor Donis>Is I don't have a, I don't have a school in intern because the terms from a commercial guys or agreement guys, yes?</v>

00:09:52.771 --> 00:09:52.891
<v Nathan Carver>Yeah.</v>

00:09:57.571 --> 00:09:57.731
<v Nathan Carver>Yeah.</v>

00:09:59.251 --> 00:10:02.691
<v Igor Donis>Okay, but if you use, if you use...</v>

00:10:00.091 --> 00:10:00.291
<v Nathan Carver>Hey.</v>

00:10:04.291 --> 00:10:23.291
<v Igor Donis>I don't know, Sean. I think the dimension is cash on delivery for all these operation, but I don't have a scope to decide what is the determined</v>

00:10:09.451 --> 00:10:09.571
<v Nathan Carver>The.</v>

00:10:16.851 --> 00:10:17.011
<v Nathan Carver>Right.</v>

00:10:20.131 --> 00:10:20.251
<v Nathan Carver>Yeah.</v>

00:10:23.451 --> 00:10:27.651
<v Igor Donis>Payables terms in this in these operations.</v>

00:10:28.611 --> 00:10:34.451
<v Igor Donis>Maybe Juan Juan Martinez explanation to that.</v>

00:10:34.851 --> 00:10:38.851
<v Sean Riley>Well, isn't everything happening on a daily basis? Like...</v>

00:10:40.291 --> 00:10:41.331
<v Nathan Carver>And so there.</v>

00:10:40.931 --> 00:10:41.171
<v Sean Riley>Okay.</v>

00:10:42.931 --> 00:10:47.491
<v Nathan Carver>So their purchase orders or their sales orders.</v>

00:10:48.851 --> 00:10:51.411
<v Nathan Carver>Will stay open until.</v>

00:10:54.131 --> 00:10:55.491
<v Nathan Carver>The cache is.</v>

00:10:56.771 --> 00:10:57.491
<v Nathan Carver>Deposited.</v>

00:10:58.691 --> 00:10:59.171
<v Sean Riley>Right.</v>

00:10:58.691 --> 00:10:59.251
<v Nathan Carver>So, it...</v>

00:11:01.091 --> 00:11:02.851
<v Sean Riley>But it's like done daily, isn't it?</v>

00:11:04.531 --> 00:11:14.611
<v Sean Riley>Like, wasn't when we were first setting this up, Val was very concerned about like the money closed every day, so there was never a credit risk to him, right?</v>

00:11:18.291 --> 00:11:22.691
<v Nathan Carver>So it takes us several days to move the money. So it's.</v>

00:11:22.291 --> 00:11:22.451
<v Sean Riley>But.</v>

00:11:23.891 --> 00:11:29.251
<v Sean Riley>But from the customer's point of view, they've paid, like the customer has sent the money.</v>

00:11:23.971 --> 00:11:24.531
<v Nathan Carver>On.</v>

00:11:31.731 --> 00:11:38.051
<v Nathan Carver>Correct. So from the customer's point of view, the transaction starts immediately.</v>

00:11:32.691 --> 00:11:33.091
<v Sean Riley>Yeah.</v>

00:11:38.451 --> 00:11:40.611
<v Sean Riley>Yes, so from the customers.</v>

00:11:39.411 --> 00:11:47.891
<v Nathan Carver>Yeah, so at the end of the day, we invoice and then immediately after we invoice, we're starting the...</v>

00:11:49.371 --> 00:11:50.211
<v Nathan Carver>transaction.</v>

00:11:52.771 --> 00:12:04.211
<v Sean Riley>So then it would be cash on demand. Like you're basically, that's what I would show on the invoice, would be cash on demand. We're invoicing you and that same day we're initiating the draw on the account.</v>

00:11:52.931 --> 00:11:53.411
<v Nathan Carver>So.</v>

00:11:58.691 --> 00:11:58.891
<v Nathan Carver>Right.</v>

00:12:05.571 --> 00:12:06.211
<v Nathan Carver>I see.</v>

00:12:07.051 --> 00:12:07.331
<v Sean Riley>Yeah.</v>

00:12:07.491 --> 00:12:09.331
<v Nathan Carver>Okay, that makes sense.</v>

00:12:10.371 --> 00:12:19.811
<v Igor Donis>Yeah, because I think it this operation is quickly is the money is coming in in short time.</v>

00:12:14.691 --> 00:12:15.171
<v Sean Riley>Mmh.</v>

00:12:15.011 --> 00:12:15.131
<v Nathan Carver>Yeah.</v>

00:12:22.611 --> 00:12:34.291
<v Sean Riley>Yeah, like from that customer point of view, you're taking the expectation is we're taking the money the same day we're invoicing you. Now, the bank, the banking transactions may lag a little bit because that's...</v>

00:12:25.931 --> 00:12:26.131
<v Nathan Carver>Yeah.</v>

00:12:35.891 --> 00:12:38.531
<v Sean Riley>the back-end side of it, but...</v>

00:12:40.051 --> 00:12:47.571
<v Sean Riley>If you put net seven days or something, the customer is going to think, well, I have seven days before you start to draw the money from my account, which is not right.</v>

00:12:49.651 --> 00:12:51.011
<v Nathan Carver>Yeah, that makes sense.</v>

00:12:53.491 --> 00:12:59.571
<v Nathan Carver>So in MSPC, are invoices then posted immediately on COD?</v>

00:13:04.211 --> 00:13:07.731
<v Sean Riley>Igor does it. It's probably posted immediately. Yeah, it would be.</v>

00:13:09.651 --> 00:13:12.531
<v Igor Donis>Sorry, sorry, I, I, I don't understand.</v>

00:13:09.971 --> 00:13:10.211
<v Nathan Carver>Okay.</v>

00:13:14.531 --> 00:13:24.131
<v Sean Riley>Nathan's asking if the terms are cash on delivery, does that trigger the invoice to be posted immediately in your system?</v>

00:13:27.171 --> 00:13:29.691
<v Igor Donis>In in this in invoicing on payment.</v>

00:13:32.531 --> 00:13:33.971
<v Sean Riley>in your accounting system.</v>

00:13:33.811 --> 00:13:33.931
<v Nathan Carver>Yeah.</v>

00:13:35.731 --> 00:13:44.771
<v Sean Riley>If you does the payment term, what triggers the invoice to get recorded in your system? Is it the payment terms or just the fact that an invoice is created?</v>

00:13:45.891 --> 00:13:47.571
<v Igor Donis>In the payment terms.</v>

00:13:48.291 --> 00:13:49.331
<v Sean Riley>The payment terms due.</v>

00:13:51.251 --> 00:13:51.491
<v Lev Rudky>The.</v>

00:13:54.691 --> 00:13:56.371
<v Lev Rudky>The fact that they...</v>

00:13:55.891 --> 00:13:56.051
<v Nathan Carver>I.</v>

00:13:57.571 --> 00:14:02.451
<v Lev Rudky>Payment terms and cash on delivery, it doesn't trigger anything.</v>

00:14:03.011 --> 00:14:09.331
<v Sean Riley>Yeah, I wouldn't think so. I would think the creation of the invoice causes the entry to get recorded.</v>

00:14:04.571 --> 00:14:04.931
<v Lev Rudky>Okay.</v>

00:14:12.291 --> 00:14:21.211
<v Sean Riley>So it needs enough, it shouldn't change from a book on the bookkeeping side, the journal entries and so on wouldn't change because the payment terms have changed.</v>

00:14:12.451 --> 00:14:13.011
<v Lev Rudky>Mm.</v>

00:14:12.771 --> 00:14:12.931
<v Nathan Carver>Mm.</v>

00:14:22.931 --> 00:14:31.331
<v Sean Riley>The invoice would be created the day we feel like we have a sale, like the day we make the transaction, we create the invoice, it would be recorded then.</v>

00:14:26.531 --> 00:14:26.651
<v Nathan Carver>Yeah.</v>

00:14:35.491 --> 00:14:38.531
<v Nathan Carver>So in MSPC, they have, there's the.</v>

00:14:39.771 --> 00:14:41.411
<v Nathan Carver>When an invoice is opened.</v>

00:14:43.091 --> 00:14:43.971
<v Nathan Carver>It has.</v>

00:14:47.171 --> 00:14:55.251
<v Nathan Carver>So for example, these, I think it goes under this ongoing sales invoice. And then it goes into a posted state.</v>

00:14:52.291 --> 00:14:52.771
<v Sean Riley>Okay.</v>

00:14:56.531 --> 00:14:58.531
<v Nathan Carver>And that actually changes.</v>

00:14:59.411 --> 00:15:02.531
<v Nathan Carver>the number on the invoice. So if I look at...</v>

00:15:07.011 --> 00:15:10.291
<v Nathan Carver>So this, this PS, so when an invoice is created.</v>

00:15:12.291 --> 00:15:16.371
<v Nathan Carver>I think it has a CS, it's a CS prefix, and then...</v>

00:15:17.731 --> 00:15:22.291
<v Nathan Carver>is posted, it switches it over to this PS prefix.</v>

00:15:22.611 --> 00:15:23.011
<v Igor Donis>Yeah.</v>

00:15:23.811 --> 00:15:24.371
<v Nathan Carver>So.</v>

00:15:27.411 --> 00:15:32.611
<v Nathan Carver>Yeah, right here. SO, that's what it is. Sales order. So it starts with a sales order.</v>

00:15:34.891 --> 00:15:38.531
<v Nathan Carver>and then it gets switched to a PS. And I think.</v>

00:15:40.531 --> 00:15:43.851
<v Nathan Carver>I'm trying to remember the testing that I went through, but the...</v>

00:15:46.211 --> 00:15:54.211
<v Nathan Carver>The COD is like an immediate, because it's cache, immediate cache, it's automatically posted.</v>

00:15:51.731 --> 00:15:52.051
<v Sean Riley>Right.</v>

00:15:55.571 --> 00:15:58.851
<v Nathan Carver>So the invoice actually switches this number.</v>

00:15:59.571 --> 00:16:01.731
<v Sean Riley>Automatically, like...</v>

00:16:01.251 --> 00:16:03.971
<v Nathan Carver>Yeah, which is, which is okay.</v>

00:16:06.931 --> 00:16:08.771
<v Nathan Carver>So, in the in the system.</v>

00:16:11.491 --> 00:16:13.651
<v Nathan Carver>Then we want to show.</v>

00:16:18.291 --> 00:16:19.251
<v Nathan Carver>When the.</v>

00:16:20.291 --> 00:16:22.291
<v Nathan Carver>In the in the ledger entry.</v>

00:16:25.251 --> 00:16:29.251
<v Nathan Carver>So this is, yeah, so if I come in here and I want to go...</v>

00:16:32.931 --> 00:16:35.491
<v Nathan Carver>to the ledger for this customer.</v>

00:16:36.611 --> 00:16:39.251
<v Nathan Carver>or the ledger for that account.</v>

00:16:41.691 --> 00:16:42.851
<v Nathan Carver>Yeah, right here, I think.</v>

00:16:51.331 --> 00:16:55.091
<v Nathan Carver>Okay, so this is what it's going to look like. So this ledger entry will be made.</v>

00:16:56.371 --> 00:16:59.011
<v Nathan Carver>after the invoice is posted.</v>

00:16:59.411 --> 00:16:59.891
<v Igor Donis>Yeah.</v>

00:17:00.171 --> 00:17:02.451
<v Nathan Carver>Which I think is fine, 'cause it's.</v>

00:17:02.371 --> 00:17:02.771
<v Igor Donis>Yeah.</v>

00:17:03.811 --> 00:17:04.131
<v Lev Rudky>Yeah.</v>

00:17:03.971 --> 00:17:25.011
<v Igor Donis>Could you please click up and find entries, please, for show, no, no, no, no, no, no, no, in this one in the menu up in find entries for show something, no, yes, for show something to.</v>

00:17:04.531 --> 00:17:05.011
<v Nathan Carver>Mhm.</v>

00:17:10.211 --> 00:17:10.291
<v Nathan Carver>The.</v>

00:17:19.571 --> 00:17:19.851
<v Nathan Carver>Perfect.</v>

00:17:25.651 --> 00:17:30.051
<v Igor Donis>To Shannon and you, Nathan.</v>

00:17:30.451 --> 00:17:30.931
<v Nathan Carver>Okay.</v>

00:17:31.731 --> 00:17:35.251
<v Igor Donis>Look, look the GL entry, please.</v>

00:17:37.491 --> 00:17:48.531
<v Igor Donis>This is according to our mapping in general entries. OK, that is right, that is OK. OK, back up.</v>

00:17:41.291 --> 00:17:41.531
<v Nathan Carver>Yes.</v>

00:17:42.691 --> 00:17:43.171
<v Nathan Carver>Mmh.</v>

00:17:47.171 --> 00:17:47.491
<v Nathan Carver>Okay.</v>

00:17:49.611 --> 00:17:49.971
<v Igor Donis>Luck.</v>

00:17:51.811 --> 00:17:54.531
<v Igor Donis>If you, if you want, check-in.</v>

00:17:54.531 --> 00:17:54.651
<v Nathan Carver>Okay.</v>

00:17:55.691 --> 00:17:57.891
<v Igor Donis>The Boston Boston sale invoices.</v>

00:17:56.531 --> 00:17:56.691
<v Nathan Carver>No.</v>

00:17:59.651 --> 00:18:18.451
<v Igor Donis>OK, that is the that is the show me the the the invoices, the structure for invoices, and I try to figure out the line GL account in the in this line.</v>

00:18:02.771 --> 00:18:02.891
<v Nathan Carver>Yes.</v>

00:18:03.931 --> 00:18:04.051
<v Nathan Carver>Yeah.</v>

00:18:11.571 --> 00:18:11.731
<v Nathan Carver>Right.</v>

00:18:15.411 --> 00:18:15.491
<v Nathan Carver>The.</v>

00:18:19.491 --> 00:18:40.051
<v Igor Donis>the fields related to the cash flow code and GBL intercompany, that is I try to explain it to you, or I understanding in G1 and G2, the related to the dimension shall be in</v>

00:18:40.371 --> 00:18:42.451
<v Igor Donis>In this file, in this field.</v>

00:18:43.811 --> 00:18:47.811
<v Igor Donis>Beside the number, amount, amount including tax.</v>

00:18:44.291 --> 00:18:44.531
<v Nathan Carver>Yeah.</v>

00:18:50.051 --> 00:19:09.011
<v Igor Donis>Beside, more, more, more right, more right. Look, I tried to explain it to you and Sean, they should be the only feel if the system requirements using the G1 cash flow code.</v>

00:19:03.211 --> 00:19:03.331
<v Nathan Carver>Yeah.</v>

00:19:06.611 --> 00:19:06.851
<v Nathan Carver>You.</v>

00:19:09.251 --> 00:19:28.211
<v Igor Donis>dimension 0107 and G2 intercompany code is 0 always, but if the business center no requirement, I don't have problem with that because your proof in your testing.</v>

00:19:22.291 --> 00:19:22.411
<v Nathan Carver>Yeah.</v>

00:19:28.371 --> 00:19:32.851
<v Igor Donis>Is no requirement to post in this this operation, no?</v>

00:19:35.571 --> 00:19:43.731
<v Sean Riley>So, Igor, you're saying those fields don't need to be completed to post the transaction? Is that what you're saying?</v>

00:19:42.451 --> 00:19:43.971
<v Igor Donis>Yeah, exactly.</v>

00:19:45.331 --> 00:20:02.291
<v Igor Donis>If requirement, I have the the the the code the code corresponds to two two fields, but but if for posting the invoices is no requirement, no problem with that.</v>

00:19:50.611 --> 00:19:50.731
<v Nathan Carver>Yeah.</v>

00:19:52.371 --> 00:19:52.611
<v Nathan Carver>Sure.</v>

00:19:54.131 --> 00:19:54.251
<v Nathan Carver>Okay.</v>

00:19:55.731 --> 00:19:55.971
<v Nathan Carver>What?</v>

00:19:58.291 --> 00:19:58.491
<v Nathan Carver>Yeah.</v>

00:20:02.891 --> 00:20:09.891
<v Sean Riley>What Igor, can I ask, what do you use the G1 code and G2 code for? What do we need those for?</v>

00:20:11.131 --> 00:20:24.371
<v Igor Donis>For a cash flow report, is only for cash flow report. Reclassify for cash flow report after the all our report is function correctly, Sean.</v>

00:20:12.291 --> 00:20:12.411
<v Nathan Carver>Yeah.</v>

00:20:20.051 --> 00:20:20.211
<v Nathan Carver>No.</v>

00:20:23.091 --> 00:20:23.331
<v Sean Riley>No.</v>

00:20:24.771 --> 00:20:36.051
<v Sean Riley>So then if you need it so that your system can pull all the transactions for a particular report, don't you need those fields filled out for every single transaction?</v>

00:20:36.531 --> 00:20:55.571
<v Igor Donis>Yeah, I need I need it for after all we configure the the right in our Business Central. After that, we try to using the best the reporting that the standard Business Central give to us.</v>

00:20:56.051 --> 00:21:04.731
<v Igor Donis>To the cash flow cash flow details that is the that is the use in this this field.</v>

00:20:59.251 --> 00:20:59.571
<v Sean Riley>Okay.</v>

00:21:01.091 --> 00:21:01.731
<v Sean Riley>So...</v>

00:21:02.531 --> 00:21:02.651
<v Nathan Carver>Yes.</v>

00:21:05.651 --> 00:21:16.291
<v Sean Riley>I see. So what is, so you're saying in the test data, only some of the data had the codes filled out in G1 and G2.</v>

00:21:10.371 --> 00:21:10.531
<v Nathan Carver>No.</v>

00:21:16.611 --> 00:21:17.011
<v Igor Donis>Yeah.</v>

00:21:17.891 --> 00:21:23.491
<v Sean Riley>And okay, so what is code G1107 mean to you? What does that mean?</v>

00:21:24.131 --> 00:21:42.291
<v Igor Donis>is only service renderers. Is it classified in our cache flow in different different codes? For example, let me show you my screen a little.</v>

00:21:39.651 --> 00:21:57.571
<v Sean Riley>screen. So, so, so code 107 is supposed to be for a cash inflow from services. That's what, okay. So then, so for all the fees that we're charging, so all these invoices, they should all have G1.</v>

00:21:48.211 --> 00:21:51.251
<v Igor Donis>Yes, exactly, exactly.</v>

00:21:58.371 --> 00:21:59.971
<v Sean Riley>Code 107 in them.</v>

00:22:00.371 --> 00:22:06.611
<v Igor Donis>Yeah, only for related well for for in in revenues only for revenues.</v>

00:22:01.571 --> 00:22:01.971
<v Sean Riley>Okay.</v>

00:22:06.691 --> 00:22:07.891
<v Sean Riley>Only for the revenues, yeah.</v>

00:22:08.051 --> 00:22:09.891
<v Igor Donis>Yes, in this case, in this case.</v>

00:22:09.491 --> 00:22:12.611
<v Nathan Carver>So, OK, so on revenue lines.</v>

00:22:10.371 --> 00:22:10.611
<v Sean Riley>Alright.</v>

00:22:13.491 --> 00:22:14.131
<v Nathan Carver>Hopefully.</v>

00:22:15.651 --> 00:22:17.411
<v Nathan Carver>Right here, we got code 106.</v>

00:22:16.691 --> 00:22:28.131
<v Igor Donis>Yeah, but yeah, but I see, I see that this, this field is no, is not open, is no, is no, you know, happen with that, nothing.</v>

00:22:21.811 --> 00:22:21.971
<v Nathan Carver>Yeah.</v>

00:22:28.651 --> 00:22:32.371
<v Sean Riley>Yeah, it looks like he can't fill it in is what I guess Igor is trying to say.</v>

00:22:32.691 --> 00:22:33.171
<v Igor Donis>Yeah.</v>

00:22:33.571 --> 00:22:33.971
<v Nathan Carver>This.</v>

00:22:34.851 --> 00:22:39.731
<v Nathan Carver>Oh yeah, well this invoice is posted, so I don't think it's going to let us change it.</v>

00:22:39.331 --> 00:22:39.891
<v Sean Riley>I see.</v>

00:22:42.091 --> 00:22:49.171
<v Sean Riley>But there should be a, there should be something that doesn't let you post it if that code's not filled in yet, like a stopper.</v>

00:22:51.571 --> 00:22:52.851
<v Lev Rudky>I Singh.</v>

00:22:54.691 --> 00:22:55.971
<v Lev Rudky>There is a setting.</v>

00:22:57.571 --> 00:22:59.651
<v Lev Rudky>That they mentioned mandatory.</v>

00:23:01.251 --> 00:23:02.331
<v Lev Rudky>Nothing like that.</v>

00:23:04.291 --> 00:23:05.171
<v Lev Rudky>Need to chip.</v>

00:23:04.531 --> 00:23:08.691
<v Sean Riley>Yeah, like is there a, I guess that's Turn Nathan. Are you able to set it up?</v>

00:23:05.811 --> 00:23:05.931
<v Nathan Carver>Okay.</v>

00:23:09.531 --> 00:23:13.491
<v Sean Riley>where you can't post the transaction unless that field is completed.</v>

00:23:10.131 --> 00:23:11.571
<v Nathan Carver>Yeah, so I can.</v>

00:23:14.211 --> 00:23:18.611
<v Nathan Carver>Yeah, we can have the system can add that.</v>

00:23:21.171 --> 00:23:23.891
<v Nathan Carver>And ensure that that that that code is there.</v>

00:23:24.611 --> 00:23:24.931
<v Sean Riley>Yeah.</v>

00:23:25.571 --> 00:23:26.091
<v Nathan Carver>And.</v>

00:23:31.411 --> 00:23:37.691
<v Sean Riley>And and Igor, what is code G2? What do you use to code G2? What's what is it?</v>

00:23:35.731 --> 00:23:35.891
<v Nathan Carver>Yeah.</v>

00:23:36.931 --> 00:23:55.891
<v Igor Donis>G2 is only related with the whenever transactions when we have something sales between the companies is for capture or identify</v>

00:23:38.451 --> 00:23:38.731
<v Nathan Carver>Okay.</v>

00:23:39.971 --> 00:23:40.131
<v Nathan Carver>Mm.</v>

00:23:56.211 --> 00:24:15.371
<v Igor Donis>A GBL labs where with GBL system or GBL game work, but in this case, it's only is only is 0, it's zero, G2 is 0 because all I understand that these operations is only.</v>

00:24:00.451 --> 00:24:01.051
<v Sean Riley>Mm-hmm.</v>

00:24:15.811 --> 00:24:21.491
<v Igor Donis>from GBL system out other customers, right?</v>

00:24:18.771 --> 00:24:18.811
<v Nathan Carver>Oh.</v>

00:24:20.851 --> 00:24:23.331
<v Sean Riley>The third parties, yeah, the third parties, yeah.</v>

00:24:22.451 --> 00:24:31.891
<v Igor Donis>The third parties, right, and in these cases, G2 is shall be go zero, zero in the companies.</v>

00:24:24.371 --> 00:24:24.691
<v Sean Riley>Right.</v>

00:24:29.811 --> 00:24:29.891
<v Nathan Carver>Oh.</v>

00:24:30.211 --> 00:24:31.371
<v Sean Riley>Yeah, I got you.</v>

00:24:32.291 --> 00:24:40.451
<v Sean Riley>Gotcha. So, yeah, Nathan, I guess, is there a way to default it so that the code always shows a zero on the G2 field?</v>

00:24:41.171 --> 00:24:42.691
<v Nathan Carver>Yep, yep.</v>

00:24:45.011 --> 00:24:46.611
<v Nathan Carver>Just, just zero.</v>

00:24:47.171 --> 00:24:47.491
<v Sean Riley>Yeah.</v>

00:24:48.611 --> 00:24:53.171
<v Nathan Carver>Okay, so G1 would have the code 107, G2 will have zero.</v>

00:24:53.411 --> 00:24:53.811
<v Sean Riley>Yeah.</v>

00:24:54.371 --> 00:24:54.611
<v Lev Rudky>No.</v>

00:24:56.451 --> 00:25:04.131
<v Nathan Carver>Will we put zero in the other fields as these S1, S2, S4, or does that matter?</v>

00:24:57.771 --> 00:24:58.211
<v Igor Donis>Hey.</v>

00:25:04.851 --> 00:25:23.811
<v Igor Donis>Yeah, I put in in the chat, Sean, I put in in the chat, Nathan, the hours, hours code corresponds to field G1 related to the revenues and related to the intercompany. In our case.</v>

00:25:14.691 --> 00:25:15.011
<v Nathan Carver>Ohh.</v>

00:25:24.131 --> 00:25:24.251
<v Nathan Carver>Yes.</v>

00:25:25.091 --> 00:25:39.651
<v Igor Donis>The code shall be 0107 service rendered. And in this case, G2 fields shall be 0, no related companies.</v>

00:25:30.171 --> 00:25:30.451
<v Sean Riley>Yeah.</v>

00:25:33.171 --> 00:25:33.291
<v Nathan Carver>Yes.</v>

00:25:36.851 --> 00:25:37.051
<v Nathan Carver>Okay.</v>

00:25:40.931 --> 00:25:44.291
<v Igor Donis>Right? Do you see my, my... Okay.</v>

00:25:41.731 --> 00:25:41.891
<v Nathan Carver>No.</v>

00:25:42.851 --> 00:25:43.331
<v Sean Riley>Yeah.</v>

00:25:43.091 --> 00:25:43.411
<v Nathan Carver>Yes.</v>

00:25:47.171 --> 00:25:48.611
<v Nathan Carver>Got it. Okay.</v>

00:26:06.171 --> 00:26:16.051
<v Igor Donis>All payment, Sean, a question. All payment hub, I understand, is the services, services rendered, yes?</v>

00:26:16.251 --> 00:26:16.491
<v Nathan Carver>Yeah.</v>

00:26:16.371 --> 00:26:17.571
<v Sean Riley>Yes, yeah.</v>

00:26:17.171 --> 00:26:18.851
<v Igor Donis>That is right, classify.</v>

00:26:19.011 --> 00:26:24.291
<v Sean Riley>We're charging a fee for the activation of the cards and so on. Yeah, it's the right code.</v>

00:26:21.131 --> 00:26:21.331
<v Igor Donis>Yeah.</v>

00:26:24.691 --> 00:26:25.091
<v Igor Donis>Yeah.</v>

00:26:38.931 --> 00:26:45.171
<v Igor Donis>Well, I don't know what other points open for Nathan.</v>

00:26:46.331 --> 00:26:47.971
<v Nathan Carver>OK, so.</v>

00:26:49.131 --> 00:26:51.091
<v Nathan Carver>When I create a customer.</v>

00:26:52.251 --> 00:26:54.291
<v Nathan Carver>a COAM customer.</v>

00:26:57.411 --> 00:27:00.851
<v Nathan Carver>I just want to make sure that I have all the correct.</v>

00:27:04.331 --> 00:27:04.451
<v Nathan Carver>Um...</v>

00:27:06.051 --> 00:27:08.051
<v Nathan Carver>I guess configurations for this customer.</v>

00:27:10.291 --> 00:27:11.411
<v Nathan Carver>So...</v>

00:27:13.331 --> 00:27:17.691
<v Nathan Carver>I guess, so the payment terms for the customers will be COD.</v>

00:27:18.491 --> 00:27:20.291
<v Nathan Carver>Obviously, they're going to be domestic.</v>

00:27:21.571 --> 00:27:21.971
<v Igor Donis>Yeah.</v>

00:27:22.051 --> 00:27:22.171
<v Nathan Carver>Um...</v>

00:27:24.371 --> 00:27:25.651
<v Nathan Carver>Is there...</v>

00:27:27.731 --> 00:27:46.211
<v Igor Donis>You can shoot, you can insert the G1 cache, take that, take them, and dimension value code, the second file, okay, C107, take another field below.</v>

00:27:28.931 --> 00:27:29.051
<v Nathan Carver>Right.</v>

00:27:30.091 --> 00:27:30.211
<v Nathan Carver>Yeah.</v>

00:27:36.611 --> 00:27:36.771
<v Nathan Carver>Yeah.</v>

00:27:40.211 --> 00:27:40.331
<v Nathan Carver>Yes.</v>

00:27:41.371 --> 00:27:41.491
<v Nathan Carver>Bing.</v>

00:27:43.331 --> 00:27:43.691
<v Nathan Carver>Okay.</v>

00:27:47.011 --> 00:28:03.411
<v Igor Donis>That you want, if you want, if you want, but I think we don't need it the second one, only the G1, because all this operation is a company with third party.</v>

00:28:02.691 --> 00:28:02.811
<v Nathan Carver>Okay.</v>

00:28:04.531 --> 00:28:11.571
<v Nathan Carver>Okay, perfect. Okay, so I will configure the customers with this G1 code 0107.</v>

00:28:11.731 --> 00:28:12.131
<v Igor Donis>Yeah.</v>

00:28:13.811 --> 00:28:15.251
<v Nathan Carver>And then.</v>

00:28:16.491 --> 00:28:19.411
<v Nathan Carver>I think they get, I thought there was.</v>

00:28:21.091 --> 00:28:23.891
<v Nathan Carver>I thought there was tax information on.</v>

00:28:27.331 --> 00:28:28.931
<v Nathan Carver>On the customer.</v>

00:28:31.011 --> 00:28:33.091
<v Igor Donis>In taxes, in invoices.</v>

00:28:34.051 --> 00:28:35.251
<v Igor Donis>That's how you call.</v>

00:28:35.171 --> 00:28:38.291
<v Sean Riley>Oh yeah, tax code has got the star beside it, yeah, right there.</v>

00:28:37.731 --> 00:28:38.371
<v Nathan Carver>All right, yeah.</v>

00:28:37.731 --> 00:28:43.091
<v Igor Donis>Maybe select, no, no, nothing there on, or I don't know, Lev while it.</v>

00:28:39.811 --> 00:28:39.931
<v Nathan Carver>Yes.</v>

00:28:42.411 --> 00:28:46.531
<v Sean Riley>Yeah, give it, yeah, non-toxable exempts, probably.</v>

00:28:45.491 --> 00:28:47.731
<v Igor Donis>What example?</v>

00:28:48.211 --> 00:28:49.571
<v Sean Riley>Yeah, exams.</v>

00:28:48.931 --> 00:28:49.731
<v Igor Donis>The last one.</v>

00:28:59.011 --> 00:29:02.531
<v Nathan Carver>Okay, so for these COAM customers, they'll be exempt.</v>

00:29:03.971 --> 00:29:04.371
<v Sean Riley>Yeah.</v>

00:29:10.451 --> 00:29:10.851
<v Nathan Carver>Okay.</v>

00:29:15.171 --> 00:29:16.131
<v Nathan Carver>Okay, I think.</v>

00:29:15.491 --> 00:29:18.611
<v Igor Donis>I think, I think that the should be all.</v>

00:29:19.411 --> 00:29:36.931
<v Igor Donis>all our customers involved in Payment Hub with this configuration. I think this is your goal. No, Nathan, is your goal exactly. Okay.</v>

00:29:25.091 --> 00:29:25.131
<v Nathan Carver>I.</v>

00:29:27.651 --> 00:29:27.971
<v Nathan Carver>Okay.</v>

00:29:32.651 --> 00:29:32.811
<v Nathan Carver>Uh-huh.</v>

00:29:36.611 --> 00:29:37.811
<v Nathan Carver>Correct. Yep.</v>

00:29:39.731 --> 00:29:41.731
<v Nathan Carver>Okay, so...</v>

00:29:40.131 --> 00:29:40.451
<v Igor Donis>So.</v>

00:29:46.131 --> 00:29:47.731
<v Nathan Carver>The Journal.</v>

00:29:53.011 --> 00:29:53.811
<v Nathan Carver>Is it?</v>

00:29:57.651 --> 00:29:59.811
<v Nathan Carver>I've never shown my journals.</v>

00:30:02.531 --> 00:30:03.571
<v Nathan Carver>No, that's not it.</v>

00:30:06.691 --> 00:30:13.171
<v Nathan Carver>So I have the payment hub journal entry. Let me find that in the configuration.</v>

00:30:32.531 --> 00:30:35.851
<v Nathan Carver>Okay, is it called Customer Payment URL?</v>

00:30:37.171 --> 00:30:39.251
<v Nathan Carver>Is it a payment journal? The sound was calling.</v>

00:30:42.651 --> 00:30:44.851
<v Sean Riley>Alright, Inna, what are you what are you trying to find here?</v>

00:30:45.771 --> 00:30:51.411
<v Nathan Carver>I'm trying to remember the name of the journal. I mean, it's like Customer Payment Journal.</v>

00:30:51.491 --> 00:30:53.011
<v Sean Riley>Customer receipts, probably.</v>

00:30:55.011 --> 00:30:56.291
<v Nathan Carver>Customer receipts.</v>

00:30:57.211 --> 00:30:57.651
<v Sean Riley>Yeah.</v>

00:30:58.611 --> 00:31:00.131
<v Lev Rudky>It's, I think it's...</v>

00:31:01.291 --> 00:31:02.291
<v Lev Rudky>Cash receipts.</v>

00:31:02.531 --> 00:31:03.651
<v Sean Riley>Cash receipts, yeah.</v>

00:31:10.051 --> 00:31:11.731
<v Sean Riley>Yeah, cache for this journal, there you go.</v>

00:31:10.211 --> 00:31:10.611
<v Nathan Carver>Yeah.</v>

00:31:18.371 --> 00:31:20.771
<v Nathan Carver>Now, is this for all of them, or is this...</v>

00:31:22.131 --> 00:31:22.611
<v Nathan Carver>Okay.</v>

00:31:23.251 --> 00:31:29.331
<v Sean Riley>Cash receipts journal should show every single payment received from all your customers.</v>

00:31:30.531 --> 00:31:31.011
<v Nathan Carver>Okay.</v>

00:31:40.131 --> 00:31:47.011
<v Nathan Carver>Okay, so currently what the code is looking for is the customer payment journal is named payment hub.</v>

00:31:50.731 --> 00:31:50.931
<v Nathan Carver>Um...</v>

00:31:53.731 --> 00:31:54.331
<v Nathan Carver>Find.</v>

00:31:56.371 --> 00:31:59.491
<v Sean Riley>Right, so this would list every single payment we got from Payment Hub.</v>

00:31:57.891 --> 00:31:58.051
<v Nathan Carver>No.</v>

00:32:00.331 --> 00:32:02.451
<v Sean Riley>Because Payment Hub was set up as a customer.</v>

00:32:00.771 --> 00:32:01.171
<v Nathan Carver>Right.</v>

00:32:07.971 --> 00:32:13.811
<v Nathan Carver>Oh, correct, right here. There it is. I don't know why I didn't see it. Yeah, so these are the batch names, right?</v>

00:32:09.491 --> 00:32:09.611
<v Sean Riley>Yeah.</v>

00:32:14.451 --> 00:32:17.811
<v Igor Donis>Yes, this is this is the standard payment hub, no?</v>

00:32:18.371 --> 00:32:18.611
<v Sean Riley>Yeah.</v>

00:32:18.691 --> 00:32:19.451
<v Nathan Carver>Yeah, okay.</v>

00:32:21.171 --> 00:32:25.811
<v Igor Donis>Yeah, he's right. This bank is called bank is Cris right, yes.</v>

00:32:23.411 --> 00:32:24.611
<v Nathan Carver>Journal.</v>

00:32:25.411 --> 00:32:25.891
<v Nathan Carver>Okay.</v>

00:32:27.051 --> 00:32:27.571
<v Nathan Carver>Perfect.</v>

00:32:29.251 --> 00:32:31.251
<v Nathan Carver>Okay, I think that was it. I think those...</v>

00:32:32.131 --> 00:32:34.211
<v Nathan Carver>To verify that, and then...</v>

00:32:36.851 --> 00:32:40.211
<v Nathan Carver>The GL account codes are good. So what I'll do.</v>

00:32:41.451 --> 00:32:42.611
<v Nathan Carver>Is that will create?</v>

00:32:44.131 --> 00:32:44.651
<v Nathan Carver>And.</v>

00:32:45.931 --> 00:32:50.051
<v Nathan Carver>example data of everything we just talked about, so you can review it inside.</v>

00:32:51.571 --> 00:32:54.611
<v Nathan Carver>The staging environment, and...</v>

00:32:56.131 --> 00:33:00.531
<v Nathan Carver>Give a thumbs up, thumbs down on that. We're getting the correct configurations in there.</v>

00:33:02.771 --> 00:33:03.331
<v Sean Riley>Okay.</v>

00:33:03.291 --> 00:33:08.291
<v Nathan Carver>So, I'll have the system generate a full cycle, so the invoice.</v>

00:33:03.651 --> 00:33:04.211
<v Igor Donis>Okay.</v>

00:33:08.931 --> 00:33:09.331
<v Igor Donis>Yeah.</v>

00:33:10.531 --> 00:33:14.051
<v Nathan Carver>And then post it, and then we can make sure all everything is correct.</v>

00:33:15.091 --> 00:33:15.571
<v Igor Donis>Okay.</v>

00:33:17.411 --> 00:33:17.811
<v Nathan Carver>So.</v>

00:33:19.571 --> 00:33:19.611
<v Nathan Carver>I.</v>

00:33:21.491 --> 00:33:23.411
<v Nathan Carver>That's it. I think that's all I need for now.</v>

00:33:24.211 --> 00:33:24.771
<v Sean Riley>Okay.</v>

00:33:25.331 --> 00:33:29.171
<v Lev Rudky>OK. Thank you.</v>

00:33:25.411 --> 00:33:27.331
<v Igor Donis>OKOK, Nathan. Thank you.</v>

00:33:27.811 --> 00:33:29.651
<v Nathan Carver>All right. Thank you, everyone.</v>

00:33:29.891 --> 00:33:31.411
<v Sean Riley>Thanks, guys. Have a good day.</v>

00:33:30.851 --> 00:33:32.491
<v Igor Donis>Thank you, Sean. Thank you, Lev.</v>

00:33:33.371 --> 00:33:33.891
<v Igor Donis>Bye-bye.</v>

00:33:34.371 --> 00:33:34.931
<v Sean Riley>Oh, bye-bye.</v>

00:33:34.531 --> 00:33:34.691
<v Nathan Carver>No.</v>
