# Raw Transcript — Bank of America (CashPro) API capabilities
**Date:** September 8, 2026, 12:30–1:05 PM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_Bank_of_America_CashPro_API_Integration-September-8-2026]]
---
00:00:03 Speaker 1
Thank you so much for joining today. I hope you had a great weekend. We do have Linda Hernandez on the line again, which is your relationship manager for JVL. I also have Connie Burke. She's the specialist that was going to cover. Is Nathan going to be doing it today?
00:00:23 Speaker 2
I hope so. He's usually very punctual.
00:00:27 Speaker 1
I know he was asking a lot of questions about the sandbox and the API.
00:00:34 Speaker 1
Information and so that's why we kind of rescheduled this with Connie. I know he has some specific questions, so if you want, we can give it a few minutes for him to join.
00:00:46 Speaker 2
Here, here, here he is.
00:00:49 Speaker 1
Hey.
00:00:55 Speaker 2
Good afternoon
00:00:59 Speaker 1
Nathan. Good afternoon. Thank you. And I was just saying to Val, thanks for.
00:01:06 Speaker 2
Yes . Yes, and and I am just an executive standing by, just in case you need executive decisions. I'm not an engineer. I will not be participating in anything, so I'll be silent in the meeting. I'm here only for executive purposes.
00:01:23 Speaker 1
Understood. Yeah, and I think we kind of talked about that last meeting. So Nathan, again, thanks for joining today. We have Lenin on the line. And also have Connie Burke on the line. So I know there was questions on the sandbox and that you're using Microsoft Dynamics 365 and just kind of how everything is going to work. And I think he had some specific questions. So I'll go ahead and kind of take a step back. I'll let Connie introduce herself, and she should be able to answer most of the questions.
00:01:56 Speaker 3
I have. Okay, sounds good. Great, thanks, Brooks, and thank you for joining us. To talk about Bank of America's API capabilities, so why don't you walk us through, Nathan, what your your goal is, what you're what you're looking to do from an API perspective? We have a set of APIs that we support here. Why don't you kind of walk me through some specific? Are we looking for just like a reporting, like a daily bank statement for reconciliation purposes? Are we looking at payments?
00:02:33 Speaker 3
Tell me what the goal is.
00:02:35 Speaker 4
Is. So, short - term goal is reconciliation purposes. So, being able to verify balances or money has transferred successfully, and then then reconcile that with our within our applications and MSBC. So, that would be a daily a daily check or a daily API call. So, not like an end of month. Right. Okay. So that's the initial goal, and then we are moving money through others, through the systems, through other systems, or third - party providers. Um. So I can see that being a goal in the future as well. Is how do we initiate the moving of money from our systems? The overall goal is going to be you know as much automation as recently possible for for the systems.
00:03:33 Speaker 3
Okay. And when you say move money, are you talking about like transferring to accounts at other financial institutions, making vendor payments? If vendor payments, what type of transactions would those be? Would they be like a in some cases maybe less so than others? Maybe a wire, but more more frequently an ACH.
00:03:58 Speaker 4
So our initial systems are doing ACH transfers from. Okay. That's a that's our initial flow. Is daily ACH transactions initiated, and as those flow through the third party into the JVL bank accounts, then that's the API calls we're going to make into Bank of America to verify those are completed. But, but future would be expanding rather than the other third parties. Bank of America as an option for initiating those trans ACH transactions.
00:04:34 Speaker 4
From customers, so I can also see, if we have capability to make payments to vendors through that same type of mechanism, that's certainly a future option.
00:04:47 Speaker 2
Just to add to what Dayton said, we obviously have suppliers. Many of them are in China, and we make regular wire payments to them.
00:04:58 Speaker 3
And are those wires typically in U. S. Dollars or in the local currency? U. S. Dollars.
00:05:09 Speaker 2
U. S. Dollars. For some reason, everybody demands U. S.
00:05:15 Speaker 3
Dollar. Yes, they they do. Unless you you can have a conversation with some of our FX partners and and convince them why it makes sense to get paid in their local currency, but that's probably a conversation for for a different time. So let's talk a little bit about what you've. Share that daily bank statement is it's often referred to. Sometimes it's referred to as bank feed, but getting that from an API perspective, balances and the transactions. So basically, everything that came in to the account, everything that went out of the account, and of course, Bank of America does have APIs that we've already developed for that specific purpose. From both from the prior day perspective.
00:06:02 Speaker 3
Which is generally, you know, around seven a.m. You set up MSD to make go out and make that call, and then it will bring in those balances and those transactions for the prior day, and then you will work out, you know, matching rules in MSD and things like that to be able to get those those transactions posted. We do, of course, offer a current day, but if that's less of a need, then you know we can strictly focus on on the prior day.
00:06:33 Speaker 3
And what the conduit is for in either case, whether it's balances and transactions or prior day or current day, the conduit for that is our Cash Pro system. So, Brookton and Lennon have probably talked to you about that, and that that would you know once Cash Pro is set up, and that prior day and or current day reporting is set up for the accounts that are in scope, and the Users are entitled at JVL that would need you know to to make that API call, then that that piece can be automated. But that that's that's the thing that needs to happen first is Casper would need to be implemented. The users would need to be entitled to it. One user in specific would need to be granted access to that prior day and or current day reporting API, and then you would set it up. And we have a.
00:07:31 Speaker 3
Sandbox for you to be able to test in to make that connection and make sure that everything is working as expected. And then once that's the case, then you can go ahead and request production access for that. And as I mentioned, Cash Pro, the person at JVL that would request that access would be the primary administrator that you all would designate, or you know. Generally, we suggest you have at least two primary admins for the Cash Pro system. But in that, you know, in that case, either you know one of a primary admin would would need to go into our API developer studio and request that sandbox access first of all, and and then of course the the production access at the at the appropriate times from there. So let me pause for just a moment and.
00:08:29 Speaker 3
See what questions I've shared may have prompted.
00:08:34 Speaker 4
Okay, so the immediate need is definitely prior day covers what we need as we'll be looking back in as transactions clear. Sure. We will then looking back. I'm assuming it's going to be a prior day, right? I don't see an immediate current day need. Okay. Um, and then on the user access. Is that when the API calls are made? That system to system is that still like a user based, or do you have like token identification or secrets for systems?
00:09:11 Speaker 3
So it is. It is that. So that's a piece of it too. That token authorization, that OAuth, and then the you know validating those credentials. It's not the person that is is making the call. You're automating that in the system. But there has to be an active Cash Pro user in place for that connection to to work. So that's that's the conduit.
00:09:40 Speaker 4
So the admin would configure the access tokens and secrets.
00:09:45 Speaker 3
Yeah. Well, actually, the secrets would be provided between the the sandbox testing and then of course the the production testing. But it's really kind of two pieces. You're working with our Cash Pro online system to make that connection as part of the connection. But then there's other steps along the way, that that customer ID, secret, and so forth. That will be all provided during the the setup process with our API developer studio and our ops team. Does that make sense?
00:10:22 Speaker 4
That makes sense.
00:10:29 Speaker 3
So, any further thoughts or questions about the reporting piece of that? And there's, of course, a lot of information. If it hasn't been provided to you already, we can send it to you. You can even go in prior to Cash Pro being set up and request sandbox access. But sandbox access will need to be requested again once Cash Pro is set up. Okay. But but developers. You know, have can have access to our sandbox and kind of work with you. Just have to start out with like an IP address that we would whitelist, and you don't necessarily have to have Cash Pro credentials at that point in time to go in. And first of all, look and see the the APIs that we offer, but also to set up that that thing that's sort of a pseudo sandbox,
00:11:20 Speaker 4
Sure. Do you have API docs available outside of the
00:11:25 Speaker 3
Sandbox? I'm sorry, API.
00:11:29 Speaker 4
Documentation.
00:11:31 Speaker 3
Yes. Yeah. We can. There will be some that will be provided, but yes, we can provide you like a whole step - by - step, you know, process and some tips and tricks about connecting with JSON and all of that. So there are things that we can send you now. It's just I wanted to be very clear about you know the the pseudo testing, if you will, and then the actual sandbox testing once our Cash Pro system is implemented. For JVL and then moving into production after that.
00:12:02 Speaker 4
Okay. Yeah, I think the API docs would help me ask questions once I have a feel for how the APIs work. Sure. So I don't really need a sandbox outside of Cash Pro being set up.
00:12:16 Speaker 3
Okay. Okay.
00:12:17 Speaker 4
Documentation.
00:12:19 Speaker 3
Yeah. Just know that you can, if you wish. Okay. You know that's that's an option for you to to go in and do that. So let's talk about payments for a minute. So you mentioned about your your initial after the recording is set up is to be able to go out and debit funds from your customers. Now at this time, Bank of America does not have an API for ACH debits. Okay. So that would need to be done in more of a file-based method or via our Cash Pro Online.
00:12:58 Speaker 3
We talk about cash flow online in a little bit today, where you know templates could be set up, and but but probably more desirable since the debit API doesn't exist is maybe you all creating a which we know Microsoft Dynamics does Central can do a Notchup file with those those that you know those debit instructions, and then that can be that can be gotten to us in a couple of different ways. So you can. Transmit that over a secure SFTP connection, or it can be manually uploaded into the Casper Online system to create all of those payment instructions. Someone has to approve it, and then you know we we send those downstream to debit your customers on the date that their payments are due. And of course, you would have agreements in place. It sounds like you already do, but you would have agreements.
00:13:56 Speaker 3
With them in place, that you know, this Bank of America file would be, you know, the one debiting their accounts. Okay. Now, from a credit perspective, you mentioned Val that you do have, you know, payments or a future state where you know you'd be paying vendors and things like that. We do have a credit an ACH crediting API that's available to both credit people. Or companies, and then we also have the API for those international wire transfers that you mentioned. So those can be those credits going out can be accomplished via API. It's just the limitation is in being able to go out and debit your customers for the funds that they owe you. Does that help?
00:14:57 Speaker 4
Yeah,
00:14:57 Speaker 3
That makes sense. That makes sense. Okay, and if you wanted to be consistent and you're like, okay, well, I gotta send a debit file for, you know, the these ACHs that I want to, you know, take the funds out. You could also create a credit file and send that over that same SFTP. If you wanted to do that, you don't, you know, if you prefer API for those credits, absolutely, that's an option that's available to you, but. Some of my clients, you know, they after we have these discussions, they're like, "Well, let's keep payments as consistent as possible and put it on a file." Now, if the wires are sort of few and far between, you know, much less so than the ACH credits that are going out, sometimes our clients elect to just do those through the Cash Pro Online system instead of doing an API call, instead of sending a file, which would be a different type of file.
00:15:56 Speaker 3
For that, but it really comes down, you know, with wires, it comes down to a numbers scenario. So when you think about, you know, that that supplier that you or the suppliers that you pay in China via wire, ballpark figure, what is that? What does that number of wires per month look like? Or and are there other vendors that you pay via wire?
00:16:20 Speaker 2
Probably, hundred fifty thousand per month.
00:16:27 Speaker 3
In dollars or in dollars U.
00:16:31 Speaker 2
S. Dollar one hundred fifty thousand U. S. Dollars per month.
00:16:35 Speaker 3
And is that typically one wire per month?
00:16:40 Speaker 2
No. It would probably be ten.
00:16:42 Speaker 3
Ten. Okay, so that would be manageable via the you know Cash App online. You could create a template for those different vendors that you're paying. In that way, go in, put in the new amount. You know, put in the invoice number, submit that, approve it. But again, that could be managed via API as well.
00:17:06 Speaker 4
For the for the files for both credit end of it, you said we upload. We would upload the Notch of file instructions. There's an approval process for that. What's your overall lead time in that regard? As far as before the transaction would actually be initiated.
00:17:31 Speaker 3
So now, and actually, there's two ways you could transmit that file over a secure SFTP connection to us, and do all of your approvals in MSD, or you can manually upload that file into Cash Pro. Generally, with your ACHs, they're they're submitted whether they're transmitted or uploaded. As the next day availability, so if you knew that you needed to pay a certain vendor or debit, you know, one of our customers on Thursday, you would upload that file on Tuesday with a two-day lead time, or you can do a one-day lead time, or you can even if you upload or transmit that file to us before I want to say it's like two thirty Eastern time. Don't quote me on that.
00:18:21 Speaker 3
You can do same day ACHs, but of course those are just in the United States. ACH is only the U.S. payment rail for those Notch payments that I mentioned.
00:18:39 Speaker 4
And once those payments are initiated, is there an API to check the status of those? Could the system actually say the system advancements? FTP upload and then the next day it looks at calls the API to check status.
00:18:57 Speaker 3
So it's it we don't have the hybrid like that either. So if you if you transmit a file or upload a file, there are notifications that you can get from a status perspective either back in a file or we can get them through Capstone. So with the API process, there are status. Those, those, those. You know, and again, credits only at this time. If you decided to kind of do the debits a file and the credits an API, yes, there are status API. You know, webhooks that you could, you know, get those those different statuses. And when the team sends you the documentation about how to go into our API developer studio, just kind of look around. You'll be able to see those. You know what those status.
00:19:50 Speaker 3
And what they look like, but you can't do a file and get an API status. You would get either a file status back or other alerts or reports and statements, as they're called, via Cash Pro.
00:20:03 Speaker 4
And it's exploring that file upload as part of the sandbox as well.
00:20:08 Speaker 3
So we that would be a little bit different, but yes, we we tend to refer to that as UAT testing. But if that's the route that you decided to go. Then instead of going to our developer studio on and doing all of this, once the ACH solutions and capabilities are set up for you by the bank and wires, of course, too, then there is if if you're transmitting that file to us, there will be a whole test process that you'll work with our implementation team for. If you are just manually uploading the file, you can just do that right into our.
00:20:49 Speaker 4
I think for us there would be an exploration phase, just understanding how that would work and if it works within our current systems.
00:20:59 Speaker 3
That's good to know. Now you mentioned that you're kind of using third parties at this time to do a lot of those payments. So are you kind of entering? You're going into the system, putting in who you need to debit or credit, and then they're managing all of that on your behalf. Taking those funds and then those funds are just.
00:21:20 Speaker 4
Correct . So they have their ecosystem where they're the abstraction between us and and the Nacho files themselves. So and we do it. We can initiate transactions as they come in, and then we batch things up and we'll fire off all the debits that we have to do in the morning first thing day each transaction. Okay. And then by the end of day, there's a flow of money into the.
00:21:50 Speaker 4
Totally correct. So that's abstracted from us. They handle the Notch side. We're still accountable for all the Notch rules.
00:21:58 Speaker 3
But of course.
00:22:00 Speaker 4
Great, but they're abstracted away.
00:22:02 Speaker 3
Yeah. So you could potentially utilize that same Notch file that you you know is is having now to you know like I said either transmit to us or upload it. But it sounds like you're what you're working on is sort of taking that. Process more in - house and doing it through MSD rather than a third - party provider.
00:22:26 Speaker 4
Right. So, if we wanted to go that route, correct? So, our system fires off these, and it's an API call for a CH debit. Okay. Then it sounds like in New York, in the Bank of America's current state, it would be rather than an API call for debit, it would be add that debit. Add it to the notecard instructions, and then send it off as an entire batch.
00:22:56 Speaker 3
You got it. That is one of the the benefits of doing an API call because you can just go in and do it, you know, as those transactions occur. But like I said, from a debit perspective, we we at Bank of America don't have that capability via API yet. You can do it with credits going out. You just can't. And the thing with credits. I'll just give you another thing to recall, and of course, we'll we'll get all this. I'll get the information over to Brooks and and Lennon, and they'll get it out to you along with some guides and things like that. But is that with those payments, those credits going out? If you're currently including any type of addenda or messaging that's telling the recipient why you're crediting them, like an invoice number, things like that.
00:23:49 Speaker 3
That that capability doesn't exist in our API at this time. It would strictly be, you know, they're expecting the credit from you. They get the amount. They know what it's for. Or you're emailing them, or you're having MSD email them, or something of that nature. With the NACHA file, however, whether it's a debit or a credit, you can include up to eighty characters of addenda if it's a TBD plus or a CCD plus, or if you need more characters than that to work with, not to also accommodate what's referred to as a CTX file, still notcha, but you can put in you know nine thousand nine hundred ninety nine characters of the reason that you're paying, as opposed to being limited to that eighty.
00:24:37 Speaker 4
So, okay, understood. Okay, so then I think for the for the you know possible future would be. If the NotchUp upload file can be a solution, would be how are failures, you know, failure codes that come back, NotchUp failure codes. How does that flow back into our system?
00:25:03 Speaker 3
So, yep. If you so our if you decide to transmit that file over to us, we can send you a file back with that information. Otherwise. It is more of a. It is more of a statement that's available in Cash Pro. It will tell you. It will acknowledge the file, and it will. I think it also gives you up to twenty rejects and the reason line. But that's more of a visual than a parsing back into your system. And for for payments that did go out, whether they're credits or debits.
00:25:45 Speaker 3
The The financial institutions once they once they receive them, if they can't process them for some reason, let's say in the case of a debit where there's an NSF, that will send you back. You know, Bank of America will send you back a returns notification to let you know why that was returned, and that again is more of a a visual in cash pro, like in a PDF or a text format. I believe there is a a Back into like MSD from a I I think we can get you that in a Nacha format as well. So we'll let you know what's what's available in each of the scenarios. But you know, again, for consistency, whether it's a credit or a debit, if you wanted to go with the file process, but I might suggest that you you know do that file transmission instead of manually importing into into Cash Pro.
00:26:44 Speaker 3
But I will tell you not to again not to muddy the waters further. But if you do want to transmit it, that file can still stop in Cash Pro for let's say that to approve it. If that was part of the business process, it doesn't have to, but it can.
00:27:02 Speaker 4
The need would be as much automation as we can do because these would be run daily. It would be a daily upload.
00:27:15 Speaker 4
I guess the question is like so. On the weekend, for example, non-banking days, through our current process, we still initiate the transactions. The vendor is holding them because they have to wait for the submission window. But is that something your system has to do? So, if we were to upload these files on a Saturday, does Bank of America then just hold it then until that next window, or does that?
00:27:43 Speaker 3
Yeah, that's gonna. Typically, I think ideally you would want to put that next business day as date in it. So if you transmitted it on a Saturday or a Sunday, you'd put that Monday date in it. But let me double check about if the if the effective date is not a biz a banking day, what we would do with that? We would just hold it and process it in the next window, or if that we'd reject.
00:28:16 Speaker 3
I'll make myself a note.
00:28:24 Speaker 4
So it sounds like that's worth exploring for us. The you know the debit side. As the future, future possibilities. And then, the immediate is making API calls to you know on the what was it the prior the banking. Got it.
00:28:51 Speaker 3
Yeah. And I have a lot of clients do do that same that hybrid scenario. They take advantage of the you know the APIs that are out there for reporting, but then you know if there's limitations, then they do they do the file for payments, or they do it just because it's you know easier, and and a part of the their their current process. So you you have options.
00:29:19 Speaker 4
Okay. Yeah, I think that's. I think that gives me enough insight into what we can do immediately. So for me, the next step, yeah, seeing some documentation to help me ask better questions as I need them, and then, need to start the process of getting the sandbox. If I was ready to go with that, otherwise, we could just do the other pre-sandbox testing. Okay.
00:29:50 Speaker 3
Well, with that, Brooks, I'll turn it back over to you, and maybe have you talk a little bit about where we are in the process. What you know, ask what questions you may have to get things rolling, and then we can go from there.
00:30:03 Speaker 1
Yep, absolutely, and thank you so much, Connie and Nathan. I learned a lot there, but yeah. So where we're at, I know we wanted to have this conversation first. So what's going to happen is I'm going to conduct. Connie, just to make sure I'm on the same page with next steps for the API and the devs and everything like that, which I think I am. But what I'll do, I know I mentioned this last time, I am going to go ahead and put together a pricing proposal for you, Val, and I'm going to send it over because we haven't done that yet, Connie. So I'm going to send that over. So that would be the first step of getting Cast Pro going. So I'll send you the cost. I know you mentioned. I just want.
00:30:49 Speaker 1
One thing correct. I think you said about ten wires, but I had you listed as twenty - five to thirty wires a month. Is that including domestic? I just want to make sure I have the volume.
00:30:58 Speaker 2
It includes domestic. I was focused on China specific.
00:31:04 Speaker 1
Got it. Just want to make sure I have.
00:31:07 Speaker 2
And again, my and again my numbers are all over the place. I never really sit down and calculate it. I'm really approximating and shooting from my hips. So these numbers are incorrect.
00:31:20 Speaker 1
Understood. This gives us a place to start.
00:31:25 Speaker 2
It's a it's a it's a placeholder.
00:31:27 Speaker 1
Yep. So I'll go ahead. I'll put together what's called a pricing proposal. It's going to show all the services that are listed. I'll have that send out. I'll I'll try and get that out today, but realistically, it may be tomorrow. Just because right after this call, I am literally back to back till five thirty.
00:31:51 Speaker 1
So I'm not sure if I'll have time to put it all together, but I'll try at least to get it by tomorrow. Sent out to you.
00:32:00 Speaker 2
There is no urgency. Tomorrow is fine.
00:32:03 Speaker 1
Okay. Okay. Perfect. So I'll get that out, and then typically, if you have any questions on the pricing or anything that we talked about, or if something comes up after this conversation today, just reply back to that email. But once we get the green light from you, basically approve. Pricing and saying yes, we want to move forward. At that stage, that's where we'll start the process, and that's just to get everything going, just normal cash flow and everything up and going. The first step would, Linen would need to get the coding correctly for the account, which usually takes anywhere from three to five business days. So we'll say a week, and then we have to repaper the account, which is another additional week. So it's just two weeks right there at the.
00:32:52 Speaker 1
When I start the implementation stage, which at that point can be, I like to say anywhere from three to five weeks. It can't be sooner. It just really depends on how responsive. So, unfortunately, these systems is not overnight. It does take a process of getting everything set up, making sure that we've got the training or that you've completed training, just so you know how to use the system, and then set up entitlements.
00:33:17 Speaker 2
As well. That works.
00:33:24 Speaker 1
I think that's all I have, Connie. Did you have any other questions at all?
00:33:28 Speaker 3
I do not, but thank you.
00:33:32 Speaker 1
Perfect. And I'll reach out to you separately, Connie. But Val or Nathan, did you have any questions at all on anything.
00:33:39 Speaker 2
No further questions. No questions from my side either. Thank you.
00:33:46 Speaker 1
Though. Okay. Perfect. Well, again, thanks everyone for joining today. Thank you, Connie. Val and Lyndon, if anything comes up after this call, you have me and Lyndon's contact information. Feel free to reach out to us.
00:34:00 Speaker 2
Thank you very much.
00:34:02 Speaker 1
Thank you. Thank you.
00:34:04 Speaker 2
Thank you, guys. Thanks, everyone. Have a good day, Val.