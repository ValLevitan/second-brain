**Requirements\_Payment\_Hub\_Operators\_Dashboard\_Front\_end-July-7-2026-20260707\_170154-Meeting Recording**

7 July 2026, 09:01pm

13m 3s

**  
Val Levitan** started transcription

**  
Val Levitan** 0:06  
I just turned on the recording. I apologize. Can you please repeat that again, please?

**  
Andrei Klimovich** 0:09  
Yeah.  
Yeah, so I'm currently I'm currently working on requirements for operational dashboard operator role and I've covered.

**  
Val Levitan** 0:12  
Thank you.

**  
Andrei Klimovich** 0:21  
almost all of them, only 5 requirements left. And my plan is to finalize them tomorrow by the midday. And if so...  
We have a really solid base for developers to start working on this functionality. My next step will be to create a prototype for JVL view, JVL role of the same dashboard, and convert it into requirements. So, as far as I see...  
JVL rule.  
contains a lot of functionality that is already in there for operator plus unique functionality. So I really...  
I will do my best to finalize it by Friday evening.  
And when I say finalize, it will include a prototype and requirements for most of functionality. So my goal is before I go to Georgia, development team will have all the required information and prototype HTML.  
A markup for the whole operational dashboard we currently see that we currently see for MVP.  
So this is my goal and it goes well. There are some tricky parts, but nothing unresolvable.

**  
Val Levitan** 1:59  
That sounds very good to me.

**  
Andrei Klimovich** 2:02  
So for the next week, again, like my major focus will be on testing IQ, running as much.  
tests and providing feedback back to the team as much as possible so we polish it in real time. I would expect them to provide updates on a daily basis. So day one I do the test, I send my feedback requirements or...  
defects, whatever, and the next day I would expect them to get an updated version. So I test it and I continue with other tests. So that's where we can utilize our time difference. So if by the end of today I send them my...  
Comments they will use, they will use, yeah.

**  
Val Levitan** 2:54  
Well...  
Let's change slightly.  
Um...  
Because, whenever developers triggers trigger any work.  
I have to see it in Jira. And that's why it's one of the reasons why I don't like.  
Ohh.  
When I'm not involved.  
And so, because we are accelerating this pace, and most likely we'll be missing a lot of things.

**  
Andrei Klimovich** 3:21  
Yeah.

**  
Val Levitan** 3:29  
Let's make sure that...  
Whatever is discussed.  
is in Jira. If it's not in Jira, that means it's not done.

**  
Andrei Klimovich** 3:41  
Yeah, for sure. Just to be sure, like we currently don't have a specific type of ticket for defects, right? So.

**  
Val Levitan** 3:50  
We don't, we don't schedule defects and it shouldn't find itself injured.  
It's only scheduled work that is in Jira.

**  
Andrei Klimovich** 4:01  
Yeah, so if something needs to be done, it goes like a requirement, as a requirement.

**  
Val Levitan** 4:08  
No, it has to go against the capability.  
not against the requirement. So a capability is a second level in the hierarchy.

**  
Andrei Klimovich** 4:12  
Yeah.

**  
Val Levitan** 4:20  
First is initiative.  
Then, right after the initiative is capability.  
Capability opens up the scope of work.

**  
Andrei Klimovich** 4:30  
Mhm.

**  
Val Levitan** 4:31  
which is measured.  
For developer is measured in features.

**  
Andrei Klimovich** 4:43  
So let me provide you with an example of a real life example. Right now, when a customer, a player...

**  
Val Levitan** 4:51  
IN.

**  
Andrei Klimovich** 4:53  
gets a debit card, he can request a receipt to be sent to his e-mail. And we are sending some e-mail right now, but it doesn't look good. And I would love it to be redesigned to use proper wording, to use proper fields.  
Et cetera, so...  
To me, it sounds like an improvement, right? So the feature itself, send an e-mail, is implemented and it works properly, but the content is not appropriate. So...  
My step is to find the proper capability where this logic is described, which says that player should get error.  
Receipt for every transaction, blah blah blah.  
And inside of this capability, I should create a requirement which will tell how the e-mail should look like. No, okay.

**  
Val Levitan** 5:59  
So, a capability lives in the form of hierarchy.  
A requirement and a capability closes.  
It does not live, it does not survive.  
And it never reopens.

**  
Andrei Klimovich** 6:19  
Mmh.

**  
Val Levitan** 6:21  
So.  
What you will do, you will open capability refinement.

**  
Andrei Klimovich** 6:28  
Okay.

**  
Val Levitan** 6:29  
And you will link the requirements. The requirement live in the form of a project. It's a...  
It's a type of a project, REQ.  
So, you will connect, and requirements always survive.  
The requirements have acceptance criteria in it.  
The requirements are reusable.  
They're single.  
They're simple, single.  
They survive.  
They're reusable.  
So when you open the capability refinement,  
Then you will link all of the requirements that you want within that capability refinement, including the old ones.  
Because we reuse acceptance criteria.  
Into that capability refinement.  
And capability lives.  
as a second level of hierarchy under initiative.

**  
Andrei Klimovich** 7:43  
Okay, so do I understand it correctly that for initiative?  
There should be should be one initiative per product, so if we're talking about IQ.

**  
Val Levitan** 7:54  
No, initiative is higher than the product. We're eliminating product. The product level disappears.

**  
Andrei Klimovich** 7:58  
Mhm.  
Mhm.

**  
Val Levitan** 8:04  
Initiative survives, initiative is to say transactional equipment.

**  
Andrei Klimovich** 8:11  
Mhm.

**  
Val Levitan** 8:13  
And under it, there is a capability. The capability belongs to a project. The project is called Flex IQ.  
And under Project Flex IQ, which is the second level of initiative, transactional.

**  
Andrei Klimovich** 8:24  
And.

**  
Val Levitan** 8:33  
You'll open capabilities.  
all the capabilities that you will be opening under FlexIQ project.  
will have requirements that are not under project, just loose items.

**  
Andrei Klimovich** 8:59  
So.  
Let's take an example. Here's our capability.  
one of them and it leaves on the product capability.  
Space.  
And as far as I see a capability as an item, it has no...  
It has no link to a project, so, or...

**  
Val Levitan** 9:28  
You're looking at capability. What you should be looking at is plans.  
On the left-hand side.  
Up, up, up.  
Plants.  
Portfolio view.  
Transactional.  
Okay, so in here, under transactional, this is a value stream.

**  
Andrei Klimovich** 10:16  
Mhm.

**  
Val Levitan** 10:18  
Let's say open Flex Recycler.  
See all the capabilities for the recycler.  
I don't have time right now to go into it, but if you, if you want to understand it, we're writing, as a matter of fact, we're writing standards right now, and...

**  
Andrei Klimovich** 10:32  
Yeah, yeah, sure.

**  
Val Levitan** 10:41  
Dmitri Kovalchuk.  
Know the subject very well.  
We developed the standards together with him. So I suggest that you speak to him about it.

**  
Andrei Klimovich** 10:55  
So IP is initiative.

**  
Val Levitan** 10:58  
An an IP is initiative.

**  
Andrei Klimovich** 11:00  
Okay.  
Okay, I got it. So basically we don't have initiative called Recycle, right? And oh, sorry, IQ.

**  
Val Levitan** 11:10  
We don't have, I mean, look, we're in transitional period where we're changing from one structure to the next. I didn't go into the old structure, I'm giving you the new structure right away.

**  
Andrei Klimovich** 11:15  
Mhm.  
Yeah, yeah, okay.

**  
Val Levitan** 11:25  
But the new structure will have an IP, then you will have capability, and capability will belong to a particular project. So FlexIQ is a project.  
The initiative is something higher.

**  
Andrei Klimovich** 11:47  
Yeah, okay, so I'll figure it out.  
So my focus for the next couple of days is just to finalize everything related to Operation Dashboard, pass it to developers to make sure they have it. And starting with the next week, I'm in Georgia and I will focus on testing, creating improvement defects, everything should be reported, everything should exist in Jira.

**  
Val Levitan** 12:12  
Hello.

**  
Andrei Klimovich** 12:13  
And for me and Juan, I think that the next step will be after the call with income regarding the, how it's called, skill pay.

**  
Juan Martinez** 12:26  
Okay, yeah.

**  
Andrei Klimovich** 12:27  
Yeah, we need to define requirements, capabilities and requirements for recycler and dispenser Georgia version. Because, yeah, we need it by August. I mean, we need it right now. It should exist in JIRA as soon as possible. Okay.  
Yeah.

**  
Val Levitan** 12:51  
I say, I gotta go, I apologize, I'm sorry.

**  
Andrei Klimovich** 12:53  
Yeah, sure. That's basically that's it. An update from my side. Yeah.  
Thank you. Bye bye.

**  
Juan Martinez** 12:59  
All right. Thanks, everybody.

**  
Val Levitan** 13:01  
Thank you. Bye bye.

**  
Val Levitan** stopped transcription
