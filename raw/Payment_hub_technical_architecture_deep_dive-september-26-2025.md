**Transcript**

26 September 2025, 12:04pm

**Val Levitan** started transcription

**Val Levitan** 0:03  
Payment Hub Technical Architecture.  
Lecture.  
I would like this meeting to be productive.  
And so if we're not ready for it, let's just say what we don't know, identify what we know.  
Discuss what we know and then create.  
A set of undertakings to find out what we don't know and that in my view is the productive is a productive part of the meeting today. I also suggest if we know and if we know how we will approach this.  
Subject and that piece of work that we start laying it out in the form of a schedule in Jira plans. So we kind of see the track of how we're going to get there.

**Pavel Frolov** 1:02  
Yes.

**Val Levitan** 1:02  
The discussion is between the two engineers, between you, Nathan and you, Pavel.  
I am a facilitator. I'm here to.  
Maybe poke business holes in your assumptions, but it's not my conversation. I cannot lead architecture of a design.  
Do you? If you like this approach, let's do it. If not, propose something else. This is first meeting of this sort, so if you think that it should be handled somehow differently, I'm OK with that.

**Nathan Carver** 1:28  
OK.

**Val Levitan** 1:45  
I am not an expert on it, I'm just getting my toes wet.

**Nathan Carver** 1:52  
OK, that makes sense.  
I guess to start then, Pavel, do you have a a start on this and a source of documentation that you've been working on?

**Pavel Frolov** 2:05  
Uh, yes, actually.  
We already have some documents described in the payment hub.  
Let's see.  
Open this and share a link with you.

**Nathan Carver** 2:39  
OK.  
OK.  
All right, cool. Um, OK.

**Pavel Frolov** 3:23  
Yeah.

**Nathan Carver** 3:24  
Um.

**Pavel Frolov** 3:24  
So actually actually I can share a screen and start probably from this document.

**Nathan Carver** 3:31  
Yeah, let's let's do that.

**Pavel Frolov** 3:34  
This is a product vision.  
So we assume that payment hub is serious.  
Uh, run on the cloud server.  
And it should support authentication and credential management.  
It's a capability, I assume.  
Uh, unified channel for income API interactions.  
It should communicate securely and with high reliability.  
And it should be open for frozen expansion. This means it can be easily add more servers in different regions.  
From one hand and from the other hand, it should be organised well structured to be able to add new modules, for example for third party ACH communications, third party.  
Account management system like income and so on.  
This is a general, I would say.  
Business requirement probably.

**Nathan Carver** 5:12  
OK, OK, yeah, this makes sense.

**Pavel Frolov** 5:23  
So actually here is goals of this project. You can review it if you if you need.  
So the the main goal is to avoid direct communication from terminal to.

**Nathan Carver** 5:45  
Correct, yeah.

**Pavel Frolov** 5:45  
Uh, API, yeah.  
Expanded security too.  
Actually I think we need to to add here.  
Uh.  
Some relationship with ACH because it's currently not listed here.

**Val Levitan** 6:15  
OK.

**Nathan Carver** 6:21  
Yep, so some type of ACH.  
Processing I did a document.  
For Payment Hub, just really just focused on select POS requirements.  
And thinking through that, it might be like some type of worker service or work queue that we use to process each of the locations.  
Uh ACH so believe it's I believe the Azure.  
An example of that in Azure is like a um.  
I think it's called. Yeah, this is here. It says settlement service, but I thought there was another name for.  
Yeah, that may not be what we want, but that's one of the recommendations. So anyway, some type of worker queue that we can queue up all of our locations and you know, process some of them sequential in parallel.  
Our batch processing, we can do that in parallel.

**Pavel Frolov** 7:58  
OK, if we switch to system architecture.  
Oh, probably it's better to take a look on some.  
Graphically implemented.  
So in general, if we take a look from.  
Top level. So we need to support communications with different types of terminals like Flex POS, Flex pay and others so.  
At least we need some core processing module that supports API communication between terminals. It needs it requires.  
Modules that communicates to income and supports income API.  
And now we understand that we need communications between the main core module and our control server control server.

**Nathan Carver** 9:36  
Mhm.

**Pavel Frolov** 9:36  
Uh.  
Actually this is a CMS server right now.  
And the purpose of having this communication to be able to use our well known architecture and well known a tool for set up machines, set up remote initial.  
Setups and be able to create parameter set.  
That can be pushed or transferred to particular.  
Terminal from one side and from the other side to be able to feed our a payment hub with all the information related to terminals, locations, credentials.  
Uh, so um.  
When the control server shared the data related to different terminal payment hub will be able to.  
Either support communication between terminal and and.  
Incom server to issue card or prohibit such communications. This is a purpose of control server integration and.

**Val Levitan** 11:15  
Sorry if we were going to.  
Go ahead.

**Pavel Frolov** 11:20  
OK, just to to cover the last module. So we are going to to have a database and also modules that logs all the transactions.  
Some issues related to communications. That's all I think in general it's quite simple architecture.

**Nathan Carver** 11:49  
Mhm.

**Val Levitan** 11:50  
So if we were gonna, if, if we're going with this architecture, hypothetically speaking, and we want to install machines in January.  
How would we layer it and how would we design it with an ability to run 1st 10 installations in January? What would it look like?

**Pavel Frolov** 12:18  
First of all, to implement communications between terminal and payment hub.  
Second one, implement communication module between payment hub and.  
Incom.

**Nathan Carver** 12:38  
Mhm.

**Pavel Frolov** 12:39  
Oh.  
The next one communication between control server and payment hub. So at this moment I think this is a minimal.  
Minimal set of features that can can be implemented until I would say November or mid November.

**Val Levitan** 13:11  
No, but we also need an API between a payment hub.  
And and ACH provider.

**Pavel Frolov** 13:26  
So this is I I think this is not a minimal. This is an additional to main mainly implemented features.

**Val Levitan** 13:39  
If we don't have.  
Uh.  
Well, OK. So this is a good discussion. I'm, I'm glad that we're on it. I think it should be minimal because without that I don't want to go into the field.  
I don't believe that we have a viable business model if we don't have an ACH provider.

**Pavel Frolov** 14:06  
I I think so. I agree with you, but.

**Val Levitan** 14:11  
So that means that means it. That means it has to be a minimum viable feature.

**Pavel Frolov** 14:15  
Yes.  
So when when I said about minimal set of features until mid of November.  
This is MVP for November. Then we can set MVP for January 1st and we can include ACH to this MVP list.

**Val Levitan** 14:47  
OK. So let's just discuss January 1st because November is not really a rollout period. We're not going to do, we're we're not going to get there in November because we don't even have the hardware to support it.  
So it has to be January and it has to include the ACH valid transaction.

**Pavel Frolov** 15:09  
Not exactly. Well, you're saying we we will not have a hardware to support this. I think we can.  
Around first test starting from November.  
Using our Flex Pay, we will need to modify Flex Pay to also support communication via payment hub and we will be able to do this November.

**Val Levitan** 15:42  
I'm not quite sure what exactly.  
Oh.  
I cannot visualize it, but maybe you're right, I don't know. But the business model that we're trying to roll out is not a flex pay, but a flex POS.  
I do not envision flex pay in the first.  
In the first rollout. So unless you're using it for testing of some sort internally, which I don't mind, but you could internally test any PC. It doesn't have to be here.  
Uh, flex space. So I do not quite visualize this.  
But I do see.  
I have a visual on January where we have a POS.  
Hardware made in temporary plastics.  
Printed printed plastic bodies.  
And we have the initial hardware that is functioning and we would want to have initial cloud architecture that is functioning at A at an MVP level and this is what I'm trying to visualize and.  
To architect that solution which can be scalable from there and on.  
And so I'm asking for minimum viable features for that architectural solution.  
That could transition and evolve into a full blown architecture, full blown model.

**Pavel Frolov** 17:39  
Mhm.  
OK, actually.  
I just need to add here just an ACH.  
Integration.  
Actually it will show the architecture of minimal viable product for January, including ACH service.

**Nathan Carver** 18:12  
I think there's probably a component of the ACH that lets us that does the processing, the daily processing of.  
The tickets to basically aggregating the value of the tickets and then propping the the jobs for the ACH transfer.  
Initiating that. And then there's a whole tracking of that. Um.  
The status of that transaction. So I think a daily job is going to be.  
Initiate new transactions to reconcile what's OJVL and then go and get status on any existing ACH transactions.  
And update that in our system.  
So it might just be two components. There's like some type of batch processing component and then uh, a communication component.  
For ACH.  
And then the if should we decide to switch ACH providers, I think the processing component doesn't really change. It would just be that communication adapter. We could adapt a different ACH provider if we wanted.

**Val Levitan** 19:22  
Yep.

**Nathan Carver** 19:32  
With ideally minimal, just replacing that component with a new adapter.

**Val Levitan** 21:06  
Yeah, we're gonna have more radio.

**Pavel Frolov** 22:00  
Something like this, just adding ACH processing with his adapter.

**Nathan Carver** 22:06  
Yep.  
Yeah, exactly.

**Pavel Frolov** 22:20  
See.  
Actually, under the system architecture, there's some.  
Some description related to core processing module.  
Described some communication to terminals validation.  
Here description to income integration module.  
To control server. So I see that next step to discuss in the probably next week to add here an ACH.  
Necessary module and describe communication related not only communication but also logic related to ACH.  
Yeah.  
OK.  
Yes.

**Val Levitan** 29:08  
So I I.  
How much more do you need to change? I I'm just I lost track a little bit.

**Pavel Frolov** 29:17  
I need to go through the documentation to payment hub to add ACH integration module.

**Val Levitan** 29:33  
But in terms of block diagram, the the architectural diagram that you.

**Pavel Frolov** 29:34  
Oh.  
Actually I already seems that in general I already updated, just added the additional module.

**Val Levitan** 29:45  
OK. OK. OK. So we have another 20 minutes or so. I would like to then.  
Divert our attention to the scheduler and to layout the main feature features in the schedule of what we need to implement so we can now start moving the the time is running out very quickly.

**Pavel Frolov** 30:02  
Mhm.  
Yes.  
Yes.

**Val Levitan** 30:14  
So let's identify the features that we need to put into work and.  
I renamed the IP744 instead of payment solution. I put it into made it the transaction solution.  
744.

**Pavel Frolov** 30:52  
Mhm.

**Val Levitan** 30:55  
OK, under there is a payment hub and under payment hub we want to list the features and to take them into work.  
So for we we agreed that we need the integration with ACH provider, we need integration with payment hub between the POS and the payment hub.  
And we need integration between the payment hub and the income.  
We should clearly identify this.  
Under the IP632.

**Nathan Carver** 31:42  
Mm-hmm.

**Pavel Frolov** 31:52  
Uh.

**Val Levitan** 32:50  
ACH processing adapter probably doesn't sound right or we it just doesn't read right to me.  
The problem needs to say.

**Nathan Carver** 33:01  
Be a API adapter. We would have like a ACH API adapter and.  
An ACH.  
Like a a job processor or our processing module that the module, the processing module would handle the daily batch jobs and then the adapter allows us to switch.  
Providers in the future.

**Val Levitan** 33:38  
That's that's a good description. Can you add, Nathan, can you go back and add the description there? Pavel, can you save it?

**Pavel Frolov** 33:46  
So you're saying that we need two separate features, one to implement logic for ACH communication and the 2nd to implement particular APA adapter related to ACH third party.

**Nathan Carver** 33:47  
Yeah.

**Val Levitan** 33:48  
It was late.

**Pavel Frolov** 34:05  
That we select at this moment.

**Nathan Carver** 34:06  
Correct, correct. Yeah. One does all the processing for us, understands JVL's business needs.  
And then the adater is just a smaller component that allows us to communicate with a specific provider.  
Um, translating.  
Now translating that communication so.  
For example, if we started with Duwalla, we would have an ACH Duwalla API adapter. That would be like the implementation of it and then we switch to, I don't know, Tabupe, we would just create a new ACH API Tabupe adapter and then.  
Um.  
Insectually, we can switch back and forth between the two at that point or just replace the dualo one completely.  
Yeah, as an example of that, yeah, it would just be a placeholder ACH API adapter.  
The the payment hub communication to ACH that might um be the same thing as the adapter. I'm thinking through that that naming.  
This might be the component that.  
Um.  
I think we've been calling it reconciliation component, so.

**Pavel Frolov** 36:31  
Reconciliation component. Mm-hmm.

**Nathan Carver** 36:35  
Yeah, this is what reconciles. So the job of this, the responsibility would be.  
For all the locations, each location, it looks at outstanding tickets to be reconciled with JVL.  
Determines the amount, creates the the batch record the transaction.  
And then um sends that the location and the dollar amount through the ACH adapter.  
Which translates that into an ACH request with the provider.  
So this reconciler would be aware of that it's moving money, but it doesn't care if it's through an ACH transaction or I don't know, there's several transaction options.  
Um, so we would abstract it away a little bit from the ACH, but it knows that it's moving money between JVL and the location.

**Pavel Frolov** 38:10  
So in in short, I write in the description using third party ACH sync to reconcile money transactions between GL location and income.

**Nathan Carver** 38:17  
Mhm.  
OK. Yeah.  
I think that's good. Well, we'll need to. We can break it down into its smaller components.

**Val Levitan** 38:57  
Yeah.

**Pavel Frolov** 40:25  
Very likely cancellation module will be.  
Before the ECH adapter.  
'Cause this adapter actually relates to particular API implementation for third party ACH.

**Nathan Carver** 40:47  
Yep.

**Pavel Frolov** 40:48  
I said like this.

**Nathan Carver** 41:16  
Yeah.

**Pavel Frolov** 41:40  
OK.  
This moment I think this is a quite a rough.  
Top view on the entire project, but next I think I I will need to discuss in more details with our developers and try to split it into smaller parts.  
Probably produce a better estimations to this.

**Val Levitan** 42:13  
Fantastic. Absolutely fantastic. Fantastic. Nathan.

**Nathan Carver** 42:20  
Yes.

**Val Levitan** 42:23  
So these features we now want descriptions.  
Uh, we want to tie them to requirements.  
And we want to start writing spec together with paddle. But your your your main thing, Nathan, yours is which the requirements into this.

**Pavel Frolov** 42:40  
OK.  
Actually.

**Nathan Carver** 42:47  
Nathan.

**Pavel Frolov** 42:51  
Actually Nathan, you can take a look on the first three features because we already made description and also we already added some and linked some requirements you can.  
Just review, probably add more requirements here.

**Val Levitan** 43:17  
So just let let's just be clear what we're trying to achieve. We're trying to link the requirements. We're trying to create a very tight spec as much as we can. It will be evolving and we're trying to bring QA to write tests for it.

**Nathan Carver** 43:17  
OK.

**Val Levitan** 43:35  
Integration test.  
It's not gonna work.  
But we will discover what needs to be done. We just need to start taste, tasting and smelling.

**Nathan Carver** 43:51  
Yep, yes, sounds good.

**Val Levitan** 43:51  
Agreed.  
OK, so your undertaking, Nathan, is to link it to requirements and you and pavel need to start describing spec pavel. You need to bring at least one.  
A tester to start coding tests.  
Torrent.

**Pavel Frolov** 44:18  
Mhm.

**Val Levitan** 44:18  
So we can start discovering issues that will come up with it because there will be issues we we just we've never done it before. So we don't know what what we will uncover.  
Uh, let's have a let's have another meeting on Wednesday.

**Pavel Frolov** 44:30  
Mhm.  
OK.

**Val Levitan** 44:36  
Wednesday, Thursday, whenever, whenever your schedule allows, you tell me.

**Nathan Carver** 44:42  
Let's do let's do Thursday since we have a Wednesday flex POS focus discussion. Unless we feel that this will take precedence, then we can.

**Val Levitan** 44:55  
No, Thursday it is. No, Thursday it is good.

**Nathan Carver** 44:56  
Just focus on that.  
OK.

**Val Levitan** 45:01  
Thank you very much. This was extremely productive. I encourage you to work together until Thursday because on Thursday I want it to be a productive meeting, productive for the Thursday meeting.

**Pavel Frolov** 45:03  
Mhm.  
OK.  
Yes.

**Val Levitan** 45:16  
Is to see the mapped out.  
Uh, links between the features.  
That we're seeing here and the set of requirements and a birth of specification.  
Agreed. Good objective.

**Pavel Frolov** 45:35  
OK, yes.

**Nathan Carver** 45:36  
All right, sounds good. Pavel, I'll go through the the links you just showed me and I'll look at those requirements and how you all are building them out. And then are you also using GitHub to to churn and create them and then move them into JIRA?  
Or just using them in JIRA?

**Pavel Frolov** 45:53  
Um, actually yesterday we started, I would say experiment.

**Nathan Carver** 45:56  
Um.

**Pavel Frolov** 46:01  
To describe features and requirements here in GitHub in Jira, but we started creating tasks in GitHub related to particular this project.

**Nathan Carver** 46:11  
OK.  
OK.  
If I create some uh diagrams, do you want me to put them in GitHub in this project specifically? Um.

**Pavel Frolov** 46:30  
Yes, yes, yes, please.

**Nathan Carver** 46:32  
OK.  
OK, then I'll probably.

**Pavel Frolov** 46:34  
Because actually I don't. I don't like what is mermaid producing for diagramming. It's not very.

**Nathan Carver** 46:47  
Yeah, it's hard to. It's hard to control very complex diagrams. I agree.

**Pavel Frolov** 46:48  
Uh, useful I think.  
Mhm.

**Nathan Carver** 46:55  
OK.

**Pavel Frolov** 46:55  
So probably we just need to make smaller pieces on top level to see a graph diagram and then each module to to show its own structure and so on.

**Nathan Carver** 47:10  
OK, sounds good.

**Val Levitan** 47:13  
Fantastic, boys. Thank you very much. I love what I see. We're making progress. Thank you. Bye, bye.

**Pavel Frolov** 47:15  
OK.

**Nathan Carver** 47:18  
OK, great. Thanks everyone.

**Val Levitan** stopped transcription