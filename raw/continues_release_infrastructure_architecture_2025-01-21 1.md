---
tags:
  - meeting
  - continuous-deployment
  - quality-assurance
  - val
  - aaron
  - github
---

**Transcript**

January 21, 2025, 1:02PM

Val Levitan** started transcription

Val Levitan** 0:09\
OK.

Jason Welco** 0:10\
I am.

Val Levitan** 0:10\
So perhaps I can start the meeting.\
Please allow me to be.\
To express myself from a non engineering perspective.\
We can get into engineering aspects a little bit later, but let me just
at least for myself, formalize my thinking on the subject.\
And the subject is.\
Continues deployment.\
Versus.\
Some sort of.\
Testing application.\
That.\
Can be used by our QA department.\
Or.\
Gli as a standalone tool.\
So I think I\'m somewhat clear on the continuous deployment from an
administrative standpoint of you, but let me just go over it.\
So in JIRA we will have projects split into and I\'m being a little bit
mechanical I understand this.\
Injera will have a project split into features and stories.\
From what I understood, features represent.\
A branch.\
In git.\
Stories are committed into a branch. When a story is committed, we
usually.\
Deploy. We will deploy some sort of unit testing.\
But by a developer himself, and when a feature branch then merged into.\
What do you call it?\
Master branch or?\
Trunk. I don\'t know.\
It at that point will probably deploy some sort of.

Aaron Bockelie** 2:24\
It\'s close.

Val Levitan** 2:32\
Integration tests.\
The integration tests are usually written or preferably written by.\
A non developer perhaps?\
AQA Department it is written ahead of the integration itself, which?\
During integration may create some sort of I\'m gonna.\
Use the word conflict of integration where.\
Possible.\
Programming deficiencies or?\
Testing deficiencies surfaced and.\
They reconciled between the developer and a person who wrote the
integration testing.\
That\'s how I primitively from an administrative point, visualize the
process of continuous deployment and integrate and continuous
integration.\
Right or wrong, this is what\'s in my mind.\
Let me regurgitate.\
Or express from administrative point how I visualize?\
A.\
Tool that can test.\
A complete product by let\'s call it GLI.\
And this is a new kind of a new development for me.\
So we need to create some sort of.\
A shell around this tool.\
That will house the actual product within it.\
As well as.\
Software and might be hardware hooks.\
For some sort of a test harness.\
There should be additional application that hooks to a harness.\
With a bunch of.\
Executable instructions.\
That can.\
Get inside the product.\
And push.\
And pull certain things. They could either be software or hardware
things.\
And it will have a display and on that display it will show results,
display computer or something.\
It\'s kind of a, a a boxy envelope.\
I don\'t know of anything.\
I don\'t know what else is in there.\
And that is going to be given or shipped or downloaded by GLI or used in
our own QA.\
So.\
What is it that I do not understand or not clearly understand? Or what
needs a correction?

Jason Welco** 5:56\
I think that\'s.\
I.\
I don\'t.\
I think everything in there is mostly accurate in terms of describing,
you know you have feature and and some use cases.\
And I\'m somewhat familiar with that \'cause we.\
In, in my experience.\
You know, we we did the deployment, we did the.\
Automating the deployment internally and then the next step on that was
to and it wasn\'t technically much different, it would just.\
Goi or whoever the ITL was, it would just be a remote host for us where
we were running it and there there are certain technical solutions to to
make that happen.\
Aaron, do you?\
I.\
I think this is.\
All.\
I understood what what Val was expressing I claim.

Aaron Bockelie** 7:00\
Yeah, I think that\'s close.\
I\'m actually just like opened a Miro. I was thinking about might be
helpful to just kind of sketch out what that looks like.

Jason Welco** 7:09\
Oh yeah, no, I actually I have. If I can share, I I\'ve actually got
something.\
I\'ve already done that.\
I rather than Draw Something new.\
Be able to see this.

Aaron Bockelie** 7:23\
Yeah.

Jason Welco** 7:24\
Alright, So what?\
I\'m just gonna walk through. What?\
What Val just says I have a developer who\'s going to commit some code
the use case.\
You\'re describing is not really the commit. It will be at some point.\
We\'re going to do the pull request.\
And in parallel to that and in parallel to the the shift lefting in
parallel to the developer coding, the tester is going to be laying out
the.\
The the test steps and some magic and a miracle happens and we can do
this automatically and that\'s what Anton and I are working on.\
And then going on to so you know in bit bit bucket builds kicked off, it
gets built, the binaries are magically delivered and now we\'ve got a
bunch of binaries.\
And now we have to go deploy them.\
So that\'s kind of what this box over here will will need to do some
work to magically deploy stuff.\
I split that out into three different areas and there\'s products to do
that detail and I guess we don\'t cover it.\
The only thing is I would do a little commercial that we also have to.\
Our code is important, but the what it runs on top of is also important
in terms of the infrastructure, right?\
So your operating system.\
How much memory do you have?\
All that other kind of stuff.\
So that\'s a end. All in that digression.\
And then we need to deploy it to different places. I started off. This
was only one box and then I just kept adding on I go. Oh, I need to a
developer\'s going to want to run it on his desktop.\
Will not want to pay for external hosting, so we\'ll we\'ll put it on on
some servers that are managed, we\'ve got the actual physical.\
EGM cabinets that we can deploy to.\
We might want to use cloud hosting, right?\
So I\'m a fan and advocate of that, but don\'t have to use it.\
And like what we\'re doing.\
But we\'re actually running the automated test.\
What we\'re what we\'re prototyping, we\'re actually running in the
context of Bitbucket.\
So when you build it, you\'ve already got a machine running.\
We\'re effectively gonna want to deploy it there and run it, and then
when you just mentioned that says, hey, I and I didn\'t add it here. So
I need to have a remote.\
For GLI or or anybody else, I need to have a remote.\
A remote host.\
You know, in in this things.

Val Levitan** 10:10\
Why do you need a remote host? If it\'s a cloud hosting?

Jason Welco** 10:10\
And.\
No, Benita, you were talking about the GLI use case.

Val Levitan** 10:19\
But wouldn\'t jli be able to use cloud hosting?\
For that harness.

Jason Welco** 10:27\
I think of the EGM the the I have to deploy to onto the EGM itself.

Val Levitan** 10:31\
But GLI has has an EGM in their laboratory.

Jason Welco** 10:36\
Yes, but we need to get.\
We need to get the software on to whatever they\'re testing and the test
tools.\
Cause those may change as well. I mean whatever it is, right?\
So instead of running it in Toronto or Minsk, whatever we\'re running is
running somewhere else.

Val Levitan** 10:55\
Well.\
The actual essence of this is not to have a physical location of this
tool, because I, in particularly importantly don\'t wanna have it in
Minsk.\
Because Minsk is as volatile as anything else.\
And I\'m pulling a lot of controls out of Minsk.\
So the last thing that I want is further entrenchment, physical
entrenchment in Minsk.

Jason Welco** 11:30\
Yeah, my point on the picture is that.\
It it there are many different, there are several different places.

Val Levitan** 11:38\
But it\'s but it\'s but but it\'s, but it\'s confusing.

Jason Welco** 11:38\
It it it could or would run.

Val Levitan** 11:43\
Because it\'s by creating more.\
Alternatives or more variations?\
It requires more programming and it doesn\'t satisfy the management
direction.\
So why are we doing it?

Jason Welco** 12:02\
Well, you\'re gonna have different use cases, right? So.\
I\'m just because I draw the box there that that doesn\'t mean we\'re
obligated to do it.\
I\'m just trying to express.\
That the continuous deployment from a technical perspective can get
you.\
You\'ve got different places where you may want it to run.\
You may not want.

Val Levitan** 12:22\
But somebody else will look at this picture and take it seriously and
eventually it will get to an architecture to an architect who\'s gonna
say, oh, I have to provide for it.\
So I have to write a bunch of layers to satisfy this. Where in
particularly I\'m stating right up front that I do not want it.\
So what are we doing?

Aaron Bockelie** 12:53\
I think.\
An easy way to simplify is to remove.\
Obvious physical hosts and things like that.\
Physical locations. These can be.\
All of this can be ran as cloud infrastructure. You can have a cloud
environment that this runs in.\
You don\'t even have to run it locally.\
I think that we just need to make sure that that\'s called out
appropriately.

Jason Welco** 13:19\
Right. But from an architecture point of view?\
So let\'s just say first of all.\
Right now, the easiest place we\'re going to go put it or a starting
place is we\'re going to the bit bucket. Host is a place is a convenient
place to do it.\
We may want not want to continue that because.\
We\'re going to we get billed by the minute at some point.\
I don\'t know exactly what the cost dynamics are.\
I mean, Aaron, the the thing when you\'re when you\'re designing a
continuous deployment solution, you need to be you need to.\
Figure out where you\'re you.\
You might be running this cause Val I\'m I\'m I\'m almost certain we\'re
gonna be wanting to run it in more than one place.

Aaron Bockelie** 14:06\
Right.\
Well, I I think it\'s to me it\'s seems really simple. Amazon has
elastic compute.\
Azure has their has Azure service like. There\'s many ways to to run
service builder runners or however we\'d like if we wanted to privately
run. We\'re still paying for cloud services by the minute for that
machine to host and run, but you know that these build platforms charge.

Jason Welco** 14:35\
Mm hmm.

Aaron Bockelie** 14:37\
A premium for their integrated runners and.

Jason Welco** 14:41\
Right. So so you get my point though, Aaron, as I, I today we\'re you
know we\'re running in bit bucket.

Aaron Bockelie** 14:41\
That\'s how to make a lot of money.\
So decide it makes more sense, yeah.

Jason Welco** 14:48\
We\'re not. You know, there\'s no problem.\
We\'re running in Bitbucket, but that may not be the only place we would
run it.

Aaron Bockelie** 14:54\
Yeah.

Jason Welco** 14:55\
And and in terms of the technical solution, Val, I don\'t. I I don\'t
think we should get hung up on this because I think our technical
approach is we\'re probably going to be looking at using containers.\
And in which case it\'s it\'s kind of mostly the same.\
Whether it runs on a desktop or you\'re running it on your own servers,
or you\'re running it in AWS or Microsoft or Google or or wherever it
is, but you have to be.\
Anyway, I can certainly simplify this. I I think I\'m I\'m making a
technical point here, but it\'s also a functional point.\
But I think we\'re, I think we\'re down a rabbit hole.

Val Levitan** 15:39\
I I am a huge supporter of Mvps and simplification.\
I would rather go through another revision of a tool.\
That is more advanced than over designing something we do not have.\
The mental capacity.\
We don\'t have administrational capacity we don\'t have.\
We are very tiny small company.\
That is trying to get things done.\
A large architecture, a large design.\
Will bury us.

Jason Welco** 16:17\
Yeah, I yeah, this isn\'t a statement. I I am not making a statement
that we have to deploy to more than one of these. We we could decide the
only place we\'re gonna run it is on an EGM cabinet.

Val Levitan** 16:18\
If we won\'t be able to get off the ground.\
The architecture, the schematic diagram will lead to a complex
architecture.

Jason Welco** 16:36\
OK.

Aaron Bockelie** 16:38\
But I see this is the to me for when I\'m looking at this graph.\
This is the end to end.\
This is everything from the development cycle to the deployment cycles.
What I\'m seeing here.

Val Levitan** 16:51\
It also it it also.\
Addresses the the two separate subjects that I\'m trying to separate.\
One is continuous deployment.\
And another one is the tool.\
That we\'re trying to design for QA that that that\'s the complete
product and I\'m trying to separate.\
I\'m trying to get to have a logical separation between the two things.\
I know that we we kind of discussing two things, but it\'s important to
arrive to a complete separation of what is it that we\'re discussing?
Are we working on a tool or are we discussing and implementing
continuous integration?\
Or continuous deployment.

Aaron Bockelie** 17:38\
I I put the screenshot up here or picture as a reminder that I believe
strongly that we should be able to deploy a completely.\
Well, a completely portable test suite or test environment. We should be
able to grab from GitHub the entire tool set and everything that AQA
engineer needs to start working to make sure that the running tests and
they\'re validating locally if they need to.\
So just the same as we have runners that can run on a development
pipeline, I believe that we should be able to completely grab the
correct Git repos given the correct starting point and pull in the
entire test suite and all pieces needed to do testing ad HO.\
Off off, you know.

Jason Welco** 18:30\
Yeah, well.\
And I think that\'s what I\'m that.

Aaron Bockelie** 18:34\
So.

Val Levitan** 18:35\
Look, look, look, I\'m probably not coming across very clearly.\
So treat it, treat it, treat it as an order.

Aaron Bockelie** 18:39\
No, I get it.

Val Levitan** 18:45\
I am not capable.\
I\'m not an engineer.\
I am not capable of understanding smart people.\
I am very primitive and stupid.\
So please, it\'s OK.\
Treat me as an idiot. I\'m OK with that. I am not capable of speaking
about two things at the same time.\
So let\'s split our efforts into continuous deployment and integration
as one effort.\
And let\'s create an effort that deals with the tool.\
So I could visually understand this.\
I\'m not capable of.\
I don\'t have the taxonomy, I don\'t have the terms.\
I don\'t have the experience.\
But logically I can comprehend simple schematic diagrams.\
Within those schematic diagrams, please.\
Only reflect the very most important Mvps, without which the thing
cannot function. If it can function without something, remove that block
because it it.\
It\'s another blog that I need to comprehend and I\'m trying to
comprehend as little as little as possible because it\'s a learning
curve for me.\
So please help me.\
Be a useful part of the decision making process.\
I\'m not capable of functioning on your level.

Anton Leshkevich** 20:26\
I guess for the.

Val Levitan** 20:26\
So simplify this thing for me.

Jason Welco** 20:29\
OK so.\
Would it then?\
So you\'re you.\
You don\'t like all these boxes, right?\
So you think too many, right?

Val Levitan** 20:36\
I just leave.\
Just leave the very few boxes necessary for this thing to function.

Jason Welco** 20:40\
Yeah, yeah.\
Alright, so would it.\
Would it be helpful in this case if I were to?\
So you\'ve got.

Val Levitan** 20:53\
Where where, where is the tool and where is the continuous integration
separated both.

Jason Welco** 21:00\
OK.\
So that\'s well I did.\
I was certainly attempting to do that right.\
So I\'ve got continuous deployment is split out into its own box here
and we\'re really not spending much effort today.\
On on this it is a big part of the solution.\
That\'s why I was trying.\
That\'s why I wanted it here \'cause. You can\'t test it until you can
deploy it.

Val Levitan** 21:26\
OK.

Jason Welco** 21:27\
Right. So especially automated, right?\
There\'s no it\'s. You\'re just gonna create, you know, a whole set of
other issues you\'re gonna have to address.\
So this continuous deployment happens for for a reason.\
So we.\
Our current thinking or hope it\'s our thinking, hope.\
Claim is that we\'re thinking that we can hope because this environment,
the target environment is eventually on the.\
EGM.\
That\'s a very narrow in scope problem.\
We only have a small number of configurations.\
Alright, maybe you got a single monitor.\
Maybe you got dual monitor.\
There are some variations.\
You will have more over time, but right now it\'s it\'s.\
It\'s a fairly narrow target. We don\'t have a lot of variety like you
would other things. Now over time, we certainly we have the EGM. You can
also think of another environment is your online game.\
Eventually, that\'s not. I\'m not really spending time thinking about
that, but that\'s another way of thinking that I\'m doing continuous
deployment but.\
I got I may have different environments. I have to get to in your
product line.\
Right. You you may have some products that run on Windows.\
You may have some products that run on Linux as an example.\
The tool itself is in this middle.\
It\'s in this middle section, so the tool I\'m representing.\
More representing over here in terms of.

Val Levitan** 23:11\
OK.\
Can you please can you please frame it and call it a stand alone tool.

Jason Welco** 23:11\
Hi.\
Guess so.

Val Levitan** 23:24\
Just to just to give you just to give.

Jason Welco** 23:27\
I haven\'t thought about it, but I hear you.

Val Levitan** 23:31\
Well, just to give you just to give you a case in point up until you
told me that this is your stand alone tool, I actually thought that this
is part of continuous integration and where the machine is and all these
blocks are. This is what I thought.\
The tool is.\
So this is just to show you how primitive my thinking is.\
I don\'t know these things.

Jason Welco** 23:57\
OK.

Anton Leshkevich** 23:57\
Maybe just to kind of simplify the whole process and moving in kind of
in iterations, adapting the MVP approach, we can start from the
deployment procedure and trim out all the unnecessary features for MVM.\
Let\'s start with simple.\
Git triggers build.

Val Levitan** 24:19\
Can you?\
Can you play?\
Can you?\
Can you paint it in blue or in in yellow?\
Just paint those \*\*\* \*\*\*\* things in a different color.

Anton Leshkevich** 24:27\
Yeah.\
Uh, I think it\'s easier for me to kinda.\
June.

Jason Welco** 24:54\
Oops, why did that not?

Anton Leshkevich** 25:16\
If you pay attention to the left bottom corner.\
This is what a very very basic setup would look like, only containing
continuous integration and delivery.\
And this is a very essential part on which all the other parts are
built.\
So probably we should be starting with with something like this we need
to set up a a pipeline that builds and deploys software.

Aaron Bockelie** 25:35\
Replay.

Anton Leshkevich** 25:45\
From there we can add JIRA and X-ray support on.\
And having the deploy configured, we will be able to kinda run to design
and run automated tests.\
So I would say this is a very essential step and should be #1.

Val Levitan** 26:08\
So this is this describes.\
Continues deployment and integration process.\
Am I correct?\
This is the basic the most primitive things for continuous integration.
OK, I understand this.

Anton Leshkevich** 26:20\
Yes, very primitive. Very basic, yes.

Val Levitan** 26:27\
OK.\
Show me where is the most primitive elements of a tool stand alone
tool.\
Similarly to what you did with the yellow blocks, show me those the most
primitive, the most, the the most basic things that requires for the
tool.\
You know really simplicity 101.\
Take your time.

Anton Leshkevich** 26:57\
Mm hmm.

Jason Welco** 26:59\
Yeah. So.\
What I did here and now this may not match.\
The rows and columns you want to see, so I basically.\
These three blocks here.\
Are three the three basic things you do with a test tool?\
I have a user interface and I want to click the login button.\
So I call that you.

Val Levitan** 27:27\
User user user interface is not the MVP.

Jason Welco** 27:34\
If I\'m going to do a test, most of our tests are going to involve
clicking the I\'m I\'m going to make a wager, right?\
I I need to configure the the game.

Val Levitan** 27:43\
Let\'s let\'s have any.\
Let\'s have any interface. It doesn\'t have to be fancy.\
Something where a more advanced developer or tester could could use.

Jason Welco** 27:55\
I\'m I\'m trying to say that I need.\
I\'m trying to write a test step.\
My test step falls in the category that I want to pretend to be the
player\'s finger, and I want to select the one cent denomination and
wager 30.

Val Levitan** 28:11\
The the 1st test the the the 1st test that GLI identified as a save as a
time saver is the math test.\
So if I\'m introducing such some sort of.\
A box that will save me money.\
My first thing will be to test math.\
Show me the most primitive blocks to test math.

Jason Welco** 28:44\
Alright so.\
Alright, it\'ll it? Yeah, so.

Anton Leshkevich** 28:52\
Aaron, Jason, let me try and you will comment if I\'m wrong, OK.\
So.\
In the right bottom corner, could you please move your?\
Yeah, yeah, yeah.\
Those are three three essential blogs that.\
Any any testing tool should have.\
Oh, I\'m sorry.\
I just duplicated author ring.

Val Levitan** 29:17\
Where does it show?\
Show me how it connects.\
Where where does it?\
Where does it connect?

Anton Leshkevich** 29:24\
Yeah, and it\'s.\
Let me just finish for a second.\
So any any tool should have three these three essential blocks.

Val Levitan** 29:31\
Go ahead.

Anton Leshkevich** 29:36\
It should manage your test cases and you should and it should provide
ability to author them.\
I don\'t write scripts in language or with building blocks and or
something like that, and it should run your test cases. So basically
once.\
Your.\
Once your applications is deployed, you can.\
Go to your testing tool.\
Get repository of your test or test test sets and invoke the test runner
to run those tests against freshly deployed environment.\
Fresh, freshly deployed, let\'s say machine or any other environment
where it is deployed and once it done it will. The test runner will give
you test execution results that you can further analyze.\
Analyze and that\'s an MVP, but for the future we can take the execution
results and upload it back to X-ray or JIRA on or some other project
management tool or whatever.

Val Levitan** 30:38\
OK, OK.\
Aaron, do you understand this?\
You were not.

Aaron Bockelie** 30:45\
I mean I.

Val Levitan** 30:46\
You were not listening, can you?\
Can you?\
I don\'t need another picture please.

Aaron Bockelie** 30:50\
I\'m not drawing more pictures for you.

Val Levitan** 30:50\
I\'m. I\'m up to here.\
I\'m already tired of it.

Aaron Bockelie** 30:53\
I\'m. I\'m I\'m.

Val Levitan** 30:53\
I\'m just going to cancel the whole \*\*\*\*\*\*\* thing.

Aaron Bockelie** 30:56\
I\'m drawing pictures for myself right now to try to simplify this a
little bit.

Val Levitan** 30:59\
OK.\
Hold on.\
How much time do you need to draw your pictures?

Aaron Bockelie** 31:06\
So I\'m taking a look at what Jason\'s done here.\
And my understanding is is that I see this is the whole and not as a
bunch of individual pieces. One cannot exist without the others. The way
I see this.

Val Levitan** 31:19\
I beg the difference.

Aaron Bockelie** 31:21\
So I can.

Val Levitan** 31:21\
Because what?\
What? What Anton is showing, it could exist without a bunch of other
things.\
All I need to do is to upgrade.\
My QA department.

Aaron Bockelie** 31:34\
So I see this a little differently.\
I see the QA department has to be upgraded, but also the developers need
to become QA engineers too.

Val Levitan** 31:45\
That\'s fine, but but the the bottom line is my QA department may or may
not be adequate to run the primitive architecture that Anton is
proposing.

Aaron Bockelie** 31:58\
I believe that we have.\
Let\'s just imagine we had a couple environments, so we have a
development environment.\
We have probably a test environment.\
We probably have a staging environment and we probably have a deployment
environment, right?\
Let\'s just say 4 environments for a minute.

Val Levitan** 32:19\
I understand this.

Aaron Bockelie** 32:19\
And.\
What I\'m imagining is, is that in a development environment we have
very low level testing going on.\
We have unit tests so I can run.\
I can take a piece of code in abstract and run unit tests against it.\
It doesn\'t even run the code, it just sort of the tests interact with
the libraries and load it and run unit tests.\
We can had coverage tests so we can see which parts of our code are
actually tested, because there may be functions or or implementations.\
Whatever depends on the language that aren\'t tested or not.\
So we wanna make sure we have good coverage.\
And then we have.

Val Levitan** 32:59\
But it\'s in the it\'s in the future.

Aaron Bockelie** 33:02\
No, this is now we have to have this now.

Val Levitan** 33:04\
But I cannot have everything like this.\
I cannot have everything at once.\
I need to start somewhere.

Aaron Bockelie** 33:09\
But I\'m telling you, this stuff already happens right now.\
This is already what I\'m telling you happens right now in SVN, outside
of Git or anything.\
Developers are writing unit tests.\
Developers are doing some code coverage tests and developers are doing
static analysis testing.\
So this is happening right now already.\
I think that what\'s different now is when we start talking about an an
environment testing.\
So when we\'re when we got a test environment.\
We need to. This is where the QA engineering team has to level up a
bit.\
We need to have.\
Automated integration testing, not manual integration testing.\
We need to have automated API endpoint testing because I know that our
tools have API endpoints on them.\
We need to have automated component testing and we need automated
contract testing.\
Contracts is not the legal version of contract.\
Contract testing is where we\'re making sure that the code is doing
what\'s expected to do from a feature perspective or from.\
Customer perspective.

Val Levitan** 34:26\
Is it that can it?\
Can it all be implemented overnight?

Aaron Bockelie** 34:30\
It has to be written in code and it cannot be written overnight.

Val Levitan** 34:33\
OK.\
Hold on. Hold on. Hold on, hold on.\
Can it all be implemented overnight?

Aaron Bockelie** 34:38\
Absolutely not.

Val Levitan** 34:40\
Good.\
What is step #1?

Aaron Bockelie** 34:45\
Step number one is getting people to understand that there\'s a testing
environment that must be controlled.

Val Levitan** 34:51\
Yes. OK. What what from a code perspective, what is test #1?

Aaron Bockelie** 34:57\
Test #1 is getting AQA engineer to open up vs code and run the test
themselves.

Val Levitan** 35:06\
Show me on the diagram.\
Where is it?

Aaron Bockelie** 35:08\
I don\'t know.

Jason Welco** 35:21\
So when you when you\'re saying VS code is that just like if I were to
have, if I were to have Python tests or something like that?

Aaron Bockelie** 35:26\
I\'m just picking up.\
Yeah, I\'m picking a development environment because I just don\'t see
QA testers opening up a terminal and using a bunch of git commands and
running it all by hand.\
They\'re gonna be opening a A.\
They\'re gonna be cloning an environment or cloning.\
A code repository and somebody will have already written a bunch of
batch scripts or some sort of scripting thing to be able to kick off all
the tests, and they\'re gonna look and see what happens.

Jason Welco** 35:56\
Right. So I mean the use case you want the tester to say, I want to test
this feature on this configuration in this environment, right?

Aaron Bockelie** 36:07\
Yeah, they should be able to do that manually before we do it
automatically start.\
Walk before we run, right?\
Obvious. Obviously, we all also call these same tests in our automation
when we run our in our runners and we\'re doing continuous deployment or
continuous, I should say continuous delivery of work. Obviously these
same tests are ran in succession and and in bulk to be able to commit.\
Code but testers should be able to run it individually too, right?\
Because the the nature of developing the tests is that we hire
developing code.\
To that makes those tests happen.

Val Levitan** 36:46\
We we need to stop this conversation.\
What?\
So the here\'s here\'s an organization.\
I know everybody knows that we cannot implement.\
Things at once.\
But we want to implement.\
Something that is that that is.\
Most.\
Basic and the easiest thing that could.\
Would be considered as a starting point on what we can build.\
What is it?

Jason Welco** 37:31\
So in my little confluence page, this is what I it\'s debatable, right?\
So I I took a crack at it.\
I said these are the MVP features.\
In this little bullet form, the last bullet is actually what Aaron
actually just mentioned recently is interesting.\
So.\
I don\'t know if this is in the language that makes sense to you.\
Val probably not.

Val Levitan** 37:59\
No, no.

Jason Welco** 37:59\
So I think Aaron, Aaron will certainly understand this and Anton
understands most of it.\
So this was my \'cause you\'re talking about.\
You want to crawl, then walk, then run.\
This is my first take at I can\'t do everything so I want to to crawl,
yeah.

Val Levitan** 38:21\
OK, OK. How how does it show in the box?\
Sure, show me, show show.\
So take the diagram.\
Put a box to it. What\'s next?\
So Anton, make made an made an attempt to show me yellow boxes, purple
boxes.\
So Anton doesn\'t understand everything. You, Jason, understand
everything.\
Show me a box.

Jason Welco** 38:48\
I.\
I I\'m trying to understand your request here.\
You saying that that MVP what which of these boxes is it?\
Is that what you\'re asking me?

Val Levitan** 38:58\
Where do I go from deployment?\
See that yellow box deployment?\
So now now it\'s deployed on what?

Jason Welco** 39:02\
OK.

Val Levitan** 39:06\
What do you call it, Aaron?\
Is it a?

Jason Welco** 39:07\
So. So in the in. So in this in this.

Val Levitan** 39:08\
Is it a test environment?\
One. One second please.\
Well, how do you call this deployment?\
Is that a test environment?

Aaron Bockelie** 39:17\
So continuous.\
I would.\
I would like to correct that Jason if possible to continuous delivery
rather than deployment if we can.

Jason Welco** 39:29\
Sure, I I not.

Val Levitan** 39:31\
So what do you call that yellow box when when Anton says deploy?\
Where does he deploy?\
Is that a test environment?\
He deploys on.

Aaron Bockelie** 39:40\
Yes, there are multiple environments you could deploy to a developer.

Jason Welco** 39:40\
Well.

Val Levitan** 39:42\
Can you?\
Can you can you change this to test deployment?

Aaron Bockelie** 39:48\
So you would have multiple copies of that those yellow boxes in that row
right there.

Val Levitan** 39:55\
Create multiple copies please.

Aaron Bockelie** 39:58\
Let\'s do this.\
Let me help this out a little bit.

Val Levitan** 40:05\
Jason, can you shift the screen?\
So I could see it a little better.\
Yeah. Thank you.

Aaron Bockelie** 40:10\
No, no, no, I think.\
If we were to, yeah.\
There you go.

Jason Welco** 40:25\
And that\'s really, to be honest, that\'s when I had.\
When I had all these different target environments here, that\'s those
are the same.\
That\'s these are equivalent.\
So I didn\'t describe it in the functional case. I just described them
physically.

Anton Leshkevich** 41:37\
Hey that it\'s development test or stage in a production.\
Because.\
Every QA engineer should have its own kind of isolated environment,
because two engineers cannot work in the same environment.\
Conducting like different test cases.\
So it\'s rather environment one, environment two, environment 3.\
Do that make sense?

Aaron Bockelie** 42:07\
Can you define environment with Anton?

Jason Welco** 42:07\
Well, you\'re just saying it\'s it\'s. You\'re just saying it\'s.
You\'re just saying it\'s plural, Anton.

Anton Leshkevich** 42:12\
Mm hmm.

Jason Welco** 42:12\
So these would be.\
Yeah. You, you, you have many targets when you\'re running a test,
you\'re going to say if you\'re running an ad hoc test, you\'re you\'re
going to say what I want to test and where I want to test it.

Anton Leshkevich** 42:17\
Yep.\
Mm hmm.

Aaron Bockelie** 43:08\
So I\'m I think that.\
We need to recognize that everything has tests.\
In this case.\
The Terraform scripts that Jason\'s talking about over here under
application configuration infrastructure is code.\
Configuration is code.\
That\'s this.\
So the application platform, Terraform. That\'s the platform.\
The environment is Docker and it has its own tests.\
Those then get built in, and those can build into the actual code
itself, which has its unit test. Because the code is contained in a
container which is contained in a platform.\
Every single bit of this is written as code in a git repository.\
Individual git repositories.\
Let\'s let\'s do this too.

Val Levitan** 44:32\
Getting coffee?

Jason Welco** 45:01\
Yeah. And Aaron, in the short run, I\'m hoping, you know, with the
especially because if it\'s an EGM, I\'m hoping to short circuit and
kind of.\
Avoid most of the infrastructure.\
Part just by having a small number of containers and then having some
manual process to build them.

Aaron Bockelie** 45:20\
I don\'t.\
I don\'t know.\
I don\'t know if Anton has spoken to you about my.\
Significant shove. I\'ve given the development team to force them to
consider even using.\
Containers inside of an EGM.

Jason Welco** 45:38\
Yeah. Yeah. No, we yeah, we, we\'ve actually discussed that.

Aaron Bockelie** 45:38\
But.

Jason Welco** 45:43\
Yeah, we had a conversation about whether each each component, each
service should run in its own container or.\
But that\'s, I think, a little bit of a development.\
Decision I. I\'m not gonna.

Aaron Bockelie** 45:58\
Well, I\'m. I\'m totally gonna go there because it it has a significant
impact on how the whole platform goes.

Jason Welco** 46:04\
Yeah. Yeah. No, I I get it right.\
So now \'cause, if you do them individually in containers then.\
It it it gets you to your component level testing faster.

Aaron Bockelie** 46:15\
The idea of disk images that are deployed to an OS is so 2007 right now.

Jason Welco** 46:21\
Yeah, I know, I know.\
But we don\'t.\
The thing is, if you think about the EGM for Omni, how many different
configurations are we going to have?

Aaron Bockelie** 46:30\
A ton, and I think an infinite amount of mixing them all up all the
time. I watched him go through thinking about it.

Jason Welco** 46:34\
No, no. I\'m saying initially the thing in in a six to 12 month time
frame. How many configurations do you think we have?

Aaron Bockelie** 46:43\
I don\'t know. I don\'t.

Jason Welco** 46:43\
Yeah. So I I\'m I\'m I guess Aaron, it\'s I.

Aaron Bockelie** 46:46\
I would rather go the parents where we want to build towards if
possible.

Jason Welco** 46:50\
No.\
I get that, but it\'s like so I actually did. You know, we were actually
using Terraform.\
We were doing, we were using not.\
We were using Packer and Terraform it took.\
I\'m going to take a look. It probably took me 8-9 months just to get to
the first thing.\
It\'s it\'s a, it\'s.

Aaron Bockelie** 47:15\
Yeah.

Jason Welco** 47:21\
So I.\
I see the vision.\
The question is what are the tactics?

Aaron Bockelie** 48:07\
I believe this test runner is kind of in the wrong area right now.

Jason Welco** 48:21\
Well, that, yeah, it just depends how you look at it.\
So the you know the test render is part of your configuration.

Aaron Bockelie** 48:29\
Yeah.

Jason Welco** 48:34\
And the split between infrastructure and configuration as code. You know
that gets really fuzzy.\
So I would I would think of the the test agents.\
Your execution agents are are part are part of that deployment.

Aaron Bockelie** 48:53\
Mm hmm.

Val Levitan** 49:33\
Aaron, are you drawing a complete schematic or just the basics?

Aaron Bockelie** 49:38\
I\'m just trying to draw some basics trying to fit these into the
picture.

Val Levitan** 50:03\
Are we still on the deployment stage or now we\'re in the testing stage?

Aaron Bockelie** 50:10\
So we have three different types of repositories that are going on
here.\
We have repositories for the code itself, like the actual software
product. We have repositories for the environments that they run in.\
We have.

Val Levitan** 50:27\
What? What is a? What is an environment? You mean framework?

Aaron Bockelie** 50:30\
Environment could be a building up an entire virtual machine that is
hosted in or a container or operating system deploy environment.\
That the code must run in. So in order to run this code you need to have
node Java, some sort of system object library, some sort of Dlls, some
sort of something, and you have to install that stuff and it has to be
available in the operating system.\
For it to work.

Val Levitan** 51:03\
OK.\
I understand that.

Aaron Bockelie** 51:06\
In a platform you need to define the compute infrastructure. It even
runs in to begin with.\
What sort of OS is it?\
What sort of virtual hardware is it?\
How is the network routed?\
That can all be defined as code in Jason\'s diagram. He\'s got it right
here as infrastructure as code, which is a great call out to have.\
And he\'s got the configuration is code. Is this part this environment?\
So we go to configuring the environment.\
For configuring the platform.\
This is the software itself.\
So we could call this.

Val Levitan** 51:40\
By software, what is it game software?

Aaron Bockelie** 51:43\
Yeah, the product.\
Doesn\'t matter whether it\'s game or framework or RGS or math or
whatever, it\'s the product code.

Jason Welco** 51:56\
I may regret this, but the the the test things themselves. Those would
then be part of the environment.

Aaron Bockelie** 52:06\
Of the environment, they can be part of the code itself, so in my.

Jason Welco** 52:10\
Yeah. Yeah. No, I I mean, I have some third party tool I need to go run
and yeah.

Aaron Bockelie** 52:13\
Yeah. So in my perspective, the tests, the runners for the tests and the
tracking of the tests are all part of the Git repo. If I clone this git
repo, I get all the tests.\
I get all the documents, I get all of the runners to be able to run
everything independently from anything else.\
And I have these tests, these same things test the environment.\
And they also test the platform.\
At all times, all things are testable.

Val Levitan** 52:48\
Anton, do you understand this?

Anton Leshkevich** 52:53\
Yes.

Val Levitan** 52:56\
You do.

Anton Leshkevich** 52:58\
Yeah, it just.\
So I presume that when test runner is linked to Git branch, it implies
that testing is done in the Git branch or like during commit.\
So during pull requests, is that correct?

Aaron Bockelie** 53:17\
Yeah. So the test test runners are propagated across all branches.\
Let\'s say I\'ve I make a a branch in my git repo to add a new feature,
a new feature branch. OK, as soon as I as soon as I clone that feature
branch onto my machine and start writing code for that new feature.

Anton Leshkevich** 53:29\
Mm hmm.

Aaron Bockelie** 53:38\
Well, what I\'m gonna do is I\'m going to write the new code. I\'m going
to write the tests.\
There will be existing tests that go with it.

Anton Leshkevich** 53:44\
Yes, of course.

Aaron Bockelie** 53:47\
And when I commit, they\'re going back into the same folder or directory
structure that the existing tests were at, or the testing framework that
we\'ve got for that particular piece of code.\
So as soon as I have a individual unit like this feature test it might.\
This feature I\'ve written will depend on all the other code.\
That exists in the code in the repo, but since I\'m writing a new
addition to it, it\'s going to basically be independent. If I don\'t
check it in or merge it back to the main code main branch, it exists on
its own and it can run on its.\
Own as a new thing that didn\'t exist before.\
And as soon as I commit it now, when somebody else runs it.\
They\'re going to see another line added to all the tests when they run
all the tests that there\'s my feature that I just added to it.

Anton Leshkevich** 54:37\
Yeah, I get it. It\'s just that.\
So I think that in this scheme you\'re talking about a unit test.\
Is that correct?

Aaron Bockelie** 54:48\
Yeah, yeah.

Anton Leshkevich** 54:48\
Because integration or endtoend test, they would, they would require.
Oh, I\'m so sorry.\
An environment so they will happen after the deployment step and I
don\'t actually need.

Aaron Bockelie** 54:59\
Right, that\'s why.\
So.\
So that\'s why it\'s a unit test.

Anton Leshkevich** 55:05\
I don\'t actually think that this boxes that we call the tool belonging
here, because like you don\'t need a specialized test runner to run unit
test.\
You can just use your regular environment because they are usually
capable of doing so.

Aaron Bockelie** 55:16\
No.\
Exactly.\
But I guess what I\'m saying is, is that it just has different meaning
in different contexts of the types of repositories.\
So I am keeping.\
An environment deployer independent from the product deployer.\
I\'ve got three different repos here in my structure here.\
I actually expect and it. I just hate to do this because it makes the
lines get really messy.\
I actually expect this.\
Let me just draw all the lines just so we see them.\
I\'m gonna change the line type to not be these angled ones because
it\'s impossible to follow.\
Give me one minute.

Jason Welco** 56:00\
Yeah, I have AI.\
Have a hard time getting them to do the line jumps correctly though.
Ordering matters.

Aaron Bockelie** 56:05\
I\'ll just do this.

Jason Welco** 56:06\
Oh, OK.

Aaron Bockelie** 56:10\
\'Cause. Otherwise it looks like \*\*\*\*\*\*\* spaghetti and I don\'t
like that.\
So here\'s my thought.\
Test management, test offering and test runners exist in different
contexts across the different types of repos that we\'ve got here.\
When I deploy my environment, which means to install it into a computer,
an operating system of some kind that I can run stuff I expect there to
be special tests that we have to author and run and manage just for the
environment itself.\
Not the code.\
I also expect specific tests that are managed, authored and ran just to
deploy the platform independent of the environment or the code that it
runs on.\
And so these tests must exist with these branches in order to do it.\
So when I push the button to give me a Kubernetes cluster on Amazon
Boop, one of the things that happens is it runs a bunch of unit tests
for that.\
And when I get to the push the button to make myself an environment
BOOP, I get a bunch of unit tests for that too.\
I haven\'t drawn it yet.\
But then we\'re gonna have something a little different here.\
I believe what Anton saying.\
Is that we might have.\
Integration testing.\
Completely independent from it, and maybe this is the thing that Val\'s
hoping to see.\
\'Cause we have different types of integrations that can occur, right?

Anton Leshkevich** 58:01\
Yeah. And the primary reason is because.

Jason Welco** 58:02\
Yeah, like.

Anton Leshkevich** 58:05\
The product is separated in multiple multiple components and each
component reside in its own Git repository and it\'s I I do not say that
this is impossible, but it\'s not trivial to kind of set up full
product.\
Git pipeline from 1 repository pulling from the other.\
It just a little bit.\
Hard. Not really hard, but I don\'t know.

Jason Welco** 58:37\
Tedious.

Anton Leshkevich** 58:39\
Yeah, that\'s the right word.

Aaron Bockelie** 58:43\
Scoot this way over to the right because this is a little premature.\
So.\
What we also have here, we have integration testing, right?

Val Levitan** 58:55\
Can you Remember Remember a diagram?\
Can you primitively show me?\
Where what do you consider to be?\
Branch, commit and.\
Where does a story get committed and where does a branch get committed?

Aaron Bockelie** 59:15\
Right here.

Val Levitan** 59:17\
Where?

Aaron Bockelie** 59:17\
These right here where it says get branch.\
That\'s why they\'re stacked things.\
You have a feature branch right here.\
A feature branch for a product.\
A feature branch for an environment, a feature branch for a platform.

Val Levitan** 59:33\
This is a parallel thinking.

Aaron Bockelie** 59:36\
Yes.

Val Levitan** 59:36\
But can you show me a? Can you show me a linear thinking?

Aaron Bockelie** 59:41\
I cannot because you have to have code independent from environments
independent from platforms.

Val Levitan** 59:46\
Fine, show me.\
A product called commit line.

Aaron Bockelie** 59:52\
Right here.\
Here, let me draw.

Val Levitan** 59:56\
So.

Aaron Bockelie** 59:57\
Let me make a.\
Let me make a thing.\
Give me one second.

Val Levitan** 59:59\
So is this word story gets committed or or or feature gets committed?

Aaron Bockelie** 1:00:09\
One minute.\
Here\'s your.\
Here\'s your what color are user stories again injura.

Val Levitan** 1:00:25\
Green, green.

Aaron Bockelie** 1:00:29\
What color features purple?

Val Levitan** 1:00:30\
Yeah.\
But purple.

Aaron Bockelie** 1:00:39\
OK.\
Here we go.\
So your user stories commit and make work for the branch.\
This is a feature branch, and So what we might actually call this.\
Let\'s change this text.\
So often in Git, a convention is to shorten the.\
Word feature to feet like that feature add a thing.\
Or in this case, let\'s do another one.\
Feature improve the thing.\
So these bits of JIRA right here or whatever your work back your backlog
is.\
Are operated in this feature and this feature is created for this and so
we could always remember that actually what we have is.\
We have main, right?\
So main sits over here.\
We peel off a copy of main into a feature, add a thing, we modify it,
then we can bring it back into it.\
So let\'s kind of detail that a little more right. Here is the git
repository.\
Here is main.

Val Levitan** 1:02:37\
Can you?\
Can you start a new board for this?

Aaron Bockelie** 1:02:41\
Yeah, we could copy it over.

Val Levitan** 1:02:45\
Let\'s start a new board on this.\
Anton, do you understand this?

Anton Leshkevich** 1:02:55\
It\'s pretty standard git flow to my understanding.

Jason Welco** 1:02:56\
Yeah, this.\
Yeah, this for and for an experienced programmer this is, you know, the
8th grade.\
I hope.

Anton Leshkevich** 1:03:10\
Yeah, yeah.

Jason Welco** 1:03:11\
So yeah, I mean, you may not know this in school.\
You may not understand this, but once you\'ve worked for a little bit.

Aaron Bockelie** 1:03:20\
Here\'s the pull request.\
And actually, I would say I\'m drawing this in the wrong direction here.
Stand by.

Val Levitan** 1:03:28\
Is this is this purple?\
Is this purple or blue?\
This is this is branch right?\
This is feature branch.\
This is purple, right?

Aaron Bockelie** 1:03:41\
No, these are not features.\
These are feature branches.\
They\'re different things.

Val Levitan** 1:03:48\
Isn\'t that feature you explain to me to a great detail that feature
branch the the naming convention is because you take a feature, you
branch it.

Aaron Bockelie** 1:04:03\
It you could call it purple. I I prefer to have these separate colors
because they\'re not.\
This is not a Jura record, this is code.\
This isn\'t a code repo.

Val Levitan** 1:04:13\
I understand, but didn\'t you specifically tell me that you will mirror
image?\
Jira and and.\
Get.\
So it\'s easy for administrator to understand.

Aaron Bockelie** 1:04:30\
Right. And I am deliberately not choosing purple because they are
different things.\
There are.\
This is a completely separate system.\
This is not related to the work itself.\
I don\'t need feature branches or anything to do this work.\
I could just go out and just do it.

Val Levitan** 1:04:51\
You don\'t need it.

Aaron Bockelie** 1:04:54\
Nor does anybody else but.

Val Levitan** 1:04:56\
But you could, but you could relate to it.

Aaron Bockelie** 1:04:58\
As.\
I could, but I I think it\'s a mistake to try to associate these with
user stories.

Val Levitan** 1:05:07\
All right.

Aaron Bockelie** 1:05:08\
It\'s not the same.\
Let\'s let\'s this is getting messy with all these wires in here, so
let\'s I\'m gonna put this back kinda where it was at before.\
We can talk about get flow if you want and I think that might help
illustrate where this is happening because actually what\'s happening is
that unit tests are executed in the Git branch.\
Separate in the feature branch before it\'s even brought back into main
again. As soon as the person commits the code that happened.

Val Levitan** 1:05:36\
Well, well. And so, so that I actually understand.\
But in my mind is this was happening during the commit of a story into a
feature branch, basically green into a purple.\
And at that point you use unit tests. So that makes sense to me.\
They again, in my mind, I understand I\'m not an engineer.\
In my mind, the future branch would be pulled into the main mini feature
is complete. It\'s demonstratable.\
You take that feature, you pull it into a main. At that point you need.\
Integration testing.

Aaron Bockelie** 1:06:23\
No, you do that integration testing before you even pull it back in.

Val Levitan** 1:06:26\
No, no, I understand a condition of pulling a feature into a main is
completion of the integration testing.

Aaron Bockelie** 1:06:37\
Right.\
Which is why we have different environments.

Jason Welco** 1:06:41\
Yeah, and yeah, and Erin a side discussion.\
We don\'t need to get into it here, but just in terms of.\
Crawl, walk, run.\
You know the component level testing is is tougher.\
You know, especially when you\'re changing the contract between things.

Aaron Bockelie** 1:07:05\
Yep.

Jason Welco** 1:07:05\
So I my proposal I originally wanted well, from our conversation I said
OK the the component level is so important.\
We need, we should do it first.\
I\'m more think I\'m running away from that thinking that the
integration the integration case is a little easier.\
So anyway, that\'s that\'s something we we can discuss at a different
time.\
They\'re they\'re both the right things to do.\
I\'m not sure about the sequence.

Aaron Bockelie** 1:07:41\
OK.

Jason Welco** 1:07:43\
I mean, I know.\
I know your feelings on it, but the it\'s the practical partner.

Aaron Bockelie** 1:07:48\
Yeah. No, I I get it. I think The thing is is that.\
Adding unit tests and making sure we have unit test coverage is very
straightforward.\
In the realm of of test management here, and I think just simply having
unit tests to make sure all code committed actually works is really
helpful too. I have no idea what the current quality of the code base is
and how much of it has unit tests.

Jason Welco** 1:08:16\
Yeah. Yeah. It\'s just like I say it\'s it\'s in the details, right?\
\'Cause you have to.\
You have to modify your simulated APIs for your contract testing and
blah blah blah blah blah so.

Aaron Bockelie** 1:08:28\
Right.\
So how likely is it?\
I just. It\'s kinda like a pyramid, right?\
You start at the base, so let\'s let\'s draw a triangle.\
I\'m drawing it out here for minute.\
So you have all these unit tests, right?\
And then on top of unit tests, what do we have?

Jason Welco** 1:09:24\
No, that should be.\
Your.\
For me it\'s the component level testing.\
Some people think of that at the unit test. There\'s a little bit of
Gray area.

Aaron Bockelie** 1:09:37\
Yeah.

Jason Welco** 1:09:39\
And then you have your integration test.

Aaron Bockelie** 1:09:57\
Then what do we have?\
Oops, let\'s take these and move them down.

Jason Welco** 1:10:57\
I guess for us, we actually have unlike other little bit different for
us we kind of at the top of the pyramid we actually you know have the
ITL type of tests.

Val Levitan** 1:11:09\
Do you?\
Do you guys remember where we started from what? What we needed to do?
What? What I wanted to achieve in this meeting?\
Do you guys remember this?\
I wanted to come up with the the 1st.\
The most basic primitive form of simplicity.

Aaron Bockelie** 1:11:45\
There\'s your pyramid. That\'s your testing pyramid.\
Whenever I think about testing, I just think it is layers that stack on
top of each other with reducing number of scope until you get to the
delivery of the product.

Val Levitan** 1:12:09\
I can assure you 1,000,000% like you could take it to the bank if I
don\'t understand it, this project is going nowhere.\
So you could draw anything you want.\
But if you don\'t make me understand.\
We\'re nowhere.

Aaron Bockelie** 1:12:31\
I\'m gonna try and exercise eval.\
Let\'s start at.\
The customer demand, we\'re gonna take it step by step through to
delivery of a product.\
Does anybody wanna write down cards and arrows while we go through it?

Val Levitan** 1:12:48\
It\'s not about customer demand.\
I understand this.

Aaron Bockelie** 1:12:51\
Well, that\'s where we start though.

Val Levitan** 1:12:51\
It\'s about what?\
What do we implement? First, because we cannot implement everything at
once.

Aaron Bockelie** 1:12:58\
We have to.\
We have to have.\
The ability to even write software.\
Do we have that? Yes.\
Do we have the ability to write specific feature improvements to our
software platform?\
We do.\
We have, yes, so.\
Customer demand says we need a new feature for our thing, OK?\
Add it to the backlog as a new feature.\
Do not work on it right away.\
Break it down into chunks that fit in time frame to be able to develop
for the for the team to work on.\
The team has an agreement that they will be writing software and tests
and any integration automation that needs to be able to run those tests.

Val Levitan** 1:13:49\
They will not write.

Aaron Bockelie** 1:13:49\
They don\'t.

Val Levitan** 1:13:50\
They will not write integration testing.\
They will not, but in the beginning they will write unit test.\
That\'s doable.\
So, so the very beginning is there will be unit test implemented that\'s
pretty we could do it pretty quickly.

Aaron Bockelie** 1:13:58\
OK.\
So the whole pipeline halts when we do integration testing then.

Val Levitan** 1:14:14\
Well, I don\'t know how integration is done right now, but somehow.\
In the most primitive, stupid, awkward manner.\
We release products without integration testing.\
So how is it so?

Aaron Bockelie** 1:14:29\
So then what happens then?

Val Levitan** 1:14:30\
How is it done today?

Aaron Bockelie** 1:14:34\
So what happens then is we have to first say things will continue to
move on and complete just as they are right now in whatever blind way
that we do integrate right now.

Val Levitan** 1:14:45\
I.\
I said that.\
I said that from the beginning I said that.

Aaron Bockelie** 1:14:48\
Yeah, OK. So to get from that?\
To something else, we have to start.

Val Levitan** 1:14:55\
So so before so before we get there, can you please on your diagram show
me in a different color or frame what is it that we\'re doing in the
beginning?\
I said in the beginning we can organize git repository and we can have
people write unit tests.

Aaron Bockelie** 1:15:15\
You have to have a git repository literally for the environment that
you\'re building itself.\
Maybe another way to say this is this?

Val Levitan** 1:15:21\
Oh.

Aaron Bockelie** 1:15:23\
You can\'t pan build a Jenkins environment anymore.\
You can\'t hand build a git build environment anymore.\
You can\'t hand build any of that.\
It must all be compiled from code.

Val Levitan** 1:15:34\
Great.\
Show me which squares, which rectangles on the diagram.

Aaron Bockelie** 1:15:40\
It\'s the second one.\
It\'s this one right here. You\'re pointing at it. Unit test
environments environment right here this get repository.

Val Levitan** 1:15:44\
This one.\
But.

Aaron Bockelie** 1:15:50\
Carries environments.

Val Levitan** 1:15:51\
So I need to so.\
So I need to implement this and this. Yeah, this block.

Aaron Bockelie** 1:15:57\
Let\'s let\'s name these clear environment get repository.\
Product get repository.\
Platform get repository.\
Integrator git repository.

Val Levitan** 1:16:22\
What does integrator get repository.\
What is integrator?

Aaron Bockelie** 1:16:26\
Basically the the the script or system that packages everything together
in order to build a independent product that makes it work.

Val Levitan** 1:16:37\
OK.

Aaron Bockelie** 1:16:37\
You can consider this the installer for example, but even the installer
is just a piece of an integrator.

Val Levitan** 1:16:41\
OK.\
OK.\
So we we don\'t have a treatment, right?

Aaron Bockelie** 1:16:53\
I don\'t think so.\
I don\'t think any of this stuff exists.

Val Levitan** 1:16:54\
OK.\
OK so.\
The the first week.\
Like what do we do?

Aaron Bockelie** 1:17:04\
You try to build the product.

Val Levitan** 1:17:08\
Try which squares in this up. OK so so this is step #1.

Aaron Bockelie** 1:17:09\
The top one, this one this this row.

Val Levitan** 1:17:16\
This is week #1, right?

Aaron Bockelie** 1:17:18\
Then you say, OK developer person.\
You can no longer hand build your environment anymore.\
I want you to completely automate building them environment that it\'s
going to run in in scripting.

Val Levitan** 1:17:34\
OK, OK. So.

Aaron Bockelie** 1:17:34\
How are you going to do it?

Val Levitan** 1:17:38\
Can we do frames around and put number 1234?\
How do we do it?

Aaron Bockelie** 1:17:47\
You commit to this one.

Val Levitan** 1:17:49\
Right.

Aaron Bockelie** 1:17:49\
It completely breaks the way people do development.

Val Levitan** 1:17:52\
OK.

Anton Leshkevich** 1:17:55\
Maybe this is the right moment, because I don\'t think there\'s much
development going in Omni project right now.

Aaron Bockelie** 1:18:04\
OK.

Val Levitan** 1:18:05\
What? What is the right?\
Moment.

Anton Leshkevich** 1:18:08\
This is the right moment.

Val Levitan** 1:18:10\
Yes, it is the right moment, that\'s why.

Anton Leshkevich** 1:18:11\
Yeah, yeah, yeah.

Val Levitan** 1:18:12\
That\'s why I\'m trying to push this through. But even though this is
the right moment, everything at once cannot be implemented.\
So what can be implemented first?\
Got it.\
OK, this this needs to be implemented first, OK.\
Clear.\
So this is step #1, right?

Aaron Bockelie** 1:18:36\
So.\
The thing is, is that you can do this without.\
Writing an entire product, you could build an empty. This this thing
could be just completely empty and be built in a in a day.

Val Levitan** 1:18:52\
OK, OK. Day Great. What\'s next?

Aaron Bockelie** 1:18:56\
Then you start adding your code back into it, and then you grow it from
there.

Val Levitan** 1:18:59\
OK.\
Clear. Got it.\
As I do that.\
I am forcing them to write. What is the environment?\
Is the environment #2.

Aaron Bockelie** 1:19:16\
No. What I\'m saying is that all four of those things could be done in a
day to begin with with.

Val Levitan** 1:19:17\
No. OK.\
Really.

Aaron Bockelie** 1:19:25\
With nothing with no code.\
You\'re not actually writing any product code other than Hello World.\
And you will go do everything to deploy it onto your environment and all
you will get is a program that says asserts Hello World and that\'s it.

Val Levitan** 1:19:43\
OK.\
So first I set up the environment that consists of these four.\
What do I call them? Integration.

Aaron Bockelie** 1:19:56\
They\'re the levels of your of your pyramid.\
Let\'s let\'s call it that for now.

Val Levitan** 1:20:02\
So I create an environment consisting of four levels of testing permit
or integration permit.

Aaron Bockelie** 1:20:11\
Let\'s start by deciding what platform it\'s going on to.

Val Levitan** 1:20:15\
What is a platform?

Aaron Bockelie** 1:20:17\
Is it an online platform?\
Is it a mobile device?\
Is it?

Val Levitan** 1:20:21\
Omni.

Aaron Bockelie** 1:20:23\
A operating system that\'s hosting the game.

Val Levitan** 1:20:27\
Yes.\
It\'s Omni platform.

Aaron Bockelie** 1:20:30\
And what does it run on a Linux OS?

Val Levitan** 1:20:33\
Linux OS, yes.

Aaron Bockelie** 1:20:35\
OK. How are we going to get it on to it?

Val Levitan** 1:20:40\
I don\'t know.

Anton Leshkevich** 1:20:42\
Probably the ISO image when that we need to build.

Aaron Bockelie** 1:20:44\
How are you going to do it without an ISO image that is physically
carried on to the machine?

Anton Leshkevich** 1:20:50\
Docker probably then.

Aaron Bockelie** 1:20:51\
But then that forces us to have a conversation about the architecture.
So I would say in Jason\'s diagram he\'s got. Or did I see SCP or arts
error right here? I saw these icons up here. I saw this little SSH thing
here, so we could assume that.

Anton Leshkevich** 1:20:52\
And and.

Aaron Bockelie** 1:21:10\
In a test environment, so the first thing we start is with development
environment.\
We\'re gonna grab this thing.\
And we\'re gonna use SSH.\
Which is a way to tunnel into a development environment or development
deployment environment, and we\'re going to say that we\'re going to
deploy.\
Our platform.\
Into that right.\
So this thing right here, this first pipeline.\
You need to be able to point it at a raw computer and have it reach out
to that computer format. Its hard drive, deploy the Linux OS and get it
set up to ready to receive the environment which is stage 2.

Val Levitan** 1:21:59\
Sorry, do I need this at that point?

Aaron Bockelie** 1:22:04\
This is later.\
It\'s it\'s not stack rank.\
There\'s no order of importance really to this right now.

Val Levitan** 1:22:13\
OK. But these three need to be implemented.

Aaron Bockelie** 1:22:18\
All of them need to be implemented, yes, because otherwise.

Val Levitan** 1:22:21\
I\'m I\'m talking about at this stage at this stage.\
This.

Aaron Bockelie** 1:22:27\
Let\'s get rid of these. You don\'t need to see these right now.

Val Levitan** 1:22:31\
So at this stage, do I need all of these?

Aaron Bockelie** 1:22:34\
Yes, you need all three of them because this if you if you run just this
right here.

Val Levitan** 1:22:37\
OK.

Aaron Bockelie** 1:22:42\
The only place your code runs is on your developer workstations, which
isn\'t helpful.\
Right.\
If you only focus on this one.\
You can control your developer workstation, but you only have a
developer workstation.\
So what you\'re doing is you\'re saying OK.\
Let\'s start with.\
The platform, so the platform is.\
Replay.\
The platform.\
Is the underlying operating system and host that the environment must be
configured for.\
I\'m gonna put operating system in quotes because platforms mean
different things in different contexts.\
OK.\
That\'s two.\
Let\'s shrink that a little bit.\
That\'s a little big for that \'cause, that is.

Anton Leshkevich** 1:23:53\
Actually the the platform is always going to be Linux, regardless
whether we decide to.\
Go with dockers or ISO images.

Aaron Bockelie** 1:24:04\
I disagree.\
It could also be a serverless platform.\
I fully expect to see RGS or your math stuff run on a serverless
platform at some point in the future.\
Serverless architecture, which means you don\'t care what it runs on.\
It runs actually independent of things.\
So let\'s be careful and not quantify ourselves into saying it\'s going
to be a Linux OSA platform could just as easily be a Windows machine for
doing tests.\
Because you guys have significant investment in Windows machines and
stuff too.\
So don\'t, don\'t quantify it yet.\
Keep it amorphous.

Anton Leshkevich** 1:24:41\
OK.

Aaron Bockelie** 1:24:44\
I understand where you\'re coming from, Anton, but I\'m. I\'m sorry.
I\'m getting coming down on you really hard.

Anton Leshkevich** 1:24:53\
It\'s OK.

Aaron Bockelie** 1:24:53\
Next.\
The environment.\
Requirement is the set of system functions, libraries and capabilities.\
Et cetera, necessary to run our application which must be configured
for.\
So.\
That\'s the environment.\
The environment also.\
Can be deployed through this way too.\
Finally.\
Product the executable compiled code based on the environment defined
and aligned with the platform expected to run on.\
Also deployable through SSH to the development environment.\
These three things are necessary to have the basic minimum of continuous
integration, continuous delivery.\
Continuously delivering to the deployment to the development
environment.

Val Levitan** 1:27:16\
OK.\
So this is a bare minimum for.\
A development environment.

Aaron Bockelie** 1:27:26\
Yeah.

Val Levitan** 1:27:27\
How long does it take to bring this to life?

Anton Leshkevich** 1:27:44\
It\'s a good question.

Jason Welco** 1:27:46\
Yeah, it\'s, it\'s it\'s, it\'s it\'s going to be a very iterative.\
So Aaron and I would probably have a spirited conversation about the
long term versus the short term.

Aaron Bockelie** 1:28:01\
What\'s the opposite color of yellow?

Anton Leshkevich** 1:28:05\
Green maybe?

Jason Welco** 1:28:06\
You mean on the wheel?\
Your yeah.

Val Levitan** 1:28:22\
So how long does it take to create this environment?

Aaron Bockelie** 1:28:26\
Purple Purple is the opposite of yellow.\
It depends on the skills of your developers.

Jason Welco** 1:28:33\
So I\'ll I\'ll.\
I\'m gonna give you a terrible answer, but it just kind of.

Val Levitan** 1:28:40\
Can you please give me a simple answer?\
Not terrible and not long.

Jason Welco** 1:28:44\
Yeah, weeks to months.

Aaron Bockelie** 1:28:51\
I say a day because I could use AI if I have all the pieces I need to
write my scaffolding.

Jason Welco** 1:28:57\
Oh well. I mean, yes, I can go take an existing environment and say here
it is, right. So.\
Yeah.

Val Levitan** 1:29:07\
What sort of specialist do I need to write this environment?

Anton Leshkevich** 1:29:15\
I mean to sit up like the repository is going to take a day.\
Just I\'m thinking how to convert existing components to this and
that\'s where I\'m getting a little bit confused.

Jason Welco** 1:29:25\
And then and well.

Val Levitan** 1:29:27\
What do you call components?\
What is component?

Anton Leshkevich** 1:29:29\
Omni LGS Omni games math engine.

Val Levitan** 1:29:32\
I see.\
I see.

Jason Welco** 1:29:35\
Yeah. So in, in terms of the platform and and the environment.\
So I had a a small group that reported to me and I called them dev OPS
engineers.\
So in terms of if your question was what type of engineer needs to
create the environment, it was the title of the engineer, was a DevOps
engineer.

Val Levitan** 1:30:07\
So Aaron, I could ask Nathan.\
Is he a dev OPS engineer?

Aaron Bockelie** 1:30:12\
Yes.

Val Levitan** 1:30:13\
And he\'s available now.\
I can bring him in.\
How long will it take for for Nathan to set up this environment for me?

Aaron Bockelie** 1:30:21\
I think that for him to give you a turnkey hello world with my little
stars here would be a few days because he has to get asked a lot of
questions and things like that and get things set up and make sure
accounts are.

Val Levitan** 1:30:35\
Who? Who would he be asking questions?

Aaron Bockelie** 1:30:39\
Probably.

Val Levitan** 1:30:39\
Anton and Sasha.

Aaron Bockelie** 1:30:40\
And I don\'t think Sasha is much.\
I mean, Sasha should be knowing what\'s going on, but I have a feeling
it\'s actually Andre and Anton.

Val Levitan** 1:30:50\
So if I pair up Nathan with Anton and Andre, this could be done within
three days.

Aaron Bockelie** 1:30:59\
I would give it a week because this the more people you.

Val Levitan** 1:31:01\
One week.\
Great. One week.\
One week, yes.

Aaron Bockelie** 1:31:04\
To get to heoworld.

Jason Welco** 1:31:06\
Yeah.

Val Levitan** 1:31:06\
I\'m saying the environment.

Aaron Bockelie** 1:31:08\
I\'m saying all three of these pipelines to be able to produce Hello
world onto something onto a a an environment.

Val Levitan** 1:31:16\
OK.\
OK. That includes the Hello World tested right it will.\
It will actually say hello world.

Aaron Bockelie** 1:31:26\
Right. If you zoom into this, it says first Test Hello World asserted as
a mock test.\
And you have first piece of code Hello World written to attempt file on
the environment.\
That\'s literally what it said.

Val Levitan** 1:31:36\
Understood, understood. OK.\
So now I have this environment.\
What\'s the second step after this environment is set up?

Aaron Bockelie** 1:31:46\
You will need to start cloning these repositories.\
And naming them and coming up with a strategy of expansion from the
initial Hello World application stack into the other into products.

Val Levitan** 1:32:02\
Who is going to be doing that?\
What sort of specialist do I need?

Aaron Bockelie** 1:32:07\
Well, you would use that same set of people to help guide and I would
imagine the first real product you\'d be doing this with would be the
Omni framework, right?

Val Levitan** 1:32:16\
Right, right.

Aaron Bockelie** 1:32:18\
So you would then bring Sasha into the mix and you\'d say Sasha here is
our.\
Our platform.\
Definition here is our environment definition and here\'s our code based
definitions we\'re at when you start committing your content into the
product code.\
You will need to grow the environment and grow the platform to support
your desires of the platform code.\
Because you\'re not just writing code anymore, Sasha.\
You\'re writing a product.\
The product has all these other pieces in it.

Val Levitan** 1:32:57\
OK. And how long would that take for this team?

Aaron Bockelie** 1:33:02\
I think it take months possibly.

Val Levitan** 1:33:04\
Months I don\'t have.

Aaron Bockelie** 1:33:05\
Yes.

Val Levitan** 1:33:06\
I don\'t have months finding.

Aaron Bockelie** 1:33:07\
So then you need another Sasha.

Val Levitan** 1:33:11\
Find another way for me.\
What\'s the other way?

Aaron Bockelie** 1:33:13\
Sasha needs to learn how to use AI.

Val Levitan** 1:33:17\
OK, good. How long will it take?

Aaron Bockelie** 1:33:22\
I don\'t know.\
We need to ask Sasha that question.

Val Levitan** 1:33:26\
I don\'t have Sasha here.

Jason Welco** 1:33:28\
Yeah. So I I mean.

Val Levitan** 1:33:29\
How long will it?\
How long will it take?

Jason Welco** 1:33:31\
I can just give you past experience so using.\
Using Packer, PowerShell and Terraform, I had probably 1 1/2 people
working on it and it took.\
Probably 5-6 months to do.

Val Levitan** 1:33:53\
Yeah, I don\'t.

Jason Welco** 1:33:53\
Yeah. I I I\'m just telling you what it took.

Val Levitan** 1:33:54\
I I I don\'t have that. I don\'t have that.\
I\'m not interested.\
I don\'t have that.

Jason Welco** 1:33:59\
Yeah. No, I I, I I was just.

Val Levitan** 1:34:01\
It\'s not.\
It\'s not gonna work.

Jason Welco** 1:34:03\
No, I I I I wasn\'t.

Aaron Bockelie** 1:34:03\
Then then OK.

Jason Welco** 1:34:05\
I was not proposing that right. I\'m just.

Aaron Bockelie** 1:34:08\
Here\'s here\'s what we do then. Here\'s an alternative Sasha gets
promoted to architect.\
He doesn\'t get to really write a lot of code anymore.

Val Levitan** 1:34:15\
We don\'t promote people in Belarus.

Aaron Bockelie** 1:34:18\
Well, OK, we laterally move him over to architect.

Val Levitan** 1:34:21\
We don\'t need to move them.\
We just need to.

Aaron Bockelie** 1:34:23\
We tell him he\'s an architect.

Val Levitan** 1:34:24\
We just need to task him.\
No, we don\'t need that.

Aaron Bockelie** 1:34:27\
He cannot write code, he Sasha the only way. This will scale then Val is
that Sasha becomes someone who writes specifications and tests and
requirements. And we hire a team of developers. 5 or 6 developers who
have experience in building softwares, on software, on platforms
especially probably J.

Val Levitan** 1:34:27\
Stop, stop.

Aaron Bockelie** 1:34:48\
Based node based applications and then we can get that team to probably
ride it in three months.

Val Levitan** 1:34:55\
Right. What in three months?

Aaron Bockelie** 1:34:57\
To to refactor the Omni framework to to minimum version in three months.

Val Levitan** 1:35:04\
What? What does it mean minimum version?

Aaron Bockelie** 1:35:08\
Something that could play a basic game.\
They could run a basic demonstrator game.

Val Levitan** 1:35:16\
Will it be written?\
What in different language?

Aaron Bockelie** 1:35:19\
No. To be written in whatever Omni framework\'s written in, which is
probably node and and TypeScript.

Val Levitan** 1:35:24\
So why?\
Why do?\
Why do I need to rewrite anything I just?\
I just need to move the the parts of the code into proper repository.

Aaron Bockelie** 1:35:35\
I don\'t.\
I have not seen any demonstrator of of.\
Omni Framework game running yet.

Val Levitan** 1:35:43\
But I understand this, but I have to assume that people are not lying to
me.

Aaron Bockelie** 1:35:49\
I also feel that as soon as you start running it, you\'ll find that you
don\'t have any tests on any of it.\
And when you write tests, you\'re gonna find a whole bunch of broken
\*\*\*\*, and you\'re gonna have to write your code.

Val Levitan** 1:35:57\
We are not talking.\
We\'re not talking about any tests yet here.

Aaron Bockelie** 1:36:03\
OK.

Val Levitan** 1:36:03\
Look, look at what you drew.\
You did not.

Aaron Bockelie** 1:36:06\
Yes.

Val Levitan** 1:36:07\
You did not say any tests, right?\
No.

Aaron Bockelie** 1:36:13\
Whole bunch of code if you take. If I took the entirety of the Omni
framework as it is right now, put it under and I and I got rid of this.

Val Levitan** 1:36:18\
Right.

Aaron Bockelie** 1:36:21\
I went poop like that and just did product code.

Val Levitan** 1:36:24\
Right.

Aaron Bockelie** 1:36:24\
You just added a \*\*\*\* ton of technical debt, and now your team\'s
gonna spend the next four months remediating all the code that they just
didn\'t test.

Val Levitan** 1:36:33\
No.\
No, because it\'s my reality.\
That\'s how I work today and we brought it to A to a particular
condition.

Aaron Bockelie** 1:36:45\
If you don\'t have.

Val Levitan** 1:36:45\
So now, now, now. It\'s whatever, whatever stage it is in, I need to.\
What\'s the word I\'m looking for?\
Parallel it or port it?\
Maybe I\'m using wrong wording onto onto this onto this environment.

Aaron Bockelie** 1:37:00\
Sure.\
Make up for it.\
Mm hmm.

Val Levitan** 1:37:06\
So the code.\
The actual language, the code remains the same.\
I just need to split it into whatever modules.

Aaron Bockelie** 1:37:14\
I\'m not saying that you have to rewrite.\
You\'re not refactoring what Sasha\'s written.

Val Levitan** 1:37:18\
I know, but I\'m trying to understand what I need to do. Like what?\
Like physically, I need to take this.\
You see the wall.

Aaron Bockelie** 1:37:27\
Yeah.

Val Levitan** 1:37:27\
Wall consists of bricks, but so it actually will be the same number of
bricks but different wall, different shape.

Aaron Bockelie** 1:37:37\
Mm hmm.

Val Levitan** 1:37:37\
Right, so I need to disassemble this wall.\
Separate them into separate breaks and don\'t go and assemble the same
wall, same number of breaks, but somewhere else.\
Is this what you\'re telling me? I need to do?

Aaron Bockelie** 1:37:54\
I think that you need to take.

Val Levitan** 1:37:55\
Give me. Give me a visual visual parallel.\
I\'m I\'m not a cold guy.

Aaron Bockelie** 1:37:59\
Sure, I\'m. I\'m trying to right now, but Bitbucket appears to not be
working.

Val Levitan** 1:38:04\
Just explain.\
You\'re very you. You can do simple explanation.

Aaron Bockelie** 1:38:09\
Take the repo that is in Bitbucket that says Omni framework.\
Ask Sasha to make it actually produce a program that can run.\
And there\'s, there\'s your starting point.\
No tests, no bothering, no nothing.\
Just stick it in the code repo.\
Declare it a A get branch for this.

Val Levitan** 1:38:30\
Which code repos so he needs to take his code, separate it into product,
environment and platform.

Aaron Bockelie** 1:38:38\
We have.

Val Levitan** 1:38:39\
Right.

Aaron Bockelie** 1:38:40\
We start.\
So since we\'re starting in reverse, we have for the product
environment. Right now we have product code right now, but we don\'t
have environments and we don\'t platforms.

Val Levitan** 1:38:47\
Right.

Aaron Bockelie** 1:38:49\
So we\'re gonna say, Sasha, where does this run at successfully?

Val Levitan** 1:38:49\
Right.

Aaron Bockelie** 1:38:54\
And he\'s gonna say what?

Val Levitan** 1:38:57\
I don\'t know.\
He needs to wrap around his mind how to logically separate the entire
code.

Anton Leshkevich** 1:38:58\
Oh oh.

Val Levitan** 1:39:05\
A monolithic code. If I I\'m trying to use your terms that you taught me
monolithic code into three.\
33.\
Umm.\
I don\'t know if there are three, three environments.

Aaron Bockelie** 1:39:24\
So he doesn\'t have this.

Val Levitan** 1:39:28\
Product environment and platform, yes.\
Is this what he has to do?

Aaron Bockelie** 1:39:33\
Incorrect. Sort of. You\'re getting close.

Val Levitan** 1:39:35\
Incorrect. OK, OK, correct me.

Aaron Bockelie** 1:39:38\
Sasha has a product code environment right now.\
He has product code.\
Sasha\'s environment.\
The middle row that you see in there is literally his workstation.\
OK.\
Sasha\'s platform isn\'t really even thought about yet.\
We have an assumption that probably the platform is the online gaming
platform that eventually it goes to.\
But right now, Sasha\'s environment is his own workstation.

Val Levitan** 1:40:14\
Online gaming club.\
You say in the machine.

Aaron Bockelie** 1:40:16\
So is that.\
So isn\'t that where Omni kind of started from?\
Was Anton. Didn\'t Omni sort of was born from the online games.

Anton Leshkevich** 1:40:28\
Yes, that\'s correct.

Aaron Bockelie** 1:40:30\
Right. So the closest thing we have to a platform right now is online
gaming platform.\
So what Sasha has to do.\
Is he has to prove that his product code will run on his workstation
first fully.\
I don\'t care how by hook or crook tests are no tests.\
Run it, Sasha.\
Make it run without an exception.\
Once he does that.\
Then we can make sure that he has an environment builder that can deploy
an environment onto a platform, probably just another computer or
workstation.\
All of the libraries, all of the configurables, all of the pieces to
independently run that code abstractly on any amount of computer he
wants.\
So we can build a factory for Sasha workstations, basically.

Val Levitan** 1:41:31\
Anton, do you understand this?

Anton Leshkevich** 1:41:37\
Yes, but it\'s got a lot of information for me.\
I\'m trying still trying to process it.

Val Levitan** 1:41:41\
Because you\'re trying to eat at the same time and.

Anton Leshkevich** 1:41:45\
No, no. I\'m answering a message.

Val Levitan** 1:41:47\
And.

Anton Leshkevich** 1:41:48\
Jason in in teams?

Val Levitan** 1:41:51\
OK, stop messaging.\
Focus on what\'s being said and stop eating.

Anton Leshkevich** 1:41:52\
OK.

Aaron Bockelie** 1:41:57\
So.

Val Levitan** 1:41:57\
And stop having coffee and don\'t go to the and don\'t go to the
bathroom.

Aaron Bockelie** 1:42:00\
So Sasha.

Val Levitan** 1:42:03\
Just think.

Aaron Bockelie** 1:42:04\
Don\'t smile.

Val Levitan** 1:42:06\
And don\'t.\
And don\'t smile.

Anton Leshkevich** 1:42:08\
OK.

Val Levitan** 1:42:09\
Just don\'t do anything.\
Let your brain focus on what Aaron is saying.\
Aaron put it all together now again.

Aaron Bockelie** 1:42:16\
Sasha has to be able to prove that his code can compile and run.\
Once he can prove that, then we ask Sasha. Where are you running it at?\
And he\'s gonna go well, my workstation, and then we\'re gonna go. OK,
write me a script or pieces of code that can deploy a copy of your
workstation.\
The essential pieces of your workstation to run this code anytime we
want.\
That\'s what. That\'s what the environment is.\
And then we\'re going to say, all right, it\'s running now, Andre.\
Work with Sasha to write some more code that when we push the GO button
carves out virtual infrastructure somewhere or on a machine or
whatever.\
I don\'t care.\
That prepares that infrastructure to be able to deploy our environment
on.\
And then once we have the prepared environment, then we can deploy our
product onto that and you can do this for forever infinitely
automatically.

Anton Leshkevich** 1:43:24\
Yeah, that makes that makes perfect sense.

Val Levitan** 1:43:27\
So repeat that.

Anton Leshkevich** 1:43:29\
We basically need.\
A.\
Well, prove that everything works.\
And then we need to builder and deployment process.\
Preferably automatic.\
But yeah.

Val Levitan** 1:43:43\
I.\
I don\'t need anything automatic right now.

Anton Leshkevich** 1:43:45\
OK so.

Jason Welco** 1:43:48\
Well then reproducible I think is probably the what you\'re looking for.

Val Levitan** 1:43:51\
OK.

Aaron Bockelie** 1:43:51\
Yep, Jason got the right word. Yep.

Val Levitan** 1:43:54\
Anton Anton. Put it all together for me. Repeat it.

Anton Leshkevich** 1:43:57\
So we need to be able to build and deploy the product code, the Omni
game, let\'s say for starter.

Val Levitan** 1:44:08\
OK.\
How do I do it?\
What\'s the physical act of doing it?\
Who can do it?

Aaron Bockelie** 1:44:18\
I can add this one here.\
Let\'s just describe it again.\
In more detail, Sasha will have his computer.\
He will have a integrated development environment, an IDE that he grabs
his code from Git, the the Omni Framework Code. It copies it to his
computer when he attempts to run it the first time, he just throws all
these errors up on his terminal when he tries to.\
Run it says you need this library and you need that library and you need
to configure this.\
You need to configure that.\
And he\'s going to work through all these 1 by 1 by 1 until he\'s got it
all set up and on a little notepad to his side, he\'s going to write
down every single thing he installed.\
I installed npx.\
I installed this library.\
I installed that library.\
The reality is, is that it\'s a little more complicated.\
Use package locks and all sorts of \*\*\*\* is stored inside the code
repo in the product code repo.\
But at the end of the day, he can then grab a copy of the product code.\
And run it on his machine with minimal configuration of his of his
machine. Once he\'s established that that code is now committed to the
product code repository.

Val Levitan** 1:45:24\
OK.

Aaron Bockelie** 1:45:30\
Then what he does is he wipes everything clean, starts clean again, and
he goes all right.\
I\'m going to try to write myself an environment configurable system, so
I\'m going to start a new code code repo.\
And I\'m going to download a piece of. I\'m gonna write some programs
that automatically configure my computer to be able to install all those
pieces.\
When I load all these bits up into it, I\'m gonna hold on to those.\
So now all he has to do is he, when he tests that and he makes sure it
works, he\'s gonna just run it to make sure.\
And then he gonna run his product code and without touching his product
code anymore, he\'s gonna try to configure that environment automation
code to set up his workstation.\
So he\'s going to completely wipe his workstation clean again.\
Is going to download from git the environment git repo. He\'s going to
push go. He\'s going to sit and watch it complete, and then he\'s going
to have a copy of the product code and he\'s going to push go and they
will run perfectly.\
The code for now, the environment and the code for the product are
committed to Git repo and his work is saved.

Anton Leshkevich** 1:46:41\
No, I get it. Now. Instead of kinda going through read me and typing in
manually commands that you need to set up your local environment, you
simply gonna clone this environment repository and run script that
configures your machine. OK.

Aaron Bockelie** 1:46:54\
Absolutely. And then you can also call it a pipeline YAML file and stick
it in Bitbucket or GitHub.

Anton Leshkevich** 1:47:02\
Yeah.

Aaron Bockelie** 1:47:02\
Same thing.\
Yeah, that\'s exactly what you\'re saying I\'m saying.

Val Levitan** 1:47:04\
OK.

Aaron Bockelie** 1:47:07\
And then finally, we\'re going to take Sasha\'s computer and Kick It Out
of 1/3 Storey window, breaking the glass and splattering it on the
ground.\
And we\'re going to give him a cell phone to connect to AWS or to
Azure.\
And he\'s going to write a deployer on his cell phone, a platform
thing.\
And he\'s going to code that as a terraform, and it\'s going to call up
a particular virtual machine.\
It\'s going to define the OS that\'s installed on it, the network egress
point and the software that gets initially loaded.\
And he\'s going to have that thing called the Environment git repo and
then calls the product repo and when he hits the GO button on his cell
phone.\
It will automatically configure virtual virtualized infrastructure.\
You\'re in the cloud somewhere. It will pull down the environment
configuration and deploy that, and then it will pull down the product
code and run that.

Val Levitan** 1:48:03\
Good. OK.\
What is the company\'s benefit for doing all of this?

Aaron Bockelie** 1:48:12\
Reproducible. You don\'t need Sasha to set up anything anymore.\
Geolocation doesn\'t care.\
Testable. Scalable.\
Those are five things to start with that come off the top of my head.

Val Levitan** 1:48:27\
Anton Anton, do you agree with what Aaron said?

Anton Leshkevich** 1:48:31\
Well, actually yes, because I tried to set up.\
Environment for LGS the other day and I couldn\'t do.\
Couldn\'t do that.\
So I was missing lots of dependencies and I had to contact Alexander to
kind of figure it out.\
So probably this is a good idea.

Val Levitan** 1:48:50\
So can you?\
Can you prove this to Sasha that it\'s a good idea without error?

Anton Leshkevich** 1:48:58\
Yes, I can try.

Jason Welco** 1:49:01\
You start off the sentence with Val wants.

Val Levitan** 1:49:01\
OK.\
Tell tell me. Tell me.\
Tell me.\
Define minimum amount of work.\
That only Alexander must do.\
And nobody else can.\
And all other work.\
Associated with this could be given to somebody else.

Anton Leshkevich** 1:49:33\
So Alexander will have to kind of.

Val Levitan** 1:49:37\
Must must. Alex. Without Alexander, it will not be done.

Anton Leshkevich** 1:49:39\
Must.

Val Levitan** 1:49:41\
So must only Alexander must do what?

Anton Leshkevich** 1:49:42\
OK.\
Alexander must.\
Define environments for LGS.\
Um.\
Or progressive controllers, I would say I would assume I I think this is
his area of responsibilities.\
I can do do the Omni framework because I used to work with the code base
and I know how to set up set the things up.\
What other components do we have?\
Yeah.

Val Levitan** 1:50:22\
Progressive progressive we could give to Igor Bitewski.

Anton Leshkevich** 1:50:26\
Yeah, math engine.\
That\'s efim\'s responsibility, obviously.

Val Levitan** 1:50:31\
But that\'s that\'s at the very last moment, right?

Anton Leshkevich** 1:50:34\
Yeah. OK.

Val Levitan** 1:50:34\
We don\'t have to.

Anton Leshkevich** 1:50:36\
So we have LGS Omni framework but for for the very basic demonstration
we we only need LGS and the Omni framework so Alexander can write
environments for LGS. I can do for Omni framework.

Val Levitan** 1:50:54\
What, what else can we take away from Alexander?

Anton Leshkevich** 1:51:01\
In the context of environments, I guess that\'s it.

Val Levitan** 1:51:06\
So we can have Nathan set up the environment.\
Am I\'m saying something incorrectly?\
What would Nathan\'s function be?\
Aaron.

Aaron Bockelie** 1:51:24\
Say that one more time.

Val Levitan** 1:51:26\
What would Nathan\'s function be in this?

Aaron Bockelie** 1:51:26\
Replay.

Val Levitan** 1:51:29\
What? What does?

Aaron Bockelie** 1:51:30\
Nathan\'s function would be to ensure that the.\
The platforms that we\'re choosing for this.

Val Levitan** 1:51:38\
I I would like to, Nathan, physically do things so he can. What\'s his
deliverable.

Aaron Bockelie** 1:51:41\
Yeah.\
He\'s he\'s configuring the platforms themselves, so Andre, he\'s he\'s
working closely with Andre to to configure the Git platform, and this
probably GitHub. He\'s helping to make sure that all of the correct.\
Pipe or actions are defined correctly and written well, so they actually
pull things down and create stuff like the operating system image and
and then also make sure the environments are pulled down.\
He\'s going to probably ensure that testing hooks and the actions.\
Are extensible for Jason to be able to put his true test harness
platform into play and to make sure that we have tie insurance to QA.\
QA might end up just running inside of GitHub instead of JIRA. For all I
know, I mean Jason.

Val Levitan** 1:52:27\
And all and all of that he can do in one week.

Aaron Bockelie** 1:52:31\
No. No way. He\'s gonna get. He\'s gonna get hello. World done in a
week.

Val Levitan** 1:52:33\
OK, how how how much time?\
OK.\
Sorry, how much time does he need for all that?

Aaron Bockelie** 1:52:40\
Hello world done in a week.\
The other stuff.\
Probably 6 months. I\'m going to give. I\'m going to give that time
frame for that.

Val Levitan** 1:52:46\
Don\'t be don\'t be crazy.\
I don\'t have six months.

Aaron Bockelie** 1:52:49\
It\'s it\'s, it\'s depends on how much you want, how much coverage do
you want.

Val Levitan** 1:52:55\
Can I split his work into two?

Aaron Bockelie** 1:52:58\
You could probably chop it into even finer pieces.\
You could just do it week by week.\
Or, you know, Sprint by Sprint.

Val Levitan** 1:53:04\
No. Into two people, can I?\
Can I deploy two people on this?

Aaron Bockelie** 1:53:09\
I don\'t think so.\
I think the amount of change management that has to occur to be able to
get it, keep everybody up to speed is gonna prevent you from moving
faster.

Val Levitan** 1:53:17\
Is Nathan the right guy?

Aaron Bockelie** 1:53:20\
Yeah, you can absolutely be the right guy.\
And I say that can be the absolutely the right guy, because he\'s going
to have to be able to start working with the other people.\
He can\'t do it on its own without everybody else going along with it
too.

Val Levitan** 1:53:38\
I have a very talented dev op.\
That set up Kubernetes for us.

Aaron Bockelie** 1:53:49\
Mm hmm.

Val Levitan** 1:53:50\
Who I can deploy, so I\'m asking is it Nathan or is it the other guy?

Aaron Bockelie** 1:53:55\
I\'d start with the other guy first.

Val Levitan** 1:53:57\
OK.

Aaron Bockelie** 1:53:58\
But you need to make sure that your other guy can communicate the
intentions and everybody else can follow along \'cause if he just comes
in and sets it up, you\'ve done nothing useful.\
You\'ve you\'ve built up a a Taj Mahal.

Val Levitan** 1:54:15\
Well, he he set up Kubernetes and passed it on to Andre and Andre
successfully running it.

Aaron Bockelie** 1:54:19\
Right.\
And nobody else knows how to run it. But Andre?

Jason Welco** 1:54:25\
Yeah, it\'s the cake versus the recipe, right?\
So if you give me a recipe, I can make the cake, but if you give me a
cake, I can only eat it.

Aaron Bockelie** 1:54:36\
Right.

Val Levitan** 1:54:37\
OK.\
So we\'re saying we\'re saying that Andre doesn\'t know the recipe to
Kubernetes.

Aaron Bockelie** 1:54:38\
Everybody.\
Andre has the ability to make a particular cake. Right now, I think he
can make variants of that cake. I think he\'s getting there, but we
need. He needs to inherently know all he needs to be a cake master.\
He needs to be a master.\
Baker is what he needs to grow in.

Val Levitan** 1:54:59\
I know, but in order to be a master Baker, you gotta practice baking.

Aaron Bockelie** 1:55:03\
Right.

Val Levitan** 1:55:04\
I could give you all the recipes in the world, but if I don\'t know how
to bake still the cake will not turn out.

Aaron Bockelie** 1:55:09\
Is.\
He\'s got he\'s got to get all of the practice from this and he has to
get everybody else in asking for all the different variants of it and
all those other people who are working with him. This is where analogy
starts to fail.\
Need to understand the the the what works and what doesn\'t for what.\
Their asks are.\
So while Andre might be our dev OPS engineer, ultimately.\
Sasha Pasha? Anybody else must be able to demand things of them and
expect a dev OPS approach to stuff rather than staying in their own
little world.\
And just kind of doing their own thing.

Val Levitan** 1:55:52\
Very long time they they cannot.

Aaron Bockelie** 1:55:53\
That\'s the change management I\'m talking about.

Val Levitan** 1:55:56\
Yeah, yeah. I\'m not asking for that.\
I\'m asking for things to start working with the support of Dev. Op
engineer.

Aaron Bockelie** 1:56:05\
So if you\'ve got an engineer on hand that speaks Russian, that can talk
to everybody else, that\'s going to be a better fit than Nate.

Val Levitan** 1:56:13\
Then who?

Aaron Bockelie** 1:56:14\
Than Nathan.\
Sorry, Nate.\
Hey, Nathan. So The thing is, is that Nathan may be the better guy for
the larger perspective of how this all gets to delivered out there and
also tool techniques and coding techniques. But I think The thing is, is
that start with the Russian guy to get the.

Val Levitan** 1:56:17\
Yeah.

Aaron Bockelie** 1:56:32\
Absolute basics in there we have.\
We must have other people.\
Everybody who\'s a developer has to be able to tell this story right
here in front of us. If they cannot, we are not going to get there.

Val Levitan** 1:56:46\
OK, that\'s that\'s future, I understand.\
OK.\
Our two hours is up.\
I need to think.\
This was productive.\
What I would like to do for Jason please.\
So now I understand what needs to be done first.\
Now try to.\
Similarly, express the tool.

Aaron Bockelie** 1:57:15\
I\'m gonna leave this nugget for you, Val.

Val Levitan** 1:57:16\
Simply in stages.

Aaron Bockelie** 1:57:18\
This is.\
This is the future nugget for things.\
Can you slow Scroll down just a little bit, Jason, that\'s on your
screen share?\
Let\'s look at this screenshot.\
I want you to zoom in on this.\
This is an aspect of GitHub.\
This is you see in the lower right corner where it says code spaces.\
Down right here.

Val Levitan** 1:57:38\
Yeah, yeah, yeah.

Aaron Bockelie** 1:57:38\
That blue thing?\
This is completely virtualized.\
It is an entire development environment.\
It\'s the workstation itself.\
It\'s all the libraries, it\'s all the testing.\
It\'s all the files.\
It\'s all the git repos in a web browser, meaning that you don\'t need a
work station anymore.\
You can write it.\
Run it. All right here.\
And this is the kind of stuff where we get to because you you gotta.

Val Levitan** 1:58:03\
OK.\
But.

Aaron Bockelie** 1:58:05\
That\'s the big value prop for this entire thing right here.

Val Levitan** 1:58:09\
The absorption of this sponge the the sponges filled to the brim, cannot
absorb anymore.

Jason Welco** 1:58:10\
All right.

Aaron Bockelie** 1:58:14\
OK.

Jason Welco** 1:58:16\
Is.\
Are we using GitHub Aaron?

Val Levitan** 1:58:18\
It\'s.

Aaron Bockelie** 1:58:20\
We\'re moving that direction is what it looks like.

Jason Welco** 1:58:22\
OK, OK, I I I didn\'t realize that was OK \'cause there\'s there\'s.

Aaron Bockelie** 1:58:24\
Yeah.\
Andre Andre is working.

Val Levitan** 1:58:28\
Thank you very much.\
Thank you very much everybody.

Aaron Bockelie** 1:58:29\
Andre is working.

Val Levitan** 1:58:32\
Time\'s up.\
Need to go and work. Thank you.\
Bye bye.

Jason Welco** 1:58:34\
Alright, Aaron, can you?

Aaron Bockelie** 1:58:34\
Alright. Thanks bill. Alright.

Anton Leshkevich** 1:58:35\
Thank you.\
Have a nice day.

Jason Welco** 1:58:37\
Can you hang? Hang out for a minute?

Aaron Bockelie** 1:58:38\
Yeah, I got one. One or two minutes here.

Jason Welco** 1:58:40\
OK.\
All right.\
So I mean, I think you and I are pretty much in synchronization, I think
I mean everything you say, I understand.\
I think it\'s the other direction.

Aaron Bockelie** 1:58:52\
Yeah.

Jason Welco** 1:58:53\
On the platform and the environment, I don\'t think we need to do big
things first because we\'re targeting the EGM.

Aaron Bockelie** 1:59:01\
No.

Jason Welco** 1:59:03\
It\'s only a couple of environments and they may change, right?

Aaron Bockelie** 1:59:06\
I.

Jason Welco** 1:59:07\
We need a way to deal with change, right?

Aaron Bockelie** 1:59:08\
Yeah.

Jason Welco** 1:59:09\
You know, I I need to add a library. I need to make sure the next
deployment\'s going to have that library.

Aaron Bockelie** 1:59:13\
Well, let\'s just, let\'s just call that the training wheels.\
It\'s something they\'re from.

Jason Welco** 1:59:16\
Yeah, yeah. But I\'m saying is, I think we can kind of do it where
whether the outputs in ISO or.

Aaron Bockelie** 1:59:23\
Yeah.

Jason Welco** 1:59:24\
A docker.\
So we have a Docker container that has a bunch of crap in it and has
some scripts to be able to deploy it. I think that\'s all I need to do.

Aaron Bockelie** 1:59:30\
My my worry.\
Yeah, my here\'s my worry.\
Is that when we start letting them?\
Sort of.\
There are a lot of ingrained bad habits with this team and I think that
if we let them sort of stay in familiar space, they will over optimize
for that space and they\'re not gonna learn as much as if we kind of
force them to stay simpler.\
And also but stay simpler on the product code but stay.

Jason Welco** 2:00:02\
Right. But I I guess what I\'m getting at is learning.

Aaron Bockelie** 2:00:02\
Attracted and build.

Jason Welco** 2:00:04\
You know, dealing with things like.\
You know whether it\'s.\
So you use Terraform so that you have a little bit of you can be nimble
and go to cloud formation versus this versus that.

Aaron Bockelie** 2:00:17\
Yeah, yeah.

Jason Welco** 2:00:18\
But there\'s just a big yeah. It\'s a huge learning curve.

Aaron Bockelie** 2:00:21\
Right. I I don\'t think we need a whole lot.

Jason Welco** 2:00:22\
Like I say I I it it was probably close to a year before I got tangible
results from having three people.

Aaron Bockelie** 2:00:29\
Right.

Jason Welco** 2:00:31\
Work on Terraform, Packer and PowerShell scripts.

Aaron Bockelie** 2:00:37\
Right.

Jason Welco** 2:00:37\
Like 3 people almost a year.\
And then we got and then we got some.

Aaron Bockelie** 2:00:41\
Yeah.

Jason Welco** 2:00:43\
We got some benefit, right?\
So I had an operations team.\
You know, we\'re deploying dozens of these multi server configurations,
right?

Aaron Bockelie** 2:00:52\
Mm hmm mm.

Jason Welco** 2:00:53\
Yeah.\
And yeah, so anyway, I think there we didn\'t talk at all. And I\'m
seeing there\'s just such a huge gulf Val.

Aaron Bockelie** 2:00:57\
Let me show you.

Jason Welco** 2:01:04\
I don\'t think has any concept of why you need a test framework tool
like, whether it\'s Tosca or smart bear or whatever it is.\
So I don\'t think he sees that. And I\'m. I\'m. I\'m gonna. I\'m. I\'m
challenged to explain that I\'m not.

Aaron Bockelie** 2:01:14\
Yeah.

Jason Welco** 2:01:22\
I might need your help to get there.

Aaron Bockelie** 2:01:24\
This is this is the kind of magic that we can pull off nowadays.

Jason Welco** 2:01:34\
Get all that? But Eve the first concept.\
I mean, I I I presume you\'re gonna start showing me some UI or AI
integration with.

Aaron Bockelie** 2:01:41\
No, it\'s not even integration.\
It\'s this is has nothing to do with integrating anything.\
This is just getting.\
It\'s like it\'s like having a custom template ready for us.\
Play.\
Replay.\
Write me a terraform Hello World for AWS using EC EC2 that can deploy
Hello world application that asserts on the deployed host the words
Hello world temp inside a Docker container.\
So we\'re gonna auto write the terraform.\
We\'re gonna create the variables. We\'re gonna create the Docker file.\
We\'re gonna write a script.\
Just a bash script that does hello World.\
In one shot.\
This is why I was saying on the call we could get to Hello World in one
day.\
Given the right access to the systems and tools here, we are watching it
get created as we go.\
We don\'t even have to necessarily understand how it all works.\
We just get to the point of making it deploy and then we reverse
engineer and learn from there. Now in conjunction, that\'s that\'s what
I said just now is the perspective of a developer who doesn\'t
necessarily know Terraform. If I am a dev OPS engineer, of course I.\
Know Terraform and it\'s going to be easy for us to be able to get this
and start it up.\
And we can then run this.

Jason Welco** 2:03:37\
Yeah, yeah. No, I mean, yeah.

Aaron Bockelie** 2:03:38\
It all.\
Write docs for this and then I could all lather on, make a make a action
in GitHub for this and then we can just get the beginning scaffolding
right away.

Jason Welco** 2:03:44\
Sure.\
I.\
Alright.

Aaron Bockelie** 2:03:55\
I don\'t think it\'s as hard as we think it is.\
Like obviously what you were doing was full scale, right?\
Like it\'s the real deal with all the code and all the all the stuff.

Jason Welco** 2:04:05\
Oh, we were just.\
But we, I mean we\'re we\'re just doing little.\
Oh, and you talk about in the past, right? Yeah.

Aaron Bockelie** 2:04:10\
Yeah, yeah, in the past.

Jason Welco** 2:04:12\
Yeah, yeah. No, because we were.

Aaron Bockelie** 2:04:12\
So what I\'m saying is.

Jason Welco** 2:04:14\
We were getting murdered to death because you know.\
Some some network setting wouldn\'t get set right on one of the VM
instances, and we\'d have some strange \*\*\* problem and.

Aaron Bockelie** 2:04:25\
Yeah.

Jason Welco** 2:04:29\
Yeah, or the Windows updates weren\'t applied correctly, and we all all
the usual horror stories.

Aaron Bockelie** 2:04:38\
So you know, can I set this up so I can use GitHub actions?

Jason Welco** 2:04:39\
But I\'m still all right.\
So I, I, Erin I, I accept this.

Aaron Bockelie** 2:04:41\
So yeah.

Jason Welco** 2:04:43\
I\'m just now on to my next challenge with Val, given how.\
What a struggle it was to kind of define this just like I I think he\'s
thinking that he can just have Anton, you know, do something magical.

Aaron Bockelie** 2:04:53\
Yeah, the issue.

Jason Welco** 2:04:59\
And suddenly testers can write test cases.\
And that\'s just not how it\'s gonna work.

Aaron Bockelie** 2:05:01\
No, this is yeah.

Jason Welco** 2:05:03\
So we gotta he. He kind of threw a little bit of cool.

Aaron Bockelie** 2:05:03\
Well.

Jason Welco** 2:05:09\
I would say not cold water, but definitely cool water. I was giving him
a budgetary idea of, you know, what, some of these tools might cost. And
he was like, well, we\'re not going to do that.\
Just like.\
OK, you know.\
So yeah, anyway I\'m I\'m. I\'m now trying to figure out what I really
need to illustrate is that we need a non coding person to be able to
write test steps.

Aaron Bockelie** 2:05:39\
Yeah, that\'s going to be cucumber.

Jason Welco** 2:05:42\
Well, I would.\
It could be, I think.

Aaron Bockelie** 2:05:44\
Or something like that.

Jason Welco** 2:05:47\
I actually.

Aaron Bockelie** 2:05:47\
\'Cause you cover gonna. Let\'s let non-technical people write stuff,
right?

Jason Welco** 2:05:51\
Yes, that that is one approach, but I don\'t know if you are you
familiar with like Tosca and and those tools.

Aaron Bockelie** 2:05:57\
Yeah, I also know that my cucumber, if you let people write any, any old
schmo write cucumber test, it turns into cucumber goo.\
And it\'s really awful.\
And you you can really.

Jason Welco** 2:06:06\
Yeah, yeah, yeah.\
Now you want something that\'s for, for, you know they\'re going to be.\
I mean it is an approach I\'m not.\
I\'m not discounting that as a as a solid BDD approach.\
It would just be without.\
Without the right tools with it, it just becomes your. Your goo
explanation was pretty good.\
I\'m gonna spend.\
I\'m gonna spend more developer dollars on the bindings and
implementation than I than I am.\
On the Tosca tool or anything else?

Aaron Bockelie** 2:06:37\
Right, so here I\'m. I\'m. Yeah, I just.\
I think The thing is, is it that conversation was basically Val
completely avoiding the topic of actually writing any tests.\
He said.\
I I almost, you know, the TV show Fraggle Rock from the 80s.

Jason Welco** 2:06:55\
I never watched it, so I know it was there, but I don\'t know what it
was.

Aaron Bockelie** 2:06:56\
It\'s like OK.\
Well, anyway, there\'s a little bit character.\
These little Muppet characters that build stuff out of looks like
glass.\
In the little glass constructions and stuff.\
And in every episode, there\'s some calamity where there\'s something
breaks and it all comes collapsing down, and they got to fix it.\
And it\'s like the tales of hardship and woe and teamwork, right?\
What we just talked about was deliberately building a glass house with
no testing framework.\
And Val needs to realize that what we just did was talked about.\
What\'s it gonna take for Sasha to make the code work enough to start
without really any unit tests or any integration tests or anything?

Jason Welco** 2:07:39\
Yeah.

Aaron Bockelie** 2:07:39\
And the very first thing we\'re doing is we\'re baking in a huge serving
of of.\
Technical debt into actually adding the testing back in.

Jason Welco** 2:07:49\
Yeah, I I guess what I\'m getting at is if we go, if we go the cucumber
approach, right? So OK, I can just, you know, go into X-ray and type
some englishish crap in there and decide, you know, have a sequence of
things in there, I don\'t think.\
It\'s going to, I don\'t think it\'s going to work very well. I think
you got to invest in a tool that I can just, you know do.

Aaron Bockelie** 2:08:09\
No.

Jason Welco** 2:08:13\
A wizzywig thing where I have a wizard and I can go.\
I can go go to the game.\
Do some things, record it and then edit it and massage it as I need to.

Aaron Bockelie** 2:08:24\
Yep.

Jason Welco** 2:08:30\
And I\'m trying to figure out, given how that explanation went, how am
I?\
How am I gonna?\
How am I gonna communicate this to Val?\
That says this is what.\
This is what ship left testing looks like.

Aaron Bockelie** 2:08:46\
So just to show you, here\'s the Terraform Repo from an initial commit.

Jason Welco** 2:08:51\
Yeah.

Aaron Bockelie** 2:08:52\
Here\'s all the docs.\
Here\'s how it works.\
Here\'s the repo setup.\
Here\'s how you deploy it.\
Here\'s how you init the project structure and everything else, and
additionally, when we go to actions, here\'s the Terraform Cicd for it.
You can see it failed because it tried to run.\
Because it didn\'t have credentials.\
So literally it tried to run the whole thing.\
Failed to refresh credentials.\
Need to get the rolls.\
Literally, we\'re at the stage where it just needs credentials.\
And here\'s the crazy thing is, if I just screwed around with this for
another hour afterwards, I\'ll have credentials done and everything else
too.\
So we can get to this really fast now.\
So anyway, that\'s all I\'m saying.

Jason Welco** 2:09:39\
Yeah.

Aaron Bockelie** 2:09:41\
I think that it feels.\
Daunting, but it doesn\'t have to be.

Jason Welco** 2:09:48\
Yeah, it was in, in our experience.\
You know, I was talking about.\
I had those people, you know, doing all this stuff and learning stuff.\
It wasn\'t.\
You know, it\'s always that that first 80% was always pretty easy.\
It was the last 20% that took you 90% of the time, yeah.

Aaron Bockelie** 2:10:00\
Yeah, of course.\
I.\
I I think I showed you the the the joke is is that this is the first 90%
to get it working and then the last 10% is the rest of the year.\
You know.

Jason Welco** 2:10:13\
Yes, yes, yes. Yes, exactly it\'s.

Aaron Bockelie** 2:10:15\
I understand that iceberg principle is very much in in in play here.

Jason Welco** 2:10:17\
Yeah.\
Yeah. So anyway, I would.\
I don\'t know.\
Do you have any advice for how to explain this to Valve?\
It says, hey, this is what it is and This is why I think we need to
spend some money.

Aaron Bockelie** 2:10:37\
I think that Val needs to see the value of it coming out and he needs to
see a clear set of actionable goals that people can work on.\
My hope is is that not only can we provide specific goals, but we can
also I my hope is to be able to work this into the sprints themselves.\
I want to see their engineers actually work in Sprint\'s.\
So we can get a gauge on the amount of time it takes to do this stuff.\
And define clear object each of these.

Jason Welco** 2:11:08\
And that was in in the picture I was showing the one with the colored
boxes. You know those were kind of like epics in my mind.\
Right, so I\'ve got an epic that says I need to be able to, you know,
interact with the UI.

Aaron Bockelie** 2:11:15\
Right.\
Sure. And I and I I just think that we\'ve got to really, there\'s no
way you can build it all at once in one big thing.\
We start with a Nope.

Jason Welco** 2:11:26\
Oh yeah, but I don\'t.\
I don\'t think I can.\
I\'m I\'m struggling right now.\
How do I get past go?

Aaron Bockelie** 2:11:33\
OK.\
So the get pass go is to do this we need to do a slightly more involved
version of what it just showed you.\
We\'re using some sort of technique to to begin the framework for
hanging stuff. I know that Anton has already worked on a lot of like git
rules and sort of working agreements and things like and I think we need
to really leverage that.

Jason Welco** 2:11:54\
Yeah, yeah.\
So I.\
I had him work. So what?\
We kind of did, was we did just a little quick prototypes to, you know,
validate that we could.\
It was mostly on the integration, right?\
How do I I get a pull request?\
What can I do right?\
So can I go get? Can I go look at the branch, parse out the JIRA of the
story?\
Go into jira.\
Find the test cases that that apply to that.\
Find the test cases that are automated.\
Well, we don\'t know how to do that yet.

Aaron Bockelie** 2:12:27\
Mm hmm.

Jason Welco** 2:12:27\
Oh no, that\'s true.\
No, we can do it.\
So anyway, those are like the little things that that we\'re going to do
and then you know, can I deploy that and.\
You know \'cause, we we\'re just cheating right now.\
We\'re just when the bit bucket does the build, you know the build
sitting there in a virtual machine of some sort.\
And then we just, you know, ran ran the Hello world test inside of
there.

Aaron Bockelie** 2:12:50\
Right.

Jason Welco** 2:12:52\
And then we take the output and we put some artifacts in into the JIRA
itself into the test and the test results.

Aaron Bockelie** 2:12:59\
You know what I suggest doing?\
I gotta run here, but I would suggest this.\
Think about the diagram that we were looking at today.\
It had a lot of pieces and parts moving around in it. I think we
simplified it into these three layer these three pipeline or actions
that action groups, you know that I kind of showed you right, there\'s
the the code, there\'s the environment, there\'s the platform I know.\
It\'s more complicated than just the three.\
There\'s a lot of nuances in between each of those that kind of
interplay with each other.\
I think that will be really helpful is to map out.\
About the typical like developer experience that happens for different
people.\
Don\'t draw all the boxes with all the logos and things like that.\
Instead, explain the developer experiences as they work on their
workstation.\
Here they work on code.\
Here the QA engineer has this experience.\
Here they work on their tests.\
Here they go.\
Check their stuff.\
In this they go run their program and that they deploy from this.\
And actually name those those things, whatever those are.\
Are they doing pull requests in GitHub?\
Are they doing code reviews in GitHub?\
Are they looking for their work in JIRA?\
Are they looking at their artifacts in artifactory?\
Or maybe it\'s Azure Azure files or whatever it happens to be we gotta.\
I think that\'s gonna make it feel much more tangible is to have named
platforms for all the things and where they\'re going.\
And then I think this is where you could say the test the the test
management platform, is this or the test harness or framework, is that
and we need to just do it for a specific product, let\'s just pick LGS
local gaming server or we pick the 0?\
Framework as a starting point and then we can use that same exact flow.\
To sell this to, to sell and tell.\
The same experience story for the different personas several times for
the different products they\'re gonna come up because that\'s gonna give
us that feel for what it\'s supposed to look like. And it\'s also gonna
be a customer centric approach to it in that we\'re telling the story
from.\
The customer, the customers, the developer of course, and the
development teams and any of the work that has to be done to be able to
build this can then be ranked and prioritized by.\
The value of the story.\
So obviously we really, really want.\
To have our our code repos first, and then we\'re gonna really, really
want to have an artifact location, and we\'re gonna really, really want
to have probably a deployment or a environment that we can run stuff in
to see it be at the EGM itself or virtual machine.\
Somewhere or whatever. I think that\'s kind of.\
The path to reality here for this.

Jason Welco** 2:16:01\
Yeah, I I was thinking it from even just from more of the testers.\
Point of view, right?\
So I\'ve got a test case.\
I\'m going to play.\
I\'m going to play a game.

Aaron Bockelie** 2:16:15\
So The thing is, is that that tester.\
Their job is to test this game.\
And they\'re gonna play it well.\
The questions that are in their head is what commit is it on what branch
is it on?\
Where do I even test it at?\
Do I run it on my local work station in order to reduce the amount of
effort the tester has to do?

Jason Welco** 2:16:29\
Mm hmm.

Aaron Bockelie** 2:16:34\
Ideally, the system itself has logged against that test that applies for
that feature and says click here to open the instance where this game is
deployed at.

Jason Welco** 2:16:44\
Yeah, yeah, yeah, yeah.\
So part of that, so like on the picture I had on the mirror board, I had
it in addition to the test cases, I had a box that said configurations.\
Right, because I have a feature I want to run it on a dual screen with
this game this RTP.\
Well, maybe not.\
I don\'t know if RTP needs to be part of that, but anyway there is a set
of things and I want to run it there.

Aaron Bockelie** 2:17:11\
We\'re only going to get the ability to run it there once we have an
automation pipeline for environments.

Jason Welco** 2:17:18\
Yeah. Yeah, no, I get that.\
But I\'m. I\'m I\'m I\'m taking this.\
I\'m taking this last two hour discussion and saying that\'s a that\'s a
parallel activity, right?

Aaron Bockelie** 2:17:27\
Yeah, yeah.

Jason Welco** 2:17:28\
Right. So somebody\'s working on the continuous deployment. Great.\
Not continue. What was your delivery? Sorry.

Aaron Bockelie** 2:17:36\
Right.

Jason Welco** 2:17:37\
So that\'s happening, right?\
So yeah, it\'s a prerequisite and.\
But now we have to get into, you know, Val talked about the tool.\
That tool.

Aaron Bockelie** 2:17:50\
No, I think it\'s The thing is, is that there\'s lots of tools and we
gotta we gotta take into consideration that Val\'s looking for a tool.

Jason Welco** 2:17:50\
So.

Aaron Bockelie** 2:18:01\
But what Val\'s really looking for is a solution for this and the tool
and solution for sort of synonymous I think.

Jason Welco** 2:18:04\
Yeah, yeah, I\'m getting. I I I\'m just getting to the use case story
that says I\'m a tester. I want to.\
I want to, you know, Ghost.\
I want to do this do that do some other things and then I want to look
for a particular result and it\'s a pass fail if right.\
So that\'s my almost every test looks like that.

Aaron Bockelie** 2:18:24\
Alright.\
I\'ll I\'ll leave.\
I\'ll, I\'ll. I\'ll wrap up with an analogy. When we build furniture,
there is no single tool that builds a chair.\
Right there is many tools.\
The joiner.\
The planer the table saw the chop saw the chisels, whatever.\
And there\'s no one tool that measures and and and tests it.\
There\'s calipers and measuring in your own \*\*\*\* and everything else
needed to test your furniture right.\
So the solution for that and I think this is the key piece that we got
to say is it, it\'s not a tool, it\'s a solution which is a series of
tools.\
Executed in the right stages and that has to be sold and told as a as an
easily understood narrative.

Jason Welco** 2:19:04\
Yeah, yeah.

Aaron Bockelie** 2:19:11\
Because I I see it like this. If Val can grok it, if he gets it, he can
easily either shove it down people\'s throats or sell it to people
inside of his company.\
Because who he is.\
And I think that\'s the key to getting this to work. So.

Jason Welco** 2:19:29\
Yeah, yeah, yeah. I\'m just.\
I\'m trying to cross the education chasm because.\
Like I say, yeah, we have all these thing.\
It\'s a very complicated picture. Lots of tools, Ansible, this that
other thing.\
So I\'m like kind of concentrate that says I have manual test cases
today. We\'ve gotten them to write them down a little bit.\
Step one through step 10.\
How do I automate that?

Aaron Bockelie** 2:19:52\
One of the one of my recommendations now that I\'ve worked with Val for
a little while, is it.\
Don\'t say it\'s a. This is my. This is my terrible idea or this is
that.\
Just say it\'s my idea.\
This is what I think we\'re gonna do and stay consistent on the message
because I think it takes a couple.\
It takes some persistence to to tell it in enough different directions
and he goes. He kind of has a light bulb moment and goes aha, and I
think we got a little bit of a light bulb today with the three things
there. \'cause. I watched him react and.\
Demand.\
Like, how do we make it actually, tangibly do that? And how long will it
take?\
And I was adamant about Hello World because I can\'t predict.\
I don\'t know how well Sasha or other people did. You see, even even how
he was trying to corner Anton into basically asking Anton like, well,
what\'s the minimum that Sasha can do?\
And because he\'s trying to make sure there\'s \'cause he\'s got, he
knows these guys like the back of back of his hand, and he\'s trying to
make sure that he\'s using.\
People for the right things and try and do that orchestration correctly
and I think that\'s we gotta just basically continue to to repeat the
story in a clear, concise fashion for Val to where he can now tell the
same story we\'re telling. I would say that like.\
8-9 months ago he would not have been able to tell the the story of
continuous integration and even get get flow really.\
But now he can.\
So I just I I think it\'s just a matter of teaching.

Jason Welco** 2:21:23\
OK.\
Yeah, yeah. No, I\'m just trying to, you know, \'cause.\
Yeah.

Aaron Bockelie** 2:21:30\
He\'s our.\
He\'s our advocate and he\'s also challenging.\
So we have to.

Jason Welco** 2:21:33\
Yeah, yeah, yeah.\
So I\'m just trying to think of if I\'m going to go show something to
him to try to, you know, tell a story, you know, where do I start
because.

Aaron Bockelie** 2:21:42\
Yeah.

Jason Welco** 2:21:43\
I didn\'t think that that diagram I started with today was not.

Aaron Bockelie** 2:21:43\
So pick pieces.\
He will.

Jason Welco** 2:21:46\
That was dumbed down to me a lot.

Aaron Bockelie** 2:21:47\
It was just too much and I think it need to be revised a little bit.\
Yeah. So he\'s going to challenge you until it breaks down into a piece
that\'s digestible.\
So that\'s the thing that\'s gonna happen.\
And he did that with me, and I tried to respond the best I could, too.

Jason Welco** 2:21:59\
Alright, see ya.

Aaron Bockelie** 2:22:02\
It just it just we got to stay consistent, stay clear and I think
this\'ll work itself out.

Jason Welco** 2:22:07\
Right.\
OK.\
Alright well so I have a meeting with him on.\
Are you invited on the Thursday meeting?\
I don\'t.\
I honestly have no idea what what, what the hell to do on that meeting.

Aaron Bockelie** 2:22:21\
Let\'s see.\
I have meetings every week with him.\
Hurt everyday with him, so look Thursday.

Jason Welco** 2:22:25\
Well, are you? It\'s Thursday.

Aaron Bockelie** 2:22:29\
Architectural proposal to QA commits in July testing.

Jason Welco** 2:22:34\
That, I think is AI. Don\'t know where that title came from.

Aaron Bockelie** 2:22:39\
OK.

Jason Welco** 2:22:39\
I think it\'s an old one, yes.

Aaron Bockelie** 2:22:39\
But that\'s the one you\'re invited on.

Jason Welco** 2:22:41\
Yeah, it is the time. So I\'ll try to message him that this whole
meeting came up today.\
\'Cause I was asking about that meeting, I said.\
What do you?\
What do you wanna do?\
Do you? Do you really need?\
I wasn\'t planning to do an end to end demo and then it just went down a
rabbit hole from there.

Aaron Bockelie** 2:22:58\
OK, my my take on that reading those notes.\
So today we didn\'t talk.\
I I told you we we talked about what I feel is a brittle approach to
starting. Sometimes you just have to be brittle to start with.\
But we gotta \'cause. It\'s brittle because there was no.\
There\'s no test really, though we talked about.\
It\'s just simply like assuming the code works well enough that we can
just slap it into a git repo.\
Hit the go button and and code is compiled and put into an environment
and so forth, right?\
I think that conversation on Thursday is an opportunity to introduce.\
A tangible aspect to what that what test looks like in that space, and I
think that\'s where you were gonna wanna talk about the the serious test
frameworks.\
That you\'re thinking about and how they might.

Jason Welco** 2:23:43\
Yeah. Yeah, \'cause, that\'s that\'s what I want to talk about. I
didn\'t.\
He kept well.\
He kept using the word he wants to see a complete proof of concept.\
So when you say POC to me it means a demo.

Aaron Bockelie** 2:23:57\
Get Apoc that day, \'cause. It\'s just not there yet, but I think that
if we.

Jason Welco** 2:24:00\
Well, I\'m not even sure that he wants AI mean. I just I we we just go
back and forth and I just I feel I I I\'m I\'m a little bit. I\'m not
complaining I\'m just lost.

Aaron Bockelie** 2:24:03\
I don\'t think he does.\
I think what?\
Well, so my suggestion would be to start.\
Let\'s build on what we established today.\
Let\'s take those those 3 layers to the application layer, the
environment layer, the platform layer.

Jason Welco** 2:24:16\
Right.

Aaron Bockelie** 2:24:22\
Let\'s I want you to try to infuse.

Jason Welco** 2:24:25\
All right.

Aaron Bockelie** 2:24:26\
The test approach inside of those, and I think that\'s the discussion
point.

Jason Welco** 2:24:28\
All right. So yeah, so for all right.\
So for example, on the environment, all all those, and I think you
alluded to it, all those things need to have test cases as well, right?

Aaron Bockelie** 2:24:39\
Yeah, absolutely. That I even said right in there test cases you can\'t
deploy, you can\'t deploy a platform, yeah.

Jason Welco** 2:24:40\
Yeah. Yeah, yeah, yeah, yeah.\
Well, I need. I need to validate the environment. We I I don\'t know
what that means, but you know you you.

Aaron Bockelie** 2:24:50\
Oh, you drop a, you drop a hello world marble in the top of your
environment, an orange in your ark. You know, in your whatever you got.

Jason Welco** 2:24:56\
Oh no, I\'m just talking about testing the platform into the environment
independently.\
I I\'m it doesn\'t matter.

Aaron Bockelie** 2:25:02\
Yeah. How do you like the question is, how do you do terraform testing
right?

Jason Welco** 2:25:03\
No. Yeah, no.\
That that, that was the mindset that so people eventually got. I I, you
know, I slowly made change.\
I would.\
You know when people would write software documentation?\
I said the last step of every you know chapter is how do I.\
How do I verify that it\'s correct?\
Right before I go off and do more damage, how do I verify that I\'m OK?\
Right. And that that just gets into this, alright, you need to go.\
I\'ll let you go.

Aaron Bockelie** 2:25:34\
Hang on, I\'ll. I\'ll show you this too.\
Please write tests for all stages of our repo.\
Super vague question. Let me look at what you\'re even talking about.\
Oh, this appears to be a Terraform project with AWS Infrastructure
code.\
It\'s gonna read the variables. It\'s gonna look at what we did.\
It\'s gonna look at the script and it\'s gonna write tests for us. For
all the pieces.\
It\'s going to grab a.\
It\'s maybe not the right decision, but it\'s a decision to get some
testing to start with.\
It\'s going to use teratest.\
It\'s going to use bats for the shell script and it\'s going to use
container structure tests for the container.\
Like, Oh my God, it\'s not the right one answer, but it\'s an answer and
it gets us in the right direction.\
And if we can you leverage, say this combination with the Russian
speaking Dev, OPS engineer.\
There.\
This is a. This is a potential direction to take for this stuff.\
I\'ll install the things for go here.\
So.\
Yeah.\
So I guess I\'m saying this is that it\'s able to write the container
testing and verification and everything else.\
Even writing the docs for being able to edit the the tests so.

Jason Welco** 2:26:54\
And what\'s the is that?\
What\'s the engine underneath?\
What\'s the a? A engine underneath that is that?

Aaron Bockelie** 2:26:59\
It\'s using cloud underneath and client and cloud like anthropic.

Jason Welco** 2:27:01\
Sorry.\
I.\
Oh, OK.

Aaron Bockelie** 2:27:05\
Yeah. So now we have so terraform tests verifies the VPC and Cedar
Block.

Jason Welco** 2:27:07\
Right, so it.

Aaron Bockelie** 2:27:11\
So the network block test, the EC2 deployment instance and type validate
security group rules includes clean up of resources. The Shell script
checks to make sure it does its thing.\
The container test checks its permissions, checks the output and the
container, and make sure the metadata works right.\
Like this is a way to really rapidly iterate on this stuff far faster
than we would normally do.\
It doesn\'t exclude us from using a DevOps engineer who has experience.

Jason Welco** 2:27:42\
Yep, for sure.

Aaron Bockelie** 2:27:44\
Anyway, alright, I\'ll see you later.

Jason Welco** 2:27:45\
Alright, alright.\
Thank you. Alright, bye bye.

Aaron Bockelie** 2:27:47\
Yep, bye.

Val Levitan** stopped transcription
