# Raw Transcript — Kyle Johnson — event recorder (black box) recruitment intro (with Nathan Carver)
**Date:** April 3, 2026, 1:07 PM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_Kyle_Johnson_Event_Recorder_Recruitment_Intro-April-3-2026]]
---
00:00:00 Val
Have a face to a name. Or maybe try to exit and log in again.
00:00:28 Val
You're On mute, just in case you didn't know.
00:00:52 Kyle Johnson
Yeah, I wonder if it's my. I think it's the.
00:01:08 Kyle Johnson
Yeah, I think it's my browser blocked it. Happens to me all the time.
00:01:33 Kyle Johnson
Uh, let me roll it back in. Maybe they'll ask me again. I know where you take off the camera. I'll be right back. Sure.
00:04:12 Nathan Carver
Okay. Sorry, I team was not letting me sign in for some reason. Funny enough, Kyle was having the same problem. Oh yeah, yeah. It took me like I guess almost ten minutes to get in. Huh?
00:04:29 Val
I have the same cup identical. Oh do you? Yeah, love these cups. Is it getting? Yeah.
00:04:39 Nathan Carver
Yeah. Yeah.
00:04:57 Val
There he comes. Oh,
00:05:05 Kyle Johnson
Hey, what's up, man? Hey Kyle. Hey, I am not running Linux this time, but I am still having camera issues. I am on Linux.
00:05:16 Val
Well, Occasionally, we had like horrible like issues back at Ion out on Linux with Teams.
00:05:24 Nathan Carver
Yeah, it was bad.
00:05:26 Kyle Johnson
I don't like it.
00:05:29 Val
Do you guys want to circulate Gmail chop? Anybody? Oh.
00:05:38 Nathan Carver
Google chat.
00:05:39 Val
Yeah, Google chat. Yeah, so I'm on Google. Yeah. Yeah, um. Do you want to invite us into a Google chat? That always works. How does it? Yeah. I don't know.
00:05:58 Nathan Carver
Uh, Google Meet.
00:06:09 Nathan Carver
It's kind of loading. I guess we're probably good now, other than Kyle. I think your camera's probably. Yeah, it's not working.
00:06:18 Kyle Johnson
I never use it, so apparently it's not working on this computer. Yeah,
00:06:28 Kyle Johnson
It's possible that I have like my antivirus is blocking it. I just couldn't figure out. I know it wasn't my other computer.
00:06:37 Nathan Carver
Yeah, I couldn't get in today either. It took me ten minutes to sign in.
00:06:42 Val
Let me just very quickly see if I could send the invite.
00:06:48 Nathan Carver
All right, I was able to start one. You want me to send the invite? Yeah, yeah, great. Here it is. You all can see it?
00:06:58 Val
Yep. Okay, I'll see you there guys. Okay. All right.
00:07:11 Mark Garland
Yeah. Hopefully, uh.
00:07:43 Mark Garland
I know. Oh, hold on a minute. I'm.
00:08:07 Nathan Carver
Not sure. I don't know if he got the message in Teams. I am going to send him to it.
00:08:44 Mark Garland
I got like uh.
00:09:16 Mark Garland
Alright. There he is. Hey,
00:09:35 Val
You are. Did you decide to use your cell phone? Yes. That.
00:09:44 Kyle Johnson
Always works. Yeah, I don't know why, but I just never used my camera on my phones and my computers. I have no idea.
00:09:55 Val
Well, I live on uh uh business calls, so I kind of i i have a setup. So i i don't blame you. Yeah,
00:10:07 Kyle Johnson
And most of the time, especially at work, even we don't have cameras. So if i'm just used to not being on camera.
00:10:16 Val
Where do you where do you work like what's the primary occupation.
00:10:21 Kyle Johnson
Um, yeah aerospace. Okay. So yeahum, I currently work for R T X and uh. Um, aeronautics aerospace division.
00:10:39 Val
That must be an experience they must have very stringent.
00:10:47 Kyle Johnson
It's very, it's very uh, very strict. Um, a lot of our. Yeah. And then most of our software is um critical system software. So it's a lot of like dealing with um either compliance for for export rules and stuff, or um uh like testing for like the FAA or the EU's um standards for flight safety software.
00:11:19 Val
Um, So we uh we make uh slot machines for the past forty two years games and uh transactional equipment. I used to own a company heavily involved in the transactional equipment. I sold it in two thousand and six, and the opportunity in our slot machine business came came around. Transactional equipment, by transactional I mean, transacting financial transactions. Right. And, yeah. So we embrace the opportunity and expanding in that direction, but parking it for a second. The particular need we have right now is in.
00:12:20 Val
It's kind of a, I'm gonna call it events recorder. And uh, it's a product that would sit on um, would be wedged on top of our system. And uh, record all of the events that happens between different modules. And if and when machine hangs for any reason we would uh, Go into that recorder and start analyzing.
00:12:58 Kyle Johnson
So, this is watching your machines, Not necessarily so kind of like recording events and determining potential issues or what happened.
00:13:08 Val
Correct, it could be different run- ins between framework and data center and Linux.
00:13:21 Val
For some reason, the watchdog timer doesn't reset. Or you know, as many events as we can capture.
00:13:29 Kyle Johnson
Okay. Okay, yeah.
00:13:31 Val
So it's kind of a in- flight black box. And if something happens, We go and investigate the first thing that we want to recover is the black box and hear everything that happened inside of the machine buttons press. Touch screen touched framework, set something to data center. Data center got into a cycle, got hung up. Um, yeah, whatever it is.
00:14:05 Kyle Johnson
Okay. Um, Are these interfaces already exposed? Or is this going to be like both that and then figuring out how to get the data like logged?
00:14:19 Val
Uh, we have. So first of all, I'm not an engineer. Okay. Um, I'm a businessman. Uh, so that's number one. I don't think I can answer your engineering questions. Okay, Okay, okay, But, uh we have a team of engineers. And uh, if you're asking me, if there is an architectural design yet, no There isn't Okay Uh, but I think we're quite capable of figuring out the architectural things.
00:14:50 Val
And at some point we need to uh. You know. Select select I I assume it will be an embedded solution of some sort, in in embedded processor. Uh, we need to probably uh. We envision that it will be sitting on top of our I O board. And so we'll Probably have to redesign the I O board, add the let's call it uh events recorder black box on top of it. Uh create some sort of a I don't know exit point. It could be a USB uh connection. It could be a um mobile uh cellular modem. But something has to you know.
00:15:49 Val
Back to us.
00:15:51 Kyle Johnson
Okay. And makes sense.
00:15:55 Val
So we have, um, we have embedded processor, we have a relationship with the current embedded processor engineer. I've known him for decades, very very knowledgeable individual but my entire company, Has been built on the Soviet Union era engineers, And although theoretically, they are top of the class when it comes to design culture, records, exchange culture, language barrier it just becomes unbearable.
00:16:47 Val
So I am seeking North American. Uh. Expertise, in everything. And hence, you know, I hired Nathan I have I surrounded myself with capable consultants. North American consultants, who is migrating my company from a certain style of doing business. To uh embracing AI properly, uh, filing things and filing it together with documentation and human notes. And um I asked Nathan, if he knows somebody who is who can not only adhere to these standards.
00:17:46 Val
Also, uh, Bring this sort of a culture or enforce this sort of a culture in my company. And he thought that you might be a good person for that. So this is this is what this call is all about.
00:18:03 Kyle Johnson
Okay, um. Yeah, I guess, some of it's gonna be how much like scope do you do you think there's gonna be? Um, I've I've definitely done a lot of, Transformations and especially when it comes to things that include grabbing information right out of a system. Normally, I do it for verification purposes, but I've done a lot for essentially taking embedded systems and getting information, making sure the system is.
00:18:44 Kyle Johnson
Correctly aligning with requirements, especially for anything that requires certifications or any regulated markets. But I guess because of my current job, My question is kind of along the lines of how much time commitment do you have? Would you expect and like how much work is there?
00:19:09 Val
Well, I have full respect to the fact that you have a full time job when you are not. To quit your job to do this job. That's how I'm reading your question. And of course, we will uh. Work around around your capacity. Okay, so with Nathan for example, He tells me that he can give me X number of hours per week, and we cater to that to that load.
00:19:44 Val
And I would picture that the same thing would work with you. And again, Your this event recorder is not schedule critical device because I can snap it in when it's ready. Okay. I don't want it to be a five-year project if this if this what you're asking me. Right, right, yeah. Within a reasonable amount of time, using reasonable amount of your personal capacity. I think that would fit nicely into your lifestyle and. I think it will satisfy us as well. And it would also expose us to uh, a North American culture. Another another input of North American design culture, which I personally have a great respect to.
00:20:44 Val
And I think, I think we could benefit. We could both benefit from it. That's how I put it. Right, that makes sense to me. Is there a particular uh embedded processor that you feel comfortable with?
00:21:09 Kyle Johnson
Um, depends on the line, I guess.
00:21:15 Kyle Johnson
Worked on multiple multitude of them, whether they're microprocessors or ARM base, I guess. I mean, would depend on which ones. I've done a lot of microprocessors when it comes to TI parts, But microprocessors sorry, things like ARMs more just been.
00:21:37 Val
So it's general you are used to European processors.
00:21:46 Val
Um. Or Chinese.
00:21:48 Kyle Johnson
Probably most of them are Chinese, honestly probably Chinese.
00:21:52 Val
Is it the RK family?
00:21:56 Kyle Johnson
Yeah andum who's the other one? Uh why can I not think of it? The their blue their company's blue what is it?
00:22:15 Val
Uh, But normally like you're familiar with Rockchip, yeah. No. R K.
00:22:25 Kyle Johnson
What kind of architecture is it?
00:22:27 Val
Um, I don't know.
00:22:31 Kyle Johnson
Is it an ARM or is it like a RISC?
00:22:36 Val
I think uh I think ARM is uh a particular architecture from Europe.
00:22:41 Kyle Johnson
Right. Uh Is it European?
00:22:45 Val
I thought it was, you know, maybe I am wrong, but I thought it was European. Um, what is that?
00:22:53 Kyle Johnson
I thought they were out of California. This is a bunch of manufacturers, right? Like his ARM is the architecture, and then there is tons of everybody's allowed to buy and manufacture. Um, And so I've done a lot of like different languages in Coretex zero, like M zeros back in the day.
00:23:15 Kyle Johnson
After that, it was the generalized ARM fives and ARM sevens and stuff. But a lot of those times. We were not necessarily doing with bare metal at that point. A lot of times that was embedded Linux and then running on top of the. The processor, Like you would have drivers and board setup and stuff you'd have to do for like your device trees. But besides that, and then yeah, and then when it comes like microprocessors, then at that point it ranged. Sometimes, it was a like proprietary operating system that was basically written in house, or it was bare metal where you were just trying to run a very specific thing. But I don't think we really do that as much anymore.
00:24:13 Val
Okay. This one in particular, like. Uh, here it is.
00:24:41 Kyle Johnson
Okay, so it's like a whole setup thing.
00:24:45 Val
Yeah, but I mean we have our own data sheet on it. This is one of the boards designed by somebody else, but we would probably want to put our own chip on it. Okay,
00:25:06 Kyle Johnson
I see. So it's a whole SOC.
00:25:11 Kyle Johnson
Okay, it's a Cortex A fifty five. Okay, four core. Yeah, I've done some things with the A fifty five before.
00:25:23 Val
But but again I am overstepping my boundaries right now. I am becoming an engineer and I shouldn't. That's not a good thing. So to which extent do you need? Are you capable of doing the architecture yourself, or do you need somebody else involved?
00:25:48 Kyle Johnson
No, I can do it as long as we have a basic understanding of the requirements and goals and stuff.
00:26:02 Val
Are you able to work with like we have a certain culture that.
00:26:10 Val
In the company that sometimes really hard to work with, and I recognize it. And I just don't want to put you in a situation where you really suffered the relationship. I don't know, Nathan, maybe you can jump in and really describe your opinion about the culture.
00:26:34 Nathan Carver
Um, yeah, I think the culture is i would say.
00:26:41 Nathan Carver
They're quiet, not necessarily assertive in meetings. It can be difficult to get information that you need, so you'll have to drive a lot of that. And for whatever the cultural reasons are, and some of it's language barrier I think. So on your side, whatever you need, You'll have to make sure you're just you're driving that forward with whoever you're working with. With the JVL and making sure that you are initiating all that, because they won't necessarily initiate with you unless you are actively pushing for it.
00:27:22 Val
I agree with those things.
00:27:25 Kyle Johnson
Okay, that makes sense.
00:27:27 Val
And they somewhat, they believe that Americans do things better, and they should be talking to this.
00:27:45 Kyle Johnson
Yeah, I mean, I don't have a problem with that. I've worked in some environments where getting information tended to be a lot more having to go and figure out who to talk to, talking to them, trying to get them to answer questions, Having to follow up, sometimes both talking to them and sending emails and trying to get the information or sometimes just. Coming up with hey, this is how I see it. Is this how you see it Sometimes that works better, And that way it facilitates them being able to communicate back, whether or notum. The issues that they have like very particular, they think a lot of times I can help a lot better.
00:28:32 Val
Okay okay so yeah so that's good. Um do you have uh in mind. Number of hours that you could allocate, and also the engineers are at zero plus three hours, and you are at zero minus what minus. The.
00:29:03 Kyle Johnson
Guy in hour minus three or something like that. Well, no zero.
00:29:11 Val
Zero minus six, Right?
00:29:12 Kyle Johnson
Yeah, I was gonna say, yeah. I think it's zero minus six.
00:29:16 Val
So there's gonna be a nine hour time difference.
00:29:22 Kyle Johnson
Okay. Yeah, I'll have to figure that out. Uh, I'll have to figure that out andum. yeah, and I'll have to think about that but.
00:29:35 Val
You're in Arizona right? Yes. Arizona is uh minus two hour Eastern time.
00:29:41 Kyle Johnson
Yeah. Yes. Yep.
00:29:49 Val
Minus six. So, anyway, there's substantial time difference. Yeah, yeah. These guys work late, but I mean to which extent? I mean that means you would have to start your day very early.
00:30:12 Val
And early riser. No.
00:30:18 Kyle Johnson
Yeah, normally I'm up really late. So, um, well sometimes I'm up to the morning in Europe. So.
00:30:30 Val
That might be an issue for you, right?
00:30:33 Kyle Johnson
Yeah, yeah in mindum we'll see if I have to change schedule then, I'll have to figure out how to do that.
00:30:46 Val
Okay, look, I'd like to leave you with these things and let you think about it and let you get back to me. I don't want you to get into a bind where you start feeling uncomfortable. Because if I start going with you, I like to know that there is longevity there. Right. And uh, you're not gonna quit in the middle but that's dangerous. Right now understand?
00:31:10 Kyle Johnson
Yeah noum, Definitely think that through before.
00:31:13 Val
Making any decisions. So, think it through. If something doesn't feel comfortable, Just let me know and we can either fix it or we just not going to go for it. Okay. Sometimes it's better this way.
00:31:25 Kyle Johnson
Yeah, no, I agree.
00:31:28 Val
Okay, what do you need? Is a week good enough for you just to.
00:31:35 Kyle Johnson
Yeah, I'll have a decision in a week. Okay, so probably before.
00:31:40 Val
Connect with me. And if you uh need to speak to our engineering team or if you wanna get more information or if if you uh want to speak to me again, connect with me and we'll continue.
00:31:54 Kyle Johnson
Okay sounds good. All right.
00:31:59 Val
Okay well very nice meeting you and wish you all the best.
00:32:03 Kyle Johnson
All right thank you have a great day bye. All right see ya see ya.
00:36:08 Mark Garland
Yes.
00:39:22 Mark Garland
Thank you.
00:45:11 Mark Garland
Yes.
01:04:07 Mark Garland
Okay.
