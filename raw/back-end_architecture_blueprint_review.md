**Transcript**

16 September 2025, 01:03pm

**Val Levitan** started transcription

**Pavel Frolov** 0:03  
Yeah, and so I will share my screen. Sure.  
Sure.

**Val Levitan** 0:10  
I just want to remind everybody of a bottleneck that we're dealing with. We have a deadline on January 1st to have a big beta version on in the market with about 10 operators.  
With about 10 operators, our hardware will most likely be ready in temporary mode format.  
And one of the most pressing bottlenecks is the ACH processing.  
Through a third party where money is swiped from operators, not operators locations accounts onto our bank's account.  
These are the most important MVP's.

**Pavel Frolov** 1:07  
So actually I will not explain how our current CMS is implemented right now. I will just probably show a main part that actually relates to.  
Flex POS project and everything related to to this project, so right now.  
In the our infrastructure.  
Uh, we have uh Flex pay manager.  
This graphic user interface that actually.  
Support working with current Flex play kiosks so it supports some settings lease control.  
Uh, assign Uh income credentials and update firmware module.  
We assume that these minor changes.  
Minor changes, I mean until end of the year you're going to.  
Uh, to change this module.  
To add support here for.  
SPOS terminals on the same module using the same graphic user interface.

**Nathan Carver** 2:44  
OK.

**Pavel Frolov** 2:50  
Uh, this this module will allow us to set up.  
Both Flex OS and Flex pay devices.  
Uh, second change. Uh, we will remove uh income.

**Val Levitan** 3:06  
Yeah.

**Pavel Frolov** 3:11  
Communication from particular terminals.  
Uh, the currently Flexpay directly communicates to Flex. Uh oh to to income server.  
And we are going to move this communication to a cloud server implementation and rename it as payment hub.  
We assume that this cloud application will support some accounting and reporting and communication is in com server actually according to.  
Business requirement. It should be a third party ACH implementation also.  
This is just a blank rectangle, but I think we need as fast as possible to determine what will be the features related to this module.  
And here in Comcloud, yeah.  
So is this new schematics? Flex POS is added.  
It will work with and.  
In the.  
You know, let's put in.  
So in general it describes the next steps after January 1st. I think it will be next evolutional step.  
To move this payment terminal manager into payment location manager and and then to move it to cloud.  
Uh, what is the difference?  
Until January 1st, I think we will support location with only one.  
Payment terminal.  
Payment terminal equals to Flex POS or equals to Flex pay.  
In the future, I think we are going to support multiple devices, support hot swappable devices.  
So I assume that the settings can be assigned to location.  
Not to directly to terminal and doesn't matter what terminal will be installed on the location, all the settings will be transferred from our control server.  
Uh.  
OK.  
Uh, so in in short.  
Uh, CMS architecture change until January 1st.  
Cloud Payment Hub. The next add support of Flex POS terminal type using current CMS application.  
Then we will need to update our Flex space software and develop Flex POS software.  
To support this cloud payment hub.  
OK. Any questions? Oh, probably I need to explain in more detail something.

**Aaron Bockelie** 7:35  
It's a lot to take in. I don't have the mind of where all this is coming from and why, and I kind of have to push that. I believe you button, Pavel, if I'm being honest.

**Nathan Carver** 7:48  
I think this makes sense as an iteration approach.

**Pavel Frolov** 8:01  
So the main change in architecture will be to introduce the cloud or.  
Payment hub.  
And then the next outcome.  
To make integration with some third party ACH.

**Val Levitan** 8:28  
What? What is involved in?  
I I understand we don't have a payment hub or as you call it cloud service. Is is cloud service and payment hub, is it one of the same or are these two different things?

**Pavel Frolov** 8:47  
Uh is the same. This is uh.  
A payment hub is just a name of the service.

**Val Levitan** 8:55  
So Payment Hub is a product name.

**Pavel Frolov** 9:00  
Mm.

**Val Levitan** 9:02  
And it will be sitting in in a cloud and therefore we need a cloud architectural design that will address all cloud specifics.

**Pavel Frolov** 9:09  
OK.

**Val Levitan** 9:19  
OK, I understand.  
So what does the what decisions need to be made when we talk about cloud architecture?  
When we start thinking through this, what is there a set of decisions or is the set of pain points or is there a selection of technology, technologies, tech stock applications?

**Pavel Frolov** 9:36  
Sure.  
It stuck.

**Val Levitan** 9:55  
That we need to take into consideration number of transactions, certain bottlenecks. What do we need to think about?  
And that's and that's one set of questions, another set of questions.  
I don't think that we have time to go outside of our.  
Uh.  
Technology expertise to seek help because we simply are pressed against time and we need to select a tech stock that our guys are familiar with so we could have.  
Almost instant output.  
So what is it? Do we know what our guys know and that something that can help us to identify this tech stock and perhaps an unrelated question may be related but unrelated.  
Nathan, do you have any expertise in cloud architecture personally? Can you contribute to this or is it out of your?

**Nathan Carver** 11:10  
Yes.  
Yes, so I've I've done um applications in the cloud.  
So I think initially choose a tech stack that the as you were saying Val that the team is familiar with. So whatever language um.  
I know that they do Java and C#, or I'm sorry, Java and JavaScript.  
So we can you can easily build up a Java container and deploy that as as the payment hub module which would just be a a service and that would that can be deployed as a API service.  
Into a cloud container. The only thing we really have to worry about at this point would be.  
Horizontal scaling and that's just creating the capability to replicate the service. If we have to scale horizontally, I think that's pretty low hanging fruit.  
And then the next is whatever database the team is familiar with. That's something that we could we could spin up as the persistence mechanism if that's needed.  
And then from what I'm seeing with the HACH vendors.  
They use a combination of REST API to OAuth 2, so that for the most part they're just Web APIs. That should be pretty easy for us to integrate with.  
From our just calling that from a cloud service container.

**Val Levitan** 12:51  
OK. Thank you, Nathan. Aaron, do you have anything to add or you prefer just to sit and listen?

**Aaron Bockelie** 12:57  
I'm just listening right now.

**Val Levitan** 12:59  
OK. Nathan, thank you. I appreciate it. I understand that you have a set of requirements already worked out for the POS. Is it only a set of requirements or is it already developing into capabilities?  
And also, is it only for the POS or does it cover cloud service as well?

**Nathan Carver** 13:28  
The use cases and capabilities have really been focused on the device. The cloud has been treated as a more of a just a service that's out there. We do have some.  
We do have some um.  
Definition of of what the communication would be between the JBL cloud service and income and the ACH providers. So we show that flow of communication, but there's no requirement.  
Focused specifically on cloud service components.  
Not yet, anyway.

**Val Levitan** 14:15  
OK.  
How do we move?  
To solidifying the architecture that could support our MVP's vis a vis.  
The POS and the minimal cloud architecture that is required to get us engaged in testing on January 1st.  
Uh.  
Sorry if my question is a little bit washed out.

**Nathan Carver** 14:49  
OK.

**Val Levitan** 14:53  
You want me to read the final question?

**Nathan Carver** 14:54  
Um, I.  
I think I I think I follow. I'll try to answer and then we can iterate on it. So I think in order to help the team move forward, we take the use cases that we have that that does show the flow using an example of ticket redemption.  
And.  
That would at least we could take the income definition so we can define the API that the cloud service must provide the flex POS and then we define we have the the end points that the cloud service must call into income.  
And we can create requirements around the cloud service for those APIs. So once the engineers have the the end points, they can start filling in the middle with.

**Val Levitan** 15:39  
I maybe.

**Nathan Carver** 15:48  
Nonfunctional requirements.

**Val Levitan** 15:50  
Maybe I'm starting to understand. Let me let me rephrase my question. Um.  
Do I understand it correctly that as we entertain a cloud service today and the tech stock related to the cloud service, we are hinging today on our knowledge of how the.  
Income API works, but we're lacking understanding of how the third party payment, ACH payment processing works, but if we had that.  
Block.  
In front of us, it would be easier for us to define the cloud service and the tech stock required for the cloud service with more clarity.

**Nathan Carver** 16:43  
Correct.  
Um, once we.

**Val Levitan** 16:46  
So does it mean that our does it mean that our priority should be on selecting the third party ACH processing company as soon as possible getting their API?  
So that we could finalize the tech stack for the cloud architecture.

**Pavel Frolov** 17:07  
Actually, I don't think that this is a dependent flows because highly likely we understand that it it will be Java, it will be some Postgres database.

**Val Levitan** 17:15  
No.

**Pavel Frolov** 17:25  
Doesn't matter what API will be provided by third party ACCCH because we can do anything using Java. So we we just call in endpoints.  
That is documented by ACH.

**Nathan Carver** 17:47  
I agree. I think the ACH, since they're all using Web API, they're going to be relatively similar in how they operate. So creating adapters that can switch between vendors isn't.

**Pavel Frolov** 17:50  
OK.  
OK.  
OK.

**Nathan Carver** 18:03  
Um, isn't complicated, so that gives us a little more time than having to choose, you know, right away an ACH vendor. Um.  
But but it also doesn't. We also don't wanna push it off too far. I think there's, I think we still have some slack there.  
Because I agree with Pavel and it should be relatively straightforward just to hook up to an API.  
A Web API from from their Java service.

**Val Levitan** 18:31  
OK, so defining our priorities further, do I understand it correctly that our back end team?  
Possesses whatever knowledge they possess. We cannot on a dime turn that knowledge into something else. I mean, we'll work with what we have and it seems like what we have is Java.  
Uh.  
Application and and this is what we are going to be basing our architecture in the text taco and furthermore, since this is already defined, we should go ahead and start.

**Pavel Frolov** 19:06  
Yeah.

**Val Levitan** 19:19  
Having that team build the cloud service.  
While in parallel to that, Nathan should.

**Pavel Frolov** 19:26  
Yes.

**Val Levitan** 19:30  
Source the third party ACH provider, get their API onboard that provider and at that time we'll already have some minimal architecture built.  
For the back end and we will just integrate the Uh endpoints for that Uh API.  
Am I speaking the right language here?

**Pavel Frolov** 19:57  
Exactly.

**Nathan Carver** 19:58  
Yes.

**Val Levitan** 20:00  
So everybody agrees on this plan. Can we move forward with this?

**Pavel Frolov** 20:05  
Yes.

**Nathan Carver** 20:07  
Yep.

**Val Levitan** 20:09  
If this is, if this is our plan, what is the next course of action for and and what what? What is the next check-in point for us? Let's let's divide and conquer. What should each one of us do?  
Each one of you do parallel and not even.

**Nathan Carver** 20:31  
So my steps right now are two things. One, gather all the API documentation that's available to me with the three vendors, ACH vendors that I'm focused on.  
And in parallel, I've reached reaching out to these vendors already asking for expert, you know, either sales consulting or technical consulting on the API so I can ask them questions and start feeding that information to Pavel and the team.

**Val Levitan** 21:07  
Fargo.

**Pavel Frolov** 21:07  
OK, for me, for me, priority number one to get more deep architecture description for a payment hub.  
We will do this with Dima and then step. The next step will be to develop API communication between our Flex POS and Flex Pay to this payment hub.  
Then it will be API between payment hub and control server.  
Transfer uh uh parameters related to particular location or particular terminal.  
Uh, I think that's all it's probably.  
You uh.

**Val Levitan** 22:08  
I think we're missing. I think we're missing one important ingredient is that we need a minimum MVP's for reporting and accounting like we should develop that early.  
In the game.  
For example, certain reconciliation reports between the payment hub and the location between the payment hub and the operator, and we need basic reconciliation reports just to.  
Manage transactions or at least understand what's the anticipated amount of money that we are collecting from each location and whether it arrived to our bank account or not.  
So expected versus factual.

**Pavel Frolov** 23:05  
Um.

**Val Levitan** 23:06  
How do we, how do we achieve that?

**Pavel Frolov** 23:14  
I'm not ready to answer right now. I since I understand that it will be some API from our control server to get accounting data and to get some reports.  
But how it can be shared with third party? I mean, if we need to share this data with Incom or with ACH, I don't know. And actually it can depend on ACH. Yeah, it's not.

**Val Levitan** 23:46  
But that's not it's not only income and the ACH, it's income, ACH, upper relocation and internal.

**Pavel Frolov** 23:53  
Thank.

**Val Levitan** 23:58  
One of the most critical reports is, let's say for me, I would like to know what is that I'm supposed to collect and what has physically arrived into my account.

**Pavel Frolov** 24:05  
Mhm.  
Actually I think this is the simplest point because we we will just develop some API to get reports and data and to store them on our database as.  
As it is implemented right now with the option to produce OLAP on OLAP server reports and can be treated as currently produced reports.  
Probably it's simplest part.

**Val Levitan** 24:50  
How do you when when you develop a back end architecture? I assume that the back end architecture largely consists of a bunch of tables with informations and various databases.

**Pavel Frolov** 25:05  
Yes.

**Val Levitan** 25:06  
And various fields need to be integrated with one another, but just understanding what information needs to be retained. How do we get that maximum number of fields that need to be retained? Is it something that is trivial?  
The back end designers, they already know it or where do we get it from?

**Pavel Frolov** 25:33  
Hmm.

**Nathan Carver** 25:33  
So a lot of that can be driven by the requirements that we place on the system. So if we define when it comes to ACH and having and ensuring that we can reconcile, reconcile every activation.  
Within a given day to an ACH draw on the location.  
We define the requirements from a reporting perspective or a status perspective of the current state and that will help. That will help the engineers.  
Determine what fields they need to save. I think there's also nonfunctional requirements. Intuitively, they're gonna know what fields they need to save just to have the system operate. So I think there's gonna be a combination of getting requirements that define it and then the engineers.  
Determine the nonfunctional data that they'll be storing.

**Val Levitan** 26:30  
Is this where we over design?  
Because I just don't understand how to get. I understand that you're saying well we have requirements we could design the tables and fields and but I'm I'm afraid that we do not know all of the requirements. This right now we're focused on MB PS.  
So we're not even thinking about a number of requirements. So how do we ensure that we take into consideration everything that we know now and that we don't know, but most likely we're missing?

**Nathan Carver** 27:12  
So I think so the approach will be that we we document what we know now and what we need for the MVP. The system will would be designed in a way that allows it to evolve and take on new requirements in the future.  
And that's Pavel's approach of having componentized services as he's, you know, he's talking about modules. All this modulization enables the system to grow with more flexibility in the future as we do add more.  
More requirements. The database can expand as new fields are needed and new new data storage is is needed or new requirements are needed to create new new data that needs to be persisted.  
Um. So we do. We do have a a balance of define what we need for Mvp, and also enable the system to expand and grow in the future with the new requirements.  
And we do have an idea of where we're going. So the the the team can architect the system in a way, which I think is what Pavel's doing is he knows the direction we're going, so the system can be designed with that flexibility in mind.

**Pavel Frolov** 28:33  
Yeah, I would. I would add some probably in my understanding what can be written as a requirement right now because we understand how it should work.  
All cards that were redeemed by Payment Hub. You definitely know the time, from what location it was requested, all the fields that we required that we sent to.  
Incom, so everything can be written into the table into database and this data can be then retrieved by JVL first of all.  
And highly likely we will transfer. We'll be able to transfer this data for assigned operator by the request.  
Of course, when we know how ACH is communicating to our service, then we will add more.  
Data because I think on each request from ACH we will need to make some some validation or some records to our database.  
But again, as a first dimension here it it will be just information related to redeemed card. This is more most important information that need for all parties.

**Val Levitan** 30:39  
So we're saying we are going to build our.  
Tables and.  
Uh, database so.  
I guess volume or fields based on income.  
Uh API for now.

**Pavel Frolov** 31:07  
Not not only income and API, but also a relationship between this request to income API to particular location to particular terminal, particular flex POS.

**Val Levitan** 31:07  
Yeah.

**Pavel Frolov** 31:24  
It will be assigned to each other.

**Val Levitan** 31:28  
But that would be missing JBL's requirements. Like what income doesn't really care about a set of business.  
Business transactions that you know they're not involved in, we would have to collect cash, we would have to ensure that.  
Cash fully reconciles with every transaction. I don't think income really cares about it.

**Pavel Frolov** 32:09  
Yes, you're right.

**Val Levitan** 32:10  
So how do we ensure that we?  
Satisfied all of JVL's requirements.  
And and and we are new in this business, many we don't even understand yet.

**Pavel Frolov** 32:33  
Mhm.

**Nathan Carver** 32:34  
So we we start with what we have, what we know, our use cases that we have, the problems that we have to solve, and then we iterate on those. So the system will evolve iteratively as we discover.  
And understand requirements as we go.

**Val Levitan** 32:54  
But can the back office?  
Can this I I don't know how to call this nucleus of you know bunch of tables and relationships in in the back end that needs to get.  
Born before all the outside things are connected to it. I I I don't know what the architectural name for it, but logically thinking about it, everything that goes inside of it, we don't know what really needs to be retained.  
O How do we form it?  
I'm sorry I'm not using proper engineering names.

**Pavel Frolov** 33:37  
Yeah, during during the development, especially when the database is used, usually architecture architect presenting.

**Nathan Carver** 33:37  
So.

**Pavel Frolov** 33:53  
Database schema that describes a relationship between different tables, different communications and what will be stored.

**Val Levitan** 34:06  
And when they present it, which I assume is the beginning of the architectural design, they will probably point to us and say, is there anything else? Are we missing anything? So how are we going to reply to that?

**Pavel Frolov** 34:35  
Of course, we will not be able to produce such schema.  
Without some requirements that relates to JVL requirement. JVL requirement means some reconciliation with ACH, with in comb without understanding how it will be work. It will not be created in schema.  
Love you.  
Mhm.

**Val Levitan** 35:09  
So if it's not fully created and we went ahead and implemented the, let's call it the MVP design on January 1st and then we say, oh ****, we should have done this and we forgot that and we missed this and here's a bunch of other things that we missed.  
So come next reiteration of it, does it mean that we have to change the nucleus?  
Again, I don't know what the name for it is.

**Pavel Frolov** 35:39  
No, I think it's quite independent from each other. Actually. In any case, we need to implement income communication during the redemption process, it looks like.

**Nathan Carver** 35:40  
The.

**Pavel Frolov** 35:55  
As an independent procedure.  
Then next procedure probably will be some checkpoint between third party ACH.  
And mine is at ACH.  
Go from particular location and get this data. I don't know something like this and according to this workflow we will need to develop.  
Other database schema that will reproduce this amount of money that we we are getting from ACH.

**Nathan Carver** 36:49  
When it comes to, if we're asked by the team, you know, is there anything else or or? And then we realize we missed something. We deploy the MVP, we realized there's new requirements that we missed that we have to add.  
The persistence of new data, tracking new services, the nature of the design. The architecture is designed in a way that these modules are specialized in what they do, so these changes will take place inside.  
The module and that reduces the impact it has across the whole system. So even if there was something drastic, which I don't see happening, but if there was something drastic to the point where we had to rewrite.  
A complete a component completely. Those components should be relatively small compared to the holistic system, so it's still not a. It's still not a huge risk to us to have to rewrite small sections of the of the.  
The system to support new.  
New features that we just didn't account for in in the design.

**Val Levitan** 38:03  
That's a that's a good point. I guess part of our approach or or I guess our work order to the back end team should be that each component is not more than a particular size.

**Nathan Carver** 38:22  
Correct. And that's what we're seeing in the architecture presented here is we have the payment hub as a module, but then in that payment hub we have 3 components that are gonna be, you know, smaller pieces of that payment hub.

**Val Levitan** 38:37  
OK, OK. OK. OK.  
OK, clear. I would like to wrap up this meeting with the next 15 minutes or earlier. What I would like to propose is maybe a 2 minute pause and I would like Pavel and Nathan to eloquently.  
Set out.  
The undertakings and the schedule.  
With definitives, definitive.  
Checkpoints for let's say two weeks I would like to meet every.  
The longest maybe a week, every week, but I prefer earlier if there is something to look at or discuss. So let's take two-minute pause just to focus. I need the.  
Concise undertaking and schedule for the next two weeks.  
Aaron, if you have anything to add.

**Aaron Bockelie** 39:49  
No.

**Val Levitan** 41:46  
Yeah.  
OK, when can we meet next and what's undertake? What's our undertaking? And let's just lay it out the schedule for two weeks. Who wants to go first?

**Nathan Carver** 43:33  
Um, so if we wanna set up the next meeting to be.  
Let's see next week, Wednesday the 24th.  
Um.  
The focus is going to be on the use cases that drive requirements for payment hub API. So that's going to be examples would be use cases around ticket redemption, use cases around location owner.  
Reconciliation.  
And and any potential JBL reconciliation or auditing?  
So that could be the focus for the first week iteration and once we get through the use cases and that really focus on payment hub, then shift into use cases around device provisioning, setup, device management.

**Val Levitan** 44:40  
OK.

**Pavel Frolov** 44:42  
So.  
I see next outcome for two weeks period to get architecture and specification for payment hub.  
Including API Payment Hub Terminal and API Payment Hub Control Server.  
Then I I think we will need a database schema.  
For income transactions from the terminal and database schema for terminal setup parameters related to payment hub.  
Actually this this database schema is part of specification for payment hub.

**Val Levitan** 45:41  
I don't want to wait two weeks until our next meeting. Is there anything that could be discussed a week from now?

**Pavel Frolov** 45:45  
Yes.  
Um.  
Probably, probably some next approach to architecture design describe in more details about payment hub in the week, yeah.  
Can be can be interviewed.

**Val Levitan** 46:23  
I would like, I would like to, I would like to discuss the specification for specification. What will be in specification? Let's agree on that. I think this is most important thing.  
Can we do that?

**Pavel Frolov** 46:42  
OK.

**Val Levitan** 46:45  
So what do we need to?  
Aaron, you brought to my attention a couple of standards for writing specifications. Can you remind me what it was?

**Aaron Bockelie** 47:00  
Right. Uh.  
I didn't have. I gotta remember where I put it.

**Val Levitan** 47:09  
What do we need to think about when we write specification? Pavel and I also discussed that there.  
I wish I was a little more prepared for this conversation.

**Aaron Bockelie** 47:23  
It's a bit of a pivot. So the idea is, is that.  
You should be starting somewhere from almost the definition of what is an acceptable spec for your software, for the tools, for the product, whatever that might be, and realistically it's choosing a number of different aspects that describe.  
You know, how are you trying to describe everything here? So.  
There is an entire.  
Profession of writing specifications depending on what you're looking for, where you have different forms of design, architectural design aspects to software to. I'm actually drawing a blank right now on the on the name of the.  
Uh, there's an open specification style for this. Um.  
Let me just Google it really quick.

**Val Levitan** 48:41  
I actually have it in my recording. I could dig it up.

**Aaron Bockelie** 48:46  
TOGAF, that's what I was thinking of. So I mean, if you wanted to start at at the big at the bottom basement level, TOGAF is an open. The open group is what that stands for, is how you define architecture and there's a whole set of standards that go about.  
But The thing is, is that.  
It's not a match for JVL's organization right now, so you're going to need to kind of come up with the more informal, smaller approach to this that engineers can sort of think about.  
And Archimate, for example, is a piece of software that Togaf promotes. It's been around for forever. It's actually like if you ever heard of plant UML and all these other things, that's where this comes from.  
And.  
Realistically, I think what we've talked about, Val, was a distillation of some of that into right. So we got ISO specifications for defining requirements for defining specs. These all sort of interrelate with each other.  
So I think that my goal was when we talked last is we need to come up with an inspired interpretation of these. You're not trying to become an ISO certified company, which you would have to accommodate this if you were.

**Pavel Frolov** 50:30  
3.

**Aaron Bockelie** 50:31  
C.

**Val Levitan** 50:31  
Yes, I would like to have some sort of an internal agreement what we consider to be a specification.  
I actually have a pretty good recording on this. I'm going to dig it up and I'm going to try to circulate this with Pavel and align myself with him for the next meeting.  
And hopefully have it reviewed in about a week, so tentatively for Monday.

**Aaron Bockelie** 51:05  
I can say with certainty that trying to take the more formal ISO or open group approach of defining architectural and standards requirements will not allow you to hit that January 1st deadline you'll be spinning.

**Pavel Frolov** 51:20  
Yeah.

**Aaron Bockelie** 51:21  
Months writing all of the specs to do this, so it's not like you're doing that.

**Val Levitan** 51:22  
Yeah, yeah, yeah, yeah, yeah, yeah. No, no, no, for sure. Yeah, yeah, yeah. It has to be. All I'm trying to do is just to have an internal document on what we all agree to be a specification of specifications. That's, that's, that's all it is.

**Pavel Frolov** 51:28  
Yes.

**Aaron Bockelie** 51:41  
Yeah.

**Val Levitan** 51:44  
OK, so I think the undertakings are clear. Nathan, we'll have a meeting on Wednesday and Pavel most likely will have a meeting on Monday.

**Pavel Frolov** 51:57  
OK.

**Val Levitan** 51:58  
OK.  
Thank you very much.

**Nathan Carver** 52:01  
The Wednesday the the 24th.

**Pavel Frolov** 52:02  
Yeah. Thank you.

**Aaron Bockelie** 52:02  
Right.

**Val Levitan** 52:04  
Wednesday the 24th, I'll send the invites to everyone.

**Nathan Carver** 52:07  
OK, perfect.

**Pavel Frolov** 52:08  
Yeah.

**Val Levitan** 52:09  
Thank you.

**Nathan Carver** 52:11  
Thanks everyone.

**Aaron Bockelie** 52:11  
Thanks. Bye.

**Pavel Frolov** 52:11  
Right.

**Val Levitan** stopped transcription