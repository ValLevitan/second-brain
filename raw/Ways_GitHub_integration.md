**Ways_GitHub_integration-20260319_081451-Meeting Recording**

19 March 2026, 12:14pm

48m 15s

**\
Val Levitan** started transcription

**\
Aaron Bockelie** 0:03\
A first order service to translate because JBL is a multinational company. You have not only do you have Slavic languages that you that you have to transform not just the translation but the intentions of, but you have the Latin American languages as well.\
Coaches as well and any other bigger markets where you\'re moving things back and forth from.

**\
Val Levitan** 0:26\
I I was trying to stay away from a large project.

**\
Aaron Bockelie** 0:31\
Right. But I\'m not saying don\'t build that yet, but start with something super simple, like just like what Clayton\'s building. But then think about how this becomes something more formalized to be able to use it at scale in the future.

**\
Val Levitan** 0:46\
So that\'s what we\'re discussing in the now.\
What? What should it become? What? What should the architecture be? Where should that glossary or text lacks or whatever we\'re going to call it, or semantic understanding document be placed?

**\
Aaron Bockelie** 0:51\
OK.\
You remember?\
Do you remember the whisper transcribe tool that I built for you?

**\
Val Levitan** 1:08\
Yes, I still have it.

**\
Aaron Bockelie** 1:09\
OK, so.

**\
Val Levitan** 1:10\
It\'s it\'s fantastic, by the way.

**\
Aaron Bockelie** 1:13\
That architecture of that is 2 pieces. It\'s both a front end and a back end, and the back end doesn\'t have to run on your machine. It could actually be out on a host somewhere else dedicated to doing the translation.\
And I guess all I\'m thinking about here is that maybe JVL has essentially some endpoints that don\'t have any user interface at all. They\'re just you put in text here and the language out of the selection of languages that you think this is, you tell it, give it a little bit of a clue, you know you can\'t just throw.\
Throw it in there and then what pops out is JVL\'s domain specific language such as throwing XA in front of deploy gets understood implicitly because of all the hinting on the way back out.\
This is essentially like using Google Translate, right? You know how you can go to Google Translate and put it in one document and get another one out. I think that having an API endpoint where you could throw voice and text and have it get transformed into text on the output on the other side.\
Is kind of a more as a better way to formalize this. This means that anybody\'s.\
Toolkits. If you\'re using Cloud Desktop or Cloud Code, or literally just like a command line tool, you can run it. It\'s part of your toolkit for JVL and out pops the correctly the the recognized official translation of whatever it is you\'re working on.\
So this is a way to maintain consistency in the translation rather than potentially passing around a language transformation table of some of sorts.

**\
Val Levitan** 3:07\
I have a.

**\
Aaron Bockelie** 3:07\
You would then wire this up to to anthropic credits or you know tokens and you could just use anthropic to do the translation.

**\
Val Levitan** 3:18\
I I have a feeling that you\'re you\'re trying to, sorry, you\'re saying what I was trying to say, but I\'m not sure that this is the same thing.

**\
Aaron Bockelie** 3:30\
So what I\'m saying is do the translation experiment with Clayton, see how it works out. Don\'t build the whole thing, but also simultaneously hold the bigger vision of how you can make this consistent for all of JVL as a service.

**\
Val Levitan** 3:46\
And that was my question. So what\'s the architecture for that past Clayton?

**\
Aaron Bockelie** 3:51\
Sure. Well, here, let\'s do this.\
Are you able to see my cloud desktop?

**\
Val Levitan** 4:31\
Yeah.

**\
Andrei Bosik** 4:32\
Yes.

**\
Aaron Bockelie** 4:33\
OK.\
There\'s the prompt. Let me share it with you so you have a copy of it.\
This is how I would just sort of write this out.\
And then from this point you can now take this into cloud code where you have the current Waze system to then build this into a proper git repo with the ADR spec and all the other tenant good things that Waze provides and you can probably go ahead and just.\
Get this built.\
O We\'ll see how this kind of lays out here.

**\
Val Levitan** 9:26\
OK, so let\'s let\'s incorporate this, I understand. So it\'s becoming part of our ways, right?

**\
Aaron Bockelie** 9:32\
No, this is a separate system that potentially Waze could call is what we could do, but other tools besides Waze could call too as well. So for instance, let us imagine for a minute that you are writing up documentation or.

**\
Val Levitan** 9:37\
I see.\
OK, I\'m.

**\
Aaron Bockelie** 9:49\
Even you need to do localization for for instructions inside of your inside of the product. If you wanted to lint lint the documentation, this would catch any of the cultural quirks that might slip through.\
Slip through Indiana a localization text for a game for example, or for just even just doc strings inside of the code.\
O you have a universal tool language kit tool that JBL sort of agrees upon O that we convert these slangs or isms into this particular way.\
So what I would do is I\'d start with this and then I would go ahead and I will go ahead and point it at the Whisper transcription service as an example of an actual service model for how this might run and then.\
That way we can kind of incororate some of the other language too.\
So let\'s see problem statement. The organization\'s internal communication blends Slavic languages with English technical vocabulary in ways that standard translation engines handle poorly. The developer might say ZA deploy Slavic prefix ZA affected the English verb deploy or use other hybrid constructions that carry precise meaning internally.\
But produce garbage when fed to off the shelf translators. Meanwhile, the company ships products to multiple regions and needs consistent high quality localization of UI strings, documentation, and meeting transcripts. No single commercial API solves both problems. This service closes the gap by combining language model based translation with.\
Exlicit Administration curated terminology override table.\
I think that.

**\
Val Levitan** 11:48\
That\'s that. That makes sense.

**\
Aaron Bockelie** 11:50\
I mean, that\'s kind of what we\'re trying to do here, right?

**\
Val Levitan** 11:54\
Yes.

**\
Aaron Bockelie** 11:55\
O We have a text to text translation capability, an audio to text translation and terminology management. It\'s very focused.

**\
Val Levitan** 12:04\
That\'s that\'s fantastic.

**\
Aaron Bockelie** 12:06\
So let me share this with you guys.\
As a starting point, I\'m not saying this is the answer or finished. We got to look at it together, right? But I think it could. I think it\'s a good starting point.\
I\'m also doing this in front of you, Andre, so you can see essentially how I build stuff. This is what I do. I think it through. I look at Val. I start talking over the top of him for a little bit. He gets a little frustrated. Then I sit there and type and he silently watches me type all this \*\*\*\* out into the text thing and out pops a magical.

**\
Andrei Bosik** 12:32\
Mhm, yeah.\
OK.

**\
Aaron Bockelie** 12:45\
Architectural document ready to start building stuff with and so this is how it works usually.

**\
Val Levitan** 12:52\
It will be 10% will be deducted from your next pay.

**\
Aaron Bockelie** 12:55\
That\'s OK. I haven\'t even got the invoice for February figured out yet, so we\'re we\'re we\'re all in floating around anyway, so.

**\
Val Levitan** 13:03\
OK.

**\
Aaron Bockelie** 13:06\
It\'s fine. Um.\
So So what we could do then Andrei is you could start a git repo already. Copy this file into the git repo, just throw just this file into it. Make sure you start a new session with up-to-date ways as it is right now and basically tell Claude.\
I want to start this project, use all of the ways to make this a first class GitHub repo. Let\'s let\'s plan it some more. It\'s all you have to say to start it off. You\'re not going to build code yet, you\'re just going to feel it out more.

**\
Andrei Bosik** 13:40\
But.

**\
Val Levitan** 13:44\
By the way, that\'s that\'s what I do in from my executive perspective. I don\'t build engineering projects, but I do build executive projects and that\'s how I start learning from Aaron.\
OK, OK, so this meeting is dedicated to setting up GitHub for.

**\
Aaron Bockelie** 14:01\
So yeah.

**\
Val Levitan** 14:09\
Um.

**\
Andrei Bosik** 14:12\
Voice.

**\
Val Levitan** 14:13\
Voice, yes.

**\
Aaron Bockelie** 14:17\
So do you want to share screen Andre and hopefully Claude behaves today?

**\
Andrei Bosik** 14:23\
And how Clotus work? But when uh most America is get up, Clotus uh start work slowly.

**\
Aaron Bockelie** 14:32\
Yeah.\
OK, so let\'s. So you gotta open. Yeah, yeah, yeah.

**\
Andrei Bosik** 14:38\
I resume our yesterday prompt and I\'m ready. Press enter.

**\
Aaron Bockelie** 14:45\
Uh huh.\
OK, let\'s see what happens.

**\
Andrei Bosik** 14:50\
OK, let\'s go.

**\
Aaron Bockelie** 14:58\
Watch it not work \'cause I\'m watching it.\
Come on, Claude. There we go. OK, see loading the Waze skill automatically. That\'s how it\'s supposed to work.\
You know about BTW, right, by the way?

**\
Andrei Bosik** 15:52\
I never use this.

**\
Aaron Bockelie** 15:55\
During any session you can type slash BTW and ask it a question and it won\'t interrupt the main work that it\'s doing. You can ask it a question about what you\'re what it\'s doing. Not not enough has happened yet to really ask BTW yet.

**\
Andrei Bosik** 16:02\
Mhm.

**\
Aaron Bockelie** 16:11\
But it\'s nice to be able to have essentially A sidebar discussion that doesn\'t interrupt the main discussion.

**\
Andrei Bosik** 16:17\
Mhm.\
Uh, what include uh this uh discussion to his uh.

**\
Aaron Bockelie** 16:31\
This is part of cloud code, not mine. Slash BTW if you type it right now slash BTW.\
Slash slash.\
See how it it prompts it for? Don\'t fill it out right now, but you can see how it shows that.\
All right, let\'s backspace out of BTW and read what it\'s created here so far.\
Let it finish writing this.\
O What we\'re going to do now is we\'re going to read through this and we\'re going to think about what it implies.\
Whether it\'s trampling existing ways and causing us to diverge from the ways and tensions that we have right now, and whether it\'s too complex for any one particular way.\
Let\'s scroll up and slowly read it together. Here, scroll up to the top.\
Now let me see what it says here.\
So first of all, I can I I\'ll just translate for you a little bit. It\'s gonna create it\'s splitting this into three different concerns of ways.\
OK, let\'s Scroll down some more.\
Let\'s keep going down some more.\
Kee going down some more because I\'m reading through it first and then I\'ll let you go back and read it some more if you want.\
Kee going a little further.\
OK, I\'m going you. You read this yourself now as to how you want. I\'m going to write the next prompt to discuss this with Claude.\
Then I\'m going to share it with you and you can you can understand it.

**\
Andrei Bosik** 19:20\
Oh, OK.

**\
Aaron Bockelie** 21:44\
Can you scroll up to the top for a minute? I need to check something up at the top.\
OK.

**\
Andrei Bosik** 21:59\
I think I copy and paste this in chat maybe.

**\
Aaron Bockelie** 22:04\
No, it\'s fine.\
OK, this is what I would actually type if I were to be doing this myself. I want you to read through that prompt.\
When you\'re done reading it, I\'ll explain why I\'ve written it the way I have.\
It may also be helpful to translate it to Russian first, I don\'t know.

**\
Andrei Bosik** 25:46\
Mm-hmm.

**\
Aaron Bockelie** 25:48\
OK, so the very first sentence that I say, which is this is a first pass of decomposition. This sets the tone and causes the dwell attractor of Claude to not discard everything it just proposed and start fresh again.\
It acknowledges that its work was useful and won\'t steer it into re redoing everything because Claude is somewhat syncophatic to user input.\
Then the next thing I do is I give a list of concerns, the first thing that stands out.\
Is that we\'re actually invoking an architect agent of of sorts. If you look through the documentation, it kind of talks about it that way. And actually the originating document talks about it as being an architect as well because we\'re we\'re taking.\
We\'re taking this shape of this text that Val had written and we\'re it\'s like clay and we\'re sort of smooshing it around into something different. We\'re we\'ve made it into clay snakes and now we need to make the pot and the handle and we\'re making a tea kettle eventually. Maybe there\'s a.\
Just an analogy. My point is, is that we kind of smoosh it through by steering it like this, the the context that we\'ve got. We\'re orchestrating the context inside of cloud right now.\
So I introduce a couple of things that I know that are in the Waze system, such as progressive disclosure and density. And then there\'s also a particularly interesting thing where it talks about two phase approach to managing things.\
And a two phase approach that it talks about. There is a informal reference to what is called breadth first search BFS. It\'s a it\'s a computer science term for how do you search for for.\
Information.\
That\'s actually what\'s going on inside of this. So when you paste this prompt in here, it\'s going to get a little bit more technical and start to consider the architectural integration that we can do with Waze, as well as make sure that we don\'t override over the top of existing ways and cause it to have problems.\
I also feel strongly that um.\
This is kind of a it\'s like a different sort of agent role. It\'s not a software architect, it\'s a product engagement engineer or product engagement architect.\
That\'s actually a new role, a new, a new agent that we\'re going to be creating in here. So let\'s just see how Claude interprets this. So go ahead and paste that in.\
So you\'re using. So internally, just watch out that your internal subagents you\'re using Sonnet. I see that right now.\
Probably fine. Just, you know, keep an eye on that.

**\
Andrei Bosik** 29:23\
Oh.

**\
Aaron Bockelie** 31:24\
OK, let\'s go back and review what it what it talked about.\
The BM25 collision map is damning for my original approach, so a lot of these things are already claimed by a whole bunch of other ways, right?\
We have only so much matching space to to use with this system.\
This is a coordination pattern against existing components inside of waves.\
OK, let\'s Scroll this down.\
Kee going down further.\
All right, so.\
I have my opinion. I\'m going to type it out before I forget it here. Give me one second.\
OK, that\'s my response.

**\
Andrei Bosik** 37:35\
I I.

**\
Val Levitan** 38:02\
And let\'s go.

**\
Aaron Bockelie** 38:59\
OK, let\'s start at the top.

**\
Andrei Bosik** 39:30\
It\'s my tools that I use for work with.

**\
Aaron Bockelie** 39:34\
I see.\
Is that tool set available to everybody else?

**\
Andrei Bosik** 39:41\
No, it\'s just for me because this doesn\'t include many predefined means features.

**\
Aaron Bockelie** 39:50\
OK, so do you understand now what\'s going to happen if you have ways that diverge from everybody else\'s ways? It\'s going to taint this and cause everybody else to depend on those ways. You might have to have this whole conversation over again.\
If you\'re introducing context into your agent, your version of cloud code isn\'t available to other people.

**\
Andrei Bosik** 40:16\
I can just say quote in this dialog use do not use this tools use for example your MCP for work with Jira and use Gahashi live work with GitHub.

**\
Aaron Bockelie** 40:33\
You can\'t. No, you can\'t do that. So I didn\'t know you had configured specialized tools and what you need to be doing this on is a standard spec environment that most of JVL gets. You have to have a clean environment because it all affects.\
The the statistical likelihood of how it creates the conversation. So now it\'s it\'s like you\'ve already put the food coloring into the into the into the dough here and you cannot unmix it now.\
If you back it out, it doesn\'t. No, it doesn\'t work like that. But we have all these prompts, so you could literally just go through mechanistically and do the same thing again. You\'ll get essentially the same results, but without the without that color in it.

**\
Andrei Bosik** 41:21\
Mm-hmm.\
Mm-hmm. Awesome.

**\
Aaron Bockelie** 41:28\
But I think it\'s getting pretty close to this, right?

**\
Andrei Bosik** 41:31\
Mm-hmm. Yeah, I agree.

**\
Aaron Bockelie** 41:40\
Let\'s keep going down and look.\
Yeah.\
Given all this, this is probably actually really good right here. The agent\'s actual job. Given all this, the engagement auditor\'s agent definition becomes surprisingly lean. It doesn\'t need to carry domain knowledge, it needs to carry the survey methodology breadth first.\
Project contacts, templates, what to ask before starting, executive output format, persona, stance and the coordination awareness. It\'s a conductor, not an orchestra.\
I like this, but now we have to do the whole thing again without your secial customizations for you.

**\
Val Levitan** 42:50\
Uh.

**\
Andrei Bosik** 42:53\
Why is the way, uh, create another.

**\
Aaron Bockelie** 42:58\
As as someone who gets to author ways and sort of administrate the whole system, you have to maintain a clean production deployment set of environment for cloud for cloud code.\
It\'s almost like you need a separate machine or a separate installation of of it, you know?

**\
Andrei Bosik** 43:15\
Yes, yes, as I say, I create a separate VSL machine for for this syncs.

**\
Aaron Bockelie** 43:24\
OK, do you want to try going through the thing again really quick? Then it should just generate it. Share your other go back into that machine and we\'ll run through the prompts one more time.

**\
Andrei Bosik** 43:36\
I I don\'t think this is quickly.

**\
Aaron Bockelie** 43:40\
Oh, you can\'t just switch over.

**\
Andrei Bosik** 43:44\
Uh, no.

**\
Aaron Bockelie** 43:45\
Like RDP to it or something.

**\
Andrei Bosik** 43:47\
No, no, no, no, no. I need to install new separated machine and configure to work with all tools. Install your MCP, install software and authorize in those services.

**\
Aaron Bockelie** 44:01\
Yeah, but don\'t install the MCPS and stuff. You got to make sure what you\'re doing is the minimum, the minimum configuration that everybody gets.

**\
Andrei Bosik** 44:10\
Yes, yes, sure, sure, sure. That that they say yes, just a minimal list of software which will install it on each machine and work with this, yes.

**\
Aaron Bockelie** 44:25\
Does cloud code get MCP server for everybody installed?

**\
Andrei Bosik** 44:31\
Uh.\
Uh.\
Ask him as a word, please.

**\
Aaron Bockelie** 44:38\
Does is cloud code on everybody\'s computer configured with the Jira MCP server at the user scope level?

**\
Andrei Bosik** 44:45\
Yes.\
Uh, yes.

**\
Aaron Bockelie** 44:50\
OK.\
So then then that\'s a valid configuration because what you\'re what you\'re looking for is we want to make this this agent and the ways harmonious with the tools and configuration that it has in the environment.\
It\'s it. It\'s very it\'s like, uh.\
You ever written a large amount of like a whole book? Have you ever written a whole book or lots of chapters of something before about a story? A coherent narrative?

**\
Andrei Bosik** 45:26\
Yes.\
Yes, I write a book.

**\
Aaron Bockelie** 45:32\
So.\
So if you\'ve done that, you know that if you.\
Try to remove chapters, Chapter 7 out of the middle of your book. It breaks the whole thing. It breaks every single chapter from beginning to end, and you have to detangle it, right?

**\
Andrei Bosik** 45:44\
Sure, sure.\
Yeah.

**\
Aaron Bockelie** 45:50\
That\'s kind of what we\'re doing here.\
So we have to rewrite the entire narrative across everything, deintegrate it or integrate it, as the case may be, as we add more capabilities and features. So we have to be very careful and selective about what book we\'re writing with this.

**\
Andrei Bosik** 46:07\
Yeah, yeah, as I say, I create the clean machine. It\'s a the long machine where this is will will be integrated.

**\
Aaron Bockelie** 46:16\
Yeah.\
OK.\
So is it clear for next steps that we got to do then? Create the machine, try to go through these prompts and do it again.

**\
Andrei Bosik** 46:26\
Yes and yes, yes.

**\
Aaron Bockelie** 46:32\
OK.\
When do we want to meet up?

**\
Andrei Bosik** 46:39\
I think we need wait well.

**\
Aaron Bockelie** 46:44\
Just meet up tomorrow, same time.

**\
Andrei Bosik** 46:50\
Tomorrow.

**\
Val Levitan** 46:52\
Are we can\'t we continue today?

**\
Aaron Bockelie** 46:56\
Andrei has to do a bunch of technical configuration to have a clean environment. He does not have a clean environment right now.

**\
Val Levitan** 47:02\
I see.\
I see. Understood.

**\
Aaron Bockelie** 47:08\
But we have the prompts that we\'ll use. We\'ll just replay them again in a new session in this clean environment.

**\
Val Levitan** 47:16\
Understood.\
Um.\
Looking at tomorrow.\
Andre, I have a meeting with you booked for 8:00 AM.

**\
Andrei Bosik** 47:40\
Mhm, yeah.

**\
Val Levitan** 47:41\
Can we move our meeting for after with Aaron and book Aaron for 8:00?

**\
Andrei Bosik** 47:47\
Yeah, sure.

**\
Val Levitan** 47:49\
OK. Will you be able to clean your environment by tomorrow?

**\
Andrei Bosik** 47:55\
Sure, sure, yeah.

**\
Val Levitan** 47:57\
OK, so let\'s do that tomorrow at 8:00.\
I will send e-vites momentarily.\
Thank you everyone.

**\
Aaron Bockelie** 48:09\
Right. Thanks. Bye.

**\
Andrei Bosik** 48:09\
OK. Thank you and bye, bye.

**\
Val Levitan** 48:11\
Bye.

**\
Andrei Bosik** stopped transcription
