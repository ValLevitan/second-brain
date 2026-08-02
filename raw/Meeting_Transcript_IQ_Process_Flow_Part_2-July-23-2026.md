# Raw Transcript — Discuss new IQ process flow- Part 2
**Date:** July 23, 2026, 8:38–10:00 AM Eastern
**Summary note:** [[Meeting_Notes_IQ_Process_Flow_Part_2-July-23-2026]]
---
WEBVTT

00:00:03.324 --> 00:00:03.724
<v Val Levitan>Just that.</v>

00:00:05.484 --> 00:00:26.404
<v Andrei Klimovich>Yeah, so regarding the printed tickets from Mother Goose, we should pass by them. So as soon as the Mother Goose receives a cash out request, the printed, the ticket should be printed right away. The same way as ad hoc requests from Mother Goose, like dailies, last 25.</v>

00:00:27.044 --> 00:00:47.604
<v Andrei Klimovich>If the button is pushed on the Mutagus, the system shall print all the requested tickets, and IQ is not blocking this connection in any way. So, as far as I understand, the major unresolved question here is what we do with transactions.</v>

00:00:47.684 --> 00:00:49.124
<v Andrei Klimovich>on IQ level.</v>

00:00:50.284 --> 00:00:50.644
<v Andrei Klimovich>So.</v>

00:00:52.404 --> 00:01:10.004
<v Andrei Klimovich>As we've defined, like there is no escrow option here. So as soon as Mutagus receives a transaction, IQ gets it immediately. So the question is, when the transaction is pending, which means it's not finalized.</v>

00:01:11.284 --> 00:01:12.244
<v Andrei Klimovich>Shall we?</v>

00:01:13.124 --> 00:01:22.804
<v Andrei Klimovich>Also keep it in the cloud, payment hub cloud database. Shall we create this transaction right away and keep it in a pending status?</v>

00:01:23.924 --> 00:01:44.084
<v Andrei Klimovich>So if we do that, the process of this solution is that we are fail proof in case if the physical device IQ is dead and those pending transactions are not lost in a cloud server. So as soon as the IQ is replaced,</v>

00:01:44.404 --> 00:02:01.044
<v Andrei Klimovich>a new one appears in the same location, this device gets all pending transaction from the cloud and they may be completed if they need to be. The disadvantage of this solution is that we are</v>

00:02:00.524 --> 00:02:02.764
<v Val Levitan>But how is, how is that?</v>

00:02:03.724 --> 00:02:05.724
<v Val Levitan>If, if our device is broken.</v>

00:02:06.764 --> 00:02:15.244
<v Val Levitan>and it requires a replacement. There will be many more than 25 transactions going through during the time that we are replacing the device.</v>

00:02:06.964 --> 00:02:07.444
<v Andrei Klimovich>Mhm.</v>

00:02:15.764 --> 00:02:34.724
<v Andrei Klimovich>It's not related to 25 location, sorry, transactions that MutaGoose keeps in the memory. So it works in a different way. Like MutaGoose receives a transaction. If IQ is functional, we can see this transaction. We create it in a Payment Hub Cloud server immediately.</v>

00:02:16.604 --> 00:02:16.924
<v Val Levitan>Okay.</v>

00:02:34.204 --> 00:02:35.884
<v Val Levitan>I, I know.</v>

00:02:35.044 --> 00:02:36.484
<v Andrei Klimovich>So now it exists over there.</v>

00:02:37.724 --> 00:02:41.564
<v Val Levitan>I know, but what I don't understand is how it helps us.</v>

00:02:42.524 --> 00:02:47.244
<v Val Levitan>that when the product is being replaced, it takes, let's say, a day.</v>

00:02:48.124 --> 00:02:48.604
<v Andrei Klimovich>Mhm.</v>

00:02:48.364 --> 00:02:50.364
<v Val Levitan>Let's say it's fast, it's a day.</v>

00:02:53.164 --> 00:02:55.404
<v Val Levitan>So I don't understand how it helps us.</v>

00:02:59.124 --> 00:03:01.444
<v Andrei Klimovich>So, if I understand you...</v>

00:03:02.324 --> 00:03:10.004
<v Andrei Klimovich>Correctly, I mean that within this period of replacement, those tickets will be will have to be proceeded anyways.</v>

00:03:10.284 --> 00:03:14.684
<v Val Levitan>Well, they they are they are following an established procedure.</v>

00:03:16.364 --> 00:03:18.044
<v Val Levitan>So, I mean...</v>

00:03:19.164 --> 00:03:35.324
<v Val Levitan>The whole thing was, or the whole conversation was, do not break a procedure. Do not, sorry, do not break a tradition. And so tradition is to print tickets and then you do something with the tickets.</v>

00:03:27.764 --> 00:03:28.004
<v Andrei Klimovich>Shpak.</v>

00:03:36.444 --> 00:03:55.364
<v Val Levitan>So we're now saying, okay, you guys continue with your tradition. We will also capture the tickets and we will provide you an automated way. So you don't have to physically enter those tickets. We will provide you, we will facilitate.</v>

00:03:56.764 --> 00:04:02.444
<v Val Levitan>a transaction of transferring the ticket value to a card.</v>

00:04:03.564 --> 00:04:12.924
<v Val Levitan>So that kind of, it dances, it matches well with the product definition.</v>

00:04:15.404 --> 00:04:17.084
<v Val Levitan>Okay, we're now saying...</v>

00:04:19.884 --> 00:04:21.084
<v Juan Martinez>If IQ is down.</v>

00:04:20.124 --> 00:04:20.164
<v Val Levitan>Uhh.</v>

00:04:21.644 --> 00:04:30.604
<v Val Levitan>Yeah, well, we're now looking at cases where we're now looking at cases justifying why we want to keep...</v>

00:04:31.724 --> 00:04:34.044
<v Val Levitan>transactions in memory.</v>

00:04:35.644 --> 00:04:49.804
<v Val Levitan>And we're saying, well, we want to keep it in memory because if IQ is down, a replacement is rushed and we have all the transactions. But in the meantime, we didn't break any traditions and they operate the business as they were.</v>

00:04:51.084 --> 00:04:51.884
<v Val Levitan>So.</v>

00:04:53.484 --> 00:05:12.924
<v Juan Martinez>I would say, Val, we offer them a second set of eyes for reconciliation. If we receive one cash out transaction for $50 and then IQ breaks after the fact, they have to pay it the old-fashioned way. Get the Mother Goose ticket,</v>

00:04:54.204 --> 00:04:54.444
<v Val Levitan>Good.</v>

00:05:13.244 --> 00:05:18.604
<v Juan Martinez>Pay it in lottery, pay it in in merchandise or whatever, but now there.</v>

00:05:17.164 --> 00:05:25.004
<v Val Levitan>No, let's say they're not paying it in lottery. They say, come back tomorrow, we'll have a replacement terminal.</v>

00:05:25.564 --> 00:05:26.084
<v Juan Martinez>Okay.</v>

00:05:25.804 --> 00:05:31.884
<v Val Levitan>But the tickets continue generating and we now have, let's say, I don't know, 50 tickets.</v>

00:05:32.444 --> 00:05:32.764
<v Juan Martinez>Right.</v>

00:05:33.564 --> 00:05:51.244
<v Val Levitan>So now we install the new IQ. And obviously, whether it's in memory or not, it's unreliable because we don't know how many tickets went through or how many tickets were generated. So we cannot rely on what's in the cloud.</v>

00:05:52.324 --> 00:06:03.484
<v Val Levitan>So there has to be now a manual reconciliation if you want to enter those tickets into IQ. So, you know, there might be...</v>

00:06:04.684 --> 00:06:12.924
<v Val Levitan>30, 50 tickets generated. So what do you take? You take a pile of these tickets and manually start entering into IQ?</v>

00:06:04.924 --> 00:06:05.524
<v Andrei Klimovich>Mm-hmm.</v>

00:06:15.844 --> 00:06:34.404
<v Andrei Klimovich>Well, yeah, so for those transactions that were in the cloud before the IQ is dead, they still can be automatically released through IQ, because if we have them in the cloud, you would display them on IQ and they can be released.</v>

00:06:34.724 --> 00:06:37.924
<v Andrei Klimovich>Without manual input, but for the rest of tickets.</v>

00:06:38.884 --> 00:06:50.404
<v Andrei Klimovich>that have been generated during the period when IQ was not present. Yes, it now, I mean, yeah, there is no other way other than the manual input.</v>

00:06:54.724 --> 00:07:01.524
<v Andrei Klimovich>Or, or you know, like, no, I'm just thinking out loud, you know, if we don't want to...</v>

00:07:02.724 --> 00:07:20.084
<v Andrei Klimovich>introduce manual input. We can do some kind of a scanner. I mean, maybe take a picture of Mutagus ticket. And IQ through the cloud server can interpret it and create a transaction just in the same way as it does with getting it from Mutagus.</v>

00:07:20.284 --> 00:07:23.404
<v Val Levitan>It is extremely, extremely unreliable.</v>

00:07:24.084 --> 00:07:24.364
<v Juan Martinez>Yeah.</v>

00:07:25.284 --> 00:07:28.844
<v Andrei Klimovich>Um, yeah, I mean, at least...</v>

00:07:29.004 --> 00:07:39.564
<v Val Levitan>The printer, the printer have low ink, some of the digits might be smudged, it might be misinterpreted, the amount might be misinterpreted. It's A dangerous proposition.</v>

00:07:38.524 --> 00:07:38.804
<v Juan Martinez>Yeah.</v>

00:07:39.924 --> 00:07:41.164
<v Juan Martinez>Yeah, that is dangerous.</v>

00:07:41.684 --> 00:07:56.964
<v Andrei Klimovich>I mean, it's definitely technically more complicated than introducing a manual input, but when it comes to the potential errors or fraud, I would say they're more or less equal with manual input.</v>

00:07:57.724 --> 00:08:13.964
<v Val Levitan>So my point is that we should not provide this service because we're opening ourselves up to fraud, to misinterpretation, misjudgment, and a bunch of other things. And that's why I said, unless you have</v>

00:08:15.204 --> 00:08:15.364
<v Andrei Klimovich>Gee.</v>

00:08:15.244 --> 00:08:26.604
<v Val Levitan>an end-to-end infrastructure, we cannot provide these, reliably provide these services. Sorry, reliably and efficiently provide these services, and therefore we're not going to do it.</v>

00:08:27.764 --> 00:08:39.084
<v Val Levitan>This way we have an excuse of, you know, and we don't get ourselves entangled into things that are beyond our control.</v>

00:08:41.644 --> 00:08:46.124
<v Val Levitan>And that's why I said don't keep the memory, don't allow manual entry.</v>

00:08:49.884 --> 00:08:51.324
<v Val Levitan>But I mean...</v>

00:08:53.004 --> 00:09:11.404
<v Val Levitan>We still didn't break their tradition of validating tickets, of generating tickets. They could still continue doing what they're doing. If they want to have an advanced system where we monitor everything on the location, sure, we can do it. But that requires another layer.</v>

00:09:13.884 --> 00:09:33.044
<v Andrei Klimovich>Well, from this point of view, yes, I do agree with you, but let's take this future step when the full JVL setup is present and there is no Mutagus, right? There still can be a situation when our service is down and the cash out transaction is lost.</v>

00:09:34.204 --> 00:09:56.244
<v Val Levitan>Well, okay, first of all, you dramatically minimize this because you could, number one, you could continue keeping transaction on the SMIB. We could put a small memory chip, and I actually think we probably do, and we can remember, I don't know, X number of transactions inside of the machine, and we could have a, and we do have a handshake.</v>

00:09:45.764 --> 00:09:46.244
<v Andrei Klimovich>Mhm.</v>

00:09:56.524 --> 00:10:03.164
<v Val Levitan>between the two programs making sure that package was delivered properly without any corruption.</v>

00:09:56.964 --> 00:09:57.444
<v Andrei Klimovich>Mhm.</v>

00:10:04.124 --> 00:10:22.524
<v Val Levitan>So, no, I don't think it's possible. And another thing, we talked about having a location-based server, local server, that keeps part of memory if host</v>

00:10:23.564 --> 00:10:44.404
<v Val Levitan>disappeared or IQ disappeared. But I don't even think we need it because within production of any sort of flex pay, it could be flex pay, flex recycler, flex dispenser. Here's your second computer on site.</v>

00:10:44.524 --> 00:10:47.164
<v Val Levitan>That could definitely.</v>

00:10:45.644 --> 00:10:46.124
<v Andrei Klimovich>Mhm.</v>

00:10:48.404 --> 00:10:58.844
<v Val Levitan>foolproof the IQ. And so no, I don't think that it's an issue. Actually, I think the system will work quite well.</v>

00:10:56.284 --> 00:10:57.084
<v Andrei Klimovich>Okay, okay.</v>

00:10:59.444 --> 00:11:00.604
<v Andrei Klimovich>Okay, so...</v>

00:10:59.764 --> 00:11:02.524
<v Val Levitan>And there are many ways of improving that system, too.</v>

00:11:03.484 --> 00:11:19.644
<v Andrei Klimovich>So if we are back to this system where, sorry, the setup where we still use a Mutagoose. So you've mentioned that we are competing against Pax. It's our main competitor and IQ should</v>

00:11:18.764 --> 00:11:19.084
<v Val Levitan>Yeah.</v>

00:11:20.524 --> 00:11:24.924
<v Val Levitan>Yes, but I just want to qualify something in this fragment of time.</v>

00:11:25.804 --> 00:11:30.604
<v Andrei Klimovich>In this fragment of time, OK, so in case of packs.</v>

00:11:31.644 --> 00:11:37.484
<v Andrei Klimovich>If something goes wrong with Pax itself or Income Server.</v>

00:11:38.684 --> 00:11:41.404
<v Val Levitan>Forget Income Server, Forget Income Server, Pax.</v>

00:11:39.244 --> 00:11:39.324
<v Andrei Klimovich>Uhh...</v>

00:11:41.884 --> 00:11:48.284
<v Andrei Klimovich>Tax itself. OK, they cannot release the card also, so it's it just cannot do that.</v>

00:11:49.244 --> 00:11:50.364
<v Andrei Klimovich>So...</v>

00:11:50.364 --> 00:11:53.964
<v Val Levitan>And they have to, and they have to get a new packs.</v>

00:11:55.164 --> 00:12:10.524
<v Andrei Klimovich>Yes, and maybe, I don't know, none of us knows, but maybe they do a copy of this ticket, give it to our player and say, get back tomorrow and we will still be able to issue the card, no worries, right? And he goes.</v>

00:12:11.244 --> 00:12:24.924
<v Val Levitan>Yes, because Parks allows manual entry. So the question is, should we allow manual entry? But one of the biggest complaints, even from income, came that</v>

00:12:11.804 --> 00:12:12.244
<v Andrei Klimovich>Scism.</v>

00:12:18.444 --> 00:12:19.484
<v Andrei Klimovich>Correct, I'm.</v>

00:12:26.444 --> 00:12:39.084
<v Val Levitan>facts designed by default is flawed because it allows manual entry. And what they prefer to do is not to have a manual entry because they look at it as a source of fraud.</v>

00:12:40.204 --> 00:13:02.484
<v Val Levitan>So by preventing fraud, we're saying no manual, sorry, a solution for preventing this particular fraud, we're saying no manual entry, only automated entry. But then we're saying, well, if there is automated entry and you print the ticket and then a player goes home and comes back tomorrow, how do you validate this ticket?</v>

00:13:02.764 --> 00:13:03.804
<v Val Levitan>Well, you don't.</v>

00:13:05.164 --> 00:13:25.164
<v Val Levitan>So, and my point was, we don't, and we don't keep the memory, and it's only during the cycle that we temporarily hold the memory while the ticket is validated, and then we do no longer allow anything. Then we don't accept any responsibility for it, and we don't allow this process.</v>

00:13:26.524 --> 00:13:30.844
<v Val Levitan>But then we're also preventing from this particular fraud.</v>

00:13:32.844 --> 00:13:42.844
<v Val Levitan>And listen, the locations may or may not appreciate this, but I can tell you that it looks like the operator, if it explained properly, will appreciate it.</v>

00:13:46.364 --> 00:13:51.964
<v Andrei Klimovich>Yeah, I'm, I agree with you. Let me just drop one more point here, like...</v>

00:13:55.004 --> 00:13:56.284
<v Andrei Klimovich>If IQ.</v>

00:13:55.724 --> 00:14:03.484
<v Val Levitan>I'm actually, I'm actually starting, I'm actually starting to think in a different direction that we never discussed.</v>

00:13:57.164 --> 00:13:57.644
<v Andrei Klimovich>Mhm.</v>

00:14:05.164 --> 00:14:24.644
<v Val Levitan>I'm actually thinking of saying, look, operator, we are going to, in addition to IQ, we are introducing, let's call it for the sake of, I don't have the exact word right now, but let's call it JVL auditor.</v>

00:14:27.164 --> 00:14:32.604
<v Val Levitan>And the reason I'm thinking in this direction, if you guys are familiar with the new trend of...</v>

00:14:35.084 --> 00:14:35.564
<v Val Levitan>AI.</v>

00:14:38.604 --> 00:14:50.684
<v Val Levitan>Prompting is out of scope anymore. Nobody prompts anymore. I mean, the housewives prompt, but the developers don't prompt anymore. They develop agents.</v>

00:14:52.124 --> 00:15:01.804
<v Val Levitan>So, and these agents play a different role. So I'm thinking in the same direction. I'm saying, well, how would I develop my program?</v>

00:15:02.764 --> 00:15:07.004
<v Val Levitan>does not necessarily have to be binary, you know.</v>

00:15:08.484 --> 00:15:27.684
<v Val Levitan>programming program, it could be a business program. So how would I develop my business program if I would become a new, fresh and looking at it? I would develop a second agent. How would they call them? I would call them an auditor, auditor agent. So physically, it's an extremely small box.</v>

00:15:28.764 --> 00:15:42.764
<v Val Levitan>right, that sits and listens on the line all the time. It does not have any displays or anything like this, but it has a full handshake with the IQ. And it sits and memorizes every single transaction.</v>

00:15:43.964 --> 00:15:44.684
<v Val Levitan>All the time.</v>

00:15:46.204 --> 00:15:54.524
<v Val Levitan>It never, it never, it never gets discontinued. It never gets, it never goes away. It has a persistent memory.</v>

00:15:56.364 --> 00:16:07.244
<v Val Levitan>And it remembers everything. And when IQ is connected, it has a handshake with accounting host in the cloud.</v>

00:16:09.324 --> 00:16:17.804
<v Val Levitan>And when IQ is not there and it doesn't see the handshake, all it does, it just continues remembering things. Could remember things for a year.</v>

00:16:19.084 --> 00:16:22.524
<v Val Levitan>IQ finally arrives and there is a massive dump.</v>

00:16:23.404 --> 00:16:26.524
<v Val Levitan>Of everything that happened while, like, you was away.</v>

00:16:27.564 --> 00:16:29.564
<v Val Levitan>Any IQ, doesn't matter which IQ.</v>

00:16:33.484 --> 00:16:40.364
<v Val Levitan>So this way, we practically erase any possibility of anything whatsoever.</v>

00:16:43.004 --> 00:16:59.484
<v Juan Martinez>Yeah, the only problem is when IQ comes back and has at least past 50 transactions, we don't know if the attendant has already created a gift card manually or given lottery tickets.</v>

00:16:57.924 --> 00:16:58.564
<v Val Levitan>We don't.</v>

00:16:59.964 --> 00:17:02.204
<v Val Levitan>We, we don't know, but do we have to?</v>

00:17:04.524 --> 00:17:11.964
<v Juan Martinez>If we want to help the operation, we should say, hey, these things occurred, but we didn't do anything with it.</v>

00:17:12.924 --> 00:17:21.724
<v Val Levitan>Correct. These things occur while we were not in service. Operator, what do you want to do with these things?</v>

00:17:22.124 --> 00:17:22.364
<v Juan Martinez>Right.</v>

00:17:25.044 --> 00:17:39.004
<v Val Levitan>And then leave it to operator. We say we have complete recording. We listened, we listened, we recorded. We didn't act on it because IQ was out of Commission, but we recorded. You have a full audit trail.</v>

00:17:40.084 --> 00:17:59.844
<v Val Levitan>What do you want to do with it? But it's the same as a CFO in the company. The company is running fine, no issues. But it records all of the transactions. At the end of the year, there is a mismatch in the GL. The CFO comes in and gives debit here, credit here, matches the transactions, and moves on.</v>

00:18:00.844 --> 00:18:01.324
<v Val Levitan>Val.</v>

00:18:02.764 --> 00:18:06.524
<v Val Levitan>How would it be possible without an accounting package?</v>

00:18:07.404 --> 00:18:08.364
<v Val Levitan>It would not be.</v>

00:18:09.444 --> 00:18:24.044
<v Val Levitan>You need to create a ledger. So what does this thing do? It creates a ledger. Okay, that is a palatable thing to me and an additional device to sell. And that's a peace of mind for an operator. It could have different sort of...</v>

00:18:25.004 --> 00:18:34.844
<v Val Levitan>It could have an audit trail, it could have different mechanism for reconciliation, different access and password limitations.</v>

00:18:37.804 --> 00:18:38.364
<v Val Levitan>Agreed.</v>

00:18:39.964 --> 00:18:46.604
<v Val Levitan>But that is to me an agent that has the right, the right to exist.</v>

00:18:48.284 --> 00:18:50.604
<v Val Levitan>And it's a logical step to me, but...</v>

00:18:52.804 --> 00:18:58.444
<v Val Levitan>designing this quasi thing that maybe works, maybe doesn't.</v>

00:19:02.124 --> 00:19:02.764
<v Val Levitan>I don't know.</v>

00:19:03.484 --> 00:19:04.124
<v Andrei Klimovich>So...</v>

00:19:05.244 --> 00:19:05.564
<v Andrei Klimovich>Um...</v>

00:19:07.804 --> 00:19:13.884
<v Andrei Klimovich>If we are still in the system with Mutagus, we have this.</v>

00:19:15.324 --> 00:19:31.484
<v Andrei Klimovich>maximum transactional limitation, right? So if there is a jackpot or a big win, whatever, which is more than 1000 K, sorry, $1000. So the question is, how are we handling it right now? We need to come up to the decision.</v>

00:19:32.684 --> 00:19:38.524
<v Val Levitan>Hold on, did you just jump into another conversation or did I miss something?</v>

00:19:40.124 --> 00:19:45.644
<v Val Levitan>Wait, so we left that, we left that undecided, we parked that, and you jumped into another conversation.</v>

00:19:40.524 --> 00:19:41.204
<v Juan Martinez>Are you move?</v>

00:19:47.724 --> 00:19:55.884
<v Andrei Klimovich>I mean like your suggestion about this agent, audit agent, right? You want to discuss it?</v>

00:19:57.004 --> 00:19:57.644
<v Andrei Klimovich>Further.</v>

00:20:00.284 --> 00:20:15.244
<v Val Levitan>Well, we don't have to discuss it further, but I would expect for you to say, look, I'm not prepared to answer that new thing that you just came up with. Let it be parked. But in the meantime, I have another conversation.</v>

00:20:18.604 --> 00:20:19.084
<v Andrei Klimovich>Okay.</v>

00:20:18.684 --> 00:20:19.004
<v Val Levitan>Just.</v>

00:20:23.404 --> 00:20:28.604
<v Andrei Klimovich>So to me it sounds absolutely reasonable and maybe it's...</v>

00:20:30.124 --> 00:20:37.724
<v Andrei Klimovich>As you mentioned previously, it can also be split between those SMIPs. You mentioned that SMIP can remember transactions, right? So...</v>

00:20:38.564 --> 00:20:44.444
<v Val Levitan>SMIB will remember transactions, but will remember transaction per machine.</v>

00:20:45.004 --> 00:20:46.124
<v Andrei Klimovich>Correct, so.</v>

00:20:45.884 --> 00:20:52.764
<v Val Levitan>The auditing, the auditor, let's call it auditor agent or auditor hardware.</v>

00:20:54.364 --> 00:20:58.924
<v Val Levitan>is meant to audit everything that goes through location locally.</v>

00:20:59.964 --> 00:21:01.724
<v Val Levitan>It's a recorder.</v>

00:21:03.724 --> 00:21:05.804
<v Val Levitan>It's A recorder that never shuts off.</v>

00:21:08.364 --> 00:21:21.484
<v Val Levitan>And it synchronizes to the cloud only through other devices. It could either be some sort of a recycler or pay or a dispenser.</v>

00:21:22.364 --> 00:21:24.284
<v Val Levitan>Or, or an IQ.</v>

00:21:26.924 --> 00:21:31.884
<v Val Levitan>But it's not, but it's we we could probably deliver it a minute.</v>

00:21:27.164 --> 00:21:27.884
<v Andrei Klimovich>Yeah, so.</v>

00:21:34.044 --> 00:21:36.444
<v Val Levitan>because it has extremely small...</v>

00:21:38.444 --> 00:21:43.244
<v Val Levitan>capabilities, a small range of capabilities. We could probably deliver it within 30 days.</v>

00:21:46.364 --> 00:21:53.484
<v Andrei Klimovich>Yeah, and it's it resolves the case if one of the snips is dead or the machine is removed by some reason, whatever.</v>

00:21:54.844 --> 00:22:06.604
<v Andrei Klimovich>this agent still contains all the information through the location. And here is my question, like it also starts to sound a little bit like a local server you mentioned previously, because local server can do the same.</v>

00:22:07.644 --> 00:22:13.164
<v Val Levitan>Yes, local local service, local server requires.</v>

00:22:10.524 --> 00:22:10.644
<v Andrei Klimovich>So.</v>

00:22:13.924 --> 00:22:15.084
<v Val Levitan>Problem much more.</v>

00:22:17.204 --> 00:22:22.124
<v Andrei Klimovich>Okay, yeah. And this agent is...</v>

00:22:23.404 --> 00:22:27.964
<v Andrei Klimovich>It just requires a power, it requires a line in, line out.</v>

00:22:28.964 --> 00:22:30.684
<v Andrei Klimovich>And basically, that's it, right?</v>

00:22:32.444 --> 00:22:34.124
<v Juan Martinez>Well, the agent runs in the cloud.</v>

00:22:35.924 --> 00:22:43.644
<v Andrei Klimovich>No, no, we are talking about the physical device, like it should remember it should exist physically in the location.</v>

00:22:41.804 --> 00:22:42.764
<v Val Levitan>Well, it.</v>

00:22:44.124 --> 00:22:47.644
<v Val Levitan>It will need some sort of a basic processor.</v>

00:22:48.684 --> 00:22:58.444
<v Val Levitan>some sort of a basic infrastructure, but I actually think we could probably adopt our...</v>

00:22:49.004 --> 00:22:49.164
<v Juan Martinez>Mm.</v>

00:22:59.604 --> 00:23:02.044
<v Val Levitan>Port that we have.</v>

00:23:03.244 --> 00:23:07.644
<v Val Levitan>Because it our current port even has a lot of memory, I think.</v>

00:23:10.604 --> 00:23:13.724
<v Val Levitan>And we could rent it for, you know, 99 cents a day.</v>

00:23:14.604 --> 00:23:21.404
<v Val Levitan>Here's your peace of mind, an auditor. It records everything. It records everything that goes through.</v>

00:23:23.084 --> 00:23:27.804
<v Val Levitan>And you could rest assured that every single transaction is captured.</v>

00:23:29.884 --> 00:23:36.444
<v Val Levitan>And we could put it actually, it's interesting now that I'm thinking out loud, we could cut the printer.</v>

00:23:38.764 --> 00:23:46.364
<v Val Levitan>Connect, move the goose one end, connect printer the other end. You remove this thing, printer is not connected, you cannot print it.</v>

00:23:56.244 --> 00:23:59.324
<v Andrei Klimovich>OK, so it's like a small box which sits.</v>

00:24:00.284 --> 00:24:07.084
<v Andrei Klimovich>Between in between Mutagus and printer, and when IQ comes to location, it connects to this box.</v>

00:24:08.324 --> 00:24:19.964
<v Val Levitan>Yes, you could think about it as Flex Port. Have you seen Flex Port? Have you seen the board on Flex Port? So it's Flex Port with no display.</v>

00:24:13.804 --> 00:24:14.284
<v Andrei Klimovich>Yes.</v>

00:24:16.124 --> 00:24:16.524
<v Andrei Klimovich>Yeah.</v>

00:24:17.604 --> 00:24:17.804
<v Andrei Klimovich>Yeah.</v>

00:24:21.564 --> 00:24:26.604
<v Andrei Klimovich>And it exists not in the game machine, it exists separately in the location.</v>

00:24:27.004 --> 00:24:29.324
<v Val Levitan>Yes, it it actually.</v>

00:24:28.284 --> 00:24:29.484
<v Andrei Klimovich>So it's like, uh...</v>

00:24:30.684 --> 00:24:32.604
<v Val Levitan>That's a black box as you showed me.</v>

00:24:33.284 --> 00:24:33.764
<v Andrei Klimovich>Mhm.</v>

00:24:34.844 --> 00:24:36.444
<v Val Levitan>It needs needs power.</v>

00:24:39.724 --> 00:24:48.204
<v Andrei Klimovich>So, yeah, this case is, in this case, we have all the transactions that had had been generated.</v>

00:24:50.124 --> 00:24:53.084
<v Andrei Klimovich>In the location and received from Mutagurus.</v>

00:24:55.724 --> 00:24:57.564
<v Andrei Klimovich>When the new machine comes in.</v>

00:24:59.564 --> 00:25:02.044
<v Andrei Klimovich>It plugs in, gets this history.</v>

00:25:03.164 --> 00:25:03.964
<v Andrei Klimovich>Uh, uh.</v>

00:25:05.564 --> 00:25:21.004
<v Andrei Klimovich>Now, as the machine is present, sorry, the IQ is present in this location, we can connect to the server, to the cloud server, to Payment Hub, and we can reconcile all those transactions. So, if we...</v>

00:25:22.844 --> 00:25:29.644
<v Andrei Klimovich>We, obviously, we ignore those transactions that have already been marked as issued.</v>

00:25:30.644 --> 00:25:32.444
<v Andrei Klimovich>Because we have those threads in cloud server.</v>

00:25:32.924 --> 00:25:42.684
<v Val Levitan>Yes, of course, we could provide an operator with a report that says, look, these transactions went through before a breakdown.</v>

00:25:33.404 --> 00:25:33.804
<v Andrei Klimovich>Ohh.</v>

00:25:44.284 --> 00:25:45.804
<v Val Levitan>These transactions.</v>

00:25:47.644 --> 00:25:51.164
<v Val Levitan>Were recorded, but we don't know how they.</v>

00:25:53.164 --> 00:25:59.084
<v Val Levitan>gone through. We don't know how they got paid out, what the ticket was.</v>

00:26:00.124 --> 00:26:00.284
<v Val Levitan>Ah.</v>

00:26:01.564 --> 00:26:09.164
<v Val Levitan>Cashed in or not, we don't know. So you, operator, you decide for every ticket, how do you want to treat it?</v>

00:26:13.684 --> 00:26:13.884
<v Juan Martinez>Yeah.</v>

00:26:16.444 --> 00:26:22.684
<v Val Levitan>This is the only way in my mind how we can offer this sort of service.</v>

00:26:23.844 --> 00:26:29.164
<v Val Levitan>But also an arm length service, like a like a third party auditor.</v>

00:26:30.644 --> 00:26:42.604
<v Val Levitan>where we don't have to make a logical decision on what to do. And then it allows me to stay with my philosophy of don't keep any memory on IQ.</v>

00:26:46.284 --> 00:26:50.524
<v Andrei Klimovich>We are not keeping any memory on the queue. We should not do that in any case.</v>

00:26:50.004 --> 00:26:53.684
<v Val Levitan>Oh, no, no, no, no. Hold on a second.</v>

00:26:55.964 --> 00:26:57.244
<v Val Levitan>I think.</v>

00:26:59.644 --> 00:27:02.284
<v Val Levitan>The edge cases that you presented.</v>

00:27:03.724 --> 00:27:13.164
<v Val Levitan>drove us to thinking that we need to revert back to keeping some data on IQ.</v>

00:27:14.204 --> 00:27:19.884
<v Val Levitan>Well, I mean, we just didn't get there yet in our conversation, but I think we're heading in that direction.</v>

00:27:14.444 --> 00:27:15.084
<v Andrei Klimovich>Not.</v>

00:27:21.004 --> 00:27:24.524
<v Andrei Klimovich>Not IQ, but cloud server. Yeah, cloud server.</v>

00:27:21.164 --> 00:27:23.524
<v Juan Martinez>I thought it was always in the cloud, yeah.</v>

00:27:24.684 --> 00:27:27.404
<v Val Levitan>No, no, no, no, sorry, sorry, sorry, I, sorry.</v>

00:27:35.244 --> 00:27:55.844
<v Val Levitan>No, no, because you're driving towards keeping some local memory, like whatever 25 transactions or whatever you want to keep that some buffer in case IQ is not connecting. And that creates a lot of issues.</v>

00:27:58.604 --> 00:27:59.644
<v Andrei Klimovich>Um, so...</v>

00:28:00.204 --> 00:28:17.884
<v Val Levitan>You would drive me towards the edge cases where you would say, but if we didn't have time to validate and something disconnected, but if we captured last five tickets, but we cannot connect to cloud, what do we do?</v>

00:28:05.684 --> 00:28:05.804
<v Andrei Klimovich>Yeah.</v>

00:28:20.444 --> 00:28:26.604
<v Val Levitan>And we don't know whether those tickets cashed out yet or what. We don't know what to do with them.</v>

00:28:28.604 --> 00:28:32.684
<v Andrei Klimovich>So, yeah, those are different cases, right? So, let's discuss.</v>

00:28:31.404 --> 00:28:36.524
<v Val Levitan>But, but you, no, but you would drive me towards keeping memory on IQ.</v>

00:28:38.284 --> 00:28:52.204
<v Andrei Klimovich>I'm not driving you to anywhere yet, right? So we're discussing it. So which case are we going to discuss right now? So what is the setup? Let's clarify the setting. What is the setup?</v>

00:28:42.204 --> 00:28:43.164
<v Val Levitan>No, OK.</v>

00:28:51.564 --> 00:28:52.364
<v Val Levitan>I am.</v>

00:28:53.804 --> 00:28:55.884
<v Val Levitan>I feel that keeping...</v>

00:28:58.444 --> 00:29:05.644
<v Val Levitan>Transactions in the local memory of IQ is the incorrect.</v>

00:29:08.124 --> 00:29:09.004
<v Val Levitan>Or imp.</v>

00:29:13.164 --> 00:29:14.844
<v Val Levitan>Sorry, I don't know what happened to my camera.</v>

00:29:13.644 --> 00:29:14.284
<v Juan Martinez>Keeping.</v>

00:29:19.484 --> 00:29:23.644
<v Val Levitan>I think that I think that IQ needs to be a...</v>

00:29:19.804 --> 00:29:20.364
<v Juan Martinez>Yeah, I, I...</v>

00:29:27.084 --> 00:29:28.524
<v Val Levitan>Transactional.</v>

00:29:30.364 --> 00:29:30.924
<v Val Levitan>Hop.</v>

00:29:32.524 --> 00:29:34.124
<v Val Levitan>With no memory in it.</v>

00:29:35.404 --> 00:29:37.044
<v Val Levitan>It it's a it's a.</v>

00:29:39.244 --> 00:29:40.924
<v Val Levitan>It's an in-betweener.</v>

00:29:45.724 --> 00:29:47.964
<v Val Levitan>It's a screen that allows you.</v>

00:29:50.204 --> 00:29:53.964
<v Val Levitan>Automation of function, but that's it.</v>

00:29:50.444 --> 00:29:50.964
<v Juan Martinez>Frolov.</v>

00:29:54.604 --> 00:30:12.524
<v Juan Martinez>Shouldn't we have though some sort of temporary memory? Let's just just in this scenario, we get a cash out message from Mother Bruce for $25 and then the building gets hit by lightning and they didn't have IQ on a UPS.</v>

00:30:13.644 --> 00:30:19.644
<v Juan Martinez>we lose the fact that we got that message if we aren't saving it temporarily.</v>

00:30:21.884 --> 00:30:25.484
<v Val Levitan>So, this is this is the start of...</v>

00:30:26.884 --> 00:30:27.004
<v Val Levitan>Um...</v>

00:30:28.284 --> 00:30:39.164
<v Val Levitan>The next case, and then the next case, because if I say yes, we have this memory, memory in transition.</v>

00:30:34.924 --> 00:30:36.084
<v Andrei Klimovich>Good morning. How are you?</v>

00:30:41.324 --> 00:30:44.044
<v Val Levitan>Then, OK, so we have check.</v>

00:30:45.004 --> 00:31:03.684
<v Val Levitan>So then your next question is, so we have five machines and locations in location. There are five players playing simultaneously, each of them cash in at the same time. All of the information for the five winners from the five machines arrive to IQ.</v>

00:31:05.484 --> 00:31:07.324
<v Val Levitan>An IQ goes out of service.</v>

00:31:09.524 --> 00:31:11.324
<v Val Levitan>Do we have them in the memory or not?</v>

00:31:15.884 --> 00:31:18.044
<v Val Levitan>So it's a slippery, it's a slippery slope.</v>

00:31:16.044 --> 00:31:16.524
<v Andrei Klimovich>So...</v>

00:31:19.564 --> 00:31:25.804
<v Val Levitan>So I'm saying that what we should have is a transitional memory.</v>

00:31:26.884 --> 00:31:29.244
<v Val Levitan>That allows to remember.</v>

00:31:30.444 --> 00:31:34.444
<v Val Levitan>Operations during the validation cycle.</v>

00:31:36.364 --> 00:31:47.004
<v Val Levitan>And if invalidation cycle has time, let's say 30 seconds, whatever gets validated within 30 seconds.</v>

00:31:48.284 --> 00:31:59.084
<v Val Levitan>is a valid transaction. If for some reason the validation code did not get back to IQ within 30 seconds, the transaction did not go through.</v>

00:32:03.324 --> 00:32:09.644
<v Val Levitan>no memory, failed. And so we always have validated or failed.</v>

00:32:10.724 --> 00:32:12.924
<v Val Levitan>And that's all, that's all that IQ does.</v>

00:32:15.484 --> 00:32:23.484
<v Juan Martinez>Yeah, but that brings us back to the fact that if we don't have manual, let's say it was a $500 cash out,</v>

00:32:24.644 --> 00:32:33.524
<v Juan Martinez>What does the player, what's the player experience when they say, "Well, we can't print you a card right now, we have to give you..."</v>

00:32:34.604 --> 00:32:37.804
<v Juan Martinez>Lottery tickets, I mean, that that's a bad experience.</v>

00:32:38.124 --> 00:32:49.004
<v Val Levitan>We don't have to, the location doesn't have to give you lottery ticket. The location, in the case of an auditor, a location then could give them a ticket.</v>

00:32:50.124 --> 00:32:59.644
<v Val Levitan>The the IQ could get replaced, the person with the ticket could come back, the auditor will reconnect to.</v>

00:33:02.284 --> 00:33:10.364
<v Val Levitan>The cloud, the accounting host, will get the summary of the transactions and the validation, the ticket, the ticket number.</v>

00:33:11.444 --> 00:33:15.804
<v Val Levitan>When a player presents a ticket under a number that has not been validated.</v>

00:33:17.884 --> 00:33:21.244
<v Val Levitan>It needs to be approved by an operator, but...</v>

00:33:22.164 --> 00:33:29.164
<v Val Levitan>What it facilitates, it facilitates an automated feed into the IQ.</v>

00:33:31.964 --> 00:33:34.284
<v Val Levitan>So we now have a screen of...</v>

00:33:35.724 --> 00:33:44.124
<v Val Levitan>100 transactions that cannot be validated, and an operator overrides each of the transactions.</v>

00:33:46.284 --> 00:34:05.764
<v Juan Martinez>The only problem there, which is the same problem the packs would have, is if the player came back hours later and said, you know what, I'll take lottery tickets. And then the IQ gets replaced and we send a message, you have this pending transaction now just playing on IQ.</v>

00:34:06.364 --> 00:34:07.324
<v Val Levitan>That's what I'm saying.</v>

00:34:07.644 --> 00:34:09.244
<v Juan Martinez>Okay, I just want to clarify that.</v>

00:34:09.564 --> 00:34:19.244
<v Val Levitan>Well, what we're saying is that these are the transactions that we don't know about. An operator has to make a decision what to do with these transactions.</v>

00:34:20.404 --> 00:34:32.844
<v Val Levitan>An operator could say, I did not cash them, these tickets are still outstanding, or I cashed them. These tickets are not outstanding, or these are outstanding and these are not.</v>

00:34:34.924 --> 00:34:40.044
<v Juan Martinez>That what you just described is completely offline and outside of Flex IQ, correct?</v>

00:34:40.844 --> 00:34:56.444
<v Val Levitan>Yes, and I believe that should be delivered to a decision maker saying the IQ was out of service, but we captured these 1,000,000 transactions. What do you want to do? Please reconcile.</v>

00:34:52.844 --> 00:34:55.404
<v Juan Martinez>Yeah, please reconcile, right?</v>

00:35:01.964 --> 00:35:05.324
<v Val Levitan>In my opinion, that's a great, valid service.</v>

00:35:06.484 --> 00:35:12.844
<v Val Levitan>That's a service that an operator would say, yeah, I, you know, great, yeah, I know how to deal with it.</v>

00:35:15.644 --> 00:35:24.604
<v Juan Martinez>Yeah, that part is true, because however they reconciled the Mother Goose tickets today, the same thing would be applied, except now they've got something to bounce it up against.</v>

00:35:26.764 --> 00:35:31.164
<v Val Levitan>And if they say, yeah, those are outstanding, IQ is back functioning.</v>

00:35:32.284 --> 00:35:50.124
<v Val Levitan>We're waiting for those tickets. The guy with the ticket came in and says, okay, ticket one, two, three. So I could enter one, two, three. It pulls up the information on IQ because it takes it from cloud. It knows that operator validated those transactions. We're waiting for them.</v>

00:35:51.804 --> 00:36:02.924
<v Val Levitan>And we could say, great, yeah, it's still outstanding. Do you want to issue a card? An attendant says, issue a card, card dispenses.</v>

00:36:04.444 --> 00:36:05.884
<v Val Levitan>And we have a good cycle.</v>

00:36:08.044 --> 00:36:13.804
<v Val Levitan>But then it satisfies my view that IQ should not keep any memory.</v>

00:36:14.924 --> 00:36:20.604
<v Val Levitan>And it satisfies the overall desire to provide an automated.</v>

00:36:24.444 --> 00:36:26.284
<v Val Levitan>you know, flow of transaction.</v>

00:36:27.484 --> 00:36:37.484
<v Val Levitan>with no manual entry. And let me just be a little more technical. By saying manual entry, I mean outside of a calling ticket number.</v>

00:36:40.724 --> 00:36:43.804
<v Val Levitan>We can recall ticket number, but the information is still...</v>

00:36:45.964 --> 00:36:48.284
<v Val Levitan>Fed out remembered.</v>

00:36:52.044 --> 00:36:52.844
<v Val Levitan>Automatically.</v>

00:36:59.084 --> 00:36:59.484
<v Andrei Klimovich>Um...</v>

00:37:03.004 --> 00:37:10.684
<v Andrei Klimovich>So, do you want us to delay the pilot launch till we have audit box?</v>

00:37:09.724 --> 00:37:10.204
<v Val Levitan>Ohh.</v>

00:37:11.164 --> 00:37:21.724
<v Val Levitan>No, no, why? I mean, you provided me with some edge cases that, you know, may or may not happen, and that's where we're testing one location.</v>

00:37:12.284 --> 00:37:12.764
<v Andrei Klimovich>Okay.</v>

00:37:14.284 --> 00:37:14.924
<v Andrei Klimovich>So.</v>

00:37:23.164 --> 00:37:27.084
<v Val Levitan>We just have to add this auditor.</v>

00:37:29.004 --> 00:37:33.164
<v Val Levitan>into the product roster and and and you know</v>

00:37:34.124 --> 00:37:37.724
<v Val Levitan>develop capabilities and quickly</v>

00:37:38.964 --> 00:37:43.724
<v Val Levitan>implemented. But again, as I said, I don't believe that it's such a big deal.</v>

00:37:46.844 --> 00:37:55.484
<v Andrei Klimovich>So, won't you mind if we will just right now discuss the experience of the setup we will we are going to have on August 1st?</v>

00:37:57.204 --> 00:38:03.324
<v Andrei Klimovich>Because let's discuss what should be changed or if we are good to have the product as it is right now.</v>

00:38:04.644 --> 00:38:05.884
<v Andrei Klimovich>Can we discuss it right now?</v>

00:38:06.524 --> 00:38:06.844
<v Val Levitan>Yeah.</v>

00:38:08.284 --> 00:38:10.524
<v Andrei Klimovich>So, the way it works right now...</v>

00:38:12.764 --> 00:38:25.564
<v Andrei Klimovich>If we don't add any specific changes, IQ is present on the location with Mutagus. Mutagus receives the cash out transaction from game machine.</v>

00:38:26.684 --> 00:38:30.044
<v Andrei Klimovich>IQ gets this transaction immediately.</v>

00:38:31.244 --> 00:38:37.404
<v Andrei Klimovich>and it exists on the IQ only. I'm describing as it works right now, today, okay?</v>

00:38:38.484 --> 00:38:46.844
<v Andrei Klimovich>So it exists on the IQ locally. The cloud server knows nothing about this transaction until it is finalized.</v>

00:38:50.284 --> 00:38:58.284
<v Andrei Klimovich>Operator, sorry, cashier sees this transaction on IQ screen and cachet can either.</v>

00:39:00.604 --> 00:39:02.844
<v Andrei Klimovich>Try to issue an income card.</v>

00:39:04.204 --> 00:39:04.764
<v Andrei Klimovich>Or...</v>

00:39:07.244 --> 00:39:22.844
<v Andrei Klimovich>Here's the fork. So right now, the void button is still present, okay? We've discussed it previously that it should be changed either to print a ticket or whatever. So there is a fork. But right now, the void is still present. So we need to discuss it.</v>

00:39:25.244 --> 00:39:40.684
<v Andrei Klimovich>So you either issue an income card or void it. So if the income card is issued, the transaction is marked as card issued and it is being created in our Payment Hub Cloud server.</v>

00:39:43.164 --> 00:39:44.124
<v Andrei Klimovich>If it's voided.</v>

00:39:45.404 --> 00:39:50.764
<v Andrei Klimovich>It also been created in our Payment Hub Cloud server with voided status.</v>

00:39:52.444 --> 00:39:55.484
<v Andrei Klimovich>In case if IQ.</v>

00:39:56.604 --> 00:39:57.404
<v Andrei Klimovich>Is that?</v>

00:39:59.324 --> 00:40:08.364
<v Andrei Klimovich>and a new IQ is delivered to the location, the new IQ knows nothing about those transactions that have not been preceded.</v>

00:40:11.764 --> 00:40:12.204
<v Andrei Klimovich>Okay.</v>

00:40:13.564 --> 00:40:19.724
<v Andrei Klimovich>So that how it will work starting with August 1st if we do not apply any changes.</v>

00:40:22.444 --> 00:40:37.404
<v Andrei Klimovich>And one more, edge case with maximum win, right? If the transaction is more than 1000 K right now, it will not be proceeded at all. Like you will try to activate income card and it will return you an error.</v>

00:40:38.604 --> 00:40:46.524
<v Andrei Klimovich>So it will be void only or just leave it in a pending status which exists only on the IQ machine only.</v>

00:40:50.204 --> 00:40:52.524
<v Andrei Klimovich>This is the current setup, so...</v>

00:40:53.604 --> 00:40:54.284
<v Andrei Klimovich>Let's.</v>

00:40:55.404 --> 00:41:00.604
<v Andrei Klimovich>Let's apply changes and see how it shall work starting with August 1st.</v>

00:41:17.484 --> 00:41:18.604
<v Val Levitan>You waiting for me?</v>

00:41:20.684 --> 00:41:27.324
<v Andrei Klimovich>I'd really appreciate your vision. How would you expect it to work? Like, from my point of view.</v>

00:41:28.524 --> 00:41:28.804
<v Andrei Klimovich>Um...</v>

00:41:32.364 --> 00:41:47.484
<v Andrei Klimovich>As we've agreed, like we first we need to implement this tickets pass through. It's something that has to be done. Then we need to address this fork, void or issue a card. So void should not exist.</v>

00:41:48.604 --> 00:42:03.164
<v Andrei Klimovich>So you, the only pass is issue a card. You try, you retry, retry, retry, then there should be a button telling, okay, what's the best?</v>

00:42:04.124 --> 00:42:07.324
<v Val Levitan>There's no, there's no button in my for in my vision.</v>

00:42:09.804 --> 00:42:14.124
<v Andrei Klimovich>So like two, three attempts, and if it's not successful, then failed.</v>

00:42:10.124 --> 00:42:10.524
<v Val Levitan>Mine.</v>

00:42:14.764 --> 00:42:15.164
<v Val Levitan>Val.</v>

00:42:15.964 --> 00:42:16.764
<v Andrei Klimovich>Automatically.</v>

00:42:17.724 --> 00:42:17.884
<v Val Levitan>Mm.</v>

00:42:18.924 --> 00:42:24.924
<v Andrei Klimovich>Okay, okay, two, three attempts, and if it's not successful, then it's failed. Got it.</v>

00:42:26.924 --> 00:42:27.004
<v Andrei Klimovich>Uhh...</v>

00:42:29.724 --> 00:42:40.044
<v Andrei Klimovich>If the IQ is replaced immediately, I don't know, like they have the second one somewhere in the warehouse. It knows nothing about those transactions that existed on the previous one.</v>

00:42:40.964 --> 00:42:50.684
<v Val Levitan>What do you mean transaction existed on the previous one? I just want full clarification. I think I know what you're saying, but I want to make sure that it's clear.</v>

00:42:48.364 --> 00:42:48.964
<v Andrei Klimovich>Mm-hmm.</v>

00:42:51.484 --> 00:43:09.884
<v Andrei Klimovich>So IQ is in this location, it works perfectly. It receives 3 transactions, like 3 players hit a cash out button. So now they're on the IQ and it's dead at this moment. I don't know, died, dies, immediately dies, yeah.</v>

00:43:06.284 --> 00:43:08.124
<v Val Levitan>It died, it, it, it died here.</v>

00:43:10.444 --> 00:43:17.484
<v Andrei Klimovich>So you take the second one, you plug it in, and it has no those 3 transactions in the memory. They do not exist.</v>

00:43:16.924 --> 00:43:26.044
<v Val Levitan>That's right, that the the requirement is only those transactions that.</v>

00:43:19.244 --> 00:43:19.484
<v Juan Martinez>Yeah.</v>

00:43:27.484 --> 00:43:32.364
<v Val Levitan>resulted in approved issuance of card.</v>

00:43:33.564 --> 00:43:35.404
<v Val Levitan>Can be retrieved from.</v>

00:43:36.364 --> 00:43:38.284
<v Val Levitan>The host, the cloud server.</v>

00:43:40.604 --> 00:43:43.804
<v Val Levitan>Nothing local is kept in the memory of IQ.</v>

00:43:43.164 --> 00:43:43.444
<v Juan Martinez>Yeah.</v>

00:43:45.604 --> 00:43:58.044
<v Juan Martinez>And that's for security reasons, Andrei, because we don't know if they process those 3 transactions through some other method. So if we bring them back, we could create a duplicate scenario.</v>

00:44:02.044 --> 00:44:04.284
<v Val Levitan>And, and what, what?</v>

00:44:05.364 --> 00:44:14.124
<v Val Levitan>What signifies A transaction is the marriage between the card number and the amount of money and the validation code from income.</v>

00:44:15.964 --> 00:44:18.604
<v Val Levitan>That's what signifies A transaction.</v>

00:44:21.404 --> 00:44:25.084
<v Val Levitan>Nothing else, no in-betweeners, no marginal.</v>

00:44:27.684 --> 00:44:29.244
<v Val Levitan>Very, very, very simple.</v>

00:44:28.204 --> 00:44:28.364
<v Andrei Klimovich>Mm.</v>

00:44:29.884 --> 00:44:33.404
<v Andrei Klimovich>What about failed transaction? Do you want to keep them in a cloud server?</v>

00:44:34.124 --> 00:44:34.444
<v Val Levitan>Ohh.</v>

00:44:35.164 --> 00:44:51.164
<v Andrei Klimovich>No, okay. How do we handle those transactions that exist on the IQ in pending status, but they have not been proceeded? Shall we remove them in once or three days or whatever?</v>

00:44:51.404 --> 00:44:52.524
<v Val Levitan>Remove them from where?</v>

00:44:53.084 --> 00:44:53.804
<v Andrei Klimovich>From Aiku.</v>

00:44:54.844 --> 00:44:57.964
<v Val Levitan>They're not there. They cannot be kept. They're not there.</v>

00:44:58.724 --> 00:45:18.284
<v Juan Martinez>No, but they are there because you have not activated, you haven't tied it to a card. Why would it disappear? What's the trigger mechanism to say that this cash out for $25 because I ran out of cards, I didn't do anything on IQ. The attendant said, oh, oh, I'm out of cards. Just wait.</v>

00:45:19.444 --> 00:45:29.124
<v Juan Martinez>You know, how long do we wait? Or how long do we allow her to wait before we clear that from the screen? And what is the trigger for clearing it from the screen?</v>

00:45:29.964 --> 00:45:30.604
<v Val Levitan>Okay.</v>

00:45:39.764 --> 00:45:51.404
<v Juan Martinez>Because aren't we rank stacking the incoming transactions? Wouldn't the next one come in above it and the next one come in above it? So conceivably you would see several on screen.</v>

00:45:54.044 --> 00:45:55.724
<v Juan Martinez>Is that how it works, Andrei?</v>

00:45:56.124 --> 00:46:00.684
<v Andrei Klimovich>Yeah, yeah, it works and they are automatically sorted by the latest one on the top.</v>

00:46:01.564 --> 00:46:01.724
<v Juan Martinez>Okay.</v>

00:46:02.924 --> 00:46:06.604
<v Juan Martinez>The question is that one on the bottom, how long do we keep it?</v>

00:46:09.724 --> 00:46:11.324
<v Juan Martinez>Because it could get dangerous.</v>

00:46:20.204 --> 00:46:27.324
<v Andrei Klimovich>We can apply a, I don't know, automatic cleanup timeout, like if it exists for three days, we just remove it.</v>

00:46:29.084 --> 00:46:33.244
<v Andrei Klimovich>exists for two days, for one day, I don't know, for 5 minutes, for one hour.</v>

00:46:36.444 --> 00:46:39.564
<v Juan Martinez>Yeah, I mean, I was thinking of an hour myself.</v>

00:46:36.844 --> 00:46:37.564
<v Andrei Klimovich>It can be done.</v>

00:46:40.844 --> 00:46:41.804
<v Juan Martinez>Should be.</v>

00:46:47.044 --> 00:47:03.564
<v Juan Martinez>Yeah, because we got to balance that the same cashier sells you Coca-Cola, cigarettes, and gas. So they could be busy doing other things and they tell the player, please wait, or the player's in line waiting to get to the cashier. So it has to be an allowable time.</v>

00:47:02.844 --> 00:47:08.604
<v Val Levitan>To me, to to me, and I'm shooting off the hip here.</v>

00:47:09.484 --> 00:47:27.164
<v Val Levitan>So to me, it seems like anything we should, if this is the use case, just like you described. So IQ is working, everything is fine, the transaction is legitimate, we captured it. How long do we keep it? I would say for 24 hours.</v>

00:47:17.844 --> 00:47:17.964
<v Andrei Klimovich>Val.</v>

00:47:28.844 --> 00:47:35.804
<v Val Levitan>After 24 hours, and I'll tell you now the procedure, I would allow 48 hours.</v>

00:47:37.084 --> 00:47:39.564
<v Val Levitan>For an operator to resolve it.</v>

00:47:41.564 --> 00:47:44.364
<v Val Levitan>So, if it's not resolved within three days...</v>

00:47:45.324 --> 00:48:00.124
<v Val Levitan>you erase. And that 48 hours of an operator influence starts ticking and then we advise an operator that within next 24 hours we'll erase it, within next 60 minutes we'll erase it unless he acts right now.</v>

00:48:01.164 --> 00:48:04.124
<v Val Levitan>And then we'll notify them those transactions have been erased.</v>

00:48:06.124 --> 00:48:09.164
<v Andrei Klimovich>So, it's seventy-two hours in total, or is it?</v>

00:48:08.124 --> 00:48:14.444
<v Val Levitan>I'm shooting from, I'm shooting from my hip. I'm shooting from my hip. I'm totally okay if I'm wrong.</v>

00:48:15.564 --> 00:48:33.804
<v Andrei Klimovich>Yeah, okay, so there is a timeout, let's say three days, whatever. If we would like to provide a nice service to our customer, we should display a timeout for sure, and we can highlight the dying transaction, trying to drag your attention. Sure. So if it exists for...</v>

00:48:31.324 --> 00:48:31.564
<v Juan Martinez>Right.</v>

00:48:34.124 --> 00:48:43.644
<v Andrei Klimovich>for some time, it also resolves another important edge case with a maximum payout, right? So let me describe it. Okay.</v>

00:48:43.324 --> 00:48:46.044
<v Val Levitan>I have, I have a solution for maximum payout.</v>

00:48:46.764 --> 00:48:47.244
<v Andrei Klimovich>Okay.</v>

00:48:47.964 --> 00:49:00.604
<v Val Levitan>My solution, my proposal, sorry, not solution, my proposal is to treat it exactly one for one, same protocol, how hand pays handled in the casino.</v>

00:49:03.484 --> 00:49:13.244
<v Val Levitan>It is an exclusion. It is a typical transaction that has a very defined steps of what needs to be done. Certain passwords need to be entered.</v>

00:49:15.884 --> 00:49:19.404
<v Val Levitan>We go by the book and we call it hand pay.</v>

00:49:21.484 --> 00:49:28.284
<v Val Levitan>And it only applies to two wins over $1000. Any win over $1000.</v>

00:49:29.964 --> 00:49:34.924
<v Val Levitan>is a hand pay and we apply a hand pay casino procedure.</v>

00:49:37.804 --> 00:49:48.044
<v Juan Martinez>Yeah, yeah, but the caveat here though is in a casino, you can pay them $1200 in cash. We cannot, they cannot pay cash. So</v>

00:49:48.284 --> 00:50:06.524
<v Val Levitan>Of course, we're not saying that we're going to pay in cash, but the procedure is the same, except giving them cash, we're not. But we hand pay, we prepare cards, and we validate the cards, make sure that all three cards in the sum in total are registered to 1 ticket number,</v>

00:50:06.764 --> 00:50:09.004
<v Val Levitan>And the total represents the total.</v>

00:50:11.124 --> 00:50:11.964
<v Val Levitan>Amount one.</v>

00:50:12.844 --> 00:50:14.044
<v Andrei Klimovich>So, we are still issue.</v>

00:50:13.044 --> 00:50:19.644
<v Val Levitan>Of course, it's not a cash transaction, but we enter a different mode of operation.</v>

00:50:13.164 --> 00:50:13.724
<v Juan Martinez>So.</v>

00:50:16.684 --> 00:50:17.324
<v Andrei Klimovich>So.</v>

00:50:21.004 --> 00:50:27.404
<v Val Levitan>And under that different mode of operation, entering an allowable password.</v>

00:50:28.484 --> 00:50:31.644
<v Val Levitan>And there is a there is a report that's associated with it.</v>

00:50:32.604 --> 00:50:38.324
<v Val Levitan>We call it a hand pay, and we go through a procedure, hand pay procedure.</v>

00:50:39.884 --> 00:50:49.204
<v Juan Martinez>So, Andrei, we're saying we're going to support the rollover of multiple cards for a win over $1000. Excuse me, second.</v>

00:50:50.804 --> 00:50:52.644
<v Andrei Klimovich>Yeah, right. So if we are still...</v>

00:50:51.604 --> 00:50:55.444
<v Val Levitan>This is, this is a suggestion. This is a suggestion. I don't have to.</v>

00:50:54.084 --> 00:51:12.884
<v Andrei Klimovich>Yeah, yeah. Let's discuss it. Let's brew some over here. So if we are still issuing cards, it requires this winning amount to be split into transactions which are issuable, sorry, if it's right term or not.</v>

00:50:56.404 --> 00:50:56.644
<v Juan Martinez>Yeah.</v>

00:51:13.284 --> 00:51:31.364
<v Andrei Klimovich>I mean, that can be handled by income. So if it's a transaction of 1,500, it should be split into transactions. One is 1,000, another one is 500. And there should be two cards issued, right? So let's pick up the process, as you call it a handpay.</v>

00:51:33.364 --> 00:51:39.444
<v Andrei Klimovich>This transaction is displayed on the IQ screen and it says 1500. He would like to...</v>

00:51:40.244 --> 00:51:46.484
<v Val Levitan>I'm sorry, I'm just adding context to what you're saying.</v>

00:51:47.444 --> 00:51:48.724
<v Val Levitan>And I'm sorry for interruption.</v>

00:51:50.004 --> 00:52:07.924
<v Val Levitan>I think it requires a different password or a different, I'm going to say not password, but a different sanctioned, validated step. And in my opinion, and we need to consult the market about it,</v>

00:52:09.284 --> 00:52:12.484
<v Val Levitan>I think a message to a decision maker needs to be sent.</v>

00:52:14.484 --> 00:52:16.804
<v Val Levitan>to let's say his mobile phone, SMS.</v>

00:52:17.684 --> 00:52:21.524
<v Val Levitan>He sends back a, yes, go ahead, payout.</v>

00:52:23.124 --> 00:52:32.164
<v Val Levitan>We attach this validation code to the process, we open another screen, and we visually set up total amount.</v>

00:52:34.244 --> 00:52:39.844
<v Val Levitan>2,500. We will issue 3 cards and we'll visually...</v>

00:52:40.964 --> 00:52:46.804
<v Val Levitan>Post 3 cards, and we hold the transaction in escrow, nothing happens, and we say...</v>

00:52:43.364 --> 00:52:43.404
<v Andrei Klimovich>Oh.</v>

00:52:48.164 --> 00:52:56.884
<v Val Levitan>Approve the first card, we get an approval. Approve the second card, we get an approval. Approve the third card, we get an approval.</v>

00:52:58.004 --> 00:53:00.404
<v Val Levitan>And now we say 3 cards are approved.</v>

00:53:01.564 --> 00:53:02.364
<v Val Levitan>Print cards.</v>

00:53:04.884 --> 00:53:12.644
<v Val Levitan>It prints, it actually prints cards. We swipe cards. I don't, I know, I am not familiar with income.</v>

00:53:15.044 --> 00:53:29.444
<v Val Levitan>marriage certificate. I don't know exactly how they do it. So conditional on how income operates, we should marry the transactions accordingly. I understand that income may require an actual</v>

00:53:31.284 --> 00:53:33.284
<v Val Levitan>integration of the card right away.</v>

00:53:33.844 --> 00:53:50.644
<v Andrei Klimovich>That's right. And we've discussed it yesterday with Dmitri and he confirmed that there is no pre-approval process with Uncom, unfortunately. So as soon as we send them a request to issue a card, they either issue it, which means they load the exact amount, or they send us an error.</v>

00:53:48.884 --> 00:53:49.724
<v Val Levitan>I understand.</v>

00:53:51.204 --> 00:54:10.804
<v Val Levitan>I understand. I understand. So if this is the case, then we issue one card and we say remaining amount is 1500. We issue a second card and we say remaining amount is 500. We always have this reconciliation. And at the end, when transaction is finished or partially finished or</v>

00:54:11.124 --> 00:54:31.044
<v Val Levitan>mostly finished, whatever that definition is, we issue a report of hand pay and we send it to the approving party. We're saying, here's, you gave us SMS, you gave us a code to approve it. We've done this with the timestamp and everything else. And here's the result. We were able to do</v>

00:54:14.164 --> 00:54:14.404
<v Andrei Klimovich>The.</v>

00:54:31.084 --> 00:54:46.884
<v Val Levitan>this and this amount is still outstanding because we cannot find the third card or because income is out of service or because we fail to validate. Whatever that report is, it falls under.</v>

00:54:31.204 --> 00:54:31.324
<v Andrei Klimovich>But.</v>

00:54:48.404 --> 00:54:52.644
<v Val Levitan>a specific procedure, hand pay procedure.</v>

00:54:55.764 --> 00:55:15.364
<v Juan Martinez>Yeah, so Andrei, this would mean that to the cashier, this line item on IQ needs to be visually different. If all of the transactions today are blue or green, this one needs to be yellow or red so that they know, hey, don't press this button until you're ready.</v>

00:55:15.524 --> 00:55:30.324
<v Juan Martinez>because there's a process behind it. You know, process the other ones because this one's going to require an approval. It's going to take 10 or 15 minutes for additional time to happen, but we've got to queue them up for the hand pay steps.</v>

00:55:30.884 --> 00:55:48.884
<v Val Levitan>Or hand pay, let's say an operator will say, don't hand pay anything over $2,500. I want to be there. I want to see the guy. I want to look him in the face. I want to take his body temperature and I want to open his eyeballs and look inside.</v>

00:55:50.164 --> 00:55:51.764
<v Val Levitan>I, I don't know what the procedure is.</v>

00:55:53.204 --> 00:55:57.124
<v Val Levitan>But we should give this cycle a different.</v>

00:55:59.764 --> 00:56:07.804
<v Val Levitan>Box, and we need to treat it within that box, and we need to apply a set of rules that an operator feels comfortable with.</v>

00:56:11.044 --> 00:56:21.684
<v Val Levitan>And thus, we have legitimate reason to remove it from the automation, regular automation cycle.</v>

00:56:28.524 --> 00:56:30.324
<v Val Levitan>Juan, how do you feel about this one?</v>

00:56:31.124 --> 00:56:49.284
<v Juan Martinez>That's the process I've lived with most of my life. So no, I think that the fact that we flag any incoming amount greater than $1,000, we treat it special, that triggers the administrator code requirement from the master or whoever.</v>

00:56:50.164 --> 00:57:08.364
<v Juan Martinez>You know, if we color code it differently and through documents and training, the cashier knows, hey, don't press this one until you're ready because it's going to take you longer than the others. There's a small learning curve there, but that then lets us, you know, handle transactions over $1,000.</v>

00:57:08.444 --> 00:57:16.484
<v Juan Martinez>with the added security that the master or location owner has approved it or denied it to say, hey, wait a minute.</v>

00:57:17.044 --> 00:57:32.724
<v Val Levitan>Or an operator has a minimum wage employee who is dumb and only can press a gas button. And so the operator could say, hey, dude, you see the yellow screen? Whenever yellow screen comes up, go on the back and call Bob.</v>

00:57:21.684 --> 00:57:22.004
<v Juan Martinez>Yeah.</v>

00:57:33.524 --> 00:57:34.964
<v Val Levitan>And I want Bob to handle it.</v>

00:57:36.004 --> 00:57:40.404
<v Val Levitan>And if Bob was not around, then the player tell the player to come back when Bob was here.</v>

00:57:43.124 --> 00:57:46.964
<v Val Levitan>But all you have to do is to make sure that yellow screen, you never ******* touch it.</v>

00:57:48.484 --> 00:57:50.484
<v Val Levitan>That's the language that you're gonna hear.</v>

00:57:50.964 --> 00:57:51.244
<v Juan Martinez>Yeah.</v>

00:57:54.004 --> 00:57:57.844
<v Val Levitan>And that's why I'd like to bring it to a different universe.</v>

00:58:01.124 --> 00:58:03.684
<v Val Levitan>It, by the way, gives us a lot of credibility, too.</v>

00:58:05.404 --> 00:58:05.644
<v Juan Martinez>Yeah.</v>

00:58:08.724 --> 00:58:12.004
<v Andrei Klimovich>Okay, so once we are inside this gate.</v>

00:58:13.364 --> 00:58:18.324
<v Andrei Klimovich>We split those transactions into those that can be handled by income.</v>

00:58:19.404 --> 00:58:19.684
<v Juan Martinez>Yep.</v>

00:58:19.924 --> 00:58:21.844
<v Andrei Klimovich>We issue them one by one.</v>

00:58:23.764 --> 00:58:28.004
<v Andrei Klimovich>If one of them failed, the remaining balance.</v>

00:58:29.924 --> 00:58:34.644
<v Andrei Klimovich>is redeemed somehow, I don't know, but we just mark it that it's...</v>

00:58:35.524 --> 00:58:37.524
<v Andrei Klimovich>It's failed, actually.</v>

00:58:36.644 --> 00:58:37.924
<v Juan Martinez>It's open on our side yet.</v>

00:58:39.444 --> 00:58:48.804
<v Andrei Klimovich>Is it opened or failed? Because we have the process discussed previously that if you retry a card issue for three times, it should be marked as failed automatically.</v>

00:58:46.884 --> 00:58:47.284
<v Juan Martinez>Right.</v>

00:58:49.044 --> 00:58:50.564
<v Juan Martinez>Correct, correct. You're right.</v>

00:58:50.644 --> 00:59:07.044
<v Andrei Klimovich>So, the winning of 2500 in this specific scenario may look like 1K issued with income card, 1K issued with one income card, and one for 500 failed.</v>

00:59:03.804 --> 00:59:04.164
<v Juan Martinez>Right.</v>

00:59:08.404 --> 00:59:12.244
<v Andrei Klimovich>And all those 3 transactions, they are linked to the same voucher.</v>

00:59:09.084 --> 00:59:09.564
<v Juan Martinez>Yeah.</v>

00:59:13.324 --> 00:59:19.684
<v Juan Martinez>And I want to clarify, it's not 1000, it's 900 and ninety-eight plus the $2 service fee.</v>

00:59:20.644 --> 00:59:25.124
<v Andrei Klimovich>I'm talking about load, actually, the amount that has been loaded to the cart.</v>

00:59:22.404 --> 00:59:22.724
<v Juan Martinez>Yeah.</v>

00:59:29.244 --> 00:59:30.804
<v Juan Martinez>Yeah, that that is the load amount.</v>

00:59:31.524 --> 00:59:35.844
<v Juan Martinez>You can't load 1000 because you, you, where did you remove the service fee?</v>

00:59:36.724 --> 00:59:43.684
<v Juan Martinez>Each card has a $2 fee, so it would be 998 loaded because you subtract $2 from it.</v>

00:59:44.484 --> 00:59:58.804
<v Andrei Klimovich>Or you can split it into 3 transactions in the way that there will be 1K load, 1K load, and the last one will be not 500, but will be 496, or how much is it?</v>

00:59:59.244 --> 01:00:05.044
<v Juan Martinez>No, but every card has a service charge. We want that charge. We want that money.</v>

01:00:05.764 --> 01:00:10.244
<v Andrei Klimovich>We will get those money. I mean, like the question is where we shall get those money from.</v>

01:00:10.884 --> 01:00:17.444
<v Juan Martinez>I thought we had to apply a service fee to every card generated. That breaks our map model.</v>

01:00:15.844 --> 01:00:16.404
<v Andrei Klimovich>Correct.</v>

01:00:18.244 --> 01:00:32.404
<v Andrei Klimovich>Correct. So let me give you an example. So there is only one transaction, which is $20, right? So when you load it, the player will get 18 and two will be deducted.</v>

01:00:26.324 --> 01:00:26.724
<v Juan Martinez>Yep.</v>

01:00:32.804 --> 01:00:33.364
<v Juan Martinez>Correct.</v>

01:00:34.084 --> 01:00:35.924
<v Andrei Klimovich>So, when you have a transaction of...</v>

01:00:36.924 --> 01:00:42.004
<v Andrei Klimovich>One 1002 dollars, 1000 will be loaded, two will be...</v>

01:00:42.964 --> 01:00:44.084
<v Andrei Klimovich>Deducted as a fee.</v>

01:00:45.684 --> 01:00:50.484
<v Val Levitan>No, $980 will be loaded and then $22 will be loaded.</v>

01:00:53.364 --> 01:00:53.844
<v Andrei Klimovich>Ohh.</v>

01:00:54.404 --> 01:00:58.404
<v Juan Martinez>I know this was a separate transaction for 1000, not not counting the 20.</v>

01:00:58.564 --> 01:01:01.924
<v Val Levitan>No, no, no, no, he says 1002.</v>

01:01:02.884 --> 01:01:03.524
<v Andrei Klimovich>Correct.</v>

01:01:03.764 --> 01:01:14.324
<v Val Levitan>So which triggers 2 transactions. So he's saying one transaction is 1000. Sorry, the first transaction is 1000, and the second transaction is 2.</v>

01:01:07.044 --> 01:01:07.684
<v Andrei Klimovich>Just if you were.</v>

01:01:16.324 --> 01:01:24.884
<v Val Levitan>So, from two, how can you deduct 2? So, I'm saying that no, in this case, the transaction will be 900.</v>

01:01:26.084 --> 01:01:29.044
<v Val Levitan>And the second transaction will be 102.</v>

01:01:30.164 --> 01:01:34.044
<v Val Levitan>So, from 102, you subtract 2 and you give him 100.</v>

01:01:35.284 --> 01:01:43.364
<v Juan Martinez>But I mean, let's for a second, let's not separate the transaction from a card, from a physical card.</v>

01:01:37.324 --> 01:01:39.444
<v Val Levitan>No, you got it. You got it, right?</v>

01:01:40.244 --> 01:01:40.724
<v Andrei Klimovich>Yeah.</v>

01:01:42.884 --> 01:01:45.204
<v Val Levitan>But, Andrei, I answered your question right.</v>

01:01:45.684 --> 01:01:58.724
<v Andrei Klimovich>Yeah, yeah, you're right. And we can split this logic for any type of transaction. We should cut it into pieces that can be redeemed successfully. So the player will not be left with amounts that he cannot redeem.</v>

01:01:55.204 --> 01:01:55.604
<v Val Levitan>Correct.</v>

01:01:59.684 --> 01:02:00.044
<v Val Levitan>Correct.</v>

01:02:02.564 --> 01:02:06.964
<v Val Levitan>The same, the same thing may happen with 2002.</v>

01:02:08.004 --> 01:02:10.004
<v Val Levitan>With 3002.</v>

01:02:12.244 --> 01:02:14.244
<v Val Levitan>Three 1002 needs 4 cards.</v>

01:02:18.084 --> 01:02:19.604
<v Juan Martinez>Why, why is that?</v>

01:02:21.204 --> 01:02:23.204
<v Val Levitan>Because, if you, if you say...</v>

01:02:24.084 --> 01:02:28.044
<v Val Levitan>Split it if the win is $3002.00.</v>

01:02:29.004 --> 01:02:32.564
<v Val Levitan>split it into four wins. First one is 1000.</v>

01:02:33.604 --> 01:02:47.604
<v Val Levitan>Easy. Second is 1000, easy. Third one is 1000, easy. But the 4th one is $2.00 remaining. From $2 remaining, you have to deduct $2 service charge.</v>

01:02:49.524 --> 01:02:54.644
<v Juan Martinez>Plus, the $2 is below the minimum you can imprint on a card, which is $5.</v>

01:02:54.004 --> 01:02:57.284
<v Val Levitan>Plus, plus the $2.00 is below minimum.</v>

01:02:58.964 --> 01:03:00.324
<v Val Levitan>Right, so...</v>

01:03:00.804 --> 01:03:19.604
<v Juan Martinez>Yeah, that's why I think we should just charge, like I said, $998 plus and minus the $2 on card one, $998 minus the $2 on card two. That keeps everything simple. One card, an amount,</v>

01:03:19.204 --> 01:03:24.644
<v Val Levitan>I know, but I know, but what, but what do you do with the $2.00, the last one?</v>

01:03:19.924 --> 01:03:20.964
<v Juan Martinez>and the service fee.</v>

01:03:27.444 --> 01:03:37.684
<v Juan Martinez>Yeah, I was thinking about that. I mean, maybe we, the limit is $1,000 per card, but maybe we come in at a lower amount to make sure there's enough to cover the final card.</v>

01:03:30.844 --> 01:03:31.604
<v Val Levitan>No, stop.</v>

01:03:32.684 --> 01:03:32.844
<v Val Levitan>And.</v>

01:03:38.404 --> 01:03:41.044
<v Andrei Klimovich>So what we do, we create, sorry.</v>

01:03:38.484 --> 01:03:44.964
<v Val Levitan>No, so, so, so the formula, the formula is always the last car cannot be less than $7.00.</v>

01:03:45.844 --> 01:03:46.404
<v Andrei Klimovich>Correct.</v>

01:03:45.924 --> 01:03:46.484
<v Juan Martinez>Correct.</v>

01:03:48.084 --> 01:03:48.604
<v Juan Martinez>Correct.</v>

01:03:52.164 --> 01:03:56.484
<v Val Levitan>And that's a mathematical rule programmingly, very easy to implement.</v>

01:03:52.244 --> 01:03:52.724
<v Andrei Klimovich>Ohh.</v>

01:03:57.524 --> 01:04:04.484
<v Andrei Klimovich>So, the question is, like, how how this authorization will work? I mean, do you want to have kind of...</v>

01:04:06.644 --> 01:04:11.284
<v Andrei Klimovich>PIN code generated automatically by some.</v>

01:04:13.044 --> 01:04:17.124
<v Val Levitan>I think the easiest is to get a cell phone number.</v>

01:04:18.404 --> 01:04:28.244
<v Val Levitan>And there could be a, you know, primary and secondary and get an approval via an SMS code.</v>

01:04:30.244 --> 01:04:35.284
<v Val Levitan>You send them a code, they'll put in the code, and that's the approval.</v>

01:04:36.244 --> 01:04:37.364
<v Andrei Klimovich>So let's play this.</v>

01:04:36.404 --> 01:04:38.724
<v Val Levitan>That's the easiest, that's the easiest way.</v>

01:04:39.444 --> 01:04:41.604
<v Andrei Klimovich>Let's play this in roles; I'll play a sheer.</v>

01:04:40.724 --> 01:04:44.964
<v Val Levitan>And, by the, and by the way, you get their cell number too, which is great.</v>

01:04:46.884 --> 01:05:00.084
<v Andrei Klimovich>Okay, so let's play this in the roles. I'll be a cashier and you will be this Bob. So I have the rule that if something is highlighted in yellow, I do not touch it until I talk to you. So I'm calling you and telling them that there is a transaction for...</v>

01:04:59.164 --> 01:05:05.044
<v Juan Martinez>No, no, no, no. You're calling your boss on property. You're not calling the master.</v>

01:05:06.164 --> 01:05:08.884
<v Juan Martinez>The master's getting the automated text from us.</v>

01:05:06.404 --> 01:05:07.684
<v Val Levitan>Or you calling your call?</v>

01:05:09.124 --> 01:05:11.364
<v Val Levitan>You're calling Bob, so I'm Bob.</v>

01:05:10.924 --> 01:05:11.164
<v Juan Martinez>Yeah.</v>

01:05:12.004 --> 01:05:12.324
<v Juan Martinez>Yeah.</v>

01:05:12.084 --> 01:05:19.844
<v Andrei Klimovich>Yes, I have a very simple, straightforward rule. If it's yellow, I'm calling Bob. I don't know who Bob is. It's just the rule.</v>

01:05:12.724 --> 01:05:13.204
<v Val Levitan>So.</v>

01:05:19.524 --> 01:05:23.764
<v Val Levitan>So, Bob, Bob was the guy at the gas station who, you know...</v>

01:05:19.604 --> 01:05:20.164
<v Juan Martinez>Yes.</v>

01:05:25.204 --> 01:05:28.404
<v Val Levitan>Run something more important than pressing your gas button.</v>

01:05:28.884 --> 01:05:29.124
<v Juan Martinez>Right.</v>

01:05:29.204 --> 01:05:34.244
<v Andrei Klimovich>Yeah, and I'm telling you that there is a transaction for 2500, there is a jackpot.</v>

01:05:29.404 --> 01:05:30.564
<v Val Levitan>I see.</v>

01:05:33.204 --> 01:05:44.884
<v Val Levitan>So, so Bob, no, no, no. So all you do, you call Bob. Bob says, son, move away. And now I'm Bob, I'm in front of the terminal.</v>

01:05:45.764 --> 01:05:51.524
<v Val Levitan>So now I know the procedures, but the procedure is even to Bob is.</v>

01:05:53.684 --> 01:05:59.844
<v Val Levitan>you know, translucent. Bob really doesn't understand what goes on in the back. But in the back.</v>

01:05:58.244 --> 01:05:58.284
<v Andrei Klimovich>Ohh.</v>

01:06:01.044 --> 01:06:06.244
<v Val Levitan>It's sending a message, SMS message to a decision maker.</v>

01:06:07.924 --> 01:06:09.844
<v Val Levitan>So let's say master operator.</v>

01:06:11.524 --> 01:06:13.044
<v Val Levitan>Chief Operating Officer.</v>

01:06:14.724 --> 01:06:22.084
<v Val Levitan>He gets a message on his phone. He says, location, gas station, lucky coin, won a...</v>

01:06:23.204 --> 01:06:25.964
<v Val Levitan>A jackpot of $2500.</v>

01:06:28.004 --> 01:06:30.084
<v Val Levitan>Do you approve handpay?</v>

01:06:31.204 --> 01:06:34.644
<v Val Levitan>So the CFO says, oh, hold on a second, let me call.</v>

01:06:35.924 --> 01:06:53.924
<v Val Levitan>Hey, Bob, are you at the machine now? You're at the location? Yeah, Susie, I'm at the location here. Yeah, I'm looking at the screen. Yeah, $2,500. What should I do? Bob, but is the player in front of you? Yeah, Susie, the player is here standing in front of me right here.</v>

01:06:54.564 --> 01:07:02.484
<v Val Levitan>I know the guy, he's a regular. Oh, okay, Bob, so I'm gonna issue an approval. Let me just give me 30 seconds. Thanks for phone.</v>

01:07:03.764 --> 01:07:09.364
<v Val Levitan>dot SMS and puts in the code that we sent, and the and the message says.</v>

01:07:10.244 --> 01:07:16.484
<v Val Levitan>The code is 1, 2, 3, 4. If you approve it.</v>

01:07:17.364 --> 01:07:22.484
<v Val Levitan>Put this code into reply. So Susie says, one, two, three, 4, send.</v>

01:07:23.844 --> 01:07:33.604
<v Val Levitan>And the terminal that the Bob was standing in front of says the transaction has been approved by the master operator's CFO, Susie Smith.</v>

01:07:36.324 --> 01:07:36.884
<v Val Levitan>And...</v>

01:07:38.324 --> 01:07:44.724
<v Val Levitan>Bob now sees the screen. It says transaction $2,500. We're splitting it into three.</v>

01:07:46.244 --> 01:07:51.524
<v Val Levitan>Cards. Bob, do you have three cards in front of you? Bob says, one second.</v>

01:07:52.884 --> 01:08:04.724
<v Val Levitan>One, two, three. Yes, I do. Presses the button. I do. Okay, we start validating card number one. Card number one, swipe it. Swipe.</v>

01:08:06.244 --> 01:08:09.044
<v Val Levitan>Card number one validated header over to player.</v>

01:08:10.004 --> 01:08:10.444
<v Val Levitan>Peari.</v>

01:08:11.684 --> 01:08:26.564
<v Val Levitan>Now you're validating card #2, transaction $1,000. Card #2 validated, swipe it. Swipe, yeah, validated, check mark, green check mark, fat, fat green check mark. Hand card #2 to the player.</v>

01:08:28.004 --> 01:08:46.644
<v Val Levitan>Got it. Card #3 validated, give it to player. The transaction is completed. It takes the SMS message, sends it to Susie. Susie, your transaction, your approved transaction for handpay dated so and so and such and such hour has been validated.</v>

01:08:44.524 --> 01:08:44.644
<v Andrei Klimovich>Yeah.</v>

01:08:46.804 --> 01:08:46.844
<v Andrei Klimovich>Oh.</v>

01:08:47.364 --> 01:08:51.764
<v Val Levitan>And Bob at the gas station, signature ABC.</v>

01:08:53.284 --> 01:08:58.004
<v Val Levitan>Uh, you know, transacted this transaction and gave away three cards.</v>

01:09:00.644 --> 01:09:03.364
<v Andrei Klimovich>And in case if one of them fails.</v>

01:09:04.564 --> 01:09:09.044
<v Val Levitan>It handed two cards and $500 is still hanging.</v>

01:09:05.444 --> 01:09:06.084
<v Andrei Klimovich>At least.</v>

01:09:10.164 --> 01:09:22.324
<v Val Levitan>You need to dispatch a service call, and you need to revalidate that transaction, and we're keeping it in the memory, and the player was underpaid $500. Same, same as the casino.</v>

01:09:21.484 --> 01:09:24.004
<v Andrei Klimovich>Whoa, whoa, whoa, whoa, wait, sorry, we are not...</v>

01:09:25.124 --> 01:09:31.924
<v Andrei Klimovich>Yes, previously we've discussed like if you retry card issue for three times, you suggested that it's marked as a failed automatically.</v>

01:09:32.564 --> 01:09:33.044
<v Val Levitan>Yes.</v>

01:09:33.684 --> 01:09:35.844
<v Andrei Klimovich>Failed means a terminal state.</v>

01:09:37.204 --> 01:09:38.564
<v Val Levitan>Yes, thank you.</v>

01:09:38.244 --> 01:09:42.164
<v Andrei Klimovich>So 500, 500 case, it's failed.</v>

01:09:41.444 --> 01:09:44.564
<v Val Levitan>Fail, yes, the the player.</v>

01:09:43.524 --> 01:09:44.484
<v Andrei Klimovich>And it can be.</v>

01:09:45.924 --> 01:09:48.164
<v Val Levitan>The player didn't get paid, failed.</v>

01:09:50.324 --> 01:09:51.284
<v Juan Martinez>But there is no.</v>

01:09:50.324 --> 01:09:55.284
<v Andrei Klimovich>And it will never be, it will never be handled by IQ in the current process.</v>

01:09:55.604 --> 01:09:58.004
<v Val Levitan>It will never be handled by IQ. It failed.</v>

01:09:58.884 --> 01:09:59.844
<v Andrei Klimovich>Okay, okay.</v>

01:09:59.524 --> 01:10:02.004
<v Val Levitan>But if you, but if you have an auditor.</v>

01:10:03.284 --> 01:10:14.964
<v Val Levitan>Right? If you have an auditor, then it could be re-automated, because now you have an auditor. It's like having your own CFO agent in the location.</v>

01:10:18.564 --> 01:10:21.564
<v Val Levitan>And actually, the more I think about it, the more I love the product.</v>

01:10:23.844 --> 01:10:25.044
<v Val Levitan>The CFO product.</v>

01:10:30.164 --> 01:10:38.404
<v Andrei Klimovich>If we move a couple steps backwards to the point where Susie approves the transaction.</v>

01:10:40.324 --> 01:10:48.004
<v Andrei Klimovich>Does she approve an exact transaction or it's because the way how we describe it, the transaction gets available for cash out immediately.</v>

01:10:47.044 --> 01:10:47.444
<v Val Levitan>Oh ****.</v>

01:10:48.364 --> 01:10:52.324
<v Val Levitan>She approves a handpay cycle.</v>

01:10:53.044 --> 01:10:55.684
<v Andrei Klimovich>Cycle, what in case if we have two?</v>

01:10:57.204 --> 01:10:59.844
<v Andrei Klimovich>Two jackpots on the screen.</v>

01:10:58.004 --> 01:11:01.604
<v Val Levitan>Sorry, sorry, she, sorry, she approves.</v>

01:11:03.044 --> 01:11:17.604
<v Val Levitan>to pay a jackpot by hand, this jackpot, to pay this jackpot to this player, this jackpot to this player, pay it, execute it by hand.</v>

01:11:19.884 --> 01:11:23.604
<v Andrei Klimovich>Which means that she needs to identify this jackpot.</v>

01:11:25.764 --> 01:11:44.804
<v Val Levitan>Of course, she, I mean, $2500 machine, whatever number, the ticket number, do you authorize that, that jackpot? Not the sum of jackpots, not something obscure, a particular, sorry,</v>

01:11:26.804 --> 01:11:27.284
<v Juan Martinez>Yeah, yeah.</v>

01:11:36.884 --> 01:11:37.284
<v Juan Martinez>Yeah.</v>

01:11:44.844 --> 01:11:45.924
<v Val Levitan>The particular.</v>

01:11:47.924 --> 01:11:55.124
<v Val Levitan>amount, the particular ticket, the particular jackpot, do you authorize it to be handled by hand?</v>

01:11:56.884 --> 01:11:57.044
<v Val Levitan>Okay.</v>

01:11:57.364 --> 01:12:14.564
<v Juan Martinez>Yeah, but just to confirm, when she selects it, the yellow hand pay, she goes and gets Bob. They're both waiting for the top guy to give them the code to enter on IQ to release the transaction, correct?</v>

01:12:14.564 --> 01:12:36.404
<v Val Levitan>Yes, yes, they cannot do anything to the IQ. IQ is idle. The SMS has been sent. We're waiting for Susie Smith, the CFO at this master operator, like a coin company, to validate the transaction. Whatever internal steps they have, whatever they decided on, it might be a phone call.</v>

01:12:36.804 --> 01:12:37.924
<v Val Levitan>It might be a trip.</v>

01:12:39.204 --> 01:12:45.844
<v Val Levitan>It might be whatever, persuasion, maybe they send a, you know, a celebration truck. I don't know what it is.</v>

01:12:46.964 --> 01:12:52.564
<v Val Levitan>But, however they, whatever their measures are, she needs to enter the code.</v>

01:12:53.924 --> 01:13:06.804
<v Val Levitan>She gets the code. She is the only one from that cell phone number that can enter the code. She enters the code, the hand pay on IQ unlocks.</v>

01:13:08.564 --> 01:13:14.244
<v Val Levitan>And now Bob, who stands in front of the IQ, the guy in the gas station.</v>

01:13:15.244 --> 01:13:23.364
<v Val Levitan>Oh, sorry, the guy at the gas station, now he can say, okay, my touch screen now is responding.</v>

01:13:25.004 --> 01:13:44.884
<v Andrei Klimovich>Okay, so how it works in the background, this authorization service needs to get this voucher number, maybe, yeah, probably it's voucher number, it's very simple, from Susie through the SMS. Now he talks to IQ to confirm that this transaction exists over there, sends Susie.</v>

01:13:26.164 --> 01:13:26.724
<v Juan Martinez>Sorry.</v>

01:13:45.724 --> 01:13:53.844
<v Andrei Klimovich>A final confirmation she confirms, and authorization service enables this transaction on IQ to be redeemed.</v>

01:13:54.644 --> 01:13:57.924
<v Juan Martinez>Nothing goes directly to Susie, she's just a cashier.</v>

01:13:58.964 --> 01:14:00.164
<v Val Levitan>No, no, Susie is that.</v>

01:13:59.204 --> 01:14:05.684
<v Andrei Klimovich>No, no, Susie is a CFO, SFO of this couple, Chief CFO.</v>

01:14:01.244 --> 01:14:05.844
<v Juan Martinez>Oh, oh, I'm sorry, I'm sorry. Okay, okay, okay. Yeah, okay.</v>

01:14:03.844 --> 01:14:04.644
<v Val Levitan>CFO, yeah.</v>

01:14:10.124 --> 01:14:10.404
<v Andrei Klimovich>Yeah.</v>

01:14:11.604 --> 01:14:18.004
<v Val Levitan>And again, I think you're trying to engineer a cloud solution right now. So I would leave it to the engineers.</v>

01:14:19.124 --> 01:14:30.084
<v Andrei Klimovich>I'm not engineering, but I'm thinking out loud, so it should be there. Because if we have a system where different actors are, they need to communicate somehow. The way how you...</v>

01:14:29.604 --> 01:14:39.764
<v Val Levitan>But to me, it's Hub that communicates to Susie, and Hub receives the validation number. IQ is dumb. There's nothing in IQ.</v>

01:14:40.244 --> 01:14:40.804
<v Andrei Klimovich>Oh.</v>

01:14:42.084 --> 01:14:43.444
<v Andrei Klimovich>Yes, I mean, like...</v>

01:14:42.324 --> 01:14:54.244
<v Val Levitan>IQ, all IQ does is temporarily displays the transaction, which by the way, could be parked because there are other players, they cash in regular tickets, you know.</v>

01:14:54.964 --> 01:15:12.084
<v Andrei Klimovich>It is parked. It is parked until while they're talking on the phone. Sure, it can be used. I mean, nothing happening on the screen. The only thing that a cashier needs is just to look at the screen and see the voucher numbers. That's it. This voucher number needs to be told to Susie through Bob or whatever it is.</v>

01:15:12.324 --> 01:15:15.084
<v Val Levitan>No, no, no.</v>

01:15:16.084 --> 01:15:22.164
<v Andrei Klimovich>But Susie, again, like if there are two jackpots living on the IQ right now, 2 jackpots, well.</v>

01:15:17.124 --> 01:15:17.524
<v Val Levitan>No.</v>

01:15:22.004 --> 01:15:40.284
<v Val Levitan>No, no, no. Nobody tells Susie anything except Susie's phone gets an SMS from our host. And our host says there are three jackpots at this point. One is for 2000.</v>

01:15:23.284 --> 01:15:23.764
<v Andrei Klimovich>Okay.</v>

01:15:40.564 --> 01:15:43.964
<v Val Levitan>Another one for 3000, and another one for 5000.</v>

01:15:45.164 --> 01:15:46.484
<v Val Levitan>What do you want to do, Susie?</v>

01:15:48.004 --> 01:15:50.804
<v Val Levitan>She says I want to approve the 2000.</v>

01:15:51.804 --> 01:16:02.564
<v Val Levitan>Great. Here's type in this validation code. This validation code approves only the 2000 jackpot. That's it.</v>

01:16:05.804 --> 01:16:13.364
<v Juan Martinez>Okay, so there is no entry at IQ. Susie's press confirmation opens up the terminal to be processed.</v>

01:16:13.044 --> 01:16:16.004
<v Val Levitan>Unlocks, unlocks that jackpot.</v>

01:16:17.284 --> 01:16:19.364
<v Val Levitan>For hands pay moves the.</v>

01:16:18.724 --> 01:16:19.364
<v Juan Martinez>And that's.</v>

01:16:20.444 --> 01:16:41.044
<v Juan Martinez>I was going to say that what Val said though is also very important because Susie, being a CFO, she knows that there's a $5,000 daily limit for the location. So she can approve all three because then income locks us out. So she's approved one and the other players have to come back or be dealt with differently.</v>

01:16:38.324 --> 01:16:38.644
<v Andrei Klimovich>Yes.</v>

01:16:44.564 --> 01:16:49.764
<v Andrei Klimovich>Or she talks to income asking to increase the payout limit for this specific location.</v>

01:16:48.644 --> 01:16:48.964
<v Juan Martinez>Yeah.</v>

01:16:50.124 --> 01:16:50.564
<v Juan Martinez>Correct.</v>

01:16:50.804 --> 01:16:51.764
<v Val Levitan>Temporarily.</v>

01:16:54.644 --> 01:16:59.284
<v Val Levitan>But there is a procedure. There is a procedure, whatever procedure is. Yeah.</v>

01:16:55.044 --> 01:16:57.204
<v Andrei Klimovich>So, right? Yeah.</v>

01:16:58.884 --> 01:17:04.004
<v Andrei Klimovich>So right now it works in the way that IQ needs to send this to Hub immediately.</v>

01:17:04.964 --> 01:17:07.204
<v Val Levitan>IQ says I have a jackpot.</v>

01:17:07.764 --> 01:17:10.004
<v Andrei Klimovich>Yes, and hop candles it.</v>

01:17:10.884 --> 01:17:24.084
<v Val Levitan>Hub knows the rules how to handle it and handles it according to the rules. When rules are executed, somebody up there, a CFO, a president, the manager, you know, a chief huncher.</v>

01:17:13.324 --> 01:17:13.684
<v Andrei Klimovich>Yes.</v>

01:17:16.004 --> 01:17:16.564
<v Andrei Klimovich>Correct.</v>

01:17:20.364 --> 01:17:20.484
<v Andrei Klimovich>Val.</v>

01:17:26.644 --> 01:17:27.524
<v Val Levitan>Gets the code.</v>

01:17:29.044 --> 01:17:47.484
<v Val Levitan>and validates and code is per jackpot, not per location, not a blank location. It's the same as in the slot machine. You could have a bank of machines, you could have three machines, 3 jackpots,</v>

01:17:48.404 --> 01:18:01.604
<v Val Levitan>And for every instant, there is a man, human that walks up to the machine with a key, inserts the key into one machine, turns the key, and enables the hand pay.</v>

01:18:03.124 --> 01:18:06.084
<v Val Levitan>But the other two machines stay locked.</v>

01:18:08.484 --> 01:18:17.684
<v Val Levitan>They're in jackpot mode, they're locked, they cannot be played. Nothing could happen to it. I'm talking about real casino environment.</v>

01:18:20.884 --> 01:18:27.444
<v Val Levitan>So it's one key unlocks each individual jackpot. The same procedure is here.</v>

01:18:29.524 --> 01:18:35.124
<v Val Levitan>So you have your three jackpots on screen listed. Nobody enters anything.</v>

01:18:36.284 --> 01:18:47.364
<v Val Levitan>Hub understands there are three jackpots, sends 3 individual signals, 3 SMS with three different codes. The codes expire within, you know, X amount of time.</v>

01:18:49.124 --> 01:18:56.084
<v Val Levitan>Susie, the CFO, gets the three codes and unlocks or whatever, does whatever procedure she decides.</v>

01:18:56.964 --> 01:18:59.204
<v Val Levitan>On A jackpot per jackpot basis.</v>

01:19:01.724 --> 01:19:06.244
<v Juan Martinez>And we definitely should include the dollar amount of the jackpot in that SMS message.</v>

01:19:05.444 --> 01:19:25.364
<v Val Levitan>Of course, of course we should, we should include the validation ticket number, we should include the location name, the address, maybe I don't know, whatever, whatever suitable information we feel that needs to be included. Yeah, sure. And by the way, it could be SMS, it could be e-mail transaction.</v>

01:19:26.084 --> 01:19:27.524
<v Val Levitan>I prefer SMS.</v>

01:19:27.844 --> 01:19:28.164
<v Juan Martinez>Yeah.</v>

01:19:28.724 --> 01:19:31.364
<v Val Levitan>I overwhelmingly prefer SMS.</v>

01:19:34.324 --> 01:19:37.684
<v Andrei Klimovich>Um, yeah, okay. So what if...</v>

01:19:39.284 --> 01:19:59.364
<v Andrei Klimovich>The next step, let me sum it up and send us, three of us in the chat, this really high level description of the improvements, the changes. So let's review them again, make sure that we're on the same page, and only after that we will unwind it into</v>

01:20:00.324 --> 01:20:04.804
<v Andrei Klimovich>development team in a proper updates for caps and recs.</v>

01:20:05.764 --> 01:20:14.084
<v Val Levitan>Absolutely. And at the same time, I would also recommend to have a basic mention of an auditor as a device.</v>

01:20:15.924 --> 01:20:17.844
<v Andrei Klimovich>Okay, yeah, but...</v>

01:20:16.884 --> 01:20:23.284
<v Val Levitan>So, so at least it it sets it sets uh landscape general landscape.</v>

01:20:22.244 --> 01:20:22.564
<v Juan Martinez>Yeah.</v>

01:20:23.684 --> 01:20:38.884
<v Juan Martinez>And just to avoid persona confusion, can we say auditor agent so we know that it's an artificial, it's not a physical person because that is a physical persona auditor versus an auditor agent?</v>

01:20:23.764 --> 01:20:24.244
<v Andrei Klimovich>Sure.</v>

01:20:40.724 --> 01:20:45.524
<v Val Levitan>Wait, instead of calling it the auditor, I suggest call it the recorder.</v>

01:20:47.084 --> 01:20:54.404
<v Val Levitan>It's just a recorder. It's a dumb recorder. All it does, it sits there and it listens to everything that happens.</v>

01:21:01.044 --> 01:21:01.444
<v Val Levitan>Scism.</v>

01:21:01.484 --> 01:21:04.084
<v Andrei Klimovich>I will, I mean, see if...</v>

01:21:02.324 --> 01:21:10.164
<v Val Levitan>I would call, I would call the agent as a CFO, and the agent goes to the recorder and gets the information.</v>

01:21:11.204 --> 01:21:12.164
<v Andrei Klimovich>Okay, yeah.</v>

01:21:13.364 --> 01:21:21.444
<v Andrei Klimovich>So let me sum it up. Let me drop you this overview today, and if it's all good, then we will do the update.</v>

01:21:25.044 --> 01:21:27.764
<v Val Levitan>Okay, so we generally agree that...</v>

01:21:28.964 --> 01:21:30.324
<v Val Levitan>IQ is.</v>

01:21:31.764 --> 01:21:34.804
<v Val Levitan>In relative terms, speaking is dumb.</v>

01:21:36.244 --> 01:21:37.284
<v Juan Martinez>Long terminal, yep.</v>

01:21:38.244 --> 01:21:38.804
<v Val Levitan>Okay.</v>

01:21:41.084 --> 01:21:43.844
<v Val Levitan>OK, good conversation, productive. Thank you.</v>

01:21:44.924 --> 01:21:45.204
<v Juan Martinez>Sorry.</v>

01:21:45.764 --> 01:21:47.524
<v Andrei Klimovich>Thank you. Talk to you later. Bye.</v>

01:21:45.884 --> 01:21:46.244
<v Val Levitan>What?</v>
