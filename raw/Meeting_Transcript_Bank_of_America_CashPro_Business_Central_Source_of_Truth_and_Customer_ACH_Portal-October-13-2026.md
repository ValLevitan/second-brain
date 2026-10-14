# Raw Transcript — Bank of America CashPro: Business Central as Source of Truth and Customer ACH Portal
**Date:** October 13, 2026, 3:32 PM – 3:56 PM Eastern
**Summary note:** [[Meeting_Notes_Bank_of_America_CashPro_Business_Central_Source_of_Truth_and_Customer_ACH_Portal-October-13-2026]]
---
00:00:00 Speaker 1
Good afternoon.
00:00:01 Speaker 2
How are you doing today, Mr. Bell? How are you, sir? Doing good. We got Linda Fernandez on the line. What is your relationship manager? And is anyone else.
00:00:22 Speaker 1
Going to join today, Bell? Is it just going to be you? I believe Nathan is joining, if I'm not mistaken. But okay. Hold on a second. I know that Nathan is on vacation, or you put everybody as optional. I know that Tina is traveling. As a matter of fact, she's in Buffalo now, and Nathan is on vacation. So that means it's just the three of us. But what would be nice is if you could turn recording and then circulate the notes.
00:00:49 Speaker 2
We actually don't have that option on our end for the recording.
00:01:01 Speaker 2
Summary after the call, just what we discussed. Yeah. Really, all I'm trying to find out on this call is I know that he was playing around with the sandbox and kind of ready to get started. And what Connie, which is our specialist who went over the API specialist, she kind of mentioned. Typically, we want to set up the cast pro first, and then we start that process. Once it's all set up, that's when they can start kind of work. He can start going around the sandbox. He would then put. The request through there, which would be the first process. And it comes to RAPI, I'm sorry, API team, who then sends them the next steps. So it's a little bit of a process. But I know the main kind of going off the last meeting we had, the main priority was the reporting with the API, getting that prior day balances and transactions. What I wanted to confirm, just so I'm giving you the.
00:02:00 Speaker 2
Pricing is, I believe, we kind of went with the way we would be doing. I know you're familiar with Notch files for the ACH payments and just uploading them. So I wanted to see with ACH, is that how we're wanting to do it? Because I understand the API reporting part, but when it comes to you actually doing the ACH transactions, are we are you just going to be manually input importing it and approving it and, Like where you're uploading a file, you can upload the file.
00:02:33 Speaker 1
May maybe it doesn't sound like I'm totally focused on it. But I should probably ask this question again. What are my choices? I understand the ACH. What are the other choices that I can have with this platform?
00:03:07 Speaker 2
Your choices with the ACH side include doing it manually by importing a file. With accounting software, you can import a file and then go to Cash Pro and upload it. I think Nathan said that's how he'd be doing it, and then you just go in and approve it.
00:03:31 Speaker 2
So if you're wanting to transmit files via secure connection, you'll have to get approvals through Microsoft Dynamics 365 and banking. But the pricing changes for transmitting files. And I have noted that I think he was okay with just uploading the Notch files on the ACA side. Yes, sir.
00:03:57 Speaker 1
Sir, that's exactly how we're planning to start.
00:04:02 Speaker 2
We can always change that. Like if they grow and it starts getting more, you know, your high volume, you can then go towards like where you're transmitting the files. But then again, that's where pricing starts increasing and different things like that. Um. So the question, really, because I didn't really touch on it last time, is for wires. It's kind of the same concept. Now you are sending. I believe you send about twenty to thirty wires a month. So you'll have the option.
00:04:33 Speaker 2
Go in and create them manually, and have templates saved if you'd like to create templates. If it's reoccurring recipients that you'll be sending it to, you can save their information. So all that's included. You can also import a CSV file into Cash Pro as well. The question I have is if you're trying to get it to. So if you want to keep it. Doing ACH, you have that option, which is included. The pricing doesn't really increase. It's if you start importing like XML files, that's where we have to get you into what we call Cash Pro Connect, and it's it's more like transmitting them over, and then there's additional costs for that. So we're trying to see if you want to keep it at first. But Connie actually advised me. She said I think they'll probably want to start with it, where you're just manually putting in or using templates, kind of the same way you're you'd be doing.
00:05:32 Speaker 2
ACH. She recommended going that route, but if you're interested in doing like transmissions with the wire files, that's where it gets a little, little more. It's increased in price.
00:05:45 Speaker 1
But it's increased in pricing, probably marginally.
00:05:51 Speaker 2
Am I correct? I'll have to look into it. So if you're interested in that route, I'll check with Connie to see what the price.
00:06:02 Speaker 2
It's a whole. I don't want to say a platform, but it's the systems have to align. So there's a cost just for having being able to do it
00:06:10 Speaker 1
Per mile per second. For me, what's important is not the initial cost. My cost on Nathan is much greater than the cost of the platform.
00:06:27 Speaker 2
I would assume.
00:06:31 Speaker 1
But if you do it manually in terms of wires, that means somebody senior on the level of either a controller or Ina needs to go in and set up those wires initially.
00:06:54 Speaker 2
You can so with your controls. There's different.
00:07:03 Speaker 2
Employees who only have access to go and set up the payment, like a wire payment, and then once they have it set up, they submit it, and then it goes to a primary admin or someone at a higher level who is sending their approval tonight. You can have it that way. You can also have it where someone uploads a CSV file, similar to how you'll be doing the ACH. You can have a lot of wires on one file that you're uploading.
00:07:34 Speaker 1
So does the second variation require the upgraded platform?
00:07:42 Speaker 2
Correct. It still would be the same.
00:07:45 Speaker 1
Sorry. Again, it does not require the upgraded platform.
00:07:53 Speaker 2
That's correct. From my understanding, that's correct. I'll double check that. But from my understanding, if you're just doing the CSV file.
00:08:05 Speaker 1
So the CSV files would work right now.
00:08:07 Speaker 2
Correct. And for some, and I'll double check with Connie. If for some reason I'm mistaken or have that incorrect, I'll let you know. But from my notes with her
00:08:20 Speaker 1
It looked like that was it. So then I'm confirming that we are fine with the CSV files. What we do not want is to go in for every single setup and continuously keep on setting up and on repeat every single month. We don't want to do that. So if it's the initial platform, I forgot what the name of it is, then we're okay with that. But if the initial platform cannot accommodate this feature, then we want to move to the advanced platform.
00:09:06 Speaker 2
So your recipient, so you're sending these wires. Is it always new people every month, or is it? Do you have a lot of? No,
00:09:14 Speaker 1
No. It's hardly ever new people. It's always the same people.
00:09:21 Speaker 2
So with that as well, once you send it to them, you can have templates saved in your normal Cash Pro setup. If you set up all the templates or send a wire, you can save it so that you can go in and just put in the new dollar amount that will be sent, and then it can be sent over to approval. Or you can do the CSV file with all that information because it's already a template.
00:09:46 Speaker 1
It's already in there. My my my problem is this. My problem is that from an administrative perspective or controlling perspective, let's not even call it administrative perspective. From the controlling perspective, the source of truth. For vendors is residing in Business Central, and so what I don't want, and what is happening now, is that when banking information changes for a supplier, our guys go inside of the bank, the template, and change it there, leaving the.
00:10:34 Speaker 1
What's supposed to be the original source of truth, which is Business Central, leaving it unchanged, because they say, well, if it's changed, then the bank. That means it will arrive correctly, which is incorrect, because my source of truth is Business Central, and so I would like Business Central to drive.
00:11:06 Speaker 1
The the template.
00:11:07 Speaker 2
Like it okay. For me, if you're saying like automatically update for bank, so like if a one of your clients' bank updates their routing number or information, yes, account information change, you want it to automatically update without you having to manually go and update? Am I hearing that correctly, or or you're saying when you go and update it, you don't want the old.
00:11:38 Speaker 1
It has nothing to do with the old information. I want information to be taken every time from Business Central, not from the template.
00:11:49 Speaker 2
Got it. So you don't necessarily want to use saved templates. You wouldn't want the new information entered by someone on your side each time.
00:12:01 Speaker 1
But if it's entered manually, then it's problematic.
00:12:10 Speaker 1
But if it's automatically taken from Business Central every time we set up a template or every time we set up a wire transfer, then it's fine as long as it's not a manual process. What I don't want is for the template to continuously live inside the Bank of America ecosystem. I want it to be gone every time.
00:12:46 Speaker 1
But if you don't save the template, that means every time we need to send a wire, and if we don't have the capability of sending this information from Business Central automatically, then somebody has to go in, set up the template. Then it becomes laborious and unacceptable. Do I make sense? That's how I'm doing it now, and it's not working for me.
00:13:17 Speaker 2
Let me check with her because I'm not even sure if we do the other services. If that would, I don't think we have a way of pulling. I think we don't have a way of having the system pull it from Business Central. So your employees or you don't have to enter it. I think with wires, they basically force you to enter that information just so.
00:13:40 Speaker 1
Then I should
00:13:42 Speaker 2
Then I should go.
00:13:44 Speaker 1
Then I should go into more advanced systems.
00:13:48 Speaker 2
Let me see. And maybe it's something I'm unaware of. That's why when I reconnect with Connie, she's an expert on it. So if it's something that exists, she'll let me know where it's able to pull from this essential without someone on your side manually putting it.
00:14:05 Speaker 1
In. I just want to make sure. I just want to make sure that you understood. The rules of how we engage.
00:14:13 Speaker 2
I'm one hundred percent with you. I completely understand what you're wanting. I'll run it by Connie to see if we have a solution for that, and if one of these other options that she mentioned to me would allow that to happen. But yeah,
00:14:35 Speaker 1
I understand what you're saying. Okay. Also for ACH. The problem with ACH is that we want ACH to be initiated by the customer. That's the whole point of ACH, and customers are willing to do that. But we want the customer to go into our account and to set up their ACH.
00:15:10 Speaker 1
Do I make sense to you or not?
00:15:12 Speaker 2
So if you need to send them a payment, you want them to go in and enter their information.
00:15:21 Speaker 1
No. We're talking about customers. Customers pay us.
00:15:26 Speaker 2
Got you. So you need. You need a portal for them to be able to go in. That's right.
00:15:46 Speaker 1
We want them to initiate their payment to our account. We want to send them a a note that says, " Look, you will be paying us three hundred dollars monthly for the next twelve months. You need to go here. This is how you log in." And this is, and you need to set up that payment. And I and I know that this is possible because I'm doing it through QuickBooks right now. So I figured that QuickBooks have has that feature. Then Bank of America should have that feature.
00:16:25 Speaker 2
And for the payments, when you send out that note saying, "Hey, I want you to pay."
00:16:37 Speaker 2
Whatever the amount, do you want the only option to be ACH, or do you want that line to have additional options?
00:16:46 Speaker 1
If additional options are available, then of course I want as many options as possible. Every option that is available for payment, I would like to offer. For example, right now we say if you want to pay by credit card, then go ahead and pay us by credit card, but be mindful that we're charging three percent or two and a half percent, whatever the credit card is charging us. The same thing goes here. If you want to pay us by wire, then be aware that there is an X amount of dollars charged for every draw. If you want to pay by ACH, be aware that there will be fifty dollars charged for every draw. So we advise the customer in advance.
00:17:37 Speaker 1
Emphasis is made on customers, not suppliers. Customers pay us. We want the customer to go in and set up their own payments and their own recurring scheme.
00:17:50 Speaker 2
Understood. And right now you have. I know you said you do something similar through QuickBooks. Right now, are you just sending invoices out? Give them the option.
00:18:07 Speaker 1
We send an agreement. They have an agreement to pay a specific amount per month. They agree to it. The agreement is executed. Then they go to our banking side and start recurring payments. On such and such date, there is a recurring payment against this particular agreement or invoice, and that's it; it gets executed.
00:18:40 Speaker 2
I'll take that over. I'll take that away, and I'm going to be connecting with Connie. Should be this week soon, so I'll be able to connect with her. I'll see if I have any questions that she may have to come back with you, or if not, I'll come back and just recap what we stated, and then give you the solutions that we have for you that would fit what you're looking for, and then I'll be able to send over the pricing.
00:19:13 Speaker 1
Thank you very much. Did you have any other questions, Val? No questions. I'm a little bit getting kind of, I need to push it through. Kind of, let's get it done. You know? Yeah.
00:19:30 Speaker 2
[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]
00:20:15 Speaker 1
Thank you very much. I have a non-related question to Lenin, if I may, please. Go. I'm right here. So I know that we were approved, or Ina got approved, or Ina approved JVL for $60,000 car purchase, company car purchase.
00:20:43 Speaker 1
And she said that it would be possible to increase it to one hundred thousand. We don't want to go through an application process, but if it's a simple increase, then we'd like to execute that. If it involves additional processing or additional approvals, then we'll go with sixty thousand.
00:21:07 Speaker 3
Are you talking about the auto loan? She took that application over a month ago, so because it was taken over a month ago, that application is no longer valid. We would have to reapply for a new application for an auto loan.
00:21:26 Speaker 1
I think that application was approved and was waiting for us to draw the amount. Can you check our file?
00:21:36 Speaker 3
Please? Is that for the auto loan?
00:21:40 Speaker 1
Is that an auto loan?
00:21:45 Speaker 3
If from the mistake, it's been over 30 days. That was when I first met you guys.
00:21:49 Speaker 1
I thought it had no. I thought it had no expiration time.
00:21:53 Speaker 3
It does. So whoever took the application for you, and I'm sorry they didn't explain this for you, but once it's approved, from that day you have 30 days to submit for the vehicle, for the loan, and then up to 45 days to complete it. Once it's past the time, then you would have to reapply. It's not complicated. I can possibly help you guys do it through the phone. Is that a hassle? But I will tell you, they would have to run the credit again.
00:22:29 Speaker 1
I will leave it with Ina. I don't want to touch it.
00:22:32 Speaker 3
That. I'll connect with Ina. I'll send her a message, and I think I communicated that to her in the past. I'll just send her a message.
00:22:50 Speaker 1
Thank you very much. That's it for me for today.
00:22:52 Speaker 3
Mr. Bell, thank you for your patience. Appreciate your time.
00:22:58 Speaker 1
Gentlemen, just to be sure, will I get something in writing from you within a reasonable time? I don't know what's reasonable — a week
00:23:07 Speaker 2
Two weeks? Are you referring to the auto loan?
00:23:16 Speaker 1
My apologies. I wasn't clear what we talked about.
00:23:20 Speaker 2
I'm hoping to get something soon. I may be able to get you something by the end of this week. Tony, once I figure out the pricing, I'll be sending that over, and then at that point, we can show you what's included, mention how it works, and then you'll have the pricing proposal in a whole email. That's when we would start the process if you agree with the price.
00:23:49 Speaker 1
Thank you, guys. All the best to you.
00:23:52 Speaker 2
Thank you, Bob. Have a great rest of your day, Mr. Bob. Bye.