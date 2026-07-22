**Flex-POS_registration_form-20251128_100122-Meeting Recording**

28 November 2025, 03:01pm

1h 10m 18s

**Juan Martinez** 0:05  
I just started the recording, Sir.

**Val Levitan** 0:08  
OK, so I'm going to repeat myself. The objective for today's meeting is to review Pavel's e-mail. Juan's reply to the e-mail. e-mail is title titled as Payment Hub Specification Requirement 980.  
And I want to review the requirement 980 itself. So I have both of it open in front of me on my screen. I recommend you guys do the same and we just talk through the points.  
That would probably be the most efficient way for us. So I'm looking at requirement 980 as it is as it's reflected in JIRA.  
Would anybody want a link to that?

**Juan Martinez** 1:01  
OK.  
I have it up.

**Val Levitan** 1:03  
OK, so let's just maybe start from acceptance criteria and the easiest thing to do is to go through data entry.  
That would probably get us quickly to a point.

**Juan Martinez** 1:24  
Sure.

**Val Levitan** 1:24  
So.  
In the acceptance criteria we have the following fields, first name, last name.  
E-mail address. I agree to all three.  
There is an abbreviation here LLH. It says location name. So does LLH stand for anything?

**Juan Martinez** 1:53  
Yeah. So the the purpose of this requisition was after our last call where we acknowledged that we did not give Igor enough information to properly create the web page. So yes, this data entry acceptance criteria.  
Is a combination of basic customer information that I know JVL will need, plus simultaneously some of these fields are required by income for their customer and location verification.  
Per their supplied Excel onboarding form. So LLH is the location license holder name where? Yep.

**Val Levitan** 2:41  
OK.  
OK, so would you mind, would you mind Mery maybe in the parentheses decoding the LLH because I forget abbreviations.

**Juan Martinez** 2:44  
Second, go ahead.  
Sure, sure.  
Do that.

**Val Levitan** 2:57  
OK, so I understand that LLH is a requirement from income, so we're going to leave it the way it is. And what does location DBA mean?

**Juan Martinez** 3:05  
Yes.  
So many owners of, let's just say Gas Station A, they use a doing business as name. It might be owned by Sam Patel, but he's doing business as Megaway Gas Station and they've legally registered that name.  
With Georgia Lottery, so I put there if applicable. So some companies are doing business as a different entity name, others are not. So it's not a required field, but it is also listed on the income onboarding form.

**Val Levitan** 3:47  
OK, so agreed. Just let's the code abbreviation to it. So location.

**Juan Martinez** 3:52  
Absolutely. I'll I'll do it.

**Val Levitan** 3:55  
Thank you. Location DBA is accepted, unless Pavel has any comments.

**Juan Martinez** 3:56  
Yeah.

**Pavel Frolov** 4:00  
Oh.

**Val Levitan** 4:01  
Hours of business operation. I don't see why we need it, I don't see why it's requested and I don't understand why we would want it.

**Pavel Frolov** 4:04  
Yes.

**Juan Martinez** 4:13  
Yeah, normally we JVL don't want it, but for some reason it is listed on the income onboarding form. I don't know if that helps them fine tune billing or if they know the business closes at 9:00 PM and there's a gift card transaction at 11.  
That's technically impossible. I don't know if they flagged that for suspicious activity, but that is again from the income onboarding form.

**Val Levitan** 4:41  
It could be an erroneous field. Can we confirm this with income?

**Juan Martinez** 4:47  
Yeah, we have their income form and it is on their form.

**Val Levitan** 4:53  
Sometimes forms are outdated.

**Juan Martinez** 4:57  
OK, I will verify it with Incomm.

**Val Levitan** 5:04  
So the undertaking is to verify the field necessity that is called hours of business operation. The undertaking is assigned to Juan.

**Juan Martinez** 5:14  
Yeah.

**Val Levitan** 5:19  
Confirm e-mail address agreed. Cell phone number agreed. I would only focus right now on US format.  
For design of our database, I don't know if you want to build in a.

**Juan Martinez** 5:35  
Yes.

**Val Levitan** 5:43  
Handling for multinational, but I don't see us using the system multinational right now.

**Juan Martinez** 5:54  
Great.

**Val Levitan** 5:54  
Although sorry, although I'm wrong because I know that there is an immediate requirement in Colombia.  
That could be applicable to us.  
So yeah, let's let's do multinational format.  
So what is the difference between LLH location name and the?  
Fields under the cell phone, which is address line 1-2, city, state, postal code and then there is another. Then there is another LLH number. OK, so forget the number.

**Juan Martinez** 6:40  
Uh, the.

**Val Levitan** 6:47  
Let's just focus the address for now.

**Juan Martinez** 6:51  
Yeah, the LLH location name is just the name. This is the.

**Val Levitan** 6:56  
Or just the.  
Gotcha. So maybe for maybe for clarity, can we just bring the address fields under the LLH?

**Juan Martinez** 6:59  
Yeah, and then.  
Sure.

**Val Levitan** 7:11  
OK, then LLH number I understand the MLH number I don't understand.

**Pavel Frolov** 7:22  
Master.

**Juan Martinez** 7:22  
Again, that's the master license holder and that is also a field on the income form. And and Val, we talked about this. There may be a very rare situation where we may want to sell our system to United.

**Pavel Frolov** 7:30  
Yes.

**Juan Martinez** 7:41  
And United would want to deploy it across the locations that belong to them. And that's where this MLH comes into play.

**Val Levitan** 7:50  
I know, but even that I kind of in my mind, I'm processing this information differently, even if we.  
Deploy a distributor.  
On our side for distribution of our POS systems, I still feel that.

**Juan Martinez** 8:06  
OK.  
Yeah.

**Val Levitan** 8:12  
Master license number is not required. There has to be some sort of a.  
Um.  
Wires crossed on this. I I don't see it.

**Juan Martinez** 8:25  
This is from the income form. If the fields are unusual, they're taking 100% off the income supplied spreadsheet.

**Val Levitan** 8:36  
I respect it. I would just verify, verify it again and and ask them to explain the grounds for this.

**Juan Martinez** 8:44  
OK.

**Val Levitan** 8:48  
Just for clarity.

**Juan Martinez** 8:48  
Will do, but again and I put there if applicable, so it's not required, therefore it would not stop the form from being completed if it's not entered.

**Val Levitan** 9:01  
OK, let's keep it. Let's keep it in the form right now, but let's just verify just for our own knowledge. Just for transparency and clarity, I sent a message to John at income.

**Juan Martinez** 9:08  
Sure.

**Val Levitan** 9:16  
Asking him if.  
The approval of a location could be instantaneous instead of three days. I expect that he'll reply next week and I will let you know what the reply is.

**Pavel Frolov** 9:31  
OK.

**Val Levitan** 9:34  
So e-mail verification. I'm just gonna read the off of the requirement.  
Um.  
Upon submission, the system sends a unique verification code to to the entered e-mail address. Yeah, customer must enter and receive code. Yes, the system might must validate the code.  
All.  
Yes, user cannot proceed until the e-mail is verified. Yes, agreed. The same goes for.

**Juan Martinez** 10:08  
And then?  
It doesn't have to be a code. It's I saw Igor responded with is a link acceptable and I would assume yes, if whatever is easiest for us, both are acceptable and that's how I responded to him.

**Pavel Frolov** 10:26  
Yeah, so highly likely it will be two types because for some reason some mail providers probably cut links, but we will provide additional codes that can be entered either link or code.

**Val Levitan** 10:27  
OK.

**Juan Martinez** 10:43  
Right.

**Val Levitan** 10:46  
OK, I agree with the cell phone verification as it reflected in the requirement.  
So what does master service agreement?  
Mean.

**Juan Martinez** 11:16  
A master service agreement is is an industry term, just that it's a contract. It's just a different name for a contract and I saw that it caused some confusion Pavel with your questions and I can call it a contract, but most people do call it.

**Val Levitan** 11:27  
What?

**Pavel Frolov** 11:31  
Yeah.

**Juan Martinez** 11:35  
Service agreement so we can replace the word contract with the master service agreement if that makes it easier for everyone to understand, but they are identical and mutually interchangeable.

**Val Levitan** 11:48  
I just don't like the word master.

**Pavel Frolov** 11:49  
OK.

**Val Levitan** 11:52  
Because it points to a master license.

**Juan Martinez** 11:57  
I can see where that confusion is in Georgia, but yeah, that that's the only place I've ever heard of a master.

**Val Levitan** 12:04  
Yeah, same here. It doesn't make any sense actually, as far as the operator is concerned.

**Juan Martinez** 12:10  
Yes.

**Val Levitan** 12:10  
But I'm afraid of a confusion here.

**Juan Martinez** 12:14  
OK.

**Val Levitan** 12:15  
So instead I prefer a location service agreement.

**Juan Martinez** 12:15  
So.  
OK.

**Val Levitan** 12:23  
So the undertaking is to rename Master Service Agreement to Location Service Agreement.

**Juan Martinez** 12:29  
Yep.

**Val Levitan** 12:56  
So when location service agreement is generated, it needs to be executed.  
Of course, my preference is to execute it electronically, provided that the state of Georgia allows electronic signature on these type of agreements.

**Juan Martinez** 13:21  
Correct, Val, the uh.  
The the question or I I did some basic lookups the software to support unless we do something simple like Adobe Acrobat which doesn't really track changes is most people want to download the contract.  
I might be the owner of location gas station A, but I'm not a lawyer. I don't know what all this means. I may want to download it and send it to my legal team for review like what you and I do with contracts today that they get reviewed and and redlined so.  
You know, I suspect 50% of the customers might accept our contract, our location service agreement as is, but most may want a change or two or at least to initiate a change.  
And how do we deal with that online in real time if they cannot download the form?

**Pavel Frolov** 14:29  
Um.

**Juan Martinez** 14:29  
And that was the real reason behind my Aruse sample red line agreement. So everybody could just get an idea of typical changes that casino and suppliers do when reviewing a contract.

**Val Levitan** 14:48  
I think that we should take a position where changes are not allowed.  
And and not negotiable. Because if we get into at least a single change, the entire ethnic community of Indians in Georgia will be negotiating with us until we're blue in the face.  
Just like it is not possible to negotiate with MasterCard and Visa and other banking alignments.  
I I just don't see what could be negotiated here, especially because our agreement is so tightly integrated not only with income but also with Dwala and and Platt.

**Pavel Frolov** 15:37  
OK.

**Val Levitan** 15:38  
I just don't see what could be negotiable and and if we allow any negotiation, we will be stuck in Alabama month.

**Juan Martinez** 15:48  
OK.

**Val Levitan** 15:50  
So I would strictly send it immediately for execution through electronic signature. I would probably make a statement that no changes are allowed. You could reject this agreement all at once.  
Or execute it. If you execute it, it becomes a binding agreement.

**Pavel Frolov** 16:14  
Agreed. OK.

**Val Levitan** 16:16  
When it's signed, all of the electronic signature applications allow a download.  
After the execution.  
So I would like to change that part one of location service agreement.

**Juan Martinez** 16:50  
So no no download link here.

**Val Levitan** 16:58  
Download link is actually available in.  
all of the electronic signature applications.

**Juan Martinez** 17:30  
OK.  
I've made some updates, so if you guys wanna refresh your Rec 980, same thing.

**Val Levitan** 18:30  
User experiment experience requirements. I am in agreement with progress indicator.  
I am in agreement with clear error messaging.  
Success messaging.  
And navigation back to the past screens and moving forward to the recent screen.  
Pages are fully responsive and.  
Uh.  
Work on mobile, tablet and desktop.  
Yes, but I would split it into MVP and 1st make it available on.  
Uh, desktop, yeah.

**Pavel Frolov** 19:24  
Desktops.

**Val Levitan** 19:27  
Because mobile may take longer.

**Juan Martinez** 20:00  
OK, um, while we're here. Um.  
The ability to go back and forth to for the user to navigate back and forth, which we agreed upon. Pavel, that answers one of your other questions is you know this has to be a fully.  
Operational website where we're saving this data somewhere the cloud so that a user can relog on and ick U where he left off.

**Pavel Frolov** 20:36  
Yeah, it relates to our last conversation and actually it was.  
Idea to have a separate status of registration when the person enters all the fields but not saved or not validated or not.  
Agreed on agreement form at at this moment. Actually we can presave all this data and assign it to his account, but with some status like template.  
And it will not be accept accessible. He he will not be able to log in to his account I think.  
But probably we can load it from the server and next time when the customer tries to achieve the same page, he will get already filled form.  
So actually at this for this point it was a question if we really want to save this data on server side or just locally on browser on browser page on current laptop for example.  
For us it more reliably to save all the data on the server side. It's not big big amount of data.

**Val Levitan** 22:09  
Oh, I.

**Juan Martinez** 22:13  
I 100% agree. I mean if you switch mobile devices and or browsers, if you move from your Safari to Chrome, then you've lost your browser history. So yes.

**Pavel Frolov** 22:14  
Right.  
Yes, yes.

**Juan Martinez** 22:29  
Yeah, we should open.

**Val Levitan** 22:29  
OK, so with that said, maybe we should turn our attention to Pavel's reply in Juan's e-mail and because we have in in black and red and go step by step.

**Pavel Frolov** 22:36  
Sure.  
Mhm.

**Val Levitan** 22:46  
So for first question, the registration scope and sequencing, the question here is the registration step intended to create only a customer account or both customer and location and the answer is both customer.

**Pavel Frolov** 22:54  
OK.

**Val Levitan** 23:05  
And at least one location. My assumption is that the reference to customer is the actual location license holder.  
Am I correct? That's the customer. Is that the description of the customer?

**Juan Martinez** 23:28  
Yes, absolutely. But whether we're calling him to me, when I create an account online, I need to give you my valid e-mail address and create a password. That's that's the definition of a customer.  
You know it doesn't require LLH for me to create a customer account. That's Part 2. Once the account has been created, do we not see it that way on our side?

**Val Levitan** 24:02  
Uh yes, I agree with that.

**Pavel Frolov** 24:04  
Yeah, so it it can be two steps. First of all, just create a customer and the customer can be can validate his e-mail and mobile phone and then he can log in.  
Log in and enter all other fields on the second step.

**Val Levitan** 24:25  
Or at least one location.

**Juan Martinez** 24:30  
Well, yeah, location and all the fields means the same thing we yes.

**Pavel Frolov** 24:31  
Yes.  
Yes.

**Val Levitan** 24:37  
OK. So then moving on.

**Juan Martinez** 24:38  
So we would, I just want to confirm we we should automatically respond once the customer's e-mail and mobile are validated and verified. We should provide a link bringing them back here to complete the balance of information.

**Val Levitan** 24:41  
Go ahead.

**Pavel Frolov** 24:59  
Yeah.

**Val Levitan** 25:04  
OK, so moving on to the next question. Current documentation is inconsistent. The requirements mix customer data and location data, while Nathan's flow separates these two. We need confirmation on the intended sequence.  
So the answer to that the goal is to create a smooth web page experience for the customer.  
So entering his or her data and initial location data should occur at the same time. We're now establishing that it doesn't have to occur at the same time.  
The first we need is the customer.  
Uh.

**Juan Martinez** 25:54  
Account, yeah.

**Val Levitan** 25:55  
Data, customer data, verification of their e-mail address and the cell phone number.  
So that's one milestone. And then the second milestone is registration of a location for that customer and then the approval of that location.  
And the customer.  
At income or through income.

**Juan Martinez** 26:24  
Yes.

**Val Levitan** 26:29  
So that brings us to the third question. At which point is the location actually created?  
The answer here is the location. The current answer lies in in the following. The location data needs to be entered once and saved with JVL and in the event that income reject.  
A specific location detail then we would need.  
Customer to reenter based on income reported issue.  
I I I think that the answer doesn't match the question. I think the question is at which point is the location actually created. But I think we're agreeing to monitor stages of each of the.  
Um.  
Endeavor or transaction or registration point. So in here we would say.

**Juan Martinez** 27:33  
Yeah.

**Val Levitan** 27:38  
We we have registration for the customer. Thank you. Part one, we're now looking for Part 2. Please enter data for one of the locations. Thank you. Part 2 is executed. We're now waiting for formal approval.

**Juan Martinez** 27:42  
Right. Part one.  
Yeah.

**Val Levitan** 27:57  
From our legal department or from income, depending on the disclosure that we need to make, I would love to disclose as little as possible in terms of who our partners are.

**Juan Martinez** 28:10  
Sure.  
Mhm.

**Val Levitan** 28:15  
So then the the gauge or the status indicator would say you are at stage 3. We're waiting for an approval that may take up to three working days.  
We will send you a message to your registered cell number and or e-mail address, at which point you will be able to proceed or to conclude your registration.  
I'm getting real time answers from John in income.  
And he tells me that.  
And I and I asked them, and I asked them.  
Whether it's possible for them to register a location instantly.  
And he says he spoke to Allen.  
Because Allen holds the answers to it and they will discuss this issue Monday in the team call.

**Juan Martinez** 29:40  
Yeah, but so Val, remember that the person validating the data is Georgia Lottery. Georgia Lottery, like any government, is closed for federal holidays, doesn't work on Saturdays or Sundays.  
All of these other restrictions. So we we need to keep that in mind that the definition of real time and government don't even go together. They're just inefficient.  
Efficient.

**Val Levitan** 30:08  
Yes, I have full appreciation of that. And you know, I'm on the same wavelength with you. My hope is that.  
Although the approval comes from lottery from Georgia Lottery, I just hope that.  
There is a verification database that income has access to.

**Juan Martinez** 30:37  
Mhm.

**Val Levitan** 30:37  
Rather than chatting on the phone with the lottery corporation, so.

**Juan Martinez** 30:43  
Yeah, and I I already sent that message in a formal e-mail to John and they responded that no, they send their spreadsheet to GLC and wait, there is no, they're not looking anything up. There's no API, nothing. So we'll let them come back again.

**Val Levitan** 31:01  
OK.  
OK, well, I asked again. He said he'll take it up with Allen. I don't know exactly what it means. Maybe he forgot what he already replied to you. Maybe the reply will come back identical as you already told us, but let's just wait for.  
In detail.

**Juan Martinez** 31:22  
Good.

**Val Levitan** 31:22  
So back to the e-mail thread.  
Title Payment Hub Specification RAQ 980.  
The question is at which point is the location actually created? And the answer is it's in stages and each stage is prominently displayed and shared with the customer.

**Juan Martinez** 31:51  
I I will edit that to be phase one customer account creation, phase two location creation.

**Val Levitan** 31:52  
Hello.  
And then phase three location approval.  
OK. The next question is, does income approval occur during registration or only when create creating a location later?  
I think the answer now we know that it's.  
Happens after the data has been entered and income has taken its steps to verify it, whether it's instant or three days or whatever is needed, right?

**Juan Martinez** 32:35  
Mhm.

**Pavel Frolov** 32:44  
Yes.

**Val Levitan** 32:47  
So that that question has been covered. The next question is.

**Pavel Frolov** 33:00  
Who is the persona?

**Val Levitan** 33:00  
I don't.  
I don't understand the the first part of it. This affects.

**Pavel Frolov** 33:09  
It's relates to previous uh question actually but.

**Val Levitan** 33:13  
Oh, OK. So then the question that we should focus on now is who is the persona filling out the fields for location registration? Is that a location owner, representative, etcetera? It can only be a location owner.

**Pavel Frolov** 33:15  
Yeah.

**Val Levitan** 33:34  
OK.

**Pavel Frolov** 33:34  
Mhm.

**Juan Martinez** 33:36  
Well.  
Val, I mean, these guys, he may, his wife, maybe be his silent partner. As long as she has the proper credentials, she's gonna enter the appropriate e-mail address. So.

**Pavel Frolov** 33:42  
Yeah, yeah, yeah, it's.

**Val Levitan** 33:51  
It could be it. It could be a driver for all I'm concerned. I I don't know who it is, but as far as we know, the person who enters those fields is the responsible person.

**Juan Martinez** 34:05  
Correct.

**Val Levitan** 34:06  
And so we we should treat it as the location owner. If the location owner decides to share his confidential data with his driver and assigns the driver or his nanny to enter the data, I I think it should be on him.

**Juan Martinez** 34:20  
Sure, sure. And that's why I put location owner or authorized representative.

**Val Levitan** 34:26  
Right. But for JBL engineers, let's just simplify if it's.  
Location on.

**Juan Martinez** 34:38  
OK.

**Val Levitan** 34:41  
Because then we're going to get into verifying bank accounts and everything else, so I'm afraid to start diluting the responsibilities.

**Juan Martinez** 34:51  
Sure.

**Val Levitan** 35:10  
I'm struggling.  
No. So should the same e-mail be used for future reports and notifications? Absolutely, yes.  
Only that only that e-mail and only that cell number.

**Pavel Frolov** 35:25  
Uh.

**Juan Martinez** 35:25  
Yep.

**Pavel Frolov** 35:28  
OK.  
Even in case when the customer has multiple locations, he will get all the reports into one OK.

**Val Levitan** 35:38  
Yes.  
It could be. It could be sorted by locations. That's fine, but.

**Juan Martinez** 35:43  
Yeah, because in theory, one owner.  
Yeah.

**Val Levitan** 35:48  
It's it's actually we want to make sure that we institute only one channel of communication.

**Juan Martinez** 35:55  
Right. That one owner's always the guy authorizing the payments to us. So it it should only be 11 e-mail and one mobile.

**Val Levitan** 36:09  
And and actually I think that we should require a two way authentication in most of our communication.  
Or transactions, at least transactions.  
For example, we are going to swipe an account on a daily basis. I am thinking that we should send an e-mail to a registered e-mail address and say that we initiated a transaction.  
For this amount of money.  
If you feel that this transaction is fraudulent.  
Uh, please.  
You know, reply to us.  
Or something of this nature.  
Or are we planning to initiate transaction transaction in the next half an hour? If you think that this is a fraudulent transaction, please.  
Initiate a call to us immediately.  
So the the the the answer is, should the same e-mail be used for future reports and notification? For now, yes. I have to tell you that in the future I feel that.  
Uh, this feature might be extended or expanded I should say.  
But for MVP, for sure, for MVP, we're not gonna do it.

**Pavel Frolov** 37:49  
Yeah, enjoy.

**Juan Martinez** 37:49  
I'm sorry, Val, just to clarify, you mean in the future allow a secondary e-mail to be added to the customer's account that it might be a generic group e-mail on their side?

**Pavel Frolov** 37:59  
Um.

**Val Levitan** 38:01  
I feel that a feature or a capability I should say, of adding organizational structure should be allowed.  
Where the owner or the customer initiates or sets up his allowable organizational structure.

**Pavel Frolov** 38:17  
Um.  
Yes.

**Juan Martinez** 38:28  
OK.

**Val Levitan** 38:30  
And says that you know this is this is a chain of command. If you get an e-mail, this particular individual is authorized to do 123 and these steps might might might need my secondary approval.  
But I think this is way after, not right now.

**Pavel Frolov** 38:47  
Sure.

**Val Levitan** 38:54  
We can document it as a non MVP feature, but if we want to go that direction.  
I just don't want too many floaters polluting.  
Polluting our objectives.  
I am not sure what the the next question mean exactly. Assuming one customer can manage multiple location, should we create a location?

**Pavel Frolov** 39:32  
I I think, I think we can just remove as we understand that the location creation is a different step from the customer creation.

**Val Levitan** 39:45  
So we're deleting the the subject of assuming 1 customer can manage multiple locations. Should we create a location automatically, etc.  
This will be deleted. OK, so then.

**Pavel Frolov** 39:59  
It.

**Val Levitan** 40:00  
What? How? How should I read the next question? Bank account assignment to the location?

**Pavel Frolov** 40:09  
Actually this is just a name of a section.

**Val Levitan** 40:10  
It's probably.  
Oh, section. OK, so.  
Instead of assignment, probably a link is more appropriate word right? Bank account not assignment but link. How to link a bank account to a location?

**Pavel Frolov** 40:27  
Yeah.

**Val Levitan** 40:40  
Need to. So the question, the question is need to clarify on the workflow for.  
Linking a bank account to.  
The Duala JVL account. I don't think that there is such a thing as Duala JVL account.

**Pavel Frolov** 41:03  
Definitely it will be.

**Val Levitan** 41:06  
I don't. I don't think so. I I.

**Pavel Frolov** 41:07  
It will be account our our account within the dual subsystem and then when we have this account we can call API related to different spheres of creating this account.  
Uh, definitely it's it's true.

**Val Levitan** 41:25  
That's you.  
That that's that's not how I understand. I understand that between a location and JVL there is an intermediary bank.  
And yes, we report our account to Duwalla, but only for the purpose of transferring the sum of all transfers, sum of all transfers from their intermediary bank.  
To our bank, but JVL account in no way never is associated with any of the cross references to the location. Location is cross reference to Wallace.  
Intermediary Bank.  
That's my understanding.

**Pavel Frolov** 42:17  
Oh.  
My understanding the following actually for production environment it will be one GVL account created at Dvolo subsystem we will enter.

**Val Levitan** 42:32  
Yes.

**Pavel Frolov** 42:35  
Uh, our internal Uh bank account.

**Val Levitan** 42:41  
Yes.

**Pavel Frolov** 42:41  
That that will accumulate all the data from all the customers, either bank account or probably a reference to plate.

**Val Levitan** 42:47  
No.  
No.

**Pavel Frolov** 42:53  
To to.

**Val Levitan** 42:55  
No.  
I the the money. The money do not move from location to JVL.  
Cannot.  
Impossible.  
Monies are moved from locations to Dwalas intermediary bank and they.  
Go on to their account. They're deposited onto their account. Then there is a pause. I don't know whether it's an hour, 2 hours, half a day, and then in a single motion it is moved from Dwala.  
Intermediary bank to JDL account.

**Pavel Frolov** 43:39  
I do not know internal implementation of their kitchen, but definitely it will be a specified bank account assigned for JVL dual account and then a JVL.  
Oh, or not JVL, but our service. Uh, will.  
Call API to create particular customer.  
During the registration of the customer and at this moment, there are two different possible ways. At this moment we can specify particularly bank account of the customer.  
Or we can redirect page to some third party widget like plate widget.  
So this this .2 relates to this branch either to go to the plate widget or to allow customer to enter his.  
Bank account.

**Val Levitan** 45:00  
That that is fine plate service as I understand, which might be erroneous but provides.  
One type of service. Well, two types of service. There should be an API call to verify an account, so their service could verify any account.

**Pavel Frolov** 45:21  
OK.

**Val Levitan** 45:27  
And the second service escapes me right now. Uh, the sorry the.  
Verifies the amount of money on the account.

**Juan Martinez** 45:38  
The balance check out.

**Val Levitan** 45:40  
The the balance check, yeah. So those are the two types of services that is available by plan, it's available to us and so when we open an account.

**Pavel Frolov** 45:48  
Mhm.

**Val Levitan** 45:54  
For a customer, we can use plot. We will use plot service to verify the existence of an account.  
That's all we're doing. And when that account has been verified, then that's it. The account is open.  
Then we establish, then we establish the ACH relationship.

**Pavel Frolov** 46:20  
Sh.

**Val Levitan** 46:26  
Sorry, then we will. Then I assume that there will be another API call telling Duala to establish that ACH relationship with that verified account.  
But that will only take the money transfer from customer's account to the Wallace.  
Intermediary bank.  
And not further.

**Pavel Frolov** 47:02  
I think to GL account actually.

**Val Levitan** 47:10  
So that probably requires verification with while I suggest that you have a meeting.  
With Wallet to verify it, I am 90% sure that I'm right.  
And then there will be another ACH for which we are charged second ACH.  
For which we are charged.  
For transferring funds from the intermediary bank, the Wallace intermediary bank to JDL's bank.  
That would be the second charge.  
So if you were to.  
Uh, reconcile the transaction.  
Of the process of swiping money from 10 accounts.  
You will have 11 charges.  
So 10 account will be, 10 accounts will be customer accounts and one transaction would be to move money from the Wallace account, the Wallace Bank to JVL Bank. That will be the 11th charge.  
Which is extremely important for reconciliation. Otherwise you will always come up short and you you wouldn't, you wouldn't know where the short is from.  
That also means that we cannot. We need a a report of how much money is taken from each of the customer's account onto the Dwala account and then from Dwala accounts.

**Pavel Frolov** 48:46  
Yes.

**Val Levitan** 48:56  
Account to JDL account. The two reports need to match with an exception of the charge for ACH couple of cents.

**Pavel Frolov** 49:12  
OK, let's discuss this with Dwola and clarify this.

**Val Levitan** 49:17  
This is important. This is important. On the outside it may look like one single transaction, but internally it's not.

**Pavel Frolov** 49:35  
Probably we will never know about the intermediary bank and for us it will be transparent.

**Val Levitan** 49:43  
We know, we know all the time because they will in particularly and and from a from a legislative standpoint of view, we are not licensed to take money from their account.

**Pavel Frolov** 49:52  
You.

**Val Levitan** 49:59  
From customers account.  
And from a legal relationship standpoint of view.  
Oh.  
We we're not doing it.  
And from the risk assessment view that there will be an insurance implication on it.  
The data data storage. Who stores the data?  
Like we we have to be very, very clear how the money move. Yes, I mean, we could say, Oh yeah, money come from here to here and we have the money, you know?  
But we shouldn't be saying this. We shouldn't be thinking this way. We should be very binary and digitally meticulous about how the money is moved and how the reconciliation works.  
That should also probably mean that we should verify Duala's intermediary bank account.  
When we establish that handshake.

**Pavel Frolov** 51:41  
Yeah, I think we can switch to the next next point.

**Val Levitan** 51:48  
OK, will this be a third party uh plot uh widget?  
Yeah, it is. It is a plot widget, yeah, for sure.

**Pavel Frolov** 52:00  
Actually at this moment client or customer should have played account and.  
Need how to use it I I assume or just to create a new one?

**Juan Martinez** 52:18  
Not not necessarily like so I just signed up for Venmo the other day and Venmo uses Plaid. So within the Venmo app I got a pop-up from Plaid.

**Pavel Frolov** 52:25  
Mhm.

**Juan Martinez** 52:35  
And Plaid detected my bank account and just had me select the right one. I don't have an account with Plaid. I didn't need an account with Plaid. It all remained within the Venmo site. So I did get a Plaid pop up, but just to verify which bank account I wanted.

**Pavel Frolov** 52:35  
Mhm.

**Juan Martinez** 52:55  
To use and nothing more, nothing less. I didn't have to log on to Plaid or anything like that. It was all handled through and I assumed Diwala would do the same thing.

**Pavel Frolov** 53:07  
Mm mhm.

**Juan Martinez** 53:09  
Yeah, Laid looks like just a *** through.

**Pavel Frolov** 53:14  
Interesting, interesting. For now I do not see how actually will be implemented this link.  
Because actually this steps assumes that the customer do not enter this his bank account using our service, he goes to the widget.  
He works with this widget. I don't know. I don't. I even don't know how it's implemented on plate, but they work with their widget and after he finish all his.  
Steps. We will just have some hash number that we provide for Duola and using this hash number we can direct communication to their bank account.

**Juan Martinez** 54:20  
And Pavel, I I don't even think we need to provide anything to Diwala. If if you're going to the Diwala website or their widget, they they already have an established connection with Plaid. I I don't believe that.  
We we need to supply them any. Everything is done via the widget directly with Plaid. Like what I just described with Venmo, it it took 10 seconds for me to be temporarily redirected to Plaid, select my bank account and then I went back to out of Plaid and into the third party app.

**Pavel Frolov** 54:55  
Oh.

**Juan Martinez** 54:57  
That that sent me there.

**Pavel Frolov** 54:58  
How's this data went to the plate?

**Juan Martinez** 55:06  
I don't know, but my bank account and my bank name, Chase and the last four digits of my bank account popped up. Now, is it because they detected the app on my phone already? I do not know, but I've seen that happen before and it was seamless. I did not have to actually enter my account.  
Information.

**Pavel Frolov** 55:26  
For me it's just a magic. I do not know how it works and how can we will implement this.

**Juan Martinez** 55:31  
Sure, no, I understood.  
Yeah.

**Val Levitan** 55:36  
So why don't we park this whole issue of bank account alignment to the location and have a dedicated call with Dwala on this subject?

**Pavel Frolov** 55:47  
Yes.  
Yeah.

**Juan Martinez** 55:52  
Yep.

**Val Levitan** 55:53  
Juan, can you take it as your undertaking to set up a call with Juan for the three of us?

**Juan Martinez** 56:00  
Sure.  
Do you not want Nathan on the call?

**Val Levitan** 56:07  
I would love to have Nathan on the call if he's available, but if he's not available, I don't want to wait. I want to proceed with the call.

**Juan Martinez** 56:15  
For sure, OK.

**Val Levitan** 56:18  
So you could you could mark him as.  
Optional. And if he has time, of course I would love him to join us.

**Juan Martinez** 56:24  
Sure.  
Will do.  
OK.  
So does this mean we can jump down to 5.1?

**Val Levitan** 56:40  
Sure.

**Pavel Frolov** 56:42  
Mhm.

**Juan Martinez** 56:46  
So yeah, so I think we kind of answered this already above, but yeah, location name, yeah, look LLH, which I'll clarify in the requirement is numeric and LLH location name is alphanumeric.

**Pavel Frolov** 56:58  
Mhm.  
Yeah.

**Juan Martinez** 57:02  
So that's correct as you've listed it there, Pavel.

**Pavel Frolov** 57:07  
Mhm, OK.

**Juan Martinez** 57:10  
You put we need clarification. Is the LLH location name a free numeric input with no validation? And I put yeah, it should be a free alphanumeric input with no validation.  
The reason being is what you describe in the next step. Do we validate against the Georgia approved list and master location list? What you're describing there is an entirely manual process.  
That destroys all of our automation. I don't know how often Georgia updates their location list. As an example, yesterday was a big holiday in the US, so nothing was happening at the government, so we can't count on that.  
You know, are we? Are you hinting that we could import a PDF or an Excel file and parse it? That that that's very messy.

**Val Levitan** 58:01  
And and and not.  
And not only that, what do we do for Nebraska and Texas?

**Juan Martinez** 58:18  
Correct. They may not even publish that that list, but.

**Val Levitan** 58:22  
They don't. I know that they don't. Nebraska is not even as sophisticated as Georgia, and Texas doesn't even that doesn't even recognize this part of the business.

**Pavel Frolov** 58:22  
But.

**Juan Martinez** 58:24  
Right, right.  
Yes, absolutely.

**Pavel Frolov** 58:34  
Yeah, I just saying that keeping some.  
Um.  
Uh, some parsing of the document and validating data that customer entered.  
Probably will will help us to to prevent some fraud or but actually I think it it's not very reliable source because anybody can download this document intent data not related to him.

**Juan Martinez** 59:11  
And and our fraud protection is income. If income got the approval from GLC that that's a valid location, it should also be good enough for us.

**Pavel Frolov** 59:17  
Yeah.

**Juan Martinez** 59:32  
So 5.2 licensed data source we expected to fetch or parse. As I said earlier, just seems like it's too much work to do that. I think we agree that we may want to have it for reference, but we can't count on this document that is.  
Not updated real time, which we know it is not. It might be updated quarterly, once a month, every other month.  
Next question, is there an official API or data set or is it the PDF the only source? Again, it's it is the only source according to income that there is no API. They send the the form to GLC and anywhere from 1:00 to 3:00.  
To three days later, GLC approves or denies the location via an e-mail response.  
You asked, are we allowed to store the data in our database for validation? And yeah, I mean I said once a state publishes any data on its website, it becomes public data. But why would we want to store it? We don't want to store that.

**Val Levitan** 1:00:46  
Hi.  
I I I prefer not to store any data.

**Juan Martinez** 1:00:51  
Agreed, so we all agree.

**Pavel Frolov** 1:00:52  
OK.

**Val Levitan** 1:00:52  
And as a matter of fact, I suggest, as a matter of fact, I suggest advertising that we don't store any data.

**Juan Martinez** 1:00:59  
Creed. Creed.

**Val Levitan** 1:00:59  
It's just such a bad practice for so many reasons to store data. It opens up to such lawsuits and liabilities and.  
And there's no benefit. There's no benefit from it.

**Juan Martinez** 1:01:09  
Absolutely.  
Yes.  
Great. So since we're not going to store it, the next question, how often is the file updated? It kind of doesn't apply anymore. We just know that it's not real time. Same thing. How do we detect new versions? We we really can't.

**Pavel Frolov** 1:01:22  
Mhm.  
Yeah, good.

**Juan Martinez** 1:01:32  
But.  
Hello.

**Pavel Frolov** 1:01:35  
Yeah, the same. This is the next question. Also not applicable.

**Juan Martinez** 1:01:35  
What will?

**Val Levitan** 1:01:38  
Continue without me. Continue.

**Juan Martinez** 1:01:42  
Sure. All right. So what is the legal nature of MSA? We agree that we're renaming this LSA, which is the location service agreement and that is 100% a contract, so.

**Val Levitan** 1:01:56  
OK.

**Juan Martinez** 1:01:58  
We will and I'll amend the rec to say that LSA equals contract and it is legally binding, so it is a contract.

**Pavel Frolov** 1:02:04  
Mhm.  
Mhm.

**Juan Martinez** 1:02:13  
Terms of use will be defined in this contract, so customer may propose red lines per as discussed with Val. We do not want the to allow the customer to make changes.  
So I will edit this my response saying the the LSA cannot be modified at this time.

**Pavel Frolov** 1:02:39  
OK.

**Juan Martinez** 1:02:44  
So.  
OK.  
Is the MSA legally binding on its own? Yes. Once it's fully executed by both parties, it is legally binding.

**Pavel Frolov** 1:03:01  
Mhm.

**Juan Martinez** 1:03:02  
Yep, income integration. Customer completes registration. Need clarity on how data is sent to income, who triggers the sending and in what format. For now it is e-mail.  
Yes. So for now, correct income has provided the Excel sheet with the data they require. So once the customer completes the online location registration.  
Information, the submit button. We should extract the relevant information that needs to be sent to income and send it. I believe they will probably accept it in in a normal table format. It doesn't have to be XLS long as all the.  
fields that they require are there.

**Pavel Frolov** 1:03:57  
But who? Who will be the person who pushes the button send income data? It will be just the customer. He fulfill all the fields.

**Juan Martinez** 1:04:11  
Correct. Once the customer has completed all the fields and you save or submit, all the data is saved and that should automatically trigger the automated e-mail to income. But what I put in there because one of your other questions is.

**Pavel Frolov** 1:04:12  
Uh, OK.  
Mhm.

**Juan Martinez** 1:04:29  
That e-mail should come from a new JVL specific group e-mail address so that we're all aware that it's gone to income and when it we get a response from income, we're all aware that we've gotten a response. So it just it can't go to one person.  
Has to go to several of us.

**Pavel Frolov** 1:04:53  
OK, so internally at JVL somebody will be assigned to get copy of all messages that need to initiate creation of location with income.

**Juan Martinez** 1:05:08  
Correct. And that's how I responded there on the last question in #7 there.

**Pavel Frolov** 1:05:16  
Mhm.

**Juan Martinez** 1:05:17  
Yeah, JVL submit the Excel form to Incom and we JVL get a response from Incom. I would suggest that we create a new JVL generic group e-mail address that we use to send the form to Incom and that.  
When we get the reply from income, it goes to several people, not just one person.

**Pavel Frolov** 1:05:35  
Mhm.  
OK. And and actually when somebody who receives this response from Incom sees that the new location was validated by Incom.  
I think here will be a manual procedure. Somebody will need to press enable button.

**Juan Martinez** 1:06:02  
Yes.  
Yes, agreed. Agreed.

**Pavel Frolov** 1:06:06  
Mhm. OK.

**Juan Martinez** 1:06:07  
Yeah, that that location is valid and then pressing that enable button should also now generate the automatic e-mail to the customer that he can resume going to the website, adding additional locations or that he's basically now registered.

**Pavel Frolov** 1:06:19  
Yeah.

**Juan Martinez** 1:06:26  
With us to do business.

**Pavel Frolov** 1:06:29  
Yeah, and uh, appropriate status change for the location.

**Juan Martinez** 1:06:33  
Yes.

**Pavel Frolov** 1:06:34  
OK.

**Juan Martinez** 1:06:37  
Next question #8 UX flow, which steps are blocking? Do you? Do you think that now based on all the above answers that Igor should redo?  
The Figma mockup and then we can address the blocking steps now that we've said there's a part one and a Part 2.

**Pavel Frolov** 1:07:00  
Mhm.  
Yeah, OK.

**Juan Martinez** 1:07:06  
OK.

**Val Levitan** 1:07:06  
So this meeting is recorded. We are going to produce a transcript and which steps are blocking could be addressed by a summary from AI.

**Pavel Frolov** 1:07:21  
Yeah, perfect.

**Juan Martinez** 1:07:24  
That was the last question.

**Val Levitan** 1:07:25  
So I.  
So I believe that we covered all the issues. I think we now have much more clarity. I think we have definite undertakings of what needs to be investigated. That includes the part that I took the undertaking to investigate.  
Investigate with income and it seems from correspondence with John the answer is forthcoming on Monday and the rest is assigned to Juan to follow with Dwala and hopefully we could have a meeting early.

**Juan Martinez** 1:08:03  
Yeah.

**Val Levitan** 1:08:05  
In the week, so we do not slow down our development, but in the meantime, I encourage Pavel to focus the internal group on continue developing the architecture and the spec.  
And please do not waste your time on actually coding anything until things are are cleared up.

**Pavel Frolov** 1:08:32  
Just.

**Juan Martinez** 1:08:33  
Perfect.

**Val Levitan** 1:08:33  
So.

**Pavel Frolov** 1:08:34  
Actually nothing except for UX workflow is in progress for this particular control server.

**Val Levitan** 1:08:44  
So just to be clear, your your team is focused on developing proper architecture. You're analyzing business flow. You should by now be breaking things into features, describing and building acceptance criteria.  
And start laying them out in Jira plans.  
And assigning which task should go into to do, meaning scheduling stage, but you should actually have it parked right now until the spec is more cleared up for you.

**Pavel Frolov** 1:09:17  
Mhm.  
Yeah.

**Val Levitan** 1:09:27  
Then you'll go back with the clear spec. You'll go back, finalize the architecture, finalize the feature, and start scheduling them for work. That's how I see it.

**Pavel Frolov** 1:09:29  
OK.

**Val Levitan** 1:09:40  
Don't forget that you need to bring in the QA into this. At the same time, the QA needs to start looking at the acceptance criteria and figuring out how it's going to be tested.

**Pavel Frolov** 1:09:56  
Yeah, agree.

**Val Levitan** 1:09:59  
OK. Thank you very much. Wish everybody a great day, great weekend.

**Pavel Frolov** 1:10:01  
OK.

**Juan Martinez** 1:10:03  
Thank you. Bye.

**Val Levitan** 1:10:10  
You know, I will post the transcript here. Thank you.

**Juan Martinez** 1:10:15  
Thank you.

**Juan Martinez** stopped transcription