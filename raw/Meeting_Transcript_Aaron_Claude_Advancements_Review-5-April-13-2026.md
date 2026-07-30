**Claude_advancement_review_implimentation-20260413_092328-Meeting Recording**

13 April 2026, 01:23pm

7m 17s

**\
Val Levitan** 0:03\
The instructions to Andrei Bosik.

**\
Aaron Bockelie** 0:05\
So, if Andrei hasn\'t noticed\...\
Cloud Code Config on the repo for Aaron SB in GitHub is still the same. It hasn\'t been touched in a couple weeks now. I did make a couple cleanup things, but overall, nothing has changed or edited on Cloud Code Config.\
I forked it into a new project called AgentWays.\
which I put a link in the chat here for.\
In agent ways is the way I\'m going forward with building the tool. It is a high performance Rust binary first approach to agent control framework.\
And it\'s no longer a collection of bash scripts that is what Cloud Code Config was.\
Um, so\...\
The auto deployment that Andrei has set up watching the Git repo for Cloud Code Config has probably not updated anything in several weeks. And so he needs to go understand agent ways now because I\'ve shifted into that project instead.\
I see agent ways as the longer-term strategic.\
steering framework that I\'m going to be investing in to make sure that when I\'m doing other work that AgentWays is able to drive.

**\
Val Levitan** 1:25\
And so Andrei needs to figure out what agent ways methodology is, and then point his.\
Uh.\
I guess, what is it called, renewal, but deployment, deployment tools onto this new Aaron repository of agent ways.

**\
Aaron Bockelie** 1:41\
Deployment tools, yeah.\
Mhm.\
Yeah, a lot of it still works the same. So like the ways documents and the guidance and the whole, all that other stuff, that still exists just like it has.\
But the way it executes is very different now.

**\
Val Levitan** 2:05\
So is there a big change for Andrei?

**\
Aaron Bockelie** 2:08\
He\'s going to need to figure out how to get the binaries to run and compile. They\'re written in Rust so they can be cross-compiled to different platforms.\
I don\'t know how he wants to have that all execute, so\...

**\
Val Levitan** 2:23\
But it\'s something that we can breach tomorrow as well.

**\
Aaron Bockelie** 2:26\
Yeah, we can talk about that, yeah.\
Just, it\'s a different way of executing ways, essentially.\
But the core idea of writing a document, which is a way.\
Remains the same.\
Oh, keep the recording going.\
I\'m going to show you one other thing here.\
You can still see my browser, right?\
OK.

**\
Val Levitan** 2:58\
Yes, I can.

**\
Aaron Bockelie** 2:59\
So in hooks, in ways.\
in Software Dev, Architecture, ADR.\
So here is the ADR way, right?\
So we all know about ADRs at this point.\
Here\'s the description, the vocabulary, the disclosure threshold for the way, the pattern of it, and what it requires.\
This is what\'s called the front matter. And the front matter is essentially the thing that guides the tools how to use it. Like Obsidian files have front matter as well.\
So we can see here that there is this other thing that\'s very interesting.\
This is front matter, but in a bunch of other languages for the description of what it is.\
And every single one of these descriptions.\
is specially tuned with a multi-language inference cosine model, vectorization model that runs at runtime. That\'s why it needs a performance Rust binary rather than a bunch of scripts. And supports other languages. So we can see here, here\'s the Russian version of the description and the specialized tuning threshold

**\
Val Levitan** 4:14\
S.

**\
Aaron Bockelie** 4:23\
or the language model that triggers the way.\
These are all configurable. So what\'s going to happen is that Andrei and friends who are using this, when I encourage them to type their words in Russian,\
If the Russian language configuration is set, this vocabulary will trigger.\
still trigger the English language way, because the instructions are the same regardless of what language it is, right? But we have what is essentially A locale for other languages for native language speakers who aren\'t English. And so every single\...\
Way in here, like, here\'s here\'s commits, the git commits way, right?\
So the vocabulary that Git commits on, if I say any of these words, right? If I say, let\'s cherry pick a thing, or let\'s refactor, or let\'s refix, or let\'s make a branch, the commit way gets invoked into Cloud Code.\
just as if always it has been.\
But now we have\...\
Another way to say this, so if somebody says it, where\'s Russian?\
Could you do me a favor, Val?\
and just speak these words here.\
Can I just read through these?\
Let me make it bigger for you.\
So you can kind of just read these.\
And what I worked with is to make sure that the tuning for these words made sense to be able to trigger the threshold for the way for Russian. So if somebody who is a native speaker of Russian, who is natively typing in Russian, will trigger the commit way properly.\
So the steering and guidance is still the English block because I wrote that.\
but the way it gets triggered semantically means the same thing in these other languages.

**\
Val Levitan** 6:29\
Yeah, it actually does.

**\
Aaron Bockelie** 6:33\
So if you set your language to Korean and you say these words in Korean, it\'ll work there. Or in Japanese, or Italian, or whatever.

**\
Val Levitan** 6:43\
I\'m surprised you don\'t have it in Mandarin and Cantonese.

**\
Aaron Bockelie** 6:49\
So I actually have it in traditional Chinese right here.\
But I don\'t have it in the other variants right now. This was the language that makes the most sense for this right now.

**\
Val Levitan** stopped transcription
