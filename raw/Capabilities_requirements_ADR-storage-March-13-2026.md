**Call with Aaron Bockelie-20260313_173307-Meeting Recording**

13 March 2026, 09:33pm

12m 34s

**\
Val Levitan** started transcription

**\
Aaron Bockelie** 0:04\
He owns, he owns a game or a system that supports games or whatever, because he knows the gaming reality really, really well, right? So he\'s gonna know what capabilities are gonna really.\
Really be the right ones to nail how they\'re implemented and the requirements for them are he\'s partially responsible for, but knowing the product and what it should do and having a clear vision, that\'s why a product owner\'s worth 1,000,000 bucks is because.\
They have a clear vision of what it\'s supposed to be.

**\
Val Levitan** 0:39\
OK, so a technical question. Is capability a type of a project in Jira? Does it reside in Jira?

**\
Aaron Bockelie** 0:50\
I don\'t know. I don\'t think so.

**\
Val Levitan** 0:53\
Because.

**\
Aaron Bockelie** 0:53\
Think a capability is.

**\
Val Levitan** 0:55\
Because Claude is suggesting it for it to resign in Jira.

**\
Aaron Bockelie** 0:59\
I mean it could. So the thing with.

**\
Val Levitan** 1:03\
As a as a project type.

**\
Aaron Bockelie** 1:07\
No, I I don\'t know. I this this isn\'t connect to me. So the capability fundamentally is not like I I would say don\'t look at it like it needs to be in in Jira. Instead, let\'s ask where do we track our capabilities at?\
Like ask that question just plainly without bias if you can to start with.

**\
Val Levitan** 1:29\
Yeah, I will. I just want to have a conversation with you just to pick your brain.

**\
Aaron Bockelie** 1:29\
Well.\
Yeah, yeah, I\'m I\'m just thinking it through right now. So, so a capability.\
It kind of exists in a couple different places simultaneously.\
So a capability can exist in JIRA, but I think it exists there as a way to be tracked. It\'s not like that\'s the source of truth. It\'s not like JIRA holds on to the capability as the place that you officially keep it at, right?\
I think you could copy a capability into JIRA as an as an issue, as an issue type to track it though I feel like capabilities.\
Probably reside more with a business operations model than they do with an actual product directly. So what you would do is you let\'s just imagine this other I don\'t even, I\'m not going to even name it yet, right?\
I\'m going to say it\'s this data lake where you keep the core of what JVL actually is.\
In a lot of cases, in smaller companies, it just might be in your head. In slightly bigger ones, you have the big book where it\'s all kept and you write it down. You might have it in Confluence or a whiteboard, or literally your notes all over the office or whatever it is you do, but at some point.\
The capabilities and and intent of the company is kept somewhere, and I think it\'s really important to make the distinction between where you actually keep the source of truth and where how you track that information that comes out of the source of truth.\
Right. So think about controlled document records for just a minute. So like.\
You know how you have the documents? It\'s like original copy or not controlled, or you\'ve probably seen those types of papers, right?\
There is one person that officially holds the copy under lock and key, and if you change this, literally everybody else\'s copy is invalid because it\'s those are all copies of the original. It\'s like money, right? So that under lock and key original copy.\
Is kept somewhere, that source of truth. And I I actually feel the capabilities sort of belong in that filing cabinet a little bit, whatever that is. And so when you take capabilities, they\'re they\'re not prevented from being seen, they\'re prevented from being changed.\
So wherever you\'re keeping them at, you you agree to those and requirements are kind of also managed this way too.

**\
Val Levitan** 4:23\
But but I mean, I mean you hit a nail on the head here if capability is this.\
Um.\
The the original form of thinking or the original form of planning and it could never be changed. I mean, it could be changed, but if it\'s changed it, you know, it\'s a domino effect. A lot of things will fall.

**\
Aaron Bockelie** 4:49\
Mhm.

**\
Val Levitan** 4:50\
So the best way to hold the unchanged source of truth is in Jira, because there you cannot change it. That\'s that\'s it.

**\
Aaron Bockelie** 5:00\
I.\
Yes and no.\
So JIRA is designed as an issue tracker and all it takes is one person to delete something and it\'s gone. It\'s in a cloud environment without any way to easily copy it out and in. And frankly, I just don\'t trust it.\
And I would say that it would be better to take a more controlled. Now it\'s interesting. And when we think about data, we say, oh, there\'s only one copy in existence. That\'s the truth, right?\
Well, that\'s not actually true. You could have 100 copies as long as they cryptographically match U.

**\
Val Levitan** 5:46\
Right.

**\
Aaron Bockelie** 5:48\
O you can have them copied everywhere, right?\
And JIRA, if you keep the source records in there, there is zero ways to cryptographically ensure integrity of an issue with with that stuff. There is no way to actually do that.

**\
Val Levitan** 6:02\
OK.\
OK, but all right, I see your point. But if I tell you so, where should it be kept? You cannot give me an answer.

**\
Aaron Bockelie** 6:12\
I think it could be kept in a git repo.\
Because a git repo can be cryptographically tracked, right? I made this requirement document or this this capability document for this product and it\'s right here.\
Right. And then we can take that and bubble it into JIRA where we just track it as a as a shadow copy of the original.

**\
Val Levitan** 6:37\
OK, so our preference is to keep it in GitHub.

**\
Aaron Bockelie** 6:41\
I think for now your preference is to keep it in a git repo and I\'m correcting from GitHub. I\'m just saying git repo because GitHub I I know it\'s semantics, but I\'m I\'m trying to just train you to think in the elemental tools that we actually have. We have a git repo.\
Which is held in GitHub, but it can also keep a copy locally and so forth. And so if we have these these individual files or whatever they are inside of the git repo, what we can do is we can actually write up a relationship in the.\
Git repo that Jira issue PRD123 is connected to Jira, right? So there\'s actually a block of text in a GitHub repo that literally describes it exactly, and PRD 123 is copied into the Jira issue if someone goes and just edits the Jira issue.\
Well, you need to always be when you\'re referring to that requirement or that that capability document, you can go back and look at the source and if you read the two and they\'re different, it\'s like, uh oh, so somebody changed the JIRA thing.\
And the stuff in GitHub is not the is is not the same as JIRA. And if you have the blanket rule that the only source of truth is in the GitHub issue, then you immediately cross off the list the question of who\'s right, right and who\'s wrong.\
We know JIRA is wrong because something changed in JIRA.

**\
Val Levitan** 8:15\
And are you still saying that the requirements should be kept in JIRA?

**\
Aaron Bockelie** 8:22\
I think that eventually the requirements in JIRA need to exfiltrate out into the projects probably. I think each of your products or projects in git should be where the requirements are actually at, and then the requirements in JIRA is just where you debate and discuss and get them.\
Pushed into it.

**\
Val Levitan** 8:42\
You lost me.

**\
Aaron Bockelie** 8:44\
OK, let me say it again.\
So you understand how architectural decision records ADR files, right? I\'ve hammered that home a lot. They\'re KET with the repo, yeah.

**\
Val Levitan** 8:54\
Yes, yes.

**\
Aaron Bockelie** 8:57\
O We don\'t keep an ADR in JIRA, and we don\'t keep an ADR in Confluence because they\'re decoupled from the project.

**\
Val Levitan** 9:05\
Yes, yes, understood.

**\
Aaron Bockelie** 9:08\
And the way you write an ADR is that you look at all the requirements and then you write your ADR according to the requirements. It\'s actually how an ADR exists.\
And so therefore it makes sense that if you have requirements, you have a master place where all requirements can kind of live like a like a bazaar, a shopping center for all of your requirements for the entire company, everything.\
Because you can reuse requirements across multile rojects and stuff like that and roducts.\
And what you can do is you can copy that set of requirements into the repo and have them available right there and then you can write your ADR and you do your thing and move on with life because requirements can change.\
Then you always are updating the requirements into the repository and cloning them into there as possible. If you look at how requirements are managed at larger companies, they begin to go beyond just writing JIRA issues.\
And tracking them as issues. They actually have secialized tools and software for tracking requirements, but I have not let JVL down that path because.\
I don\'t think JVL has had the attention span to be able to manage requirements with one of those tools and the cost of the tools.\
Though we\'ve kind of kept them as informal large text blobs inside of JIRA, which is functionally works well. And I think The thing is, is that now if Juan is.\
Cleaning up all of those requirements and accepting them and moving them into an accepted state and generally curing the data set for requirements. That\'s where you\'re finally beginning to get to the point of maturity to even think about a potential other requirements tool besides Jira.\
But I would say JVL is not ready to move into a requirements tool yet because they don\'t even they lack the maturity to even get to just doing it in JIRA as a my my baby steps first requirements management tool.

**\
Val Levitan** 11:18\
Understood. So to simplify everything that\'s said, requirements for now until we reach the state of maturity will be kept in Jira. The capabilities will be kept in GitHub, Git, but we use GitHub.

**\
Aaron Bockelie** 11:28\
Mhm.\
Yeah, because because capability. So I I would say the flow kind of works like this for me, maybe different other people, but it it flows requirements to capabilities to architecture decision.

**\
Val Levitan** 11:45\
Right to to to specification to to.

**\
Aaron Bockelie** 11:46\
In that order.\
Right to actual to actual code to, you know the actual thing, right? And the and the tests become the contracts that verify that your spec and your requirements are met, right?

**\
Val Levitan** 11:55\
Right.\
I got it.

**\
Aaron Bockelie** 12:05\
So yeah, and and I think The thing is, is that for now we\'ve we\'re we\'re in the fortunate position of being able to keep both capabilities and architectural decisions in the git repo already right now.

**\
Val Levitan** 12:22\
I got it clear. Clear. OK. Thank you very much. I\'m I\'m cooked for today.\
Bye.

**\
Val Levitan** stopped transcription
