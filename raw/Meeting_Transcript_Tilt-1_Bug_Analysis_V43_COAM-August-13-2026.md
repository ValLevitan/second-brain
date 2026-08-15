# Raw Transcript — Tilt-1_analysis
**Date:** August 13, 2026, 9:05–9:25 AM Eastern
**Summary note:** [[Meeting_Notes_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026]]
---
WEBVTT

00:00:07.823 --> 00:00:10.223
<v Val Levitan>So, for my benefit...</v>

00:00:11.423 --> 00:00:15.783
<v Val Levitan>I would like to understand and to align myself with.</v>

00:00:16.863 --> 00:00:21.023
<v Val Levitan>the recent bugs that we discovered in the...</v>

00:00:23.983 --> 00:00:30.383
<v Val Levitan>testing of the 10 machines, as we refer to those machines, version two.</v>

00:00:31.583 --> 00:00:36.303
<v Val Levitan>Uh, for Georgia Coam for V.43.</v>

00:00:38.863 --> 00:00:44.783
<v Val Levitan>So, I understand that originally we thought that there was a tilt one.</v>

00:00:46.063 --> 00:00:52.223
<v Val Levitan>bug, but when we started to look at it, we discovered 3 unrelated bugs.</v>

00:00:57.103 --> 00:00:59.183
<v Val Levitan>Oh, I just would like to understand.</v>

00:01:00.423 --> 00:01:02.783
<v Val Levitan>What does the nature of those bugs?</v>

00:01:04.943 --> 00:01:07.703
<v Val Levitan>What may have caused their appearance?</v>

00:01:11.823 --> 00:01:14.463
<v Val Levitan>and how we can rectify it.</v>

00:01:17.903 --> 00:01:19.583
<v Val Levitan>And what do we do in the meantime?</v>

00:01:25.023 --> 00:01:34.463
<v Juan Martinez>And just a question for me, so it's now happened on 2 out of 10 machines. Will it happen on the rest of them? It's just a matter of time?</v>

00:01:38.783 --> 00:01:39.423
<v Pavel Frolov>GM.</v>

00:01:40.383 --> 00:01:40.543
<v Val Levitan>Yeah.</v>

00:02:15.183 --> 00:02:35.023
<v Pavel Frolov>So, Evgeniy said that actually when machine will arrive to Georgia office and Felipe will connect it to the internet remotely and we can collect logs and make some investigation, it will be more</v>

00:02:35.343 --> 00:02:48.783
<v Pavel Frolov>useful and we will understand more. But for now, when Irina tried to reproduce this behavior, she found at least three bugs.</v>

00:02:49.863 --> 00:02:55.103
<v Pavel Frolov>Probably they related to production, probably not.</v>

00:02:58.543 --> 00:02:59.343
<v Pavel Frolov>Ohh...</v>

00:02:59.543 --> 00:03:02.303
<v Val Levitan>Let me, let me say it, let me say it differently.</v>

00:03:09.343 --> 00:03:28.903
<v Val Levitan>Until we take, until we assess the logs that we took from the machines, we cannot say with certainty that the bugs that Irina found independently by trying to reproduce the bug in the QA department in Minsk.</v>

00:03:29.103 --> 00:03:39.263
<v Val Levitan>relates to the bug that will be discovered in the second machine. Chances are that it could be, but there's always a chance that maybe she discovered something else.</v>

00:03:40.383 --> 00:03:45.263
<v Val Levitan>In the meantime, we know of three bugs that are reproducible.</v>

00:03:46.863 --> 00:03:50.303
<v Val Levitan>And they are what, how are they labeled?</v>

00:03:53.263 --> 00:03:55.663
<v Pavel Frolov>Irina, could you guide us?</v>

00:03:54.783 --> 00:03:59.903
<v Val Levitan>I, I, I actually three three.</v>

00:04:01.583 --> 00:04:03.903
<v Val Levitan>Three Baga.</v>

00:04:06.703 --> 00:04:07.023
<v Irina Shishko>Ohh.</v>

00:04:12.503 --> 00:04:14.463
<v Val Levitan>For, for, I may talk back another one.</v>

00:04:15.103 --> 00:04:18.063
<v Pavel Frolov>For Giorgi.</v>

00:04:19.896 --> 00:04:25.376
<v Val Levitan>И не описание, а как как название этих багов там, например, филд один, что там ещё?</v>

00:04:20.606 --> 00:04:21.046
<v Irina Shishko>А.</v>

00:04:27.366 --> 00:04:39.486
<v Irina Shishko>А ну 1 Тел это самое 1 бак это thind один, но как бы я сразу объясню что tillt один это если мы не знаем.</v>

00:04:40.156 --> 00:04:50.636
<v Irina Shishko>Как этот бак называть от чего, почему он случается? Мы спишем просто tilltoдин, это такое общее название для всех, не да для всех неизвестных багов.</v>

00:04:46.946 --> 00:04:47.496
<v Pavel Frolov>Дженерал.</v>

00:04:51.436 --> 00:04:57.516
<v Irina Shishko>Поэтому то, что мы 1 получили это тилтодин, он случается.</v>

00:04:58.476 --> 00:05:05.956
<v Irina Shishko>Если мы сасо выключаем все игры на машине, которая сейчас есть в какомлибо продукте.</v>

00:05:16.416 --> 00:05:21.346
<v Val Levitan>Ну это тяжело мне себе представить, что поле выключают все игры.</v>

00:05:21.736 --> 00:05:22.216
<v Val Levitan>Поле.</v>

00:05:23.566 --> 00:05:28.166
<v Irina Shishko>Так делают в этом в сауздакоте.</v>

00:05:28.716 --> 00:05:41.916
<v Irina Shishko>Если они хотят заблокировать машину, они автоматом выключают все игры, а потом блокируют, блокируется машина. Это пришло к нам с полей. Это не не мы придумали такой кейс.</v>

00:05:43.456 --> 00:05:46.146
<v Val Levitan>Но филтатин мы нашли?</v>

00:05:48.976 --> 00:05:49.616
<v Val Levitan>Джорджи.</v>

00:05:53.026 --> 00:05:56.306
<v Irina Shishko>Да вот мы почему?</v>

00:05:54.026 --> 00:05:57.066
<v Val Levitan>Там там же, там даже легко все машины не выключают.</v>

00:05:59.536 --> 00:06:11.016
<v Irina Shishko>Почему мы нашли этот кейс, потому что Филипп в одном из описаний сказал, что они блокируют машину? Так, ну интролод блокируют машину.</v>

00:06:11.676 --> 00:06:15.476
<v Irina Shishko>Потому что получают весь матч сигныча.</v>

00:06:16.676 --> 00:06:28.676
<v Irina Shishko>2 пути заблокировать машину это либо просто отправить лонг заблокирую машину либо 2 вариант. Вот как делают в сауз дакоте выключают те игры.</v>

00:06:29.676 --> 00:06:32.316
<v Irina Shishko>Просто отправляют выключи, выключи, выключи выключа.</v>

00:06:35.156 --> 00:06:35.596
<v Irina Shishko>Вот.</v>

00:06:37.026 --> 00:06:37.496
<v Val Levitan>Пока.</v>

00:06:38.236 --> 00:06:50.356
<v Irina Shishko>Поэтому мы как бы вот попробовали здесь повторить. Ну точно так же блокировать машины и получили 1 бак. Это если блокировать машины thilt один.</v>

00:06:51.116 --> 00:06:54.956
<v Irina Shishko>Когда из одного продукта сразу все игры выключаются.</v>

00:06:55.916 --> 00:07:03.036
<v Irina Shishko>А 2 это мы как бы выяснили то, что в полях делает обходной путь для разблокировки машины.</v>

00:07:04.626 --> 00:07:13.506
<v Irina Shishko>Есть у нас вот эта вот лазейка. Если интерлот заблокировал машину, пойти в setap сначала поставить.</v>

00:07:14.966 --> 00:07:23.526
<v Irina Shishko>Аутов сервис выйти из сетапатом, вернуться обратно в seap и сказать машина voperation и машина в машине.</v>

00:07:25.406 --> 00:07:26.006
<v Irina Shishko>Станет операшен.</v>

00:07:28.296 --> 00:07:28.496
<v Val Levitan>То есть.</v>

00:07:28.506 --> 00:07:29.226
<v Pavel Frolov>Тепироваться VPN?</v>

00:07:31.386 --> 00:07:33.106
<v Irina Shishko>А сейчас я выключу.</v>

00:07:37.396 --> 00:07:37.876
<v Val Levitan>Тольс.</v>

00:07:38.766 --> 00:07:40.286
<v Val Levitan>То есть мы нашли?</v>

00:07:41.006 --> 00:07:42.966
<v Val Levitan>Когда вы говорите обходной путь?</v>

00:07:43.926 --> 00:07:46.166
<v Val Levitan>Он в принципе неправильно, да это.</v>

00:07:47.706 --> 00:07:48.586
<v Pavel Frolov>Поэтому табак.</v>

00:07:47.916 --> 00:07:49.006
<v Irina Shishko>Ну да.</v>

00:07:49.076 --> 00:08:01.196
<v Irina Shishko>Да потому что ну как бы интролод заблокировал машину посчитал нужным, а техник просто может сходить туда сюда пощёлкать она станет это самое опирейшена.</v>

00:07:54.586 --> 00:07:55.426
<v Val Levitan>Пока я понял.</v>

00:08:00.336 --> 00:08:00.976
<v Val Levitan>Я Панда.</v>

00:08:02.326 --> 00:08:02.886
<v Val Levitan>Я понял.</v>

00:08:04.286 --> 00:08:06.246
<v Val Levitan>Уж окей, так это 2.</v>

00:08:07.036 --> 00:08:09.596
<v Irina Shishko>Да 2 и 3.</v>

00:08:07.206 --> 00:08:08.006
<v Val Levitan>Банк.</v>

00:08:10.236 --> 00:08:20.396
<v Irina Shishko>Если на машине выключили игру, но по какойто причине ребутнули машину, то при загрузке она появится обратно, её можно играть.</v>

00:08:20.836 --> 00:08:24.276
<v Irina Shishko>Хотя она должна оставаться выключенная игра.</v>

00:08:24.916 --> 00:08:29.596
<v Irina Shishko>И если мы зайдём в сетап и вернёмся, то она станет, ну будет выключена.</v>

00:08:37.296 --> 00:08:40.296
<v Juan Martinez>Хотя гдето счет другой даренника.</v>

00:08:40.216 --> 00:08:45.576
<v Pavel Frolov>А я вот не знаю соус forst bosi.</v>

00:08:46.656 --> 00:08:48.176
<v Pavel Frolov>Вэн.</v>

00:08:49.626 --> 00:08:51.866
<v Pavel Frolov>Гейм или геймс?</v>

00:08:52.976 --> 00:08:53.856
<v Pavel Frolov>А.</v>

00:08:55.936 --> 00:08:58.056
<v Pavel Frolov>Свичит оф байс.</v>

00:08:58.896 --> 00:09:09.216
<v Pavel Frolov>Что интролод и сенса с comand sto lock game one lock game to and son s one wi final allegte an tillt one.</v>

00:09:12.476 --> 00:09:12.926
<v Val Levitan>Но.</v>

00:09:20.639 --> 00:09:21.039
<v Juan Martinez>Um...</v>

00:09:20.639 --> 00:09:21.199
<v Pavel Frolov>Yes.</v>

00:09:22.639 --> 00:09:30.959
<v Juan Martinez>You're saying that they do? We have, or we saw an incoming signal from Interlock attempting to disable a specific game?</v>

00:09:31.439 --> 00:09:49.279
<v Pavel Frolov>Yeah, Juan, we do not know exactly, but when Irina tried to reproduce, she heard from Felipe that, for some reason, locking our machines due to signature.</v>

00:09:50.399 --> 00:10:07.919
<v Pavel Frolov>mismatch. That's why Irina and team tried to reproduce it by locking machine from SAS, directly locking all the machine, and then tried to lock game by game and found that this</v>

00:10:08.399 --> 00:10:12.399
<v Pavel Frolov>close to tilt one.</v>

00:10:14.159 --> 00:10:15.519
<v Val Levitan>Mobile.</v>

00:10:14.479 --> 00:10:27.199
<v Pavel Frolov>Because, because we have we have three different groups of games, and this is they cannot support showing group without games.</v>

00:10:28.319 --> 00:10:31.759
<v Pavel Frolov>That's why it leads to tilt one.</v>

00:10:35.999 --> 00:10:39.839
<v Val Levitan>I think it, I think it's important to add what Irina said in Russian.</v>

00:10:40.879 --> 00:10:41.519
<v Val Levitan>So.</v>

00:10:43.119 --> 00:10:46.799
<v Val Levitan>According to Irina, we learned.</v>

00:10:47.999 --> 00:10:51.719
<v Val Levitan>in particularly in South Dakota, which is a...</v>

00:10:53.119 --> 00:10:55.519
<v Val Levitan>Light and water system.</v>

00:10:57.919 --> 00:11:03.759
<v Val Levitan>that in particular in South Dakota, light and wonder could send</v>

00:11:05.439 --> 00:11:08.239
<v Val Levitan>either of the two commands.</v>

00:11:09.679 --> 00:11:13.919
<v Val Levitan>One command could be just block the machine.</v>

00:11:15.079 --> 00:11:21.439
<v Val Levitan>And another command could be block all the games on the machine one by one.</v>

00:11:21.639 --> 00:11:22.399
<v Pavel Frolov>Yeah, yeah.</v>

00:11:22.719 --> 00:11:23.279
<v Irina Shishko>Yes.</v>

00:11:23.919 --> 00:11:27.679
<v Pavel Frolov>But this is not one command. One command per game.</v>

00:11:28.559 --> 00:11:30.519
<v Val Levitan>Yes, so they they send.</v>

00:11:31.999 --> 00:11:36.879
<v Val Levitan>commands to disable one game at a time, one command at a time.</v>

00:11:38.799 --> 00:11:43.759
<v Val Levitan>So they could use either methodology of blocking the game.</v>

00:11:44.559 --> 00:11:45.119
<v Val Levitan>So...</v>

00:11:46.199 --> 00:11:54.959
<v Val Levitan>Irina is not saying that this is what's happening here in Georgia, but she just tried on her own.</v>

00:11:56.319 --> 00:12:01.759
<v Val Levitan>To send a command to block one game at a time, so multiple commands.</v>

00:12:02.959 --> 00:12:10.079
<v Val Levitan>one command per game. And when she did that, the game goes into tilt one.</v>

00:12:13.079 --> 00:12:17.199
<v Val Levitan>So, it's a discovery, but she also mentioned that.</v>

00:12:18.399 --> 00:12:21.919
<v Val Levitan>Tilt one is more of a general tilt.</v>

00:12:23.159 --> 00:12:26.159
<v Val Levitan>Like it, it's not, it's not very descriptive.</v>

00:12:29.119 --> 00:12:39.119
<v Juan Martinez>But the general meaning, you can clear it by just turning a reset key or anything like that. Is that what we mean? That it's not a, or the game is going to go out of service?</v>

00:12:37.039 --> 00:12:37.839
<v Val Levitan>No.</v>

00:12:39.839 --> 00:12:52.959
<v Val Levitan>No, general meaning, it's wide, it's broad, like it covers a lot of things. And it's difficult to narrow down on what tilt one is.</v>

00:12:56.559 --> 00:12:57.199
<v Juan Martinez>And then...</v>

00:12:56.639 --> 00:13:02.559
<v Val Levitan>By the way, parallel brings me to a point where when we're discussing Novo.</v>

00:13:04.719 --> 00:13:12.159
<v Val Levitan>Our tilt should be narrowly focused on our function rather than broad.</v>

00:13:17.439 --> 00:13:26.639
<v Val Levitan>But I don't want to public this meeting. I just want to say it for the record for the transcript so it migrates into Nova discussion.</v>

00:13:21.679 --> 00:13:21.919
<v Irina Shishko>Mm.</v>

00:13:28.559 --> 00:13:37.679
<v Val Levitan>But back here, so this is how Irina reproduce tilt one, but because tilt one is a broad tilt.</v>

00:13:41.519 --> 00:13:46.319
<v Val Levitan>There is no certainty that the tilt one that shows in Georgia.</v>

00:13:47.919 --> 00:13:56.879
<v Val Levitan>in the machine that is now in Felipe's office is the tilt one that Irina discovered in the QA department in this.</v>

00:14:00.319 --> 00:14:14.719
<v Val Levitan>But while she discovered tilt one in this particular execution, she also discovered that there is a flaw in how we...</v>

00:14:15.719 --> 00:14:18.559
<v Val Levitan>Take the machine out of the tilt one.</v>

00:14:20.159 --> 00:14:20.959
<v Val Levitan>Because.</v>

00:14:21.959 --> 00:14:22.479
<v Val Levitan>What?</v>

00:14:24.239 --> 00:14:27.119
<v Val Levitan>The in the current execution.</v>

00:14:28.559 --> 00:14:29.199
<v Val Levitan>You could.</v>

00:14:30.479 --> 00:14:32.319
<v Val Levitan>Put the machine out of service.</v>

00:14:34.319 --> 00:14:37.119
<v Val Levitan>Then, power machine on and off.</v>

00:14:39.119 --> 00:14:55.599
<v Val Levitan>Sorry, put machine out of service, then enable each all of the games, then take machine out of being out of service. Okay, whatever. There is a workaround that she described. It's not really important.</v>

00:14:49.199 --> 00:14:49.839
<v Irina Shishko>No.</v>

00:14:51.279 --> 00:14:51.679
<v Irina Shishko>Yep.</v>

00:14:56.679 --> 00:14:57.679
<v Val Levitan>which needs to be fixed.</v>

00:14:59.279 --> 00:15:04.719
<v Val Levitan>So that's problem #2. And what's the problem #3? Again, remind me.</v>

00:14:59.359 --> 00:14:59.839
<v Irina Shishko>Mhm.</v>

00:15:05.279 --> 00:15:10.479
<v Pavel Frolov>Blocked game after power off becomes available. That's wrong.</v>

00:15:05.599 --> 00:15:06.159
<v Irina Shishko>Uh, yeah.</v>

00:15:10.159 --> 00:15:13.039
<v Val Levitan>Oh, that's no, that's #2. What's #3?</v>

00:15:12.719 --> 00:15:19.919
<v Pavel Frolov>It's 3, it's #3. Number 2, machine can be enabled.</v>

00:15:15.039 --> 00:15:16.159
<v Irina Shishko>Yeah, no, the...</v>

00:15:21.279 --> 00:15:41.199
<v Pavel Frolov>even blocked machine by switching to out of service and then to the operational, yes, this number two. And #3, when the game is blocked and the machine is powered off and then powered on.</v>

00:15:25.439 --> 00:15:28.479
<v Val Levitan>That's what I said, and that's number two then.</v>

00:15:32.079 --> 00:15:32.719
<v Val Levitan>Yes, I'm not.</v>

00:15:41.919 --> 00:15:43.839
<v Pavel Frolov>This game becomes available.</v>

00:15:44.639 --> 00:15:45.599
<v Pavel Frolov>That should not be.</v>

00:15:48.159 --> 00:15:55.119
<v Juan Martinez>So, a power on is overriding the disabled command, possibly sent by the regulator. OK, yeah, we got that one, we got it.</v>

00:15:52.399 --> 00:15:54.079
<v Pavel Frolov>Yes, yes.</v>

00:15:59.599 --> 00:16:00.319
<v Juan Martinez>Understood.</v>

00:16:04.639 --> 00:16:19.199
<v Irina Shishko>No friends. You had to say my perfect. Research to let's yes. Leave a clear child Igor.</v>

00:16:32.119 --> 00:16:33.399
<v Irina Shishko>No, it is over an attack.</v>

00:16:36.319 --> 00:16:43.839
<v Pavel Frolov>So, currently, this set of games requires that each group.</v>

00:16:45.039 --> 00:16:51.439
<v Pavel Frolov>I need to have at least one game enabled and graphic user interface for game select screen.</v>

00:16:51.959 --> 00:16:52.319
<v Juan Martinez>Yes.</v>

00:16:53.439 --> 00:17:13.799
<v Pavel Frolov>should at least have this, at least one game in one group. So from the business perspective, we need to understand how to implement this option, blocking games and enabling games. How can we treat this case?</v>

00:17:15.439 --> 00:17:24.279
<v Pavel Frolov>Should we, instead of games, show some placeholder or a question mark or something else?</v>

00:17:25.359 --> 00:17:40.479
<v Juan Martinez>Yeah, I mean, I would say on the main game screen, the icon for that game theme, let's just say Queen of Luxorg, it should be grayed out, indicating to the player that, hey, this game is not currently available.</v>

00:17:42.319 --> 00:17:54.719
<v Irina Shishko>Please holder.</v>

00:17:50.919 --> 00:17:51.439
<v Pavel Frolov>Good, good.</v>

00:17:57.439 --> 00:17:57.839
<v Pavel Frolov>Ohh.</v>

00:17:59.359 --> 00:18:08.879
<v Pavel Frolov>So, Inna sent a picture showing how it implemented in South Dakota, yeah? South Dakota.</v>

00:18:08.399 --> 00:18:14.159
<v Irina Shishko>No, that.</v>

00:18:15.759 --> 00:18:17.119
<v Irina Shishko>**** the bull shoes.</v>

00:18:17.439 --> 00:18:22.719
<v Pavel Frolov>So this shows just blank card instead of a game card.</v>

00:18:29.199 --> 00:18:35.039
<v Pavel Frolov>So, I think we can implement this order or implement.</v>

00:18:34.159 --> 00:18:35.039
<v Juan Martinez>Yeah, that's fine.</v>

00:18:35.759 --> 00:18:48.959
<v Val Levitan>I think, I think, I think, I think that we shouldn't be implementing anything right now. We should look at your findings from the machine that was brought into the office and then have this conversation again.</v>

00:18:36.239 --> 00:18:38.079
<v Juan Martinez>Yeah, the the blank card is okay.</v>

00:18:49.359 --> 00:18:49.679
<v Juan Martinez>Yeah.</v>

00:18:51.999 --> 00:19:06.079
<v Val Levitan>Okay, so unless anything else to discuss, I think this meeting could be over and I'm going to let you investigate the machine in the office. I think that's the most acute.</v>

00:19:07.039 --> 00:19:08.799
<v Val Levitan>Point of infliction right now.</v>

00:19:09.599 --> 00:19:09.839
<v Juan Martinez>For.</v>

00:19:11.479 --> 00:19:14.639
<v Val Levitan>But this, this is the this is the most important priority.</v>

00:19:11.799 --> 00:19:12.239
<v Juan Martinez>Great.</v>

00:19:16.359 --> 00:19:16.719
<v Pavel Frolov>Okay.</v>

00:19:17.759 --> 00:19:27.839
<v Val Levitan>Okay, so keep us posted on what your findings will be. What is the goal right now? So the machine is connected. Now Pavel has to access the machine.</v>

00:19:30.399 --> 00:19:42.799
<v Pavel Frolov>Yes, I think I already used remote access yesterday with Andrei Klimovich. I think we just need to find this machine in business network and...</v>

00:19:43.759 --> 00:19:45.119
<v Pavel Frolov>Try to investigate it.</v>

00:19:45.839 --> 00:19:50.719
<v Val Levitan>OK, so if you find something, let us know. Thank you. Bye bye.</v>

00:19:50.079 --> 00:19:51.519
<v Pavel Frolov>OK, bye.</v>

00:19:50.159 --> 00:19:50.719
<v Juan Martinez>Thanks, Scott.</v>

00:19:51.839 --> 00:19:52.239
<v Irina Shishko>Bye.</v>
