# Raw Transcript — Game_Development
**Date:** September 25, 2026, 2:32 PM – 3:14 PM Eastern
**Summary note:** [[Meeting_Notes_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026]]
---
WEBVTT

00:00:15.041 --> 00:00:34.881
<v Michael Gottlieb>The one thing I did want to mention is for whatever reason, Georgia Vertical 2 was deployed at 92 plus 4.5 for the progressive. So those machines were deployed at 96.5, which doesn't do your hold a whole lot of favors.</v>

00:00:36.081 --> 00:00:45.681
<v Michael Gottlieb>So I hope we're not overshooting because I can tell you that the difference from a player's perspective, you can feel the difference between 96.5 and 92.</v>

00:00:46.001 --> 00:00:46.761
<v Efim Podvoiski>Absolutely.</v>

00:00:48.241 --> 00:00:53.121
<v Michael Gottlieb>We'll see what happens. That's a pretty substantial delta.</v>

00:00:54.961 --> 00:01:11.041
<v Efim Podvoiski>You will see it immediately in the ways that progressive increments if you pay attention. Otherwise, maybe not that much because the progressive events do not happen every session, so maybe...</v>

00:01:12.401 --> 00:01:12.881
<v Michael Gottlieb>Maybe.</v>

00:01:12.561 --> 00:01:16.161
<v Efim Podvoiski>Maybe it's not that maybe, maybe, maybe, maybe.</v>

00:01:14.841 --> 00:01:15.441
<v Michael Gottlieb>Maybe.</v>

00:01:16.561 --> 00:01:22.401
<v Michael Gottlieb>I'm not reaching any conclusions. I'm simply citing data. That's it.</v>

00:01:24.241 --> 00:01:42.561
<v Michael Gottlieb>Second point, progressives, we are going to go with 2400 top award for Match 3, 2400 top award for Fiery Ice, and 1500 top award for Jackpot Rush. I did a lot of field research. Progressives are all over the map.</v>

00:01:42.801 --> 00:02:05.841
<v Michael Gottlieb>There is not one-size-fits-all. Some of the guys are out there doing $5,000 top awards, IGT, which is a strong competitor, they're out there at the granular level of doing discrete progressives per game. And because they're discrete progressives per game, those progressives are like 300 bucks, 400 bucks, nothing.</v>

00:02:06.401 --> 00:02:24.801
<v Michael Gottlieb>nothing crazy. So we talked with Felipe extensively about this, challenged him from every angle to encourage him to think three-dimensionally, which we're making good progress on in my opinion. And those are the numbers that we come up with. We did have a discussion, Val, about</v>

00:02:24.921 --> 00:02:44.681
<v Michael Gottlieb>bumping up that match three. But the problem is, is that Fiery Ice and Jackpot Rush, those are fixed. Those top awards, they can't go any higher. So given those parameters in the ecosystem of these three progressives, we didn't want one to be drastically different.</v>

00:02:45.041 --> 00:03:05.361
<v Michael Gottlieb>than the others because we were concerned it could affect the performance of the others. So this way, it's kind of a comparatively fair horse race. IGT has a Jackpot Rush style product in the market. Their top award is a little bit higher than what we're doing with Jackpot Rush, but we're kind of, I think, where we need to be.</v>

00:03:06.081 --> 00:03:25.121
<v Michael Gottlieb>And then I think we were all in agreement that what we were doing made sense. And Felipe also mentioned, and again, I challenged him, is this one story or have he had this happen more than once, Val? And he had indicated that he's had locations request resetting the progressive when it gets to 8,000 bucks.</v>

00:03:25.721 --> 00:03:48.161
<v Michael Gottlieb>which obviously is not something they're supposed to do. When they hit 8,000, it goes into an overflow bucket. And then the problem is it'll pop 8,000 and then the overflow bucket's already 8,000, it'll pop 8,000 again. So his feeling was that, you know, there's enough breathing room here for the progressives to go up. And I didn't, I don't disagree with him, especially since the match three</v>

00:03:48.561 --> 00:04:02.481
<v Michael Gottlieb>is fed by all six games. All six games will feed into that match three. So I think those values are going to go up at a pretty decent clip. Anyway, that was the logic behind what we were doing.</v>

00:04:15.201 --> 00:04:18.161
<v Val Levitan>I understand the logic, but I don't know where the truth is.</v>

00:04:22.721 --> 00:04:23.681
<v Efim Podvoiski>You don't know, is it?</v>

00:04:22.801 --> 00:04:42.401
<v Michael Gottlieb>The first rule of medicine is do no harm. And I just don't think we're in a position to go off and do anything drastic based upon instinct and gut or, hey, these guys are doing this. I found successful examples of multiple different approaches, implementations,</v>

00:04:42.961 --> 00:04:51.921
<v Michael Gottlieb>there was not one-size-fits-all. And I'm not talking about **** stuff from GTech or these little guys. I'm talking about the big boys.</v>

00:04:53.041 --> 00:05:16.321
<v Michael Gottlieb>There's a couple of different approaches out there. And one of the most important salient things I learned Saturday night about the nature of having more than one progressive in a cabinet and why it's important to have it, no matter how you execute it, is he was saying that if you just have one progressive in a cabinet, if all the games feed one progressive, the big one,</v>

00:05:16.721 --> 00:05:36.881
<v Michael Gottlieb>and that progressive hits, then that cabinet goes dead. It goes soft. The regular players look at it and go, oh, hey, man, that top award is not, I'm not touching that. That thing is way off base of where it needs to be. Right? So we are, we've got a three horse race here with the match three, the fiery ice, the jackpot rush.</v>

00:05:37.201 --> 00:05:58.481
<v Michael Gottlieb>those values will go up. And most importantly, the salient point that I'm making is when a fiery ice pops at 5, 6, 7,000, the other ones are still cooking and they're still running. And that was his explanation as to why IGT does these discrete progressives, where they literally have every game has its own progressive.</v>

00:05:59.041 --> 00:06:18.401
<v Michael Gottlieb>But again, those values are only like 3 or $400, and that's working in the market. So I agree with you. More data would be great. Something definitive would be great. But based upon poking at Felipe really, really hard to just not to move beyond opinion and move into data,</v>

00:06:18.961 --> 00:06:25.921
<v Michael Gottlieb>Um, I think we landed it. This is a this is a reasonable approach and Efim opinion as well, right?</v>

00:06:26.481 --> 00:06:40.561
<v Efim Podvoiski>Yes, yes, this is, yeah, some something in the middle, because they don't have data to to support going into any specific direction, direction very far.</v>

00:06:41.921 --> 00:06:48.241
<v Val Levitan>Well, data is coming. I mean, for the first time, we're putting out, we'll be putting out machines with models.</v>

00:06:49.601 --> 00:06:52.801
<v Val Levitan>And that's a big, big, humongous breakthrough.</v>

00:06:52.401 --> 00:06:53.601
<v Michael Gottlieb>Oh, massive.</v>

00:06:54.961 --> 00:06:58.801
<v Michael Gottlieb>Massive, massive, you know, massive upside.</v>

00:06:58.521 --> 00:07:03.361
<v Val Levitan>Month, it cannot be, it cannot be overstated. It's months.</v>

00:07:02.521 --> 00:07:03.121
<v Michael Gottlieb>No.</v>

00:07:04.081 --> 00:07:23.801
<v Michael Gottlieb>It's like taking the blinders off and having some x-ray vision and visibility into what the, you know, what the heck is going on. So, you know, I think that the trick, I don't want to say the trick with Felipe, but on some levels of the trick with Felipe is getting them to process and understand that sometimes what we want.</v>

00:07:24.001 --> 00:07:45.641
<v Michael Gottlieb>what the customer wants and what the player wants can be 3 different things. And you have to balance those three different things as opposed to just being reactionary and say, oh, well, it's this or oh, well, it's that. It's like, no, you have to think three-dimensionally because you can reward the player and F the customer, or you can give the customer what they want and F the player.</v>

00:07:45.881 --> 00:08:02.761
<v Michael Gottlieb>So you have to find balance. And again, first rule of medicine, do no harm. I don't believe we're in a place where we're in trouble. Oh, and most importantly, Val, most importantly, Felipe has not had issues or complaints or any negative feedback about where our progressive levels are right now.</v>

00:08:04.241 --> 00:08:12.361
<v Michael Gottlieb>Again, he said that these guys are coming back saying, hey, it's at 88,000 and I want to reset it because they get nervous for obvious reasons when those numbers get so high.</v>

00:08:12.281 --> 00:08:30.121
<v Val Levitan>I agree with everything. There's nothing that you said that bothers me at all. We agree. We agree that we don't have enough data. We agree that do no harm. We agree that we need multiple progressives. We agree that we don't have solid data on</v>

00:08:31.081 --> 00:08:41.961
<v Val Levitan>Oh, these guys with this large progressives win. No, they don't. They don't. It's not black and white. It's all over the place. It's hearsay, it's gossip, it's...</v>

00:08:35.801 --> 00:08:37.081
<v Michael Gottlieb>Right, right.</v>

00:08:43.321 --> 00:08:45.001
<v Val Levitan>It's not conclusive.</v>

00:08:45.001 --> 00:08:45.481
<v Michael Gottlieb>Yes.</v>

00:08:45.961 --> 00:09:00.361
<v Val Levitan>I agree that we cannot be at 96.5% because we will never get to our net win. It just never. And eventually we're going to get kicked out.</v>

00:08:56.041 --> 00:08:57.081
<v Michael Gottlieb>Should have never been there.</v>

00:08:58.601 --> 00:08:59.641
<v Michael Gottlieb>No, that was a mistake.</v>

00:09:00.641 --> 00:09:01.121
<v Michael Gottlieb>Mmh.</v>

00:09:01.721 --> 00:09:03.961
<v Val Levitan>So, 92 percent.</v>

00:09:05.161 --> 00:09:23.561
<v Val Levitan>Should it be 93? Should it be 91? I don't know. But 92 is good enough right now. Let's put the machines out there. Let's just make sure that the RIS that's being installed, let's spot check it.</v>

00:09:13.081 --> 00:09:14.121
<v Michael Gottlieb>Yes, I don't, yes.</v>

00:09:25.001 --> 00:09:31.401
<v Val Levitan>I cannot do it because I don't know what the hell I'm looking at, but maybe Efim, if you could take it upon yourself to spot check.</v>

00:09:32.361 --> 00:09:45.401
<v Val Levitan>Just ask them, hey, send me the RAS that you actually installed yesterday on the machine, spot check it, because I honestly don't know how the F they got to 96.5%.</v>

00:09:46.041 --> 00:09:57.081
<v Efim Podvoiski>Yeah, somebody sent some some some document originated somewhere from the and some and they folded.</v>

00:09:48.041 --> 00:09:50.841
<v Val Levitan>Say again, somebody, you know, wait to start.</v>

00:09:54.761 --> 00:09:55.161
<v Michael Gottlieb>Right.</v>

00:09:57.321 --> 00:10:07.721
<v Val Levitan>So just take it upon yourself, just spot check it. So we know that we are doing maximum we can for a small company with ****** QA right now.</v>

00:10:11.641 --> 00:10:12.041
<v Val Levitan>Yeah.</v>

00:10:11.961 --> 00:10:33.361
<v Michael Gottlieb>And to that point, I was very supportive of Felipe taking responsibility as if I was like, dude, I understand that you're saying there's a body laying there and somebody needs to do something, but you're basically the first line of defense, preventative defense. Can be, I'm not expecting you to be, you know, all of it,</v>

00:10:33.481 --> 00:10:39.881
<v Michael Gottlieb>But you need to be communicative, because *** **** it, if one more time I hear after the fact, we blew it.</v>

00:10:40.921 --> 00:10:59.561
<v Michael Gottlieb>I'm going to pull my hair out, what little hair I have left, right? I mean, we got to do this **** on the front end. And he promised me that he would be communicative, and he has been, and I think it's great. And that loop is going to be strong, and it's going to continue on. And to your point, Val, I did mention the same thing to Efim that we need him to</v>

00:10:59.721 --> 00:11:08.681
<v Michael Gottlieb>trust but verify the data and make sure there's integrity to it, make sure that it's correct, make sure that it's accurate, and that we're doing things the way we should be doing.</v>

00:11:09.881 --> 00:11:11.241
<v Michael Gottlieb>So, we're all in agreement there.</v>

00:11:23.721 --> 00:11:35.241
<v Michael Gottlieb>Okay, the one other thing I just wanted to mention, and this is not a big deal. Well, let me back up a step. Where are we with submission of Georgia V3? Have we submitted it?</v>

00:11:35.961 --> 00:11:48.441
<v Val Levitan>Yes, we are, it passed the interlock test and we should get a letter on hand on Monday and we are delivering Monday, Tuesday, Wednesday.</v>

00:11:40.441 --> 00:11:40.921
<v Michael Gottlieb>Okay.</v>

00:11:49.321 --> 00:11:51.881
<v Michael Gottlieb>Okay, so it's go time then. That's where we're at.</v>

00:11:52.961 --> 00:11:53.801
<v Michael Gottlieb>Okay, great.</v>

00:11:53.161 --> 00:11:55.481
<v Val Levitan>But, but, but listen.</v>

00:11:56.841 --> 00:12:16.441
<v Val Levitan>I did not check whether all the changes that you worked on made into that release. I simply, I don't know enough to even check that. So I encourage you, just dial Felipe and say, hey, dude, I just want to spot check my ****.</v>

00:12:16.921 --> 00:12:17.321
<v Michael Gottlieb>Yes.</v>

00:12:17.641 --> 00:12:33.481
<v Val Levitan>You know, take your video camera, take me to the machine, show me the video, show me the VDEC, show me the, show me that, show me the settings, show me the RTP. They have machines running right now.</v>

00:12:22.201 --> 00:12:22.601
<v Michael Gottlieb>Right.</v>

00:12:30.681 --> 00:12:30.721
<v Michael Gottlieb>100%.</v>

00:12:34.841 --> 00:12:47.481
<v Val Levitan>I would do it myself. I just don't know what I'm looking at, to be honest with you. So if you or you feel if you or you feel could take it upon yourself, that would be a great actual physical help for me.</v>

00:12:39.521 --> 00:12:40.601
<v Michael Gottlieb>No, I understand, and I...</v>

00:12:47.721 --> 00:13:01.601
<v Michael Gottlieb>We will do it. Efim and I will do it. We had a great talk with Felipe this week and we were, you know, my hands are on his throat right now in a good way, in a good way. Just close. We got to be close. We got to be close.</v>

00:13:00.441 --> 00:13:05.721
<v Val Levitan>We have, we, we, we're we're zeroing in on.</v>

00:13:06.801 --> 00:13:11.641
<v Val Levitan>A lot of little things that I think will take us to where we need to be.</v>

00:13:14.161 --> 00:13:34.961
<v Michael Gottlieb>No question. I agree with you completely. So, okay, well, that is good news. That is the direction everything is headed then. Class A development is the beginnings of it is moving forward. We are going to use Lions Riches as the test</v>

00:13:35.041 --> 00:13:40.041
<v Michael Gottlieb>bed for the Class A product. Lena, do you want to show some of the images of where we're at?</v>

00:13:41.721 --> 00:13:44.521
<v Michael Gottlieb>Just so everybody can see what the game is going to look like.</v>

00:13:52.441 --> 00:14:11.121
<v Michael Gottlieb>Okay, so go ahead, please. Okay, I was just going to say, so this image reflects, this is what the Class A product is going to look like. Important to note, we have got the dual box, kind of that reduced dual box that you had liked</v>

00:13:52.601 --> 00:13:56.281
<v Lena Zhukova>So, no, you're good.</v>

00:14:11.201 --> 00:14:32.201
<v Michael Gottlieb>to Val. I like it too. I think it's nice. I think it's clean. I think it's elegant. Again, on the bottom, you've got credits on the left, awards in the center. And then we're going to do the bet levels plus and minus. And I was showing a theme this week, videos of how they're doing it in increments of 25 cents.</v>

00:14:32.601 --> 00:14:50.841
<v Michael Gottlieb>25 cents all the way up to 5 bucks. And then we will have to come up with a layout for the V deck that's got that plus and minus buttons on it, something clean, something simple. So yeah, that's this is this is where we're at. And this is</v>

00:14:51.281 --> 00:15:06.041
<v Michael Gottlieb>Graphically, not overwhelming, but mathematically it remains to be seen, and the reason for this is that we are not just taking Lions Riches Georgia, because Lions Riches Georgia is a nudge-based game.</v>

00:15:07.001 --> 00:15:13.401
<v Michael Gottlieb>And so, Efim has got to dig in and determine, because we no longer have the constraints and requirements of nudge.</v>

00:15:14.761 --> 00:15:33.161
<v Michael Gottlieb>how are we going to do the math such that it makes sense? Because he doesn't have to worry about real three in the same way anymore. So basically, are we taking a class 3 lions riches and just throwing the dual box on top of it? That appears to be what our competitors are doing. But there is some amount of work there. I don't think it's overwhelming, but</v>

00:15:32.201 --> 00:15:33.161
<v Efim Podvoiski>Yeah, but the big...</v>

00:15:35.081 --> 00:15:55.161
<v Efim Podvoiski>The big challenge is this $50 cup. Yeah, yeah. What to do with free spins? How do we deal with all party time and so on? And another challenge is that it's just amount of work and the amount of files that will be generated because</v>

00:15:38.401 --> 00:15:40.281
<v Michael Gottlieb>Top win, yeah, max win per, yeah.</v>

00:15:43.641 --> 00:15:43.881
<v Michael Gottlieb>Right.</v>

00:15:46.761 --> 00:15:47.081
<v Michael Gottlieb>Yeah.</v>

00:15:55.321 --> 00:16:03.401
<v Efim Podvoiski>If we have for every bird, I will have to have something specific in mass, at least something, and so...</v>

00:16:02.521 --> 00:16:03.321
<v Michael Gottlieb>Yeah, go ahead, Val.</v>

00:16:04.521 --> 00:16:05.401
<v Michael Gottlieb>That was saying something.</v>

00:16:05.881 --> 00:16:08.921
<v Val Levitan>I just, I just want to say.</v>

00:16:10.761 --> 00:16:11.241
<v Val Levitan>That.</v>

00:16:12.321 --> 00:16:16.121
<v Val Levitan>Plus A will go inside of a...</v>

00:16:17.161 --> 00:16:21.881
<v Val Levitan>Let's call it Flex - capital S.</v>

00:16:23.001 --> 00:16:24.201
<v Val Levitan>Stands for...</v>

00:16:25.721 --> 00:16:29.761
<v Val Levitan>Sporty version, AKA Street Machine.</v>

00:16:35.001 --> 00:16:35.961
<v Val Levitan>So...</v>

00:16:36.121 --> 00:16:37.041
<v Michael Gottlieb>No VDEC.</v>

00:16:38.201 --> 00:16:38.761
<v Val Levitan>Well...</v>

00:16:40.921 --> 00:16:42.281
<v Val Levitan>You know I love Vivek.</v>

00:16:43.961 --> 00:16:46.121
<v Michael Gottlieb>I know, but it's unnecessary.</v>

00:16:45.241 --> 00:16:45.961
<v Val Levitan>So...</v>

00:16:47.001 --> 00:16:51.401
<v Val Levitan>Right, so the basic machine will go without be there.</v>

00:16:53.881 --> 00:16:59.801
<v Val Levitan>But I am building a provision just in case we source.</v>

00:17:01.161 --> 00:17:09.801
<v Val Levitan>The right screen and the right touch screen to put the VDAC inside, but even if the VDAC comes.</v>

00:17:11.641 --> 00:17:15.321
<v Val Levitan>It will be a skinny and narrow screen.</v>

00:17:19.561 --> 00:17:22.601
<v Val Levitan>It will only be an upright version.</v>

00:17:23.721 --> 00:17:27.241
<v Val Levitan>So, there is no depth to the machine.</v>

00:17:30.841 --> 00:17:33.561
<v Val Levitan>That means it's a shallow deck.</v>

00:17:35.961 --> 00:17:40.281
<v Val Levitan>It will be slanted on slope approximately 10 degrees.</v>

00:17:42.601 --> 00:17:44.921
<v Val Levitan>It will have a cup holder.</v>

00:17:46.241 --> 00:17:47.321
<v Val Levitan>On one side.</v>

00:17:48.841 --> 00:17:50.841
<v Val Levitan>and slam button on the other side.</v>

00:17:52.921 --> 00:17:54.201
<v Val Levitan>Large slim button.</v>

00:17:55.281 --> 00:17:56.041
<v Val Levitan>On the other side.</v>

00:17:58.241 --> 00:18:02.241
<v Val Levitan>And you need to tell me how many button panels do you need?</v>

00:18:05.281 --> 00:18:06.681
<v Val Levitan>Probably 8 buttons.</v>

00:18:10.601 --> 00:18:21.241
<v Val Levitan>And so your controls need to be on the screen. It will be 43 inch screen because if we get into 47 or 50, it's substantially more money.</v>

00:18:26.121 --> 00:18:28.281
<v Val Levitan>So 43 inch vertical.</v>

00:18:29.481 --> 00:18:36.681
<v Val Levitan>The controls need to be on the control panel, which you have a beautiful control panel. I really love it.</v>

00:18:42.841 --> 00:18:56.201
<v Michael Gottlieb>Okay, we'll take those parameters into account. I think we'll probably orient similar to what Primero is doing. The vast majority of the interface with Primero is on the screen.</v>

00:18:56.841 --> 00:18:57.241
<v Val Levitan>Yeah.</v>

00:18:57.281 --> 00:19:05.241
<v Michael Gottlieb>I mean, other than spinning the reels, ain't a whole lot going on on that deck, on that, on the button panel. Not a lot of buttons, not a little.</v>

00:19:04.521 --> 00:19:11.161
<v Val Levitan>I also, I also would like to put the same Flex-S hardware in Texas.</v>

00:19:17.081 --> 00:19:19.401
<v Val Levitan>Excuse me, please. I need 3 minutes. Hold on.</v>

00:19:25.961 --> 00:19:27.241
<v Michael Gottlieb>I'll take a minute as well.</v>

00:21:31.321 --> 00:21:39.961
<v Michael Gottlieb>Efim is the Nebraska software basically class 3 with dual box added or is there anything else about it that's unique?</v>

00:21:39.561 --> 00:21:41.961
<v Efim Podvoiski>It's basically class 3, yes, I think.</v>

00:21:41.161 --> 00:21:44.361
<v Michael Gottlieb>OK, good. OKOK, good.</v>

00:21:43.561 --> 00:21:44.441
<v Efim Podvoiski>Nice and fancy.</v>

00:21:46.841 --> 00:21:50.521
<v Michael Gottlieb>Okay, go ahead, Lena, show the next image.</v>

00:21:58.921 --> 00:22:07.881
<v Michael Gottlieb>So when we storyboard this lane, we'll want the real spinning to communicate to the guys what, you know, that party time is a pre-spin event.</v>

00:22:08.201 --> 00:22:08.721
<v Lena Zhukova>Mmh.</v>

00:22:09.721 --> 00:22:27.801
<v Michael Gottlieb>So basically, Val, we've got this feature called party time. And when you go into party time, you're going to get repeated $50 wins. It's similar to their hot streak. Basically, I have concluded that this mechanism is a substitute for progressives.</v>

00:22:28.361 --> 00:22:32.521
<v Michael Gottlieb>So, instead of winning 250 bucks, you win 50 bucks five times.</v>

00:22:33.881 --> 00:22:42.121
<v Lena Zhukova>And yeah, each time we will be also, or do we need like party time on top when you have this message or?</v>

00:22:41.801 --> 00:23:00.841
<v Michael Gottlieb>Yes, yeah, when party time is active, the party time message needs to stay on top. It's basically a state, right? And you're going to go into party time, and while you're in party time, there you go. And while you're in party time, you'll have the dual box, you'll touch the correct thing.</v>

00:22:43.481 --> 00:22:43.881
<v Lena Zhukova>Moody.</v>

00:23:01.001 --> 00:23:02.201
<v Michael Gottlieb>You'll get the pop-up.</v>

00:23:06.561 --> 00:23:08.361
<v Michael Gottlieb>So that's the direction things are headed.</v>

00:23:09.641 --> 00:23:13.721
<v Val Levitan>So, from a perspective of mathematics.</v>

00:23:15.441 --> 00:23:17.681
<v Val Levitan>And I, I don't know if he's with us or not.</v>

00:23:17.961 --> 00:23:23.721
<v Efim Podvoiski>I am busy, I am just, I am taking off my cold machine sleeve, so I...</v>

00:23:24.681 --> 00:23:27.721
<v Val Levitan>So, from the perspective of the mathematics...</v>

00:23:28.761 --> 00:23:34.161
<v Val Levitan>Are we able to create interesting payouts with the party time concept?</v>

00:23:35.081 --> 00:23:38.281
<v Val Levitan>I would say yes, I mean, I'm answering my own question, but...</v>

00:23:38.681 --> 00:23:39.881
<v Efim Podvoiski>You have to be special.</v>

00:23:39.401 --> 00:23:40.121
<v Val Levitan>Seems like...</v>

00:23:47.881 --> 00:24:06.681
<v Michael Gottlieb>The answer is yes. I think you can have compelling pays. It's just a function of if free spins is limited to $50, how we handle that. Because generally, basically, you know, the fundamental question one asks is,</v>

00:24:06.801 --> 00:24:26.841
<v Michael Gottlieb>what am I chasing as a player? And after pumping an ungodly amount of money into these machines, you're chasing this. You're chasing the party time. And I'm sure you saw the same thing, Val, right? Your base game wins were nothing to get excited about. Your free spins weren't even that exciting, and you didn't get them very often.</v>

00:24:26.921 --> 00:24:46.441
<v Michael Gottlieb>They seem way, way, way out there. And it looks like this is the chase. This is what you want to do. It's what I wanted to do because it felt to me like the rest of the game was kind of like, forget about it. This is what hits. And when this thing goes, two, three, four of them, 100 bucks, 150 bucks, 200 bucks,</v>

00:24:47.161 --> 00:24:48.361
<v Michael Gottlieb>None of the game.</v>

00:24:47.241 --> 00:24:48.241
<v Val Levitan>It's actually exciting.</v>

00:24:49.321 --> 00:24:50.601
<v Val Levitan>It's actually exciting.</v>

00:24:49.441 --> 00:24:49.801
<v Michael Gottlieb>Yeah.</v>

00:24:51.241 --> 00:25:12.201
<v Michael Gottlieb>It's exciting and the dopamine hit of being in it and not knowing how long it's going to last, huge, huge. Because you're watching that and you're watching the hot streak thing that they have and you don't want it to end. Obviously, you want the thing to continue on and on.</v>

00:25:12.921 --> 00:25:32.601
<v Michael Gottlieb>So we're going to make sure that we work on that choreography and have it be exciting, have it be rewarding. But this definitely appears to be the mechanism by which they're giving meaningful wins to the player. And consequently, the pay tables, nothing to really get excited about. You know, I can I call it</v>

00:25:32.641 --> 00:25:41.641
<v Michael Gottlieb>gasoline or fuel to get to the oasis across the desert. It just kind of keeps you chugging along. It's time on device, but this is the real chase here.</v>

00:25:43.321 --> 00:26:02.041
<v Efim Podvoiski>I see it like you have the payout distribution and whatever is above $50 you put into this 50 this party time wins and you and you distribute it in some interesting way but this is this is the amount you play this like maybe</v>

00:26:02.761 --> 00:26:08.841
<v Efim Podvoiski>10, 15, 20% of RTP and you make insisting wins out of this.</v>

00:26:09.081 --> 00:26:24.201
<v Michael Gottlieb>But the part, but Efim, the party time win profile that Val and I experienced was not a single dollar, excuse me, not a single $50 win. It was always at least $100 and in many instances more than that. So when we...</v>

00:26:23.121 --> 00:26:30.441
<v Efim Podvoiski>Yeah, so if you go into party time, you mean you have 15 on the 1st and another two or?</v>

00:26:25.401 --> 00:26:25.801
<v Michael Gottlieb>Right.</v>

00:26:30.521 --> 00:26:33.721
<v Michael Gottlieb>Another one, another two. The point I'm making is that in...</v>

00:26:32.441 --> 00:26:46.441
<v Efim Podvoiski>Yeah, another one is given. So if you are in a party times that's given, you got 100, right? We agreed that we don't have in the party time, we do have smaller events. So yes, yes, yes. So discrete distribution, but</v>

00:26:35.921 --> 00:26:36.201
<v Michael Gottlieb>Right.</v>

00:26:41.801 --> 00:26:42.561
<v Michael Gottlieb>Exactly.</v>

00:26:45.801 --> 00:26:46.201
<v Michael Gottlieb>Yes.</v>

00:26:48.321 --> 00:26:54.041
<v Michael Gottlieb>And we'll, and we'll sweet spot it somewhere in that 150 to $250 range.</v>

00:26:53.721 --> 00:27:02.041
<v Efim Podvoiski>I guess so, I guess so, yeah, because going, going, going farther is is to to to to intricate.</v>

00:26:55.401 --> 00:26:58.441
<v Michael Gottlieb>Right, we'll have to, but it's not going to be 50. 50 is not enough.</v>

00:27:02.361 --> 00:27:21.321
<v Michael Gottlieb>Exactly. It's not going to happen often enough. I think I can almost guarantee we're going to be somewhere between 100 and 250. I don't know, Val, if you won more than 250 in their streak bonus on any one time. It seemed like 5 was the top end of what you could do.</v>

00:27:03.641 --> 00:27:05.321
<v Efim Podvoiski>Yes, yes, yes.</v>

00:27:21.401 --> 00:27:23.961
<v Michael Gottlieb>with their bonus, $250 win.</v>

00:27:23.241 --> 00:27:29.561
<v Val Levitan>I absolutely have no opinion. I have no opinion. I have no clue.</v>

00:27:26.761 --> 00:27:27.161
<v Michael Gottlieb>Okay.</v>

00:27:30.521 --> 00:27:34.441
<v Val Levitan>And I shouldn't be, I shouldn't be a binding on this, I just have no clue.</v>

00:27:30.721 --> 00:27:31.001
<v Michael Gottlieb>Okay.</v>

00:27:30.841 --> 00:27:31.321
<v Efim Podvoiski>Yeah.</v>

00:27:34.361 --> 00:27:39.081
<v Michael Gottlieb>Oh, I'm not asking for your opinion. I'm asking what your experience was when you were pumping money in the game.</v>

00:27:40.041 --> 00:27:47.801
<v Val Levitan>My experience was that I enjoyed the party time. Everything else was an enigma to me.</v>

00:27:48.441 --> 00:27:48.841
<v Michael Gottlieb>Okay.</v>

00:27:48.921 --> 00:27:50.281
<v Efim Podvoiski>Yeah, yeah, I think.</v>

00:27:49.401 --> 00:28:05.801
<v Val Levitan>I have no, I had no idea what was happening. I didn't really care, but when party time hits, I'm in the money and it's enjoyful, it's fast. I like the turbo thing because I just like the pace.</v>

00:28:06.681 --> 00:28:11.721
<v Val Levitan>I want to win or lose and move, move back, so turbo is not a bad thing.</v>

00:28:09.881 --> 00:28:10.841
<v Michael Gottlieb>Move on, right?</v>

00:28:12.921 --> 00:28:33.481
<v Michael Gottlieb>No, turbo's not a bad thing. I think your time on device player, I mean that location that we went to, that type of player, that's a $20 player, maybe a $50 player. If you play the way you're describing, and by the way, I did the same, excuse me, ****** thing, where I was so frustrated because I wanted free spins, I would put 200 bucks in there.</v>

00:28:33.801 --> 00:28:54.201
<v Michael Gottlieb>I turn the turbo on and just let go. And I burned through 200 bucks before I finished my peach flan. Joking to, you know, I mean, like the Mexican food, right? I mean, you just have to, there's a pacing there. I think autoplay is perfectly fine, but I think your average player is probably going to be pacing it slower. So all good. In any case, this is the confirmation message.</v>

00:28:54.521 --> 00:28:59.801
<v Michael Gottlieb>When you go to cash out, do you want to collect your $300 in cashable awards, right?</v>

00:29:01.241 --> 00:29:11.361
<v Lena Zhukova>Do you want me to change it to 250 or it doesn't? Do you want to change it to 300 to 250 or we don't know yet?</v>

00:29:01.401 --> 00:29:02.041
<v Michael Gottlieb>Go to the next.</v>

00:29:04.921 --> 00:29:05.481
<v Michael Gottlieb>To what?</v>

00:29:10.361 --> 00:29:22.041
<v Michael Gottlieb>No, no, no, no, no. Well, it's not it's not a function of we don't know yet. It's a function of whatever amount of awards the player happens to have. They might want to. Please go ahead.</v>

00:29:17.441 --> 00:29:18.121
<v Lena Zhukova>And.</v>

00:29:20.201 --> 00:29:22.681
<v Val Levitan>I'm sorry, sorry, I need to take this.</v>

00:29:23.001 --> 00:29:23.561
<v Michael Gottlieb>Yes, of course.</v>

00:29:25.401 --> 00:29:39.761
<v Michael Gottlieb>He is busy today. We all are. No, it's not, it's not, I mean, there can be, we have to determine what the minimal, minimal cashable award is. I think it's, I don't know if it's $5.</v>

00:29:30.041 --> 00:29:30.441
<v Lena Zhukova>I know.</v>

00:29:41.881 --> 00:30:01.241
<v Michael Gottlieb>But there's a minimum cashable award that you need in order to be able to cash out. So the number doesn't mean anything. Again, I think it's a function of let's storyboard the whole thing out so the engineers clearly understand, you know, what it is that we're doing.</v>

00:29:50.521 --> 00:29:51.001
<v Lena Zhukova>Hello.</v>

00:29:51.961 --> 00:29:52.521
<v Lena Zhukova>Okarak.</v>

00:30:07.321 --> 00:30:08.601
<v Michael Gottlieb>Well, we know he can stand.</v>

00:30:11.081 --> 00:30:12.601
<v Michael Gottlieb>Oh, poor Efim.</v>

00:30:13.961 --> 00:30:15.001
<v Michael Gottlieb>He's healing fast.</v>

00:30:26.841 --> 00:30:28.921
<v Michael Gottlieb>You okay, Efim, or do you need to take a break?</v>

00:30:29.001 --> 00:30:30.841
<v Efim Podvoiski>No, I am good, I am good, thank you, sorry.</v>

00:30:30.441 --> 00:30:31.881
<v Michael Gottlieb>Okay, okay.</v>

00:30:33.561 --> 00:30:38.841
<v Michael Gottlieb>Not here, no need to torture you. I'm impressed that you're doing as well as you are.</v>

00:30:39.961 --> 00:30:48.601
<v Michael Gottlieb>Given all the circumstances, so, um, yeah, this is our this is our uh confirmation for the cash out screen.</v>

00:30:51.801 --> 00:31:09.601
<v Michael Gottlieb>Felipe, by the way, Felipe was very complimentary, Lena, about the look of twin bison, about the look of the revised lion's riches. He was very impressed. And he was particularly enamored with the behavior of the parrots.</v>

00:30:58.441 --> 00:30:58.961
<v Lena Zhukova>Mhm.</v>

00:31:03.721 --> 00:31:04.201
<v Lena Zhukova>Good job.</v>

00:31:09.961 --> 00:31:14.201
<v Michael Gottlieb>and tropical paradise. That turned out really good.</v>

00:31:15.881 --> 00:31:34.081
<v Michael Gottlieb>You know, sometimes you try something and it works and sometimes you're like, oh, okay, this is pretty good. It, you know, it turned out really, really good. So positive feedback, always, always appreciate it. Okay, Val is back. So here's the confirmation screen and then go ahead to the next screen, Lena.</v>

00:31:16.601 --> 00:31:16.921
<v Lena Zhukova>No.</v>

00:31:33.681 --> 00:31:36.281
<v Lena Zhukova>And also, we have this kind of dialogue.</v>

00:31:36.601 --> 00:31:45.481
<v Michael Gottlieb>And then we've got the R version of continue playing, print the ticket, insert it back in the machine. We've got the graphic.</v>

00:31:47.081 --> 00:32:02.761
<v Michael Gottlieb>I didn't want to get too clever with this, Val, because, you know, Primero's kind of established the look and a bill validator is a bill validator, a hand is a hand. I don't know how much more, you know, variety we would want than what they're doing. So this is quite similar to what they're doing.</v>

00:32:05.161 --> 00:32:06.121
<v Val Levitan>Um...</v>

00:32:14.361 --> 00:32:15.241
<v Val Levitan>I'm not sure.</v>

00:32:24.441 --> 00:32:28.521
<v Michael Gottlieb>My philosophy is when you're messing with people's money, don't be clever.</v>

00:32:30.521 --> 00:32:36.041
<v Michael Gottlieb>We don't need to create animations. We don't need to have any fanfare. It's like an...</v>

00:32:35.161 --> 00:32:43.641
<v Val Levitan>I'm not about animation. I'm thinking, I'm thinking how to avoid putting a printer inside.</v>

00:32:38.521 --> 00:32:38.921
<v Michael Gottlieb>Yeah.</v>

00:32:44.601 --> 00:32:45.001
<v Lena Zhukova>And...</v>

00:32:45.001 --> 00:32:46.681
<v Michael Gottlieb>Ah, okay. Well, that's...</v>

00:32:52.841 --> 00:32:56.121
<v Val Levitan>Well, we can have our AFT with...</v>

00:33:01.321 --> 00:33:04.201
<v Val Levitan>The ticket scanner, the optical scanner.</v>

00:33:04.761 --> 00:33:05.241
<v Michael Gottlieb>Mhm.</v>

00:33:06.521 --> 00:33:12.521
<v Val Levitan>I just don't want to print another ticket. We already have ticket, we already have an e-mail in hand.</v>

00:33:13.881 --> 00:33:14.281
<v Michael Gottlieb>Okay.</v>

00:33:13.881 --> 00:33:14.601
<v Val Levitan>So.</v>

00:33:15.681 --> 00:33:19.601
<v Val Levitan>Theoretically, I could just scan the e-wallet again.</v>

00:33:20.761 --> 00:33:26.761
<v Val Levitan>But let's just leave it at that. Let's just leave it at this icon. We could always revise it.</v>

00:33:28.681 --> 00:33:38.521
<v Michael Gottlieb>Sure, yeah, the important thing is that the engineers understand the flow of what's going to happen, and this is the state of.</v>

00:33:40.281 --> 00:33:47.481
<v Michael Gottlieb>taking your money out and putting your money back, basically converting your awards back into credits.</v>

00:33:48.441 --> 00:33:49.561
<v Michael Gottlieb>That's the way we're going to.</v>

00:33:48.841 --> 00:33:52.841
<v Val Levitan>And yeah, I'd like to see the mirror. How do you show your mirrors?</v>

00:33:56.041 --> 00:34:00.361
<v Michael Gottlieb>Can you zoom out a little bit, Lena? The meters are on the bottom.</v>

00:34:03.721 --> 00:34:04.281
<v Michael Gottlieb>There you go.</v>

00:34:03.721 --> 00:34:10.841
<v Val Levitan>So, awards is large, you don't wanna show credits.</v>

00:34:12.201 --> 00:34:15.321
<v Val Levitan>more dominant at the point when you're transferring.</v>

00:34:13.721 --> 00:34:14.081
<v Michael Gottlieb>No.</v>

00:34:17.761 --> 00:34:18.761
<v Michael Gottlieb>When?</v>

00:34:21.721 --> 00:34:25.081
<v Val Levitan>Because the logic here is to have two pods.</v>

00:34:26.041 --> 00:34:28.281
<v Michael Gottlieb>Right, and we, and we have two, yeah.</v>

00:34:26.921 --> 00:34:38.601
<v Val Levitan>You transfer it from one and then you're winning into another. You're transferring back to the first one, you're reducing it, putting it into another. The whole thing is demonstration of the...</v>

00:34:40.761 --> 00:34:40.961
<v Val Levitan>No.</v>

00:34:48.521 --> 00:35:01.881
<v Michael Gottlieb>No, I get it. When the player completes the cash out process, the ticket will print and as concurrent with the ticket printing, as we normally do, your awards will go to zero.</v>

00:35:02.881 --> 00:35:04.921
<v Michael Gottlieb>because you have redeemed your awards.</v>

00:35:16.681 --> 00:35:29.241
<v Michael Gottlieb>I didn't find what Primera is doing as particularly confusing. It was more annoying. It was certainly annoying, but it wasn't particularly confusing. It was pretty clear as to how it all worked.</v>

00:35:37.561 --> 00:35:39.081
<v Val Levitan>Let's leave it like this for now.</v>

00:35:42.761 --> 00:35:44.441
<v Michael Gottlieb>Okay, is that all of Atlanta?</v>

00:35:44.921 --> 00:35:53.241
<v Lena Zhukova>Yeah, I think that's all like specific graphics we need to add and adjust in.</v>

00:35:48.041 --> 00:35:48.281
<v Michael Gottlieb>Yeah.</v>

00:35:55.761 --> 00:35:57.001
<v Lena Zhukova>Giorgi every three.</v>

00:35:57.081 --> 00:36:06.841
<v Val Levitan>I have another meeting in 7 minutes. So the only thing that is missing here, I need to see, you need to schedule that out for me.</v>

00:36:00.601 --> 00:36:00.921
<v Michael Gottlieb>Not.</v>

00:36:08.361 --> 00:36:26.761
<v Michael Gottlieb>Yes, we're not there yet. We're getting close. We're getting close. We're still blocking out. I literally just had the conversation with the theme this week about the math component and pieces of it. We do have a, there is a deadline in there. It is in JIRA. And then I'm going to be working with Lena next week on the different</v>

00:36:26.801 --> 00:36:33.321
<v Michael Gottlieb>pieces and parts of all of this and the time is going to take the storyboard. So 100%. It is all, it is all in, go ahead.</v>

00:36:31.721 --> 00:36:32.441
<v Lena Zhukova>Anton.</v>

00:36:31.881 --> 00:36:32.481
<v Val Levitan>Are you still?</v>

00:36:33.801 --> 00:36:39.241
<v Val Levitan>You feel this is this is you have your rust.</v>

00:36:40.521 --> 00:36:42.601
<v Val Levitan>Portion done, right?</v>

00:36:43.641 --> 00:36:45.961
<v Efim Podvoiski>Yes, it's ready for use, yes.</v>

00:36:46.281 --> 00:36:53.241
<v Val Levitan>Yes, yes, I know. So most likely this will be done in Omni.</v>

00:36:53.721 --> 00:36:55.881
<v Efim Podvoiski>Yeah, sure, no problem with it.</v>

00:36:55.881 --> 00:37:02.441
<v Lena Zhukova>So that's what we agreed that this Class A is going to be done in Nova. That's why.</v>

00:36:57.961 --> 00:36:58.761
<v Efim Podvoiski>Yeah, yeah.</v>

00:37:01.041 --> 00:37:01.481
<v Michael Gottlieb>Nova.</v>

00:37:01.401 --> 00:37:01.801
<v Efim Podvoiski>Yeah.</v>

00:37:02.121 --> 00:37:04.201
<v Val Levitan>Sorry, no, no, no, no, no.</v>

00:37:03.321 --> 00:37:05.401
<v Efim Podvoiski>No, yeah, you don't want to.</v>

00:37:03.561 --> 00:37:05.001
<v Michael Gottlieb>Oh yeah, right.</v>

00:37:03.881 --> 00:37:26.361
<v Lena Zhukova>Yeah, yeah, that's why we now we can focus on mass, and we also focus in with Dima, Sasha Biratko, and Igor on experimenting with assets transfer and how we are going to do liquid glass in Nova. So, once we finish Nebraska in production, we...</v>

00:37:26.521 --> 00:37:38.121
<v Lena Zhukova>We will be, we will have mass and we will know all our new game flow workflow in Nova and we will start full-blown production for this class A after Nebraska.</v>

00:37:38.601 --> 00:37:45.241
<v Val Levitan>Okay, let's briefly, quickly, literally 3 minutes. Let's look at the schedule.</v>

00:37:47.641 --> 00:37:48.041
<v Michael Gottlieb>OK.</v>

00:37:59.721 --> 00:38:14.681
<v Michael Gottlieb>Okay, so yeah, I mean, basically, as I indicated, we're working on the Class A Nova. Can you expand that game concept section IP 1190?</v>

00:38:16.841 --> 00:38:17.401
<v Michael Gottlieb>There you go.</v>

00:38:19.001 --> 00:38:26.041
<v Michael Gottlieb>So it's all in there now. The abstract for Lions Riches, we're targeting October 9th.</v>

00:38:27.481 --> 00:38:35.721
<v Michael Gottlieb>And then it's all in there. I'm starting. I've been cooking on this. I've got abstracts drafted for the rest of them, but everything leads with Lion's Riches.</v>

00:38:37.401 --> 00:38:39.641
<v Lena Zhukova>Yes, and design design for lunch.</v>

00:38:37.561 --> 00:38:44.121
<v Val Levitan>OK, so we see it, we see concept, we see concept ending at October 9th, is that what you're saying?</v>

00:38:44.041 --> 00:38:48.201
<v Michael Gottlieb>The abstract, yes, conceivably, we have to see, right?</v>

00:38:46.601 --> 00:38:47.721
<v Val Levitan>The abstract, yeah.</v>

00:38:48.921 --> 00:38:51.321
<v Val Levitan>OK, so then moving into design.</v>

00:38:52.441 --> 00:39:07.801
<v Lena Zhukova>Actually, design is already there, like for this one, because we already have for these games. I designed already all extra pieces we will need to add to each game, so design is basically already done for.</v>

00:38:57.561 --> 00:38:57.961
<v Michael Gottlieb>Right.</v>

00:39:08.121 --> 00:39:11.081
<v Efim Podvoiski>Except the mass, I don't know.</v>

00:39:10.281 --> 00:39:26.361
<v Lena Zhukova>No, no, I mean, I mean only only visual parts, and it still it will be changed, maybe because, as we discussed, maybe this dialogue will be changed, or we will change dashboard, but we will know basic pieces we will need to add to the games.</v>

00:39:10.361 --> 00:39:10.761
<v Michael Gottlieb>Right.</v>

00:39:11.241 --> 00:39:12.401
<v Val Levitan>OKOK, so.</v>

00:39:11.881 --> 00:39:12.281
<v Michael Gottlieb>Art.</v>

00:39:13.721 --> 00:39:14.121
<v Michael Gottlieb>Right.</v>

00:39:26.601 --> 00:39:32.281
<v Michael Gottlieb>Right, but we still need to create the storyboards so the engineers understand what this is going to be.</v>

00:39:31.401 --> 00:39:36.361
<v Lena Zhukova>OK, I will add, I will add this another feature to my.</v>

00:39:35.961 --> 00:39:37.721
<v Michael Gottlieb>We have to have storyboards.</v>

00:39:38.001 --> 00:39:46.281
<v Lena Zhukova>Yes, I will add, I will close this feature, like of graphical adaptation, and now I will create all storyboards, yes.</v>

00:39:49.481 --> 00:39:50.041
<v Val Levitan>Okarak.</v>

00:39:51.241 --> 00:39:54.601
<v Val Levitan>And the production part of it has not been measured yet, right?</v>

00:39:55.321 --> 00:40:00.921
<v Lena Zhukova>No, no, because we will not start it until December, January.</v>

00:39:55.761 --> 00:39:56.841
<v Michael Gottlieb>No, nothing is.</v>

00:40:03.321 --> 00:40:08.201
<v Lena Zhukova>But we will, we will do R&D during this month.</v>

00:40:10.681 --> 00:40:13.881
<v Val Levitan>Okay, I cannot spend any more time with you today.</v>

00:40:15.161 --> 00:40:17.001
<v Val Levitan>if we need to talk about something else.</v>

00:40:18.201 --> 00:40:19.641
<v Val Levitan>I'm happy to do it on Monday.</v>

00:40:20.521 --> 00:40:23.881
<v Michael Gottlieb>Okay, can I throw in one quick one or do you need to go right now?</v>

00:40:24.081 --> 00:40:25.081
<v Val Levitan>No, no, go ahead.</v>

00:40:25.481 --> 00:40:46.921
<v Michael Gottlieb>Okay, just making the point that this is all being done in Jira and Confluence. And I know that the guys are using GitHub for code, but you had mentioned at some point that we may be migrating to GitHub for other elements as well. So I'm just letting you know we're going full steam ahead with Confluence and</v>

00:40:47.481 --> 00:40:56.361
<v Michael Gottlieb>And JIRA and building everything right now in Confluence and JIRA for the for the for the first set of Nova products, just so you know.</v>

00:40:56.281 --> 00:41:09.321
<v Val Levitan>Yes, yes, but also I want you to know that there might be some redundancy and there might be some migration in the way. I cannot predict how and when. And honestly, I don't have the bandwidth for this right now.</v>

00:41:09.881 --> 00:41:14.121
<v Michael Gottlieb>Okay, perfectly fine. Just again, being communicative. No, didn't want any surprises. Yep.</v>

00:41:10.921 --> 00:41:11.201
<v Lena Zhukova>And.</v>

00:41:12.521 --> 00:41:17.401
<v Lena Zhukova>We will try, we will transfer a conference document to M.D. when when it's needed.</v>

00:41:16.681 --> 00:41:23.081
<v Val Levitan>It's quite, yes, it's quite easy, yes, yes, but, but, but if that comes to...</v>

00:41:18.681 --> 00:41:19.481
<v Lena Zhukova>Yeah, yeah.</v>

00:41:25.081 --> 00:41:33.601
<v Val Levitan>If that materializes, then just don't get upset with me that it's partially redundant work. It's repetitive work.</v>

00:41:34.561 --> 00:41:35.481
<v Michael Gottlieb>Nobody's upset.</v>

00:41:35.401 --> 00:41:38.521
<v Val Levitan>I just don't have, I just don't have the bandwidth for this now.</v>

00:41:38.281 --> 00:41:41.481
<v Michael Gottlieb>We are all happy, great leader. Thank you for your time. Have a great weekend.</v>

00:41:41.241 --> 00:41:43.441
<v Val Levitan>Okay. Thank you. Have a good weekend. Bye-bye.</v>

00:41:42.281 --> 00:41:43.881
<v Lena Zhukova>Okay, thank you. Bye.</v>

00:41:44.601 --> 00:41:45.161
<v Efim Podvoiski>Bye.</v>

