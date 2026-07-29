**Clayton-Aaron-JVL-20260313_140034UTC-Meeting Recording**

March 13, 2026, 2:00PM

56m 22s

**\
Clayton Chancey** 0:08\
Oh.

**\**
0:32\
I agree then.

**\
Clayton Chancey** 0:32\
Hey, Lena, how\'s it going?\
Hey, I I have been sort of exploring.\
It.

**\
Lena Zhukova** 0:47\
Wait, you\'re freezing. You\'re freezing from time to time.

**\
Clayton Chancey** 0:48\
Is he?\
Exactly like, OK. Oh, really? Oh, hold on.

**\
Lena Zhukova** 0:53\
Mhm.

**\
Clayton Chancey** 0:56\
Let me see.\
I hope it\'s not my Internet. Let me see.\
Should be OK. Am I still breaking up?

**\
Lena Zhukova** 1:11\
No, not now.

**\
Clayton Chancey** 1:13\
No, OK.\
Um, anyway, I\'ve been.\
Thinking about this use case, I asked uh Aaron if he can join as well because.\
Almost like a year, actually more than a year ago now. Both he and I were really deep into a project that involved transcribing meetings in different languages and then stopped. You know, I I my project went a bit longer and his.\
Ended a bit earlier, but they were both in this use case and we have utilities that we wrote, but they\'re all kind of like self hosted solutions that live on your laptop, like an MCP server, like they live on your device.\
And so.\
I thought surely Microsoft Teams has a native Russian support.

**\
Lena Zhukova** 2:08\
OK.

**\
Clayton Chancey** 2:13\
But it seems like it doesn\'t so.

**\
Lena Zhukova** 2:15\
Yeah, it\'s very strange. Yeah, that\'s why like Russian IT people, they all trying to use some third party like tools and they they\'re actually like even the three tool. It did like pretty good job from from the I I was so surprised that.

**\
Clayton Chancey** 2:25\
Yeah.\
OK.

**\
Lena Zhukova** 2:34\
Teams did such a poor job.

**\
Clayton Chancey** 2:36\
Yeah, and that that\'s what I want to figure out before I.\
Put unnecessary time into it. It is. Is it better? Is it cheaper to just use a tool like Turboscribe, which I have actually heard from? You know, I never heard about it from a bilingual perspective, but just from just transcription. I\'ve I know people who use.

**\
Lena Zhukova** 2:48\
Mhm.\
OK.

**\
Clayton Chancey** 3:04\
it and like it. So it might be better.

**\
Lena Zhukova** 3:05\
The the problem is like our IT support guys, they told me that they it might be not secure because it\'s free, it\'s it\'s online, it might keep like our files somewhere and they are going to be like available for I don\'t know.

**\
Clayton Chancey** 3:21\
Hmm.

**\
Lena Zhukova** 3:22\
Um.

**\
Clayton Chancey** 3:24\
I think it\'s pretty. I think it\'s pretty secure, but I mean if we wanted it to be really secure, I know that Turboscribe just uses the.\
The same Whisper API, which is what both Aaron\'s project and my project were built on. It\'s it\'s also open API, open AI, which is the same thing that Copilot uses. It\'s the same thing that Microsoft Teams uses. It\'s all just.

**\
Lena Zhukova** 3:44\
Mhm.\
And.

**\
Clayton Chancey** 3:54\
The strategy that they use to actually transcribe the audio will basically determine the quality. So hey Val, how are you?

**\
Lena Zhukova** 4:06\
Hello.

**\
Val Levitan** 4:08\
Hey.

**\
Clayton Chancey** 4:08\
I asked. I asked Aaron if he could spare a few minutes to join at some point this morning too, because this use case around the transcription is.\
Interesting. And he I was telling Lena that both Aaron and I, maybe like a year or a year and a half ago, were both independently working on transcription projects that were sort of related to this.\
And I was really.\
Surprised to hear that like Microsoft Teams and even Copilot don\'t support Russian terms the way that they do with other some of the other languages that are even.\
Like Tagalog and stuff, which is also similarly dialect heavy, so.\
Um.\
Oh.\
One of my questions though, was around.\
Are these transcripts?\
Like what percentage of the terms that are used in the like if you were to say here\'s a here\'s an entire meeting transcript.\
What percentage of the spoken words in that transcript would actually not be in the same?\
Dialect or the same consistent? Not even. I don\'t mean like accent, but in the same exact.

**\
Val Levitan** 5:48\
A question.

**\
Lena Zhukova** 5:49\
Up to up to 30%, up to 30.

**\
Val Levitan** 5:51\
I I I question, I question whether it\'s the right question to ask.

**\
Clayton Chancey** 5:57\
Why is that?

**\
Val Levitan** 6:00\
Because even if the percentage is radically smaller, then it it\'s not really the percentage, it it\'s the immediate skew of the subject like it\'s a, it\'s a.

**\
Clayton Chancey** 6:04\
Mhm.

**\
Val Levitan** 6:16\
Black hole. It\'s like becomes a hollow.\
Misunderstanding of what\'s going on.

**\
Lena Zhukova** 6:23\
Yeah, it\'s losing context. Uh, very fast and the but the problem also not only in this terms which we are like uh uh saying in Russian some like English words, but it\'s even like it\'s not good transcript for just normal Russian.

**\
Val Levitan** 6:26\
The.

**\
Lena Zhukova** 6:41\
Speech. So Turbo Transcribe did like job like I don\'t know like times better, times better so.

**\
Val Levitan** 6:52\
Well, I use I I use whisper transcribe. That\'s that\'s the best that there is, but still.

**\
Clayton Chancey** 6:52\
Well, here\'s.

**\
Val Levitan** 7:04\
The the skewing of the direction of the conversation the moment you start using slang.\
It\'s just wild. It\'s the the moment you correct like what I do, I read this transcript, catch those words and and then I run another transcript. I explain what it is and then run another transcript. The difference is huge.

**\
Clayton Chancey** 7:28\
Yeah, well, so the reason I ask.\
That process you just described is what Whisper, Transcribe and Turboscribe are doing behind the scenes. They\'re all parallel processing all of these transcripts, and there\'s all this like prompting logic that\'s behind the scenes that\'s taking place because.\
The whisper model is not a large language model. It\'s like a different type of AI that is just correlating waveforms with words in in.\
A attention mechanism of different languages and language libraries. So basically like there\'s two problems with these types of scenarios and the one that always seems the most important is how to get this transcript.\
Into the large language model world where now Claude can interact with it and understand. But then the the cleaner, better way to solve the problem is to get the transcript very tightly focused on recognizing and just transcribing different terms.\
And the reason why Microsoft Teams does such a bad job is because in an effort and they all of these services all use the Whisper API, they all use the same transcription service that they consume. And so does the project that I\'ve worked on before and the project that Aaron worked on before. They\'re all Whisper API. It\'s the only.\
Cost efficient way to transcribe. The difference is that Microsoft Teams just transcribes the whole thing once and puts it out there. And the way that they do it is if someone uses a term which is unrecognized.\
And in the in the whisper model, if that term is recognized with a low confidence score in the and I\'m sort of almost oversimplifying how it works. But basically if someone uses a term like if I started like I speak this dialect of Juba Arabic from when I lived.\
In Sudan, if I started speaking that right now, there\'s probably less than 1% of all Zoom meetings and recorded audio in the world that Whisper has ever been trained on that has Juba Arabic in the mix. Ever. It\'s just a dialect.\
And if I use that word Microsoft Teams, what it will do is it will try to correlate those words to Latin loanwords.\
Birds.\
And this is just the strange magic of what\'s happening behind the scenes. And so it\'s basically translating that to Latin and then translating them back into English, which is what, which is for some reason what Whisper does on the first process.\
And So what you have to do is you have to say, and Microsoft Teams just does not do this because it\'s it\'s slightly more expensive to do this. But there\'s so many, you know, millions and millions of people doing Microsoft Teams meetings every day that it\'s very expensive for Microsoft to offer this.\
But Turboscribe will do this, and people have different strategies. They basically take that audio and they\'ll run it through once, twice, and again. And this will give you a very clear definition of which terms are uncertain, because if three different transcripts say.\
This particular term, we don\'t know what it is, then we know it is some other thing that means something else and then we can defer to prompting and say in this and if we could just say in this context.\
There\'s a 99% certainty these people are Russian. This is the specific organizational context. They\'re talking about this and then you do 2 passes of that, then it will get it. And so that\'s the value of like custom whisper solutions.\
And Whisper is extremely cheap. The question in my and that would be like, it\'s pretty easy to just vibe code that honestly, cause Whisper is so easy to interact with. But the question would be whether it\'s actually easy to.\
Add such a solution.\
Into the JVL stack somewhere that makes sense and then plug that into the process. Or if it would be actually cheaper and easier to just use a tool like Turboscribe or something that\'s commercially available that is just a license.

**\
Lena Zhukova** 12:05\
I got pretty good result is through Turboscribe. So I extracted audio from video meeting recorder. I I used MP3 file. I loaded to this Turboscriber. Good. OK transcript not not not not good but OK much better than teams did and then I.\
I took this transcript and our taxonomy vocabulary and loaded to AI and then after that I got almost perfect. Oh, several mistakes, but almost perfect.

**\
Val Levitan** 12:38\
I prefer. I prefer to have our own slang to English document.

**\
Clayton Chancey** 12:39\
Yeah.\
Yeah, yeah. Well, yeah, we need that no matter what.

**\
Val Levitan** 12:48\
And then and then and then.\
Yeah, and and then deal with full audio just like Lena does. But I would use whisper overlap it with our kind of a knowledge base.

**\
Clayton Chancey** 12:58\
Mhm.\
Mm-hmm.

**\
Val Levitan** 13:06\
Which is our slang dictionary.

**\
Clayton Chancey** 13:07\
Yeah.

**\
Val Levitan** 13:10\
And move from there, but I don\'t see how teams could work for us.

**\
Clayton Chancey** 13:11\
Yeah.\
Yeah, well the nice thing is no matter what we need them, we need the mapping document Val that you that you mentioned in teams already. Like we need that because we can give it to a whisper solution and that will actually help it transcribe.\
And then to be extra sure, we give it to Claude as well through the and I can actually just bake that into that MCP server in a way that if it\'s processing a transcript, it\'s just in the MCP and it can pull it down from GitHub if that\'s where you should, which is where you should host it, of course.\
And that way we\'re covered on both ends so that hopefully the quality of the transcript is much more accurate, but then even in cases where it is missing things, still Claude, which is of course very intelligent compared to Whisper.\
Should be able to recognize and.\
The only fine, the only fine tuning I think we might need to do is there might be cases. I\'m I\'m just I\'m really saying this more for myself as as I\'m solutioning here, but there might be cases where the whisper API.\
Unsuccessfully. It\'s not really transcribes, but transliterates. Do you know you guys know what I mean? The difference between like transcribe and transliterate?

**\
Val Levitan** 14:40\
I I think I understand, but I\'m not sure. Maybe you should explore.

**\
Clayton Chancey** 14:41\
Like.\
That to transliterate is. In my mind, transliterate is.\
To attempt to spell a word in the phonetics of another language. So if I wrote in English PRIVYET, which is in English letters saying privyet, that\'s like a transliteration.\
As opposed to writing in the Cyrillic text, a Russian term, and so there will be times when.\
The transcript that we might get on the other side will have transliterated terms and and they will probably be inaccurate because it\'s kind of reading or or transliterating into a a language that may not have the full.\
Nuance and so we need to arm Claude against that.

**\
Val Levitan** 15:35\
But but but why? But but let\'s say we have a transcript, right? And I\'m just thinking out loud for myself and and the reason I\'m asking this question is because very frequently I would put.

**\
Clayton Chancey** 15:41\
Cool.\
Mhm.\
Of course.

**\
Val Levitan** 15:51\
Weird expressions that I\'ve heard my grandmother say that, you know, in some.

**\
Clayton Chancey** 15:55\
Sure.

**\
Val Levitan** 15:58\
Crazy thing into Claude and say what does it really mean? And Claude would explain it, would find a way, right? So I\'m saying to myself, OK, so we are in a meeting and somebody is using something that is, let\'s call it, not.

**\
Clayton Chancey** 16:00\
Yeah.\
Yeah.\
Right.

**\
Val Levitan** 16:15\
Current conventional language, you know, acceptable. Whatever it is, doesn\'t matter. Leave it in an audio form.

**\
Clayton Chancey** 16:20\
Mm-hmm.\
Yeah.\
Mhm.

**\
Val Levitan** 16:26\
Like don\'t digitize it, just leave it in that analog audio form and that piece together with already well organized transcript goes inside Claude and Claude decides what to do with it.

**\
Clayton Chancey** 16:31\
Mhm.\
I don\'t think Claude can handle.\
Long form or high volume audio clips well enough, but I could be proven wrong. I might be wrong there.

**\
Val Levitan** 16:53\
No.

**\
Lena Zhukova** 16:55\
No, no I I I tried it. It asked me to it it I can upload audio file but it ask you add to this transcript as well. So when I when I have audio and transcript then I can work with it.\
And once I loaded this audio file and this is good transcript from so then did a good job but just MP3 file he said I cannot analyze.

**\
Clayton Chancey** 17:29\
Yeah, \'cause Claude uses the Whisper API to to transcribe files that you upload.\
So maybe there\'s some exerimentation here because.\
This is a good example of like there\'s domain expertise which is.\
The ability to fluently use Russian slang and and audit it and understand how good the the transcription is that I don\'t possess.\
Um.\
1.\
Let me build the lowest effort pipeline which I can have. I can send it back to you today by the end of the day, which takes audio and is optimized for this use case. I have to take this Microsoft Teams transcript of our conversation here. I\'ll give it to Claude.\
Code and it\'ll build off of the existing project that I have and I\'ll send it to you guys and then.\
If Lena or or Val or both, if you could send me three to five examples and if it\'s audio files or even Microsoft Teams meeting or I can download the the audio file.\
Just out of some meeting and and in my mind, ideally it would be something that has a lot of code switching where there\'s some English terms, there\'s modern conventional Russian, and then there\'s also some crazy old.

**\
Lena Zhukova** 19:10\
Yeah, I can send you an MP3 file immediately from we had like load meeting that was like about 50 minutes and we used a lot of mix of Russian and and do do you need my taxonomy vocabulary as well?

**\
Clayton Chancey** 19:12\
Yeah.\
Great.\
Yeah, I mean, that\'d be very, very useful. Yes. Yeah. I\'ll just build the minimum viable product as quickly as I can. I\'ll try to send that to you by the end of the day or in the worst case, tomorrow, you know, on Saturday morning.\
And then and then I would like to get your gut reactions as to how it is, because what I want to avoid is like reinventing a wheel that you can you can get somewhere else cheaply with lots of time. So let\'s just try something, see how close it is if it\'s good.\
Then we can invest a bit more time into it because that seems like the the final piece to unlock this like this flow we\'ve been talking about from a complex and in this case my, you know, multilingual and as we all know with the with the language at that level, it\'s also like lots of cultural.\
Assumtions that are going into things, all cultural as well, bringing all of that filtering into a JIRA hierarchy, and that\'s a pretty amazing flow. But if we can get this piece worked out.\
Then um, that\'s a very.\
Useful solution. So anyway, long way of saying let if you send me thank you, I got that file you sent. If you have any others like I\'ll download this now and if you have any others.

**\
Lena Zhukova** 20:47\
And this is an Excel file. It\'s all the way.

**\
Clayton Chancey** 20:47\
That are similar.

**\
Val Levitan** 20:49\
What?

**\
Clayton Chancey** 20:50\
OK, perfect. Let me organize myself here.\
Quickly, if you think of others or you have others that you want to send, then feel free to send them because the more.\
Test cases that the easier it is to just quickly test and iterate. And I will, you know, I will lean on Claude\'s understanding of some of this and then I\'m gonna refer quickly to you.\
For your expertise, JVL Whisperer, I\'m just moving this over to a project file so I can get this built out.

**\
Val Levitan** 21:36\
So I see this as a.\
Like a a service that is called for every call, right? So we do not press record anymore on teams, but every time we organize a a meeting.

**\
Clayton Chancey** 21:54\
Yeah.\
Yeah.

**\
Val Levitan** 22:01\
This another caller, you know, AI caller logs in and records the meeting, right? That\'s that\'s how we see.

**\
Clayton Chancey** 22:06\
Mhm.\
Probably it\'s possible. I have to align the solution, but probably what it would be is instead it will probably be you do hit record, you hit record on Teams, but our service goes to Microsoft Teams.\
And grabs the audio file and ignores the transcript and then sends a follow-up e-mail that says actually here\'s a better transcript. That is actually much easier than building like a a whole bot that joins the call for you for which you have to host a microservice. And so this would be.

**\
Val Levitan** 22:30\
Well.\
OK.

**\
Clayton Chancey** 22:42\
Essentially free to operate because Whisper is so insanely cheap. You know, hundredths of a cent per meeting, so.\
So probably you would continue using the record button and then our service would go in find the meet that Microsoft Teams meet.\
And then grab the audio file and transcribe that with our own technique and then store that somewhere. And the the trick, the question that I have to maybe determine would be where where should we save that? It would be very convenient I think to just go ahead and save it to a nice.\
Big old GitHub repository that becomes the enterprise brain and then we sort of bypass Microsoft Teams and make that transcription process the the pipeline for storing transcripts now and we trust it more anyway.\
But then it should also go out to all the participants of that meeting and sort of supersede the existing Microsoft Teams transcript in many cases. So I have to think about that a bit more, but.\
OK.

**\
Val Levitan** 23:58\
OK, so.\
As a form of an alignment between us, where are we now and what did we achieve in the past month?

**\
Clayton Chancey** 24:11\
So what we have is we have a very specific MCP server that can take a good transcript and auto populate.\
A very accurate hierarchy of JIRA tickets and upload images and associate correct descriptions with all of that based on the existing conventions in JIRA.

**\
Val Levitan** 24:45\
Specifically aligned with how things are done right now in the game development department.

**\
Clayton Chancey** 24:54\
Yes, yeah.

**\
Lena Zhukova** 24:54\
That\'s I actually I wanted to discuss it with you because yeah, because when I set a good transcript I uploaded to Claude. I I used like pretty like simple prompt which I like. It was short and simple it.

**\
Clayton Chancey** 24:58\
Mhm.\
Mm-hmm.

**\
Lena Zhukova** 25:14\
Created a pretty good recommendation here. It recognized the problem files, I mean images, JPX. They should be in desktop. It\'s not recognized in my folders, but it\'s OK, I moved just the whole folder.\
Of comparts for this game, for Dragon based game, I moved it to desktop and I used this folder in a like so. OK, it\'s it\'s minor inconvenient because usually it\'s always I can always make a copy of this folder to desktop.\
It\'s my main convenience for this case. It might be bigger inconvenience for case when we work, when for example we discussed several games during meeting and we need to make changes in several IPS and in this case it will be big and convenient because I I I will need to go in different.

**\
Clayton Chancey** 26:02\
Mm-hmm.\
Yeah, yeah.

**\
Lena Zhukova** 26:12\
Folders and copy it to desktop. In this case it was OK because I just copied 1 folder but still it sees it sees only what what it should be in like user name of the user desktop folder.\
That\'s only that\'s the only way it can access files. It it created a couple of mistakes losing context. I asked. I asked to fix it on the way. Then I I asked to start to create it in sandbox and it\'s.\
It creates in sandbox. I mean, it\'s not 100% accurate. I had to know how to work with it because it\'s kind of like inconsistent mistakes. Like for example, like for this feature, it rather pays main game character.

**\
Val Levitan** 26:49\
Mm-hmm.

**\
Clayton Chancey** 27:06\
Mhm.

**\
Lena Zhukova** 27:07\
Took description for this feature. I don\'t know from where because it it was not in in chat, it was not in the set. So I think it copies it from some other issue in existing.

**\
Clayton Chancey** 27:14\
Mm-hmm.\
Hmm.

**\
Lena Zhukova** 27:23\
It and it\'s relevant. That\'s that\'s what interesting. Yeah that\'s that was one mistake like structure of story like features was pretty good and stories inside most of descriptions are accurate but there are like again like still some mistake and interesting that for example.

**\
Clayton Chancey** 27:25\
Oh, OK. OK.

**\
Lena Zhukova** 27:42\
For this feature like toppers, it first it\'s only attached only one image for one topper and when I ask to attach.

**\
Clayton Chancey** 27:53\
Mm-hmm.

**\
Lena Zhukova** 27:58\
Because there is 3 story here like topper for game logo, topper for free spins and topper for big win celebration. When I asked to attach images to other stories, it did it, but somehow it told me like I I cannot do it.\
So like to get this image attached you you you have two options, manual attach or fix MCP connector. But it it did it. Why? Why? It said me like it\'s impossible. That\'s that\'s so strange.

**\
Clayton Chancey** 28:30\
Yeah, what? What? This is maybe a strange question, but what day was this that like in the last week or so that you?

**\
Lena Zhukova** 28:40\
Oh, I I think last changes so like I did a couple of days ago.

**\
Clayton Chancey** 28:51\
OK, yeah, there\'s a big Claude code outage and both Aaron and I noticed Claude getting.\
Dumber for a day or two, for a for an hour or two there.

**\
Lena Zhukova** 29:04\
Oh, seriously. Interesting.

**\
Clayton Chancey** 29:06\
Um, no. But there\'s also, uh, another.\
Feature that I added and I\'m not sure if it\'s working here. You can also try to pull down the latest version, but that\'s um.

**\
Lena Zhukova** 29:19\
Mm-hmm. Let\'s do it. Yeah, let\'s try. I will close call, call desktop.

**\
Clayton Chancey** 29:25\
No.\
But that also what it will do is it will just. Actually I think this was working already. The last time we did this was to quiz. It should quiz you like if there\'s ambiguity that it should ask you questions and give you.\
Like options. So did it? Did it also like ask you clarifying questions throughout that process?

**\
Lena Zhukova** 29:50\
No, it mostly it asked me when it started to create issues. Most question was allow, so asking to allow me to create something. Yeah, so it was, yeah, it was a lot of questions like this. I did not press always allow because I wanted to.

**\
Clayton Chancey** 29:59\
Just to approve, but they didn\'t ask you. Hmm.

**\
Lena Zhukova** 30:10\
Because it was like first time I wanted to see what is going on. So it was a lot of questions like I like allow this time, allow this time. But it was like mostly these questions and like this was like mystery for me like this is images. It did it. So I asked to attach image like lost images. It did it properly.\
But it says to me like go and do it manually, right?

**\
Clayton Chancey** 30:34\
Yeah, yeah. Well, that\'s the, I mean, that\'s.\
That particular thing is sort of the laziness of the task, which is one reason why I designed it to to ask you to approve, but it should. It should also ask you like.\
Like multiple choice questions. If there is, if there\'s something that it finds to be ambiguous or unclear about the requirements, it should say, you know, I don\'t understand.\
Between options ABC and D, which one did you mean? And it should give you options. Did you encounter that at all?

**\
Lena Zhukova** 31:21\
Hello.

**\
Clayton Chancey** 31:23\
Test.\
Let me just check if that works.

**\
Lena Zhukova** 31:29\
OK and.

**\
Clayton Chancey** 31:33\
Um.

**\
Lena Zhukova** 31:35\
We we need to pull uh.

**\
Clayton Chancey** 31:38\
Let me just see quickly if that\'s in there, because I think I remembered the last time that we worked on this, it did that for you in a cloud desktop session. So my guess is that if we ran that same test again in co-work or in desktop, I think it would.\
I think it would do better now because there was this cloud code outage and Claude Co work is basically cloud code behind the scenes. But let me just check before you do anything and see if those if that quiz feature is actually pushed and when I pushed it because then that would confirm something for me. So let me check.\
Check really quick.

**\
Lena Zhukova** 32:18\
But I was pretty happy like that it attached like all images it it did it properly according to like stories and features. So it was it was good result and structural features and stories was good but descriptions description unfortunately not 100% accurate.

**\
Clayton Chancey** 32:38\
Mhm.

**\
Lena Zhukova** 32:38\
We.

**\
Clayton Chancey** 32:53\
Yeah. So I did actually push that almost two weeks ago now. So I think, I don\'t think there\'s a new poll for you to do. I think, I think if we.

**\
Lena Zhukova** 32:56\
Oh, OK, so we don\'t need to.\
Uh, OK, OK, OK.

**\
Clayton Chancey** 33:06\
You know, and I it\'s.\
And you said that was with a with a good transcript where everything was very was very clear. OK, well, we can keep refining on that. I think generally with things like this it is good to break it into chunks. So what I might also try.

**\
Lena Zhukova** 33:12\
It was just good. That was good, yeah.

**\
Clayton Chancey** 33:28\
Uh.\
In addition to the transcript thing that we already finished talking about, I might also try a little bit of prompting in this MCP to use sub agents.\
Um.\
Which would which would actually probably help with cause such a long running task. What it\'s doing here it\'s taking your transcript, it\'s going and and this is also part of what our agent is doing is it\'s going in and researching the active convention. So rather than hard coding into our tools.

**\
Lena Zhukova** 34:08\
Mhm.

**\
Clayton Chancey** 34:09\
Oh, here\'s here\'s how all these IP and these game structures look in Jira. Here\'s how it should work. We actually just tell the tool, actually go research it and go find the latest one and and decide what is the good structure to use.\
So that as you change and improve your ways of working the tool, we don\'t need to just update this text in the in the back of the tool. So it goes and does this research and then it plans what it should structure and then it it goes and executes and that\'s a very long running task.\
And probably as it gets really, really far into that task, it might start just making decisions on its own about here\'s what the here\'s what I think the description should be. And a way to to preserve the groundedness of that would be to break that work up.

**\
Lena Zhukova** 34:54\
Damn.

**\
Clayton Chancey** 35:03\
Into sub agents and now cowork. Cowork can do sub agents and it used to be that like really only Cloud Code does that very well and now Cowork does that pretty well and I think even Cloud Desktop can like also do that pretty well.\
O we can.

**\
Lena Zhukova** 35:19\
But uh, it doesn\'t mean I need to break uh uh transcript in in several pieces and we\'ll want to.

**\
Clayton Chancey** 35:24\
No, no, no. It would just break that that process that I described into different sub agents and then the instance of Claude which you are talking to is sort of orchestrating other agents so that so that.

**\
Lena Zhukova** 35:30\
Huh.\
Mhm.

**\
Clayton Chancey** 35:41\
The context of the chat, if you will, is not degrading over time so that it\'s attention is not degrading. So Claude would say, all right, I\'m going to dispatch a sub agent to go read the transcript and develop a plan and then it will and then an agent will do all.\
All that work and spend lots of time. It\'ll be very high quality, but then that\'s all it has to do. It doesn\'t have to save more context, if you will, to then go and execute everything. It just brings that back up and now that chat is done and the plan is presented to you.\
And then if you like it, if you if you agree, then another sub agent goes and now researches. All right, cool. What\'s the structure in JIRA which I should use and it presents back to you. And each one of those phases of the workflow is its own.\
Session and so this I have seen. This drastically improves the quality of basically the reasoning quality over a long duration task and this is maybe it\'s complex enough that this is.\
Something we should try, so let me try that.\
And and basically my explanation is this is almost more work to explain it than it is to actually make the change. Because what this the way that you do this in Claude is you basically say hey Claude.\
Use sub agents to do this work. And so basically adding one sentence or maybe emphasizing this very clearly in our MCP prompting, it will sort of invoke that Claude should approach this task.

**\
Lena Zhukova** 37:10\
Mhm.

**\
Clayton Chancey** 37:24\
Which we\'re giving it in our MCP prompting using sub agents and and I suspect that that would improve the quality, but it will also the other thing it will do is it will also require more of you.\
As the user, because the intensity of it, of the confirmations and the approvals, it will be very fast and it\'ll be like a barrage and there will be lots of questions, but it will be much faster. So I mean that\'s the general.

**\
Lena Zhukova** 37:55\
OK, I will try to. I will try to use this from.

**\
Clayton Chancey** 37:58\
Yeah, yeah, so all. So just for the notes that are that the the recording here for my and for myself later today.\
Add some sub agents to the MCP prompting so that we get Claude to reliably invoke sub agents and we should hopefully see as a example of a reasoning improvement. We should see more accurate descriptions.\
And and you know, it shouldn\'t hallucinate its lack of image capabilities. And then secondly, maybe more importantly, we are.\
Aaron, this is the PC. You kind of missed it, but.\
Exploring the idea of a custom whisper.\
Integration that sort of intercepts some of these bilingual slang riddled Russian conversations that grabs the audio from ideally from Microsoft Teams, but I down there\'s in the chat I downloaded. I could share with you an example of one MP3 file.\
That\'s an example of that, and Lena has provided a spreadsheet that\'s a taxonomy of many of the terms that they use that might be slang and what they should translate to in English. And unfortunately the Microsoft Teams feature that\'s like kind of the copilot dictionary or whatever. It\'s basically meant to like post train their whisper.

**\
Aaron Bockelie** 39:12\
Yeah.

**\
Clayton Chancey** 39:31\
Process explicitly does not support Russian. Yeah, right. Yeah, yeah, gotta love it. So.

**\
Aaron Bockelie** 39:31\
Right.\
Huh. Gosh, I wonder why.\
Politics.\
Yeah.\
There are really good. So there\'s a lot of like fine tune Russian models in whispered in the various transcription, yeah.

**\
Clayton Chancey** 39:47\
Um.\
Yeah. So my thought was just what I what I committed to was very low level MVP because you and I have both done a lot of whisper stuff before. Just take that example that she gave us the taxonomy and spin out a quick little whisper thing where we can test a pipeline and just try.\
I like what if we got audio like that, which would be stored in the Microsoft Teams record. Anyway, we could pull through the Graph API. What if we took those audio files and then just did our own quick process of it and it might be a couple runs of whisper to get it to a place where it makes sense with some prompting and everything but.

**\
Aaron Bockelie** 40:21\
Yeah.

**\
Clayton Chancey** 40:33\
If we do that, then submit those transcripts to GitHub as the actual transcript record for JVL and then the Microsoft Teams auto-generated one is pretty reliably pretty pretty unreliable.\
Um.\
So I committed to just not spend a lot of time on that. Maybe it\'s like an hour or less of my time since I have all those templates and we\'ve I\'ve done all the, you know, the scribe and all the different things I\'ve messed around with. You\'ve got your thing and then.

**\
Aaron Bockelie** 41:06\
Yeah.

**\
Clayton Chancey** 41:08\
If it makes sense and it\'s, you know, it\'s obviously going to be a lot cheaper and more secure than trying to find a subscription service to pay for for everybody, then then just integrate that in and we can even use N8N as a good example of a place where we can just have that flow going.

**\
Aaron Bockelie** 41:25\
Right. I think that\'s actually a really good place to be because it\'s sort of it\'s just hosted and it doesn\'t. We don\'t have to worry about execution and a lot of other the way it runs, it just becomes kind of a a low, a low code service to run it on.

**\
Clayton Chancey** 41:36\
You are hosting or anything.\
Yeah, and it\'s just it\'s in the cloud, does its thing, it talks to the whisper API and then we can do the the sort of back and forth like the loop where you it\'s a whisper API, but it\'s also like there\'s some API like AI large language model calling in there, yeah.

**\
Aaron Bockelie** 41:52\
Yeah.\
Give it the brains to kind of filter and refine it appropriately, yeah.

**\
Clayton Chancey** 42:00\
And then that\'s where we can inject that taxonomy, which is a spreadsheet that goes just right in there as a binary file that just gets re-injected every time. It\'s just it becomes very easy, like plug and play. So that would be my hope of go for it, go for it.

**\
Aaron Bockelie** 42:11\
My wife\'s calling me. I gotta. I gotta run for a minute, guys.

**\
Clayton Chancey** 42:15\
So anyway, I know that\'s a lot of back and forth, but that\'s a very, very quick hit and then hopefully by.\
By next week we\'ll we would be able to determine once and for all with your, you know, expertise in hearing Russian and knowing whether it makes sense to translate it in a certain way. You can then listen to the outputs of that and then say.\
Like, how does this compare? Is it worth ursuing? If so, then it\'s a very, very quick shift to just turn it on for everybody.

**\
Lena Zhukova** 42:54\
And you recommendation to add to the prompt use sub agents to this work. It\'s on a stage when I\'m asking for a plan or it\'s on a stage when I\'m asking to do like real creation of features and stories or or both.

**\
Clayton Chancey** 43:11\
Well.\
Well, I would add it so so in in the MCP server there are also prompts in the MCP server. So I\'m not. I\'m not actually talking about your user prompt where you as if you should add it in yours. I would basically add it in the MCP server so that you don\'t.

**\
Lena Zhukova** 43:29\
No, OK. OK.

**\
Clayton Chancey** 43:33\
I have to add it. So let me just it\'s a it\'s a quick change I can make and then I will.\
Commit that to the JVL GitHub where that MCP is stored and then send you just like. I mean you\'ve done it many times now so you you probably know, but just send you some instructions on how to pull that down and you can check cloud desktop and see if it works again so you so that way you don\'t have to like tell it to use.\
Ubagents every time it will just it will always naturally use subagents when you are using that articular tool in clock.

**\
Lena Zhukova** 44:08\
Thank you.

**\
Val Levitan** 44:10\
So one one more issue.

**\
Clayton Chancey** 44:10\
Yeah.\
Mhm.

**\
Val Levitan** 44:18\
Mm.\
So when when we are.\
When we want simultaneous access during prompting to Jira and GitHub, we for GitHub we use something that I was introduced to called.\
GH.\
Uh MCP.

**\
Clayton Chancey** 44:42\
Mhm.

**\
Val Levitan** 44:44\
And this is, from what I was told, the only MCP that is able to look at every repository within the organization. All other MCPS for some reason are quite limited.

**\
Clayton Chancey** 44:59\
Yeah.

**\
Val Levitan** 44:59\
But the problem with and the the problem is that this GHMCP works only within cloud code.\
But not Co work.

**\
Clayton Chancey** 45:14\
Um.\
OK.

**\
Val Levitan** 45:22\
But the benefit of cowork is that it could the cowork could look at your local files.\
And so it becomes a three-pointed prompt, your local files, Jira and hopefully GitHub.

**\
Clayton Chancey** 45:31\
Yeah.\
Yes.

**\
Val Levitan** 45:44\
So how do we get that GHMCP for cohort?

**\
Clayton Chancey** 45:52\
Well, a couple of things. First I will note.\
That in Lena\'s case, I don\'t know if this is.\
There are many good reasons to use cowork, like you said. In Lena\'s case, the only reason that we must use cowork is because she\'s on a Windows machine and in Windows cowork.\
Is the only way for you to access images and send them through to JIRA.\
So this same task that Lena is doing if if you had another user that was using Mac they would not, they would not need to use Co work. They could use Cloud desktop for all of this. So but I agree with you that Co work is very.\
High utility because it\'s like cloud code, but it has a user interface.

**\
Val Levitan** 46:58\
Well, cloud, cloud code. Oh yeah, but yeah, you\'re saying cloud code could actually look at your local files as well, right? That\'s what you\'re saying.

**\
Clayton Chancey** 46:59\
And.\
Oh yeah, yeah, yeah. Cloudcode does that far better than Cowork does.

**\
Val Levitan** 47:13\
Yeah, so OK, so I don\'t even need it.

**\
Clayton Chancey** 47:19\
Yeah, if you use cloud code, I I basically see cowork is sort of a a middle ground.

**\
Val Levitan** 47:28\
Yeah, it\'s a cozy. It\'s a cozy environment.

**\
Clayton Chancey** 47:31\
Yeah, it\'s it\'s cloud code for people who are in unfamiliar with the terminal interface.\
Which is or or or people who don\'t want to work in there for like normal knowledge work, like writing emails and chatting and things like that, which to be fair is is plenty of people so.

**\
Val Levitan** 47:43\
Would be intimidating.\
Oh.\
OK, I\'ll I\'ll part my question for now that it\'s it\'s not relevant. I I need to experiment more. OK, but focusing on Lena, I think the undertakings are clear, but the overall course or the objective is to take a conversation.

**\
Clayton Chancey** 47:56\
Yeah.\
Mhm.\
Mhm.

**\
Val Levitan** 48:15\
Immediately turn it into.\
Um.\
Actionable items for JIRA.\
With the outmost efficiency.

**\
Clayton Chancey** 48:28\
Yep.

**\
Val Levitan** 48:29\
And so our objective here, our goal here is to cut down on the, we call it good necessary bureaucracy, but make it very efficient and practically bring it to 0 cost as much as possible.\
0 overhead as much as possible. That\'s that\'s our objective. And so we\'re we\'re probably what, a week away.

**\
Clayton Chancey** 48:46\
Yeah, Yep, right. Yeah, yeah.\
Yeah, I mean, I think this transcription piece is really the final piece because the JIRA structure having.

**\
Val Levitan** 49:04\
Assuming assuming that multiple agents will improve Lena\'s prompting.

**\
Clayton Chancey** 49:13\
Yeah.\
Yes, yes.

**\
Val Levitan** 49:16\
The not prompting, but the output from the prompting. If that really improves on a longer transcript, then of course that\'s that\'s great.

**\
Clayton Chancey** 49:20\
Yeah.\
Yes, Yep. And the JIRA record, all of those tickets, that is sort of the good bureaucracy in this, in this process is like having all of that knowledge work and those orders stored and organized and it\'s quite complex.

**\
Val Levitan** 49:42\
So I just want to let you know what. I just want to let you know what the next step is. So every time Lena will be opening feature branches, sorry features, features, these features need to then.

**\
Clayton Chancey** 49:43\
And so having that.\
Mhm.\
Mhm, mhm.

**\
Val Levitan** 49:58\
Get linked to GitHub.\
And and whatever Lena\'s execution, final execution of a feature, meaning feature is completed, done, the result of it should be an artifact.

**\
Clayton Chancey** 50:03\
Yeah.\
Mhm.

**\
Val Levitan** 50:17\
In GitHub.

**\
Clayton Chancey** 50:18\
Yeah.

**\
Lena Zhukova** 50:19\
But not in 100% of times because uh for example like now like you\'re doing production and uh in this like this production is not.

**\
Val Levitan** 50:28\
Yes, yes, yes, yes, yes, yes. Right. Right now we\'re working. We\'re working in uh.

**\
Lena Zhukova** 50:32\
M.\
Oh.

**\
Val Levitan** 50:38\
And it is, it is on the way out. This is a we\'re kind of adapting right now to a dying substance while we are ramping up the the new way what we call Omni framework. So understood.

**\
Lena Zhukova** 50:38\
Oh.

**\
Clayton Chancey** 50:47\
Yeah.\
Right, right.

**\
Val Levitan** 50:55\
The this current framework that Lena is referring to, that is in SVM, but that\'s a kind of a dying thing and we\'re not worried about it. The new framework, whatever is opened in.

**\
Clayton Chancey** 51:05\
Mhm.

**\
Val Levitan** 51:10\
JIRA as a feature becomes a branch in GitHub and done, meaning we have a set of final artifacts and.

**\
Lena Zhukova** 51:16\
No.

**\
Clayton Chancey** 51:25\
Yep.

**\
Val Levitan** 51:26\
And GitHub is also a versioning control. So as we go through versioning of artifacts, it keeps on accumulating.\
In GitHub, but eventually when feature is completed and then resolution is done, that\'s the final artifact. So yes, yes, correct.

**\
Clayton Chancey** 51:38\
Yep.\
Yep, Yep, that\'s the CICD.\
Approach. Yeah, yes, which is, which is. And the beautiful thing about this is.

**\
Val Levitan** 51:54\
Attitude, attitude.

**\
Clayton Chancey** 52:01\
That integration from Jira to GitHub is like just setting a custom field our and and the GitHub pipelines connectors and all of that which can be just wired to Jira.\
Will automatically do that. So if the MCP is creating Jira tickets correctly, then that just happens by nature. Everything you describe would happen by nature of the integration between Jira and GitHub.

**\
Val Levitan** 52:30\
I just want to align us further. As Lena opens stories under a feature, the completion of a story is a result of some sort of an artifact under that particular feature branch within the GitHub.

**\
Clayton Chancey** 52:49\
Yeah. So all of that, all of that, that logic is governed by the GitHub JIRA integration and the yes in the future and and so that\'s actually a good way to contextualize our current work to that is to say we need to make sure that this MCP.

**\
Val Levitan** 52:57\
Correct in the in the future.

**\
Clayton Chancey** 53:09\
Is making those stories rich and accurate so that when those integrations fire the the artifacts that are stored automatically and pushed to GitHub and version control are actually the right ones. And so that\'s yeah.

**\
Val Levitan** 53:21\
And this is actually and and the difference is is to shifting away from understanding a story is A to do list versus a story is an applicable.\
Uh, next reiteration of an artifact.

**\
Clayton Chancey** 53:42\
Yeah, it\'s a deliverable.

**\
Val Levitan** 53:44\
It\'s a deliverable, yeah.

**\
Clayton Chancey** 53:45\
Yeah, yeah, yeah.

**\
Lena Zhukova** 53:47\
Clayton, I also wanted to ask you why?\
Probably I needed to mention in front, but why? When it created features and stories, Claude did not like UMCP did not make any assignments because in plan like which we created, it was clear that he understood.\
Understood that for example like illustration should be assigned to Anton Regionov for example and dragon animation should be assigned to Dima Khandov. It was clear that he read it properly from the transcript, but it didn\'t do it when it created so.

**\
Clayton Chancey** 54:17\
Mm-hmm.\
Well.

**\
Lena Zhukova** 54:32\
Everything is unassigned.

**\
Clayton Chancey** 54:33\
That\'s because we\'re in the sandbox here for testing. I don\'t think those people exist here.

**\
Lena Zhukova** 54:39\
Um, I see.

**\
Clayton Chancey** 54:41\
Yeah, so that\'s why it did assign you because you exist. But I you know this this.

**\
Lena Zhukova** 54:45\
Uh huh. So should they add them? So should they add them for sake of experiment or?

**\
Clayton Chancey** 54:54\
If you want to, they will probably get a bunch of emails and stuff. I personally, I think Andrei created this like just for us because I think we\'re the only people in there. So I would personally.

**\
Lena Zhukova** 54:58\
Uh, OK, I see.

**\
Clayton Chancey** 55:09\
Not worry about it until. I mean, we know that it assigned some things correctly and we know that it it probably tried and can\'t find those people and didn\'t. So I\'m personally not concerned about it, but if you wanted to validate it then you could add maybe one or two extra.

**\
Lena Zhukova** 55:12\
And.\
Uh huh.\
I see, I see.

**\
Clayton Chancey** 55:28\
People to see if it if it does actually assign those things diversely, and that would be a way to prove that. But that is why it\'s not assigning those is because the actual instance that we\'re writing to is the sandbox, you know.

**\
Lena Zhukova** 55:39\
Yeah, thank you for explaining it. Yeah, it\'s it. Yeah, it it\'s fair. It makes sense.

**\
Clayton Chancey** 55:44\
\'Cause obviously we don\'t. Yeah, we don\'t wanna test this in production \'cause it\'ll blow everything up, but.\
Yep.\
OK, cool. We\'re aligned. We have the whole meeting has been recorded, transcribed. I owe you guys some some things. And then Aaron, you and I are.\
Talking, hanging out anyway, so we will work on the whisper thing a little bit for maybe an hour at some point.

**\
Aaron Bockelie** 56:09\
Yep.

**\
Lena Zhukova** 56:09\
OK.

**\
Aaron Bockelie** 56:13\
Yeah.

**\
Val Levitan** 56:15\
Bye bye guys.

**\
Aaron Bockelie** 56:16\
Alright, thanks. Bye.

**\
Clayton Chancey** 56:16\
Sweet. Thanks. See you guys.

**\
Lena Zhukova** 56:17\
Bye. Thank you.

**\
Clayton Chancey** stopped transcription
