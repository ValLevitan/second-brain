# Raw Transcript — Flex-Recycler_alignemt_update-August-14-2026
**Date:** August 14, 2026, 12:00 PM ET
**Summary note:** [[Meeting_Notes_Flex_Recycler_Cycle_Test_MEI_Rework-August-14-2026]]
---
WEBVTT

00:00:03.353 --> 00:00:09.193
<v Juan Martinez>I'm just going to post your note here in the chat for those who did not see it on the status.</v>

00:00:08.553 --> 00:00:11.833
<v Val Levitan>The recording is on, Andrea. Please report.</v>

00:00:14.568 --> 00:00:32.888
<v Andrei Klimovich>Yeah, so yesterday we've completed a full assembly and connected recycler to two gaming machines with flex ports, new flex ports. And we've run the full cycle, starting with creating a wallet, playing the game machine, cashing out.</v>

00:00:33.288 --> 00:00:40.328
<v Andrei Klimovich>Returning back to recycler and getting real cash in our hands, so this cycle works.</v>

00:00:41.448 --> 00:00:47.688
<v Val Levitan>Let's go through use case. Give me a use case. Walk me through the use case.</v>

00:00:42.008 --> 00:00:42.088
<v Andrei Klimovich>Uh...</v>

00:00:48.888 --> 00:01:07.608
<v Andrei Klimovich>Okay, so me as a player, I approached Recycler. I picked up a scenario on the screen which told me start playing here or something like that, create your e-wallet or whatever. I input $5 into a cash dispenser.</v>

00:01:08.648 --> 00:01:27.208
<v Andrei Klimovich>And it asked me to create a PIN code, then to confirm a PIN code. And then there was an option either to continue with inputting money or print a ticket. So we followed the way to print a ticket.</v>

00:01:27.768 --> 00:01:31.528
<v Andrei Klimovich>It was successfully printed. I took the ticket, yeah.</v>

00:01:29.848 --> 00:01:30.408
<v Val Levitan>Sorry.</v>

00:01:31.528 --> 00:01:34.808
<v Val Levitan>Sorry, forgive me. You put in a $20 bill.</v>

00:01:35.368 --> 00:01:36.728
<v Andrei Klimovich>Five dollar, 5.</v>

00:01:36.728 --> 00:01:43.128
<v Val Levitan>So, you put in a $5 bill and you printed a QR temporary wallet.</v>

00:01:43.688 --> 00:01:47.768
<v Andrei Klimovich>Not QR, but Tito-like ticket. It's like a banknote.</v>

00:01:48.648 --> 00:01:49.208
<v Val Levitan>Okay.</v>

00:01:50.328 --> 00:02:01.928
<v Andrei Klimovich>So then we went to Game Machines with Flexports installed. We scanned the ticket, we confirmed the PIN code, and it...</v>

00:02:01.368 --> 00:02:05.208
<v Val Levitan>In you, you scanned it in Flex port.</v>

00:02:05.848 --> 00:02:07.128
<v Andrei Klimovich>Correct, export.</v>

00:02:06.648 --> 00:02:11.128
<v Val Levitan>And was the the the Flexport screen was it communicating properly?</v>

00:02:12.008 --> 00:02:30.728
<v Andrei Klimovich>Yeah, so after the ticket was scanned, it asked for a PIN code. We've input a PIN code. Then it asked us about the amount of credits we'd like to transfer. There was only one option, $5, 5 credits. This amount was successfully uploaded to the game machine.</v>

00:02:30.888 --> 00:02:50.568
<v Andrei Klimovich>We played it, we won $15, so we decided to cash out. It asked us to scan the ticket again. We did it, confirmed the PIN code, and $15 were successfully transferred to e-wallet. Then we returned back to the recycler.</v>

00:02:51.368 --> 00:02:53.848
<v Val Levitan>Did you play? Did you play a second machine?</v>

00:02:51.448 --> 00:02:52.248
<v Andrei Klimovich>We.</v>

00:02:55.928 --> 00:02:59.368
<v Andrei Klimovich>No, I don't think so. Not in this case.</v>

00:02:58.728 --> 00:03:02.248
<v Val Levitan>It's a problem. I'd like you to play the second machine.</v>

00:03:03.368 --> 00:03:08.808
<v Andrei Klimovich>Yeah, of course. I mean, like, we'll we still have a plan for a lot of testing for today.</v>

00:03:09.288 --> 00:03:18.168
<v Val Levitan>I know, but it's important because I want to make sure that there's communication that allows you to traverse through machine play.</v>

00:03:19.128 --> 00:03:20.888
<v Andrei Klimovich>Yes, of course, we've done it with pay.</v>

00:03:21.848 --> 00:03:32.168
<v Andrei Klimovich>So, we pay it works, so of course we will test it. So, back at recycler, we scan the ticket, we confirm the pin code, and there was an...</v>

00:03:33.848 --> 00:03:53.288
<v Andrei Klimovich>I'm not sure about the details, but the interface told us that the maximum amount I can dispense right now is $5 because there was only one $5 bank note in the whole bank right now. We've agreed. So $5 were dispensed and the screen was updated with the rest of</v>

00:03:44.608 --> 00:03:45.128
<v Val Levitan>Of course.</v>

00:03:53.448 --> 00:03:56.968
<v Andrei Klimovich>Balance equals $10, still playable.</v>

00:03:57.848 --> 00:04:06.528
<v Andrei Klimovich>We've taken $5 and we scanned this ticket again just to make sure that the e-wallet was updated and it showed us that the current balance is $10.</v>

00:04:09.448 --> 00:04:16.848
<v Val Levitan>OK, so I need you to fill recycler with a little bit more currency as a base.</v>

00:04:18.248 --> 00:04:20.408
<v Val Levitan>and then re-enact it again.</v>

00:04:21.608 --> 00:04:25.128
<v Val Levitan>as well as to traverse through machines.</v>

00:04:26.648 --> 00:04:28.408
<v Val Levitan>Maybe a couple of times.</v>

00:04:29.768 --> 00:04:32.888
<v Val Levitan>Back and forth a couple of times between the two machines.</v>

00:04:34.328 --> 00:04:36.408
<v Val Levitan>Then return to.</v>

00:04:37.608 --> 00:04:38.488
<v Val Levitan>The recycler.</v>

00:04:39.448 --> 00:04:41.528
<v Val Levitan>and cash out the entire amount.</v>

00:04:42.808 --> 00:04:45.928
<v Val Levitan>Make sure your entire amount is under $50.</v>

00:04:42.888 --> 00:04:43.368
<v Andrei Klimovich>Of course.</v>

00:04:47.848 --> 00:04:48.328
<v Andrei Klimovich>Mhm.</v>

00:04:48.288 --> 00:04:54.808
<v Val Levitan>And I want to see the fives and the 20s pulled from the recycler.</v>

00:04:58.088 --> 00:05:06.008
<v Val Levitan>So let's say ideal case scenario is $55 payout, two 20s and three fives.</v>

00:05:07.448 --> 00:05:09.648
<v Andrei Klimovich>Yeah, of course, I will do that.</v>

00:05:11.128 --> 00:05:19.048
<v Andrei Klimovich>We are not, I mean, like me as a player, I'm not controlling the combination of bills, of course, but let's see how it works, yeah.</v>

00:05:18.408 --> 00:05:29.048
<v Val Levitan>You know, but we don't have 10s. So if you have 20s and fives, there will be two 20s and three fives. That's why I insist on $55 payout.</v>

00:05:31.848 --> 00:05:35.368
<v Andrei Klimovich>Just one quick clarification. Why don't we have tens?</v>

00:05:37.208 --> 00:05:43.768
<v Val Levitan>I mean, we will have 10s, but in this particular setup, I don't believe you have 10s.</v>

00:05:40.408 --> 00:05:41.368
<v Andrei Klimovich>Okay, okay, okay.</v>

00:05:42.408 --> 00:05:42.968
<v Andrei Klimovich>Yes.</v>

00:05:44.248 --> 00:05:45.848
<v Andrei Klimovich>Okay, okay, I got it. Sure.</v>

00:05:45.288 --> 00:05:55.768
<v Val Levitan>The MEI recycler at the end, the MEI mechanics, the construction of it is incorrect. We're not going to go with it.</v>

00:05:58.088 --> 00:06:16.728
<v Val Levitan>It just, it's a wrong recycler. We just don't have time before the show to get the right thing. But we're going to go with the right recycler, right combination. We need multiple cassettes. MEI is not going to cut it. They're not going to supply us with the product. We have the product. We are</v>

00:06:16.888 --> 00:06:17.768
<v Val Levitan>Redoing.</v>

00:06:18.728 --> 00:06:21.048
<v Val Levitan>We're already sent, we're sending it to Minsk.</v>

00:06:22.248 --> 00:06:23.448
<v Val Levitan>We will redo it.</v>

00:06:25.648 --> 00:06:27.688
<v Val Levitan>By mid-September.</v>

00:06:28.848 --> 00:06:33.048
<v Val Levitan>that coincides with the introduction of...</v>

00:06:34.248 --> 00:06:34.968
<v Val Levitan>Point.</v>

00:06:35.768 --> 00:06:38.408
<v Val Levitan>Play or price play?</v>

00:06:37.368 --> 00:06:38.008
<v Andrei Klimovich>Skill play.</v>

00:06:38.048 --> 00:06:39.608
<v Felipe Miranda Giorgi>Rice, Scooby.</v>

00:06:39.048 --> 00:06:40.328
<v Juan Martinez>You'll still pay.</v>

00:06:39.248 --> 00:06:44.328
<v Val Levitan>Skill, skill, sorry, I apologize, skill pay, income.</v>

00:06:45.848 --> 00:06:51.968
<v Val Levitan>introduction of their card, we will have the right recycler sitting in the recycler.</v>

00:06:52.968 --> 00:06:53.768
<v Val Levitan>A box.</v>

00:06:55.128 --> 00:06:57.768
<v Val Levitan>And mid-September.</v>

00:06:55.288 --> 00:06:55.688
<v Andrei Klimovich>Okay.</v>

00:06:58.848 --> 00:07:05.448
<v Val Levitan>hypothetically speaking, approximate date is when we are launching first beta sample.</v>

00:07:10.408 --> 00:07:12.168
<v Val Levitan>Approximately, right?</v>

00:07:15.368 --> 00:07:15.848
<v Andrei Klimovich>Okay.</v>

00:07:16.248 --> 00:07:16.568
<v Pavel Frolov>Yeah.</v>

00:07:20.088 --> 00:07:32.328
<v Val Levitan>Okay. Okay, this is excellent news. Excellent news. Just do that traversing through the machines, get payout of $55, report back to us.</v>

00:07:33.528 --> 00:07:52.448
<v Andrei Klimovich>Yeah, so for sure I will do that. But before that, I need to finalize the assembly. And I really like to run dispenser first to boot it up. I've received the most recent build from Alexander, and it's already uploaded. So I just want to make sure the dispenser sees.</v>

00:07:53.048 --> 00:08:00.808
<v Andrei Klimovich>all the parameters, all the parts, and after that I will finalize the recycler while Minsk is still online.</v>

00:08:04.808 --> 00:08:08.088
<v Val Levitan>Okay. Irina, you're working tomorrow, right?</v>

00:08:09.848 --> 00:08:10.248
<v Irina Shishko>The.</v>

00:08:10.808 --> 00:08:13.848
<v Val Levitan>So, tomorrow, your goal is V3.</v>

00:08:14.928 --> 00:08:16.648
<v Val Levitan>Must be done, V3.</v>

00:08:15.128 --> 00:08:15.688
<v Irina Shishko>Yes.</v>

00:08:24.488 --> 00:08:27.448
<v Val Levitan>Monday, Monday morning, Monday morning.</v>

00:08:27.928 --> 00:08:28.888
<v Irina Shishko>Ah, OK.</v>

00:08:29.928 --> 00:08:32.368
<v Val Levitan>North American time, Monday morning, North America.</v>

00:08:34.646 --> 00:08:35.006
<v Irina Shishko>Да.</v>

00:08:34.676 --> 00:08:35.436
<v Pavel Frolov>Окей, профессор.</v>

00:08:36.536 --> 00:08:39.496
<v Irina Shishko>Да, мы 14:00 работаем поэтому.</v>

00:08:36.856 --> 00:08:40.816
<v Val Levitan>Со егор и я с егорке нот гогом.</v>

00:08:41.936 --> 00:08:43.696
<v Val Levitan>Час паемпаем начос.</v>

00:08:47.516 --> 00:08:49.356
<v Val Levitan>Окей, большие.</v>

00:08:50.736 --> 00:08:51.936
<v Val Levitan>Andreighta закочен.</v>

00:08:54.156 --> 00:08:57.156
<v Val Levitan>Возил туда.</v>

00:08:57.926 --> 00:08:59.286
<v Val Levitan>Таньки говорим, что у банки.</v>

00:08:58.946 --> 00:08:59.366
<v Andrei Klimovich>Окей.</v>

00:08:59.876 --> 00:09:00.356
<v Pavel Frolov>Бай.</v>

00:09:00.006 --> 00:09:00.566
<v Irina Shishko>Понимаю.</v>

00:09:01.106 --> 00:09:01.666
<v Andrei Klimovich>Давай.</v>

