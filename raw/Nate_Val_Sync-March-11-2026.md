**Nate Val Sync-20260311_100119-Meeting Recording**

March 11, 2026, 2:01PM

25m 47s

**\
Val Levitan** started transcription

**\
Nathan Carver** 0:04\
Say that again.

**\
Val Levitan** 0:05\
Something air calls on your computer.

**\
Nathan Carver** 0:06\
OK.\
Oh.

**\
Val Levitan** 0:09\
And the reason it\'s saying on your computer because I had three different meetings this morning.

**\
Nathan Carver** 0:17\
OK, I bet you I could.\
All right, any better?

**\
Val Levitan** 0:23\
Yeah, yeah, all good now.

**\
Nathan Carver** 0:25\
OK.\
All right.\
So.\
I have. I\'m prepping for our meeting with finance today. I have a list of questions for them. We\'re pretty much down to just.\
Configuring the sandbox and so once we get that sorted out with them, how they want to configure the sandbox, but I\'ll have precise questions as far as those configurations go and that should keep it moving and then.\
Once we have that piece in place, we can initiate the invoicing and see an invoice appear in MSBC.\
So I think we\'.\
I think we\'ve mitigated a lot of risk with the MSBC side as far as creating invoices, so and then and posting posting payments for those.

**\
Val Levitan** 1:27\
So I\'ve been, I\'ve been thinking about it. Is there and and I don\'t know, this is probably a limitation of the.

**\
Nathan Carver** 1:32\
Yes.

**\
Val Levitan** 1:38\
Database that Microsoft is using, which I assume should not be the case, but here\'s my question. Is there a concern that?\
We have a lot of micro transactions.\
That will stall the processing or?\
I mean in in in terms of volume, can the database handle this volume or will it crash the application? Is there a test that we should be running like a load test of some sort? I I know that I\'m not an engineer and.\
Maybe it\'s not my thing to focus on, but as a concerned business owner, I\'m just maybe.\
Yeah, I\'m raising the subject.

**\
Nathan Carver** 2:29\
And.\
Yeah, so for MSPC we can two couple things we can do. One is we can check for any specification for Microsoft on how fast we should be making API calls.\
And then we can follow that, whether it\'s one API call per several milliseconds, their database should be able to handle high volume, but we can easily create a. We could set up a sandbox and we could generate.\
What we think a normal volume of invoicing would be for a day and whether it\'s 1000 invoices or 2000 and we could run through a simulation of just generating, you know, 2000 invoices in MSPC Sandbox and see how how it handles that load.\
So we can definitely do that.

**\
Val Levitan** 3:22\
Well, do you, do you have a requirement of let\'s say if we achieve 30% market penetration then then we should handle so many transactions?

**\
Nathan Carver** 3:37\
Um, we don\'t have a specific requirement on handling.\
For the percentage of the market, but we do have requirements that indicate every customer will have an invoice every day. So and there is a the knowledge that we\'re gonna have to scale that out.\
And our initial application is built to handle in the first iteration, right, smaller number of customers. I think the load will probably be more on our application dealing with thousands of customers. MSPC should be.\
My guess is I\'m pretty robust in handling that.\
So, but I running a load test for a high volume, it should be is gonna be straightforward. It\'s not complicated.

**\
Val Levitan** 4:23\
OK.\
OK, so.\
To which extent did you test the API between, well, our end, which is our host and?

**\
Nathan Carver** 4:37\
Mhm.

**\
Val Levitan** 4:39\
Microsoft Business Central, Have you tried every single call or have you tried a few like I\'m trying to understand to which extent have you?

**\
Nathan Carver** 4:47\
Um.

**\
Val Levitan** 4:56\
Experimented with the API.

**\
Nathan Carver** 5:00\
Correct. So I have experimented with creating customers.\
Creating updating customers in Business Central and then creating updating invoices in Business Central so.

**\
Val Levitan** 5:16\
And this is through direct Uh API call.

**\
Nathan Carver** 5:20\
Correct. Yep, this is direct direct API calls.\
That\'s right. Um, so.

**\
Val Levitan** 5:27\
And there were no hang ups. There were no misses. Is it like a pretty reliable thing?

**\
Nathan Carver** 5:36\
Yeah, it\'s reliable. So the things that we built in to the system will be.\
The most common hang up would be the the token in payment hub has expired, so it makes a request and it fails and then it has to go get a new token, reauthenticate with MSPC and then it makes the request again. So that\'s built into the system. It can handle that kind of.\
Retry. So that\'s really the only that\'s the mode. That will be probably a daily thing that we do is just reauthenticate with MSBC, but that\'s a normal expected flow.\
Beyond that, it didn\'t have any issue. All the all the pain points were just in the internal configuration so that Payment Hub sends the correct codes when it attempts to create the customer and create the invoice. It just has to have the correct codes and that\'s all internal.\
Configuration and that\'s not an API issue.\
And that\'s what I\'ll discuss with finance today is just making sure these are the codes we\'ve identified that we have to know what they are and that way finance can set it up as needed.

**\
Val Levitan** 6:50\
OK, so explain to me this then through an API we.\
Transfer the transaction data into Business Central. So we know that it\'s there now. Let\'s say all the data we we are, we have achieved our goal. We transferred the data into Business Central.

**\
Nathan Carver** 7:18\
Correct.

**\
Val Levitan** 7:22\
By which means of operation? By which operational means do we say?\
To uh, Business Central to reconcile.\
Either a daily or hourly transaction or for whatever period.

**\
Nathan Carver** 7:43\
Um.\
OK, so how do we? OK, so the plan for reconciling would be.\
Um.\
It\'s going to start when we receive the income invoice.\
Because that will allow us to take an an activation on the incom invoice cause they\'ll have a line item for each activation and then we can search our system for that.\
Um line item in the invoice, so the activation in the invoice should match on their line items.

**\
Val Levitan** 8:21\
But uh, hold, hold on a second.\
We push the data into Business Central.\
Prior to receiving an invoice.

**\
Nathan Carver** 8:39\
Correct. Yeah.

**\
Val Levitan** 8:42\
So that data is pushed based on our knowledge of what our actions were, and this is taken from our own POS or our own flex pay.

**\
Nathan Carver** 8:47\
Is.

**\
Val Levitan** 8:55\
But from our own devices. So we kind of we\'re saying, OK, we know how many cards we activated. Let us send this these transaction facts to Business Central. And so now our facts are laying inside of Business Central.

**\
Nathan Carver** 9:13\
Correct.

**\
Val Levitan** 9:13\
Then we\'re receiving somebody else\'s facts. In this case it would be income through their invoicing and at this point are we placing their facts or their their set of facts?

**\
Nathan Carver** 9:20\
Yep.

**\
Val Levitan** 9:29\
Into Business Central. So now we\'re working inside of Business Central with two data facts.

**\
Nathan Carver** 9:35\
Well, only from the sense that their invoice will go into Business Central.\
And we can verify their and we need to reconcile their invoice with what we have, so.

**\
Val Levitan** 9:51\
But that means, but that means that we already have a data set sitting inside of Business Central, which already has two key parameters, the period and the amount if period and the total amount reconciles with the incoming invoice.\
Voice, then it\'s not an issue.

**\
Nathan Carver** 10:11\
I see what you\'re saying, yeah. So the volume not per, not per activation, but just the volume coming in.

**\
Val Levitan** 10:20\
I\'m I\'m asking a question. I don\'t know. So that\'s that\'s my question. What is the trigger for reconciliation? Is it the incoming invoice or is it per transaction? My preference is per transaction.

**\
Nathan Carver** 10:25\
Correct. OK.\
So.\
Um.\
When it sounds, it sounds like what MSBC would do is when the invoice, when the incom invoice comes in, that should be a trigger to the system to start reconciling.\
Uh, line items and.\
Because our invoices will already be there and the and the income invoice is coming later. So the idea is we can trigger off income because we know that the JBL invoice is already in the system, so.\
The trigger is just using the last in basically piece of data.\
Um.

**\
Val Levitan** 11:25\
So that means.

**\
Nathan Carver** 11:25\
So that\'s the trigger and then they can reconcile per line item at that point, which would.

**\
Val Levitan** 11:32\
So you know, so in order to reconcile per line item, we at least have to have at a very minimum we could have more, but at the very minimum we could we need to have the same information or more.

**\
Nathan Carver** 11:47\
Hmm, correct.

**\
Val Levitan** 11:48\
From our transaction, from our set of data, then is offered through income.

**\
Nathan Carver** 11:58\
Correct.

**\
Val Levitan** 12:01\
Are we? Are we sure that we have that?

**\
Nathan Carver** 12:01\
Right.\
We so.\
I would say where the edge case would be is if income. I think a failure mode would be if income came in and they had a line item that we didn\'t have. So that would most likely be some type of edge case failure mode.

**\
Val Levitan** 12:22\
Mhm.

**\
Nathan Carver** 12:26\
Um, because of the because invoices are created.\
On the JVL side, on the day that they\'re.\
On the day that they\'re run or the next day and in common voices are delayed by I think what, two business days?\
But that we need to verify because if income is sending them right away and then delaying payment, that means that we could get invoices from them.\
Uh, before or the synchronization of when we get their invoice and when we actually generate ours, uh could be off so.\
That\'s what we will have to verify with income and once started that conversation, we\'re waiting for feedback on.\
Their reference number in the endpoint so we can for sure know this is how we\'re gonna trace it. And then the second piece is they\'re sending invoice format and and how we get that invoice. We need to verify those pieces.\
So I think the traceability would stay the same. The verificate the way we verify line items will stay the same. But if Incom is sending their invoice sooner, then we\'ll have to have a different trigger and it could be a timing trigger. There could be other. There\'ll be other ways to trigger the reconciliation.

**\
Val Levitan** 13:55\
But OK, so I I think what you\'re saying is that.\
Business Central will have a larger always will always have a larger range.\
Off.\
Our own invoices or our own transaction records than we get from income.

**\
Nathan Carver** 14:20\
Yeah, that was my thinking. And the reason I thought that is because of when in Comm sends their invoice.\
Um.

**\
Val Levitan** 14:31\
So I\'m just curious whether it could be accepted as a.\
As a rule.\
And what if it\'s not? Then what?

**\
Nathan Carver** 14:48\
Right. So if something doesn\'t exist, what do we do? Is that?

**\
Val Levitan** 14:55\
I I don\'t even know whether we should be thinking about it. What would be a?\
What would be the scenario?

**\
Nathan Carver** 15:06\
I\'m not sure, I think.\
So the yeah, that\'s a good question. So if.\
There is gonna we do have to have this. What happens if we run reconcile and something exists on one side and not the other and if it\'s not a issue of timing?

**\
Val Levitan** 15:26\
No, but no. But our assumption is that it always exists on our side. Maybe it doesn\'t exist on income side. We we don\'t care, but it always exists on our side. And my my question is what if we missed our side?\
What if we think we received it, but we didn\'t receive? Then what do we do?

**\
Nathan Carver** 15:43\
Correct.\
Right. I think if if there\'s something that\'s, so let\'s say we get something from an invoice from Incom and they have a an activation that we don\'t have.\
Then we need a we need a mechanism to trace that in the in the system in which we have. So we should be able to look into payment hub and for that reference number that is there.\
Their activation reference number that they put in the invoice and so we\'re gonna be capturing that from the ticket activation. They\'ll give us that reference number and then we record that in that system, so.

**\
Val Levitan** 16:26\
But could, uh, could.\
Could payment hub transaction not be there? A reset failure accidentally erase?

**\
Nathan Carver** 16:39\
Right. It\'s yes. So we have to have audits in the system that would indicate that data was lost somewhere in the chain. So and that starts at the gift gift card activation.\
We would want audit records that are outside the database, and that\'s typically just your logging. I activated this card and this is the reference number I got back and we write it to a log and then.\
Every step in the system is going to be logging that vital piece of information.

**\
Val Levitan** 17:18\
But how do we make sure that logging is that the integrity is not broken? Is there an architectural design criteria that should be implemented when designing these sort of?

**\
Nathan Carver** 17:20\
OK.

**\
Val Levitan** 17:37\
Databases like for example logging must always be sequential and if something is missing in the sequence then it\'s a red flag and and and the sequence not only that it has to be.

**\
Nathan Carver** 17:50\
OK.

**\
Val Levitan** 17:55\
Sequenced correctly, but the I don\'t know some something else need to match and something. There must be some sort of architectural standard that it\'s designed to, and if it is, has it been a part of the specification for our back end?

**\
Nathan Carver** 18:06\
Yeah, correct.\
So what we would do is you have the concept of a a transaction with Incom. So we create a database record that says I have this gift card number and I\'m going to activate it with gift with Incom and you and you create that record in the database.\
And if that\'s successful, you then communicate with Incom to activate it, and when you get that back, you write the updated information to the database. So what that creates is a.\
If the database fails on the first try, then you\'ll never activate with Incom and that prevents that activation and loss of data if the database fails after we get the response back from Incom.\
And we don\'t write that updated information to the database. What we\'ll see in our data is we\'ll see half a transaction. So then that\'s an that\'s a early, that\'s like an immediate indicator that something failed in the system.\
And we\'ll be able to trace it because we\'ve already written the gift card number. We still have traceability to understand what happened. So it\'s these multi-step transactions that we can use.\
That help us create a robust way to detect those failures.\
That\'s that\'s one method. And then there\'s there\'s technology methods that we could use like guaranteed logging messaging that we can we can write a log out to a queue and the queue system itself guarantees that that gets recorded and it has you know failover and redundancy so.\
There\'s those are there\'s both engineered system redundancy and then there\'s the way we design the system to handle transactions type of fail safe.\
So there are there are steps that we can take to do this with MSBC because we\'re using.\
We\'re we\'re creating. We have two keys, right? For example, an MSBC and Duala has the same thing. So when we initiate A transaction with Duala or we put something in MSBC, we always give it one of our internal system keys.\
And then and then we get a key back from MSBC and Dwala and we record that on our side. So both sides have like a double key that allow us to look for these failure states if.\
The transaction only halfway occurred. We\'ll see that because we\'ll see missing missing keys and we\'ll be able to trace back to what happened.\
So I don\'t know if that makes sense. Um, if that.\
Answers your question on how often an engineering perspective we can try to design for that.

**\
Val Levitan** 21:21\
Well, it does what? What? I still don\'t have a clear picture.\
Is whether.

**\
Nathan Carver** 21:31\
OK.

**\
Val Levitan** 21:33\
This development hygiene has been or this development standard or development requirement has been discussed with those that are writing our back office host.

**\
Nathan Carver** 21:34\
She.\
OK.\
Understood.

**\
Val Levitan** 21:52\
And uh, I I assume that it\'s it\'s being written by.\
By Dima and Sergey in Minsk, unless it\'s written by you.

**\
Nathan Carver** 22:08\
So the part that I wrote is gonna with MSBC, so that redundancy is is being put into the system. The gift card activation is gonna be I think Dima.\
So I\'m not sure how they\'re designing around that.

**\
Val Levitan** 22:27\
But who does? Who? Who\'s actually designing the back end of it? Dima?

**\
Nathan Carver** 22:34\
Yes. So there Dima will be doing, I I believe so. That\'s what Pavel indicated in our morning discussions.

**\
Val Levitan** 22:43\
So has has has this sort of.\
Development standard be discussed or implemented. I I wouldn\'t try to hope that it\'s understood unless it has been explicitly discussed.

**\
Nathan Carver** 23:01\
That I don\'t. No, no, we did not discuss that design. What we have discussed is there is a reference number that we must get back from income when we activate the card and that\'s going to be used right for reconciliation, so.\
That part they know, but they haven\'t implemented that yet because of their work on Flex POS, so they haven\'t done the gift card activations yet.

**\
Val Levitan** 23:30\
OK, so this meeting is transcribed. So when you send me the transcription, would you then please initiate?\
I guess an e-mail exchange that raises the question of.\
The design integrity.

**\
Nathan Carver** 23:55\
OK.

**\
Val Levitan** 23:57\
As it as it concerns the back office.

**\
Nathan Carver** 24:01\
OK. All right. Would you like me to send that to you, to you and Pavel? Like how would you?

**\
Val Levitan** 24:08\
I think it needs to cover Pavel and yeah, Pavel with a copy to myself.

**\
Nathan Carver** 24:12\
OK.\
OK, I can do that.\
No problem.

**\
Val Levitan** 24:28\
OK.\
Anything else?

**\
Nathan Carver** 24:32\
All right. No, no, nothing else. Moving forward with Duala now.\
In integrating there so.\
We started on that this week.

**\
Val Levitan** 24:46\
Explain that. What does it mean?

**\
Nathan Carver** 24:50\
So initiating the ACH transfers from the customer and then the transfer to from JBL wallet to JBL bank. So those are the features I\'m building now.

**\
Val Levitan** 25:07\
OK, OK. And when you say building it, this means that you are testing this functionality in inside their sandbox.

**\
Nathan Carver** 25:16\
Mhm.\
Correct, right. I\'ll be creating our API calls to that sandbox so I can test test the flow and functionality.

**\
Val Levitan** 25:31\
OK, great. Thank you very much. Please circulate the the transcript.

**\
Nathan Carver** 25:38\
OK, sounds good. Thanks, Don.

**\
Val Levitan** 25:40\
I\'ll see. I\'ll see you later today at the financial meeting.

**\
Nathan Carver** 25:44\
Alright, sounds good. See ya.

**\
Val Levitan** stopped transcription
