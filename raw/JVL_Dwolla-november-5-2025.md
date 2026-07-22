**JVL + Dwolla-20251105_101938-Meeting Recording**

5 November 2025, 03:19pm

31m 52s

**\
Val Levitan** started transcription

**\
Cody Van Wyk** 0:03\
Quick points. I see the recording is just getting started.

**\
Val Levitan** 0:07\
So should I should I terminate the recording?

**\
Cody Van Wyk** 0:09\
No, it\'s fine. It\'s totally fine. Just I just wanted to interject a
couple of points. Val, we connected Monday. I know I still owe you a
couple of things, so I\'m working on it. I\'ve had a full plate here,
but I\'ll follow up with you hopefully by tomorrow on those points on
the contract we do.

**\
Val Levitan** 0:09\
The recording.

**\
Cody Van Wyk** 0:26\
With each client during onboarding typically meet once a week, Nancy and
I with the client and we have a developer relations team that may be
more equipped to dive into the technical details with you. Spencer and
Shreya are.\
Are on that team. So once we get the contracting piece behind us, we\'ll
set that up. We\'ll have a kickoff meeting. I think we worked with
Nathan this morning to get him invited to that onboarding project plan
portal. He had a little bit of a technical issue. So we do have.\
Great supports process and teams and it\'s really well organized. We
just haven\'t quite gotten there yet and I owe you a follow up on the
contract. So bear with me a minute on that, but take it away Pavel.
Happy to connect with you this morning. Thanks.

**\
Val Levitan** 1:07\
Of course.\
Of course, and and just to be very quick, the purpose of this meeting is
to understand how to enroll the engineers and how the whole structure is
working. So you are actually partially answering the question. So yeah,
go, go ahead.

**\
Pavel Frolov** 1:10\
Uh.\
Yeah, exactly. Because because I I think we will have lots of question
during the process when we start working with your service. So initially
it was a question when we tried to play with your sandbox.\
We able to create customers, but it was a problem how to make them
verified, but actually we just found a solution.\
Practically 10 minutes ago we\'re able to do this using API.\
So probably the last question for today for us to understand the
environment because actually I think we need to work in in such
environments that.\
We have one bank account that we want to use to get money from other
customers to this account and we need to create many of customers with
bank accounts that we need to charge.\
From probably you can guide us how to start, what to create, should we
create customers and what types of customers?

**\
Cody Van Wyk** 2:54\
The customer object for JVL.\
Unverified customer is what you\'ll be utilizing Pavel. You\'ll see in
there verified customer and something called receive only user, which is
very similar to unverified customer.

**\
Pavel Frolov** 3:04\
Mhm.\
Mm-hmm.

**\
Cody Van Wyk** 3:17\
You\'re going to be using the unverified customer.\
Did that address what you were asking about?

**\
Pavel Frolov** 3:29\
No, not exactly. For some reason I can\'t can\'t show you the sandbox.
It\'s not it\'s not working for me right now.

**\
Nancy Baccam** 3:37\
OK.

**\
Cody Van Wyk** 3:41\
The screen share.

**\
Pavel Frolov** 3:43\
Yeah, one second. Try.

**\
Val Levitan** 3:45\
Well, maybe Cody could, maybe Cody could initiate the sandbox and you
just tell her where to go.

**\
Pavel Frolov** 3:54\
Oh, it\'s OK. It works OK.\
So here on the customer tab you have dashboard with all the customers
that we are able to create and change settings. I already understand how
to make them verified.\
It\'s not a problem, but from now for our developers, it\'s important to
understand in the real world how can we operate. For example, we will
need to create a customer JVL.\
Uh, with assigned Uh bank account.\
Also here or it should be something else how it can be organised. One
account, one bank account to get money on it and lots of other customers
with their bank accounts to take money from.\
Do we need to create all the customers in this list?

**\
Cody Van Wyk** 5:10\
Yeah, so your your basic setup Pavel is the retail location.

**\
Pavel Frolov** 5:18\
Mhm.

**\
Cody Van Wyk** 5:18\
Convenience store in Georgia. We\'ve talked to that in this case with
Nathan previously. They\'ll be an unverified customer. You\'ll create
them on your wall application as unverified customer, which looks like
what you\'ve been doing in the sandbox environment you\'re showing.

**\
Pavel Frolov** 5:22\
Yes.\
Uh, unverified.

**\
Nancy Baccam** 5:35\
Mm.

**\
Cody Van Wyk** 5:36\
Here verifying the bank account, the bank funding source. It is a
distinct and separate thing. You\'ve got the customer object and the
funding source object or bank account. Bank account needs to be
verified, customers unverified.

**\
Nancy Baccam** 5:38\
OK.

**\
Cody Van Wyk** 5:55\
And that\'s it.

**\
Pavel Frolov** 5:55\
Oh, OK, OK, OK.

**\
Cody Van Wyk** 5:58\
And same, same to ACH is we\'ve talked through that with Val, like
that\'s the focus. That\'s what you\'re looking to do.

**\
Pavel Frolov** 6:08\
OK.

**\
Nancy Baccam** 6:09\
Yeah, I.

**\
Pavel Frolov** 6:11\
Uh.

**\
Nancy Baccam** 6:13\
Pavel, so did you create these customers in this dashboard or did you do
the API? OK, so the customers you\'re creating in this dashboard are
receive only users, which is not the correct customer types that you
should be creating.

**\
Pavel Frolov** 6:19\
Yes.

**\
Nancy Baccam** 6:28\
In order to create customers, you have to do that via API call.

**\
Cody Van Wyk** 6:32\
It.\
Side point, Nancy. It shows an unverified customer in the dashboard.
Why?

**\
Nancy Baccam** 6:42\
No, I can see it as receive only. I don\'t know why the customer, why
it\'s reflecting it that way in the dashboard.

**\
Pavel Frolov** 6:42\
OK.

**\
Cody Van Wyk** 6:42\
if it\'s a receive only user.

**\
Nancy Baccam** 6:53\
Because we do allow.

**\
Cody Van Wyk** 6:54\
Just says.\
That\'s so confusing. Why did they build that UI like that?

**\
Nancy Baccam** 6:57\
Yeah, they just did some updates to the UI recently. Our product team, I
know that. So I don\'t know why that\'s showing that way. Yeah, and send
it.

**\
Cody Van Wyk** 7:07\
Can I screenshot this?\
Pavel, I\'m just gonna take it. I won\'t get.\
Can you go? Do you want to go back and screen share?

**\
Pavel Frolov** 7:16\
Oh, OK, one second.

**\
Cody Van Wyk** 7:19\
It\'s gonna screenshot the dashboard there and share that with our
product team that.

**\
Pavel Frolov** 7:24\
OK.

**\
Cody Van Wyk** 7:25\
Seems kind of odd. They built it that way. OK, it\'s just your sandbox
environment. OK, here we go.\
Thank you.

**\
Pavel Frolov** 7:37\
So I I think we\'re going to organize meetings with your developers to
fast access to to such questions like like I\'m asking you to.

**\
Cody Van Wyk** 7:51\
Yeah.

**\
Nancy Baccam** 7:53\
Yeah, so let me just jump in here. So right now this project plan, which
let me share, I don\'t know if I can share my screen, but if you go to
the onboarding.duwala.com project plan.\
Right now if you look at that, you only see a handful of tasks because
we again we need to get through the contracting risk review items first
and then once we get you guys pre-approved by our risk team, it will
unlock all these additional tasks within the project plan which will
also include development.\
Task specific for you and your team and they\'ll have different sections
with a lot of different tasks that breaks down, creating customers,
creating funding. So it\'s kind of walking you through. Here are the
things you guys should be testing within the sandbox environment and
links to your documentation as well. So that should help guide you and
your team.\
And then like Cody mentioned, she will have, we\'ll have an official
sort of like kick off call. I\'ll I\'ll kind of walk through the project
plan, talk through those, you know those phases and those tasks. And
then Yep, moving forward, we would set up really how often you guys want
to meet, whether that\'s once a week.\
Whatever cadence you guys decide, you guys want to meet where myself,
Cody and then someone from our dev team will be on on that and you guys
can go ahead and ask questions, you know, as they come up for for
development. So yeah, we\'ll be in constant communication. The project
plan also has like a chat feature where you can type a message and ask a
question as well if you\'re working.\
You know, maybe since I know the time zones are different and we\'ll
respond to you though, you know the next following day as well, so.

**\
Val Levitan** 9:30\
No.

**\
Pavel Frolov** 9:32\
Yeah, good. It works for us.

**\
Nancy Baccam** 9:35\
We also have to configure so your sandbox account. Pavel, I know that
you signed up for your own sandbox account and so you have your own set
of API testing keys. I also just did a quick check before hopping on
this call and it looks like.\
A handful of other members of your team sign up for their own sandbox
account as well. So are you guys each trying to test with different API
keys or are you really wanting to? Because like the way that it works is
if you guys sign up for your own sandbox accounts, you guys have your
own.\
API key, your own set of customers, your own set of like they don\'t.
Each environment then is separate. So are you and your team wanting to
perhaps just maybe just have one sandbox account? OK, OK.

**\
Pavel Frolov** 10:20\
No, no, no. It\'s OK to have separate because we will need at least a
personal account for developer, then staging account and then probably.

**\
Nancy Baccam** 10:30\
OK.\
OK, I just wanted to double check because I do have to manually
configure each sandbox account so that the the configuration will match
what\'s gonna be in production and so I\'ll I see that there\'s.\
1234.\
There\'s five different sandbox accounts, so I\'ll go in and manually
figure those and because there\'s another account saying that we manage
where again for JBL what what you guys would be doing is what we call
the receive flow where you\'re just receiving funds in from customers.
And so again that\'s a a setting that we control on our end, so I\'ll
update.

**\
Val Levitan** 10:53\
OK.

**\
Nancy Baccam** 11:12\
I\'ll update, yeah, your sandbox accounts to make sure that it\'s going
to reflect what would be in production as well just to make sure that,
yeah, you guys are testing and doing the right things. But yeah, like I
like we mentioned once we kind of get you guys passed through sort of
the commercials and.\
Administrative items, once we actually get into that kickoff call and
talk through, you know, the development task things, it will all make a
little bit more sense for you and the team.

**\
Pavel Frolov** 11:47\
So, so I think you can find our sandbox accounts right now and set up
for all of them.

**\
Nancy Baccam** 11:55\
And.

**\
Val Levitan** 11:59\
Are you saying, Nancy, that we don\'t need so many sandboxes? Am I
detecting? Maybe we maybe we shouldn\'t have configured individual
sandboxes and just use a company sandbox. Can you teach us best best
practices?

**\
Pavel Frolov** 11:59\
Uh.\
OK.

**\
Nancy Baccam** 12:15\
Yeah, so I don\'t know if I can share my screen maybe.

**\
Val Levitan** 12:21\
Yeah, sure, stop top right.

**\
Nancy Baccam** 12:21\
OK, I.\
OK, so let me find. Sorry.\
So I see Pavel, Nathan, Dmitri, Serge. So these are all individual
sandbox accounts. I\'m gonna log in as sorry, this is gonna look a
little bit different. Am I sharing my screen? I can\'t see if I am.

**\
Pavel Frolov** 12:48\
Yes, yes.

**\
Cody Van Wyk** 12:49\
You are.

**\
Nancy Baccam** 12:49\
So this is again, assuming Nathan or not Nathan Pavel, if I\'m logged in
as you because it has your information here. So if you go to
applications, this is the API key and secret that you\'re working with,
right? You do have the option.

**\
Pavel Frolov** 13:04\
Yes.

**\
Nancy Baccam** 13:06\
So if you guys are again sort of like if you guys want to have one
account where you guys are all creating different customers and testing
sort of using one API key, what you can do is have invite your other
team members. So if you click on teams there should be like a plus sign
for you to invite anybody else to have access to this so that when you
are testing.\
And making those API calls, like any customers you\'re creating, any
funding sources, transfers that you are initiating, it will all show up,
you know, for for your team. They\'ll be able to see all that data
within the Duala dashboard.\
Right now I see like Nathan has his own sandbox account, his own e-mail
and so if he\'s testing doing something separately and see he\'s wanting
you to see maybe like you know what\'s going on with this customer like
you guys won\'t be able to see each other\'s data cause it\'s two
separate sandbox accounts so.\
So yeah, I guess it just depends on how how you guys want to handle that
with it. I don\'t know how many different team members are going to be
testing, but if you guys want to be able to see each other\'s data and
customers you guys created, I would recommend that you guys, maybe
Pavel, you you\'re the main admin user. Go ahead and invite other team
members to join.\
And you guys are just working off of one API key.

**\
Pavel Frolov** 14:26\
Yeah, OK, clear. This clear.

**\
Nancy Baccam** 14:29\
That\'s what most most folks would do. And then if you have a separate,
I think you mentioned maybe like a separate staging environment, then in
that instance you can set up a a new sandbox account, right? So you get
a set of new testing keys so they can keep it totally separate, so.\
Yeah, just let me know. Yeah. Either way, the accounts that are set up
today, I\'ll go ahead and configure them so that they will match
essentially what\'s going to be in production in the project plan here.\
If you go under spaces and there\'s an integration overview, this is
essentially outlining sort of what we discussed early on of what your
expected integration is going to look like. So you guys are going to be,
you know, debiting from what we what we mentioned, the unverified
customer records.\
And so again, your funds flow is what we call the receive flow
unverified and I\'ll have to enable these faster speeds as well on your
account. So you guys start testing out sort of the faster ACH speeds and
then same thing with transaction limits. So I\'ll configure your sandbox
so that it, you know, matches everything here.\
But we would talk through this and confirm that everything makes sense
here as well once we have the kickoff call after Cody has received
approval from our risk team.

**\
Val Levitan** 15:53\
And how long, how far are we away from potentially receiving the
approval? Is it weeks or days?

**\
Nancy Baccam** 16:07\
Um, I.\
I I mean, it might take a week or so, just depends if whenever you guys
provide, I guess Cody, do you have financials or anything like that yet?

**\
Cody Van Wyk** 16:18\
No, we\'re and we don\'t have like we\'re working on the contract too,
I.

**\
Nancy Baccam** 16:19\
Okay, yeah.

**\
Cody Van Wyk** 16:24\
I have a follow up, but so yeah, it\'s.

**\
Val Levitan** 16:25\
So, so, so I guess, I guess contract comes first.\
Then you\'ll probably when we sign the contract, you\'ll send you a list
of requirements of what you would like to receive from us. Then that
goes through process.

**\
Cody Van Wyk** 16:33\
Wait.

**\
Nancy Baccam** 16:39\
Mhm.

**\
Cody Van Wyk** 16:42\
Me.\
I think, yeah, thanks for pulling that up, Nancy.

**\
Nancy Baccam** 16:47\
We talked about this a little bit early on.

**\
Cody Van Wyk** 16:49\
This is the order of operations, your account registration. I think
Monica is going to handle that. I not sure if it\'s been started.\
Reviewing the financial position bank statement, our Duwalla\'s risk
department will review.\
All of that with giving you the contracts, we\'ve kind of done Step 3,
getting the the first one, the integration agreement signed would be the
precursor for kicking off the review, which is Step 4 and I see if you
go forward one slide.\
All of these areas for review will need to be completed by JBL and its
team. So if you want to divide and say hey Pavel, you can take Infosec,
fill this out, complete it, submit it to Duala and Nathan.\
You are filling out the UX.\
And the legal piece of it, you could do it that way. And that\'s where
we\'re meeting with your team every week. We\'ll pull on our dev rel
team also tying it together with the technical side of what they built
within your sandbox environment. You know the developer relations team
at Duala will be able to.\
There will probably be questions that your team will have and we can
help work through those.\
Both in that onboarding portal and in meetings, calls like this, you
know, in real life.\
We have clients to to get back to the root of your question, Val. We\'ve
had clients work through these, all of them within a few weeks. It\'s
not uncommon. Others can take a little longer. So it\'s not a very,
it\'s not super complicated, the flow that you\'re building.\
But there there is these review and due diligence areas that we complete
with each client and the project plan will be tailored accordingly at
onboarding.dwell.com. So I think getting your team in there, getting
them to start reviewing that.\
Nathan had a technical issue getting signed in there will be vital. And
then having a weekly meeting or every maybe twice a week meeting with
your team where everyone comes together and we talk through different
you know what you\'re working on, what issues are you seeing and kind of
troubleshoot it.

**\
Val Levitan** 19:06\
I understand. So how how would I get?\
Uh.\
The list of deliverables required from our legal team.

**\
Cody Van Wyk** 19:21\
Yeah, it\'s a good, good question. So if you click, Nancy, just go ahead
and click the integration guide. We have shared this document with your
team previously, Val, Nathan has it and I think Juan and Pavel as well.\
This guide is called the Integration Guide. It lays out to the inth
degree what we would need depending upon your build. Now there are a lot
of things within this that you won\'t need or you can ignore.\
And so we can help. That\'s what the project plan does is help narrow
your team so they\'re focusing on the right areas and not building out
like verified customer stuff for example. But this is it and the legal
side of it, the terms and conditions.

**\
Nancy Baccam** 20:05\
Mhm.

**\
Val Levitan** 20:19\
OK, so.

**\
Cody Van Wyk** 20:19\
Ultimately works through with each client to get that approved.

**\
Val Levitan** 20:23\
OK, so should I work with Nancy just to figure out our particular list
of deliverables that you want from our legal department?

**\
Cody Van Wyk** 20:30\
Yes, Yep.\
Yeah.\
Yeah, Nancy, go back to the slide deck. Here\'s a way of thinking of it,
Val. Go back one slide. Nancy needs to be involved for all
communications herein. I am your main point of contact for this stuff.
Contracting account registration.\
And then move forward on Nancy. Nancy will work through all of this
stuff with your team and our Devrel team. I\'ll be there too, but to a
much lesser degree because that\'s what they do.\
And then when?

**\
Val Levitan** 21:07\
OK, Nancy, can you, can you babysit me through making me understand what
are the deliverables, exact deliverables from our legal team? And then,
you know, just like every culture in our company, I have this presence
about me that you know if I.\
Know what needs to be delivered. It usually gets delivered faster.

**\
Nancy Baccam** 21:30\
Mm-hmm. Um.

**\
Val Levitan** 21:32\
And that\'s and that\'s our culture. So I would like to understand
precisely what our legal team needs to deliver so we can expedite the
process of.\
Yeah, of enrollment. I guess I don\'t need Pavel in this meeting. We
don\'t need Cody, I assume. I mean, he\'s welcome to stay, but I don\'t
think we need to eat up anybody\'s time on that.\
May I organize myself with you directly to work on these things?

**\
Nancy Baccam** 22:06\
Yeah, I mean, I guess, are you, are you asking for signing up the
registration, that portion, OK.

**\
Val Levitan** 22:06\
Nancy.

**\
Cody Van Wyk** 22:12\
Yeah, we we we can work on that Val Val. We need to make progress on
this side here first like be getting the account registered, the
financial position review and contracts which we talked through Monday.
I just I\'ve been I\'ve.\
Had a lot on my plate, so I I\'ll work on getting you a follow up on the
contract front. Um, but that\'s where we\'re at, yeah.

**\
Val Levitan** 22:33\
No, no, that\'s no, that\'s fine. No, no, that\'s fine. I know that this
is on your side of the fence and and you\'re kind of running as fast as
you can. You just need a little bit of time. I know that part. I want to
prepare myself for delivering legal documents to you.

**\
Cody Van Wyk** 22:40\
Yeah.\
Yeah.

**\
Val Levitan** 22:51\
And because I\'m not very quick on my feet, I\'d like to take as much
time as possible in preparing myself for that next stage. While you,
Cody, still doing your stuff, I\'m asking whether I could work with
Nancy on getting the list of deliverables.\
From us to you, from our legal department.

**\
Cody Van Wyk** 23:17\
Populating the Rocket Lane project, Nancy, with the legal stuff, I mean.

**\
Nancy Baccam** 23:23\
Yeah, I was trying to pull up an example cause right now and that will
all populate and it will tell you exactly what we\'ll need in this
project plan. Like right now it just has these phases because we need to
get you guys approved first in this area once we get you.\
Then the remaining tasks for legal and everything really on this slide
here will populate as separate tasks for you. So really terms of service
and terms of service of privacy policy review are the main legal
documents that we\'ll look that we\'ll need.\
If you guys have these on your website already, then you know you just
give us a link to that so.

**\
Val Levitan** 24:11\
Well, you know, a simple thing. I saw this particular menu and uh.

**\
Nancy Baccam** 24:16\
Mhm.

**\
Val Levitan** 24:18\
I don\'t know what to do with it. Like I I do you want me to press any
buttons or like what do you want me to do with this thing? I so I see
it. It\'s in front of me. When I log in, what what should I be doing
with it? That\'s it. I I love the way you work.\
I actually, I wish JDL had this much sophistication, but I just, I\'m
not versed in it. I don\'t know what you want me to do with it.

**\
Nancy Baccam** 24:43\
Yeah, so right, right now this project plan, this is what we\'re trying
to get set up right now. The account set up, we have signed it I believe
to Monica to to register the account. So this is telling her the
instructions of what she needs to do to register for the Duwalla
production account.

**\
Cody Van Wyk** 24:44\
The.

**\
Val Levitan** 25:03\
OK, so I I need to see what Monica is seeing. Am I seeing this?

**\
Nancy Baccam** 25:09\
Oh.\
Do you? Have you logged into onboarding.dwell.com? OK, yeah, you guys,
your entire team should have access to view all of this. So right now we
have Juan, Monica, Nathan, Pavel and Val. Yeah, so everyone.

**\
Val Levitan** 25:18\
Yeah.

**\
Nancy Baccam** 25:32\
Everyone here has access to this project plan.

**\
Val Levitan** 25:36\
OK, so how do I see? Show me how to see what Monica\'s deliverables are.

**\
Nancy Baccam** 25:42\
If you click into the task, the signee, it\'s assigned to Monica and
we\'ve tagged her in as well to let her know, hey, you know, please
complete this step to register the account set up.

**\
Val Levitan** 25:54\
No, no, no, not that. So that\'s fine. So what are the deliverables
here?

**\
Nancy Baccam** 26:00\
For you guys to register a production account. After that\'s done,
attach a billing account. Again, this all happens within our Duala
production account. That\'s all the details of what you guys need to do
is listed there. The risk review use case. This is things that I mean
Cody.\
Right now they\'re assigned to Cody, Cody to Cody at this point, cause
he again has to get you guys those contracts and you know.

**\
Val Levitan** 26:26\
No, I I got it. I got I I no, I got it. Can you show me what\'s
Monica\'s deliverables?

**\
Cody Van Wyk** 26:27\
They have the contracts, yeah.

**\
Nancy Baccam** 26:35\
Register the production account.

**\
Val Levitan** 26:38\
What does it mean? Register the production account? I don\'t understand
this.

**\
Cody Van Wyk** 26:41\
OK.\
If you click in here, it does describe it. Val. Monica had communicated
that she would be handling that portion of it. I think let\'s start with
the basic block. Nancy is Monica in this portal? I\'m not. I haven\'t
looked this morning, but.

**\
Nancy Baccam** 27:01\
Yeah.

**\
Cody Van Wyk** 27:02\
OK, so Monica, let\'s start. Go back there a minute.\
Locking and tackling, OK.\
Back. Nope, you\'re on the slide deck. Go to The Who has joined the
rocket lane? There we go. Everyone has joined. Your whole team is within
this onboarding project portal. This is home central for.

**\
Nancy Baccam** 27:18\
Everyone\'s.

**\
Cody Van Wyk** 27:26\
Moving forward, submitting due diligence and getting approved to go live
with Tuala. That\'s good. So we\'ve got your team in there. Monica,
we\'ve go back now, go to the thing, register your account. We
communicated.\
With Monica in here, it doesn\'t look like she\'s responded around
registering the productive environment account. I had also emailed about
this a couple of weeks back and she\'d mentioned that she would be
handling this part portion of it.\
So generally speaking, we try and keep communications within this
project portal so we\'re all have visibility on it. We can use the
e-mail thread for this section. It\'s not a big deal because I I did
e-mail you previously about it.\
But this is what this is, is where KY being JVL Inc registered in
Florida or Delaware or whatever your company is. If it\'s beneficially
owned, there\'s beneficial ownership to it. There is a guide.\
Robably within here, maybe not. I\'ll drop it in the chat.\
Around what this is.\
And what you\'ll need, let\'s see if there\'s a chat function here. Here
we go. This was in the e-mail sent to Monica a couple of weeks back, and
I don\'t think she\'s created the account yet. So that\'s step one is
getting this going.\
And getting it verified, it can take a couple days.\
Does that help provide some context, Val?

**\
Val Levitan** 29:06\
It it, it did. It\'s actually quite clear. I understood everything
you\'re saying. The only thing that I don\'t understand is the taxonomy
that you\'re using. When you say production account, what does it mean
production?

**\
Cody Van Wyk** 29:19\
Yep. I\'ll I\'ll clarify. Yep. So.\
You have your sandbox account. JVL has that with, you know, Pavel has
one. I think Nathan has one. We\'ve configured certain settings for them
to be able to test and build and develop.

**\
Val Levitan** 29:34\
You know sandbox is the is your is your play account. This is you. You
know you have your children playing in the sandbox. I got it.

**\
Pavel Frolov** 29:37\
2.

**\
Cody Van Wyk** 29:37\
Yeah, correct.\
Correct sandbox environment, productive environment is separate
environments, technical environments wherein we would eventually provide
your API keys for go live when you\'re approved and ready to go live.\
They\'re separate technical environments. This is real information here,
yeah.

**\
Val Levitan** 29:57\
So here.\
So in order to set up this, sorry for interruption. In order to set up
this production environment or production account, Monica needs to open
that account and by opening she needs to supply a set of corporate
information.

**\
Cody Van Wyk** 30:12\
Correct.

**\
Val Levitan** 30:17\
I am looking for the list of that information that you are looking for
Monica to supply.

**\
Cody Van Wyk** 30:18\
Correct. Yep.\
I dropped a link in the chat for this meeting that lays that out. Nancy,
if you click that link in the chat.\
This is it. This is the guide you need. And this should be in Rocket
Lane. I\'m not sure why it\'s not. This is a good guide that she\'ll
want to reference. I\'d also emailed this to Monica a week or so back.\
But it walks you through the different sections, the information you\'d
need. We may need a document, an EIN letter.

**\
Nancy Baccam** 31:01\
You will, yeah. It says it up here too. We\'ll need businesses EIN
letter.\
Um.\
Whoever\'s registering so Monica, whoever she\'s entering as.

**\
Val Levitan** 31:15\
OK, let me let me let let me thoroughly understand this.\
Clear.\
OK. I I think this meeting covers more than we were hoping for. So thank
you very much. Let us continue working on this. And of course, Cody,
we\'re looking for.

**\
Cody Van Wyk** 31:33\
Yeah.

**\
Val Levitan** 31:38\
The information when you you know when you get around this.

**\
Cody Van Wyk** 31:42\
Yep, Yep. I\'m hoping we can have have an update on that tomorrow. Well,
so.

**\
Pavel Frolov** 31:48\
Thank you. Bye.

**\
Val Levitan** stopped transcription
