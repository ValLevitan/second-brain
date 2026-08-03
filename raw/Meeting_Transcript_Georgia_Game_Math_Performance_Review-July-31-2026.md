# Raw Transcript — Game_Development
**Date:** July 31, 2026, 2:00 PM Eastern
**Summary note:** [[Meeting_Notes_Georgia_Game_Math_Performance_Review-July-31-2026]]
---
WEBVTT

00:00:11.478 --> 00:00:35.758
<v Michael Gottlieb>which look great and have nice animations, were not coming up nearly as much as we wanted. We were getting royals all over the place. So, which sucks because you're chasing the animals. Ultimately, you're chasing the bison and the big bear. But so we started by dropping the 10 out of the royals to kind of, and then shifted everything over, if you will.</v>

00:00:35.798 --> 00:00:57.838
<v Michael Gottlieb>one register. That made a small amount of improvement. But then the big thing we decided to do with this game is we're going to do fractional pays, which is to say pays less than a dollar. And before, it was a big deal. And before we went down that path, I talked to Efim and said, you know, what was the logic?</v>

00:00:39.318 --> 00:00:39.598
<v Val Levitan>Mm.</v>

00:00:50.038 --> 00:00:50.518
<v Juan Martinez>Mhm.</v>

00:00:58.238 --> 00:01:22.918
<v Michael Gottlieb>of the original, original Peach releases that were done that David did. And his response, well, it was based on some IGT games. And I said, well, were those IGT games particularly successful? And the answer was no, not necessarily. In the early, early days of Georgia, it was people kind of finding their way, right? So we are now doing fractional pays. So the net result is the</v>

00:01:15.918 --> 00:01:16.318
<v Juan Martinez>Sure.</v>

00:01:22.998 --> 00:01:30.318
<v Michael Gottlieb>oils come up significantly less. The animals are coming up quite frequently, which is really good.</v>

00:01:32.158 --> 00:01:50.878
<v Michael Gottlieb>And that is working now as it should. It's behaving the way that it should. The other thing that we did is that on reel 3, there's a precognition and that reel turns wild. And the frequency of that was not happening as often as we would have liked. So we bumped.</v>

00:01:50.958 --> 00:02:15.798
<v Michael Gottlieb>up that frequency. And then I sent Lena some notes this week on the behavior of how the bison should run across the screen and turn that real wild. So we're getting there. We're getting there. And free spins are a hammer. Free spins are a hammer. I'm really pleased with how they're playing. There's a couple of bugs that we need to get in there. We need to get the sound effect for when the bison locks and the snow and the ice comes around.</v>

00:02:02.798 --> 00:02:03.278
<v Juan Martinez>Mhm.</v>

00:02:15.798 --> 00:02:40.398
<v Michael Gottlieb>That looks really, really good. But we're cooking. We're getting there. So that was the big focus on that. And then for South Dakota, we went through how we were going to handle messaging to the player win capping. So that was a big topic of discussion because there's different combinations and permutations. Did you win cap and free spins? Did you win cap and free spins with the progressive?</v>

00:02:40.798 --> 00:02:48.318
<v Michael Gottlieb>pending. Did you win cap in the base game? Did you win cap in the base game with a progressive pending? So we came up with all the conditions and the behaviors and...</v>

00:02:47.158 --> 00:02:47.678
<v Juan Martinez>Avdeyev.</v>

00:02:49.678 --> 00:03:00.078
<v Michael Gottlieb>The REQ has been updated and so we made progress on that front and hopefully there's a new build. Lena, is there a new build hopefully in the next couple of days?</v>

00:02:53.838 --> 00:02:53.998
<v Juan Martinez>Igor.</v>

00:02:59.598 --> 00:03:00.158
<v Juan Martinez>People.</v>

00:03:00.238 --> 00:03:13.558
<v Lena Zhukova>It crashed yesterday and today on Bisons and promised me to send as soon as possible when it's working again. So I will send to a mediator.</v>

00:03:04.718 --> 00:03:04.878
<v Michael Gottlieb>Mm.</v>

00:03:04.718 --> 00:03:04.838
<v Val Levitan>Yeah.</v>

00:03:08.398 --> 00:03:08.878
<v Val Levitan>Book.</v>

00:03:11.758 --> 00:03:11.918
<v Efim Podvoiski>Mm.</v>

00:03:14.838 --> 00:03:26.478
<v Michael Gottlieb>Tyson was crashing on me too. It's kind of a pain in the *** because you have to clear out the docker, restart everything. You basically burn 10 minutes of jerking around and it takes you out of the, you know, out of the out of the flow.</v>

00:03:18.718 --> 00:03:19.038
<v Efim Podvoiski>Yeah.</v>

00:03:26.958 --> 00:03:27.718
<v Lena Zhukova>I understand.</v>

00:03:27.038 --> 00:03:36.958
<v Efim Podvoiski>If it is, sorry, if it's just animation crash, you probably can start just by killing framework and restarting framework.</v>

00:03:37.998 --> 00:03:40.558
<v Michael Gottlieb>I tried but it came up with the see attendant message.</v>

00:03:39.278 --> 00:03:43.838
<v Efim Podvoiski>Uh, sometimes, yeah, it depends on what actually happens, yeah.</v>

00:03:43.998 --> 00:03:46.238
<v Michael Gottlieb>Yeah, exactly. So it's like, what?</v>

00:03:45.358 --> 00:03:54.718
<v Lena Zhukova>Usually it's not working like 90% times it's not working when it crashes and you're just trying to start framework again at 90% is not working.</v>

00:03:49.758 --> 00:03:50.238
<v Efim Podvoiski>Or?</v>

00:03:51.998 --> 00:04:00.238
<v Efim Podvoiski>I understand, yeah, but I was lucky, so all the crashes I had was like just this animation, I just started framework.</v>

00:03:54.158 --> 00:03:54.558
<v Michael Gottlieb>Right.</v>

00:03:56.358 --> 00:03:56.638
<v Michael Gottlieb>Yeah.</v>

00:04:00.158 --> 00:04:22.398
<v Michael Gottlieb>Exactly. So it's like Clint Eastwood says, do you feel lucky, punk? You know, I mean, just clear out the damn Docker and start it over with life is too short. We've got to get this stuff. We've got to get this stuff done. So no, good, good across the board on that front. And then I guess from my perspective, two things I would like to touch on is this</v>

00:04:04.998 --> 00:04:05.198
<v Juan Martinez>Yeah.</v>

00:04:09.238 --> 00:04:09.438
<v Lena Zhukova>And.</v>

00:04:09.598 --> 00:04:09.918
<v Efim Podvoiski>Yeah.</v>

00:04:22.958 --> 00:04:40.478
<v Michael Gottlieb>this coming attraction video thing, Juan, that you and I talked about, just to, you know, talk to give the group a sense of what direction we want to go with that. And then if you have any insights or commentary on the performance of the products, any color, we're seeing numbers coming in. Some of them look pretty darn good to me.</v>

00:04:41.278 --> 00:05:00.678
<v Juan Martinez>Yeah, no, like Efim said, it's just, it's simply too early. You know, the data, some of the data is only two days, other machines are only six days. The longest data, I think, is 16 days. So we still just, we need another 30 days of data to come in before anything really starts to look.</v>

00:04:45.638 --> 00:04:45.838
<v Michael Gottlieb>And.</v>

00:04:46.838 --> 00:04:46.958
<v Val Levitan>Yeah.</v>

00:04:57.438 --> 00:04:57.998
<v Efim Podvoiski>Sure.</v>

00:05:01.038 --> 00:05:02.958
<v Juan Martinez>Like, it's conclusive, yeah.</v>

00:05:01.318 --> 00:05:02.078
<v Michael Gottlieb>and settle down.</v>

00:05:02.878 --> 00:05:13.278
<v Efim Podvoiski>But what is considered a good handle, daily handle in, does not handle, no daily hold in Georgia?</v>

00:05:14.238 --> 00:05:31.998
<v Juan Martinez>I color-coded whatever I, I'm using my arbitrary number of $1,500 for coin in and anything above $200 based on what customers expect and what they told us, you know, would be a solid number.</v>

00:05:26.318 --> 00:05:26.798
<v Efim Podvoiski>Mhm.</v>

00:05:32.558 --> 00:05:46.158
<v Efim Podvoiski>Oh, okay, 200 is tough. Yeah, 1500, 1500 we have, but this 9%, this only 9% hold, it's not, it doesn't translate into $200.00 and only it's only.</v>

00:05:35.398 --> 00:05:35.838
<v Juan Martinez>Yes.</v>

00:05:37.838 --> 00:05:38.638
<v Juan Martinez>Yeah, absolutely.</v>

00:05:44.798 --> 00:05:48.878
<v Juan Martinez>Correct. And sadly, it's not even 9%, it's actually 6%.</v>

00:05:49.198 --> 00:05:50.558
<v Efim Podvoiski>Oh, sorry.</v>

00:05:50.078 --> 00:05:54.358
<v Juan Martinez>I've replied to you. It's 92 base plus 2%.</v>

00:05:53.278 --> 00:05:57.598
<v Efim Podvoiski>Oh, I'm sorry, I missed 9292.</v>

00:05:55.838 --> 00:06:01.198
<v Juan Martinez>Yeah, yeah, 92 plus 2, 92 plus 2. We're at 94% all in.</v>

00:05:56.958 --> 00:05:57.998
<v Michael Gottlieb>Plus 2 to the meter.</v>

00:06:00.918 --> 00:06:07.118
<v Efim Podvoiski>Ohh, OK. I didn't realize it. OK, so, so we are very lucky in terms of holes so far.</v>

00:06:06.958 --> 00:06:08.158
<v Juan Martinez>Yes, yes.</v>

00:06:08.478 --> 00:06:16.118
<v Efim Podvoiski>They are just, yeah, they are just winning, as, as, as opposite as the players winning, yeah, they are, they are.</v>

00:06:11.598 --> 00:06:11.958
<v Juan Martinez>Yeah.</v>

00:06:15.358 --> 00:06:35.438
<v Juan Martinez>Yeah, yeah, we wanted to make the games as close to the original peach setups for those games are doing well. So that's why we went with this. And certainly, if the numbers start to slip, you know, we'll reduce the progressive by 1%. Then we can talk about reducing the base game percentages if needed.</v>

00:06:21.398 --> 00:06:21.598
<v Efim Podvoiski>Uh-huh.</v>

00:06:24.598 --> 00:06:25.118
<v Efim Podvoiski>Okay.</v>

00:06:36.398 --> 00:06:37.518
<v Efim Podvoiski>Mhm, mhm.</v>

00:06:37.278 --> 00:06:49.118
<v Michael Gottlieb>And the may I ask if do we know that the locations these are going in, are these replacing the previous peach vertical one that we released or are these new installs fresh?</v>

00:06:51.358 --> 00:06:57.838
<v Juan Martinez>Good question. I do believe they're new for the most part, but I'll confirm that.</v>

00:06:55.518 --> 00:06:55.998
<v Michael Gottlieb>Okay.</v>

00:07:07.998 --> 00:07:08.638
<v Juan Martinez>Yes.</v>

00:07:08.678 --> 00:07:11.118
<v Michael Gottlieb>Everybody in some of them, not as much.</v>

00:07:10.598 --> 00:07:29.758
<v Juan Martinez>Yeah, yeah, yeah. And then that's why I questioned some of the diamond locations, especially just seem to have very low coin in. So is this really a top tier? And it may, as Felipe put it in, we may be in their top tier and that's a good number for them, but not nothing like arc.</v>

00:07:19.838 --> 00:07:20.238
<v Michael Gottlieb>Yeah.</v>

00:07:29.798 --> 00:07:33.438
<v Juan Martinez>where we're seeing 4 or $5,000 coin in days, which is crazy.</v>

00:07:33.838 --> 00:07:54.158
<v Michael Gottlieb>That's just mind-blowing to me. But that's great. That's great. And I'm particularly pleased that we're seeing good numbers in some of these instances with the Jackpot Rush titles with the Add Any Bet, because that only gets better, right? As those meters just continue to run and people chase it, that only gets...</v>

00:07:36.318 --> 00:07:38.638
<v Juan Martinez>Yep, yeah, yep.</v>

00:07:48.798 --> 00:07:49.518
<v Juan Martinez>Absolutely.</v>

00:07:54.958 --> 00:08:17.518
<v Michael Gottlieb>better over time. And the, I mean, if we have to pull back on how much we feed the progressive meter for the match three, I get it, but I like that bonus. I think that bonus turned out really good. It is proportional to bet, which is, you know, I was explaining to Efim, I was playing Twin Bison and I took a roller coaster ride where I started with, you know, a dollar bet.</v>

00:08:17.918 --> 00:08:37.438
<v Michael Gottlieb>and I won and I moved up to a $2 bet, then a $5 bet. I crushed it in free spins and then I got all the way. I was betting 10 bucks a spin and at 10 bucks a spin, you start hitting that progressive a little more often and it feels really good. But it is what it is. You can only, you know, you can only give it to them.</v>

00:08:30.078 --> 00:08:30.198
<v Juan Martinez>Yeah.</v>

00:08:38.558 --> 00:08:48.718
<v Michael Gottlieb>so much. The most important thing is you're happy with the levels and the frequency and all that stuff. It's what you want, so, and it's right for the market, so that's the most important thing.</v>

00:08:42.558 --> 00:08:43.198
<v Juan Martinez>Yeah, yeah.</v>

00:08:44.398 --> 00:08:44.678
<v Juan Martinez>Yeah.</v>

00:08:49.278 --> 00:08:49.678
<v Juan Martinez>Gotcha.</v>

00:08:50.318 --> 00:08:54.958
<v Michael Gottlieb>Okay, so some degree of encouragement then on your part about how things are okay.</v>

00:08:53.198 --> 00:09:02.398
<v Juan Martinez>Oh, absolutely, yeah. I mean, this game has started out better than all the revised peach nudges, in my opinion. So that says something.</v>

00:09:03.518 --> 00:09:22.398
<v Michael Gottlieb>Yeah, well, I mean, it's every bit, we've touched all of it, right? I mean, it's got the, it's got liquid glass, it's got revised nudge, it's got match three, it's got a great catalog of games, it's got a broader, if you want hold and re-spin, if you want a quick hit style, I mean, there really is something for</v>

00:09:08.078 --> 00:09:08.358
<v Juan Martinez>Yeah.</v>

00:09:12.398 --> 00:09:12.798
<v Juan Martinez>Hmm.</v>

00:09:14.718 --> 00:09:15.038
<v Juan Martinez>Yeah.</v>

00:09:22.798 --> 00:09:43.678
<v Michael Gottlieb>everybody there, you know, for the most part. So, and I think that obviously this is a bigger discussion over time, but I would say thematically, we probably need to circle back around and take a look at more Egyptian themes, because I see our competitors going back heavy on the Egyptian themes. We have a couple of good Egyptian</v>

00:09:23.998 --> 00:09:26.638
<v Juan Martinez>Absolutely, yeah, yeah, yeah.</v>

00:09:41.118 --> 00:09:41.438
<v Juan Martinez>Yeah.</v>

00:09:43.798 --> 00:10:05.358
<v Michael Gottlieb>themes. They need to they need another pass at art. But I think we'll go back and take a look at Keops Wild and some of the other stuff that we've done and bring some more Egyptian themes into the mix. And as we said, they seem to go light on Chinese. It's okay to have one, but they tend to go light on the Chinese stuff. They're not nearly as</v>

00:09:47.198 --> 00:09:47.518
<v Juan Martinez>Yeah.</v>

00:10:01.038 --> 00:10:02.718
<v Juan Martinez>Yes, right.</v>

00:10:04.318 --> 00:10:04.758
<v Juan Martinez>Correct.</v>

00:10:06.158 --> 00:10:25.598
<v Michael Gottlieb>crazy about it as they used to be. And it seems, obviously the numbers are so preliminary, who the hell knows, but they don't hate horses. They don't hate rodeo, rodeo queen, rodeo spins. So I was already thinking we can continue to track that over time.</v>

00:10:14.958 --> 00:10:15.198
<v Juan Martinez>Yeah.</v>

00:10:17.358 --> 00:10:19.038
<v Juan Martinez>Right, right.</v>

00:10:20.438 --> 00:10:21.518
<v Juan Martinez>Yeah, yeah.</v>

00:10:25.918 --> 00:10:31.598
<v Michael Gottlieb>And if that works, we could take Jackpot Rush and make Jackpot Rodeo.</v>

00:10:26.158 --> 00:10:26.318
<v Val Levitan>Mm.</v>

00:10:32.318 --> 00:10:50.678
<v Juan Martinez>Sure, yeah, yeah, because I'm curious, I mean, because Rodeo Queen is also a very visually attractive game, but because we know this market is like 70% male, do they, are they embarrassed to play a cute blonde game?</v>

00:10:32.958 --> 00:10:34.478
<v Michael Gottlieb>We could do that. That's something we could...</v>

00:10:37.038 --> 00:10:37.358
<v Michael Gottlieb>Yeah.</v>

00:10:40.318 --> 00:10:40.878
<v Michael Gottlieb>Yes.</v>

00:10:45.678 --> 00:10:46.158
<v Michael Gottlieb>Right.</v>

00:10:51.038 --> 00:11:00.078
<v Juan Martinez>It's just, you know, too early to tell, but, you know, I'm surprised that Rodeo Queen isn't closer to the top like I expected it to be.</v>

00:11:00.558 --> 00:11:21.678
<v Michael Gottlieb>Yeah, well, and you never know. I mean, I have seen in these scenarios, women, in many instances, they bet less. They're not as aggressive. Bluntly, they don't drink as much. Their inhibitions don't get loosened up. They're not as comfortable losing as much money. They're not as impulsive and out of control as men and gambling as a general rule.</v>

00:11:08.958 --> 00:11:09.278
<v Juan Martinez>Yeah.</v>

00:11:22.238 --> 00:11:45.198
<v Michael Gottlieb>So guys will step up, they'll pump the machine full of money, and they'll bet heavy, and that affects the numbers for that game. And women, not as much in some instances. So something like a rodeo queen, it might have the same number of plays, but at a lower bet level, right? So then it's not necessarily ranking as high. But all that being said, the most important thing is, does it stick?</v>

00:11:22.398 --> 00:11:22.718
<v Juan Martinez>Oh.</v>

00:11:29.278 --> 00:11:29.438
<v Juan Martinez>Mm.</v>

00:11:32.238 --> 00:11:32.638
<v Juan Martinez>Yep.</v>

00:11:40.078 --> 00:11:40.718
<v Juan Martinez>Absolutely.</v>

00:11:45.518 --> 00:12:01.278
<v Michael Gottlieb>Does it stick? Does it stay? Do people come back to it? And so far, I haven't seen, I mean, the numbers are very, very early. We haven't found, I'm actually kind of surprised. We'll have to see, you know, are there any turkeys here? Is there anything that they absolutely just like, don't like at all and can't stand?</v>

00:11:45.918 --> 00:11:47.358
<v Juan Martinez>Right. Exactly.</v>

00:11:48.718 --> 00:11:49.038
<v Juan Martinez>Yeah.</v>

00:11:55.718 --> 00:11:55.918
<v Efim Podvoiski>It.</v>

00:11:58.478 --> 00:12:20.398
<v Juan Martinez>Yeah. No, I mean, you saw in the first couple of days, I said, okay, Ocho's at the bottom, what's going on here? But it's also been at the top at one location and certainly in the top four in a few locations. So I think people are playing everything, trying to find out what their new favorite game is. And it's just going to take a little bit more time. But</v>

00:12:20.398 --> 00:12:21.158
<v Efim Podvoiski>It's.</v>

00:12:20.718 --> 00:12:23.838
<v Juan Martinez>The spread is not too far apart from all the games.</v>

00:12:23.318 --> 00:12:42.478
<v Michael Gottlieb>No, no, the distribution is is is pretty is pretty smooth, and I think there's a there's a tale of multiple markets here. I think you've got Hispanic locations, and then I think you've got your your predominantly Caucasian, whatever you want to refer to it as. So, I think we just need to look at our mix and...</v>

00:12:25.678 --> 00:12:25.958
<v Juan Martinez>Yeah.</v>

00:12:28.278 --> 00:12:28.438
<v Juan Martinez>Yeah.</v>

00:12:33.798 --> 00:12:34.238
<v Juan Martinez>Yes.</v>

00:12:39.118 --> 00:12:40.478
<v Juan Martinez>Yeah, yeah.</v>

00:12:42.958 --> 00:13:02.958
<v Michael Gottlieb>and blend it. And maybe the cowboy rodeo thing crosses over, right? Because that is a very much part of Mexican culture. It's very much part of that Georgia, Southern culture. But I don't think we should be opposed, and I think like La Rosa still makes sense. There's going to be places where La Rosa works down there.</v>

00:12:47.518 --> 00:12:47.758
<v Juan Martinez>Yeah.</v>

00:12:52.238 --> 00:12:52.318
<v Juan Martinez>The.</v>

00:12:59.358 --> 00:13:00.958
<v Juan Martinez>Yeah, I agree.</v>

00:13:03.118 --> 00:13:03.758
<v Juan Martinez>Absolutely.</v>

00:13:03.318 --> 00:13:10.078
<v Michael Gottlieb>Because you've got the beautiful woman and you've got the, you know, the romance of the whole thing. So, cool.</v>

00:13:08.998 --> 00:13:09.598
<v Juan Martinez>Absolutely.</v>

00:13:11.598 --> 00:13:31.158
<v Michael Gottlieb>Cool. And then the Felipe had a comment and Juan's going to get some more data on this because you can't just like kind of go off half cocked. And this is really most important for you, Lena. Our competitors are...</v>

00:13:31.278 --> 00:13:37.598
<v Michael Gottlieb>running full screen attraction videos when there are no credits on the machine.</v>

00:13:38.158 --> 00:13:39.758
<v Lena Zhukova>Yeah, we will do it for retreat.</v>

00:13:38.558 --> 00:13:38.918
<v Michael Gottlieb>And...</v>

00:13:40.558 --> 00:13:43.198
<v Michael Gottlieb>I'm talking like no buttons at all, though.</v>

00:13:44.078 --> 00:13:47.758
<v Michael Gottlieb>No, no buttons during the attract mode.</v>

00:13:44.398 --> 00:13:44.958
<v Juan Martinez>Yeah, I...</v>

00:13:47.518 --> 00:13:50.158
<v Lena Zhukova>Ah, yes, yes, it's going to be full screen, yay.</v>

00:13:50.478 --> 00:13:52.958
<v Michael Gottlieb>Right. When will we start seeing that?</v>

00:13:55.638 --> 00:14:18.238
<v Lena Zhukova>When all games are like in their like final shape. So yeah, I think I planned for Vitaliy to start to record videos next week, starting from Jet Potrush games and Lines and Waves games, which are already like in good shape.</v>

00:14:01.838 --> 00:14:02.318
<v Michael Gottlieb>Okay.</v>

00:14:03.678 --> 00:14:04.238
<v Juan Martinez>But, but...</v>

00:14:04.878 --> 00:14:05.358
<v Michael Gottlieb>Good.</v>

00:14:18.558 --> 00:14:26.718
<v Lena Zhukova>And then, meanwhile, Lion and Bison will, we will fine-tune these two games, and...</v>

00:14:25.598 --> 00:14:44.998
<v Michael Gottlieb>Okay, could you move higher in priority, just taking, let's just call it a test video that would be representative, even if it isn't every, even if everything isn't perfect, just throw a test video in there, so in the build, so we can look at it and see how it behaves and verify that the length of time that it's up.</v>

00:14:44.478 --> 00:14:59.838
<v Lena Zhukova>You know, like for Anton, it will be like for him, it's better to focus on this task and create the full flow of this attraction. If you want, I can do it, but it will kind of, it will break his.</v>

00:14:57.278 --> 00:15:08.238
<v Michael Gottlieb>Oh, so you're saying that, so you're saying, sorry, sorry, sorry. So what you're saying is, is that Anton hasn't done the underlying code structure of it yet. Didn't understand that. Okay, okay, so.</v>

00:15:04.078 --> 00:15:04.478
<v Lena Zhukova>Mm.</v>

00:15:07.358 --> 00:15:10.638
<v Efim Podvoiski>And Anton is away for a week. He is on vacation.</v>

00:15:11.358 --> 00:15:12.158
<v Lena Zhukova>Next week.</v>

00:15:12.478 --> 00:15:13.038
<v Efim Podvoiski>Yes.</v>

00:15:13.238 --> 00:15:15.918
<v Lena Zhukova>Oh, I did not know this. Interesting.</v>

00:15:15.158 --> 00:15:19.998
<v Efim Podvoiski>And he just told me casually, I didn't, I didn't realize that he didn't tell everyone.</v>

00:15:18.118 --> 00:15:20.798
<v Lena Zhukova>Interesting. I don't have any note from him.</v>

00:15:21.278 --> 00:15:21.918
<v Efim Podvoiski>Okay.</v>

00:15:23.118 --> 00:15:39.918
<v Juan Martinez>Well, and that'll give me some time as we discuss, Michael, I'll collect the parameters that the other guys are doing for length of video, whether it's, you know, three of six games are shown or do they even bother showing everything. I'll have all that by next week.</v>

00:15:38.478 --> 00:15:46.478
<v Michael Gottlieb>Right. Is there a touch to start message? You know, on some of them, all of them, none of them. Okay, I mean, I...</v>

00:15:41.598 --> 00:15:42.638
<v Juan Martinez>Right, exactly.</v>

00:15:45.918 --> 00:16:05.198
<v Lena Zhukova>I will ask, maybe Igor will, I will talk to Igor like next week and I will ask what is his schedule and maybe he, we can assign this creating this attraction flow to Igor because he did it for South Dakota. I think Igor is capable to do it for George as well.</v>

00:15:50.638 --> 00:15:50.958
<v Michael Gottlieb>Yeah.</v>

00:16:04.798 --> 00:16:23.758
<v Michael Gottlieb>Okay. Well, I don't want to, you know, knock over the apple cart. Those guys should know how to do what they're doing. They should have the best sense of procedurally what should follow what. If it makes sense, great, but let's not, I don't want to do something that doesn't make sense. My only observation then is that</v>

00:16:23.838 --> 00:16:43.998
<v Michael Gottlieb>Here we are, you know, at the end of July, and we're wanting to submit this kind of, you know, mid-August. I would probably push it out a week or two to give us enough breathing room to get through all this stuff and make sure that we do it right. That would be my suggestion. I don't know how you feel about that, Juan.</v>

00:16:45.838 --> 00:16:56.238
<v Juan Martinez>I feel bad, but I certainly understand what you're saying. I mean, we don't, you know, we don't want to submit it if it's not ready. And I don't think a week or two is going to kill us.</v>

00:16:49.278 --> 00:16:49.678
<v Michael Gottlieb>Right.</v>

00:16:52.998 --> 00:16:53.278
<v Michael Gottlieb>Yeah.</v>

00:17:00.718 --> 00:17:01.198
<v Juan Martinez>Yes.</v>

00:17:03.998 --> 00:17:05.438
<v Juan Martinez>Correct. Yep.</v>

00:17:11.278 --> 00:17:12.158
<v Juan Martinez>Absolutely, yeah.</v>

00:17:12.518 --> 00:17:13.478
<v Michael Gottlieb>Um, okay.</v>

00:17:14.478 --> 00:17:28.478
<v Juan Martinez>And one of those things could be affecting performance. You know, the max bet required to win on Jackpot Rush, even though Jackpot Rush seems to be doing very well, imagine when they read, now it's available on any bet, it could really...</v>

00:17:14.798 --> 00:17:15.158
<v Michael Gottlieb>Yeah.</v>

00:17:27.398 --> 00:17:48.518
<v Michael Gottlieb>I was thinking about that last night when I was trying to sleep. I was thinking about that last night after studying the numbers, thinking, I wonder if that dissuades players because the messaging is incorrect. So, you know, I really, I really want to get the correct messaging in there. So yeah, I mean, I mean, if Anton's on vacation for a week, I would be.</v>

00:17:29.838 --> 00:17:30.158
<v Juan Martinez>Yep.</v>

00:17:37.238 --> 00:17:37.518
<v Juan Martinez>Yeah.</v>

00:17:44.918 --> 00:17:45.438
<v Juan Martinez>Definitely.</v>

00:17:48.598 --> 00:18:00.478
<v Michael Gottlieb>be of the opinion that pushing it out a week or two, getting it right, because it looks like we've got something here that's got some traction, and you know, that's my take on it.</v>

00:17:57.318 --> 00:17:57.518
<v Juan Martinez>Yeah.</v>

00:18:01.038 --> 00:18:01.238
<v Juan Martinez>Yeah.</v>

00:18:02.078 --> 00:18:02.318
<v Michael Gottlieb>O.</v>

00:18:05.118 --> 00:18:05.598
<v Juan Martinez>Understood.</v>

00:18:07.878 --> 00:18:09.838
<v Michael Gottlieb>Lena, do you have anything you want to cover?</v>

00:18:10.798 --> 00:18:30.558
<v Lena Zhukova>No, no, because I would like to have like latest build, especially now I know Anton is going on vacation, so I will now I will contact him and I will ask, because I want to see resolved issues in the Lion game, because they are definitely on Anton side.</v>

00:18:23.998 --> 00:18:24.158
<v Val Levitan>Yeah.</v>

00:18:30.798 --> 00:18:49.118
<v Lena Zhukova>that the click is not right on in the pick bonus and always you pick any symbol and you got lion, but inside the click spins you have like all kinds of different symbols stacking and clicking, clicking, clicking area is not working properly.</v>

00:18:40.718 --> 00:18:41.118
<v Michael Gottlieb>Right.</v>

00:18:45.598 --> 00:18:46.718
<v Michael Gottlieb>You know, and I'm going.</v>

00:18:48.718 --> 00:18:57.758
<v Michael Gottlieb>I'm going to, yeah, I apologize for interrupting you with no criticism to the guys. It blows my mind that we can have a game that we've been making for years.</v>

00:18:58.958 --> 00:19:12.238
<v Michael Gottlieb>How could a bug like that be introduced? You see what I'm saying? It's the same game code. It's the same game logic. What in the world did these guys do? Did they rewrite it? You know, it just doesn't make... Go ahead, Efim.</v>

00:19:05.518 --> 00:19:05.918
<v Juan Martinez>Yeah.</v>

00:19:10.078 --> 00:19:10.798
<v Efim Podvoiski>I get.</v>

00:19:11.438 --> 00:19:16.438
<v Lena Zhukova>The only difference is size of the reels and size of the symbols, that's the only difference.</v>

00:19:14.718 --> 00:19:19.198
<v Efim Podvoiski>And maybe this scene was not reshuffled in any way.</v>

00:19:20.158 --> 00:19:20.958
<v Efim Podvoiski>I was in the...</v>

00:19:20.238 --> 00:19:26.438
<v Lena Zhukova>Only graphical assets are changed, and of course, like a real size and the symbol size changed.</v>

00:19:24.278 --> 00:19:28.318
<v Efim Podvoiski>No, no, no, but not the hierarchy, well...</v>

00:19:25.918 --> 00:19:25.958
<v Val Levitan>I.</v>

00:19:27.398 --> 00:19:33.758
<v Michael Gottlieb>No, it's just an art swap. Fundamentally, it's just an art swap. It doesn't make any sense.</v>

00:19:31.678 --> 00:19:32.958
<v Efim Podvoiski>Yeah, yeah.</v>

00:19:34.638 --> 00:19:35.038
<v Efim Podvoiski>Right.</v>

00:19:35.278 --> 00:19:49.038
<v Michael Gottlieb>I don't know what's going on with their revision control. If it's something that was an old bug that got reintroduced or something, I just don't even know how you can introduce it. We're not asking to change the game logic and now the game logic doesn't work correctly. It's just a head scratch.</v>

00:19:51.998 --> 00:19:54.838
<v Michael Gottlieb>So, we'll get it figured out. I just, I...</v>

00:19:53.758 --> 00:19:54.718
<v Val Levitan>There is nothing.</v>

00:19:53.838 --> 00:20:12.238
<v Lena Zhukova>OK, so in this build, we should have this issue fixed, and also in bystand, we should have like proper arrows, golden arrows in Frispins, and I think you can, you will review all stages of Locket Wild.</v>

00:20:03.598 --> 00:20:03.998
<v Michael Gottlieb>Yes.</v>

00:20:12.558 --> 00:20:18.478
<v Michael Gottlieb>Okay. Is the, will the, what about the wild reel? Will the new wild reel affect being that you and I talked about?</v>

00:20:12.958 --> 00:20:15.598
<v Lena Zhukova>Uh, like, how to get it?</v>

00:20:18.638 --> 00:20:35.518
<v Lena Zhukova>Yes, I think this one should be there as well. I will confirm it with Anton. And inside free spins, you will have all stages. So how wild is frozen, getting frozen, how it wins, and how it's getting like, I mean, ice getting melted and it go away on the...</v>

00:20:23.518 --> 00:20:23.998
<v Michael Gottlieb>Okay.</v>

00:20:26.318 --> 00:20:26.478
<v Val Levitan>Mm.</v>

00:20:29.678 --> 00:20:30.318
<v Michael Gottlieb>Okay.</v>

00:20:34.318 --> 00:20:34.878
<v Michael Gottlieb>Right.</v>

00:20:36.638 --> 00:20:41.038
<v Michael Gottlieb>Okay, and has has Vladimir had a chance to uh drop us some new audio?</v>

00:20:42.718 --> 00:21:06.878
<v Lena Zhukova>I sent Vlad all your comments like Diego. I need to confirm with Vlad if Anton has inserted it already. So I think Vlad said it's easy for him to fix all this, like all this like review comments, but I probably need to ask them both, like Anton and Vlad, and confirm as they inserted, I mean, as it changes.</v>

00:20:49.278 --> 00:20:49.838
<v Michael Gottlieb>Okay.</v>

00:20:51.518 --> 00:20:51.918
<v Michael Gottlieb>Yeah.</v>

00:20:55.398 --> 00:20:55.758
<v Michael Gottlieb>Yeah.</v>

00:21:02.718 --> 00:21:03.118
<v Michael Gottlieb>Yeah.</v>

00:21:05.758 --> 00:21:24.078
<v Michael Gottlieb>Yeah, because the point, yeah, because the point is, is that that wild, the wild reel on, the reel 3 wild freezing, that you're selling that with the audio and then the bump, bump, bump of the bison running across the screen, there's an audio cell that there, the freezing effect, the tinkly winkly of the...</v>

00:21:24.598 --> 00:21:36.158
<v Michael Gottlieb>or whatever that's going to do with that. There's a cell there. And then the base game music is really, really good. I was not happy with the free spins music, so I sent them exactly. You remember Juan, the Blues Brothers, the movie?</v>

00:21:36.638 --> 00:21:37.198
<v Juan Martinez>Oh yeah.</v>

00:21:37.358 --> 00:21:38.398
<v Michael Gottlieb>The song, Rahide.</v>

00:21:38.798 --> 00:21:39.678
<v Juan Martinez>Yeah.</v>

00:21:39.638 --> 00:21:55.438
<v Michael Gottlieb>That's the vibe that I sent him. That's a touch slow. I told him go faster than Rawhide, but just, you know, bada bum bada bum bada bum, or Bonanza is the other one. That's what Twin Bison is in free spins. It's, you know, that type of vibe. So that'll work really well.</v>

00:21:41.038 --> 00:21:41.758
<v Juan Martinez>Oh, nice.</v>

00:21:44.158 --> 00:21:46.118
<v Juan Martinez>Yeah. Oh, yeah.</v>

00:21:48.958 --> 00:21:49.358
<v Juan Martinez>Yeah.</v>

00:21:51.958 --> 00:21:52.318
<v Juan Martinez>Sure.</v>

00:21:57.838 --> 00:22:05.278
<v Michael Gottlieb>Cool. Okay. Well, that's very encouraging then. Hopefully we can get a get a new build soon. I'm very much looking forward to it.</v>

00:22:07.598 --> 00:22:07.678
<v Michael Gottlieb>The.</v>

00:22:09.278 --> 00:22:10.238
<v Michael Gottlieb>Efim, do you have anything?</v>

00:22:10.718 --> 00:22:11.758
<v Efim Podvoiski>No, no.</v>

00:22:15.278 --> 00:22:23.198
<v Michael Gottlieb>We had a good week with, I think we're just about where we want to be with the twin bison math, which is really good.</v>

00:22:26.558 --> 00:22:45.358
<v Michael Gottlieb>Yeah, we're happy with that. Oh, the other thing is that, you know, we're going through and some of the games that do not have characters, if you will, Midnight Money is a perfect example. It doesn't make sense to do the simplified pay table with that game because there's nothing to...</v>

00:22:45.598 --> 00:23:05.478
<v Michael Gottlieb>focus on with that game. It's got a moon. Moons are cool, but Lena tried some comp art with it and we looked at it and I just, I think we, the conventional pay table for that game makes the most sense. I think that now that we've established our kind of design language and aesthetic of when you've got this character,</v>

00:23:05.558 --> 00:23:25.438
<v Michael Gottlieb>big, bold, ******** character with the eyes staring you down, or a beautiful woman or whatever. That type of stuff makes sense. But when you're talking about things like a moon, I don't think you're gaining anything from it. And I also think it doesn't, it helps make it so like all of our games don't look the same.</v>

00:23:26.358 --> 00:23:30.798
<v Michael Gottlieb>Which I think is a valuable, you know, is a valuable thing itself.</v>

00:23:31.998 --> 00:23:34.478
<v Michael Gottlieb>So cool. Val, do you have anything?</v>

00:23:36.158 --> 00:23:46.478
<v Val Levitan>I just want to tell you that we run a substantial experiment with the platform that I thought would be the economy platform.</v>

00:23:49.518 --> 00:23:51.758
<v Val Levitan>And the results are quite spectacular.</v>

00:23:53.318 --> 00:23:54.798
<v Juan Martinez>Is this the FP7?</v>

00:23:56.238 --> 00:23:59.678
<v Val Levitan>No, FP7 is the elaborate platform.</v>

00:23:59.918 --> 00:24:00.478
<v Juan Martinez>Oh, okay.</v>

00:24:01.438 --> 00:24:04.958
<v Val Levitan>The FP7 is just going to kill it, but the...</v>

00:24:06.238 --> 00:24:13.998
<v Val Levitan>Economy hardware that I thought would be economy. I mean, it is economy. It's quite impressive.</v>

00:24:14.718 --> 00:24:29.358
<v Michael Gottlieb>Do we have a sense of why? Is it like faster memory, larger bus? Because there's so many factors that come into play. I learned that lesson years ago where I always thought like, oh, just put a faster processor in there. And then I had some friends that were double E's that went through and explained to me bus size matters.</v>

00:24:27.758 --> 00:24:32.078
<v Val Levitan>No, no, the processor is not faster.</v>

00:24:32.638 --> 00:24:35.038
<v Michael Gottlieb>Okay, graphics card, graphics chip.</v>

00:24:37.278 --> 00:24:40.958
<v Val Levitan>It's a different architecture that we're looking at, and...</v>

00:24:40.558 --> 00:24:40.878
<v Michael Gottlieb>Right.</v>

00:24:43.198 --> 00:24:51.598
<v Val Levitan>All of us are quite impressed. I mean, it's running right now, it's running at 60 FPS with no loss of 60.</v>

00:24:52.798 --> 00:24:55.038
<v Val Levitan>We don't need 60. We don't need 60.</v>

00:24:52.878 --> 00:24:59.678
<v Michael Gottlieb>Fantastic. Right. Right. Is this a new vendor or the same vendor we used for previous boards?</v>

00:25:00.798 --> 00:25:07.598
<v Val Levitan>It's not an AMD based, it's RK based. So Chinese architecture.</v>

00:25:07.998 --> 00:25:08.638
<v Michael Gottlieb>Okay.</v>

00:25:09.678 --> 00:25:13.918
<v Val Levitan>And we use this architecture for our transactional products.</v>

00:25:15.118 --> 00:25:21.838
<v Val Levitan>And when we looked at the spec, actually Genadi said, I'm looking at the spec and it's...</v>

00:25:22.958 --> 00:25:26.318
<v Val Levitan>******* amazing. I don't know how to say it in English.</v>

00:25:26.798 --> 00:25:26.958
<v Michael Gottlieb>Yeah.</v>

00:25:27.678 --> 00:25:28.078
<v Val Levitan>Um...</v>

00:25:29.758 --> 00:25:31.918
<v Val Levitan>And so why don't we try it?</v>

00:25:34.438 --> 00:25:37.678
<v Val Levitan>So we tried it and everybody stunned by it.</v>

00:25:39.038 --> 00:25:39.198
<v Efim Podvoiski>Mm.</v>

00:25:39.518 --> 00:25:39.918
<v Juan Martinez>Good.</v>

00:25:41.118 --> 00:25:42.478
<v Val Levitan>So, um...</v>

00:25:46.438 --> 00:25:53.598
<v Val Levitan>What didn't work is the transition from base to bonus.</v>

00:25:56.158 --> 00:26:01.438
<v Val Levitan>It had a momentary pause, froze.</v>

00:26:01.678 --> 00:26:02.358
<v Michael Gottlieb>Coked.</v>

00:26:03.678 --> 00:26:10.318
<v Val Levitan>Joke, but we understand why it's just we bought minimal memory.</v>

00:26:12.318 --> 00:26:13.198
<v Val Levitan>Not an issue.</v>

00:26:15.118 --> 00:26:33.718
<v Val Levitan>We're now expanding memory to 16 gigabytes, and it should easily handle six games with transitions. And even if FPS falls to 30, even 25, we're still okay, but</v>

00:26:33.838 --> 00:26:36.158
<v Val Levitan>Runs at 60, so quite impressive.</v>

00:26:36.798 --> 00:26:37.518
<v Michael Gottlieb>Outstanding.</v>

00:26:39.118 --> 00:26:39.878
<v Val Levitan>And it's.</v>

00:26:39.158 --> 00:26:59.678
<v Michael Gottlieb>That is not the first story I've heard like that. My friend George Gonzalez runs Stern Pinball Product Development. He runs the whole place. And he was telling me that their previous generation platform was a fairly expensive PCB with an expensive processor, expensive this, expensive that.</v>

00:27:00.078 --> 00:27:22.918
<v Michael Gottlieb>And they have actually moved the entire platform to a Raspberry Pi. And they're running Pinball machines now with Raspberry Pis, including graphics monitors, running video. There's nothing interactive with the graphics monitor. It's just basically a movie player, if you will, that they've migrated to, you know, you used to open up the back box and this PCB was massive.</v>

00:27:05.758 --> 00:27:06.318
<v Juan Martinez>Wow.</v>

00:27:22.998 --> 00:27:36.038
<v Michael Gottlieb>huge thing. And now you open up the back box and it's like this little tiny. The biggest issue is fitting all the damn connectors. The entire perimeter is all connectors. That's the big issue now is fitting all the connectors on the board.</v>

00:27:34.518 --> 00:27:34.718
<v Juan Martinez>Yeah.</v>

00:27:37.398 --> 00:27:37.758
<v Juan Martinez>Thanks.</v>

00:27:38.278 --> 00:27:42.838
<v Michael Gottlieb>So that's cool. What do we have a time frame, Val, of when we think we'll get into it?</v>

00:27:42.438 --> 00:27:42.558
<v Val Levitan>Yes.</v>

00:27:47.398 --> 00:27:48.038
<v Val Levitan>I am.</v>

00:27:48.918 --> 00:27:50.518
<v Val Levitan>So confused about everything.</v>

00:27:53.718 --> 00:27:54.438
<v Val Levitan>I don't know.</v>

00:27:56.598 --> 00:27:58.278
<v Val Levitan>I'm just, I'm just frozen.</v>

00:28:02.918 --> 00:28:05.478
<v Val Levitan>I need, I need a little bit of time to figure it out.</v>

00:28:07.878 --> 00:28:10.678
<v Val Levitan>I'm honestly, honestly, I'm frozen.</v>

00:28:12.798 --> 00:28:18.518
<v Val Levitan>Like I can't, I can't make a decision, I can't move, I can't, there's so many.</v>

00:28:19.878 --> 00:28:25.878
<v Val Levitan>Irons in the fire and there are so many ants are screaming bloody hell everywhere.</v>

00:28:26.838 --> 00:28:28.118
<v Val Levitan>That I'm frozen.</v>

00:28:32.198 --> 00:28:32.758
<v Val Levitan>It's hard.</v>

00:28:36.198 --> 00:28:36.758
<v Juan Martinez>So.</v>

00:28:41.318 --> 00:28:44.358
<v Val Levitan>We must, we must switch to.</v>

00:28:41.518 --> 00:28:41.878
<v Michael Gottlieb>Noted.</v>

00:28:47.478 --> 00:28:49.158
<v Val Levitan>We must switch to...</v>

00:28:52.838 --> 00:28:55.798
<v Val Levitan>Omni, well, the Novo.</v>

00:28:57.718 --> 00:28:59.798
<v Val Levitan>And we also must switch to...</v>

00:29:00.998 --> 00:29:04.438
<v Val Levitan>Galaxy, that's the new name for backend.</v>

00:29:06.198 --> 00:29:10.198
<v Val Levitan>Galaxy, we must switch. It's independent, somewhat independent.</v>

00:29:12.118 --> 00:29:13.398
<v Val Levitan>But we also...</v>

00:29:14.598 --> 00:29:18.438
<v Val Levitan>Just doing so many things in internally in.</v>

00:29:19.598 --> 00:29:21.958
<v Val Levitan>how we keep our files and how we now.</v>

00:29:23.398 --> 00:29:26.998
<v Val Levitan>pushing our product to production.</v>

00:29:30.238 --> 00:29:31.638
<v Val Levitan>It's just everything at once.</v>

00:29:39.438 --> 00:29:40.118
<v Val Levitan>So, yeah.</v>

00:29:40.758 --> 00:29:46.838
<v Michael Gottlieb>Well, hopefully, when the sun goes down, you can clear your mind and enjoy Shabbat and unplug.</v>

00:29:46.438 --> 00:29:46.918
<v Val Levitan>Yeah.</v>

00:29:48.278 --> 00:29:59.318
<v Val Levitan>Okay, guys, but I enjoyed this meeting. I feel all of you are uplifted and that helps me go through my week. So that's really great.</v>

00:30:00.518 --> 00:30:02.758
<v Val Levitan>Georgia shows.</v>

00:30:05.318 --> 00:30:08.038
<v Val Levitan>Uplifting results and</v>

00:30:10.438 --> 00:30:11.078
<v Val Levitan>Oh.</v>

00:30:13.878 --> 00:30:17.238
<v Val Levitan>I understand Nebraska is switching games, right?</v>

00:30:19.638 --> 00:30:24.838
<v Juan Martinez>Yeah, they're changing the settings. We've eliminated the 25 cent bits.</v>

00:30:22.518 --> 00:30:23.158
<v Val Levitan>Church.</v>

00:30:24.998 --> 00:30:29.158
<v Val Levitan>changing the settings, but our next focus should be on Nebraska.</v>

00:30:30.118 --> 00:30:32.438
<v Lena Zhukova>Not going to be our next production.</v>

00:30:30.438 --> 00:30:32.038
<v Val Levitan>Wait, wait, wait.</v>

00:30:31.798 --> 00:30:34.758
<v Juan Martinez>Yeah, after Giorgi B3.</v>

00:30:33.478 --> 00:30:35.078
<v Val Levitan>Wait, we need, we need to.</v>

00:30:36.598 --> 00:30:48.838
<v Val Levitan>Well, after, yeah, I mean, starting September, we should focus on Nebraska, make sure that it makes money. That's our battle ground. We're shifting the battle ground to Nebraska.</v>

00:30:42.838 --> 00:30:43.158
<v Juan Martinez>Yeah.</v>

00:30:49.958 --> 00:30:57.398
<v Michael Gottlieb>On the PD side, we still have to finish South Dakota as well. We put South Dakota on pause to focus on Georgia, but that's just our problem.</v>

00:30:54.838 --> 00:30:55.398
<v Val Levitan>Like.</v>

00:30:56.598 --> 00:30:57.158
<v Val Levitan>Well...</v>

00:30:59.878 --> 00:31:06.678
<v Val Levitan>No, but I mean, I mean, we're performing well in South Dakota, from what I gather, unless something dramatically changed.</v>

00:31:07.118 --> 00:31:10.598
<v Michael Gottlieb>No, but it's just that we've done these keynotes and we...</v>

00:31:09.678 --> 00:31:22.438
<v Val Levitan>Oh, no, no, no, no, I understand, but I'm expecting an improvement in performance with Kinos out. I mean, we're not on fire in South Dakota. I mean, we're...</v>

00:31:12.038 --> 00:31:12.198
<v Michael Gottlieb>Yeah.</v>

00:31:16.598 --> 00:31:16.918
<v Michael Gottlieb>Right.</v>

00:31:16.758 --> 00:31:17.038
<v Juan Martinez>Yeah.</v>

00:31:23.798 --> 00:31:25.318
<v Val Levitan>I mean, we're cruising okay.</v>

00:31:25.798 --> 00:31:26.198
<v Michael Gottlieb>Right.</v>

00:31:27.798 --> 00:31:42.118
<v Val Levitan>In terms of performance, so adding adding Kinos, I assume, should probably improve our performance, I assume, but Nebraska, but Nebraska is not performing.</v>

00:31:29.718 --> 00:31:30.278
<v Michael Gottlieb>Right, right.</v>

00:31:37.398 --> 00:31:38.678
<v Juan Martinez>Yep, yep.</v>

00:31:43.238 --> 00:31:44.998
<v Val Levitan>And, and it's a...</v>

00:31:46.598 --> 00:31:56.198
<v Val Levitan>It's A fertile market. I mean, we want to sell there. It will immediately influence our bottom line. So we need to sell in Nebraska.</v>

00:31:49.558 --> 00:31:49.958
<v Michael Gottlieb>Right.</v>

00:31:59.358 --> 00:32:02.558
<v Val Levitan>So that's why I'm saying the bottle ground will shift in Nebraska.</v>

00:31:59.678 --> 00:31:59.958
<v Juan Martinez>Great.</v>

00:32:03.318 --> 00:32:04.038
<v Michael Gottlieb>Understood.</v>

00:32:06.438 --> 00:32:08.118
<v Val Levitan>Okay, um...</v>

00:32:09.158 --> 00:32:12.358
<v Val Levitan>Good Friday, everyone. Good weekend. Shabbat.</v>

00:32:11.318 --> 00:32:18.118
<v Lena Zhukova>I also want to remind that Monday is a holiday in Canada, so...</v>

00:32:11.438 --> 00:32:11.638
<v Juan Martinez>Yeah.</v>

00:32:18.838 --> 00:32:21.078
<v Val Levitan>It's a virtual company, there are no holidays.</v>

00:32:22.758 --> 00:32:28.598
<v Val Levitan>We all virtually work and as a matter of fact, we elect that next week we'll work out of US.</v>

00:32:22.838 --> 00:32:23.238
<v Juan Martinez>Yeah.</v>

00:32:29.878 --> 00:32:31.558
<v Val Levitan>No holidays in the US, right?</v>

00:32:30.318 --> 00:32:30.678
<v Juan Martinez>Yeah.</v>

00:32:32.438 --> 00:32:34.278
<v Juan Martinez>There's no holiday in the U.S. yet.</v>

00:32:32.518 --> 00:32:36.998
<v Val Levitan>And whenever there's holiday in US, because we're a virtual company, we'll work out of Canada.</v>

00:32:37.238 --> 00:32:37.398
<v Lena Zhukova>Yeah.</v>

00:32:38.118 --> 00:32:41.238
<v Val Levitan>In some cases, we could virtually work from Belarus.</v>

00:32:42.118 --> 00:32:45.238
<v Efim Podvoiski>In some cases we are Christians, in some cases we are Jews, right?</v>

00:32:42.438 --> 00:32:42.758
<v Val Levitan>Right.</v>

00:32:47.718 --> 00:32:48.838
<v Val Levitan>Listen, we're humans.</v>

00:32:49.078 --> 00:32:49.718
<v Lena Zhukova>This is.</v>

00:32:49.878 --> 00:32:50.518
<v Juan Martinez>I love it.</v>

00:32:51.078 --> 00:33:00.358
<v Efim Podvoiski>Yeah, yeah, but I, but I asked for the day off to for Monday, yeah, I know we are not getting it's like free, yeah, but...</v>

00:32:51.798 --> 00:32:52.598
<v Michael Gottlieb>You, yeah.</v>

00:32:54.598 --> 00:32:56.838
<v Lena Zhukova>Yeah, yeah, so I'm thinking they open.</v>

00:32:58.518 --> 00:33:03.718
<v Lena Zhukova>Yeah, it's yeah, yeah, yeah, I will mark it on EGP because it's not paid for. It's not paid for.</v>

00:33:02.038 --> 00:33:04.478
<v Efim Podvoiski>I am up to here, yeah, yeah.</v>

00:33:06.038 --> 00:33:08.038
<v Val Levitan>Okay guys, take care.</v>

00:33:06.918 --> 00:33:07.958
<v Michael Gottlieb>All right.</v>

00:33:07.478 --> 00:33:23.878
<v Efim Podvoiski>I think I forget to mention, we got Linux built today for Georgia because it didn't work with Alliance and Twin Bison for last week, and finally we get a start, which also not a bad news.</v>

00:33:07.718 --> 00:33:08.278
<v Michael Gottlieb>Okay.</v>

00:33:25.878 --> 00:33:26.678
<v Juan Martinez>Good news.</v>

00:33:29.158 --> 00:33:29.718
<v Val Levitan>Okay.</v>

00:33:30.118 --> 00:33:30.518
<v Michael Gottlieb>Great.</v>

00:33:30.998 --> 00:33:32.358
<v Efim Podvoiski>Thank you. Bye.</v>

00:33:31.158 --> 00:33:33.158
<v Juan Martinez>Thanks, everybody. Bye bye.</v>

00:33:32.198 --> 00:33:32.518
<v Lena Zhukova>Anton.</v>

00:33:32.758 --> 00:33:33.078
<v Val Levitan>But.</v>

