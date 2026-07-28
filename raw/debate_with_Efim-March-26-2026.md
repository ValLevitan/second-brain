Efim
 
I have a few questions, if I may, please.
 
I understand that the Math engine for OMNI is written in C++
 
Is that correct?
 
Did you have a say in it?
Did you chose to have it written in C++?
Why did you make a choice to write in C++ if this was a choice?
 
Thank you.  I look forward to your reply.
 
Math Engine for OMNI is the same as our Math Engine for Rage or RGS. It is  written in C++ because it was started like 10 yes ago.  I think it was a good choice then, either that or Java. No Rust would be preferrable, but we have path dependency
 
How much code is in math engine?
 
Does it have to be C++ because MATH NEEDS it?
 
On the second question - I think it should be a language with solid type checks and  object-oriented capabilities. Wouldn't touch Python for it. Java, Rust would be good too. C++ was chosen over Java back than because it supposed to be faster, but this isn't critical. 
 
on the first question ~50k lines of code
 
Did you realize that the new system (OMNI) will have 5 languages?
 
I wasn't aware that it is 5
 
but other members of the team do not touch Math Engine anyway. How would unification help? 
 
... where if we were thinking about it correctly from the start it could have been 3 languages only:
C - Drivers
Js for framework and Games and LGS
Java for math
 
Efim Podvoiski
but other members of the team do not touch Math Engine anyway. How would unification help?
I think the problem is the run-in programming standards between languages.  The guardrails for each language is  different (as I read it) 
 
 
 
Have you ever thought about these things while architecting the las systems?
 Old System (In the Field Now)
Component	Language	
 

Framework	C++	
 

DataCenter	JavaScript	
 

HAL / Drivers	Presumably C/C++	
 

SAS	Protocol, not a component	
 
The fact that the DC is JavaScript talking to a C++ Framework across a socket boundary is significant. These two languages have completely different concurrency models — C++ uses threads and shared memory, JavaScript is single-threaded with an event loop. The "dead socket" freeze in Georgia makes sense in this context: the C++ Framework is likely blocking on a synchronous socket call waiting for a response from a JS process that is either stuck in its event loop or has crashed. C++ will wait forever unless you've coded an explicit timeout. JS won't tell you it's stuck because there's no second thread to notice.
There is no unified coding standard that spans both. The contract between them — the socket protocol, message format, timeouts — is the only thing that can enforce discipline at that boundary. Which is exactly what your initiative identified.
 
 
Is what I am learning now make sense or not?
 
To a non-engineer like myself this is very telling and very logical...  Perhaps I am just fascinated with it as a conspiracy novel...???  That could be.
 
I don't believe that C++ is talking to JS in setup via socket. 
 
No it does not
 
I did not say that
 
Framework C++ is talking to Java in DC via http. Setup has some callbacks to Framework to play sound as far as I remember, not even sure it is the case now. 
 
I simply asked for the reason that Math must be written in C++, adding yet another standard to the system's architecture
 
if they don't talk why do we care 
 
If you do not understand - I do not want to talk to you, because you do not add any value to me
 
I thought that I was very clear
 
Each language = to a programming standards
 
each programming standards must coexist with a next programming standards
 
even a child can understand it
 
coexist in which sense?
 
they exist under the same roof.
 
same system that co-exists (functions) to perform tasks
 
but if they interact via clear http protocol, what does it matter?
 
that why client-server architecture exists
 
DC is JavaScript talking to a C++ Framework
 
Is this not the case in RAGE?
 
Java, not JS. 
 
and again talking via http
 
DC and Framework communicate over http?
 
yes
 
in the new system or in RAGE?
 
in the RAGE
 
but in OMNI, I suppose, too. 
 
actually I believe, not suppose. 
 
 
 HTTP doesn't save you automatically. It gives you the mechanism for timeouts, but if nobody configured them — or if the C++ side is using a raw socket wrapped in minimal HTTP parsing rather than a proper HTTP client — you're in the same position as a bare socket. The machine freezes waiting for a response that never comes.
What the Georgia Overnight Freeze Likely Looks Like
DC (Java) stops responding — GC pause, thread deadlock, crash, doesn't matter
Framework (C++) has an open HTTP connection to DC
Framework sends a request (or is waiting for a response from a previous one)
TCP connection is still technically open — the OS hasn't closed it, DC's JVM may still be running
HTTP read blocks. No response timeout configured. Framework thread hangs.
No monitoring daemon to notice. No heartbeat. Machine found frozen the next morning.
The fix is the same regardless of protocol: AC-1 demands a contract that specifies the expected response time and what happens when it's violated. For HTTP specifically, that means:
Explicit connection timeout (e.g. 3 seconds)
Explicit response timeout (e.g. 5 seconds)
Defined retry/recovery behavior when a timeout fires
The Framework must never make a blocking HTTP call with no timeout on the thread that governs machine state
Is this something Pavel and Alexander can confirm — whether the HTTP client on the C++ side has explicit timeouts configured?
 
I believe that HTTP client on C++ did not configure timeouts. Was this a wrong decision? It was done in the assumption that 
1) if DC is not responding we can't proceed anyway
2) we have watchdog controlled by framework, so when framework stuck waiting for DC we will reboot anyway 
 
3) DC being stuck is much less probable that any other cause of Framework being stuck
 
In any case, honestly, I don't see this as a problem of having two different languages. 
 
We should not be mixing up watchdog and design standards. Watchdog is the suspenders. Design standards is a belt. 

Belt and suspenders = safety.
 
You are right. 
 
Anyways - all of this is not a point
 
The point is - more languages = more design standards = more incompatibility to deal with
 
Efim,
 
I was very efficient in developing personas with Claude MPC using Cline in Visual Studio Code and ChatGPT
 
It is on Visual Studio Code
 
I don't agree. Are we talking about organisational, human resources issues - like all people don't know all the languages? I think not, just to confirm?
 
If we are talking about pure architecture, breaking the system into units that use well defined interfaces to talk to each other is good. As these interfaces are language-agnostic having these units implemented in different languages is irrelevant. Using the best fitting language for each part is an advantage. 
That said, must Math Engine be in C++? - no. Java or Rust could be a better choice if we do it from scratch. 
But is it an architecture  problem on its own - having it in C++ when LGS is (I guess) in Java? - I think the answer is a clear no.
 
Efim Podvoiski
I don't agree. Are we talking about organisational, human resources issues - like all people don't know all the languages? I think not, just to confirm?
I do not understand this at all.  I have no idea what this means
 
.
 
sorry - we are talking about a design of a system that has the highest probability of working without being out of service in locations that are unattended
 
a machine that breaks down in an unattended location is WORTHLESS.
 
I can only repeat - aligning the languages is not relevant at all. 
 
I CANNOT BE further apart from you on this - and this is disapointing
 
imagine our RAGE case. say DC done in C++ and we talk through direct calls. DC is "broken". The system is still dead blocked on DC call
 
 
DO you realize that you are replying to a wrong set of questions?
 
 
 I would like to understand where exactly we disagree. Let's do it in steps. 
Do you agree that as we have a few well-defined modules (Game (aka client, aka framework), LGS, Setup, Math Engine, Progressive Controller) each having its own functions, it makes sense to keep them in independent compartments (dockers)  and make them to communicate with each other via well defined http interfaces?   
 
first of all - are you referring to RAGE or OMNI?
 
OMNI
 
Efim Podvoiski
I would like to understand where exactly we disagree. Let's do it in steps. Do you agree that as we have a few well-defined modules (Game (aka client, aka framework), LGS, Setup, Math Engine, Progres…
yes
 
as a matter of fact - I like that
 
it has nothing to do with what I am discussing
 
So, we have units which know nothing about each other, only which requests can be sent and how to prepare data for these requests, and how the response will look. Correct?
 
This is not the point
 
To me it is the point. The is no place for different programming languages to influence this communication.
 
I am not certain about it
 
why? 
 
because each language has its own design intricacies (specifications).
 
In example - each language would manifest its own malfunctioning differently; and the next language would not know how to deal with it.
 
 
the units are black boxes to each other. All they know are how to send json messages.  
 
Now too?
 
in RAGE this is also the case?
 
In RAGE it is different. 
 
Math Engine talks to Framework directly
 
so you see the problem I am raising in RAGE,  But you are saying that this problem cannot happen in OMNI?
 
But Framework ->DC DC->Setup are like this
 
I don't see an absence of timeout for communication from Framework to DC  in RAGE as growing from having different languages. I am not sure that you mean exactly this problem. 
 
