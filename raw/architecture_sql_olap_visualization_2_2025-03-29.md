---
tags:
  - SQL-OLAP-visualization
  - SAS-protocol-integration
  - cloud-architecture
  - technical
  - design
  - strategy
---

Architecture of SQL_OLAP_Visualization -- 2

Summary by Copilot:

> Here\'s a summary of the document:
>
> The document details a meeting discussion about the architecture for
> SQL OLAP visualization and the integration of SAS protocols. The team
> explores various options for system design, including the use of
> third-party or proprietary SAS hosts, and considers the implications
> of future legislation and technology trends.

-   **Meeting Overview**: The meeting covers the broad topic of
    designing an SQL OLAP visualization system, focusing on integrating
    SAS protocols and considering future technological trends and
    legislative requirements.**^12^**

-   **SAS Protocol Integration**: Different options for integrating SAS
    protocols are discussed, including using third-party SAS hosts or
    developing proprietary solutions within kiosks to reduce hardware
    overhead and costs.**^34^**

-   **Current System Limitations**: The existing system involves
    machines reporting to a remote SQL database server, converting data
    to Excel, and presenting it in Tableau, which is labor-intensive and
    inefficient.**^56^**

-   **Future Considerations**: The team considers moving towards Power
    BI for data visualization due to its integration with Microsoft 365
    and potential cost benefits.**^78^**

-   **Cloud and Hardware Solutions**: Discussions include replacing
    physical hardware with cloud architecture and the potential benefits
    and challenges of such a transition.**^910^**

-   **Technical Details**: Technical aspects such as using serial to
    Ethernet converters, micro PCs for player tracking, and ensuring
    robust communication protocols are explored.**^1112^**

-   **Next Steps**: The team plans to study both SAS/Tito and digital
    wallet solutions, revising the schematic for future
    meetings.**^1314^**

**Transcript:**

okay good morning everyone today our meeting is a little bit broader and
we have

more on the board I invite everybody to the bureau board please this

is where you should be

So, Pavel, maybe you should brief us on what do we see on the mirror
board,

so everybody is aligned accordingly.

I just tried to present some sorts about different options,

how to build a system based on SAS protocol.

I assume that all machines, our machines, and third party machines,

already equipped with the second SAS. And then they connect these
machines

to SAS Post to operate.

Usually, as I understand, it\'s done through some sort of converters or
player

tracking systems that installed within each of the machine to convert
SAS to some as

a proprietary protocol based on the physical Ethernet channel.

And all of these machines finally connects to some SaaS host or back
office system

that facilitates as a forced to play the transactions to machine and
from machines

so in this general statements and from this moment we can split this
into two

different options first option when Vensas host is provided by third
party

and we just need to provide a solution how to connect our kiosk to
already existing

system. And

the second diagram shows that,

for example, we are going to implement our own SAS post that can be run
as an

separate hardware or within our kiosk. I assume this is a preferable way
because it

saves money for operator and we can say that we have a

better solution, cheaper solution, and provide cheaper way to allow
other machines to

work using SAS with minimal hardware overhead.

Because first schematic I assume that it\'s quite costly for the
operator to set back

-office system,

to install kiosk, our kiosk or third -party kiosk doesn\'t matter.

Any question on this moment?

What\'s the intention of this architecture?

Are you attempting to just log and store the SAS commands remotely? Are
you pushing

the \[INAUDIBLE\] further away? Let me answer this question. If we could
go to the

top schematic,

The discussion started from the current solution.

Follow me please, I\'m here.

Everybody can come in here please. Okay, so the current solution in
place right now

is our machines report to SQL database server that is in a remote
hosting facility

via direct connection or through QR code.

This data goes into OLAP,

convert it into Excel format, present it in Tableau.

This doesn\'t work for us anymore. It requires manual labor for
preparing Excel and

Tableau files. It\'s I think it occupies one and a half person
permanently and

It\'s an issue So of course we can take from all up,

we can take the data from all up server, please follow me,

get directly into Tableau presented in the reports. But the problem is
that we don\'t

have any expertise in Tableau and for us it doesn\'t matter whether to
learn Tableau

or any other program,

still time consuming. Also the current application,

sorry, current architecture today has,

what

do you call this, Microsoft reminds me of the name of this server.
Active Directory.

Active Directory. So we have Active Directory in Minsk,

Toronto and the data center. I don\'t know the exact architecture,

but it\'s kind of duplicate installations. And this installation,

from what I understand, synchronizes actively. I don\'t know how it
works.

It doesn\'t matter. But it allows us today, we can take the data from
all up.

Again, Questionable do we need to all up? We don\'t have so much data

Put it into power BI we have to learn either tableau or power BI and
because we\'re

Microsoft house more or less Probably we should go with power BI in
terms of cost.

It\'s about the same and then create a visualization for the data It
opens up a

question whether we need to deploy Azure to some extent. We\'re mostly
Microsoft 365

Outlook and other applications. So eventually everything gravitates
towards Azure and

Active Directory.

Andre here could talk much more about it. To add to this architecture,

if you follow my cursor, the new thing that\'s coming online is our
kiosk and the

flex port as it will be rolled out in 2026.

I make an emphasis on 2026 June, not 25 because I refer it in the past
as the

deadline for 2025. I made a mistake. the deadline is June 2026.

The legislation in Georgia will dictate that all winnings must be
converted into a

prepaid card. So this whole architecture needs to be entertained.

As we started to entertain this architecture, Power BI Azur, we said,

well, hold on a second follow me please how would in 2026 this work it
could be

that either our kiosk will be installed or competitive kiosk will be
installed one

moment there is one more point here as part of the architecture here
we\'re saying

there could be

a piece of hardware, kind of a kiosk deployed in a location,

or we can advance this design into cloud architecture,

so we can physically replace costly hardware with cloud architecture.

Okay, so as we started to think how it will all work. We understand that
it could

be our physical kiosk or I guess some sort of competitive kiosk. So
Pavel started

to imagine how the competitive kiosk will work. We know that it\'s a SAS
bound

technology. The competitors will not introduce any new technology,

so it\'s for sure SAS and Tito.

And I guess here Pavel is imagining, I assume he\'s imagining how our
architecture

will advance by replacing this hardware piece with cloud piece.

I\'m assuming. No? No. This is also hardware solution,

but first schematic shows using third -party back office hardware and
the second one

if we replace with our kiosk software some features related to sus post

cloud solution will be next so in here we\'ll probably imagine cloud
solution.

So,

and just to underline who is in this meeting.

So, Dima and Sergei are designing back office solutions,

back office architecture. So,

That\'s the primary design team here, and of course, Andrej is designing
DevOps.

On this diagram here where it says is FlexPay with integrated SaaS. I\'m
seeing JBL\'s

protocol right here. What does that mean?

Where are you? Sorry? Oh, here. Okay. Yeah.

What is that? It\'s probably WSS. Yeah, some sort of\...

It\'s related to current WebSocket probably will step forward with some
updates to

this protocol, but very likely it will be WebSocket secure protocol. So
the intention

is to allow third -party gaming machines to collect SAS data from it and
collect

things from JBL machines that are also talking same SAS. And then
that\'s what you

want to do is to give a casino management system on the back end that
you can do

your data metrics with. Is that the intention overall? We must fully
wedge ourselves

into SAS standard.

I\'m gonna say SAS /Tito architecture.

Is this web socket thing could it be transacted over SAS as well?

Do you issue these commands over SAS with special commands or special
package of

SAS?

\>\> Actually, SAS is just press 232 on hardware level and it has a
limited number

of commands that we rely on. It has standard description standard
specification how

is it just that\'s actually deployed in casino environments the most
part do they

actually run dedicated serial lines or do they just transport serial
over over

internet and then convert it back highly highly likely they connected to
sub

-converters I assume probably four or eight ports,

serial ports to be converted to Ethernet.

It\'s possible option. Another possible option to install some micro PC.

Sometimes it\'s Windows -based micro -PC within each EGM machine and
work as a player

-tracking system with a separate

graphic

monitors with touch screen placed on each machine. Additionally,

it will enable using player -tracking cards. When you present card to
machine,

it will assign some account, take some money from this account,

withdraw winnings to this card, so on.

Internally, this micro PC has serial line that connects to motherboard
RS232.

the RS232. On the other side, it has Ethernet line that connected to
backoffice to

exchange statistical data, to exchange setup data and so on.

I have a question for you. on the left here, how could we reduce the
hardware

footprint to an absolute minimum?

What I mean by that is manufacturing custom hardware is expensive

and from a supply chain standpoint and everything else. If you can make
a device

that is effectively just software, maybe just a general post that sits
somewhere or

whatever. Even in a back office, it doesn\'t even need to be a fancy
thing, just a

rack mount, or maybe even installs on another computer infrastructure
already. That

would be far more ideal than a lot of custom hardware,

unless you want to get into the hardware manufacturing business. I
actually have to

compliment you on your question, Aaron. I\'m of the same opinion,

100%.

And I believe you will find support with everybody on the team here.

So that\'s a great question to ask.

Yeah, The minimal solution could be implementing some SAS hosts.

You can take a look on the Cloud FlexPay frame.

So instead of installing FlexPay kiosk,

it could be some small piece of hardware that just operates as a source
post and

transfers some data to the cloud. And instead of using Flexport,

we can install Ethernet to serial property.

I\'m not sure 100 % that it could work because we are not just using no
model

connection, but we need to use 9 bits operation.

It\'s quite different.

You\'re using a parity bit, right? Yes, yes. Also,

it\'s not just a parity bit. This bit is used quite abnormal,

according to the specification. hhhh

Tam

I don\'t have an answer.

We need to check. We need to get some sub -converters,

serial to the net, try to connect them to some source as possible later

to answer this question.

I want to add something to the diagram, we forgot, it\'s income
validation and

income validation will develop income into income

validation and

digital wallet

and income validation will stop to exist

and get converted into

validation and wallet, digital wallet, as of June 2025.

And we need

some sort of an app

for managing

the setup and restrictions,

etc.

Probably. I don\'t know where it needs to be connected.

And I also don\'t know how this is connected where, where is this
connected?

By the way, I have no idea.

See this one?

Then in Chrome, highlighting is of cloud,

we will need to have a server -based application. maybe try connecting
it here

somewhere, because it\'s starting here,

so I don\'t know what\... Actually, in this schematic, second and first,

we can connect in -com communication directly to flex plane kiosk,

like this.

Паша, можешь по варианте объяснить, что у нас происходит с физическими
карточками,

они отсутствуют, физических физических грацистов, Они будут карточки
выпускать с

верпуальной. А

зачем нам тогда промежуточный application -sus -host для того,

чтобы иметь возможность зачислять деньги на машину,

снимать деньги с машину, работать с тикетами и все данные,

которые мы получаем, пропускать через\... Так почему? Так почему в
Lexport application

не сможет общаться сразу с cloud -вариантом, пока ты делаешь сейчас в
связи через

девайс.

В варианте cloud мы просто заменяем киоск на какую -то коробочку,

которая нет патч -скрин, нет экранчика. Там тоже самое может быть
application,

который флицкл. Он без девайсов, он без ничего, он только коммуникации.

Он здесь может быть изборточный. А без него мы не сможем работать.
Почему?

Почему флекспорт не может сразу коммуницировать с клаудром? Здесь нет
флекспорта в

этой сее. Он ничего нарисовал.

Не трону.

В самом простом варианте это SAS.

Это не портел. Надо другое что -то нарисовать.

Нет.

Так хорошо, ну что если я присылаю этот конверт? Это девайс?

Это что?

Какая -то кладка.

I don\'t know where to connect in this case where to connect the debit
card

Or maybe it will be digital wallet, I don\'t know.

In short, there is no option to issue physical cards.

In this variant where\... Yes, yes. Yes, there is.

Yes, you can, you can, you can. You can either do digital wallet or a
card.

they feel they actually spoke to income they feel that the transition to
digital

wallet will be slower and

it will take time over 10 years they say

so in this case we need card dispenser either card dispenser either card
dispenser

or we can the cards have no value so we can we can hang the cards on the
wall

and you know validate them you know manually

but I I don\'t know where to connect this

Попеременитый картридер \...хия

\...пот\... \...надо\... In place of physical card,

highly likely we will need to use flex tray with monitor and touch
screen.

We can do it through flex port.

We don\'t have flex port, but it\'s in the schematic.

We use nature of communication with OZ -машин связал с текспортом.

We will need to present one more diagram

with flexport and without flexports.

Well, when we talk about flexport, let\'s define what it is.

Flexport is a combination of an embedded controller

screen sandwiched with the touchscreen,

a separate interface board and

an optical barcode reader and a magnetic card reader.

I\'m maybe a little bit behind on that picture on your conversation for
a minute.

I was drawing a possible other style architecture that truncates a lot
of hardware

potentially.

If you follow to the right, maybe I can explain.

It\'s very simple drawing right now, so it\'s not very well rendered
yet. So just to

start the conversation up at the top is a traditional transport layer to
Ethernet

and back, dripped for serial interfaces. So here it\'s like a gaming
device and it

could be anything like this is common in machine controlling and
industrial controls

and stuff. So you have a serial port, so we\'ll just say not SAS,

but Serial Physical Protocol to Ethernet Frames. It\'s then transmitted
over either a

frame to the serial data is, and it\'s just unwrapped at the other end
and turned

back into serial. This is a two -way transport to normal stuff.
That\'s\--I\'ve seen

that a lot. So this doesn\'t give you anything other than a serial port
at the end,

so you can\'t really, like, use it. You can\'t\--you can\'t use
something with this data

because it\'s private. It\'s encrypted. It\'s got a single endpoint for
stuff. Now,

let\'s go down to this other diagram below. What if\--that\'s kind of
how I\'ll start

this with\--what if instead of decomposing it or recomposing it back
into serial

frames for\--from Ethernet, we could connect it to some sort of server
that unwraps

this to something. So we can then take this and take these serial frames
and send

them to wherever we would like. So for example, internally, the very
first thing we

want to do is to make sure we don\'t lose the connection to the existing
serial

stuff so you can see that if we follow this line, this Ethernet if they
contain

serial data, go to a unwrapper, they go to a serial framemux,

which is just like literally another thing to route the traffic
correctly,

and then goes back to the same Ethernet serial adapter again to wherever
it may go.

So these things kind of just look like network switches.

So if we look at these pictures here, here\'s like what one of them
would look like

on the EGM or on the device out on the floor side and this is kind of
what they

look like on the server side inside the network, right? So you can
imagine this

thing is this, and these things are here.

So, here\'s where the magic happens, is that this big box here is
actually just

a\--it\'s a container host of some kind or a virtual machine host of
some kind. We\'ll

call it a container host. Inside of here, you can build virtual server
adapters for

all this stuff. So if you can decompose the protocol that is right here
in this

line right here, you can build as many adapter things as you want and
you can

connect it to whatever you want. So if you wanted to take all this
serial traffic,

turn it back into SAS, wire it to a SAS server, have the SAS server push
it to

an upstream internet service which is your database or whatever,

fine. it\'s all software, it\'s just containers. If you wanted to push
to some other

management host to, like, you know, maybe a local accounting server
right here,

you have this, and it\'s all internally. If you want to use your, maybe
other type

of serial transport that\'s not SAS or something, you could have another
adapter

routed for that. But basically, you just have some sort of interframe,
of interface

mixer to be able to drive the things to different places you want.

And this puts this all on a single virtual machine post instead. So if
you could

get away with identifying the protocol and use commodity hardware for
the interface

out of the field side, you can just literally write a virtual server
adapter driver

thing that is running in a host and is deployable at all times inside of
the

container.

This follows a architecture for a lot of more modern multi -function
devices.

A lot of things nowadays use this containerized approach like this. If
you look

under the hood, even Cisco unified other companies do this now,

internal containers.

Am I way off base on this, or does this have any merit as a potential
alternative

to a hardware heavy approach?

I think we are looking for the simplest possible solution.

Ideally, if we can use some components that we can directly buy without
developing

something.

Я не понимал ответы, извините.

Паша, можно опять сказать?

что мы могли предоставить максимально простое и масштабируемое решение.

Максимально простое в том плане, что мы можем что -то купить готовое,
например,

Converter Serial to Ethernet, используя стандартный Ethernet connection,

при этом написав свой са -спост,

мы можем общаться со всеми машинами.

Конечно, да, мы можем разработать какое -то более сложное решение,

развести свои платы,

мы можем использовать flexport.

I just grabbed a picture from their website which is just kind of
explaining

different architectures that they support and it\'s just a way to kind
of maybe think

about how this is done. So So these are really\--I had to deal with
these way back

in the day when I was in retail\--proper retail engineering. So we used
scanners,

so like a phone sled scanner, and that thing connected to a register
which then

connected to a serial to Ethernet thing and then it was pretty common to
do this

even back then and I\--that was for managing retail transactions So I
think it is

sufficiently robust enough to be able to manage transactions this way as
well.

So just to grab this as well, this has some other architecture layouts
for how this

could possibly look as well.

So you can see what\--if they\'re using TCP, you know, you\'ve got
retries on the TCP

side. It\'s not UDP. And then if you\'ve also got\--the SAS have a
robustness to it.

Does it\--is there a 2A acknowledgement on SAS that the command has been
received?

Does that work that way? I don\'t know anything about SAS.

\>\> So this is two direction protocols for this particular direction?

\>\> If I send a packet over RS485 with SAS command or SAS message and I
am

expecting something back from that SAS message, does the SAS or need to
I need to

send it but it\'s a very important message does the thing that
originated in the

message give a confirmation and acknowledgement that it was received yes
okay okay

and then if it times out it will it is robust enough to resend that
message is

that right yes or is out according to the stack configuration.

\>\> It\'s up to SassPost to make additional requests if it requires.

\>\> But you do have a logic layer that will resend if you wanted to
build that

into the\-- okay, so then if\--so imagine that\'s the SassLayer, then
we\'re just

standing on another layer which is Ethernet TCP. So TCP is going to
retry all the

time hammering against something to make sure it goes to the other end,
wire the Wi

-Fi or whatever. And then you have multiple layers of redundancy to make
sure that

traffic gets to its destination.

And this way there\'s a kind of a\--maybe this already exists with
casinos but I

would imagine they would rather run one infrastructure wiring set up
only or maybe

not and make it all Wi -Fi or have an option to I know that people
mentioned the

passive Wi -Fi as a nightmare but I don\'t know maybe it is maybe it
isn\'t I\'m not

my here to judge but certainly only needing to wire Ethernet cables as
opposed to

both special serial interfaces and Ethernet makes a ton of sense and if
we never

have to give them anything other than a little converter box and
everything else is

orchestrated on the other end, that would be pretty fantastic from a
user, customer

acceptance perspective.

So then, when you have all the devices here, so like I\'m looking at the
card

reader or the other kind of transactional, you know,

player interface things, all of them are abstracted over ethernet to
remote services

endpoint for things. The other thing that\'s kind of interesting too is
that assuming

that you\--if you go back to the service architecture, there is really
little reason

why this whole setup here, if configured properly,

needs to exist there. This also, I believe could be cloud -based as
well.

So you could just kind of deploy that whole thing on cloud and then just
make sure

that the traffic here from the frames goes off into the right spot.

So maybe instead of having a huge heavy post, you just literally give
them a super

lightweight little thing that just collects the traffic and sends it off
to where it

needs to go. Just like a little baby router of some kind. Maybe a
specific

container or whatever. I\'m just thinking about different applications
where maybe you

want to host all this and run this infrastructure on cloud -based and so
now you

have everything on JBL infrastructure and they just pay you an extra
bill. This is

a way to kind of turn everything into casino as a service effectively?

Actually, conversion from SAS to Cloud will not work on Azure,

because it has time limitation.

\[INAUDIBLE\]

\[INTERPOSING VOICES\] Could you do anything with Buffer locally, or
something like

that, or some sort of part of the\-- \>\> Yeah, so this\--this cloud can
implement a

resistance location. \>\> Sure. So\--so you could have potentially just
a super stripped

down SAS helper, I guess. I don\'t know what the right way to call it.

That kind of just buffers commands and then lets them go off to where
they need to

go with more\--in areas\--situations where there\'s more latency. Or
maybe it just

doesn\'t matter. Just put it in a container and whatever. Who cares? I
mean, I would

say I\'m not going to say Raspberry Pi level sort of computer is
sufficient,

but probably not much more than that is actually necessary to host a
bunch of these

containers to do stuff. Like, it could be a fairly small architecture of
physical

hardware for this. It\'s more about storage and interface and everything
else.

Or, you know, another thing to consider is that you could take this
entire

architecture, if this is in this box locally, and make constant backup
to the cloud.

You could also use ways to give plus one services for customers to say,

\"If you buy into this architecture, we do these things for you.\" Like,
you can

reload this configuration or you could deploy it automatically to other
sites. You

could configure and control it remotely, that kind of thing. Because I
would imagine

that, like, if you wanted to update containers in here, which literally
do everything

that we\'re talking about on the stuff on the left here from a
configuration between

either this box in this cloud or the other bit, you have now the ability
to push

down remote updates to containers and all sorts of things. This is
outside of the

gaming space. This is more in the casino space or you let the casino run
the

thing. Like, I just\--I don\'t know where the rules stop with, like,
allowing access

to that or managing it or whatever, but I could see that tension being
valuable.

So like if I go back to the diagram on the left here where it says flex
pay with

integrated SAS,

so instead of having flex port converters here,

You could kind of imagine

Let\'s uh,

let\'s see here Let\'s take one of these machines here If we put it over
here

If we call this Lexport

See here,

so let\'s just imagine flexport was ethernet only just for a minute.
Okay So then

this means that a minimum Flexport ethernet only

would always go back to this point over here and So you could have these
as

capabilities that you can turn on inside of your container and you
license them or

or give them as a pay per per service thing you turn them on so if you
buy the

flex port package you get flex port and the minimums for for these
things and as

soon as whatever where it needs to connect to an existing thing, hand
off SAS back

to whatever, or run some other internal accounting commands or
architecture.

And then if you buy into it more, then you can turn on the other pieces
of this

environment here to the point of being able to support a full casino
from this

virtual environment like this.

But don\'t take me as, you know, not, I\'m not trying to discard what
you\'ve drawn

over here. I\'m just trying to present something that is a possible
approach to a

lower hardware investment.

Depending on the way this is laid out, if you have like PCI zone
requirements,

so if you\'ve got PAN or other type of payment information or things
like that,

you may be able to even deploy these inside of that space or have
isolation

networks for things like internally in a container host you could define
multiple

networks and some of those networks could be determined deemed PCI zone
space. So,

you know, storing, storing payment stuff, information or tokenizing
payment information

or whatever. I don\'t know how you guys do all that internally, But I
just know

that you could kind of lay that out that way.

If you look at, like, Stripe, or what\'s the other payment terminal
stuff for\--

\[INAUDIBLE\]

So clover, stripe, square. You see those,

right? They\'re kind of

clover. Let\'s find you a picture.

So

Here\'s Clover looks like this just

payment terminal right, but the point is is that 100 % wireless point of
sales

device Everything on this is designed to run to cloud infrastructure on
the other

end It\'s like the Internet of Things deal that\'s set up and you pay a
you pay

rent on it, right? So you can imagine a retail store with 20 of these
devices is

35 times 25 devices a month for running this, and that\'s an awesome
amount of thing

where they don\'t have to put any hardware infrastructure. They\'re
basically

down\--deconverted all of the hardware infrastructure into a monthly
payment for driving

this.

Clover, So Striped is kind of the same way. So if you look at what

Striped\'s doing in

the region here,

this is all, you know, I\'m just grabbing stuff that kind of is in the
same theme

of this kind of thing, which is to give somebody somebody managed
infrastructure for

this. It\'s only when you get into really big retail that they tend to
run their

entire own stack of custom things or really build it. And when you think
about

that, that\'s like super vertical oriented. So I would say like very
large casinos

and things are gonna run their own, whatever anyway. - I just wanna make
a couple

of corrections. First of all, this meeting needs to end in about five
minutes.

Number two, we are sandwiched between two established methodologies.

One is driven by the retail sector, which is income settled products.

And I suggest you guys, meaning Dima, Andrei,

Sergei, Pavel, you need to go and research income products.

machine manufacturers, and they are SaaS and Tito oriented. So the two
eventually

will merge into one service and whoever will find the solution,

the cheapest solution for a location and an operator will win.

So because I\'d like to finish the meeting in the next two minutes, I
would like to

give you an opportunity today and tomorrow to go and study both items
and revise

the schematic and the evolution of the schematic from where we need to
be today,

meaning Kiosk and Tito and SAS versus future,

digital wallet and cloud solution.

And with your permission, I would like to schedule another meeting,

if you guys could look at your calendars, for either Thursday or Friday
of this

week. I know that Thursday Aaron will be busy in a meeting from 12 .30
to,

actually I\'m going to move it a little bit further. So Thursday is not
preferable,

But Friday, I would like to meet on the same subject and go through the
evolution.

When we go through the evolution, I would like you guys, you meaning
Dima, Andrei,

Sergei, Pavel, to make the most progress in studying both items.

Will Friday be okay with you okay so Friday Aaron you okay on Friday
yeah what

time again well can I do it at seven o \'clock your time sure okay

how much time do we need an hour two and an hour, if that\'s sufficient.

Okay,

I need to give it a proper name,

What should I call it?

What do you guys suggest architecture of SQL all up visualization

When the diagram I drew, it doesn\'t even show SQL, it just makes a
cloud picture

at the end. I do that because I think the SQL part is pretty well
solved.

It\'s architecture for SQL hosting and all that stuff. There\'s a ton of
design

patterns that are just pick one off the shelf and choose one. They are
all straight

forward.

This is the hard part right here. So what do you get to me?

I\'m drawing blank. I would say local

infrastructure to application host environments.

It\'s kind of how I would term this,

but I don\'t know how that translates. Okay, so this

invitation has been sent and I\'ll see you guys on Friday. That means
that you need

to work for Friday. Friday is the showtime for you guys.

Thank you very much.
