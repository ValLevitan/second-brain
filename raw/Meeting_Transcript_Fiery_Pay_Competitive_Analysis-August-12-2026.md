# Raw Transcript — GA-COAM_Fiery_Pay
**Date:** August 12, 2026, 3:31–4:02 PM (Eastern)
**Summary note:** [[Meeting_Notes_Fiery_Pay_Competitive_Analysis-August-12-2026]]
---
WEBVTT

00:00:09.369 --> 00:00:09.769
<v Felipe Miranda Giorgi>Hi.</v>

00:00:11.209 --> 00:00:11.929
<v Val Levitan>Hello.</v>

00:00:13.689 --> 00:00:14.089
<v Juan Martinez>No.</v>

00:00:20.729 --> 00:00:22.329
<v Juan Martinez>Are we waiting for Andrei?</v>

00:00:22.609 --> 00:00:29.209
<v Felipe Miranda Giorgi>I don't think, I don't think he's in the office. I think he's, I don't know if he's out to lunch or I didn't see him around right now.</v>

00:00:28.089 --> 00:00:28.489
<v Juan Martinez>Okay.</v>

00:00:36.649 --> 00:00:38.329
<v Val Levitan>Okay, so...</v>

00:00:44.249 --> 00:01:03.009
<v Juan Martinez>I threw together a quick use case based on what Felipe described. Obviously, I didn't have much time to dig into it, but it might help you generate some further questions or what to look at when you go and visit the site. So I just posted it in the chat.</v>

00:01:04.169 --> 00:01:04.649
<v Felipe Miranda Giorgi>Okay.</v>

00:01:05.849 --> 00:01:06.809
<v Juan Martinez>Okay, so...</v>

00:01:05.929 --> 00:01:06.809
<v Felipe Miranda Giorgi>Appreciate it.</v>

00:01:09.289 --> 00:01:27.409
<v Juan Martinez>So I see what you posted. I see that, you know, Fiery Pay has some hardware, both external to the cashier maybe, as well as something, these kits inside of the machines. And the...</v>

00:01:25.369 --> 00:01:26.089
<v Felipe Miranda Giorgi>No, yeah.</v>

00:01:28.569 --> 00:01:42.889
<v Juan Martinez>The statement you made about JVL being the most complex to me means they're not using SAS, which would be easy. They're tying into the printers or bill acceptors and doing pulses.</v>

00:01:41.849 --> 00:01:48.649
<v Felipe Miranda Giorgi>No, no printer, no printer in this system. As a matter of fact, this particular location, Juan, if you recall,</v>

00:01:44.569 --> 00:01:45.609
<v Juan Martinez>No printer, OK.</v>

00:01:47.969 --> 00:01:55.929
<v Val Levitan>No, they cannot. They cannot tie to a printer. They gotta go through a bill acceptor because bill acceptor issues credits.</v>

00:01:56.329 --> 00:01:56.969
<v Juan Martinez>Right, right.</v>

00:01:56.489 --> 00:01:56.809
<v Felipe Miranda Giorgi>Yeah.</v>

00:01:57.769 --> 00:02:07.009
<v Val Levitan>So they tie into a print, a bill acceptor, and because bill acceptor, let's say protocol is, I don't know, JCM or MEI.</v>

00:02:08.489 --> 00:02:10.969
<v Val Levitan>They have to communicate through the protocol as well.</v>

00:02:13.289 --> 00:02:21.129
<v Juan Martinez>And I think that Val described that all makes sense. What is unclear.</v>

00:02:20.169 --> 00:02:26.649
<v Val Levitan>And, and so, and just to just to continue the way I visualize it, so sorry for interrupting.</v>

00:02:24.569 --> 00:02:28.489
<v Juan Martinez>Ohh, guess my camera was off. No, no, sorry, go ahead, Val.</v>

00:02:27.529 --> 00:02:27.929
<v Val Levitan>Hello?</v>

00:02:31.289 --> 00:02:34.089
<v Val Levitan>Sorry, did I interrupt anybody? I didn't, I wasn't watching a screen.</v>

00:02:35.689 --> 00:02:54.889
<v Val Levitan>OK, so they the way I understand it, and this is I haven't read your use case. I I don't know what your role, but I assume let me let me play a player. So I come in, I put $20, I win on the machine, it generates a ticket in the bag.</v>

00:02:55.129 --> 00:03:14.649
<v Val Levitan>I go in the back, it's a fiery system, whatever device, and they say, oh, great, you won $100. Do you want it on a card or do you want me to send it back to the machine? Would you like to continue playing? He says, I'd like to send it to the machine.</v>

00:03:15.209 --> 00:03:20.009
<v Val Levitan>Can you send it to machine number 5? Oh yes, machine number 5. Boom.</v>

00:03:21.129 --> 00:03:36.809
<v Val Levitan>The credit going machine #5 and he goes like this three times. At the end he won $200.00. Says, OK, I'm done playing. I don't want to play anymore. Give me the card. So they issue a card and the player leaves.</v>

00:03:38.889 --> 00:03:41.849
<v Val Levitan>That is the only legal legitimate.</v>

00:03:43.129 --> 00:03:48.089
<v Val Levitan>solution that I can see. And if this is what they're doing, it's a failure.</v>

00:03:49.289 --> 00:03:54.809
<v Juan Martinez>And but Val, you used the word legal. I was going to say I don't think it's legal. You.</v>

00:03:54.329 --> 00:03:57.849
<v Val Levitan>I don't think it's legal, but okay, let me rephrase it.</v>

00:04:00.889 --> 00:04:05.289
<v Val Levitan>A gymnastics workaround.</v>

00:04:05.289 --> 00:04:06.249
<v Felipe Miranda Giorgi>Park around, yeah.</v>

00:04:06.809 --> 00:04:07.129
<v Juan Martinez>Yeah.</v>

00:04:07.529 --> 00:04:09.289
<v Felipe Miranda Giorgi>I, I believe that's exactly.</v>

00:04:07.769 --> 00:04:14.009
<v Val Levitan>Not, not, not legal, not legal for sure, but let's call it legal-ish.</v>

00:04:15.129 --> 00:04:36.049
<v Val Levitan>Like supposedly, the way they interpret the law, they say, well, it didn't really get to the redemption point yet. It is a transfer point. So I use it as a transfer from machine A to machine B. I don't know if the law allows that or not, but in their mind, they probably think this way.</v>

00:04:38.329 --> 00:04:43.689
<v Val Levitan>I don't know, but if this is the case, it's ******* suicidal.</v>

00:04:45.209 --> 00:04:57.769
<v Juan Martinez>I mean, what they're leveraging what Tito does is you cash out, you take the ticket, you move to the next machine. When you're done with your final cash out, that's when you go to the gift card option.</v>

00:04:58.169 --> 00:05:16.489
<v Val Levitan>Yeah, but excuse me, T2 is convenient, right? You print a ticket, you never have to touch cash anymore. You walk from machine to machine. It's inconvenient for small locations because it creates a nightmare for service operators. But in a casino environment, it is quasi-convenient.</v>

00:05:01.009 --> 00:05:02.569
<v Juan Martinez>Of course, of course.</v>

00:05:17.289 --> 00:05:37.569
<v Val Levitan>Well, yeah, I mean, it's convenient because it's easier to print paper than to allow a player to cash out, and you know, it allowed casinos to remove hoppers, etcetera, etcetera, etcetera. But you know, that's a different story. We don't have to get into philosophy of that. My point is...</v>

00:05:36.169 --> 00:05:38.649
<v Juan Martinez>Sure, but one of my questions go ahead, Val.</v>

00:05:40.169 --> 00:05:46.969
<v Val Levitan>Yeah, you know, I took I took over the floor just like just like I always do, which is I always regret doing that.</v>

00:05:50.409 --> 00:05:51.689
<v Val Levitan>Yeah, okay.</v>

00:05:53.289 --> 00:05:54.009
<v Felipe Miranda Giorgi>I just...</v>

00:05:53.449 --> 00:05:54.649
<v Val Levitan>I, I start everything.</v>

00:05:55.049 --> 00:06:02.489
<v Felipe Miranda Giorgi>I just wanna add that in the user case that Val Mery, there could also be partial.</v>

00:06:04.329 --> 00:06:10.209
<v Felipe Miranda Giorgi>redemption and partial transfer of credits, not the full amount.</v>

00:06:11.449 --> 00:06:13.689
<v Juan Martinez>And what happens, Felipe?</v>

00:06:11.849 --> 00:06:23.929
<v Felipe Miranda Giorgi>And I believe that in the POS, they can actually select if they want to buy lottery ticket or if they're getting this or that. It's, you know, it's a different options.</v>

00:06:24.089 --> 00:06:38.329
<v Val Levitan>I hope that this is it, because, in my opinion, if we play our cards right, if we do things right, we should disseminate them. We should we should rip them in pieces with our with our offer.</v>

00:06:39.449 --> 00:06:48.329
<v Val Levitan>In my opinion, I'm biased. I am in love with a product. Of course I am. How can I create otherwise? But in my opinion...</v>

00:06:49.849 --> 00:06:51.129
<v Val Levitan>They wouldn't hold a candle.</v>

00:06:51.849 --> 00:07:12.409
<v Juan Martinez>Yeah, but Val, I mean, what my concern is, it's, well, what we just walked through is so obviously a major security flaw, because if it's my uncle and he says, oh, I want $100, send 50 back to the machine, you could probably type in 60 because there's no real systems check. I mean, the...</v>

00:07:12.649 --> 00:07:16.089
<v Juan Martinez>The fraud possibility is through the roof.</v>

00:07:12.729 --> 00:07:13.369
<v Val Levitan>No.</v>

00:07:16.329 --> 00:07:18.089
<v Val Levitan>Through the roof, through the roof.</v>

00:07:17.609 --> 00:07:20.329
<v Juan Martinez>But it just, it seems like they just don't care.</v>

00:07:20.729 --> 00:07:21.449
<v Val Levitan>Don't care.</v>

00:07:22.009 --> 00:07:24.089
<v Juan Martinez>So are we over caring?</v>

00:07:25.049 --> 00:07:33.609
<v Juan Martinez>You know, because this is so unregulated. When GLC said, we're not controlling what these kiosks do, they wipe their hands of everything.</v>

00:07:34.009 --> 00:07:34.809
<v Val Levitan>I...</v>

00:07:36.249 --> 00:07:52.969
<v Val Levitan>In my mind, my philosophy personally is different. My philosophy is that it is imminent. It is 100% imminent that either this month or the following month, income is coming out with a price play card.</v>

00:07:56.009 --> 00:08:03.369
<v Val Levitan>I already spoke to Herring Bank. We are getting our ATM license.</v>

00:08:04.569 --> 00:08:05.289
<v Val Levitan>So...</v>

00:08:06.649 --> 00:08:12.009
<v Val Levitan>We're, in essence, we're becoming an approved ATM.</v>

00:08:14.009 --> 00:08:17.209
<v Val Levitan>in the location with dual function.</v>

00:08:18.289 --> 00:08:20.409
<v Val Levitan>Actually, with triple function.</v>

00:08:21.449 --> 00:08:29.129
<v Val Levitan>We accept the money, we act as an ATM, and we also act as a...</v>

00:08:30.329 --> 00:08:30.889
<v Val Levitan>Uh...</v>

00:08:32.249 --> 00:08:35.769
<v Val Levitan>Traversing organ where a player could...</v>

00:08:37.849 --> 00:08:44.249
<v Val Levitan>Use temporary wallet to play from machine to machine, all without any supervision.</v>

00:08:45.449 --> 00:08:52.569
<v Val Levitan>I don't understand how they will be able to compete. And that is a lot of technology. I'm sorry. That is a lot of technology.</v>

00:08:51.249 --> 00:08:51.609
<v Juan Martinez>Yeah.</v>

00:08:54.489 --> 00:08:55.929
<v Val Levitan>It's not easy to compete.</v>

00:08:58.409 --> 00:09:07.129
<v Juan Martinez>Yeah, because I mean, even what you say put $50 back on my game. What if somebody's now sitting at the machine immediately after I got up?</v>

00:09:08.649 --> 00:09:18.889
<v Juan Martinez>Yeah, and he inserts the dollar. Who's to say, you know, that I don't even, that's such a huge flaw, sending money back to an unattended machine.</v>

00:09:08.969 --> 00:09:09.289
<v Felipe Miranda Giorgi>Yeah.</v>

00:09:15.809 --> 00:09:16.729
<v Val Levitan>No, but...</v>

00:09:19.209 --> 00:09:32.249
<v Val Levitan>Which, by the way, it existed over and over in every country. Do you remember Belgian setups after Bali left?</v>

00:09:24.569 --> 00:09:24.969
<v Juan Martinez>Yeah.</v>

00:09:34.569 --> 00:09:52.489
<v Val Levitan>the bingo business, mechanical bingo machine business. The Belgian manufacturer picked up on this and there was a huge Belgian business with former Bally bingo machines when they went from solid relay to solid-state boards.</v>

00:09:37.049 --> 00:09:37.169
<v Juan Martinez>Yeah.</v>

00:09:53.209 --> 00:09:55.689
<v Val Levitan>They had so-called telephones.</v>

00:09:56.889 --> 00:10:01.049
<v Val Levitan>where they used to send credits to the machines. It never worked.</v>

00:10:01.609 --> 00:10:02.889
<v Juan Martinez>Sure, sure, sure.</v>

00:10:02.929 --> 00:10:21.969
<v Val Levitan>It was a gimmick. It never worked. It will never work. You cannot send credits to the machines. But okay, you know what? Let me take a step back. Let me remove my hatred hat. Let me put a sympathizer hat on. So you know what?</v>

00:10:08.489 --> 00:10:08.769
<v Juan Martinez>Yeah.</v>

00:10:23.169 --> 00:10:29.289
<v Val Levitan>Let's assume I like that telephone business, but at the end, when a player won.</v>

00:10:32.329 --> 00:10:33.929
<v Val Levitan>Is he walking away with the card?</v>

00:10:35.449 --> 00:10:53.209
<v Val Levitan>So you send that telephone, you send credits back to the machine three times. So first player won $20. He wants now to travel to another machine. You send $20 to machine B. He won $100. You now take $100 and you send telephone to...</v>

00:10:54.729 --> 00:11:00.129
<v Val Levitan>to machine #3, and he ended up winning $500.</v>

00:11:01.529 --> 00:11:07.249
<v Val Levitan>So he says, enough. I've been here for three hours. I'm leaving. Give me my $500.</v>

00:11:03.609 --> 00:11:03.929
<v Juan Martinez>Right.</v>

00:11:08.569 --> 00:11:24.169
<v Val Levitan>So at this point, after all this gymnastic, after all of this ******* around, you still issue a card that a player walks away with, where your entire purpose was to take the money off of the player.</v>

00:11:19.049 --> 00:11:19.369
<v Juan Martinez>Yeah.</v>

00:11:26.409 --> 00:11:27.529
<v Juan Martinez>Yeah, but Val and your...</v>

00:11:26.649 --> 00:11:29.049
<v Val Levitan>So, what do, what's the ******* purpose?</v>

00:11:28.169 --> 00:11:29.769
<v Felipe Miranda Giorgi>But, but that's...</v>

00:11:28.689 --> 00:11:36.649
<v Juan Martinez>But your scenario only implies that he won. He could have likely lost all of his money. So it's a 50-50.</v>

00:11:36.569 --> 00:11:38.569
<v Felipe Miranda Giorgi>Yes, but, but that's.</v>

00:11:37.929 --> 00:11:40.329
<v Val Levitan>It's actually, it's actually sorry, it's ninety-five percent.</v>

00:11:40.729 --> 00:11:42.169
<v Juan Martinez>Yeah, yeah, yeah, sorry.</v>

00:11:42.569 --> 00:11:42.809
<v Val Levitan>Yeah.</v>

00:11:42.729 --> 00:12:00.089
<v Felipe Miranda Giorgi>Yeah, but then that's the additional, and that's why I mentioned the fact that he claims that people can come back with that same gift card and they can send credits to machines from whatever amount he wants to play from the balance he has left. I want to play 50.</v>

00:11:59.169 --> 00:11:59.609
<v Val Levitan>What?</v>

00:12:00.289 --> 00:12:20.169
<v Juan Martinez>That's the part, Felipe, that doesn't make sense because this gift card is supposedly not redeemable for cash. Like you try to shove it in an ATM, it gets blocked. Income has always been up front with us on that. So how are they legally converting that to cash?</v>

00:12:00.729 --> 00:12:01.049
<v Val Levitan>Val.</v>

00:12:14.729 --> 00:12:15.209
<v Felipe Miranda Giorgi>Oh yeah.</v>

00:12:20.089 --> 00:12:24.569
<v Felipe Miranda Giorgi>Well, the POS allows them to buy lottery tickets.</v>

00:12:24.889 --> 00:12:30.489
<v Juan Martinez>No, no, but what you just described is the player came back with yesterday's card.</v>

00:12:30.729 --> 00:12:31.209
<v Felipe Miranda Giorgi>Right.</v>

00:12:31.689 --> 00:12:37.449
<v Juan Martinez>Okay, now he gives your card to the attendant and they do what?</v>

00:12:36.089 --> 00:12:46.649
<v Felipe Miranda Giorgi>He gives a card. I don't know if they scan it. I didn't see it live, but that's what he claims. I actually called them about this because I had a question.</v>

00:12:45.529 --> 00:13:03.849
<v Val Levitan>But in order to move money that is now sitting on the prepaid card, that's a MasterCard domain. You have to be a MasterCard registered, what do you call it? What's that number called?</v>

00:13:03.369 --> 00:13:04.569
<v Juan Martinez>A reseller.</v>

00:13:04.809 --> 00:13:13.289
<v Val Levitan>Reseller, yeah. It's not your money anymore. It's not locations money anymore. It's master's card money.</v>

00:13:06.169 --> 00:13:07.929
<v Juan Martinez>Yeah, with the merchant ID and...</v>

00:13:11.529 --> 00:13:11.929
<v Juan Martinez>Right.</v>

00:13:15.129 --> 00:13:20.889
<v Juan Martinez>But now this fiery pay, it looks like they may be a reseller because they're in the payment business.</v>

00:13:20.889 --> 00:13:21.529
<v Felipe Miranda Giorgi>Yes.</v>

00:13:23.369 --> 00:13:30.009
<v Val Levitan>But, but then, but I I don't understand how are they so it doesn't touch their Mastercard.</v>

00:13:30.569 --> 00:13:38.009
<v Juan Martinez>Well, no, maybe it does. I mean, maybe because they have a valid merchant ID. Let's say the card has $100 on it.</v>

00:13:37.929 --> 00:13:41.769
<v Val Levitan>But it's not them, it's the location that has to have merchant ID.</v>

00:13:44.009 --> 00:13:46.409
<v Juan Martinez>I'm not sure about that. If you're on...</v>

00:13:45.449 --> 00:13:49.769
<v Val Levitan>Well, the fiery, okay, but the fireplace came to Seminoles.</v>

00:13:50.729 --> 00:13:51.049
<v Juan Martinez>Yeah.</v>

00:13:51.129 --> 00:13:53.049
<v Val Levitan>Who, who's gonna have?</v>

00:13:54.329 --> 00:13:56.649
<v Val Levitan>merchant ID, them or the seminals.</v>

00:13:57.769 --> 00:14:17.249
<v Juan Martinez>The Seminoles, because we are smart enough, we would have been smart enough to want all of those ATM fees to come to us. But Fiery Ice might be or Fiery Pay might be saying, listen, you don't have to register, we'll do it and we'll split something with you. I mean, they may be on the network because how else can you accept</v>

00:14:17.689 --> 00:14:32.409
<v Juan Martinez>this gift card and convert it into, it looks like you're buying a fake transaction at the location and that's how you're emptying your card. But the card, they're not giving you cash, at least not today. They're giving you credits for the machine.</v>

00:14:32.329 --> 00:14:44.009
<v Felipe Miranda Giorgi>I just want to ask you a simple question. Is the kiosk any different from this system for gift card redemption to a ticket, for example? Is it different in that case?</v>

00:14:42.409 --> 00:14:46.729
<v Val Levitan>What do you mean? What do you mean kiosk? Can you elaborate on the kiosk?</v>

00:14:46.649 --> 00:14:48.969
<v Felipe Miranda Giorgi>A kiosk machine, a kiosk.</v>

00:14:50.249 --> 00:14:51.209
<v Felipe Miranda Giorgi>You know, much.</v>

00:14:50.489 --> 00:15:08.729
<v Juan Martinez>Yeah, that's my idea of what they're doing as their argument. Hey, when you cash out in a location in Georgia that has a Tito system and kiosk, you instantly move from machine to machine. You don't have to create a gift card every time you cash out, only when you're done.</v>

00:15:08.889 --> 00:15:11.409
<v Juan Martinez>and they're probably using the same argument.</v>

00:15:09.849 --> 00:15:30.249
<v Felipe Miranda Giorgi>Yeah, yeah, but now my question is, would it also apply to a kiosk where you go back with your gift card and turn it into player points? Because Andrei, I told Andrei to go visit a location where he could actually see this live and he went on Saturday or Sunday and he went through the whole flow of creating a gift card and coming back with a gift card.</v>

00:15:30.569 --> 00:15:33.769
<v Felipe Miranda Giorgi>from gift card to player points and from player point to machines.</v>

00:15:34.929 --> 00:15:36.809
<v Felipe Miranda Giorgi>I mean, it, how is it different?</v>

00:15:37.209 --> 00:15:40.569
<v Juan Martinez>Did he write that up? No, I don't. I didn't see anything from Andrei.</v>

00:15:40.649 --> 00:16:00.609
<v Felipe Miranda Giorgi>Well, I reported it back in the day when I went. I have video, I showed him video, and I said, look, this is the address. And I know that he went and visited on Saturday or Sunday because he went to Macon. And he told me, oh, I went to that place, I played, yeah, and the gift card, you can turn it. I have pictures. Yeah, I know I reported this to both of you.</v>

00:16:01.609 --> 00:16:03.849
<v Felipe Miranda Giorgi>my experience at that particular location.</v>

00:16:04.009 --> 00:16:07.689
<v Val Levitan>And I'm sorry, what's the flow in that location? Can you repeat that, please?</v>

00:16:07.289 --> 00:16:27.209
<v Felipe Miranda Giorgi>So player comes in, he can put cash directly on the bill acceptor, play the machine. When he cashes out, that moment there was the like a loyalty card, let's call it an e-wallet or a loyalty card or card.</v>

00:16:27.289 --> 00:16:48.249
<v Felipe Miranda Giorgi>sitting on the machine that anybody could use for cash outs. And then you cash out, it says, please insert or swipe the loyalty card. You swipe it, and then all the credits you cashed out go to this card. Then you move on to the kiosk, and you say, it gives you the option.</v>

00:16:48.489 --> 00:17:07.649
<v Felipe Miranda Giorgi>Player points to gift card or gift card to player points. Okay, player points to gift cards. So then I slide it. It issues a gift card, charges the $2 fee, issues the gift card, but I could come back with the same gift card, scan the barcode, and convert gift card</v>

00:17:07.729 --> 00:17:15.929
<v Felipe Miranda Giorgi>Two player point, and with this point I go back to machine, I swipe it, and my credits are in machine, I...</v>

00:17:16.329 --> 00:17:19.049
<v Val Levitan>But, but what else can you do with this gift card?</v>

00:17:19.769 --> 00:17:21.089
<v Felipe Miranda Giorgi>Ohh, you can buy anything.</v>

00:17:22.169 --> 00:17:22.969
<v Felipe Miranda Giorgi>It's a gift card.</v>

00:17:22.169 --> 00:17:24.089
<v Juan Martinez>It's a standard prize pay card.</v>

00:17:25.209 --> 00:17:25.449
<v Felipe Miranda Giorgi>Yeah.</v>

00:17:26.569 --> 00:17:30.089
<v Val Levitan>Sorry, you can buy anything you mean.</v>

00:17:31.769 --> 00:17:32.409
<v Val Levitan>Where?</v>

00:17:31.929 --> 00:17:42.329
<v Felipe Miranda Giorgi>Yeah, I can go to Walmart with this gift card. I can go to, I mean, anything. It's a gift card. It's one of these. It should have one here. But I mean, I've...</v>

00:17:32.009 --> 00:17:32.809
<v Juan Martinez>Any item?</v>

00:17:44.649 --> 00:17:57.289
<v Felipe Miranda Giorgi>And I personally did the floor. I know, and maybe Andrei's memory would be fresher because he went there just a few days ago and he can tell us his experience, but yeah, it's a regular gift card type.</v>

00:18:01.049 --> 00:18:03.209
<v Felipe Miranda Giorgi>Price pay or yeah.</v>

00:18:04.729 --> 00:18:06.329
<v Felipe Miranda Giorgi>Debit or yeah.</v>

00:18:08.329 --> 00:18:14.969
<v Juan Martinez>Yeah, I'm just confused on how you're converting A MasterCard gift card into player points.</v>

00:18:16.169 --> 00:18:25.449
<v Juan Martinez>You have to be doing a fake transaction being reported to MasterCard. Hey, this guy just bought $100 worth of tobacco products.</v>

00:18:25.609 --> 00:18:27.049
<v Felipe Miranda Giorgi>Yeah, let, let, let.</v>

00:18:26.329 --> 00:18:30.329
<v Juan Martinez>Instead of paying them in cash, you're converting it to player points.</v>

00:18:32.329 --> 00:18:41.129
<v Juan Martinez>I mean, there's, that's so gray. It also, it violates the intent of the original gift card.</v>

00:18:46.489 --> 00:18:56.729
<v Felipe Miranda Giorgi>Yeah, but I remember I reported this whole flow in a, I believe in confluence or one of the pages we had for this purpose, because I...</v>

00:18:59.689 --> 00:19:01.209
<v Felipe Miranda Giorgi>This is a location about.</v>

00:19:02.729 --> 00:19:16.809
<v Felipe Miranda Giorgi>Two hours away. And by the way, this new location where I just went to and I investigated about Fire Repay, they had Tito. This is the location where our game froze and I had to go and that's when we discovered the bug and blah, blah, blah.</v>

00:19:18.409 --> 00:19:37.049
<v Felipe Miranda Giorgi>So they needed me to reconfigure machine to no printer again because they were sick of the kiosk. So they're getting rid of the printers, they're moving the kiosk out, and they're going with the solution. They don't want to deal with the kiosk. Funny enough.</v>

00:19:42.329 --> 00:19:47.289
<v Felipe Miranda Giorgi>I can look, I can look for the video. It'll take me a while, but I can resend it.</v>

00:19:46.329 --> 00:19:57.289
<v Juan Martinez>And Felipe, is it fair that you've heard from multiple operators or was it from fiery pay that there's an appetite for their system in multiple locations?</v>

00:19:57.209 --> 00:20:16.409
<v Felipe Miranda Giorgi>I've heard from several operators. So I hear appetite for their system. Right now, like I said last time, I think that the Tito rush is flying down. Nobody, like, you don't hear Tito anymore so much. But when you do hear Tito, it's because you're hearing about...</v>

00:20:16.729 --> 00:20:22.089
<v Felipe Miranda Giorgi>The new solution from Mad Send, Lion Wonder, and...</v>

00:20:23.129 --> 00:20:35.769
<v Felipe Miranda Giorgi>Well, Batson is Light and Wonder, but Batson and Easylinks, where the ticket is printed in the back, right? And they move around with that ticket.</v>

00:20:37.289 --> 00:20:52.089
<v Felipe Miranda Giorgi>And this one that is from Afshad, Fiery Pay, the link with Aristocrat, you know, it's the most popular, and Access, of course, a lot of people moving towards Access solution with printer.</v>

00:20:52.769 --> 00:21:05.529
<v Juan Martinez>Yeah, I mean, because based on the pictures you supplied, this has to be supported by the operator who has everybody's machines so that the proper installation kits could have been created.</v>

00:21:05.769 --> 00:21:27.289
<v Felipe Miranda Giorgi>Yes. So what, you know, I was just sitting in the office and this guy came and he said, you know, we need a new software. So I redid his RIS. I gave it to him. He said, we're going to, we're going to remove the kiosk and we're going to install this. I said, oh, nice. Let me know if you need help. So he sent me a picture with the box and it said, JVL kit for flex. I was like, what?</v>

00:21:27.689 --> 00:21:37.769
<v Felipe Miranda Giorgi>Okay, what's in that kid? I'm here. Can I go with you? Do you mind if I join you to take a look? They said, no, come on. So that's why I had the opportunity to take a look, but...</v>

00:21:39.929 --> 00:21:55.849
<v Felipe Miranda Giorgi>But I hear a lot of people, plus I know Afshad has a lot of reach with the Indian crowd and all this skies. And by the way, fiery payments is a whole, I don't know if they have</v>

00:21:56.929 --> 00:22:16.649
<v Felipe Miranda Giorgi>I don't know if you call it bank license or merchant, but this kind of thing, because this is not only for Georgia. I mean, Fiery Payments is much bigger than Cohen. It has to do with many different kind of payment solutions, not only Cohen. I know it's ATM. I know it's a lot of different things.</v>

00:22:08.449 --> 00:22:08.809
<v Juan Martinez>Yeah.</v>

00:22:18.489 --> 00:22:22.569
<v Felipe Miranda Giorgi>Well, you spoke to him, Juan, and I believe you too, Val, with F shot.</v>

00:22:24.729 --> 00:22:26.249
<v Val Levitan>I did not speak to him now.</v>

00:22:27.049 --> 00:22:27.449
<v Felipe Miranda Giorgi>No.</v>

00:22:28.329 --> 00:22:28.649
<v Val Levitan>No.</v>

00:22:30.889 --> 00:22:47.289
<v Juan Martinez>Yeah, I mean, according to their website, they work with Visa, MasterCard, American Express, Discover, Union Pay, and some other bank called JCB. So they are definitely somehow connected to credit card processing.</v>

00:22:31.049 --> 00:22:31.449
<v Felipe Miranda Giorgi>Listen.</v>

00:22:48.409 --> 00:22:49.049
<v Felipe Miranda Giorgi>Yes.</v>

00:22:51.209 --> 00:22:54.329
<v Juan Martinez>Well, I mean, to me, it sounds like hello.</v>

00:22:53.849 --> 00:23:02.969
<v Felipe Miranda Giorgi>No Val, you did speak to him and we had an NDA that we did not sign or they did not sign, but there was a lot of back and forth conversation.</v>

00:23:02.929 --> 00:23:12.329
<v Val Levitan>No, there was a lot of back and forth on your side. I was asking you questions, but I never ended up speaking to him because I refused to sign the NDA.</v>

00:23:09.529 --> 00:23:10.329
<v Felipe Miranda Giorgi>I'm OK.</v>

00:23:12.569 --> 00:23:14.769
<v Felipe Miranda Giorgi>Ohh, okay, yeah.</v>

00:23:16.849 --> 00:23:26.169
<v Juan Martinez>So, I mean, basically, it sounds like the replay is winning people over that, that is a critical point.</v>

00:23:26.929 --> 00:23:32.929
<v Juan Martinez>Where, um, you know, we need to figure out how to get money back onto the machines, which could...</v>

00:23:32.169 --> 00:23:38.329
<v Val Levitan>But replay, but replay is our version of the temporary wallet.</v>

00:23:39.209 --> 00:23:39.689
<v Juan Martinez>Yes.</v>

00:23:42.409 --> 00:23:43.409
<v Felipe Miranda Giorgi>Yes, Cris.</v>

00:23:45.529 --> 00:23:53.929
<v Juan Martinez>But in order to print that temporary, the initial QR code, don't we need a FlexPay kiosk in the location?</v>

00:23:54.889 --> 00:23:56.409
<v Val Levitan>We need a recycler.</v>

00:23:57.529 --> 00:23:57.929
<v Juan Martinez>Okay.</v>

00:24:00.169 --> 00:24:09.209
<v Val Levitan>We got a, our winning combination is a recycler with the IQ. This is how we need to win the market.</v>

00:24:11.609 --> 00:24:16.169
<v Felipe Miranda Giorgi>Why would you need IQ if you have recycler? I'm curious. Okay.</v>

00:24:14.569 --> 00:24:18.089
<v Val Levitan>You don't, you don't, you don't need IQ, no.</v>

00:24:20.729 --> 00:24:25.849
<v Val Levitan>I think people will still end up having IQ, but you probably don't need it.</v>

00:24:33.449 --> 00:24:34.249
<v Juan Martinez>Can we?</v>

00:24:33.609 --> 00:24:39.769
<v Val Levitan>But if you have a recycler, don't forget, you also need a flex port.</v>

00:24:40.409 --> 00:24:41.289
<v Felipe Miranda Giorgi>Yeah, of course.</v>

00:24:41.209 --> 00:24:41.529
<v Juan Martinez>Yeah.</v>

00:24:43.369 --> 00:24:56.969
<v Val Levitan>So then we should install recycler, flex port, and then we can provide very sophisticated reporting to operators. Like we can we can offer a lot of things.</v>

00:25:00.729 --> 00:25:01.049
<v Juan Martinez>Yeah.</v>

00:25:01.849 --> 00:25:09.769
<v Val Levitan>But recycler is the ideal thing. And our recycler will heavily depend on the price play card from income.</v>

00:25:11.849 --> 00:25:13.769
<v Juan Martinez>On the the.</v>

00:25:15.529 --> 00:25:16.889
<v Juan Martinez>The new one, the new card.</v>

00:25:17.289 --> 00:25:19.609
<v Val Levitan>The new car price, price play, or...</v>

00:25:20.209 --> 00:25:26.249
<v Juan Martinez>No, Prize Play or Prize Pay is the current card. The new card is called Skill Pay.</v>

00:25:27.049 --> 00:25:29.129
<v Val Levitan>Skill pay, okay, skill pay, yeah.</v>

00:25:36.809 --> 00:25:55.809
<v Juan Martinez>So I guess, Felipe, since you're right, it's probably freshest on Andrei's mind. Whenever you took space with him, I would like to know what he actually observed this weekend, because, you know, if that's the direction the market is heading into, then, you know, we just need to start preparing for it.</v>

00:25:56.169 --> 00:26:00.329
<v Juan Martinez>even though we're technically we are already more than halfway there.</v>

00:26:01.529 --> 00:26:18.649
<v Felipe Miranda Giorgi>Yes, yes, sir. Yeah, I will try to find anyway the videos that I took, all the experience, but I know it was posted in Confluence somewhere. I don't know if I can find it, but I had posted everything. I know we spoke about it at some point, but</v>

00:26:22.009 --> 00:26:22.809
<v Felipe Miranda Giorgi>I'll find it.</v>

00:26:23.689 --> 00:26:28.729
<v Juan Martinez>Understand, and when does this place that you just want to go live with Fiery Pay?</v>

00:26:28.569 --> 00:26:31.929
<v Felipe Miranda Giorgi>Well, he told me they might finish up today.</v>

00:26:33.009 --> 00:26:52.329
<v Felipe Miranda Giorgi>But I mean, if I go by myself to, you know, as a player, sure, I can cash out, but I won't be able to enter like I did, you know, the where it's actually issued, how it is connected, everything, and I need that, you know.</v>

00:26:39.129 --> 00:26:39.449
<v Juan Martinez>Yeah.</v>

00:26:53.289 --> 00:26:53.609
<v Juan Martinez>Yeah.</v>

00:26:54.169 --> 00:27:14.849
<v Felipe Miranda Giorgi>Knowledge, maybe. I don't know if it's necessary. I can go by myself, but... And here's the funny, here's the awkward part. This location, I don't think is fit for that system. And I'll tell you why. It's a very big bar. It's a hookah bar. You know, it's more for like...</v>

00:26:58.409 --> 00:26:59.369
<v Juan Martinez>Yeah, no, I mean.</v>

00:27:16.169 --> 00:27:16.729
<v Felipe Miranda Giorgi>Earth.</v>

00:27:17.849 --> 00:27:19.689
<v Juan Martinez>People who smoke marijuana.</v>

00:27:19.689 --> 00:27:39.809
<v Felipe Miranda Giorgi>Yeah, and some, and it's got so many, but more black and vibe, more hip-hop kind of vibe, and ladies wearing short shorts and you know, whatever. And, but the games are all the way down, like all the way down, and the bar is all the way up, like</v>

00:27:39.929 --> 00:27:58.329
<v Felipe Miranda Giorgi>You go up not many stairs, like 5 stairs, but in total, but it is very separate. So you have to go all the way here and say, listen, I need 20, you know, in my gift card and 70 in my machine and I have to run back because it's not, you know, it's not right there. I actually.</v>

00:27:42.849 --> 00:27:43.129
<v Juan Martinez>Yeah.</v>

00:27:55.929 --> 00:28:03.289
<v Juan Martinez>Yeah. And the clientele you just described, that someone would sit in, I would be sitting in the seat next to it.</v>

00:28:02.249 --> 00:28:10.889
<v Felipe Miranda Giorgi>I think I think it's I it's not ghetto. It is kind of a plus, so I don't think though it's, you know, it's gonna be a dangerous place to be, but...</v>

00:28:07.489 --> 00:28:07.849
<v Juan Martinez>Yeah.</v>

00:28:11.849 --> 00:28:25.129
<v Juan Martinez>But I mean, I would say if I just shoved in a $5 bill real quick after I saw someone get up and cash out, then you can take the money. That just seems like a terrible situation, especially with the distance they have to cover.</v>

00:28:18.009 --> 00:28:18.569
<v Felipe Miranda Giorgi>Yeah.</v>

00:28:20.089 --> 00:28:21.049
<v Felipe Miranda Giorgi>Too bad.</v>

00:28:23.049 --> 00:28:23.769
<v Felipe Miranda Giorgi>Yeah, Inna.</v>

00:28:25.529 --> 00:28:33.609
<v Felipe Miranda Giorgi>Exactly. That's why I said, well, that's weird. I mean, for a gas station, maybe if it's right there, but you know, this is long distance.</v>

00:28:33.969 --> 00:28:34.169
<v Juan Martinez>Yeah.</v>

00:28:36.489 --> 00:28:40.489
<v Felipe Miranda Giorgi>Yeah, but let me, let me, let me get with Andrei. I'll ask him to.</v>

00:28:41.529 --> 00:29:06.169
<v Felipe Miranda Giorgi>to give us what he saw there. I'll look for the video and if we want, and I spoke to this guy, Mo Patel. He's like Mike Patel, who is a former president of Gomoa and is very influential. He is his, I think his family member. He's got to be like a family member because he's got, he knows everything about everything.</v>

00:28:46.409 --> 00:28:46.809
<v Juan Martinez>Yeah.</v>

00:29:06.489 --> 00:29:20.169
<v Felipe Miranda Giorgi>And he's not like a regular tech, so he's got to be family, but he said maybe on Sunday we could go for breakfast. I was like, okay, breakfast at a bar, but maybe it's the time they are allowed to work, so.</v>

00:29:06.609 --> 00:29:06.889
<v Juan Martinez>Terra.</v>

00:29:20.449 --> 00:29:21.049
<v Juan Martinez>Sure, sure.</v>

00:29:21.769 --> 00:29:30.489
<v Felipe Miranda Giorgi>is the best time. So we'll see if Sunday I'm able to meet with him for that purpose. Because I want to see the, you know, step by step.</v>

00:29:23.289 --> 00:29:23.609
<v Juan Martinez>Yeah.</v>

00:29:31.649 --> 00:29:32.489
<v Felipe Miranda Giorgi>Experience.</v>

00:29:32.889 --> 00:29:34.729
<v Juan Martinez>Absolutely. That'd be interesting. Yeah.</v>

00:29:34.689 --> 00:29:43.929
<v Felipe Miranda Giorgi>Don't get me wrong, I'm happy to go see, you know, get a beer, see some booty shorts. Yeah, I'll do it during the week, but I want.</v>

00:29:42.729 --> 00:29:46.889
<v Juan Martinez>I was counting on that and then don't forget the blueberry pancakes.</v>

00:29:44.969 --> 00:29:45.769
<v Felipe Miranda Giorgi>Yeah, yeah, yeah.</v>

00:29:47.129 --> 00:29:47.769
<v Felipe Miranda Giorgi>Yeah, yeah.</v>

00:29:49.129 --> 00:29:51.289
<v Felipe Miranda Giorgi>Oh, this is being recorded. I apologize.</v>

00:29:54.329 --> 00:29:55.529
<v Val Levitan>That's why I keep quiet.</v>

00:29:55.769 --> 00:29:56.249
<v Felipe Miranda Giorgi>Yeah.</v>

00:29:56.169 --> 00:29:56.649
<v Juan Martinez>Yeah.</v>

00:29:59.929 --> 00:30:00.409
<v Felipe Miranda Giorgi>Okay.</v>

00:30:04.889 --> 00:30:08.569
<v Val Levitan>So I just got a message from John Hasel.</v>

00:30:05.009 --> 00:30:05.849
<v Juan Martinez>So, Val.</v>

00:30:09.249 --> 00:30:09.409
<v Juan Martinez>Two.</v>

00:30:09.649 --> 00:30:13.449
<v Val Levitan>From income, and he says that the card will be available from mid-September.</v>

00:30:14.409 --> 00:30:15.689
<v Felipe Miranda Giorgi>Wow, okay.</v>

00:30:16.889 --> 00:30:22.329
<v Val Levitan>So that means that we could truly implement the entire thing.</v>

00:30:24.009 --> 00:30:24.729
<v Val Levitan>November.</v>

00:30:25.729 --> 00:30:26.009
<v Juan Martinez>Yeah.</v>

00:30:27.609 --> 00:30:27.929
<v Juan Martinez>Yeah.</v>

00:30:30.249 --> 00:30:31.049
<v Juan Martinez>Makes sense.</v>

00:30:34.609 --> 00:30:39.929
<v Val Levitan>Alright, thank you very much, Ray. I'm not sure that I understand all the landscape, but...</v>

00:30:36.089 --> 00:30:36.729
<v Felipe Miranda Giorgi>Thank you.</v>

00:30:36.529 --> 00:30:37.689
<v Juan Martinez>Thanks, guys. Thank you.</v>

00:30:43.289 --> 00:30:49.129
<v Val Levitan>Yeah, let's, but don't get discouraged when there is an information available, just shoot it our way.</v>

00:30:49.529 --> 00:30:50.809
<v Felipe Miranda Giorgi>Yeah, yes, sir.</v>

00:30:51.849 --> 00:30:55.049
<v Val Levitan>Yeah, I'd like to hear that. I'd like to hear the the.</v>

00:30:52.009 --> 00:30:52.649
<v Felipe Miranda Giorgi>One bit.</v>

00:30:56.409 --> 00:30:57.369
<v Val Levitan>The gossip, you know.</v>

00:30:57.609 --> 00:30:58.249
<v Felipe Miranda Giorgi>Yes, sir.</v>

00:30:58.729 --> 00:30:59.609
<v Val Levitan>Thank you, bye-bye.</v>

00:30:59.929 --> 00:31:00.649
<v Felipe Miranda Giorgi>Okay, goodbye.</v>

00:31:00.009 --> 00:31:00.729
<v Juan Martinez>This guys.</v>

