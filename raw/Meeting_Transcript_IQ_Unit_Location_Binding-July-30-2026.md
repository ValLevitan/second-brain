# Raw Transcript — Spec_gaps
**Date:** July 30, 2026, 10:01–10:25 AM Eastern
**Summary note:** [[Meeting_Notes_IQ_Unit_Location_Binding-July-30-2026]]
---
WEBVTT

00:00:07.638 --> 00:00:07.718
<v Andrei Klimovich>The.</v>

00:00:12.118 --> 00:00:13.238
<v Andrei Klimovich>Just the case.</v>

00:00:14.678 --> 00:00:15.318
<v Andrei Klimovich>I will ask you.</v>

00:00:18.478 --> 00:00:22.198
<v Andrei Klimovich>Okay, so please let me know if you can see my screen.</v>

00:00:22.918 --> 00:00:23.478
<v Val Levitan>Yes.</v>

00:00:22.998 --> 00:00:23.398
<v Juan Martinez>Yep.</v>

00:00:24.998 --> 00:00:30.358
<v Andrei Klimovich>Okay, have you had a chance to look through this page?</v>

00:00:32.278 --> 00:00:42.998
<v Andrei Klimovich>Well, do you want me to give you a brief intro on what the question is and what the whole...</v>

00:00:44.118 --> 00:00:45.718
<v Andrei Klimovich>Whole idea is about.</v>

00:00:47.878 --> 00:00:51.398
<v Andrei Klimovich>So, I just, no, no, no.</v>

00:00:52.518 --> 00:00:53.558
<v Juan Martinez>I went through it.</v>

00:00:54.518 --> 00:00:54.758
<v Andrei Klimovich>Right.</v>

00:00:55.878 --> 00:00:56.198
<v Andrei Klimovich>Good.</v>

00:00:57.318 --> 00:01:01.878
<v Juan Martinez>Andrei, is that is somebody speaking in your area? Not here.</v>

00:01:01.158 --> 00:01:07.398
<v Andrei Klimovich>Is it really so loud? Let me switch to my earphones. It should be better. Yeah, because it's...</v>

00:01:08.438 --> 00:01:08.838
<v Andrei Klimovich>Canon.</v>

00:01:10.518 --> 00:01:15.158
<v Andrei Klimovich>Cross the corridor, so actually quite far from here, yeah.</v>

00:01:13.398 --> 00:01:15.958
<v Juan Martinez>Okay, yeah, that's much clearer.</v>

00:01:16.838 --> 00:01:17.318
<v Andrei Klimovich>Okay.</v>

00:01:20.998 --> 00:01:24.038
<v Juan Martinez>Tell those Colombians to quit drinking so much coffee.</v>

00:01:28.198 --> 00:01:29.958
<v Andrei Klimovich>No, I don't want to take this risk.</v>

00:01:30.798 --> 00:01:31.118
<v Juan Martinez>Yeah.</v>

00:01:32.838 --> 00:01:36.678
<v Val Levitan>Colombians are peaceful. It's the Mexicans that you should be worried about.</v>

00:01:37.038 --> 00:01:38.118
<v Juan Martinez>That's true.</v>

00:01:40.278 --> 00:01:40.398
<v Andrei Klimovich>It.</v>

00:01:41.638 --> 00:01:43.158
<v Andrei Klimovich>Yeah, so.</v>

00:01:45.838 --> 00:02:05.598
<v Andrei Klimovich>Basically, the question is, how can we be sure that a specific unit is working at a specific location? Right now, this is being done through our payment hub interface, being done manually, but it does not guarantee anything.</v>

00:01:59.478 --> 00:01:59.878
<v Val Levitan>Music.</v>

00:02:05.878 --> 00:02:06.758
<v Andrei Klimovich>Is just a...</v>

00:02:08.838 --> 00:02:18.918
<v Andrei Klimovich>just to believe someone assigned a specific unit to a specific location and that's it. But we cannot be sure that it's physically in this exact location.</v>

00:02:20.118 --> 00:02:20.518
<v Juan Martinez>Sure.</v>

00:02:21.638 --> 00:02:29.638
<v Andrei Klimovich>And the question is, if we want to track it or we are ready to accept this gap and it's okay, we can live with that.</v>

00:02:21.878 --> 00:02:22.518
<v Juan Martinez>Wow.</v>

00:02:30.038 --> 00:02:34.678
<v Val Levitan>Is this for this rollout or this is for future?</v>

00:02:36.518 --> 00:02:52.838
<v Andrei Klimovich>Well, for this rollout, it will be simple. It's 5 machines maximum for the pilot. We will be sure that it's only one location per operator. We will be in close communication with them. It shouldn't be an issue.</v>

00:02:53.958 --> 00:03:07.078
<v Andrei Klimovich>But if we are talking about a period of three, five months ahead, and we would like the product to be successful, we will have the situation when...</v>

00:03:08.438 --> 00:03:27.758
<v Val Levitan>No, no, no, no, I'm agreeing that it needs to be resolved. I'm just trying to understand, is it how urgent is this resolution? Because sometimes, sometimes you don't have a good thought about it. Or sorry, sometimes you cannot pin a good idea. But if we need to pin it now, it's an issue.</v>

00:03:08.518 --> 00:03:08.998
<v Andrei Klimovich>One of.</v>

00:03:15.238 --> 00:03:16.118
<v Andrei Klimovich>Not.</v>

00:03:27.878 --> 00:03:29.478
<v Val Levitan>But if we need to pin it...</v>

00:03:31.078 --> 00:03:35.558
<v Val Levitan>For future development, I'm sure that there are ways that we could come up with.</v>

00:03:36.438 --> 00:03:38.038
<v Andrei Klimovich>Of course, yeah, so it's not our.</v>

00:03:36.758 --> 00:03:50.358
<v Juan Martinez>And under, I'm sorry, just the process though, we have an onboarding form with income. If JVL has never been in location C,</v>

00:03:51.238 --> 00:04:11.838
<v Juan Martinez>then how can income activate our connection and API to them if we didn't do an onboarding form? And the example you provided, if a unit is moved from location A to location C, well, that location has never been onboarded with JVL.</v>

00:04:12.238 --> 00:04:15.398
<v Juan Martinez>an income, how can it actually even go live?</v>

00:04:16.918 --> 00:04:17.638
<v Andrei Klimovich>It's.</v>

00:04:21.318 --> 00:04:21.518
<v Andrei Klimovich>The.</v>

00:04:23.398 --> 00:04:25.878
<v Andrei Klimovich>It's not exactly the case.</v>

00:04:28.118 --> 00:04:32.518
<v Andrei Klimovich>But let's try to unwind it, actually. Like, what blocks?</v>

00:04:33.998 --> 00:04:34.998
<v Andrei Klimovich>What blocks?</v>

00:04:38.038 --> 00:04:38.438
<v Andrei Klimovich>No.</v>

00:04:43.718 --> 00:04:48.358
<v Andrei Klimovich>What blocks operator from using IQ?</v>

00:04:49.318 --> 00:04:52.518
<v Andrei Klimovich>on the locations that has not been registered with income.</v>

00:04:58.918 --> 00:04:58.958
<v Juan Martinez>Uh...</v>

00:05:01.118 --> 00:05:19.238
<v Juan Martinez>Really, in my opinion, so income used to track locations and I suspect that they got overwhelmed. You know, go back one year, our conversations with them were, hey, we have this onboarding form. It may take up to 36 hours for income</v>

00:05:19.478 --> 00:05:39.558
<v Juan Martinez>to verify that that location has been authorized by GLC to operate a gaming environment. Then Incom said they stopped checking because it was probably such a headache to verify thousands of locations and the illness falls back</v>

00:05:39.638 --> 00:05:56.438
<v Juan Martinez>on the master, the location under penalty from the lottery that you cannot operate this device in an unauthorized location. So, you know, the question is, if we don't, yeah.</v>

00:05:54.598 --> 00:06:09.878
<v Andrei Klimovich>Sorry, Juan, not the device. There is nothing about the device or kiosk or whatever. There is like you cannot issue gift cards at this location, right? So they do not regulate the device itself. It's up to us.</v>

00:06:06.198 --> 00:06:07.118
<v Juan Martinez>Correct, correct.</v>

00:06:09.478 --> 00:06:10.438
<v Juan Martinez>Correct, correct.</v>

00:06:12.198 --> 00:06:12.678
<v Andrei Klimovich>Mhm.</v>

00:06:13.598 --> 00:06:34.118
<v Juan Martinez>Yeah, but it's the same thing. The device does nothing but issue gift cards. You can plug it in, but if it's not fully connected to Incom and it's not, that's what we need to clarify is, can an operator actually move it next door because it was previously registered and operational?</v>

00:06:31.078 --> 00:06:31.638
<v Andrei Klimovich>That's.</v>

00:06:34.358 --> 00:06:35.318
<v Juan Martinez>as a unit.</v>

00:06:36.078 --> 00:07:00.438
<v Andrei Klimovich>Yes, let's try to unwind it. So step one, operator registers location A with JVL for IQ, right? What happens, JVL is sending this specific location A details to income to register it. And this location details include license number,</v>

00:07:00.718 --> 00:07:23.398
<v Andrei Klimovich>address, contact person, et cetera. So income is doing some kind of verification process. We don't know exactly what they are doing, but they send us a reply in a matter of 24, 72 hours that yes, this location can be registered. And here are the secret key details that you need to input.</v>

00:07:04.358 --> 00:07:04.678
<v Juan Martinez>Yep.</v>

00:07:23.798 --> 00:07:30.198
<v Andrei Klimovich>Into your system, when it will talk to us, and we will be sure that this is this specific location.</v>

00:07:31.158 --> 00:07:34.998
<v Andrei Klimovich>So we set up this in a payment hub.</v>

00:07:36.198 --> 00:07:37.398
<v Andrei Klimovich>Location profile.</v>

00:07:38.558 --> 00:07:59.398
<v Andrei Klimovich>So this profile now contains the address, the license number, and those secret keys from income. So each time when IQ is initiating a card issue request to income, we are sending those secret keys details.</v>

00:07:59.558 --> 00:08:07.558
<v Andrei Klimovich>and a specific location information. Income verifies, if it all match, and they can issue the card, there is a success pass.</v>

00:08:08.998 --> 00:08:20.278
<v Andrei Klimovich>But the point is, the whole problem is that IQ basically knows nothing about what location he stands at, except...</v>

00:08:21.398 --> 00:08:25.398
<v Andrei Klimovich>Us manually assigned them to specific location.</v>

00:08:26.318 --> 00:08:26.438
<v Val Levitan>Yeah.</v>

00:08:26.438 --> 00:08:27.158
<v Andrei Klimovich>Do you follow me?</v>

00:08:27.638 --> 00:08:28.278
<v Juan Martinez>Yeah, yeah.</v>

00:08:28.518 --> 00:08:46.038
<v Andrei Klimovich>Yeah, so from IQ as a device, there is no way to verify where I am and if this location is really a location A, but not location B, C, D or whatever, except us menu linking it in a payment hub.</v>

00:08:47.238 --> 00:09:07.638
<v Andrei Klimovich>So, and here is the situation that you have described. Like, we have an operator with two locations. Location A is properly registered. Location B is not verified yet. It's not registered. So they take IQ from location A and move it to location B, connect it to Mutagus.</v>

00:09:09.318 --> 00:09:20.518
<v Andrei Klimovich>And in the system, we still think that this unit is located in location A. So when they will issue a card in location B, there will be a success pass.</v>

00:09:23.718 --> 00:09:43.198
<v Juan Martinez>Okay, I mean, I would take the stance that income did when they stopped verifying these addresses that you as a master, you as a location have agreed to operate lawfully. So if the location is authorized under GLC to do</v>

00:09:43.478 --> 00:09:48.118
<v Juan Martinez>Dysfunction, then so be it, because aren't we still going to bill?</v>

00:09:49.398 --> 00:10:07.158
<v Juan Martinez>Because every time a card is created, we know about it, income knows about it, and we generate a bill. Now what that bill might go to the wrong address, but it's going to go to the right e-mail. Does it really matter? It's not like they're avoiding the service fees.</v>

00:10:11.438 --> 00:10:30.038
<v Andrei Klimovich>It's a business question. I don't know. That's why I'm raising it. If it's a problem for us, or we can live with that. So yes, the card physically issued at location B will be billed to location A. It will appear in the invoice, which is sent to location A.</v>

00:10:31.078 --> 00:10:39.478
<v Juan Martinez>Right, right. And if the customer disputes it, then we're like, hey, no, you must have moved this device without our knowledge.</v>

00:10:38.438 --> 00:10:42.998
<v Andrei Klimovich>We, we, we don't know that, I mean, like, we don't know that.</v>

00:10:42.118 --> 00:10:45.238
<v Juan Martinez>No, no, if they dispute, if they dispute.</v>

00:10:47.878 --> 00:11:04.998
<v Andrei Klimovich>So this is one side of the question. And another side of the question is if it really should be done like that, when we manually bind a unit to a location, or maybe it should be done in semi or full automatic way. So when you connect,</v>

00:11:06.078 --> 00:11:18.118
<v Andrei Klimovich>connect a unit to a motor goose environment, there will be some kind of binding procedure which will be done by operator, but not by us.</v>

00:11:19.398 --> 00:11:23.478
<v Andrei Klimovich>So I've also described it here, like there are different ways how we can do that.</v>

00:11:25.078 --> 00:11:36.198
<v Andrei Klimovich>So what manual approach is being done right now? It requires us as JVL to know explicitly where this unit will go, if it will be location A, B, C, or D.</v>

00:11:37.158 --> 00:11:38.438
<v Andrei Klimovich>So, we will bind it.</v>

00:11:37.358 --> 00:11:37.838
<v Juan Martinez>Mhm.</v>

00:11:39.798 --> 00:11:53.158
<v Andrei Klimovich>Another approach, when we put it on the shoulder of operators, it removes this issue. So we just send them units, and they distribute those units by different locations in the way they want.</v>

00:11:53.958 --> 00:11:54.398
<v Juan Martinez>Correct.</v>

00:11:54.998 --> 00:11:58.158
<v Val Levitan>I like, I like the second one better.</v>

00:11:59.558 --> 00:12:18.518
<v Juan Martinez>Yeah, because that follows what they do with our machines today. Many operators pick up the machine and move it to another location, assign it a new co-MID, and it's all unbeknownst to us. We're unaware of where a machine that we sold two years ago is actually operating at.</v>

00:12:03.398 --> 00:12:03.878
<v Andrei Klimovich>Mhm.</v>

00:12:14.998 --> 00:12:15.318
<v Andrei Klimovich>Pavel.</v>

00:12:19.558 --> 00:12:22.278
<v Val Levitan>Well, I mean, in this case, we will know.</v>

00:12:24.038 --> 00:12:37.318
<v Val Levitan>Yeah, I mean, pretty, you know, Pavel Pavel says it's not reliable, but from my experience, it's pretty reliable. The moment you have an LTE modem, the triangulation is quite good.</v>

00:12:39.878 --> 00:12:48.838
<v Juan Martinez>Yeah, but that implies, you know, somebody actually having to check that. I guess the bigger question is, do we care? Do we really care?</v>

00:12:40.118 --> 00:12:40.758
<v Andrei Klimovich>Ohh.</v>

00:12:46.198 --> 00:12:46.678
<v Val Levitan>Well...</v>

00:12:49.798 --> 00:12:54.598
<v Val Levitan>Well, we, number one, even if we care, I don't think we should care.</v>

00:12:55.238 --> 00:12:55.478
<v Juan Martinez>Right.</v>

00:12:57.878 --> 00:13:08.358
<v Val Levitan>Actually, I think it's better for us not to care. However, the LTE modem does provide this.</v>

00:13:09.718 --> 00:13:14.678
<v Val Levitan>information and I think that quietly we should probably listen to it.</v>

00:13:15.878 --> 00:13:17.638
<v Juan Martinez>Yeah, oh, agreed, agreed.</v>

00:13:18.038 --> 00:13:24.438
<v Val Levitan>Also, I think that it's quite the two things combined.</v>

00:13:26.598 --> 00:13:36.438
<v Val Levitan>are even more reliable, which is the triangulation of the LTE modem plus the serial number of the Mother Goose.</v>

00:13:37.958 --> 00:13:39.078
<v Val Levitan>Internal system.</v>

00:13:40.998 --> 00:13:41.798
<v Juan Martinez>Right, yeah.</v>

00:13:42.998 --> 00:14:02.758
<v Juan Martinez>Yeah, because I mean, Andrei today in Georgia and Felipe can verify this. Locations are bought and sold on a weekly basis. The larger master buys out the smaller master. And, you know, the master selling may say, oh, you know what? I love Flex IQ. That's not included in the deal. I'm taking it with me.</v>

00:14:02.998 --> 00:14:17.558
<v Juan Martinez>That's a very, very possible scenario. And from the customer's perspective, hey, I signed a master agreement, the unit is working, why shouldn't I be able to plug it in at my new location? And it just works.</v>

00:14:18.198 --> 00:14:29.878
<v Andrei Klimovich>Well, yeah, sure. This should be done only in case if this location is registered with JVL. If you don't know anything about this location, it will not work.</v>

00:14:26.278 --> 00:14:26.838
<v Juan Martinez>Right, right.</v>

00:14:30.918 --> 00:14:43.798
<v Juan Martinez>Right. The only the only concern I have is our master agreement and our sales agreement are going to say this deal was done for location A.</v>

00:14:31.398 --> 00:14:31.558
<v Andrei Klimovich>Uh...</v>

00:14:44.318 --> 00:14:44.958
<v Andrei Klimovich>Mhm.</v>

00:14:45.158 --> 00:14:53.718
<v Juan Martinez>If, if, if a master didn't want to pay is saying, "Ohh, I I sold that location, I'm not in there, you're billing, you're billing the wrong guy."</v>

00:14:54.798 --> 00:15:11.678
<v Juan Martinez>What legal claim do we have to go after them if we have a contract that says this was negotiated for the Mobil gas station and now the unit is at an Exxon gas station 5 miles away? You know, do we have...</v>

00:15:10.758 --> 00:15:19.478
<v Val Levitan>We have legal, we have legal claim, but in order for a legal claim to stand, I mean the legal claim will stand.</v>

00:15:21.478 --> 00:15:35.638
<v Val Levitan>The problem will be is to enforce collection. So if an operator doesn't have any assets, even if you win your legal bottle and the claim will be awarded to you, who do you collect from?</v>

00:15:26.118 --> 00:15:26.278
<v Juan Martinez>Right.</v>

00:15:36.318 --> 00:15:36.598
<v Juan Martinez>There.</v>

00:15:36.918 --> 00:15:41.798
<v Val Levitan>On a large scale, if the company is above...</v>

00:15:44.598 --> 00:15:47.798
<v Val Levitan>Uh, sorry, if if it's a legitimate transaction.</v>

00:15:48.878 --> 00:15:53.478
<v Val Levitan>And when a credit is given to an operator, it should be registered against the title.</v>

00:15:54.438 --> 00:15:58.198
<v Val Levitan>And if it's registered against the title, you cannot simply sell a company.</v>

00:15:54.518 --> 00:15:54.838
<v Juan Martinez>Yeah.</v>

00:15:59.318 --> 00:16:01.718
<v Val Levitan>So, if a company undertakes...</v>

00:16:03.438 --> 00:16:06.518
<v Val Levitan>A loan of any sort that should be registered on title.</v>

00:16:10.078 --> 00:16:11.318
<v Val Levitan>Which is not a...</v>

00:16:13.038 --> 00:16:16.118
<v Val Levitan>difficult procedure. I think it's actually fully automated now.</v>

00:16:17.558 --> 00:16:27.158
<v Val Levitan>So, when we when we sell when we sell product to an operator A, it is proper for us to register it against the company's title.</v>

00:16:30.118 --> 00:16:30.598
<v Andrei Klimovich>Mhm.</v>

00:16:30.678 --> 00:16:31.078
<v Juan Martinez>But...</v>

00:16:32.278 --> 00:16:33.958
<v Juan Martinez>We do that with machines, Val.</v>

00:16:34.918 --> 00:16:36.438
<v Val Levitan>We don't currently.</v>

00:16:37.238 --> 00:16:39.558
<v Val Levitan>But should we? We should.</v>

00:16:40.918 --> 00:16:41.198
<v Juan Martinez>Yeah.</v>

00:16:41.958 --> 00:16:59.798
<v Val Levitan>The question is, the moment you registered something, what will the operator say? The operator will immediately say, oh, God, you know, discharge the title. And we're going to say, how can we discharge a title if you owe us money? An operator says, you know, you are, you know,</v>

00:16:50.918 --> 00:16:51.238
<v Juan Martinez>Yeah.</v>

00:16:54.918 --> 00:16:55.238
<v Juan Martinez>Yeah.</v>

00:17:01.398 --> 00:17:14.038
<v Val Levitan>you are in my way and you know, I'm not going to buy from you. And then you're going to say, oh, you're not going to buy from me. Then, you know, I'm better remove the title. Sorry, registration against the title. So it's a thin ice.</v>

00:17:09.998 --> 00:17:10.278
<v Juan Martinez>Yeah.</v>

00:17:13.398 --> 00:17:13.718
<v Juan Martinez>Yeah.</v>

00:17:14.678 --> 00:17:31.958
<v Juan Martinez>Yeah. Plus, we also, Andrei, we had a conversation with Incom. I mean, there's a decommission process, right? Where we're supposed to alert them if a kiosk or IQ POS device is being taken out of service.</v>

00:17:34.198 --> 00:17:36.838
<v Val Levitan>Well, that, that, that is not difficult.</v>

00:17:38.038 --> 00:17:54.358
<v Val Levitan>Because the only way we will know that it's decommissioned is, number one, somebody advise us of decommissioning. Or #2, there is a new device that will be registered, our device that is registered at the same location. Otherwise, we don't know.</v>

00:17:51.878 --> 00:17:52.118
<v Juan Martinez>Right.</v>

00:17:55.478 --> 00:17:55.798
<v Juan Martinez>Right.</v>

00:17:56.118 --> 00:17:58.918
<v Val Levitan>We just think that device has zero revenue.</v>

00:18:00.278 --> 00:18:00.598
<v Juan Martinez>Yeah.</v>

00:18:07.198 --> 00:18:26.038
<v Juan Martinez>Yeah, because without the decommissioning step, I mean, you know, worst case scenario, somebody could be using this device, Flex IQ, at their house and encoding cards and selling them for, you know, less than whatever they've encoded on them for profit. I mean, it...</v>

00:18:26.918 --> 00:18:27.478
<v Juan Martinez>You know.</v>

00:18:28.998 --> 00:18:31.158
<v Juan Martinez>It's a potential source of theft, too.</v>

00:18:34.718 --> 00:18:35.358
<v Andrei Klimovich>Mm-hmm.</v>

00:18:42.198 --> 00:18:58.438
<v Val Levitan>I'm not really worried about it because, sorry, I don't mean to say I'm not worried about this case. I am worried about this case, but I'm not particularly worried about all of these issues because usually life has its way of</v>

00:18:59.558 --> 00:19:11.318
<v Val Levitan>steering the solution and right now it's not important. So, and this is one of the reasons I asked, do we need it for today or do we need it for tomorrow?</v>

00:19:13.158 --> 00:19:31.478
<v Val Levitan>We need to get on locations, we need to start getting real life cases. Real life cases will help us resolve a lot of issues. Right now, you could guess this way, guess the other way, but in reality, we don't have experience. And until we start getting this experience,</v>

00:19:32.038 --> 00:19:32.278
<v Juan Martinez>Right.</v>

00:19:32.358 --> 00:19:35.398
<v Val Levitan>Everything else is just guessing work.</v>

00:19:36.678 --> 00:19:40.278
<v Val Levitan>And for these five machines roll out, it's not that important.</v>

00:19:41.958 --> 00:19:51.638
<v Andrei Klimovich>Yeah, I agree. Okay, so let's park it for now. Let's get the data from the fields and see, and we can return back to this issue later.</v>

00:19:43.638 --> 00:19:43.798
<v Juan Martinez>Yes.</v>

00:19:52.598 --> 00:19:55.158
<v Val Levitan>I think so. It's the only way to handle it properly.</v>

00:19:57.238 --> 00:20:05.478
<v Val Levitan>I don't believe that you can really engineer a solution because you're trying to engineer something without exposure to a problem.</v>

00:19:57.318 --> 00:19:57.878
<v Andrei Klimovich>OK.</v>

00:20:06.838 --> 00:20:21.478
<v Val Levitan>And so you're going to be engineering all kinds of solution in a vacuum. And that's a dangerous thing to do. You're going to be spinning around, spinning around, and over-engineer a product that maybe is not required.</v>

00:20:10.278 --> 00:20:10.398
<v Andrei Klimovich>Yeah.</v>

00:20:25.158 --> 00:20:26.158
<v Andrei Klimovich>Okay, agreed.</v>

00:20:28.358 --> 00:20:36.518
<v Andrei Klimovich>Yeah, so the current solution, which is not perfect, but it allows us to launch pilots without any issues. So we can stick to it.</v>

00:20:35.718 --> 00:20:55.358
<v Val Levitan>And our focus and these conversations, we shouldn't book our time wasting our time on anything, but getting into a pilot run. We need a pilot run. And the sooner we get there, the sooner we will resolve a lot of issues.</v>

00:20:57.238 --> 00:21:06.598
<v Andrei Klimovich>Yeah, I already have the rewired cable for these solutions that we came up yesterday for a direct connection, so I'll test it right away. I'll let you know.</v>

00:20:58.598 --> 00:20:58.718
<v Val Levitan>Yeah.</v>

00:21:08.598 --> 00:21:11.558
<v Val Levitan>This is what's important. Let's get...</v>

00:21:13.798 --> 00:21:16.198
<v Val Levitan>Let's install locations.</v>

00:21:17.558 --> 00:21:26.518
<v Val Levitan>For example, one thing that is in my mind is, do we need a minimum monthly payment?</v>

00:21:28.918 --> 00:21:29.958
<v Val Levitan>I think we do.</v>

00:21:31.558 --> 00:21:43.078
<v Val Levitan>an operator could get our unit, pay us, I don't know, 500 bucks with all the discounts and then park it and we never make a penny on it.</v>

00:21:44.238 --> 00:21:49.318
<v Val Levitan>But that's really not a good thing for us. So we should probably have...</v>

00:21:50.358 --> 00:21:53.478
<v Val Levitan>Something like $10 a month minimum charge.</v>

00:21:56.438 --> 00:22:02.118
<v Val Levitan>I don't know whether it's $10 or $100. I don't know, but a minimum charge of some sort.</v>

00:22:04.358 --> 00:22:06.998
<v Val Levitan>So yeah, a lot of these issues will surface.</v>

00:22:07.838 --> 00:22:08.318
<v Andrei Klimovich>Mhm.</v>

00:22:09.558 --> 00:22:13.398
<v Val Levitan>We need to start operating without commitments, without...</v>

00:22:16.518 --> 00:22:18.918
<v Val Levitan>Opening our hand or showing our hand.</v>

00:22:20.358 --> 00:22:20.758
<v Juan Martinez>Green.</v>

00:22:22.518 --> 00:22:30.038
<v Juan Martinez>Andrei, are any of the other apps preventing the pilot?</v>

00:22:32.278 --> 00:22:32.678
<v Juan Martinez>Okay.</v>

00:22:32.758 --> 00:22:43.238
<v Andrei Klimovich>Well, the main blocker I would say right now is this production environment that I'm trying to get from income. I'm pushing them, but...</v>

00:22:41.558 --> 00:22:42.278
<v Juan Martinez>Yes, yes.</v>

00:22:42.838 --> 00:22:43.238
<v Val Levitan>She.</v>

00:22:44.958 --> 00:22:49.798
<v Andrei Klimovich>Until we test it on a production environment, I don't feel comfortable about releasing.</v>

00:22:50.598 --> 00:22:53.798
<v Val Levitan>Yes, yeah, and that should be the push.</v>

00:22:55.638 --> 00:23:02.358
<v Andrei Klimovich>Yeah, so I followed up yesterday again. I don't know, maybe I'll follow up today so I can push them every day.</v>

00:23:03.798 --> 00:23:04.598
<v Val Levitan>Absolutely.</v>

00:23:04.118 --> 00:23:21.238
<v Andrei Klimovich>That's the process, unfortunately. Okay. So, yeah, okay, let's park it. It's written. It will not slip from our radar. Let's get back to it later when we have more knowledge from the real environment.</v>

00:23:23.398 --> 00:23:23.958
<v Val Levitan>Okay.</v>

00:23:23.638 --> 00:23:26.678
<v Andrei Klimovich>Thank you. Thank you for your attention. I really appreciate this.</v>

00:23:25.078 --> 00:23:25.318
<v Val Levitan>Okay.</v>

00:23:26.398 --> 00:23:27.318
<v Val Levitan>Thank you, bye bye.</v>

00:23:27.518 --> 00:23:28.278
<v Juan Martinez>Thank you, bye-bye.</v>
