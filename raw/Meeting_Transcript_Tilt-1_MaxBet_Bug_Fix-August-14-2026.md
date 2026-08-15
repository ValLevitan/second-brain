# Raw Transcript — Bug_Tilt-1 (Tilt-1 Max Bet Bug Fix)
**Date:** August 14, 2026, 11:30 AM ET
**Summary note:** [[Meeting_Notes_Tilt-1_MaxBet_Bug_Fix-August-14-2026]]
---
WEBVTT

00:00:15.844 --> 00:00:16.564
<v Pavel Frolov>Good morning.</v>

00:00:17.164 --> 00:00:18.084
<v Juan Martinez>Morning, everybody.</v>

00:00:18.404 --> 00:00:19.684
<v Val Levitan>Good afternoon, everyone.</v>

00:00:35.404 --> 00:00:36.564
<v Irina Shishko>Let me ask Lyashenko.</v>

00:00:37.604 --> 00:00:37.844
<v Juan Martinez>But.</v>

00:00:38.644 --> 00:00:38.804
<v Pavel Frolov>Yeah.</v>

00:00:38.644 --> 00:00:39.924
<v Irina Shishko>So.</v>

00:00:41.644 --> 00:00:42.484
<v Irina Shishko>Religious.</v>

00:00:45.724 --> 00:00:46.644
<v Val Levitan>Me out of it.</v>

00:00:49.204 --> 00:00:49.524
<v Irina Shishko>Ohh.</v>

00:00:55.244 --> 00:00:55.764
<v Irina Shishko>Mhm.</v>

00:00:57.284 --> 00:00:58.804
<v Irina Shishko>No.</v>

00:01:00.804 --> 00:01:02.164
<v Val Levitan>Okay, tell us.</v>

00:01:03.844 --> 00:01:04.284
<v Pavel Frolov>Payables.</v>

00:01:04.802 --> 00:01:07.162
<v Pavel Frolov>Liam, it was an idea.</v>

00:01:08.922 --> 00:01:20.042
<v Pavel Frolov>Because originally we found in dump and in reports that it was different, but value.</v>

00:01:22.522 --> 00:01:25.722
<v Pavel Frolov>Looks like player tried to play on.</v>

00:01:26.922 --> 00:01:34.882
<v Pavel Frolov>Fifty cents, but in history it was a value equal to $3.</v>

00:01:36.122 --> 00:01:53.402
<v Pavel Frolov>So Irina tried to reproduce it, trying to push immediately breadth equal to 50 cents and try to play on max bet value.</v>

00:01:54.402 --> 00:02:08.922
<v Pavel Frolov>and actually found that in some cases it could be accepted, pressing MaxBet immediately with other bet variable.</v>

00:02:10.282 --> 00:02:14.442
<v Irina Shishko>Play, play, but button and the mugs back.</v>

00:02:17.322 --> 00:02:17.802
<v Irina Shishko>Yeah.</v>

00:02:19.322 --> 00:02:20.282
<v Irina Shishko>Come, listen.</v>

00:02:21.882 --> 00:02:22.922
<v Val Levitan>I, I don't understand.</v>

00:02:25.562 --> 00:02:26.682
<v Juan Martinez>Yeah, I can.</v>

00:02:25.802 --> 00:02:26.802
<v Irina Shishko>No, Irina.</v>

00:02:27.842 --> 00:02:28.522
<v Juan Martinez>No, go Irina.</v>

00:02:32.042 --> 00:02:33.482
<v Irina Shishko>Play.</v>

00:02:34.762 --> 00:02:52.842
<v Irina Shishko>E Max bet.</v>

00:02:43.242 --> 00:02:44.682
<v Pavel Frolov>Doing a person.</v>

00:02:55.890 --> 00:03:13.410
<v Irina Shishko>Ну вот попасть в такой вот я не знаю даже как это сказать промежуток или что в такую ситуацию. И тогда у нас срабатывает первоначально маленький бет, а потом отправляется вот этот большой бет и фреймворк. Это самое конфликтует.</v>

00:03:14.160 --> 00:03:15.600
<v Irina Shishko>Ну 2 ставки.</v>

00:03:16.280 --> 00:03:25.640
<v Irina Shishko>После репута уже и математика подтягивается и говорит, да, там в игре одна математика, ты мне теперь другую математику подсовываешь.</v>

00:03:26.600 --> 00:03:30.760
<v Irina Shishko>Вот получается, вот этот вот конфликт в беттах и математике.</v>

00:03:31.960 --> 00:03:59.160
<v Irina Shishko>Логи мы, которые как бы вот получились с нашей машиной, плюс то, что с продакшн они идентичные после ребута и скрины то же самое. То есть там мы смогли вчера с это с Элизабет достать скрины с хистори с транзакшен это самое логи, поэтому как бы мы к этому и пришли, имея вот эту вот всю информацию, что это где то вот здесь вот рядом.</v>

00:03:59.890 --> 00:04:01.010
<v Irina Shishko>Между плей и максбет.</v>

00:04:02.650 --> 00:04:04.210
<v Irina Shishko>Этого конфликт.</v>

00:04:07.780 --> 00:04:09.740
<v Irina Shishko>Этот самый Антон.</v>

00:04:09.680 --> 00:04:17.340
<v Val Levitan>Тьфу тьфу тьен макс бэт аренд клоус просимери вот вами надо.</v>

00:04:17.690 --> 00:04:25.370
<v Val Levitan>Я физиков беллари whare а плеер danote yous wonfing abotin eber.</v>

00:04:26.250 --> 00:04:31.210
<v Val Levitan>Lopet mores corporate no screen tasbort patins the samen time.</v>

00:04:32.090 --> 00:04:44.050
<v Val Levitan>Да я форст play beater rich forest, martinal erier, danda martberd martbber фолз chartley freen work ges confutsust.</v>

00:04:45.130 --> 00:04:51.290
<v Val Levitan>Автор и сэр да я маф энд конференц это возле конфликта, неинформацион.</v>

00:04:51.970 --> 00:04:52.810
<v Val Levitan>Это.</v>

00:04:58.540 --> 00:04:58.860
<v Val Levitan>Стоп.</v>

00:05:10.662 --> 00:05:10.822
<v Irina Shishko>No.</v>

00:05:12.262 --> 00:05:14.262
<v Irina Shishko>Sepulveda.</v>

00:05:24.742 --> 00:05:29.142
<v Val Levitan>The bug, the bug has already been fixed by Anton.</v>

00:05:30.262 --> 00:05:33.062
<v Val Levitan>Irina is compiling this version.</v>

00:05:34.422 --> 00:05:37.862
<v Val Levitan>Do we need to go through Eclipse?</v>

00:05:40.102 --> 00:05:59.302
<v Pavel Frolov>For this particular case, we can inject this fix on current ISO, but we previously discussed this. What bugs should we fix immediately and what bugs should we postpone until?</v>

00:06:00.582 --> 00:06:05.462
<v Pavel Frolov>Uh, Giorgi, I think this is only one back.</v>

00:06:06.582 --> 00:06:11.622
<v Pavel Frolov>That we can urgently implement and deliver.</v>

00:06:12.902 --> 00:06:23.142
<v Juan Martinez>Yeah, I would say if what you're describing resolves the tilt one software error, then yeah, that should be the highest priority.</v>

00:06:24.022 --> 00:06:24.822
<v Val Levitan>Do it now.</v>

00:06:26.982 --> 00:06:34.902
<v Val Levitan>One organized Felipe to switch it right away on the 10 machines. I'm only concerned with the 10 machines over the weekend.</v>

00:06:31.062 --> 00:06:31.542
<v Juan Martinez>Okay.</v>

00:06:36.822 --> 00:06:40.262
<v Val Levitan>That's my concern. The rest, I agree.</v>

00:06:41.222 --> 00:06:42.902
<v Val Levitan>Groom it, test it.</v>

00:06:45.702 --> 00:06:50.822
<v Val Levitan>Group it together with V3 release, go through Eclipse.</v>

00:06:52.022 --> 00:06:57.542
<v Val Levitan>Updated, new sales will go into V3, V2 dies finished.</v>

00:06:59.142 --> 00:07:12.422
<v Juan Martinez>And quick question, so whatever update you'll do in CMS, they will have to just re-download a new RIS file, a new installation file, and that will contain the fix?</v>

00:07:01.462 --> 00:07:01.782
<v Val Levitan>Go.</v>

00:07:13.622 --> 00:07:17.622
<v Juan Martinez>Or I mean, or do we need to reinstall the ISO as well?</v>

00:07:18.022 --> 00:07:25.542
<v Pavel Frolov>Need to reinstall ISO, but you can use the same array assessments.</v>

00:07:26.822 --> 00:07:27.222
<v Juan Martinez>Okay.</v>

00:07:29.942 --> 00:07:33.142
<v Juan Martinez>And we think that the ISO file will be available today.</v>

00:07:36.662 --> 00:07:44.182
<v Pavel Frolov>I hope so because I will not be available tomorrow and day after tomorrow. So I will be doing this today.</v>

00:07:37.382 --> 00:07:38.182
<v Irina Shishko>No.</v>

00:07:45.462 --> 00:07:59.542
<v Juan Martinez>And there's no guarantee on our side that the customers will let us do anything on a Friday. And because if we have to do a full software install Val, that means a new co-MID, they got to call Intralat and go through the whole process.</v>

00:08:01.062 --> 00:08:02.902
<v Val Levitan>Yeah, probably not.</v>

00:08:04.102 --> 00:08:07.222
<v Val Levitan>But let's have it, let's have it handy, let's have it in our hands.</v>

00:08:08.062 --> 00:08:08.502
<v Juan Martinez>Absolutely.</v>

00:08:11.142 --> 00:08:13.622
<v Val Levitan>Okay, good job, good job, good job.</v>

00:08:12.902 --> 00:08:13.102
<v Pavel Frolov>Thind.</v>

00:08:14.022 --> 00:08:18.742
<v Juan Martinez>Just send me a message when the ISO is ready, and I'll make sure Felipe gets it.</v>

00:08:20.182 --> 00:08:20.582
<v Pavel Frolov>Okay.</v>

00:08:22.022 --> 00:08:33.302
<v Val Levitan>Pavel, can you, I mean, Andrei is updating me in writing, but can you update me right now since we have this conference call? Can you update me on flex recycler?</v>

00:08:22.062 --> 00:08:22.422
<v Juan Martinez>Two.</v>

00:08:34.342 --> 00:08:41.062
<v Pavel Frolov>Can we join with Andrei together? Because I do not know probably updated the data from him.</v>

00:08:37.462 --> 00:08:38.262
<v Val Levitan>Yeah, okay.</v>

00:08:40.822 --> 00:08:43.382
<v Val Levitan>I'll organize the call now for the team.</v>

00:08:43.062 --> 00:08:43.462
<v Pavel Frolov>Yes.</v>

00:08:44.262 --> 00:08:45.622
<v Val Levitan>Wait for another invitation.</v>

00:08:44.582 --> 00:08:45.062
<v Juan Martinez>Thanks.</v>

