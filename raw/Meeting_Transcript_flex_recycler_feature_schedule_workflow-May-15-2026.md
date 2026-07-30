**Flex_Recycler Requirements Working Session-20260515_080123-Meeting Recording**

May 15, 2026, 12:01PM

49m 55s

**\
Val Levitan** started transcription

**\
Andrei Klimovich** 0:03\
Maybe we shall probably arrange a different meeting for that.

**\
Juan Martinez** 0:08\
That\'s up to you. I good morning.

**\
Irina Shishko** 0:08\
Good morning.

**\
Andrei Klimovich** 0:09\
Good morning.

**\
Juan Martinez** 0:12\
Val, did you want any updates from last night to Gomoa meeting or should that be a separate call?

**\
Andrei Klimovich** 0:19\
Well, excuse me, you\'re on mute.

**\
Juan Martinez** 0:22\
But we read your lips separate call.\
Yeah.

**\
Alexander Biratko** 0:34\
Was close to location.

**\
Andrei Klimovich** 0:40\
Yeah.

**\
Alexander Biratko** 0:43\
It seems Podvoiski was mute.

**\
Irina Shishko** 0:46\
Mhm.

**\
Alexander Biratko** 0:48\
It was not about that.

**\
Andrei Klimovich** 1:01\
Regarding the update, meanwhile, so the major update was about this initiative, if those gift cards can be used in ATM, which actually is the next step to real cash out, right? And everything is on hold right now.

**\
Juan Martinez** 1:17\
Yep.

**\
Andrei Klimovich** 1:22\
Because they wait for mid-term elections, they wait for how it will all turn out with it.

**\
Juan Martinez** 1:28\
Sure, yeah, let\'s leave that for a separate conversation.

**\
Andrei Klimovich** 1:29\
Yeah, Igor.\
Yeah, okay, okay, okay. So from my side, like I have this task regarding finalizing capabilities and turning them into requirements. As I\'ve written as an update, we are prioritizing player facing capabilities first. So we need to make sure that the whole\...\
a flow of a player is covered. And right now I have only three capabilities left, which are minor capabilities mostly related to edge cases, while the rest of them already described. So we got all the requirements and use cases for them.\
From my side, there was one major requirement related to PIN generation, and actually\...\
I\'m just thinking that maybe I\'ve designed it not in the proper way. Let me share.\
So yeah, I will definitely let Alex do an update. No problem. Just let me discuss one requirement, which is a cornerstone of player experience. And we can, after this, switch, because I need your feedback, guys, to understand if I\'m moving in the right direction or not.\
Um\...

**\
Alexander Biratko** 2:58\
The.

**\
Andrei Klimovich** 3:01\
I don\'t know if you can see my screen.

**\
Juan Martinez** 3:03\
Yep.

**\
Andrei Klimovich** 3:04\
Okay, cool. So the pin generation, I was thinking about minimizing the friction as much as possible. So I suggested an idea that the pin code will be generated automatically and we will just display it to a player so he doesn\'t need to spend time inputting it and confirming it.\
But I\'m not really sure if it\'s the best solution. So on one side, we are cutting the corner with player activity, but on the other side, maybe it\'s not the best behavior. What do you think?

**\
Juan Martinez** 3:37\
Yeah, I would think it\'s not the best behavior because remember, the player has to enter the pin when they come back to FlexPay to cash out. So I remember my birthday. I remember my wife\'s birthday. That\'s usually the pins I use. If you\'ve given me a pin and I had two beers,

**\
Andrei Klimovich** 3:46\
Right.

**\
Juan Martinez** 3:55\
I might forget that pin, and then what?

**\
Andrei Klimovich** 3:57\
No.\
Yeah, right. So yeah, I will redesign it. Thank you for the feedback. I will just rewrite it and it will be a very straightforward flow over here. So the player will be asked to input pin and confirm pin. Okay.

**\
Juan Martinez** 4:02\
Okay.\
Okay.\
Perfect.

**\
Andrei Klimovich** 4:17\
So, Alex, please.\
Continue.

**\
Alexander Biratko** 4:23\
Where is Val Levitan?

**\
Juan Martinez** 4:25\
I\'m sure Val is rebooting his computer.

**\
Irina Shishko** 4:26\
Oh.

**\
Alexander Biratko** 4:28\
Val.\
Oh.

**\
Andrei Klimovich** 4:39\
Player activity.

**\
Irina Shishko** 4:48\
So.

**\
Andrei Klimovich** 4:49\
Da da da.

**\
Irina Shishko** 4:55\
I\'m still plus Matthew.\
Sood.

**\
Andrei Klimovich** 5:09\
Well, I think that there is a recording in place, right? So we are doing the recording both video and audio, so we will share this recording with Val.

**\
Juan Martinez** 5:17\
That\'s correct.\
Yeah.

**\
Andrei Klimovich** 5:20\
I suggest to continue because I have only this hour and after that I need to go to other meetings. So let\'s go on.

**\
Alexander Biratko** 5:21\
Okay.\
OK, no translate.

**\
Val Levitan** 5:40\
Minasa.

**\
Irina Shishko** 5:42\
Val.

**\
Andrei Klimovich** 5:42\
No.

**\
Juan Martinez** 5:42\
Yeah.

**\
Alexander Biratko** 5:43\
No.\
All the speech.

**\
Val Levitan** 5:46\
I would like, I\'m sorry, I just, I apologize.\
We must stick with the agenda. Must. So no other conversations, please. I would like to understand if based on the capabilities that has already been generated, have already been generated, and we have plenty of capabilities right now. I want to make sure, I want to make sure\
I want to be 100% sure that Alex can generate features.\
And that these features could be traced, so we could have a set of features to a capability.\
To a set of requirements to use cases.\
I must have it.\
Laser precision.

**\
Alexander Biratko** 6:47\
OK, no.\
Capability, feature, requirements, user cases, meeting, Andre, capability, and Andre.

**\
Val Levitan** 7:10\
No problems.

**\
Alexander Biratko** 7:12\
Andrei.\
The deal all what 3 capability? Ocean, Padrovna, Mosni.\
He polishes its capability, a pisson or not in a future me. Stalis, Nisk capability, Andrea.

**\
Val Levitan** 7:48\
So I see another problem and I want to underline this. Andrei may create capabilities.

**\
Alexander Biratko** 7:49\
No.

**\
Val Levitan** 7:59\
Knowing.\
the subject well or imagining the subject well.\
There is a difference between knowing and imagining.\
I want to make sure that all capabilities that have been created by Andrei have been run by me.\
End by one.\
Because I don\'t believe that Andrei knows the subject.\
Yep.\
Okay, so we need to make sure that these capabilities are true capabilities.\
But what we\'re discussing now is that we want one capability to many features, and those many features to\...\
Isolated repo.\
And that repo is\...\
Programmed by Cloud Code.\
That\'s the chain that I want to see.\
So let\'s focus, give me one capability, multiple features, to one repo, and I want to see Cloud Code programming.

**\
Alexander Biratko** 9:38\
Repository, repository, repository.\
What is, yes, yes, point review?\
Store.\
What? So, just move what we do. So, if features a piece on it, but almost an issue, no chest, the chest was more.\
What?

**\
Val Levitan** 10:25\
Okay, so let\'s discuss something else.

**\
Alexander Biratko** 10:30\
Oh.

**\
Val Levitan** 10:30\
Features must have acceptance criteria.\
Features, features.

**\
Irina Shishko** 10:36\
Mm.

**\
Val Levitan** 10:38\
And requirements must have acceptance criteria.\
Not capabilities, so a set of features will close the capability, and the capability.\
Goes away.\
Requirements do not go away and are reusable and are testable.\
So when Sasha will say capability is done, I will ask Andrei.\
Go ahead and test it.\
And Andrei will say, I tested and I confirm that the capability may go away. It\'s closed.\
Can we all agree to this condition?\
On another hand, on another hand, I will ask Irina to run.

**\
Alexander Biratko** 11:32\
Yes.

**\
Andrei Klimovich** 11:32\
Yes.

**\
Val Levitan** 11:40\
And I\'m specific, I\'m being specific now. I will ask Irina to run to run end-to-end testing.\
I will insist that end-to-end testing run in automated format.\
Maybe not from the beginning, maybe not from the start, but I will be pushing for end-to-end testing to be run in automated regime.

**\
Irina Shishko** 12:03\
Yes.\
Yes.

**\
Val Levitan** 12:10\
So, when Andrei says\...\
I agree.\
Complies, no issues.\
Irina, at the same time, will be running end-to-end testing with no failure. This is what we consider capability is done.\
Can we agree to that?

**\
Irina Shishko** 12:32\
Okay.

**\
Alexander Biratko** 12:32\
Yes.

**\
Val Levitan** 12:34\
Fantastic. Okay, so now all we need to do is to accelerate.

**\
Andrei Klimovich** 12:42\
Yes, so from my side, I have the whole next week. It will be partially required from my side to help in Texas Expo preparations, but my role is minor over there, so I\'ll have enough time to finalize everything. And you\'ve also mentioned, Val, that you\'d like to make sure that those capabilities are based on knowledge.

**\
Alexander Biratko** 12:43\
Thanks.\
Very.\
Going.

**\
Andrei Klimovich** 13:05\
So all caps are right now in Jira, so you may go and read through them and there is a cross-links to.

**\
Val Levitan** 13:11\
I can, I can, I cannot, I cannot, I don\'t have physical.

**\
Andrei Klimovich** 13:16\
Yeah, yeah, sure.

**\
Val Levitan** 13:17\
capacity to read every capability. It\'s on you, Andrei, to make sure that you are in constant discussion, especially with one.

**\
Irina Shishko** 13:25\
I.

**\
Alexander Biratko** 13:28\
Okay.

**\
Val Levitan** 13:28\
especially with one, on how do you interpret capability? Humans will remain humans. We\'re not digital people. We have colors. We have interpretation. We have colors. I want to make sure that the way you, Andrei, understand capability,

**\
Andrei Klimovich** 13:38\
Mhm.

**\
Val Levitan** 13:49\
is the same that one understands capability.

**\
Alexander Biratko** 13:50\
Yeah.

**\
Juan Martinez** 13:54\
Yeah.

**\
Andrei Klimovich** 13:54\
Okarak.

**\
Val Levitan** 13:54\
Because we\'re because we\'re human, we we have room for interpretation and slight interpretation to degree.\
Um\...\
What do you call it?

**\
Juan Martinez** 14:09\
Yeah, just a different view of it. But I mean, but again, since we define the capability as the highest level, so it\'s the simplest level, i.e., you know, the flex recycler must accept money or must have a bill acceptor. That when we keep it to that level, it\'s very hard to

**\
Alexander Biratko** 14:25\
Okay.

**\
Juan Martinez** 14:31\
to not to have an incorrect capability because we agree that it must have a bill acceptor as an example.

**\
Andrei Klimovich** 14:34\
Yeah.

**\
Val Levitan** 14:37\
You\'re right. You\'re right. And it\'s a good point.

**\
Andrei Klimovich** 14:38\
Yeah, well, it\'s a good, it\'s a good point, but requirements requirement is where the drift happens.

**\
Juan Martinez** 14:45\
Oh, of course, of course, yeah.

**\
Val Levitan** 14:47\
Exactly, Andrei is right, and so we use requirement in use cases to narrow capability to a\...

**\
Juan Martinez** 14:48\
Yeah, yeah.

**\
Alexander Biratko** 14:52\
Ohh.

**\
Val Levitan** 14:55\
To an exact interpretation.

**\
Juan Martinez** 14:58\
Yeah.\
So Andrei, other than Tuesday of next week, I\'m good the rest of the week. Tuesday, I\'ve got a doctor\'s thing.

**\
Andrei Klimovich** 15:08\
Yeah, sure. So let\'s do that on Monday, because today I will be back to fields and yeah, on Monday. But you can go through those caps that I\'ve shared in our common chat. You can see what is done, what is considered to be done, and feel free to get feedback.

**\
Juan Martinez** 15:13\
But.\
Absolutely.\
Sure.\
And then\...

**\
Andrei Klimovich** 15:27\
Sood.\
Oh, may I ask you a question while, like\...\
The moment of prioritization, the moment when we will\...\
form our release versions. When does it happen? Because from product point of view, I may have my vision of MVP, for example, my vision of version one, version two, et cetera. When does it happen? When do we prioritize?

**\
Val Levitan** 15:53\
At the point, at the point of scheduling.

**\
Andrei Klimovich** 15:57\
Okay, and\...

**\
Val Levitan** 15:58\
So, so what happens next? Uh, Alex and Pavel must schedule, so\...\
Sasha Will.\
lay out all of the features with acceptance criteria. Irina is looking at these features and says, well, I mean.

**\
Andrei Klimovich** 16:13\
Mm-hmm.

**\
Val Levitan** 16:21\
I don\'t have everything automated yet. I will need time to test it.\
So, she writes for test cases.\
She groups them into test suites.\
She aligns them.\
with a certain pace that Sasha lays out as his development priority. Pasha looks at the development priority and says, well, I have issues with resources. I, you know, I need, for example, Sasha\'s attention on another project because this is my priority.\
I push overall priorities. I am the only authority to push the overall priority, to set overall priority. So when I said this is more important than that, Pasha then says, well, I need resources here and I need resources there. So then Sasha says, well, I can only work 8 hours a day.\
Obviously, you understand. So then my schedule here stretches.\
Okay, so there is negotiation, internal negotiation, and we all compromise and arrive to a certain schedule. When that schedule is presented, you then Andrei say, okay,\
but I need it for such and such date, then let\'s scrub this capability.\
For now, it\'s not going to be MVP.\
But one, 5, and seven.\
Will be an MVP.\
For such and such date.

**\
Andrei Klimovich** 17:59\
Okay, I got it. Makes sense.

**\
Val Levitan** 18:04\
Of course, we all try to kind of\...\
We will want you to succeed. You want another project to succeed. The overall goal is to have\...

**\
Andrei Klimovich** 18:10\
Yeah.

**\
Val Levitan** 18:16\
You know, symbiotic.\
company that functions as, you know, human normal company. So obviously, we\'re not idiots. We will take your suggestion to what you think MVP is, and maybe that will stimulate reprioritization of some other projects.

**\
Andrei Klimovich** 18:39\
So I have another question, like when features are being created by Alex, is it also part of my involvement to read through those features, right? Just to make sure that Alex understood my requirements correctly. But the problem is that I may not be skilled enough to understand.\
technical features, right? Because so is it a\...

**\
Val Levitan** 19:04\
I don\'t believe that it. I don\'t believe that it\'s a practical thing for you to do. I\'m open to exposing you to it, but from my experience, it\'s not a very practical thing.

**\
Andrei Klimovich** 19:04\
How do you say that?\
Okay, so let\'s keep it on our communication level with Alex. So if you have any doubts, you\'re not sure if you understand certain requirement properly, just it\'s better to ask twice before, you know, making it a feature. Okay.

**\
Val Levitan** 19:34\
I am opening lines of communication. My job is to introduce people to each other, make it a comfortable work environment, and have people directly communicating to each other.\
And by doing that, I am hoping that\...\
It will remove a lot of\...\
Misunderstandings, especially in written communication, but\...\
Nothing is perfect.

**\
Andrei Klimovich** 20:13\
Yeah.

**\
Juan Martinez** 20:14\
So I think so as we just revisit and regroom all the capabilities next week, Andrei, I think as we\'re done with each one, it\'ll make Alex\'s life easier. If we tell him, hey, capability one is ready, please start looking at it, then two, then three. Just if we give him a list, it just makes it easier for him to target.\
the capabilities we\'ve already groomed and reviewed.

**\
Andrei Klimovich** 20:39\
Ohh yeah, we actually we are currently doing that, so we are sending Alex updates, so this set is ready. Please take a look.

**\
Juan Martinez** 20:42\
Yeah.\
Yes, absolutely.

**\
Val Levitan** 20:48\
I can tell you, I would like to share something with you. This week I was working on a different set of, a different initiative. And that initiative had to do with material management in\
in our ERP system. And we have a different developer who looks at the at providing this material requirement report to our procurement department.\
And so I personally\...\
Spend a lot of time developing user profile, so the procurement manager as a user profile and the manufacturing manager is another.\
user profile. And so by spending a lot of time and actually digesting every single verb and adjective and really polishing user profile, I then\...\
Set Claude in motion to develop.\
Set of.\
Ohh.\
requirements and capabilities.\
for the developer to develop the proper MCP.\
for material requirement.\
And I could tell you that I had the most\...\
Productive experience through Claude.\
Moving through use cases.\
to requirement, to capabilities. Of course, the, you know, human.\
Interaction is needed, but the experience was quite smooth.\
And by delivering tight set of capabilities with tight set of requirements, where we pay attention to every single verb and adjective in it.\
The set that the quality of this job was such a good job that developing features through Claude, we just flew through it.\
It was quite easy. I think that knowing, Andrei, how meticulous you are in writing requirements and capabilities, I think you\'re making Alex\'s job very, very easy.

**\
Andrei Klimovich** 23:21\
Hope so.

**\
Val Levitan** 23:24\
Alex, did you have a good experience writing features based on capabilities and requirements?

**\
Alexander Biratko** 23:29\
Yes.\
Yes.\
If, if requirements good, feature is good.\
Yeah.

**\
Val Levitan** 23:37\
I, I actually think I actually think it opens up a new.

**\
Andrei Klimovich** 23:38\
Okay.

**\
Irina Shishko** 23:38\
B.

**\
Val Levitan** 23:47\
opportunity for a company like JVL to excel by\
Empowering.\
a product owner, a product manager.\
It will have direct effect on the quality of code.

**\
Andrei Klimovich** 24:10\
So, Juan, when you will get a chance to look through those caps and requirements, please take a look at open questions, right? So when I work on requirements, there are a lot of things coming up, like ideas and questions that cannot be addressed.\
at the moment. So those section with open questions is very important and may be a source for new requirements or maybe a source for changes or any, you know. So it\'s very important that you take your time to look to them.

**\
Juan Martinez** 24:44\
Yeah.\
Absolutely. The capabilities don\'t have a proper sorting mechanism. Did you tag everything related to the recycler with something?

**\
Andrei Klimovich** 24:57\
Yeah, so basically the best way is to go through caps. So all caps related to recycler are tagged with flex recycler label. And then you go through cap. When you open the cap, you can see all requirements related to this cap linked. So you just go one by one.

**\
Juan Martinez** 25:06\
Okay, perfect.\
Yeah.\
Yeah, no, absolutely. I just wanted to know what filter to use. So flex recycler.

**\
Andrei Klimovich** 25:20\
Yeah, and actually it\'s a good point about the label for.\
for the requirement, because when I create a requirement manually in Jira, there is no field called label. I cannot set a label. I don\'t know why it\'s just hidden or whatever, but I\'ve set up an automatic Jira requirement transfer from Claude.\
So when I polish a requirement, I\'m ready for it to be posted in JIRA. I\'m doing this through Claude. And when I\'m doing this through Claude, I can set up a label.\
which I cannot do manually.

**\
Juan Martinez** 25:58\
I have.\
On the requirements, there\'s a second.

**\
Val Levitan** 26:00\
The don\'t don\'t let labels. I just want to tell you that labels is not a good thing in Jira.\
I, I in.\
I\'m trying to avoid using labels as much as possible. I encourage people not to use labels. The better way is probably use of component. So I think recycler should be a component.\
I\'m checking, I\'m checking with with IT. I\'d like to make it a component in Jira. Let me let me just while you talk while you\'re talking, let me let me address this issue.

**\
Andrei Klimovich** 26:32\
Mm.\
Okay.

**\
Juan Martinez** 26:38\
And also, on\...\
Sure, let me just share my screen real quick. So, um\...

**\
Irina Shishko** 26:43\
Oh.\
Companions, companion, yes, requirements of.

**\
Juan Martinez** 26:49\
Yeah, so.\
Yeah, so if you go to the requirements categorization, you know, the gaming sector, at least transactional, is something I use to filter. So all products related to transactional, and I tagged these. Even when you finished yours, I went back and tagged it. If I miss any, I\'ll make sure. But, you know, we do have a couple of hard-coded tags in here where\...\
You know, this is column, it\'s skill-based, it\'s land-based, it\'s transactional. So I use transactional to define all transactional products, and that\'s a filter that\'s readily available.

**\
Irina Shishko** 27:17\
I.

**\
Juan Martinez** 27:26\
Just so you know.

**\
Andrei Klimovich** 27:28\
Okay.

**\
Val Levitan** 27:28\
How did you use transactional as a component?

**\
Juan Martinez** 27:32\
Well, I mean, currently it\'s under the gaming sector. I don\'t see the word component itself anywhere today under the requirements tab.

**\
Irina Shishko** 27:33\
Right.\
Pop.

**\
Val Levitan** 27:41\
Let me, let\...

**\
Andrei Klimovich** 27:47\
Mhm.

**\
Val Levitan** 27:47\
Like, bottom, bottom right, bottom right.

**\
Irina Shishko** 27:48\
Huh.

**\
Juan Martinez** 27:50\
Ah, okay.

**\
Val Levitan** 27:53\
Bottom, yeah, yeah, yeah, up, up.

**\
Juan Martinez** 27:55\
Okay.

**\
Val Levitan** 27:58\
So we just need to make it a component.

**\
Juan Martinez** 28:02\
The.

**\
Val Levitan** 28:03\
I need to again re-log into Teams. It\'s got the Microsoft drives me nuts.

**\
Irina Shishko** 28:12\
Ohh.

**\
Andrei Klimovich** 28:16\
Oh yeah, so I\'ve just checked a filter and then indeed you can filter by component, so no problem with that. So yeah, it might be used.

**\
Juan Martinez** 28:22\
OK.\
Perfect.

**\
Irina Shishko** 28:25\
Andre Label, yes, City Hotel, yes, we meta, what time with your details, general requirements.

**\
Andrei Klimovich** 28:26\
Mhm.\
Uh-huh.\
Are you, are you?

**\
Irina Shishko** 28:51\
Mhm.\
Just.

**\
Andrei Klimovich** 29:01\
OK.

**\
Irina Shishko** 29:03\
Uh huh.

**\
Andrei Klimovich** 29:04\
Okay.

**\
Irina Shishko** 29:09\
What is child of?

**\
Andrei Klimovich** 29:16\
I think it was somewhere.

**\
Irina Shishko** 29:24\
With Elizabeth, what we should say about.\
On child of.\
No, yeah, no, yeah, she is me, but almost structure product requirements, but I guess.\
Yuri.

**\
Andrei Klimovich** 30:13\
Flex recycle parent on the.

**\
Irina Shishko** 30:15\
This is.

**\
Andrei Klimovich** 30:25\
OKOK, open.\
That shows the little crucial.

**\
Alexander Biratko** 30:58\
Yes, we come to know.\
Сказать клубы, ну я обычно куда фичи писал. Я ему говорил о том, что.\
Пиши более понятным языком, ну там без спец терминов.\
Без длинных ссылок там и так далее, и тогда он писатель начинает писать более.\
Более хорошо.\
А если Так вот сам, Ну вот ты сам зайди попробуй вот прочитать. Ну насколько она сложная языком написана? Она действительно, ну, чтобы разобраться, нужно долго вникать. Ну либо с помощью Клода пытаться это прогнать. Ну вот это вот небольшое замечание.

**\
Val Levitan** 31:47\
Ага и mickoda awawaskill.\
Процесс коммьюникет waters the to praidrear.

**\
Andrei Klimovich** 31:58\
Угу.

**\
Val Levitan** 32:01\
Саша IM fully innagreement we watersange i fu lo low clood you what sorry fielsof fie.\
Achest runds willd.\
Эцлмас like it irsa despplea of fancey worry ac lick onesin of.\
Say \*\*\*\* that nobody can read.\
So I have a skill, you know, communicate to me like a, like I\'m a, like I\'m an idiot.\
And I like it to be a rule through the company. Just say it simply, I don\'t need PowerPoint presentations. I don\'t need fancy wording. Just get to the point within first three sentences.

**\
Andrei Klimovich** 32:36\
But\...\
Yeah, it\'s a good point. So I got this film too, but\...\
Uh, it\'s a balance, it\'s a balance between, you know, trying to cover the requirements, yeah.

**\
Val Levitan** 32:57\
I, I, but there is nothing, Andrei, nothing to balance. Andrei, I\'m telling you 100%.\
Trust me on this.

**\
Andrei Klimovich** 33:09\
But.

**\
Val Levitan** 33:11\
Put a prompt in there, your communication on all subjects must be in very simple wording. Whatever.\
However, you want to simplify your communication, but it has to be simple. I agree with Sash 1,000,000 percent.

**\
Andrei Klimovich** 33:26\
Okay.\
Yeah, sure. Let me let me try, not not try, let me rerun a couple of requirements that have already been done and to see how it may be changed. OK, good point. Thank you.

**\
Val Levitan** 33:36\
Thank you.\
Good point.

**\
Alexander Biratko** 33:50\
requirements I didn\'t specialist. No problem with projected. Yes, because I can.\
Thank you.

**\
Val Levitan** 34:20\
Wonderful point. Let\'s embrace it, please.

**\
Andrei Klimovich** 34:24\
Okay, do.

**\
Alexander Biratko** 34:28\
Ну ещё, если опять же, как к пониманию этих вещей, в клод создаёт много ссылок на другие рекларименты, и чтобы понять этот реклаймент, приходится очень много прыгать на другие, хотя он мог бы вместо этой ссылки.\
Дать простое описание, потом 23 словах, что он имел ввиду.\
Да ну первым пишет, что чтобы, но обеспечить требования.\
И ссылка да идет ссылка на другой, он бы мог написать.

**\
Andrei Klimovich** 34:56\
Я я я понимаю о чём ты. Я на самом деле это специально сделал это такой подход. Ну то есть ты.

**\
Alexander Biratko** 34:58\
Он мог бы написать просто.\
Да я я понимаю, но но мне чтобы понять, что это за требования мне нужно нажать на ссылку и перейти туда.\
Получается и там почитаться, что же это за требования?\
Исполнилось словах, описал, что это за требование бы ни столь не нужно было переходить, но это просто для упрощения понимания.

**\
Val Levitan** 35:19\
То есть.

**\
Andrei Klimovich** 35:20\
Я я я понимаю твой комментарий саша с моей стороны.

**\
Val Levitan** 35:21\
Саша, вы хотите саша вы хотите ссылку вы хотите ссылку и описание.

**\
Alexander Biratko** 35:27\
Это этого идеальный вариант, то есть если описание мне недостаточно, я могу перейти посылки.\
Да, но чаще всего ссылки не надо, то есть клод.\
Он слишком заумно делает, когда он сам почитает, он кажется, перешел по ссылке, посчитал, вернулся и очень быстро всё красиво. Но он это, если он сам.

**\
Andrei Klimovich** 35:47\
Смотри, сейчас я объясню свою логику, я специально эти кровь ссылки вставляю, когда идёт описание, потому что если есть ссылка на другой рекламент и он меняется по какойлибо причине, то ссылка остаётся актуальной и как бы знания требуется изменить в одной точке.\
А если ты прописываешь в одном рекламенте и ссылку и ещё какоето текстовую логику, то придётся тебе лезть в 2 места и менять это в 2 местах. А если ты этого не будешь делать, то у тебя накапливаться будет постоянно.\
Как это сказать? Ну.

**\
Val Levitan** 36:20\
Ноль.\
Ной.

**\
Andrei Klimovich** 36:21\
Ной нойс да у себя не будет точки истины.

**\
Irina Shishko** 36:25\
А.\
Возможно, Андрей, там можно.

**\
Alexander Biratko** 36:28\
Ну я бы сказал, если если логика рекуармента не меняется, то ну тут тут уже неважно. То есть наверное, если ты меняешь название рекларамента, название да, то как бы оно должно быть другое у него должно быть другая ссылка и другая страница. Ну скорее всего.\
Если если название рекламента сохраняется, тонн часто просто название рекламы.

**\
Irina Shishko** 36:45\
А.

**\
Alexander Biratko** 36:50\
Достаточно, чтобы понять, что что же оно там, то есть просто 2 слова 3.

**\
Andrei Klimovich** 36:54\
Угу.

**\
Alexander Biratko** 36:55\
И достаточно.\
Ну, может быть, в каких то местах естественно оправданно ссылки больше.

**\
Irina Shishko** 36:59\
Андре.\
Андрей, возможно, можно вставлять ссылки, так чтоб оно сразу и.\
Вписывало название этого регламента, и тогда, если ты будешь там менять, то будут меняться и здесь, и не надо будет никуда лазить.

**\
Andrei Klimovich** 37:11\
Вас согласен?\
Отлично, согласен.

**\
Irina Shishko** 37:16\
То есть быстрее всего, что там там можно.

**\
Alexander Biratko** 37:19\
Это идеальный вариант, да?

**\
Andrei Klimovich** 37:20\
Да да да, иди вообще сделаем хорошая идея. То есть если вам будет видно просто хотя бы название экваймент это вам уже комфортнее, гораздо будет работе, понял хорошо.

**\
Val Levitan** 37:34\
Анджели сама из форума lonple playse.

**\
Andrei Klimovich** 37:37\
Sungystoldas IT voliber mooth wi to wistore a cramens. It\'s the the cross links to as there a cramens, mensinit thind this wan wo will be in not jest all link and and NID recraiment wantos refor potreet dow links zoos inste form of the name оф реклармент господин зек завел хавчу до лод оф кросс линкин.\
Werd avery runds in toutrive the ruber name it full say folders it thile hept to mary maic app te conotest.

**\
Juan Martinez** 38:13\
Кстати, время мой.

**\
Andrei Klimovich** 38:16\
Но внутренние суд заехал дисплей за link tou aser corment it mine be a juster i de youter cramment it my bye link.\
Смотрит мальби клика bolling willox like anam of ecroment окей serbe text name.\
За контекст.

**\
Val Levitan** 38:41\
У нее спровай и откуда бы провайрит Джаст azen id nomberber w wer werses anam lenank.

**\
Juan Martinez** 38:51\
Она нужна, надеюсь, до сознательной талкин.

**\
Andrei Klimovich** 39:01\
Ононо thindown batwannet to inse bardiose recrarment it my bye osresser reense inse bardian.

**\
Irina Shishko** 39:02\
Но Ну да.

**\
Juan Martinez** 39:06\
А окей что тебе?

**\
Irina Shishko** 39:06\
А.

**\
Juan Martinez** 39:08\
Данная, кстати, окей, кое что, Кларк.

**\
Andrei Klimovich** 39:08\
Окей.

**\
Juan Martinez** 39:21\
All start corte thindown, Google cortes from thind.

**\
Andrei Klimovich** 39:38\
5.\
70.\
Cortes are stelly.

**\
Val Levitan** 39:56\
А вы там?

**\
Andrei Klimovich** 39:58\
Алло айга айгар май job thinde dan facet wik s ald do my best to final lis for recor MS and will ben clus tress wiss hound ind allex.

**\
Juan Martinez** 39:59\
Так что.

**\
Andrei Klimovich** 40:09\
Уайлд моркино open castin servel red.\
Song way to sre crinest waters moner i red for thure она vost здесь проще thinds contand thind and cr mondes is it is goers innation gamen like the main golnter is dot you cortes for ol caps.

**\
Val Levitan** 40:36\
Окей соу.\
Майлз Стоун for may.\
Sona i open IP tifty nine waters flex ru siqler.\
I wall co.\
Фьючерс скетжу.\
Райна оси lesto fetures.\
Мост да мэндеклок.\
Бат и фаи.\
Да майнек смайл Стоун id туэм скет.\
Яз.\
Солак столько болта самый start anandate.\
Соблюз и роллоп fice.\
Энрола фичер воркс айдер он де левел оф.\
Сабтаск ой таск.\
Орсторы.\
По фичер.\
Соо ифлекцей ficers fave.\
Stores andreid.\
Wech i prostongley don\'t recwier.\
Поэтому pazzanger sto mary seck sen II don not recwwish stories stories и sumtinder halp.\
Саша forexple.\
Туда и секс.\
Через министепс.\
Хау из гонь tod thi lever он офиc.\
Саша в плане но форма.\
Ай год pays of fe furse be cortes to me afiecter.\
И запрог смотри.\
При ту файв дэйс оф work.\
Фотот Минск рафли.\
Fift tin toony aures.\
О форд.\
Лука future branching gi.\
А блоки над малту камед spreday.\
Коничка metome с биткоин ту forgan red lines of cort.\
Саша мейда сайт хе вонс то сплырит intu stories waters pex to inna or or sorry erina or pavel.\
Good inna afforem one level fic this.\
Алёна окончате?\
Бат и в саше должно брать сториз andrew fiter.\
Дэн фичер net store and and dendate.\
Соул.\
Ломея ломегра.

**\
Juan Martinez** 43:56\
Мы сообщаем.\
5.\
Ешь.

**\
Alexander Biratko** 44:06\
Ясно.

**\
Val Levitan** 44:07\
Сонау а блокнот flex там син.\
Скетчиал.\
Вот а свои нанки.\
Сован саша с окей wall inow, a prock, some matley waterswall tayk.\
Сигнал.\
Мне надо.\
Атеисты скот со нациз.\
Amazon to do do here.\
Через май файс.\
Я огонь то дует хиро and word.\
Одесс и эс лэнг инги.\
Окей sotu.\
I\'m good with that.\
Or Sasha could say, and then Sasha says, you know what, this is going to be actually starting here.\
And I\'m going to link it here.\
Sorry, and and it\'s going to be\...\
Three days like this.\
So I\'m okay with that.\
Sasha may decide that in here he wants to\...\
Start planning based on stories.\
So, to me, a story is something that is one or two days, not more.\
So you want to schedule stories? God bless you. Go ahead.\
So we see then the feature, this main feature, has a\...\
A barbed wire.\
Image to it.\
And you see this image stretches. For example, now if I stretch this story and I will say the story starts here, suddenly my feature now.\
On a calendar day, stretched out.\
So that, to me, that is planning.\
The moment we start moving.\
Start assigning schedule. This must go from backlog to to do.\
To do means\...\
It\'s scheduled.\
and it needs to be stock ranked.

**\
Andrei Klimovich** 47:05\
Igor.

**\
Val Levitan** 47:07\
Questions?

**\
Juan Martinez** 47:10\
No.

**\
Andrei Klimovich** 47:18\
Looks good. I mean, there might be there might be questions when we will move to this stage, yeah.

**\
Val Levitan** 47:18\
Talk to me.\
That\'s.\
Okay, so to me, that\'s the next milestone.

**\
Andrei Klimovich** 47:30\
Mhm.

**\
Val Levitan** 47:31\
My question to this forum right now is, when can I see this milestone?

**\
Andrei Klimovich** 47:40\
So again, from my side, I have the whole next week just to make sure that all capabilities are converted into requirements and they are groomed by me and Juan as much as possible, just to make sure that that\'s exactly what we want to have. Then it will take some time for Alex to convert them to features.\
Um\...

**\
Val Levitan** 48:02\
No, I don\'t need it to be done in tandem. This needs to be done in parallel.

**\
Alexander Biratko** 48:09\
But, see, see, see, after most with national scheduling.

**\
Andrei Klimovich** 48:09\
Yeah, sure.

**\
Irina Shishko** 48:16\
No.

**\
Alexander Biratko** 48:18\
When you did.

**\
Irina Shishko** 48:19\
But are the.

**\
Val Levitan** 48:22\
Okay, so let\'s have a next checkpoint on Wednesday the 20th.\
I will circulate a meeting invite.

**\
Irina Shishko** 48:30\
Slope.

**\
Andrei Klimovich** 48:34\
Mhm.

**\
Val Levitan** 48:35\
To review the schedule of the features.

**\
Irina Shishko** 48:36\
Okay.

**\
Val Levitan** 48:41\
That are known.\
So you go ahead, continue working on your capabilities and requirements, that\'s fine.\
But, Sasha, for now with Pavel.\
And Irina.

**\
Irina Shishko** 49:01\
Mm.

**\
Val Levitan** 49:01\
We\'ll start scheduling.\
Uh, the known features.

**\
Irina Shishko** 49:09\
Game.

**\
Val Levitan** 49:09\
And we will review them on Wednesday at 8 A.m.\
Eastern Time. I will circulate on the right.\
So with that in mind, I think we can conclude this meeting.

**\
Irina Shishko** 49:18\
Okay.

**\
Andrei Klimovich** 49:22\
Yeah.\
Okay, sounds good.

**\
Juan Martinez** 49:25\
It\'s good.

**\
Val Levitan** 49:27\
OK, Andrei and Juan, can we meet with Felipe now?

**\
Juan Martinez** 49:32\
Sure. And well, Andrei, don\'t you have to run to an appointment?

**\
Val Levitan** 49:36\
Oh, sorry, yeah.

**\
Andrei Klimovich** 49:37\
So, we have an, yeah, we have an amazing at 10, and I still need to get to there, so\...

**\
Val Levitan** 49:42\
Yeah, yeah, yeah. Go ahead. Go ahead. Go ahead.

**\
Andrei Klimovich** 49:44\
Mm-hmm.

**\
Val Levitan** 49:46\
All right, thank you very much. All the best.\
Bye.

**\
Andrei Klimovich** 49:50\
Thank you. Bye-bye.

**\
Alexander Biratko** 49:52\
Why?

**\
Irina Shishko** 49:52\
Bye.

**\
Val Levitan** 49:52\
Yeah.

**\
Alexander Biratko** stopped transcription
