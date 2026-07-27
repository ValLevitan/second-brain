**Aaron_Val-release_procedure_GitHub-March-16-2026-20260316_082125-Meeting Recording**

16 March 2026, 12:21pm

4m 52s

**\
Aaron Bockelie** 0:03\
I\'ve reviewed both the JVL Administration Documentation Guide and the JVL Engineering Documentation Guide, and I have a few bits of feedback for both of these. First of all, I actually really like the part where we\'ve mentioned capabilities.\
And I like that we\'re talking about tying capabilities to requirements and that we\'re making some hard rules about what it is and is not. However, I am going to take issue and sort of pivot on something I had recommended to Val earlier, which was that maybe we should keep capabilities inside of GitHub.\
I\'ve looking at this and the way it\'s described and structured is pretty pretty makes a lot of sense, but I think that I\'m going to push back on the part where we keep capabilities in the GitHub in GitHub.\
Or in the git repo, because we\'re already mentioning in the administration document that we\'re tracking capabilities with literally a three letter code of CAP and a number, and we\'re saying that they need to be tied to requirements.\
That sounds a whole lot like a JIRA issue, not something we keep in GitHub. The reason I\'m saying this is that there\'s no while we can keep track of exactly where a documentation such as CAP 123 inside of.\
GitHub as a markdown document. There\'s no way to verify referential integrity of the document to the requirement. You can\'t enforce it. So I think what we\'re going to do is we\'re going to use JIRA as essentially just a tool to maintain referential integrity through.\
To issue links. This means that requirements can use issue links to capabilities and capabilities can match to requirements and this forms a network of the two. This also means that in some future state when we abandon JIRA for our own issue tracker or something else.\
We will have a well referenced body of data for both requirements and capabilities, which they themselves, according to the administration document, don\'t need to get into architecture. The ADRS, they still live inside of the git repo and the ADRS can reference the codes that are in.\
So this means ADRS can be composed from both requirements and capabilities. This way we keep the links in the ADR that are in git back to the capabilities and requirements that are in JIRA.\
And allows us to process those. Otherwise what will happen is the non-technical people who are choosing capability issues will have to deal with all the git repos, which will add a lot of confusion. So I\'m thinking of Juan and others who have would have to work in git.\
The other thing that is the capability drafting prompt mentions sequential numbering, which is exactly what JIRA does, so why not put that into JIRA? Other than that, I think the other rules about AI first, let\'s just make sure what AI first is defined clearly. It\'s not a I only.\
And we don\'t just let AI do the thinking for us. It is collaborate with AI where we back and forth a few times till we\'re both satisfied with the output. Because at the end of the day, machines cannot make decisions, people make decisions and we have to let the people accept the conversation that happened with between.\
An AI and a person. So any PR, any project requirement, any capability, any ADR, all of these need to be authored with AI and can be cleaned up and referenced and originated.\
But they need to be read by the people and they need to be accepted by the people before moving on. So I\'ll that I will also admit one last thing is that this process of review of both requirements and capabilities and architectural decision records.\
By humans will be difficult from a cognitive standpoint, simply because AI systems are capable of producing lots and lots of content. So it\'s going to be JVL\'s goal to maintain.

**\
Val Levitan** 4:29\
OK.

**\
Val Levitan** stopped transcription
