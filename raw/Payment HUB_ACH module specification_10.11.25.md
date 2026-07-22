**Payment HUBACH module specification-20251110_070443-Meeting
Recording**

November 10, 2025, 12:04PM

1h 35m 48s

**\
Pavel Frolov** 0:04\
We\'ll share this requirement for all of us to to review.\
One second.

**\
Val Levitan** 0:48\
I would like to organize this meeting maybe slightly differently, if I
may, while there is a pause.

**\
**0:53\
Um.

**\
Val Levitan** 0:57\
So based on the meeting recordings.\
I took the last two recordings.\
And ask the AI to summarize it in the shortest possible form. Some
simple possible form.\
And these are the these are the undertakings from the last two
meetings.\
And giving it a very brief read. I didn\'t go into depth.\
But they seem to be.\
You know, probably the correct undertakings and maybe if we reviewed
those undertakings, maybe the meeting would take a better shape.\
Because those are essentially good undertakings. For example, we have to
create a state machine diagram for requirement 106. Is it done?

**\
Pavel Frolov** 2:04\
No.

**\
Val Levitan** 2:06\
But this was an undertaking. So if we undertake to do something, we
should do it. Otherwise, why are, why are we, you know?

**\
Pavel Frolov** 2:12\
Definitely.

**\
Val Levitan** 2:17\
Create business flow diagram for customer onboarding on Duala. Did we do
it?

**\
Pavel Frolov** 2:24\
No, no.

**\
Val Levitan** 2:29\
Post terminal registration requirement to GitHub.

**\
Pavel Frolov** 2:33\
Uh.

**\
Val Levitan** 2:33\
Clarified passport registration versus terminal registration procedure.
I think we did that partly, yeah.\
We need to start design web interface for location and customer
registration.

**\
Pavel Frolov** 2:50\
Yes, started initiated, created tasks for UI.

**\
Val Levitan** 2:58\
So who\'s who was it assigned to?

**\
Pavel Frolov** 2:59\
Uh, don\'t. Yeah.\
Assigned to.

**\
Val Levitan** 3:06\
OK. Is there a schedule when we will be able to review it?

**\
Pavel Frolov** 3:11\
At least for upcoming two weeks. I think he will create some drawings,
mockups and we can take a look on this.

**\
Val Levitan** 3:24\
OK. So looking at the calendar, we can review it on the 24th of
November.

**\
Pavel Frolov** 3:30\
Yeah.

**\
Val Levitan** 3:32\
The recording is running, so we\'re going to have an undertaking to
review the web design on the 24th of November.

**\
Pavel Frolov** 3:37\
Um.

**\
Val Levitan** 3:46\
2nd.\
Irina Irina was supposed to define requirements for testing hooks or
tools how to verify invoice state changes in the system.

**\
Pavel Frolov** 4:25\
I I.

**\
Val Levitan** 4:35\
So let\'s take. So let\'s take. So let\'s take this list and let\'s
discuss it now.\
If there are questions, OK.\
Nathan was supposed to facilitate Duala portal access for team members.
That probably is not even possible right now.\
Because Dwala has not finished their internal review of our comments on
the agreement, so they\'re probably not moving ahead with with it here.
Nathan was supposed to clarify.\
Dual account structure that probably also not possible right now.\
I met with Dwala representative. Again, same problem. Dwala is stuck on
reviewing the agreement.\
Have you signed in? Has everyone signed in to their sandbox portal?
Duala sandbox portal? I know that Dima was was trying to sign in. I
think he signed in, but I\'m not sure that Sergey or Alexei signed in.

**\
Alexey Khamin** 5:51\
Not yet.

**\
Val Levitan** 5:55\
You\'re waiting, so you register.

**\
Pavel Frolov** 5:55\
Sergei registered.

**\
Sergey Tsimanov** 5:59\
No, yes.

**\
Irina Shishko** 6:01\
Mhm.

**\
Val Levitan** 6:02\
OK. Alexei, can you please? OK, Alexei, can you please register? And
Irina, have you registered?

**\
Pavel Frolov** 6:03\
New also register.

**\
Irina Shishko** 6:09\
No.

**\
Val Levitan** 6:10\
Can you please register?

**\
Irina Shishko** 6:12\
Yes.

**\
Pavel Frolov** 6:22\
Um.

**\
Val Levitan** 6:23\
We decided to park certain customer account architecture questions until
Wallace fully registered with us, but that probably should remain as an
undertaking.\
The last task or the last undertaking?\
The internal team was going to focus on CMS web interface design for
location verification credential management. I think part of you told me
that this has already been structured and assigned. Can I please?

**\
Pavel Frolov** 7:00\
Sent. Yeah.

**\
Val Levitan** 7:02\
Can I please see the? Can you please share your screen? I want to see
where is it assigned.

**\
Pavel Frolov** 7:09\
One second.

**\
Val Levitan** 7:10\
I\'d like to see the Jira plans.\
Alexei, in the meantime, please prepare your questions. We\'re going to
review them now.

**\
Pavel Frolov** 7:15\
Oh.\
Um.

**\
Alexey Khamin** 7:21\
OK.

**\
Val Levitan** 7:28\
In the future, ladies and gentlemen, I suggest that as we record our
meetings after the recording, I suggest for you.\
To take the transcript, the raw transcript.\
And using this particular prompt, you could obviously modify the prompt
as you wish. This is the prompt that works for me. I use this prompt. I
put the transcript into an AI AI of your choice I happen to like.

**\
Pavel Frolov** 7:59\
Hello.

**\
Val Levitan** 8:05\
Um, uh, Claude.\
Uh, instead of Uh Chang GBT, but it\'s my personal preference.\
And you could just say here\'s the transcript. Please summarize the
undertakings in the shortest possible style.\
Again, obviously it\'s an A I. Obviously it makes a mistake. Obviously
sometimes it could, you know, hallucinate certain things. But we\'re
humans and we can decipher through right and wrong.\
Information. So let\'s.\
Build on what we have after every meeting. As you prepare yourself for
the next meeting, please use the recording so next meeting becomes
efficient and next meeting should build on the undertakings that we
assumed.

**\
Pavel Frolov** 8:54\
Mm.

**\
Val Levitan** 9:02\
As we record the meetings, I strongly suggest to use the verbiage as
undertakings or as a commitment or as objective.\
So the AI could pick up on these problems.\
OK, Pavel, you\'re not sharing your screen yet, yeah?

**\
Pavel Frolov** 9:25\
Yeah, yeah, one second.\
It\'s quite.

**\
Val Levitan** 9:34\
So first we\'re gonna review our.\
Plan for CMS web interface design.\
And after we had reviewed that.\
Alexi will have his questions on.

**\
Pavel Frolov** 9:51\
Probably I I suggest before to switch to Alexey to focus on Mitri\'s
question related to to to different options related to ACH and.

**\
Val Levitan** 10:01\
Of course.

**\
Pavel Frolov** 10:05\
And.\
How to assign bank accounts for particular client? It was a question.

**\
Val Levitan** 10:12\
Of course we can do that.

**\
Pavel Frolov** 10:24\
OK.\
Timo will Timo will share what he is investigation related to ACH and
how to assign bank accounts and probably will lead to some other.

**\
Val Levitan** 10:41\
So, sorry, so sorry. I just want to make sure that everybody\'s aligned
what\'s happening here. Pavel, would you rather have us review the
schedule first or Dima\'s question first because we see your schedule?

**\
Pavel Frolov** 10:42\
Decision on architecture.\
It\'s.\
First.\
Schedule first.

**\
Val Levitan** 11:02\
Schedule first. OK, so let\'s do schedule first.

**\
Pavel Frolov** 11:03\
Yes.

**\
Nathan Carver** 11:05\
.

**\
Val Levitan** 11:06\
What? What value stream are you in right now?

**\
Pavel Frolov** 11:11\
One second. Right now it\'s payment hub.

**\
Val Levitan** 11:16\
So application value stream is IP90.\
And under IP 90 payment hub.

**\
Pavel Frolov** 11:29\
IP632 and here BEP 2677 clients location dashboard graphic user
interface prototype.

**\
Val Levitan** 11:42\
Sorry, excuse me under IP632, where are you?

**\
Pavel Frolov** 11:49\
IE632.

**\
Val Levitan** 11:51\
Uh, payment have you and after that?

**\
Pavel Frolov** 11:53\
And then BEP 2677 client location dashboard, traffic user interface
prototype.

**\
Val Levitan** 12:03\
OK, I I don\'t see a schedule here.

**\
Pavel Frolov** 12:04\
And it.\
Yeah, no specify it here.\
Be here until November 21st.

**\
Val Levitan** 13:19\
Can you please say the changes? Thank you.

**\
Pavel Frolov** 13:33\
OK, now I think we can switch to.

**\
Val Levitan** 13:37\
Sorry, I see two stories under under it. Is it that that\'s all that\'s
required, two stories?

**\
Pavel Frolov** 13:42\
Yes.\
For pro for first approach to prototype, yes. In future definitely it
can be switched to a different feature to implement this layout
according to this prototype.

**\
Val Levitan** 14:03\
OK, understood. Anybody has questions on the schedule?

**\
Pavel Frolov** 14:03\
And it\'s.

**\
Val Levitan** 14:08\
OK. Thank you very much. So let\'s please stop sharing the screen and
can we now focus on Dima\'s question for English speaking people only?

**\
Irina Shishko** 14:08\
Hello.

**\
Val Levitan** 14:21\
Either myself or Pavel will try to translate it. So Dima, please speak
in small chunks because we cannot translate everything.

**\
Dzmitry Chudzinau** 14:32\
Option TMR O processor Kakanum presides southernly national system
location cool.

**\
Pavel Frolov** 15:00\
So the open question from Dima, probably not only from Dima, but from
our team who.\
To dwell fairly likely how to assign bank accounts of particular client
to our internal entity in database I assume.\
That\'s.

**\
Val Levitan** 15:30\
Let me let me rephrase the question. Maybe let me try to rephrase the
question and maybe I\'m not going to say it correctly, but I just want
to rephrase it RCMS.\
Natively has a definition of allocation.\
And I think Dima is saying we have a definition of location in our
database structure and we can say that and we can open this location, we
can enter the owner\'s name, telephone number, address, et cetera, et
cetera.\
Right.\
The the the most important tie in between a location in our database and
let\'s say duala or in the future it will be not in the future but.\
It will be dweller and it will be income.\
On the wallet side, it will be account number and I anticipate that
eventually Tim will ask a question, but we also have a POS with a
certain serial number that will go into that location. So should we
assign?\
That serial number of the POS.\
And tie it to that location. So there will be basically dim. I guess
Dima is asking.

**\
Nathan Carver** 16:55\
2.

**\
Val Levitan** 17:01\
I\'m slightly reading his mind maybe, or in a way reading his, he\'s
saying our database.\
Already hosted definition of address, name, location, owner, etcetera.
Should we and how then?\
Hook in an account number and the UA serial number to that location.

**\
Pavel Frolov** 17:29\
No, no, not exactly. First of all, just to clarify, we are going to
introduce new database with new control server that will be hosted in
the cloud, but in general.\
We will replicate some entities like location, I assume probably in the
same order as current CMS implemented, but the question mostly related
not to assignment between location terminal.\
ACH provider and income, but mostly how can we assign particularly bank
account of the customer to our location?\
Dimo will describe more detailed.

**\
Dzmitry Chudzinau** 18:25\
The.\
OK.\
Sure is the chat to across and I showed was possible.\
Clients, Catroma robotum, account late Bank of system.\
It will emit integras of settly played system.\
E-mail address.\
The music interface. Uh.\
Bullet account secured credential account.\
Now I\'m basically here with books.

**\
Nathan Carver** 20:11\
OK.

**\
Pavel Frolov** 20:11\
So the according to to Dimas investigations, there are two possible ways
how a bank account can be assigned to our internal location entity. It
it\'s implemented based on plate.\
Serious plate infrastructure that the wall also implemented on their
side in this approach actually on our web page when the.\
Client want to enter his bank account at at this moment we will switch
to different page and we will not know actual bank account numbers.\
All security will be outside of our site on the site of plate service
and we will get only some.\
Identification that we will be able to use in future to access this bank
account. It it related to option #1.\
Uh.

**\
Nathan Carver** 21:43\
That\'s what I\'ve that\'s what I\'ve seen as well in the API is you you
create a customer verified or unverified.\
Mm.\
An unverified customer and then you can create an account and store the
ID.

**\
Pavel Frolov** 21:54\
Uh, it surely it.\
Actually option #2 is also using the wall API, but we will be able to
directly ask for customer to enter.

**\
Nathan Carver** 22:07\
Correct.

**\
Pavel Frolov** 22:16\
His bank account. So this is option #2 as I understand. Jim, correct me
if I\'m wrong.

**\
Dzmitry Chudzinau** 22:21\
Yes, you\'re right. Mash is not.

**\
Val Levitan** 22:23\
And what\'s the sorry, sorry, option number one, who enters the account?

**\
Pavel Frolov** 22:28\
Say enter a bank account, but in the option number one it will be a
third party page, not Wallace page as I understand, but directly
played.\
Uh, page.\
In option #2 we are just using API from Dwala and also customer will
enter all the fields including number but this.

**\
Val Levitan** 22:58\
But but it will be right.

**\
Pavel Frolov** 23:01\
But this numbers will.

**\
Val Levitan** 23:01\
But this is a JJDL page.

**\
Pavel Frolov** 23:04\
Yes, and all the data including bank account can be stored in database
not secure for customer. Of course we can implement this in a different
way, never.

**\
Val Levitan** 23:18\
OK.

**\
Pavel Frolov** 23:20\
A stores this bank account in our database but.

**\
Val Levitan** 23:20\
Hey, hi.\
I I I prefer not to touch that.\
I I don\'t wanna have any secrets.\
I don\'t wanna keep any secrets.

**\
Pavel Frolov** 23:33\
So this is a preferred way to use blade service.

**\
Val Levitan** 23:38\
Juan Juan, do you have an opinion on this?

**\
Juan Martinez** 23:42\
Yeah, no, 100%. We for to retain and store U.S. banking information
makes us have to follow protocols that we don\'t want to follow.

**\
Val Levitan** 23:54\
Especially, especially, especially in Belarus, who is the enemy of the
world.

**\
Nathan Carver** 23:55\
So.\
Using this option two, we don\'t have to store their bank and routing
number, we just use it to make the API call and then we store the GUID
the the unique ID that Duala returns to us.

**\
Pavel Frolov** 24:05\
Yeah.\
Yeah, yeah, we understand it. But in in any case, I think the first
approach will be preferred if all the customer support working with
plate.

**\
Val Levitan** 24:28\
I I prefer to have played.\
Interface.

**\
Pavel Frolov** 24:33\
It.

**\
Val Levitan** 24:35\
I I guess we\'re gonna have to then put a disclaimer that you\'re
leaving JVL domain, you\'re now on plate, your secure information will
not be stored at JVL, and this is the relationship between you and plate
who verifies your account.

**\
Pavel Frolov** 24:55\
Yes.

**\
Val Levitan** 24:55\
Some sort of a some sort of a verbiage that suggests that they\'re
leaving JVL site. They\'re going on the plate. Yeah, Juan Nathan,
you\'re good with that.

**\
Pavel Frolov** 24:56\
Yeah, yeah.

**\
Juan Martinez** 25:08\
Yeah, I agree.

**\
Nathan Carver** 25:09\
Yes.

**\
Pavel Frolov** 25:10\
Yes, it\'s the same behaviour as as as currently implemented payment
solutions when you need to enter your when you enter your card, when you
it\'s redirects you to some page related to particularly this bank and.\
Then you answer some other data more securely. OK, screw you.

**\
Val Levitan** 25:37\
I agree. I agree. Let\'s let\'s. So the decision to follow the first
scenario where we hand over the confidential information to a third
party, we put proper disclaimers.\
Yeah.\
And we do not keep any information with us.

**\
Irina Shishko** 26:02\
Listen.

**\
Val Levitan** 26:02\
By the way, I suggest that you convey this message to the interface
designers.

**\
Pavel Frolov** 26:10\
Mhm.

**\
Juan Martinez** 26:12\
I think Irina has a question.

**\
Irina Shishko** 26:14\
Uh.

**\
Val Levitan** 26:15\
No, Irina. Irina. Irina is scratching her hand. And by the way, when she
scratches the right hand, according to the Russian superstition, that
means she\'s going to meet a friend.

**\
Juan Martinez** 26:25\
Uh oh.

**\
Irina Shishko** 26:28\
But.

**\
Val Levitan** 26:29\
And if you scratch your left hand, that means you\'re going to be
counting money.

**\
Irina Shishko** 26:35\
Duck.

**\
Val Levitan** 27:05\
Yes, yes, Tracy, Estrada, Catora, Spitzanas and you might say, but it
does say at the Informatsi at our companion is the wise blood or played.
I need a quick of partnerships.

**\
Irina Shishko** 27:11\
Mhm.\
Mhm.\
Mhm.

**\
Val Levitan** 27:25\
A quick disclaimer. So we we particed it to JVL side. We shall do it in
the third party validation side. JVL will not keep any of your
information.

**\
Pavel Frolov** 27:37\
OK.

**\
Val Levitan** 27:41\
And uh.\
This will be handled by a third party.

**\
Irina Shishko** 28:00\
Yeah.\
Just.

**\
Pavel Frolov** 28:04\
The.

**\
Val Levitan** 28:07\
Yes.

**\
Irina Shishko** 28:07\
I can\'t.

**\
Val Levitan** 28:10\
I just want to dwell a little, not Walla, but dwell a little bit on the
subject of registration. So my plan is to hand over all.\
Laborious operations to.\
Location.

**\
Irina Shishko** 28:32\
Uh, so yeah, we\'re on all the.

**\
Val Levitan** 28:34\
Oh.\
I would like to I read for your benefit. I\'m going to repeat it again.
The objective of JVL is to design the interface registration interface
in such a way that all of the.

**\
Irina Shishko** 28:42\
Mhm.

**\
Val Levitan** 28:53\
Laborious procedure of entering data is handed over to individual
locations, so they themselves for themselves.\
Enter all the data so we don\'t have to do it.\
This is a very strong point. That means that our interface has to be
intuitive. It has to have tutorials, it has to have Q&A in multiple
languages.\
But to begin with, it should have Spanish and English equally.\
Because America is Duolingo.\
OK.

**\
Nathan Carver** 29:51\
Yes.

**\
Val Levitan** 29:54\
OK, Dima, go ahead next, unless we answered all your questions.

**\
Dzmitry Chudzinau** 30:03\
Table of processes.

**\
Val Levitan** 30:19\
Correct. Either you\'re registered or we cannot work with you.\
Nathan, the question is, Juan, Nathan, the question is.\
If if a location is not registered with us, we can\'t work with it.

**\
Pavel Frolov** 30:39\
Display it.

**\
Val Levitan** 30:41\
Wait, well, it doesn\'t matter. We cannot do anything for the location.
There\'s nothing that we can do for the location.

**\
Dzmitry Chudzinau** 30:48\
No, it\'s just the yeah, you have to split what were my account
previously to.

**\
Juan Martinez** 30:49\
Which will.

**\
Val Levitan** 30:49\
Like.\
Yes, of course everything is possible. I mean, I\'m I\'m actually
thinking that we should have online help, not only AI help, not only
robotic help, but we should have a human help. I actually have a person
in mind to allocate to that.\
But the, you know, that help is within reasonable time. I mean, that\'s
not immediate. We\'re not going to have an operator immediately.\
Yeah, but the bottom line is if if you\'re not registered, we can\'t
work with you. Is it possible that a location picks up the phone and
says, hey Felipe, you know what? I have 10 accounts.\
Come over here, give me a hand, you know, drive to my location, help me.
Sit next to me, next to my computer and help me register. And Felipe
will say, of course, Mr. Smith, I\'m on my way. I will be there
tomorrow. I will help you out.\
Yeah, sure, it\'s possible. Of course. Why not?\
Maybe even our online help works so nicely that we will be able to help
on a video call. Maybe, I don\'t know.

**\
Dzmitry Chudzinau** 32:09\
Mm.

**\
Val Levitan** 32:14\
But we should assume that if a location is not registered, we cannot
work with you.

**\
Pavel Frolov** 32:26\
Yep.

**\
Val Levitan** 32:27\
OK, Dima, I understand we you have no more questions for now, right?

**\
Juan Martinez** 32:32\
Yeah.

**\
Val Levitan** 32:33\
OK. OK. Thank you very much for your questions. I think we can move on
to answering Alexi\'s questions. Am I correct?

**\
Dzmitry Chudzinau** 32:34\
Right.

**\
Val Levitan** 32:45\
Alexey, so you speak, you speak wonderful English. I heard you speak in
English.

**\
Pavel Frolov** 32:46\
It\'s.

**\
Alexey Khamin** 32:51\
Yeah, yeah, yeah.\
The document you know.

**\
Val Levitan** 32:58\
You you\'re you\'re you\'re very good in English. Speak English is good
for you.

**\
Nathan Carver** 33:06\
Yeah.

**\
Val Levitan** 33:09\
I will help you out or Pasha will help you out. Speak in English.

**\
Pavel Frolov** 33:14\
Oh, you can just read this from from your document. You already have
written in English.

**\
Alexey Khamin** 33:21\
Yeah, but can you share it and do the work after answering?

**\
Nathan Carver** 33:22\
Or or or.

**\
Alexey Khamin** 33:31\
OK.

**\
Val Levitan** 33:38\
Don\'t be shy. Don\'t be shy. We all of us understand that this is your
second language and we\'re grateful for you to speak English.

**\
Alexey Khamin** 33:43\
Yeah. OK. Thanks.\
Is it?

**\
Val Levitan** 33:49\
Yes.

**\
Alexey Khamin** 33:52\
OK.\
So there\'s a list that, uh, I can hear that after.\
My things about how testing.\
Will be proceed and.\
But first of all, it\'s related to previous demos question and maybe
CMAS part. How are we going to create bank accounts and?\
Locations.\
For testing it means so not not real accounts but testing we we will
need to generate it.\
Maybe a lot of it.

**\
Val Levitan** 34:42\
I I swiped myself while I has interface that allows you to generate test
accounts.

**\
Alexey Khamin** 34:42\
So.\
Yeah, uh, it has the APIs and we can do it by request to it, but uh.\
How are we going to do it using our interface or just by request and
then where we can?\
Review the result and check, check, balance, something else.\
We can do it by requests using API, but will we have possibilities to do
it using SUI?

**\
Val Levitan** 35:32\
I don\'t know the answer to that question, Nathan.\
Um.

**\
Nathan Carver** 35:40\
Could you repeat the question? How do we transfer?\
Um.\
From the customer to our bank account.

**\
Val Levitan** 35:46\
Uh.\
No, Alexi says that.\
In order. So Alexi is in QA department. He\'s a QA engineer, so his
primary concern is how to test.

**\
Nathan Carver** 35:58\
OK.\
OK, got it.

**\
Val Levitan** 36:04\
So he says one one of the element of testing is to be able to generate
an API and to test the creation of an account. Alexey, do I understand
your question correctly?

**\
Nathan Carver** 36:17\
Correct.

**\
Alexey Khamin** 36:20\
Yeah, yeah.

**\
Val Levitan** 36:23\
And he says, what is the would Waller allow us to set up fake accounts?\
And what is the procedure for that and or should we build hooks in the
API simulating the account account set up? What from a QA perspective,
what is the procedure?

**\
Nathan Carver** 36:48\
I my assumption was the Wallace Sandbox provides us a testing
mechanism.\
So could we integrate that with our production deployment would be I
guess the question. If so, then that would provide QA with the ability
to run tests on a on a sandbox account and they can go into the Wallace
portal and verify.\
Results.

**\
Val Levitan** 37:20\
Yeah.\
Pavel, do you have an opinion on this?

**\
Pavel Frolov** 37:22\
Yeah, I I see a a difficulties here because we can create account on
Duala, but definitely we need to perform this manually, but if you
want.\
To have some action, for example on GitHub that automatically creates
some workflow, including creating account and transmitting some monies
from tool. Probably it will be a little bit.\
Difficult. Uh, then.\
As a fully automated process, but definitely we will be able to create
several account and use them in different workflows.

**\
Alexey Khamin** 38:15\
You mean when are they great?

**\
Val Levitan** 38:16\
So I think, I think one second, one second please. I think you want to
create these accounts. I think the question is.

**\
Pavel Frolov** 38:18\
Yes, my name.

**\
Val Levitan** 38:27\
And your question is probably to Dwala.\
How to implement a hook for recurring testing of of this step?

**\
Pavel Frolov** 38:40\
Probably some some accounts for testing will be enough for us. For
example, we will create account number one, #2, #3, #4 and before each
test we can full.\
Fuels this account with some amount of money if it available at the
sandbox, highly likely, yes. And then we are sure that each account has
enough money and we can use this money according to our test cases.\
Just even using the same names of accounts each time.

**\
Val Levitan** 39:14\
OK.\
So why? So why don\'t Pavel puts it on his agenda as an undertaking to
consult the Wallace specifically on this?\
Yeah, period.\
Let\'s do that.\
OK, Alexey, good question. Next question please.

**\
Pavel Frolov** 39:52\
Um.

**\
Alexey Khamin** 39:53\
And some addition do we need to do some hooks from our site?\
To be sure that it\'s it\'s from our site, from humans, maybe from.

**\
Pavel Frolov** 40:02\
The hooks for for for whom?

**\
Alexey Khamin** 40:10\
Um.\
ACH to be sure that it will be testing data and we will not.\
I can\'t and to don\'t spam from our looks.\
When come to or something else.

**\
Val Levitan** 40:39\
I I do not understand the question.

**\
Alexey Khamin** 40:41\
For example, on the machines we have production build and debug builds
and debug builds will.\
The log builds uh do not set send all information about machine, all
logs and so.

**\
Val Levitan** 40:56\
I I don\'t. I I don\'t see how we have debug builds, I think.\
Our commits are going into GitHub, and in GitHub we always pull to the
name to the master branch. So each master branch serves as a production
branch, isn\'t it?

**\
Pavel Frolov** 41:19\
It relates to production environment and staging environment. It\'s
it\'s mostly about this, so for staging environment.\
Probably the question is for staging environment, do we need to
implement some additional to have more more hooks at at this regime?

**\
Val Levitan** 41:51\
Um.

**\
Pavel Frolov** 41:55\
Comparing this production environment.

**\
Val Levitan** 42:00\
My understanding that GitHub has only one environment.

**\
Pavel Frolov** 42:04\
No, no, no. You can specify as much environment as you want during the
action when you run action.

**\
Val Levitan** 42:13\
So you assemble it differently for staging and for roduction.

**\
Pavel Frolov** 42:19\
Yeah, actually it\'s enabled to have actions to create different
environments.\
Any name you want and each environment we will do different actions,
different steps. For example for staging it will be more data, more
debug, more logging and so on.

**\
Irina Shishko** 42:36\
OK.

**\
Val Levitan** 42:48\
So the the question is.\
What?\
I guess what calls to uh.\
Pull into the assembly of the staging environment through actions in
GitHub to facilitate.\
Emulation of.\
Testing an account.\
That\'s that\'s the question. So we don\'t know the answer to that and
we should consult Duolo on it, which should be Pavel\'s undertaking to
speak to Duolo.

**\
Pavel Frolov** 43:38\
For me, it\'s question mostly to QA and probably to Dima. What you as a
QA engineers want us, want Dima to implement for your convenience? What
the hooks do we need?

**\
Val Levitan** 43:53\
I see.

**\
Pavel Frolov** 43:59\
What hooks will help you to to test all the workflow?

**\
Val Levitan** 44:05\
Well, the hooks that they want is to test different states.

**\
Pavel Frolov** 44:10\
Yes, yes, probably. The question is, for example, we have some stage,
but we don\'t want to to go all the steps. We want to set it
artificially to some different state and to see how the system behaves.\
This state.

**\
Val Levitan** 44:32\
OK, but that is dependent on a if if let\'s say a QA engineers have a
state machine diagram.\
They would be able to point to a particular state and to say I want to
emulate this state.

**\
Pavel Frolov** 44:52\
Yes, yes.

**\
Val Levitan** 44:55\
So one of the previous undertakings was to create a state machine
diagram for requirement 106. Should we expand the state diagram for
other requirements?

**\
Pavel Frolov** 45:12\
Oh.\
I think state machine relates not directly to particular requirements.
In some cases it can be a general state machine, but in some cases it\'s
more locally related.\
To some features, yes, in all places where where we can write a state
machine, we need to use it and to provide the state machine for QA for
their convenience to to decide.\
Does a need to check particular state and state changes?

**\
Val Levitan** 45:57\
So my question is to Irina and Alexei.\
Had we provided you with a machine state diagram or state machine
diagram? I don\'t know how to say it correctly.\
Would you be able? Would that be beneficial for you? It\'s a boom of
Wamdali state machine diagram.\
Globally warm.

**\
Alexey Khamin** 46:37\
The planning routes.

**\
Val Levitan** 46:46\
OK.\
OK, fantastic. So we need to focus our efforts on providing state
machine diagram. So Pavel, explain to me who and how.\
This state diagram is generated.\
Is it a function of a developer? A particular developer? Is it Sergey
that needs to do state diagram? I don\'t know.

**\
Pavel Frolov** 47:22\
As an initial point, it was some state diagram from Nathan I assume.\
But definitely during development this diagram can be changed.\
Due to different reasons.

**\
Val Levitan** 47:39\
Yes, Nathan. Nathan, I remember you provided the state diagram.

**\
Nathan Carver** 47:46\
So we had some documentation, yes, that described the concepts that in
the requirements and then the engineers can create the diagram as they
understand the design of the system.

**\
Pavel Frolov** 47:54\
Mhm.

**\
Nathan Carver** 48:02\
The the information I had was very focused on the state of an invoice or
an an ACH transaction. That\'s it as they move from created to in
process to pending or completed.\
Or failed those types of states.

**\
Val Levitan** 48:21\
OK, can you place your focus diagram?

**\
Nathan Carver** 48:26\
Let me see what we have. Yeah, let me see what we have here.

**\
Val Levitan** 48:27\
Here.\
OK, so obviously other states will be somehow complementing your diagram
or addressing other conditions. So who creates this diagram?\
I just need a name of the individual.

**\
Nathan Carver** 48:53\
Uh.

**\
Val Levitan** 48:55\
I have a feeling that it\'s her gate tomorrow.

**\
Pavel Frolov** 48:59\
Um, I like it. Uh, if you\'re saying about um.\
Terminal registration, for example, procedure, yes, it can be a search
as an input point of our systems.

**\
Val Levitan** 49:17\
OK. So Sergey, Tomanov, question is to you.\
Are you able to produce state machine diagram for? How did you describe
it, Pavel?

**\
Pavel Frolov** 49:31\
Terminal registration procedure.

**\
Val Levitan** 49:35\
Thank you.

**\
Dzmitry Chudzinau** 49:39\
There was.

**\
Pavel Frolov** 49:40\
You need to.\
Import terminal registration.

**\
Dzmitry Chudzinau** 49:58\
No question.

**\
Sergey Tsimanov** 49:58\
No question.

**\
Pavel Frolov** 49:59\
And you do this.

**\
Val Levitan** 50:02\
How much time do you need for that?

**\
Dzmitry Chudzinau** 50:08\
No, it was.

**\
Sergey Tsimanov** 50:08\
No, it was.

**\
Val Levitan** 50:08\
Don\'t, don\'t, don\'t push yourself. Don\'t, don\'t, don\'t give
unrealistic schedule, comfortable schedule. When can we have a diagram?

**\
Dzmitry Chudzinau** 50:11\
Zoom.

**\
Pavel Frolov** 50:32\
Yeah, the E-authentication series.\
Terminal registration will.

**\
Sergey Tsimanov** 50:41\
Mhm.

**\
Pavel Frolov** 50:54\
Mm.\
The next next Wednesday, Wednesday.

**\
Juan Martinez** 51:04\
Can I just get a clarification of the terminal registration terminal
equals Flex DOS, correct?

**\
Pavel Frolov** 51:13\
Yes.

**\
Juan Martinez** 51:14\
So this registration has nothing to do with Diwala, it only is internal
and with income, correct?

**\
Sergey Tsimanov** 51:23\
Yeah.

**\
Juan Martinez** 51:24\
We never register a device with.

**\
Sergey Tsimanov** 51:25\
No.

**\
Pavel Frolov** 51:28\
Yes.

**\
Juan Martinez** 51:29\
OK. Thanks.

**\
Val Levitan** 51:34\
OK, so terminal registration state diagram will be ready.\
On Wednesday the 19th.\
Of November, and the undertaking is assigned to Sergey Samanov.

**\
Sergey Tsimanov** 51:53\
No.

**\
Val Levitan** 51:54\
OK.\
Moving on.

**\
Alexey Khamin** 52:00\
OK, OK. The next question is about ignition data for testing. So for
example we will need to.

**\
Val Levitan** 52:00\
Alexi, go ahead.

**\
Pavel Frolov** 52:10\
.

**\
Alexey Khamin** 52:13\
Proceed with maybe 100 invoices in a day in 9:00 AM. So we need to
prepare data for it. We need to get some amounts for these invoices and
so on.

**\
Pavel Frolov** 52:26\
This.

**\
Alexey Khamin** 52:31\
So how can we get?\
So many locations and.\
Bank accounts and so on.

**\
Pavel Frolov** 52:42\
So.\
Oh, I think this is a question to dwell on.\
Uh, how to the late big?

**\
Alexey Khamin** 52:51\
Not, not, not, not, not, not only because we need to have our locations
also from POS.

**\
Irina Shishko** 53:00\
Mhm.\
My showers, not just not done.

**\
Dzmitry Chudzinau** 53:06\
Test of environment, dwellers in books, place in books is at Eastern
income.

**\
Irina Shishko** 53:11\
Oh.

**\
Dzmitry Chudzinau** 53:20\
In just my.\
And I\'ll support at least.\
I see a motion robot is forget to prezio. My motion proster is robot
CPI.\
Like here.

**\
Alexey Khamin** 54:09\
Start.

**\
Juan Martinez** 54:29\
Can I ask a question for for this to generate test data? How, how or why
is this different than what Felipe has been assisting us with where we
we set up a terminal, a POS with income?\
And we just need to add more testing on Felipe\'s part. Is that what
we\'re saying?

**\
Val Levitan** 54:45\
But.

**\
Pavel Frolov** 54:54\
Alexei assumes that this this particular task will will be done by by
him, but not remotely by.

**\
Juan Martinez** 55:04\
OK.

**\
Pavel Frolov** 55:09\
Filipa, Filipa, I think this is a final, final, final test and highly
likely this production environment.

**\
Irina Shishko** 55:20\
Oh.

**\
Juan Martinez** 55:23\
OK, so I I don\'t think there would be a problem between us and income
to set up however many POSS or flex pays you want to use to to create
the scenario like we\'ve done in the Georgia office today.

**\
Pavel Frolov** 55:43\
So highly likely we will need thousands of cards.\
Cards card numbers from income to be able to generate activation, fake
activations and then to clean all this activation and make deactivation
for for them.\
If we actually want to to check how the system behaves in case of many
cards generated at a day.

**\
Nathan Carver** 56:10\
Sure.

**\
Val Levitan** 56:32\
Can somebody summarize the essence of the problem?

**\
Juan Martinez** 56:41\
I chip.

**\
Dzmitry Chudzinau** 56:48\
After Miti Zero, it\'s Gineratzu Lienta test. There\'s another prior
priority.

**\
Val Levitan** 57:08\
OK.\
The cards have put it\'s a Karteskata income.

**\
Irina Shishko** 57:17\
Oh.

**\
Pavel Frolov** 57:52\
Mm.\
So Dima and Alexey said that actually we need to request more cards,
test cards that can be dumped entered to our staging.\
Database to be able to reuse them in a test environment.

**\
Val Levitan** 58:33\
I will. I I will undertake.\
The responsibility for ordering more test cards from income and shipping
them to Minsk.\
How many cards should I order 1020?

**\
Pavel Frolov** 58:51\
Yeah.\
You\'re just.

**\
Nathan Carver** 59:06\
Well.

**\
Pavel Frolov** 59:11\
Yeah, it\'s OK, Shane.

**\
Alexey Khamin** 59:15\
Well.\
Beside some kagunal, both the battery location of more than which.\
Yeah, maybe the POS.

**\
Val Levitan** 59:27\
One POS per location.

**\
Alexey Khamin** 59:30\
It\'s called.

**\
Irina Shishko** 59:34\
It\'s just like a.

**\
Dzmitry Chudzinau** 59:59\
Lagrosco.

**\
Irina Shishko** 1:00:01\
Oh.

**\
Alexey Khamin** 1:00:03\
The.

**\
Dzmitry Chudzinau** 1:00:10\
I knew, yeah.

**\
Val Levitan** 1:00:16\
That\'s sort new cartridge.

**\
Dzmitry Chudzinau** 1:00:17\
OK.\
You set the coist.

**\
Val Levitan** 1:00:28\
Yeah, tomorrow stop.

**\
**1:00:29\
Probably.

**\
Val Levitan** 1:00:31\
Yeah, yeah, don\'t much.

**\
Pavel Frolov** 1:00:41\
Um.

**\
Val Levitan** 1:00:46\
I think there is a confusion about what we need to test and how we\'re
going to test it. I cannot picture anybody testing simultaneously 6 six
and a half thousand locations with 50,000.\
Issued cards but.\
Probably.\
Nobody does it and I find it to be unrealistic and and we should
probably emulate a process of some sort of a mass query, but definitely
not in the mechanic, not not mechanically, but probably.

**\
Juan Martinez** 1:01:13\
Yeah.

**\
Pavel Frolov** 1:01:22\
Um.

**\
Val Levitan** 1:01:27\
In the form of.\
Binary simulation.

**\
Pavel Frolov** 1:01:35\
Yeah, exactly as we assume to use this, Dima said. We do not even need
physical cards because we do not have so much flex POS devices and we do
not have enough.\
But all of these cards we can dump right to database and provide some
test environment where each number will be requested from the database
in case when the card need to be activated.\
In test environment.

**\
Val Levitan** 1:02:13\
So.\
So should I cancel my effort to get 10 or 20 more cards for you?

**\
Pavel Frolov** 1:02:22\
No, we we still need, let\'s say, 20 cards. They can be, I think, just.\
Uh.\
Captured in Canada or in USA and all the captured data we need to to
post here into database.\
When I say captures, they need to be, uh, swiped.

**\
Val Levitan** 1:02:51\
OK, so.

**\
Pavel Frolov** 1:02:57\
And sent all the data.

**\
Val Levitan** 1:02:59\
OK, I will issue 10 to 20 cards shipped to Minsk. That\'s my
undertaking, but but I think the the question remains how to test large
volume of process simultaneous processing.

**\
Pavel Frolov** 1:03:05\
OK.\
We definitely knows that it will not be many requests from 1 terminal,
but from different terminal at one moment. OK, I I think 20.

**\
Val Levitan** 1:03:25\
Right.

**\
Pavel Frolov** 1:03:34\
Independent access at one time. Highly likely it will be enough.

**\
Val Levitan** 1:03:39\
But access but but they never access our database, right? They access
probably Duala database.

**\
Pavel Frolov** 1:03:47\
Incom date incom, incom. Uh.

**\
Val Levitan** 1:03:49\
Oh, sorry, income database.\
So the question is to income how to simulate?\
Uh.\
Simultaneous queries.\
To their server.

**\
Pavel Frolov** 1:04:09\
Mm.

**\
Val Levitan** 1:04:10\
So that should probably be Pavel\'s undertaking.\
To income.

**\
Pavel Frolov** 1:04:21\
Actually I see in this form we are getting 20 cards and we can generate
activation process using this 20 cards in a cycle as much activation as
we need in cycle. I mean we activate card.\
Write all the data to database to process processes related to ACH
because we need to to assign what cards where.\
Generated for particular client and what ACH process need to relate to
what particular card?\
Me, it\'s, uh, quite clear.

**\
Val Levitan** 1:05:10\
OK.

**\
Pavel Frolov** 1:05:11\
And actually in case even if we had 1000 cards, what what are we really
testing? We do not test performance of income I assume.\
They they do this test for themselves.\
And highly likely for test environment it will not. They will not
provide us.\
Enough performance for test environment probably they will not support
one 100 immediate transaction at the time and but but the good question
here could be.\
To Dima, how can we optimize our communication to income? Probably we
can organize some queue not to perform more than 10 parallel
transactions to income.\
Probably it it it should be sequential request and so on.\
Hey, in this approach I don\'t think that we need more than 20 cards,
card numbers, just this numbers need need for us only in case to
differentiate different transactions to see that the transaction number
one, it was card number one, transaction #2.\
Card #2 and so on and we we can see sequence of different values
activated for particular cards and in general it will summarize in the
common transaction to ACH for card number 1/5 and.\
For example and so.

**\
Val Levitan** 1:07:27\
OK, I consider the subject closed next.

**\
Nathan Carver** 1:07:31\
Yeah.

**\
Val Levitan** 1:07:33\
Next.

**\
Alexey Khamin** 1:07:34\
But next it\'s easy. Maybe to demo how we can trigger the the invoices
without waiting 24 hours.

**\
Irina Shishko** 1:07:35\
And.

**\
Alexey Khamin** 1:07:51\
Oh, we\'re gonna get the data. We have the data from USS and.

**\
Irina Shishko** 1:07:52\
Who is the better?

**\
Alexey Khamin** 1:08:01\
I don\'t want. I don\'t want waiting for the cycle sent.

**\
Dzmitry Chudzinau** 1:08:26\
It\'s user friendly interface.\
Yes, so another bits state of.\
API API user graphic interface test.

**\
Val Levitan** 1:09:43\
OK, next subject.

**\
Juan Martinez** 1:09:47\
Just a quick question on on that one. Will we also be testing how to
avoid a duplicate entry, not just accelerating the date and time, but
also filtering out for to make sure we don\'t duplicate an invoice
item?\
want to make sure we were thinking about that.

**\
Pavel Frolov** 1:10:10\
Um.\
Uh, demo.\
The Shiitsa or Dublikatov? What was mostly Dublikatov in voice or?

**\
Dzmitry Chudzinau** 1:10:35\
Cars the transacts.\
When you call new transacts with Lincoma, when you call new transacts
with ACH.\
On the client is otherwise option, no option transact message not to
transact.\
Transfer.

**\
Pavel Frolov** 1:11:20\
So do my do my sense that each transaction from terminal to payment hub
will have its own identification number, the same each transaction from
payment hub to income. Also you\'ll have identification.

**\
Dzmitry Chudzinau** 1:11:21\
I\'m.

**\
Pavel Frolov** 1:11:40\
Numbers all the transaction is in the system. We will have this numbers.
So during the invoice generation we should implement the system to.\
To monitor this numbers to prevent such situation when duplicates is
generated, probably probably as I see it, we can insert for each line
related to activation card.\
These numbers and client can check all the numbers that there is no
duplicates independently from us.\
And to directly guide us in case when they found something to say OK
transaction number 123 ABC at 12:30.\
Value 5000 We have some complaints related to this value and we can
definitely relates to the same identification within our database on
Payment Hub to.\
To find any issues related to particular transaction.

**\
Juan Martinez** 1:13:09\
Thanks, Pabo.

**\
Val Levitan** 1:13:14\
OK, this question has been has been answered, right?

**\
Pavel Frolov** 1:13:14\
You.

**\
Alexey Khamin** 1:13:17\
No, no.\
Done.

**\
Pavel Frolov** 1:13:25\
Yeah, uh.

**\
Alexey Khamin** 1:13:30\
Yeah, it\'s.

**\
Val Levitan** 1:13:39\
How to I guess, I guess, I guess the I I guess the question is how to
test negative testing or how to test negative occurrences or negative
results. So there\'s going to be a bunch of.

**\
Pavel Frolov** 1:13:54\
How to trigger?

**\
Val Levitan** 1:13:56\
It\'s going to be a bunch of negative results. So your question is how
will we test or how will we simulate that negative results do not result
in overpayment?

**\
Dzmitry Chudzinau** 1:14:09\
Document that say we expose a payment hub with it\'s ASCP sign.\
Mhm.

**\
Alexey Khamin** 1:14:39\
No the test.

**\
Pavel Frolov** 1:14:42\
So using the API, any transaction you\'ll be able to to post some
manually entered value and Alexia you\'ll be able to enter duplicate
transactions to check that the system is correctly.\
Uh, if you search transactions.

**\
Juan Martinez** 1:15:07\
OK.

**\
Nathan Carver** 1:15:08\
Uh, create this. You can create the conditions that would cause
duplicate invoices, such as running the daily processing job twice.\
To ensure that it\'s correctly marking transactions has been connected
to an invoice and that an invoice already exists.\
Running the job a second time should not produce an empty invoice. Um,
and it shouldn\'t produce a duplicate invoice.\
Those would be things QA could easily do from the interface without a
special API.

**\
Juan Martinez** 1:15:45\
And also we we will get it. We JVL will get an invoice from Incomm that
we can reference our own transactions against. So Incomm says we owe
them 1000 and we we can verify that ourselves that that is in fact what
our side shows.

**\
Nathan Carver** 1:16:06\
Yeah, you could do some defensive programming there and feed the income
invoice into the system and have it also internally check
programmatically for values and to assure the invoices align.

**\
Pavel Frolov** 1:17:07\
Question from Alexi.\
If we are requesting some transaction, doesn\'t matter what\'s the
recipient income or the wall, it specified that we need to make repeat.
We need to repeat transaction.\
In case when we don\'t have answer.

**\
Nathan Carver** 1:17:35\
Thanks.

**\
Pavel Frolov** 1:17:37\
Or if you have some some error related to communication for example. So
if we perform retry #2, retry #4 and what should we do in case when all
the tries?\
Well done.\
But no positive answer. What\'s the logic should be here? Should we
initiate some repeat after time out or or something else?

**\
Juan Martinez** 1:18:20\
Nathan, would wouldn\'t the API actually define the number of retries? I
I I would think that it can\'t be infinite.

**\
Nathan Carver** 1:18:31\
Our API, yeah, we could put.\
You could put caps on there that well, I don\'t know if you want to
completely limit it, but perhaps escalate when a number of retries has
been performed.\
You you escalate a problem and then have other conditions at which you
would re-enable the retries.

**\
Pavel Frolov** 1:19:01\
Should it be some logic to cancel this retries or to initiate some
manual process to start this cycle again?

**\
Nathan Carver** 1:19:02\
Let\'s see.\
Yeah, and this is the system attempting to retry on a failure, correct?

**\
Pavel Frolov** 1:19:22\
Yes.

**\
Nathan Carver** 1:19:25\
Um.\
Yeah, I think that would. I think that\'s a good path is you have a
number of retries based on the error codes that you receive. So if the
server\'s down, you may wanna retry periodically.\
Um.\
And then maybe escalate. I think it\'s just going to be an engineering
just, you know, decision based on the types of codes you\'re getting,
how often you want to retry, how you want to escalate the problem, and
at what point do you stop retrying until?\
Um, there\'s manual intervention to start it again.

**\
Juan Martinez** 1:20:03\
Yeah, because if the dispensers are out of cards, we don\'t want to
infinitely retry until the cards have been refilled. There\'s no point
in retrying because we acknowledge that that error requires manual human
intervention to.\
Reload more cards so that we can continue printing. So yeah, the retries
have to be tied to the specific error that caused them.

**\
Pavel Frolov** 1:20:36\
Uh, but it\'s.\
What\'s, uh, apropos to retry?\
Yeah, just news.

**\
Val Levitan** 1:21:21\
Retry and we.

**\
Irina Shishko** 1:21:23\
Mm mm.

**\
Val Levitan** 1:21:38\
Overwhelmed their system. They charge us three and a half \$1000 per
occurrence.\
It\'s in their contract, so we have to be careful how many retries was
sent. I\'m going to say it in English. Dewala in their contract has
three and a half \$1000 penalty for overwhelming their system.\
With uh.\
Large number of API queries. Unnecessary large number of API queries. I
don\'t know what it means large and I don\'t know what it means and how
to measure it, but it\'s a heavy penalty of 3 1/2 thousand dollars per
occurrence.

**\
Irina Shishko** 1:22:05\
With.

**\
Dzmitry Chudzinau** 1:22:24\
Pasha.

**\
Val Levitan** 1:22:24\
So we can we I want, I want the developers to understand. Pasha, you
should explain to the developers that Diwala, Diwala penalize us for
overwhelming their system. They they cannot send endless number of
inquiries.

**\
Nathan Carver** 1:22:27\
I.

**\
Pavel Frolov** 1:22:31\
Mm-hmm. No.

**\
Irina Shishko** 1:22:51\
So.\
Oh.

**\
Val Levitan** 1:23:09\
The the.

**\
Irina Shishko** 1:23:10\
Mm-hmm.\
So.\
Uh.\
Send.

**\
Dzmitry Chudzinau** 1:25:28\
Stop when you provide limitations.\
Yeah.\
That one.\
The primary to.

**\
Pavel Frolov** 1:26:03\
Mm-hmm.\
So, so here\'s the question is we need to understand and know the
limitation related to Duolo or any other ECH providers. For example, how
often can we request?\
For example, Balance.

**\
Val Levitan** 1:26:32\
I think Paral, I think this is the undertaking that you should take upon
yourself to discuss with Walla and income.

**\
Pavel Frolov** 1:26:33\
Uh.\
For income, I think we we know everything and they don\'t know.

**\
Val Levitan** 1:26:49\
But but, but regardless, it\'s it\'s worthwhile discussing it again.

**\
Pavel Frolov** 1:26:55\
Mhm.\
OK, I I will make a notes when they open.\
Open support for us. We can ask all the particular technical question,
how often, what limitation, what the prices and so on.

**\
Val Levitan** 1:27:25\
By we meaning we meaning you.

**\
Pavel Frolov** 1:27:30\
I mean me, Nathan, Juan.\
Who can participate?

**\
Val Levitan** 1:27:35\
But let\'s leave it to let, but let\'s leave it in the engineering
domain. But let\'s not put it on administration on domain. So it\'s an
engineering question.

**\
Pavel Frolov** 1:27:48\
OK.\
I think this is the last questions is also question to Duvala. Is it
possible to simulate some error cases from Duvala responses?

**\
Alexey Khamin** 1:28:35\
I use TPI or AA for me and.\
We told that.\
Has not 500.\
I love you.\
But maybe as the demo said we can do it on our side.

**\
Val Levitan** 1:29:15\
OK.

**\
Irina Shishko** 1:29:34\
I lost it if so.

**\
Alexey Khamin** 1:29:36\
Uh, go next some questions or the head answer.\
A book that uh.\
One question. It\'s about so.\
How we can, uh, check?\
Emerging from.\
It\'s question to GMI, I think.

**\
Val Levitan** 1:30:25\
No, I think this question should be.\
Address to Dimay. It should be his undertaking.\
And he should get back to us when the decision will mature.\
Mature.\
But it should be his undertaking.

**\
**1:30:50\
Yeah.

**\
Alexey Khamin** 1:30:56\
OK. Yeah, that\'s it for me.

**\
Val Levitan** 1:30:56\
OK, um.\
OK. Thank you. We\'re about 5 minutes past the mark.

**\
Irina Shishko** 1:31:02\
OK.

**\
Val Levitan** 1:31:11\
So I\'m happy to continue if anybody has questions, otherwise I would
like to.\
close this meeting. I think we have a set of undertakings that we
documented through the transcript. Pavel, please place the transcript in
this meeting when it\'s ready. I encourage everybody to.\
Prepare for the next meeting by first, fulfilling the undertakings from
this meeting and then, if possible, maybe we should circulate the
objectives of the meeting ahead of time so we come prepared.\
So the meeting is more structured and when we open the meeting, we
don\'t have to think about what to discuss. The objectives should be
sent with the invitation.\
Or at least updated prior to the meeting.

**\
Pavel Frolov** 1:32:16\
Mm-hmm.

**\
Val Levitan** 1:32:16\
So in this case, Pavel should be taking charge of these meetings. Like
you should be the driver, you should be the force behind it.

**\
Pavel Frolov** 1:32:28\
Mm-hmm.

**\
Val Levitan** 1:32:28\
It\'s your it\'s your bulldozer now, like you got to get through the
walls.

**\
Pavel Frolov** 1:32:35\
Okay, clear.

**\
Val Levitan** 1:32:38\
OK. When is our next meeting?\
I don\'t see any point meeting tomorrow.

**\
Pavel Frolov** 1:32:48\
At least at least we need to to be prepared.\
Uh.

**\
Val Levitan** 1:32:54\
Hello.

**\
Pavel Frolov** 1:33:10\
Uh.

**\
Irina Shishko** 1:33:12\
By the put.

**\
Pavel Frolov** 1:33:28\
OK, what about uh uh Thursday same time?

**\
Val Levitan** 1:33:39\
OK.

**\
Pavel Frolov** 1:33:43\
OK, create a location.\
Uh, well, we.

**\
Val Levitan** 1:34:17\
My, my, yeah, go ahead.

**\
Pavel Frolov** 1:34:19\
We\'re going to create. I\'m going to create an invitation for Thursday,
same time.\
Irina cannot attend on Wednesday and asked him to move it for Thursday.\
Um.\
Mhm.\
Just send the invitation.

**\
Pavel Frolov** stopped transcription
