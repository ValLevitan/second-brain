# Raw Transcript — JVL Systems / Bank of America treasury review (Brooks Darnell, Lenin Hernandez; Nathan Carver, Felipe) — ACH + Microsoft Dynamics 365 Business Central reconciliation
**Date:** August 27, 2026, ~12:28 PM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_BofA_Treasury_MS_Dynamics_Integration-August-27-2026]]
---
00:03:01 Speaker 1
Good afternoon.
00:03:03 Val Levitan
Hey, good afternoon, is it just going to be the two of you today? Yes, and the two of us is plenty more than you can handle. We are aggressive.
00:03:15 Speaker 1
Just going to go into here and make sure for the morning. Well, we do have Linnet Hernandez on the line as well; that's your relationship manager. I know he speaks with Kino a lot, but he is on the line as well.
00:03:29 Felipe Miranda
Hello there, Mr. Bob. Good to speak to you again. I know we met them once at Ventura. Yes,
00:03:35 Val Levitan
Yes, Mister Vladimir, I remember you.
00:03:45 Val Levitan
How Can I ever forget your name?
00:03:54 Val Levitan
Thank You for arranging the call and, Darryl, pleasure meeting you. And we look forward to moving forward with this program.
00:04:26 Speaker 1
Be honest, We have a specialist or a vendor I partner with who would take more of a deep dive into this. So today, What I'm trying to do is just really find out all the needs that you would have because we have to look at some stuff. And then from that point, If it is going to be like an API or integration between your accounting software, and we need to get a specialist involved just to go over the details, just so we're not missing anything. All.
00:06:05 Val Levitan
Brooks, Before we get into technicality, I would like to apologize for mispronouncing your name. I read it as Darryl, But now I see Darnell is your last name, and Brooks is your first name. Please accept my apologies. No offense.
00:06:19 Speaker 1
Apology accepted. You probably won't believe this pal, but that happens to me every day. But.
00:06:27 Val Levitan
Yeah, I I'm sometimes I'm dyslexic as well. And so yeah, maybe it's my age already. But uh yeah, thank you for your understanding. Uh Nathan is an engineer on this initiative. Uh and a specialist and I'm going to uh take a backstage to this meeting unless I'm needed because I think that uh, it's more of a technical approach.
00:07:18 Val Levitan
Yeah, Let me let me contribute to this. Nathan is working on a particular project where we are clearing multiple transactions through a third party ACH provider. That particular ACH provider sweeps multiple accounts, brings it into his account, then transfers into, Our account, right now we deal with a small bank in the US in Chicago. It's a large Canadian bank but has a small presence in Chicago, And they just don't have enough capacity, no capacity, but technology I should say to facilitate everything. So this is one thing, And let me reiterate, it is a multiple ACH transaction that has moved through a third party provider onto our account.
00:08:16 Val Levitan
Lends in our account, and from there it needs to reconcile with Microsoft three sixty five, Microsoft Dynamics. However, we are tying ourselves more and more with Bank of America. And we would like to expand our queries to other accounts. And interface it directly with.
00:08:47 Val Levitan
Microsoft Dynamics three sixty five Business Central.
00:08:55 Speaker 1
Okay, so you have so you're using Microsoft Dynamics three sixty five right now. That's uh, that's what you're using. And you're looking to you're looking to have the payments read through and come into your bank statement.
00:09:11 Val Levitan
Yes, and hopefully reconcile our, Invoicing with ACH because many of our customers pay through ACH directly to us. So, if we have invoice in Microsoft Dynamics, we have receipt in the bank. We'd like to reconcile it with invoice.
00:09:35 Speaker 1
Okay, are you do you have the ability to send.
00:09:48 Val Levitan
Um, I don't know.
00:09:52 Speaker 5
So yeah, Weum we want to build out invoicing, and the approach is going to be through Business Central. Um, However, if there's other options through Bank of America, that's you know I'm just giving you.
00:10:09 Speaker 1
How much, how many like volume wise? How many invoices would you send out in a month? Twenty.
00:10:22 Speaker 1
Yes, twenty. Okay. Um, okay. Not sure if we because we have. That, would we wouldn't qualify for the full AP? I mean, that's going to be that's minimal requirements is two hundred invoices per month.
00:10:41 Val Levitan
Yeah, I figured I figured.
00:10:43 Speaker 1
Yeah but I mean I think we can still assist with this I. Think with what we're looking for I think I will need to get.
00:11:01 Speaker 1
How it integrates with the CastPro platform. So, I think what we'll need to do is probably schedule something. So, It sounds like one of the main things we're trying to do here with your business is be able to.
00:11:33 Speaker 1
Initiatives for Microsoft Dynamics, are we trying to have that work?
00:11:42 Val Levitan
To Answer your question, Brooks, yes. But, we did not dare to ask for it because we felt that it would complicate issues. But since you're on this subject, this would probably be stage two for us is vendor relationship. So our payments outgoing payments to our vendors that would definitely be extremely useful to us.
00:12:09 Speaker 1
How are you paying right now? How are you making payments.
00:12:14 Val Levitan
We are going into Bank of America, one vendor at a time, setting up wire transfers.
00:12:22 Speaker 1
How many wires are you doing.
00:12:25 Val Levitan
Probably uh Well.
00:12:34 Val Levitan
I'm I'm I'm going to say that we're probably at a range of, thirty per month, twenty to thirty per month. Mostly International. China.
00:13:02 Val Levitan
A lot of payments to China, some to the US, very few to Canada.
00:13:09 Speaker 1
And when you're when looking at sending ACHs, do you also send ACHs? Or, are we looking to do? Or are we looking to send batch files instead of it sounds like you're sending everything manually.
00:13:22 Val Levitan
Well, we're sending everything manually because we don't have any other solution. Uh okay. But uh.
00:13:34 Val Levitan
I don't know. Not too many.
00:13:38 Speaker 1
Okay, mainly right now, mainly we're sending wires. Are you running into any challenges with limits, like where you have to go into a financial center to send a wire because you've hit a limit? No. Okay, what's the total dollar?
00:14:00 Val Levitan
Well, our business is rapidly growing, so we we're see. I mean that's easy to calculate. We're, we're probably uh very, very quickly get to uh and we're transferring our company from Canada to the U S. We're closing Canadian accounts, We're moving to the U S accounts because we use Royal Bank of Canada as well. Uh, So the Royal Bank of Canada transactions will hit a sunset, and Bank of America accounts will increase to probably. Ten million per year. So, it will be uh ten million in revenue and approximately seven million in payments. So that means roughly seven hundred thousand per month in payments.
00:14:54 Val Levitan
Six hundred thousand in payments and roughly, I don't know, seven hundred fifty thousand in receivables.
00:15:09 Val Levitan
Probably Split probably split in twenty transactions.
00:15:14 Speaker 1
What is uh just a current limit they have for wires? Do you know offhand on what they're using now?
00:15:23 Felipe Miranda
Well, usually the limit.
00:15:29 Speaker 1
Thirty days okay.
00:15:30 Speaker 5
The road in thirty days, that's correct.
00:15:32 Speaker 1
Okay, and then it's typically for international wires what what is the cost? Forty dollars a wire?
00:15:38 Speaker 5
Yeah, it's usually forty five dollars for uh for international wire.
00:15:48 Val Levitan
I I detect I detect potential savings.
00:15:53 Speaker 1
Uh yeah.
00:16:35 Val Levitan
Uh, probably two hundred fifty thousand.
00:16:40 Speaker 1
Okay, and I'll address that in just a second. I'll kind of go over how the pricing works and all that. I just want to make sure I am understanding all the things. So, I think the wider capability. I think that's going to be more efficient on the CapPro platform. I know you are not hitting limits, but if for one month you ever hit it.
00:17:33 Val Levitan
And And Bruce, just to highlight on this item, this is the main point of frustration for us.
00:17:45 Val Levitan
Well, No multiple approvals, multiple privileges. We're not able we're not able to set up, but the company within the company. We have various access, privileges and. In the bank, we don't have it, so it becomes a very complicated matter. And you know, One senior person is involved in setting up wires and moving money around because of not having the proper access control.
00:18:44 Speaker 1
Right.
00:19:33 Speaker 1
No. Well,
00:19:39 Val Levitan
Cash for sure not for the longest time already, but checks we do. Yeah, yeah we do.
00:19:57 Val Levitan
No, No, because of the access control we have to uh take it to the bank.
00:20:05 Val Levitan
Which is obviously a hassle and expensive thing for us.
00:20:11 Speaker 1
Understood. Um, I'll stop there just for a moment. Do Nathan or Valda, either one of you have any questions on anything we've covered so far?
00:20:25 Speaker 5
Uh, no questions.
00:20:54 Speaker 1
Yeah, exactly. That's where when I bring Connie in, she's our specialist on that. The integration between the two platforms and the sandbox. So I think that call is going to be more beneficial on what you are looking for, and she'll be able to answer questions back. She's the one to kind of really take a deep dive on it and make sure that we understand.
00:22:37 Speaker 1
It would be used.
00:23:09 Val Levitan
Yeah, it's roughly based on your calculations. It's about one hundred sixty five dollars a month.
00:23:20 Val Levitan
So The more the more balance we hold, the potentially we could offset the entire thing.
00:24:03 Speaker 1
The only time you pay that four twenty five is if you have zero dollars in the account. So last year, uh, the rate was higher but it has dropped. Um, you know with the Fed. So just to give you an example.
00:24:40 Speaker 1
Okay. Does that make sense? Yeah. I know how the earnings credit works. It also did a pricing proposal that just shows you everything that's included. Um, also, I'll base it off of two hundred thousand. This this isn't saying this what you'll you have to have in the account. What I'm sending you is just a reference to just kind of give you an idea of how it works. I understand. Perfect, uh, did we.
00:25:09 Speaker 1
Not for me. Okay, what I'd like to do, and if we can't do it now, Connie is.
00:25:44 Speaker 1
We need to change if we can,
00:25:45 Val Levitan
But yeah, of course. Of course, go ahead.
00:27:30 Speaker 1
We go into the next week. She has a twelve thirty spot on Tuesday the eighth. That's at twelve thirty, just like we might could get an hour spot there. I don't know that we need that much time, but twelve.
00:27:49 Val Levitan
Thirty or so. Nathan, it's really you so.
00:27:54 Speaker 5
Tuesday the eighth.
00:28:09 Speaker 1
I'll Go ahead and I'll send it out to you. I'll just send it to all of you, Val. If you want to join, you can.
00:28:19 Val Levitan
Yeah, thank you. And well, it's a technical meeting, right? Yeah.
00:28:43 Val Levitan
Yeah, So put me put me as optional.
00:28:46 Speaker 1
Okay. And then what I'll do Nathan, I'll send this out to you. I just got it shows are open. I just got to confirm she is truly available for this, which typically she is because her calendar is typically up to date. So I'll put that in and then once I have it, uh approved with her, I'll just send that Teams meeting over just like I did. Okay. And, without all the problems with the phone call. Here we go again with the phone call. Here we go again with the phone call. Here we go again with the phone call. Here we go again.
00:29:40 Val Levitan
Yes, Thank you. Thank you, Brooks.
00:29:43 Speaker 1
All right, perfect. Well, I do appreciate your time today. If anything any questions come up after this, Feel free to reach out to me Joel Linnett and look forward to working with you guys going forward.
00:29:57 Abiguele
Thank you very much for your time. Thank you all right appreciate it thank you.
00:34:34 Abiguele
Hello. Yes, it is.
00:34:44 Val Levitan
I'm doing well, thank you very much. Not at all, I would like to hear from you.
00:35:08 Val Levitan
You know what, I didn't get the medication, but I'm taking Pravasac because I. Yeah, I thought it was the same thing and I, uh kind of had it at home. And so yeah. But uh, i mean i don't like taking Pravasac long term. Uh speaking about how i feel, I mean, my heartburn has gone because of Pravasac. But uh, it's not a long-term solution.
00:35:40 Abiguele
No, no, I no, I stopped taking that.
00:36:31 Val Levitan
Okay. Okay, fair fair suggestion. I like it, smart.
00:36:52 Val Levitan
Okay. Okay, But I will diarize myself to be in your hands again in about three years. I'll be six, Sixty-five years of young, and I'll be happy to see you. Thank you very much for the call.
00:43:49 Abiguele
How's it going, Felicia?
00:43:55 Val Levitan
I see you're making appointments. People are confirming easily or you have to pressure them. So what what is your pitch to them?
00:44:05 Felipe Miranda
So basically, uh, The reason I wanted to touch base with you uh about the new product we're doing with some more P S games. You know, I think it's important for you to know the fact that, The president of JVL is currently here. I would love for you to meet him. We have some very interesting possibilities for your route, Not only a new game but also transactional products for gift card redemption that I think will solve many of your problems in your route. Do you have some time this week or next week to meet? Wonderful, wonderful, wonderful. We always celebrate.
00:44:47 Felipe Miranda
They are they're all agreeing most. Some I have some people that I need to call back next week. Solid solid. But yeah, solid. I ordered the sushi, he wasvegetarian. You're absolutely right, So he wasvegetarian and I ordered. Uh, you know,
00:45:05 Val Levitan
Avegetarian roll or vegetable rolls, yeah, yes. Yeah make make sure that there is no meat on the same or fish, like justvegetarian order thevegetarian too. So for this contingency, this is a wonderful solution. We don't have to go out with them. Yeah. We can have focused conversation and sushi is finger food, so it's very easy to ingest while you converse.
00:45:29 Felipe Miranda
Yeah, it's not messy as such.
00:45:31 Val Levitan
Yeah, so you open a tray, put a put a tray in the middle. Yeah, I should probably bring one of the round tables or black round table or we could put it there. You know they could put it there over there.
00:45:41 Felipe Miranda
I just don't I might need to go get some water because we don't have more water. I need to go. Why do you have to go to Sam's Club,
00:45:49 Val Levitan
Sam's Club, whatever you call it.
00:45:50 Felipe Miranda
Yeah, Sam's Club. No, I normally go to Sam's Club when I when we need to get stuff and buy for the company.
00:45:58 Val Levitan
Okay okay listen you know what you're doing.
00:53:59 Val Levitan
How do I, who do I start with at United if I have to? Who's the most senior and serious guy there?
00:54:22 Felipe Miranda
Business guy,
00:54:23 Val Levitan
Not a tech.
00:54:24 Felipe Miranda
No, no, no. Not a tech business guy. It's.
00:54:29 Felipe Miranda
I've been texting him. He's not replying. He's never replied to me. There was before that it was Jason Hall, who is in now with helping Andre at income. He, he was the person. I had contact with.
00:54:45 Val Levitan
Jason Hall, was with United?
00:54:48 Felipe Miranda
Yeah, he was the he was my contact for for placing orders and everything. I remember one time I had, Talk to him about five diamond links and trial, and then just say no, I don't want trial. If if they want trial, they have to pay something. And then he said okay, then we don't want them or whatever. But yeah, it was everything through JSON. I could never go well when Christos was there.
00:55:16 Val Levitan
Christos was with United? Christos where is he now?
00:55:22 Felipe Miranda
He's with Dallas Interlock. He's the guy that, I made that he was a student. Yeah,
00:55:40 Abiguele
Jason Hall.
00:55:42 Val Levitan
Yes, he is inum local here.
00:55:52 Felipe Miranda
I think so. Yeah, you should be local here.
00:55:54 Val Levitan
You have a cell number?
00:55:59 Felipe Miranda
I know, Andre has direct contact with Jason. From the InCom.
00:56:13 Val Levitan
Andre, do you have Jason Hall's cell number? Just email address? You mean the guy from Logical? Jason Hall from InCom.
00:56:49 Val Levitan
Can you send it to me?
00:57:21 Val Levitan
Can I please see the envelope of the blue card and the black card?
00:58:58 Felipe Miranda
I'm gonna send you his number. I don't know if it's the current one or if this was his business number with United for Jason. Yeah.
01:02:05 Val Levitan
Jason, this is Val Leviton with JVL. How are you? Good, good. Are you busy? Am I interrupting? Um, I'm in Atlanta. I'm actually working from Atlanta located located in Buckhead. Can I invite you to uh dinner or lunch, so we could sit and chat? Like to uh learn more about you and and.
01:02:39 Val Levitan
I'm uh working here weekly, so I fly uh in and out of Miami. Uh I'm returning uh this Friday and coming back on Sunday. Sun-Sunday meaning I'm coming back Sunday to Atlanta, so next week until Thursday I'm here. I'm here tonight, I'm here. I'm leaving tomorrow. Here here tonight or next week.
01:03:14 Val Levitan
Fantastic, where do you wanna meet? Buckhead somewhere or close. I don't. That's fantastic. I just like a little bit upscale places. So you'll you'll let me know what it is? No, I would love to meet as many people as possible. I'm here to meet. Camila is a girl or a boy? Okay. That's fantastic. I also understand that you uh worked for United, am I correct? Okay.
01:04:10 Val Levitan
Interesting. How long did you work for, uh, for them? Hmm. I don't know that. Okay. Just for your information, I will i also uh requested a meeting with uh uh legal counsel at at G L C just wanna make sure that nobody is alarmed and everybody is at peace.
01:04:56 Val Levitan
Okay. Tuesday lunch. Thanks. Bye.
01:05:38 Val Levitan
I need to move the Mariani meeting. Is that possible or is he going to be upset about it? Hold on, let me hold on. Hold on before you do that.
01:06:16 Val Levitan
Can we do Wednesday instead?
01:06:31 Val Levitan
Fantastic. Eleven thirty it is. Excellent. Excellent, Wednesday at eleven thirty. Bye.
01:07:56 Val Levitan
That changes a lot of things that Jason worked for, income. Thank you for telling me. Worked, sorry, worked for United. Yeah. That changes a lot of.
01:09:23 Abiguele
Bon appetit.",)
