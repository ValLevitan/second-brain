# Raw Transcript — Pyramid Technologies — printer integration intro call
**Date:** January 8, 2026, 9:01 AM Eastern
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Summary note:** [[Meeting_Notes_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026]]
---
00:00:01 Speaker 1
are we waiting for uh anybody else to join us yes should be jonathan anybody else joining us.
00:00:32 Val
let's give them another five minutes well two minutes maybe we should take this time and introduce ourselves i'm the president of jvl jvl is a 42 year old company we started as an amusement manufacturer and we uh moved on into uh. gaming devices. As a side business, I used to own a company called Cash Code. I was the.
00:01:07 Val
original founder of the company, and the company later was sold in 2006 to Crane. And obviously, consequently, Crane bought MEI and History. And Pavel is a director of engineering. He is located in Belarus. JVL in Minsk is 100% subsidiary of JVL, a Canadian company, and.
00:01:43 Val
we had owned the company for the past 28 years. So yeah, that's shortly about us.
00:01:58 Speaker 3
Jonathan, you want to spend a little over 13 years on carry space.
00:02:18 Speaker 1
So we do this here in Mesa, Arizona. So we have our mechanical electrical software all under one roof. You should be able to answer.
00:02:59 Val
Okay maybe I should add something about us as well. We are currently departing Canada and we're moving to the US. Headquarters will be split between Miami, this is where I am now, and just a suburb of Atlanta in the state of Georgia. We love the US and we love Florida. I'm a big, big fan of your country. I was born in the Soviet Union and immigrated 45 years ago. But I was born and raised in Minsk.
00:04:04 Speaker 4
Yes, several times we are going and Texas Markets and Pyramid printers are widely used in the kiosks and we are going to repair the machines, the system.
00:04:31 Val
As an initial stage.
00:04:33 Speaker 4
Yes, as an initial, because we produce our own different schema.
00:04:44 Val
We actually have an expanded line of transactional equipment that's going to be introduced in the market later this year. We look at ourselves as direct competitors to Banilla.
00:05:10 Speaker 4
Okay, probably let's start with some technical questions. Let me share, I think it will help us understand. So this is the tickets captured by Exxon. We understand that the printer needs to be paired with the kiosk, so it's quite clear. The question came with Banilla kiosk.
00:05:49 Speaker 4
Should we produce tickets looks like presented on the screen? Yes. so the first question is if we connect a pyramid printer to our machines via a serial serial port and we use printer commands with something as you just printed using some kind of sql it will.
00:06:37 Speaker 1
generate just after send right specifically the escape pos documentation so once you talk about, serial so the recommendation there is the db9 table or the rj4 you are correct that the qr.
00:07:10 Speaker 1
compare our code will be automatically generated the payload that we previously sent to the printer.
00:07:22 Speaker 4
or encoded into this qr so all the tickets that we printed on the printer just need to. and it will be encoded into this qr okay so doesn't we are printing on this ticket we need just.
00:08:29 Speaker 4
You got it. So it looks quite real. So, okay.
00:08:54 Speaker 3
Sort of struggling to... Explain the consent might be required. Certain tickets you might not need to be a print box ticket.
00:09:10 Speaker 1
A ticket where there's duplicates.
00:09:46 Speaker 1
Exactly. Tickets that you use the same sort of. ...or lights, just use the same as generator.
00:10:23 Speaker 4
...configurations that we need set up before you replace.
00:10:39 Speaker 1
But that's pretty industry standard.
00:11:03 Speaker 4
So I assume that the easiest way, how can we start? Just to connect to your application. Application confirms tickets. First of all, just make a payment process and then rebate tickets. Yeah, without a...
00:11:38 Speaker 3
You use that mobile app. Browser. I mean, our support. So that's why we sent that. That whole kit is just so you can generate...
00:12:14 Speaker 1
What you want to do is, so I was working with Jonathan on a printer, two years ago, so the print configurations are all right, and the book and all of them, and in the future.
00:12:51 Speaker 3
after we're done with printers, because we can pre-drop that, that you could run JVL.
00:13:48 Val
I will ask our connection in Texas to clarify the types of tickets we need to support and I will revert back to you, Pavel, on this. Maybe I have another question for Kerry. Is it possible for you to release a, mechanical CAD file for our hardware integration into our machine? This would make our life easier,
00:14:24 Val
we don't have to hand measure it. So yes. So can it be sent to Gennady? By the way, introducing you to Gennady, our director of electromechanical department. Gennady is located in Toronto, Canada, but I am bribing him to move to Georgia.
00:15:05 Val
If I cannot entice him financially, I'll have to call my uncle Charlie to speak to him another way. All right, any more questions? Okay, Jonathan, thank you for introducing us to Kerry. Kerry, pleasure meeting you, sincerely, and I thank you very much for accommodating our time schedule.
00:15:38 Val
and look forward to working with you on this project.
00:15:42 Speaker 1
Thank you.
00:15:46 Speaker 4
Thank you, bye-bye. Thank you, bye.
