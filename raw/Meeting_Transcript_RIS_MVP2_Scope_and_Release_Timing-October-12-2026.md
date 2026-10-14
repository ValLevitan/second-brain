# Raw Transcript — RIS MSVP2 Meeting
**Date:** October 12, 2026, 11:29 AM – 12:02 PM Eastern
**Summary note:** [[Meeting_Notes_RIS_MVP2_Scope_and_Release_Timing-October-12-2026]]
---
WEBVTT

00:00:03.431 --> 00:00:04.591
<v Irina Shishko>See you.</v>

00:00:05.711 --> 00:00:26.391
<v Pavel Frolov>Yeah, the main question here, the main question here will be, are we really want to resubmit next version because we are making changes for actually three different versions, for pitch one, pitch two, and...</v>

00:00:05.951 --> 00:00:07.471
<v Irina Shishko>Tucatores Seitz.</v>

00:00:24.991 --> 00:00:25.791
<v Felipe Miranda Giorgi>That's.</v>

00:00:28.031 --> 00:00:47.631
<v Felipe Miranda Giorgi>Yes, well, before we start there, let's go back as a form of reviewing what we're doing because we started the recording late. So we are going to start discussing now the Mvp 2 RIS improvements. And what Pavel was doing right now was...</v>

00:00:34.911 --> 00:00:35.391
<v Pavel Frolov>Mhm.</v>

00:00:48.191 --> 00:00:55.631
<v Felipe Miranda Giorgi>setting up the fixed start date and the fixed release date for Mvp 2. Now,</v>

00:00:56.751 --> 00:01:09.071
<v Felipe Miranda Giorgi>Pavel or Irina asked if it's worth sending the Mvp one for the lab because we're going to have three different builds, correct, for page one, two, and three.</v>

00:01:11.471 --> 00:01:18.111
<v Felipe Miranda Giorgi>Personally speaking, I don't think the changes in Mvp one.</v>

00:01:19.711 --> 00:01:20.271
<v Felipe Miranda Giorgi>Arc.</v>

00:01:21.951 --> 00:01:29.711
<v Felipe Miranda Giorgi>or cover most of the customers' concerns because...</v>

00:01:30.831 --> 00:01:40.111
<v Felipe Miranda Giorgi>Yeah, they they fix some some areas, but they are not the biggest pain points on customers, right? So...</v>

00:01:41.391 --> 00:01:50.431
<v Felipe Miranda Giorgi>I am of the opinion, but I don't know what Val wants, right? But I am of the opinion that releasing this for the lab.</v>

00:01:51.711 --> 00:02:12.671
<v Felipe Miranda Giorgi>and paying the lab and getting this new build, getting it changed, and a few, maybe a month later, or I don't know, asking the customer again, okay, we have to do a new upgrade. After all the upgrades that we've done, it's going to be complicated. Yes, I think it will be complicated.</v>

00:02:14.111 --> 00:02:17.471
<v Pavel Frolov>Okay, for now I will save.</v>

00:02:18.671 --> 00:02:20.271
<v Pavel Frolov>I, I will save this for now.</v>

00:02:18.791 --> 00:02:19.911
<v Irina Shishko>It's been you.</v>

00:02:27.631 --> 00:02:34.031
<v Pavel Frolov>What is the main painful point from the customer?</v>

00:02:35.471 --> 00:02:39.311
<v Felipe Miranda Giorgi>I think the most painful point for the customer is...</v>

00:02:40.831 --> 00:02:59.071
<v Felipe Miranda Giorgi>They complain a lot about having to do a hard reset to fix any issue with Jvl, like a boot loop, like a wrong version, so you have to do a hard reset. But all this...</v>

00:02:59.711 --> 00:03:19.951
<v Felipe Miranda Giorgi>Those fixes, some of the ones you mentioned for Mvp 2, cover some of the reasons for this hard reset, but the ones on Mvp 1, I don't think they do. If we look at Mvp 1, if you want to look at it, yes, yeah, only one QR scan.</v>

00:03:20.191 --> 00:03:27.631
<v Felipe Miranda Giorgi>But this is after a hard reset, or, or, or you know, but the biggest pain points is...</v>

00:03:28.511 --> 00:03:36.911
<v Felipe Miranda Giorgi>Having to do a hard reset for everything, every problem on a Jvl, the passport scan, and the software mismatching.</v>

00:03:38.111 --> 00:03:39.391
<v Felipe Miranda Giorgi>Do you agree, Celestia?</v>

00:03:42.431 --> 00:03:42.751
<v Felipe Miranda Giorgi>Yeah.</v>

00:03:42.511 --> 00:03:43.791
<v Sebastian Cortes>Yes, yes, I agree.</v>

00:03:43.591 --> 00:03:49.991
<v Pavel Frolov>OKOK, so let's come back to.</v>

00:03:51.431 --> 00:03:53.431
<v Pavel Frolov>It show capabilities.</v>

00:03:54.871 --> 00:03:55.911
<v Pavel Frolov>Mark them.</v>

00:03:59.431 --> 00:04:01.831
<v Pavel Frolov>to give them a proper versions.</v>

00:03:59.791 --> 00:04:18.111
<v Felipe Miranda Giorgi>Add, for example, add and remove printer without a hard reset. That is, you know, hard reset. You need a hard reset. You need new settings. You need to come here, pick up the settings or pick up the new software. We need</v>

00:04:10.511 --> 00:04:10.911
<v Sebastian Cortes>MM.</v>

00:04:18.911 --> 00:04:32.911
<v Felipe Miranda Giorgi>Elizabeth or anyone in Jvl to create new file for every new, you know, configuration that takes time and and resources also, you know, we.</v>

00:04:32.191 --> 00:04:39.311
<v Pavel Frolov>OK, if you take a look on capabilities.</v>

00:04:40.111 --> 00:04:41.311
<v Pavel Frolov>241</v>

00:04:43.431 --> 00:04:47.471
<v Pavel Frolov>If, uh, particularly this, and...</v>

00:04:48.671 --> 00:04:49.631
<v Pavel Frolov>Lease one.</v>

00:04:50.751 --> 00:04:55.391
<v Pavel Frolov>This tool capabilities actually.</v>

00:04:56.311 --> 00:05:00.831
<v Pavel Frolov>Related to Sierra looks like.</v>

00:05:02.591 --> 00:05:08.991
<v Pavel Frolov>From the machine perspective, Nathan need to be implemented, so actually...</v>

00:05:10.791 --> 00:05:22.831
<v Pavel Frolov>If we submit Mvp one version, we can add this further after the release and make it separately.</v>

00:05:23.671 --> 00:05:27.751
<v Felipe Miranda Giorgi>You can add it after without submitting again.</v>

00:05:27.711 --> 00:05:37.311
<v Pavel Frolov>Yes, yes, yes. That's why I think this is not a problem. It will be added for already submitted version.</v>

00:05:28.871 --> 00:05:29.351
<v Felipe Miranda Giorgi>Okarak.</v>

00:05:36.791 --> 00:05:39.671
<v Felipe Miranda Giorgi>Okay, which one? Capability 251?</v>

00:05:40.191 --> 00:05:41.551
<v Pavel Frolov>and 253</v>

00:05:41.671 --> 00:05:42.791
<v Felipe Miranda Giorgi>Okay, got it.</v>

00:05:43.631 --> 00:05:44.111
<v Sebastian Cortes>Mhm.</v>

00:05:44.711 --> 00:05:48.191
<v Pavel Frolov>What about printer right now, actually?</v>

00:05:49.071 --> 00:06:05.151
<v Pavel Frolov>This feature already implemented by mistake, I would say. How a developer made it even not for Mvp one, but already created.</v>

00:06:04.391 --> 00:06:06.551
<v Felipe Miranda Giorgi>How is it implemented?</v>

00:06:09.871 --> 00:06:13.631
<v Pavel Frolov>Actually, you will enable.</v>

00:06:14.911 --> 00:06:16.831
<v Pavel Frolov>Uh, if, if you connect printer.</v>

00:06:19.791 --> 00:06:25.311
<v Pavel Frolov>And you have a RIS without printer.</v>

00:06:26.511 --> 00:06:47.391
<v Pavel Frolov>But if you connect the printer, it will appear in the system. And if you enter setup screens, it will be an additional option to set a check mark, use printer or not use.</v>

00:06:46.071 --> 00:06:46.471
<v Felipe Miranda Giorgi>Hal.</v>

00:06:48.671 --> 00:06:49.351
<v Felipe Miranda Giorgi>Fantastic.</v>

00:06:49.951 --> 00:07:07.151
<v Pavel Frolov>And if if it selected, it will be added into a list of cash out cash out possible device before the hand play, but after Aft.</v>

00:06:50.031 --> 00:06:50.351
<v Sebastian Cortes>And...</v>

00:06:59.991 --> 00:07:02.311
<v Felipe Miranda Giorgi>Peripheral, yeah. Oh, okay.</v>

00:07:07.991 --> 00:07:08.711
<v Felipe Miranda Giorgi>Okarak.</v>

00:07:10.751 --> 00:07:11.071
<v Irina Shishko>Up.</v>

00:07:11.311 --> 00:07:24.311
<v Pavel Frolov>Frankly speaking, we have not tested this feature; it's just just developed, and I haven't seen this, but according to description, it's already mostly implemented.</v>

00:07:19.591 --> 00:07:20.151
<v Felipe Miranda Giorgi>Okay.</v>

00:07:25.511 --> 00:07:26.071
<v Felipe Miranda Giorgi>Okay.</v>

00:07:33.551 --> 00:07:52.551
<v Pavel Frolov>I mean, I say that probably, probably we will need to add something on server side, but again, if it's properly implemented, server part could be implemented further after submission, but yeah, better to implement it together with release.</v>

00:07:53.031 --> 00:07:53.511
<v Irina Shishko>Mhm.</v>

00:07:53.951 --> 00:07:54.591
<v Felipe Miranda Giorgi>Okay.</v>

00:07:54.591 --> 00:07:55.831
<v Irina Shishko>And I show many private area.</v>

00:07:55.951 --> 00:08:05.471
<v Pavel Frolov>So definitely, definitely the most difficult part related to capability 248.</v>

00:08:09.631 --> 00:08:20.111
<v Pavel Frolov>Upgrade software without creating a new RIS. It requires both local gaming server fix and server side.</v>

00:08:22.551 --> 00:08:24.631
<v Felipe Miranda Giorgi>So that is Mvp 2 for sure.</v>

00:08:26.431 --> 00:08:26.751
<v Pavel Frolov>Um...</v>

00:08:28.351 --> 00:08:35.951
<v Pavel Frolov>Probably, probably the first one can be implemented and released on the Mvp one.</v>

00:08:30.311 --> 00:08:30.871
<v Felipe Miranda Giorgi>Okay.</v>

00:08:38.271 --> 00:08:45.311
<v Pavel Frolov>That relates to, as we discussed previously, if you remember, to reuse.</v>

00:08:46.431 --> 00:08:49.151
<v Pavel Frolov>Reserved areas, if you do not change.</v>

00:08:50.991 --> 00:08:51.711
<v Pavel Frolov>Version.</v>

00:08:52.911 --> 00:09:03.231
<v Pavel Frolov>If you do not change version and apply it, arrays, and for some reason you need to make factory reset.</v>

00:09:05.711 --> 00:09:14.831
<v Pavel Frolov>It will be possible during the next initial setup just to select pre-saved version of RIS.</v>

00:09:16.031 --> 00:09:18.351
<v Pavel Frolov>Without using USB stick or...</v>

00:09:18.391 --> 00:09:20.791
<v Felipe Miranda Giorgi>and apply to the new software.</v>

00:09:22.071 --> 00:09:22.591
<v Felipe Miranda Giorgi>Virtue.</v>

00:09:22.111 --> 00:09:41.311
<v Pavel Frolov>No, for current version. And the next and the next feature actually it will relate to different software if it's suitable. Suitable means the same games, same games, same lines number for games.</v>

00:09:24.631 --> 00:09:25.191
<v Felipe Miranda Giorgi>Okay.</v>

00:09:34.111 --> 00:09:35.831
<v Felipe Miranda Giorgi>Peripherals, yeah.</v>

00:09:42.351 --> 00:09:44.671
<v Pavel Frolov>Nothing special is games.</v>

00:09:43.991 --> 00:09:44.471
<v Felipe Miranda Giorgi>Yeah.</v>

00:09:46.031 --> 00:09:53.351
<v Pavel Frolov>Just, just to reuse for the for the same suitable version, for example, no newer newer software version.</v>

00:09:51.351 --> 00:09:52.471
<v Felipe Miranda Giorgi>Right, right, right.</v>

00:09:53.671 --> 00:09:54.151
<v Felipe Miranda Giorgi>Okay.</v>

00:10:02.551 --> 00:10:03.271
<v Felipe Miranda Giorgi>Okay.</v>

00:10:05.191 --> 00:10:11.351
<v Pavel Frolov>And the last one, recover from the boot loop without hard reset.</v>

00:10:12.951 --> 00:10:26.711
<v Pavel Frolov>Frankly speaking, I don't know what to do with this. Seems we need to perform lots of experimenting even before we decide what to do and how to do.</v>

00:10:17.911 --> 00:10:18.551
<v Felipe Miranda Giorgi>Okay.</v>

00:10:29.511 --> 00:10:30.871
<v Pavel Frolov>Cause it it.</v>

00:10:29.911 --> 00:10:30.551
<v Felipe Miranda Giorgi>So.</v>

00:10:32.471 --> 00:10:33.751
<v Felipe Miranda Giorgi>Go ahead, I'm sorry.</v>

00:10:32.791 --> 00:10:39.831
<v Pavel Frolov>Yeah, it's it says it says that we need to recover, saving all the...</v>

00:10:41.351 --> 00:10:47.031
<v Pavel Frolov>History, all the game settings, but in most cases.</v>

00:10:51.591 --> 00:10:54.711
<v Pavel Frolov>Critical error caused by some.</v>

00:10:56.711 --> 00:11:00.311
<v Pavel Frolov>Wrongly written data in storage, and...</v>

00:11:00.471 --> 00:11:20.071
<v Felipe Miranda Giorgi>You know, when it, we've seen that, for example, when there is a storm and there is a power peak or something happens, sometimes machines go into this never-ending boot loop. I think it has to do with power or maybe, you know, whatever. I think it requires more, you know, technical investigation.</v>

00:11:06.631 --> 00:11:06.951
<v Pavel Frolov>Uh-huh.</v>

00:11:20.311 --> 00:11:28.871
<v Felipe Miranda Giorgi>But, but I, I don't know if it's directly related to missing, you know, parts on the ISO. I'm not sure about that.</v>

00:11:30.791 --> 00:11:46.071
<v Pavel Frolov>Yeah, actually, as I have already said last time, probably, probably some cases could be fixed by clearing last game status.</v>

00:11:47.431 --> 00:11:48.151
<v Felipe Miranda Giorgi>Okay.</v>

00:11:48.111 --> 00:12:08.551
<v Pavel Frolov>If it's suitable, I don't know. Probably Gaming Commission will already receive the last records. And if we clear it and restore game, it will lost last game status. It's not so good.</v>

00:12:08.031 --> 00:12:08.471
<v Felipe Miranda Giorgi>Lei.</v>

00:12:09.591 --> 00:12:09.991
<v Felipe Miranda Giorgi>Yeah.</v>

00:12:13.431 --> 00:12:14.631
<v Felipe Miranda Giorgi>Something else.</v>

00:12:17.511 --> 00:12:32.631
<v Felipe Miranda Giorgi>that we had requested, and maybe I need to discuss this with Sebastian before I discuss it with you, but one requirement that we had asked, and I don't know if it was, I think one told me it was implemented for this new version, but it's...</v>

00:12:25.351 --> 00:12:25.831
<v Pavel Frolov>Mhm.</v>

00:12:34.631 --> 00:12:37.111
<v Felipe Miranda Giorgi>It's a cash out.</v>

00:12:38.071 --> 00:12:57.671
<v Felipe Miranda Giorgi>only screen, not for Tito, but for ticket cash out, where we see all the cash out logs. Why? Because right now we have transaction history, where we see bad win, bad win, deposit, bad, bad win, bad, 81 pages.</v>

00:12:57.711 --> 00:13:16.831
<v Felipe Miranda Giorgi>Correct. And sometimes when they want to go back in time and look for a specific cash out, they need to go back, back, back. But if they continue playing the machine, this record is overwritten very fast, right? But if you have...</v>

00:13:16.071 --> 00:13:16.471
<v Pavel Frolov>Yeah.</v>

00:13:17.271 --> 00:13:37.191
<v Felipe Miranda Giorgi>a dedicated window for cash out only, I think 81 pages would be more than enough for anything, right? So I think this is very important. I don't know if I had discussed it with Sebastian, but I know I discussed it with Juan and Juan told me that it was in progress.</v>

00:13:33.351 --> 00:13:33.831
<v Sebastian Cortes>No, no.</v>

00:13:37.351 --> 00:13:38.151
<v Felipe Miranda Giorgi>At some point.</v>

00:13:39.031 --> 00:13:39.511
<v Pavel Frolov>Mhm.</v>

00:13:40.471 --> 00:13:41.151
<v Felipe Miranda Giorgi>Adt.</v>

00:13:40.711 --> 00:13:41.351
<v Pavel Frolov>Oh.</v>

00:13:42.551 --> 00:14:03.191
<v Felipe Miranda Giorgi>There's this situation where sometimes machines are disconnected from Intralot for any reason from the server, from their SAS, RS232 port. And when they, because of signature mismatch or something, or we didn't respond very soon,</v>

00:13:42.711 --> 00:13:43.591
<v Pavel Frolov>Okay, think.</v>

00:14:03.511 --> 00:14:19.351
<v Felipe Miranda Giorgi>And when they come back up, we stay locked by accounting system until someone manually goes out of service, operational, out of service, operational, exit, and the game comes back up.</v>

00:14:20.631 --> 00:14:32.231
<v Felipe Miranda Giorgi>Now, during that time, the lottery is not able to unlock the machine from their server because our machine stays in locked.</v>

00:14:20.951 --> 00:14:21.431
<v Pavel Frolov>Mmh.</v>

00:14:33.111 --> 00:14:39.511
<v Felipe Miranda Giorgi>You can manually unlock it, but it will not do it automatically sometimes.</v>

00:14:40.551 --> 00:14:52.231
<v Felipe Miranda Giorgi>I don't know why that happens, but this is something that we will, we have a meeting with Val tomorrow at Intralot in the morning, and I think it's something that he wants to discuss there.</v>

00:14:54.711 --> 00:15:05.271
<v Pavel Frolov>Okay, clear, clear. Okay, I will ask Sebastian to write down capability related to cash out only page.</v>

00:15:06.231 --> 00:15:12.391
<v Pavel Frolov>And we will take a look. I think this is not a big deal to add into Mvp tool.</v>

00:15:06.791 --> 00:15:07.191
<v Sebastian Cortes>Okay.</v>

00:15:13.591 --> 00:15:15.031
<v Pavel Frolov>This improvement.</v>

00:15:16.231 --> 00:15:21.031
<v Pavel Frolov>And what about locking and unlocking?</v>

00:15:25.031 --> 00:15:44.111
<v Felipe Miranda Giorgi>I can forward all of you the conversation exchange we've had with Juan and the lottery and everyone regarding this subject so that you are up to date with what we have reported, what they have told us, and I believe</v>

00:15:34.111 --> 00:15:34.591
<v Pavel Frolov>Mmh.</v>

00:15:44.231 --> 00:15:48.311
<v Felipe Miranda Giorgi>I believe that Juan was working on this with you guys, but...</v>

00:15:51.111 --> 00:15:52.551
<v Felipe Miranda Giorgi>I will, I will find out.</v>

00:15:56.711 --> 00:15:57.471
<v Felipe Miranda Giorgi>Systems.</v>

00:15:56.951 --> 00:15:58.471
<v Pavel Frolov>Okay, okay.</v>

00:16:01.831 --> 00:16:08.791
<v Pavel Frolov>At least we will need to make an investigation related to lock and lock behavior.</v>

00:16:10.551 --> 00:16:11.431
<v Felipe Miranda Giorgi>Yes.</v>

00:16:10.551 --> 00:16:11.431
<v Pavel Frolov>And so...</v>

00:16:12.391 --> 00:16:16.071
<v Pavel Frolov>Probably, it will give us some ideas.</v>

00:16:31.191 --> 00:16:33.111
<v Pavel Frolov>So, co correct me if I wrong.</v>

00:16:34.471 --> 00:16:41.111
<v Pavel Frolov>For some reason, after Intralot locked our machine.</v>

00:16:42.231 --> 00:16:55.111
<v Pavel Frolov>and then unlocked our machine. Our machines still left in the state of locked until you manually switch it to unlock.</v>

00:16:52.391 --> 00:16:53.031
<v Felipe Miranda Giorgi>Right.</v>

00:16:55.751 --> 00:17:00.631
<v Felipe Miranda Giorgi>Yes, you have to go from locked to out of service to operation.</v>

00:17:02.951 --> 00:17:03.351
<v Pavel Frolov>K.</v>

00:17:02.951 --> 00:17:24.311
<v Felipe Miranda Giorgi>Now, when they are locked by the lottery, you are not supposed to unlock it manually. And that's what the lottery told me. There shouldn't be that possibility. If it's locked, it's locked. But because they unlock it, you can, okay? That's why you can actually do it.</v>

00:17:10.551 --> 00:17:11.031
<v Sebastian Cortes>Mhm.</v>

00:17:12.471 --> 00:17:13.031
<v Pavel Frolov>Yes.</v>

00:17:17.671 --> 00:17:18.231
<v Pavel Frolov>Yes.</v>

00:17:24.391 --> 00:17:27.031
<v Felipe Miranda Giorgi>But we, it doesn't do it automatically.</v>

00:17:28.151 --> 00:17:28.991
<v Felipe Miranda Giorgi>That is a problem.</v>

00:17:32.711 --> 00:17:33.271
<v Pavel Frolov>Okay.</v>

00:17:36.071 --> 00:17:37.271
<v Felipe Miranda Giorgi>I took logs.</v>

00:17:39.511 --> 00:17:48.871
<v Felipe Miranda Giorgi>I took logs and I sent to lottery and I sent to you at to Juan at some point, so I have all the history of this.</v>

00:17:40.071 --> 00:17:40.951
<v Pavel Frolov>Actually.</v>

00:17:40.231 --> 00:17:41.111
<v Irina Shishko>Yeah, I was just...</v>

00:17:50.031 --> 00:17:59.911
<v Pavel Frolov>Uh, Felipe, actually, on last on last software, uh, vertical pitch pitch vertical.</v>

00:17:51.991 --> 00:17:52.391
<v Felipe Miranda Giorgi>Yes.</v>

00:17:58.751 --> 00:17:59.031
<v Irina Shishko>Uh-huh.</v>

00:18:04.791 --> 00:18:05.511
<v Irina Shishko>Yes.</v>

00:18:06.951 --> 00:18:16.791
<v Pavel Frolov>Actually, it was fixed introduced in this version related to lock-unlock. Please collect some.</v>

00:18:18.311 --> 00:18:21.431
<v Felipe Miranda Giorgi>Wait, wait, which version, please? Can you tell me the...</v>

00:18:22.991 --> 00:18:24.231
<v Irina Shishko>Our last version.</v>

00:18:23.751 --> 00:18:25.751
<v Felipe Miranda Giorgi>Peach vertical, not mega hits.</v>

00:18:27.271 --> 00:18:34.631
<v Pavel Frolov>Not yet, last version that we submitted to Eclipse, it was a pitch vertical.</v>

00:18:32.791 --> 00:18:32.831
<v Irina Shishko>Ahh.</v>

00:18:36.071 --> 00:18:37.831
<v Irina Shishko>Cortana.</v>

00:18:36.111 --> 00:18:37.671
<v Pavel Frolov>What's the numbers?</v>

00:18:38.471 --> 00:18:42.791
<v Felipe Miranda Giorgi>Oh, Peach vertical, you're talking about the build.</v>

00:18:44.631 --> 00:18:46.151
<v Felipe Miranda Giorgi>3866.</v>

00:18:45.031 --> 00:18:45.511
<v Irina Shishko>Oh.</v>

00:18:47.271 --> 00:18:48.071
<v Felipe Miranda Giorgi>I believe.</v>

00:18:53.911 --> 00:18:54.471
<v Pavel Frolov>Irina.</v>

00:19:16.711 --> 00:19:17.111
<v Irina Shishko>Uh-huh.</v>

00:19:18.951 --> 00:19:19.511
<v Irina Shishko>The.</v>

00:19:20.671 --> 00:19:23.191
<v Irina Shishko>On my friends, something in my damn mum.</v>

00:19:24.431 --> 00:19:26.431
<v Pavel Frolov>Down on the builds about with.</v>

00:19:27.551 --> 00:19:27.591
<v Irina Shishko>Ahh.</v>

00:19:27.911 --> 00:19:28.231
<v Pavel Frolov>Ohh.</v>

00:19:29.751 --> 00:19:37.671
<v Irina Shishko>Yes, but it's just, yeah, it's just secondo that, yeah, we just say it do to the.</v>

00:19:33.231 --> 00:19:33.911
<v Pavel Frolov>Confluence.</v>

00:19:42.631 --> 00:19:44.551
<v Irina Shishko>Still, I need you.</v>

00:19:47.911 --> 00:19:49.511
<v Pavel Frolov>Irina will.</v>

00:19:51.031 --> 00:19:53.191
<v Pavel Frolov>Found actual numbers.</v>

00:19:55.031 --> 00:19:56.551
<v Pavel Frolov>Was it for my records?</v>

00:20:08.511 --> 00:20:09.751
<v Pavel Frolov>So, probably...</v>

00:20:10.951 --> 00:20:13.191
<v Pavel Frolov>Those behavior will be different.</v>

00:20:11.191 --> 00:20:13.151
<v Irina Shishko>That's soicious.</v>

00:20:14.711 --> 00:20:21.391
<v Pavel Frolov>And the games probably will be fixed to unlocked, to unlock them automatically.</v>

00:20:22.151 --> 00:20:23.671
<v Irina Shishko>Show up, three, three.</v>

00:20:26.471 --> 00:20:28.471
<v Pavel Frolov>4333 version.</v>

00:20:29.111 --> 00:20:39.591
<v Felipe Miranda Giorgi>Oh no, this is just released. This is Megahit Hits. This is the new version that is not even installed. We have not installed the first one. So, okay.</v>

00:20:37.591 --> 00:20:43.351
<v Pavel Frolov>Yes, yes, yes, so, but, but when when you start to install in this version.</v>

00:20:42.951 --> 00:20:45.111
<v Felipe Miranda Giorgi>OK, we will, we will observe.</v>

00:20:46.551 --> 00:20:53.911
<v Pavel Frolov>Yeah, we will observe and understand if it actually fix or probably we need to continue fixing.</v>

00:20:47.271 --> 00:20:47.911
<v Felipe Miranda Giorgi>Perfect.</v>

00:20:54.391 --> 00:21:00.871
<v Felipe Miranda Giorgi>Well, we have the IGT SAS simulator here. We could try to simulate locking, unlocking, locking, unlocking, see what happens.</v>

00:21:02.071 --> 00:21:03.431
<v Pavel Frolov>Okay, yeah, yeah.</v>

00:21:03.191 --> 00:21:03.471
<v Felipe Miranda Giorgi>Adt.</v>

00:21:06.391 --> 00:21:11.831
<v Pavel Frolov>So actually, yeah, in Office, we can do this testing right now, I think.</v>

00:21:12.391 --> 00:21:12.951
<v Felipe Miranda Giorgi>Okay.</v>

00:21:21.511 --> 00:21:25.151
<v Irina Shishko>Oh, should you? It's not sort of three, three, three.</v>

00:21:32.311 --> 00:21:48.871
<v Irina Shishko>Die, yeah, but there's the. South Dakota.</v>

00:21:50.631 --> 00:22:00.231
<v Irina Shishko>Stop Megahit at the South Dakota.</v>

00:22:06.231 --> 00:22:08.631
<v Felipe Miranda Giorgi>I see that you are here.</v>

00:22:11.671 --> 00:22:14.471
<v Pavel Frolov>Okay, related to work unlock.</v>

00:22:16.951 --> 00:22:17.831
<v Pavel Frolov>I think.</v>

00:22:19.551 --> 00:22:27.911
<v Pavel Frolov>Testing in office this version 4333.</v>

00:22:29.111 --> 00:22:33.071
<v Pavel Frolov>You give us some more information about locked and unlocked.</v>

00:22:37.271 --> 00:22:39.111
<v Felipe Miranda Giorgi>Okay, 4333, got it.</v>

00:22:37.831 --> 00:22:38.471
<v Pavel Frolov>Cools.</v>

00:22:40.471 --> 00:22:44.631
<v Felipe Miranda Giorgi>Sebastian, before you, you were going to say something, no?</v>

00:22:40.751 --> 00:22:41.111
<v Pavel Frolov>Gaming.</v>

00:22:46.231 --> 00:23:05.071
<v Sebastian Cortes>Oh yeah, Pavel, I understood the case in the capability 250 about to add the printer. I can check the printer in the setup menu, right? So what happens</v>

00:22:46.311 --> 00:22:46.871
<v Felipe Miranda Giorgi>I think.</v>

00:23:05.391 --> 00:23:23.911
<v Sebastian Cortes>if is there another case if for any reason I reinstall the software and I apply the RIS that has the printer added. So when I try to apply that RIS, the machine will</v>

00:23:23.991 --> 00:23:26.311
<v Sebastian Cortes>Ask for the printer, or...</v>

00:23:27.391 --> 00:23:31.191
<v Sebastian Cortes>What the what will happen that in that in that in that case?</v>

00:23:32.871 --> 00:23:38.551
<v Pavel Frolov>Even on the machine, no printer, but RIS require printer.</v>

00:23:39.271 --> 00:23:39.911
<v Sebastian Cortes>Yes.</v>

00:23:42.551 --> 00:23:43.191
<v Pavel Frolov>Ohh.</v>

00:23:43.591 --> 00:24:01.991
<v Sebastian Cortes>I'm asking that because now if I try to apply an RIS with printer added, if I don't have the printer installed, I can't do that. So I can apply the RIS.</v>

00:23:53.511 --> 00:23:53.671
<v Pavel Frolov>Okay.</v>

00:24:03.591 --> 00:24:04.871
<v Sebastian Cortes>Will be the case.</v>

00:24:06.431 --> 00:24:10.071
<v Sebastian Cortes>Or, what will happens that in that case?</v>

00:24:07.031 --> 00:24:07.591
<v Irina Shishko>dot.</v>

00:24:22.551 --> 00:24:35.031
<v Pavel Frolov>Yeah, in this case, during the initial setup, it should be a message saying that RIS require a printer, but you don't have this printer.</v>

00:24:37.111 --> 00:24:38.631
<v Felipe Miranda Giorgi>But will it let it continue?</v>

00:24:37.751 --> 00:24:38.271
<v Sebastian Cortes>But I...</v>

00:24:39.431 --> 00:24:43.111
<v Sebastian Cortes>Yes, but I will able to continue the applying the RIS.</v>

00:24:46.151 --> 00:24:49.431
<v Pavel Frolov>I think this is up to us to decide this.</v>

00:24:51.911 --> 00:25:00.631
<v Felipe Miranda Giorgi>Well, it should, because if later I can say that there is no printer and a checkmark, it should apply it, correct?</v>

00:25:00.311 --> 00:25:00.951
<v Sebastian Cortes>Anything.</v>

00:25:01.271 --> 00:25:07.111
<v Pavel Frolov>Okay, let's write down this case and we will think about this.</v>

00:25:08.031 --> 00:25:12.511
<v Pavel Frolov>No printer on machine. No printer.</v>

00:25:14.231 --> 00:25:16.151
<v Pavel Frolov>A RIS.</v>

00:25:17.231 --> 00:25:18.391
<v Pavel Frolov>Require printer.</v>

00:25:19.351 --> 00:25:19.831
<v Sebastian Cortes>Mhm.</v>

00:25:19.831 --> 00:25:23.511
<v Pavel Frolov>Claude, so looks like we will.</v>

00:25:25.511 --> 00:25:25.551
<v Pavel Frolov>Ah.</v>

00:25:26.951 --> 00:25:32.071
<v Pavel Frolov>We will be able to continue installation even in this case.</v>

00:25:33.671 --> 00:25:35.031
<v Irina Shishko>No bottom budget.</v>

00:25:38.071 --> 00:25:47.031
<v Pavel Frolov>But then, on the machine, it will be a tilt saying that we cannot work until you install printer, or...</v>

00:25:47.991 --> 00:25:50.231
<v Pavel Frolov>You, you will need to enter.</v>

00:25:51.591 --> 00:25:54.471
<v Pavel Frolov>Set up and uncheck printer.</v>

00:25:55.831 --> 00:25:59.351
<v Pavel Frolov>And it will enable working without printer in this case.</v>

00:26:01.111 --> 00:26:01.591
<v Felipe Miranda Giorgi>Now.</v>

00:26:04.151 --> 00:26:09.751
<v Felipe Miranda Giorgi>But maybe this is something that I need to talk to Sebastian first, but we have another case where...</v>

00:26:12.071 --> 00:26:31.151
<v Felipe Miranda Giorgi>Customers are asking for Tito in but not Tito out, meaning that the ticket can be registered by the bill acceptor, but there is no printer physically inside the machine. They are printing behind the counter. Correct?</v>

00:26:22.471 --> 00:26:22.951
<v Sebastian Cortes>Felix.</v>

00:26:26.951 --> 00:26:28.711
<v Sebastian Cortes>Please install.</v>

00:26:30.551 --> 00:26:31.111
<v Pavel Frolov>Ohh.</v>

00:26:30.751 --> 00:26:31.351
<v Sebastian Cortes>Mm-hmm.</v>

00:26:31.831 --> 00:26:42.871
<v Felipe Miranda Giorgi>So in this case, I only have access to the Tito menu for secure enhanced configuration if I have a printer.</v>

00:26:43.631 --> 00:26:44.231
<v Sebastian Cortes>Mhm.</v>

00:26:44.231 --> 00:26:54.911
<v Felipe Miranda Giorgi>But I don't have this option if I don't have a printer. How can we configure machines with Tito in but not Tito out?</v>

00:26:53.631 --> 00:26:54.391
<v Sebastian Cortes>Jira Win.</v>

00:26:55.911 --> 00:26:56.951
<v Sebastian Cortes>without printer.</v>

00:26:56.071 --> 00:27:09.671
<v Pavel Frolov>Good question. Good question. I don't know. I don't know. Need to think about this. Probably this is not a big deal to make this change, but need to take a look.</v>

00:26:58.511 --> 00:26:58.671
<v Irina Shishko>Uh-huh.</v>

00:27:08.311 --> 00:27:15.991
<v Irina Shishko>No, no, there is.</v>

00:27:17.831 --> 00:27:33.431
<v Pavel Frolov>Probably, as this fix that we discussed right now about enabling printer on the fly, probably it will enable page related to Tito settings.</v>

00:27:33.871 --> 00:27:34.391
<v Felipe Miranda Giorgi>Yes.</v>

00:27:35.471 --> 00:27:37.111
<v Felipe Miranda Giorgi>But only if there is a printer.</v>

00:27:38.031 --> 00:27:38.551
<v Sebastian Cortes>Mhm.</v>

00:27:39.431 --> 00:27:53.671
<v Pavel Frolov>In future fixes, I think not only, probably in all cases for this software. Okay, let's take a look and discuss this with developers to actually understand.</v>

00:27:43.111 --> 00:27:43.911
<v Felipe Miranda Giorgi>Oh, okay.</v>

00:27:52.871 --> 00:27:52.991
<v Irina Shishko>Play.</v>

00:27:54.831 --> 00:27:55.991
<v Pavel Frolov>What needs to be done?</v>

00:28:00.711 --> 00:28:01.271
<v Pavel Frolov>Okay.</v>

00:28:02.471 --> 00:28:02.631
<v Felipe Miranda Giorgi>Ee.</v>

00:28:04.471 --> 00:28:05.351
<v Felipe Miranda Giorgi>In theory.</v>

00:28:09.511 --> 00:28:17.991
<v Felipe Miranda Giorgi>So let me just record this. In theory, oh, not record, share. In theory, what we need is...</v>

00:28:18.871 --> 00:28:32.031
<v Felipe Miranda Giorgi>ticket in, not ticket out, right? But we need to be able to see the Tito configuration place so we can set up as secure enhanced.</v>

00:28:22.311 --> 00:28:22.951
<v Sebastian Cortes>Mm-hmm.</v>

00:28:23.031 --> 00:28:23.351
<v Pavel Frolov>Yeah.</v>

00:28:27.431 --> 00:28:28.551
<v Sebastian Cortes>Tito option.</v>

00:28:33.231 --> 00:28:33.911
<v Pavel Frolov>Yeah, here.</v>

00:28:33.511 --> 00:28:33.991
<v Sebastian Cortes>Mhm.</v>

00:28:34.551 --> 00:28:37.191
<v Felipe Miranda Giorgi>Yeah, this just sound word clear. Thank you. Okay.</v>

00:28:38.791 --> 00:28:41.431
<v Felipe Miranda Giorgi>Anything else, Sebastian?</v>

00:28:44.231 --> 00:28:47.591
<v Felipe Miranda Giorgi>So I think where we're at is...</v>

00:28:48.671 --> 00:28:51.271
<v Felipe Miranda Giorgi>We still need Val input on.</v>

00:28:52.431 --> 00:29:06.471
<v Felipe Miranda Giorgi>Do we want to send Mvp 1 to the lab and not wait for Mvp 2 or add the changes possible to Mvp 1 correct? What is the right course of action?</v>

00:29:08.311 --> 00:29:11.351
<v Felipe Miranda Giorgi>Pavel or Irina, what do you think is the right course of action?</v>

00:29:14.231 --> 00:29:15.511
<v Pavel Frolov>Yes, actually.</v>

00:29:17.031 --> 00:29:24.791
<v Pavel Frolov>Yeah, it looks like not so much work left on machine side.</v>

00:29:26.711 --> 00:29:40.551
<v Pavel Frolov>In general, we just have two features here related to RIS improvement to reuse last RIS or reuse RIS with newer software.</v>

00:29:41.111 --> 00:29:41.671
<v Felipe Miranda Giorgi>Mhm.</v>

00:29:41.991 --> 00:29:50.151
<v Pavel Frolov>No, it looks not so big. It will require server side, but server side could be released afterwards.</v>

00:29:51.351 --> 00:29:52.711
<v Pavel Frolov>And the...</v>

00:30:03.951 --> 00:30:04.231
<v Pavel Frolov>Yeah.</v>

00:30:08.231 --> 00:30:15.751
<v Pavel Frolov>Yeah, actually looks like we can close these features in two weeks.</v>

00:30:15.271 --> 00:30:18.791
<v Felipe Miranda Giorgi>Can you share? Can you share your screen again? Ohh, yeah.</v>

00:30:17.191 --> 00:30:18.631
<v Pavel Frolov>Oh, so, so, so, so.</v>

00:30:20.631 --> 00:30:21.671
<v Pavel Frolov>Yes.</v>

00:30:21.751 --> 00:30:22.231
<v Felipe Miranda Giorgi>Thank you.</v>

00:30:23.191 --> 00:30:39.751
<v Pavel Frolov>Looks like we can close most of this work in two weeks, approximately. I do not know about the last one, about boot loop, but the rest...</v>

00:30:31.191 --> 00:30:31.871
<v Felipe Miranda Giorgi>Okarak.</v>

00:30:36.311 --> 00:30:36.951
<v Felipe Miranda Giorgi>Okay.</v>

00:30:40.871 --> 00:30:43.431
<v Pavel Frolov>Would be done in two weeks, I assume.</v>

00:30:44.711 --> 00:30:45.271
<v Felipe Miranda Giorgi>Okay.</v>

00:30:46.631 --> 00:30:47.911
<v Irina Shishko>No.</v>

00:30:47.231 --> 00:30:51.111
<v Pavel Frolov>Probably, probably plus one week for testing.</v>

00:30:52.391 --> 00:30:56.551
<v Pavel Frolov>But we are going to release.</v>

00:30:58.071 --> 00:30:59.351
<v Pavel Frolov>Mvp one.</v>

00:31:02.231 --> 00:31:12.311
<v Pavel Frolov>In 2 weeks, probably, with testing. If we add in one more week, probably we can release Mvp 2.</v>

00:31:14.231 --> 00:31:14.871
<v Felipe Miranda Giorgi>Yeah.</v>

00:31:19.031 --> 00:31:20.631
<v Felipe Miranda Giorgi>Still November 1st.</v>

00:31:24.311 --> 00:31:24.551
<v Pavel Frolov>Ohh.</v>

00:31:25.431 --> 00:31:26.631
<v Irina Shishko>Is mean, yeah.</v>

00:31:26.431 --> 00:31:34.791
<v Pavel Frolov>But Irina is saying that, okay, probably until November 1st, so from from now.</v>

00:31:34.071 --> 00:31:45.271
<v Felipe Miranda Giorgi>Okay, so November 1st, we finished, then we send to Eclipse one more week, five days. So the release would be like November 9th, 10th.</v>

00:31:47.591 --> 00:31:49.871
<v Pavel Frolov>Yes, yes, approximately.</v>

00:31:49.111 --> 00:31:51.591
<v Felipe Miranda Giorgi>Or 9th, approximately, yes.</v>

00:31:49.191 --> 00:31:52.231
<v Irina Shishko>The shot with a certificate.</v>

00:31:52.751 --> 00:31:57.751
<v Felipe Miranda Giorgi>Yeah, one more week delay. OK, let's see what Val thinks about that, if he's OK.</v>

00:31:58.711 --> 00:31:59.111
<v Pavel Frolov>Yeah.</v>

00:32:00.391 --> 00:32:05.271
<v Pavel Frolov>And, and of course, we will need some more investigation on.</v>

00:32:06.231 --> 00:32:09.111
<v Pavel Frolov>Capability to fortune on.</v>

00:32:06.711 --> 00:32:14.911
<v Felipe Miranda Giorgi>But, but I would be much happier with all the fixes in Mvp 2 that just the fixes on the Mvp one, yeah.</v>

00:32:16.391 --> 00:32:17.191
<v Pavel Frolov>Yeah, I...</v>

00:32:16.631 --> 00:32:17.431
<v Felipe Miranda Giorgi>Definitely.</v>

00:32:19.111 --> 00:32:26.631
<v Pavel Frolov>I see your point. Yeah, it will give lots of convenience for technician and for...</v>

00:32:25.191 --> 00:32:25.911
<v Felipe Miranda Giorgi>Correct.</v>

00:32:27.591 --> 00:32:30.471
<v Felipe Miranda Giorgi>Correct, and that's what we're going after, so yes.</v>

00:32:33.111 --> 00:32:35.991
<v Felipe Miranda Giorgi>Alright, anything else?</v>

00:32:37.711 --> 00:32:39.191
<v Pavel Frolov>No, not for now.</v>

00:32:38.391 --> 00:32:39.191
<v Felipe Miranda Giorgi>Sebastian.</v>

00:32:40.151 --> 00:32:41.271
<v Sebastian Cortes>No, that's fine.</v>

00:32:43.911 --> 00:32:45.191
<v Pavel Frolov>Okay, thank you.</v>

00:32:44.151 --> 00:32:48.231
<v Felipe Miranda Giorgi>Well, thank you so much, everyone. Have a wonderful day.</v>

00:32:47.871 --> 00:32:48.551
<v Sebastian Cortes>Thank you, thank you.</v>

00:32:49.911 --> 00:32:50.391
<v Felipe Miranda Giorgi>Alright.</v>

00:32:50.511 --> 00:32:51.111
<v Sebastian Cortes>Bye-bye.</v>

