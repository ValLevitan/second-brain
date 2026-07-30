**CI Architecture Reconvene --- v3 Standard & Integration Repo Review-20260424_081557-Meeting Recording**

24 April 2026, 12:15pm

1h 43m 32s

**\
Val Levitan** started transcription

**\
Aaron Bockelie** 6:43\
So\...\
Who is the person who drafted the document?\
version of it.\
Yeah.

**\
Alexander Biratko** 6:57\
We will try this document. I, Genadi and Andrei.

**\
Andrei Bosik** 7:04\
Yeah, Sasha started this document. Your game continuous and I finished at my part of CICD.

**\
Aaron Bockelie** 7:04\
Did you?\
Did you draft it in Russian first and then translate it the last bit to English?

**\
Alexander Biratko** 7:17\
Yes.

**\
Andrei Bosik** 7:18\
Yes.

**\
Aaron Bockelie** 7:19\
OK, so I\'m going to point out a few critiques of this, so I don\'t be.\
Just be prepared.\
So, first of all, you\'re defining something that is extremely brittle. You\'re defining specific technologies that will go away in six months, probably.\
Next is that you are not defining the invariance, you are defining what you think it\'s supposed to look like.\
You\'re creating a fence or a cage for yourself in defining this this way. And what\'s going to happen is that you\'re locking yourself out of being able to use submodules, which is a very, very normal thing to be using when appropriate.\
by banning it and then go back and going back and reversing it and then allowing it as well.\
Makes it a very confusing thing to follow.\
So\...\
I guess what I\'m trying to tell you is that I think I can see the intentions that you\'ve got, but they\'re mixed up.\
What\'s also happened is that you\'ve then asked for formal\...\
Um\...\
regulatory prose from Claude who happily obliges because it doesn\'t know what it\'s doing. And it gave that to you. So it\'s dressed up as formalism in the prose of the words rather than actually doing what it\'s supposed to do.\
So I think that what you\'ve done is you\'ve stepped into very dangerous territory by masquerading at something that sounds official that will absolutely ruin everything that you\'re trying to do.\
So what I\'m doing right now, I\'m asking Claude to rewrite this with what I call the invariants that you actually need. You know what an invariant means?

**\
Val Levitan** 9:14\
No.

**\
Aaron Bockelie** 9:16\
Invariant means, so, so what is\...

**\
Andrei Bosik** 9:17\
Vern said.

**\
Aaron Bockelie** 9:18\
Go ahead, Andrei.

**\
Andrei Bosik** 9:20\
No, no, continues. I know what is the invariance.

**\
Aaron Bockelie** 9:22\
Okay.\
So variant, variables is the things that can change. Invariant is the things that cannot change.

**\
Val Levitan** 9:31\
No, I know what it means, but I don\'t understand where is it applicable here.

**\
Aaron Bockelie** 9:36\
So what you need to do is you need to define the invariant principles of what you\'re trying to tell everybody in this document rather than tell a bunch of people to use specific technical means that will expire after a while.\
Two.\
Yeah, yeah.\
So, so let\'s see here.\
I need to just kind of briefly review what was down, what was created here.\
Give me one moment.\
Okay, I have something good here. I\'m just making some slight adjustments.\
It\'s similar to V4. The thing is, is that I want you to\...\
Have something that you can work within, rather.\
Game.\
I know it\'ll take some time to review through this, but we can start if you\'d like. Kind of, you can just kind of\...\
Glance through it for a minute.\
I want to point out.\
that the revision note at the beginning is probably the best summary for this.\
So I wanted to be able to state the architectural principles rather than prescribe a specific tool chain.\
I think the thing that you guys jumped onto, the zero trust idea, I think it\'s good. And I think that\'s something I pushed you on, and I strongly believe in that. This is how many different systems and tool chains work, is a zero trust approach. It\'s just hard to call it out explicitly.\
Oh.\
I think it\'s, I think I kind of wanted to push that direction a little bit because out of all the bits that I read in your version 4 graph, I think the zero trust thing is actually what you were trying to hit while also defining a lot of the tech inside of it.\
So at the bottom of this document, do you want me to share my screen with you guys or are you just reading it?

**\
Andrei Bosik** 14:26\
Yeah, I just read it on my screen, not need share.

**\
Aaron Bockelie** 14:28\
Okay.\
Sure, sure. At the very bottom, I\'ve left the appendix that lists the changes and also the reference for technical pieces that you were talking about throughout the version 4 of the document.\
not part of this, so I\'ve removed your specific tools out of the standard.

**\
Val Levitan** 15:34\
Yeah.

**\
Aaron Bockelie** 15:55\
Something that I thought about considering in section 2, which is 0 trust between subsystems, was to clarify that when you write things this way, they become easier to independently verify. So if you\'re submitting something to GLI, for example, a zero trust approach to software means that GLI can review these items.\
in isolation, essentially, and not have to look at the larger dependency chain as often.\
But I elected to not put that in there just so it stays generalized.\
Reading through this in more detail while you guys are reading, I found a slight adjustment I\'m going to make.

**\
Val Levitan** 18:56\
Advance the version number.

**\
Aaron Bockelie** 18:58\
Yep.\
What I\'m doing, Andrei, is I\'m adding some continuous integration SLA targets.\
So, service level agreement, how long, how long is it OK to iterate on a platform before it\'s stable?\
And then also, how long does the old platform exist till it\'s stale?

**\
Andrei Bosik** 20:56\
Yeah, I agree.\
Mhm, mhm.

**\
Aaron Bockelie** 21:37\
All right, here\'s 5.1. It\'s almost identical.\
Three new sections.\
3.1, 5.6, and 6.3.1.\
When you\'re largely done, let me know, please.\
So I forced something pretty\...\
drastic compared to how you guys operate right now.\
In 6.3.1, the new section there. I specified 30 calendar days as the depreciation.\
Timeline from one version to the next.\
Right now you guys go for years.\
Remember, this is a standard documentation, not a as built. It\'s like what you should be doing. So by me pointing it out that ideally 30 days should be the time that you should be able to rip and remove old stuff out is the target you\'re shooting for, not like, you know, some sort of, oh, I guess.\
you know, kind of thing.\
Gives you something to compare it against.\
You could consider that as essentially this means that removing code from your code base is just as important as adding code to your code base by this.\
I mean, I don\'t expecting everybody to be able to comprehend the whole thing right now.

**\
Val Levitan** 26:51\
How do we?\
So.\
Let\'s say Nathan, you know Nathan.\
He\'s working on a particular.\
A part of\...\
Point of sale product.

**\
Aaron Bockelie** 27:12\
Yep.

**\
Val Levitan** 27:12\
And.\
Up until now, we didn\'t get involved in how he organized his repos. And let\'s say we want to go in and implement this structure.

**\
Aaron Bockelie** 27:21\
Yeah.

**\
Val Levitan** 27:26\
Where do we start from? And Nathan is highly intelligent, highly eloquent, highly cooperative, and willing to go to any extent to comply with the standard. So, you know, I\'m going to start with Nathan. I\'m going to say, Nathan, here\'s version 5.1.

**\
Aaron Bockelie** 27:38\
Right.

**\
Val Levitan** 27:45\
This is how we structure our repos, and before we even approached you, we created this.\
Catch mechanism of what doesn\'t work.

**\
Aaron Bockelie** 27:59\
Right.

**\
Val Levitan** 28:00\
So, so about this catch mechanism, number one, is it possible to have this catch mechanism?

**\
Aaron Bockelie** 28:00\
Um\...

**\
Val Levitan** 28:09\
And I don\'t know if I\'m properly calling this.\
And #2.\
And this catch mechanism.\
Direct, highlight the incorrect structure, assist.\
How do I spring this on the Developers who is intelligent, highly educated?\
willing to do work, willing to comply, but find themselves\
Antiquated.\
In this sort of environment, it\'s a horrible feeling for somebody who\'s\...\
proud of his achievements, now realize that for \*\*\*\*\*\* sake, I\'m doing things wrong.\
It\'s a very demoralizing thing.

**\
Aaron Bockelie** 29:03\
I want to rephrase a few things that you said.

**\
Val Levitan** 29:05\
Sure.

**\
Aaron Bockelie** 29:06\
First, first, and actually it\'s interesting because the very way you ask the question demonstrates a way out of the feeling that you\'ve got right now. The first one is, how do we make the changes?\
So, the first when you when you first started asking.\
And I would say that it\'s not about, you don\'t want to just make the changes. What you do is you define, you say, this is the definition of what our quality bar for how our system will operate. This is the definition of how we will operate from this point going forward. And we understand that every single one of your repos is now out of.\
compliance.\
It\'s very different than saying, how do we change it all? Because what it does is it defines that, okay, we\'ve set some new laws up and everybody\'s out of compliance.\
So what we can then say is, how do we actually measure this, right?\
So we can look through the doc and we can start to make some some specific technological measures for how we how we might interact with this.\
So, if we\'re thinking about\...\
Zero trust and autonomy testing and things like that.\
That\'s actually just the spec to be able to write tests. This is the base understanding of the way you would write tests for your software. So if your modules, your repo doesn\'t even have tests.\
You could start there. You could start to accommodate this that way.\
When we start talking about what continuous integration looks like, the whole section about CI. If your repo doesn\'t even have any way to express CI, that is a gross.

**\
Val Levitan** 30:59\
violation.

**\
Aaron Bockelie** 31:00\
violation of this whole thing. And sure, it sounds like we got to put some CI in place for our repo because literally it\'s missing.\
And you\'re never going to get perfection on the first pass. It might be the 10th pass that you finally have got it figured out, and you\'ve got an even pattern. It\'s a\...\
It\'s a control loop, right? It\'s like the thermostat turning on and off. You can\'t ever perfect it. You kind of overshoot it and undershoot it until you find on average that you\'ve got something that you\'re accommodating the problem with.\
So every single one of these sections, from versioning to defining where Cloud MD is at, to how does the repository structure look like, or whatever.

**\
Val Levitan** 31:47\
So, so who\'s who\'s going to do it? Somebody who\'s doing it needs to\...\
aside from having authority, needs to have a clear vision on why we\'re doing it and how to explain it to the developer, what needs to be done. I just, I don\'t understand how to implement it.

**\
Aaron Bockelie** 32:09\
So there\'s this concept in Git, it\'s called code owners.\
Usually a file.\
dot code owners. And it\'s structured in a particular way that basically says these people are the owners of the code.\
You don\'t have a code owner.

**\
Val Levitan** 32:26\
So, do we have this?

**\
Aaron Bockelie** 32:29\
I don\'t think so.

**\
Andrei Bosik** 32:30\
But the owner know.

**\
Val Levitan** 32:33\
So.

**\
Aaron Bockelie** 32:37\
Basically, it\'s the responsible person who is taking on the charge of that piece of the of the code at the has has some amount of maximum decision rights about the code.\
Now, if I assign Sasha as the code owner of everything in JVL, that would be unfair.\
because he isn\'t the sole responsible owner. But if Sasha was assigned on every repo along with other people, then Sasha can share the code owner load with the other people as well. If you add too many people, it doesn\'t mean anything and have any.\
Keith, because ownership by everybody means nobody owns it.\
So you have to find the right fit for code owners inside of your organization to decide.\
who actually is responsible for it. Because the code owners then are responsible for uploading, upholding.\
a specification document like this, the repository standards.

**\
Val Levitan** 33:44\
So, Andrei, let me ask you a question.\
Oh.\
Do you know what to do, like, if I, if I left you alone now?\
What would you do?

**\
Andrei Bosik** 34:01\
Do you mean in this meeting or in no company?

**\
Val Levitan** 34:08\
I mean, this is such a strange answer, I don\'t even know how to answer that.\
What do you mean?

**\
Andrei Bosik** 34:14\
Ohh.

**\
Val Levitan** 34:15\
I\'m confused.

**\
Andrei Bosik** 34:17\
We need to do.

**\
Val Levitan** 34:17\
We\'re discussing repos, repo structures, and enforcing repo structures. What do you think I\'m talking about? Ballet, gymnastics, volleyball? What do you think I\'m talking about?

**\
Andrei Bosik** 34:23\
Ohh.\
Uh\...

**\
Aaron Bockelie** 34:32\
Baccarat.

**\
Val Levitan** 34:32\
Oh.

**\
Andrei Bosik** 34:35\
Yeah, yeah.\
Yeah, the.\
Put back to me, yeah.\
Okay, I\...

**\
Val Levitan** 35:02\
We are too much.

**\
Andrei Bosik** 35:06\
Ahh.\
I think if we speak about this document, yes, I think I know what we need to do, not only I, we all.

**\
Val Levitan** 35:18\
We all just answer for yourself.\
So, you know, right?

**\
Andrei Bosik** 35:24\
Think I, if I think yes, but I think\...

**\
Val Levitan** 35:27\
So, let\'s say, let\'s say, let\'s say Kharetski shows you his repo structure.\
And you would ask him a question, how do I continuously integrate?\
And Kharetski would say what? I don\'t know. That\'s, you know, I\'m the owner of this code.

**\
Andrei Bosik** 35:44\
Mm.\
Mm.\
Yeah.

**\
Val Levitan** 35:59\
My code work, my code works. I don\'t know how you continuously integrate.

**\
Andrei Bosik** 35:59\
Most too.\
I, I think all employers in I mean, and then all developers in our company know what is continuous integration and what is continuous delivery. It\'s the basic things.

**\
Val Levitan** 36:31\
So, Kharetski would know how to continuously integrate his repos, not knowing, let\'s say, Biratko repos.

**\
Andrei Bosik** 36:41\
Thinking, yes.\
And I say more.

**\
Val Levitan** 36:44\
And everyone and everyone in the company knows how to integrate their repos, yes?

**\
Andrei Bosik** 36:52\
In my understanding, I think yes.

**\
Val Levitan** 36:56\
and how to test. So they would answer 2 questions. I know how to test it and I know I know how to integrate it. Yeah.

**\
Andrei Bosik** 36:59\
Mm.\
About this, no, I think no.

**\
Val Levitan** 37:09\
So they wouldn\'t know how to test it. They wrote it. They wouldn\'t have a clue how to test it.\
But they know how to integrate it. But they only own, let\'s say, 5 repos out of 50. And they know how to integrate it into the entire product. Or they would tell you, I only have 10% of the entire product. How do you expect me to integrate it?

**\
Andrei Bosik** 37:35\
Ohh, uh, uh.

**\
Val Levitan** 37:45\
Every developer knows where at the end their repo will be integrated in the product.

**\
Andrei Bosik** 37:50\
Unit test.

**\
Val Levitan** 37:55\
but not everyone knows how to test it.

**\
Andrei Bosik** 37:59\
Because the developer can do unit test, but he can do not understanding how this work in full infrastructure.

**\
Val Levitan** 38:08\
So I could, I understand, but I could tell you from a logical perspective, so I don\'t know anything about programming or development. Nothing, zero.\
But what you\'re telling me doesn\'t make any sense to me.\
If you know how to integrate but you don\'t know how to test.\
Doesn\'t make any sense to me, but okay, I\'m wrong. Maybe I\'m wrong.\
I\'m just telling you in front of everyone.\
But logically to me, it doesn\'t make any sense. But okay, I\'m wrong.

**\
Andrei Bosik** 38:42\
We have two different tests. We have unit tests and we have integrated tests.

**\
Val Levitan** 38:48\
We have 3 tests, unit test, integration test, and end-to-end test.

**\
Andrei Bosik** 38:50\
Maybe 3 years.\
I have, for example, for example, today we try deploy and.

**\
Val Levitan** 39:03\
My point, my point is this: What does not make sense to me as a business owner, as just a logical individual.\
What does not make sense to me is this.

**\
Andrei Bosik** 39:14\
The.

**\
Val Levitan** 39:15\
The developer knows how to integrate.\
but does not know how to test. It doesn\'t make any sense. I think that the developer doesn\'t know how to integrate and doesn\'t know how to test. Our developers, our developers.

**\
Aaron Bockelie** 39:39\
I\'d like to direct you to the chat. I\'m kind of giving you some hints, Andrei, about how I would be thinking about this next.\
I think you already have some of the structure set up.\
but the contents can be adjusted.

**\
Andrei Bosik** 40:46\
If I correctly understand that your propose create actions in the repository which check this repo.\
If this rep contain, for example, documentation or something else.

**\
Aaron Bockelie** 41:03\
That is the output of it, but I need you to\...\
Something that Val has pointed out to me that happens with you guys is that you are very, very literal in taking exactly what I say and doing exactly what I tell you to do.\
And you will continue to walk off cliffs doing that.\
You\'re doing it right now.\
So what I\'m trying to get to you is that the key distinction is that the repo standards document that you started, we started at 4, we went to 5, now we\'re at 5.1.\
It will continue. It will eventually go to 5.2 and 5.5 and 6 and whatever in the future, not today.\
The standards.\
Is separate from the applied standards. Applied standards means the repo spec definition is its own thing.\
When it applies to a predominantly Spring architecture software repo, or predominantly a CI Terraform repo, or predominantly A TypeScript and React repo, there\'s going to be different.\
applied interpretations of what that means for each of these.\
Largely, they remain the same, but there\'s a lot of differences and nuances for every single implementation.\
And one of the things that you now have to think about is that there is an applied standard for even GitHub itself.\
Everything is code here, including GitHub, and the way it\'s defined.\
So when you say, Aaron, well, what you\'re saying is I need to make actions to do, enforce these things. Yeah, that\'s the output of it. But you have to, as kind of owner of CI and GitHub, you have to tell me not what your actions are, you have to tell me what your intentions are.\
So try telling me why, why would you make these actions?\
Try that first.\
Take a minute to think it over. Give me two reasons why you should make these actions happen.

**\
Andrei Bosik** 43:30\
So, to track that, we\...\
Mm.\
Way.\
Come, please.\
Simple shaming.

**\
Val Levitan** 43:48\
Agreement.

**\
Andrei Bosik** 43:49\
Agreements between Developers and GitHub owner, for example.

**\
Val Levitan** 43:55\
Contract.

**\
Andrei Bosik** 43:57\
Contract, yes.

**\
Aaron Bockelie** 44:02\
So\...\
A contract is put in place not to hold over somebody\'s head in violation of the contract. A contract is put in place to make sure there\'s mutual understanding of the outcome that\'s supposed to happen.\
Right.\
When I sign a contract to buy a house\...

**\
Andrei Bosik** 44:22\
Yes.

**\
Aaron Bockelie** 44:26\
Um\...\
The contract is a mutual understanding between the person I purchased it from and me about what we\'re going to be doing to get this house.\
Right.\
It has nothing to do with, well, you did all these things wrong when purchasing the house. It is the mutual outcome of both parties, not the other way around.\
Obviously, the other side is enforceable, but that\'s not the that\'s not the genuine goal.\
If you\'re going to create a contract around code ownership of repos, the goal is not to beat people over the head with it.\
The goal is to make sure that every repo has a caretaker.\
or every repo has somebody who will be concerned about that.\
And as soon as you phrase it this way\...\
You have a new interesting thing, a way to reward people for doing the ownership correctly.\
As soon as you can reward somebody for this by saying, this person has all of the obligations for repo standards covered. This person has one out of 20 of the items that I\'m identifying covered. Now you can rank them.\
them by order.\
And if you\'ve identified who is\...\
poorly owned and who is well owned, you can focus on the poorly owned ones to get them up to the better standard. And the ones that are well owned might be able to help the lessers and be rewarded for that in some way or otherwise\
give them the opportunity to run with whatever they\'ve built and continue. So what we\'re going is we\'re moving into what\'s called game theory right now.\
We\'re defining how the company or the org works in a way that gives people an opportunity to.\
prioritize this work because otherwise you can define all the standards you\'d like and nobody will care because they\'re not prioritized over the regular work that needs to get done.\
This is the governance aspect of this.

**\
Val Levitan** 46:54\
I.

**\
Aaron Bockelie** 46:56\
And one of the things that you can do with Claude and AI tools.\
is that you could make it extremely inexpensive from both a time and investment perspective to make them fit the pattern you\'re looking for.\
It collapses the time required to do so. When you ask, let\'s say that Evgeny has a code owner on a repo somewhere. And you say, Evgeny, this code only passes one of the 20 measures that are defined from our repo standards.\
So when Evgeny goes, yeah, that\'s great, but I got 100 other things I\'m doing.\
then you could say, all right, I have a small reward that I can give you for this in the term, in the way of\...\
actual compensation or changing how things work or whatever.\
In addition to that, we have defined explicitly that you can use tools like code to fix this in a much faster way than you would have normally taken to do this. Here are the recipes. Here are the applied standards that you can use to make changes to it.\
And you don\'t have to do it all at once. You can slowly build it into your work as you go overtime.

**\
Andrei Bosik** 48:19\
I have questions.\
When we speak about the owner, this is the one person in the repository or it\'s a no.

**\
Aaron Bockelie** 48:28\
No.\
It\'s several people, code owners. It can be 1 to several.

**\
Andrei Bosik** 48:31\
Several people.\
Okay.

**\
Val Levitan** 48:39\
In the former Soviet Union structure, these things don\'t work.

**\
Aaron Bockelie** 48:45\
Yeah.

**\
Val Levitan** 48:47\
There\'s no\...\
That there\'s no culture.\
Of mutual sharing, and it it it\'s absent, just like there is there is no culture about.\
Um\...\
Courtesy.

**\
Aaron Bockelie** 49:09\
Demystification.

**\
Val Levitan** 49:09\
sharing, courtesy, courtesy sharing of information.

**\
Aaron Bockelie** 49:14\
Yeah.

**\
Val Levitan** 49:16\
There\'s no such thing. People are very helpful, but there\'s no culture of sharing a task. It\'s not going to work.

**\
Aaron Bockelie** 49:28\
So, if at a minimum, you define one code owner.\
per repo, then that\'s your control.

**\
Val Levitan** 49:35\
So, one code owner will work.

**\
Aaron Bockelie** 49:38\
Yeah, you need to have at least one.

**\
Val Levitan** 49:40\
So each code, each repo needs to have a code owner. Okay, so I can wrap my mind around this thing.

**\
Aaron Bockelie** 49:49\
Game.

**\
Val Levitan** 49:50\
Then what?\
So how do we\... So then we say, okay, this repo must have a contract or\...

**\
Aaron Bockelie** 49:52\
Scism.

**\
Val Levitan** 50:01\
I, I don\'t, I\'m looking for the word.

**\
Aaron Bockelie** 50:04\
I, I\'ll let me let me define it.

**\
Val Levitan** 50:04\
or for integration. There has to be instructions for integration.

**\
Aaron Bockelie** 50:08\
So\...\
Each repo has to follow the standards that we\'ve defined here throughout the different sections.

**\
Val Levitan** 50:18\
But how do I, but how do I catch that it doesn\'t?

**\
Aaron Bockelie** 50:19\
And\...\
So what you can do is you can run tests.

**\
Val Levitan** 50:24\
How do I raise a flag? So there will be a, I don\'t know, Nathan will say, okay, I\'m cooperative, I\'m going to do it. This is my code.

**\
Aaron Bockelie** 50:26\
You can.

**\
Val Levitan** 50:34\
Ohh.\
Changes something, restructures, moves the code around, reconfigures the repos.\
and then implements it and here it goes, me, this one doesn\'t work and this one is greenlight. How do I do that?

**\
Aaron Bockelie** 50:57\
Hang on one second here.

**\
Val Levitan** 51:06\
This usually happens when Aaron says, there is no point interrupting Val, he is on attendant.

**\
Aaron Bockelie** 51:13\
The.

**\
Val Levitan** 51:36\
Evgeny, do you know how to do it?\
How would you build a set of rules that catches violations?

**\
Evgeny Kharetski** 51:51\
But he managed to.\
No more standard.\
Uh.\
Oh.\
Motion.\
Store, store, edit repository, yeah, I need.

**\
Alexander Biratko** 52:32\
Modern PSAT integration repository test.

**\
Evgeny Kharetski** 52:32\
What?

**\
Andrei Bosik** 52:34\
No action.

**\
Evgeny Kharetski** 52:34\
It was so impressed.

**\
Val Levitan** 52:39\
Yup, and you manage by much more, and integration.

**\
Alexander Biratko** 52:39\
No, would you please do it? Would you please do it?

**\
Evgeny Kharetski** 52:39\
No, would you please, would you please do it?

**\
Alexander Biratko** 52:45\
Yeah, no.

**\
Evgeny Kharetski** 52:45\
Yeah, it is actually was.

**\
Alexander Biratko** 52:51\
CA.

**\
Evgeny Kharetski** 52:51\
Yeah.\
It means music.

**\
Alexander Biratko** 53:00\
Uh, but standard on us or repository policy interface contract yet at contract. We did attack repository some post structure contract directory is what the key file.

**\
Val Levitan** 53:29\
You have to contract contract over it, crack in the grid road.

**\
Alexander Biratko** 53:29\
Vijayal.\
Southwest with nation Southwest to is standard. Standard. Standard. Standard. Standard.

**\
Evgeny Kharetski** 54:10\
Yeah, probably.\
Just familiar.\
Platform contract.

**\
Alexander Biratko** 54:27\
Contract.\
Support.

**\
Evgeny Kharetski** 54:41\
No.

**\
Alexander Biratko** 54:42\
Premier.

**\
Evgeny Kharetski** 54:44\
No, no, no.

**\
Val Levitan** 55:02\
Yeah.

**\
Andrei Bosik** 55:12\
No, to touch a relative.\
Image.\
No.

**\
Val Levitan** 55:21\
Can you, can you change, can you change the version to?

**\
Andrei Bosik** 55:21\
They get in there.

**\
Val Levitan** 55:27\
Can you increment the version, please?

**\
Aaron Bockelie** 55:37\
Who is changing the version? This should be matching the 5.1 that I\'m\...

**\
Val Levitan** 55:44\
Well, are you advancing 5.1?

**\
Aaron Bockelie** 55:47\
No, the change I just made earlier, so I started, I replied with five and I said I caught a few things, so I incremented to 5.1. And this is not, this is not a version of the standards. This is a companion document to the standards to be able to test everything.

**\
Val Levitan** 55:57\
And that.\
So, can you rename it then?

**\
Aaron Bockelie** 56:07\
Yeah, it\'s called Repo Standards 5.1 draft checks.\
Compliance checks, it\'s not it\'s not the standard stock.\
So this is sort of an idea of test cases, test ideas, Andrei, that you might be able to implement and manage per repo or essentially verify from a\...\
start of a governance repo area. I\'m not sure how you want to structure that yet.\
But this is essentially a set of checks that you can have.

**\
Val Levitan** 57:54\
Oh.

**\
Aaron Bockelie** 57:58\
Look for the manifest checks. Look for autonomy.\
Make sure you actually have unit tests. Make sure you have contract assertions.\
All these things.\
Basically, you\'re looking for code smell. You\'re looking for four patterns that don\'t fit.\
Did anybody know the\... Ohh, go ahead.

**\
Val Levitan** 59:35\
So, Andrei.\
No, no.

**\
Aaron Bockelie** 59:38\
I was going to ask, did anybody recognize the well-architected.github.com link? I\'ve mentioned it several times over our longer discourse.

**\
Andrei Bosik** 59:38\
Oh.

**\
Aaron Bockelie** 59:49\
Most of what we\'re talking about in the repo standards is this well-architected.github.com is essentially the larger, bigger picture of the applied standards for GitHub.\
So remember earlier in the chat, I was saying\...\
Have your repo standards document as the core, have a bunch of applied standards for different types of repos that\...\
are the applied intentions of that.\
And if you look at the well-architected.github.com site, it is a high-level enterprise-scale version of applied standards for GitHub.\
You can\'t adopt that directly for your company, Andrei, but you can.\
Take pieces from it and assemble your own understanding of applied standards for GitHub.\
And you can also add the other pieces that you want.\
You have a lot of the ingredients here to build what you need. You have to figure out what\'s the right way to structure this so you don\'t box everybody in and give them the ability, all the code owners, the ability to follow the conventions as well.\
If I could direct your attention to the appendix of that last sort of checks document that I shared.\
is this provides the structural evidence, not the actual, like, tangible, real thing.\
Structural evidence is what another, there\'s a phrase called code smell. Have you ever heard of the phrase code smell? There\'s a smell to the code.\
There\'s an odor.\
I\'m guessing no by the looks on everybody\'s faces.

**\
Andrei Bosik** 1:03:20\
No, no.

**\
Aaron Bockelie** 1:03:22\
Hey.\
When something smells off, what do you do? You probably don\'t eat it, right?\
When you look at code and you\'re like\...\
Why is this written this way? That code has a smell to it.\
Sometimes you just have to eat it anyway, but in many cases you can question or follow your intuition into reading what you think it does, and you go\...\
This has a particular flavor, odor, or smell to the way it reads.\
And I believe there\'s something incorrect. I can\'t put my finger on it exactly.\
That\'s kind of the thing that happens in my head, at least, you know, in English words. I\'m sure there\'s an equivalent functional equivalent in your primary language as well.\
And when you think this, you can use your intuition to dig into it.\
And so, what this\...\
This sort of checks.\
draft is about, this meta testing here, is to help understand and detect smell or a particular odor that might be being emitted from various repos.\
Not going to fix it. It\'s not going to tell you what\'s wrong with it. It\'s going to say, you\'re missing a lot of the patterns that we defined in the repo standards, and you need to investigate them.

**\
Val Levitan** 1:04:56\
You, you talk like a business owner, small business owner.\
Because you pay your own bills, you own your own code.\
you optimize your own distribution.\
Um\...\
But.\
I am not sure that it\'s going to work in distributed environment.

**\
Aaron Bockelie** 1:05:30\
So every code owner is actually a kind of a owner of their own thing. If it\'s a small business, it\'s a big business is a bunch of small businesses under the same umbrella, right?

**\
Val Levitan** 1:05:43\
in the ideal case scenario.

**\
Aaron Bockelie** 1:05:45\
In the ideal scenario.

**\
Val Levitan** 1:05:47\
But the world is not ideal.

**\
Aaron Bockelie** 1:05:49\
No.\
The only way we can get this to get functional is to define the ideal scenario.\
The other alternative is there\'s infinite alternatives here.\
is to not do this.\
Particular implementation and try something else.\
I just know that from my experience of governing a lot of repos.\
when there\'s 10s to thousands, 10s of thousands of repos.\
is that at a very large corporation, it\'s just a bunch of independent groups doing whatever they\'re doing in a very small organization.\
There\'s very few owners, but it\'s the same sort of thing. And those few owners assert a strong amount of control, a very strong control over those repos and have a very strong opinion.\
Instead of just being blase and letting it go get in, they\'re very picky about what actually makes their way into the repo.\
And, in the intermediate area, where there\'s\...\
10 to 50 part owners, let\'s just say.\
That\'s the dangerous area, which is exactly where you\'re at, because you have enough people to overwhelm a strong, strongly typed owner.\
and not enough people to be able to break up the pieces into small enough pieces to deal with.\
This is the danger area that you\'re sitting in for ownership of things.

**\
Val Levitan** 1:07:29\
Okay, too much philosophy.\
Developers.\
Andrei.

**\
Aaron Bockelie** 1:07:43\
Hmm.

**\
Val Levitan** 1:07:45\
Developers.\
Country.\
I would like to have a Andrei.\
I wanna have.\
A gate that does not let.\
Incorrect things through.\
Can I do it?

**\
Aaron Bockelie** 1:08:10\
Andrei needs to pick one of those developers for every repo. Not A one-to-one, but one developer could own 5 repos. I don\'t really care what the ratio is. And he needs to deputize them to make sure that they can uphold the repo standards that he\'s trying to uphold.\
Those people are the code owners.\
If Andrei is the actual sheriff, the elected sheriff.\
the sheriff of JVL\'s Git infrastructure, all of the repositories that Andrei you need.\
You need sheriff\'s deputies.\
who have been appointed as the owners of various repos, right? You\'re deputizing them.

**\
Andrei Bosik** 1:09:02\
Mhm.\
Yeah, I understand.

**\
Aaron Bockelie** 1:09:05\
And your deputies are the code owners.\
And their goal is to uphold your edicts, your definition of what you find it will be. The sheriff deputies follow your rules.\
And they\'re the ones that allow the regular developers to contribute or not contribute to the repos.

**\
Andrei Bosik** 1:09:20\
Ohh.\
How can I check?\
Uhh\...\
Not in each repository, globally.\
that code owners work is right.\
For my vision, I can create action.

**\
Aaron Bockelie** 1:09:45\
Take the\...

**\
Andrei Bosik** 1:09:50\
The section can build.\
Report, for example, and show me.\
Information about this repository contain documentation, this repository contain tests, for example, something else.

**\
Aaron Bockelie** 1:10:12\
Sure, did you look at the check strap?

**\
Andrei Bosik** 1:10:15\
Ohh.

**\
Aaron Bockelie** 1:10:19\
Open the checks draft.

**\
Andrei Bosik** 1:10:21\
What is check stuff? I don\'t know what is it.

**\
Aaron Bockelie** 1:10:21\
That.\
I just literally attached it. That was the last file I attached in the chat.

**\
Andrei Bosik** 1:10:29\
Ah, oh, okay, yeah, yes, I see, yeah, yeah, I see, I see you had questions by each part.

**\
Aaron Bockelie** 1:10:38\
And so, yeah, so these are the various understanding of what type of thing you\'re testing for. It may not be accurate perfectly. You need to, we need to go revise that or you need to go make sure it makes sense.\
But these are the things that you define and then your deputies go, oh, I think I can do that.\
and you say, I need the report for every single one of the repos you own every month.\
And then when you see the reports and they say that I\'ve only got about 6% of 100% passing, or I\'ve only got 10% passing, or I\'ve only got 50% passing.\
Now you have metrics that you can work against to help improve it.

**\
Val Levitan** 1:11:25\
That\'s the answer.\
That\'s the answer I was looking for.

**\
Aaron Bockelie** 1:11:30\
And do you know what all of this stuff is actually based on from a framework standpoint, Andrei? What 2 frameworks?

**\
Andrei Bosik** 1:11:40\
Mm.

**\
Aaron Bockelie** 1:11:40\
is all of this based on that you can use. As a sheriff, an elected sheriff, you have to enforce the standards, societal standards. And what are those societal standards? They\'re DORA.\
And they\'re calm.\
Those are the two standards that you\'re working on.

**\
Andrei Bosik** 1:12:02\
I know about Dora. What is columns? I don\'t know.

**\
Aaron Bockelie** 1:12:10\
Let me send you a link.

**\
Val Levitan** 1:12:18\
That\'s the answer, Andrei.\
This is what I was looking for.\
So, here\'s your undertaking.\
We\'re gonna meet again, and you\'re gonna tell us.\
Present us with a document similar to what Biratko wrote.\
on how are you going to test the repos?\
Constantly.\
Test the repos.\
In a in a circular motion.\
constantly test the repos.\
So, they do not stray from where we want them to be.

**\
Andrei Bosik** 1:13:07\
Mm.\
I have questions. Aaron say that people submit reports about their code owner sent to me a report about their repositories, but in my vision I need to self-check.\
Their repositories, because they can do it wrong or.\
Greater pressure.

**\
Val Levitan** 1:13:57\
But the most the Aaron.\
Is an.\
Idealist.\
Yeah.

**\
Alexander Biratko** 1:14:09\
We Elsa.

**\
Val Levitan** 1:14:09\
He\'s bordering, huh?

**\
Alexander Biratko** 1:14:11\
The Elsa.

**\
Val Levitan** 1:14:14\
Stop, stop.

**\
Alexander Biratko** 1:14:15\
Motoras.

**\
Andrei Bosik** 1:14:19\
Space he has managed to.

**\
Val Levitan** 1:14:19\
It doesn\'t work. It doesn\'t work in real life.

**\
Aaron Bockelie** 1:14:26\
You can\'t take all of these and just make it work in your organization.\
You have to take pieces of this and work it into whatever size it fits. That\'s what has to happen next.\
These things need to to.\
Inform your decisions. These are architectural styles of defining how you operate.\
This is like, so to Val\'s credit, I am talking about the ideal situation, right?\
Reality is a compromise and you can\'t build an ideal building or ideal structure. You have to build something grounded in reality.\
So if the very reality, the contact with reality is code that you can execute, then I would really, really recommend thinking about how are you going to actually measure that stuff in those repo standards, the compliance checks.\
What would you do to measure things to start with?\
O, let me give one.\
Tangible thing here.

**\
Val Levitan** 1:16:47\
Alexander, would you know how to\...\
If, if, if, if I asked you to build.\
A gate.\
Would you know how to do it?

**\
Alexander Biratko** 1:17:07\
Gate.

**\
Val Levitan** 1:17:09\
Gate.

**\
Andrei Bosik** 1:17:11\
For Artur.

**\
Val Levitan** 1:17:16\
Andrea.\
So, repository.\
Brian, I need.

**\
Alexander Biratko** 1:17:27\
Yeah.\
We also have no discussion.

**\
Val Levitan** 1:17:45\
The whip.

**\
Alexander Biratko** 1:17:52\
No.

**\
Val Levitan** 1:18:04\
Net, net, net, net.

**\
Alexander Biratko** 1:18:07\
Elite.\
At Crevide repository.\
No.

**\
Andrei Bosik** 1:18:33\
The planning structure is just design it, which prior.

**\
Alexander Biratko** 1:18:34\
Notes.

**\
Andrei Bosik** 1:18:49\
No, I don\'t look at it with me at the case.

**\
Val Levitan** 1:18:51\
He had a he had a repository.

**\
Alexander Biratko** 1:18:52\
Yeah.\
The.

**\
Val Levitan** 1:18:57\
On that.

**\
Alexander Biratko** 1:18:58\
Just.\
What?\
It was not very private.\
No, I can provide.\
Notifications now with me also on eating these meals.

**\
Val Levitan** 1:19:36\
Repository on near new compliant.

**\
Alexander Biratko** 1:19:44\
the test at any problem, which result at.

**\
Val Levitan** 1:20:06\
Yeah.\
No, my God.

**\
Alexander Biratko** 1:20:10\
Flag, flag is time, flag is time. What, what directory adds to it? We need documentation.

**\
Val Levitan** 1:20:20\
At the at the most now.\
Are going to my teachers\' skills?

**\
Alexander Biratko** 1:20:28\
The surprisilion urb nim viro y at nesti to is at a motion but near absolute no chatkologica to is nalice file documentation in the premier on nepus toy\
What, dear?

**\
Andrei Bosik** 1:20:51\
No, I thought it was the same.

**\
Alexander Biratko** 1:21:10\
Utah.

**\
Andrei Bosik** 1:21:13\
No, no, no.

**\
Alexander Biratko** 1:22:35\
But also.

**\
Val Levitan** 1:23:01\
Yeah.\
Yeah.

**\
Andrei Bosik** 1:23:05\
Those parents want to change, like, I need.

**\
Alexander Biratko** 1:23:13\
No, no, no. Repo standard checks draft.

**\
Andrei Bosik** 1:23:13\
No, Tamil.

**\
Val Levitan** 1:23:27\
Yeah.

**\
Alexander Biratko** 1:23:52\
It is symmetric.

**\
Val Levitan** 1:25:08\
Yeah.\
Yes.

**\
Aaron Bockelie** 1:25:33\
This last document is using the compliance data. Remember I was talking about the thermostat, overshoot and undershoot?

**\
Val Levitan** 1:25:41\
Yeah.

**\
Aaron Bockelie** 1:25:42\
That\'s what this is for.

**\
Val Levitan** 1:25:43\
BY.

**\
Aaron Bockelie** 1:25:46\
How do you actually take what we\'re measuring after we\'ve stuffed it into some sort of data structure, look at it, and go, well, we should do this with it, or we should make that decision?\
This is where having tools like Datadog or Prometheus or whatever, whatever your choice of time series data logging is, Andrei, this is where you can start to collect this over time and start to see the patterns that emerge from the team.\
I think that since this is just a first draft, it\'s pretty straightforward to dial in.\
The scope and scale of this, too.\
So, we\'re talking about something that\...\
Ultimately, you are responsible for Andrei.\
is what it sounds like from the number of people that we have to actually interact with. And so you are basically the person who is looking at all of these things and flagging them. I\'m kind of, in a way, redefining the way that you should be watching the status and quality of all these. And this also turns into potentially\
too much work for one person to do. Because I\'m asking you essentially to be more involved with every single repository and how it works.\
By being the sheriff, you have to have time to be the sheriff.\
So if we were to focus on Nathan\'s repo first.\
You would talk to Nathan and go, Nathan, I think you\'re the co-owner of your own thing. He would go, yeah, I probably am. And then you would say, these are the things I\'m looking to measure.\
Let\'s work together to come up with a way to measure them. I have an opinion on how I\'d like to set this up. I\'m going to start measuring them in GitHub this way. Are you cool with that? He\'s going to go, yeah, I have this stuff. None of it\'s going to be passing when you start measuring it. And you\'re going to say, okay, that\'s fine. Let me start collecting the measures.\
First, and then I\'m going to start asking you on it some sort of\...\
cadence, monthly, bi-weekly, whatever it is, I\'d like you to work on this metric because that makes it more important. That\'s the most important metric I want to focus on as the sheriff of all of the GitHub repos.\
So this turns into a set of goals for Andrei to try to chase.\
Andrei needs to now have an understanding that he is responsible for making these repos have these particular shapes to them, which is itself a type of quality management of the repos.\
I actually don\'t know whether you want to be doing this or not.

**\
Andrei Bosik** 1:29:56\
You have no choice.

**\
Aaron Bockelie** 1:29:58\
Well, there has to be a reason why you want to do it. You can be paid as much money as you want, but at the end of the day, if you sit down and look at this and go, oh my God, I hate doing this, it\'s not going to go well.

**\
Val Levitan** 1:30:14\
Well, he chose the profession, so obviously he likes it.

**\
Andrei Bosik** 1:30:15\
Up.

**\
Aaron Bockelie** 1:30:18\
Yeah, you love it.\
Give you all-you-can-eat buffet.

**\
Andrei Bosik** 1:30:21\
Yes.\
But, Aaron, I have one small question. I ask this question too well, but I not ask you. In your proposition, you say people need check.\
As a owner of this repository, this repository is\...\
Uh\...\
Um\...\
Ohh.\
correspondence to our standards and people need to use this metrics. I correct understand or second variant I need to check their repositories to

**\
Val Levitan** 1:31:04\
It\'s.\
Yeah.

**\
Andrei Bosik** 1:31:13\
Bonds to our standards using this matrix.

**\
Aaron Bockelie** 1:31:18\
If people do it, then you have to have a way to give them a pattern to follow. And you need to be able to follow up with them to make sure that you can enforce it.\
If you do it, you need to make sure you have sufficient time and also control of all the repos to make the changes to be able to do it.\
So, which control, what, what, what span of influence and control do you have, Andrei?

**\
Andrei Bosik** 1:31:41\
But.\
But I can use automatic tools, for example. I can create scripts that can check container repository documents test or something else.

**\
Aaron Bockelie** 1:32:00\
Certainly, of course, you\'re going to be using tools, but my question remains: when your tools report 0 compliance, what do you, how do you, what are you going to do?

**\
Andrei Bosik** 1:32:02\
Ohh.\
Send letter.

**\
Aaron Bockelie** 1:32:20\
A strongly worded letter.

**\
Andrei Bosik** 1:32:22\
Maybe, yes. Why not?

**\
Aaron Bockelie** 1:32:23\
And then when they ignore it, what happens next?

**\
Andrei Bosik** 1:32:27\
Hmm.\
It\'s a good questions, I don\'t know.

**\
Aaron Bockelie** 1:32:35\
So one of the things\...

**\
Andrei Bosik** 1:32:35\
Close access to this repository for him.

**\
Aaron Bockelie** 1:32:38\
No, because then you break the business. So try again.

**\
Andrei Bosik** 1:32:39\
Hmm.

**\
Aaron Bockelie** 1:32:43\
What can you do instead?

**\
Andrei Bosik** 1:32:47\
Your propositions.

**\
Aaron Bockelie** 1:32:49\
The beatings will continue until morale improves.\
That\'s one way to do it.\
You replace beatings with meetings, so the meetings will continue until morale improves. That\'s one way to do it. Another way is to\...\
Maintain control of release of the product.\
So if you have the ability to say, this doesn\'t follow any of our repo standards, and I have teeth, I have enforcement from Val and the company to say, I can delay the release of your product to this point until you have some sort of quality standards, is a control that you have.\
But you can\'t prevent it.\
It can be monetary.\
You can say that actually, you have to do all this work to get this out the door, because if we don\'t, we will be missing our quality bars for this. And you need to hire somebody or bring somebody in or spend some hours to make that happen.\
That\'s another way that you can kind of enforce it.\
Another way you can do it is you can just say, okay, give me some control of your repo because you\'re clearly incapable of steering your own repo.\
And so you take control of it and you make changes. And shame is the control. Basically, you\'re just overriding their decisions and taking control of it. But that\'s dangerous because they might just give up and, okay, Andrei, you do it.\
So there\'s different patterns and anti-patterns to controlling this that you can do.\
In larger companies, you do it economically. You actually prevent bonuses from occurring or you demote people or whatever. In small companies, it\'s much more personal. And so you have to be able to talk to the other person and say, I just need to get this working so we can hit our minimum standards. Because if we don\'t, we all know collectively what\'s going to happen.\
It\'s all going to turn into mush.\
Trying to get out of the mush.\
No, what mash borscht. We\'re trying to get out of the borscht. That\'s what Val was using the other day.\
And so that\'s kind of\...\
probably the best control you\'ve got.\
It\'s a social control of saying, if we don\'t do this, we\'re going to be stuck, doomed to doing this this way for forever, and it\'s hard.\
And you have to clearly indicate what happens when you don\'t do this anymore. You have clarity, you have demystification of what\'s going on. You can actually see how things are operating and so forth.\
And by picking one project, Nathan\'s project for example, as a starting point, you can prove and show what happens when done correctly.

**\
Val Levitan** 1:35:48\
But I like the position, meetings will continue until you change.

**\
Aaron Bockelie** 1:35:53\
Right.

**\
Val Levitan** 1:35:54\
It\'s demoralizing when you continuously meeting with the same guy and saying, dude, hey brother, you either extremely stupid.\
Or are you extremely arrogant?\
Both cases just don\'t work for us.\
We\'re looking for happiness here. We explain to you how to do your \*\*\*\*.\
You keep on insisting and ignoring us, all of us. You\'re starting to influence our happiness in the company.\
Dude, maybe you should go and look for another job.

**\
Aaron Bockelie** 1:36:32\
Right.

**\
Val Levitan** 1:36:33\
Eventually, that\'s the message, right?

**\
Aaron Bockelie** 1:36:36\
Yeah, that\'s the shame message.

**\
Val Levitan** 1:36:39\
I mean, I keep on meeting with you, and meeting with you, and meeting with you, and meeting with you.\
It seems like you\'re not stupid, well-educated, right?\
So that means you\'re arrogant and you just ignore all of us.\
Because we all decided, I mean, this is a good way for us. We like what we\'re doing here.\
And our families depend on this.

**\
Aaron Bockelie** 1:37:13\
The social pressure angle is probably the best one you\'ve got, Andrei.

**\
Andrei Bosik** 1:37:21\
Okay, I think yes.\
It\'s a good idea.

**\
Aaron Bockelie** 1:37:27\
And, and I want you to make sure, like, practice this with me right now.\
We\'re doing this together because we collectively understand that if we do it together, we will actually make our experience more pleasurable to do the work that we want to do, rather than be trapped in managing all of the micro frictions of every single thing we do every day.\
And the only way we get out of the pit, out of the sand pit, is by being deliberate and putting energy in one direction, which is what this standard thing represents.

**\
Val Levitan** 1:38:13\
Let\'s.\
Create a guiding document.\
For our next meeting, Andrei, that\'s your undertaking.

**\
Andrei Bosik** 1:38:25\
Yes, I understand.

**\
Val Levitan** 1:38:27\
a guiding framework. I want to see a framework of how you are going, you, Andrei, not anybody else, not me.\
How you will manage it on a daily basis?\
So then what we will do when you create that framework, we are, we, all of us, mainly the three of you, will present it in the company and say, we.\
came up with this. This is the framework of how everything will be organized. And this is the framework, how it\'s going to be controlled.\
And I\'m going to put in my reliance on you.\
to make everybody\'s job easier. So that\'s what you need to do in your own repo, because you are the owner of this repo.\
We want to have one person per repo, not multiple. Multiple don\'t work.\
So, start the signing.\
You guys, the three of you, should start pushing, assigning who is the owner for each of the repos that we have.

**\
Aaron Bockelie** 1:39:43\
I\'ll tell you why I think this works, Andrei. It works because people like to be given a list of things to do.\
People ultimately like to be said, told, and promised that if you do these things, you\'ll get these rewards.\
And people like to just know what actually is meaningful to get accomplished.\
This is a universal human thing. I don\'t care what language you speak. People enjoy and crave the ability to have meaning and purpose in whatever they\'re doing.\
And what we\'re defining here is the structure and architecture to have meaning and purpose to get these things done this way.

**\
Andrei Bosik** 1:40:33\
Okay, uh, what do we\...\
To the next meeting, we want to have guide.

**\
Val Levitan** 1:40:40\
We, we, we, we, we are accepting the framework that has been summed up in version 5.1.\
We, we are now.\
Yes, we we are now.\
Diverting our attention to a management framework.\
that makes our job st, meaning on a daily basis we could have our sanity.\
As well as creates a standard JVL standard for how everybody should work.

**\
Andrei Bosik** 1:41:31\
OK, for me, it\'s clear.

**\
Val Levitan** 1:41:32\
The moment your framework, the moment your framework is ready.\
You?\
Andrei, Evgeny, and Alexander, you will present this in Minsk.\
And collect input from everybody.\
But their input is\...\
I mean, we\'ll consider it, but if their input is, you know, I\'ve never worked this way and I don\'t think it\'s going to work or I\'ve never worked this way and\...\
that this sounds stupid, then I mean I don\'t consider it to be input. It\'s just, it\'s irrelevant.\
But if the input is, Luke, I\'ve tried it, and how do we resolve this inconvenience? That\'s a great input. Let\'s analyze it. Let\'s look at it.\
So, if the remark is stupid, then we just dismiss it, but if the remark is smart, we\'ll address it.\
But regardless, we\'re moving in that direction plus minus small deviations.\
So we now know how to organize it. Your next chore, your undertaken for next meeting, which is a week from today, next Friday.

**\
Aaron Bockelie** 1:42:41\
Here, yeah.

**\
Val Levitan** 1:42:53\
is to create a framework for management control.\
Agreed.

**\
Andrei Bosik** 1:43:05\
Yes.

**\
Val Levitan** 1:43:06\
Okay, I\'ll set up a meeting for next Friday.

**\
Evgeny Kharetski** 1:43:10\
Unless we had never had to go.

**\
Val Levitan** 1:43:13\
Ah, sorry, next Thursday.\
Is that okay, next Thursday?

**\
Andrei Bosik** 1:43:21\
Mhm.

**\
Aaron Bockelie** 1:43:21\
Yeah.

**\
Val Levitan** 1:43:23\
Okay.\
Thank you very much. Thank you everyone. Aaron, thank you. Hope you\'re feeling better.

**\
Aaron Bockelie** 1:43:26\
Alright, thanks guys.

**\
Alexander Biratko** 1:43:28\
Yeah.

**\
Aaron Bockelie** 1:43:29\
Thanks, bye.

**\
Evgeny Kharetski** 1:43:30\
By.

**\
Val Levitan** 1:43:30\
Butler.

**\
Andrei Bosik** 1:43:30\
Yeah, bye-bye.

**\
Andrei Bosik** stopped transcription
