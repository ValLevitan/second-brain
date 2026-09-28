# Raw Transcript — Engineering — reliably detecting the Mutha Goose–to–printer connection under Flex-IQ (relay approach)
**Date:** August 10, 2026, 5:00 PM Eastern (Russian conversation, English rendering)
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_Mutha_Goose_Flex_IQ_Printer_Detection-August-10-2026]]
---
00:00:00 Speaker 1
The problem that Andrey mentioned today, which is related to the fact that we have a new system. After we switched from connecting through Utkus, Flexidio and Printer to connecting directly in parallel to the printer, a difficulty arose with the fact that we cannot reliably.
00:00:30 Speaker 1
Detect that our mutabus is connected. Because it's a standalone device, we don't know how it communicates with the printer. We can only catch signals. Since mutabus starts up much faster than flexid in case of power loss, it manages to, We send a signal to the printer, and it prints a small ticket. We don't have time to catch it in the LexisNexis system, so we determine that something is connected using other indirect methods. So, there are some alternative ways to do this. We probably discussed this with Kina, but we agreed that.
00:01:30 Speaker 1
There are no reliable ways. Probably we don't have such a thing as an FPE. The only reliable way is to turn off the motor, turn it on again. The only reliable way is to turn it on and off.
00:01:47 Ben
Yes, but this is only the first time. This is the first time I've encountered this in PowerLab. But temperature has not.
00:01:59 Speaker 1
Yet dropped below 50 degrees, It will continue to work, but if the power fails and then reappears, we'll catch the same situation again. So for an exhibition, it's not a big deal; you can just restart it. But for long- term use,
00:02:23 Ben
We need to think of some alternative approach. What changed?
00:03:33 Speaker 1
It is necessary to connect with two different cables, not in parallel, but in split. But at the same time, while the FlexIO is not loaded or is not working, shorten the lines inside the device. And if FlexIO is turned off, then the signal will pass through to the printer. We can't work as if we don't have FlexiQ. But when we've loaded, in this case, we can switch to managing through our packages. And then, in this case, we control everything that happens. First of all, we can print these checks that we currently cannot print.
00:04:35 Speaker 1
And to catch some packets that go through the network and send them to the computer. If we lose a connection, we just disconnect and reconnect.
00:04:53 Ben
To the network. But how does it work? What do you mean by" shortening"?
00:05:03 Speaker 1
There are several ways, but the most primitive is relays. These three lines have relays that, if the application is not working, they just pass the signal through. But as soon as the application turns on, we send a signal and take these controls to ourselves. We switch to another line and start passing through.
00:05:27 Ben
Ourselves. So this is delegation itself.
00:06:03 Speaker 1
And print something yourself, But at the same time, not break your head, if something happens in the flexi. That's what I mean. So, you can do it. Then, if everything suits you, we understand that for an exhibition this is enough. For an exhibition and for the first.
00:07:33 Ben
It's not a matter of time, it's not a matter of time. It's a matter of at least convening the meeting, signing it. That's four weeks until this reaches us. Okay, month is good, month. Well,
00:07:53 Speaker 1
That's how it is. But just very few people are interested in this issue anyway.
00:08:03 Speaker 1
Okay, let's try to do it. You know, we'll see how it goes. I think we can say something about this application and add something here. Yes, let's see what happens in this state where the object is detected. If you have a mark, you can check it. You can see the mark on the bus. It's very important that there is a connection. This a good sign, this a very good sign.
00:11:29 Ben
We don't have that. Well, I don't know,
00:11:33 Speaker 1
They turn on the localization for us. If they are in the morning, Every morning, they should be waiting for our departure from IKEA and then call and reconnect every day. It's very unpleasant. So, if there is a more or less acceptable option to just release some kind of release so that we can connect to it?
00:12:01 Speaker 1
We know that the girl is not in the hospital, because we have a specific location of her address.
00:12:07 Ben
It's a gas station. We already discussed this, but it was unclear in the morning. This is a new address, and if it's still true, then they will definitely turn on their phones tonight. This needs to be checked now. I am sure that they will turn on their phones at 90%.
00:12:32 Ben
Okay, we've.
00:12:34 Speaker 1
Arrived. We're stopping. I don't know what to do next. What should we do? How can we help? I don't know if she's not the one who was supposed to be there, then it's mostly a problem with the card,
00:12:49 Ben
But I don't have any money on me right now. If they don't make hand gestures, then without them it won't work. You can't let her go through.
00:13:01 Speaker 1
Ticket. So, we have a ticket in the system. We can see that there is such a thing as a standard trip. If we get this ticket in the flex system, then remove this ticket from us, an event will occur. We know that it works even if you get this standard trip. But what happens if you remove it from the example?
00:13:59 Ben
No, I'm not. But by the way, not the first, but the second one. The first one was thought out as we did it now. The second one was thought out so that we do it with a flame now. If just to talk about.
00:14:21 Speaker 1
Analogies. Let's sort it out today, maybe you'll think that. That you're comparing something else here.
00:14:58 Ben
Well, we said that we are ready.
00:15:01 Speaker 1
To sign the contract with the operator. We have a lot of questions about documentation, because it will be necessary to conclude a contract directly with the operator. They clearly indicated that they do not want to sign anything.
00:15:12 Ben
But I argued and insisted on this, so that they would conclude a contract with us. For us, this seems like a better option than being dependent on the operator. Although if you depend on someone else's operator.
00:15:30 Ben
Legal support. Yes,
00:15:37 Speaker 1
We'll call Philip in a few hours and talk about the details of what needs to be obtained from these masters.
00:15:48 Ben
In order to get this certificate. I hope it all happens quickly. If you don't have a certificate, you can't do anything. I wouldn't even try to sign a contract or close a deal with them.
00:17:04 Ben
Okay.
