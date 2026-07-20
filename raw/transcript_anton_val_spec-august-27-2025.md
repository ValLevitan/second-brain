Val:

Hi Anton
 
How are you?
 
I have a question
 
Anton:
Good morning
 
doing great, thanks?
how are you?
 
Val:
If I asked you to create a spec for something that you are about to code, would you know what I am asking for? Do you understand my question?
 
Anton:
I think I do
In my understanding that would be a technical specification of a feature im about to code, listing the following:
Technologies (e.g. frameworks, programming languages etc)
Technical approach (e.g. network protocols and API specs)
List of the system components, changes to them and how a feature would interact with them.
And possibly other things depending on the task
 
Val:
do I understand this matter correctly: "There is NO WAY that you or any other developer can actually code a feature without a spec?"  Granted - currently we do not have written specifications, however each developer will make up a specification as they go along a project; otherwise, it is not possible to code.  In other words, I am suggesting that currently this spec is a tribal knowledge.
Am I thinking correctly or erroneously about this subject?
 
Anton:
In theory this is how it should be, and ideally every tech spec should be reviewed before actually implementing the feature. As of now, we miss this steps and yes, it results in a Huge amount of tribal knowledge

Val:
ok, this is clear to me, however, I am asserting that despite that we do not have a written spec we have the spec in our minds.  I am further hypothesizing that without a spec (be it now in the minds of the developers) it is impossible to code a software.

Anton:
Again, I cannot say that is it impossible to write a code without specs, but having specs and documentation helps tremendously. 
 
For example, in the NAD project I had to work with the module that interprets math engine messages. When Valentin left, he left some documentation on the subject, but a lot of sub-modules do not have documentation. As a result, I added a new module in order to support NAD bonus games, and as I was done, I've noticed, that my code partially resembles already existing code. So theoretically, instead of creating new code I could've extended an already existing module to support the required functionality. If I had more information (docs & specs) I probably would've done it, but since those are very critical pieces of code I decided not to risk it.

Val:
I want drill down on this part of your answer: "Again, I cannot say that is it impossible to write a code without specs, but having specs and documentation helps tremendously."
How can a developer write a code without having a spec?
Please let me be clear.  I am actually playing out an active scenario: "You know what I need you to make" - "How would you know how to make it?" without imagining your own version of a spec?
I am asserting that you cannot possibly write any code if you do not know "HOW" you will code it.  I am asserting that "HOW" is a form of a tribal spec.

Val Levitan
I want drill down on this part of your answer: "Again, I cannot say that is it impossible to write a code without specs, but having specs and documentation helps tremendously."     How can a developer write a code without having a spec?     Please let me be clear.  I am actually playing out an acti…

Anton:
I understand now. 
Yes, that is impossible, especially if a developer is new to the project.
The only way is to spend a lot of times trying to decipher the project's code and from personal experience I can say that it takes a LOT of time.
It took me at least a year to become comfortable making changes to our v100 framework and still, there are certain areas which I havent worked with.

Val:
You still do not fully understand my question.
Let me try again.
I am speculating (asserting) that if I asked you to develop a certain feature of a product that you are already familiar with; in other words, if I explained to you in a verbal presentation of “WHAT” I want the feature to do and asked you to code this feature for me, you would go away and THINK “HOW” you could code it in a away that would satisfy my “WHAT” I needed that feature to do.
This process of you going away and thinking would in fact be - you were spec-ing the “HOW” in your mind before you could actually start keying the code.

Anton:
Yes, pretty much so.

Val:
So if after you had thought about it; if I sat you down in front of another, equally knowledgeable developer like yourself (for example, if I sat you down with Biratka) and asked you to explain the “HOW” - and recorded your discussion with Biratka and then asked an AI to interpret this discussion in a Format of a written spec - it would most likely come close enough for the first draft.
Assuming that I would then allow you and Biratka to comment on that draft again - I would most likely come very close to a spec Ina few reiteration.

Anton:
Yeah.
 
 
