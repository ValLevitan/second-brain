# Raw Transcript — CIBC (Sanjay, Michael Hill) — ACH receiving-account architecture
**Date:** July 2, 2026, 11:07 AM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_CIBC_ACH_Account_Architecture-July-2-2026]]
---
00:00:00 Speaker 1
Account, Whereas this initial receiving account is going to sit at zero, and it's going to be shared or it's going to be pushed out to another account.
00:00:13 Val Levitan
Everything is correct, but you lost me on the very last part.
00:00:19 Speaker 1
So, the funds so when the funds come in, The account that the funds are received in that account is always going to stay at zero. Yes. So, when those funds come in, you want those funds pushed out of that account into another CIBC account?
00:00:34 Val Levitan
Yes, but not before we took a reading electronic reading of that account.
00:00:44 Speaker 1
Okay, so what does that reading look like?
00:00:50 Val Levitan
It's an API call: How much money do I have on this account now? There is a reply to us. We say, okay, one hundred and five dollars in this account now. Transfer this money to this CIBC account. That's it. Now from that CIBC account we want to see, okay, one hundred and five dollars moved from here to here. Great. This account is at zero.
00:01:25 Speaker 1
So that, That API call, I'm not familiar with that term. I'll have to talk to someone else to see if I can get it. But you.
00:01:33 Val Levitan
Call it something else. You call it, you have this platform that you electronic platform forgot the name. You mentioned it last time.
00:01:51 Speaker 3
Business banking. What do you mean that?
00:01:55 Speaker 1
Are you just talking about like the, um. Like the bank transactions, like you want to see the transaction in the account, and then once you see the transaction in the account. So this how it I'm I'm thinking now and just. Let me make sure you just let me know if this anything different. So when the funds come into the account. Um from your third party it will go into this zero balance account. That zero balance account is going to record that deposit occurring in that account. It's also going to record the subtraction of that from out of that account and it being added into another account. Is that what you're looking for?
00:02:41 Val Levitan
Yes, And the reason I'm looking for two accounts, because one account must always be zero.
00:02:47 Speaker 1
Yeah, yeah, yeah.
00:02:50 Val Levitan
And the second account is accumulation account. We, that's a transactional account already. We we can use those funds afterwards. What, we don't what we don't want to do is to intermingle the funds, and we want to record it hundred five dollars received, date stamp and then hundred and five dollars moved on this account becomes zero. We're waiting for new money. New money is two hundred dollars, came in okay record date. Stamp move two hundred dollars that account becomes.
00:03:23 Val Levitan
Three hundred and five dollars. And this account sits at zero. Two days later, there is another transaction of four hundred dollars. Four hundred dollars came in, Date stamp now two hundred and five plus four hundred dollars is six oh, five in the cumulative account. The first account is still zero. And we catching we're catching electronic date stamp and the amount. Okay.
00:03:52 Speaker 1
Perfect, so a couple of things have to happen now. I am going to have to look at your. So, do we already have the second account open? Okay, so we need to open up the second account. Okay, The other part of it val is we didn't open you all up with analysis accounts. ;, you all have our small business accounts or our business banking accounts. So, we'll have to convert your account type. So that we can set up this initial funding account to be a zero balance account, and it'll have that automatic transfer into this new account. So we can we can do that all of that can happen. I just want you to know that that's going to change your fee structure. And you know what now I think I think we talked about this initially. I think were look, were going down this path initially, but were waiting until you guys got everything all fleshed out. Okay, alright. So so I don't have to re explain it. But so now we're at this.
00:04:48 Speaker 1
Point now about, well, we'll make those changes so that we can have this initial funding account as a zero balance account. And then we'll have the second account, which will be your operating account. Or however, you're going to use the funds for it.
00:05:03 Val Levitan
I just want to uh verify that it's not just uh an erroneous expression, but so I I want to be very exact in what I'm saying. So there is no automated transfer, From one account to the next. We don't want that. We want force transfer. So, we need to communicate electronically with each account, and we need to trigger that transfer based on a command.
00:05:34 Speaker 1
So okay, so that's a little bit different. So we don't have, and I'll check with the other team to confirm, but the way that our our zero balance account works now is.
00:05:47 Speaker 1
It's ten thirteen in the morning here, in where we're located. Okay, a balance of one hundred and five dollars gets deposited into your account, into this funding account. At the end of the day, that hundred and five dollars is going to be reported. And it's going to be moved out of that account into another account automatically. So you won't have any intervention in it. You won't be able to say that if you want to, Have it so that this account stays at zero, but it only stays at zero, at your command. Then, you will have to manually go in and complete a transfer from this funding account into your other account.
00:06:36 Val Levitan
I expect frequent transfers into account. I mean, I cannot manually do it. That's going to be a tremendous, Overhead expense,
00:06:47 Speaker 1
Yeah. So, So the only other option, like we don't have it where you communicate to us transfer, and it's done automatically. We either have two options where you would manually go in and do it, or it's going to be automatically done at the end of the day. So if this funding account receives seven batch transactions on today Thursday. At the end of the day, Thursday, Those seven are going to move out of that account, and they're going to go into the other funding account.
00:07:22 Speaker 3
Can I have a question? The question is: So. Let us say that the account that is going to be zero receives all these batches at different points in time. Is Val able to see those at different points in time? He will. So, if there is, for example, at ten fifteen one hundred and five dollars coming, and then Val doesn't have to do anything. But. If there is some discrepancy, how do you how does VAWL stop that? If, there is a discrepancy in terms of what he was expecting and what came through, Vawl.
00:07:53 Speaker 1
Would have to file that discrepancy with the third party. And ultimately, the third party would have to go or VAWL would have to go to whomever the initial sender was of those payments. So with the zero balance account, those funds come into the account they are recorded and once, The end of the day occurs; those funds move out of that account. And then they go into whatever account is designated to receive those funds. There's no intervention by anyone, but Val would be able to see: one hundred and five dollars came in, two hundred and five dollars came in, three hundred dollars came in. He'll be able to see that he'll also see that one hundred and five dollars was moved out, two hundred and five was moved out, three hundred and five was moved out.
00:08:38 Speaker 3
Right? But I think Val what I want to ask from you is you said, You have to approve it or that API call. Why is that required? Are you checking the transaction? What is the reason for you to get a reply in terms of the one hundred and five that came in?
00:08:58 Val Levitan
Well, it's a good question. This was a mental architecture we had in our minds. We did not assume that there was a limitation or there was an issue.
00:09:12 Val Levitan
Doing that at the bank level, I don't know whether we can change this architecture and why this architecture was created in the first place.
00:09:28 Speaker 3
But I am just thinking out aloud:, whether you check the account online and contrast that with what is expected to come in. Or, you know, if you had an API call, The effort is the same because you have to keep on getting these calls coming to you. And then you're approving it. It means the same to me. So, the question I have for you is: when these payments come, How often do you see them? And how much do you expect in a day? Because if it's like five hundred of them coming in a day, that's like crazy. There's no way. You know. No system can recreate.
00:10:04 Val Levitan
No no no no uh of course not, All of the amalgamation takes place with.
00:10:17 Speaker 3
The other end,
00:10:19 Val Levitan
And there we have a detailed report. You know, It could be twenty dollars plus forty dollars plus sixty dollars plus five dollars plus ten dollars, and it could be I don't know one hundred two hundred you know. And it will grow the more. The more accounts we open up, the more it will grow. And the amalgamator on the other side will have many, many transactions. But it's okay; we can manage it on the other side. What, we want is an absolute purity between transferring that whatever that amount is and receiving exactly the same amount.
00:11:04 Val Levitan
And I understand your question, but you could see it not even in the zero account. You could see it in any account. You could see that one hundred and five dollars came in at eleven o'clock, and then you could see another two hundred dollars came in at one o'clock, and another four hundred dollars came in at four o'clock. I understand what you are saying. I don't have the answer to this.
00:11:30 Speaker 3
Yeah, no, I appreciate that, but in my mind, And I presume this is done by your accounting team. That's why you wanted the accountants to be, you know, on the be able to access it. So as far as they're concerned, They're seeing all these credits into your account, and they also have the invoices coming in from the other intermediary, which is collecting this. So for me, it becomes very simple between beginning of the day and the end of the day. Because the transfers only happen at the end of the day. Between that.
00:12:01 Speaker 3
All the transactions are visible to them and they're able to compare that. The only time there's a discrepancy, like Michael said, you have to go back to the aggregator, the company which is aggregating that and say, "Hey, you reported this but what has actually come in is that." Therefore there's a discrepancy and you have to solve it. To me, that seems far more simpler because all you're doing is validating. What has come in from the aggregator in terms of the collective amount. Looking at the bank account and say, "Hey, yeah, it matches. That's fine. That's all." And if there is a discrepancy, then you report to them saying, "You reported this, but what I got was that." That's it. Because it only happens by the end of the day. So maybe this is not what you want, But in a simple way, in my mind seems logical because you are able to see that and validate that and go back to the aggregator and say, hey, You, send this ;. We received this fine."
00:13:01 Speaker 3
And is this in JVL? Yes. Okay, So I presume you want to create the, not the zero balance, but the other account you want that to be in a money market account because it has to generate some money. In terms of the back cash back,
00:13:18 Val Levitan
No, no, that's an operational account.
00:13:20 Speaker 3
So oh so just checking account again.
00:13:23 Val Levitan
Uh yeah check. But but again, how do we operate the accounts? Can we operate it? We give instructions electronically. Let's say we need to transfer money in and out.
00:13:36 Speaker 3
You can do it online, it's straightforward.
00:13:38 Val Levitan
Not online, can we do it with with a tool?
00:13:43 Speaker 1
If if if it's integrated into it, yes. So if you're let's say QuickBooks, Like if you're using QuickBooks to be able to, yes, you can, you can do that.
00:13:53 Val Levitan
Okay so how does this integration take place? For example QuickBooks is what? You have it directly integrated.
00:14:01 Speaker 1
Yeah, So it's remember a couple months ago, Monica and I were working together for that service to be cut on and to be integrated. You would just do it through that through thatum through that API. What would happen isum if you wanted additional features to be available, then you would have to because I don't know what your QuickBooks is like, I don't know what you have available to you to be able to do that. So you just want to make sure that, That is something that's been turned on for you via your QuickBooks or whatever the, um. ERP system is that you're using.
00:14:37 Val Levitan
But why are you using in particular the QuickBooks? Is it because QuickBooks?
00:14:46 Speaker 1
No, I just use that because that's usually the simplest form of an ERP piece system that people know.
00:14:52 Val Levitan
So we use Microsoft Business Central. Okay. And and I don't know whether you have native integration with Microsoft Business Central or not. I I don't know. But if you don't, then do you have an API that has that capability?
00:15:13 Speaker 1
You said it's called Microsoft?
00:15:15 Val Levitan
Business Central. Thank you, Johnson. I can look up the exact name. Give me just a few seconds.
00:16:21 Speaker 1
You said Microsoft Business Central? Yes. Yes, we do have access to that.
00:16:29 Val Levitan
What does it mean? We have access to it.
00:16:31 Speaker 1
So, we have clients that are using Microsoft Business Central to integrate into the banking system.
00:16:40 Val Levitan
So is it a native integration? This is something that you have on your end because this is what I would expect. Yes.
00:16:51 Speaker 1
So what it means is the two will they can talk together. So our online banking system can talk to the Microsoft Business Central. We just need to turn it on so that they do talk to one another.
00:17:05 Val Levitan
So, what is the process of that?
00:17:08 Speaker 1
That's what Monica and I were going through earlier this month. So she has to, and I don't know if she's completed it or not, but she would have to, Turn that on, and then she would work through Microsoft Business Central to establish the connection.
00:17:30 Val Levitan
I don't want to contradict what you are saying, but it doesn't look right.
00:17:38 Speaker 1
So, on the online banking, there is an open access process. So that was the API that we were talking about. So, once that.
00:17:50 Val Levitan
Sorry, sorry for interruption. I apologize, Michael. I just want to catch my own thought. So, on your site, on your portal, There is already a provision for us going into it and turning on a switch that gives us an ability to talk to your. Side through Microsoft Business Central. Yes. Is this what you're saying? Yes. Uhhuh. So Monica will not be able to do it, we need a technical person on that.
00:18:33 Speaker 1
I would talk to Monica first, So I would talk to Monica first to see if she's turned it on. And then we would be able to go from there, so if she hasn't then I would say then yeah, Yes, you would need to bring someone in to kind of work through that. But I sent Monica directions and everything like that to be able to do that.
00:18:52 Val Levitan
Okay, gotcha. Uh- huh. Okay, so that to me is urgent. So how do I accelerate this? I speak to Monica; she already knows what to do.
00:19:07 Speaker 1
Yes, so it's just confirm with.
00:19:09 Val Levitan
Do I organize another call between Monica, you and. My tech guy.
00:19:16 Speaker 1
I don't know about your tech guy yet, But let's let's just check with Monica and see if she has turned that on and she's actioned that. And she may have already initiated this. And if she's already initiated it, then we don't have to do anything else.
00:19:31 Val Levitan
Understood. And I and can I use my currently opened account for yes for a receipt of ACH?
00:19:44 Val Levitan
And I can use the same account to access to Microsoft Central. Yes. Okay, got it. So that's what I need. Let's start there.
00:19:56 Speaker 3
So so, wait, Sanjay, And just say, I will set up the other account. So Monday morning is when you will get the account paperwork to sign for the second account under JVL.
00:20:10 Val Levitan
Don't don't do it yet. Let me let me work with this. No, let me work with this account. I'm going to go with your uh suggestion, Michael, And your suggestion uh trying to work through one account because if it's integrated with Microsoft Central, Then indeed, there should be no reason why it cannot simply reconcile what's received and the what and and the dates uh and the timestamp. Uh It sounds logical. So maybe there was an error in our architectural thinking.
00:20:43 Val Levitan
Let me let me do that first. Okay, so my undertaking, My action is to uh work with Monica, and my my tech in enabling that account setting. When that account is enabled, and if there is any technical uh back and forth, Then I assume my technical guy could speak to somebody on your side who's equally technical, and they could probably find an alignment.
00:21:13 Speaker 1
Yeah, So so normally the the normally there isn't anything that we would do on our end. It's normally driven by whatever the requirements are for Microsoft Dynamics. Is it Microsoft Business? Yeah, so that's usually like Microsoft Business Central. I am sorry, like usually that's where most of the work has to occur at.
00:21:35 Val Levitan
It's Microsoft Dynamics you are also involved with.
00:21:41 Speaker 4
Okay, now I understand completely.
00:21:43 Val Levitan
Okay, I'll be working with Monica. Uh, yeah, please expect another call. And Michael, how what's I don't want to bother Sanjay. How do I get a hold of you or do I get a hold of through Sanjay? How do you want me to act?
00:21:59 Speaker 1
You go through Sanjay. Yeah.
00:22:01 Val Levitan
Okay, perfect. Okay, thank you very much. That's it for me.
00:22:05 Speaker 1
Okay, thanks well okay Thank you Bye bye Bye.
