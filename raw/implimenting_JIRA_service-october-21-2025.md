**Aaron + Val-20251021_094526-Meeting Recording**

21 October 2025, 01:45pm

11m 40s

**Val Levitan** 0:03  
To begin, uh.  
Where to begin?  
The organization or the thinking process of implementing Jira service in Georgia.

**Aaron Bockelie** 0:18  
Yes.

**Val Levitan** 0:19  
So we have clients, we have regular service calls. We actually started a WhatsApp discussion and for example that WhatsApp discussion could totally migrate to Jerry discussion.  
Uh, we have uh.  
Service people, we have one in particular that answers all the questions we have here reports to a supervisor who's also a production supervisor and she controls all the.  
Final product leaving the shop, so I I need to start thinking about engaging Jira service now.  
How? How should I start thinking about it? Just try, just just focus me, you know, point me in the direction.

**Aaron Bockelie** 1:16  
Sure. All right. So I think you've got an existing JSM sort of service desk environment that has been.  
Established. I haven't looked into it to understand how it's being used or managed right now, but it's it's there.  
So.  
Because you have a market specific support space that you need to fulfill.  
The uh.  
The JSM thinking JIRA service management space for this in in Georgia becomes just another sort of help desk system, essentially another project potentially. That's kind of where I'm thinking first.  
So this means that you have dedicated staff, you've got people on call, you've got people who are being dispatched and so forth in that space.  
I love the fact that you guys are using WhatsApp. I think that demonstrates just sort of a a desired organization. There's actually plugins for JIRA. There's apps for JIRA that you can add to your service management that integrate with WhatsApp.  
So you can actually take those chats or those threads in WhatsApp and turn them into discussions on a support ticket inside your.  
As an example, or capture the conversation for WhatsApp by including the JIRA issue as a as a third participant essentially and then all of the back and forth in WhatsApp.  
Becomes comments on that support tick in JIRA, so it's all tracked.

**Val Levitan** 3:05  
So if we if we define MV PS for engaging JIRA service module, the export or I should say integration of what's up the current procedures integration of the current.

**Aaron Bockelie** 3:14  
Mhm.

**Val Levitan** 3:23  
What's up? Culture could be my MVP. This could be my starting point if even if I don't format anything else and I'm just saying hey.

**Aaron Bockelie** 3:26  
Yep.  
Yeah.

**Val Levitan** 3:36  
I have this thing that is really working. Let me capture these discussions in Jira Service module.

**Aaron Bockelie** 3:44  
Mhm.

**Val Levitan** 3:45  
That's already a huge step forward because from there I could probably synthesize the actual problems or create or maybe even create tickets and work on the tickets and open and close tickets.

**Aaron Bockelie** 3:53  
Right.

**Val Levitan** 4:02  
Because the basic procedure is if a service call is received in whatever format, it opens a ticket and the job of a service person is to quickly close the ticket.

**Aaron Bockelie** 4:15  
Right.

**Val Levitan** 4:17  
And and and to satisfy the customer.

**Aaron Bockelie** 4:21  
So this is this is basically what is called chat OPS. This is an actual term. I don't know if you want to write that down, but chat OPS.  
Is a way to operate a platform with chat, and it's not limited to to WhatsApp. There's obviously a million different chat tools out there. You could just as easily do this with with Teams.  
Or half a dozen other chat tools for integration.  
What it really needs to be decided is is what is the actual flow for um.  
Integrating What is the flow that you want to have for supporting the customer? Does the customer reach out to JVL first? Do we? Does JVL make their rounds and ask if there's any problems?  
Is there instrumentation in the machines that flags it automatically? Like what initiates service calls and things like that, you know?

**Val Levitan** 5:27  
A number of things, a number of things, but but but I want to stick with MVP's. I want to pick the lowest hanging fruits first. I know that.

**Aaron Bockelie** 5:28  
Yeah, right. So.  
Parts.  
So pick the golden path, pick the golden path. Like we know there's lots of initiators, right? Let's pick the best one that would give us the most bang for our buck to start it out with and then we follow the flow through.

**Val Levitan** 5:47  
Customer.  
OK, so customer initiates a call either in the form of a call on on a mobile and the call is handed handed out or a WhatsApp message.

**Aaron Bockelie** 5:53  
Yep.  
Yes.  
Right. And if a phone call happens, the very next thing that the technician has to do is they have to switch the modes from phone call because they only last so long. They're epheromal, they they just last for a few minutes into.  
A support IA track support item.

**Val Levitan** 6:22  
How do they do it?

**Aaron Bockelie** 6:23  
They should be able to they they could start a WhatsApp message, right? Hi, are you? But maybe they're not on WhatsApp. Let's just assume that maybe the customer doesn't use WhatsApp.

**Val Levitan** 6:36  
They're they're always on the mobile. The entire world today operates on a mobile. So they call, they call. Hey, Tony.

**Aaron Bockelie** 6:39  
Right.

**Val Levitan** 6:47  
I have a problem.

**Aaron Bockelie** 6:48  
So, OK, so Tony, Tony, the operator, the the person who is is like, hey JVL, my machine's not working. OK. And then the and then and then here's JVL. Yeah. OK, Tony, I hear you. Let me let me go write that down. I got some notes here.  
Bye JVL so and so Tony from so and so has issues with things.

**Val Levitan** 7:17  
So, so I could implement a very quick initiative here. I could say a service call comes in, must be recorded and I could take that recording because my guys speak poor English and convert it into.  
A transcript.

**Aaron Bockelie** 7:35  
You could do that, but caturing the audio endoint on a mobile phone is hard.

**Val Levitan** 7:40  
No, it's not. It's actually on Android. It's there. It's available by a press of a button.

**Aaron Bockelie** 7:46  
So.  
You would have to have a special. So as soon as you say that though, we're talking about specialized tools to upsert a conversation into a ticket. My suggestion would be is that you can actually configure.  
JSM to work with SMS very simply. Everybody's got SMS, right? So you could have it. So basically.

**Val Levitan** 8:12  
OK.

**Aaron Bockelie** 8:15  
Technician text SMS.  
To JVL's SMS support system or even just right it there's we got to explore how how the right way to do this is. But essentially the very core is to get a ticket in JSM that we have to get a ticket registered in JSM.  
It's either by sending a text message to it, or by doing something that triggers that to happen.  
And once that happens, JSM has the ability to have a flow like it can ask a text message back to the technician. It can say who is the customer and then the person says blah blah blah and then JSM tries to match that customer name for example.  
These are more advanced flows already that we're talking about.  
But the the goal is, is to clearly identify who the customer is and a contact for that customer so the customer sees the connection from JVL's support system, not just random.  
Random phone number to some guy.  
Because that means that the that that Tony over there and the operator Tony is going to see JVLS on the ball because now you've got an official support ticket and Tony's going to see, oh, I can go here, I can click on this thing or I can just chat with my friend.  
You know Juan, who's from JBL? I shouldn't use Juan.  
I don't know somebody in the field at for for JVL.  
Um.  
So this means that you've established the ticket and Tony can either send another text message to the technician. The technician could gently redirect them to some other thing, say, hey, click on this link or maybe.  
As soon as the support request is officially accepted, Tony's gonna get an official text message from JVL's JIRA support system saying hi, your ticket is registered here. You can click here and see it on a web browser. Just click it on your mobile and it will pop up.  
U the login for the thing or you can text me for the status.  
Like that's kind of the flow that you might want.  
And then then Tony is like, uh ha, I don't even need to actually call the JVL tech because I can just use this link right here to communicate further till my problem solved.

**Val Levitan** 11:02  
You you gave me enough things to think about. Let me investigate how we work now. Let me formalize my thinking and I will revert back to you.

**Aaron Bockelie** 11:07  
Yeah.  
OK.  
Uh, little bit of.  
Process news outside of everything here, because we're about wrapping up is. Oh, sure. Yep. Stop recording. Yep.

**Val Levitan** 11:21  
Oh, hold on, hold on. One second. One second. Let me just. I need to.

**Val Levitan** stopped transcription