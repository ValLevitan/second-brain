# Raw Transcript — RIS features follow-up: fewer factory resets
**Date:** September 25, 2026, 10:34 AM – 11:33 AM Eastern
**Segment:** 2 of 2
**Summary note:** [[Meeting_Notes_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026]]
---
WEBVTT

00:00:03.053 --> 00:00:14.293
<v Val Levitan>meeting. Yeah. So what we were, we left the meeting, we got deviated and we got into the thick of.</v>

00:00:15.413 --> 00:00:16.613
<v Val Levitan>The discussion.</v>

00:00:17.733 --> 00:00:29.093
<v Val Levitan>of everything that we need to change. So we lost our focus of the conversation. And I want to bring us back into focus. I want to find at least one.</v>

00:00:30.373 --> 00:00:41.173
<v Val Levitan>maybe hopefully two, three items that by fixing it, we can alleviate maybe 50, 60% of the issues.</v>

00:00:43.093 --> 00:00:50.453
<v Val Levitan>And I would call it MVP1 release of the RIS. So RIS rework.</v>

00:00:52.453 --> 00:00:54.693
<v Val Levitan>MVP1 release.</v>

00:00:58.213 --> 00:01:13.373
<v Val Levitan>If Irina and Pavel can tell me, look, the number one thing I can do is this. And this will take us to, let's say, 40% or 30%.</v>

00:01:14.533 --> 00:01:24.053
<v Val Levitan>And here's #2 I could do, it will take us to 50%. And here's #3 I could do, it will take us to 60%.</v>

00:01:24.853 --> 00:01:33.413
<v Val Levitan>And it will take us approximately that long and we can get it to MVP1 approximate release date, I don't know, whatever that date is.</v>

00:01:34.373 --> 00:01:41.733
<v Val Levitan>Then between these three items, maybe I will say, look, when can you give me just one?</v>

00:01:43.093 --> 00:02:02.493
<v Val Levitan>The number one, can you do it much faster? And they will say, yeah, it will shave 50% of the time. And we'll say, go for number one right now. Let me introduce it in the MVP one, or even maybe possible within the V3 release. Maybe I will go through quick reapproval.</v>

00:02:04.853 --> 00:02:07.813
<v Val Levitan>Even if we can get it next week, OK, fine.</v>

00:02:12.213 --> 00:02:31.813
<v Val Levitan>So that is the focus of the discussion. I think last time we really lost focus. Not that we, I'm not saying that we were discussing wrong things, we were discussing the right thing. But I think we lost focus of what we need to deliver. And what we need to deliver is</v>

00:02:31.973 --> 00:02:35.173
<v Val Levitan>An immediate relief, relief.</v>

00:02:36.253 --> 00:02:42.293
<v Val Levitan>Of the suffering that is out there, and the suffering is incredibly immense.</v>

00:02:44.613 --> 00:02:59.653
<v Val Levitan>And the most suffering comes with the factory reset, that everything requires a factory reset for us, which I'm repeating myself, is appropriate design for 20 year ago.</v>

00:03:00.693 --> 00:03:02.053
<v Val Levitan>Uh, use cases.</v>

00:03:05.093 --> 00:03:05.893
<v Val Levitan>But not today.</v>

00:03:09.973 --> 00:03:13.733
<v Val Levitan>So, I'm gonna pause, I'm gonna let maybe...</v>

00:03:14.893 --> 00:03:26.053
<v Val Levitan>Pavel and Irina to philosophize a little bit and get back to us maybe with one, possibly two, and if we're lucky, maybe three things that we can shave off right now. Thank you.</v>

00:03:27.493 --> 00:03:33.493
<v Pavel Frolov>So, last time when we when we talked about this, it was a suggestion.</v>

00:03:32.453 --> 00:03:32.933
<v Irina Shishko>Mhm.</v>

00:03:34.693 --> 00:03:38.133
<v Pavel Frolov>That we can quite easily introduce new feature.</v>

00:03:39.893 --> 00:03:43.333
<v Pavel Frolov>To apply the same AR, yes.</v>

00:03:44.773 --> 00:03:48.933
<v Pavel Frolov>After factory reset, as it was previously installed.</v>

00:03:50.133 --> 00:04:12.133
<v Pavel Frolov>I think this will fix more than 50% of cases when the person needs to go to the office, download file, write it to USB stick, come back to the location and so on. Of course, this is not a void procedure of decommissioning and commissioning.</v>

00:04:09.093 --> 00:04:09.573
<v Irina Shishko>Mhm.</v>

00:04:14.293 --> 00:04:16.773
<v Pavel Frolov>But at least it will save lots of time.</v>

00:04:23.013 --> 00:04:24.613
<v Pavel Frolov>I think this is #1.</v>

00:04:25.413 --> 00:04:28.053
<v Pavel Frolov>That can be fixed, that can be fixed.</v>

00:04:27.333 --> 00:04:30.053
<v Val Levitan>I need, I need to take this, continue talking.</v>

00:04:32.773 --> 00:04:42.933
<v Pavel Frolov>Next, this is not a separate point, but we need to keep in our mind that performing factory reset.</v>

00:04:33.573 --> 00:04:33.813
<v Irina Shishko>Uh...</v>

00:04:44.533 --> 00:04:56.293
<v Pavel Frolov>Instead of reinstalling software, we'll save also time because the same software will be installed, not not installed, but reinitiated during factory reset.</v>

00:04:50.373 --> 00:04:51.013
<v Felipe Miranda Giorgi>Yes.</v>

00:05:09.893 --> 00:05:16.453
<v Irina Shishko>Device of Elisa.</v>

00:05:15.093 --> 00:05:26.373
<v Pavel Frolov>Yeah, Irina, Irina is asking what is the most possible reason why new software installed on the machine?</v>

00:05:27.333 --> 00:05:28.973
<v Irina Shishko>No, you are.</v>

00:05:29.413 --> 00:05:32.893
<v Pavel Frolov>The same, why the same software installed on the machine?</v>

00:05:34.373 --> 00:05:34.973
<v Pavel Frolov>Ach.</v>

00:05:35.653 --> 00:05:53.653
<v Felipe Miranda Giorgi>Maybe, can you hear me? Okay, yes. Maybe, Irina, maybe cases where the software crash for any reason, like a boot loop, is not an update, but, and to be honest with you,</v>

00:05:38.693 --> 00:05:39.173
<v Pavel Frolov>Yes.</v>

00:05:54.693 --> 00:06:07.413
<v Felipe Miranda Giorgi>It was, I remember that we were always told, in any case, you need to do a factory reset, it's faster to upload the software.</v>

00:06:08.853 --> 00:06:27.413
<v Felipe Miranda Giorgi>Yes, it is the same process and you starting from the same point. Now, I mean, I understand it's not because you lose some information, correct, Pavel? But if RIS could be saved and factory reset is the...</v>

00:06:21.413 --> 00:06:21.973
<v Pavel Frolov>Yes.</v>

00:06:27.973 --> 00:06:41.493
<v Felipe Miranda Giorgi>is the solution? That helps A lot. Yes, it doesn't help the decommissioning or recommissioning, but it saves the problem of not having the RIS in hand. Yes, it helps.</v>

00:06:43.093 --> 00:06:43.373
<v Pavel Frolov>Yeah.</v>

00:06:44.613 --> 00:06:45.733
<v Irina Shishko>No.</v>

00:06:47.653 --> 00:06:49.493
<v Felipe Miranda Giorgi>Did I answer your question, Irina?</v>

00:06:49.893 --> 00:07:07.253
<v Pavel Frolov>How, how, how often? How often? Probably you can split different cases when the technician perform factory reset on or reinstallation. How much, how many percentage for particular cases?</v>

00:06:56.933 --> 00:06:57.573
<v Felipe Miranda Giorgi>Okay.</v>

00:07:07.973 --> 00:07:09.093
<v Felipe Miranda Giorgi>Okay, so...</v>

00:07:10.253 --> 00:07:14.613
<v Felipe Miranda Giorgi>So, for example, if you look at the 8 user cases that are there.</v>

00:07:14.573 --> 00:07:15.053
<v Pavel Frolov>Mhm.</v>

00:07:15.973 --> 00:07:34.733
<v Felipe Miranda Giorgi>Battery changer is an error, so hard reset. Software upgrade, no. Software crash. Add or remove printer, yes. So user case one, user case 3, user case 4, user case 5. User case 6.</v>

00:07:35.733 --> 00:07:35.893
<v Pavel Frolov>Okay.</v>

00:07:36.533 --> 00:07:38.693
<v Felipe Miranda Giorgi>and user case 8.</v>

00:07:42.773 --> 00:07:45.573
<v Pavel Frolov>So the most painful.</v>

00:07:43.173 --> 00:07:49.253
<v Felipe Miranda Giorgi>All of this, you could reinstall software for the same version.</v>

00:07:50.533 --> 00:07:50.853
<v Pavel Frolov>Yeah.</v>

00:07:51.333 --> 00:07:52.373
<v Irina Shishko>Nava Prose.</v>

00:07:53.333 --> 00:08:02.213
<v Pavel Frolov>So, the most painful case with battery change, as I understand, and air crashes.</v>

00:07:59.413 --> 00:08:00.053
<v Felipe Miranda Giorgi>No.</v>

00:08:01.413 --> 00:08:12.133
<v Felipe Miranda Giorgi>Battery change, everything, a little bit of everything. All of them happen very, very often. Unfortunately, I don't have...</v>

00:08:07.253 --> 00:08:07.653
<v Pavel Frolov>Ohh.</v>

00:08:13.493 --> 00:08:25.653
<v Felipe Miranda Giorgi>A log of all reported troubleshooting on the phone or on text, because it's too much work. Sometimes you're doing something and they call you and you help, but...</v>

00:08:18.813 --> 00:08:19.253
<v Pavel Frolov>EHT.</v>

00:08:27.093 --> 00:08:30.613
<v Felipe Miranda Giorgi>But I can show you, for instance.</v>

00:08:33.133 --> 00:08:52.053
<v Felipe Miranda Giorgi>And I don't want to deviate because I don't want to correct, cause the same problem, but I have a log of all the repairs in-house and all the repairs that we do hard reset is most of them. Critical errors and...</v>

00:08:45.173 --> 00:08:45.333
<v Pavel Frolov>The.</v>

00:08:52.293 --> 00:08:54.333
<v Felipe Miranda Giorgi>software crashing, etc.</v>

00:09:25.653 --> 00:09:27.413
<v Pavel Frolov>Felipe, correct me if I wrong.</v>

00:09:30.413 --> 00:09:40.533
<v Pavel Frolov>In any case, when we clear meters on the machine, we also need the commissioning and commissioning.</v>

00:09:41.893 --> 00:09:42.693
<v Felipe Miranda Giorgi>Yes.</v>

00:09:43.173 --> 00:09:46.853
<v Pavel Frolov>Even if we do not change any games, settings.</v>

00:09:46.853 --> 00:09:50.693
<v Felipe Miranda Giorgi>If you do a factory reset, you need to decommission, yeah.</v>

00:10:04.773 --> 00:10:05.493
<v Felipe Miranda Giorgi>Okay.</v>

00:10:06.693 --> 00:10:26.373
<v Felipe Miranda Giorgi>I think if you clean, I need to confirm, but I am pretty sure if you must clear the meters, you have to do a hard reset. I mean, you have to decommission because you need to let the lottery know that the numbers will go, the turnaround will change.</v>

00:10:07.013 --> 00:10:07.053
<v Pavel Frolov>Uhh...</v>

00:10:26.693 --> 00:10:35.653
<v Pavel Frolov>So, okay, the next idea is this factory reset to provide.</v>

00:10:36.613 --> 00:11:00.533
<v Pavel Frolov>different versions, different types of soft factory reset. For example, we do not touch game settings, we do not touch meters, but we clear events probably, we clear some state. For example, last game was crushed for some reason and</v>

00:11:00.933 --> 00:11:16.373
<v Pavel Frolov>goes to an undefined state. So probably we can try to clear this data, but left all the rest, including accounting data.</v>

00:11:18.773 --> 00:11:29.893
<v Pavel Frolov>In this case, I think probably it could help in some critical error cases. And it could be done without decommissioning.</v>

00:11:32.373 --> 00:11:44.933
<v Pavel Frolov>It, but it looks not so easy. It really requires some investigation, how it works and what exactly can we fix.</v>

00:11:41.733 --> 00:11:42.293
<v Irina Shishko>Mhm.</v>

00:11:46.453 --> 00:11:59.413
<v Pavel Frolov>Definitely it can be done in some case and when the machine crashes due to money transfer error. Not sure that this is quite often.</v>

00:11:59.973 --> 00:12:00.613
<v Felipe Miranda Giorgi>Nah.</v>

00:12:01.613 --> 00:12:01.813
<v Pavel Frolov>Egm.</v>

00:12:05.093 --> 00:12:20.533
<v Felipe Miranda Giorgi>Money transfer error happens. It has happened, but it's usually because the printer does not have the right firmware when it's first installed and when they correct this, no problem after that.</v>

00:12:21.253 --> 00:12:22.213
<v Pavel Frolov>Okay.</v>

00:12:37.973 --> 00:12:55.893
<v Irina Shishko>Yeah, precise. What are the commission? Commission. No, no. It's your device.</v>

00:12:56.133 --> 00:12:57.333
<v Irina Shishko>So, just come.</v>

00:12:58.453 --> 00:12:59.693
<v Irina Shishko>Seven and Shavialeu.</v>

00:13:03.413 --> 00:13:04.453
<v Irina Shishko>Love my body.</v>

00:13:08.013 --> 00:13:17.173
<v Irina Shishko>He is Elisa.</v>

00:13:21.813 --> 00:13:22.613
<v Pavel Frolov>Oh.</v>

00:13:34.175 --> 00:13:36.335
<v Irina Shishko>2 просто одинаковых этих.</v>

00:13:37.605 --> 00:13:42.085
<v Val Levitan>Да, я думаю, что нам не нужно передавать статистику на.</v>

00:13:43.275 --> 00:13:46.515
<v Val Levitan>Это старые игры, нам нужно переходить на.</v>

00:13:48.355 --> 00:13:54.115
<v Val Levitan>Модуль выше нот, перевод или пару seanding stade s overqqу.</v>

00:13:56.165 --> 00:14:01.205
<v Val Levitan>Модам порашен and and moody ансамбль газа модом выкрут.</v>

00:14:02.405 --> 00:14:05.125
<v Val Levitan>Изоли чанс foreting dotonet.</v>

00:14:06.115 --> 00:14:12.195
<v Val Levitan>Конечно, мама Фрейд от idendot here thind sation am sorry het thi tech.</v>

00:14:13.115 --> 00:14:14.555
<v Val Levitan>Это ты лайн.</v>

00:14:17.505 --> 00:14:20.145
<v Val Levitan>Филиппины, джон хасал.</v>

00:14:21.285 --> 00:14:21.975
<v Felipe Miranda Giorgi>Алка.</v>

00:14:22.995 --> 00:14:23.315
<v Felipe Miranda Giorgi>Да.</v>

00:14:26.235 --> 00:14:31.315
<v Val Levitan>Freed atrutive renager, fronder сабчук.</v>

00:14:33.025 --> 00:14:40.985
<v Val Levitan>I want of fine won towe sray i tams taty hot chave and pavel stary to to tok bate the fone ragin i hato.</v>

00:14:41.395 --> 00:14:42.075
<v Pavel Frolov>Окей.</v>

00:14:41.795 --> 00:14:42.675
<v Felipe Miranda Giorgi>Да.</v>

00:14:44.015 --> 00:14:48.495
<v Felipe Miranda Giorgi>Это не лучше, говорит палу.</v>

00:14:48.555 --> 00:14:52.555
<v Pavel Frolov>Окей, solutsin namber one jo andle.</v>

00:14:53.205 --> 00:14:56.285
<v Pavel Frolov>Оплаен привисли.</v>

00:14:57.815 --> 00:14:59.295
<v Pavel Frolov>Привисли плает рис.</v>

00:15:00.245 --> 00:15:05.245
<v Pavel Frolov>Автофэкторе ресет баднот after softway rintallation.</v>

00:15:06.965 --> 00:15:07.295
<v Pavel Frolov>Баты.</v>

00:15:07.638 --> 00:15:11.158
<v Pavel Frolov>It will require the commissioning and commissioning.</v>

00:15:14.438 --> 00:15:30.598
<v Pavel Frolov>The next possible idea is just started discussion discussion in this relates to cases when we have some crashes or.</v>

00:15:33.078 --> 00:15:33.718
<v Pavel Frolov>Error.</v>

00:15:34.878 --> 00:15:53.958
<v Pavel Frolov>Critical errors: What if we do not perform a full factory reset, but introduce some soft version of factory reset? For example, we are left on the machine all the game settings.</v>

00:15:55.158 --> 00:15:58.518
<v Pavel Frolov>And try to save all the meters.</v>

00:15:59.798 --> 00:16:02.198
<v Pavel Frolov>But clear all other information.</v>

00:16:03.278 --> 00:16:15.558
<v Pavel Frolov>In some cases, it looks like it will fix crash, and probably it will not require decommissioning and commissioning.</v>

00:16:16.918 --> 00:16:29.558
<v Val Levitan>I have a couple of questions about it. First of all, I want to make sure that the previous version of software that are registering tilt or crash have the watchdog timer in them.</v>

00:16:31.478 --> 00:16:52.118
<v Pavel Frolov>Okay, a watchdog timer is doing what? A machine booted into, let's say, tilt one. It determines tilt one, and it goes to reboot after 30 seconds. During next boot, it again goes to tilt one.</v>

00:16:52.278 --> 00:16:56.038
<v Pavel Frolov>And after 30 seconds goes to reboot and so on, so on.</v>

00:16:57.638 --> 00:17:07.638
<v Val Levitan>Okay, so maybe the logic should be if this still reappears after reboot, then automatically enter soft reset.</v>

00:17:10.438 --> 00:17:18.198
<v Val Levitan>Not hard reset and only after the soft reset didn't help. Soft reset is what you are suggesting.</v>

00:17:19.478 --> 00:17:19.718
<v Pavel Frolov>Yeah.</v>

00:17:20.198 --> 00:17:28.278
<v Val Levitan>If that didn't help, maybe display the final tilt. Basically, tilt will call, we'll call it pizdet.</v>

00:17:29.318 --> 00:17:29.398
<v Pavel Frolov>The.</v>

00:17:30.038 --> 00:17:32.758
<v Val Levitan>And at that point, hard reset.</v>

00:17:34.918 --> 00:17:35.398
<v Pavel Frolov>Mhm.</v>

00:17:36.758 --> 00:17:40.358
<v Val Levitan>You could spell it out in English, in English.</v>

00:17:37.238 --> 00:17:37.798
<v Irina Shishko>Mhm.</v>

00:17:45.478 --> 00:17:51.238
<v Val Levitan>Felipe, this is a very important reset. You have to remember, it's called peace deaths.</v>

00:17:47.438 --> 00:17:47.878
<v Pavel Frolov>Hmm.</v>

00:17:49.238 --> 00:17:49.398
<v Pavel Frolov>Ach.</v>

00:17:52.078 --> 00:17:56.198
<v Irina Shishko>I can speak to you, Alex.</v>

00:17:53.398 --> 00:17:54.918
<v Val Levitan>Write it down. Write it down.</v>

00:17:54.598 --> 00:17:57.718
<v Felipe Miranda Giorgi>Yeah, I'm spelling it. I'm spelling it, yeah.</v>

00:17:57.958 --> 00:17:58.918
<v Val Levitan>Spell it out.</v>

00:17:58.198 --> 00:17:58.758
<v Irina Shishko>Two.</v>

00:17:59.318 --> 00:18:05.158
<v Felipe Miranda Giorgi>Sounds like business, so I'll remember biz debts. That's fine. Biz debts, right?</v>

00:17:59.798 --> 00:18:00.358
<v Val Levitan>That's it.</v>

00:18:02.438 --> 00:18:02.838
<v Pavel Frolov>Yeah.</v>

00:18:02.598 --> 00:18:06.598
<v Val Levitan>Is this, is this, and it's called, and it's called hard reset.</v>

00:18:07.078 --> 00:18:07.718
<v Felipe Miranda Giorgi>OK.</v>

00:18:08.598 --> 00:18:10.918
<v Felipe Miranda Giorgi>You're teaching me some bad words, probably, right?</v>

00:18:11.158 --> 00:18:11.718
<v Pavel Frolov>He.</v>

00:18:11.398 --> 00:18:15.718
<v Val Levitan>That's the word you should know, especially in our business.</v>

00:18:13.878 --> 00:18:14.478
<v Felipe Miranda Giorgi>Okay.</v>

00:18:16.518 --> 00:18:17.158
<v Felipe Miranda Giorgi>Okay.</v>

00:18:20.358 --> 00:18:20.918
<v Pavel Frolov>Pki.</v>

00:18:22.598 --> 00:18:25.398
<v Val Levitan>I wonder how, wonder how the transcript will pick up.</v>

00:18:33.718 --> 00:18:37.398
<v Val Levitan>And also, then I may as well ask another question.</v>

00:18:40.358 --> 00:18:47.398
<v Val Levitan>Anything that relates to passport, can passport changes be silenced out?</v>

00:18:48.278 --> 00:18:49.158
<v Val Levitan>Without.</v>

00:18:50.438 --> 00:18:51.558
<v Val Levitan>Hunt reset.</v>

00:18:53.718 --> 00:18:56.518
<v Val Levitan>Can we take a note of a passport change?</v>

00:18:57.638 --> 00:18:58.278
<v Val Levitan>But...</v>

00:19:00.598 --> 00:19:00.678
<v Pavel Frolov>The.</v>

00:19:00.598 --> 00:19:02.598
<v Val Levitan>Allow it, basically allow.</v>

00:19:03.798 --> 00:19:08.038
<v Val Levitan>component exchange. We have that flag already.</v>

00:19:09.078 --> 00:19:22.438
<v Pavel Frolov>Yes, yes, it works on the fly when you just reboot and change something. But it required during factory reset to apply and send to the serial this information.</v>

00:19:19.638 --> 00:19:20.118
<v Irina Shishko>Mhm.</v>

00:19:22.678 --> 00:19:23.318
<v Felipe Miranda Giorgi>Yes.</v>

00:19:23.478 --> 00:19:27.478
<v Val Levitan>So can we rework it? Can we rework it in a way that it doesn't need it?</v>

00:19:24.118 --> 00:19:24.158
<v Pavel Frolov>Uhh...</v>

00:19:28.358 --> 00:19:46.278
<v Pavel Frolov>Yes, I think the logic could be pre-save all the changes, but and do not anything during factory reset, but send this information during next QR scan, for example.</v>

00:19:49.158 --> 00:19:49.318
<v Irina Shishko>Mm.</v>

00:19:49.798 --> 00:19:55.318
<v Val Levitan>Or, in case it will be a modem, then send it via modem.</v>

00:19:56.678 --> 00:19:57.638
<v Pavel Frolov>Yeah, yes.</v>

00:19:57.078 --> 00:19:57.718
<v Irina Shishko>Yes.</v>

00:19:57.878 --> 00:20:05.078
<v Val Levitan>So look, we have 3000 machines and locations. This software that we will be releasing.</v>

00:20:02.198 --> 00:20:02.358
<v Pavel Frolov>No.</v>

00:20:06.518 --> 00:20:12.198
<v Val Levitan>It will only, it will not update any games. All it will do, it will remove.</v>

00:20:13.638 --> 00:20:27.398
<v Val Levitan>any sort of hard form of reset that requires decommissioning. And so Sebastian, when he arrives there, his job will be to go and...</v>

00:20:28.998 --> 00:20:30.518
<v Val Levitan>Update all of the machines.</v>

00:20:31.798 --> 00:20:37.398
<v Val Levitan>Of course, it will not be as direct as this, but assist in upgrading all of the machines.</v>

00:20:37.678 --> 00:20:38.038
<v Felipe Miranda Giorgi>Ready?</v>

00:20:40.358 --> 00:20:41.318
<v Val Levitan>In locations.</v>

00:20:45.318 --> 00:21:00.678
<v Val Levitan>So, no game changes, but three and a half, the two and a half, 3000 machines that we have, we will remove all type of, as many type of hard resets as possible, as many decommissioning as possible or recommissioning as possible.</v>

00:21:00.438 --> 00:21:03.398
<v Felipe Miranda Giorgi>Only, only Flex machines, right? Obviously.</v>

00:21:04.118 --> 00:21:04.758
<v Val Levitan>Only.</v>

00:21:05.478 --> 00:21:10.678
<v Felipe Miranda Giorgi>Only Flex machines. We're not referring to Altera H or any.</v>

00:21:10.678 --> 00:21:14.758
<v Val Levitan>Yeah, yeah, yeah, yeah, no, Altera is done, finished, finished, is done.</v>

00:21:13.558 --> 00:21:16.678
<v Felipe Miranda Giorgi>Yeah, yeah, we're upgrading only Flex machines, correct?</v>

00:21:16.598 --> 00:21:17.318
<v Val Levitan>Yes.</v>

00:21:18.078 --> 00:21:21.718
<v Val Levitan>Whatever that number is, 2000, 2 1/2, 3000, I don't know.</v>

00:21:19.878 --> 00:21:23.478
<v Felipe Miranda Giorgi>Yes, yes, yes, whatever it is. Yes, understood, Understood.</v>

00:21:25.318 --> 00:21:29.318
<v Val Levitan>And we're not upgrading games. We're only upgrading that feature.</v>

00:21:27.558 --> 00:21:29.198
<v Felipe Miranda Giorgi>Yeah, yeah, we're not upgrading games.</v>

00:21:34.038 --> 00:21:49.638
<v Pavel Frolov>As we have a big amount of different software, these fixes will require to make changes to these particular versions or to install the latest.</v>

00:21:50.358 --> 00:21:51.158
<v Pavel Frolov>Version.</v>

00:21:52.758 --> 00:21:53.478
<v Pavel Frolov>Uh, Juan.</v>

00:21:55.478 --> 00:21:56.678
<v Pavel Frolov>Cortana, pretty.</v>

00:21:57.958 --> 00:21:58.358
<v Pavel Frolov>Wap.</v>

00:22:02.118 --> 00:22:03.078
<v Pavel Frolov>Don't do a three.</v>

00:22:05.638 --> 00:22:06.438
<v Pavel Frolov>So, lust.</v>

00:22:07.398 --> 00:22:15.878
<v Val Levitan>So then you will do, you will then create 2 versions, one for vertical, one for dual screen.</v>

00:22:17.078 --> 00:22:22.198
<v Pavel Frolov>And install the same games, but the latest software.</v>

00:22:22.998 --> 00:22:23.398
<v Val Levitan>Yeah.</v>

00:22:24.518 --> 00:22:26.838
<v Pavel Frolov>OKOKOKOK, so it.</v>

00:22:25.798 --> 00:22:29.838
<v Val Levitan>I want Felipe, I want Felipe confirmation. Felipe, did you understand what?</v>

00:22:28.998 --> 00:22:33.238
<v Felipe Miranda Giorgi>I, I, yeah, I'm lost there. How, how, how is it that two softwares?</v>

00:22:34.838 --> 00:22:36.278
<v Val Levitan>Let me, let me say this.</v>

00:22:37.398 --> 00:22:38.358
<v Val Levitan>If we...</v>

00:22:39.558 --> 00:22:42.598
<v Val Levitan>Decide to only upgrade.</v>

00:22:44.518 --> 00:22:45.238
<v Val Levitan>The year.</v>

00:22:47.478 --> 00:22:55.318
<v Val Levitan>Reset side of the software and not the games themselves; we need to take each version.</v>

00:22:56.918 --> 00:23:04.198
<v Val Levitan>that we release that's in the field and update, sorry, upgrade that particular version.</v>

00:23:05.318 --> 00:23:11.798
<v Val Levitan>So from, let's say, version very earliest to now, this version that will have.</v>

00:23:05.558 --> 00:23:05.958
<v Felipe Miranda Giorgi>Okay.</v>

00:23:12.678 --> 00:23:15.318
<v Val Levitan>The hard resets removed.</v>

00:23:16.518 --> 00:23:18.358
<v Val Levitan>But only for that version of the game.</v>

00:23:19.558 --> 00:23:24.918
<v Val Levitan>But we have many versions that were released. So I don't know, maybe 10, 20.</v>

00:23:24.838 --> 00:23:25.478
<v Felipe Miranda Giorgi>Yes.</v>

00:23:25.798 --> 00:23:29.558
<v Val Levitan>So we will need 20 upgrades.</v>

00:23:30.678 --> 00:23:42.918
<v Val Levitan>And each upgrade, first we need to know, okay, what version of the software do you need? If you have version A, B, C, I have to give you this one. If you have version X, Y, Z, I have to give you that one.</v>

00:23:34.918 --> 00:23:35.398
<v Pavel Frolov>That was.</v>

00:23:44.838 --> 00:23:51.158
<v Felipe Miranda Giorgi>Yes, yes. Okay, so it's not going to be two, one for dual, one for vertical, but 20.</v>

00:23:50.038 --> 00:23:50.998
<v Val Levitan>No, no.</v>

00:23:51.478 --> 00:23:52.918
<v Pavel Frolov>No, no, no, no, no.</v>

00:23:51.878 --> 00:23:57.318
<v Val Levitan>No, so, so what we're suggesting is to do only two upgrades.</v>

00:23:54.758 --> 00:23:54.838
<v Pavel Frolov>The.</v>

00:23:58.518 --> 00:24:00.678
<v Val Levitan>Not to operate, to pass.</v>

00:24:02.198 --> 00:24:08.838
<v Val Levitan>all of the dual screens, bring them from whatever version it is to the final version to now.</v>

00:24:08.638 --> 00:24:09.078
<v Felipe Miranda Giorgi>Right.</v>

00:24:09.878 --> 00:24:10.118
<v Pavel Frolov>Yeah.</v>

00:24:09.958 --> 00:24:14.358
<v Val Levitan>and all the vertical games from earlier version to now.</v>

00:24:15.718 --> 00:24:16.278
<v Felipe Miranda Giorgi>Correct.</v>

00:24:15.798 --> 00:24:19.398
<v Val Levitan>But that will require game changes as well.</v>

00:24:21.598 --> 00:24:26.758
<v Val Levitan>which might be problematic for you because some people like pitch one, pitch two.</v>

00:24:26.278 --> 00:24:30.838
<v Felipe Miranda Giorgi>But why would it require all, because we want, I mean, only one.</v>

00:24:32.518 --> 00:24:33.078
<v Felipe Miranda Giorgi>Okay.</v>

00:24:37.158 --> 00:24:39.958
<v Felipe Miranda Giorgi>To the latest one, meaning peach 3, Val.</v>

00:24:42.158 --> 00:24:46.118
<v Felipe Miranda Giorgi>For dual, for example, which is our latest release.</v>

00:24:48.278 --> 00:24:49.238
<v Val Levitan>I don't know.</v>

00:24:50.278 --> 00:25:10.398
<v Felipe Miranda Giorgi>I don't think that's a good idea. Listen, what we did before is we took page one, page two, page three, and we made the newer versions with the nudge and the watchdog and all this. And those are, we would have one, two, three, 4, 5, 5 versions total.</v>

00:25:10.958 --> 00:25:29.438
<v Felipe Miranda Giorgi>Three for dual, 2 for vertical. Has everyone updated the software? No. And it's been slowing down because I haven't pushed it. Because with Val, we had a conversation, those customers that have 1919 software, which is</v>

00:25:29.678 --> 00:25:47.438
<v Felipe Miranda Giorgi>For you, for you, the build is 1919. Those, they don't complain much about machines freezing or anything, and we have the highest performance from all the different versions, so...</v>

00:25:49.358 --> 00:25:51.598
<v Felipe Miranda Giorgi>I don't know if up upgrading them.</v>

00:25:54.238 --> 00:25:55.118
<v Felipe Miranda Giorgi>Would be.</v>

00:25:56.318 --> 00:25:59.998
<v Felipe Miranda Giorgi>I mean, it would be a challenge, yes, to get everyone on board.</v>

00:26:01.518 --> 00:26:10.078
<v Felipe Miranda Giorgi>Yes, a lot of work. And we can have the best intentions, but unless they move it, it won't happen.</v>

00:26:04.358 --> 00:26:04.558
<v Pavel Frolov>Egm.</v>

00:26:06.558 --> 00:26:07.198
<v Val Levitan>So...</v>

00:26:12.238 --> 00:26:25.038
<v Val Levitan>Well, that's going to happen with every, regardless which software we give them. I mean, I mean, I think we're discussing two different things. You're saying...</v>

00:26:18.638 --> 00:26:18.758
<v Pavel Frolov>Yeah.</v>

00:26:19.518 --> 00:26:20.078
<v Felipe Miranda Giorgi>Right.</v>

00:26:26.638 --> 00:26:33.118
<v Val Levitan>Your Felipe is saying it doesn't matter what I will give them, it will be a challenge of upgrading.</v>

00:26:29.798 --> 00:26:29.918
<v Pavel Frolov>The.</v>

00:26:34.238 --> 00:26:35.998
<v Val Levitan>But Pavel is saying, well...</v>

00:26:38.638 --> 00:26:46.318
<v Val Levitan>Do I upgrade every single version separately, one by one? By the way, this will require approvals.</v>

00:26:43.758 --> 00:26:44.318
<v Felipe Miranda Giorgi>No.</v>

00:26:47.758 --> 00:26:50.398
<v Val Levitan>So there's a difference, 20 approvals.</v>

00:26:51.758 --> 00:26:53.518
<v Val Levitan>Or 2 approvals.</v>

00:26:54.718 --> 00:26:55.198
<v Felipe Miranda Giorgi>Yeah.</v>

00:26:56.158 --> 00:26:57.038
<v Felipe Miranda Giorgi>I understand.</v>

00:27:00.878 --> 00:27:09.518
<v Pavel Frolov>And of course, this update of software will add additional feature to enable modem.</v>

00:27:11.118 --> 00:27:21.598
<v Pavel Frolov>Even if this is an old software, I assume that we can make upgrade and allow additional option if you install modem.</v>

00:27:21.278 --> 00:27:25.998
<v Felipe Miranda Giorgi>Even, even if the boards are five years old, they'll OK.</v>

00:27:24.638 --> 00:27:25.678
<v Pavel Frolov>Yes, yes.</v>

00:27:50.958 --> 00:27:58.718
<v Irina Shishko>Stop them.</v>

00:28:02.638 --> 00:28:20.958
<v Pavel Frolov>Yeah, in a sense that we need to decide how to release a newer version for dual machine dual screen machines, either to release as one file with speech 1 + 2 + 3, or keep them as a different.</v>

00:28:21.038 --> 00:28:21.758
<v Pavel Frolov>Releases.</v>

00:28:24.478 --> 00:28:40.638
<v Pavel Frolov>From the perspective of getting certificates, the cheaper is to get one bundle with 18 games within one package.</v>

00:28:28.238 --> 00:28:28.878
<v Felipe Miranda Giorgi>Wow.</v>

00:28:43.358 --> 00:28:48.638
<v Felipe Miranda Giorgi>Yes, that would be ideal. And if the RIS would be saved.</v>

00:28:49.678 --> 00:28:52.158
<v Felipe Miranda Giorgi>And after a soft reset,</v>

00:28:53.718 --> 00:28:53.958
<v Pavel Frolov>And...</v>

00:28:55.278 --> 00:29:03.438
<v Pavel Frolov>No, this will not work this way. For newer version, we still need to generate new.</v>

00:29:06.798 --> 00:29:10.158
<v Pavel Frolov>generate new arrays for this particular version.</v>

00:29:10.718 --> 00:29:13.198
<v Felipe Miranda Giorgi>Yes, yes, for the first time.</v>

00:29:13.678 --> 00:29:14.958
<v Pavel Frolov>Yes, yes, for the first time.</v>

00:29:14.798 --> 00:29:17.278
<v Felipe Miranda Giorgi>But after that, it will save it.</v>

00:29:17.518 --> 00:29:18.158
<v Pavel Frolov>Yes.</v>

00:29:18.478 --> 00:29:34.158
<v Felipe Miranda Giorgi>And for future problems, they will have it the new way. But it would be that the technicians wouldn't have to run around with Peach 1 software, Peach 2 software, and Peach 3 software, but they would have them all in one.</v>

00:29:22.518 --> 00:29:22.958
<v Pavel Frolov>Yes.</v>

00:29:35.438 --> 00:29:36.158
<v Felipe Miranda Giorgi>Dongle.</v>

00:29:36.958 --> 00:29:37.358
<v Pavel Frolov>Yeah.</v>

00:29:37.278 --> 00:29:46.718
<v Felipe Miranda Giorgi>And we simply give them the first RIS. This is for this machine, right? Loads them up.</v>

00:29:48.238 --> 00:29:54.238
<v Felipe Miranda Giorgi>And if we could add to that release the...</v>

00:29:56.798 --> 00:30:04.478
<v Felipe Miranda Giorgi>manual change of printer, no printer to avoid another hard reset.</v>

00:30:05.358 --> 00:30:06.718
<v Felipe Miranda Giorgi>I think that's...</v>

00:30:07.838 --> 00:30:09.918
<v Felipe Miranda Giorgi>That's very positive.</v>

00:30:12.899 --> 00:30:16.139
<v Felipe Miranda Giorgi>35 обвинения, проведения цифра.</v>

00:30:16.819 --> 00:30:20.459
<v Felipe Miranda Giorgi>What dango WW witing games.</v>

00:30:22.929 --> 00:30:29.489
<v Felipe Miranda Giorgi>Юнир и вывод не 3.</v>

00:30:30.619 --> 00:30:34.979
<v Felipe Miranda Giorgi>Уанфорда миллион форвард пичт.</v>

00:30:35.205 --> 00:30:35.565
<v Felipe Miranda Giorgi>Echo.</v>

00:30:36.685 --> 00:30:37.325
<v Felipe Miranda Giorgi>Correct.</v>

00:30:39.805 --> 00:30:40.285
<v Pavel Frolov>Ohh.</v>

00:30:42.125 --> 00:30:43.085
<v Pavel Frolov>Yeah, yes.</v>

00:30:45.885 --> 00:30:48.845
<v Felipe Miranda Giorgi>And then one for mega hits, but that's a different story.</v>

00:30:47.565 --> 00:30:48.125
<v Pavel Frolov>You.</v>

00:30:50.525 --> 00:30:50.565
<v Felipe Miranda Giorgi>I.</v>

00:31:18.925 --> 00:31:21.365
<v Irina Shishko>I do.</v>

00:31:22.981 --> 00:31:32.581
<v Irina Shishko>Что набор машин говорим, что это будто для вот таких вот машин этот рис, то есть мы там и сохраняем номер машины.</v>

00:31:33.661 --> 00:31:42.861
<v Irina Shishko>И это самое мы не привязываемся к тому. Это сколько там этих машин, как у нас там есть 3 машины в банке 6 машин там скай.</v>

00:31:44.101 --> 00:31:45.341
<v Irina Shishko>18.</v>

00:31:51.591 --> 00:31:55.641
<v Pavel Frolov>Ну а чем это отличается от Того, что сейчас на одну флешку записываешь несколько рисов?</v>

00:31:57.421 --> 00:32:04.631
<v Irina Shishko>Один рис и просто это самое нет. Вот да можно так мы делаем на каждую машину рис.</v>

00:32:04.701 --> 00:32:13.581
<v Irina Shishko>И это самое тут больше, наверное, Филипп и облегчается жизнь, потому что он делает инсталляции, потом их туда отправляют и говорит, вот запишите на.</v>

00:32:13.941 --> 00:32:15.221
<v Irina Shishko>Эту флешку.</v>

00:32:17.201 --> 00:32:20.241
<v Irina Shishko>А если у нас один рис и просто список машин.</v>

00:32:22.101 --> 00:32:27.021
<v Irina Shishko>То есть ли машина видит, что есть её номер? Она этот рис себе забирает и всё.</v>

00:32:27.981 --> 00:32:29.181
<v Irina Shishko>И не нужно делать.</v>

00:32:30.741 --> 00:32:31.981
<v Irina Shishko>Много инсталляций.</v>

00:32:37.281 --> 00:32:40.031
<v Pavel Frolov>Ну это переделка инсталляции это.</v>

00:32:40.871 --> 00:32:43.591
<v Irina Shishko>Ну это если небольшая, это самое переделка.</v>

00:32:44.221 --> 00:32:49.061
<v Irina Shishko>Это вот эти, если bank инсталляции посмотреть.</v>

00:32:51.831 --> 00:32:53.711
<v Irina Shishko>Но это как только.</v>

00:32:54.341 --> 00:32:55.701
<v Irina Shishko>Просто то, что пришло.</v>

00:32:58.871 --> 00:33:00.711
<v Irina Shishko>А головы на сколько это?</v>

00:33:06.411 --> 00:33:10.211
<v Irina Shishko>Но нам нужно переделывать инсталляции.</v>

00:33:11.261 --> 00:33:15.541
<v Irina Shishko>Всё равно как то, чтобы с паспортом они там не конфликтовали.</v>

00:33:18.631 --> 00:33:21.991
<v Irina Shishko>Дальше нам нужно переделывать.</v>

00:33:23.381 --> 00:33:26.781
<v Irina Shishko>Чтобы мы полизе получали только lestot.</v>

00:33:27.501 --> 00:33:29.301
<v Irina Shishko>И никаких статистик.</v>

00:33:32.591 --> 00:33:32.751
<v Irina Shishko>А.</v>

00:33:43.351 --> 00:33:46.191
<v Irina Shishko>И если делается, например.</v>

00:33:47.661 --> 00:33:52.781
<v Irina Shishko>Нет модема пока если, например, делается facetory reset.</v>

00:33:54.461 --> 00:34:12.581
<v Irina Shishko>Нужно ли нам отправлять статистику? То есть там у нас тоже есть вот этот вот флажок, который говорит запрашивать отображать QR код, чтобы в статистику отправить или не отображать. Ну то есть это достаточно просто регулируется сейчас уже в текущем рейсе.</v>

00:34:14.571 --> 00:34:15.491
<v Irina Shishko>Нужно она.</v>

00:34:15.441 --> 00:34:18.961
<v Pavel Frolov>Филиппа заквещен.</v>

00:34:16.821 --> 00:34:17.311
<v Felipe Miranda Giorgi>Час.</v>

00:34:20.391 --> 00:34:25.511
<v Pavel Frolov>Карентли в mashion recvester to make facetory reseat.</v>

00:34:27.791 --> 00:34:28.631
<v Pavel Frolov>Кюар.</v>

00:34:29.261 --> 00:34:32.621
<v Pavel Frolov>Усенз глаз статистик will be shown.</v>

00:34:36.031 --> 00:34:40.751
<v Pavel Frolov>Бат экчелль викен, removesy s Victoria.</v>

00:34:41.941 --> 00:34:45.941
<v Pavel Frolov>Frolksamp, пол your chats perfomen factory reseat.</v>

00:34:46.941 --> 00:34:50.901
<v Pavel Frolov>Энд lost all the accountsindata.</v>

00:34:52.061 --> 00:34:55.861
<v Pavel Frolov>Пациейнг тайм энд вод здесь скринс вис.</v>

00:34:57.791 --> 00:34:58.511
<v Pavel Frolov>Кюарс.</v>

00:35:00.731 --> 00:35:01.331
<v Pavel Frolov>Вот и.</v>

00:35:05.461 --> 00:35:05.861
<v Pavel Frolov>Угу.</v>

00:35:05.901 --> 00:35:08.621
<v Felipe Miranda Giorgi>Youmia posting poten.</v>

00:35:13.551 --> 00:35:13.951
<v Pavel Frolov>Лес.</v>

00:35:16.141 --> 00:35:16.701
<v Felipe Miranda Giorgi>Номер.</v>

00:35:21.781 --> 00:35:28.021
<v Felipe Miranda Giorgi>Арнольд чейни бараповый синий гонки войск югера фордевым.</v>

00:35:25.451 --> 00:35:25.691
<v Pavel Frolov>Да.</v>

00:35:27.281 --> 00:35:27.521
<v Irina Shishko>Угу.</v>

00:35:34.661 --> 00:35:35.061
<v Irina Shishko>А ты?</v>

00:35:52.401 --> 00:35:53.641
<v Felipe Miranda Giorgi>Только я соу.</v>

00:35:52.701 --> 00:35:55.221
<v Pavel Frolov>Здесь ноты проблем. Yes yes.</v>

00:35:52.891 --> 00:35:53.131
<v Irina Shishko>Ох.</v>

00:35:56.661 --> 00:35:57.221
<v Irina Shishko>Окей.</v>

00:35:59.541 --> 00:36:06.861
<v Felipe Miranda Giorgi>No, no no srines sex ten de delts baryder frees for fore change.</v>

00:36:06.981 --> 00:36:07.861
<v Felipe Miranda Giorgi>Dech oder?</v>

00:36:08.981 --> 00:36:14.221
<v Felipe Miranda Giorgi>Every thind whidow we hove deoder.</v>

00:36:15.501 --> 00:36:21.661
<v Felipe Miranda Giorgi>Sum sergery bittes bat sat sant thind tarset serger i wost thind mort.</v>

00:36:25.701 --> 00:36:31.311
<v Irina Shishko>Паша мы не можем там пересмотреть, чтобы меньше выводить этих самых, как было раньше для паспорта.</v>

00:36:32.031 --> 00:36:38.431
<v Irina Shishko>Он на старых версиях было 4, потом сделали сколько там 4 на 4 16.</v>

00:36:40.031 --> 00:36:40.591
<v Irina Shishko>Кот.</v>

00:36:41.051 --> 00:36:45.431
<v Pavel Frolov>Это именно это именно для паспорта делалось, чтобы корректно.</v>

00:36:45.981 --> 00:36:47.181
<v Pavel Frolov>Номер передавать?</v>

00:36:48.471 --> 00:36:48.671
<v Irina Shishko>Угу.</v>

00:36:57.671 --> 00:36:58.551
<v Pavel Frolov>Ну.</v>

00:37:03.841 --> 00:37:04.561
<v Pavel Frolov>Соу.</v>

00:37:05.421 --> 00:37:08.981
<v Pavel Frolov>Ой зэт кэнби danes.</v>

00:37:11.001 --> 00:37:14.591
<v Pavel Frolov>Forst MVPIC.</v>

00:37:16.745 --> 00:37:21.225
<v Pavel Frolov>Remove statistics from scanning Lease.</v>

00:37:22.505 --> 00:37:25.865
<v Pavel Frolov>Point #1, point #2.</v>

00:37:26.985 --> 00:37:30.105
<v Pavel Frolov>Remove passport QR screen.</v>

00:37:31.705 --> 00:37:38.825
<v Pavel Frolov>after factory reset and move this data to next to our</v>

00:37:39.945 --> 00:37:54.745
<v Pavel Frolov>scan procedures. For example, if you are just going to location to transfer location statistics from all the machines. Point #3.</v>

00:37:59.785 --> 00:38:02.905
<v Pavel Frolov>Make some changes related to.</v>

00:38:09.065 --> 00:38:26.265
<v Pavel Frolov>To enable change of some components within remote initial setup. For example, if remote initial setup created this without printer, but location decided to use printer,</v>

00:38:26.905 --> 00:38:31.945
<v Pavel Frolov>To allow this change during initial setup.</v>

00:38:37.665 --> 00:38:43.985
<v Pavel Frolov>So, it takes not only machine changes, but also serial.</v>

00:38:45.465 --> 00:38:46.385
<v Pavel Frolov>And.</v>

00:38:47.985 --> 00:38:48.265
<v Pavel Frolov>Mm.</v>

00:38:49.705 --> 00:38:56.345
<v Pavel Frolov>The next idea about soft factory reset looks quite difficult.</v>

00:38:58.185 --> 00:39:00.985
<v Pavel Frolov>and requires some investigation.</v>

00:39:10.785 --> 00:39:14.185
<v Pavel Frolov>Ah, of course, point #4.</v>

00:39:15.945 --> 00:39:16.825
<v Pavel Frolov>Enable.</v>

00:39:18.265 --> 00:39:21.465
<v Pavel Frolov>Reuse lastly applied RIS.</v>

00:39:21.625 --> 00:39:22.345
<v Irina Shishko>Mhm.</v>

00:39:22.545 --> 00:39:26.985
<v Pavel Frolov>If this, if the same version left on the machine.</v>

00:39:29.225 --> 00:39:38.265
<v Pavel Frolov>And the.5 will be investigations connected with software reset.</v>

00:39:44.465 --> 00:39:52.185
<v Pavel Frolov>Probably logic will be like Val explained if we are getting.</v>

00:39:54.425 --> 00:39:57.785
<v Pavel Frolov>Let's say two or three reboots with the same.</v>

00:39:59.145 --> 00:39:59.945
<v Pavel Frolov>*******.</v>

00:40:02.585 --> 00:40:03.945
<v Pavel Frolov>Same, same error.</v>

00:40:06.425 --> 00:40:12.585
<v Pavel Frolov>Then probably to do automatic soft factory reset.</v>

00:40:13.945 --> 00:40:20.025
<v Pavel Frolov>Clearing some known critical data, like meters.</v>

00:40:22.505 --> 00:40:24.505
<v Pavel Frolov>Left meters and left.</v>

00:40:23.545 --> 00:40:26.585
<v Val Levitan>Site, silent, silent percent.</v>

00:40:27.225 --> 00:40:32.185
<v Pavel Frolov>Yes, without any participation of third party.</v>

00:40:34.585 --> 00:40:36.825
<v Pavel Frolov>Okay, this is 0.5.</v>

00:40:36.825 --> 00:40:44.345
<v Felipe Miranda Giorgi>You meant, you meant clearing the meters with the, I mean, silently? Oh, okay. Without clearing the meters. Okay.</v>

00:40:40.225 --> 00:40:40.825
<v Pavel Frolov>No, no.</v>

00:40:41.225 --> 00:40:42.105
<v Irina Shishko>Nsw.</v>

00:40:42.505 --> 00:40:50.825
<v Pavel Frolov>Left meters, left meters, left game settings, clear game history, clear error state.</v>

00:40:52.585 --> 00:40:54.665
<v Pavel Frolov>If it's possible, of course.</v>

00:40:54.905 --> 00:40:57.625
<v Val Levitan>But there has to be a record of it.</v>

00:40:58.985 --> 00:41:01.385
<v Val Levitan>That, that you went through silent.</v>

00:41:02.505 --> 00:41:04.105
<v Val Levitan>A soft reset.</v>

00:41:06.985 --> 00:41:09.465
<v Val Levitan>You have to leave a trace of it somehow.</v>

00:41:10.665 --> 00:41:11.145
<v Pavel Frolov>Mhm.</v>

00:41:11.065 --> 00:41:22.905
<v Val Levitan>So either you're in setup mode or maybe there is a QR scan if you want to, the transfer that silent reset, the fact that it has taken place.</v>

00:41:11.825 --> 00:41:12.345
<v Irina Shishko>Mhm.</v>

00:41:16.545 --> 00:41:16.905
<v Pavel Frolov>Ach.</v>

00:41:25.865 --> 00:41:26.505
<v Pavel Frolov>Okay.</v>

00:41:26.025 --> 00:41:29.225
<v Val Levitan>And Felipe, I just want to let you know that all of this...</v>

00:41:30.905 --> 00:41:34.185
<v Val Levitan>is called patching. It's not really fixing.</v>

00:41:36.745 --> 00:41:41.545
<v Val Levitan>So fixing, for example, is moving people to a modem.</v>

00:41:44.705 --> 00:41:46.025
<v Val Levitan>That is a progress.</v>

00:41:49.305 --> 00:41:49.785
<v Felipe Miranda Giorgi>Okay.</v>

00:42:00.265 --> 00:42:12.665
<v Felipe Miranda Giorgi>Now, I'm a little concerned about, and yeah, but this is not related a little bit, but the modem working everywhere, even in locations with very bad connectivity.</v>

00:42:13.945 --> 00:42:15.465
<v Felipe Miranda Giorgi>There's no concern about that.</v>

00:42:17.625 --> 00:42:19.305
<v Val Levitan>There is a concern, of course.</v>

00:42:17.705 --> 00:42:18.105
<v Felipe Miranda Giorgi>From...</v>

00:42:20.025 --> 00:42:20.505
<v Felipe Miranda Giorgi>Okay.</v>

00:42:21.065 --> 00:42:25.625
<v Val Levitan>Of course there is a concern. How can we not be concerned with model not connecting?</v>

00:42:27.545 --> 00:42:41.785
<v Val Levitan>Number one, we don't know to which extent it will be. Also, is it 24-7, 365 or is it spotty? Because it could be change of weather, it could be, I don't know.</v>

00:42:27.585 --> 00:42:27.785
<v Pavel Frolov>Yeah.</v>

00:42:43.705 --> 00:43:02.425
<v Val Levitan>weakness of the signal, interferences that come and go. Maybe when the fridge starts on a location, it creates electromagnetic interference and we don't have a reception. But when the fridge is off, maybe there is a reception. I don't know.</v>

00:43:03.945 --> 00:43:04.505
<v Felipe Miranda Giorgi>Okay.</v>

00:43:05.145 --> 00:43:14.425
<v Val Levitan>But of course, it's and and also maybe maybe if you find limited amount of locations with bad reception.</v>

00:43:15.505 --> 00:43:18.505
<v Val Levitan>Maybe we can put an amplifier.</v>

00:43:19.945 --> 00:43:23.305
<v Val Levitan>Cellular retransmitter, cellular amplifier.</v>

00:43:24.185 --> 00:43:42.345
<v Val Levitan>For example, when I built a hotel in downtown Toronto, certain floors, certain areas just did not have any reception because of the amount of concrete and reinforcement rebar in the building. So in those areas, we installed</v>

00:43:44.425 --> 00:43:47.145
<v Val Levitan>cellular amplifiers.</v>

00:43:48.345 --> 00:43:51.065
<v Val Levitan>And that worked just fine, so...</v>

00:43:50.345 --> 00:43:50.665
<v Felipe Miranda Giorgi>Okay.</v>

00:43:52.145 --> 00:44:04.505
<v Val Levitan>Do I think it's a fixable problem? I think so. I mean, if you're not getting transmission from a machine constantly, I would send a technician and install a $300 amplifier.</v>

00:44:05.785 --> 00:44:06.185
<v Felipe Miranda Giorgi>Okay.</v>

00:44:09.465 --> 00:44:13.785
<v Val Levitan>Or maybe have that machine permanently off, like, I mean, you know.</v>

00:44:32.665 --> 00:44:36.025
<v Pavel Frolov>Point number six, I think it's not very...</v>

00:44:38.105 --> 00:44:38.905
<v Pavel Frolov>Difficult.</v>

00:44:41.945 --> 00:44:45.065
<v Pavel Frolov>As you asked last time.</v>

00:44:45.985 --> 00:44:53.465
<v Pavel Frolov>To provide more information about devices not found during installation or during boot.</v>

00:44:56.585 --> 00:45:13.545
<v Pavel Frolov>If you remember, Felipe, in some cases, a machine cannot be booted due to counter board, not connected or IO board. It was reported in general, hardware not detected. We will split this.</v>

00:44:58.145 --> 00:44:58.745
<v Felipe Miranda Giorgi>Yes.</v>

00:45:14.585 --> 00:45:15.625
<v Felipe Miranda Giorgi>Yeah, and we...</v>

00:45:17.225 --> 00:45:33.305
<v Felipe Miranda Giorgi>I mean, there was a firmware that you guys gave us to install on machines to prevent this from happening. We rolled it out to as much as we could. I don't know if it's everywhere now, but whenever we get IO devices not found.</v>

00:45:34.265 --> 00:45:49.225
<v Felipe Miranda Giorgi>Board here with that problem, we always install the firmware, so it goes with the firmware, and this also helps, you know, those that are out there, but, and we, we...</v>

00:45:50.665 --> 00:46:02.185
<v Felipe Miranda Giorgi>And I think Genadi suggested moving the connection of the IO board from the original port it was connected to to the one under the IO board. This seems to help a lot.</v>

00:46:03.345 --> 00:46:03.825
<v Pavel Frolov>Mhm.</v>

00:46:05.545 --> 00:46:07.225
<v Felipe Miranda Giorgi>I mean a hardware fix, yeah.</v>

00:46:14.105 --> 00:46:14.665
<v Pavel Frolov>Okay.</v>

00:46:14.425 --> 00:46:33.305
<v Felipe Miranda Giorgi>The other one was the error code 2 and error code 3 during boot up. I don't know if this is something we want to discuss now about, but when we load software and we get that error, it frustrates people so much because they cannot get the machine up and running when we do have to do a hard reset.</v>

00:46:35.465 --> 00:46:45.225
<v Pavel Frolov>I think we can change a little bit spelling, saying that cannot read data from your USB stick, something like this.</v>

00:46:46.825 --> 00:46:49.145
<v Felipe Miranda Giorgi>But is it the USB stick?</v>

00:46:50.265 --> 00:46:51.705
<v Pavel Frolov>In most cases, yes.</v>

00:46:52.425 --> 00:47:01.465
<v Felipe Miranda Giorgi>Because I, I mean, we've seen cases where, I mean, we see a lot of cases where they use the USB stick on this machine, they go to the next machine and it stops working.</v>

00:47:03.225 --> 00:47:07.465
<v Pavel Frolov>It's just read the error from the stick, so...</v>

00:47:07.065 --> 00:47:07.625
<v Felipe Miranda Giorgi>Okay.</v>

00:47:10.425 --> 00:47:13.545
<v Pavel Frolov>Actually, we can just change spelling.</v>

00:47:14.185 --> 00:47:26.665
<v Felipe Miranda Giorgi>Now, are there any specific USB sticks that we should be getting for software? Any specs that you can share? Speed? I don't know. Maybe I'm buying the wrong ones. I don't know.</v>

00:47:24.385 --> 00:47:42.185
<v Pavel Frolov>No, no, no. Any suggestions, actually. Any, any USB stick producers, sometimes they work perfect, sometimes they become a...</v>

00:47:43.705 --> 00:47:44.265
<v Felipe Miranda Giorgi>Okay.</v>

00:47:44.985 --> 00:47:46.265
<v Pavel Frolov>Not so good quality.</v>

00:47:46.585 --> 00:47:47.385
<v Felipe Miranda Giorgi>Understood.</v>

00:47:59.145 --> 00:48:01.065
<v Pavel Frolov>Seems that's a full deed.</v>

00:48:00.345 --> 00:48:02.905
<v Felipe Miranda Giorgi>I had, I don't know, I, I...</v>

00:48:01.665 --> 00:48:02.185
<v Irina Shishko>Mhm.</v>

00:48:06.305 --> 00:48:28.305
<v Felipe Miranda Giorgi>I had another idea, but it might not, it might be cheaper than what we're doing now, but you know, the fact that the RIS, if the RIS could live inside the cabinet permanently and only technicians having to connect and disconnect to.</v>

00:48:28.425 --> 00:48:29.865
<v Felipe Miranda Giorgi>Load the RIS.</v>

00:48:32.745 --> 00:48:53.265
<v Felipe Miranda Giorgi>It would never be lost. Of course, you would have to update it if anything changes. But if, I don't know, I imagine if we could create a way in which to keep the RIS USB stick or some sort of stick or some, I don't know what, like if it were a Dallas chip that is always there.</v>

00:48:54.585 --> 00:49:02.745
<v Felipe Miranda Giorgi>and they just simply connect and load, that would solve the issue too without redoing a lot of the...</v>

00:49:03.865 --> 00:49:10.025
<v Felipe Miranda Giorgi>the stuff that we're talking about, but if we can save it in the system, that's fine too.</v>

00:49:11.385 --> 00:49:20.905
<v Felipe Miranda Giorgi>I'm just concerned that if there's not enough internet for that particular moment, and we don't have a backup, a physical backup like the USB.</v>

00:49:11.625 --> 00:49:12.345
<v Pavel Frolov>Yeah, I think...</v>

00:49:19.625 --> 00:49:23.785
<v Val Levitan>Maybe, maybe, maybe it's not a bad, maybe it's not a bad idea.</v>

00:49:25.625 --> 00:49:26.985
<v Val Levitan>That's an interesting idea.</v>

00:49:38.025 --> 00:49:45.545
<v Val Levitan>So, you're saying that when we configure a machine and we download the RIS?</v>

00:49:46.345 --> 00:49:51.545
<v Val Levitan>We keep this RIS in where? In the memory of the machine?</v>

00:49:50.465 --> 00:50:11.945
<v Felipe Miranda Giorgi>When I deliver machines, the USB stick is attached to the side of the cabinet, but you have to remove it. Although we have the extensor, right, the USB extensor to connect it, they shouldn't remove it from where it's hanging, but they do remove it.</v>

00:50:12.345 --> 00:50:26.505
<v Felipe Miranda Giorgi>Right? They connect it, and sometimes it doesn't read, so they have to open the board and connect it in another port. But if somehow it could live inside the board,</v>

00:50:28.505 --> 00:50:40.585
<v Felipe Miranda Giorgi>I don't know. It's simply connected like a piece of hardware that would solve the issue. And in case there's no internet, there's always a manual way to do it.</v>

00:50:42.505 --> 00:50:44.025
<v Felipe Miranda Giorgi>To load the settings.</v>

00:50:56.425 --> 00:50:56.825
<v Pavel Frolov>Yeah.</v>

00:50:58.105 --> 00:51:05.145
<v Pavel Frolov>The difficulty here begins when you need to update.</v>

00:51:05.545 --> 00:51:08.985
<v Felipe Miranda Giorgi>The update that board, yeah, that's a problem, yes.</v>

00:51:06.305 --> 00:51:14.425
<v Pavel Frolov>AR, yes, yeah, it will be more difficult, difficult process than than right now.</v>

00:51:16.905 --> 00:51:17.545
<v Pavel Frolov>Oh.</v>

00:51:16.985 --> 00:51:22.745
<v Felipe Miranda Giorgi>And believe me, I've tried everything. I bought Amazon some...</v>

00:51:24.425 --> 00:51:43.465
<v Felipe Miranda Giorgi>some adapters for iPhones, Type C and Lightning and all. And I distributed them to technicians, so they always have somehow to load the settings. I send them the settings via WhatsApp, and it has worked many times. And they update it on the phone because the connector helps.</v>

00:51:43.945 --> 00:51:44.345
<v Felipe Miranda Giorgi>But...</v>

00:51:45.225 --> 00:51:48.265
<v Felipe Miranda Giorgi>I mean, something like that would be...</v>

00:51:48.185 --> 00:51:48.585
<v Pavel Frolov>Um...</v>

00:51:49.865 --> 00:52:03.465
<v Felipe Miranda Giorgi>Val, may I share what I know that, for example, I know we don't want to go back, but for example, what they are doing, for example, for aristocrat, they set up the machine.</v>

00:52:04.425 --> 00:52:23.905
<v Felipe Miranda Giorgi>The first technician sets up the machine, configures, then has a USB stick, sticks it in, saves this configuration on this machine. And if he ever needs to configure a machine the same way or in the same location or the same area, he takes this one and he simply loads it.</v>

00:52:24.665 --> 00:52:26.185
<v Felipe Miranda Giorgi>So he copies it from the...</v>

00:52:24.745 --> 00:52:36.825
<v Val Levitan>Yes, it's a, yes, it's a, they liked our idea. They couldn't implement it. And so they did it. In Russian, it's called Cherez Zhukova.</v>

00:52:38.425 --> 00:52:44.905
<v Felipe Miranda Giorgi>In Spanish is chambon. Sounds similar. I get the point. Okay, but...</v>

00:52:41.185 --> 00:52:41.705
<v Pavel Frolov>This is.</v>

00:52:41.465 --> 00:52:41.865
<v Irina Shishko>Thank you.</v>

00:52:44.705 --> 00:52:51.065
<v Val Levitan>Basically, basically, instead of right way, they did it through the rearrange.</v>

00:52:51.585 --> 00:52:52.665
<v Felipe Miranda Giorgi>Uh-huh. OK.</v>

00:52:53.305 --> 00:52:54.425
<v Val Levitan>Call Chudzinau.</v>

00:52:56.105 --> 00:52:58.905
<v Val Levitan>So now you know 2 words.</v>

00:52:56.145 --> 00:52:56.665
<v Pavel Frolov>Mhm.</v>

00:52:58.905 --> 00:53:00.745
<v Felipe Miranda Giorgi>But that's, yeah, I wrote it.</v>

00:53:03.945 --> 00:53:10.585
<v Val Levitan>Usually, when you do things, usually when you do things, this death comes very quickly after that.</v>

00:53:04.265 --> 00:53:05.145
<v Irina Shishko>But, through.</v>

00:53:18.505 --> 00:53:20.745
<v Felipe Miranda Giorgi>Okay, well, anyway, I don't know if...</v>

00:53:21.825 --> 00:53:29.385
<v Felipe Miranda Giorgi>you know, but somehow to attach to so that they don't remove it, that would be ideal, but I get the point of updating this.</v>

00:53:28.505 --> 00:53:49.385
<v Val Levitan>I need to organize these thoughts that Pavel outline by numbers, one, two, three, 4, 5, 10. I need to organize it in a way that it makes sense what needs to be done. Because right now, kind of, I cannot comprehend what needs to be done. I don't have the...</v>

00:53:49.705 --> 00:53:50.665
<v Val Levitan>Grasp of it.</v>

00:53:52.945 --> 00:53:58.345
<v Val Levitan>It's like, I almost need another meeting to groom the final ideas.</v>

00:54:00.745 --> 00:54:01.225
<v Pavel Frolov>OK.</v>

00:54:01.305 --> 00:54:01.545
<v Irina Shishko>PIN.</v>

00:54:01.705 --> 00:54:04.265
<v Val Levitan>I'm going to post the transcript here.</v>

00:54:05.425 --> 00:54:07.545
<v Val Levitan>What I would like you, Felipe, to do?</v>

00:54:09.385 --> 00:54:12.345
<v Val Levitan>is to groom everything that we said in the meeting.</v>

00:54:14.025 --> 00:54:15.465
<v Val Levitan>Into.</v>

00:54:16.385 --> 00:54:18.265
<v Val Levitan>Tiny, small.</v>

00:54:19.865 --> 00:54:23.705
<v Val Levitan>written in the ESL type of English.</v>

00:54:24.225 --> 00:54:24.505
<v Felipe Miranda Giorgi>Yeah.</v>

00:54:26.665 --> 00:54:27.785
<v Val Levitan>Compressed.</v>

00:54:30.025 --> 00:54:30.665
<v Val Levitan>Summary.</v>

00:54:31.625 --> 00:54:32.345
<v Felipe Miranda Giorgi>Understood.</v>

00:54:32.985 --> 00:54:39.225
<v Val Levitan>of the changes that need to be done and then from there we need to create.</v>

00:54:41.305 --> 00:54:43.065
<v Val Levitan>New use cases.</v>

00:54:44.265 --> 00:54:45.865
<v Val Levitan>Positive use cases.</v>

00:54:48.105 --> 00:54:51.545
<v Val Levitan>and break those down into new capabilities.</v>

00:54:53.385 --> 00:55:02.985
<v Val Levitan>So if you could do it for our next meeting, Felipe, we would have good progress. Can you do that?</v>

00:55:02.105 --> 00:55:06.425
<v Felipe Miranda Giorgi>Okay. Yes, I will do that. Absolutely. Yes.</v>

00:55:06.105 --> 00:55:08.745
<v Val Levitan>Half an hour, half an hour is good enough for you.</v>

00:55:09.385 --> 00:55:09.785
<v Felipe Miranda Giorgi>No.</v>

00:55:11.225 --> 00:55:15.465
<v Val Levitan>Okay, then, then Monday, Monday, 10 o'clock.</v>

00:55:16.265 --> 00:55:18.265
<v Felipe Miranda Giorgi>Monday, 10 o'clock is good, yeah.</v>

00:55:19.225 --> 00:55:22.265
<v Val Levitan>Okay, so great. Book the meeting with us.</v>

00:55:22.425 --> 00:55:22.985
<v Felipe Miranda Giorgi>Okay.</v>

00:55:23.225 --> 00:55:25.225
<v Val Levitan>For Monday, 10 o'clock, Felipe.</v>

00:55:25.465 --> 00:55:26.105
<v Felipe Miranda Giorgi>Yes, Sir.</v>

00:55:26.585 --> 00:55:40.105
<v Val Levitan>You're acting as a product manager now. Sorry, sorry, you acting, no, you're acting as a product owner. Do you know the difference between product owner? Do you guys know the difference between product owner and product manager?</v>

00:55:29.625 --> 00:55:30.345
<v Felipe Miranda Giorgi>I understand.</v>

00:55:41.385 --> 00:55:41.625
<v Felipe Miranda Giorgi>NI.</v>

00:55:42.825 --> 00:55:44.825
<v Felipe Miranda Giorgi>I think, I think I understand.</v>

00:55:45.225 --> 00:56:04.785
<v Val Levitan>Product owner is an individual who participates in the beginning of the spec in the design and gets it out of the engineering hands into the field and hands it over to a product manager who then manages the product in the field.</v>

00:56:05.625 --> 00:56:07.305
<v Felipe Miranda Giorgi>Okay, oh yeah, okay.</v>

00:56:07.465 --> 00:56:10.345
<v Val Levitan>So, you're acting right now as a product owner?</v>

00:56:11.465 --> 00:56:17.065
<v Val Levitan>You'll get it out of the engineering and you will start adding, start acting as a product manager.</v>

00:56:17.385 --> 00:56:18.025
<v Felipe Miranda Giorgi>Rights.</v>

00:56:18.345 --> 00:56:20.745
<v Val Levitan>Handing it over to Sebastian.</v>

00:56:21.385 --> 00:56:21.865
<v Felipe Miranda Giorgi>Okay.</v>

00:56:21.625 --> 00:56:25.625
<v Val Levitan>And Sebastian will then manage the product in the field.</v>

00:56:26.745 --> 00:56:28.025
<v Felipe Miranda Giorgi>Understood. Yes, sir.</v>

00:56:28.745 --> 00:56:32.025
<v Val Levitan>So, I'm asking you to act as a product owner.</v>

00:56:33.465 --> 00:56:36.425
<v Val Levitan>which would be one's responsibility normally.</v>

00:56:37.385 --> 00:56:39.785
<v Val Levitan>We obviously regret that Juan is not here.</v>

00:56:42.905 --> 00:56:49.625
<v Val Levitan>And your objective is to have a set of capabilities.</v>

00:56:51.465 --> 00:56:54.585
<v Val Levitan>Requirements with acceptance criteria.</v>

00:56:56.265 --> 00:57:14.545
<v Val Levitan>You need to start with use cases. Use cases first lead you into capabilities. Then you explain how the capability works through a set of requirements. A set of requirements will have, each requirement will have a set of acceptance criteria.</v>

00:57:15.985 --> 00:57:18.785
<v Val Levitan>You will hand over the package to Pavel.</v>

00:57:20.145 --> 00:57:31.985
<v Val Levitan>Pavel will hand assign resources to it and negotiate, internally negotiate a set of features for each of the capability.</v>

00:57:31.505 --> 00:57:31.745
<v Pavel Frolov>Shop.</v>

00:57:33.185 --> 00:57:33.665
<v Felipe Miranda Giorgi>Okay.</v>

00:57:34.345 --> 00:57:36.625
<v Val Levitan>A feature becomes a...</v>

00:57:37.905 --> 00:57:40.225
<v Val Levitan>Feature branch in Github.</v>

00:57:41.665 --> 00:57:45.505
<v Val Levitan>which gets cold deposited.</v>

00:57:46.545 --> 00:57:47.185
<v Val Levitan>in there.</v>

00:57:51.185 --> 00:57:51.825
<v Felipe Miranda Giorgi>Understood.</v>

00:57:53.265 --> 00:57:59.905
<v Val Levitan>So I'm expecting a meeting invitation for Monday the 28th for 10 A.m. Eastern Time.</v>

00:58:00.145 --> 00:58:00.865
<v Felipe Miranda Giorgi>Yes, sir.</v>

00:58:02.625 --> 00:58:03.105
<v Pavel Frolov>No.</v>

00:58:03.425 --> 00:58:11.505
<v Val Levitan>And your goal is to have use cases, capabilities, requirement with acceptance criteria for Monday 10 o'clock.</v>

00:58:11.985 --> 00:58:12.705
<v Felipe Miranda Giorgi>Yes, Sir.</v>

00:58:13.345 --> 00:58:18.185
<v Val Levitan>And our objective for the meeting will be to review those in the meeting.</v>

00:58:19.345 --> 00:58:20.545
<v Val Levitan>Thank you very much.</v>

00:58:20.625 --> 00:58:23.905
<v Felipe Miranda Giorgi>Thank you, Val. Thank you, guys. Bye bye.</v>

00:58:20.745 --> 00:58:22.385
<v Pavel Frolov>Thank you, bye.</v>

00:58:22.145 --> 00:58:23.425
<v Irina Shishko>Thank you. Bye.</v>

