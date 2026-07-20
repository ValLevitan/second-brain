**Transcript**

July 31, 2025, 12:03PM

**Val Levitan** started transcription

**Nathan Carver**   0:04  
Wanna share some links here for.  
Documents I added to the.  
Repository.  
Let's see.  
Mhm.  
All three in here.  
No.  
OK.  
Um, so I added I.  
Summarized.  
A lot of the architecture discussion from yesterday and the previous meeting and put them in these docs just so we'd start to have a record.  
In GitHub and we can go through and make sure that they're aligned with what everybody was, everyone's expectations based on the discussions and we also have the confluence document.  
Um, with our diagram.  
We ready to get started? Everyone says it feels like a Friday so far.

**Pavel Frolov**   2:20  
Mhm.

**Nathan Carver**   2:23  
Did we lose Val? I think we lost Val.

**Juan Martinez**   2:55  
I think we're ready, Nathan.

**Nathan Carver**   2:56  
All right, we're all set.

**Val Levitan**   2:59  
What is? What is the difference between basic e-wallet configuration? Oh, single kiosk I see.  
I'm multiple.

**Nathan Carver**   3:08  
Yeah, actually we should probably call that single, but.

**Pavel Frolov**   3:19  
And location hub. In first schematic I see within redemption kiosk and the 2nd schematic shows a different dedicated device for location hub.

**Nathan Carver**   3:20  
Yeah, OK.

**Pavel Frolov**   3:39  
I understand.

**Nathan Carver**   3:39  
OK.  
Yes, correct. So.  
Basic and advanced we should we should switch the names to single kiosk and then perhaps JBL server should be the better a better name.  
OK.  
I also yeah, we added the transaction flow to try to grab.  
What the events might look like.  
And how the pieces will talk to each other during wallet creation gaming session and then cash out.  
These actually render really well on GitHub.

**Val Levitan**   4:45  
Also, I see that you are describing the.  
Replication database replication. Yesterday we had a different word for it, I forgot.

**Nathan Carver**   4:57  
Uh, clustering is another.

**Val Levitan**   4:59  
Clustering, yeah. Can we can we rename it? Because I have difficult time understanding all the terms.

**Nathan Carver**   5:01  
Yeah, so, um, I.  
Yes, so real quick distinction. A cluster is specific to a database, a group of databases.  
Working together, a replication can be done without a cluster, so it's it's a little more flexible approach so we can use other. In fact that's what I have in here.

**Pavel Frolov**   5:24  
Mm.

**Nathan Carver**   5:40  
As I was churning through my exploration.  
The event driven replication as actually doesn't need a cluster. It can be done with with a message queue for example so.  
That's why I changed the term, but I can add that in there for that.

**Val Levitan**   6:02  
No, no, I don't need it. I've learned something new right now. That's fine.

**Nathan Carver**   6:02  
If we want clustering.  
OK.  
Uh, OK.  
Um, yeah, so the.  
Event-driven replication would be.  
Anytime there's an activity in one of the devices, so for example JVL's server would be the hub.  
Anytime any of the kiosks or any device on the net in the on the location network, it would send a message to the server. The server would then ensure that that message gets distributed to all the other devices on the network so they could update their internal.  
Storage to to match it.  
The advantage to that specific. The specific advantage to that is it's much easier to swap in a new device because it just has to register with the the message queue as a consumer.  
To to swap in a new database until a a cluster is more far more complicated.  
Than just subscribing to a message queue. So that's a distinct advantage there. I did have. I had Claude just quickly generate a a matrix for me so that I could visually see what it was.  
What it was thinking as far as the trade-offs.  
And I think it's pretty good. I think what it came up with that seemed reasonable to me, so I put it in there.

**Val Levitan**   7:59  
OK, well, I'm not a specialist. Don't expect any comments from me.

**Nathan Carver**   8:04  
Yeah, so I think we have, we have options. The engineering team has options and um.  
The event driven. I've done that before. We have used that a number of times. Event driven with a message queue is is pretty straightforward and pretty, pretty simple.  
Shouldn't say simple, but there's less complexity in implementing that in the in the architecture.

**Val Levitan**   8:32  
I guess the point here is that in the e-wallet architecture with or without with single or or multiple redemption kiosks.  
We are not showing a local server.  
So my understanding is that.  
We're now.  
Suggesting that the server component will not be a physical device, but would would would rather be an application that can be installed on either.  
POS or a redemption kiosk?

**Nathan Carver**   9:17  
Um.

**Val Levitan**   9:17  
Do I understand the architecture correctly?

**Nathan Carver**   9:24  
Yes, we can do that. Um.

**Val Levitan**   9:29  
Well, I'm saying we're intentionally not showing.

**Pavel Frolov**   9:31  
M.

**Nathan Carver**   9:33  
Hold on.

**Val Levitan**   9:35  
A local server.

**Nathan Carver**   9:37  
Oh, it's in the second second diagram.

**Val Levitan**   9:38  
So.

**Nathan Carver**   9:43  
With multiple kiosks, there's a local JVL server as the location hub.

**Val Levitan**   9:48  
Oh, I see. Oh.  
Oh, now I see it. Did we not decide against it?

**Nathan Carver**   10:00  
I don't. I don't recall a decision. I remember it's it was it's an option that's been talked about. I know Pablo said reference to it. So I think it's.

**Val Levitan**   10:10  
So what is the what is the functionality of the local server if we're we're talking about?  
A parallel data application.  
That could be mounted.

**Pavel Frolov**   10:28  
Hmm.

**Val Levitan**   10:31  
In any of the hardware.  
I'm not sure if I'm structuring my question correctly.

**Nathan Carver**   10:39  
Correct. So why have a physical local server when the applications it runs could be installed on a kiosk for example?

**Val Levitan**   10:52  
Well, I think the point here is that we are developing.  
A specific architecture where a database will be presented or a server server side will be presented in the form of an application.  
That could be installed on any of the hardware, either POS or redemption kiosk or both and will be and will have the redundancy aspect to it and and and the benefit of installing.  
Server as an application is the fact that we are guaranteeing a redundancy.

**Nathan Carver**   11:37  
Correct. So if right, so if all the if, let's say all the kiosks are capable of hosting the location as the server, right? And then if one goes down, the other can take on.

**Val Levitan**   11:52  
Well, not only Kios, but any of our hardware. We're saying, look, any of our hardware is capable of hosting a server application and that's how we're making our hardware. We're specifically making our hardware.

**Nathan Carver**   11:53  
Not hosting.

**Val Levitan**   12:09  
With enough whatever memory or processing power to host a server application on it.  
That this becomes a requirement.

**Nathan Carver**   12:23  
Correct.

**Val Levitan**   12:24  
So each of our hardware products, we're saying any well products like POS or redemption kiosk will come with the capability of hosting a server application therefore.  
Answering a requirement for redundancy in the location and we identified server being an important.  
Object of redundancy. Why? Because if a local server goes down, the entire location goes down, especially in configuration under Tito architecture.

**Nathan Carver**   13:08  
Correct.

**Pavel Frolov**   13:09  
Hmm.

**Val Levitan**   13:09  
Well if this is the case then in GitHub advanced e-wallet configuration multiple kiosks with local server hub.  
I assume is the wrong.  
Schematic, is it not?

**Nathan Carver**   13:28  
So I think so as far as the systems go, the difference between a local server and a kiosk. Well, I'm making some assumptions, but it.  
It's gonna it could have more local storage capacity, so the databases could be bigger. It could support.  
Setting up a a hard drive array so you know multiple drives. If an internal drive fails, it has redundancy internally, so it has the advantage of being more of a robust system. I'm not sure I definitely.  
Know that like the between the Flex POS and the kiosk, the kiosk just being a much bigger device could have more storage options than the Flex POS and then the server ideally would have even more.  
Um, capacity to add, you know, um, physical storage.  
So that would be the advantage of the server is just it.  
It can. It'd be larger in a sense. It can store more data, have more hard drives on the on the hard drive array, and potentially more memory to serve the entire location.  
So I think one of the things we'll want to do architecturally is is understand what's the data limitation of a kiosk and a flex POS. How much data can they persist? Because over time while our cloud can persist, you know N number of.  
Terabytes of data. The kiosks can't do that, so eventually data's gonna have to be cycled on the kiosk, so old data would have to be purged and once it's archived to the cloud.  
Um, so those decisions would have to be made.

**Val Levitan**   15:22  
I think I think.  
But if I understand correctly, that's the whole point. We don't want to keep much of a data on even the local server. We want it to be like what, a week?

**Juan Martinez**   15:38  
I was gonna say a week at the most. Yeah, unlike a normal casino, Nathan, there, there's no historical analysis going on here. We want that ticket to expire as quickly as possible from a reconciliation standpoint, so.

**Nathan Carver**   15:50  
OK.

**Juan Martinez**   15:55  
Yeah, I will, yeah.

**Nathan Carver**   15:56  
Oh, I see. So tickets bullets relatively quickly, I guess.

**Pavel Frolov**   15:56  
Actually.  
Actually, I think the smallest storage available right now for our platforms, modern platform will be enough for ages to store data because events not so frequent.

**Nathan Carver**   16:15  
OK.

**Pavel Frolov**   16:18  
We just need to store each transaction from ticket to machine, from machine to ticket. It's very, very.

**Nathan Carver**   16:28  
OK.

**Pavel Frolov**   16:30  
No, not so frequently, yeah.

**Nathan Carver**   16:34  
OK, that's good to know. Yeah. So I think that makes the case.

**Pavel Frolov**   16:35  
Oh.

**Val Levitan**   16:37  
So this calls this calls for an update of the requirements.  
So we require for data to be replaced every week, so we're holding data only for seven days.

**Nathan Carver**   17:01  
OK.

**Val Levitan**   17:02  
And the requirement is for daily or hourly migration of data from local to cloud server.  
We don't need a minute by minute migration, but we're probably or second by second, but we probably need hourly dump.

**Nathan Carver**   17:26  
OK.

**Val Levitan**   17:27  
Again, not an engineer, so I'm overstepping my boundaries here.  
I'm just saying that.

**Nathan Carver**   17:35  
Thanks.

**Val Levitan**   17:35  
This is not a life or death situation, but we should not have the data set too long on the local server.

**Nathan Carver**   17:48  
Yeah. And I think this based on what Pavel said and the fact that we don't have to keep, you know, we are going to wipe the data after a period of time. I think the messaging replication makes sense because it's.

**Pavel Frolov**   18:00  
Yeah.

**Nathan Carver**   18:07  
I think it's that should that that should make sense as far as an implementation.

**Pavel Frolov**   18:12  
Actually I prefer not to to wipe data anytime on database, but taken some snapshots periodically to the cloud server, but never remove data from the database because.  
Actually it will increase write or clear commands to database, but if we left all the data on the database less write commands to storage, it will save us.

**Nathan Carver**   18:49  
Yeah.

**Val Levitan**   18:53  
Well, we don't want data.  
On the local devices for longer than a week, because if you accumulate data for a long time, it becomes dangerous. Somebody takes a device and our data is exposed.

**Pavel Frolov**   19:14  
Oh.

**Val Levitan**   19:17  
So you do not want local data sitting for a long time. It should be. And when I'm saying wiped out, it should be overwritten. That's the proper term that I should be using. So I'm not talking about wiping data off, but I'm saying overwriting data. So the previous data is limited.  
Or or total exposure is limiting.  
And I don't know what people could do with that data. Maybe it's not really dangerous information, but why expose yourself? Because.

**Nathan Carver**   19:46  
OK.

**Juan Martinez**   19:51  
No, but the the.  
No, I agree about the the data. The database growth is the concerning problem too. I mean, if if we don't do a purge or an overwrite, it it just gets out of hand and eventually starts slowing down and requires database maintenance, which we don't necessarily want to do.

**Val Levitan**   20:10  
But even if there is engineering solution for it, I'm against keeping the data on the local server. Don't need it, don't need that exposure. There's no, there's no useful application for.

**Juan Martinez**   20:10  
2\.  
Sure.

**Pavel Frolov**   20:20  
OK, got it.

**Juan Martinez**   20:26  
Yeah.

**Val Levitan**   20:28  
And again, I'm not saying that our servers should be busy with communicating with the cloud, but within a reasonable time, reasonable stream of data should.  
Minimize the local exposure.

**Juan Martinez**   20:44  
And Pavel, that that snapshot you mentioned would let's say there's a scenario where it it it something happens on a Friday night, we lose the three days there because of the weekend. Will it ever take more than seven days to troubleshoot an incident where we need that?  
Data or will the snapshot process you described collect that data and move it to the cloud so we can analyze it there?

**Pavel Frolov**   21:13  
Oh, actually, I don't know. It's up to us to implement any behavior.

**Juan Martinez**   21:22  
OK.

**Pavel Frolov**   21:22  
The frequency of making snapshots and so on.  
It's not implemented right now, so that's why we are open to any suggestions.

**Juan Martinez**   21:32  
OK.

**Nathan Carver**   21:34  
Yeah, I think the with the replication approach for example.  
If you look at the E wallet transaction flow, um.  
As soon as the player inserts cash, the e-wallet is created and recorded on that. That redemption kiosk saves it locally. There's an immediate message that's sent to JVL control server.  
Of that transaction. So it transaction by transaction will be sent as they happen. So if there's three kiosks, they would all be sending transactions now because the nature of the messaging and I can diagram this up.  
The message would be posted and every device on the network listening included the JVL server would get that transaction and and save it. So the server will be just saving these transactions as they happen as opposed to a a larger data synchronization step at some point in time.  
And then the nature of the message queue is if the Internet is down and the control server can't receive the messages, as soon as connection is reestablished, all of those messages would have we would configure the system to be guaranteed delivery.  
So essentially once the network's back up, the control server would get message by message and could it would eventually catch back up to where that location to the location transactions.

**Pavel Frolov**   23:08  
But in in this schematic you means that the master of all messaging will be on on the cloud.

**Nathan Carver**   23:20  
So the location would have to have a look a local message queue in order to store those messages until no Internet connection was reestablished.

**Pavel Frolov**   23:29  
Mhm.  
And then just synchronization between main uh cloud server and the master uh queue.

**Nathan Carver**   23:42  
Correct.  
Yeah, and then the messaging.

**Pavel Frolov**   23:45  
But and master queue. Master queue can be changed by some controlling operation from from server for example or on location.

**Nathan Carver**   23:57  
Correct. So if it right, if the kiosk with the master queue or the local server goes down, then a new queue would have to be switch. We'd switch over to a new queue if there was a second kiosk device on site.

**Pavel Frolov**   24:13  
Mhm.

**Juan Martinez**   24:17  
The this cloud based the replication to the cloud, though the cloud server could contain extended data for historical reporting purposes and analysis, correct?

**Nathan Carver**   24:31  
Yes.

**Juan Martinez**   24:33  
Yeah, Val, I think it's helpful to know that, hey, if this gets deployed at multiple locations, you know which location was the busiest, who did the most day by day transactional views. I think that there's value to for us to keep.  
Extended data in the cloud for our own use.

**Val Levitan**   24:52  
We extended the the the cloud. I think we should keep forever and protect and defend. I mean, but that's a totally different ball of wax now.

**Juan Martinez**   24:58  
Yeah.  
Absolutely.

**Val Levitan**   25:05  
So back to the schematic, does it trigger the change in how the schematic illustrate, how the schematic, how schematic is illustrated?

**Nathan Carver**   25:18  
Yes, so we would want to do a data flow. That's it doesn't change this these two schematics too much other than if we remove the local server and say we just have two kiosks doing this.  
Uh.  
Because the queue would actually be in one of the kiosks, so we could create a data flow that shows how the messaging would work.

**Juan Martinez**   25:36  
But.  
Well, Ken, I I think we should still show the what you're calling the location hub, but just maybe a a pen, the word embedded. So it's all clear that this is software now running inside of.

**Nathan Carver**   25:46  
Since it's all software.

**Juan Martinez**   26:00  
One of several local devices and maybe disconnect it from the flex ports.

**Nathan Carver**   26:06  
Yes, yeah, I think we'll what I'll create is a.  
And we could draw this out. It'll be a lot faster than designing a mermaid duck on the fly, but let's do that.  
Uh, let's see here. Let me share this.  
I'm just gonna jump into the.  
Into the doc. So um, what's the best way to do this?  
Ask.  
Make these a little bigger.  
Um.  
So there would be a message queue.  
So let's say that kiosk is the main. Um.  
So we'll we'll kind of identify.  
The software components in here, so there would be a um.  
We'll just say this is the kiosk application, right? So for lack of a better term.  
And so when when a transaction occurs.  
The Kiosk application would um.  
Create a transaction message.  
So this is going to create a transaction message.  
And then over here this also has a kiosk application and it's going to what it's going to do.  
Is it's going to subscribe.  
Subscribes to message queue.  
So.  
This kiosk will say OK, I'm I'm a subscriber to your message queue and it's listening for these transaction messages. So what would happen is this kiosk does a transaction.  
Post that information to the message queue and then what the message queue will then push.  
Push transaction message.  
The kiosk be for example.  
So we'd also do the same thing.

**Juan Martinez**   29:32  
And.

**Nathan Carver**   29:35  
So if we dropped in kiosk C.

**Juan Martinez**   29:38  
Or or POS.

**Nathan Carver**   29:39  
To the.  
Or POS. No. Yeah, that's actually. Let's do that.

**Juan Martinez**   29:44  
And also just to clarify, Nathan, you've got the message queue only in kiosk A because we've designated that as the primary for this location.

**Nathan Carver**   29:53  
Yeah, exactly.

**Pavel Frolov**   29:56  
No, not exactly. I think also all the device able to run message queue server, but we still need a procedure how to swap this.  
Of this feature between devices.

**Nathan Carver**   30:14  
Yes.  
Yeah, I agree. That has to be determined.  
If.  
So when this message gets.  
Created. Let's create. Let's make this.  
So we can see it.  
That same message will get pushed.  
To both devices. So anything listening any any device that comes online in our location subscribes to this message queue when the single transaction happens.  
We also have.  
JVL Control server.  
Um, so this would just be um.  
It just seems right there. Thank you.  
This would be PLS application.  
So the idea is that they all can subscribe to this.  
So when transaction happens, it's gonna get pushed to everything listening on the network.  
This one may be a little different, but since they're all established establishing the same type of connection, the control server should also be able to listen on that message queue.  
So that's the basic approach.  
This has and the big advantage is anytime a new device is added or swapped, they just have to know where to register on this queue.  
And then the ideally is if kiosk A goes down, we need some way to.  
Roll this over into another. Another device spins up the queue. The network somehow understands how to find that queue and register to it. So that's going to be the queue itself is pretty straightforward. It's been.  
It's a very robust, there's a lot of different technical options to implement the queue. So I think the engineering challenge will be how do we switch this over.  
Um, and I wouldn't be surprised if there's already some technical solutions for this since.  
Redundancy in message queues has to be has to be considered in all major systems anyway.

**Juan Martinez**   33:18  
Are we fearful of duplicate messaging when we've got?  
Ossibly 2 simultaneously active message queues.

**Nathan Carver**   33:29  
Um.  
So right. So if if let's say oh I see so if KSB had also had a message queue for example.

**Juan Martinez**   33:41  
Right.

**Nathan Carver**   33:43  
Um.  
So I think by design it they would all have their message queues already, but they would Flex POS would only get messages from the one that it subscribes to.  
O.  
If it subscribes to Kiosk A and let's say B does actually, you know, write a transaction to this message queue, nothing will receive that queue that message unless it's actually subscribed.  
Um.  
So we would want. I'm trying to think the scenario where we get a duplicate message.  
If OK, so for example, let's just say K ask A\&B both have message queues. When Flex POS comes online, it just subscribes to every message queue in the location.  
Then the replication would the duplication would come. Then if the kiosk was pushing transactions to two queues, that would create a duplicate.  
But if we actually had, if we are just out of the gate, we just said every kiosk creates a message queue and everything listens on the individual queue, then in that case.  
Kiosk A would post its transactions to its queue and Kiosk B would post transactions to its queue. So then when these things occur then.  
They would also.  
Post transactions they would their transaction or messages would get transmitted to each other. So you kind of have this.  
This constant internal communication, everybody updating to what's going on within the ecosystem.  
So I think then we would get into the OK, what happens when?  
Right.  
So now we have flex ports out here.  
So I think the question will be OK, where do these flex ports, where do they publish to?  
Because a user will.  
Go to the flex bar and that's gonna as they're playing the game right, that automatically updates the e-wallet or when they cash out, it updates the e-wallet.

**Juan Martinez**   36:33  
Yeah, only only when they hit cash out. Then the process of PIN number verification I guess would initiate that initial conversation with another device.

**Nathan Carver**   36:49  
OK, right. So when those things are happening on the port, it's going to have to update. We want that wallet to be updated across. So here we would have to decide where this goes.  
The ports will not have a message queue and I don't think and Pavel can correct me if I'm wrong, but I I don't think these boards would be.  
Compatible. Or at least it wouldn't be technically feasible to do that. We would want those these flex ports sending the transaction information directly to a kiosk.

**Juan Martinez**   37:30  
Oh, just on that note, go ahead, go ahead, Pavel. Yeah, 'cause we did a use case where that's not.

**Pavel Frolov**   37:30  
Hey.  
Flexport will will not be able to drive message queue or drive any database, so it it will be.

**Nathan Carver**   37:44  
OK, yes, that's the.

**Pavel Frolov**   37:48  
Always slave device.

**Juan Martinez**   37:52  
A slave device the Pavel, but one of the use cases was what if we lost power during the pin entry process and Flexport is is has to retain some data to complete the transaction when power is restored.  
We agree there, correct?

**Pavel Frolov**   38:11  
Yes, correct, correct.

**Juan Martinez**   38:13  
OK.

**Pavel Frolov**   38:17  
So here it it will be a question what if transaction was initiated by Flexport and PIN was entered then power off for entire band and then?  
Different chaos become a master how to treat such situation, but probably this is too too difficult schematic and not real.

**Juan Martinez**   38:46  
Yeah.

**Nathan Carver**   38:47  
Yeah, the the flex ports are just, uh, slates. They would be dedicated to a kiosk.  
So the kiosk essentially becomes their persistence in their memory, and they're really just kind of the interface between the player and the kiosk.

**Pavel Frolov**   39:03  
Oh.  
Even in this situation, I think we need to have a security procedure to swap kiosk one and kiosk 2 to be master and after power up and establish new master, we still have information about this E wallet and we are able to proceed.  
This redemption from Flexport A.

**Nathan Carver**   39:34  
Got it.  
Right. So if B goes down, the process is we'll put it up here for.  
So if if currently.  
A is attached to B\&B goes down. The process is how do we reattach?  
A becomes the master and the port is flex port is now talking to a directly.  
OK.  
Correct.

**Pavel Frolov**   40:21  
Mhm.

**Nathan Carver**   40:26  
Yeah, and you wanna be able to do it from the kiosk.  
Right. Each port would find the kiosk automatically somehow, because you don't want to go to each game machine in a large, yeah.

**Juan Martinez**   40:38  
Oh, absolutely, yeah.  
Yeah, there'll be a player at that machine. You don't want to disrupt the player.

**Nathan Carver**   40:49  
And I think as far as the message queues go, as long as the ports are going directly to the kiosk application.  
They're not publishing any messages, so we don't run a risk of duplicate messages there and if kiosk just comes online.  
Then the same type of.  
Uh, realization has to be made with.  
Flex POS JBL control server that a new a new kiosk is online. That means there's a new message queue for them to subscribe to.  
And well, they'll have to know so they can make a connection to that kiosk anyway. So maybe that connection becomes.  
Once we make that connection, maybe it's less of a subscription model, but more of a internal queue that's pushing messages out.  
So anyway, the concept is guaranteed delivery if this message queue knows who its listeners are and the Internet is down, so.  
Message QA gets a transaction creates that the e-wallet is created with the balance of $10. It wants to push that transaction to all of its other peers.  
So that $10 would get pushed to B. It would get pushed to Flex POS, but if the Internet is down, it can't push that message. So the queue would then hold it for the JVL control server until.  
The server reestablishes connection and then it would get pushed. Um.  
OK, I think that makes sense.  
Let's see anything else we wanna dive into on the.  
Messaging replicating the transaction data.

**Juan Martinez**   43:20  
In a I mean this is a scenario where we have the redemption kiosk. If it's a POS only location, do we need the message queue to also be in the POS device?  
For any reason.

**Nathan Carver**   43:40  
Is the POS, will it also maintain an e-wallet then has the ability to do that or is it just for redemption of gift cards still?

**Juan Martinez**   43:56  
Uh.

**Nathan Carver**   44:00  
So in the current design, because we're just activating gift cards, redeeming tickets.

**Pavel Frolov**   44:02  
Hmm.

**Nathan Carver**   44:07  
With Flex POS, it wouldn't need a message queue. It's gonna make those direct.  
Um, the Flex VOS will kind of have a this a similar connection to the control server that.  
The flex art would have the key out, right? They're going to be directly communicating with each other.

**Juan Martinez**   44:29  
Yeah. And then to directly answer your question is no, because if if it's a POS only site, then there is no printer to generate the e-wallet ticket, so no.

**Nathan Carver**   44:44  
Uh, yes, that makes sense.  
Yes, so in a POS only site there would be no need for a message queue since it would be direct communication.

**Juan Martinez**   44:56  
Right.

**Pavel Frolov**   44:58  
Yeah.

**Juan Martinez**   45:00  
Yeah, the the ticket is is the output from the Mother Goose to us, so.

**Nathan Carver**   45:09  
Correct.  
OK.  
Um, alright. Any other questions there?

**Pavel Frolov**   45:32  
No.

**Val Levitan**   45:33  
So the undertaking for you, Nathan, is to update the schematic diagrams in GitHub.

**Nathan Carver**   45:41  
Yes.

**Val Levitan**   45:44  
Just as a side note, I foresee uh.  
Market moving towards.  
Replacing.  
Move the goose with JVL Smith boards.

**Nathan Carver**   46:03  
Hmm.

**Val Levitan**   46:05  
Because we will practically give it away.  
So I expect new installations. When people buy new machines, they will install our POS and we're going to give them free smibs for their machines.  
So typical installation, an operator says, OK, I need to buy two more machines for a location. I'm going to buy one light and wonders and another one IGT.  
And OK, these two machines require the the interface ports. How much is it? Well, I get a discounted price of $150.00 each board. Well, why should I pay $300.00 for two machines if JVL gives away?  
Oh.  
Smith boards for free. All I need to do is to commit to a three-year usage of JVL's POS system, which by the way gives me a bunch of advantages.

**Nathan Carver**   47:17  
Yeah.

**Pavel Frolov**   47:27  
No.  
But uh uh, remember SMIP board requires uh cheater approach.

**Nathan Carver**   47:29  
All right.

**Pavel Frolov**   47:38  
Not the wallet.

**Val Levitan**   47:40  
Why?  
Uh.

**Pavel Frolov**   47:44  
Because we do not have.

**Val Levitan**   47:45  
No, no, no, no, no. I'm I'm not saying E wallet or Tito. I'm saying retrofit for Mother Goose.

**Pavel Frolov**   47:56  
Oh, OK.

**Val Levitan**   48:01  
So neither Tito nor an e-wallet. All I want to do is to install a new location with two new machines in it, for which I have to buy a fledgling board for each machine.  
At a price of one. Do you remember the price for the fledglings?

**Juan Martinez**   48:20  
I don't, but one second here.

**Val Levitan**   48:36  
Quick.

**Juan Martinez**   48:38  
Bye.

**Pavel Frolov**   48:39  
One hundreds 110 approximately.

**Juan Martinez**   48:43  
Yeah.

**Val Levitan**   48:44  
OK, so let's say a discounted price of $80.00 for an operator who buys a lot of boards.

**Juan Martinez**   48:44  
Yeah.

**Pavel Frolov**   48:50  
Mm-hmm.

**Val Levitan**   48:51  
So two boards, $160.00 with JVL $0.00. All you need to do is to commit yourself to a three-year contract with us.  
OK, one more thing that we need to talk right now about is and we kind of brushed, brushed on the subject a while back, but then parked the subject.  
We definitely want to have an an application, a mobile application that gives an operator basic intelligence on the location performance.  
Which connects to our cloud server.  
So that should be always reflected in our schematic diagrams, even if it's not an MVP.

**Nathan Carver**   50:02  
OK.

**Juan Martinez**   50:09  
Nathan, I'll share some of the vendors design docs on on the topic of mobile with you.

**Nathan Carver**   50:18  
OK, so let's see here.

**Val Levitan**   50:21  
So as an undertaking, it should be added to all our schematics.

**Nathan Carver**   50:35  
Yeah, it's kind of a, um, external.  
So there would be some.  
OK, yeah.  
That makes sense.  
So in that sense the Um.  
The gateway becomes essentially a collection of APIs.  
OK.  
Uh.  
This really becomes a collection of um.  
APIs and it supports. Um.  
So this would be um.  
So it would have various systems behind the the gateway.  
That support those APIs.  
OK, that makes sense.  
Uh, is there anything else we wanna dive into today?

**Pavel Frolov**   52:17  
Mm.  
I'm not not sure.

**Nathan Carver**   52:34  
OK.

**Juan Martinez**   52:43  
I would say as a side note, Nathan, we probably should map out the Smith scenario that Val just presented as as another possible setup. Not necessarily on this page, but just.

**Nathan Carver**   52:55  
OK.  
Yeah, that would help me understand a little bit more. That's where replacing the Mother Goose scenario.

**Juan Martinez**   53:00  
keep everything.  
Yes.

**Nathan Carver**   53:09  
OK.  
Oh, looks like OK, Val stepped away.  
OK, so I can add more detailed on the.  
I'll update the diagrams with.  
A data flow showing how the messages would flow in the system.  
Um.  
And.  
I'll dig around a little bit more.  
On message queues that we could possibly use or if there's, yeah, just what the tech options are there. I've used several different types of queues, but.  
Um, some of them are pretty lightweight and.  
Shouldn't be too hard to implement those in these systems.  
Yeah, from this sense, from a mobile app perspective, if JBL just has a gateway of some kind, you could you could create web apps as well.  
For customers, you could have a lot of, you got a lot of options, I think some flexibility.

**Juan Martinez**   54:42  
Yeah. Is that Pavel, would that be the preferred way to do our own internal reporting tools where it's it's we're calling, we're going to a web page to do any analysis on on?  
On the functionality of each location here.

**Pavel Frolov**   55:02  
Yeah, actually we will collect all the data related to each particular location with all statistical and we'll be able to produce some reporting.  
In any suitable way, but it actually depends on if it will be internal or we need to to produce some reporting for mobile app.

**Val Levitan**   55:36  
Let's park this conversation right now. Let's.

**Pavel Frolov**   55:39  
Mm-hmm.

**Val Levitan**   55:41  
Let's just understand that there might be a a mobile app and let's represent it in the schematic diagram and assume it as an undertaking for Nathan to update diagrams accordingly.

**Nathan Carver**   55:58  
OK.  
That's good.  
OK, Val, is there anything else you want to dive into?

**Val Levitan**   56:11  
No, I think I'm satisfied. I would like to go back to Tito.  
And discuss Tito in the form of a similar diagram and yes, we have for E wallet.

**Nathan Carver**   56:26  
OK.

**Val Levitan**   56:28  
We have plenty of time to do it today. I don't want to spend any more time on this.  
I think you could work on it on your own, but Cito needs everybody's participation.

**Nathan Carver**   56:42  
OK, sounds good.

**Val Levitan**   56:44  
So if you could copy and paste this and we'll just butcher it for Tito purpose.

**Nathan Carver**   56:57  
OK.

**Val Levitan**   57:00  
I'll start start a new one please if possible.

**Nathan Carver**   57:04  
Ah, OK, let me do that.

**Val Levitan**   57:07  
And send the links to us, please.

**Pavel Frolov**   57:23  
Oh, actually you can just press the duplicate button and the same.

**Nathan Carver**   57:29  
Oh, really? OK.  
Oh, nice.  
OK.

**Val Levitan**   58:09  
What's the link please?  
Thank you very much. I'm on it.  
Hello world.

**Nathan Carver**   58:32  
OK.  
So the Tito obviously is not going to have the E wallet, correct?

**Juan Martinez**   59:05  
Perfect.

**Nathan Carver**   59:08  
Get rid of that.

**Juan Martinez**   59:16  
Geo must have a printer.  
And must have.

**Nathan Carver**   59:23  
Is that this of the dispenser?

**Juan Martinez**   59:27  
What's that?

**Val Levitan**   59:29  
No dispenser.

**Nathan Carver**   59:31  
No dispenser.  
We would have a printer.

**Juan Martinez**   59:39  
Yep.

**Nathan Carver**   59:40  
But no dispenser.

**Juan Martinez**   1:01:40  
Um.  
Pavel, where? Where are we generating and validating Tito ticket numbers? Where's the Tito ticket database in this drawing?

**Pavel Frolov**   1:01:54  
Uh, processing application.

**Juan Martinez**   1:01:59  
So OK, inside of Flex POS, OK.

**Pavel Frolov**   1:02:02  
Yeah, if only one smart device available here in form of Flex POS and it will be on Flex POS.

**Juan Martinez**   1:02:12  
I'm gonna add Tito to that just so it's clear.

**Val Levitan**   1:02:28  
OK, so in here we need a dispensing tower.

**Nathan Carver**   1:02:44  
In the cage.

**Val Levitan**   1:02:46  
Uh, no here.

**Nathan Carver**   1:02:47  
OK.  
Oh, OK.  
I think we can.  
There we can lock those boxes so they don't move.  
Is this what sits between the machines? Is that?

**Juan Martinez**   1:03:37  
It could, or off to the side either way.

**Nathan Carver**   1:03:44  
That's a really horrible color. Let's see.

**Juan Martinez**   1:04:33  
And dispensing tower also gets connected to the router.  
And.

**Val Levitan**   1:05:02  
Let's illustrate multiple dispensing towers.

**Nathan Carver**   1:05:07  
OK.  
Um.

**Pavel Frolov**   1:06:27  
Usually in schematic of Tita, when the player want to redeem his ticket with value printed on it, he need to insert it to bill acceptor.

**Val Levitan**   1:06:27  
OK.

**Pavel Frolov**   1:06:43  
On any of device.

**Val Levitan**   1:06:46  
Yes, Pavel, you're right.

**Pavel Frolov**   1:06:50  
So do we need to install for this purpose bill acceptor or do we need to inform the player if you redeem your ticket?

**Val Levitan**   1:07:00  
No, you're probably telling us that dispensing tower in this application is not applicable.  
I think, I think this is what you're telling us.

**Juan Martinez**   1:07:14  
I mean, well, that's.

**Pavel Frolov**   1:07:14  
Oh.

**Juan Martinez**   1:07:20  
Why we we can't scan a a standard barcode at at the?

**Val Levitan**   1:07:25  
We can.

**Pavel Frolov**   1:07:25  
We can. We can scan.

**Val Levitan**   1:07:28  
But the premise of Tito is to take possession of the ticket.

**Juan Martinez**   1:07:36  
Yes, yes, yes, yes.

**Val Levitan**   1:07:39  
That's why I'm assuming that having a dispensing tower in this case is not applicable.  
So then what happens? Trying to play a use case through my mind. A player must must go to the cage.

**Juan Martinez**   1:07:58  
You.  
Yeah, without a form of redemption on the floor, you must go to the cage to hand in your ticket and get your gift card.  
Unless we add a bill acceptor to the dispensing tower.

**Val Levitan**   1:08:43  
Interestingly enough, we don't really need a bill acceptor in the dispensing tower, we just need to swallow the ticket.

**Juan Martinez**   1:08:56  
Yes.

**Val Levitan**   1:09:02  
O We need a truck that scans the ticket.  
Stocks it.

**Juan Martinez**   1:09:13  
You just described it, Bill Exceptre.

**Nathan Carver**   1:09:14  
OK.

**Val Levitan**   1:09:19  
Man, it's just a PD to pay so much money for a bill accepted.

**Juan Martinez**   1:09:24  
Sure.  
Well, I mean for this purpose there there's so many low-cost bill acceptors out there like that BV50 or whatever. There's certainly inexpensive solutions to versus because what I mean you what you also described is is a.

**Pavel Frolov**   1:09:28  
Just.  
4\.  
It.

**Juan Martinez**   1:09:43  
A like a belt-driven ticket insertion slash scanning device where it scans it and then just drops it in in like a reject bin for lack of a better word.

**Val Levitan**   1:09:56  
OK.

**Pavel Frolov**   1:09:58  
We just need some hot device that burns a space whereas a barcode is printed.

**Juan Martinez**   1:10:12  
Shooting lasers near players is never a good idea.

**Pavel Frolov**   1:10:16  
Thank you.

**Val Levitan**   1:10:28  
What are we saying?

**Pavel Frolov**   1:10:32  
Actually in this schematic we still able to install Flex pay that actually contains bill acceptor.

**Val Levitan**   1:10:45  
Yes, but that's expensive.

**Juan Martinez**   1:11:05  
Yeah, Val, I, I, I still think that if we remove the dispensing towers and the player has to go to the cage that that that is sort of an interaction that we believe the locations welcome so that they can try to upsell their own products or as you know maybe.  
Convert directly to cash instead of a gift card.

**Val Levitan**   1:11:29  
One What happens in a casino environment where a Tito ticket is presented at a cage? What happens to that Tito ticket?

**Juan Martinez**   1:11:39  
Below the cage window there's been a a drawer with the lock and key which just has a a slit cut out in it and they just slide the ticket that the redeemed ticket in there and then at the end of the shift a supervisor.  
Takes all of those. They get rescanned to make sure nothing was missed and then they get shredded.  
Because the tickets are in the database, there's no value anymore to physically keeping those tickets.

**Val Levitan**   1:12:15  
So what? What will the procedure be here?  
I'm afraid that if we're going to put bill acceptors with stackers, stacker's going to get filled, nobody's going to empty it and bill acceptor will manifest will malfunction.

**Juan Martinez**   1:12:31  
No, but the the same process occurs on the on the slot machines. Somebody has to come and and empty the the cash boxes on the machines. They would just have one more machine which is the dispenser.

**Val Levitan**   1:12:49  
Yes, no, I understand in the ideal or not ideal, but in a disciplined environment. But locations are not exactly disciplined and.

**Juan Martinez**   1:12:57  
Yeah.

**Val Levitan**   1:13:01  
A dispenser is not looked upon as a as a machine to be emptied.

**Juan Martinez**   1:13:09  
Sure.

**Val Levitan**   1:13:10  
So I'm just a little bit concerned with it.  
And the same goes for the.  
Countertop dispenser that Gennady and I discussed yesterday.

**Nathan Carver**   1:13:21  
OK.

**Val Levitan**   1:13:25  
If we have to put a bill acceptor in there.  
It grows dramatically in size.

**Juan Martinez**   1:13:34  
Yeah.

**Val Levitan**   1:13:37  
And also functionality. How do you open it? How do you empty it out? It's the point of service, just a tremendous point of service here now.

**Juan Martinez**   1:13:42  
Yeah.  
Yeah.  
No, I mean the this would be, we would have to create an operational procedure for the location where they collect the process tickets in a bag in a bin like a tip bin and that they're shredded later in the day or destroyed however they want to because they're they're no good.  
Granted that an employee will try to take one of those tickets and try to insert it in the machine, but they'll quickly learn that they're already invalid tickets.  
That's the only thing I can think of. It becomes a a process that the location now has to follow.

**Val Levitan**   1:14:42  
May I think?  
Um, freely without being criticized.

**Juan Martinez**   1:14:53  
Or spell.

**Val Levitan**   1:14:54  
What if we made a device?  
That reads the barcode and shreds it.

**Juan Martinez**   1:15:09  
We would still there would still be a reject bin that would become full of shredded paper that somebody has to empty.

**Val Levitan**   1:15:19  
Right. But we wouldn't run a risk of any stupidity and and it's much easier to empty a shredded then.

**Juan Martinez**   1:15:32  
Yes.  
Shredded paper does not stack as nicely as a compressed stack of tickets in a cash box, so the shredder bin may need the the device may need to be a little taller to allow for extra.  
Paper in that reject bin. Think about a portable office paper shredder type of bin. Not that big, but certainly.

**Val Levitan**   1:16:05  
A better idea. We instead of stacking it, we shred it and exit it.

**Pavel Frolov**   1:16:12  
No, no need to shred, just we can just print over the regular ticket, just a black rectangle over the bar code.

**Juan Martinez**   1:16:28  
So.

**Val Levitan**   1:16:29  
But but printing. But printing is not cheap. It's better to cut and exit.  
So we take it, read it.  
Deal with it electronically or digitally.

**Pavel Frolov**   1:16:49  
Again, well again when.

**Val Levitan**   1:16:50  
Cut cut next.

**Pavel Frolov**   1:16:53  
When I said to head hot device, it was not a joke, it was a real suggestion. Hot device will make a black picture on the ticket because this is a terminal.

**Juan Martinez**   1:17:05  
Yes, yeah.  
Right. Yeah. But what Pavel's describing the exact process of you accidentally leaving your Tito ticket in your car for a week, the sun makes it all black out.

**Val Levitan**   1:17:11  
OK.

**Pavel Frolov**   1:17:11  
Paper.

**Juan Martinez**   1:17:23  
But that that still sounds more more expensive than shredding Pavel. I I don't know, applying a heat lamp inside close to electronics cause Val what what the pedestal for the dispensing tower could now be this reject bin.  
Just a basically a plastic nice garbage can.

**Val Levitan**   1:17:44  
I see.  
I suggest no reject. I suggest exit.

**Juan Martinez**   1:17:51  
Well, that's what I mean. It it it exit into this plastic bin. That's garbage.

**Val Levitan**   1:17:54  
No, no exit to the outside.

**Juan Martinez**   1:18:01  
Where does it? What is the outside? You you now have a a physical Tito ticket that somebody can grab. I'm I'm just trying to envision.

**Val Levitan**   1:18:10  
Yeah, falls on the floor, falls out, falls away. You know, hold on a second. One second.

**Juan Martinez**   1:18:17  
Sure.  
Yeah, that I I can't envision that process of tickets on the floor. The place could look dirty. If anybody's smoking and they drop it on a piece of paper, we could have a fire hazard. We got to think about that one.

**Genadi Peari**   1:19:10  
I might missing something. Are we talking about the same ticket that they printed after?

**Juan Martinez**   1:19:14  
Yeah, what, what, what?  
After a Tito cash out, yeah.

**Genadi Peari**   1:19:19  
Player finish. Player finish the game, right?

**Juan Martinez**   1:19:22  
Yes, player finishes the game. Now he has a Tito ticket and most other solutions. You then take the Tito ticket to a kiosk and the kiosk dispenses a card or cash or whatever in this case.  
We don't have a device with a bill acceptor to receive the Tito ticket. So the question is, where does that Tito ticket go so that it can get scanned, redeemed, converted to a gift card and disposed of?

**Val Levitan**   1:19:57  
So I'm saying burn it or cut it and throw it away.  
So there will be a lot of paper.  
Piled or thrown away, but it will create a mess on purpose and somebody will help to clean it up, but it will be obvious that it cannot be reused.  
I know it might be a stupid idea, but maybe not so stupid.

**Juan Martinez**   1:20:27  
Yeah, if I'm a player, I I would pick up the ticket that I just scanned, convert to my card and go to the cage and try to reuse that ticket and, you know, create an argument. No, here's my ticket. I have it. I didn't get paid. Please pay me.

**Val Levitan**   1:20:45  
But if it's cut or destroyed, or, as Pavel said, burned.  
What? What is he gonna do?

**Juan Martinez**   1:20:55  
But why? Why are you opposed to a a plastic reject bin at at the bottom of the unit that's very easily removed by the employee?

**Val Levitan**   1:21:04  
I'm not opposed, I am suggesting that.  
Maybe it's not perfect.

**Juan Martinez**   1:21:12  
Yeah, I I just think that, you know, dropping something on the floor just does not look good.  
We're we're creating a mess and if the employee is a terrible employee, well, I'll clean it right before I'm going home. And you know, we we're JVL is creating a mess, I guess would be the the word that could get out.

**Val Levitan**   1:21:43  
Well.  
You are not wrong.

**Juan Martinez**   1:21:52  
Now the device that Pavel described, if it successfully scanned the ticket infrared lamp blacked out the paper and then spit it back out, then the player can grab it and throw it out on his way out.  
Or throw it on the floor. But then that way we didn't throw it on the floor.  
So it it is our device that can receive, scan the ticket, deface the ticket and then reject it right back out to the player.  
Yeah. Or Val, we, you know, the dispensing tower is not necessarily in between the machines. It's off to the side and we just recommend that they put a garbage can right next to the dispenser at the locations, you know, garbage can.  
And then the players are, you know, through signage or whatever, they can just discard the ticket immediately into a a garbage can that's right next to the dispenser.

**Val Levitan**   1:23:13  
I prefer that over.  
Over installation of a bill acceptor or you know, I I prefer destroying the use ticket and it matches the casino environment.

**Juan Martinez**   1:23:22  
Yeah, yeah.  
Yeah.

**Val Levitan**   1:23:33  
The same same type of procedure.

**Juan Martinez**   1:23:36  
You prefer the destruction, not the that the player just throws it away in the trash.

**Val Levitan**   1:23:41  
I prefer a distraction. I prefer, let's say using Pavel's method. I prefer to take in the ticket, then apply laser defacing it or some sort of defacing.

**Juan Martinez**   1:23:47  
Mhm.

**Val Levitan**   1:23:57  
Then dispensing it.  
And a garbage can next to it.

**Juan Martinez**   1:24:11  
OK, Gennady, we need a bill accepting type device with a built-in optical scanner and some of the functionality of a bread toaster. How long is it going to take?

**Pavel Frolov**   1:24:22  
Mhm.

**Juan Martinez**   1:24:25  
OK.

**Pavel Frolov**   1:24:26  
Yes.

**Val Levitan**   1:24:27  
I don't think it's so difficult.  
I don't think so.

**Juan Martinez**   1:24:33  
Yeah, I just don't know what the duration of heat required to deface that thermal print. I I don't know if it's a halogen lamp or a low wattage laser. We would have to test something like that.

**Pavel Frolov**   1:24:48  
Or chemical liquid.

**Val Levitan**   1:24:51  
No, no liquid. Cannot do liquid. You have to refill it.

**Pavel Frolov**   1:24:54  
Mm.

**Juan Martinez**   1:24:57  
Yeah.

**Val Levitan**   1:25:01  
But I think it's very easy to create a cut through the device, through through let's say a center line.

**Juan Martinez**   1:25:14  
Yeah, even if we only cut it 50% of the way so that it can come back out, it's still it's still now cut and obvious that it is no longer a a valid ticket.  
Because if we cut it 100%, I don't know how we get it back out without jamming.

**Val Levitan**   1:25:32  
Well, on the way out, you cut it. You keep on.

**Juan Martinez**   1:25:35  
Yes.

**Val Levitan**   1:25:44  
I mean, shredders are very inexpensive, so this whole shredding thing is is a known entity.  
Anyways, going back to dispensing.  
Dispensing tower. The premise of the dispensing tower is to obsolete the.  
Tito ticket. So we're we're validated with dispense the card and we obsolete the ticket or we take possession of the ticket.

**Pavel Frolov**   1:26:27  
In any case, we need somehow to take this ticket, move it inside of the dispensing unit to do something and then remove it.  
What's the device?

**Val Levitan**   1:26:42  
But it's extremely simple. It's a fixed width, fixed length. The barcode is centered. It's very, very easy to read it. It doesn't take really much.  
Expertise to read it.  
It could be a slim linear device like flat flatbed.

**Juan Martinez**   1:27:33  
Research dot dot one.

**Val Levitan**   1:27:41  
OK, anyways, let's leave the dispensing towers here and as the outside solution least favorable, install a bill acceptor in there.  
But as as an undertaking for myself, I'm going to speak to our engineering team.  
About creating a flood bed device that is able to.  
Transport the ticket.  
Read it.  
And then dispense it out.  
Shredded.

**Juan Martinez**   1:28:46  
OK.

**Val Levitan**   1:28:51  
And if this device can't be made, then it should be part of the countertop.  
Card dispensing device.  
I think we also need a an easy way for a dispute resolution.  
Let me explain what I'm saying. Players will find, present and try the system.  
For various types of fraud. So they'll pick up a an electronic wallet barcode or or a QR code or Tito ticket barcode and we need a mechanism for.  
And the tandem location to rescan the.  
The ticket and present the player with.  
A report.  
When it was generated, when it was played, when it was cashed in.

**Juan Martinez**   1:31:01  
That that should definitely be the function of of the POS device where you simply scan the ticket and they can rotate the screen and it would show you everything that you just described Val.

**Val Levitan**   1:31:14  
I'm suggesting that it should be a function of any device equipped with a scanner.  
It should be. It should be a function of anything that scans.  
That type of report.

**Pavel Frolov**   1:31:34  
Hmm.

**Val Levitan**   1:31:37  
So it should be a function of our database design. Because this information is available, we should be able to scan it at any time and present it to a player or an attendant or whoever it is.

**Juan Martinez**   1:31:51  
I mean that what what you described is definitely got to be built in. So if I take a ticket that is fake to a dispensing tower, I should get an invalid or zero funds when it is scanned.

**Nathan Carver**   1:31:58  
OK.

**Val Levitan**   1:32:06  
Correct, but I'm also suggesting adding an explanation.

**Juan Martinez**   1:32:11  
OK, OK.

**Val Levitan**   1:32:13  
So, so let's say a short report, invalid or extended report. This ticket was generated on such and such date, time used here, here and here. These are the times and cashed in on such and such time.  
So short report, not valid. Extended report with more data.

**Pavel Frolov**   1:32:32  
Mm-hmm.

**Juan Martinez**   1:32:33  
Sure.  
OK.

**Val Levitan**   1:32:41  
That should probably be our MVP for the database designers.

**Nathan Carver**   1:32:45  
Yes.  
So so when the ticket's printed.  
Um, is it the?

**Val Levitan**   1:32:55  
No, any any ticket that is presented to a scanner has either a short reply, not valid, or long reply.

**Nathan Carver**   1:32:59  
Is it OK?  
How does the ticket get into the database initially when it's?  
When it's first present.

**Juan Martinez**   1:33:15  
When it's generated at the machine.

**Nathan Carver**   1:33:18  
OK. And that's the Smith that's doing that?

**Juan Martinez**   1:33:22  
In yeah, in in this scenario, any of the devices that have a printer, we we agreed that the processing application on the POS is also acting as the Tito database server. So when a machine requests a cash out.

**Nathan Carver**   1:33:33  
The record.

**Juan Martinez**   1:33:39  
Through a Flexport or through a SMIB, the printer installed inside the machine will print out a ticket with the value and the barcode number that's been assigned from the processing applicant.

**Nathan Carver**   1:33:52  
Got it. OK, so there's a transaction that's happening there first before it's printed. OK.

**Val Levitan**   1:33:59  
It's it's part of SAS protocol.

**Nathan Carver**   1:34:05  
OK.  
Yeah. So then anytime that's scanned on our devices, we can.  
Easily indicate the status through a short summary or write a description of.

**Val Levitan**   1:34:18  
Right.  
Either short or extended summary.  
Either a message or an extended summary.

**Nathan Carver**   1:34:28  
Mhm.

**Juan Martinez**   1:34:37  
That Val, we agree that that message should only appear for a non-valid ticket. Obviously when they scan a proper ticket, we shouldn't waste their time with any messaging.

**Val Levitan**   1:34:52  
Yeah, we should just validate it just like a normal machine.

**Juan Martinez**   1:34:56  
Perfect. OK.

**Val Levitan**   1:35:00  
You then convert the ticket into a value. There's nothing to talk about.

**Pavel Frolov**   1:35:06  
Actually, for for theater, there is no enough historical information on the ticket, just produced time and value and nothing else.

**Val Levitan**   1:35:19  
Yes, but the historical information comes from the server application when it was first issued and which machine it will have.

**Juan Martinez**   1:35:19  
No.

**Val Levitan**   1:35:31  
Uh, when it was cached in right, it will have that information on the server.

**Juan Martinez**   1:35:38  
Right.  
Yeah, Pavel, we should be able to hypothetically, if you took the ticket home and we have an expiration of five days and you came back on day seven, it should say this ticket is expired. Or as Val said, this ticket was paid on January 1st at this time for this amount.

**Pavel Frolov**   1:35:51  
Mm-hmm.  
Mm-hmm. Yeah, definitely.

**Juan Martinez**   1:35:58  
Yeah.  
Nathan, could you slide the drawing over to the left? I I've got a Kia Tito ticket there or a Kia Flexpay ticket there at the bottom. The Pavel will is this printing of this barcode over on the side?

**Nathan Carver**   1:36:38  
OK.  
Uh.

**Juan Martinez**   1:36:53  
Limited to how the Flexpay kiosk is set up or we can produce this exact ticket with the smaller barcode on the left and right, even at the machines.

**Pavel Frolov**   1:37:04  
No, no, no, no. In case of Tita, it will be only one central central position at barcode because it relates to machine. We cannot influence on machine logic.

**Juan Martinez**   1:37:08  
OK, I'll.  
OK.  
OK, so I'll I'll add in a a standard ticket and relabel this one the E wallet ticket.

**Pavel Frolov**   1:37:27  
Yeah.

**Nathan Carver**   1:37:46  
OK.

**Juan Martinez**   1:38:10  
Anything else, gentlemen?

**Nathan Carver**   1:38:50  
Does that cover it?

**Juan Martinez**   1:38:53  
So.

**Val Levitan**   1:39:01  
Mhm.  
Yes, I think it covers it. It opens a conversation with the engineering team on how to treat.  
Validated Tito ticket what to do with them, but in my mind we can.  
We can conclude this it it opens up the the next stage of the conversation should be about the database that satisfies.  
The E wallet architecture and the Tito architecture.  
And the simple POS with Mothergoose architecture.  
So we now need to start diving in into database design and together with that we should probably start selecting a tech stack.  
And together with tech stock, we should probably start selecting the exact hardware.  
Capability by hardware I mean CPU and you know.  
You know, boards, etcetera. Again, I'm not an engineer. I'm sitting in front of Nathan, Pavel B and and Gennady being the the engineers. I shouldn't be saying what what should be next. I'm just exploring the conversation.  
From an administrative perspective, so please guide me on this. What should be next? What should be our next conversation?

**Nathan Carver**   1:40:48  
Yeah, I.  
So I think we can the design between E wallet and Tito look for the things that are similar so that we only have to build and choose once and then identify those different requirements between the two that have to be.  
Accounted for because ideally the Flex POS is a single device, single deployed application and it's configurable for e-wallet or Tito or both. However that needs to go into the location.

**Val Levitan**   1:41:26  
But we.

**Nathan Carver**   1:41:26  
And I think we have, we have.  
I think we have architect or as far as devices, boards, all that has been selected or maybe not, maybe the engineering team knows what they want to use.

**Val Levitan**   1:41:39  
Well, device devices, the devices and boards have been more or less identified, but we need to 0 in on the tech stack and the hardware solution inside of those devices.  
For example, we are racing against time on the design of the POS. We really need to nail this and so it's important to choose the right hardware for it. It's it's important to choose. Also, we're going to be quickly behind on on the.

**Nathan Carver**   1:42:03  
So I think.

**Val Levitan**   1:42:14  
Design of the database and we also are very limited on the internal resources for the design of the database. So we need to start this conversation with the internal team on selecting the tech stock and the architecture of the database while.

**Nathan Carver**   1:42:23  
OK.

**Val Levitan**   1:42:34  
To start pushing design of the Flex POS. So in the meantime, he is zeroing in over this weekend, especially engaging an industrial designer on our side and he's providing the industrial designer with the spatial design.  
Of the Flex POS. So the industrial designer will now have the spatial design. He'll he's going to put a cover over it. So we're going to create a industrial look.  
But when that is done, we should by then have already selected all hardware.  
Uh.  
Pieces that will go inside of that POS, including the CPU board.  
Including the touch screen, including the screen, the sizes, all of that has to be nailed. So Yanari could then quickly start working on the POS is going to have to work with.  
Tooling design people, the manufacturing people in order to produce samples.  
Then we'll need to.  
If if it's a Linux device, then in the meantime we have to prepare Linux kernel for it and.  
Some sort of hardware obstruction layer, like all of that needs to come into effect quickly.  
So tell tell me what needs to be done.

**Nathan Carver**   1:44:14  
OK.  
So for influencing the hardware selection, um.  
Now I was assuming we're running Linux and I think all the applications we're referring to here.  
Should be easily run on Linux, so I think it comes down to for selecting the board. I don't if Pavel if you have a board already selected.  
And if not, what do we need to make that decision?  
For the board.  
And then the database design. Um.  
That really it's just gonna be how much capacity do we have in processing power do we need for the database for the board selection? I don't think that's going to be. We don't need much of A design I think to make that decision. So that can be done relatively quickly.  
But then the database design will evolve independently of that, and we can move that along.

**Val Levitan**   1:45:16  
I think it's important to understand that as part of the database design, we have technological debt that accumulated in our own database design, previous database design, and I don't know to which extent this new design will.  
Uh, wedge into.  
The the the repayment of the technological debt that we have accumulated.  
So I think that will be one of the most difficult conversations to be had.

**Nathan Carver**   1:45:56  
OK.  
Um.

**Val Levitan**   1:46:00  
Do you have any opinion on this, Pavel?

**Pavel Frolov**   1:46:06  
Not exactly related to server, but for the devices that will be installed on the location, I would say we we will use Linux.  
Operating system we will use uh MySQL as uh database.  
Uh, we will use um Java.  
Uh for uh main applications, back end applications.  
And we will use React as a JavaScript framework to produce graph graphic user interface.  
It doesn't matter what will be the board, highly likely.

**Val Levitan**   1:46:59  
OK.  
I, you know, I rest my case. I just need to get into.  
Design stage.  
Nathan and Pavel, as far as I understand, our internal database team has not been a part of these negotiations and have not had a preview of the entire architecture or the entire.  
Scope of design. So naturally if you bring somebody in, it will take people some time to absorb it and there has to be a conversation that brings them up to speed on everything and.  
Having them understand the design particulars or design direction, the reasoning for it, etcetera.  
So we should probably start having these conversations.

**Pavel Frolov**   1:47:55  
Oh.  
Actually I'm doing this conversation on the probably not daily basis, but each second day I talk about changes in design, new thoughts about this, and actually I already shared with Dima and Sergey Smanov schematics.  
We we just review it.  
They they know that they already asked the questions this morning. I answered and we continue to to discuss what what will be the product in general.  
Actually, actually I will take, I will collect the questions, I will collect some some limitations after our internal communication probably.

**Nathan Carver**   1:48:38  
Um.

**Pavel Frolov**   1:48:54  
They can, uh, produce some ideas, but.

**Val Levitan**   1:49:00  
Alright, so.

**Pavel Frolov**   1:49:01  
Actually, we are in the beginning of the process, yeah.

**Val Levitan**   1:49:05  
OK, so take me through the calendar. What's next on the agenda? What do we need to?  
What do we need to do?

**Nathan Carver**   1:49:15  
Um, it sounds like we will start.

**Val Levitan**   1:49:16  
Somebody, somebody, somebody other than me needs to take the lead on it. I'm not an engineer. I don't know what needs to be designed.

**Nathan Carver**   1:49:27  
So I can create some data designs based on our conversations. At least that would help drive out what we're thinking, gives us a communication medium with the database team. I don't know if that would be helpful or more noise, but I can certainly start adding that to GitHub.  
Um.  
So that those those schematics the potential database scheme and solution for this.  
If that helps, get that conversation rolling. So then so database and settled on some of the design we need is messaging, keeping the location, all the devices In Sync, provisioning those devices, devices having the ability to negotiate.  
A master device for the flex ports, for example, devices detecting each other. We also have the security.  
How do we how do we securely identify a device on a network so that we're not getting spoofed by a new?  
A new device being added. Um.  
So those are the the checklists I have in my head that I think they're those are gonna be the heavy lists for the engineering team that we need to start exploring.

**Val Levitan**   1:50:53  
So you decide you're you're describing requirements, additional requirements for each of the device like we already understand the passport, remote initial setup, hot swap.  
Uh.

**Nathan Carver**   1:51:11  
Yes. So these are things that we have that we know we want. Then we have to get down to the details is how do we?  
How do we include the security with with these concepts and how do we do the new concept of negotiating the the master device at a location on the network?

**Val Levitan**   1:51:34  
OK, so this should be the topic of our next conversation to in in order to further this architecture, right? So when can we, when can we have this conversation?

**Nathan Carver**   1:51:43  
Yeah.

**Val Levitan**   1:51:47  
And and who should be in this meeting?

**Nathan Carver**   1:51:47  
Um.  
So I definitely myself and Pavel, and then whoever Pavel thinks should be included as well.

**Val Levitan**   1:52:01  
Do you need any prep time or do you need internal conversation prior to our discussion? Because I want to be a part of this conversation.

**Nathan Carver**   1:52:11  
Um.  
Correct. So I want to I'll put together my thoughts on this. I can have. So if if we repurpose tomorrow for an hour just to kick off the discussion, I'll have some information available then that we can talk about.

**Val Levitan**   1:52:28  
I I want to be. I want to be in the conversation tomorrow. This is too fresh for me. This is this should probably engineering eccentric conversation.

**Nathan Carver**   1:52:29  
Or we can wait.  
OK.

**Val Levitan**   1:52:41  
I suggest a conversation with me.  
Next week.  
Probably on Tuesday or Wednesday.  
That will give you 2 solid days to communicate with engineers or amongst engineers.

**Nathan Carver**   1:53:07  
OK, sounds good. So we'll next week.

**Val Levitan**   1:53:08  
So if you feel that Tuesday is a good day, then great. If not, then suggested day.

**Nathan Carver**   1:53:15  
OK.  
All right, sounds good. We will do that.

**Juan Martinez**   1:53:25  
And Nathan does, based on having this meeting today, do we need that meeting tomorrow or do you repurpose it for something else with a different with Pavel? I'm just asking.

**Nathan Carver**   1:53:38  
Um.  
Yeah, I think if we do tomorrow, we'll we'll focus more on just what this action item is for next week.  
And I guess Paab, I'll leave that up to you. Do you want to bring in anyone from the database team? Do you want to just we can decide how we want to talk through this with them and how to send questions? Just let me know your preference.

**Pavel Frolov**   1:54:01  
So.  
Let's make this meeting clear for three of us. I think I will definitely work with our developers to to take their ideas, probably or their vision.  
Of the pro project and probably I think we we will work tomorrow with particular requirements, particular requirements. I mean for example hot swap.  
Probably we will need to write down it in more details what technological it will require from from our our side.

**Nathan Carver**   1:54:46  
OK.

**Pavel Frolov**   1:54:50  
And what use cases will be in this case?

**Nathan Carver**   1:54:54  
OK, so we can repurpose tomorrow or we probably you can schedule a meeting with me and whoever else you want to bring for Friday or Monday.

**Val Levitan**   1:55:08  
I prefer for you to repurpose tomorrow for your internal engineering meeting.

**Nathan Carver**   1:55:15  
OK.

**Val Levitan**   1:55:17  
So Nathan Pavel, I already, I already cancelled myself out of that meeting.  
I don't believe that you need Gennari for this meeting, so there's no point wasting his time on this.  
I think it should be Pavel, Nathan and the database guys.

**Nathan Carver**   1:55:34  
OK, sounds good. We'll do that.

**Genadi Peari**   1:55:38  
My about hardware devices, may we speak a few minutes about?  
Because we have multiple devices which needs to be produced and we still, I see most of the devices still have a fluctuations on the specs and we we still think what to do, right?  
The first one, the POS is actually more or less already speced, like almost completed. So I would rather start working with the POS if we I may present.  
I would like to present the hardware, complete hardware spec. So we briefly go over see that we didn't miss anything because together with the industrial design we can start development.  
Actually.  
Right.  
Um.  
For the dispensing unit, for example, I see it's still fluctuating because it's still not ready to to speak it out. Same for the redemption center.  
So I would rather start working because it's really long. A lot of things needs to be to happen before it will look at the device.  
How about the next meeting? I'll present who starts from the POS and.  
We added to the.  
With the specs.  
All agree and then.  
Put the move.

**Nathan Carver**   1:57:36  
Start with the people.

**Genadi Peari**   1:57:36  
Oh, always want to finish all this architecture first to see if new things not pop up.

**Val Levitan**   1:57:45  
I prefer to progress the architecture and I prefer now start engaging the database design.

**Pavel Frolov**   1:58:08  
Oh.

**Nathan Carver**   1:58:21  
OK, so tomorrow will then be repurposed for the engineers and the database.

**Val Levitan**   1:58:28  
So.

**Nathan Carver**   1:58:28  
To talk about the design.

**Val Levitan**   1:58:30  
So then my then next week I would like to get engaged with Pavel and Nathan on the results of your.  
Negotiations with the database designers.  
I don't need them in the meeting. This is already Pavel and Nathan and the the the higher level.  
So my my question to you is, is one meeting enough for you or do you want to schedule Monday as a second meeting with the database designers?  
I I see it as a waste of time for you, Nathan, to spend more than an hour in each of the meetings. So I see it like I I see it as Pavel, Nathan and the database designers, then Pavel internal meetings with the database designers.  
Then Nathan Pavel and the database designers continue result and then Nathan Pavel and I.  
As the uh.  
Architecture meeting.

**Nathan Carver**   1:59:45  
So we have our Friday meeting we're going to use. We also have the Monday meeting. We can, we can use that as well.

**Val Levitan**   1:59:53  
I suggest I suggest you repurpose that meeting for your internal engineering discussions and and then Wednesday. Let's take Wednesday meeting and have an architecture design meeting.

**Nathan Carver**   1:59:58  
Yeah.  
All right, we'll do that.

**Val Levitan**   2:00:12  
Gennady, as far as design of the POS, hardly anything can change. The board has been selected.  
We understand that the capability of that board should be enough.  
Major components have been selected. You should go ahead and do spatial design, then do the industrial design, then just continue with designing the POS.

**Genadi Peari**   2:00:45  
OK.

**Val Levitan**   2:00:46  
If you want, we can have a POS review design for Friday of next week.

**Genadi Peari**   2:00:57  
OK, at least we all need to agree on all the interfaces that it covers everything, at least to see the list of all the interfaces and.

**Val Levitan**   2:01:10  
Please remember when you design a product, it must have a passport.  
And remote initial setup capabilities.  
And and sorry and the lease capabilities lease.  
So passport lease Rs.  
Each product that every product that comes from from JVL.  
This should be design constraints.  
Or design fundamentals, I should say.  
Or design minimals minimums.  
OK.

**Nathan Carver**   2:02:05  
All right, sounds good.

**Val Levitan**   2:02:07  
So we have our schedule. We have a schedule nailed Friday and Monday. This is internal engineering review. Wednesday we'll continue with in this in this forum on architecture and Friday we will do.  
POS design review.

**Pavel Frolov**   2:02:31  
Mhm.

**Genadi Peari**   2:02:31  
Sure.

**Nathan Carver**   2:02:32  
All right, sounds good.

**Val Levitan**   2:02:34  
OK, Nathan, please post dot MD recording.

**Nathan Carver**   2:02:39  
Will do.

**Val Levitan**   2:02:39  
Thank you very much.

**Nathan Carver**   2:02:41  
All right. Thanks everyone.

**Pavel Frolov**   2:02:42  
Thank you. Bye.

**Val Levitan**   2:02:42  
Bye.

**Juan Martinez**   2:02:43  
OK.

**Val Levitan** stopped transcription