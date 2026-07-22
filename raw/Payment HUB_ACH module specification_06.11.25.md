**Payment HUBACH module specification-20251106_070210-Meeting
Recording**

November 6, 2025, 12:02PM

2h 35m 45s

**\
Val Levitan** 0:08\
OK, who is crazy enough to start this meeting?

**\
Irina Shishko** 0:16\
Yes, I can do that.

**\
Pavel Frolov** 0:17\
So.

**\
Nathan Carver** 0:17\
Uh, well, I have a.

**\
Val Levitan** 0:21\
Here\'s here\'s the crazy one speaking.\
Go ahead.

**\
Nathan Carver** 0:25\
You\'re the you\'re the crazy one.

**\
Val Levitan** 0:27\
Yeah, the crazy one that\'s speaking.

**\
Nathan Carver** 0:34\
So I have a a a question on.\
I guess to you, Val, because you\'ve spoken with Dwala, but I I need to
clarify something with them and maybe you know, but let me let me share
my screen real quick.\
OK. So when we do an ACH transaction with Duwalla, according to their
documentation, the transaction always flows through the Duwalla balance
or also called the wallet.

**\
Pavel Frolov** 1:12\
OK.

**\
Nathan Carver** 1:26\
And from what I can understand in their documentation, this is the one
day transaction for a same day ACH. It goes from the customer or the
location.\
To the Dual wallet and then if we want to move it to a JVL.\
Bank account, that\'s actually another transfer that we have to
initiate.\
Um.\
And so this would be the flow of money in my head. Um.\
Then it would go from the location to our JBL Dwalla wallet and from
there we could transfer it to the JBL bank account.\
And pay income with that.\
The alternative is.\
And I\'m wondering if this is what Duala was discussing at all is that
we can use um.\
A virtual account number on the Dewalla wallet and actually pay income
straight from the wallet.\
So it would go from the location bank account to the JBL wallet on the
first day of the ACH and then when income pulls, they would pull from
this wallet rather than.\
Uh, Bank of America.\
So I don\'t know if this has been your understanding, if you\'ve heard
about this with Cody or anyone else from Diwala.

**\
Pavel Frolov** 2:45\
Oh.

**\
Val Levitan** 2:51\
So I have not discussed this and I don\'t know how to do it correctly
and I actually never thought of the difference or never paid attention
to it. So yeah, I I don\'t know.

**\
Nathan Carver** 2:58\
OK, I\'ll reach out to him.

**\
Pavel Frolov** 3:07\
May I may I say something? Looks like you are mistaken, Nathan. I think
it\'s not possible on. Probably it\'s not works in this order.

**\
Nathan Carver** 3:07\
OK.\
OK.

**\
Pavel Frolov** 3:23\
Actually we do not need to have some account like Dwolo wallet. I would
say something else for each account for each customer Dwolo creates seal
the name or some hash code.\
That we will use during our transactions and we will specify this hash
code, hash code for particular customer. It will be directly referred to
the bank account.\
Their bank account and as a destination point, we will specify hash code
of our bank account and it will be directly referred to our bank
account. It should be direct, I think.

**\
Nathan Carver** 4:02\
Mhm.\
Understood.

**\
Pavel Frolov** 4:18\
Um, transaction from bank to bank.

**\
Nathan Carver** 4:23\
OK.

**\
Pavel Frolov** 4:24\
And this bullet, probably this is not the correct word word bullet.
It\'s mostly let me check what\'s the correct name within duola.

**\
Nathan Carver** 4:34\
I believe it\'s referred to it the wall of balance.

**\
Dzmitry Chudzinau** 6:30\
What\'s your of issues?\
No, we\'re writing what you can find in source.

**\
Pavel Frolov** 6:35\
Hmm.\
OK.\
For finding source.\
So highly likely we just operate using a funding source ID value instead
of actual bank account.\
Actually, I I think you will need to investigate this according to the
API.\
Uh.\
Actually, when we spoken yesterday to Dwola, they confirmed that we will
need to work with the customers that are created as some non-authorized
customers.\
But me as JVL need to be an authorized recipient or a recipient or
client. Actually today we tried to discuss this internally.

**\
Irina Shishko** 7:37\
Yeah.

**\
Pavel Frolov** 7:52\
And at least we have.\
A question related to how customer will be created on.\
Dwola.\
Second, probably I\'m I\'m still trying to open the page and login to
the page.

**\
Nathan Carver** 8:16\
OK.

**\
Pavel Frolov** 8:17\
For some reason it\'s not working again.\
So probably.\
We can, uh, follow some.\
Some module description and requirements that Dima created in form of
documents today just to be on on the same understanding level.\
And confirm or decline what we are going to develop.\
Probably let me share my screen.\
So at least we need to to understand how terminal registration.\
Performed in our system.\
I will copy all this text and post it into chat.\
Oh, convenience.\
And I I think we will post this to GitHub just after we agreed on.\
All the steps.\
So we we assume that we need some special procedures when we firstly
run.\
Terminal software.\
Terminal equals to Flex POS right now.\
So first first of all we need to assign internal hardware number with
cabinet serial number as it was done previously for all of our machines
by showing.\
A QR code during first boot for registration and some authorized
personnel who logged into our system using his mobile phone can scan
this QR code.\
Then scan a barcode to to make this assignment within our server
database.\
This is just the steps describe it here.

**\
Juan Martinez** 11:20\
Mm.\
Pavel, why do we need the cabinet serial number?

**\
Pavel Frolov** 11:30\
We need the user friendly name of the terminal that can be easily found
in the system.

**\
Juan Martinez** 11:38\
So, so when you say cabinet, you don\'t mean the machine, you mean the
POS.

**\
Pavel Frolov** 11:43\
Your serial number.

**\
Juan Martinez** 11:45\
OK. OK. I\'m sorry. OK, perfect. Thank you.

**\
Pavel Frolov** 11:58\
So the difference between current procedures that we are doing on
machines you can find starting from FR008 because.\
Flex POS has its own secure scanner we can produce on mobile phone when
we made assignment.\
I internal IDV is cabinet serial number. We can answer in form of QR
code, present this QR code to the Flex POS device and you will
understand that.\
It has a registration and it can continue working.\
In production environment.\
Oh.\
So the the last requirement relates to case when the terminal is was
powered on, connected to the Internet to our server and server
understands that new POS device online.\
But it has still unassigned status.\
No cabinet serial number assigned for this cabinet.\
Any questions here or concerns?

**\
Alexey Khamin** 13:55\
You just store it.

**\
Pavel Frolov** 13:58\
Uh.\
Use. Yeah, in in most cases it\'s look it. It looks like use cases for
different steps of terminal registration procedure.

**\
Val Levitan** 14:20\
Sorry, there was something wrong with my computer. I had to log in and
back into the meeting.\
If there were any questions, if there were any questions to me and it
seems like I ignored it, please bring it up now.

**\
Pavel Frolov** 14:28\
Yeah.\
2.\
No, I just try to to explain what the terminal registration procedure
looks like and to do anybody do anybody has questions related to this or
concerns about steps?\
If no, I I would say that we will pose this in form of some description
and requirements in GitHub and JIRA.\
Oh.\
So yeah.

**\
Nathan Carver** 15:16\
Uh, Pavel is the.\
For employee authentication, they\'re logging into an existing system.
Is that CMS or is or is that a new system like the control server
that\'s gonna be accepting that login?

**\
Pavel Frolov** 15:22\
2.\
Um, good, good question. Um.\
You\'re talking about, uh, configuration server.\
Highly likely we will move everything related to terminal out outside of
CMS and highly likely it would be separate.

**\
Nathan Carver** 15:46\
OK.

**\
Pavel Frolov** 16:00\
Cloud control server, but it will still have the the same access to
authentication server.\
Actually it\'s it will use our LDAP accounts.

**\
Val Levitan** 16:16\
Yeah.

**\
Pavel Frolov** 16:22\
Um, correct me if I\'m on demo.

**\
Alexey Khamin** 16:26\
Mm.

**\
Pavel Frolov** 16:27\
The same and authentification server will be used.\
Yes.\
8.

**\
Dzmitry Chudzinau** 16:42\
On my system, well, some somewhere else.

**\
Pavel Frolov** 16:51\
So this this process is still in progress of moving from our CMS central
authentication server to Azure Cloud services.

**\
Nathan Carver** 17:08\
OK.

**\
Pavel Frolov** 17:15\
OK, so the next topic.\
Uh.\
OK.

**\
Alexey Khamin** 17:28\
Total here employee mode.

**\
Dzmitry Chudzinau** 17:28\
That the premiere.

**\
Alexey Khamin** 17:45\
OK.

**\
Pavel Frolov** 17:47\
Yes, resolution role, registrats, employees.

**\
Nathan Carver** 17:47\
So.

**\
Val Levitan** 17:58\
This is registration of what?

**\
Pavel Frolov** 18:02\
Terminal registration system terminal equals to Flex POS in our
discussion right now.

**\
Val Levitan** 18:11\
Well, let\'s talk a little bit about it. What\'s the mechanism? What
mechanism do we propose for terminal registration?

**\
Pavel Frolov** 18:24\
Practically the same as it exists right now for machines. We need
somehow to make assignment between internal serial number of let\'s say
motherboard ID with a cabinet serial number.

**\
Val Levitan** 18:40\
But so.

**\
Pavel Frolov** 18:40\
Some user-friendly IDs that can be easily found on the case can be
easily found within our system when you try to find this this terminal
on the server side.

**\
Val Levitan** 18:56\
So it\'s like passport registration on the machine and the purpose of it
is to give birth.

**\
Pavel Frolov** 19:00\
Yes.

**\
Val Levitan** 19:07\
Of of a device.\
And at birth, we\'re saying you were born with these genetic qualities.
You have this heart, you have this lungs.\
You have the kidney, etcetera, meaning that you have a CPU, you have IO
board, you have, but this is done at the factory level. This is when a
machine or a device gets created. This is the last stage of.\
Initiating the device.\
Uh.\
And so a machine or a device now gets a passport. But is this what being
discussed here? Because I think that we\'re discussing two different
things.

**\
Pavel Frolov** 20:01\
Yes, it\'s very close to passport registration procedures existing right
now for machines.\
Except for the last step that we can confirm registration on terminal
site by reverse procedure by presenting QR code on mobile phone to the
terminal.

**\
Val Levitan** 20:26\
Well, I I think what you\'re discussing here is when a terminal is
actually received on the location, the the location signed the agreement
already with us, we shipped the.\
No.

**\
Pavel Frolov** 20:43\
No, no, no, no. It\'s registration on assemble line.\
Uh.

**\
Val Levitan** 21:01\
Because I was under impression that what\'s being discussed is one step
before linking it to income.

**\
Pavel Frolov** 21:17\
Not exactly.

**\
Dzmitry Chudzinau** 21:19\
No, no.

**\
Pavel Frolov** 21:23\
This is just a burning of the of the terminal and how it can be burned
in server on the server database.

**\
Val Levitan** 21:38\
This is a birth. This is a birth. Uh, birth of a terminal.

**\
Pavel Frolov** 21:38\
So after.\
Yes.\
Sure.

**\
Dzmitry Chudzinau** 22:01\
Your pride is a broadly your priority.\
It is a registered.

**\
Val Levitan** 22:25\
No, no, I understand that, but this is a possible procedure.

**\
Pavel Frolov** 22:26\
Thank.

**\
Val Levitan** 22:30\
Like we we already have this procedure. Maybe we\'re taking, maybe
we\'re advancing this procedure to some other level, but we already have
this procedure.

**\
Pavel Frolov** 22:43\
Yeah, in general it described practically the same procedures as
passport registration machines.

**\
Val Levitan** 22:50\
But but why are we renaming this? I mean, we already have a passport
registration procedure. For example, right now I just got confused. I
thought we were talking about something else.

**\
Pavel Frolov** 22:59\
Yes.\
Because.

**\
Val Levitan** 23:03\
But the point that I\'m trying to make that we we already have passport
registration procedure.

**\
Pavel Frolov** 23:12\
Because actually for the terminal that that\'s I developed right now, we
will not have one wire EEPROM.\
And to set an extent, we will emulate passport.\
Somehow probably to assign special storage storage partition to place
this information instead of one wire E from.

**\
Val Levitan** 23:43\
The the one, the one wire EPROM or the Dallas chip as we call it is
simply a hardware solution to facilitate the requirement of machine
registration or passport registration.\
Whichever hardware solution you implement, it doesn\'t really matter for
the executive team as we all we know is that.

**\
Pavel Frolov** 24:01\
Um.

**\
Val Levitan** 24:11\
A device that we a device that is coming off the production line will
have a birth certificate or a passport or something that gives it give
gives this device a legitimacy to exist.

**\
Pavel Frolov** 24:18\
Mhm.

**\
Val Levitan** 24:31\
That that\'s the essence, that\'s the requirement for passport
registration. The fact that you said instead of issuing a paper
passport, we\'ll issue a passport in something in some other form.

**\
Pavel Frolov** 24:33\
Hello.\
It.

**\
Val Levitan** 24:48\
OK, that\'s fine, but it still will. It will still play a role of a
birth certificate.

**\
Pavel Frolov** 25:00\
OK, let let let\'s rename it to passport terminal registration.

**\
Val Levitan** 25:09\
No, I would like to name it exactly as we name it before. It\'s a
passport registration procedure. It\'s not a system.\
It\'s it\'s it\'s exactly what it used to be that there\'s there are no
changes. We\'re not creating anything new. We all know how it needs to
work. There is no mystery there.\
Again, I\'m I\'m underlying the point. I just got confused.\
Thank you.

**\
Pavel Frolov** 25:51\
Actually, actually it looks a little bit different from the regular
passport registration procedures. It\'s special for terminal.

**\
Val Levitan** 25:51\
OK, the functional.\
Well, we have a passport registration procedure. We have had it up until
now.

**\
Pavel Frolov** 26:09\
Mhm.

**\
Val Levitan** 26:13\
The fact that we are designing a new device or introducing a new device
in the market, it may or may not require and.

**\
Pavel Frolov** 26:18\
Mm.

**\
Val Levitan** 26:26\
An evolution of some sort of passport registration procedure.

**\
Pavel Frolov** 26:33\
Yeah.

**\
Val Levitan** 26:34\
Which is what you do now. But the question now as we evolving our new
passport registration procedure, what happens to the old passport
registration procedure? Is it? Is it also a time? Is it also the time
for us?

**\
Pavel Frolov** 26:35\
Agree.

**\
Val Levitan** 26:53\
To evolve, evolve the.\
Previous passport registration procedure for other devices. Maybe maybe
this procedure offers some.\
Interesting ideas. I again, I don\'t know.\
I just don\'t want to confuse this team by saying, well, this is
something that, you know, never existed before. No, I mean, it existed
before. We had this procedure in place. We have, we have been using this
procedure for many years. It maybe it has.\
Some inefficiencies that need to be addressed.\
Which is fine. Let\'s address inefficiencies. But let\'s not pretend
that we\'re creating something new. There\'s nothing new here. We have
this procedure in place.

**\
Pavel Frolov** 27:48\
Yes, in general, yes, except for it will be run on a different server
and different logic.

**\
Val Levitan** 27:58\
Well, well, I don\'t know. So now we have to have two servers. Why do we
need to have two servers? Why can\'t we have the old server evolve into
a new server and have one single server?\
It it doesn\'t seem practical for us to have two different servers.

**\
Pavel Frolov** 28:21\
Because right now we we need to continue working with all the cabinets
that were released.

**\
Val Levitan** 28:21\
It\'s a matter.

**\
Dzmitry Chudzinau** 28:27\
Best practice.

**\
Val Levitan** 28:33\
But but this is.\
But why is it different functionality? I don\'t understand.\
The the.\
A device we give where where a device is manufactured on a manufacturing
line. It\'s it\'s not active.\
We now need to activate the device and we created for this purpose. We
created a procedure which is called passport registration procedure.
This procedure aims to register.\
A device that\'s being rolled out of a manufacturing line. It doesn\'t
matter which device it is.\
But the procedure serves the same purpose. There\'s no other purpose for
this device for this procedure.\
So and and but and and we already have a database of a lot of devices
and I don\'t know, maybe that database needs to be converted, evolved,
moved forward, transferred to a new technology. Maybe there\'s a new
technology stack. I don\'t know what what\'s going on in your minds.\
But I certainly don\'t want to treat it as a new procedure. I don\'t
want to introduce it as a new procedure. I don\'t want to have two
separate procedures because it costs a lot of money to introduce each
and every procedure.\
And every time I rehire individual on my on my production line, it
requires new training.\
That you\'re that this is this is not an elegant solution. This is this
is just.\
A very direct and brute thinking.

**\
Pavel Frolov** 30:46\
Actually it will not introduce new behavior for a person who release or
register passport on the production line.\
It will looks the same, but actually it can refer to different server.
He will not see anything.

**\
Val Levitan** 31:02\
Maybe not.\
What happens? What? What happens when Sergey Tsimanov decides to go and
work for another company? How do I introduce a new replacement for
Sergey to this procedure? Should I tell him that I have two different
procedures?\
One is located here, another one\'s located here. This is the code for
this. This is the code for something else.\
Yeah, it is.

**\
Pavel Frolov** 31:33\
Yeah, yes, yes, we will need to to do this.

**\
Val Levitan** 31:35\
Yeah, yeah.\
But but is there another way?\
Maybe there is a better way. Right now we need to do that, but is there
another way?

**\
Pavel Frolov** 31:53\
Actually, I think this this will be our first approach to move.

**\
Dzmitry Chudzinau** 32:01\
Pash, it\'s in conference.

**\
Pavel Frolov** 32:04\
Um, yes, this now.

**\
Irina Shishko** 32:05\
Yes, yes, Lucia.

**\
Dzmitry Chudzinau** 32:06\
Oh, I don\'t need to move some groups online.

**\
Pavel Frolov** 32:06\
Yeah.\
So it looks like this this will be a first approach when we move
passport registration procedure to Azure services.

**\
Irina Shishko** 32:24\
Uh.

**\
Pavel Frolov** 32:26\
And in the future, in the future, I think all the registrations will be
evolved to this cloud server, but for some period it will be two
different servers working.

**\
Val Levitan** 32:26\
Interesting.\
Pardon. Pardon.

**\
Pavel Frolov** 32:43\
In parallel.

**\
Val Levitan** 32:44\
Pavel, my dear friend, now you\'re describing something else. You\'re
saying that the old procedure is dying out.\
And it will evolve into this rocedure.

**\
Pavel Frolov** 33:02\
Yes.

**\
Val Levitan** 33:03\
OK, my friend, that\'s a different conversation now.

**\
Pavel Frolov** 33:10\
I just want to say there is no right way and wrong way.\
We do not need to be black and white. We need to understand the entire
system and everything.

**\
Val Levitan** 33:26\
Yes, but I didn\'t understand it. I, you know, I thought that there is.\
OK.\
Let\'s move forward.\
Let\'s make a note to ourselves that the current procedure of password
registration is migrating to cloud and that brings changes to.\
How we?\
Manage.\
This migration.\
So now I understand it.

**\
Pavel Frolov** 34:15\
Mhm.

**\
Val Levitan** 34:16\
Did everybody, did everybody understand from the beginning that we\'re
migrating passport registration procedure to cloud? Was it clear for
everybody else?

**\
Dzmitry Chudzinau** 34:27\
No.

**\
Val Levitan** 34:30\
OK, that\'s.\
That\'s that\'s an important thing that we should.\
That should that we should.\
OK, moving on.\
No.

**\
Pavel Frolov** 34:49\
OK.\
Yes.

**\
Val Levitan** 35:13\
It would.\
That\'s a that\'s a great question. Pasha, can you translate this into
English? Or maybe I can try Alexey. Alexey, who\'s our QA engineer, is
raising an issue that we should have additional fields or a list of
fields that need to be filled out.

**\
Dzmitry Chudzinau** 35:16\
Yeah.

**\
Pavel Frolov** 35:20\
Oh, oh.\
Mhm.

**\
Val Levitan** 35:32\
And a.\
I think, I think what he\'s saying, what represents a positive outcome?
How does an operator know that there was a positive outcome during
passport registration procedure?\
Alexey, did I understand you correctly? This is this is what you said.

**\
Pavel Frolov** 35:54\
Yeah, yes.

**\
Val Levitan** 35:56\
So additional fields. So a list, a list of a list of fields.

**\
Dzmitry Chudzinau** 36:18\
Cars of experience.

**\
Juan Martinez** 36:40\
Can I just ask a question? Just to clarify, the question said, how does
an operator know of a successful registration? We we agreed that
passport registration is a production line.

**\
Val Levitan** 36:52\
By by by an operator, I mean an individual who operates the procedure.

**\
Juan Martinez** 36:58\
OK, OK.

**\
Val Levitan** 37:00\
Who, whoever, whoever makes that thing work. I don\'t. I don\'t mean an
operator, meaning the.

**\
Pavel Frolov** 37:10\
Yeah, in if we think on this requirement, I think we need to specify in
general terms that the graphic user interface will.\
Show something else from initial registration page. In some cases it can
be switched to working mode. In some cases terminal will show something
some messages like.\
You need to fulfill some some special fields.\
In in most cases, yeah, Flex POS will not be ready to operate right now.
It will require additional fields to be entered by some authorized
personnel to enter.\
Uh, yeah.

**\
Val Levitan** 38:11\
I think, sorry, respectfully, excuse me for interruption. I just want to
make sure that I\'m catching you at the right moment. I think we\'re
talking about two different things. So the the end of line now, so the.\
The product is ready and we want to marry all the internals with the box
that that it sits in. It doesn\'t mean that by marrying or initializing
everything it could actually be functioning fully functioning.\
In the location or registered in the in the system. So the fact that you
know the the firm where it checks out the.\
It registered all of the devices. It doesn\'t mean that it could accept
money.\
And and I for some reason proper taxonomy escapes me, but maybe with the
help of Nathan or Juan, maybe I could get proper taxonomy. But I believe
that we have a manufacturing.\
Kind of a live switch. Here\'s you know the product is manufactured and
then we have a registration procedure which is when a terminal, it could
be a machine, it could be POS actually is received by a location.\
And proper fields are entered. It connects to all the services and now
it goes live in the location. So I\'m struggling with the taxonomy of
things, but I believe that.\
Passport registration procedure is not a registration of a device on the
network.\
And I think here we\'re trying to, we\'re mixing two things.\
And we need to separate it. We we need to separate into two functions.
One is part of registration procedure.\
Another one again, I\'m struggling with the taxonomy.\
But.\
Operational registration.

**\
Pavel Frolov** 40:34\
Yeah, it\'s definitely relates to registration.

**\
Val Levitan** 40:41\
Some sort of operational registration.\
Which is different from passport registration.

**\
Pavel Frolov** 40:51\
No, this particular document describes only passport registration,
nothing more.

**\
Val Levitan** 40:58\
But entering fields, when when we\'re talking about fields, we\'re
talking about operational registration, right?

**\
Pavel Frolov** 41:01\
Yes.\
Yes.

**\
Irina Shishko** 41:04\
E.

**\
Pavel Frolov** 41:06\
Yes, yes, exactly.

**\
Val Levitan** 41:09\
So we were mixing this conversation. We\'re mixing two things.

**\
Pavel Frolov** 41:19\
Yes, yes, probably. Uh.\
Question from Alexey relates to operation.\
And actually nothing else except for message that device successfully
registered or not registered for some reason. That\'s the end of this
conversation.

**\
Val Levitan** 41:29\
OK.\
Miguel, I\'m sorry.\
I\'m I\'m dwelling on the taxonomy here. During password registration,
the device itself doesn\'t register.\
We\'re we\'re simply turning a live switch. We we\'re saying you now can
breathe on your own.\
But we\'re not connecting it to any of the services, so the the passport
registration procedure is quite limited and I\'m not sure that it needs
to have all these fields. Maybe it does, but the purpose of passport
registration is to marry.\
All of the internals.\
Of a device to an outside shell that has a serial number of it.\
And and that\'s it. So the positive outcome is the message of what
exactly it found internally.\
What kind of organs it found?\
What serial number it register registering?\
It gives you maybe gives you an opportunity to scan some internals if
you want to verify the outside serial number on the plate.\
Or to scan that outside plate.

**\
**43:13\
We.

**\
Val Levitan** 43:15\
And at that point it should say all the hardware is registered
properly.\
And passport is created.\
So that is the positive message, that is the outcome or some sort of an
error message.\
That would be a negative outcome, I mean positive outcome, but in the
negative scenario.\
And that\'s it.\
And I believe that Dima was answering some other question, but not
related to password registration.

**\
Pavel Frolov** 43:56\
Yes.

**\
Val Levitan** 43:57\
OK.\
So I\'m sorry for being so, you know, in English there\'s a word
nitpicking. I\'m sorry for nitpicking.\
But when I read passport registration procedure.\
Does it describe things as we just talked, or is it describing more?\
For example, temporary session ID for registration. Why do we need
that?\
Or terminal public key. Why do we need it here?\
And I don\'t know whether we do or we don\'t. I\'m asking a question.
No, it\'s it\'s actually on top.\
Yeah, here, yes.

**\
Pavel Frolov** 45:01\
Yes.\
Uh, so uh.\
I I think added something.

**\
Dzmitry Chudzinau** 45:13\
Temporary, temporary session ID.\
Terminal when you must at the pressure. Uh, then a switch might be
requirement.

**\
Val Levitan** 45:51\
No, no, I don\'t.

**\
Dzmitry Chudzinau** 46:21\
Yeah, got your box of this as now my business flow. The XPS just make up
new registrates. Yes, live registrates a passport.

**\
Pavel Frolov** 46:44\
I I will add something particularly for security. We have never worked
on a sign for machines some.\
Pairs of private and public keys because for machines we do not need
this, but for terminal as we need to communicate using security
channels, we need for each terminal.\
To make assignment particular.

**\
Val Levitan** 47:24\
I I.

**\
Pavel Frolov** 47:24\
Private, private and public key. That\'s why we will need to generate
these keys during registration procedure for terminal.

**\
Val Levitan** 47:27\
Bye.

**\
Pavel Frolov** 47:39\
That\'s what is different from the previous procedures for machines.

**\
Val Levitan** 47:43\
I\'m sorry, you\'re you\'re you\'re raising very good questions and I\'m
not arguing that point. If we need the public and private keys, that\'s
that\'s fine. Again, I\'m not a specialist and maybe this is a subject
for comments.

**\
Pavel Frolov** 47:56\
OK.\
Yes.

**\
Val Levitan** 48:00\
By Nathan or Juan?\
But from what I\'ve seen in registering other devices, for example, you
get a computer out-of-the-box.\
And a user at that point is presented with an ability to register public
and private keys.\
On a on a on an empty computer, on an empty box before before
anything\'s happening or after you install certain applications. I
don\'t know. Again, I\'m not a computer savvy person, but and and maybe
this is the case, but when the computer is created at a factory.\
Maybe they change ports, sorry, maybe they check ports, or maybe they
check certain firmware or ability to communicate somehow with outside
world, but do they really?\
Register public and private keys at the point of the birth of a
computer. Maybe that\'s the case. If this is the case, OK, I I don\'t
know the technology, but it sounds strange for me to assign public and
private keys at the time when the computer.\
Or in our case, POS. We don\'t even know where we\'re shipping it. It\'s
at the factory floor.\
So please take my comment with the qualifier that I don\'t know what
I\'m saying. I\'m simply hinging myself on the basic logic, which might
be erroneous. I agree.

**\
Juan Martinez** 49:40\
So on.

**\
Pavel Frolov** 49:40\
Would you would you like to hear my answer or?\
Cancel.

**\
Val Levitan** 49:45\
I would like it. I\'ve raised the question.\
I definitely want to know your your opinion and I want to know Juan\'s
opinion and I want to know Nathan\'s opinion. I am not looking to win
to. This is not a competition. I\'m not looking to win anything.
There\'s no medal at the end. I just want to create as much simplicity
and clarity for everybody in the room.

**\
Pavel Frolov** 50:08\
This is.

**\
Val Levitan** 50:10\
So if I\'m wrong, great, fantastic. It doesn\'t mean anything.\
Yes, I do want to hear opinions, please.

**\
Nathan Carver** 50:19\
OK. Pavel, could you ask that question again?

**\
Pavel Frolov** 50:26\
I haven\'t asked any questions right now.

**\
Val Levitan** 50:31\
So, so, so here, here\'s, here, here\'s the dilemma.\
We\'re looking at point number one that was renamed to passport
registration procedure. The passport registration procedure is a
procedure at the level of the end of the manufacturing line. So imagine
manufacturing procedure, you put all the guts inside of the machine, you
install all the peripherals.

**\
Nathan Carver** 50:42\
Correct.

**\
Val Levitan** 50:55\
And you install all of the firmware and whatever application needs to
turn on the screen. The screen is on and now the whoever\'s at the end
of the line assembling this point of sale machine.\
Says OK, the screen is on, the switch is on, the power is on. Now let\'s
go through initialization procedure ready before I put I unplug this
point of sale, put it into a box and ship it to a warehouse.\
This rocedure is called passport registration rocedure. The intent of
this rocedure is to capture all of the hardware, its serial numbers.\
Whatever firmware is installed to give us as much of the intelligence at
the point of releasing the product, what is it born with?\
Before we ship it out, before we lose control over it, the end of it. So
the end result, the end result of this procedure is to say go ahead, put
it in the box. I don\'t know where it\'s going to be shipped. You could
now put it in the storage warehouse.

**\
Nathan Carver** 52:00\
Understood.\
Understood.

**\
Val Levitan** 52:16\
What happens when it\'s in the storage warehouse?\
A sales is created. This unnamed machine, not designated for anything,
is shipped. It arrives on the location and it says OK, well, I\'m
out-of-the-box, the plug is in, I\'m turning on, I\'m live.\
But I\'m I\'m stupid. I need intelligence. Where am I? How I go? How am
I going to be configured? I don\'t know, depending on whatever
configuration is going to be fed into me.\
That is not a passport registration procedure. That is something. That
is something else.

**\
Pavel Frolov** 52:57\
That that\'s why it was named, why it was named as terminal
registration, because it a little bit more wider.

**\
Val Levitan** 53:07\
Right.\
Fine, fine. So maybe we need a second set. Now a terminal registration.
So this is where I know all of the insides of the machine. I know what
it is and now it\'s in different hands.\
It changed hands. First passport registration procedure. I have
different surroundings. I have a technician. I can call my engineer. He
can come to the manufacturing floor. We can adjust the procedure. We can
test it. We can troubleshoot it.

**\
Pavel Frolov** 53:29\
OK.

**\
Nathan Carver** 53:38\
Yeah.

**\
Val Levitan** 53:43\
We can change the components. We can do whatever we want. The second
procedure, as you call it, Pavel terminal registration procedure, is
where I don\'t have a technician, I don\'t have any tools, I cannot
measure anything.\
It other it either goes live or it goes in the garbage.\
Those are vastly different things.

**\
Pavel Frolov** 54:10\
So I I don\'t want to add more procedure between registration and and
onboarding on location.

**\
Val Levitan** 54:25\
Listen, I don\'t.

**\
Pavel Frolov** 54:25\
The simplest procedures, the the best for our future operation.

**\
Val Levitan** 54:31\
Listen, I don\'t want to add any any manufacturing procedures either. I
want to go from idea to my bank account.

**\
Pavel Frolov** 54:40\
I\'m too.

**\
Val Levitan** 54:40\
So, so, so I I think that POS terminals will create us \$5,000,000 per
year. Fantastic. Show me my bank account with \$5,000,000. That would be
the end of the procedure. Whatever happens in the middle, I really
don\'t care.\
But it doesn\'t work this way.

**\
Pavel Frolov** 55:05\
So let let me try to answer this is the most simplest way. So when we
switch Flex POS terminal the second time.\
After it was registered, we already need to initiate security
communication to our server at this moment.\
So before this moment we need to to have a pair of certificate.\
That\'s why we suggest to do this during passport registration.\
Because actually we are running this procedure in security environment
on our manufacturing line.

**\
Dzmitry Chudzinau** 55:56\
Do you?

**\
Nathan Carver** 55:57\
So you will register the POS before it leaves JBL.

**\
Pavel Frolov** 56:03\
Yes.

**\
Nathan Carver** 56:05\
OK.\
So this QR code will already be recorded. Go ahead on.

**\
Juan Martinez** 56:07\
Yeah, what what Pavel described it.

**\
Dzmitry Chudzinau** 56:11\
We should.

**\
Pavel Frolov** 56:12\
OK, let let me repeat I I think for a while. So the second time when we
power off power on terminal outside of GVL warehouse.

**\
Juan Martinez** 56:12\
No, sorry, it\'s.

**\
Pavel Frolov** 56:28\
Uh, we already need to make a security communication to Sierra.\
So at this moment we need terminal Flex POS need to know where of the of
certificates and apply encoding of of all the data.\
That why we suggest to add this procedure to to to generate pair of
certificates during the passport registration procedure because.\
This procedure is run in our security environment on the production and
nobody can steal channel of communication at this moment.

**\
Juan Martinez** 57:24\
It sounds like what what Pavel is saying. In order to deliver an almost
truly plug and play POS to the customer\'s hands, the the public key and
or session ID need to be assigned on the production line in a controlled
JVL environment.

**\
Pavel Frolov** 57:43\
Accept.

**\
Val Levitan** 57:46\
Maybe this is the case, but this is not.\
The the origin of this discussion was.\
That there are two steps. There is passport registration procedure and
then there is a terminal registration procedure. I\'m only using these
statements as I developed the my views on taxonomy.\
Um.\
So let\'s park it for a second. I believe that there are it\'s a it\'s a
two step thing.\
The second, the second point that Pavel is raising at which point and
how to ensure that the secure keys are.\
Entered into the machine, Pavel definitely knows better than I do.\
Accept.\
The the common sense logic tells me that when servers receive public
keys or assign public keys.\
There must be a developed procedure already that ensures that those keys
are secured.\
And not intercepted. So I I I highly doubt that we\'re breaking any
technological grounds by downloading keys.\
My reservation to having keys inside is is twofold. First of all, I
believe that internal fraud is more prevalent than external fraud.\
I want to make sure that it translates properly. You guys that Russian
speaking guys, do you understand what I\'m saying?

**\
**59:52\
Yes.

**\
Val Levitan** 59:56\
Fraud 3 company fraud pre downloading keys.\
I just translated from English to Russian.\
#1 #2 if we change anything procedurally.\
And changed our cloud server somehow functioned differently.\
The more that machines arrived with presettings or preprogrammed or
predetermined.\
It it presents more of an issue for us because the outside world where
we could change things easily.\
And then download information as we need it. If the machine is totally
blank, like it doesn\'t have any history or any keys or any procedures
or anything that needs to be erased.\
And then re download it, the better it is theoretically. And because
we\'re dealing with two worlds, one is cloud, one is physical. I think
that the physical world should be as undetermined.\
As undefined as possible.\
That is the only.

**\
Juan Martinez** 1:01:35\
But that I\'m, I\'m sorry that the only concern that I have there though
is, you know, these are not going to casinos where there\'s 20
technicians with tools and a bench. These are going to a gas station.\
With zero skill set from a technical level, so to deliver a nonworking O
becomes a nightmare.

**\
Val Levitan** 1:02:02\
If it cannot be configured through the cloud.

**\
Juan Martinez** 1:02:08\
Correct.

**\
Val Levitan** 1:02:10\
But we rely on full configuration from the cloud.

**\
Juan Martinez** 1:02:20\
So I I would then say because of the time difference between Georgia and
Minsk, unless that cloud solution is automated, you know we\'re we\'re
now asking the team to be available almost 24/7 whenever these devices
get delivered.\
So the question is, once the POS is is connected to a Ethernet or Wi-Fi
network, can the cloud automatically do everything without any manual
intervention?\
If it cannot, then we\'re right back to having that problem.

**\
Val Levitan** 1:03:04\
How does it change if the POS that arrives to a location doesn\'t work?\
We have amusement machines that are being sold right now through
Amazon.\
And we now don\'t trust our manufacturing QA in Toronto, so we\'ll bring
it to Miami and Andrei, before he ships every machine, diligently checks
each of the machines.\
Repackages, ships it to a customer. Customer opens up the machine and it
doesn\'t work.\
So if this will happen.\
With POS, we are heading into a a catastrophe.\
But equally the same as if the cloud doesn\'t work, but at least with
with the cloud, at least we have an opportunity to.\
Put fixes in.\
If we ship reconfigured machines, we\'re going to have to recall all of
the machines, bring it back to the manufacturing floor.\
Change something reboot.\
Or readjust or replace or reload.\
It\'s even more of a nightmare. I think that if something doesn\'t work,
it\'s a problem.\
But to me, I think it\'s better if something doesn\'t match in the
cloud. At least we have an opportunity to fix it remotely. This way I
don\'t even see any opportunities.\
But I think it\'s a valid point. If something doesn\'t work, it\'s just
it\'s a nightmare.

**\
Pavel Frolov** 1:05:09\
I think, uh, everybody on this meeting can understand this.

**\
Val Levitan** 1:05:14\
Yeah.\
For sure.

**\
Pavel Frolov** 1:05:17\
Um.\
But I do sure that the communications between Flex, POS and cloud server
on production environment need to be secured at the moment when we send
them our terminals.

**\
Val Levitan** 1:05:37\
Well, then it\'s a then it\'s a closed issue. If it needs to be secured,
it needs to be secured. So then.

**\
Pavel Frolov** 1:05:38\
At this.\
That\'s why we need the pair of public and private key at this moment on
the machine and the cloud server at this moment need to understand how
to communicate to this machine using these keys.

**\
Val Levitan** 1:05:59\
OK.\
But that\'s not a part of register passport registration procedure. This
is you\'re saying that after we have passport register passport
registered correctly, we need to initiate terminal registration
procedure consists of two steps.\
Loading your public key and loading your.\
A private key. That\'s what you\'re saying.

**\
Pavel Frolov** 1:06:29\
It.

**\
Val Levitan** 1:06:30\
But you don\'t want to, you don\'t want to face face the the truth. So
you\'re you\'re hiding behind the passport registration procedure.

**\
Pavel Frolov** 1:06:41\
I like this approach to hide some procedures within passport
registration.

**\
Val Levitan** 1:06:49\
Yes, but it\'s it\'s incorrect because if you hide the procedure and a
new technology comes out that could be that could erase this issue or
could remove this issue from our from our lives, it\'s hidden. You
don\'t know it.

**\
Pavel Frolov** 1:07:07\
If it described, it\'s it\'s known.\
Anybody else on this meeting also decide think that this is incorrect?

**\
Dzmitry Chudzinau** 1:07:33\
The manufacturer forces scan your QR code.\
No.

**\
Val Levitan** 1:08:05\
Terminal registration procedure at the new passport registration
procedure.

**\
Dzmitry Chudzinau** 1:08:19\
I could go on a personal documents.\
Yes, Sir.

**\
Val Levitan** 1:08:23\
Passport registration procedure.

**\
Dzmitry Chudzinau** 1:08:40\
No.

**\
Val Levitan** 1:08:42\
No.

**\
Dzmitry Chudzinau** 1:08:43\
I\'m in the company.

**\
Val Levitan** 1:08:46\
I am registering passport registering terminal.\
Yeah. Chui meets the via procedures. A passport registration procedure,
terminal registration procedure.\
He passed the youngest brush with the chimney at the procedure. Now,
yes, we do go in method, registrat the terminal.\
Transparency and alignment passport registration procedure.

**\
Nathan Carver** 1:10:04\
Oh.

**\
Pavel Frolov** 1:10:10\
Mm.

**\
Val Levitan** 1:10:14\
A terminal registration procedure.

**\
Pavel Frolov** 1:10:17\
Terminal registration procedure passport registration procedure.

**\
Val Levitan** 1:11:37\
As in my data.\
Passport registration terminal registration.\
Passport registration procedures, voice code, terminal registration
procedures, voice code.\
Nathan and Juan, the conversation is about either to hide the terminal
registration procedure under the passport registration procedure or to
separate it.\
I said both versions could exist, but my reference is to have it
visually separately.

**\
Juan Martinez** 1:12:50\
I I agree that this should just be renamed POS registration procedure
and then there should be a section for passport and a section for
terminal. To quote you Val, this way there\'s no tribal knowledge. It\'s
clearly documented what needs to be done with this device.

**\
Val Levitan** 1:13:09\
Yeah.\
I also agree with that.\
It\'s and and I I just want to develop this thought further. Maybe
terminal registration procedure will grow or maybe maybe shrink or maybe
amend. I I I don\'t know.\
But we as a company, we will know that the outcome of the terminal
registration procedure is, you know, 1234 and the positive outcome from
passport registration procedure is, you know, ABCD.\
And then Alexey also knows, and the key way knows, and it\'s easy to
describe.\
And it has a logical, logical.\
Kind of administrational differences.\
But I\'m not arguing that you could combine everything together. That\'s
fine, I just don\'t want to combine it.\
OK, let\'s separate it. Let\'s put terminal registration procedure and
let\'s put whatever you need on the terminal registration procedure,
please.

**\
Pavel Frolov** 1:14:29\
Mm-hmm. OK, clear.

**\
Val Levitan** 1:14:33\
Thank you very much. I\'m I\'m sorry that I insisted. I usually don\'t,
but this is important then.

**\
Pavel Frolov** 1:14:40\
Any questions left here?

**\
Val Levitan** 1:14:48\
OK, let\'s move on.

**\
Pavel Frolov** 1:14:52\
So the next procedure. Oh, sorry, it\'s not.\
Yeah.\
Location registration.

**\
Val Levitan** 1:15:06\
Procedure.

**\
Pavel Frolov** 1:15:08\
Yeah, I\'d like to proceed here.

**\
Juan Martinez** 1:15:12\
Oh, can you post paste this to chat as well?

**\
Pavel Frolov** 1:15:16\
Yes.\
I I would say that the key point of this description will be to
determine this 1.3.\
How we actually need to operate this duola accounts?\
Do we create customers within our production account and create for each
customer customer ID plus their bank account?\
Or each customer need to create its own account within Duolo.

**\
Juan Martinez** 1:17:57\
I\'m quite sure how to help you with that.\
Yeah, Pavel. So the the scenario is if Diwala goes away because we\'re
unhappy with their service and we replace them with somebody else, we
naturally want to save and maintain.\
All of our own customer information, so we could feed that to the new
entity. Hypothetically that replaces Diwala. So I I would say that we
want to keep a mirror of all of the customer information.\
In our own system, not to mention we also have to fill out the form
provided by income and their definition of the customer, which includes
the master, the location, both of their license numbers.\
So I definitely think that we need to maintain in CMS or elsewhere our
own customer database.\
Nathan, your thoughts on that?

**\
Nathan Carver** 1:19:04\
Um, yeah. So looking at how the customers they have.\
Verified customer and unverified customer.

**\
Pavel Frolov** 1:19:15\
Actually, when we spoke, sorry, sorry for interruption. When we spoke
yesterday, they said that our customer will be unauthorized.

**\
Nathan Carver** 1:19:17\
So.\
OK.\
Unauthorized or unverified?

**\
Pavel Frolov** 1:19:30\
Oh, I\'m unverified. Sorry, sorry.

**\
Nathan Carver** 1:19:34\
OK, OK. So if they\'re unverified based on how I\'m seeing the lifecycle
work, I don\'t think they need a Duwalla account. I think we can draw
straight from their bank as the source.

**\
Pavel Frolov** 1:19:35\
On this.\
OK.\
Yeah, I I also highly likely we will operate with only one dual account
in my understanding.

**\
Nathan Carver** 1:19:57\
Correct. I think you\'re right.

**\
Pavel Frolov** 1:19:59\
To to be clarified, but the question here for us it quite quite strange
when each client will share with us their account and ask us to enter
this account within.

**\
Nathan Carver** 1:19:59\
Right.

**\
Pavel Frolov** 1:20:17\
Let\'s say CMS account, CCMS location, more secure for customers just to
share with us ID, customer ID or.\
Um.\
Funding source ID and we can just use this numbers, but we do not reuse
their bank account directly.

**\
Dzmitry Chudzinau** 1:20:37\
Band and source.

**\
Pavel Frolov** 1:20:49\
But I will repeat again, I still think that they\'re highly likely they
will provide us a bank account just for simplicity.

**\
Juan Martinez** 1:21:01\
Well, yeah, well, they may not even have to provide it to us directly
because Diwala will provide the web interface for them to enter the data
and then we can probably just get an export from Diwala and mirror that
information into CMS.

**\
Pavel Frolov** 1:21:22\
But actually actually we we will have our JVL account and knowing this
account.\
We will be able to access the.\
Dashboard where where you can see everything. Sorry, sorry, not
everything. Actually the bank account is not is not fully reflected
there they.

**\
Juan Martinez** 1:21:47\
Yes.

**\
Pavel Frolov** 1:22:02\
So yeah, mask. Yeah, yeah, yeah, you\'re you\'re right. So in in
general, it it answers my question.

**\
Juan Martinez** 1:22:03\
A mask it.\
Well, they they mask it for view, but they do know the full account
number because they have to transact with it. So, so Diwala has the full
account, both the the routing number and the account number for their
bank and I don\'t see why we wouldn\'t be able to get that from Diwala.

**\
Pavel Frolov** 1:22:26\
Yeah.

**\
Juan Martinez** 1:22:30\
And and I\'m only saying, hey, if a year from now Dhawal is out, we at
least have all of that saved on our side and and should, you know,
switching over should be a quicker process to somebody else.

**\
Nathan Carver** 1:22:47\
Yeah. If they\'re an unverified customer, that means they\'ve never gone
through Dualis. So they don\'t necessarily have. We can keep their bank
account information and we keep the agreement, right, that we\'ve agreed
with them that we will. They\'ve pre-authorized us.\
To draw the money and JBL would be responsible to for keeping all that
documentation.

**\
Juan Martinez** 1:23:06\
Right, the earlier we.\
Sure. Which, which I\'m not necessarily a fan of. I mean, there\'s some
PCI compliance issues there that Diwala already complies with. So why,
why, why would we when we earlier said Diwala is going to create a
personalized JDL webpage, the customer goes directly there enters.

**\
Nathan Carver** 1:23:12\
Um.

**\
Juan Martinez** 1:23:31\
All the information. Why would we create our own if the Walla has done
that for us, at least for this go around?

**\
Nathan Carver** 1:23:39\
Yeah, understood. So when they when the customer goes to that site,
it\'s not clear to me is are they creating their own Duala ID or they is
Duala just providing a mechanism for us to capture the information?

**\
Juan Martinez** 1:23:56\
I\'m not sure yet.

**\
Nathan Carver** 1:24:01\
So Duwalla requires a Duwalla balance or Duwalla.\
What do they call it?\
Yeah, they call it the Duala balance. So one either the sender or the
receiver, one of them has to be a Duala.\
Verified business, verified customer with a Duwalla balance.\
So that would be JVL in this case. So that means the customer that we
draw from doesn\'t have to be verified as Pavel was saying. So they
don\'t even need a Duwalla balance, which means they don\'t have a
Duwalla account.

**\
Juan Martinez** 1:24:45\
So where does that unverified customer provide their ABA routing and
bank information to?

**\
Nathan Carver** 1:24:52\
Right. So that\'s it\'s. So Duwalla provides components that we can plug
into our site, but I don\'t. My understanding isn\'t clear on is Duwalla
actually capturing that or are they making a mechanism easier so it\'s
easier for us to capture that and we have to.\
We have to secure that that information on our side if they\'re an
unverified customer. If they\'re a verified customer, then they\'re in
Duwalla and alls we need is there.\
There\'s Walla ID and we can actually transfer money from balance to
balance, which is an immediate transfer.\
Um.\
That\'s my understanding of it.

**\
Juan Martinez** 1:25:36\
Sure.\
And then likewise, because there\'s a little bit different information
that income requires us to ask of the location, you know all of that
data should be combined under the one customer account in our CMS. So
CMS does need to be modified whether or not.\
Not we collect the Diwala data. We still have additional income data
that doesn\'t exist in our CMS today.

**\
Pavel Frolov** 1:26:12\
So actually I think we still need to implement some graphic user
interface.\
This list of different fields that the customer needs to enter by
themselves. Then part of this fields we can take for our internal
storage.\
And part of the entered fields like account number, bank number just
goes directly to API from Voila or any other provider.

**\
Nathan Carver** 1:26:40\
3.

**\
Pavel Frolov** 1:26:54\
To create new account on on to new customer on duola related to to our
account.\
And that and and finally we need to get dual customer ID.\
To use this use it in future to make transaction to this ID.

**\
Dzmitry Chudzinau** 1:27:31\
I don\'t understand session, uh.

**\
Pavel Frolov** 1:27:37\
Mhm.\
So actually for each customer that will be created by themselves.\
We will get.

**\
Dzmitry Chudzinau** 1:28:06\
Hmm. Push to release needs.\
Uh, customer location.

**\
Pavel Frolov** 1:28:13\
Yes.

**\
Nathan Carver** 1:28:16\
Yeah.

**\
Pavel Frolov** 1:28:20\
None.\
No, no.\
So the Dima again asked the question, are we going to use a scenario #1
or scenario #2? And I think we will need to ask this question or
footballer.\
So looking into the internal implementation from Duola for each customer
we will have.\
Funding source. Here we do not see exact account number from the
customer, but we will operate using funding source ID and this
particular number need to be transferred to our cloud server.

**\
Nathan Carver** 1:29:18\
Mhm.\
H.

**\
Pavel Frolov** 1:29:30\
Database Uh and will be used for further transactions.

**\
Nathan Carver** 1:29:32\
Yes.\
Yeah, so it looks like they don\'t need a Duala account. The Duala is
just proxying that information for us, so we don\'t have to store
account numbers.\
Yep.\
Right, exactly.\
OK.

**\
Pavel Frolov** 1:30:03\
Uh, actually if uh the uh operation scenario.\
What for scenario one, then all these customers need to be created
within our account.

**\
Dzmitry Chudzinau** 1:30:11\
1.

**\
Pavel Frolov** 1:30:22\
Customer will not have access to this account.

**\
Nathan Carver** 1:30:30\
Correct. The customer won\'t have access.

**\
Pavel Frolov** 1:30:31\
So.

**\
Val Levitan** 1:30:32\
I I would like I I would like to suggest the following. Yesterday when
we spoke to Dwala, they admitted that they have fallen behind in.\
In in their replies to us. So we have a bunch of agreements that needs
to be resolved, which should be resolved by the end of this week. When
the agreements are resolved, they will open a development cooperation.\
Between Dwala and JBL and all these questions that we are contemplating
right now, which have already been resolved with other companies, may
become trivial and they could provide us with.\
Answers very quickly. So instead of us spending time right now on
something that.\
May be answered very quickly by the wallet between the two engineering
teams. Maybe we should park these questions and then address them next
week or the week after when this channel of communication is open and in
the meantime focus our efforts on something that we can resolve
internally.\
Wouldn\'t that be a more efficient way?

**\
Juan Martinez** 1:31:48\
Yes.

**\
Pavel Frolov** 1:31:52\
Um.

**\
Val Levitan** 1:32:02\
I, I, I, I, I understand. I probably I\'m of tomb to me, JV on your
shine metal business.\
But the Moshe the business or chin yochi regulierum Bankovski
structori.\
He, I present only meet, um, legislative, I keep it up.\
It\'s a business and we made.\
Legislation regulation.\
OK, let\'s move forward.

**\
Pavel Frolov** 1:33:20\
Back.\
Yeah.\
Um.\
OK, we will wait answer on this question next week when we will be able
to communicate to technical personnel from Duvala.\
Understands this.\
Oh.

**\
Val Levitan** 1:33:55\
But by the way, just to be clear, when we\'re saying Dwala\'s
engineering team, it includes the executive side of Dwala. So they
assign an executive to us amongst the engineers.

**\
Pavel Frolov** 1:34:10\
Uh huh.

**\
Val Levitan** 1:34:13\
So it\'s not purely engineering back and forth. It, you know, we\'ll
we\'ll have our our executives and their executives speaking to at the
same time.\
OK, moving on.

**\
Pavel Frolov** 1:35:09\
OK, I think we will left this scenarios.\
To read by Nathan Juan Val and probably next question I will post next
document.\
Can you hear me?

**\
Val Levitan** 1:35:34\
Yes.

**\
Irina Shishko** 1:35:35\
Yes.

**\
Pavel Frolov** 1:35:35\
No.\
Yeah.\
Uh.\
So the next point will be Flex QS management system.\
So it\'s.

**\
Val Levitan** 1:36:21\
Sorry, I\'m at a loss. What what question is on the table now?

**\
Pavel Frolov** 1:36:34\
This this document describes Flex POS management system related to
location.\
It describes points that we need a back end and graphic user interface
to to assign particular flex POS to the location.

**\
Val Levitan** 1:36:45\
OK.\
What does management? What does management system mean?

**\
Pavel Frolov** 1:37:02\
Uh, do it.

**\
Val Levitan** 1:37:09\
Can you describe to me what we\'re trying to achieve?

**\
Pavel Frolov** 1:37:16\
To describe some procedures or some systems.\
That need to be done for operation of the XPOS payment hub.\
And communications between income and ACH.

**\
Val Levitan** 1:37:40\
Can you can you put? Can you copy paste this into chat?

**\
Pavel Frolov** 1:37:44\
Oh, not pressed send button. Sorry.

**\
Val Levitan** 1:37:49\
No problems. Thank you.

**\
Pavel Frolov** 1:38:45\
Dimas is.\
This problem, yeah.

**\
Val Levitan** 1:39:29\
So this document is describing how.\
Or I guess JVL.\
As a company manages the installation, linking and operation of Flex POS
terminal at merchant site, am I correct?

**\
Pavel Frolov** 1:39:58\
Yes.

**\
Dzmitry Chudzinau** 1:39:58\
Yes.

**\
Val Levitan** 1:40:04\
So this document aims to establish rules for verifying a location before
linking the terminal.\
The process to install and activate terminal at location, how leases
define operational time frame and how to maintain data integrity and
security for these relationships.\
Is that the purpose?

**\
Pavel Frolov** 1:40:34\
In general, yes, yes.

**\
Val Levitan** 1:41:25\
This is the suggested name.\
Is this what we\'re trying to do?

**\
Pavel Frolov** 1:41:39\
Um, everything except for guide.

**\
Val Levitan** 1:41:46\
Guide means manual. It\'s like it\'s another word for manual.

**\
Pavel Frolov** 1:41:50\
But.\
But we are trying to describe system, not the guide.

**\
Val Levitan** 1:41:53\
Well, put.\
We we tend to use the word system for everything that we don\'t know how
to call it.\
So we just apply the word system and I\'m trying to be.

**\
Nathan Carver** 1:42:18\
It\'s more like a SOP, right? A standard operating procedure.

**\
Val Levitan** 1:42:18\
I don\'t know if the system.\
Yeah, it\'s a SOP. Yeah, it\'s like, it\'s a it\'s a guide or SOP, you
know?\
They\'re being so instrued, you know.\
No, Tipoca constructs.\
Plan.

**\
Pavel Frolov** 1:43:06\
Management model.

**\
Val Levitan** 1:43:18\
Yeah, no.\
No guided by a Pisania that can instructs it. I\'m a robot and not
instructs it OK.

**\
Pavel Frolov** 1:43:30\
Done.

**\
Val Levitan** 1:43:33\
O Let\'s rename it.\
Plex POS deployment and credential management. You could call it SOP if
you would like standard operating procedure or a guide, whatever you
would like.\
Let let\'s let\'s put in the purpose. The purpose of this document. I
put it in chat.

**\
Pavel Frolov** 1:44:00\
Mhm.

**\
Val Levitan** 1:44:02\
Please copy copy the purpose.\
Is the purpose correct? Purpose is correct.\
Elik Tota, Alexey, Irina, Sergey, Brazil, Brokamin, Serge.

**\
Dzmitry Chudzinau** 1:44:39\
Correct.

**\
Val Levitan** 1:44:41\
OK, so.

**\
Dzmitry Chudzinau** 1:45:01\
At the Mario, isn\'t he Pistolinia \*\*\*\* Mabusum Mastro it\'s uh.\
The experience terminal uh application.

**\
Val Levitan** 1:45:28\
Deployment and credential management procedure.

**\
Dzmitry Chudzinau** 1:45:38\
That was most of one. It was web share.

**\
Val Levitan** 1:45:44\
I understand. Let me translate it. So gentlemen and ladies, below is
Dmitri\'s vision on Flex POS deployment and credential management
procedure.\
When the POS arrives to a location and Dima in this document is
triggering a discussion of his interpretation versus any of the comments
from QA from executive.\
Product management team, how do you guys envision the procedure?\
Oh.\
Yeah, so clear. Is it clear for everybody?

**\
Nathan Carver** 1:46:36\
Yes.

**\
Val Levitan** 1:46:37\
Let\'s let\'s comment on it.\
OK, I want to comment on the first thing, verified location. We left it
for comments by Duwalla. Am I correct? Because this is largely
unresolved subject.\
How do we go about verifying locations? We need guidance from Duala.\
Or guidance from income. Am I correct on this?\
Nathan, what\'s your thing?

**\
Nathan Carver** 1:47:41\
Uh, yeah.\
Is is this verified location meaning JBL understands this is a real
business location?

**\
Juan Martinez** 1:47:53\
Correct. That\'s it.

**\
Val Levitan** 1:47:54\
I think I love.

**\
Nathan Carver** 1:47:54\
Are not a Duala verified customer.

**\
Val Levitan** 1:47:57\
I think.\
Let me let me talk a little bit about my understanding of the
legislation, and this is where Juan can really weigh in. But let me
start with my understanding.\
It seems that the the US government in particularly is.\
U.S. government says, look, when money are transferred from point to
point, we want to know that there is no fraud and there\'s no
underground thing going on.\
And anything that that is over \$10,000 in transfer, we want to fall
under KYC, know your customer and we assign this responsibility largely
to the banks.\
And the accountants and the lawyers. But here\'s the small transfers,
400 dollars, 500 dollars, \$1000.\
There is no meaningful way of controlling and we as a government
recognize that this could be wishy washy thing. So you banks are not
responsible for it. Now the banks are savvy and they say huh.\
If I\'m not responsible, then I will explicitly say that this is an
unverified customer.\
And they created this.\
Inventory.\
Of definitions or definition of inventory of transfers that falls under
unverified customers, Duala says. OK, I am allowed to take transactions
from unverified customers to a verified.\
Destination. The verified destination is JVL. So JVL we will scrutinize
under KYC.\
JVL will take responsibility for the part of unverified customers. So we
the banks and we Dwala are arm\'s length to that relationship and
that\'s why we need JVL in this.\
Place JVL is saying. Uh huh. Hold on a second.\
I will say that unverify customer is the player, but I still need KYC on
the location.\
I\'m specifically pausing here.\
To allow one to comment and for the Russian speaking audience to
comprehend what I\'m saying and to ask questions.

**\
Juan Martinez** 1:50:56\
Yeah, so I mean the the Diwala portion can apply to this because the
flex POS terminal setup procedure #3 should be the same irrelevant of
who.\
Our partner for ACH is so on #3 where it says a verified location is
selected for terminal installation to to the Minsk team. Are we saying
that this is a drop down list?\
That is selected during the setup of the POS terminal.

**\
Pavel Frolov** 1:51:38\
I don\'t think that this is a drop down list, but highly likely for each
particular location it will be assigned terminal ID terminal number.\
These credentials from income. Some fields related to income will be
filled and assigned to this ACH.\
Uh.\
Good how this ID ID of the account and everything assigned to this
location.

**\
Juan Martinez** 1:52:14\
Yeah, so.\
OK. So I mean, so in this case, the verified location is basically the
income requirement where they asked us that they need up to 36 hours to
verify that a location and their license number are valid.\
With the Georgia Lottery to to that this location is authorized to do
GCOM business. So that is what this location definition means.\
Yes. So I I guess Val that the process is we use the income form along
with our contract with a new location that wants to enter business from
us once income has verified that that location and the license number is
legit.\
We can take the same information from the income form and enter it into
CMS saying that yes, this is a verified location.

**\
Val Levitan** 1:53:54\
OK, so in my view, the actual mechanics, the mechanism for taking
information that\'s required by Duala is through a web interface.\
That will be provided to us by Guala.\
While the income side of information right now.\
The way it\'s designed today is.\
In a hard copy agreement.

**\
Juan Martinez** 1:54:27\
But.\
Yes, spreadsheet, yes.

**\
Val Levitan** 1:54:31\
Which is unacceptable for a mass rollout.\
We we simply cannot manage it. It\'s just.\
It it requires a human uh.\
Presence in front of.\
For every, for every engagement.\
It\'s just it\'s not realistic.

**\
Juan Martinez** 1:55:00\
Yeah, but Val, I guess, isn\'t that Felipe\'s role when he\'s taking a
contract to a location and they\'re signing it and reviewing the
document?

**\
Val Levitan** 1:55:13\
But one you could give any role to anybody and they might be faithful
in.\
Uh.\
Complying with that role, but.\
Do you not feel that it this if you put an individual into this
position, you will create a massive bottleneck, procedural bottleneck?

**\
Juan Martinez** 1:55:40\
No, no, I I I agree. I\'m I\'m amazed that Incomm has this spreadsheet
requirement. But are we saying we should take the data and create our
own web form for the purposes of allowing the customer to enter this?

**\
Val Levitan** 1:55:57\
Yes, of course. And we should very we should find a mechanism. So we
should see, we should.\
Undress. We should undress all of the fields that income is required.\
And find the mechanism for verifying those fields in somewhat either
logical or automated.\
Procedure.\
I don\'t know what fields are in that Excel spreadsheet, but.

**\
Juan Martinez** 1:56:34\
I\'m posting it into chat right now.

**\
Val Levitan** 1:56:39\
Let let\'s pause for a second because I really want the Dima to
understand what I\'m saying.\
Diba, do you require? Do you want me to translate it into Russian?

**\
Juan Martinez** 1:56:49\
Hey.

**\
Val Levitan** 1:57:17\
Yeah.\
Compliance. So no Estrada. We had see with those name comply. Simuta
mush to dual a process.\
As.\
Income travel it.\
Uh, a new, uh, web interface.\
Uh.\
The other day store.\
Location, buoy to meet access, catamar interface.\
The premier location will enter their account. We motion thrust a
trigger function. Katori verified that account. The motion should are
activated. Clean the location.\
Excel.\
Samona Leechia.

**\
Pavel Frolov** 1:58:45\
So I.

**\
Val Levitan** 1:58:47\
Chilavieca E Excel.\
Create rocedural bottleneck.\
Principia with Australian implement here with not a large scale at the
still its web interface.\
Supported by someone at JBL remotely.\
Astrovoister on the NIT pushed to the cash the field. Most of it\'s most
of the of the Maticheski Verify and it\'s not the key top fields.\
To a principle for that mass roll out any visual motion.

**\
Pavel Frolov** 1:59:55\
No.\
Watching some new wires, watching some new wires, the the discussions.

**\
Val Levitan** 2:00:11\
What? What point?\
Probably. Yes, it\'s all. Yes, no, I\'m not James.

**\
Pavel Frolov** 2:00:49\
Web interface.

**\
Val Levitan** 2:01:08\
You are possibly correct. Pavel is saying that most likely Duala
interface will not work for us. And even if they provide Duala interface
and even if Duala provides interface, it will not be usable by us and we
will be forced to create our own web interface that we could.\
Migrate the data directly into our database. I said possibly. I don\'t
know, maybe.\
So Pavel is raising an issue. Do we?\
Interacting with the.\
This way I I don\'t have an answer, but regardless that my point is even
if Duala gives us the interface income doesn\'t.

**\
Nathan Carver** 2:01:55\
Correct.

**\
Val Levitan** 2:01:57\
And so for income side and can somebody pull pull up the table again?\
Yes, thank you. This needs to be ported hopefully in a in an automated
fashion or verified in an automated fashion.\
Again, if we are hoping of capturing.\
A sizable market share.\
So.\
Seeing the the fields now, how can we automate this rocedure?

**\
Pavel Frolov** 2:02:44\
I think we need to we need to implement to implement this web page that.

**\
Val Levitan** 2:02:44\
It\'s a question question to the team.

**\
Pavel Frolov** 2:02:54\
Customer need to be entered all the fields that he knows.

**\
Val Levitan** 2:03:00\
So, so part of KYC and and the reason I started Pavel, I\'m actually
commenting on what you\'re saying. I\'m I\'m taking it further when
customer enters fields.

**\
Nathan Carver** 2:03:00\
OK.

**\
Val Levitan** 2:03:13\
In a cute format by saying cute.\
Juan and Nathan understands what I\'m saying, but for the Russian
speaking people in this cute means.\
Um, as the quote Pavidinia could be a pot stuff come and you must put
stone out.\
But I\'m not not KYC. It does not yet know your customer.

**\
Juan Martinez** 2:04:21\
Yeah, and as Pavel put it there, the the customer can only enter some of
this information. We have to enter the kiosk terminal ID. And again, as
I said earlier, Felipe and the Georgia team, they have to 1st approach a
location.\
To, you know, discuss with them doing business with us and also give
them a contract to review and sign. So some of this has to be entered
also by the Georgia team as a starting point. I\'m about to do business
with this location.\
And so this needs to be entered by at least two different parties and
saved into one customer account.

**\
Pavel Frolov** 2:05:12\
We we have lost the wall.

**\
Irina Shishko** 2:05:16\
Mhm.

**\
Pavel Frolov** 2:05:25\
Yeah.\
That, that.\
Yeah.\
So this is an input point for income particular location. We need to
present all the fields, fill it to income and they will return us actual
credential related to this location.\
Only after this field is filled.

**\
Juan Martinez** 2:06:08\
Correct. And after they verified that the provided license number and
location are approved by Georgia Lottery and that could take up to 36
hours or three business days.

**\
Pavel Frolov** 2:06:51\
Oh, um, so do you mind asking uh do uh?\
Should we really check what the field is entered by the customer? How
can we be sure that this is correct and do?\
Incom also really check this values before provide us credentials for
accessing their service.

**\
Juan Martinez** 2:07:29\
Oh, Oh, yes. I mean, income can only do business with the location that
is authorized by the Georgia State Lottery, so they will most likely
verify this LLH, which is the location\'s license number.

**\
Pavel Frolov** 2:07:39\
Hmm.\
Yeah.

**\
Juan Martinez** 2:07:45\
Sadly, in Georgia, the location there is no master list because up until
this point we\'re only doing business with the masters and not directly
with the location. So Georgia does not publish a master location list
for us to even verify against.\
The lottery has to do that investigation and confirmation.

**\
Pavel Frolov** 2:08:10\
That\'s demo the the point of store in coma, sort of no boots, let\'s
change it because let\'s change in the.

**\
Val Levitan** 2:08:12\
Thank you.

**\
Pavel Frolov** 2:08:21\
What in for Matsu\'s night location? Metal for Matsu is times around.\
So the question is do Incom knows or probably have access to some
database? How to check license, license and other fields related to
location?

**\
Juan Martinez** 2:09:00\
I doubt it. Remember, this is going to the government of Georgia and
they want to give jobs and have 10 people researching this document so
they can justify their roles and be typical government waste. So I doubt
it\'s automated.

**\
Nathan Carver** 2:09:19\
Yes.

**\
Juan Martinez** 2:09:20\
It.\
Because the location might enter gas station 711, but that legally that
might not be the name that Georgia has. So there may be some back and
forth verification in case the location or the master enters the
information.\
Partly incorrect.

**\
Pavel Frolov** 2:09:44\
So if even in case when for example we provide fields that contain some
errors, for example in name of the location, but they can check or we we
see that one.\
Value is is wrong, but all the other is correct. We can continue working
with business.

**\
Juan Martinez** 2:10:08\
Correct, correct. I mean, I\'m I\'m sure the most important thing
they\'re going to check is that license number for either MLH, the
master or LLH, the location, and they will probably correct the proper
location name or if they\'re doing business as the DBA column there, J.\
They may have a completely different name because they\'re owned by
somebody else.

**\
Pavel Frolov** 2:10:33\
Uh huh.

**\
Val Levitan** 2:10:35\
But I question whether we should even verify this. Maybe we should just
take the information and leave it to.\
To income to verify.

**\
Juan Martinez** 2:10:48\
Oh, 100%. This is between income and the lottery. We we we\'re not
authorized to verify this because there is no master location list for
us to look up against.\
Yeah, if we had a master location list, it would be a lot easier for
Elipe to do businesses, but the masters prevent that list from existing.

**\
Val Levitan** 2:11:04\
OK, so.

**\
Nathan Carver** 2:11:11\
Oh.

**\
Pavel Frolov** 2:11:16\
So in in any case, I think location on our server should have different
pending statuses I would say related to.\
What account validation uh stage we we met?

**\
Juan Martinez** 2:11:40\
Yes.

**\
Pavel Frolov** 2:11:41\
And what is the current status of onboarding on incom site and only
after we get credentials from incom we actually can continue and can
enable this location for operation.

**\
Juan Martinez** 2:11:48\
Correct. Yeah, I.\
Agreed, yes. So the customer enters the information, they\'re pending
until we hear back from income and and again that could take up to three
days.

**\
Pavel Frolov** 2:12:11\
At at actually after entering the credentials of in from income at this
moment I think our server can try to initiate to.\
To call some API to say OK, we we are getting no errors from income
communication related to this location and we can validate actually this
credentials.\
At this moment.

**\
Juan Martinez** 2:12:45\
Agree.

**\
Pavel Frolov** 2:12:47\
At and at this moment we definitely will know that the account created
for customer also valid account and we can try to to initiate ACH with
this account.

**\
Juan Martinez** 2:13:05\
Yes.

**\
Val Levitan** 2:13:17\
So we\'re basically boiling this down to\
A web and web interface.\
The customer fills out the information. We pass it on to income.\
Let income reply to us.\
And we reply to the customer.

**\
Pavel Frolov** 2:13:42\
Um.\
Yes, but still have a question here in well now.

**\
Val Levitan** 2:13:50\
Yeah, I also am.

**\
Pavel Frolov** 2:13:53\
On our dashboard is all the locations. I think we have two options how
to for for initial point as an initial point I think for.\
Philippa could be just press a plus button to create new location, blank
location and he can enter name of location and that\'s all at this
moment.

**\
Juan Martinez** 2:14:22\
That\'s right.

**\
Val Levitan** 2:14:24\
What? Why? Why?

**\
Pavel Frolov** 2:14:25\
A special special link will be created and we can send this link to the
customer.

**\
Val Levitan** 2:14:33\
Why? Why do we need? Why do we need that?

**\
Juan Martinez** 2:14:37\
You do, Val, because remember, Felipe has to approach the location. Do
you want the JVLPOS? Do you want to do business with us? And here\'s a
contract.

**\
Val Levitan** 2:14:45\
I I\'m.\
I\'m sorry, I respectfully disagree. I don\'t think it we should be
doing this.

**\
Pavel Frolov** 2:14:53\
OK, let\'s switch to option #2. We just give a common link that anybody
in the world can be accessed.\
And then the customer can fulfill all the fields.\
And it automatically will create a location entity on our server.

**\
Juan Martinez** 2:15:22\
So.

**\
Val Levitan** 2:15:23\
No, no, no. It only creates an entity on our server after it has been
approved by income and develop, then it automatically creates an entry
for us.\
OK, OK.\
Right, right, right, right, right, right. We have to put it in pending
status, pending. And if it\'s approved, yes, I agree. Sorry. But yeah,
but but yeah, definitely, definitely this way, yeah.

**\
Juan Martinez** 2:15:53\
Yes.\
Right, but the Val the the.\
But remember, Val, because there is no master location list published,
we we we don\'t have a phone number. We don\'t have an e-mail address
for 711 number 2248 that\'s five miles away from the office because
Felipe has never contacted them.\
Up until now, the master has only been our contact.

**\
Dzmitry Chudzinau** 2:16:26\
Uh.

**\
Val Levitan** 2:16:29\
I\'m suggesting not to contact. I\'m suggesting marketing and through
marketing leading the locations to a particular website where they
entered their information, we create a pending status.\
For them within the same application, we should probably before they
even start an application, we should probably verify their e-mail and
cell number.\
Go through a simple cycle of verification. If they want to access this
account, we should ask them for their e-mail address. If we don\'t have
their e-mail address, we don\'t even correspond with them. We send them
an e-mail. So enter your e-mail validjvl.ca.\
Oh, sorry, we don\'t have you in our database. Let us send you an
e-mail. We\'ll send you an e-mail, verification e-mail. You reply. Oh,
so now, Val, we understand who you are. Your name, your last name.
What\'s your cell number?\
Cell number. We send an SMS, we verify it. Now we have the e-mail, we
have the first name, the last name, the cell number.\
Now we lead them to an application.\
Here\'s an application. Fill out your register, whatever register and
fills out all the application required by income and by Duolo. We put
him in depending status and we\'ll wait for verification. Now Felipe has
a full.\
Marketing target.

**\
Juan Martinez** 2:18:06\
But I I guess, Val, why? If I\'m a location, why would I fill out
anything when I haven\'t seen a contract that says JVL is going to
charge you an extra \$10 per gift card? Because that\'s our rule.\
You know, why? Why would I? Why would I buy a car without knowing the
price? You know what I mean?

**\
Pavel Frolov** 2:18:23\
Yeah.\
And and especially answering entering your bank account.

**\
Val Levitan** 2:18:28\
You\'re you\'re you\'re rising. You\'re you\'re rising.

**\
Juan Martinez** 2:18:32\
Exactly.

**\
Val Levitan** 2:18:33\
You\'re you\'re raising a very good point. So I went through this very
quickly. It may need stages. So the next stage could be here is our
pricing or our pricing could be as part of the initial page before you
even consider giving us your e-mail. Here\'s our.\
Rice structure.\
Maybe that\'s the way to do it, or maybe some partial disclosure, maybe
that\'s the way to do it. But I\'m just saying that this is a marketing
detail, doing it the other way where Philippe initializes the screen and
everything else.\
Leads me back to pointing that this is a bottleneck issue.\
But yes, I agree with you. Why would you give me information on my bank
account if I don\'t even know whether I want to do business with you?
And maybe the bank account is the last thing that we need to ask for.

**\
Juan Martinez** 2:19:36\
Well, technically it is because we we need to wait for Incom and their
36 hour window to say yes, this is a legitimate location. Then Diwala
comes next.

**\
Val Levitan** 2:19:37\
Oh.\
Right.\
Right.

**\
Dzmitry Chudzinau** 2:20:10\
The location of state process.

**\
Val Levitan** 2:20:18\
Maybe, but the address will be the location. The address might be the
same. They sorry, the e-mail might be the same, this cell number might
be the same, the first and last name might be the same, but we are
obligated to register each of the locations. So if let\'s say Val at
jbl.ca already.\
Exist.\
Maybe then I have I as a client have an ability to enter my other
location, so there\'s a plus sign. So I have my landing page. Val will
have his own landing page.\
And I can add additional location.

**\
Juan Martinez** 2:21:01\
Yeah, the the location license number or the master license number,
that\'s the key and it can have multiple or the same e-mail address if
one master manages multiple locations, but each one of those is gonna
have a different license number.

**\
Val Levitan** 2:21:06\
But.\
For me.\
We\'re we\'re not talking about master, we\'re talking about the same
location. Let\'s say Mr. Smith owns gas station ABC, gas station 123,
gas station 9/10/11.

**\
Juan Martinez** 2:21:33\
Right.\
Yeah, yeah. Each one of those has a license number, unique license
number. It may have the same contact information, but each one has a
license number.

**\
Val Levitan** 2:21:45\
And may have the same bank account.

**\
Juan Martinez** 2:21:47\
Yes, correct.

**\
Val Levitan** 2:21:51\
So Val Levitan val@jvl.ca Val\'s cell phone number, Val\'s account in
Bank of America account number ABC123 is the same, but it will be a
location gas station one.\
Gas station 2, Variety Store A, Variety Store B, and I may have ten of
those.

**\
Juan Martinez** 2:22:15\
Yes.

**\
Val Levitan** 2:22:17\
But as I like doing business with JVLI will keep on adding account in my
profile. I will wait for 36 hours for verification. My next account is
verified.\
And on and on and on.

**\
Juan Martinez** 2:22:34\
Right, yeah. Ideally during the form, if you when we ask would you like
to add a additional location, we should automatically move over the
contact information and the phone number, maybe even the the banking
information just to make it easier for the customer.

**\
Val Levitan** 2:22:44\
Yes.

**\
Juan Martinez** 2:22:54\
Customer and then let him edit if necessary.\
Although at the income form, the banking information is not needed at
that time.

**\
Pavel Frolov** 2:23:15\
So we can agreed at this moment that we need to create a requirement.\
For the customer to be able to log in to our service to see some
dashboard related to his locations.

**\
Juan Martinez** 2:23:39\
Yes.

**\
Pavel Frolov** 2:23:43\
And what else will we provide on this dashboard?\
Except for location, location, name, location, credentials and so on.

**\
Juan Martinez** 2:24:03\
So in in order to see the location, so Pavel, we\'re talking about
having a username and password for the customer to log on to our web
portal.

**\
Pavel Frolov** 2:24:16\
Yes, first of all we need to support all the features related to to
customers login, change password, verification emails and so on.\
But in addition to this, let\'s let\'s assume that a customer\'s logged
in to his account on our service. He can see two locations. He can open
each location and see some particulars.\
Fulfilled fields. What\'s the current field to entered? What else?\
Do we need to provide some financial reports or this is not MVP?

**\
Juan Martinez** 2:25:04\
Well, so once income has approved the location, we then need to allow
the customer to come back and enter their banking information because in
in order for us to debit their account, we need that, you know they owe
JVL the money.\
So we need that information, whether it\'s entered in CMS or Diwala or
both. It\'s just not clear yet.

**\
Irina Shishko** 2:25:28\
It.

**\
Pavel Frolov** 2:25:33\
So income credentials 1st and the account bank account enter in duola or
other ACH adapter the second one.

**\
Nathan Carver** 2:25:47\
Correct.

**\
Val Levitan** 2:25:50\
Yes, but Pavel, I\'m adopting your philosophy when you said we will
still need our own web interface.

**\
Pavel Frolov** 2:25:51\
And.

**\
Val Levitan** 2:26:02\
So when and how to present this information? It\'s just a matter of
discussing it or polishing it off.\
In further meetings, I think the undertaking from this meeting is
realization that we need our own web interface.

**\
Juan Martinez** 2:26:15\
Well, I.\
Sure. But just Pavel, do you know why we would need like Diwala does
this every day, 1000 times a day, so they know all the necessary fields
required. Why would we need our own web interface for the Diwala side?\
Of the data.

**\
Pavel Frolov** 2:26:43\
Because we need this data in our database.\
We need somehow to transfer this data. Let\'s assume that we do not
implement interface to dual for customer. In this case they will enter
all the fields and probably share with us just ID.

**\
Juan Martinez** 2:26:57\
Right.

**\
Pavel Frolov** 2:27:05\
Necessary for transactions, but what? What should we do with all the
rest fields to enter it by ourselves?

**\
Juan Martinez** 2:27:16\
No, no, I know what you\'re saying that and that\'s what I said earlier.
I mean, we are Diwalis customer. So there\'s probably an administrative
dashboard for JVL that lets us access all this information and it it can
probably be exported and then we import it.\
Is again, I don\'t know that for a fact, but I I got to think that\'s
possible. Would you agree, Nathan?

**\
Pavel Frolov** 2:27:39\
Uh, yeah.

**\
Val Levitan** 2:27:41\
Yes, but assuming, assuming that this is even possible, let\'s assume
that it\'s fully possible. We still do not have the income side of the
data.\
So if we are forced to make it for income, we may as well add the
dweller in the face.

**\
Pavel Frolov** 2:28:00\
Yeah, we we need to to make a alignment between our terminal and income.
It\'s better to do this in our database.

**\
Juan Martinez** 2:28:09\
Perfect.\
No, I understood. But we agree that the income web interface is for the
customer. The Diwala web interface is not for customer. That\'s more of
internal.

**\
Pavel Frolov** 2:28:25\
No.\
Yes, again, we are returning back to the question.

**\
Juan Martinez** 2:28:29\
OK.

**\
Pavel Frolov** 2:28:34\
Do the customer will use our account to create a customer entity within
or it will be a separate account with the customer?

**\
Nathan Carver** 2:28:49\
Yeah, I think we need to verify if if we can proxy that creation or if
they have to go to Duala site to enter in there at the very least their
bank account because the API and Duala provides an ability to create a
customer.

**\
Pavel Frolov** 2:28:54\
Yes.

**\
Nathan Carver** 2:29:06\
But looking at that API offhand, it doesn\'t have the ability to assign
bank information, so we may not be able to do that. The customer may
have to do that.

**\
Pavel Frolov** 2:29:15\
Oh.\
Yes.\
Seems I saw the same guy today.\
Yeah, link. Yeah, it was API to link uh bank um bank account to the
customer.\
It\'s available.\
Oh.

**\
Nathan Carver** 2:29:56\
It could be a different endpoint.

**\
Pavel Frolov** 2:30:32\
Sources.\
Oh.\
Create customer funds in source.\
This one.\
You need to specify a particular customer ID.\
And then you you will be.

**\
Nathan Carver** 2:31:13\
Uh, so it\'s gonna be two calls. So create the customer and then call
this to create the fun source.

**\
Pavel Frolov** 2:31:20\
Yes.

**\
Juan Martinez** 2:31:22\
Right, but this is after the fact. You know, in order for a customer ID
to exist, someone created the customer in Diwala. Did the customer do it
pseudo themselves or are we doing it via this website?

**\
Nathan Carver** 2:31:34\
So we can do it. So they do all the provides us the ability to do that.
Essentially they they provide their own components so that we wouldn\'t
have to build this, but they also provide an API that allows us to
capture all that same information.\
And send it to Duwalla and we create that account on the customer\'s
behalf.

**\
Juan Martinez** 2:32:03\
Yeah, but I mean, I would you agree, Nathan, unless there\'s an
additional charge, the Diwala interface is very clean, simple. They\'ve
ironed out all their bugs. Why would we reinvent the wheel?

**\
Nathan Carver** 2:32:19\
Uh.\
So I agree that yes, there\'s an advantage to using their site. As far
as engineering goes, it was gonna be, I think it\'s more of a decision
of customer experience. There\'s information that.\
Pavel wants to collect for the engineering side, so our our database we
need specific information. So as long as it\'s not a case of the
customer entering information in JBL and then entering that same
information in to Diwala.\
I think that comes down to customer experience. Um.

**\
Juan Martinez** 2:32:51\
Right.\
Yeah. And again, that that\'s all answered by what Diwala will give us
in terms of an export of the entire customer data file.

**\
Pavel Frolov** 2:33:06\
Oh, I I definitely sure that it will be enabled through the API list of
customer sources list the customer.\
Uh, I think everything will be available to get from.

**\
Juan Martinez** 2:33:22\
OK.

**\
Pavel Frolov** 2:33:23\
But again, why? Why should we request the data if you already have this
in our database?

**\
Juan Martinez** 2:33:32\
Well, that that that\'s the question is you know we don\'t, we don\'t
want the customer to enter it twice. So either they enter it with us or
they enter it with Duala.

**\
Nathan Carver** 2:33:48\
But they may still have to go to our site, enter in information and then
we would kick them over to Diwala for just.\
That specific Dwala information.\
Or I think if actually maybe not, it\'s not even. So if we actually
embed Duala components into our site, it could be one.\
You know, seamless experience or at least semi seamless to the customer.

**\
Dzmitry Chudzinau** 2:34:22\
All the insurance in the world.

**\
Pavel Frolov** 2:34:28\
OK. Anything else can we discuss today or?

**\
Val Levitan** 2:34:33\
I think we have been at it for 2 1/2 hours. I think it\'s enough.\
Do we have any plans for tomorrow?

**\
Pavel Frolov** 2:34:48\
We are going to the.

**\
Val Levitan** 2:34:59\
Yeah, yeah, yeah, yeah, yeah, yes, yes, yes.\
Long weekend. OK, enjoy your long weekend. Thank you very much. And
should we then set something up for Monday?\
So Monday at 7:00.

**\
Nathan Carver** 2:35:23\
Sounds good.

**\
Irina Shishko** 2:35:25\
Yep.

**\
Val Levitan** 2:35:25\
Pavel, you\'ll send the E right, right?

**\
Pavel Frolov** 2:35:28\
Yes.

**\
Val Levitan** 2:35:29\
OK. Thank you very much. Have a good weekend. Bye, bye. Bye, bye.
Thanks.

**\
Sergey Tsimanov** 2:35:31\
How many?

**\
Pavel Frolov** 2:35:33\
Right. Thank you, Bonnie.

**\
Juan Martinez** 2:35:33\
Bye.

**\
Dzmitry Chudzinau** stopped transcription
