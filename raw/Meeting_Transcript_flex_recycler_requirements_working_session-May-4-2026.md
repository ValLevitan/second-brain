**Flex_Recycler Requirements Working Session-20260504_090104-Meeting Recording**

4 May 2026, 01:01pm

**\
Val Levitan** started transcription

**\
Val Levitan** 0:05\
So the next priority we should groom the current capabilities and to drive these capabilities into capability project type, CAP, capability project type.

**\
Juan Martinez** 0:19\
Yep.

**\
Val Levitan** 0:19\
And so right now you\'re going to be migrating and merging 24 capabilities with the 8 capabilities that we have so far.\
So that\'s priority number one. Priority #2, while you\'re doing it, you said early, Andrei, you said that it would take you a day or so. Well, it\'s the end of the day in Minsk. So tomorrow when Minsk comes back to the office, Alexander will start\
Developing features.\
We also agreed that those capabilities that are done, we\'re not going to retroactively go through a circle of fictitious development, but we\'ll just mark them as done.\
We also contemplating removing the\...\
In initiative level.\
Ohh.\
task in JIRA project and replacing it with a capability under, sorry, replacing it with a product. So initiative will cease to exist, product will replace it, and under product between product and feature, we will wedge a capability level.

**\
Juan Martinez** 1:40\
Just to clarify, doesn\'t Alexander need the requirement in order to create the feature?

**\
Val Levitan** 1:46\
He does, if, well, yes and no, if Alexander doesn\'t understand.

**\
Juan Martinez** 1:47\
K.

**\
Val Levitan** 1:54\
how to describe a capability in features. He would be reverting to requirements. Requirements and use cases is what.\
help Alexander to develop features. But many he knows already, it has been discussed. So we\'re kind of catching up on both sides. Andrei is catching up on the capability requirement and use cases, and Alexander is catching up on features and stories.

**\
Irina Shishko** 2:10\
Ohh.

**\
Juan Martinez** 2:14\
The.\
Right, right.

**\
Val Levitan** 2:25\
So, I would say that our goal should be\...\
by the end of the week.\
to have a full set of on one side capabilities and requirements.\
And requirements with acceptance criteria, capabilities so far we should not develop acceptance criteria.

**\
Irina Shishko** 2:49\
Mhm.

**\
Val Levitan** 2:49\
And then on the other side is capabilities and features.\
And features may or may not be.\
Broken into\...\
Stories and subtasks.\
I\'m just going to repeat it because now this portion of the meeting is recorded.\
I\'m just going to repeat that each feature.\
eventually represents a feature branch.\
And the feature branch is opened in GitHub.\
And this is what a developer, when they start punching code, this is where code goes. This is, it goes into a feature branch. I consider feature, well, we consider a JVL feature branch lasting approximately.\
At one calendar week.\
And we expect multiple pull requests.\
And our pull request is considered approximately between 2 and 400 lines of code.\
Those are the approximate measures. Of course, they\'re approximate.\
So, a future branch, we feel that it should be.\
Multiple commits.\
Multiple commits, sorry. I should say not pull requests, but multiple commits to a feature branch.\
during one working day. So my expectation on an average, approximately 10 commits per feature branch.\
Right.\
But that\'s very, very rough orientation math.\
I don\'t know if you agree or disagree, Sasha. Any opinion?

**\
Alexander Biratko** 4:43\
How are you?

**\
Val Levitan** 4:45\
Okay, Irina, very, very important.

**\
Irina Shishko** 4:48\
Yeah.

**\
Val Levitan** 4:50\
Oh.\
Feature branch, we are attaching, we are wedging.\
Uhh\...\
Claude Pull Request Reviewer.

**\
Irina Shishko** 5:06\
Uh-huh.

**\
Val Levitan** 5:06\
And at this point, you, that\'s your basic reliance on the integration testing.

**\
Irina Shishko** 5:17\
Yeah.

**\
Val Levitan** 5:17\
So your acceptance criteria should also be\...\
Right there.\
And so your goal now, Irina, your goal is to have a set of.

**\
Irina Shishko** 5:30\
Mhm.

**\
Val Levitan** 5:37\
Test.\
cases that could enable you to do end-to-end testing.\
Of the product.\
And because not all features appear at the same time, your end-to-end testing has to be catered to that as well.\
So, as Sasha is developing his feature branches.\
Your team should be developing a set of end-to-end testing.\
So as the product, as we deliver, as Sasha delivers features, you should be engaging end-to-end testing.\
We must have test running parallel to development, not sequential.

**\
Irina Shishko** 6:31\
Ohh.

**\
Val Levitan** 6:32\
I will never accept sequential testing. It\'s going to be a fight forever.\
Tests must be done.\
in parallel.\
So, I need\...\
End-to-end testing.\
That will test capabilities.

**\
Irina Shishko** 7:00\
Mhm.\
Yeah.

**\
Val Levitan** 7:09\
Okay, so let\'s check again on Friday. Are we good on Friday? Will it give us enough time to do something tangible?\
Should we do should we do earlier than Friday, maybe Thursday?

**\
Andrei Klimovich** 7:21\
If we can\...

**\
Juan Martinez** 7:21\
Hi, Pavel.

**\
Alexander Biratko** 7:26\
No.\
Friday.

**\
Andrei Klimovich** 7:29\
Can we do that on Monday because I will be away on Friday.

**\
Val Levitan** 7:29\
Right.\
Of course.

**\
Irina Shishko** 7:36\
Where can you find?

**\
Alexander Biratko** 7:39\
Yeah.

**\
Val Levitan** 7:47\
Then I suggest let\'s check in on the 7th on Thursday.

**\
Juan Martinez** 7:52\
Hey.

**\
Val Levitan** 7:53\
because then it\'s too far out. I don\'t like far-out meetings.

**\
Andrei Klimovich** 7:55\
Okay.

**\
Alexander Biratko** 7:56\
I.

**\
Andrei Klimovich** 7:58\
Okay. Morning.

**\
Juan Martinez** 8:02\
Yep.

**\
Val Levitan** 8:02\
Yes, let\'s do 8am.\
On Thursday.

**\
Andrei Klimovich** 8:07\
Okay, deal.

**\
Val Levitan** 8:08\
Thursday the 7th, I will book the meeting for us.\
I will circulate the undertaking and the notes.\
Thank you very much, everyone. I wish everyone a great day.

**\
Irina Shishko** 8:22\
The.

**\
Juan Martinez** 8:26\
Thank you.

**\
Alexander Biratko** 8:26\
Math.

**\
Andrei Klimovich** 8:28\
Thank you, bye-bye.

**\
Juan Martinez** 8:28\
Bye-bye.

**\
Irina Shishko** 8:29\
Ohh.

**\
Val Levitan** 8:29\
By.

**\
Alexander Biratko** stopped transcription
