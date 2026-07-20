---
tags:
  - communication
  - misunderstanding
  - game-design
  - val
  - juan
  - technical
---

# Overall Alignment - Transcript

[00:00:03] **Val Levitan**: In some of the emails, maybe I misread it, but I understood that when Yefim tells

[00:00:07] **Juan Martinez**: Sure.

[00:00:12] **Val Levitan**: you that the base payout is, let's say 92%, he in this 92% he included. The progressive payouts. So in effect it was 89 + 3% and he presented it as a base pay.

[00:00:32] **Juan Martinez**: Mhm.

[00:00:32] **Val Levitan**: Let's say, sorry, let me let me rephrase it. It was 88. 5% base plus 1 1/2% progressive for the total of 90% and he called it base pay. And then? In the remote initial setup, we allocated, let's say, another two percentage point or 1 1/2 percentage point to the progressive.

[00:01:01] **Juan Martinez**: Right.

[00:01:03] **Val Levitan**: For the total of 91.5% of the total RTP. Did I read this message correctly?

[00:01:10] **Juan Martinez**: Right. No, he he's trying to say that the the functionality and the awarding of the progressives are part of the game, and hence that's the total expected RTP when he's trying to measure it. Against what the game is actually holding, you know, and I think he was trying to. I don't want to accuse them of anything, but make the situation look not as bad as it was. And no, it's not. What you're saying is, are we applying another progressive contribution on top of something else that's been inserted into the math? And no, I I I don't think that that is at all what's going on.

[00:02:01] **Val Levitan**: But I believe that this is what's going on.

[00:02:05] **Juan Martinez**: Well then that should have been a very easy thing for him to have calculated along with Pavel, and that would be like a core game design mistake. I mean, all of our games have progressives. Why would this particular game? Have an extra 1. 5% or 2% actually added to it. I just don't understand how that could even happen.

[00:02:31] **Val Levitan**: But I believe this is what's happening.

[00:02:34] **Juan Martinez**: OK.

[00:02:38] **Val Levitan**: I also I also want to tell you that. The progressive engine, the progressive engine, to the best of my recollection, was designed by somebody else. Who is I call? I call these people binary programmers. They're not. They're not. They're they're very well educated.

[00:03:07] **Juan Martinez**: Mm.

[00:03:08] **Val Levitan**: This guy is very well educated, but he is somewhat of a a horse with the blinders, you know?

[00:03:16] **Juan Martinez**: Yeah. But you're saying this same person didn't design the progressive that for Diamond Link and Jackpot Rush and and everything else?

[00:03:31] **Val Levitan**: He did, but I believe that we have this mistake across the board.

[00:03:35] **Juan Martinez**: OK, cause I I was also gonna go there, but slightly different because since Fiery Ice Link, a chunk of it is built around Diamond Link that maybe this has been our problem all along. I wasn't even thinking about the progressive because I have. Reduce the progressives on Diamond Link when it was dropping off, but um. Then we need to relook at how we're testing because I I suggested several times, well, can I reduce the progressive contribution rate just to make the impact less? And both Pavel and Efim said, well, if you reduce it by 1% then it's just going to be 1% less. Of the amount, but the problem is still going to be there. So at no point in time did it seem to occur to them that it was progressive on top of progressive.

[00:04:31] **Val Levitan**: They're. I mean, they're much smarter than me. But I I believe that they're wrong.

[00:04:39] **Juan Martinez**: Right. All right, we need to, uh, dig into this differently then.

[00:04:48] **Val Levitan**: But why can't we set up this machine? Set up couple of machines. First of all, a machine with additional progressive set at 0. And then a machine that's set up identical to what you see in the location and play, for example, couple of millions of games.

[00:05:12] **Juan Martinez**: Yeah, well that that's what we're doing right now. I mean the on on the 18th they got the machines mirrored in production. We don't have the one with 0 progressives yet, but there's two machines now. But a theme says it's just difficult to with autoplay to achieve the same. Amount of coin in that the casinos are seeing. That's why it's taking so long. It's not two machine, it's just two machines, not four, and they're just not getting the same amount of play that we're seeing in the casinos. Autoplay runs on the last bet you select, so the team has to stop autoplay, change the bet, you know, go down to 60, go up to Max bet. You know they're trying to simulate the levels that you might have seen in the casino, and that's why it's not continuous autoplay. You know they're not use.

[00:06:12] **Val Levitan**: But do but do we? Do we not have the emulation software? I believe that we can emulate math. Yefim has a math emulator that he can run.

[00:06:27] **Juan Martinez**: I believe that might have been used early on by him, but the fact was, if we're looking for a bug and we don't recreate production, how do we know it's not the one thing they change for the MEI bill acceptor when we fix Gayocho that's causing the problem? I mean, nothing is too remote at. This point in time, Val.

[00:06:50] **Val Levitan**: No, it's not. I'm not insinuating that we should test something else, but I do believe that if we test with an

[00:06:59] **Juan Martinez**: Mm.

[00:06:59] **Val Levitan**: emulator in particularly running. Progressive set at 0. That the problem will not manifest itself, so I would leave the machines running on autoplay as is. Although at a slow rate, but I would also, in addition to it, run my hypothesis through an emulator and just get a quick look at the data through

[00:07:23] **Juan Martinez**: Sure.

[00:07:29] **Val Levitan**: an emulator.

[00:07:31] **Juan Martinez**: Sure.

[00:07:31] **Val Levitan**: Because I just think that we're getting confused in what is the base percentage versus. What they interpret as base game because now they packaging the game and the progressive into a base play. If you know what I'm saying, I mean, maybe I'm not.

[00:07:55] **Juan Martinez**: OK. I know, I yeah, I know what you're saying. Hmm.

[00:08:04] **Val Levitan**: I mean, I cannot guarantee that this is the case, but.

[00:08:08] **Juan Martinez**: Sure. Well, and then just to it's we're not getting unusual amounts, but the frequency of amounts. So if we sent 0% to the meter, then the top award would be 10,000, the second level would be 500 and they would never increment. But that second level, that's 500 is still paying out more than it should. It's just under your scenario, it's going to be 500 and then 500 and then 500 and then 500 versus now it's 510 cents and then it grows to $520 and hits and then it's at. $600 in hits. It's the number of occurrences and not necessarily the dollar amount that's causing the problem, but we should still test it.

[00:08:56] **Val Levitan**: Well. Well, number of occurrences, number of occurrences, but eventually results in the amount too, right where we're overpaid.

[00:09:07] **Juan Martinez**: Of course, yes, yeah. But just so you understand, we'd still be overpaying if the 500 is only supposed to hit on average once a month based on our coin in and it hits three times at 500. That's still overpaying, it's just at a at a lower amount. Than with the progressive contributions added to it. You know, it's the number of times that these awards are happening.

[00:09:39] **Val Levitan**: But they're happening at 500. That means there is no progressive contribution. That's what you're saying.

[00:09:46] **Juan Martinez**: No, no, no. They're have that 500 is the base reset for the major. They've happened at, you know, the the progressive has incremented and it's hit. And just that it's hit more than it should have based on the number of games played and coin in that a theme calculated for.

[00:10:11] **Val Levitan**: Because I believe that the progressive portion of the design was relegated to somebody else, not Yafim. And the mistake probably is in there. Again, I'm not, you know, I stayed out of it for a very long time, but I'm seeing that it's not getting resolved. That's why I'm getting involved.

[00:10:42] **Juan Martinez**: Sure. No, I I agree. It's definitely not. We're not necessarily any closer other than a theme openly admitting that there is an overpayment issue. He he's not can't say why, but it is there and and visible in all the data.

[00:10:58] **Val Levitan**: Would you like me to invite Yifim to this and ask him if that could be an issue?

[00:11:03] **Juan Martinez**: Sure, I think he's out of the office on vacation, but absolutely.

[00:11:09] **Val Levitan**: Oh, I wasn't aware that he is on vacation.

[00:11:12] **Juan Martinez**: Yeah, I think he he was burning himself out and I think he took off for two days if I'm not mistaken.

[00:11:18] **Val Levitan**: But he's usually available anyway.

[00:11:21] **Juan Martinez**: OK.

[00:12:00] **Val Levitan**: Yeah, he's out of the office, but let's see if he's going to reply. OK. OK, bring me up to speed on. On the Florida kids. Oh, here's your second.

[00:12:25] **Juan Martinez**: Um.

[00:13:30] **Val Levitan**: Yeah, he's gonna join now.

[00:13:32] **Juan Martinez**: OK.

[00:13:58] **Val Levitan**: Does it mean that we burnt the Kaya Orcher game?

[00:14:03] **Juan Martinez**: No, I mean, surprisingly, I mean the customers are aware that

[00:14:04] **Val Levitan**: No.

[00:14:09] **Juan Martinez**: something is off, but not anything that's alarming them yet. And from the player perspective, these people have hit several majors, so. I'm surprised more money hasn't gone into the games. So no, I I still think that we have not burned the games at all. You're muted if you can hear me. There you go.

[00:14:43] **Efim Podvoiski**: Hello.

[00:14:44] **Val Levitan**: How you feel?

[00:14:46] **Efim Podvoiski**: Hi. Yes.

[00:14:48] **Val Levitan**: OK, so here's the question in terms of how we calculate math. And by no means neither myself nor one are mathematicians, but I just have a logical question. So I read in one of the messages that. You calculate based base math including the progressive or a portion of progressive or the full progressive, but do I understand it correctly when we set up the remote initial set up? We in within the remote initial setup, we set up progressive separately, so could.

[00:15:32] **Efim Podvoiski**: We set up, we set up progress for increments separately. There is portion when you win the progressive, you win always win basically the base plus increment, you win increments that you accumulated during the time.

[00:15:48] **Val Levitan**: OK. So could it, could it, so could it be, could it be that when we set up?

[00:15:49] **Efim Podvoiski**: But then you're.

[00:15:54] **Val Levitan**: That increment. Within the RIS, we actually set it up in a way that it calculates the the not the increment, but the base and the increment.

[00:16:09] **Efim Podvoiski**: The answer is no. And the and the 2nd and yes, we checked that we paid exactly the increments that we should pay.

[00:16:23] **Juan Martinez**: I I guess this.

[00:16:24] **Val Levitan**: Which how? How could we do that? Because we're not paying the exact increment, we actually pay much more.

[00:16:30] **Efim Podvoiski**: Why? Why? What do you mean? Why? Why you saying?

[00:16:35] **Juan Martinez**: No, but yeah, that'll work. Yeah. Just to confirm, Val, the progressive increment is growing at

[00:16:38] **Efim Podvoiski**: By yourself.

[00:16:42] **Juan Martinez**: the proper amount if you insert a.

[00:16:44] **Val Levitan**: No, no, no, no, no. It's growing at the right amount, but we keep on paying it more frequently.

[00:16:52] **Efim Podvoiski**: Yes. So we are playing more progressive in this sense, but it's not. It has nothing to do with sessions on the progressive controller.

[00:16:59] **Val Levitan**: But what? What action says the progressive is ready

[00:17:03] **Efim Podvoiski**: OK.

[00:17:05] **Val Levitan**: for payout? It's the progressive controller that can.

[00:17:10] **Efim Podvoiski**: It's it's it's it's no, it's in game. It's in game progressive. The event in the game triggers a progressive.

[00:17:20] **Val Levitan**: But you didn't design that progressive controller, did you?

[00:17:24] **Efim Podvoiski**: But it has nothing to do with this frequency of playing progressive. Progressive controller has nothing to do with this and this progressive. It's in game progressive.

[00:17:34] **Val Levitan**: But we we don't know that. We it's. I mean, it's supposed to work as you describe,

[00:17:38] **Efim Podvoiski**: Uh.

[00:17:42] **Val Levitan**: but what if it doesn't work the way you described? You didn't.

[00:17:45] **Efim Podvoiski**: If it doesn't work, if it doesn't work, in addition, the game should should somehow play progressive and it does not expect to play progressive and it probably it wouldn't do it and just doesn't know how to do it.

[00:18:00] **Val Levitan**: But you don't know how it's programmed.

[00:18:05] **Efim Podvoiski**: OK, well, I I agree that everything is possible, but it's something very, very stretched. I I.

[00:18:12] **Val Levitan**: I know, but you, but you, but you're checking everything, everything that comes to mind. You're questioning everything that comes to mind.

[00:18:23] **Efim Podvoiski**: Yeah, OK, I agree. OK, but yeah, OK, but OK, so people who know how progressive works should double check that they it's impossible or to generate progressive.

[00:18:35] **Val Levitan**: Well, why don't we? Why? Why don't we before we go to those people and before we question the code, why don't we do a practical experiment? Why don't we set up two machines? That play on the on your emulator. You have a math emulator, right? So 11.

[00:19:00] **Efim Podvoiski**: What do you mean? What do you mean I have a mass in America?

[00:19:05] **Val Levitan**: Well, you have an emulator that could play many games quickly, right?

[00:19:09] **Efim Podvoiski**: It just runs my my mass engine. It's doesn't, doesn't, it cannot communicate to progressive controller or something. And even if it could, it would have nothing to do with the codes that actually on the machine, so it wouldn't help us.

[00:19:26] **Val Levitan**: So when, so when you run your emulator on the machine without the controller, your math is good. Your you check out your math well, right? That's.

[00:19:37] **Efim Podvoiski**: Yes, yes, yes, yes.

[00:19:38] **Val Levitan**: It works, but when it when it connects to a controller, somehow it doesn't work.

[00:19:46] **Efim Podvoiski**: We don't see it in our tests yet.

[00:19:50] **Val Levitan**: Well, it I mean, we run just.

[00:19:54] **Efim Podvoiski**: Yeah, I.

[00:19:54] **Val Levitan**: We we don't test. But I suggest is there a way to? Is there a way to set up a, let's say,

[00:19:57] **Efim Podvoiski**: Did you?

[00:20:02] **Val Levitan**: progressive controller? Or set up the machines without the progressive controller and then maybe set up a controller to a 0 contribution. And then set up a third stack of machines that have progressive controller as intended.

[00:20:25] **Efim Podvoiski**: Sorry, what's the first one you said one with 01

[00:20:28] **Val Levitan**: I'm just.

[00:20:29] **Efim Podvoiski**: or one proper and one?

[00:20:30] **Val Levitan**: I'm just, I'm just thinking out loud. I'm saying maybe one with controller set at zero, one with the controller set at the percentage as we install it exactly emulating our installation. And the third one with no controller at all, just a game running a single game, single machine.

[00:20:55] **Efim Podvoiski**: It will. It will not single mushroom progressive on a single mushroom, OK. OK. I just don't see how it can possibly do something and also our progressive controller is used in many places, so it's not like it's a.

[00:21:14] **Val Levitan**: But our machines never make any money. Our machines don't make money and they always overpay. We just never paid attention to it. But it has been my complaint in Colombia, in Peru, the machines overpay.

[00:21:28] **Efim Podvoiski**: I I I never heard about this. I never heard that much. All this,

[00:21:30] **Val Levitan**: Sure.

[00:21:32] **Efim Podvoiski**: all this work, but I never. Sorry, I I never. I never heard about this confirmed with data.

[00:21:39] **Val Levitan**: OK.

[00:21:40] **Efim Podvoiski**: I always see complaints from single locations. They say machine over play. Uh huh. You complain the machine over play, but you never complain the machine under the machine under play.

[00:21:52] **Val Levitan**: Yeah, you feel, I think, I think very often we don't see forest from the trees. You know, we're too, we're too close to, we're hugging the trees now where we're too close to the forest, we don't see it. So let's just remove absolutely all of the emotions, because I get very angry when people say that my machines are not good, so I try to remove myself from any emotions. So let's just start splitting and finding the problem in in in dissecting, in dividing it into different stages. So my question to you, I would like to find a way to separate your math from the controller math. What can you? What can you suggest from a practical perspective?

[00:22:52] **Efim Podvoiski**: OK, if you want, if you want to test this, OK, then we have to set up machines with as a single machine progressive, yes.

[00:23:02] **Val Levitan**: As a single machine, progressive with 0 contribution, right? The progressive.

[00:23:06] **Efim Podvoiski**: ohh OK with 0 contribution.

[00:23:10] **Val Levitan**: Yes, let's do that.

[00:23:12] **Efim Podvoiski**: OK. OK, we have much chance to set. Yes, OK.

[00:23:20] **Val Levitan**: So is there any way we could accelerate the play? Is there? And like, does Irina have this? Irina told me that she has a math. What do you call it? Tester.

[00:23:31] **Efim Podvoiski**: Mass test, mass test, but mass test ignores everything else that happens to the machine and just calls the mass basically and the door and we know that this mass test produced a good result so.

[00:23:43] **Val Levitan**: On it. So that's a single machine, right?

[00:23:46] **Efim Podvoiski**: It's a simple machine. Mm.

[00:23:49] **Val Levitan**: So, so that's so and produces the right result.

[00:23:54] **Efim Podvoiski**: Yes.

[00:23:55] **Val Levitan**: But when you when you connect the machine to the progressive, it doesn't produce the result.

[00:24:01] **Efim Podvoiski**: I honestly, well, I don't believe it. I don't believe that this is this is the

[00:24:06] **Val Levitan**: If you right now is not important what you believe it it also it doesn't.

[00:24:07] **Efim Podvoiski**: problem. OK.

[00:24:11] **Val Levitan**: It's not even important what any of us believe. It makes no difference what I believe or you believe or what one believes.

[00:24:19] **Efim Podvoiski**: Yeah, but what? OK, but what I'm saying is you cannot connect mass test of progressive controller and try to and hope to see something. It's it's it's OK if you have infinite resources, we can do this test also. But I it's it's very stretching. It's very, very stretching that we can possibly find something there.

[00:24:46] **Val Levitan**: If you all all the low hanging fruits were already tested and didn't yield in

[00:24:46] **Efim Podvoiski**: It's uh.

[00:24:53] **Val Levitan**: any results, so as you call it the stretching. Stretching it too far. Maybe it's not too far, but.

[00:25:01] **Efim Podvoiski**: Yeah, but no, no, no. When you are saying, sorry, when you are saying that you want to test, when you want to test the machine with progressive controller, this without progressive controller, I understand what you're saying and I understand that even if I don't like it, I cannot argue it. It's it makes sense. But then if you want to connect masters to progressive controller, I believe. OK, first of all, we cannot do it regularly. But second of all, OK, OK, OK, I will not argue, OK. It will be relatively fast, we will get negative result and go forward. OK, but I'm not sure that we can do it, if we can connect mass test and progressive controller.

[00:25:53] **Val Levitan**: Why don't we write a specific test like a math test that that pushes the machine to play faster, that we could play a couple of million games an hour?

[00:26:06] **Efim Podvoiski**: No, we have much test. Yes, yes, yes we have much test, but it's done in certain. It's assumed certain conditions. I I'm not sure if that it really can connect to progressive control.

[00:26:18] **Val Levitan**: Well, can we change the logic of the condition?

[00:26:18] **Efim Podvoiski**: Sure. I think it's possible, yes. But it has to be done. Somebody has to do it. Anton, maybe.

[00:26:27] **Val Levitan**: Well, OK. I mean, we have no, we have no choice, but we need to mobilize our people, write an emulator, proper emulator, or to adopt your math test with proper hookups. Can you direct the person? Can you tell the person what what we need to test? Because I, you know, I'm not capable of. I'm not capable of directing people.

[00:27:02] **Efim Podvoiski**: OK, I'll try to explain to to Anton what what what is suspected, but here it will take some time to understand how the math test work and how to do it. It will take time to to to to prepare for this test.

[00:27:17] **Val Levitan**: We're talking about time, we're talking about a week or we're talking about hours.

[00:27:23] **Efim Podvoiski**: It's 20 days. I guess this the.

[00:27:29] **Val Levitan**: I'm OK with this. We have no choice. We got to fix this thing. We got, we got to find the source, not even fix. We really have to point inequivocally without any doubt that we found a problem, because there is a problem. And when we find that we are going to be making money, so there is a problem. We're not looking at something. There is a problem. So let's just. But let's just Anton is a clever, clever kid. I like him. He's a he's a clever guy and he thinks outside the box.

[00:28:07] **Efim Podvoiski**: Yeah.

[00:28:09] **Val Levitan**: Let's let's bring him in. Let's give him this task. Create an emulator that simulates player's condition and test the controller and the machine and the machine and the controller.

[00:28:23] **Efim Podvoiski**: No, I'm sorry. When you say simulates player condition, it scares me because I don't know how to simulate player condition. We are talking about, we are talking about running mass test

[00:28:31] **Val Levitan**: That's not that's.

[00:28:35] **Efim Podvoiski**: and this progressive controller. That's what, that's how to understand it,

[00:28:37] **Val Levitan**: Oh.

[00:28:39] **Efim Podvoiski**: right?

[00:28:40] **Val Levitan**: Well, almost right. But instead of, let's say, having fixed beds, fluctuate beds, let's say.

[00:28:49] **Efim Podvoiski**: Okay, so it's another story. This is something else that needs to be added. Okay, ok it makes sense, right? Right It makes sense to test it. Yes, Yes but if he will have to make change in bets, it's OK, I don't know how much time it will take, but we are talking about this and tonight I will e-mail Tonton.

[00:29:16] **Val Levitan**: OK. Fantastic. Fantastic. I'm very happy that we had this conversation. OK. Thank you, Yifim. I appreciate it. Sorry to disturb you on your vacation. Where are you in Vancouver?

[00:29:27] **Efim Podvoiski**: No, no, I am in. But I'm with kids. I'm in Phenolon Falls, Phenolon Falls, actually in in Ontario, in Ontario and Cabarta.

[00:29:35] **Val Levitan**: OK, I don't know where it is, but. Oh, OK, OK, alright. Enjoy your you with your kids or

[00:29:40] **Efim Podvoiski**: OK.

[00:29:44] **Val Levitan**: grandkids.

[00:29:45] **Efim Podvoiski**: Yeah, this everybody.

[00:29:46] **Val Levitan**: Oh, OK. OK. Enjoy. Enjoy. Enjoy. Sorry to disturb you. Thank you. Bye.

[00:29:46] **Juan Martinez**: Oh, nice.

[00:29:49] **Efim Podvoiski**: OK. Thank you. OK, thank you. Bye.

[00:29:51] **Juan Martinez**: Thanks, Sakhim.

[00:29:53] **Efim Podvoiski**: Bye.

[00:29:56] **Val Levitan**: OK, so one, if you will write the spec, let's just stay on top of it. And I think that's let's let's just do the right thing. Let's do the right test.

[00:30:08] **Juan Martinez**: Absolutely.

[00:30:11] **Val Levitan**: OK. Can you update me on the kids please?

[00:30:15] **Juan Martinez**: Sadly, I I have no update, Val. They we reached out to them as late as last Friday afternoon. They're supposed to get back to us this week and they haven't. I mean, at this point, I believe that they're stalling. I even spoke to Alex last Tuesday. And he promised he would get me an update this week, but we don't ever seem to get an update from those guys. The machines were working. Sebastian got all of that resolved with their last issue, and I asked him yesterday to follow up, so I might get something from them today. I'll try myself again, but you know that when they switched from, oh, we don't want to lease anymore, we only want to sell. I found that statement to be odd from them. You know, when did all of these locations all of a sudden have money that they just want to buy and not lease? I thought that was very odd statement from Alex, so I'm not really sure. What's going on with those guys?

[00:31:12] **Val Levitan**: OK. OK. Interesting. So we don't know whether the machines are out in locations or not.

[00:31:23] **Juan Martinez**: No, as of last Friday, they were not out. The technician told Sebastian and they copied me that he was going to speak to his boss about Duke getting them out this week, but we've got no further updates from them.

[00:31:39] **Val Levitan**: That's so weird, French.

[00:31:42] **Juan Martinez**: Yes.

[00:31:45] **Val Levitan**: Why? Why do you think that is like what? What's on your mind?

[00:31:47] **Juan Martinez**: I I don't know. I I really, I don't know. I mean, I've known Alex for ages. I I don't know. I mean, I I'm gonna give him a call now just an off the record to say, hey, if there's something here I don't know about, please tell me. You know, 'cause we're just spinning our wheels right now.

[00:32:07] **Val Levitan**: Yeah, maybe not now. Maybe you should take him out for a meal or somewhere.

[00:32:11] **Juan Martinez**: Yeah, yeah, good idea.

[00:32:12] **Val Levitan**: Just maybe a glass of wine.

[00:32:14] **Juan Martinez**: Yeah.

[00:32:17] **Val Levitan**: OK. And how is Javier? Is he giving up on us? Frustrated?

[00:32:23] **Juan Martinez**: No, no. I mean, he did say, hey, something's wrong with the math, but he he knows we're working on it. He knows we'll fix it because we usually fix everything else that has ever surfaced. So he's he's being patient with us.

[00:32:40] **Val Levitan**: OK. Last question, organizational. So I'm still trying to secure the office

[00:32:48] **Juan Martinez**: Yes.

[00:32:51] **Val Levitan**: for us in the White White Tower.

[00:32:53] **Juan Martinez**: OK. Yes.

[00:32:56] **Val Levitan**: But while I'm trying to secure the lease and supposedly they're working on it with their lawyers, I I mean, I don't understand what's. What is taking them so long? But let's park it for a second.

[00:33:13] **Juan Martinez**: Mhm.

[00:33:15] **Val Levitan**: You know where White Tower is located, right?

[00:33:16] **Juan Martinez**: Good. You told me that it was just close by, but I don't actually know.

[00:33:22] **Val Levitan**: White White Tower. I'll tell you exactly where it is.

[00:33:22] **Juan Martinez**: I can look it up right now.

[00:33:26] **Val Levitan**: It's right across the Gulfstream racetrack, right across Biscayne.

[00:33:31] **Juan Martinez**: Oh. OK.

[00:33:34] **Val Levitan**: Literally, literally across, directly across. On Biscayne. So you you know where it is, right?

[00:33:41] **Juan Martinez**: Yeah, I know that generally. Absolutely, absolutely.

[00:33:45] **Val Levitan**: OK, so pretend that this is the racetrack location on Biscayne off of Biscayne.

[00:33:49] **Juan Martinez**: Sure.

[00:34:06] **Val Levitan**: So while I was trying to secure while I'm trying to secure the lease.

[00:34:11] **Juan Martinez**: Mhm.

[00:34:12] **Val Levitan**: I somebody approached me to buy a building. But the building is located further South, much further South. So exact location of the building is 85071st, sorry 850 NW 71st.

[00:34:40] **Juan Martinez**: 7 weeks.

[00:34:40] **Val Levitan**: That's the exact location.

[00:34:43] **Juan Martinez**: There's Ave. in Hollywood or 71st St. in Miami.

[00:34:47] **Val Levitan**: Miami.

[00:34:51] **Juan Martinez**: Oh, wow.

[00:34:52] **Val Levitan**: So it's it's off of 95.

[00:34:56] **Juan Martinez**: Yes.

[00:34:57] **Val Levitan**: I think it's 2 streets over off of 95 or 4th streets or something like this.

[00:35:02] **Juan Martinez**: Yeah, yeah, yeah, I see it.

[00:35:07] **Val Levitan**: And so the building by by itself, it's just a good real estate purchase, which I'm going for, but aside from it, I think it's and it's not too close for me at all. So I'm a little bit hesitating, but I think that we can bring everything

[00:35:22] **Juan Martinez**: Sure.

[00:35:27] **Val Levitan**: together, even a small part of manufacturing that we could actually produce for ourselves in Miami.

[00:35:35] **Juan Martinez**: Sure.

[00:35:37] **Val Levitan**: My question is, if I secure an office for us there, are you going to be traveling that far? It will be in the morning. It's close to 45 minutes for you, maybe. Maybe close to an hour.

[00:35:55] **Juan Martinez**: Yeah, Val. I mean, I will do whatever's needed. Yeah, it it's, it's 45 minutes like right now. But yeah, it's not, it's no different than driving down to Hialeah Casino. So it's not necessarily the end of the world. I might need to shift my hours a little bit. Or, you know, not necessarily going every single day of the week. But yeah, that's not, you know, as you know, everything in South Florida is 35 minutes anyway, so another 10 minutes isn't gonna kill me.

[00:36:28] **Val Levitan**: Yeah, I'm in Florida. It's just crazy. Everywhere's crazy, no matter where you.

[00:36:32] **Juan Martinez**: Yeah.

[00:36:36] **Val Levitan**: Yeah, I guess I guess hypothetically you could

[00:36:39] **Juan Martinez**: Um, that was.

[00:36:40] **Val Levitan**: start from let's say 7, finish at 3:00 and beat the traffic both

[00:36:45] **Juan Martinez**: The.

[00:36:46] **Val Levitan**: ways.

[00:36:48] **Juan Martinez**: Sure. Sure.

[00:36:51] **Val Levitan**: OK, let's see where we'll end up.

[00:36:53] **Juan Martinez**: OK. Now on that note, Sebastian, do you think you're going to need access to our storage unit where we have your monitor and some of the other things from the office before we get back? From South Dakota.

[00:37:12] **Val Levitan**: And when? When do you get back from South Dakota?

[00:37:14] **Juan Martinez**: I I brought one way tickets Val, because I don't know yet. I'm trying to immediately install the games all right away, but as you know it's it's subject to the customer. They've got to install their locks. We have to drive 6 hours every day to get back and forth, so. It's probably gonna take us another 10 days after the training, so it could be, you know, I want to get back no later than August 20th. Um.

[00:37:43] **Val Levitan**: Yeah, I will not need anything until September.

[00:37:47] **Juan Martinez**: OK. OK. So we'll be fine then.

[00:37:51] **Val Levitan**: OK, what? What is your? What are your thoughts on Dennis?

[00:37:54] **Juan Martinez**: OK.

[00:37:57] **Val Levitan**: Any any thoughts?

[00:37:57] **Juan Martinez**: So far, so good. I mean, he just, you know, sometimes goes on and on. And you know, you asked me why I don't offload some stuff to him because, you know, just sometimes he comes up with these crazy things and I'm like, where is your mind today, Dennis, you know? We had a call scheduled. He changed the time. I needed to go over some stuff with him on the computer, and he calls me from the parking lot of Home Depot. Oh yeah, I had to get a folding table for the office, so I'm not at my computer. I'm like, Dennis, I specifically needed you to see my screen. That's why. But he'll be fine, Val. I mean, it's he's perfect for that market.

[00:38:37] **Val Levitan**: I think so too. Where with all the quirks, I think it works for the market.

[00:38:39] **Juan Martinez**: Yeah. Absolutely, absolutely.

[00:38:42] **Val Levitan**: So speaking, speaking about the market, do you have anybody for Texas market?

[00:38:47] **Juan Martinez**: You know, it's funny, I I would you ever consider because I saw a LinkedIn post the other day. Would you ever be interested in Andres coming back, someone that at least we know and now has had some sales under his belt? I'm hearing from others that that company. Former Rocket Class 2 may not be on on good standing. Other than that it would. I would need to lean on other people that are industry people that probably have expectations. Car allowances, 401 KS, you know, a lot of that heavy stuff that I don't know if we may or may not be able to negotiate. But I can certainly start pulling some feelers out there.

[00:39:37] **Val Levitan**: But what did you see Andres is looking for a job?

[00:39:41] **Juan Martinez**: No, no, no. That I just Ares is hurting. I saw his name on LinkedIn that he was up in New York and it just made me think of him. Then someone else happened to tell me that that company he's with might be hurting a bit and may not last too much longer in the future. I haven't said anything to him, obviously, or talked to him, but that, you know, it popped up. I wonder if he'd be interested in Texas.

[00:40:11] **Val Levitan**: Interesting. No, it wouldn't wouldn't be my first choice.

[00:40:17] **Juan Martinez**: Or do you want me to actively just collect some names of people and get a sense of what what they it would be like people who handled the Oklahoma market because it's so close by. That's who I'd tap into because they probably are used to flying in and out of Dallas or Houston to get wherever they're going. In Oklahoma.

[00:40:40] **Val Levitan**: Oklahoma is just a very specific market, like it's beyond specific. I mean, Texas is not Oklahoma.

[00:40:49] **Juan Martinez**: Oh, absolutely not.

[00:40:50] **Val Levitan**: There's much more sophistication than Texas.

[00:40:53] **Juan Martinez**: In Texas, you think no, these are. I would disagree.

[00:40:56] **Val Levitan**: No, versus Oklahoma, I'm just saying Oklahoma is, which is very simple market.

[00:41:01] **Juan Martinez**: Yeah.

[00:41:02] **Val Levitan**: Although, listen, I've never worked in Texas myself, so I don't know.

[00:41:06] **Juan Martinez**: Sure. Well, I mean, let me do we re spin this? I mean, I think that we're going to get in early in Texas. It's still wide open. Do we necessarily need someone that truly has gaming experience more so than somebody who's just a good salesperson? A right personality, you know.

[00:41:27] **Val Levitan**: I think it's the right personality. We're looking for the right personality and actually I'm not looking for a specific sales person.

[00:41:35] **Juan Martinez**: Yeah, sure.

[00:41:36] **Val Levitan**: I think I'm looking for a relationship individual and don't forget that we are.

[00:41:38] **Juan Martinez**: OK.

[00:41:43] **Val Levitan**: We we will walk into the market with two different products. We have gaming product, we have transactional products. I don't know whether it should be one person,

[00:41:52] **Juan Martinez**: Sure.

[00:41:55] **Val Levitan**: but surely would help at least in the beginning to have one person.

[00:42:00] **Juan Martinez**: Of course, of course. And Val, just so you know, I I'm certainly not opposed until we figure Texas out about me going to Texas and doing some hustling in in the first however long it takes. So just so you know.

[00:42:13] **Val Levitan**: And same for me too, by the way. I will go there myself as well.

[00:42:16] **Juan Martinez**: Sure.

[00:42:18] **Val Levitan**: So I the the the reason I'm not jumping at anybody is because I am ready to go there myself as well.

[00:42:26] **Juan Martinez**: Perfect.

[00:42:26] **Val Levitan**: I I mean, I don't, I I don't mind working or going into locations that I I never did and I'm OK with that. But thank you.

[00:42:34] **Juan Martinez**: Yeah.

[00:42:34] **Val Levitan**: It's good to know that you're also available. That's nice. OK, let's let's continue thinking.

[00:42:54] **Juan Martinez**: OK. OK, yeah, absolutely. And I, I, I, I have some pictures from San Antonio, TX. Nothing just to just to show you. I'll share those with you and Michael here shortly from Texas and I will keep you posted on what Lonnie. Uh has to say with today's reinstallation of software.

[00:43:15] **Val Levitan**: Yeah, speaking about Michael, where are we with the design of? Oh.

[00:43:25] **Juan Martinez**: Lone Star.

[00:43:25] **Val Levitan**: Nebraska, Nebraska and the Gold Star both.

[00:43:30] **Juan Martinez**: Yeah, so the the secondary skill is being tested now. The the game artwork is ready. I believe Anton is doing some basic testing. He shot me some messages on exactly what the expectations were, which I clarified for him and I know the artwork for Lone Star. Is probably 80% done. So I think that'll be a quick transition. We did hear the Nevada, Nebraska Department of Revenue says they won't actually issue our license until we have a machine or preliminary documents to submit. So just so. So you know they have everything from us, they've confirmed it with Mary and I, but that that they need the approval, the initial submission from us to say yes, this is skill and then something from GLI or Eclipse to then issue us the final license paperwork. So we're on standby pending submission of of the product.

[00:44:33] **Val Levitan**: So they're waiting for Eclipse to say that they tested and only then they will give us the license.

[00:44:38] **Juan Martinez**: That's correct.

[00:44:39] **Val Levitan**: Understood. So they want, they want somebody else's *** on the line.

[00:44:43] **Juan Martinez**: That's correct, yes. Yeah, cause they're they're the Department of

[00:44:45] **Val Levitan**: Typical.

[00:44:47] **Juan Martinez**: Revenue. They're not even regulators and they handle all this. So they definitely want someone else to blame.

[00:44:54] **Val Levitan**: Yeah, typical bureaucrats. OK. And when do you think we'll be ready to

[00:44:56] **Juan Martinez**: Yep.

[00:45:00] **Val Levitan**: send the machine to Eclipse?

[00:45:03] **Juan Martinez**: I don't see why we couldn't be possibly ready in 45 days. Worst case scenario.

[00:45:12] **Val Levitan**: OK. And I guess Texas is really next, right? That's like, but right, right.

[00:45:14] **Juan Martinez**: Oh, absolutely. Yeah, might even be first. Yeah, yeah.

[00:45:19] **Val Levitan**: I I hear, I hear you. Well, I guess the moment we submit to Nebraska, we. Like immediately more or less of Texas. So would you be OK if let's say while

[00:45:27] **Juan Martinez**: OK. Correct.

[00:45:33] **Val Levitan**: we're doing Nebraska approval, send machine to reach the guy that I sent you the message for the operator in Texas?

[00:45:42] **Juan Martinez**: Yeah. Yes. OK.

[00:45:49] **Val Levitan**: OK, alright.

[00:45:53] **Juan Martinez**: OK.
