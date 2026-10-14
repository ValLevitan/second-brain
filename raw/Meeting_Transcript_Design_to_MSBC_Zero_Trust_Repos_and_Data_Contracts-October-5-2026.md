# Raw Transcript — Design-to-MSBC_Organization_repositories_
**Date:** October 5, 2026, 1:19 PM – 1:53 PM Eastern
**Summary note:** [[Meeting_Notes_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026]]
---
WEBVTT

00:00:11.142 --> 00:00:11.622
<v Genadi Peari>Do you know?</v>

00:00:14.262 --> 00:00:15.062
<v Val Levitan>I'm over there.</v>

00:00:19.702 --> 00:00:20.582
<v Val Levitan>Hi, Genadi.</v>

00:00:27.862 --> 00:00:32.822
<v Val Levitan>Dr. Vosto, I'm going to introduce you to the idea of how I think it should work.</v>

00:00:34.662 --> 00:00:38.102
<v Val Levitan>Between Github and Msbc.</v>

00:00:39.622 --> 00:00:46.102
<v Val Levitan>I want to tell you about how it works, the new system, how it works for...</v>

00:00:47.222 --> 00:00:48.582
<v Val Levitan>Code developers.</v>

00:00:51.662 --> 00:00:54.422
<v Val Levitan>And I understand that you're not a code developer.</v>

00:00:56.182 --> 00:00:59.382
<v Val Levitan>But I want you to understand how it works for code developers.</v>

00:01:01.302 --> 00:01:02.022
<v Val Levitan>So.</v>

00:01:03.142 --> 00:01:09.462
<v Val Levitan>The way the repositories are built for code developers is that...</v>

00:01:11.302 --> 00:01:12.742
<v Val Levitan>Each repository.</v>

00:01:13.862 --> 00:01:16.182
<v Val Levitan>Is equal to a Project in Jira.</v>

00:01:20.822 --> 00:01:21.062
<v Genadi Peari>Pay.</v>

00:01:23.542 --> 00:01:25.062
<v Val Levitan>Each repository.</v>

00:01:25.942 --> 00:01:27.142
<v Val Levitan>Has a...</v>

00:01:29.622 --> 00:01:32.342
<v Val Levitan>has zero trust state.</v>

00:01:34.822 --> 00:01:34.982
<v Val Levitan>Yeah.</v>

00:01:38.822 --> 00:01:49.062
<v Val Levitan>So one repository does not trust the next repository. There is no reference between one repository to the next repository.</v>

00:01:51.462 --> 00:01:54.022
<v Val Levitan>It's called Zero Trust State.</v>

00:01:55.422 --> 00:01:55.782
<v Genadi Peari>OK.</v>

00:01:57.542 --> 00:02:04.342
<v Val Levitan>Each repository has code in it, has pros in it.</v>

00:02:06.022 --> 00:02:08.182
<v Val Levitan>Has ADRs in it.</v>

00:02:10.422 --> 00:02:18.102
<v Val Levitan>And most importantly, and I'm making a pause because I'm going to say something very important right now. Most importantly,</v>

00:02:19.702 --> 00:02:20.662
<v Val Levitan>It has...</v>

00:02:22.582 --> 00:02:23.222
<v Val Levitan>Um...</v>

00:02:25.182 --> 00:02:27.542
<v Val Levitan>Date the contract in it.</v>

00:02:30.822 --> 00:02:36.822
<v Val Levitan>Data contract is a description of what it can do.</v>

00:02:41.302 --> 00:02:43.222
<v Val Levitan>Not what?</v>

00:02:44.502 --> 00:02:46.022
<v Val Levitan>It expects it.</v>

00:02:48.502 --> 00:02:57.222
<v Val Levitan>what information it expects because it's zero trust. It doesn't trust anything. So it doesn't want to know about anything.</v>

00:02:59.062 --> 00:03:05.382
<v Val Levitan>It only wants to specify what it can give output.</v>

00:03:10.302 --> 00:03:11.062
<v Genadi Peari>Inverting.</v>

00:03:12.102 --> 00:03:12.502
<v Val Levitan>Huh?</v>

00:03:12.902 --> 00:03:14.982
<v Genadi Peari>Inverting text.</v>

00:03:15.942 --> 00:03:19.542
<v Val Levitan>Yeah, it's actually in a dot MD file.</v>

00:03:20.822 --> 00:03:22.942
<v Val Levitan>It's called data contract.</v>

00:03:25.782 --> 00:03:34.662
<v Val Levitan>So again, repository is one-to-one relationship to a project in Jira. So there's a project code.</v>

00:03:35.942 --> 00:03:40.022
<v Val Levitan>And the repository has code for that project.</v>

00:03:41.102 --> 00:03:45.142
<v Val Levitan>It has zero trust, it has a DTR.</v>

00:03:46.262 --> 00:03:47.622
<v Val Levitan>It has rose.</v>

00:03:50.822 --> 00:03:52.902
<v Val Levitan>And it has data contracts.</v>

00:03:56.422 --> 00:04:03.622
<v Val Levitan>Data contract described what it can do while trusting 0 to everything else.</v>

00:04:07.382 --> 00:04:08.502
<v Val Levitan>From there.</v>

00:04:10.102 --> 00:04:17.462
<v Val Levitan>Claude, Claude code is able to put things together into entire code of the product.</v>

00:04:19.702 --> 00:04:25.542
<v Val Levitan>As well, as well as it's capable of testing, run end-to-end testing.</v>

00:04:27.222 --> 00:04:44.262
<v Val Levitan>This is how smart Cloud Code is from a logical perspective. The moment it assumes zero trust, assumes data contract inside the repository, everything else and the pros.</v>

00:04:48.342 --> 00:04:50.182
<v Val Levitan>It could figure out everything else.</v>

00:04:52.902 --> 00:04:57.542
<v Val Levitan>The reason I'm telling you this, because I think this is what you were missing.</v>

00:04:59.382 --> 00:05:03.182
<v Val Levitan>In figuring out how a bill of material will work.</v>

00:05:13.862 --> 00:05:14.342
<v Genadi Peari>Mm.</v>

00:05:15.782 --> 00:05:25.542
<v Val Levitan>Because the moment you have a prose as a description, the moment you have zero trust between the repositories, and most importantly...</v>

00:05:27.302 --> 00:05:30.102
<v Val Levitan>Data contract of what it can do.</v>

00:05:32.102 --> 00:05:42.582
<v Val Levitan>Then, understanding how the machine works is not an issue, and it will pull, it should it should be able to build a bill of material.</v>

00:05:44.422 --> 00:05:48.822
<v Val Levitan>I haven't tried it yet, but I'm 70% sure that it should be able to do it.</v>

00:05:49.942 --> 00:05:53.342
<v Val Levitan>because it can put the entire code together.</v>

00:05:56.422 --> 00:06:06.422
<v Val Levitan>For developers, it doesn't matter: game developer framework, LG, I mean, database.</v>

00:06:08.182 --> 00:06:09.382
<v Val Levitan>Doesn't really matter.</v>

00:06:11.702 --> 00:06:17.542
<v Val Levitan>This is how logical and how smart Claude code is.</v>

00:06:24.742 --> 00:06:26.262
<v Genadi Peari>Okay, yeah.</v>

00:06:26.902 --> 00:06:37.942
<v Val Levitan>So I don't know. I cannot tell you 100% that this will work. But I can tell you that at 100%, 100%, it works in development.</v>

00:06:38.822 --> 00:06:41.062
<v Val Levitan>I, I am 70% sure.</v>

00:06:42.022 --> 00:06:45.142
<v Val Levitan>that it will work for electromechanical design.</v>

00:06:48.502 --> 00:06:50.342
<v Val Levitan>We just have to play with it a little bit.</v>

00:06:52.742 --> 00:06:55.702
<v Val Levitan>But it will save you a crazy amount of time.</v>

00:07:00.662 --> 00:07:08.502
<v Val Levitan>You will never have to do bill of material, you will, the substitutions will automatically just work out.</v>

00:07:09.702 --> 00:07:12.422
<v Val Levitan>The versioning will be automatically there.</v>

00:07:15.622 --> 00:07:23.462
<v Val Levitan>I can even foresee that it will start doing the actual hardware development, electromechanical development for you.</v>

00:07:28.022 --> 00:07:32.342
<v Val Levitan>That's honestly, this honestly, this is what I think will happen.</v>

00:07:49.622 --> 00:07:50.102
<v Genadi Peari>Ohh.</v>

00:07:55.422 --> 00:07:58.582
<v Genadi Peari>No, okay, yeah, I hear you, so...</v>

00:08:00.662 --> 00:08:01.462
<v Genadi Peari>Dongguan.</v>

00:08:04.822 --> 00:08:05.222
<v Genadi Peari>Flex.</v>

00:08:08.662 --> 00:08:13.942
<v Genadi Peari>Bill of material.</v>

00:08:17.302 --> 00:08:20.822
<v Genadi Peari>A car cut up from a guide maintain bill of material.</v>

00:08:22.582 --> 00:08:23.462
<v Genadi Peari>The Premier.</v>

00:08:25.422 --> 00:08:38.182
<v Val Levitan>SolidWorks design from a supplier substitution. All you have to do is in Github to put a new revision.</v>

00:08:41.142 --> 00:08:42.342
<v Val Levitan>That's all you have to do.</v>

00:08:49.222 --> 00:08:49.782
<v Genadi Peari>No.</v>

00:08:51.062 --> 00:08:51.862
<v Genadi Peari>Example.</v>

00:08:55.302 --> 00:08:57.782
<v Genadi Peari>Jurisdiction, other Dubai is Modem Kabil.</v>

00:08:58.662 --> 00:09:01.542
<v Genadi Peari>Search not is deleted to ad one part number.</v>

00:09:03.782 --> 00:09:05.462
<v Genadi Peari>Click, enter.</v>

00:09:06.582 --> 00:09:07.942
<v Genadi Peari>Cockatop Ris.</v>

00:09:10.422 --> 00:09:11.382
<v Genadi Peari>Twist.</v>

00:09:29.622 --> 00:09:35.302
<v Val Levitan>This development on the bicycle capabilities.</v>

00:09:37.742 --> 00:09:38.662
<v Genadi Peari>Ohh yeah, that.</v>

00:09:47.542 --> 00:09:55.862
<v Val Levitan>Now, Printer of us, yes, yes, capability.</v>

00:09:57.262 --> 00:09:59.862
<v Val Levitan>What are manufactures for stupid drawings?</v>

00:10:21.062 --> 00:10:27.622
<v Genadi Peari>No, most likely as devil drawing.</v>

00:10:29.582 --> 00:10:35.142
<v Genadi Peari>Another part number. OK, Claude.</v>

00:10:33.622 --> 00:10:40.582
<v Val Levitan>Yeah, you do well, yeah, no, no part numbers, so us here standard got part numbers are created.</v>

00:10:40.902 --> 00:10:44.422
<v Genadi Peari>No, no, not actually what crit system was interesting.</v>

00:10:43.542 --> 00:11:03.302
<v Val Levitan>You want another, you want another printer printer. One of principal dozens not harness connector. Release a joy.</v>

00:11:11.222 --> 00:11:12.022
<v Genadi Peari>At the.</v>

00:11:21.302 --> 00:11:21.862
<v Genadi Peari>Yeah.</v>

00:11:31.222 --> 00:11:38.262
<v Genadi Peari>Part number.</v>

00:11:39.462 --> 00:11:42.982
<v Val Levitan>On on some it is daily, put it into a Msbc.</v>

00:11:44.662 --> 00:11:53.462
<v Genadi Peari>No, no, okay, we got it.</v>

00:11:51.822 --> 00:12:03.542
<v Val Levitan>When you more skill skill capability.</v>

00:12:04.622 --> 00:12:06.782
<v Val Levitan>All those are not Cris part number.</v>

00:12:07.702 --> 00:12:09.062
<v Val Levitan>Standard.</v>

00:12:16.262 --> 00:12:16.902
<v Genadi Peari>Ohh.</v>

00:12:19.622 --> 00:12:29.142
<v Val Levitan>is transcript.</v>

00:12:40.542 --> 00:12:59.782
<v Val Levitan>supplier and appreciate some e-mail. Github, part number, the part number of Msbc.</v>

00:13:00.902 --> 00:13:09.222
<v Val Levitan>Probably the most supplier was private request for quotation night at harness.</v>

00:13:11.062 --> 00:13:12.662
<v Val Levitan>The pollution quotation.</v>

00:13:13.942 --> 00:13:18.342
<v Val Levitan>quotation, Msbc.</v>

00:13:21.542 --> 00:13:28.102
<v Val Levitan>You want the quotation was not premovas emails. A private supplier will not wash away e-mail.</v>

00:13:45.462 --> 00:13:46.742
<v Val Levitan>Yes, I should.</v>

00:14:07.702 --> 00:14:27.582
<v Genadi Peari>Yeah, yeah, yeah, yeah, we should be behind. Yeah, yes, yes, the previous parallel diet was not robotic.</v>

00:14:28.502 --> 00:14:29.302
<v Genadi Peari>Miss Lisbon.</v>

00:14:31.542 --> 00:14:35.222
<v Genadi Peari>Bill of material, Github.</v>

00:14:36.262 --> 00:14:37.342
<v Val Levitan>Yes, in the ocean.</v>

00:14:36.422 --> 00:14:37.542
<v Genadi Peari>On dozens on.</v>

00:14:38.422 --> 00:14:41.302
<v Genadi Peari>Bill of material.</v>

00:14:42.862 --> 00:14:44.102
<v Val Levitan>Are you so much improved though?</v>

00:14:45.862 --> 00:14:50.342
<v Genadi Peari>Bill of material on Msbc.</v>

00:14:50.822 --> 00:14:51.302
<v Val Levitan>Yeah.</v>

00:14:53.622 --> 00:14:57.942
<v Genadi Peari>When was getting real, pushed it to Msbc, we keep it there.</v>

00:14:58.982 --> 00:15:00.662
<v Genadi Peari>We don't keep it as a reference.</v>

00:14:59.542 --> 00:14:59.942
<v Val Levitan>Yeah.</v>

00:15:02.262 --> 00:15:09.622
<v Val Levitan>Stop the the definition of bill of material bill of material.</v>

00:15:11.542 --> 00:15:12.982
<v Genadi Peari>I love material at the.</v>

00:15:14.422 --> 00:15:28.262
<v Genadi Peari>structure instances, how many were assembly sub-assemblies?</v>

00:15:28.742 --> 00:15:33.662
<v Val Levitan>Uh, if we we we go already to talk through it.</v>

00:15:34.822 --> 00:15:35.942
<v Genadi Peari>Data.</v>

00:15:36.902 --> 00:15:37.782
<v Val Levitan>But I must BC.</v>

00:15:38.342 --> 00:15:39.142
<v Genadi Peari>Msbc.</v>

00:15:39.782 --> 00:15:40.142
<v Val Levitan>No.</v>

00:15:40.102 --> 00:15:51.622
<v Genadi Peari>It's on a dinner set up a problem, was correct, but the monitor pushed to Msbc, and then if we keep it there as a reference.</v>

00:15:53.302 --> 00:15:55.862
<v Genadi Peari>Stone is a source of truth, a bill of material.</v>

00:15:53.702 --> 00:15:54.262
<v Val Levitan>Show.</v>

00:16:00.182 --> 00:16:01.222
<v Val Levitan>Kakoy truth.</v>

00:16:01.862 --> 00:16:04.502
<v Genadi Peari>Source of truth in the instances.</v>

00:16:05.542 --> 00:16:09.182
<v Val Levitan>Engineering bill of material in a commercial bill of material.</v>

00:16:10.302 --> 00:16:15.902
<v Genadi Peari>Production production.</v>

00:16:17.862 --> 00:16:18.742
<v Val Levitan>from Github.</v>

00:16:20.262 --> 00:16:21.862
<v Genadi Peari>So we need to keep it in Github.</v>

00:16:22.582 --> 00:16:30.022
<v Val Levitan>It's always on Github, not not bill of material, not bill of material, flat list of parts.</v>

00:16:31.742 --> 00:16:40.102
<v Genadi Peari>Production, they need the bill of material for.</v>

00:16:39.382 --> 00:16:43.462
<v Val Levitan>You, you can generate it on the fly from Github.</v>

00:16:44.182 --> 00:16:46.742
<v Genadi Peari>So every time generate from the scratch.</v>

00:16:47.862 --> 00:16:50.742
<v Val Levitan>Store that **** all the time. We got it all the time.</v>

00:16:50.182 --> 00:16:56.982
<v Genadi Peari>Every time, every time they go in to build monitor, Github will generate the bill of material.</v>

00:16:58.102 --> 00:17:01.782
<v Genadi Peari>Why? It's already in Msbc. We pushed it already once.</v>

00:17:03.062 --> 00:17:20.582
<v Val Levitan>So this video you pushed it. Primero. Primero. Nash's Msbc. Stories. Sub assembly.</v>

00:17:21.382 --> 00:17:26.502
<v Val Levitan>Bill of material, it's from flat to full.</v>

00:17:27.862 --> 00:17:41.702
<v Val Levitan>To show MSPC manufacturing bill of material, yes, my premier flat bill of material, yes, manufacturing bill of material assembly.</v>

00:17:47.942 --> 00:17:49.142
<v Val Levitan>We are pre-assembled.</v>

00:17:50.302 --> 00:17:51.462
<v Val Levitan>When are you?</v>

00:17:54.182 --> 00:17:59.942
<v Val Levitan>Manufacturing manufacturing component.</v>

00:18:02.422 --> 00:18:03.382
<v Genadi Peari>Nathan Inna.</v>

00:18:05.022 --> 00:18:05.862
<v Genadi Peari>But then you love.</v>

00:18:06.662 --> 00:18:07.142
<v Val Levitan>Okay.</v>

00:18:08.942 --> 00:18:09.822
<v Genadi Peari>You know the...</v>

00:18:11.142 --> 00:18:28.022
<v Genadi Peari>You know, in the reference of Sigda, Pastani, Cox, right, Machino, at a push once, you keep it.</v>

00:18:23.062 --> 00:18:23.702
<v Val Levitan>Such a.</v>

00:18:29.142 --> 00:18:33.142
<v Val Levitan>At the show, at the show, at the show, from Github.</v>

00:18:29.302 --> 00:18:30.022
<v Genadi Peari>What is?</v>

00:18:37.222 --> 00:18:46.102
<v Genadi Peari>Production order, not the deal at Cardana, but the light machine, no video in your reference with the production order, bill of material for production order.</v>

00:18:48.502 --> 00:18:49.382
<v Genadi Peari>Costa yani.</v>

00:18:51.782 --> 00:18:53.382
<v Genadi Peari>And approved and final.</v>

00:18:57.142 --> 00:18:58.262
<v Genadi Peari>No product.</v>

00:19:00.982 --> 00:19:05.622
<v Val Levitan>When you get that, when you get done, you find a substitution of parts.</v>

00:19:01.062 --> 00:19:01.862
<v Genadi Peari>Kirsten.</v>

00:19:06.102 --> 00:19:17.382
<v Genadi Peari>On final, what picture? It needs to be a picture of what has been sent.</v>

00:19:19.542 --> 00:19:25.382
<v Val Levitan>Yeah, but let me ask source of truth at the Github.</v>

00:19:28.742 --> 00:19:36.822
<v Genadi Peari>everything, but for bill of material.</v>

00:19:36.542 --> 00:19:39.222
<v Val Levitan>No, when is nice when you got a sit in your robot today?</v>

00:19:39.462 --> 00:19:40.102
<v Genadi Peari>Probably.</v>

00:19:43.622 --> 00:19:47.462
<v Genadi Peari>Yeah, they want concrete new points with the visual problem.</v>

00:20:07.062 --> 00:20:09.862
<v Val Levitan>From the source of truth to me, I'm going to Github.</v>

00:20:11.022 --> 00:20:12.902
<v Val Levitan>Yeah, I think you will be as a ship.</v>

00:20:14.822 --> 00:20:16.902
<v Val Levitan>Cash the D, Monica.</v>

00:20:21.382 --> 00:20:29.302
<v Val Levitan>Yeah, developer.</v>

00:20:30.582 --> 00:20:32.302
<v Val Levitan>Uh, sister.</v>

00:20:35.862 --> 00:20:42.742
<v Val Levitan>Such interesting machine.</v>

00:20:44.662 --> 00:20:59.782
<v Val Levitan>The bill of material in the premier VRCM machine in the vertical 43 in Georgia, 27 VLT South Dakota.</v>

00:21:03.238 --> 00:21:08.878
<v Val Levitan>Это между как собирается кот и как генерируется биолог материл.</v>

00:21:09.208 --> 00:21:13.568
<v Genadi Peari>Разница в том, что коды не собрали, после этого они его релиз.</v>

00:21:14.918 --> 00:21:17.118
<v Genadi Peari>Правильно и используется.</v>

00:21:19.078 --> 00:21:19.998
<v Val Levitan>То следующей переметой.</v>

00:21:20.828 --> 00:21:22.188
<v Val Levitan>До следующей ревизии.</v>

00:21:20.978 --> 00:21:22.778
<v Genadi Peari>Абсолютно верно.</v>

00:21:23.348 --> 00:21:34.228
<v Val Levitan>Они, простите, они у них другой код для Джорджия, другой код для saftoda. Какая разница код для сата или.</v>

00:21:35.638 --> 00:21:38.558
<v Val Levitan>Билов матируй для там какойто особой машины.</v>

00:21:39.728 --> 00:21:45.328
<v Val Levitan>В теории я не вижу разницы, какая разница они это генерируют, это называется.</v>

00:21:45.328 --> 00:21:56.008
<v Val Levitan>У них называется gicksting action, знают как генерируется, как собирается код для определённой juy sechin.</v>

00:21:58.208 --> 00:22:01.168
<v Val Levitan>Если он это постоянно без ошибок на лету.</v>

00:21:58.958 --> 00:21:59.768
<v Genadi Peari>Ну хорошо.</v>

00:22:02.818 --> 00:22:05.298
<v Val Levitan>Собирает это на лету собирает.</v>

00:22:06.588 --> 00:22:09.628
<v Val Levitan>Весь код вам во много 1000 линий.</v>

00:22:10.828 --> 00:22:13.028
<v Val Levitan>Почему они будут собирать белого мотивой?</v>

00:22:11.528 --> 00:22:11.728
<v Genadi Peari>Да.</v>

00:22:13.518 --> 00:22:17.518
<v Genadi Peari>Он этот код собирает абсолютно одинаково, каждый раз или по разному.</v>

00:22:18.208 --> 00:22:19.168
<v Val Levitan>Одинаково.</v>

00:22:19.398 --> 00:22:23.798
<v Genadi Peari>Вы результат одинаковый, но уверены, что количество линии не меняются.</v>

00:22:24.478 --> 00:22:32.358
<v Val Levitan>Уверен, потому что это они они, я вам скажу, почему я уверен, потому что они подписаны под тике чекса.</v>

00:22:32.708 --> 00:22:37.268
<v Val Levitan>Они не могут поменяться, ни одна точка не может поменяться, другой человек сам будет.</v>

00:22:38.468 --> 00:22:40.008
<v Genadi Peari>Новый код, новый чек сам.</v>

00:22:40.448 --> 00:22:49.208
<v Val Levitan>Нет один и тот же человек сам, потому что мне дают разрешение распространять код Андрей деспотии чек сам.</v>

00:22:50.468 --> 00:22:51.828
<v Val Levitan>И он должен совпадать?</v>

00:22:53.558 --> 00:22:54.958
<v Val Levitan>В эсапул фром.</v>

00:22:57.228 --> 00:22:58.028
<v Val Levitan>Делай.</v>

00:22:59.158 --> 00:22:59.848
<v Genadi Peari>Окей мало.</v>

00:23:00.858 --> 00:23:01.978
<v Genadi Peari>Хорошо, я не знаю.</v>

00:23:06.608 --> 00:23:07.648
<v Genadi Peari>Может быть.</v>

00:23:07.788 --> 00:23:11.028
<v Val Levitan>Я вам пытаюсь, просто аналогию продемонстрировать.</v>

00:23:14.338 --> 00:23:17.658
<v Genadi Peari>Я не вижу, что у нас тут.</v>

00:23:21.788 --> 00:23:25.188
<v Genadi Peari>Когда они делают новый код, это много работы.</v>

00:23:26.568 --> 00:23:39.608
<v Genadi Peari>Много времени, когда вы хотите открыть urisdicton текст from jorgia, например, и и 2 разных продукта у них разница будет там может быть в 3 харнеса.</v>

00:23:41.738 --> 00:23:42.458
<v Genadi Peari>Которые.</v>

00:23:43.158 --> 00:23:48.238
<v Genadi Peari>Меняются за 4 минуты, и потом этот код он живёт это.</v>

00:23:47.488 --> 00:23:59.958
<v Val Levitan>Ни дело, ни дело в том, что это меняется за 3 минуты. Здесь здесь много, что затянутое здесь хочется, чтоб был полный aliman chender.</v>

00:24:00.308 --> 00:24:04.308
<v Val Levitan>Очень, чтоб был полный лаймонд с переводом денег.</v>

00:24:04.868 --> 00:24:08.308
<v Val Levitan>Хочется, чтоб был полный лаймонд и нолоч бейс.</v>

00:24:09.398 --> 00:24:10.758
<v Val Levitan>Здесь много завязок.</v>

00:24:11.468 --> 00:24:15.268
<v Val Levitan>Ты был управки, работает 12 человек.</v>

00:24:16.108 --> 00:24:17.508
<v Val Levitan>А вы работаете один?</v>

00:24:19.838 --> 00:24:42.128
<v Genadi Peari>Этим пользуется потом и этот пёрли этот и продакшн, и этот и лев, и но они разные пользуются одним и тем же билов материал это как бы то, что они все пул эвритай я вам говорю, что это это сорс.</v>

00:24:33.848 --> 00:24:34.518
<v Val Levitan>Я я.</v>

00:24:38.878 --> 00:24:41.598
<v Val Levitan>Деньги надо Геннадий когда делается?</v>

00:24:42.668 --> 00:24:51.748
<v Val Levitan>Кино ты когда делается код им пользуются q им пользуются на каждом лкейшине программирует свою машину.</v>

00:24:52.188 --> 00:24:53.068
<v Val Levitan>То же самое.</v>

00:24:54.608 --> 00:24:55.288
<v Genadi Peari>Ну как?</v>

00:24:55.358 --> 00:25:01.518
<v Genadi Peari>Так что каждый когда пользуется, он пойдёт в genading билов материал, и каждый раз он будет генерить.</v>

00:25:00.518 --> 00:25:17.118
<v Val Levitan>На лету гетто кеннадия это на лету кетхаб есть в кидхаб есть акшинс, который генерирует этот колод энд плейс. Этот cold в ia sofile это становится iason как ваш билов материал вы говорите ваш билов материал.</v>

00:25:17.228 --> 00:25:19.068
<v Val Levitan>Вот это тот же i sofile.</v>

00:25:20.308 --> 00:25:24.948
<v Val Levitan>Который уже закрыт, вот вы говорите, кто сгенерирует этот билов матирил.</v>

00:25:26.248 --> 00:25:32.008
<v Val Levitan>Здесь генерируется ая софайл через gid через gickstions.</v>

00:25:33.958 --> 00:25:47.318
<v Val Levitan>Собирается лишь кот, и потом этот аесо мы отправляем, и он живет уже жизнью, постоянной жизнью. Пока чтото не поменялось в azor клауд.</v>

00:25:48.588 --> 00:26:00.468
<v Val Levitan>И отправляется куда хочешь ты можешь его на лету в USB засунуть и вставить в машину или ты просто можешь do. Вот Сейчас мы делаем через моду, мы сможем его просто don.</v>

00:26:01.828 --> 00:26:09.468
<v Val Levitan>Но живёт он в азор. Клауд то же самое, как он буший в Microsoft m sbc clowd.</v>

00:26:13.518 --> 00:26:16.478
<v Val Levitan>Но когда вы говорите, что является собственным чуть.</v>

00:26:17.818 --> 00:26:19.978
<v Val Levitan>Сортов чуд является гигант.</v>

00:26:20.948 --> 00:26:24.108
<v Val Levitan>Где он живёт или вазур потом или в эсбиси.</v>

00:26:25.088 --> 00:26:27.408
<v Val Levitan>Это уже мало что значит?</v>

00:26:37.918 --> 00:26:38.328
<v Genadi Peari>Хорошо.</v>

00:26:51.248 --> 00:26:55.048
<v Genadi Peari>У меня просто есть чувство, что мы немножко оторваны от реальности.</v>

00:26:56.328 --> 00:27:00.728
<v Genadi Peari>У миши до сих пор нету репорта, с которым он работает, а мы уже говорим про.</v>

00:27:02.368 --> 00:27:08.998
<v Val Levitan>У миши у миши пока нету репорта, пока ещё не всё налажено вы мы просто.</v>

00:27:09.188 --> 00:27:14.068
<v Val Levitan>Ну это ну это какойто подход странный это.</v>

00:27:09.408 --> 00:27:09.728
<v Genadi Peari>Ну.</v>

00:27:14.988 --> 00:27:20.228
<v Val Levitan>То, что у миши это одна проблема, у вас это другая проблема с кодом.</v>

00:27:20.228 --> 00:27:25.508
<v Val Levitan>Это 3 программа профитобило эти игр это 3, это ещё другая проблема.</v>

00:27:26.308 --> 00:27:30.668
<v Val Levitan>Очень компот киев бизнес здесь везде проблемы, всё проблемы.</v>

00:27:34.008 --> 00:27:39.848
<v Val Levitan>Это нельзя сказать, что хорошо вот мы сейчас наладим мишу, а потом мы сделаем это.</v>

00:27:43.698 --> 00:27:54.298
<v Val Levitan>Мишина проблема существует изза друг изза других вещей, которые да нужно адресовывать. Также важно, как и это, но совершенно идёт параллельно.</v>

00:27:44.928 --> 00:27:45.528
<v Genadi Peari>Я.</v>

00:27:57.048 --> 00:27:57.648
<v Genadi Peari>Ну.</v>

00:27:57.958 --> 00:28:06.518
<v Genadi Peari>Бал я это упомянул не как отдышную проблему, а как мне. Почемуто видится, что она связана, и это может ему ещё.</v>

00:28:06.598 --> 00:28:13.558
<v Val Levitan>Ну, безусловно, безусловно, она связана, но когда мы фиг с миши в проблему, это не значит, что вагонафикс эту проблему.</v>

00:28:14.378 --> 00:28:20.978
<v Val Levitan>Им иметь правильный сток или иметь правильный репорт. Инвентурий это совершенно другое дело.</v>

00:28:25.468 --> 00:28:25.848
<v Genadi Peari>А.</v>

00:28:25.808 --> 00:28:33.728
<v Val Levitan>И Мишина проблема тоже, я ещё не уверен на изза миши или изза лёвы или изза.</v>

00:28:35.158 --> 00:28:36.718
<v Val Levitan>Правильного физика. Аккаунт.</v>

00:28:38.508 --> 00:28:45.788
<v Val Levitan>Сегодня был интересный пример, когда я с вами переписывался, вы были в этом в копии сколько мониторов?</v>

00:28:46.828 --> 00:28:48.748
<v Val Levitan>57 или 65?</v>

00:28:49.748 --> 00:28:58.668
<v Val Levitan>Компьютер показывает 65. Она посчитала 57, когда миша сказал, дана, у меня компьютер показывает 65, она пошла и посчитала да 65.</v>

00:28:59.748 --> 00:29:11.868
<v Val Levitan>Я сейчас, например, завожу себе co о скоро этот керактер скоро эта персона заработает, эта персона будет толкать человека на спад чек недельный спад чек.</v>

00:29:13.868 --> 00:29:15.508
<v Val Levitan>Интерторе, park namberce.</v>

00:29:16.778 --> 00:29:27.408
<v Genadi Peari>Алтори парк нам бэрс это не то, что имел в виду это это я понимаю то, что вы говорите у него есть проблема сейчас вот то что вы написали давайте делать.</v>

00:29:27.478 --> 00:29:33.358
<v Genadi Peari>Хочу через месяц дипло и 100 perfers podact perfer prodax.</v>

00:29:34.478 --> 00:29:38.118
<v Genadi Peari>А миша говорит, а я не могу ничего делать с этим. У меня нет репорта.</v>

00:29:39.388 --> 00:29:40.868
<v Genadi Peari>Убилов материал.</v>

00:29:40.788 --> 00:29:46.398
<v Val Levitan>Но миша миша миша может с этим делать, просто миша становится в позу.</v>

00:29:46.508 --> 00:29:49.468
<v Val Levitan>Дайте мне рефорд, а потом я вам дам это.</v>

00:29:50.228 --> 00:29:55.468
<v Val Levitan>Я знаю как мне делать свою работу, не указывайте мне дайте мне репорт.</v>

00:29:56.228 --> 00:30:02.468
<v Val Levitan>Я понимаю, что миша делает, но это это детская дилетантная такая как бы.</v>

00:30:06.268 --> 00:30:07.068
<v Genadi Peari>А.</v>

00:30:10.778 --> 00:30:13.338
<v Genadi Peari>Посмотрите то, что вы говорите это.</v>

00:30:17.938 --> 00:30:19.218
<v Genadi Peari>Все maix seanse.</v>

00:30:20.518 --> 00:30:23.198
<v Genadi Peari>Ну просто её, когда хочется разбить на.</v>

00:30:23.878 --> 00:30:25.358
<v Genadi Peari>Морг лиер степс?</v>

00:30:25.958 --> 00:30:27.798
<v Genadi Peari>На на более простые степс.</v>

00:30:29.138 --> 00:30:32.218
<v Genadi Peari>Как мы тут и как мы идём туда?</v>

00:30:30.048 --> 00:30:31.168
<v Val Levitan>Так с этим?</v>

00:30:32.498 --> 00:30:37.738
<v Val Levitan>Да, с этим Я согласен, Я согласен, вы сами это не подтянете.</v>

00:30:37.978 --> 00:30:44.938
<v Val Levitan>Я хотел вам просто с вами встретиться и хотел вам объяснить концепт. Этот концерт легко подхватит.</v>

00:30:47.438 --> 00:30:47.958
<v Val Levitan>Нейтан.</v>

00:30:48.428 --> 00:30:54.828
<v Val Levitan>Ему будет очень легко с этим работать. Я сейчас позвоню ему. После этого я хотел с вами быть с первым поговорить.</v>

00:30:55.508 --> 00:31:03.868
<v Val Levitan>Я позвоню ему сейчас, назначу с ним митинг, я ему объясню этот канцлер и попрошу его имплементировать вот этот вот шёл.</v>

00:31:04.538 --> 00:31:05.418
<v Val Levitan>На.</v>

00:31:06.908 --> 00:31:08.068
<v Genadi Peari>На том проверю.</v>

00:31:08.388 --> 00:31:10.948
<v Val Levitan>Плей flax pay slan.</v>

00:31:12.778 --> 00:31:19.978
<v Val Levitan>Чтоб он наладил всё это и показал, и он сделает весь этот демонстрашен, и тогда вы на всё это посмотрите.</v>

00:31:22.018 --> 00:31:35.348
<v Genadi Peari>Вау вал только давайте мы не упустим очень важные важные вещи то, что мы говорили раньше, чтоб мы не побежали, забыв то, что мы уже хотели сделать. Очень важно правильно сделать флат.</v>

00:31:35.538 --> 00:31:39.178
<v Genadi Peari>Вот этот гитхабе, как это вы назвали флат лист.</v>

00:31:39.338 --> 00:31:40.098
<v Genadi Peari>В партс.</v>

00:31:41.018 --> 00:31:50.898
<v Genadi Peari>С правильным нумеровацией, чтоб можно было намберс по нашей системе продолжить оно прекрасно, всё работает, просто эти rull сдать ему плоду.</v>

00:31:51.728 --> 00:32:04.588
<v Genadi Peari>Правильно, правильно сделать фил слор, куда откуда пол ревижнс? Откуда pol droings? Вот это strockture rice как кирпичики и nishill brix это всё надо построить.</v>

00:32:04.738 --> 00:32:06.218
<v Genadi Peari>Чтобы это все было перфект.</v>

00:32:07.378 --> 00:32:10.778
<v Genadi Peari>И потом идти апп, ну так мне это я вижу.</v>

00:32:11.078 --> 00:32:13.308
<v Val Levitan>Я я, я не вижу в этом проблем это.</v>

00:32:13.538 --> 00:32:15.378
<v Val Levitan>Это это очень просто делается.</v>

00:32:16.218 --> 00:32:17.338
<v Val Levitan>Я не вижу плохо.</v>

00:32:16.298 --> 00:32:18.898
<v Genadi Peari>Да, это это просто.</v>

00:32:20.058 --> 00:32:24.658
<v Genadi Peari>Но оно, должно быть, уже уже ничего не мешает, чтобы это было.</v>

00:32:25.618 --> 00:32:30.258
<v Genadi Peari>И уже это можно будет давать использовать уже можно будет это для заказов использовать.</v>

00:32:30.658 --> 00:32:31.418
<v Genadi Peari>Faberricin.</v>

00:32:36.578 --> 00:32:38.738
<v Val Levitan>Я хотел просто вам это рассказать, чтобы.</v>

00:32:39.458 --> 00:32:40.058
<v Genadi Peari>Ну я.</v>

00:32:41.578 --> 00:32:48.458
<v Genadi Peari>Я понимаю, я понимаю, что вы говорите, я понимаю, что есть очень высокие копбелити су.</v>

00:32:49.898 --> 00:32:50.898
<v Genadi Peari>Укладывает.</v>

00:32:52.408 --> 00:32:52.948
<v Val Levitan>Просто.</v>

00:32:53.058 --> 00:33:03.098
<v Val Levitan>Всё, что я вам рассказываю, это двухгодичной давности в лучшем случае двухгодичной давности, но это ещё даже до мейнстрим не доходит.</v>

00:33:05.068 --> 00:33:06.988
<v Val Levitan>90% компаний.</v>

00:33:07.858 --> 00:33:09.578
<v Val Levitan>Вот про это даже не говорят.</v>

00:33:10.698 --> 00:33:12.698
<v Val Levitan>Да даже разговоров на эту тему нет.</v>

00:33:15.048 --> 00:33:19.128
<v Val Levitan>Потому что газ между экзенке инженеры огромнейший.</v>

00:33:21.628 --> 00:33:23.108
<v Val Levitan>Никто просто про это не говорит.</v>

00:33:25.698 --> 00:33:31.858
<v Val Levitan>Даже если ты берёшь консультанта, то пройти через все лейс не хватает даже бэнд.</v>

00:33:33.838 --> 00:33:36.478
<v Val Levitan>90% компаний про это не говорят.</v>

00:33:39.488 --> 00:33:44.208
<v Val Levitan>Поэтому то, что я говорю, кажется, что ну я б наверное с Марса откудато.</v>

00:33:45.058 --> 00:33:46.378
<v Val Levitan>Я ниоткуда не с Марса.</v>

00:33:53.098 --> 00:33:54.108
<v Genadi Peari>Есть такая книжка.</v>

00:33:56.198 --> 00:33:58.398
<v Genadi Peari>Мужчины с Марса, а женщины с Венеры.</v>

00:33:58.768 --> 00:34:00.188
<v Val Levitan>Женщины, Полина.</v>

00:34:00.458 --> 00:34:02.138
<v Genadi Peari>Да понятно.</v>

00:34:09.068 --> 00:34:09.668
<v Val Levitan>Окей.</v>

00:34:11.168 --> 00:34:11.648
<v Val Levitan>Окей.</v>

00:34:14.838 --> 00:34:15.398
<v Val Levitan>Всё.</v>

00:34:16.298 --> 00:34:17.418
<v Val Levitan>Я на этом закончен.</v>

00:34:18.658 --> 00:34:19.138
<v Val Levitan>Ничего.</v>

