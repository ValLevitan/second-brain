# Raw Transcript — Game_Development
**Date:** October 30, 2026, 2:00 PM – 3:09 PM Eastern
**Summary note:** [[Meeting_Notes_Game_Development_Class_A_Party_Time_and_Colombia_Refresh-October-30-2026]]
---
WEBVTT

00:00:07.697 --> 00:00:09.217
<v Val Levitan>Good afternoon, morning.</v>

00:00:09.857 --> 00:00:11.697
<v Michael Gottlieb>Hey Val, how are you?</v>

00:00:11.297 --> 00:00:12.577
<v Val Levitan>How's everyone doing?</v>

00:00:13.617 --> 00:00:14.177
<v Efim Podvoiski>Good, good.</v>

00:00:14.737 --> 00:00:15.217
<v Michael Gottlieb>Code.</v>

00:00:16.257 --> 00:00:16.657
<v Val Levitan>Really?</v>

00:00:17.217 --> 00:00:17.937
<v Michael Gottlieb>How are you?</v>

00:00:18.897 --> 00:00:19.857
<v Val Levitan>Alright, OK.</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

00:00:40.257 --> 00:00:40.657
<v Val Levitan>Igor.</v>

00:00:41.777 --> 00:00:42.417
<v Michael Gottlieb>Fair enough.</v>

00:00:42.257 --> 00:00:42.337
<v Val Levitan>Ha.</v>

00:00:44.257 --> 00:01:03.817
<v Michael Gottlieb>So I've been working this week on refining the Nebraska dual skill box behavior. The history of it is that, if you remember, we originally had that power meter thing going back and forth, and that</v>

00:01:04.337 --> 00:01:24.017
<v Michael Gottlieb>dictated a lot of how the choreography and the flow worked. And then very quickly, we switched over to dual box for Nebraska and did a, I guess, just a very quick implementation. But now in reviewing it and looking at some of the things that I saw in Georgia</v>

00:01:24.337 --> 00:01:43.577
<v Michael Gottlieb>We're going to make, we have made a couple of changes to it. Primarily what we were doing before is on a winning spin, the reels would stop, the dual box would come up and we would show you how much you've won. We're not going to do that anymore. The reels are going to stop.</v>

00:01:43.697 --> 00:02:02.497
<v Michael Gottlieb>The dual box is going to come up. The win is going to say 0 because you haven't won anything yet. And then when you press the correct coin, then we're going to rack. And I think that behavior makes more sense. And it also works better with the bonus behavior of not triggering the bonus until after you pick the correct.</v>

00:02:02.817 --> 00:02:04.897
<v Michael Gottlieb>Coin, so it gives us more continuity.</v>

00:02:06.417 --> 00:02:25.577
<v Michael Gottlieb>makes more sense because we're no longer shackled by that wind meter thing that we had before. So I wanted to take a fresh look at it. And I think the guys are, I let the guys know yesterday, so hopefully we'll have a new build in the not too distant future. We can have a look at it and see how that's coming along.</v>

00:02:29.057 --> 00:02:31.297
<v Michael Gottlieb>And then, um, Efim.</v>

00:02:30.297 --> 00:02:35.697
<v Val Levitan>Are you are you convinced that are you convinced that showing a zero value is a good thing?</v>

00:02:35.857 --> 00:02:37.777
<v Michael Gottlieb>Hundred percent, absolutely.</v>

00:02:40.177 --> 00:03:01.617
<v Michael Gottlieb>Yeah, there's no doubt in my mind. We were doing what we were doing for different reasons. And then when that wind meter went away, we just switched over to the dual box really quick because we were just trying to get it done really fast, which was fine. I don't think there's anything wrong with it, but I think it's superior doing it the way that we've described doing it.</v>

00:03:02.257 --> 00:03:21.217
<v Michael Gottlieb>And so we've got that, I think, nailed down. I'll play the build and see if it feels right. And then Efim and I are continuing to talk this week about the, now I'm switching over to Class A, about how the Class A Georgia behavior is going to work specifically in regard to free games.</v>

00:03:21.377 --> 00:03:40.257
<v Michael Gottlieb>and the idea that because you can only win 50 bucks in free games before you get win capped, that we were going to have the player after free games is over going to party time. But we had to basically go through the logic flow and say, okay, well, what if the player cashes out? So that would disable it.</v>

00:03:40.577 --> 00:03:59.017
<v Michael Gottlieb>what if the player changes bets, right? That would disable that potentiality of being able to trigger it. So basically, you know, Efim has got a big brain. He had some additional combinations and permutations that we needed to discuss. So we went through that. I think we're in a good place on that. But then there's the whole aspect.</v>

00:03:59.937 --> 00:04:17.817
<v Michael Gottlieb>of math and hit frequency and EV and how often it happens. I told Efim when I play, I played the hell out of those games and free spins did not seem to be something that was particularly achievable. They seem to be way, way, way out there. But more importantly, once you play those games, all you're chasing</v>

00:04:18.257 --> 00:04:30.977
<v Michael Gottlieb>is the winning streak feature or our party time feature. That's really all you want. The base game wins are not anything to get excited about. There's nothing there that it...</v>

00:04:30.177 --> 00:04:36.577
<v Val Levitan>So, what do you do? What? So, what do you do with base base game? You do you award any wins at all?</v>

00:04:36.857 --> 00:04:59.777
<v Michael Gottlieb>Oh, sure, yeah, we'll definitely award wins in the base game, and there'll be some water to help get you around the desert to the get you across the desert to the oasis, but this, the just the mathematical profile of what they're doing with that, there's a lot, there's a meaningful amount of Rtp coming out of those fifty-dollar.</v>

00:05:00.257 --> 00:05:11.457
<v Michael Gottlieb>those $50 wins. I mean, you saw it, right? You, you, when you were playing it, you saw that you were really chasing that. And when you don't have that, it's not all that exciting. But.</v>

00:05:10.897 --> 00:05:22.257
<v Val Levitan>Well, it's all about getting the party time. Base is not important. And as you say, it's water to get you through the desert.</v>

00:05:14.257 --> 00:05:16.577
<v Michael Gottlieb>Exactly. That's exactly right. Yep.</v>

00:05:22.817 --> 00:05:23.537
<v Michael Gottlieb>Right, right.</v>

00:05:23.137 --> 00:05:24.817
<v Val Levitan>That's the right approach.</v>

00:05:25.217 --> 00:05:46.177
<v Michael Gottlieb>And philosophically, Efim and I were going back and forth because I had established a rule that if you get party time, you'll get it twice at minimum. You can get more, but you get it twice. Now, twice is $100. Okay, that's pretty decent. The problem is, is that if we're going to trigger party time coming out of free spins,</v>

00:05:46.497 --> 00:06:09.097
<v Michael Gottlieb>we don't have enough money necessarily to trigger it twice. So then we're going to only trigger potentially, if the math plays out in such a fashion, we'll only trigger party time maybe once after free spins. And Efim's argument was, well, maybe that's disappointing to the player. And I'm like, I don't think it's disappointing to the player because they've won 50 bucks in free spins. They got win cap. They're kind of ******. And then on the next</v>

00:06:09.177 --> 00:06:29.457
<v Michael Gottlieb>spin, they get thrown another $50. I don't know how you can be bent out of shape about that, right? So that's my premise and my theory. I think that free spins is, we kind of take the sting out of getting wind capped at the 50 bucks. And of course, you're not always going to get wind capped, but if you get wind capped and we're in a scenario where we need to give you back more.</v>

00:06:30.097 --> 00:06:49.217
<v Michael Gottlieb>I think giving, you know, basically doubling your win on the first spin after free spins makes all the sense in the world. And it's okay that it's only one. Because you've got free spins, you come out of free spins, you get the surprise and delight of hitting party time once. And now I thought I had a $50 win and I got win cap, and all of a sudden I got a $100 win. I think it'll be a surprise.</v>

00:06:49.297 --> 00:06:50.537
<v Michael Gottlieb>Rise and delight factor.</v>

00:06:53.017 --> 00:07:02.297
<v Michael Gottlieb>So that's where we're at now. But obviously all of this is theoretical. Up until the point we actually have the games up and running, we'll know more and learn more and whatever else.</v>

00:07:08.017 --> 00:07:09.937
<v Michael Gottlieb>So that's what's going on there.</v>

00:07:09.017 --> 00:07:11.297
<v Val Levitan>Seems, seems, seems logical.</v>

00:07:11.697 --> 00:07:33.377
<v Michael Gottlieb>Yeah, it makes sense. And it's not, you know, first rule of medicine is do no harm. I don't think we're doing anything unconventional or drastic or crazy or anything like that. I mean, I think it's within the realm of expectation and logic and reason. The question is, does the player perceive the glass as half empty or half full? And I think that if they get a party time coming out of free spins,</v>

00:07:34.097 --> 00:07:46.577
<v Michael Gottlieb>that'll feel like the glass is half full. Like, yeah, I got wind capped, but hey, boom, just doubled my win. I got wind capped at 50 bucks and then bam, I got another 50 bucks. Who can be angry about that? I don't know.</v>

00:07:47.937 --> 00:07:48.817
<v Michael Gottlieb>Yeah, so that's what...</v>

00:07:47.937 --> 00:07:51.377
<v Val Levitan>And what is the what? What is the wind frequency?</v>

00:07:53.297 --> 00:07:55.537
<v Michael Gottlieb>Haven't determined that yet. I think Efim's gotta...</v>

00:07:57.857 --> 00:08:00.097
<v Michael Gottlieb>The wind frequency of how often party time triggers.</v>

00:08:02.977 --> 00:08:03.697
<v Val Levitan>Well...</v>

00:08:06.257 --> 00:08:17.697
<v Efim Podvoiski>It's obviously, obviously it depends on your bid, because the higher the bid, the more often it happens, because it's always $50, so there is no, it's not scaled.</v>

00:08:06.417 --> 00:08:08.097
<v Val Levitan>Yeah, yeah.</v>

00:08:19.617 --> 00:08:25.137
<v Efim Podvoiski>You cannot give, if you play 25 cents, $15 is a lot.</v>

00:08:26.657 --> 00:08:29.377
<v Efim Podvoiski>It's like 400 beds.</v>

00:08:30.377 --> 00:08:32.577
<v Efim Podvoiski>Two 100 bits, so it's...</v>

00:08:32.257 --> 00:08:40.177
<v Val Levitan>But why do you? Why do you have to give $50 on the twenty-five cent bet? Why can't you give us?</v>

00:08:40.657 --> 00:08:46.897
<v Michael Gottlieb>That's what our competitors are doing. When you hit that bonus round, you win 50 bucks. That's the lowest win that I saw.</v>

00:08:47.937 --> 00:08:49.777
<v Val Levitan>I know, but why do we have to do that?</v>

00:08:50.337 --> 00:09:09.657
<v Michael Gottlieb>Well, because you don't want to be less than. Now it's all a balance. I will absolutely say to you that once we get this up and playing and on some of the lower bet levels, it feels like you never hit party time. Yeah, we're going to have a conversation about 10, 20, 30, 40, and $50 wins and basically tie the win levels</v>

00:09:08.977 --> 00:09:09.617
<v Val Levitan>But we.</v>

00:09:09.737 --> 00:09:10.577
<v Michael Gottlieb>to the bet levels.</v>

00:09:10.817 --> 00:09:14.097
<v Val Levitan>But we already, we already saw it, we know that.</v>

00:09:15.457 --> 00:09:18.257
<v Val Levitan>On the competitor's machine, Betty.</v>

00:09:20.177 --> 00:09:22.577
<v Val Levitan>Smaller bets is frustrating.</v>

00:09:24.817 --> 00:09:27.617
<v Val Levitan>We've experimented with it already, we know.</v>

00:09:28.097 --> 00:09:28.497
<v Michael Gottlieb>Yeah.</v>

00:09:30.897 --> 00:09:35.377
<v Michael Gottlieb>So, you're an advocate of winning smaller, having smaller wins in party time?</v>

00:09:36.817 --> 00:09:39.417
<v Efim Podvoiski>And to me, it's...</v>

00:09:40.737 --> 00:09:46.177
<v Efim Podvoiski>Not necessarily because you can just give $50 a win. Why would you go?</v>

00:09:45.377 --> 00:09:48.897
<v Michael Gottlieb>Frequency to have it, have it, have it happen more often.</v>

00:09:46.417 --> 00:09:48.377
<v Val Levitan>Frequency, frequency.</v>

00:09:49.617 --> 00:09:52.177
<v Efim Podvoiski>To have a party time as an event.</v>

00:09:49.777 --> 00:09:51.177
<v Val Levitan>Frequency invasion.</v>

00:09:54.577 --> 00:09:55.977
<v Val Levitan>The issue is the frequency.</v>

00:09:54.737 --> 00:10:06.777
<v Michael Gottlieb>Yeah, have party time, have, yeah, have party time hit multiple times. I mean, Val was playing and he was playing on a pretty decent bet level and he popped 50, 50, 50. I mean, I think you got 250 bucks in one session.</v>

00:10:04.297 --> 00:10:04.657
<v Efim Podvoiski>Yeah.</v>

00:10:05.697 --> 00:10:10.017
<v Val Levitan>I want 800, I want $800, which is, you know...</v>

00:10:10.897 --> 00:10:11.537
<v Val Levitan>Crazy.</v>

00:10:12.737 --> 00:10:15.857
<v Val Levitan>But Felipe was playing machine next to me.</v>

00:10:16.897 --> 00:10:20.737
<v Val Levitan>And he was conservative in his beds, and he lost money.</v>

00:10:21.457 --> 00:10:21.937
<v Michael Gottlieb>Right.</v>

00:10:22.337 --> 00:10:24.577
<v Efim Podvoiski>Yeah, but obviously it was money, anyway.</v>

00:10:25.697 --> 00:10:42.097
<v Michael Gottlieb>Yeah, but Val's point is that the experience should be as good for somebody betting it. We're failing if the if the experience at 5 bucks a spin is significantly superior to the experience at the at the lower bet levels. My concern.</v>

00:10:41.497 --> 00:10:45.977
<v Val Levitan>And, and, and that is, and that is well said. That's exactly how I felt.</v>

00:10:46.417 --> 00:11:05.857
<v Michael Gottlieb>Right. But then the flip is you don't want to be less than your competitor, right? I mean, if you're sitting in the exact same place as your competitor right next to it, and there's somebody's playing and they get the winning streak and the winning streak pops them 50 bucks at a time and we're only popping them 10 bucks at a time,</v>

00:11:06.577 --> 00:11:08.577
<v Michael Gottlieb>They might perceive that as a negative.</v>

00:11:09.457 --> 00:11:16.817
<v Michael Gottlieb>They might feel that it's that it's less than, right? Because perception is really, really important. It really and truly is, you know.</v>

00:11:19.137 --> 00:11:27.937
<v Michael Gottlieb>We will play it once we get the math up and going. And if we find that the frequency of party time at the...</v>

00:11:30.337 --> 00:11:49.777
<v Michael Gottlieb>not lowest bet level, but kind of mid to lower bet levels is unacceptable, then we'll have the conversation about, you know, having it done. Because there's also something to be said of the illusion of multiple events replacing cold hard cash.</v>

00:11:50.057 --> 00:12:03.057
<v Michael Gottlieb>And what I mean, here's a thought experiment. I hit winning streak and I win 50 bucks once, versus I go into party time and I win $10 three times in a row. What experience is more exciting?</v>

00:12:04.097 --> 00:12:25.697
<v Michael Gottlieb>hitting $10 three times in a row, right? It gets your cortisol or adrenaline or whatever the hell it is, the endorphins, the endorphins, it gets your endorphins pumping and you're in the event for a longer period of time. You feel like, oh, I just keep winning, winning, winning. So there is a case to be made for that. There is a case to be made for that. So we're not set in stone.</v>

00:12:26.737 --> 00:12:30.337
<v Michael Gottlieb>But we're going to start with that $50 and see what it feels like.</v>

00:12:34.697 --> 00:12:36.337
<v Michael Gottlieb>You don't agree? You're making the face.</v>

00:12:38.817 --> 00:12:42.977
<v Val Levitan>I don't have enough knowledge to say I agree or disagree. I don't know.</v>

00:12:44.257 --> 00:12:45.777
<v Val Levitan>If I had a concrete...</v>

00:12:49.137 --> 00:12:50.897
<v Val Levitan>A position, I would have said that.</v>

00:12:51.977 --> 00:12:52.417
<v Michael Gottlieb>Turn off.</v>

00:12:55.057 --> 00:13:00.977
<v Val Levitan>The logic, the logic tells me that most people don't play on maximum bet.</v>

00:13:03.137 --> 00:13:18.417
<v Val Levitan>So the experience would definitely be negative. Even if you have two machines side by side, and they award only 50 bucks on their machine, then the experience on our machine would be much better because we award.</v>

00:13:19.377 --> 00:13:20.177
<v Val Levitan>Something.</v>

00:13:21.377 --> 00:13:42.177
<v Val Levitan>And if, and the logic tells me if it's all about party time and the excitement about getting party time and multiple wins within party time, then I would rather go for smaller wins on a per win basis, increase the frequency of wins, which is exactly what you said,</v>

00:13:42.377 --> 00:13:50.097
<v Val Levitan>Where is the best experience: 3 * 10 or 1 * 50? Three times 10 is better, so...</v>

00:13:52.657 --> 00:14:07.217
<v Michael Gottlieb>There's a case to be made both ways. We'll have to look at the math. The only reason I'm holding on to our current approach is that I'm not convinced that it's going to be unacceptable at like bet level 2 with $50 wins.</v>

00:13:52.977 --> 00:13:53.377
<v Efim Podvoiski>Spins.</v>

00:14:07.857 --> 00:14:12.337
<v Val Levitan>We know that the competitive machines doesn't really make money.</v>

00:14:13.457 --> 00:14:13.777
<v Efim Podvoiski>Oh.</v>

00:14:14.657 --> 00:14:20.497
<v Efim Podvoiski>But why people are so excited about them? I mean, operators, operators.</v>

00:14:18.177 --> 00:14:35.817
<v Val Levitan>People are excited. First of all, let's define excited. I don't think anybody is particularly excited about what the machine makes. The industry is excited about the potential of unregulated Class A</v>

00:14:24.017 --> 00:14:24.417
<v Efim Podvoiski>Yes.</v>

00:14:36.897 --> 00:14:38.737
<v Val Levitan>machine entering the market.</v>

00:14:39.697 --> 00:14:42.337
<v Val Levitan>So I think there is a confusion about...</v>

00:14:43.457 --> 00:14:45.137
<v Val Levitan>The definition of excitement.</v>

00:14:47.217 --> 00:14:53.617
<v Michael Gottlieb>It bypasses the tax, Efim. There's like some ridiculous tax, and by doing Class A, there's like no tax, so...</v>

00:14:54.097 --> 00:14:59.017
<v Val Levitan>Well, and also, and also truly unprecedented.</v>

00:14:59.937 --> 00:15:19.937
<v Val Levitan>amount of locations available to you. Because they're not regulated. You could have as many machines as you want in one location. So right now the market is 47,000 machines, but Class A, if it's properly manufactured, may take it to</v>

00:15:07.617 --> 00:15:09.137
<v Michael Gottlieb>Anywhere, yeah.</v>

00:15:22.017 --> 00:15:36.417
<v Val Levitan>100,000 machines? Imagine the growth of the market. That's crazy. That's the exciting part. But what's not exciting is that machine right now does not make money.</v>

00:15:27.697 --> 00:15:28.097
<v Michael Gottlieb>Right.</v>

00:15:31.377 --> 00:15:32.017
<v Efim Podvoiski>But this...</v>

00:15:38.217 --> 00:15:45.937
<v Michael Gottlieb>When you use a figure of speech not make money, can you elaborate on that relative to its cost you mean or compared to its competitors or what does that mean?</v>

00:15:46.337 --> 00:15:48.417
<v Val Levitan>Well, there's no competitors really yet.</v>

00:15:48.817 --> 00:15:49.297
<v Michael Gottlieb>Right.</v>

00:15:52.577 --> 00:15:54.097
<v Michael Gottlieb>It makes more money than an MT.</v>

00:15:52.977 --> 00:15:53.937
<v Val Levitan>That's not done.</v>

00:15:54.817 --> 00:16:04.737
<v Val Levitan>Does not make money, meaning some of the locations make $6 a day per machine, and some and some make.</v>

00:15:55.177 --> 00:15:55.537
<v Michael Gottlieb>Sorry.</v>

00:16:02.417 --> 00:16:03.457
<v Michael Gottlieb>Oh, Jesus. Okay.</v>

00:16:08.177 --> 00:16:09.697
<v Val Levitan>Forty dollars a day.</v>

00:16:11.217 --> 00:16:11.697
<v Val Levitan>But...</v>

00:16:12.817 --> 00:16:15.697
<v Val Levitan>Either 6, first of all, 6 and 40.</v>

00:16:16.977 --> 00:16:24.977
<v Val Levitan>Either is not really exciting, but at $40, okay, it's, I mean, we have a business of $40, but...</v>

00:16:19.697 --> 00:16:20.177
<v Michael Gottlieb>Right.</v>

00:16:26.177 --> 00:16:30.177
<v Val Levitan>The disparity between 6:00 and 40 is huge.</v>

00:16:31.817 --> 00:16:36.337
<v Val Levitan>And nobody will dive into a business at such spread.</v>

00:16:38.737 --> 00:16:42.497
<v Val Levitan>It will, it it will be very, very cautious market.</v>

00:16:38.977 --> 00:16:40.097
<v Michael Gottlieb>Interesting.</v>

00:16:43.217 --> 00:16:47.217
<v Michael Gottlieb>Okay, this is new information. This is new data for me, Efim.</v>

00:16:46.417 --> 00:17:04.537
<v Val Levitan>That makes me believe that the current machine is not interesting. A couple of remarks from operators also, you know, they don't find the play in particularly interesting. I also don't find the play in particularly interesting unless you hear what we</v>

00:16:50.537 --> 00:16:51.137
<v Michael Gottlieb>Clearly.</v>

00:17:04.617 --> 00:17:06.097
<v Val Levitan>defined as party time.</v>

00:17:06.417 --> 00:17:06.817
<v Michael Gottlieb>Right.</v>

00:17:08.657 --> 00:17:15.537
<v Val Levitan>So that's why I'm asking what's the frequency of party time, but you're telling me now that the frequency of party time.</v>

00:17:16.657 --> 00:17:21.057
<v Val Levitan>is dependent on the bed. Well, I can tell you for sure that...</v>

00:17:22.177 --> 00:17:27.977
<v Val Levitan>Especially on the new machine, a player will not be betting $5 or $6.</v>

00:17:27.057 --> 00:17:27.617
<v Michael Gottlieb>Agreed.</v>

00:17:28.497 --> 00:17:30.097
<v Michael Gottlieb>Agreed. No question.</v>

00:17:29.377 --> 00:17:40.017
<v Val Levitan>And we already know that the player really feels comfortable at around a dollar. That's really an average bet. Well, a dollar to $1.50, you know.</v>

00:17:41.457 --> 00:17:45.937
<v Val Levitan>But definitely not $5 and or $6, so...</v>

00:17:47.137 --> 00:18:06.897
<v Val Levitan>Why cater to a player at $5 bet if we need to, if we already know that we need to cater to a player at a dollar? And at a dollar, the frequency of party time is not sufficient for us because the multiplier between the bet and the win is huge.</v>

00:18:07.577 --> 00:18:12.097
<v Efim Podvoiski>Fifty is not that huge; it's reasonable, but...</v>

00:18:07.777 --> 00:18:08.497
<v Val Levitan>Do you wanna?</v>

00:18:12.417 --> 00:18:18.657
<v Michael Gottlieb>Yeah, but what he's saying is that the model that's been put forth by Primero isn't working.</v>

00:18:19.817 --> 00:18:39.217
<v Michael Gottlieb>So there's no reason to chase what isn't working, okay? And within that context, there have been, and I've talked about this before, where there are mechanics where you hit a progressive, a low-level progressive, multiple times.</v>

00:18:24.097 --> 00:18:24.657
<v Efim Podvoiski>Okay.</v>

00:18:39.617 --> 00:18:58.257
<v Michael Gottlieb>Instead of having a $50 Progressive, you'll hit the same $10 progress. Well, shoot, we do it in the Hold and Respin Bonus, right? You can win, you can win the lower level progressive multiple times. So again, from the standpoint of endorphins and adrenaline,</v>

00:18:58.737 --> 00:19:19.537
<v Michael Gottlieb>It's more rewarding to pop a $10 party time three times in a row. Boom, boom, boom. Oh, is this ever going to end? This is great. This is amazing. Versus A one-time pop of $50, which is never going to happen, right? Because we're at a lower bet level. So we have concerns about hit frequency. I get that.</v>

00:19:38.177 --> 00:19:38.977
<v Efim Podvoiski>Yes, of course.</v>

00:19:39.057 --> 00:20:00.817
<v Michael Gottlieb>off party time, if we set it 5 bet levels, 10, 20, 30, 40, 50, I'm just being arbitrary, but just as a thought experiment, then even if you're a 25 cent player, you can pop party time once or twice and win 10 or $20. And that's a perfectly reasonable win for a 25 cent player, right? Or A 50 cent player. So</v>

00:20:01.137 --> 00:20:03.857
<v Michael Gottlieb>Okay, Val, I'm with you. I'm with you. I hear what you're saying.</v>

00:20:02.977 --> 00:20:03.857
<v Efim Podvoiski>I am looking.</v>

00:20:04.897 --> 00:20:24.657
<v Efim Podvoiski>I am not looking at this from a different perspective. Okay, let's look on a normal game. It's normal because in a machine, people are playing it. People are playing Georgia, which is even less fun because you have this nudge and something interrupts your playing.</v>

00:20:25.537 --> 00:20:44.097
<v Efim Podvoiski>You can have a good game at 25 cents. You have free spins, you have some bonus. Why not? And occasionally you have your progress. We can replicate this game. And the problem the party time solves is that there is a hard cap on 50 cents.</v>

00:20:44.177 --> 00:21:04.057
<v Efim Podvoiski>dollars and when you go into one, two, three, especially $5 bets, this $50 win is nothing. So now party time goes into play. And so party time allows players who bet at least $2.00 to have a meaningful game. But game can be interesting without it if you just...</v>

00:20:45.057 --> 00:20:45.457
<v Michael Gottlieb>Right.</v>

00:21:04.337 --> 00:21:20.177
<v Efim Podvoiski>If this cup is not hitting you, unless we consider then party time is a great invention on itself, and suddenly we have the stool that we are not using on smaller beds. If this is approach, yes.</v>

00:21:19.937 --> 00:21:39.697
<v Michael Gottlieb>I think I think it is. I think it's I think it is an interesting innovation. I think that the players being trained by Primero to chase their winning streak feature. That's the only thing of value in the game. The rest of the game is ****. Let's call it what it is. I mean, I get what you're saying, Val. I didn't find anything redeeming.</v>

00:21:40.017 --> 00:22:01.057
<v Michael Gottlieb>in those games other than the winning streak feature, because that's where all the money is. So, and I said this to you a couple days ago, we were just talking about this a couple days ago, Efim, that the base game has nothing. Free Spins is kind of a, and the other, I will also make the argument to you that we increase the value of free spins, we make free spins</v>

00:22:01.697 --> 00:22:19.937
<v Michael Gottlieb>Great again, we give free spins some legitimacy if the party time wins aren't as high, right? Because if you're winning 50 bucks in party time, but you're freaking win capped at 50 bucks in free spins, but party time can trigger more than once and free spins is a hard $50 ceiling.</v>

00:22:21.137 --> 00:22:34.337
<v Michael Gottlieb>Free Spins is less than. It is not what you're chasing. So I think we're also achieving the point of giving some chase to Free Spins by bringing those, bringing the party time cap down.</v>

00:22:25.537 --> 00:22:26.417
<v Efim Podvoiski>Yes, yes.</v>

00:22:35.297 --> 00:22:40.337
<v Michael Gottlieb>and having it hit more often, I think it gives us some more flexibility, you know.</v>

00:22:41.777 --> 00:23:06.137
<v Michael Gottlieb>People want to win. And on the games that Val and I played, you don't win unless you bet high and unless you pop the winning streak. That's it. I mean, I can personally tell you, I pumped $800 through those things. And basically, you're begging for winning streak. There's not one other feature in that game. And free spins don't trigger. And they did trigger once.</v>

00:23:06.137 --> 00:23:17.217
<v Michael Gottlieb>and I was on a higher bet level and I won like 30 bucks. I was trying to win cap free spins to see if they messaged right, how they treated it. And I couldn't even do it. I didn't have a great experience. I'll acknowledge that.</v>

00:23:18.337 --> 00:23:36.817
<v Michael Gottlieb>So I think Val is right. I think let's give it some thought a theme to what the most rational way of implementing it. And it doesn't have to be hard and fast. It doesn't have to be, you know, if you bet a dollar, party time can only be $10. You can set up a bin and pick from a bin and have a variety of values if you want.</v>

00:23:38.497 --> 00:23:51.377
<v Michael Gottlieb>Although having it be linear might be interesting because it just like progressive values going up, right? Progressive values go up as you bet more. Maybe the party time value goes up as you bet more. 10, 20, 30, 40, 50.</v>

00:23:54.017 --> 00:24:04.817
<v Michael Gottlieb>Okay, I'm sold. I'm not gonna, I'm certainly, I have no kind, if you're telling me the stuff they're doing is not working, there is no argument to be made. This is an opportunity, Efim.</v>

00:24:03.377 --> 00:24:07.057
<v Val Levitan>Well, that, that, that, that I know factually.</v>

00:24:07.217 --> 00:24:07.617
<v Michael Gottlieb>Okay.</v>

00:24:09.217 --> 00:24:17.857
<v Michael Gottlieb>I think it's an opportunity, Efim. I think we can, if we just basically treat it like a mystery progressive, if you will, and think about it like a mystery progressive.</v>

00:24:18.497 --> 00:24:24.657
<v Val Levitan>It is in a way, it is in a way, so create, create an interesting base game.</v>

00:24:18.977 --> 00:24:19.297
<v Michael Gottlieb>Um...</v>

00:24:20.177 --> 00:24:21.617
<v Michael Gottlieb>Yeah, sure it is.</v>

00:24:25.777 --> 00:24:32.417
<v Val Levitan>Have a have a, you know, Progressive or or the party time, as you call it.</v>

00:24:32.017 --> 00:24:32.977
<v Michael Gottlieb>Right, right.</v>

00:24:34.497 --> 00:24:36.417
<v Val Levitan>A, you know, to chase for.</v>

00:24:37.777 --> 00:24:39.857
<v Val Levitan>Or to chase to.</v>

00:24:39.057 --> 00:24:39.537
<v Michael Gottlieb>Mhm.</v>

00:24:40.617 --> 00:25:01.137
<v Michael Gottlieb>And then we've also got free spins. I think it helps round out. I think it's the third leg of the stool is what it is. Because the game, the game as it is now, what I saw was extremely one-dimensional. And the only reason I didn't question it is I thought, oh, well, these are the, this is the market leader. These guys are on fire. What they're doing is working. What they're doing is popular.</v>

00:24:41.537 --> 00:24:42.177
<v Val Levitan>Then.</v>

00:25:02.177 --> 00:25:21.297
<v Michael Gottlieb>If they've got machines making 6 bucks a day, there's no stickiness. It's not sticking. You're out, your low, your mid to lower end. And I got it, dude. I mean, Georgia is nice depending upon where we were, but Felipe and I went to this basically kind of taco shop, right? Perfectly fine taco shop. But it's one of those like,</v>

00:25:07.777 --> 00:25:09.457
<v Val Levitan>No, no.</v>

00:25:21.377 --> 00:25:41.897
<v Michael Gottlieb>Don't talk about it. There's no sign. But if you go up these stairs, there's space on a mezzanine and they've got the machines kind of set up there. It was a little funky. And what I mean by that is the nature of the player that you're getting. You're not getting James Bond. There's not a guy putting on a tuxedo and a woman putting on an evening gown and going out and dining at this establishment.</v>

00:25:42.497 --> 00:25:58.897
<v Michael Gottlieb>right? You've got people buying 15 and $20 taco plates and then maybe taking their five or $10 worth of change, going up the stairs and putting it in the machine and trying to get a little time on device, right? That's your player up there. That's my vibe that I got out of it.</v>

00:25:59.017 --> 00:26:02.257
<v Val Levitan>Yes, but don't forget that if these machines stick.</v>

00:26:03.377 --> 00:26:09.537
<v Val Levitan>If it has legs, the market is really nuts.</v>

00:26:10.017 --> 00:26:10.337
<v Michael Gottlieb>Right.</v>

00:26:10.817 --> 00:26:11.617
<v Val Levitan>Nuts.</v>

00:26:12.977 --> 00:26:15.457
<v Michael Gottlieb>Yeah, the opportunity is limitless, basically.</v>

00:26:15.377 --> 00:26:23.697
<v Val Levitan>It's not regulated. It's A loophole. It's a it was meant for.</v>

00:26:24.897 --> 00:26:34.417
<v Val Levitan>The crane type of amusement devices, they call it Class A amusement devices, to limit.</v>

00:26:35.617 --> 00:26:36.977
<v Val Levitan>The maximum win.</v>

00:26:38.057 --> 00:26:42.817
<v Val Levitan>And at that time, nobody felt that there would be a workaround.</v>

00:26:45.297 --> 00:26:50.257
<v Val Levitan>of that, you know, multiple awards of multiple wins. That's what we're doing here.</v>

00:26:56.737 --> 00:27:04.977
<v Val Levitan>We're kind of, we're kind of linking a chain of single games into a party time.</v>

00:27:12.177 --> 00:27:16.697
<v Val Levitan>The game that you saw, it does not have legs. That's the proverb.</v>

00:27:12.417 --> 00:27:12.817
<v Michael Gottlieb>I am.</v>

00:27:18.097 --> 00:27:21.617
<v Val Levitan>expression and I'm glad that we brought it to light.</v>

00:27:27.377 --> 00:27:34.897
<v Michael Gottlieb>Okay. Well, I mean, in many ways, this is better for us because, you know, we've got some pretty darn good games. And I think Lions Riches.</v>

00:27:36.217 --> 00:27:39.617
<v Michael Gottlieb>I think it'll play better. I know it'll play better, Rafim, because you're going to hit it.</v>

00:27:41.137 --> 00:27:44.897
<v Michael Gottlieb>You'll hit it more often, and that, and that's really what you want.</v>

00:27:46.017 --> 00:28:06.657
<v Michael Gottlieb>Especially if there is no, I mean, the competition isn't the competition. A cabinet making $4 a day is not a cabinet I'm concerned about or interested in. And you saw the art for those games. I mean, they're really bad. And the presentation level is really bad. God love those guys. They're doing the best they can, but they don't have the talent that we do.</v>

00:28:06.817 --> 00:28:07.217
<v Michael Gottlieb>Reply.</v>

00:28:08.257 --> 00:28:29.977
<v Efim Podvoiski>Okay, if you try to do it, there are a lot, a lot of questions that we have to answer. How do we do it? Because $50 is natural cup and you can win more than $50, but it's still $50. Here you, what do I do? You artificially make a win of $10 exactly? Find the combinations that gives always $10 or?</v>

00:28:30.337 --> 00:28:40.097
<v Efim Podvoiski>You like in twelve dollars here, fifteen dollars here, fifteen dollars there, and but then uh how that's up. We we we would have to think about it.</v>

00:28:36.817 --> 00:28:42.097
<v Val Levitan>But why, but why, but why not? I just, I, I...</v>

00:28:43.937 --> 00:28:51.337
<v Val Levitan>I mean, even logically, I don't understand why not. What's the hesitation? Yes, maximum win is $50.</v>

00:28:52.017 --> 00:28:58.617
<v Val Levitan>And maximum debt is whatever, $6, I think, or $6.50. I don't even know where they got $6 from.</v>

00:29:00.897 --> 00:29:03.497
<v Val Levitan>I don't even know why $6. I have no idea.</v>

00:29:04.537 --> 00:29:08.977
<v Val Levitan>but whatever, $5 bet and $50 win.</v>

00:29:10.337 --> 00:29:13.857
<v Val Levitan>Uh, but, but, but why does it have to be this way?</v>

00:29:16.497 --> 00:29:26.977
<v Val Levitan>If we fall within, if our award for what we call, what our definition of a game is, or what we selling as a game,</v>

00:29:28.977 --> 00:29:34.417
<v Val Levitan>The maximum award is $50 and we're saying, yeah, but we will link.</v>

00:29:38.897 --> 00:29:45.537
<v Val Levitan>the start and the end of these games together will link them into a chain. That's what we're saying, right?</v>

00:29:46.577 --> 00:29:49.617
<v Val Levitan>And we're saying this, our interpretation, that this is legal.</v>

00:29:51.297 --> 00:29:56.177
<v Val Levitan>Then why do we need to go with $50 a word on the smaller bed?</v>

00:29:55.177 --> 00:29:56.177
<v Efim Podvoiski>No, I am not saying.</v>

00:29:57.657 --> 00:30:15.937
<v Michael Gottlieb>A theme's logic is the $50 award is a solution to a specific problem. It is utilized to solve a specific issue. And now what we're doing, what's that? The $50 win cap. The $50 win cap.</v>

00:30:10.177 --> 00:30:14.017
<v Val Levitan>Which, which problem? Which problem? Which problem?</v>

00:30:18.577 --> 00:30:27.617
<v Val Levitan>But win win cup meaning maximum win. Why do we have to award maximum win on a minimum bet?</v>

00:30:28.257 --> 00:30:28.857
<v Michael Gottlieb>We don't.</v>

00:30:29.457 --> 00:30:30.897
<v Efim Podvoiski>You don't, yes.</v>

00:30:30.417 --> 00:30:31.097
<v Michael Gottlieb>We don't.</v>

00:30:31.457 --> 00:30:48.257
<v Val Levitan>No, but why would you feel want to stay with that philosophy of awarding $50? Why, why, why not partial? No, maybe I'm maybe I'm misreading what you're saying.</v>

00:30:42.497 --> 00:30:46.017
<v Efim Podvoiski>I'm just saying, I'm just saying that.</v>

00:30:47.937 --> 00:31:06.857
<v Efim Podvoiski>No, no, I am saying two things. Initially I said, and this is my position, but I understand you and I not necessarily dug into my position, that you can have a good game on small bets because</v>

00:31:06.977 --> 00:31:13.617
<v Efim Podvoiski>Dean Cup is not affecting these games and one don't you have just just go and play casino.</v>

00:31:14.897 --> 00:31:19.937
<v Efim Podvoiski>But why do you need this chain? But I do understand that this...</v>

00:31:19.537 --> 00:31:38.217
<v Val Levitan>Sorry, sorry, sorry. Hold on. Because we're discussing philosophy, I am very picky about every single thing that you say. I don't understand what you say, what you said. Why not to go and play in a casino? I don't understand this. Can you elaborate on this? I know that I'm.</v>

00:31:38.417 --> 00:31:41.377
<v Val Levitan>That, that I'm that I'm that I'm leave picking.</v>

00:31:38.817 --> 00:31:53.137
<v Efim Podvoiski>On a small, on a small bets, on the on a small bet we can take a game and put into this machine on twenty-five cents, because $50 is is is not not limiting.</v>

00:31:49.457 --> 00:31:50.497
<v Val Levitan>I, I...</v>

00:31:53.537 --> 00:31:55.057
<v Val Levitan>But that's what I'm suggesting.</v>

00:31:56.497 --> 00:31:59.537
<v Val Levitan>I am in fact suggesting that this should be done.</v>

00:31:56.657 --> 00:31:57.297
<v Efim Podvoiski>But.</v>

00:32:01.057 --> 00:32:06.497
<v Efim Podvoiski>No, that's not, I, now I don't understand what you are saying, because...</v>

00:32:05.697 --> 00:32:20.177
<v Val Levitan>I am saying that, I'm saying that if we don't breach the $50 maximum win, we should use the casino logic, the native casino logic of bet and awards.</v>

00:32:20.417 --> 00:32:23.377
<v Efim Podvoiski>Native logics live without this.</v>

00:32:26.737 --> 00:32:27.697
<v Efim Podvoiski>Elizabeth.</v>

00:32:26.897 --> 00:32:30.017
<v Val Levitan>Yes, yes, the party.</v>

00:32:28.577 --> 00:32:30.177
<v Efim Podvoiski>So, you, so you're saying?</v>

00:32:33.377 --> 00:32:44.337
<v Val Levitan>Yes, that's what I'm saying. The party time only kicks in as a loophole for larger awards. I look at it as two games in one.</v>

00:32:46.097 --> 00:32:59.937
<v Efim Podvoiski>Yeah, me too, actually. But this looks like you proposed something totally different. And it doesn't make sense to me. I just not in that position, but this position doesn't make sense to me.</v>

00:32:59.137 --> 00:33:09.617
<v Val Levitan>I'm not, I'm not a game, I'm not a game designer. I can't propose. I'm not proposing. Don't read, don't read this as a proposal. This is a pure conversation.</v>

00:33:10.457 --> 00:33:17.057
<v Efim Podvoiski>Yeah, proposal in sense, we we all we everybody can get do a proposal. It's not like your proposal is forcing us.</v>

00:33:15.057 --> 00:33:39.657
<v Val Levitan>I am not, I am not on your level. I cannot, my opinion cannot be considered as a design opinion. I'm simply saying that in my view, if I did not have you designing games, and I would be thinking about it myself in a vacuum, I think about it as two games. One is a casino, exactly a casino type of a game.</v>

00:33:39.657 --> 00:33:58.657
<v Val Levitan>game as long as it falls under the maximum award. And another one that, you know, if we now need to award more than 50, then I'm looking at it as a second game, as you call it, party time, which is</v>

00:33:58.737 --> 00:33:59.297
<v Val Levitan>A.</v>

00:34:00.457 --> 00:34:19.697
<v Val Levitan>Chain of various links of assorted wins that are below 50, assorted wins that are below 50, not multiple wins of 50, but assorted wins below 50. So it could be a win of five, five.</v>

00:34:19.777 --> 00:34:22.417
<v Val Levitan>15, 50, and 50.</v>

00:34:23.537 --> 00:34:25.457
<v Val Levitan>And it could be Linkedin to a one win.</v>

00:34:26.097 --> 00:34:36.097
<v Michael Gottlieb>Yes, I don't know that I, I don't know that I think that's adding a level of complexity that is perhaps unnecessary. I see it as a mystery.</v>

00:34:35.537 --> 00:34:39.097
<v Val Levitan>I am not a game designer. I don't know. I have no idea.</v>

00:34:38.257 --> 00:34:59.217
<v Michael Gottlieb>No, we're good. We're good. I think the best way of looking at it is let's look at it like a mystery progressive, but a low-level mystery progressive. And what we'll do a theme is let's just look at the win profile. And instead of just saying, let's just take the casino math straight up, let's look at those higher end multiple of</v>

00:34:59.297 --> 00:35:18.697
<v Michael Gottlieb>that wins and have party time kick in instead of 100% of those wins being derived from the top, you know, the top end of the pay table, or I'm saying like maybe shave off the top end of the pay table a little bit and then push those.</v>

00:35:18.897 --> 00:35:37.777
<v Michael Gottlieb>bigger base game wins out and then use that money to give it back to the player via party time by popping party time at, you know, 10 bucks a pop. But I think that if it's a mystery level, if it's a progressive concept, hitting the same progressive multiple times in a row,</v>

00:35:38.097 --> 00:36:02.257
<v Michael Gottlieb>You don't want the values all over the place. You want them fixed. For when you're in a respective party time session, either all those wins are 10 bucks or all those wins are 20 bucks. There's no reason to, I think you potentially disappoint the player. And you want to train the player that, oh, hey, I go into party time. I got a $10 win. Let's see how many $10 wins I can get or $20 wins I can get.</v>

00:36:02.857 --> 00:36:22.217
<v Michael Gottlieb>We can do this. This is fine. It's just a question of making it a mystery progressive that a low-level mystery progressive hits multiple times and will shave off the top end of the pay table. So instead of the player, you know, winning bigger wins on the high pay symbols, they won't hit those as frequently and the party time will trigger more often.</v>

00:36:23.137 --> 00:36:24.097
<v Michael Gottlieb>If this this.</v>

00:36:23.297 --> 00:36:26.977
<v Val Levitan>I think that, sorry, I thought you're finished. Go ahead.</v>

00:36:25.457 --> 00:36:44.737
<v Michael Gottlieb>But please. No, no. Well, I was just going to say that it's just, it just, it becomes instead of, it becomes 3D chess for a theme mentally, because now you've got, it just introduces a lot more variables and a lot more decisions that we have to make. Not to say that we can't make them, we will.</v>

00:36:45.377 --> 00:37:03.937
<v Michael Gottlieb>But it's not as easy because $50 is a one number and it's a nice multiple number. And to a theme's point, when you're at lower bet levels, it's not all completely linear, right? If you're betting at 25 cents, you have to have a multiple of 25 cents that makes sense. And by the way,</v>

00:37:04.257 --> 00:37:17.857
<v Michael Gottlieb>These wins are base game wins based upon symbol combinations, right? The $50 win is, you know how they turn, you know, those top pay table wins are 50 bucks and they're green, but...</v>

00:37:16.737 --> 00:37:33.937
<v Val Levitan>Yeah. And on this point, just want to just want to throw darts at this point. And at this point, I think that they made another mistake by imitating the bad buttons as they have in Georgia co-op.</v>

00:37:35.057 --> 00:37:56.937
<v Val Levitan>And maybe this was made erroneously to look like it's the same type of a game. But I think that if you want to have five bet buttons, they should be lower bet. They should intentionally start with 25 cents and go maybe to $2.50.</v>

00:37:59.937 --> 00:38:13.137
<v Val Levitan>And so then the win table, yes, but then the win table, you know how you increase your bet and the odds? Paytable doesn't change anymore.</v>

00:38:02.737 --> 00:38:03.217
<v Michael Gottlieb>Right.</v>

00:38:09.297 --> 00:38:10.977
<v Michael Gottlieb>Paytable, right?</v>

00:38:13.377 --> 00:38:13.777
<v Michael Gottlieb>Right.</v>

00:38:14.257 --> 00:38:17.217
<v Val Levitan>Like it, it marks this out, but if you...</v>

00:38:16.097 --> 00:38:16.817
<v Michael Gottlieb>It caps.</v>

00:38:18.257 --> 00:38:25.697
<v Michael Gottlieb>It caps. You're right. Yeah, whether you're so Efim, whether you're 4 bucks a spin or 6 bucks a spin, the top award is green.</v>

00:38:19.377 --> 00:38:22.817
<v Val Levitan>It caps, yeah, if, if.</v>

00:38:23.617 --> 00:38:28.737
<v Efim Podvoiski>Yeah, I, I, I, I have seen it yet, but we will, we will, we will avoid it for sure.</v>

00:38:26.337 --> 00:38:30.577
<v Val Levitan>Isn't it, isn't it, isn't it, isn't it insulting?</v>

00:38:31.297 --> 00:38:31.697
<v Michael Gottlieb>Yes.</v>

00:38:31.537 --> 00:38:33.057
<v Val Levitan>It's insulting.</v>

00:38:33.297 --> 00:38:35.137
<v Michael Gottlieb>It doesn't give you a reason to bet higher.</v>

00:38:33.537 --> 00:38:35.537
<v Efim Podvoiski>We will not do it.</v>

00:38:34.737 --> 00:38:46.817
<v Val Levitan>But if you, but if you keep, but if you keep bet lower, then it will be fine. It will be okay. Like it will get 250 bucks.</v>

00:38:44.417 --> 00:38:44.977
<v Michael Gottlieb>Well...</v>

00:38:48.177 --> 00:38:57.537
<v Michael Gottlieb>The only qualifier to that is you don't want to cripple yourself if you do have people coming in and betting more. You know, if...</v>

00:38:59.617 --> 00:39:19.777
<v Val Levitan>Sorry, so sorry, I sorry that I consider quite knowledgeable. I consider myself to be quite knowledgeable. This is not a casino. This is a street business. And honestly, yeah, there are some locations. There are a few players that are crazy, maybe in Vietnamese or.</v>

00:39:00.857 --> 00:39:01.217
<v Michael Gottlieb>What?</v>

00:39:19.857 --> 00:39:24.417
<v Val Levitan>Chinese locations, yes, maybe, but you know what? I've seen how...</v>

00:39:26.697 --> 00:39:39.937
<v Val Levitan>High rollers deal with it. They occupy two, three machines. And it's another way to show them or to show everybody whose **** is bigger. Excuse me, Lena, I'm sorry.</v>

00:39:41.617 --> 00:39:51.137
<v Val Levitan>You know, they sit like this, they put their feet on the table, they occupy 3 machines, that's mine, don't touch it, and they play, yeah, and they play on it.</v>

00:39:45.297 --> 00:39:45.617
<v Michael Gottlieb>Right.</v>

00:39:51.217 --> 00:39:56.257
<v Michael Gottlieb>They have drinks on both and an ashtray on one. They just take it over. That's true, that's true.</v>

00:39:53.057 --> 00:40:04.777
<v Val Levitan>Yeah, yeah, yeah, yeah. And they demonstrationally, they demonstrate that they are high rollers. So this is street business. I know street business.</v>

00:40:05.377 --> 00:40:11.057
<v Michael Gottlieb>Why did our competitors come out at 6 bucks a spin max bet? Are they stupid?</v>

00:40:05.617 --> 00:40:05.937
<v Efim Podvoiski>AR.</v>

00:40:09.537 --> 00:40:25.857
<v Val Levitan>Okay, okay, okay. For the past 40 years, I've been dealing with the same question. Why do our competitors do something? And how often do we say at the end, well, that was stupid.</v>

00:40:27.777 --> 00:40:31.377
<v Val Levitan>So a lot of smart people do a lot of stupid things.</v>

00:40:27.857 --> 00:40:28.497
<v Efim Podvoiski>I just...</v>

00:40:33.057 --> 00:40:49.457
<v Val Levitan>I don't know why they did it. I cannot explain it. But if I cannot explain it, it doesn't mean that I have to copy it. I mean, in this room right here, there is quite a bit of knowledge of things. If something doesn't make sense, it doesn't make sense. I'm sorry, it doesn't make sense.</v>

00:40:50.497 --> 00:40:51.457
<v Efim Podvoiski>I just want...</v>

00:40:50.897 --> 00:40:57.377
<v Val Levitan>And those odds, when you increase your bets, when those odds cup cup cup out.</v>

00:40:58.257 --> 00:41:02.417
<v Val Levitan>It's freaking insulting. It's insulting and it's stupid.</v>

00:41:02.817 --> 00:41:10.497
<v Michael Gottlieb>It doesn't give you a reason to bet more. That's certainly obvious. Yeah, that's fair. I'll acknowledge that. I felt that too. I felt that too. Efim, you were.</v>

00:41:04.737 --> 00:41:06.977
<v Val Levitan>Yeah, yeah, of course.</v>

00:41:09.777 --> 00:41:12.497
<v Val Levitan>No, but it's insulting. Come on.</v>

00:41:12.177 --> 00:41:15.937
<v Michael Gottlieb>Yeah, that's true. That's true. Efim, you were saying something. Go ahead.</v>

00:41:14.337 --> 00:41:24.337
<v Efim Podvoiski>I just want, I just want to mention that from the data, it's not the freshest data, it's some data from Jacob from a few years ago.</v>

00:41:25.497 --> 00:41:29.457
<v Efim Podvoiski>The bet level, the money-wise.</v>

00:41:30.257 --> 00:41:36.937
<v Efim Podvoiski>Quarter of the beds grow quarter of the money on the beds comes from beds from three to $5.</v>

00:41:40.737 --> 00:41:44.897
<v Efim Podvoiski>28%, 29%, something like this.</v>

00:41:52.097 --> 00:42:02.497
<v Val Levitan>And maybe this is what made them design it this way, but it still doesn't cater to logical.</v>

00:42:05.057 --> 00:42:07.537
<v Val Levitan>Explanation, there's no.</v>

00:42:06.737 --> 00:42:20.657
<v Efim Podvoiski>Yeah, we definitely will avoid capping the Paytable this way or that way. We will avoid it. Or maybe if you want to go to $5, you see a couple of...</v>

00:42:19.937 --> 00:42:23.537
<v Val Levitan>You don't need to go to $5, you don't need to.</v>

00:42:25.457 --> 00:42:26.657
<v Val Levitan>You, you're not.</v>

00:42:28.257 --> 00:42:32.017
<v Val Levitan>This is not a Georgia coam machine. You don't need to.</v>

00:42:31.217 --> 00:42:31.777
<v Efim Podvoiski>Okay.</v>

00:42:34.497 --> 00:42:36.977
<v Val Levitan>You're absolutely fine to have.</v>

00:42:38.097 --> 00:42:43.097
<v Val Levitan>Five bed buttons from 50 cents to $2.50.</v>

00:42:43.937 --> 00:42:46.257
<v Val Levitan>You're fine. You're good. You're good.</v>

00:42:50.257 --> 00:43:05.617
<v Michael Gottlieb>Okay, but there's also the case to be made of the granularity of being able, because what they're doing is they're doing bets in 25 cent increments, starting at 25. So it's like 25, 50, 75, a dollar, a dollar, 25, a dollar 50.</v>

00:43:07.937 --> 00:43:19.297
<v Michael Gottlieb>And that's also what Georgia Coham is doing as well. That's what Aristocrat is doing. That's what IGT is doing, where you just press on the screen up and down arrows for your bet levels. So.</v>

00:43:18.977 --> 00:43:30.497
<v Val Levitan>And by the way, it will deviate the conversation, but I had it in my mind to discuss it with you. I think I steered you the wrong way to do the Aristocrat type of button.</v>

00:43:33.377 --> 00:43:34.417
<v Michael Gottlieb>with the BEP levels.</v>

00:43:33.457 --> 00:43:34.897
<v Val Levitan>I just want to put it out there.</v>

00:43:35.697 --> 00:43:39.377
<v Val Levitan>That I reached the correct type of a bet with the arrows, I think it's a mistake.</v>

00:43:35.777 --> 00:43:36.097
<v Efim Podvoiski>And.</v>

00:43:39.977 --> 00:43:50.537
<v Michael Gottlieb>But that, okay, and I know you said maybe our competitors are idiots, but you know, 50,000 Elvis fans can't be wrong. That's what everybody is doing now. We would be sticking out, we would be taking...</v>

00:43:49.057 --> 00:43:50.377
<v Val Levitan>No, no.</v>

00:43:51.417 --> 00:43:55.777
<v Michael Gottlieb>IGT Aristocrat and Light and Wonder are all doing the bet up and down on the screen.</v>

00:43:51.457 --> 00:43:52.017
<v Val Levitan>No.</v>

00:43:57.857 --> 00:43:58.337
<v Val Levitan>Yeah.</v>

00:43:59.537 --> 00:44:00.017
<v Michael Gottlieb>Okay.</v>

00:44:01.777 --> 00:44:06.017
<v Val Levitan>I think what we're doing is correct, and I steered you the wrong way.</v>

00:44:06.817 --> 00:44:09.217
<v Val Levitan>I think our VDEC is devil.</v>

00:44:12.577 --> 00:44:17.617
<v Efim Podvoiski>I asked Michael why would somebody bet 675 and he had a good answer.</v>

00:44:18.577 --> 00:44:20.337
<v Efim Podvoiski>Remember what you said?</v>

00:44:19.777 --> 00:44:38.017
<v Michael Gottlieb>Right. So, and you experience this, you have to remember, right, you're earning awards. It doesn't go to your credit meter. I put 20 bucks in, I'm earning awards. I now have a fractional number of credits left.</v>

00:44:38.977 --> 00:44:45.257
<v Michael Gottlieb>By giving me the ability to increment or decrement in 25 cent.</v>

00:44:46.417 --> 00:44:53.697
<v Michael Gottlieb>intervals, I can basically set my bet to the amount of money that I have left.</v>

00:44:55.697 --> 00:45:18.617
<v Michael Gottlieb>And I did that a couple of times. Otherwise, you're kind of, I don't want to say you're leaving money on the table, Val, but if somebody, if somebody's betting 2 bucks a spend and they've earned a decent amount of awards and they want to keep playing, but they have $1.75 left, my theory is that the reason they have the bet up and down and that level of granularity is you can set it to $1.75</v>

00:45:19.137 --> 00:45:32.657
<v Michael Gottlieb>and hit spin. More importantly, let's say you don't really win any awards and you're not interested in putting any more money in the freaking machine and you have $1.75 left, being able to set it to $1.75 and hit spin, you're good.</v>

00:45:33.497 --> 00:45:36.577
<v Michael Gottlieb>What are you gonna do? Cash out a dollar seventy-five? It's annoying.</v>

00:45:42.097 --> 00:45:46.417
<v Val Levitan>I don't believe that this is what makes Aristocrat make money.</v>

00:45:46.977 --> 00:46:05.897
<v Michael Gottlieb>No, no, I'm talking specifically about Class A. I'm talking about awards, about the fact that you're accumulating awards and you don't win credits. So all this money goes into the awards bucket. So you can only continue playing if you have credits and if you have a weird number of currency, money left.</v>

00:46:06.017 --> 00:46:07.377
<v Michael Gottlieb>A dollar twenty-five.</v>

00:46:08.897 --> 00:46:18.977
<v Michael Gottlieb>You can choose that you want to bet $1.25 and use up, you know, zero yourself out. Basically bet all of your money and clear yourself out. And I did do that a couple times.</v>

00:46:17.297 --> 00:46:21.377
<v Val Levitan>Ah, yes, yes, yes, yeah, yes.</v>

00:46:21.937 --> 00:46:35.537
<v Michael Gottlieb>You saw that. I think one of your videos showed that, that it was like you got to a point and it's like, oh, I've got a whatever, $1.75 or I've got 75 cents. And 75 cents isn't a dollar, but it's also, you know,</v>

00:46:37.457 --> 00:46:57.137
<v Michael Gottlieb>it allows you to clear out your credit meter, to 0 out your credit meter, because otherwise you're cashing out. And I think you need a certain minimum number to get a gift card, right? There's even a charge for the stupid gift card. So I think they allow that granularity</v>

00:46:57.937 --> 00:47:00.737
<v Michael Gottlieb>To get every last nickel out of the player, bluntly.</v>

00:47:01.897 --> 00:47:21.897
<v Michael Gottlieb>That's what I did. I wasn't going to F around with $1.75. I had $1.75 and I'm like, $2.00, okay, boop, $1.75, boom. I'm either going to win or I'm going to lose. And by the way, let's say you win a little bit and now I have 75 cents. Okay, I'm going to hit 75 cents. Boom. Oh, hey, I've got $2.75.</v>

00:47:22.097 --> 00:47:23.857
<v Michael Gottlieb>Two dollars and seventy-five cents, boom!</v>

00:47:23.257 --> 00:47:27.297
<v Efim Podvoiski>No, no, no, no, don't forget your words don't go.</v>

00:47:24.417 --> 00:47:25.057
<v Val Levitan>So.</v>

00:47:26.417 --> 00:47:31.377
<v Michael Gottlieb>Oh, your awards, awards, that's true, that's true. Awards, it doesn't count. It doesn't count. Blog logic, yeah.</v>

00:47:28.497 --> 00:47:29.057
<v Efim Podvoiski>Yeah, yeah.</v>

00:47:30.017 --> 00:47:44.017
<v Efim Podvoiski>Yeah, arguably, if you have dollar 75, you bet dollar 50 and 25 in three bets and you are gone. But yeah, easier to bet once and makes more sense for the player, yes.</v>

00:47:44.817 --> 00:47:55.617
<v Val Levitan>So for that reason, I would agree. But I don't think that changing it specifically because our machine will be making more money, I don't think so.</v>

00:47:56.737 --> 00:48:16.137
<v Michael Gottlieb>No, I agree. I agree with that point. I'm just talking about the flow, reducing friction. I think it reduces friction. I think it keeps it cleaner. You know, that cash out experience and going to the kiosk was a little bit of a pain in the ***. It didn't even work.</v>

00:47:57.457 --> 00:47:58.097
<v Efim Podvoiski>If it.</v>

00:48:16.377 --> 00:48:37.817
<v Michael Gottlieb>when I was there with Felipe, he had to sit there and type like a 30 digit number into the freaking screen in order to get his gift card or his debit card. And the whole thing was just kind of wonky. And I know that we're going to do it far superior to that, that I'm sure of, but it is, I experienced the, I've got fractional money left</v>

00:48:38.257 --> 00:48:57.697
<v Michael Gottlieb>I want to keep playing. I want to 0 out. And especially, here's the other thing is, let's say I have $20 and that's all I have. All I have is 20 bucks. I've got 20 bucks. I play, I play. Maybe I get some awards. I cash out. I take the awards. I put them back in the machine. I play and play and play. Inevitably, you will lose.</v>

00:48:58.097 --> 00:49:13.937
<v Michael Gottlieb>And when I'm down to $1.75, I'm not going to put any more money in the machine. I can't get a gift card. So let me set it to $1.75 and put me out of my misery. It makes perfect sense. It is logical. It reduces friction.</v>

00:49:13.937 --> 00:49:15.617
<v Val Levitan>That, that part, yes.</v>

00:49:15.857 --> 00:49:37.977
<v Michael Gottlieb>Yeah. And I think, and I think there's set it and forget it. I think people pick a bet level like you were talking about. I think that by having the buttons, it's the piano. I think it invites people to jerk around. It probably reduces velocity of play because what I saw when I saw people playing, whether it was class A or whether it was in the gas stations or whatever else, I saw set it and forget it.</v>

00:49:16.177 --> 00:49:17.137
<v Efim Podvoiski>Yeah, but it's.</v>

00:49:56.337 --> 00:49:56.977
<v Val Levitan>Yes.</v>

00:49:57.537 --> 00:50:14.497
<v Efim Podvoiski>I just, from my perspective, there is a big cost of making all this intermediate bed levels, because math is different and it's not just my work, which is would be good if I could do it and forget, but it's testing</v>

00:50:17.297 --> 00:50:21.537
<v Efim Podvoiski>And having a little bit more complexity of the whole product because of this.</v>

00:50:20.177 --> 00:50:25.337
<v Val Levitan>By intermediate intermediate work, what do you mean by that? I don't understand.</v>

00:50:24.977 --> 00:50:28.257
<v Efim Podvoiski>Intermediate bets, I mean, like if you have...</v>

00:50:27.457 --> 00:50:30.097
<v Val Levitan>What is intermediate? What is intermediate then?</v>

00:50:29.617 --> 00:50:51.057
<v Efim Podvoiski>75 cents, dollar 75 cents. Naturally, you have like five bets, like 25, 50, dollar, two, two and a half, something like this, right? And you have five maths. If you have 25 cents increment, you have 10 maths instead of five, if you max bet to 50.</v>

00:50:51.697 --> 00:50:55.457
<v Val Levitan>Sorry, you're saying you like the 25 cents increment or you like...</v>

00:50:55.697 --> 00:51:14.017
<v Efim Podvoiski>I I I am not talking about like, don't like. I am saying that I have twice as much work for 25 cents increment, and not not just me. We just adding complexity to the system, adding more tests to do more ways to make a mistake.</v>

00:51:15.617 --> 00:51:20.017
<v Val Levitan>I cannot connect. I cannot connect that. I'm sorry. I don't know what she's saying.</v>

00:51:20.337 --> 00:51:22.657
<v Michael Gottlieb>It's more work when you have.</v>

00:51:22.097 --> 00:51:24.977
<v Val Levitan>It's more work to do it which way, they arise the pathway.</v>

00:51:25.297 --> 00:51:25.857
<v Michael Gottlieb>Yes.</v>

00:51:27.537 --> 00:51:29.057
<v Michael Gottlieb>I just posted in the chat.</v>

00:51:29.537 --> 00:51:34.897
<v Val Levitan>But you are advocating the Aristocrat way or the Jvl way? What are you advocating?</v>

00:51:34.097 --> 00:51:54.017
<v Michael Gottlieb>I'm advocating the Aristocrat way. Efim is identifying the fact that doing it the Aristocrat way is just a lot more work and it introduces the possibility of error on the QA side because you've got that many more bet levels that you have to test. It is significantly more bet levels.</v>

00:51:41.457 --> 00:51:42.017
<v Val Levitan>Ssn.</v>

00:51:54.657 --> 00:51:58.457
<v Val Levitan>So, so with that in mind, which way do you want to go?</v>

00:51:54.737 --> 00:51:55.297
<v Michael Gottlieb>That's all.</v>

00:52:00.497 --> 00:52:19.937
<v Michael Gottlieb>Oh, I think we should do it the Aristocrat way, the IGT Aristocrat way. I think that's what everybody's doing in the market. I'm sorry that it's more work, Efim. I, you know, I get it, but I certainly think it's worth doing, especially for Class A. I don't know how we can't do it in Class A. I think we'd put ourselves in harm's way if we don't do it for Class A.</v>

00:52:25.777 --> 00:52:29.537
<v Michael Gottlieb>I think all Efim was pointing out is that it's more work. Is that accurate, Efim?</v>

00:52:30.017 --> 00:52:32.977
<v Efim Podvoiski>Yes, yes, I am not judging.</v>

00:52:34.657 --> 00:52:45.697
<v Efim Podvoiski>I'm just saying that, and you waited it and you said it's, so I trust your vision. Yeah, I understand. I understand and trust. Yeah, I.</v>

00:52:46.817 --> 00:52:50.417
<v Efim Podvoiski>I being lazy would do a different way, but just me being lazy.</v>

00:52:51.577 --> 00:52:52.737
<v Michael Gottlieb>Fortunately, you're not lazy.</v>

00:52:53.377 --> 00:52:58.897
<v Val Levitan>What is the compelling argument here is that set it and forget it.</v>

00:53:01.537 --> 00:53:07.217
<v Val Levitan>And if we wanted to get rid of the V deck and just use buttons.</v>

00:53:08.497 --> 00:53:09.857
<v Val Levitan>That is an advantage.</v>

00:53:13.857 --> 00:53:17.057
<v Michael Gottlieb>And even if we use the VDEC, it's going to look something like this.</v>

00:53:41.617 --> 00:53:43.057
<v Michael Gottlieb>This is the current IGT.</v>

00:53:44.977 --> 00:53:46.577
<v Michael Gottlieb>Honestly, with that, I mean...</v>

00:53:47.697 --> 00:53:57.537
<v Michael Gottlieb>If you were building the cabinet and saying, do we have VDEC or don't, I wouldn't spend the money on it for Class A. I don't know what you get. I don't see any advantage or upside to it.</v>

00:54:01.897 --> 00:54:03.857
<v Michael Gottlieb>And really, with regular Georgia Callan.</v>

00:54:02.977 --> 00:54:06.897
<v Val Levitan>Well, because, because all you need is 1 slam button.</v>

00:54:07.097 --> 00:54:07.697
<v Michael Gottlieb>You got it.</v>

00:54:13.777 --> 00:54:15.777
<v Michael Gottlieb>And a part can't fail that doesn't exist.</v>

00:54:18.097 --> 00:54:26.017
<v Michael Gottlieb>Automobiles got 3000 part, well, automobiles got 3000 parts and Elon Musk came in and a Tesla has 300 parts, 10 times less.</v>

00:54:18.977 --> 00:54:20.657
<v Val Levitan>Hello, yeah.</v>

00:54:25.137 --> 00:54:28.257
<v Val Levitan>Elon, Elon Musk, Elon Musk philosophy.</v>

00:54:29.857 --> 00:54:30.337
<v Michael Gottlieb>Plus.</v>

00:54:29.857 --> 00:54:32.497
<v Val Levitan>Excuse me, I need 3 minutes to use the bathroom.</v>

00:54:32.737 --> 00:54:33.377
<v Michael Gottlieb>Yes, of course.</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

00:57:49.777 --> 00:57:54.177
<v Val Levitan>Okay, so enough said so far on the Class A.</v>

00:57:54.657 --> 00:57:55.937
<v Michael Gottlieb>Yeah, I think that covers it.</v>

00:58:04.617 --> 00:58:11.297
<v Michael Gottlieb>And then I think the just top line, the question Lena and I had is.</v>

00:58:13.857 --> 00:58:24.657
<v Michael Gottlieb>Do we want to start working on, well, let me take a step back. Are we planning on bringing this new curve cabinet to the Georgia show?</v>

00:58:25.617 --> 00:58:35.937
<v Michael Gottlieb>in the fall and is there another software release that should go with that? Basically V43 or C4 V 4?</v>

00:58:37.017 --> 00:58:38.497
<v Michael Gottlieb>Because we've got V3 right now.</v>

00:58:39.657 --> 00:58:40.897
<v Michael Gottlieb>So there's, I've got a...</v>

00:58:40.457 --> 00:58:47.057
<v Val Levitan>No, no, no, no doubts that there will be another Georgia software. It must be.</v>

00:58:47.937 --> 00:59:07.057
<v Michael Gottlieb>Okay, I have it planned. I know right now, I think what the games are going to be. There's a couple of more ambitious products in there, some perceived persistence, which is a space that we need to get into. So there</v>

00:59:06.177 --> 00:59:08.337
<v Val Levitan>I, I am, I am all for it.</v>

00:59:08.577 --> 00:59:08.897
<v Michael Gottlieb>Yeah.</v>

00:59:11.217 --> 00:59:13.457
<v Val Levitan>Yeah, vertical V4.</v>

00:59:14.657 --> 00:59:19.377
<v Val Levitan>Definitely, I'm calling it large format games.</v>

00:59:21.017 --> 00:59:21.377
<v Michael Gottlieb>Okay.</v>

00:59:21.777 --> 00:59:28.897
<v Val Levitan>Similar to what you guys did with Bison, but perceived persistence is absolutely the right way to go.</v>

00:59:29.137 --> 00:59:31.377
<v Michael Gottlieb>Yeah, well, we've got a couple of um...</v>

00:59:33.937 --> 00:59:43.617
<v Michael Gottlieb>couple of new game ideas. We'll have to see timing wise what slots and where. And then you said there was potentially an interest level and maybe doing something in Columbia.</v>

00:59:45.417 --> 00:59:56.937
<v Val Levitan>Yes, I would love to do something in Columbia to renew our Park of Games because we, our contracts expire December 2017, 2027.</v>

00:59:59.737 --> 01:00:04.377
<v Val Levitan>So the entire install base need to be refreshed. I would love to have.</v>

01:00:06.857 --> 01:00:11.257
<v Val Levitan>Bison and wolves brought into that market in class 3.</v>

01:00:12.657 --> 01:00:14.217
<v Val Levitan>And the lions.</v>

01:00:15.977 --> 01:00:16.777
<v Michael Gottlieb>Be updated.</v>

01:00:19.097 --> 01:00:19.577
<v Michael Gottlieb>Okay.</v>

01:00:19.497 --> 01:00:21.337
<v Val Levitan>Yeah, if you could take your...</v>

01:00:22.217 --> 01:00:27.657
<v Val Levitan>Your updated games for Georgia and made them into Class Three.</v>

01:00:29.097 --> 01:00:29.977
<v Michael Gottlieb>For Columbia.</v>

01:00:30.377 --> 01:00:30.857
<v Val Levitan>Yeah.</v>

01:00:32.177 --> 01:00:32.537
<v Michael Gottlieb>Okay.</v>

01:00:38.457 --> 01:00:42.297
<v Michael Gottlieb>Six game pack, 12 game pack.</v>

01:00:43.897 --> 01:00:44.857
<v Michael Gottlieb>Don't know yet.</v>

01:00:45.417 --> 01:00:47.977
<v Val Levitan>Minimum 6, maximum 12.</v>

01:00:49.177 --> 01:00:49.577
<v Michael Gottlieb>Okay.</v>

01:01:02.297 --> 01:01:04.377
<v Val Levitan>Most of the machines horizontal though.</v>

01:01:06.137 --> 01:01:07.177
<v Val Levitan>Dual Screens.</v>

01:01:14.137 --> 01:01:31.257
<v Michael Gottlieb>Would it make sense to potentially do 2 releases and have each release be like 6 lines and waves games, 2 Jackpot Rush games, and two Fiery Ice games? Very similar to what we've done in Georgia, so there's a nice variety.</v>

01:01:33.337 --> 01:01:34.137
<v Michael Gottlieb>Of.</v>

01:01:33.577 --> 01:01:36.457
<v Val Levitan>I don't, I, I don't, I don't know.</v>

01:01:38.377 --> 01:01:41.177
<v Val Levitan>I'm the wrong person to talk to on this.</v>

01:01:41.617 --> 01:02:00.297
<v Michael Gottlieb>No worries, no worries. It doesn't really, in the scheme of things, from the perspective of Lena and I, we'll just come up with a list of games and we'll do the games and they can be released however they're going to be released. The good news is we do have dual screen versions of Jackpot Rush coming. We do have dual screen versions of Fiery Ice product coming.</v>

01:01:42.937 --> 01:01:43.097
<v Val Levitan>You.</v>

01:02:00.697 --> 01:02:02.857
<v Michael Gottlieb>Um, and then, uh...</v>

01:02:02.057 --> 01:02:05.817
<v Val Levitan>Fiery, fiery ice product did not do well in Columbia.</v>

01:02:06.617 --> 01:02:10.937
<v Michael Gottlieb>It never, no, it never went to Columbia, Val. That's never released in Columbia, I think in Diamond Link.</v>

01:02:11.817 --> 01:02:12.937
<v Val Levitan>Not done, yeah.</v>

01:02:12.937 --> 01:02:17.417
<v Michael Gottlieb>Yeah, yeah, Diamond Link, Diamond Link did not do well in Columbia.</v>

01:02:19.337 --> 01:02:26.457
<v Michael Gottlieb>But we can bring Jackpot Rush, we can bring Fiery Ice, and then if I can get some Market.</v>

01:02:27.977 --> 01:02:46.377
<v Michael Gottlieb>sensibilities, some market insight, you know, maybe we can do something more tailored specifically to Columbia in the same way that we did, we did Calle Ocho, you know, for the Cubans. I'm not sure the Colombians are big fans of Cuba one way or another. Maybe Calle Ocho works there, maybe it doesn't.</v>

01:02:46.537 --> 01:03:05.457
<v Michael Gottlieb>It's not even Cuba, it's more Miami, but I don't want to miss the mark, right? I mean, Chinese, Korean are both Asian, but they're drastically different and they don't necessarily care for each other's culture, as we know. So I'd like to...</v>

01:03:05.577 --> 01:03:15.417
<v Michael Gottlieb>All I'm saying is I want to be in alignment with what's cool in Columbia, what's hip in Columbia. I don't know if like Carnival is in Brazil.</v>

01:03:16.937 --> 01:03:25.897
<v Val Levitan>I would suggest having a meeting with Martha, but if you have a set of questions that you want her to answer,</v>

01:03:25.977 --> 01:03:26.377
<v Michael Gottlieb>Yeah.</v>

01:03:27.017 --> 01:03:35.097
<v Val Levitan>She is quite binary, like digital, very structured. So I would...</v>

01:03:30.057 --> 01:03:31.657
<v Michael Gottlieb>Yeah, you mentioned that. Yep.</v>

01:03:36.617 --> 01:03:53.177
<v Val Levitan>Give her a list of questions, have her reply. Give her another list of verification questions. She will go research and she'll reply. Her answer will be factual based on the research. It will not be an opinion.</v>

01:03:54.297 --> 01:03:56.137
<v Val Levitan>She will go to the casino.</v>

01:03:58.937 --> 01:04:00.937
<v Val Levitan>Operators, and...</v>

01:04:02.137 --> 01:04:13.337
<v Val Levitan>Hand them the questions, and they will answer, and she will say, "I've collected replies from 5 casino operators," and this is the factual reply.</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

01:04:19.897 --> 01:04:22.217
<v Michael Gottlieb>Okay, great. So, so cheat.</v>

01:04:23.097 --> 01:04:29.897
<v Michael Gottlieb>Unless she hates music, maybe she listens to music, maybe she can tell me a couple of the popular, you know...</v>

01:04:31.897 --> 01:04:53.257
<v Michael Gottlieb>I mean, I'll get the hard data, but I'm sure she's not a robot. I'm sure she's a human being and I will connect with her on a human level and just kind of get a sense from her as to what's popular down there. What's the best movie she's seen? What's the most popular performing artist? You know, is there a look, a feel, a vibe? And I'll see.</v>

01:04:53.937 --> 01:04:58.217
<v Michael Gottlieb>That's okay. Ah, I'm, well, she's a human being.</v>

01:04:53.977 --> 01:04:54.857
<v Val Levitan>Good luck to you.</v>

01:04:59.977 --> 01:05:04.137
<v Lena Zhukova>Should it be Nova release or?</v>

01:05:03.817 --> 01:05:06.057
<v Val Levitan>Nova, Nova, Nova.</v>

01:05:09.177 --> 01:05:11.977
<v Val Levitan>Norway is very advanced and we're advancing more.</v>

01:05:14.697 --> 01:05:16.857
<v Michael Gottlieb>Do these cabinets have V-decks or no?</v>

01:05:21.017 --> 01:05:26.137
<v Val Levitan>The the the the cabinets in Columbia.</v>

01:05:21.337 --> 01:05:22.137
<v Michael Gottlieb>I'll find out.</v>

01:05:26.217 --> 01:05:26.937
<v Michael Gottlieb>Yes, correct.</v>

01:05:27.417 --> 01:05:28.537
<v Val Levitan>All the decks.</v>

01:05:28.697 --> 01:05:30.217
<v Michael Gottlieb>Oh, I'll be deck, okay.</v>

01:05:40.537 --> 01:05:46.537
<v Michael Gottlieb>Efim, did we do Columbia specific math because their denom is different than American denom?</v>

01:05:45.817 --> 01:05:47.257
<v Efim Podvoiski>No, no.</v>

01:05:47.577 --> 01:05:48.697
<v Michael Gottlieb>Just class 3 math.</v>

01:05:49.257 --> 01:05:50.297
<v Efim Podvoiski>Just questimos.</v>

01:05:50.937 --> 01:05:51.337
<v Michael Gottlieb>Okay.</v>

01:05:57.977 --> 01:06:00.777
<v Michael Gottlieb>Great, okay. Well, I mean, I think that gives us a...</v>

01:06:01.857 --> 01:06:05.017
<v Michael Gottlieb>Our marching orders, Lena, that we know we're doing another.</v>

01:06:06.257 --> 01:06:26.537
<v Michael Gottlieb>another Georgia, they'll be a Georgia V4 release. I've got that blocked out and we know what the, you know, what the titles are. And then I think let's, I'll talk to Martha and we'll determine what we need to bring to Columbia. I got a list, Val, of the.</v>

01:06:26.577 --> 01:06:47.817
<v Michael Gottlieb>top performing games in Columbia. So we've got some data as to as to what's working. What's interesting is pub crawl is actually pretty darn popular, which is not a theme that I think makes any sense. So maybe we can look at like a Rosita's.</v>

01:06:47.937 --> 01:07:04.177
<v Michael Gottlieb>pub or whatever a good, Marta's Cantina, right, whatever's appropriate for the market. Use that same map though and run with it. And they really like these fruit games. The fruit games are super popular down there. So maybe we'll go in and...</v>

01:07:03.337 --> 01:07:05.817
<v Val Levitan>Yeah, used used to be, used to be.</v>

01:07:06.697 --> 01:07:08.217
<v Michael Gottlieb>Okay, how?</v>

01:07:06.897 --> 01:07:13.377
<v Val Levitan>Used to be, I think, I think they they outlive themselves. My personal, this is my personal opinion.</v>

01:07:10.937 --> 01:07:11.337
<v Michael Gottlieb>Okay.</v>

01:07:14.137 --> 01:07:17.817
<v Michael Gottlieb>That's fair. Okay. Efim, how recent is this data?</v>

01:07:19.017 --> 01:07:23.817
<v Efim Podvoiski>I collected from for the last two years.</v>

01:07:24.457 --> 01:07:27.337
<v Michael Gottlieb>Is there any way of looking at like maybe the last six months?</v>

01:07:28.377 --> 01:07:30.377
<v Efim Podvoiski>Okay, well, no problem.</v>

01:07:29.817 --> 01:07:32.697
<v Michael Gottlieb>Just the last six months to see if what...</v>

01:07:31.737 --> 01:07:34.937
<v Efim Podvoiski>Yeah, just afraid it will be a small, too small asset.</v>

01:07:35.257 --> 01:07:36.297
<v Michael Gottlieb>Oh, maybe.</v>

01:07:37.017 --> 01:07:38.537
<v Michael Gottlieb>I, but, but if we, if the...</v>

01:07:37.217 --> 01:07:40.777
<v Efim Podvoiski>OK, no, no, no problem. I'll do it. No problem. Easy.</v>

01:07:39.897 --> 01:07:59.377
<v Michael Gottlieb>Yeah. I mean, all I want to see is have the do the fruit games fall to the bottom of the list? Or do the fruit games kind of still stay up there? Right. But I think we I think we need to offer a little bit of everything as we're doing in other markets. And a number of these games could use some updated art.</v>

01:07:49.297 --> 01:07:50.297
<v Efim Podvoiski>Mhm, mhm.</v>

01:07:59.737 --> 01:08:00.377
<v Michael Gottlieb>For sure.</v>

01:08:01.817 --> 01:08:06.537
<v Michael Gottlieb>So, good. Okay. Well, I think that covers it. Val, do you have anything?</v>

01:08:07.817 --> 01:08:08.857
<v Val Levitan>That's it for me.</v>

[Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]

01:08:29.897 --> 01:08:30.457
<v Michael Gottlieb>Okay.</v>

01:08:32.617 --> 01:08:36.617
<v Michael Gottlieb>Cool. Okay, well, we're good. Atlanta, do you have anything further?</v>

01:08:35.737 --> 01:08:38.857
<v Val Levitan>You guys, you guys enjoy yourselves.</v>

01:08:40.457 --> 01:08:41.657
<v Val Levitan>Have a great weekend.</v>

01:08:42.377 --> 01:08:43.577
<v Efim Podvoiski>Thank you, you too.</v>

01:08:43.817 --> 01:08:44.457
<v Michael Gottlieb>Appreciate it.</v>

01:08:44.777 --> 01:08:45.977
<v Val Levitan>We'll see you next week.</v>

01:08:46.137 --> 01:08:47.097
<v Michael Gottlieb>Yep, take care.</v>

01:08:48.097 --> 01:08:48.857
<v Lena Zhukova>Okay, bye.</v>

