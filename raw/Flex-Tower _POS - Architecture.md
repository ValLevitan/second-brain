---
tags:
  - meeting
  - system-architecture
  - communication
  - juan
  - pavel
  - val
  - flex-pay
  - technical
---

**Transcript**

June 13, 2025, 10:02AM

**\
Juan Martinez** started transcription

**\
Juan Martinez** 0:03\
The focus for this morning\'s meeting was to hear what advancements or
directions you\'ve made on the architecture side. So I\'d go ahead and
turn it over to you to start with.

**\
Pavel Frolov** 0:27\
So I will share my screen.\
So I just made made some general notes about the system in general. So
the primary purpose of the system to enable cashless.\
Transactions from tickets across EGMs.\
Supports and security, validation, tracking, redemption, credits to gift
cards.\
Either by automatically means or manually. It depends on what device is
used, either Tower or Flex POS.\
Next companions.

**\
Juan Martinez** 1:25\
Sorry Pablo, one one quick question on do I for the sentence above
either automatically via kiosk or manually they can they need to both
coexist. There could be a a location that has both the flex tower and
the POS. So I just want to clarify that that is your intention.

**\
Pavel Frolov** 1:27\
Yeah.\
Yeah, uh, we can write and or.

**\
Juan Martinez** 1:48\
Perfect.

**\
Pavel Frolov** 1:49\
So components of the system. First of all, the central part of flex data
server.\
General processing unit transaction coordinator, so it uses connection
via web security web sockets connection to.\
All all other components of the system.\
It it can be SMIP board units installed on each machine. It can be Flex
tower, it can be Flex POS, it can be technical laptops.\
Connected you during the initial initialization or set up and cloud
commit, yeah.

**\
Juan Martinez** 2:45\
Just to I just just to clarify on the laptops we\'re this is because
right now the Tito server has no no monitor or keyboard, correct. It\'s
OK. Yeah. Thank you.

**\
Pavel Frolov** 2:58\
Yes, yes.\
And then it communicates to to cloud server for configuration, firmware
updates, reports and logging.\
Hello world.

**\
Val Levitan** 3:21\
Morning guys.

**\
Juan Martinez** 3:22\
9.

**\
Pavel Frolov** 3:22\
And and the next communication will be to a third party cards provider
like Incol.\
So here section responsibilities, but probably a better word
capabilities will be we will discuss it. So validate ticket.

**\
Juan Martinez** 3:53\
Yeah.

**\
Pavel Frolov** 3:58\
One capability manage unique ticket issuance, activate gift cards.\
Store full system configuration and credentials. Maintain device
passport.\
Devices and checksums.

**\
Val Levitan** 4:21\
Sorry, this is for Tito server, right?

**\
Pavel Frolov** 4:24\
Yeah, yeah, yeah. This is, uh, uh, 40 to Sierra first, first section.

**\
Val Levitan** 4:30\
OK.

**\
Pavel Frolov** 4:30\
And role based access to web graphic user interface.\
The next device for the system will be a Flex SMIP slot slot machine
interface board. Install it on each EGM. It communicates using RS232.\
Via SAS to each machine, third party or JVL machine, Websocket
communication to Stata Sierra.\
Responsibilities or capabilities translate SAS commands to cheater
requests to validate cheater tickets and to produce new cheater tickets
in in case when player shouts.\
Uh, ensure communication to server.\
Next Uh Flex Tower.\
You ask with card dispenser.\
It can be installed on optionally, it can be installed on location.\
Hardware. It will equipped with QR scanner 6 inch or probably like this
six or five inch display with touch screen.\
Card dispenser.\
And magnetic swipe reader.\
It communicates to Tito server via secure web sockets and capabilities
scan Tito tickets display redeemable balance.\
Uh request uh and uh issue.\
A gift card.\
Here it it could be manually or automatically because we have.

**\
Val Levitan** 6:57\
Well, no, it\'s only automatically. Why would it do manually?

**\
Pavel Frolov** 6:57\
So.\
As I remember, we have a swipe reader on tower.

**\
Val Levitan** 7:20\
By you mean cards swipe, card swipe reader.

**\
Pavel Frolov** 7:25\
Yeah, on tower. So it optionally could be a manual.

**\
Juan Martinez** 7:31\
Yeah, Val, remember that next year when we switch to reloadable cards, a
player could conceivably already have his card in his hand, so we would
need to support that ability to.\
Uh, transfer the funds to a card you already physically have.

**\
Pavel Frolov** 7:53\
So probably a reward.\
More.\
Uh.

**\
Juan Martinez** 8:09\
Uh, yeah, just one.\
Just for Nathan\'s sake, yeah, Nathan, as it stands today, the gift
cards are not reload reloadable today. That changes next year along with
this June 1st date. So conceivably you could keep reusing and coming
back with the card that you already have.

**\
Nathan Carver** 8:26\
OK.\
So the the automatic wording here means it the issuing automatically
issuing a new one or manually adding it to an existing.

**\
Val Levitan** 8:46\
How would it automatically do it?

**\
Juan Martinez** 8:48\
When you scan your ticket, it auto auto dispenses. The card is what I
think Pavel meant here. You scan your ticket and it dispenses.

**\
Val Levitan** 8:55\
But it\'s but it\'s only the but it\'s only the dispensing part.

**\
Nathan Carver** 8:58\
Mm.

**\
Juan Martinez** 9:05\
Yeah, that\'s this. This sentence is act. How do you activate your gift
card? It\'s all you know. Once you scan your ticket, you communicate
with income and then it\'s automatically dispensed from the tower.

**\
Val Levitan** 9:19\
So when it dispenses from the tower, does it validate the card as well?

**\
Pavel Frolov** 9:26\
Yes.

**\
Juan Martinez** 9:26\
Yeah, it\'s a Yep, it\'s a fully ready to go gift card with whatever
monies you have transferred on to it from your machine cash out.

**\
Val Levitan** 9:37\
So the swipe credit card swipe on the side is for future capabilities.

**\
Juan Martinez** 9:47\
Yeah, Pablo is right. We definitely have a a swipe reader right next to
the screen on all drawings we\'ve done so far for the tower.

**\
Val Levitan** 9:57\
But that\'s I\'m I\'m saying I know we do, but that\'s for future
expansion.\
Expansion.

**\
Juan Martinez** 10:03\
Correct.\
That\'s correct though.

**\
Val Levitan** 10:06\
OK.

**\
Pavel Frolov** 10:13\
So one more here provide user friendly interface to communicate to
player. One more capability and in security section.\
Uh.\
Secure access to card storage. So this device needs have the capability
to open back door and fulfill stacker for these cards.\
Next Flex POS.\
Used by cashiers. It placed on cash tax.

**\
Val Levitan** 11:00\
One second, one second. I I don\'t know whether it should go into
capability or not, but we should be able to know how many cards
approximately remains in the stacker.

**\
Juan Martinez** 11:17\
Yes, yeah, there should be a a low card sensor.

**\
Val Levitan** 11:24\
I suggest, uh, I don\'t know whether to call it low card sensor or uh.\
Card counter or some sort of a optical ruler?\
That, uh, can indicate what the cards are.\
But but there should be some sort of a level indicator.\
Also, I think that the screen is the only.\
Um.\
The screen on the tower.\
Is the only communicator to to a player.\
So I think that the emphasis should be made on.\
On that fact that.\
I mean the words that for some reason the words don\'t come to me this
morning, but.

**\
Juan Martinez** 12:31\
You mean just a a user-friendly UI on the screen now?

**\
Val Levitan** 12:38\
Well, it\'s the only way to commute for instructional or directional
interface.

**\
Pavel Frolov** 12:52\
Mhm.

**\
Val Levitan** 12:56\
I mean, maybe it\'s obvious, but I don\'t know if we should add any
wording to it.

**\
Pavel Frolov** 13:01\
I.\
I think any line here related to capabilities need to be rewritten in
more details, but right now I think it relates to user-friendly
interface.\
Um, again.

**\
Val Levitan** 13:20\
And also and also you say it it\'s it connects to Tito server, but does
it connect directly to Tito server or does it connect through a router?

**\
Pavel Frolov** 13:34\
It doesn\'t matter. You can just say we have connection. How it
organized it\'s not important at this level.

**\
Val Levitan** 13:46\
OK. Yeah, good point. Yeah.

**\
Pavel Frolov** 13:49\
So, so next, yeah.

**\
Val Levitan** 13:52\
We should probably, we should probably say that tower may be mounted on
a counter or a pedestal, \'cause we should probably discuss a pedestal
as a.\
As an integrated component.

**\
Pavel Frolov** 14:14\
It\'s.

**\
Val Levitan** 14:20\
I think it\'s important to say that all of the components discussed here
in this meetings.\
Should be swappable by a non-technical personnel.

**\
Pavel Frolov** 14:37\
Um.

**\
Val Levitan** 14:45\
What it means is that if we have to swap anything on location.\
A location personnel.\
Can physically do it, but connecting or establishing connection. If
it\'s not automated, then it\'s not going to happen.\
So when device is replaced and it goes live, how do you make sure that
it starts talking and properly communicates?\
Do we scan a barcode or do we wait for a light to blink? Do we need any
indicators to troubleshoot things over the phone? How does it happen?

**\
Pavel Frolov** 15:36\
Uhuh.

**\
Val Levitan** 15:37\
These devices are in very large distances in terms of service.\
I think we should also use the language that these devices are
operations critical.

**\
Juan Martinez** 15:49\
Uh.

**\
Val Levitan** 15:57\
If they do not operate, then the entire location goes out of service.\
I think it\'s important to put these sort of sentences in it.

**\
Juan Martinez** 16:16\
The STM based OS Pavel, we\'re not gonna have like the hardware
limitation that we do on the machines, correct? I I don\'t want to use
the word hot swappable parts, but if you power the unit down and you
replace the card.\
Dispenser or the scanner and you power the device back up, it should
auto detect these. I think that\'s where Val is going that you know
there shouldn\'t be any extra effort besides replacing the parts
physically and they should reconnect automatically upon power up.

**\
Pavel Frolov** 16:56\
Mm-hmm.

**\
Val Levitan** 17:09\
I mean, I\'m sure you guys thought about it, but if it\'s a matter of
passport registration, the registration when after the swap should
happen automatically.

**\
Pavel Frolov** 17:24\
Mhm.

**\
Felipe Miranda Giorgi** 17:44\
Well, I have a question one, how is it done now in Florida when you swap
something and and games are are connected to the Internet, do they does
this passport update by itself or do you have to scan the code and input
the I mean scan the QR code and put the code that is given?

**\
Juan Martinez** 18:04\
Yeah, in in in most Class 3 casinos, Internet connectivity is not
allowed down to the EGM level. So yeah, we I I we set up the setup file.
I\'ve removed the hardware requirement, but when we do swap, we do have
to scan.

**\
Felipe Miranda Giorgi** 18:09\
Oh, OK.\
Oh, OK.

**\
Pavel Frolov** 18:22\
Um, OK, not uh commands is.\
So the next device is Flex POS.\
So I have already said it user by cashiers.\
Waste.\
On the cashier desk.\
Um.\
Preliminary it will keep it by 10 inches monitor with touch screen.\
Probably optional second screen.\
Pure scanner to scan cheater tickets and magnetic swipe reader.\
Um.\
And keep in mind probably that we need a special key that switch
operation of POS device to operational and set up mode.\
Because actually on the location this will be a device with bigger
screen so it will be able to to make settings of all other device using
this screen.\
Other device using this screen.

**\
Juan Martinez** 20:14\
Just to clarify, all other devices, I E Flex tower could be configured
from this device if they\'re networked together when you say other
devices.

**\
Pavel Frolov** 20:24\
I think yes, I think yes, we can think about this.

**\
Val Levitan** 20:30\
Pavel, this could be an option, but it cannot be. I mean, having a POS
does not guarantee that we have any other devices in the location.

**\
Pavel Frolov** 20:33\
Yeah.

**\
Val Levitan** 20:46\
Or or or not having POS doesn\'t mean that we don\'t have any other
devices.

**\
Pavel Frolov** 20:46\
Yeah.

**\
Val Levitan** 20:53\
So I don\'t know how much reliance you want to put on configuration and
I also want to comment on a a key. We call it an audit key or a setup
key. That\'s not a good idea for POS.\
Because PPOS the the best, the best way to get into service mode for POS
is to swipe a card.

**\
Pavel Frolov** 21:10\
Um.

**\
Val Levitan** 21:19\
Or to enter or to or to enter or to enter a password.

**\
Pavel Frolov** 21:19\
Uh, yeah, yeah, yeah.

**\
Juan Martinez** 21:24\
Yeah, password or PIN would be preferred.

**\
Val Levitan** 21:26\
Yeah.

**\
Pavel Frolov** 21:27\
Mm-hmm.

**\
Val Levitan** 21:29\
But uh, definitely not a mechanical key because it always gets lost
somewhere.

**\
Pavel Frolov** 21:46\
Yeah.\
Connectivity. So it\'s the same. So we\'ll use security web sockets to
communicate to Tita Sierra capabilities validate Tita ticket via.\
Scummed you are.\
Uh, swipe cards to activate.\
Uh, allow parcel redemption.\
1.

**\
Val Levitan** 22:25\
A partial redemption is not really a function of the.

**\
Pavel Frolov** 22:29\
Um.

**\
Val Levitan** 22:30\
Of of the POS.

**\
Pavel Frolov** 22:32\
I I think actually pressure will always suggest do you want to spend
some money to some goods and the rest amount to redeem to card.

**\
Juan Martinez** 22:49\
Yeah, but that that violates the actual law. The effective. Yeah, the
the law says effective June 1st, all transactions must go to the card.
Once they have the card, then they negotiate whatever merchandise or
cash they want to do.

**\
Val Levitan** 22:50\
Uh.

**\
Pavel Frolov** 22:55\
Yeah.\
Mm.\
Uh, OK, we will remove this.

**\
Val Levitan** 23:09\
No, but not only that. I mean if if there is any sort of processing, I
don\'t know. Do you leave it, leave it on the POS or up to POS?\
Or do you?\
Let some other external device like a server device.\
Uh.

**\
Juan Martinez** 23:36\
Well, Val, as you as you mentioned that they\'ll remember if we\'re
going to have this alternate new POS device that\'s sort of offline, it
needs to be able to fully process. I I wasn\'t going to bring it up yet,
but you know, so the the other offline mode POS needs to be fully
operational and and interconnected.

**\
Val Levitan** 23:50\
The.

**\
Juan Martinez** 23:54\
Com in com communications and all that.

**\
Val Levitan** 23:58\
The POS could never be offline.\
Because it always.

**\
Juan Martinez** 24:02\
But when I say offline from the Flexpay ecosystem.

**\
Val Levitan** 24:07\
Oh, I see. Oh, OK, the off of the internal network.

**\
Juan Martinez** 24:13\
Correct.

**\
Pavel Frolov** 24:17\
Um, one more capability for POS to provide graphic user interface.\
For some reports, like what was the transactions internally on the
system?\
And of course graphic user interface to show current balance and
operations that.\
That is, uh, proceed by.\
Um.\
Any questions related to POS?

**\
Juan Martinez** 24:59\
I get this is for Val. Val, do we want to finish this entire deck and
then bring up the new POS needs or or do we do it now?

**\
Val Levitan** 25:13\
How much do we have left or?

**\
Pavel Frolov** 25:13\
So.

**\
Val Levitan** 25:18\
It seems like POS was the last topic on Pavel\'s agenda.

**\
Juan Martinez** 25:23\
No, there\'s a bit more here.

**\
Pavel Frolov** 25:25\
Here just just some notes related to everything probably. So we will
need the external integration with income cards API.\
And cloud integration to to our server and in the future I think with
mobile application.

**\
Juan Martinez** 25:49\
Yes.

**\
Pavel Frolov** 25:52\
It will be used for firmware update, reporting, logs and so on.\
Um.\
So the last one, operational module, optional modules also related to
some monitoring communications and.\
Remote update. Now probably I will switch to some schematics for better
understanding. So here I tried to to place everything at at one
schematic.\
To show we need to understand that some components can be optional, but
all the location correct me if I\'m wrong, all the location will need to
install Flex Theta server as a center.\
Brain of the system and all the communication will be.\
Uh, go through this uh cheater server.\
So it has the security web socket communication tool snip to Flex POS
terminal and to Flex tower.\
And it has communication to cloud server. This is our JBL based server
to to work with leases to work with configurations to work with
firmware.\
Updates to work with reports and logs.\
Uh, next external Uh communication.\
Web graphic user interface access.\
Here I think it relates to mobile application, some sort of
communication, communication to.\
A director\'s laptop or technician laptop that can be access to the
system via graphic user interface.\
Next communication will be to support third party gift card API in com
right now.\
Um.\
So it seems.\
Seems that\'s all.\
Any question here with the schematic?

**\
Juan Martinez** 29:09\
Just to confirm that all in this implementation all of the API is is
being handled by the Tito server. So the the POS terminal and flex tower
are sort of.

**\
Pavel Frolov** 29:21\
Yes.

**\
Juan Martinez** 29:27\
Dumb devices and they rely on Tito. And I I\'m only saying that because
when we bring up this new additional POS device we need, we\'re going to
have to re-architecture that piece. So, OK, thank you.

**\
Pavel Frolov** 29:27\
Yes.\
Yeah.\
Yeah, I understand your question because actually we can make direct
communication in case when we issue a card directly from POS to income
or directly from Flex Tower to income, but discussing this.\
Internally, we decided that the structure, the architecture of the
system will be simpler if all the logic will be under the server and the
rest of the devices will communicate via the.\
Tita server. In this approach you will be able to install several tower,
several POS terminals and everything will work using the same
identifications placed on Tita server.

**\
Juan Martinez** 30:38\
Understood.\
And that that I mean Val, we need to consider in the next model of POS
whether we leave things as is and even in the offline POS, we still
insist on installing a Tito server at the site. So we don\'t have to
change too much here or we talk about.

**\
Val Levitan** 30:58\
OK.

**\
Juan Martinez** 31:05\
A more advanced POS device that could directly run the APIs to income
without the need for any other device on property.

**\
Val Levitan** 31:17\
I don\'t think it\'s more advanced. I mean, the device itself is
identical the way I see it, but it\'s the internal configuration that
probably will change, I assume. Anyway, let let Pavel finish his
presentation.

**\
Juan Martinez** 31:29\
Yeah, yeah, no.

**\
Pavel Frolov** 31:32\
Yeah, also it\'s open question related to Flex Tita server main
application because.\
Actually we can use this application and install it internally on Flex
pose or it can be installed on Flex tower.\
Utilizing working of Tita server, but entire architecture will be the
same, but the communication between Tita server and POS and the tower
will be internally within one device.

**\
Juan Martinez** 32:00\
OK.

**\
Pavel Frolov** 32:16\
It it possible up to us to to decide is it suitable for us to make a
little bit more difficult devices that contains multiple.\
Application on on the board.\
But right now general architecture like this.\
Um.\
Actually, uh, I I started some.\
Some schematic workflows.\
So I don\'t know, do we need this to review right now or?

**\
Val Levitan** 33:08\
I I don\'t think, I I don\'t think that we should review it at the
moment.

**\
Pavel Frolov** 33:12\
Mhm.\
So probably this is all for me.

**\
Juan Martinez** 33:23\
Excellent. So Valke, can we jump now into this the new sort of
freestanding POS device?

**\
Val Levitan** 33:25\
OK.\
Yeah, yeah. Do you wanna go with it or do you want me to do it? I don\'t
know.

**\
Juan Martinez** 33:40\
Yeah, I mean I you I\'ll start it if you know if and you just jump in if
you need to. So Val approached us the other day, which actually is a a
very clever idea is there\'s a a ton of operators that want to.

**\
Val Levitan** 33:45\
OK.

**\
Juan Martinez** 33:56\
Put in as little effort and certainly as as little expense as possible.
So what if the locations could remain the way they function today? Newer
equipment, older equipment without printers and we had only a.\
POS installed at this device at this location, but this new POS was a
fully self-contained unit where they would cash out through Mother Goose
and then we have no connections needed to Mother Goose.\
Would be a manual process of entering the dollar amount from the Mother
Goose ticket, a few relevant fields from the Mother Goose receipt for
tracking purposes, and the cashier could create the gift card at the
window without the need for any additional hardware.\
At the machines and without the need for any operational changes for
these locations today. So that\'s why I said, hey, maybe this is a more
robust POS device that has to directly communicate with the income
APIs.\
But nothing else internally to do this.\
So it Pablo, it sounded like you confirmed that whatever code or logic
is in the Tito server could be made to run on the STM hardware in
principle.

**\
Pavel Frolov** 35:32\
Um.

**\
Val Levitan** 35:32\
I just want, I I just want to qualify. We\'re not looking at STM, we\'re
looking at ARM processor running Linux.

**\
Juan Martinez** 35:42\
OK.

**\
Pavel Frolov** 35:44\
Yeah, it.

**\
Val Levitan** 35:45\
Because thinking about STM is probably very limiting and I would like
engineers to have an ability to choose whether to choose ARM or STM. I
don\'t. I don\'t want to dictate that.\
Also we have more of a Linux. We are more of a Linux house than than an
STM embedded house. So for us it\'s better to function on on Linux.

**\
Juan Martinez** 36:14\
Oh, agreed. So does that mean that we won\'t be using STM even on tower
or on flexport?

**\
Val Levitan** 36:15\
We also got.\
Flexport is definitely STM. I mean, it\'s a it\'s a done product. It\'s,
you know, we\'re we\'re there. Tower is a choice that we need to make. I
don\'t want to make it the subject of this meeting right now.

**\
Juan Martinez** 36:37\
OK.

**\
Val Levitan** 36:42\
But with cash register we are inclined to think that it\'s should be an
ARM processor running Linux. We we found an extremely compelling
hardware now from one of our core suppliers.\
In China, and that\'s extremely appetizing proposition.\
By appetizing, I I mean quote UN quote.

**\
Juan Martinez** 37:11\
Sure.

**\
Val Levitan** 37:16\
But we\'re gonna make we we\'re gonna have Pavel and the team to make
that decision.

**\
Pavel Frolov** 37:23\
Mhm.

**\
Val Levitan** 37:23\
Regardless, the theory here is, as Juan already explained, maybe I\'ll
just elaborate a little bit more, just, you know, maybe for Philippe\'s
sake, largely.\
So the situation today is, and again, I\'m going to map out for
everybody what the situation is. There are 35,000 machines in the state
with approximately 6000.\
I think 6500 locations.\
Which roughly puts us at 6-7 machines on an average per location, and
each and every location today is functioning. It\'s working. It doesn\'t
really need anything.\
And by installing something it will not roduce more money.\
So an operator is saying, man, come on, you came up with this
legislation and now, sorry, I don\'t realize my camera was off. I cannot
get into the building. I\'m.\
Sit sitting in a parking lot and I can\'t get into the building.\
Yeah, I look stupid on camera, OK?\
Um.\
Yeah, so uh.\
And and nobody today in the industry is saying, hey, Mr. Operator, you
know what? You really don\'t need to spend money. I mean, everybody\'s
pushing you to spend money, but man, I feel for you. You don\'t have to
spend this money.\
No, but people are saying, man, you got to spend 5000 or 3000 or 10,000.
Every machine has to have a printer. Every machine has to be connected
and if it\'s not connected, Oh my God, it it will be a horrible
experience.\
But truly, if you install printers, and if you connect all of the
machines, and if you install servers, and if you convert everything into
Tito model, do you think you\'ll make more money from it?\
I don\'t know. These are not casinos. These are street locations. And if
the operator chooses to go that route, fine, we\'ll be ready. But in the
beginning, what I propose, and it seems like one is agreeing with me
that, hey, let\'s go back to an operator and to say.\
Mr. Operator, you do not have to do any of it. You have a running
business. You are issuing tickets. You are absolutely complying with all
the legislative needs of the state.\
And this new legislation that is being forced on you, you could take
care of it very easily by installing this small POS.\
The mother goose will print the print the ticket just like it does now
behind the counter and behind the counter you just use the POS and you
pair this particular issue ticket.\
With a card that you have, you know stacked on your desk, you take any
of the cards. You enter a couple of details through POS on the screen,
through touch screen.\
And you pair up a.\
Card and you give that card to a player.\
And that\'s it. And that\'s it. And that\'s all you have to do.\
And whatever that little cost of of a.\
POS, you know what? We will lease it to you for, you know, three years
in exchange for exclusive contract with you.\
And that\'s it. And you don\'t have to worry about it. How much does a
POS cost? 1000 bucks? OK, so over three years, 300 bucks per year, like
you\'re going to pay a dollar per day for the POS.\
And that\'s it. And you got it going and you don\'t have to worry about
anything. And if in the future you decide that, oh man, this Tito
architecture is, you know, God\'s gift to the world and you want to
convert to it and you want to.\
Install your printers on the machines and you want to connect to a Tito
server on the location and you want all this infrastructure. Guess what?
You did not throw away this money. RPOS just like easily connects to it.
It could be your auxiliary device or.\
If it\'s really a pain in the neck for you, we will trade it in.\
For other equipment, you could have our tower and you could have our
Tito server and you could have printers and you could have flex port and
you could have sophisticated flex paid. Hey, and if you want we can
even.\
Discuss maybe installing ATM. I\'m fantasizing a little bit right now,
but.\
But yeah, I mean, everything\'s available to you. But to start your
business, Mr. Operator, you don\'t have to panic and you don\'t have to
start spending 10s of thousands of dollars just on hard cost, just like
on.\
Hardware plus labor, plus additional service, plus additional fills. You
know, one could tell you stories about filling all the printers with
paper.\
That\'s a that\'s a fun job too.

**\
Juan Martinez** 43:31\
Yeah.\
Full time job.

**\
Val Levitan** 43:34\
So.\
So that\'s I I think this is, you know, I I mainly mainly told the story
for Felipe because obviously Pavel got on to it very quickly, but I
wanted to Felipe hear the whole spiel.

**\
Felipe Miranda Giorgi** 43:45\
OK.\
I\'m sold.

**\
Val Levitan** 43:55\
It it makes it makes sense, right, Philippe?

**\
Pavel Frolov** 43:55\
Uh, actually.

**\
Felipe Miranda Giorgi** 43:59\
Absolutely, Val. And most people don\'t want to rush into anything, so
it\'s AI think it\'s a good solution. Excellent.

**\
Pavel Frolov** 44:06\
I I have only one one question. So I I see one disadvantage of the
system because.\
Passure will be able to issue many cards by himself without any
validation.

**\
Juan Martinez** 44:32\
So we we talked about that, Pavel, but that that\'s an operational
decision. By asking them to enter information that\'s on the Mother
Goose, we have married a cash out through Mother Goose to the card it\'s
attached.\
There\'s a it\'s assigned a number and whatever else we want to put on
there, but that that\'s that becomes a between the master and location
owner, an audit that they do. And if there\'s a mismatch, yes, I mean, I
thought like you thought originally, but.\
Then I realized, hey, I I I visited these locations, I I went with
Felipe and that you know they\'re OK doing it the way they do it today
and they could cheat the system. But it it it it\'s it\'s the low cost
solution that I think that they prefer no matter what. I agree with you
that there are.\
Some security concerns here, but I think the market is willing to
overlook that.

**\
Pavel Frolov** 45:36\
And actually we need to understand that highly likely they will work
through our merchant JVL systems and we will.\
Immediately give this this personal. We issue some cards for himself.
Probably we give this money immediately.\
But then we need to pay this money to income and and then try to to
investigate what is going on, who is the the person who.\
Take mining outside of the mutoguls system.

**\
Val Levitan** 46:33\
Actually, it\'s a solid argument. I like it.\
I I didn\'t think about it.

**\
Pavel Frolov** 46:40\
Uh, uh, bulb.

**\
Val Levitan** 46:41\
It\'s it\'s a new, it\'s a it\'s a new angle. It\'s a it\'s a good new
angle I didn\'t consider.

**\
Pavel Frolov** 46:47\
Actually, well, when we have spoken to Incom last time, probably you
remember that they say they said that they have a limit installed for
each location.\
So the cashier will not be able to issue more than, for example, 5000
per day or something like this. It will protect us, it will protect
location.\
Uh, from uh, such.\
Uh, such cases.

**\
Juan Martinez** 47:27\
And we could probably go ahead, Val.

**\
Val Levitan** 47:27\
I think we\'re.

**\
Pavel Frolov** 47:28\
Mhm.

**\
Val Levitan** 47:31\
No, no, go ahead. I I yeah.

**\
Juan Martinez** 47:33\
No, it\'s just, yeah, those are called throttling limits and I\'m sure
we could even work with income to bring them down to further enforce
security where we specifically have this POS only at a location, you
know where we can limit that that concern. I mean there there are other
tools.\
Tools from the income side to help protect us.

**\
Pavel Frolov** 47:53\
And.\
Yeah, we can think about some additional limits, for example to prohibit
multiple.\
Uh, card activation is big amount uh.\
30 hour for example.

**\
Val Levitan** 48:15\
Look, look at the at the end, at the end.

**\
Juan Martinez** 48:15\
Sure.

**\
Val Levitan** 48:21\
You cannot issue more total money out than the the machine produces,
right?

**\
Juan Martinez** 48:30\
Right, though to to Pavel\'s point.

**\
Val Levitan** 48:32\
Otherwise, otherwise you\'re committing a fraud.

**\
Juan Martinez** 48:38\
Absolutely, yeah. But to Pavel\'s point, we have no visibility directly
of the Mother Goose side. You know that that this becomes a conversation
between us, the master and the location owner. Because if Mother, if
people cashed out \$500 but we issued.\
\$800 in gift cards for the same gaming day. We won\'t know that
immediately that, you know, an audit has to be done and we are not Privy
to part of the data in that audit, meaning the actual locations.\
Cash out amounts. That\'s not something we have access to at all today,
nor is it even on intra lot site. So this this becomes an operational
issue between the master and location that we have to co-exist, but we
are temporarily on the hook for.

**\
Val Levitan** 49:33\
I think Pavel brought up a very valid concern. I did not think about it.
It is a valid concern. I think for the sake of this meeting, it\'s not,
it\'s not important.\
Uh, the overall architecture stands.\
It it actually kind of solidifies even more the Tito.\
Or a temporary wallet, whatever, whichever way we go. But yeah, I I see.
I see your point, Pavel. Great point. I love the argument.\
For the sake of this meeting, let\'s move on.\
But this is something really to consider.\
Maybe we should have a discussion with income.

**\
Juan Martinez** 50:29\
Yes, agreed, agreed. And one other point, Val, I thought about and why I
said there might be two different kiosks is because today your
smartphone can scan a receipt and you know optical character recognition
can auto populate.\
Whatever you want, so we can change the scanner on this particular POS
device to read whatever we want from the Mother Goose ticket, so that at
least the cashier believes we\'re scanning and reading something to help
alleviate that and reduce the manual.\
Data entry of the date and the number and and the sequence number of the
ticket. So you know, that\'s something I think we should explore as
well.

**\
Val Levitan** 51:18\
So I thought about that as well. What concerns me with in this scenario
is.\
How well the ticket will be scanned and if errors are made and there is
a reliance on it, I don\'t know if it\'s such a good idea. So I thought
about. I thought about maybe even storing or.

**\
Pavel Frolov** 51:39\
Yes.

**\
Val Levitan** 51:44\
Optical even chits just.

**\
Juan Martinez** 51:50\
Mhm.

**\
Val Levitan** 51:51\
Instead of capturing the numbers, just storing the actual image.\
So maybe that is a good idea too. I I don\'t know.

**\
Pavel Frolov** 52:00\
One one more idea to think if we connect a POS instead of their printer
and connect printer after our terminal.\
Then probably we can monitor all the data, try to find within this data
some numbers, validate numbers with what is entered by a cashier and say
sorry it wasn\'t this amount.

**\
Val Levitan** 52:19\
Oh yeah, yeah.

**\
Juan Martinez** 52:36\
Mm-hmm.

**\
Val Levitan** 52:36\
That\'s actually a fantastic idea.

**\
Pavel Frolov** 52:40\
But need some investigation if it\'s possible to to monitor data. Kindly
likely, yes.

**\
Juan Martinez** 52:49\
Felipe, do do we have any contacts at RKS that you\'ve ever dealt with?

**\
Val Levitan** 52:55\
Yeah.\
It\'s actually a very good idea.

**\
Pavel Frolov** 53:11\
You already have experience bypassing the bill acceptor by flex port.

**\
Juan Martinez** 53:11\
That is.

**\
Pavel Frolov** 53:21\
Wait, why should we try to do this with POS and the printer instead of?

**\
Val Levitan** 53:30\
Yeah, you\'re saying why? You\'re saying why shouldn\'t we?

**\
Pavel Frolov** 53:33\
Yeah, yeah.

**\
Val Levitan** 53:38\
It\'s a good idea.

**\
Juan Martinez** 53:43\
Just.\
It is.

**\
Pavel Frolov** 53:50\
Actually they use serial printers, so we just need the two arrest 232
connection on POS additionally.\
Want to input data from Mutagus and the 2nd to bypass same data on the
second port and try to analyze traffic.

**\
Juan Martinez** 54:29\
I guess Felipe, you mentioned that there might be multiple variations of
Mother Goose and or systems out there. You think what are you talking
about two or three or more than that because we would.

**\
Felipe Miranda Giorgi** 54:41\
Systems. I\'m unfamiliar with two the mother goose and the one Omega
makes fledglings. There are several, but here\'s here\'s my concern.

**\
Juan Martinez** 54:46\
2.

**\
Felipe Miranda Giorgi** 54:56\
If for instance, there are many occasions where the our and and I\'m
just speaking about our devices, right? I\'m not. I don\'t know what
happens with other machines, other manufacturers, but.\
For instance, with our counterboard, when it goes bad, it starts
printing odd numbers like \$39.00 payout or 3999999 or \$1.00 tickets.\
Right. And this is just from ours. But if this collect button is pushed
and it\'s in the and the signal is sent, if there\'s an error, how can
it go back before it reaches the printer?\
Or I mean what? What could be done there?

**\
Juan Martinez** 55:48\
Yeah, that that\'s the disadvantage of directly sniffing the
communication to the printer is you\'re trusting.\
30 year old serial data, whereas at least if the receipt is off, the
attendant already knows what to do or how to handle the situation. Maybe
they go back to the machine and verify what the amount should have been
or whatever.

**\
Felipe Miranda Giorgi** 56:04\
Exactly.

**\
Juan Martinez** 56:13\
You know, so we would lose that policing of that ticket.

**\
Felipe Miranda Giorgi** 56:18\
And remember we and remember we don\'t have a dedicated page in our menu
for Mother Goose printed tickets there in the transaction history. Yes,
you can see cash out, but after so many plays it disappears and I can\'t
tell you how many times.\
They have called me two days later about a dispute on a on a cash out
and I said, well let\'s go back and you know the latest history is 3
hours ago. So there\'s no way to tell if it really printed or what was
the value, what was the cash out value. I mean it\'s, it\'s.

**\
Pavel Frolov** 56:53\
OK.

**\
Felipe Miranda Giorgi** 56:56\
It\'s an inconvenience there.

**\
Juan Martinez** 56:59\
Absolutely. Yeah, Val. I mean the the the whole serial and we know
people cheat with these handheld EMP jammers and shocking devices that
you know that we were told at several meetings that that remains.

**\
Felipe Miranda Giorgi** 57:12\
Mhm.

**\
Juan Martinez** 57:17\
In place. So we you know the possibility of getting false data from the
machines through the serial pulses is still prevalent.

**\
Felipe Miranda Giorgi** 57:19\
OK.

**\
Juan Martinez** 57:31\
We almost have to walk through a couple scenarios just to see, but
you\'re right, I mean, we would be on the hook for the encoded money on
the card until it\'s resolved.

**\
Val Levitan** 57:48\
Solid point.\
It may justify the the expense for the operator to convert to Tito.

**\
Pavel Frolov** 58:02\
So.

**\
Val Levitan** 58:09\
See, these are great operational inputs. I didn\'t have that
perspective.

**\
Pavel Frolov** 58:18\
Yes.

**\
Val Levitan** 58:20\
OK, regardless, nothing changes for this meeting.\
We continue moving in that direction.

**\
Felipe Miranda Giorgi** 58:31\
Yep.

**\
Juan Martinez** 58:33\
And Paul, will you be able to share that document and and that mermaid
diagram sometime?

**\
Pavel Frolov** 58:42\
Yeah, we\'ll try to find how to place it for your access.

**\
Juan Martinez** 58:51\
For now, a screen a screenshot is OK for now.

**\
Pavel Frolov** 58:51\
Definitely.\
Uh, OK.\
Because this this variant of online editor is limited to personal access
and only for two schematics probably need to switch to other.

**\
Val Levitan** 59:10\
OK, we can we can do it after the meeting.

**\
Pavel Frolov** 59:14\
S.

**\
Juan Martinez** 59:14\
Yeah.

**\
Val Levitan** 59:16\
OK, I I I think that concludes everything we wanted to cover.

**\
Juan Martinez** 59:20\
Yes.\
Yes, agreed.

**\
Pavel Frolov** 59:26\
I think I think I will add the additional solution with Flex POS as a
separate system to work with Mutagus shows that it\'s also possible
variant.

**\
Val Levitan** 59:26\
Um.\
Yeah.

**\
Pavel Frolov** 59:45\
That will that will join Flex Tita server plus Flex POS operation under
one device.

**\
Val Levitan** 59:55\
Felipe is um, what\'s the name of the company that produces this
motogus?

**\
Felipe Miranda Giorgi** 1:00:01\
RKS.

**\
Val Levitan** 1:00:03\
Is RKSRKSA player in this in this new market?

**\
Felipe Miranda Giorgi** 1:00:12\
Not really. This is like a Georgia based company. It\'s a gentleman and
his wife. He\'s been making this for years and years and years and not
really. It\'s not a strong. I mean, it\'s a it\'s a player because they
still sell, but it\'s not.\
Evolving into new, you know, new Mother Goose version 2.0 or something
like that that I know of now. Omega is more of the one with the new
device they brought. It\'s like a a separate or or another option for
Mother Goose.\
But RKS? Not really. It\'s the same. They made a newer version of the
fledgling about four or five years ago, and that that\'s about it.

**\
Val Levitan** 1:01:01\
It\'s a it\'s a husband and wife dying company.

**\
Felipe Miranda Giorgi** 1:01:05\
I I think so.

**\
Val Levitan** 1:01:05\
Yeah.\
Real quick.\
OK.

**\
Pavel Frolov** 1:01:13\
Hmm.

**\
Val Levitan** 1:01:17\
So what? What\'s our undertakings from this meeting?

**\
Juan Martinez** 1:01:25\
So we\'ve entered the second POS requirement and I\'ll share that with
everybody. For now I\'m calling it POS SAS and POS non SAS. Just to
differentiate the two, we we probably need to find a better name for
that.

**\
Pavel Frolov** 1:01:38\
Uh.

**\
Juan Martinez** 1:01:41\
And I\'ll start to review that with Nathan and and Pavel as a starting
point just to you know see if we really want to move forward with with
the offline POS as I\'m calling it based on this discussion that we just
had.\
But I think we should at least get get it documented and and in the
system.

**\
Val Levitan** 1:02:04\
But regardless whether we\'re moving forward with the second POS or not,
we are moving forward with the current architecture.

**\
Juan Martinez** 1:02:13\
Correct, correct. Yeah, that, that, the requirements already in as well
for that.

**\
Val Levitan** 1:02:23\
So my understanding is when requirements are written, we want to write
use cases.\
And we want to.\
Breakdown product into caabilities.\
And we want to connect use cases to.\
Discussion of features when we break it down in Jira, am I correct?

**\
Juan Martinez** 1:02:56\
Yes.\
That is correct.

**\
Pavel Frolov** 1:02:59\
Oh.

**\
Nathan Carver** 1:03:00\
Correct, right. We want to create a traceability from through those
different components of the requirements, building out requirements, use
cases, and I\'m assuming so you\'re all getting into GitHub, so that
traceability should go from.\
Wherever they exist in JIRA down into the issue trackers that the
engineers are working on so that we can we can see what\'s being
implemented and create a road map from that.

**\
Val Levitan** 1:03:27\
So this is where you made them come in. This is this is your.

**\
Nathan Carver** 1:03:30\
Correct. Yep. Yeah. So I want to bridge that gap so I\'m I\'m not
overlapping with or not redoing work that Juan and Pavel are doing, but
just complementing that by helping create that traceable bridge between
those.

**\
Val Levitan** 1:03:32\
Yeah.

**\
Nathan Carver** 1:03:47\
Between product and engineering.

**\
Val Levitan** 1:03:57\
Very quickly we\'ll have to start working on user interface, I guess
when we when we describe use cases.\
I\'m thinking out loud. Help me out if the the moment we Polish our use
cases.\
We should probably.\
Start working on graphic user interface based on use cases. Am I correct
on this or how does it? How does it technically work? I don\'t know.

**\
Ihar Hrybko** 1:04:31\
Yes we can and we need to understand do we rely on existing flex pay
user interface and ecosystem and then we can use some cases from from
the flex pay.

**\
Val Levitan** 1:04:42\
Yes.

**\
Ihar Hrybko** 1:04:49\
Integrated into Flex POS or Flex Tower. Yeah, we can make a.

**\
Val Levitan** 1:04:56\
Both Flex Flex Tower will largely borrow flex port behavior or
interface.

**\
Ihar Hrybko** 1:05:06\
Not exactly.

**\
Val Levitan** 1:05:09\
No.

**\
Ihar Hrybko** 1:05:09\
No, I think it\'s.\
The export is so different.\
Different device and with different purpose because in flex tower
basically it\'s for now for me I guess it\'s like flex pay without.\
A capability to insert money.

**\
Nathan Carver** 1:05:42\
Yeah.

**\
Ihar Hrybko** 1:05:43\
And only we have only one part to dispense card.

**\
Juan Martinez** 1:05:51\
Yeah, but.

**\
Ihar Hrybko** 1:05:52\
Flex dollar so.

**\
Val Levitan** 1:05:55\
So that.

**\
Juan Martinez** 1:05:57\
So it\'s more of a flex pay light UI.

**\
Ihar Hrybko** 1:06:00\
Yeah.

**\
Val Levitan** 1:06:01\
So that brings me. That brings me to the point.\
That um.\
The industrial schematic industrial design of Flex Tower.\
Is counting on using the same hardware sandwich.\
That is used for flex port which.\
assumes a 5-inch display.\
So I don\'t know how much of A graphic user interface can you port from
a 21 inch screen onto a 5 inch screen.

**\
Ihar Hrybko** 1:06:43\
Yes we can. We have some limitation, but in general for now the only
problem is if we\'re talking about on the player side screens is
keyboard.\
To enter e-mail or mobile phone, but in general.\
Can migrate. OK, this is not.\
Not exactly.\
I mean for the player, for a player to user-friendly like the biggest
big screen on Flex pay, but in general we make this user interface.\
Um.\
Oh, I think good and for this suitable for these cases.

**\
Juan Martinez** 1:07:54\
Read.

**\
Val Levitan** 1:08:02\
I understand. I understand what you\'re saying, but I\'m concerned.

**\
Ihar Hrybko** 1:08:12\
Well, we can make.

**\
Val Levitan** 1:08:14\
And if we and if we.

**\
Pavel Frolov** 1:08:18\
S.

**\
Val Levitan** 1:08:19\
And if it\'s going to be, forgive the expression, if it\'s going to be
an abortion.\
And we are stuck with five inch screen. That\'s a problem.\
And we need to make a decision.\
Two weeks ago on the size of the screen.\
So I don\'t know which way to go.

**\
Juan Martinez** 1:08:46\
So.\
Well, I mean, let\'s let\'s quickly get some use cases to Igor so we can
see what as an example, one thing we know Flex Tower needs is the legal
disclaimer for acceptance of the service fee.\
That that\'s a mandatory requirement. So we can argue that nobody reads
that and they\'re going to just swipe down and hit accept. But legally
it has to be readable. So that would be a perfect example. Igor, you
already have that text.\
How will it look like on the small 5 inch screen? Or how many pages will
it be if you have to increase the font size that that will help?

**\
Val Levitan** 1:09:32\
And and actually, and actually, I want to go along with what you\'re
saying, Juan. Uh.\
We are in America, which is highly litigious country, and if they say we
couldn\'t read it, it wasn\'t legible. They will sue us and the most
likely they will win and most likely it could be a.

**\
Juan Martinez** 1:09:48\
Right.

**\
Val Levitan** 1:09:55\
Um.

**\
Juan Martinez** 1:09:57\
Expensive.

**\
Val Levitan** 1:09:58\
Yeah.\
So I have to think about.

**\
Ihar Hrybko** 1:10:07\
Yeah, for these cases I will make interactive prototype. We can go
through all screens and make some corrections or even decide this this
screen size not.

**\
Nathan Carver** 1:10:22\
Oh.

**\
Ihar Hrybko** 1:10:25\
Exactly what we need. We go with bigger screen.\
So I make this supposed type in Figma.\
Before we actually go with actual development.

**\
Val Levitan** 1:10:47\
How long will it take?

**\
Ihar Hrybko** 1:10:49\
Uh well.\
I think uh.\
So.\
We can see something on.\
Maybe Wednesday 18 or 19. Oh yeah.

**\
Val Levitan** 1:11:16\
OK, let\'s do that.\
Let\'s have some mockups on a small screen because I\'m really concerned
now.

**\
Juan Martinez** 1:11:29\
So I\'ll I\'ll set something up for Thursday the 19th. Uh uh, this same
time Val.

**\
Val Levitan** 1:11:38\
Looking at the calendar.\
We could go at 7 if you want.

**\
Juan Martinez** 1:11:55\
OK.

**\
Val Levitan** 1:11:58\
7:00 or or 10:30 whatever time.

**\
Juan Martinez** 1:12:04\
Uh, I guess the the earlier the better for for me.\
Nathan, that works for you.

**\
Nathan Carver** 1:12:11\
Yeah, that works for me.

**\
Juan Martinez** 1:12:14\
Felipe, are you good with 7?

**\
Felipe Miranda Giorgi** 1:12:20\
Sorry, I was muted. Yes, Sir.

**\
Val Levitan** 1:12:23\
So our undertaking is for Thursday, June 19th to have a.\
Um, how do we call?

**\
Juan Martinez** 1:12:34\
A mock mock up for flex tower.

**\
Ihar Hrybko** 1:12:35\
Interactive prototype for only layer side because we actually.

**\
Val Levitan** 1:12:43\
Yeah, we want to. We want to test for sizing. That\'s what we want to
do.

**\
Juan Martinez** 1:12:46\
Yeah.\
So Igor, well, I\'ll I\'ll sidebar with you to go over what screens
don\'t apply to Flex Tower.\
Val, did you have anything else?

**\
Val Levitan** 1:13:28\
Thank you.\
So in the background, in the meantime, who is working with who and what
are we trying to move forward now?\
I\'m a little bit frozen, frozen in terms of thinking.

**\
Juan Martinez** 1:13:54\
Well, uh.\
Nathan and I will continue with the some of the use cases so he can work
with Pavel. We\'ll also work on use cases to give to Igor as quickly as
possible so that he knows what screens we need to at least see from a
player perspective for this Thursday presentation.

**\
Val Levitan** 1:14:17\
So one your objective is to and I guess Felipe should be Felipe and Juan
is to.\
Expedite use cases for each of the personas.

**\
Juan Martinez** 1:14:32\
Yes.

**\
Felipe Miranda Giorgi** 1:14:34\
Yes, Sir.

**\
Val Levitan** 1:14:35\
And Natan\'s objective is to translate use cases into technical.\
Um.

**\
Juan Martinez** 1:14:45\
Capabilities.

**\
Nathan Carver** 1:14:47\
Yes, the use case discussions. Those should drive out binary
requirements that we can identify and then those requirements we can
translate into tasks for the engineers.\
And that\'ll show us the progression towards implementing each of the OR
satisfying the use cases. The use cases will align with capabilities,
that\'s correct.

**\
Val Levitan** 1:15:09\
And just.\
And just to be clear, Nathan, when you\'re saying tasks, those are on
the level of features because we really don\'t want to get in into
splitting hourly tasks.\
For developers.

**\
Nathan Carver** 1:15:29\
Correct. I\'m thinking of a when I\'m saying Tess, I\'m really just
thinking of a a work item in the in the GitHub backlog, not a. Yep,
correct.

**\
Val Levitan** 1:15:38\
Right.\
So something something that in GitHub you could open a feature branch.

**\
Nathan Carver** 1:15:45\
Correct. That\'s right. So we would want to take. So use cases will
drive binary requirements. This is just nothing more than for us to say
yes or no. We satisfy this particular requirement and a feature could be
made-up of one or more.\
Well, a feature will be made-up of one or more requirements. A feature
may also have multiple use cases, so there\'s no. I don\'t think
there\'s a one to one for any of those, but the one to one we do want is
is our batch of requirements being satisfied.

**\
Val Levitan** 1:16:11\
No, it\'s not.

**\
Nathan Carver** 1:16:17\
By all of the engineering work that\'s being done and we want to be able
to trace that so that we can quantitatively say that we are, we\'ve
satisfied all the use cases and and capabilities.

**\
Val Levitan** 1:16:30\
And Pavel, on your side, I understand that you\'re going to be thinking
of tech stock.\
Based on the architecture that you\'re proposing.

**\
Pavel Frolov** 1:16:42\
I I think I will drill down the architecture. We\'ll add some notes.
Probably we\'ll create some schematics related to communications,
communication schematics.\
Um.\
Seems that\'s that\'s all for for next week.

**\
Val Levitan** 1:17:11\
And next week we\'re saying Friday.

**\
Felipe Miranda Giorgi** 1:17:14\
Thursday.

**\
Juan Martinez** 1:17:15\
Thursday. Oh.

**\
Val Levitan** 1:17:16\
when we\'ll be able to cover everything on Thursday.

**\
Pavel Frolov** 1:17:17\
So.

**\
Juan Martinez** 1:17:20\
Or or do we move the mockups to Friday and have it all as part of one
single meeting?

**\
Val Levitan** 1:17:25\
Then we need two hours. Then we need to start at six.

**\
Juan Martinez** 1:17:30\
OK.

**\
Val Levitan** 1:17:31\
Is it too early for Philippe and Nathan?

**\
Felipe Miranda Giorgi** 1:17:35\
No, I\'m good.

**\
Nathan Carver** 1:17:36\
No, that\'s not too early.

**\
Val Levitan** 1:17:38\
OK, so single singular meeting on Friday at 6:00 AM.\
Hopefully I\'ll get into the building all time.\
Philippa, this is the beauty of having your own building.

**\
Felipe Miranda Giorgi** 1:17:54\
Yes, yes.

**\
Juan Martinez** 1:17:54\
Yeah.

**\
Nathan Carver** 1:17:55\
Mm.

**\
Val Levitan** 1:17:59\
OK, gentlemen, so the work is carved out. We understand the
undertakings. I\'m always available. Knock on my door if you need.

**\
Felipe Miranda Giorgi** 1:18:11\
Thank you.

**\
Pavel Frolov** 1:18:12\
Thank you. Bye. Thank you. Bye.

**\
Juan Martinez** 1:18:13\
Thanks. Thanks everybody.
