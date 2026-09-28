# Raw Transcript — RIS- Capabilities and Requirements Review
**Date:** September 28, 2026, 11:07 AM – 11:36 AM Eastern
**Summary note:** [[Meeting_Notes_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026]]
---
WEBVTT

00:00:07.761 --> 00:00:08.121
<v Felipe Miranda Giorgi>Hello!</v>

00:00:12.201 --> 00:00:15.321
<v Val Levitan>OK, so let's do this.</v>

00:00:16.481 --> 00:00:20.601
<v Val Levitan>Felipe, you playing the role of a product owner.</v>

00:00:22.761 --> 00:00:34.441
<v Val Levitan>Product owner is somebody who understands the market and can clearly state in the form of a capability what does he want the product to be capable of doing.</v>

00:00:35.881 --> 00:00:43.721
<v Val Levitan>The capability is supported by a set of requirements which explains how the capability works.</v>

00:00:45.961 --> 00:00:46.361
<v Felipe Miranda Giorgi>Yes.</v>

00:00:48.161 --> 00:00:50.081
<v Val Levitan>The capability itself.</v>

00:00:51.761 --> 00:00:59.801
<v Val Levitan>When developed by the engineers, it closes, it collapses, and it doesn't exist anymore. It's taken off.</v>

00:01:01.321 --> 00:01:04.041
<v Val Levitan>taken off of the board. It's not there anymore.</v>

00:01:04.841 --> 00:01:09.401
<v Val Levitan>The requirement is something that lives. It continues with the product.</v>

00:01:10.481 --> 00:01:15.801
<v Val Levitan>The acceptance criteria within requirements are written simplistically.</v>

00:01:16.761 --> 00:01:17.961
<v Val Levitan>in basic form.</v>

00:01:19.721 --> 00:01:24.761
<v Val Levitan>And the acceptance criteria is something that allows.</v>

00:01:26.681 --> 00:01:29.641
<v Val Levitan>the QA department to test the product.</v>

00:01:32.921 --> 00:01:37.881
<v Val Levitan>I'm explaining to you this because you're playing the role now. It's not your primary role.</v>

00:01:38.521 --> 00:01:39.241
<v Felipe Miranda Giorgi>Yes.</v>

00:01:41.481 --> 00:01:56.921
<v Val Levitan>Irina and Pavel knows the subject very well. So Pavel will drive the meeting from an engineering perspective. He will demand that the capabilities be clear, simplistic, and very high level.</v>

00:01:58.281 --> 00:01:58.841
<v Felipe Miranda Giorgi>Okay.</v>

00:01:59.321 --> 00:02:03.401
<v Val Levitan>And you, as a product owner, will demand.</v>

00:02:04.561 --> 00:02:05.721
<v Val Levitan>From Pavel.</v>

00:02:06.881 --> 00:02:12.521
<v Val Levitan>understanding of what needs to be done. So Pavel will start explaining to you from an engineering term.</v>

00:02:13.681 --> 00:02:32.121
<v Val Levitan>approximately what he understands the capability is, and you will ask a question or a series of questions of what you think it needs to do. And this is where you find your alignment between product ownership and the engineering group.</v>

00:02:33.401 --> 00:02:34.121
<v Felipe Miranda Giorgi>Understood.</v>

00:02:36.761 --> 00:02:40.841
<v Val Levitan>I have another meeting to attend. I didn't expect this shift.</v>

00:02:42.041 --> 00:02:50.681
<v Val Levitan>So I'm going to leave, but I'm here, I'm present. You guys continue working on it because I really need this done.</v>

00:02:52.201 --> 00:02:52.761
<v Felipe Miranda Giorgi>Okay.</v>

00:02:53.481 --> 00:02:54.361
<v Val Levitan>Go Goya.</v>

00:02:55.241 --> 00:02:56.841
<v Felipe Miranda Giorgi>So, uh...</v>

00:02:58.121 --> 00:03:05.481
<v Felipe Miranda Giorgi>Pavel, I made two different versions, one very simple and like Val says, basically.</v>

00:03:06.441 --> 00:03:21.881
<v Felipe Miranda Giorgi>Very easy, simple to understand. The capability, a simple sentence, and then the requirements of what needs to happen. And also, Sebastian had worked on this for other...</v>

00:03:23.561 --> 00:03:25.641
<v Felipe Miranda Giorgi>Or even similar.</v>

00:03:27.721 --> 00:03:31.801
<v Felipe Miranda Giorgi>Oh, sorry. I don't want this. What the hell?</v>

00:03:31.161 --> 00:03:40.761
<v Val Levitan>Felipe, Felipe, you're blabbing now, you're wasting time. Nobody needs any of it. Capability, requirement, move on.</v>

00:03:41.321 --> 00:03:43.001
<v Felipe Miranda Giorgi>Okay, so...</v>

00:03:42.121 --> 00:03:45.001
<v Val Levitan>Don't, don't, don't build an essay around this.</v>

00:03:45.401 --> 00:03:48.521
<v Felipe Miranda Giorgi>Now, I'm just asking how he prefers to see it in this con.</v>

00:03:47.561 --> 00:03:57.281
<v Val Levitan>You're losing, English is second language for them. You're losing them. They cannot digest every single word you're blubbing around.</v>

00:03:53.161 --> 00:03:53.681
<v Felipe Miranda Giorgi>Okay.</v>

00:03:57.561 --> 00:04:14.441
<v Felipe Miranda Giorgi>Okay, understood. Okay, we need to first capabilities to replace the battery without a factory reset. I've got the description here. The EGM shall allow CPU battery to be replaced without causing a critical error, a factory reset, or a hard reset. Right?</v>

00:03:58.521 --> 00:03:59.081
<v Val Levitan>Goal.</v>

00:04:16.921 --> 00:04:33.801
<v Felipe Miranda Giorgi>The background is that currently a low battery shows a QR code instructing it to scan it. If they don't scan the QR code and the machine for any reason is powered off and they replace the battery, it goes into a critical error.</v>

00:04:34.881 --> 00:04:51.121
<v Felipe Miranda Giorgi>causing it when you replace the battery and you need to actually do a hard reset after this, right? It becomes a 30 minute to two hour outage because of the critical error. What is the acceptance?</v>

00:04:49.641 --> 00:04:55.481
<v Pavel Frolov>Okay, this particular case is clear. Let's switch to next one.</v>

00:04:56.041 --> 00:05:00.441
<v Felipe Miranda Giorgi>OK, and the require you don't need to see the requirements or OK.</v>

00:04:57.481 --> 00:04:58.601
<v Pavel Frolov>Weather is clear.</v>

00:05:03.081 --> 00:05:23.001
<v Felipe Miranda Giorgi>Upgrade software without creating new RIS. The AGM shall keep its configuration where the software is upgraded, so JVL does not need to create a new RIS file for each machine. JVL shall be able to select which machines to upgrade, one, some or all, without deleting or recreating installations in CMS.</v>

00:05:24.521 --> 00:05:29.161
<v Felipe Miranda Giorgi>So right now what we're doing is we have to create every installation per serial number.</v>

00:05:31.801 --> 00:05:50.601
<v Felipe Miranda Giorgi>What I'm suggesting here that we do in CMS or what we believe needs to happen is for the new installation going on to a newer version to take the exact same settings of the previous installation.</v>

00:05:51.001 --> 00:05:55.481
<v Felipe Miranda Giorgi>So that we don't have to repeat the work 2500 times.</v>

00:06:00.921 --> 00:06:01.401
<v Irina Shishko>Ohh.</v>

00:06:05.721 --> 00:06:06.281
<v Pavel Frolov>No.</v>

00:06:10.441 --> 00:06:34.961
<v Irina Shishko>At the motion is deal. It's no.</v>

00:06:35.041 --> 00:06:37.001
<v Irina Shishko>Issue file, Elisa.</v>

00:06:38.121 --> 00:06:56.441
<v Pavel Frolov>Or Irina is saying that probably it's better to write it in sort of two separate capability capability number ones that we discussed previous time about reusing RIS file.</v>

00:06:57.601 --> 00:06:58.921
<v Pavel Frolov>After fact, it is set.</v>

00:07:00.841 --> 00:07:03.401
<v Pavel Frolov>But with the same software reaction.</v>

00:07:02.201 --> 00:07:03.241
<v Felipe Miranda Giorgi>Reusing.</v>

00:07:05.881 --> 00:07:06.761
<v Felipe Miranda Giorgi>I think.</v>

00:07:06.201 --> 00:07:07.641
<v Pavel Frolov>Reusing this.</v>

00:07:11.561 --> 00:07:19.561
<v Pavel Frolov>Yeah, using pre-saved RIS file on the machine without USB stick after factory reset.</v>

00:07:20.761 --> 00:07:25.321
<v Pavel Frolov>ability to apply this area after a fair or...</v>

00:07:24.841 --> 00:07:26.201
<v Felipe Miranda Giorgi>Right, yes.</v>

00:07:27.241 --> 00:07:37.881
<v Pavel Frolov>But the second second one is looks more difficult for implementation because it touches a lot a lot.</v>

00:07:39.401 --> 00:07:42.521
<v Pavel Frolov>Off on server side right now.</v>

00:07:44.201 --> 00:07:51.961
<v Pavel Frolov>It's prohibited and all arrays files relates to particular software version.</v>

00:07:53.161 --> 00:07:54.361
<v Pavel Frolov>After installation, I mean.</v>

00:08:01.321 --> 00:08:05.961
<v Pavel Frolov>But actually, we think that this is possible.</v>

00:08:10.761 --> 00:08:18.281
<v Pavel Frolov>And how much time it will take to implement? I will not be ready to answer this question right now.</v>

00:08:19.721 --> 00:08:20.361
<v Felipe Miranda Giorgi>Okay.</v>

00:08:21.001 --> 00:08:33.801
<v Pavel Frolov>But if it really neat and we decided that this is MVP 1 or MVP 3 on something like this, it can be implemented.</v>

00:08:36.921 --> 00:08:37.401
<v Felipe Miranda Giorgi>Okay.</v>

00:08:41.401 --> 00:08:42.041
<v Felipe Miranda Giorgi>Ohh.</v>

00:08:43.321 --> 00:08:45.001
<v Felipe Miranda Giorgi>Should I move on to the next one?</v>

00:08:46.201 --> 00:08:46.841
<v Pavel Frolov>Ohh, yes.</v>

00:08:50.841 --> 00:08:53.481
<v Felipe Miranda Giorgi>Recover from a boot loop without hard reset.</v>

00:08:54.441 --> 00:09:10.281
<v Felipe Miranda Giorgi>The AGM shall recover itself from a repeated software error boot loop without a hard reset and without a technician. We talked about this last time. Recovery must keep meters, player credits, game settings, and RIS configuration will not require decommission.</v>

00:09:05.161 --> 00:09:05.641
<v Pavel Frolov>Mhm.</v>

00:09:12.521 --> 00:09:20.041
<v Felipe Miranda Giorgi>I understand, I think Irina said that the boot loop is, or this is caused by the watchdog.</v>

00:09:22.281 --> 00:09:27.721
<v Pavel Frolov>Yes, yes, reboots causing by watchdog.</v>

00:09:29.081 --> 00:09:37.721
<v Pavel Frolov>But in case when it was an error on storage, for example.</v>

00:09:39.081 --> 00:09:40.601
<v Pavel Frolov>It will not help us.</v>

00:09:41.881 --> 00:09:44.361
<v Pavel Frolov>Even if we clear some.</v>

00:09:46.121 --> 00:09:51.561
<v Pavel Frolov>some settings on non-volatile memory, make a soft.</v>

00:09:52.841 --> 00:09:55.241
<v Pavel Frolov>Factory reset after this.</v>

00:09:56.761 --> 00:09:58.921
<v Pavel Frolov>In some cases, it will not help us.</v>

00:10:02.441 --> 00:10:02.921
<v Felipe Miranda Giorgi>Mhm.</v>

00:10:02.961 --> 00:10:10.841
<v Pavel Frolov>For example, if some sector fault on HDD or something like this.</v>

00:10:11.961 --> 00:10:14.281
<v Pavel Frolov>On that on database.</v>

00:10:16.521 --> 00:10:25.961
<v Felipe Miranda Giorgi>For example, today, earlier this morning, we had a boot loop case, and it seemed to be something about the printer not connected to power.</v>

00:10:27.481 --> 00:10:35.481
<v Felipe Miranda Giorgi>I don't know if that's the case, but that's what the technician told me. So it's not the watchdog. I don't think that's...</v>

00:10:36.401 --> 00:10:38.041
<v Felipe Miranda Giorgi>That's what's causing the boot loop.</v>

00:10:36.801 --> 00:10:37.321
<v Pavel Frolov>Mhm.</v>

00:10:41.481 --> 00:10:52.521
<v Felipe Miranda Giorgi>And we've seen it before the watchdog was implemented. Like with earlier software versions, we've always seen the boot loop happen again and again.</v>

00:10:58.681 --> 00:11:07.961
<v Pavel Frolov>So the requirement is clear, but implementation is absolutely in the fog. We do not know what we are fixing.</v>

00:11:02.121 --> 00:11:02.321
<v Irina Shishko>No.</v>

00:11:18.521 --> 00:11:19.161
<v Felipe Miranda Giorgi>Okay.</v>

00:11:19.721 --> 00:11:20.041
<v Irina Shishko>Ohh.</v>

00:11:21.721 --> 00:11:27.721
<v Felipe Miranda Giorgi>Well, I have some question. What causes those boot loops we have identified?</v>

00:11:29.481 --> 00:11:30.601
<v Felipe Miranda Giorgi>It could be...</v>

00:11:31.961 --> 00:11:39.241
<v Felipe Miranda Giorgi>the new added watchdog, what else could cause this boot loops when it goes, what other?</v>

00:11:42.841 --> 00:11:44.441
<v Felipe Miranda Giorgi>Hardware power.</v>

00:11:42.841 --> 00:12:01.441
<v Pavel Frolov>Yes, if we write down all the cases, for example, it was not connected printer, and after this, it causes reboot of machine. Okay, we can review.</v>

00:12:01.881 --> 00:12:03.561
<v Pavel Frolov>This is a separate.</v>

00:12:04.681 --> 00:12:06.761
<v Pavel Frolov>Bug or bug bug fix?</v>

00:12:09.321 --> 00:12:12.761
<v Pavel Frolov>But in general, I don't know how to fix it.</v>

00:12:18.561 --> 00:12:30.281
<v Pavel Frolov>If it was some error related to non-volatile memory, we can try to clear some settings, make a soft factory reset.</v>

00:12:31.961 --> 00:12:50.281
<v Pavel Frolov>And after three, after three tries of boot loops, probably we can make a soft factory reset and try to up a machine. But all other cases, again, it's not.</v>

00:12:51.641 --> 00:12:53.881
<v Pavel Frolov>Closely understandable for me.</v>

00:12:58.361 --> 00:13:16.441
<v Felipe Miranda Giorgi>The problem also is that we were speaking with this about this with Sebastian. We, every time we have attempted to get logs from this boot loop situation, we don't get logs because it doesn't load to a point to send any logs.</v>

00:13:15.401 --> 00:13:15.721
<v Sebastian Cortes>Hey.</v>

00:13:17.721 --> 00:13:31.801
<v Felipe Miranda Giorgi>And every time it reboots it, like you say, it doesn't help because the information is missing. So how can we investigate all possible cases of boot looping? It's complicated.</v>

00:13:30.841 --> 00:13:36.281
<v Val Levitan>But don't forget that we are switching to cell modem right now.</v>

00:13:39.801 --> 00:13:43.401
<v Val Levitan>And I think we might be addressing it somehow differently.</v>

00:13:51.361 --> 00:14:10.561
<v Pavel Frolov>Actually, I do understand. I do understand that working on this capability, at least during next our steps, we can implement some additional logging, for example, and the ability to get logs in case of boot loops.</v>

00:13:51.561 --> 00:13:53.561
<v Val Levitan>Regardless, regardless.</v>

00:14:12.681 --> 00:14:20.201
<v Val Levitan>Or you could you could put it into a second release. We absolutely find doing a multi-step.</v>

00:14:21.321 --> 00:14:24.041
<v Val Levitan>Release the the texts are looking for.</v>

00:14:26.041 --> 00:14:27.481
<v Val Levitan>Immediate improvement.</v>

00:14:29.641 --> 00:14:39.041
<v Val Levitan>Like within a short period of time, we have to come back to the market and offer an improvement. If we don't, our product will be rejected.</v>

00:14:41.721 --> 00:14:47.641
<v Pavel Frolov>Okay, this capability description quite understandable.</v>

00:14:49.441 --> 00:14:53.081
<v Pavel Frolov>Probably implementation.</v>

00:14:51.961 --> 00:14:54.841
<v Val Levitan>Why don't you, why don't you, why don't you think about it?</v>

00:14:56.761 --> 00:15:09.321
<v Pavel Frolov>Definitely, definitely. And I think it will be splitted into some approaches. And during, for example, first release of improvements.</v>

00:15:10.401 --> 00:15:17.481
<v Pavel Frolov>Probably it will be just an additional logging or something like this to understand different cases.</v>

00:15:37.601 --> 00:15:38.121
<v Felipe Miranda Giorgi>Move on.</v>

00:15:38.841 --> 00:15:39.241
<v Pavel Frolov>Yeah.</v>

00:15:40.441 --> 00:15:55.961
<v Felipe Miranda Giorgi>Okay. Case number four was add or remove printer without hard reset. We said the EGM shall allow technician to enable or disable the printer after machine is set up without a hard reset and without a new RIS file.</v>

00:15:58.921 --> 00:16:20.441
<v Felipe Miranda Giorgi>So the acceptance criteria is that the technician can enable or disable the printer with no hard reset. Meters or settings are the same after the change. The Tito menu is available when the printer is enabled and not available when it is disabled. That is up for discussion, right? Because maybe the Tito menu could be available always.</v>

00:16:03.881 --> 00:16:04.361
<v Irina Shishko>Mhm.</v>

00:16:21.641 --> 00:16:27.641
<v Felipe Miranda Giorgi>It's just, you know, becomes important when the Peter printer is there.</v>

00:16:30.601 --> 00:16:36.681
<v Felipe Miranda Giorgi>And CMS shows the new printer setting after the new least QR scan.</v>

00:16:57.801 --> 00:17:03.721
<v Pavel Frolov>So, some some notes related to this capability right now.</v>

00:17:05.241 --> 00:17:21.241
<v Pavel Frolov>Right now, on all softwares that we produce, printer and bill acceptor is a number of devices that cannot be added on the fly.</v>

00:17:22.521 --> 00:17:26.921
<v Pavel Frolov>only through the initial setup.</v>

00:17:27.721 --> 00:17:28.121
<v Felipe Miranda Giorgi>Reed.</v>

00:17:36.201 --> 00:17:38.841
<v Pavel Frolov>Let's investigate this.</v>

00:17:40.001 --> 00:17:43.961
<v Pavel Frolov>I'm not sure that this is quite simple.</v>

00:17:46.041 --> 00:17:48.881
<v Pavel Frolov>But probably it can be implemented.</v>

00:18:03.561 --> 00:18:06.281
<v Val Levitan>Sebastian, please pay attention to...</v>

00:18:07.241 --> 00:18:10.481
<v Val Levitan>The machine at least that needs to be restored in the browser.</v>

00:18:11.881 --> 00:18:16.841
<v Sebastian Cortes>Yes, sir, I'm waiting for the technician is on his way to the location.</v>

00:18:17.561 --> 00:18:21.401
<v Val Levitan>Okay, will you need the Irina help for this?</v>

00:18:18.681 --> 00:18:19.161
<v Sebastian Cortes>Mmh.</v>

00:18:25.801 --> 00:18:26.201
<v Sebastian Cortes>Sorry?</v>

00:18:27.401 --> 00:18:29.801
<v Val Levitan>Will you need Irina help for this?</v>

00:18:31.241 --> 00:18:32.921
<v Sebastian Cortes>No, I don't think so.</v>

00:18:38.041 --> 00:18:46.681
<v Felipe Miranda Giorgi>Okay, can we go to #5 or should... Okay, 5. Issue lease when a machine and CMS installations do not match.</v>

00:18:41.321 --> 00:18:41.801
<v Pavel Frolov>Yes.</v>

00:18:48.441 --> 00:18:55.481
<v Felipe Miranda Giorgi>CMS shall issue a new valid lease automatically even if the installation on the machine does not match the installation approved in CMS.</v>

00:18:57.161 --> 00:19:11.641
<v Felipe Miranda Giorgi>So in this case, I'm referring to when we do software upgrades and we give customers a time limit to upgrade the software, let's say three months. They did it on most cabinets, but they forgot a few.</v>

00:19:13.561 --> 00:19:16.601
<v Felipe Miranda Giorgi>What, what, what we request is...</v>

00:19:17.761 --> 00:19:26.521
<v Felipe Miranda Giorgi>that a mismatch does not block the lease. A new valid lease is issued with no action at JVL. And I think this starts from.</v>

00:19:27.721 --> 00:19:32.521
<v Felipe Miranda Giorgi>From the previous, I think it was #3, when, when...</v>

00:19:34.201 --> 00:19:54.281
<v Felipe Miranda Giorgi>In order to issue a new software for any given cabinet or to create a new installation for a serial number, I need to delete the old installation and make it not valid. Right? Because otherwise the serial number is not available</v>

00:19:50.121 --> 00:19:50.681
<v Pavel Frolov>Mhm.</v>

00:19:54.761 --> 00:20:00.041
<v Felipe Miranda Giorgi>For the new installation, what we are what we are suggesting here is that.</v>

00:20:00.881 --> 00:20:19.881
<v Felipe Miranda Giorgi>A mismatch does not block the lease. A new valid lease is issued with no action at JVL. The lease does not depend on passport scan or a code from JVL. If an upgrade was created in CMS but not loaded, the machine still gets a new lease for its current installation.</v>

00:20:21.961 --> 00:20:26.041
<v Felipe Miranda Giorgi>This, I don't know if you have questions. This is quite tricky, but...</v>

00:20:27.641 --> 00:20:29.961
<v Pavel Frolov>Yes, the description is clear.</v>

00:20:32.441 --> 00:20:38.041
<v Pavel Frolov>Do not know what changes it will require on the server side.</v>

00:20:55.161 --> 00:20:55.801
<v Felipe Miranda Giorgi>K.</v>

00:20:56.881 --> 00:21:00.681
<v Felipe Miranda Giorgi>Should I move on, or do we want to discuss it? OK.</v>

00:20:59.081 --> 00:20:59.801
<v Pavel Frolov>Yes.</v>

00:21:01.321 --> 00:21:05.401
<v Pavel Frolov>Nothing to discuss, just need to investigation.</v>

00:21:03.321 --> 00:21:04.841
<v Felipe Miranda Giorgi>Replace a part.</v>

00:21:06.201 --> 00:21:25.161
<v Felipe Miranda Giorgi>Replace a part without passport QR. After a part is replaced, for example, a bill acceptor, the AGM shall register in your device without passport QR code and without a code from JVL. So right now, yes, you can replace the bill acceptor, you can replace a printer, and it continues working.</v>

00:21:25.241 --> 00:21:40.761
<v Felipe Miranda Giorgi>There is no problem with that. But the moment there is a hard reset for any given reason, passport is required. Passport update. The idea is to go without passport updates or to update automatically.</v>

00:21:43.161 --> 00:21:43.561
<v Pavel Frolov>Yeah.</v>

00:21:45.561 --> 00:21:46.201
<v Felipe Miranda Giorgi>So it.</v>

00:21:56.681 --> 00:21:57.161
<v Felipe Miranda Giorgi>Clear.</v>

00:21:59.961 --> 00:22:00.921
<v Pavel Frolov>Yes, yes.</v>

00:22:03.481 --> 00:22:05.041
<v Felipe Miranda Giorgi>Uh, the text.</v>

00:22:08.281 --> 00:22:23.801
<v Felipe Miranda Giorgi>Okay, this is something that maybe was not discussed there. Detect missed upgrades before lease expiration. CMS shall track which selected machines were upgraded and alert JBL about the machine still pending before the lease expires. So...</v>

00:22:25.881 --> 00:22:39.241
<v Felipe Miranda Giorgi>A master operator requests an upgrade on a list of cabinets. The customer upgrades most of the machine, but misses one, two, or several. Nothing, this is very similar to the one, what was it, the case number?</v>

00:22:40.841 --> 00:22:41.161
<v Felipe Miranda Giorgi>Five.</v>

00:22:42.121 --> 00:22:44.201
<v Felipe Miranda Giorgi>It's got to do with that, right?</v>

00:22:48.001 --> 00:23:08.761
<v Felipe Miranda Giorgi>And I think case number 5 might have been confused with all this quick, but acceptance criteria, CMS shows which selected machines are upgraded and which are pending the upgrade to be implemented in the machine. Ten days before lease expiration, JVL receives an e-mail.</v>

00:23:09.001 --> 00:23:16.761
<v Felipe Miranda Giorgi>Lease expiring, update pending on X number of machines, and the list of serial numbers, and then...</v>

00:23:14.041 --> 00:23:14.201
<v Sebastian Cortes>Be.</v>

00:23:17.921 --> 00:23:25.401
<v Felipe Miranda Giorgi>The miss machine still gets a lease renewal and shows a clear upgrade pending message, so...</v>

00:23:26.761 --> 00:23:40.361
<v Felipe Miranda Giorgi>There is, you know, a clear update pending message, but the lease still activates if the customer was not able to get to all the machines on time.</v>

00:23:43.001 --> 00:23:46.521
<v Felipe Miranda Giorgi>It's very similar to the other one.</v>

00:24:15.081 --> 00:24:15.561
<v Irina Shishko>True.</v>

00:24:25.001 --> 00:24:26.041
<v Pavel Frolov>Okay, it's clear.</v>

00:24:27.161 --> 00:24:27.321
<v Irina Shishko>Mm.</v>

00:24:29.401 --> 00:24:31.241
<v Pavel Frolov>You know what?</v>

00:24:30.921 --> 00:24:32.201
<v Irina Shishko>The, the.</v>

00:24:33.321 --> 00:24:33.961
<v Irina Shishko>A.</v>

00:24:35.841 --> 00:24:38.441
<v Felipe Miranda Giorgi>Show the real case of a critical error.</v>

00:24:40.361 --> 00:24:44.361
<v Felipe Miranda Giorgi>The AGM shall show the real cause of a critical error and was needed to fix it.</v>

00:24:45.561 --> 00:24:51.881
<v Felipe Miranda Giorgi>Well, right now we have the big yellow QR code. If it could show the technician.</v>

00:24:55.801 --> 00:25:14.241
<v Felipe Miranda Giorgi>So currently the machine shows a full yellow screen, large warning triangle, and the words critical error. The QR code returns only information was sent to JBL customer support. The technician learns that the error is critical, not the cause, not the fix, not the parts required, and arrives unprepared.</v>

00:25:14.921 --> 00:25:15.561
<v Felipe Miranda Giorgi>So...</v>

00:25:16.761 --> 00:25:17.961
<v Felipe Miranda Giorgi>If we could tell him.</v>

00:25:19.121 --> 00:25:24.841
<v Felipe Miranda Giorgi>If the machine could say what the error is, it would be much easier to fix it on the fly.</v>

00:25:28.681 --> 00:25:42.681
<v Pavel Frolov>In most cases, we do not know beforehand, before we investigate crash logs, what was the reason of this crash.</v>

00:25:44.441 --> 00:25:53.721
<v Pavel Frolov>Several times we discussed about some special tool, error explanation tool. It was named.</v>

00:25:54.681 --> 00:25:56.121
<v Pavel Frolov>To have, um...</v>

00:25:57.481 --> 00:25:58.521
<v Pavel Frolov>Central.</v>

00:26:00.841 --> 00:26:02.121
<v Val Levitan>That, that's could be.</v>

00:26:01.001 --> 00:26:02.761
<v Pavel Frolov>Database of all.</v>

00:26:04.041 --> 00:26:07.721
<v Val Levitan>This could be moved to the second MVP.</v>

00:26:08.521 --> 00:26:09.961
<v Val Levitan>We, we don't need it right now.</v>

00:26:08.601 --> 00:26:11.401
<v Pavel Frolov>Or tense, or tense.</v>

00:26:13.801 --> 00:26:14.921
<v Pavel Frolov>Because it.</v>

00:26:13.881 --> 00:26:15.121
<v Val Levitan>We don't need it right now.</v>

00:26:16.961 --> 00:26:18.681
<v Val Levitan>Let's move it to MVP 2.</v>

00:26:22.281 --> 00:26:22.841
<v Val Levitan>Felipe.</v>

00:26:23.961 --> 00:26:24.521
<v Felipe Miranda Giorgi>Clear.</v>

00:26:28.361 --> 00:26:44.841
<v Felipe Miranda Giorgi>Okay, I'm going to move to #9. Lease renew with one QR scan. That was one that was added. Remember how we have four, 5, 6 QR codes? We want to do it with just one QR code and be done with it.</v>

00:26:46.121 --> 00:26:48.921
<v Felipe Miranda Giorgi>That's this capability, or or or.</v>

00:26:50.441 --> 00:26:52.361
<v Pavel Frolov>It's clear. It's okay.</v>

00:26:51.321 --> 00:26:53.241
<v Irina Shishko>Okay, it's simple.</v>

00:26:53.721 --> 00:26:54.601
<v Pavel Frolov>No problem.</v>

00:26:56.041 --> 00:26:57.321
<v Felipe Miranda Giorgi>That's what I have, Val.</v>

00:26:58.761 --> 00:26:59.641
<v Val Levitan>Fantastic.</v>

00:27:02.041 --> 00:27:06.521
<v Val Levitan>So what we want now is the capabilities to be entered in Jira.</v>

00:27:07.961 --> 00:27:09.001
<v Val Levitan>And we want.</v>

00:27:11.801 --> 00:27:15.561
<v Val Levitan>requirements to be linked. Sebastian, you know how to do it, right?</v>

00:27:16.201 --> 00:27:17.481
<v Sebastian Cortes>Yes, sir, I know.</v>

00:27:17.081 --> 00:27:18.441
<v Val Levitan>Okay, so it's on you.</v>

00:27:19.321 --> 00:27:21.081
<v Val Levitan>Work with Pavel directly.</v>

00:27:22.201 --> 00:27:23.881
<v Val Levitan>You're taking over from now.</v>

00:27:26.361 --> 00:27:28.601
<v Val Levitan>I want to free up Felipe for other things.</v>

00:27:29.721 --> 00:27:30.201
<v Sebastian Cortes>Okay.</v>

00:27:29.881 --> 00:27:39.881
<v Val Levitan>So you work, Felipe will help you in the background, but you manage Jira. Make sure that the capabilities are in Jira, requirements are linked to the capabilities.</v>

00:27:40.361 --> 00:27:40.841
<v Sebastian Cortes>Mhm.</v>

00:27:41.081 --> 00:28:00.361
<v Val Levitan>Pavel direct you what to do, and then on the other side, Pavel will create features and schedule resources and work. Irina will manage acceptance criteria, and her department will create automated testing for.</v>

00:27:41.441 --> 00:27:41.641
<v Irina Shishko>No.</v>

00:27:44.121 --> 00:27:44.601
<v Sebastian Cortes>Mhm.</v>

00:27:53.401 --> 00:27:53.641
<v Sebastian Cortes>Oh.</v>

00:28:01.161 --> 00:28:02.921
<v Val Levitan>Well, no, no, sorry.</v>

00:28:04.081 --> 00:28:04.201
<v Irina Shishko>Yeah.</v>

00:28:04.361 --> 00:28:08.761
<v Val Levitan>The automated testing will not be created on this. That's fine. Yeah.</v>

00:28:11.641 --> 00:28:15.561
<v Val Levitan>Okay. Thank you very much. I wish everybody a great day.</v>

00:28:12.681 --> 00:28:13.081
<v Pavel Frolov>Yep.</v>

00:28:13.321 --> 00:28:13.641
<v Sebastian Cortes>Hey.</v>

00:28:14.361 --> 00:28:15.081
<v Felipe Miranda Giorgi>Thank you.</v>

00:28:16.121 --> 00:28:19.161
<v Val Levitan>OK, Felipe, Felipe, happy birthday!</v>

00:28:16.441 --> 00:28:17.961
<v Sebastian Cortes>Thank you. You too. Bye.</v>

00:28:16.521 --> 00:28:16.921
<v Pavel Frolov>Bye.</v>

00:28:19.321 --> 00:28:20.761
<v Felipe Miranda Giorgi>Thank you, thank you, sir.</v>

00:28:22.121 --> 00:28:22.601
<v Felipe Miranda Giorgi>Bye-bye.</v>

00:28:23.241 --> 00:28:23.681
<v Sebastian Cortes>Ivan.</v>

